## `memcached:trixie`

```console
$ docker pull memcached@sha256:e3f16220c1ca3ca45e91686e4ba8dfb010be87a3fb713b75add9cb13a162e3b8
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
$ docker pull memcached@sha256:33e9867b97e512512f6d565ecaed597c0c4140822e27baf02e3ac018caba2137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32195518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcf903955e9c2bab6ac20e3d7a7a265cb2d46321c9ae84e627efe398a66453b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:22:29 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 03 Feb 2026 02:22:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:25:21 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 03 Feb 2026 02:25:21 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 03 Feb 2026 02:25:21 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 03 Feb 2026 02:25:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 03 Feb 2026 02:25:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:25:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:25:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:25:21 GMT
USER memcache
# Tue, 03 Feb 2026 02:25:21 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 03 Feb 2026 02:25:21 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5deab379793a5b0aea7bd03292c1e2d3a8b2a9c569f4967dae45e0956a44b496`  
		Last Modified: Tue, 03 Feb 2026 02:25:27 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea05fbaa7819118e45d578b174916c006003e0171b173776b12ac8369b0ebc3`  
		Last Modified: Tue, 03 Feb 2026 02:25:27 GMT  
		Size: 136.7 KB (136676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8ee46647fb26b6925aaae659f35f0313d3ce40bcb96c575c8f239d197d3c3e`  
		Last Modified: Tue, 03 Feb 2026 02:25:27 GMT  
		Size: 2.3 MB (2278727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7866f34cb273caa1307acb66aff2faa029e5b72a83d93268fdc4bb2752a3577d`  
		Last Modified: Tue, 03 Feb 2026 02:25:27 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc0ff1059d57ce15a80b481f7cf6d024cce3094b12eb878b28f5a786919ab90`  
		Last Modified: Tue, 03 Feb 2026 02:25:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:6d8c0e698759774ca44c4d8541428fa2c8900a5ce3b76601e9485ab4058f6a5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0997f6f3df830b761d3bb0240d04e9726ca807b9c92db5603daed0ea48f7aa3`

```dockerfile
```

-	Layers:
	-	`sha256:39ee95e4ebe1c8150ff7a132197f3a0d16c08bc69aead388451de12c1772da4f`  
		Last Modified: Tue, 03 Feb 2026 02:25:27 GMT  
		Size: 2.0 MB (2008290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52c81cd09c6ce8c4a6b8c29256390be3f6a32dc22306ed9fd54a9d0552e088d1`  
		Last Modified: Tue, 03 Feb 2026 02:25:27 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; arm variant v5

```console
$ docker pull memcached@sha256:59a356fd5b303fe760e48d8a36d6e843e69a6f45eefb5597c4ad04383911d17f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30303654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e71df154843ed6ac5c9f3d28cfd4a344adfb711e611453d8dec2113143ab7525`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:17:26 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 03 Feb 2026 02:17:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:20:47 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 03 Feb 2026 02:20:47 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 03 Feb 2026 02:20:47 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 03 Feb 2026 02:20:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 03 Feb 2026 02:20:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:20:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:20:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:20:47 GMT
USER memcache
# Tue, 03 Feb 2026 02:20:47 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 03 Feb 2026 02:20:47 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2a2986ba48ae233640829460f6772db2ffbc330d97d2b29a533694dfdc7dc893`  
		Last Modified: Tue, 03 Feb 2026 01:14:07 GMT  
		Size: 27.9 MB (27947555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5782e3b508f0c2dccb65f0ae3d2b521eebe4c0a5aa797ea131b7197ff6951557`  
		Last Modified: Tue, 03 Feb 2026 02:20:53 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a59ffaabad25bc5e204e9da202149f964d8538fefc95b45a13481d047d5286`  
		Last Modified: Tue, 03 Feb 2026 02:20:53 GMT  
		Size: 144.2 KB (144175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d0adfe279829d5e4d346b5eb21ea032f1e8154b07b4c4b1b9ff96f5fa187446`  
		Last Modified: Tue, 03 Feb 2026 02:20:53 GMT  
		Size: 2.2 MB (2210409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f5b8dc51746ff9e8ab01be6158f9ebcd875d3a9e5bd42d741934ee8fb864e0`  
		Last Modified: Tue, 03 Feb 2026 02:20:53 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f5b9a0a377792403f61f417ea02ef493018541f9a358ec84a0c0d9dc4d51ba7`  
		Last Modified: Tue, 03 Feb 2026 02:20:54 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:7bdf4b4cb4dfee328e8bd005615315a7e592d6e54e63ce39c09638004e20f9bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a680bbeb69803c3ad250ac927c771e0d0ce084216fa607c88e6ae51436f14fc3`

```dockerfile
```

-	Layers:
	-	`sha256:2aa600b70de43d982a724bdafe5cdd8a8103f332acb214b059c76103c9a46e61`  
		Last Modified: Tue, 03 Feb 2026 02:20:53 GMT  
		Size: 2.0 MB (2011293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ca9bd32f4d197b402c22e889f132efc5619c955b8909436549aa58555584fd4`  
		Last Modified: Tue, 03 Feb 2026 02:20:53 GMT  
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
$ docker pull memcached@sha256:ee2fb336d7acaef21163567a663314ecd1c410ecc6508d64d336c69db55304bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36165948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8b3625cad529638a9b2b485f5662193e76bbc42e5a1d08025499280c2042802`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:29:15 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 03 Feb 2026 02:29:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:32:53 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 03 Feb 2026 02:32:53 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 03 Feb 2026 02:32:53 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 03 Feb 2026 02:32:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 03 Feb 2026 02:32:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:32:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:32:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:32:54 GMT
USER memcache
# Tue, 03 Feb 2026 02:32:54 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 03 Feb 2026 02:32:54 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1aee42d34fb7e3a2db6f83f2a84e17846ac990ed8ecf693a309ae759efdbdaa3`  
		Last Modified: Tue, 03 Feb 2026 01:16:35 GMT  
		Size: 33.6 MB (33600184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78bfd196c2cb241381eaf59c973f4ba760ce5fd0be08840969dc7bcdcba104ce`  
		Last Modified: Tue, 03 Feb 2026 02:33:10 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:575ddd8f4328625544be88305da8bc120013e49e7af566558c961790e81016f1`  
		Last Modified: Tue, 03 Feb 2026 02:33:10 GMT  
		Size: 170.4 KB (170393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f85bec2d6e837c8a7580e1fbd44ee42e6e626e511d6676c4b5c07d5a2aede9`  
		Last Modified: Tue, 03 Feb 2026 02:33:10 GMT  
		Size: 2.4 MB (2393856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2004226d3d1c2d3dc7d9cb0c9a6c274d79c49edc574b6714d51a70d9aa0497`  
		Last Modified: Tue, 03 Feb 2026 02:33:10 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a990bdde6127e94d3a07b066c7c3a34b2c56a370a70937c937febaa2231f9a43`  
		Last Modified: Tue, 03 Feb 2026 02:33:11 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:ffdc337c2936969db145c7fe8c740167d0fed758a6ab0148c7c8543cb9db4ad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dc9cb9d597a56c2a3fa86fa03b9634b328941dd4ab616db3fdff9b1957006c0`

```dockerfile
```

-	Layers:
	-	`sha256:d702f963f06c7239446afa5db2b020a96571127e3341962549334bf3b9bf5553`  
		Last Modified: Tue, 03 Feb 2026 02:33:10 GMT  
		Size: 2.0 MB (2011891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cec3972b44c818f1ee30da62b36d1b7ad239cf2e4c49e36b1aa1c1d74dd142b0`  
		Last Modified: Tue, 03 Feb 2026 02:33:10 GMT  
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
$ docker pull memcached@sha256:ca57f3d0b419870b3de49f7d39bb1f73cabe3ff04c8bd3d6ca13a3e46da0a568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32277571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1031ffa68db32cd43971c829646e02cc645e8ca5d9ef830924c1da0593e91953`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:19:22 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 03 Feb 2026 02:19:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:41:13 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 03 Feb 2026 02:41:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 03 Feb 2026 02:41:13 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 03 Feb 2026 02:41:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 03 Feb 2026 02:41:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:41:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:41:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:41:13 GMT
USER memcache
# Tue, 03 Feb 2026 02:41:13 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 03 Feb 2026 02:41:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:809310277795fa02ff585c83bc37c8fb5e06066ee7e053bab5d08bf186beeae9`  
		Last Modified: Tue, 03 Feb 2026 01:14:11 GMT  
		Size: 29.8 MB (29838149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf54d4929696aef38fc786423b59f0aa9c5de349490cf2ec77f6c89b1be9311`  
		Last Modified: Tue, 03 Feb 2026 02:41:23 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ddb9429330b1b35bfbf2759e131b6b7a4e4f068167808e08ea295f9b64ee387`  
		Last Modified: Tue, 03 Feb 2026 02:41:23 GMT  
		Size: 140.5 KB (140503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5c794fa041bb467c46a0df94a44fde0c2031b5046f88a58a585d83eed5b45f`  
		Last Modified: Tue, 03 Feb 2026 02:41:23 GMT  
		Size: 2.3 MB (2297404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:476dcab1e4b0500ce67e01aa889fbb818ca116b07755f10e3e7012fce342e8b6`  
		Last Modified: Tue, 03 Feb 2026 02:41:23 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b787d0acf48cb25f0dbed5379a387628293b68421a49e1989528ca1a8d49ab5c`  
		Last Modified: Tue, 03 Feb 2026 02:41:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:15e096d0247c842865cd21a21920e1ba01fc2aa119f05368ae0b5b922574a109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7309e5fffb5499d19bb8267f9f77b4047ec3eed92d61f431ea5caf10e672893e`

```dockerfile
```

-	Layers:
	-	`sha256:1b3468ecb19c89422a3d2f2310b254ce0bdd70798e297baaf0b0c00048782cd7`  
		Last Modified: Tue, 03 Feb 2026 02:41:23 GMT  
		Size: 2.0 MB (2009727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef2594449779f1777370bfb67b979fe63265a3b911c797c36e5d7706e6e3c955`  
		Last Modified: Tue, 03 Feb 2026 02:41:23 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json
