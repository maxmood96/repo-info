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
$ docker pull memcached@sha256:302493fd5e802f3bad0b33d2dc1db60e026fc16a1e43a758bdc3e769218f3f44
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
$ docker pull memcached@sha256:b995c17f51fbc95ab650436bf004e0e08aac1e231a0c4ced640ba25409a53ab5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32209591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2ebce0923097e2ebc228b419829228444709a8f2168920008cde8f0aacd5f50`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:339cbfbe5560ff0c225f888ba7ae149a9ce0536968c1bcccc467ceea4e3b09a0`  
		Last Modified: Mon, 29 Sep 2025 23:53:01 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84637889c9320e34d3cc8375e48fdc43299460f2280a8b62690c6d78f6a1ccf0`  
		Last Modified: Mon, 29 Sep 2025 23:53:01 GMT  
		Size: 136.6 KB (136571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe788cc20223f97addb89c197bd5ea5d77c3bbe084b00e8dcb70731168abb3b`  
		Last Modified: Mon, 29 Sep 2025 23:53:02 GMT  
		Size: 2.3 MB (2293745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e090b148236c9a2470abf0308fbdf9c8ed3c23b04efdfb18e68f20902a2e2f36`  
		Last Modified: Mon, 29 Sep 2025 23:53:02 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93fa1d160038c361af454d4a8eb44b68dcda89fc415ad571b6e9707fb59a0082`  
		Last Modified: Mon, 29 Sep 2025 23:53:02 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:5cd8c391814b8c7fbf65b5d657526c37f0516c6e4fe7dc245bfc347550a31200
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40690a93df6f911472221738e6595b6a746bd957d3bf1552c92ff83f17536644`

```dockerfile
```

-	Layers:
	-	`sha256:4b787171563846ab285584301f579a404cecd6f570a25225e02ff18939e29124`  
		Last Modified: Tue, 30 Sep 2025 00:34:34 GMT  
		Size: 2.0 MB (2008180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5a013035c58f0ea6bcc734d2c89618a0e98d1d8b3d3f07a169cd97b52bf4c0d`  
		Last Modified: Tue, 30 Sep 2025 00:34:35 GMT  
		Size: 22.2 KB (22196 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm variant v5

```console
$ docker pull memcached@sha256:29d660bf29e180ab12efa8f4cdf6a974ec008d83e2c3c8ec051dee748eb9ed04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30319195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d982473f8bce68d8cb2795fc64f125c06b91ec37e8e238bf7464d2e1fdba6a1b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1760918400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:389bac9f76fa529ccf801fd7c9cb260ecee27d208221c25004185ab22936c4d4`  
		Last Modified: Tue, 21 Oct 2025 00:20:45 GMT  
		Size: 27.9 MB (27946283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed93883017eb3f4dde85524af233ee0b6e174c0abe1cef988e9bce8d5375e89`  
		Last Modified: Tue, 21 Oct 2025 01:23:33 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:791751af616e97272032619ddc7968fe23e71223657f52594fb2c62a2a47eda5`  
		Last Modified: Tue, 21 Oct 2025 01:23:33 GMT  
		Size: 144.0 KB (144045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5ea9c6e85cf6a029a9ba48b6b73a8dc6479d59392f254b1c2db7b1902074dd`  
		Last Modified: Tue, 21 Oct 2025 01:23:33 GMT  
		Size: 2.2 MB (2227357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a58aefd26c4b989c6b88d95adb3a6920797ab35bfccd55f1001d478ea7c38e`  
		Last Modified: Tue, 21 Oct 2025 01:23:33 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87cab310dfac01ff5304eeb4a6ea3ddebf9ab9ab7badd32bb16312e9ad5c22ae`  
		Last Modified: Tue, 21 Oct 2025 01:23:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:63d0a43eb60f7ffb19e7cc876899b414f91eda292c74d1ecd4894dbc17394c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81a59c35b11c8306faf5db19cf7b6aee2213f889fcdcad2f2058c233038f5c2d`

```dockerfile
```

-	Layers:
	-	`sha256:b6117037dd5100454e92bb311823f69d718d18239a54c39029a154a68618f82b`  
		Last Modified: Tue, 21 Oct 2025 06:34:24 GMT  
		Size: 2.0 MB (2011237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfc7fdadb808663bde556e0343ab1151a3545e7211fe7e6e71915327352feedf`  
		Last Modified: Tue, 21 Oct 2025 06:34:25 GMT  
		Size: 22.3 KB (22346 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm variant v7

```console
$ docker pull memcached@sha256:889cba709c7ad01fa2925b49389f4e73f9d759d8020c2a108aabd5a1b1f2ee95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28532153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56676dc32ecaa308b63acf0b41885c581e3700d44bc04a653a595327d4198c3a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1759104000'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0289e98159900b326d4cedde367bf225e25835a3ad879647f17f922e43cfa884`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 26.2 MB (26212758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c067599f6c6ba1a22613aa308e4d66e5249d6cc507b1229b6f4d482aecce8a6`  
		Last Modified: Tue, 30 Sep 2025 00:01:20 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cf0eec4f32f0da160c5e99bd0b57756034bb7093c545143caf6e310210cb44`  
		Last Modified: Tue, 30 Sep 2025 00:01:20 GMT  
		Size: 135.3 KB (135298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e59b4e18c59ebfcadada2142ce2be01e708dd3af20396b507979cf3a15f6f22`  
		Last Modified: Tue, 30 Sep 2025 00:01:20 GMT  
		Size: 2.2 MB (2182588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a24488f6b368fccedb9bb9614c2c525964ee0e3cc91e91d2b41f74b38a1c9a59`  
		Last Modified: Tue, 30 Sep 2025 00:01:20 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413fbe42e3bd71205a88a777ab5027fc34a2ad8053f6593d6653d72ae17ba8ff`  
		Last Modified: Tue, 30 Sep 2025 00:01:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:ca8765c9f99276788e2b51ecfaf135680c03e0c222b9753d99dc4218bcc94095
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b6914431db285aeda4c9e27af56a106671c3541420f5b3bce905bed9f17ac6f`

```dockerfile
```

-	Layers:
	-	`sha256:fb1138fbff85001f5063fc6944faf0e66d26d9a179651b7a6b0c05c7f33a9240`  
		Last Modified: Tue, 30 Sep 2025 00:34:43 GMT  
		Size: 2.0 MB (2009640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c15f19f4d680266479069e896e888cb3a6a008b2f385c644c4f0baa61370937`  
		Last Modified: Tue, 30 Sep 2025 00:34:44 GMT  
		Size: 22.3 KB (22345 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:ef5cebc6723efc4307b7e2459b1b2c096013265dcfc93ee6e929dfb04399da59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32570960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b078c21daa3a3ef97cfc057882f396e936961312205c8e1a12712f179cf9f15`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c850e44210e9493ef7540c5c65cd48360355c3e6e94094c44d15af0045dc8dea`  
		Last Modified: Mon, 29 Sep 2025 23:59:01 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a741f1a1ae0d87da15466cd2dafd5acfb37dd72d94dda9656931ef24906d618`  
		Last Modified: Mon, 29 Sep 2025 23:59:01 GMT  
		Size: 153.4 KB (153385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa09f33f1e4c185a911cfd4dcd7d1dbbba5b9909fbe9100480230f1436457116`  
		Last Modified: Mon, 29 Sep 2025 23:59:01 GMT  
		Size: 2.3 MB (2275224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9a30963a9969bd789a111826840c0e97edd5d71548b548a30932bee7448fcc`  
		Last Modified: Mon, 29 Sep 2025 23:59:01 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ffdbd101cdb57f8b290f16ae4fa6106fd6ea85695fed7d08e98fdd19332d85`  
		Last Modified: Mon, 29 Sep 2025 23:59:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:573b95a8bb8dd5178978144dbd1446143419bbfc4edb099c6ebbe467c8e00b83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2a5e2b768012fff6837a6324e893b847c3948649e73a49b722b5d6b4b2d1f38`

```dockerfile
```

-	Layers:
	-	`sha256:8ab701ab9aad8acae756d96838becc2299738dcbdd81cb0071e6fbb5459b2f5b`  
		Last Modified: Tue, 30 Sep 2025 00:34:48 GMT  
		Size: 2.0 MB (2008496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71a37a40aa0845aeb88bc64f742dc25764c4824bedfe40f31b6f13e0bbd595b7`  
		Last Modified: Tue, 30 Sep 2025 00:34:48 GMT  
		Size: 22.4 KB (22393 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; 386

```console
$ docker pull memcached@sha256:0d993065ea1ed42de5bd4fcda3bafa779f274987bcb4d302b8a927344105ce6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33687876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fe2c39bed6edf857f276a7b8e77499f6c2110ebe12362143053acafdf31fba3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ab4c7760f4a4bda4b0797f3f0b56bd90b9778b76fc8351f2e1bd7c332b9dcc92`  
		Last Modified: Mon, 29 Sep 2025 23:35:33 GMT  
		Size: 31.3 MB (31294536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bcd1d82da4702bb3c598bb03b9d138dea8bd5e459160d5276b3fb8ebfb58923`  
		Last Modified: Mon, 29 Sep 2025 23:58:18 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ceba58f3514163ba75fa31b3b659efbe123eee61ee1e13161b71c6976b9cca2`  
		Last Modified: Mon, 29 Sep 2025 23:58:17 GMT  
		Size: 147.4 KB (147429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0453c4dd0d673c524b37cefb6f3412d20dde32e36c7999a26420bfb8481b0add`  
		Last Modified: Mon, 29 Sep 2025 23:58:18 GMT  
		Size: 2.2 MB (2244401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8916b29a59d03a745388da5e0a1aae97b201cd0e333de592e8a0fbe93da42b2f`  
		Last Modified: Mon, 29 Sep 2025 23:58:18 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28a35d7ac2cedad97d815d581ffa42e79c00126410603b586fb754ff264b578`  
		Last Modified: Mon, 29 Sep 2025 23:58:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:a1cbda14df44fff2e8baad5f7b53a3c32f617c55d96176326e107932e625e1d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef21897bb3061b8deedad86c30704928e376dad42a0a0bd9bdd946ff1cd46e37`

```dockerfile
```

-	Layers:
	-	`sha256:1f6010c4e760c848d7546664960f84f5082bc718d59b4dee6be3dc6489f1b283`  
		Last Modified: Tue, 30 Sep 2025 00:34:53 GMT  
		Size: 2.0 MB (2005337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f0fb1a46b98e7a2df02e226e82cd6854123a501d2d649bd70f05dbba8c4ffb7`  
		Last Modified: Tue, 30 Sep 2025 00:34:54 GMT  
		Size: 22.1 KB (22138 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; ppc64le

```console
$ docker pull memcached@sha256:78facd60957c01a0fc2c93514ec1f636e2acc585252bf3d2b224c9e4a2720751
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36187154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:078835e44984fd2f6238dc1bedb2dcc1eb3d45b38c738650295299276d8e3052`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1760918400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a9b4dd19a96be85b367998327f4288ed2fa8f174d1b3e8bea8ac7c2c626ec865`  
		Last Modified: Tue, 21 Oct 2025 00:26:55 GMT  
		Size: 33.6 MB (33598518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbed628a221d903400b8d49b4dc58aa0541e23d5a909543d626205670fd1072e`  
		Last Modified: Tue, 21 Oct 2025 01:54:52 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e748ebb38f38290596ca068f9f7e75e6c669eb4588462f2fe0b3566753e7f5`  
		Last Modified: Tue, 21 Oct 2025 01:54:53 GMT  
		Size: 170.3 KB (170257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b23f2908f85849ad3cfc2d526edf441cafb4862876c74e7c77fb5daeac7cc908`  
		Last Modified: Tue, 21 Oct 2025 01:54:53 GMT  
		Size: 2.4 MB (2416870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82d739662461ca129d2f470c2fa271c4962856a0f4a86f15d9469b59228c429`  
		Last Modified: Tue, 21 Oct 2025 01:54:52 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cefac88d4c183e05bebf79bdd2a0ad83aa10bbf75f4d809e74a8e7adb46146d`  
		Last Modified: Tue, 21 Oct 2025 01:54:53 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:766403e34da539f4d7944ceccfddc6817ff9a2e87659514dca52e26b77f14121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:093b6d02f98d1abdf2e4d567f2158cd54a22a08c01d42563dcd4d0f7a8d6121b`

```dockerfile
```

-	Layers:
	-	`sha256:89c9d8d8bddf968ee9f05171ddf674944ccf96d2c3df27dd2f5612e452da714e`  
		Last Modified: Tue, 21 Oct 2025 03:34:32 GMT  
		Size: 2.0 MB (2011835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72201c797f2648a5b0be16e7dc44930d3ddc214e2d4bc27d43cd6b923d85e481`  
		Last Modified: Tue, 21 Oct 2025 03:34:33 GMT  
		Size: 22.3 KB (22270 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; riscv64

```console
$ docker pull memcached@sha256:275951d176352ae7a6c07c3342e4a3696ed07e5711b47a3d3eac6d077943d7fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30629997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a439308e1f0b95ecea2e57b1abd7e75a6013568a1a7500b1f4d7bd0e21ad63`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6d1567708d42906165204f9177d357cb6a2fd51f758da447f1743b00813f892f`  
		Last Modified: Tue, 21 Oct 2025 00:37:37 GMT  
		Size: 28.3 MB (28275650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3633fd6545714a9d496af99598a2f2d1d149fd30ccb0af33ca4b5a64f2c80db2`  
		Last Modified: Tue, 21 Oct 2025 03:45:15 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0080b76dfc5efa9880c5885d69ca4cb830c2b81c8868038da6c3ec979f4df45f`  
		Last Modified: Tue, 21 Oct 2025 03:45:15 GMT  
		Size: 133.0 KB (132972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852a88ae8dfab39558e6bfca2ab58f39c01708aae430b3414e67d8fadc449694`  
		Last Modified: Tue, 21 Oct 2025 03:45:16 GMT  
		Size: 2.2 MB (2219861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a327b2de5a4375096f16800253786a6cfa67cce06f9f359b1c824e8232e98410`  
		Last Modified: Tue, 21 Oct 2025 03:45:15 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c933f2561e6f8e1189581b1eeb13dad69d7136a328a0533102686c15e68cb541`  
		Last Modified: Tue, 21 Oct 2025 03:45:15 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:7b68aaa7179e5972f8e6c99cbc3683f42653a9b4e71b3083cc76c60f88a4ecb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29ef9b8ffe7eed5ede85b59399c486af192d1744333cfa894153cffdf84ebefa`

```dockerfile
```

-	Layers:
	-	`sha256:861eae89f87c467092bc44440857f9d241e78153edc4d2e4fa84f83964fcbefe`  
		Last Modified: Tue, 21 Oct 2025 06:34:37 GMT  
		Size: 2.0 MB (2002198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7005598b4f28cfd2d5cfca73d6642c460d950449af439a25f8d87d7e8442aef6`  
		Last Modified: Tue, 21 Oct 2025 06:34:38 GMT  
		Size: 22.3 KB (22270 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; s390x

```console
$ docker pull memcached@sha256:97d22f11a028c8313d60f2b0d408dda8b2d48228b9b75aa2837e5463a793b535
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32292996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3e07eed38bed1a525726cbdc7874a25878c07feafb0bd683fe1f6583de2f83e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1759104000'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:924b0740f35a15fc20142be5c392f6b033c8051daecf16d2db38c22d6d73eb53`  
		Last Modified: Mon, 29 Sep 2025 23:41:29 GMT  
		Size: 29.8 MB (29837230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f51adc9bddc158c97c423c25020f779f6eaf1052b5377d27f3c426f6e1bfc021`  
		Last Modified: Tue, 30 Sep 2025 06:33:13 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e96b9e4bc41b016b366753e5d7d24d6ec0ad57f58fd33f9950ec9221297a8a4`  
		Last Modified: Tue, 30 Sep 2025 06:33:13 GMT  
		Size: 140.4 KB (140431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e41252907eabe8a9429031bb41587143d8a76355a4ec8726199ab91669e2ec3`  
		Last Modified: Tue, 30 Sep 2025 06:33:13 GMT  
		Size: 2.3 MB (2313824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2a41347a9c48966679d812976b6782615489e8d5f3d097e121b6150546f1cb`  
		Last Modified: Tue, 30 Sep 2025 06:33:13 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:969f1ab4db0027abb6561b0f8c35ae90cdfd2564247531bffcfb8860284b4319`  
		Last Modified: Tue, 30 Sep 2025 06:33:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:3f77e30f08514ef437bcf703e92082745153815200f728ce23b57a22ebbe9f84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0af62fcf07f143e611b564b8cdb2e08d11e05d8a8917d137e71fa925d6c936e4`

```dockerfile
```

-	Layers:
	-	`sha256:2db70adf2290adc880f8aa191f9e3b299c9dd28f01e3277a5386f4830c1f1f16`  
		Last Modified: Wed, 01 Oct 2025 21:34:44 GMT  
		Size: 2.0 MB (2009617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c002c1b0040529dcbb20761ae0b22e83c70cbf1d616626a80eff7eeccc02b1e6`  
		Last Modified: Wed, 01 Oct 2025 21:34:45 GMT  
		Size: 22.2 KB (22196 bytes)  
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
$ docker pull memcached@sha256:302493fd5e802f3bad0b33d2dc1db60e026fc16a1e43a758bdc3e769218f3f44
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
$ docker pull memcached@sha256:b995c17f51fbc95ab650436bf004e0e08aac1e231a0c4ced640ba25409a53ab5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32209591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2ebce0923097e2ebc228b419829228444709a8f2168920008cde8f0aacd5f50`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:339cbfbe5560ff0c225f888ba7ae149a9ce0536968c1bcccc467ceea4e3b09a0`  
		Last Modified: Mon, 29 Sep 2025 23:53:01 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84637889c9320e34d3cc8375e48fdc43299460f2280a8b62690c6d78f6a1ccf0`  
		Last Modified: Mon, 29 Sep 2025 23:53:01 GMT  
		Size: 136.6 KB (136571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe788cc20223f97addb89c197bd5ea5d77c3bbe084b00e8dcb70731168abb3b`  
		Last Modified: Mon, 29 Sep 2025 23:53:02 GMT  
		Size: 2.3 MB (2293745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e090b148236c9a2470abf0308fbdf9c8ed3c23b04efdfb18e68f20902a2e2f36`  
		Last Modified: Mon, 29 Sep 2025 23:53:02 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93fa1d160038c361af454d4a8eb44b68dcda89fc415ad571b6e9707fb59a0082`  
		Last Modified: Mon, 29 Sep 2025 23:53:02 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:5cd8c391814b8c7fbf65b5d657526c37f0516c6e4fe7dc245bfc347550a31200
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40690a93df6f911472221738e6595b6a746bd957d3bf1552c92ff83f17536644`

```dockerfile
```

-	Layers:
	-	`sha256:4b787171563846ab285584301f579a404cecd6f570a25225e02ff18939e29124`  
		Last Modified: Tue, 30 Sep 2025 00:34:34 GMT  
		Size: 2.0 MB (2008180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5a013035c58f0ea6bcc734d2c89618a0e98d1d8b3d3f07a169cd97b52bf4c0d`  
		Last Modified: Tue, 30 Sep 2025 00:34:35 GMT  
		Size: 22.2 KB (22196 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; arm variant v5

```console
$ docker pull memcached@sha256:29d660bf29e180ab12efa8f4cdf6a974ec008d83e2c3c8ec051dee748eb9ed04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30319195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d982473f8bce68d8cb2795fc64f125c06b91ec37e8e238bf7464d2e1fdba6a1b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1760918400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:389bac9f76fa529ccf801fd7c9cb260ecee27d208221c25004185ab22936c4d4`  
		Last Modified: Tue, 21 Oct 2025 00:20:45 GMT  
		Size: 27.9 MB (27946283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed93883017eb3f4dde85524af233ee0b6e174c0abe1cef988e9bce8d5375e89`  
		Last Modified: Tue, 21 Oct 2025 01:23:33 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:791751af616e97272032619ddc7968fe23e71223657f52594fb2c62a2a47eda5`  
		Last Modified: Tue, 21 Oct 2025 01:23:33 GMT  
		Size: 144.0 KB (144045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5ea9c6e85cf6a029a9ba48b6b73a8dc6479d59392f254b1c2db7b1902074dd`  
		Last Modified: Tue, 21 Oct 2025 01:23:33 GMT  
		Size: 2.2 MB (2227357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a58aefd26c4b989c6b88d95adb3a6920797ab35bfccd55f1001d478ea7c38e`  
		Last Modified: Tue, 21 Oct 2025 01:23:33 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87cab310dfac01ff5304eeb4a6ea3ddebf9ab9ab7badd32bb16312e9ad5c22ae`  
		Last Modified: Tue, 21 Oct 2025 01:23:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:63d0a43eb60f7ffb19e7cc876899b414f91eda292c74d1ecd4894dbc17394c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81a59c35b11c8306faf5db19cf7b6aee2213f889fcdcad2f2058c233038f5c2d`

```dockerfile
```

-	Layers:
	-	`sha256:b6117037dd5100454e92bb311823f69d718d18239a54c39029a154a68618f82b`  
		Last Modified: Tue, 21 Oct 2025 06:34:24 GMT  
		Size: 2.0 MB (2011237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfc7fdadb808663bde556e0343ab1151a3545e7211fe7e6e71915327352feedf`  
		Last Modified: Tue, 21 Oct 2025 06:34:25 GMT  
		Size: 22.3 KB (22346 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; arm variant v7

```console
$ docker pull memcached@sha256:889cba709c7ad01fa2925b49389f4e73f9d759d8020c2a108aabd5a1b1f2ee95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28532153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56676dc32ecaa308b63acf0b41885c581e3700d44bc04a653a595327d4198c3a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1759104000'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0289e98159900b326d4cedde367bf225e25835a3ad879647f17f922e43cfa884`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 26.2 MB (26212758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c067599f6c6ba1a22613aa308e4d66e5249d6cc507b1229b6f4d482aecce8a6`  
		Last Modified: Tue, 30 Sep 2025 00:01:20 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cf0eec4f32f0da160c5e99bd0b57756034bb7093c545143caf6e310210cb44`  
		Last Modified: Tue, 30 Sep 2025 00:01:20 GMT  
		Size: 135.3 KB (135298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e59b4e18c59ebfcadada2142ce2be01e708dd3af20396b507979cf3a15f6f22`  
		Last Modified: Tue, 30 Sep 2025 00:01:20 GMT  
		Size: 2.2 MB (2182588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a24488f6b368fccedb9bb9614c2c525964ee0e3cc91e91d2b41f74b38a1c9a59`  
		Last Modified: Tue, 30 Sep 2025 00:01:20 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413fbe42e3bd71205a88a777ab5027fc34a2ad8053f6593d6653d72ae17ba8ff`  
		Last Modified: Tue, 30 Sep 2025 00:01:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:ca8765c9f99276788e2b51ecfaf135680c03e0c222b9753d99dc4218bcc94095
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b6914431db285aeda4c9e27af56a106671c3541420f5b3bce905bed9f17ac6f`

```dockerfile
```

-	Layers:
	-	`sha256:fb1138fbff85001f5063fc6944faf0e66d26d9a179651b7a6b0c05c7f33a9240`  
		Last Modified: Tue, 30 Sep 2025 00:34:43 GMT  
		Size: 2.0 MB (2009640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c15f19f4d680266479069e896e888cb3a6a008b2f385c644c4f0baa61370937`  
		Last Modified: Tue, 30 Sep 2025 00:34:44 GMT  
		Size: 22.3 KB (22345 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:ef5cebc6723efc4307b7e2459b1b2c096013265dcfc93ee6e929dfb04399da59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32570960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b078c21daa3a3ef97cfc057882f396e936961312205c8e1a12712f179cf9f15`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c850e44210e9493ef7540c5c65cd48360355c3e6e94094c44d15af0045dc8dea`  
		Last Modified: Mon, 29 Sep 2025 23:59:01 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a741f1a1ae0d87da15466cd2dafd5acfb37dd72d94dda9656931ef24906d618`  
		Last Modified: Mon, 29 Sep 2025 23:59:01 GMT  
		Size: 153.4 KB (153385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa09f33f1e4c185a911cfd4dcd7d1dbbba5b9909fbe9100480230f1436457116`  
		Last Modified: Mon, 29 Sep 2025 23:59:01 GMT  
		Size: 2.3 MB (2275224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9a30963a9969bd789a111826840c0e97edd5d71548b548a30932bee7448fcc`  
		Last Modified: Mon, 29 Sep 2025 23:59:01 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ffdbd101cdb57f8b290f16ae4fa6106fd6ea85695fed7d08e98fdd19332d85`  
		Last Modified: Mon, 29 Sep 2025 23:59:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:573b95a8bb8dd5178978144dbd1446143419bbfc4edb099c6ebbe467c8e00b83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2a5e2b768012fff6837a6324e893b847c3948649e73a49b722b5d6b4b2d1f38`

```dockerfile
```

-	Layers:
	-	`sha256:8ab701ab9aad8acae756d96838becc2299738dcbdd81cb0071e6fbb5459b2f5b`  
		Last Modified: Tue, 30 Sep 2025 00:34:48 GMT  
		Size: 2.0 MB (2008496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71a37a40aa0845aeb88bc64f742dc25764c4824bedfe40f31b6f13e0bbd595b7`  
		Last Modified: Tue, 30 Sep 2025 00:34:48 GMT  
		Size: 22.4 KB (22393 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; 386

```console
$ docker pull memcached@sha256:0d993065ea1ed42de5bd4fcda3bafa779f274987bcb4d302b8a927344105ce6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33687876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fe2c39bed6edf857f276a7b8e77499f6c2110ebe12362143053acafdf31fba3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ab4c7760f4a4bda4b0797f3f0b56bd90b9778b76fc8351f2e1bd7c332b9dcc92`  
		Last Modified: Mon, 29 Sep 2025 23:35:33 GMT  
		Size: 31.3 MB (31294536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bcd1d82da4702bb3c598bb03b9d138dea8bd5e459160d5276b3fb8ebfb58923`  
		Last Modified: Mon, 29 Sep 2025 23:58:18 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ceba58f3514163ba75fa31b3b659efbe123eee61ee1e13161b71c6976b9cca2`  
		Last Modified: Mon, 29 Sep 2025 23:58:17 GMT  
		Size: 147.4 KB (147429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0453c4dd0d673c524b37cefb6f3412d20dde32e36c7999a26420bfb8481b0add`  
		Last Modified: Mon, 29 Sep 2025 23:58:18 GMT  
		Size: 2.2 MB (2244401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8916b29a59d03a745388da5e0a1aae97b201cd0e333de592e8a0fbe93da42b2f`  
		Last Modified: Mon, 29 Sep 2025 23:58:18 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28a35d7ac2cedad97d815d581ffa42e79c00126410603b586fb754ff264b578`  
		Last Modified: Mon, 29 Sep 2025 23:58:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:a1cbda14df44fff2e8baad5f7b53a3c32f617c55d96176326e107932e625e1d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef21897bb3061b8deedad86c30704928e376dad42a0a0bd9bdd946ff1cd46e37`

```dockerfile
```

-	Layers:
	-	`sha256:1f6010c4e760c848d7546664960f84f5082bc718d59b4dee6be3dc6489f1b283`  
		Last Modified: Tue, 30 Sep 2025 00:34:53 GMT  
		Size: 2.0 MB (2005337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f0fb1a46b98e7a2df02e226e82cd6854123a501d2d649bd70f05dbba8c4ffb7`  
		Last Modified: Tue, 30 Sep 2025 00:34:54 GMT  
		Size: 22.1 KB (22138 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; ppc64le

```console
$ docker pull memcached@sha256:78facd60957c01a0fc2c93514ec1f636e2acc585252bf3d2b224c9e4a2720751
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36187154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:078835e44984fd2f6238dc1bedb2dcc1eb3d45b38c738650295299276d8e3052`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1760918400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a9b4dd19a96be85b367998327f4288ed2fa8f174d1b3e8bea8ac7c2c626ec865`  
		Last Modified: Tue, 21 Oct 2025 00:26:55 GMT  
		Size: 33.6 MB (33598518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbed628a221d903400b8d49b4dc58aa0541e23d5a909543d626205670fd1072e`  
		Last Modified: Tue, 21 Oct 2025 01:54:52 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e748ebb38f38290596ca068f9f7e75e6c669eb4588462f2fe0b3566753e7f5`  
		Last Modified: Tue, 21 Oct 2025 01:54:53 GMT  
		Size: 170.3 KB (170257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b23f2908f85849ad3cfc2d526edf441cafb4862876c74e7c77fb5daeac7cc908`  
		Last Modified: Tue, 21 Oct 2025 01:54:53 GMT  
		Size: 2.4 MB (2416870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82d739662461ca129d2f470c2fa271c4962856a0f4a86f15d9469b59228c429`  
		Last Modified: Tue, 21 Oct 2025 01:54:52 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cefac88d4c183e05bebf79bdd2a0ad83aa10bbf75f4d809e74a8e7adb46146d`  
		Last Modified: Tue, 21 Oct 2025 01:54:53 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:766403e34da539f4d7944ceccfddc6817ff9a2e87659514dca52e26b77f14121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:093b6d02f98d1abdf2e4d567f2158cd54a22a08c01d42563dcd4d0f7a8d6121b`

```dockerfile
```

-	Layers:
	-	`sha256:89c9d8d8bddf968ee9f05171ddf674944ccf96d2c3df27dd2f5612e452da714e`  
		Last Modified: Tue, 21 Oct 2025 03:34:32 GMT  
		Size: 2.0 MB (2011835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72201c797f2648a5b0be16e7dc44930d3ddc214e2d4bc27d43cd6b923d85e481`  
		Last Modified: Tue, 21 Oct 2025 03:34:33 GMT  
		Size: 22.3 KB (22270 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; riscv64

```console
$ docker pull memcached@sha256:275951d176352ae7a6c07c3342e4a3696ed07e5711b47a3d3eac6d077943d7fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30629997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a439308e1f0b95ecea2e57b1abd7e75a6013568a1a7500b1f4d7bd0e21ad63`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6d1567708d42906165204f9177d357cb6a2fd51f758da447f1743b00813f892f`  
		Last Modified: Tue, 21 Oct 2025 00:37:37 GMT  
		Size: 28.3 MB (28275650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3633fd6545714a9d496af99598a2f2d1d149fd30ccb0af33ca4b5a64f2c80db2`  
		Last Modified: Tue, 21 Oct 2025 03:45:15 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0080b76dfc5efa9880c5885d69ca4cb830c2b81c8868038da6c3ec979f4df45f`  
		Last Modified: Tue, 21 Oct 2025 03:45:15 GMT  
		Size: 133.0 KB (132972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852a88ae8dfab39558e6bfca2ab58f39c01708aae430b3414e67d8fadc449694`  
		Last Modified: Tue, 21 Oct 2025 03:45:16 GMT  
		Size: 2.2 MB (2219861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a327b2de5a4375096f16800253786a6cfa67cce06f9f359b1c824e8232e98410`  
		Last Modified: Tue, 21 Oct 2025 03:45:15 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c933f2561e6f8e1189581b1eeb13dad69d7136a328a0533102686c15e68cb541`  
		Last Modified: Tue, 21 Oct 2025 03:45:15 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:7b68aaa7179e5972f8e6c99cbc3683f42653a9b4e71b3083cc76c60f88a4ecb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29ef9b8ffe7eed5ede85b59399c486af192d1744333cfa894153cffdf84ebefa`

```dockerfile
```

-	Layers:
	-	`sha256:861eae89f87c467092bc44440857f9d241e78153edc4d2e4fa84f83964fcbefe`  
		Last Modified: Tue, 21 Oct 2025 06:34:37 GMT  
		Size: 2.0 MB (2002198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7005598b4f28cfd2d5cfca73d6642c460d950449af439a25f8d87d7e8442aef6`  
		Last Modified: Tue, 21 Oct 2025 06:34:38 GMT  
		Size: 22.3 KB (22270 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; s390x

```console
$ docker pull memcached@sha256:97d22f11a028c8313d60f2b0d408dda8b2d48228b9b75aa2837e5463a793b535
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32292996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3e07eed38bed1a525726cbdc7874a25878c07feafb0bd683fe1f6583de2f83e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1759104000'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:924b0740f35a15fc20142be5c392f6b033c8051daecf16d2db38c22d6d73eb53`  
		Last Modified: Mon, 29 Sep 2025 23:41:29 GMT  
		Size: 29.8 MB (29837230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f51adc9bddc158c97c423c25020f779f6eaf1052b5377d27f3c426f6e1bfc021`  
		Last Modified: Tue, 30 Sep 2025 06:33:13 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e96b9e4bc41b016b366753e5d7d24d6ec0ad57f58fd33f9950ec9221297a8a4`  
		Last Modified: Tue, 30 Sep 2025 06:33:13 GMT  
		Size: 140.4 KB (140431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e41252907eabe8a9429031bb41587143d8a76355a4ec8726199ab91669e2ec3`  
		Last Modified: Tue, 30 Sep 2025 06:33:13 GMT  
		Size: 2.3 MB (2313824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2a41347a9c48966679d812976b6782615489e8d5f3d097e121b6150546f1cb`  
		Last Modified: Tue, 30 Sep 2025 06:33:13 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:969f1ab4db0027abb6561b0f8c35ae90cdfd2564247531bffcfb8860284b4319`  
		Last Modified: Tue, 30 Sep 2025 06:33:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:3f77e30f08514ef437bcf703e92082745153815200f728ce23b57a22ebbe9f84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0af62fcf07f143e611b564b8cdb2e08d11e05d8a8917d137e71fa925d6c936e4`

```dockerfile
```

-	Layers:
	-	`sha256:2db70adf2290adc880f8aa191f9e3b299c9dd28f01e3277a5386f4830c1f1f16`  
		Last Modified: Wed, 01 Oct 2025 21:34:44 GMT  
		Size: 2.0 MB (2009617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c002c1b0040529dcbb20761ae0b22e83c70cbf1d616626a80eff7eeccc02b1e6`  
		Last Modified: Wed, 01 Oct 2025 21:34:45 GMT  
		Size: 22.2 KB (22196 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6`

```console
$ docker pull memcached@sha256:302493fd5e802f3bad0b33d2dc1db60e026fc16a1e43a758bdc3e769218f3f44
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
$ docker pull memcached@sha256:b995c17f51fbc95ab650436bf004e0e08aac1e231a0c4ced640ba25409a53ab5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32209591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2ebce0923097e2ebc228b419829228444709a8f2168920008cde8f0aacd5f50`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:339cbfbe5560ff0c225f888ba7ae149a9ce0536968c1bcccc467ceea4e3b09a0`  
		Last Modified: Mon, 29 Sep 2025 23:53:01 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84637889c9320e34d3cc8375e48fdc43299460f2280a8b62690c6d78f6a1ccf0`  
		Last Modified: Mon, 29 Sep 2025 23:53:01 GMT  
		Size: 136.6 KB (136571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe788cc20223f97addb89c197bd5ea5d77c3bbe084b00e8dcb70731168abb3b`  
		Last Modified: Mon, 29 Sep 2025 23:53:02 GMT  
		Size: 2.3 MB (2293745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e090b148236c9a2470abf0308fbdf9c8ed3c23b04efdfb18e68f20902a2e2f36`  
		Last Modified: Mon, 29 Sep 2025 23:53:02 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93fa1d160038c361af454d4a8eb44b68dcda89fc415ad571b6e9707fb59a0082`  
		Last Modified: Mon, 29 Sep 2025 23:53:02 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:5cd8c391814b8c7fbf65b5d657526c37f0516c6e4fe7dc245bfc347550a31200
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40690a93df6f911472221738e6595b6a746bd957d3bf1552c92ff83f17536644`

```dockerfile
```

-	Layers:
	-	`sha256:4b787171563846ab285584301f579a404cecd6f570a25225e02ff18939e29124`  
		Last Modified: Tue, 30 Sep 2025 00:34:34 GMT  
		Size: 2.0 MB (2008180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5a013035c58f0ea6bcc734d2c89618a0e98d1d8b3d3f07a169cd97b52bf4c0d`  
		Last Modified: Tue, 30 Sep 2025 00:34:35 GMT  
		Size: 22.2 KB (22196 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm variant v5

```console
$ docker pull memcached@sha256:29d660bf29e180ab12efa8f4cdf6a974ec008d83e2c3c8ec051dee748eb9ed04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30319195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d982473f8bce68d8cb2795fc64f125c06b91ec37e8e238bf7464d2e1fdba6a1b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1760918400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:389bac9f76fa529ccf801fd7c9cb260ecee27d208221c25004185ab22936c4d4`  
		Last Modified: Tue, 21 Oct 2025 00:20:45 GMT  
		Size: 27.9 MB (27946283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed93883017eb3f4dde85524af233ee0b6e174c0abe1cef988e9bce8d5375e89`  
		Last Modified: Tue, 21 Oct 2025 01:23:33 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:791751af616e97272032619ddc7968fe23e71223657f52594fb2c62a2a47eda5`  
		Last Modified: Tue, 21 Oct 2025 01:23:33 GMT  
		Size: 144.0 KB (144045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5ea9c6e85cf6a029a9ba48b6b73a8dc6479d59392f254b1c2db7b1902074dd`  
		Last Modified: Tue, 21 Oct 2025 01:23:33 GMT  
		Size: 2.2 MB (2227357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a58aefd26c4b989c6b88d95adb3a6920797ab35bfccd55f1001d478ea7c38e`  
		Last Modified: Tue, 21 Oct 2025 01:23:33 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87cab310dfac01ff5304eeb4a6ea3ddebf9ab9ab7badd32bb16312e9ad5c22ae`  
		Last Modified: Tue, 21 Oct 2025 01:23:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:63d0a43eb60f7ffb19e7cc876899b414f91eda292c74d1ecd4894dbc17394c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81a59c35b11c8306faf5db19cf7b6aee2213f889fcdcad2f2058c233038f5c2d`

```dockerfile
```

-	Layers:
	-	`sha256:b6117037dd5100454e92bb311823f69d718d18239a54c39029a154a68618f82b`  
		Last Modified: Tue, 21 Oct 2025 06:34:24 GMT  
		Size: 2.0 MB (2011237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfc7fdadb808663bde556e0343ab1151a3545e7211fe7e6e71915327352feedf`  
		Last Modified: Tue, 21 Oct 2025 06:34:25 GMT  
		Size: 22.3 KB (22346 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm variant v7

```console
$ docker pull memcached@sha256:889cba709c7ad01fa2925b49389f4e73f9d759d8020c2a108aabd5a1b1f2ee95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28532153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56676dc32ecaa308b63acf0b41885c581e3700d44bc04a653a595327d4198c3a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1759104000'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0289e98159900b326d4cedde367bf225e25835a3ad879647f17f922e43cfa884`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 26.2 MB (26212758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c067599f6c6ba1a22613aa308e4d66e5249d6cc507b1229b6f4d482aecce8a6`  
		Last Modified: Tue, 30 Sep 2025 00:01:20 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cf0eec4f32f0da160c5e99bd0b57756034bb7093c545143caf6e310210cb44`  
		Last Modified: Tue, 30 Sep 2025 00:01:20 GMT  
		Size: 135.3 KB (135298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e59b4e18c59ebfcadada2142ce2be01e708dd3af20396b507979cf3a15f6f22`  
		Last Modified: Tue, 30 Sep 2025 00:01:20 GMT  
		Size: 2.2 MB (2182588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a24488f6b368fccedb9bb9614c2c525964ee0e3cc91e91d2b41f74b38a1c9a59`  
		Last Modified: Tue, 30 Sep 2025 00:01:20 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413fbe42e3bd71205a88a777ab5027fc34a2ad8053f6593d6653d72ae17ba8ff`  
		Last Modified: Tue, 30 Sep 2025 00:01:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:ca8765c9f99276788e2b51ecfaf135680c03e0c222b9753d99dc4218bcc94095
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b6914431db285aeda4c9e27af56a106671c3541420f5b3bce905bed9f17ac6f`

```dockerfile
```

-	Layers:
	-	`sha256:fb1138fbff85001f5063fc6944faf0e66d26d9a179651b7a6b0c05c7f33a9240`  
		Last Modified: Tue, 30 Sep 2025 00:34:43 GMT  
		Size: 2.0 MB (2009640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c15f19f4d680266479069e896e888cb3a6a008b2f385c644c4f0baa61370937`  
		Last Modified: Tue, 30 Sep 2025 00:34:44 GMT  
		Size: 22.3 KB (22345 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:ef5cebc6723efc4307b7e2459b1b2c096013265dcfc93ee6e929dfb04399da59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32570960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b078c21daa3a3ef97cfc057882f396e936961312205c8e1a12712f179cf9f15`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c850e44210e9493ef7540c5c65cd48360355c3e6e94094c44d15af0045dc8dea`  
		Last Modified: Mon, 29 Sep 2025 23:59:01 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a741f1a1ae0d87da15466cd2dafd5acfb37dd72d94dda9656931ef24906d618`  
		Last Modified: Mon, 29 Sep 2025 23:59:01 GMT  
		Size: 153.4 KB (153385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa09f33f1e4c185a911cfd4dcd7d1dbbba5b9909fbe9100480230f1436457116`  
		Last Modified: Mon, 29 Sep 2025 23:59:01 GMT  
		Size: 2.3 MB (2275224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9a30963a9969bd789a111826840c0e97edd5d71548b548a30932bee7448fcc`  
		Last Modified: Mon, 29 Sep 2025 23:59:01 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ffdbd101cdb57f8b290f16ae4fa6106fd6ea85695fed7d08e98fdd19332d85`  
		Last Modified: Mon, 29 Sep 2025 23:59:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:573b95a8bb8dd5178978144dbd1446143419bbfc4edb099c6ebbe467c8e00b83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2a5e2b768012fff6837a6324e893b847c3948649e73a49b722b5d6b4b2d1f38`

```dockerfile
```

-	Layers:
	-	`sha256:8ab701ab9aad8acae756d96838becc2299738dcbdd81cb0071e6fbb5459b2f5b`  
		Last Modified: Tue, 30 Sep 2025 00:34:48 GMT  
		Size: 2.0 MB (2008496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71a37a40aa0845aeb88bc64f742dc25764c4824bedfe40f31b6f13e0bbd595b7`  
		Last Modified: Tue, 30 Sep 2025 00:34:48 GMT  
		Size: 22.4 KB (22393 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; 386

```console
$ docker pull memcached@sha256:0d993065ea1ed42de5bd4fcda3bafa779f274987bcb4d302b8a927344105ce6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33687876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fe2c39bed6edf857f276a7b8e77499f6c2110ebe12362143053acafdf31fba3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ab4c7760f4a4bda4b0797f3f0b56bd90b9778b76fc8351f2e1bd7c332b9dcc92`  
		Last Modified: Mon, 29 Sep 2025 23:35:33 GMT  
		Size: 31.3 MB (31294536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bcd1d82da4702bb3c598bb03b9d138dea8bd5e459160d5276b3fb8ebfb58923`  
		Last Modified: Mon, 29 Sep 2025 23:58:18 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ceba58f3514163ba75fa31b3b659efbe123eee61ee1e13161b71c6976b9cca2`  
		Last Modified: Mon, 29 Sep 2025 23:58:17 GMT  
		Size: 147.4 KB (147429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0453c4dd0d673c524b37cefb6f3412d20dde32e36c7999a26420bfb8481b0add`  
		Last Modified: Mon, 29 Sep 2025 23:58:18 GMT  
		Size: 2.2 MB (2244401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8916b29a59d03a745388da5e0a1aae97b201cd0e333de592e8a0fbe93da42b2f`  
		Last Modified: Mon, 29 Sep 2025 23:58:18 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28a35d7ac2cedad97d815d581ffa42e79c00126410603b586fb754ff264b578`  
		Last Modified: Mon, 29 Sep 2025 23:58:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:a1cbda14df44fff2e8baad5f7b53a3c32f617c55d96176326e107932e625e1d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef21897bb3061b8deedad86c30704928e376dad42a0a0bd9bdd946ff1cd46e37`

```dockerfile
```

-	Layers:
	-	`sha256:1f6010c4e760c848d7546664960f84f5082bc718d59b4dee6be3dc6489f1b283`  
		Last Modified: Tue, 30 Sep 2025 00:34:53 GMT  
		Size: 2.0 MB (2005337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f0fb1a46b98e7a2df02e226e82cd6854123a501d2d649bd70f05dbba8c4ffb7`  
		Last Modified: Tue, 30 Sep 2025 00:34:54 GMT  
		Size: 22.1 KB (22138 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; ppc64le

```console
$ docker pull memcached@sha256:78facd60957c01a0fc2c93514ec1f636e2acc585252bf3d2b224c9e4a2720751
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36187154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:078835e44984fd2f6238dc1bedb2dcc1eb3d45b38c738650295299276d8e3052`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1760918400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a9b4dd19a96be85b367998327f4288ed2fa8f174d1b3e8bea8ac7c2c626ec865`  
		Last Modified: Tue, 21 Oct 2025 00:26:55 GMT  
		Size: 33.6 MB (33598518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbed628a221d903400b8d49b4dc58aa0541e23d5a909543d626205670fd1072e`  
		Last Modified: Tue, 21 Oct 2025 01:54:52 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e748ebb38f38290596ca068f9f7e75e6c669eb4588462f2fe0b3566753e7f5`  
		Last Modified: Tue, 21 Oct 2025 01:54:53 GMT  
		Size: 170.3 KB (170257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b23f2908f85849ad3cfc2d526edf441cafb4862876c74e7c77fb5daeac7cc908`  
		Last Modified: Tue, 21 Oct 2025 01:54:53 GMT  
		Size: 2.4 MB (2416870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82d739662461ca129d2f470c2fa271c4962856a0f4a86f15d9469b59228c429`  
		Last Modified: Tue, 21 Oct 2025 01:54:52 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cefac88d4c183e05bebf79bdd2a0ad83aa10bbf75f4d809e74a8e7adb46146d`  
		Last Modified: Tue, 21 Oct 2025 01:54:53 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:766403e34da539f4d7944ceccfddc6817ff9a2e87659514dca52e26b77f14121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:093b6d02f98d1abdf2e4d567f2158cd54a22a08c01d42563dcd4d0f7a8d6121b`

```dockerfile
```

-	Layers:
	-	`sha256:89c9d8d8bddf968ee9f05171ddf674944ccf96d2c3df27dd2f5612e452da714e`  
		Last Modified: Tue, 21 Oct 2025 03:34:32 GMT  
		Size: 2.0 MB (2011835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72201c797f2648a5b0be16e7dc44930d3ddc214e2d4bc27d43cd6b923d85e481`  
		Last Modified: Tue, 21 Oct 2025 03:34:33 GMT  
		Size: 22.3 KB (22270 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; riscv64

```console
$ docker pull memcached@sha256:275951d176352ae7a6c07c3342e4a3696ed07e5711b47a3d3eac6d077943d7fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30629997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a439308e1f0b95ecea2e57b1abd7e75a6013568a1a7500b1f4d7bd0e21ad63`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6d1567708d42906165204f9177d357cb6a2fd51f758da447f1743b00813f892f`  
		Last Modified: Tue, 21 Oct 2025 00:37:37 GMT  
		Size: 28.3 MB (28275650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3633fd6545714a9d496af99598a2f2d1d149fd30ccb0af33ca4b5a64f2c80db2`  
		Last Modified: Tue, 21 Oct 2025 03:45:15 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0080b76dfc5efa9880c5885d69ca4cb830c2b81c8868038da6c3ec979f4df45f`  
		Last Modified: Tue, 21 Oct 2025 03:45:15 GMT  
		Size: 133.0 KB (132972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852a88ae8dfab39558e6bfca2ab58f39c01708aae430b3414e67d8fadc449694`  
		Last Modified: Tue, 21 Oct 2025 03:45:16 GMT  
		Size: 2.2 MB (2219861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a327b2de5a4375096f16800253786a6cfa67cce06f9f359b1c824e8232e98410`  
		Last Modified: Tue, 21 Oct 2025 03:45:15 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c933f2561e6f8e1189581b1eeb13dad69d7136a328a0533102686c15e68cb541`  
		Last Modified: Tue, 21 Oct 2025 03:45:15 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:7b68aaa7179e5972f8e6c99cbc3683f42653a9b4e71b3083cc76c60f88a4ecb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29ef9b8ffe7eed5ede85b59399c486af192d1744333cfa894153cffdf84ebefa`

```dockerfile
```

-	Layers:
	-	`sha256:861eae89f87c467092bc44440857f9d241e78153edc4d2e4fa84f83964fcbefe`  
		Last Modified: Tue, 21 Oct 2025 06:34:37 GMT  
		Size: 2.0 MB (2002198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7005598b4f28cfd2d5cfca73d6642c460d950449af439a25f8d87d7e8442aef6`  
		Last Modified: Tue, 21 Oct 2025 06:34:38 GMT  
		Size: 22.3 KB (22270 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; s390x

```console
$ docker pull memcached@sha256:97d22f11a028c8313d60f2b0d408dda8b2d48228b9b75aa2837e5463a793b535
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32292996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3e07eed38bed1a525726cbdc7874a25878c07feafb0bd683fe1f6583de2f83e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1759104000'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:924b0740f35a15fc20142be5c392f6b033c8051daecf16d2db38c22d6d73eb53`  
		Last Modified: Mon, 29 Sep 2025 23:41:29 GMT  
		Size: 29.8 MB (29837230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f51adc9bddc158c97c423c25020f779f6eaf1052b5377d27f3c426f6e1bfc021`  
		Last Modified: Tue, 30 Sep 2025 06:33:13 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e96b9e4bc41b016b366753e5d7d24d6ec0ad57f58fd33f9950ec9221297a8a4`  
		Last Modified: Tue, 30 Sep 2025 06:33:13 GMT  
		Size: 140.4 KB (140431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e41252907eabe8a9429031bb41587143d8a76355a4ec8726199ab91669e2ec3`  
		Last Modified: Tue, 30 Sep 2025 06:33:13 GMT  
		Size: 2.3 MB (2313824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2a41347a9c48966679d812976b6782615489e8d5f3d097e121b6150546f1cb`  
		Last Modified: Tue, 30 Sep 2025 06:33:13 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:969f1ab4db0027abb6561b0f8c35ae90cdfd2564247531bffcfb8860284b4319`  
		Last Modified: Tue, 30 Sep 2025 06:33:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:3f77e30f08514ef437bcf703e92082745153815200f728ce23b57a22ebbe9f84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0af62fcf07f143e611b564b8cdb2e08d11e05d8a8917d137e71fa925d6c936e4`

```dockerfile
```

-	Layers:
	-	`sha256:2db70adf2290adc880f8aa191f9e3b299c9dd28f01e3277a5386f4830c1f1f16`  
		Last Modified: Wed, 01 Oct 2025 21:34:44 GMT  
		Size: 2.0 MB (2009617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c002c1b0040529dcbb20761ae0b22e83c70cbf1d616626a80eff7eeccc02b1e6`  
		Last Modified: Wed, 01 Oct 2025 21:34:45 GMT  
		Size: 22.2 KB (22196 bytes)  
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
$ docker pull memcached@sha256:302493fd5e802f3bad0b33d2dc1db60e026fc16a1e43a758bdc3e769218f3f44
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
$ docker pull memcached@sha256:b995c17f51fbc95ab650436bf004e0e08aac1e231a0c4ced640ba25409a53ab5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32209591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2ebce0923097e2ebc228b419829228444709a8f2168920008cde8f0aacd5f50`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:339cbfbe5560ff0c225f888ba7ae149a9ce0536968c1bcccc467ceea4e3b09a0`  
		Last Modified: Mon, 29 Sep 2025 23:53:01 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84637889c9320e34d3cc8375e48fdc43299460f2280a8b62690c6d78f6a1ccf0`  
		Last Modified: Mon, 29 Sep 2025 23:53:01 GMT  
		Size: 136.6 KB (136571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe788cc20223f97addb89c197bd5ea5d77c3bbe084b00e8dcb70731168abb3b`  
		Last Modified: Mon, 29 Sep 2025 23:53:02 GMT  
		Size: 2.3 MB (2293745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e090b148236c9a2470abf0308fbdf9c8ed3c23b04efdfb18e68f20902a2e2f36`  
		Last Modified: Mon, 29 Sep 2025 23:53:02 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93fa1d160038c361af454d4a8eb44b68dcda89fc415ad571b6e9707fb59a0082`  
		Last Modified: Mon, 29 Sep 2025 23:53:02 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:5cd8c391814b8c7fbf65b5d657526c37f0516c6e4fe7dc245bfc347550a31200
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40690a93df6f911472221738e6595b6a746bd957d3bf1552c92ff83f17536644`

```dockerfile
```

-	Layers:
	-	`sha256:4b787171563846ab285584301f579a404cecd6f570a25225e02ff18939e29124`  
		Last Modified: Tue, 30 Sep 2025 00:34:34 GMT  
		Size: 2.0 MB (2008180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5a013035c58f0ea6bcc734d2c89618a0e98d1d8b3d3f07a169cd97b52bf4c0d`  
		Last Modified: Tue, 30 Sep 2025 00:34:35 GMT  
		Size: 22.2 KB (22196 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; arm variant v5

```console
$ docker pull memcached@sha256:29d660bf29e180ab12efa8f4cdf6a974ec008d83e2c3c8ec051dee748eb9ed04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30319195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d982473f8bce68d8cb2795fc64f125c06b91ec37e8e238bf7464d2e1fdba6a1b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1760918400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:389bac9f76fa529ccf801fd7c9cb260ecee27d208221c25004185ab22936c4d4`  
		Last Modified: Tue, 21 Oct 2025 00:20:45 GMT  
		Size: 27.9 MB (27946283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed93883017eb3f4dde85524af233ee0b6e174c0abe1cef988e9bce8d5375e89`  
		Last Modified: Tue, 21 Oct 2025 01:23:33 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:791751af616e97272032619ddc7968fe23e71223657f52594fb2c62a2a47eda5`  
		Last Modified: Tue, 21 Oct 2025 01:23:33 GMT  
		Size: 144.0 KB (144045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5ea9c6e85cf6a029a9ba48b6b73a8dc6479d59392f254b1c2db7b1902074dd`  
		Last Modified: Tue, 21 Oct 2025 01:23:33 GMT  
		Size: 2.2 MB (2227357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a58aefd26c4b989c6b88d95adb3a6920797ab35bfccd55f1001d478ea7c38e`  
		Last Modified: Tue, 21 Oct 2025 01:23:33 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87cab310dfac01ff5304eeb4a6ea3ddebf9ab9ab7badd32bb16312e9ad5c22ae`  
		Last Modified: Tue, 21 Oct 2025 01:23:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:63d0a43eb60f7ffb19e7cc876899b414f91eda292c74d1ecd4894dbc17394c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81a59c35b11c8306faf5db19cf7b6aee2213f889fcdcad2f2058c233038f5c2d`

```dockerfile
```

-	Layers:
	-	`sha256:b6117037dd5100454e92bb311823f69d718d18239a54c39029a154a68618f82b`  
		Last Modified: Tue, 21 Oct 2025 06:34:24 GMT  
		Size: 2.0 MB (2011237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfc7fdadb808663bde556e0343ab1151a3545e7211fe7e6e71915327352feedf`  
		Last Modified: Tue, 21 Oct 2025 06:34:25 GMT  
		Size: 22.3 KB (22346 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; arm variant v7

```console
$ docker pull memcached@sha256:889cba709c7ad01fa2925b49389f4e73f9d759d8020c2a108aabd5a1b1f2ee95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28532153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56676dc32ecaa308b63acf0b41885c581e3700d44bc04a653a595327d4198c3a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1759104000'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0289e98159900b326d4cedde367bf225e25835a3ad879647f17f922e43cfa884`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 26.2 MB (26212758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c067599f6c6ba1a22613aa308e4d66e5249d6cc507b1229b6f4d482aecce8a6`  
		Last Modified: Tue, 30 Sep 2025 00:01:20 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cf0eec4f32f0da160c5e99bd0b57756034bb7093c545143caf6e310210cb44`  
		Last Modified: Tue, 30 Sep 2025 00:01:20 GMT  
		Size: 135.3 KB (135298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e59b4e18c59ebfcadada2142ce2be01e708dd3af20396b507979cf3a15f6f22`  
		Last Modified: Tue, 30 Sep 2025 00:01:20 GMT  
		Size: 2.2 MB (2182588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a24488f6b368fccedb9bb9614c2c525964ee0e3cc91e91d2b41f74b38a1c9a59`  
		Last Modified: Tue, 30 Sep 2025 00:01:20 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413fbe42e3bd71205a88a777ab5027fc34a2ad8053f6593d6653d72ae17ba8ff`  
		Last Modified: Tue, 30 Sep 2025 00:01:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:ca8765c9f99276788e2b51ecfaf135680c03e0c222b9753d99dc4218bcc94095
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b6914431db285aeda4c9e27af56a106671c3541420f5b3bce905bed9f17ac6f`

```dockerfile
```

-	Layers:
	-	`sha256:fb1138fbff85001f5063fc6944faf0e66d26d9a179651b7a6b0c05c7f33a9240`  
		Last Modified: Tue, 30 Sep 2025 00:34:43 GMT  
		Size: 2.0 MB (2009640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c15f19f4d680266479069e896e888cb3a6a008b2f385c644c4f0baa61370937`  
		Last Modified: Tue, 30 Sep 2025 00:34:44 GMT  
		Size: 22.3 KB (22345 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:ef5cebc6723efc4307b7e2459b1b2c096013265dcfc93ee6e929dfb04399da59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32570960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b078c21daa3a3ef97cfc057882f396e936961312205c8e1a12712f179cf9f15`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c850e44210e9493ef7540c5c65cd48360355c3e6e94094c44d15af0045dc8dea`  
		Last Modified: Mon, 29 Sep 2025 23:59:01 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a741f1a1ae0d87da15466cd2dafd5acfb37dd72d94dda9656931ef24906d618`  
		Last Modified: Mon, 29 Sep 2025 23:59:01 GMT  
		Size: 153.4 KB (153385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa09f33f1e4c185a911cfd4dcd7d1dbbba5b9909fbe9100480230f1436457116`  
		Last Modified: Mon, 29 Sep 2025 23:59:01 GMT  
		Size: 2.3 MB (2275224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9a30963a9969bd789a111826840c0e97edd5d71548b548a30932bee7448fcc`  
		Last Modified: Mon, 29 Sep 2025 23:59:01 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ffdbd101cdb57f8b290f16ae4fa6106fd6ea85695fed7d08e98fdd19332d85`  
		Last Modified: Mon, 29 Sep 2025 23:59:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:573b95a8bb8dd5178978144dbd1446143419bbfc4edb099c6ebbe467c8e00b83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2a5e2b768012fff6837a6324e893b847c3948649e73a49b722b5d6b4b2d1f38`

```dockerfile
```

-	Layers:
	-	`sha256:8ab701ab9aad8acae756d96838becc2299738dcbdd81cb0071e6fbb5459b2f5b`  
		Last Modified: Tue, 30 Sep 2025 00:34:48 GMT  
		Size: 2.0 MB (2008496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71a37a40aa0845aeb88bc64f742dc25764c4824bedfe40f31b6f13e0bbd595b7`  
		Last Modified: Tue, 30 Sep 2025 00:34:48 GMT  
		Size: 22.4 KB (22393 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; 386

```console
$ docker pull memcached@sha256:0d993065ea1ed42de5bd4fcda3bafa779f274987bcb4d302b8a927344105ce6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33687876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fe2c39bed6edf857f276a7b8e77499f6c2110ebe12362143053acafdf31fba3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ab4c7760f4a4bda4b0797f3f0b56bd90b9778b76fc8351f2e1bd7c332b9dcc92`  
		Last Modified: Mon, 29 Sep 2025 23:35:33 GMT  
		Size: 31.3 MB (31294536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bcd1d82da4702bb3c598bb03b9d138dea8bd5e459160d5276b3fb8ebfb58923`  
		Last Modified: Mon, 29 Sep 2025 23:58:18 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ceba58f3514163ba75fa31b3b659efbe123eee61ee1e13161b71c6976b9cca2`  
		Last Modified: Mon, 29 Sep 2025 23:58:17 GMT  
		Size: 147.4 KB (147429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0453c4dd0d673c524b37cefb6f3412d20dde32e36c7999a26420bfb8481b0add`  
		Last Modified: Mon, 29 Sep 2025 23:58:18 GMT  
		Size: 2.2 MB (2244401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8916b29a59d03a745388da5e0a1aae97b201cd0e333de592e8a0fbe93da42b2f`  
		Last Modified: Mon, 29 Sep 2025 23:58:18 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28a35d7ac2cedad97d815d581ffa42e79c00126410603b586fb754ff264b578`  
		Last Modified: Mon, 29 Sep 2025 23:58:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:a1cbda14df44fff2e8baad5f7b53a3c32f617c55d96176326e107932e625e1d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef21897bb3061b8deedad86c30704928e376dad42a0a0bd9bdd946ff1cd46e37`

```dockerfile
```

-	Layers:
	-	`sha256:1f6010c4e760c848d7546664960f84f5082bc718d59b4dee6be3dc6489f1b283`  
		Last Modified: Tue, 30 Sep 2025 00:34:53 GMT  
		Size: 2.0 MB (2005337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f0fb1a46b98e7a2df02e226e82cd6854123a501d2d649bd70f05dbba8c4ffb7`  
		Last Modified: Tue, 30 Sep 2025 00:34:54 GMT  
		Size: 22.1 KB (22138 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; ppc64le

```console
$ docker pull memcached@sha256:78facd60957c01a0fc2c93514ec1f636e2acc585252bf3d2b224c9e4a2720751
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36187154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:078835e44984fd2f6238dc1bedb2dcc1eb3d45b38c738650295299276d8e3052`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1760918400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a9b4dd19a96be85b367998327f4288ed2fa8f174d1b3e8bea8ac7c2c626ec865`  
		Last Modified: Tue, 21 Oct 2025 00:26:55 GMT  
		Size: 33.6 MB (33598518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbed628a221d903400b8d49b4dc58aa0541e23d5a909543d626205670fd1072e`  
		Last Modified: Tue, 21 Oct 2025 01:54:52 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e748ebb38f38290596ca068f9f7e75e6c669eb4588462f2fe0b3566753e7f5`  
		Last Modified: Tue, 21 Oct 2025 01:54:53 GMT  
		Size: 170.3 KB (170257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b23f2908f85849ad3cfc2d526edf441cafb4862876c74e7c77fb5daeac7cc908`  
		Last Modified: Tue, 21 Oct 2025 01:54:53 GMT  
		Size: 2.4 MB (2416870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82d739662461ca129d2f470c2fa271c4962856a0f4a86f15d9469b59228c429`  
		Last Modified: Tue, 21 Oct 2025 01:54:52 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cefac88d4c183e05bebf79bdd2a0ad83aa10bbf75f4d809e74a8e7adb46146d`  
		Last Modified: Tue, 21 Oct 2025 01:54:53 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:766403e34da539f4d7944ceccfddc6817ff9a2e87659514dca52e26b77f14121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:093b6d02f98d1abdf2e4d567f2158cd54a22a08c01d42563dcd4d0f7a8d6121b`

```dockerfile
```

-	Layers:
	-	`sha256:89c9d8d8bddf968ee9f05171ddf674944ccf96d2c3df27dd2f5612e452da714e`  
		Last Modified: Tue, 21 Oct 2025 03:34:32 GMT  
		Size: 2.0 MB (2011835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72201c797f2648a5b0be16e7dc44930d3ddc214e2d4bc27d43cd6b923d85e481`  
		Last Modified: Tue, 21 Oct 2025 03:34:33 GMT  
		Size: 22.3 KB (22270 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; riscv64

```console
$ docker pull memcached@sha256:275951d176352ae7a6c07c3342e4a3696ed07e5711b47a3d3eac6d077943d7fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30629997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a439308e1f0b95ecea2e57b1abd7e75a6013568a1a7500b1f4d7bd0e21ad63`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6d1567708d42906165204f9177d357cb6a2fd51f758da447f1743b00813f892f`  
		Last Modified: Tue, 21 Oct 2025 00:37:37 GMT  
		Size: 28.3 MB (28275650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3633fd6545714a9d496af99598a2f2d1d149fd30ccb0af33ca4b5a64f2c80db2`  
		Last Modified: Tue, 21 Oct 2025 03:45:15 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0080b76dfc5efa9880c5885d69ca4cb830c2b81c8868038da6c3ec979f4df45f`  
		Last Modified: Tue, 21 Oct 2025 03:45:15 GMT  
		Size: 133.0 KB (132972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852a88ae8dfab39558e6bfca2ab58f39c01708aae430b3414e67d8fadc449694`  
		Last Modified: Tue, 21 Oct 2025 03:45:16 GMT  
		Size: 2.2 MB (2219861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a327b2de5a4375096f16800253786a6cfa67cce06f9f359b1c824e8232e98410`  
		Last Modified: Tue, 21 Oct 2025 03:45:15 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c933f2561e6f8e1189581b1eeb13dad69d7136a328a0533102686c15e68cb541`  
		Last Modified: Tue, 21 Oct 2025 03:45:15 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:7b68aaa7179e5972f8e6c99cbc3683f42653a9b4e71b3083cc76c60f88a4ecb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29ef9b8ffe7eed5ede85b59399c486af192d1744333cfa894153cffdf84ebefa`

```dockerfile
```

-	Layers:
	-	`sha256:861eae89f87c467092bc44440857f9d241e78153edc4d2e4fa84f83964fcbefe`  
		Last Modified: Tue, 21 Oct 2025 06:34:37 GMT  
		Size: 2.0 MB (2002198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7005598b4f28cfd2d5cfca73d6642c460d950449af439a25f8d87d7e8442aef6`  
		Last Modified: Tue, 21 Oct 2025 06:34:38 GMT  
		Size: 22.3 KB (22270 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; s390x

```console
$ docker pull memcached@sha256:97d22f11a028c8313d60f2b0d408dda8b2d48228b9b75aa2837e5463a793b535
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32292996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3e07eed38bed1a525726cbdc7874a25878c07feafb0bd683fe1f6583de2f83e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1759104000'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:924b0740f35a15fc20142be5c392f6b033c8051daecf16d2db38c22d6d73eb53`  
		Last Modified: Mon, 29 Sep 2025 23:41:29 GMT  
		Size: 29.8 MB (29837230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f51adc9bddc158c97c423c25020f779f6eaf1052b5377d27f3c426f6e1bfc021`  
		Last Modified: Tue, 30 Sep 2025 06:33:13 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e96b9e4bc41b016b366753e5d7d24d6ec0ad57f58fd33f9950ec9221297a8a4`  
		Last Modified: Tue, 30 Sep 2025 06:33:13 GMT  
		Size: 140.4 KB (140431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e41252907eabe8a9429031bb41587143d8a76355a4ec8726199ab91669e2ec3`  
		Last Modified: Tue, 30 Sep 2025 06:33:13 GMT  
		Size: 2.3 MB (2313824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2a41347a9c48966679d812976b6782615489e8d5f3d097e121b6150546f1cb`  
		Last Modified: Tue, 30 Sep 2025 06:33:13 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:969f1ab4db0027abb6561b0f8c35ae90cdfd2564247531bffcfb8860284b4319`  
		Last Modified: Tue, 30 Sep 2025 06:33:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:3f77e30f08514ef437bcf703e92082745153815200f728ce23b57a22ebbe9f84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0af62fcf07f143e611b564b8cdb2e08d11e05d8a8917d137e71fa925d6c936e4`

```dockerfile
```

-	Layers:
	-	`sha256:2db70adf2290adc880f8aa191f9e3b299c9dd28f01e3277a5386f4830c1f1f16`  
		Last Modified: Wed, 01 Oct 2025 21:34:44 GMT  
		Size: 2.0 MB (2009617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c002c1b0040529dcbb20761ae0b22e83c70cbf1d616626a80eff7eeccc02b1e6`  
		Last Modified: Wed, 01 Oct 2025 21:34:45 GMT  
		Size: 22.2 KB (22196 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.39`

```console
$ docker pull memcached@sha256:57f9012f8aaa9a257b51f39c4a0f30ba228430e5e3f7873e84d0eaa4c53cf0e3
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
$ docker pull memcached@sha256:b995c17f51fbc95ab650436bf004e0e08aac1e231a0c4ced640ba25409a53ab5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32209591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2ebce0923097e2ebc228b419829228444709a8f2168920008cde8f0aacd5f50`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:339cbfbe5560ff0c225f888ba7ae149a9ce0536968c1bcccc467ceea4e3b09a0`  
		Last Modified: Mon, 29 Sep 2025 23:53:01 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84637889c9320e34d3cc8375e48fdc43299460f2280a8b62690c6d78f6a1ccf0`  
		Last Modified: Mon, 29 Sep 2025 23:53:01 GMT  
		Size: 136.6 KB (136571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe788cc20223f97addb89c197bd5ea5d77c3bbe084b00e8dcb70731168abb3b`  
		Last Modified: Mon, 29 Sep 2025 23:53:02 GMT  
		Size: 2.3 MB (2293745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e090b148236c9a2470abf0308fbdf9c8ed3c23b04efdfb18e68f20902a2e2f36`  
		Last Modified: Mon, 29 Sep 2025 23:53:02 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93fa1d160038c361af454d4a8eb44b68dcda89fc415ad571b6e9707fb59a0082`  
		Last Modified: Mon, 29 Sep 2025 23:53:02 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39` - unknown; unknown

```console
$ docker pull memcached@sha256:5cd8c391814b8c7fbf65b5d657526c37f0516c6e4fe7dc245bfc347550a31200
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40690a93df6f911472221738e6595b6a746bd957d3bf1552c92ff83f17536644`

```dockerfile
```

-	Layers:
	-	`sha256:4b787171563846ab285584301f579a404cecd6f570a25225e02ff18939e29124`  
		Last Modified: Tue, 30 Sep 2025 00:34:34 GMT  
		Size: 2.0 MB (2008180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5a013035c58f0ea6bcc734d2c89618a0e98d1d8b3d3f07a169cd97b52bf4c0d`  
		Last Modified: Tue, 30 Sep 2025 00:34:35 GMT  
		Size: 22.2 KB (22196 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39` - linux; arm variant v5

```console
$ docker pull memcached@sha256:29d660bf29e180ab12efa8f4cdf6a974ec008d83e2c3c8ec051dee748eb9ed04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30319195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d982473f8bce68d8cb2795fc64f125c06b91ec37e8e238bf7464d2e1fdba6a1b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1760918400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:389bac9f76fa529ccf801fd7c9cb260ecee27d208221c25004185ab22936c4d4`  
		Last Modified: Tue, 21 Oct 2025 00:20:45 GMT  
		Size: 27.9 MB (27946283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed93883017eb3f4dde85524af233ee0b6e174c0abe1cef988e9bce8d5375e89`  
		Last Modified: Tue, 21 Oct 2025 01:23:33 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:791751af616e97272032619ddc7968fe23e71223657f52594fb2c62a2a47eda5`  
		Last Modified: Tue, 21 Oct 2025 01:23:33 GMT  
		Size: 144.0 KB (144045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5ea9c6e85cf6a029a9ba48b6b73a8dc6479d59392f254b1c2db7b1902074dd`  
		Last Modified: Tue, 21 Oct 2025 01:23:33 GMT  
		Size: 2.2 MB (2227357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a58aefd26c4b989c6b88d95adb3a6920797ab35bfccd55f1001d478ea7c38e`  
		Last Modified: Tue, 21 Oct 2025 01:23:33 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87cab310dfac01ff5304eeb4a6ea3ddebf9ab9ab7badd32bb16312e9ad5c22ae`  
		Last Modified: Tue, 21 Oct 2025 01:23:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39` - unknown; unknown

```console
$ docker pull memcached@sha256:63d0a43eb60f7ffb19e7cc876899b414f91eda292c74d1ecd4894dbc17394c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81a59c35b11c8306faf5db19cf7b6aee2213f889fcdcad2f2058c233038f5c2d`

```dockerfile
```

-	Layers:
	-	`sha256:b6117037dd5100454e92bb311823f69d718d18239a54c39029a154a68618f82b`  
		Last Modified: Tue, 21 Oct 2025 06:34:24 GMT  
		Size: 2.0 MB (2011237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfc7fdadb808663bde556e0343ab1151a3545e7211fe7e6e71915327352feedf`  
		Last Modified: Tue, 21 Oct 2025 06:34:25 GMT  
		Size: 22.3 KB (22346 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39` - linux; arm variant v7

```console
$ docker pull memcached@sha256:889cba709c7ad01fa2925b49389f4e73f9d759d8020c2a108aabd5a1b1f2ee95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28532153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56676dc32ecaa308b63acf0b41885c581e3700d44bc04a653a595327d4198c3a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1759104000'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0289e98159900b326d4cedde367bf225e25835a3ad879647f17f922e43cfa884`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 26.2 MB (26212758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c067599f6c6ba1a22613aa308e4d66e5249d6cc507b1229b6f4d482aecce8a6`  
		Last Modified: Tue, 30 Sep 2025 00:01:20 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cf0eec4f32f0da160c5e99bd0b57756034bb7093c545143caf6e310210cb44`  
		Last Modified: Tue, 30 Sep 2025 00:01:20 GMT  
		Size: 135.3 KB (135298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e59b4e18c59ebfcadada2142ce2be01e708dd3af20396b507979cf3a15f6f22`  
		Last Modified: Tue, 30 Sep 2025 00:01:20 GMT  
		Size: 2.2 MB (2182588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a24488f6b368fccedb9bb9614c2c525964ee0e3cc91e91d2b41f74b38a1c9a59`  
		Last Modified: Tue, 30 Sep 2025 00:01:20 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413fbe42e3bd71205a88a777ab5027fc34a2ad8053f6593d6653d72ae17ba8ff`  
		Last Modified: Tue, 30 Sep 2025 00:01:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39` - unknown; unknown

```console
$ docker pull memcached@sha256:ca8765c9f99276788e2b51ecfaf135680c03e0c222b9753d99dc4218bcc94095
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b6914431db285aeda4c9e27af56a106671c3541420f5b3bce905bed9f17ac6f`

```dockerfile
```

-	Layers:
	-	`sha256:fb1138fbff85001f5063fc6944faf0e66d26d9a179651b7a6b0c05c7f33a9240`  
		Last Modified: Tue, 30 Sep 2025 00:34:43 GMT  
		Size: 2.0 MB (2009640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c15f19f4d680266479069e896e888cb3a6a008b2f385c644c4f0baa61370937`  
		Last Modified: Tue, 30 Sep 2025 00:34:44 GMT  
		Size: 22.3 KB (22345 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:ef5cebc6723efc4307b7e2459b1b2c096013265dcfc93ee6e929dfb04399da59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32570960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b078c21daa3a3ef97cfc057882f396e936961312205c8e1a12712f179cf9f15`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c850e44210e9493ef7540c5c65cd48360355c3e6e94094c44d15af0045dc8dea`  
		Last Modified: Mon, 29 Sep 2025 23:59:01 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a741f1a1ae0d87da15466cd2dafd5acfb37dd72d94dda9656931ef24906d618`  
		Last Modified: Mon, 29 Sep 2025 23:59:01 GMT  
		Size: 153.4 KB (153385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa09f33f1e4c185a911cfd4dcd7d1dbbba5b9909fbe9100480230f1436457116`  
		Last Modified: Mon, 29 Sep 2025 23:59:01 GMT  
		Size: 2.3 MB (2275224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9a30963a9969bd789a111826840c0e97edd5d71548b548a30932bee7448fcc`  
		Last Modified: Mon, 29 Sep 2025 23:59:01 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ffdbd101cdb57f8b290f16ae4fa6106fd6ea85695fed7d08e98fdd19332d85`  
		Last Modified: Mon, 29 Sep 2025 23:59:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39` - unknown; unknown

```console
$ docker pull memcached@sha256:573b95a8bb8dd5178978144dbd1446143419bbfc4edb099c6ebbe467c8e00b83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2a5e2b768012fff6837a6324e893b847c3948649e73a49b722b5d6b4b2d1f38`

```dockerfile
```

-	Layers:
	-	`sha256:8ab701ab9aad8acae756d96838becc2299738dcbdd81cb0071e6fbb5459b2f5b`  
		Last Modified: Tue, 30 Sep 2025 00:34:48 GMT  
		Size: 2.0 MB (2008496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71a37a40aa0845aeb88bc64f742dc25764c4824bedfe40f31b6f13e0bbd595b7`  
		Last Modified: Tue, 30 Sep 2025 00:34:48 GMT  
		Size: 22.4 KB (22393 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39` - linux; 386

```console
$ docker pull memcached@sha256:0d993065ea1ed42de5bd4fcda3bafa779f274987bcb4d302b8a927344105ce6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33687876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fe2c39bed6edf857f276a7b8e77499f6c2110ebe12362143053acafdf31fba3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ab4c7760f4a4bda4b0797f3f0b56bd90b9778b76fc8351f2e1bd7c332b9dcc92`  
		Last Modified: Mon, 29 Sep 2025 23:35:33 GMT  
		Size: 31.3 MB (31294536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bcd1d82da4702bb3c598bb03b9d138dea8bd5e459160d5276b3fb8ebfb58923`  
		Last Modified: Mon, 29 Sep 2025 23:58:18 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ceba58f3514163ba75fa31b3b659efbe123eee61ee1e13161b71c6976b9cca2`  
		Last Modified: Mon, 29 Sep 2025 23:58:17 GMT  
		Size: 147.4 KB (147429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0453c4dd0d673c524b37cefb6f3412d20dde32e36c7999a26420bfb8481b0add`  
		Last Modified: Mon, 29 Sep 2025 23:58:18 GMT  
		Size: 2.2 MB (2244401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8916b29a59d03a745388da5e0a1aae97b201cd0e333de592e8a0fbe93da42b2f`  
		Last Modified: Mon, 29 Sep 2025 23:58:18 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28a35d7ac2cedad97d815d581ffa42e79c00126410603b586fb754ff264b578`  
		Last Modified: Mon, 29 Sep 2025 23:58:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39` - unknown; unknown

```console
$ docker pull memcached@sha256:a1cbda14df44fff2e8baad5f7b53a3c32f617c55d96176326e107932e625e1d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef21897bb3061b8deedad86c30704928e376dad42a0a0bd9bdd946ff1cd46e37`

```dockerfile
```

-	Layers:
	-	`sha256:1f6010c4e760c848d7546664960f84f5082bc718d59b4dee6be3dc6489f1b283`  
		Last Modified: Tue, 30 Sep 2025 00:34:53 GMT  
		Size: 2.0 MB (2005337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f0fb1a46b98e7a2df02e226e82cd6854123a501d2d649bd70f05dbba8c4ffb7`  
		Last Modified: Tue, 30 Sep 2025 00:34:54 GMT  
		Size: 22.1 KB (22138 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39` - linux; ppc64le

```console
$ docker pull memcached@sha256:78facd60957c01a0fc2c93514ec1f636e2acc585252bf3d2b224c9e4a2720751
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36187154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:078835e44984fd2f6238dc1bedb2dcc1eb3d45b38c738650295299276d8e3052`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1760918400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a9b4dd19a96be85b367998327f4288ed2fa8f174d1b3e8bea8ac7c2c626ec865`  
		Last Modified: Tue, 21 Oct 2025 00:26:55 GMT  
		Size: 33.6 MB (33598518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbed628a221d903400b8d49b4dc58aa0541e23d5a909543d626205670fd1072e`  
		Last Modified: Tue, 21 Oct 2025 01:54:52 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e748ebb38f38290596ca068f9f7e75e6c669eb4588462f2fe0b3566753e7f5`  
		Last Modified: Tue, 21 Oct 2025 01:54:53 GMT  
		Size: 170.3 KB (170257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b23f2908f85849ad3cfc2d526edf441cafb4862876c74e7c77fb5daeac7cc908`  
		Last Modified: Tue, 21 Oct 2025 01:54:53 GMT  
		Size: 2.4 MB (2416870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82d739662461ca129d2f470c2fa271c4962856a0f4a86f15d9469b59228c429`  
		Last Modified: Tue, 21 Oct 2025 01:54:52 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cefac88d4c183e05bebf79bdd2a0ad83aa10bbf75f4d809e74a8e7adb46146d`  
		Last Modified: Tue, 21 Oct 2025 01:54:53 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39` - unknown; unknown

```console
$ docker pull memcached@sha256:766403e34da539f4d7944ceccfddc6817ff9a2e87659514dca52e26b77f14121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:093b6d02f98d1abdf2e4d567f2158cd54a22a08c01d42563dcd4d0f7a8d6121b`

```dockerfile
```

-	Layers:
	-	`sha256:89c9d8d8bddf968ee9f05171ddf674944ccf96d2c3df27dd2f5612e452da714e`  
		Last Modified: Tue, 21 Oct 2025 03:34:32 GMT  
		Size: 2.0 MB (2011835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72201c797f2648a5b0be16e7dc44930d3ddc214e2d4bc27d43cd6b923d85e481`  
		Last Modified: Tue, 21 Oct 2025 03:34:33 GMT  
		Size: 22.3 KB (22270 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39` - linux; riscv64

```console
$ docker pull memcached@sha256:275951d176352ae7a6c07c3342e4a3696ed07e5711b47a3d3eac6d077943d7fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30629997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a439308e1f0b95ecea2e57b1abd7e75a6013568a1a7500b1f4d7bd0e21ad63`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6d1567708d42906165204f9177d357cb6a2fd51f758da447f1743b00813f892f`  
		Last Modified: Tue, 21 Oct 2025 00:37:37 GMT  
		Size: 28.3 MB (28275650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3633fd6545714a9d496af99598a2f2d1d149fd30ccb0af33ca4b5a64f2c80db2`  
		Last Modified: Tue, 21 Oct 2025 03:45:15 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0080b76dfc5efa9880c5885d69ca4cb830c2b81c8868038da6c3ec979f4df45f`  
		Last Modified: Tue, 21 Oct 2025 03:45:15 GMT  
		Size: 133.0 KB (132972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852a88ae8dfab39558e6bfca2ab58f39c01708aae430b3414e67d8fadc449694`  
		Last Modified: Tue, 21 Oct 2025 03:45:16 GMT  
		Size: 2.2 MB (2219861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a327b2de5a4375096f16800253786a6cfa67cce06f9f359b1c824e8232e98410`  
		Last Modified: Tue, 21 Oct 2025 03:45:15 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c933f2561e6f8e1189581b1eeb13dad69d7136a328a0533102686c15e68cb541`  
		Last Modified: Tue, 21 Oct 2025 03:45:15 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39` - unknown; unknown

```console
$ docker pull memcached@sha256:7b68aaa7179e5972f8e6c99cbc3683f42653a9b4e71b3083cc76c60f88a4ecb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29ef9b8ffe7eed5ede85b59399c486af192d1744333cfa894153cffdf84ebefa`

```dockerfile
```

-	Layers:
	-	`sha256:861eae89f87c467092bc44440857f9d241e78153edc4d2e4fa84f83964fcbefe`  
		Last Modified: Tue, 21 Oct 2025 06:34:37 GMT  
		Size: 2.0 MB (2002198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7005598b4f28cfd2d5cfca73d6642c460d950449af439a25f8d87d7e8442aef6`  
		Last Modified: Tue, 21 Oct 2025 06:34:38 GMT  
		Size: 22.3 KB (22270 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39` - linux; s390x

```console
$ docker pull memcached@sha256:a95b2e7570fb1eb02135de63cbeb215972274a84b11c12a7d04ddd9bf3de6580
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32293114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f610e90f96aca46738207b5db8f23d66eed6872283b54d92dde496a989b7f243`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1760918400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:71dc03f1fd788f9fc2bbb931d3df17cbfaf0b486bdfb19f4e3b8792a206689a1`  
		Last Modified: Tue, 21 Oct 2025 00:28:26 GMT  
		Size: 29.8 MB (29837255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44dbc4c5c53013685d3377712d0c9bd7329733dedc975c104d595400ddeeb391`  
		Last Modified: Tue, 21 Oct 2025 01:46:14 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d288eee322878a4d9b6704cf2a6236f438b9daf19ed5c560df6dada549f626ed`  
		Last Modified: Tue, 21 Oct 2025 01:46:14 GMT  
		Size: 140.4 KB (140414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b326506421aba244d885b71cac80630fae5007fa91bb31cf73833ecf9c65780f`  
		Last Modified: Tue, 21 Oct 2025 01:46:15 GMT  
		Size: 2.3 MB (2313938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3db2ecc57bcb619c401fee1fa916699e8438d831d041c30b7e5c73a309fcb53`  
		Last Modified: Tue, 21 Oct 2025 01:46:14 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa6c6a0d8a512cc17edee286e08a2dc681ae4f5e2201c80276a59aa1b620211`  
		Last Modified: Tue, 21 Oct 2025 01:46:14 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39` - unknown; unknown

```console
$ docker pull memcached@sha256:292e311306fc3d99b24163db180bc4eb533d4d4d75b4e27ee449e3f1cfff375c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6319ea5d7c1da5cbd85ce121aa089b5180f71099c90a0bc6bee007bca4c54a3f`

```dockerfile
```

-	Layers:
	-	`sha256:753a01ea8cebac86c44ad769ec101f1c2bb7ab2707522a32a76b34602461944a`  
		Last Modified: Tue, 21 Oct 2025 06:35:00 GMT  
		Size: 2.0 MB (2009671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7625599bd4983e6cdf9a43b3cbd69a4b2037e083333c420fb05a396cb2e48231`  
		Last Modified: Tue, 21 Oct 2025 06:35:01 GMT  
		Size: 22.2 KB (22196 bytes)  
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
$ docker pull memcached@sha256:302493fd5e802f3bad0b33d2dc1db60e026fc16a1e43a758bdc3e769218f3f44
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
$ docker pull memcached@sha256:b995c17f51fbc95ab650436bf004e0e08aac1e231a0c4ced640ba25409a53ab5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32209591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2ebce0923097e2ebc228b419829228444709a8f2168920008cde8f0aacd5f50`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:339cbfbe5560ff0c225f888ba7ae149a9ce0536968c1bcccc467ceea4e3b09a0`  
		Last Modified: Mon, 29 Sep 2025 23:53:01 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84637889c9320e34d3cc8375e48fdc43299460f2280a8b62690c6d78f6a1ccf0`  
		Last Modified: Mon, 29 Sep 2025 23:53:01 GMT  
		Size: 136.6 KB (136571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe788cc20223f97addb89c197bd5ea5d77c3bbe084b00e8dcb70731168abb3b`  
		Last Modified: Mon, 29 Sep 2025 23:53:02 GMT  
		Size: 2.3 MB (2293745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e090b148236c9a2470abf0308fbdf9c8ed3c23b04efdfb18e68f20902a2e2f36`  
		Last Modified: Mon, 29 Sep 2025 23:53:02 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93fa1d160038c361af454d4a8eb44b68dcda89fc415ad571b6e9707fb59a0082`  
		Last Modified: Mon, 29 Sep 2025 23:53:02 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:5cd8c391814b8c7fbf65b5d657526c37f0516c6e4fe7dc245bfc347550a31200
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40690a93df6f911472221738e6595b6a746bd957d3bf1552c92ff83f17536644`

```dockerfile
```

-	Layers:
	-	`sha256:4b787171563846ab285584301f579a404cecd6f570a25225e02ff18939e29124`  
		Last Modified: Tue, 30 Sep 2025 00:34:34 GMT  
		Size: 2.0 MB (2008180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5a013035c58f0ea6bcc734d2c89618a0e98d1d8b3d3f07a169cd97b52bf4c0d`  
		Last Modified: Tue, 30 Sep 2025 00:34:35 GMT  
		Size: 22.2 KB (22196 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-trixie` - linux; arm variant v5

```console
$ docker pull memcached@sha256:29d660bf29e180ab12efa8f4cdf6a974ec008d83e2c3c8ec051dee748eb9ed04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30319195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d982473f8bce68d8cb2795fc64f125c06b91ec37e8e238bf7464d2e1fdba6a1b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1760918400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:389bac9f76fa529ccf801fd7c9cb260ecee27d208221c25004185ab22936c4d4`  
		Last Modified: Tue, 21 Oct 2025 00:20:45 GMT  
		Size: 27.9 MB (27946283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed93883017eb3f4dde85524af233ee0b6e174c0abe1cef988e9bce8d5375e89`  
		Last Modified: Tue, 21 Oct 2025 01:23:33 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:791751af616e97272032619ddc7968fe23e71223657f52594fb2c62a2a47eda5`  
		Last Modified: Tue, 21 Oct 2025 01:23:33 GMT  
		Size: 144.0 KB (144045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5ea9c6e85cf6a029a9ba48b6b73a8dc6479d59392f254b1c2db7b1902074dd`  
		Last Modified: Tue, 21 Oct 2025 01:23:33 GMT  
		Size: 2.2 MB (2227357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a58aefd26c4b989c6b88d95adb3a6920797ab35bfccd55f1001d478ea7c38e`  
		Last Modified: Tue, 21 Oct 2025 01:23:33 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87cab310dfac01ff5304eeb4a6ea3ddebf9ab9ab7badd32bb16312e9ad5c22ae`  
		Last Modified: Tue, 21 Oct 2025 01:23:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:63d0a43eb60f7ffb19e7cc876899b414f91eda292c74d1ecd4894dbc17394c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81a59c35b11c8306faf5db19cf7b6aee2213f889fcdcad2f2058c233038f5c2d`

```dockerfile
```

-	Layers:
	-	`sha256:b6117037dd5100454e92bb311823f69d718d18239a54c39029a154a68618f82b`  
		Last Modified: Tue, 21 Oct 2025 06:34:24 GMT  
		Size: 2.0 MB (2011237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfc7fdadb808663bde556e0343ab1151a3545e7211fe7e6e71915327352feedf`  
		Last Modified: Tue, 21 Oct 2025 06:34:25 GMT  
		Size: 22.3 KB (22346 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-trixie` - linux; arm variant v7

```console
$ docker pull memcached@sha256:889cba709c7ad01fa2925b49389f4e73f9d759d8020c2a108aabd5a1b1f2ee95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28532153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56676dc32ecaa308b63acf0b41885c581e3700d44bc04a653a595327d4198c3a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1759104000'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0289e98159900b326d4cedde367bf225e25835a3ad879647f17f922e43cfa884`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 26.2 MB (26212758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c067599f6c6ba1a22613aa308e4d66e5249d6cc507b1229b6f4d482aecce8a6`  
		Last Modified: Tue, 30 Sep 2025 00:01:20 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cf0eec4f32f0da160c5e99bd0b57756034bb7093c545143caf6e310210cb44`  
		Last Modified: Tue, 30 Sep 2025 00:01:20 GMT  
		Size: 135.3 KB (135298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e59b4e18c59ebfcadada2142ce2be01e708dd3af20396b507979cf3a15f6f22`  
		Last Modified: Tue, 30 Sep 2025 00:01:20 GMT  
		Size: 2.2 MB (2182588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a24488f6b368fccedb9bb9614c2c525964ee0e3cc91e91d2b41f74b38a1c9a59`  
		Last Modified: Tue, 30 Sep 2025 00:01:20 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413fbe42e3bd71205a88a777ab5027fc34a2ad8053f6593d6653d72ae17ba8ff`  
		Last Modified: Tue, 30 Sep 2025 00:01:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:ca8765c9f99276788e2b51ecfaf135680c03e0c222b9753d99dc4218bcc94095
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b6914431db285aeda4c9e27af56a106671c3541420f5b3bce905bed9f17ac6f`

```dockerfile
```

-	Layers:
	-	`sha256:fb1138fbff85001f5063fc6944faf0e66d26d9a179651b7a6b0c05c7f33a9240`  
		Last Modified: Tue, 30 Sep 2025 00:34:43 GMT  
		Size: 2.0 MB (2009640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c15f19f4d680266479069e896e888cb3a6a008b2f385c644c4f0baa61370937`  
		Last Modified: Tue, 30 Sep 2025 00:34:44 GMT  
		Size: 22.3 KB (22345 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-trixie` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:ef5cebc6723efc4307b7e2459b1b2c096013265dcfc93ee6e929dfb04399da59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32570960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b078c21daa3a3ef97cfc057882f396e936961312205c8e1a12712f179cf9f15`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c850e44210e9493ef7540c5c65cd48360355c3e6e94094c44d15af0045dc8dea`  
		Last Modified: Mon, 29 Sep 2025 23:59:01 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a741f1a1ae0d87da15466cd2dafd5acfb37dd72d94dda9656931ef24906d618`  
		Last Modified: Mon, 29 Sep 2025 23:59:01 GMT  
		Size: 153.4 KB (153385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa09f33f1e4c185a911cfd4dcd7d1dbbba5b9909fbe9100480230f1436457116`  
		Last Modified: Mon, 29 Sep 2025 23:59:01 GMT  
		Size: 2.3 MB (2275224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9a30963a9969bd789a111826840c0e97edd5d71548b548a30932bee7448fcc`  
		Last Modified: Mon, 29 Sep 2025 23:59:01 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ffdbd101cdb57f8b290f16ae4fa6106fd6ea85695fed7d08e98fdd19332d85`  
		Last Modified: Mon, 29 Sep 2025 23:59:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:573b95a8bb8dd5178978144dbd1446143419bbfc4edb099c6ebbe467c8e00b83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2a5e2b768012fff6837a6324e893b847c3948649e73a49b722b5d6b4b2d1f38`

```dockerfile
```

-	Layers:
	-	`sha256:8ab701ab9aad8acae756d96838becc2299738dcbdd81cb0071e6fbb5459b2f5b`  
		Last Modified: Tue, 30 Sep 2025 00:34:48 GMT  
		Size: 2.0 MB (2008496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71a37a40aa0845aeb88bc64f742dc25764c4824bedfe40f31b6f13e0bbd595b7`  
		Last Modified: Tue, 30 Sep 2025 00:34:48 GMT  
		Size: 22.4 KB (22393 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-trixie` - linux; 386

```console
$ docker pull memcached@sha256:0d993065ea1ed42de5bd4fcda3bafa779f274987bcb4d302b8a927344105ce6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33687876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fe2c39bed6edf857f276a7b8e77499f6c2110ebe12362143053acafdf31fba3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ab4c7760f4a4bda4b0797f3f0b56bd90b9778b76fc8351f2e1bd7c332b9dcc92`  
		Last Modified: Mon, 29 Sep 2025 23:35:33 GMT  
		Size: 31.3 MB (31294536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bcd1d82da4702bb3c598bb03b9d138dea8bd5e459160d5276b3fb8ebfb58923`  
		Last Modified: Mon, 29 Sep 2025 23:58:18 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ceba58f3514163ba75fa31b3b659efbe123eee61ee1e13161b71c6976b9cca2`  
		Last Modified: Mon, 29 Sep 2025 23:58:17 GMT  
		Size: 147.4 KB (147429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0453c4dd0d673c524b37cefb6f3412d20dde32e36c7999a26420bfb8481b0add`  
		Last Modified: Mon, 29 Sep 2025 23:58:18 GMT  
		Size: 2.2 MB (2244401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8916b29a59d03a745388da5e0a1aae97b201cd0e333de592e8a0fbe93da42b2f`  
		Last Modified: Mon, 29 Sep 2025 23:58:18 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28a35d7ac2cedad97d815d581ffa42e79c00126410603b586fb754ff264b578`  
		Last Modified: Mon, 29 Sep 2025 23:58:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:a1cbda14df44fff2e8baad5f7b53a3c32f617c55d96176326e107932e625e1d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef21897bb3061b8deedad86c30704928e376dad42a0a0bd9bdd946ff1cd46e37`

```dockerfile
```

-	Layers:
	-	`sha256:1f6010c4e760c848d7546664960f84f5082bc718d59b4dee6be3dc6489f1b283`  
		Last Modified: Tue, 30 Sep 2025 00:34:53 GMT  
		Size: 2.0 MB (2005337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f0fb1a46b98e7a2df02e226e82cd6854123a501d2d649bd70f05dbba8c4ffb7`  
		Last Modified: Tue, 30 Sep 2025 00:34:54 GMT  
		Size: 22.1 KB (22138 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-trixie` - linux; ppc64le

```console
$ docker pull memcached@sha256:78facd60957c01a0fc2c93514ec1f636e2acc585252bf3d2b224c9e4a2720751
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36187154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:078835e44984fd2f6238dc1bedb2dcc1eb3d45b38c738650295299276d8e3052`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1760918400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a9b4dd19a96be85b367998327f4288ed2fa8f174d1b3e8bea8ac7c2c626ec865`  
		Last Modified: Tue, 21 Oct 2025 00:26:55 GMT  
		Size: 33.6 MB (33598518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbed628a221d903400b8d49b4dc58aa0541e23d5a909543d626205670fd1072e`  
		Last Modified: Tue, 21 Oct 2025 01:54:52 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e748ebb38f38290596ca068f9f7e75e6c669eb4588462f2fe0b3566753e7f5`  
		Last Modified: Tue, 21 Oct 2025 01:54:53 GMT  
		Size: 170.3 KB (170257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b23f2908f85849ad3cfc2d526edf441cafb4862876c74e7c77fb5daeac7cc908`  
		Last Modified: Tue, 21 Oct 2025 01:54:53 GMT  
		Size: 2.4 MB (2416870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82d739662461ca129d2f470c2fa271c4962856a0f4a86f15d9469b59228c429`  
		Last Modified: Tue, 21 Oct 2025 01:54:52 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cefac88d4c183e05bebf79bdd2a0ad83aa10bbf75f4d809e74a8e7adb46146d`  
		Last Modified: Tue, 21 Oct 2025 01:54:53 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:766403e34da539f4d7944ceccfddc6817ff9a2e87659514dca52e26b77f14121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:093b6d02f98d1abdf2e4d567f2158cd54a22a08c01d42563dcd4d0f7a8d6121b`

```dockerfile
```

-	Layers:
	-	`sha256:89c9d8d8bddf968ee9f05171ddf674944ccf96d2c3df27dd2f5612e452da714e`  
		Last Modified: Tue, 21 Oct 2025 03:34:32 GMT  
		Size: 2.0 MB (2011835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72201c797f2648a5b0be16e7dc44930d3ddc214e2d4bc27d43cd6b923d85e481`  
		Last Modified: Tue, 21 Oct 2025 03:34:33 GMT  
		Size: 22.3 KB (22270 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-trixie` - linux; riscv64

```console
$ docker pull memcached@sha256:275951d176352ae7a6c07c3342e4a3696ed07e5711b47a3d3eac6d077943d7fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30629997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a439308e1f0b95ecea2e57b1abd7e75a6013568a1a7500b1f4d7bd0e21ad63`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6d1567708d42906165204f9177d357cb6a2fd51f758da447f1743b00813f892f`  
		Last Modified: Tue, 21 Oct 2025 00:37:37 GMT  
		Size: 28.3 MB (28275650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3633fd6545714a9d496af99598a2f2d1d149fd30ccb0af33ca4b5a64f2c80db2`  
		Last Modified: Tue, 21 Oct 2025 03:45:15 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0080b76dfc5efa9880c5885d69ca4cb830c2b81c8868038da6c3ec979f4df45f`  
		Last Modified: Tue, 21 Oct 2025 03:45:15 GMT  
		Size: 133.0 KB (132972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852a88ae8dfab39558e6bfca2ab58f39c01708aae430b3414e67d8fadc449694`  
		Last Modified: Tue, 21 Oct 2025 03:45:16 GMT  
		Size: 2.2 MB (2219861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a327b2de5a4375096f16800253786a6cfa67cce06f9f359b1c824e8232e98410`  
		Last Modified: Tue, 21 Oct 2025 03:45:15 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c933f2561e6f8e1189581b1eeb13dad69d7136a328a0533102686c15e68cb541`  
		Last Modified: Tue, 21 Oct 2025 03:45:15 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:7b68aaa7179e5972f8e6c99cbc3683f42653a9b4e71b3083cc76c60f88a4ecb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29ef9b8ffe7eed5ede85b59399c486af192d1744333cfa894153cffdf84ebefa`

```dockerfile
```

-	Layers:
	-	`sha256:861eae89f87c467092bc44440857f9d241e78153edc4d2e4fa84f83964fcbefe`  
		Last Modified: Tue, 21 Oct 2025 06:34:37 GMT  
		Size: 2.0 MB (2002198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7005598b4f28cfd2d5cfca73d6642c460d950449af439a25f8d87d7e8442aef6`  
		Last Modified: Tue, 21 Oct 2025 06:34:38 GMT  
		Size: 22.3 KB (22270 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-trixie` - linux; s390x

```console
$ docker pull memcached@sha256:97d22f11a028c8313d60f2b0d408dda8b2d48228b9b75aa2837e5463a793b535
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32292996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3e07eed38bed1a525726cbdc7874a25878c07feafb0bd683fe1f6583de2f83e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1759104000'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:924b0740f35a15fc20142be5c392f6b033c8051daecf16d2db38c22d6d73eb53`  
		Last Modified: Mon, 29 Sep 2025 23:41:29 GMT  
		Size: 29.8 MB (29837230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f51adc9bddc158c97c423c25020f779f6eaf1052b5377d27f3c426f6e1bfc021`  
		Last Modified: Tue, 30 Sep 2025 06:33:13 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e96b9e4bc41b016b366753e5d7d24d6ec0ad57f58fd33f9950ec9221297a8a4`  
		Last Modified: Tue, 30 Sep 2025 06:33:13 GMT  
		Size: 140.4 KB (140431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e41252907eabe8a9429031bb41587143d8a76355a4ec8726199ab91669e2ec3`  
		Last Modified: Tue, 30 Sep 2025 06:33:13 GMT  
		Size: 2.3 MB (2313824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2a41347a9c48966679d812976b6782615489e8d5f3d097e121b6150546f1cb`  
		Last Modified: Tue, 30 Sep 2025 06:33:13 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:969f1ab4db0027abb6561b0f8c35ae90cdfd2564247531bffcfb8860284b4319`  
		Last Modified: Tue, 30 Sep 2025 06:33:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:3f77e30f08514ef437bcf703e92082745153815200f728ce23b57a22ebbe9f84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0af62fcf07f143e611b564b8cdb2e08d11e05d8a8917d137e71fa925d6c936e4`

```dockerfile
```

-	Layers:
	-	`sha256:2db70adf2290adc880f8aa191f9e3b299c9dd28f01e3277a5386f4830c1f1f16`  
		Last Modified: Wed, 01 Oct 2025 21:34:44 GMT  
		Size: 2.0 MB (2009617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c002c1b0040529dcbb20761ae0b22e83c70cbf1d616626a80eff7eeccc02b1e6`  
		Last Modified: Wed, 01 Oct 2025 21:34:45 GMT  
		Size: 22.2 KB (22196 bytes)  
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
$ docker pull memcached@sha256:302493fd5e802f3bad0b33d2dc1db60e026fc16a1e43a758bdc3e769218f3f44
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
$ docker pull memcached@sha256:b995c17f51fbc95ab650436bf004e0e08aac1e231a0c4ced640ba25409a53ab5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32209591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2ebce0923097e2ebc228b419829228444709a8f2168920008cde8f0aacd5f50`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:339cbfbe5560ff0c225f888ba7ae149a9ce0536968c1bcccc467ceea4e3b09a0`  
		Last Modified: Mon, 29 Sep 2025 23:53:01 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84637889c9320e34d3cc8375e48fdc43299460f2280a8b62690c6d78f6a1ccf0`  
		Last Modified: Mon, 29 Sep 2025 23:53:01 GMT  
		Size: 136.6 KB (136571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe788cc20223f97addb89c197bd5ea5d77c3bbe084b00e8dcb70731168abb3b`  
		Last Modified: Mon, 29 Sep 2025 23:53:02 GMT  
		Size: 2.3 MB (2293745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e090b148236c9a2470abf0308fbdf9c8ed3c23b04efdfb18e68f20902a2e2f36`  
		Last Modified: Mon, 29 Sep 2025 23:53:02 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93fa1d160038c361af454d4a8eb44b68dcda89fc415ad571b6e9707fb59a0082`  
		Last Modified: Mon, 29 Sep 2025 23:53:02 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:5cd8c391814b8c7fbf65b5d657526c37f0516c6e4fe7dc245bfc347550a31200
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40690a93df6f911472221738e6595b6a746bd957d3bf1552c92ff83f17536644`

```dockerfile
```

-	Layers:
	-	`sha256:4b787171563846ab285584301f579a404cecd6f570a25225e02ff18939e29124`  
		Last Modified: Tue, 30 Sep 2025 00:34:34 GMT  
		Size: 2.0 MB (2008180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5a013035c58f0ea6bcc734d2c89618a0e98d1d8b3d3f07a169cd97b52bf4c0d`  
		Last Modified: Tue, 30 Sep 2025 00:34:35 GMT  
		Size: 22.2 KB (22196 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm variant v5

```console
$ docker pull memcached@sha256:29d660bf29e180ab12efa8f4cdf6a974ec008d83e2c3c8ec051dee748eb9ed04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30319195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d982473f8bce68d8cb2795fc64f125c06b91ec37e8e238bf7464d2e1fdba6a1b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1760918400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:389bac9f76fa529ccf801fd7c9cb260ecee27d208221c25004185ab22936c4d4`  
		Last Modified: Tue, 21 Oct 2025 00:20:45 GMT  
		Size: 27.9 MB (27946283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed93883017eb3f4dde85524af233ee0b6e174c0abe1cef988e9bce8d5375e89`  
		Last Modified: Tue, 21 Oct 2025 01:23:33 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:791751af616e97272032619ddc7968fe23e71223657f52594fb2c62a2a47eda5`  
		Last Modified: Tue, 21 Oct 2025 01:23:33 GMT  
		Size: 144.0 KB (144045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5ea9c6e85cf6a029a9ba48b6b73a8dc6479d59392f254b1c2db7b1902074dd`  
		Last Modified: Tue, 21 Oct 2025 01:23:33 GMT  
		Size: 2.2 MB (2227357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a58aefd26c4b989c6b88d95adb3a6920797ab35bfccd55f1001d478ea7c38e`  
		Last Modified: Tue, 21 Oct 2025 01:23:33 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87cab310dfac01ff5304eeb4a6ea3ddebf9ab9ab7badd32bb16312e9ad5c22ae`  
		Last Modified: Tue, 21 Oct 2025 01:23:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:63d0a43eb60f7ffb19e7cc876899b414f91eda292c74d1ecd4894dbc17394c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81a59c35b11c8306faf5db19cf7b6aee2213f889fcdcad2f2058c233038f5c2d`

```dockerfile
```

-	Layers:
	-	`sha256:b6117037dd5100454e92bb311823f69d718d18239a54c39029a154a68618f82b`  
		Last Modified: Tue, 21 Oct 2025 06:34:24 GMT  
		Size: 2.0 MB (2011237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfc7fdadb808663bde556e0343ab1151a3545e7211fe7e6e71915327352feedf`  
		Last Modified: Tue, 21 Oct 2025 06:34:25 GMT  
		Size: 22.3 KB (22346 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm variant v7

```console
$ docker pull memcached@sha256:889cba709c7ad01fa2925b49389f4e73f9d759d8020c2a108aabd5a1b1f2ee95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28532153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56676dc32ecaa308b63acf0b41885c581e3700d44bc04a653a595327d4198c3a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1759104000'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0289e98159900b326d4cedde367bf225e25835a3ad879647f17f922e43cfa884`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 26.2 MB (26212758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c067599f6c6ba1a22613aa308e4d66e5249d6cc507b1229b6f4d482aecce8a6`  
		Last Modified: Tue, 30 Sep 2025 00:01:20 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cf0eec4f32f0da160c5e99bd0b57756034bb7093c545143caf6e310210cb44`  
		Last Modified: Tue, 30 Sep 2025 00:01:20 GMT  
		Size: 135.3 KB (135298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e59b4e18c59ebfcadada2142ce2be01e708dd3af20396b507979cf3a15f6f22`  
		Last Modified: Tue, 30 Sep 2025 00:01:20 GMT  
		Size: 2.2 MB (2182588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a24488f6b368fccedb9bb9614c2c525964ee0e3cc91e91d2b41f74b38a1c9a59`  
		Last Modified: Tue, 30 Sep 2025 00:01:20 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413fbe42e3bd71205a88a777ab5027fc34a2ad8053f6593d6653d72ae17ba8ff`  
		Last Modified: Tue, 30 Sep 2025 00:01:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:ca8765c9f99276788e2b51ecfaf135680c03e0c222b9753d99dc4218bcc94095
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b6914431db285aeda4c9e27af56a106671c3541420f5b3bce905bed9f17ac6f`

```dockerfile
```

-	Layers:
	-	`sha256:fb1138fbff85001f5063fc6944faf0e66d26d9a179651b7a6b0c05c7f33a9240`  
		Last Modified: Tue, 30 Sep 2025 00:34:43 GMT  
		Size: 2.0 MB (2009640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c15f19f4d680266479069e896e888cb3a6a008b2f385c644c4f0baa61370937`  
		Last Modified: Tue, 30 Sep 2025 00:34:44 GMT  
		Size: 22.3 KB (22345 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:ef5cebc6723efc4307b7e2459b1b2c096013265dcfc93ee6e929dfb04399da59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32570960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b078c21daa3a3ef97cfc057882f396e936961312205c8e1a12712f179cf9f15`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c850e44210e9493ef7540c5c65cd48360355c3e6e94094c44d15af0045dc8dea`  
		Last Modified: Mon, 29 Sep 2025 23:59:01 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a741f1a1ae0d87da15466cd2dafd5acfb37dd72d94dda9656931ef24906d618`  
		Last Modified: Mon, 29 Sep 2025 23:59:01 GMT  
		Size: 153.4 KB (153385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa09f33f1e4c185a911cfd4dcd7d1dbbba5b9909fbe9100480230f1436457116`  
		Last Modified: Mon, 29 Sep 2025 23:59:01 GMT  
		Size: 2.3 MB (2275224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9a30963a9969bd789a111826840c0e97edd5d71548b548a30932bee7448fcc`  
		Last Modified: Mon, 29 Sep 2025 23:59:01 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ffdbd101cdb57f8b290f16ae4fa6106fd6ea85695fed7d08e98fdd19332d85`  
		Last Modified: Mon, 29 Sep 2025 23:59:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:573b95a8bb8dd5178978144dbd1446143419bbfc4edb099c6ebbe467c8e00b83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2a5e2b768012fff6837a6324e893b847c3948649e73a49b722b5d6b4b2d1f38`

```dockerfile
```

-	Layers:
	-	`sha256:8ab701ab9aad8acae756d96838becc2299738dcbdd81cb0071e6fbb5459b2f5b`  
		Last Modified: Tue, 30 Sep 2025 00:34:48 GMT  
		Size: 2.0 MB (2008496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71a37a40aa0845aeb88bc64f742dc25764c4824bedfe40f31b6f13e0bbd595b7`  
		Last Modified: Tue, 30 Sep 2025 00:34:48 GMT  
		Size: 22.4 KB (22393 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; 386

```console
$ docker pull memcached@sha256:0d993065ea1ed42de5bd4fcda3bafa779f274987bcb4d302b8a927344105ce6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33687876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fe2c39bed6edf857f276a7b8e77499f6c2110ebe12362143053acafdf31fba3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ab4c7760f4a4bda4b0797f3f0b56bd90b9778b76fc8351f2e1bd7c332b9dcc92`  
		Last Modified: Mon, 29 Sep 2025 23:35:33 GMT  
		Size: 31.3 MB (31294536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bcd1d82da4702bb3c598bb03b9d138dea8bd5e459160d5276b3fb8ebfb58923`  
		Last Modified: Mon, 29 Sep 2025 23:58:18 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ceba58f3514163ba75fa31b3b659efbe123eee61ee1e13161b71c6976b9cca2`  
		Last Modified: Mon, 29 Sep 2025 23:58:17 GMT  
		Size: 147.4 KB (147429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0453c4dd0d673c524b37cefb6f3412d20dde32e36c7999a26420bfb8481b0add`  
		Last Modified: Mon, 29 Sep 2025 23:58:18 GMT  
		Size: 2.2 MB (2244401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8916b29a59d03a745388da5e0a1aae97b201cd0e333de592e8a0fbe93da42b2f`  
		Last Modified: Mon, 29 Sep 2025 23:58:18 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28a35d7ac2cedad97d815d581ffa42e79c00126410603b586fb754ff264b578`  
		Last Modified: Mon, 29 Sep 2025 23:58:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:a1cbda14df44fff2e8baad5f7b53a3c32f617c55d96176326e107932e625e1d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef21897bb3061b8deedad86c30704928e376dad42a0a0bd9bdd946ff1cd46e37`

```dockerfile
```

-	Layers:
	-	`sha256:1f6010c4e760c848d7546664960f84f5082bc718d59b4dee6be3dc6489f1b283`  
		Last Modified: Tue, 30 Sep 2025 00:34:53 GMT  
		Size: 2.0 MB (2005337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f0fb1a46b98e7a2df02e226e82cd6854123a501d2d649bd70f05dbba8c4ffb7`  
		Last Modified: Tue, 30 Sep 2025 00:34:54 GMT  
		Size: 22.1 KB (22138 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; ppc64le

```console
$ docker pull memcached@sha256:78facd60957c01a0fc2c93514ec1f636e2acc585252bf3d2b224c9e4a2720751
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36187154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:078835e44984fd2f6238dc1bedb2dcc1eb3d45b38c738650295299276d8e3052`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1760918400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a9b4dd19a96be85b367998327f4288ed2fa8f174d1b3e8bea8ac7c2c626ec865`  
		Last Modified: Tue, 21 Oct 2025 00:26:55 GMT  
		Size: 33.6 MB (33598518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbed628a221d903400b8d49b4dc58aa0541e23d5a909543d626205670fd1072e`  
		Last Modified: Tue, 21 Oct 2025 01:54:52 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e748ebb38f38290596ca068f9f7e75e6c669eb4588462f2fe0b3566753e7f5`  
		Last Modified: Tue, 21 Oct 2025 01:54:53 GMT  
		Size: 170.3 KB (170257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b23f2908f85849ad3cfc2d526edf441cafb4862876c74e7c77fb5daeac7cc908`  
		Last Modified: Tue, 21 Oct 2025 01:54:53 GMT  
		Size: 2.4 MB (2416870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82d739662461ca129d2f470c2fa271c4962856a0f4a86f15d9469b59228c429`  
		Last Modified: Tue, 21 Oct 2025 01:54:52 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cefac88d4c183e05bebf79bdd2a0ad83aa10bbf75f4d809e74a8e7adb46146d`  
		Last Modified: Tue, 21 Oct 2025 01:54:53 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:766403e34da539f4d7944ceccfddc6817ff9a2e87659514dca52e26b77f14121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:093b6d02f98d1abdf2e4d567f2158cd54a22a08c01d42563dcd4d0f7a8d6121b`

```dockerfile
```

-	Layers:
	-	`sha256:89c9d8d8bddf968ee9f05171ddf674944ccf96d2c3df27dd2f5612e452da714e`  
		Last Modified: Tue, 21 Oct 2025 03:34:32 GMT  
		Size: 2.0 MB (2011835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72201c797f2648a5b0be16e7dc44930d3ddc214e2d4bc27d43cd6b923d85e481`  
		Last Modified: Tue, 21 Oct 2025 03:34:33 GMT  
		Size: 22.3 KB (22270 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; riscv64

```console
$ docker pull memcached@sha256:275951d176352ae7a6c07c3342e4a3696ed07e5711b47a3d3eac6d077943d7fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30629997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a439308e1f0b95ecea2e57b1abd7e75a6013568a1a7500b1f4d7bd0e21ad63`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6d1567708d42906165204f9177d357cb6a2fd51f758da447f1743b00813f892f`  
		Last Modified: Tue, 21 Oct 2025 00:37:37 GMT  
		Size: 28.3 MB (28275650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3633fd6545714a9d496af99598a2f2d1d149fd30ccb0af33ca4b5a64f2c80db2`  
		Last Modified: Tue, 21 Oct 2025 03:45:15 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0080b76dfc5efa9880c5885d69ca4cb830c2b81c8868038da6c3ec979f4df45f`  
		Last Modified: Tue, 21 Oct 2025 03:45:15 GMT  
		Size: 133.0 KB (132972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852a88ae8dfab39558e6bfca2ab58f39c01708aae430b3414e67d8fadc449694`  
		Last Modified: Tue, 21 Oct 2025 03:45:16 GMT  
		Size: 2.2 MB (2219861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a327b2de5a4375096f16800253786a6cfa67cce06f9f359b1c824e8232e98410`  
		Last Modified: Tue, 21 Oct 2025 03:45:15 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c933f2561e6f8e1189581b1eeb13dad69d7136a328a0533102686c15e68cb541`  
		Last Modified: Tue, 21 Oct 2025 03:45:15 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:7b68aaa7179e5972f8e6c99cbc3683f42653a9b4e71b3083cc76c60f88a4ecb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29ef9b8ffe7eed5ede85b59399c486af192d1744333cfa894153cffdf84ebefa`

```dockerfile
```

-	Layers:
	-	`sha256:861eae89f87c467092bc44440857f9d241e78153edc4d2e4fa84f83964fcbefe`  
		Last Modified: Tue, 21 Oct 2025 06:34:37 GMT  
		Size: 2.0 MB (2002198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7005598b4f28cfd2d5cfca73d6642c460d950449af439a25f8d87d7e8442aef6`  
		Last Modified: Tue, 21 Oct 2025 06:34:38 GMT  
		Size: 22.3 KB (22270 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; s390x

```console
$ docker pull memcached@sha256:97d22f11a028c8313d60f2b0d408dda8b2d48228b9b75aa2837e5463a793b535
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32292996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3e07eed38bed1a525726cbdc7874a25878c07feafb0bd683fe1f6583de2f83e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1759104000'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:924b0740f35a15fc20142be5c392f6b033c8051daecf16d2db38c22d6d73eb53`  
		Last Modified: Mon, 29 Sep 2025 23:41:29 GMT  
		Size: 29.8 MB (29837230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f51adc9bddc158c97c423c25020f779f6eaf1052b5377d27f3c426f6e1bfc021`  
		Last Modified: Tue, 30 Sep 2025 06:33:13 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e96b9e4bc41b016b366753e5d7d24d6ec0ad57f58fd33f9950ec9221297a8a4`  
		Last Modified: Tue, 30 Sep 2025 06:33:13 GMT  
		Size: 140.4 KB (140431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e41252907eabe8a9429031bb41587143d8a76355a4ec8726199ab91669e2ec3`  
		Last Modified: Tue, 30 Sep 2025 06:33:13 GMT  
		Size: 2.3 MB (2313824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2a41347a9c48966679d812976b6782615489e8d5f3d097e121b6150546f1cb`  
		Last Modified: Tue, 30 Sep 2025 06:33:13 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:969f1ab4db0027abb6561b0f8c35ae90cdfd2564247531bffcfb8860284b4319`  
		Last Modified: Tue, 30 Sep 2025 06:33:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:3f77e30f08514ef437bcf703e92082745153815200f728ce23b57a22ebbe9f84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0af62fcf07f143e611b564b8cdb2e08d11e05d8a8917d137e71fa925d6c936e4`

```dockerfile
```

-	Layers:
	-	`sha256:2db70adf2290adc880f8aa191f9e3b299c9dd28f01e3277a5386f4830c1f1f16`  
		Last Modified: Wed, 01 Oct 2025 21:34:44 GMT  
		Size: 2.0 MB (2009617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c002c1b0040529dcbb20761ae0b22e83c70cbf1d616626a80eff7eeccc02b1e6`  
		Last Modified: Wed, 01 Oct 2025 21:34:45 GMT  
		Size: 22.2 KB (22196 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:trixie`

```console
$ docker pull memcached@sha256:302493fd5e802f3bad0b33d2dc1db60e026fc16a1e43a758bdc3e769218f3f44
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
$ docker pull memcached@sha256:b995c17f51fbc95ab650436bf004e0e08aac1e231a0c4ced640ba25409a53ab5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32209591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2ebce0923097e2ebc228b419829228444709a8f2168920008cde8f0aacd5f50`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:339cbfbe5560ff0c225f888ba7ae149a9ce0536968c1bcccc467ceea4e3b09a0`  
		Last Modified: Mon, 29 Sep 2025 23:53:01 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84637889c9320e34d3cc8375e48fdc43299460f2280a8b62690c6d78f6a1ccf0`  
		Last Modified: Mon, 29 Sep 2025 23:53:01 GMT  
		Size: 136.6 KB (136571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe788cc20223f97addb89c197bd5ea5d77c3bbe084b00e8dcb70731168abb3b`  
		Last Modified: Mon, 29 Sep 2025 23:53:02 GMT  
		Size: 2.3 MB (2293745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e090b148236c9a2470abf0308fbdf9c8ed3c23b04efdfb18e68f20902a2e2f36`  
		Last Modified: Mon, 29 Sep 2025 23:53:02 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93fa1d160038c361af454d4a8eb44b68dcda89fc415ad571b6e9707fb59a0082`  
		Last Modified: Mon, 29 Sep 2025 23:53:02 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:5cd8c391814b8c7fbf65b5d657526c37f0516c6e4fe7dc245bfc347550a31200
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40690a93df6f911472221738e6595b6a746bd957d3bf1552c92ff83f17536644`

```dockerfile
```

-	Layers:
	-	`sha256:4b787171563846ab285584301f579a404cecd6f570a25225e02ff18939e29124`  
		Last Modified: Tue, 30 Sep 2025 00:34:34 GMT  
		Size: 2.0 MB (2008180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5a013035c58f0ea6bcc734d2c89618a0e98d1d8b3d3f07a169cd97b52bf4c0d`  
		Last Modified: Tue, 30 Sep 2025 00:34:35 GMT  
		Size: 22.2 KB (22196 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; arm variant v5

```console
$ docker pull memcached@sha256:29d660bf29e180ab12efa8f4cdf6a974ec008d83e2c3c8ec051dee748eb9ed04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30319195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d982473f8bce68d8cb2795fc64f125c06b91ec37e8e238bf7464d2e1fdba6a1b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1760918400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:389bac9f76fa529ccf801fd7c9cb260ecee27d208221c25004185ab22936c4d4`  
		Last Modified: Tue, 21 Oct 2025 00:20:45 GMT  
		Size: 27.9 MB (27946283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed93883017eb3f4dde85524af233ee0b6e174c0abe1cef988e9bce8d5375e89`  
		Last Modified: Tue, 21 Oct 2025 01:23:33 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:791751af616e97272032619ddc7968fe23e71223657f52594fb2c62a2a47eda5`  
		Last Modified: Tue, 21 Oct 2025 01:23:33 GMT  
		Size: 144.0 KB (144045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5ea9c6e85cf6a029a9ba48b6b73a8dc6479d59392f254b1c2db7b1902074dd`  
		Last Modified: Tue, 21 Oct 2025 01:23:33 GMT  
		Size: 2.2 MB (2227357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a58aefd26c4b989c6b88d95adb3a6920797ab35bfccd55f1001d478ea7c38e`  
		Last Modified: Tue, 21 Oct 2025 01:23:33 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87cab310dfac01ff5304eeb4a6ea3ddebf9ab9ab7badd32bb16312e9ad5c22ae`  
		Last Modified: Tue, 21 Oct 2025 01:23:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:63d0a43eb60f7ffb19e7cc876899b414f91eda292c74d1ecd4894dbc17394c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81a59c35b11c8306faf5db19cf7b6aee2213f889fcdcad2f2058c233038f5c2d`

```dockerfile
```

-	Layers:
	-	`sha256:b6117037dd5100454e92bb311823f69d718d18239a54c39029a154a68618f82b`  
		Last Modified: Tue, 21 Oct 2025 06:34:24 GMT  
		Size: 2.0 MB (2011237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfc7fdadb808663bde556e0343ab1151a3545e7211fe7e6e71915327352feedf`  
		Last Modified: Tue, 21 Oct 2025 06:34:25 GMT  
		Size: 22.3 KB (22346 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; arm variant v7

```console
$ docker pull memcached@sha256:889cba709c7ad01fa2925b49389f4e73f9d759d8020c2a108aabd5a1b1f2ee95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28532153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56676dc32ecaa308b63acf0b41885c581e3700d44bc04a653a595327d4198c3a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1759104000'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0289e98159900b326d4cedde367bf225e25835a3ad879647f17f922e43cfa884`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 26.2 MB (26212758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c067599f6c6ba1a22613aa308e4d66e5249d6cc507b1229b6f4d482aecce8a6`  
		Last Modified: Tue, 30 Sep 2025 00:01:20 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cf0eec4f32f0da160c5e99bd0b57756034bb7093c545143caf6e310210cb44`  
		Last Modified: Tue, 30 Sep 2025 00:01:20 GMT  
		Size: 135.3 KB (135298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e59b4e18c59ebfcadada2142ce2be01e708dd3af20396b507979cf3a15f6f22`  
		Last Modified: Tue, 30 Sep 2025 00:01:20 GMT  
		Size: 2.2 MB (2182588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a24488f6b368fccedb9bb9614c2c525964ee0e3cc91e91d2b41f74b38a1c9a59`  
		Last Modified: Tue, 30 Sep 2025 00:01:20 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413fbe42e3bd71205a88a777ab5027fc34a2ad8053f6593d6653d72ae17ba8ff`  
		Last Modified: Tue, 30 Sep 2025 00:01:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:ca8765c9f99276788e2b51ecfaf135680c03e0c222b9753d99dc4218bcc94095
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b6914431db285aeda4c9e27af56a106671c3541420f5b3bce905bed9f17ac6f`

```dockerfile
```

-	Layers:
	-	`sha256:fb1138fbff85001f5063fc6944faf0e66d26d9a179651b7a6b0c05c7f33a9240`  
		Last Modified: Tue, 30 Sep 2025 00:34:43 GMT  
		Size: 2.0 MB (2009640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c15f19f4d680266479069e896e888cb3a6a008b2f385c644c4f0baa61370937`  
		Last Modified: Tue, 30 Sep 2025 00:34:44 GMT  
		Size: 22.3 KB (22345 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:ef5cebc6723efc4307b7e2459b1b2c096013265dcfc93ee6e929dfb04399da59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32570960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b078c21daa3a3ef97cfc057882f396e936961312205c8e1a12712f179cf9f15`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c850e44210e9493ef7540c5c65cd48360355c3e6e94094c44d15af0045dc8dea`  
		Last Modified: Mon, 29 Sep 2025 23:59:01 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a741f1a1ae0d87da15466cd2dafd5acfb37dd72d94dda9656931ef24906d618`  
		Last Modified: Mon, 29 Sep 2025 23:59:01 GMT  
		Size: 153.4 KB (153385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa09f33f1e4c185a911cfd4dcd7d1dbbba5b9909fbe9100480230f1436457116`  
		Last Modified: Mon, 29 Sep 2025 23:59:01 GMT  
		Size: 2.3 MB (2275224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9a30963a9969bd789a111826840c0e97edd5d71548b548a30932bee7448fcc`  
		Last Modified: Mon, 29 Sep 2025 23:59:01 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ffdbd101cdb57f8b290f16ae4fa6106fd6ea85695fed7d08e98fdd19332d85`  
		Last Modified: Mon, 29 Sep 2025 23:59:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:573b95a8bb8dd5178978144dbd1446143419bbfc4edb099c6ebbe467c8e00b83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2a5e2b768012fff6837a6324e893b847c3948649e73a49b722b5d6b4b2d1f38`

```dockerfile
```

-	Layers:
	-	`sha256:8ab701ab9aad8acae756d96838becc2299738dcbdd81cb0071e6fbb5459b2f5b`  
		Last Modified: Tue, 30 Sep 2025 00:34:48 GMT  
		Size: 2.0 MB (2008496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71a37a40aa0845aeb88bc64f742dc25764c4824bedfe40f31b6f13e0bbd595b7`  
		Last Modified: Tue, 30 Sep 2025 00:34:48 GMT  
		Size: 22.4 KB (22393 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; 386

```console
$ docker pull memcached@sha256:0d993065ea1ed42de5bd4fcda3bafa779f274987bcb4d302b8a927344105ce6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33687876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fe2c39bed6edf857f276a7b8e77499f6c2110ebe12362143053acafdf31fba3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ab4c7760f4a4bda4b0797f3f0b56bd90b9778b76fc8351f2e1bd7c332b9dcc92`  
		Last Modified: Mon, 29 Sep 2025 23:35:33 GMT  
		Size: 31.3 MB (31294536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bcd1d82da4702bb3c598bb03b9d138dea8bd5e459160d5276b3fb8ebfb58923`  
		Last Modified: Mon, 29 Sep 2025 23:58:18 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ceba58f3514163ba75fa31b3b659efbe123eee61ee1e13161b71c6976b9cca2`  
		Last Modified: Mon, 29 Sep 2025 23:58:17 GMT  
		Size: 147.4 KB (147429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0453c4dd0d673c524b37cefb6f3412d20dde32e36c7999a26420bfb8481b0add`  
		Last Modified: Mon, 29 Sep 2025 23:58:18 GMT  
		Size: 2.2 MB (2244401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8916b29a59d03a745388da5e0a1aae97b201cd0e333de592e8a0fbe93da42b2f`  
		Last Modified: Mon, 29 Sep 2025 23:58:18 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28a35d7ac2cedad97d815d581ffa42e79c00126410603b586fb754ff264b578`  
		Last Modified: Mon, 29 Sep 2025 23:58:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:a1cbda14df44fff2e8baad5f7b53a3c32f617c55d96176326e107932e625e1d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef21897bb3061b8deedad86c30704928e376dad42a0a0bd9bdd946ff1cd46e37`

```dockerfile
```

-	Layers:
	-	`sha256:1f6010c4e760c848d7546664960f84f5082bc718d59b4dee6be3dc6489f1b283`  
		Last Modified: Tue, 30 Sep 2025 00:34:53 GMT  
		Size: 2.0 MB (2005337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f0fb1a46b98e7a2df02e226e82cd6854123a501d2d649bd70f05dbba8c4ffb7`  
		Last Modified: Tue, 30 Sep 2025 00:34:54 GMT  
		Size: 22.1 KB (22138 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; ppc64le

```console
$ docker pull memcached@sha256:78facd60957c01a0fc2c93514ec1f636e2acc585252bf3d2b224c9e4a2720751
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36187154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:078835e44984fd2f6238dc1bedb2dcc1eb3d45b38c738650295299276d8e3052`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1760918400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a9b4dd19a96be85b367998327f4288ed2fa8f174d1b3e8bea8ac7c2c626ec865`  
		Last Modified: Tue, 21 Oct 2025 00:26:55 GMT  
		Size: 33.6 MB (33598518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbed628a221d903400b8d49b4dc58aa0541e23d5a909543d626205670fd1072e`  
		Last Modified: Tue, 21 Oct 2025 01:54:52 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e748ebb38f38290596ca068f9f7e75e6c669eb4588462f2fe0b3566753e7f5`  
		Last Modified: Tue, 21 Oct 2025 01:54:53 GMT  
		Size: 170.3 KB (170257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b23f2908f85849ad3cfc2d526edf441cafb4862876c74e7c77fb5daeac7cc908`  
		Last Modified: Tue, 21 Oct 2025 01:54:53 GMT  
		Size: 2.4 MB (2416870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82d739662461ca129d2f470c2fa271c4962856a0f4a86f15d9469b59228c429`  
		Last Modified: Tue, 21 Oct 2025 01:54:52 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cefac88d4c183e05bebf79bdd2a0ad83aa10bbf75f4d809e74a8e7adb46146d`  
		Last Modified: Tue, 21 Oct 2025 01:54:53 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:766403e34da539f4d7944ceccfddc6817ff9a2e87659514dca52e26b77f14121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:093b6d02f98d1abdf2e4d567f2158cd54a22a08c01d42563dcd4d0f7a8d6121b`

```dockerfile
```

-	Layers:
	-	`sha256:89c9d8d8bddf968ee9f05171ddf674944ccf96d2c3df27dd2f5612e452da714e`  
		Last Modified: Tue, 21 Oct 2025 03:34:32 GMT  
		Size: 2.0 MB (2011835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72201c797f2648a5b0be16e7dc44930d3ddc214e2d4bc27d43cd6b923d85e481`  
		Last Modified: Tue, 21 Oct 2025 03:34:33 GMT  
		Size: 22.3 KB (22270 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; riscv64

```console
$ docker pull memcached@sha256:275951d176352ae7a6c07c3342e4a3696ed07e5711b47a3d3eac6d077943d7fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30629997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a439308e1f0b95ecea2e57b1abd7e75a6013568a1a7500b1f4d7bd0e21ad63`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6d1567708d42906165204f9177d357cb6a2fd51f758da447f1743b00813f892f`  
		Last Modified: Tue, 21 Oct 2025 00:37:37 GMT  
		Size: 28.3 MB (28275650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3633fd6545714a9d496af99598a2f2d1d149fd30ccb0af33ca4b5a64f2c80db2`  
		Last Modified: Tue, 21 Oct 2025 03:45:15 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0080b76dfc5efa9880c5885d69ca4cb830c2b81c8868038da6c3ec979f4df45f`  
		Last Modified: Tue, 21 Oct 2025 03:45:15 GMT  
		Size: 133.0 KB (132972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852a88ae8dfab39558e6bfca2ab58f39c01708aae430b3414e67d8fadc449694`  
		Last Modified: Tue, 21 Oct 2025 03:45:16 GMT  
		Size: 2.2 MB (2219861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a327b2de5a4375096f16800253786a6cfa67cce06f9f359b1c824e8232e98410`  
		Last Modified: Tue, 21 Oct 2025 03:45:15 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c933f2561e6f8e1189581b1eeb13dad69d7136a328a0533102686c15e68cb541`  
		Last Modified: Tue, 21 Oct 2025 03:45:15 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:7b68aaa7179e5972f8e6c99cbc3683f42653a9b4e71b3083cc76c60f88a4ecb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29ef9b8ffe7eed5ede85b59399c486af192d1744333cfa894153cffdf84ebefa`

```dockerfile
```

-	Layers:
	-	`sha256:861eae89f87c467092bc44440857f9d241e78153edc4d2e4fa84f83964fcbefe`  
		Last Modified: Tue, 21 Oct 2025 06:34:37 GMT  
		Size: 2.0 MB (2002198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7005598b4f28cfd2d5cfca73d6642c460d950449af439a25f8d87d7e8442aef6`  
		Last Modified: Tue, 21 Oct 2025 06:34:38 GMT  
		Size: 22.3 KB (22270 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; s390x

```console
$ docker pull memcached@sha256:97d22f11a028c8313d60f2b0d408dda8b2d48228b9b75aa2837e5463a793b535
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32292996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3e07eed38bed1a525726cbdc7874a25878c07feafb0bd683fe1f6583de2f83e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1759104000'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:924b0740f35a15fc20142be5c392f6b033c8051daecf16d2db38c22d6d73eb53`  
		Last Modified: Mon, 29 Sep 2025 23:41:29 GMT  
		Size: 29.8 MB (29837230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f51adc9bddc158c97c423c25020f779f6eaf1052b5377d27f3c426f6e1bfc021`  
		Last Modified: Tue, 30 Sep 2025 06:33:13 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e96b9e4bc41b016b366753e5d7d24d6ec0ad57f58fd33f9950ec9221297a8a4`  
		Last Modified: Tue, 30 Sep 2025 06:33:13 GMT  
		Size: 140.4 KB (140431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e41252907eabe8a9429031bb41587143d8a76355a4ec8726199ab91669e2ec3`  
		Last Modified: Tue, 30 Sep 2025 06:33:13 GMT  
		Size: 2.3 MB (2313824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2a41347a9c48966679d812976b6782615489e8d5f3d097e121b6150546f1cb`  
		Last Modified: Tue, 30 Sep 2025 06:33:13 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:969f1ab4db0027abb6561b0f8c35ae90cdfd2564247531bffcfb8860284b4319`  
		Last Modified: Tue, 30 Sep 2025 06:33:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:3f77e30f08514ef437bcf703e92082745153815200f728ce23b57a22ebbe9f84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0af62fcf07f143e611b564b8cdb2e08d11e05d8a8917d137e71fa925d6c936e4`

```dockerfile
```

-	Layers:
	-	`sha256:2db70adf2290adc880f8aa191f9e3b299c9dd28f01e3277a5386f4830c1f1f16`  
		Last Modified: Wed, 01 Oct 2025 21:34:44 GMT  
		Size: 2.0 MB (2009617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c002c1b0040529dcbb20761ae0b22e83c70cbf1d616626a80eff7eeccc02b1e6`  
		Last Modified: Wed, 01 Oct 2025 21:34:45 GMT  
		Size: 22.2 KB (22196 bytes)  
		MIME: application/vnd.in-toto+json
