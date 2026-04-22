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
-	[`memcached:1.6.41`](#memcached1641)
-	[`memcached:1.6.41-alpine`](#memcached1641-alpine)
-	[`memcached:1.6.41-alpine3.23`](#memcached1641-alpine323)
-	[`memcached:1.6.41-trixie`](#memcached1641-trixie)
-	[`memcached:alpine`](#memcachedalpine)
-	[`memcached:alpine3.23`](#memcachedalpine323)
-	[`memcached:latest`](#memcachedlatest)
-	[`memcached:trixie`](#memcachedtrixie)

## `memcached:1`

```console
$ docker pull memcached@sha256:277e0c4f249b118e95ab10e535bae2fa1af772271d9152f3468e58d59348db56
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
$ docker pull memcached@sha256:518f136cafc43439a777c20224d30b6fadc3433e3de9573f514dca10dd7e0082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32198630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ec7b3eba028951d3aeee1ef26a365c913edaf06de6c008653f175c0ff0078ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:21:37 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 22 Apr 2026 01:21:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:24:27 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 22 Apr 2026 01:24:27 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 22 Apr 2026 01:24:27 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 22 Apr 2026 01:24:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 22 Apr 2026 01:24:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:24:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:24:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:24:27 GMT
USER memcache
# Wed, 22 Apr 2026 01:24:27 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 Apr 2026 01:24:27 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53e27a8dc2608bcd39496d6e1a0a021aa8933953409444f778d810ec220ab89`  
		Last Modified: Wed, 22 Apr 2026 01:24:33 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d02c07f7ffb4ea4d70b3af1ed59da72e778c143718ba2a7bcb8cd6d12afd95b`  
		Last Modified: Wed, 22 Apr 2026 01:24:33 GMT  
		Size: 136.7 KB (136658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b1a619145ef14a0e4599b98a19dbdc4fc96cfdf359ecf816454cd80ccf2dd2`  
		Last Modified: Wed, 22 Apr 2026 01:24:34 GMT  
		Size: 2.3 MB (2280287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7716efee154a639ac02ada0d1638837bb72c3fc33ecac40f78ffb91daf9dfc5`  
		Last Modified: Wed, 22 Apr 2026 01:24:34 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712f24abcdc2a432d57253a569a16eddd36ff1f8a4ace323467cdb642eae2850`  
		Last Modified: Wed, 22 Apr 2026 01:24:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:f32546667bf4926fd4e7c91aa55a833e8636777f2aa68437cb2bc7a5330e2307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3700c2c8b8182ac20db287282cdafbde42f55966784e109b48a9e5c2ba4d7492`

```dockerfile
```

-	Layers:
	-	`sha256:a3fe3f55746c35c0a798536b5abfc78349217684ca67ba43649a1c86d2a6ebe3`  
		Last Modified: Wed, 22 Apr 2026 01:24:33 GMT  
		Size: 2.0 MB (2008326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0b151a6f180676864b1e8721dddbaf0c105e743520356d58f7df86572a295fa`  
		Last Modified: Wed, 22 Apr 2026 01:24:33 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm variant v5

```console
$ docker pull memcached@sha256:4b91aeabb9b5d253e27cc0e6f6fa6cc82780c4d686f484c9ed1057a1dd429ba2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30305389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e62e4552c0bfc9dd8f4797df2c1386943df5780d342654ed3050e75668231e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:17:31 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 22 Apr 2026 01:17:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:20:57 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 22 Apr 2026 01:20:57 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 22 Apr 2026 01:20:57 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 22 Apr 2026 01:20:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 22 Apr 2026 01:20:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:20:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:20:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:20:57 GMT
USER memcache
# Wed, 22 Apr 2026 01:20:57 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 Apr 2026 01:20:57 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6496d93bca0663211b9252da346044ecb734ee5b3ecaae5b1fbd230753faee2f`  
		Last Modified: Wed, 22 Apr 2026 00:15:59 GMT  
		Size: 27.9 MB (27948180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64cdc01a23d15e84ef2ee2165c1a90970fb54d98f29377fa63fbd82988cdcc40`  
		Last Modified: Wed, 22 Apr 2026 01:21:03 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:303fc6e2ad4e0da497f7e238e61ec9e1fbde60909262de4a50e05c4db2191602`  
		Last Modified: Wed, 22 Apr 2026 01:21:03 GMT  
		Size: 144.2 KB (144163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c438ec3169ba426bc8374ca37b4f159272d50b60173c35c396f8fbf2208b8806`  
		Last Modified: Wed, 22 Apr 2026 01:21:03 GMT  
		Size: 2.2 MB (2211533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b5512f6aab6e3147798ce406f1035f68f18c2dd046b5fdd6344a17ace7fb31`  
		Last Modified: Wed, 22 Apr 2026 01:21:03 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a320e8acb7760a30eb688cd929fda03bf41ba23a307e06071106c3c0415d03`  
		Last Modified: Wed, 22 Apr 2026 01:21:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:4faa0397c26f0f4a312a28578db40b0f95f89c09769520c7cc09900886412dd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af54d9e6dbb4f86d5a79e417071faea8dd939b7758f640ce360a49c55069e2eb`

```dockerfile
```

-	Layers:
	-	`sha256:1850a912cc062cca1f70a2b76861d54c0ad06921d2a4960a7c483b5f8820eaa1`  
		Last Modified: Wed, 22 Apr 2026 01:21:03 GMT  
		Size: 2.0 MB (2011329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02fdad23f354f6597bfec3258d6bbee5142bcce9e1faaa7de87f9859bf8c6d14`  
		Last Modified: Wed, 22 Apr 2026 01:21:03 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm variant v7

```console
$ docker pull memcached@sha256:4d262b60fea5a97e91a6c1827ab7209a344c47616388ada79b27e4e69eea9d38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28516774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02f2f7426f06caeeb218b724a947fa35544b0749bacf781227878e40cb98d08f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:18:06 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 22 Apr 2026 01:18:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:21:19 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 22 Apr 2026 01:21:19 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 22 Apr 2026 01:21:19 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 22 Apr 2026 01:21:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 22 Apr 2026 01:21:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:21:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:21:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:21:19 GMT
USER memcache
# Wed, 22 Apr 2026 01:21:19 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 Apr 2026 01:21:19 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9e541e5bfbbe69b7bbe01cd2f1abf8560e2e43bf76eb96b2e88a3df29020834b`  
		Last Modified: Wed, 22 Apr 2026 00:17:02 GMT  
		Size: 26.2 MB (26214838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0867e20c7ab47539b3f27abc4c7f4bf41d367127d9ffbd30a531ab387a69e2e`  
		Last Modified: Wed, 22 Apr 2026 01:21:25 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34eedf23d5ae4af59fe6ecfd854e48545ede507ce44d930cea5c11b652b31f4`  
		Last Modified: Wed, 22 Apr 2026 01:21:25 GMT  
		Size: 135.4 KB (135382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fff54fd1447de9c8b377640a2720588785769320b1a65d59a1da8e9690e6f9`  
		Last Modified: Wed, 22 Apr 2026 01:21:25 GMT  
		Size: 2.2 MB (2165043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac214a1bada6a999cda6b6b021b8ef5ba954108062e3ee4df0161a500fc566f`  
		Last Modified: Wed, 22 Apr 2026 01:21:25 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0431aacefa9d6f210c7c4778e75df5a21c196127779acc2da1bd7b32088f47dc`  
		Last Modified: Wed, 22 Apr 2026 01:21:26 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:e4f840cb65bd892b2aafc305cb008de10d4d41475876ef9c9bbf51831f9cd7e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:987452d71cfba90bac820fca09f2954a061813125a8832038df5c062224577c5`

```dockerfile
```

-	Layers:
	-	`sha256:f5793a9489c1e1010726124554d7404a19b2675ce8596a38169b160edc81d045`  
		Last Modified: Wed, 22 Apr 2026 01:21:25 GMT  
		Size: 2.0 MB (2009786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef3c23077c5adc1a06a0e1f66d0ec1e57032a5b35685c53064098e236a62c5a1`  
		Last Modified: Wed, 22 Apr 2026 01:21:25 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:52e2a52a542b0fff64533e7271ce3af9825a80a1126998cf6070b0ec4c0030b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32560736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c3fcfefa704f0162e85ab03d515502e07a6ff91ec994dc4b6c956cc2ce80990`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:22:08 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 22 Apr 2026 01:22:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:25:10 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 22 Apr 2026 01:25:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 22 Apr 2026 01:25:10 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 22 Apr 2026 01:25:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 22 Apr 2026 01:25:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:25:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:25:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:25:10 GMT
USER memcache
# Wed, 22 Apr 2026 01:25:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 Apr 2026 01:25:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebea5231ebe63bff9044a4ee7713dac1b62fc15d85ee920f04eae4010a67b668`  
		Last Modified: Wed, 22 Apr 2026 01:25:16 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5921030f644563277c2af1be27b21dfded0e01763210710efac613f07dc74c`  
		Last Modified: Wed, 22 Apr 2026 01:25:16 GMT  
		Size: 153.5 KB (153515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1ef7f1deafd8e81fec98af35ef4fe12c2436c1eddb6bb87377b83f524f7d6f`  
		Last Modified: Wed, 22 Apr 2026 01:25:16 GMT  
		Size: 2.3 MB (2262106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd4f58ffc6f10cea1171fbb552aff0b93a04aba0ca6815cd9ad66ab3a49f8419`  
		Last Modified: Wed, 22 Apr 2026 01:25:16 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace7ea462603345a875235135df0b8dd036890eacdb25150c1a8089604e3ca1f`  
		Last Modified: Wed, 22 Apr 2026 01:25:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:63aba0d160ad2159dd41a074d79446fc4ba2e745c7e5a10a41dbd1d5c2abc86d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b67f2365f86c60d496eb140fde16a0d6fbf89ae6a83d200c6a3971e32eca706b`

```dockerfile
```

-	Layers:
	-	`sha256:e87d247df404b9fe7e19667c95311e8109ea54acdcca2f52ceba73b7099d144e`  
		Last Modified: Wed, 22 Apr 2026 01:25:16 GMT  
		Size: 2.0 MB (2008642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5290960be9e7480bf28bf59599ba02b7792ea80b3309570c3b3a24465ad7d58`  
		Last Modified: Wed, 22 Apr 2026 01:25:16 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; 386

```console
$ docker pull memcached@sha256:0b8f07a6f169bfe4cc362cbabca8c92d5140665660c615383f2755c40c0036f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33670125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd6a79877127262a308ef5f3bd216749c6f0b1fc43971b56c533d4e47f5c6de2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:17:33 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 22 Apr 2026 01:17:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:20:28 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 22 Apr 2026 01:20:28 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 22 Apr 2026 01:20:28 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 22 Apr 2026 01:20:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 22 Apr 2026 01:20:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:20:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:20:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:20:28 GMT
USER memcache
# Wed, 22 Apr 2026 01:20:28 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 Apr 2026 01:20:28 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:dacd7cda306bf5bd7a2030f9b0c2e9d71fda44ea58493a33450d210b74a8ec75`  
		Last Modified: Wed, 22 Apr 2026 00:17:04 GMT  
		Size: 31.3 MB (31296327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a0c9fe363e7e198726a5e39cf627131e43cd59d319a350f978180f6f449b8a`  
		Last Modified: Wed, 22 Apr 2026 01:20:34 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dff2976b24139841065357d1f81c8cf6d9b45ee35e2947f1345e86493b2f5e67`  
		Last Modified: Wed, 22 Apr 2026 01:20:34 GMT  
		Size: 147.5 KB (147529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8b8718f120acc0033835790e0bd541e38b843c6b260688b8fde3c94eadd5911`  
		Last Modified: Wed, 22 Apr 2026 01:20:34 GMT  
		Size: 2.2 MB (2224758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f70ea447cee314191f67e0ce5ccc23703730c89810e26bfa3f96f81964849dc`  
		Last Modified: Wed, 22 Apr 2026 01:20:34 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:789bc1b0beaaf9809e3cab832a0b6b29f50aec3b18f7a7cdf04e343d3ee800a3`  
		Last Modified: Wed, 22 Apr 2026 01:20:35 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:45cfea0c565e5e6c79f4a36cf4ec611ccc7e910c481110b37be04eca3276511b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d33423fad9c4c2f3b1af3eb87b8af48d7cfc9e00d70e6c33937d7d215fb94c5`

```dockerfile
```

-	Layers:
	-	`sha256:2656e01c20323e582a0ba03c06d82008eb35ae9850f7d6c7f73c0e5ae040805b`  
		Last Modified: Wed, 22 Apr 2026 01:20:34 GMT  
		Size: 2.0 MB (2005483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d267990174d3038591d6a8ffe07af06d961bb5c68b86a9cdac459f5a0996ddbe`  
		Last Modified: Wed, 22 Apr 2026 01:20:34 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; ppc64le

```console
$ docker pull memcached@sha256:3df945008f026e1a7782fc67d0107a07c9103d9d50dd7ae605082ea97fb64ff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36164269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7eb2db1cbb0c7ddc2688ee498498fb5122ee78ab349b636a43585b1beb30da9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:35:49 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 22 Apr 2026 01:35:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:39:22 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 22 Apr 2026 01:39:22 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 22 Apr 2026 01:39:22 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 22 Apr 2026 01:39:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 22 Apr 2026 01:39:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:39:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:39:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:39:23 GMT
USER memcache
# Wed, 22 Apr 2026 01:39:23 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 Apr 2026 01:39:23 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b5fd051d0fcd0789e7358cba300f83befdba943416041497be86050e282a6d02`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 33.6 MB (33598032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e271c91c5c30b04dee49fb4c9ab2f9863d13146641f1b8681b59467d0f8ab5`  
		Last Modified: Wed, 22 Apr 2026 01:39:42 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb7fa3c8c45f87e36929f71acaead9bcb07985c205ea0aa6fd83aca31691d78`  
		Last Modified: Wed, 22 Apr 2026 01:39:42 GMT  
		Size: 170.4 KB (170378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f09610f9abffbf6411865ebc07ee20de6c14b2250467c4682f423dddc0ab82`  
		Last Modified: Wed, 22 Apr 2026 01:39:42 GMT  
		Size: 2.4 MB (2394347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a0fb856cc435334489ebeec58afd76f4e676c8bae4b3688daefedfbc7f7c1a8`  
		Last Modified: Wed, 22 Apr 2026 01:39:42 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea36b259fc26e36b99ded4a3aa0ca190c1117ecd424f26565f8474b55964d787`  
		Last Modified: Wed, 22 Apr 2026 01:39:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:c619fe6b2206166796157b814c0d60ca38e29a646b71cd6f5635e2f507cf70d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49e66f35bf963d54f332469bbdef0ca608c651311f5af0e923aca630f4429ae9`

```dockerfile
```

-	Layers:
	-	`sha256:f870fab207e6594315e4d18f50f3ebf834ebc298b6ec128104607668ae939995`  
		Last Modified: Wed, 22 Apr 2026 01:39:42 GMT  
		Size: 2.0 MB (2011927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bf20b8b72f84425e9121a35ea191dab3cf17562679390195740f260304727d7`  
		Last Modified: Wed, 22 Apr 2026 01:39:42 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; riscv64

```console
$ docker pull memcached@sha256:5554043a87027cff145bdb04810a9f8a067c72479937ce0328af056a5c3efe8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30623256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad08d83e675d61f6e230bee3e1d5d5e4b4e8d0b1b3656b71812168b7db5e08e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 08:28:54 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 22 Apr 2026 08:29:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 08:55:11 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 22 Apr 2026 08:55:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 22 Apr 2026 08:55:11 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 22 Apr 2026 08:55:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 22 Apr 2026 08:55:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 08:55:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 08:55:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 08:55:12 GMT
USER memcache
# Wed, 22 Apr 2026 08:55:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 Apr 2026 08:55:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8aa73197c6983c411cf26b41c64a557cfc81f9b4e6d897ff2829a66eac03b37`  
		Last Modified: Wed, 22 Apr 2026 08:55:56 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee379d85ef42145b3f09328c98634e8cd3320230281217ad58867c6982e1d8c`  
		Last Modified: Wed, 22 Apr 2026 08:55:57 GMT  
		Size: 133.1 KB (133094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:310a92cbf1cb95664c58022062af028a81e69f127cd8d9ee044bf7d5087db961`  
		Last Modified: Wed, 22 Apr 2026 08:55:57 GMT  
		Size: 2.2 MB (2208455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336575624802c397f4947f3ddfc2737281bfe2ba8cd714be646b72152c1ec1d0`  
		Last Modified: Wed, 22 Apr 2026 08:55:56 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e926175ab529d298755a0e0507accca74feec6c90ea4495edeaafb07954ad57d`  
		Last Modified: Wed, 22 Apr 2026 08:55:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:9b8b4751f5823830cf382050f0174dd5ade6dc0650b2a3134803b886b2652dba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bc1698424d742c630d5a555fa2c70be3195da5b1a2cd148a331c7aa9fb94b6f`

```dockerfile
```

-	Layers:
	-	`sha256:18aa82332065ff68528148bb97bd5681424d4c57e9e5e331b8908b44023570a9`  
		Last Modified: Wed, 22 Apr 2026 08:55:57 GMT  
		Size: 2.0 MB (2002290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edeefd058e4dbdf6c3026618be5f5184cd3d2c22f14746d890cd45a42004dc8f`  
		Last Modified: Wed, 22 Apr 2026 08:55:57 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; s390x

```console
$ docker pull memcached@sha256:e0fadaa0ad7c323c4f8ead5d8e1ebb9566adc59b25cbc280f40bef816f9d62eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32280559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5d7f2d629511f566dd7c4b3a944adb9989b05bb41dbd3e3881734bc1c1079c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:19:00 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 22 Apr 2026 01:19:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:22:27 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 22 Apr 2026 01:22:27 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 22 Apr 2026 01:22:27 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 22 Apr 2026 01:22:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 22 Apr 2026 01:22:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:22:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:22:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:22:27 GMT
USER memcache
# Wed, 22 Apr 2026 01:22:27 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 Apr 2026 01:22:27 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:71574deb335f1e823f938f4a215de00a90d63866898f1f354a0b15e8b9c30577`  
		Last Modified: Wed, 22 Apr 2026 00:17:08 GMT  
		Size: 29.8 MB (29840300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b460058bd06ca18e629070cadcc158edef16e034340796f661d4fab362ee94`  
		Last Modified: Wed, 22 Apr 2026 01:22:38 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5386c57fa90d49931296cf79f5e8d2ae18d07b9bcffe5eee8354033fee4b673`  
		Last Modified: Wed, 22 Apr 2026 01:22:38 GMT  
		Size: 140.5 KB (140521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd8308c0fc0224d29acef5aadae977dfea2e1ba7c9be0e207ee89c84a4f6417`  
		Last Modified: Wed, 22 Apr 2026 01:22:38 GMT  
		Size: 2.3 MB (2298228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fda405f0b2226447c88ba0d395ee00616ec775cecba66d9a980d4aac7b44fb49`  
		Last Modified: Wed, 22 Apr 2026 01:22:38 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fcaa079ef0e24aab0065df6b15e28d19a0807e2c9cdc639bbc63923135e6daa`  
		Last Modified: Wed, 22 Apr 2026 01:22:39 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:7d2e45f2ecd9448a99f98a077da16fb59c37827c2acbac9e99dea8f79d753165
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54358ef5a62ded9fafc9e908e79d81e5d01102cd4f2082017f54d92232acb7c4`

```dockerfile
```

-	Layers:
	-	`sha256:eb9c1105cc4bf8d4cf2089f7a2a43afe0a113388e7f5a4af9db1f44f9f0fbe11`  
		Last Modified: Wed, 22 Apr 2026 01:22:38 GMT  
		Size: 2.0 MB (2009763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af1c4a20085e6a6f3d2b2fcb2ce9c10456d057c6905b84fe6ad6d99ba351a872`  
		Last Modified: Wed, 22 Apr 2026 01:22:38 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine`

```console
$ docker pull memcached@sha256:65c80b311a9601ef5ca8af3814e5cd06a9c4277ea139d80bd53da6b4d39eb46e
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
$ docker pull memcached@sha256:7b962825022657b112923d502400d5734870d5eb12c19e7f1f6585f7534a6795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5959872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b58f7e71f30daaa3f466fa31d855fddb7101e42c0c42fac520be5d1d43ec32e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:46 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:17:47 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:20:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:20:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:20:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:20:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:20:22 GMT
USER memcache
# Wed, 15 Apr 2026 20:20:22 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:20:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73d5ffe265b83073ce3c7211fb3c15ebbd5e7146d870d9ce69d2e7dfc493348`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6cb4fdd95ced0d5a9528e97ff0f20742749cbd9ef6dc1322d13e682a7085a67`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 106.1 KB (106063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe17fc291d9444fbae93d7f45eab008318f87302c016c06e6e911c1a571a053`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 2.0 MB (1988274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1948bd131d2cbd05c6bf2962d18b15d105abee6f42f398bab3c13737537f197`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bde8ceae30a2a0890715bbc591167ee301c57d7f75023e80be460035187def`  
		Last Modified: Wed, 15 Apr 2026 20:20:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:58ed333482f8a8530c82ad7399d5917a7db85fbcdf70fc1dec55fbedcdf09253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4255278359004afd8c94db1a7fe6129fc984d0716c33665c9eca3168476fdcb`

```dockerfile
```

-	Layers:
	-	`sha256:5f47d88d89d22d065a3590d477ae130520b882176ab07e95862afb4d8b69b214`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 94.9 KB (94901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab2d532e4a6ce2f362d25c79dfaeb88d333fe6efe7c1b5b293630bf6ca292eb8`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 20.5 KB (20530 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:47a06cd0daead339b96ed90e425336a8a49a75e4e358b5ec1ea63a630720f704
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3947facc9e9fae3eee283f24b611a8ae87e353b6d6447bc6f582e90f2fce3743`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:58 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:17:59 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:21:02 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:21:02 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:21:02 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:21:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:21:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:21:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:21:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:21:03 GMT
USER memcache
# Wed, 15 Apr 2026 20:21:03 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:21:03 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77001163fdaab47f07a85fc5bb15f3512a8cb9b9b049cec7e0c88bcbbdb5bb5d`  
		Last Modified: Wed, 15 Apr 2026 20:21:07 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee1b43c0cfbf2ee56e39441933ff06803264d22918fe867d8b5ba7d5adfb9c3`  
		Last Modified: Wed, 15 Apr 2026 20:21:06 GMT  
		Size: 102.6 KB (102630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c041bfac12e599ad87749289dec9672dac36e8c0e16779f13fa695d10f2f0cc5`  
		Last Modified: Wed, 15 Apr 2026 20:21:07 GMT  
		Size: 1.9 MB (1937835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2dfd492dd0f295311a0c314fae06f4b325ae22cb0e673a53e0705f3d4e0504`  
		Last Modified: Wed, 15 Apr 2026 20:21:07 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671c66eac839c2f0a5b2e64d1f581069c4cdf119e784bff16540ecc94e2c2b10`  
		Last Modified: Wed, 15 Apr 2026 20:21:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:2a6148a6aebb042e55781b40ed626d0c5871833be4ae8dc303af7aace07d9d60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbaadfaacfaf0e7c226b35236bb84c2268d4c6eb017efd435a3999a44edfcc77`

```dockerfile
```

-	Layers:
	-	`sha256:c68bb3ee35fc0ac716bca45cc759f3b1ff52b1d5a0acae9876eaf0aa55aa667d`  
		Last Modified: Wed, 15 Apr 2026 20:21:06 GMT  
		Size: 20.5 KB (20466 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:fb58bae12ffa00c9cbafc8bee2341b43ffdccacbde7085fa707ef6c7f2d69e37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5273034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddd4e85c30e4df5803b553b8a7f84084c3dae6f72531ac70fcabf7099cfa8148`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 21:14:38 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 21:14:39 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 21:17:34 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 21:17:34 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 21:17:34 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 21:17:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 21:17:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:17:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 21:17:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:17:34 GMT
USER memcache
# Wed, 15 Apr 2026 21:17:34 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 21:17:34 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e312136cfedda9620407d42650d0595220e60d3c40ae8853bfbdd83f392b9e6`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53697a39f37b691917c91310ac4e107308674bddcc9017e3bbc0d0134eaf4c3e`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 92.4 KB (92369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5e4be9e0df543f152c376fe2cc74b89b75585793fdbd7d12476737d386d8e1`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 1.9 MB (1896191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a083f41edf5f859feb4367eeeea0955dc9799c8202fb8a67c40915ed5b195002`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c43503b1f4f42ffc5e0e4415befe45199dec730bc26347df151298345ba640`  
		Last Modified: Wed, 15 Apr 2026 21:17:40 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7535cf6b6a140771131c2c524301d4616f34856fcd8ecbe3e52300108c49de2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d73c906894a0a3d178edd69991f310225c0daef314e6faa83a0b9adecfbeb34`

```dockerfile
```

-	Layers:
	-	`sha256:8f1fddd7d14560fb90f381b09cde9302dfc9253e6702adf28c55961d755b1ad8`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 94.3 KB (94319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fcf119d246607aa25330c4c05fe14a64cebda69b02d14507862a9f07c1404e6`  
		Last Modified: Wed, 15 Apr 2026 21:17:38 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:6d70439467a65065c52894232a3085c724da2810a9b3205130d5e434ab411e3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6288798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4be3e105216d2507b68e772f7d08d52a5076dd55fad35c29775038d05c24112`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:15:23 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:15:24 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:18:13 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:18:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:18:13 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:18:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:18:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:18:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:18:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:18:13 GMT
USER memcache
# Wed, 15 Apr 2026 20:18:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:18:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81758f5fc2e8fa13e3625f253d7c999560ac666121c026f7251dbfb919cca611`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d735737d3a0cf1eda63bd72c09f64eb679313e9c5f8a105849848bdd779e1d`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 121.8 KB (121846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ac0921d2cc2b3388e0f006a6672c5a9e1098a59e570121dde092104d845c51`  
		Last Modified: Wed, 15 Apr 2026 20:18:19 GMT  
		Size: 2.0 MB (1965733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca9cf731b18a76c3ac25cc3add219660d57516c12680d7b1f1ece282406eb82`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:717a6b23dd1cd76b686bf26066af23265e0d002ed6a3e87f6aa4f79264b7da11`  
		Last Modified: Wed, 15 Apr 2026 20:18:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7e5232b868d3222e3ce2b0ee39c62f6cb294bea27456b00940fbc4e3c8c3f84d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:780bf975a24d5fdc511c857720c04cb077d64abcfe4c93ea0db7c9487c323718`

```dockerfile
```

-	Layers:
	-	`sha256:addb0f46e3b5adb674175c11fc85526d4628e24d74d210c8b00c9a945b44407c`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 94.4 KB (94355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3364e418b74b6f6ca17deec7d55783a6e1554de3783ab0a6d5e56496d935ddb0`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 20.7 KB (20728 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; 386

```console
$ docker pull memcached@sha256:80328bf779fa1494f7677b441ad1c16c2134f126e6556953deb3cfab1c4c9770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5744816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d957405dd0811f1cd15fe39563938a60c2008204d2f63ebc7e39f8989c796f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 22:20:45 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 22:20:46 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 22:23:32 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 22:23:32 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 22:23:32 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 22:23:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 22:23:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 22:23:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 22:23:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 22:23:32 GMT
USER memcache
# Wed, 15 Apr 2026 22:23:32 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 22:23:32 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0617a09eee85c2032f5596ded56b733366513074f9096177315b50dc45485e20`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c67275dbc381ac3ae0b21dda20edaf245e2ca54d6f5dc3af8805db03c17cc93`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 110.7 KB (110715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6ecb23f1f4bc89d5c315aac493f29fe7bb33061c70d926c904f4f55d374461`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 1.9 MB (1942309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e782df8f482a58603ea70ef9e04e838d044a6070c7e4cd116c90a09b917ed940`  
		Last Modified: Wed, 15 Apr 2026 22:23:38 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616df56d574e39c00ae772c6a29e2b724698048a83cc29ea17049573f9073b10`  
		Last Modified: Wed, 15 Apr 2026 22:23:38 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:c726e7abf461d963e544818339e4cd12fd2f31e41436475f0e51818a0885fbdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12e41b9d6f745d686c2649255bd14fe4e0b97a3477d383e719490e5ef66b27ae`

```dockerfile
```

-	Layers:
	-	`sha256:b44003cd1ea209090a063c5abfb4ee881849abba47e8711191b7637f86d8ee8b`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 94.9 KB (94856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f431de53d9b6c7e2cbc847af9daec064d061f8bd625615734012051336c495a`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 20.5 KB (20472 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:8182e35a9a404f0b522cb3c176d3dc4aade974e5556184c0a5a19e800721868a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6034321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30c6f532e81b50ea71c3520a80da0c8154b4cb14ebc17f87eb3a026862b47ed8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:41 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:17:43 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:20:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:20:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:20:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:20:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:20:22 GMT
USER memcache
# Wed, 15 Apr 2026 20:20:22 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:20:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee88d1c88fa46aa906a297c2919c9a085e74d04f20e4f827ca240a20f10ad34`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c574329cc1ebf156e2d89ab608bd58a3c0db550845c0ec394d265aa98fc5c4`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 126.3 KB (126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc2a28510bcba91734e7b38682847296011b63458db8a87a4bcecd180b8de7b5`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 2.1 MB (2075767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c524eb15ef0a41bf969efc93ef579db92dc59e8df57c9abfd099e7f6ff0756`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bde8ceae30a2a0890715bbc591167ee301c57d7f75023e80be460035187def`  
		Last Modified: Wed, 15 Apr 2026 20:20:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:4051408ef6c5bf4d4f37abf19c13f0298d8baa81770fcbfb588221e49e3bb834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ec3a4d49e6f325e484db43c9c9981f4eaa0223d9ae98282d95c3ee20c2089cb`

```dockerfile
```

-	Layers:
	-	`sha256:0e4e65db585f857844a67a831eb876dbb0a8a40d9269393d6c0fa83a2df995ae`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 94.3 KB (94308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50f58ec8aff3c96cc7b58e689122c27ee26121c598034cdc59ec95fd6423effe`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:f3209d1ca2c4ce827614d16445231d96372944d218f18fd22850eec83874e5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5772332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e30170e0826b89d0ca59ffcae54b850ded07e6ae9451ecf1fd60f3ca8adcc725`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2026 00:00:48 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 16 Apr 2026 00:00:52 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 16 Apr 2026 00:14:21 GMT
ENV MEMCACHED_VERSION=1.6.41
# Thu, 16 Apr 2026 00:14:21 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Thu, 16 Apr 2026 00:14:21 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Thu, 16 Apr 2026 00:14:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 16 Apr 2026 00:14:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Apr 2026 00:14:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 16 Apr 2026 00:14:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Apr 2026 00:14:22 GMT
USER memcache
# Thu, 16 Apr 2026 00:14:22 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 16 Apr 2026 00:14:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62b143e34f5b89277e3a88ed4d722339d188a094d4bb534e222ca80e7741031`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bfff7c64f831ba03c491874cdf9a1c3f42bff72bb0e1951c63d8cf718854cff`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 108.9 KB (108903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69aef1050272a61cfbfd97c041d3776f96bdd03b102f2c3c54bbb0af2e1235a5`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 2.1 MB (2074414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ce340fb37f86db0d3aa774c23880b7c8322d2af8e3adc27a6ffa25d67c2122`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e40c6fb92d819994d38fae7accdffd583465eb6e645834b66f3ce9f0562f69`  
		Last Modified: Thu, 16 Apr 2026 00:14:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:2caae198d1efb7d4df14da45a3ff360a697982b544a61a3f907076b414983ea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1503bd38f4b30bc91be18dd93359e7376a9da1c7cb652ade64efd154064543fe`

```dockerfile
```

-	Layers:
	-	`sha256:e2d79fb634d76e28f055ab09953f59c371b93599e2b79f20f3d758f2c9520118`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 94.3 KB (94304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3614ad9b1715c3d6aa488496fca74d7143ea095d227f599407c933c62ec266aa`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 20.6 KB (20604 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:1da27660ae89a83aaf603e1affd51be573e5b8dac6c07ed592aee2a3a2b20581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5859702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13aa64df69a308e46b054bbd8e7a5d2f1e079005771f61748dae0d049889ba7f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:14:40 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:14:41 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:17:58 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:17:58 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:17:58 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:17:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:17:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:17:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:17:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:17:58 GMT
USER memcache
# Wed, 15 Apr 2026 20:17:58 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:17:58 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c42733e5f451590186b9b76c4b374ae5a84b657f7f1fd405647f5ba82c65bcd`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a14431ac88e8fe205b07f09b7e4843bb254de41cbc044725d6eaee3c2f822f`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 114.3 KB (114293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6377b7d98f32173cd47682aa73b32e4eba42781fa9224b9eb7a6f87367d37f94`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 2.0 MB (2017525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d022ae992296922747a4b69694b0185a0ce1f6cdece7f794e39e74dab92d250`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255cb3a435cbd623c1235d0429160faf72c244a6c1a613525df36f58a8c1f784`  
		Last Modified: Wed, 15 Apr 2026 20:18:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:531ee140f06db77d73b71bce7339abec3c6d976092bb80542bb337bb406acdbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b17d6f7e71efe3ee05ebcdb8ae90c28cf60db9ef069b0a98fe442c949740a6c`

```dockerfile
```

-	Layers:
	-	`sha256:820a080f49bf9e33948dbe5c13f6254f135d90bcb2b2277e3d2fd2430626c1a2`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 94.2 KB (94250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8ab82f4f240f46f9e34b74691925ab4af7f1cbb12ad3cb8639e0f317cf06653`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine3.23`

```console
$ docker pull memcached@sha256:65c80b311a9601ef5ca8af3814e5cd06a9c4277ea139d80bd53da6b4d39eb46e
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
$ docker pull memcached@sha256:7b962825022657b112923d502400d5734870d5eb12c19e7f1f6585f7534a6795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5959872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b58f7e71f30daaa3f466fa31d855fddb7101e42c0c42fac520be5d1d43ec32e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:46 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:17:47 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:20:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:20:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:20:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:20:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:20:22 GMT
USER memcache
# Wed, 15 Apr 2026 20:20:22 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:20:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73d5ffe265b83073ce3c7211fb3c15ebbd5e7146d870d9ce69d2e7dfc493348`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6cb4fdd95ced0d5a9528e97ff0f20742749cbd9ef6dc1322d13e682a7085a67`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 106.1 KB (106063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe17fc291d9444fbae93d7f45eab008318f87302c016c06e6e911c1a571a053`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 2.0 MB (1988274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1948bd131d2cbd05c6bf2962d18b15d105abee6f42f398bab3c13737537f197`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bde8ceae30a2a0890715bbc591167ee301c57d7f75023e80be460035187def`  
		Last Modified: Wed, 15 Apr 2026 20:20:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:58ed333482f8a8530c82ad7399d5917a7db85fbcdf70fc1dec55fbedcdf09253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4255278359004afd8c94db1a7fe6129fc984d0716c33665c9eca3168476fdcb`

```dockerfile
```

-	Layers:
	-	`sha256:5f47d88d89d22d065a3590d477ae130520b882176ab07e95862afb4d8b69b214`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 94.9 KB (94901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab2d532e4a6ce2f362d25c79dfaeb88d333fe6efe7c1b5b293630bf6ca292eb8`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 20.5 KB (20530 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; arm variant v6

```console
$ docker pull memcached@sha256:47a06cd0daead339b96ed90e425336a8a49a75e4e358b5ec1ea63a630720f704
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3947facc9e9fae3eee283f24b611a8ae87e353b6d6447bc6f582e90f2fce3743`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:58 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:17:59 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:21:02 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:21:02 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:21:02 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:21:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:21:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:21:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:21:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:21:03 GMT
USER memcache
# Wed, 15 Apr 2026 20:21:03 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:21:03 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77001163fdaab47f07a85fc5bb15f3512a8cb9b9b049cec7e0c88bcbbdb5bb5d`  
		Last Modified: Wed, 15 Apr 2026 20:21:07 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee1b43c0cfbf2ee56e39441933ff06803264d22918fe867d8b5ba7d5adfb9c3`  
		Last Modified: Wed, 15 Apr 2026 20:21:06 GMT  
		Size: 102.6 KB (102630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c041bfac12e599ad87749289dec9672dac36e8c0e16779f13fa695d10f2f0cc5`  
		Last Modified: Wed, 15 Apr 2026 20:21:07 GMT  
		Size: 1.9 MB (1937835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2dfd492dd0f295311a0c314fae06f4b325ae22cb0e673a53e0705f3d4e0504`  
		Last Modified: Wed, 15 Apr 2026 20:21:07 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671c66eac839c2f0a5b2e64d1f581069c4cdf119e784bff16540ecc94e2c2b10`  
		Last Modified: Wed, 15 Apr 2026 20:21:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:2a6148a6aebb042e55781b40ed626d0c5871833be4ae8dc303af7aace07d9d60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbaadfaacfaf0e7c226b35236bb84c2268d4c6eb017efd435a3999a44edfcc77`

```dockerfile
```

-	Layers:
	-	`sha256:c68bb3ee35fc0ac716bca45cc759f3b1ff52b1d5a0acae9876eaf0aa55aa667d`  
		Last Modified: Wed, 15 Apr 2026 20:21:06 GMT  
		Size: 20.5 KB (20466 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; arm variant v7

```console
$ docker pull memcached@sha256:fb58bae12ffa00c9cbafc8bee2341b43ffdccacbde7085fa707ef6c7f2d69e37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5273034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddd4e85c30e4df5803b553b8a7f84084c3dae6f72531ac70fcabf7099cfa8148`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 21:14:38 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 21:14:39 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 21:17:34 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 21:17:34 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 21:17:34 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 21:17:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 21:17:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:17:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 21:17:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:17:34 GMT
USER memcache
# Wed, 15 Apr 2026 21:17:34 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 21:17:34 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e312136cfedda9620407d42650d0595220e60d3c40ae8853bfbdd83f392b9e6`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53697a39f37b691917c91310ac4e107308674bddcc9017e3bbc0d0134eaf4c3e`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 92.4 KB (92369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5e4be9e0df543f152c376fe2cc74b89b75585793fdbd7d12476737d386d8e1`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 1.9 MB (1896191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a083f41edf5f859feb4367eeeea0955dc9799c8202fb8a67c40915ed5b195002`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c43503b1f4f42ffc5e0e4415befe45199dec730bc26347df151298345ba640`  
		Last Modified: Wed, 15 Apr 2026 21:17:40 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:7535cf6b6a140771131c2c524301d4616f34856fcd8ecbe3e52300108c49de2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d73c906894a0a3d178edd69991f310225c0daef314e6faa83a0b9adecfbeb34`

```dockerfile
```

-	Layers:
	-	`sha256:8f1fddd7d14560fb90f381b09cde9302dfc9253e6702adf28c55961d755b1ad8`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 94.3 KB (94319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fcf119d246607aa25330c4c05fe14a64cebda69b02d14507862a9f07c1404e6`  
		Last Modified: Wed, 15 Apr 2026 21:17:38 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:6d70439467a65065c52894232a3085c724da2810a9b3205130d5e434ab411e3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6288798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4be3e105216d2507b68e772f7d08d52a5076dd55fad35c29775038d05c24112`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:15:23 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:15:24 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:18:13 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:18:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:18:13 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:18:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:18:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:18:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:18:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:18:13 GMT
USER memcache
# Wed, 15 Apr 2026 20:18:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:18:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81758f5fc2e8fa13e3625f253d7c999560ac666121c026f7251dbfb919cca611`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d735737d3a0cf1eda63bd72c09f64eb679313e9c5f8a105849848bdd779e1d`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 121.8 KB (121846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ac0921d2cc2b3388e0f006a6672c5a9e1098a59e570121dde092104d845c51`  
		Last Modified: Wed, 15 Apr 2026 20:18:19 GMT  
		Size: 2.0 MB (1965733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca9cf731b18a76c3ac25cc3add219660d57516c12680d7b1f1ece282406eb82`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:717a6b23dd1cd76b686bf26066af23265e0d002ed6a3e87f6aa4f79264b7da11`  
		Last Modified: Wed, 15 Apr 2026 20:18:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:7e5232b868d3222e3ce2b0ee39c62f6cb294bea27456b00940fbc4e3c8c3f84d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:780bf975a24d5fdc511c857720c04cb077d64abcfe4c93ea0db7c9487c323718`

```dockerfile
```

-	Layers:
	-	`sha256:addb0f46e3b5adb674175c11fc85526d4628e24d74d210c8b00c9a945b44407c`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 94.4 KB (94355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3364e418b74b6f6ca17deec7d55783a6e1554de3783ab0a6d5e56496d935ddb0`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 20.7 KB (20728 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; 386

```console
$ docker pull memcached@sha256:80328bf779fa1494f7677b441ad1c16c2134f126e6556953deb3cfab1c4c9770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5744816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d957405dd0811f1cd15fe39563938a60c2008204d2f63ebc7e39f8989c796f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 22:20:45 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 22:20:46 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 22:23:32 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 22:23:32 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 22:23:32 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 22:23:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 22:23:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 22:23:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 22:23:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 22:23:32 GMT
USER memcache
# Wed, 15 Apr 2026 22:23:32 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 22:23:32 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0617a09eee85c2032f5596ded56b733366513074f9096177315b50dc45485e20`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c67275dbc381ac3ae0b21dda20edaf245e2ca54d6f5dc3af8805db03c17cc93`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 110.7 KB (110715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6ecb23f1f4bc89d5c315aac493f29fe7bb33061c70d926c904f4f55d374461`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 1.9 MB (1942309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e782df8f482a58603ea70ef9e04e838d044a6070c7e4cd116c90a09b917ed940`  
		Last Modified: Wed, 15 Apr 2026 22:23:38 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616df56d574e39c00ae772c6a29e2b724698048a83cc29ea17049573f9073b10`  
		Last Modified: Wed, 15 Apr 2026 22:23:38 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:c726e7abf461d963e544818339e4cd12fd2f31e41436475f0e51818a0885fbdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12e41b9d6f745d686c2649255bd14fe4e0b97a3477d383e719490e5ef66b27ae`

```dockerfile
```

-	Layers:
	-	`sha256:b44003cd1ea209090a063c5abfb4ee881849abba47e8711191b7637f86d8ee8b`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 94.9 KB (94856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f431de53d9b6c7e2cbc847af9daec064d061f8bd625615734012051336c495a`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 20.5 KB (20472 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; ppc64le

```console
$ docker pull memcached@sha256:8182e35a9a404f0b522cb3c176d3dc4aade974e5556184c0a5a19e800721868a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6034321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30c6f532e81b50ea71c3520a80da0c8154b4cb14ebc17f87eb3a026862b47ed8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:41 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:17:43 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:20:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:20:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:20:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:20:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:20:22 GMT
USER memcache
# Wed, 15 Apr 2026 20:20:22 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:20:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee88d1c88fa46aa906a297c2919c9a085e74d04f20e4f827ca240a20f10ad34`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c574329cc1ebf156e2d89ab608bd58a3c0db550845c0ec394d265aa98fc5c4`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 126.3 KB (126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc2a28510bcba91734e7b38682847296011b63458db8a87a4bcecd180b8de7b5`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 2.1 MB (2075767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c524eb15ef0a41bf969efc93ef579db92dc59e8df57c9abfd099e7f6ff0756`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bde8ceae30a2a0890715bbc591167ee301c57d7f75023e80be460035187def`  
		Last Modified: Wed, 15 Apr 2026 20:20:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:4051408ef6c5bf4d4f37abf19c13f0298d8baa81770fcbfb588221e49e3bb834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ec3a4d49e6f325e484db43c9c9981f4eaa0223d9ae98282d95c3ee20c2089cb`

```dockerfile
```

-	Layers:
	-	`sha256:0e4e65db585f857844a67a831eb876dbb0a8a40d9269393d6c0fa83a2df995ae`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 94.3 KB (94308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50f58ec8aff3c96cc7b58e689122c27ee26121c598034cdc59ec95fd6423effe`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; riscv64

```console
$ docker pull memcached@sha256:f3209d1ca2c4ce827614d16445231d96372944d218f18fd22850eec83874e5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5772332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e30170e0826b89d0ca59ffcae54b850ded07e6ae9451ecf1fd60f3ca8adcc725`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2026 00:00:48 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 16 Apr 2026 00:00:52 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 16 Apr 2026 00:14:21 GMT
ENV MEMCACHED_VERSION=1.6.41
# Thu, 16 Apr 2026 00:14:21 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Thu, 16 Apr 2026 00:14:21 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Thu, 16 Apr 2026 00:14:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 16 Apr 2026 00:14:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Apr 2026 00:14:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 16 Apr 2026 00:14:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Apr 2026 00:14:22 GMT
USER memcache
# Thu, 16 Apr 2026 00:14:22 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 16 Apr 2026 00:14:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62b143e34f5b89277e3a88ed4d722339d188a094d4bb534e222ca80e7741031`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bfff7c64f831ba03c491874cdf9a1c3f42bff72bb0e1951c63d8cf718854cff`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 108.9 KB (108903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69aef1050272a61cfbfd97c041d3776f96bdd03b102f2c3c54bbb0af2e1235a5`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 2.1 MB (2074414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ce340fb37f86db0d3aa774c23880b7c8322d2af8e3adc27a6ffa25d67c2122`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e40c6fb92d819994d38fae7accdffd583465eb6e645834b66f3ce9f0562f69`  
		Last Modified: Thu, 16 Apr 2026 00:14:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:2caae198d1efb7d4df14da45a3ff360a697982b544a61a3f907076b414983ea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1503bd38f4b30bc91be18dd93359e7376a9da1c7cb652ade64efd154064543fe`

```dockerfile
```

-	Layers:
	-	`sha256:e2d79fb634d76e28f055ab09953f59c371b93599e2b79f20f3d758f2c9520118`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 94.3 KB (94304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3614ad9b1715c3d6aa488496fca74d7143ea095d227f599407c933c62ec266aa`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 20.6 KB (20604 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; s390x

```console
$ docker pull memcached@sha256:1da27660ae89a83aaf603e1affd51be573e5b8dac6c07ed592aee2a3a2b20581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5859702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13aa64df69a308e46b054bbd8e7a5d2f1e079005771f61748dae0d049889ba7f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:14:40 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:14:41 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:17:58 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:17:58 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:17:58 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:17:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:17:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:17:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:17:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:17:58 GMT
USER memcache
# Wed, 15 Apr 2026 20:17:58 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:17:58 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c42733e5f451590186b9b76c4b374ae5a84b657f7f1fd405647f5ba82c65bcd`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a14431ac88e8fe205b07f09b7e4843bb254de41cbc044725d6eaee3c2f822f`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 114.3 KB (114293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6377b7d98f32173cd47682aa73b32e4eba42781fa9224b9eb7a6f87367d37f94`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 2.0 MB (2017525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d022ae992296922747a4b69694b0185a0ce1f6cdece7f794e39e74dab92d250`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255cb3a435cbd623c1235d0429160faf72c244a6c1a613525df36f58a8c1f784`  
		Last Modified: Wed, 15 Apr 2026 20:18:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:531ee140f06db77d73b71bce7339abec3c6d976092bb80542bb337bb406acdbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b17d6f7e71efe3ee05ebcdb8ae90c28cf60db9ef069b0a98fe442c949740a6c`

```dockerfile
```

-	Layers:
	-	`sha256:820a080f49bf9e33948dbe5c13f6254f135d90bcb2b2277e3d2fd2430626c1a2`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 94.2 KB (94250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8ab82f4f240f46f9e34b74691925ab4af7f1cbb12ad3cb8639e0f317cf06653`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-trixie`

```console
$ docker pull memcached@sha256:277e0c4f249b118e95ab10e535bae2fa1af772271d9152f3468e58d59348db56
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
$ docker pull memcached@sha256:518f136cafc43439a777c20224d30b6fadc3433e3de9573f514dca10dd7e0082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32198630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ec7b3eba028951d3aeee1ef26a365c913edaf06de6c008653f175c0ff0078ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:21:37 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 22 Apr 2026 01:21:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:24:27 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 22 Apr 2026 01:24:27 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 22 Apr 2026 01:24:27 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 22 Apr 2026 01:24:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 22 Apr 2026 01:24:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:24:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:24:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:24:27 GMT
USER memcache
# Wed, 22 Apr 2026 01:24:27 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 Apr 2026 01:24:27 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53e27a8dc2608bcd39496d6e1a0a021aa8933953409444f778d810ec220ab89`  
		Last Modified: Wed, 22 Apr 2026 01:24:33 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d02c07f7ffb4ea4d70b3af1ed59da72e778c143718ba2a7bcb8cd6d12afd95b`  
		Last Modified: Wed, 22 Apr 2026 01:24:33 GMT  
		Size: 136.7 KB (136658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b1a619145ef14a0e4599b98a19dbdc4fc96cfdf359ecf816454cd80ccf2dd2`  
		Last Modified: Wed, 22 Apr 2026 01:24:34 GMT  
		Size: 2.3 MB (2280287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7716efee154a639ac02ada0d1638837bb72c3fc33ecac40f78ffb91daf9dfc5`  
		Last Modified: Wed, 22 Apr 2026 01:24:34 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712f24abcdc2a432d57253a569a16eddd36ff1f8a4ace323467cdb642eae2850`  
		Last Modified: Wed, 22 Apr 2026 01:24:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:f32546667bf4926fd4e7c91aa55a833e8636777f2aa68437cb2bc7a5330e2307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3700c2c8b8182ac20db287282cdafbde42f55966784e109b48a9e5c2ba4d7492`

```dockerfile
```

-	Layers:
	-	`sha256:a3fe3f55746c35c0a798536b5abfc78349217684ca67ba43649a1c86d2a6ebe3`  
		Last Modified: Wed, 22 Apr 2026 01:24:33 GMT  
		Size: 2.0 MB (2008326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0b151a6f180676864b1e8721dddbaf0c105e743520356d58f7df86572a295fa`  
		Last Modified: Wed, 22 Apr 2026 01:24:33 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; arm variant v5

```console
$ docker pull memcached@sha256:4b91aeabb9b5d253e27cc0e6f6fa6cc82780c4d686f484c9ed1057a1dd429ba2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30305389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e62e4552c0bfc9dd8f4797df2c1386943df5780d342654ed3050e75668231e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:17:31 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 22 Apr 2026 01:17:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:20:57 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 22 Apr 2026 01:20:57 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 22 Apr 2026 01:20:57 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 22 Apr 2026 01:20:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 22 Apr 2026 01:20:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:20:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:20:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:20:57 GMT
USER memcache
# Wed, 22 Apr 2026 01:20:57 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 Apr 2026 01:20:57 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6496d93bca0663211b9252da346044ecb734ee5b3ecaae5b1fbd230753faee2f`  
		Last Modified: Wed, 22 Apr 2026 00:15:59 GMT  
		Size: 27.9 MB (27948180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64cdc01a23d15e84ef2ee2165c1a90970fb54d98f29377fa63fbd82988cdcc40`  
		Last Modified: Wed, 22 Apr 2026 01:21:03 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:303fc6e2ad4e0da497f7e238e61ec9e1fbde60909262de4a50e05c4db2191602`  
		Last Modified: Wed, 22 Apr 2026 01:21:03 GMT  
		Size: 144.2 KB (144163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c438ec3169ba426bc8374ca37b4f159272d50b60173c35c396f8fbf2208b8806`  
		Last Modified: Wed, 22 Apr 2026 01:21:03 GMT  
		Size: 2.2 MB (2211533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b5512f6aab6e3147798ce406f1035f68f18c2dd046b5fdd6344a17ace7fb31`  
		Last Modified: Wed, 22 Apr 2026 01:21:03 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a320e8acb7760a30eb688cd929fda03bf41ba23a307e06071106c3c0415d03`  
		Last Modified: Wed, 22 Apr 2026 01:21:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:4faa0397c26f0f4a312a28578db40b0f95f89c09769520c7cc09900886412dd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af54d9e6dbb4f86d5a79e417071faea8dd939b7758f640ce360a49c55069e2eb`

```dockerfile
```

-	Layers:
	-	`sha256:1850a912cc062cca1f70a2b76861d54c0ad06921d2a4960a7c483b5f8820eaa1`  
		Last Modified: Wed, 22 Apr 2026 01:21:03 GMT  
		Size: 2.0 MB (2011329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02fdad23f354f6597bfec3258d6bbee5142bcce9e1faaa7de87f9859bf8c6d14`  
		Last Modified: Wed, 22 Apr 2026 01:21:03 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; arm variant v7

```console
$ docker pull memcached@sha256:4d262b60fea5a97e91a6c1827ab7209a344c47616388ada79b27e4e69eea9d38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28516774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02f2f7426f06caeeb218b724a947fa35544b0749bacf781227878e40cb98d08f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:18:06 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 22 Apr 2026 01:18:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:21:19 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 22 Apr 2026 01:21:19 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 22 Apr 2026 01:21:19 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 22 Apr 2026 01:21:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 22 Apr 2026 01:21:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:21:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:21:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:21:19 GMT
USER memcache
# Wed, 22 Apr 2026 01:21:19 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 Apr 2026 01:21:19 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9e541e5bfbbe69b7bbe01cd2f1abf8560e2e43bf76eb96b2e88a3df29020834b`  
		Last Modified: Wed, 22 Apr 2026 00:17:02 GMT  
		Size: 26.2 MB (26214838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0867e20c7ab47539b3f27abc4c7f4bf41d367127d9ffbd30a531ab387a69e2e`  
		Last Modified: Wed, 22 Apr 2026 01:21:25 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34eedf23d5ae4af59fe6ecfd854e48545ede507ce44d930cea5c11b652b31f4`  
		Last Modified: Wed, 22 Apr 2026 01:21:25 GMT  
		Size: 135.4 KB (135382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fff54fd1447de9c8b377640a2720588785769320b1a65d59a1da8e9690e6f9`  
		Last Modified: Wed, 22 Apr 2026 01:21:25 GMT  
		Size: 2.2 MB (2165043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac214a1bada6a999cda6b6b021b8ef5ba954108062e3ee4df0161a500fc566f`  
		Last Modified: Wed, 22 Apr 2026 01:21:25 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0431aacefa9d6f210c7c4778e75df5a21c196127779acc2da1bd7b32088f47dc`  
		Last Modified: Wed, 22 Apr 2026 01:21:26 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:e4f840cb65bd892b2aafc305cb008de10d4d41475876ef9c9bbf51831f9cd7e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:987452d71cfba90bac820fca09f2954a061813125a8832038df5c062224577c5`

```dockerfile
```

-	Layers:
	-	`sha256:f5793a9489c1e1010726124554d7404a19b2675ce8596a38169b160edc81d045`  
		Last Modified: Wed, 22 Apr 2026 01:21:25 GMT  
		Size: 2.0 MB (2009786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef3c23077c5adc1a06a0e1f66d0ec1e57032a5b35685c53064098e236a62c5a1`  
		Last Modified: Wed, 22 Apr 2026 01:21:25 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:52e2a52a542b0fff64533e7271ce3af9825a80a1126998cf6070b0ec4c0030b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32560736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c3fcfefa704f0162e85ab03d515502e07a6ff91ec994dc4b6c956cc2ce80990`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:22:08 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 22 Apr 2026 01:22:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:25:10 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 22 Apr 2026 01:25:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 22 Apr 2026 01:25:10 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 22 Apr 2026 01:25:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 22 Apr 2026 01:25:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:25:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:25:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:25:10 GMT
USER memcache
# Wed, 22 Apr 2026 01:25:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 Apr 2026 01:25:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebea5231ebe63bff9044a4ee7713dac1b62fc15d85ee920f04eae4010a67b668`  
		Last Modified: Wed, 22 Apr 2026 01:25:16 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5921030f644563277c2af1be27b21dfded0e01763210710efac613f07dc74c`  
		Last Modified: Wed, 22 Apr 2026 01:25:16 GMT  
		Size: 153.5 KB (153515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1ef7f1deafd8e81fec98af35ef4fe12c2436c1eddb6bb87377b83f524f7d6f`  
		Last Modified: Wed, 22 Apr 2026 01:25:16 GMT  
		Size: 2.3 MB (2262106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd4f58ffc6f10cea1171fbb552aff0b93a04aba0ca6815cd9ad66ab3a49f8419`  
		Last Modified: Wed, 22 Apr 2026 01:25:16 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace7ea462603345a875235135df0b8dd036890eacdb25150c1a8089604e3ca1f`  
		Last Modified: Wed, 22 Apr 2026 01:25:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:63aba0d160ad2159dd41a074d79446fc4ba2e745c7e5a10a41dbd1d5c2abc86d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b67f2365f86c60d496eb140fde16a0d6fbf89ae6a83d200c6a3971e32eca706b`

```dockerfile
```

-	Layers:
	-	`sha256:e87d247df404b9fe7e19667c95311e8109ea54acdcca2f52ceba73b7099d144e`  
		Last Modified: Wed, 22 Apr 2026 01:25:16 GMT  
		Size: 2.0 MB (2008642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5290960be9e7480bf28bf59599ba02b7792ea80b3309570c3b3a24465ad7d58`  
		Last Modified: Wed, 22 Apr 2026 01:25:16 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; 386

```console
$ docker pull memcached@sha256:0b8f07a6f169bfe4cc362cbabca8c92d5140665660c615383f2755c40c0036f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33670125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd6a79877127262a308ef5f3bd216749c6f0b1fc43971b56c533d4e47f5c6de2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:17:33 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 22 Apr 2026 01:17:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:20:28 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 22 Apr 2026 01:20:28 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 22 Apr 2026 01:20:28 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 22 Apr 2026 01:20:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 22 Apr 2026 01:20:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:20:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:20:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:20:28 GMT
USER memcache
# Wed, 22 Apr 2026 01:20:28 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 Apr 2026 01:20:28 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:dacd7cda306bf5bd7a2030f9b0c2e9d71fda44ea58493a33450d210b74a8ec75`  
		Last Modified: Wed, 22 Apr 2026 00:17:04 GMT  
		Size: 31.3 MB (31296327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a0c9fe363e7e198726a5e39cf627131e43cd59d319a350f978180f6f449b8a`  
		Last Modified: Wed, 22 Apr 2026 01:20:34 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dff2976b24139841065357d1f81c8cf6d9b45ee35e2947f1345e86493b2f5e67`  
		Last Modified: Wed, 22 Apr 2026 01:20:34 GMT  
		Size: 147.5 KB (147529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8b8718f120acc0033835790e0bd541e38b843c6b260688b8fde3c94eadd5911`  
		Last Modified: Wed, 22 Apr 2026 01:20:34 GMT  
		Size: 2.2 MB (2224758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f70ea447cee314191f67e0ce5ccc23703730c89810e26bfa3f96f81964849dc`  
		Last Modified: Wed, 22 Apr 2026 01:20:34 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:789bc1b0beaaf9809e3cab832a0b6b29f50aec3b18f7a7cdf04e343d3ee800a3`  
		Last Modified: Wed, 22 Apr 2026 01:20:35 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:45cfea0c565e5e6c79f4a36cf4ec611ccc7e910c481110b37be04eca3276511b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d33423fad9c4c2f3b1af3eb87b8af48d7cfc9e00d70e6c33937d7d215fb94c5`

```dockerfile
```

-	Layers:
	-	`sha256:2656e01c20323e582a0ba03c06d82008eb35ae9850f7d6c7f73c0e5ae040805b`  
		Last Modified: Wed, 22 Apr 2026 01:20:34 GMT  
		Size: 2.0 MB (2005483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d267990174d3038591d6a8ffe07af06d961bb5c68b86a9cdac459f5a0996ddbe`  
		Last Modified: Wed, 22 Apr 2026 01:20:34 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; ppc64le

```console
$ docker pull memcached@sha256:3df945008f026e1a7782fc67d0107a07c9103d9d50dd7ae605082ea97fb64ff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36164269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7eb2db1cbb0c7ddc2688ee498498fb5122ee78ab349b636a43585b1beb30da9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:35:49 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 22 Apr 2026 01:35:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:39:22 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 22 Apr 2026 01:39:22 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 22 Apr 2026 01:39:22 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 22 Apr 2026 01:39:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 22 Apr 2026 01:39:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:39:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:39:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:39:23 GMT
USER memcache
# Wed, 22 Apr 2026 01:39:23 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 Apr 2026 01:39:23 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b5fd051d0fcd0789e7358cba300f83befdba943416041497be86050e282a6d02`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 33.6 MB (33598032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e271c91c5c30b04dee49fb4c9ab2f9863d13146641f1b8681b59467d0f8ab5`  
		Last Modified: Wed, 22 Apr 2026 01:39:42 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb7fa3c8c45f87e36929f71acaead9bcb07985c205ea0aa6fd83aca31691d78`  
		Last Modified: Wed, 22 Apr 2026 01:39:42 GMT  
		Size: 170.4 KB (170378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f09610f9abffbf6411865ebc07ee20de6c14b2250467c4682f423dddc0ab82`  
		Last Modified: Wed, 22 Apr 2026 01:39:42 GMT  
		Size: 2.4 MB (2394347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a0fb856cc435334489ebeec58afd76f4e676c8bae4b3688daefedfbc7f7c1a8`  
		Last Modified: Wed, 22 Apr 2026 01:39:42 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea36b259fc26e36b99ded4a3aa0ca190c1117ecd424f26565f8474b55964d787`  
		Last Modified: Wed, 22 Apr 2026 01:39:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:c619fe6b2206166796157b814c0d60ca38e29a646b71cd6f5635e2f507cf70d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49e66f35bf963d54f332469bbdef0ca608c651311f5af0e923aca630f4429ae9`

```dockerfile
```

-	Layers:
	-	`sha256:f870fab207e6594315e4d18f50f3ebf834ebc298b6ec128104607668ae939995`  
		Last Modified: Wed, 22 Apr 2026 01:39:42 GMT  
		Size: 2.0 MB (2011927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bf20b8b72f84425e9121a35ea191dab3cf17562679390195740f260304727d7`  
		Last Modified: Wed, 22 Apr 2026 01:39:42 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; riscv64

```console
$ docker pull memcached@sha256:5554043a87027cff145bdb04810a9f8a067c72479937ce0328af056a5c3efe8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30623256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad08d83e675d61f6e230bee3e1d5d5e4b4e8d0b1b3656b71812168b7db5e08e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 08:28:54 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 22 Apr 2026 08:29:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 08:55:11 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 22 Apr 2026 08:55:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 22 Apr 2026 08:55:11 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 22 Apr 2026 08:55:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 22 Apr 2026 08:55:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 08:55:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 08:55:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 08:55:12 GMT
USER memcache
# Wed, 22 Apr 2026 08:55:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 Apr 2026 08:55:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8aa73197c6983c411cf26b41c64a557cfc81f9b4e6d897ff2829a66eac03b37`  
		Last Modified: Wed, 22 Apr 2026 08:55:56 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee379d85ef42145b3f09328c98634e8cd3320230281217ad58867c6982e1d8c`  
		Last Modified: Wed, 22 Apr 2026 08:55:57 GMT  
		Size: 133.1 KB (133094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:310a92cbf1cb95664c58022062af028a81e69f127cd8d9ee044bf7d5087db961`  
		Last Modified: Wed, 22 Apr 2026 08:55:57 GMT  
		Size: 2.2 MB (2208455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336575624802c397f4947f3ddfc2737281bfe2ba8cd714be646b72152c1ec1d0`  
		Last Modified: Wed, 22 Apr 2026 08:55:56 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e926175ab529d298755a0e0507accca74feec6c90ea4495edeaafb07954ad57d`  
		Last Modified: Wed, 22 Apr 2026 08:55:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:9b8b4751f5823830cf382050f0174dd5ade6dc0650b2a3134803b886b2652dba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bc1698424d742c630d5a555fa2c70be3195da5b1a2cd148a331c7aa9fb94b6f`

```dockerfile
```

-	Layers:
	-	`sha256:18aa82332065ff68528148bb97bd5681424d4c57e9e5e331b8908b44023570a9`  
		Last Modified: Wed, 22 Apr 2026 08:55:57 GMT  
		Size: 2.0 MB (2002290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edeefd058e4dbdf6c3026618be5f5184cd3d2c22f14746d890cd45a42004dc8f`  
		Last Modified: Wed, 22 Apr 2026 08:55:57 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; s390x

```console
$ docker pull memcached@sha256:e0fadaa0ad7c323c4f8ead5d8e1ebb9566adc59b25cbc280f40bef816f9d62eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32280559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5d7f2d629511f566dd7c4b3a944adb9989b05bb41dbd3e3881734bc1c1079c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:19:00 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 22 Apr 2026 01:19:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:22:27 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 22 Apr 2026 01:22:27 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 22 Apr 2026 01:22:27 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 22 Apr 2026 01:22:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 22 Apr 2026 01:22:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:22:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:22:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:22:27 GMT
USER memcache
# Wed, 22 Apr 2026 01:22:27 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 Apr 2026 01:22:27 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:71574deb335f1e823f938f4a215de00a90d63866898f1f354a0b15e8b9c30577`  
		Last Modified: Wed, 22 Apr 2026 00:17:08 GMT  
		Size: 29.8 MB (29840300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b460058bd06ca18e629070cadcc158edef16e034340796f661d4fab362ee94`  
		Last Modified: Wed, 22 Apr 2026 01:22:38 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5386c57fa90d49931296cf79f5e8d2ae18d07b9bcffe5eee8354033fee4b673`  
		Last Modified: Wed, 22 Apr 2026 01:22:38 GMT  
		Size: 140.5 KB (140521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd8308c0fc0224d29acef5aadae977dfea2e1ba7c9be0e207ee89c84a4f6417`  
		Last Modified: Wed, 22 Apr 2026 01:22:38 GMT  
		Size: 2.3 MB (2298228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fda405f0b2226447c88ba0d395ee00616ec775cecba66d9a980d4aac7b44fb49`  
		Last Modified: Wed, 22 Apr 2026 01:22:38 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fcaa079ef0e24aab0065df6b15e28d19a0807e2c9cdc639bbc63923135e6daa`  
		Last Modified: Wed, 22 Apr 2026 01:22:39 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:7d2e45f2ecd9448a99f98a077da16fb59c37827c2acbac9e99dea8f79d753165
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54358ef5a62ded9fafc9e908e79d81e5d01102cd4f2082017f54d92232acb7c4`

```dockerfile
```

-	Layers:
	-	`sha256:eb9c1105cc4bf8d4cf2089f7a2a43afe0a113388e7f5a4af9db1f44f9f0fbe11`  
		Last Modified: Wed, 22 Apr 2026 01:22:38 GMT  
		Size: 2.0 MB (2009763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af1c4a20085e6a6f3d2b2fcb2ce9c10456d057c6905b84fe6ad6d99ba351a872`  
		Last Modified: Wed, 22 Apr 2026 01:22:38 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6`

```console
$ docker pull memcached@sha256:277e0c4f249b118e95ab10e535bae2fa1af772271d9152f3468e58d59348db56
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
$ docker pull memcached@sha256:518f136cafc43439a777c20224d30b6fadc3433e3de9573f514dca10dd7e0082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32198630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ec7b3eba028951d3aeee1ef26a365c913edaf06de6c008653f175c0ff0078ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:21:37 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 22 Apr 2026 01:21:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:24:27 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 22 Apr 2026 01:24:27 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 22 Apr 2026 01:24:27 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 22 Apr 2026 01:24:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 22 Apr 2026 01:24:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:24:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:24:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:24:27 GMT
USER memcache
# Wed, 22 Apr 2026 01:24:27 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 Apr 2026 01:24:27 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53e27a8dc2608bcd39496d6e1a0a021aa8933953409444f778d810ec220ab89`  
		Last Modified: Wed, 22 Apr 2026 01:24:33 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d02c07f7ffb4ea4d70b3af1ed59da72e778c143718ba2a7bcb8cd6d12afd95b`  
		Last Modified: Wed, 22 Apr 2026 01:24:33 GMT  
		Size: 136.7 KB (136658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b1a619145ef14a0e4599b98a19dbdc4fc96cfdf359ecf816454cd80ccf2dd2`  
		Last Modified: Wed, 22 Apr 2026 01:24:34 GMT  
		Size: 2.3 MB (2280287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7716efee154a639ac02ada0d1638837bb72c3fc33ecac40f78ffb91daf9dfc5`  
		Last Modified: Wed, 22 Apr 2026 01:24:34 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712f24abcdc2a432d57253a569a16eddd36ff1f8a4ace323467cdb642eae2850`  
		Last Modified: Wed, 22 Apr 2026 01:24:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:f32546667bf4926fd4e7c91aa55a833e8636777f2aa68437cb2bc7a5330e2307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3700c2c8b8182ac20db287282cdafbde42f55966784e109b48a9e5c2ba4d7492`

```dockerfile
```

-	Layers:
	-	`sha256:a3fe3f55746c35c0a798536b5abfc78349217684ca67ba43649a1c86d2a6ebe3`  
		Last Modified: Wed, 22 Apr 2026 01:24:33 GMT  
		Size: 2.0 MB (2008326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0b151a6f180676864b1e8721dddbaf0c105e743520356d58f7df86572a295fa`  
		Last Modified: Wed, 22 Apr 2026 01:24:33 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm variant v5

```console
$ docker pull memcached@sha256:4b91aeabb9b5d253e27cc0e6f6fa6cc82780c4d686f484c9ed1057a1dd429ba2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30305389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e62e4552c0bfc9dd8f4797df2c1386943df5780d342654ed3050e75668231e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:17:31 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 22 Apr 2026 01:17:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:20:57 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 22 Apr 2026 01:20:57 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 22 Apr 2026 01:20:57 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 22 Apr 2026 01:20:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 22 Apr 2026 01:20:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:20:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:20:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:20:57 GMT
USER memcache
# Wed, 22 Apr 2026 01:20:57 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 Apr 2026 01:20:57 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6496d93bca0663211b9252da346044ecb734ee5b3ecaae5b1fbd230753faee2f`  
		Last Modified: Wed, 22 Apr 2026 00:15:59 GMT  
		Size: 27.9 MB (27948180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64cdc01a23d15e84ef2ee2165c1a90970fb54d98f29377fa63fbd82988cdcc40`  
		Last Modified: Wed, 22 Apr 2026 01:21:03 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:303fc6e2ad4e0da497f7e238e61ec9e1fbde60909262de4a50e05c4db2191602`  
		Last Modified: Wed, 22 Apr 2026 01:21:03 GMT  
		Size: 144.2 KB (144163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c438ec3169ba426bc8374ca37b4f159272d50b60173c35c396f8fbf2208b8806`  
		Last Modified: Wed, 22 Apr 2026 01:21:03 GMT  
		Size: 2.2 MB (2211533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b5512f6aab6e3147798ce406f1035f68f18c2dd046b5fdd6344a17ace7fb31`  
		Last Modified: Wed, 22 Apr 2026 01:21:03 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a320e8acb7760a30eb688cd929fda03bf41ba23a307e06071106c3c0415d03`  
		Last Modified: Wed, 22 Apr 2026 01:21:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:4faa0397c26f0f4a312a28578db40b0f95f89c09769520c7cc09900886412dd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af54d9e6dbb4f86d5a79e417071faea8dd939b7758f640ce360a49c55069e2eb`

```dockerfile
```

-	Layers:
	-	`sha256:1850a912cc062cca1f70a2b76861d54c0ad06921d2a4960a7c483b5f8820eaa1`  
		Last Modified: Wed, 22 Apr 2026 01:21:03 GMT  
		Size: 2.0 MB (2011329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02fdad23f354f6597bfec3258d6bbee5142bcce9e1faaa7de87f9859bf8c6d14`  
		Last Modified: Wed, 22 Apr 2026 01:21:03 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm variant v7

```console
$ docker pull memcached@sha256:4d262b60fea5a97e91a6c1827ab7209a344c47616388ada79b27e4e69eea9d38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28516774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02f2f7426f06caeeb218b724a947fa35544b0749bacf781227878e40cb98d08f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:18:06 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 22 Apr 2026 01:18:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:21:19 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 22 Apr 2026 01:21:19 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 22 Apr 2026 01:21:19 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 22 Apr 2026 01:21:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 22 Apr 2026 01:21:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:21:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:21:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:21:19 GMT
USER memcache
# Wed, 22 Apr 2026 01:21:19 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 Apr 2026 01:21:19 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9e541e5bfbbe69b7bbe01cd2f1abf8560e2e43bf76eb96b2e88a3df29020834b`  
		Last Modified: Wed, 22 Apr 2026 00:17:02 GMT  
		Size: 26.2 MB (26214838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0867e20c7ab47539b3f27abc4c7f4bf41d367127d9ffbd30a531ab387a69e2e`  
		Last Modified: Wed, 22 Apr 2026 01:21:25 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34eedf23d5ae4af59fe6ecfd854e48545ede507ce44d930cea5c11b652b31f4`  
		Last Modified: Wed, 22 Apr 2026 01:21:25 GMT  
		Size: 135.4 KB (135382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fff54fd1447de9c8b377640a2720588785769320b1a65d59a1da8e9690e6f9`  
		Last Modified: Wed, 22 Apr 2026 01:21:25 GMT  
		Size: 2.2 MB (2165043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac214a1bada6a999cda6b6b021b8ef5ba954108062e3ee4df0161a500fc566f`  
		Last Modified: Wed, 22 Apr 2026 01:21:25 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0431aacefa9d6f210c7c4778e75df5a21c196127779acc2da1bd7b32088f47dc`  
		Last Modified: Wed, 22 Apr 2026 01:21:26 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:e4f840cb65bd892b2aafc305cb008de10d4d41475876ef9c9bbf51831f9cd7e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:987452d71cfba90bac820fca09f2954a061813125a8832038df5c062224577c5`

```dockerfile
```

-	Layers:
	-	`sha256:f5793a9489c1e1010726124554d7404a19b2675ce8596a38169b160edc81d045`  
		Last Modified: Wed, 22 Apr 2026 01:21:25 GMT  
		Size: 2.0 MB (2009786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef3c23077c5adc1a06a0e1f66d0ec1e57032a5b35685c53064098e236a62c5a1`  
		Last Modified: Wed, 22 Apr 2026 01:21:25 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:52e2a52a542b0fff64533e7271ce3af9825a80a1126998cf6070b0ec4c0030b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32560736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c3fcfefa704f0162e85ab03d515502e07a6ff91ec994dc4b6c956cc2ce80990`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:22:08 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 22 Apr 2026 01:22:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:25:10 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 22 Apr 2026 01:25:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 22 Apr 2026 01:25:10 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 22 Apr 2026 01:25:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 22 Apr 2026 01:25:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:25:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:25:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:25:10 GMT
USER memcache
# Wed, 22 Apr 2026 01:25:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 Apr 2026 01:25:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebea5231ebe63bff9044a4ee7713dac1b62fc15d85ee920f04eae4010a67b668`  
		Last Modified: Wed, 22 Apr 2026 01:25:16 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5921030f644563277c2af1be27b21dfded0e01763210710efac613f07dc74c`  
		Last Modified: Wed, 22 Apr 2026 01:25:16 GMT  
		Size: 153.5 KB (153515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1ef7f1deafd8e81fec98af35ef4fe12c2436c1eddb6bb87377b83f524f7d6f`  
		Last Modified: Wed, 22 Apr 2026 01:25:16 GMT  
		Size: 2.3 MB (2262106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd4f58ffc6f10cea1171fbb552aff0b93a04aba0ca6815cd9ad66ab3a49f8419`  
		Last Modified: Wed, 22 Apr 2026 01:25:16 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace7ea462603345a875235135df0b8dd036890eacdb25150c1a8089604e3ca1f`  
		Last Modified: Wed, 22 Apr 2026 01:25:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:63aba0d160ad2159dd41a074d79446fc4ba2e745c7e5a10a41dbd1d5c2abc86d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b67f2365f86c60d496eb140fde16a0d6fbf89ae6a83d200c6a3971e32eca706b`

```dockerfile
```

-	Layers:
	-	`sha256:e87d247df404b9fe7e19667c95311e8109ea54acdcca2f52ceba73b7099d144e`  
		Last Modified: Wed, 22 Apr 2026 01:25:16 GMT  
		Size: 2.0 MB (2008642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5290960be9e7480bf28bf59599ba02b7792ea80b3309570c3b3a24465ad7d58`  
		Last Modified: Wed, 22 Apr 2026 01:25:16 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; 386

```console
$ docker pull memcached@sha256:0b8f07a6f169bfe4cc362cbabca8c92d5140665660c615383f2755c40c0036f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33670125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd6a79877127262a308ef5f3bd216749c6f0b1fc43971b56c533d4e47f5c6de2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:17:33 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 22 Apr 2026 01:17:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:20:28 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 22 Apr 2026 01:20:28 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 22 Apr 2026 01:20:28 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 22 Apr 2026 01:20:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 22 Apr 2026 01:20:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:20:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:20:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:20:28 GMT
USER memcache
# Wed, 22 Apr 2026 01:20:28 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 Apr 2026 01:20:28 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:dacd7cda306bf5bd7a2030f9b0c2e9d71fda44ea58493a33450d210b74a8ec75`  
		Last Modified: Wed, 22 Apr 2026 00:17:04 GMT  
		Size: 31.3 MB (31296327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a0c9fe363e7e198726a5e39cf627131e43cd59d319a350f978180f6f449b8a`  
		Last Modified: Wed, 22 Apr 2026 01:20:34 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dff2976b24139841065357d1f81c8cf6d9b45ee35e2947f1345e86493b2f5e67`  
		Last Modified: Wed, 22 Apr 2026 01:20:34 GMT  
		Size: 147.5 KB (147529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8b8718f120acc0033835790e0bd541e38b843c6b260688b8fde3c94eadd5911`  
		Last Modified: Wed, 22 Apr 2026 01:20:34 GMT  
		Size: 2.2 MB (2224758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f70ea447cee314191f67e0ce5ccc23703730c89810e26bfa3f96f81964849dc`  
		Last Modified: Wed, 22 Apr 2026 01:20:34 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:789bc1b0beaaf9809e3cab832a0b6b29f50aec3b18f7a7cdf04e343d3ee800a3`  
		Last Modified: Wed, 22 Apr 2026 01:20:35 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:45cfea0c565e5e6c79f4a36cf4ec611ccc7e910c481110b37be04eca3276511b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d33423fad9c4c2f3b1af3eb87b8af48d7cfc9e00d70e6c33937d7d215fb94c5`

```dockerfile
```

-	Layers:
	-	`sha256:2656e01c20323e582a0ba03c06d82008eb35ae9850f7d6c7f73c0e5ae040805b`  
		Last Modified: Wed, 22 Apr 2026 01:20:34 GMT  
		Size: 2.0 MB (2005483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d267990174d3038591d6a8ffe07af06d961bb5c68b86a9cdac459f5a0996ddbe`  
		Last Modified: Wed, 22 Apr 2026 01:20:34 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; ppc64le

```console
$ docker pull memcached@sha256:3df945008f026e1a7782fc67d0107a07c9103d9d50dd7ae605082ea97fb64ff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36164269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7eb2db1cbb0c7ddc2688ee498498fb5122ee78ab349b636a43585b1beb30da9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:35:49 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 22 Apr 2026 01:35:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:39:22 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 22 Apr 2026 01:39:22 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 22 Apr 2026 01:39:22 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 22 Apr 2026 01:39:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 22 Apr 2026 01:39:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:39:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:39:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:39:23 GMT
USER memcache
# Wed, 22 Apr 2026 01:39:23 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 Apr 2026 01:39:23 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b5fd051d0fcd0789e7358cba300f83befdba943416041497be86050e282a6d02`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 33.6 MB (33598032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e271c91c5c30b04dee49fb4c9ab2f9863d13146641f1b8681b59467d0f8ab5`  
		Last Modified: Wed, 22 Apr 2026 01:39:42 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb7fa3c8c45f87e36929f71acaead9bcb07985c205ea0aa6fd83aca31691d78`  
		Last Modified: Wed, 22 Apr 2026 01:39:42 GMT  
		Size: 170.4 KB (170378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f09610f9abffbf6411865ebc07ee20de6c14b2250467c4682f423dddc0ab82`  
		Last Modified: Wed, 22 Apr 2026 01:39:42 GMT  
		Size: 2.4 MB (2394347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a0fb856cc435334489ebeec58afd76f4e676c8bae4b3688daefedfbc7f7c1a8`  
		Last Modified: Wed, 22 Apr 2026 01:39:42 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea36b259fc26e36b99ded4a3aa0ca190c1117ecd424f26565f8474b55964d787`  
		Last Modified: Wed, 22 Apr 2026 01:39:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:c619fe6b2206166796157b814c0d60ca38e29a646b71cd6f5635e2f507cf70d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49e66f35bf963d54f332469bbdef0ca608c651311f5af0e923aca630f4429ae9`

```dockerfile
```

-	Layers:
	-	`sha256:f870fab207e6594315e4d18f50f3ebf834ebc298b6ec128104607668ae939995`  
		Last Modified: Wed, 22 Apr 2026 01:39:42 GMT  
		Size: 2.0 MB (2011927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bf20b8b72f84425e9121a35ea191dab3cf17562679390195740f260304727d7`  
		Last Modified: Wed, 22 Apr 2026 01:39:42 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; riscv64

```console
$ docker pull memcached@sha256:5554043a87027cff145bdb04810a9f8a067c72479937ce0328af056a5c3efe8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30623256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad08d83e675d61f6e230bee3e1d5d5e4b4e8d0b1b3656b71812168b7db5e08e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 08:28:54 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 22 Apr 2026 08:29:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 08:55:11 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 22 Apr 2026 08:55:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 22 Apr 2026 08:55:11 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 22 Apr 2026 08:55:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 22 Apr 2026 08:55:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 08:55:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 08:55:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 08:55:12 GMT
USER memcache
# Wed, 22 Apr 2026 08:55:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 Apr 2026 08:55:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8aa73197c6983c411cf26b41c64a557cfc81f9b4e6d897ff2829a66eac03b37`  
		Last Modified: Wed, 22 Apr 2026 08:55:56 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee379d85ef42145b3f09328c98634e8cd3320230281217ad58867c6982e1d8c`  
		Last Modified: Wed, 22 Apr 2026 08:55:57 GMT  
		Size: 133.1 KB (133094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:310a92cbf1cb95664c58022062af028a81e69f127cd8d9ee044bf7d5087db961`  
		Last Modified: Wed, 22 Apr 2026 08:55:57 GMT  
		Size: 2.2 MB (2208455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336575624802c397f4947f3ddfc2737281bfe2ba8cd714be646b72152c1ec1d0`  
		Last Modified: Wed, 22 Apr 2026 08:55:56 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e926175ab529d298755a0e0507accca74feec6c90ea4495edeaafb07954ad57d`  
		Last Modified: Wed, 22 Apr 2026 08:55:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:9b8b4751f5823830cf382050f0174dd5ade6dc0650b2a3134803b886b2652dba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bc1698424d742c630d5a555fa2c70be3195da5b1a2cd148a331c7aa9fb94b6f`

```dockerfile
```

-	Layers:
	-	`sha256:18aa82332065ff68528148bb97bd5681424d4c57e9e5e331b8908b44023570a9`  
		Last Modified: Wed, 22 Apr 2026 08:55:57 GMT  
		Size: 2.0 MB (2002290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edeefd058e4dbdf6c3026618be5f5184cd3d2c22f14746d890cd45a42004dc8f`  
		Last Modified: Wed, 22 Apr 2026 08:55:57 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; s390x

```console
$ docker pull memcached@sha256:e0fadaa0ad7c323c4f8ead5d8e1ebb9566adc59b25cbc280f40bef816f9d62eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32280559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5d7f2d629511f566dd7c4b3a944adb9989b05bb41dbd3e3881734bc1c1079c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:19:00 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 22 Apr 2026 01:19:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:22:27 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 22 Apr 2026 01:22:27 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 22 Apr 2026 01:22:27 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 22 Apr 2026 01:22:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 22 Apr 2026 01:22:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:22:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:22:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:22:27 GMT
USER memcache
# Wed, 22 Apr 2026 01:22:27 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 Apr 2026 01:22:27 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:71574deb335f1e823f938f4a215de00a90d63866898f1f354a0b15e8b9c30577`  
		Last Modified: Wed, 22 Apr 2026 00:17:08 GMT  
		Size: 29.8 MB (29840300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b460058bd06ca18e629070cadcc158edef16e034340796f661d4fab362ee94`  
		Last Modified: Wed, 22 Apr 2026 01:22:38 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5386c57fa90d49931296cf79f5e8d2ae18d07b9bcffe5eee8354033fee4b673`  
		Last Modified: Wed, 22 Apr 2026 01:22:38 GMT  
		Size: 140.5 KB (140521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd8308c0fc0224d29acef5aadae977dfea2e1ba7c9be0e207ee89c84a4f6417`  
		Last Modified: Wed, 22 Apr 2026 01:22:38 GMT  
		Size: 2.3 MB (2298228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fda405f0b2226447c88ba0d395ee00616ec775cecba66d9a980d4aac7b44fb49`  
		Last Modified: Wed, 22 Apr 2026 01:22:38 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fcaa079ef0e24aab0065df6b15e28d19a0807e2c9cdc639bbc63923135e6daa`  
		Last Modified: Wed, 22 Apr 2026 01:22:39 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:7d2e45f2ecd9448a99f98a077da16fb59c37827c2acbac9e99dea8f79d753165
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54358ef5a62ded9fafc9e908e79d81e5d01102cd4f2082017f54d92232acb7c4`

```dockerfile
```

-	Layers:
	-	`sha256:eb9c1105cc4bf8d4cf2089f7a2a43afe0a113388e7f5a4af9db1f44f9f0fbe11`  
		Last Modified: Wed, 22 Apr 2026 01:22:38 GMT  
		Size: 2.0 MB (2009763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af1c4a20085e6a6f3d2b2fcb2ce9c10456d057c6905b84fe6ad6d99ba351a872`  
		Last Modified: Wed, 22 Apr 2026 01:22:38 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine`

```console
$ docker pull memcached@sha256:65c80b311a9601ef5ca8af3814e5cd06a9c4277ea139d80bd53da6b4d39eb46e
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
$ docker pull memcached@sha256:7b962825022657b112923d502400d5734870d5eb12c19e7f1f6585f7534a6795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5959872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b58f7e71f30daaa3f466fa31d855fddb7101e42c0c42fac520be5d1d43ec32e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:46 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:17:47 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:20:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:20:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:20:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:20:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:20:22 GMT
USER memcache
# Wed, 15 Apr 2026 20:20:22 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:20:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73d5ffe265b83073ce3c7211fb3c15ebbd5e7146d870d9ce69d2e7dfc493348`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6cb4fdd95ced0d5a9528e97ff0f20742749cbd9ef6dc1322d13e682a7085a67`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 106.1 KB (106063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe17fc291d9444fbae93d7f45eab008318f87302c016c06e6e911c1a571a053`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 2.0 MB (1988274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1948bd131d2cbd05c6bf2962d18b15d105abee6f42f398bab3c13737537f197`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bde8ceae30a2a0890715bbc591167ee301c57d7f75023e80be460035187def`  
		Last Modified: Wed, 15 Apr 2026 20:20:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:58ed333482f8a8530c82ad7399d5917a7db85fbcdf70fc1dec55fbedcdf09253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4255278359004afd8c94db1a7fe6129fc984d0716c33665c9eca3168476fdcb`

```dockerfile
```

-	Layers:
	-	`sha256:5f47d88d89d22d065a3590d477ae130520b882176ab07e95862afb4d8b69b214`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 94.9 KB (94901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab2d532e4a6ce2f362d25c79dfaeb88d333fe6efe7c1b5b293630bf6ca292eb8`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 20.5 KB (20530 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:47a06cd0daead339b96ed90e425336a8a49a75e4e358b5ec1ea63a630720f704
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3947facc9e9fae3eee283f24b611a8ae87e353b6d6447bc6f582e90f2fce3743`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:58 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:17:59 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:21:02 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:21:02 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:21:02 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:21:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:21:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:21:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:21:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:21:03 GMT
USER memcache
# Wed, 15 Apr 2026 20:21:03 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:21:03 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77001163fdaab47f07a85fc5bb15f3512a8cb9b9b049cec7e0c88bcbbdb5bb5d`  
		Last Modified: Wed, 15 Apr 2026 20:21:07 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee1b43c0cfbf2ee56e39441933ff06803264d22918fe867d8b5ba7d5adfb9c3`  
		Last Modified: Wed, 15 Apr 2026 20:21:06 GMT  
		Size: 102.6 KB (102630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c041bfac12e599ad87749289dec9672dac36e8c0e16779f13fa695d10f2f0cc5`  
		Last Modified: Wed, 15 Apr 2026 20:21:07 GMT  
		Size: 1.9 MB (1937835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2dfd492dd0f295311a0c314fae06f4b325ae22cb0e673a53e0705f3d4e0504`  
		Last Modified: Wed, 15 Apr 2026 20:21:07 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671c66eac839c2f0a5b2e64d1f581069c4cdf119e784bff16540ecc94e2c2b10`  
		Last Modified: Wed, 15 Apr 2026 20:21:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:2a6148a6aebb042e55781b40ed626d0c5871833be4ae8dc303af7aace07d9d60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbaadfaacfaf0e7c226b35236bb84c2268d4c6eb017efd435a3999a44edfcc77`

```dockerfile
```

-	Layers:
	-	`sha256:c68bb3ee35fc0ac716bca45cc759f3b1ff52b1d5a0acae9876eaf0aa55aa667d`  
		Last Modified: Wed, 15 Apr 2026 20:21:06 GMT  
		Size: 20.5 KB (20466 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:fb58bae12ffa00c9cbafc8bee2341b43ffdccacbde7085fa707ef6c7f2d69e37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5273034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddd4e85c30e4df5803b553b8a7f84084c3dae6f72531ac70fcabf7099cfa8148`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 21:14:38 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 21:14:39 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 21:17:34 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 21:17:34 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 21:17:34 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 21:17:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 21:17:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:17:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 21:17:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:17:34 GMT
USER memcache
# Wed, 15 Apr 2026 21:17:34 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 21:17:34 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e312136cfedda9620407d42650d0595220e60d3c40ae8853bfbdd83f392b9e6`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53697a39f37b691917c91310ac4e107308674bddcc9017e3bbc0d0134eaf4c3e`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 92.4 KB (92369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5e4be9e0df543f152c376fe2cc74b89b75585793fdbd7d12476737d386d8e1`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 1.9 MB (1896191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a083f41edf5f859feb4367eeeea0955dc9799c8202fb8a67c40915ed5b195002`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c43503b1f4f42ffc5e0e4415befe45199dec730bc26347df151298345ba640`  
		Last Modified: Wed, 15 Apr 2026 21:17:40 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7535cf6b6a140771131c2c524301d4616f34856fcd8ecbe3e52300108c49de2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d73c906894a0a3d178edd69991f310225c0daef314e6faa83a0b9adecfbeb34`

```dockerfile
```

-	Layers:
	-	`sha256:8f1fddd7d14560fb90f381b09cde9302dfc9253e6702adf28c55961d755b1ad8`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 94.3 KB (94319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fcf119d246607aa25330c4c05fe14a64cebda69b02d14507862a9f07c1404e6`  
		Last Modified: Wed, 15 Apr 2026 21:17:38 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:6d70439467a65065c52894232a3085c724da2810a9b3205130d5e434ab411e3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6288798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4be3e105216d2507b68e772f7d08d52a5076dd55fad35c29775038d05c24112`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:15:23 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:15:24 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:18:13 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:18:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:18:13 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:18:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:18:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:18:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:18:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:18:13 GMT
USER memcache
# Wed, 15 Apr 2026 20:18:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:18:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81758f5fc2e8fa13e3625f253d7c999560ac666121c026f7251dbfb919cca611`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d735737d3a0cf1eda63bd72c09f64eb679313e9c5f8a105849848bdd779e1d`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 121.8 KB (121846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ac0921d2cc2b3388e0f006a6672c5a9e1098a59e570121dde092104d845c51`  
		Last Modified: Wed, 15 Apr 2026 20:18:19 GMT  
		Size: 2.0 MB (1965733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca9cf731b18a76c3ac25cc3add219660d57516c12680d7b1f1ece282406eb82`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:717a6b23dd1cd76b686bf26066af23265e0d002ed6a3e87f6aa4f79264b7da11`  
		Last Modified: Wed, 15 Apr 2026 20:18:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7e5232b868d3222e3ce2b0ee39c62f6cb294bea27456b00940fbc4e3c8c3f84d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:780bf975a24d5fdc511c857720c04cb077d64abcfe4c93ea0db7c9487c323718`

```dockerfile
```

-	Layers:
	-	`sha256:addb0f46e3b5adb674175c11fc85526d4628e24d74d210c8b00c9a945b44407c`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 94.4 KB (94355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3364e418b74b6f6ca17deec7d55783a6e1554de3783ab0a6d5e56496d935ddb0`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 20.7 KB (20728 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; 386

```console
$ docker pull memcached@sha256:80328bf779fa1494f7677b441ad1c16c2134f126e6556953deb3cfab1c4c9770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5744816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d957405dd0811f1cd15fe39563938a60c2008204d2f63ebc7e39f8989c796f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 22:20:45 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 22:20:46 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 22:23:32 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 22:23:32 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 22:23:32 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 22:23:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 22:23:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 22:23:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 22:23:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 22:23:32 GMT
USER memcache
# Wed, 15 Apr 2026 22:23:32 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 22:23:32 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0617a09eee85c2032f5596ded56b733366513074f9096177315b50dc45485e20`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c67275dbc381ac3ae0b21dda20edaf245e2ca54d6f5dc3af8805db03c17cc93`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 110.7 KB (110715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6ecb23f1f4bc89d5c315aac493f29fe7bb33061c70d926c904f4f55d374461`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 1.9 MB (1942309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e782df8f482a58603ea70ef9e04e838d044a6070c7e4cd116c90a09b917ed940`  
		Last Modified: Wed, 15 Apr 2026 22:23:38 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616df56d574e39c00ae772c6a29e2b724698048a83cc29ea17049573f9073b10`  
		Last Modified: Wed, 15 Apr 2026 22:23:38 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:c726e7abf461d963e544818339e4cd12fd2f31e41436475f0e51818a0885fbdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12e41b9d6f745d686c2649255bd14fe4e0b97a3477d383e719490e5ef66b27ae`

```dockerfile
```

-	Layers:
	-	`sha256:b44003cd1ea209090a063c5abfb4ee881849abba47e8711191b7637f86d8ee8b`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 94.9 KB (94856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f431de53d9b6c7e2cbc847af9daec064d061f8bd625615734012051336c495a`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 20.5 KB (20472 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:8182e35a9a404f0b522cb3c176d3dc4aade974e5556184c0a5a19e800721868a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6034321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30c6f532e81b50ea71c3520a80da0c8154b4cb14ebc17f87eb3a026862b47ed8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:41 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:17:43 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:20:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:20:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:20:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:20:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:20:22 GMT
USER memcache
# Wed, 15 Apr 2026 20:20:22 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:20:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee88d1c88fa46aa906a297c2919c9a085e74d04f20e4f827ca240a20f10ad34`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c574329cc1ebf156e2d89ab608bd58a3c0db550845c0ec394d265aa98fc5c4`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 126.3 KB (126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc2a28510bcba91734e7b38682847296011b63458db8a87a4bcecd180b8de7b5`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 2.1 MB (2075767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c524eb15ef0a41bf969efc93ef579db92dc59e8df57c9abfd099e7f6ff0756`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bde8ceae30a2a0890715bbc591167ee301c57d7f75023e80be460035187def`  
		Last Modified: Wed, 15 Apr 2026 20:20:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:4051408ef6c5bf4d4f37abf19c13f0298d8baa81770fcbfb588221e49e3bb834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ec3a4d49e6f325e484db43c9c9981f4eaa0223d9ae98282d95c3ee20c2089cb`

```dockerfile
```

-	Layers:
	-	`sha256:0e4e65db585f857844a67a831eb876dbb0a8a40d9269393d6c0fa83a2df995ae`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 94.3 KB (94308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50f58ec8aff3c96cc7b58e689122c27ee26121c598034cdc59ec95fd6423effe`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:f3209d1ca2c4ce827614d16445231d96372944d218f18fd22850eec83874e5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5772332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e30170e0826b89d0ca59ffcae54b850ded07e6ae9451ecf1fd60f3ca8adcc725`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2026 00:00:48 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 16 Apr 2026 00:00:52 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 16 Apr 2026 00:14:21 GMT
ENV MEMCACHED_VERSION=1.6.41
# Thu, 16 Apr 2026 00:14:21 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Thu, 16 Apr 2026 00:14:21 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Thu, 16 Apr 2026 00:14:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 16 Apr 2026 00:14:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Apr 2026 00:14:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 16 Apr 2026 00:14:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Apr 2026 00:14:22 GMT
USER memcache
# Thu, 16 Apr 2026 00:14:22 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 16 Apr 2026 00:14:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62b143e34f5b89277e3a88ed4d722339d188a094d4bb534e222ca80e7741031`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bfff7c64f831ba03c491874cdf9a1c3f42bff72bb0e1951c63d8cf718854cff`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 108.9 KB (108903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69aef1050272a61cfbfd97c041d3776f96bdd03b102f2c3c54bbb0af2e1235a5`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 2.1 MB (2074414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ce340fb37f86db0d3aa774c23880b7c8322d2af8e3adc27a6ffa25d67c2122`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e40c6fb92d819994d38fae7accdffd583465eb6e645834b66f3ce9f0562f69`  
		Last Modified: Thu, 16 Apr 2026 00:14:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:2caae198d1efb7d4df14da45a3ff360a697982b544a61a3f907076b414983ea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1503bd38f4b30bc91be18dd93359e7376a9da1c7cb652ade64efd154064543fe`

```dockerfile
```

-	Layers:
	-	`sha256:e2d79fb634d76e28f055ab09953f59c371b93599e2b79f20f3d758f2c9520118`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 94.3 KB (94304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3614ad9b1715c3d6aa488496fca74d7143ea095d227f599407c933c62ec266aa`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 20.6 KB (20604 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:1da27660ae89a83aaf603e1affd51be573e5b8dac6c07ed592aee2a3a2b20581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5859702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13aa64df69a308e46b054bbd8e7a5d2f1e079005771f61748dae0d049889ba7f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:14:40 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:14:41 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:17:58 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:17:58 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:17:58 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:17:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:17:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:17:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:17:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:17:58 GMT
USER memcache
# Wed, 15 Apr 2026 20:17:58 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:17:58 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c42733e5f451590186b9b76c4b374ae5a84b657f7f1fd405647f5ba82c65bcd`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a14431ac88e8fe205b07f09b7e4843bb254de41cbc044725d6eaee3c2f822f`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 114.3 KB (114293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6377b7d98f32173cd47682aa73b32e4eba42781fa9224b9eb7a6f87367d37f94`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 2.0 MB (2017525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d022ae992296922747a4b69694b0185a0ce1f6cdece7f794e39e74dab92d250`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255cb3a435cbd623c1235d0429160faf72c244a6c1a613525df36f58a8c1f784`  
		Last Modified: Wed, 15 Apr 2026 20:18:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:531ee140f06db77d73b71bce7339abec3c6d976092bb80542bb337bb406acdbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b17d6f7e71efe3ee05ebcdb8ae90c28cf60db9ef069b0a98fe442c949740a6c`

```dockerfile
```

-	Layers:
	-	`sha256:820a080f49bf9e33948dbe5c13f6254f135d90bcb2b2277e3d2fd2430626c1a2`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 94.2 KB (94250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8ab82f4f240f46f9e34b74691925ab4af7f1cbb12ad3cb8639e0f317cf06653`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine3.23`

```console
$ docker pull memcached@sha256:65c80b311a9601ef5ca8af3814e5cd06a9c4277ea139d80bd53da6b4d39eb46e
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
$ docker pull memcached@sha256:7b962825022657b112923d502400d5734870d5eb12c19e7f1f6585f7534a6795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5959872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b58f7e71f30daaa3f466fa31d855fddb7101e42c0c42fac520be5d1d43ec32e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:46 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:17:47 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:20:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:20:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:20:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:20:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:20:22 GMT
USER memcache
# Wed, 15 Apr 2026 20:20:22 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:20:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73d5ffe265b83073ce3c7211fb3c15ebbd5e7146d870d9ce69d2e7dfc493348`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6cb4fdd95ced0d5a9528e97ff0f20742749cbd9ef6dc1322d13e682a7085a67`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 106.1 KB (106063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe17fc291d9444fbae93d7f45eab008318f87302c016c06e6e911c1a571a053`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 2.0 MB (1988274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1948bd131d2cbd05c6bf2962d18b15d105abee6f42f398bab3c13737537f197`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bde8ceae30a2a0890715bbc591167ee301c57d7f75023e80be460035187def`  
		Last Modified: Wed, 15 Apr 2026 20:20:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:58ed333482f8a8530c82ad7399d5917a7db85fbcdf70fc1dec55fbedcdf09253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4255278359004afd8c94db1a7fe6129fc984d0716c33665c9eca3168476fdcb`

```dockerfile
```

-	Layers:
	-	`sha256:5f47d88d89d22d065a3590d477ae130520b882176ab07e95862afb4d8b69b214`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 94.9 KB (94901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab2d532e4a6ce2f362d25c79dfaeb88d333fe6efe7c1b5b293630bf6ca292eb8`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 20.5 KB (20530 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.23` - linux; arm variant v6

```console
$ docker pull memcached@sha256:47a06cd0daead339b96ed90e425336a8a49a75e4e358b5ec1ea63a630720f704
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3947facc9e9fae3eee283f24b611a8ae87e353b6d6447bc6f582e90f2fce3743`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:58 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:17:59 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:21:02 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:21:02 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:21:02 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:21:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:21:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:21:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:21:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:21:03 GMT
USER memcache
# Wed, 15 Apr 2026 20:21:03 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:21:03 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77001163fdaab47f07a85fc5bb15f3512a8cb9b9b049cec7e0c88bcbbdb5bb5d`  
		Last Modified: Wed, 15 Apr 2026 20:21:07 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee1b43c0cfbf2ee56e39441933ff06803264d22918fe867d8b5ba7d5adfb9c3`  
		Last Modified: Wed, 15 Apr 2026 20:21:06 GMT  
		Size: 102.6 KB (102630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c041bfac12e599ad87749289dec9672dac36e8c0e16779f13fa695d10f2f0cc5`  
		Last Modified: Wed, 15 Apr 2026 20:21:07 GMT  
		Size: 1.9 MB (1937835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2dfd492dd0f295311a0c314fae06f4b325ae22cb0e673a53e0705f3d4e0504`  
		Last Modified: Wed, 15 Apr 2026 20:21:07 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671c66eac839c2f0a5b2e64d1f581069c4cdf119e784bff16540ecc94e2c2b10`  
		Last Modified: Wed, 15 Apr 2026 20:21:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:2a6148a6aebb042e55781b40ed626d0c5871833be4ae8dc303af7aace07d9d60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbaadfaacfaf0e7c226b35236bb84c2268d4c6eb017efd435a3999a44edfcc77`

```dockerfile
```

-	Layers:
	-	`sha256:c68bb3ee35fc0ac716bca45cc759f3b1ff52b1d5a0acae9876eaf0aa55aa667d`  
		Last Modified: Wed, 15 Apr 2026 20:21:06 GMT  
		Size: 20.5 KB (20466 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.23` - linux; arm variant v7

```console
$ docker pull memcached@sha256:fb58bae12ffa00c9cbafc8bee2341b43ffdccacbde7085fa707ef6c7f2d69e37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5273034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddd4e85c30e4df5803b553b8a7f84084c3dae6f72531ac70fcabf7099cfa8148`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 21:14:38 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 21:14:39 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 21:17:34 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 21:17:34 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 21:17:34 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 21:17:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 21:17:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:17:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 21:17:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:17:34 GMT
USER memcache
# Wed, 15 Apr 2026 21:17:34 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 21:17:34 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e312136cfedda9620407d42650d0595220e60d3c40ae8853bfbdd83f392b9e6`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53697a39f37b691917c91310ac4e107308674bddcc9017e3bbc0d0134eaf4c3e`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 92.4 KB (92369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5e4be9e0df543f152c376fe2cc74b89b75585793fdbd7d12476737d386d8e1`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 1.9 MB (1896191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a083f41edf5f859feb4367eeeea0955dc9799c8202fb8a67c40915ed5b195002`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c43503b1f4f42ffc5e0e4415befe45199dec730bc26347df151298345ba640`  
		Last Modified: Wed, 15 Apr 2026 21:17:40 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:7535cf6b6a140771131c2c524301d4616f34856fcd8ecbe3e52300108c49de2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d73c906894a0a3d178edd69991f310225c0daef314e6faa83a0b9adecfbeb34`

```dockerfile
```

-	Layers:
	-	`sha256:8f1fddd7d14560fb90f381b09cde9302dfc9253e6702adf28c55961d755b1ad8`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 94.3 KB (94319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fcf119d246607aa25330c4c05fe14a64cebda69b02d14507862a9f07c1404e6`  
		Last Modified: Wed, 15 Apr 2026 21:17:38 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:6d70439467a65065c52894232a3085c724da2810a9b3205130d5e434ab411e3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6288798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4be3e105216d2507b68e772f7d08d52a5076dd55fad35c29775038d05c24112`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:15:23 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:15:24 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:18:13 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:18:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:18:13 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:18:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:18:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:18:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:18:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:18:13 GMT
USER memcache
# Wed, 15 Apr 2026 20:18:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:18:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81758f5fc2e8fa13e3625f253d7c999560ac666121c026f7251dbfb919cca611`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d735737d3a0cf1eda63bd72c09f64eb679313e9c5f8a105849848bdd779e1d`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 121.8 KB (121846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ac0921d2cc2b3388e0f006a6672c5a9e1098a59e570121dde092104d845c51`  
		Last Modified: Wed, 15 Apr 2026 20:18:19 GMT  
		Size: 2.0 MB (1965733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca9cf731b18a76c3ac25cc3add219660d57516c12680d7b1f1ece282406eb82`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:717a6b23dd1cd76b686bf26066af23265e0d002ed6a3e87f6aa4f79264b7da11`  
		Last Modified: Wed, 15 Apr 2026 20:18:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:7e5232b868d3222e3ce2b0ee39c62f6cb294bea27456b00940fbc4e3c8c3f84d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:780bf975a24d5fdc511c857720c04cb077d64abcfe4c93ea0db7c9487c323718`

```dockerfile
```

-	Layers:
	-	`sha256:addb0f46e3b5adb674175c11fc85526d4628e24d74d210c8b00c9a945b44407c`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 94.4 KB (94355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3364e418b74b6f6ca17deec7d55783a6e1554de3783ab0a6d5e56496d935ddb0`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 20.7 KB (20728 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.23` - linux; 386

```console
$ docker pull memcached@sha256:80328bf779fa1494f7677b441ad1c16c2134f126e6556953deb3cfab1c4c9770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5744816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d957405dd0811f1cd15fe39563938a60c2008204d2f63ebc7e39f8989c796f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 22:20:45 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 22:20:46 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 22:23:32 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 22:23:32 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 22:23:32 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 22:23:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 22:23:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 22:23:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 22:23:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 22:23:32 GMT
USER memcache
# Wed, 15 Apr 2026 22:23:32 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 22:23:32 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0617a09eee85c2032f5596ded56b733366513074f9096177315b50dc45485e20`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c67275dbc381ac3ae0b21dda20edaf245e2ca54d6f5dc3af8805db03c17cc93`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 110.7 KB (110715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6ecb23f1f4bc89d5c315aac493f29fe7bb33061c70d926c904f4f55d374461`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 1.9 MB (1942309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e782df8f482a58603ea70ef9e04e838d044a6070c7e4cd116c90a09b917ed940`  
		Last Modified: Wed, 15 Apr 2026 22:23:38 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616df56d574e39c00ae772c6a29e2b724698048a83cc29ea17049573f9073b10`  
		Last Modified: Wed, 15 Apr 2026 22:23:38 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:c726e7abf461d963e544818339e4cd12fd2f31e41436475f0e51818a0885fbdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12e41b9d6f745d686c2649255bd14fe4e0b97a3477d383e719490e5ef66b27ae`

```dockerfile
```

-	Layers:
	-	`sha256:b44003cd1ea209090a063c5abfb4ee881849abba47e8711191b7637f86d8ee8b`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 94.9 KB (94856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f431de53d9b6c7e2cbc847af9daec064d061f8bd625615734012051336c495a`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 20.5 KB (20472 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.23` - linux; ppc64le

```console
$ docker pull memcached@sha256:8182e35a9a404f0b522cb3c176d3dc4aade974e5556184c0a5a19e800721868a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6034321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30c6f532e81b50ea71c3520a80da0c8154b4cb14ebc17f87eb3a026862b47ed8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:41 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:17:43 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:20:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:20:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:20:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:20:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:20:22 GMT
USER memcache
# Wed, 15 Apr 2026 20:20:22 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:20:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee88d1c88fa46aa906a297c2919c9a085e74d04f20e4f827ca240a20f10ad34`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c574329cc1ebf156e2d89ab608bd58a3c0db550845c0ec394d265aa98fc5c4`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 126.3 KB (126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc2a28510bcba91734e7b38682847296011b63458db8a87a4bcecd180b8de7b5`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 2.1 MB (2075767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c524eb15ef0a41bf969efc93ef579db92dc59e8df57c9abfd099e7f6ff0756`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bde8ceae30a2a0890715bbc591167ee301c57d7f75023e80be460035187def`  
		Last Modified: Wed, 15 Apr 2026 20:20:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:4051408ef6c5bf4d4f37abf19c13f0298d8baa81770fcbfb588221e49e3bb834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ec3a4d49e6f325e484db43c9c9981f4eaa0223d9ae98282d95c3ee20c2089cb`

```dockerfile
```

-	Layers:
	-	`sha256:0e4e65db585f857844a67a831eb876dbb0a8a40d9269393d6c0fa83a2df995ae`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 94.3 KB (94308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50f58ec8aff3c96cc7b58e689122c27ee26121c598034cdc59ec95fd6423effe`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.23` - linux; riscv64

```console
$ docker pull memcached@sha256:f3209d1ca2c4ce827614d16445231d96372944d218f18fd22850eec83874e5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5772332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e30170e0826b89d0ca59ffcae54b850ded07e6ae9451ecf1fd60f3ca8adcc725`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2026 00:00:48 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 16 Apr 2026 00:00:52 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 16 Apr 2026 00:14:21 GMT
ENV MEMCACHED_VERSION=1.6.41
# Thu, 16 Apr 2026 00:14:21 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Thu, 16 Apr 2026 00:14:21 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Thu, 16 Apr 2026 00:14:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 16 Apr 2026 00:14:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Apr 2026 00:14:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 16 Apr 2026 00:14:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Apr 2026 00:14:22 GMT
USER memcache
# Thu, 16 Apr 2026 00:14:22 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 16 Apr 2026 00:14:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62b143e34f5b89277e3a88ed4d722339d188a094d4bb534e222ca80e7741031`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bfff7c64f831ba03c491874cdf9a1c3f42bff72bb0e1951c63d8cf718854cff`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 108.9 KB (108903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69aef1050272a61cfbfd97c041d3776f96bdd03b102f2c3c54bbb0af2e1235a5`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 2.1 MB (2074414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ce340fb37f86db0d3aa774c23880b7c8322d2af8e3adc27a6ffa25d67c2122`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e40c6fb92d819994d38fae7accdffd583465eb6e645834b66f3ce9f0562f69`  
		Last Modified: Thu, 16 Apr 2026 00:14:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:2caae198d1efb7d4df14da45a3ff360a697982b544a61a3f907076b414983ea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1503bd38f4b30bc91be18dd93359e7376a9da1c7cb652ade64efd154064543fe`

```dockerfile
```

-	Layers:
	-	`sha256:e2d79fb634d76e28f055ab09953f59c371b93599e2b79f20f3d758f2c9520118`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 94.3 KB (94304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3614ad9b1715c3d6aa488496fca74d7143ea095d227f599407c933c62ec266aa`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 20.6 KB (20604 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.23` - linux; s390x

```console
$ docker pull memcached@sha256:1da27660ae89a83aaf603e1affd51be573e5b8dac6c07ed592aee2a3a2b20581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5859702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13aa64df69a308e46b054bbd8e7a5d2f1e079005771f61748dae0d049889ba7f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:14:40 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:14:41 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:17:58 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:17:58 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:17:58 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:17:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:17:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:17:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:17:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:17:58 GMT
USER memcache
# Wed, 15 Apr 2026 20:17:58 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:17:58 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c42733e5f451590186b9b76c4b374ae5a84b657f7f1fd405647f5ba82c65bcd`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a14431ac88e8fe205b07f09b7e4843bb254de41cbc044725d6eaee3c2f822f`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 114.3 KB (114293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6377b7d98f32173cd47682aa73b32e4eba42781fa9224b9eb7a6f87367d37f94`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 2.0 MB (2017525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d022ae992296922747a4b69694b0185a0ce1f6cdece7f794e39e74dab92d250`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255cb3a435cbd623c1235d0429160faf72c244a6c1a613525df36f58a8c1f784`  
		Last Modified: Wed, 15 Apr 2026 20:18:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:531ee140f06db77d73b71bce7339abec3c6d976092bb80542bb337bb406acdbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b17d6f7e71efe3ee05ebcdb8ae90c28cf60db9ef069b0a98fe442c949740a6c`

```dockerfile
```

-	Layers:
	-	`sha256:820a080f49bf9e33948dbe5c13f6254f135d90bcb2b2277e3d2fd2430626c1a2`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 94.2 KB (94250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8ab82f4f240f46f9e34b74691925ab4af7f1cbb12ad3cb8639e0f317cf06653`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-trixie`

```console
$ docker pull memcached@sha256:277e0c4f249b118e95ab10e535bae2fa1af772271d9152f3468e58d59348db56
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
$ docker pull memcached@sha256:518f136cafc43439a777c20224d30b6fadc3433e3de9573f514dca10dd7e0082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32198630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ec7b3eba028951d3aeee1ef26a365c913edaf06de6c008653f175c0ff0078ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:21:37 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 22 Apr 2026 01:21:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:24:27 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 22 Apr 2026 01:24:27 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 22 Apr 2026 01:24:27 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 22 Apr 2026 01:24:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 22 Apr 2026 01:24:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:24:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:24:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:24:27 GMT
USER memcache
# Wed, 22 Apr 2026 01:24:27 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 Apr 2026 01:24:27 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53e27a8dc2608bcd39496d6e1a0a021aa8933953409444f778d810ec220ab89`  
		Last Modified: Wed, 22 Apr 2026 01:24:33 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d02c07f7ffb4ea4d70b3af1ed59da72e778c143718ba2a7bcb8cd6d12afd95b`  
		Last Modified: Wed, 22 Apr 2026 01:24:33 GMT  
		Size: 136.7 KB (136658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b1a619145ef14a0e4599b98a19dbdc4fc96cfdf359ecf816454cd80ccf2dd2`  
		Last Modified: Wed, 22 Apr 2026 01:24:34 GMT  
		Size: 2.3 MB (2280287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7716efee154a639ac02ada0d1638837bb72c3fc33ecac40f78ffb91daf9dfc5`  
		Last Modified: Wed, 22 Apr 2026 01:24:34 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712f24abcdc2a432d57253a569a16eddd36ff1f8a4ace323467cdb642eae2850`  
		Last Modified: Wed, 22 Apr 2026 01:24:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:f32546667bf4926fd4e7c91aa55a833e8636777f2aa68437cb2bc7a5330e2307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3700c2c8b8182ac20db287282cdafbde42f55966784e109b48a9e5c2ba4d7492`

```dockerfile
```

-	Layers:
	-	`sha256:a3fe3f55746c35c0a798536b5abfc78349217684ca67ba43649a1c86d2a6ebe3`  
		Last Modified: Wed, 22 Apr 2026 01:24:33 GMT  
		Size: 2.0 MB (2008326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0b151a6f180676864b1e8721dddbaf0c105e743520356d58f7df86572a295fa`  
		Last Modified: Wed, 22 Apr 2026 01:24:33 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; arm variant v5

```console
$ docker pull memcached@sha256:4b91aeabb9b5d253e27cc0e6f6fa6cc82780c4d686f484c9ed1057a1dd429ba2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30305389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e62e4552c0bfc9dd8f4797df2c1386943df5780d342654ed3050e75668231e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:17:31 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 22 Apr 2026 01:17:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:20:57 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 22 Apr 2026 01:20:57 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 22 Apr 2026 01:20:57 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 22 Apr 2026 01:20:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 22 Apr 2026 01:20:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:20:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:20:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:20:57 GMT
USER memcache
# Wed, 22 Apr 2026 01:20:57 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 Apr 2026 01:20:57 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6496d93bca0663211b9252da346044ecb734ee5b3ecaae5b1fbd230753faee2f`  
		Last Modified: Wed, 22 Apr 2026 00:15:59 GMT  
		Size: 27.9 MB (27948180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64cdc01a23d15e84ef2ee2165c1a90970fb54d98f29377fa63fbd82988cdcc40`  
		Last Modified: Wed, 22 Apr 2026 01:21:03 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:303fc6e2ad4e0da497f7e238e61ec9e1fbde60909262de4a50e05c4db2191602`  
		Last Modified: Wed, 22 Apr 2026 01:21:03 GMT  
		Size: 144.2 KB (144163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c438ec3169ba426bc8374ca37b4f159272d50b60173c35c396f8fbf2208b8806`  
		Last Modified: Wed, 22 Apr 2026 01:21:03 GMT  
		Size: 2.2 MB (2211533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b5512f6aab6e3147798ce406f1035f68f18c2dd046b5fdd6344a17ace7fb31`  
		Last Modified: Wed, 22 Apr 2026 01:21:03 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a320e8acb7760a30eb688cd929fda03bf41ba23a307e06071106c3c0415d03`  
		Last Modified: Wed, 22 Apr 2026 01:21:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:4faa0397c26f0f4a312a28578db40b0f95f89c09769520c7cc09900886412dd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af54d9e6dbb4f86d5a79e417071faea8dd939b7758f640ce360a49c55069e2eb`

```dockerfile
```

-	Layers:
	-	`sha256:1850a912cc062cca1f70a2b76861d54c0ad06921d2a4960a7c483b5f8820eaa1`  
		Last Modified: Wed, 22 Apr 2026 01:21:03 GMT  
		Size: 2.0 MB (2011329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02fdad23f354f6597bfec3258d6bbee5142bcce9e1faaa7de87f9859bf8c6d14`  
		Last Modified: Wed, 22 Apr 2026 01:21:03 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; arm variant v7

```console
$ docker pull memcached@sha256:4d262b60fea5a97e91a6c1827ab7209a344c47616388ada79b27e4e69eea9d38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28516774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02f2f7426f06caeeb218b724a947fa35544b0749bacf781227878e40cb98d08f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:18:06 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 22 Apr 2026 01:18:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:21:19 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 22 Apr 2026 01:21:19 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 22 Apr 2026 01:21:19 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 22 Apr 2026 01:21:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 22 Apr 2026 01:21:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:21:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:21:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:21:19 GMT
USER memcache
# Wed, 22 Apr 2026 01:21:19 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 Apr 2026 01:21:19 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9e541e5bfbbe69b7bbe01cd2f1abf8560e2e43bf76eb96b2e88a3df29020834b`  
		Last Modified: Wed, 22 Apr 2026 00:17:02 GMT  
		Size: 26.2 MB (26214838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0867e20c7ab47539b3f27abc4c7f4bf41d367127d9ffbd30a531ab387a69e2e`  
		Last Modified: Wed, 22 Apr 2026 01:21:25 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34eedf23d5ae4af59fe6ecfd854e48545ede507ce44d930cea5c11b652b31f4`  
		Last Modified: Wed, 22 Apr 2026 01:21:25 GMT  
		Size: 135.4 KB (135382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fff54fd1447de9c8b377640a2720588785769320b1a65d59a1da8e9690e6f9`  
		Last Modified: Wed, 22 Apr 2026 01:21:25 GMT  
		Size: 2.2 MB (2165043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac214a1bada6a999cda6b6b021b8ef5ba954108062e3ee4df0161a500fc566f`  
		Last Modified: Wed, 22 Apr 2026 01:21:25 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0431aacefa9d6f210c7c4778e75df5a21c196127779acc2da1bd7b32088f47dc`  
		Last Modified: Wed, 22 Apr 2026 01:21:26 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:e4f840cb65bd892b2aafc305cb008de10d4d41475876ef9c9bbf51831f9cd7e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:987452d71cfba90bac820fca09f2954a061813125a8832038df5c062224577c5`

```dockerfile
```

-	Layers:
	-	`sha256:f5793a9489c1e1010726124554d7404a19b2675ce8596a38169b160edc81d045`  
		Last Modified: Wed, 22 Apr 2026 01:21:25 GMT  
		Size: 2.0 MB (2009786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef3c23077c5adc1a06a0e1f66d0ec1e57032a5b35685c53064098e236a62c5a1`  
		Last Modified: Wed, 22 Apr 2026 01:21:25 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:52e2a52a542b0fff64533e7271ce3af9825a80a1126998cf6070b0ec4c0030b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32560736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c3fcfefa704f0162e85ab03d515502e07a6ff91ec994dc4b6c956cc2ce80990`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:22:08 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 22 Apr 2026 01:22:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:25:10 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 22 Apr 2026 01:25:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 22 Apr 2026 01:25:10 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 22 Apr 2026 01:25:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 22 Apr 2026 01:25:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:25:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:25:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:25:10 GMT
USER memcache
# Wed, 22 Apr 2026 01:25:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 Apr 2026 01:25:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebea5231ebe63bff9044a4ee7713dac1b62fc15d85ee920f04eae4010a67b668`  
		Last Modified: Wed, 22 Apr 2026 01:25:16 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5921030f644563277c2af1be27b21dfded0e01763210710efac613f07dc74c`  
		Last Modified: Wed, 22 Apr 2026 01:25:16 GMT  
		Size: 153.5 KB (153515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1ef7f1deafd8e81fec98af35ef4fe12c2436c1eddb6bb87377b83f524f7d6f`  
		Last Modified: Wed, 22 Apr 2026 01:25:16 GMT  
		Size: 2.3 MB (2262106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd4f58ffc6f10cea1171fbb552aff0b93a04aba0ca6815cd9ad66ab3a49f8419`  
		Last Modified: Wed, 22 Apr 2026 01:25:16 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace7ea462603345a875235135df0b8dd036890eacdb25150c1a8089604e3ca1f`  
		Last Modified: Wed, 22 Apr 2026 01:25:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:63aba0d160ad2159dd41a074d79446fc4ba2e745c7e5a10a41dbd1d5c2abc86d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b67f2365f86c60d496eb140fde16a0d6fbf89ae6a83d200c6a3971e32eca706b`

```dockerfile
```

-	Layers:
	-	`sha256:e87d247df404b9fe7e19667c95311e8109ea54acdcca2f52ceba73b7099d144e`  
		Last Modified: Wed, 22 Apr 2026 01:25:16 GMT  
		Size: 2.0 MB (2008642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5290960be9e7480bf28bf59599ba02b7792ea80b3309570c3b3a24465ad7d58`  
		Last Modified: Wed, 22 Apr 2026 01:25:16 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; 386

```console
$ docker pull memcached@sha256:0b8f07a6f169bfe4cc362cbabca8c92d5140665660c615383f2755c40c0036f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33670125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd6a79877127262a308ef5f3bd216749c6f0b1fc43971b56c533d4e47f5c6de2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:17:33 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 22 Apr 2026 01:17:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:20:28 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 22 Apr 2026 01:20:28 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 22 Apr 2026 01:20:28 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 22 Apr 2026 01:20:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 22 Apr 2026 01:20:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:20:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:20:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:20:28 GMT
USER memcache
# Wed, 22 Apr 2026 01:20:28 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 Apr 2026 01:20:28 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:dacd7cda306bf5bd7a2030f9b0c2e9d71fda44ea58493a33450d210b74a8ec75`  
		Last Modified: Wed, 22 Apr 2026 00:17:04 GMT  
		Size: 31.3 MB (31296327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a0c9fe363e7e198726a5e39cf627131e43cd59d319a350f978180f6f449b8a`  
		Last Modified: Wed, 22 Apr 2026 01:20:34 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dff2976b24139841065357d1f81c8cf6d9b45ee35e2947f1345e86493b2f5e67`  
		Last Modified: Wed, 22 Apr 2026 01:20:34 GMT  
		Size: 147.5 KB (147529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8b8718f120acc0033835790e0bd541e38b843c6b260688b8fde3c94eadd5911`  
		Last Modified: Wed, 22 Apr 2026 01:20:34 GMT  
		Size: 2.2 MB (2224758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f70ea447cee314191f67e0ce5ccc23703730c89810e26bfa3f96f81964849dc`  
		Last Modified: Wed, 22 Apr 2026 01:20:34 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:789bc1b0beaaf9809e3cab832a0b6b29f50aec3b18f7a7cdf04e343d3ee800a3`  
		Last Modified: Wed, 22 Apr 2026 01:20:35 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:45cfea0c565e5e6c79f4a36cf4ec611ccc7e910c481110b37be04eca3276511b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d33423fad9c4c2f3b1af3eb87b8af48d7cfc9e00d70e6c33937d7d215fb94c5`

```dockerfile
```

-	Layers:
	-	`sha256:2656e01c20323e582a0ba03c06d82008eb35ae9850f7d6c7f73c0e5ae040805b`  
		Last Modified: Wed, 22 Apr 2026 01:20:34 GMT  
		Size: 2.0 MB (2005483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d267990174d3038591d6a8ffe07af06d961bb5c68b86a9cdac459f5a0996ddbe`  
		Last Modified: Wed, 22 Apr 2026 01:20:34 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; ppc64le

```console
$ docker pull memcached@sha256:3df945008f026e1a7782fc67d0107a07c9103d9d50dd7ae605082ea97fb64ff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36164269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7eb2db1cbb0c7ddc2688ee498498fb5122ee78ab349b636a43585b1beb30da9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:35:49 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 22 Apr 2026 01:35:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:39:22 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 22 Apr 2026 01:39:22 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 22 Apr 2026 01:39:22 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 22 Apr 2026 01:39:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 22 Apr 2026 01:39:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:39:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:39:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:39:23 GMT
USER memcache
# Wed, 22 Apr 2026 01:39:23 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 Apr 2026 01:39:23 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b5fd051d0fcd0789e7358cba300f83befdba943416041497be86050e282a6d02`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 33.6 MB (33598032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e271c91c5c30b04dee49fb4c9ab2f9863d13146641f1b8681b59467d0f8ab5`  
		Last Modified: Wed, 22 Apr 2026 01:39:42 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb7fa3c8c45f87e36929f71acaead9bcb07985c205ea0aa6fd83aca31691d78`  
		Last Modified: Wed, 22 Apr 2026 01:39:42 GMT  
		Size: 170.4 KB (170378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f09610f9abffbf6411865ebc07ee20de6c14b2250467c4682f423dddc0ab82`  
		Last Modified: Wed, 22 Apr 2026 01:39:42 GMT  
		Size: 2.4 MB (2394347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a0fb856cc435334489ebeec58afd76f4e676c8bae4b3688daefedfbc7f7c1a8`  
		Last Modified: Wed, 22 Apr 2026 01:39:42 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea36b259fc26e36b99ded4a3aa0ca190c1117ecd424f26565f8474b55964d787`  
		Last Modified: Wed, 22 Apr 2026 01:39:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:c619fe6b2206166796157b814c0d60ca38e29a646b71cd6f5635e2f507cf70d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49e66f35bf963d54f332469bbdef0ca608c651311f5af0e923aca630f4429ae9`

```dockerfile
```

-	Layers:
	-	`sha256:f870fab207e6594315e4d18f50f3ebf834ebc298b6ec128104607668ae939995`  
		Last Modified: Wed, 22 Apr 2026 01:39:42 GMT  
		Size: 2.0 MB (2011927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bf20b8b72f84425e9121a35ea191dab3cf17562679390195740f260304727d7`  
		Last Modified: Wed, 22 Apr 2026 01:39:42 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; riscv64

```console
$ docker pull memcached@sha256:5554043a87027cff145bdb04810a9f8a067c72479937ce0328af056a5c3efe8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30623256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad08d83e675d61f6e230bee3e1d5d5e4b4e8d0b1b3656b71812168b7db5e08e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 08:28:54 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 22 Apr 2026 08:29:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 08:55:11 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 22 Apr 2026 08:55:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 22 Apr 2026 08:55:11 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 22 Apr 2026 08:55:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 22 Apr 2026 08:55:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 08:55:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 08:55:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 08:55:12 GMT
USER memcache
# Wed, 22 Apr 2026 08:55:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 Apr 2026 08:55:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8aa73197c6983c411cf26b41c64a557cfc81f9b4e6d897ff2829a66eac03b37`  
		Last Modified: Wed, 22 Apr 2026 08:55:56 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee379d85ef42145b3f09328c98634e8cd3320230281217ad58867c6982e1d8c`  
		Last Modified: Wed, 22 Apr 2026 08:55:57 GMT  
		Size: 133.1 KB (133094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:310a92cbf1cb95664c58022062af028a81e69f127cd8d9ee044bf7d5087db961`  
		Last Modified: Wed, 22 Apr 2026 08:55:57 GMT  
		Size: 2.2 MB (2208455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336575624802c397f4947f3ddfc2737281bfe2ba8cd714be646b72152c1ec1d0`  
		Last Modified: Wed, 22 Apr 2026 08:55:56 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e926175ab529d298755a0e0507accca74feec6c90ea4495edeaafb07954ad57d`  
		Last Modified: Wed, 22 Apr 2026 08:55:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:9b8b4751f5823830cf382050f0174dd5ade6dc0650b2a3134803b886b2652dba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bc1698424d742c630d5a555fa2c70be3195da5b1a2cd148a331c7aa9fb94b6f`

```dockerfile
```

-	Layers:
	-	`sha256:18aa82332065ff68528148bb97bd5681424d4c57e9e5e331b8908b44023570a9`  
		Last Modified: Wed, 22 Apr 2026 08:55:57 GMT  
		Size: 2.0 MB (2002290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edeefd058e4dbdf6c3026618be5f5184cd3d2c22f14746d890cd45a42004dc8f`  
		Last Modified: Wed, 22 Apr 2026 08:55:57 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; s390x

```console
$ docker pull memcached@sha256:e0fadaa0ad7c323c4f8ead5d8e1ebb9566adc59b25cbc280f40bef816f9d62eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32280559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5d7f2d629511f566dd7c4b3a944adb9989b05bb41dbd3e3881734bc1c1079c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:19:00 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 22 Apr 2026 01:19:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:22:27 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 22 Apr 2026 01:22:27 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 22 Apr 2026 01:22:27 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 22 Apr 2026 01:22:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 22 Apr 2026 01:22:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:22:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:22:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:22:27 GMT
USER memcache
# Wed, 22 Apr 2026 01:22:27 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 Apr 2026 01:22:27 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:71574deb335f1e823f938f4a215de00a90d63866898f1f354a0b15e8b9c30577`  
		Last Modified: Wed, 22 Apr 2026 00:17:08 GMT  
		Size: 29.8 MB (29840300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b460058bd06ca18e629070cadcc158edef16e034340796f661d4fab362ee94`  
		Last Modified: Wed, 22 Apr 2026 01:22:38 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5386c57fa90d49931296cf79f5e8d2ae18d07b9bcffe5eee8354033fee4b673`  
		Last Modified: Wed, 22 Apr 2026 01:22:38 GMT  
		Size: 140.5 KB (140521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd8308c0fc0224d29acef5aadae977dfea2e1ba7c9be0e207ee89c84a4f6417`  
		Last Modified: Wed, 22 Apr 2026 01:22:38 GMT  
		Size: 2.3 MB (2298228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fda405f0b2226447c88ba0d395ee00616ec775cecba66d9a980d4aac7b44fb49`  
		Last Modified: Wed, 22 Apr 2026 01:22:38 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fcaa079ef0e24aab0065df6b15e28d19a0807e2c9cdc639bbc63923135e6daa`  
		Last Modified: Wed, 22 Apr 2026 01:22:39 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:7d2e45f2ecd9448a99f98a077da16fb59c37827c2acbac9e99dea8f79d753165
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54358ef5a62ded9fafc9e908e79d81e5d01102cd4f2082017f54d92232acb7c4`

```dockerfile
```

-	Layers:
	-	`sha256:eb9c1105cc4bf8d4cf2089f7a2a43afe0a113388e7f5a4af9db1f44f9f0fbe11`  
		Last Modified: Wed, 22 Apr 2026 01:22:38 GMT  
		Size: 2.0 MB (2009763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af1c4a20085e6a6f3d2b2fcb2ce9c10456d057c6905b84fe6ad6d99ba351a872`  
		Last Modified: Wed, 22 Apr 2026 01:22:38 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.41`

```console
$ docker pull memcached@sha256:277e0c4f249b118e95ab10e535bae2fa1af772271d9152f3468e58d59348db56
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

### `memcached:1.6.41` - linux; amd64

```console
$ docker pull memcached@sha256:518f136cafc43439a777c20224d30b6fadc3433e3de9573f514dca10dd7e0082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32198630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ec7b3eba028951d3aeee1ef26a365c913edaf06de6c008653f175c0ff0078ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:21:37 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 22 Apr 2026 01:21:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:24:27 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 22 Apr 2026 01:24:27 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 22 Apr 2026 01:24:27 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 22 Apr 2026 01:24:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 22 Apr 2026 01:24:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:24:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:24:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:24:27 GMT
USER memcache
# Wed, 22 Apr 2026 01:24:27 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 Apr 2026 01:24:27 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53e27a8dc2608bcd39496d6e1a0a021aa8933953409444f778d810ec220ab89`  
		Last Modified: Wed, 22 Apr 2026 01:24:33 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d02c07f7ffb4ea4d70b3af1ed59da72e778c143718ba2a7bcb8cd6d12afd95b`  
		Last Modified: Wed, 22 Apr 2026 01:24:33 GMT  
		Size: 136.7 KB (136658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b1a619145ef14a0e4599b98a19dbdc4fc96cfdf359ecf816454cd80ccf2dd2`  
		Last Modified: Wed, 22 Apr 2026 01:24:34 GMT  
		Size: 2.3 MB (2280287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7716efee154a639ac02ada0d1638837bb72c3fc33ecac40f78ffb91daf9dfc5`  
		Last Modified: Wed, 22 Apr 2026 01:24:34 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712f24abcdc2a432d57253a569a16eddd36ff1f8a4ace323467cdb642eae2850`  
		Last Modified: Wed, 22 Apr 2026 01:24:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41` - unknown; unknown

```console
$ docker pull memcached@sha256:f32546667bf4926fd4e7c91aa55a833e8636777f2aa68437cb2bc7a5330e2307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3700c2c8b8182ac20db287282cdafbde42f55966784e109b48a9e5c2ba4d7492`

```dockerfile
```

-	Layers:
	-	`sha256:a3fe3f55746c35c0a798536b5abfc78349217684ca67ba43649a1c86d2a6ebe3`  
		Last Modified: Wed, 22 Apr 2026 01:24:33 GMT  
		Size: 2.0 MB (2008326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0b151a6f180676864b1e8721dddbaf0c105e743520356d58f7df86572a295fa`  
		Last Modified: Wed, 22 Apr 2026 01:24:33 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41` - linux; arm variant v5

```console
$ docker pull memcached@sha256:4b91aeabb9b5d253e27cc0e6f6fa6cc82780c4d686f484c9ed1057a1dd429ba2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30305389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e62e4552c0bfc9dd8f4797df2c1386943df5780d342654ed3050e75668231e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:17:31 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 22 Apr 2026 01:17:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:20:57 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 22 Apr 2026 01:20:57 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 22 Apr 2026 01:20:57 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 22 Apr 2026 01:20:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 22 Apr 2026 01:20:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:20:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:20:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:20:57 GMT
USER memcache
# Wed, 22 Apr 2026 01:20:57 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 Apr 2026 01:20:57 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6496d93bca0663211b9252da346044ecb734ee5b3ecaae5b1fbd230753faee2f`  
		Last Modified: Wed, 22 Apr 2026 00:15:59 GMT  
		Size: 27.9 MB (27948180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64cdc01a23d15e84ef2ee2165c1a90970fb54d98f29377fa63fbd82988cdcc40`  
		Last Modified: Wed, 22 Apr 2026 01:21:03 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:303fc6e2ad4e0da497f7e238e61ec9e1fbde60909262de4a50e05c4db2191602`  
		Last Modified: Wed, 22 Apr 2026 01:21:03 GMT  
		Size: 144.2 KB (144163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c438ec3169ba426bc8374ca37b4f159272d50b60173c35c396f8fbf2208b8806`  
		Last Modified: Wed, 22 Apr 2026 01:21:03 GMT  
		Size: 2.2 MB (2211533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b5512f6aab6e3147798ce406f1035f68f18c2dd046b5fdd6344a17ace7fb31`  
		Last Modified: Wed, 22 Apr 2026 01:21:03 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a320e8acb7760a30eb688cd929fda03bf41ba23a307e06071106c3c0415d03`  
		Last Modified: Wed, 22 Apr 2026 01:21:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41` - unknown; unknown

```console
$ docker pull memcached@sha256:4faa0397c26f0f4a312a28578db40b0f95f89c09769520c7cc09900886412dd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af54d9e6dbb4f86d5a79e417071faea8dd939b7758f640ce360a49c55069e2eb`

```dockerfile
```

-	Layers:
	-	`sha256:1850a912cc062cca1f70a2b76861d54c0ad06921d2a4960a7c483b5f8820eaa1`  
		Last Modified: Wed, 22 Apr 2026 01:21:03 GMT  
		Size: 2.0 MB (2011329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02fdad23f354f6597bfec3258d6bbee5142bcce9e1faaa7de87f9859bf8c6d14`  
		Last Modified: Wed, 22 Apr 2026 01:21:03 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41` - linux; arm variant v7

```console
$ docker pull memcached@sha256:4d262b60fea5a97e91a6c1827ab7209a344c47616388ada79b27e4e69eea9d38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28516774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02f2f7426f06caeeb218b724a947fa35544b0749bacf781227878e40cb98d08f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:18:06 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 22 Apr 2026 01:18:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:21:19 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 22 Apr 2026 01:21:19 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 22 Apr 2026 01:21:19 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 22 Apr 2026 01:21:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 22 Apr 2026 01:21:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:21:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:21:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:21:19 GMT
USER memcache
# Wed, 22 Apr 2026 01:21:19 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 Apr 2026 01:21:19 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9e541e5bfbbe69b7bbe01cd2f1abf8560e2e43bf76eb96b2e88a3df29020834b`  
		Last Modified: Wed, 22 Apr 2026 00:17:02 GMT  
		Size: 26.2 MB (26214838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0867e20c7ab47539b3f27abc4c7f4bf41d367127d9ffbd30a531ab387a69e2e`  
		Last Modified: Wed, 22 Apr 2026 01:21:25 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34eedf23d5ae4af59fe6ecfd854e48545ede507ce44d930cea5c11b652b31f4`  
		Last Modified: Wed, 22 Apr 2026 01:21:25 GMT  
		Size: 135.4 KB (135382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fff54fd1447de9c8b377640a2720588785769320b1a65d59a1da8e9690e6f9`  
		Last Modified: Wed, 22 Apr 2026 01:21:25 GMT  
		Size: 2.2 MB (2165043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac214a1bada6a999cda6b6b021b8ef5ba954108062e3ee4df0161a500fc566f`  
		Last Modified: Wed, 22 Apr 2026 01:21:25 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0431aacefa9d6f210c7c4778e75df5a21c196127779acc2da1bd7b32088f47dc`  
		Last Modified: Wed, 22 Apr 2026 01:21:26 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41` - unknown; unknown

```console
$ docker pull memcached@sha256:e4f840cb65bd892b2aafc305cb008de10d4d41475876ef9c9bbf51831f9cd7e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:987452d71cfba90bac820fca09f2954a061813125a8832038df5c062224577c5`

```dockerfile
```

-	Layers:
	-	`sha256:f5793a9489c1e1010726124554d7404a19b2675ce8596a38169b160edc81d045`  
		Last Modified: Wed, 22 Apr 2026 01:21:25 GMT  
		Size: 2.0 MB (2009786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef3c23077c5adc1a06a0e1f66d0ec1e57032a5b35685c53064098e236a62c5a1`  
		Last Modified: Wed, 22 Apr 2026 01:21:25 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:52e2a52a542b0fff64533e7271ce3af9825a80a1126998cf6070b0ec4c0030b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32560736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c3fcfefa704f0162e85ab03d515502e07a6ff91ec994dc4b6c956cc2ce80990`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:22:08 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 22 Apr 2026 01:22:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:25:10 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 22 Apr 2026 01:25:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 22 Apr 2026 01:25:10 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 22 Apr 2026 01:25:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 22 Apr 2026 01:25:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:25:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:25:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:25:10 GMT
USER memcache
# Wed, 22 Apr 2026 01:25:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 Apr 2026 01:25:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebea5231ebe63bff9044a4ee7713dac1b62fc15d85ee920f04eae4010a67b668`  
		Last Modified: Wed, 22 Apr 2026 01:25:16 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5921030f644563277c2af1be27b21dfded0e01763210710efac613f07dc74c`  
		Last Modified: Wed, 22 Apr 2026 01:25:16 GMT  
		Size: 153.5 KB (153515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1ef7f1deafd8e81fec98af35ef4fe12c2436c1eddb6bb87377b83f524f7d6f`  
		Last Modified: Wed, 22 Apr 2026 01:25:16 GMT  
		Size: 2.3 MB (2262106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd4f58ffc6f10cea1171fbb552aff0b93a04aba0ca6815cd9ad66ab3a49f8419`  
		Last Modified: Wed, 22 Apr 2026 01:25:16 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace7ea462603345a875235135df0b8dd036890eacdb25150c1a8089604e3ca1f`  
		Last Modified: Wed, 22 Apr 2026 01:25:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41` - unknown; unknown

```console
$ docker pull memcached@sha256:63aba0d160ad2159dd41a074d79446fc4ba2e745c7e5a10a41dbd1d5c2abc86d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b67f2365f86c60d496eb140fde16a0d6fbf89ae6a83d200c6a3971e32eca706b`

```dockerfile
```

-	Layers:
	-	`sha256:e87d247df404b9fe7e19667c95311e8109ea54acdcca2f52ceba73b7099d144e`  
		Last Modified: Wed, 22 Apr 2026 01:25:16 GMT  
		Size: 2.0 MB (2008642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5290960be9e7480bf28bf59599ba02b7792ea80b3309570c3b3a24465ad7d58`  
		Last Modified: Wed, 22 Apr 2026 01:25:16 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41` - linux; 386

```console
$ docker pull memcached@sha256:0b8f07a6f169bfe4cc362cbabca8c92d5140665660c615383f2755c40c0036f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33670125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd6a79877127262a308ef5f3bd216749c6f0b1fc43971b56c533d4e47f5c6de2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:17:33 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 22 Apr 2026 01:17:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:20:28 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 22 Apr 2026 01:20:28 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 22 Apr 2026 01:20:28 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 22 Apr 2026 01:20:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 22 Apr 2026 01:20:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:20:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:20:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:20:28 GMT
USER memcache
# Wed, 22 Apr 2026 01:20:28 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 Apr 2026 01:20:28 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:dacd7cda306bf5bd7a2030f9b0c2e9d71fda44ea58493a33450d210b74a8ec75`  
		Last Modified: Wed, 22 Apr 2026 00:17:04 GMT  
		Size: 31.3 MB (31296327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a0c9fe363e7e198726a5e39cf627131e43cd59d319a350f978180f6f449b8a`  
		Last Modified: Wed, 22 Apr 2026 01:20:34 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dff2976b24139841065357d1f81c8cf6d9b45ee35e2947f1345e86493b2f5e67`  
		Last Modified: Wed, 22 Apr 2026 01:20:34 GMT  
		Size: 147.5 KB (147529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8b8718f120acc0033835790e0bd541e38b843c6b260688b8fde3c94eadd5911`  
		Last Modified: Wed, 22 Apr 2026 01:20:34 GMT  
		Size: 2.2 MB (2224758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f70ea447cee314191f67e0ce5ccc23703730c89810e26bfa3f96f81964849dc`  
		Last Modified: Wed, 22 Apr 2026 01:20:34 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:789bc1b0beaaf9809e3cab832a0b6b29f50aec3b18f7a7cdf04e343d3ee800a3`  
		Last Modified: Wed, 22 Apr 2026 01:20:35 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41` - unknown; unknown

```console
$ docker pull memcached@sha256:45cfea0c565e5e6c79f4a36cf4ec611ccc7e910c481110b37be04eca3276511b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d33423fad9c4c2f3b1af3eb87b8af48d7cfc9e00d70e6c33937d7d215fb94c5`

```dockerfile
```

-	Layers:
	-	`sha256:2656e01c20323e582a0ba03c06d82008eb35ae9850f7d6c7f73c0e5ae040805b`  
		Last Modified: Wed, 22 Apr 2026 01:20:34 GMT  
		Size: 2.0 MB (2005483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d267990174d3038591d6a8ffe07af06d961bb5c68b86a9cdac459f5a0996ddbe`  
		Last Modified: Wed, 22 Apr 2026 01:20:34 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41` - linux; ppc64le

```console
$ docker pull memcached@sha256:3df945008f026e1a7782fc67d0107a07c9103d9d50dd7ae605082ea97fb64ff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36164269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7eb2db1cbb0c7ddc2688ee498498fb5122ee78ab349b636a43585b1beb30da9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:35:49 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 22 Apr 2026 01:35:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:39:22 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 22 Apr 2026 01:39:22 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 22 Apr 2026 01:39:22 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 22 Apr 2026 01:39:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 22 Apr 2026 01:39:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:39:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:39:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:39:23 GMT
USER memcache
# Wed, 22 Apr 2026 01:39:23 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 Apr 2026 01:39:23 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b5fd051d0fcd0789e7358cba300f83befdba943416041497be86050e282a6d02`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 33.6 MB (33598032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e271c91c5c30b04dee49fb4c9ab2f9863d13146641f1b8681b59467d0f8ab5`  
		Last Modified: Wed, 22 Apr 2026 01:39:42 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb7fa3c8c45f87e36929f71acaead9bcb07985c205ea0aa6fd83aca31691d78`  
		Last Modified: Wed, 22 Apr 2026 01:39:42 GMT  
		Size: 170.4 KB (170378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f09610f9abffbf6411865ebc07ee20de6c14b2250467c4682f423dddc0ab82`  
		Last Modified: Wed, 22 Apr 2026 01:39:42 GMT  
		Size: 2.4 MB (2394347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a0fb856cc435334489ebeec58afd76f4e676c8bae4b3688daefedfbc7f7c1a8`  
		Last Modified: Wed, 22 Apr 2026 01:39:42 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea36b259fc26e36b99ded4a3aa0ca190c1117ecd424f26565f8474b55964d787`  
		Last Modified: Wed, 22 Apr 2026 01:39:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41` - unknown; unknown

```console
$ docker pull memcached@sha256:c619fe6b2206166796157b814c0d60ca38e29a646b71cd6f5635e2f507cf70d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49e66f35bf963d54f332469bbdef0ca608c651311f5af0e923aca630f4429ae9`

```dockerfile
```

-	Layers:
	-	`sha256:f870fab207e6594315e4d18f50f3ebf834ebc298b6ec128104607668ae939995`  
		Last Modified: Wed, 22 Apr 2026 01:39:42 GMT  
		Size: 2.0 MB (2011927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bf20b8b72f84425e9121a35ea191dab3cf17562679390195740f260304727d7`  
		Last Modified: Wed, 22 Apr 2026 01:39:42 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41` - linux; riscv64

```console
$ docker pull memcached@sha256:5554043a87027cff145bdb04810a9f8a067c72479937ce0328af056a5c3efe8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30623256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad08d83e675d61f6e230bee3e1d5d5e4b4e8d0b1b3656b71812168b7db5e08e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 08:28:54 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 22 Apr 2026 08:29:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 08:55:11 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 22 Apr 2026 08:55:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 22 Apr 2026 08:55:11 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 22 Apr 2026 08:55:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 22 Apr 2026 08:55:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 08:55:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 08:55:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 08:55:12 GMT
USER memcache
# Wed, 22 Apr 2026 08:55:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 Apr 2026 08:55:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8aa73197c6983c411cf26b41c64a557cfc81f9b4e6d897ff2829a66eac03b37`  
		Last Modified: Wed, 22 Apr 2026 08:55:56 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee379d85ef42145b3f09328c98634e8cd3320230281217ad58867c6982e1d8c`  
		Last Modified: Wed, 22 Apr 2026 08:55:57 GMT  
		Size: 133.1 KB (133094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:310a92cbf1cb95664c58022062af028a81e69f127cd8d9ee044bf7d5087db961`  
		Last Modified: Wed, 22 Apr 2026 08:55:57 GMT  
		Size: 2.2 MB (2208455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336575624802c397f4947f3ddfc2737281bfe2ba8cd714be646b72152c1ec1d0`  
		Last Modified: Wed, 22 Apr 2026 08:55:56 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e926175ab529d298755a0e0507accca74feec6c90ea4495edeaafb07954ad57d`  
		Last Modified: Wed, 22 Apr 2026 08:55:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41` - unknown; unknown

```console
$ docker pull memcached@sha256:9b8b4751f5823830cf382050f0174dd5ade6dc0650b2a3134803b886b2652dba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bc1698424d742c630d5a555fa2c70be3195da5b1a2cd148a331c7aa9fb94b6f`

```dockerfile
```

-	Layers:
	-	`sha256:18aa82332065ff68528148bb97bd5681424d4c57e9e5e331b8908b44023570a9`  
		Last Modified: Wed, 22 Apr 2026 08:55:57 GMT  
		Size: 2.0 MB (2002290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edeefd058e4dbdf6c3026618be5f5184cd3d2c22f14746d890cd45a42004dc8f`  
		Last Modified: Wed, 22 Apr 2026 08:55:57 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41` - linux; s390x

```console
$ docker pull memcached@sha256:e0fadaa0ad7c323c4f8ead5d8e1ebb9566adc59b25cbc280f40bef816f9d62eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32280559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5d7f2d629511f566dd7c4b3a944adb9989b05bb41dbd3e3881734bc1c1079c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:19:00 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 22 Apr 2026 01:19:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:22:27 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 22 Apr 2026 01:22:27 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 22 Apr 2026 01:22:27 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 22 Apr 2026 01:22:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 22 Apr 2026 01:22:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:22:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:22:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:22:27 GMT
USER memcache
# Wed, 22 Apr 2026 01:22:27 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 Apr 2026 01:22:27 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:71574deb335f1e823f938f4a215de00a90d63866898f1f354a0b15e8b9c30577`  
		Last Modified: Wed, 22 Apr 2026 00:17:08 GMT  
		Size: 29.8 MB (29840300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b460058bd06ca18e629070cadcc158edef16e034340796f661d4fab362ee94`  
		Last Modified: Wed, 22 Apr 2026 01:22:38 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5386c57fa90d49931296cf79f5e8d2ae18d07b9bcffe5eee8354033fee4b673`  
		Last Modified: Wed, 22 Apr 2026 01:22:38 GMT  
		Size: 140.5 KB (140521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd8308c0fc0224d29acef5aadae977dfea2e1ba7c9be0e207ee89c84a4f6417`  
		Last Modified: Wed, 22 Apr 2026 01:22:38 GMT  
		Size: 2.3 MB (2298228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fda405f0b2226447c88ba0d395ee00616ec775cecba66d9a980d4aac7b44fb49`  
		Last Modified: Wed, 22 Apr 2026 01:22:38 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fcaa079ef0e24aab0065df6b15e28d19a0807e2c9cdc639bbc63923135e6daa`  
		Last Modified: Wed, 22 Apr 2026 01:22:39 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41` - unknown; unknown

```console
$ docker pull memcached@sha256:7d2e45f2ecd9448a99f98a077da16fb59c37827c2acbac9e99dea8f79d753165
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54358ef5a62ded9fafc9e908e79d81e5d01102cd4f2082017f54d92232acb7c4`

```dockerfile
```

-	Layers:
	-	`sha256:eb9c1105cc4bf8d4cf2089f7a2a43afe0a113388e7f5a4af9db1f44f9f0fbe11`  
		Last Modified: Wed, 22 Apr 2026 01:22:38 GMT  
		Size: 2.0 MB (2009763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af1c4a20085e6a6f3d2b2fcb2ce9c10456d057c6905b84fe6ad6d99ba351a872`  
		Last Modified: Wed, 22 Apr 2026 01:22:38 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.41-alpine`

```console
$ docker pull memcached@sha256:65c80b311a9601ef5ca8af3814e5cd06a9c4277ea139d80bd53da6b4d39eb46e
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

### `memcached:1.6.41-alpine` - linux; amd64

```console
$ docker pull memcached@sha256:7b962825022657b112923d502400d5734870d5eb12c19e7f1f6585f7534a6795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5959872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b58f7e71f30daaa3f466fa31d855fddb7101e42c0c42fac520be5d1d43ec32e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:46 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:17:47 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:20:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:20:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:20:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:20:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:20:22 GMT
USER memcache
# Wed, 15 Apr 2026 20:20:22 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:20:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73d5ffe265b83073ce3c7211fb3c15ebbd5e7146d870d9ce69d2e7dfc493348`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6cb4fdd95ced0d5a9528e97ff0f20742749cbd9ef6dc1322d13e682a7085a67`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 106.1 KB (106063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe17fc291d9444fbae93d7f45eab008318f87302c016c06e6e911c1a571a053`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 2.0 MB (1988274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1948bd131d2cbd05c6bf2962d18b15d105abee6f42f398bab3c13737537f197`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bde8ceae30a2a0890715bbc591167ee301c57d7f75023e80be460035187def`  
		Last Modified: Wed, 15 Apr 2026 20:20:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:58ed333482f8a8530c82ad7399d5917a7db85fbcdf70fc1dec55fbedcdf09253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4255278359004afd8c94db1a7fe6129fc984d0716c33665c9eca3168476fdcb`

```dockerfile
```

-	Layers:
	-	`sha256:5f47d88d89d22d065a3590d477ae130520b882176ab07e95862afb4d8b69b214`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 94.9 KB (94901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab2d532e4a6ce2f362d25c79dfaeb88d333fe6efe7c1b5b293630bf6ca292eb8`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 20.5 KB (20530 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:47a06cd0daead339b96ed90e425336a8a49a75e4e358b5ec1ea63a630720f704
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3947facc9e9fae3eee283f24b611a8ae87e353b6d6447bc6f582e90f2fce3743`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:58 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:17:59 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:21:02 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:21:02 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:21:02 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:21:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:21:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:21:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:21:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:21:03 GMT
USER memcache
# Wed, 15 Apr 2026 20:21:03 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:21:03 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77001163fdaab47f07a85fc5bb15f3512a8cb9b9b049cec7e0c88bcbbdb5bb5d`  
		Last Modified: Wed, 15 Apr 2026 20:21:07 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee1b43c0cfbf2ee56e39441933ff06803264d22918fe867d8b5ba7d5adfb9c3`  
		Last Modified: Wed, 15 Apr 2026 20:21:06 GMT  
		Size: 102.6 KB (102630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c041bfac12e599ad87749289dec9672dac36e8c0e16779f13fa695d10f2f0cc5`  
		Last Modified: Wed, 15 Apr 2026 20:21:07 GMT  
		Size: 1.9 MB (1937835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2dfd492dd0f295311a0c314fae06f4b325ae22cb0e673a53e0705f3d4e0504`  
		Last Modified: Wed, 15 Apr 2026 20:21:07 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671c66eac839c2f0a5b2e64d1f581069c4cdf119e784bff16540ecc94e2c2b10`  
		Last Modified: Wed, 15 Apr 2026 20:21:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:2a6148a6aebb042e55781b40ed626d0c5871833be4ae8dc303af7aace07d9d60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbaadfaacfaf0e7c226b35236bb84c2268d4c6eb017efd435a3999a44edfcc77`

```dockerfile
```

-	Layers:
	-	`sha256:c68bb3ee35fc0ac716bca45cc759f3b1ff52b1d5a0acae9876eaf0aa55aa667d`  
		Last Modified: Wed, 15 Apr 2026 20:21:06 GMT  
		Size: 20.5 KB (20466 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:fb58bae12ffa00c9cbafc8bee2341b43ffdccacbde7085fa707ef6c7f2d69e37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5273034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddd4e85c30e4df5803b553b8a7f84084c3dae6f72531ac70fcabf7099cfa8148`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 21:14:38 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 21:14:39 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 21:17:34 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 21:17:34 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 21:17:34 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 21:17:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 21:17:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:17:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 21:17:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:17:34 GMT
USER memcache
# Wed, 15 Apr 2026 21:17:34 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 21:17:34 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e312136cfedda9620407d42650d0595220e60d3c40ae8853bfbdd83f392b9e6`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53697a39f37b691917c91310ac4e107308674bddcc9017e3bbc0d0134eaf4c3e`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 92.4 KB (92369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5e4be9e0df543f152c376fe2cc74b89b75585793fdbd7d12476737d386d8e1`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 1.9 MB (1896191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a083f41edf5f859feb4367eeeea0955dc9799c8202fb8a67c40915ed5b195002`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c43503b1f4f42ffc5e0e4415befe45199dec730bc26347df151298345ba640`  
		Last Modified: Wed, 15 Apr 2026 21:17:40 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7535cf6b6a140771131c2c524301d4616f34856fcd8ecbe3e52300108c49de2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d73c906894a0a3d178edd69991f310225c0daef314e6faa83a0b9adecfbeb34`

```dockerfile
```

-	Layers:
	-	`sha256:8f1fddd7d14560fb90f381b09cde9302dfc9253e6702adf28c55961d755b1ad8`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 94.3 KB (94319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fcf119d246607aa25330c4c05fe14a64cebda69b02d14507862a9f07c1404e6`  
		Last Modified: Wed, 15 Apr 2026 21:17:38 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:6d70439467a65065c52894232a3085c724da2810a9b3205130d5e434ab411e3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6288798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4be3e105216d2507b68e772f7d08d52a5076dd55fad35c29775038d05c24112`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:15:23 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:15:24 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:18:13 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:18:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:18:13 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:18:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:18:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:18:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:18:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:18:13 GMT
USER memcache
# Wed, 15 Apr 2026 20:18:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:18:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81758f5fc2e8fa13e3625f253d7c999560ac666121c026f7251dbfb919cca611`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d735737d3a0cf1eda63bd72c09f64eb679313e9c5f8a105849848bdd779e1d`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 121.8 KB (121846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ac0921d2cc2b3388e0f006a6672c5a9e1098a59e570121dde092104d845c51`  
		Last Modified: Wed, 15 Apr 2026 20:18:19 GMT  
		Size: 2.0 MB (1965733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca9cf731b18a76c3ac25cc3add219660d57516c12680d7b1f1ece282406eb82`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:717a6b23dd1cd76b686bf26066af23265e0d002ed6a3e87f6aa4f79264b7da11`  
		Last Modified: Wed, 15 Apr 2026 20:18:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7e5232b868d3222e3ce2b0ee39c62f6cb294bea27456b00940fbc4e3c8c3f84d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:780bf975a24d5fdc511c857720c04cb077d64abcfe4c93ea0db7c9487c323718`

```dockerfile
```

-	Layers:
	-	`sha256:addb0f46e3b5adb674175c11fc85526d4628e24d74d210c8b00c9a945b44407c`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 94.4 KB (94355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3364e418b74b6f6ca17deec7d55783a6e1554de3783ab0a6d5e56496d935ddb0`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 20.7 KB (20728 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-alpine` - linux; 386

```console
$ docker pull memcached@sha256:80328bf779fa1494f7677b441ad1c16c2134f126e6556953deb3cfab1c4c9770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5744816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d957405dd0811f1cd15fe39563938a60c2008204d2f63ebc7e39f8989c796f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 22:20:45 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 22:20:46 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 22:23:32 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 22:23:32 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 22:23:32 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 22:23:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 22:23:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 22:23:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 22:23:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 22:23:32 GMT
USER memcache
# Wed, 15 Apr 2026 22:23:32 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 22:23:32 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0617a09eee85c2032f5596ded56b733366513074f9096177315b50dc45485e20`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c67275dbc381ac3ae0b21dda20edaf245e2ca54d6f5dc3af8805db03c17cc93`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 110.7 KB (110715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6ecb23f1f4bc89d5c315aac493f29fe7bb33061c70d926c904f4f55d374461`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 1.9 MB (1942309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e782df8f482a58603ea70ef9e04e838d044a6070c7e4cd116c90a09b917ed940`  
		Last Modified: Wed, 15 Apr 2026 22:23:38 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616df56d574e39c00ae772c6a29e2b724698048a83cc29ea17049573f9073b10`  
		Last Modified: Wed, 15 Apr 2026 22:23:38 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:c726e7abf461d963e544818339e4cd12fd2f31e41436475f0e51818a0885fbdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12e41b9d6f745d686c2649255bd14fe4e0b97a3477d383e719490e5ef66b27ae`

```dockerfile
```

-	Layers:
	-	`sha256:b44003cd1ea209090a063c5abfb4ee881849abba47e8711191b7637f86d8ee8b`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 94.9 KB (94856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f431de53d9b6c7e2cbc847af9daec064d061f8bd625615734012051336c495a`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 20.5 KB (20472 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:8182e35a9a404f0b522cb3c176d3dc4aade974e5556184c0a5a19e800721868a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6034321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30c6f532e81b50ea71c3520a80da0c8154b4cb14ebc17f87eb3a026862b47ed8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:41 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:17:43 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:20:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:20:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:20:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:20:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:20:22 GMT
USER memcache
# Wed, 15 Apr 2026 20:20:22 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:20:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee88d1c88fa46aa906a297c2919c9a085e74d04f20e4f827ca240a20f10ad34`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c574329cc1ebf156e2d89ab608bd58a3c0db550845c0ec394d265aa98fc5c4`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 126.3 KB (126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc2a28510bcba91734e7b38682847296011b63458db8a87a4bcecd180b8de7b5`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 2.1 MB (2075767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c524eb15ef0a41bf969efc93ef579db92dc59e8df57c9abfd099e7f6ff0756`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bde8ceae30a2a0890715bbc591167ee301c57d7f75023e80be460035187def`  
		Last Modified: Wed, 15 Apr 2026 20:20:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:4051408ef6c5bf4d4f37abf19c13f0298d8baa81770fcbfb588221e49e3bb834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ec3a4d49e6f325e484db43c9c9981f4eaa0223d9ae98282d95c3ee20c2089cb`

```dockerfile
```

-	Layers:
	-	`sha256:0e4e65db585f857844a67a831eb876dbb0a8a40d9269393d6c0fa83a2df995ae`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 94.3 KB (94308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50f58ec8aff3c96cc7b58e689122c27ee26121c598034cdc59ec95fd6423effe`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:f3209d1ca2c4ce827614d16445231d96372944d218f18fd22850eec83874e5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5772332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e30170e0826b89d0ca59ffcae54b850ded07e6ae9451ecf1fd60f3ca8adcc725`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2026 00:00:48 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 16 Apr 2026 00:00:52 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 16 Apr 2026 00:14:21 GMT
ENV MEMCACHED_VERSION=1.6.41
# Thu, 16 Apr 2026 00:14:21 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Thu, 16 Apr 2026 00:14:21 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Thu, 16 Apr 2026 00:14:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 16 Apr 2026 00:14:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Apr 2026 00:14:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 16 Apr 2026 00:14:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Apr 2026 00:14:22 GMT
USER memcache
# Thu, 16 Apr 2026 00:14:22 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 16 Apr 2026 00:14:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62b143e34f5b89277e3a88ed4d722339d188a094d4bb534e222ca80e7741031`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bfff7c64f831ba03c491874cdf9a1c3f42bff72bb0e1951c63d8cf718854cff`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 108.9 KB (108903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69aef1050272a61cfbfd97c041d3776f96bdd03b102f2c3c54bbb0af2e1235a5`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 2.1 MB (2074414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ce340fb37f86db0d3aa774c23880b7c8322d2af8e3adc27a6ffa25d67c2122`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e40c6fb92d819994d38fae7accdffd583465eb6e645834b66f3ce9f0562f69`  
		Last Modified: Thu, 16 Apr 2026 00:14:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:2caae198d1efb7d4df14da45a3ff360a697982b544a61a3f907076b414983ea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1503bd38f4b30bc91be18dd93359e7376a9da1c7cb652ade64efd154064543fe`

```dockerfile
```

-	Layers:
	-	`sha256:e2d79fb634d76e28f055ab09953f59c371b93599e2b79f20f3d758f2c9520118`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 94.3 KB (94304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3614ad9b1715c3d6aa488496fca74d7143ea095d227f599407c933c62ec266aa`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 20.6 KB (20604 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:1da27660ae89a83aaf603e1affd51be573e5b8dac6c07ed592aee2a3a2b20581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5859702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13aa64df69a308e46b054bbd8e7a5d2f1e079005771f61748dae0d049889ba7f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:14:40 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:14:41 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:17:58 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:17:58 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:17:58 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:17:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:17:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:17:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:17:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:17:58 GMT
USER memcache
# Wed, 15 Apr 2026 20:17:58 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:17:58 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c42733e5f451590186b9b76c4b374ae5a84b657f7f1fd405647f5ba82c65bcd`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a14431ac88e8fe205b07f09b7e4843bb254de41cbc044725d6eaee3c2f822f`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 114.3 KB (114293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6377b7d98f32173cd47682aa73b32e4eba42781fa9224b9eb7a6f87367d37f94`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 2.0 MB (2017525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d022ae992296922747a4b69694b0185a0ce1f6cdece7f794e39e74dab92d250`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255cb3a435cbd623c1235d0429160faf72c244a6c1a613525df36f58a8c1f784`  
		Last Modified: Wed, 15 Apr 2026 20:18:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:531ee140f06db77d73b71bce7339abec3c6d976092bb80542bb337bb406acdbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b17d6f7e71efe3ee05ebcdb8ae90c28cf60db9ef069b0a98fe442c949740a6c`

```dockerfile
```

-	Layers:
	-	`sha256:820a080f49bf9e33948dbe5c13f6254f135d90bcb2b2277e3d2fd2430626c1a2`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 94.2 KB (94250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8ab82f4f240f46f9e34b74691925ab4af7f1cbb12ad3cb8639e0f317cf06653`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.41-alpine3.23`

```console
$ docker pull memcached@sha256:65c80b311a9601ef5ca8af3814e5cd06a9c4277ea139d80bd53da6b4d39eb46e
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

### `memcached:1.6.41-alpine3.23` - linux; amd64

```console
$ docker pull memcached@sha256:7b962825022657b112923d502400d5734870d5eb12c19e7f1f6585f7534a6795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5959872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b58f7e71f30daaa3f466fa31d855fddb7101e42c0c42fac520be5d1d43ec32e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:46 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:17:47 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:20:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:20:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:20:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:20:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:20:22 GMT
USER memcache
# Wed, 15 Apr 2026 20:20:22 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:20:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73d5ffe265b83073ce3c7211fb3c15ebbd5e7146d870d9ce69d2e7dfc493348`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6cb4fdd95ced0d5a9528e97ff0f20742749cbd9ef6dc1322d13e682a7085a67`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 106.1 KB (106063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe17fc291d9444fbae93d7f45eab008318f87302c016c06e6e911c1a571a053`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 2.0 MB (1988274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1948bd131d2cbd05c6bf2962d18b15d105abee6f42f398bab3c13737537f197`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bde8ceae30a2a0890715bbc591167ee301c57d7f75023e80be460035187def`  
		Last Modified: Wed, 15 Apr 2026 20:20:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:58ed333482f8a8530c82ad7399d5917a7db85fbcdf70fc1dec55fbedcdf09253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4255278359004afd8c94db1a7fe6129fc984d0716c33665c9eca3168476fdcb`

```dockerfile
```

-	Layers:
	-	`sha256:5f47d88d89d22d065a3590d477ae130520b882176ab07e95862afb4d8b69b214`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 94.9 KB (94901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab2d532e4a6ce2f362d25c79dfaeb88d333fe6efe7c1b5b293630bf6ca292eb8`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 20.5 KB (20530 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-alpine3.23` - linux; arm variant v6

```console
$ docker pull memcached@sha256:47a06cd0daead339b96ed90e425336a8a49a75e4e358b5ec1ea63a630720f704
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3947facc9e9fae3eee283f24b611a8ae87e353b6d6447bc6f582e90f2fce3743`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:58 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:17:59 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:21:02 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:21:02 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:21:02 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:21:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:21:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:21:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:21:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:21:03 GMT
USER memcache
# Wed, 15 Apr 2026 20:21:03 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:21:03 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77001163fdaab47f07a85fc5bb15f3512a8cb9b9b049cec7e0c88bcbbdb5bb5d`  
		Last Modified: Wed, 15 Apr 2026 20:21:07 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee1b43c0cfbf2ee56e39441933ff06803264d22918fe867d8b5ba7d5adfb9c3`  
		Last Modified: Wed, 15 Apr 2026 20:21:06 GMT  
		Size: 102.6 KB (102630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c041bfac12e599ad87749289dec9672dac36e8c0e16779f13fa695d10f2f0cc5`  
		Last Modified: Wed, 15 Apr 2026 20:21:07 GMT  
		Size: 1.9 MB (1937835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2dfd492dd0f295311a0c314fae06f4b325ae22cb0e673a53e0705f3d4e0504`  
		Last Modified: Wed, 15 Apr 2026 20:21:07 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671c66eac839c2f0a5b2e64d1f581069c4cdf119e784bff16540ecc94e2c2b10`  
		Last Modified: Wed, 15 Apr 2026 20:21:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:2a6148a6aebb042e55781b40ed626d0c5871833be4ae8dc303af7aace07d9d60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbaadfaacfaf0e7c226b35236bb84c2268d4c6eb017efd435a3999a44edfcc77`

```dockerfile
```

-	Layers:
	-	`sha256:c68bb3ee35fc0ac716bca45cc759f3b1ff52b1d5a0acae9876eaf0aa55aa667d`  
		Last Modified: Wed, 15 Apr 2026 20:21:06 GMT  
		Size: 20.5 KB (20466 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-alpine3.23` - linux; arm variant v7

```console
$ docker pull memcached@sha256:fb58bae12ffa00c9cbafc8bee2341b43ffdccacbde7085fa707ef6c7f2d69e37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5273034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddd4e85c30e4df5803b553b8a7f84084c3dae6f72531ac70fcabf7099cfa8148`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 21:14:38 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 21:14:39 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 21:17:34 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 21:17:34 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 21:17:34 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 21:17:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 21:17:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:17:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 21:17:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:17:34 GMT
USER memcache
# Wed, 15 Apr 2026 21:17:34 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 21:17:34 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e312136cfedda9620407d42650d0595220e60d3c40ae8853bfbdd83f392b9e6`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53697a39f37b691917c91310ac4e107308674bddcc9017e3bbc0d0134eaf4c3e`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 92.4 KB (92369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5e4be9e0df543f152c376fe2cc74b89b75585793fdbd7d12476737d386d8e1`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 1.9 MB (1896191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a083f41edf5f859feb4367eeeea0955dc9799c8202fb8a67c40915ed5b195002`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c43503b1f4f42ffc5e0e4415befe45199dec730bc26347df151298345ba640`  
		Last Modified: Wed, 15 Apr 2026 21:17:40 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:7535cf6b6a140771131c2c524301d4616f34856fcd8ecbe3e52300108c49de2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d73c906894a0a3d178edd69991f310225c0daef314e6faa83a0b9adecfbeb34`

```dockerfile
```

-	Layers:
	-	`sha256:8f1fddd7d14560fb90f381b09cde9302dfc9253e6702adf28c55961d755b1ad8`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 94.3 KB (94319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fcf119d246607aa25330c4c05fe14a64cebda69b02d14507862a9f07c1404e6`  
		Last Modified: Wed, 15 Apr 2026 21:17:38 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:6d70439467a65065c52894232a3085c724da2810a9b3205130d5e434ab411e3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6288798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4be3e105216d2507b68e772f7d08d52a5076dd55fad35c29775038d05c24112`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:15:23 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:15:24 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:18:13 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:18:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:18:13 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:18:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:18:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:18:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:18:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:18:13 GMT
USER memcache
# Wed, 15 Apr 2026 20:18:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:18:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81758f5fc2e8fa13e3625f253d7c999560ac666121c026f7251dbfb919cca611`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d735737d3a0cf1eda63bd72c09f64eb679313e9c5f8a105849848bdd779e1d`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 121.8 KB (121846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ac0921d2cc2b3388e0f006a6672c5a9e1098a59e570121dde092104d845c51`  
		Last Modified: Wed, 15 Apr 2026 20:18:19 GMT  
		Size: 2.0 MB (1965733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca9cf731b18a76c3ac25cc3add219660d57516c12680d7b1f1ece282406eb82`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:717a6b23dd1cd76b686bf26066af23265e0d002ed6a3e87f6aa4f79264b7da11`  
		Last Modified: Wed, 15 Apr 2026 20:18:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:7e5232b868d3222e3ce2b0ee39c62f6cb294bea27456b00940fbc4e3c8c3f84d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:780bf975a24d5fdc511c857720c04cb077d64abcfe4c93ea0db7c9487c323718`

```dockerfile
```

-	Layers:
	-	`sha256:addb0f46e3b5adb674175c11fc85526d4628e24d74d210c8b00c9a945b44407c`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 94.4 KB (94355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3364e418b74b6f6ca17deec7d55783a6e1554de3783ab0a6d5e56496d935ddb0`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 20.7 KB (20728 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-alpine3.23` - linux; 386

```console
$ docker pull memcached@sha256:80328bf779fa1494f7677b441ad1c16c2134f126e6556953deb3cfab1c4c9770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5744816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d957405dd0811f1cd15fe39563938a60c2008204d2f63ebc7e39f8989c796f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 22:20:45 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 22:20:46 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 22:23:32 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 22:23:32 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 22:23:32 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 22:23:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 22:23:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 22:23:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 22:23:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 22:23:32 GMT
USER memcache
# Wed, 15 Apr 2026 22:23:32 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 22:23:32 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0617a09eee85c2032f5596ded56b733366513074f9096177315b50dc45485e20`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c67275dbc381ac3ae0b21dda20edaf245e2ca54d6f5dc3af8805db03c17cc93`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 110.7 KB (110715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6ecb23f1f4bc89d5c315aac493f29fe7bb33061c70d926c904f4f55d374461`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 1.9 MB (1942309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e782df8f482a58603ea70ef9e04e838d044a6070c7e4cd116c90a09b917ed940`  
		Last Modified: Wed, 15 Apr 2026 22:23:38 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616df56d574e39c00ae772c6a29e2b724698048a83cc29ea17049573f9073b10`  
		Last Modified: Wed, 15 Apr 2026 22:23:38 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:c726e7abf461d963e544818339e4cd12fd2f31e41436475f0e51818a0885fbdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12e41b9d6f745d686c2649255bd14fe4e0b97a3477d383e719490e5ef66b27ae`

```dockerfile
```

-	Layers:
	-	`sha256:b44003cd1ea209090a063c5abfb4ee881849abba47e8711191b7637f86d8ee8b`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 94.9 KB (94856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f431de53d9b6c7e2cbc847af9daec064d061f8bd625615734012051336c495a`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 20.5 KB (20472 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-alpine3.23` - linux; ppc64le

```console
$ docker pull memcached@sha256:8182e35a9a404f0b522cb3c176d3dc4aade974e5556184c0a5a19e800721868a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6034321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30c6f532e81b50ea71c3520a80da0c8154b4cb14ebc17f87eb3a026862b47ed8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:41 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:17:43 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:20:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:20:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:20:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:20:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:20:22 GMT
USER memcache
# Wed, 15 Apr 2026 20:20:22 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:20:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee88d1c88fa46aa906a297c2919c9a085e74d04f20e4f827ca240a20f10ad34`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c574329cc1ebf156e2d89ab608bd58a3c0db550845c0ec394d265aa98fc5c4`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 126.3 KB (126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc2a28510bcba91734e7b38682847296011b63458db8a87a4bcecd180b8de7b5`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 2.1 MB (2075767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c524eb15ef0a41bf969efc93ef579db92dc59e8df57c9abfd099e7f6ff0756`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bde8ceae30a2a0890715bbc591167ee301c57d7f75023e80be460035187def`  
		Last Modified: Wed, 15 Apr 2026 20:20:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:4051408ef6c5bf4d4f37abf19c13f0298d8baa81770fcbfb588221e49e3bb834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ec3a4d49e6f325e484db43c9c9981f4eaa0223d9ae98282d95c3ee20c2089cb`

```dockerfile
```

-	Layers:
	-	`sha256:0e4e65db585f857844a67a831eb876dbb0a8a40d9269393d6c0fa83a2df995ae`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 94.3 KB (94308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50f58ec8aff3c96cc7b58e689122c27ee26121c598034cdc59ec95fd6423effe`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-alpine3.23` - linux; riscv64

```console
$ docker pull memcached@sha256:f3209d1ca2c4ce827614d16445231d96372944d218f18fd22850eec83874e5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5772332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e30170e0826b89d0ca59ffcae54b850ded07e6ae9451ecf1fd60f3ca8adcc725`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2026 00:00:48 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 16 Apr 2026 00:00:52 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 16 Apr 2026 00:14:21 GMT
ENV MEMCACHED_VERSION=1.6.41
# Thu, 16 Apr 2026 00:14:21 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Thu, 16 Apr 2026 00:14:21 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Thu, 16 Apr 2026 00:14:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 16 Apr 2026 00:14:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Apr 2026 00:14:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 16 Apr 2026 00:14:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Apr 2026 00:14:22 GMT
USER memcache
# Thu, 16 Apr 2026 00:14:22 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 16 Apr 2026 00:14:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62b143e34f5b89277e3a88ed4d722339d188a094d4bb534e222ca80e7741031`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bfff7c64f831ba03c491874cdf9a1c3f42bff72bb0e1951c63d8cf718854cff`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 108.9 KB (108903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69aef1050272a61cfbfd97c041d3776f96bdd03b102f2c3c54bbb0af2e1235a5`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 2.1 MB (2074414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ce340fb37f86db0d3aa774c23880b7c8322d2af8e3adc27a6ffa25d67c2122`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e40c6fb92d819994d38fae7accdffd583465eb6e645834b66f3ce9f0562f69`  
		Last Modified: Thu, 16 Apr 2026 00:14:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:2caae198d1efb7d4df14da45a3ff360a697982b544a61a3f907076b414983ea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1503bd38f4b30bc91be18dd93359e7376a9da1c7cb652ade64efd154064543fe`

```dockerfile
```

-	Layers:
	-	`sha256:e2d79fb634d76e28f055ab09953f59c371b93599e2b79f20f3d758f2c9520118`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 94.3 KB (94304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3614ad9b1715c3d6aa488496fca74d7143ea095d227f599407c933c62ec266aa`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 20.6 KB (20604 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-alpine3.23` - linux; s390x

```console
$ docker pull memcached@sha256:1da27660ae89a83aaf603e1affd51be573e5b8dac6c07ed592aee2a3a2b20581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5859702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13aa64df69a308e46b054bbd8e7a5d2f1e079005771f61748dae0d049889ba7f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:14:40 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:14:41 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:17:58 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:17:58 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:17:58 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:17:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:17:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:17:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:17:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:17:58 GMT
USER memcache
# Wed, 15 Apr 2026 20:17:58 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:17:58 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c42733e5f451590186b9b76c4b374ae5a84b657f7f1fd405647f5ba82c65bcd`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a14431ac88e8fe205b07f09b7e4843bb254de41cbc044725d6eaee3c2f822f`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 114.3 KB (114293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6377b7d98f32173cd47682aa73b32e4eba42781fa9224b9eb7a6f87367d37f94`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 2.0 MB (2017525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d022ae992296922747a4b69694b0185a0ce1f6cdece7f794e39e74dab92d250`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255cb3a435cbd623c1235d0429160faf72c244a6c1a613525df36f58a8c1f784`  
		Last Modified: Wed, 15 Apr 2026 20:18:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:531ee140f06db77d73b71bce7339abec3c6d976092bb80542bb337bb406acdbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b17d6f7e71efe3ee05ebcdb8ae90c28cf60db9ef069b0a98fe442c949740a6c`

```dockerfile
```

-	Layers:
	-	`sha256:820a080f49bf9e33948dbe5c13f6254f135d90bcb2b2277e3d2fd2430626c1a2`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 94.2 KB (94250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8ab82f4f240f46f9e34b74691925ab4af7f1cbb12ad3cb8639e0f317cf06653`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.41-trixie`

```console
$ docker pull memcached@sha256:277e0c4f249b118e95ab10e535bae2fa1af772271d9152f3468e58d59348db56
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

### `memcached:1.6.41-trixie` - linux; amd64

```console
$ docker pull memcached@sha256:518f136cafc43439a777c20224d30b6fadc3433e3de9573f514dca10dd7e0082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32198630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ec7b3eba028951d3aeee1ef26a365c913edaf06de6c008653f175c0ff0078ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:21:37 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 22 Apr 2026 01:21:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:24:27 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 22 Apr 2026 01:24:27 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 22 Apr 2026 01:24:27 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 22 Apr 2026 01:24:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 22 Apr 2026 01:24:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:24:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:24:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:24:27 GMT
USER memcache
# Wed, 22 Apr 2026 01:24:27 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 Apr 2026 01:24:27 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53e27a8dc2608bcd39496d6e1a0a021aa8933953409444f778d810ec220ab89`  
		Last Modified: Wed, 22 Apr 2026 01:24:33 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d02c07f7ffb4ea4d70b3af1ed59da72e778c143718ba2a7bcb8cd6d12afd95b`  
		Last Modified: Wed, 22 Apr 2026 01:24:33 GMT  
		Size: 136.7 KB (136658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b1a619145ef14a0e4599b98a19dbdc4fc96cfdf359ecf816454cd80ccf2dd2`  
		Last Modified: Wed, 22 Apr 2026 01:24:34 GMT  
		Size: 2.3 MB (2280287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7716efee154a639ac02ada0d1638837bb72c3fc33ecac40f78ffb91daf9dfc5`  
		Last Modified: Wed, 22 Apr 2026 01:24:34 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712f24abcdc2a432d57253a569a16eddd36ff1f8a4ace323467cdb642eae2850`  
		Last Modified: Wed, 22 Apr 2026 01:24:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:f32546667bf4926fd4e7c91aa55a833e8636777f2aa68437cb2bc7a5330e2307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3700c2c8b8182ac20db287282cdafbde42f55966784e109b48a9e5c2ba4d7492`

```dockerfile
```

-	Layers:
	-	`sha256:a3fe3f55746c35c0a798536b5abfc78349217684ca67ba43649a1c86d2a6ebe3`  
		Last Modified: Wed, 22 Apr 2026 01:24:33 GMT  
		Size: 2.0 MB (2008326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0b151a6f180676864b1e8721dddbaf0c105e743520356d58f7df86572a295fa`  
		Last Modified: Wed, 22 Apr 2026 01:24:33 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-trixie` - linux; arm variant v5

```console
$ docker pull memcached@sha256:4b91aeabb9b5d253e27cc0e6f6fa6cc82780c4d686f484c9ed1057a1dd429ba2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30305389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e62e4552c0bfc9dd8f4797df2c1386943df5780d342654ed3050e75668231e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:17:31 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 22 Apr 2026 01:17:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:20:57 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 22 Apr 2026 01:20:57 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 22 Apr 2026 01:20:57 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 22 Apr 2026 01:20:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 22 Apr 2026 01:20:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:20:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:20:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:20:57 GMT
USER memcache
# Wed, 22 Apr 2026 01:20:57 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 Apr 2026 01:20:57 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6496d93bca0663211b9252da346044ecb734ee5b3ecaae5b1fbd230753faee2f`  
		Last Modified: Wed, 22 Apr 2026 00:15:59 GMT  
		Size: 27.9 MB (27948180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64cdc01a23d15e84ef2ee2165c1a90970fb54d98f29377fa63fbd82988cdcc40`  
		Last Modified: Wed, 22 Apr 2026 01:21:03 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:303fc6e2ad4e0da497f7e238e61ec9e1fbde60909262de4a50e05c4db2191602`  
		Last Modified: Wed, 22 Apr 2026 01:21:03 GMT  
		Size: 144.2 KB (144163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c438ec3169ba426bc8374ca37b4f159272d50b60173c35c396f8fbf2208b8806`  
		Last Modified: Wed, 22 Apr 2026 01:21:03 GMT  
		Size: 2.2 MB (2211533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b5512f6aab6e3147798ce406f1035f68f18c2dd046b5fdd6344a17ace7fb31`  
		Last Modified: Wed, 22 Apr 2026 01:21:03 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a320e8acb7760a30eb688cd929fda03bf41ba23a307e06071106c3c0415d03`  
		Last Modified: Wed, 22 Apr 2026 01:21:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:4faa0397c26f0f4a312a28578db40b0f95f89c09769520c7cc09900886412dd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af54d9e6dbb4f86d5a79e417071faea8dd939b7758f640ce360a49c55069e2eb`

```dockerfile
```

-	Layers:
	-	`sha256:1850a912cc062cca1f70a2b76861d54c0ad06921d2a4960a7c483b5f8820eaa1`  
		Last Modified: Wed, 22 Apr 2026 01:21:03 GMT  
		Size: 2.0 MB (2011329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02fdad23f354f6597bfec3258d6bbee5142bcce9e1faaa7de87f9859bf8c6d14`  
		Last Modified: Wed, 22 Apr 2026 01:21:03 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-trixie` - linux; arm variant v7

```console
$ docker pull memcached@sha256:4d262b60fea5a97e91a6c1827ab7209a344c47616388ada79b27e4e69eea9d38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28516774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02f2f7426f06caeeb218b724a947fa35544b0749bacf781227878e40cb98d08f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:18:06 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 22 Apr 2026 01:18:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:21:19 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 22 Apr 2026 01:21:19 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 22 Apr 2026 01:21:19 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 22 Apr 2026 01:21:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 22 Apr 2026 01:21:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:21:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:21:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:21:19 GMT
USER memcache
# Wed, 22 Apr 2026 01:21:19 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 Apr 2026 01:21:19 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9e541e5bfbbe69b7bbe01cd2f1abf8560e2e43bf76eb96b2e88a3df29020834b`  
		Last Modified: Wed, 22 Apr 2026 00:17:02 GMT  
		Size: 26.2 MB (26214838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0867e20c7ab47539b3f27abc4c7f4bf41d367127d9ffbd30a531ab387a69e2e`  
		Last Modified: Wed, 22 Apr 2026 01:21:25 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34eedf23d5ae4af59fe6ecfd854e48545ede507ce44d930cea5c11b652b31f4`  
		Last Modified: Wed, 22 Apr 2026 01:21:25 GMT  
		Size: 135.4 KB (135382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fff54fd1447de9c8b377640a2720588785769320b1a65d59a1da8e9690e6f9`  
		Last Modified: Wed, 22 Apr 2026 01:21:25 GMT  
		Size: 2.2 MB (2165043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac214a1bada6a999cda6b6b021b8ef5ba954108062e3ee4df0161a500fc566f`  
		Last Modified: Wed, 22 Apr 2026 01:21:25 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0431aacefa9d6f210c7c4778e75df5a21c196127779acc2da1bd7b32088f47dc`  
		Last Modified: Wed, 22 Apr 2026 01:21:26 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:e4f840cb65bd892b2aafc305cb008de10d4d41475876ef9c9bbf51831f9cd7e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:987452d71cfba90bac820fca09f2954a061813125a8832038df5c062224577c5`

```dockerfile
```

-	Layers:
	-	`sha256:f5793a9489c1e1010726124554d7404a19b2675ce8596a38169b160edc81d045`  
		Last Modified: Wed, 22 Apr 2026 01:21:25 GMT  
		Size: 2.0 MB (2009786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef3c23077c5adc1a06a0e1f66d0ec1e57032a5b35685c53064098e236a62c5a1`  
		Last Modified: Wed, 22 Apr 2026 01:21:25 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-trixie` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:52e2a52a542b0fff64533e7271ce3af9825a80a1126998cf6070b0ec4c0030b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32560736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c3fcfefa704f0162e85ab03d515502e07a6ff91ec994dc4b6c956cc2ce80990`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:22:08 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 22 Apr 2026 01:22:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:25:10 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 22 Apr 2026 01:25:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 22 Apr 2026 01:25:10 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 22 Apr 2026 01:25:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 22 Apr 2026 01:25:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:25:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:25:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:25:10 GMT
USER memcache
# Wed, 22 Apr 2026 01:25:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 Apr 2026 01:25:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebea5231ebe63bff9044a4ee7713dac1b62fc15d85ee920f04eae4010a67b668`  
		Last Modified: Wed, 22 Apr 2026 01:25:16 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5921030f644563277c2af1be27b21dfded0e01763210710efac613f07dc74c`  
		Last Modified: Wed, 22 Apr 2026 01:25:16 GMT  
		Size: 153.5 KB (153515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1ef7f1deafd8e81fec98af35ef4fe12c2436c1eddb6bb87377b83f524f7d6f`  
		Last Modified: Wed, 22 Apr 2026 01:25:16 GMT  
		Size: 2.3 MB (2262106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd4f58ffc6f10cea1171fbb552aff0b93a04aba0ca6815cd9ad66ab3a49f8419`  
		Last Modified: Wed, 22 Apr 2026 01:25:16 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace7ea462603345a875235135df0b8dd036890eacdb25150c1a8089604e3ca1f`  
		Last Modified: Wed, 22 Apr 2026 01:25:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:63aba0d160ad2159dd41a074d79446fc4ba2e745c7e5a10a41dbd1d5c2abc86d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b67f2365f86c60d496eb140fde16a0d6fbf89ae6a83d200c6a3971e32eca706b`

```dockerfile
```

-	Layers:
	-	`sha256:e87d247df404b9fe7e19667c95311e8109ea54acdcca2f52ceba73b7099d144e`  
		Last Modified: Wed, 22 Apr 2026 01:25:16 GMT  
		Size: 2.0 MB (2008642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5290960be9e7480bf28bf59599ba02b7792ea80b3309570c3b3a24465ad7d58`  
		Last Modified: Wed, 22 Apr 2026 01:25:16 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-trixie` - linux; 386

```console
$ docker pull memcached@sha256:0b8f07a6f169bfe4cc362cbabca8c92d5140665660c615383f2755c40c0036f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33670125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd6a79877127262a308ef5f3bd216749c6f0b1fc43971b56c533d4e47f5c6de2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:17:33 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 22 Apr 2026 01:17:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:20:28 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 22 Apr 2026 01:20:28 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 22 Apr 2026 01:20:28 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 22 Apr 2026 01:20:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 22 Apr 2026 01:20:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:20:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:20:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:20:28 GMT
USER memcache
# Wed, 22 Apr 2026 01:20:28 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 Apr 2026 01:20:28 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:dacd7cda306bf5bd7a2030f9b0c2e9d71fda44ea58493a33450d210b74a8ec75`  
		Last Modified: Wed, 22 Apr 2026 00:17:04 GMT  
		Size: 31.3 MB (31296327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a0c9fe363e7e198726a5e39cf627131e43cd59d319a350f978180f6f449b8a`  
		Last Modified: Wed, 22 Apr 2026 01:20:34 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dff2976b24139841065357d1f81c8cf6d9b45ee35e2947f1345e86493b2f5e67`  
		Last Modified: Wed, 22 Apr 2026 01:20:34 GMT  
		Size: 147.5 KB (147529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8b8718f120acc0033835790e0bd541e38b843c6b260688b8fde3c94eadd5911`  
		Last Modified: Wed, 22 Apr 2026 01:20:34 GMT  
		Size: 2.2 MB (2224758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f70ea447cee314191f67e0ce5ccc23703730c89810e26bfa3f96f81964849dc`  
		Last Modified: Wed, 22 Apr 2026 01:20:34 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:789bc1b0beaaf9809e3cab832a0b6b29f50aec3b18f7a7cdf04e343d3ee800a3`  
		Last Modified: Wed, 22 Apr 2026 01:20:35 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:45cfea0c565e5e6c79f4a36cf4ec611ccc7e910c481110b37be04eca3276511b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d33423fad9c4c2f3b1af3eb87b8af48d7cfc9e00d70e6c33937d7d215fb94c5`

```dockerfile
```

-	Layers:
	-	`sha256:2656e01c20323e582a0ba03c06d82008eb35ae9850f7d6c7f73c0e5ae040805b`  
		Last Modified: Wed, 22 Apr 2026 01:20:34 GMT  
		Size: 2.0 MB (2005483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d267990174d3038591d6a8ffe07af06d961bb5c68b86a9cdac459f5a0996ddbe`  
		Last Modified: Wed, 22 Apr 2026 01:20:34 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-trixie` - linux; ppc64le

```console
$ docker pull memcached@sha256:3df945008f026e1a7782fc67d0107a07c9103d9d50dd7ae605082ea97fb64ff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36164269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7eb2db1cbb0c7ddc2688ee498498fb5122ee78ab349b636a43585b1beb30da9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:35:49 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 22 Apr 2026 01:35:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:39:22 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 22 Apr 2026 01:39:22 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 22 Apr 2026 01:39:22 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 22 Apr 2026 01:39:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 22 Apr 2026 01:39:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:39:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:39:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:39:23 GMT
USER memcache
# Wed, 22 Apr 2026 01:39:23 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 Apr 2026 01:39:23 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b5fd051d0fcd0789e7358cba300f83befdba943416041497be86050e282a6d02`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 33.6 MB (33598032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e271c91c5c30b04dee49fb4c9ab2f9863d13146641f1b8681b59467d0f8ab5`  
		Last Modified: Wed, 22 Apr 2026 01:39:42 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb7fa3c8c45f87e36929f71acaead9bcb07985c205ea0aa6fd83aca31691d78`  
		Last Modified: Wed, 22 Apr 2026 01:39:42 GMT  
		Size: 170.4 KB (170378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f09610f9abffbf6411865ebc07ee20de6c14b2250467c4682f423dddc0ab82`  
		Last Modified: Wed, 22 Apr 2026 01:39:42 GMT  
		Size: 2.4 MB (2394347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a0fb856cc435334489ebeec58afd76f4e676c8bae4b3688daefedfbc7f7c1a8`  
		Last Modified: Wed, 22 Apr 2026 01:39:42 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea36b259fc26e36b99ded4a3aa0ca190c1117ecd424f26565f8474b55964d787`  
		Last Modified: Wed, 22 Apr 2026 01:39:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:c619fe6b2206166796157b814c0d60ca38e29a646b71cd6f5635e2f507cf70d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49e66f35bf963d54f332469bbdef0ca608c651311f5af0e923aca630f4429ae9`

```dockerfile
```

-	Layers:
	-	`sha256:f870fab207e6594315e4d18f50f3ebf834ebc298b6ec128104607668ae939995`  
		Last Modified: Wed, 22 Apr 2026 01:39:42 GMT  
		Size: 2.0 MB (2011927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bf20b8b72f84425e9121a35ea191dab3cf17562679390195740f260304727d7`  
		Last Modified: Wed, 22 Apr 2026 01:39:42 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-trixie` - linux; riscv64

```console
$ docker pull memcached@sha256:5554043a87027cff145bdb04810a9f8a067c72479937ce0328af056a5c3efe8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30623256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad08d83e675d61f6e230bee3e1d5d5e4b4e8d0b1b3656b71812168b7db5e08e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 08:28:54 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 22 Apr 2026 08:29:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 08:55:11 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 22 Apr 2026 08:55:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 22 Apr 2026 08:55:11 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 22 Apr 2026 08:55:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 22 Apr 2026 08:55:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 08:55:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 08:55:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 08:55:12 GMT
USER memcache
# Wed, 22 Apr 2026 08:55:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 Apr 2026 08:55:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8aa73197c6983c411cf26b41c64a557cfc81f9b4e6d897ff2829a66eac03b37`  
		Last Modified: Wed, 22 Apr 2026 08:55:56 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee379d85ef42145b3f09328c98634e8cd3320230281217ad58867c6982e1d8c`  
		Last Modified: Wed, 22 Apr 2026 08:55:57 GMT  
		Size: 133.1 KB (133094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:310a92cbf1cb95664c58022062af028a81e69f127cd8d9ee044bf7d5087db961`  
		Last Modified: Wed, 22 Apr 2026 08:55:57 GMT  
		Size: 2.2 MB (2208455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336575624802c397f4947f3ddfc2737281bfe2ba8cd714be646b72152c1ec1d0`  
		Last Modified: Wed, 22 Apr 2026 08:55:56 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e926175ab529d298755a0e0507accca74feec6c90ea4495edeaafb07954ad57d`  
		Last Modified: Wed, 22 Apr 2026 08:55:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:9b8b4751f5823830cf382050f0174dd5ade6dc0650b2a3134803b886b2652dba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bc1698424d742c630d5a555fa2c70be3195da5b1a2cd148a331c7aa9fb94b6f`

```dockerfile
```

-	Layers:
	-	`sha256:18aa82332065ff68528148bb97bd5681424d4c57e9e5e331b8908b44023570a9`  
		Last Modified: Wed, 22 Apr 2026 08:55:57 GMT  
		Size: 2.0 MB (2002290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edeefd058e4dbdf6c3026618be5f5184cd3d2c22f14746d890cd45a42004dc8f`  
		Last Modified: Wed, 22 Apr 2026 08:55:57 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-trixie` - linux; s390x

```console
$ docker pull memcached@sha256:e0fadaa0ad7c323c4f8ead5d8e1ebb9566adc59b25cbc280f40bef816f9d62eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32280559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5d7f2d629511f566dd7c4b3a944adb9989b05bb41dbd3e3881734bc1c1079c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:19:00 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 22 Apr 2026 01:19:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:22:27 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 22 Apr 2026 01:22:27 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 22 Apr 2026 01:22:27 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 22 Apr 2026 01:22:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 22 Apr 2026 01:22:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:22:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:22:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:22:27 GMT
USER memcache
# Wed, 22 Apr 2026 01:22:27 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 Apr 2026 01:22:27 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:71574deb335f1e823f938f4a215de00a90d63866898f1f354a0b15e8b9c30577`  
		Last Modified: Wed, 22 Apr 2026 00:17:08 GMT  
		Size: 29.8 MB (29840300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b460058bd06ca18e629070cadcc158edef16e034340796f661d4fab362ee94`  
		Last Modified: Wed, 22 Apr 2026 01:22:38 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5386c57fa90d49931296cf79f5e8d2ae18d07b9bcffe5eee8354033fee4b673`  
		Last Modified: Wed, 22 Apr 2026 01:22:38 GMT  
		Size: 140.5 KB (140521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd8308c0fc0224d29acef5aadae977dfea2e1ba7c9be0e207ee89c84a4f6417`  
		Last Modified: Wed, 22 Apr 2026 01:22:38 GMT  
		Size: 2.3 MB (2298228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fda405f0b2226447c88ba0d395ee00616ec775cecba66d9a980d4aac7b44fb49`  
		Last Modified: Wed, 22 Apr 2026 01:22:38 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fcaa079ef0e24aab0065df6b15e28d19a0807e2c9cdc639bbc63923135e6daa`  
		Last Modified: Wed, 22 Apr 2026 01:22:39 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:7d2e45f2ecd9448a99f98a077da16fb59c37827c2acbac9e99dea8f79d753165
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54358ef5a62ded9fafc9e908e79d81e5d01102cd4f2082017f54d92232acb7c4`

```dockerfile
```

-	Layers:
	-	`sha256:eb9c1105cc4bf8d4cf2089f7a2a43afe0a113388e7f5a4af9db1f44f9f0fbe11`  
		Last Modified: Wed, 22 Apr 2026 01:22:38 GMT  
		Size: 2.0 MB (2009763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af1c4a20085e6a6f3d2b2fcb2ce9c10456d057c6905b84fe6ad6d99ba351a872`  
		Last Modified: Wed, 22 Apr 2026 01:22:38 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine`

```console
$ docker pull memcached@sha256:65c80b311a9601ef5ca8af3814e5cd06a9c4277ea139d80bd53da6b4d39eb46e
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
$ docker pull memcached@sha256:7b962825022657b112923d502400d5734870d5eb12c19e7f1f6585f7534a6795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5959872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b58f7e71f30daaa3f466fa31d855fddb7101e42c0c42fac520be5d1d43ec32e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:46 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:17:47 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:20:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:20:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:20:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:20:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:20:22 GMT
USER memcache
# Wed, 15 Apr 2026 20:20:22 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:20:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73d5ffe265b83073ce3c7211fb3c15ebbd5e7146d870d9ce69d2e7dfc493348`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6cb4fdd95ced0d5a9528e97ff0f20742749cbd9ef6dc1322d13e682a7085a67`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 106.1 KB (106063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe17fc291d9444fbae93d7f45eab008318f87302c016c06e6e911c1a571a053`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 2.0 MB (1988274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1948bd131d2cbd05c6bf2962d18b15d105abee6f42f398bab3c13737537f197`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bde8ceae30a2a0890715bbc591167ee301c57d7f75023e80be460035187def`  
		Last Modified: Wed, 15 Apr 2026 20:20:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:58ed333482f8a8530c82ad7399d5917a7db85fbcdf70fc1dec55fbedcdf09253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4255278359004afd8c94db1a7fe6129fc984d0716c33665c9eca3168476fdcb`

```dockerfile
```

-	Layers:
	-	`sha256:5f47d88d89d22d065a3590d477ae130520b882176ab07e95862afb4d8b69b214`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 94.9 KB (94901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab2d532e4a6ce2f362d25c79dfaeb88d333fe6efe7c1b5b293630bf6ca292eb8`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 20.5 KB (20530 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:47a06cd0daead339b96ed90e425336a8a49a75e4e358b5ec1ea63a630720f704
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3947facc9e9fae3eee283f24b611a8ae87e353b6d6447bc6f582e90f2fce3743`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:58 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:17:59 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:21:02 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:21:02 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:21:02 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:21:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:21:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:21:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:21:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:21:03 GMT
USER memcache
# Wed, 15 Apr 2026 20:21:03 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:21:03 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77001163fdaab47f07a85fc5bb15f3512a8cb9b9b049cec7e0c88bcbbdb5bb5d`  
		Last Modified: Wed, 15 Apr 2026 20:21:07 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee1b43c0cfbf2ee56e39441933ff06803264d22918fe867d8b5ba7d5adfb9c3`  
		Last Modified: Wed, 15 Apr 2026 20:21:06 GMT  
		Size: 102.6 KB (102630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c041bfac12e599ad87749289dec9672dac36e8c0e16779f13fa695d10f2f0cc5`  
		Last Modified: Wed, 15 Apr 2026 20:21:07 GMT  
		Size: 1.9 MB (1937835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2dfd492dd0f295311a0c314fae06f4b325ae22cb0e673a53e0705f3d4e0504`  
		Last Modified: Wed, 15 Apr 2026 20:21:07 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671c66eac839c2f0a5b2e64d1f581069c4cdf119e784bff16540ecc94e2c2b10`  
		Last Modified: Wed, 15 Apr 2026 20:21:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:2a6148a6aebb042e55781b40ed626d0c5871833be4ae8dc303af7aace07d9d60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbaadfaacfaf0e7c226b35236bb84c2268d4c6eb017efd435a3999a44edfcc77`

```dockerfile
```

-	Layers:
	-	`sha256:c68bb3ee35fc0ac716bca45cc759f3b1ff52b1d5a0acae9876eaf0aa55aa667d`  
		Last Modified: Wed, 15 Apr 2026 20:21:06 GMT  
		Size: 20.5 KB (20466 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:fb58bae12ffa00c9cbafc8bee2341b43ffdccacbde7085fa707ef6c7f2d69e37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5273034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddd4e85c30e4df5803b553b8a7f84084c3dae6f72531ac70fcabf7099cfa8148`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 21:14:38 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 21:14:39 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 21:17:34 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 21:17:34 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 21:17:34 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 21:17:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 21:17:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:17:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 21:17:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:17:34 GMT
USER memcache
# Wed, 15 Apr 2026 21:17:34 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 21:17:34 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e312136cfedda9620407d42650d0595220e60d3c40ae8853bfbdd83f392b9e6`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53697a39f37b691917c91310ac4e107308674bddcc9017e3bbc0d0134eaf4c3e`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 92.4 KB (92369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5e4be9e0df543f152c376fe2cc74b89b75585793fdbd7d12476737d386d8e1`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 1.9 MB (1896191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a083f41edf5f859feb4367eeeea0955dc9799c8202fb8a67c40915ed5b195002`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c43503b1f4f42ffc5e0e4415befe45199dec730bc26347df151298345ba640`  
		Last Modified: Wed, 15 Apr 2026 21:17:40 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7535cf6b6a140771131c2c524301d4616f34856fcd8ecbe3e52300108c49de2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d73c906894a0a3d178edd69991f310225c0daef314e6faa83a0b9adecfbeb34`

```dockerfile
```

-	Layers:
	-	`sha256:8f1fddd7d14560fb90f381b09cde9302dfc9253e6702adf28c55961d755b1ad8`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 94.3 KB (94319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fcf119d246607aa25330c4c05fe14a64cebda69b02d14507862a9f07c1404e6`  
		Last Modified: Wed, 15 Apr 2026 21:17:38 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:6d70439467a65065c52894232a3085c724da2810a9b3205130d5e434ab411e3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6288798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4be3e105216d2507b68e772f7d08d52a5076dd55fad35c29775038d05c24112`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:15:23 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:15:24 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:18:13 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:18:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:18:13 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:18:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:18:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:18:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:18:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:18:13 GMT
USER memcache
# Wed, 15 Apr 2026 20:18:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:18:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81758f5fc2e8fa13e3625f253d7c999560ac666121c026f7251dbfb919cca611`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d735737d3a0cf1eda63bd72c09f64eb679313e9c5f8a105849848bdd779e1d`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 121.8 KB (121846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ac0921d2cc2b3388e0f006a6672c5a9e1098a59e570121dde092104d845c51`  
		Last Modified: Wed, 15 Apr 2026 20:18:19 GMT  
		Size: 2.0 MB (1965733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca9cf731b18a76c3ac25cc3add219660d57516c12680d7b1f1ece282406eb82`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:717a6b23dd1cd76b686bf26066af23265e0d002ed6a3e87f6aa4f79264b7da11`  
		Last Modified: Wed, 15 Apr 2026 20:18:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7e5232b868d3222e3ce2b0ee39c62f6cb294bea27456b00940fbc4e3c8c3f84d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:780bf975a24d5fdc511c857720c04cb077d64abcfe4c93ea0db7c9487c323718`

```dockerfile
```

-	Layers:
	-	`sha256:addb0f46e3b5adb674175c11fc85526d4628e24d74d210c8b00c9a945b44407c`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 94.4 KB (94355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3364e418b74b6f6ca17deec7d55783a6e1554de3783ab0a6d5e56496d935ddb0`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 20.7 KB (20728 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; 386

```console
$ docker pull memcached@sha256:80328bf779fa1494f7677b441ad1c16c2134f126e6556953deb3cfab1c4c9770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5744816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d957405dd0811f1cd15fe39563938a60c2008204d2f63ebc7e39f8989c796f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 22:20:45 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 22:20:46 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 22:23:32 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 22:23:32 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 22:23:32 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 22:23:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 22:23:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 22:23:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 22:23:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 22:23:32 GMT
USER memcache
# Wed, 15 Apr 2026 22:23:32 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 22:23:32 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0617a09eee85c2032f5596ded56b733366513074f9096177315b50dc45485e20`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c67275dbc381ac3ae0b21dda20edaf245e2ca54d6f5dc3af8805db03c17cc93`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 110.7 KB (110715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6ecb23f1f4bc89d5c315aac493f29fe7bb33061c70d926c904f4f55d374461`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 1.9 MB (1942309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e782df8f482a58603ea70ef9e04e838d044a6070c7e4cd116c90a09b917ed940`  
		Last Modified: Wed, 15 Apr 2026 22:23:38 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616df56d574e39c00ae772c6a29e2b724698048a83cc29ea17049573f9073b10`  
		Last Modified: Wed, 15 Apr 2026 22:23:38 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:c726e7abf461d963e544818339e4cd12fd2f31e41436475f0e51818a0885fbdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12e41b9d6f745d686c2649255bd14fe4e0b97a3477d383e719490e5ef66b27ae`

```dockerfile
```

-	Layers:
	-	`sha256:b44003cd1ea209090a063c5abfb4ee881849abba47e8711191b7637f86d8ee8b`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 94.9 KB (94856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f431de53d9b6c7e2cbc847af9daec064d061f8bd625615734012051336c495a`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 20.5 KB (20472 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:8182e35a9a404f0b522cb3c176d3dc4aade974e5556184c0a5a19e800721868a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6034321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30c6f532e81b50ea71c3520a80da0c8154b4cb14ebc17f87eb3a026862b47ed8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:41 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:17:43 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:20:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:20:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:20:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:20:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:20:22 GMT
USER memcache
# Wed, 15 Apr 2026 20:20:22 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:20:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee88d1c88fa46aa906a297c2919c9a085e74d04f20e4f827ca240a20f10ad34`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c574329cc1ebf156e2d89ab608bd58a3c0db550845c0ec394d265aa98fc5c4`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 126.3 KB (126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc2a28510bcba91734e7b38682847296011b63458db8a87a4bcecd180b8de7b5`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 2.1 MB (2075767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c524eb15ef0a41bf969efc93ef579db92dc59e8df57c9abfd099e7f6ff0756`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bde8ceae30a2a0890715bbc591167ee301c57d7f75023e80be460035187def`  
		Last Modified: Wed, 15 Apr 2026 20:20:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:4051408ef6c5bf4d4f37abf19c13f0298d8baa81770fcbfb588221e49e3bb834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ec3a4d49e6f325e484db43c9c9981f4eaa0223d9ae98282d95c3ee20c2089cb`

```dockerfile
```

-	Layers:
	-	`sha256:0e4e65db585f857844a67a831eb876dbb0a8a40d9269393d6c0fa83a2df995ae`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 94.3 KB (94308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50f58ec8aff3c96cc7b58e689122c27ee26121c598034cdc59ec95fd6423effe`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:f3209d1ca2c4ce827614d16445231d96372944d218f18fd22850eec83874e5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5772332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e30170e0826b89d0ca59ffcae54b850ded07e6ae9451ecf1fd60f3ca8adcc725`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2026 00:00:48 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 16 Apr 2026 00:00:52 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 16 Apr 2026 00:14:21 GMT
ENV MEMCACHED_VERSION=1.6.41
# Thu, 16 Apr 2026 00:14:21 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Thu, 16 Apr 2026 00:14:21 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Thu, 16 Apr 2026 00:14:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 16 Apr 2026 00:14:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Apr 2026 00:14:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 16 Apr 2026 00:14:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Apr 2026 00:14:22 GMT
USER memcache
# Thu, 16 Apr 2026 00:14:22 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 16 Apr 2026 00:14:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62b143e34f5b89277e3a88ed4d722339d188a094d4bb534e222ca80e7741031`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bfff7c64f831ba03c491874cdf9a1c3f42bff72bb0e1951c63d8cf718854cff`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 108.9 KB (108903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69aef1050272a61cfbfd97c041d3776f96bdd03b102f2c3c54bbb0af2e1235a5`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 2.1 MB (2074414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ce340fb37f86db0d3aa774c23880b7c8322d2af8e3adc27a6ffa25d67c2122`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e40c6fb92d819994d38fae7accdffd583465eb6e645834b66f3ce9f0562f69`  
		Last Modified: Thu, 16 Apr 2026 00:14:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:2caae198d1efb7d4df14da45a3ff360a697982b544a61a3f907076b414983ea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1503bd38f4b30bc91be18dd93359e7376a9da1c7cb652ade64efd154064543fe`

```dockerfile
```

-	Layers:
	-	`sha256:e2d79fb634d76e28f055ab09953f59c371b93599e2b79f20f3d758f2c9520118`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 94.3 KB (94304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3614ad9b1715c3d6aa488496fca74d7143ea095d227f599407c933c62ec266aa`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 20.6 KB (20604 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; s390x

```console
$ docker pull memcached@sha256:1da27660ae89a83aaf603e1affd51be573e5b8dac6c07ed592aee2a3a2b20581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5859702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13aa64df69a308e46b054bbd8e7a5d2f1e079005771f61748dae0d049889ba7f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:14:40 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:14:41 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:17:58 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:17:58 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:17:58 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:17:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:17:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:17:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:17:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:17:58 GMT
USER memcache
# Wed, 15 Apr 2026 20:17:58 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:17:58 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c42733e5f451590186b9b76c4b374ae5a84b657f7f1fd405647f5ba82c65bcd`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a14431ac88e8fe205b07f09b7e4843bb254de41cbc044725d6eaee3c2f822f`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 114.3 KB (114293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6377b7d98f32173cd47682aa73b32e4eba42781fa9224b9eb7a6f87367d37f94`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 2.0 MB (2017525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d022ae992296922747a4b69694b0185a0ce1f6cdece7f794e39e74dab92d250`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255cb3a435cbd623c1235d0429160faf72c244a6c1a613525df36f58a8c1f784`  
		Last Modified: Wed, 15 Apr 2026 20:18:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:531ee140f06db77d73b71bce7339abec3c6d976092bb80542bb337bb406acdbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b17d6f7e71efe3ee05ebcdb8ae90c28cf60db9ef069b0a98fe442c949740a6c`

```dockerfile
```

-	Layers:
	-	`sha256:820a080f49bf9e33948dbe5c13f6254f135d90bcb2b2277e3d2fd2430626c1a2`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 94.2 KB (94250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8ab82f4f240f46f9e34b74691925ab4af7f1cbb12ad3cb8639e0f317cf06653`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine3.23`

```console
$ docker pull memcached@sha256:65c80b311a9601ef5ca8af3814e5cd06a9c4277ea139d80bd53da6b4d39eb46e
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
$ docker pull memcached@sha256:7b962825022657b112923d502400d5734870d5eb12c19e7f1f6585f7534a6795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5959872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b58f7e71f30daaa3f466fa31d855fddb7101e42c0c42fac520be5d1d43ec32e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:46 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:17:47 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:20:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:20:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:20:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:20:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:20:22 GMT
USER memcache
# Wed, 15 Apr 2026 20:20:22 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:20:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73d5ffe265b83073ce3c7211fb3c15ebbd5e7146d870d9ce69d2e7dfc493348`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6cb4fdd95ced0d5a9528e97ff0f20742749cbd9ef6dc1322d13e682a7085a67`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 106.1 KB (106063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe17fc291d9444fbae93d7f45eab008318f87302c016c06e6e911c1a571a053`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 2.0 MB (1988274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1948bd131d2cbd05c6bf2962d18b15d105abee6f42f398bab3c13737537f197`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bde8ceae30a2a0890715bbc591167ee301c57d7f75023e80be460035187def`  
		Last Modified: Wed, 15 Apr 2026 20:20:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:58ed333482f8a8530c82ad7399d5917a7db85fbcdf70fc1dec55fbedcdf09253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4255278359004afd8c94db1a7fe6129fc984d0716c33665c9eca3168476fdcb`

```dockerfile
```

-	Layers:
	-	`sha256:5f47d88d89d22d065a3590d477ae130520b882176ab07e95862afb4d8b69b214`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 94.9 KB (94901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab2d532e4a6ce2f362d25c79dfaeb88d333fe6efe7c1b5b293630bf6ca292eb8`  
		Last Modified: Wed, 15 Apr 2026 20:20:26 GMT  
		Size: 20.5 KB (20530 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.23` - linux; arm variant v6

```console
$ docker pull memcached@sha256:47a06cd0daead339b96ed90e425336a8a49a75e4e358b5ec1ea63a630720f704
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3947facc9e9fae3eee283f24b611a8ae87e353b6d6447bc6f582e90f2fce3743`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:58 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:17:59 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:21:02 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:21:02 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:21:02 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:21:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:21:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:21:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:21:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:21:03 GMT
USER memcache
# Wed, 15 Apr 2026 20:21:03 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:21:03 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77001163fdaab47f07a85fc5bb15f3512a8cb9b9b049cec7e0c88bcbbdb5bb5d`  
		Last Modified: Wed, 15 Apr 2026 20:21:07 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee1b43c0cfbf2ee56e39441933ff06803264d22918fe867d8b5ba7d5adfb9c3`  
		Last Modified: Wed, 15 Apr 2026 20:21:06 GMT  
		Size: 102.6 KB (102630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c041bfac12e599ad87749289dec9672dac36e8c0e16779f13fa695d10f2f0cc5`  
		Last Modified: Wed, 15 Apr 2026 20:21:07 GMT  
		Size: 1.9 MB (1937835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2dfd492dd0f295311a0c314fae06f4b325ae22cb0e673a53e0705f3d4e0504`  
		Last Modified: Wed, 15 Apr 2026 20:21:07 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671c66eac839c2f0a5b2e64d1f581069c4cdf119e784bff16540ecc94e2c2b10`  
		Last Modified: Wed, 15 Apr 2026 20:21:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:2a6148a6aebb042e55781b40ed626d0c5871833be4ae8dc303af7aace07d9d60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbaadfaacfaf0e7c226b35236bb84c2268d4c6eb017efd435a3999a44edfcc77`

```dockerfile
```

-	Layers:
	-	`sha256:c68bb3ee35fc0ac716bca45cc759f3b1ff52b1d5a0acae9876eaf0aa55aa667d`  
		Last Modified: Wed, 15 Apr 2026 20:21:06 GMT  
		Size: 20.5 KB (20466 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.23` - linux; arm variant v7

```console
$ docker pull memcached@sha256:fb58bae12ffa00c9cbafc8bee2341b43ffdccacbde7085fa707ef6c7f2d69e37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5273034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddd4e85c30e4df5803b553b8a7f84084c3dae6f72531ac70fcabf7099cfa8148`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 21:14:38 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 21:14:39 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 21:17:34 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 21:17:34 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 21:17:34 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 21:17:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 21:17:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:17:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 21:17:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:17:34 GMT
USER memcache
# Wed, 15 Apr 2026 21:17:34 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 21:17:34 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e312136cfedda9620407d42650d0595220e60d3c40ae8853bfbdd83f392b9e6`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53697a39f37b691917c91310ac4e107308674bddcc9017e3bbc0d0134eaf4c3e`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 92.4 KB (92369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5e4be9e0df543f152c376fe2cc74b89b75585793fdbd7d12476737d386d8e1`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 1.9 MB (1896191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a083f41edf5f859feb4367eeeea0955dc9799c8202fb8a67c40915ed5b195002`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c43503b1f4f42ffc5e0e4415befe45199dec730bc26347df151298345ba640`  
		Last Modified: Wed, 15 Apr 2026 21:17:40 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:7535cf6b6a140771131c2c524301d4616f34856fcd8ecbe3e52300108c49de2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d73c906894a0a3d178edd69991f310225c0daef314e6faa83a0b9adecfbeb34`

```dockerfile
```

-	Layers:
	-	`sha256:8f1fddd7d14560fb90f381b09cde9302dfc9253e6702adf28c55961d755b1ad8`  
		Last Modified: Wed, 15 Apr 2026 21:17:39 GMT  
		Size: 94.3 KB (94319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fcf119d246607aa25330c4c05fe14a64cebda69b02d14507862a9f07c1404e6`  
		Last Modified: Wed, 15 Apr 2026 21:17:38 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.23` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:6d70439467a65065c52894232a3085c724da2810a9b3205130d5e434ab411e3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6288798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4be3e105216d2507b68e772f7d08d52a5076dd55fad35c29775038d05c24112`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:15:23 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:15:24 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:18:13 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:18:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:18:13 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:18:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:18:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:18:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:18:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:18:13 GMT
USER memcache
# Wed, 15 Apr 2026 20:18:13 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:18:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81758f5fc2e8fa13e3625f253d7c999560ac666121c026f7251dbfb919cca611`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d735737d3a0cf1eda63bd72c09f64eb679313e9c5f8a105849848bdd779e1d`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 121.8 KB (121846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ac0921d2cc2b3388e0f006a6672c5a9e1098a59e570121dde092104d845c51`  
		Last Modified: Wed, 15 Apr 2026 20:18:19 GMT  
		Size: 2.0 MB (1965733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca9cf731b18a76c3ac25cc3add219660d57516c12680d7b1f1ece282406eb82`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:717a6b23dd1cd76b686bf26066af23265e0d002ed6a3e87f6aa4f79264b7da11`  
		Last Modified: Wed, 15 Apr 2026 20:18:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:7e5232b868d3222e3ce2b0ee39c62f6cb294bea27456b00940fbc4e3c8c3f84d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:780bf975a24d5fdc511c857720c04cb077d64abcfe4c93ea0db7c9487c323718`

```dockerfile
```

-	Layers:
	-	`sha256:addb0f46e3b5adb674175c11fc85526d4628e24d74d210c8b00c9a945b44407c`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 94.4 KB (94355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3364e418b74b6f6ca17deec7d55783a6e1554de3783ab0a6d5e56496d935ddb0`  
		Last Modified: Wed, 15 Apr 2026 20:18:18 GMT  
		Size: 20.7 KB (20728 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.23` - linux; 386

```console
$ docker pull memcached@sha256:80328bf779fa1494f7677b441ad1c16c2134f126e6556953deb3cfab1c4c9770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5744816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d957405dd0811f1cd15fe39563938a60c2008204d2f63ebc7e39f8989c796f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 22:20:45 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 22:20:46 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 22:23:32 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 22:23:32 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 22:23:32 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 22:23:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 22:23:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 22:23:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 22:23:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 22:23:32 GMT
USER memcache
# Wed, 15 Apr 2026 22:23:32 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 22:23:32 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0617a09eee85c2032f5596ded56b733366513074f9096177315b50dc45485e20`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c67275dbc381ac3ae0b21dda20edaf245e2ca54d6f5dc3af8805db03c17cc93`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 110.7 KB (110715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6ecb23f1f4bc89d5c315aac493f29fe7bb33061c70d926c904f4f55d374461`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 1.9 MB (1942309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e782df8f482a58603ea70ef9e04e838d044a6070c7e4cd116c90a09b917ed940`  
		Last Modified: Wed, 15 Apr 2026 22:23:38 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616df56d574e39c00ae772c6a29e2b724698048a83cc29ea17049573f9073b10`  
		Last Modified: Wed, 15 Apr 2026 22:23:38 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:c726e7abf461d963e544818339e4cd12fd2f31e41436475f0e51818a0885fbdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12e41b9d6f745d686c2649255bd14fe4e0b97a3477d383e719490e5ef66b27ae`

```dockerfile
```

-	Layers:
	-	`sha256:b44003cd1ea209090a063c5abfb4ee881849abba47e8711191b7637f86d8ee8b`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 94.9 KB (94856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f431de53d9b6c7e2cbc847af9daec064d061f8bd625615734012051336c495a`  
		Last Modified: Wed, 15 Apr 2026 22:23:37 GMT  
		Size: 20.5 KB (20472 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.23` - linux; ppc64le

```console
$ docker pull memcached@sha256:8182e35a9a404f0b522cb3c176d3dc4aade974e5556184c0a5a19e800721868a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6034321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30c6f532e81b50ea71c3520a80da0c8154b4cb14ebc17f87eb3a026862b47ed8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:41 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:17:43 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:20:21 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:20:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:20:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:20:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:20:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:20:22 GMT
USER memcache
# Wed, 15 Apr 2026 20:20:22 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:20:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee88d1c88fa46aa906a297c2919c9a085e74d04f20e4f827ca240a20f10ad34`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c574329cc1ebf156e2d89ab608bd58a3c0db550845c0ec394d265aa98fc5c4`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 126.3 KB (126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc2a28510bcba91734e7b38682847296011b63458db8a87a4bcecd180b8de7b5`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 2.1 MB (2075767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c524eb15ef0a41bf969efc93ef579db92dc59e8df57c9abfd099e7f6ff0756`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bde8ceae30a2a0890715bbc591167ee301c57d7f75023e80be460035187def`  
		Last Modified: Wed, 15 Apr 2026 20:20:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:4051408ef6c5bf4d4f37abf19c13f0298d8baa81770fcbfb588221e49e3bb834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ec3a4d49e6f325e484db43c9c9981f4eaa0223d9ae98282d95c3ee20c2089cb`

```dockerfile
```

-	Layers:
	-	`sha256:0e4e65db585f857844a67a831eb876dbb0a8a40d9269393d6c0fa83a2df995ae`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 94.3 KB (94308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50f58ec8aff3c96cc7b58e689122c27ee26121c598034cdc59ec95fd6423effe`  
		Last Modified: Wed, 15 Apr 2026 20:20:32 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.23` - linux; riscv64

```console
$ docker pull memcached@sha256:f3209d1ca2c4ce827614d16445231d96372944d218f18fd22850eec83874e5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5772332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e30170e0826b89d0ca59ffcae54b850ded07e6ae9451ecf1fd60f3ca8adcc725`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2026 00:00:48 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 16 Apr 2026 00:00:52 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 16 Apr 2026 00:14:21 GMT
ENV MEMCACHED_VERSION=1.6.41
# Thu, 16 Apr 2026 00:14:21 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Thu, 16 Apr 2026 00:14:21 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Thu, 16 Apr 2026 00:14:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 16 Apr 2026 00:14:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Apr 2026 00:14:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 16 Apr 2026 00:14:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Apr 2026 00:14:22 GMT
USER memcache
# Thu, 16 Apr 2026 00:14:22 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 16 Apr 2026 00:14:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62b143e34f5b89277e3a88ed4d722339d188a094d4bb534e222ca80e7741031`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bfff7c64f831ba03c491874cdf9a1c3f42bff72bb0e1951c63d8cf718854cff`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 108.9 KB (108903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69aef1050272a61cfbfd97c041d3776f96bdd03b102f2c3c54bbb0af2e1235a5`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 2.1 MB (2074414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ce340fb37f86db0d3aa774c23880b7c8322d2af8e3adc27a6ffa25d67c2122`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e40c6fb92d819994d38fae7accdffd583465eb6e645834b66f3ce9f0562f69`  
		Last Modified: Thu, 16 Apr 2026 00:14:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:2caae198d1efb7d4df14da45a3ff360a697982b544a61a3f907076b414983ea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1503bd38f4b30bc91be18dd93359e7376a9da1c7cb652ade64efd154064543fe`

```dockerfile
```

-	Layers:
	-	`sha256:e2d79fb634d76e28f055ab09953f59c371b93599e2b79f20f3d758f2c9520118`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 94.3 KB (94304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3614ad9b1715c3d6aa488496fca74d7143ea095d227f599407c933c62ec266aa`  
		Last Modified: Thu, 16 Apr 2026 00:14:54 GMT  
		Size: 20.6 KB (20604 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.23` - linux; s390x

```console
$ docker pull memcached@sha256:1da27660ae89a83aaf603e1affd51be573e5b8dac6c07ed592aee2a3a2b20581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5859702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13aa64df69a308e46b054bbd8e7a5d2f1e079005771f61748dae0d049889ba7f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:14:40 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 15 Apr 2026 20:14:41 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 15 Apr 2026 20:17:58 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 15 Apr 2026 20:17:58 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 15 Apr 2026 20:17:58 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 15 Apr 2026 20:17:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 15 Apr 2026 20:17:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:17:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 15 Apr 2026 20:17:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:17:58 GMT
USER memcache
# Wed, 15 Apr 2026 20:17:58 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 15 Apr 2026 20:17:58 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c42733e5f451590186b9b76c4b374ae5a84b657f7f1fd405647f5ba82c65bcd`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a14431ac88e8fe205b07f09b7e4843bb254de41cbc044725d6eaee3c2f822f`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 114.3 KB (114293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6377b7d98f32173cd47682aa73b32e4eba42781fa9224b9eb7a6f87367d37f94`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 2.0 MB (2017525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d022ae992296922747a4b69694b0185a0ce1f6cdece7f794e39e74dab92d250`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255cb3a435cbd623c1235d0429160faf72c244a6c1a613525df36f58a8c1f784`  
		Last Modified: Wed, 15 Apr 2026 20:18:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:531ee140f06db77d73b71bce7339abec3c6d976092bb80542bb337bb406acdbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b17d6f7e71efe3ee05ebcdb8ae90c28cf60db9ef069b0a98fe442c949740a6c`

```dockerfile
```

-	Layers:
	-	`sha256:820a080f49bf9e33948dbe5c13f6254f135d90bcb2b2277e3d2fd2430626c1a2`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 94.2 KB (94250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8ab82f4f240f46f9e34b74691925ab4af7f1cbb12ad3cb8639e0f317cf06653`  
		Last Modified: Wed, 15 Apr 2026 20:18:08 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:latest`

```console
$ docker pull memcached@sha256:277e0c4f249b118e95ab10e535bae2fa1af772271d9152f3468e58d59348db56
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
$ docker pull memcached@sha256:518f136cafc43439a777c20224d30b6fadc3433e3de9573f514dca10dd7e0082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32198630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ec7b3eba028951d3aeee1ef26a365c913edaf06de6c008653f175c0ff0078ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:21:37 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 22 Apr 2026 01:21:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:24:27 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 22 Apr 2026 01:24:27 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 22 Apr 2026 01:24:27 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 22 Apr 2026 01:24:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 22 Apr 2026 01:24:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:24:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:24:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:24:27 GMT
USER memcache
# Wed, 22 Apr 2026 01:24:27 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 Apr 2026 01:24:27 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53e27a8dc2608bcd39496d6e1a0a021aa8933953409444f778d810ec220ab89`  
		Last Modified: Wed, 22 Apr 2026 01:24:33 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d02c07f7ffb4ea4d70b3af1ed59da72e778c143718ba2a7bcb8cd6d12afd95b`  
		Last Modified: Wed, 22 Apr 2026 01:24:33 GMT  
		Size: 136.7 KB (136658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b1a619145ef14a0e4599b98a19dbdc4fc96cfdf359ecf816454cd80ccf2dd2`  
		Last Modified: Wed, 22 Apr 2026 01:24:34 GMT  
		Size: 2.3 MB (2280287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7716efee154a639ac02ada0d1638837bb72c3fc33ecac40f78ffb91daf9dfc5`  
		Last Modified: Wed, 22 Apr 2026 01:24:34 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712f24abcdc2a432d57253a569a16eddd36ff1f8a4ace323467cdb642eae2850`  
		Last Modified: Wed, 22 Apr 2026 01:24:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:f32546667bf4926fd4e7c91aa55a833e8636777f2aa68437cb2bc7a5330e2307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3700c2c8b8182ac20db287282cdafbde42f55966784e109b48a9e5c2ba4d7492`

```dockerfile
```

-	Layers:
	-	`sha256:a3fe3f55746c35c0a798536b5abfc78349217684ca67ba43649a1c86d2a6ebe3`  
		Last Modified: Wed, 22 Apr 2026 01:24:33 GMT  
		Size: 2.0 MB (2008326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0b151a6f180676864b1e8721dddbaf0c105e743520356d58f7df86572a295fa`  
		Last Modified: Wed, 22 Apr 2026 01:24:33 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm variant v5

```console
$ docker pull memcached@sha256:4b91aeabb9b5d253e27cc0e6f6fa6cc82780c4d686f484c9ed1057a1dd429ba2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30305389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e62e4552c0bfc9dd8f4797df2c1386943df5780d342654ed3050e75668231e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:17:31 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 22 Apr 2026 01:17:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:20:57 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 22 Apr 2026 01:20:57 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 22 Apr 2026 01:20:57 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 22 Apr 2026 01:20:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 22 Apr 2026 01:20:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:20:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:20:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:20:57 GMT
USER memcache
# Wed, 22 Apr 2026 01:20:57 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 Apr 2026 01:20:57 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6496d93bca0663211b9252da346044ecb734ee5b3ecaae5b1fbd230753faee2f`  
		Last Modified: Wed, 22 Apr 2026 00:15:59 GMT  
		Size: 27.9 MB (27948180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64cdc01a23d15e84ef2ee2165c1a90970fb54d98f29377fa63fbd82988cdcc40`  
		Last Modified: Wed, 22 Apr 2026 01:21:03 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:303fc6e2ad4e0da497f7e238e61ec9e1fbde60909262de4a50e05c4db2191602`  
		Last Modified: Wed, 22 Apr 2026 01:21:03 GMT  
		Size: 144.2 KB (144163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c438ec3169ba426bc8374ca37b4f159272d50b60173c35c396f8fbf2208b8806`  
		Last Modified: Wed, 22 Apr 2026 01:21:03 GMT  
		Size: 2.2 MB (2211533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b5512f6aab6e3147798ce406f1035f68f18c2dd046b5fdd6344a17ace7fb31`  
		Last Modified: Wed, 22 Apr 2026 01:21:03 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a320e8acb7760a30eb688cd929fda03bf41ba23a307e06071106c3c0415d03`  
		Last Modified: Wed, 22 Apr 2026 01:21:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:4faa0397c26f0f4a312a28578db40b0f95f89c09769520c7cc09900886412dd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af54d9e6dbb4f86d5a79e417071faea8dd939b7758f640ce360a49c55069e2eb`

```dockerfile
```

-	Layers:
	-	`sha256:1850a912cc062cca1f70a2b76861d54c0ad06921d2a4960a7c483b5f8820eaa1`  
		Last Modified: Wed, 22 Apr 2026 01:21:03 GMT  
		Size: 2.0 MB (2011329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02fdad23f354f6597bfec3258d6bbee5142bcce9e1faaa7de87f9859bf8c6d14`  
		Last Modified: Wed, 22 Apr 2026 01:21:03 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm variant v7

```console
$ docker pull memcached@sha256:4d262b60fea5a97e91a6c1827ab7209a344c47616388ada79b27e4e69eea9d38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28516774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02f2f7426f06caeeb218b724a947fa35544b0749bacf781227878e40cb98d08f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:18:06 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 22 Apr 2026 01:18:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:21:19 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 22 Apr 2026 01:21:19 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 22 Apr 2026 01:21:19 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 22 Apr 2026 01:21:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 22 Apr 2026 01:21:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:21:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:21:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:21:19 GMT
USER memcache
# Wed, 22 Apr 2026 01:21:19 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 Apr 2026 01:21:19 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9e541e5bfbbe69b7bbe01cd2f1abf8560e2e43bf76eb96b2e88a3df29020834b`  
		Last Modified: Wed, 22 Apr 2026 00:17:02 GMT  
		Size: 26.2 MB (26214838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0867e20c7ab47539b3f27abc4c7f4bf41d367127d9ffbd30a531ab387a69e2e`  
		Last Modified: Wed, 22 Apr 2026 01:21:25 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34eedf23d5ae4af59fe6ecfd854e48545ede507ce44d930cea5c11b652b31f4`  
		Last Modified: Wed, 22 Apr 2026 01:21:25 GMT  
		Size: 135.4 KB (135382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fff54fd1447de9c8b377640a2720588785769320b1a65d59a1da8e9690e6f9`  
		Last Modified: Wed, 22 Apr 2026 01:21:25 GMT  
		Size: 2.2 MB (2165043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac214a1bada6a999cda6b6b021b8ef5ba954108062e3ee4df0161a500fc566f`  
		Last Modified: Wed, 22 Apr 2026 01:21:25 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0431aacefa9d6f210c7c4778e75df5a21c196127779acc2da1bd7b32088f47dc`  
		Last Modified: Wed, 22 Apr 2026 01:21:26 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:e4f840cb65bd892b2aafc305cb008de10d4d41475876ef9c9bbf51831f9cd7e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:987452d71cfba90bac820fca09f2954a061813125a8832038df5c062224577c5`

```dockerfile
```

-	Layers:
	-	`sha256:f5793a9489c1e1010726124554d7404a19b2675ce8596a38169b160edc81d045`  
		Last Modified: Wed, 22 Apr 2026 01:21:25 GMT  
		Size: 2.0 MB (2009786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef3c23077c5adc1a06a0e1f66d0ec1e57032a5b35685c53064098e236a62c5a1`  
		Last Modified: Wed, 22 Apr 2026 01:21:25 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:52e2a52a542b0fff64533e7271ce3af9825a80a1126998cf6070b0ec4c0030b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32560736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c3fcfefa704f0162e85ab03d515502e07a6ff91ec994dc4b6c956cc2ce80990`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:22:08 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 22 Apr 2026 01:22:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:25:10 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 22 Apr 2026 01:25:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 22 Apr 2026 01:25:10 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 22 Apr 2026 01:25:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 22 Apr 2026 01:25:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:25:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:25:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:25:10 GMT
USER memcache
# Wed, 22 Apr 2026 01:25:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 Apr 2026 01:25:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebea5231ebe63bff9044a4ee7713dac1b62fc15d85ee920f04eae4010a67b668`  
		Last Modified: Wed, 22 Apr 2026 01:25:16 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5921030f644563277c2af1be27b21dfded0e01763210710efac613f07dc74c`  
		Last Modified: Wed, 22 Apr 2026 01:25:16 GMT  
		Size: 153.5 KB (153515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1ef7f1deafd8e81fec98af35ef4fe12c2436c1eddb6bb87377b83f524f7d6f`  
		Last Modified: Wed, 22 Apr 2026 01:25:16 GMT  
		Size: 2.3 MB (2262106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd4f58ffc6f10cea1171fbb552aff0b93a04aba0ca6815cd9ad66ab3a49f8419`  
		Last Modified: Wed, 22 Apr 2026 01:25:16 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace7ea462603345a875235135df0b8dd036890eacdb25150c1a8089604e3ca1f`  
		Last Modified: Wed, 22 Apr 2026 01:25:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:63aba0d160ad2159dd41a074d79446fc4ba2e745c7e5a10a41dbd1d5c2abc86d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b67f2365f86c60d496eb140fde16a0d6fbf89ae6a83d200c6a3971e32eca706b`

```dockerfile
```

-	Layers:
	-	`sha256:e87d247df404b9fe7e19667c95311e8109ea54acdcca2f52ceba73b7099d144e`  
		Last Modified: Wed, 22 Apr 2026 01:25:16 GMT  
		Size: 2.0 MB (2008642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5290960be9e7480bf28bf59599ba02b7792ea80b3309570c3b3a24465ad7d58`  
		Last Modified: Wed, 22 Apr 2026 01:25:16 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; 386

```console
$ docker pull memcached@sha256:0b8f07a6f169bfe4cc362cbabca8c92d5140665660c615383f2755c40c0036f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33670125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd6a79877127262a308ef5f3bd216749c6f0b1fc43971b56c533d4e47f5c6de2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:17:33 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 22 Apr 2026 01:17:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:20:28 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 22 Apr 2026 01:20:28 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 22 Apr 2026 01:20:28 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 22 Apr 2026 01:20:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 22 Apr 2026 01:20:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:20:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:20:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:20:28 GMT
USER memcache
# Wed, 22 Apr 2026 01:20:28 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 Apr 2026 01:20:28 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:dacd7cda306bf5bd7a2030f9b0c2e9d71fda44ea58493a33450d210b74a8ec75`  
		Last Modified: Wed, 22 Apr 2026 00:17:04 GMT  
		Size: 31.3 MB (31296327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a0c9fe363e7e198726a5e39cf627131e43cd59d319a350f978180f6f449b8a`  
		Last Modified: Wed, 22 Apr 2026 01:20:34 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dff2976b24139841065357d1f81c8cf6d9b45ee35e2947f1345e86493b2f5e67`  
		Last Modified: Wed, 22 Apr 2026 01:20:34 GMT  
		Size: 147.5 KB (147529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8b8718f120acc0033835790e0bd541e38b843c6b260688b8fde3c94eadd5911`  
		Last Modified: Wed, 22 Apr 2026 01:20:34 GMT  
		Size: 2.2 MB (2224758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f70ea447cee314191f67e0ce5ccc23703730c89810e26bfa3f96f81964849dc`  
		Last Modified: Wed, 22 Apr 2026 01:20:34 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:789bc1b0beaaf9809e3cab832a0b6b29f50aec3b18f7a7cdf04e343d3ee800a3`  
		Last Modified: Wed, 22 Apr 2026 01:20:35 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:45cfea0c565e5e6c79f4a36cf4ec611ccc7e910c481110b37be04eca3276511b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d33423fad9c4c2f3b1af3eb87b8af48d7cfc9e00d70e6c33937d7d215fb94c5`

```dockerfile
```

-	Layers:
	-	`sha256:2656e01c20323e582a0ba03c06d82008eb35ae9850f7d6c7f73c0e5ae040805b`  
		Last Modified: Wed, 22 Apr 2026 01:20:34 GMT  
		Size: 2.0 MB (2005483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d267990174d3038591d6a8ffe07af06d961bb5c68b86a9cdac459f5a0996ddbe`  
		Last Modified: Wed, 22 Apr 2026 01:20:34 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; ppc64le

```console
$ docker pull memcached@sha256:3df945008f026e1a7782fc67d0107a07c9103d9d50dd7ae605082ea97fb64ff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36164269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7eb2db1cbb0c7ddc2688ee498498fb5122ee78ab349b636a43585b1beb30da9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:35:49 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 22 Apr 2026 01:35:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:39:22 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 22 Apr 2026 01:39:22 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 22 Apr 2026 01:39:22 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 22 Apr 2026 01:39:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 22 Apr 2026 01:39:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:39:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:39:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:39:23 GMT
USER memcache
# Wed, 22 Apr 2026 01:39:23 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 Apr 2026 01:39:23 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b5fd051d0fcd0789e7358cba300f83befdba943416041497be86050e282a6d02`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 33.6 MB (33598032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e271c91c5c30b04dee49fb4c9ab2f9863d13146641f1b8681b59467d0f8ab5`  
		Last Modified: Wed, 22 Apr 2026 01:39:42 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb7fa3c8c45f87e36929f71acaead9bcb07985c205ea0aa6fd83aca31691d78`  
		Last Modified: Wed, 22 Apr 2026 01:39:42 GMT  
		Size: 170.4 KB (170378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f09610f9abffbf6411865ebc07ee20de6c14b2250467c4682f423dddc0ab82`  
		Last Modified: Wed, 22 Apr 2026 01:39:42 GMT  
		Size: 2.4 MB (2394347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a0fb856cc435334489ebeec58afd76f4e676c8bae4b3688daefedfbc7f7c1a8`  
		Last Modified: Wed, 22 Apr 2026 01:39:42 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea36b259fc26e36b99ded4a3aa0ca190c1117ecd424f26565f8474b55964d787`  
		Last Modified: Wed, 22 Apr 2026 01:39:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:c619fe6b2206166796157b814c0d60ca38e29a646b71cd6f5635e2f507cf70d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49e66f35bf963d54f332469bbdef0ca608c651311f5af0e923aca630f4429ae9`

```dockerfile
```

-	Layers:
	-	`sha256:f870fab207e6594315e4d18f50f3ebf834ebc298b6ec128104607668ae939995`  
		Last Modified: Wed, 22 Apr 2026 01:39:42 GMT  
		Size: 2.0 MB (2011927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bf20b8b72f84425e9121a35ea191dab3cf17562679390195740f260304727d7`  
		Last Modified: Wed, 22 Apr 2026 01:39:42 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; riscv64

```console
$ docker pull memcached@sha256:5554043a87027cff145bdb04810a9f8a067c72479937ce0328af056a5c3efe8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30623256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad08d83e675d61f6e230bee3e1d5d5e4b4e8d0b1b3656b71812168b7db5e08e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 08:28:54 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 22 Apr 2026 08:29:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 08:55:11 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 22 Apr 2026 08:55:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 22 Apr 2026 08:55:11 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 22 Apr 2026 08:55:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 22 Apr 2026 08:55:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 08:55:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 08:55:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 08:55:12 GMT
USER memcache
# Wed, 22 Apr 2026 08:55:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 Apr 2026 08:55:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8aa73197c6983c411cf26b41c64a557cfc81f9b4e6d897ff2829a66eac03b37`  
		Last Modified: Wed, 22 Apr 2026 08:55:56 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee379d85ef42145b3f09328c98634e8cd3320230281217ad58867c6982e1d8c`  
		Last Modified: Wed, 22 Apr 2026 08:55:57 GMT  
		Size: 133.1 KB (133094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:310a92cbf1cb95664c58022062af028a81e69f127cd8d9ee044bf7d5087db961`  
		Last Modified: Wed, 22 Apr 2026 08:55:57 GMT  
		Size: 2.2 MB (2208455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336575624802c397f4947f3ddfc2737281bfe2ba8cd714be646b72152c1ec1d0`  
		Last Modified: Wed, 22 Apr 2026 08:55:56 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e926175ab529d298755a0e0507accca74feec6c90ea4495edeaafb07954ad57d`  
		Last Modified: Wed, 22 Apr 2026 08:55:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:9b8b4751f5823830cf382050f0174dd5ade6dc0650b2a3134803b886b2652dba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bc1698424d742c630d5a555fa2c70be3195da5b1a2cd148a331c7aa9fb94b6f`

```dockerfile
```

-	Layers:
	-	`sha256:18aa82332065ff68528148bb97bd5681424d4c57e9e5e331b8908b44023570a9`  
		Last Modified: Wed, 22 Apr 2026 08:55:57 GMT  
		Size: 2.0 MB (2002290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edeefd058e4dbdf6c3026618be5f5184cd3d2c22f14746d890cd45a42004dc8f`  
		Last Modified: Wed, 22 Apr 2026 08:55:57 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; s390x

```console
$ docker pull memcached@sha256:e0fadaa0ad7c323c4f8ead5d8e1ebb9566adc59b25cbc280f40bef816f9d62eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32280559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5d7f2d629511f566dd7c4b3a944adb9989b05bb41dbd3e3881734bc1c1079c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:19:00 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 22 Apr 2026 01:19:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:22:27 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 22 Apr 2026 01:22:27 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 22 Apr 2026 01:22:27 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 22 Apr 2026 01:22:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 22 Apr 2026 01:22:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:22:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:22:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:22:27 GMT
USER memcache
# Wed, 22 Apr 2026 01:22:27 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 Apr 2026 01:22:27 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:71574deb335f1e823f938f4a215de00a90d63866898f1f354a0b15e8b9c30577`  
		Last Modified: Wed, 22 Apr 2026 00:17:08 GMT  
		Size: 29.8 MB (29840300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b460058bd06ca18e629070cadcc158edef16e034340796f661d4fab362ee94`  
		Last Modified: Wed, 22 Apr 2026 01:22:38 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5386c57fa90d49931296cf79f5e8d2ae18d07b9bcffe5eee8354033fee4b673`  
		Last Modified: Wed, 22 Apr 2026 01:22:38 GMT  
		Size: 140.5 KB (140521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd8308c0fc0224d29acef5aadae977dfea2e1ba7c9be0e207ee89c84a4f6417`  
		Last Modified: Wed, 22 Apr 2026 01:22:38 GMT  
		Size: 2.3 MB (2298228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fda405f0b2226447c88ba0d395ee00616ec775cecba66d9a980d4aac7b44fb49`  
		Last Modified: Wed, 22 Apr 2026 01:22:38 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fcaa079ef0e24aab0065df6b15e28d19a0807e2c9cdc639bbc63923135e6daa`  
		Last Modified: Wed, 22 Apr 2026 01:22:39 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:7d2e45f2ecd9448a99f98a077da16fb59c37827c2acbac9e99dea8f79d753165
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54358ef5a62ded9fafc9e908e79d81e5d01102cd4f2082017f54d92232acb7c4`

```dockerfile
```

-	Layers:
	-	`sha256:eb9c1105cc4bf8d4cf2089f7a2a43afe0a113388e7f5a4af9db1f44f9f0fbe11`  
		Last Modified: Wed, 22 Apr 2026 01:22:38 GMT  
		Size: 2.0 MB (2009763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af1c4a20085e6a6f3d2b2fcb2ce9c10456d057c6905b84fe6ad6d99ba351a872`  
		Last Modified: Wed, 22 Apr 2026 01:22:38 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:trixie`

```console
$ docker pull memcached@sha256:277e0c4f249b118e95ab10e535bae2fa1af772271d9152f3468e58d59348db56
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
$ docker pull memcached@sha256:518f136cafc43439a777c20224d30b6fadc3433e3de9573f514dca10dd7e0082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32198630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ec7b3eba028951d3aeee1ef26a365c913edaf06de6c008653f175c0ff0078ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:21:37 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 22 Apr 2026 01:21:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:24:27 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 22 Apr 2026 01:24:27 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 22 Apr 2026 01:24:27 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 22 Apr 2026 01:24:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 22 Apr 2026 01:24:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:24:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:24:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:24:27 GMT
USER memcache
# Wed, 22 Apr 2026 01:24:27 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 Apr 2026 01:24:27 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53e27a8dc2608bcd39496d6e1a0a021aa8933953409444f778d810ec220ab89`  
		Last Modified: Wed, 22 Apr 2026 01:24:33 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d02c07f7ffb4ea4d70b3af1ed59da72e778c143718ba2a7bcb8cd6d12afd95b`  
		Last Modified: Wed, 22 Apr 2026 01:24:33 GMT  
		Size: 136.7 KB (136658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b1a619145ef14a0e4599b98a19dbdc4fc96cfdf359ecf816454cd80ccf2dd2`  
		Last Modified: Wed, 22 Apr 2026 01:24:34 GMT  
		Size: 2.3 MB (2280287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7716efee154a639ac02ada0d1638837bb72c3fc33ecac40f78ffb91daf9dfc5`  
		Last Modified: Wed, 22 Apr 2026 01:24:34 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712f24abcdc2a432d57253a569a16eddd36ff1f8a4ace323467cdb642eae2850`  
		Last Modified: Wed, 22 Apr 2026 01:24:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:f32546667bf4926fd4e7c91aa55a833e8636777f2aa68437cb2bc7a5330e2307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3700c2c8b8182ac20db287282cdafbde42f55966784e109b48a9e5c2ba4d7492`

```dockerfile
```

-	Layers:
	-	`sha256:a3fe3f55746c35c0a798536b5abfc78349217684ca67ba43649a1c86d2a6ebe3`  
		Last Modified: Wed, 22 Apr 2026 01:24:33 GMT  
		Size: 2.0 MB (2008326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0b151a6f180676864b1e8721dddbaf0c105e743520356d58f7df86572a295fa`  
		Last Modified: Wed, 22 Apr 2026 01:24:33 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; arm variant v5

```console
$ docker pull memcached@sha256:4b91aeabb9b5d253e27cc0e6f6fa6cc82780c4d686f484c9ed1057a1dd429ba2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30305389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e62e4552c0bfc9dd8f4797df2c1386943df5780d342654ed3050e75668231e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:17:31 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 22 Apr 2026 01:17:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:20:57 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 22 Apr 2026 01:20:57 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 22 Apr 2026 01:20:57 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 22 Apr 2026 01:20:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 22 Apr 2026 01:20:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:20:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:20:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:20:57 GMT
USER memcache
# Wed, 22 Apr 2026 01:20:57 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 Apr 2026 01:20:57 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6496d93bca0663211b9252da346044ecb734ee5b3ecaae5b1fbd230753faee2f`  
		Last Modified: Wed, 22 Apr 2026 00:15:59 GMT  
		Size: 27.9 MB (27948180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64cdc01a23d15e84ef2ee2165c1a90970fb54d98f29377fa63fbd82988cdcc40`  
		Last Modified: Wed, 22 Apr 2026 01:21:03 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:303fc6e2ad4e0da497f7e238e61ec9e1fbde60909262de4a50e05c4db2191602`  
		Last Modified: Wed, 22 Apr 2026 01:21:03 GMT  
		Size: 144.2 KB (144163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c438ec3169ba426bc8374ca37b4f159272d50b60173c35c396f8fbf2208b8806`  
		Last Modified: Wed, 22 Apr 2026 01:21:03 GMT  
		Size: 2.2 MB (2211533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b5512f6aab6e3147798ce406f1035f68f18c2dd046b5fdd6344a17ace7fb31`  
		Last Modified: Wed, 22 Apr 2026 01:21:03 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a320e8acb7760a30eb688cd929fda03bf41ba23a307e06071106c3c0415d03`  
		Last Modified: Wed, 22 Apr 2026 01:21:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:4faa0397c26f0f4a312a28578db40b0f95f89c09769520c7cc09900886412dd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af54d9e6dbb4f86d5a79e417071faea8dd939b7758f640ce360a49c55069e2eb`

```dockerfile
```

-	Layers:
	-	`sha256:1850a912cc062cca1f70a2b76861d54c0ad06921d2a4960a7c483b5f8820eaa1`  
		Last Modified: Wed, 22 Apr 2026 01:21:03 GMT  
		Size: 2.0 MB (2011329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02fdad23f354f6597bfec3258d6bbee5142bcce9e1faaa7de87f9859bf8c6d14`  
		Last Modified: Wed, 22 Apr 2026 01:21:03 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; arm variant v7

```console
$ docker pull memcached@sha256:4d262b60fea5a97e91a6c1827ab7209a344c47616388ada79b27e4e69eea9d38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28516774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02f2f7426f06caeeb218b724a947fa35544b0749bacf781227878e40cb98d08f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:18:06 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 22 Apr 2026 01:18:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:21:19 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 22 Apr 2026 01:21:19 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 22 Apr 2026 01:21:19 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 22 Apr 2026 01:21:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 22 Apr 2026 01:21:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:21:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:21:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:21:19 GMT
USER memcache
# Wed, 22 Apr 2026 01:21:19 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 Apr 2026 01:21:19 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9e541e5bfbbe69b7bbe01cd2f1abf8560e2e43bf76eb96b2e88a3df29020834b`  
		Last Modified: Wed, 22 Apr 2026 00:17:02 GMT  
		Size: 26.2 MB (26214838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0867e20c7ab47539b3f27abc4c7f4bf41d367127d9ffbd30a531ab387a69e2e`  
		Last Modified: Wed, 22 Apr 2026 01:21:25 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34eedf23d5ae4af59fe6ecfd854e48545ede507ce44d930cea5c11b652b31f4`  
		Last Modified: Wed, 22 Apr 2026 01:21:25 GMT  
		Size: 135.4 KB (135382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fff54fd1447de9c8b377640a2720588785769320b1a65d59a1da8e9690e6f9`  
		Last Modified: Wed, 22 Apr 2026 01:21:25 GMT  
		Size: 2.2 MB (2165043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac214a1bada6a999cda6b6b021b8ef5ba954108062e3ee4df0161a500fc566f`  
		Last Modified: Wed, 22 Apr 2026 01:21:25 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0431aacefa9d6f210c7c4778e75df5a21c196127779acc2da1bd7b32088f47dc`  
		Last Modified: Wed, 22 Apr 2026 01:21:26 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:e4f840cb65bd892b2aafc305cb008de10d4d41475876ef9c9bbf51831f9cd7e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:987452d71cfba90bac820fca09f2954a061813125a8832038df5c062224577c5`

```dockerfile
```

-	Layers:
	-	`sha256:f5793a9489c1e1010726124554d7404a19b2675ce8596a38169b160edc81d045`  
		Last Modified: Wed, 22 Apr 2026 01:21:25 GMT  
		Size: 2.0 MB (2009786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef3c23077c5adc1a06a0e1f66d0ec1e57032a5b35685c53064098e236a62c5a1`  
		Last Modified: Wed, 22 Apr 2026 01:21:25 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:52e2a52a542b0fff64533e7271ce3af9825a80a1126998cf6070b0ec4c0030b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32560736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c3fcfefa704f0162e85ab03d515502e07a6ff91ec994dc4b6c956cc2ce80990`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:22:08 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 22 Apr 2026 01:22:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:25:10 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 22 Apr 2026 01:25:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 22 Apr 2026 01:25:10 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 22 Apr 2026 01:25:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 22 Apr 2026 01:25:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:25:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:25:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:25:10 GMT
USER memcache
# Wed, 22 Apr 2026 01:25:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 Apr 2026 01:25:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebea5231ebe63bff9044a4ee7713dac1b62fc15d85ee920f04eae4010a67b668`  
		Last Modified: Wed, 22 Apr 2026 01:25:16 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5921030f644563277c2af1be27b21dfded0e01763210710efac613f07dc74c`  
		Last Modified: Wed, 22 Apr 2026 01:25:16 GMT  
		Size: 153.5 KB (153515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1ef7f1deafd8e81fec98af35ef4fe12c2436c1eddb6bb87377b83f524f7d6f`  
		Last Modified: Wed, 22 Apr 2026 01:25:16 GMT  
		Size: 2.3 MB (2262106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd4f58ffc6f10cea1171fbb552aff0b93a04aba0ca6815cd9ad66ab3a49f8419`  
		Last Modified: Wed, 22 Apr 2026 01:25:16 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace7ea462603345a875235135df0b8dd036890eacdb25150c1a8089604e3ca1f`  
		Last Modified: Wed, 22 Apr 2026 01:25:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:63aba0d160ad2159dd41a074d79446fc4ba2e745c7e5a10a41dbd1d5c2abc86d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b67f2365f86c60d496eb140fde16a0d6fbf89ae6a83d200c6a3971e32eca706b`

```dockerfile
```

-	Layers:
	-	`sha256:e87d247df404b9fe7e19667c95311e8109ea54acdcca2f52ceba73b7099d144e`  
		Last Modified: Wed, 22 Apr 2026 01:25:16 GMT  
		Size: 2.0 MB (2008642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5290960be9e7480bf28bf59599ba02b7792ea80b3309570c3b3a24465ad7d58`  
		Last Modified: Wed, 22 Apr 2026 01:25:16 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; 386

```console
$ docker pull memcached@sha256:0b8f07a6f169bfe4cc362cbabca8c92d5140665660c615383f2755c40c0036f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33670125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd6a79877127262a308ef5f3bd216749c6f0b1fc43971b56c533d4e47f5c6de2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:17:33 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 22 Apr 2026 01:17:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:20:28 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 22 Apr 2026 01:20:28 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 22 Apr 2026 01:20:28 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 22 Apr 2026 01:20:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 22 Apr 2026 01:20:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:20:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:20:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:20:28 GMT
USER memcache
# Wed, 22 Apr 2026 01:20:28 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 Apr 2026 01:20:28 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:dacd7cda306bf5bd7a2030f9b0c2e9d71fda44ea58493a33450d210b74a8ec75`  
		Last Modified: Wed, 22 Apr 2026 00:17:04 GMT  
		Size: 31.3 MB (31296327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a0c9fe363e7e198726a5e39cf627131e43cd59d319a350f978180f6f449b8a`  
		Last Modified: Wed, 22 Apr 2026 01:20:34 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dff2976b24139841065357d1f81c8cf6d9b45ee35e2947f1345e86493b2f5e67`  
		Last Modified: Wed, 22 Apr 2026 01:20:34 GMT  
		Size: 147.5 KB (147529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8b8718f120acc0033835790e0bd541e38b843c6b260688b8fde3c94eadd5911`  
		Last Modified: Wed, 22 Apr 2026 01:20:34 GMT  
		Size: 2.2 MB (2224758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f70ea447cee314191f67e0ce5ccc23703730c89810e26bfa3f96f81964849dc`  
		Last Modified: Wed, 22 Apr 2026 01:20:34 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:789bc1b0beaaf9809e3cab832a0b6b29f50aec3b18f7a7cdf04e343d3ee800a3`  
		Last Modified: Wed, 22 Apr 2026 01:20:35 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:45cfea0c565e5e6c79f4a36cf4ec611ccc7e910c481110b37be04eca3276511b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d33423fad9c4c2f3b1af3eb87b8af48d7cfc9e00d70e6c33937d7d215fb94c5`

```dockerfile
```

-	Layers:
	-	`sha256:2656e01c20323e582a0ba03c06d82008eb35ae9850f7d6c7f73c0e5ae040805b`  
		Last Modified: Wed, 22 Apr 2026 01:20:34 GMT  
		Size: 2.0 MB (2005483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d267990174d3038591d6a8ffe07af06d961bb5c68b86a9cdac459f5a0996ddbe`  
		Last Modified: Wed, 22 Apr 2026 01:20:34 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; ppc64le

```console
$ docker pull memcached@sha256:3df945008f026e1a7782fc67d0107a07c9103d9d50dd7ae605082ea97fb64ff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36164269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7eb2db1cbb0c7ddc2688ee498498fb5122ee78ab349b636a43585b1beb30da9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:35:49 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 22 Apr 2026 01:35:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:39:22 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 22 Apr 2026 01:39:22 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 22 Apr 2026 01:39:22 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 22 Apr 2026 01:39:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 22 Apr 2026 01:39:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:39:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:39:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:39:23 GMT
USER memcache
# Wed, 22 Apr 2026 01:39:23 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 Apr 2026 01:39:23 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b5fd051d0fcd0789e7358cba300f83befdba943416041497be86050e282a6d02`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 33.6 MB (33598032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e271c91c5c30b04dee49fb4c9ab2f9863d13146641f1b8681b59467d0f8ab5`  
		Last Modified: Wed, 22 Apr 2026 01:39:42 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb7fa3c8c45f87e36929f71acaead9bcb07985c205ea0aa6fd83aca31691d78`  
		Last Modified: Wed, 22 Apr 2026 01:39:42 GMT  
		Size: 170.4 KB (170378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f09610f9abffbf6411865ebc07ee20de6c14b2250467c4682f423dddc0ab82`  
		Last Modified: Wed, 22 Apr 2026 01:39:42 GMT  
		Size: 2.4 MB (2394347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a0fb856cc435334489ebeec58afd76f4e676c8bae4b3688daefedfbc7f7c1a8`  
		Last Modified: Wed, 22 Apr 2026 01:39:42 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea36b259fc26e36b99ded4a3aa0ca190c1117ecd424f26565f8474b55964d787`  
		Last Modified: Wed, 22 Apr 2026 01:39:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:c619fe6b2206166796157b814c0d60ca38e29a646b71cd6f5635e2f507cf70d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49e66f35bf963d54f332469bbdef0ca608c651311f5af0e923aca630f4429ae9`

```dockerfile
```

-	Layers:
	-	`sha256:f870fab207e6594315e4d18f50f3ebf834ebc298b6ec128104607668ae939995`  
		Last Modified: Wed, 22 Apr 2026 01:39:42 GMT  
		Size: 2.0 MB (2011927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bf20b8b72f84425e9121a35ea191dab3cf17562679390195740f260304727d7`  
		Last Modified: Wed, 22 Apr 2026 01:39:42 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; riscv64

```console
$ docker pull memcached@sha256:5554043a87027cff145bdb04810a9f8a067c72479937ce0328af056a5c3efe8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30623256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad08d83e675d61f6e230bee3e1d5d5e4b4e8d0b1b3656b71812168b7db5e08e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 08:28:54 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 22 Apr 2026 08:29:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 08:55:11 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 22 Apr 2026 08:55:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 22 Apr 2026 08:55:11 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 22 Apr 2026 08:55:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 22 Apr 2026 08:55:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 08:55:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 08:55:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 08:55:12 GMT
USER memcache
# Wed, 22 Apr 2026 08:55:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 Apr 2026 08:55:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8aa73197c6983c411cf26b41c64a557cfc81f9b4e6d897ff2829a66eac03b37`  
		Last Modified: Wed, 22 Apr 2026 08:55:56 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee379d85ef42145b3f09328c98634e8cd3320230281217ad58867c6982e1d8c`  
		Last Modified: Wed, 22 Apr 2026 08:55:57 GMT  
		Size: 133.1 KB (133094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:310a92cbf1cb95664c58022062af028a81e69f127cd8d9ee044bf7d5087db961`  
		Last Modified: Wed, 22 Apr 2026 08:55:57 GMT  
		Size: 2.2 MB (2208455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336575624802c397f4947f3ddfc2737281bfe2ba8cd714be646b72152c1ec1d0`  
		Last Modified: Wed, 22 Apr 2026 08:55:56 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e926175ab529d298755a0e0507accca74feec6c90ea4495edeaafb07954ad57d`  
		Last Modified: Wed, 22 Apr 2026 08:55:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:9b8b4751f5823830cf382050f0174dd5ade6dc0650b2a3134803b886b2652dba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bc1698424d742c630d5a555fa2c70be3195da5b1a2cd148a331c7aa9fb94b6f`

```dockerfile
```

-	Layers:
	-	`sha256:18aa82332065ff68528148bb97bd5681424d4c57e9e5e331b8908b44023570a9`  
		Last Modified: Wed, 22 Apr 2026 08:55:57 GMT  
		Size: 2.0 MB (2002290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edeefd058e4dbdf6c3026618be5f5184cd3d2c22f14746d890cd45a42004dc8f`  
		Last Modified: Wed, 22 Apr 2026 08:55:57 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; s390x

```console
$ docker pull memcached@sha256:e0fadaa0ad7c323c4f8ead5d8e1ebb9566adc59b25cbc280f40bef816f9d62eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32280559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5d7f2d629511f566dd7c4b3a944adb9989b05bb41dbd3e3881734bc1c1079c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:19:00 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 22 Apr 2026 01:19:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:22:27 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 22 Apr 2026 01:22:27 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 22 Apr 2026 01:22:27 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 22 Apr 2026 01:22:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 22 Apr 2026 01:22:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:22:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:22:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:22:27 GMT
USER memcache
# Wed, 22 Apr 2026 01:22:27 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 Apr 2026 01:22:27 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:71574deb335f1e823f938f4a215de00a90d63866898f1f354a0b15e8b9c30577`  
		Last Modified: Wed, 22 Apr 2026 00:17:08 GMT  
		Size: 29.8 MB (29840300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b460058bd06ca18e629070cadcc158edef16e034340796f661d4fab362ee94`  
		Last Modified: Wed, 22 Apr 2026 01:22:38 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5386c57fa90d49931296cf79f5e8d2ae18d07b9bcffe5eee8354033fee4b673`  
		Last Modified: Wed, 22 Apr 2026 01:22:38 GMT  
		Size: 140.5 KB (140521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd8308c0fc0224d29acef5aadae977dfea2e1ba7c9be0e207ee89c84a4f6417`  
		Last Modified: Wed, 22 Apr 2026 01:22:38 GMT  
		Size: 2.3 MB (2298228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fda405f0b2226447c88ba0d395ee00616ec775cecba66d9a980d4aac7b44fb49`  
		Last Modified: Wed, 22 Apr 2026 01:22:38 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fcaa079ef0e24aab0065df6b15e28d19a0807e2c9cdc639bbc63923135e6daa`  
		Last Modified: Wed, 22 Apr 2026 01:22:39 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:7d2e45f2ecd9448a99f98a077da16fb59c37827c2acbac9e99dea8f79d753165
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54358ef5a62ded9fafc9e908e79d81e5d01102cd4f2082017f54d92232acb7c4`

```dockerfile
```

-	Layers:
	-	`sha256:eb9c1105cc4bf8d4cf2089f7a2a43afe0a113388e7f5a4af9db1f44f9f0fbe11`  
		Last Modified: Wed, 22 Apr 2026 01:22:38 GMT  
		Size: 2.0 MB (2009763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af1c4a20085e6a6f3d2b2fcb2ce9c10456d057c6905b84fe6ad6d99ba351a872`  
		Last Modified: Wed, 22 Apr 2026 01:22:38 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json
