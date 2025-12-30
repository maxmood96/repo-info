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
$ docker pull memcached@sha256:36c36f0c38cda62ab29af64a0eefa53e99879265ff70df8ac12597be28c482f7
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
$ docker pull memcached@sha256:61bcd214c8da24f2bacfd9152bccafef4f4c0993897c945ee3058106e084b314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32193395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5dafc7d411a870fbc52ca64194006e50e355d34f1edf56b4e1dc5b8019b0934`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:21:34 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 29 Dec 2025 23:21:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:24:22 GMT
ENV MEMCACHED_VERSION=1.6.40
# Mon, 29 Dec 2025 23:24:22 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Mon, 29 Dec 2025 23:24:22 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Mon, 29 Dec 2025 23:24:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 29 Dec 2025 23:24:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:24:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 29 Dec 2025 23:24:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:24:22 GMT
USER memcache
# Mon, 29 Dec 2025 23:24:22 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 29 Dec 2025 23:24:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d08d8001380dd7c5a9be2e59244310ccfa7e84f3b896b354059d46d1928401`  
		Last Modified: Mon, 29 Dec 2025 23:24:36 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8420bae5d2af8b5b5e66d7e5ba882f5e2034cc64eacfb1a0b4b32a259a541b16`  
		Last Modified: Mon, 29 Dec 2025 23:24:35 GMT  
		Size: 136.7 KB (136694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc2daf1b2287468ea06570c5bedff8bc84ab6833050a7e0686f5f7d7a2679e1`  
		Last Modified: Mon, 29 Dec 2025 23:24:35 GMT  
		Size: 2.3 MB (2278657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a54c348dd92d8a79d150c1fe56008dba798b633f010e1e57c0a18f62b2752d90`  
		Last Modified: Mon, 29 Dec 2025 23:24:35 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e147936d0f858c8f726dea003b7220347e43918cab2714f81c66c1553cc160cd`  
		Last Modified: Mon, 29 Dec 2025 23:24:35 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:e6d0cef74a4a91255f97601317c1cd45953291e56aebea597b1f5fedb87772df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a114559b11eef9830f21c5cfd0b3dff0712acd507604d89ab89f16d229d637c`

```dockerfile
```

-	Layers:
	-	`sha256:31d77d05cfee83189fed485cbb6de83d56b3fc5c8a37eafd4e5ab2a8646bcee5`  
		Last Modified: Tue, 30 Dec 2025 04:34:52 GMT  
		Size: 2.0 MB (2008228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:daae5d64f19c0b653f152172ab207032a103d7a2c198208a2472a4565869c64e`  
		Last Modified: Tue, 30 Dec 2025 04:34:53 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm variant v5

```console
$ docker pull memcached@sha256:19778ab8ffe04b579956362255d1b4be4646df675a0c0db5662d882e7e062834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30300227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85e834ef35584236d3b04d1823e406899096de386d548c5f0bfd896cfba41631`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:17:23 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 29 Dec 2025 23:17:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:39:32 GMT
ENV MEMCACHED_VERSION=1.6.40
# Mon, 29 Dec 2025 23:39:32 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Mon, 29 Dec 2025 23:39:32 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Mon, 29 Dec 2025 23:39:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 29 Dec 2025 23:39:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:39:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 29 Dec 2025 23:39:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:39:32 GMT
USER memcache
# Mon, 29 Dec 2025 23:39:32 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 29 Dec 2025 23:39:32 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b99a8d8dab982a1a4ea341e66b178b14c0f373c2cd90ac46a67308a4f43c82ae`  
		Last Modified: Mon, 29 Dec 2025 22:27:09 GMT  
		Size: 27.9 MB (27944146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0be68f37541245f1acaee607441dfc983a00e90d78d5e0941265d0b67b1cc9a`  
		Last Modified: Mon, 29 Dec 2025 23:39:44 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10905a7698a57312678edda9f8fc0748b6288699f5fed1f8e7e7e909240d441`  
		Last Modified: Mon, 29 Dec 2025 23:39:44 GMT  
		Size: 144.1 KB (144149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea062eb6d6681b78497a81a8d5ca89088b56f5a5d629e3124df93b9ca0e4f16`  
		Last Modified: Mon, 29 Dec 2025 23:39:44 GMT  
		Size: 2.2 MB (2210419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d59770b8679e935091911e6294f61a53df8f59b5cc8aae431217cc391864a0`  
		Last Modified: Mon, 29 Dec 2025 23:39:44 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945c1d27fa6617071d97eddd3d962ac571276f7f757f99edc1a93ebbe6eb5a9c`  
		Last Modified: Mon, 29 Dec 2025 23:39:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:27e3afeed14c4cac078a10db01ef22eef58848fc65d93501050f872bc3cf64d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:939368d93857b65d5e6bbdc97a5f4d158eeca9efc9fb02875eae93350ea663fb`

```dockerfile
```

-	Layers:
	-	`sha256:3559f8384ca294c984900b7325032abfe47459734f215e79264a22aa23802031`  
		Last Modified: Tue, 30 Dec 2025 01:35:12 GMT  
		Size: 2.0 MB (2011231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b310c8a994e22e59ca814cd06500201d5b78c4bbfe3baa8785ae093760d4a4fb`  
		Last Modified: Tue, 30 Dec 2025 01:35:13 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm variant v7

```console
$ docker pull memcached@sha256:34f932820fcffc223d050d31ceeef236f4bc4a1a8e776006560fe2ef14348a2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28510848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0a0c32503881f91ec515af1fd074032b8070eac0faa4afca5e1f2f60609b237`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:17:22 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 29 Dec 2025 23:17:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:20:31 GMT
ENV MEMCACHED_VERSION=1.6.40
# Mon, 29 Dec 2025 23:20:31 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Mon, 29 Dec 2025 23:20:31 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Mon, 29 Dec 2025 23:20:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 29 Dec 2025 23:20:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:20:31 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 29 Dec 2025 23:20:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:20:31 GMT
USER memcache
# Mon, 29 Dec 2025 23:20:31 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 29 Dec 2025 23:20:31 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6d3e0fea3cb8eb29b9c06956265b47cd00f7ebfb48e35e818f686d52c21353f5`  
		Last Modified: Mon, 29 Dec 2025 22:28:07 GMT  
		Size: 26.2 MB (26210001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f916949d5244227fca363e62638c31c65e0f6a941ceaa0fb79c37d962e9b95bb`  
		Last Modified: Mon, 29 Dec 2025 23:20:45 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f24598f250037f41edf0d0093ed08f2b3b3937f91d7708c687330e0feca3fdcf`  
		Last Modified: Mon, 29 Dec 2025 23:20:45 GMT  
		Size: 135.4 KB (135362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f260cb2adbfa9ad1d74da541da12d2146b1a06685021b42e924c843481237ee2`  
		Last Modified: Mon, 29 Dec 2025 23:20:46 GMT  
		Size: 2.2 MB (2163975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0f315cda938284ce51afa280bd8e89b891448b2da00c28c66c638c2d4a4cc6`  
		Last Modified: Mon, 29 Dec 2025 23:20:45 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c38a3204b12ac8ee46611fe38ab1a706ee2c310f8a4e0439862ee702d7b5481c`  
		Last Modified: Mon, 29 Dec 2025 23:20:45 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:4c6e114c037bf19003547b10ffc5b077c88be25cd990cd30d1f26945409bf69c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5de9929189cfe8912f0ebace1f73497b21396b8561e62dab4d98cefa02760f10`

```dockerfile
```

-	Layers:
	-	`sha256:1bc6b02786844de8506e80bae2bf850ea8bf7875761b0a8ff17497e18e297086`  
		Last Modified: Tue, 30 Dec 2025 04:34:58 GMT  
		Size: 2.0 MB (2009688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48de2da0a0a924a9a938d6ea9a12b2eb727da5a33bad6987e74e57dcfdc66f51`  
		Last Modified: Tue, 30 Dec 2025 04:34:59 GMT  
		Size: 22.3 KB (22303 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:517aefb9e9ff071c2aa387ca68e1b63663f210c5bc838b8d928cb657795329fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32554923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20bd9e6ac4a3626ae8b8108e846570938ea003859e516dcd2134d2d628fd2c79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:21:52 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 29 Dec 2025 23:21:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:24:52 GMT
ENV MEMCACHED_VERSION=1.6.40
# Mon, 29 Dec 2025 23:24:52 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Mon, 29 Dec 2025 23:24:52 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Mon, 29 Dec 2025 23:24:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 29 Dec 2025 23:24:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:24:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 29 Dec 2025 23:24:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:24:52 GMT
USER memcache
# Mon, 29 Dec 2025 23:24:52 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 29 Dec 2025 23:24:52 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d74ee4724223b1c44d3bdff5ee6ee8c7eceabc636fe61128ec308914b5999f8`  
		Last Modified: Mon, 29 Dec 2025 23:25:06 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d74224a341d3e408a0affb0b0eb0c53f99939a1b669f25e6b34026f224a3745`  
		Last Modified: Mon, 29 Dec 2025 23:25:06 GMT  
		Size: 153.5 KB (153455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5db3b7f17de3125f5608801faf4e6a1615d96c6be2fa7f1c09e52d0cd7cd80`  
		Last Modified: Mon, 29 Dec 2025 23:25:06 GMT  
		Size: 2.3 MB (2261324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885dc482553144838528b69fa53518cc1fafb03d7eac91e773730285029e30e9`  
		Last Modified: Mon, 29 Dec 2025 23:25:06 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8afa8cb30ddae48c82fab84d30d0457bfa667059caff286dcfc57999e07a8b1`  
		Last Modified: Mon, 29 Dec 2025 23:25:06 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:62c7db64a99cd405d4330dc5c878884ef8a0e107864d7314a4cb66a8242b7dee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cfb248343584b4b08d6f7b363daf97f9506e303159317383e87ae5b82750335`

```dockerfile
```

-	Layers:
	-	`sha256:f38f799c754160125bc6daafe2fc1bd335001b11d94be74b560069268f8246e4`  
		Last Modified: Tue, 30 Dec 2025 04:35:02 GMT  
		Size: 2.0 MB (2008544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad51b10b5d6e7e377d3219a2f60c17ba2d754739a985c052724e0826650144fc`  
		Last Modified: Tue, 30 Dec 2025 04:35:03 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; 386

```console
$ docker pull memcached@sha256:0be60a562cdf0c05ebc768c0de49cf333584a650766b962f308610539a885a4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33665696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7b7c835420cd1e7ae8cd0eb0b0df1b2020c581061f1938dfa5292723e395058`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:17:02 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 29 Dec 2025 23:17:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:19:58 GMT
ENV MEMCACHED_VERSION=1.6.40
# Mon, 29 Dec 2025 23:19:58 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Mon, 29 Dec 2025 23:19:58 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Mon, 29 Dec 2025 23:19:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 29 Dec 2025 23:19:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:19:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 29 Dec 2025 23:19:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:19:58 GMT
USER memcache
# Mon, 29 Dec 2025 23:19:58 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 29 Dec 2025 23:19:58 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:796ffff142a3158a5c48a8d81b8b722c5cf4889d5e22da70bdd13a6459d6e40b`  
		Last Modified: Mon, 29 Dec 2025 22:27:31 GMT  
		Size: 31.3 MB (31293100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8fc762766a28f1d89093cb569234311423930c02de910408e80cad47e30647`  
		Last Modified: Mon, 29 Dec 2025 23:20:11 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b725b75ef28bdf7d63e19355a971dc87c6501efa1f70edbee592d52e763fee94`  
		Last Modified: Mon, 29 Dec 2025 23:20:11 GMT  
		Size: 147.5 KB (147508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9509121c0551cdeef95fef92e5598954065e802767669466cffb6c8dada5c3`  
		Last Modified: Mon, 29 Dec 2025 23:20:11 GMT  
		Size: 2.2 MB (2223574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f6e90b6aa0c5dbad71d717fad6007d2dfc7dbc186fa2c07eb8ce8416168801`  
		Last Modified: Mon, 29 Dec 2025 23:20:11 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4fa5d83d611a53674f14bb3fea7ff4465d235101cd9c5640e6c822413b3f4e`  
		Last Modified: Mon, 29 Dec 2025 23:20:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:2f28d2975c37dc6c21579400a4d8a911f45c78e460466164e094c3b114a8a739
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b72a726f712c69433343b634304351532be5cd25051c5bba2f1842cbe52c9fd`

```dockerfile
```

-	Layers:
	-	`sha256:0b522eb7b1ed969865d6941e83230cfad34490504dd209cdf0a9574b09a02415`  
		Last Modified: Tue, 30 Dec 2025 04:35:06 GMT  
		Size: 2.0 MB (2005385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9244708212b7f5f5094918a876558a69b2ba5df9e6a6187f1f97b3dd699465a`  
		Last Modified: Tue, 30 Dec 2025 04:35:08 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; ppc64le

```console
$ docker pull memcached@sha256:38a236f83eb206f786b39c53e8f756815f0bda1460157b11844faf21735208bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36162589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d41292f5c75fe5f3a464b809bde41e0ae8849ad8d7046918a548d0c6b2e250a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 21:34:54 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 17 Dec 2025 21:35:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:28 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:28 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:28 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ddd908d99c8b32da8685339ba6296773100f66e08c8bf508ab82174ba5a4f600`  
		Last Modified: Tue, 09 Dec 2025 00:06:51 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d2b42546c7b688160cfd1a0da61a24922a019b4ebead88e23aff01482ddd477`  
		Last Modified: Wed, 17 Dec 2025 21:38:49 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4efe9fd2e012174cd86a64f83d7b7facfe14ee67c9c9fa5ce994f22c24173f2c`  
		Last Modified: Wed, 17 Dec 2025 21:38:49 GMT  
		Size: 170.4 KB (170393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9752985ba696f0f8d5831ac91e19bfe336342b1c403542641c575b1dc6116e`  
		Last Modified: Wed, 17 Dec 2025 21:38:49 GMT  
		Size: 2.4 MB (2393786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d11c68ba0bc913d139eea51cb2957c1ddd713515fc06dfa5d4c398b119535a`  
		Last Modified: Wed, 17 Dec 2025 21:38:49 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9186b8b7184cef442ae3ed6a3feadcaa8f4ccc974ed5ae6c6cf8efe37e679f23`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:00d1019e9978171df76f638253f212405bf7d53251607ef5a5933d5b28d867b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:588d3d6ab54a9ea5c8baf9b013bb23c12826989ba0d09cb862431e2fa30e5189`

```dockerfile
```

-	Layers:
	-	`sha256:799ad025578a6d5d0155dc5be223bfbc25ffa3aa0548e4fb2e4bedeb0a5088d9`  
		Last Modified: Wed, 17 Dec 2025 22:35:03 GMT  
		Size: 2.0 MB (2011829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eaa03114ccb63fbbd8ca04eef46baa26c8a0508f1256aa45d851f3a49f2ed47a`  
		Last Modified: Wed, 17 Dec 2025 22:35:04 GMT  
		Size: 22.2 KB (22225 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; riscv64

```console
$ docker pull memcached@sha256:30d185f5c04056622fe346fecdf9a07a4d861871fef4028424c9b38e979d2ba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30615105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6048e6bd3b428597fcae4887d0b69fb252944cd1c8afdd85045a4e4c68837ecf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 03:48:33 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 30 Dec 2025 03:49:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 04:02:23 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 30 Dec 2025 04:02:23 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 30 Dec 2025 04:02:23 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 30 Dec 2025 04:02:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 30 Dec 2025 04:02:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Dec 2025 04:02:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 30 Dec 2025 04:02:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Dec 2025 04:02:23 GMT
USER memcache
# Tue, 30 Dec 2025 04:02:23 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 30 Dec 2025 04:02:23 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:96d8ad310358e2403b7b44cf38db606dc1ea6b58b915684d38e13f573860f64e`  
		Last Modified: Tue, 30 Dec 2025 00:53:22 GMT  
		Size: 28.3 MB (28273129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d30361332d6c36fa201043e1df585bb5cea535dfbf760f9b2ed1827c4a53ac`  
		Last Modified: Tue, 30 Dec 2025 04:03:16 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe44badb419e8d40ff093c52477fa45ed79bb9d483ed2f517359e5583617d73a`  
		Last Modified: Tue, 30 Dec 2025 04:03:17 GMT  
		Size: 133.1 KB (133088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a36426c8facdb7304fc9999aee0ca442e6e3b75be15714fa9cadff5589e57f20`  
		Last Modified: Tue, 30 Dec 2025 04:03:16 GMT  
		Size: 2.2 MB (2207375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7820ce69e6809e314e3ef1cf5cc6d3c2bafcd597d9eaf7f0f491c3ea69249db`  
		Last Modified: Tue, 30 Dec 2025 04:03:16 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc77699b8548736e5d2fa9873720c2f41ddfbc89354a6f902b7e5b5651ad0135`  
		Last Modified: Tue, 30 Dec 2025 04:03:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:7f4ca8337c70973f8b5a8eb90158eacfc3a792f5af42d7edf68da0a3a4846cd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a70852a9b9663c0d61ac529b72228ba271972017a65a149b4af634dadda75c5b`

```dockerfile
```

-	Layers:
	-	`sha256:45586a078529026200d6db8b774cf2db02f7292ac8bd6cfd4f8e68ddbe883e64`  
		Last Modified: Tue, 30 Dec 2025 04:35:15 GMT  
		Size: 2.0 MB (2002192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e23345b5880eafecc6509da78e5a9b8e6e95ce6050b2ecb71bb24c1aa03342e5`  
		Last Modified: Tue, 30 Dec 2025 04:35:15 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; s390x

```console
$ docker pull memcached@sha256:e513e62f8a86f2c8f23e06b9b73d141d7e53163ab557ec297be5f3c682a70bc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32273670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd4c0f39122c5c6e9cb01d08aebb1281a0ce18244cbc1e051742de47c5bd51f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:17:26 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 29 Dec 2025 23:17:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:20:38 GMT
ENV MEMCACHED_VERSION=1.6.40
# Mon, 29 Dec 2025 23:20:38 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Mon, 29 Dec 2025 23:20:38 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Mon, 29 Dec 2025 23:20:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 29 Dec 2025 23:20:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:20:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 29 Dec 2025 23:20:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:20:38 GMT
USER memcache
# Mon, 29 Dec 2025 23:20:38 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 29 Dec 2025 23:20:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c9a83915f7d4b9d7fbe5dceeedd49718d2702fd67d78b63a38ec344f3fbfcc41`  
		Last Modified: Mon, 29 Dec 2025 22:27:07 GMT  
		Size: 29.8 MB (29834418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1fd9e99d807cb897b4653efa7815d408df0bb7175d7fb89ab19b79b7737dc1d`  
		Last Modified: Mon, 29 Dec 2025 23:20:55 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7251a4bef45871483e5419196b0bd7ee7440a6dcc98993bd541eb9cf6ee89b06`  
		Last Modified: Mon, 29 Dec 2025 23:20:55 GMT  
		Size: 140.5 KB (140511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16461f97f95d5d1b2cb64bc91ad5a73d23e505f74a1cf95eeb9de840c9a06488`  
		Last Modified: Mon, 29 Dec 2025 23:20:55 GMT  
		Size: 2.3 MB (2297231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa6eecd4b590cab77eae19d421ebb50ce6ed90281723d604c775bcb78b5408f`  
		Last Modified: Mon, 29 Dec 2025 23:20:55 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2779e4a3a9763cc09cc4694ec9a5b304164f44aa2869a8ccbca67eeca523c305`  
		Last Modified: Mon, 29 Dec 2025 23:20:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:89b3d47f58bd28d04b77c9a4cb6634d06120bc2fa943508ae1125915480f511e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b70d80ce63a4423c1c153bdb4d489ec092debf0f20017e21d47e05ed147b71d9`

```dockerfile
```

-	Layers:
	-	`sha256:0be1a3049197ac03e690e9365edd513ffeb121d05d4b6883a58c6356f44ce72f`  
		Last Modified: Tue, 30 Dec 2025 01:35:29 GMT  
		Size: 2.0 MB (2009665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4be7a57b181c7a7314b420b859583bfaa463e17fc94b8f57edc563abf95a3257`  
		Last Modified: Tue, 30 Dec 2025 01:35:30 GMT  
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
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57c33ac8581cd04f31208409f36331e938a78e6ae3a7a3b530fe9dfebe6eb9ad`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583aae99135b9036c602a1c60743fc4fd519f261ac6d48ed60b01e1beb019e7f`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 106.0 KB (106050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ca22885c42a537f033850e8dff7eaeddbb7514902286739b48c084b55a8d6b`  
		Last Modified: Thu, 18 Dec 2025 00:32:19 GMT  
		Size: 2.0 MB (1989265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d146e2038834770bed57033a6c5d66ead5b731b8b133856dec6726ca21baee9`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
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
		Last Modified: Thu, 18 Dec 2025 01:34:48 GMT  
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
		Last Modified: Thu, 18 Dec 2025 00:50:01 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01bb148ea8fbe93dd8097d85f9ee3cf547d314e669748b4239c05711b0d5f719`  
		Last Modified: Thu, 18 Dec 2025 00:50:02 GMT  
		Size: 102.7 KB (102652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6549359cda37ac41cf41a5ece5f37f1322a82f6b232f12e446c62840637093e`  
		Last Modified: Thu, 18 Dec 2025 00:50:02 GMT  
		Size: 1.9 MB (1939215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:041e37eaffefcfb0809564ddea591be3cd818de5530e2c853c0bc9a2fa25c116`  
		Last Modified: Thu, 18 Dec 2025 00:50:05 GMT  
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
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 1.9 MB (1897191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f237be962bb57c3f749904b5925c8e1d7e9013dfac7dd52cc9611ada81858e`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
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
		Last Modified: Thu, 18 Dec 2025 01:34:55 GMT  
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
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb7b8445facedfc145b9478f74880f520776460f153005b7f437ec339aee530`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1853c901134389608b6e80aaa3e43cd67a35c71aecfdde4b5b7ed3b989a03c`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 121.9 KB (121860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a01d1ac5ce47f4494363e411e1cd25dea26438213a2d18d6bb104d0974d9a52`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 2.0 MB (1966561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115624f24ba74d393c2da3d65ed5b35a7afb3fa9ad143d3fb82c64953b3d0401`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87bba524314294ca97195ce65a35ec6d42d3f9f18c9cc0c05c064c9a3cf85c0`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
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
		Last Modified: Thu, 18 Dec 2025 00:32:41 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b2862af05c1582c8625c82ea0863dc2b6474e410d3e6a32876c920e0152c73`  
		Last Modified: Thu, 18 Dec 2025 00:32:42 GMT  
		Size: 110.7 KB (110740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30872a43f6c591fd9b979b49b0fb32107b4bfa8c1155657fa255aa199cf0b83b`  
		Last Modified: Thu, 18 Dec 2025 00:32:42 GMT  
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
		Last Modified: Thu, 18 Dec 2025 01:35:04 GMT  
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
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4079a2d61bafcf146b8f57b35f0e39bf2548e0963be10cff5086f9a56ccdd9d`  
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
		Size: 126.3 KB (126257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f69efa1066815d67cf415d0aac5dcd305032257b6bded5a4c57a7444a1e7fd4`  
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
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
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f270744f8d8b82bc6657387109b33836a76d6dbf8faa645a997db7ea290cdb`  
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
		Size: 114.3 KB (114299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91f8ee8f36703944a7bdcaf57cc5772fe9f79c74a088c33fa1b6da7de119f93`  
		Last Modified: Thu, 18 Dec 2025 00:34:02 GMT  
		Size: 2.0 MB (2017131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e21d2db88668745770273c7b36d4d2c1e87a80b0118b8d775813860b467384c8`  
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd847159e169b898a67d4454fd5a22406c5ae623b16889d084a1d5f2d46a499`  
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
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
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57c33ac8581cd04f31208409f36331e938a78e6ae3a7a3b530fe9dfebe6eb9ad`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583aae99135b9036c602a1c60743fc4fd519f261ac6d48ed60b01e1beb019e7f`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 106.0 KB (106050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ca22885c42a537f033850e8dff7eaeddbb7514902286739b48c084b55a8d6b`  
		Last Modified: Thu, 18 Dec 2025 00:32:19 GMT  
		Size: 2.0 MB (1989265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d146e2038834770bed57033a6c5d66ead5b731b8b133856dec6726ca21baee9`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
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
		Last Modified: Thu, 18 Dec 2025 01:34:48 GMT  
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
		Last Modified: Thu, 18 Dec 2025 00:50:01 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01bb148ea8fbe93dd8097d85f9ee3cf547d314e669748b4239c05711b0d5f719`  
		Last Modified: Thu, 18 Dec 2025 00:50:02 GMT  
		Size: 102.7 KB (102652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6549359cda37ac41cf41a5ece5f37f1322a82f6b232f12e446c62840637093e`  
		Last Modified: Thu, 18 Dec 2025 00:50:02 GMT  
		Size: 1.9 MB (1939215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:041e37eaffefcfb0809564ddea591be3cd818de5530e2c853c0bc9a2fa25c116`  
		Last Modified: Thu, 18 Dec 2025 00:50:05 GMT  
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
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 1.9 MB (1897191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f237be962bb57c3f749904b5925c8e1d7e9013dfac7dd52cc9611ada81858e`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
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
		Last Modified: Thu, 18 Dec 2025 01:34:55 GMT  
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
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb7b8445facedfc145b9478f74880f520776460f153005b7f437ec339aee530`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1853c901134389608b6e80aaa3e43cd67a35c71aecfdde4b5b7ed3b989a03c`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 121.9 KB (121860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a01d1ac5ce47f4494363e411e1cd25dea26438213a2d18d6bb104d0974d9a52`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 2.0 MB (1966561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115624f24ba74d393c2da3d65ed5b35a7afb3fa9ad143d3fb82c64953b3d0401`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87bba524314294ca97195ce65a35ec6d42d3f9f18c9cc0c05c064c9a3cf85c0`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
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
		Last Modified: Thu, 18 Dec 2025 00:32:41 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b2862af05c1582c8625c82ea0863dc2b6474e410d3e6a32876c920e0152c73`  
		Last Modified: Thu, 18 Dec 2025 00:32:42 GMT  
		Size: 110.7 KB (110740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30872a43f6c591fd9b979b49b0fb32107b4bfa8c1155657fa255aa199cf0b83b`  
		Last Modified: Thu, 18 Dec 2025 00:32:42 GMT  
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
		Last Modified: Thu, 18 Dec 2025 01:35:04 GMT  
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
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4079a2d61bafcf146b8f57b35f0e39bf2548e0963be10cff5086f9a56ccdd9d`  
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
		Size: 126.3 KB (126257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f69efa1066815d67cf415d0aac5dcd305032257b6bded5a4c57a7444a1e7fd4`  
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
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
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f270744f8d8b82bc6657387109b33836a76d6dbf8faa645a997db7ea290cdb`  
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
		Size: 114.3 KB (114299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91f8ee8f36703944a7bdcaf57cc5772fe9f79c74a088c33fa1b6da7de119f93`  
		Last Modified: Thu, 18 Dec 2025 00:34:02 GMT  
		Size: 2.0 MB (2017131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e21d2db88668745770273c7b36d4d2c1e87a80b0118b8d775813860b467384c8`  
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd847159e169b898a67d4454fd5a22406c5ae623b16889d084a1d5f2d46a499`  
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
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
$ docker pull memcached@sha256:36c36f0c38cda62ab29af64a0eefa53e99879265ff70df8ac12597be28c482f7
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
$ docker pull memcached@sha256:61bcd214c8da24f2bacfd9152bccafef4f4c0993897c945ee3058106e084b314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32193395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5dafc7d411a870fbc52ca64194006e50e355d34f1edf56b4e1dc5b8019b0934`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:21:34 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 29 Dec 2025 23:21:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:24:22 GMT
ENV MEMCACHED_VERSION=1.6.40
# Mon, 29 Dec 2025 23:24:22 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Mon, 29 Dec 2025 23:24:22 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Mon, 29 Dec 2025 23:24:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 29 Dec 2025 23:24:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:24:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 29 Dec 2025 23:24:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:24:22 GMT
USER memcache
# Mon, 29 Dec 2025 23:24:22 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 29 Dec 2025 23:24:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d08d8001380dd7c5a9be2e59244310ccfa7e84f3b896b354059d46d1928401`  
		Last Modified: Mon, 29 Dec 2025 23:24:36 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8420bae5d2af8b5b5e66d7e5ba882f5e2034cc64eacfb1a0b4b32a259a541b16`  
		Last Modified: Mon, 29 Dec 2025 23:24:35 GMT  
		Size: 136.7 KB (136694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc2daf1b2287468ea06570c5bedff8bc84ab6833050a7e0686f5f7d7a2679e1`  
		Last Modified: Mon, 29 Dec 2025 23:24:35 GMT  
		Size: 2.3 MB (2278657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a54c348dd92d8a79d150c1fe56008dba798b633f010e1e57c0a18f62b2752d90`  
		Last Modified: Mon, 29 Dec 2025 23:24:35 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e147936d0f858c8f726dea003b7220347e43918cab2714f81c66c1553cc160cd`  
		Last Modified: Mon, 29 Dec 2025 23:24:35 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:e6d0cef74a4a91255f97601317c1cd45953291e56aebea597b1f5fedb87772df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a114559b11eef9830f21c5cfd0b3dff0712acd507604d89ab89f16d229d637c`

```dockerfile
```

-	Layers:
	-	`sha256:31d77d05cfee83189fed485cbb6de83d56b3fc5c8a37eafd4e5ab2a8646bcee5`  
		Last Modified: Tue, 30 Dec 2025 04:34:52 GMT  
		Size: 2.0 MB (2008228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:daae5d64f19c0b653f152172ab207032a103d7a2c198208a2472a4565869c64e`  
		Last Modified: Tue, 30 Dec 2025 04:34:53 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; arm variant v5

```console
$ docker pull memcached@sha256:19778ab8ffe04b579956362255d1b4be4646df675a0c0db5662d882e7e062834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30300227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85e834ef35584236d3b04d1823e406899096de386d548c5f0bfd896cfba41631`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:17:23 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 29 Dec 2025 23:17:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:39:32 GMT
ENV MEMCACHED_VERSION=1.6.40
# Mon, 29 Dec 2025 23:39:32 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Mon, 29 Dec 2025 23:39:32 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Mon, 29 Dec 2025 23:39:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 29 Dec 2025 23:39:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:39:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 29 Dec 2025 23:39:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:39:32 GMT
USER memcache
# Mon, 29 Dec 2025 23:39:32 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 29 Dec 2025 23:39:32 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b99a8d8dab982a1a4ea341e66b178b14c0f373c2cd90ac46a67308a4f43c82ae`  
		Last Modified: Mon, 29 Dec 2025 22:27:09 GMT  
		Size: 27.9 MB (27944146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0be68f37541245f1acaee607441dfc983a00e90d78d5e0941265d0b67b1cc9a`  
		Last Modified: Mon, 29 Dec 2025 23:39:44 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10905a7698a57312678edda9f8fc0748b6288699f5fed1f8e7e7e909240d441`  
		Last Modified: Mon, 29 Dec 2025 23:39:44 GMT  
		Size: 144.1 KB (144149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea062eb6d6681b78497a81a8d5ca89088b56f5a5d629e3124df93b9ca0e4f16`  
		Last Modified: Mon, 29 Dec 2025 23:39:44 GMT  
		Size: 2.2 MB (2210419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d59770b8679e935091911e6294f61a53df8f59b5cc8aae431217cc391864a0`  
		Last Modified: Mon, 29 Dec 2025 23:39:44 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945c1d27fa6617071d97eddd3d962ac571276f7f757f99edc1a93ebbe6eb5a9c`  
		Last Modified: Mon, 29 Dec 2025 23:39:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:27e3afeed14c4cac078a10db01ef22eef58848fc65d93501050f872bc3cf64d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:939368d93857b65d5e6bbdc97a5f4d158eeca9efc9fb02875eae93350ea663fb`

```dockerfile
```

-	Layers:
	-	`sha256:3559f8384ca294c984900b7325032abfe47459734f215e79264a22aa23802031`  
		Last Modified: Tue, 30 Dec 2025 01:35:12 GMT  
		Size: 2.0 MB (2011231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b310c8a994e22e59ca814cd06500201d5b78c4bbfe3baa8785ae093760d4a4fb`  
		Last Modified: Tue, 30 Dec 2025 01:35:13 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; arm variant v7

```console
$ docker pull memcached@sha256:34f932820fcffc223d050d31ceeef236f4bc4a1a8e776006560fe2ef14348a2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28510848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0a0c32503881f91ec515af1fd074032b8070eac0faa4afca5e1f2f60609b237`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:17:22 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 29 Dec 2025 23:17:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:20:31 GMT
ENV MEMCACHED_VERSION=1.6.40
# Mon, 29 Dec 2025 23:20:31 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Mon, 29 Dec 2025 23:20:31 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Mon, 29 Dec 2025 23:20:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 29 Dec 2025 23:20:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:20:31 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 29 Dec 2025 23:20:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:20:31 GMT
USER memcache
# Mon, 29 Dec 2025 23:20:31 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 29 Dec 2025 23:20:31 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6d3e0fea3cb8eb29b9c06956265b47cd00f7ebfb48e35e818f686d52c21353f5`  
		Last Modified: Mon, 29 Dec 2025 22:28:07 GMT  
		Size: 26.2 MB (26210001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f916949d5244227fca363e62638c31c65e0f6a941ceaa0fb79c37d962e9b95bb`  
		Last Modified: Mon, 29 Dec 2025 23:20:45 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f24598f250037f41edf0d0093ed08f2b3b3937f91d7708c687330e0feca3fdcf`  
		Last Modified: Mon, 29 Dec 2025 23:20:45 GMT  
		Size: 135.4 KB (135362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f260cb2adbfa9ad1d74da541da12d2146b1a06685021b42e924c843481237ee2`  
		Last Modified: Mon, 29 Dec 2025 23:20:46 GMT  
		Size: 2.2 MB (2163975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0f315cda938284ce51afa280bd8e89b891448b2da00c28c66c638c2d4a4cc6`  
		Last Modified: Mon, 29 Dec 2025 23:20:45 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c38a3204b12ac8ee46611fe38ab1a706ee2c310f8a4e0439862ee702d7b5481c`  
		Last Modified: Mon, 29 Dec 2025 23:20:45 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:4c6e114c037bf19003547b10ffc5b077c88be25cd990cd30d1f26945409bf69c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5de9929189cfe8912f0ebace1f73497b21396b8561e62dab4d98cefa02760f10`

```dockerfile
```

-	Layers:
	-	`sha256:1bc6b02786844de8506e80bae2bf850ea8bf7875761b0a8ff17497e18e297086`  
		Last Modified: Tue, 30 Dec 2025 04:34:58 GMT  
		Size: 2.0 MB (2009688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48de2da0a0a924a9a938d6ea9a12b2eb727da5a33bad6987e74e57dcfdc66f51`  
		Last Modified: Tue, 30 Dec 2025 04:34:59 GMT  
		Size: 22.3 KB (22303 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:517aefb9e9ff071c2aa387ca68e1b63663f210c5bc838b8d928cb657795329fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32554923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20bd9e6ac4a3626ae8b8108e846570938ea003859e516dcd2134d2d628fd2c79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:21:52 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 29 Dec 2025 23:21:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:24:52 GMT
ENV MEMCACHED_VERSION=1.6.40
# Mon, 29 Dec 2025 23:24:52 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Mon, 29 Dec 2025 23:24:52 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Mon, 29 Dec 2025 23:24:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 29 Dec 2025 23:24:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:24:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 29 Dec 2025 23:24:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:24:52 GMT
USER memcache
# Mon, 29 Dec 2025 23:24:52 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 29 Dec 2025 23:24:52 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d74ee4724223b1c44d3bdff5ee6ee8c7eceabc636fe61128ec308914b5999f8`  
		Last Modified: Mon, 29 Dec 2025 23:25:06 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d74224a341d3e408a0affb0b0eb0c53f99939a1b669f25e6b34026f224a3745`  
		Last Modified: Mon, 29 Dec 2025 23:25:06 GMT  
		Size: 153.5 KB (153455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5db3b7f17de3125f5608801faf4e6a1615d96c6be2fa7f1c09e52d0cd7cd80`  
		Last Modified: Mon, 29 Dec 2025 23:25:06 GMT  
		Size: 2.3 MB (2261324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885dc482553144838528b69fa53518cc1fafb03d7eac91e773730285029e30e9`  
		Last Modified: Mon, 29 Dec 2025 23:25:06 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8afa8cb30ddae48c82fab84d30d0457bfa667059caff286dcfc57999e07a8b1`  
		Last Modified: Mon, 29 Dec 2025 23:25:06 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:62c7db64a99cd405d4330dc5c878884ef8a0e107864d7314a4cb66a8242b7dee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cfb248343584b4b08d6f7b363daf97f9506e303159317383e87ae5b82750335`

```dockerfile
```

-	Layers:
	-	`sha256:f38f799c754160125bc6daafe2fc1bd335001b11d94be74b560069268f8246e4`  
		Last Modified: Tue, 30 Dec 2025 04:35:02 GMT  
		Size: 2.0 MB (2008544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad51b10b5d6e7e377d3219a2f60c17ba2d754739a985c052724e0826650144fc`  
		Last Modified: Tue, 30 Dec 2025 04:35:03 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; 386

```console
$ docker pull memcached@sha256:0be60a562cdf0c05ebc768c0de49cf333584a650766b962f308610539a885a4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33665696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7b7c835420cd1e7ae8cd0eb0b0df1b2020c581061f1938dfa5292723e395058`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:17:02 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 29 Dec 2025 23:17:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:19:58 GMT
ENV MEMCACHED_VERSION=1.6.40
# Mon, 29 Dec 2025 23:19:58 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Mon, 29 Dec 2025 23:19:58 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Mon, 29 Dec 2025 23:19:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 29 Dec 2025 23:19:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:19:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 29 Dec 2025 23:19:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:19:58 GMT
USER memcache
# Mon, 29 Dec 2025 23:19:58 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 29 Dec 2025 23:19:58 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:796ffff142a3158a5c48a8d81b8b722c5cf4889d5e22da70bdd13a6459d6e40b`  
		Last Modified: Mon, 29 Dec 2025 22:27:31 GMT  
		Size: 31.3 MB (31293100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8fc762766a28f1d89093cb569234311423930c02de910408e80cad47e30647`  
		Last Modified: Mon, 29 Dec 2025 23:20:11 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b725b75ef28bdf7d63e19355a971dc87c6501efa1f70edbee592d52e763fee94`  
		Last Modified: Mon, 29 Dec 2025 23:20:11 GMT  
		Size: 147.5 KB (147508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9509121c0551cdeef95fef92e5598954065e802767669466cffb6c8dada5c3`  
		Last Modified: Mon, 29 Dec 2025 23:20:11 GMT  
		Size: 2.2 MB (2223574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f6e90b6aa0c5dbad71d717fad6007d2dfc7dbc186fa2c07eb8ce8416168801`  
		Last Modified: Mon, 29 Dec 2025 23:20:11 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4fa5d83d611a53674f14bb3fea7ff4465d235101cd9c5640e6c822413b3f4e`  
		Last Modified: Mon, 29 Dec 2025 23:20:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:2f28d2975c37dc6c21579400a4d8a911f45c78e460466164e094c3b114a8a739
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b72a726f712c69433343b634304351532be5cd25051c5bba2f1842cbe52c9fd`

```dockerfile
```

-	Layers:
	-	`sha256:0b522eb7b1ed969865d6941e83230cfad34490504dd209cdf0a9574b09a02415`  
		Last Modified: Tue, 30 Dec 2025 04:35:06 GMT  
		Size: 2.0 MB (2005385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9244708212b7f5f5094918a876558a69b2ba5df9e6a6187f1f97b3dd699465a`  
		Last Modified: Tue, 30 Dec 2025 04:35:08 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; ppc64le

```console
$ docker pull memcached@sha256:38a236f83eb206f786b39c53e8f756815f0bda1460157b11844faf21735208bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36162589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d41292f5c75fe5f3a464b809bde41e0ae8849ad8d7046918a548d0c6b2e250a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 21:34:54 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 17 Dec 2025 21:35:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:28 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:28 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:28 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ddd908d99c8b32da8685339ba6296773100f66e08c8bf508ab82174ba5a4f600`  
		Last Modified: Tue, 09 Dec 2025 00:06:51 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d2b42546c7b688160cfd1a0da61a24922a019b4ebead88e23aff01482ddd477`  
		Last Modified: Wed, 17 Dec 2025 21:38:49 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4efe9fd2e012174cd86a64f83d7b7facfe14ee67c9c9fa5ce994f22c24173f2c`  
		Last Modified: Wed, 17 Dec 2025 21:38:49 GMT  
		Size: 170.4 KB (170393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9752985ba696f0f8d5831ac91e19bfe336342b1c403542641c575b1dc6116e`  
		Last Modified: Wed, 17 Dec 2025 21:38:49 GMT  
		Size: 2.4 MB (2393786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d11c68ba0bc913d139eea51cb2957c1ddd713515fc06dfa5d4c398b119535a`  
		Last Modified: Wed, 17 Dec 2025 21:38:49 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9186b8b7184cef442ae3ed6a3feadcaa8f4ccc974ed5ae6c6cf8efe37e679f23`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:00d1019e9978171df76f638253f212405bf7d53251607ef5a5933d5b28d867b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:588d3d6ab54a9ea5c8baf9b013bb23c12826989ba0d09cb862431e2fa30e5189`

```dockerfile
```

-	Layers:
	-	`sha256:799ad025578a6d5d0155dc5be223bfbc25ffa3aa0548e4fb2e4bedeb0a5088d9`  
		Last Modified: Wed, 17 Dec 2025 22:35:03 GMT  
		Size: 2.0 MB (2011829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eaa03114ccb63fbbd8ca04eef46baa26c8a0508f1256aa45d851f3a49f2ed47a`  
		Last Modified: Wed, 17 Dec 2025 22:35:04 GMT  
		Size: 22.2 KB (22225 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; riscv64

```console
$ docker pull memcached@sha256:30d185f5c04056622fe346fecdf9a07a4d861871fef4028424c9b38e979d2ba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30615105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6048e6bd3b428597fcae4887d0b69fb252944cd1c8afdd85045a4e4c68837ecf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 03:48:33 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 30 Dec 2025 03:49:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 04:02:23 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 30 Dec 2025 04:02:23 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 30 Dec 2025 04:02:23 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 30 Dec 2025 04:02:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 30 Dec 2025 04:02:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Dec 2025 04:02:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 30 Dec 2025 04:02:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Dec 2025 04:02:23 GMT
USER memcache
# Tue, 30 Dec 2025 04:02:23 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 30 Dec 2025 04:02:23 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:96d8ad310358e2403b7b44cf38db606dc1ea6b58b915684d38e13f573860f64e`  
		Last Modified: Tue, 30 Dec 2025 00:53:22 GMT  
		Size: 28.3 MB (28273129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d30361332d6c36fa201043e1df585bb5cea535dfbf760f9b2ed1827c4a53ac`  
		Last Modified: Tue, 30 Dec 2025 04:03:16 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe44badb419e8d40ff093c52477fa45ed79bb9d483ed2f517359e5583617d73a`  
		Last Modified: Tue, 30 Dec 2025 04:03:17 GMT  
		Size: 133.1 KB (133088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a36426c8facdb7304fc9999aee0ca442e6e3b75be15714fa9cadff5589e57f20`  
		Last Modified: Tue, 30 Dec 2025 04:03:16 GMT  
		Size: 2.2 MB (2207375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7820ce69e6809e314e3ef1cf5cc6d3c2bafcd597d9eaf7f0f491c3ea69249db`  
		Last Modified: Tue, 30 Dec 2025 04:03:16 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc77699b8548736e5d2fa9873720c2f41ddfbc89354a6f902b7e5b5651ad0135`  
		Last Modified: Tue, 30 Dec 2025 04:03:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:7f4ca8337c70973f8b5a8eb90158eacfc3a792f5af42d7edf68da0a3a4846cd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a70852a9b9663c0d61ac529b72228ba271972017a65a149b4af634dadda75c5b`

```dockerfile
```

-	Layers:
	-	`sha256:45586a078529026200d6db8b774cf2db02f7292ac8bd6cfd4f8e68ddbe883e64`  
		Last Modified: Tue, 30 Dec 2025 04:35:15 GMT  
		Size: 2.0 MB (2002192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e23345b5880eafecc6509da78e5a9b8e6e95ce6050b2ecb71bb24c1aa03342e5`  
		Last Modified: Tue, 30 Dec 2025 04:35:15 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; s390x

```console
$ docker pull memcached@sha256:e513e62f8a86f2c8f23e06b9b73d141d7e53163ab557ec297be5f3c682a70bc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32273670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd4c0f39122c5c6e9cb01d08aebb1281a0ce18244cbc1e051742de47c5bd51f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:17:26 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 29 Dec 2025 23:17:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:20:38 GMT
ENV MEMCACHED_VERSION=1.6.40
# Mon, 29 Dec 2025 23:20:38 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Mon, 29 Dec 2025 23:20:38 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Mon, 29 Dec 2025 23:20:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 29 Dec 2025 23:20:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:20:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 29 Dec 2025 23:20:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:20:38 GMT
USER memcache
# Mon, 29 Dec 2025 23:20:38 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 29 Dec 2025 23:20:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c9a83915f7d4b9d7fbe5dceeedd49718d2702fd67d78b63a38ec344f3fbfcc41`  
		Last Modified: Mon, 29 Dec 2025 22:27:07 GMT  
		Size: 29.8 MB (29834418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1fd9e99d807cb897b4653efa7815d408df0bb7175d7fb89ab19b79b7737dc1d`  
		Last Modified: Mon, 29 Dec 2025 23:20:55 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7251a4bef45871483e5419196b0bd7ee7440a6dcc98993bd541eb9cf6ee89b06`  
		Last Modified: Mon, 29 Dec 2025 23:20:55 GMT  
		Size: 140.5 KB (140511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16461f97f95d5d1b2cb64bc91ad5a73d23e505f74a1cf95eeb9de840c9a06488`  
		Last Modified: Mon, 29 Dec 2025 23:20:55 GMT  
		Size: 2.3 MB (2297231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa6eecd4b590cab77eae19d421ebb50ce6ed90281723d604c775bcb78b5408f`  
		Last Modified: Mon, 29 Dec 2025 23:20:55 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2779e4a3a9763cc09cc4694ec9a5b304164f44aa2869a8ccbca67eeca523c305`  
		Last Modified: Mon, 29 Dec 2025 23:20:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:89b3d47f58bd28d04b77c9a4cb6634d06120bc2fa943508ae1125915480f511e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b70d80ce63a4423c1c153bdb4d489ec092debf0f20017e21d47e05ed147b71d9`

```dockerfile
```

-	Layers:
	-	`sha256:0be1a3049197ac03e690e9365edd513ffeb121d05d4b6883a58c6356f44ce72f`  
		Last Modified: Tue, 30 Dec 2025 01:35:29 GMT  
		Size: 2.0 MB (2009665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4be7a57b181c7a7314b420b859583bfaa463e17fc94b8f57edc563abf95a3257`  
		Last Modified: Tue, 30 Dec 2025 01:35:30 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6`

```console
$ docker pull memcached@sha256:36c36f0c38cda62ab29af64a0eefa53e99879265ff70df8ac12597be28c482f7
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
$ docker pull memcached@sha256:61bcd214c8da24f2bacfd9152bccafef4f4c0993897c945ee3058106e084b314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32193395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5dafc7d411a870fbc52ca64194006e50e355d34f1edf56b4e1dc5b8019b0934`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:21:34 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 29 Dec 2025 23:21:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:24:22 GMT
ENV MEMCACHED_VERSION=1.6.40
# Mon, 29 Dec 2025 23:24:22 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Mon, 29 Dec 2025 23:24:22 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Mon, 29 Dec 2025 23:24:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 29 Dec 2025 23:24:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:24:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 29 Dec 2025 23:24:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:24:22 GMT
USER memcache
# Mon, 29 Dec 2025 23:24:22 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 29 Dec 2025 23:24:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d08d8001380dd7c5a9be2e59244310ccfa7e84f3b896b354059d46d1928401`  
		Last Modified: Mon, 29 Dec 2025 23:24:36 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8420bae5d2af8b5b5e66d7e5ba882f5e2034cc64eacfb1a0b4b32a259a541b16`  
		Last Modified: Mon, 29 Dec 2025 23:24:35 GMT  
		Size: 136.7 KB (136694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc2daf1b2287468ea06570c5bedff8bc84ab6833050a7e0686f5f7d7a2679e1`  
		Last Modified: Mon, 29 Dec 2025 23:24:35 GMT  
		Size: 2.3 MB (2278657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a54c348dd92d8a79d150c1fe56008dba798b633f010e1e57c0a18f62b2752d90`  
		Last Modified: Mon, 29 Dec 2025 23:24:35 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e147936d0f858c8f726dea003b7220347e43918cab2714f81c66c1553cc160cd`  
		Last Modified: Mon, 29 Dec 2025 23:24:35 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:e6d0cef74a4a91255f97601317c1cd45953291e56aebea597b1f5fedb87772df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a114559b11eef9830f21c5cfd0b3dff0712acd507604d89ab89f16d229d637c`

```dockerfile
```

-	Layers:
	-	`sha256:31d77d05cfee83189fed485cbb6de83d56b3fc5c8a37eafd4e5ab2a8646bcee5`  
		Last Modified: Tue, 30 Dec 2025 04:34:52 GMT  
		Size: 2.0 MB (2008228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:daae5d64f19c0b653f152172ab207032a103d7a2c198208a2472a4565869c64e`  
		Last Modified: Tue, 30 Dec 2025 04:34:53 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm variant v5

```console
$ docker pull memcached@sha256:19778ab8ffe04b579956362255d1b4be4646df675a0c0db5662d882e7e062834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30300227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85e834ef35584236d3b04d1823e406899096de386d548c5f0bfd896cfba41631`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:17:23 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 29 Dec 2025 23:17:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:39:32 GMT
ENV MEMCACHED_VERSION=1.6.40
# Mon, 29 Dec 2025 23:39:32 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Mon, 29 Dec 2025 23:39:32 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Mon, 29 Dec 2025 23:39:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 29 Dec 2025 23:39:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:39:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 29 Dec 2025 23:39:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:39:32 GMT
USER memcache
# Mon, 29 Dec 2025 23:39:32 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 29 Dec 2025 23:39:32 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b99a8d8dab982a1a4ea341e66b178b14c0f373c2cd90ac46a67308a4f43c82ae`  
		Last Modified: Mon, 29 Dec 2025 22:27:09 GMT  
		Size: 27.9 MB (27944146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0be68f37541245f1acaee607441dfc983a00e90d78d5e0941265d0b67b1cc9a`  
		Last Modified: Mon, 29 Dec 2025 23:39:44 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10905a7698a57312678edda9f8fc0748b6288699f5fed1f8e7e7e909240d441`  
		Last Modified: Mon, 29 Dec 2025 23:39:44 GMT  
		Size: 144.1 KB (144149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea062eb6d6681b78497a81a8d5ca89088b56f5a5d629e3124df93b9ca0e4f16`  
		Last Modified: Mon, 29 Dec 2025 23:39:44 GMT  
		Size: 2.2 MB (2210419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d59770b8679e935091911e6294f61a53df8f59b5cc8aae431217cc391864a0`  
		Last Modified: Mon, 29 Dec 2025 23:39:44 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945c1d27fa6617071d97eddd3d962ac571276f7f757f99edc1a93ebbe6eb5a9c`  
		Last Modified: Mon, 29 Dec 2025 23:39:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:27e3afeed14c4cac078a10db01ef22eef58848fc65d93501050f872bc3cf64d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:939368d93857b65d5e6bbdc97a5f4d158eeca9efc9fb02875eae93350ea663fb`

```dockerfile
```

-	Layers:
	-	`sha256:3559f8384ca294c984900b7325032abfe47459734f215e79264a22aa23802031`  
		Last Modified: Tue, 30 Dec 2025 01:35:12 GMT  
		Size: 2.0 MB (2011231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b310c8a994e22e59ca814cd06500201d5b78c4bbfe3baa8785ae093760d4a4fb`  
		Last Modified: Tue, 30 Dec 2025 01:35:13 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm variant v7

```console
$ docker pull memcached@sha256:34f932820fcffc223d050d31ceeef236f4bc4a1a8e776006560fe2ef14348a2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28510848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0a0c32503881f91ec515af1fd074032b8070eac0faa4afca5e1f2f60609b237`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:17:22 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 29 Dec 2025 23:17:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:20:31 GMT
ENV MEMCACHED_VERSION=1.6.40
# Mon, 29 Dec 2025 23:20:31 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Mon, 29 Dec 2025 23:20:31 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Mon, 29 Dec 2025 23:20:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 29 Dec 2025 23:20:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:20:31 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 29 Dec 2025 23:20:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:20:31 GMT
USER memcache
# Mon, 29 Dec 2025 23:20:31 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 29 Dec 2025 23:20:31 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6d3e0fea3cb8eb29b9c06956265b47cd00f7ebfb48e35e818f686d52c21353f5`  
		Last Modified: Mon, 29 Dec 2025 22:28:07 GMT  
		Size: 26.2 MB (26210001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f916949d5244227fca363e62638c31c65e0f6a941ceaa0fb79c37d962e9b95bb`  
		Last Modified: Mon, 29 Dec 2025 23:20:45 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f24598f250037f41edf0d0093ed08f2b3b3937f91d7708c687330e0feca3fdcf`  
		Last Modified: Mon, 29 Dec 2025 23:20:45 GMT  
		Size: 135.4 KB (135362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f260cb2adbfa9ad1d74da541da12d2146b1a06685021b42e924c843481237ee2`  
		Last Modified: Mon, 29 Dec 2025 23:20:46 GMT  
		Size: 2.2 MB (2163975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0f315cda938284ce51afa280bd8e89b891448b2da00c28c66c638c2d4a4cc6`  
		Last Modified: Mon, 29 Dec 2025 23:20:45 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c38a3204b12ac8ee46611fe38ab1a706ee2c310f8a4e0439862ee702d7b5481c`  
		Last Modified: Mon, 29 Dec 2025 23:20:45 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:4c6e114c037bf19003547b10ffc5b077c88be25cd990cd30d1f26945409bf69c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5de9929189cfe8912f0ebace1f73497b21396b8561e62dab4d98cefa02760f10`

```dockerfile
```

-	Layers:
	-	`sha256:1bc6b02786844de8506e80bae2bf850ea8bf7875761b0a8ff17497e18e297086`  
		Last Modified: Tue, 30 Dec 2025 04:34:58 GMT  
		Size: 2.0 MB (2009688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48de2da0a0a924a9a938d6ea9a12b2eb727da5a33bad6987e74e57dcfdc66f51`  
		Last Modified: Tue, 30 Dec 2025 04:34:59 GMT  
		Size: 22.3 KB (22303 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:517aefb9e9ff071c2aa387ca68e1b63663f210c5bc838b8d928cb657795329fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32554923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20bd9e6ac4a3626ae8b8108e846570938ea003859e516dcd2134d2d628fd2c79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:21:52 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 29 Dec 2025 23:21:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:24:52 GMT
ENV MEMCACHED_VERSION=1.6.40
# Mon, 29 Dec 2025 23:24:52 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Mon, 29 Dec 2025 23:24:52 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Mon, 29 Dec 2025 23:24:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 29 Dec 2025 23:24:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:24:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 29 Dec 2025 23:24:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:24:52 GMT
USER memcache
# Mon, 29 Dec 2025 23:24:52 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 29 Dec 2025 23:24:52 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d74ee4724223b1c44d3bdff5ee6ee8c7eceabc636fe61128ec308914b5999f8`  
		Last Modified: Mon, 29 Dec 2025 23:25:06 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d74224a341d3e408a0affb0b0eb0c53f99939a1b669f25e6b34026f224a3745`  
		Last Modified: Mon, 29 Dec 2025 23:25:06 GMT  
		Size: 153.5 KB (153455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5db3b7f17de3125f5608801faf4e6a1615d96c6be2fa7f1c09e52d0cd7cd80`  
		Last Modified: Mon, 29 Dec 2025 23:25:06 GMT  
		Size: 2.3 MB (2261324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885dc482553144838528b69fa53518cc1fafb03d7eac91e773730285029e30e9`  
		Last Modified: Mon, 29 Dec 2025 23:25:06 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8afa8cb30ddae48c82fab84d30d0457bfa667059caff286dcfc57999e07a8b1`  
		Last Modified: Mon, 29 Dec 2025 23:25:06 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:62c7db64a99cd405d4330dc5c878884ef8a0e107864d7314a4cb66a8242b7dee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cfb248343584b4b08d6f7b363daf97f9506e303159317383e87ae5b82750335`

```dockerfile
```

-	Layers:
	-	`sha256:f38f799c754160125bc6daafe2fc1bd335001b11d94be74b560069268f8246e4`  
		Last Modified: Tue, 30 Dec 2025 04:35:02 GMT  
		Size: 2.0 MB (2008544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad51b10b5d6e7e377d3219a2f60c17ba2d754739a985c052724e0826650144fc`  
		Last Modified: Tue, 30 Dec 2025 04:35:03 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; 386

```console
$ docker pull memcached@sha256:0be60a562cdf0c05ebc768c0de49cf333584a650766b962f308610539a885a4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33665696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7b7c835420cd1e7ae8cd0eb0b0df1b2020c581061f1938dfa5292723e395058`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:17:02 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 29 Dec 2025 23:17:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:19:58 GMT
ENV MEMCACHED_VERSION=1.6.40
# Mon, 29 Dec 2025 23:19:58 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Mon, 29 Dec 2025 23:19:58 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Mon, 29 Dec 2025 23:19:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 29 Dec 2025 23:19:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:19:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 29 Dec 2025 23:19:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:19:58 GMT
USER memcache
# Mon, 29 Dec 2025 23:19:58 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 29 Dec 2025 23:19:58 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:796ffff142a3158a5c48a8d81b8b722c5cf4889d5e22da70bdd13a6459d6e40b`  
		Last Modified: Mon, 29 Dec 2025 22:27:31 GMT  
		Size: 31.3 MB (31293100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8fc762766a28f1d89093cb569234311423930c02de910408e80cad47e30647`  
		Last Modified: Mon, 29 Dec 2025 23:20:11 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b725b75ef28bdf7d63e19355a971dc87c6501efa1f70edbee592d52e763fee94`  
		Last Modified: Mon, 29 Dec 2025 23:20:11 GMT  
		Size: 147.5 KB (147508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9509121c0551cdeef95fef92e5598954065e802767669466cffb6c8dada5c3`  
		Last Modified: Mon, 29 Dec 2025 23:20:11 GMT  
		Size: 2.2 MB (2223574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f6e90b6aa0c5dbad71d717fad6007d2dfc7dbc186fa2c07eb8ce8416168801`  
		Last Modified: Mon, 29 Dec 2025 23:20:11 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4fa5d83d611a53674f14bb3fea7ff4465d235101cd9c5640e6c822413b3f4e`  
		Last Modified: Mon, 29 Dec 2025 23:20:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:2f28d2975c37dc6c21579400a4d8a911f45c78e460466164e094c3b114a8a739
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b72a726f712c69433343b634304351532be5cd25051c5bba2f1842cbe52c9fd`

```dockerfile
```

-	Layers:
	-	`sha256:0b522eb7b1ed969865d6941e83230cfad34490504dd209cdf0a9574b09a02415`  
		Last Modified: Tue, 30 Dec 2025 04:35:06 GMT  
		Size: 2.0 MB (2005385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9244708212b7f5f5094918a876558a69b2ba5df9e6a6187f1f97b3dd699465a`  
		Last Modified: Tue, 30 Dec 2025 04:35:08 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; ppc64le

```console
$ docker pull memcached@sha256:38a236f83eb206f786b39c53e8f756815f0bda1460157b11844faf21735208bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36162589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d41292f5c75fe5f3a464b809bde41e0ae8849ad8d7046918a548d0c6b2e250a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 21:34:54 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 17 Dec 2025 21:35:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:28 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:28 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:28 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ddd908d99c8b32da8685339ba6296773100f66e08c8bf508ab82174ba5a4f600`  
		Last Modified: Tue, 09 Dec 2025 00:06:51 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d2b42546c7b688160cfd1a0da61a24922a019b4ebead88e23aff01482ddd477`  
		Last Modified: Wed, 17 Dec 2025 21:38:49 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4efe9fd2e012174cd86a64f83d7b7facfe14ee67c9c9fa5ce994f22c24173f2c`  
		Last Modified: Wed, 17 Dec 2025 21:38:49 GMT  
		Size: 170.4 KB (170393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9752985ba696f0f8d5831ac91e19bfe336342b1c403542641c575b1dc6116e`  
		Last Modified: Wed, 17 Dec 2025 21:38:49 GMT  
		Size: 2.4 MB (2393786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d11c68ba0bc913d139eea51cb2957c1ddd713515fc06dfa5d4c398b119535a`  
		Last Modified: Wed, 17 Dec 2025 21:38:49 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9186b8b7184cef442ae3ed6a3feadcaa8f4ccc974ed5ae6c6cf8efe37e679f23`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:00d1019e9978171df76f638253f212405bf7d53251607ef5a5933d5b28d867b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:588d3d6ab54a9ea5c8baf9b013bb23c12826989ba0d09cb862431e2fa30e5189`

```dockerfile
```

-	Layers:
	-	`sha256:799ad025578a6d5d0155dc5be223bfbc25ffa3aa0548e4fb2e4bedeb0a5088d9`  
		Last Modified: Wed, 17 Dec 2025 22:35:03 GMT  
		Size: 2.0 MB (2011829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eaa03114ccb63fbbd8ca04eef46baa26c8a0508f1256aa45d851f3a49f2ed47a`  
		Last Modified: Wed, 17 Dec 2025 22:35:04 GMT  
		Size: 22.2 KB (22225 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; riscv64

```console
$ docker pull memcached@sha256:30d185f5c04056622fe346fecdf9a07a4d861871fef4028424c9b38e979d2ba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30615105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6048e6bd3b428597fcae4887d0b69fb252944cd1c8afdd85045a4e4c68837ecf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 03:48:33 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 30 Dec 2025 03:49:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 04:02:23 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 30 Dec 2025 04:02:23 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 30 Dec 2025 04:02:23 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 30 Dec 2025 04:02:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 30 Dec 2025 04:02:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Dec 2025 04:02:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 30 Dec 2025 04:02:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Dec 2025 04:02:23 GMT
USER memcache
# Tue, 30 Dec 2025 04:02:23 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 30 Dec 2025 04:02:23 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:96d8ad310358e2403b7b44cf38db606dc1ea6b58b915684d38e13f573860f64e`  
		Last Modified: Tue, 30 Dec 2025 00:53:22 GMT  
		Size: 28.3 MB (28273129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d30361332d6c36fa201043e1df585bb5cea535dfbf760f9b2ed1827c4a53ac`  
		Last Modified: Tue, 30 Dec 2025 04:03:16 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe44badb419e8d40ff093c52477fa45ed79bb9d483ed2f517359e5583617d73a`  
		Last Modified: Tue, 30 Dec 2025 04:03:17 GMT  
		Size: 133.1 KB (133088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a36426c8facdb7304fc9999aee0ca442e6e3b75be15714fa9cadff5589e57f20`  
		Last Modified: Tue, 30 Dec 2025 04:03:16 GMT  
		Size: 2.2 MB (2207375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7820ce69e6809e314e3ef1cf5cc6d3c2bafcd597d9eaf7f0f491c3ea69249db`  
		Last Modified: Tue, 30 Dec 2025 04:03:16 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc77699b8548736e5d2fa9873720c2f41ddfbc89354a6f902b7e5b5651ad0135`  
		Last Modified: Tue, 30 Dec 2025 04:03:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:7f4ca8337c70973f8b5a8eb90158eacfc3a792f5af42d7edf68da0a3a4846cd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a70852a9b9663c0d61ac529b72228ba271972017a65a149b4af634dadda75c5b`

```dockerfile
```

-	Layers:
	-	`sha256:45586a078529026200d6db8b774cf2db02f7292ac8bd6cfd4f8e68ddbe883e64`  
		Last Modified: Tue, 30 Dec 2025 04:35:15 GMT  
		Size: 2.0 MB (2002192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e23345b5880eafecc6509da78e5a9b8e6e95ce6050b2ecb71bb24c1aa03342e5`  
		Last Modified: Tue, 30 Dec 2025 04:35:15 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; s390x

```console
$ docker pull memcached@sha256:e513e62f8a86f2c8f23e06b9b73d141d7e53163ab557ec297be5f3c682a70bc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32273670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd4c0f39122c5c6e9cb01d08aebb1281a0ce18244cbc1e051742de47c5bd51f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:17:26 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 29 Dec 2025 23:17:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:20:38 GMT
ENV MEMCACHED_VERSION=1.6.40
# Mon, 29 Dec 2025 23:20:38 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Mon, 29 Dec 2025 23:20:38 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Mon, 29 Dec 2025 23:20:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 29 Dec 2025 23:20:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:20:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 29 Dec 2025 23:20:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:20:38 GMT
USER memcache
# Mon, 29 Dec 2025 23:20:38 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 29 Dec 2025 23:20:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c9a83915f7d4b9d7fbe5dceeedd49718d2702fd67d78b63a38ec344f3fbfcc41`  
		Last Modified: Mon, 29 Dec 2025 22:27:07 GMT  
		Size: 29.8 MB (29834418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1fd9e99d807cb897b4653efa7815d408df0bb7175d7fb89ab19b79b7737dc1d`  
		Last Modified: Mon, 29 Dec 2025 23:20:55 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7251a4bef45871483e5419196b0bd7ee7440a6dcc98993bd541eb9cf6ee89b06`  
		Last Modified: Mon, 29 Dec 2025 23:20:55 GMT  
		Size: 140.5 KB (140511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16461f97f95d5d1b2cb64bc91ad5a73d23e505f74a1cf95eeb9de840c9a06488`  
		Last Modified: Mon, 29 Dec 2025 23:20:55 GMT  
		Size: 2.3 MB (2297231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa6eecd4b590cab77eae19d421ebb50ce6ed90281723d604c775bcb78b5408f`  
		Last Modified: Mon, 29 Dec 2025 23:20:55 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2779e4a3a9763cc09cc4694ec9a5b304164f44aa2869a8ccbca67eeca523c305`  
		Last Modified: Mon, 29 Dec 2025 23:20:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:89b3d47f58bd28d04b77c9a4cb6634d06120bc2fa943508ae1125915480f511e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b70d80ce63a4423c1c153bdb4d489ec092debf0f20017e21d47e05ed147b71d9`

```dockerfile
```

-	Layers:
	-	`sha256:0be1a3049197ac03e690e9365edd513ffeb121d05d4b6883a58c6356f44ce72f`  
		Last Modified: Tue, 30 Dec 2025 01:35:29 GMT  
		Size: 2.0 MB (2009665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4be7a57b181c7a7314b420b859583bfaa463e17fc94b8f57edc563abf95a3257`  
		Last Modified: Tue, 30 Dec 2025 01:35:30 GMT  
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
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57c33ac8581cd04f31208409f36331e938a78e6ae3a7a3b530fe9dfebe6eb9ad`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583aae99135b9036c602a1c60743fc4fd519f261ac6d48ed60b01e1beb019e7f`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 106.0 KB (106050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ca22885c42a537f033850e8dff7eaeddbb7514902286739b48c084b55a8d6b`  
		Last Modified: Thu, 18 Dec 2025 00:32:19 GMT  
		Size: 2.0 MB (1989265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d146e2038834770bed57033a6c5d66ead5b731b8b133856dec6726ca21baee9`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
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
		Last Modified: Thu, 18 Dec 2025 01:34:48 GMT  
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
		Last Modified: Thu, 18 Dec 2025 00:50:01 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01bb148ea8fbe93dd8097d85f9ee3cf547d314e669748b4239c05711b0d5f719`  
		Last Modified: Thu, 18 Dec 2025 00:50:02 GMT  
		Size: 102.7 KB (102652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6549359cda37ac41cf41a5ece5f37f1322a82f6b232f12e446c62840637093e`  
		Last Modified: Thu, 18 Dec 2025 00:50:02 GMT  
		Size: 1.9 MB (1939215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:041e37eaffefcfb0809564ddea591be3cd818de5530e2c853c0bc9a2fa25c116`  
		Last Modified: Thu, 18 Dec 2025 00:50:05 GMT  
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
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 1.9 MB (1897191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f237be962bb57c3f749904b5925c8e1d7e9013dfac7dd52cc9611ada81858e`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
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
		Last Modified: Thu, 18 Dec 2025 01:34:55 GMT  
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
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb7b8445facedfc145b9478f74880f520776460f153005b7f437ec339aee530`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1853c901134389608b6e80aaa3e43cd67a35c71aecfdde4b5b7ed3b989a03c`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 121.9 KB (121860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a01d1ac5ce47f4494363e411e1cd25dea26438213a2d18d6bb104d0974d9a52`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 2.0 MB (1966561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115624f24ba74d393c2da3d65ed5b35a7afb3fa9ad143d3fb82c64953b3d0401`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87bba524314294ca97195ce65a35ec6d42d3f9f18c9cc0c05c064c9a3cf85c0`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
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
		Last Modified: Thu, 18 Dec 2025 00:32:41 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b2862af05c1582c8625c82ea0863dc2b6474e410d3e6a32876c920e0152c73`  
		Last Modified: Thu, 18 Dec 2025 00:32:42 GMT  
		Size: 110.7 KB (110740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30872a43f6c591fd9b979b49b0fb32107b4bfa8c1155657fa255aa199cf0b83b`  
		Last Modified: Thu, 18 Dec 2025 00:32:42 GMT  
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
		Last Modified: Thu, 18 Dec 2025 01:35:04 GMT  
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
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4079a2d61bafcf146b8f57b35f0e39bf2548e0963be10cff5086f9a56ccdd9d`  
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
		Size: 126.3 KB (126257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f69efa1066815d67cf415d0aac5dcd305032257b6bded5a4c57a7444a1e7fd4`  
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
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
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f270744f8d8b82bc6657387109b33836a76d6dbf8faa645a997db7ea290cdb`  
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
		Size: 114.3 KB (114299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91f8ee8f36703944a7bdcaf57cc5772fe9f79c74a088c33fa1b6da7de119f93`  
		Last Modified: Thu, 18 Dec 2025 00:34:02 GMT  
		Size: 2.0 MB (2017131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e21d2db88668745770273c7b36d4d2c1e87a80b0118b8d775813860b467384c8`  
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd847159e169b898a67d4454fd5a22406c5ae623b16889d084a1d5f2d46a499`  
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
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
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57c33ac8581cd04f31208409f36331e938a78e6ae3a7a3b530fe9dfebe6eb9ad`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583aae99135b9036c602a1c60743fc4fd519f261ac6d48ed60b01e1beb019e7f`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 106.0 KB (106050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ca22885c42a537f033850e8dff7eaeddbb7514902286739b48c084b55a8d6b`  
		Last Modified: Thu, 18 Dec 2025 00:32:19 GMT  
		Size: 2.0 MB (1989265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d146e2038834770bed57033a6c5d66ead5b731b8b133856dec6726ca21baee9`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
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
		Last Modified: Thu, 18 Dec 2025 01:34:48 GMT  
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
		Last Modified: Thu, 18 Dec 2025 00:50:01 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01bb148ea8fbe93dd8097d85f9ee3cf547d314e669748b4239c05711b0d5f719`  
		Last Modified: Thu, 18 Dec 2025 00:50:02 GMT  
		Size: 102.7 KB (102652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6549359cda37ac41cf41a5ece5f37f1322a82f6b232f12e446c62840637093e`  
		Last Modified: Thu, 18 Dec 2025 00:50:02 GMT  
		Size: 1.9 MB (1939215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:041e37eaffefcfb0809564ddea591be3cd818de5530e2c853c0bc9a2fa25c116`  
		Last Modified: Thu, 18 Dec 2025 00:50:05 GMT  
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
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 1.9 MB (1897191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f237be962bb57c3f749904b5925c8e1d7e9013dfac7dd52cc9611ada81858e`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
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
		Last Modified: Thu, 18 Dec 2025 01:34:55 GMT  
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
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb7b8445facedfc145b9478f74880f520776460f153005b7f437ec339aee530`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1853c901134389608b6e80aaa3e43cd67a35c71aecfdde4b5b7ed3b989a03c`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 121.9 KB (121860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a01d1ac5ce47f4494363e411e1cd25dea26438213a2d18d6bb104d0974d9a52`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 2.0 MB (1966561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115624f24ba74d393c2da3d65ed5b35a7afb3fa9ad143d3fb82c64953b3d0401`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87bba524314294ca97195ce65a35ec6d42d3f9f18c9cc0c05c064c9a3cf85c0`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
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
		Last Modified: Thu, 18 Dec 2025 00:32:41 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b2862af05c1582c8625c82ea0863dc2b6474e410d3e6a32876c920e0152c73`  
		Last Modified: Thu, 18 Dec 2025 00:32:42 GMT  
		Size: 110.7 KB (110740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30872a43f6c591fd9b979b49b0fb32107b4bfa8c1155657fa255aa199cf0b83b`  
		Last Modified: Thu, 18 Dec 2025 00:32:42 GMT  
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
		Last Modified: Thu, 18 Dec 2025 01:35:04 GMT  
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
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4079a2d61bafcf146b8f57b35f0e39bf2548e0963be10cff5086f9a56ccdd9d`  
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
		Size: 126.3 KB (126257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f69efa1066815d67cf415d0aac5dcd305032257b6bded5a4c57a7444a1e7fd4`  
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
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
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f270744f8d8b82bc6657387109b33836a76d6dbf8faa645a997db7ea290cdb`  
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
		Size: 114.3 KB (114299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91f8ee8f36703944a7bdcaf57cc5772fe9f79c74a088c33fa1b6da7de119f93`  
		Last Modified: Thu, 18 Dec 2025 00:34:02 GMT  
		Size: 2.0 MB (2017131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e21d2db88668745770273c7b36d4d2c1e87a80b0118b8d775813860b467384c8`  
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd847159e169b898a67d4454fd5a22406c5ae623b16889d084a1d5f2d46a499`  
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
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
$ docker pull memcached@sha256:36c36f0c38cda62ab29af64a0eefa53e99879265ff70df8ac12597be28c482f7
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
$ docker pull memcached@sha256:61bcd214c8da24f2bacfd9152bccafef4f4c0993897c945ee3058106e084b314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32193395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5dafc7d411a870fbc52ca64194006e50e355d34f1edf56b4e1dc5b8019b0934`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:21:34 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 29 Dec 2025 23:21:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:24:22 GMT
ENV MEMCACHED_VERSION=1.6.40
# Mon, 29 Dec 2025 23:24:22 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Mon, 29 Dec 2025 23:24:22 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Mon, 29 Dec 2025 23:24:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 29 Dec 2025 23:24:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:24:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 29 Dec 2025 23:24:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:24:22 GMT
USER memcache
# Mon, 29 Dec 2025 23:24:22 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 29 Dec 2025 23:24:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d08d8001380dd7c5a9be2e59244310ccfa7e84f3b896b354059d46d1928401`  
		Last Modified: Mon, 29 Dec 2025 23:24:36 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8420bae5d2af8b5b5e66d7e5ba882f5e2034cc64eacfb1a0b4b32a259a541b16`  
		Last Modified: Mon, 29 Dec 2025 23:24:35 GMT  
		Size: 136.7 KB (136694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc2daf1b2287468ea06570c5bedff8bc84ab6833050a7e0686f5f7d7a2679e1`  
		Last Modified: Mon, 29 Dec 2025 23:24:35 GMT  
		Size: 2.3 MB (2278657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a54c348dd92d8a79d150c1fe56008dba798b633f010e1e57c0a18f62b2752d90`  
		Last Modified: Mon, 29 Dec 2025 23:24:35 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e147936d0f858c8f726dea003b7220347e43918cab2714f81c66c1553cc160cd`  
		Last Modified: Mon, 29 Dec 2025 23:24:35 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:e6d0cef74a4a91255f97601317c1cd45953291e56aebea597b1f5fedb87772df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a114559b11eef9830f21c5cfd0b3dff0712acd507604d89ab89f16d229d637c`

```dockerfile
```

-	Layers:
	-	`sha256:31d77d05cfee83189fed485cbb6de83d56b3fc5c8a37eafd4e5ab2a8646bcee5`  
		Last Modified: Tue, 30 Dec 2025 04:34:52 GMT  
		Size: 2.0 MB (2008228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:daae5d64f19c0b653f152172ab207032a103d7a2c198208a2472a4565869c64e`  
		Last Modified: Tue, 30 Dec 2025 04:34:53 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; arm variant v5

```console
$ docker pull memcached@sha256:19778ab8ffe04b579956362255d1b4be4646df675a0c0db5662d882e7e062834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30300227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85e834ef35584236d3b04d1823e406899096de386d548c5f0bfd896cfba41631`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:17:23 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 29 Dec 2025 23:17:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:39:32 GMT
ENV MEMCACHED_VERSION=1.6.40
# Mon, 29 Dec 2025 23:39:32 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Mon, 29 Dec 2025 23:39:32 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Mon, 29 Dec 2025 23:39:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 29 Dec 2025 23:39:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:39:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 29 Dec 2025 23:39:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:39:32 GMT
USER memcache
# Mon, 29 Dec 2025 23:39:32 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 29 Dec 2025 23:39:32 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b99a8d8dab982a1a4ea341e66b178b14c0f373c2cd90ac46a67308a4f43c82ae`  
		Last Modified: Mon, 29 Dec 2025 22:27:09 GMT  
		Size: 27.9 MB (27944146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0be68f37541245f1acaee607441dfc983a00e90d78d5e0941265d0b67b1cc9a`  
		Last Modified: Mon, 29 Dec 2025 23:39:44 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10905a7698a57312678edda9f8fc0748b6288699f5fed1f8e7e7e909240d441`  
		Last Modified: Mon, 29 Dec 2025 23:39:44 GMT  
		Size: 144.1 KB (144149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea062eb6d6681b78497a81a8d5ca89088b56f5a5d629e3124df93b9ca0e4f16`  
		Last Modified: Mon, 29 Dec 2025 23:39:44 GMT  
		Size: 2.2 MB (2210419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d59770b8679e935091911e6294f61a53df8f59b5cc8aae431217cc391864a0`  
		Last Modified: Mon, 29 Dec 2025 23:39:44 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945c1d27fa6617071d97eddd3d962ac571276f7f757f99edc1a93ebbe6eb5a9c`  
		Last Modified: Mon, 29 Dec 2025 23:39:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:27e3afeed14c4cac078a10db01ef22eef58848fc65d93501050f872bc3cf64d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:939368d93857b65d5e6bbdc97a5f4d158eeca9efc9fb02875eae93350ea663fb`

```dockerfile
```

-	Layers:
	-	`sha256:3559f8384ca294c984900b7325032abfe47459734f215e79264a22aa23802031`  
		Last Modified: Tue, 30 Dec 2025 01:35:12 GMT  
		Size: 2.0 MB (2011231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b310c8a994e22e59ca814cd06500201d5b78c4bbfe3baa8785ae093760d4a4fb`  
		Last Modified: Tue, 30 Dec 2025 01:35:13 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; arm variant v7

```console
$ docker pull memcached@sha256:34f932820fcffc223d050d31ceeef236f4bc4a1a8e776006560fe2ef14348a2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28510848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0a0c32503881f91ec515af1fd074032b8070eac0faa4afca5e1f2f60609b237`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:17:22 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 29 Dec 2025 23:17:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:20:31 GMT
ENV MEMCACHED_VERSION=1.6.40
# Mon, 29 Dec 2025 23:20:31 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Mon, 29 Dec 2025 23:20:31 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Mon, 29 Dec 2025 23:20:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 29 Dec 2025 23:20:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:20:31 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 29 Dec 2025 23:20:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:20:31 GMT
USER memcache
# Mon, 29 Dec 2025 23:20:31 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 29 Dec 2025 23:20:31 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6d3e0fea3cb8eb29b9c06956265b47cd00f7ebfb48e35e818f686d52c21353f5`  
		Last Modified: Mon, 29 Dec 2025 22:28:07 GMT  
		Size: 26.2 MB (26210001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f916949d5244227fca363e62638c31c65e0f6a941ceaa0fb79c37d962e9b95bb`  
		Last Modified: Mon, 29 Dec 2025 23:20:45 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f24598f250037f41edf0d0093ed08f2b3b3937f91d7708c687330e0feca3fdcf`  
		Last Modified: Mon, 29 Dec 2025 23:20:45 GMT  
		Size: 135.4 KB (135362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f260cb2adbfa9ad1d74da541da12d2146b1a06685021b42e924c843481237ee2`  
		Last Modified: Mon, 29 Dec 2025 23:20:46 GMT  
		Size: 2.2 MB (2163975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0f315cda938284ce51afa280bd8e89b891448b2da00c28c66c638c2d4a4cc6`  
		Last Modified: Mon, 29 Dec 2025 23:20:45 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c38a3204b12ac8ee46611fe38ab1a706ee2c310f8a4e0439862ee702d7b5481c`  
		Last Modified: Mon, 29 Dec 2025 23:20:45 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:4c6e114c037bf19003547b10ffc5b077c88be25cd990cd30d1f26945409bf69c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5de9929189cfe8912f0ebace1f73497b21396b8561e62dab4d98cefa02760f10`

```dockerfile
```

-	Layers:
	-	`sha256:1bc6b02786844de8506e80bae2bf850ea8bf7875761b0a8ff17497e18e297086`  
		Last Modified: Tue, 30 Dec 2025 04:34:58 GMT  
		Size: 2.0 MB (2009688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48de2da0a0a924a9a938d6ea9a12b2eb727da5a33bad6987e74e57dcfdc66f51`  
		Last Modified: Tue, 30 Dec 2025 04:34:59 GMT  
		Size: 22.3 KB (22303 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:517aefb9e9ff071c2aa387ca68e1b63663f210c5bc838b8d928cb657795329fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32554923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20bd9e6ac4a3626ae8b8108e846570938ea003859e516dcd2134d2d628fd2c79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:21:52 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 29 Dec 2025 23:21:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:24:52 GMT
ENV MEMCACHED_VERSION=1.6.40
# Mon, 29 Dec 2025 23:24:52 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Mon, 29 Dec 2025 23:24:52 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Mon, 29 Dec 2025 23:24:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 29 Dec 2025 23:24:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:24:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 29 Dec 2025 23:24:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:24:52 GMT
USER memcache
# Mon, 29 Dec 2025 23:24:52 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 29 Dec 2025 23:24:52 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d74ee4724223b1c44d3bdff5ee6ee8c7eceabc636fe61128ec308914b5999f8`  
		Last Modified: Mon, 29 Dec 2025 23:25:06 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d74224a341d3e408a0affb0b0eb0c53f99939a1b669f25e6b34026f224a3745`  
		Last Modified: Mon, 29 Dec 2025 23:25:06 GMT  
		Size: 153.5 KB (153455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5db3b7f17de3125f5608801faf4e6a1615d96c6be2fa7f1c09e52d0cd7cd80`  
		Last Modified: Mon, 29 Dec 2025 23:25:06 GMT  
		Size: 2.3 MB (2261324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885dc482553144838528b69fa53518cc1fafb03d7eac91e773730285029e30e9`  
		Last Modified: Mon, 29 Dec 2025 23:25:06 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8afa8cb30ddae48c82fab84d30d0457bfa667059caff286dcfc57999e07a8b1`  
		Last Modified: Mon, 29 Dec 2025 23:25:06 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:62c7db64a99cd405d4330dc5c878884ef8a0e107864d7314a4cb66a8242b7dee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cfb248343584b4b08d6f7b363daf97f9506e303159317383e87ae5b82750335`

```dockerfile
```

-	Layers:
	-	`sha256:f38f799c754160125bc6daafe2fc1bd335001b11d94be74b560069268f8246e4`  
		Last Modified: Tue, 30 Dec 2025 04:35:02 GMT  
		Size: 2.0 MB (2008544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad51b10b5d6e7e377d3219a2f60c17ba2d754739a985c052724e0826650144fc`  
		Last Modified: Tue, 30 Dec 2025 04:35:03 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; 386

```console
$ docker pull memcached@sha256:0be60a562cdf0c05ebc768c0de49cf333584a650766b962f308610539a885a4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33665696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7b7c835420cd1e7ae8cd0eb0b0df1b2020c581061f1938dfa5292723e395058`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:17:02 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 29 Dec 2025 23:17:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:19:58 GMT
ENV MEMCACHED_VERSION=1.6.40
# Mon, 29 Dec 2025 23:19:58 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Mon, 29 Dec 2025 23:19:58 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Mon, 29 Dec 2025 23:19:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 29 Dec 2025 23:19:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:19:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 29 Dec 2025 23:19:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:19:58 GMT
USER memcache
# Mon, 29 Dec 2025 23:19:58 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 29 Dec 2025 23:19:58 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:796ffff142a3158a5c48a8d81b8b722c5cf4889d5e22da70bdd13a6459d6e40b`  
		Last Modified: Mon, 29 Dec 2025 22:27:31 GMT  
		Size: 31.3 MB (31293100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8fc762766a28f1d89093cb569234311423930c02de910408e80cad47e30647`  
		Last Modified: Mon, 29 Dec 2025 23:20:11 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b725b75ef28bdf7d63e19355a971dc87c6501efa1f70edbee592d52e763fee94`  
		Last Modified: Mon, 29 Dec 2025 23:20:11 GMT  
		Size: 147.5 KB (147508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9509121c0551cdeef95fef92e5598954065e802767669466cffb6c8dada5c3`  
		Last Modified: Mon, 29 Dec 2025 23:20:11 GMT  
		Size: 2.2 MB (2223574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f6e90b6aa0c5dbad71d717fad6007d2dfc7dbc186fa2c07eb8ce8416168801`  
		Last Modified: Mon, 29 Dec 2025 23:20:11 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4fa5d83d611a53674f14bb3fea7ff4465d235101cd9c5640e6c822413b3f4e`  
		Last Modified: Mon, 29 Dec 2025 23:20:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:2f28d2975c37dc6c21579400a4d8a911f45c78e460466164e094c3b114a8a739
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b72a726f712c69433343b634304351532be5cd25051c5bba2f1842cbe52c9fd`

```dockerfile
```

-	Layers:
	-	`sha256:0b522eb7b1ed969865d6941e83230cfad34490504dd209cdf0a9574b09a02415`  
		Last Modified: Tue, 30 Dec 2025 04:35:06 GMT  
		Size: 2.0 MB (2005385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9244708212b7f5f5094918a876558a69b2ba5df9e6a6187f1f97b3dd699465a`  
		Last Modified: Tue, 30 Dec 2025 04:35:08 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; ppc64le

```console
$ docker pull memcached@sha256:38a236f83eb206f786b39c53e8f756815f0bda1460157b11844faf21735208bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36162589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d41292f5c75fe5f3a464b809bde41e0ae8849ad8d7046918a548d0c6b2e250a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 21:34:54 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 17 Dec 2025 21:35:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:28 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:28 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:28 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ddd908d99c8b32da8685339ba6296773100f66e08c8bf508ab82174ba5a4f600`  
		Last Modified: Tue, 09 Dec 2025 00:06:51 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d2b42546c7b688160cfd1a0da61a24922a019b4ebead88e23aff01482ddd477`  
		Last Modified: Wed, 17 Dec 2025 21:38:49 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4efe9fd2e012174cd86a64f83d7b7facfe14ee67c9c9fa5ce994f22c24173f2c`  
		Last Modified: Wed, 17 Dec 2025 21:38:49 GMT  
		Size: 170.4 KB (170393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9752985ba696f0f8d5831ac91e19bfe336342b1c403542641c575b1dc6116e`  
		Last Modified: Wed, 17 Dec 2025 21:38:49 GMT  
		Size: 2.4 MB (2393786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d11c68ba0bc913d139eea51cb2957c1ddd713515fc06dfa5d4c398b119535a`  
		Last Modified: Wed, 17 Dec 2025 21:38:49 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9186b8b7184cef442ae3ed6a3feadcaa8f4ccc974ed5ae6c6cf8efe37e679f23`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:00d1019e9978171df76f638253f212405bf7d53251607ef5a5933d5b28d867b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:588d3d6ab54a9ea5c8baf9b013bb23c12826989ba0d09cb862431e2fa30e5189`

```dockerfile
```

-	Layers:
	-	`sha256:799ad025578a6d5d0155dc5be223bfbc25ffa3aa0548e4fb2e4bedeb0a5088d9`  
		Last Modified: Wed, 17 Dec 2025 22:35:03 GMT  
		Size: 2.0 MB (2011829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eaa03114ccb63fbbd8ca04eef46baa26c8a0508f1256aa45d851f3a49f2ed47a`  
		Last Modified: Wed, 17 Dec 2025 22:35:04 GMT  
		Size: 22.2 KB (22225 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; riscv64

```console
$ docker pull memcached@sha256:30d185f5c04056622fe346fecdf9a07a4d861871fef4028424c9b38e979d2ba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30615105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6048e6bd3b428597fcae4887d0b69fb252944cd1c8afdd85045a4e4c68837ecf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 03:48:33 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 30 Dec 2025 03:49:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 04:02:23 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 30 Dec 2025 04:02:23 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 30 Dec 2025 04:02:23 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 30 Dec 2025 04:02:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 30 Dec 2025 04:02:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Dec 2025 04:02:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 30 Dec 2025 04:02:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Dec 2025 04:02:23 GMT
USER memcache
# Tue, 30 Dec 2025 04:02:23 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 30 Dec 2025 04:02:23 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:96d8ad310358e2403b7b44cf38db606dc1ea6b58b915684d38e13f573860f64e`  
		Last Modified: Tue, 30 Dec 2025 00:53:22 GMT  
		Size: 28.3 MB (28273129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d30361332d6c36fa201043e1df585bb5cea535dfbf760f9b2ed1827c4a53ac`  
		Last Modified: Tue, 30 Dec 2025 04:03:16 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe44badb419e8d40ff093c52477fa45ed79bb9d483ed2f517359e5583617d73a`  
		Last Modified: Tue, 30 Dec 2025 04:03:17 GMT  
		Size: 133.1 KB (133088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a36426c8facdb7304fc9999aee0ca442e6e3b75be15714fa9cadff5589e57f20`  
		Last Modified: Tue, 30 Dec 2025 04:03:16 GMT  
		Size: 2.2 MB (2207375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7820ce69e6809e314e3ef1cf5cc6d3c2bafcd597d9eaf7f0f491c3ea69249db`  
		Last Modified: Tue, 30 Dec 2025 04:03:16 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc77699b8548736e5d2fa9873720c2f41ddfbc89354a6f902b7e5b5651ad0135`  
		Last Modified: Tue, 30 Dec 2025 04:03:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:7f4ca8337c70973f8b5a8eb90158eacfc3a792f5af42d7edf68da0a3a4846cd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a70852a9b9663c0d61ac529b72228ba271972017a65a149b4af634dadda75c5b`

```dockerfile
```

-	Layers:
	-	`sha256:45586a078529026200d6db8b774cf2db02f7292ac8bd6cfd4f8e68ddbe883e64`  
		Last Modified: Tue, 30 Dec 2025 04:35:15 GMT  
		Size: 2.0 MB (2002192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e23345b5880eafecc6509da78e5a9b8e6e95ce6050b2ecb71bb24c1aa03342e5`  
		Last Modified: Tue, 30 Dec 2025 04:35:15 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; s390x

```console
$ docker pull memcached@sha256:e513e62f8a86f2c8f23e06b9b73d141d7e53163ab557ec297be5f3c682a70bc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32273670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd4c0f39122c5c6e9cb01d08aebb1281a0ce18244cbc1e051742de47c5bd51f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:17:26 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 29 Dec 2025 23:17:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:20:38 GMT
ENV MEMCACHED_VERSION=1.6.40
# Mon, 29 Dec 2025 23:20:38 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Mon, 29 Dec 2025 23:20:38 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Mon, 29 Dec 2025 23:20:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 29 Dec 2025 23:20:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:20:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 29 Dec 2025 23:20:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:20:38 GMT
USER memcache
# Mon, 29 Dec 2025 23:20:38 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 29 Dec 2025 23:20:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c9a83915f7d4b9d7fbe5dceeedd49718d2702fd67d78b63a38ec344f3fbfcc41`  
		Last Modified: Mon, 29 Dec 2025 22:27:07 GMT  
		Size: 29.8 MB (29834418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1fd9e99d807cb897b4653efa7815d408df0bb7175d7fb89ab19b79b7737dc1d`  
		Last Modified: Mon, 29 Dec 2025 23:20:55 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7251a4bef45871483e5419196b0bd7ee7440a6dcc98993bd541eb9cf6ee89b06`  
		Last Modified: Mon, 29 Dec 2025 23:20:55 GMT  
		Size: 140.5 KB (140511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16461f97f95d5d1b2cb64bc91ad5a73d23e505f74a1cf95eeb9de840c9a06488`  
		Last Modified: Mon, 29 Dec 2025 23:20:55 GMT  
		Size: 2.3 MB (2297231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa6eecd4b590cab77eae19d421ebb50ce6ed90281723d604c775bcb78b5408f`  
		Last Modified: Mon, 29 Dec 2025 23:20:55 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2779e4a3a9763cc09cc4694ec9a5b304164f44aa2869a8ccbca67eeca523c305`  
		Last Modified: Mon, 29 Dec 2025 23:20:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:89b3d47f58bd28d04b77c9a4cb6634d06120bc2fa943508ae1125915480f511e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b70d80ce63a4423c1c153bdb4d489ec092debf0f20017e21d47e05ed147b71d9`

```dockerfile
```

-	Layers:
	-	`sha256:0be1a3049197ac03e690e9365edd513ffeb121d05d4b6883a58c6356f44ce72f`  
		Last Modified: Tue, 30 Dec 2025 01:35:29 GMT  
		Size: 2.0 MB (2009665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4be7a57b181c7a7314b420b859583bfaa463e17fc94b8f57edc563abf95a3257`  
		Last Modified: Tue, 30 Dec 2025 01:35:30 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.40`

```console
$ docker pull memcached@sha256:36c36f0c38cda62ab29af64a0eefa53e99879265ff70df8ac12597be28c482f7
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
$ docker pull memcached@sha256:61bcd214c8da24f2bacfd9152bccafef4f4c0993897c945ee3058106e084b314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32193395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5dafc7d411a870fbc52ca64194006e50e355d34f1edf56b4e1dc5b8019b0934`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:21:34 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 29 Dec 2025 23:21:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:24:22 GMT
ENV MEMCACHED_VERSION=1.6.40
# Mon, 29 Dec 2025 23:24:22 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Mon, 29 Dec 2025 23:24:22 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Mon, 29 Dec 2025 23:24:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 29 Dec 2025 23:24:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:24:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 29 Dec 2025 23:24:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:24:22 GMT
USER memcache
# Mon, 29 Dec 2025 23:24:22 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 29 Dec 2025 23:24:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d08d8001380dd7c5a9be2e59244310ccfa7e84f3b896b354059d46d1928401`  
		Last Modified: Mon, 29 Dec 2025 23:24:36 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8420bae5d2af8b5b5e66d7e5ba882f5e2034cc64eacfb1a0b4b32a259a541b16`  
		Last Modified: Mon, 29 Dec 2025 23:24:35 GMT  
		Size: 136.7 KB (136694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc2daf1b2287468ea06570c5bedff8bc84ab6833050a7e0686f5f7d7a2679e1`  
		Last Modified: Mon, 29 Dec 2025 23:24:35 GMT  
		Size: 2.3 MB (2278657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a54c348dd92d8a79d150c1fe56008dba798b633f010e1e57c0a18f62b2752d90`  
		Last Modified: Mon, 29 Dec 2025 23:24:35 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e147936d0f858c8f726dea003b7220347e43918cab2714f81c66c1553cc160cd`  
		Last Modified: Mon, 29 Dec 2025 23:24:35 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40` - unknown; unknown

```console
$ docker pull memcached@sha256:e6d0cef74a4a91255f97601317c1cd45953291e56aebea597b1f5fedb87772df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a114559b11eef9830f21c5cfd0b3dff0712acd507604d89ab89f16d229d637c`

```dockerfile
```

-	Layers:
	-	`sha256:31d77d05cfee83189fed485cbb6de83d56b3fc5c8a37eafd4e5ab2a8646bcee5`  
		Last Modified: Tue, 30 Dec 2025 04:34:52 GMT  
		Size: 2.0 MB (2008228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:daae5d64f19c0b653f152172ab207032a103d7a2c198208a2472a4565869c64e`  
		Last Modified: Tue, 30 Dec 2025 04:34:53 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40` - linux; arm variant v5

```console
$ docker pull memcached@sha256:19778ab8ffe04b579956362255d1b4be4646df675a0c0db5662d882e7e062834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30300227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85e834ef35584236d3b04d1823e406899096de386d548c5f0bfd896cfba41631`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:17:23 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 29 Dec 2025 23:17:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:39:32 GMT
ENV MEMCACHED_VERSION=1.6.40
# Mon, 29 Dec 2025 23:39:32 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Mon, 29 Dec 2025 23:39:32 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Mon, 29 Dec 2025 23:39:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 29 Dec 2025 23:39:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:39:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 29 Dec 2025 23:39:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:39:32 GMT
USER memcache
# Mon, 29 Dec 2025 23:39:32 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 29 Dec 2025 23:39:32 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b99a8d8dab982a1a4ea341e66b178b14c0f373c2cd90ac46a67308a4f43c82ae`  
		Last Modified: Mon, 29 Dec 2025 22:27:09 GMT  
		Size: 27.9 MB (27944146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0be68f37541245f1acaee607441dfc983a00e90d78d5e0941265d0b67b1cc9a`  
		Last Modified: Mon, 29 Dec 2025 23:39:44 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10905a7698a57312678edda9f8fc0748b6288699f5fed1f8e7e7e909240d441`  
		Last Modified: Mon, 29 Dec 2025 23:39:44 GMT  
		Size: 144.1 KB (144149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea062eb6d6681b78497a81a8d5ca89088b56f5a5d629e3124df93b9ca0e4f16`  
		Last Modified: Mon, 29 Dec 2025 23:39:44 GMT  
		Size: 2.2 MB (2210419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d59770b8679e935091911e6294f61a53df8f59b5cc8aae431217cc391864a0`  
		Last Modified: Mon, 29 Dec 2025 23:39:44 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945c1d27fa6617071d97eddd3d962ac571276f7f757f99edc1a93ebbe6eb5a9c`  
		Last Modified: Mon, 29 Dec 2025 23:39:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40` - unknown; unknown

```console
$ docker pull memcached@sha256:27e3afeed14c4cac078a10db01ef22eef58848fc65d93501050f872bc3cf64d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:939368d93857b65d5e6bbdc97a5f4d158eeca9efc9fb02875eae93350ea663fb`

```dockerfile
```

-	Layers:
	-	`sha256:3559f8384ca294c984900b7325032abfe47459734f215e79264a22aa23802031`  
		Last Modified: Tue, 30 Dec 2025 01:35:12 GMT  
		Size: 2.0 MB (2011231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b310c8a994e22e59ca814cd06500201d5b78c4bbfe3baa8785ae093760d4a4fb`  
		Last Modified: Tue, 30 Dec 2025 01:35:13 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40` - linux; arm variant v7

```console
$ docker pull memcached@sha256:34f932820fcffc223d050d31ceeef236f4bc4a1a8e776006560fe2ef14348a2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28510848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0a0c32503881f91ec515af1fd074032b8070eac0faa4afca5e1f2f60609b237`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:17:22 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 29 Dec 2025 23:17:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:20:31 GMT
ENV MEMCACHED_VERSION=1.6.40
# Mon, 29 Dec 2025 23:20:31 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Mon, 29 Dec 2025 23:20:31 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Mon, 29 Dec 2025 23:20:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 29 Dec 2025 23:20:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:20:31 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 29 Dec 2025 23:20:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:20:31 GMT
USER memcache
# Mon, 29 Dec 2025 23:20:31 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 29 Dec 2025 23:20:31 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6d3e0fea3cb8eb29b9c06956265b47cd00f7ebfb48e35e818f686d52c21353f5`  
		Last Modified: Mon, 29 Dec 2025 22:28:07 GMT  
		Size: 26.2 MB (26210001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f916949d5244227fca363e62638c31c65e0f6a941ceaa0fb79c37d962e9b95bb`  
		Last Modified: Mon, 29 Dec 2025 23:20:45 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f24598f250037f41edf0d0093ed08f2b3b3937f91d7708c687330e0feca3fdcf`  
		Last Modified: Mon, 29 Dec 2025 23:20:45 GMT  
		Size: 135.4 KB (135362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f260cb2adbfa9ad1d74da541da12d2146b1a06685021b42e924c843481237ee2`  
		Last Modified: Mon, 29 Dec 2025 23:20:46 GMT  
		Size: 2.2 MB (2163975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0f315cda938284ce51afa280bd8e89b891448b2da00c28c66c638c2d4a4cc6`  
		Last Modified: Mon, 29 Dec 2025 23:20:45 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c38a3204b12ac8ee46611fe38ab1a706ee2c310f8a4e0439862ee702d7b5481c`  
		Last Modified: Mon, 29 Dec 2025 23:20:45 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40` - unknown; unknown

```console
$ docker pull memcached@sha256:4c6e114c037bf19003547b10ffc5b077c88be25cd990cd30d1f26945409bf69c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5de9929189cfe8912f0ebace1f73497b21396b8561e62dab4d98cefa02760f10`

```dockerfile
```

-	Layers:
	-	`sha256:1bc6b02786844de8506e80bae2bf850ea8bf7875761b0a8ff17497e18e297086`  
		Last Modified: Tue, 30 Dec 2025 04:34:58 GMT  
		Size: 2.0 MB (2009688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48de2da0a0a924a9a938d6ea9a12b2eb727da5a33bad6987e74e57dcfdc66f51`  
		Last Modified: Tue, 30 Dec 2025 04:34:59 GMT  
		Size: 22.3 KB (22303 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:517aefb9e9ff071c2aa387ca68e1b63663f210c5bc838b8d928cb657795329fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32554923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20bd9e6ac4a3626ae8b8108e846570938ea003859e516dcd2134d2d628fd2c79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:21:52 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 29 Dec 2025 23:21:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:24:52 GMT
ENV MEMCACHED_VERSION=1.6.40
# Mon, 29 Dec 2025 23:24:52 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Mon, 29 Dec 2025 23:24:52 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Mon, 29 Dec 2025 23:24:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 29 Dec 2025 23:24:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:24:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 29 Dec 2025 23:24:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:24:52 GMT
USER memcache
# Mon, 29 Dec 2025 23:24:52 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 29 Dec 2025 23:24:52 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d74ee4724223b1c44d3bdff5ee6ee8c7eceabc636fe61128ec308914b5999f8`  
		Last Modified: Mon, 29 Dec 2025 23:25:06 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d74224a341d3e408a0affb0b0eb0c53f99939a1b669f25e6b34026f224a3745`  
		Last Modified: Mon, 29 Dec 2025 23:25:06 GMT  
		Size: 153.5 KB (153455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5db3b7f17de3125f5608801faf4e6a1615d96c6be2fa7f1c09e52d0cd7cd80`  
		Last Modified: Mon, 29 Dec 2025 23:25:06 GMT  
		Size: 2.3 MB (2261324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885dc482553144838528b69fa53518cc1fafb03d7eac91e773730285029e30e9`  
		Last Modified: Mon, 29 Dec 2025 23:25:06 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8afa8cb30ddae48c82fab84d30d0457bfa667059caff286dcfc57999e07a8b1`  
		Last Modified: Mon, 29 Dec 2025 23:25:06 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40` - unknown; unknown

```console
$ docker pull memcached@sha256:62c7db64a99cd405d4330dc5c878884ef8a0e107864d7314a4cb66a8242b7dee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cfb248343584b4b08d6f7b363daf97f9506e303159317383e87ae5b82750335`

```dockerfile
```

-	Layers:
	-	`sha256:f38f799c754160125bc6daafe2fc1bd335001b11d94be74b560069268f8246e4`  
		Last Modified: Tue, 30 Dec 2025 04:35:02 GMT  
		Size: 2.0 MB (2008544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad51b10b5d6e7e377d3219a2f60c17ba2d754739a985c052724e0826650144fc`  
		Last Modified: Tue, 30 Dec 2025 04:35:03 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40` - linux; 386

```console
$ docker pull memcached@sha256:0be60a562cdf0c05ebc768c0de49cf333584a650766b962f308610539a885a4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33665696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7b7c835420cd1e7ae8cd0eb0b0df1b2020c581061f1938dfa5292723e395058`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:17:02 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 29 Dec 2025 23:17:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:19:58 GMT
ENV MEMCACHED_VERSION=1.6.40
# Mon, 29 Dec 2025 23:19:58 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Mon, 29 Dec 2025 23:19:58 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Mon, 29 Dec 2025 23:19:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 29 Dec 2025 23:19:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:19:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 29 Dec 2025 23:19:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:19:58 GMT
USER memcache
# Mon, 29 Dec 2025 23:19:58 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 29 Dec 2025 23:19:58 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:796ffff142a3158a5c48a8d81b8b722c5cf4889d5e22da70bdd13a6459d6e40b`  
		Last Modified: Mon, 29 Dec 2025 22:27:31 GMT  
		Size: 31.3 MB (31293100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8fc762766a28f1d89093cb569234311423930c02de910408e80cad47e30647`  
		Last Modified: Mon, 29 Dec 2025 23:20:11 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b725b75ef28bdf7d63e19355a971dc87c6501efa1f70edbee592d52e763fee94`  
		Last Modified: Mon, 29 Dec 2025 23:20:11 GMT  
		Size: 147.5 KB (147508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9509121c0551cdeef95fef92e5598954065e802767669466cffb6c8dada5c3`  
		Last Modified: Mon, 29 Dec 2025 23:20:11 GMT  
		Size: 2.2 MB (2223574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f6e90b6aa0c5dbad71d717fad6007d2dfc7dbc186fa2c07eb8ce8416168801`  
		Last Modified: Mon, 29 Dec 2025 23:20:11 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4fa5d83d611a53674f14bb3fea7ff4465d235101cd9c5640e6c822413b3f4e`  
		Last Modified: Mon, 29 Dec 2025 23:20:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40` - unknown; unknown

```console
$ docker pull memcached@sha256:2f28d2975c37dc6c21579400a4d8a911f45c78e460466164e094c3b114a8a739
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b72a726f712c69433343b634304351532be5cd25051c5bba2f1842cbe52c9fd`

```dockerfile
```

-	Layers:
	-	`sha256:0b522eb7b1ed969865d6941e83230cfad34490504dd209cdf0a9574b09a02415`  
		Last Modified: Tue, 30 Dec 2025 04:35:06 GMT  
		Size: 2.0 MB (2005385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9244708212b7f5f5094918a876558a69b2ba5df9e6a6187f1f97b3dd699465a`  
		Last Modified: Tue, 30 Dec 2025 04:35:08 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40` - linux; ppc64le

```console
$ docker pull memcached@sha256:38a236f83eb206f786b39c53e8f756815f0bda1460157b11844faf21735208bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36162589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d41292f5c75fe5f3a464b809bde41e0ae8849ad8d7046918a548d0c6b2e250a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 21:34:54 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 17 Dec 2025 21:35:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:28 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:28 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:28 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ddd908d99c8b32da8685339ba6296773100f66e08c8bf508ab82174ba5a4f600`  
		Last Modified: Tue, 09 Dec 2025 00:06:51 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d2b42546c7b688160cfd1a0da61a24922a019b4ebead88e23aff01482ddd477`  
		Last Modified: Wed, 17 Dec 2025 21:38:49 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4efe9fd2e012174cd86a64f83d7b7facfe14ee67c9c9fa5ce994f22c24173f2c`  
		Last Modified: Wed, 17 Dec 2025 21:38:49 GMT  
		Size: 170.4 KB (170393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9752985ba696f0f8d5831ac91e19bfe336342b1c403542641c575b1dc6116e`  
		Last Modified: Wed, 17 Dec 2025 21:38:49 GMT  
		Size: 2.4 MB (2393786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d11c68ba0bc913d139eea51cb2957c1ddd713515fc06dfa5d4c398b119535a`  
		Last Modified: Wed, 17 Dec 2025 21:38:49 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9186b8b7184cef442ae3ed6a3feadcaa8f4ccc974ed5ae6c6cf8efe37e679f23`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40` - unknown; unknown

```console
$ docker pull memcached@sha256:00d1019e9978171df76f638253f212405bf7d53251607ef5a5933d5b28d867b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:588d3d6ab54a9ea5c8baf9b013bb23c12826989ba0d09cb862431e2fa30e5189`

```dockerfile
```

-	Layers:
	-	`sha256:799ad025578a6d5d0155dc5be223bfbc25ffa3aa0548e4fb2e4bedeb0a5088d9`  
		Last Modified: Wed, 17 Dec 2025 22:35:03 GMT  
		Size: 2.0 MB (2011829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eaa03114ccb63fbbd8ca04eef46baa26c8a0508f1256aa45d851f3a49f2ed47a`  
		Last Modified: Wed, 17 Dec 2025 22:35:04 GMT  
		Size: 22.2 KB (22225 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40` - linux; riscv64

```console
$ docker pull memcached@sha256:30d185f5c04056622fe346fecdf9a07a4d861871fef4028424c9b38e979d2ba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30615105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6048e6bd3b428597fcae4887d0b69fb252944cd1c8afdd85045a4e4c68837ecf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 03:48:33 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 30 Dec 2025 03:49:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 04:02:23 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 30 Dec 2025 04:02:23 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 30 Dec 2025 04:02:23 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 30 Dec 2025 04:02:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 30 Dec 2025 04:02:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Dec 2025 04:02:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 30 Dec 2025 04:02:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Dec 2025 04:02:23 GMT
USER memcache
# Tue, 30 Dec 2025 04:02:23 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 30 Dec 2025 04:02:23 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:96d8ad310358e2403b7b44cf38db606dc1ea6b58b915684d38e13f573860f64e`  
		Last Modified: Tue, 30 Dec 2025 00:53:22 GMT  
		Size: 28.3 MB (28273129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d30361332d6c36fa201043e1df585bb5cea535dfbf760f9b2ed1827c4a53ac`  
		Last Modified: Tue, 30 Dec 2025 04:03:16 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe44badb419e8d40ff093c52477fa45ed79bb9d483ed2f517359e5583617d73a`  
		Last Modified: Tue, 30 Dec 2025 04:03:17 GMT  
		Size: 133.1 KB (133088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a36426c8facdb7304fc9999aee0ca442e6e3b75be15714fa9cadff5589e57f20`  
		Last Modified: Tue, 30 Dec 2025 04:03:16 GMT  
		Size: 2.2 MB (2207375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7820ce69e6809e314e3ef1cf5cc6d3c2bafcd597d9eaf7f0f491c3ea69249db`  
		Last Modified: Tue, 30 Dec 2025 04:03:16 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc77699b8548736e5d2fa9873720c2f41ddfbc89354a6f902b7e5b5651ad0135`  
		Last Modified: Tue, 30 Dec 2025 04:03:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40` - unknown; unknown

```console
$ docker pull memcached@sha256:7f4ca8337c70973f8b5a8eb90158eacfc3a792f5af42d7edf68da0a3a4846cd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a70852a9b9663c0d61ac529b72228ba271972017a65a149b4af634dadda75c5b`

```dockerfile
```

-	Layers:
	-	`sha256:45586a078529026200d6db8b774cf2db02f7292ac8bd6cfd4f8e68ddbe883e64`  
		Last Modified: Tue, 30 Dec 2025 04:35:15 GMT  
		Size: 2.0 MB (2002192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e23345b5880eafecc6509da78e5a9b8e6e95ce6050b2ecb71bb24c1aa03342e5`  
		Last Modified: Tue, 30 Dec 2025 04:35:15 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40` - linux; s390x

```console
$ docker pull memcached@sha256:e513e62f8a86f2c8f23e06b9b73d141d7e53163ab557ec297be5f3c682a70bc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32273670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd4c0f39122c5c6e9cb01d08aebb1281a0ce18244cbc1e051742de47c5bd51f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:17:26 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 29 Dec 2025 23:17:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:20:38 GMT
ENV MEMCACHED_VERSION=1.6.40
# Mon, 29 Dec 2025 23:20:38 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Mon, 29 Dec 2025 23:20:38 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Mon, 29 Dec 2025 23:20:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 29 Dec 2025 23:20:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:20:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 29 Dec 2025 23:20:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:20:38 GMT
USER memcache
# Mon, 29 Dec 2025 23:20:38 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 29 Dec 2025 23:20:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c9a83915f7d4b9d7fbe5dceeedd49718d2702fd67d78b63a38ec344f3fbfcc41`  
		Last Modified: Mon, 29 Dec 2025 22:27:07 GMT  
		Size: 29.8 MB (29834418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1fd9e99d807cb897b4653efa7815d408df0bb7175d7fb89ab19b79b7737dc1d`  
		Last Modified: Mon, 29 Dec 2025 23:20:55 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7251a4bef45871483e5419196b0bd7ee7440a6dcc98993bd541eb9cf6ee89b06`  
		Last Modified: Mon, 29 Dec 2025 23:20:55 GMT  
		Size: 140.5 KB (140511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16461f97f95d5d1b2cb64bc91ad5a73d23e505f74a1cf95eeb9de840c9a06488`  
		Last Modified: Mon, 29 Dec 2025 23:20:55 GMT  
		Size: 2.3 MB (2297231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa6eecd4b590cab77eae19d421ebb50ce6ed90281723d604c775bcb78b5408f`  
		Last Modified: Mon, 29 Dec 2025 23:20:55 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2779e4a3a9763cc09cc4694ec9a5b304164f44aa2869a8ccbca67eeca523c305`  
		Last Modified: Mon, 29 Dec 2025 23:20:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40` - unknown; unknown

```console
$ docker pull memcached@sha256:89b3d47f58bd28d04b77c9a4cb6634d06120bc2fa943508ae1125915480f511e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b70d80ce63a4423c1c153bdb4d489ec092debf0f20017e21d47e05ed147b71d9`

```dockerfile
```

-	Layers:
	-	`sha256:0be1a3049197ac03e690e9365edd513ffeb121d05d4b6883a58c6356f44ce72f`  
		Last Modified: Tue, 30 Dec 2025 01:35:29 GMT  
		Size: 2.0 MB (2009665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4be7a57b181c7a7314b420b859583bfaa463e17fc94b8f57edc563abf95a3257`  
		Last Modified: Tue, 30 Dec 2025 01:35:30 GMT  
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
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57c33ac8581cd04f31208409f36331e938a78e6ae3a7a3b530fe9dfebe6eb9ad`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583aae99135b9036c602a1c60743fc4fd519f261ac6d48ed60b01e1beb019e7f`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 106.0 KB (106050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ca22885c42a537f033850e8dff7eaeddbb7514902286739b48c084b55a8d6b`  
		Last Modified: Thu, 18 Dec 2025 00:32:19 GMT  
		Size: 2.0 MB (1989265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d146e2038834770bed57033a6c5d66ead5b731b8b133856dec6726ca21baee9`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
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
		Last Modified: Thu, 18 Dec 2025 01:34:48 GMT  
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
		Last Modified: Thu, 18 Dec 2025 00:50:01 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01bb148ea8fbe93dd8097d85f9ee3cf547d314e669748b4239c05711b0d5f719`  
		Last Modified: Thu, 18 Dec 2025 00:50:02 GMT  
		Size: 102.7 KB (102652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6549359cda37ac41cf41a5ece5f37f1322a82f6b232f12e446c62840637093e`  
		Last Modified: Thu, 18 Dec 2025 00:50:02 GMT  
		Size: 1.9 MB (1939215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:041e37eaffefcfb0809564ddea591be3cd818de5530e2c853c0bc9a2fa25c116`  
		Last Modified: Thu, 18 Dec 2025 00:50:05 GMT  
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
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 1.9 MB (1897191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f237be962bb57c3f749904b5925c8e1d7e9013dfac7dd52cc9611ada81858e`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
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
		Last Modified: Thu, 18 Dec 2025 01:34:55 GMT  
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
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb7b8445facedfc145b9478f74880f520776460f153005b7f437ec339aee530`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1853c901134389608b6e80aaa3e43cd67a35c71aecfdde4b5b7ed3b989a03c`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 121.9 KB (121860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a01d1ac5ce47f4494363e411e1cd25dea26438213a2d18d6bb104d0974d9a52`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 2.0 MB (1966561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115624f24ba74d393c2da3d65ed5b35a7afb3fa9ad143d3fb82c64953b3d0401`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87bba524314294ca97195ce65a35ec6d42d3f9f18c9cc0c05c064c9a3cf85c0`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
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
		Last Modified: Thu, 18 Dec 2025 00:32:41 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b2862af05c1582c8625c82ea0863dc2b6474e410d3e6a32876c920e0152c73`  
		Last Modified: Thu, 18 Dec 2025 00:32:42 GMT  
		Size: 110.7 KB (110740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30872a43f6c591fd9b979b49b0fb32107b4bfa8c1155657fa255aa199cf0b83b`  
		Last Modified: Thu, 18 Dec 2025 00:32:42 GMT  
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
		Last Modified: Thu, 18 Dec 2025 01:35:04 GMT  
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
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4079a2d61bafcf146b8f57b35f0e39bf2548e0963be10cff5086f9a56ccdd9d`  
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
		Size: 126.3 KB (126257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f69efa1066815d67cf415d0aac5dcd305032257b6bded5a4c57a7444a1e7fd4`  
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
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
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f270744f8d8b82bc6657387109b33836a76d6dbf8faa645a997db7ea290cdb`  
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
		Size: 114.3 KB (114299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91f8ee8f36703944a7bdcaf57cc5772fe9f79c74a088c33fa1b6da7de119f93`  
		Last Modified: Thu, 18 Dec 2025 00:34:02 GMT  
		Size: 2.0 MB (2017131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e21d2db88668745770273c7b36d4d2c1e87a80b0118b8d775813860b467384c8`  
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd847159e169b898a67d4454fd5a22406c5ae623b16889d084a1d5f2d46a499`  
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
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
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57c33ac8581cd04f31208409f36331e938a78e6ae3a7a3b530fe9dfebe6eb9ad`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583aae99135b9036c602a1c60743fc4fd519f261ac6d48ed60b01e1beb019e7f`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 106.0 KB (106050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ca22885c42a537f033850e8dff7eaeddbb7514902286739b48c084b55a8d6b`  
		Last Modified: Thu, 18 Dec 2025 00:32:19 GMT  
		Size: 2.0 MB (1989265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d146e2038834770bed57033a6c5d66ead5b731b8b133856dec6726ca21baee9`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
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
		Last Modified: Thu, 18 Dec 2025 01:34:48 GMT  
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
		Last Modified: Thu, 18 Dec 2025 00:50:01 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01bb148ea8fbe93dd8097d85f9ee3cf547d314e669748b4239c05711b0d5f719`  
		Last Modified: Thu, 18 Dec 2025 00:50:02 GMT  
		Size: 102.7 KB (102652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6549359cda37ac41cf41a5ece5f37f1322a82f6b232f12e446c62840637093e`  
		Last Modified: Thu, 18 Dec 2025 00:50:02 GMT  
		Size: 1.9 MB (1939215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:041e37eaffefcfb0809564ddea591be3cd818de5530e2c853c0bc9a2fa25c116`  
		Last Modified: Thu, 18 Dec 2025 00:50:05 GMT  
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
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 1.9 MB (1897191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f237be962bb57c3f749904b5925c8e1d7e9013dfac7dd52cc9611ada81858e`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
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
		Last Modified: Thu, 18 Dec 2025 01:34:55 GMT  
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
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb7b8445facedfc145b9478f74880f520776460f153005b7f437ec339aee530`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1853c901134389608b6e80aaa3e43cd67a35c71aecfdde4b5b7ed3b989a03c`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 121.9 KB (121860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a01d1ac5ce47f4494363e411e1cd25dea26438213a2d18d6bb104d0974d9a52`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 2.0 MB (1966561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115624f24ba74d393c2da3d65ed5b35a7afb3fa9ad143d3fb82c64953b3d0401`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87bba524314294ca97195ce65a35ec6d42d3f9f18c9cc0c05c064c9a3cf85c0`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
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
		Last Modified: Thu, 18 Dec 2025 00:32:41 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b2862af05c1582c8625c82ea0863dc2b6474e410d3e6a32876c920e0152c73`  
		Last Modified: Thu, 18 Dec 2025 00:32:42 GMT  
		Size: 110.7 KB (110740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30872a43f6c591fd9b979b49b0fb32107b4bfa8c1155657fa255aa199cf0b83b`  
		Last Modified: Thu, 18 Dec 2025 00:32:42 GMT  
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
		Last Modified: Thu, 18 Dec 2025 01:35:04 GMT  
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
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4079a2d61bafcf146b8f57b35f0e39bf2548e0963be10cff5086f9a56ccdd9d`  
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
		Size: 126.3 KB (126257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f69efa1066815d67cf415d0aac5dcd305032257b6bded5a4c57a7444a1e7fd4`  
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
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
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f270744f8d8b82bc6657387109b33836a76d6dbf8faa645a997db7ea290cdb`  
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
		Size: 114.3 KB (114299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91f8ee8f36703944a7bdcaf57cc5772fe9f79c74a088c33fa1b6da7de119f93`  
		Last Modified: Thu, 18 Dec 2025 00:34:02 GMT  
		Size: 2.0 MB (2017131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e21d2db88668745770273c7b36d4d2c1e87a80b0118b8d775813860b467384c8`  
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd847159e169b898a67d4454fd5a22406c5ae623b16889d084a1d5f2d46a499`  
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
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
$ docker pull memcached@sha256:36c36f0c38cda62ab29af64a0eefa53e99879265ff70df8ac12597be28c482f7
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
$ docker pull memcached@sha256:61bcd214c8da24f2bacfd9152bccafef4f4c0993897c945ee3058106e084b314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32193395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5dafc7d411a870fbc52ca64194006e50e355d34f1edf56b4e1dc5b8019b0934`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:21:34 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 29 Dec 2025 23:21:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:24:22 GMT
ENV MEMCACHED_VERSION=1.6.40
# Mon, 29 Dec 2025 23:24:22 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Mon, 29 Dec 2025 23:24:22 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Mon, 29 Dec 2025 23:24:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 29 Dec 2025 23:24:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:24:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 29 Dec 2025 23:24:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:24:22 GMT
USER memcache
# Mon, 29 Dec 2025 23:24:22 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 29 Dec 2025 23:24:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d08d8001380dd7c5a9be2e59244310ccfa7e84f3b896b354059d46d1928401`  
		Last Modified: Mon, 29 Dec 2025 23:24:36 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8420bae5d2af8b5b5e66d7e5ba882f5e2034cc64eacfb1a0b4b32a259a541b16`  
		Last Modified: Mon, 29 Dec 2025 23:24:35 GMT  
		Size: 136.7 KB (136694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc2daf1b2287468ea06570c5bedff8bc84ab6833050a7e0686f5f7d7a2679e1`  
		Last Modified: Mon, 29 Dec 2025 23:24:35 GMT  
		Size: 2.3 MB (2278657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a54c348dd92d8a79d150c1fe56008dba798b633f010e1e57c0a18f62b2752d90`  
		Last Modified: Mon, 29 Dec 2025 23:24:35 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e147936d0f858c8f726dea003b7220347e43918cab2714f81c66c1553cc160cd`  
		Last Modified: Mon, 29 Dec 2025 23:24:35 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:e6d0cef74a4a91255f97601317c1cd45953291e56aebea597b1f5fedb87772df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a114559b11eef9830f21c5cfd0b3dff0712acd507604d89ab89f16d229d637c`

```dockerfile
```

-	Layers:
	-	`sha256:31d77d05cfee83189fed485cbb6de83d56b3fc5c8a37eafd4e5ab2a8646bcee5`  
		Last Modified: Tue, 30 Dec 2025 04:34:52 GMT  
		Size: 2.0 MB (2008228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:daae5d64f19c0b653f152172ab207032a103d7a2c198208a2472a4565869c64e`  
		Last Modified: Tue, 30 Dec 2025 04:34:53 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-trixie` - linux; arm variant v5

```console
$ docker pull memcached@sha256:19778ab8ffe04b579956362255d1b4be4646df675a0c0db5662d882e7e062834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30300227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85e834ef35584236d3b04d1823e406899096de386d548c5f0bfd896cfba41631`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:17:23 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 29 Dec 2025 23:17:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:39:32 GMT
ENV MEMCACHED_VERSION=1.6.40
# Mon, 29 Dec 2025 23:39:32 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Mon, 29 Dec 2025 23:39:32 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Mon, 29 Dec 2025 23:39:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 29 Dec 2025 23:39:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:39:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 29 Dec 2025 23:39:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:39:32 GMT
USER memcache
# Mon, 29 Dec 2025 23:39:32 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 29 Dec 2025 23:39:32 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b99a8d8dab982a1a4ea341e66b178b14c0f373c2cd90ac46a67308a4f43c82ae`  
		Last Modified: Mon, 29 Dec 2025 22:27:09 GMT  
		Size: 27.9 MB (27944146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0be68f37541245f1acaee607441dfc983a00e90d78d5e0941265d0b67b1cc9a`  
		Last Modified: Mon, 29 Dec 2025 23:39:44 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10905a7698a57312678edda9f8fc0748b6288699f5fed1f8e7e7e909240d441`  
		Last Modified: Mon, 29 Dec 2025 23:39:44 GMT  
		Size: 144.1 KB (144149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea062eb6d6681b78497a81a8d5ca89088b56f5a5d629e3124df93b9ca0e4f16`  
		Last Modified: Mon, 29 Dec 2025 23:39:44 GMT  
		Size: 2.2 MB (2210419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d59770b8679e935091911e6294f61a53df8f59b5cc8aae431217cc391864a0`  
		Last Modified: Mon, 29 Dec 2025 23:39:44 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945c1d27fa6617071d97eddd3d962ac571276f7f757f99edc1a93ebbe6eb5a9c`  
		Last Modified: Mon, 29 Dec 2025 23:39:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:27e3afeed14c4cac078a10db01ef22eef58848fc65d93501050f872bc3cf64d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:939368d93857b65d5e6bbdc97a5f4d158eeca9efc9fb02875eae93350ea663fb`

```dockerfile
```

-	Layers:
	-	`sha256:3559f8384ca294c984900b7325032abfe47459734f215e79264a22aa23802031`  
		Last Modified: Tue, 30 Dec 2025 01:35:12 GMT  
		Size: 2.0 MB (2011231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b310c8a994e22e59ca814cd06500201d5b78c4bbfe3baa8785ae093760d4a4fb`  
		Last Modified: Tue, 30 Dec 2025 01:35:13 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-trixie` - linux; arm variant v7

```console
$ docker pull memcached@sha256:34f932820fcffc223d050d31ceeef236f4bc4a1a8e776006560fe2ef14348a2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28510848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0a0c32503881f91ec515af1fd074032b8070eac0faa4afca5e1f2f60609b237`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:17:22 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 29 Dec 2025 23:17:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:20:31 GMT
ENV MEMCACHED_VERSION=1.6.40
# Mon, 29 Dec 2025 23:20:31 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Mon, 29 Dec 2025 23:20:31 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Mon, 29 Dec 2025 23:20:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 29 Dec 2025 23:20:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:20:31 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 29 Dec 2025 23:20:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:20:31 GMT
USER memcache
# Mon, 29 Dec 2025 23:20:31 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 29 Dec 2025 23:20:31 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6d3e0fea3cb8eb29b9c06956265b47cd00f7ebfb48e35e818f686d52c21353f5`  
		Last Modified: Mon, 29 Dec 2025 22:28:07 GMT  
		Size: 26.2 MB (26210001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f916949d5244227fca363e62638c31c65e0f6a941ceaa0fb79c37d962e9b95bb`  
		Last Modified: Mon, 29 Dec 2025 23:20:45 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f24598f250037f41edf0d0093ed08f2b3b3937f91d7708c687330e0feca3fdcf`  
		Last Modified: Mon, 29 Dec 2025 23:20:45 GMT  
		Size: 135.4 KB (135362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f260cb2adbfa9ad1d74da541da12d2146b1a06685021b42e924c843481237ee2`  
		Last Modified: Mon, 29 Dec 2025 23:20:46 GMT  
		Size: 2.2 MB (2163975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0f315cda938284ce51afa280bd8e89b891448b2da00c28c66c638c2d4a4cc6`  
		Last Modified: Mon, 29 Dec 2025 23:20:45 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c38a3204b12ac8ee46611fe38ab1a706ee2c310f8a4e0439862ee702d7b5481c`  
		Last Modified: Mon, 29 Dec 2025 23:20:45 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:4c6e114c037bf19003547b10ffc5b077c88be25cd990cd30d1f26945409bf69c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5de9929189cfe8912f0ebace1f73497b21396b8561e62dab4d98cefa02760f10`

```dockerfile
```

-	Layers:
	-	`sha256:1bc6b02786844de8506e80bae2bf850ea8bf7875761b0a8ff17497e18e297086`  
		Last Modified: Tue, 30 Dec 2025 04:34:58 GMT  
		Size: 2.0 MB (2009688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48de2da0a0a924a9a938d6ea9a12b2eb727da5a33bad6987e74e57dcfdc66f51`  
		Last Modified: Tue, 30 Dec 2025 04:34:59 GMT  
		Size: 22.3 KB (22303 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-trixie` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:517aefb9e9ff071c2aa387ca68e1b63663f210c5bc838b8d928cb657795329fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32554923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20bd9e6ac4a3626ae8b8108e846570938ea003859e516dcd2134d2d628fd2c79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:21:52 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 29 Dec 2025 23:21:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:24:52 GMT
ENV MEMCACHED_VERSION=1.6.40
# Mon, 29 Dec 2025 23:24:52 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Mon, 29 Dec 2025 23:24:52 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Mon, 29 Dec 2025 23:24:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 29 Dec 2025 23:24:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:24:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 29 Dec 2025 23:24:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:24:52 GMT
USER memcache
# Mon, 29 Dec 2025 23:24:52 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 29 Dec 2025 23:24:52 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d74ee4724223b1c44d3bdff5ee6ee8c7eceabc636fe61128ec308914b5999f8`  
		Last Modified: Mon, 29 Dec 2025 23:25:06 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d74224a341d3e408a0affb0b0eb0c53f99939a1b669f25e6b34026f224a3745`  
		Last Modified: Mon, 29 Dec 2025 23:25:06 GMT  
		Size: 153.5 KB (153455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5db3b7f17de3125f5608801faf4e6a1615d96c6be2fa7f1c09e52d0cd7cd80`  
		Last Modified: Mon, 29 Dec 2025 23:25:06 GMT  
		Size: 2.3 MB (2261324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885dc482553144838528b69fa53518cc1fafb03d7eac91e773730285029e30e9`  
		Last Modified: Mon, 29 Dec 2025 23:25:06 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8afa8cb30ddae48c82fab84d30d0457bfa667059caff286dcfc57999e07a8b1`  
		Last Modified: Mon, 29 Dec 2025 23:25:06 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:62c7db64a99cd405d4330dc5c878884ef8a0e107864d7314a4cb66a8242b7dee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cfb248343584b4b08d6f7b363daf97f9506e303159317383e87ae5b82750335`

```dockerfile
```

-	Layers:
	-	`sha256:f38f799c754160125bc6daafe2fc1bd335001b11d94be74b560069268f8246e4`  
		Last Modified: Tue, 30 Dec 2025 04:35:02 GMT  
		Size: 2.0 MB (2008544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad51b10b5d6e7e377d3219a2f60c17ba2d754739a985c052724e0826650144fc`  
		Last Modified: Tue, 30 Dec 2025 04:35:03 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-trixie` - linux; 386

```console
$ docker pull memcached@sha256:0be60a562cdf0c05ebc768c0de49cf333584a650766b962f308610539a885a4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33665696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7b7c835420cd1e7ae8cd0eb0b0df1b2020c581061f1938dfa5292723e395058`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:17:02 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 29 Dec 2025 23:17:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:19:58 GMT
ENV MEMCACHED_VERSION=1.6.40
# Mon, 29 Dec 2025 23:19:58 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Mon, 29 Dec 2025 23:19:58 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Mon, 29 Dec 2025 23:19:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 29 Dec 2025 23:19:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:19:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 29 Dec 2025 23:19:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:19:58 GMT
USER memcache
# Mon, 29 Dec 2025 23:19:58 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 29 Dec 2025 23:19:58 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:796ffff142a3158a5c48a8d81b8b722c5cf4889d5e22da70bdd13a6459d6e40b`  
		Last Modified: Mon, 29 Dec 2025 22:27:31 GMT  
		Size: 31.3 MB (31293100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8fc762766a28f1d89093cb569234311423930c02de910408e80cad47e30647`  
		Last Modified: Mon, 29 Dec 2025 23:20:11 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b725b75ef28bdf7d63e19355a971dc87c6501efa1f70edbee592d52e763fee94`  
		Last Modified: Mon, 29 Dec 2025 23:20:11 GMT  
		Size: 147.5 KB (147508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9509121c0551cdeef95fef92e5598954065e802767669466cffb6c8dada5c3`  
		Last Modified: Mon, 29 Dec 2025 23:20:11 GMT  
		Size: 2.2 MB (2223574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f6e90b6aa0c5dbad71d717fad6007d2dfc7dbc186fa2c07eb8ce8416168801`  
		Last Modified: Mon, 29 Dec 2025 23:20:11 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4fa5d83d611a53674f14bb3fea7ff4465d235101cd9c5640e6c822413b3f4e`  
		Last Modified: Mon, 29 Dec 2025 23:20:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:2f28d2975c37dc6c21579400a4d8a911f45c78e460466164e094c3b114a8a739
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b72a726f712c69433343b634304351532be5cd25051c5bba2f1842cbe52c9fd`

```dockerfile
```

-	Layers:
	-	`sha256:0b522eb7b1ed969865d6941e83230cfad34490504dd209cdf0a9574b09a02415`  
		Last Modified: Tue, 30 Dec 2025 04:35:06 GMT  
		Size: 2.0 MB (2005385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9244708212b7f5f5094918a876558a69b2ba5df9e6a6187f1f97b3dd699465a`  
		Last Modified: Tue, 30 Dec 2025 04:35:08 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-trixie` - linux; ppc64le

```console
$ docker pull memcached@sha256:38a236f83eb206f786b39c53e8f756815f0bda1460157b11844faf21735208bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36162589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d41292f5c75fe5f3a464b809bde41e0ae8849ad8d7046918a548d0c6b2e250a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 21:34:54 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 17 Dec 2025 21:35:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:28 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:28 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:28 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ddd908d99c8b32da8685339ba6296773100f66e08c8bf508ab82174ba5a4f600`  
		Last Modified: Tue, 09 Dec 2025 00:06:51 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d2b42546c7b688160cfd1a0da61a24922a019b4ebead88e23aff01482ddd477`  
		Last Modified: Wed, 17 Dec 2025 21:38:49 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4efe9fd2e012174cd86a64f83d7b7facfe14ee67c9c9fa5ce994f22c24173f2c`  
		Last Modified: Wed, 17 Dec 2025 21:38:49 GMT  
		Size: 170.4 KB (170393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9752985ba696f0f8d5831ac91e19bfe336342b1c403542641c575b1dc6116e`  
		Last Modified: Wed, 17 Dec 2025 21:38:49 GMT  
		Size: 2.4 MB (2393786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d11c68ba0bc913d139eea51cb2957c1ddd713515fc06dfa5d4c398b119535a`  
		Last Modified: Wed, 17 Dec 2025 21:38:49 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9186b8b7184cef442ae3ed6a3feadcaa8f4ccc974ed5ae6c6cf8efe37e679f23`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:00d1019e9978171df76f638253f212405bf7d53251607ef5a5933d5b28d867b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:588d3d6ab54a9ea5c8baf9b013bb23c12826989ba0d09cb862431e2fa30e5189`

```dockerfile
```

-	Layers:
	-	`sha256:799ad025578a6d5d0155dc5be223bfbc25ffa3aa0548e4fb2e4bedeb0a5088d9`  
		Last Modified: Wed, 17 Dec 2025 22:35:03 GMT  
		Size: 2.0 MB (2011829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eaa03114ccb63fbbd8ca04eef46baa26c8a0508f1256aa45d851f3a49f2ed47a`  
		Last Modified: Wed, 17 Dec 2025 22:35:04 GMT  
		Size: 22.2 KB (22225 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-trixie` - linux; riscv64

```console
$ docker pull memcached@sha256:30d185f5c04056622fe346fecdf9a07a4d861871fef4028424c9b38e979d2ba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30615105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6048e6bd3b428597fcae4887d0b69fb252944cd1c8afdd85045a4e4c68837ecf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 03:48:33 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 30 Dec 2025 03:49:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 04:02:23 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 30 Dec 2025 04:02:23 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 30 Dec 2025 04:02:23 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 30 Dec 2025 04:02:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 30 Dec 2025 04:02:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Dec 2025 04:02:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 30 Dec 2025 04:02:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Dec 2025 04:02:23 GMT
USER memcache
# Tue, 30 Dec 2025 04:02:23 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 30 Dec 2025 04:02:23 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:96d8ad310358e2403b7b44cf38db606dc1ea6b58b915684d38e13f573860f64e`  
		Last Modified: Tue, 30 Dec 2025 00:53:22 GMT  
		Size: 28.3 MB (28273129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d30361332d6c36fa201043e1df585bb5cea535dfbf760f9b2ed1827c4a53ac`  
		Last Modified: Tue, 30 Dec 2025 04:03:16 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe44badb419e8d40ff093c52477fa45ed79bb9d483ed2f517359e5583617d73a`  
		Last Modified: Tue, 30 Dec 2025 04:03:17 GMT  
		Size: 133.1 KB (133088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a36426c8facdb7304fc9999aee0ca442e6e3b75be15714fa9cadff5589e57f20`  
		Last Modified: Tue, 30 Dec 2025 04:03:16 GMT  
		Size: 2.2 MB (2207375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7820ce69e6809e314e3ef1cf5cc6d3c2bafcd597d9eaf7f0f491c3ea69249db`  
		Last Modified: Tue, 30 Dec 2025 04:03:16 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc77699b8548736e5d2fa9873720c2f41ddfbc89354a6f902b7e5b5651ad0135`  
		Last Modified: Tue, 30 Dec 2025 04:03:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:7f4ca8337c70973f8b5a8eb90158eacfc3a792f5af42d7edf68da0a3a4846cd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a70852a9b9663c0d61ac529b72228ba271972017a65a149b4af634dadda75c5b`

```dockerfile
```

-	Layers:
	-	`sha256:45586a078529026200d6db8b774cf2db02f7292ac8bd6cfd4f8e68ddbe883e64`  
		Last Modified: Tue, 30 Dec 2025 04:35:15 GMT  
		Size: 2.0 MB (2002192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e23345b5880eafecc6509da78e5a9b8e6e95ce6050b2ecb71bb24c1aa03342e5`  
		Last Modified: Tue, 30 Dec 2025 04:35:15 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.40-trixie` - linux; s390x

```console
$ docker pull memcached@sha256:e513e62f8a86f2c8f23e06b9b73d141d7e53163ab557ec297be5f3c682a70bc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32273670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd4c0f39122c5c6e9cb01d08aebb1281a0ce18244cbc1e051742de47c5bd51f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:17:26 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 29 Dec 2025 23:17:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:20:38 GMT
ENV MEMCACHED_VERSION=1.6.40
# Mon, 29 Dec 2025 23:20:38 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Mon, 29 Dec 2025 23:20:38 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Mon, 29 Dec 2025 23:20:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 29 Dec 2025 23:20:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:20:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 29 Dec 2025 23:20:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:20:38 GMT
USER memcache
# Mon, 29 Dec 2025 23:20:38 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 29 Dec 2025 23:20:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c9a83915f7d4b9d7fbe5dceeedd49718d2702fd67d78b63a38ec344f3fbfcc41`  
		Last Modified: Mon, 29 Dec 2025 22:27:07 GMT  
		Size: 29.8 MB (29834418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1fd9e99d807cb897b4653efa7815d408df0bb7175d7fb89ab19b79b7737dc1d`  
		Last Modified: Mon, 29 Dec 2025 23:20:55 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7251a4bef45871483e5419196b0bd7ee7440a6dcc98993bd541eb9cf6ee89b06`  
		Last Modified: Mon, 29 Dec 2025 23:20:55 GMT  
		Size: 140.5 KB (140511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16461f97f95d5d1b2cb64bc91ad5a73d23e505f74a1cf95eeb9de840c9a06488`  
		Last Modified: Mon, 29 Dec 2025 23:20:55 GMT  
		Size: 2.3 MB (2297231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa6eecd4b590cab77eae19d421ebb50ce6ed90281723d604c775bcb78b5408f`  
		Last Modified: Mon, 29 Dec 2025 23:20:55 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2779e4a3a9763cc09cc4694ec9a5b304164f44aa2869a8ccbca67eeca523c305`  
		Last Modified: Mon, 29 Dec 2025 23:20:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.40-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:89b3d47f58bd28d04b77c9a4cb6634d06120bc2fa943508ae1125915480f511e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b70d80ce63a4423c1c153bdb4d489ec092debf0f20017e21d47e05ed147b71d9`

```dockerfile
```

-	Layers:
	-	`sha256:0be1a3049197ac03e690e9365edd513ffeb121d05d4b6883a58c6356f44ce72f`  
		Last Modified: Tue, 30 Dec 2025 01:35:29 GMT  
		Size: 2.0 MB (2009665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4be7a57b181c7a7314b420b859583bfaa463e17fc94b8f57edc563abf95a3257`  
		Last Modified: Tue, 30 Dec 2025 01:35:30 GMT  
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
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57c33ac8581cd04f31208409f36331e938a78e6ae3a7a3b530fe9dfebe6eb9ad`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583aae99135b9036c602a1c60743fc4fd519f261ac6d48ed60b01e1beb019e7f`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 106.0 KB (106050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ca22885c42a537f033850e8dff7eaeddbb7514902286739b48c084b55a8d6b`  
		Last Modified: Thu, 18 Dec 2025 00:32:19 GMT  
		Size: 2.0 MB (1989265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d146e2038834770bed57033a6c5d66ead5b731b8b133856dec6726ca21baee9`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
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
		Last Modified: Thu, 18 Dec 2025 01:34:48 GMT  
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
		Last Modified: Thu, 18 Dec 2025 00:50:01 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01bb148ea8fbe93dd8097d85f9ee3cf547d314e669748b4239c05711b0d5f719`  
		Last Modified: Thu, 18 Dec 2025 00:50:02 GMT  
		Size: 102.7 KB (102652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6549359cda37ac41cf41a5ece5f37f1322a82f6b232f12e446c62840637093e`  
		Last Modified: Thu, 18 Dec 2025 00:50:02 GMT  
		Size: 1.9 MB (1939215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:041e37eaffefcfb0809564ddea591be3cd818de5530e2c853c0bc9a2fa25c116`  
		Last Modified: Thu, 18 Dec 2025 00:50:05 GMT  
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
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 1.9 MB (1897191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f237be962bb57c3f749904b5925c8e1d7e9013dfac7dd52cc9611ada81858e`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
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
		Last Modified: Thu, 18 Dec 2025 01:34:55 GMT  
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
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb7b8445facedfc145b9478f74880f520776460f153005b7f437ec339aee530`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1853c901134389608b6e80aaa3e43cd67a35c71aecfdde4b5b7ed3b989a03c`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 121.9 KB (121860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a01d1ac5ce47f4494363e411e1cd25dea26438213a2d18d6bb104d0974d9a52`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 2.0 MB (1966561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115624f24ba74d393c2da3d65ed5b35a7afb3fa9ad143d3fb82c64953b3d0401`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87bba524314294ca97195ce65a35ec6d42d3f9f18c9cc0c05c064c9a3cf85c0`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
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
		Last Modified: Thu, 18 Dec 2025 00:32:41 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b2862af05c1582c8625c82ea0863dc2b6474e410d3e6a32876c920e0152c73`  
		Last Modified: Thu, 18 Dec 2025 00:32:42 GMT  
		Size: 110.7 KB (110740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30872a43f6c591fd9b979b49b0fb32107b4bfa8c1155657fa255aa199cf0b83b`  
		Last Modified: Thu, 18 Dec 2025 00:32:42 GMT  
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
		Last Modified: Thu, 18 Dec 2025 01:35:04 GMT  
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
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4079a2d61bafcf146b8f57b35f0e39bf2548e0963be10cff5086f9a56ccdd9d`  
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
		Size: 126.3 KB (126257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f69efa1066815d67cf415d0aac5dcd305032257b6bded5a4c57a7444a1e7fd4`  
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
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
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f270744f8d8b82bc6657387109b33836a76d6dbf8faa645a997db7ea290cdb`  
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
		Size: 114.3 KB (114299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91f8ee8f36703944a7bdcaf57cc5772fe9f79c74a088c33fa1b6da7de119f93`  
		Last Modified: Thu, 18 Dec 2025 00:34:02 GMT  
		Size: 2.0 MB (2017131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e21d2db88668745770273c7b36d4d2c1e87a80b0118b8d775813860b467384c8`  
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd847159e169b898a67d4454fd5a22406c5ae623b16889d084a1d5f2d46a499`  
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
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
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57c33ac8581cd04f31208409f36331e938a78e6ae3a7a3b530fe9dfebe6eb9ad`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583aae99135b9036c602a1c60743fc4fd519f261ac6d48ed60b01e1beb019e7f`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 106.0 KB (106050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ca22885c42a537f033850e8dff7eaeddbb7514902286739b48c084b55a8d6b`  
		Last Modified: Thu, 18 Dec 2025 00:32:19 GMT  
		Size: 2.0 MB (1989265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d146e2038834770bed57033a6c5d66ead5b731b8b133856dec6726ca21baee9`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
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
		Last Modified: Thu, 18 Dec 2025 01:34:48 GMT  
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
		Last Modified: Thu, 18 Dec 2025 00:50:01 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01bb148ea8fbe93dd8097d85f9ee3cf547d314e669748b4239c05711b0d5f719`  
		Last Modified: Thu, 18 Dec 2025 00:50:02 GMT  
		Size: 102.7 KB (102652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6549359cda37ac41cf41a5ece5f37f1322a82f6b232f12e446c62840637093e`  
		Last Modified: Thu, 18 Dec 2025 00:50:02 GMT  
		Size: 1.9 MB (1939215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:041e37eaffefcfb0809564ddea591be3cd818de5530e2c853c0bc9a2fa25c116`  
		Last Modified: Thu, 18 Dec 2025 00:50:05 GMT  
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
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
		Size: 1.9 MB (1897191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f237be962bb57c3f749904b5925c8e1d7e9013dfac7dd52cc9611ada81858e`  
		Last Modified: Thu, 18 Dec 2025 00:34:03 GMT  
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
		Last Modified: Thu, 18 Dec 2025 01:34:55 GMT  
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
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb7b8445facedfc145b9478f74880f520776460f153005b7f437ec339aee530`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1853c901134389608b6e80aaa3e43cd67a35c71aecfdde4b5b7ed3b989a03c`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 121.9 KB (121860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a01d1ac5ce47f4494363e411e1cd25dea26438213a2d18d6bb104d0974d9a52`  
		Last Modified: Thu, 18 Dec 2025 00:32:18 GMT  
		Size: 2.0 MB (1966561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115624f24ba74d393c2da3d65ed5b35a7afb3fa9ad143d3fb82c64953b3d0401`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87bba524314294ca97195ce65a35ec6d42d3f9f18c9cc0c05c064c9a3cf85c0`  
		Last Modified: Thu, 18 Dec 2025 00:32:17 GMT  
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
		Last Modified: Thu, 18 Dec 2025 00:32:41 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b2862af05c1582c8625c82ea0863dc2b6474e410d3e6a32876c920e0152c73`  
		Last Modified: Thu, 18 Dec 2025 00:32:42 GMT  
		Size: 110.7 KB (110740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30872a43f6c591fd9b979b49b0fb32107b4bfa8c1155657fa255aa199cf0b83b`  
		Last Modified: Thu, 18 Dec 2025 00:32:42 GMT  
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
		Last Modified: Thu, 18 Dec 2025 01:35:04 GMT  
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
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4079a2d61bafcf146b8f57b35f0e39bf2548e0963be10cff5086f9a56ccdd9d`  
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
		Size: 126.3 KB (126257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f69efa1066815d67cf415d0aac5dcd305032257b6bded5a4c57a7444a1e7fd4`  
		Last Modified: Thu, 18 Dec 2025 00:36:33 GMT  
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
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f270744f8d8b82bc6657387109b33836a76d6dbf8faa645a997db7ea290cdb`  
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
		Size: 114.3 KB (114299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91f8ee8f36703944a7bdcaf57cc5772fe9f79c74a088c33fa1b6da7de119f93`  
		Last Modified: Thu, 18 Dec 2025 00:34:02 GMT  
		Size: 2.0 MB (2017131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e21d2db88668745770273c7b36d4d2c1e87a80b0118b8d775813860b467384c8`  
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd847159e169b898a67d4454fd5a22406c5ae623b16889d084a1d5f2d46a499`  
		Last Modified: Thu, 18 Dec 2025 00:34:01 GMT  
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
$ docker pull memcached@sha256:36c36f0c38cda62ab29af64a0eefa53e99879265ff70df8ac12597be28c482f7
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
$ docker pull memcached@sha256:61bcd214c8da24f2bacfd9152bccafef4f4c0993897c945ee3058106e084b314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32193395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5dafc7d411a870fbc52ca64194006e50e355d34f1edf56b4e1dc5b8019b0934`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:21:34 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 29 Dec 2025 23:21:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:24:22 GMT
ENV MEMCACHED_VERSION=1.6.40
# Mon, 29 Dec 2025 23:24:22 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Mon, 29 Dec 2025 23:24:22 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Mon, 29 Dec 2025 23:24:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 29 Dec 2025 23:24:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:24:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 29 Dec 2025 23:24:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:24:22 GMT
USER memcache
# Mon, 29 Dec 2025 23:24:22 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 29 Dec 2025 23:24:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d08d8001380dd7c5a9be2e59244310ccfa7e84f3b896b354059d46d1928401`  
		Last Modified: Mon, 29 Dec 2025 23:24:36 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8420bae5d2af8b5b5e66d7e5ba882f5e2034cc64eacfb1a0b4b32a259a541b16`  
		Last Modified: Mon, 29 Dec 2025 23:24:35 GMT  
		Size: 136.7 KB (136694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc2daf1b2287468ea06570c5bedff8bc84ab6833050a7e0686f5f7d7a2679e1`  
		Last Modified: Mon, 29 Dec 2025 23:24:35 GMT  
		Size: 2.3 MB (2278657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a54c348dd92d8a79d150c1fe56008dba798b633f010e1e57c0a18f62b2752d90`  
		Last Modified: Mon, 29 Dec 2025 23:24:35 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e147936d0f858c8f726dea003b7220347e43918cab2714f81c66c1553cc160cd`  
		Last Modified: Mon, 29 Dec 2025 23:24:35 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:e6d0cef74a4a91255f97601317c1cd45953291e56aebea597b1f5fedb87772df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a114559b11eef9830f21c5cfd0b3dff0712acd507604d89ab89f16d229d637c`

```dockerfile
```

-	Layers:
	-	`sha256:31d77d05cfee83189fed485cbb6de83d56b3fc5c8a37eafd4e5ab2a8646bcee5`  
		Last Modified: Tue, 30 Dec 2025 04:34:52 GMT  
		Size: 2.0 MB (2008228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:daae5d64f19c0b653f152172ab207032a103d7a2c198208a2472a4565869c64e`  
		Last Modified: Tue, 30 Dec 2025 04:34:53 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm variant v5

```console
$ docker pull memcached@sha256:19778ab8ffe04b579956362255d1b4be4646df675a0c0db5662d882e7e062834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30300227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85e834ef35584236d3b04d1823e406899096de386d548c5f0bfd896cfba41631`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:17:23 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 29 Dec 2025 23:17:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:39:32 GMT
ENV MEMCACHED_VERSION=1.6.40
# Mon, 29 Dec 2025 23:39:32 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Mon, 29 Dec 2025 23:39:32 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Mon, 29 Dec 2025 23:39:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 29 Dec 2025 23:39:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:39:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 29 Dec 2025 23:39:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:39:32 GMT
USER memcache
# Mon, 29 Dec 2025 23:39:32 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 29 Dec 2025 23:39:32 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b99a8d8dab982a1a4ea341e66b178b14c0f373c2cd90ac46a67308a4f43c82ae`  
		Last Modified: Mon, 29 Dec 2025 22:27:09 GMT  
		Size: 27.9 MB (27944146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0be68f37541245f1acaee607441dfc983a00e90d78d5e0941265d0b67b1cc9a`  
		Last Modified: Mon, 29 Dec 2025 23:39:44 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10905a7698a57312678edda9f8fc0748b6288699f5fed1f8e7e7e909240d441`  
		Last Modified: Mon, 29 Dec 2025 23:39:44 GMT  
		Size: 144.1 KB (144149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea062eb6d6681b78497a81a8d5ca89088b56f5a5d629e3124df93b9ca0e4f16`  
		Last Modified: Mon, 29 Dec 2025 23:39:44 GMT  
		Size: 2.2 MB (2210419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d59770b8679e935091911e6294f61a53df8f59b5cc8aae431217cc391864a0`  
		Last Modified: Mon, 29 Dec 2025 23:39:44 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945c1d27fa6617071d97eddd3d962ac571276f7f757f99edc1a93ebbe6eb5a9c`  
		Last Modified: Mon, 29 Dec 2025 23:39:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:27e3afeed14c4cac078a10db01ef22eef58848fc65d93501050f872bc3cf64d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:939368d93857b65d5e6bbdc97a5f4d158eeca9efc9fb02875eae93350ea663fb`

```dockerfile
```

-	Layers:
	-	`sha256:3559f8384ca294c984900b7325032abfe47459734f215e79264a22aa23802031`  
		Last Modified: Tue, 30 Dec 2025 01:35:12 GMT  
		Size: 2.0 MB (2011231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b310c8a994e22e59ca814cd06500201d5b78c4bbfe3baa8785ae093760d4a4fb`  
		Last Modified: Tue, 30 Dec 2025 01:35:13 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm variant v7

```console
$ docker pull memcached@sha256:34f932820fcffc223d050d31ceeef236f4bc4a1a8e776006560fe2ef14348a2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28510848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0a0c32503881f91ec515af1fd074032b8070eac0faa4afca5e1f2f60609b237`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:17:22 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 29 Dec 2025 23:17:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:20:31 GMT
ENV MEMCACHED_VERSION=1.6.40
# Mon, 29 Dec 2025 23:20:31 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Mon, 29 Dec 2025 23:20:31 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Mon, 29 Dec 2025 23:20:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 29 Dec 2025 23:20:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:20:31 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 29 Dec 2025 23:20:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:20:31 GMT
USER memcache
# Mon, 29 Dec 2025 23:20:31 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 29 Dec 2025 23:20:31 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6d3e0fea3cb8eb29b9c06956265b47cd00f7ebfb48e35e818f686d52c21353f5`  
		Last Modified: Mon, 29 Dec 2025 22:28:07 GMT  
		Size: 26.2 MB (26210001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f916949d5244227fca363e62638c31c65e0f6a941ceaa0fb79c37d962e9b95bb`  
		Last Modified: Mon, 29 Dec 2025 23:20:45 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f24598f250037f41edf0d0093ed08f2b3b3937f91d7708c687330e0feca3fdcf`  
		Last Modified: Mon, 29 Dec 2025 23:20:45 GMT  
		Size: 135.4 KB (135362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f260cb2adbfa9ad1d74da541da12d2146b1a06685021b42e924c843481237ee2`  
		Last Modified: Mon, 29 Dec 2025 23:20:46 GMT  
		Size: 2.2 MB (2163975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0f315cda938284ce51afa280bd8e89b891448b2da00c28c66c638c2d4a4cc6`  
		Last Modified: Mon, 29 Dec 2025 23:20:45 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c38a3204b12ac8ee46611fe38ab1a706ee2c310f8a4e0439862ee702d7b5481c`  
		Last Modified: Mon, 29 Dec 2025 23:20:45 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:4c6e114c037bf19003547b10ffc5b077c88be25cd990cd30d1f26945409bf69c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5de9929189cfe8912f0ebace1f73497b21396b8561e62dab4d98cefa02760f10`

```dockerfile
```

-	Layers:
	-	`sha256:1bc6b02786844de8506e80bae2bf850ea8bf7875761b0a8ff17497e18e297086`  
		Last Modified: Tue, 30 Dec 2025 04:34:58 GMT  
		Size: 2.0 MB (2009688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48de2da0a0a924a9a938d6ea9a12b2eb727da5a33bad6987e74e57dcfdc66f51`  
		Last Modified: Tue, 30 Dec 2025 04:34:59 GMT  
		Size: 22.3 KB (22303 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:517aefb9e9ff071c2aa387ca68e1b63663f210c5bc838b8d928cb657795329fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32554923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20bd9e6ac4a3626ae8b8108e846570938ea003859e516dcd2134d2d628fd2c79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:21:52 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 29 Dec 2025 23:21:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:24:52 GMT
ENV MEMCACHED_VERSION=1.6.40
# Mon, 29 Dec 2025 23:24:52 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Mon, 29 Dec 2025 23:24:52 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Mon, 29 Dec 2025 23:24:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 29 Dec 2025 23:24:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:24:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 29 Dec 2025 23:24:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:24:52 GMT
USER memcache
# Mon, 29 Dec 2025 23:24:52 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 29 Dec 2025 23:24:52 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d74ee4724223b1c44d3bdff5ee6ee8c7eceabc636fe61128ec308914b5999f8`  
		Last Modified: Mon, 29 Dec 2025 23:25:06 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d74224a341d3e408a0affb0b0eb0c53f99939a1b669f25e6b34026f224a3745`  
		Last Modified: Mon, 29 Dec 2025 23:25:06 GMT  
		Size: 153.5 KB (153455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5db3b7f17de3125f5608801faf4e6a1615d96c6be2fa7f1c09e52d0cd7cd80`  
		Last Modified: Mon, 29 Dec 2025 23:25:06 GMT  
		Size: 2.3 MB (2261324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885dc482553144838528b69fa53518cc1fafb03d7eac91e773730285029e30e9`  
		Last Modified: Mon, 29 Dec 2025 23:25:06 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8afa8cb30ddae48c82fab84d30d0457bfa667059caff286dcfc57999e07a8b1`  
		Last Modified: Mon, 29 Dec 2025 23:25:06 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:62c7db64a99cd405d4330dc5c878884ef8a0e107864d7314a4cb66a8242b7dee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cfb248343584b4b08d6f7b363daf97f9506e303159317383e87ae5b82750335`

```dockerfile
```

-	Layers:
	-	`sha256:f38f799c754160125bc6daafe2fc1bd335001b11d94be74b560069268f8246e4`  
		Last Modified: Tue, 30 Dec 2025 04:35:02 GMT  
		Size: 2.0 MB (2008544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad51b10b5d6e7e377d3219a2f60c17ba2d754739a985c052724e0826650144fc`  
		Last Modified: Tue, 30 Dec 2025 04:35:03 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; 386

```console
$ docker pull memcached@sha256:0be60a562cdf0c05ebc768c0de49cf333584a650766b962f308610539a885a4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33665696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7b7c835420cd1e7ae8cd0eb0b0df1b2020c581061f1938dfa5292723e395058`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:17:02 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 29 Dec 2025 23:17:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:19:58 GMT
ENV MEMCACHED_VERSION=1.6.40
# Mon, 29 Dec 2025 23:19:58 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Mon, 29 Dec 2025 23:19:58 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Mon, 29 Dec 2025 23:19:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 29 Dec 2025 23:19:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:19:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 29 Dec 2025 23:19:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:19:58 GMT
USER memcache
# Mon, 29 Dec 2025 23:19:58 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 29 Dec 2025 23:19:58 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:796ffff142a3158a5c48a8d81b8b722c5cf4889d5e22da70bdd13a6459d6e40b`  
		Last Modified: Mon, 29 Dec 2025 22:27:31 GMT  
		Size: 31.3 MB (31293100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8fc762766a28f1d89093cb569234311423930c02de910408e80cad47e30647`  
		Last Modified: Mon, 29 Dec 2025 23:20:11 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b725b75ef28bdf7d63e19355a971dc87c6501efa1f70edbee592d52e763fee94`  
		Last Modified: Mon, 29 Dec 2025 23:20:11 GMT  
		Size: 147.5 KB (147508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9509121c0551cdeef95fef92e5598954065e802767669466cffb6c8dada5c3`  
		Last Modified: Mon, 29 Dec 2025 23:20:11 GMT  
		Size: 2.2 MB (2223574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f6e90b6aa0c5dbad71d717fad6007d2dfc7dbc186fa2c07eb8ce8416168801`  
		Last Modified: Mon, 29 Dec 2025 23:20:11 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4fa5d83d611a53674f14bb3fea7ff4465d235101cd9c5640e6c822413b3f4e`  
		Last Modified: Mon, 29 Dec 2025 23:20:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:2f28d2975c37dc6c21579400a4d8a911f45c78e460466164e094c3b114a8a739
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b72a726f712c69433343b634304351532be5cd25051c5bba2f1842cbe52c9fd`

```dockerfile
```

-	Layers:
	-	`sha256:0b522eb7b1ed969865d6941e83230cfad34490504dd209cdf0a9574b09a02415`  
		Last Modified: Tue, 30 Dec 2025 04:35:06 GMT  
		Size: 2.0 MB (2005385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9244708212b7f5f5094918a876558a69b2ba5df9e6a6187f1f97b3dd699465a`  
		Last Modified: Tue, 30 Dec 2025 04:35:08 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; ppc64le

```console
$ docker pull memcached@sha256:38a236f83eb206f786b39c53e8f756815f0bda1460157b11844faf21735208bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36162589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d41292f5c75fe5f3a464b809bde41e0ae8849ad8d7046918a548d0c6b2e250a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 21:34:54 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 17 Dec 2025 21:35:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:28 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:28 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:28 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ddd908d99c8b32da8685339ba6296773100f66e08c8bf508ab82174ba5a4f600`  
		Last Modified: Tue, 09 Dec 2025 00:06:51 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d2b42546c7b688160cfd1a0da61a24922a019b4ebead88e23aff01482ddd477`  
		Last Modified: Wed, 17 Dec 2025 21:38:49 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4efe9fd2e012174cd86a64f83d7b7facfe14ee67c9c9fa5ce994f22c24173f2c`  
		Last Modified: Wed, 17 Dec 2025 21:38:49 GMT  
		Size: 170.4 KB (170393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9752985ba696f0f8d5831ac91e19bfe336342b1c403542641c575b1dc6116e`  
		Last Modified: Wed, 17 Dec 2025 21:38:49 GMT  
		Size: 2.4 MB (2393786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d11c68ba0bc913d139eea51cb2957c1ddd713515fc06dfa5d4c398b119535a`  
		Last Modified: Wed, 17 Dec 2025 21:38:49 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9186b8b7184cef442ae3ed6a3feadcaa8f4ccc974ed5ae6c6cf8efe37e679f23`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:00d1019e9978171df76f638253f212405bf7d53251607ef5a5933d5b28d867b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:588d3d6ab54a9ea5c8baf9b013bb23c12826989ba0d09cb862431e2fa30e5189`

```dockerfile
```

-	Layers:
	-	`sha256:799ad025578a6d5d0155dc5be223bfbc25ffa3aa0548e4fb2e4bedeb0a5088d9`  
		Last Modified: Wed, 17 Dec 2025 22:35:03 GMT  
		Size: 2.0 MB (2011829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eaa03114ccb63fbbd8ca04eef46baa26c8a0508f1256aa45d851f3a49f2ed47a`  
		Last Modified: Wed, 17 Dec 2025 22:35:04 GMT  
		Size: 22.2 KB (22225 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; riscv64

```console
$ docker pull memcached@sha256:30d185f5c04056622fe346fecdf9a07a4d861871fef4028424c9b38e979d2ba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30615105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6048e6bd3b428597fcae4887d0b69fb252944cd1c8afdd85045a4e4c68837ecf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 03:48:33 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 30 Dec 2025 03:49:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 04:02:23 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 30 Dec 2025 04:02:23 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 30 Dec 2025 04:02:23 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 30 Dec 2025 04:02:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 30 Dec 2025 04:02:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Dec 2025 04:02:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 30 Dec 2025 04:02:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Dec 2025 04:02:23 GMT
USER memcache
# Tue, 30 Dec 2025 04:02:23 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 30 Dec 2025 04:02:23 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:96d8ad310358e2403b7b44cf38db606dc1ea6b58b915684d38e13f573860f64e`  
		Last Modified: Tue, 30 Dec 2025 00:53:22 GMT  
		Size: 28.3 MB (28273129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d30361332d6c36fa201043e1df585bb5cea535dfbf760f9b2ed1827c4a53ac`  
		Last Modified: Tue, 30 Dec 2025 04:03:16 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe44badb419e8d40ff093c52477fa45ed79bb9d483ed2f517359e5583617d73a`  
		Last Modified: Tue, 30 Dec 2025 04:03:17 GMT  
		Size: 133.1 KB (133088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a36426c8facdb7304fc9999aee0ca442e6e3b75be15714fa9cadff5589e57f20`  
		Last Modified: Tue, 30 Dec 2025 04:03:16 GMT  
		Size: 2.2 MB (2207375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7820ce69e6809e314e3ef1cf5cc6d3c2bafcd597d9eaf7f0f491c3ea69249db`  
		Last Modified: Tue, 30 Dec 2025 04:03:16 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc77699b8548736e5d2fa9873720c2f41ddfbc89354a6f902b7e5b5651ad0135`  
		Last Modified: Tue, 30 Dec 2025 04:03:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:7f4ca8337c70973f8b5a8eb90158eacfc3a792f5af42d7edf68da0a3a4846cd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a70852a9b9663c0d61ac529b72228ba271972017a65a149b4af634dadda75c5b`

```dockerfile
```

-	Layers:
	-	`sha256:45586a078529026200d6db8b774cf2db02f7292ac8bd6cfd4f8e68ddbe883e64`  
		Last Modified: Tue, 30 Dec 2025 04:35:15 GMT  
		Size: 2.0 MB (2002192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e23345b5880eafecc6509da78e5a9b8e6e95ce6050b2ecb71bb24c1aa03342e5`  
		Last Modified: Tue, 30 Dec 2025 04:35:15 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; s390x

```console
$ docker pull memcached@sha256:e513e62f8a86f2c8f23e06b9b73d141d7e53163ab557ec297be5f3c682a70bc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32273670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd4c0f39122c5c6e9cb01d08aebb1281a0ce18244cbc1e051742de47c5bd51f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:17:26 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 29 Dec 2025 23:17:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:20:38 GMT
ENV MEMCACHED_VERSION=1.6.40
# Mon, 29 Dec 2025 23:20:38 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Mon, 29 Dec 2025 23:20:38 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Mon, 29 Dec 2025 23:20:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 29 Dec 2025 23:20:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:20:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 29 Dec 2025 23:20:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:20:38 GMT
USER memcache
# Mon, 29 Dec 2025 23:20:38 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 29 Dec 2025 23:20:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c9a83915f7d4b9d7fbe5dceeedd49718d2702fd67d78b63a38ec344f3fbfcc41`  
		Last Modified: Mon, 29 Dec 2025 22:27:07 GMT  
		Size: 29.8 MB (29834418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1fd9e99d807cb897b4653efa7815d408df0bb7175d7fb89ab19b79b7737dc1d`  
		Last Modified: Mon, 29 Dec 2025 23:20:55 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7251a4bef45871483e5419196b0bd7ee7440a6dcc98993bd541eb9cf6ee89b06`  
		Last Modified: Mon, 29 Dec 2025 23:20:55 GMT  
		Size: 140.5 KB (140511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16461f97f95d5d1b2cb64bc91ad5a73d23e505f74a1cf95eeb9de840c9a06488`  
		Last Modified: Mon, 29 Dec 2025 23:20:55 GMT  
		Size: 2.3 MB (2297231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa6eecd4b590cab77eae19d421ebb50ce6ed90281723d604c775bcb78b5408f`  
		Last Modified: Mon, 29 Dec 2025 23:20:55 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2779e4a3a9763cc09cc4694ec9a5b304164f44aa2869a8ccbca67eeca523c305`  
		Last Modified: Mon, 29 Dec 2025 23:20:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:89b3d47f58bd28d04b77c9a4cb6634d06120bc2fa943508ae1125915480f511e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b70d80ce63a4423c1c153bdb4d489ec092debf0f20017e21d47e05ed147b71d9`

```dockerfile
```

-	Layers:
	-	`sha256:0be1a3049197ac03e690e9365edd513ffeb121d05d4b6883a58c6356f44ce72f`  
		Last Modified: Tue, 30 Dec 2025 01:35:29 GMT  
		Size: 2.0 MB (2009665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4be7a57b181c7a7314b420b859583bfaa463e17fc94b8f57edc563abf95a3257`  
		Last Modified: Tue, 30 Dec 2025 01:35:30 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:trixie`

```console
$ docker pull memcached@sha256:36c36f0c38cda62ab29af64a0eefa53e99879265ff70df8ac12597be28c482f7
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
$ docker pull memcached@sha256:61bcd214c8da24f2bacfd9152bccafef4f4c0993897c945ee3058106e084b314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32193395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5dafc7d411a870fbc52ca64194006e50e355d34f1edf56b4e1dc5b8019b0934`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:21:34 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 29 Dec 2025 23:21:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:24:22 GMT
ENV MEMCACHED_VERSION=1.6.40
# Mon, 29 Dec 2025 23:24:22 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Mon, 29 Dec 2025 23:24:22 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Mon, 29 Dec 2025 23:24:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 29 Dec 2025 23:24:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:24:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 29 Dec 2025 23:24:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:24:22 GMT
USER memcache
# Mon, 29 Dec 2025 23:24:22 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 29 Dec 2025 23:24:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d08d8001380dd7c5a9be2e59244310ccfa7e84f3b896b354059d46d1928401`  
		Last Modified: Mon, 29 Dec 2025 23:24:36 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8420bae5d2af8b5b5e66d7e5ba882f5e2034cc64eacfb1a0b4b32a259a541b16`  
		Last Modified: Mon, 29 Dec 2025 23:24:35 GMT  
		Size: 136.7 KB (136694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc2daf1b2287468ea06570c5bedff8bc84ab6833050a7e0686f5f7d7a2679e1`  
		Last Modified: Mon, 29 Dec 2025 23:24:35 GMT  
		Size: 2.3 MB (2278657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a54c348dd92d8a79d150c1fe56008dba798b633f010e1e57c0a18f62b2752d90`  
		Last Modified: Mon, 29 Dec 2025 23:24:35 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e147936d0f858c8f726dea003b7220347e43918cab2714f81c66c1553cc160cd`  
		Last Modified: Mon, 29 Dec 2025 23:24:35 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:e6d0cef74a4a91255f97601317c1cd45953291e56aebea597b1f5fedb87772df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a114559b11eef9830f21c5cfd0b3dff0712acd507604d89ab89f16d229d637c`

```dockerfile
```

-	Layers:
	-	`sha256:31d77d05cfee83189fed485cbb6de83d56b3fc5c8a37eafd4e5ab2a8646bcee5`  
		Last Modified: Tue, 30 Dec 2025 04:34:52 GMT  
		Size: 2.0 MB (2008228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:daae5d64f19c0b653f152172ab207032a103d7a2c198208a2472a4565869c64e`  
		Last Modified: Tue, 30 Dec 2025 04:34:53 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; arm variant v5

```console
$ docker pull memcached@sha256:19778ab8ffe04b579956362255d1b4be4646df675a0c0db5662d882e7e062834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30300227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85e834ef35584236d3b04d1823e406899096de386d548c5f0bfd896cfba41631`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:17:23 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 29 Dec 2025 23:17:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:39:32 GMT
ENV MEMCACHED_VERSION=1.6.40
# Mon, 29 Dec 2025 23:39:32 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Mon, 29 Dec 2025 23:39:32 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Mon, 29 Dec 2025 23:39:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 29 Dec 2025 23:39:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:39:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 29 Dec 2025 23:39:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:39:32 GMT
USER memcache
# Mon, 29 Dec 2025 23:39:32 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 29 Dec 2025 23:39:32 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b99a8d8dab982a1a4ea341e66b178b14c0f373c2cd90ac46a67308a4f43c82ae`  
		Last Modified: Mon, 29 Dec 2025 22:27:09 GMT  
		Size: 27.9 MB (27944146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0be68f37541245f1acaee607441dfc983a00e90d78d5e0941265d0b67b1cc9a`  
		Last Modified: Mon, 29 Dec 2025 23:39:44 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10905a7698a57312678edda9f8fc0748b6288699f5fed1f8e7e7e909240d441`  
		Last Modified: Mon, 29 Dec 2025 23:39:44 GMT  
		Size: 144.1 KB (144149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea062eb6d6681b78497a81a8d5ca89088b56f5a5d629e3124df93b9ca0e4f16`  
		Last Modified: Mon, 29 Dec 2025 23:39:44 GMT  
		Size: 2.2 MB (2210419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d59770b8679e935091911e6294f61a53df8f59b5cc8aae431217cc391864a0`  
		Last Modified: Mon, 29 Dec 2025 23:39:44 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945c1d27fa6617071d97eddd3d962ac571276f7f757f99edc1a93ebbe6eb5a9c`  
		Last Modified: Mon, 29 Dec 2025 23:39:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:27e3afeed14c4cac078a10db01ef22eef58848fc65d93501050f872bc3cf64d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:939368d93857b65d5e6bbdc97a5f4d158eeca9efc9fb02875eae93350ea663fb`

```dockerfile
```

-	Layers:
	-	`sha256:3559f8384ca294c984900b7325032abfe47459734f215e79264a22aa23802031`  
		Last Modified: Tue, 30 Dec 2025 01:35:12 GMT  
		Size: 2.0 MB (2011231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b310c8a994e22e59ca814cd06500201d5b78c4bbfe3baa8785ae093760d4a4fb`  
		Last Modified: Tue, 30 Dec 2025 01:35:13 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; arm variant v7

```console
$ docker pull memcached@sha256:34f932820fcffc223d050d31ceeef236f4bc4a1a8e776006560fe2ef14348a2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28510848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0a0c32503881f91ec515af1fd074032b8070eac0faa4afca5e1f2f60609b237`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:17:22 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 29 Dec 2025 23:17:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:20:31 GMT
ENV MEMCACHED_VERSION=1.6.40
# Mon, 29 Dec 2025 23:20:31 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Mon, 29 Dec 2025 23:20:31 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Mon, 29 Dec 2025 23:20:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 29 Dec 2025 23:20:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:20:31 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 29 Dec 2025 23:20:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:20:31 GMT
USER memcache
# Mon, 29 Dec 2025 23:20:31 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 29 Dec 2025 23:20:31 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6d3e0fea3cb8eb29b9c06956265b47cd00f7ebfb48e35e818f686d52c21353f5`  
		Last Modified: Mon, 29 Dec 2025 22:28:07 GMT  
		Size: 26.2 MB (26210001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f916949d5244227fca363e62638c31c65e0f6a941ceaa0fb79c37d962e9b95bb`  
		Last Modified: Mon, 29 Dec 2025 23:20:45 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f24598f250037f41edf0d0093ed08f2b3b3937f91d7708c687330e0feca3fdcf`  
		Last Modified: Mon, 29 Dec 2025 23:20:45 GMT  
		Size: 135.4 KB (135362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f260cb2adbfa9ad1d74da541da12d2146b1a06685021b42e924c843481237ee2`  
		Last Modified: Mon, 29 Dec 2025 23:20:46 GMT  
		Size: 2.2 MB (2163975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0f315cda938284ce51afa280bd8e89b891448b2da00c28c66c638c2d4a4cc6`  
		Last Modified: Mon, 29 Dec 2025 23:20:45 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c38a3204b12ac8ee46611fe38ab1a706ee2c310f8a4e0439862ee702d7b5481c`  
		Last Modified: Mon, 29 Dec 2025 23:20:45 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:4c6e114c037bf19003547b10ffc5b077c88be25cd990cd30d1f26945409bf69c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5de9929189cfe8912f0ebace1f73497b21396b8561e62dab4d98cefa02760f10`

```dockerfile
```

-	Layers:
	-	`sha256:1bc6b02786844de8506e80bae2bf850ea8bf7875761b0a8ff17497e18e297086`  
		Last Modified: Tue, 30 Dec 2025 04:34:58 GMT  
		Size: 2.0 MB (2009688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48de2da0a0a924a9a938d6ea9a12b2eb727da5a33bad6987e74e57dcfdc66f51`  
		Last Modified: Tue, 30 Dec 2025 04:34:59 GMT  
		Size: 22.3 KB (22303 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:517aefb9e9ff071c2aa387ca68e1b63663f210c5bc838b8d928cb657795329fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32554923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20bd9e6ac4a3626ae8b8108e846570938ea003859e516dcd2134d2d628fd2c79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:21:52 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 29 Dec 2025 23:21:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:24:52 GMT
ENV MEMCACHED_VERSION=1.6.40
# Mon, 29 Dec 2025 23:24:52 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Mon, 29 Dec 2025 23:24:52 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Mon, 29 Dec 2025 23:24:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 29 Dec 2025 23:24:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:24:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 29 Dec 2025 23:24:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:24:52 GMT
USER memcache
# Mon, 29 Dec 2025 23:24:52 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 29 Dec 2025 23:24:52 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d74ee4724223b1c44d3bdff5ee6ee8c7eceabc636fe61128ec308914b5999f8`  
		Last Modified: Mon, 29 Dec 2025 23:25:06 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d74224a341d3e408a0affb0b0eb0c53f99939a1b669f25e6b34026f224a3745`  
		Last Modified: Mon, 29 Dec 2025 23:25:06 GMT  
		Size: 153.5 KB (153455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5db3b7f17de3125f5608801faf4e6a1615d96c6be2fa7f1c09e52d0cd7cd80`  
		Last Modified: Mon, 29 Dec 2025 23:25:06 GMT  
		Size: 2.3 MB (2261324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885dc482553144838528b69fa53518cc1fafb03d7eac91e773730285029e30e9`  
		Last Modified: Mon, 29 Dec 2025 23:25:06 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8afa8cb30ddae48c82fab84d30d0457bfa667059caff286dcfc57999e07a8b1`  
		Last Modified: Mon, 29 Dec 2025 23:25:06 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:62c7db64a99cd405d4330dc5c878884ef8a0e107864d7314a4cb66a8242b7dee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cfb248343584b4b08d6f7b363daf97f9506e303159317383e87ae5b82750335`

```dockerfile
```

-	Layers:
	-	`sha256:f38f799c754160125bc6daafe2fc1bd335001b11d94be74b560069268f8246e4`  
		Last Modified: Tue, 30 Dec 2025 04:35:02 GMT  
		Size: 2.0 MB (2008544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad51b10b5d6e7e377d3219a2f60c17ba2d754739a985c052724e0826650144fc`  
		Last Modified: Tue, 30 Dec 2025 04:35:03 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; 386

```console
$ docker pull memcached@sha256:0be60a562cdf0c05ebc768c0de49cf333584a650766b962f308610539a885a4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33665696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7b7c835420cd1e7ae8cd0eb0b0df1b2020c581061f1938dfa5292723e395058`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:17:02 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 29 Dec 2025 23:17:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:19:58 GMT
ENV MEMCACHED_VERSION=1.6.40
# Mon, 29 Dec 2025 23:19:58 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Mon, 29 Dec 2025 23:19:58 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Mon, 29 Dec 2025 23:19:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 29 Dec 2025 23:19:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:19:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 29 Dec 2025 23:19:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:19:58 GMT
USER memcache
# Mon, 29 Dec 2025 23:19:58 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 29 Dec 2025 23:19:58 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:796ffff142a3158a5c48a8d81b8b722c5cf4889d5e22da70bdd13a6459d6e40b`  
		Last Modified: Mon, 29 Dec 2025 22:27:31 GMT  
		Size: 31.3 MB (31293100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8fc762766a28f1d89093cb569234311423930c02de910408e80cad47e30647`  
		Last Modified: Mon, 29 Dec 2025 23:20:11 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b725b75ef28bdf7d63e19355a971dc87c6501efa1f70edbee592d52e763fee94`  
		Last Modified: Mon, 29 Dec 2025 23:20:11 GMT  
		Size: 147.5 KB (147508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9509121c0551cdeef95fef92e5598954065e802767669466cffb6c8dada5c3`  
		Last Modified: Mon, 29 Dec 2025 23:20:11 GMT  
		Size: 2.2 MB (2223574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f6e90b6aa0c5dbad71d717fad6007d2dfc7dbc186fa2c07eb8ce8416168801`  
		Last Modified: Mon, 29 Dec 2025 23:20:11 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4fa5d83d611a53674f14bb3fea7ff4465d235101cd9c5640e6c822413b3f4e`  
		Last Modified: Mon, 29 Dec 2025 23:20:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:2f28d2975c37dc6c21579400a4d8a911f45c78e460466164e094c3b114a8a739
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b72a726f712c69433343b634304351532be5cd25051c5bba2f1842cbe52c9fd`

```dockerfile
```

-	Layers:
	-	`sha256:0b522eb7b1ed969865d6941e83230cfad34490504dd209cdf0a9574b09a02415`  
		Last Modified: Tue, 30 Dec 2025 04:35:06 GMT  
		Size: 2.0 MB (2005385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9244708212b7f5f5094918a876558a69b2ba5df9e6a6187f1f97b3dd699465a`  
		Last Modified: Tue, 30 Dec 2025 04:35:08 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; ppc64le

```console
$ docker pull memcached@sha256:38a236f83eb206f786b39c53e8f756815f0bda1460157b11844faf21735208bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36162589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d41292f5c75fe5f3a464b809bde41e0ae8849ad8d7046918a548d0c6b2e250a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 21:34:54 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 17 Dec 2025 21:35:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 17 Dec 2025 21:38:27 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 17 Dec 2025 21:38:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 17 Dec 2025 21:38:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:38:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 17 Dec 2025 21:38:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:38:28 GMT
USER memcache
# Wed, 17 Dec 2025 21:38:28 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 17 Dec 2025 21:38:28 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ddd908d99c8b32da8685339ba6296773100f66e08c8bf508ab82174ba5a4f600`  
		Last Modified: Tue, 09 Dec 2025 00:06:51 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d2b42546c7b688160cfd1a0da61a24922a019b4ebead88e23aff01482ddd477`  
		Last Modified: Wed, 17 Dec 2025 21:38:49 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4efe9fd2e012174cd86a64f83d7b7facfe14ee67c9c9fa5ce994f22c24173f2c`  
		Last Modified: Wed, 17 Dec 2025 21:38:49 GMT  
		Size: 170.4 KB (170393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9752985ba696f0f8d5831ac91e19bfe336342b1c403542641c575b1dc6116e`  
		Last Modified: Wed, 17 Dec 2025 21:38:49 GMT  
		Size: 2.4 MB (2393786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d11c68ba0bc913d139eea51cb2957c1ddd713515fc06dfa5d4c398b119535a`  
		Last Modified: Wed, 17 Dec 2025 21:38:49 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9186b8b7184cef442ae3ed6a3feadcaa8f4ccc974ed5ae6c6cf8efe37e679f23`  
		Last Modified: Wed, 17 Dec 2025 21:38:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:00d1019e9978171df76f638253f212405bf7d53251607ef5a5933d5b28d867b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:588d3d6ab54a9ea5c8baf9b013bb23c12826989ba0d09cb862431e2fa30e5189`

```dockerfile
```

-	Layers:
	-	`sha256:799ad025578a6d5d0155dc5be223bfbc25ffa3aa0548e4fb2e4bedeb0a5088d9`  
		Last Modified: Wed, 17 Dec 2025 22:35:03 GMT  
		Size: 2.0 MB (2011829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eaa03114ccb63fbbd8ca04eef46baa26c8a0508f1256aa45d851f3a49f2ed47a`  
		Last Modified: Wed, 17 Dec 2025 22:35:04 GMT  
		Size: 22.2 KB (22225 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; riscv64

```console
$ docker pull memcached@sha256:30d185f5c04056622fe346fecdf9a07a4d861871fef4028424c9b38e979d2ba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30615105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6048e6bd3b428597fcae4887d0b69fb252944cd1c8afdd85045a4e4c68837ecf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 03:48:33 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 30 Dec 2025 03:49:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 04:02:23 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 30 Dec 2025 04:02:23 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 30 Dec 2025 04:02:23 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 30 Dec 2025 04:02:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 30 Dec 2025 04:02:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Dec 2025 04:02:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 30 Dec 2025 04:02:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Dec 2025 04:02:23 GMT
USER memcache
# Tue, 30 Dec 2025 04:02:23 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 30 Dec 2025 04:02:23 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:96d8ad310358e2403b7b44cf38db606dc1ea6b58b915684d38e13f573860f64e`  
		Last Modified: Tue, 30 Dec 2025 00:53:22 GMT  
		Size: 28.3 MB (28273129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d30361332d6c36fa201043e1df585bb5cea535dfbf760f9b2ed1827c4a53ac`  
		Last Modified: Tue, 30 Dec 2025 04:03:16 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe44badb419e8d40ff093c52477fa45ed79bb9d483ed2f517359e5583617d73a`  
		Last Modified: Tue, 30 Dec 2025 04:03:17 GMT  
		Size: 133.1 KB (133088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a36426c8facdb7304fc9999aee0ca442e6e3b75be15714fa9cadff5589e57f20`  
		Last Modified: Tue, 30 Dec 2025 04:03:16 GMT  
		Size: 2.2 MB (2207375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7820ce69e6809e314e3ef1cf5cc6d3c2bafcd597d9eaf7f0f491c3ea69249db`  
		Last Modified: Tue, 30 Dec 2025 04:03:16 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc77699b8548736e5d2fa9873720c2f41ddfbc89354a6f902b7e5b5651ad0135`  
		Last Modified: Tue, 30 Dec 2025 04:03:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:7f4ca8337c70973f8b5a8eb90158eacfc3a792f5af42d7edf68da0a3a4846cd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a70852a9b9663c0d61ac529b72228ba271972017a65a149b4af634dadda75c5b`

```dockerfile
```

-	Layers:
	-	`sha256:45586a078529026200d6db8b774cf2db02f7292ac8bd6cfd4f8e68ddbe883e64`  
		Last Modified: Tue, 30 Dec 2025 04:35:15 GMT  
		Size: 2.0 MB (2002192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e23345b5880eafecc6509da78e5a9b8e6e95ce6050b2ecb71bb24c1aa03342e5`  
		Last Modified: Tue, 30 Dec 2025 04:35:15 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; s390x

```console
$ docker pull memcached@sha256:e513e62f8a86f2c8f23e06b9b73d141d7e53163ab557ec297be5f3c682a70bc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32273670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd4c0f39122c5c6e9cb01d08aebb1281a0ce18244cbc1e051742de47c5bd51f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:17:26 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 29 Dec 2025 23:17:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:20:38 GMT
ENV MEMCACHED_VERSION=1.6.40
# Mon, 29 Dec 2025 23:20:38 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Mon, 29 Dec 2025 23:20:38 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Mon, 29 Dec 2025 23:20:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 29 Dec 2025 23:20:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:20:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 29 Dec 2025 23:20:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:20:38 GMT
USER memcache
# Mon, 29 Dec 2025 23:20:38 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 29 Dec 2025 23:20:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c9a83915f7d4b9d7fbe5dceeedd49718d2702fd67d78b63a38ec344f3fbfcc41`  
		Last Modified: Mon, 29 Dec 2025 22:27:07 GMT  
		Size: 29.8 MB (29834418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1fd9e99d807cb897b4653efa7815d408df0bb7175d7fb89ab19b79b7737dc1d`  
		Last Modified: Mon, 29 Dec 2025 23:20:55 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7251a4bef45871483e5419196b0bd7ee7440a6dcc98993bd541eb9cf6ee89b06`  
		Last Modified: Mon, 29 Dec 2025 23:20:55 GMT  
		Size: 140.5 KB (140511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16461f97f95d5d1b2cb64bc91ad5a73d23e505f74a1cf95eeb9de840c9a06488`  
		Last Modified: Mon, 29 Dec 2025 23:20:55 GMT  
		Size: 2.3 MB (2297231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa6eecd4b590cab77eae19d421ebb50ce6ed90281723d604c775bcb78b5408f`  
		Last Modified: Mon, 29 Dec 2025 23:20:55 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2779e4a3a9763cc09cc4694ec9a5b304164f44aa2869a8ccbca67eeca523c305`  
		Last Modified: Mon, 29 Dec 2025 23:20:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:89b3d47f58bd28d04b77c9a4cb6634d06120bc2fa943508ae1125915480f511e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b70d80ce63a4423c1c153bdb4d489ec092debf0f20017e21d47e05ed147b71d9`

```dockerfile
```

-	Layers:
	-	`sha256:0be1a3049197ac03e690e9365edd513ffeb121d05d4b6883a58c6356f44ce72f`  
		Last Modified: Tue, 30 Dec 2025 01:35:29 GMT  
		Size: 2.0 MB (2009665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4be7a57b181c7a7314b420b859583bfaa463e17fc94b8f57edc563abf95a3257`  
		Last Modified: Tue, 30 Dec 2025 01:35:30 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json
