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
		Last Modified: Tue, 13 Jan 2026 00:42:27 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b6e737e1a3eed198cc17e2b92231ab084bcf55ba90a36136e7a2f4fd04a95b`  
		Last Modified: Tue, 13 Jan 2026 01:25:25 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16835fec399670b74d32630a7368a65ca2a3c32d8b7a690d33bebc7b9e9458d`  
		Last Modified: Tue, 13 Jan 2026 01:25:24 GMT  
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
		Last Modified: Tue, 13 Jan 2026 01:25:25 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 27.9 MB (27942724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96776850dc1206c3fd163b84cea19599306159eb0d020b4241d0172240f88d13`  
		Last Modified: Tue, 13 Jan 2026 01:22:50 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3697c7c790d9c4caaa904abdaf809dcdee3f0b518fc5ad82d2e21dd7fe24f64d`  
		Last Modified: Tue, 13 Jan 2026 01:22:50 GMT  
		Size: 144.2 KB (144212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a247339c7ec57a491c3ffe43531dbfaa132f3ff16a481fc41cbb9e3e3ad6476`  
		Last Modified: Tue, 13 Jan 2026 01:22:50 GMT  
		Size: 2.2 MB (2210412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2dcebe3ab2a9945cdea142301e4a64eebbc59c948a54385dbfca4afd561b508`  
		Last Modified: Tue, 13 Jan 2026 01:22:50 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb8ef5ecbc44efd5280f9cf15687dfd80a34fa2966ad039238647177f75dc6c`  
		Last Modified: Tue, 13 Jan 2026 01:22:51 GMT  
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
		Last Modified: Tue, 13 Jan 2026 01:22:50 GMT  
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
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
		Size: 135.4 KB (135398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9371e974781bd91adc657086f00cd7d91b5530ca9da37597c347dd7d4eaff0`  
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
		Size: 2.2 MB (2164040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c2e0f64c0afa16b5e214ae208c8c81e8c78c79ddd90f54983a93c7297395f6b`  
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
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
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
		Size: 2.0 MB (2009750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e76d5584f581b7668c61a661da2858bc1d5e11b31e3629e0d2b3af52d9c22ed8`  
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:41 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78edb6b991369235f90958a936afc89dc37b82439c632988ed143b5bd76deadb`  
		Last Modified: Tue, 13 Jan 2026 01:25:33 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e1afbb765f6cc3923e864d44fb6cd6c9167b884e596b09bd37c7c276f65a2b`  
		Last Modified: Tue, 13 Jan 2026 01:25:33 GMT  
		Size: 153.5 KB (153512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff9edc68fe57c233001afd442eb6c248bf070d32fbb412a8bfeef6f9a6217f5`  
		Last Modified: Tue, 13 Jan 2026 01:25:33 GMT  
		Size: 2.3 MB (2261341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c4648fbc4a4189184946895d1041e0eee2c5d40fd70638a553bedb0cbf5cf8`  
		Last Modified: Tue, 13 Jan 2026 01:25:33 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26bd1b32b048e73091ddf6e6762e368d4bb6ef2cc7d3aa43467749b36fe08e38`  
		Last Modified: Tue, 13 Jan 2026 01:25:34 GMT  
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
		Last Modified: Tue, 13 Jan 2026 01:25:33 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:56 GMT  
		Size: 31.3 MB (31288476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cedb4f2840edea9de46e0d955a0512f469211880560a8948f10b54381bcd728`  
		Last Modified: Tue, 13 Jan 2026 01:22:46 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c4b2d1574ee5f238dc6948164abd39ffcc91929b2c464c6b3874dec01fd964`  
		Last Modified: Tue, 13 Jan 2026 01:22:46 GMT  
		Size: 147.6 KB (147554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc1bf5870b84175607f3d012b3cfebc5859869f8125114ea5d6ed1a05f81d2d`  
		Last Modified: Tue, 13 Jan 2026 01:22:46 GMT  
		Size: 2.2 MB (2223652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6434e73ed67e81f1016f27c7cc175290b0ce959d8a1bf5e9b0f3119f161246`  
		Last Modified: Tue, 13 Jan 2026 01:22:46 GMT  
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
		Last Modified: Tue, 13 Jan 2026 01:22:46 GMT  
		Size: 2.0 MB (2005447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6358862e12c5c5367efd52bea0b1194e04e76f267084da591229f64ee7482dc3`  
		Last Modified: Tue, 13 Jan 2026 01:22:46 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:57:06 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093e59deb53ff01a892be2a5df928c4b04a289df7f6c135570c11d6a4fdbc53a`  
		Last Modified: Tue, 13 Jan 2026 01:37:09 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4da25c8b13ee47050a38843c1954d2bd7bbdba2666f725aee2f603e03fcb6d`  
		Last Modified: Tue, 13 Jan 2026 01:37:09 GMT  
		Size: 170.4 KB (170427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cab5f6f805c735c0f324c87ff8c66cfab0e35fb691b7761e85bb9a2bbb31cfe`  
		Last Modified: Tue, 13 Jan 2026 01:37:09 GMT  
		Size: 2.4 MB (2393947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3a7dfc8da65bd6101de156530bc2688c5588c718bbc3131ff4594cbefd0e66`  
		Last Modified: Tue, 13 Jan 2026 01:37:09 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06153b2e2bde9b06f1c2719aabb5ff6a6c23056152a024fa2c990d97b4d9c799`  
		Last Modified: Tue, 13 Jan 2026 01:37:10 GMT  
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
		Last Modified: Tue, 13 Jan 2026 01:37:09 GMT  
		Size: 2.0 MB (2011891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc718b3aa0399c50248bba6165cad8666196a5351b6ed095a8101d2f8a5d37da`  
		Last Modified: Tue, 13 Jan 2026 01:37:09 GMT  
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
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168d1b37fe07dfb8bef5240057ad6597058647499a9e771eedd2091f2d6b30f0`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 133.1 KB (133105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a5ebc1ef49cab24f75e0c751a1e0563ee042c246c509279fa38cf3cbf0a3f1`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 2.2 MB (2207499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbc8df7ca1d2f273c3c8fec55b30f17ebc72a45687976efd9c8779a66369d46`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4057c9476d421ae1ecae3607afb0db57dbc6eb2bc0aa5e41daed169a70319c1`  
		Last Modified: Wed, 14 Jan 2026 06:50:29 GMT  
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
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 2.0 MB (2002254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0de5bd0cbff9df1fc11e05bd38936b6915195663b273b5c23840bf5eb9373a8`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
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
		Last Modified: Tue, 13 Jan 2026 13:10:27 GMT  
		Size: 29.8 MB (29833411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2727771ad16d920baecb7c96b9b54e67178369b881fc20901d381dfd5f873e27`  
		Last Modified: Tue, 13 Jan 2026 14:17:08 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6b0ec5581f8591522a6327cdcfa4e1197d9ada9fb60840f57b5d3e4dd3304d1`  
		Last Modified: Tue, 13 Jan 2026 14:17:08 GMT  
		Size: 140.6 KB (140562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382a3e1ebed70673a0789fcc2104ab941fe04b9a020339f9286ac85b67ae5ff9`  
		Last Modified: Tue, 13 Jan 2026 14:17:08 GMT  
		Size: 2.3 MB (2297368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85fe5f9afd355e3dd76ce942e1c295e356d96ae3b0e3f8236a0e33c5f75ffe71`  
		Last Modified: Tue, 13 Jan 2026 14:17:08 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4546f3c3457928dc273f98dae7c7ac2f945b203138e964ee72fc92aabcef434`  
		Last Modified: Tue, 13 Jan 2026 14:17:09 GMT  
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
		Last Modified: Tue, 13 Jan 2026 14:17:08 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine`

```console
$ docker pull memcached@sha256:8a82a3927694e42bc52679dc81532244de51e5faed5f9541a1283e3ad7271db1
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
$ docker pull memcached@sha256:947366d40559340a4385b3e05f92186b9546e7feb59ef280e243ec8bf34f01a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5958530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7977390ffe9a7f3b6d3c5840f262b8058ca015d7daf5237e480d3f51a29e0b6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:18:28 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:18:29 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:21:03 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:21:03 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:21:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:21:03 GMT
USER memcache
# Wed, 28 Jan 2026 02:21:03 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:21:03 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e0ee508166c94a4f9ca8c32f743bd3733afb7660800042c7da03c2ea1da6b4`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15bf9562ecbc21cc4f52d1a4d33eb5eec98aa63c36c59f018b55071b8dd9f05f`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 106.1 KB (106059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24c6974a0da2f6cdd2022450be6195683245ba21f601d207ad14566c653ddea`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 2.0 MB (1989295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a859de0eb0253d066d7de73c90f4ebdc8b737fddab90420fd0ba6bd1c74669`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7be89a9ef60cc91d2346c9bc9a975138908bbc03aa40c948ab5e7336aa8e8b`  
		Last Modified: Wed, 28 Jan 2026 02:21:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7579a20056cd9531e754a57f957da811356775f676bfa6cd6e86b95f6de172d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8408948e08375e96299e735072f97a85aca5d58f65fc7cca125dfe5389160cb`

```dockerfile
```

-	Layers:
	-	`sha256:533c466de2027803aea398674e5a5ffd7d67b9e1eddc4228741a130ff830b02a`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 94.9 KB (94873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27c54b10e342535e2af7655af306fbf617d3dbf0922a7dd440f8ed4ea3e1fd5c`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:3a1e785feba037614143f75204bac3225d838127c68805b29ff23df9d8638070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c891a4120404380161eeeddd4e7c7cb748eb55193453c6e9090a59909bf1969`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 06:07:09 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 06:07:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 06:19:29 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 06:19:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 06:19:29 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 06:19:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 06:19:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 06:19:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 06:19:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 06:19:29 GMT
USER memcache
# Wed, 28 Jan 2026 06:19:29 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 06:19:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9dfe3bd7930f213b1f0f6c2854f26637f5a52c7cd4796e9eb59071fe2ff4b2f`  
		Last Modified: Wed, 28 Jan 2026 06:19:33 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:707447698613ddcfad121290546b5d9e04e2c3194b8f59394a272fe30f42dba1`  
		Last Modified: Wed, 28 Jan 2026 06:19:33 GMT  
		Size: 102.6 KB (102646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d366a66d67c4233b2ac1bc38363cb9881e63ca3af7f82ebbffbfb76942e1a34`  
		Last Modified: Wed, 28 Jan 2026 06:19:34 GMT  
		Size: 1.9 MB (1939230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e5326e5c6353c918ea1ac99aedfb19f688830f93037e66268b39c31f670e01`  
		Last Modified: Wed, 28 Jan 2026 06:19:33 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2ead2e4800bd6e32bbdb6225ecb70b554d33b3c17f3e8b973890f3b3c532da`  
		Last Modified: Wed, 28 Jan 2026 06:19:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:fd7fcbdf0e7f96a083f3d6aec29c9d21ac4b768be5949f68958c25756c153f95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07888c8ad7065e17bfea11af8f4f20b5f956ab1b553160f5ea4a484c4e437674`

```dockerfile
```

-	Layers:
	-	`sha256:aed006a02d773c56c072711ddc729af9ce5001ab757071fc3abdc5094822e7c7`  
		Last Modified: Wed, 28 Jan 2026 06:19:34 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:f08c7e3ff92e718b22bc7b21385421ebcf4bf6f542b797690d6547506821ab35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5272638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a6fc0ce35a3d59414018d4d8fe69929016a9e8dc7dc27daaafc617e3a7165d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:22:45 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:22:46 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:25:41 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:25:41 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:25:41 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:25:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:25:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:25:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:25:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:25:41 GMT
USER memcache
# Wed, 28 Jan 2026 02:25:41 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:25:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f61af882efa215dd577f7a17129442647756c535df9c13e821da864cddcf0e6`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b88f23b7692bcb2301e4e0a862af10c70c6ec663fca9e0a3389a74a3ba0520e`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 92.4 KB (92374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0549b4be8a16d49c33d6adaf28e4f8f7acbdea009dec2daed172741f7540ce5a`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 1.9 MB (1897188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6760f49ea55e45e14e26aaaf690948c109a5d85256175c84bbd06beccc8cd1`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9fca934ad2088c9a34e9f20e65d902054dfb9accdb4c6865924dd1fa88685b`  
		Last Modified: Wed, 28 Jan 2026 02:25:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:b5c2e8ac0b1fd0bd9c534bf163bad10efc0dc2c3afdfb66e3eb1a827d7bbfc87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dd20e2507c3ff3732182e3d2d44e5f7bc9b449bb172d5c7895b2fcc2dd423c6`

```dockerfile
```

-	Layers:
	-	`sha256:36627c0161ebd5c055e99a596a600017e5608e5895d1f95159116ff2df2eb3a6`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 94.3 KB (94291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a5914862f1fb65973ac0def541c9da056e1a5ef0bb26623a5bbad81803a4383`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:1a4aa193f53b5a4e2d82f6c67c23e87ef5d3d1cd1ddf96e0aabe73d49e537c2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6286893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f275b1c508af04216ccc891e9de0d7cbb35441f4eb424197e529ddbfb1d1b62`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:18:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:18:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:20:58 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:20:58 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:20:58 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:20:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:20:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:20:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:20:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:20:59 GMT
USER memcache
# Wed, 28 Jan 2026 02:20:59 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:20:59 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42047232a88cba1fc4d173d71bdf04395f6e4b83472de9f225ae2dd70ce14bc`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b625b9113e283efad9a0ee8e305f08edfd38a6c015224459a1ec0f2f49a0b915`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 121.8 KB (121845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf057b1d31677325905e009d68a97c3741028480d8b254105b145f39d157f2a`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 2.0 MB (1966604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db407fe2bd85342d8cb160bd73b5efe730723df2d20f2f6021eef8ad2d8f16eb`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfefb839a309e8b3df7a659236c09776f4eff9f8a47d9b331f131d9ad4c5d6b`  
		Last Modified: Wed, 28 Jan 2026 02:21:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:28b857747dd2742dbf00b9c1fc07265248073390d37bacf6cf8bfd313cf52a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f34aaccc9ca109270d86cdb6e46e56b207775ad700dadb1604f0a56b3ed4536e`

```dockerfile
```

-	Layers:
	-	`sha256:53b8cb56ae6a2b4c94fae4924dc03d881acba2e6c746fdb05808f3a86186ceff`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 94.3 KB (94327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03361fd0b86b6e905c14afa88e91f00f54a7e68e1d12d191b3d65c41986adc2e`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 20.7 KB (20728 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; 386

```console
$ docker pull memcached@sha256:8c10f776d94f57c5e0a4807247add0a2f3638eaafc3f6571b66ac325cc251866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5741838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f2329492e766d962366bfa352f931d82d7cd74d9e771ae6db7d44c1345197b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:16:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:16:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:18:59 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:18:59 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:18:59 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:18:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:18:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:18:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:18:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:18:59 GMT
USER memcache
# Wed, 28 Jan 2026 02:18:59 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:18:59 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbdb7a800485646296958fbca0c9cfdd5c397a0dbc2e33f1bc0c55dfca3c47a6`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7651295f62c54da7297c4ef646e146ef0acac3f551fb8a3dccc49190efced234`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 110.7 KB (110722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87d7b2cf89ac568b76f6e27208734340c49f4d7b0fedb8e5ae16f54a0cadc43`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 1.9 MB (1942772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4f82eada80af7ef4ec5dfcb36c5a93fa36157801318f374c5ab0d0987cd352`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61a034237824e579d4d24c5ec4b58ee8c400255488e658c36064d43c0001301`  
		Last Modified: Wed, 28 Jan 2026 02:19:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:118dd83c690f154abc02b708a01a0a0a48519b7faa920e5540ebf81c8e626429
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a7e54c817c006a1a17af2f06a4b3e4d1816cb0051c626c3f5e18a5012224b2`

```dockerfile
```

-	Layers:
	-	`sha256:11c94853238efef3a0c48e7cc56222e34874215e568475cfb20d3f2394aad42e`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 94.8 KB (94828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c97d62051151c9b1528a1b64a558c48025170f167ba863808d5fb67d4c59006`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:3a553e0d4ee19ee930775d8f8848969c6ff96b11e6b20f159ad754d11f5a8f8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6033619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfcda9c1811a9129ce53ed17b8ca116ffbaeebc21da0604c23b90e0dd042b0aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:33:21 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:33:22 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:35:40 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:35:40 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:35:40 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:35:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:35:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:35:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:35:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:35:41 GMT
USER memcache
# Wed, 28 Jan 2026 02:35:41 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:35:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c501a178d8bd3c1966eb75a7610efc35f292a3662f9fa7ca0d0089f54f723ce9`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac221803a5094f2d41563eece02e2e93293557ecb1eb5b7b646bcf143abcb82`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 126.3 KB (126255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d71af754023c45f69e3c70d3b4bfad1459328a7922268883ea41f2089ffe32ac`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 2.1 MB (2076366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c5df498426baf66bbc7701a67818ff6903c4420dc16591e79270ea8799caa35`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723a9c7624c2d00490e93ff507b003a4b495513fa6ec61b766c50bf5ccb8e23f`  
		Last Modified: Wed, 28 Jan 2026 02:35:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:238c5819c270bbc55c4140407b62939bf6ca158cb58cdbda8098f069301739a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9f43e248be2e248fe895fc3beccdf145fb06637800c6b89c19bf606d7c22975`

```dockerfile
```

-	Layers:
	-	`sha256:88da11471f4f95fd0f4679af21785a14ccb57b8bbd7fb96e4c42e1c49c333c33`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 94.3 KB (94280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b1fb2f254a022e51ca3dae9140daca46922a20d56b46607f22f1eef757d2fbb`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:8e9681abd0b8d92bb9145c49b7056cd27503f3420c10928ae606e4a65bdb9c9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5769974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:402a203724e613388d65f9de266b282381d864954d277c9552b24343915e9c40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 08:29:56 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 08:29:59 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 08:43:13 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 08:43:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 08:43:13 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 08:43:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 08:43:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 08:43:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 08:43:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 08:43:14 GMT
USER memcache
# Wed, 28 Jan 2026 08:43:14 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 08:43:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914e61f980ba6c54647d03d80091a261aae3ba7ab3d715251e992ea9407ad42e`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d963624519ed571edcf05aed3166ea5b7c1cd5fdae41a0d996d79be268f71e85`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 108.9 KB (108895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab35062ef9866f40cf3445147d50436a982e80d0ed984cca2f11d3ebcde5821`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 2.1 MB (2074437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82838004f4581bf0e6c37cecd3054aeb9fe5e1b92aeeb8cab2e86d9f9ed17af9`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b15a31cacc0f8dc4445667f3d0689a9857004aef390e2a16f7987db8124da4d7`  
		Last Modified: Wed, 28 Jan 2026 08:43:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:f15acc0a96b37da08e228c4fc099dbf28f370723c976c1a8a4d08679f5384799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c47e5bd1d37bec13b189586d46312efcb90ac656c7a80b9fd45fde1dd13f8e6e`

```dockerfile
```

-	Layers:
	-	`sha256:216d743a064cca1bd85c432678c24f3fa640798967115037f27c923138aa7af6`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 94.3 KB (94276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c38c6e624d8af51c7da79f4f214eb73cbfe3c2a2f9b465649a72b8dfa18429f`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:f52690bd1266bfbe887fa9c03fc963f0277f331a85d8e81f4f134076c6d899f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5858103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7903f118ee1fcea4632b09ffbabd30b82ef4aa3b68dd3570b1173f263cacc343`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:21:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:21:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:24:07 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:24:07 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:24:07 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:24:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:24:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:24:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:24:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:24:08 GMT
USER memcache
# Wed, 28 Jan 2026 02:24:08 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:24:08 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030f843902eb7c01da3de08b6efb672d46d4f41e9e298640c66daabea5d901ef`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100608bf5f6494395c46670a28e6df9d705e08dc9129c1fb36b8f265fa52c22b`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 114.3 KB (114299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b706c73349baf76aabbef50d7dba3c89b85ffc84ad0aca5c544b1fe047706785`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 2.0 MB (2017124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce545f5bb33e4374e2e0bb9b11e751c89272699812f06c49e8e6a2e5ac3d524`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ac2e9e98ac3e799be9d54501be2f2304ef93065d34bef18f002ea38838ea24`  
		Last Modified: Wed, 28 Jan 2026 02:24:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:b4850489cf16ad5f72674b698ab0c2d16d95c6cc43e1b3f611f9fa67adcf4962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b79deed0597f9356a7dd99d34cb933d7634c520350fcabb9da14b254006070d0`

```dockerfile
```

-	Layers:
	-	`sha256:00a586e58a4b437f0260b3197ecff606cb3380869c6861c89d769a99132c10e9`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 94.2 KB (94222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8caeef6fbf9d37a3d092d84298ef02b53e2efff54347431fcc362c14dcdb9eb5`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine3.23`

```console
$ docker pull memcached@sha256:8a82a3927694e42bc52679dc81532244de51e5faed5f9541a1283e3ad7271db1
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
$ docker pull memcached@sha256:947366d40559340a4385b3e05f92186b9546e7feb59ef280e243ec8bf34f01a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5958530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7977390ffe9a7f3b6d3c5840f262b8058ca015d7daf5237e480d3f51a29e0b6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:18:28 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:18:29 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:21:03 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:21:03 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:21:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:21:03 GMT
USER memcache
# Wed, 28 Jan 2026 02:21:03 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:21:03 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e0ee508166c94a4f9ca8c32f743bd3733afb7660800042c7da03c2ea1da6b4`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15bf9562ecbc21cc4f52d1a4d33eb5eec98aa63c36c59f018b55071b8dd9f05f`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 106.1 KB (106059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24c6974a0da2f6cdd2022450be6195683245ba21f601d207ad14566c653ddea`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 2.0 MB (1989295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a859de0eb0253d066d7de73c90f4ebdc8b737fddab90420fd0ba6bd1c74669`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7be89a9ef60cc91d2346c9bc9a975138908bbc03aa40c948ab5e7336aa8e8b`  
		Last Modified: Wed, 28 Jan 2026 02:21:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:7579a20056cd9531e754a57f957da811356775f676bfa6cd6e86b95f6de172d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8408948e08375e96299e735072f97a85aca5d58f65fc7cca125dfe5389160cb`

```dockerfile
```

-	Layers:
	-	`sha256:533c466de2027803aea398674e5a5ffd7d67b9e1eddc4228741a130ff830b02a`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 94.9 KB (94873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27c54b10e342535e2af7655af306fbf617d3dbf0922a7dd440f8ed4ea3e1fd5c`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; arm variant v6

```console
$ docker pull memcached@sha256:3a1e785feba037614143f75204bac3225d838127c68805b29ff23df9d8638070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c891a4120404380161eeeddd4e7c7cb748eb55193453c6e9090a59909bf1969`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 06:07:09 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 06:07:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 06:19:29 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 06:19:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 06:19:29 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 06:19:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 06:19:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 06:19:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 06:19:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 06:19:29 GMT
USER memcache
# Wed, 28 Jan 2026 06:19:29 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 06:19:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9dfe3bd7930f213b1f0f6c2854f26637f5a52c7cd4796e9eb59071fe2ff4b2f`  
		Last Modified: Wed, 28 Jan 2026 06:19:33 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:707447698613ddcfad121290546b5d9e04e2c3194b8f59394a272fe30f42dba1`  
		Last Modified: Wed, 28 Jan 2026 06:19:33 GMT  
		Size: 102.6 KB (102646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d366a66d67c4233b2ac1bc38363cb9881e63ca3af7f82ebbffbfb76942e1a34`  
		Last Modified: Wed, 28 Jan 2026 06:19:34 GMT  
		Size: 1.9 MB (1939230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e5326e5c6353c918ea1ac99aedfb19f688830f93037e66268b39c31f670e01`  
		Last Modified: Wed, 28 Jan 2026 06:19:33 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2ead2e4800bd6e32bbdb6225ecb70b554d33b3c17f3e8b973890f3b3c532da`  
		Last Modified: Wed, 28 Jan 2026 06:19:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:fd7fcbdf0e7f96a083f3d6aec29c9d21ac4b768be5949f68958c25756c153f95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07888c8ad7065e17bfea11af8f4f20b5f956ab1b553160f5ea4a484c4e437674`

```dockerfile
```

-	Layers:
	-	`sha256:aed006a02d773c56c072711ddc729af9ce5001ab757071fc3abdc5094822e7c7`  
		Last Modified: Wed, 28 Jan 2026 06:19:34 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; arm variant v7

```console
$ docker pull memcached@sha256:f08c7e3ff92e718b22bc7b21385421ebcf4bf6f542b797690d6547506821ab35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5272638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a6fc0ce35a3d59414018d4d8fe69929016a9e8dc7dc27daaafc617e3a7165d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:22:45 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:22:46 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:25:41 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:25:41 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:25:41 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:25:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:25:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:25:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:25:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:25:41 GMT
USER memcache
# Wed, 28 Jan 2026 02:25:41 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:25:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f61af882efa215dd577f7a17129442647756c535df9c13e821da864cddcf0e6`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b88f23b7692bcb2301e4e0a862af10c70c6ec663fca9e0a3389a74a3ba0520e`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 92.4 KB (92374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0549b4be8a16d49c33d6adaf28e4f8f7acbdea009dec2daed172741f7540ce5a`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 1.9 MB (1897188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6760f49ea55e45e14e26aaaf690948c109a5d85256175c84bbd06beccc8cd1`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9fca934ad2088c9a34e9f20e65d902054dfb9accdb4c6865924dd1fa88685b`  
		Last Modified: Wed, 28 Jan 2026 02:25:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:b5c2e8ac0b1fd0bd9c534bf163bad10efc0dc2c3afdfb66e3eb1a827d7bbfc87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dd20e2507c3ff3732182e3d2d44e5f7bc9b449bb172d5c7895b2fcc2dd423c6`

```dockerfile
```

-	Layers:
	-	`sha256:36627c0161ebd5c055e99a596a600017e5608e5895d1f95159116ff2df2eb3a6`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 94.3 KB (94291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a5914862f1fb65973ac0def541c9da056e1a5ef0bb26623a5bbad81803a4383`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:1a4aa193f53b5a4e2d82f6c67c23e87ef5d3d1cd1ddf96e0aabe73d49e537c2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6286893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f275b1c508af04216ccc891e9de0d7cbb35441f4eb424197e529ddbfb1d1b62`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:18:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:18:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:20:58 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:20:58 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:20:58 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:20:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:20:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:20:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:20:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:20:59 GMT
USER memcache
# Wed, 28 Jan 2026 02:20:59 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:20:59 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42047232a88cba1fc4d173d71bdf04395f6e4b83472de9f225ae2dd70ce14bc`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b625b9113e283efad9a0ee8e305f08edfd38a6c015224459a1ec0f2f49a0b915`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 121.8 KB (121845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf057b1d31677325905e009d68a97c3741028480d8b254105b145f39d157f2a`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 2.0 MB (1966604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db407fe2bd85342d8cb160bd73b5efe730723df2d20f2f6021eef8ad2d8f16eb`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfefb839a309e8b3df7a659236c09776f4eff9f8a47d9b331f131d9ad4c5d6b`  
		Last Modified: Wed, 28 Jan 2026 02:21:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:28b857747dd2742dbf00b9c1fc07265248073390d37bacf6cf8bfd313cf52a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f34aaccc9ca109270d86cdb6e46e56b207775ad700dadb1604f0a56b3ed4536e`

```dockerfile
```

-	Layers:
	-	`sha256:53b8cb56ae6a2b4c94fae4924dc03d881acba2e6c746fdb05808f3a86186ceff`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 94.3 KB (94327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03361fd0b86b6e905c14afa88e91f00f54a7e68e1d12d191b3d65c41986adc2e`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 20.7 KB (20728 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; 386

```console
$ docker pull memcached@sha256:8c10f776d94f57c5e0a4807247add0a2f3638eaafc3f6571b66ac325cc251866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5741838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f2329492e766d962366bfa352f931d82d7cd74d9e771ae6db7d44c1345197b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:16:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:16:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:18:59 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:18:59 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:18:59 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:18:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:18:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:18:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:18:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:18:59 GMT
USER memcache
# Wed, 28 Jan 2026 02:18:59 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:18:59 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbdb7a800485646296958fbca0c9cfdd5c397a0dbc2e33f1bc0c55dfca3c47a6`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7651295f62c54da7297c4ef646e146ef0acac3f551fb8a3dccc49190efced234`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 110.7 KB (110722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87d7b2cf89ac568b76f6e27208734340c49f4d7b0fedb8e5ae16f54a0cadc43`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 1.9 MB (1942772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4f82eada80af7ef4ec5dfcb36c5a93fa36157801318f374c5ab0d0987cd352`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61a034237824e579d4d24c5ec4b58ee8c400255488e658c36064d43c0001301`  
		Last Modified: Wed, 28 Jan 2026 02:19:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:118dd83c690f154abc02b708a01a0a0a48519b7faa920e5540ebf81c8e626429
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a7e54c817c006a1a17af2f06a4b3e4d1816cb0051c626c3f5e18a5012224b2`

```dockerfile
```

-	Layers:
	-	`sha256:11c94853238efef3a0c48e7cc56222e34874215e568475cfb20d3f2394aad42e`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 94.8 KB (94828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c97d62051151c9b1528a1b64a558c48025170f167ba863808d5fb67d4c59006`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; ppc64le

```console
$ docker pull memcached@sha256:3a553e0d4ee19ee930775d8f8848969c6ff96b11e6b20f159ad754d11f5a8f8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6033619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfcda9c1811a9129ce53ed17b8ca116ffbaeebc21da0604c23b90e0dd042b0aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:33:21 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:33:22 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:35:40 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:35:40 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:35:40 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:35:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:35:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:35:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:35:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:35:41 GMT
USER memcache
# Wed, 28 Jan 2026 02:35:41 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:35:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c501a178d8bd3c1966eb75a7610efc35f292a3662f9fa7ca0d0089f54f723ce9`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac221803a5094f2d41563eece02e2e93293557ecb1eb5b7b646bcf143abcb82`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 126.3 KB (126255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d71af754023c45f69e3c70d3b4bfad1459328a7922268883ea41f2089ffe32ac`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 2.1 MB (2076366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c5df498426baf66bbc7701a67818ff6903c4420dc16591e79270ea8799caa35`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723a9c7624c2d00490e93ff507b003a4b495513fa6ec61b766c50bf5ccb8e23f`  
		Last Modified: Wed, 28 Jan 2026 02:35:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:238c5819c270bbc55c4140407b62939bf6ca158cb58cdbda8098f069301739a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9f43e248be2e248fe895fc3beccdf145fb06637800c6b89c19bf606d7c22975`

```dockerfile
```

-	Layers:
	-	`sha256:88da11471f4f95fd0f4679af21785a14ccb57b8bbd7fb96e4c42e1c49c333c33`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 94.3 KB (94280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b1fb2f254a022e51ca3dae9140daca46922a20d56b46607f22f1eef757d2fbb`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; riscv64

```console
$ docker pull memcached@sha256:8e9681abd0b8d92bb9145c49b7056cd27503f3420c10928ae606e4a65bdb9c9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5769974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:402a203724e613388d65f9de266b282381d864954d277c9552b24343915e9c40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 08:29:56 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 08:29:59 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 08:43:13 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 08:43:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 08:43:13 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 08:43:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 08:43:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 08:43:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 08:43:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 08:43:14 GMT
USER memcache
# Wed, 28 Jan 2026 08:43:14 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 08:43:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914e61f980ba6c54647d03d80091a261aae3ba7ab3d715251e992ea9407ad42e`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d963624519ed571edcf05aed3166ea5b7c1cd5fdae41a0d996d79be268f71e85`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 108.9 KB (108895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab35062ef9866f40cf3445147d50436a982e80d0ed984cca2f11d3ebcde5821`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 2.1 MB (2074437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82838004f4581bf0e6c37cecd3054aeb9fe5e1b92aeeb8cab2e86d9f9ed17af9`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b15a31cacc0f8dc4445667f3d0689a9857004aef390e2a16f7987db8124da4d7`  
		Last Modified: Wed, 28 Jan 2026 08:43:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:f15acc0a96b37da08e228c4fc099dbf28f370723c976c1a8a4d08679f5384799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c47e5bd1d37bec13b189586d46312efcb90ac656c7a80b9fd45fde1dd13f8e6e`

```dockerfile
```

-	Layers:
	-	`sha256:216d743a064cca1bd85c432678c24f3fa640798967115037f27c923138aa7af6`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 94.3 KB (94276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c38c6e624d8af51c7da79f4f214eb73cbfe3c2a2f9b465649a72b8dfa18429f`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; s390x

```console
$ docker pull memcached@sha256:f52690bd1266bfbe887fa9c03fc963f0277f331a85d8e81f4f134076c6d899f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5858103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7903f118ee1fcea4632b09ffbabd30b82ef4aa3b68dd3570b1173f263cacc343`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:21:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:21:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:24:07 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:24:07 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:24:07 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:24:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:24:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:24:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:24:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:24:08 GMT
USER memcache
# Wed, 28 Jan 2026 02:24:08 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:24:08 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030f843902eb7c01da3de08b6efb672d46d4f41e9e298640c66daabea5d901ef`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100608bf5f6494395c46670a28e6df9d705e08dc9129c1fb36b8f265fa52c22b`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 114.3 KB (114299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b706c73349baf76aabbef50d7dba3c89b85ffc84ad0aca5c544b1fe047706785`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 2.0 MB (2017124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce545f5bb33e4374e2e0bb9b11e751c89272699812f06c49e8e6a2e5ac3d524`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ac2e9e98ac3e799be9d54501be2f2304ef93065d34bef18f002ea38838ea24`  
		Last Modified: Wed, 28 Jan 2026 02:24:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:b4850489cf16ad5f72674b698ab0c2d16d95c6cc43e1b3f611f9fa67adcf4962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b79deed0597f9356a7dd99d34cb933d7634c520350fcabb9da14b254006070d0`

```dockerfile
```

-	Layers:
	-	`sha256:00a586e58a4b437f0260b3197ecff606cb3380869c6861c89d769a99132c10e9`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 94.2 KB (94222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8caeef6fbf9d37a3d092d84298ef02b53e2efff54347431fcc362c14dcdb9eb5`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:27 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b6e737e1a3eed198cc17e2b92231ab084bcf55ba90a36136e7a2f4fd04a95b`  
		Last Modified: Tue, 13 Jan 2026 01:25:25 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16835fec399670b74d32630a7368a65ca2a3c32d8b7a690d33bebc7b9e9458d`  
		Last Modified: Tue, 13 Jan 2026 01:25:24 GMT  
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
		Last Modified: Tue, 13 Jan 2026 01:25:25 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 27.9 MB (27942724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96776850dc1206c3fd163b84cea19599306159eb0d020b4241d0172240f88d13`  
		Last Modified: Tue, 13 Jan 2026 01:22:50 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3697c7c790d9c4caaa904abdaf809dcdee3f0b518fc5ad82d2e21dd7fe24f64d`  
		Last Modified: Tue, 13 Jan 2026 01:22:50 GMT  
		Size: 144.2 KB (144212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a247339c7ec57a491c3ffe43531dbfaa132f3ff16a481fc41cbb9e3e3ad6476`  
		Last Modified: Tue, 13 Jan 2026 01:22:50 GMT  
		Size: 2.2 MB (2210412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2dcebe3ab2a9945cdea142301e4a64eebbc59c948a54385dbfca4afd561b508`  
		Last Modified: Tue, 13 Jan 2026 01:22:50 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb8ef5ecbc44efd5280f9cf15687dfd80a34fa2966ad039238647177f75dc6c`  
		Last Modified: Tue, 13 Jan 2026 01:22:51 GMT  
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
		Last Modified: Tue, 13 Jan 2026 01:22:50 GMT  
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
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
		Size: 135.4 KB (135398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9371e974781bd91adc657086f00cd7d91b5530ca9da37597c347dd7d4eaff0`  
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
		Size: 2.2 MB (2164040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c2e0f64c0afa16b5e214ae208c8c81e8c78c79ddd90f54983a93c7297395f6b`  
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
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
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
		Size: 2.0 MB (2009750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e76d5584f581b7668c61a661da2858bc1d5e11b31e3629e0d2b3af52d9c22ed8`  
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:41 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78edb6b991369235f90958a936afc89dc37b82439c632988ed143b5bd76deadb`  
		Last Modified: Tue, 13 Jan 2026 01:25:33 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e1afbb765f6cc3923e864d44fb6cd6c9167b884e596b09bd37c7c276f65a2b`  
		Last Modified: Tue, 13 Jan 2026 01:25:33 GMT  
		Size: 153.5 KB (153512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff9edc68fe57c233001afd442eb6c248bf070d32fbb412a8bfeef6f9a6217f5`  
		Last Modified: Tue, 13 Jan 2026 01:25:33 GMT  
		Size: 2.3 MB (2261341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c4648fbc4a4189184946895d1041e0eee2c5d40fd70638a553bedb0cbf5cf8`  
		Last Modified: Tue, 13 Jan 2026 01:25:33 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26bd1b32b048e73091ddf6e6762e368d4bb6ef2cc7d3aa43467749b36fe08e38`  
		Last Modified: Tue, 13 Jan 2026 01:25:34 GMT  
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
		Last Modified: Tue, 13 Jan 2026 01:25:33 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:56 GMT  
		Size: 31.3 MB (31288476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cedb4f2840edea9de46e0d955a0512f469211880560a8948f10b54381bcd728`  
		Last Modified: Tue, 13 Jan 2026 01:22:46 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c4b2d1574ee5f238dc6948164abd39ffcc91929b2c464c6b3874dec01fd964`  
		Last Modified: Tue, 13 Jan 2026 01:22:46 GMT  
		Size: 147.6 KB (147554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc1bf5870b84175607f3d012b3cfebc5859869f8125114ea5d6ed1a05f81d2d`  
		Last Modified: Tue, 13 Jan 2026 01:22:46 GMT  
		Size: 2.2 MB (2223652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6434e73ed67e81f1016f27c7cc175290b0ce959d8a1bf5e9b0f3119f161246`  
		Last Modified: Tue, 13 Jan 2026 01:22:46 GMT  
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
		Last Modified: Tue, 13 Jan 2026 01:22:46 GMT  
		Size: 2.0 MB (2005447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6358862e12c5c5367efd52bea0b1194e04e76f267084da591229f64ee7482dc3`  
		Last Modified: Tue, 13 Jan 2026 01:22:46 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:57:06 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093e59deb53ff01a892be2a5df928c4b04a289df7f6c135570c11d6a4fdbc53a`  
		Last Modified: Tue, 13 Jan 2026 01:37:09 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4da25c8b13ee47050a38843c1954d2bd7bbdba2666f725aee2f603e03fcb6d`  
		Last Modified: Tue, 13 Jan 2026 01:37:09 GMT  
		Size: 170.4 KB (170427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cab5f6f805c735c0f324c87ff8c66cfab0e35fb691b7761e85bb9a2bbb31cfe`  
		Last Modified: Tue, 13 Jan 2026 01:37:09 GMT  
		Size: 2.4 MB (2393947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3a7dfc8da65bd6101de156530bc2688c5588c718bbc3131ff4594cbefd0e66`  
		Last Modified: Tue, 13 Jan 2026 01:37:09 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06153b2e2bde9b06f1c2719aabb5ff6a6c23056152a024fa2c990d97b4d9c799`  
		Last Modified: Tue, 13 Jan 2026 01:37:10 GMT  
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
		Last Modified: Tue, 13 Jan 2026 01:37:09 GMT  
		Size: 2.0 MB (2011891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc718b3aa0399c50248bba6165cad8666196a5351b6ed095a8101d2f8a5d37da`  
		Last Modified: Tue, 13 Jan 2026 01:37:09 GMT  
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
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168d1b37fe07dfb8bef5240057ad6597058647499a9e771eedd2091f2d6b30f0`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 133.1 KB (133105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a5ebc1ef49cab24f75e0c751a1e0563ee042c246c509279fa38cf3cbf0a3f1`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 2.2 MB (2207499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbc8df7ca1d2f273c3c8fec55b30f17ebc72a45687976efd9c8779a66369d46`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4057c9476d421ae1ecae3607afb0db57dbc6eb2bc0aa5e41daed169a70319c1`  
		Last Modified: Wed, 14 Jan 2026 06:50:29 GMT  
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
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 2.0 MB (2002254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0de5bd0cbff9df1fc11e05bd38936b6915195663b273b5c23840bf5eb9373a8`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
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
		Last Modified: Tue, 13 Jan 2026 13:10:27 GMT  
		Size: 29.8 MB (29833411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2727771ad16d920baecb7c96b9b54e67178369b881fc20901d381dfd5f873e27`  
		Last Modified: Tue, 13 Jan 2026 14:17:08 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6b0ec5581f8591522a6327cdcfa4e1197d9ada9fb60840f57b5d3e4dd3304d1`  
		Last Modified: Tue, 13 Jan 2026 14:17:08 GMT  
		Size: 140.6 KB (140562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382a3e1ebed70673a0789fcc2104ab941fe04b9a020339f9286ac85b67ae5ff9`  
		Last Modified: Tue, 13 Jan 2026 14:17:08 GMT  
		Size: 2.3 MB (2297368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85fe5f9afd355e3dd76ce942e1c295e356d96ae3b0e3f8236a0e33c5f75ffe71`  
		Last Modified: Tue, 13 Jan 2026 14:17:08 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4546f3c3457928dc273f98dae7c7ac2f945b203138e964ee72fc92aabcef434`  
		Last Modified: Tue, 13 Jan 2026 14:17:09 GMT  
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
		Last Modified: Tue, 13 Jan 2026 14:17:08 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:27 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b6e737e1a3eed198cc17e2b92231ab084bcf55ba90a36136e7a2f4fd04a95b`  
		Last Modified: Tue, 13 Jan 2026 01:25:25 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16835fec399670b74d32630a7368a65ca2a3c32d8b7a690d33bebc7b9e9458d`  
		Last Modified: Tue, 13 Jan 2026 01:25:24 GMT  
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
		Last Modified: Tue, 13 Jan 2026 01:25:25 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 27.9 MB (27942724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96776850dc1206c3fd163b84cea19599306159eb0d020b4241d0172240f88d13`  
		Last Modified: Tue, 13 Jan 2026 01:22:50 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3697c7c790d9c4caaa904abdaf809dcdee3f0b518fc5ad82d2e21dd7fe24f64d`  
		Last Modified: Tue, 13 Jan 2026 01:22:50 GMT  
		Size: 144.2 KB (144212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a247339c7ec57a491c3ffe43531dbfaa132f3ff16a481fc41cbb9e3e3ad6476`  
		Last Modified: Tue, 13 Jan 2026 01:22:50 GMT  
		Size: 2.2 MB (2210412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2dcebe3ab2a9945cdea142301e4a64eebbc59c948a54385dbfca4afd561b508`  
		Last Modified: Tue, 13 Jan 2026 01:22:50 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb8ef5ecbc44efd5280f9cf15687dfd80a34fa2966ad039238647177f75dc6c`  
		Last Modified: Tue, 13 Jan 2026 01:22:51 GMT  
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
		Last Modified: Tue, 13 Jan 2026 01:22:50 GMT  
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
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
		Size: 135.4 KB (135398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9371e974781bd91adc657086f00cd7d91b5530ca9da37597c347dd7d4eaff0`  
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
		Size: 2.2 MB (2164040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c2e0f64c0afa16b5e214ae208c8c81e8c78c79ddd90f54983a93c7297395f6b`  
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
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
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
		Size: 2.0 MB (2009750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e76d5584f581b7668c61a661da2858bc1d5e11b31e3629e0d2b3af52d9c22ed8`  
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:41 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78edb6b991369235f90958a936afc89dc37b82439c632988ed143b5bd76deadb`  
		Last Modified: Tue, 13 Jan 2026 01:25:33 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e1afbb765f6cc3923e864d44fb6cd6c9167b884e596b09bd37c7c276f65a2b`  
		Last Modified: Tue, 13 Jan 2026 01:25:33 GMT  
		Size: 153.5 KB (153512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff9edc68fe57c233001afd442eb6c248bf070d32fbb412a8bfeef6f9a6217f5`  
		Last Modified: Tue, 13 Jan 2026 01:25:33 GMT  
		Size: 2.3 MB (2261341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c4648fbc4a4189184946895d1041e0eee2c5d40fd70638a553bedb0cbf5cf8`  
		Last Modified: Tue, 13 Jan 2026 01:25:33 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26bd1b32b048e73091ddf6e6762e368d4bb6ef2cc7d3aa43467749b36fe08e38`  
		Last Modified: Tue, 13 Jan 2026 01:25:34 GMT  
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
		Last Modified: Tue, 13 Jan 2026 01:25:33 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:56 GMT  
		Size: 31.3 MB (31288476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cedb4f2840edea9de46e0d955a0512f469211880560a8948f10b54381bcd728`  
		Last Modified: Tue, 13 Jan 2026 01:22:46 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c4b2d1574ee5f238dc6948164abd39ffcc91929b2c464c6b3874dec01fd964`  
		Last Modified: Tue, 13 Jan 2026 01:22:46 GMT  
		Size: 147.6 KB (147554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc1bf5870b84175607f3d012b3cfebc5859869f8125114ea5d6ed1a05f81d2d`  
		Last Modified: Tue, 13 Jan 2026 01:22:46 GMT  
		Size: 2.2 MB (2223652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6434e73ed67e81f1016f27c7cc175290b0ce959d8a1bf5e9b0f3119f161246`  
		Last Modified: Tue, 13 Jan 2026 01:22:46 GMT  
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
		Last Modified: Tue, 13 Jan 2026 01:22:46 GMT  
		Size: 2.0 MB (2005447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6358862e12c5c5367efd52bea0b1194e04e76f267084da591229f64ee7482dc3`  
		Last Modified: Tue, 13 Jan 2026 01:22:46 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:57:06 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093e59deb53ff01a892be2a5df928c4b04a289df7f6c135570c11d6a4fdbc53a`  
		Last Modified: Tue, 13 Jan 2026 01:37:09 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4da25c8b13ee47050a38843c1954d2bd7bbdba2666f725aee2f603e03fcb6d`  
		Last Modified: Tue, 13 Jan 2026 01:37:09 GMT  
		Size: 170.4 KB (170427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cab5f6f805c735c0f324c87ff8c66cfab0e35fb691b7761e85bb9a2bbb31cfe`  
		Last Modified: Tue, 13 Jan 2026 01:37:09 GMT  
		Size: 2.4 MB (2393947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3a7dfc8da65bd6101de156530bc2688c5588c718bbc3131ff4594cbefd0e66`  
		Last Modified: Tue, 13 Jan 2026 01:37:09 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06153b2e2bde9b06f1c2719aabb5ff6a6c23056152a024fa2c990d97b4d9c799`  
		Last Modified: Tue, 13 Jan 2026 01:37:10 GMT  
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
		Last Modified: Tue, 13 Jan 2026 01:37:09 GMT  
		Size: 2.0 MB (2011891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc718b3aa0399c50248bba6165cad8666196a5351b6ed095a8101d2f8a5d37da`  
		Last Modified: Tue, 13 Jan 2026 01:37:09 GMT  
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
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168d1b37fe07dfb8bef5240057ad6597058647499a9e771eedd2091f2d6b30f0`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 133.1 KB (133105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a5ebc1ef49cab24f75e0c751a1e0563ee042c246c509279fa38cf3cbf0a3f1`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 2.2 MB (2207499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbc8df7ca1d2f273c3c8fec55b30f17ebc72a45687976efd9c8779a66369d46`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4057c9476d421ae1ecae3607afb0db57dbc6eb2bc0aa5e41daed169a70319c1`  
		Last Modified: Wed, 14 Jan 2026 06:50:29 GMT  
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
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 2.0 MB (2002254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0de5bd0cbff9df1fc11e05bd38936b6915195663b273b5c23840bf5eb9373a8`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
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
		Last Modified: Tue, 13 Jan 2026 13:10:27 GMT  
		Size: 29.8 MB (29833411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2727771ad16d920baecb7c96b9b54e67178369b881fc20901d381dfd5f873e27`  
		Last Modified: Tue, 13 Jan 2026 14:17:08 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6b0ec5581f8591522a6327cdcfa4e1197d9ada9fb60840f57b5d3e4dd3304d1`  
		Last Modified: Tue, 13 Jan 2026 14:17:08 GMT  
		Size: 140.6 KB (140562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382a3e1ebed70673a0789fcc2104ab941fe04b9a020339f9286ac85b67ae5ff9`  
		Last Modified: Tue, 13 Jan 2026 14:17:08 GMT  
		Size: 2.3 MB (2297368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85fe5f9afd355e3dd76ce942e1c295e356d96ae3b0e3f8236a0e33c5f75ffe71`  
		Last Modified: Tue, 13 Jan 2026 14:17:08 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4546f3c3457928dc273f98dae7c7ac2f945b203138e964ee72fc92aabcef434`  
		Last Modified: Tue, 13 Jan 2026 14:17:09 GMT  
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
		Last Modified: Tue, 13 Jan 2026 14:17:08 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine`

```console
$ docker pull memcached@sha256:8a82a3927694e42bc52679dc81532244de51e5faed5f9541a1283e3ad7271db1
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
$ docker pull memcached@sha256:947366d40559340a4385b3e05f92186b9546e7feb59ef280e243ec8bf34f01a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5958530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7977390ffe9a7f3b6d3c5840f262b8058ca015d7daf5237e480d3f51a29e0b6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:18:28 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:18:29 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:21:03 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:21:03 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:21:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:21:03 GMT
USER memcache
# Wed, 28 Jan 2026 02:21:03 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:21:03 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e0ee508166c94a4f9ca8c32f743bd3733afb7660800042c7da03c2ea1da6b4`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15bf9562ecbc21cc4f52d1a4d33eb5eec98aa63c36c59f018b55071b8dd9f05f`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 106.1 KB (106059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24c6974a0da2f6cdd2022450be6195683245ba21f601d207ad14566c653ddea`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 2.0 MB (1989295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a859de0eb0253d066d7de73c90f4ebdc8b737fddab90420fd0ba6bd1c74669`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7be89a9ef60cc91d2346c9bc9a975138908bbc03aa40c948ab5e7336aa8e8b`  
		Last Modified: Wed, 28 Jan 2026 02:21:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7579a20056cd9531e754a57f957da811356775f676bfa6cd6e86b95f6de172d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8408948e08375e96299e735072f97a85aca5d58f65fc7cca125dfe5389160cb`

```dockerfile
```

-	Layers:
	-	`sha256:533c466de2027803aea398674e5a5ffd7d67b9e1eddc4228741a130ff830b02a`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 94.9 KB (94873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27c54b10e342535e2af7655af306fbf617d3dbf0922a7dd440f8ed4ea3e1fd5c`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:3a1e785feba037614143f75204bac3225d838127c68805b29ff23df9d8638070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c891a4120404380161eeeddd4e7c7cb748eb55193453c6e9090a59909bf1969`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 06:07:09 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 06:07:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 06:19:29 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 06:19:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 06:19:29 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 06:19:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 06:19:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 06:19:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 06:19:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 06:19:29 GMT
USER memcache
# Wed, 28 Jan 2026 06:19:29 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 06:19:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9dfe3bd7930f213b1f0f6c2854f26637f5a52c7cd4796e9eb59071fe2ff4b2f`  
		Last Modified: Wed, 28 Jan 2026 06:19:33 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:707447698613ddcfad121290546b5d9e04e2c3194b8f59394a272fe30f42dba1`  
		Last Modified: Wed, 28 Jan 2026 06:19:33 GMT  
		Size: 102.6 KB (102646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d366a66d67c4233b2ac1bc38363cb9881e63ca3af7f82ebbffbfb76942e1a34`  
		Last Modified: Wed, 28 Jan 2026 06:19:34 GMT  
		Size: 1.9 MB (1939230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e5326e5c6353c918ea1ac99aedfb19f688830f93037e66268b39c31f670e01`  
		Last Modified: Wed, 28 Jan 2026 06:19:33 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2ead2e4800bd6e32bbdb6225ecb70b554d33b3c17f3e8b973890f3b3c532da`  
		Last Modified: Wed, 28 Jan 2026 06:19:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:fd7fcbdf0e7f96a083f3d6aec29c9d21ac4b768be5949f68958c25756c153f95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07888c8ad7065e17bfea11af8f4f20b5f956ab1b553160f5ea4a484c4e437674`

```dockerfile
```

-	Layers:
	-	`sha256:aed006a02d773c56c072711ddc729af9ce5001ab757071fc3abdc5094822e7c7`  
		Last Modified: Wed, 28 Jan 2026 06:19:34 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:f08c7e3ff92e718b22bc7b21385421ebcf4bf6f542b797690d6547506821ab35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5272638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a6fc0ce35a3d59414018d4d8fe69929016a9e8dc7dc27daaafc617e3a7165d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:22:45 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:22:46 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:25:41 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:25:41 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:25:41 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:25:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:25:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:25:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:25:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:25:41 GMT
USER memcache
# Wed, 28 Jan 2026 02:25:41 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:25:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f61af882efa215dd577f7a17129442647756c535df9c13e821da864cddcf0e6`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b88f23b7692bcb2301e4e0a862af10c70c6ec663fca9e0a3389a74a3ba0520e`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 92.4 KB (92374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0549b4be8a16d49c33d6adaf28e4f8f7acbdea009dec2daed172741f7540ce5a`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 1.9 MB (1897188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6760f49ea55e45e14e26aaaf690948c109a5d85256175c84bbd06beccc8cd1`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9fca934ad2088c9a34e9f20e65d902054dfb9accdb4c6865924dd1fa88685b`  
		Last Modified: Wed, 28 Jan 2026 02:25:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:b5c2e8ac0b1fd0bd9c534bf163bad10efc0dc2c3afdfb66e3eb1a827d7bbfc87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dd20e2507c3ff3732182e3d2d44e5f7bc9b449bb172d5c7895b2fcc2dd423c6`

```dockerfile
```

-	Layers:
	-	`sha256:36627c0161ebd5c055e99a596a600017e5608e5895d1f95159116ff2df2eb3a6`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 94.3 KB (94291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a5914862f1fb65973ac0def541c9da056e1a5ef0bb26623a5bbad81803a4383`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:1a4aa193f53b5a4e2d82f6c67c23e87ef5d3d1cd1ddf96e0aabe73d49e537c2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6286893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f275b1c508af04216ccc891e9de0d7cbb35441f4eb424197e529ddbfb1d1b62`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:18:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:18:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:20:58 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:20:58 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:20:58 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:20:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:20:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:20:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:20:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:20:59 GMT
USER memcache
# Wed, 28 Jan 2026 02:20:59 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:20:59 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42047232a88cba1fc4d173d71bdf04395f6e4b83472de9f225ae2dd70ce14bc`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b625b9113e283efad9a0ee8e305f08edfd38a6c015224459a1ec0f2f49a0b915`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 121.8 KB (121845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf057b1d31677325905e009d68a97c3741028480d8b254105b145f39d157f2a`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 2.0 MB (1966604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db407fe2bd85342d8cb160bd73b5efe730723df2d20f2f6021eef8ad2d8f16eb`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfefb839a309e8b3df7a659236c09776f4eff9f8a47d9b331f131d9ad4c5d6b`  
		Last Modified: Wed, 28 Jan 2026 02:21:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:28b857747dd2742dbf00b9c1fc07265248073390d37bacf6cf8bfd313cf52a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f34aaccc9ca109270d86cdb6e46e56b207775ad700dadb1604f0a56b3ed4536e`

```dockerfile
```

-	Layers:
	-	`sha256:53b8cb56ae6a2b4c94fae4924dc03d881acba2e6c746fdb05808f3a86186ceff`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 94.3 KB (94327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03361fd0b86b6e905c14afa88e91f00f54a7e68e1d12d191b3d65c41986adc2e`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 20.7 KB (20728 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; 386

```console
$ docker pull memcached@sha256:8c10f776d94f57c5e0a4807247add0a2f3638eaafc3f6571b66ac325cc251866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5741838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f2329492e766d962366bfa352f931d82d7cd74d9e771ae6db7d44c1345197b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:16:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:16:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:18:59 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:18:59 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:18:59 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:18:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:18:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:18:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:18:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:18:59 GMT
USER memcache
# Wed, 28 Jan 2026 02:18:59 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:18:59 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbdb7a800485646296958fbca0c9cfdd5c397a0dbc2e33f1bc0c55dfca3c47a6`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7651295f62c54da7297c4ef646e146ef0acac3f551fb8a3dccc49190efced234`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 110.7 KB (110722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87d7b2cf89ac568b76f6e27208734340c49f4d7b0fedb8e5ae16f54a0cadc43`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 1.9 MB (1942772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4f82eada80af7ef4ec5dfcb36c5a93fa36157801318f374c5ab0d0987cd352`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61a034237824e579d4d24c5ec4b58ee8c400255488e658c36064d43c0001301`  
		Last Modified: Wed, 28 Jan 2026 02:19:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:118dd83c690f154abc02b708a01a0a0a48519b7faa920e5540ebf81c8e626429
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a7e54c817c006a1a17af2f06a4b3e4d1816cb0051c626c3f5e18a5012224b2`

```dockerfile
```

-	Layers:
	-	`sha256:11c94853238efef3a0c48e7cc56222e34874215e568475cfb20d3f2394aad42e`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 94.8 KB (94828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c97d62051151c9b1528a1b64a558c48025170f167ba863808d5fb67d4c59006`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:3a553e0d4ee19ee930775d8f8848969c6ff96b11e6b20f159ad754d11f5a8f8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6033619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfcda9c1811a9129ce53ed17b8ca116ffbaeebc21da0604c23b90e0dd042b0aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:33:21 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:33:22 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:35:40 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:35:40 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:35:40 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:35:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:35:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:35:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:35:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:35:41 GMT
USER memcache
# Wed, 28 Jan 2026 02:35:41 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:35:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c501a178d8bd3c1966eb75a7610efc35f292a3662f9fa7ca0d0089f54f723ce9`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac221803a5094f2d41563eece02e2e93293557ecb1eb5b7b646bcf143abcb82`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 126.3 KB (126255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d71af754023c45f69e3c70d3b4bfad1459328a7922268883ea41f2089ffe32ac`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 2.1 MB (2076366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c5df498426baf66bbc7701a67818ff6903c4420dc16591e79270ea8799caa35`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723a9c7624c2d00490e93ff507b003a4b495513fa6ec61b766c50bf5ccb8e23f`  
		Last Modified: Wed, 28 Jan 2026 02:35:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:238c5819c270bbc55c4140407b62939bf6ca158cb58cdbda8098f069301739a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9f43e248be2e248fe895fc3beccdf145fb06637800c6b89c19bf606d7c22975`

```dockerfile
```

-	Layers:
	-	`sha256:88da11471f4f95fd0f4679af21785a14ccb57b8bbd7fb96e4c42e1c49c333c33`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 94.3 KB (94280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b1fb2f254a022e51ca3dae9140daca46922a20d56b46607f22f1eef757d2fbb`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:8e9681abd0b8d92bb9145c49b7056cd27503f3420c10928ae606e4a65bdb9c9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5769974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:402a203724e613388d65f9de266b282381d864954d277c9552b24343915e9c40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 08:29:56 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 08:29:59 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 08:43:13 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 08:43:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 08:43:13 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 08:43:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 08:43:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 08:43:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 08:43:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 08:43:14 GMT
USER memcache
# Wed, 28 Jan 2026 08:43:14 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 08:43:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914e61f980ba6c54647d03d80091a261aae3ba7ab3d715251e992ea9407ad42e`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d963624519ed571edcf05aed3166ea5b7c1cd5fdae41a0d996d79be268f71e85`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 108.9 KB (108895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab35062ef9866f40cf3445147d50436a982e80d0ed984cca2f11d3ebcde5821`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 2.1 MB (2074437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82838004f4581bf0e6c37cecd3054aeb9fe5e1b92aeeb8cab2e86d9f9ed17af9`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b15a31cacc0f8dc4445667f3d0689a9857004aef390e2a16f7987db8124da4d7`  
		Last Modified: Wed, 28 Jan 2026 08:43:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:f15acc0a96b37da08e228c4fc099dbf28f370723c976c1a8a4d08679f5384799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c47e5bd1d37bec13b189586d46312efcb90ac656c7a80b9fd45fde1dd13f8e6e`

```dockerfile
```

-	Layers:
	-	`sha256:216d743a064cca1bd85c432678c24f3fa640798967115037f27c923138aa7af6`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 94.3 KB (94276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c38c6e624d8af51c7da79f4f214eb73cbfe3c2a2f9b465649a72b8dfa18429f`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:f52690bd1266bfbe887fa9c03fc963f0277f331a85d8e81f4f134076c6d899f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5858103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7903f118ee1fcea4632b09ffbabd30b82ef4aa3b68dd3570b1173f263cacc343`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:21:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:21:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:24:07 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:24:07 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:24:07 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:24:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:24:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:24:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:24:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:24:08 GMT
USER memcache
# Wed, 28 Jan 2026 02:24:08 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:24:08 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030f843902eb7c01da3de08b6efb672d46d4f41e9e298640c66daabea5d901ef`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100608bf5f6494395c46670a28e6df9d705e08dc9129c1fb36b8f265fa52c22b`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 114.3 KB (114299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b706c73349baf76aabbef50d7dba3c89b85ffc84ad0aca5c544b1fe047706785`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 2.0 MB (2017124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce545f5bb33e4374e2e0bb9b11e751c89272699812f06c49e8e6a2e5ac3d524`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ac2e9e98ac3e799be9d54501be2f2304ef93065d34bef18f002ea38838ea24`  
		Last Modified: Wed, 28 Jan 2026 02:24:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:b4850489cf16ad5f72674b698ab0c2d16d95c6cc43e1b3f611f9fa67adcf4962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b79deed0597f9356a7dd99d34cb933d7634c520350fcabb9da14b254006070d0`

```dockerfile
```

-	Layers:
	-	`sha256:00a586e58a4b437f0260b3197ecff606cb3380869c6861c89d769a99132c10e9`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 94.2 KB (94222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8caeef6fbf9d37a3d092d84298ef02b53e2efff54347431fcc362c14dcdb9eb5`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine3.23`

```console
$ docker pull memcached@sha256:8a82a3927694e42bc52679dc81532244de51e5faed5f9541a1283e3ad7271db1
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
$ docker pull memcached@sha256:947366d40559340a4385b3e05f92186b9546e7feb59ef280e243ec8bf34f01a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5958530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7977390ffe9a7f3b6d3c5840f262b8058ca015d7daf5237e480d3f51a29e0b6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:18:28 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:18:29 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:21:03 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:21:03 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:21:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:21:03 GMT
USER memcache
# Wed, 28 Jan 2026 02:21:03 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:21:03 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e0ee508166c94a4f9ca8c32f743bd3733afb7660800042c7da03c2ea1da6b4`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15bf9562ecbc21cc4f52d1a4d33eb5eec98aa63c36c59f018b55071b8dd9f05f`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 106.1 KB (106059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24c6974a0da2f6cdd2022450be6195683245ba21f601d207ad14566c653ddea`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 2.0 MB (1989295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a859de0eb0253d066d7de73c90f4ebdc8b737fddab90420fd0ba6bd1c74669`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7be89a9ef60cc91d2346c9bc9a975138908bbc03aa40c948ab5e7336aa8e8b`  
		Last Modified: Wed, 28 Jan 2026 02:21:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:7579a20056cd9531e754a57f957da811356775f676bfa6cd6e86b95f6de172d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8408948e08375e96299e735072f97a85aca5d58f65fc7cca125dfe5389160cb`

```dockerfile
```

-	Layers:
	-	`sha256:533c466de2027803aea398674e5a5ffd7d67b9e1eddc4228741a130ff830b02a`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 94.9 KB (94873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27c54b10e342535e2af7655af306fbf617d3dbf0922a7dd440f8ed4ea3e1fd5c`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.23` - linux; arm variant v6

```console
$ docker pull memcached@sha256:3a1e785feba037614143f75204bac3225d838127c68805b29ff23df9d8638070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c891a4120404380161eeeddd4e7c7cb748eb55193453c6e9090a59909bf1969`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 06:07:09 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 06:07:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 06:19:29 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 06:19:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 06:19:29 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 06:19:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 06:19:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 06:19:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 06:19:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 06:19:29 GMT
USER memcache
# Wed, 28 Jan 2026 06:19:29 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 06:19:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9dfe3bd7930f213b1f0f6c2854f26637f5a52c7cd4796e9eb59071fe2ff4b2f`  
		Last Modified: Wed, 28 Jan 2026 06:19:33 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:707447698613ddcfad121290546b5d9e04e2c3194b8f59394a272fe30f42dba1`  
		Last Modified: Wed, 28 Jan 2026 06:19:33 GMT  
		Size: 102.6 KB (102646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d366a66d67c4233b2ac1bc38363cb9881e63ca3af7f82ebbffbfb76942e1a34`  
		Last Modified: Wed, 28 Jan 2026 06:19:34 GMT  
		Size: 1.9 MB (1939230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e5326e5c6353c918ea1ac99aedfb19f688830f93037e66268b39c31f670e01`  
		Last Modified: Wed, 28 Jan 2026 06:19:33 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2ead2e4800bd6e32bbdb6225ecb70b554d33b3c17f3e8b973890f3b3c532da`  
		Last Modified: Wed, 28 Jan 2026 06:19:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:fd7fcbdf0e7f96a083f3d6aec29c9d21ac4b768be5949f68958c25756c153f95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07888c8ad7065e17bfea11af8f4f20b5f956ab1b553160f5ea4a484c4e437674`

```dockerfile
```

-	Layers:
	-	`sha256:aed006a02d773c56c072711ddc729af9ce5001ab757071fc3abdc5094822e7c7`  
		Last Modified: Wed, 28 Jan 2026 06:19:34 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.23` - linux; arm variant v7

```console
$ docker pull memcached@sha256:f08c7e3ff92e718b22bc7b21385421ebcf4bf6f542b797690d6547506821ab35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5272638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a6fc0ce35a3d59414018d4d8fe69929016a9e8dc7dc27daaafc617e3a7165d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:22:45 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:22:46 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:25:41 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:25:41 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:25:41 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:25:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:25:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:25:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:25:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:25:41 GMT
USER memcache
# Wed, 28 Jan 2026 02:25:41 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:25:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f61af882efa215dd577f7a17129442647756c535df9c13e821da864cddcf0e6`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b88f23b7692bcb2301e4e0a862af10c70c6ec663fca9e0a3389a74a3ba0520e`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 92.4 KB (92374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0549b4be8a16d49c33d6adaf28e4f8f7acbdea009dec2daed172741f7540ce5a`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 1.9 MB (1897188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6760f49ea55e45e14e26aaaf690948c109a5d85256175c84bbd06beccc8cd1`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9fca934ad2088c9a34e9f20e65d902054dfb9accdb4c6865924dd1fa88685b`  
		Last Modified: Wed, 28 Jan 2026 02:25:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:b5c2e8ac0b1fd0bd9c534bf163bad10efc0dc2c3afdfb66e3eb1a827d7bbfc87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dd20e2507c3ff3732182e3d2d44e5f7bc9b449bb172d5c7895b2fcc2dd423c6`

```dockerfile
```

-	Layers:
	-	`sha256:36627c0161ebd5c055e99a596a600017e5608e5895d1f95159116ff2df2eb3a6`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 94.3 KB (94291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a5914862f1fb65973ac0def541c9da056e1a5ef0bb26623a5bbad81803a4383`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:1a4aa193f53b5a4e2d82f6c67c23e87ef5d3d1cd1ddf96e0aabe73d49e537c2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6286893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f275b1c508af04216ccc891e9de0d7cbb35441f4eb424197e529ddbfb1d1b62`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:18:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:18:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:20:58 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:20:58 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:20:58 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:20:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:20:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:20:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:20:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:20:59 GMT
USER memcache
# Wed, 28 Jan 2026 02:20:59 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:20:59 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42047232a88cba1fc4d173d71bdf04395f6e4b83472de9f225ae2dd70ce14bc`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b625b9113e283efad9a0ee8e305f08edfd38a6c015224459a1ec0f2f49a0b915`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 121.8 KB (121845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf057b1d31677325905e009d68a97c3741028480d8b254105b145f39d157f2a`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 2.0 MB (1966604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db407fe2bd85342d8cb160bd73b5efe730723df2d20f2f6021eef8ad2d8f16eb`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfefb839a309e8b3df7a659236c09776f4eff9f8a47d9b331f131d9ad4c5d6b`  
		Last Modified: Wed, 28 Jan 2026 02:21:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:28b857747dd2742dbf00b9c1fc07265248073390d37bacf6cf8bfd313cf52a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f34aaccc9ca109270d86cdb6e46e56b207775ad700dadb1604f0a56b3ed4536e`

```dockerfile
```

-	Layers:
	-	`sha256:53b8cb56ae6a2b4c94fae4924dc03d881acba2e6c746fdb05808f3a86186ceff`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 94.3 KB (94327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03361fd0b86b6e905c14afa88e91f00f54a7e68e1d12d191b3d65c41986adc2e`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 20.7 KB (20728 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.23` - linux; 386

```console
$ docker pull memcached@sha256:8c10f776d94f57c5e0a4807247add0a2f3638eaafc3f6571b66ac325cc251866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5741838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f2329492e766d962366bfa352f931d82d7cd74d9e771ae6db7d44c1345197b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:16:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:16:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:18:59 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:18:59 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:18:59 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:18:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:18:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:18:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:18:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:18:59 GMT
USER memcache
# Wed, 28 Jan 2026 02:18:59 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:18:59 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbdb7a800485646296958fbca0c9cfdd5c397a0dbc2e33f1bc0c55dfca3c47a6`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7651295f62c54da7297c4ef646e146ef0acac3f551fb8a3dccc49190efced234`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 110.7 KB (110722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87d7b2cf89ac568b76f6e27208734340c49f4d7b0fedb8e5ae16f54a0cadc43`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 1.9 MB (1942772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4f82eada80af7ef4ec5dfcb36c5a93fa36157801318f374c5ab0d0987cd352`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61a034237824e579d4d24c5ec4b58ee8c400255488e658c36064d43c0001301`  
		Last Modified: Wed, 28 Jan 2026 02:19:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:118dd83c690f154abc02b708a01a0a0a48519b7faa920e5540ebf81c8e626429
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a7e54c817c006a1a17af2f06a4b3e4d1816cb0051c626c3f5e18a5012224b2`

```dockerfile
```

-	Layers:
	-	`sha256:11c94853238efef3a0c48e7cc56222e34874215e568475cfb20d3f2394aad42e`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 94.8 KB (94828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c97d62051151c9b1528a1b64a558c48025170f167ba863808d5fb67d4c59006`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.23` - linux; ppc64le

```console
$ docker pull memcached@sha256:3a553e0d4ee19ee930775d8f8848969c6ff96b11e6b20f159ad754d11f5a8f8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6033619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfcda9c1811a9129ce53ed17b8ca116ffbaeebc21da0604c23b90e0dd042b0aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:33:21 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:33:22 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:35:40 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:35:40 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:35:40 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:35:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:35:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:35:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:35:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:35:41 GMT
USER memcache
# Wed, 28 Jan 2026 02:35:41 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:35:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c501a178d8bd3c1966eb75a7610efc35f292a3662f9fa7ca0d0089f54f723ce9`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac221803a5094f2d41563eece02e2e93293557ecb1eb5b7b646bcf143abcb82`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 126.3 KB (126255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d71af754023c45f69e3c70d3b4bfad1459328a7922268883ea41f2089ffe32ac`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 2.1 MB (2076366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c5df498426baf66bbc7701a67818ff6903c4420dc16591e79270ea8799caa35`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723a9c7624c2d00490e93ff507b003a4b495513fa6ec61b766c50bf5ccb8e23f`  
		Last Modified: Wed, 28 Jan 2026 02:35:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:238c5819c270bbc55c4140407b62939bf6ca158cb58cdbda8098f069301739a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9f43e248be2e248fe895fc3beccdf145fb06637800c6b89c19bf606d7c22975`

```dockerfile
```

-	Layers:
	-	`sha256:88da11471f4f95fd0f4679af21785a14ccb57b8bbd7fb96e4c42e1c49c333c33`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 94.3 KB (94280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b1fb2f254a022e51ca3dae9140daca46922a20d56b46607f22f1eef757d2fbb`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.23` - linux; riscv64

```console
$ docker pull memcached@sha256:8e9681abd0b8d92bb9145c49b7056cd27503f3420c10928ae606e4a65bdb9c9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5769974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:402a203724e613388d65f9de266b282381d864954d277c9552b24343915e9c40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 08:29:56 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 08:29:59 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 08:43:13 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 08:43:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 08:43:13 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 08:43:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 08:43:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 08:43:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 08:43:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 08:43:14 GMT
USER memcache
# Wed, 28 Jan 2026 08:43:14 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 08:43:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914e61f980ba6c54647d03d80091a261aae3ba7ab3d715251e992ea9407ad42e`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d963624519ed571edcf05aed3166ea5b7c1cd5fdae41a0d996d79be268f71e85`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 108.9 KB (108895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab35062ef9866f40cf3445147d50436a982e80d0ed984cca2f11d3ebcde5821`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 2.1 MB (2074437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82838004f4581bf0e6c37cecd3054aeb9fe5e1b92aeeb8cab2e86d9f9ed17af9`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b15a31cacc0f8dc4445667f3d0689a9857004aef390e2a16f7987db8124da4d7`  
		Last Modified: Wed, 28 Jan 2026 08:43:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:f15acc0a96b37da08e228c4fc099dbf28f370723c976c1a8a4d08679f5384799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c47e5bd1d37bec13b189586d46312efcb90ac656c7a80b9fd45fde1dd13f8e6e`

```dockerfile
```

-	Layers:
	-	`sha256:216d743a064cca1bd85c432678c24f3fa640798967115037f27c923138aa7af6`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 94.3 KB (94276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c38c6e624d8af51c7da79f4f214eb73cbfe3c2a2f9b465649a72b8dfa18429f`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.23` - linux; s390x

```console
$ docker pull memcached@sha256:f52690bd1266bfbe887fa9c03fc963f0277f331a85d8e81f4f134076c6d899f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5858103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7903f118ee1fcea4632b09ffbabd30b82ef4aa3b68dd3570b1173f263cacc343`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:21:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:21:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:24:07 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:24:07 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:24:07 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:24:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:24:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:24:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:24:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:24:08 GMT
USER memcache
# Wed, 28 Jan 2026 02:24:08 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:24:08 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030f843902eb7c01da3de08b6efb672d46d4f41e9e298640c66daabea5d901ef`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100608bf5f6494395c46670a28e6df9d705e08dc9129c1fb36b8f265fa52c22b`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 114.3 KB (114299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b706c73349baf76aabbef50d7dba3c89b85ffc84ad0aca5c544b1fe047706785`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 2.0 MB (2017124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce545f5bb33e4374e2e0bb9b11e751c89272699812f06c49e8e6a2e5ac3d524`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ac2e9e98ac3e799be9d54501be2f2304ef93065d34bef18f002ea38838ea24`  
		Last Modified: Wed, 28 Jan 2026 02:24:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:b4850489cf16ad5f72674b698ab0c2d16d95c6cc43e1b3f611f9fa67adcf4962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b79deed0597f9356a7dd99d34cb933d7634c520350fcabb9da14b254006070d0`

```dockerfile
```

-	Layers:
	-	`sha256:00a586e58a4b437f0260b3197ecff606cb3380869c6861c89d769a99132c10e9`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 94.2 KB (94222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8caeef6fbf9d37a3d092d84298ef02b53e2efff54347431fcc362c14dcdb9eb5`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:27 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b6e737e1a3eed198cc17e2b92231ab084bcf55ba90a36136e7a2f4fd04a95b`  
		Last Modified: Tue, 13 Jan 2026 01:25:25 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16835fec399670b74d32630a7368a65ca2a3c32d8b7a690d33bebc7b9e9458d`  
		Last Modified: Tue, 13 Jan 2026 01:25:24 GMT  
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
		Last Modified: Tue, 13 Jan 2026 01:25:25 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 27.9 MB (27942724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96776850dc1206c3fd163b84cea19599306159eb0d020b4241d0172240f88d13`  
		Last Modified: Tue, 13 Jan 2026 01:22:50 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3697c7c790d9c4caaa904abdaf809dcdee3f0b518fc5ad82d2e21dd7fe24f64d`  
		Last Modified: Tue, 13 Jan 2026 01:22:50 GMT  
		Size: 144.2 KB (144212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a247339c7ec57a491c3ffe43531dbfaa132f3ff16a481fc41cbb9e3e3ad6476`  
		Last Modified: Tue, 13 Jan 2026 01:22:50 GMT  
		Size: 2.2 MB (2210412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2dcebe3ab2a9945cdea142301e4a64eebbc59c948a54385dbfca4afd561b508`  
		Last Modified: Tue, 13 Jan 2026 01:22:50 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb8ef5ecbc44efd5280f9cf15687dfd80a34fa2966ad039238647177f75dc6c`  
		Last Modified: Tue, 13 Jan 2026 01:22:51 GMT  
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
		Last Modified: Tue, 13 Jan 2026 01:22:50 GMT  
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
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
		Size: 135.4 KB (135398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9371e974781bd91adc657086f00cd7d91b5530ca9da37597c347dd7d4eaff0`  
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
		Size: 2.2 MB (2164040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c2e0f64c0afa16b5e214ae208c8c81e8c78c79ddd90f54983a93c7297395f6b`  
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
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
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
		Size: 2.0 MB (2009750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e76d5584f581b7668c61a661da2858bc1d5e11b31e3629e0d2b3af52d9c22ed8`  
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:41 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78edb6b991369235f90958a936afc89dc37b82439c632988ed143b5bd76deadb`  
		Last Modified: Tue, 13 Jan 2026 01:25:33 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e1afbb765f6cc3923e864d44fb6cd6c9167b884e596b09bd37c7c276f65a2b`  
		Last Modified: Tue, 13 Jan 2026 01:25:33 GMT  
		Size: 153.5 KB (153512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff9edc68fe57c233001afd442eb6c248bf070d32fbb412a8bfeef6f9a6217f5`  
		Last Modified: Tue, 13 Jan 2026 01:25:33 GMT  
		Size: 2.3 MB (2261341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c4648fbc4a4189184946895d1041e0eee2c5d40fd70638a553bedb0cbf5cf8`  
		Last Modified: Tue, 13 Jan 2026 01:25:33 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26bd1b32b048e73091ddf6e6762e368d4bb6ef2cc7d3aa43467749b36fe08e38`  
		Last Modified: Tue, 13 Jan 2026 01:25:34 GMT  
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
		Last Modified: Tue, 13 Jan 2026 01:25:33 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:56 GMT  
		Size: 31.3 MB (31288476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cedb4f2840edea9de46e0d955a0512f469211880560a8948f10b54381bcd728`  
		Last Modified: Tue, 13 Jan 2026 01:22:46 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c4b2d1574ee5f238dc6948164abd39ffcc91929b2c464c6b3874dec01fd964`  
		Last Modified: Tue, 13 Jan 2026 01:22:46 GMT  
		Size: 147.6 KB (147554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc1bf5870b84175607f3d012b3cfebc5859869f8125114ea5d6ed1a05f81d2d`  
		Last Modified: Tue, 13 Jan 2026 01:22:46 GMT  
		Size: 2.2 MB (2223652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6434e73ed67e81f1016f27c7cc175290b0ce959d8a1bf5e9b0f3119f161246`  
		Last Modified: Tue, 13 Jan 2026 01:22:46 GMT  
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
		Last Modified: Tue, 13 Jan 2026 01:22:46 GMT  
		Size: 2.0 MB (2005447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6358862e12c5c5367efd52bea0b1194e04e76f267084da591229f64ee7482dc3`  
		Last Modified: Tue, 13 Jan 2026 01:22:46 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:57:06 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093e59deb53ff01a892be2a5df928c4b04a289df7f6c135570c11d6a4fdbc53a`  
		Last Modified: Tue, 13 Jan 2026 01:37:09 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4da25c8b13ee47050a38843c1954d2bd7bbdba2666f725aee2f603e03fcb6d`  
		Last Modified: Tue, 13 Jan 2026 01:37:09 GMT  
		Size: 170.4 KB (170427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cab5f6f805c735c0f324c87ff8c66cfab0e35fb691b7761e85bb9a2bbb31cfe`  
		Last Modified: Tue, 13 Jan 2026 01:37:09 GMT  
		Size: 2.4 MB (2393947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3a7dfc8da65bd6101de156530bc2688c5588c718bbc3131ff4594cbefd0e66`  
		Last Modified: Tue, 13 Jan 2026 01:37:09 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06153b2e2bde9b06f1c2719aabb5ff6a6c23056152a024fa2c990d97b4d9c799`  
		Last Modified: Tue, 13 Jan 2026 01:37:10 GMT  
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
		Last Modified: Tue, 13 Jan 2026 01:37:09 GMT  
		Size: 2.0 MB (2011891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc718b3aa0399c50248bba6165cad8666196a5351b6ed095a8101d2f8a5d37da`  
		Last Modified: Tue, 13 Jan 2026 01:37:09 GMT  
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
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168d1b37fe07dfb8bef5240057ad6597058647499a9e771eedd2091f2d6b30f0`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 133.1 KB (133105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a5ebc1ef49cab24f75e0c751a1e0563ee042c246c509279fa38cf3cbf0a3f1`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 2.2 MB (2207499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbc8df7ca1d2f273c3c8fec55b30f17ebc72a45687976efd9c8779a66369d46`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4057c9476d421ae1ecae3607afb0db57dbc6eb2bc0aa5e41daed169a70319c1`  
		Last Modified: Wed, 14 Jan 2026 06:50:29 GMT  
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
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 2.0 MB (2002254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0de5bd0cbff9df1fc11e05bd38936b6915195663b273b5c23840bf5eb9373a8`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
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
		Last Modified: Tue, 13 Jan 2026 13:10:27 GMT  
		Size: 29.8 MB (29833411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2727771ad16d920baecb7c96b9b54e67178369b881fc20901d381dfd5f873e27`  
		Last Modified: Tue, 13 Jan 2026 14:17:08 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6b0ec5581f8591522a6327cdcfa4e1197d9ada9fb60840f57b5d3e4dd3304d1`  
		Last Modified: Tue, 13 Jan 2026 14:17:08 GMT  
		Size: 140.6 KB (140562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382a3e1ebed70673a0789fcc2104ab941fe04b9a020339f9286ac85b67ae5ff9`  
		Last Modified: Tue, 13 Jan 2026 14:17:08 GMT  
		Size: 2.3 MB (2297368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85fe5f9afd355e3dd76ce942e1c295e356d96ae3b0e3f8236a0e33c5f75ffe71`  
		Last Modified: Tue, 13 Jan 2026 14:17:08 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4546f3c3457928dc273f98dae7c7ac2f945b203138e964ee72fc92aabcef434`  
		Last Modified: Tue, 13 Jan 2026 14:17:09 GMT  
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
		Last Modified: Tue, 13 Jan 2026 14:17:08 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:27 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b6e737e1a3eed198cc17e2b92231ab084bcf55ba90a36136e7a2f4fd04a95b`  
		Last Modified: Tue, 13 Jan 2026 01:25:25 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16835fec399670b74d32630a7368a65ca2a3c32d8b7a690d33bebc7b9e9458d`  
		Last Modified: Tue, 13 Jan 2026 01:25:24 GMT  
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
		Last Modified: Tue, 13 Jan 2026 01:25:25 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 27.9 MB (27942724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96776850dc1206c3fd163b84cea19599306159eb0d020b4241d0172240f88d13`  
		Last Modified: Tue, 13 Jan 2026 01:22:50 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3697c7c790d9c4caaa904abdaf809dcdee3f0b518fc5ad82d2e21dd7fe24f64d`  
		Last Modified: Tue, 13 Jan 2026 01:22:50 GMT  
		Size: 144.2 KB (144212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a247339c7ec57a491c3ffe43531dbfaa132f3ff16a481fc41cbb9e3e3ad6476`  
		Last Modified: Tue, 13 Jan 2026 01:22:50 GMT  
		Size: 2.2 MB (2210412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2dcebe3ab2a9945cdea142301e4a64eebbc59c948a54385dbfca4afd561b508`  
		Last Modified: Tue, 13 Jan 2026 01:22:50 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb8ef5ecbc44efd5280f9cf15687dfd80a34fa2966ad039238647177f75dc6c`  
		Last Modified: Tue, 13 Jan 2026 01:22:51 GMT  
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
		Last Modified: Tue, 13 Jan 2026 01:22:50 GMT  
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
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
		Size: 135.4 KB (135398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9371e974781bd91adc657086f00cd7d91b5530ca9da37597c347dd7d4eaff0`  
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
		Size: 2.2 MB (2164040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c2e0f64c0afa16b5e214ae208c8c81e8c78c79ddd90f54983a93c7297395f6b`  
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
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
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
		Size: 2.0 MB (2009750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e76d5584f581b7668c61a661da2858bc1d5e11b31e3629e0d2b3af52d9c22ed8`  
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:41 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78edb6b991369235f90958a936afc89dc37b82439c632988ed143b5bd76deadb`  
		Last Modified: Tue, 13 Jan 2026 01:25:33 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e1afbb765f6cc3923e864d44fb6cd6c9167b884e596b09bd37c7c276f65a2b`  
		Last Modified: Tue, 13 Jan 2026 01:25:33 GMT  
		Size: 153.5 KB (153512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff9edc68fe57c233001afd442eb6c248bf070d32fbb412a8bfeef6f9a6217f5`  
		Last Modified: Tue, 13 Jan 2026 01:25:33 GMT  
		Size: 2.3 MB (2261341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c4648fbc4a4189184946895d1041e0eee2c5d40fd70638a553bedb0cbf5cf8`  
		Last Modified: Tue, 13 Jan 2026 01:25:33 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26bd1b32b048e73091ddf6e6762e368d4bb6ef2cc7d3aa43467749b36fe08e38`  
		Last Modified: Tue, 13 Jan 2026 01:25:34 GMT  
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
		Last Modified: Tue, 13 Jan 2026 01:25:33 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:56 GMT  
		Size: 31.3 MB (31288476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cedb4f2840edea9de46e0d955a0512f469211880560a8948f10b54381bcd728`  
		Last Modified: Tue, 13 Jan 2026 01:22:46 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c4b2d1574ee5f238dc6948164abd39ffcc91929b2c464c6b3874dec01fd964`  
		Last Modified: Tue, 13 Jan 2026 01:22:46 GMT  
		Size: 147.6 KB (147554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc1bf5870b84175607f3d012b3cfebc5859869f8125114ea5d6ed1a05f81d2d`  
		Last Modified: Tue, 13 Jan 2026 01:22:46 GMT  
		Size: 2.2 MB (2223652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6434e73ed67e81f1016f27c7cc175290b0ce959d8a1bf5e9b0f3119f161246`  
		Last Modified: Tue, 13 Jan 2026 01:22:46 GMT  
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
		Last Modified: Tue, 13 Jan 2026 01:22:46 GMT  
		Size: 2.0 MB (2005447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6358862e12c5c5367efd52bea0b1194e04e76f267084da591229f64ee7482dc3`  
		Last Modified: Tue, 13 Jan 2026 01:22:46 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:57:06 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093e59deb53ff01a892be2a5df928c4b04a289df7f6c135570c11d6a4fdbc53a`  
		Last Modified: Tue, 13 Jan 2026 01:37:09 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4da25c8b13ee47050a38843c1954d2bd7bbdba2666f725aee2f603e03fcb6d`  
		Last Modified: Tue, 13 Jan 2026 01:37:09 GMT  
		Size: 170.4 KB (170427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cab5f6f805c735c0f324c87ff8c66cfab0e35fb691b7761e85bb9a2bbb31cfe`  
		Last Modified: Tue, 13 Jan 2026 01:37:09 GMT  
		Size: 2.4 MB (2393947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3a7dfc8da65bd6101de156530bc2688c5588c718bbc3131ff4594cbefd0e66`  
		Last Modified: Tue, 13 Jan 2026 01:37:09 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06153b2e2bde9b06f1c2719aabb5ff6a6c23056152a024fa2c990d97b4d9c799`  
		Last Modified: Tue, 13 Jan 2026 01:37:10 GMT  
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
		Last Modified: Tue, 13 Jan 2026 01:37:09 GMT  
		Size: 2.0 MB (2011891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc718b3aa0399c50248bba6165cad8666196a5351b6ed095a8101d2f8a5d37da`  
		Last Modified: Tue, 13 Jan 2026 01:37:09 GMT  
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
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168d1b37fe07dfb8bef5240057ad6597058647499a9e771eedd2091f2d6b30f0`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 133.1 KB (133105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a5ebc1ef49cab24f75e0c751a1e0563ee042c246c509279fa38cf3cbf0a3f1`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 2.2 MB (2207499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbc8df7ca1d2f273c3c8fec55b30f17ebc72a45687976efd9c8779a66369d46`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4057c9476d421ae1ecae3607afb0db57dbc6eb2bc0aa5e41daed169a70319c1`  
		Last Modified: Wed, 14 Jan 2026 06:50:29 GMT  
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
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 2.0 MB (2002254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0de5bd0cbff9df1fc11e05bd38936b6915195663b273b5c23840bf5eb9373a8`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
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
		Last Modified: Tue, 13 Jan 2026 13:10:27 GMT  
		Size: 29.8 MB (29833411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2727771ad16d920baecb7c96b9b54e67178369b881fc20901d381dfd5f873e27`  
		Last Modified: Tue, 13 Jan 2026 14:17:08 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6b0ec5581f8591522a6327cdcfa4e1197d9ada9fb60840f57b5d3e4dd3304d1`  
		Last Modified: Tue, 13 Jan 2026 14:17:08 GMT  
		Size: 140.6 KB (140562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382a3e1ebed70673a0789fcc2104ab941fe04b9a020339f9286ac85b67ae5ff9`  
		Last Modified: Tue, 13 Jan 2026 14:17:08 GMT  
		Size: 2.3 MB (2297368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85fe5f9afd355e3dd76ce942e1c295e356d96ae3b0e3f8236a0e33c5f75ffe71`  
		Last Modified: Tue, 13 Jan 2026 14:17:08 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4546f3c3457928dc273f98dae7c7ac2f945b203138e964ee72fc92aabcef434`  
		Last Modified: Tue, 13 Jan 2026 14:17:09 GMT  
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
		Last Modified: Tue, 13 Jan 2026 14:17:08 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.40-alpine`

```console
$ docker pull memcached@sha256:8a82a3927694e42bc52679dc81532244de51e5faed5f9541a1283e3ad7271db1
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
$ docker pull memcached@sha256:947366d40559340a4385b3e05f92186b9546e7feb59ef280e243ec8bf34f01a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5958530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7977390ffe9a7f3b6d3c5840f262b8058ca015d7daf5237e480d3f51a29e0b6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:18:28 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:18:29 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:21:03 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:21:03 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:21:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:21:03 GMT
USER memcache
# Wed, 28 Jan 2026 02:21:03 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:21:03 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e0ee508166c94a4f9ca8c32f743bd3733afb7660800042c7da03c2ea1da6b4`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15bf9562ecbc21cc4f52d1a4d33eb5eec98aa63c36c59f018b55071b8dd9f05f`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 106.1 KB (106059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24c6974a0da2f6cdd2022450be6195683245ba21f601d207ad14566c653ddea`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 2.0 MB (1989295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a859de0eb0253d066d7de73c90f4ebdc8b737fddab90420fd0ba6bd1c74669`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7be89a9ef60cc91d2346c9bc9a975138908bbc03aa40c948ab5e7336aa8e8b`  
		Last Modified: Wed, 28 Jan 2026 02:21:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7579a20056cd9531e754a57f957da811356775f676bfa6cd6e86b95f6de172d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8408948e08375e96299e735072f97a85aca5d58f65fc7cca125dfe5389160cb`

```dockerfile
```

-	Layers:
	-	`sha256:533c466de2027803aea398674e5a5ffd7d67b9e1eddc4228741a130ff830b02a`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 94.9 KB (94873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27c54b10e342535e2af7655af306fbf617d3dbf0922a7dd440f8ed4ea3e1fd5c`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:3a1e785feba037614143f75204bac3225d838127c68805b29ff23df9d8638070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c891a4120404380161eeeddd4e7c7cb748eb55193453c6e9090a59909bf1969`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 06:07:09 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 06:07:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 06:19:29 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 06:19:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 06:19:29 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 06:19:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 06:19:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 06:19:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 06:19:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 06:19:29 GMT
USER memcache
# Wed, 28 Jan 2026 06:19:29 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 06:19:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9dfe3bd7930f213b1f0f6c2854f26637f5a52c7cd4796e9eb59071fe2ff4b2f`  
		Last Modified: Wed, 28 Jan 2026 06:19:33 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:707447698613ddcfad121290546b5d9e04e2c3194b8f59394a272fe30f42dba1`  
		Last Modified: Wed, 28 Jan 2026 06:19:33 GMT  
		Size: 102.6 KB (102646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d366a66d67c4233b2ac1bc38363cb9881e63ca3af7f82ebbffbfb76942e1a34`  
		Last Modified: Wed, 28 Jan 2026 06:19:34 GMT  
		Size: 1.9 MB (1939230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e5326e5c6353c918ea1ac99aedfb19f688830f93037e66268b39c31f670e01`  
		Last Modified: Wed, 28 Jan 2026 06:19:33 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2ead2e4800bd6e32bbdb6225ecb70b554d33b3c17f3e8b973890f3b3c532da`  
		Last Modified: Wed, 28 Jan 2026 06:19:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:fd7fcbdf0e7f96a083f3d6aec29c9d21ac4b768be5949f68958c25756c153f95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07888c8ad7065e17bfea11af8f4f20b5f956ab1b553160f5ea4a484c4e437674`

```dockerfile
```

-	Layers:
	-	`sha256:aed006a02d773c56c072711ddc729af9ce5001ab757071fc3abdc5094822e7c7`  
		Last Modified: Wed, 28 Jan 2026 06:19:34 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:f08c7e3ff92e718b22bc7b21385421ebcf4bf6f542b797690d6547506821ab35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5272638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a6fc0ce35a3d59414018d4d8fe69929016a9e8dc7dc27daaafc617e3a7165d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:22:45 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:22:46 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:25:41 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:25:41 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:25:41 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:25:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:25:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:25:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:25:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:25:41 GMT
USER memcache
# Wed, 28 Jan 2026 02:25:41 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:25:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f61af882efa215dd577f7a17129442647756c535df9c13e821da864cddcf0e6`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b88f23b7692bcb2301e4e0a862af10c70c6ec663fca9e0a3389a74a3ba0520e`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 92.4 KB (92374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0549b4be8a16d49c33d6adaf28e4f8f7acbdea009dec2daed172741f7540ce5a`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 1.9 MB (1897188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6760f49ea55e45e14e26aaaf690948c109a5d85256175c84bbd06beccc8cd1`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9fca934ad2088c9a34e9f20e65d902054dfb9accdb4c6865924dd1fa88685b`  
		Last Modified: Wed, 28 Jan 2026 02:25:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:b5c2e8ac0b1fd0bd9c534bf163bad10efc0dc2c3afdfb66e3eb1a827d7bbfc87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dd20e2507c3ff3732182e3d2d44e5f7bc9b449bb172d5c7895b2fcc2dd423c6`

```dockerfile
```

-	Layers:
	-	`sha256:36627c0161ebd5c055e99a596a600017e5608e5895d1f95159116ff2df2eb3a6`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 94.3 KB (94291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a5914862f1fb65973ac0def541c9da056e1a5ef0bb26623a5bbad81803a4383`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:1a4aa193f53b5a4e2d82f6c67c23e87ef5d3d1cd1ddf96e0aabe73d49e537c2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6286893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f275b1c508af04216ccc891e9de0d7cbb35441f4eb424197e529ddbfb1d1b62`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:18:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:18:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:20:58 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:20:58 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:20:58 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:20:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:20:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:20:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:20:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:20:59 GMT
USER memcache
# Wed, 28 Jan 2026 02:20:59 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:20:59 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42047232a88cba1fc4d173d71bdf04395f6e4b83472de9f225ae2dd70ce14bc`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b625b9113e283efad9a0ee8e305f08edfd38a6c015224459a1ec0f2f49a0b915`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 121.8 KB (121845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf057b1d31677325905e009d68a97c3741028480d8b254105b145f39d157f2a`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 2.0 MB (1966604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db407fe2bd85342d8cb160bd73b5efe730723df2d20f2f6021eef8ad2d8f16eb`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfefb839a309e8b3df7a659236c09776f4eff9f8a47d9b331f131d9ad4c5d6b`  
		Last Modified: Wed, 28 Jan 2026 02:21:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:28b857747dd2742dbf00b9c1fc07265248073390d37bacf6cf8bfd313cf52a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f34aaccc9ca109270d86cdb6e46e56b207775ad700dadb1604f0a56b3ed4536e`

```dockerfile
```

-	Layers:
	-	`sha256:53b8cb56ae6a2b4c94fae4924dc03d881acba2e6c746fdb05808f3a86186ceff`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 94.3 KB (94327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03361fd0b86b6e905c14afa88e91f00f54a7e68e1d12d191b3d65c41986adc2e`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 20.7 KB (20728 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-alpine` - linux; 386

```console
$ docker pull memcached@sha256:8c10f776d94f57c5e0a4807247add0a2f3638eaafc3f6571b66ac325cc251866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5741838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f2329492e766d962366bfa352f931d82d7cd74d9e771ae6db7d44c1345197b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:16:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:16:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:18:59 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:18:59 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:18:59 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:18:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:18:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:18:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:18:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:18:59 GMT
USER memcache
# Wed, 28 Jan 2026 02:18:59 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:18:59 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbdb7a800485646296958fbca0c9cfdd5c397a0dbc2e33f1bc0c55dfca3c47a6`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7651295f62c54da7297c4ef646e146ef0acac3f551fb8a3dccc49190efced234`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 110.7 KB (110722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87d7b2cf89ac568b76f6e27208734340c49f4d7b0fedb8e5ae16f54a0cadc43`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 1.9 MB (1942772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4f82eada80af7ef4ec5dfcb36c5a93fa36157801318f374c5ab0d0987cd352`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61a034237824e579d4d24c5ec4b58ee8c400255488e658c36064d43c0001301`  
		Last Modified: Wed, 28 Jan 2026 02:19:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:118dd83c690f154abc02b708a01a0a0a48519b7faa920e5540ebf81c8e626429
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a7e54c817c006a1a17af2f06a4b3e4d1816cb0051c626c3f5e18a5012224b2`

```dockerfile
```

-	Layers:
	-	`sha256:11c94853238efef3a0c48e7cc56222e34874215e568475cfb20d3f2394aad42e`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 94.8 KB (94828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c97d62051151c9b1528a1b64a558c48025170f167ba863808d5fb67d4c59006`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:3a553e0d4ee19ee930775d8f8848969c6ff96b11e6b20f159ad754d11f5a8f8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6033619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfcda9c1811a9129ce53ed17b8ca116ffbaeebc21da0604c23b90e0dd042b0aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:33:21 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:33:22 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:35:40 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:35:40 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:35:40 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:35:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:35:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:35:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:35:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:35:41 GMT
USER memcache
# Wed, 28 Jan 2026 02:35:41 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:35:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c501a178d8bd3c1966eb75a7610efc35f292a3662f9fa7ca0d0089f54f723ce9`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac221803a5094f2d41563eece02e2e93293557ecb1eb5b7b646bcf143abcb82`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 126.3 KB (126255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d71af754023c45f69e3c70d3b4bfad1459328a7922268883ea41f2089ffe32ac`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 2.1 MB (2076366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c5df498426baf66bbc7701a67818ff6903c4420dc16591e79270ea8799caa35`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723a9c7624c2d00490e93ff507b003a4b495513fa6ec61b766c50bf5ccb8e23f`  
		Last Modified: Wed, 28 Jan 2026 02:35:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:238c5819c270bbc55c4140407b62939bf6ca158cb58cdbda8098f069301739a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9f43e248be2e248fe895fc3beccdf145fb06637800c6b89c19bf606d7c22975`

```dockerfile
```

-	Layers:
	-	`sha256:88da11471f4f95fd0f4679af21785a14ccb57b8bbd7fb96e4c42e1c49c333c33`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 94.3 KB (94280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b1fb2f254a022e51ca3dae9140daca46922a20d56b46607f22f1eef757d2fbb`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:8e9681abd0b8d92bb9145c49b7056cd27503f3420c10928ae606e4a65bdb9c9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5769974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:402a203724e613388d65f9de266b282381d864954d277c9552b24343915e9c40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 08:29:56 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 08:29:59 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 08:43:13 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 08:43:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 08:43:13 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 08:43:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 08:43:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 08:43:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 08:43:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 08:43:14 GMT
USER memcache
# Wed, 28 Jan 2026 08:43:14 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 08:43:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914e61f980ba6c54647d03d80091a261aae3ba7ab3d715251e992ea9407ad42e`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d963624519ed571edcf05aed3166ea5b7c1cd5fdae41a0d996d79be268f71e85`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 108.9 KB (108895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab35062ef9866f40cf3445147d50436a982e80d0ed984cca2f11d3ebcde5821`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 2.1 MB (2074437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82838004f4581bf0e6c37cecd3054aeb9fe5e1b92aeeb8cab2e86d9f9ed17af9`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b15a31cacc0f8dc4445667f3d0689a9857004aef390e2a16f7987db8124da4d7`  
		Last Modified: Wed, 28 Jan 2026 08:43:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:f15acc0a96b37da08e228c4fc099dbf28f370723c976c1a8a4d08679f5384799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c47e5bd1d37bec13b189586d46312efcb90ac656c7a80b9fd45fde1dd13f8e6e`

```dockerfile
```

-	Layers:
	-	`sha256:216d743a064cca1bd85c432678c24f3fa640798967115037f27c923138aa7af6`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 94.3 KB (94276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c38c6e624d8af51c7da79f4f214eb73cbfe3c2a2f9b465649a72b8dfa18429f`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:f52690bd1266bfbe887fa9c03fc963f0277f331a85d8e81f4f134076c6d899f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5858103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7903f118ee1fcea4632b09ffbabd30b82ef4aa3b68dd3570b1173f263cacc343`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:21:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:21:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:24:07 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:24:07 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:24:07 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:24:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:24:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:24:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:24:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:24:08 GMT
USER memcache
# Wed, 28 Jan 2026 02:24:08 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:24:08 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030f843902eb7c01da3de08b6efb672d46d4f41e9e298640c66daabea5d901ef`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100608bf5f6494395c46670a28e6df9d705e08dc9129c1fb36b8f265fa52c22b`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 114.3 KB (114299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b706c73349baf76aabbef50d7dba3c89b85ffc84ad0aca5c544b1fe047706785`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 2.0 MB (2017124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce545f5bb33e4374e2e0bb9b11e751c89272699812f06c49e8e6a2e5ac3d524`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ac2e9e98ac3e799be9d54501be2f2304ef93065d34bef18f002ea38838ea24`  
		Last Modified: Wed, 28 Jan 2026 02:24:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:b4850489cf16ad5f72674b698ab0c2d16d95c6cc43e1b3f611f9fa67adcf4962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b79deed0597f9356a7dd99d34cb933d7634c520350fcabb9da14b254006070d0`

```dockerfile
```

-	Layers:
	-	`sha256:00a586e58a4b437f0260b3197ecff606cb3380869c6861c89d769a99132c10e9`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 94.2 KB (94222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8caeef6fbf9d37a3d092d84298ef02b53e2efff54347431fcc362c14dcdb9eb5`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.40-alpine3.23`

```console
$ docker pull memcached@sha256:8a82a3927694e42bc52679dc81532244de51e5faed5f9541a1283e3ad7271db1
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
$ docker pull memcached@sha256:947366d40559340a4385b3e05f92186b9546e7feb59ef280e243ec8bf34f01a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5958530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7977390ffe9a7f3b6d3c5840f262b8058ca015d7daf5237e480d3f51a29e0b6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:18:28 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:18:29 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:21:03 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:21:03 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:21:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:21:03 GMT
USER memcache
# Wed, 28 Jan 2026 02:21:03 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:21:03 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e0ee508166c94a4f9ca8c32f743bd3733afb7660800042c7da03c2ea1da6b4`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15bf9562ecbc21cc4f52d1a4d33eb5eec98aa63c36c59f018b55071b8dd9f05f`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 106.1 KB (106059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24c6974a0da2f6cdd2022450be6195683245ba21f601d207ad14566c653ddea`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 2.0 MB (1989295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a859de0eb0253d066d7de73c90f4ebdc8b737fddab90420fd0ba6bd1c74669`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7be89a9ef60cc91d2346c9bc9a975138908bbc03aa40c948ab5e7336aa8e8b`  
		Last Modified: Wed, 28 Jan 2026 02:21:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:7579a20056cd9531e754a57f957da811356775f676bfa6cd6e86b95f6de172d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8408948e08375e96299e735072f97a85aca5d58f65fc7cca125dfe5389160cb`

```dockerfile
```

-	Layers:
	-	`sha256:533c466de2027803aea398674e5a5ffd7d67b9e1eddc4228741a130ff830b02a`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 94.9 KB (94873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27c54b10e342535e2af7655af306fbf617d3dbf0922a7dd440f8ed4ea3e1fd5c`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-alpine3.23` - linux; arm variant v6

```console
$ docker pull memcached@sha256:3a1e785feba037614143f75204bac3225d838127c68805b29ff23df9d8638070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c891a4120404380161eeeddd4e7c7cb748eb55193453c6e9090a59909bf1969`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 06:07:09 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 06:07:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 06:19:29 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 06:19:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 06:19:29 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 06:19:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 06:19:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 06:19:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 06:19:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 06:19:29 GMT
USER memcache
# Wed, 28 Jan 2026 06:19:29 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 06:19:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9dfe3bd7930f213b1f0f6c2854f26637f5a52c7cd4796e9eb59071fe2ff4b2f`  
		Last Modified: Wed, 28 Jan 2026 06:19:33 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:707447698613ddcfad121290546b5d9e04e2c3194b8f59394a272fe30f42dba1`  
		Last Modified: Wed, 28 Jan 2026 06:19:33 GMT  
		Size: 102.6 KB (102646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d366a66d67c4233b2ac1bc38363cb9881e63ca3af7f82ebbffbfb76942e1a34`  
		Last Modified: Wed, 28 Jan 2026 06:19:34 GMT  
		Size: 1.9 MB (1939230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e5326e5c6353c918ea1ac99aedfb19f688830f93037e66268b39c31f670e01`  
		Last Modified: Wed, 28 Jan 2026 06:19:33 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2ead2e4800bd6e32bbdb6225ecb70b554d33b3c17f3e8b973890f3b3c532da`  
		Last Modified: Wed, 28 Jan 2026 06:19:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:fd7fcbdf0e7f96a083f3d6aec29c9d21ac4b768be5949f68958c25756c153f95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07888c8ad7065e17bfea11af8f4f20b5f956ab1b553160f5ea4a484c4e437674`

```dockerfile
```

-	Layers:
	-	`sha256:aed006a02d773c56c072711ddc729af9ce5001ab757071fc3abdc5094822e7c7`  
		Last Modified: Wed, 28 Jan 2026 06:19:34 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-alpine3.23` - linux; arm variant v7

```console
$ docker pull memcached@sha256:f08c7e3ff92e718b22bc7b21385421ebcf4bf6f542b797690d6547506821ab35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5272638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a6fc0ce35a3d59414018d4d8fe69929016a9e8dc7dc27daaafc617e3a7165d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:22:45 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:22:46 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:25:41 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:25:41 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:25:41 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:25:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:25:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:25:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:25:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:25:41 GMT
USER memcache
# Wed, 28 Jan 2026 02:25:41 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:25:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f61af882efa215dd577f7a17129442647756c535df9c13e821da864cddcf0e6`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b88f23b7692bcb2301e4e0a862af10c70c6ec663fca9e0a3389a74a3ba0520e`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 92.4 KB (92374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0549b4be8a16d49c33d6adaf28e4f8f7acbdea009dec2daed172741f7540ce5a`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 1.9 MB (1897188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6760f49ea55e45e14e26aaaf690948c109a5d85256175c84bbd06beccc8cd1`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9fca934ad2088c9a34e9f20e65d902054dfb9accdb4c6865924dd1fa88685b`  
		Last Modified: Wed, 28 Jan 2026 02:25:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:b5c2e8ac0b1fd0bd9c534bf163bad10efc0dc2c3afdfb66e3eb1a827d7bbfc87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dd20e2507c3ff3732182e3d2d44e5f7bc9b449bb172d5c7895b2fcc2dd423c6`

```dockerfile
```

-	Layers:
	-	`sha256:36627c0161ebd5c055e99a596a600017e5608e5895d1f95159116ff2df2eb3a6`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 94.3 KB (94291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a5914862f1fb65973ac0def541c9da056e1a5ef0bb26623a5bbad81803a4383`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:1a4aa193f53b5a4e2d82f6c67c23e87ef5d3d1cd1ddf96e0aabe73d49e537c2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6286893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f275b1c508af04216ccc891e9de0d7cbb35441f4eb424197e529ddbfb1d1b62`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:18:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:18:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:20:58 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:20:58 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:20:58 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:20:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:20:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:20:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:20:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:20:59 GMT
USER memcache
# Wed, 28 Jan 2026 02:20:59 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:20:59 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42047232a88cba1fc4d173d71bdf04395f6e4b83472de9f225ae2dd70ce14bc`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b625b9113e283efad9a0ee8e305f08edfd38a6c015224459a1ec0f2f49a0b915`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 121.8 KB (121845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf057b1d31677325905e009d68a97c3741028480d8b254105b145f39d157f2a`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 2.0 MB (1966604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db407fe2bd85342d8cb160bd73b5efe730723df2d20f2f6021eef8ad2d8f16eb`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfefb839a309e8b3df7a659236c09776f4eff9f8a47d9b331f131d9ad4c5d6b`  
		Last Modified: Wed, 28 Jan 2026 02:21:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:28b857747dd2742dbf00b9c1fc07265248073390d37bacf6cf8bfd313cf52a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f34aaccc9ca109270d86cdb6e46e56b207775ad700dadb1604f0a56b3ed4536e`

```dockerfile
```

-	Layers:
	-	`sha256:53b8cb56ae6a2b4c94fae4924dc03d881acba2e6c746fdb05808f3a86186ceff`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 94.3 KB (94327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03361fd0b86b6e905c14afa88e91f00f54a7e68e1d12d191b3d65c41986adc2e`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 20.7 KB (20728 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-alpine3.23` - linux; 386

```console
$ docker pull memcached@sha256:8c10f776d94f57c5e0a4807247add0a2f3638eaafc3f6571b66ac325cc251866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5741838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f2329492e766d962366bfa352f931d82d7cd74d9e771ae6db7d44c1345197b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:16:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:16:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:18:59 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:18:59 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:18:59 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:18:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:18:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:18:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:18:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:18:59 GMT
USER memcache
# Wed, 28 Jan 2026 02:18:59 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:18:59 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbdb7a800485646296958fbca0c9cfdd5c397a0dbc2e33f1bc0c55dfca3c47a6`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7651295f62c54da7297c4ef646e146ef0acac3f551fb8a3dccc49190efced234`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 110.7 KB (110722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87d7b2cf89ac568b76f6e27208734340c49f4d7b0fedb8e5ae16f54a0cadc43`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 1.9 MB (1942772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4f82eada80af7ef4ec5dfcb36c5a93fa36157801318f374c5ab0d0987cd352`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61a034237824e579d4d24c5ec4b58ee8c400255488e658c36064d43c0001301`  
		Last Modified: Wed, 28 Jan 2026 02:19:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:118dd83c690f154abc02b708a01a0a0a48519b7faa920e5540ebf81c8e626429
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a7e54c817c006a1a17af2f06a4b3e4d1816cb0051c626c3f5e18a5012224b2`

```dockerfile
```

-	Layers:
	-	`sha256:11c94853238efef3a0c48e7cc56222e34874215e568475cfb20d3f2394aad42e`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 94.8 KB (94828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c97d62051151c9b1528a1b64a558c48025170f167ba863808d5fb67d4c59006`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-alpine3.23` - linux; ppc64le

```console
$ docker pull memcached@sha256:3a553e0d4ee19ee930775d8f8848969c6ff96b11e6b20f159ad754d11f5a8f8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6033619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfcda9c1811a9129ce53ed17b8ca116ffbaeebc21da0604c23b90e0dd042b0aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:33:21 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:33:22 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:35:40 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:35:40 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:35:40 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:35:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:35:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:35:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:35:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:35:41 GMT
USER memcache
# Wed, 28 Jan 2026 02:35:41 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:35:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c501a178d8bd3c1966eb75a7610efc35f292a3662f9fa7ca0d0089f54f723ce9`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac221803a5094f2d41563eece02e2e93293557ecb1eb5b7b646bcf143abcb82`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 126.3 KB (126255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d71af754023c45f69e3c70d3b4bfad1459328a7922268883ea41f2089ffe32ac`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 2.1 MB (2076366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c5df498426baf66bbc7701a67818ff6903c4420dc16591e79270ea8799caa35`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723a9c7624c2d00490e93ff507b003a4b495513fa6ec61b766c50bf5ccb8e23f`  
		Last Modified: Wed, 28 Jan 2026 02:35:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:238c5819c270bbc55c4140407b62939bf6ca158cb58cdbda8098f069301739a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9f43e248be2e248fe895fc3beccdf145fb06637800c6b89c19bf606d7c22975`

```dockerfile
```

-	Layers:
	-	`sha256:88da11471f4f95fd0f4679af21785a14ccb57b8bbd7fb96e4c42e1c49c333c33`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 94.3 KB (94280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b1fb2f254a022e51ca3dae9140daca46922a20d56b46607f22f1eef757d2fbb`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-alpine3.23` - linux; riscv64

```console
$ docker pull memcached@sha256:8e9681abd0b8d92bb9145c49b7056cd27503f3420c10928ae606e4a65bdb9c9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5769974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:402a203724e613388d65f9de266b282381d864954d277c9552b24343915e9c40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 08:29:56 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 08:29:59 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 08:43:13 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 08:43:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 08:43:13 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 08:43:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 08:43:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 08:43:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 08:43:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 08:43:14 GMT
USER memcache
# Wed, 28 Jan 2026 08:43:14 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 08:43:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914e61f980ba6c54647d03d80091a261aae3ba7ab3d715251e992ea9407ad42e`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d963624519ed571edcf05aed3166ea5b7c1cd5fdae41a0d996d79be268f71e85`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 108.9 KB (108895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab35062ef9866f40cf3445147d50436a982e80d0ed984cca2f11d3ebcde5821`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 2.1 MB (2074437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82838004f4581bf0e6c37cecd3054aeb9fe5e1b92aeeb8cab2e86d9f9ed17af9`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b15a31cacc0f8dc4445667f3d0689a9857004aef390e2a16f7987db8124da4d7`  
		Last Modified: Wed, 28 Jan 2026 08:43:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:f15acc0a96b37da08e228c4fc099dbf28f370723c976c1a8a4d08679f5384799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c47e5bd1d37bec13b189586d46312efcb90ac656c7a80b9fd45fde1dd13f8e6e`

```dockerfile
```

-	Layers:
	-	`sha256:216d743a064cca1bd85c432678c24f3fa640798967115037f27c923138aa7af6`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 94.3 KB (94276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c38c6e624d8af51c7da79f4f214eb73cbfe3c2a2f9b465649a72b8dfa18429f`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-alpine3.23` - linux; s390x

```console
$ docker pull memcached@sha256:f52690bd1266bfbe887fa9c03fc963f0277f331a85d8e81f4f134076c6d899f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5858103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7903f118ee1fcea4632b09ffbabd30b82ef4aa3b68dd3570b1173f263cacc343`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:21:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:21:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:24:07 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:24:07 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:24:07 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:24:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:24:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:24:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:24:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:24:08 GMT
USER memcache
# Wed, 28 Jan 2026 02:24:08 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:24:08 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030f843902eb7c01da3de08b6efb672d46d4f41e9e298640c66daabea5d901ef`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100608bf5f6494395c46670a28e6df9d705e08dc9129c1fb36b8f265fa52c22b`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 114.3 KB (114299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b706c73349baf76aabbef50d7dba3c89b85ffc84ad0aca5c544b1fe047706785`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 2.0 MB (2017124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce545f5bb33e4374e2e0bb9b11e751c89272699812f06c49e8e6a2e5ac3d524`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ac2e9e98ac3e799be9d54501be2f2304ef93065d34bef18f002ea38838ea24`  
		Last Modified: Wed, 28 Jan 2026 02:24:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:b4850489cf16ad5f72674b698ab0c2d16d95c6cc43e1b3f611f9fa67adcf4962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b79deed0597f9356a7dd99d34cb933d7634c520350fcabb9da14b254006070d0`

```dockerfile
```

-	Layers:
	-	`sha256:00a586e58a4b437f0260b3197ecff606cb3380869c6861c89d769a99132c10e9`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 94.2 KB (94222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8caeef6fbf9d37a3d092d84298ef02b53e2efff54347431fcc362c14dcdb9eb5`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:27 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b6e737e1a3eed198cc17e2b92231ab084bcf55ba90a36136e7a2f4fd04a95b`  
		Last Modified: Tue, 13 Jan 2026 01:25:25 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16835fec399670b74d32630a7368a65ca2a3c32d8b7a690d33bebc7b9e9458d`  
		Last Modified: Tue, 13 Jan 2026 01:25:24 GMT  
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
		Last Modified: Tue, 13 Jan 2026 01:25:25 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 27.9 MB (27942724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96776850dc1206c3fd163b84cea19599306159eb0d020b4241d0172240f88d13`  
		Last Modified: Tue, 13 Jan 2026 01:22:50 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3697c7c790d9c4caaa904abdaf809dcdee3f0b518fc5ad82d2e21dd7fe24f64d`  
		Last Modified: Tue, 13 Jan 2026 01:22:50 GMT  
		Size: 144.2 KB (144212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a247339c7ec57a491c3ffe43531dbfaa132f3ff16a481fc41cbb9e3e3ad6476`  
		Last Modified: Tue, 13 Jan 2026 01:22:50 GMT  
		Size: 2.2 MB (2210412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2dcebe3ab2a9945cdea142301e4a64eebbc59c948a54385dbfca4afd561b508`  
		Last Modified: Tue, 13 Jan 2026 01:22:50 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb8ef5ecbc44efd5280f9cf15687dfd80a34fa2966ad039238647177f75dc6c`  
		Last Modified: Tue, 13 Jan 2026 01:22:51 GMT  
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
		Last Modified: Tue, 13 Jan 2026 01:22:50 GMT  
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
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
		Size: 135.4 KB (135398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9371e974781bd91adc657086f00cd7d91b5530ca9da37597c347dd7d4eaff0`  
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
		Size: 2.2 MB (2164040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c2e0f64c0afa16b5e214ae208c8c81e8c78c79ddd90f54983a93c7297395f6b`  
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
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
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
		Size: 2.0 MB (2009750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e76d5584f581b7668c61a661da2858bc1d5e11b31e3629e0d2b3af52d9c22ed8`  
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:41 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78edb6b991369235f90958a936afc89dc37b82439c632988ed143b5bd76deadb`  
		Last Modified: Tue, 13 Jan 2026 01:25:33 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e1afbb765f6cc3923e864d44fb6cd6c9167b884e596b09bd37c7c276f65a2b`  
		Last Modified: Tue, 13 Jan 2026 01:25:33 GMT  
		Size: 153.5 KB (153512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff9edc68fe57c233001afd442eb6c248bf070d32fbb412a8bfeef6f9a6217f5`  
		Last Modified: Tue, 13 Jan 2026 01:25:33 GMT  
		Size: 2.3 MB (2261341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c4648fbc4a4189184946895d1041e0eee2c5d40fd70638a553bedb0cbf5cf8`  
		Last Modified: Tue, 13 Jan 2026 01:25:33 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26bd1b32b048e73091ddf6e6762e368d4bb6ef2cc7d3aa43467749b36fe08e38`  
		Last Modified: Tue, 13 Jan 2026 01:25:34 GMT  
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
		Last Modified: Tue, 13 Jan 2026 01:25:33 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:56 GMT  
		Size: 31.3 MB (31288476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cedb4f2840edea9de46e0d955a0512f469211880560a8948f10b54381bcd728`  
		Last Modified: Tue, 13 Jan 2026 01:22:46 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c4b2d1574ee5f238dc6948164abd39ffcc91929b2c464c6b3874dec01fd964`  
		Last Modified: Tue, 13 Jan 2026 01:22:46 GMT  
		Size: 147.6 KB (147554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc1bf5870b84175607f3d012b3cfebc5859869f8125114ea5d6ed1a05f81d2d`  
		Last Modified: Tue, 13 Jan 2026 01:22:46 GMT  
		Size: 2.2 MB (2223652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6434e73ed67e81f1016f27c7cc175290b0ce959d8a1bf5e9b0f3119f161246`  
		Last Modified: Tue, 13 Jan 2026 01:22:46 GMT  
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
		Last Modified: Tue, 13 Jan 2026 01:22:46 GMT  
		Size: 2.0 MB (2005447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6358862e12c5c5367efd52bea0b1194e04e76f267084da591229f64ee7482dc3`  
		Last Modified: Tue, 13 Jan 2026 01:22:46 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:57:06 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093e59deb53ff01a892be2a5df928c4b04a289df7f6c135570c11d6a4fdbc53a`  
		Last Modified: Tue, 13 Jan 2026 01:37:09 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4da25c8b13ee47050a38843c1954d2bd7bbdba2666f725aee2f603e03fcb6d`  
		Last Modified: Tue, 13 Jan 2026 01:37:09 GMT  
		Size: 170.4 KB (170427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cab5f6f805c735c0f324c87ff8c66cfab0e35fb691b7761e85bb9a2bbb31cfe`  
		Last Modified: Tue, 13 Jan 2026 01:37:09 GMT  
		Size: 2.4 MB (2393947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3a7dfc8da65bd6101de156530bc2688c5588c718bbc3131ff4594cbefd0e66`  
		Last Modified: Tue, 13 Jan 2026 01:37:09 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06153b2e2bde9b06f1c2719aabb5ff6a6c23056152a024fa2c990d97b4d9c799`  
		Last Modified: Tue, 13 Jan 2026 01:37:10 GMT  
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
		Last Modified: Tue, 13 Jan 2026 01:37:09 GMT  
		Size: 2.0 MB (2011891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc718b3aa0399c50248bba6165cad8666196a5351b6ed095a8101d2f8a5d37da`  
		Last Modified: Tue, 13 Jan 2026 01:37:09 GMT  
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
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168d1b37fe07dfb8bef5240057ad6597058647499a9e771eedd2091f2d6b30f0`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 133.1 KB (133105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a5ebc1ef49cab24f75e0c751a1e0563ee042c246c509279fa38cf3cbf0a3f1`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 2.2 MB (2207499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbc8df7ca1d2f273c3c8fec55b30f17ebc72a45687976efd9c8779a66369d46`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4057c9476d421ae1ecae3607afb0db57dbc6eb2bc0aa5e41daed169a70319c1`  
		Last Modified: Wed, 14 Jan 2026 06:50:29 GMT  
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
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 2.0 MB (2002254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0de5bd0cbff9df1fc11e05bd38936b6915195663b273b5c23840bf5eb9373a8`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
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
		Last Modified: Tue, 13 Jan 2026 13:10:27 GMT  
		Size: 29.8 MB (29833411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2727771ad16d920baecb7c96b9b54e67178369b881fc20901d381dfd5f873e27`  
		Last Modified: Tue, 13 Jan 2026 14:17:08 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6b0ec5581f8591522a6327cdcfa4e1197d9ada9fb60840f57b5d3e4dd3304d1`  
		Last Modified: Tue, 13 Jan 2026 14:17:08 GMT  
		Size: 140.6 KB (140562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382a3e1ebed70673a0789fcc2104ab941fe04b9a020339f9286ac85b67ae5ff9`  
		Last Modified: Tue, 13 Jan 2026 14:17:08 GMT  
		Size: 2.3 MB (2297368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85fe5f9afd355e3dd76ce942e1c295e356d96ae3b0e3f8236a0e33c5f75ffe71`  
		Last Modified: Tue, 13 Jan 2026 14:17:08 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4546f3c3457928dc273f98dae7c7ac2f945b203138e964ee72fc92aabcef434`  
		Last Modified: Tue, 13 Jan 2026 14:17:09 GMT  
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
		Last Modified: Tue, 13 Jan 2026 14:17:08 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine`

```console
$ docker pull memcached@sha256:8a82a3927694e42bc52679dc81532244de51e5faed5f9541a1283e3ad7271db1
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
$ docker pull memcached@sha256:947366d40559340a4385b3e05f92186b9546e7feb59ef280e243ec8bf34f01a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5958530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7977390ffe9a7f3b6d3c5840f262b8058ca015d7daf5237e480d3f51a29e0b6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:18:28 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:18:29 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:21:03 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:21:03 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:21:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:21:03 GMT
USER memcache
# Wed, 28 Jan 2026 02:21:03 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:21:03 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e0ee508166c94a4f9ca8c32f743bd3733afb7660800042c7da03c2ea1da6b4`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15bf9562ecbc21cc4f52d1a4d33eb5eec98aa63c36c59f018b55071b8dd9f05f`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 106.1 KB (106059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24c6974a0da2f6cdd2022450be6195683245ba21f601d207ad14566c653ddea`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 2.0 MB (1989295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a859de0eb0253d066d7de73c90f4ebdc8b737fddab90420fd0ba6bd1c74669`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7be89a9ef60cc91d2346c9bc9a975138908bbc03aa40c948ab5e7336aa8e8b`  
		Last Modified: Wed, 28 Jan 2026 02:21:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7579a20056cd9531e754a57f957da811356775f676bfa6cd6e86b95f6de172d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8408948e08375e96299e735072f97a85aca5d58f65fc7cca125dfe5389160cb`

```dockerfile
```

-	Layers:
	-	`sha256:533c466de2027803aea398674e5a5ffd7d67b9e1eddc4228741a130ff830b02a`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 94.9 KB (94873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27c54b10e342535e2af7655af306fbf617d3dbf0922a7dd440f8ed4ea3e1fd5c`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:3a1e785feba037614143f75204bac3225d838127c68805b29ff23df9d8638070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c891a4120404380161eeeddd4e7c7cb748eb55193453c6e9090a59909bf1969`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 06:07:09 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 06:07:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 06:19:29 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 06:19:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 06:19:29 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 06:19:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 06:19:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 06:19:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 06:19:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 06:19:29 GMT
USER memcache
# Wed, 28 Jan 2026 06:19:29 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 06:19:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9dfe3bd7930f213b1f0f6c2854f26637f5a52c7cd4796e9eb59071fe2ff4b2f`  
		Last Modified: Wed, 28 Jan 2026 06:19:33 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:707447698613ddcfad121290546b5d9e04e2c3194b8f59394a272fe30f42dba1`  
		Last Modified: Wed, 28 Jan 2026 06:19:33 GMT  
		Size: 102.6 KB (102646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d366a66d67c4233b2ac1bc38363cb9881e63ca3af7f82ebbffbfb76942e1a34`  
		Last Modified: Wed, 28 Jan 2026 06:19:34 GMT  
		Size: 1.9 MB (1939230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e5326e5c6353c918ea1ac99aedfb19f688830f93037e66268b39c31f670e01`  
		Last Modified: Wed, 28 Jan 2026 06:19:33 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2ead2e4800bd6e32bbdb6225ecb70b554d33b3c17f3e8b973890f3b3c532da`  
		Last Modified: Wed, 28 Jan 2026 06:19:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:fd7fcbdf0e7f96a083f3d6aec29c9d21ac4b768be5949f68958c25756c153f95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07888c8ad7065e17bfea11af8f4f20b5f956ab1b553160f5ea4a484c4e437674`

```dockerfile
```

-	Layers:
	-	`sha256:aed006a02d773c56c072711ddc729af9ce5001ab757071fc3abdc5094822e7c7`  
		Last Modified: Wed, 28 Jan 2026 06:19:34 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:f08c7e3ff92e718b22bc7b21385421ebcf4bf6f542b797690d6547506821ab35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5272638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a6fc0ce35a3d59414018d4d8fe69929016a9e8dc7dc27daaafc617e3a7165d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:22:45 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:22:46 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:25:41 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:25:41 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:25:41 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:25:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:25:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:25:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:25:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:25:41 GMT
USER memcache
# Wed, 28 Jan 2026 02:25:41 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:25:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f61af882efa215dd577f7a17129442647756c535df9c13e821da864cddcf0e6`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b88f23b7692bcb2301e4e0a862af10c70c6ec663fca9e0a3389a74a3ba0520e`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 92.4 KB (92374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0549b4be8a16d49c33d6adaf28e4f8f7acbdea009dec2daed172741f7540ce5a`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 1.9 MB (1897188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6760f49ea55e45e14e26aaaf690948c109a5d85256175c84bbd06beccc8cd1`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9fca934ad2088c9a34e9f20e65d902054dfb9accdb4c6865924dd1fa88685b`  
		Last Modified: Wed, 28 Jan 2026 02:25:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:b5c2e8ac0b1fd0bd9c534bf163bad10efc0dc2c3afdfb66e3eb1a827d7bbfc87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dd20e2507c3ff3732182e3d2d44e5f7bc9b449bb172d5c7895b2fcc2dd423c6`

```dockerfile
```

-	Layers:
	-	`sha256:36627c0161ebd5c055e99a596a600017e5608e5895d1f95159116ff2df2eb3a6`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 94.3 KB (94291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a5914862f1fb65973ac0def541c9da056e1a5ef0bb26623a5bbad81803a4383`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:1a4aa193f53b5a4e2d82f6c67c23e87ef5d3d1cd1ddf96e0aabe73d49e537c2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6286893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f275b1c508af04216ccc891e9de0d7cbb35441f4eb424197e529ddbfb1d1b62`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:18:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:18:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:20:58 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:20:58 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:20:58 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:20:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:20:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:20:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:20:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:20:59 GMT
USER memcache
# Wed, 28 Jan 2026 02:20:59 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:20:59 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42047232a88cba1fc4d173d71bdf04395f6e4b83472de9f225ae2dd70ce14bc`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b625b9113e283efad9a0ee8e305f08edfd38a6c015224459a1ec0f2f49a0b915`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 121.8 KB (121845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf057b1d31677325905e009d68a97c3741028480d8b254105b145f39d157f2a`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 2.0 MB (1966604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db407fe2bd85342d8cb160bd73b5efe730723df2d20f2f6021eef8ad2d8f16eb`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfefb839a309e8b3df7a659236c09776f4eff9f8a47d9b331f131d9ad4c5d6b`  
		Last Modified: Wed, 28 Jan 2026 02:21:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:28b857747dd2742dbf00b9c1fc07265248073390d37bacf6cf8bfd313cf52a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f34aaccc9ca109270d86cdb6e46e56b207775ad700dadb1604f0a56b3ed4536e`

```dockerfile
```

-	Layers:
	-	`sha256:53b8cb56ae6a2b4c94fae4924dc03d881acba2e6c746fdb05808f3a86186ceff`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 94.3 KB (94327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03361fd0b86b6e905c14afa88e91f00f54a7e68e1d12d191b3d65c41986adc2e`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 20.7 KB (20728 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; 386

```console
$ docker pull memcached@sha256:8c10f776d94f57c5e0a4807247add0a2f3638eaafc3f6571b66ac325cc251866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5741838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f2329492e766d962366bfa352f931d82d7cd74d9e771ae6db7d44c1345197b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:16:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:16:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:18:59 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:18:59 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:18:59 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:18:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:18:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:18:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:18:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:18:59 GMT
USER memcache
# Wed, 28 Jan 2026 02:18:59 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:18:59 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbdb7a800485646296958fbca0c9cfdd5c397a0dbc2e33f1bc0c55dfca3c47a6`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7651295f62c54da7297c4ef646e146ef0acac3f551fb8a3dccc49190efced234`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 110.7 KB (110722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87d7b2cf89ac568b76f6e27208734340c49f4d7b0fedb8e5ae16f54a0cadc43`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 1.9 MB (1942772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4f82eada80af7ef4ec5dfcb36c5a93fa36157801318f374c5ab0d0987cd352`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61a034237824e579d4d24c5ec4b58ee8c400255488e658c36064d43c0001301`  
		Last Modified: Wed, 28 Jan 2026 02:19:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:118dd83c690f154abc02b708a01a0a0a48519b7faa920e5540ebf81c8e626429
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a7e54c817c006a1a17af2f06a4b3e4d1816cb0051c626c3f5e18a5012224b2`

```dockerfile
```

-	Layers:
	-	`sha256:11c94853238efef3a0c48e7cc56222e34874215e568475cfb20d3f2394aad42e`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 94.8 KB (94828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c97d62051151c9b1528a1b64a558c48025170f167ba863808d5fb67d4c59006`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:3a553e0d4ee19ee930775d8f8848969c6ff96b11e6b20f159ad754d11f5a8f8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6033619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfcda9c1811a9129ce53ed17b8ca116ffbaeebc21da0604c23b90e0dd042b0aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:33:21 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:33:22 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:35:40 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:35:40 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:35:40 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:35:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:35:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:35:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:35:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:35:41 GMT
USER memcache
# Wed, 28 Jan 2026 02:35:41 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:35:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c501a178d8bd3c1966eb75a7610efc35f292a3662f9fa7ca0d0089f54f723ce9`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac221803a5094f2d41563eece02e2e93293557ecb1eb5b7b646bcf143abcb82`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 126.3 KB (126255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d71af754023c45f69e3c70d3b4bfad1459328a7922268883ea41f2089ffe32ac`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 2.1 MB (2076366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c5df498426baf66bbc7701a67818ff6903c4420dc16591e79270ea8799caa35`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723a9c7624c2d00490e93ff507b003a4b495513fa6ec61b766c50bf5ccb8e23f`  
		Last Modified: Wed, 28 Jan 2026 02:35:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:238c5819c270bbc55c4140407b62939bf6ca158cb58cdbda8098f069301739a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9f43e248be2e248fe895fc3beccdf145fb06637800c6b89c19bf606d7c22975`

```dockerfile
```

-	Layers:
	-	`sha256:88da11471f4f95fd0f4679af21785a14ccb57b8bbd7fb96e4c42e1c49c333c33`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 94.3 KB (94280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b1fb2f254a022e51ca3dae9140daca46922a20d56b46607f22f1eef757d2fbb`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:8e9681abd0b8d92bb9145c49b7056cd27503f3420c10928ae606e4a65bdb9c9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5769974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:402a203724e613388d65f9de266b282381d864954d277c9552b24343915e9c40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 08:29:56 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 08:29:59 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 08:43:13 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 08:43:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 08:43:13 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 08:43:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 08:43:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 08:43:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 08:43:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 08:43:14 GMT
USER memcache
# Wed, 28 Jan 2026 08:43:14 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 08:43:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914e61f980ba6c54647d03d80091a261aae3ba7ab3d715251e992ea9407ad42e`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d963624519ed571edcf05aed3166ea5b7c1cd5fdae41a0d996d79be268f71e85`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 108.9 KB (108895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab35062ef9866f40cf3445147d50436a982e80d0ed984cca2f11d3ebcde5821`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 2.1 MB (2074437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82838004f4581bf0e6c37cecd3054aeb9fe5e1b92aeeb8cab2e86d9f9ed17af9`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b15a31cacc0f8dc4445667f3d0689a9857004aef390e2a16f7987db8124da4d7`  
		Last Modified: Wed, 28 Jan 2026 08:43:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:f15acc0a96b37da08e228c4fc099dbf28f370723c976c1a8a4d08679f5384799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c47e5bd1d37bec13b189586d46312efcb90ac656c7a80b9fd45fde1dd13f8e6e`

```dockerfile
```

-	Layers:
	-	`sha256:216d743a064cca1bd85c432678c24f3fa640798967115037f27c923138aa7af6`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 94.3 KB (94276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c38c6e624d8af51c7da79f4f214eb73cbfe3c2a2f9b465649a72b8dfa18429f`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; s390x

```console
$ docker pull memcached@sha256:f52690bd1266bfbe887fa9c03fc963f0277f331a85d8e81f4f134076c6d899f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5858103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7903f118ee1fcea4632b09ffbabd30b82ef4aa3b68dd3570b1173f263cacc343`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:21:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:21:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:24:07 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:24:07 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:24:07 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:24:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:24:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:24:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:24:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:24:08 GMT
USER memcache
# Wed, 28 Jan 2026 02:24:08 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:24:08 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030f843902eb7c01da3de08b6efb672d46d4f41e9e298640c66daabea5d901ef`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100608bf5f6494395c46670a28e6df9d705e08dc9129c1fb36b8f265fa52c22b`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 114.3 KB (114299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b706c73349baf76aabbef50d7dba3c89b85ffc84ad0aca5c544b1fe047706785`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 2.0 MB (2017124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce545f5bb33e4374e2e0bb9b11e751c89272699812f06c49e8e6a2e5ac3d524`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ac2e9e98ac3e799be9d54501be2f2304ef93065d34bef18f002ea38838ea24`  
		Last Modified: Wed, 28 Jan 2026 02:24:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:b4850489cf16ad5f72674b698ab0c2d16d95c6cc43e1b3f611f9fa67adcf4962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b79deed0597f9356a7dd99d34cb933d7634c520350fcabb9da14b254006070d0`

```dockerfile
```

-	Layers:
	-	`sha256:00a586e58a4b437f0260b3197ecff606cb3380869c6861c89d769a99132c10e9`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 94.2 KB (94222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8caeef6fbf9d37a3d092d84298ef02b53e2efff54347431fcc362c14dcdb9eb5`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine3.23`

```console
$ docker pull memcached@sha256:8a82a3927694e42bc52679dc81532244de51e5faed5f9541a1283e3ad7271db1
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
$ docker pull memcached@sha256:947366d40559340a4385b3e05f92186b9546e7feb59ef280e243ec8bf34f01a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5958530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7977390ffe9a7f3b6d3c5840f262b8058ca015d7daf5237e480d3f51a29e0b6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:18:28 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:18:29 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:21:03 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:21:03 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:21:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:21:03 GMT
USER memcache
# Wed, 28 Jan 2026 02:21:03 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:21:03 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e0ee508166c94a4f9ca8c32f743bd3733afb7660800042c7da03c2ea1da6b4`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15bf9562ecbc21cc4f52d1a4d33eb5eec98aa63c36c59f018b55071b8dd9f05f`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 106.1 KB (106059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24c6974a0da2f6cdd2022450be6195683245ba21f601d207ad14566c653ddea`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 2.0 MB (1989295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a859de0eb0253d066d7de73c90f4ebdc8b737fddab90420fd0ba6bd1c74669`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7be89a9ef60cc91d2346c9bc9a975138908bbc03aa40c948ab5e7336aa8e8b`  
		Last Modified: Wed, 28 Jan 2026 02:21:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:7579a20056cd9531e754a57f957da811356775f676bfa6cd6e86b95f6de172d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8408948e08375e96299e735072f97a85aca5d58f65fc7cca125dfe5389160cb`

```dockerfile
```

-	Layers:
	-	`sha256:533c466de2027803aea398674e5a5ffd7d67b9e1eddc4228741a130ff830b02a`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 94.9 KB (94873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27c54b10e342535e2af7655af306fbf617d3dbf0922a7dd440f8ed4ea3e1fd5c`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.23` - linux; arm variant v6

```console
$ docker pull memcached@sha256:3a1e785feba037614143f75204bac3225d838127c68805b29ff23df9d8638070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c891a4120404380161eeeddd4e7c7cb748eb55193453c6e9090a59909bf1969`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 06:07:09 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 06:07:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 06:19:29 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 06:19:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 06:19:29 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 06:19:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 06:19:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 06:19:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 06:19:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 06:19:29 GMT
USER memcache
# Wed, 28 Jan 2026 06:19:29 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 06:19:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9dfe3bd7930f213b1f0f6c2854f26637f5a52c7cd4796e9eb59071fe2ff4b2f`  
		Last Modified: Wed, 28 Jan 2026 06:19:33 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:707447698613ddcfad121290546b5d9e04e2c3194b8f59394a272fe30f42dba1`  
		Last Modified: Wed, 28 Jan 2026 06:19:33 GMT  
		Size: 102.6 KB (102646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d366a66d67c4233b2ac1bc38363cb9881e63ca3af7f82ebbffbfb76942e1a34`  
		Last Modified: Wed, 28 Jan 2026 06:19:34 GMT  
		Size: 1.9 MB (1939230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e5326e5c6353c918ea1ac99aedfb19f688830f93037e66268b39c31f670e01`  
		Last Modified: Wed, 28 Jan 2026 06:19:33 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2ead2e4800bd6e32bbdb6225ecb70b554d33b3c17f3e8b973890f3b3c532da`  
		Last Modified: Wed, 28 Jan 2026 06:19:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:fd7fcbdf0e7f96a083f3d6aec29c9d21ac4b768be5949f68958c25756c153f95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07888c8ad7065e17bfea11af8f4f20b5f956ab1b553160f5ea4a484c4e437674`

```dockerfile
```

-	Layers:
	-	`sha256:aed006a02d773c56c072711ddc729af9ce5001ab757071fc3abdc5094822e7c7`  
		Last Modified: Wed, 28 Jan 2026 06:19:34 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.23` - linux; arm variant v7

```console
$ docker pull memcached@sha256:f08c7e3ff92e718b22bc7b21385421ebcf4bf6f542b797690d6547506821ab35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5272638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a6fc0ce35a3d59414018d4d8fe69929016a9e8dc7dc27daaafc617e3a7165d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:22:45 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:22:46 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:25:41 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:25:41 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:25:41 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:25:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:25:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:25:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:25:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:25:41 GMT
USER memcache
# Wed, 28 Jan 2026 02:25:41 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:25:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f61af882efa215dd577f7a17129442647756c535df9c13e821da864cddcf0e6`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b88f23b7692bcb2301e4e0a862af10c70c6ec663fca9e0a3389a74a3ba0520e`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 92.4 KB (92374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0549b4be8a16d49c33d6adaf28e4f8f7acbdea009dec2daed172741f7540ce5a`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 1.9 MB (1897188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6760f49ea55e45e14e26aaaf690948c109a5d85256175c84bbd06beccc8cd1`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9fca934ad2088c9a34e9f20e65d902054dfb9accdb4c6865924dd1fa88685b`  
		Last Modified: Wed, 28 Jan 2026 02:25:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:b5c2e8ac0b1fd0bd9c534bf163bad10efc0dc2c3afdfb66e3eb1a827d7bbfc87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dd20e2507c3ff3732182e3d2d44e5f7bc9b449bb172d5c7895b2fcc2dd423c6`

```dockerfile
```

-	Layers:
	-	`sha256:36627c0161ebd5c055e99a596a600017e5608e5895d1f95159116ff2df2eb3a6`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 94.3 KB (94291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a5914862f1fb65973ac0def541c9da056e1a5ef0bb26623a5bbad81803a4383`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.23` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:1a4aa193f53b5a4e2d82f6c67c23e87ef5d3d1cd1ddf96e0aabe73d49e537c2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6286893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f275b1c508af04216ccc891e9de0d7cbb35441f4eb424197e529ddbfb1d1b62`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:18:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:18:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:20:58 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:20:58 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:20:58 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:20:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:20:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:20:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:20:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:20:59 GMT
USER memcache
# Wed, 28 Jan 2026 02:20:59 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:20:59 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42047232a88cba1fc4d173d71bdf04395f6e4b83472de9f225ae2dd70ce14bc`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b625b9113e283efad9a0ee8e305f08edfd38a6c015224459a1ec0f2f49a0b915`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 121.8 KB (121845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf057b1d31677325905e009d68a97c3741028480d8b254105b145f39d157f2a`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 2.0 MB (1966604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db407fe2bd85342d8cb160bd73b5efe730723df2d20f2f6021eef8ad2d8f16eb`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfefb839a309e8b3df7a659236c09776f4eff9f8a47d9b331f131d9ad4c5d6b`  
		Last Modified: Wed, 28 Jan 2026 02:21:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:28b857747dd2742dbf00b9c1fc07265248073390d37bacf6cf8bfd313cf52a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f34aaccc9ca109270d86cdb6e46e56b207775ad700dadb1604f0a56b3ed4536e`

```dockerfile
```

-	Layers:
	-	`sha256:53b8cb56ae6a2b4c94fae4924dc03d881acba2e6c746fdb05808f3a86186ceff`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 94.3 KB (94327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03361fd0b86b6e905c14afa88e91f00f54a7e68e1d12d191b3d65c41986adc2e`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 20.7 KB (20728 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.23` - linux; 386

```console
$ docker pull memcached@sha256:8c10f776d94f57c5e0a4807247add0a2f3638eaafc3f6571b66ac325cc251866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5741838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f2329492e766d962366bfa352f931d82d7cd74d9e771ae6db7d44c1345197b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:16:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:16:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:18:59 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:18:59 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:18:59 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:18:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:18:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:18:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:18:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:18:59 GMT
USER memcache
# Wed, 28 Jan 2026 02:18:59 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:18:59 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbdb7a800485646296958fbca0c9cfdd5c397a0dbc2e33f1bc0c55dfca3c47a6`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7651295f62c54da7297c4ef646e146ef0acac3f551fb8a3dccc49190efced234`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 110.7 KB (110722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87d7b2cf89ac568b76f6e27208734340c49f4d7b0fedb8e5ae16f54a0cadc43`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 1.9 MB (1942772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4f82eada80af7ef4ec5dfcb36c5a93fa36157801318f374c5ab0d0987cd352`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61a034237824e579d4d24c5ec4b58ee8c400255488e658c36064d43c0001301`  
		Last Modified: Wed, 28 Jan 2026 02:19:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:118dd83c690f154abc02b708a01a0a0a48519b7faa920e5540ebf81c8e626429
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a7e54c817c006a1a17af2f06a4b3e4d1816cb0051c626c3f5e18a5012224b2`

```dockerfile
```

-	Layers:
	-	`sha256:11c94853238efef3a0c48e7cc56222e34874215e568475cfb20d3f2394aad42e`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 94.8 KB (94828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c97d62051151c9b1528a1b64a558c48025170f167ba863808d5fb67d4c59006`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.23` - linux; ppc64le

```console
$ docker pull memcached@sha256:3a553e0d4ee19ee930775d8f8848969c6ff96b11e6b20f159ad754d11f5a8f8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6033619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfcda9c1811a9129ce53ed17b8ca116ffbaeebc21da0604c23b90e0dd042b0aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:33:21 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:33:22 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:35:40 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:35:40 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:35:40 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:35:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:35:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:35:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:35:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:35:41 GMT
USER memcache
# Wed, 28 Jan 2026 02:35:41 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:35:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c501a178d8bd3c1966eb75a7610efc35f292a3662f9fa7ca0d0089f54f723ce9`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac221803a5094f2d41563eece02e2e93293557ecb1eb5b7b646bcf143abcb82`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 126.3 KB (126255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d71af754023c45f69e3c70d3b4bfad1459328a7922268883ea41f2089ffe32ac`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 2.1 MB (2076366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c5df498426baf66bbc7701a67818ff6903c4420dc16591e79270ea8799caa35`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723a9c7624c2d00490e93ff507b003a4b495513fa6ec61b766c50bf5ccb8e23f`  
		Last Modified: Wed, 28 Jan 2026 02:35:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:238c5819c270bbc55c4140407b62939bf6ca158cb58cdbda8098f069301739a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9f43e248be2e248fe895fc3beccdf145fb06637800c6b89c19bf606d7c22975`

```dockerfile
```

-	Layers:
	-	`sha256:88da11471f4f95fd0f4679af21785a14ccb57b8bbd7fb96e4c42e1c49c333c33`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 94.3 KB (94280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b1fb2f254a022e51ca3dae9140daca46922a20d56b46607f22f1eef757d2fbb`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.23` - linux; riscv64

```console
$ docker pull memcached@sha256:8e9681abd0b8d92bb9145c49b7056cd27503f3420c10928ae606e4a65bdb9c9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5769974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:402a203724e613388d65f9de266b282381d864954d277c9552b24343915e9c40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 08:29:56 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 08:29:59 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 08:43:13 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 08:43:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 08:43:13 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 08:43:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 08:43:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 08:43:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 08:43:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 08:43:14 GMT
USER memcache
# Wed, 28 Jan 2026 08:43:14 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 08:43:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914e61f980ba6c54647d03d80091a261aae3ba7ab3d715251e992ea9407ad42e`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d963624519ed571edcf05aed3166ea5b7c1cd5fdae41a0d996d79be268f71e85`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 108.9 KB (108895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab35062ef9866f40cf3445147d50436a982e80d0ed984cca2f11d3ebcde5821`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 2.1 MB (2074437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82838004f4581bf0e6c37cecd3054aeb9fe5e1b92aeeb8cab2e86d9f9ed17af9`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b15a31cacc0f8dc4445667f3d0689a9857004aef390e2a16f7987db8124da4d7`  
		Last Modified: Wed, 28 Jan 2026 08:43:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:f15acc0a96b37da08e228c4fc099dbf28f370723c976c1a8a4d08679f5384799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c47e5bd1d37bec13b189586d46312efcb90ac656c7a80b9fd45fde1dd13f8e6e`

```dockerfile
```

-	Layers:
	-	`sha256:216d743a064cca1bd85c432678c24f3fa640798967115037f27c923138aa7af6`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 94.3 KB (94276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c38c6e624d8af51c7da79f4f214eb73cbfe3c2a2f9b465649a72b8dfa18429f`  
		Last Modified: Wed, 28 Jan 2026 08:43:46 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.23` - linux; s390x

```console
$ docker pull memcached@sha256:f52690bd1266bfbe887fa9c03fc963f0277f331a85d8e81f4f134076c6d899f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5858103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7903f118ee1fcea4632b09ffbabd30b82ef4aa3b68dd3570b1173f263cacc343`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:21:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:21:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:24:07 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:24:07 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:24:07 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:24:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:24:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:24:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:24:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:24:08 GMT
USER memcache
# Wed, 28 Jan 2026 02:24:08 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:24:08 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030f843902eb7c01da3de08b6efb672d46d4f41e9e298640c66daabea5d901ef`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100608bf5f6494395c46670a28e6df9d705e08dc9129c1fb36b8f265fa52c22b`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 114.3 KB (114299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b706c73349baf76aabbef50d7dba3c89b85ffc84ad0aca5c544b1fe047706785`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 2.0 MB (2017124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce545f5bb33e4374e2e0bb9b11e751c89272699812f06c49e8e6a2e5ac3d524`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ac2e9e98ac3e799be9d54501be2f2304ef93065d34bef18f002ea38838ea24`  
		Last Modified: Wed, 28 Jan 2026 02:24:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:b4850489cf16ad5f72674b698ab0c2d16d95c6cc43e1b3f611f9fa67adcf4962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b79deed0597f9356a7dd99d34cb933d7634c520350fcabb9da14b254006070d0`

```dockerfile
```

-	Layers:
	-	`sha256:00a586e58a4b437f0260b3197ecff606cb3380869c6861c89d769a99132c10e9`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 94.2 KB (94222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8caeef6fbf9d37a3d092d84298ef02b53e2efff54347431fcc362c14dcdb9eb5`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:27 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b6e737e1a3eed198cc17e2b92231ab084bcf55ba90a36136e7a2f4fd04a95b`  
		Last Modified: Tue, 13 Jan 2026 01:25:25 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16835fec399670b74d32630a7368a65ca2a3c32d8b7a690d33bebc7b9e9458d`  
		Last Modified: Tue, 13 Jan 2026 01:25:24 GMT  
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
		Last Modified: Tue, 13 Jan 2026 01:25:25 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 27.9 MB (27942724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96776850dc1206c3fd163b84cea19599306159eb0d020b4241d0172240f88d13`  
		Last Modified: Tue, 13 Jan 2026 01:22:50 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3697c7c790d9c4caaa904abdaf809dcdee3f0b518fc5ad82d2e21dd7fe24f64d`  
		Last Modified: Tue, 13 Jan 2026 01:22:50 GMT  
		Size: 144.2 KB (144212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a247339c7ec57a491c3ffe43531dbfaa132f3ff16a481fc41cbb9e3e3ad6476`  
		Last Modified: Tue, 13 Jan 2026 01:22:50 GMT  
		Size: 2.2 MB (2210412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2dcebe3ab2a9945cdea142301e4a64eebbc59c948a54385dbfca4afd561b508`  
		Last Modified: Tue, 13 Jan 2026 01:22:50 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb8ef5ecbc44efd5280f9cf15687dfd80a34fa2966ad039238647177f75dc6c`  
		Last Modified: Tue, 13 Jan 2026 01:22:51 GMT  
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
		Last Modified: Tue, 13 Jan 2026 01:22:50 GMT  
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
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
		Size: 135.4 KB (135398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9371e974781bd91adc657086f00cd7d91b5530ca9da37597c347dd7d4eaff0`  
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
		Size: 2.2 MB (2164040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c2e0f64c0afa16b5e214ae208c8c81e8c78c79ddd90f54983a93c7297395f6b`  
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
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
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
		Size: 2.0 MB (2009750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e76d5584f581b7668c61a661da2858bc1d5e11b31e3629e0d2b3af52d9c22ed8`  
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:41 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78edb6b991369235f90958a936afc89dc37b82439c632988ed143b5bd76deadb`  
		Last Modified: Tue, 13 Jan 2026 01:25:33 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e1afbb765f6cc3923e864d44fb6cd6c9167b884e596b09bd37c7c276f65a2b`  
		Last Modified: Tue, 13 Jan 2026 01:25:33 GMT  
		Size: 153.5 KB (153512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff9edc68fe57c233001afd442eb6c248bf070d32fbb412a8bfeef6f9a6217f5`  
		Last Modified: Tue, 13 Jan 2026 01:25:33 GMT  
		Size: 2.3 MB (2261341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c4648fbc4a4189184946895d1041e0eee2c5d40fd70638a553bedb0cbf5cf8`  
		Last Modified: Tue, 13 Jan 2026 01:25:33 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26bd1b32b048e73091ddf6e6762e368d4bb6ef2cc7d3aa43467749b36fe08e38`  
		Last Modified: Tue, 13 Jan 2026 01:25:34 GMT  
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
		Last Modified: Tue, 13 Jan 2026 01:25:33 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:56 GMT  
		Size: 31.3 MB (31288476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cedb4f2840edea9de46e0d955a0512f469211880560a8948f10b54381bcd728`  
		Last Modified: Tue, 13 Jan 2026 01:22:46 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c4b2d1574ee5f238dc6948164abd39ffcc91929b2c464c6b3874dec01fd964`  
		Last Modified: Tue, 13 Jan 2026 01:22:46 GMT  
		Size: 147.6 KB (147554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc1bf5870b84175607f3d012b3cfebc5859869f8125114ea5d6ed1a05f81d2d`  
		Last Modified: Tue, 13 Jan 2026 01:22:46 GMT  
		Size: 2.2 MB (2223652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6434e73ed67e81f1016f27c7cc175290b0ce959d8a1bf5e9b0f3119f161246`  
		Last Modified: Tue, 13 Jan 2026 01:22:46 GMT  
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
		Last Modified: Tue, 13 Jan 2026 01:22:46 GMT  
		Size: 2.0 MB (2005447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6358862e12c5c5367efd52bea0b1194e04e76f267084da591229f64ee7482dc3`  
		Last Modified: Tue, 13 Jan 2026 01:22:46 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:57:06 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093e59deb53ff01a892be2a5df928c4b04a289df7f6c135570c11d6a4fdbc53a`  
		Last Modified: Tue, 13 Jan 2026 01:37:09 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4da25c8b13ee47050a38843c1954d2bd7bbdba2666f725aee2f603e03fcb6d`  
		Last Modified: Tue, 13 Jan 2026 01:37:09 GMT  
		Size: 170.4 KB (170427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cab5f6f805c735c0f324c87ff8c66cfab0e35fb691b7761e85bb9a2bbb31cfe`  
		Last Modified: Tue, 13 Jan 2026 01:37:09 GMT  
		Size: 2.4 MB (2393947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3a7dfc8da65bd6101de156530bc2688c5588c718bbc3131ff4594cbefd0e66`  
		Last Modified: Tue, 13 Jan 2026 01:37:09 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06153b2e2bde9b06f1c2719aabb5ff6a6c23056152a024fa2c990d97b4d9c799`  
		Last Modified: Tue, 13 Jan 2026 01:37:10 GMT  
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
		Last Modified: Tue, 13 Jan 2026 01:37:09 GMT  
		Size: 2.0 MB (2011891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc718b3aa0399c50248bba6165cad8666196a5351b6ed095a8101d2f8a5d37da`  
		Last Modified: Tue, 13 Jan 2026 01:37:09 GMT  
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
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168d1b37fe07dfb8bef5240057ad6597058647499a9e771eedd2091f2d6b30f0`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 133.1 KB (133105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a5ebc1ef49cab24f75e0c751a1e0563ee042c246c509279fa38cf3cbf0a3f1`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 2.2 MB (2207499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbc8df7ca1d2f273c3c8fec55b30f17ebc72a45687976efd9c8779a66369d46`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4057c9476d421ae1ecae3607afb0db57dbc6eb2bc0aa5e41daed169a70319c1`  
		Last Modified: Wed, 14 Jan 2026 06:50:29 GMT  
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
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 2.0 MB (2002254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0de5bd0cbff9df1fc11e05bd38936b6915195663b273b5c23840bf5eb9373a8`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
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
		Last Modified: Tue, 13 Jan 2026 13:10:27 GMT  
		Size: 29.8 MB (29833411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2727771ad16d920baecb7c96b9b54e67178369b881fc20901d381dfd5f873e27`  
		Last Modified: Tue, 13 Jan 2026 14:17:08 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6b0ec5581f8591522a6327cdcfa4e1197d9ada9fb60840f57b5d3e4dd3304d1`  
		Last Modified: Tue, 13 Jan 2026 14:17:08 GMT  
		Size: 140.6 KB (140562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382a3e1ebed70673a0789fcc2104ab941fe04b9a020339f9286ac85b67ae5ff9`  
		Last Modified: Tue, 13 Jan 2026 14:17:08 GMT  
		Size: 2.3 MB (2297368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85fe5f9afd355e3dd76ce942e1c295e356d96ae3b0e3f8236a0e33c5f75ffe71`  
		Last Modified: Tue, 13 Jan 2026 14:17:08 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4546f3c3457928dc273f98dae7c7ac2f945b203138e964ee72fc92aabcef434`  
		Last Modified: Tue, 13 Jan 2026 14:17:09 GMT  
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
		Last Modified: Tue, 13 Jan 2026 14:17:08 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:27 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b6e737e1a3eed198cc17e2b92231ab084bcf55ba90a36136e7a2f4fd04a95b`  
		Last Modified: Tue, 13 Jan 2026 01:25:25 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16835fec399670b74d32630a7368a65ca2a3c32d8b7a690d33bebc7b9e9458d`  
		Last Modified: Tue, 13 Jan 2026 01:25:24 GMT  
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
		Last Modified: Tue, 13 Jan 2026 01:25:25 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 27.9 MB (27942724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96776850dc1206c3fd163b84cea19599306159eb0d020b4241d0172240f88d13`  
		Last Modified: Tue, 13 Jan 2026 01:22:50 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3697c7c790d9c4caaa904abdaf809dcdee3f0b518fc5ad82d2e21dd7fe24f64d`  
		Last Modified: Tue, 13 Jan 2026 01:22:50 GMT  
		Size: 144.2 KB (144212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a247339c7ec57a491c3ffe43531dbfaa132f3ff16a481fc41cbb9e3e3ad6476`  
		Last Modified: Tue, 13 Jan 2026 01:22:50 GMT  
		Size: 2.2 MB (2210412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2dcebe3ab2a9945cdea142301e4a64eebbc59c948a54385dbfca4afd561b508`  
		Last Modified: Tue, 13 Jan 2026 01:22:50 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb8ef5ecbc44efd5280f9cf15687dfd80a34fa2966ad039238647177f75dc6c`  
		Last Modified: Tue, 13 Jan 2026 01:22:51 GMT  
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
		Last Modified: Tue, 13 Jan 2026 01:22:50 GMT  
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
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
		Size: 135.4 KB (135398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9371e974781bd91adc657086f00cd7d91b5530ca9da37597c347dd7d4eaff0`  
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
		Size: 2.2 MB (2164040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c2e0f64c0afa16b5e214ae208c8c81e8c78c79ddd90f54983a93c7297395f6b`  
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
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
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
		Size: 2.0 MB (2009750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e76d5584f581b7668c61a661da2858bc1d5e11b31e3629e0d2b3af52d9c22ed8`  
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:41 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78edb6b991369235f90958a936afc89dc37b82439c632988ed143b5bd76deadb`  
		Last Modified: Tue, 13 Jan 2026 01:25:33 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e1afbb765f6cc3923e864d44fb6cd6c9167b884e596b09bd37c7c276f65a2b`  
		Last Modified: Tue, 13 Jan 2026 01:25:33 GMT  
		Size: 153.5 KB (153512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff9edc68fe57c233001afd442eb6c248bf070d32fbb412a8bfeef6f9a6217f5`  
		Last Modified: Tue, 13 Jan 2026 01:25:33 GMT  
		Size: 2.3 MB (2261341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c4648fbc4a4189184946895d1041e0eee2c5d40fd70638a553bedb0cbf5cf8`  
		Last Modified: Tue, 13 Jan 2026 01:25:33 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26bd1b32b048e73091ddf6e6762e368d4bb6ef2cc7d3aa43467749b36fe08e38`  
		Last Modified: Tue, 13 Jan 2026 01:25:34 GMT  
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
		Last Modified: Tue, 13 Jan 2026 01:25:33 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:56 GMT  
		Size: 31.3 MB (31288476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cedb4f2840edea9de46e0d955a0512f469211880560a8948f10b54381bcd728`  
		Last Modified: Tue, 13 Jan 2026 01:22:46 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c4b2d1574ee5f238dc6948164abd39ffcc91929b2c464c6b3874dec01fd964`  
		Last Modified: Tue, 13 Jan 2026 01:22:46 GMT  
		Size: 147.6 KB (147554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc1bf5870b84175607f3d012b3cfebc5859869f8125114ea5d6ed1a05f81d2d`  
		Last Modified: Tue, 13 Jan 2026 01:22:46 GMT  
		Size: 2.2 MB (2223652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6434e73ed67e81f1016f27c7cc175290b0ce959d8a1bf5e9b0f3119f161246`  
		Last Modified: Tue, 13 Jan 2026 01:22:46 GMT  
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
		Last Modified: Tue, 13 Jan 2026 01:22:46 GMT  
		Size: 2.0 MB (2005447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6358862e12c5c5367efd52bea0b1194e04e76f267084da591229f64ee7482dc3`  
		Last Modified: Tue, 13 Jan 2026 01:22:46 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:57:06 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093e59deb53ff01a892be2a5df928c4b04a289df7f6c135570c11d6a4fdbc53a`  
		Last Modified: Tue, 13 Jan 2026 01:37:09 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4da25c8b13ee47050a38843c1954d2bd7bbdba2666f725aee2f603e03fcb6d`  
		Last Modified: Tue, 13 Jan 2026 01:37:09 GMT  
		Size: 170.4 KB (170427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cab5f6f805c735c0f324c87ff8c66cfab0e35fb691b7761e85bb9a2bbb31cfe`  
		Last Modified: Tue, 13 Jan 2026 01:37:09 GMT  
		Size: 2.4 MB (2393947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3a7dfc8da65bd6101de156530bc2688c5588c718bbc3131ff4594cbefd0e66`  
		Last Modified: Tue, 13 Jan 2026 01:37:09 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06153b2e2bde9b06f1c2719aabb5ff6a6c23056152a024fa2c990d97b4d9c799`  
		Last Modified: Tue, 13 Jan 2026 01:37:10 GMT  
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
		Last Modified: Tue, 13 Jan 2026 01:37:09 GMT  
		Size: 2.0 MB (2011891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc718b3aa0399c50248bba6165cad8666196a5351b6ed095a8101d2f8a5d37da`  
		Last Modified: Tue, 13 Jan 2026 01:37:09 GMT  
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
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168d1b37fe07dfb8bef5240057ad6597058647499a9e771eedd2091f2d6b30f0`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 133.1 KB (133105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a5ebc1ef49cab24f75e0c751a1e0563ee042c246c509279fa38cf3cbf0a3f1`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 2.2 MB (2207499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbc8df7ca1d2f273c3c8fec55b30f17ebc72a45687976efd9c8779a66369d46`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4057c9476d421ae1ecae3607afb0db57dbc6eb2bc0aa5e41daed169a70319c1`  
		Last Modified: Wed, 14 Jan 2026 06:50:29 GMT  
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
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
		Size: 2.0 MB (2002254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0de5bd0cbff9df1fc11e05bd38936b6915195663b273b5c23840bf5eb9373a8`  
		Last Modified: Wed, 14 Jan 2026 06:50:28 GMT  
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
		Last Modified: Tue, 13 Jan 2026 13:10:27 GMT  
		Size: 29.8 MB (29833411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2727771ad16d920baecb7c96b9b54e67178369b881fc20901d381dfd5f873e27`  
		Last Modified: Tue, 13 Jan 2026 14:17:08 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6b0ec5581f8591522a6327cdcfa4e1197d9ada9fb60840f57b5d3e4dd3304d1`  
		Last Modified: Tue, 13 Jan 2026 14:17:08 GMT  
		Size: 140.6 KB (140562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382a3e1ebed70673a0789fcc2104ab941fe04b9a020339f9286ac85b67ae5ff9`  
		Last Modified: Tue, 13 Jan 2026 14:17:08 GMT  
		Size: 2.3 MB (2297368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85fe5f9afd355e3dd76ce942e1c295e356d96ae3b0e3f8236a0e33c5f75ffe71`  
		Last Modified: Tue, 13 Jan 2026 14:17:08 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4546f3c3457928dc273f98dae7c7ac2f945b203138e964ee72fc92aabcef434`  
		Last Modified: Tue, 13 Jan 2026 14:17:09 GMT  
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
		Last Modified: Tue, 13 Jan 2026 14:17:08 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json
