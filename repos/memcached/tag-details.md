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
-	[`memcached:1.6.40`](#memcached1640)
-	[`memcached:1.6.40-alpine`](#memcached1640-alpine)
-	[`memcached:1.6.40-alpine3.23`](#memcached1640-alpine323)
-	[`memcached:1.6.40-trixie`](#memcached1640-trixie)
-	[`memcached:alpine`](#memcachedalpine)
-	[`memcached:alpine3.23`](#memcachedalpine323)
-	[`memcached:latest`](#memcachedlatest)
-	[`memcached:trixie`](#memcachedtrixie)

## `memcached:1`

```console
$ docker pull memcached@sha256:e4e5eca37e4334f9579f10fcdd88a58c4eb9d0a8eacedde6ec49d4ea4391637a
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
$ docker pull memcached@sha256:1613c35e314db0c64d8b5679786ad99ced10069c3f9778d40b6c522ff3c04218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32190619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a38251b773d15614da3036dd0d756bbf4a7d16d27fe1c52023517a419372b245`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:22:30 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 13 Jan 2026 01:22:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:25:18 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 13 Jan 2026 01:25:18 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 13 Jan 2026 01:25:18 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 13 Jan 2026 01:25:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 13 Jan 2026 01:25:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:25:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 01:25:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:25:18 GMT
USER memcache
# Tue, 13 Jan 2026 01:25:18 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 13 Jan 2026 01:25:18 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:34 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b6e737e1a3eed198cc17e2b92231ab084bcf55ba90a36136e7a2f4fd04a95b`  
		Last Modified: Tue, 13 Jan 2026 01:25:30 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16835fec399670b74d32630a7368a65ca2a3c32d8b7a690d33bebc7b9e9458d`  
		Last Modified: Tue, 13 Jan 2026 01:25:30 GMT  
		Size: 136.7 KB (136737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c848acbad27f1c9d2fd95e0facabbb28d5d8be19e5fa5912e5474c1301522523`  
		Last Modified: Tue, 13 Jan 2026 01:25:25 GMT  
		Size: 2.3 MB (2278686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9529916038b7840d3177e93bf04b78390bb91bca78623bd9c0769f9e2a965079`  
		Last Modified: Tue, 13 Jan 2026 01:25:25 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24239fc168f5eb73ae9964e2cdcb3c3b878ae79835c6b94585cb648fd50479d`  
		Last Modified: Tue, 13 Jan 2026 01:25:26 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:0d72ad7b507d17cffe5dbec1ddecf1c254c3a85d2b605fa0ddbc9913ba4fc678
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe582f0cad77d385a3debb0f2acf0c96b7b85c6a7d2c95fcc54f938d63635c9`

```dockerfile
```

-	Layers:
	-	`sha256:7d598d8c3b4cd06481693da06e86554144167d205cc60f43382fafba94dd4592`  
		Last Modified: Tue, 13 Jan 2026 04:35:37 GMT  
		Size: 2.0 MB (2008290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dd2469227ab0e75822eb9d56a5d7c05f52a445840f65934e010a2562e509718`  
		Last Modified: Tue, 13 Jan 2026 01:25:24 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm variant v5

```console
$ docker pull memcached@sha256:efa6728c05b024b605597e5025f04155aab614b52f56b1b31a4c70a23f909e07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30298859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14119dc07998a4322ac912beaaf4e6ad16e5487f2243c332fdaad86bdce6f55e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:19:21 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 13 Jan 2026 01:19:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:22:43 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 13 Jan 2026 01:22:43 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 13 Jan 2026 01:22:43 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 13 Jan 2026 01:22:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 13 Jan 2026 01:22:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:22:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 01:22:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:22:43 GMT
USER memcache
# Tue, 13 Jan 2026 01:22:43 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 13 Jan 2026 01:22:43 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c113d410d30c2c035a105b56d3937958c81fbe2530f44add3bae903be6864324`  
		Last Modified: Tue, 13 Jan 2026 00:42:30 GMT  
		Size: 27.9 MB (27942724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96776850dc1206c3fd163b84cea19599306159eb0d020b4241d0172240f88d13`  
		Last Modified: Tue, 13 Jan 2026 01:22:55 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3697c7c790d9c4caaa904abdaf809dcdee3f0b518fc5ad82d2e21dd7fe24f64d`  
		Last Modified: Tue, 13 Jan 2026 01:22:55 GMT  
		Size: 144.2 KB (144212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a247339c7ec57a491c3ffe43531dbfaa132f3ff16a481fc41cbb9e3e3ad6476`  
		Last Modified: Tue, 13 Jan 2026 01:22:50 GMT  
		Size: 2.2 MB (2210412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2dcebe3ab2a9945cdea142301e4a64eebbc59c948a54385dbfca4afd561b508`  
		Last Modified: Tue, 13 Jan 2026 01:22:55 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb8ef5ecbc44efd5280f9cf15687dfd80a34fa2966ad039238647177f75dc6c`  
		Last Modified: Tue, 13 Jan 2026 01:22:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:190bb1ecd7376720e541621921c2d4931a9d0f85a047255ba2b56afa3a504212
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9736e9545a46e4ef65dcb5238691292d27fac4dccb330354ce59ac93ae6994b5`

```dockerfile
```

-	Layers:
	-	`sha256:4f5461bf596f750b56b3f10e315936c2326b2c32901d28cdf22db97072bba685`  
		Last Modified: Tue, 13 Jan 2026 01:22:50 GMT  
		Size: 2.0 MB (2011293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8657d28d0436d39193457fb90119ea6e4ddb566df2a83fd1aa9df75651731188`  
		Last Modified: Tue, 13 Jan 2026 04:35:43 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm variant v7

```console
$ docker pull memcached@sha256:9c322c838b4648fa30e742e53ed6647a31383760fb73fa82de32b4b6dc88c494
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28509532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6e130248535c57fccff4d89a9d442e31cabd471e41c9eed52e5207a54f9f944`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:25:47 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 13 Jan 2026 01:25:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:28:55 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 13 Jan 2026 01:28:55 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 13 Jan 2026 01:28:55 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 13 Jan 2026 01:28:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 13 Jan 2026 01:28:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:28:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 01:28:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:28:55 GMT
USER memcache
# Tue, 13 Jan 2026 01:28:55 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 13 Jan 2026 01:28:55 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029a2cbe46c1e12ab6d47a63f40fb29056b6c6277c7822085ed0fe62e0a1791d`  
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c7827f95482598f1bd32dd8cbe071ad009795fa108661234eeb872d1a1e8bd`  
		Last Modified: Tue, 13 Jan 2026 01:29:07 GMT  
		Size: 135.4 KB (135398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9371e974781bd91adc657086f00cd7d91b5530ca9da37597c347dd7d4eaff0`  
		Last Modified: Tue, 13 Jan 2026 01:29:07 GMT  
		Size: 2.2 MB (2164040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c2e0f64c0afa16b5e214ae208c8c81e8c78c79ddd90f54983a93c7297395f6b`  
		Last Modified: Tue, 13 Jan 2026 01:29:07 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92151d443057f88ed7f60405440b698ff9e6abe1a2ca1c91a0c7e7626339ad2`  
		Last Modified: Tue, 13 Jan 2026 01:29:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:12cc31a1ce56d2c6dd1c0dcfd4ef1fe74484985d010594950c086c0f4431559b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b2d844d5393973080c37fde0b92cd48bd1a64e03973290631be5486d814de7e`

```dockerfile
```

-	Layers:
	-	`sha256:99fc27444c1ccdd6cbd08a33aac22e9e85f55958bda7b6216bdea08eae374cff`  
		Last Modified: Tue, 13 Jan 2026 04:35:47 GMT  
		Size: 2.0 MB (2009750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e76d5584f581b7668c61a661da2858bc1d5e11b31e3629e0d2b3af52d9c22ed8`  
		Last Modified: Tue, 13 Jan 2026 04:35:47 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:2ed537fa0376a3eb0864d6a3b51ea7da59b9ff4bb3270189a8a5082f02f811e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32550406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf26d75d787aabbd202c97db1079b96e45105d3ca509a1001ab973cb473cae8c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:22:29 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 13 Jan 2026 01:22:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:25:26 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 13 Jan 2026 01:25:26 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 13 Jan 2026 01:25:26 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 13 Jan 2026 01:25:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 13 Jan 2026 01:25:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:25:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 01:25:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:25:27 GMT
USER memcache
# Tue, 13 Jan 2026 01:25:27 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 13 Jan 2026 01:25:27 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78edb6b991369235f90958a936afc89dc37b82439c632988ed143b5bd76deadb`  
		Last Modified: Tue, 13 Jan 2026 01:25:40 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e1afbb765f6cc3923e864d44fb6cd6c9167b884e596b09bd37c7c276f65a2b`  
		Last Modified: Tue, 13 Jan 2026 01:25:40 GMT  
		Size: 153.5 KB (153512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff9edc68fe57c233001afd442eb6c248bf070d32fbb412a8bfeef6f9a6217f5`  
		Last Modified: Tue, 13 Jan 2026 01:25:40 GMT  
		Size: 2.3 MB (2261341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c4648fbc4a4189184946895d1041e0eee2c5d40fd70638a553bedb0cbf5cf8`  
		Last Modified: Tue, 13 Jan 2026 01:25:40 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26bd1b32b048e73091ddf6e6762e368d4bb6ef2cc7d3aa43467749b36fe08e38`  
		Last Modified: Tue, 13 Jan 2026 01:25:40 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:72333c6222fb20b5a9f9f92b8d56c47ebb5b4e6cd65512a6b5172ad0c0cade67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a2a4e23cbe2d062f3fcfb84c8590190eb72294786a0b8238add858e67a93914`

```dockerfile
```

-	Layers:
	-	`sha256:1f8545bcc66309a59381c88c4c87b0f8352893dbaa167be48947976c1e0cef1d`  
		Last Modified: Tue, 13 Jan 2026 04:35:51 GMT  
		Size: 2.0 MB (2008606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95e6875e372e1d6a9660c08726cb96d08b272e52a2446f275089efccfc3096b3`  
		Last Modified: Tue, 13 Jan 2026 01:25:33 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; 386

```console
$ docker pull memcached@sha256:29540e588e9065db9ecc8865fe74544260980d73786f00dfc4df3f3cee148bd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33661194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66843ae7a7d968c4f056a8e350dd84ff80a06e48b48c298c3427333b7ec259ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:19:43 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 13 Jan 2026 01:19:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:22:40 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 13 Jan 2026 01:22:40 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 13 Jan 2026 01:22:40 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 13 Jan 2026 01:22:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 13 Jan 2026 01:22:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:22:40 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 01:22:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:22:40 GMT
USER memcache
# Tue, 13 Jan 2026 01:22:40 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 13 Jan 2026 01:22:40 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:27bb6d39eda5ced7626db280c3902aacdfade5acd11a16ef9618e3185f69b102`  
		Last Modified: Tue, 13 Jan 2026 00:43:03 GMT  
		Size: 31.3 MB (31288476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cedb4f2840edea9de46e0d955a0512f469211880560a8948f10b54381bcd728`  
		Last Modified: Tue, 13 Jan 2026 01:22:53 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c4b2d1574ee5f238dc6948164abd39ffcc91929b2c464c6b3874dec01fd964`  
		Last Modified: Tue, 13 Jan 2026 01:22:46 GMT  
		Size: 147.6 KB (147554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc1bf5870b84175607f3d012b3cfebc5859869f8125114ea5d6ed1a05f81d2d`  
		Last Modified: Tue, 13 Jan 2026 01:22:53 GMT  
		Size: 2.2 MB (2223652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6434e73ed67e81f1016f27c7cc175290b0ce959d8a1bf5e9b0f3119f161246`  
		Last Modified: Tue, 13 Jan 2026 01:22:53 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abaf99fdf0e2b9620d20088b389b3f18eb67ad356c8c6c7961074e1428b8af0c`  
		Last Modified: Tue, 13 Jan 2026 01:22:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:f64192985f4635b04ce1ab99b3cae89f71d0b11f9670fb6d9c470158e3c5c63e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bb9ce834f23725c4bfc4fb2d6a24a96d3d0bc7685d3a759c0085871f34231e8`

```dockerfile
```

-	Layers:
	-	`sha256:ed9937c762728e5abc93b88bd7932a5762d2bc8e0001e81bb25ef0b27e2bc6ff`  
		Last Modified: Tue, 13 Jan 2026 04:35:56 GMT  
		Size: 2.0 MB (2005447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6358862e12c5c5367efd52bea0b1194e04e76f267084da591229f64ee7482dc3`  
		Last Modified: Tue, 13 Jan 2026 04:35:57 GMT  
		Size: 22.1 KB (22094 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; ppc64le

```console
$ docker pull memcached@sha256:309e0faad388272d7e37d6ee0cb354707d099e3140298105499711823d7a0eea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36161489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6f50ee10fc83da67b90c9bda7499251fa073fea87400d5fb70e31e693d6f902`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:33:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 13 Jan 2026 01:33:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:36:52 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 13 Jan 2026 01:36:52 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 13 Jan 2026 01:36:52 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 13 Jan 2026 01:36:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 13 Jan 2026 01:36:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:36:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 01:36:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:36:53 GMT
USER memcache
# Tue, 13 Jan 2026 01:36:53 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 13 Jan 2026 01:36:53 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9a275bb13cf8b3e9db52a41b6b4ff22ee1ffed00394f6deddd2de45044bd3bae`  
		Last Modified: Tue, 13 Jan 2026 00:57:13 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093e59deb53ff01a892be2a5df928c4b04a289df7f6c135570c11d6a4fdbc53a`  
		Last Modified: Tue, 13 Jan 2026 01:37:16 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4da25c8b13ee47050a38843c1954d2bd7bbdba2666f725aee2f603e03fcb6d`  
		Last Modified: Tue, 13 Jan 2026 01:37:16 GMT  
		Size: 170.4 KB (170427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cab5f6f805c735c0f324c87ff8c66cfab0e35fb691b7761e85bb9a2bbb31cfe`  
		Last Modified: Tue, 13 Jan 2026 01:37:16 GMT  
		Size: 2.4 MB (2393947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3a7dfc8da65bd6101de156530bc2688c5588c718bbc3131ff4594cbefd0e66`  
		Last Modified: Tue, 13 Jan 2026 01:37:09 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06153b2e2bde9b06f1c2719aabb5ff6a6c23056152a024fa2c990d97b4d9c799`  
		Last Modified: Tue, 13 Jan 2026 01:37:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:8dfcc685b38edcaec140b90716d19e543715184f20f7a401d6f734ad8f8cf1dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7442b6e23a86bfe5ee9a534d43f0a55ba9629d3c24128b1b3e2b5121644dcf00`

```dockerfile
```

-	Layers:
	-	`sha256:a4b6027eed506a371ad9a2314b6be299e5c509b4c4be66e5842b29837171b0cf`  
		Last Modified: Tue, 13 Jan 2026 04:36:00 GMT  
		Size: 2.0 MB (2011891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc718b3aa0399c50248bba6165cad8666196a5351b6ed095a8101d2f8a5d37da`  
		Last Modified: Tue, 13 Jan 2026 04:36:01 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; riscv64

```console
$ docker pull memcached@sha256:bce857473a0aeeec89bc5383841d05d99df2b89bba49caf3059874a9442ff224
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30613806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc8f84b5bfd0d6518442de566ffa39b2113651446c246e419f61a8e5fa68e87`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Wed, 14 Jan 2026 06:36:03 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 14 Jan 2026 06:36:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jan 2026 06:49:42 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 14 Jan 2026 06:49:42 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 14 Jan 2026 06:49:42 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 14 Jan 2026 06:49:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 14 Jan 2026 06:49:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 06:49:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 14 Jan 2026 06:49:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 06:49:43 GMT
USER memcache
# Wed, 14 Jan 2026 06:49:43 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 14 Jan 2026 06:49:43 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7c6f79d4d52450222a8a38f8fc98e229a4711a246fc94fdaaab31930d3135d`  
		Last Modified: Wed, 14 Jan 2026 06:50:36 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168d1b37fe07dfb8bef5240057ad6597058647499a9e771eedd2091f2d6b30f0`  
		Last Modified: Wed, 14 Jan 2026 06:50:36 GMT  
		Size: 133.1 KB (133105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a5ebc1ef49cab24f75e0c751a1e0563ee042c246c509279fa38cf3cbf0a3f1`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 2.2 MB (2207499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbc8df7ca1d2f273c3c8fec55b30f17ebc72a45687976efd9c8779a66369d46`  
		Last Modified: Wed, 14 Jan 2026 06:50:36 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4057c9476d421ae1ecae3607afb0db57dbc6eb2bc0aa5e41daed169a70319c1`  
		Last Modified: Wed, 14 Jan 2026 06:50:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:75823016a946bfe52b08e1f80032a64b0202a08f2e30dd8cb7035a01e1244518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b86887925c9eccb39ad75807a81768a06591c668cfd4bf4af00a40b2414f22bc`

```dockerfile
```

-	Layers:
	-	`sha256:0d93e934848935cdae8d83be9ebaff197aaa6e70f5b224c2107461561ea0064d`  
		Last Modified: Wed, 14 Jan 2026 07:34:47 GMT  
		Size: 2.0 MB (2002254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0de5bd0cbff9df1fc11e05bd38936b6915195663b273b5c23840bf5eb9373a8`  
		Last Modified: Wed, 14 Jan 2026 07:34:48 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; s390x

```console
$ docker pull memcached@sha256:46c34c0b238fbae2980413fe2b6590839b6afbc43e0a1e07eb456fc274eaf811
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32272852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8666231b78b1bdfb283fe302437321dedf8ecc2d869ff2acdce9f8461f285519`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 14:13:49 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 13 Jan 2026 14:13:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 14:16:57 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 13 Jan 2026 14:16:57 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 13 Jan 2026 14:16:57 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 13 Jan 2026 14:16:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 13 Jan 2026 14:16:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 14:16:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 14:16:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 14:16:57 GMT
USER memcache
# Tue, 13 Jan 2026 14:16:57 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 13 Jan 2026 14:16:57 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2b46bc94baaae0a37e5e04b1babf7e1f37c4390b83d49c3c6820188deba770e3`  
		Last Modified: Tue, 13 Jan 2026 13:10:43 GMT  
		Size: 29.8 MB (29833411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2727771ad16d920baecb7c96b9b54e67178369b881fc20901d381dfd5f873e27`  
		Last Modified: Tue, 13 Jan 2026 14:17:12 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6b0ec5581f8591522a6327cdcfa4e1197d9ada9fb60840f57b5d3e4dd3304d1`  
		Last Modified: Tue, 13 Jan 2026 14:17:12 GMT  
		Size: 140.6 KB (140562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382a3e1ebed70673a0789fcc2104ab941fe04b9a020339f9286ac85b67ae5ff9`  
		Last Modified: Tue, 13 Jan 2026 14:17:13 GMT  
		Size: 2.3 MB (2297368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85fe5f9afd355e3dd76ce942e1c295e356d96ae3b0e3f8236a0e33c5f75ffe71`  
		Last Modified: Tue, 13 Jan 2026 14:17:08 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4546f3c3457928dc273f98dae7c7ac2f945b203138e964ee72fc92aabcef434`  
		Last Modified: Tue, 13 Jan 2026 14:17:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:d620668087c443f58d215a372a70eb0697c7031777d3537d244fa26e62d3ec3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e48c5956bcfcf63509c135da7076a0f247bc2858c7df68331b5a112e937ff6c`

```dockerfile
```

-	Layers:
	-	`sha256:507d45d8f4547a846c07788edb1628f89b93ac7616169374be23f29601b7be68`  
		Last Modified: Tue, 13 Jan 2026 14:17:08 GMT  
		Size: 2.0 MB (2009727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78fdd8684e48fc4ee1817e00df577a38250864ffbcf34ec341937d525d9dfabd`  
		Last Modified: Tue, 13 Jan 2026 16:34:40 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine`

```console
$ docker pull memcached@sha256:c77536380fd3c7740933767bb5279bd30e31c8d496081e5113a37d9b9eec43cb
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
$ docker pull memcached@sha256:9573a2399011fa86bb7b5d12bdab987d7931c98ddec0ef6802de7eb6d3c3e338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5956768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c79853acc5f24e9c28f15d45cef0aedc114e76bbacf7958eb6f555c22246e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:34 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:29:34 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:32:07 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:32:07 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:32:07 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:32:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:32:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:32:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:32:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:32:07 GMT
USER memcache
# Thu, 18 Dec 2025 00:32:07 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:32:07 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:48:50 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57c33ac8581cd04f31208409f36331e938a78e6ae3a7a3b530fe9dfebe6eb9ad`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583aae99135b9036c602a1c60743fc4fd519f261ac6d48ed60b01e1beb019e7f`  
		Last Modified: Thu, 18 Dec 2025 00:32:12 GMT  
		Size: 106.0 KB (106050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ca22885c42a537f033850e8dff7eaeddbb7514902286739b48c084b55a8d6b`  
		Last Modified: Thu, 18 Dec 2025 00:32:12 GMT  
		Size: 2.0 MB (1989265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d146e2038834770bed57033a6c5d66ead5b731b8b133856dec6726ca21baee9`  
		Last Modified: Thu, 18 Dec 2025 00:32:12 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c66e6c3acbe07806e3e96a97d97a2d4503713c4814d9b24a2f57f2c39200d05`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:cfdf2ea6bf2a04bb7ee1568efe0c8bd38a1f5e644250a9409479cce281891ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de792623281192b3965fdc95f31532c4d166e731f53e202be1e2a224c654633b`

```dockerfile
```

-	Layers:
	-	`sha256:87a0d23eeeda6353dfc603cc4ffee062e5383be07b611754f3a88db3fc644036`  
		Last Modified: Thu, 18 Dec 2025 00:32:12 GMT  
		Size: 94.9 KB (94873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b73cd5efe31baa1fbf0eecea269426edcfc795cbb9b5dd74b523ff51b6f7c9f`  
		Last Modified: Thu, 18 Dec 2025 01:34:48 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:c1a12b64cc8b47f50ea4610d9c1c362da7157b3ba67deac8b4760e6b589cde75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5611647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3591f95cad049a0509bd23a95556f8f848452d2a5491ed00bae293897c7a6b2f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:27:48 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:27:49 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:49:50 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:49:50 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:49:50 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:49:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:49:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:49:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:49:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:49:50 GMT
USER memcache
# Thu, 18 Dec 2025 00:49:50 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:49:50 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf585eb2bfa372c2097b9f7a5214ecb0941a30581b10fb74a26518fcc7addec`  
		Last Modified: Thu, 18 Dec 2025 00:49:55 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01bb148ea8fbe93dd8097d85f9ee3cf547d314e669748b4239c05711b0d5f719`  
		Last Modified: Thu, 18 Dec 2025 00:49:55 GMT  
		Size: 102.7 KB (102652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6549359cda37ac41cf41a5ece5f37f1322a82f6b232f12e446c62840637093e`  
		Last Modified: Thu, 18 Dec 2025 00:50:02 GMT  
		Size: 1.9 MB (1939215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:041e37eaffefcfb0809564ddea591be3cd818de5530e2c853c0bc9a2fa25c116`  
		Last Modified: Thu, 18 Dec 2025 00:49:55 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7907ae218c75b36c9a9002be8554131c271cde78b0280cb7a85029f99ad0bcdc`  
		Last Modified: Thu, 18 Dec 2025 00:50:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:a9c26fc290551b691574e093d3c28f4fe7b558b3f8173b3c99eb8a664c83a8e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ca65d7156e6586d96310ea3162facd9849d5460d2939b461a25247b06a4d59`

```dockerfile
```

-	Layers:
	-	`sha256:d9c217dc241f1175812c47b6489d325a0574c0da554c6f8aa0b86a2d8aff05f9`  
		Last Modified: Thu, 18 Dec 2025 01:34:52 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:cee00a47bf7b8b5899a6cf1f5c692494df31b454f52b81f3c4886905a0c9bdd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5270304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d91d78dbe118f2b7b0d6e850e1115de72c4fe3e30c55a5b53d8a844d14357d16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:30:56 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:30:57 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:33:51 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:33:51 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:33:51 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:33:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:33:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:33:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:33:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:33:51 GMT
USER memcache
# Thu, 18 Dec 2025 00:33:51 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:33:51 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:43 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa22c446792763e48f4680945ccc68d43c7906ef35a92e0b908f57ef53e72f0`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954155078f2265364295ebdf16fb114e991b1938d8a6951fb511163ab3b2b385`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 92.4 KB (92378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a25584b03ac5e45c66c3c616acfd9df1848e5db25219ef20feb2868c30c6332`  
		Last Modified: Thu, 18 Dec 2025 00:33:57 GMT  
		Size: 1.9 MB (1897191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f237be962bb57c3f749904b5925c8e1d7e9013dfac7dd52cc9611ada81858e`  
		Last Modified: Thu, 18 Dec 2025 00:33:57 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b07d9170b246a631c262d9f5d57f49278f7cd4805463b90b14aeca4dc61d93`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:64abe011fed6a9cf7b3290c752c50bffe81bb2e65cf6337e023efda87d49b451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b251b9c15ab7c5742bd3ab725df09f0ecb9f2491f92cf1c825bec598a31f4407`

```dockerfile
```

-	Layers:
	-	`sha256:1882c6d4361100a29fd5ab265587f65fa27b1df15e7f9349b30dac454facf98e`  
		Last Modified: Thu, 18 Dec 2025 00:33:57 GMT  
		Size: 94.3 KB (94291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf0a88ab3838de6beab653497ab62a64cfb87b1dc83c5fa5b6f3907abfd88080`  
		Last Modified: Thu, 18 Dec 2025 01:34:56 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:b6c3042e2bf09ec3d3f054d03b81313e8df717a49371ce916ff743e602796bc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6285509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6691028570bbd843e6da26558c46162b8383212fcaaefcecb2d3f919e3401429`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:18 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:29:19 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:32:06 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:32:06 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:32:06 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:32:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:32:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:32:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:32:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:32:06 GMT
USER memcache
# Thu, 18 Dec 2025 00:32:06 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:32:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb7b8445facedfc145b9478f74880f520776460f153005b7f437ec339aee530`  
		Last Modified: Thu, 18 Dec 2025 00:32:11 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1853c901134389608b6e80aaa3e43cd67a35c71aecfdde4b5b7ed3b989a03c`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 121.9 KB (121860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a01d1ac5ce47f4494363e411e1cd25dea26438213a2d18d6bb104d0974d9a52`  
		Last Modified: Thu, 18 Dec 2025 00:32:11 GMT  
		Size: 2.0 MB (1966561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115624f24ba74d393c2da3d65ed5b35a7afb3fa9ad143d3fb82c64953b3d0401`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87bba524314294ca97195ce65a35ec6d42d3f9f18c9cc0c05c064c9a3cf85c0`  
		Last Modified: Thu, 18 Dec 2025 00:32:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:2feda8921a7d67cd9f2f3d7186ed69ceb0d3c22af7a20bd230664e9bcf39096c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d73c6548a24cc8ce7782d03377e89a4b4b0e4c2a48cd3a03a79193320fc4d834`

```dockerfile
```

-	Layers:
	-	`sha256:984e438122735983bf56bc3d638fb1b0baf8cfb26ce26f71e0a9b847d25f76b5`  
		Last Modified: Thu, 18 Dec 2025 01:34:59 GMT  
		Size: 94.3 KB (94327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d6e8d91ca57b45f0050ec3833a8f09a7ce62f7ba9ec70e1ae12881ad4b2bb6f`  
		Last Modified: Thu, 18 Dec 2025 01:35:00 GMT  
		Size: 20.7 KB (20728 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; 386

```console
$ docker pull memcached@sha256:df1ba8af73cd6e3f8227557b097cd6b128ec0d410a3bbe7a2c282089c5641b41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5740953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78dbfc1f8ea65ad6466795e278180963d4afe98dfbca4a4497bc73c99f07ed4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:13:19 GMT
ADD alpine-minirootfs-3.23.2-x86.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:13:19 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:43 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:29:44 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:32:29 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:32:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:32:29 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:32:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:32:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:32:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:32:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:32:29 GMT
USER memcache
# Thu, 18 Dec 2025 00:32:29 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:32:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c21df6a7383dfce37a4bfe31b291881f55907c419caf5d06cb6d699d290d0718`  
		Last Modified: Thu, 18 Dec 2025 00:13:38 GMT  
		Size: 3.7 MB (3686100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37ec5bf455c1d98d22e6f3dacb5b971dac8ea96d1fe9b9177a07c5277530646`  
		Last Modified: Thu, 18 Dec 2025 00:32:35 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b2862af05c1582c8625c82ea0863dc2b6474e410d3e6a32876c920e0152c73`  
		Last Modified: Thu, 18 Dec 2025 00:32:35 GMT  
		Size: 110.7 KB (110740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30872a43f6c591fd9b979b49b0fb32107b4bfa8c1155657fa255aa199cf0b83b`  
		Last Modified: Thu, 18 Dec 2025 00:32:35 GMT  
		Size: 1.9 MB (1942762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a62c11b4aeceaba2e5e73a1bc29aa8b4fc42ccd0c7e8512cc11b96e48aef2f`  
		Last Modified: Thu, 18 Dec 2025 00:32:41 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f553d362a11992264bf5364cfe13d248403c5baf2ecac784c26f444dbfb90388`  
		Last Modified: Thu, 18 Dec 2025 00:32:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:e3b020c2afd9ae372e234c6ab67456908861fd24200448fd3cf741503a8a6f55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6abfcddfb1575f6cc07e51c6a379141589de7ea8c329a9bc5c1592f3186e6fda`

```dockerfile
```

-	Layers:
	-	`sha256:ff9be8ef1bab92275eb15ae5fd6a05e767abc1fe855455766200b3c0a1866e33`  
		Last Modified: Thu, 18 Dec 2025 01:35:03 GMT  
		Size: 94.8 KB (94828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d7026bdf84e278b6976f0ccab2297ddc0284cf329414f56d12608dbc2acb940`  
		Last Modified: Thu, 18 Dec 2025 00:32:35 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:7292c7b145e08f87f78644bf2c3355fad1d0b4d9366f173ffa0634c3ec93addf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6031729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ae72ba97ecea986f01bda1eb392aee1ded4b5a86b2edcabe92a2034143e155b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:33:41 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:33:42 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:36:14 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:36:14 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:36:14 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:36:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:36:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:36:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:36:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:36:14 GMT
USER memcache
# Thu, 18 Dec 2025 00:36:14 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:36:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c95450233dfe3e06529eb39ca4b46e6ad51ccf338cab64157669ff1fc0a8d72`  
		Last Modified: Thu, 18 Dec 2025 00:36:26 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4079a2d61bafcf146b8f57b35f0e39bf2548e0963be10cff5086f9a56ccdd9d`  
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
		Size: 126.3 KB (126257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f69efa1066815d67cf415d0aac5dcd305032257b6bded5a4c57a7444a1e7fd4`  
		Last Modified: Thu, 18 Dec 2025 00:36:26 GMT  
		Size: 2.1 MB (2076363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357f4165f53a3d4c66ef270bcb5b5283a066af50f79924cccc7c73f6a4f6f4ab`  
		Last Modified: Thu, 18 Dec 2025 00:36:36 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a65ff5cefcbfc874c1cac0857339eaee0b07147dd26b6bfa18c00921b4f30c`  
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:1d06281345f2ac44a607d40d5e87de6abb99bbc6ee82d319e73f3794602d0282
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4867a5aa08041c7e5ec69dfc84214226a7323d1ce703747ae2117675e2f74bcd`

```dockerfile
```

-	Layers:
	-	`sha256:282960f007d3f1f008333191d98a2ded5ff0f83075ace30043349b6c082c18fd`  
		Last Modified: Thu, 18 Dec 2025 01:35:08 GMT  
		Size: 94.3 KB (94280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4755fffd5924e8405adfbed0f328ad9792eff20e2b8ad2025e1f5c85bca88618`  
		Last Modified: Thu, 18 Dec 2025 01:35:09 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:9023f4a863c531a74c6ff8cc3b49c3be80ad1db07cc93fdcbf87c5d8e4cccc72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5768619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2159b7b74e5ffe77e6304def07dec2cfc2bdead26c3012e1e4d39bcd267adfe5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 06:39:34 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 06:39:38 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 06:52:53 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 06:52:53 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 06:52:53 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 06:52:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 06:52:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 06:52:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 06:52:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 06:52:53 GMT
USER memcache
# Thu, 18 Dec 2025 06:52:53 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 06:52:53 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc016d1883c21894ae540944be0270a95cb663037e8592a944bac62e0cc39e7`  
		Last Modified: Thu, 18 Dec 2025 06:53:25 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c580cd51da178bea3e44467f8b445f50ec9272e42e0254d269a9e38204b12dc`  
		Last Modified: Thu, 18 Dec 2025 06:53:25 GMT  
		Size: 108.9 KB (108898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11881c79ebc6a05357f0e2095f00d6d5a8a58bd9f11efeefc80b616d0230ff9`  
		Last Modified: Thu, 18 Dec 2025 06:53:25 GMT  
		Size: 2.1 MB (2074429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735bfa953d895df9672fe0b34207075bd7e686f71104973ad4e02d89db8719a9`  
		Last Modified: Thu, 18 Dec 2025 06:53:25 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b8c865432ff9b07178ba7cb96426e0515b00cc91866fb4dfb8c243e4187172`  
		Last Modified: Thu, 18 Dec 2025 06:53:25 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7cd6a8f4c278ff9062def241e6cdb501032ed72b091608a6da35812eece0954c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38b0c310a1ad4186c4beae0e268b71f1a80ed998cd80ceb81095aa9da7e6b02e`

```dockerfile
```

-	Layers:
	-	`sha256:88642ee1ee3c124ff8f2f640525172206ce9483620a70142ca673e0eca181c4d`  
		Last Modified: Thu, 18 Dec 2025 07:34:34 GMT  
		Size: 94.3 KB (94276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:441bda294fdd657b4574cd5337193125e3d0565433a700136501a858fce53d46`  
		Last Modified: Thu, 18 Dec 2025 07:34:34 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:e011484878fd5d1e2da6de478ac11d01ae80f0bdef1902dcde3ed53728803741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5857090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:689ea71c305b80e206c68a215481290a1378e6375e32ad059455f7d041396aa6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:30:26 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:30:27 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:33:46 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:33:46 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:33:46 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:33:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:33:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:33:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:33:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:33:46 GMT
USER memcache
# Thu, 18 Dec 2025 00:33:46 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:33:46 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4594a6826f7ed03c8c4f9f2aebb9716eb6e16d5b5ab7e1bc247783b503c5b10`  
		Last Modified: Thu, 18 Dec 2025 00:33:55 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f270744f8d8b82bc6657387109b33836a76d6dbf8faa645a997db7ea290cdb`  
		Last Modified: Thu, 18 Dec 2025 00:33:55 GMT  
		Size: 114.3 KB (114299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91f8ee8f36703944a7bdcaf57cc5772fe9f79c74a088c33fa1b6da7de119f93`  
		Last Modified: Thu, 18 Dec 2025 00:33:55 GMT  
		Size: 2.0 MB (2017131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e21d2db88668745770273c7b36d4d2c1e87a80b0118b8d775813860b467384c8`  
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd847159e169b898a67d4454fd5a22406c5ae623b16889d084a1d5f2d46a499`  
		Last Modified: Thu, 18 Dec 2025 00:33:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:33ab737cb23dcde22de59a58e40f1f80d2c5e808ff3036519ae7d9db228fa37d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3562f7fd7806da24b1865c01a2246ac041b5e98d69c10ce6cbbe479f9408f9a1`

```dockerfile
```

-	Layers:
	-	`sha256:d5f43e64a79ee525bd0354a06e3284444fd642bbe6c1a782aa45ec2e20462f1d`  
		Last Modified: Thu, 18 Dec 2025 01:35:19 GMT  
		Size: 94.2 KB (94222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bd2c024010f4f53d350bde9967c349efb3a58a2a812b14e17b29ddbd19eab87`  
		Last Modified: Thu, 18 Dec 2025 01:35:20 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine3.23`

```console
$ docker pull memcached@sha256:c77536380fd3c7740933767bb5279bd30e31c8d496081e5113a37d9b9eec43cb
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
$ docker pull memcached@sha256:9573a2399011fa86bb7b5d12bdab987d7931c98ddec0ef6802de7eb6d3c3e338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5956768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c79853acc5f24e9c28f15d45cef0aedc114e76bbacf7958eb6f555c22246e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:34 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:29:34 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:32:07 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:32:07 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:32:07 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:32:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:32:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:32:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:32:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:32:07 GMT
USER memcache
# Thu, 18 Dec 2025 00:32:07 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:32:07 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:48:50 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57c33ac8581cd04f31208409f36331e938a78e6ae3a7a3b530fe9dfebe6eb9ad`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583aae99135b9036c602a1c60743fc4fd519f261ac6d48ed60b01e1beb019e7f`  
		Last Modified: Thu, 18 Dec 2025 00:32:12 GMT  
		Size: 106.0 KB (106050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ca22885c42a537f033850e8dff7eaeddbb7514902286739b48c084b55a8d6b`  
		Last Modified: Thu, 18 Dec 2025 00:32:12 GMT  
		Size: 2.0 MB (1989265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d146e2038834770bed57033a6c5d66ead5b731b8b133856dec6726ca21baee9`  
		Last Modified: Thu, 18 Dec 2025 00:32:12 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c66e6c3acbe07806e3e96a97d97a2d4503713c4814d9b24a2f57f2c39200d05`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:cfdf2ea6bf2a04bb7ee1568efe0c8bd38a1f5e644250a9409479cce281891ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de792623281192b3965fdc95f31532c4d166e731f53e202be1e2a224c654633b`

```dockerfile
```

-	Layers:
	-	`sha256:87a0d23eeeda6353dfc603cc4ffee062e5383be07b611754f3a88db3fc644036`  
		Last Modified: Thu, 18 Dec 2025 00:32:12 GMT  
		Size: 94.9 KB (94873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b73cd5efe31baa1fbf0eecea269426edcfc795cbb9b5dd74b523ff51b6f7c9f`  
		Last Modified: Thu, 18 Dec 2025 01:34:48 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; arm variant v6

```console
$ docker pull memcached@sha256:c1a12b64cc8b47f50ea4610d9c1c362da7157b3ba67deac8b4760e6b589cde75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5611647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3591f95cad049a0509bd23a95556f8f848452d2a5491ed00bae293897c7a6b2f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:27:48 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:27:49 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:49:50 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:49:50 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:49:50 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:49:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:49:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:49:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:49:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:49:50 GMT
USER memcache
# Thu, 18 Dec 2025 00:49:50 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:49:50 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf585eb2bfa372c2097b9f7a5214ecb0941a30581b10fb74a26518fcc7addec`  
		Last Modified: Thu, 18 Dec 2025 00:49:55 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01bb148ea8fbe93dd8097d85f9ee3cf547d314e669748b4239c05711b0d5f719`  
		Last Modified: Thu, 18 Dec 2025 00:49:55 GMT  
		Size: 102.7 KB (102652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6549359cda37ac41cf41a5ece5f37f1322a82f6b232f12e446c62840637093e`  
		Last Modified: Thu, 18 Dec 2025 00:50:02 GMT  
		Size: 1.9 MB (1939215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:041e37eaffefcfb0809564ddea591be3cd818de5530e2c853c0bc9a2fa25c116`  
		Last Modified: Thu, 18 Dec 2025 00:49:55 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7907ae218c75b36c9a9002be8554131c271cde78b0280cb7a85029f99ad0bcdc`  
		Last Modified: Thu, 18 Dec 2025 00:50:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:a9c26fc290551b691574e093d3c28f4fe7b558b3f8173b3c99eb8a664c83a8e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ca65d7156e6586d96310ea3162facd9849d5460d2939b461a25247b06a4d59`

```dockerfile
```

-	Layers:
	-	`sha256:d9c217dc241f1175812c47b6489d325a0574c0da554c6f8aa0b86a2d8aff05f9`  
		Last Modified: Thu, 18 Dec 2025 01:34:52 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; arm variant v7

```console
$ docker pull memcached@sha256:cee00a47bf7b8b5899a6cf1f5c692494df31b454f52b81f3c4886905a0c9bdd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5270304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d91d78dbe118f2b7b0d6e850e1115de72c4fe3e30c55a5b53d8a844d14357d16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:30:56 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:30:57 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:33:51 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:33:51 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:33:51 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:33:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:33:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:33:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:33:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:33:51 GMT
USER memcache
# Thu, 18 Dec 2025 00:33:51 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:33:51 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:43 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa22c446792763e48f4680945ccc68d43c7906ef35a92e0b908f57ef53e72f0`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954155078f2265364295ebdf16fb114e991b1938d8a6951fb511163ab3b2b385`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 92.4 KB (92378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a25584b03ac5e45c66c3c616acfd9df1848e5db25219ef20feb2868c30c6332`  
		Last Modified: Thu, 18 Dec 2025 00:33:57 GMT  
		Size: 1.9 MB (1897191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f237be962bb57c3f749904b5925c8e1d7e9013dfac7dd52cc9611ada81858e`  
		Last Modified: Thu, 18 Dec 2025 00:33:57 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b07d9170b246a631c262d9f5d57f49278f7cd4805463b90b14aeca4dc61d93`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:64abe011fed6a9cf7b3290c752c50bffe81bb2e65cf6337e023efda87d49b451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b251b9c15ab7c5742bd3ab725df09f0ecb9f2491f92cf1c825bec598a31f4407`

```dockerfile
```

-	Layers:
	-	`sha256:1882c6d4361100a29fd5ab265587f65fa27b1df15e7f9349b30dac454facf98e`  
		Last Modified: Thu, 18 Dec 2025 00:33:57 GMT  
		Size: 94.3 KB (94291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf0a88ab3838de6beab653497ab62a64cfb87b1dc83c5fa5b6f3907abfd88080`  
		Last Modified: Thu, 18 Dec 2025 01:34:56 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:b6c3042e2bf09ec3d3f054d03b81313e8df717a49371ce916ff743e602796bc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6285509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6691028570bbd843e6da26558c46162b8383212fcaaefcecb2d3f919e3401429`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:18 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:29:19 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:32:06 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:32:06 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:32:06 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:32:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:32:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:32:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:32:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:32:06 GMT
USER memcache
# Thu, 18 Dec 2025 00:32:06 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:32:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb7b8445facedfc145b9478f74880f520776460f153005b7f437ec339aee530`  
		Last Modified: Thu, 18 Dec 2025 00:32:11 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1853c901134389608b6e80aaa3e43cd67a35c71aecfdde4b5b7ed3b989a03c`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 121.9 KB (121860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a01d1ac5ce47f4494363e411e1cd25dea26438213a2d18d6bb104d0974d9a52`  
		Last Modified: Thu, 18 Dec 2025 00:32:11 GMT  
		Size: 2.0 MB (1966561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115624f24ba74d393c2da3d65ed5b35a7afb3fa9ad143d3fb82c64953b3d0401`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87bba524314294ca97195ce65a35ec6d42d3f9f18c9cc0c05c064c9a3cf85c0`  
		Last Modified: Thu, 18 Dec 2025 00:32:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:2feda8921a7d67cd9f2f3d7186ed69ceb0d3c22af7a20bd230664e9bcf39096c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d73c6548a24cc8ce7782d03377e89a4b4b0e4c2a48cd3a03a79193320fc4d834`

```dockerfile
```

-	Layers:
	-	`sha256:984e438122735983bf56bc3d638fb1b0baf8cfb26ce26f71e0a9b847d25f76b5`  
		Last Modified: Thu, 18 Dec 2025 01:34:59 GMT  
		Size: 94.3 KB (94327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d6e8d91ca57b45f0050ec3833a8f09a7ce62f7ba9ec70e1ae12881ad4b2bb6f`  
		Last Modified: Thu, 18 Dec 2025 01:35:00 GMT  
		Size: 20.7 KB (20728 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; 386

```console
$ docker pull memcached@sha256:df1ba8af73cd6e3f8227557b097cd6b128ec0d410a3bbe7a2c282089c5641b41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5740953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78dbfc1f8ea65ad6466795e278180963d4afe98dfbca4a4497bc73c99f07ed4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:13:19 GMT
ADD alpine-minirootfs-3.23.2-x86.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:13:19 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:43 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:29:44 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:32:29 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:32:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:32:29 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:32:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:32:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:32:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:32:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:32:29 GMT
USER memcache
# Thu, 18 Dec 2025 00:32:29 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:32:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c21df6a7383dfce37a4bfe31b291881f55907c419caf5d06cb6d699d290d0718`  
		Last Modified: Thu, 18 Dec 2025 00:13:38 GMT  
		Size: 3.7 MB (3686100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37ec5bf455c1d98d22e6f3dacb5b971dac8ea96d1fe9b9177a07c5277530646`  
		Last Modified: Thu, 18 Dec 2025 00:32:35 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b2862af05c1582c8625c82ea0863dc2b6474e410d3e6a32876c920e0152c73`  
		Last Modified: Thu, 18 Dec 2025 00:32:35 GMT  
		Size: 110.7 KB (110740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30872a43f6c591fd9b979b49b0fb32107b4bfa8c1155657fa255aa199cf0b83b`  
		Last Modified: Thu, 18 Dec 2025 00:32:35 GMT  
		Size: 1.9 MB (1942762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a62c11b4aeceaba2e5e73a1bc29aa8b4fc42ccd0c7e8512cc11b96e48aef2f`  
		Last Modified: Thu, 18 Dec 2025 00:32:41 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f553d362a11992264bf5364cfe13d248403c5baf2ecac784c26f444dbfb90388`  
		Last Modified: Thu, 18 Dec 2025 00:32:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:e3b020c2afd9ae372e234c6ab67456908861fd24200448fd3cf741503a8a6f55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6abfcddfb1575f6cc07e51c6a379141589de7ea8c329a9bc5c1592f3186e6fda`

```dockerfile
```

-	Layers:
	-	`sha256:ff9be8ef1bab92275eb15ae5fd6a05e767abc1fe855455766200b3c0a1866e33`  
		Last Modified: Thu, 18 Dec 2025 01:35:03 GMT  
		Size: 94.8 KB (94828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d7026bdf84e278b6976f0ccab2297ddc0284cf329414f56d12608dbc2acb940`  
		Last Modified: Thu, 18 Dec 2025 00:32:35 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; ppc64le

```console
$ docker pull memcached@sha256:7292c7b145e08f87f78644bf2c3355fad1d0b4d9366f173ffa0634c3ec93addf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6031729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ae72ba97ecea986f01bda1eb392aee1ded4b5a86b2edcabe92a2034143e155b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:33:41 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:33:42 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:36:14 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:36:14 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:36:14 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:36:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:36:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:36:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:36:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:36:14 GMT
USER memcache
# Thu, 18 Dec 2025 00:36:14 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:36:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c95450233dfe3e06529eb39ca4b46e6ad51ccf338cab64157669ff1fc0a8d72`  
		Last Modified: Thu, 18 Dec 2025 00:36:26 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4079a2d61bafcf146b8f57b35f0e39bf2548e0963be10cff5086f9a56ccdd9d`  
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
		Size: 126.3 KB (126257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f69efa1066815d67cf415d0aac5dcd305032257b6bded5a4c57a7444a1e7fd4`  
		Last Modified: Thu, 18 Dec 2025 00:36:26 GMT  
		Size: 2.1 MB (2076363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357f4165f53a3d4c66ef270bcb5b5283a066af50f79924cccc7c73f6a4f6f4ab`  
		Last Modified: Thu, 18 Dec 2025 00:36:36 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a65ff5cefcbfc874c1cac0857339eaee0b07147dd26b6bfa18c00921b4f30c`  
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:1d06281345f2ac44a607d40d5e87de6abb99bbc6ee82d319e73f3794602d0282
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4867a5aa08041c7e5ec69dfc84214226a7323d1ce703747ae2117675e2f74bcd`

```dockerfile
```

-	Layers:
	-	`sha256:282960f007d3f1f008333191d98a2ded5ff0f83075ace30043349b6c082c18fd`  
		Last Modified: Thu, 18 Dec 2025 01:35:08 GMT  
		Size: 94.3 KB (94280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4755fffd5924e8405adfbed0f328ad9792eff20e2b8ad2025e1f5c85bca88618`  
		Last Modified: Thu, 18 Dec 2025 01:35:09 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; riscv64

```console
$ docker pull memcached@sha256:9023f4a863c531a74c6ff8cc3b49c3be80ad1db07cc93fdcbf87c5d8e4cccc72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5768619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2159b7b74e5ffe77e6304def07dec2cfc2bdead26c3012e1e4d39bcd267adfe5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 06:39:34 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 06:39:38 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 06:52:53 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 06:52:53 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 06:52:53 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 06:52:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 06:52:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 06:52:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 06:52:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 06:52:53 GMT
USER memcache
# Thu, 18 Dec 2025 06:52:53 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 06:52:53 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc016d1883c21894ae540944be0270a95cb663037e8592a944bac62e0cc39e7`  
		Last Modified: Thu, 18 Dec 2025 06:53:25 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c580cd51da178bea3e44467f8b445f50ec9272e42e0254d269a9e38204b12dc`  
		Last Modified: Thu, 18 Dec 2025 06:53:25 GMT  
		Size: 108.9 KB (108898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11881c79ebc6a05357f0e2095f00d6d5a8a58bd9f11efeefc80b616d0230ff9`  
		Last Modified: Thu, 18 Dec 2025 06:53:25 GMT  
		Size: 2.1 MB (2074429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735bfa953d895df9672fe0b34207075bd7e686f71104973ad4e02d89db8719a9`  
		Last Modified: Thu, 18 Dec 2025 06:53:25 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b8c865432ff9b07178ba7cb96426e0515b00cc91866fb4dfb8c243e4187172`  
		Last Modified: Thu, 18 Dec 2025 06:53:25 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:7cd6a8f4c278ff9062def241e6cdb501032ed72b091608a6da35812eece0954c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38b0c310a1ad4186c4beae0e268b71f1a80ed998cd80ceb81095aa9da7e6b02e`

```dockerfile
```

-	Layers:
	-	`sha256:88642ee1ee3c124ff8f2f640525172206ce9483620a70142ca673e0eca181c4d`  
		Last Modified: Thu, 18 Dec 2025 07:34:34 GMT  
		Size: 94.3 KB (94276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:441bda294fdd657b4574cd5337193125e3d0565433a700136501a858fce53d46`  
		Last Modified: Thu, 18 Dec 2025 07:34:34 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; s390x

```console
$ docker pull memcached@sha256:e011484878fd5d1e2da6de478ac11d01ae80f0bdef1902dcde3ed53728803741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5857090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:689ea71c305b80e206c68a215481290a1378e6375e32ad059455f7d041396aa6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:30:26 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:30:27 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:33:46 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:33:46 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:33:46 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:33:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:33:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:33:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:33:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:33:46 GMT
USER memcache
# Thu, 18 Dec 2025 00:33:46 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:33:46 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4594a6826f7ed03c8c4f9f2aebb9716eb6e16d5b5ab7e1bc247783b503c5b10`  
		Last Modified: Thu, 18 Dec 2025 00:33:55 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f270744f8d8b82bc6657387109b33836a76d6dbf8faa645a997db7ea290cdb`  
		Last Modified: Thu, 18 Dec 2025 00:33:55 GMT  
		Size: 114.3 KB (114299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91f8ee8f36703944a7bdcaf57cc5772fe9f79c74a088c33fa1b6da7de119f93`  
		Last Modified: Thu, 18 Dec 2025 00:33:55 GMT  
		Size: 2.0 MB (2017131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e21d2db88668745770273c7b36d4d2c1e87a80b0118b8d775813860b467384c8`  
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd847159e169b898a67d4454fd5a22406c5ae623b16889d084a1d5f2d46a499`  
		Last Modified: Thu, 18 Dec 2025 00:33:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:33ab737cb23dcde22de59a58e40f1f80d2c5e808ff3036519ae7d9db228fa37d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3562f7fd7806da24b1865c01a2246ac041b5e98d69c10ce6cbbe479f9408f9a1`

```dockerfile
```

-	Layers:
	-	`sha256:d5f43e64a79ee525bd0354a06e3284444fd642bbe6c1a782aa45ec2e20462f1d`  
		Last Modified: Thu, 18 Dec 2025 01:35:19 GMT  
		Size: 94.2 KB (94222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bd2c024010f4f53d350bde9967c349efb3a58a2a812b14e17b29ddbd19eab87`  
		Last Modified: Thu, 18 Dec 2025 01:35:20 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-trixie`

```console
$ docker pull memcached@sha256:e4e5eca37e4334f9579f10fcdd88a58c4eb9d0a8eacedde6ec49d4ea4391637a
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
$ docker pull memcached@sha256:1613c35e314db0c64d8b5679786ad99ced10069c3f9778d40b6c522ff3c04218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32190619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a38251b773d15614da3036dd0d756bbf4a7d16d27fe1c52023517a419372b245`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:22:30 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 13 Jan 2026 01:22:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:25:18 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 13 Jan 2026 01:25:18 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 13 Jan 2026 01:25:18 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 13 Jan 2026 01:25:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 13 Jan 2026 01:25:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:25:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 01:25:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:25:18 GMT
USER memcache
# Tue, 13 Jan 2026 01:25:18 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 13 Jan 2026 01:25:18 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:34 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b6e737e1a3eed198cc17e2b92231ab084bcf55ba90a36136e7a2f4fd04a95b`  
		Last Modified: Tue, 13 Jan 2026 01:25:30 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16835fec399670b74d32630a7368a65ca2a3c32d8b7a690d33bebc7b9e9458d`  
		Last Modified: Tue, 13 Jan 2026 01:25:30 GMT  
		Size: 136.7 KB (136737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c848acbad27f1c9d2fd95e0facabbb28d5d8be19e5fa5912e5474c1301522523`  
		Last Modified: Tue, 13 Jan 2026 01:25:25 GMT  
		Size: 2.3 MB (2278686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9529916038b7840d3177e93bf04b78390bb91bca78623bd9c0769f9e2a965079`  
		Last Modified: Tue, 13 Jan 2026 01:25:25 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24239fc168f5eb73ae9964e2cdcb3c3b878ae79835c6b94585cb648fd50479d`  
		Last Modified: Tue, 13 Jan 2026 01:25:26 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:0d72ad7b507d17cffe5dbec1ddecf1c254c3a85d2b605fa0ddbc9913ba4fc678
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe582f0cad77d385a3debb0f2acf0c96b7b85c6a7d2c95fcc54f938d63635c9`

```dockerfile
```

-	Layers:
	-	`sha256:7d598d8c3b4cd06481693da06e86554144167d205cc60f43382fafba94dd4592`  
		Last Modified: Tue, 13 Jan 2026 04:35:37 GMT  
		Size: 2.0 MB (2008290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dd2469227ab0e75822eb9d56a5d7c05f52a445840f65934e010a2562e509718`  
		Last Modified: Tue, 13 Jan 2026 01:25:24 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; arm variant v5

```console
$ docker pull memcached@sha256:efa6728c05b024b605597e5025f04155aab614b52f56b1b31a4c70a23f909e07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30298859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14119dc07998a4322ac912beaaf4e6ad16e5487f2243c332fdaad86bdce6f55e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:19:21 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 13 Jan 2026 01:19:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:22:43 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 13 Jan 2026 01:22:43 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 13 Jan 2026 01:22:43 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 13 Jan 2026 01:22:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 13 Jan 2026 01:22:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:22:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 01:22:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:22:43 GMT
USER memcache
# Tue, 13 Jan 2026 01:22:43 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 13 Jan 2026 01:22:43 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c113d410d30c2c035a105b56d3937958c81fbe2530f44add3bae903be6864324`  
		Last Modified: Tue, 13 Jan 2026 00:42:30 GMT  
		Size: 27.9 MB (27942724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96776850dc1206c3fd163b84cea19599306159eb0d020b4241d0172240f88d13`  
		Last Modified: Tue, 13 Jan 2026 01:22:55 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3697c7c790d9c4caaa904abdaf809dcdee3f0b518fc5ad82d2e21dd7fe24f64d`  
		Last Modified: Tue, 13 Jan 2026 01:22:55 GMT  
		Size: 144.2 KB (144212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a247339c7ec57a491c3ffe43531dbfaa132f3ff16a481fc41cbb9e3e3ad6476`  
		Last Modified: Tue, 13 Jan 2026 01:22:50 GMT  
		Size: 2.2 MB (2210412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2dcebe3ab2a9945cdea142301e4a64eebbc59c948a54385dbfca4afd561b508`  
		Last Modified: Tue, 13 Jan 2026 01:22:55 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb8ef5ecbc44efd5280f9cf15687dfd80a34fa2966ad039238647177f75dc6c`  
		Last Modified: Tue, 13 Jan 2026 01:22:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:190bb1ecd7376720e541621921c2d4931a9d0f85a047255ba2b56afa3a504212
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9736e9545a46e4ef65dcb5238691292d27fac4dccb330354ce59ac93ae6994b5`

```dockerfile
```

-	Layers:
	-	`sha256:4f5461bf596f750b56b3f10e315936c2326b2c32901d28cdf22db97072bba685`  
		Last Modified: Tue, 13 Jan 2026 01:22:50 GMT  
		Size: 2.0 MB (2011293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8657d28d0436d39193457fb90119ea6e4ddb566df2a83fd1aa9df75651731188`  
		Last Modified: Tue, 13 Jan 2026 04:35:43 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; arm variant v7

```console
$ docker pull memcached@sha256:9c322c838b4648fa30e742e53ed6647a31383760fb73fa82de32b4b6dc88c494
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28509532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6e130248535c57fccff4d89a9d442e31cabd471e41c9eed52e5207a54f9f944`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:25:47 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 13 Jan 2026 01:25:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:28:55 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 13 Jan 2026 01:28:55 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 13 Jan 2026 01:28:55 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 13 Jan 2026 01:28:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 13 Jan 2026 01:28:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:28:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 01:28:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:28:55 GMT
USER memcache
# Tue, 13 Jan 2026 01:28:55 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 13 Jan 2026 01:28:55 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029a2cbe46c1e12ab6d47a63f40fb29056b6c6277c7822085ed0fe62e0a1791d`  
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c7827f95482598f1bd32dd8cbe071ad009795fa108661234eeb872d1a1e8bd`  
		Last Modified: Tue, 13 Jan 2026 01:29:07 GMT  
		Size: 135.4 KB (135398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9371e974781bd91adc657086f00cd7d91b5530ca9da37597c347dd7d4eaff0`  
		Last Modified: Tue, 13 Jan 2026 01:29:07 GMT  
		Size: 2.2 MB (2164040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c2e0f64c0afa16b5e214ae208c8c81e8c78c79ddd90f54983a93c7297395f6b`  
		Last Modified: Tue, 13 Jan 2026 01:29:07 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92151d443057f88ed7f60405440b698ff9e6abe1a2ca1c91a0c7e7626339ad2`  
		Last Modified: Tue, 13 Jan 2026 01:29:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:12cc31a1ce56d2c6dd1c0dcfd4ef1fe74484985d010594950c086c0f4431559b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b2d844d5393973080c37fde0b92cd48bd1a64e03973290631be5486d814de7e`

```dockerfile
```

-	Layers:
	-	`sha256:99fc27444c1ccdd6cbd08a33aac22e9e85f55958bda7b6216bdea08eae374cff`  
		Last Modified: Tue, 13 Jan 2026 04:35:47 GMT  
		Size: 2.0 MB (2009750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e76d5584f581b7668c61a661da2858bc1d5e11b31e3629e0d2b3af52d9c22ed8`  
		Last Modified: Tue, 13 Jan 2026 04:35:47 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:2ed537fa0376a3eb0864d6a3b51ea7da59b9ff4bb3270189a8a5082f02f811e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32550406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf26d75d787aabbd202c97db1079b96e45105d3ca509a1001ab973cb473cae8c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:22:29 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 13 Jan 2026 01:22:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:25:26 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 13 Jan 2026 01:25:26 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 13 Jan 2026 01:25:26 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 13 Jan 2026 01:25:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 13 Jan 2026 01:25:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:25:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 01:25:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:25:27 GMT
USER memcache
# Tue, 13 Jan 2026 01:25:27 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 13 Jan 2026 01:25:27 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78edb6b991369235f90958a936afc89dc37b82439c632988ed143b5bd76deadb`  
		Last Modified: Tue, 13 Jan 2026 01:25:40 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e1afbb765f6cc3923e864d44fb6cd6c9167b884e596b09bd37c7c276f65a2b`  
		Last Modified: Tue, 13 Jan 2026 01:25:40 GMT  
		Size: 153.5 KB (153512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff9edc68fe57c233001afd442eb6c248bf070d32fbb412a8bfeef6f9a6217f5`  
		Last Modified: Tue, 13 Jan 2026 01:25:40 GMT  
		Size: 2.3 MB (2261341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c4648fbc4a4189184946895d1041e0eee2c5d40fd70638a553bedb0cbf5cf8`  
		Last Modified: Tue, 13 Jan 2026 01:25:40 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26bd1b32b048e73091ddf6e6762e368d4bb6ef2cc7d3aa43467749b36fe08e38`  
		Last Modified: Tue, 13 Jan 2026 01:25:40 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:72333c6222fb20b5a9f9f92b8d56c47ebb5b4e6cd65512a6b5172ad0c0cade67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a2a4e23cbe2d062f3fcfb84c8590190eb72294786a0b8238add858e67a93914`

```dockerfile
```

-	Layers:
	-	`sha256:1f8545bcc66309a59381c88c4c87b0f8352893dbaa167be48947976c1e0cef1d`  
		Last Modified: Tue, 13 Jan 2026 04:35:51 GMT  
		Size: 2.0 MB (2008606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95e6875e372e1d6a9660c08726cb96d08b272e52a2446f275089efccfc3096b3`  
		Last Modified: Tue, 13 Jan 2026 01:25:33 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; 386

```console
$ docker pull memcached@sha256:29540e588e9065db9ecc8865fe74544260980d73786f00dfc4df3f3cee148bd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33661194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66843ae7a7d968c4f056a8e350dd84ff80a06e48b48c298c3427333b7ec259ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:19:43 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 13 Jan 2026 01:19:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:22:40 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 13 Jan 2026 01:22:40 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 13 Jan 2026 01:22:40 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 13 Jan 2026 01:22:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 13 Jan 2026 01:22:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:22:40 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 01:22:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:22:40 GMT
USER memcache
# Tue, 13 Jan 2026 01:22:40 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 13 Jan 2026 01:22:40 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:27bb6d39eda5ced7626db280c3902aacdfade5acd11a16ef9618e3185f69b102`  
		Last Modified: Tue, 13 Jan 2026 00:43:03 GMT  
		Size: 31.3 MB (31288476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cedb4f2840edea9de46e0d955a0512f469211880560a8948f10b54381bcd728`  
		Last Modified: Tue, 13 Jan 2026 01:22:53 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c4b2d1574ee5f238dc6948164abd39ffcc91929b2c464c6b3874dec01fd964`  
		Last Modified: Tue, 13 Jan 2026 01:22:46 GMT  
		Size: 147.6 KB (147554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc1bf5870b84175607f3d012b3cfebc5859869f8125114ea5d6ed1a05f81d2d`  
		Last Modified: Tue, 13 Jan 2026 01:22:53 GMT  
		Size: 2.2 MB (2223652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6434e73ed67e81f1016f27c7cc175290b0ce959d8a1bf5e9b0f3119f161246`  
		Last Modified: Tue, 13 Jan 2026 01:22:53 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abaf99fdf0e2b9620d20088b389b3f18eb67ad356c8c6c7961074e1428b8af0c`  
		Last Modified: Tue, 13 Jan 2026 01:22:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:f64192985f4635b04ce1ab99b3cae89f71d0b11f9670fb6d9c470158e3c5c63e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bb9ce834f23725c4bfc4fb2d6a24a96d3d0bc7685d3a759c0085871f34231e8`

```dockerfile
```

-	Layers:
	-	`sha256:ed9937c762728e5abc93b88bd7932a5762d2bc8e0001e81bb25ef0b27e2bc6ff`  
		Last Modified: Tue, 13 Jan 2026 04:35:56 GMT  
		Size: 2.0 MB (2005447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6358862e12c5c5367efd52bea0b1194e04e76f267084da591229f64ee7482dc3`  
		Last Modified: Tue, 13 Jan 2026 04:35:57 GMT  
		Size: 22.1 KB (22094 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; ppc64le

```console
$ docker pull memcached@sha256:309e0faad388272d7e37d6ee0cb354707d099e3140298105499711823d7a0eea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36161489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6f50ee10fc83da67b90c9bda7499251fa073fea87400d5fb70e31e693d6f902`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:33:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 13 Jan 2026 01:33:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:36:52 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 13 Jan 2026 01:36:52 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 13 Jan 2026 01:36:52 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 13 Jan 2026 01:36:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 13 Jan 2026 01:36:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:36:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 01:36:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:36:53 GMT
USER memcache
# Tue, 13 Jan 2026 01:36:53 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 13 Jan 2026 01:36:53 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9a275bb13cf8b3e9db52a41b6b4ff22ee1ffed00394f6deddd2de45044bd3bae`  
		Last Modified: Tue, 13 Jan 2026 00:57:13 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093e59deb53ff01a892be2a5df928c4b04a289df7f6c135570c11d6a4fdbc53a`  
		Last Modified: Tue, 13 Jan 2026 01:37:16 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4da25c8b13ee47050a38843c1954d2bd7bbdba2666f725aee2f603e03fcb6d`  
		Last Modified: Tue, 13 Jan 2026 01:37:16 GMT  
		Size: 170.4 KB (170427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cab5f6f805c735c0f324c87ff8c66cfab0e35fb691b7761e85bb9a2bbb31cfe`  
		Last Modified: Tue, 13 Jan 2026 01:37:16 GMT  
		Size: 2.4 MB (2393947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3a7dfc8da65bd6101de156530bc2688c5588c718bbc3131ff4594cbefd0e66`  
		Last Modified: Tue, 13 Jan 2026 01:37:09 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06153b2e2bde9b06f1c2719aabb5ff6a6c23056152a024fa2c990d97b4d9c799`  
		Last Modified: Tue, 13 Jan 2026 01:37:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:8dfcc685b38edcaec140b90716d19e543715184f20f7a401d6f734ad8f8cf1dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7442b6e23a86bfe5ee9a534d43f0a55ba9629d3c24128b1b3e2b5121644dcf00`

```dockerfile
```

-	Layers:
	-	`sha256:a4b6027eed506a371ad9a2314b6be299e5c509b4c4be66e5842b29837171b0cf`  
		Last Modified: Tue, 13 Jan 2026 04:36:00 GMT  
		Size: 2.0 MB (2011891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc718b3aa0399c50248bba6165cad8666196a5351b6ed095a8101d2f8a5d37da`  
		Last Modified: Tue, 13 Jan 2026 04:36:01 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; riscv64

```console
$ docker pull memcached@sha256:bce857473a0aeeec89bc5383841d05d99df2b89bba49caf3059874a9442ff224
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30613806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc8f84b5bfd0d6518442de566ffa39b2113651446c246e419f61a8e5fa68e87`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Wed, 14 Jan 2026 06:36:03 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 14 Jan 2026 06:36:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jan 2026 06:49:42 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 14 Jan 2026 06:49:42 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 14 Jan 2026 06:49:42 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 14 Jan 2026 06:49:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 14 Jan 2026 06:49:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 06:49:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 14 Jan 2026 06:49:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 06:49:43 GMT
USER memcache
# Wed, 14 Jan 2026 06:49:43 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 14 Jan 2026 06:49:43 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7c6f79d4d52450222a8a38f8fc98e229a4711a246fc94fdaaab31930d3135d`  
		Last Modified: Wed, 14 Jan 2026 06:50:36 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168d1b37fe07dfb8bef5240057ad6597058647499a9e771eedd2091f2d6b30f0`  
		Last Modified: Wed, 14 Jan 2026 06:50:36 GMT  
		Size: 133.1 KB (133105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a5ebc1ef49cab24f75e0c751a1e0563ee042c246c509279fa38cf3cbf0a3f1`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 2.2 MB (2207499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbc8df7ca1d2f273c3c8fec55b30f17ebc72a45687976efd9c8779a66369d46`  
		Last Modified: Wed, 14 Jan 2026 06:50:36 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4057c9476d421ae1ecae3607afb0db57dbc6eb2bc0aa5e41daed169a70319c1`  
		Last Modified: Wed, 14 Jan 2026 06:50:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:75823016a946bfe52b08e1f80032a64b0202a08f2e30dd8cb7035a01e1244518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b86887925c9eccb39ad75807a81768a06591c668cfd4bf4af00a40b2414f22bc`

```dockerfile
```

-	Layers:
	-	`sha256:0d93e934848935cdae8d83be9ebaff197aaa6e70f5b224c2107461561ea0064d`  
		Last Modified: Wed, 14 Jan 2026 07:34:47 GMT  
		Size: 2.0 MB (2002254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0de5bd0cbff9df1fc11e05bd38936b6915195663b273b5c23840bf5eb9373a8`  
		Last Modified: Wed, 14 Jan 2026 07:34:48 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; s390x

```console
$ docker pull memcached@sha256:46c34c0b238fbae2980413fe2b6590839b6afbc43e0a1e07eb456fc274eaf811
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32272852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8666231b78b1bdfb283fe302437321dedf8ecc2d869ff2acdce9f8461f285519`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 14:13:49 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 13 Jan 2026 14:13:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 14:16:57 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 13 Jan 2026 14:16:57 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 13 Jan 2026 14:16:57 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 13 Jan 2026 14:16:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 13 Jan 2026 14:16:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 14:16:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 14:16:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 14:16:57 GMT
USER memcache
# Tue, 13 Jan 2026 14:16:57 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 13 Jan 2026 14:16:57 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2b46bc94baaae0a37e5e04b1babf7e1f37c4390b83d49c3c6820188deba770e3`  
		Last Modified: Tue, 13 Jan 2026 13:10:43 GMT  
		Size: 29.8 MB (29833411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2727771ad16d920baecb7c96b9b54e67178369b881fc20901d381dfd5f873e27`  
		Last Modified: Tue, 13 Jan 2026 14:17:12 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6b0ec5581f8591522a6327cdcfa4e1197d9ada9fb60840f57b5d3e4dd3304d1`  
		Last Modified: Tue, 13 Jan 2026 14:17:12 GMT  
		Size: 140.6 KB (140562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382a3e1ebed70673a0789fcc2104ab941fe04b9a020339f9286ac85b67ae5ff9`  
		Last Modified: Tue, 13 Jan 2026 14:17:13 GMT  
		Size: 2.3 MB (2297368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85fe5f9afd355e3dd76ce942e1c295e356d96ae3b0e3f8236a0e33c5f75ffe71`  
		Last Modified: Tue, 13 Jan 2026 14:17:08 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4546f3c3457928dc273f98dae7c7ac2f945b203138e964ee72fc92aabcef434`  
		Last Modified: Tue, 13 Jan 2026 14:17:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:d620668087c443f58d215a372a70eb0697c7031777d3537d244fa26e62d3ec3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e48c5956bcfcf63509c135da7076a0f247bc2858c7df68331b5a112e937ff6c`

```dockerfile
```

-	Layers:
	-	`sha256:507d45d8f4547a846c07788edb1628f89b93ac7616169374be23f29601b7be68`  
		Last Modified: Tue, 13 Jan 2026 14:17:08 GMT  
		Size: 2.0 MB (2009727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78fdd8684e48fc4ee1817e00df577a38250864ffbcf34ec341937d525d9dfabd`  
		Last Modified: Tue, 13 Jan 2026 16:34:40 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6`

```console
$ docker pull memcached@sha256:e4e5eca37e4334f9579f10fcdd88a58c4eb9d0a8eacedde6ec49d4ea4391637a
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
$ docker pull memcached@sha256:1613c35e314db0c64d8b5679786ad99ced10069c3f9778d40b6c522ff3c04218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32190619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a38251b773d15614da3036dd0d756bbf4a7d16d27fe1c52023517a419372b245`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:22:30 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 13 Jan 2026 01:22:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:25:18 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 13 Jan 2026 01:25:18 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 13 Jan 2026 01:25:18 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 13 Jan 2026 01:25:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 13 Jan 2026 01:25:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:25:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 01:25:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:25:18 GMT
USER memcache
# Tue, 13 Jan 2026 01:25:18 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 13 Jan 2026 01:25:18 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:34 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b6e737e1a3eed198cc17e2b92231ab084bcf55ba90a36136e7a2f4fd04a95b`  
		Last Modified: Tue, 13 Jan 2026 01:25:30 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16835fec399670b74d32630a7368a65ca2a3c32d8b7a690d33bebc7b9e9458d`  
		Last Modified: Tue, 13 Jan 2026 01:25:30 GMT  
		Size: 136.7 KB (136737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c848acbad27f1c9d2fd95e0facabbb28d5d8be19e5fa5912e5474c1301522523`  
		Last Modified: Tue, 13 Jan 2026 01:25:25 GMT  
		Size: 2.3 MB (2278686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9529916038b7840d3177e93bf04b78390bb91bca78623bd9c0769f9e2a965079`  
		Last Modified: Tue, 13 Jan 2026 01:25:25 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24239fc168f5eb73ae9964e2cdcb3c3b878ae79835c6b94585cb648fd50479d`  
		Last Modified: Tue, 13 Jan 2026 01:25:26 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:0d72ad7b507d17cffe5dbec1ddecf1c254c3a85d2b605fa0ddbc9913ba4fc678
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe582f0cad77d385a3debb0f2acf0c96b7b85c6a7d2c95fcc54f938d63635c9`

```dockerfile
```

-	Layers:
	-	`sha256:7d598d8c3b4cd06481693da06e86554144167d205cc60f43382fafba94dd4592`  
		Last Modified: Tue, 13 Jan 2026 04:35:37 GMT  
		Size: 2.0 MB (2008290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dd2469227ab0e75822eb9d56a5d7c05f52a445840f65934e010a2562e509718`  
		Last Modified: Tue, 13 Jan 2026 01:25:24 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm variant v5

```console
$ docker pull memcached@sha256:efa6728c05b024b605597e5025f04155aab614b52f56b1b31a4c70a23f909e07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30298859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14119dc07998a4322ac912beaaf4e6ad16e5487f2243c332fdaad86bdce6f55e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:19:21 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 13 Jan 2026 01:19:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:22:43 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 13 Jan 2026 01:22:43 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 13 Jan 2026 01:22:43 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 13 Jan 2026 01:22:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 13 Jan 2026 01:22:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:22:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 01:22:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:22:43 GMT
USER memcache
# Tue, 13 Jan 2026 01:22:43 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 13 Jan 2026 01:22:43 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c113d410d30c2c035a105b56d3937958c81fbe2530f44add3bae903be6864324`  
		Last Modified: Tue, 13 Jan 2026 00:42:30 GMT  
		Size: 27.9 MB (27942724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96776850dc1206c3fd163b84cea19599306159eb0d020b4241d0172240f88d13`  
		Last Modified: Tue, 13 Jan 2026 01:22:55 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3697c7c790d9c4caaa904abdaf809dcdee3f0b518fc5ad82d2e21dd7fe24f64d`  
		Last Modified: Tue, 13 Jan 2026 01:22:55 GMT  
		Size: 144.2 KB (144212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a247339c7ec57a491c3ffe43531dbfaa132f3ff16a481fc41cbb9e3e3ad6476`  
		Last Modified: Tue, 13 Jan 2026 01:22:50 GMT  
		Size: 2.2 MB (2210412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2dcebe3ab2a9945cdea142301e4a64eebbc59c948a54385dbfca4afd561b508`  
		Last Modified: Tue, 13 Jan 2026 01:22:55 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb8ef5ecbc44efd5280f9cf15687dfd80a34fa2966ad039238647177f75dc6c`  
		Last Modified: Tue, 13 Jan 2026 01:22:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:190bb1ecd7376720e541621921c2d4931a9d0f85a047255ba2b56afa3a504212
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9736e9545a46e4ef65dcb5238691292d27fac4dccb330354ce59ac93ae6994b5`

```dockerfile
```

-	Layers:
	-	`sha256:4f5461bf596f750b56b3f10e315936c2326b2c32901d28cdf22db97072bba685`  
		Last Modified: Tue, 13 Jan 2026 01:22:50 GMT  
		Size: 2.0 MB (2011293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8657d28d0436d39193457fb90119ea6e4ddb566df2a83fd1aa9df75651731188`  
		Last Modified: Tue, 13 Jan 2026 04:35:43 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm variant v7

```console
$ docker pull memcached@sha256:9c322c838b4648fa30e742e53ed6647a31383760fb73fa82de32b4b6dc88c494
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28509532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6e130248535c57fccff4d89a9d442e31cabd471e41c9eed52e5207a54f9f944`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:25:47 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 13 Jan 2026 01:25:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:28:55 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 13 Jan 2026 01:28:55 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 13 Jan 2026 01:28:55 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 13 Jan 2026 01:28:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 13 Jan 2026 01:28:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:28:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 01:28:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:28:55 GMT
USER memcache
# Tue, 13 Jan 2026 01:28:55 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 13 Jan 2026 01:28:55 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029a2cbe46c1e12ab6d47a63f40fb29056b6c6277c7822085ed0fe62e0a1791d`  
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c7827f95482598f1bd32dd8cbe071ad009795fa108661234eeb872d1a1e8bd`  
		Last Modified: Tue, 13 Jan 2026 01:29:07 GMT  
		Size: 135.4 KB (135398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9371e974781bd91adc657086f00cd7d91b5530ca9da37597c347dd7d4eaff0`  
		Last Modified: Tue, 13 Jan 2026 01:29:07 GMT  
		Size: 2.2 MB (2164040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c2e0f64c0afa16b5e214ae208c8c81e8c78c79ddd90f54983a93c7297395f6b`  
		Last Modified: Tue, 13 Jan 2026 01:29:07 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92151d443057f88ed7f60405440b698ff9e6abe1a2ca1c91a0c7e7626339ad2`  
		Last Modified: Tue, 13 Jan 2026 01:29:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:12cc31a1ce56d2c6dd1c0dcfd4ef1fe74484985d010594950c086c0f4431559b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b2d844d5393973080c37fde0b92cd48bd1a64e03973290631be5486d814de7e`

```dockerfile
```

-	Layers:
	-	`sha256:99fc27444c1ccdd6cbd08a33aac22e9e85f55958bda7b6216bdea08eae374cff`  
		Last Modified: Tue, 13 Jan 2026 04:35:47 GMT  
		Size: 2.0 MB (2009750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e76d5584f581b7668c61a661da2858bc1d5e11b31e3629e0d2b3af52d9c22ed8`  
		Last Modified: Tue, 13 Jan 2026 04:35:47 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:2ed537fa0376a3eb0864d6a3b51ea7da59b9ff4bb3270189a8a5082f02f811e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32550406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf26d75d787aabbd202c97db1079b96e45105d3ca509a1001ab973cb473cae8c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:22:29 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 13 Jan 2026 01:22:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:25:26 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 13 Jan 2026 01:25:26 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 13 Jan 2026 01:25:26 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 13 Jan 2026 01:25:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 13 Jan 2026 01:25:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:25:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 01:25:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:25:27 GMT
USER memcache
# Tue, 13 Jan 2026 01:25:27 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 13 Jan 2026 01:25:27 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78edb6b991369235f90958a936afc89dc37b82439c632988ed143b5bd76deadb`  
		Last Modified: Tue, 13 Jan 2026 01:25:40 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e1afbb765f6cc3923e864d44fb6cd6c9167b884e596b09bd37c7c276f65a2b`  
		Last Modified: Tue, 13 Jan 2026 01:25:40 GMT  
		Size: 153.5 KB (153512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff9edc68fe57c233001afd442eb6c248bf070d32fbb412a8bfeef6f9a6217f5`  
		Last Modified: Tue, 13 Jan 2026 01:25:40 GMT  
		Size: 2.3 MB (2261341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c4648fbc4a4189184946895d1041e0eee2c5d40fd70638a553bedb0cbf5cf8`  
		Last Modified: Tue, 13 Jan 2026 01:25:40 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26bd1b32b048e73091ddf6e6762e368d4bb6ef2cc7d3aa43467749b36fe08e38`  
		Last Modified: Tue, 13 Jan 2026 01:25:40 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:72333c6222fb20b5a9f9f92b8d56c47ebb5b4e6cd65512a6b5172ad0c0cade67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a2a4e23cbe2d062f3fcfb84c8590190eb72294786a0b8238add858e67a93914`

```dockerfile
```

-	Layers:
	-	`sha256:1f8545bcc66309a59381c88c4c87b0f8352893dbaa167be48947976c1e0cef1d`  
		Last Modified: Tue, 13 Jan 2026 04:35:51 GMT  
		Size: 2.0 MB (2008606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95e6875e372e1d6a9660c08726cb96d08b272e52a2446f275089efccfc3096b3`  
		Last Modified: Tue, 13 Jan 2026 01:25:33 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; 386

```console
$ docker pull memcached@sha256:29540e588e9065db9ecc8865fe74544260980d73786f00dfc4df3f3cee148bd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33661194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66843ae7a7d968c4f056a8e350dd84ff80a06e48b48c298c3427333b7ec259ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:19:43 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 13 Jan 2026 01:19:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:22:40 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 13 Jan 2026 01:22:40 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 13 Jan 2026 01:22:40 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 13 Jan 2026 01:22:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 13 Jan 2026 01:22:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:22:40 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 01:22:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:22:40 GMT
USER memcache
# Tue, 13 Jan 2026 01:22:40 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 13 Jan 2026 01:22:40 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:27bb6d39eda5ced7626db280c3902aacdfade5acd11a16ef9618e3185f69b102`  
		Last Modified: Tue, 13 Jan 2026 00:43:03 GMT  
		Size: 31.3 MB (31288476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cedb4f2840edea9de46e0d955a0512f469211880560a8948f10b54381bcd728`  
		Last Modified: Tue, 13 Jan 2026 01:22:53 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c4b2d1574ee5f238dc6948164abd39ffcc91929b2c464c6b3874dec01fd964`  
		Last Modified: Tue, 13 Jan 2026 01:22:46 GMT  
		Size: 147.6 KB (147554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc1bf5870b84175607f3d012b3cfebc5859869f8125114ea5d6ed1a05f81d2d`  
		Last Modified: Tue, 13 Jan 2026 01:22:53 GMT  
		Size: 2.2 MB (2223652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6434e73ed67e81f1016f27c7cc175290b0ce959d8a1bf5e9b0f3119f161246`  
		Last Modified: Tue, 13 Jan 2026 01:22:53 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abaf99fdf0e2b9620d20088b389b3f18eb67ad356c8c6c7961074e1428b8af0c`  
		Last Modified: Tue, 13 Jan 2026 01:22:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:f64192985f4635b04ce1ab99b3cae89f71d0b11f9670fb6d9c470158e3c5c63e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bb9ce834f23725c4bfc4fb2d6a24a96d3d0bc7685d3a759c0085871f34231e8`

```dockerfile
```

-	Layers:
	-	`sha256:ed9937c762728e5abc93b88bd7932a5762d2bc8e0001e81bb25ef0b27e2bc6ff`  
		Last Modified: Tue, 13 Jan 2026 04:35:56 GMT  
		Size: 2.0 MB (2005447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6358862e12c5c5367efd52bea0b1194e04e76f267084da591229f64ee7482dc3`  
		Last Modified: Tue, 13 Jan 2026 04:35:57 GMT  
		Size: 22.1 KB (22094 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; ppc64le

```console
$ docker pull memcached@sha256:309e0faad388272d7e37d6ee0cb354707d099e3140298105499711823d7a0eea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36161489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6f50ee10fc83da67b90c9bda7499251fa073fea87400d5fb70e31e693d6f902`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:33:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 13 Jan 2026 01:33:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:36:52 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 13 Jan 2026 01:36:52 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 13 Jan 2026 01:36:52 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 13 Jan 2026 01:36:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 13 Jan 2026 01:36:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:36:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 01:36:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:36:53 GMT
USER memcache
# Tue, 13 Jan 2026 01:36:53 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 13 Jan 2026 01:36:53 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9a275bb13cf8b3e9db52a41b6b4ff22ee1ffed00394f6deddd2de45044bd3bae`  
		Last Modified: Tue, 13 Jan 2026 00:57:13 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093e59deb53ff01a892be2a5df928c4b04a289df7f6c135570c11d6a4fdbc53a`  
		Last Modified: Tue, 13 Jan 2026 01:37:16 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4da25c8b13ee47050a38843c1954d2bd7bbdba2666f725aee2f603e03fcb6d`  
		Last Modified: Tue, 13 Jan 2026 01:37:16 GMT  
		Size: 170.4 KB (170427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cab5f6f805c735c0f324c87ff8c66cfab0e35fb691b7761e85bb9a2bbb31cfe`  
		Last Modified: Tue, 13 Jan 2026 01:37:16 GMT  
		Size: 2.4 MB (2393947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3a7dfc8da65bd6101de156530bc2688c5588c718bbc3131ff4594cbefd0e66`  
		Last Modified: Tue, 13 Jan 2026 01:37:09 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06153b2e2bde9b06f1c2719aabb5ff6a6c23056152a024fa2c990d97b4d9c799`  
		Last Modified: Tue, 13 Jan 2026 01:37:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:8dfcc685b38edcaec140b90716d19e543715184f20f7a401d6f734ad8f8cf1dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7442b6e23a86bfe5ee9a534d43f0a55ba9629d3c24128b1b3e2b5121644dcf00`

```dockerfile
```

-	Layers:
	-	`sha256:a4b6027eed506a371ad9a2314b6be299e5c509b4c4be66e5842b29837171b0cf`  
		Last Modified: Tue, 13 Jan 2026 04:36:00 GMT  
		Size: 2.0 MB (2011891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc718b3aa0399c50248bba6165cad8666196a5351b6ed095a8101d2f8a5d37da`  
		Last Modified: Tue, 13 Jan 2026 04:36:01 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; riscv64

```console
$ docker pull memcached@sha256:bce857473a0aeeec89bc5383841d05d99df2b89bba49caf3059874a9442ff224
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30613806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc8f84b5bfd0d6518442de566ffa39b2113651446c246e419f61a8e5fa68e87`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Wed, 14 Jan 2026 06:36:03 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 14 Jan 2026 06:36:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jan 2026 06:49:42 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 14 Jan 2026 06:49:42 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 14 Jan 2026 06:49:42 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 14 Jan 2026 06:49:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 14 Jan 2026 06:49:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 06:49:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 14 Jan 2026 06:49:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 06:49:43 GMT
USER memcache
# Wed, 14 Jan 2026 06:49:43 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 14 Jan 2026 06:49:43 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7c6f79d4d52450222a8a38f8fc98e229a4711a246fc94fdaaab31930d3135d`  
		Last Modified: Wed, 14 Jan 2026 06:50:36 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168d1b37fe07dfb8bef5240057ad6597058647499a9e771eedd2091f2d6b30f0`  
		Last Modified: Wed, 14 Jan 2026 06:50:36 GMT  
		Size: 133.1 KB (133105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a5ebc1ef49cab24f75e0c751a1e0563ee042c246c509279fa38cf3cbf0a3f1`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 2.2 MB (2207499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbc8df7ca1d2f273c3c8fec55b30f17ebc72a45687976efd9c8779a66369d46`  
		Last Modified: Wed, 14 Jan 2026 06:50:36 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4057c9476d421ae1ecae3607afb0db57dbc6eb2bc0aa5e41daed169a70319c1`  
		Last Modified: Wed, 14 Jan 2026 06:50:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:75823016a946bfe52b08e1f80032a64b0202a08f2e30dd8cb7035a01e1244518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b86887925c9eccb39ad75807a81768a06591c668cfd4bf4af00a40b2414f22bc`

```dockerfile
```

-	Layers:
	-	`sha256:0d93e934848935cdae8d83be9ebaff197aaa6e70f5b224c2107461561ea0064d`  
		Last Modified: Wed, 14 Jan 2026 07:34:47 GMT  
		Size: 2.0 MB (2002254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0de5bd0cbff9df1fc11e05bd38936b6915195663b273b5c23840bf5eb9373a8`  
		Last Modified: Wed, 14 Jan 2026 07:34:48 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; s390x

```console
$ docker pull memcached@sha256:46c34c0b238fbae2980413fe2b6590839b6afbc43e0a1e07eb456fc274eaf811
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32272852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8666231b78b1bdfb283fe302437321dedf8ecc2d869ff2acdce9f8461f285519`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 14:13:49 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 13 Jan 2026 14:13:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 14:16:57 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 13 Jan 2026 14:16:57 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 13 Jan 2026 14:16:57 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 13 Jan 2026 14:16:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 13 Jan 2026 14:16:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 14:16:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 14:16:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 14:16:57 GMT
USER memcache
# Tue, 13 Jan 2026 14:16:57 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 13 Jan 2026 14:16:57 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2b46bc94baaae0a37e5e04b1babf7e1f37c4390b83d49c3c6820188deba770e3`  
		Last Modified: Tue, 13 Jan 2026 13:10:43 GMT  
		Size: 29.8 MB (29833411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2727771ad16d920baecb7c96b9b54e67178369b881fc20901d381dfd5f873e27`  
		Last Modified: Tue, 13 Jan 2026 14:17:12 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6b0ec5581f8591522a6327cdcfa4e1197d9ada9fb60840f57b5d3e4dd3304d1`  
		Last Modified: Tue, 13 Jan 2026 14:17:12 GMT  
		Size: 140.6 KB (140562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382a3e1ebed70673a0789fcc2104ab941fe04b9a020339f9286ac85b67ae5ff9`  
		Last Modified: Tue, 13 Jan 2026 14:17:13 GMT  
		Size: 2.3 MB (2297368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85fe5f9afd355e3dd76ce942e1c295e356d96ae3b0e3f8236a0e33c5f75ffe71`  
		Last Modified: Tue, 13 Jan 2026 14:17:08 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4546f3c3457928dc273f98dae7c7ac2f945b203138e964ee72fc92aabcef434`  
		Last Modified: Tue, 13 Jan 2026 14:17:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:d620668087c443f58d215a372a70eb0697c7031777d3537d244fa26e62d3ec3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e48c5956bcfcf63509c135da7076a0f247bc2858c7df68331b5a112e937ff6c`

```dockerfile
```

-	Layers:
	-	`sha256:507d45d8f4547a846c07788edb1628f89b93ac7616169374be23f29601b7be68`  
		Last Modified: Tue, 13 Jan 2026 14:17:08 GMT  
		Size: 2.0 MB (2009727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78fdd8684e48fc4ee1817e00df577a38250864ffbcf34ec341937d525d9dfabd`  
		Last Modified: Tue, 13 Jan 2026 16:34:40 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine`

```console
$ docker pull memcached@sha256:c77536380fd3c7740933767bb5279bd30e31c8d496081e5113a37d9b9eec43cb
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
$ docker pull memcached@sha256:9573a2399011fa86bb7b5d12bdab987d7931c98ddec0ef6802de7eb6d3c3e338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5956768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c79853acc5f24e9c28f15d45cef0aedc114e76bbacf7958eb6f555c22246e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:34 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:29:34 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:32:07 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:32:07 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:32:07 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:32:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:32:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:32:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:32:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:32:07 GMT
USER memcache
# Thu, 18 Dec 2025 00:32:07 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:32:07 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:48:50 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57c33ac8581cd04f31208409f36331e938a78e6ae3a7a3b530fe9dfebe6eb9ad`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583aae99135b9036c602a1c60743fc4fd519f261ac6d48ed60b01e1beb019e7f`  
		Last Modified: Thu, 18 Dec 2025 00:32:12 GMT  
		Size: 106.0 KB (106050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ca22885c42a537f033850e8dff7eaeddbb7514902286739b48c084b55a8d6b`  
		Last Modified: Thu, 18 Dec 2025 00:32:12 GMT  
		Size: 2.0 MB (1989265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d146e2038834770bed57033a6c5d66ead5b731b8b133856dec6726ca21baee9`  
		Last Modified: Thu, 18 Dec 2025 00:32:12 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c66e6c3acbe07806e3e96a97d97a2d4503713c4814d9b24a2f57f2c39200d05`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:cfdf2ea6bf2a04bb7ee1568efe0c8bd38a1f5e644250a9409479cce281891ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de792623281192b3965fdc95f31532c4d166e731f53e202be1e2a224c654633b`

```dockerfile
```

-	Layers:
	-	`sha256:87a0d23eeeda6353dfc603cc4ffee062e5383be07b611754f3a88db3fc644036`  
		Last Modified: Thu, 18 Dec 2025 00:32:12 GMT  
		Size: 94.9 KB (94873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b73cd5efe31baa1fbf0eecea269426edcfc795cbb9b5dd74b523ff51b6f7c9f`  
		Last Modified: Thu, 18 Dec 2025 01:34:48 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:c1a12b64cc8b47f50ea4610d9c1c362da7157b3ba67deac8b4760e6b589cde75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5611647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3591f95cad049a0509bd23a95556f8f848452d2a5491ed00bae293897c7a6b2f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:27:48 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:27:49 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:49:50 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:49:50 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:49:50 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:49:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:49:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:49:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:49:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:49:50 GMT
USER memcache
# Thu, 18 Dec 2025 00:49:50 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:49:50 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf585eb2bfa372c2097b9f7a5214ecb0941a30581b10fb74a26518fcc7addec`  
		Last Modified: Thu, 18 Dec 2025 00:49:55 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01bb148ea8fbe93dd8097d85f9ee3cf547d314e669748b4239c05711b0d5f719`  
		Last Modified: Thu, 18 Dec 2025 00:49:55 GMT  
		Size: 102.7 KB (102652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6549359cda37ac41cf41a5ece5f37f1322a82f6b232f12e446c62840637093e`  
		Last Modified: Thu, 18 Dec 2025 00:50:02 GMT  
		Size: 1.9 MB (1939215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:041e37eaffefcfb0809564ddea591be3cd818de5530e2c853c0bc9a2fa25c116`  
		Last Modified: Thu, 18 Dec 2025 00:49:55 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7907ae218c75b36c9a9002be8554131c271cde78b0280cb7a85029f99ad0bcdc`  
		Last Modified: Thu, 18 Dec 2025 00:50:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:a9c26fc290551b691574e093d3c28f4fe7b558b3f8173b3c99eb8a664c83a8e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ca65d7156e6586d96310ea3162facd9849d5460d2939b461a25247b06a4d59`

```dockerfile
```

-	Layers:
	-	`sha256:d9c217dc241f1175812c47b6489d325a0574c0da554c6f8aa0b86a2d8aff05f9`  
		Last Modified: Thu, 18 Dec 2025 01:34:52 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:cee00a47bf7b8b5899a6cf1f5c692494df31b454f52b81f3c4886905a0c9bdd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5270304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d91d78dbe118f2b7b0d6e850e1115de72c4fe3e30c55a5b53d8a844d14357d16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:30:56 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:30:57 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:33:51 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:33:51 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:33:51 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:33:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:33:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:33:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:33:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:33:51 GMT
USER memcache
# Thu, 18 Dec 2025 00:33:51 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:33:51 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:43 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa22c446792763e48f4680945ccc68d43c7906ef35a92e0b908f57ef53e72f0`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954155078f2265364295ebdf16fb114e991b1938d8a6951fb511163ab3b2b385`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 92.4 KB (92378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a25584b03ac5e45c66c3c616acfd9df1848e5db25219ef20feb2868c30c6332`  
		Last Modified: Thu, 18 Dec 2025 00:33:57 GMT  
		Size: 1.9 MB (1897191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f237be962bb57c3f749904b5925c8e1d7e9013dfac7dd52cc9611ada81858e`  
		Last Modified: Thu, 18 Dec 2025 00:33:57 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b07d9170b246a631c262d9f5d57f49278f7cd4805463b90b14aeca4dc61d93`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:64abe011fed6a9cf7b3290c752c50bffe81bb2e65cf6337e023efda87d49b451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b251b9c15ab7c5742bd3ab725df09f0ecb9f2491f92cf1c825bec598a31f4407`

```dockerfile
```

-	Layers:
	-	`sha256:1882c6d4361100a29fd5ab265587f65fa27b1df15e7f9349b30dac454facf98e`  
		Last Modified: Thu, 18 Dec 2025 00:33:57 GMT  
		Size: 94.3 KB (94291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf0a88ab3838de6beab653497ab62a64cfb87b1dc83c5fa5b6f3907abfd88080`  
		Last Modified: Thu, 18 Dec 2025 01:34:56 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:b6c3042e2bf09ec3d3f054d03b81313e8df717a49371ce916ff743e602796bc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6285509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6691028570bbd843e6da26558c46162b8383212fcaaefcecb2d3f919e3401429`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:18 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:29:19 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:32:06 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:32:06 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:32:06 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:32:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:32:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:32:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:32:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:32:06 GMT
USER memcache
# Thu, 18 Dec 2025 00:32:06 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:32:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb7b8445facedfc145b9478f74880f520776460f153005b7f437ec339aee530`  
		Last Modified: Thu, 18 Dec 2025 00:32:11 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1853c901134389608b6e80aaa3e43cd67a35c71aecfdde4b5b7ed3b989a03c`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 121.9 KB (121860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a01d1ac5ce47f4494363e411e1cd25dea26438213a2d18d6bb104d0974d9a52`  
		Last Modified: Thu, 18 Dec 2025 00:32:11 GMT  
		Size: 2.0 MB (1966561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115624f24ba74d393c2da3d65ed5b35a7afb3fa9ad143d3fb82c64953b3d0401`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87bba524314294ca97195ce65a35ec6d42d3f9f18c9cc0c05c064c9a3cf85c0`  
		Last Modified: Thu, 18 Dec 2025 00:32:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:2feda8921a7d67cd9f2f3d7186ed69ceb0d3c22af7a20bd230664e9bcf39096c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d73c6548a24cc8ce7782d03377e89a4b4b0e4c2a48cd3a03a79193320fc4d834`

```dockerfile
```

-	Layers:
	-	`sha256:984e438122735983bf56bc3d638fb1b0baf8cfb26ce26f71e0a9b847d25f76b5`  
		Last Modified: Thu, 18 Dec 2025 01:34:59 GMT  
		Size: 94.3 KB (94327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d6e8d91ca57b45f0050ec3833a8f09a7ce62f7ba9ec70e1ae12881ad4b2bb6f`  
		Last Modified: Thu, 18 Dec 2025 01:35:00 GMT  
		Size: 20.7 KB (20728 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; 386

```console
$ docker pull memcached@sha256:df1ba8af73cd6e3f8227557b097cd6b128ec0d410a3bbe7a2c282089c5641b41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5740953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78dbfc1f8ea65ad6466795e278180963d4afe98dfbca4a4497bc73c99f07ed4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:13:19 GMT
ADD alpine-minirootfs-3.23.2-x86.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:13:19 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:43 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:29:44 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:32:29 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:32:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:32:29 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:32:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:32:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:32:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:32:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:32:29 GMT
USER memcache
# Thu, 18 Dec 2025 00:32:29 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:32:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c21df6a7383dfce37a4bfe31b291881f55907c419caf5d06cb6d699d290d0718`  
		Last Modified: Thu, 18 Dec 2025 00:13:38 GMT  
		Size: 3.7 MB (3686100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37ec5bf455c1d98d22e6f3dacb5b971dac8ea96d1fe9b9177a07c5277530646`  
		Last Modified: Thu, 18 Dec 2025 00:32:35 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b2862af05c1582c8625c82ea0863dc2b6474e410d3e6a32876c920e0152c73`  
		Last Modified: Thu, 18 Dec 2025 00:32:35 GMT  
		Size: 110.7 KB (110740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30872a43f6c591fd9b979b49b0fb32107b4bfa8c1155657fa255aa199cf0b83b`  
		Last Modified: Thu, 18 Dec 2025 00:32:35 GMT  
		Size: 1.9 MB (1942762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a62c11b4aeceaba2e5e73a1bc29aa8b4fc42ccd0c7e8512cc11b96e48aef2f`  
		Last Modified: Thu, 18 Dec 2025 00:32:41 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f553d362a11992264bf5364cfe13d248403c5baf2ecac784c26f444dbfb90388`  
		Last Modified: Thu, 18 Dec 2025 00:32:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:e3b020c2afd9ae372e234c6ab67456908861fd24200448fd3cf741503a8a6f55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6abfcddfb1575f6cc07e51c6a379141589de7ea8c329a9bc5c1592f3186e6fda`

```dockerfile
```

-	Layers:
	-	`sha256:ff9be8ef1bab92275eb15ae5fd6a05e767abc1fe855455766200b3c0a1866e33`  
		Last Modified: Thu, 18 Dec 2025 01:35:03 GMT  
		Size: 94.8 KB (94828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d7026bdf84e278b6976f0ccab2297ddc0284cf329414f56d12608dbc2acb940`  
		Last Modified: Thu, 18 Dec 2025 00:32:35 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:7292c7b145e08f87f78644bf2c3355fad1d0b4d9366f173ffa0634c3ec93addf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6031729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ae72ba97ecea986f01bda1eb392aee1ded4b5a86b2edcabe92a2034143e155b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:33:41 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:33:42 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:36:14 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:36:14 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:36:14 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:36:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:36:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:36:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:36:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:36:14 GMT
USER memcache
# Thu, 18 Dec 2025 00:36:14 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:36:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c95450233dfe3e06529eb39ca4b46e6ad51ccf338cab64157669ff1fc0a8d72`  
		Last Modified: Thu, 18 Dec 2025 00:36:26 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4079a2d61bafcf146b8f57b35f0e39bf2548e0963be10cff5086f9a56ccdd9d`  
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
		Size: 126.3 KB (126257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f69efa1066815d67cf415d0aac5dcd305032257b6bded5a4c57a7444a1e7fd4`  
		Last Modified: Thu, 18 Dec 2025 00:36:26 GMT  
		Size: 2.1 MB (2076363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357f4165f53a3d4c66ef270bcb5b5283a066af50f79924cccc7c73f6a4f6f4ab`  
		Last Modified: Thu, 18 Dec 2025 00:36:36 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a65ff5cefcbfc874c1cac0857339eaee0b07147dd26b6bfa18c00921b4f30c`  
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:1d06281345f2ac44a607d40d5e87de6abb99bbc6ee82d319e73f3794602d0282
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4867a5aa08041c7e5ec69dfc84214226a7323d1ce703747ae2117675e2f74bcd`

```dockerfile
```

-	Layers:
	-	`sha256:282960f007d3f1f008333191d98a2ded5ff0f83075ace30043349b6c082c18fd`  
		Last Modified: Thu, 18 Dec 2025 01:35:08 GMT  
		Size: 94.3 KB (94280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4755fffd5924e8405adfbed0f328ad9792eff20e2b8ad2025e1f5c85bca88618`  
		Last Modified: Thu, 18 Dec 2025 01:35:09 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:9023f4a863c531a74c6ff8cc3b49c3be80ad1db07cc93fdcbf87c5d8e4cccc72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5768619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2159b7b74e5ffe77e6304def07dec2cfc2bdead26c3012e1e4d39bcd267adfe5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 06:39:34 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 06:39:38 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 06:52:53 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 06:52:53 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 06:52:53 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 06:52:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 06:52:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 06:52:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 06:52:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 06:52:53 GMT
USER memcache
# Thu, 18 Dec 2025 06:52:53 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 06:52:53 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc016d1883c21894ae540944be0270a95cb663037e8592a944bac62e0cc39e7`  
		Last Modified: Thu, 18 Dec 2025 06:53:25 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c580cd51da178bea3e44467f8b445f50ec9272e42e0254d269a9e38204b12dc`  
		Last Modified: Thu, 18 Dec 2025 06:53:25 GMT  
		Size: 108.9 KB (108898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11881c79ebc6a05357f0e2095f00d6d5a8a58bd9f11efeefc80b616d0230ff9`  
		Last Modified: Thu, 18 Dec 2025 06:53:25 GMT  
		Size: 2.1 MB (2074429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735bfa953d895df9672fe0b34207075bd7e686f71104973ad4e02d89db8719a9`  
		Last Modified: Thu, 18 Dec 2025 06:53:25 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b8c865432ff9b07178ba7cb96426e0515b00cc91866fb4dfb8c243e4187172`  
		Last Modified: Thu, 18 Dec 2025 06:53:25 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7cd6a8f4c278ff9062def241e6cdb501032ed72b091608a6da35812eece0954c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38b0c310a1ad4186c4beae0e268b71f1a80ed998cd80ceb81095aa9da7e6b02e`

```dockerfile
```

-	Layers:
	-	`sha256:88642ee1ee3c124ff8f2f640525172206ce9483620a70142ca673e0eca181c4d`  
		Last Modified: Thu, 18 Dec 2025 07:34:34 GMT  
		Size: 94.3 KB (94276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:441bda294fdd657b4574cd5337193125e3d0565433a700136501a858fce53d46`  
		Last Modified: Thu, 18 Dec 2025 07:34:34 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:e011484878fd5d1e2da6de478ac11d01ae80f0bdef1902dcde3ed53728803741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5857090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:689ea71c305b80e206c68a215481290a1378e6375e32ad059455f7d041396aa6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:30:26 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:30:27 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:33:46 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:33:46 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:33:46 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:33:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:33:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:33:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:33:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:33:46 GMT
USER memcache
# Thu, 18 Dec 2025 00:33:46 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:33:46 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4594a6826f7ed03c8c4f9f2aebb9716eb6e16d5b5ab7e1bc247783b503c5b10`  
		Last Modified: Thu, 18 Dec 2025 00:33:55 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f270744f8d8b82bc6657387109b33836a76d6dbf8faa645a997db7ea290cdb`  
		Last Modified: Thu, 18 Dec 2025 00:33:55 GMT  
		Size: 114.3 KB (114299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91f8ee8f36703944a7bdcaf57cc5772fe9f79c74a088c33fa1b6da7de119f93`  
		Last Modified: Thu, 18 Dec 2025 00:33:55 GMT  
		Size: 2.0 MB (2017131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e21d2db88668745770273c7b36d4d2c1e87a80b0118b8d775813860b467384c8`  
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd847159e169b898a67d4454fd5a22406c5ae623b16889d084a1d5f2d46a499`  
		Last Modified: Thu, 18 Dec 2025 00:33:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:33ab737cb23dcde22de59a58e40f1f80d2c5e808ff3036519ae7d9db228fa37d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3562f7fd7806da24b1865c01a2246ac041b5e98d69c10ce6cbbe479f9408f9a1`

```dockerfile
```

-	Layers:
	-	`sha256:d5f43e64a79ee525bd0354a06e3284444fd642bbe6c1a782aa45ec2e20462f1d`  
		Last Modified: Thu, 18 Dec 2025 01:35:19 GMT  
		Size: 94.2 KB (94222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bd2c024010f4f53d350bde9967c349efb3a58a2a812b14e17b29ddbd19eab87`  
		Last Modified: Thu, 18 Dec 2025 01:35:20 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine3.23`

```console
$ docker pull memcached@sha256:c77536380fd3c7740933767bb5279bd30e31c8d496081e5113a37d9b9eec43cb
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
$ docker pull memcached@sha256:9573a2399011fa86bb7b5d12bdab987d7931c98ddec0ef6802de7eb6d3c3e338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5956768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c79853acc5f24e9c28f15d45cef0aedc114e76bbacf7958eb6f555c22246e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:34 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:29:34 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:32:07 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:32:07 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:32:07 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:32:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:32:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:32:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:32:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:32:07 GMT
USER memcache
# Thu, 18 Dec 2025 00:32:07 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:32:07 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:48:50 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57c33ac8581cd04f31208409f36331e938a78e6ae3a7a3b530fe9dfebe6eb9ad`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583aae99135b9036c602a1c60743fc4fd519f261ac6d48ed60b01e1beb019e7f`  
		Last Modified: Thu, 18 Dec 2025 00:32:12 GMT  
		Size: 106.0 KB (106050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ca22885c42a537f033850e8dff7eaeddbb7514902286739b48c084b55a8d6b`  
		Last Modified: Thu, 18 Dec 2025 00:32:12 GMT  
		Size: 2.0 MB (1989265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d146e2038834770bed57033a6c5d66ead5b731b8b133856dec6726ca21baee9`  
		Last Modified: Thu, 18 Dec 2025 00:32:12 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c66e6c3acbe07806e3e96a97d97a2d4503713c4814d9b24a2f57f2c39200d05`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:cfdf2ea6bf2a04bb7ee1568efe0c8bd38a1f5e644250a9409479cce281891ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de792623281192b3965fdc95f31532c4d166e731f53e202be1e2a224c654633b`

```dockerfile
```

-	Layers:
	-	`sha256:87a0d23eeeda6353dfc603cc4ffee062e5383be07b611754f3a88db3fc644036`  
		Last Modified: Thu, 18 Dec 2025 00:32:12 GMT  
		Size: 94.9 KB (94873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b73cd5efe31baa1fbf0eecea269426edcfc795cbb9b5dd74b523ff51b6f7c9f`  
		Last Modified: Thu, 18 Dec 2025 01:34:48 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.23` - linux; arm variant v6

```console
$ docker pull memcached@sha256:c1a12b64cc8b47f50ea4610d9c1c362da7157b3ba67deac8b4760e6b589cde75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5611647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3591f95cad049a0509bd23a95556f8f848452d2a5491ed00bae293897c7a6b2f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:27:48 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:27:49 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:49:50 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:49:50 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:49:50 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:49:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:49:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:49:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:49:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:49:50 GMT
USER memcache
# Thu, 18 Dec 2025 00:49:50 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:49:50 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf585eb2bfa372c2097b9f7a5214ecb0941a30581b10fb74a26518fcc7addec`  
		Last Modified: Thu, 18 Dec 2025 00:49:55 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01bb148ea8fbe93dd8097d85f9ee3cf547d314e669748b4239c05711b0d5f719`  
		Last Modified: Thu, 18 Dec 2025 00:49:55 GMT  
		Size: 102.7 KB (102652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6549359cda37ac41cf41a5ece5f37f1322a82f6b232f12e446c62840637093e`  
		Last Modified: Thu, 18 Dec 2025 00:50:02 GMT  
		Size: 1.9 MB (1939215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:041e37eaffefcfb0809564ddea591be3cd818de5530e2c853c0bc9a2fa25c116`  
		Last Modified: Thu, 18 Dec 2025 00:49:55 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7907ae218c75b36c9a9002be8554131c271cde78b0280cb7a85029f99ad0bcdc`  
		Last Modified: Thu, 18 Dec 2025 00:50:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:a9c26fc290551b691574e093d3c28f4fe7b558b3f8173b3c99eb8a664c83a8e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ca65d7156e6586d96310ea3162facd9849d5460d2939b461a25247b06a4d59`

```dockerfile
```

-	Layers:
	-	`sha256:d9c217dc241f1175812c47b6489d325a0574c0da554c6f8aa0b86a2d8aff05f9`  
		Last Modified: Thu, 18 Dec 2025 01:34:52 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.23` - linux; arm variant v7

```console
$ docker pull memcached@sha256:cee00a47bf7b8b5899a6cf1f5c692494df31b454f52b81f3c4886905a0c9bdd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5270304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d91d78dbe118f2b7b0d6e850e1115de72c4fe3e30c55a5b53d8a844d14357d16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:30:56 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:30:57 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:33:51 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:33:51 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:33:51 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:33:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:33:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:33:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:33:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:33:51 GMT
USER memcache
# Thu, 18 Dec 2025 00:33:51 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:33:51 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:43 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa22c446792763e48f4680945ccc68d43c7906ef35a92e0b908f57ef53e72f0`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954155078f2265364295ebdf16fb114e991b1938d8a6951fb511163ab3b2b385`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 92.4 KB (92378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a25584b03ac5e45c66c3c616acfd9df1848e5db25219ef20feb2868c30c6332`  
		Last Modified: Thu, 18 Dec 2025 00:33:57 GMT  
		Size: 1.9 MB (1897191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f237be962bb57c3f749904b5925c8e1d7e9013dfac7dd52cc9611ada81858e`  
		Last Modified: Thu, 18 Dec 2025 00:33:57 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b07d9170b246a631c262d9f5d57f49278f7cd4805463b90b14aeca4dc61d93`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:64abe011fed6a9cf7b3290c752c50bffe81bb2e65cf6337e023efda87d49b451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b251b9c15ab7c5742bd3ab725df09f0ecb9f2491f92cf1c825bec598a31f4407`

```dockerfile
```

-	Layers:
	-	`sha256:1882c6d4361100a29fd5ab265587f65fa27b1df15e7f9349b30dac454facf98e`  
		Last Modified: Thu, 18 Dec 2025 00:33:57 GMT  
		Size: 94.3 KB (94291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf0a88ab3838de6beab653497ab62a64cfb87b1dc83c5fa5b6f3907abfd88080`  
		Last Modified: Thu, 18 Dec 2025 01:34:56 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:b6c3042e2bf09ec3d3f054d03b81313e8df717a49371ce916ff743e602796bc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6285509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6691028570bbd843e6da26558c46162b8383212fcaaefcecb2d3f919e3401429`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:18 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:29:19 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:32:06 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:32:06 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:32:06 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:32:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:32:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:32:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:32:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:32:06 GMT
USER memcache
# Thu, 18 Dec 2025 00:32:06 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:32:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb7b8445facedfc145b9478f74880f520776460f153005b7f437ec339aee530`  
		Last Modified: Thu, 18 Dec 2025 00:32:11 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1853c901134389608b6e80aaa3e43cd67a35c71aecfdde4b5b7ed3b989a03c`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 121.9 KB (121860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a01d1ac5ce47f4494363e411e1cd25dea26438213a2d18d6bb104d0974d9a52`  
		Last Modified: Thu, 18 Dec 2025 00:32:11 GMT  
		Size: 2.0 MB (1966561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115624f24ba74d393c2da3d65ed5b35a7afb3fa9ad143d3fb82c64953b3d0401`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87bba524314294ca97195ce65a35ec6d42d3f9f18c9cc0c05c064c9a3cf85c0`  
		Last Modified: Thu, 18 Dec 2025 00:32:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:2feda8921a7d67cd9f2f3d7186ed69ceb0d3c22af7a20bd230664e9bcf39096c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d73c6548a24cc8ce7782d03377e89a4b4b0e4c2a48cd3a03a79193320fc4d834`

```dockerfile
```

-	Layers:
	-	`sha256:984e438122735983bf56bc3d638fb1b0baf8cfb26ce26f71e0a9b847d25f76b5`  
		Last Modified: Thu, 18 Dec 2025 01:34:59 GMT  
		Size: 94.3 KB (94327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d6e8d91ca57b45f0050ec3833a8f09a7ce62f7ba9ec70e1ae12881ad4b2bb6f`  
		Last Modified: Thu, 18 Dec 2025 01:35:00 GMT  
		Size: 20.7 KB (20728 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.23` - linux; 386

```console
$ docker pull memcached@sha256:df1ba8af73cd6e3f8227557b097cd6b128ec0d410a3bbe7a2c282089c5641b41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5740953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78dbfc1f8ea65ad6466795e278180963d4afe98dfbca4a4497bc73c99f07ed4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:13:19 GMT
ADD alpine-minirootfs-3.23.2-x86.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:13:19 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:43 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:29:44 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:32:29 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:32:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:32:29 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:32:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:32:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:32:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:32:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:32:29 GMT
USER memcache
# Thu, 18 Dec 2025 00:32:29 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:32:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c21df6a7383dfce37a4bfe31b291881f55907c419caf5d06cb6d699d290d0718`  
		Last Modified: Thu, 18 Dec 2025 00:13:38 GMT  
		Size: 3.7 MB (3686100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37ec5bf455c1d98d22e6f3dacb5b971dac8ea96d1fe9b9177a07c5277530646`  
		Last Modified: Thu, 18 Dec 2025 00:32:35 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b2862af05c1582c8625c82ea0863dc2b6474e410d3e6a32876c920e0152c73`  
		Last Modified: Thu, 18 Dec 2025 00:32:35 GMT  
		Size: 110.7 KB (110740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30872a43f6c591fd9b979b49b0fb32107b4bfa8c1155657fa255aa199cf0b83b`  
		Last Modified: Thu, 18 Dec 2025 00:32:35 GMT  
		Size: 1.9 MB (1942762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a62c11b4aeceaba2e5e73a1bc29aa8b4fc42ccd0c7e8512cc11b96e48aef2f`  
		Last Modified: Thu, 18 Dec 2025 00:32:41 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f553d362a11992264bf5364cfe13d248403c5baf2ecac784c26f444dbfb90388`  
		Last Modified: Thu, 18 Dec 2025 00:32:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:e3b020c2afd9ae372e234c6ab67456908861fd24200448fd3cf741503a8a6f55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6abfcddfb1575f6cc07e51c6a379141589de7ea8c329a9bc5c1592f3186e6fda`

```dockerfile
```

-	Layers:
	-	`sha256:ff9be8ef1bab92275eb15ae5fd6a05e767abc1fe855455766200b3c0a1866e33`  
		Last Modified: Thu, 18 Dec 2025 01:35:03 GMT  
		Size: 94.8 KB (94828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d7026bdf84e278b6976f0ccab2297ddc0284cf329414f56d12608dbc2acb940`  
		Last Modified: Thu, 18 Dec 2025 00:32:35 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.23` - linux; ppc64le

```console
$ docker pull memcached@sha256:7292c7b145e08f87f78644bf2c3355fad1d0b4d9366f173ffa0634c3ec93addf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6031729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ae72ba97ecea986f01bda1eb392aee1ded4b5a86b2edcabe92a2034143e155b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:33:41 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:33:42 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:36:14 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:36:14 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:36:14 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:36:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:36:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:36:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:36:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:36:14 GMT
USER memcache
# Thu, 18 Dec 2025 00:36:14 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:36:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c95450233dfe3e06529eb39ca4b46e6ad51ccf338cab64157669ff1fc0a8d72`  
		Last Modified: Thu, 18 Dec 2025 00:36:26 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4079a2d61bafcf146b8f57b35f0e39bf2548e0963be10cff5086f9a56ccdd9d`  
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
		Size: 126.3 KB (126257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f69efa1066815d67cf415d0aac5dcd305032257b6bded5a4c57a7444a1e7fd4`  
		Last Modified: Thu, 18 Dec 2025 00:36:26 GMT  
		Size: 2.1 MB (2076363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357f4165f53a3d4c66ef270bcb5b5283a066af50f79924cccc7c73f6a4f6f4ab`  
		Last Modified: Thu, 18 Dec 2025 00:36:36 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a65ff5cefcbfc874c1cac0857339eaee0b07147dd26b6bfa18c00921b4f30c`  
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:1d06281345f2ac44a607d40d5e87de6abb99bbc6ee82d319e73f3794602d0282
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4867a5aa08041c7e5ec69dfc84214226a7323d1ce703747ae2117675e2f74bcd`

```dockerfile
```

-	Layers:
	-	`sha256:282960f007d3f1f008333191d98a2ded5ff0f83075ace30043349b6c082c18fd`  
		Last Modified: Thu, 18 Dec 2025 01:35:08 GMT  
		Size: 94.3 KB (94280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4755fffd5924e8405adfbed0f328ad9792eff20e2b8ad2025e1f5c85bca88618`  
		Last Modified: Thu, 18 Dec 2025 01:35:09 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.23` - linux; riscv64

```console
$ docker pull memcached@sha256:9023f4a863c531a74c6ff8cc3b49c3be80ad1db07cc93fdcbf87c5d8e4cccc72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5768619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2159b7b74e5ffe77e6304def07dec2cfc2bdead26c3012e1e4d39bcd267adfe5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 06:39:34 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 06:39:38 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 06:52:53 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 06:52:53 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 06:52:53 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 06:52:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 06:52:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 06:52:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 06:52:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 06:52:53 GMT
USER memcache
# Thu, 18 Dec 2025 06:52:53 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 06:52:53 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc016d1883c21894ae540944be0270a95cb663037e8592a944bac62e0cc39e7`  
		Last Modified: Thu, 18 Dec 2025 06:53:25 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c580cd51da178bea3e44467f8b445f50ec9272e42e0254d269a9e38204b12dc`  
		Last Modified: Thu, 18 Dec 2025 06:53:25 GMT  
		Size: 108.9 KB (108898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11881c79ebc6a05357f0e2095f00d6d5a8a58bd9f11efeefc80b616d0230ff9`  
		Last Modified: Thu, 18 Dec 2025 06:53:25 GMT  
		Size: 2.1 MB (2074429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735bfa953d895df9672fe0b34207075bd7e686f71104973ad4e02d89db8719a9`  
		Last Modified: Thu, 18 Dec 2025 06:53:25 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b8c865432ff9b07178ba7cb96426e0515b00cc91866fb4dfb8c243e4187172`  
		Last Modified: Thu, 18 Dec 2025 06:53:25 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:7cd6a8f4c278ff9062def241e6cdb501032ed72b091608a6da35812eece0954c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38b0c310a1ad4186c4beae0e268b71f1a80ed998cd80ceb81095aa9da7e6b02e`

```dockerfile
```

-	Layers:
	-	`sha256:88642ee1ee3c124ff8f2f640525172206ce9483620a70142ca673e0eca181c4d`  
		Last Modified: Thu, 18 Dec 2025 07:34:34 GMT  
		Size: 94.3 KB (94276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:441bda294fdd657b4574cd5337193125e3d0565433a700136501a858fce53d46`  
		Last Modified: Thu, 18 Dec 2025 07:34:34 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.23` - linux; s390x

```console
$ docker pull memcached@sha256:e011484878fd5d1e2da6de478ac11d01ae80f0bdef1902dcde3ed53728803741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5857090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:689ea71c305b80e206c68a215481290a1378e6375e32ad059455f7d041396aa6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:30:26 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:30:27 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:33:46 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:33:46 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:33:46 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:33:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:33:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:33:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:33:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:33:46 GMT
USER memcache
# Thu, 18 Dec 2025 00:33:46 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:33:46 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4594a6826f7ed03c8c4f9f2aebb9716eb6e16d5b5ab7e1bc247783b503c5b10`  
		Last Modified: Thu, 18 Dec 2025 00:33:55 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f270744f8d8b82bc6657387109b33836a76d6dbf8faa645a997db7ea290cdb`  
		Last Modified: Thu, 18 Dec 2025 00:33:55 GMT  
		Size: 114.3 KB (114299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91f8ee8f36703944a7bdcaf57cc5772fe9f79c74a088c33fa1b6da7de119f93`  
		Last Modified: Thu, 18 Dec 2025 00:33:55 GMT  
		Size: 2.0 MB (2017131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e21d2db88668745770273c7b36d4d2c1e87a80b0118b8d775813860b467384c8`  
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd847159e169b898a67d4454fd5a22406c5ae623b16889d084a1d5f2d46a499`  
		Last Modified: Thu, 18 Dec 2025 00:33:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:33ab737cb23dcde22de59a58e40f1f80d2c5e808ff3036519ae7d9db228fa37d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3562f7fd7806da24b1865c01a2246ac041b5e98d69c10ce6cbbe479f9408f9a1`

```dockerfile
```

-	Layers:
	-	`sha256:d5f43e64a79ee525bd0354a06e3284444fd642bbe6c1a782aa45ec2e20462f1d`  
		Last Modified: Thu, 18 Dec 2025 01:35:19 GMT  
		Size: 94.2 KB (94222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bd2c024010f4f53d350bde9967c349efb3a58a2a812b14e17b29ddbd19eab87`  
		Last Modified: Thu, 18 Dec 2025 01:35:20 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-trixie`

```console
$ docker pull memcached@sha256:e4e5eca37e4334f9579f10fcdd88a58c4eb9d0a8eacedde6ec49d4ea4391637a
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
$ docker pull memcached@sha256:1613c35e314db0c64d8b5679786ad99ced10069c3f9778d40b6c522ff3c04218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32190619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a38251b773d15614da3036dd0d756bbf4a7d16d27fe1c52023517a419372b245`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:22:30 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 13 Jan 2026 01:22:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:25:18 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 13 Jan 2026 01:25:18 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 13 Jan 2026 01:25:18 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 13 Jan 2026 01:25:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 13 Jan 2026 01:25:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:25:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 01:25:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:25:18 GMT
USER memcache
# Tue, 13 Jan 2026 01:25:18 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 13 Jan 2026 01:25:18 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:34 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b6e737e1a3eed198cc17e2b92231ab084bcf55ba90a36136e7a2f4fd04a95b`  
		Last Modified: Tue, 13 Jan 2026 01:25:30 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16835fec399670b74d32630a7368a65ca2a3c32d8b7a690d33bebc7b9e9458d`  
		Last Modified: Tue, 13 Jan 2026 01:25:30 GMT  
		Size: 136.7 KB (136737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c848acbad27f1c9d2fd95e0facabbb28d5d8be19e5fa5912e5474c1301522523`  
		Last Modified: Tue, 13 Jan 2026 01:25:25 GMT  
		Size: 2.3 MB (2278686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9529916038b7840d3177e93bf04b78390bb91bca78623bd9c0769f9e2a965079`  
		Last Modified: Tue, 13 Jan 2026 01:25:25 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24239fc168f5eb73ae9964e2cdcb3c3b878ae79835c6b94585cb648fd50479d`  
		Last Modified: Tue, 13 Jan 2026 01:25:26 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:0d72ad7b507d17cffe5dbec1ddecf1c254c3a85d2b605fa0ddbc9913ba4fc678
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe582f0cad77d385a3debb0f2acf0c96b7b85c6a7d2c95fcc54f938d63635c9`

```dockerfile
```

-	Layers:
	-	`sha256:7d598d8c3b4cd06481693da06e86554144167d205cc60f43382fafba94dd4592`  
		Last Modified: Tue, 13 Jan 2026 04:35:37 GMT  
		Size: 2.0 MB (2008290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dd2469227ab0e75822eb9d56a5d7c05f52a445840f65934e010a2562e509718`  
		Last Modified: Tue, 13 Jan 2026 01:25:24 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; arm variant v5

```console
$ docker pull memcached@sha256:efa6728c05b024b605597e5025f04155aab614b52f56b1b31a4c70a23f909e07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30298859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14119dc07998a4322ac912beaaf4e6ad16e5487f2243c332fdaad86bdce6f55e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:19:21 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 13 Jan 2026 01:19:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:22:43 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 13 Jan 2026 01:22:43 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 13 Jan 2026 01:22:43 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 13 Jan 2026 01:22:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 13 Jan 2026 01:22:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:22:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 01:22:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:22:43 GMT
USER memcache
# Tue, 13 Jan 2026 01:22:43 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 13 Jan 2026 01:22:43 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c113d410d30c2c035a105b56d3937958c81fbe2530f44add3bae903be6864324`  
		Last Modified: Tue, 13 Jan 2026 00:42:30 GMT  
		Size: 27.9 MB (27942724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96776850dc1206c3fd163b84cea19599306159eb0d020b4241d0172240f88d13`  
		Last Modified: Tue, 13 Jan 2026 01:22:55 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3697c7c790d9c4caaa904abdaf809dcdee3f0b518fc5ad82d2e21dd7fe24f64d`  
		Last Modified: Tue, 13 Jan 2026 01:22:55 GMT  
		Size: 144.2 KB (144212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a247339c7ec57a491c3ffe43531dbfaa132f3ff16a481fc41cbb9e3e3ad6476`  
		Last Modified: Tue, 13 Jan 2026 01:22:50 GMT  
		Size: 2.2 MB (2210412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2dcebe3ab2a9945cdea142301e4a64eebbc59c948a54385dbfca4afd561b508`  
		Last Modified: Tue, 13 Jan 2026 01:22:55 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb8ef5ecbc44efd5280f9cf15687dfd80a34fa2966ad039238647177f75dc6c`  
		Last Modified: Tue, 13 Jan 2026 01:22:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:190bb1ecd7376720e541621921c2d4931a9d0f85a047255ba2b56afa3a504212
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9736e9545a46e4ef65dcb5238691292d27fac4dccb330354ce59ac93ae6994b5`

```dockerfile
```

-	Layers:
	-	`sha256:4f5461bf596f750b56b3f10e315936c2326b2c32901d28cdf22db97072bba685`  
		Last Modified: Tue, 13 Jan 2026 01:22:50 GMT  
		Size: 2.0 MB (2011293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8657d28d0436d39193457fb90119ea6e4ddb566df2a83fd1aa9df75651731188`  
		Last Modified: Tue, 13 Jan 2026 04:35:43 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; arm variant v7

```console
$ docker pull memcached@sha256:9c322c838b4648fa30e742e53ed6647a31383760fb73fa82de32b4b6dc88c494
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28509532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6e130248535c57fccff4d89a9d442e31cabd471e41c9eed52e5207a54f9f944`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:25:47 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 13 Jan 2026 01:25:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:28:55 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 13 Jan 2026 01:28:55 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 13 Jan 2026 01:28:55 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 13 Jan 2026 01:28:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 13 Jan 2026 01:28:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:28:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 01:28:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:28:55 GMT
USER memcache
# Tue, 13 Jan 2026 01:28:55 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 13 Jan 2026 01:28:55 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029a2cbe46c1e12ab6d47a63f40fb29056b6c6277c7822085ed0fe62e0a1791d`  
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c7827f95482598f1bd32dd8cbe071ad009795fa108661234eeb872d1a1e8bd`  
		Last Modified: Tue, 13 Jan 2026 01:29:07 GMT  
		Size: 135.4 KB (135398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9371e974781bd91adc657086f00cd7d91b5530ca9da37597c347dd7d4eaff0`  
		Last Modified: Tue, 13 Jan 2026 01:29:07 GMT  
		Size: 2.2 MB (2164040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c2e0f64c0afa16b5e214ae208c8c81e8c78c79ddd90f54983a93c7297395f6b`  
		Last Modified: Tue, 13 Jan 2026 01:29:07 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92151d443057f88ed7f60405440b698ff9e6abe1a2ca1c91a0c7e7626339ad2`  
		Last Modified: Tue, 13 Jan 2026 01:29:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:12cc31a1ce56d2c6dd1c0dcfd4ef1fe74484985d010594950c086c0f4431559b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b2d844d5393973080c37fde0b92cd48bd1a64e03973290631be5486d814de7e`

```dockerfile
```

-	Layers:
	-	`sha256:99fc27444c1ccdd6cbd08a33aac22e9e85f55958bda7b6216bdea08eae374cff`  
		Last Modified: Tue, 13 Jan 2026 04:35:47 GMT  
		Size: 2.0 MB (2009750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e76d5584f581b7668c61a661da2858bc1d5e11b31e3629e0d2b3af52d9c22ed8`  
		Last Modified: Tue, 13 Jan 2026 04:35:47 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:2ed537fa0376a3eb0864d6a3b51ea7da59b9ff4bb3270189a8a5082f02f811e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32550406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf26d75d787aabbd202c97db1079b96e45105d3ca509a1001ab973cb473cae8c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:22:29 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 13 Jan 2026 01:22:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:25:26 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 13 Jan 2026 01:25:26 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 13 Jan 2026 01:25:26 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 13 Jan 2026 01:25:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 13 Jan 2026 01:25:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:25:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 01:25:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:25:27 GMT
USER memcache
# Tue, 13 Jan 2026 01:25:27 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 13 Jan 2026 01:25:27 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78edb6b991369235f90958a936afc89dc37b82439c632988ed143b5bd76deadb`  
		Last Modified: Tue, 13 Jan 2026 01:25:40 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e1afbb765f6cc3923e864d44fb6cd6c9167b884e596b09bd37c7c276f65a2b`  
		Last Modified: Tue, 13 Jan 2026 01:25:40 GMT  
		Size: 153.5 KB (153512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff9edc68fe57c233001afd442eb6c248bf070d32fbb412a8bfeef6f9a6217f5`  
		Last Modified: Tue, 13 Jan 2026 01:25:40 GMT  
		Size: 2.3 MB (2261341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c4648fbc4a4189184946895d1041e0eee2c5d40fd70638a553bedb0cbf5cf8`  
		Last Modified: Tue, 13 Jan 2026 01:25:40 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26bd1b32b048e73091ddf6e6762e368d4bb6ef2cc7d3aa43467749b36fe08e38`  
		Last Modified: Tue, 13 Jan 2026 01:25:40 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:72333c6222fb20b5a9f9f92b8d56c47ebb5b4e6cd65512a6b5172ad0c0cade67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a2a4e23cbe2d062f3fcfb84c8590190eb72294786a0b8238add858e67a93914`

```dockerfile
```

-	Layers:
	-	`sha256:1f8545bcc66309a59381c88c4c87b0f8352893dbaa167be48947976c1e0cef1d`  
		Last Modified: Tue, 13 Jan 2026 04:35:51 GMT  
		Size: 2.0 MB (2008606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95e6875e372e1d6a9660c08726cb96d08b272e52a2446f275089efccfc3096b3`  
		Last Modified: Tue, 13 Jan 2026 01:25:33 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; 386

```console
$ docker pull memcached@sha256:29540e588e9065db9ecc8865fe74544260980d73786f00dfc4df3f3cee148bd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33661194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66843ae7a7d968c4f056a8e350dd84ff80a06e48b48c298c3427333b7ec259ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:19:43 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 13 Jan 2026 01:19:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:22:40 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 13 Jan 2026 01:22:40 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 13 Jan 2026 01:22:40 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 13 Jan 2026 01:22:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 13 Jan 2026 01:22:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:22:40 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 01:22:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:22:40 GMT
USER memcache
# Tue, 13 Jan 2026 01:22:40 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 13 Jan 2026 01:22:40 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:27bb6d39eda5ced7626db280c3902aacdfade5acd11a16ef9618e3185f69b102`  
		Last Modified: Tue, 13 Jan 2026 00:43:03 GMT  
		Size: 31.3 MB (31288476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cedb4f2840edea9de46e0d955a0512f469211880560a8948f10b54381bcd728`  
		Last Modified: Tue, 13 Jan 2026 01:22:53 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c4b2d1574ee5f238dc6948164abd39ffcc91929b2c464c6b3874dec01fd964`  
		Last Modified: Tue, 13 Jan 2026 01:22:46 GMT  
		Size: 147.6 KB (147554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc1bf5870b84175607f3d012b3cfebc5859869f8125114ea5d6ed1a05f81d2d`  
		Last Modified: Tue, 13 Jan 2026 01:22:53 GMT  
		Size: 2.2 MB (2223652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6434e73ed67e81f1016f27c7cc175290b0ce959d8a1bf5e9b0f3119f161246`  
		Last Modified: Tue, 13 Jan 2026 01:22:53 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abaf99fdf0e2b9620d20088b389b3f18eb67ad356c8c6c7961074e1428b8af0c`  
		Last Modified: Tue, 13 Jan 2026 01:22:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:f64192985f4635b04ce1ab99b3cae89f71d0b11f9670fb6d9c470158e3c5c63e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bb9ce834f23725c4bfc4fb2d6a24a96d3d0bc7685d3a759c0085871f34231e8`

```dockerfile
```

-	Layers:
	-	`sha256:ed9937c762728e5abc93b88bd7932a5762d2bc8e0001e81bb25ef0b27e2bc6ff`  
		Last Modified: Tue, 13 Jan 2026 04:35:56 GMT  
		Size: 2.0 MB (2005447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6358862e12c5c5367efd52bea0b1194e04e76f267084da591229f64ee7482dc3`  
		Last Modified: Tue, 13 Jan 2026 04:35:57 GMT  
		Size: 22.1 KB (22094 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; ppc64le

```console
$ docker pull memcached@sha256:309e0faad388272d7e37d6ee0cb354707d099e3140298105499711823d7a0eea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36161489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6f50ee10fc83da67b90c9bda7499251fa073fea87400d5fb70e31e693d6f902`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:33:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 13 Jan 2026 01:33:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:36:52 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 13 Jan 2026 01:36:52 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 13 Jan 2026 01:36:52 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 13 Jan 2026 01:36:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 13 Jan 2026 01:36:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:36:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 01:36:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:36:53 GMT
USER memcache
# Tue, 13 Jan 2026 01:36:53 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 13 Jan 2026 01:36:53 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9a275bb13cf8b3e9db52a41b6b4ff22ee1ffed00394f6deddd2de45044bd3bae`  
		Last Modified: Tue, 13 Jan 2026 00:57:13 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093e59deb53ff01a892be2a5df928c4b04a289df7f6c135570c11d6a4fdbc53a`  
		Last Modified: Tue, 13 Jan 2026 01:37:16 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4da25c8b13ee47050a38843c1954d2bd7bbdba2666f725aee2f603e03fcb6d`  
		Last Modified: Tue, 13 Jan 2026 01:37:16 GMT  
		Size: 170.4 KB (170427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cab5f6f805c735c0f324c87ff8c66cfab0e35fb691b7761e85bb9a2bbb31cfe`  
		Last Modified: Tue, 13 Jan 2026 01:37:16 GMT  
		Size: 2.4 MB (2393947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3a7dfc8da65bd6101de156530bc2688c5588c718bbc3131ff4594cbefd0e66`  
		Last Modified: Tue, 13 Jan 2026 01:37:09 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06153b2e2bde9b06f1c2719aabb5ff6a6c23056152a024fa2c990d97b4d9c799`  
		Last Modified: Tue, 13 Jan 2026 01:37:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:8dfcc685b38edcaec140b90716d19e543715184f20f7a401d6f734ad8f8cf1dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7442b6e23a86bfe5ee9a534d43f0a55ba9629d3c24128b1b3e2b5121644dcf00`

```dockerfile
```

-	Layers:
	-	`sha256:a4b6027eed506a371ad9a2314b6be299e5c509b4c4be66e5842b29837171b0cf`  
		Last Modified: Tue, 13 Jan 2026 04:36:00 GMT  
		Size: 2.0 MB (2011891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc718b3aa0399c50248bba6165cad8666196a5351b6ed095a8101d2f8a5d37da`  
		Last Modified: Tue, 13 Jan 2026 04:36:01 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; riscv64

```console
$ docker pull memcached@sha256:bce857473a0aeeec89bc5383841d05d99df2b89bba49caf3059874a9442ff224
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30613806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc8f84b5bfd0d6518442de566ffa39b2113651446c246e419f61a8e5fa68e87`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Wed, 14 Jan 2026 06:36:03 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 14 Jan 2026 06:36:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jan 2026 06:49:42 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 14 Jan 2026 06:49:42 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 14 Jan 2026 06:49:42 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 14 Jan 2026 06:49:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 14 Jan 2026 06:49:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 06:49:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 14 Jan 2026 06:49:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 06:49:43 GMT
USER memcache
# Wed, 14 Jan 2026 06:49:43 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 14 Jan 2026 06:49:43 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7c6f79d4d52450222a8a38f8fc98e229a4711a246fc94fdaaab31930d3135d`  
		Last Modified: Wed, 14 Jan 2026 06:50:36 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168d1b37fe07dfb8bef5240057ad6597058647499a9e771eedd2091f2d6b30f0`  
		Last Modified: Wed, 14 Jan 2026 06:50:36 GMT  
		Size: 133.1 KB (133105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a5ebc1ef49cab24f75e0c751a1e0563ee042c246c509279fa38cf3cbf0a3f1`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 2.2 MB (2207499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbc8df7ca1d2f273c3c8fec55b30f17ebc72a45687976efd9c8779a66369d46`  
		Last Modified: Wed, 14 Jan 2026 06:50:36 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4057c9476d421ae1ecae3607afb0db57dbc6eb2bc0aa5e41daed169a70319c1`  
		Last Modified: Wed, 14 Jan 2026 06:50:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:75823016a946bfe52b08e1f80032a64b0202a08f2e30dd8cb7035a01e1244518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b86887925c9eccb39ad75807a81768a06591c668cfd4bf4af00a40b2414f22bc`

```dockerfile
```

-	Layers:
	-	`sha256:0d93e934848935cdae8d83be9ebaff197aaa6e70f5b224c2107461561ea0064d`  
		Last Modified: Wed, 14 Jan 2026 07:34:47 GMT  
		Size: 2.0 MB (2002254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0de5bd0cbff9df1fc11e05bd38936b6915195663b273b5c23840bf5eb9373a8`  
		Last Modified: Wed, 14 Jan 2026 07:34:48 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; s390x

```console
$ docker pull memcached@sha256:46c34c0b238fbae2980413fe2b6590839b6afbc43e0a1e07eb456fc274eaf811
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32272852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8666231b78b1bdfb283fe302437321dedf8ecc2d869ff2acdce9f8461f285519`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 14:13:49 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 13 Jan 2026 14:13:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 14:16:57 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 13 Jan 2026 14:16:57 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 13 Jan 2026 14:16:57 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 13 Jan 2026 14:16:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 13 Jan 2026 14:16:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 14:16:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 14:16:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 14:16:57 GMT
USER memcache
# Tue, 13 Jan 2026 14:16:57 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 13 Jan 2026 14:16:57 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2b46bc94baaae0a37e5e04b1babf7e1f37c4390b83d49c3c6820188deba770e3`  
		Last Modified: Tue, 13 Jan 2026 13:10:43 GMT  
		Size: 29.8 MB (29833411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2727771ad16d920baecb7c96b9b54e67178369b881fc20901d381dfd5f873e27`  
		Last Modified: Tue, 13 Jan 2026 14:17:12 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6b0ec5581f8591522a6327cdcfa4e1197d9ada9fb60840f57b5d3e4dd3304d1`  
		Last Modified: Tue, 13 Jan 2026 14:17:12 GMT  
		Size: 140.6 KB (140562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382a3e1ebed70673a0789fcc2104ab941fe04b9a020339f9286ac85b67ae5ff9`  
		Last Modified: Tue, 13 Jan 2026 14:17:13 GMT  
		Size: 2.3 MB (2297368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85fe5f9afd355e3dd76ce942e1c295e356d96ae3b0e3f8236a0e33c5f75ffe71`  
		Last Modified: Tue, 13 Jan 2026 14:17:08 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4546f3c3457928dc273f98dae7c7ac2f945b203138e964ee72fc92aabcef434`  
		Last Modified: Tue, 13 Jan 2026 14:17:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:d620668087c443f58d215a372a70eb0697c7031777d3537d244fa26e62d3ec3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e48c5956bcfcf63509c135da7076a0f247bc2858c7df68331b5a112e937ff6c`

```dockerfile
```

-	Layers:
	-	`sha256:507d45d8f4547a846c07788edb1628f89b93ac7616169374be23f29601b7be68`  
		Last Modified: Tue, 13 Jan 2026 14:17:08 GMT  
		Size: 2.0 MB (2009727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78fdd8684e48fc4ee1817e00df577a38250864ffbcf34ec341937d525d9dfabd`  
		Last Modified: Tue, 13 Jan 2026 16:34:40 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.40`

```console
$ docker pull memcached@sha256:e4e5eca37e4334f9579f10fcdd88a58c4eb9d0a8eacedde6ec49d4ea4391637a
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

### `memcached:1.6.40` - linux; amd64

```console
$ docker pull memcached@sha256:1613c35e314db0c64d8b5679786ad99ced10069c3f9778d40b6c522ff3c04218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32190619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a38251b773d15614da3036dd0d756bbf4a7d16d27fe1c52023517a419372b245`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:22:30 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 13 Jan 2026 01:22:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:25:18 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 13 Jan 2026 01:25:18 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 13 Jan 2026 01:25:18 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 13 Jan 2026 01:25:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 13 Jan 2026 01:25:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:25:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 01:25:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:25:18 GMT
USER memcache
# Tue, 13 Jan 2026 01:25:18 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 13 Jan 2026 01:25:18 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:34 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b6e737e1a3eed198cc17e2b92231ab084bcf55ba90a36136e7a2f4fd04a95b`  
		Last Modified: Tue, 13 Jan 2026 01:25:30 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16835fec399670b74d32630a7368a65ca2a3c32d8b7a690d33bebc7b9e9458d`  
		Last Modified: Tue, 13 Jan 2026 01:25:30 GMT  
		Size: 136.7 KB (136737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c848acbad27f1c9d2fd95e0facabbb28d5d8be19e5fa5912e5474c1301522523`  
		Last Modified: Tue, 13 Jan 2026 01:25:25 GMT  
		Size: 2.3 MB (2278686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9529916038b7840d3177e93bf04b78390bb91bca78623bd9c0769f9e2a965079`  
		Last Modified: Tue, 13 Jan 2026 01:25:25 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24239fc168f5eb73ae9964e2cdcb3c3b878ae79835c6b94585cb648fd50479d`  
		Last Modified: Tue, 13 Jan 2026 01:25:26 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40` - unknown; unknown

```console
$ docker pull memcached@sha256:0d72ad7b507d17cffe5dbec1ddecf1c254c3a85d2b605fa0ddbc9913ba4fc678
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe582f0cad77d385a3debb0f2acf0c96b7b85c6a7d2c95fcc54f938d63635c9`

```dockerfile
```

-	Layers:
	-	`sha256:7d598d8c3b4cd06481693da06e86554144167d205cc60f43382fafba94dd4592`  
		Last Modified: Tue, 13 Jan 2026 04:35:37 GMT  
		Size: 2.0 MB (2008290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dd2469227ab0e75822eb9d56a5d7c05f52a445840f65934e010a2562e509718`  
		Last Modified: Tue, 13 Jan 2026 01:25:24 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40` - linux; arm variant v5

```console
$ docker pull memcached@sha256:efa6728c05b024b605597e5025f04155aab614b52f56b1b31a4c70a23f909e07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30298859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14119dc07998a4322ac912beaaf4e6ad16e5487f2243c332fdaad86bdce6f55e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:19:21 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 13 Jan 2026 01:19:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:22:43 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 13 Jan 2026 01:22:43 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 13 Jan 2026 01:22:43 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 13 Jan 2026 01:22:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 13 Jan 2026 01:22:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:22:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 01:22:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:22:43 GMT
USER memcache
# Tue, 13 Jan 2026 01:22:43 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 13 Jan 2026 01:22:43 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c113d410d30c2c035a105b56d3937958c81fbe2530f44add3bae903be6864324`  
		Last Modified: Tue, 13 Jan 2026 00:42:30 GMT  
		Size: 27.9 MB (27942724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96776850dc1206c3fd163b84cea19599306159eb0d020b4241d0172240f88d13`  
		Last Modified: Tue, 13 Jan 2026 01:22:55 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3697c7c790d9c4caaa904abdaf809dcdee3f0b518fc5ad82d2e21dd7fe24f64d`  
		Last Modified: Tue, 13 Jan 2026 01:22:55 GMT  
		Size: 144.2 KB (144212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a247339c7ec57a491c3ffe43531dbfaa132f3ff16a481fc41cbb9e3e3ad6476`  
		Last Modified: Tue, 13 Jan 2026 01:22:50 GMT  
		Size: 2.2 MB (2210412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2dcebe3ab2a9945cdea142301e4a64eebbc59c948a54385dbfca4afd561b508`  
		Last Modified: Tue, 13 Jan 2026 01:22:55 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb8ef5ecbc44efd5280f9cf15687dfd80a34fa2966ad039238647177f75dc6c`  
		Last Modified: Tue, 13 Jan 2026 01:22:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40` - unknown; unknown

```console
$ docker pull memcached@sha256:190bb1ecd7376720e541621921c2d4931a9d0f85a047255ba2b56afa3a504212
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9736e9545a46e4ef65dcb5238691292d27fac4dccb330354ce59ac93ae6994b5`

```dockerfile
```

-	Layers:
	-	`sha256:4f5461bf596f750b56b3f10e315936c2326b2c32901d28cdf22db97072bba685`  
		Last Modified: Tue, 13 Jan 2026 01:22:50 GMT  
		Size: 2.0 MB (2011293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8657d28d0436d39193457fb90119ea6e4ddb566df2a83fd1aa9df75651731188`  
		Last Modified: Tue, 13 Jan 2026 04:35:43 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40` - linux; arm variant v7

```console
$ docker pull memcached@sha256:9c322c838b4648fa30e742e53ed6647a31383760fb73fa82de32b4b6dc88c494
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28509532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6e130248535c57fccff4d89a9d442e31cabd471e41c9eed52e5207a54f9f944`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:25:47 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 13 Jan 2026 01:25:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:28:55 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 13 Jan 2026 01:28:55 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 13 Jan 2026 01:28:55 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 13 Jan 2026 01:28:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 13 Jan 2026 01:28:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:28:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 01:28:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:28:55 GMT
USER memcache
# Tue, 13 Jan 2026 01:28:55 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 13 Jan 2026 01:28:55 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029a2cbe46c1e12ab6d47a63f40fb29056b6c6277c7822085ed0fe62e0a1791d`  
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c7827f95482598f1bd32dd8cbe071ad009795fa108661234eeb872d1a1e8bd`  
		Last Modified: Tue, 13 Jan 2026 01:29:07 GMT  
		Size: 135.4 KB (135398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9371e974781bd91adc657086f00cd7d91b5530ca9da37597c347dd7d4eaff0`  
		Last Modified: Tue, 13 Jan 2026 01:29:07 GMT  
		Size: 2.2 MB (2164040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c2e0f64c0afa16b5e214ae208c8c81e8c78c79ddd90f54983a93c7297395f6b`  
		Last Modified: Tue, 13 Jan 2026 01:29:07 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92151d443057f88ed7f60405440b698ff9e6abe1a2ca1c91a0c7e7626339ad2`  
		Last Modified: Tue, 13 Jan 2026 01:29:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40` - unknown; unknown

```console
$ docker pull memcached@sha256:12cc31a1ce56d2c6dd1c0dcfd4ef1fe74484985d010594950c086c0f4431559b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b2d844d5393973080c37fde0b92cd48bd1a64e03973290631be5486d814de7e`

```dockerfile
```

-	Layers:
	-	`sha256:99fc27444c1ccdd6cbd08a33aac22e9e85f55958bda7b6216bdea08eae374cff`  
		Last Modified: Tue, 13 Jan 2026 04:35:47 GMT  
		Size: 2.0 MB (2009750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e76d5584f581b7668c61a661da2858bc1d5e11b31e3629e0d2b3af52d9c22ed8`  
		Last Modified: Tue, 13 Jan 2026 04:35:47 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:2ed537fa0376a3eb0864d6a3b51ea7da59b9ff4bb3270189a8a5082f02f811e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32550406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf26d75d787aabbd202c97db1079b96e45105d3ca509a1001ab973cb473cae8c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:22:29 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 13 Jan 2026 01:22:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:25:26 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 13 Jan 2026 01:25:26 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 13 Jan 2026 01:25:26 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 13 Jan 2026 01:25:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 13 Jan 2026 01:25:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:25:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 01:25:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:25:27 GMT
USER memcache
# Tue, 13 Jan 2026 01:25:27 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 13 Jan 2026 01:25:27 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78edb6b991369235f90958a936afc89dc37b82439c632988ed143b5bd76deadb`  
		Last Modified: Tue, 13 Jan 2026 01:25:40 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e1afbb765f6cc3923e864d44fb6cd6c9167b884e596b09bd37c7c276f65a2b`  
		Last Modified: Tue, 13 Jan 2026 01:25:40 GMT  
		Size: 153.5 KB (153512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff9edc68fe57c233001afd442eb6c248bf070d32fbb412a8bfeef6f9a6217f5`  
		Last Modified: Tue, 13 Jan 2026 01:25:40 GMT  
		Size: 2.3 MB (2261341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c4648fbc4a4189184946895d1041e0eee2c5d40fd70638a553bedb0cbf5cf8`  
		Last Modified: Tue, 13 Jan 2026 01:25:40 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26bd1b32b048e73091ddf6e6762e368d4bb6ef2cc7d3aa43467749b36fe08e38`  
		Last Modified: Tue, 13 Jan 2026 01:25:40 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40` - unknown; unknown

```console
$ docker pull memcached@sha256:72333c6222fb20b5a9f9f92b8d56c47ebb5b4e6cd65512a6b5172ad0c0cade67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a2a4e23cbe2d062f3fcfb84c8590190eb72294786a0b8238add858e67a93914`

```dockerfile
```

-	Layers:
	-	`sha256:1f8545bcc66309a59381c88c4c87b0f8352893dbaa167be48947976c1e0cef1d`  
		Last Modified: Tue, 13 Jan 2026 04:35:51 GMT  
		Size: 2.0 MB (2008606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95e6875e372e1d6a9660c08726cb96d08b272e52a2446f275089efccfc3096b3`  
		Last Modified: Tue, 13 Jan 2026 01:25:33 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40` - linux; 386

```console
$ docker pull memcached@sha256:29540e588e9065db9ecc8865fe74544260980d73786f00dfc4df3f3cee148bd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33661194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66843ae7a7d968c4f056a8e350dd84ff80a06e48b48c298c3427333b7ec259ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:19:43 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 13 Jan 2026 01:19:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:22:40 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 13 Jan 2026 01:22:40 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 13 Jan 2026 01:22:40 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 13 Jan 2026 01:22:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 13 Jan 2026 01:22:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:22:40 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 01:22:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:22:40 GMT
USER memcache
# Tue, 13 Jan 2026 01:22:40 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 13 Jan 2026 01:22:40 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:27bb6d39eda5ced7626db280c3902aacdfade5acd11a16ef9618e3185f69b102`  
		Last Modified: Tue, 13 Jan 2026 00:43:03 GMT  
		Size: 31.3 MB (31288476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cedb4f2840edea9de46e0d955a0512f469211880560a8948f10b54381bcd728`  
		Last Modified: Tue, 13 Jan 2026 01:22:53 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c4b2d1574ee5f238dc6948164abd39ffcc91929b2c464c6b3874dec01fd964`  
		Last Modified: Tue, 13 Jan 2026 01:22:46 GMT  
		Size: 147.6 KB (147554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc1bf5870b84175607f3d012b3cfebc5859869f8125114ea5d6ed1a05f81d2d`  
		Last Modified: Tue, 13 Jan 2026 01:22:53 GMT  
		Size: 2.2 MB (2223652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6434e73ed67e81f1016f27c7cc175290b0ce959d8a1bf5e9b0f3119f161246`  
		Last Modified: Tue, 13 Jan 2026 01:22:53 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abaf99fdf0e2b9620d20088b389b3f18eb67ad356c8c6c7961074e1428b8af0c`  
		Last Modified: Tue, 13 Jan 2026 01:22:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40` - unknown; unknown

```console
$ docker pull memcached@sha256:f64192985f4635b04ce1ab99b3cae89f71d0b11f9670fb6d9c470158e3c5c63e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bb9ce834f23725c4bfc4fb2d6a24a96d3d0bc7685d3a759c0085871f34231e8`

```dockerfile
```

-	Layers:
	-	`sha256:ed9937c762728e5abc93b88bd7932a5762d2bc8e0001e81bb25ef0b27e2bc6ff`  
		Last Modified: Tue, 13 Jan 2026 04:35:56 GMT  
		Size: 2.0 MB (2005447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6358862e12c5c5367efd52bea0b1194e04e76f267084da591229f64ee7482dc3`  
		Last Modified: Tue, 13 Jan 2026 04:35:57 GMT  
		Size: 22.1 KB (22094 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40` - linux; ppc64le

```console
$ docker pull memcached@sha256:309e0faad388272d7e37d6ee0cb354707d099e3140298105499711823d7a0eea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36161489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6f50ee10fc83da67b90c9bda7499251fa073fea87400d5fb70e31e693d6f902`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:33:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 13 Jan 2026 01:33:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:36:52 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 13 Jan 2026 01:36:52 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 13 Jan 2026 01:36:52 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 13 Jan 2026 01:36:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 13 Jan 2026 01:36:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:36:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 01:36:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:36:53 GMT
USER memcache
# Tue, 13 Jan 2026 01:36:53 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 13 Jan 2026 01:36:53 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9a275bb13cf8b3e9db52a41b6b4ff22ee1ffed00394f6deddd2de45044bd3bae`  
		Last Modified: Tue, 13 Jan 2026 00:57:13 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093e59deb53ff01a892be2a5df928c4b04a289df7f6c135570c11d6a4fdbc53a`  
		Last Modified: Tue, 13 Jan 2026 01:37:16 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4da25c8b13ee47050a38843c1954d2bd7bbdba2666f725aee2f603e03fcb6d`  
		Last Modified: Tue, 13 Jan 2026 01:37:16 GMT  
		Size: 170.4 KB (170427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cab5f6f805c735c0f324c87ff8c66cfab0e35fb691b7761e85bb9a2bbb31cfe`  
		Last Modified: Tue, 13 Jan 2026 01:37:16 GMT  
		Size: 2.4 MB (2393947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3a7dfc8da65bd6101de156530bc2688c5588c718bbc3131ff4594cbefd0e66`  
		Last Modified: Tue, 13 Jan 2026 01:37:09 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06153b2e2bde9b06f1c2719aabb5ff6a6c23056152a024fa2c990d97b4d9c799`  
		Last Modified: Tue, 13 Jan 2026 01:37:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40` - unknown; unknown

```console
$ docker pull memcached@sha256:8dfcc685b38edcaec140b90716d19e543715184f20f7a401d6f734ad8f8cf1dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7442b6e23a86bfe5ee9a534d43f0a55ba9629d3c24128b1b3e2b5121644dcf00`

```dockerfile
```

-	Layers:
	-	`sha256:a4b6027eed506a371ad9a2314b6be299e5c509b4c4be66e5842b29837171b0cf`  
		Last Modified: Tue, 13 Jan 2026 04:36:00 GMT  
		Size: 2.0 MB (2011891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc718b3aa0399c50248bba6165cad8666196a5351b6ed095a8101d2f8a5d37da`  
		Last Modified: Tue, 13 Jan 2026 04:36:01 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40` - linux; riscv64

```console
$ docker pull memcached@sha256:bce857473a0aeeec89bc5383841d05d99df2b89bba49caf3059874a9442ff224
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30613806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc8f84b5bfd0d6518442de566ffa39b2113651446c246e419f61a8e5fa68e87`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Wed, 14 Jan 2026 06:36:03 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 14 Jan 2026 06:36:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jan 2026 06:49:42 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 14 Jan 2026 06:49:42 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 14 Jan 2026 06:49:42 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 14 Jan 2026 06:49:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 14 Jan 2026 06:49:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 06:49:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 14 Jan 2026 06:49:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 06:49:43 GMT
USER memcache
# Wed, 14 Jan 2026 06:49:43 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 14 Jan 2026 06:49:43 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7c6f79d4d52450222a8a38f8fc98e229a4711a246fc94fdaaab31930d3135d`  
		Last Modified: Wed, 14 Jan 2026 06:50:36 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168d1b37fe07dfb8bef5240057ad6597058647499a9e771eedd2091f2d6b30f0`  
		Last Modified: Wed, 14 Jan 2026 06:50:36 GMT  
		Size: 133.1 KB (133105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a5ebc1ef49cab24f75e0c751a1e0563ee042c246c509279fa38cf3cbf0a3f1`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 2.2 MB (2207499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbc8df7ca1d2f273c3c8fec55b30f17ebc72a45687976efd9c8779a66369d46`  
		Last Modified: Wed, 14 Jan 2026 06:50:36 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4057c9476d421ae1ecae3607afb0db57dbc6eb2bc0aa5e41daed169a70319c1`  
		Last Modified: Wed, 14 Jan 2026 06:50:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40` - unknown; unknown

```console
$ docker pull memcached@sha256:75823016a946bfe52b08e1f80032a64b0202a08f2e30dd8cb7035a01e1244518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b86887925c9eccb39ad75807a81768a06591c668cfd4bf4af00a40b2414f22bc`

```dockerfile
```

-	Layers:
	-	`sha256:0d93e934848935cdae8d83be9ebaff197aaa6e70f5b224c2107461561ea0064d`  
		Last Modified: Wed, 14 Jan 2026 07:34:47 GMT  
		Size: 2.0 MB (2002254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0de5bd0cbff9df1fc11e05bd38936b6915195663b273b5c23840bf5eb9373a8`  
		Last Modified: Wed, 14 Jan 2026 07:34:48 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40` - linux; s390x

```console
$ docker pull memcached@sha256:46c34c0b238fbae2980413fe2b6590839b6afbc43e0a1e07eb456fc274eaf811
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32272852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8666231b78b1bdfb283fe302437321dedf8ecc2d869ff2acdce9f8461f285519`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 14:13:49 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 13 Jan 2026 14:13:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 14:16:57 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 13 Jan 2026 14:16:57 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 13 Jan 2026 14:16:57 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 13 Jan 2026 14:16:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 13 Jan 2026 14:16:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 14:16:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 14:16:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 14:16:57 GMT
USER memcache
# Tue, 13 Jan 2026 14:16:57 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 13 Jan 2026 14:16:57 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2b46bc94baaae0a37e5e04b1babf7e1f37c4390b83d49c3c6820188deba770e3`  
		Last Modified: Tue, 13 Jan 2026 13:10:43 GMT  
		Size: 29.8 MB (29833411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2727771ad16d920baecb7c96b9b54e67178369b881fc20901d381dfd5f873e27`  
		Last Modified: Tue, 13 Jan 2026 14:17:12 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6b0ec5581f8591522a6327cdcfa4e1197d9ada9fb60840f57b5d3e4dd3304d1`  
		Last Modified: Tue, 13 Jan 2026 14:17:12 GMT  
		Size: 140.6 KB (140562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382a3e1ebed70673a0789fcc2104ab941fe04b9a020339f9286ac85b67ae5ff9`  
		Last Modified: Tue, 13 Jan 2026 14:17:13 GMT  
		Size: 2.3 MB (2297368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85fe5f9afd355e3dd76ce942e1c295e356d96ae3b0e3f8236a0e33c5f75ffe71`  
		Last Modified: Tue, 13 Jan 2026 14:17:08 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4546f3c3457928dc273f98dae7c7ac2f945b203138e964ee72fc92aabcef434`  
		Last Modified: Tue, 13 Jan 2026 14:17:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40` - unknown; unknown

```console
$ docker pull memcached@sha256:d620668087c443f58d215a372a70eb0697c7031777d3537d244fa26e62d3ec3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e48c5956bcfcf63509c135da7076a0f247bc2858c7df68331b5a112e937ff6c`

```dockerfile
```

-	Layers:
	-	`sha256:507d45d8f4547a846c07788edb1628f89b93ac7616169374be23f29601b7be68`  
		Last Modified: Tue, 13 Jan 2026 14:17:08 GMT  
		Size: 2.0 MB (2009727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78fdd8684e48fc4ee1817e00df577a38250864ffbcf34ec341937d525d9dfabd`  
		Last Modified: Tue, 13 Jan 2026 16:34:40 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.40-alpine`

```console
$ docker pull memcached@sha256:c77536380fd3c7740933767bb5279bd30e31c8d496081e5113a37d9b9eec43cb
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

### `memcached:1.6.40-alpine` - linux; amd64

```console
$ docker pull memcached@sha256:9573a2399011fa86bb7b5d12bdab987d7931c98ddec0ef6802de7eb6d3c3e338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5956768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c79853acc5f24e9c28f15d45cef0aedc114e76bbacf7958eb6f555c22246e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:34 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:29:34 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:32:07 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:32:07 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:32:07 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:32:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:32:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:32:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:32:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:32:07 GMT
USER memcache
# Thu, 18 Dec 2025 00:32:07 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:32:07 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:48:50 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57c33ac8581cd04f31208409f36331e938a78e6ae3a7a3b530fe9dfebe6eb9ad`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583aae99135b9036c602a1c60743fc4fd519f261ac6d48ed60b01e1beb019e7f`  
		Last Modified: Thu, 18 Dec 2025 00:32:12 GMT  
		Size: 106.0 KB (106050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ca22885c42a537f033850e8dff7eaeddbb7514902286739b48c084b55a8d6b`  
		Last Modified: Thu, 18 Dec 2025 00:32:12 GMT  
		Size: 2.0 MB (1989265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d146e2038834770bed57033a6c5d66ead5b731b8b133856dec6726ca21baee9`  
		Last Modified: Thu, 18 Dec 2025 00:32:12 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c66e6c3acbe07806e3e96a97d97a2d4503713c4814d9b24a2f57f2c39200d05`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:cfdf2ea6bf2a04bb7ee1568efe0c8bd38a1f5e644250a9409479cce281891ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de792623281192b3965fdc95f31532c4d166e731f53e202be1e2a224c654633b`

```dockerfile
```

-	Layers:
	-	`sha256:87a0d23eeeda6353dfc603cc4ffee062e5383be07b611754f3a88db3fc644036`  
		Last Modified: Thu, 18 Dec 2025 00:32:12 GMT  
		Size: 94.9 KB (94873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b73cd5efe31baa1fbf0eecea269426edcfc795cbb9b5dd74b523ff51b6f7c9f`  
		Last Modified: Thu, 18 Dec 2025 01:34:48 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:c1a12b64cc8b47f50ea4610d9c1c362da7157b3ba67deac8b4760e6b589cde75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5611647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3591f95cad049a0509bd23a95556f8f848452d2a5491ed00bae293897c7a6b2f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:27:48 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:27:49 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:49:50 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:49:50 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:49:50 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:49:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:49:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:49:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:49:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:49:50 GMT
USER memcache
# Thu, 18 Dec 2025 00:49:50 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:49:50 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf585eb2bfa372c2097b9f7a5214ecb0941a30581b10fb74a26518fcc7addec`  
		Last Modified: Thu, 18 Dec 2025 00:49:55 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01bb148ea8fbe93dd8097d85f9ee3cf547d314e669748b4239c05711b0d5f719`  
		Last Modified: Thu, 18 Dec 2025 00:49:55 GMT  
		Size: 102.7 KB (102652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6549359cda37ac41cf41a5ece5f37f1322a82f6b232f12e446c62840637093e`  
		Last Modified: Thu, 18 Dec 2025 00:50:02 GMT  
		Size: 1.9 MB (1939215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:041e37eaffefcfb0809564ddea591be3cd818de5530e2c853c0bc9a2fa25c116`  
		Last Modified: Thu, 18 Dec 2025 00:49:55 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7907ae218c75b36c9a9002be8554131c271cde78b0280cb7a85029f99ad0bcdc`  
		Last Modified: Thu, 18 Dec 2025 00:50:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:a9c26fc290551b691574e093d3c28f4fe7b558b3f8173b3c99eb8a664c83a8e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ca65d7156e6586d96310ea3162facd9849d5460d2939b461a25247b06a4d59`

```dockerfile
```

-	Layers:
	-	`sha256:d9c217dc241f1175812c47b6489d325a0574c0da554c6f8aa0b86a2d8aff05f9`  
		Last Modified: Thu, 18 Dec 2025 01:34:52 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:cee00a47bf7b8b5899a6cf1f5c692494df31b454f52b81f3c4886905a0c9bdd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5270304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d91d78dbe118f2b7b0d6e850e1115de72c4fe3e30c55a5b53d8a844d14357d16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:30:56 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:30:57 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:33:51 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:33:51 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:33:51 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:33:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:33:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:33:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:33:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:33:51 GMT
USER memcache
# Thu, 18 Dec 2025 00:33:51 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:33:51 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:43 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa22c446792763e48f4680945ccc68d43c7906ef35a92e0b908f57ef53e72f0`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954155078f2265364295ebdf16fb114e991b1938d8a6951fb511163ab3b2b385`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 92.4 KB (92378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a25584b03ac5e45c66c3c616acfd9df1848e5db25219ef20feb2868c30c6332`  
		Last Modified: Thu, 18 Dec 2025 00:33:57 GMT  
		Size: 1.9 MB (1897191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f237be962bb57c3f749904b5925c8e1d7e9013dfac7dd52cc9611ada81858e`  
		Last Modified: Thu, 18 Dec 2025 00:33:57 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b07d9170b246a631c262d9f5d57f49278f7cd4805463b90b14aeca4dc61d93`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:64abe011fed6a9cf7b3290c752c50bffe81bb2e65cf6337e023efda87d49b451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b251b9c15ab7c5742bd3ab725df09f0ecb9f2491f92cf1c825bec598a31f4407`

```dockerfile
```

-	Layers:
	-	`sha256:1882c6d4361100a29fd5ab265587f65fa27b1df15e7f9349b30dac454facf98e`  
		Last Modified: Thu, 18 Dec 2025 00:33:57 GMT  
		Size: 94.3 KB (94291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf0a88ab3838de6beab653497ab62a64cfb87b1dc83c5fa5b6f3907abfd88080`  
		Last Modified: Thu, 18 Dec 2025 01:34:56 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:b6c3042e2bf09ec3d3f054d03b81313e8df717a49371ce916ff743e602796bc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6285509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6691028570bbd843e6da26558c46162b8383212fcaaefcecb2d3f919e3401429`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:18 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:29:19 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:32:06 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:32:06 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:32:06 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:32:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:32:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:32:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:32:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:32:06 GMT
USER memcache
# Thu, 18 Dec 2025 00:32:06 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:32:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb7b8445facedfc145b9478f74880f520776460f153005b7f437ec339aee530`  
		Last Modified: Thu, 18 Dec 2025 00:32:11 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1853c901134389608b6e80aaa3e43cd67a35c71aecfdde4b5b7ed3b989a03c`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 121.9 KB (121860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a01d1ac5ce47f4494363e411e1cd25dea26438213a2d18d6bb104d0974d9a52`  
		Last Modified: Thu, 18 Dec 2025 00:32:11 GMT  
		Size: 2.0 MB (1966561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115624f24ba74d393c2da3d65ed5b35a7afb3fa9ad143d3fb82c64953b3d0401`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87bba524314294ca97195ce65a35ec6d42d3f9f18c9cc0c05c064c9a3cf85c0`  
		Last Modified: Thu, 18 Dec 2025 00:32:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:2feda8921a7d67cd9f2f3d7186ed69ceb0d3c22af7a20bd230664e9bcf39096c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d73c6548a24cc8ce7782d03377e89a4b4b0e4c2a48cd3a03a79193320fc4d834`

```dockerfile
```

-	Layers:
	-	`sha256:984e438122735983bf56bc3d638fb1b0baf8cfb26ce26f71e0a9b847d25f76b5`  
		Last Modified: Thu, 18 Dec 2025 01:34:59 GMT  
		Size: 94.3 KB (94327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d6e8d91ca57b45f0050ec3833a8f09a7ce62f7ba9ec70e1ae12881ad4b2bb6f`  
		Last Modified: Thu, 18 Dec 2025 01:35:00 GMT  
		Size: 20.7 KB (20728 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-alpine` - linux; 386

```console
$ docker pull memcached@sha256:df1ba8af73cd6e3f8227557b097cd6b128ec0d410a3bbe7a2c282089c5641b41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5740953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78dbfc1f8ea65ad6466795e278180963d4afe98dfbca4a4497bc73c99f07ed4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:13:19 GMT
ADD alpine-minirootfs-3.23.2-x86.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:13:19 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:43 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:29:44 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:32:29 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:32:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:32:29 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:32:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:32:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:32:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:32:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:32:29 GMT
USER memcache
# Thu, 18 Dec 2025 00:32:29 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:32:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c21df6a7383dfce37a4bfe31b291881f55907c419caf5d06cb6d699d290d0718`  
		Last Modified: Thu, 18 Dec 2025 00:13:38 GMT  
		Size: 3.7 MB (3686100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37ec5bf455c1d98d22e6f3dacb5b971dac8ea96d1fe9b9177a07c5277530646`  
		Last Modified: Thu, 18 Dec 2025 00:32:35 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b2862af05c1582c8625c82ea0863dc2b6474e410d3e6a32876c920e0152c73`  
		Last Modified: Thu, 18 Dec 2025 00:32:35 GMT  
		Size: 110.7 KB (110740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30872a43f6c591fd9b979b49b0fb32107b4bfa8c1155657fa255aa199cf0b83b`  
		Last Modified: Thu, 18 Dec 2025 00:32:35 GMT  
		Size: 1.9 MB (1942762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a62c11b4aeceaba2e5e73a1bc29aa8b4fc42ccd0c7e8512cc11b96e48aef2f`  
		Last Modified: Thu, 18 Dec 2025 00:32:41 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f553d362a11992264bf5364cfe13d248403c5baf2ecac784c26f444dbfb90388`  
		Last Modified: Thu, 18 Dec 2025 00:32:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:e3b020c2afd9ae372e234c6ab67456908861fd24200448fd3cf741503a8a6f55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6abfcddfb1575f6cc07e51c6a379141589de7ea8c329a9bc5c1592f3186e6fda`

```dockerfile
```

-	Layers:
	-	`sha256:ff9be8ef1bab92275eb15ae5fd6a05e767abc1fe855455766200b3c0a1866e33`  
		Last Modified: Thu, 18 Dec 2025 01:35:03 GMT  
		Size: 94.8 KB (94828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d7026bdf84e278b6976f0ccab2297ddc0284cf329414f56d12608dbc2acb940`  
		Last Modified: Thu, 18 Dec 2025 00:32:35 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:7292c7b145e08f87f78644bf2c3355fad1d0b4d9366f173ffa0634c3ec93addf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6031729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ae72ba97ecea986f01bda1eb392aee1ded4b5a86b2edcabe92a2034143e155b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:33:41 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:33:42 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:36:14 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:36:14 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:36:14 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:36:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:36:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:36:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:36:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:36:14 GMT
USER memcache
# Thu, 18 Dec 2025 00:36:14 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:36:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c95450233dfe3e06529eb39ca4b46e6ad51ccf338cab64157669ff1fc0a8d72`  
		Last Modified: Thu, 18 Dec 2025 00:36:26 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4079a2d61bafcf146b8f57b35f0e39bf2548e0963be10cff5086f9a56ccdd9d`  
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
		Size: 126.3 KB (126257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f69efa1066815d67cf415d0aac5dcd305032257b6bded5a4c57a7444a1e7fd4`  
		Last Modified: Thu, 18 Dec 2025 00:36:26 GMT  
		Size: 2.1 MB (2076363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357f4165f53a3d4c66ef270bcb5b5283a066af50f79924cccc7c73f6a4f6f4ab`  
		Last Modified: Thu, 18 Dec 2025 00:36:36 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a65ff5cefcbfc874c1cac0857339eaee0b07147dd26b6bfa18c00921b4f30c`  
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:1d06281345f2ac44a607d40d5e87de6abb99bbc6ee82d319e73f3794602d0282
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4867a5aa08041c7e5ec69dfc84214226a7323d1ce703747ae2117675e2f74bcd`

```dockerfile
```

-	Layers:
	-	`sha256:282960f007d3f1f008333191d98a2ded5ff0f83075ace30043349b6c082c18fd`  
		Last Modified: Thu, 18 Dec 2025 01:35:08 GMT  
		Size: 94.3 KB (94280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4755fffd5924e8405adfbed0f328ad9792eff20e2b8ad2025e1f5c85bca88618`  
		Last Modified: Thu, 18 Dec 2025 01:35:09 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:9023f4a863c531a74c6ff8cc3b49c3be80ad1db07cc93fdcbf87c5d8e4cccc72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5768619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2159b7b74e5ffe77e6304def07dec2cfc2bdead26c3012e1e4d39bcd267adfe5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 06:39:34 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 06:39:38 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 06:52:53 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 06:52:53 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 06:52:53 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 06:52:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 06:52:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 06:52:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 06:52:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 06:52:53 GMT
USER memcache
# Thu, 18 Dec 2025 06:52:53 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 06:52:53 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc016d1883c21894ae540944be0270a95cb663037e8592a944bac62e0cc39e7`  
		Last Modified: Thu, 18 Dec 2025 06:53:25 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c580cd51da178bea3e44467f8b445f50ec9272e42e0254d269a9e38204b12dc`  
		Last Modified: Thu, 18 Dec 2025 06:53:25 GMT  
		Size: 108.9 KB (108898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11881c79ebc6a05357f0e2095f00d6d5a8a58bd9f11efeefc80b616d0230ff9`  
		Last Modified: Thu, 18 Dec 2025 06:53:25 GMT  
		Size: 2.1 MB (2074429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735bfa953d895df9672fe0b34207075bd7e686f71104973ad4e02d89db8719a9`  
		Last Modified: Thu, 18 Dec 2025 06:53:25 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b8c865432ff9b07178ba7cb96426e0515b00cc91866fb4dfb8c243e4187172`  
		Last Modified: Thu, 18 Dec 2025 06:53:25 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7cd6a8f4c278ff9062def241e6cdb501032ed72b091608a6da35812eece0954c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38b0c310a1ad4186c4beae0e268b71f1a80ed998cd80ceb81095aa9da7e6b02e`

```dockerfile
```

-	Layers:
	-	`sha256:88642ee1ee3c124ff8f2f640525172206ce9483620a70142ca673e0eca181c4d`  
		Last Modified: Thu, 18 Dec 2025 07:34:34 GMT  
		Size: 94.3 KB (94276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:441bda294fdd657b4574cd5337193125e3d0565433a700136501a858fce53d46`  
		Last Modified: Thu, 18 Dec 2025 07:34:34 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:e011484878fd5d1e2da6de478ac11d01ae80f0bdef1902dcde3ed53728803741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5857090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:689ea71c305b80e206c68a215481290a1378e6375e32ad059455f7d041396aa6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:30:26 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:30:27 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:33:46 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:33:46 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:33:46 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:33:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:33:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:33:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:33:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:33:46 GMT
USER memcache
# Thu, 18 Dec 2025 00:33:46 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:33:46 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4594a6826f7ed03c8c4f9f2aebb9716eb6e16d5b5ab7e1bc247783b503c5b10`  
		Last Modified: Thu, 18 Dec 2025 00:33:55 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f270744f8d8b82bc6657387109b33836a76d6dbf8faa645a997db7ea290cdb`  
		Last Modified: Thu, 18 Dec 2025 00:33:55 GMT  
		Size: 114.3 KB (114299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91f8ee8f36703944a7bdcaf57cc5772fe9f79c74a088c33fa1b6da7de119f93`  
		Last Modified: Thu, 18 Dec 2025 00:33:55 GMT  
		Size: 2.0 MB (2017131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e21d2db88668745770273c7b36d4d2c1e87a80b0118b8d775813860b467384c8`  
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd847159e169b898a67d4454fd5a22406c5ae623b16889d084a1d5f2d46a499`  
		Last Modified: Thu, 18 Dec 2025 00:33:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:33ab737cb23dcde22de59a58e40f1f80d2c5e808ff3036519ae7d9db228fa37d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3562f7fd7806da24b1865c01a2246ac041b5e98d69c10ce6cbbe479f9408f9a1`

```dockerfile
```

-	Layers:
	-	`sha256:d5f43e64a79ee525bd0354a06e3284444fd642bbe6c1a782aa45ec2e20462f1d`  
		Last Modified: Thu, 18 Dec 2025 01:35:19 GMT  
		Size: 94.2 KB (94222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bd2c024010f4f53d350bde9967c349efb3a58a2a812b14e17b29ddbd19eab87`  
		Last Modified: Thu, 18 Dec 2025 01:35:20 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.40-alpine3.23`

```console
$ docker pull memcached@sha256:c77536380fd3c7740933767bb5279bd30e31c8d496081e5113a37d9b9eec43cb
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

### `memcached:1.6.40-alpine3.23` - linux; amd64

```console
$ docker pull memcached@sha256:9573a2399011fa86bb7b5d12bdab987d7931c98ddec0ef6802de7eb6d3c3e338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5956768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c79853acc5f24e9c28f15d45cef0aedc114e76bbacf7958eb6f555c22246e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:34 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:29:34 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:32:07 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:32:07 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:32:07 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:32:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:32:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:32:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:32:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:32:07 GMT
USER memcache
# Thu, 18 Dec 2025 00:32:07 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:32:07 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:48:50 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57c33ac8581cd04f31208409f36331e938a78e6ae3a7a3b530fe9dfebe6eb9ad`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583aae99135b9036c602a1c60743fc4fd519f261ac6d48ed60b01e1beb019e7f`  
		Last Modified: Thu, 18 Dec 2025 00:32:12 GMT  
		Size: 106.0 KB (106050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ca22885c42a537f033850e8dff7eaeddbb7514902286739b48c084b55a8d6b`  
		Last Modified: Thu, 18 Dec 2025 00:32:12 GMT  
		Size: 2.0 MB (1989265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d146e2038834770bed57033a6c5d66ead5b731b8b133856dec6726ca21baee9`  
		Last Modified: Thu, 18 Dec 2025 00:32:12 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c66e6c3acbe07806e3e96a97d97a2d4503713c4814d9b24a2f57f2c39200d05`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:cfdf2ea6bf2a04bb7ee1568efe0c8bd38a1f5e644250a9409479cce281891ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de792623281192b3965fdc95f31532c4d166e731f53e202be1e2a224c654633b`

```dockerfile
```

-	Layers:
	-	`sha256:87a0d23eeeda6353dfc603cc4ffee062e5383be07b611754f3a88db3fc644036`  
		Last Modified: Thu, 18 Dec 2025 00:32:12 GMT  
		Size: 94.9 KB (94873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b73cd5efe31baa1fbf0eecea269426edcfc795cbb9b5dd74b523ff51b6f7c9f`  
		Last Modified: Thu, 18 Dec 2025 01:34:48 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-alpine3.23` - linux; arm variant v6

```console
$ docker pull memcached@sha256:c1a12b64cc8b47f50ea4610d9c1c362da7157b3ba67deac8b4760e6b589cde75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5611647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3591f95cad049a0509bd23a95556f8f848452d2a5491ed00bae293897c7a6b2f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:27:48 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:27:49 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:49:50 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:49:50 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:49:50 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:49:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:49:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:49:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:49:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:49:50 GMT
USER memcache
# Thu, 18 Dec 2025 00:49:50 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:49:50 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf585eb2bfa372c2097b9f7a5214ecb0941a30581b10fb74a26518fcc7addec`  
		Last Modified: Thu, 18 Dec 2025 00:49:55 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01bb148ea8fbe93dd8097d85f9ee3cf547d314e669748b4239c05711b0d5f719`  
		Last Modified: Thu, 18 Dec 2025 00:49:55 GMT  
		Size: 102.7 KB (102652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6549359cda37ac41cf41a5ece5f37f1322a82f6b232f12e446c62840637093e`  
		Last Modified: Thu, 18 Dec 2025 00:50:02 GMT  
		Size: 1.9 MB (1939215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:041e37eaffefcfb0809564ddea591be3cd818de5530e2c853c0bc9a2fa25c116`  
		Last Modified: Thu, 18 Dec 2025 00:49:55 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7907ae218c75b36c9a9002be8554131c271cde78b0280cb7a85029f99ad0bcdc`  
		Last Modified: Thu, 18 Dec 2025 00:50:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:a9c26fc290551b691574e093d3c28f4fe7b558b3f8173b3c99eb8a664c83a8e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ca65d7156e6586d96310ea3162facd9849d5460d2939b461a25247b06a4d59`

```dockerfile
```

-	Layers:
	-	`sha256:d9c217dc241f1175812c47b6489d325a0574c0da554c6f8aa0b86a2d8aff05f9`  
		Last Modified: Thu, 18 Dec 2025 01:34:52 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-alpine3.23` - linux; arm variant v7

```console
$ docker pull memcached@sha256:cee00a47bf7b8b5899a6cf1f5c692494df31b454f52b81f3c4886905a0c9bdd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5270304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d91d78dbe118f2b7b0d6e850e1115de72c4fe3e30c55a5b53d8a844d14357d16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:30:56 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:30:57 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:33:51 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:33:51 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:33:51 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:33:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:33:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:33:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:33:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:33:51 GMT
USER memcache
# Thu, 18 Dec 2025 00:33:51 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:33:51 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:43 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa22c446792763e48f4680945ccc68d43c7906ef35a92e0b908f57ef53e72f0`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954155078f2265364295ebdf16fb114e991b1938d8a6951fb511163ab3b2b385`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 92.4 KB (92378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a25584b03ac5e45c66c3c616acfd9df1848e5db25219ef20feb2868c30c6332`  
		Last Modified: Thu, 18 Dec 2025 00:33:57 GMT  
		Size: 1.9 MB (1897191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f237be962bb57c3f749904b5925c8e1d7e9013dfac7dd52cc9611ada81858e`  
		Last Modified: Thu, 18 Dec 2025 00:33:57 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b07d9170b246a631c262d9f5d57f49278f7cd4805463b90b14aeca4dc61d93`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:64abe011fed6a9cf7b3290c752c50bffe81bb2e65cf6337e023efda87d49b451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b251b9c15ab7c5742bd3ab725df09f0ecb9f2491f92cf1c825bec598a31f4407`

```dockerfile
```

-	Layers:
	-	`sha256:1882c6d4361100a29fd5ab265587f65fa27b1df15e7f9349b30dac454facf98e`  
		Last Modified: Thu, 18 Dec 2025 00:33:57 GMT  
		Size: 94.3 KB (94291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf0a88ab3838de6beab653497ab62a64cfb87b1dc83c5fa5b6f3907abfd88080`  
		Last Modified: Thu, 18 Dec 2025 01:34:56 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:b6c3042e2bf09ec3d3f054d03b81313e8df717a49371ce916ff743e602796bc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6285509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6691028570bbd843e6da26558c46162b8383212fcaaefcecb2d3f919e3401429`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:18 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:29:19 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:32:06 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:32:06 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:32:06 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:32:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:32:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:32:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:32:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:32:06 GMT
USER memcache
# Thu, 18 Dec 2025 00:32:06 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:32:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb7b8445facedfc145b9478f74880f520776460f153005b7f437ec339aee530`  
		Last Modified: Thu, 18 Dec 2025 00:32:11 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1853c901134389608b6e80aaa3e43cd67a35c71aecfdde4b5b7ed3b989a03c`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 121.9 KB (121860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a01d1ac5ce47f4494363e411e1cd25dea26438213a2d18d6bb104d0974d9a52`  
		Last Modified: Thu, 18 Dec 2025 00:32:11 GMT  
		Size: 2.0 MB (1966561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115624f24ba74d393c2da3d65ed5b35a7afb3fa9ad143d3fb82c64953b3d0401`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87bba524314294ca97195ce65a35ec6d42d3f9f18c9cc0c05c064c9a3cf85c0`  
		Last Modified: Thu, 18 Dec 2025 00:32:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:2feda8921a7d67cd9f2f3d7186ed69ceb0d3c22af7a20bd230664e9bcf39096c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d73c6548a24cc8ce7782d03377e89a4b4b0e4c2a48cd3a03a79193320fc4d834`

```dockerfile
```

-	Layers:
	-	`sha256:984e438122735983bf56bc3d638fb1b0baf8cfb26ce26f71e0a9b847d25f76b5`  
		Last Modified: Thu, 18 Dec 2025 01:34:59 GMT  
		Size: 94.3 KB (94327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d6e8d91ca57b45f0050ec3833a8f09a7ce62f7ba9ec70e1ae12881ad4b2bb6f`  
		Last Modified: Thu, 18 Dec 2025 01:35:00 GMT  
		Size: 20.7 KB (20728 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-alpine3.23` - linux; 386

```console
$ docker pull memcached@sha256:df1ba8af73cd6e3f8227557b097cd6b128ec0d410a3bbe7a2c282089c5641b41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5740953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78dbfc1f8ea65ad6466795e278180963d4afe98dfbca4a4497bc73c99f07ed4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:13:19 GMT
ADD alpine-minirootfs-3.23.2-x86.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:13:19 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:43 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:29:44 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:32:29 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:32:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:32:29 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:32:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:32:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:32:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:32:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:32:29 GMT
USER memcache
# Thu, 18 Dec 2025 00:32:29 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:32:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c21df6a7383dfce37a4bfe31b291881f55907c419caf5d06cb6d699d290d0718`  
		Last Modified: Thu, 18 Dec 2025 00:13:38 GMT  
		Size: 3.7 MB (3686100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37ec5bf455c1d98d22e6f3dacb5b971dac8ea96d1fe9b9177a07c5277530646`  
		Last Modified: Thu, 18 Dec 2025 00:32:35 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b2862af05c1582c8625c82ea0863dc2b6474e410d3e6a32876c920e0152c73`  
		Last Modified: Thu, 18 Dec 2025 00:32:35 GMT  
		Size: 110.7 KB (110740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30872a43f6c591fd9b979b49b0fb32107b4bfa8c1155657fa255aa199cf0b83b`  
		Last Modified: Thu, 18 Dec 2025 00:32:35 GMT  
		Size: 1.9 MB (1942762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a62c11b4aeceaba2e5e73a1bc29aa8b4fc42ccd0c7e8512cc11b96e48aef2f`  
		Last Modified: Thu, 18 Dec 2025 00:32:41 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f553d362a11992264bf5364cfe13d248403c5baf2ecac784c26f444dbfb90388`  
		Last Modified: Thu, 18 Dec 2025 00:32:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:e3b020c2afd9ae372e234c6ab67456908861fd24200448fd3cf741503a8a6f55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6abfcddfb1575f6cc07e51c6a379141589de7ea8c329a9bc5c1592f3186e6fda`

```dockerfile
```

-	Layers:
	-	`sha256:ff9be8ef1bab92275eb15ae5fd6a05e767abc1fe855455766200b3c0a1866e33`  
		Last Modified: Thu, 18 Dec 2025 01:35:03 GMT  
		Size: 94.8 KB (94828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d7026bdf84e278b6976f0ccab2297ddc0284cf329414f56d12608dbc2acb940`  
		Last Modified: Thu, 18 Dec 2025 00:32:35 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-alpine3.23` - linux; ppc64le

```console
$ docker pull memcached@sha256:7292c7b145e08f87f78644bf2c3355fad1d0b4d9366f173ffa0634c3ec93addf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6031729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ae72ba97ecea986f01bda1eb392aee1ded4b5a86b2edcabe92a2034143e155b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:33:41 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:33:42 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:36:14 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:36:14 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:36:14 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:36:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:36:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:36:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:36:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:36:14 GMT
USER memcache
# Thu, 18 Dec 2025 00:36:14 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:36:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c95450233dfe3e06529eb39ca4b46e6ad51ccf338cab64157669ff1fc0a8d72`  
		Last Modified: Thu, 18 Dec 2025 00:36:26 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4079a2d61bafcf146b8f57b35f0e39bf2548e0963be10cff5086f9a56ccdd9d`  
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
		Size: 126.3 KB (126257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f69efa1066815d67cf415d0aac5dcd305032257b6bded5a4c57a7444a1e7fd4`  
		Last Modified: Thu, 18 Dec 2025 00:36:26 GMT  
		Size: 2.1 MB (2076363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357f4165f53a3d4c66ef270bcb5b5283a066af50f79924cccc7c73f6a4f6f4ab`  
		Last Modified: Thu, 18 Dec 2025 00:36:36 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a65ff5cefcbfc874c1cac0857339eaee0b07147dd26b6bfa18c00921b4f30c`  
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:1d06281345f2ac44a607d40d5e87de6abb99bbc6ee82d319e73f3794602d0282
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4867a5aa08041c7e5ec69dfc84214226a7323d1ce703747ae2117675e2f74bcd`

```dockerfile
```

-	Layers:
	-	`sha256:282960f007d3f1f008333191d98a2ded5ff0f83075ace30043349b6c082c18fd`  
		Last Modified: Thu, 18 Dec 2025 01:35:08 GMT  
		Size: 94.3 KB (94280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4755fffd5924e8405adfbed0f328ad9792eff20e2b8ad2025e1f5c85bca88618`  
		Last Modified: Thu, 18 Dec 2025 01:35:09 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-alpine3.23` - linux; riscv64

```console
$ docker pull memcached@sha256:9023f4a863c531a74c6ff8cc3b49c3be80ad1db07cc93fdcbf87c5d8e4cccc72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5768619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2159b7b74e5ffe77e6304def07dec2cfc2bdead26c3012e1e4d39bcd267adfe5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 06:39:34 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 06:39:38 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 06:52:53 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 06:52:53 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 06:52:53 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 06:52:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 06:52:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 06:52:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 06:52:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 06:52:53 GMT
USER memcache
# Thu, 18 Dec 2025 06:52:53 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 06:52:53 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc016d1883c21894ae540944be0270a95cb663037e8592a944bac62e0cc39e7`  
		Last Modified: Thu, 18 Dec 2025 06:53:25 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c580cd51da178bea3e44467f8b445f50ec9272e42e0254d269a9e38204b12dc`  
		Last Modified: Thu, 18 Dec 2025 06:53:25 GMT  
		Size: 108.9 KB (108898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11881c79ebc6a05357f0e2095f00d6d5a8a58bd9f11efeefc80b616d0230ff9`  
		Last Modified: Thu, 18 Dec 2025 06:53:25 GMT  
		Size: 2.1 MB (2074429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735bfa953d895df9672fe0b34207075bd7e686f71104973ad4e02d89db8719a9`  
		Last Modified: Thu, 18 Dec 2025 06:53:25 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b8c865432ff9b07178ba7cb96426e0515b00cc91866fb4dfb8c243e4187172`  
		Last Modified: Thu, 18 Dec 2025 06:53:25 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:7cd6a8f4c278ff9062def241e6cdb501032ed72b091608a6da35812eece0954c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38b0c310a1ad4186c4beae0e268b71f1a80ed998cd80ceb81095aa9da7e6b02e`

```dockerfile
```

-	Layers:
	-	`sha256:88642ee1ee3c124ff8f2f640525172206ce9483620a70142ca673e0eca181c4d`  
		Last Modified: Thu, 18 Dec 2025 07:34:34 GMT  
		Size: 94.3 KB (94276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:441bda294fdd657b4574cd5337193125e3d0565433a700136501a858fce53d46`  
		Last Modified: Thu, 18 Dec 2025 07:34:34 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-alpine3.23` - linux; s390x

```console
$ docker pull memcached@sha256:e011484878fd5d1e2da6de478ac11d01ae80f0bdef1902dcde3ed53728803741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5857090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:689ea71c305b80e206c68a215481290a1378e6375e32ad059455f7d041396aa6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:30:26 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:30:27 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:33:46 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:33:46 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:33:46 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:33:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:33:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:33:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:33:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:33:46 GMT
USER memcache
# Thu, 18 Dec 2025 00:33:46 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:33:46 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4594a6826f7ed03c8c4f9f2aebb9716eb6e16d5b5ab7e1bc247783b503c5b10`  
		Last Modified: Thu, 18 Dec 2025 00:33:55 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f270744f8d8b82bc6657387109b33836a76d6dbf8faa645a997db7ea290cdb`  
		Last Modified: Thu, 18 Dec 2025 00:33:55 GMT  
		Size: 114.3 KB (114299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91f8ee8f36703944a7bdcaf57cc5772fe9f79c74a088c33fa1b6da7de119f93`  
		Last Modified: Thu, 18 Dec 2025 00:33:55 GMT  
		Size: 2.0 MB (2017131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e21d2db88668745770273c7b36d4d2c1e87a80b0118b8d775813860b467384c8`  
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd847159e169b898a67d4454fd5a22406c5ae623b16889d084a1d5f2d46a499`  
		Last Modified: Thu, 18 Dec 2025 00:33:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:33ab737cb23dcde22de59a58e40f1f80d2c5e808ff3036519ae7d9db228fa37d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3562f7fd7806da24b1865c01a2246ac041b5e98d69c10ce6cbbe479f9408f9a1`

```dockerfile
```

-	Layers:
	-	`sha256:d5f43e64a79ee525bd0354a06e3284444fd642bbe6c1a782aa45ec2e20462f1d`  
		Last Modified: Thu, 18 Dec 2025 01:35:19 GMT  
		Size: 94.2 KB (94222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bd2c024010f4f53d350bde9967c349efb3a58a2a812b14e17b29ddbd19eab87`  
		Last Modified: Thu, 18 Dec 2025 01:35:20 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.40-trixie`

```console
$ docker pull memcached@sha256:e4e5eca37e4334f9579f10fcdd88a58c4eb9d0a8eacedde6ec49d4ea4391637a
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

### `memcached:1.6.40-trixie` - linux; amd64

```console
$ docker pull memcached@sha256:1613c35e314db0c64d8b5679786ad99ced10069c3f9778d40b6c522ff3c04218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32190619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a38251b773d15614da3036dd0d756bbf4a7d16d27fe1c52023517a419372b245`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:22:30 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 13 Jan 2026 01:22:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:25:18 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 13 Jan 2026 01:25:18 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 13 Jan 2026 01:25:18 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 13 Jan 2026 01:25:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 13 Jan 2026 01:25:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:25:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 01:25:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:25:18 GMT
USER memcache
# Tue, 13 Jan 2026 01:25:18 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 13 Jan 2026 01:25:18 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:34 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b6e737e1a3eed198cc17e2b92231ab084bcf55ba90a36136e7a2f4fd04a95b`  
		Last Modified: Tue, 13 Jan 2026 01:25:30 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16835fec399670b74d32630a7368a65ca2a3c32d8b7a690d33bebc7b9e9458d`  
		Last Modified: Tue, 13 Jan 2026 01:25:30 GMT  
		Size: 136.7 KB (136737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c848acbad27f1c9d2fd95e0facabbb28d5d8be19e5fa5912e5474c1301522523`  
		Last Modified: Tue, 13 Jan 2026 01:25:25 GMT  
		Size: 2.3 MB (2278686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9529916038b7840d3177e93bf04b78390bb91bca78623bd9c0769f9e2a965079`  
		Last Modified: Tue, 13 Jan 2026 01:25:25 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24239fc168f5eb73ae9964e2cdcb3c3b878ae79835c6b94585cb648fd50479d`  
		Last Modified: Tue, 13 Jan 2026 01:25:26 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:0d72ad7b507d17cffe5dbec1ddecf1c254c3a85d2b605fa0ddbc9913ba4fc678
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe582f0cad77d385a3debb0f2acf0c96b7b85c6a7d2c95fcc54f938d63635c9`

```dockerfile
```

-	Layers:
	-	`sha256:7d598d8c3b4cd06481693da06e86554144167d205cc60f43382fafba94dd4592`  
		Last Modified: Tue, 13 Jan 2026 04:35:37 GMT  
		Size: 2.0 MB (2008290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dd2469227ab0e75822eb9d56a5d7c05f52a445840f65934e010a2562e509718`  
		Last Modified: Tue, 13 Jan 2026 01:25:24 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-trixie` - linux; arm variant v5

```console
$ docker pull memcached@sha256:efa6728c05b024b605597e5025f04155aab614b52f56b1b31a4c70a23f909e07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30298859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14119dc07998a4322ac912beaaf4e6ad16e5487f2243c332fdaad86bdce6f55e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:19:21 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 13 Jan 2026 01:19:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:22:43 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 13 Jan 2026 01:22:43 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 13 Jan 2026 01:22:43 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 13 Jan 2026 01:22:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 13 Jan 2026 01:22:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:22:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 01:22:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:22:43 GMT
USER memcache
# Tue, 13 Jan 2026 01:22:43 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 13 Jan 2026 01:22:43 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c113d410d30c2c035a105b56d3937958c81fbe2530f44add3bae903be6864324`  
		Last Modified: Tue, 13 Jan 2026 00:42:30 GMT  
		Size: 27.9 MB (27942724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96776850dc1206c3fd163b84cea19599306159eb0d020b4241d0172240f88d13`  
		Last Modified: Tue, 13 Jan 2026 01:22:55 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3697c7c790d9c4caaa904abdaf809dcdee3f0b518fc5ad82d2e21dd7fe24f64d`  
		Last Modified: Tue, 13 Jan 2026 01:22:55 GMT  
		Size: 144.2 KB (144212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a247339c7ec57a491c3ffe43531dbfaa132f3ff16a481fc41cbb9e3e3ad6476`  
		Last Modified: Tue, 13 Jan 2026 01:22:50 GMT  
		Size: 2.2 MB (2210412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2dcebe3ab2a9945cdea142301e4a64eebbc59c948a54385dbfca4afd561b508`  
		Last Modified: Tue, 13 Jan 2026 01:22:55 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb8ef5ecbc44efd5280f9cf15687dfd80a34fa2966ad039238647177f75dc6c`  
		Last Modified: Tue, 13 Jan 2026 01:22:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:190bb1ecd7376720e541621921c2d4931a9d0f85a047255ba2b56afa3a504212
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9736e9545a46e4ef65dcb5238691292d27fac4dccb330354ce59ac93ae6994b5`

```dockerfile
```

-	Layers:
	-	`sha256:4f5461bf596f750b56b3f10e315936c2326b2c32901d28cdf22db97072bba685`  
		Last Modified: Tue, 13 Jan 2026 01:22:50 GMT  
		Size: 2.0 MB (2011293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8657d28d0436d39193457fb90119ea6e4ddb566df2a83fd1aa9df75651731188`  
		Last Modified: Tue, 13 Jan 2026 04:35:43 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-trixie` - linux; arm variant v7

```console
$ docker pull memcached@sha256:9c322c838b4648fa30e742e53ed6647a31383760fb73fa82de32b4b6dc88c494
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28509532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6e130248535c57fccff4d89a9d442e31cabd471e41c9eed52e5207a54f9f944`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:25:47 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 13 Jan 2026 01:25:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:28:55 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 13 Jan 2026 01:28:55 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 13 Jan 2026 01:28:55 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 13 Jan 2026 01:28:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 13 Jan 2026 01:28:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:28:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 01:28:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:28:55 GMT
USER memcache
# Tue, 13 Jan 2026 01:28:55 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 13 Jan 2026 01:28:55 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029a2cbe46c1e12ab6d47a63f40fb29056b6c6277c7822085ed0fe62e0a1791d`  
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c7827f95482598f1bd32dd8cbe071ad009795fa108661234eeb872d1a1e8bd`  
		Last Modified: Tue, 13 Jan 2026 01:29:07 GMT  
		Size: 135.4 KB (135398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9371e974781bd91adc657086f00cd7d91b5530ca9da37597c347dd7d4eaff0`  
		Last Modified: Tue, 13 Jan 2026 01:29:07 GMT  
		Size: 2.2 MB (2164040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c2e0f64c0afa16b5e214ae208c8c81e8c78c79ddd90f54983a93c7297395f6b`  
		Last Modified: Tue, 13 Jan 2026 01:29:07 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92151d443057f88ed7f60405440b698ff9e6abe1a2ca1c91a0c7e7626339ad2`  
		Last Modified: Tue, 13 Jan 2026 01:29:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:12cc31a1ce56d2c6dd1c0dcfd4ef1fe74484985d010594950c086c0f4431559b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b2d844d5393973080c37fde0b92cd48bd1a64e03973290631be5486d814de7e`

```dockerfile
```

-	Layers:
	-	`sha256:99fc27444c1ccdd6cbd08a33aac22e9e85f55958bda7b6216bdea08eae374cff`  
		Last Modified: Tue, 13 Jan 2026 04:35:47 GMT  
		Size: 2.0 MB (2009750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e76d5584f581b7668c61a661da2858bc1d5e11b31e3629e0d2b3af52d9c22ed8`  
		Last Modified: Tue, 13 Jan 2026 04:35:47 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-trixie` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:2ed537fa0376a3eb0864d6a3b51ea7da59b9ff4bb3270189a8a5082f02f811e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32550406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf26d75d787aabbd202c97db1079b96e45105d3ca509a1001ab973cb473cae8c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:22:29 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 13 Jan 2026 01:22:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:25:26 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 13 Jan 2026 01:25:26 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 13 Jan 2026 01:25:26 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 13 Jan 2026 01:25:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 13 Jan 2026 01:25:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:25:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 01:25:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:25:27 GMT
USER memcache
# Tue, 13 Jan 2026 01:25:27 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 13 Jan 2026 01:25:27 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78edb6b991369235f90958a936afc89dc37b82439c632988ed143b5bd76deadb`  
		Last Modified: Tue, 13 Jan 2026 01:25:40 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e1afbb765f6cc3923e864d44fb6cd6c9167b884e596b09bd37c7c276f65a2b`  
		Last Modified: Tue, 13 Jan 2026 01:25:40 GMT  
		Size: 153.5 KB (153512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff9edc68fe57c233001afd442eb6c248bf070d32fbb412a8bfeef6f9a6217f5`  
		Last Modified: Tue, 13 Jan 2026 01:25:40 GMT  
		Size: 2.3 MB (2261341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c4648fbc4a4189184946895d1041e0eee2c5d40fd70638a553bedb0cbf5cf8`  
		Last Modified: Tue, 13 Jan 2026 01:25:40 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26bd1b32b048e73091ddf6e6762e368d4bb6ef2cc7d3aa43467749b36fe08e38`  
		Last Modified: Tue, 13 Jan 2026 01:25:40 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:72333c6222fb20b5a9f9f92b8d56c47ebb5b4e6cd65512a6b5172ad0c0cade67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a2a4e23cbe2d062f3fcfb84c8590190eb72294786a0b8238add858e67a93914`

```dockerfile
```

-	Layers:
	-	`sha256:1f8545bcc66309a59381c88c4c87b0f8352893dbaa167be48947976c1e0cef1d`  
		Last Modified: Tue, 13 Jan 2026 04:35:51 GMT  
		Size: 2.0 MB (2008606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95e6875e372e1d6a9660c08726cb96d08b272e52a2446f275089efccfc3096b3`  
		Last Modified: Tue, 13 Jan 2026 01:25:33 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-trixie` - linux; 386

```console
$ docker pull memcached@sha256:29540e588e9065db9ecc8865fe74544260980d73786f00dfc4df3f3cee148bd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33661194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66843ae7a7d968c4f056a8e350dd84ff80a06e48b48c298c3427333b7ec259ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:19:43 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 13 Jan 2026 01:19:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:22:40 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 13 Jan 2026 01:22:40 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 13 Jan 2026 01:22:40 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 13 Jan 2026 01:22:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 13 Jan 2026 01:22:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:22:40 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 01:22:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:22:40 GMT
USER memcache
# Tue, 13 Jan 2026 01:22:40 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 13 Jan 2026 01:22:40 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:27bb6d39eda5ced7626db280c3902aacdfade5acd11a16ef9618e3185f69b102`  
		Last Modified: Tue, 13 Jan 2026 00:43:03 GMT  
		Size: 31.3 MB (31288476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cedb4f2840edea9de46e0d955a0512f469211880560a8948f10b54381bcd728`  
		Last Modified: Tue, 13 Jan 2026 01:22:53 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c4b2d1574ee5f238dc6948164abd39ffcc91929b2c464c6b3874dec01fd964`  
		Last Modified: Tue, 13 Jan 2026 01:22:46 GMT  
		Size: 147.6 KB (147554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc1bf5870b84175607f3d012b3cfebc5859869f8125114ea5d6ed1a05f81d2d`  
		Last Modified: Tue, 13 Jan 2026 01:22:53 GMT  
		Size: 2.2 MB (2223652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6434e73ed67e81f1016f27c7cc175290b0ce959d8a1bf5e9b0f3119f161246`  
		Last Modified: Tue, 13 Jan 2026 01:22:53 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abaf99fdf0e2b9620d20088b389b3f18eb67ad356c8c6c7961074e1428b8af0c`  
		Last Modified: Tue, 13 Jan 2026 01:22:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:f64192985f4635b04ce1ab99b3cae89f71d0b11f9670fb6d9c470158e3c5c63e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bb9ce834f23725c4bfc4fb2d6a24a96d3d0bc7685d3a759c0085871f34231e8`

```dockerfile
```

-	Layers:
	-	`sha256:ed9937c762728e5abc93b88bd7932a5762d2bc8e0001e81bb25ef0b27e2bc6ff`  
		Last Modified: Tue, 13 Jan 2026 04:35:56 GMT  
		Size: 2.0 MB (2005447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6358862e12c5c5367efd52bea0b1194e04e76f267084da591229f64ee7482dc3`  
		Last Modified: Tue, 13 Jan 2026 04:35:57 GMT  
		Size: 22.1 KB (22094 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-trixie` - linux; ppc64le

```console
$ docker pull memcached@sha256:309e0faad388272d7e37d6ee0cb354707d099e3140298105499711823d7a0eea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36161489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6f50ee10fc83da67b90c9bda7499251fa073fea87400d5fb70e31e693d6f902`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:33:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 13 Jan 2026 01:33:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:36:52 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 13 Jan 2026 01:36:52 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 13 Jan 2026 01:36:52 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 13 Jan 2026 01:36:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 13 Jan 2026 01:36:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:36:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 01:36:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:36:53 GMT
USER memcache
# Tue, 13 Jan 2026 01:36:53 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 13 Jan 2026 01:36:53 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9a275bb13cf8b3e9db52a41b6b4ff22ee1ffed00394f6deddd2de45044bd3bae`  
		Last Modified: Tue, 13 Jan 2026 00:57:13 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093e59deb53ff01a892be2a5df928c4b04a289df7f6c135570c11d6a4fdbc53a`  
		Last Modified: Tue, 13 Jan 2026 01:37:16 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4da25c8b13ee47050a38843c1954d2bd7bbdba2666f725aee2f603e03fcb6d`  
		Last Modified: Tue, 13 Jan 2026 01:37:16 GMT  
		Size: 170.4 KB (170427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cab5f6f805c735c0f324c87ff8c66cfab0e35fb691b7761e85bb9a2bbb31cfe`  
		Last Modified: Tue, 13 Jan 2026 01:37:16 GMT  
		Size: 2.4 MB (2393947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3a7dfc8da65bd6101de156530bc2688c5588c718bbc3131ff4594cbefd0e66`  
		Last Modified: Tue, 13 Jan 2026 01:37:09 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06153b2e2bde9b06f1c2719aabb5ff6a6c23056152a024fa2c990d97b4d9c799`  
		Last Modified: Tue, 13 Jan 2026 01:37:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:8dfcc685b38edcaec140b90716d19e543715184f20f7a401d6f734ad8f8cf1dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7442b6e23a86bfe5ee9a534d43f0a55ba9629d3c24128b1b3e2b5121644dcf00`

```dockerfile
```

-	Layers:
	-	`sha256:a4b6027eed506a371ad9a2314b6be299e5c509b4c4be66e5842b29837171b0cf`  
		Last Modified: Tue, 13 Jan 2026 04:36:00 GMT  
		Size: 2.0 MB (2011891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc718b3aa0399c50248bba6165cad8666196a5351b6ed095a8101d2f8a5d37da`  
		Last Modified: Tue, 13 Jan 2026 04:36:01 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-trixie` - linux; riscv64

```console
$ docker pull memcached@sha256:bce857473a0aeeec89bc5383841d05d99df2b89bba49caf3059874a9442ff224
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30613806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc8f84b5bfd0d6518442de566ffa39b2113651446c246e419f61a8e5fa68e87`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Wed, 14 Jan 2026 06:36:03 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 14 Jan 2026 06:36:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jan 2026 06:49:42 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 14 Jan 2026 06:49:42 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 14 Jan 2026 06:49:42 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 14 Jan 2026 06:49:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 14 Jan 2026 06:49:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 06:49:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 14 Jan 2026 06:49:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 06:49:43 GMT
USER memcache
# Wed, 14 Jan 2026 06:49:43 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 14 Jan 2026 06:49:43 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7c6f79d4d52450222a8a38f8fc98e229a4711a246fc94fdaaab31930d3135d`  
		Last Modified: Wed, 14 Jan 2026 06:50:36 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168d1b37fe07dfb8bef5240057ad6597058647499a9e771eedd2091f2d6b30f0`  
		Last Modified: Wed, 14 Jan 2026 06:50:36 GMT  
		Size: 133.1 KB (133105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a5ebc1ef49cab24f75e0c751a1e0563ee042c246c509279fa38cf3cbf0a3f1`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 2.2 MB (2207499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbc8df7ca1d2f273c3c8fec55b30f17ebc72a45687976efd9c8779a66369d46`  
		Last Modified: Wed, 14 Jan 2026 06:50:36 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4057c9476d421ae1ecae3607afb0db57dbc6eb2bc0aa5e41daed169a70319c1`  
		Last Modified: Wed, 14 Jan 2026 06:50:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:75823016a946bfe52b08e1f80032a64b0202a08f2e30dd8cb7035a01e1244518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b86887925c9eccb39ad75807a81768a06591c668cfd4bf4af00a40b2414f22bc`

```dockerfile
```

-	Layers:
	-	`sha256:0d93e934848935cdae8d83be9ebaff197aaa6e70f5b224c2107461561ea0064d`  
		Last Modified: Wed, 14 Jan 2026 07:34:47 GMT  
		Size: 2.0 MB (2002254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0de5bd0cbff9df1fc11e05bd38936b6915195663b273b5c23840bf5eb9373a8`  
		Last Modified: Wed, 14 Jan 2026 07:34:48 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-trixie` - linux; s390x

```console
$ docker pull memcached@sha256:46c34c0b238fbae2980413fe2b6590839b6afbc43e0a1e07eb456fc274eaf811
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32272852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8666231b78b1bdfb283fe302437321dedf8ecc2d869ff2acdce9f8461f285519`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 14:13:49 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 13 Jan 2026 14:13:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 14:16:57 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 13 Jan 2026 14:16:57 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 13 Jan 2026 14:16:57 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 13 Jan 2026 14:16:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 13 Jan 2026 14:16:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 14:16:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 14:16:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 14:16:57 GMT
USER memcache
# Tue, 13 Jan 2026 14:16:57 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 13 Jan 2026 14:16:57 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2b46bc94baaae0a37e5e04b1babf7e1f37c4390b83d49c3c6820188deba770e3`  
		Last Modified: Tue, 13 Jan 2026 13:10:43 GMT  
		Size: 29.8 MB (29833411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2727771ad16d920baecb7c96b9b54e67178369b881fc20901d381dfd5f873e27`  
		Last Modified: Tue, 13 Jan 2026 14:17:12 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6b0ec5581f8591522a6327cdcfa4e1197d9ada9fb60840f57b5d3e4dd3304d1`  
		Last Modified: Tue, 13 Jan 2026 14:17:12 GMT  
		Size: 140.6 KB (140562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382a3e1ebed70673a0789fcc2104ab941fe04b9a020339f9286ac85b67ae5ff9`  
		Last Modified: Tue, 13 Jan 2026 14:17:13 GMT  
		Size: 2.3 MB (2297368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85fe5f9afd355e3dd76ce942e1c295e356d96ae3b0e3f8236a0e33c5f75ffe71`  
		Last Modified: Tue, 13 Jan 2026 14:17:08 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4546f3c3457928dc273f98dae7c7ac2f945b203138e964ee72fc92aabcef434`  
		Last Modified: Tue, 13 Jan 2026 14:17:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:d620668087c443f58d215a372a70eb0697c7031777d3537d244fa26e62d3ec3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e48c5956bcfcf63509c135da7076a0f247bc2858c7df68331b5a112e937ff6c`

```dockerfile
```

-	Layers:
	-	`sha256:507d45d8f4547a846c07788edb1628f89b93ac7616169374be23f29601b7be68`  
		Last Modified: Tue, 13 Jan 2026 14:17:08 GMT  
		Size: 2.0 MB (2009727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78fdd8684e48fc4ee1817e00df577a38250864ffbcf34ec341937d525d9dfabd`  
		Last Modified: Tue, 13 Jan 2026 16:34:40 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine`

```console
$ docker pull memcached@sha256:c77536380fd3c7740933767bb5279bd30e31c8d496081e5113a37d9b9eec43cb
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
$ docker pull memcached@sha256:9573a2399011fa86bb7b5d12bdab987d7931c98ddec0ef6802de7eb6d3c3e338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5956768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c79853acc5f24e9c28f15d45cef0aedc114e76bbacf7958eb6f555c22246e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:34 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:29:34 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:32:07 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:32:07 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:32:07 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:32:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:32:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:32:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:32:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:32:07 GMT
USER memcache
# Thu, 18 Dec 2025 00:32:07 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:32:07 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:48:50 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57c33ac8581cd04f31208409f36331e938a78e6ae3a7a3b530fe9dfebe6eb9ad`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583aae99135b9036c602a1c60743fc4fd519f261ac6d48ed60b01e1beb019e7f`  
		Last Modified: Thu, 18 Dec 2025 00:32:12 GMT  
		Size: 106.0 KB (106050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ca22885c42a537f033850e8dff7eaeddbb7514902286739b48c084b55a8d6b`  
		Last Modified: Thu, 18 Dec 2025 00:32:12 GMT  
		Size: 2.0 MB (1989265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d146e2038834770bed57033a6c5d66ead5b731b8b133856dec6726ca21baee9`  
		Last Modified: Thu, 18 Dec 2025 00:32:12 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c66e6c3acbe07806e3e96a97d97a2d4503713c4814d9b24a2f57f2c39200d05`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:cfdf2ea6bf2a04bb7ee1568efe0c8bd38a1f5e644250a9409479cce281891ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de792623281192b3965fdc95f31532c4d166e731f53e202be1e2a224c654633b`

```dockerfile
```

-	Layers:
	-	`sha256:87a0d23eeeda6353dfc603cc4ffee062e5383be07b611754f3a88db3fc644036`  
		Last Modified: Thu, 18 Dec 2025 00:32:12 GMT  
		Size: 94.9 KB (94873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b73cd5efe31baa1fbf0eecea269426edcfc795cbb9b5dd74b523ff51b6f7c9f`  
		Last Modified: Thu, 18 Dec 2025 01:34:48 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:c1a12b64cc8b47f50ea4610d9c1c362da7157b3ba67deac8b4760e6b589cde75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5611647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3591f95cad049a0509bd23a95556f8f848452d2a5491ed00bae293897c7a6b2f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:27:48 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:27:49 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:49:50 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:49:50 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:49:50 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:49:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:49:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:49:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:49:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:49:50 GMT
USER memcache
# Thu, 18 Dec 2025 00:49:50 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:49:50 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf585eb2bfa372c2097b9f7a5214ecb0941a30581b10fb74a26518fcc7addec`  
		Last Modified: Thu, 18 Dec 2025 00:49:55 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01bb148ea8fbe93dd8097d85f9ee3cf547d314e669748b4239c05711b0d5f719`  
		Last Modified: Thu, 18 Dec 2025 00:49:55 GMT  
		Size: 102.7 KB (102652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6549359cda37ac41cf41a5ece5f37f1322a82f6b232f12e446c62840637093e`  
		Last Modified: Thu, 18 Dec 2025 00:50:02 GMT  
		Size: 1.9 MB (1939215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:041e37eaffefcfb0809564ddea591be3cd818de5530e2c853c0bc9a2fa25c116`  
		Last Modified: Thu, 18 Dec 2025 00:49:55 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7907ae218c75b36c9a9002be8554131c271cde78b0280cb7a85029f99ad0bcdc`  
		Last Modified: Thu, 18 Dec 2025 00:50:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:a9c26fc290551b691574e093d3c28f4fe7b558b3f8173b3c99eb8a664c83a8e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ca65d7156e6586d96310ea3162facd9849d5460d2939b461a25247b06a4d59`

```dockerfile
```

-	Layers:
	-	`sha256:d9c217dc241f1175812c47b6489d325a0574c0da554c6f8aa0b86a2d8aff05f9`  
		Last Modified: Thu, 18 Dec 2025 01:34:52 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:cee00a47bf7b8b5899a6cf1f5c692494df31b454f52b81f3c4886905a0c9bdd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5270304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d91d78dbe118f2b7b0d6e850e1115de72c4fe3e30c55a5b53d8a844d14357d16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:30:56 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:30:57 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:33:51 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:33:51 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:33:51 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:33:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:33:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:33:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:33:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:33:51 GMT
USER memcache
# Thu, 18 Dec 2025 00:33:51 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:33:51 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:43 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa22c446792763e48f4680945ccc68d43c7906ef35a92e0b908f57ef53e72f0`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954155078f2265364295ebdf16fb114e991b1938d8a6951fb511163ab3b2b385`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 92.4 KB (92378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a25584b03ac5e45c66c3c616acfd9df1848e5db25219ef20feb2868c30c6332`  
		Last Modified: Thu, 18 Dec 2025 00:33:57 GMT  
		Size: 1.9 MB (1897191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f237be962bb57c3f749904b5925c8e1d7e9013dfac7dd52cc9611ada81858e`  
		Last Modified: Thu, 18 Dec 2025 00:33:57 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b07d9170b246a631c262d9f5d57f49278f7cd4805463b90b14aeca4dc61d93`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:64abe011fed6a9cf7b3290c752c50bffe81bb2e65cf6337e023efda87d49b451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b251b9c15ab7c5742bd3ab725df09f0ecb9f2491f92cf1c825bec598a31f4407`

```dockerfile
```

-	Layers:
	-	`sha256:1882c6d4361100a29fd5ab265587f65fa27b1df15e7f9349b30dac454facf98e`  
		Last Modified: Thu, 18 Dec 2025 00:33:57 GMT  
		Size: 94.3 KB (94291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf0a88ab3838de6beab653497ab62a64cfb87b1dc83c5fa5b6f3907abfd88080`  
		Last Modified: Thu, 18 Dec 2025 01:34:56 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:b6c3042e2bf09ec3d3f054d03b81313e8df717a49371ce916ff743e602796bc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6285509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6691028570bbd843e6da26558c46162b8383212fcaaefcecb2d3f919e3401429`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:18 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:29:19 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:32:06 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:32:06 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:32:06 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:32:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:32:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:32:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:32:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:32:06 GMT
USER memcache
# Thu, 18 Dec 2025 00:32:06 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:32:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb7b8445facedfc145b9478f74880f520776460f153005b7f437ec339aee530`  
		Last Modified: Thu, 18 Dec 2025 00:32:11 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1853c901134389608b6e80aaa3e43cd67a35c71aecfdde4b5b7ed3b989a03c`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 121.9 KB (121860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a01d1ac5ce47f4494363e411e1cd25dea26438213a2d18d6bb104d0974d9a52`  
		Last Modified: Thu, 18 Dec 2025 00:32:11 GMT  
		Size: 2.0 MB (1966561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115624f24ba74d393c2da3d65ed5b35a7afb3fa9ad143d3fb82c64953b3d0401`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87bba524314294ca97195ce65a35ec6d42d3f9f18c9cc0c05c064c9a3cf85c0`  
		Last Modified: Thu, 18 Dec 2025 00:32:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:2feda8921a7d67cd9f2f3d7186ed69ceb0d3c22af7a20bd230664e9bcf39096c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d73c6548a24cc8ce7782d03377e89a4b4b0e4c2a48cd3a03a79193320fc4d834`

```dockerfile
```

-	Layers:
	-	`sha256:984e438122735983bf56bc3d638fb1b0baf8cfb26ce26f71e0a9b847d25f76b5`  
		Last Modified: Thu, 18 Dec 2025 01:34:59 GMT  
		Size: 94.3 KB (94327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d6e8d91ca57b45f0050ec3833a8f09a7ce62f7ba9ec70e1ae12881ad4b2bb6f`  
		Last Modified: Thu, 18 Dec 2025 01:35:00 GMT  
		Size: 20.7 KB (20728 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; 386

```console
$ docker pull memcached@sha256:df1ba8af73cd6e3f8227557b097cd6b128ec0d410a3bbe7a2c282089c5641b41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5740953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78dbfc1f8ea65ad6466795e278180963d4afe98dfbca4a4497bc73c99f07ed4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:13:19 GMT
ADD alpine-minirootfs-3.23.2-x86.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:13:19 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:43 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:29:44 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:32:29 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:32:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:32:29 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:32:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:32:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:32:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:32:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:32:29 GMT
USER memcache
# Thu, 18 Dec 2025 00:32:29 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:32:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c21df6a7383dfce37a4bfe31b291881f55907c419caf5d06cb6d699d290d0718`  
		Last Modified: Thu, 18 Dec 2025 00:13:38 GMT  
		Size: 3.7 MB (3686100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37ec5bf455c1d98d22e6f3dacb5b971dac8ea96d1fe9b9177a07c5277530646`  
		Last Modified: Thu, 18 Dec 2025 00:32:35 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b2862af05c1582c8625c82ea0863dc2b6474e410d3e6a32876c920e0152c73`  
		Last Modified: Thu, 18 Dec 2025 00:32:35 GMT  
		Size: 110.7 KB (110740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30872a43f6c591fd9b979b49b0fb32107b4bfa8c1155657fa255aa199cf0b83b`  
		Last Modified: Thu, 18 Dec 2025 00:32:35 GMT  
		Size: 1.9 MB (1942762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a62c11b4aeceaba2e5e73a1bc29aa8b4fc42ccd0c7e8512cc11b96e48aef2f`  
		Last Modified: Thu, 18 Dec 2025 00:32:41 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f553d362a11992264bf5364cfe13d248403c5baf2ecac784c26f444dbfb90388`  
		Last Modified: Thu, 18 Dec 2025 00:32:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:e3b020c2afd9ae372e234c6ab67456908861fd24200448fd3cf741503a8a6f55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6abfcddfb1575f6cc07e51c6a379141589de7ea8c329a9bc5c1592f3186e6fda`

```dockerfile
```

-	Layers:
	-	`sha256:ff9be8ef1bab92275eb15ae5fd6a05e767abc1fe855455766200b3c0a1866e33`  
		Last Modified: Thu, 18 Dec 2025 01:35:03 GMT  
		Size: 94.8 KB (94828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d7026bdf84e278b6976f0ccab2297ddc0284cf329414f56d12608dbc2acb940`  
		Last Modified: Thu, 18 Dec 2025 00:32:35 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:7292c7b145e08f87f78644bf2c3355fad1d0b4d9366f173ffa0634c3ec93addf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6031729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ae72ba97ecea986f01bda1eb392aee1ded4b5a86b2edcabe92a2034143e155b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:33:41 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:33:42 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:36:14 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:36:14 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:36:14 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:36:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:36:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:36:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:36:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:36:14 GMT
USER memcache
# Thu, 18 Dec 2025 00:36:14 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:36:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c95450233dfe3e06529eb39ca4b46e6ad51ccf338cab64157669ff1fc0a8d72`  
		Last Modified: Thu, 18 Dec 2025 00:36:26 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4079a2d61bafcf146b8f57b35f0e39bf2548e0963be10cff5086f9a56ccdd9d`  
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
		Size: 126.3 KB (126257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f69efa1066815d67cf415d0aac5dcd305032257b6bded5a4c57a7444a1e7fd4`  
		Last Modified: Thu, 18 Dec 2025 00:36:26 GMT  
		Size: 2.1 MB (2076363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357f4165f53a3d4c66ef270bcb5b5283a066af50f79924cccc7c73f6a4f6f4ab`  
		Last Modified: Thu, 18 Dec 2025 00:36:36 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a65ff5cefcbfc874c1cac0857339eaee0b07147dd26b6bfa18c00921b4f30c`  
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:1d06281345f2ac44a607d40d5e87de6abb99bbc6ee82d319e73f3794602d0282
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4867a5aa08041c7e5ec69dfc84214226a7323d1ce703747ae2117675e2f74bcd`

```dockerfile
```

-	Layers:
	-	`sha256:282960f007d3f1f008333191d98a2ded5ff0f83075ace30043349b6c082c18fd`  
		Last Modified: Thu, 18 Dec 2025 01:35:08 GMT  
		Size: 94.3 KB (94280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4755fffd5924e8405adfbed0f328ad9792eff20e2b8ad2025e1f5c85bca88618`  
		Last Modified: Thu, 18 Dec 2025 01:35:09 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:9023f4a863c531a74c6ff8cc3b49c3be80ad1db07cc93fdcbf87c5d8e4cccc72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5768619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2159b7b74e5ffe77e6304def07dec2cfc2bdead26c3012e1e4d39bcd267adfe5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 06:39:34 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 06:39:38 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 06:52:53 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 06:52:53 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 06:52:53 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 06:52:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 06:52:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 06:52:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 06:52:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 06:52:53 GMT
USER memcache
# Thu, 18 Dec 2025 06:52:53 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 06:52:53 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc016d1883c21894ae540944be0270a95cb663037e8592a944bac62e0cc39e7`  
		Last Modified: Thu, 18 Dec 2025 06:53:25 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c580cd51da178bea3e44467f8b445f50ec9272e42e0254d269a9e38204b12dc`  
		Last Modified: Thu, 18 Dec 2025 06:53:25 GMT  
		Size: 108.9 KB (108898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11881c79ebc6a05357f0e2095f00d6d5a8a58bd9f11efeefc80b616d0230ff9`  
		Last Modified: Thu, 18 Dec 2025 06:53:25 GMT  
		Size: 2.1 MB (2074429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735bfa953d895df9672fe0b34207075bd7e686f71104973ad4e02d89db8719a9`  
		Last Modified: Thu, 18 Dec 2025 06:53:25 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b8c865432ff9b07178ba7cb96426e0515b00cc91866fb4dfb8c243e4187172`  
		Last Modified: Thu, 18 Dec 2025 06:53:25 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7cd6a8f4c278ff9062def241e6cdb501032ed72b091608a6da35812eece0954c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38b0c310a1ad4186c4beae0e268b71f1a80ed998cd80ceb81095aa9da7e6b02e`

```dockerfile
```

-	Layers:
	-	`sha256:88642ee1ee3c124ff8f2f640525172206ce9483620a70142ca673e0eca181c4d`  
		Last Modified: Thu, 18 Dec 2025 07:34:34 GMT  
		Size: 94.3 KB (94276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:441bda294fdd657b4574cd5337193125e3d0565433a700136501a858fce53d46`  
		Last Modified: Thu, 18 Dec 2025 07:34:34 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; s390x

```console
$ docker pull memcached@sha256:e011484878fd5d1e2da6de478ac11d01ae80f0bdef1902dcde3ed53728803741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5857090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:689ea71c305b80e206c68a215481290a1378e6375e32ad059455f7d041396aa6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:30:26 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:30:27 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:33:46 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:33:46 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:33:46 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:33:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:33:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:33:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:33:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:33:46 GMT
USER memcache
# Thu, 18 Dec 2025 00:33:46 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:33:46 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4594a6826f7ed03c8c4f9f2aebb9716eb6e16d5b5ab7e1bc247783b503c5b10`  
		Last Modified: Thu, 18 Dec 2025 00:33:55 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f270744f8d8b82bc6657387109b33836a76d6dbf8faa645a997db7ea290cdb`  
		Last Modified: Thu, 18 Dec 2025 00:33:55 GMT  
		Size: 114.3 KB (114299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91f8ee8f36703944a7bdcaf57cc5772fe9f79c74a088c33fa1b6da7de119f93`  
		Last Modified: Thu, 18 Dec 2025 00:33:55 GMT  
		Size: 2.0 MB (2017131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e21d2db88668745770273c7b36d4d2c1e87a80b0118b8d775813860b467384c8`  
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd847159e169b898a67d4454fd5a22406c5ae623b16889d084a1d5f2d46a499`  
		Last Modified: Thu, 18 Dec 2025 00:33:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:33ab737cb23dcde22de59a58e40f1f80d2c5e808ff3036519ae7d9db228fa37d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3562f7fd7806da24b1865c01a2246ac041b5e98d69c10ce6cbbe479f9408f9a1`

```dockerfile
```

-	Layers:
	-	`sha256:d5f43e64a79ee525bd0354a06e3284444fd642bbe6c1a782aa45ec2e20462f1d`  
		Last Modified: Thu, 18 Dec 2025 01:35:19 GMT  
		Size: 94.2 KB (94222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bd2c024010f4f53d350bde9967c349efb3a58a2a812b14e17b29ddbd19eab87`  
		Last Modified: Thu, 18 Dec 2025 01:35:20 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine3.23`

```console
$ docker pull memcached@sha256:c77536380fd3c7740933767bb5279bd30e31c8d496081e5113a37d9b9eec43cb
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
$ docker pull memcached@sha256:9573a2399011fa86bb7b5d12bdab987d7931c98ddec0ef6802de7eb6d3c3e338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5956768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c79853acc5f24e9c28f15d45cef0aedc114e76bbacf7958eb6f555c22246e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:34 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:29:34 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:32:07 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:32:07 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:32:07 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:32:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:32:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:32:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:32:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:32:07 GMT
USER memcache
# Thu, 18 Dec 2025 00:32:07 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:32:07 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:48:50 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57c33ac8581cd04f31208409f36331e938a78e6ae3a7a3b530fe9dfebe6eb9ad`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583aae99135b9036c602a1c60743fc4fd519f261ac6d48ed60b01e1beb019e7f`  
		Last Modified: Thu, 18 Dec 2025 00:32:12 GMT  
		Size: 106.0 KB (106050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ca22885c42a537f033850e8dff7eaeddbb7514902286739b48c084b55a8d6b`  
		Last Modified: Thu, 18 Dec 2025 00:32:12 GMT  
		Size: 2.0 MB (1989265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d146e2038834770bed57033a6c5d66ead5b731b8b133856dec6726ca21baee9`  
		Last Modified: Thu, 18 Dec 2025 00:32:12 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c66e6c3acbe07806e3e96a97d97a2d4503713c4814d9b24a2f57f2c39200d05`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:cfdf2ea6bf2a04bb7ee1568efe0c8bd38a1f5e644250a9409479cce281891ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de792623281192b3965fdc95f31532c4d166e731f53e202be1e2a224c654633b`

```dockerfile
```

-	Layers:
	-	`sha256:87a0d23eeeda6353dfc603cc4ffee062e5383be07b611754f3a88db3fc644036`  
		Last Modified: Thu, 18 Dec 2025 00:32:12 GMT  
		Size: 94.9 KB (94873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b73cd5efe31baa1fbf0eecea269426edcfc795cbb9b5dd74b523ff51b6f7c9f`  
		Last Modified: Thu, 18 Dec 2025 01:34:48 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.23` - linux; arm variant v6

```console
$ docker pull memcached@sha256:c1a12b64cc8b47f50ea4610d9c1c362da7157b3ba67deac8b4760e6b589cde75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5611647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3591f95cad049a0509bd23a95556f8f848452d2a5491ed00bae293897c7a6b2f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:27:48 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:27:49 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:49:50 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:49:50 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:49:50 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:49:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:49:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:49:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:49:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:49:50 GMT
USER memcache
# Thu, 18 Dec 2025 00:49:50 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:49:50 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf585eb2bfa372c2097b9f7a5214ecb0941a30581b10fb74a26518fcc7addec`  
		Last Modified: Thu, 18 Dec 2025 00:49:55 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01bb148ea8fbe93dd8097d85f9ee3cf547d314e669748b4239c05711b0d5f719`  
		Last Modified: Thu, 18 Dec 2025 00:49:55 GMT  
		Size: 102.7 KB (102652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6549359cda37ac41cf41a5ece5f37f1322a82f6b232f12e446c62840637093e`  
		Last Modified: Thu, 18 Dec 2025 00:50:02 GMT  
		Size: 1.9 MB (1939215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:041e37eaffefcfb0809564ddea591be3cd818de5530e2c853c0bc9a2fa25c116`  
		Last Modified: Thu, 18 Dec 2025 00:49:55 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7907ae218c75b36c9a9002be8554131c271cde78b0280cb7a85029f99ad0bcdc`  
		Last Modified: Thu, 18 Dec 2025 00:50:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:a9c26fc290551b691574e093d3c28f4fe7b558b3f8173b3c99eb8a664c83a8e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ca65d7156e6586d96310ea3162facd9849d5460d2939b461a25247b06a4d59`

```dockerfile
```

-	Layers:
	-	`sha256:d9c217dc241f1175812c47b6489d325a0574c0da554c6f8aa0b86a2d8aff05f9`  
		Last Modified: Thu, 18 Dec 2025 01:34:52 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.23` - linux; arm variant v7

```console
$ docker pull memcached@sha256:cee00a47bf7b8b5899a6cf1f5c692494df31b454f52b81f3c4886905a0c9bdd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5270304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d91d78dbe118f2b7b0d6e850e1115de72c4fe3e30c55a5b53d8a844d14357d16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:30:56 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:30:57 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:33:51 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:33:51 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:33:51 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:33:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:33:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:33:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:33:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:33:51 GMT
USER memcache
# Thu, 18 Dec 2025 00:33:51 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:33:51 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:43 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa22c446792763e48f4680945ccc68d43c7906ef35a92e0b908f57ef53e72f0`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954155078f2265364295ebdf16fb114e991b1938d8a6951fb511163ab3b2b385`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 92.4 KB (92378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a25584b03ac5e45c66c3c616acfd9df1848e5db25219ef20feb2868c30c6332`  
		Last Modified: Thu, 18 Dec 2025 00:33:57 GMT  
		Size: 1.9 MB (1897191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f237be962bb57c3f749904b5925c8e1d7e9013dfac7dd52cc9611ada81858e`  
		Last Modified: Thu, 18 Dec 2025 00:33:57 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b07d9170b246a631c262d9f5d57f49278f7cd4805463b90b14aeca4dc61d93`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:64abe011fed6a9cf7b3290c752c50bffe81bb2e65cf6337e023efda87d49b451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b251b9c15ab7c5742bd3ab725df09f0ecb9f2491f92cf1c825bec598a31f4407`

```dockerfile
```

-	Layers:
	-	`sha256:1882c6d4361100a29fd5ab265587f65fa27b1df15e7f9349b30dac454facf98e`  
		Last Modified: Thu, 18 Dec 2025 00:33:57 GMT  
		Size: 94.3 KB (94291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf0a88ab3838de6beab653497ab62a64cfb87b1dc83c5fa5b6f3907abfd88080`  
		Last Modified: Thu, 18 Dec 2025 01:34:56 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.23` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:b6c3042e2bf09ec3d3f054d03b81313e8df717a49371ce916ff743e602796bc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6285509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6691028570bbd843e6da26558c46162b8383212fcaaefcecb2d3f919e3401429`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:18 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:29:19 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:32:06 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:32:06 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:32:06 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:32:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:32:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:32:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:32:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:32:06 GMT
USER memcache
# Thu, 18 Dec 2025 00:32:06 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:32:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb7b8445facedfc145b9478f74880f520776460f153005b7f437ec339aee530`  
		Last Modified: Thu, 18 Dec 2025 00:32:11 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1853c901134389608b6e80aaa3e43cd67a35c71aecfdde4b5b7ed3b989a03c`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 121.9 KB (121860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a01d1ac5ce47f4494363e411e1cd25dea26438213a2d18d6bb104d0974d9a52`  
		Last Modified: Thu, 18 Dec 2025 00:32:11 GMT  
		Size: 2.0 MB (1966561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115624f24ba74d393c2da3d65ed5b35a7afb3fa9ad143d3fb82c64953b3d0401`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87bba524314294ca97195ce65a35ec6d42d3f9f18c9cc0c05c064c9a3cf85c0`  
		Last Modified: Thu, 18 Dec 2025 00:32:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:2feda8921a7d67cd9f2f3d7186ed69ceb0d3c22af7a20bd230664e9bcf39096c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d73c6548a24cc8ce7782d03377e89a4b4b0e4c2a48cd3a03a79193320fc4d834`

```dockerfile
```

-	Layers:
	-	`sha256:984e438122735983bf56bc3d638fb1b0baf8cfb26ce26f71e0a9b847d25f76b5`  
		Last Modified: Thu, 18 Dec 2025 01:34:59 GMT  
		Size: 94.3 KB (94327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d6e8d91ca57b45f0050ec3833a8f09a7ce62f7ba9ec70e1ae12881ad4b2bb6f`  
		Last Modified: Thu, 18 Dec 2025 01:35:00 GMT  
		Size: 20.7 KB (20728 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.23` - linux; 386

```console
$ docker pull memcached@sha256:df1ba8af73cd6e3f8227557b097cd6b128ec0d410a3bbe7a2c282089c5641b41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5740953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78dbfc1f8ea65ad6466795e278180963d4afe98dfbca4a4497bc73c99f07ed4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:13:19 GMT
ADD alpine-minirootfs-3.23.2-x86.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:13:19 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:43 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:29:44 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:32:29 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:32:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:32:29 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:32:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:32:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:32:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:32:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:32:29 GMT
USER memcache
# Thu, 18 Dec 2025 00:32:29 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:32:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c21df6a7383dfce37a4bfe31b291881f55907c419caf5d06cb6d699d290d0718`  
		Last Modified: Thu, 18 Dec 2025 00:13:38 GMT  
		Size: 3.7 MB (3686100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37ec5bf455c1d98d22e6f3dacb5b971dac8ea96d1fe9b9177a07c5277530646`  
		Last Modified: Thu, 18 Dec 2025 00:32:35 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b2862af05c1582c8625c82ea0863dc2b6474e410d3e6a32876c920e0152c73`  
		Last Modified: Thu, 18 Dec 2025 00:32:35 GMT  
		Size: 110.7 KB (110740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30872a43f6c591fd9b979b49b0fb32107b4bfa8c1155657fa255aa199cf0b83b`  
		Last Modified: Thu, 18 Dec 2025 00:32:35 GMT  
		Size: 1.9 MB (1942762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a62c11b4aeceaba2e5e73a1bc29aa8b4fc42ccd0c7e8512cc11b96e48aef2f`  
		Last Modified: Thu, 18 Dec 2025 00:32:41 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f553d362a11992264bf5364cfe13d248403c5baf2ecac784c26f444dbfb90388`  
		Last Modified: Thu, 18 Dec 2025 00:32:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:e3b020c2afd9ae372e234c6ab67456908861fd24200448fd3cf741503a8a6f55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6abfcddfb1575f6cc07e51c6a379141589de7ea8c329a9bc5c1592f3186e6fda`

```dockerfile
```

-	Layers:
	-	`sha256:ff9be8ef1bab92275eb15ae5fd6a05e767abc1fe855455766200b3c0a1866e33`  
		Last Modified: Thu, 18 Dec 2025 01:35:03 GMT  
		Size: 94.8 KB (94828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d7026bdf84e278b6976f0ccab2297ddc0284cf329414f56d12608dbc2acb940`  
		Last Modified: Thu, 18 Dec 2025 00:32:35 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.23` - linux; ppc64le

```console
$ docker pull memcached@sha256:7292c7b145e08f87f78644bf2c3355fad1d0b4d9366f173ffa0634c3ec93addf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6031729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ae72ba97ecea986f01bda1eb392aee1ded4b5a86b2edcabe92a2034143e155b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:33:41 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:33:42 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:36:14 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:36:14 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:36:14 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:36:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:36:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:36:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:36:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:36:14 GMT
USER memcache
# Thu, 18 Dec 2025 00:36:14 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:36:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c95450233dfe3e06529eb39ca4b46e6ad51ccf338cab64157669ff1fc0a8d72`  
		Last Modified: Thu, 18 Dec 2025 00:36:26 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4079a2d61bafcf146b8f57b35f0e39bf2548e0963be10cff5086f9a56ccdd9d`  
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
		Size: 126.3 KB (126257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f69efa1066815d67cf415d0aac5dcd305032257b6bded5a4c57a7444a1e7fd4`  
		Last Modified: Thu, 18 Dec 2025 00:36:26 GMT  
		Size: 2.1 MB (2076363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357f4165f53a3d4c66ef270bcb5b5283a066af50f79924cccc7c73f6a4f6f4ab`  
		Last Modified: Thu, 18 Dec 2025 00:36:36 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a65ff5cefcbfc874c1cac0857339eaee0b07147dd26b6bfa18c00921b4f30c`  
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:1d06281345f2ac44a607d40d5e87de6abb99bbc6ee82d319e73f3794602d0282
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4867a5aa08041c7e5ec69dfc84214226a7323d1ce703747ae2117675e2f74bcd`

```dockerfile
```

-	Layers:
	-	`sha256:282960f007d3f1f008333191d98a2ded5ff0f83075ace30043349b6c082c18fd`  
		Last Modified: Thu, 18 Dec 2025 01:35:08 GMT  
		Size: 94.3 KB (94280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4755fffd5924e8405adfbed0f328ad9792eff20e2b8ad2025e1f5c85bca88618`  
		Last Modified: Thu, 18 Dec 2025 01:35:09 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.23` - linux; riscv64

```console
$ docker pull memcached@sha256:9023f4a863c531a74c6ff8cc3b49c3be80ad1db07cc93fdcbf87c5d8e4cccc72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5768619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2159b7b74e5ffe77e6304def07dec2cfc2bdead26c3012e1e4d39bcd267adfe5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 06:39:34 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 06:39:38 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 06:52:53 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 06:52:53 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 06:52:53 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 06:52:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 06:52:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 06:52:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 06:52:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 06:52:53 GMT
USER memcache
# Thu, 18 Dec 2025 06:52:53 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 06:52:53 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc016d1883c21894ae540944be0270a95cb663037e8592a944bac62e0cc39e7`  
		Last Modified: Thu, 18 Dec 2025 06:53:25 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c580cd51da178bea3e44467f8b445f50ec9272e42e0254d269a9e38204b12dc`  
		Last Modified: Thu, 18 Dec 2025 06:53:25 GMT  
		Size: 108.9 KB (108898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11881c79ebc6a05357f0e2095f00d6d5a8a58bd9f11efeefc80b616d0230ff9`  
		Last Modified: Thu, 18 Dec 2025 06:53:25 GMT  
		Size: 2.1 MB (2074429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735bfa953d895df9672fe0b34207075bd7e686f71104973ad4e02d89db8719a9`  
		Last Modified: Thu, 18 Dec 2025 06:53:25 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b8c865432ff9b07178ba7cb96426e0515b00cc91866fb4dfb8c243e4187172`  
		Last Modified: Thu, 18 Dec 2025 06:53:25 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:7cd6a8f4c278ff9062def241e6cdb501032ed72b091608a6da35812eece0954c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38b0c310a1ad4186c4beae0e268b71f1a80ed998cd80ceb81095aa9da7e6b02e`

```dockerfile
```

-	Layers:
	-	`sha256:88642ee1ee3c124ff8f2f640525172206ce9483620a70142ca673e0eca181c4d`  
		Last Modified: Thu, 18 Dec 2025 07:34:34 GMT  
		Size: 94.3 KB (94276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:441bda294fdd657b4574cd5337193125e3d0565433a700136501a858fce53d46`  
		Last Modified: Thu, 18 Dec 2025 07:34:34 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.23` - linux; s390x

```console
$ docker pull memcached@sha256:e011484878fd5d1e2da6de478ac11d01ae80f0bdef1902dcde3ed53728803741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5857090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:689ea71c305b80e206c68a215481290a1378e6375e32ad059455f7d041396aa6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:30:26 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 00:30:27 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 00:33:46 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 00:33:46 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 00:33:46 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 00:33:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 00:33:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:33:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 00:33:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:33:46 GMT
USER memcache
# Thu, 18 Dec 2025 00:33:46 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 00:33:46 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4594a6826f7ed03c8c4f9f2aebb9716eb6e16d5b5ab7e1bc247783b503c5b10`  
		Last Modified: Thu, 18 Dec 2025 00:33:55 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f270744f8d8b82bc6657387109b33836a76d6dbf8faa645a997db7ea290cdb`  
		Last Modified: Thu, 18 Dec 2025 00:33:55 GMT  
		Size: 114.3 KB (114299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91f8ee8f36703944a7bdcaf57cc5772fe9f79c74a088c33fa1b6da7de119f93`  
		Last Modified: Thu, 18 Dec 2025 00:33:55 GMT  
		Size: 2.0 MB (2017131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e21d2db88668745770273c7b36d4d2c1e87a80b0118b8d775813860b467384c8`  
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd847159e169b898a67d4454fd5a22406c5ae623b16889d084a1d5f2d46a499`  
		Last Modified: Thu, 18 Dec 2025 00:33:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:33ab737cb23dcde22de59a58e40f1f80d2c5e808ff3036519ae7d9db228fa37d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3562f7fd7806da24b1865c01a2246ac041b5e98d69c10ce6cbbe479f9408f9a1`

```dockerfile
```

-	Layers:
	-	`sha256:d5f43e64a79ee525bd0354a06e3284444fd642bbe6c1a782aa45ec2e20462f1d`  
		Last Modified: Thu, 18 Dec 2025 01:35:19 GMT  
		Size: 94.2 KB (94222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bd2c024010f4f53d350bde9967c349efb3a58a2a812b14e17b29ddbd19eab87`  
		Last Modified: Thu, 18 Dec 2025 01:35:20 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:latest`

```console
$ docker pull memcached@sha256:e4e5eca37e4334f9579f10fcdd88a58c4eb9d0a8eacedde6ec49d4ea4391637a
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
$ docker pull memcached@sha256:1613c35e314db0c64d8b5679786ad99ced10069c3f9778d40b6c522ff3c04218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32190619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a38251b773d15614da3036dd0d756bbf4a7d16d27fe1c52023517a419372b245`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:22:30 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 13 Jan 2026 01:22:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:25:18 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 13 Jan 2026 01:25:18 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 13 Jan 2026 01:25:18 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 13 Jan 2026 01:25:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 13 Jan 2026 01:25:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:25:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 01:25:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:25:18 GMT
USER memcache
# Tue, 13 Jan 2026 01:25:18 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 13 Jan 2026 01:25:18 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:34 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b6e737e1a3eed198cc17e2b92231ab084bcf55ba90a36136e7a2f4fd04a95b`  
		Last Modified: Tue, 13 Jan 2026 01:25:30 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16835fec399670b74d32630a7368a65ca2a3c32d8b7a690d33bebc7b9e9458d`  
		Last Modified: Tue, 13 Jan 2026 01:25:30 GMT  
		Size: 136.7 KB (136737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c848acbad27f1c9d2fd95e0facabbb28d5d8be19e5fa5912e5474c1301522523`  
		Last Modified: Tue, 13 Jan 2026 01:25:25 GMT  
		Size: 2.3 MB (2278686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9529916038b7840d3177e93bf04b78390bb91bca78623bd9c0769f9e2a965079`  
		Last Modified: Tue, 13 Jan 2026 01:25:25 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24239fc168f5eb73ae9964e2cdcb3c3b878ae79835c6b94585cb648fd50479d`  
		Last Modified: Tue, 13 Jan 2026 01:25:26 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:0d72ad7b507d17cffe5dbec1ddecf1c254c3a85d2b605fa0ddbc9913ba4fc678
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe582f0cad77d385a3debb0f2acf0c96b7b85c6a7d2c95fcc54f938d63635c9`

```dockerfile
```

-	Layers:
	-	`sha256:7d598d8c3b4cd06481693da06e86554144167d205cc60f43382fafba94dd4592`  
		Last Modified: Tue, 13 Jan 2026 04:35:37 GMT  
		Size: 2.0 MB (2008290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dd2469227ab0e75822eb9d56a5d7c05f52a445840f65934e010a2562e509718`  
		Last Modified: Tue, 13 Jan 2026 01:25:24 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm variant v5

```console
$ docker pull memcached@sha256:efa6728c05b024b605597e5025f04155aab614b52f56b1b31a4c70a23f909e07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30298859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14119dc07998a4322ac912beaaf4e6ad16e5487f2243c332fdaad86bdce6f55e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:19:21 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 13 Jan 2026 01:19:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:22:43 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 13 Jan 2026 01:22:43 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 13 Jan 2026 01:22:43 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 13 Jan 2026 01:22:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 13 Jan 2026 01:22:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:22:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 01:22:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:22:43 GMT
USER memcache
# Tue, 13 Jan 2026 01:22:43 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 13 Jan 2026 01:22:43 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c113d410d30c2c035a105b56d3937958c81fbe2530f44add3bae903be6864324`  
		Last Modified: Tue, 13 Jan 2026 00:42:30 GMT  
		Size: 27.9 MB (27942724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96776850dc1206c3fd163b84cea19599306159eb0d020b4241d0172240f88d13`  
		Last Modified: Tue, 13 Jan 2026 01:22:55 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3697c7c790d9c4caaa904abdaf809dcdee3f0b518fc5ad82d2e21dd7fe24f64d`  
		Last Modified: Tue, 13 Jan 2026 01:22:55 GMT  
		Size: 144.2 KB (144212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a247339c7ec57a491c3ffe43531dbfaa132f3ff16a481fc41cbb9e3e3ad6476`  
		Last Modified: Tue, 13 Jan 2026 01:22:50 GMT  
		Size: 2.2 MB (2210412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2dcebe3ab2a9945cdea142301e4a64eebbc59c948a54385dbfca4afd561b508`  
		Last Modified: Tue, 13 Jan 2026 01:22:55 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb8ef5ecbc44efd5280f9cf15687dfd80a34fa2966ad039238647177f75dc6c`  
		Last Modified: Tue, 13 Jan 2026 01:22:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:190bb1ecd7376720e541621921c2d4931a9d0f85a047255ba2b56afa3a504212
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9736e9545a46e4ef65dcb5238691292d27fac4dccb330354ce59ac93ae6994b5`

```dockerfile
```

-	Layers:
	-	`sha256:4f5461bf596f750b56b3f10e315936c2326b2c32901d28cdf22db97072bba685`  
		Last Modified: Tue, 13 Jan 2026 01:22:50 GMT  
		Size: 2.0 MB (2011293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8657d28d0436d39193457fb90119ea6e4ddb566df2a83fd1aa9df75651731188`  
		Last Modified: Tue, 13 Jan 2026 04:35:43 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm variant v7

```console
$ docker pull memcached@sha256:9c322c838b4648fa30e742e53ed6647a31383760fb73fa82de32b4b6dc88c494
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28509532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6e130248535c57fccff4d89a9d442e31cabd471e41c9eed52e5207a54f9f944`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:25:47 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 13 Jan 2026 01:25:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:28:55 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 13 Jan 2026 01:28:55 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 13 Jan 2026 01:28:55 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 13 Jan 2026 01:28:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 13 Jan 2026 01:28:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:28:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 01:28:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:28:55 GMT
USER memcache
# Tue, 13 Jan 2026 01:28:55 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 13 Jan 2026 01:28:55 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029a2cbe46c1e12ab6d47a63f40fb29056b6c6277c7822085ed0fe62e0a1791d`  
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c7827f95482598f1bd32dd8cbe071ad009795fa108661234eeb872d1a1e8bd`  
		Last Modified: Tue, 13 Jan 2026 01:29:07 GMT  
		Size: 135.4 KB (135398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9371e974781bd91adc657086f00cd7d91b5530ca9da37597c347dd7d4eaff0`  
		Last Modified: Tue, 13 Jan 2026 01:29:07 GMT  
		Size: 2.2 MB (2164040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c2e0f64c0afa16b5e214ae208c8c81e8c78c79ddd90f54983a93c7297395f6b`  
		Last Modified: Tue, 13 Jan 2026 01:29:07 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92151d443057f88ed7f60405440b698ff9e6abe1a2ca1c91a0c7e7626339ad2`  
		Last Modified: Tue, 13 Jan 2026 01:29:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:12cc31a1ce56d2c6dd1c0dcfd4ef1fe74484985d010594950c086c0f4431559b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b2d844d5393973080c37fde0b92cd48bd1a64e03973290631be5486d814de7e`

```dockerfile
```

-	Layers:
	-	`sha256:99fc27444c1ccdd6cbd08a33aac22e9e85f55958bda7b6216bdea08eae374cff`  
		Last Modified: Tue, 13 Jan 2026 04:35:47 GMT  
		Size: 2.0 MB (2009750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e76d5584f581b7668c61a661da2858bc1d5e11b31e3629e0d2b3af52d9c22ed8`  
		Last Modified: Tue, 13 Jan 2026 04:35:47 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:2ed537fa0376a3eb0864d6a3b51ea7da59b9ff4bb3270189a8a5082f02f811e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32550406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf26d75d787aabbd202c97db1079b96e45105d3ca509a1001ab973cb473cae8c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:22:29 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 13 Jan 2026 01:22:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:25:26 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 13 Jan 2026 01:25:26 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 13 Jan 2026 01:25:26 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 13 Jan 2026 01:25:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 13 Jan 2026 01:25:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:25:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 01:25:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:25:27 GMT
USER memcache
# Tue, 13 Jan 2026 01:25:27 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 13 Jan 2026 01:25:27 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78edb6b991369235f90958a936afc89dc37b82439c632988ed143b5bd76deadb`  
		Last Modified: Tue, 13 Jan 2026 01:25:40 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e1afbb765f6cc3923e864d44fb6cd6c9167b884e596b09bd37c7c276f65a2b`  
		Last Modified: Tue, 13 Jan 2026 01:25:40 GMT  
		Size: 153.5 KB (153512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff9edc68fe57c233001afd442eb6c248bf070d32fbb412a8bfeef6f9a6217f5`  
		Last Modified: Tue, 13 Jan 2026 01:25:40 GMT  
		Size: 2.3 MB (2261341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c4648fbc4a4189184946895d1041e0eee2c5d40fd70638a553bedb0cbf5cf8`  
		Last Modified: Tue, 13 Jan 2026 01:25:40 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26bd1b32b048e73091ddf6e6762e368d4bb6ef2cc7d3aa43467749b36fe08e38`  
		Last Modified: Tue, 13 Jan 2026 01:25:40 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:72333c6222fb20b5a9f9f92b8d56c47ebb5b4e6cd65512a6b5172ad0c0cade67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a2a4e23cbe2d062f3fcfb84c8590190eb72294786a0b8238add858e67a93914`

```dockerfile
```

-	Layers:
	-	`sha256:1f8545bcc66309a59381c88c4c87b0f8352893dbaa167be48947976c1e0cef1d`  
		Last Modified: Tue, 13 Jan 2026 04:35:51 GMT  
		Size: 2.0 MB (2008606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95e6875e372e1d6a9660c08726cb96d08b272e52a2446f275089efccfc3096b3`  
		Last Modified: Tue, 13 Jan 2026 01:25:33 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; 386

```console
$ docker pull memcached@sha256:29540e588e9065db9ecc8865fe74544260980d73786f00dfc4df3f3cee148bd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33661194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66843ae7a7d968c4f056a8e350dd84ff80a06e48b48c298c3427333b7ec259ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:19:43 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 13 Jan 2026 01:19:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:22:40 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 13 Jan 2026 01:22:40 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 13 Jan 2026 01:22:40 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 13 Jan 2026 01:22:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 13 Jan 2026 01:22:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:22:40 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 01:22:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:22:40 GMT
USER memcache
# Tue, 13 Jan 2026 01:22:40 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 13 Jan 2026 01:22:40 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:27bb6d39eda5ced7626db280c3902aacdfade5acd11a16ef9618e3185f69b102`  
		Last Modified: Tue, 13 Jan 2026 00:43:03 GMT  
		Size: 31.3 MB (31288476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cedb4f2840edea9de46e0d955a0512f469211880560a8948f10b54381bcd728`  
		Last Modified: Tue, 13 Jan 2026 01:22:53 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c4b2d1574ee5f238dc6948164abd39ffcc91929b2c464c6b3874dec01fd964`  
		Last Modified: Tue, 13 Jan 2026 01:22:46 GMT  
		Size: 147.6 KB (147554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc1bf5870b84175607f3d012b3cfebc5859869f8125114ea5d6ed1a05f81d2d`  
		Last Modified: Tue, 13 Jan 2026 01:22:53 GMT  
		Size: 2.2 MB (2223652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6434e73ed67e81f1016f27c7cc175290b0ce959d8a1bf5e9b0f3119f161246`  
		Last Modified: Tue, 13 Jan 2026 01:22:53 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abaf99fdf0e2b9620d20088b389b3f18eb67ad356c8c6c7961074e1428b8af0c`  
		Last Modified: Tue, 13 Jan 2026 01:22:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:f64192985f4635b04ce1ab99b3cae89f71d0b11f9670fb6d9c470158e3c5c63e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bb9ce834f23725c4bfc4fb2d6a24a96d3d0bc7685d3a759c0085871f34231e8`

```dockerfile
```

-	Layers:
	-	`sha256:ed9937c762728e5abc93b88bd7932a5762d2bc8e0001e81bb25ef0b27e2bc6ff`  
		Last Modified: Tue, 13 Jan 2026 04:35:56 GMT  
		Size: 2.0 MB (2005447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6358862e12c5c5367efd52bea0b1194e04e76f267084da591229f64ee7482dc3`  
		Last Modified: Tue, 13 Jan 2026 04:35:57 GMT  
		Size: 22.1 KB (22094 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; ppc64le

```console
$ docker pull memcached@sha256:309e0faad388272d7e37d6ee0cb354707d099e3140298105499711823d7a0eea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36161489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6f50ee10fc83da67b90c9bda7499251fa073fea87400d5fb70e31e693d6f902`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:33:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 13 Jan 2026 01:33:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:36:52 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 13 Jan 2026 01:36:52 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 13 Jan 2026 01:36:52 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 13 Jan 2026 01:36:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 13 Jan 2026 01:36:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:36:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 01:36:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:36:53 GMT
USER memcache
# Tue, 13 Jan 2026 01:36:53 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 13 Jan 2026 01:36:53 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9a275bb13cf8b3e9db52a41b6b4ff22ee1ffed00394f6deddd2de45044bd3bae`  
		Last Modified: Tue, 13 Jan 2026 00:57:13 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093e59deb53ff01a892be2a5df928c4b04a289df7f6c135570c11d6a4fdbc53a`  
		Last Modified: Tue, 13 Jan 2026 01:37:16 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4da25c8b13ee47050a38843c1954d2bd7bbdba2666f725aee2f603e03fcb6d`  
		Last Modified: Tue, 13 Jan 2026 01:37:16 GMT  
		Size: 170.4 KB (170427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cab5f6f805c735c0f324c87ff8c66cfab0e35fb691b7761e85bb9a2bbb31cfe`  
		Last Modified: Tue, 13 Jan 2026 01:37:16 GMT  
		Size: 2.4 MB (2393947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3a7dfc8da65bd6101de156530bc2688c5588c718bbc3131ff4594cbefd0e66`  
		Last Modified: Tue, 13 Jan 2026 01:37:09 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06153b2e2bde9b06f1c2719aabb5ff6a6c23056152a024fa2c990d97b4d9c799`  
		Last Modified: Tue, 13 Jan 2026 01:37:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:8dfcc685b38edcaec140b90716d19e543715184f20f7a401d6f734ad8f8cf1dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7442b6e23a86bfe5ee9a534d43f0a55ba9629d3c24128b1b3e2b5121644dcf00`

```dockerfile
```

-	Layers:
	-	`sha256:a4b6027eed506a371ad9a2314b6be299e5c509b4c4be66e5842b29837171b0cf`  
		Last Modified: Tue, 13 Jan 2026 04:36:00 GMT  
		Size: 2.0 MB (2011891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc718b3aa0399c50248bba6165cad8666196a5351b6ed095a8101d2f8a5d37da`  
		Last Modified: Tue, 13 Jan 2026 04:36:01 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; riscv64

```console
$ docker pull memcached@sha256:bce857473a0aeeec89bc5383841d05d99df2b89bba49caf3059874a9442ff224
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30613806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc8f84b5bfd0d6518442de566ffa39b2113651446c246e419f61a8e5fa68e87`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Wed, 14 Jan 2026 06:36:03 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 14 Jan 2026 06:36:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jan 2026 06:49:42 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 14 Jan 2026 06:49:42 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 14 Jan 2026 06:49:42 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 14 Jan 2026 06:49:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 14 Jan 2026 06:49:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 06:49:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 14 Jan 2026 06:49:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 06:49:43 GMT
USER memcache
# Wed, 14 Jan 2026 06:49:43 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 14 Jan 2026 06:49:43 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7c6f79d4d52450222a8a38f8fc98e229a4711a246fc94fdaaab31930d3135d`  
		Last Modified: Wed, 14 Jan 2026 06:50:36 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168d1b37fe07dfb8bef5240057ad6597058647499a9e771eedd2091f2d6b30f0`  
		Last Modified: Wed, 14 Jan 2026 06:50:36 GMT  
		Size: 133.1 KB (133105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a5ebc1ef49cab24f75e0c751a1e0563ee042c246c509279fa38cf3cbf0a3f1`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 2.2 MB (2207499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbc8df7ca1d2f273c3c8fec55b30f17ebc72a45687976efd9c8779a66369d46`  
		Last Modified: Wed, 14 Jan 2026 06:50:36 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4057c9476d421ae1ecae3607afb0db57dbc6eb2bc0aa5e41daed169a70319c1`  
		Last Modified: Wed, 14 Jan 2026 06:50:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:75823016a946bfe52b08e1f80032a64b0202a08f2e30dd8cb7035a01e1244518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b86887925c9eccb39ad75807a81768a06591c668cfd4bf4af00a40b2414f22bc`

```dockerfile
```

-	Layers:
	-	`sha256:0d93e934848935cdae8d83be9ebaff197aaa6e70f5b224c2107461561ea0064d`  
		Last Modified: Wed, 14 Jan 2026 07:34:47 GMT  
		Size: 2.0 MB (2002254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0de5bd0cbff9df1fc11e05bd38936b6915195663b273b5c23840bf5eb9373a8`  
		Last Modified: Wed, 14 Jan 2026 07:34:48 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; s390x

```console
$ docker pull memcached@sha256:46c34c0b238fbae2980413fe2b6590839b6afbc43e0a1e07eb456fc274eaf811
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32272852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8666231b78b1bdfb283fe302437321dedf8ecc2d869ff2acdce9f8461f285519`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 14:13:49 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 13 Jan 2026 14:13:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 14:16:57 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 13 Jan 2026 14:16:57 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 13 Jan 2026 14:16:57 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 13 Jan 2026 14:16:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 13 Jan 2026 14:16:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 14:16:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 14:16:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 14:16:57 GMT
USER memcache
# Tue, 13 Jan 2026 14:16:57 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 13 Jan 2026 14:16:57 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2b46bc94baaae0a37e5e04b1babf7e1f37c4390b83d49c3c6820188deba770e3`  
		Last Modified: Tue, 13 Jan 2026 13:10:43 GMT  
		Size: 29.8 MB (29833411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2727771ad16d920baecb7c96b9b54e67178369b881fc20901d381dfd5f873e27`  
		Last Modified: Tue, 13 Jan 2026 14:17:12 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6b0ec5581f8591522a6327cdcfa4e1197d9ada9fb60840f57b5d3e4dd3304d1`  
		Last Modified: Tue, 13 Jan 2026 14:17:12 GMT  
		Size: 140.6 KB (140562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382a3e1ebed70673a0789fcc2104ab941fe04b9a020339f9286ac85b67ae5ff9`  
		Last Modified: Tue, 13 Jan 2026 14:17:13 GMT  
		Size: 2.3 MB (2297368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85fe5f9afd355e3dd76ce942e1c295e356d96ae3b0e3f8236a0e33c5f75ffe71`  
		Last Modified: Tue, 13 Jan 2026 14:17:08 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4546f3c3457928dc273f98dae7c7ac2f945b203138e964ee72fc92aabcef434`  
		Last Modified: Tue, 13 Jan 2026 14:17:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:d620668087c443f58d215a372a70eb0697c7031777d3537d244fa26e62d3ec3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e48c5956bcfcf63509c135da7076a0f247bc2858c7df68331b5a112e937ff6c`

```dockerfile
```

-	Layers:
	-	`sha256:507d45d8f4547a846c07788edb1628f89b93ac7616169374be23f29601b7be68`  
		Last Modified: Tue, 13 Jan 2026 14:17:08 GMT  
		Size: 2.0 MB (2009727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78fdd8684e48fc4ee1817e00df577a38250864ffbcf34ec341937d525d9dfabd`  
		Last Modified: Tue, 13 Jan 2026 16:34:40 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:trixie`

```console
$ docker pull memcached@sha256:e4e5eca37e4334f9579f10fcdd88a58c4eb9d0a8eacedde6ec49d4ea4391637a
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
$ docker pull memcached@sha256:1613c35e314db0c64d8b5679786ad99ced10069c3f9778d40b6c522ff3c04218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32190619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a38251b773d15614da3036dd0d756bbf4a7d16d27fe1c52023517a419372b245`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:22:30 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 13 Jan 2026 01:22:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:25:18 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 13 Jan 2026 01:25:18 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 13 Jan 2026 01:25:18 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 13 Jan 2026 01:25:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 13 Jan 2026 01:25:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:25:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 01:25:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:25:18 GMT
USER memcache
# Tue, 13 Jan 2026 01:25:18 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 13 Jan 2026 01:25:18 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:34 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b6e737e1a3eed198cc17e2b92231ab084bcf55ba90a36136e7a2f4fd04a95b`  
		Last Modified: Tue, 13 Jan 2026 01:25:30 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16835fec399670b74d32630a7368a65ca2a3c32d8b7a690d33bebc7b9e9458d`  
		Last Modified: Tue, 13 Jan 2026 01:25:30 GMT  
		Size: 136.7 KB (136737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c848acbad27f1c9d2fd95e0facabbb28d5d8be19e5fa5912e5474c1301522523`  
		Last Modified: Tue, 13 Jan 2026 01:25:25 GMT  
		Size: 2.3 MB (2278686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9529916038b7840d3177e93bf04b78390bb91bca78623bd9c0769f9e2a965079`  
		Last Modified: Tue, 13 Jan 2026 01:25:25 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24239fc168f5eb73ae9964e2cdcb3c3b878ae79835c6b94585cb648fd50479d`  
		Last Modified: Tue, 13 Jan 2026 01:25:26 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:0d72ad7b507d17cffe5dbec1ddecf1c254c3a85d2b605fa0ddbc9913ba4fc678
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe582f0cad77d385a3debb0f2acf0c96b7b85c6a7d2c95fcc54f938d63635c9`

```dockerfile
```

-	Layers:
	-	`sha256:7d598d8c3b4cd06481693da06e86554144167d205cc60f43382fafba94dd4592`  
		Last Modified: Tue, 13 Jan 2026 04:35:37 GMT  
		Size: 2.0 MB (2008290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dd2469227ab0e75822eb9d56a5d7c05f52a445840f65934e010a2562e509718`  
		Last Modified: Tue, 13 Jan 2026 01:25:24 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; arm variant v5

```console
$ docker pull memcached@sha256:efa6728c05b024b605597e5025f04155aab614b52f56b1b31a4c70a23f909e07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30298859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14119dc07998a4322ac912beaaf4e6ad16e5487f2243c332fdaad86bdce6f55e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:19:21 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 13 Jan 2026 01:19:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:22:43 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 13 Jan 2026 01:22:43 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 13 Jan 2026 01:22:43 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 13 Jan 2026 01:22:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 13 Jan 2026 01:22:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:22:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 01:22:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:22:43 GMT
USER memcache
# Tue, 13 Jan 2026 01:22:43 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 13 Jan 2026 01:22:43 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c113d410d30c2c035a105b56d3937958c81fbe2530f44add3bae903be6864324`  
		Last Modified: Tue, 13 Jan 2026 00:42:30 GMT  
		Size: 27.9 MB (27942724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96776850dc1206c3fd163b84cea19599306159eb0d020b4241d0172240f88d13`  
		Last Modified: Tue, 13 Jan 2026 01:22:55 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3697c7c790d9c4caaa904abdaf809dcdee3f0b518fc5ad82d2e21dd7fe24f64d`  
		Last Modified: Tue, 13 Jan 2026 01:22:55 GMT  
		Size: 144.2 KB (144212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a247339c7ec57a491c3ffe43531dbfaa132f3ff16a481fc41cbb9e3e3ad6476`  
		Last Modified: Tue, 13 Jan 2026 01:22:50 GMT  
		Size: 2.2 MB (2210412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2dcebe3ab2a9945cdea142301e4a64eebbc59c948a54385dbfca4afd561b508`  
		Last Modified: Tue, 13 Jan 2026 01:22:55 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb8ef5ecbc44efd5280f9cf15687dfd80a34fa2966ad039238647177f75dc6c`  
		Last Modified: Tue, 13 Jan 2026 01:22:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:190bb1ecd7376720e541621921c2d4931a9d0f85a047255ba2b56afa3a504212
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9736e9545a46e4ef65dcb5238691292d27fac4dccb330354ce59ac93ae6994b5`

```dockerfile
```

-	Layers:
	-	`sha256:4f5461bf596f750b56b3f10e315936c2326b2c32901d28cdf22db97072bba685`  
		Last Modified: Tue, 13 Jan 2026 01:22:50 GMT  
		Size: 2.0 MB (2011293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8657d28d0436d39193457fb90119ea6e4ddb566df2a83fd1aa9df75651731188`  
		Last Modified: Tue, 13 Jan 2026 04:35:43 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; arm variant v7

```console
$ docker pull memcached@sha256:9c322c838b4648fa30e742e53ed6647a31383760fb73fa82de32b4b6dc88c494
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28509532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6e130248535c57fccff4d89a9d442e31cabd471e41c9eed52e5207a54f9f944`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:25:47 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 13 Jan 2026 01:25:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:28:55 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 13 Jan 2026 01:28:55 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 13 Jan 2026 01:28:55 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 13 Jan 2026 01:28:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 13 Jan 2026 01:28:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:28:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 01:28:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:28:55 GMT
USER memcache
# Tue, 13 Jan 2026 01:28:55 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 13 Jan 2026 01:28:55 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029a2cbe46c1e12ab6d47a63f40fb29056b6c6277c7822085ed0fe62e0a1791d`  
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c7827f95482598f1bd32dd8cbe071ad009795fa108661234eeb872d1a1e8bd`  
		Last Modified: Tue, 13 Jan 2026 01:29:07 GMT  
		Size: 135.4 KB (135398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9371e974781bd91adc657086f00cd7d91b5530ca9da37597c347dd7d4eaff0`  
		Last Modified: Tue, 13 Jan 2026 01:29:07 GMT  
		Size: 2.2 MB (2164040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c2e0f64c0afa16b5e214ae208c8c81e8c78c79ddd90f54983a93c7297395f6b`  
		Last Modified: Tue, 13 Jan 2026 01:29:07 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92151d443057f88ed7f60405440b698ff9e6abe1a2ca1c91a0c7e7626339ad2`  
		Last Modified: Tue, 13 Jan 2026 01:29:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:12cc31a1ce56d2c6dd1c0dcfd4ef1fe74484985d010594950c086c0f4431559b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b2d844d5393973080c37fde0b92cd48bd1a64e03973290631be5486d814de7e`

```dockerfile
```

-	Layers:
	-	`sha256:99fc27444c1ccdd6cbd08a33aac22e9e85f55958bda7b6216bdea08eae374cff`  
		Last Modified: Tue, 13 Jan 2026 04:35:47 GMT  
		Size: 2.0 MB (2009750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e76d5584f581b7668c61a661da2858bc1d5e11b31e3629e0d2b3af52d9c22ed8`  
		Last Modified: Tue, 13 Jan 2026 04:35:47 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:2ed537fa0376a3eb0864d6a3b51ea7da59b9ff4bb3270189a8a5082f02f811e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32550406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf26d75d787aabbd202c97db1079b96e45105d3ca509a1001ab973cb473cae8c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:22:29 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 13 Jan 2026 01:22:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:25:26 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 13 Jan 2026 01:25:26 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 13 Jan 2026 01:25:26 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 13 Jan 2026 01:25:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 13 Jan 2026 01:25:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:25:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 01:25:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:25:27 GMT
USER memcache
# Tue, 13 Jan 2026 01:25:27 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 13 Jan 2026 01:25:27 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78edb6b991369235f90958a936afc89dc37b82439c632988ed143b5bd76deadb`  
		Last Modified: Tue, 13 Jan 2026 01:25:40 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e1afbb765f6cc3923e864d44fb6cd6c9167b884e596b09bd37c7c276f65a2b`  
		Last Modified: Tue, 13 Jan 2026 01:25:40 GMT  
		Size: 153.5 KB (153512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff9edc68fe57c233001afd442eb6c248bf070d32fbb412a8bfeef6f9a6217f5`  
		Last Modified: Tue, 13 Jan 2026 01:25:40 GMT  
		Size: 2.3 MB (2261341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c4648fbc4a4189184946895d1041e0eee2c5d40fd70638a553bedb0cbf5cf8`  
		Last Modified: Tue, 13 Jan 2026 01:25:40 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26bd1b32b048e73091ddf6e6762e368d4bb6ef2cc7d3aa43467749b36fe08e38`  
		Last Modified: Tue, 13 Jan 2026 01:25:40 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:72333c6222fb20b5a9f9f92b8d56c47ebb5b4e6cd65512a6b5172ad0c0cade67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a2a4e23cbe2d062f3fcfb84c8590190eb72294786a0b8238add858e67a93914`

```dockerfile
```

-	Layers:
	-	`sha256:1f8545bcc66309a59381c88c4c87b0f8352893dbaa167be48947976c1e0cef1d`  
		Last Modified: Tue, 13 Jan 2026 04:35:51 GMT  
		Size: 2.0 MB (2008606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95e6875e372e1d6a9660c08726cb96d08b272e52a2446f275089efccfc3096b3`  
		Last Modified: Tue, 13 Jan 2026 01:25:33 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; 386

```console
$ docker pull memcached@sha256:29540e588e9065db9ecc8865fe74544260980d73786f00dfc4df3f3cee148bd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33661194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66843ae7a7d968c4f056a8e350dd84ff80a06e48b48c298c3427333b7ec259ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:19:43 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 13 Jan 2026 01:19:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:22:40 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 13 Jan 2026 01:22:40 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 13 Jan 2026 01:22:40 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 13 Jan 2026 01:22:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 13 Jan 2026 01:22:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:22:40 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 01:22:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:22:40 GMT
USER memcache
# Tue, 13 Jan 2026 01:22:40 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 13 Jan 2026 01:22:40 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:27bb6d39eda5ced7626db280c3902aacdfade5acd11a16ef9618e3185f69b102`  
		Last Modified: Tue, 13 Jan 2026 00:43:03 GMT  
		Size: 31.3 MB (31288476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cedb4f2840edea9de46e0d955a0512f469211880560a8948f10b54381bcd728`  
		Last Modified: Tue, 13 Jan 2026 01:22:53 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c4b2d1574ee5f238dc6948164abd39ffcc91929b2c464c6b3874dec01fd964`  
		Last Modified: Tue, 13 Jan 2026 01:22:46 GMT  
		Size: 147.6 KB (147554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc1bf5870b84175607f3d012b3cfebc5859869f8125114ea5d6ed1a05f81d2d`  
		Last Modified: Tue, 13 Jan 2026 01:22:53 GMT  
		Size: 2.2 MB (2223652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6434e73ed67e81f1016f27c7cc175290b0ce959d8a1bf5e9b0f3119f161246`  
		Last Modified: Tue, 13 Jan 2026 01:22:53 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abaf99fdf0e2b9620d20088b389b3f18eb67ad356c8c6c7961074e1428b8af0c`  
		Last Modified: Tue, 13 Jan 2026 01:22:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:f64192985f4635b04ce1ab99b3cae89f71d0b11f9670fb6d9c470158e3c5c63e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bb9ce834f23725c4bfc4fb2d6a24a96d3d0bc7685d3a759c0085871f34231e8`

```dockerfile
```

-	Layers:
	-	`sha256:ed9937c762728e5abc93b88bd7932a5762d2bc8e0001e81bb25ef0b27e2bc6ff`  
		Last Modified: Tue, 13 Jan 2026 04:35:56 GMT  
		Size: 2.0 MB (2005447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6358862e12c5c5367efd52bea0b1194e04e76f267084da591229f64ee7482dc3`  
		Last Modified: Tue, 13 Jan 2026 04:35:57 GMT  
		Size: 22.1 KB (22094 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; ppc64le

```console
$ docker pull memcached@sha256:309e0faad388272d7e37d6ee0cb354707d099e3140298105499711823d7a0eea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36161489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6f50ee10fc83da67b90c9bda7499251fa073fea87400d5fb70e31e693d6f902`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:33:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 13 Jan 2026 01:33:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:36:52 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 13 Jan 2026 01:36:52 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 13 Jan 2026 01:36:52 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 13 Jan 2026 01:36:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 13 Jan 2026 01:36:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:36:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 01:36:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:36:53 GMT
USER memcache
# Tue, 13 Jan 2026 01:36:53 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 13 Jan 2026 01:36:53 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9a275bb13cf8b3e9db52a41b6b4ff22ee1ffed00394f6deddd2de45044bd3bae`  
		Last Modified: Tue, 13 Jan 2026 00:57:13 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093e59deb53ff01a892be2a5df928c4b04a289df7f6c135570c11d6a4fdbc53a`  
		Last Modified: Tue, 13 Jan 2026 01:37:16 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4da25c8b13ee47050a38843c1954d2bd7bbdba2666f725aee2f603e03fcb6d`  
		Last Modified: Tue, 13 Jan 2026 01:37:16 GMT  
		Size: 170.4 KB (170427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cab5f6f805c735c0f324c87ff8c66cfab0e35fb691b7761e85bb9a2bbb31cfe`  
		Last Modified: Tue, 13 Jan 2026 01:37:16 GMT  
		Size: 2.4 MB (2393947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3a7dfc8da65bd6101de156530bc2688c5588c718bbc3131ff4594cbefd0e66`  
		Last Modified: Tue, 13 Jan 2026 01:37:09 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06153b2e2bde9b06f1c2719aabb5ff6a6c23056152a024fa2c990d97b4d9c799`  
		Last Modified: Tue, 13 Jan 2026 01:37:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:8dfcc685b38edcaec140b90716d19e543715184f20f7a401d6f734ad8f8cf1dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7442b6e23a86bfe5ee9a534d43f0a55ba9629d3c24128b1b3e2b5121644dcf00`

```dockerfile
```

-	Layers:
	-	`sha256:a4b6027eed506a371ad9a2314b6be299e5c509b4c4be66e5842b29837171b0cf`  
		Last Modified: Tue, 13 Jan 2026 04:36:00 GMT  
		Size: 2.0 MB (2011891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc718b3aa0399c50248bba6165cad8666196a5351b6ed095a8101d2f8a5d37da`  
		Last Modified: Tue, 13 Jan 2026 04:36:01 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; riscv64

```console
$ docker pull memcached@sha256:bce857473a0aeeec89bc5383841d05d99df2b89bba49caf3059874a9442ff224
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30613806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc8f84b5bfd0d6518442de566ffa39b2113651446c246e419f61a8e5fa68e87`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Wed, 14 Jan 2026 06:36:03 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 14 Jan 2026 06:36:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jan 2026 06:49:42 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 14 Jan 2026 06:49:42 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 14 Jan 2026 06:49:42 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 14 Jan 2026 06:49:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 14 Jan 2026 06:49:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 06:49:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 14 Jan 2026 06:49:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 06:49:43 GMT
USER memcache
# Wed, 14 Jan 2026 06:49:43 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 14 Jan 2026 06:49:43 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7c6f79d4d52450222a8a38f8fc98e229a4711a246fc94fdaaab31930d3135d`  
		Last Modified: Wed, 14 Jan 2026 06:50:36 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168d1b37fe07dfb8bef5240057ad6597058647499a9e771eedd2091f2d6b30f0`  
		Last Modified: Wed, 14 Jan 2026 06:50:36 GMT  
		Size: 133.1 KB (133105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a5ebc1ef49cab24f75e0c751a1e0563ee042c246c509279fa38cf3cbf0a3f1`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 2.2 MB (2207499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbc8df7ca1d2f273c3c8fec55b30f17ebc72a45687976efd9c8779a66369d46`  
		Last Modified: Wed, 14 Jan 2026 06:50:36 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4057c9476d421ae1ecae3607afb0db57dbc6eb2bc0aa5e41daed169a70319c1`  
		Last Modified: Wed, 14 Jan 2026 06:50:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:75823016a946bfe52b08e1f80032a64b0202a08f2e30dd8cb7035a01e1244518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b86887925c9eccb39ad75807a81768a06591c668cfd4bf4af00a40b2414f22bc`

```dockerfile
```

-	Layers:
	-	`sha256:0d93e934848935cdae8d83be9ebaff197aaa6e70f5b224c2107461561ea0064d`  
		Last Modified: Wed, 14 Jan 2026 07:34:47 GMT  
		Size: 2.0 MB (2002254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0de5bd0cbff9df1fc11e05bd38936b6915195663b273b5c23840bf5eb9373a8`  
		Last Modified: Wed, 14 Jan 2026 07:34:48 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; s390x

```console
$ docker pull memcached@sha256:46c34c0b238fbae2980413fe2b6590839b6afbc43e0a1e07eb456fc274eaf811
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32272852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8666231b78b1bdfb283fe302437321dedf8ecc2d869ff2acdce9f8461f285519`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 14:13:49 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 13 Jan 2026 14:13:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 14:16:57 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 13 Jan 2026 14:16:57 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 13 Jan 2026 14:16:57 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 13 Jan 2026 14:16:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 13 Jan 2026 14:16:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 14:16:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 13 Jan 2026 14:16:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 14:16:57 GMT
USER memcache
# Tue, 13 Jan 2026 14:16:57 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 13 Jan 2026 14:16:57 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2b46bc94baaae0a37e5e04b1babf7e1f37c4390b83d49c3c6820188deba770e3`  
		Last Modified: Tue, 13 Jan 2026 13:10:43 GMT  
		Size: 29.8 MB (29833411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2727771ad16d920baecb7c96b9b54e67178369b881fc20901d381dfd5f873e27`  
		Last Modified: Tue, 13 Jan 2026 14:17:12 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6b0ec5581f8591522a6327cdcfa4e1197d9ada9fb60840f57b5d3e4dd3304d1`  
		Last Modified: Tue, 13 Jan 2026 14:17:12 GMT  
		Size: 140.6 KB (140562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382a3e1ebed70673a0789fcc2104ab941fe04b9a020339f9286ac85b67ae5ff9`  
		Last Modified: Tue, 13 Jan 2026 14:17:13 GMT  
		Size: 2.3 MB (2297368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85fe5f9afd355e3dd76ce942e1c295e356d96ae3b0e3f8236a0e33c5f75ffe71`  
		Last Modified: Tue, 13 Jan 2026 14:17:08 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4546f3c3457928dc273f98dae7c7ac2f945b203138e964ee72fc92aabcef434`  
		Last Modified: Tue, 13 Jan 2026 14:17:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:d620668087c443f58d215a372a70eb0697c7031777d3537d244fa26e62d3ec3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e48c5956bcfcf63509c135da7076a0f247bc2858c7df68331b5a112e937ff6c`

```dockerfile
```

-	Layers:
	-	`sha256:507d45d8f4547a846c07788edb1628f89b93ac7616169374be23f29601b7be68`  
		Last Modified: Tue, 13 Jan 2026 14:17:08 GMT  
		Size: 2.0 MB (2009727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78fdd8684e48fc4ee1817e00df577a38250864ffbcf34ec341937d525d9dfabd`  
		Last Modified: Tue, 13 Jan 2026 16:34:40 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json
