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
$ docker pull memcached@sha256:157c563eef6954ac0bc583c36def96d8ed2d3b3c5b37214f27d210ac53942386
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
$ docker pull memcached@sha256:742d5665f0f292e1278bafd0dff520b5f4edb101c587c29fb0ef273f9d7e124f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30319041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc1024c223c5953b97de26e48cce8df89bee4493e37781f6826e6df56c590056`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1759104000'
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
	-	`sha256:d2a243ecf382412941b4d6772dba911a8093cf3703c933872fbb7ecc21e27e20`  
		Last Modified: Mon, 29 Sep 2025 23:34:24 GMT  
		Size: 27.9 MB (27946145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d24bdf1148108d2d3fc42a07dae247e5242de03db9a71e04066262a853f139d`  
		Last Modified: Mon, 29 Sep 2025 23:59:31 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e717ac34c0d292ae77e9118ac1581d40d881e518d32d9e64f01fddf818164b`  
		Last Modified: Mon, 29 Sep 2025 23:59:31 GMT  
		Size: 144.0 KB (144036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a3b7d16c874ce52964b6ba216127f7fcf604d326cc965210eb58119d605d28`  
		Last Modified: Mon, 29 Sep 2025 23:59:31 GMT  
		Size: 2.2 MB (2227345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb7f38fc7bbd06b5c988a48649d103d93ab0d8011b6a4f5bd8ad38bbd4cac432`  
		Last Modified: Mon, 29 Sep 2025 23:59:31 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5307470e3430d06e3f04b798774d1905a98a13f5ba3387596a0aa97e34b7eba`  
		Last Modified: Mon, 29 Sep 2025 23:59:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:92764b7963e735b77f5e5b433bf1311bc919679a81273cf442178538cf7da2ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:512f0e0d6001116f7984270337608de656664abeb7602b6fc4add42303ba8ee6`

```dockerfile
```

-	Layers:
	-	`sha256:a8fc1cbacd56787b740b886369c6eaafa6151c97fade289ea774600c03a80e11`  
		Last Modified: Tue, 30 Sep 2025 00:34:39 GMT  
		Size: 2.0 MB (2011183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57884b3635fcf7e290933e3a1da7210a05c98ab3187a6e484a5cc8cedf845e98`  
		Last Modified: Tue, 30 Sep 2025 00:34:39 GMT  
		Size: 22.3 KB (22347 bytes)  
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
$ docker pull memcached@sha256:5a071a15dfae20029d56a8845f8053a4f4447934a87e0db0678b6f4ddc2e924a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36187246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6957fdbfa2f978334c6c02013b0e9b928534ddf41009ccae3597ccaf389fd455`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
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
	-	`sha256:8bcecd3ced4047f6a4d35464fc2ee9b45e7fcc10b49690427794f4421b0552ab`  
		Last Modified: Mon, 29 Sep 2025 23:41:19 GMT  
		Size: 33.6 MB (33598454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cee3e1fdea897c6a6b3a982e1918145b5bcd716e5ae6ed66b5e7184e651e059`  
		Last Modified: Tue, 30 Sep 2025 07:50:11 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dea6ee42e2fcf50b7f0d213d52ea27f8eebdaf12c0aa80c5df4828c4566af25`  
		Last Modified: Tue, 30 Sep 2025 07:50:12 GMT  
		Size: 170.3 KB (170259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629d93745cabb21520c860c7612f141299a2c0f2632cf40b7dcc88799307dcd7`  
		Last Modified: Tue, 30 Sep 2025 07:50:13 GMT  
		Size: 2.4 MB (2417019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afbd1630af2c91474bfc04cf614cc4d0a7093510b706f978f20f426127e93305`  
		Last Modified: Tue, 30 Sep 2025 07:50:12 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8293ad839e50f443a419fb4c0f6a6dbde6204ad3bf467cdff6e99385a7d1c3`  
		Last Modified: Tue, 30 Sep 2025 07:50:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:987b950cf472a2d95cc860d4c3c9e95c51ab792c33f5ac61607b7e4f38d1d8d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:973c6753846fed972084489bd202cf7da6e77ddc33d584a90658a8949b5730ee`

```dockerfile
```

-	Layers:
	-	`sha256:821a5821beef4d6bdae90ea0d98277dd982af05804dd43f706310bc7263244c4`  
		Last Modified: Wed, 01 Oct 2025 21:34:36 GMT  
		Size: 2.0 MB (2011781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:222d48bb5ef6a86d72ecccaf90a1cd7cf49c644139aee33815b1e7d0fd87cfcb`  
		Last Modified: Wed, 01 Oct 2025 21:34:36 GMT  
		Size: 22.3 KB (22270 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; riscv64

```console
$ docker pull memcached@sha256:31bb76b9b98cd96febc6b1d5056f839ffab9aaaa12690d0a47353df1b2b49221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30629784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e010912f76722a300766eb6afe7e6b13e8f72682c8dec557d00826b2a7cba503`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1759104000'
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
	-	`sha256:ecc6f9aec21fb94a493c2875c244e720a2f7c6c034063ce87b2f5b6b46962ec9`  
		Last Modified: Tue, 30 Sep 2025 01:05:14 GMT  
		Size: 28.3 MB (28275502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c2f28b5ea15f2b021d2f93df684963b9d27de2301bfccbf53d01abc5bdaa97`  
		Last Modified: Tue, 30 Sep 2025 04:00:18 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179b31cc3aad1ab89917cf87cb268b6e8e4291ec4b8996317231c4ac0003ebf9`  
		Last Modified: Tue, 30 Sep 2025 04:00:18 GMT  
		Size: 133.0 KB (132970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca5db35fb11036dcb8f2d55bbe271869356c9b4b2e08c0d0293a9b0c894f5dff`  
		Last Modified: Tue, 30 Sep 2025 04:00:19 GMT  
		Size: 2.2 MB (2219797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc4c908359c51ce26778438a3886b2eb2d6987ee3a22862dbdbe2056a3cd95d`  
		Last Modified: Tue, 30 Sep 2025 04:00:19 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7254f9df049c190c1c3ffa9794b395fb4e3ec7ab18b8dce7a58733c63a54dd`  
		Last Modified: Tue, 30 Sep 2025 04:00:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:10dcedf955ee46896155ca87f9a292967d1ce021fbab41f3a0fc44045a885e25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85a06d87da790b7800c970ca38989414eeae6c950cf890286591dc59c6163cc5`

```dockerfile
```

-	Layers:
	-	`sha256:b8fb80942d713e49171d0a98b2306b7bbb0023e57f180295e56893f7ea7f458d`  
		Last Modified: Tue, 30 Sep 2025 06:34:34 GMT  
		Size: 2.0 MB (2002144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cbc67dcbbe8db9619b2b3e3b962ebb7d9640901e2048fa63620351cc03d940d`  
		Last Modified: Tue, 30 Sep 2025 06:34:34 GMT  
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
$ docker pull memcached@sha256:eca5d776fe62e6ffe5e27e1a4d357e0bbd9ac609a271243c210599a898122ad2
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
$ docker pull memcached@sha256:033134f4dd9f45d4e22b6e98b040ea3fccf0dca740af3c949b44bebf458b04d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5904246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca259aa2216a248c482fc8a069d48b1e70b087529d2c3de97154bfa458dbb7a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23fb46bc7dee2beda6f5f6f567aecd4d7d7698b9749ed917988a859b7dd96e30`  
		Last Modified: Tue, 29 Jul 2025 16:32:22 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48faf8c85515fb9d17e0752e77d8241f223d53b1adc90439c606d17daabd0ae`  
		Last Modified: Tue, 29 Jul 2025 16:32:24 GMT  
		Size: 104.7 KB (104725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d552a2d777fd444b41cb79438f9f1b441821162e78d73e96dc848a773cf43892`  
		Last Modified: Tue, 29 Jul 2025 16:32:24 GMT  
		Size: 2.0 MB (1998477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c70665f30f3e15975d429b494cb17b21c5d4630c1800cb0addc3fce3a11aa29`  
		Last Modified: Tue, 29 Jul 2025 16:32:20 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ff68520caaf588cec750ad7c403cf55d79eecfff4b7a4ac5eb3910c90c2817`  
		Last Modified: Tue, 29 Jul 2025 16:32:21 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7b27e0df383f45d6d523345a078898524a69cee4d6978cf64bf26532b8679dca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 KB (116752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb88e7ee6d3e67b2e4f307c081504a685666917ddf50770fe8beb5abd60a3dc5`

```dockerfile
```

-	Layers:
	-	`sha256:2cf00a09ffccb2c00421311314137de90d0586c126b79dbe5315ce321c168b34`  
		Last Modified: Tue, 29 Jul 2025 18:35:07 GMT  
		Size: 96.2 KB (96180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55325ecc9b276e9c55badf949ed4f06840c34aa8baf0aa6f974e0b90dc5d4e0d`  
		Last Modified: Tue, 29 Jul 2025 18:35:07 GMT  
		Size: 20.6 KB (20572 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:78b59dd3af5a55e950f5106869e642af122a7dc470545f4ba533f6833d83b62c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5550795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb09d5ce1b7010f7a36d77494bc5358d666339628c183692906db6a961373847`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c710b5ddcc2882c5014d0c8cb93aec2bd8b6cc3c59fd42b40c87d94f89a7bc7f`  
		Last Modified: Wed, 23 Jul 2025 22:59:16 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c42040d822a4af7f05f9ccd4d18a7a5e4712b118b7f18d1a7969761029a9d2`  
		Last Modified: Wed, 23 Jul 2025 22:59:16 GMT  
		Size: 101.5 KB (101533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3095e18cd24048696efd57ac64d04dde381a3abde625964e02165c7364eb5633`  
		Last Modified: Tue, 29 Jul 2025 16:50:12 GMT  
		Size: 1.9 MB (1947003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0436ec50f04ed972ff0dd760f7e820f192236e5e720bddb6173f65159c7c36`  
		Last Modified: Tue, 29 Jul 2025 16:50:11 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671c24aae36bb04a32e05bd64e1371384f594889cdbbc41029c916447666d402`  
		Last Modified: Tue, 29 Jul 2025 16:50:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:c2a050c6822d834285577c3a001fdfcf9949b7f5a483a4a76a49b549bea19641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54e8bda3e734528caeab4505f084ca7a3076d5ec2273287f66954b5e91af42f`

```dockerfile
```

-	Layers:
	-	`sha256:0d86924831d61ce8b792b25421e9ff0fa2eda9ab940eba5309d44d0eeada7e8e`  
		Last Modified: Tue, 29 Jul 2025 18:35:11 GMT  
		Size: 20.5 KB (20506 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:c9f5db2389b9b0b4a2cd199c4417a9f49a60c42d616e8421177e662d4830de07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5217393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9421ed030d4b6b6405714612b8858bda87bc53ac8b0c5ed65c582119527f2d9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251060498ca8f0484e20714689b9caba533d09c1b74ed8f2a06780db515a28e2`  
		Last Modified: Thu, 24 Jul 2025 00:27:37 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2293bd2fb47d57e5869c197133067e17f9b1e51ea0f298af1e480e7fd33d681`  
		Last Modified: Thu, 24 Jul 2025 00:27:38 GMT  
		Size: 91.3 KB (91313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ae82f2bac2f7e6fe57f8cb7006fc227c972da1ae5749eba9f5f73e6f3248ec`  
		Last Modified: Tue, 29 Jul 2025 17:11:51 GMT  
		Size: 1.9 MB (1905692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e60bf2b2164c620b69e40bdcb64d4104d02eab86c96ea6e170a3601b9ecfd82`  
		Last Modified: Tue, 29 Jul 2025 17:11:51 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:665fe4cd856f1a5c2193568e756c572656949b17c381fc8d43efaa823e18cfa7`  
		Last Modified: Tue, 29 Jul 2025 17:11:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:376a71bc0fef7741e92fdae8b96c825c4622e980de01e724b1a3a0bec3d95f20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 KB (116963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22b574f6c6d021a917c0e99ff4800d8ac3c22fb94b94f88c404cc7609f562fb5`

```dockerfile
```

-	Layers:
	-	`sha256:58ebd4bc7ee5888c552e0fa618f93aefbdb1d15a56ecd3abef19a46ce2f93eee`  
		Last Modified: Tue, 29 Jul 2025 18:35:15 GMT  
		Size: 96.2 KB (96248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d432ed2053ed8249834dd5016fe3199bbc3f82dc7013027c3ead9efe2a007b98`  
		Last Modified: Tue, 29 Jul 2025 18:35:16 GMT  
		Size: 20.7 KB (20715 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:b5e4ecc3e927ee30e5cfcfc8aa044960631c75eb8abed9d0fcee6232aa5fdf79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6241700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40c880dc2c785861dc9010b813bb6f533f30518443a3bb7e7f477bc96af14582`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfbfeb6ac9fd2045c5bea10a301ad554c1f703ffc2885c41520dd5e42eb4a59a`  
		Last Modified: Tue, 29 Jul 2025 16:41:08 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47acaa5035f94aed634b9d7ecae02fb3838f19e38f8e752ecd6cfba97699b31`  
		Last Modified: Tue, 29 Jul 2025 16:41:08 GMT  
		Size: 120.8 KB (120812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8160f3136c6863b52f0dec4f9918b91b8a509700b2071ec0aecd5a6231f00f2a`  
		Last Modified: Tue, 29 Jul 2025 16:41:09 GMT  
		Size: 2.0 MB (1988782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff22f0cad01950efb78a7a862b0becb8b2fd22d795b585f97dad66c091c3dd7`  
		Last Modified: Tue, 29 Jul 2025 16:41:08 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed19cbfb574c7d8cab364e2ec072c0e03f694468ada41cd70bfcd35392df9e7`  
		Last Modified: Tue, 29 Jul 2025 16:41:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:b4c81c7ababb91ecdda3b7d70514d16818602199d759eb2aadd74de732d52960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.1 KB (117055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80452fd4f79f6e7a0dab0beebf5c144f9df7c257255cdd3cb93ccbff77001fd6`

```dockerfile
```

-	Layers:
	-	`sha256:f11d2a322f6088804ee63ae1a77b9d5ddcdfdc0c65c22e7a70b7ee67cf4532ed`  
		Last Modified: Tue, 29 Jul 2025 18:35:20 GMT  
		Size: 96.3 KB (96284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e225dd6ea14146ddf445598f24189c065ec684fbeb92e7d053a0211a7d60efda`  
		Last Modified: Tue, 29 Jul 2025 18:35:21 GMT  
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
$ docker pull memcached@sha256:04386ede5dcbf35cabad144bcdc951cc64882f7b9727f2d09927fe0d5551dd19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5942089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8252590eee78d67456ac83fd8279259aaea4d2a555c8bc20b173663fcaa2883`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc22e0cec7e7fe8cff10539bca58363ad6749e2de4f878015c25b5f2b6ecadb9`  
		Last Modified: Tue, 29 Jul 2025 16:33:46 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992ebe18219bd78e59e7e56661aae22f700927f47bc7ad1dfe7717093b371c15`  
		Last Modified: Tue, 29 Jul 2025 16:33:49 GMT  
		Size: 124.3 KB (124315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953f5a37d23881d59809ea64dc6ebf1a152a1ff8929f51befb10577771755f5d`  
		Last Modified: Tue, 29 Jul 2025 16:33:49 GMT  
		Size: 2.1 MB (2089310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10b62870a2d7b266495d83cfd72dcf702c91c5c60a7e29836bd9bdac776511a7`  
		Last Modified: Tue, 29 Jul 2025 16:33:47 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1cc8c0fe9a4ef7e2ef70e32ddbfbd2fd68985dd452630a8f390c5b41c654f8`  
		Last Modified: Tue, 29 Jul 2025 16:33:47 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:cf7e9735e4ef5d00dc25928653b808214f070708e9d879ef54afc4d77ce9db2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcceb455cfdb86bdb0c165af3bc54cbab794d56fef1dbae2b484d28027db791c`

```dockerfile
```

-	Layers:
	-	`sha256:a40704a0afb5cf1b90c0fbdf73c5218a4d8f0e93bb39014507b5fa5f8c7265dd`  
		Last Modified: Tue, 29 Jul 2025 18:35:29 GMT  
		Size: 94.3 KB (94287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da22397f364310e72420738395739c36e25b4e4813bbc5da197582a91bb55ac9`  
		Last Modified: Tue, 29 Jul 2025 18:35:29 GMT  
		Size: 20.6 KB (20648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:d55b98c34ba1c2f546461bd57477d46ab868f9de6b107ffb8f20e06dab1e10d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5555034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1034dde2661f43165e85db9a13ff0e10d237d14d4b1b7ee1d4570f19d7df4e69`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00bbdcecb4dec3cbaba0500f9425897948884cfd8db95ccdf9b824d448b24049`  
		Last Modified: Wed, 23 Jul 2025 23:54:15 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c18051d55886d147cafcee8f9e220087c0b60c0e11ec8898a4005352ee0f7e4`  
		Last Modified: Wed, 23 Jul 2025 23:50:14 GMT  
		Size: 107.9 KB (107902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953c2b44fe537b63907764cf78cbb294c6a1133eacb39c62d35ee5d4914779cb`  
		Last Modified: Tue, 29 Jul 2025 16:42:10 GMT  
		Size: 1.9 MB (1932977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d69b2f63abf91684a15b9de7b5e617996762376da3fdda50c4e20c2f1e0f4da`  
		Last Modified: Tue, 29 Jul 2025 16:42:10 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f57c134601fc15e8f2cf183cfd9a3057731ad48b915988217f51df31b5d3cf38`  
		Last Modified: Tue, 29 Jul 2025 16:42:10 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:d50b42de80ef3381b05da20cef4ba6ab4491facb607528e075c034257fe9d327
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27766c161110b7e46063a39ce6e176f87233fd6722a825ec338e1568892a77a3`

```dockerfile
```

-	Layers:
	-	`sha256:f933f968a4a14795196607a1337a19431e9f61db78bb49c5c2f89f64a17a1d89`  
		Last Modified: Tue, 29 Jul 2025 18:35:33 GMT  
		Size: 94.3 KB (94283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffc41094fe9f57bca69da70bbb18eca52aaf6d27d0fb6d79eda79f9e011a157a`  
		Last Modified: Tue, 29 Jul 2025 18:35:33 GMT  
		Size: 20.6 KB (20647 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:cfd223eb11df3d2297224d458caf974f3f0aae4742ff917812f1b8c84c84e705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5797268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78e23f18e891a12e72ef84139504baf8783a7db21d4976fc0b607f8e9bbf736f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f00131fb0ca26b15f1ac64b82554fc342b19f8c1ef38312a75addb6686f7bc24`  
		Last Modified: Tue, 29 Jul 2025 16:41:40 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e54da6ab620e035fd78987688d45401e87278ec8a5c02cef8a57e4ea9fd286`  
		Last Modified: Tue, 29 Jul 2025 16:41:42 GMT  
		Size: 113.5 KB (113499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6160f9fac1fd86eda224e9ce4740ea46f7e23dc7edb6d1fe9d830001313e63a`  
		Last Modified: Tue, 29 Jul 2025 16:41:46 GMT  
		Size: 2.0 MB (2037446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d01cd71d33b01b420652f4ad9275f1475f4f0bf253dc0a1b48198df2010be5`  
		Last Modified: Tue, 29 Jul 2025 16:41:52 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:831dd5e3c39dd2744dc8823190095f709c36020b55ccdaf85f62a146582c7d9d`  
		Last Modified: Tue, 29 Jul 2025 16:41:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:79f0de7e4dcc9afdbfa1fa22250cf3e544d6f3c33174246b427d2865c7e343d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71dad4d71741d8d354038cb6898389aebb54c956dfcd865d57f78dcc3b238bf8`

```dockerfile
```

-	Layers:
	-	`sha256:f942bbb9520308ae352a056c148fdce8f6b09672c257e0a769aa2504bacf1845`  
		Last Modified: Tue, 29 Jul 2025 18:35:37 GMT  
		Size: 94.2 KB (94229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c46680ef7cf08a43965ab9c7727cc70268ee89e366a1ce1806d0f7980b4ad812`  
		Last Modified: Tue, 29 Jul 2025 18:35:38 GMT  
		Size: 20.6 KB (20574 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine3.22`

```console
$ docker pull memcached@sha256:eca5d776fe62e6ffe5e27e1a4d357e0bbd9ac609a271243c210599a898122ad2
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
$ docker pull memcached@sha256:033134f4dd9f45d4e22b6e98b040ea3fccf0dca740af3c949b44bebf458b04d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5904246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca259aa2216a248c482fc8a069d48b1e70b087529d2c3de97154bfa458dbb7a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23fb46bc7dee2beda6f5f6f567aecd4d7d7698b9749ed917988a859b7dd96e30`  
		Last Modified: Tue, 29 Jul 2025 16:32:22 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48faf8c85515fb9d17e0752e77d8241f223d53b1adc90439c606d17daabd0ae`  
		Last Modified: Tue, 29 Jul 2025 16:32:24 GMT  
		Size: 104.7 KB (104725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d552a2d777fd444b41cb79438f9f1b441821162e78d73e96dc848a773cf43892`  
		Last Modified: Tue, 29 Jul 2025 16:32:24 GMT  
		Size: 2.0 MB (1998477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c70665f30f3e15975d429b494cb17b21c5d4630c1800cb0addc3fce3a11aa29`  
		Last Modified: Tue, 29 Jul 2025 16:32:20 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ff68520caaf588cec750ad7c403cf55d79eecfff4b7a4ac5eb3910c90c2817`  
		Last Modified: Tue, 29 Jul 2025 16:32:21 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:7b27e0df383f45d6d523345a078898524a69cee4d6978cf64bf26532b8679dca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 KB (116752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb88e7ee6d3e67b2e4f307c081504a685666917ddf50770fe8beb5abd60a3dc5`

```dockerfile
```

-	Layers:
	-	`sha256:2cf00a09ffccb2c00421311314137de90d0586c126b79dbe5315ce321c168b34`  
		Last Modified: Tue, 29 Jul 2025 18:35:07 GMT  
		Size: 96.2 KB (96180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55325ecc9b276e9c55badf949ed4f06840c34aa8baf0aa6f974e0b90dc5d4e0d`  
		Last Modified: Tue, 29 Jul 2025 18:35:07 GMT  
		Size: 20.6 KB (20572 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.22` - linux; arm variant v6

```console
$ docker pull memcached@sha256:78b59dd3af5a55e950f5106869e642af122a7dc470545f4ba533f6833d83b62c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5550795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb09d5ce1b7010f7a36d77494bc5358d666339628c183692906db6a961373847`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c710b5ddcc2882c5014d0c8cb93aec2bd8b6cc3c59fd42b40c87d94f89a7bc7f`  
		Last Modified: Wed, 23 Jul 2025 22:59:16 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c42040d822a4af7f05f9ccd4d18a7a5e4712b118b7f18d1a7969761029a9d2`  
		Last Modified: Wed, 23 Jul 2025 22:59:16 GMT  
		Size: 101.5 KB (101533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3095e18cd24048696efd57ac64d04dde381a3abde625964e02165c7364eb5633`  
		Last Modified: Tue, 29 Jul 2025 16:50:12 GMT  
		Size: 1.9 MB (1947003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0436ec50f04ed972ff0dd760f7e820f192236e5e720bddb6173f65159c7c36`  
		Last Modified: Tue, 29 Jul 2025 16:50:11 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671c24aae36bb04a32e05bd64e1371384f594889cdbbc41029c916447666d402`  
		Last Modified: Tue, 29 Jul 2025 16:50:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:c2a050c6822d834285577c3a001fdfcf9949b7f5a483a4a76a49b549bea19641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54e8bda3e734528caeab4505f084ca7a3076d5ec2273287f66954b5e91af42f`

```dockerfile
```

-	Layers:
	-	`sha256:0d86924831d61ce8b792b25421e9ff0fa2eda9ab940eba5309d44d0eeada7e8e`  
		Last Modified: Tue, 29 Jul 2025 18:35:11 GMT  
		Size: 20.5 KB (20506 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.22` - linux; arm variant v7

```console
$ docker pull memcached@sha256:c9f5db2389b9b0b4a2cd199c4417a9f49a60c42d616e8421177e662d4830de07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5217393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9421ed030d4b6b6405714612b8858bda87bc53ac8b0c5ed65c582119527f2d9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251060498ca8f0484e20714689b9caba533d09c1b74ed8f2a06780db515a28e2`  
		Last Modified: Thu, 24 Jul 2025 00:27:37 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2293bd2fb47d57e5869c197133067e17f9b1e51ea0f298af1e480e7fd33d681`  
		Last Modified: Thu, 24 Jul 2025 00:27:38 GMT  
		Size: 91.3 KB (91313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ae82f2bac2f7e6fe57f8cb7006fc227c972da1ae5749eba9f5f73e6f3248ec`  
		Last Modified: Tue, 29 Jul 2025 17:11:51 GMT  
		Size: 1.9 MB (1905692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e60bf2b2164c620b69e40bdcb64d4104d02eab86c96ea6e170a3601b9ecfd82`  
		Last Modified: Tue, 29 Jul 2025 17:11:51 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:665fe4cd856f1a5c2193568e756c572656949b17c381fc8d43efaa823e18cfa7`  
		Last Modified: Tue, 29 Jul 2025 17:11:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:376a71bc0fef7741e92fdae8b96c825c4622e980de01e724b1a3a0bec3d95f20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 KB (116963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22b574f6c6d021a917c0e99ff4800d8ac3c22fb94b94f88c404cc7609f562fb5`

```dockerfile
```

-	Layers:
	-	`sha256:58ebd4bc7ee5888c552e0fa618f93aefbdb1d15a56ecd3abef19a46ce2f93eee`  
		Last Modified: Tue, 29 Jul 2025 18:35:15 GMT  
		Size: 96.2 KB (96248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d432ed2053ed8249834dd5016fe3199bbc3f82dc7013027c3ead9efe2a007b98`  
		Last Modified: Tue, 29 Jul 2025 18:35:16 GMT  
		Size: 20.7 KB (20715 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:b5e4ecc3e927ee30e5cfcfc8aa044960631c75eb8abed9d0fcee6232aa5fdf79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6241700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40c880dc2c785861dc9010b813bb6f533f30518443a3bb7e7f477bc96af14582`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfbfeb6ac9fd2045c5bea10a301ad554c1f703ffc2885c41520dd5e42eb4a59a`  
		Last Modified: Tue, 29 Jul 2025 16:41:08 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47acaa5035f94aed634b9d7ecae02fb3838f19e38f8e752ecd6cfba97699b31`  
		Last Modified: Tue, 29 Jul 2025 16:41:08 GMT  
		Size: 120.8 KB (120812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8160f3136c6863b52f0dec4f9918b91b8a509700b2071ec0aecd5a6231f00f2a`  
		Last Modified: Tue, 29 Jul 2025 16:41:09 GMT  
		Size: 2.0 MB (1988782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff22f0cad01950efb78a7a862b0becb8b2fd22d795b585f97dad66c091c3dd7`  
		Last Modified: Tue, 29 Jul 2025 16:41:08 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed19cbfb574c7d8cab364e2ec072c0e03f694468ada41cd70bfcd35392df9e7`  
		Last Modified: Tue, 29 Jul 2025 16:41:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:b4c81c7ababb91ecdda3b7d70514d16818602199d759eb2aadd74de732d52960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.1 KB (117055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80452fd4f79f6e7a0dab0beebf5c144f9df7c257255cdd3cb93ccbff77001fd6`

```dockerfile
```

-	Layers:
	-	`sha256:f11d2a322f6088804ee63ae1a77b9d5ddcdfdc0c65c22e7a70b7ee67cf4532ed`  
		Last Modified: Tue, 29 Jul 2025 18:35:20 GMT  
		Size: 96.3 KB (96284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e225dd6ea14146ddf445598f24189c065ec684fbeb92e7d053a0211a7d60efda`  
		Last Modified: Tue, 29 Jul 2025 18:35:21 GMT  
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
$ docker pull memcached@sha256:04386ede5dcbf35cabad144bcdc951cc64882f7b9727f2d09927fe0d5551dd19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5942089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8252590eee78d67456ac83fd8279259aaea4d2a555c8bc20b173663fcaa2883`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc22e0cec7e7fe8cff10539bca58363ad6749e2de4f878015c25b5f2b6ecadb9`  
		Last Modified: Tue, 29 Jul 2025 16:33:46 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992ebe18219bd78e59e7e56661aae22f700927f47bc7ad1dfe7717093b371c15`  
		Last Modified: Tue, 29 Jul 2025 16:33:49 GMT  
		Size: 124.3 KB (124315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953f5a37d23881d59809ea64dc6ebf1a152a1ff8929f51befb10577771755f5d`  
		Last Modified: Tue, 29 Jul 2025 16:33:49 GMT  
		Size: 2.1 MB (2089310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10b62870a2d7b266495d83cfd72dcf702c91c5c60a7e29836bd9bdac776511a7`  
		Last Modified: Tue, 29 Jul 2025 16:33:47 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1cc8c0fe9a4ef7e2ef70e32ddbfbd2fd68985dd452630a8f390c5b41c654f8`  
		Last Modified: Tue, 29 Jul 2025 16:33:47 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:cf7e9735e4ef5d00dc25928653b808214f070708e9d879ef54afc4d77ce9db2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcceb455cfdb86bdb0c165af3bc54cbab794d56fef1dbae2b484d28027db791c`

```dockerfile
```

-	Layers:
	-	`sha256:a40704a0afb5cf1b90c0fbdf73c5218a4d8f0e93bb39014507b5fa5f8c7265dd`  
		Last Modified: Tue, 29 Jul 2025 18:35:29 GMT  
		Size: 94.3 KB (94287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da22397f364310e72420738395739c36e25b4e4813bbc5da197582a91bb55ac9`  
		Last Modified: Tue, 29 Jul 2025 18:35:29 GMT  
		Size: 20.6 KB (20648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.22` - linux; riscv64

```console
$ docker pull memcached@sha256:d55b98c34ba1c2f546461bd57477d46ab868f9de6b107ffb8f20e06dab1e10d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5555034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1034dde2661f43165e85db9a13ff0e10d237d14d4b1b7ee1d4570f19d7df4e69`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00bbdcecb4dec3cbaba0500f9425897948884cfd8db95ccdf9b824d448b24049`  
		Last Modified: Wed, 23 Jul 2025 23:54:15 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c18051d55886d147cafcee8f9e220087c0b60c0e11ec8898a4005352ee0f7e4`  
		Last Modified: Wed, 23 Jul 2025 23:50:14 GMT  
		Size: 107.9 KB (107902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953c2b44fe537b63907764cf78cbb294c6a1133eacb39c62d35ee5d4914779cb`  
		Last Modified: Tue, 29 Jul 2025 16:42:10 GMT  
		Size: 1.9 MB (1932977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d69b2f63abf91684a15b9de7b5e617996762376da3fdda50c4e20c2f1e0f4da`  
		Last Modified: Tue, 29 Jul 2025 16:42:10 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f57c134601fc15e8f2cf183cfd9a3057731ad48b915988217f51df31b5d3cf38`  
		Last Modified: Tue, 29 Jul 2025 16:42:10 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:d50b42de80ef3381b05da20cef4ba6ab4491facb607528e075c034257fe9d327
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27766c161110b7e46063a39ce6e176f87233fd6722a825ec338e1568892a77a3`

```dockerfile
```

-	Layers:
	-	`sha256:f933f968a4a14795196607a1337a19431e9f61db78bb49c5c2f89f64a17a1d89`  
		Last Modified: Tue, 29 Jul 2025 18:35:33 GMT  
		Size: 94.3 KB (94283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffc41094fe9f57bca69da70bbb18eca52aaf6d27d0fb6d79eda79f9e011a157a`  
		Last Modified: Tue, 29 Jul 2025 18:35:33 GMT  
		Size: 20.6 KB (20647 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.22` - linux; s390x

```console
$ docker pull memcached@sha256:cfd223eb11df3d2297224d458caf974f3f0aae4742ff917812f1b8c84c84e705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5797268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78e23f18e891a12e72ef84139504baf8783a7db21d4976fc0b607f8e9bbf736f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f00131fb0ca26b15f1ac64b82554fc342b19f8c1ef38312a75addb6686f7bc24`  
		Last Modified: Tue, 29 Jul 2025 16:41:40 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e54da6ab620e035fd78987688d45401e87278ec8a5c02cef8a57e4ea9fd286`  
		Last Modified: Tue, 29 Jul 2025 16:41:42 GMT  
		Size: 113.5 KB (113499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6160f9fac1fd86eda224e9ce4740ea46f7e23dc7edb6d1fe9d830001313e63a`  
		Last Modified: Tue, 29 Jul 2025 16:41:46 GMT  
		Size: 2.0 MB (2037446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d01cd71d33b01b420652f4ad9275f1475f4f0bf253dc0a1b48198df2010be5`  
		Last Modified: Tue, 29 Jul 2025 16:41:52 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:831dd5e3c39dd2744dc8823190095f709c36020b55ccdaf85f62a146582c7d9d`  
		Last Modified: Tue, 29 Jul 2025 16:41:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:79f0de7e4dcc9afdbfa1fa22250cf3e544d6f3c33174246b427d2865c7e343d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71dad4d71741d8d354038cb6898389aebb54c956dfcd865d57f78dcc3b238bf8`

```dockerfile
```

-	Layers:
	-	`sha256:f942bbb9520308ae352a056c148fdce8f6b09672c257e0a769aa2504bacf1845`  
		Last Modified: Tue, 29 Jul 2025 18:35:37 GMT  
		Size: 94.2 KB (94229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c46680ef7cf08a43965ab9c7727cc70268ee89e366a1ce1806d0f7980b4ad812`  
		Last Modified: Tue, 29 Jul 2025 18:35:38 GMT  
		Size: 20.6 KB (20574 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-trixie`

```console
$ docker pull memcached@sha256:157c563eef6954ac0bc583c36def96d8ed2d3b3c5b37214f27d210ac53942386
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
$ docker pull memcached@sha256:742d5665f0f292e1278bafd0dff520b5f4edb101c587c29fb0ef273f9d7e124f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30319041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc1024c223c5953b97de26e48cce8df89bee4493e37781f6826e6df56c590056`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1759104000'
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
	-	`sha256:d2a243ecf382412941b4d6772dba911a8093cf3703c933872fbb7ecc21e27e20`  
		Last Modified: Mon, 29 Sep 2025 23:34:24 GMT  
		Size: 27.9 MB (27946145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d24bdf1148108d2d3fc42a07dae247e5242de03db9a71e04066262a853f139d`  
		Last Modified: Mon, 29 Sep 2025 23:59:31 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e717ac34c0d292ae77e9118ac1581d40d881e518d32d9e64f01fddf818164b`  
		Last Modified: Mon, 29 Sep 2025 23:59:31 GMT  
		Size: 144.0 KB (144036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a3b7d16c874ce52964b6ba216127f7fcf604d326cc965210eb58119d605d28`  
		Last Modified: Mon, 29 Sep 2025 23:59:31 GMT  
		Size: 2.2 MB (2227345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb7f38fc7bbd06b5c988a48649d103d93ab0d8011b6a4f5bd8ad38bbd4cac432`  
		Last Modified: Mon, 29 Sep 2025 23:59:31 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5307470e3430d06e3f04b798774d1905a98a13f5ba3387596a0aa97e34b7eba`  
		Last Modified: Mon, 29 Sep 2025 23:59:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:92764b7963e735b77f5e5b433bf1311bc919679a81273cf442178538cf7da2ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:512f0e0d6001116f7984270337608de656664abeb7602b6fc4add42303ba8ee6`

```dockerfile
```

-	Layers:
	-	`sha256:a8fc1cbacd56787b740b886369c6eaafa6151c97fade289ea774600c03a80e11`  
		Last Modified: Tue, 30 Sep 2025 00:34:39 GMT  
		Size: 2.0 MB (2011183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57884b3635fcf7e290933e3a1da7210a05c98ab3187a6e484a5cc8cedf845e98`  
		Last Modified: Tue, 30 Sep 2025 00:34:39 GMT  
		Size: 22.3 KB (22347 bytes)  
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
$ docker pull memcached@sha256:5a071a15dfae20029d56a8845f8053a4f4447934a87e0db0678b6f4ddc2e924a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36187246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6957fdbfa2f978334c6c02013b0e9b928534ddf41009ccae3597ccaf389fd455`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
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
	-	`sha256:8bcecd3ced4047f6a4d35464fc2ee9b45e7fcc10b49690427794f4421b0552ab`  
		Last Modified: Mon, 29 Sep 2025 23:41:19 GMT  
		Size: 33.6 MB (33598454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cee3e1fdea897c6a6b3a982e1918145b5bcd716e5ae6ed66b5e7184e651e059`  
		Last Modified: Tue, 30 Sep 2025 07:50:11 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dea6ee42e2fcf50b7f0d213d52ea27f8eebdaf12c0aa80c5df4828c4566af25`  
		Last Modified: Tue, 30 Sep 2025 07:50:12 GMT  
		Size: 170.3 KB (170259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629d93745cabb21520c860c7612f141299a2c0f2632cf40b7dcc88799307dcd7`  
		Last Modified: Tue, 30 Sep 2025 07:50:13 GMT  
		Size: 2.4 MB (2417019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afbd1630af2c91474bfc04cf614cc4d0a7093510b706f978f20f426127e93305`  
		Last Modified: Tue, 30 Sep 2025 07:50:12 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8293ad839e50f443a419fb4c0f6a6dbde6204ad3bf467cdff6e99385a7d1c3`  
		Last Modified: Tue, 30 Sep 2025 07:50:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:987b950cf472a2d95cc860d4c3c9e95c51ab792c33f5ac61607b7e4f38d1d8d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:973c6753846fed972084489bd202cf7da6e77ddc33d584a90658a8949b5730ee`

```dockerfile
```

-	Layers:
	-	`sha256:821a5821beef4d6bdae90ea0d98277dd982af05804dd43f706310bc7263244c4`  
		Last Modified: Wed, 01 Oct 2025 21:34:36 GMT  
		Size: 2.0 MB (2011781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:222d48bb5ef6a86d72ecccaf90a1cd7cf49c644139aee33815b1e7d0fd87cfcb`  
		Last Modified: Wed, 01 Oct 2025 21:34:36 GMT  
		Size: 22.3 KB (22270 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; riscv64

```console
$ docker pull memcached@sha256:31bb76b9b98cd96febc6b1d5056f839ffab9aaaa12690d0a47353df1b2b49221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30629784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e010912f76722a300766eb6afe7e6b13e8f72682c8dec557d00826b2a7cba503`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1759104000'
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
	-	`sha256:ecc6f9aec21fb94a493c2875c244e720a2f7c6c034063ce87b2f5b6b46962ec9`  
		Last Modified: Tue, 30 Sep 2025 01:05:14 GMT  
		Size: 28.3 MB (28275502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c2f28b5ea15f2b021d2f93df684963b9d27de2301bfccbf53d01abc5bdaa97`  
		Last Modified: Tue, 30 Sep 2025 04:00:18 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179b31cc3aad1ab89917cf87cb268b6e8e4291ec4b8996317231c4ac0003ebf9`  
		Last Modified: Tue, 30 Sep 2025 04:00:18 GMT  
		Size: 133.0 KB (132970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca5db35fb11036dcb8f2d55bbe271869356c9b4b2e08c0d0293a9b0c894f5dff`  
		Last Modified: Tue, 30 Sep 2025 04:00:19 GMT  
		Size: 2.2 MB (2219797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc4c908359c51ce26778438a3886b2eb2d6987ee3a22862dbdbe2056a3cd95d`  
		Last Modified: Tue, 30 Sep 2025 04:00:19 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7254f9df049c190c1c3ffa9794b395fb4e3ec7ab18b8dce7a58733c63a54dd`  
		Last Modified: Tue, 30 Sep 2025 04:00:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:10dcedf955ee46896155ca87f9a292967d1ce021fbab41f3a0fc44045a885e25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85a06d87da790b7800c970ca38989414eeae6c950cf890286591dc59c6163cc5`

```dockerfile
```

-	Layers:
	-	`sha256:b8fb80942d713e49171d0a98b2306b7bbb0023e57f180295e56893f7ea7f458d`  
		Last Modified: Tue, 30 Sep 2025 06:34:34 GMT  
		Size: 2.0 MB (2002144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cbc67dcbbe8db9619b2b3e3b962ebb7d9640901e2048fa63620351cc03d940d`  
		Last Modified: Tue, 30 Sep 2025 06:34:34 GMT  
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
$ docker pull memcached@sha256:157c563eef6954ac0bc583c36def96d8ed2d3b3c5b37214f27d210ac53942386
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
$ docker pull memcached@sha256:742d5665f0f292e1278bafd0dff520b5f4edb101c587c29fb0ef273f9d7e124f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30319041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc1024c223c5953b97de26e48cce8df89bee4493e37781f6826e6df56c590056`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1759104000'
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
	-	`sha256:d2a243ecf382412941b4d6772dba911a8093cf3703c933872fbb7ecc21e27e20`  
		Last Modified: Mon, 29 Sep 2025 23:34:24 GMT  
		Size: 27.9 MB (27946145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d24bdf1148108d2d3fc42a07dae247e5242de03db9a71e04066262a853f139d`  
		Last Modified: Mon, 29 Sep 2025 23:59:31 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e717ac34c0d292ae77e9118ac1581d40d881e518d32d9e64f01fddf818164b`  
		Last Modified: Mon, 29 Sep 2025 23:59:31 GMT  
		Size: 144.0 KB (144036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a3b7d16c874ce52964b6ba216127f7fcf604d326cc965210eb58119d605d28`  
		Last Modified: Mon, 29 Sep 2025 23:59:31 GMT  
		Size: 2.2 MB (2227345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb7f38fc7bbd06b5c988a48649d103d93ab0d8011b6a4f5bd8ad38bbd4cac432`  
		Last Modified: Mon, 29 Sep 2025 23:59:31 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5307470e3430d06e3f04b798774d1905a98a13f5ba3387596a0aa97e34b7eba`  
		Last Modified: Mon, 29 Sep 2025 23:59:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:92764b7963e735b77f5e5b433bf1311bc919679a81273cf442178538cf7da2ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:512f0e0d6001116f7984270337608de656664abeb7602b6fc4add42303ba8ee6`

```dockerfile
```

-	Layers:
	-	`sha256:a8fc1cbacd56787b740b886369c6eaafa6151c97fade289ea774600c03a80e11`  
		Last Modified: Tue, 30 Sep 2025 00:34:39 GMT  
		Size: 2.0 MB (2011183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57884b3635fcf7e290933e3a1da7210a05c98ab3187a6e484a5cc8cedf845e98`  
		Last Modified: Tue, 30 Sep 2025 00:34:39 GMT  
		Size: 22.3 KB (22347 bytes)  
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
$ docker pull memcached@sha256:5a071a15dfae20029d56a8845f8053a4f4447934a87e0db0678b6f4ddc2e924a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36187246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6957fdbfa2f978334c6c02013b0e9b928534ddf41009ccae3597ccaf389fd455`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
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
	-	`sha256:8bcecd3ced4047f6a4d35464fc2ee9b45e7fcc10b49690427794f4421b0552ab`  
		Last Modified: Mon, 29 Sep 2025 23:41:19 GMT  
		Size: 33.6 MB (33598454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cee3e1fdea897c6a6b3a982e1918145b5bcd716e5ae6ed66b5e7184e651e059`  
		Last Modified: Tue, 30 Sep 2025 07:50:11 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dea6ee42e2fcf50b7f0d213d52ea27f8eebdaf12c0aa80c5df4828c4566af25`  
		Last Modified: Tue, 30 Sep 2025 07:50:12 GMT  
		Size: 170.3 KB (170259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629d93745cabb21520c860c7612f141299a2c0f2632cf40b7dcc88799307dcd7`  
		Last Modified: Tue, 30 Sep 2025 07:50:13 GMT  
		Size: 2.4 MB (2417019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afbd1630af2c91474bfc04cf614cc4d0a7093510b706f978f20f426127e93305`  
		Last Modified: Tue, 30 Sep 2025 07:50:12 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8293ad839e50f443a419fb4c0f6a6dbde6204ad3bf467cdff6e99385a7d1c3`  
		Last Modified: Tue, 30 Sep 2025 07:50:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:987b950cf472a2d95cc860d4c3c9e95c51ab792c33f5ac61607b7e4f38d1d8d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:973c6753846fed972084489bd202cf7da6e77ddc33d584a90658a8949b5730ee`

```dockerfile
```

-	Layers:
	-	`sha256:821a5821beef4d6bdae90ea0d98277dd982af05804dd43f706310bc7263244c4`  
		Last Modified: Wed, 01 Oct 2025 21:34:36 GMT  
		Size: 2.0 MB (2011781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:222d48bb5ef6a86d72ecccaf90a1cd7cf49c644139aee33815b1e7d0fd87cfcb`  
		Last Modified: Wed, 01 Oct 2025 21:34:36 GMT  
		Size: 22.3 KB (22270 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; riscv64

```console
$ docker pull memcached@sha256:31bb76b9b98cd96febc6b1d5056f839ffab9aaaa12690d0a47353df1b2b49221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30629784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e010912f76722a300766eb6afe7e6b13e8f72682c8dec557d00826b2a7cba503`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1759104000'
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
	-	`sha256:ecc6f9aec21fb94a493c2875c244e720a2f7c6c034063ce87b2f5b6b46962ec9`  
		Last Modified: Tue, 30 Sep 2025 01:05:14 GMT  
		Size: 28.3 MB (28275502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c2f28b5ea15f2b021d2f93df684963b9d27de2301bfccbf53d01abc5bdaa97`  
		Last Modified: Tue, 30 Sep 2025 04:00:18 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179b31cc3aad1ab89917cf87cb268b6e8e4291ec4b8996317231c4ac0003ebf9`  
		Last Modified: Tue, 30 Sep 2025 04:00:18 GMT  
		Size: 133.0 KB (132970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca5db35fb11036dcb8f2d55bbe271869356c9b4b2e08c0d0293a9b0c894f5dff`  
		Last Modified: Tue, 30 Sep 2025 04:00:19 GMT  
		Size: 2.2 MB (2219797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc4c908359c51ce26778438a3886b2eb2d6987ee3a22862dbdbe2056a3cd95d`  
		Last Modified: Tue, 30 Sep 2025 04:00:19 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7254f9df049c190c1c3ffa9794b395fb4e3ec7ab18b8dce7a58733c63a54dd`  
		Last Modified: Tue, 30 Sep 2025 04:00:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:10dcedf955ee46896155ca87f9a292967d1ce021fbab41f3a0fc44045a885e25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85a06d87da790b7800c970ca38989414eeae6c950cf890286591dc59c6163cc5`

```dockerfile
```

-	Layers:
	-	`sha256:b8fb80942d713e49171d0a98b2306b7bbb0023e57f180295e56893f7ea7f458d`  
		Last Modified: Tue, 30 Sep 2025 06:34:34 GMT  
		Size: 2.0 MB (2002144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cbc67dcbbe8db9619b2b3e3b962ebb7d9640901e2048fa63620351cc03d940d`  
		Last Modified: Tue, 30 Sep 2025 06:34:34 GMT  
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
$ docker pull memcached@sha256:eca5d776fe62e6ffe5e27e1a4d357e0bbd9ac609a271243c210599a898122ad2
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
$ docker pull memcached@sha256:033134f4dd9f45d4e22b6e98b040ea3fccf0dca740af3c949b44bebf458b04d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5904246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca259aa2216a248c482fc8a069d48b1e70b087529d2c3de97154bfa458dbb7a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23fb46bc7dee2beda6f5f6f567aecd4d7d7698b9749ed917988a859b7dd96e30`  
		Last Modified: Tue, 29 Jul 2025 16:32:22 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48faf8c85515fb9d17e0752e77d8241f223d53b1adc90439c606d17daabd0ae`  
		Last Modified: Tue, 29 Jul 2025 16:32:24 GMT  
		Size: 104.7 KB (104725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d552a2d777fd444b41cb79438f9f1b441821162e78d73e96dc848a773cf43892`  
		Last Modified: Tue, 29 Jul 2025 16:32:24 GMT  
		Size: 2.0 MB (1998477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c70665f30f3e15975d429b494cb17b21c5d4630c1800cb0addc3fce3a11aa29`  
		Last Modified: Tue, 29 Jul 2025 16:32:20 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ff68520caaf588cec750ad7c403cf55d79eecfff4b7a4ac5eb3910c90c2817`  
		Last Modified: Tue, 29 Jul 2025 16:32:21 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7b27e0df383f45d6d523345a078898524a69cee4d6978cf64bf26532b8679dca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 KB (116752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb88e7ee6d3e67b2e4f307c081504a685666917ddf50770fe8beb5abd60a3dc5`

```dockerfile
```

-	Layers:
	-	`sha256:2cf00a09ffccb2c00421311314137de90d0586c126b79dbe5315ce321c168b34`  
		Last Modified: Tue, 29 Jul 2025 18:35:07 GMT  
		Size: 96.2 KB (96180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55325ecc9b276e9c55badf949ed4f06840c34aa8baf0aa6f974e0b90dc5d4e0d`  
		Last Modified: Tue, 29 Jul 2025 18:35:07 GMT  
		Size: 20.6 KB (20572 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:78b59dd3af5a55e950f5106869e642af122a7dc470545f4ba533f6833d83b62c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5550795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb09d5ce1b7010f7a36d77494bc5358d666339628c183692906db6a961373847`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c710b5ddcc2882c5014d0c8cb93aec2bd8b6cc3c59fd42b40c87d94f89a7bc7f`  
		Last Modified: Wed, 23 Jul 2025 22:59:16 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c42040d822a4af7f05f9ccd4d18a7a5e4712b118b7f18d1a7969761029a9d2`  
		Last Modified: Wed, 23 Jul 2025 22:59:16 GMT  
		Size: 101.5 KB (101533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3095e18cd24048696efd57ac64d04dde381a3abde625964e02165c7364eb5633`  
		Last Modified: Tue, 29 Jul 2025 16:50:12 GMT  
		Size: 1.9 MB (1947003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0436ec50f04ed972ff0dd760f7e820f192236e5e720bddb6173f65159c7c36`  
		Last Modified: Tue, 29 Jul 2025 16:50:11 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671c24aae36bb04a32e05bd64e1371384f594889cdbbc41029c916447666d402`  
		Last Modified: Tue, 29 Jul 2025 16:50:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:c2a050c6822d834285577c3a001fdfcf9949b7f5a483a4a76a49b549bea19641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54e8bda3e734528caeab4505f084ca7a3076d5ec2273287f66954b5e91af42f`

```dockerfile
```

-	Layers:
	-	`sha256:0d86924831d61ce8b792b25421e9ff0fa2eda9ab940eba5309d44d0eeada7e8e`  
		Last Modified: Tue, 29 Jul 2025 18:35:11 GMT  
		Size: 20.5 KB (20506 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:c9f5db2389b9b0b4a2cd199c4417a9f49a60c42d616e8421177e662d4830de07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5217393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9421ed030d4b6b6405714612b8858bda87bc53ac8b0c5ed65c582119527f2d9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251060498ca8f0484e20714689b9caba533d09c1b74ed8f2a06780db515a28e2`  
		Last Modified: Thu, 24 Jul 2025 00:27:37 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2293bd2fb47d57e5869c197133067e17f9b1e51ea0f298af1e480e7fd33d681`  
		Last Modified: Thu, 24 Jul 2025 00:27:38 GMT  
		Size: 91.3 KB (91313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ae82f2bac2f7e6fe57f8cb7006fc227c972da1ae5749eba9f5f73e6f3248ec`  
		Last Modified: Tue, 29 Jul 2025 17:11:51 GMT  
		Size: 1.9 MB (1905692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e60bf2b2164c620b69e40bdcb64d4104d02eab86c96ea6e170a3601b9ecfd82`  
		Last Modified: Tue, 29 Jul 2025 17:11:51 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:665fe4cd856f1a5c2193568e756c572656949b17c381fc8d43efaa823e18cfa7`  
		Last Modified: Tue, 29 Jul 2025 17:11:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:376a71bc0fef7741e92fdae8b96c825c4622e980de01e724b1a3a0bec3d95f20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 KB (116963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22b574f6c6d021a917c0e99ff4800d8ac3c22fb94b94f88c404cc7609f562fb5`

```dockerfile
```

-	Layers:
	-	`sha256:58ebd4bc7ee5888c552e0fa618f93aefbdb1d15a56ecd3abef19a46ce2f93eee`  
		Last Modified: Tue, 29 Jul 2025 18:35:15 GMT  
		Size: 96.2 KB (96248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d432ed2053ed8249834dd5016fe3199bbc3f82dc7013027c3ead9efe2a007b98`  
		Last Modified: Tue, 29 Jul 2025 18:35:16 GMT  
		Size: 20.7 KB (20715 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:b5e4ecc3e927ee30e5cfcfc8aa044960631c75eb8abed9d0fcee6232aa5fdf79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6241700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40c880dc2c785861dc9010b813bb6f533f30518443a3bb7e7f477bc96af14582`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfbfeb6ac9fd2045c5bea10a301ad554c1f703ffc2885c41520dd5e42eb4a59a`  
		Last Modified: Tue, 29 Jul 2025 16:41:08 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47acaa5035f94aed634b9d7ecae02fb3838f19e38f8e752ecd6cfba97699b31`  
		Last Modified: Tue, 29 Jul 2025 16:41:08 GMT  
		Size: 120.8 KB (120812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8160f3136c6863b52f0dec4f9918b91b8a509700b2071ec0aecd5a6231f00f2a`  
		Last Modified: Tue, 29 Jul 2025 16:41:09 GMT  
		Size: 2.0 MB (1988782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff22f0cad01950efb78a7a862b0becb8b2fd22d795b585f97dad66c091c3dd7`  
		Last Modified: Tue, 29 Jul 2025 16:41:08 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed19cbfb574c7d8cab364e2ec072c0e03f694468ada41cd70bfcd35392df9e7`  
		Last Modified: Tue, 29 Jul 2025 16:41:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:b4c81c7ababb91ecdda3b7d70514d16818602199d759eb2aadd74de732d52960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.1 KB (117055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80452fd4f79f6e7a0dab0beebf5c144f9df7c257255cdd3cb93ccbff77001fd6`

```dockerfile
```

-	Layers:
	-	`sha256:f11d2a322f6088804ee63ae1a77b9d5ddcdfdc0c65c22e7a70b7ee67cf4532ed`  
		Last Modified: Tue, 29 Jul 2025 18:35:20 GMT  
		Size: 96.3 KB (96284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e225dd6ea14146ddf445598f24189c065ec684fbeb92e7d053a0211a7d60efda`  
		Last Modified: Tue, 29 Jul 2025 18:35:21 GMT  
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
$ docker pull memcached@sha256:04386ede5dcbf35cabad144bcdc951cc64882f7b9727f2d09927fe0d5551dd19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5942089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8252590eee78d67456ac83fd8279259aaea4d2a555c8bc20b173663fcaa2883`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc22e0cec7e7fe8cff10539bca58363ad6749e2de4f878015c25b5f2b6ecadb9`  
		Last Modified: Tue, 29 Jul 2025 16:33:46 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992ebe18219bd78e59e7e56661aae22f700927f47bc7ad1dfe7717093b371c15`  
		Last Modified: Tue, 29 Jul 2025 16:33:49 GMT  
		Size: 124.3 KB (124315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953f5a37d23881d59809ea64dc6ebf1a152a1ff8929f51befb10577771755f5d`  
		Last Modified: Tue, 29 Jul 2025 16:33:49 GMT  
		Size: 2.1 MB (2089310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10b62870a2d7b266495d83cfd72dcf702c91c5c60a7e29836bd9bdac776511a7`  
		Last Modified: Tue, 29 Jul 2025 16:33:47 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1cc8c0fe9a4ef7e2ef70e32ddbfbd2fd68985dd452630a8f390c5b41c654f8`  
		Last Modified: Tue, 29 Jul 2025 16:33:47 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:cf7e9735e4ef5d00dc25928653b808214f070708e9d879ef54afc4d77ce9db2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcceb455cfdb86bdb0c165af3bc54cbab794d56fef1dbae2b484d28027db791c`

```dockerfile
```

-	Layers:
	-	`sha256:a40704a0afb5cf1b90c0fbdf73c5218a4d8f0e93bb39014507b5fa5f8c7265dd`  
		Last Modified: Tue, 29 Jul 2025 18:35:29 GMT  
		Size: 94.3 KB (94287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da22397f364310e72420738395739c36e25b4e4813bbc5da197582a91bb55ac9`  
		Last Modified: Tue, 29 Jul 2025 18:35:29 GMT  
		Size: 20.6 KB (20648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:d55b98c34ba1c2f546461bd57477d46ab868f9de6b107ffb8f20e06dab1e10d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5555034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1034dde2661f43165e85db9a13ff0e10d237d14d4b1b7ee1d4570f19d7df4e69`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00bbdcecb4dec3cbaba0500f9425897948884cfd8db95ccdf9b824d448b24049`  
		Last Modified: Wed, 23 Jul 2025 23:54:15 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c18051d55886d147cafcee8f9e220087c0b60c0e11ec8898a4005352ee0f7e4`  
		Last Modified: Wed, 23 Jul 2025 23:50:14 GMT  
		Size: 107.9 KB (107902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953c2b44fe537b63907764cf78cbb294c6a1133eacb39c62d35ee5d4914779cb`  
		Last Modified: Tue, 29 Jul 2025 16:42:10 GMT  
		Size: 1.9 MB (1932977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d69b2f63abf91684a15b9de7b5e617996762376da3fdda50c4e20c2f1e0f4da`  
		Last Modified: Tue, 29 Jul 2025 16:42:10 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f57c134601fc15e8f2cf183cfd9a3057731ad48b915988217f51df31b5d3cf38`  
		Last Modified: Tue, 29 Jul 2025 16:42:10 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:d50b42de80ef3381b05da20cef4ba6ab4491facb607528e075c034257fe9d327
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27766c161110b7e46063a39ce6e176f87233fd6722a825ec338e1568892a77a3`

```dockerfile
```

-	Layers:
	-	`sha256:f933f968a4a14795196607a1337a19431e9f61db78bb49c5c2f89f64a17a1d89`  
		Last Modified: Tue, 29 Jul 2025 18:35:33 GMT  
		Size: 94.3 KB (94283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffc41094fe9f57bca69da70bbb18eca52aaf6d27d0fb6d79eda79f9e011a157a`  
		Last Modified: Tue, 29 Jul 2025 18:35:33 GMT  
		Size: 20.6 KB (20647 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:cfd223eb11df3d2297224d458caf974f3f0aae4742ff917812f1b8c84c84e705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5797268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78e23f18e891a12e72ef84139504baf8783a7db21d4976fc0b607f8e9bbf736f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f00131fb0ca26b15f1ac64b82554fc342b19f8c1ef38312a75addb6686f7bc24`  
		Last Modified: Tue, 29 Jul 2025 16:41:40 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e54da6ab620e035fd78987688d45401e87278ec8a5c02cef8a57e4ea9fd286`  
		Last Modified: Tue, 29 Jul 2025 16:41:42 GMT  
		Size: 113.5 KB (113499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6160f9fac1fd86eda224e9ce4740ea46f7e23dc7edb6d1fe9d830001313e63a`  
		Last Modified: Tue, 29 Jul 2025 16:41:46 GMT  
		Size: 2.0 MB (2037446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d01cd71d33b01b420652f4ad9275f1475f4f0bf253dc0a1b48198df2010be5`  
		Last Modified: Tue, 29 Jul 2025 16:41:52 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:831dd5e3c39dd2744dc8823190095f709c36020b55ccdaf85f62a146582c7d9d`  
		Last Modified: Tue, 29 Jul 2025 16:41:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:79f0de7e4dcc9afdbfa1fa22250cf3e544d6f3c33174246b427d2865c7e343d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71dad4d71741d8d354038cb6898389aebb54c956dfcd865d57f78dcc3b238bf8`

```dockerfile
```

-	Layers:
	-	`sha256:f942bbb9520308ae352a056c148fdce8f6b09672c257e0a769aa2504bacf1845`  
		Last Modified: Tue, 29 Jul 2025 18:35:37 GMT  
		Size: 94.2 KB (94229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c46680ef7cf08a43965ab9c7727cc70268ee89e366a1ce1806d0f7980b4ad812`  
		Last Modified: Tue, 29 Jul 2025 18:35:38 GMT  
		Size: 20.6 KB (20574 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine3.22`

```console
$ docker pull memcached@sha256:eca5d776fe62e6ffe5e27e1a4d357e0bbd9ac609a271243c210599a898122ad2
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
$ docker pull memcached@sha256:033134f4dd9f45d4e22b6e98b040ea3fccf0dca740af3c949b44bebf458b04d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5904246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca259aa2216a248c482fc8a069d48b1e70b087529d2c3de97154bfa458dbb7a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23fb46bc7dee2beda6f5f6f567aecd4d7d7698b9749ed917988a859b7dd96e30`  
		Last Modified: Tue, 29 Jul 2025 16:32:22 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48faf8c85515fb9d17e0752e77d8241f223d53b1adc90439c606d17daabd0ae`  
		Last Modified: Tue, 29 Jul 2025 16:32:24 GMT  
		Size: 104.7 KB (104725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d552a2d777fd444b41cb79438f9f1b441821162e78d73e96dc848a773cf43892`  
		Last Modified: Tue, 29 Jul 2025 16:32:24 GMT  
		Size: 2.0 MB (1998477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c70665f30f3e15975d429b494cb17b21c5d4630c1800cb0addc3fce3a11aa29`  
		Last Modified: Tue, 29 Jul 2025 16:32:20 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ff68520caaf588cec750ad7c403cf55d79eecfff4b7a4ac5eb3910c90c2817`  
		Last Modified: Tue, 29 Jul 2025 16:32:21 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:7b27e0df383f45d6d523345a078898524a69cee4d6978cf64bf26532b8679dca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 KB (116752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb88e7ee6d3e67b2e4f307c081504a685666917ddf50770fe8beb5abd60a3dc5`

```dockerfile
```

-	Layers:
	-	`sha256:2cf00a09ffccb2c00421311314137de90d0586c126b79dbe5315ce321c168b34`  
		Last Modified: Tue, 29 Jul 2025 18:35:07 GMT  
		Size: 96.2 KB (96180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55325ecc9b276e9c55badf949ed4f06840c34aa8baf0aa6f974e0b90dc5d4e0d`  
		Last Modified: Tue, 29 Jul 2025 18:35:07 GMT  
		Size: 20.6 KB (20572 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.22` - linux; arm variant v6

```console
$ docker pull memcached@sha256:78b59dd3af5a55e950f5106869e642af122a7dc470545f4ba533f6833d83b62c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5550795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb09d5ce1b7010f7a36d77494bc5358d666339628c183692906db6a961373847`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c710b5ddcc2882c5014d0c8cb93aec2bd8b6cc3c59fd42b40c87d94f89a7bc7f`  
		Last Modified: Wed, 23 Jul 2025 22:59:16 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c42040d822a4af7f05f9ccd4d18a7a5e4712b118b7f18d1a7969761029a9d2`  
		Last Modified: Wed, 23 Jul 2025 22:59:16 GMT  
		Size: 101.5 KB (101533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3095e18cd24048696efd57ac64d04dde381a3abde625964e02165c7364eb5633`  
		Last Modified: Tue, 29 Jul 2025 16:50:12 GMT  
		Size: 1.9 MB (1947003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0436ec50f04ed972ff0dd760f7e820f192236e5e720bddb6173f65159c7c36`  
		Last Modified: Tue, 29 Jul 2025 16:50:11 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671c24aae36bb04a32e05bd64e1371384f594889cdbbc41029c916447666d402`  
		Last Modified: Tue, 29 Jul 2025 16:50:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:c2a050c6822d834285577c3a001fdfcf9949b7f5a483a4a76a49b549bea19641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54e8bda3e734528caeab4505f084ca7a3076d5ec2273287f66954b5e91af42f`

```dockerfile
```

-	Layers:
	-	`sha256:0d86924831d61ce8b792b25421e9ff0fa2eda9ab940eba5309d44d0eeada7e8e`  
		Last Modified: Tue, 29 Jul 2025 18:35:11 GMT  
		Size: 20.5 KB (20506 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.22` - linux; arm variant v7

```console
$ docker pull memcached@sha256:c9f5db2389b9b0b4a2cd199c4417a9f49a60c42d616e8421177e662d4830de07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5217393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9421ed030d4b6b6405714612b8858bda87bc53ac8b0c5ed65c582119527f2d9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251060498ca8f0484e20714689b9caba533d09c1b74ed8f2a06780db515a28e2`  
		Last Modified: Thu, 24 Jul 2025 00:27:37 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2293bd2fb47d57e5869c197133067e17f9b1e51ea0f298af1e480e7fd33d681`  
		Last Modified: Thu, 24 Jul 2025 00:27:38 GMT  
		Size: 91.3 KB (91313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ae82f2bac2f7e6fe57f8cb7006fc227c972da1ae5749eba9f5f73e6f3248ec`  
		Last Modified: Tue, 29 Jul 2025 17:11:51 GMT  
		Size: 1.9 MB (1905692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e60bf2b2164c620b69e40bdcb64d4104d02eab86c96ea6e170a3601b9ecfd82`  
		Last Modified: Tue, 29 Jul 2025 17:11:51 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:665fe4cd856f1a5c2193568e756c572656949b17c381fc8d43efaa823e18cfa7`  
		Last Modified: Tue, 29 Jul 2025 17:11:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:376a71bc0fef7741e92fdae8b96c825c4622e980de01e724b1a3a0bec3d95f20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 KB (116963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22b574f6c6d021a917c0e99ff4800d8ac3c22fb94b94f88c404cc7609f562fb5`

```dockerfile
```

-	Layers:
	-	`sha256:58ebd4bc7ee5888c552e0fa618f93aefbdb1d15a56ecd3abef19a46ce2f93eee`  
		Last Modified: Tue, 29 Jul 2025 18:35:15 GMT  
		Size: 96.2 KB (96248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d432ed2053ed8249834dd5016fe3199bbc3f82dc7013027c3ead9efe2a007b98`  
		Last Modified: Tue, 29 Jul 2025 18:35:16 GMT  
		Size: 20.7 KB (20715 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:b5e4ecc3e927ee30e5cfcfc8aa044960631c75eb8abed9d0fcee6232aa5fdf79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6241700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40c880dc2c785861dc9010b813bb6f533f30518443a3bb7e7f477bc96af14582`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfbfeb6ac9fd2045c5bea10a301ad554c1f703ffc2885c41520dd5e42eb4a59a`  
		Last Modified: Tue, 29 Jul 2025 16:41:08 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47acaa5035f94aed634b9d7ecae02fb3838f19e38f8e752ecd6cfba97699b31`  
		Last Modified: Tue, 29 Jul 2025 16:41:08 GMT  
		Size: 120.8 KB (120812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8160f3136c6863b52f0dec4f9918b91b8a509700b2071ec0aecd5a6231f00f2a`  
		Last Modified: Tue, 29 Jul 2025 16:41:09 GMT  
		Size: 2.0 MB (1988782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff22f0cad01950efb78a7a862b0becb8b2fd22d795b585f97dad66c091c3dd7`  
		Last Modified: Tue, 29 Jul 2025 16:41:08 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed19cbfb574c7d8cab364e2ec072c0e03f694468ada41cd70bfcd35392df9e7`  
		Last Modified: Tue, 29 Jul 2025 16:41:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:b4c81c7ababb91ecdda3b7d70514d16818602199d759eb2aadd74de732d52960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.1 KB (117055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80452fd4f79f6e7a0dab0beebf5c144f9df7c257255cdd3cb93ccbff77001fd6`

```dockerfile
```

-	Layers:
	-	`sha256:f11d2a322f6088804ee63ae1a77b9d5ddcdfdc0c65c22e7a70b7ee67cf4532ed`  
		Last Modified: Tue, 29 Jul 2025 18:35:20 GMT  
		Size: 96.3 KB (96284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e225dd6ea14146ddf445598f24189c065ec684fbeb92e7d053a0211a7d60efda`  
		Last Modified: Tue, 29 Jul 2025 18:35:21 GMT  
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
$ docker pull memcached@sha256:04386ede5dcbf35cabad144bcdc951cc64882f7b9727f2d09927fe0d5551dd19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5942089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8252590eee78d67456ac83fd8279259aaea4d2a555c8bc20b173663fcaa2883`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc22e0cec7e7fe8cff10539bca58363ad6749e2de4f878015c25b5f2b6ecadb9`  
		Last Modified: Tue, 29 Jul 2025 16:33:46 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992ebe18219bd78e59e7e56661aae22f700927f47bc7ad1dfe7717093b371c15`  
		Last Modified: Tue, 29 Jul 2025 16:33:49 GMT  
		Size: 124.3 KB (124315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953f5a37d23881d59809ea64dc6ebf1a152a1ff8929f51befb10577771755f5d`  
		Last Modified: Tue, 29 Jul 2025 16:33:49 GMT  
		Size: 2.1 MB (2089310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10b62870a2d7b266495d83cfd72dcf702c91c5c60a7e29836bd9bdac776511a7`  
		Last Modified: Tue, 29 Jul 2025 16:33:47 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1cc8c0fe9a4ef7e2ef70e32ddbfbd2fd68985dd452630a8f390c5b41c654f8`  
		Last Modified: Tue, 29 Jul 2025 16:33:47 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:cf7e9735e4ef5d00dc25928653b808214f070708e9d879ef54afc4d77ce9db2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcceb455cfdb86bdb0c165af3bc54cbab794d56fef1dbae2b484d28027db791c`

```dockerfile
```

-	Layers:
	-	`sha256:a40704a0afb5cf1b90c0fbdf73c5218a4d8f0e93bb39014507b5fa5f8c7265dd`  
		Last Modified: Tue, 29 Jul 2025 18:35:29 GMT  
		Size: 94.3 KB (94287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da22397f364310e72420738395739c36e25b4e4813bbc5da197582a91bb55ac9`  
		Last Modified: Tue, 29 Jul 2025 18:35:29 GMT  
		Size: 20.6 KB (20648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.22` - linux; riscv64

```console
$ docker pull memcached@sha256:d55b98c34ba1c2f546461bd57477d46ab868f9de6b107ffb8f20e06dab1e10d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5555034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1034dde2661f43165e85db9a13ff0e10d237d14d4b1b7ee1d4570f19d7df4e69`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00bbdcecb4dec3cbaba0500f9425897948884cfd8db95ccdf9b824d448b24049`  
		Last Modified: Wed, 23 Jul 2025 23:54:15 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c18051d55886d147cafcee8f9e220087c0b60c0e11ec8898a4005352ee0f7e4`  
		Last Modified: Wed, 23 Jul 2025 23:50:14 GMT  
		Size: 107.9 KB (107902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953c2b44fe537b63907764cf78cbb294c6a1133eacb39c62d35ee5d4914779cb`  
		Last Modified: Tue, 29 Jul 2025 16:42:10 GMT  
		Size: 1.9 MB (1932977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d69b2f63abf91684a15b9de7b5e617996762376da3fdda50c4e20c2f1e0f4da`  
		Last Modified: Tue, 29 Jul 2025 16:42:10 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f57c134601fc15e8f2cf183cfd9a3057731ad48b915988217f51df31b5d3cf38`  
		Last Modified: Tue, 29 Jul 2025 16:42:10 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:d50b42de80ef3381b05da20cef4ba6ab4491facb607528e075c034257fe9d327
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27766c161110b7e46063a39ce6e176f87233fd6722a825ec338e1568892a77a3`

```dockerfile
```

-	Layers:
	-	`sha256:f933f968a4a14795196607a1337a19431e9f61db78bb49c5c2f89f64a17a1d89`  
		Last Modified: Tue, 29 Jul 2025 18:35:33 GMT  
		Size: 94.3 KB (94283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffc41094fe9f57bca69da70bbb18eca52aaf6d27d0fb6d79eda79f9e011a157a`  
		Last Modified: Tue, 29 Jul 2025 18:35:33 GMT  
		Size: 20.6 KB (20647 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.22` - linux; s390x

```console
$ docker pull memcached@sha256:cfd223eb11df3d2297224d458caf974f3f0aae4742ff917812f1b8c84c84e705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5797268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78e23f18e891a12e72ef84139504baf8783a7db21d4976fc0b607f8e9bbf736f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f00131fb0ca26b15f1ac64b82554fc342b19f8c1ef38312a75addb6686f7bc24`  
		Last Modified: Tue, 29 Jul 2025 16:41:40 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e54da6ab620e035fd78987688d45401e87278ec8a5c02cef8a57e4ea9fd286`  
		Last Modified: Tue, 29 Jul 2025 16:41:42 GMT  
		Size: 113.5 KB (113499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6160f9fac1fd86eda224e9ce4740ea46f7e23dc7edb6d1fe9d830001313e63a`  
		Last Modified: Tue, 29 Jul 2025 16:41:46 GMT  
		Size: 2.0 MB (2037446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d01cd71d33b01b420652f4ad9275f1475f4f0bf253dc0a1b48198df2010be5`  
		Last Modified: Tue, 29 Jul 2025 16:41:52 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:831dd5e3c39dd2744dc8823190095f709c36020b55ccdaf85f62a146582c7d9d`  
		Last Modified: Tue, 29 Jul 2025 16:41:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:79f0de7e4dcc9afdbfa1fa22250cf3e544d6f3c33174246b427d2865c7e343d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71dad4d71741d8d354038cb6898389aebb54c956dfcd865d57f78dcc3b238bf8`

```dockerfile
```

-	Layers:
	-	`sha256:f942bbb9520308ae352a056c148fdce8f6b09672c257e0a769aa2504bacf1845`  
		Last Modified: Tue, 29 Jul 2025 18:35:37 GMT  
		Size: 94.2 KB (94229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c46680ef7cf08a43965ab9c7727cc70268ee89e366a1ce1806d0f7980b4ad812`  
		Last Modified: Tue, 29 Jul 2025 18:35:38 GMT  
		Size: 20.6 KB (20574 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-trixie`

```console
$ docker pull memcached@sha256:157c563eef6954ac0bc583c36def96d8ed2d3b3c5b37214f27d210ac53942386
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
$ docker pull memcached@sha256:742d5665f0f292e1278bafd0dff520b5f4edb101c587c29fb0ef273f9d7e124f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30319041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc1024c223c5953b97de26e48cce8df89bee4493e37781f6826e6df56c590056`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1759104000'
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
	-	`sha256:d2a243ecf382412941b4d6772dba911a8093cf3703c933872fbb7ecc21e27e20`  
		Last Modified: Mon, 29 Sep 2025 23:34:24 GMT  
		Size: 27.9 MB (27946145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d24bdf1148108d2d3fc42a07dae247e5242de03db9a71e04066262a853f139d`  
		Last Modified: Mon, 29 Sep 2025 23:59:31 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e717ac34c0d292ae77e9118ac1581d40d881e518d32d9e64f01fddf818164b`  
		Last Modified: Mon, 29 Sep 2025 23:59:31 GMT  
		Size: 144.0 KB (144036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a3b7d16c874ce52964b6ba216127f7fcf604d326cc965210eb58119d605d28`  
		Last Modified: Mon, 29 Sep 2025 23:59:31 GMT  
		Size: 2.2 MB (2227345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb7f38fc7bbd06b5c988a48649d103d93ab0d8011b6a4f5bd8ad38bbd4cac432`  
		Last Modified: Mon, 29 Sep 2025 23:59:31 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5307470e3430d06e3f04b798774d1905a98a13f5ba3387596a0aa97e34b7eba`  
		Last Modified: Mon, 29 Sep 2025 23:59:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:92764b7963e735b77f5e5b433bf1311bc919679a81273cf442178538cf7da2ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:512f0e0d6001116f7984270337608de656664abeb7602b6fc4add42303ba8ee6`

```dockerfile
```

-	Layers:
	-	`sha256:a8fc1cbacd56787b740b886369c6eaafa6151c97fade289ea774600c03a80e11`  
		Last Modified: Tue, 30 Sep 2025 00:34:39 GMT  
		Size: 2.0 MB (2011183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57884b3635fcf7e290933e3a1da7210a05c98ab3187a6e484a5cc8cedf845e98`  
		Last Modified: Tue, 30 Sep 2025 00:34:39 GMT  
		Size: 22.3 KB (22347 bytes)  
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
$ docker pull memcached@sha256:5a071a15dfae20029d56a8845f8053a4f4447934a87e0db0678b6f4ddc2e924a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36187246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6957fdbfa2f978334c6c02013b0e9b928534ddf41009ccae3597ccaf389fd455`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
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
	-	`sha256:8bcecd3ced4047f6a4d35464fc2ee9b45e7fcc10b49690427794f4421b0552ab`  
		Last Modified: Mon, 29 Sep 2025 23:41:19 GMT  
		Size: 33.6 MB (33598454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cee3e1fdea897c6a6b3a982e1918145b5bcd716e5ae6ed66b5e7184e651e059`  
		Last Modified: Tue, 30 Sep 2025 07:50:11 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dea6ee42e2fcf50b7f0d213d52ea27f8eebdaf12c0aa80c5df4828c4566af25`  
		Last Modified: Tue, 30 Sep 2025 07:50:12 GMT  
		Size: 170.3 KB (170259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629d93745cabb21520c860c7612f141299a2c0f2632cf40b7dcc88799307dcd7`  
		Last Modified: Tue, 30 Sep 2025 07:50:13 GMT  
		Size: 2.4 MB (2417019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afbd1630af2c91474bfc04cf614cc4d0a7093510b706f978f20f426127e93305`  
		Last Modified: Tue, 30 Sep 2025 07:50:12 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8293ad839e50f443a419fb4c0f6a6dbde6204ad3bf467cdff6e99385a7d1c3`  
		Last Modified: Tue, 30 Sep 2025 07:50:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:987b950cf472a2d95cc860d4c3c9e95c51ab792c33f5ac61607b7e4f38d1d8d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:973c6753846fed972084489bd202cf7da6e77ddc33d584a90658a8949b5730ee`

```dockerfile
```

-	Layers:
	-	`sha256:821a5821beef4d6bdae90ea0d98277dd982af05804dd43f706310bc7263244c4`  
		Last Modified: Wed, 01 Oct 2025 21:34:36 GMT  
		Size: 2.0 MB (2011781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:222d48bb5ef6a86d72ecccaf90a1cd7cf49c644139aee33815b1e7d0fd87cfcb`  
		Last Modified: Wed, 01 Oct 2025 21:34:36 GMT  
		Size: 22.3 KB (22270 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; riscv64

```console
$ docker pull memcached@sha256:31bb76b9b98cd96febc6b1d5056f839ffab9aaaa12690d0a47353df1b2b49221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30629784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e010912f76722a300766eb6afe7e6b13e8f72682c8dec557d00826b2a7cba503`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1759104000'
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
	-	`sha256:ecc6f9aec21fb94a493c2875c244e720a2f7c6c034063ce87b2f5b6b46962ec9`  
		Last Modified: Tue, 30 Sep 2025 01:05:14 GMT  
		Size: 28.3 MB (28275502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c2f28b5ea15f2b021d2f93df684963b9d27de2301bfccbf53d01abc5bdaa97`  
		Last Modified: Tue, 30 Sep 2025 04:00:18 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179b31cc3aad1ab89917cf87cb268b6e8e4291ec4b8996317231c4ac0003ebf9`  
		Last Modified: Tue, 30 Sep 2025 04:00:18 GMT  
		Size: 133.0 KB (132970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca5db35fb11036dcb8f2d55bbe271869356c9b4b2e08c0d0293a9b0c894f5dff`  
		Last Modified: Tue, 30 Sep 2025 04:00:19 GMT  
		Size: 2.2 MB (2219797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc4c908359c51ce26778438a3886b2eb2d6987ee3a22862dbdbe2056a3cd95d`  
		Last Modified: Tue, 30 Sep 2025 04:00:19 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7254f9df049c190c1c3ffa9794b395fb4e3ec7ab18b8dce7a58733c63a54dd`  
		Last Modified: Tue, 30 Sep 2025 04:00:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:10dcedf955ee46896155ca87f9a292967d1ce021fbab41f3a0fc44045a885e25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85a06d87da790b7800c970ca38989414eeae6c950cf890286591dc59c6163cc5`

```dockerfile
```

-	Layers:
	-	`sha256:b8fb80942d713e49171d0a98b2306b7bbb0023e57f180295e56893f7ea7f458d`  
		Last Modified: Tue, 30 Sep 2025 06:34:34 GMT  
		Size: 2.0 MB (2002144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cbc67dcbbe8db9619b2b3e3b962ebb7d9640901e2048fa63620351cc03d940d`  
		Last Modified: Tue, 30 Sep 2025 06:34:34 GMT  
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
$ docker pull memcached@sha256:157c563eef6954ac0bc583c36def96d8ed2d3b3c5b37214f27d210ac53942386
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
$ docker pull memcached@sha256:742d5665f0f292e1278bafd0dff520b5f4edb101c587c29fb0ef273f9d7e124f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30319041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc1024c223c5953b97de26e48cce8df89bee4493e37781f6826e6df56c590056`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1759104000'
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
	-	`sha256:d2a243ecf382412941b4d6772dba911a8093cf3703c933872fbb7ecc21e27e20`  
		Last Modified: Mon, 29 Sep 2025 23:34:24 GMT  
		Size: 27.9 MB (27946145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d24bdf1148108d2d3fc42a07dae247e5242de03db9a71e04066262a853f139d`  
		Last Modified: Mon, 29 Sep 2025 23:59:31 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e717ac34c0d292ae77e9118ac1581d40d881e518d32d9e64f01fddf818164b`  
		Last Modified: Mon, 29 Sep 2025 23:59:31 GMT  
		Size: 144.0 KB (144036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a3b7d16c874ce52964b6ba216127f7fcf604d326cc965210eb58119d605d28`  
		Last Modified: Mon, 29 Sep 2025 23:59:31 GMT  
		Size: 2.2 MB (2227345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb7f38fc7bbd06b5c988a48649d103d93ab0d8011b6a4f5bd8ad38bbd4cac432`  
		Last Modified: Mon, 29 Sep 2025 23:59:31 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5307470e3430d06e3f04b798774d1905a98a13f5ba3387596a0aa97e34b7eba`  
		Last Modified: Mon, 29 Sep 2025 23:59:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39` - unknown; unknown

```console
$ docker pull memcached@sha256:92764b7963e735b77f5e5b433bf1311bc919679a81273cf442178538cf7da2ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:512f0e0d6001116f7984270337608de656664abeb7602b6fc4add42303ba8ee6`

```dockerfile
```

-	Layers:
	-	`sha256:a8fc1cbacd56787b740b886369c6eaafa6151c97fade289ea774600c03a80e11`  
		Last Modified: Tue, 30 Sep 2025 00:34:39 GMT  
		Size: 2.0 MB (2011183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57884b3635fcf7e290933e3a1da7210a05c98ab3187a6e484a5cc8cedf845e98`  
		Last Modified: Tue, 30 Sep 2025 00:34:39 GMT  
		Size: 22.3 KB (22347 bytes)  
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
$ docker pull memcached@sha256:5a071a15dfae20029d56a8845f8053a4f4447934a87e0db0678b6f4ddc2e924a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36187246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6957fdbfa2f978334c6c02013b0e9b928534ddf41009ccae3597ccaf389fd455`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
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
	-	`sha256:8bcecd3ced4047f6a4d35464fc2ee9b45e7fcc10b49690427794f4421b0552ab`  
		Last Modified: Mon, 29 Sep 2025 23:41:19 GMT  
		Size: 33.6 MB (33598454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cee3e1fdea897c6a6b3a982e1918145b5bcd716e5ae6ed66b5e7184e651e059`  
		Last Modified: Tue, 30 Sep 2025 07:50:11 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dea6ee42e2fcf50b7f0d213d52ea27f8eebdaf12c0aa80c5df4828c4566af25`  
		Last Modified: Tue, 30 Sep 2025 07:50:12 GMT  
		Size: 170.3 KB (170259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629d93745cabb21520c860c7612f141299a2c0f2632cf40b7dcc88799307dcd7`  
		Last Modified: Tue, 30 Sep 2025 07:50:13 GMT  
		Size: 2.4 MB (2417019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afbd1630af2c91474bfc04cf614cc4d0a7093510b706f978f20f426127e93305`  
		Last Modified: Tue, 30 Sep 2025 07:50:12 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8293ad839e50f443a419fb4c0f6a6dbde6204ad3bf467cdff6e99385a7d1c3`  
		Last Modified: Tue, 30 Sep 2025 07:50:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39` - unknown; unknown

```console
$ docker pull memcached@sha256:987b950cf472a2d95cc860d4c3c9e95c51ab792c33f5ac61607b7e4f38d1d8d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:973c6753846fed972084489bd202cf7da6e77ddc33d584a90658a8949b5730ee`

```dockerfile
```

-	Layers:
	-	`sha256:821a5821beef4d6bdae90ea0d98277dd982af05804dd43f706310bc7263244c4`  
		Last Modified: Wed, 01 Oct 2025 21:34:36 GMT  
		Size: 2.0 MB (2011781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:222d48bb5ef6a86d72ecccaf90a1cd7cf49c644139aee33815b1e7d0fd87cfcb`  
		Last Modified: Wed, 01 Oct 2025 21:34:36 GMT  
		Size: 22.3 KB (22270 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39` - linux; riscv64

```console
$ docker pull memcached@sha256:31bb76b9b98cd96febc6b1d5056f839ffab9aaaa12690d0a47353df1b2b49221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30629784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e010912f76722a300766eb6afe7e6b13e8f72682c8dec557d00826b2a7cba503`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1759104000'
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
	-	`sha256:ecc6f9aec21fb94a493c2875c244e720a2f7c6c034063ce87b2f5b6b46962ec9`  
		Last Modified: Tue, 30 Sep 2025 01:05:14 GMT  
		Size: 28.3 MB (28275502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c2f28b5ea15f2b021d2f93df684963b9d27de2301bfccbf53d01abc5bdaa97`  
		Last Modified: Tue, 30 Sep 2025 04:00:18 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179b31cc3aad1ab89917cf87cb268b6e8e4291ec4b8996317231c4ac0003ebf9`  
		Last Modified: Tue, 30 Sep 2025 04:00:18 GMT  
		Size: 133.0 KB (132970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca5db35fb11036dcb8f2d55bbe271869356c9b4b2e08c0d0293a9b0c894f5dff`  
		Last Modified: Tue, 30 Sep 2025 04:00:19 GMT  
		Size: 2.2 MB (2219797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc4c908359c51ce26778438a3886b2eb2d6987ee3a22862dbdbe2056a3cd95d`  
		Last Modified: Tue, 30 Sep 2025 04:00:19 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7254f9df049c190c1c3ffa9794b395fb4e3ec7ab18b8dce7a58733c63a54dd`  
		Last Modified: Tue, 30 Sep 2025 04:00:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39` - unknown; unknown

```console
$ docker pull memcached@sha256:10dcedf955ee46896155ca87f9a292967d1ce021fbab41f3a0fc44045a885e25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85a06d87da790b7800c970ca38989414eeae6c950cf890286591dc59c6163cc5`

```dockerfile
```

-	Layers:
	-	`sha256:b8fb80942d713e49171d0a98b2306b7bbb0023e57f180295e56893f7ea7f458d`  
		Last Modified: Tue, 30 Sep 2025 06:34:34 GMT  
		Size: 2.0 MB (2002144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cbc67dcbbe8db9619b2b3e3b962ebb7d9640901e2048fa63620351cc03d940d`  
		Last Modified: Tue, 30 Sep 2025 06:34:34 GMT  
		Size: 22.3 KB (22270 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39` - linux; s390x

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

### `memcached:1.6.39` - unknown; unknown

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

## `memcached:1.6.39-alpine`

```console
$ docker pull memcached@sha256:eca5d776fe62e6ffe5e27e1a4d357e0bbd9ac609a271243c210599a898122ad2
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
$ docker pull memcached@sha256:033134f4dd9f45d4e22b6e98b040ea3fccf0dca740af3c949b44bebf458b04d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5904246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca259aa2216a248c482fc8a069d48b1e70b087529d2c3de97154bfa458dbb7a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23fb46bc7dee2beda6f5f6f567aecd4d7d7698b9749ed917988a859b7dd96e30`  
		Last Modified: Tue, 29 Jul 2025 16:32:22 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48faf8c85515fb9d17e0752e77d8241f223d53b1adc90439c606d17daabd0ae`  
		Last Modified: Tue, 29 Jul 2025 16:32:24 GMT  
		Size: 104.7 KB (104725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d552a2d777fd444b41cb79438f9f1b441821162e78d73e96dc848a773cf43892`  
		Last Modified: Tue, 29 Jul 2025 16:32:24 GMT  
		Size: 2.0 MB (1998477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c70665f30f3e15975d429b494cb17b21c5d4630c1800cb0addc3fce3a11aa29`  
		Last Modified: Tue, 29 Jul 2025 16:32:20 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ff68520caaf588cec750ad7c403cf55d79eecfff4b7a4ac5eb3910c90c2817`  
		Last Modified: Tue, 29 Jul 2025 16:32:21 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7b27e0df383f45d6d523345a078898524a69cee4d6978cf64bf26532b8679dca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 KB (116752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb88e7ee6d3e67b2e4f307c081504a685666917ddf50770fe8beb5abd60a3dc5`

```dockerfile
```

-	Layers:
	-	`sha256:2cf00a09ffccb2c00421311314137de90d0586c126b79dbe5315ce321c168b34`  
		Last Modified: Tue, 29 Jul 2025 18:35:07 GMT  
		Size: 96.2 KB (96180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55325ecc9b276e9c55badf949ed4f06840c34aa8baf0aa6f974e0b90dc5d4e0d`  
		Last Modified: Tue, 29 Jul 2025 18:35:07 GMT  
		Size: 20.6 KB (20572 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:78b59dd3af5a55e950f5106869e642af122a7dc470545f4ba533f6833d83b62c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5550795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb09d5ce1b7010f7a36d77494bc5358d666339628c183692906db6a961373847`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c710b5ddcc2882c5014d0c8cb93aec2bd8b6cc3c59fd42b40c87d94f89a7bc7f`  
		Last Modified: Wed, 23 Jul 2025 22:59:16 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c42040d822a4af7f05f9ccd4d18a7a5e4712b118b7f18d1a7969761029a9d2`  
		Last Modified: Wed, 23 Jul 2025 22:59:16 GMT  
		Size: 101.5 KB (101533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3095e18cd24048696efd57ac64d04dde381a3abde625964e02165c7364eb5633`  
		Last Modified: Tue, 29 Jul 2025 16:50:12 GMT  
		Size: 1.9 MB (1947003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0436ec50f04ed972ff0dd760f7e820f192236e5e720bddb6173f65159c7c36`  
		Last Modified: Tue, 29 Jul 2025 16:50:11 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671c24aae36bb04a32e05bd64e1371384f594889cdbbc41029c916447666d402`  
		Last Modified: Tue, 29 Jul 2025 16:50:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:c2a050c6822d834285577c3a001fdfcf9949b7f5a483a4a76a49b549bea19641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54e8bda3e734528caeab4505f084ca7a3076d5ec2273287f66954b5e91af42f`

```dockerfile
```

-	Layers:
	-	`sha256:0d86924831d61ce8b792b25421e9ff0fa2eda9ab940eba5309d44d0eeada7e8e`  
		Last Modified: Tue, 29 Jul 2025 18:35:11 GMT  
		Size: 20.5 KB (20506 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:c9f5db2389b9b0b4a2cd199c4417a9f49a60c42d616e8421177e662d4830de07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5217393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9421ed030d4b6b6405714612b8858bda87bc53ac8b0c5ed65c582119527f2d9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251060498ca8f0484e20714689b9caba533d09c1b74ed8f2a06780db515a28e2`  
		Last Modified: Thu, 24 Jul 2025 00:27:37 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2293bd2fb47d57e5869c197133067e17f9b1e51ea0f298af1e480e7fd33d681`  
		Last Modified: Thu, 24 Jul 2025 00:27:38 GMT  
		Size: 91.3 KB (91313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ae82f2bac2f7e6fe57f8cb7006fc227c972da1ae5749eba9f5f73e6f3248ec`  
		Last Modified: Tue, 29 Jul 2025 17:11:51 GMT  
		Size: 1.9 MB (1905692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e60bf2b2164c620b69e40bdcb64d4104d02eab86c96ea6e170a3601b9ecfd82`  
		Last Modified: Tue, 29 Jul 2025 17:11:51 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:665fe4cd856f1a5c2193568e756c572656949b17c381fc8d43efaa823e18cfa7`  
		Last Modified: Tue, 29 Jul 2025 17:11:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:376a71bc0fef7741e92fdae8b96c825c4622e980de01e724b1a3a0bec3d95f20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 KB (116963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22b574f6c6d021a917c0e99ff4800d8ac3c22fb94b94f88c404cc7609f562fb5`

```dockerfile
```

-	Layers:
	-	`sha256:58ebd4bc7ee5888c552e0fa618f93aefbdb1d15a56ecd3abef19a46ce2f93eee`  
		Last Modified: Tue, 29 Jul 2025 18:35:15 GMT  
		Size: 96.2 KB (96248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d432ed2053ed8249834dd5016fe3199bbc3f82dc7013027c3ead9efe2a007b98`  
		Last Modified: Tue, 29 Jul 2025 18:35:16 GMT  
		Size: 20.7 KB (20715 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:b5e4ecc3e927ee30e5cfcfc8aa044960631c75eb8abed9d0fcee6232aa5fdf79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6241700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40c880dc2c785861dc9010b813bb6f533f30518443a3bb7e7f477bc96af14582`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfbfeb6ac9fd2045c5bea10a301ad554c1f703ffc2885c41520dd5e42eb4a59a`  
		Last Modified: Tue, 29 Jul 2025 16:41:08 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47acaa5035f94aed634b9d7ecae02fb3838f19e38f8e752ecd6cfba97699b31`  
		Last Modified: Tue, 29 Jul 2025 16:41:08 GMT  
		Size: 120.8 KB (120812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8160f3136c6863b52f0dec4f9918b91b8a509700b2071ec0aecd5a6231f00f2a`  
		Last Modified: Tue, 29 Jul 2025 16:41:09 GMT  
		Size: 2.0 MB (1988782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff22f0cad01950efb78a7a862b0becb8b2fd22d795b585f97dad66c091c3dd7`  
		Last Modified: Tue, 29 Jul 2025 16:41:08 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed19cbfb574c7d8cab364e2ec072c0e03f694468ada41cd70bfcd35392df9e7`  
		Last Modified: Tue, 29 Jul 2025 16:41:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:b4c81c7ababb91ecdda3b7d70514d16818602199d759eb2aadd74de732d52960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.1 KB (117055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80452fd4f79f6e7a0dab0beebf5c144f9df7c257255cdd3cb93ccbff77001fd6`

```dockerfile
```

-	Layers:
	-	`sha256:f11d2a322f6088804ee63ae1a77b9d5ddcdfdc0c65c22e7a70b7ee67cf4532ed`  
		Last Modified: Tue, 29 Jul 2025 18:35:20 GMT  
		Size: 96.3 KB (96284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e225dd6ea14146ddf445598f24189c065ec684fbeb92e7d053a0211a7d60efda`  
		Last Modified: Tue, 29 Jul 2025 18:35:21 GMT  
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
$ docker pull memcached@sha256:04386ede5dcbf35cabad144bcdc951cc64882f7b9727f2d09927fe0d5551dd19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5942089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8252590eee78d67456ac83fd8279259aaea4d2a555c8bc20b173663fcaa2883`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc22e0cec7e7fe8cff10539bca58363ad6749e2de4f878015c25b5f2b6ecadb9`  
		Last Modified: Tue, 29 Jul 2025 16:33:46 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992ebe18219bd78e59e7e56661aae22f700927f47bc7ad1dfe7717093b371c15`  
		Last Modified: Tue, 29 Jul 2025 16:33:49 GMT  
		Size: 124.3 KB (124315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953f5a37d23881d59809ea64dc6ebf1a152a1ff8929f51befb10577771755f5d`  
		Last Modified: Tue, 29 Jul 2025 16:33:49 GMT  
		Size: 2.1 MB (2089310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10b62870a2d7b266495d83cfd72dcf702c91c5c60a7e29836bd9bdac776511a7`  
		Last Modified: Tue, 29 Jul 2025 16:33:47 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1cc8c0fe9a4ef7e2ef70e32ddbfbd2fd68985dd452630a8f390c5b41c654f8`  
		Last Modified: Tue, 29 Jul 2025 16:33:47 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:cf7e9735e4ef5d00dc25928653b808214f070708e9d879ef54afc4d77ce9db2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcceb455cfdb86bdb0c165af3bc54cbab794d56fef1dbae2b484d28027db791c`

```dockerfile
```

-	Layers:
	-	`sha256:a40704a0afb5cf1b90c0fbdf73c5218a4d8f0e93bb39014507b5fa5f8c7265dd`  
		Last Modified: Tue, 29 Jul 2025 18:35:29 GMT  
		Size: 94.3 KB (94287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da22397f364310e72420738395739c36e25b4e4813bbc5da197582a91bb55ac9`  
		Last Modified: Tue, 29 Jul 2025 18:35:29 GMT  
		Size: 20.6 KB (20648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:d55b98c34ba1c2f546461bd57477d46ab868f9de6b107ffb8f20e06dab1e10d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5555034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1034dde2661f43165e85db9a13ff0e10d237d14d4b1b7ee1d4570f19d7df4e69`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00bbdcecb4dec3cbaba0500f9425897948884cfd8db95ccdf9b824d448b24049`  
		Last Modified: Wed, 23 Jul 2025 23:54:15 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c18051d55886d147cafcee8f9e220087c0b60c0e11ec8898a4005352ee0f7e4`  
		Last Modified: Wed, 23 Jul 2025 23:50:14 GMT  
		Size: 107.9 KB (107902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953c2b44fe537b63907764cf78cbb294c6a1133eacb39c62d35ee5d4914779cb`  
		Last Modified: Tue, 29 Jul 2025 16:42:10 GMT  
		Size: 1.9 MB (1932977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d69b2f63abf91684a15b9de7b5e617996762376da3fdda50c4e20c2f1e0f4da`  
		Last Modified: Tue, 29 Jul 2025 16:42:10 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f57c134601fc15e8f2cf183cfd9a3057731ad48b915988217f51df31b5d3cf38`  
		Last Modified: Tue, 29 Jul 2025 16:42:10 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:d50b42de80ef3381b05da20cef4ba6ab4491facb607528e075c034257fe9d327
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27766c161110b7e46063a39ce6e176f87233fd6722a825ec338e1568892a77a3`

```dockerfile
```

-	Layers:
	-	`sha256:f933f968a4a14795196607a1337a19431e9f61db78bb49c5c2f89f64a17a1d89`  
		Last Modified: Tue, 29 Jul 2025 18:35:33 GMT  
		Size: 94.3 KB (94283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffc41094fe9f57bca69da70bbb18eca52aaf6d27d0fb6d79eda79f9e011a157a`  
		Last Modified: Tue, 29 Jul 2025 18:35:33 GMT  
		Size: 20.6 KB (20647 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:cfd223eb11df3d2297224d458caf974f3f0aae4742ff917812f1b8c84c84e705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5797268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78e23f18e891a12e72ef84139504baf8783a7db21d4976fc0b607f8e9bbf736f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f00131fb0ca26b15f1ac64b82554fc342b19f8c1ef38312a75addb6686f7bc24`  
		Last Modified: Tue, 29 Jul 2025 16:41:40 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e54da6ab620e035fd78987688d45401e87278ec8a5c02cef8a57e4ea9fd286`  
		Last Modified: Tue, 29 Jul 2025 16:41:42 GMT  
		Size: 113.5 KB (113499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6160f9fac1fd86eda224e9ce4740ea46f7e23dc7edb6d1fe9d830001313e63a`  
		Last Modified: Tue, 29 Jul 2025 16:41:46 GMT  
		Size: 2.0 MB (2037446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d01cd71d33b01b420652f4ad9275f1475f4f0bf253dc0a1b48198df2010be5`  
		Last Modified: Tue, 29 Jul 2025 16:41:52 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:831dd5e3c39dd2744dc8823190095f709c36020b55ccdaf85f62a146582c7d9d`  
		Last Modified: Tue, 29 Jul 2025 16:41:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:79f0de7e4dcc9afdbfa1fa22250cf3e544d6f3c33174246b427d2865c7e343d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71dad4d71741d8d354038cb6898389aebb54c956dfcd865d57f78dcc3b238bf8`

```dockerfile
```

-	Layers:
	-	`sha256:f942bbb9520308ae352a056c148fdce8f6b09672c257e0a769aa2504bacf1845`  
		Last Modified: Tue, 29 Jul 2025 18:35:37 GMT  
		Size: 94.2 KB (94229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c46680ef7cf08a43965ab9c7727cc70268ee89e366a1ce1806d0f7980b4ad812`  
		Last Modified: Tue, 29 Jul 2025 18:35:38 GMT  
		Size: 20.6 KB (20574 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.39-alpine3.22`

```console
$ docker pull memcached@sha256:eca5d776fe62e6ffe5e27e1a4d357e0bbd9ac609a271243c210599a898122ad2
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
$ docker pull memcached@sha256:033134f4dd9f45d4e22b6e98b040ea3fccf0dca740af3c949b44bebf458b04d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5904246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca259aa2216a248c482fc8a069d48b1e70b087529d2c3de97154bfa458dbb7a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23fb46bc7dee2beda6f5f6f567aecd4d7d7698b9749ed917988a859b7dd96e30`  
		Last Modified: Tue, 29 Jul 2025 16:32:22 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48faf8c85515fb9d17e0752e77d8241f223d53b1adc90439c606d17daabd0ae`  
		Last Modified: Tue, 29 Jul 2025 16:32:24 GMT  
		Size: 104.7 KB (104725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d552a2d777fd444b41cb79438f9f1b441821162e78d73e96dc848a773cf43892`  
		Last Modified: Tue, 29 Jul 2025 16:32:24 GMT  
		Size: 2.0 MB (1998477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c70665f30f3e15975d429b494cb17b21c5d4630c1800cb0addc3fce3a11aa29`  
		Last Modified: Tue, 29 Jul 2025 16:32:20 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ff68520caaf588cec750ad7c403cf55d79eecfff4b7a4ac5eb3910c90c2817`  
		Last Modified: Tue, 29 Jul 2025 16:32:21 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:7b27e0df383f45d6d523345a078898524a69cee4d6978cf64bf26532b8679dca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 KB (116752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb88e7ee6d3e67b2e4f307c081504a685666917ddf50770fe8beb5abd60a3dc5`

```dockerfile
```

-	Layers:
	-	`sha256:2cf00a09ffccb2c00421311314137de90d0586c126b79dbe5315ce321c168b34`  
		Last Modified: Tue, 29 Jul 2025 18:35:07 GMT  
		Size: 96.2 KB (96180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55325ecc9b276e9c55badf949ed4f06840c34aa8baf0aa6f974e0b90dc5d4e0d`  
		Last Modified: Tue, 29 Jul 2025 18:35:07 GMT  
		Size: 20.6 KB (20572 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-alpine3.22` - linux; arm variant v6

```console
$ docker pull memcached@sha256:78b59dd3af5a55e950f5106869e642af122a7dc470545f4ba533f6833d83b62c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5550795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb09d5ce1b7010f7a36d77494bc5358d666339628c183692906db6a961373847`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c710b5ddcc2882c5014d0c8cb93aec2bd8b6cc3c59fd42b40c87d94f89a7bc7f`  
		Last Modified: Wed, 23 Jul 2025 22:59:16 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c42040d822a4af7f05f9ccd4d18a7a5e4712b118b7f18d1a7969761029a9d2`  
		Last Modified: Wed, 23 Jul 2025 22:59:16 GMT  
		Size: 101.5 KB (101533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3095e18cd24048696efd57ac64d04dde381a3abde625964e02165c7364eb5633`  
		Last Modified: Tue, 29 Jul 2025 16:50:12 GMT  
		Size: 1.9 MB (1947003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0436ec50f04ed972ff0dd760f7e820f192236e5e720bddb6173f65159c7c36`  
		Last Modified: Tue, 29 Jul 2025 16:50:11 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671c24aae36bb04a32e05bd64e1371384f594889cdbbc41029c916447666d402`  
		Last Modified: Tue, 29 Jul 2025 16:50:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:c2a050c6822d834285577c3a001fdfcf9949b7f5a483a4a76a49b549bea19641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54e8bda3e734528caeab4505f084ca7a3076d5ec2273287f66954b5e91af42f`

```dockerfile
```

-	Layers:
	-	`sha256:0d86924831d61ce8b792b25421e9ff0fa2eda9ab940eba5309d44d0eeada7e8e`  
		Last Modified: Tue, 29 Jul 2025 18:35:11 GMT  
		Size: 20.5 KB (20506 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-alpine3.22` - linux; arm variant v7

```console
$ docker pull memcached@sha256:c9f5db2389b9b0b4a2cd199c4417a9f49a60c42d616e8421177e662d4830de07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5217393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9421ed030d4b6b6405714612b8858bda87bc53ac8b0c5ed65c582119527f2d9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251060498ca8f0484e20714689b9caba533d09c1b74ed8f2a06780db515a28e2`  
		Last Modified: Thu, 24 Jul 2025 00:27:37 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2293bd2fb47d57e5869c197133067e17f9b1e51ea0f298af1e480e7fd33d681`  
		Last Modified: Thu, 24 Jul 2025 00:27:38 GMT  
		Size: 91.3 KB (91313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ae82f2bac2f7e6fe57f8cb7006fc227c972da1ae5749eba9f5f73e6f3248ec`  
		Last Modified: Tue, 29 Jul 2025 17:11:51 GMT  
		Size: 1.9 MB (1905692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e60bf2b2164c620b69e40bdcb64d4104d02eab86c96ea6e170a3601b9ecfd82`  
		Last Modified: Tue, 29 Jul 2025 17:11:51 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:665fe4cd856f1a5c2193568e756c572656949b17c381fc8d43efaa823e18cfa7`  
		Last Modified: Tue, 29 Jul 2025 17:11:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:376a71bc0fef7741e92fdae8b96c825c4622e980de01e724b1a3a0bec3d95f20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 KB (116963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22b574f6c6d021a917c0e99ff4800d8ac3c22fb94b94f88c404cc7609f562fb5`

```dockerfile
```

-	Layers:
	-	`sha256:58ebd4bc7ee5888c552e0fa618f93aefbdb1d15a56ecd3abef19a46ce2f93eee`  
		Last Modified: Tue, 29 Jul 2025 18:35:15 GMT  
		Size: 96.2 KB (96248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d432ed2053ed8249834dd5016fe3199bbc3f82dc7013027c3ead9efe2a007b98`  
		Last Modified: Tue, 29 Jul 2025 18:35:16 GMT  
		Size: 20.7 KB (20715 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:b5e4ecc3e927ee30e5cfcfc8aa044960631c75eb8abed9d0fcee6232aa5fdf79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6241700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40c880dc2c785861dc9010b813bb6f533f30518443a3bb7e7f477bc96af14582`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfbfeb6ac9fd2045c5bea10a301ad554c1f703ffc2885c41520dd5e42eb4a59a`  
		Last Modified: Tue, 29 Jul 2025 16:41:08 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47acaa5035f94aed634b9d7ecae02fb3838f19e38f8e752ecd6cfba97699b31`  
		Last Modified: Tue, 29 Jul 2025 16:41:08 GMT  
		Size: 120.8 KB (120812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8160f3136c6863b52f0dec4f9918b91b8a509700b2071ec0aecd5a6231f00f2a`  
		Last Modified: Tue, 29 Jul 2025 16:41:09 GMT  
		Size: 2.0 MB (1988782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff22f0cad01950efb78a7a862b0becb8b2fd22d795b585f97dad66c091c3dd7`  
		Last Modified: Tue, 29 Jul 2025 16:41:08 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed19cbfb574c7d8cab364e2ec072c0e03f694468ada41cd70bfcd35392df9e7`  
		Last Modified: Tue, 29 Jul 2025 16:41:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:b4c81c7ababb91ecdda3b7d70514d16818602199d759eb2aadd74de732d52960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.1 KB (117055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80452fd4f79f6e7a0dab0beebf5c144f9df7c257255cdd3cb93ccbff77001fd6`

```dockerfile
```

-	Layers:
	-	`sha256:f11d2a322f6088804ee63ae1a77b9d5ddcdfdc0c65c22e7a70b7ee67cf4532ed`  
		Last Modified: Tue, 29 Jul 2025 18:35:20 GMT  
		Size: 96.3 KB (96284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e225dd6ea14146ddf445598f24189c065ec684fbeb92e7d053a0211a7d60efda`  
		Last Modified: Tue, 29 Jul 2025 18:35:21 GMT  
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
$ docker pull memcached@sha256:04386ede5dcbf35cabad144bcdc951cc64882f7b9727f2d09927fe0d5551dd19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5942089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8252590eee78d67456ac83fd8279259aaea4d2a555c8bc20b173663fcaa2883`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc22e0cec7e7fe8cff10539bca58363ad6749e2de4f878015c25b5f2b6ecadb9`  
		Last Modified: Tue, 29 Jul 2025 16:33:46 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992ebe18219bd78e59e7e56661aae22f700927f47bc7ad1dfe7717093b371c15`  
		Last Modified: Tue, 29 Jul 2025 16:33:49 GMT  
		Size: 124.3 KB (124315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953f5a37d23881d59809ea64dc6ebf1a152a1ff8929f51befb10577771755f5d`  
		Last Modified: Tue, 29 Jul 2025 16:33:49 GMT  
		Size: 2.1 MB (2089310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10b62870a2d7b266495d83cfd72dcf702c91c5c60a7e29836bd9bdac776511a7`  
		Last Modified: Tue, 29 Jul 2025 16:33:47 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1cc8c0fe9a4ef7e2ef70e32ddbfbd2fd68985dd452630a8f390c5b41c654f8`  
		Last Modified: Tue, 29 Jul 2025 16:33:47 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:cf7e9735e4ef5d00dc25928653b808214f070708e9d879ef54afc4d77ce9db2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcceb455cfdb86bdb0c165af3bc54cbab794d56fef1dbae2b484d28027db791c`

```dockerfile
```

-	Layers:
	-	`sha256:a40704a0afb5cf1b90c0fbdf73c5218a4d8f0e93bb39014507b5fa5f8c7265dd`  
		Last Modified: Tue, 29 Jul 2025 18:35:29 GMT  
		Size: 94.3 KB (94287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da22397f364310e72420738395739c36e25b4e4813bbc5da197582a91bb55ac9`  
		Last Modified: Tue, 29 Jul 2025 18:35:29 GMT  
		Size: 20.6 KB (20648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-alpine3.22` - linux; riscv64

```console
$ docker pull memcached@sha256:d55b98c34ba1c2f546461bd57477d46ab868f9de6b107ffb8f20e06dab1e10d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5555034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1034dde2661f43165e85db9a13ff0e10d237d14d4b1b7ee1d4570f19d7df4e69`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00bbdcecb4dec3cbaba0500f9425897948884cfd8db95ccdf9b824d448b24049`  
		Last Modified: Wed, 23 Jul 2025 23:54:15 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c18051d55886d147cafcee8f9e220087c0b60c0e11ec8898a4005352ee0f7e4`  
		Last Modified: Wed, 23 Jul 2025 23:50:14 GMT  
		Size: 107.9 KB (107902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953c2b44fe537b63907764cf78cbb294c6a1133eacb39c62d35ee5d4914779cb`  
		Last Modified: Tue, 29 Jul 2025 16:42:10 GMT  
		Size: 1.9 MB (1932977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d69b2f63abf91684a15b9de7b5e617996762376da3fdda50c4e20c2f1e0f4da`  
		Last Modified: Tue, 29 Jul 2025 16:42:10 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f57c134601fc15e8f2cf183cfd9a3057731ad48b915988217f51df31b5d3cf38`  
		Last Modified: Tue, 29 Jul 2025 16:42:10 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:d50b42de80ef3381b05da20cef4ba6ab4491facb607528e075c034257fe9d327
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27766c161110b7e46063a39ce6e176f87233fd6722a825ec338e1568892a77a3`

```dockerfile
```

-	Layers:
	-	`sha256:f933f968a4a14795196607a1337a19431e9f61db78bb49c5c2f89f64a17a1d89`  
		Last Modified: Tue, 29 Jul 2025 18:35:33 GMT  
		Size: 94.3 KB (94283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffc41094fe9f57bca69da70bbb18eca52aaf6d27d0fb6d79eda79f9e011a157a`  
		Last Modified: Tue, 29 Jul 2025 18:35:33 GMT  
		Size: 20.6 KB (20647 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-alpine3.22` - linux; s390x

```console
$ docker pull memcached@sha256:cfd223eb11df3d2297224d458caf974f3f0aae4742ff917812f1b8c84c84e705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5797268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78e23f18e891a12e72ef84139504baf8783a7db21d4976fc0b607f8e9bbf736f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f00131fb0ca26b15f1ac64b82554fc342b19f8c1ef38312a75addb6686f7bc24`  
		Last Modified: Tue, 29 Jul 2025 16:41:40 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e54da6ab620e035fd78987688d45401e87278ec8a5c02cef8a57e4ea9fd286`  
		Last Modified: Tue, 29 Jul 2025 16:41:42 GMT  
		Size: 113.5 KB (113499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6160f9fac1fd86eda224e9ce4740ea46f7e23dc7edb6d1fe9d830001313e63a`  
		Last Modified: Tue, 29 Jul 2025 16:41:46 GMT  
		Size: 2.0 MB (2037446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d01cd71d33b01b420652f4ad9275f1475f4f0bf253dc0a1b48198df2010be5`  
		Last Modified: Tue, 29 Jul 2025 16:41:52 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:831dd5e3c39dd2744dc8823190095f709c36020b55ccdaf85f62a146582c7d9d`  
		Last Modified: Tue, 29 Jul 2025 16:41:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:79f0de7e4dcc9afdbfa1fa22250cf3e544d6f3c33174246b427d2865c7e343d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71dad4d71741d8d354038cb6898389aebb54c956dfcd865d57f78dcc3b238bf8`

```dockerfile
```

-	Layers:
	-	`sha256:f942bbb9520308ae352a056c148fdce8f6b09672c257e0a769aa2504bacf1845`  
		Last Modified: Tue, 29 Jul 2025 18:35:37 GMT  
		Size: 94.2 KB (94229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c46680ef7cf08a43965ab9c7727cc70268ee89e366a1ce1806d0f7980b4ad812`  
		Last Modified: Tue, 29 Jul 2025 18:35:38 GMT  
		Size: 20.6 KB (20574 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.39-trixie`

```console
$ docker pull memcached@sha256:157c563eef6954ac0bc583c36def96d8ed2d3b3c5b37214f27d210ac53942386
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
$ docker pull memcached@sha256:742d5665f0f292e1278bafd0dff520b5f4edb101c587c29fb0ef273f9d7e124f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30319041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc1024c223c5953b97de26e48cce8df89bee4493e37781f6826e6df56c590056`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1759104000'
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
	-	`sha256:d2a243ecf382412941b4d6772dba911a8093cf3703c933872fbb7ecc21e27e20`  
		Last Modified: Mon, 29 Sep 2025 23:34:24 GMT  
		Size: 27.9 MB (27946145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d24bdf1148108d2d3fc42a07dae247e5242de03db9a71e04066262a853f139d`  
		Last Modified: Mon, 29 Sep 2025 23:59:31 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e717ac34c0d292ae77e9118ac1581d40d881e518d32d9e64f01fddf818164b`  
		Last Modified: Mon, 29 Sep 2025 23:59:31 GMT  
		Size: 144.0 KB (144036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a3b7d16c874ce52964b6ba216127f7fcf604d326cc965210eb58119d605d28`  
		Last Modified: Mon, 29 Sep 2025 23:59:31 GMT  
		Size: 2.2 MB (2227345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb7f38fc7bbd06b5c988a48649d103d93ab0d8011b6a4f5bd8ad38bbd4cac432`  
		Last Modified: Mon, 29 Sep 2025 23:59:31 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5307470e3430d06e3f04b798774d1905a98a13f5ba3387596a0aa97e34b7eba`  
		Last Modified: Mon, 29 Sep 2025 23:59:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:92764b7963e735b77f5e5b433bf1311bc919679a81273cf442178538cf7da2ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:512f0e0d6001116f7984270337608de656664abeb7602b6fc4add42303ba8ee6`

```dockerfile
```

-	Layers:
	-	`sha256:a8fc1cbacd56787b740b886369c6eaafa6151c97fade289ea774600c03a80e11`  
		Last Modified: Tue, 30 Sep 2025 00:34:39 GMT  
		Size: 2.0 MB (2011183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57884b3635fcf7e290933e3a1da7210a05c98ab3187a6e484a5cc8cedf845e98`  
		Last Modified: Tue, 30 Sep 2025 00:34:39 GMT  
		Size: 22.3 KB (22347 bytes)  
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
$ docker pull memcached@sha256:5a071a15dfae20029d56a8845f8053a4f4447934a87e0db0678b6f4ddc2e924a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36187246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6957fdbfa2f978334c6c02013b0e9b928534ddf41009ccae3597ccaf389fd455`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
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
	-	`sha256:8bcecd3ced4047f6a4d35464fc2ee9b45e7fcc10b49690427794f4421b0552ab`  
		Last Modified: Mon, 29 Sep 2025 23:41:19 GMT  
		Size: 33.6 MB (33598454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cee3e1fdea897c6a6b3a982e1918145b5bcd716e5ae6ed66b5e7184e651e059`  
		Last Modified: Tue, 30 Sep 2025 07:50:11 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dea6ee42e2fcf50b7f0d213d52ea27f8eebdaf12c0aa80c5df4828c4566af25`  
		Last Modified: Tue, 30 Sep 2025 07:50:12 GMT  
		Size: 170.3 KB (170259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629d93745cabb21520c860c7612f141299a2c0f2632cf40b7dcc88799307dcd7`  
		Last Modified: Tue, 30 Sep 2025 07:50:13 GMT  
		Size: 2.4 MB (2417019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afbd1630af2c91474bfc04cf614cc4d0a7093510b706f978f20f426127e93305`  
		Last Modified: Tue, 30 Sep 2025 07:50:12 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8293ad839e50f443a419fb4c0f6a6dbde6204ad3bf467cdff6e99385a7d1c3`  
		Last Modified: Tue, 30 Sep 2025 07:50:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:987b950cf472a2d95cc860d4c3c9e95c51ab792c33f5ac61607b7e4f38d1d8d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:973c6753846fed972084489bd202cf7da6e77ddc33d584a90658a8949b5730ee`

```dockerfile
```

-	Layers:
	-	`sha256:821a5821beef4d6bdae90ea0d98277dd982af05804dd43f706310bc7263244c4`  
		Last Modified: Wed, 01 Oct 2025 21:34:36 GMT  
		Size: 2.0 MB (2011781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:222d48bb5ef6a86d72ecccaf90a1cd7cf49c644139aee33815b1e7d0fd87cfcb`  
		Last Modified: Wed, 01 Oct 2025 21:34:36 GMT  
		Size: 22.3 KB (22270 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.39-trixie` - linux; riscv64

```console
$ docker pull memcached@sha256:31bb76b9b98cd96febc6b1d5056f839ffab9aaaa12690d0a47353df1b2b49221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30629784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e010912f76722a300766eb6afe7e6b13e8f72682c8dec557d00826b2a7cba503`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1759104000'
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
	-	`sha256:ecc6f9aec21fb94a493c2875c244e720a2f7c6c034063ce87b2f5b6b46962ec9`  
		Last Modified: Tue, 30 Sep 2025 01:05:14 GMT  
		Size: 28.3 MB (28275502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c2f28b5ea15f2b021d2f93df684963b9d27de2301bfccbf53d01abc5bdaa97`  
		Last Modified: Tue, 30 Sep 2025 04:00:18 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179b31cc3aad1ab89917cf87cb268b6e8e4291ec4b8996317231c4ac0003ebf9`  
		Last Modified: Tue, 30 Sep 2025 04:00:18 GMT  
		Size: 133.0 KB (132970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca5db35fb11036dcb8f2d55bbe271869356c9b4b2e08c0d0293a9b0c894f5dff`  
		Last Modified: Tue, 30 Sep 2025 04:00:19 GMT  
		Size: 2.2 MB (2219797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc4c908359c51ce26778438a3886b2eb2d6987ee3a22862dbdbe2056a3cd95d`  
		Last Modified: Tue, 30 Sep 2025 04:00:19 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7254f9df049c190c1c3ffa9794b395fb4e3ec7ab18b8dce7a58733c63a54dd`  
		Last Modified: Tue, 30 Sep 2025 04:00:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.39-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:10dcedf955ee46896155ca87f9a292967d1ce021fbab41f3a0fc44045a885e25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85a06d87da790b7800c970ca38989414eeae6c950cf890286591dc59c6163cc5`

```dockerfile
```

-	Layers:
	-	`sha256:b8fb80942d713e49171d0a98b2306b7bbb0023e57f180295e56893f7ea7f458d`  
		Last Modified: Tue, 30 Sep 2025 06:34:34 GMT  
		Size: 2.0 MB (2002144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cbc67dcbbe8db9619b2b3e3b962ebb7d9640901e2048fa63620351cc03d940d`  
		Last Modified: Tue, 30 Sep 2025 06:34:34 GMT  
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
$ docker pull memcached@sha256:eca5d776fe62e6ffe5e27e1a4d357e0bbd9ac609a271243c210599a898122ad2
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
$ docker pull memcached@sha256:033134f4dd9f45d4e22b6e98b040ea3fccf0dca740af3c949b44bebf458b04d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5904246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca259aa2216a248c482fc8a069d48b1e70b087529d2c3de97154bfa458dbb7a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23fb46bc7dee2beda6f5f6f567aecd4d7d7698b9749ed917988a859b7dd96e30`  
		Last Modified: Tue, 29 Jul 2025 16:32:22 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48faf8c85515fb9d17e0752e77d8241f223d53b1adc90439c606d17daabd0ae`  
		Last Modified: Tue, 29 Jul 2025 16:32:24 GMT  
		Size: 104.7 KB (104725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d552a2d777fd444b41cb79438f9f1b441821162e78d73e96dc848a773cf43892`  
		Last Modified: Tue, 29 Jul 2025 16:32:24 GMT  
		Size: 2.0 MB (1998477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c70665f30f3e15975d429b494cb17b21c5d4630c1800cb0addc3fce3a11aa29`  
		Last Modified: Tue, 29 Jul 2025 16:32:20 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ff68520caaf588cec750ad7c403cf55d79eecfff4b7a4ac5eb3910c90c2817`  
		Last Modified: Tue, 29 Jul 2025 16:32:21 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7b27e0df383f45d6d523345a078898524a69cee4d6978cf64bf26532b8679dca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 KB (116752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb88e7ee6d3e67b2e4f307c081504a685666917ddf50770fe8beb5abd60a3dc5`

```dockerfile
```

-	Layers:
	-	`sha256:2cf00a09ffccb2c00421311314137de90d0586c126b79dbe5315ce321c168b34`  
		Last Modified: Tue, 29 Jul 2025 18:35:07 GMT  
		Size: 96.2 KB (96180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55325ecc9b276e9c55badf949ed4f06840c34aa8baf0aa6f974e0b90dc5d4e0d`  
		Last Modified: Tue, 29 Jul 2025 18:35:07 GMT  
		Size: 20.6 KB (20572 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:78b59dd3af5a55e950f5106869e642af122a7dc470545f4ba533f6833d83b62c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5550795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb09d5ce1b7010f7a36d77494bc5358d666339628c183692906db6a961373847`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c710b5ddcc2882c5014d0c8cb93aec2bd8b6cc3c59fd42b40c87d94f89a7bc7f`  
		Last Modified: Wed, 23 Jul 2025 22:59:16 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c42040d822a4af7f05f9ccd4d18a7a5e4712b118b7f18d1a7969761029a9d2`  
		Last Modified: Wed, 23 Jul 2025 22:59:16 GMT  
		Size: 101.5 KB (101533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3095e18cd24048696efd57ac64d04dde381a3abde625964e02165c7364eb5633`  
		Last Modified: Tue, 29 Jul 2025 16:50:12 GMT  
		Size: 1.9 MB (1947003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0436ec50f04ed972ff0dd760f7e820f192236e5e720bddb6173f65159c7c36`  
		Last Modified: Tue, 29 Jul 2025 16:50:11 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671c24aae36bb04a32e05bd64e1371384f594889cdbbc41029c916447666d402`  
		Last Modified: Tue, 29 Jul 2025 16:50:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:c2a050c6822d834285577c3a001fdfcf9949b7f5a483a4a76a49b549bea19641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54e8bda3e734528caeab4505f084ca7a3076d5ec2273287f66954b5e91af42f`

```dockerfile
```

-	Layers:
	-	`sha256:0d86924831d61ce8b792b25421e9ff0fa2eda9ab940eba5309d44d0eeada7e8e`  
		Last Modified: Tue, 29 Jul 2025 18:35:11 GMT  
		Size: 20.5 KB (20506 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:c9f5db2389b9b0b4a2cd199c4417a9f49a60c42d616e8421177e662d4830de07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5217393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9421ed030d4b6b6405714612b8858bda87bc53ac8b0c5ed65c582119527f2d9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251060498ca8f0484e20714689b9caba533d09c1b74ed8f2a06780db515a28e2`  
		Last Modified: Thu, 24 Jul 2025 00:27:37 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2293bd2fb47d57e5869c197133067e17f9b1e51ea0f298af1e480e7fd33d681`  
		Last Modified: Thu, 24 Jul 2025 00:27:38 GMT  
		Size: 91.3 KB (91313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ae82f2bac2f7e6fe57f8cb7006fc227c972da1ae5749eba9f5f73e6f3248ec`  
		Last Modified: Tue, 29 Jul 2025 17:11:51 GMT  
		Size: 1.9 MB (1905692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e60bf2b2164c620b69e40bdcb64d4104d02eab86c96ea6e170a3601b9ecfd82`  
		Last Modified: Tue, 29 Jul 2025 17:11:51 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:665fe4cd856f1a5c2193568e756c572656949b17c381fc8d43efaa823e18cfa7`  
		Last Modified: Tue, 29 Jul 2025 17:11:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:376a71bc0fef7741e92fdae8b96c825c4622e980de01e724b1a3a0bec3d95f20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 KB (116963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22b574f6c6d021a917c0e99ff4800d8ac3c22fb94b94f88c404cc7609f562fb5`

```dockerfile
```

-	Layers:
	-	`sha256:58ebd4bc7ee5888c552e0fa618f93aefbdb1d15a56ecd3abef19a46ce2f93eee`  
		Last Modified: Tue, 29 Jul 2025 18:35:15 GMT  
		Size: 96.2 KB (96248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d432ed2053ed8249834dd5016fe3199bbc3f82dc7013027c3ead9efe2a007b98`  
		Last Modified: Tue, 29 Jul 2025 18:35:16 GMT  
		Size: 20.7 KB (20715 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:b5e4ecc3e927ee30e5cfcfc8aa044960631c75eb8abed9d0fcee6232aa5fdf79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6241700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40c880dc2c785861dc9010b813bb6f533f30518443a3bb7e7f477bc96af14582`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfbfeb6ac9fd2045c5bea10a301ad554c1f703ffc2885c41520dd5e42eb4a59a`  
		Last Modified: Tue, 29 Jul 2025 16:41:08 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47acaa5035f94aed634b9d7ecae02fb3838f19e38f8e752ecd6cfba97699b31`  
		Last Modified: Tue, 29 Jul 2025 16:41:08 GMT  
		Size: 120.8 KB (120812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8160f3136c6863b52f0dec4f9918b91b8a509700b2071ec0aecd5a6231f00f2a`  
		Last Modified: Tue, 29 Jul 2025 16:41:09 GMT  
		Size: 2.0 MB (1988782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff22f0cad01950efb78a7a862b0becb8b2fd22d795b585f97dad66c091c3dd7`  
		Last Modified: Tue, 29 Jul 2025 16:41:08 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed19cbfb574c7d8cab364e2ec072c0e03f694468ada41cd70bfcd35392df9e7`  
		Last Modified: Tue, 29 Jul 2025 16:41:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:b4c81c7ababb91ecdda3b7d70514d16818602199d759eb2aadd74de732d52960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.1 KB (117055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80452fd4f79f6e7a0dab0beebf5c144f9df7c257255cdd3cb93ccbff77001fd6`

```dockerfile
```

-	Layers:
	-	`sha256:f11d2a322f6088804ee63ae1a77b9d5ddcdfdc0c65c22e7a70b7ee67cf4532ed`  
		Last Modified: Tue, 29 Jul 2025 18:35:20 GMT  
		Size: 96.3 KB (96284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e225dd6ea14146ddf445598f24189c065ec684fbeb92e7d053a0211a7d60efda`  
		Last Modified: Tue, 29 Jul 2025 18:35:21 GMT  
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
$ docker pull memcached@sha256:04386ede5dcbf35cabad144bcdc951cc64882f7b9727f2d09927fe0d5551dd19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5942089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8252590eee78d67456ac83fd8279259aaea4d2a555c8bc20b173663fcaa2883`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc22e0cec7e7fe8cff10539bca58363ad6749e2de4f878015c25b5f2b6ecadb9`  
		Last Modified: Tue, 29 Jul 2025 16:33:46 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992ebe18219bd78e59e7e56661aae22f700927f47bc7ad1dfe7717093b371c15`  
		Last Modified: Tue, 29 Jul 2025 16:33:49 GMT  
		Size: 124.3 KB (124315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953f5a37d23881d59809ea64dc6ebf1a152a1ff8929f51befb10577771755f5d`  
		Last Modified: Tue, 29 Jul 2025 16:33:49 GMT  
		Size: 2.1 MB (2089310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10b62870a2d7b266495d83cfd72dcf702c91c5c60a7e29836bd9bdac776511a7`  
		Last Modified: Tue, 29 Jul 2025 16:33:47 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1cc8c0fe9a4ef7e2ef70e32ddbfbd2fd68985dd452630a8f390c5b41c654f8`  
		Last Modified: Tue, 29 Jul 2025 16:33:47 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:cf7e9735e4ef5d00dc25928653b808214f070708e9d879ef54afc4d77ce9db2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcceb455cfdb86bdb0c165af3bc54cbab794d56fef1dbae2b484d28027db791c`

```dockerfile
```

-	Layers:
	-	`sha256:a40704a0afb5cf1b90c0fbdf73c5218a4d8f0e93bb39014507b5fa5f8c7265dd`  
		Last Modified: Tue, 29 Jul 2025 18:35:29 GMT  
		Size: 94.3 KB (94287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da22397f364310e72420738395739c36e25b4e4813bbc5da197582a91bb55ac9`  
		Last Modified: Tue, 29 Jul 2025 18:35:29 GMT  
		Size: 20.6 KB (20648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:d55b98c34ba1c2f546461bd57477d46ab868f9de6b107ffb8f20e06dab1e10d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5555034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1034dde2661f43165e85db9a13ff0e10d237d14d4b1b7ee1d4570f19d7df4e69`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00bbdcecb4dec3cbaba0500f9425897948884cfd8db95ccdf9b824d448b24049`  
		Last Modified: Wed, 23 Jul 2025 23:54:15 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c18051d55886d147cafcee8f9e220087c0b60c0e11ec8898a4005352ee0f7e4`  
		Last Modified: Wed, 23 Jul 2025 23:50:14 GMT  
		Size: 107.9 KB (107902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953c2b44fe537b63907764cf78cbb294c6a1133eacb39c62d35ee5d4914779cb`  
		Last Modified: Tue, 29 Jul 2025 16:42:10 GMT  
		Size: 1.9 MB (1932977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d69b2f63abf91684a15b9de7b5e617996762376da3fdda50c4e20c2f1e0f4da`  
		Last Modified: Tue, 29 Jul 2025 16:42:10 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f57c134601fc15e8f2cf183cfd9a3057731ad48b915988217f51df31b5d3cf38`  
		Last Modified: Tue, 29 Jul 2025 16:42:10 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:d50b42de80ef3381b05da20cef4ba6ab4491facb607528e075c034257fe9d327
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27766c161110b7e46063a39ce6e176f87233fd6722a825ec338e1568892a77a3`

```dockerfile
```

-	Layers:
	-	`sha256:f933f968a4a14795196607a1337a19431e9f61db78bb49c5c2f89f64a17a1d89`  
		Last Modified: Tue, 29 Jul 2025 18:35:33 GMT  
		Size: 94.3 KB (94283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffc41094fe9f57bca69da70bbb18eca52aaf6d27d0fb6d79eda79f9e011a157a`  
		Last Modified: Tue, 29 Jul 2025 18:35:33 GMT  
		Size: 20.6 KB (20647 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; s390x

```console
$ docker pull memcached@sha256:cfd223eb11df3d2297224d458caf974f3f0aae4742ff917812f1b8c84c84e705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5797268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78e23f18e891a12e72ef84139504baf8783a7db21d4976fc0b607f8e9bbf736f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f00131fb0ca26b15f1ac64b82554fc342b19f8c1ef38312a75addb6686f7bc24`  
		Last Modified: Tue, 29 Jul 2025 16:41:40 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e54da6ab620e035fd78987688d45401e87278ec8a5c02cef8a57e4ea9fd286`  
		Last Modified: Tue, 29 Jul 2025 16:41:42 GMT  
		Size: 113.5 KB (113499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6160f9fac1fd86eda224e9ce4740ea46f7e23dc7edb6d1fe9d830001313e63a`  
		Last Modified: Tue, 29 Jul 2025 16:41:46 GMT  
		Size: 2.0 MB (2037446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d01cd71d33b01b420652f4ad9275f1475f4f0bf253dc0a1b48198df2010be5`  
		Last Modified: Tue, 29 Jul 2025 16:41:52 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:831dd5e3c39dd2744dc8823190095f709c36020b55ccdaf85f62a146582c7d9d`  
		Last Modified: Tue, 29 Jul 2025 16:41:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:79f0de7e4dcc9afdbfa1fa22250cf3e544d6f3c33174246b427d2865c7e343d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71dad4d71741d8d354038cb6898389aebb54c956dfcd865d57f78dcc3b238bf8`

```dockerfile
```

-	Layers:
	-	`sha256:f942bbb9520308ae352a056c148fdce8f6b09672c257e0a769aa2504bacf1845`  
		Last Modified: Tue, 29 Jul 2025 18:35:37 GMT  
		Size: 94.2 KB (94229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c46680ef7cf08a43965ab9c7727cc70268ee89e366a1ce1806d0f7980b4ad812`  
		Last Modified: Tue, 29 Jul 2025 18:35:38 GMT  
		Size: 20.6 KB (20574 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine3.22`

```console
$ docker pull memcached@sha256:eca5d776fe62e6ffe5e27e1a4d357e0bbd9ac609a271243c210599a898122ad2
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
$ docker pull memcached@sha256:033134f4dd9f45d4e22b6e98b040ea3fccf0dca740af3c949b44bebf458b04d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5904246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca259aa2216a248c482fc8a069d48b1e70b087529d2c3de97154bfa458dbb7a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23fb46bc7dee2beda6f5f6f567aecd4d7d7698b9749ed917988a859b7dd96e30`  
		Last Modified: Tue, 29 Jul 2025 16:32:22 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48faf8c85515fb9d17e0752e77d8241f223d53b1adc90439c606d17daabd0ae`  
		Last Modified: Tue, 29 Jul 2025 16:32:24 GMT  
		Size: 104.7 KB (104725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d552a2d777fd444b41cb79438f9f1b441821162e78d73e96dc848a773cf43892`  
		Last Modified: Tue, 29 Jul 2025 16:32:24 GMT  
		Size: 2.0 MB (1998477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c70665f30f3e15975d429b494cb17b21c5d4630c1800cb0addc3fce3a11aa29`  
		Last Modified: Tue, 29 Jul 2025 16:32:20 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ff68520caaf588cec750ad7c403cf55d79eecfff4b7a4ac5eb3910c90c2817`  
		Last Modified: Tue, 29 Jul 2025 16:32:21 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:7b27e0df383f45d6d523345a078898524a69cee4d6978cf64bf26532b8679dca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 KB (116752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb88e7ee6d3e67b2e4f307c081504a685666917ddf50770fe8beb5abd60a3dc5`

```dockerfile
```

-	Layers:
	-	`sha256:2cf00a09ffccb2c00421311314137de90d0586c126b79dbe5315ce321c168b34`  
		Last Modified: Tue, 29 Jul 2025 18:35:07 GMT  
		Size: 96.2 KB (96180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55325ecc9b276e9c55badf949ed4f06840c34aa8baf0aa6f974e0b90dc5d4e0d`  
		Last Modified: Tue, 29 Jul 2025 18:35:07 GMT  
		Size: 20.6 KB (20572 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.22` - linux; arm variant v6

```console
$ docker pull memcached@sha256:78b59dd3af5a55e950f5106869e642af122a7dc470545f4ba533f6833d83b62c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5550795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb09d5ce1b7010f7a36d77494bc5358d666339628c183692906db6a961373847`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c710b5ddcc2882c5014d0c8cb93aec2bd8b6cc3c59fd42b40c87d94f89a7bc7f`  
		Last Modified: Wed, 23 Jul 2025 22:59:16 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c42040d822a4af7f05f9ccd4d18a7a5e4712b118b7f18d1a7969761029a9d2`  
		Last Modified: Wed, 23 Jul 2025 22:59:16 GMT  
		Size: 101.5 KB (101533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3095e18cd24048696efd57ac64d04dde381a3abde625964e02165c7364eb5633`  
		Last Modified: Tue, 29 Jul 2025 16:50:12 GMT  
		Size: 1.9 MB (1947003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0436ec50f04ed972ff0dd760f7e820f192236e5e720bddb6173f65159c7c36`  
		Last Modified: Tue, 29 Jul 2025 16:50:11 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671c24aae36bb04a32e05bd64e1371384f594889cdbbc41029c916447666d402`  
		Last Modified: Tue, 29 Jul 2025 16:50:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:c2a050c6822d834285577c3a001fdfcf9949b7f5a483a4a76a49b549bea19641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54e8bda3e734528caeab4505f084ca7a3076d5ec2273287f66954b5e91af42f`

```dockerfile
```

-	Layers:
	-	`sha256:0d86924831d61ce8b792b25421e9ff0fa2eda9ab940eba5309d44d0eeada7e8e`  
		Last Modified: Tue, 29 Jul 2025 18:35:11 GMT  
		Size: 20.5 KB (20506 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.22` - linux; arm variant v7

```console
$ docker pull memcached@sha256:c9f5db2389b9b0b4a2cd199c4417a9f49a60c42d616e8421177e662d4830de07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5217393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9421ed030d4b6b6405714612b8858bda87bc53ac8b0c5ed65c582119527f2d9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251060498ca8f0484e20714689b9caba533d09c1b74ed8f2a06780db515a28e2`  
		Last Modified: Thu, 24 Jul 2025 00:27:37 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2293bd2fb47d57e5869c197133067e17f9b1e51ea0f298af1e480e7fd33d681`  
		Last Modified: Thu, 24 Jul 2025 00:27:38 GMT  
		Size: 91.3 KB (91313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ae82f2bac2f7e6fe57f8cb7006fc227c972da1ae5749eba9f5f73e6f3248ec`  
		Last Modified: Tue, 29 Jul 2025 17:11:51 GMT  
		Size: 1.9 MB (1905692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e60bf2b2164c620b69e40bdcb64d4104d02eab86c96ea6e170a3601b9ecfd82`  
		Last Modified: Tue, 29 Jul 2025 17:11:51 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:665fe4cd856f1a5c2193568e756c572656949b17c381fc8d43efaa823e18cfa7`  
		Last Modified: Tue, 29 Jul 2025 17:11:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:376a71bc0fef7741e92fdae8b96c825c4622e980de01e724b1a3a0bec3d95f20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 KB (116963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22b574f6c6d021a917c0e99ff4800d8ac3c22fb94b94f88c404cc7609f562fb5`

```dockerfile
```

-	Layers:
	-	`sha256:58ebd4bc7ee5888c552e0fa618f93aefbdb1d15a56ecd3abef19a46ce2f93eee`  
		Last Modified: Tue, 29 Jul 2025 18:35:15 GMT  
		Size: 96.2 KB (96248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d432ed2053ed8249834dd5016fe3199bbc3f82dc7013027c3ead9efe2a007b98`  
		Last Modified: Tue, 29 Jul 2025 18:35:16 GMT  
		Size: 20.7 KB (20715 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.22` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:b5e4ecc3e927ee30e5cfcfc8aa044960631c75eb8abed9d0fcee6232aa5fdf79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6241700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40c880dc2c785861dc9010b813bb6f533f30518443a3bb7e7f477bc96af14582`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfbfeb6ac9fd2045c5bea10a301ad554c1f703ffc2885c41520dd5e42eb4a59a`  
		Last Modified: Tue, 29 Jul 2025 16:41:08 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47acaa5035f94aed634b9d7ecae02fb3838f19e38f8e752ecd6cfba97699b31`  
		Last Modified: Tue, 29 Jul 2025 16:41:08 GMT  
		Size: 120.8 KB (120812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8160f3136c6863b52f0dec4f9918b91b8a509700b2071ec0aecd5a6231f00f2a`  
		Last Modified: Tue, 29 Jul 2025 16:41:09 GMT  
		Size: 2.0 MB (1988782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff22f0cad01950efb78a7a862b0becb8b2fd22d795b585f97dad66c091c3dd7`  
		Last Modified: Tue, 29 Jul 2025 16:41:08 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed19cbfb574c7d8cab364e2ec072c0e03f694468ada41cd70bfcd35392df9e7`  
		Last Modified: Tue, 29 Jul 2025 16:41:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:b4c81c7ababb91ecdda3b7d70514d16818602199d759eb2aadd74de732d52960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.1 KB (117055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80452fd4f79f6e7a0dab0beebf5c144f9df7c257255cdd3cb93ccbff77001fd6`

```dockerfile
```

-	Layers:
	-	`sha256:f11d2a322f6088804ee63ae1a77b9d5ddcdfdc0c65c22e7a70b7ee67cf4532ed`  
		Last Modified: Tue, 29 Jul 2025 18:35:20 GMT  
		Size: 96.3 KB (96284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e225dd6ea14146ddf445598f24189c065ec684fbeb92e7d053a0211a7d60efda`  
		Last Modified: Tue, 29 Jul 2025 18:35:21 GMT  
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
$ docker pull memcached@sha256:04386ede5dcbf35cabad144bcdc951cc64882f7b9727f2d09927fe0d5551dd19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5942089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8252590eee78d67456ac83fd8279259aaea4d2a555c8bc20b173663fcaa2883`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc22e0cec7e7fe8cff10539bca58363ad6749e2de4f878015c25b5f2b6ecadb9`  
		Last Modified: Tue, 29 Jul 2025 16:33:46 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992ebe18219bd78e59e7e56661aae22f700927f47bc7ad1dfe7717093b371c15`  
		Last Modified: Tue, 29 Jul 2025 16:33:49 GMT  
		Size: 124.3 KB (124315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953f5a37d23881d59809ea64dc6ebf1a152a1ff8929f51befb10577771755f5d`  
		Last Modified: Tue, 29 Jul 2025 16:33:49 GMT  
		Size: 2.1 MB (2089310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10b62870a2d7b266495d83cfd72dcf702c91c5c60a7e29836bd9bdac776511a7`  
		Last Modified: Tue, 29 Jul 2025 16:33:47 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1cc8c0fe9a4ef7e2ef70e32ddbfbd2fd68985dd452630a8f390c5b41c654f8`  
		Last Modified: Tue, 29 Jul 2025 16:33:47 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:cf7e9735e4ef5d00dc25928653b808214f070708e9d879ef54afc4d77ce9db2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcceb455cfdb86bdb0c165af3bc54cbab794d56fef1dbae2b484d28027db791c`

```dockerfile
```

-	Layers:
	-	`sha256:a40704a0afb5cf1b90c0fbdf73c5218a4d8f0e93bb39014507b5fa5f8c7265dd`  
		Last Modified: Tue, 29 Jul 2025 18:35:29 GMT  
		Size: 94.3 KB (94287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da22397f364310e72420738395739c36e25b4e4813bbc5da197582a91bb55ac9`  
		Last Modified: Tue, 29 Jul 2025 18:35:29 GMT  
		Size: 20.6 KB (20648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.22` - linux; riscv64

```console
$ docker pull memcached@sha256:d55b98c34ba1c2f546461bd57477d46ab868f9de6b107ffb8f20e06dab1e10d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5555034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1034dde2661f43165e85db9a13ff0e10d237d14d4b1b7ee1d4570f19d7df4e69`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00bbdcecb4dec3cbaba0500f9425897948884cfd8db95ccdf9b824d448b24049`  
		Last Modified: Wed, 23 Jul 2025 23:54:15 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c18051d55886d147cafcee8f9e220087c0b60c0e11ec8898a4005352ee0f7e4`  
		Last Modified: Wed, 23 Jul 2025 23:50:14 GMT  
		Size: 107.9 KB (107902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953c2b44fe537b63907764cf78cbb294c6a1133eacb39c62d35ee5d4914779cb`  
		Last Modified: Tue, 29 Jul 2025 16:42:10 GMT  
		Size: 1.9 MB (1932977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d69b2f63abf91684a15b9de7b5e617996762376da3fdda50c4e20c2f1e0f4da`  
		Last Modified: Tue, 29 Jul 2025 16:42:10 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f57c134601fc15e8f2cf183cfd9a3057731ad48b915988217f51df31b5d3cf38`  
		Last Modified: Tue, 29 Jul 2025 16:42:10 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:d50b42de80ef3381b05da20cef4ba6ab4491facb607528e075c034257fe9d327
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27766c161110b7e46063a39ce6e176f87233fd6722a825ec338e1568892a77a3`

```dockerfile
```

-	Layers:
	-	`sha256:f933f968a4a14795196607a1337a19431e9f61db78bb49c5c2f89f64a17a1d89`  
		Last Modified: Tue, 29 Jul 2025 18:35:33 GMT  
		Size: 94.3 KB (94283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffc41094fe9f57bca69da70bbb18eca52aaf6d27d0fb6d79eda79f9e011a157a`  
		Last Modified: Tue, 29 Jul 2025 18:35:33 GMT  
		Size: 20.6 KB (20647 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.22` - linux; s390x

```console
$ docker pull memcached@sha256:cfd223eb11df3d2297224d458caf974f3f0aae4742ff917812f1b8c84c84e705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5797268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78e23f18e891a12e72ef84139504baf8783a7db21d4976fc0b607f8e9bbf736f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
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
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f00131fb0ca26b15f1ac64b82554fc342b19f8c1ef38312a75addb6686f7bc24`  
		Last Modified: Tue, 29 Jul 2025 16:41:40 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e54da6ab620e035fd78987688d45401e87278ec8a5c02cef8a57e4ea9fd286`  
		Last Modified: Tue, 29 Jul 2025 16:41:42 GMT  
		Size: 113.5 KB (113499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6160f9fac1fd86eda224e9ce4740ea46f7e23dc7edb6d1fe9d830001313e63a`  
		Last Modified: Tue, 29 Jul 2025 16:41:46 GMT  
		Size: 2.0 MB (2037446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d01cd71d33b01b420652f4ad9275f1475f4f0bf253dc0a1b48198df2010be5`  
		Last Modified: Tue, 29 Jul 2025 16:41:52 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:831dd5e3c39dd2744dc8823190095f709c36020b55ccdaf85f62a146582c7d9d`  
		Last Modified: Tue, 29 Jul 2025 16:41:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:79f0de7e4dcc9afdbfa1fa22250cf3e544d6f3c33174246b427d2865c7e343d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71dad4d71741d8d354038cb6898389aebb54c956dfcd865d57f78dcc3b238bf8`

```dockerfile
```

-	Layers:
	-	`sha256:f942bbb9520308ae352a056c148fdce8f6b09672c257e0a769aa2504bacf1845`  
		Last Modified: Tue, 29 Jul 2025 18:35:37 GMT  
		Size: 94.2 KB (94229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c46680ef7cf08a43965ab9c7727cc70268ee89e366a1ce1806d0f7980b4ad812`  
		Last Modified: Tue, 29 Jul 2025 18:35:38 GMT  
		Size: 20.6 KB (20574 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:latest`

```console
$ docker pull memcached@sha256:157c563eef6954ac0bc583c36def96d8ed2d3b3c5b37214f27d210ac53942386
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
$ docker pull memcached@sha256:742d5665f0f292e1278bafd0dff520b5f4edb101c587c29fb0ef273f9d7e124f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30319041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc1024c223c5953b97de26e48cce8df89bee4493e37781f6826e6df56c590056`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1759104000'
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
	-	`sha256:d2a243ecf382412941b4d6772dba911a8093cf3703c933872fbb7ecc21e27e20`  
		Last Modified: Mon, 29 Sep 2025 23:34:24 GMT  
		Size: 27.9 MB (27946145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d24bdf1148108d2d3fc42a07dae247e5242de03db9a71e04066262a853f139d`  
		Last Modified: Mon, 29 Sep 2025 23:59:31 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e717ac34c0d292ae77e9118ac1581d40d881e518d32d9e64f01fddf818164b`  
		Last Modified: Mon, 29 Sep 2025 23:59:31 GMT  
		Size: 144.0 KB (144036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a3b7d16c874ce52964b6ba216127f7fcf604d326cc965210eb58119d605d28`  
		Last Modified: Mon, 29 Sep 2025 23:59:31 GMT  
		Size: 2.2 MB (2227345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb7f38fc7bbd06b5c988a48649d103d93ab0d8011b6a4f5bd8ad38bbd4cac432`  
		Last Modified: Mon, 29 Sep 2025 23:59:31 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5307470e3430d06e3f04b798774d1905a98a13f5ba3387596a0aa97e34b7eba`  
		Last Modified: Mon, 29 Sep 2025 23:59:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:92764b7963e735b77f5e5b433bf1311bc919679a81273cf442178538cf7da2ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:512f0e0d6001116f7984270337608de656664abeb7602b6fc4add42303ba8ee6`

```dockerfile
```

-	Layers:
	-	`sha256:a8fc1cbacd56787b740b886369c6eaafa6151c97fade289ea774600c03a80e11`  
		Last Modified: Tue, 30 Sep 2025 00:34:39 GMT  
		Size: 2.0 MB (2011183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57884b3635fcf7e290933e3a1da7210a05c98ab3187a6e484a5cc8cedf845e98`  
		Last Modified: Tue, 30 Sep 2025 00:34:39 GMT  
		Size: 22.3 KB (22347 bytes)  
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
$ docker pull memcached@sha256:5a071a15dfae20029d56a8845f8053a4f4447934a87e0db0678b6f4ddc2e924a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36187246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6957fdbfa2f978334c6c02013b0e9b928534ddf41009ccae3597ccaf389fd455`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
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
	-	`sha256:8bcecd3ced4047f6a4d35464fc2ee9b45e7fcc10b49690427794f4421b0552ab`  
		Last Modified: Mon, 29 Sep 2025 23:41:19 GMT  
		Size: 33.6 MB (33598454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cee3e1fdea897c6a6b3a982e1918145b5bcd716e5ae6ed66b5e7184e651e059`  
		Last Modified: Tue, 30 Sep 2025 07:50:11 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dea6ee42e2fcf50b7f0d213d52ea27f8eebdaf12c0aa80c5df4828c4566af25`  
		Last Modified: Tue, 30 Sep 2025 07:50:12 GMT  
		Size: 170.3 KB (170259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629d93745cabb21520c860c7612f141299a2c0f2632cf40b7dcc88799307dcd7`  
		Last Modified: Tue, 30 Sep 2025 07:50:13 GMT  
		Size: 2.4 MB (2417019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afbd1630af2c91474bfc04cf614cc4d0a7093510b706f978f20f426127e93305`  
		Last Modified: Tue, 30 Sep 2025 07:50:12 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8293ad839e50f443a419fb4c0f6a6dbde6204ad3bf467cdff6e99385a7d1c3`  
		Last Modified: Tue, 30 Sep 2025 07:50:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:987b950cf472a2d95cc860d4c3c9e95c51ab792c33f5ac61607b7e4f38d1d8d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:973c6753846fed972084489bd202cf7da6e77ddc33d584a90658a8949b5730ee`

```dockerfile
```

-	Layers:
	-	`sha256:821a5821beef4d6bdae90ea0d98277dd982af05804dd43f706310bc7263244c4`  
		Last Modified: Wed, 01 Oct 2025 21:34:36 GMT  
		Size: 2.0 MB (2011781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:222d48bb5ef6a86d72ecccaf90a1cd7cf49c644139aee33815b1e7d0fd87cfcb`  
		Last Modified: Wed, 01 Oct 2025 21:34:36 GMT  
		Size: 22.3 KB (22270 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; riscv64

```console
$ docker pull memcached@sha256:31bb76b9b98cd96febc6b1d5056f839ffab9aaaa12690d0a47353df1b2b49221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30629784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e010912f76722a300766eb6afe7e6b13e8f72682c8dec557d00826b2a7cba503`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1759104000'
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
	-	`sha256:ecc6f9aec21fb94a493c2875c244e720a2f7c6c034063ce87b2f5b6b46962ec9`  
		Last Modified: Tue, 30 Sep 2025 01:05:14 GMT  
		Size: 28.3 MB (28275502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c2f28b5ea15f2b021d2f93df684963b9d27de2301bfccbf53d01abc5bdaa97`  
		Last Modified: Tue, 30 Sep 2025 04:00:18 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179b31cc3aad1ab89917cf87cb268b6e8e4291ec4b8996317231c4ac0003ebf9`  
		Last Modified: Tue, 30 Sep 2025 04:00:18 GMT  
		Size: 133.0 KB (132970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca5db35fb11036dcb8f2d55bbe271869356c9b4b2e08c0d0293a9b0c894f5dff`  
		Last Modified: Tue, 30 Sep 2025 04:00:19 GMT  
		Size: 2.2 MB (2219797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc4c908359c51ce26778438a3886b2eb2d6987ee3a22862dbdbe2056a3cd95d`  
		Last Modified: Tue, 30 Sep 2025 04:00:19 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7254f9df049c190c1c3ffa9794b395fb4e3ec7ab18b8dce7a58733c63a54dd`  
		Last Modified: Tue, 30 Sep 2025 04:00:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:10dcedf955ee46896155ca87f9a292967d1ce021fbab41f3a0fc44045a885e25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85a06d87da790b7800c970ca38989414eeae6c950cf890286591dc59c6163cc5`

```dockerfile
```

-	Layers:
	-	`sha256:b8fb80942d713e49171d0a98b2306b7bbb0023e57f180295e56893f7ea7f458d`  
		Last Modified: Tue, 30 Sep 2025 06:34:34 GMT  
		Size: 2.0 MB (2002144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cbc67dcbbe8db9619b2b3e3b962ebb7d9640901e2048fa63620351cc03d940d`  
		Last Modified: Tue, 30 Sep 2025 06:34:34 GMT  
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
$ docker pull memcached@sha256:157c563eef6954ac0bc583c36def96d8ed2d3b3c5b37214f27d210ac53942386
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
$ docker pull memcached@sha256:742d5665f0f292e1278bafd0dff520b5f4edb101c587c29fb0ef273f9d7e124f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30319041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc1024c223c5953b97de26e48cce8df89bee4493e37781f6826e6df56c590056`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1759104000'
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
	-	`sha256:d2a243ecf382412941b4d6772dba911a8093cf3703c933872fbb7ecc21e27e20`  
		Last Modified: Mon, 29 Sep 2025 23:34:24 GMT  
		Size: 27.9 MB (27946145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d24bdf1148108d2d3fc42a07dae247e5242de03db9a71e04066262a853f139d`  
		Last Modified: Mon, 29 Sep 2025 23:59:31 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e717ac34c0d292ae77e9118ac1581d40d881e518d32d9e64f01fddf818164b`  
		Last Modified: Mon, 29 Sep 2025 23:59:31 GMT  
		Size: 144.0 KB (144036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a3b7d16c874ce52964b6ba216127f7fcf604d326cc965210eb58119d605d28`  
		Last Modified: Mon, 29 Sep 2025 23:59:31 GMT  
		Size: 2.2 MB (2227345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb7f38fc7bbd06b5c988a48649d103d93ab0d8011b6a4f5bd8ad38bbd4cac432`  
		Last Modified: Mon, 29 Sep 2025 23:59:31 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5307470e3430d06e3f04b798774d1905a98a13f5ba3387596a0aa97e34b7eba`  
		Last Modified: Mon, 29 Sep 2025 23:59:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:92764b7963e735b77f5e5b433bf1311bc919679a81273cf442178538cf7da2ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:512f0e0d6001116f7984270337608de656664abeb7602b6fc4add42303ba8ee6`

```dockerfile
```

-	Layers:
	-	`sha256:a8fc1cbacd56787b740b886369c6eaafa6151c97fade289ea774600c03a80e11`  
		Last Modified: Tue, 30 Sep 2025 00:34:39 GMT  
		Size: 2.0 MB (2011183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57884b3635fcf7e290933e3a1da7210a05c98ab3187a6e484a5cc8cedf845e98`  
		Last Modified: Tue, 30 Sep 2025 00:34:39 GMT  
		Size: 22.3 KB (22347 bytes)  
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
$ docker pull memcached@sha256:5a071a15dfae20029d56a8845f8053a4f4447934a87e0db0678b6f4ddc2e924a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36187246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6957fdbfa2f978334c6c02013b0e9b928534ddf41009ccae3597ccaf389fd455`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
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
	-	`sha256:8bcecd3ced4047f6a4d35464fc2ee9b45e7fcc10b49690427794f4421b0552ab`  
		Last Modified: Mon, 29 Sep 2025 23:41:19 GMT  
		Size: 33.6 MB (33598454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cee3e1fdea897c6a6b3a982e1918145b5bcd716e5ae6ed66b5e7184e651e059`  
		Last Modified: Tue, 30 Sep 2025 07:50:11 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dea6ee42e2fcf50b7f0d213d52ea27f8eebdaf12c0aa80c5df4828c4566af25`  
		Last Modified: Tue, 30 Sep 2025 07:50:12 GMT  
		Size: 170.3 KB (170259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629d93745cabb21520c860c7612f141299a2c0f2632cf40b7dcc88799307dcd7`  
		Last Modified: Tue, 30 Sep 2025 07:50:13 GMT  
		Size: 2.4 MB (2417019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afbd1630af2c91474bfc04cf614cc4d0a7093510b706f978f20f426127e93305`  
		Last Modified: Tue, 30 Sep 2025 07:50:12 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8293ad839e50f443a419fb4c0f6a6dbde6204ad3bf467cdff6e99385a7d1c3`  
		Last Modified: Tue, 30 Sep 2025 07:50:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:987b950cf472a2d95cc860d4c3c9e95c51ab792c33f5ac61607b7e4f38d1d8d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:973c6753846fed972084489bd202cf7da6e77ddc33d584a90658a8949b5730ee`

```dockerfile
```

-	Layers:
	-	`sha256:821a5821beef4d6bdae90ea0d98277dd982af05804dd43f706310bc7263244c4`  
		Last Modified: Wed, 01 Oct 2025 21:34:36 GMT  
		Size: 2.0 MB (2011781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:222d48bb5ef6a86d72ecccaf90a1cd7cf49c644139aee33815b1e7d0fd87cfcb`  
		Last Modified: Wed, 01 Oct 2025 21:34:36 GMT  
		Size: 22.3 KB (22270 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; riscv64

```console
$ docker pull memcached@sha256:31bb76b9b98cd96febc6b1d5056f839ffab9aaaa12690d0a47353df1b2b49221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30629784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e010912f76722a300766eb6afe7e6b13e8f72682c8dec557d00826b2a7cba503`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 Aug 2025 00:54:11 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1759104000'
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
	-	`sha256:ecc6f9aec21fb94a493c2875c244e720a2f7c6c034063ce87b2f5b6b46962ec9`  
		Last Modified: Tue, 30 Sep 2025 01:05:14 GMT  
		Size: 28.3 MB (28275502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c2f28b5ea15f2b021d2f93df684963b9d27de2301bfccbf53d01abc5bdaa97`  
		Last Modified: Tue, 30 Sep 2025 04:00:18 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179b31cc3aad1ab89917cf87cb268b6e8e4291ec4b8996317231c4ac0003ebf9`  
		Last Modified: Tue, 30 Sep 2025 04:00:18 GMT  
		Size: 133.0 KB (132970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca5db35fb11036dcb8f2d55bbe271869356c9b4b2e08c0d0293a9b0c894f5dff`  
		Last Modified: Tue, 30 Sep 2025 04:00:19 GMT  
		Size: 2.2 MB (2219797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc4c908359c51ce26778438a3886b2eb2d6987ee3a22862dbdbe2056a3cd95d`  
		Last Modified: Tue, 30 Sep 2025 04:00:19 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7254f9df049c190c1c3ffa9794b395fb4e3ec7ab18b8dce7a58733c63a54dd`  
		Last Modified: Tue, 30 Sep 2025 04:00:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:10dcedf955ee46896155ca87f9a292967d1ce021fbab41f3a0fc44045a885e25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85a06d87da790b7800c970ca38989414eeae6c950cf890286591dc59c6163cc5`

```dockerfile
```

-	Layers:
	-	`sha256:b8fb80942d713e49171d0a98b2306b7bbb0023e57f180295e56893f7ea7f458d`  
		Last Modified: Tue, 30 Sep 2025 06:34:34 GMT  
		Size: 2.0 MB (2002144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cbc67dcbbe8db9619b2b3e3b962ebb7d9640901e2048fa63620351cc03d940d`  
		Last Modified: Tue, 30 Sep 2025 06:34:34 GMT  
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
