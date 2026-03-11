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
$ docker pull memcached@sha256:d99136ed4c1cf2e3fceb498763f2b7fedec7c486a0fe8a57be19f2a0519ce1fa
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
$ docker pull memcached@sha256:c08df224e6ccee2c893ac468902a8b68d8221910014da88f892d483b145f2e80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32197142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc0c289673d3b6f117607d5014b52d276fa02ad622404df04deac38f7a3b2b75`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Sat, 07 Mar 2026 00:34:28 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Mar 2026 00:34:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Mar 2026 00:37:16 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:37:16 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:37:16 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:37:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:37:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:37:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:37:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:37:16 GMT
USER memcache
# Sat, 07 Mar 2026 00:37:16 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:37:16 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65546826072afb14e8706d66b636911c885382731f6d325cba605469fdb363e7`  
		Last Modified: Sat, 07 Mar 2026 00:37:23 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f84d4f33fb93823aaef11588c633186a7b4c7e9c0fea6cf0c2c2e912be6b9f`  
		Last Modified: Sat, 07 Mar 2026 00:37:23 GMT  
		Size: 136.7 KB (136684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f30a00378f01ca7716c334349799965f472572c2377432ae0948fb3481a330`  
		Last Modified: Sat, 07 Mar 2026 00:37:23 GMT  
		Size: 2.3 MB (2280310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd736c12c1d448b0585c460fd3f417da3a21193665ef2aefd67c221cbd97df0b`  
		Last Modified: Sat, 07 Mar 2026 00:37:23 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f072b1e28c7bdff147ef49013b08dfe871999faec678a4219890f645e2d14b`  
		Last Modified: Sat, 07 Mar 2026 00:37:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:b0cd4839975a3f144a6d44260b40e6cebfaad48ae0dabae69c8a84a1912f55ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d69fb1b8b08633539bde084818362e1b13aae93417c6fc42c6c674e4039d2ab4`

```dockerfile
```

-	Layers:
	-	`sha256:0bc9fc51640e8d0b171e44a65462e97d0e54980aca3e0ea45f57320911a0f07c`  
		Last Modified: Sat, 07 Mar 2026 00:37:23 GMT  
		Size: 2.0 MB (2008290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2632163ed214b82be06d84daacb113b153e4ec7def67cd764cb771fb9700aeaf`  
		Last Modified: Sat, 07 Mar 2026 00:37:23 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm variant v5

```console
$ docker pull memcached@sha256:514cbf94b5380f36ac3c88108bf78a84ae83c3ed26e638ebe2e2f5bb88bd25ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30304774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc4d63874316ce18eaa26acb02c5e3dc129e31ea8c480a3a966621c75552572c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1771804800'
# Sat, 07 Mar 2026 00:34:25 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Mar 2026 00:34:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Mar 2026 00:37:50 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:37:50 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:37:50 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:37:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:37:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:37:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:37:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:37:50 GMT
USER memcache
# Sat, 07 Mar 2026 00:37:50 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:37:50 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:280a075cc1d2a97445b9f4430aa9774bfc38fc4217b7fc9d6a7b04e7e431cb65`  
		Last Modified: Tue, 24 Feb 2026 18:42:44 GMT  
		Size: 27.9 MB (27947608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fee55b7ab1f18dde561acdb3246640b49ed746f0a6f679b8b4be2fe96c38edc`  
		Last Modified: Sat, 07 Mar 2026 00:37:56 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e90ce24e8e18d6e22b1819e0c183af55656f28a490d2a5f5db1bb199759ae2`  
		Last Modified: Sat, 07 Mar 2026 00:37:56 GMT  
		Size: 144.2 KB (144173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e14eaa4ef07ee7a2796a97655630e5b528d0f2f8120ba62ac860fcf148e2b813`  
		Last Modified: Sat, 07 Mar 2026 00:37:56 GMT  
		Size: 2.2 MB (2211477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0271cbc419600dba0091ae986cd78ada6340afbfa697b93993e1f63555a831`  
		Last Modified: Sat, 07 Mar 2026 00:37:56 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ecc8023e8fc75e87c4b1fc32230e35e765d671345bd42f98dfe13b7118bc13`  
		Last Modified: Sat, 07 Mar 2026 00:37:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:3b41b0fb30672979494c2bcc11e11de72d662cbeef4e097e83bf3637c45aba4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b344e75a26fbd848f3d4bda6dfbc82971e7c99f16f8b8d3c2f4e0046b3e36cf`

```dockerfile
```

-	Layers:
	-	`sha256:a8abf2c9952faed7ee6a8484d94c195f2f516d28b4aa99d61fde6a938373ef14`  
		Last Modified: Sat, 07 Mar 2026 00:37:56 GMT  
		Size: 2.0 MB (2011293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4baff3ba9a329e3fdeaee0149357b33f76e181413fc6e5b4d1b9502670d8aab3`  
		Last Modified: Sat, 07 Mar 2026 00:37:56 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm variant v7

```console
$ docker pull memcached@sha256:5e39383d269092b745c7426583a0849917817a2861226858ff17c34f227cadc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28515640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4d89f2522b7f402debcdfe4ae5ef33ccc13694e72756aabd8c894fd1a657663`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Sat, 07 Mar 2026 00:34:26 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Mar 2026 00:34:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Mar 2026 00:37:36 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:37:36 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:37:36 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:37:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:37:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:37:37 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:37:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:37:37 GMT
USER memcache
# Sat, 07 Mar 2026 00:37:37 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:37:37 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b5f623d77fff35b334b15c7b208113b4b778a70ce39168e1270421140984e6`  
		Last Modified: Sat, 07 Mar 2026 00:37:43 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d378422d428b98928a2c392598ff24dddba86412c764099339db2c9b84dab7`  
		Last Modified: Sat, 07 Mar 2026 00:37:43 GMT  
		Size: 135.4 KB (135371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ebe7571649e14f8ae60c2aa9c7464f120d47deb28852880adc72f5958fb268`  
		Last Modified: Sat, 07 Mar 2026 00:37:43 GMT  
		Size: 2.2 MB (2165006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab8a97091ab7e05c0561d93041f6833b293ec83a81c5cd316d914c7cd4797f5`  
		Last Modified: Sat, 07 Mar 2026 00:37:43 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06917ca5c3af99a9a619b7c0077abf8521b0777d4c07464889139b6030aaa445`  
		Last Modified: Sat, 07 Mar 2026 00:37:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:17c7cd3931d1614e411d593e6027c70049d32dd6b78b4523f5e29ff13b7b1f21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b42f736130d7735ab6bde638b9206c6be06a848c316aa0776562b9d2b05634b5`

```dockerfile
```

-	Layers:
	-	`sha256:1700f9d32fecaf2a6fff6e275b9eac8036467ba4e592635351cf279712b2017b`  
		Last Modified: Sat, 07 Mar 2026 00:37:43 GMT  
		Size: 2.0 MB (2009750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef3320ccea4ba2f43dfdeb26388b30f9251a45c8b87522656d05eb856e022fa0`  
		Last Modified: Sat, 07 Mar 2026 00:37:43 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:03ff213526efc235b60a048b3efa0c67c6d697a62bdc207561fb8ee00f254f89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32557234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4742c51756a2139de24009e1c754635923a703d67706387249d261e4dc62712`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Sat, 07 Mar 2026 00:34:23 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Mar 2026 00:34:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Mar 2026 00:37:25 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:37:25 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:37:25 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:37:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:37:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:37:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:37:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:37:25 GMT
USER memcache
# Sat, 07 Mar 2026 00:37:25 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:37:25 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:461d33f62f9a4e4fbc09492d8ce59e548e8c794e3122411c5f7a8370f2bbedba`  
		Last Modified: Sat, 07 Mar 2026 00:37:31 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e642309aa5a12065d7f985c382b7658fa51b45c2a111039cdb9b7240299809e7`  
		Last Modified: Sat, 07 Mar 2026 00:37:31 GMT  
		Size: 153.5 KB (153496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c81e14adafcb230598de8ae3eaf03443a9ae10bd04e616ae4ab64a2f379a48d`  
		Last Modified: Sat, 07 Mar 2026 00:37:31 GMT  
		Size: 2.3 MB (2262125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62e12af1edbdc302c3fd82e9561c5eac5def3110b53dc9d527b277d70a0c5b0`  
		Last Modified: Sat, 07 Mar 2026 00:37:31 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eee7fdafd6f634c0431e5a06be62ff9a726cb1fa8367483d6b026fa3164c7f0`  
		Last Modified: Sat, 07 Mar 2026 00:37:32 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:f791266a2bf814187fed117fa0abd604df8d26056d2e2791b51eb537a958de3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e7b8f74c70d2427388103547caa9c90ef2b4ec4ee11ce197e642593e10f6979`

```dockerfile
```

-	Layers:
	-	`sha256:88d9544d6eb9588edcaeabdc26922a9afb53b2222e8f9972e5b4b52199893738`  
		Last Modified: Sat, 07 Mar 2026 00:37:31 GMT  
		Size: 2.0 MB (2008606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b245266f3e6e113152f086489529a68f1c8c229363d9b678823c16250c48131`  
		Last Modified: Sat, 07 Mar 2026 00:37:31 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; 386

```console
$ docker pull memcached@sha256:1219e49a37eb8fa43f5cabcda7eb69df920734c5d615f2fc63e4fba52a06dfd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33667722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d141db22d43d8c6503a206b3413976c2fd0b84654a45bb46a3da3f39594ee93e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1771804800'
# Sat, 07 Mar 2026 00:34:41 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Mar 2026 00:34:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Mar 2026 00:37:41 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:37:41 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:37:41 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:37:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:37:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:37:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:37:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:37:41 GMT
USER memcache
# Sat, 07 Mar 2026 00:37:41 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:37:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f4e0b944ee1e7e50bdfbfa77bda370b6eccee7d698a7adca78c38f5ca0767ca5`  
		Last Modified: Tue, 24 Feb 2026 18:43:18 GMT  
		Size: 31.3 MB (31293918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d38eff546890db9ae0646486b61a548d8067820adc96ceb6eb4f5d7c2206bb8`  
		Last Modified: Sat, 07 Mar 2026 00:37:47 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c454125cf8ccd03f95714478c13c1d671ba0807b980ee5e6df450d611f61e156`  
		Last Modified: Sat, 07 Mar 2026 00:37:47 GMT  
		Size: 147.5 KB (147517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42b7d17f494cc1acab1da36a724a41a46ecf955d058123b89b170ea63bafda97`  
		Last Modified: Sat, 07 Mar 2026 00:37:47 GMT  
		Size: 2.2 MB (2224772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56fcaee4e2b815384392953fdf84278be4b9a4b116e3a5ad6436f7b13a7c6d9`  
		Last Modified: Sat, 07 Mar 2026 00:37:47 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6adacd7f3e38f46b44efa4ff006b35719382afa26b95b7a9b0c62ef7e7a01bfc`  
		Last Modified: Sat, 07 Mar 2026 00:37:48 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:9f65574f3294736b3dc217e4b07a4045282c517d258eaa96a32035e09cda6fa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb96fc147195e16ed2b6e99c3582cd8c6a67516fb0387c563d09fbf85f6a4dc0`

```dockerfile
```

-	Layers:
	-	`sha256:cdc74dec8f482313433fa0011e8531a8e816610bf31af8b63d2203318e8a59f9`  
		Last Modified: Sat, 07 Mar 2026 00:37:47 GMT  
		Size: 2.0 MB (2005447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bbcbbf7d1935fe3e711cd689ff38f789c3f7334bff2fd2518c106c4bf5d805f`  
		Last Modified: Sat, 07 Mar 2026 00:37:47 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; ppc64le

```console
$ docker pull memcached@sha256:ffac94778c7c882a7f2cbaae5af33e755639de207d07834e052412c2b22a24b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36754462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5640d71fb49b8eaef07631709a9f4924bd191fcfe9b44b7df2d525e247075b64`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Sat, 07 Mar 2026 00:33:31 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Mar 2026 00:33:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Mar 2026 00:56:42 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:56:42 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:56:42 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:56:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:56:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:56:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:56:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:56:44 GMT
USER memcache
# Sat, 07 Mar 2026 00:56:44 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:56:44 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab70996aa4a561e7f3e1f1e1b14df7912a1456b20b317937391cfa826c93f2ea`  
		Last Modified: Sat, 07 Mar 2026 00:57:10 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1ba00921effa53d91205ba3e5e3280c719885f49b5e9e0f8e2a387cf316d89`  
		Last Modified: Sat, 07 Mar 2026 00:57:10 GMT  
		Size: 170.4 KB (170386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd00738358190677470eca91b6732f6fcc475639b7f07f1943af6f5d268ae47`  
		Last Modified: Sat, 07 Mar 2026 00:57:10 GMT  
		Size: 3.0 MB (2982343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f7dc97a8f5d8c677e24bd2f8014c3e315619d726d409033dc3ce4f6d7d7569d`  
		Last Modified: Sat, 07 Mar 2026 00:57:10 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f2b48241128f09e1c613b0fb34d37f79c77417d033b7a00041f8cd08d6241f`  
		Last Modified: Sat, 07 Mar 2026 00:57:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:da557c745e92be8dd35823b9c24b79e47c55ff727768980abe9b659a14672408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e89b8bba62432d49e11baad935eddf449853276e5bb492953ae6bb995bf81ef`

```dockerfile
```

-	Layers:
	-	`sha256:7bf94ead3bca06412117cdc5395bde9d799ffc799dd28be779209634f64bfc0b`  
		Last Modified: Sat, 07 Mar 2026 00:57:10 GMT  
		Size: 2.0 MB (2011891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ec351466954789ecb039e735ecf9fd0235d5d4cfcf8bd6bcf2cf68049016c1c`  
		Last Modified: Sat, 07 Mar 2026 00:57:10 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; riscv64

```console
$ docker pull memcached@sha256:ccac0e143b4efd5bd15fb67df5ad87f5b743cc3db826cbb27d1874cbb3b6d549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30619564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f9320af1aa6fbbae22f81ef28d68694abc001739c71a195b4b1cd490b3b9107`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 23:50:36 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 09 Mar 2026 23:51:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Mar 2026 00:09:03 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 10 Mar 2026 00:09:03 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 10 Mar 2026 00:09:03 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 10 Mar 2026 00:09:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 10 Mar 2026 00:09:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 10 Mar 2026 00:09:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 10 Mar 2026 00:09:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Mar 2026 00:09:03 GMT
USER memcache
# Tue, 10 Mar 2026 00:09:03 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 10 Mar 2026 00:09:03 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e1366b1f74881f04901f31cfdecf9f3f5d4794ebf89911083a239bf462bf21`  
		Last Modified: Tue, 10 Mar 2026 00:09:56 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918782f8ab4ae7fe2ab9f1fc0aa7ad4e48d83dc362a4dcac336048ded3de9b6e`  
		Last Modified: Tue, 10 Mar 2026 00:09:56 GMT  
		Size: 133.1 KB (133079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963fbe1d00657987e81bdc270499ad5aacf8f91b100915c30ddf9fc57cd67346`  
		Last Modified: Tue, 10 Mar 2026 00:09:56 GMT  
		Size: 2.2 MB (2208551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729657786193241c665df2cbaeb72b5d157865abb3bbd8b9460e88d08fb65fea`  
		Last Modified: Tue, 10 Mar 2026 00:09:56 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8246f12fbc1ee94790a418b9655df55d80968171273b5994aaffa40c04fa2f3c`  
		Last Modified: Tue, 10 Mar 2026 00:09:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:de9f0d80a354763898649af4229a6f696fb51689e3b577af2e1d918d365777e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d72c30b80e1c2deaee38b267b52cab1a28e245b2a3608fcf459f2232dad3faa7`

```dockerfile
```

-	Layers:
	-	`sha256:03d9f11a7e8cf93ffe1f13ecfd86632a66af5a6efc142ae7a4ecac0c19418b2d`  
		Last Modified: Tue, 10 Mar 2026 00:09:56 GMT  
		Size: 2.0 MB (2002254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:452e3f764b5054c447aa8e63046155a20784d6f10159282ce633afdb79bf9279`  
		Last Modified: Tue, 10 Mar 2026 00:09:56 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; s390x

```console
$ docker pull memcached@sha256:8e1f3fb07bf1702ad27a7e2a6b2364e61d7b5165c113d0202db31adaa90d91df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32278340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1088ed36ed575f78d3e06fdd24f1ccdcc908d6e579970b2cae128c29f8d6e7a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Sat, 07 Mar 2026 00:33:32 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Mar 2026 00:33:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Mar 2026 00:36:51 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:36:51 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:36:51 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:36:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:36:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:36:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:36:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:36:51 GMT
USER memcache
# Sat, 07 Mar 2026 00:36:51 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:36:51 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986cc162f1a9b2f1b4c673da47497d87b8a542990f29c7823ee4d64cd160ea34`  
		Last Modified: Sat, 07 Mar 2026 00:37:00 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e3b516d24d039487b70f5d718d6f2b0c5473b5da4e6b82815239c7730587d6`  
		Last Modified: Sat, 07 Mar 2026 00:37:00 GMT  
		Size: 140.5 KB (140520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb611bdb547903f4763e52741be4c28e6ed0f172ebffc4ddae4e56a1a4d3ebc2`  
		Last Modified: Sat, 07 Mar 2026 00:37:00 GMT  
		Size: 2.3 MB (2298126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b32c7b8a27f2284141ba22bde8036a295b3e0d397cde405054e47e550cced01`  
		Last Modified: Sat, 07 Mar 2026 00:37:00 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3240387a49966ed4c1475913af7c7648c5499d01045e56e16637a760300918a`  
		Last Modified: Sat, 07 Mar 2026 00:37:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:b725149e071a1d02723f7674a5f7c477144350f79f2243558bce2360da7bf73b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:628ead940c50f3d4776c150c412d2270c2238893cfd1a57f8c17647ec35223e2`

```dockerfile
```

-	Layers:
	-	`sha256:b118af94ed9d10ab8f0c0221725860a15ff82dce98bd35abb240f411b745e0f7`  
		Last Modified: Sat, 07 Mar 2026 00:37:00 GMT  
		Size: 2.0 MB (2009727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:737fa51b5113fe89d161d6b7d0d81d66c28e666617dc1fb7c410b093ecf35625`  
		Last Modified: Sat, 07 Mar 2026 00:37:00 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine`

```console
$ docker pull memcached@sha256:1c6a2d48c5f561226f1dc54ed37132f83b4cde94b5e3f3e2d88386d028b86a27
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
$ docker pull memcached@sha256:84dd21b0c8ebc30032a8aaa7270c7e6c11da52efd7bf3c7593530168946d3bd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5959699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaf5f46bdf2c26a9dda97cd7dd2b6a05c5d8135b2f9cbacf33ff8e8365f5e1eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Sat, 07 Mar 2026 00:36:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Mar 2026 00:36:14 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Mar 2026 00:38:52 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:38:52 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:38:52 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:38:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:38:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:38:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:38:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:38:52 GMT
USER memcache
# Sat, 07 Mar 2026 00:38:52 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:38:52 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d055707374a501222192f988c0ff35fcfdc5a017dd49a48e1dd38106c605f400`  
		Last Modified: Sat, 07 Mar 2026 00:38:57 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5abb10c57422a10d35029047d7b017a29437bc0081f375524cbfb3db3c9eaf9`  
		Last Modified: Sat, 07 Mar 2026 00:38:57 GMT  
		Size: 106.1 KB (106057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4fd18d57089d5254541b428a6a2429569ff07d571c824af865b666901af275e`  
		Last Modified: Sat, 07 Mar 2026 00:38:57 GMT  
		Size: 2.0 MB (1990468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885d9eb83efad8e7a74f165d5e00bd1e547b62348f4084f8748eb5123cfd5ef2`  
		Last Modified: Sat, 07 Mar 2026 00:38:57 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32954341fb1b6227e3bb596d1a3f58beb03c348455e63c0e6a810197d1922e9`  
		Last Modified: Sat, 07 Mar 2026 00:38:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:e0615e85e00302f3ab01f14593cf39cf7e4ac01f448e6904dd61247bf63b3ff0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3b92ada03392c40180327b1e82f1b29a80b1164d4b65115558c1efc811142ad`

```dockerfile
```

-	Layers:
	-	`sha256:cc3e65e74aa6c619611c020b3d498d3c756e6168a9b26434ca30c3099cfa3261`  
		Last Modified: Sat, 07 Mar 2026 00:38:57 GMT  
		Size: 94.9 KB (94873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:327a47bce4975ea9e581754831550ac249839dc3708d4841f78ebc6cbd78d014`  
		Last Modified: Sat, 07 Mar 2026 00:38:57 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:6cde7ea7574023751e83c90e1e8f1f7aef03c1d5b0fbe20a17d981d57edb99dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:376e43ecede029f4d02a7634c75d3107a5797f724660eb9b02b0eb12c3e49748`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Sat, 07 Mar 2026 00:34:25 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Mar 2026 00:34:26 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Mar 2026 00:37:29 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:37:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:37:29 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:37:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:37:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:37:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:37:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:37:29 GMT
USER memcache
# Sat, 07 Mar 2026 00:37:29 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:37:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18dad4d028ff2b78314498b57b872634656cb70add272a07cde87477543ea34b`  
		Last Modified: Sat, 07 Mar 2026 00:37:33 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5343ac0baa24b86f7ffac4e0a3296276d4a7aa05b74617720244260e34dc5aba`  
		Last Modified: Sat, 07 Mar 2026 00:37:33 GMT  
		Size: 102.7 KB (102655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f65584616382b3a0c0b70214fd4046110bedf9cfbb2c2f89c2301372f8aa27`  
		Last Modified: Sat, 07 Mar 2026 00:37:33 GMT  
		Size: 1.9 MB (1940281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a378f9c04f9d21fc788013f2928b3637ad3724011b85ecb4d8fe5a61ca9bb2`  
		Last Modified: Sat, 07 Mar 2026 00:37:33 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9600d067846989777b70f754cdd61c2012197736201713e9b5ff3703b147be02`  
		Last Modified: Sat, 07 Mar 2026 00:37:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:1d36396e4f4bb90ed2d326fbc737d8ab225cf619e64f08c3ff0beaff000177ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e204629c18255bb70ea677237338842d7ed3a140e1ecbbc4b8d5727cafa1668e`

```dockerfile
```

-	Layers:
	-	`sha256:1ea1c312fb87cc4d7c73a561d98b13a1f13504625a2de3953101370977fc6745`  
		Last Modified: Sat, 07 Mar 2026 00:37:33 GMT  
		Size: 20.5 KB (20466 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:91fe29148d686af2a0fdc23ba01a1b272f4c6365fc45bc37d00d4687a0c41b1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5273746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a56ac817dd40669cbf75609948d0f6fc05e648f6453d8f9deba7740682f741f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Sat, 07 Mar 2026 00:37:41 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Mar 2026 00:37:42 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Mar 2026 00:40:39 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:40:39 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:40:39 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:40:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:40:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:40:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:40:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:40:39 GMT
USER memcache
# Sat, 07 Mar 2026 00:40:39 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:40:39 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a51b7877e94969180dbb0be219881bc9230f055057f9e3f4b65f1db0708689a`  
		Last Modified: Sat, 07 Mar 2026 00:40:44 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c32abf408db65abfcd3224db5db2abaa977bd3ce59942c389c73320a4051cc`  
		Last Modified: Sat, 07 Mar 2026 00:40:44 GMT  
		Size: 92.4 KB (92374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ddc29b1020998fb5a3b242cc4e45954bc53540a31017ab6a020f9dff807bd22`  
		Last Modified: Sat, 07 Mar 2026 00:40:44 GMT  
		Size: 1.9 MB (1898298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae00440f5f6fd5951552907706f8df3661315090758ede99bb2933aa3384040b`  
		Last Modified: Sat, 07 Mar 2026 00:40:44 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb70de481e3407c522658dfa65d701fde07648ab9b8c732379d8a92f44092a81`  
		Last Modified: Sat, 07 Mar 2026 00:40:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:073366e4d50888ea6d43868ab35c2a063ea12dc243105f0c614c4feaa55d0eda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c47e8e147c04b6fae9be2f9c70644395f05ac10516981d5f48aac87100f9aabf`

```dockerfile
```

-	Layers:
	-	`sha256:f128294dbb16b2300fe484115b6bd24498974e73ac8835f70a3dd5df2f3211cd`  
		Last Modified: Sat, 07 Mar 2026 00:40:44 GMT  
		Size: 94.3 KB (94291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad6c6671c716b1f4cb8882be9d7cee792a3b5a0500ba4330e4c34c83d3401a1c`  
		Last Modified: Sat, 07 Mar 2026 00:40:44 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:eeb1c0de2b6b33a7a724454aaf9fd945503a062302d133c059f1b829db991b61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6287490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0de2d8f866d91b49adb4cfa80ffd26e168ac627328864d7ceae76dfd0bc4d7a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Sat, 07 Mar 2026 00:36:34 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Mar 2026 00:36:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Mar 2026 00:39:22 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:39:22 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:39:22 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:39:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:39:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:39:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:39:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:39:22 GMT
USER memcache
# Sat, 07 Mar 2026 00:39:22 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:39:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d65cacaa69d1c76240e558dab714b69561f9bb333c2c1c147f9be7d6b29c36`  
		Last Modified: Sat, 07 Mar 2026 00:39:27 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca80346986e335b6e96f14599a1ab3629964fa8702f4570e2d199da8b04498e`  
		Last Modified: Sat, 07 Mar 2026 00:39:27 GMT  
		Size: 121.9 KB (121860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bcaaaf5541ab3a5d055204886aadf36871e66f535b6c1978b4b4c58a4dc2367`  
		Last Modified: Sat, 07 Mar 2026 00:39:27 GMT  
		Size: 2.0 MB (1967188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6167d1b1458d5cedc7774a2a1e9e621f5b32de851a6b19d82ea2275ec9f1bc5`  
		Last Modified: Sat, 07 Mar 2026 00:39:27 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2040432b455fd0270cf480396dc9c1570b8710e21539cc0110e13fe10105062`  
		Last Modified: Sat, 07 Mar 2026 00:39:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:3d8284de1f87be934ca3ad16b60f3a624262a50260f7f8db4cc80575af22e7c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9a54dfb1a405917a8fe0eaf03a1588913998eac5cacc5141cad5d053c6ba838`

```dockerfile
```

-	Layers:
	-	`sha256:8eefe1140db7c68e1990a3744cd3126838a63605758bc6825cb1c090277cf806`  
		Last Modified: Sat, 07 Mar 2026 00:39:27 GMT  
		Size: 94.3 KB (94327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92f28d8e0dd01f916858b48749b2827fadaadb7ca45a0a8a872ac9d74043589d`  
		Last Modified: Sat, 07 Mar 2026 00:39:27 GMT  
		Size: 20.7 KB (20728 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; 386

```console
$ docker pull memcached@sha256:006134e843d0ad5a3c64e903cc20d00c9f3e78a542fa3d6ba1e3ecec5b0ba3c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5742709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06188a4fb3481bcf32a3e44fca9d58ab763a52c65e02c95fbef5e98f4b78ee86`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Sat, 07 Mar 2026 00:37:00 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Mar 2026 00:37:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Mar 2026 00:39:49 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:39:49 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:39:49 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:39:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:39:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:39:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:39:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:39:50 GMT
USER memcache
# Sat, 07 Mar 2026 00:39:50 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:39:50 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ba4a2e327b273e788cfdef17b5c31ac5fefd6010584aa1c11b0d0104a041d6`  
		Last Modified: Sat, 07 Mar 2026 00:39:54 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ba4e8e1182330d5f76532f2f48fe38af386558e3e7fa4d94ce3dbf055be5ab`  
		Last Modified: Sat, 07 Mar 2026 00:39:54 GMT  
		Size: 110.7 KB (110732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01c1fe355d65277d08c7962b0be21d39386b4121b36381bbcb9a60d29449a5c`  
		Last Modified: Sat, 07 Mar 2026 00:39:54 GMT  
		Size: 1.9 MB (1943630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e102587e979593069cf080e59b8471ecf62f9c40abad1e62014f1742341827d0`  
		Last Modified: Sat, 07 Mar 2026 00:39:54 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46411b86935a4104c9cbb43c595a9cbf0e0330c814ca33c36935c5a9cb7f37d`  
		Last Modified: Sat, 07 Mar 2026 00:39:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:d0cb60f8d8c989514001fd52bf793673fa8f281758af2b58f8359d1d41973b11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58f3853067ae595d4075c459fe7b8361d199af21eaa1f93413e882c2e0bc9042`

```dockerfile
```

-	Layers:
	-	`sha256:2cd10df8bfae391e9a94e270083baf145ca51970a41e64ab71cd781740d00c73`  
		Last Modified: Sat, 07 Mar 2026 00:39:54 GMT  
		Size: 94.8 KB (94828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1d4f0d3116c96944777e5e4b1130eaff94973a8664033f37d3c60ceb36ed173`  
		Last Modified: Sat, 07 Mar 2026 00:39:54 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:35c354ed5e627574c294e54f0232ed89e8eacd7ed7e2670634db2396b8f2a39c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6034990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3da727092e7c56a19e8b1a382da13658524813ce0d2bca55dee5f4067987b77a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Sat, 07 Mar 2026 00:33:31 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Mar 2026 00:33:34 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Mar 2026 00:36:15 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:36:15 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:36:15 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:36:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:36:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:36:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:36:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:36:16 GMT
USER memcache
# Sat, 07 Mar 2026 00:36:16 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:36:16 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364a7d7b961599919f81b228a22514e1935e6774971d671f38dbad14ef71cbfd`  
		Last Modified: Sat, 07 Mar 2026 00:36:29 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d77d50c27f0ae298d21083636544fb7f795b9708dc480f081e1e936f1246e7`  
		Last Modified: Sat, 07 Mar 2026 00:36:29 GMT  
		Size: 126.3 KB (126266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d559c6185e0bba610ac4ee55bed1b0d85afdad6f054f17906fadb6311cc44007`  
		Last Modified: Sat, 07 Mar 2026 00:36:29 GMT  
		Size: 2.1 MB (2077727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce553e1c7553a28f652dbbd9f3d79596edea9eecf47883032057409cd1d977f`  
		Last Modified: Sat, 07 Mar 2026 00:36:29 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf30d9d84b197d47332200b954fc9fcedf3653c9a44fe6b72a5cf721ec170f1`  
		Last Modified: Sat, 07 Mar 2026 00:36:30 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7c60879107d9d8ce6f5e597f4c108df4a413d312eaf52e4c9303b96e80e84fbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eee93b7e24e493f45076a5a793e8b01aad30e3643bcb7583bc1fa26a1c4ff826`

```dockerfile
```

-	Layers:
	-	`sha256:b4505eef72239eda1b1c608b3226cd19dc02c372be606494a473db623050489a`  
		Last Modified: Sat, 07 Mar 2026 00:36:29 GMT  
		Size: 94.3 KB (94280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43cc72cbc203c87b12cbef8914fb2835a461df6bb0445da26d96b5a14e610184`  
		Last Modified: Sat, 07 Mar 2026 00:36:29 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:874942dd4e337f828a5480fa7e7e03b28951302101475540a14d752215e0b99e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5771014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61e6da61960009cb5e1d5f173422857994cb30b45c987fc35062485420c05ddf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 11 Mar 2026 21:21:50 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 11 Mar 2026 21:21:54 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 11 Mar 2026 21:35:15 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 11 Mar 2026 21:35:15 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 11 Mar 2026 21:35:15 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 11 Mar 2026 21:35:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 11 Mar 2026 21:35:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 11 Mar 2026 21:35:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 11 Mar 2026 21:35:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2026 21:35:16 GMT
USER memcache
# Wed, 11 Mar 2026 21:35:16 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 11 Mar 2026 21:35:16 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63b25af376cdb2cb3ddbdf009ec368c61af0677da2ff36f56052ba87ef9d03e`  
		Last Modified: Wed, 11 Mar 2026 21:35:39 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efcf2b36003649471638502666fa028dd48ae26bf7a732d6d7fe38a8432a7016`  
		Last Modified: Wed, 11 Mar 2026 21:35:39 GMT  
		Size: 108.9 KB (108902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddaf732ffb5731ec8232eec8940c917de4727564501c45fce52a7e2ebd641224`  
		Last Modified: Wed, 11 Mar 2026 21:35:40 GMT  
		Size: 2.1 MB (2075471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91cabf0fbda848cc214b782cee7c5c7224ddb7674e75de41599a3bbe85d6a689`  
		Last Modified: Wed, 11 Mar 2026 21:35:39 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:306ecccaa7e256f58e1e772b44b962766fdf35f118efb1596b4c9ae2431987ab`  
		Last Modified: Wed, 11 Mar 2026 21:35:40 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:5e6d73b60a6ccb5dda56fc4d483b45097e7ef55ce412da110e15c6c478c8d882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebcfe45486057ddd0b85095c8ca2fd1a8656b95e8ecf579e4de8717551ada915`

```dockerfile
```

-	Layers:
	-	`sha256:7176cf6ddf61d50975dee6f26ce9fdcb0b77085375b0dde58bb44b8337adca94`  
		Last Modified: Wed, 11 Mar 2026 21:35:39 GMT  
		Size: 94.3 KB (94276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5799ace3d1f3a380e60d9e9676ffbd335daf84ded3af9d5e1dd8ce83eee2060`  
		Last Modified: Wed, 11 Mar 2026 21:35:39 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:9c94884aa3d27f0c0ed5df500b79a6f3c2685bba5c632e3b871c0a262314d935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5858795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cd8a0886a7efaab4d69edd3b15f2a68384bcfdb1ff1a454930ba3a6a6ba29fc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Sat, 07 Mar 2026 00:33:34 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Mar 2026 00:33:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Mar 2026 00:36:49 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:36:49 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:36:49 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:36:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:36:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:36:49 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:36:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:36:49 GMT
USER memcache
# Sat, 07 Mar 2026 00:36:49 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:36:49 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f0d8799f878cf05935221d46a9b462122587e33ba748e54c983e03bbcb7ad2`  
		Last Modified: Sat, 07 Mar 2026 00:36:57 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef440db2f09493c5c9eae06dd0e59dafbd4761a74731e3ffa8ac968dcca712ca`  
		Last Modified: Sat, 07 Mar 2026 00:36:57 GMT  
		Size: 114.3 KB (114309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:134d34534319282a3e54d23ff3c63c0362a6c2ba38fb854b6a94a202d67347c2`  
		Last Modified: Sat, 07 Mar 2026 00:36:57 GMT  
		Size: 2.0 MB (2017802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:655653db981f7dce0174439408f99d0c480cb5082436a0682568bdaab190cd39`  
		Last Modified: Sat, 07 Mar 2026 00:36:57 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92dd0a7cdddba4f0415d5e0b6aa52c11369fa65b7c8c4ae965c949d55e7d52dd`  
		Last Modified: Sat, 07 Mar 2026 00:36:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:b9dd2a68695665b98af82b5110aa7af831b2d15654c26ffd200cc198ac79fb69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29c28af5a544343faaa1ff91b74bb776f4c5013c23bc2f45a2bbadb0fa1acc12`

```dockerfile
```

-	Layers:
	-	`sha256:47a88819c43763550a569259221f913c63dfd51ac45adc283170d20d81240959`  
		Last Modified: Sat, 07 Mar 2026 00:36:57 GMT  
		Size: 94.2 KB (94222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a9409046e85d857b00aa1f263c8c811160eeaa0c58b29abf61985c657289659`  
		Last Modified: Sat, 07 Mar 2026 00:36:57 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine3.23`

```console
$ docker pull memcached@sha256:1c6a2d48c5f561226f1dc54ed37132f83b4cde94b5e3f3e2d88386d028b86a27
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
$ docker pull memcached@sha256:84dd21b0c8ebc30032a8aaa7270c7e6c11da52efd7bf3c7593530168946d3bd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5959699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaf5f46bdf2c26a9dda97cd7dd2b6a05c5d8135b2f9cbacf33ff8e8365f5e1eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Sat, 07 Mar 2026 00:36:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Mar 2026 00:36:14 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Mar 2026 00:38:52 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:38:52 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:38:52 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:38:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:38:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:38:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:38:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:38:52 GMT
USER memcache
# Sat, 07 Mar 2026 00:38:52 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:38:52 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d055707374a501222192f988c0ff35fcfdc5a017dd49a48e1dd38106c605f400`  
		Last Modified: Sat, 07 Mar 2026 00:38:57 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5abb10c57422a10d35029047d7b017a29437bc0081f375524cbfb3db3c9eaf9`  
		Last Modified: Sat, 07 Mar 2026 00:38:57 GMT  
		Size: 106.1 KB (106057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4fd18d57089d5254541b428a6a2429569ff07d571c824af865b666901af275e`  
		Last Modified: Sat, 07 Mar 2026 00:38:57 GMT  
		Size: 2.0 MB (1990468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885d9eb83efad8e7a74f165d5e00bd1e547b62348f4084f8748eb5123cfd5ef2`  
		Last Modified: Sat, 07 Mar 2026 00:38:57 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32954341fb1b6227e3bb596d1a3f58beb03c348455e63c0e6a810197d1922e9`  
		Last Modified: Sat, 07 Mar 2026 00:38:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:e0615e85e00302f3ab01f14593cf39cf7e4ac01f448e6904dd61247bf63b3ff0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3b92ada03392c40180327b1e82f1b29a80b1164d4b65115558c1efc811142ad`

```dockerfile
```

-	Layers:
	-	`sha256:cc3e65e74aa6c619611c020b3d498d3c756e6168a9b26434ca30c3099cfa3261`  
		Last Modified: Sat, 07 Mar 2026 00:38:57 GMT  
		Size: 94.9 KB (94873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:327a47bce4975ea9e581754831550ac249839dc3708d4841f78ebc6cbd78d014`  
		Last Modified: Sat, 07 Mar 2026 00:38:57 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; arm variant v6

```console
$ docker pull memcached@sha256:6cde7ea7574023751e83c90e1e8f1f7aef03c1d5b0fbe20a17d981d57edb99dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:376e43ecede029f4d02a7634c75d3107a5797f724660eb9b02b0eb12c3e49748`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Sat, 07 Mar 2026 00:34:25 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Mar 2026 00:34:26 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Mar 2026 00:37:29 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:37:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:37:29 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:37:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:37:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:37:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:37:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:37:29 GMT
USER memcache
# Sat, 07 Mar 2026 00:37:29 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:37:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18dad4d028ff2b78314498b57b872634656cb70add272a07cde87477543ea34b`  
		Last Modified: Sat, 07 Mar 2026 00:37:33 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5343ac0baa24b86f7ffac4e0a3296276d4a7aa05b74617720244260e34dc5aba`  
		Last Modified: Sat, 07 Mar 2026 00:37:33 GMT  
		Size: 102.7 KB (102655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f65584616382b3a0c0b70214fd4046110bedf9cfbb2c2f89c2301372f8aa27`  
		Last Modified: Sat, 07 Mar 2026 00:37:33 GMT  
		Size: 1.9 MB (1940281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a378f9c04f9d21fc788013f2928b3637ad3724011b85ecb4d8fe5a61ca9bb2`  
		Last Modified: Sat, 07 Mar 2026 00:37:33 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9600d067846989777b70f754cdd61c2012197736201713e9b5ff3703b147be02`  
		Last Modified: Sat, 07 Mar 2026 00:37:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:1d36396e4f4bb90ed2d326fbc737d8ab225cf619e64f08c3ff0beaff000177ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e204629c18255bb70ea677237338842d7ed3a140e1ecbbc4b8d5727cafa1668e`

```dockerfile
```

-	Layers:
	-	`sha256:1ea1c312fb87cc4d7c73a561d98b13a1f13504625a2de3953101370977fc6745`  
		Last Modified: Sat, 07 Mar 2026 00:37:33 GMT  
		Size: 20.5 KB (20466 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; arm variant v7

```console
$ docker pull memcached@sha256:91fe29148d686af2a0fdc23ba01a1b272f4c6365fc45bc37d00d4687a0c41b1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5273746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a56ac817dd40669cbf75609948d0f6fc05e648f6453d8f9deba7740682f741f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Sat, 07 Mar 2026 00:37:41 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Mar 2026 00:37:42 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Mar 2026 00:40:39 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:40:39 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:40:39 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:40:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:40:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:40:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:40:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:40:39 GMT
USER memcache
# Sat, 07 Mar 2026 00:40:39 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:40:39 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a51b7877e94969180dbb0be219881bc9230f055057f9e3f4b65f1db0708689a`  
		Last Modified: Sat, 07 Mar 2026 00:40:44 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c32abf408db65abfcd3224db5db2abaa977bd3ce59942c389c73320a4051cc`  
		Last Modified: Sat, 07 Mar 2026 00:40:44 GMT  
		Size: 92.4 KB (92374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ddc29b1020998fb5a3b242cc4e45954bc53540a31017ab6a020f9dff807bd22`  
		Last Modified: Sat, 07 Mar 2026 00:40:44 GMT  
		Size: 1.9 MB (1898298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae00440f5f6fd5951552907706f8df3661315090758ede99bb2933aa3384040b`  
		Last Modified: Sat, 07 Mar 2026 00:40:44 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb70de481e3407c522658dfa65d701fde07648ab9b8c732379d8a92f44092a81`  
		Last Modified: Sat, 07 Mar 2026 00:40:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:073366e4d50888ea6d43868ab35c2a063ea12dc243105f0c614c4feaa55d0eda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c47e8e147c04b6fae9be2f9c70644395f05ac10516981d5f48aac87100f9aabf`

```dockerfile
```

-	Layers:
	-	`sha256:f128294dbb16b2300fe484115b6bd24498974e73ac8835f70a3dd5df2f3211cd`  
		Last Modified: Sat, 07 Mar 2026 00:40:44 GMT  
		Size: 94.3 KB (94291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad6c6671c716b1f4cb8882be9d7cee792a3b5a0500ba4330e4c34c83d3401a1c`  
		Last Modified: Sat, 07 Mar 2026 00:40:44 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:eeb1c0de2b6b33a7a724454aaf9fd945503a062302d133c059f1b829db991b61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6287490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0de2d8f866d91b49adb4cfa80ffd26e168ac627328864d7ceae76dfd0bc4d7a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Sat, 07 Mar 2026 00:36:34 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Mar 2026 00:36:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Mar 2026 00:39:22 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:39:22 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:39:22 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:39:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:39:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:39:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:39:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:39:22 GMT
USER memcache
# Sat, 07 Mar 2026 00:39:22 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:39:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d65cacaa69d1c76240e558dab714b69561f9bb333c2c1c147f9be7d6b29c36`  
		Last Modified: Sat, 07 Mar 2026 00:39:27 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca80346986e335b6e96f14599a1ab3629964fa8702f4570e2d199da8b04498e`  
		Last Modified: Sat, 07 Mar 2026 00:39:27 GMT  
		Size: 121.9 KB (121860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bcaaaf5541ab3a5d055204886aadf36871e66f535b6c1978b4b4c58a4dc2367`  
		Last Modified: Sat, 07 Mar 2026 00:39:27 GMT  
		Size: 2.0 MB (1967188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6167d1b1458d5cedc7774a2a1e9e621f5b32de851a6b19d82ea2275ec9f1bc5`  
		Last Modified: Sat, 07 Mar 2026 00:39:27 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2040432b455fd0270cf480396dc9c1570b8710e21539cc0110e13fe10105062`  
		Last Modified: Sat, 07 Mar 2026 00:39:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:3d8284de1f87be934ca3ad16b60f3a624262a50260f7f8db4cc80575af22e7c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9a54dfb1a405917a8fe0eaf03a1588913998eac5cacc5141cad5d053c6ba838`

```dockerfile
```

-	Layers:
	-	`sha256:8eefe1140db7c68e1990a3744cd3126838a63605758bc6825cb1c090277cf806`  
		Last Modified: Sat, 07 Mar 2026 00:39:27 GMT  
		Size: 94.3 KB (94327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92f28d8e0dd01f916858b48749b2827fadaadb7ca45a0a8a872ac9d74043589d`  
		Last Modified: Sat, 07 Mar 2026 00:39:27 GMT  
		Size: 20.7 KB (20728 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; 386

```console
$ docker pull memcached@sha256:006134e843d0ad5a3c64e903cc20d00c9f3e78a542fa3d6ba1e3ecec5b0ba3c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5742709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06188a4fb3481bcf32a3e44fca9d58ab763a52c65e02c95fbef5e98f4b78ee86`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Sat, 07 Mar 2026 00:37:00 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Mar 2026 00:37:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Mar 2026 00:39:49 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:39:49 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:39:49 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:39:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:39:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:39:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:39:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:39:50 GMT
USER memcache
# Sat, 07 Mar 2026 00:39:50 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:39:50 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ba4a2e327b273e788cfdef17b5c31ac5fefd6010584aa1c11b0d0104a041d6`  
		Last Modified: Sat, 07 Mar 2026 00:39:54 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ba4e8e1182330d5f76532f2f48fe38af386558e3e7fa4d94ce3dbf055be5ab`  
		Last Modified: Sat, 07 Mar 2026 00:39:54 GMT  
		Size: 110.7 KB (110732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01c1fe355d65277d08c7962b0be21d39386b4121b36381bbcb9a60d29449a5c`  
		Last Modified: Sat, 07 Mar 2026 00:39:54 GMT  
		Size: 1.9 MB (1943630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e102587e979593069cf080e59b8471ecf62f9c40abad1e62014f1742341827d0`  
		Last Modified: Sat, 07 Mar 2026 00:39:54 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46411b86935a4104c9cbb43c595a9cbf0e0330c814ca33c36935c5a9cb7f37d`  
		Last Modified: Sat, 07 Mar 2026 00:39:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:d0cb60f8d8c989514001fd52bf793673fa8f281758af2b58f8359d1d41973b11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58f3853067ae595d4075c459fe7b8361d199af21eaa1f93413e882c2e0bc9042`

```dockerfile
```

-	Layers:
	-	`sha256:2cd10df8bfae391e9a94e270083baf145ca51970a41e64ab71cd781740d00c73`  
		Last Modified: Sat, 07 Mar 2026 00:39:54 GMT  
		Size: 94.8 KB (94828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1d4f0d3116c96944777e5e4b1130eaff94973a8664033f37d3c60ceb36ed173`  
		Last Modified: Sat, 07 Mar 2026 00:39:54 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; ppc64le

```console
$ docker pull memcached@sha256:35c354ed5e627574c294e54f0232ed89e8eacd7ed7e2670634db2396b8f2a39c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6034990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3da727092e7c56a19e8b1a382da13658524813ce0d2bca55dee5f4067987b77a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Sat, 07 Mar 2026 00:33:31 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Mar 2026 00:33:34 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Mar 2026 00:36:15 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:36:15 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:36:15 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:36:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:36:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:36:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:36:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:36:16 GMT
USER memcache
# Sat, 07 Mar 2026 00:36:16 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:36:16 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364a7d7b961599919f81b228a22514e1935e6774971d671f38dbad14ef71cbfd`  
		Last Modified: Sat, 07 Mar 2026 00:36:29 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d77d50c27f0ae298d21083636544fb7f795b9708dc480f081e1e936f1246e7`  
		Last Modified: Sat, 07 Mar 2026 00:36:29 GMT  
		Size: 126.3 KB (126266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d559c6185e0bba610ac4ee55bed1b0d85afdad6f054f17906fadb6311cc44007`  
		Last Modified: Sat, 07 Mar 2026 00:36:29 GMT  
		Size: 2.1 MB (2077727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce553e1c7553a28f652dbbd9f3d79596edea9eecf47883032057409cd1d977f`  
		Last Modified: Sat, 07 Mar 2026 00:36:29 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf30d9d84b197d47332200b954fc9fcedf3653c9a44fe6b72a5cf721ec170f1`  
		Last Modified: Sat, 07 Mar 2026 00:36:30 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:7c60879107d9d8ce6f5e597f4c108df4a413d312eaf52e4c9303b96e80e84fbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eee93b7e24e493f45076a5a793e8b01aad30e3643bcb7583bc1fa26a1c4ff826`

```dockerfile
```

-	Layers:
	-	`sha256:b4505eef72239eda1b1c608b3226cd19dc02c372be606494a473db623050489a`  
		Last Modified: Sat, 07 Mar 2026 00:36:29 GMT  
		Size: 94.3 KB (94280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43cc72cbc203c87b12cbef8914fb2835a461df6bb0445da26d96b5a14e610184`  
		Last Modified: Sat, 07 Mar 2026 00:36:29 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; riscv64

```console
$ docker pull memcached@sha256:874942dd4e337f828a5480fa7e7e03b28951302101475540a14d752215e0b99e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5771014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61e6da61960009cb5e1d5f173422857994cb30b45c987fc35062485420c05ddf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 11 Mar 2026 21:21:50 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 11 Mar 2026 21:21:54 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 11 Mar 2026 21:35:15 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 11 Mar 2026 21:35:15 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 11 Mar 2026 21:35:15 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 11 Mar 2026 21:35:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 11 Mar 2026 21:35:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 11 Mar 2026 21:35:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 11 Mar 2026 21:35:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2026 21:35:16 GMT
USER memcache
# Wed, 11 Mar 2026 21:35:16 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 11 Mar 2026 21:35:16 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63b25af376cdb2cb3ddbdf009ec368c61af0677da2ff36f56052ba87ef9d03e`  
		Last Modified: Wed, 11 Mar 2026 21:35:39 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efcf2b36003649471638502666fa028dd48ae26bf7a732d6d7fe38a8432a7016`  
		Last Modified: Wed, 11 Mar 2026 21:35:39 GMT  
		Size: 108.9 KB (108902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddaf732ffb5731ec8232eec8940c917de4727564501c45fce52a7e2ebd641224`  
		Last Modified: Wed, 11 Mar 2026 21:35:40 GMT  
		Size: 2.1 MB (2075471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91cabf0fbda848cc214b782cee7c5c7224ddb7674e75de41599a3bbe85d6a689`  
		Last Modified: Wed, 11 Mar 2026 21:35:39 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:306ecccaa7e256f58e1e772b44b962766fdf35f118efb1596b4c9ae2431987ab`  
		Last Modified: Wed, 11 Mar 2026 21:35:40 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:5e6d73b60a6ccb5dda56fc4d483b45097e7ef55ce412da110e15c6c478c8d882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebcfe45486057ddd0b85095c8ca2fd1a8656b95e8ecf579e4de8717551ada915`

```dockerfile
```

-	Layers:
	-	`sha256:7176cf6ddf61d50975dee6f26ce9fdcb0b77085375b0dde58bb44b8337adca94`  
		Last Modified: Wed, 11 Mar 2026 21:35:39 GMT  
		Size: 94.3 KB (94276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5799ace3d1f3a380e60d9e9676ffbd335daf84ded3af9d5e1dd8ce83eee2060`  
		Last Modified: Wed, 11 Mar 2026 21:35:39 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; s390x

```console
$ docker pull memcached@sha256:9c94884aa3d27f0c0ed5df500b79a6f3c2685bba5c632e3b871c0a262314d935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5858795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cd8a0886a7efaab4d69edd3b15f2a68384bcfdb1ff1a454930ba3a6a6ba29fc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Sat, 07 Mar 2026 00:33:34 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Mar 2026 00:33:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Mar 2026 00:36:49 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:36:49 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:36:49 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:36:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:36:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:36:49 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:36:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:36:49 GMT
USER memcache
# Sat, 07 Mar 2026 00:36:49 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:36:49 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f0d8799f878cf05935221d46a9b462122587e33ba748e54c983e03bbcb7ad2`  
		Last Modified: Sat, 07 Mar 2026 00:36:57 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef440db2f09493c5c9eae06dd0e59dafbd4761a74731e3ffa8ac968dcca712ca`  
		Last Modified: Sat, 07 Mar 2026 00:36:57 GMT  
		Size: 114.3 KB (114309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:134d34534319282a3e54d23ff3c63c0362a6c2ba38fb854b6a94a202d67347c2`  
		Last Modified: Sat, 07 Mar 2026 00:36:57 GMT  
		Size: 2.0 MB (2017802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:655653db981f7dce0174439408f99d0c480cb5082436a0682568bdaab190cd39`  
		Last Modified: Sat, 07 Mar 2026 00:36:57 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92dd0a7cdddba4f0415d5e0b6aa52c11369fa65b7c8c4ae965c949d55e7d52dd`  
		Last Modified: Sat, 07 Mar 2026 00:36:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:b9dd2a68695665b98af82b5110aa7af831b2d15654c26ffd200cc198ac79fb69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29c28af5a544343faaa1ff91b74bb776f4c5013c23bc2f45a2bbadb0fa1acc12`

```dockerfile
```

-	Layers:
	-	`sha256:47a88819c43763550a569259221f913c63dfd51ac45adc283170d20d81240959`  
		Last Modified: Sat, 07 Mar 2026 00:36:57 GMT  
		Size: 94.2 KB (94222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a9409046e85d857b00aa1f263c8c811160eeaa0c58b29abf61985c657289659`  
		Last Modified: Sat, 07 Mar 2026 00:36:57 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-trixie`

```console
$ docker pull memcached@sha256:d99136ed4c1cf2e3fceb498763f2b7fedec7c486a0fe8a57be19f2a0519ce1fa
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
$ docker pull memcached@sha256:c08df224e6ccee2c893ac468902a8b68d8221910014da88f892d483b145f2e80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32197142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc0c289673d3b6f117607d5014b52d276fa02ad622404df04deac38f7a3b2b75`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Sat, 07 Mar 2026 00:34:28 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Mar 2026 00:34:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Mar 2026 00:37:16 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:37:16 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:37:16 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:37:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:37:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:37:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:37:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:37:16 GMT
USER memcache
# Sat, 07 Mar 2026 00:37:16 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:37:16 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65546826072afb14e8706d66b636911c885382731f6d325cba605469fdb363e7`  
		Last Modified: Sat, 07 Mar 2026 00:37:23 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f84d4f33fb93823aaef11588c633186a7b4c7e9c0fea6cf0c2c2e912be6b9f`  
		Last Modified: Sat, 07 Mar 2026 00:37:23 GMT  
		Size: 136.7 KB (136684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f30a00378f01ca7716c334349799965f472572c2377432ae0948fb3481a330`  
		Last Modified: Sat, 07 Mar 2026 00:37:23 GMT  
		Size: 2.3 MB (2280310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd736c12c1d448b0585c460fd3f417da3a21193665ef2aefd67c221cbd97df0b`  
		Last Modified: Sat, 07 Mar 2026 00:37:23 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f072b1e28c7bdff147ef49013b08dfe871999faec678a4219890f645e2d14b`  
		Last Modified: Sat, 07 Mar 2026 00:37:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:b0cd4839975a3f144a6d44260b40e6cebfaad48ae0dabae69c8a84a1912f55ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d69fb1b8b08633539bde084818362e1b13aae93417c6fc42c6c674e4039d2ab4`

```dockerfile
```

-	Layers:
	-	`sha256:0bc9fc51640e8d0b171e44a65462e97d0e54980aca3e0ea45f57320911a0f07c`  
		Last Modified: Sat, 07 Mar 2026 00:37:23 GMT  
		Size: 2.0 MB (2008290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2632163ed214b82be06d84daacb113b153e4ec7def67cd764cb771fb9700aeaf`  
		Last Modified: Sat, 07 Mar 2026 00:37:23 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; arm variant v5

```console
$ docker pull memcached@sha256:514cbf94b5380f36ac3c88108bf78a84ae83c3ed26e638ebe2e2f5bb88bd25ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30304774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc4d63874316ce18eaa26acb02c5e3dc129e31ea8c480a3a966621c75552572c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1771804800'
# Sat, 07 Mar 2026 00:34:25 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Mar 2026 00:34:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Mar 2026 00:37:50 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:37:50 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:37:50 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:37:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:37:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:37:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:37:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:37:50 GMT
USER memcache
# Sat, 07 Mar 2026 00:37:50 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:37:50 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:280a075cc1d2a97445b9f4430aa9774bfc38fc4217b7fc9d6a7b04e7e431cb65`  
		Last Modified: Tue, 24 Feb 2026 18:42:44 GMT  
		Size: 27.9 MB (27947608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fee55b7ab1f18dde561acdb3246640b49ed746f0a6f679b8b4be2fe96c38edc`  
		Last Modified: Sat, 07 Mar 2026 00:37:56 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e90ce24e8e18d6e22b1819e0c183af55656f28a490d2a5f5db1bb199759ae2`  
		Last Modified: Sat, 07 Mar 2026 00:37:56 GMT  
		Size: 144.2 KB (144173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e14eaa4ef07ee7a2796a97655630e5b528d0f2f8120ba62ac860fcf148e2b813`  
		Last Modified: Sat, 07 Mar 2026 00:37:56 GMT  
		Size: 2.2 MB (2211477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0271cbc419600dba0091ae986cd78ada6340afbfa697b93993e1f63555a831`  
		Last Modified: Sat, 07 Mar 2026 00:37:56 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ecc8023e8fc75e87c4b1fc32230e35e765d671345bd42f98dfe13b7118bc13`  
		Last Modified: Sat, 07 Mar 2026 00:37:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:3b41b0fb30672979494c2bcc11e11de72d662cbeef4e097e83bf3637c45aba4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b344e75a26fbd848f3d4bda6dfbc82971e7c99f16f8b8d3c2f4e0046b3e36cf`

```dockerfile
```

-	Layers:
	-	`sha256:a8abf2c9952faed7ee6a8484d94c195f2f516d28b4aa99d61fde6a938373ef14`  
		Last Modified: Sat, 07 Mar 2026 00:37:56 GMT  
		Size: 2.0 MB (2011293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4baff3ba9a329e3fdeaee0149357b33f76e181413fc6e5b4d1b9502670d8aab3`  
		Last Modified: Sat, 07 Mar 2026 00:37:56 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; arm variant v7

```console
$ docker pull memcached@sha256:5e39383d269092b745c7426583a0849917817a2861226858ff17c34f227cadc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28515640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4d89f2522b7f402debcdfe4ae5ef33ccc13694e72756aabd8c894fd1a657663`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Sat, 07 Mar 2026 00:34:26 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Mar 2026 00:34:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Mar 2026 00:37:36 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:37:36 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:37:36 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:37:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:37:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:37:37 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:37:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:37:37 GMT
USER memcache
# Sat, 07 Mar 2026 00:37:37 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:37:37 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b5f623d77fff35b334b15c7b208113b4b778a70ce39168e1270421140984e6`  
		Last Modified: Sat, 07 Mar 2026 00:37:43 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d378422d428b98928a2c392598ff24dddba86412c764099339db2c9b84dab7`  
		Last Modified: Sat, 07 Mar 2026 00:37:43 GMT  
		Size: 135.4 KB (135371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ebe7571649e14f8ae60c2aa9c7464f120d47deb28852880adc72f5958fb268`  
		Last Modified: Sat, 07 Mar 2026 00:37:43 GMT  
		Size: 2.2 MB (2165006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab8a97091ab7e05c0561d93041f6833b293ec83a81c5cd316d914c7cd4797f5`  
		Last Modified: Sat, 07 Mar 2026 00:37:43 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06917ca5c3af99a9a619b7c0077abf8521b0777d4c07464889139b6030aaa445`  
		Last Modified: Sat, 07 Mar 2026 00:37:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:17c7cd3931d1614e411d593e6027c70049d32dd6b78b4523f5e29ff13b7b1f21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b42f736130d7735ab6bde638b9206c6be06a848c316aa0776562b9d2b05634b5`

```dockerfile
```

-	Layers:
	-	`sha256:1700f9d32fecaf2a6fff6e275b9eac8036467ba4e592635351cf279712b2017b`  
		Last Modified: Sat, 07 Mar 2026 00:37:43 GMT  
		Size: 2.0 MB (2009750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef3320ccea4ba2f43dfdeb26388b30f9251a45c8b87522656d05eb856e022fa0`  
		Last Modified: Sat, 07 Mar 2026 00:37:43 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:03ff213526efc235b60a048b3efa0c67c6d697a62bdc207561fb8ee00f254f89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32557234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4742c51756a2139de24009e1c754635923a703d67706387249d261e4dc62712`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Sat, 07 Mar 2026 00:34:23 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Mar 2026 00:34:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Mar 2026 00:37:25 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:37:25 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:37:25 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:37:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:37:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:37:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:37:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:37:25 GMT
USER memcache
# Sat, 07 Mar 2026 00:37:25 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:37:25 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:461d33f62f9a4e4fbc09492d8ce59e548e8c794e3122411c5f7a8370f2bbedba`  
		Last Modified: Sat, 07 Mar 2026 00:37:31 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e642309aa5a12065d7f985c382b7658fa51b45c2a111039cdb9b7240299809e7`  
		Last Modified: Sat, 07 Mar 2026 00:37:31 GMT  
		Size: 153.5 KB (153496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c81e14adafcb230598de8ae3eaf03443a9ae10bd04e616ae4ab64a2f379a48d`  
		Last Modified: Sat, 07 Mar 2026 00:37:31 GMT  
		Size: 2.3 MB (2262125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62e12af1edbdc302c3fd82e9561c5eac5def3110b53dc9d527b277d70a0c5b0`  
		Last Modified: Sat, 07 Mar 2026 00:37:31 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eee7fdafd6f634c0431e5a06be62ff9a726cb1fa8367483d6b026fa3164c7f0`  
		Last Modified: Sat, 07 Mar 2026 00:37:32 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:f791266a2bf814187fed117fa0abd604df8d26056d2e2791b51eb537a958de3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e7b8f74c70d2427388103547caa9c90ef2b4ec4ee11ce197e642593e10f6979`

```dockerfile
```

-	Layers:
	-	`sha256:88d9544d6eb9588edcaeabdc26922a9afb53b2222e8f9972e5b4b52199893738`  
		Last Modified: Sat, 07 Mar 2026 00:37:31 GMT  
		Size: 2.0 MB (2008606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b245266f3e6e113152f086489529a68f1c8c229363d9b678823c16250c48131`  
		Last Modified: Sat, 07 Mar 2026 00:37:31 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; 386

```console
$ docker pull memcached@sha256:1219e49a37eb8fa43f5cabcda7eb69df920734c5d615f2fc63e4fba52a06dfd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33667722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d141db22d43d8c6503a206b3413976c2fd0b84654a45bb46a3da3f39594ee93e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1771804800'
# Sat, 07 Mar 2026 00:34:41 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Mar 2026 00:34:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Mar 2026 00:37:41 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:37:41 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:37:41 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:37:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:37:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:37:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:37:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:37:41 GMT
USER memcache
# Sat, 07 Mar 2026 00:37:41 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:37:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f4e0b944ee1e7e50bdfbfa77bda370b6eccee7d698a7adca78c38f5ca0767ca5`  
		Last Modified: Tue, 24 Feb 2026 18:43:18 GMT  
		Size: 31.3 MB (31293918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d38eff546890db9ae0646486b61a548d8067820adc96ceb6eb4f5d7c2206bb8`  
		Last Modified: Sat, 07 Mar 2026 00:37:47 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c454125cf8ccd03f95714478c13c1d671ba0807b980ee5e6df450d611f61e156`  
		Last Modified: Sat, 07 Mar 2026 00:37:47 GMT  
		Size: 147.5 KB (147517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42b7d17f494cc1acab1da36a724a41a46ecf955d058123b89b170ea63bafda97`  
		Last Modified: Sat, 07 Mar 2026 00:37:47 GMT  
		Size: 2.2 MB (2224772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56fcaee4e2b815384392953fdf84278be4b9a4b116e3a5ad6436f7b13a7c6d9`  
		Last Modified: Sat, 07 Mar 2026 00:37:47 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6adacd7f3e38f46b44efa4ff006b35719382afa26b95b7a9b0c62ef7e7a01bfc`  
		Last Modified: Sat, 07 Mar 2026 00:37:48 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:9f65574f3294736b3dc217e4b07a4045282c517d258eaa96a32035e09cda6fa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb96fc147195e16ed2b6e99c3582cd8c6a67516fb0387c563d09fbf85f6a4dc0`

```dockerfile
```

-	Layers:
	-	`sha256:cdc74dec8f482313433fa0011e8531a8e816610bf31af8b63d2203318e8a59f9`  
		Last Modified: Sat, 07 Mar 2026 00:37:47 GMT  
		Size: 2.0 MB (2005447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bbcbbf7d1935fe3e711cd689ff38f789c3f7334bff2fd2518c106c4bf5d805f`  
		Last Modified: Sat, 07 Mar 2026 00:37:47 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; ppc64le

```console
$ docker pull memcached@sha256:ffac94778c7c882a7f2cbaae5af33e755639de207d07834e052412c2b22a24b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36754462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5640d71fb49b8eaef07631709a9f4924bd191fcfe9b44b7df2d525e247075b64`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Sat, 07 Mar 2026 00:33:31 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Mar 2026 00:33:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Mar 2026 00:56:42 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:56:42 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:56:42 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:56:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:56:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:56:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:56:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:56:44 GMT
USER memcache
# Sat, 07 Mar 2026 00:56:44 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:56:44 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab70996aa4a561e7f3e1f1e1b14df7912a1456b20b317937391cfa826c93f2ea`  
		Last Modified: Sat, 07 Mar 2026 00:57:10 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1ba00921effa53d91205ba3e5e3280c719885f49b5e9e0f8e2a387cf316d89`  
		Last Modified: Sat, 07 Mar 2026 00:57:10 GMT  
		Size: 170.4 KB (170386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd00738358190677470eca91b6732f6fcc475639b7f07f1943af6f5d268ae47`  
		Last Modified: Sat, 07 Mar 2026 00:57:10 GMT  
		Size: 3.0 MB (2982343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f7dc97a8f5d8c677e24bd2f8014c3e315619d726d409033dc3ce4f6d7d7569d`  
		Last Modified: Sat, 07 Mar 2026 00:57:10 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f2b48241128f09e1c613b0fb34d37f79c77417d033b7a00041f8cd08d6241f`  
		Last Modified: Sat, 07 Mar 2026 00:57:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:da557c745e92be8dd35823b9c24b79e47c55ff727768980abe9b659a14672408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e89b8bba62432d49e11baad935eddf449853276e5bb492953ae6bb995bf81ef`

```dockerfile
```

-	Layers:
	-	`sha256:7bf94ead3bca06412117cdc5395bde9d799ffc799dd28be779209634f64bfc0b`  
		Last Modified: Sat, 07 Mar 2026 00:57:10 GMT  
		Size: 2.0 MB (2011891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ec351466954789ecb039e735ecf9fd0235d5d4cfcf8bd6bcf2cf68049016c1c`  
		Last Modified: Sat, 07 Mar 2026 00:57:10 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; riscv64

```console
$ docker pull memcached@sha256:ccac0e143b4efd5bd15fb67df5ad87f5b743cc3db826cbb27d1874cbb3b6d549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30619564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f9320af1aa6fbbae22f81ef28d68694abc001739c71a195b4b1cd490b3b9107`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 23:50:36 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 09 Mar 2026 23:51:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Mar 2026 00:09:03 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 10 Mar 2026 00:09:03 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 10 Mar 2026 00:09:03 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 10 Mar 2026 00:09:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 10 Mar 2026 00:09:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 10 Mar 2026 00:09:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 10 Mar 2026 00:09:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Mar 2026 00:09:03 GMT
USER memcache
# Tue, 10 Mar 2026 00:09:03 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 10 Mar 2026 00:09:03 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e1366b1f74881f04901f31cfdecf9f3f5d4794ebf89911083a239bf462bf21`  
		Last Modified: Tue, 10 Mar 2026 00:09:56 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918782f8ab4ae7fe2ab9f1fc0aa7ad4e48d83dc362a4dcac336048ded3de9b6e`  
		Last Modified: Tue, 10 Mar 2026 00:09:56 GMT  
		Size: 133.1 KB (133079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963fbe1d00657987e81bdc270499ad5aacf8f91b100915c30ddf9fc57cd67346`  
		Last Modified: Tue, 10 Mar 2026 00:09:56 GMT  
		Size: 2.2 MB (2208551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729657786193241c665df2cbaeb72b5d157865abb3bbd8b9460e88d08fb65fea`  
		Last Modified: Tue, 10 Mar 2026 00:09:56 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8246f12fbc1ee94790a418b9655df55d80968171273b5994aaffa40c04fa2f3c`  
		Last Modified: Tue, 10 Mar 2026 00:09:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:de9f0d80a354763898649af4229a6f696fb51689e3b577af2e1d918d365777e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d72c30b80e1c2deaee38b267b52cab1a28e245b2a3608fcf459f2232dad3faa7`

```dockerfile
```

-	Layers:
	-	`sha256:03d9f11a7e8cf93ffe1f13ecfd86632a66af5a6efc142ae7a4ecac0c19418b2d`  
		Last Modified: Tue, 10 Mar 2026 00:09:56 GMT  
		Size: 2.0 MB (2002254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:452e3f764b5054c447aa8e63046155a20784d6f10159282ce633afdb79bf9279`  
		Last Modified: Tue, 10 Mar 2026 00:09:56 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; s390x

```console
$ docker pull memcached@sha256:8e1f3fb07bf1702ad27a7e2a6b2364e61d7b5165c113d0202db31adaa90d91df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32278340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1088ed36ed575f78d3e06fdd24f1ccdcc908d6e579970b2cae128c29f8d6e7a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Sat, 07 Mar 2026 00:33:32 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Mar 2026 00:33:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Mar 2026 00:36:51 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:36:51 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:36:51 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:36:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:36:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:36:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:36:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:36:51 GMT
USER memcache
# Sat, 07 Mar 2026 00:36:51 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:36:51 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986cc162f1a9b2f1b4c673da47497d87b8a542990f29c7823ee4d64cd160ea34`  
		Last Modified: Sat, 07 Mar 2026 00:37:00 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e3b516d24d039487b70f5d718d6f2b0c5473b5da4e6b82815239c7730587d6`  
		Last Modified: Sat, 07 Mar 2026 00:37:00 GMT  
		Size: 140.5 KB (140520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb611bdb547903f4763e52741be4c28e6ed0f172ebffc4ddae4e56a1a4d3ebc2`  
		Last Modified: Sat, 07 Mar 2026 00:37:00 GMT  
		Size: 2.3 MB (2298126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b32c7b8a27f2284141ba22bde8036a295b3e0d397cde405054e47e550cced01`  
		Last Modified: Sat, 07 Mar 2026 00:37:00 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3240387a49966ed4c1475913af7c7648c5499d01045e56e16637a760300918a`  
		Last Modified: Sat, 07 Mar 2026 00:37:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:b725149e071a1d02723f7674a5f7c477144350f79f2243558bce2360da7bf73b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:628ead940c50f3d4776c150c412d2270c2238893cfd1a57f8c17647ec35223e2`

```dockerfile
```

-	Layers:
	-	`sha256:b118af94ed9d10ab8f0c0221725860a15ff82dce98bd35abb240f411b745e0f7`  
		Last Modified: Sat, 07 Mar 2026 00:37:00 GMT  
		Size: 2.0 MB (2009727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:737fa51b5113fe89d161d6b7d0d81d66c28e666617dc1fb7c410b093ecf35625`  
		Last Modified: Sat, 07 Mar 2026 00:37:00 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6`

```console
$ docker pull memcached@sha256:d99136ed4c1cf2e3fceb498763f2b7fedec7c486a0fe8a57be19f2a0519ce1fa
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
$ docker pull memcached@sha256:c08df224e6ccee2c893ac468902a8b68d8221910014da88f892d483b145f2e80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32197142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc0c289673d3b6f117607d5014b52d276fa02ad622404df04deac38f7a3b2b75`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Sat, 07 Mar 2026 00:34:28 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Mar 2026 00:34:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Mar 2026 00:37:16 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:37:16 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:37:16 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:37:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:37:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:37:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:37:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:37:16 GMT
USER memcache
# Sat, 07 Mar 2026 00:37:16 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:37:16 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65546826072afb14e8706d66b636911c885382731f6d325cba605469fdb363e7`  
		Last Modified: Sat, 07 Mar 2026 00:37:23 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f84d4f33fb93823aaef11588c633186a7b4c7e9c0fea6cf0c2c2e912be6b9f`  
		Last Modified: Sat, 07 Mar 2026 00:37:23 GMT  
		Size: 136.7 KB (136684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f30a00378f01ca7716c334349799965f472572c2377432ae0948fb3481a330`  
		Last Modified: Sat, 07 Mar 2026 00:37:23 GMT  
		Size: 2.3 MB (2280310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd736c12c1d448b0585c460fd3f417da3a21193665ef2aefd67c221cbd97df0b`  
		Last Modified: Sat, 07 Mar 2026 00:37:23 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f072b1e28c7bdff147ef49013b08dfe871999faec678a4219890f645e2d14b`  
		Last Modified: Sat, 07 Mar 2026 00:37:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:b0cd4839975a3f144a6d44260b40e6cebfaad48ae0dabae69c8a84a1912f55ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d69fb1b8b08633539bde084818362e1b13aae93417c6fc42c6c674e4039d2ab4`

```dockerfile
```

-	Layers:
	-	`sha256:0bc9fc51640e8d0b171e44a65462e97d0e54980aca3e0ea45f57320911a0f07c`  
		Last Modified: Sat, 07 Mar 2026 00:37:23 GMT  
		Size: 2.0 MB (2008290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2632163ed214b82be06d84daacb113b153e4ec7def67cd764cb771fb9700aeaf`  
		Last Modified: Sat, 07 Mar 2026 00:37:23 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm variant v5

```console
$ docker pull memcached@sha256:514cbf94b5380f36ac3c88108bf78a84ae83c3ed26e638ebe2e2f5bb88bd25ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30304774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc4d63874316ce18eaa26acb02c5e3dc129e31ea8c480a3a966621c75552572c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1771804800'
# Sat, 07 Mar 2026 00:34:25 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Mar 2026 00:34:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Mar 2026 00:37:50 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:37:50 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:37:50 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:37:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:37:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:37:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:37:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:37:50 GMT
USER memcache
# Sat, 07 Mar 2026 00:37:50 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:37:50 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:280a075cc1d2a97445b9f4430aa9774bfc38fc4217b7fc9d6a7b04e7e431cb65`  
		Last Modified: Tue, 24 Feb 2026 18:42:44 GMT  
		Size: 27.9 MB (27947608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fee55b7ab1f18dde561acdb3246640b49ed746f0a6f679b8b4be2fe96c38edc`  
		Last Modified: Sat, 07 Mar 2026 00:37:56 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e90ce24e8e18d6e22b1819e0c183af55656f28a490d2a5f5db1bb199759ae2`  
		Last Modified: Sat, 07 Mar 2026 00:37:56 GMT  
		Size: 144.2 KB (144173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e14eaa4ef07ee7a2796a97655630e5b528d0f2f8120ba62ac860fcf148e2b813`  
		Last Modified: Sat, 07 Mar 2026 00:37:56 GMT  
		Size: 2.2 MB (2211477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0271cbc419600dba0091ae986cd78ada6340afbfa697b93993e1f63555a831`  
		Last Modified: Sat, 07 Mar 2026 00:37:56 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ecc8023e8fc75e87c4b1fc32230e35e765d671345bd42f98dfe13b7118bc13`  
		Last Modified: Sat, 07 Mar 2026 00:37:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:3b41b0fb30672979494c2bcc11e11de72d662cbeef4e097e83bf3637c45aba4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b344e75a26fbd848f3d4bda6dfbc82971e7c99f16f8b8d3c2f4e0046b3e36cf`

```dockerfile
```

-	Layers:
	-	`sha256:a8abf2c9952faed7ee6a8484d94c195f2f516d28b4aa99d61fde6a938373ef14`  
		Last Modified: Sat, 07 Mar 2026 00:37:56 GMT  
		Size: 2.0 MB (2011293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4baff3ba9a329e3fdeaee0149357b33f76e181413fc6e5b4d1b9502670d8aab3`  
		Last Modified: Sat, 07 Mar 2026 00:37:56 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm variant v7

```console
$ docker pull memcached@sha256:5e39383d269092b745c7426583a0849917817a2861226858ff17c34f227cadc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28515640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4d89f2522b7f402debcdfe4ae5ef33ccc13694e72756aabd8c894fd1a657663`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Sat, 07 Mar 2026 00:34:26 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Mar 2026 00:34:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Mar 2026 00:37:36 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:37:36 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:37:36 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:37:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:37:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:37:37 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:37:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:37:37 GMT
USER memcache
# Sat, 07 Mar 2026 00:37:37 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:37:37 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b5f623d77fff35b334b15c7b208113b4b778a70ce39168e1270421140984e6`  
		Last Modified: Sat, 07 Mar 2026 00:37:43 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d378422d428b98928a2c392598ff24dddba86412c764099339db2c9b84dab7`  
		Last Modified: Sat, 07 Mar 2026 00:37:43 GMT  
		Size: 135.4 KB (135371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ebe7571649e14f8ae60c2aa9c7464f120d47deb28852880adc72f5958fb268`  
		Last Modified: Sat, 07 Mar 2026 00:37:43 GMT  
		Size: 2.2 MB (2165006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab8a97091ab7e05c0561d93041f6833b293ec83a81c5cd316d914c7cd4797f5`  
		Last Modified: Sat, 07 Mar 2026 00:37:43 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06917ca5c3af99a9a619b7c0077abf8521b0777d4c07464889139b6030aaa445`  
		Last Modified: Sat, 07 Mar 2026 00:37:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:17c7cd3931d1614e411d593e6027c70049d32dd6b78b4523f5e29ff13b7b1f21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b42f736130d7735ab6bde638b9206c6be06a848c316aa0776562b9d2b05634b5`

```dockerfile
```

-	Layers:
	-	`sha256:1700f9d32fecaf2a6fff6e275b9eac8036467ba4e592635351cf279712b2017b`  
		Last Modified: Sat, 07 Mar 2026 00:37:43 GMT  
		Size: 2.0 MB (2009750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef3320ccea4ba2f43dfdeb26388b30f9251a45c8b87522656d05eb856e022fa0`  
		Last Modified: Sat, 07 Mar 2026 00:37:43 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:03ff213526efc235b60a048b3efa0c67c6d697a62bdc207561fb8ee00f254f89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32557234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4742c51756a2139de24009e1c754635923a703d67706387249d261e4dc62712`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Sat, 07 Mar 2026 00:34:23 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Mar 2026 00:34:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Mar 2026 00:37:25 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:37:25 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:37:25 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:37:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:37:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:37:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:37:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:37:25 GMT
USER memcache
# Sat, 07 Mar 2026 00:37:25 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:37:25 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:461d33f62f9a4e4fbc09492d8ce59e548e8c794e3122411c5f7a8370f2bbedba`  
		Last Modified: Sat, 07 Mar 2026 00:37:31 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e642309aa5a12065d7f985c382b7658fa51b45c2a111039cdb9b7240299809e7`  
		Last Modified: Sat, 07 Mar 2026 00:37:31 GMT  
		Size: 153.5 KB (153496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c81e14adafcb230598de8ae3eaf03443a9ae10bd04e616ae4ab64a2f379a48d`  
		Last Modified: Sat, 07 Mar 2026 00:37:31 GMT  
		Size: 2.3 MB (2262125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62e12af1edbdc302c3fd82e9561c5eac5def3110b53dc9d527b277d70a0c5b0`  
		Last Modified: Sat, 07 Mar 2026 00:37:31 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eee7fdafd6f634c0431e5a06be62ff9a726cb1fa8367483d6b026fa3164c7f0`  
		Last Modified: Sat, 07 Mar 2026 00:37:32 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:f791266a2bf814187fed117fa0abd604df8d26056d2e2791b51eb537a958de3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e7b8f74c70d2427388103547caa9c90ef2b4ec4ee11ce197e642593e10f6979`

```dockerfile
```

-	Layers:
	-	`sha256:88d9544d6eb9588edcaeabdc26922a9afb53b2222e8f9972e5b4b52199893738`  
		Last Modified: Sat, 07 Mar 2026 00:37:31 GMT  
		Size: 2.0 MB (2008606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b245266f3e6e113152f086489529a68f1c8c229363d9b678823c16250c48131`  
		Last Modified: Sat, 07 Mar 2026 00:37:31 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; 386

```console
$ docker pull memcached@sha256:1219e49a37eb8fa43f5cabcda7eb69df920734c5d615f2fc63e4fba52a06dfd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33667722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d141db22d43d8c6503a206b3413976c2fd0b84654a45bb46a3da3f39594ee93e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1771804800'
# Sat, 07 Mar 2026 00:34:41 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Mar 2026 00:34:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Mar 2026 00:37:41 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:37:41 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:37:41 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:37:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:37:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:37:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:37:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:37:41 GMT
USER memcache
# Sat, 07 Mar 2026 00:37:41 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:37:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f4e0b944ee1e7e50bdfbfa77bda370b6eccee7d698a7adca78c38f5ca0767ca5`  
		Last Modified: Tue, 24 Feb 2026 18:43:18 GMT  
		Size: 31.3 MB (31293918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d38eff546890db9ae0646486b61a548d8067820adc96ceb6eb4f5d7c2206bb8`  
		Last Modified: Sat, 07 Mar 2026 00:37:47 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c454125cf8ccd03f95714478c13c1d671ba0807b980ee5e6df450d611f61e156`  
		Last Modified: Sat, 07 Mar 2026 00:37:47 GMT  
		Size: 147.5 KB (147517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42b7d17f494cc1acab1da36a724a41a46ecf955d058123b89b170ea63bafda97`  
		Last Modified: Sat, 07 Mar 2026 00:37:47 GMT  
		Size: 2.2 MB (2224772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56fcaee4e2b815384392953fdf84278be4b9a4b116e3a5ad6436f7b13a7c6d9`  
		Last Modified: Sat, 07 Mar 2026 00:37:47 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6adacd7f3e38f46b44efa4ff006b35719382afa26b95b7a9b0c62ef7e7a01bfc`  
		Last Modified: Sat, 07 Mar 2026 00:37:48 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:9f65574f3294736b3dc217e4b07a4045282c517d258eaa96a32035e09cda6fa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb96fc147195e16ed2b6e99c3582cd8c6a67516fb0387c563d09fbf85f6a4dc0`

```dockerfile
```

-	Layers:
	-	`sha256:cdc74dec8f482313433fa0011e8531a8e816610bf31af8b63d2203318e8a59f9`  
		Last Modified: Sat, 07 Mar 2026 00:37:47 GMT  
		Size: 2.0 MB (2005447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bbcbbf7d1935fe3e711cd689ff38f789c3f7334bff2fd2518c106c4bf5d805f`  
		Last Modified: Sat, 07 Mar 2026 00:37:47 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; ppc64le

```console
$ docker pull memcached@sha256:ffac94778c7c882a7f2cbaae5af33e755639de207d07834e052412c2b22a24b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36754462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5640d71fb49b8eaef07631709a9f4924bd191fcfe9b44b7df2d525e247075b64`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Sat, 07 Mar 2026 00:33:31 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Mar 2026 00:33:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Mar 2026 00:56:42 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:56:42 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:56:42 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:56:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:56:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:56:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:56:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:56:44 GMT
USER memcache
# Sat, 07 Mar 2026 00:56:44 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:56:44 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab70996aa4a561e7f3e1f1e1b14df7912a1456b20b317937391cfa826c93f2ea`  
		Last Modified: Sat, 07 Mar 2026 00:57:10 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1ba00921effa53d91205ba3e5e3280c719885f49b5e9e0f8e2a387cf316d89`  
		Last Modified: Sat, 07 Mar 2026 00:57:10 GMT  
		Size: 170.4 KB (170386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd00738358190677470eca91b6732f6fcc475639b7f07f1943af6f5d268ae47`  
		Last Modified: Sat, 07 Mar 2026 00:57:10 GMT  
		Size: 3.0 MB (2982343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f7dc97a8f5d8c677e24bd2f8014c3e315619d726d409033dc3ce4f6d7d7569d`  
		Last Modified: Sat, 07 Mar 2026 00:57:10 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f2b48241128f09e1c613b0fb34d37f79c77417d033b7a00041f8cd08d6241f`  
		Last Modified: Sat, 07 Mar 2026 00:57:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:da557c745e92be8dd35823b9c24b79e47c55ff727768980abe9b659a14672408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e89b8bba62432d49e11baad935eddf449853276e5bb492953ae6bb995bf81ef`

```dockerfile
```

-	Layers:
	-	`sha256:7bf94ead3bca06412117cdc5395bde9d799ffc799dd28be779209634f64bfc0b`  
		Last Modified: Sat, 07 Mar 2026 00:57:10 GMT  
		Size: 2.0 MB (2011891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ec351466954789ecb039e735ecf9fd0235d5d4cfcf8bd6bcf2cf68049016c1c`  
		Last Modified: Sat, 07 Mar 2026 00:57:10 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; riscv64

```console
$ docker pull memcached@sha256:ccac0e143b4efd5bd15fb67df5ad87f5b743cc3db826cbb27d1874cbb3b6d549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30619564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f9320af1aa6fbbae22f81ef28d68694abc001739c71a195b4b1cd490b3b9107`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 23:50:36 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 09 Mar 2026 23:51:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Mar 2026 00:09:03 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 10 Mar 2026 00:09:03 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 10 Mar 2026 00:09:03 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 10 Mar 2026 00:09:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 10 Mar 2026 00:09:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 10 Mar 2026 00:09:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 10 Mar 2026 00:09:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Mar 2026 00:09:03 GMT
USER memcache
# Tue, 10 Mar 2026 00:09:03 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 10 Mar 2026 00:09:03 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e1366b1f74881f04901f31cfdecf9f3f5d4794ebf89911083a239bf462bf21`  
		Last Modified: Tue, 10 Mar 2026 00:09:56 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918782f8ab4ae7fe2ab9f1fc0aa7ad4e48d83dc362a4dcac336048ded3de9b6e`  
		Last Modified: Tue, 10 Mar 2026 00:09:56 GMT  
		Size: 133.1 KB (133079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963fbe1d00657987e81bdc270499ad5aacf8f91b100915c30ddf9fc57cd67346`  
		Last Modified: Tue, 10 Mar 2026 00:09:56 GMT  
		Size: 2.2 MB (2208551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729657786193241c665df2cbaeb72b5d157865abb3bbd8b9460e88d08fb65fea`  
		Last Modified: Tue, 10 Mar 2026 00:09:56 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8246f12fbc1ee94790a418b9655df55d80968171273b5994aaffa40c04fa2f3c`  
		Last Modified: Tue, 10 Mar 2026 00:09:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:de9f0d80a354763898649af4229a6f696fb51689e3b577af2e1d918d365777e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d72c30b80e1c2deaee38b267b52cab1a28e245b2a3608fcf459f2232dad3faa7`

```dockerfile
```

-	Layers:
	-	`sha256:03d9f11a7e8cf93ffe1f13ecfd86632a66af5a6efc142ae7a4ecac0c19418b2d`  
		Last Modified: Tue, 10 Mar 2026 00:09:56 GMT  
		Size: 2.0 MB (2002254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:452e3f764b5054c447aa8e63046155a20784d6f10159282ce633afdb79bf9279`  
		Last Modified: Tue, 10 Mar 2026 00:09:56 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; s390x

```console
$ docker pull memcached@sha256:8e1f3fb07bf1702ad27a7e2a6b2364e61d7b5165c113d0202db31adaa90d91df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32278340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1088ed36ed575f78d3e06fdd24f1ccdcc908d6e579970b2cae128c29f8d6e7a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Sat, 07 Mar 2026 00:33:32 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Mar 2026 00:33:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Mar 2026 00:36:51 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:36:51 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:36:51 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:36:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:36:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:36:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:36:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:36:51 GMT
USER memcache
# Sat, 07 Mar 2026 00:36:51 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:36:51 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986cc162f1a9b2f1b4c673da47497d87b8a542990f29c7823ee4d64cd160ea34`  
		Last Modified: Sat, 07 Mar 2026 00:37:00 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e3b516d24d039487b70f5d718d6f2b0c5473b5da4e6b82815239c7730587d6`  
		Last Modified: Sat, 07 Mar 2026 00:37:00 GMT  
		Size: 140.5 KB (140520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb611bdb547903f4763e52741be4c28e6ed0f172ebffc4ddae4e56a1a4d3ebc2`  
		Last Modified: Sat, 07 Mar 2026 00:37:00 GMT  
		Size: 2.3 MB (2298126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b32c7b8a27f2284141ba22bde8036a295b3e0d397cde405054e47e550cced01`  
		Last Modified: Sat, 07 Mar 2026 00:37:00 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3240387a49966ed4c1475913af7c7648c5499d01045e56e16637a760300918a`  
		Last Modified: Sat, 07 Mar 2026 00:37:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:b725149e071a1d02723f7674a5f7c477144350f79f2243558bce2360da7bf73b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:628ead940c50f3d4776c150c412d2270c2238893cfd1a57f8c17647ec35223e2`

```dockerfile
```

-	Layers:
	-	`sha256:b118af94ed9d10ab8f0c0221725860a15ff82dce98bd35abb240f411b745e0f7`  
		Last Modified: Sat, 07 Mar 2026 00:37:00 GMT  
		Size: 2.0 MB (2009727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:737fa51b5113fe89d161d6b7d0d81d66c28e666617dc1fb7c410b093ecf35625`  
		Last Modified: Sat, 07 Mar 2026 00:37:00 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine`

```console
$ docker pull memcached@sha256:1c6a2d48c5f561226f1dc54ed37132f83b4cde94b5e3f3e2d88386d028b86a27
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
$ docker pull memcached@sha256:84dd21b0c8ebc30032a8aaa7270c7e6c11da52efd7bf3c7593530168946d3bd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5959699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaf5f46bdf2c26a9dda97cd7dd2b6a05c5d8135b2f9cbacf33ff8e8365f5e1eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Sat, 07 Mar 2026 00:36:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Mar 2026 00:36:14 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Mar 2026 00:38:52 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:38:52 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:38:52 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:38:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:38:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:38:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:38:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:38:52 GMT
USER memcache
# Sat, 07 Mar 2026 00:38:52 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:38:52 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d055707374a501222192f988c0ff35fcfdc5a017dd49a48e1dd38106c605f400`  
		Last Modified: Sat, 07 Mar 2026 00:38:57 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5abb10c57422a10d35029047d7b017a29437bc0081f375524cbfb3db3c9eaf9`  
		Last Modified: Sat, 07 Mar 2026 00:38:57 GMT  
		Size: 106.1 KB (106057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4fd18d57089d5254541b428a6a2429569ff07d571c824af865b666901af275e`  
		Last Modified: Sat, 07 Mar 2026 00:38:57 GMT  
		Size: 2.0 MB (1990468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885d9eb83efad8e7a74f165d5e00bd1e547b62348f4084f8748eb5123cfd5ef2`  
		Last Modified: Sat, 07 Mar 2026 00:38:57 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32954341fb1b6227e3bb596d1a3f58beb03c348455e63c0e6a810197d1922e9`  
		Last Modified: Sat, 07 Mar 2026 00:38:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:e0615e85e00302f3ab01f14593cf39cf7e4ac01f448e6904dd61247bf63b3ff0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3b92ada03392c40180327b1e82f1b29a80b1164d4b65115558c1efc811142ad`

```dockerfile
```

-	Layers:
	-	`sha256:cc3e65e74aa6c619611c020b3d498d3c756e6168a9b26434ca30c3099cfa3261`  
		Last Modified: Sat, 07 Mar 2026 00:38:57 GMT  
		Size: 94.9 KB (94873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:327a47bce4975ea9e581754831550ac249839dc3708d4841f78ebc6cbd78d014`  
		Last Modified: Sat, 07 Mar 2026 00:38:57 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:6cde7ea7574023751e83c90e1e8f1f7aef03c1d5b0fbe20a17d981d57edb99dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:376e43ecede029f4d02a7634c75d3107a5797f724660eb9b02b0eb12c3e49748`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Sat, 07 Mar 2026 00:34:25 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Mar 2026 00:34:26 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Mar 2026 00:37:29 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:37:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:37:29 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:37:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:37:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:37:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:37:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:37:29 GMT
USER memcache
# Sat, 07 Mar 2026 00:37:29 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:37:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18dad4d028ff2b78314498b57b872634656cb70add272a07cde87477543ea34b`  
		Last Modified: Sat, 07 Mar 2026 00:37:33 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5343ac0baa24b86f7ffac4e0a3296276d4a7aa05b74617720244260e34dc5aba`  
		Last Modified: Sat, 07 Mar 2026 00:37:33 GMT  
		Size: 102.7 KB (102655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f65584616382b3a0c0b70214fd4046110bedf9cfbb2c2f89c2301372f8aa27`  
		Last Modified: Sat, 07 Mar 2026 00:37:33 GMT  
		Size: 1.9 MB (1940281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a378f9c04f9d21fc788013f2928b3637ad3724011b85ecb4d8fe5a61ca9bb2`  
		Last Modified: Sat, 07 Mar 2026 00:37:33 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9600d067846989777b70f754cdd61c2012197736201713e9b5ff3703b147be02`  
		Last Modified: Sat, 07 Mar 2026 00:37:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:1d36396e4f4bb90ed2d326fbc737d8ab225cf619e64f08c3ff0beaff000177ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e204629c18255bb70ea677237338842d7ed3a140e1ecbbc4b8d5727cafa1668e`

```dockerfile
```

-	Layers:
	-	`sha256:1ea1c312fb87cc4d7c73a561d98b13a1f13504625a2de3953101370977fc6745`  
		Last Modified: Sat, 07 Mar 2026 00:37:33 GMT  
		Size: 20.5 KB (20466 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:91fe29148d686af2a0fdc23ba01a1b272f4c6365fc45bc37d00d4687a0c41b1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5273746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a56ac817dd40669cbf75609948d0f6fc05e648f6453d8f9deba7740682f741f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Sat, 07 Mar 2026 00:37:41 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Mar 2026 00:37:42 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Mar 2026 00:40:39 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:40:39 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:40:39 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:40:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:40:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:40:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:40:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:40:39 GMT
USER memcache
# Sat, 07 Mar 2026 00:40:39 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:40:39 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a51b7877e94969180dbb0be219881bc9230f055057f9e3f4b65f1db0708689a`  
		Last Modified: Sat, 07 Mar 2026 00:40:44 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c32abf408db65abfcd3224db5db2abaa977bd3ce59942c389c73320a4051cc`  
		Last Modified: Sat, 07 Mar 2026 00:40:44 GMT  
		Size: 92.4 KB (92374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ddc29b1020998fb5a3b242cc4e45954bc53540a31017ab6a020f9dff807bd22`  
		Last Modified: Sat, 07 Mar 2026 00:40:44 GMT  
		Size: 1.9 MB (1898298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae00440f5f6fd5951552907706f8df3661315090758ede99bb2933aa3384040b`  
		Last Modified: Sat, 07 Mar 2026 00:40:44 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb70de481e3407c522658dfa65d701fde07648ab9b8c732379d8a92f44092a81`  
		Last Modified: Sat, 07 Mar 2026 00:40:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:073366e4d50888ea6d43868ab35c2a063ea12dc243105f0c614c4feaa55d0eda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c47e8e147c04b6fae9be2f9c70644395f05ac10516981d5f48aac87100f9aabf`

```dockerfile
```

-	Layers:
	-	`sha256:f128294dbb16b2300fe484115b6bd24498974e73ac8835f70a3dd5df2f3211cd`  
		Last Modified: Sat, 07 Mar 2026 00:40:44 GMT  
		Size: 94.3 KB (94291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad6c6671c716b1f4cb8882be9d7cee792a3b5a0500ba4330e4c34c83d3401a1c`  
		Last Modified: Sat, 07 Mar 2026 00:40:44 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:eeb1c0de2b6b33a7a724454aaf9fd945503a062302d133c059f1b829db991b61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6287490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0de2d8f866d91b49adb4cfa80ffd26e168ac627328864d7ceae76dfd0bc4d7a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Sat, 07 Mar 2026 00:36:34 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Mar 2026 00:36:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Mar 2026 00:39:22 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:39:22 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:39:22 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:39:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:39:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:39:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:39:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:39:22 GMT
USER memcache
# Sat, 07 Mar 2026 00:39:22 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:39:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d65cacaa69d1c76240e558dab714b69561f9bb333c2c1c147f9be7d6b29c36`  
		Last Modified: Sat, 07 Mar 2026 00:39:27 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca80346986e335b6e96f14599a1ab3629964fa8702f4570e2d199da8b04498e`  
		Last Modified: Sat, 07 Mar 2026 00:39:27 GMT  
		Size: 121.9 KB (121860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bcaaaf5541ab3a5d055204886aadf36871e66f535b6c1978b4b4c58a4dc2367`  
		Last Modified: Sat, 07 Mar 2026 00:39:27 GMT  
		Size: 2.0 MB (1967188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6167d1b1458d5cedc7774a2a1e9e621f5b32de851a6b19d82ea2275ec9f1bc5`  
		Last Modified: Sat, 07 Mar 2026 00:39:27 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2040432b455fd0270cf480396dc9c1570b8710e21539cc0110e13fe10105062`  
		Last Modified: Sat, 07 Mar 2026 00:39:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:3d8284de1f87be934ca3ad16b60f3a624262a50260f7f8db4cc80575af22e7c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9a54dfb1a405917a8fe0eaf03a1588913998eac5cacc5141cad5d053c6ba838`

```dockerfile
```

-	Layers:
	-	`sha256:8eefe1140db7c68e1990a3744cd3126838a63605758bc6825cb1c090277cf806`  
		Last Modified: Sat, 07 Mar 2026 00:39:27 GMT  
		Size: 94.3 KB (94327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92f28d8e0dd01f916858b48749b2827fadaadb7ca45a0a8a872ac9d74043589d`  
		Last Modified: Sat, 07 Mar 2026 00:39:27 GMT  
		Size: 20.7 KB (20728 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; 386

```console
$ docker pull memcached@sha256:006134e843d0ad5a3c64e903cc20d00c9f3e78a542fa3d6ba1e3ecec5b0ba3c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5742709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06188a4fb3481bcf32a3e44fca9d58ab763a52c65e02c95fbef5e98f4b78ee86`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Sat, 07 Mar 2026 00:37:00 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Mar 2026 00:37:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Mar 2026 00:39:49 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:39:49 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:39:49 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:39:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:39:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:39:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:39:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:39:50 GMT
USER memcache
# Sat, 07 Mar 2026 00:39:50 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:39:50 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ba4a2e327b273e788cfdef17b5c31ac5fefd6010584aa1c11b0d0104a041d6`  
		Last Modified: Sat, 07 Mar 2026 00:39:54 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ba4e8e1182330d5f76532f2f48fe38af386558e3e7fa4d94ce3dbf055be5ab`  
		Last Modified: Sat, 07 Mar 2026 00:39:54 GMT  
		Size: 110.7 KB (110732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01c1fe355d65277d08c7962b0be21d39386b4121b36381bbcb9a60d29449a5c`  
		Last Modified: Sat, 07 Mar 2026 00:39:54 GMT  
		Size: 1.9 MB (1943630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e102587e979593069cf080e59b8471ecf62f9c40abad1e62014f1742341827d0`  
		Last Modified: Sat, 07 Mar 2026 00:39:54 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46411b86935a4104c9cbb43c595a9cbf0e0330c814ca33c36935c5a9cb7f37d`  
		Last Modified: Sat, 07 Mar 2026 00:39:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:d0cb60f8d8c989514001fd52bf793673fa8f281758af2b58f8359d1d41973b11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58f3853067ae595d4075c459fe7b8361d199af21eaa1f93413e882c2e0bc9042`

```dockerfile
```

-	Layers:
	-	`sha256:2cd10df8bfae391e9a94e270083baf145ca51970a41e64ab71cd781740d00c73`  
		Last Modified: Sat, 07 Mar 2026 00:39:54 GMT  
		Size: 94.8 KB (94828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1d4f0d3116c96944777e5e4b1130eaff94973a8664033f37d3c60ceb36ed173`  
		Last Modified: Sat, 07 Mar 2026 00:39:54 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:35c354ed5e627574c294e54f0232ed89e8eacd7ed7e2670634db2396b8f2a39c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6034990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3da727092e7c56a19e8b1a382da13658524813ce0d2bca55dee5f4067987b77a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Sat, 07 Mar 2026 00:33:31 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Mar 2026 00:33:34 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Mar 2026 00:36:15 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:36:15 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:36:15 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:36:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:36:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:36:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:36:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:36:16 GMT
USER memcache
# Sat, 07 Mar 2026 00:36:16 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:36:16 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364a7d7b961599919f81b228a22514e1935e6774971d671f38dbad14ef71cbfd`  
		Last Modified: Sat, 07 Mar 2026 00:36:29 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d77d50c27f0ae298d21083636544fb7f795b9708dc480f081e1e936f1246e7`  
		Last Modified: Sat, 07 Mar 2026 00:36:29 GMT  
		Size: 126.3 KB (126266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d559c6185e0bba610ac4ee55bed1b0d85afdad6f054f17906fadb6311cc44007`  
		Last Modified: Sat, 07 Mar 2026 00:36:29 GMT  
		Size: 2.1 MB (2077727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce553e1c7553a28f652dbbd9f3d79596edea9eecf47883032057409cd1d977f`  
		Last Modified: Sat, 07 Mar 2026 00:36:29 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf30d9d84b197d47332200b954fc9fcedf3653c9a44fe6b72a5cf721ec170f1`  
		Last Modified: Sat, 07 Mar 2026 00:36:30 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7c60879107d9d8ce6f5e597f4c108df4a413d312eaf52e4c9303b96e80e84fbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eee93b7e24e493f45076a5a793e8b01aad30e3643bcb7583bc1fa26a1c4ff826`

```dockerfile
```

-	Layers:
	-	`sha256:b4505eef72239eda1b1c608b3226cd19dc02c372be606494a473db623050489a`  
		Last Modified: Sat, 07 Mar 2026 00:36:29 GMT  
		Size: 94.3 KB (94280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43cc72cbc203c87b12cbef8914fb2835a461df6bb0445da26d96b5a14e610184`  
		Last Modified: Sat, 07 Mar 2026 00:36:29 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:874942dd4e337f828a5480fa7e7e03b28951302101475540a14d752215e0b99e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5771014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61e6da61960009cb5e1d5f173422857994cb30b45c987fc35062485420c05ddf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 11 Mar 2026 21:21:50 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 11 Mar 2026 21:21:54 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 11 Mar 2026 21:35:15 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 11 Mar 2026 21:35:15 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 11 Mar 2026 21:35:15 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 11 Mar 2026 21:35:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 11 Mar 2026 21:35:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 11 Mar 2026 21:35:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 11 Mar 2026 21:35:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2026 21:35:16 GMT
USER memcache
# Wed, 11 Mar 2026 21:35:16 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 11 Mar 2026 21:35:16 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63b25af376cdb2cb3ddbdf009ec368c61af0677da2ff36f56052ba87ef9d03e`  
		Last Modified: Wed, 11 Mar 2026 21:35:39 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efcf2b36003649471638502666fa028dd48ae26bf7a732d6d7fe38a8432a7016`  
		Last Modified: Wed, 11 Mar 2026 21:35:39 GMT  
		Size: 108.9 KB (108902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddaf732ffb5731ec8232eec8940c917de4727564501c45fce52a7e2ebd641224`  
		Last Modified: Wed, 11 Mar 2026 21:35:40 GMT  
		Size: 2.1 MB (2075471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91cabf0fbda848cc214b782cee7c5c7224ddb7674e75de41599a3bbe85d6a689`  
		Last Modified: Wed, 11 Mar 2026 21:35:39 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:306ecccaa7e256f58e1e772b44b962766fdf35f118efb1596b4c9ae2431987ab`  
		Last Modified: Wed, 11 Mar 2026 21:35:40 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:5e6d73b60a6ccb5dda56fc4d483b45097e7ef55ce412da110e15c6c478c8d882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebcfe45486057ddd0b85095c8ca2fd1a8656b95e8ecf579e4de8717551ada915`

```dockerfile
```

-	Layers:
	-	`sha256:7176cf6ddf61d50975dee6f26ce9fdcb0b77085375b0dde58bb44b8337adca94`  
		Last Modified: Wed, 11 Mar 2026 21:35:39 GMT  
		Size: 94.3 KB (94276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5799ace3d1f3a380e60d9e9676ffbd335daf84ded3af9d5e1dd8ce83eee2060`  
		Last Modified: Wed, 11 Mar 2026 21:35:39 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:9c94884aa3d27f0c0ed5df500b79a6f3c2685bba5c632e3b871c0a262314d935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5858795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cd8a0886a7efaab4d69edd3b15f2a68384bcfdb1ff1a454930ba3a6a6ba29fc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Sat, 07 Mar 2026 00:33:34 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Mar 2026 00:33:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Mar 2026 00:36:49 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:36:49 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:36:49 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:36:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:36:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:36:49 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:36:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:36:49 GMT
USER memcache
# Sat, 07 Mar 2026 00:36:49 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:36:49 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f0d8799f878cf05935221d46a9b462122587e33ba748e54c983e03bbcb7ad2`  
		Last Modified: Sat, 07 Mar 2026 00:36:57 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef440db2f09493c5c9eae06dd0e59dafbd4761a74731e3ffa8ac968dcca712ca`  
		Last Modified: Sat, 07 Mar 2026 00:36:57 GMT  
		Size: 114.3 KB (114309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:134d34534319282a3e54d23ff3c63c0362a6c2ba38fb854b6a94a202d67347c2`  
		Last Modified: Sat, 07 Mar 2026 00:36:57 GMT  
		Size: 2.0 MB (2017802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:655653db981f7dce0174439408f99d0c480cb5082436a0682568bdaab190cd39`  
		Last Modified: Sat, 07 Mar 2026 00:36:57 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92dd0a7cdddba4f0415d5e0b6aa52c11369fa65b7c8c4ae965c949d55e7d52dd`  
		Last Modified: Sat, 07 Mar 2026 00:36:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:b9dd2a68695665b98af82b5110aa7af831b2d15654c26ffd200cc198ac79fb69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29c28af5a544343faaa1ff91b74bb776f4c5013c23bc2f45a2bbadb0fa1acc12`

```dockerfile
```

-	Layers:
	-	`sha256:47a88819c43763550a569259221f913c63dfd51ac45adc283170d20d81240959`  
		Last Modified: Sat, 07 Mar 2026 00:36:57 GMT  
		Size: 94.2 KB (94222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a9409046e85d857b00aa1f263c8c811160eeaa0c58b29abf61985c657289659`  
		Last Modified: Sat, 07 Mar 2026 00:36:57 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine3.23`

```console
$ docker pull memcached@sha256:1c6a2d48c5f561226f1dc54ed37132f83b4cde94b5e3f3e2d88386d028b86a27
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
$ docker pull memcached@sha256:84dd21b0c8ebc30032a8aaa7270c7e6c11da52efd7bf3c7593530168946d3bd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5959699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaf5f46bdf2c26a9dda97cd7dd2b6a05c5d8135b2f9cbacf33ff8e8365f5e1eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Sat, 07 Mar 2026 00:36:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Mar 2026 00:36:14 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Mar 2026 00:38:52 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:38:52 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:38:52 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:38:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:38:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:38:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:38:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:38:52 GMT
USER memcache
# Sat, 07 Mar 2026 00:38:52 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:38:52 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d055707374a501222192f988c0ff35fcfdc5a017dd49a48e1dd38106c605f400`  
		Last Modified: Sat, 07 Mar 2026 00:38:57 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5abb10c57422a10d35029047d7b017a29437bc0081f375524cbfb3db3c9eaf9`  
		Last Modified: Sat, 07 Mar 2026 00:38:57 GMT  
		Size: 106.1 KB (106057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4fd18d57089d5254541b428a6a2429569ff07d571c824af865b666901af275e`  
		Last Modified: Sat, 07 Mar 2026 00:38:57 GMT  
		Size: 2.0 MB (1990468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885d9eb83efad8e7a74f165d5e00bd1e547b62348f4084f8748eb5123cfd5ef2`  
		Last Modified: Sat, 07 Mar 2026 00:38:57 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32954341fb1b6227e3bb596d1a3f58beb03c348455e63c0e6a810197d1922e9`  
		Last Modified: Sat, 07 Mar 2026 00:38:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:e0615e85e00302f3ab01f14593cf39cf7e4ac01f448e6904dd61247bf63b3ff0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3b92ada03392c40180327b1e82f1b29a80b1164d4b65115558c1efc811142ad`

```dockerfile
```

-	Layers:
	-	`sha256:cc3e65e74aa6c619611c020b3d498d3c756e6168a9b26434ca30c3099cfa3261`  
		Last Modified: Sat, 07 Mar 2026 00:38:57 GMT  
		Size: 94.9 KB (94873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:327a47bce4975ea9e581754831550ac249839dc3708d4841f78ebc6cbd78d014`  
		Last Modified: Sat, 07 Mar 2026 00:38:57 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.23` - linux; arm variant v6

```console
$ docker pull memcached@sha256:6cde7ea7574023751e83c90e1e8f1f7aef03c1d5b0fbe20a17d981d57edb99dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:376e43ecede029f4d02a7634c75d3107a5797f724660eb9b02b0eb12c3e49748`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Sat, 07 Mar 2026 00:34:25 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Mar 2026 00:34:26 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Mar 2026 00:37:29 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:37:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:37:29 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:37:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:37:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:37:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:37:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:37:29 GMT
USER memcache
# Sat, 07 Mar 2026 00:37:29 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:37:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18dad4d028ff2b78314498b57b872634656cb70add272a07cde87477543ea34b`  
		Last Modified: Sat, 07 Mar 2026 00:37:33 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5343ac0baa24b86f7ffac4e0a3296276d4a7aa05b74617720244260e34dc5aba`  
		Last Modified: Sat, 07 Mar 2026 00:37:33 GMT  
		Size: 102.7 KB (102655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f65584616382b3a0c0b70214fd4046110bedf9cfbb2c2f89c2301372f8aa27`  
		Last Modified: Sat, 07 Mar 2026 00:37:33 GMT  
		Size: 1.9 MB (1940281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a378f9c04f9d21fc788013f2928b3637ad3724011b85ecb4d8fe5a61ca9bb2`  
		Last Modified: Sat, 07 Mar 2026 00:37:33 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9600d067846989777b70f754cdd61c2012197736201713e9b5ff3703b147be02`  
		Last Modified: Sat, 07 Mar 2026 00:37:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:1d36396e4f4bb90ed2d326fbc737d8ab225cf619e64f08c3ff0beaff000177ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e204629c18255bb70ea677237338842d7ed3a140e1ecbbc4b8d5727cafa1668e`

```dockerfile
```

-	Layers:
	-	`sha256:1ea1c312fb87cc4d7c73a561d98b13a1f13504625a2de3953101370977fc6745`  
		Last Modified: Sat, 07 Mar 2026 00:37:33 GMT  
		Size: 20.5 KB (20466 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.23` - linux; arm variant v7

```console
$ docker pull memcached@sha256:91fe29148d686af2a0fdc23ba01a1b272f4c6365fc45bc37d00d4687a0c41b1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5273746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a56ac817dd40669cbf75609948d0f6fc05e648f6453d8f9deba7740682f741f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Sat, 07 Mar 2026 00:37:41 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Mar 2026 00:37:42 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Mar 2026 00:40:39 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:40:39 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:40:39 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:40:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:40:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:40:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:40:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:40:39 GMT
USER memcache
# Sat, 07 Mar 2026 00:40:39 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:40:39 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a51b7877e94969180dbb0be219881bc9230f055057f9e3f4b65f1db0708689a`  
		Last Modified: Sat, 07 Mar 2026 00:40:44 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c32abf408db65abfcd3224db5db2abaa977bd3ce59942c389c73320a4051cc`  
		Last Modified: Sat, 07 Mar 2026 00:40:44 GMT  
		Size: 92.4 KB (92374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ddc29b1020998fb5a3b242cc4e45954bc53540a31017ab6a020f9dff807bd22`  
		Last Modified: Sat, 07 Mar 2026 00:40:44 GMT  
		Size: 1.9 MB (1898298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae00440f5f6fd5951552907706f8df3661315090758ede99bb2933aa3384040b`  
		Last Modified: Sat, 07 Mar 2026 00:40:44 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb70de481e3407c522658dfa65d701fde07648ab9b8c732379d8a92f44092a81`  
		Last Modified: Sat, 07 Mar 2026 00:40:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:073366e4d50888ea6d43868ab35c2a063ea12dc243105f0c614c4feaa55d0eda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c47e8e147c04b6fae9be2f9c70644395f05ac10516981d5f48aac87100f9aabf`

```dockerfile
```

-	Layers:
	-	`sha256:f128294dbb16b2300fe484115b6bd24498974e73ac8835f70a3dd5df2f3211cd`  
		Last Modified: Sat, 07 Mar 2026 00:40:44 GMT  
		Size: 94.3 KB (94291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad6c6671c716b1f4cb8882be9d7cee792a3b5a0500ba4330e4c34c83d3401a1c`  
		Last Modified: Sat, 07 Mar 2026 00:40:44 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:eeb1c0de2b6b33a7a724454aaf9fd945503a062302d133c059f1b829db991b61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6287490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0de2d8f866d91b49adb4cfa80ffd26e168ac627328864d7ceae76dfd0bc4d7a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Sat, 07 Mar 2026 00:36:34 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Mar 2026 00:36:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Mar 2026 00:39:22 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:39:22 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:39:22 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:39:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:39:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:39:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:39:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:39:22 GMT
USER memcache
# Sat, 07 Mar 2026 00:39:22 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:39:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d65cacaa69d1c76240e558dab714b69561f9bb333c2c1c147f9be7d6b29c36`  
		Last Modified: Sat, 07 Mar 2026 00:39:27 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca80346986e335b6e96f14599a1ab3629964fa8702f4570e2d199da8b04498e`  
		Last Modified: Sat, 07 Mar 2026 00:39:27 GMT  
		Size: 121.9 KB (121860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bcaaaf5541ab3a5d055204886aadf36871e66f535b6c1978b4b4c58a4dc2367`  
		Last Modified: Sat, 07 Mar 2026 00:39:27 GMT  
		Size: 2.0 MB (1967188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6167d1b1458d5cedc7774a2a1e9e621f5b32de851a6b19d82ea2275ec9f1bc5`  
		Last Modified: Sat, 07 Mar 2026 00:39:27 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2040432b455fd0270cf480396dc9c1570b8710e21539cc0110e13fe10105062`  
		Last Modified: Sat, 07 Mar 2026 00:39:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:3d8284de1f87be934ca3ad16b60f3a624262a50260f7f8db4cc80575af22e7c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9a54dfb1a405917a8fe0eaf03a1588913998eac5cacc5141cad5d053c6ba838`

```dockerfile
```

-	Layers:
	-	`sha256:8eefe1140db7c68e1990a3744cd3126838a63605758bc6825cb1c090277cf806`  
		Last Modified: Sat, 07 Mar 2026 00:39:27 GMT  
		Size: 94.3 KB (94327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92f28d8e0dd01f916858b48749b2827fadaadb7ca45a0a8a872ac9d74043589d`  
		Last Modified: Sat, 07 Mar 2026 00:39:27 GMT  
		Size: 20.7 KB (20728 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.23` - linux; 386

```console
$ docker pull memcached@sha256:006134e843d0ad5a3c64e903cc20d00c9f3e78a542fa3d6ba1e3ecec5b0ba3c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5742709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06188a4fb3481bcf32a3e44fca9d58ab763a52c65e02c95fbef5e98f4b78ee86`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Sat, 07 Mar 2026 00:37:00 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Mar 2026 00:37:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Mar 2026 00:39:49 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:39:49 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:39:49 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:39:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:39:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:39:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:39:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:39:50 GMT
USER memcache
# Sat, 07 Mar 2026 00:39:50 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:39:50 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ba4a2e327b273e788cfdef17b5c31ac5fefd6010584aa1c11b0d0104a041d6`  
		Last Modified: Sat, 07 Mar 2026 00:39:54 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ba4e8e1182330d5f76532f2f48fe38af386558e3e7fa4d94ce3dbf055be5ab`  
		Last Modified: Sat, 07 Mar 2026 00:39:54 GMT  
		Size: 110.7 KB (110732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01c1fe355d65277d08c7962b0be21d39386b4121b36381bbcb9a60d29449a5c`  
		Last Modified: Sat, 07 Mar 2026 00:39:54 GMT  
		Size: 1.9 MB (1943630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e102587e979593069cf080e59b8471ecf62f9c40abad1e62014f1742341827d0`  
		Last Modified: Sat, 07 Mar 2026 00:39:54 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46411b86935a4104c9cbb43c595a9cbf0e0330c814ca33c36935c5a9cb7f37d`  
		Last Modified: Sat, 07 Mar 2026 00:39:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:d0cb60f8d8c989514001fd52bf793673fa8f281758af2b58f8359d1d41973b11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58f3853067ae595d4075c459fe7b8361d199af21eaa1f93413e882c2e0bc9042`

```dockerfile
```

-	Layers:
	-	`sha256:2cd10df8bfae391e9a94e270083baf145ca51970a41e64ab71cd781740d00c73`  
		Last Modified: Sat, 07 Mar 2026 00:39:54 GMT  
		Size: 94.8 KB (94828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1d4f0d3116c96944777e5e4b1130eaff94973a8664033f37d3c60ceb36ed173`  
		Last Modified: Sat, 07 Mar 2026 00:39:54 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.23` - linux; ppc64le

```console
$ docker pull memcached@sha256:35c354ed5e627574c294e54f0232ed89e8eacd7ed7e2670634db2396b8f2a39c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6034990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3da727092e7c56a19e8b1a382da13658524813ce0d2bca55dee5f4067987b77a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Sat, 07 Mar 2026 00:33:31 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Mar 2026 00:33:34 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Mar 2026 00:36:15 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:36:15 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:36:15 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:36:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:36:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:36:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:36:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:36:16 GMT
USER memcache
# Sat, 07 Mar 2026 00:36:16 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:36:16 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364a7d7b961599919f81b228a22514e1935e6774971d671f38dbad14ef71cbfd`  
		Last Modified: Sat, 07 Mar 2026 00:36:29 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d77d50c27f0ae298d21083636544fb7f795b9708dc480f081e1e936f1246e7`  
		Last Modified: Sat, 07 Mar 2026 00:36:29 GMT  
		Size: 126.3 KB (126266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d559c6185e0bba610ac4ee55bed1b0d85afdad6f054f17906fadb6311cc44007`  
		Last Modified: Sat, 07 Mar 2026 00:36:29 GMT  
		Size: 2.1 MB (2077727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce553e1c7553a28f652dbbd9f3d79596edea9eecf47883032057409cd1d977f`  
		Last Modified: Sat, 07 Mar 2026 00:36:29 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf30d9d84b197d47332200b954fc9fcedf3653c9a44fe6b72a5cf721ec170f1`  
		Last Modified: Sat, 07 Mar 2026 00:36:30 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:7c60879107d9d8ce6f5e597f4c108df4a413d312eaf52e4c9303b96e80e84fbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eee93b7e24e493f45076a5a793e8b01aad30e3643bcb7583bc1fa26a1c4ff826`

```dockerfile
```

-	Layers:
	-	`sha256:b4505eef72239eda1b1c608b3226cd19dc02c372be606494a473db623050489a`  
		Last Modified: Sat, 07 Mar 2026 00:36:29 GMT  
		Size: 94.3 KB (94280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43cc72cbc203c87b12cbef8914fb2835a461df6bb0445da26d96b5a14e610184`  
		Last Modified: Sat, 07 Mar 2026 00:36:29 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.23` - linux; riscv64

```console
$ docker pull memcached@sha256:874942dd4e337f828a5480fa7e7e03b28951302101475540a14d752215e0b99e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5771014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61e6da61960009cb5e1d5f173422857994cb30b45c987fc35062485420c05ddf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 11 Mar 2026 21:21:50 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 11 Mar 2026 21:21:54 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 11 Mar 2026 21:35:15 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 11 Mar 2026 21:35:15 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 11 Mar 2026 21:35:15 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 11 Mar 2026 21:35:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 11 Mar 2026 21:35:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 11 Mar 2026 21:35:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 11 Mar 2026 21:35:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2026 21:35:16 GMT
USER memcache
# Wed, 11 Mar 2026 21:35:16 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 11 Mar 2026 21:35:16 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63b25af376cdb2cb3ddbdf009ec368c61af0677da2ff36f56052ba87ef9d03e`  
		Last Modified: Wed, 11 Mar 2026 21:35:39 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efcf2b36003649471638502666fa028dd48ae26bf7a732d6d7fe38a8432a7016`  
		Last Modified: Wed, 11 Mar 2026 21:35:39 GMT  
		Size: 108.9 KB (108902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddaf732ffb5731ec8232eec8940c917de4727564501c45fce52a7e2ebd641224`  
		Last Modified: Wed, 11 Mar 2026 21:35:40 GMT  
		Size: 2.1 MB (2075471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91cabf0fbda848cc214b782cee7c5c7224ddb7674e75de41599a3bbe85d6a689`  
		Last Modified: Wed, 11 Mar 2026 21:35:39 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:306ecccaa7e256f58e1e772b44b962766fdf35f118efb1596b4c9ae2431987ab`  
		Last Modified: Wed, 11 Mar 2026 21:35:40 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:5e6d73b60a6ccb5dda56fc4d483b45097e7ef55ce412da110e15c6c478c8d882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebcfe45486057ddd0b85095c8ca2fd1a8656b95e8ecf579e4de8717551ada915`

```dockerfile
```

-	Layers:
	-	`sha256:7176cf6ddf61d50975dee6f26ce9fdcb0b77085375b0dde58bb44b8337adca94`  
		Last Modified: Wed, 11 Mar 2026 21:35:39 GMT  
		Size: 94.3 KB (94276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5799ace3d1f3a380e60d9e9676ffbd335daf84ded3af9d5e1dd8ce83eee2060`  
		Last Modified: Wed, 11 Mar 2026 21:35:39 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.23` - linux; s390x

```console
$ docker pull memcached@sha256:9c94884aa3d27f0c0ed5df500b79a6f3c2685bba5c632e3b871c0a262314d935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5858795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cd8a0886a7efaab4d69edd3b15f2a68384bcfdb1ff1a454930ba3a6a6ba29fc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Sat, 07 Mar 2026 00:33:34 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Mar 2026 00:33:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Mar 2026 00:36:49 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:36:49 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:36:49 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:36:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:36:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:36:49 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:36:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:36:49 GMT
USER memcache
# Sat, 07 Mar 2026 00:36:49 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:36:49 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f0d8799f878cf05935221d46a9b462122587e33ba748e54c983e03bbcb7ad2`  
		Last Modified: Sat, 07 Mar 2026 00:36:57 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef440db2f09493c5c9eae06dd0e59dafbd4761a74731e3ffa8ac968dcca712ca`  
		Last Modified: Sat, 07 Mar 2026 00:36:57 GMT  
		Size: 114.3 KB (114309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:134d34534319282a3e54d23ff3c63c0362a6c2ba38fb854b6a94a202d67347c2`  
		Last Modified: Sat, 07 Mar 2026 00:36:57 GMT  
		Size: 2.0 MB (2017802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:655653db981f7dce0174439408f99d0c480cb5082436a0682568bdaab190cd39`  
		Last Modified: Sat, 07 Mar 2026 00:36:57 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92dd0a7cdddba4f0415d5e0b6aa52c11369fa65b7c8c4ae965c949d55e7d52dd`  
		Last Modified: Sat, 07 Mar 2026 00:36:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:b9dd2a68695665b98af82b5110aa7af831b2d15654c26ffd200cc198ac79fb69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29c28af5a544343faaa1ff91b74bb776f4c5013c23bc2f45a2bbadb0fa1acc12`

```dockerfile
```

-	Layers:
	-	`sha256:47a88819c43763550a569259221f913c63dfd51ac45adc283170d20d81240959`  
		Last Modified: Sat, 07 Mar 2026 00:36:57 GMT  
		Size: 94.2 KB (94222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a9409046e85d857b00aa1f263c8c811160eeaa0c58b29abf61985c657289659`  
		Last Modified: Sat, 07 Mar 2026 00:36:57 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-trixie`

```console
$ docker pull memcached@sha256:d99136ed4c1cf2e3fceb498763f2b7fedec7c486a0fe8a57be19f2a0519ce1fa
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
$ docker pull memcached@sha256:c08df224e6ccee2c893ac468902a8b68d8221910014da88f892d483b145f2e80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32197142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc0c289673d3b6f117607d5014b52d276fa02ad622404df04deac38f7a3b2b75`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Sat, 07 Mar 2026 00:34:28 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Mar 2026 00:34:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Mar 2026 00:37:16 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:37:16 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:37:16 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:37:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:37:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:37:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:37:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:37:16 GMT
USER memcache
# Sat, 07 Mar 2026 00:37:16 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:37:16 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65546826072afb14e8706d66b636911c885382731f6d325cba605469fdb363e7`  
		Last Modified: Sat, 07 Mar 2026 00:37:23 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f84d4f33fb93823aaef11588c633186a7b4c7e9c0fea6cf0c2c2e912be6b9f`  
		Last Modified: Sat, 07 Mar 2026 00:37:23 GMT  
		Size: 136.7 KB (136684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f30a00378f01ca7716c334349799965f472572c2377432ae0948fb3481a330`  
		Last Modified: Sat, 07 Mar 2026 00:37:23 GMT  
		Size: 2.3 MB (2280310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd736c12c1d448b0585c460fd3f417da3a21193665ef2aefd67c221cbd97df0b`  
		Last Modified: Sat, 07 Mar 2026 00:37:23 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f072b1e28c7bdff147ef49013b08dfe871999faec678a4219890f645e2d14b`  
		Last Modified: Sat, 07 Mar 2026 00:37:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:b0cd4839975a3f144a6d44260b40e6cebfaad48ae0dabae69c8a84a1912f55ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d69fb1b8b08633539bde084818362e1b13aae93417c6fc42c6c674e4039d2ab4`

```dockerfile
```

-	Layers:
	-	`sha256:0bc9fc51640e8d0b171e44a65462e97d0e54980aca3e0ea45f57320911a0f07c`  
		Last Modified: Sat, 07 Mar 2026 00:37:23 GMT  
		Size: 2.0 MB (2008290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2632163ed214b82be06d84daacb113b153e4ec7def67cd764cb771fb9700aeaf`  
		Last Modified: Sat, 07 Mar 2026 00:37:23 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; arm variant v5

```console
$ docker pull memcached@sha256:514cbf94b5380f36ac3c88108bf78a84ae83c3ed26e638ebe2e2f5bb88bd25ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30304774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc4d63874316ce18eaa26acb02c5e3dc129e31ea8c480a3a966621c75552572c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1771804800'
# Sat, 07 Mar 2026 00:34:25 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Mar 2026 00:34:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Mar 2026 00:37:50 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:37:50 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:37:50 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:37:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:37:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:37:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:37:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:37:50 GMT
USER memcache
# Sat, 07 Mar 2026 00:37:50 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:37:50 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:280a075cc1d2a97445b9f4430aa9774bfc38fc4217b7fc9d6a7b04e7e431cb65`  
		Last Modified: Tue, 24 Feb 2026 18:42:44 GMT  
		Size: 27.9 MB (27947608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fee55b7ab1f18dde561acdb3246640b49ed746f0a6f679b8b4be2fe96c38edc`  
		Last Modified: Sat, 07 Mar 2026 00:37:56 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e90ce24e8e18d6e22b1819e0c183af55656f28a490d2a5f5db1bb199759ae2`  
		Last Modified: Sat, 07 Mar 2026 00:37:56 GMT  
		Size: 144.2 KB (144173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e14eaa4ef07ee7a2796a97655630e5b528d0f2f8120ba62ac860fcf148e2b813`  
		Last Modified: Sat, 07 Mar 2026 00:37:56 GMT  
		Size: 2.2 MB (2211477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0271cbc419600dba0091ae986cd78ada6340afbfa697b93993e1f63555a831`  
		Last Modified: Sat, 07 Mar 2026 00:37:56 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ecc8023e8fc75e87c4b1fc32230e35e765d671345bd42f98dfe13b7118bc13`  
		Last Modified: Sat, 07 Mar 2026 00:37:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:3b41b0fb30672979494c2bcc11e11de72d662cbeef4e097e83bf3637c45aba4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b344e75a26fbd848f3d4bda6dfbc82971e7c99f16f8b8d3c2f4e0046b3e36cf`

```dockerfile
```

-	Layers:
	-	`sha256:a8abf2c9952faed7ee6a8484d94c195f2f516d28b4aa99d61fde6a938373ef14`  
		Last Modified: Sat, 07 Mar 2026 00:37:56 GMT  
		Size: 2.0 MB (2011293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4baff3ba9a329e3fdeaee0149357b33f76e181413fc6e5b4d1b9502670d8aab3`  
		Last Modified: Sat, 07 Mar 2026 00:37:56 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; arm variant v7

```console
$ docker pull memcached@sha256:5e39383d269092b745c7426583a0849917817a2861226858ff17c34f227cadc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28515640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4d89f2522b7f402debcdfe4ae5ef33ccc13694e72756aabd8c894fd1a657663`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Sat, 07 Mar 2026 00:34:26 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Mar 2026 00:34:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Mar 2026 00:37:36 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:37:36 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:37:36 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:37:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:37:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:37:37 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:37:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:37:37 GMT
USER memcache
# Sat, 07 Mar 2026 00:37:37 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:37:37 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b5f623d77fff35b334b15c7b208113b4b778a70ce39168e1270421140984e6`  
		Last Modified: Sat, 07 Mar 2026 00:37:43 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d378422d428b98928a2c392598ff24dddba86412c764099339db2c9b84dab7`  
		Last Modified: Sat, 07 Mar 2026 00:37:43 GMT  
		Size: 135.4 KB (135371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ebe7571649e14f8ae60c2aa9c7464f120d47deb28852880adc72f5958fb268`  
		Last Modified: Sat, 07 Mar 2026 00:37:43 GMT  
		Size: 2.2 MB (2165006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab8a97091ab7e05c0561d93041f6833b293ec83a81c5cd316d914c7cd4797f5`  
		Last Modified: Sat, 07 Mar 2026 00:37:43 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06917ca5c3af99a9a619b7c0077abf8521b0777d4c07464889139b6030aaa445`  
		Last Modified: Sat, 07 Mar 2026 00:37:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:17c7cd3931d1614e411d593e6027c70049d32dd6b78b4523f5e29ff13b7b1f21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b42f736130d7735ab6bde638b9206c6be06a848c316aa0776562b9d2b05634b5`

```dockerfile
```

-	Layers:
	-	`sha256:1700f9d32fecaf2a6fff6e275b9eac8036467ba4e592635351cf279712b2017b`  
		Last Modified: Sat, 07 Mar 2026 00:37:43 GMT  
		Size: 2.0 MB (2009750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef3320ccea4ba2f43dfdeb26388b30f9251a45c8b87522656d05eb856e022fa0`  
		Last Modified: Sat, 07 Mar 2026 00:37:43 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:03ff213526efc235b60a048b3efa0c67c6d697a62bdc207561fb8ee00f254f89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32557234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4742c51756a2139de24009e1c754635923a703d67706387249d261e4dc62712`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Sat, 07 Mar 2026 00:34:23 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Mar 2026 00:34:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Mar 2026 00:37:25 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:37:25 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:37:25 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:37:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:37:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:37:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:37:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:37:25 GMT
USER memcache
# Sat, 07 Mar 2026 00:37:25 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:37:25 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:461d33f62f9a4e4fbc09492d8ce59e548e8c794e3122411c5f7a8370f2bbedba`  
		Last Modified: Sat, 07 Mar 2026 00:37:31 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e642309aa5a12065d7f985c382b7658fa51b45c2a111039cdb9b7240299809e7`  
		Last Modified: Sat, 07 Mar 2026 00:37:31 GMT  
		Size: 153.5 KB (153496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c81e14adafcb230598de8ae3eaf03443a9ae10bd04e616ae4ab64a2f379a48d`  
		Last Modified: Sat, 07 Mar 2026 00:37:31 GMT  
		Size: 2.3 MB (2262125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62e12af1edbdc302c3fd82e9561c5eac5def3110b53dc9d527b277d70a0c5b0`  
		Last Modified: Sat, 07 Mar 2026 00:37:31 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eee7fdafd6f634c0431e5a06be62ff9a726cb1fa8367483d6b026fa3164c7f0`  
		Last Modified: Sat, 07 Mar 2026 00:37:32 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:f791266a2bf814187fed117fa0abd604df8d26056d2e2791b51eb537a958de3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e7b8f74c70d2427388103547caa9c90ef2b4ec4ee11ce197e642593e10f6979`

```dockerfile
```

-	Layers:
	-	`sha256:88d9544d6eb9588edcaeabdc26922a9afb53b2222e8f9972e5b4b52199893738`  
		Last Modified: Sat, 07 Mar 2026 00:37:31 GMT  
		Size: 2.0 MB (2008606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b245266f3e6e113152f086489529a68f1c8c229363d9b678823c16250c48131`  
		Last Modified: Sat, 07 Mar 2026 00:37:31 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; 386

```console
$ docker pull memcached@sha256:1219e49a37eb8fa43f5cabcda7eb69df920734c5d615f2fc63e4fba52a06dfd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33667722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d141db22d43d8c6503a206b3413976c2fd0b84654a45bb46a3da3f39594ee93e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1771804800'
# Sat, 07 Mar 2026 00:34:41 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Mar 2026 00:34:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Mar 2026 00:37:41 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:37:41 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:37:41 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:37:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:37:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:37:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:37:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:37:41 GMT
USER memcache
# Sat, 07 Mar 2026 00:37:41 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:37:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f4e0b944ee1e7e50bdfbfa77bda370b6eccee7d698a7adca78c38f5ca0767ca5`  
		Last Modified: Tue, 24 Feb 2026 18:43:18 GMT  
		Size: 31.3 MB (31293918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d38eff546890db9ae0646486b61a548d8067820adc96ceb6eb4f5d7c2206bb8`  
		Last Modified: Sat, 07 Mar 2026 00:37:47 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c454125cf8ccd03f95714478c13c1d671ba0807b980ee5e6df450d611f61e156`  
		Last Modified: Sat, 07 Mar 2026 00:37:47 GMT  
		Size: 147.5 KB (147517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42b7d17f494cc1acab1da36a724a41a46ecf955d058123b89b170ea63bafda97`  
		Last Modified: Sat, 07 Mar 2026 00:37:47 GMT  
		Size: 2.2 MB (2224772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56fcaee4e2b815384392953fdf84278be4b9a4b116e3a5ad6436f7b13a7c6d9`  
		Last Modified: Sat, 07 Mar 2026 00:37:47 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6adacd7f3e38f46b44efa4ff006b35719382afa26b95b7a9b0c62ef7e7a01bfc`  
		Last Modified: Sat, 07 Mar 2026 00:37:48 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:9f65574f3294736b3dc217e4b07a4045282c517d258eaa96a32035e09cda6fa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb96fc147195e16ed2b6e99c3582cd8c6a67516fb0387c563d09fbf85f6a4dc0`

```dockerfile
```

-	Layers:
	-	`sha256:cdc74dec8f482313433fa0011e8531a8e816610bf31af8b63d2203318e8a59f9`  
		Last Modified: Sat, 07 Mar 2026 00:37:47 GMT  
		Size: 2.0 MB (2005447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bbcbbf7d1935fe3e711cd689ff38f789c3f7334bff2fd2518c106c4bf5d805f`  
		Last Modified: Sat, 07 Mar 2026 00:37:47 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; ppc64le

```console
$ docker pull memcached@sha256:ffac94778c7c882a7f2cbaae5af33e755639de207d07834e052412c2b22a24b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36754462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5640d71fb49b8eaef07631709a9f4924bd191fcfe9b44b7df2d525e247075b64`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Sat, 07 Mar 2026 00:33:31 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Mar 2026 00:33:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Mar 2026 00:56:42 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:56:42 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:56:42 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:56:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:56:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:56:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:56:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:56:44 GMT
USER memcache
# Sat, 07 Mar 2026 00:56:44 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:56:44 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab70996aa4a561e7f3e1f1e1b14df7912a1456b20b317937391cfa826c93f2ea`  
		Last Modified: Sat, 07 Mar 2026 00:57:10 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1ba00921effa53d91205ba3e5e3280c719885f49b5e9e0f8e2a387cf316d89`  
		Last Modified: Sat, 07 Mar 2026 00:57:10 GMT  
		Size: 170.4 KB (170386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd00738358190677470eca91b6732f6fcc475639b7f07f1943af6f5d268ae47`  
		Last Modified: Sat, 07 Mar 2026 00:57:10 GMT  
		Size: 3.0 MB (2982343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f7dc97a8f5d8c677e24bd2f8014c3e315619d726d409033dc3ce4f6d7d7569d`  
		Last Modified: Sat, 07 Mar 2026 00:57:10 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f2b48241128f09e1c613b0fb34d37f79c77417d033b7a00041f8cd08d6241f`  
		Last Modified: Sat, 07 Mar 2026 00:57:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:da557c745e92be8dd35823b9c24b79e47c55ff727768980abe9b659a14672408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e89b8bba62432d49e11baad935eddf449853276e5bb492953ae6bb995bf81ef`

```dockerfile
```

-	Layers:
	-	`sha256:7bf94ead3bca06412117cdc5395bde9d799ffc799dd28be779209634f64bfc0b`  
		Last Modified: Sat, 07 Mar 2026 00:57:10 GMT  
		Size: 2.0 MB (2011891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ec351466954789ecb039e735ecf9fd0235d5d4cfcf8bd6bcf2cf68049016c1c`  
		Last Modified: Sat, 07 Mar 2026 00:57:10 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; riscv64

```console
$ docker pull memcached@sha256:ccac0e143b4efd5bd15fb67df5ad87f5b743cc3db826cbb27d1874cbb3b6d549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30619564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f9320af1aa6fbbae22f81ef28d68694abc001739c71a195b4b1cd490b3b9107`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 23:50:36 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 09 Mar 2026 23:51:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Mar 2026 00:09:03 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 10 Mar 2026 00:09:03 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 10 Mar 2026 00:09:03 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 10 Mar 2026 00:09:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 10 Mar 2026 00:09:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 10 Mar 2026 00:09:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 10 Mar 2026 00:09:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Mar 2026 00:09:03 GMT
USER memcache
# Tue, 10 Mar 2026 00:09:03 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 10 Mar 2026 00:09:03 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e1366b1f74881f04901f31cfdecf9f3f5d4794ebf89911083a239bf462bf21`  
		Last Modified: Tue, 10 Mar 2026 00:09:56 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918782f8ab4ae7fe2ab9f1fc0aa7ad4e48d83dc362a4dcac336048ded3de9b6e`  
		Last Modified: Tue, 10 Mar 2026 00:09:56 GMT  
		Size: 133.1 KB (133079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963fbe1d00657987e81bdc270499ad5aacf8f91b100915c30ddf9fc57cd67346`  
		Last Modified: Tue, 10 Mar 2026 00:09:56 GMT  
		Size: 2.2 MB (2208551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729657786193241c665df2cbaeb72b5d157865abb3bbd8b9460e88d08fb65fea`  
		Last Modified: Tue, 10 Mar 2026 00:09:56 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8246f12fbc1ee94790a418b9655df55d80968171273b5994aaffa40c04fa2f3c`  
		Last Modified: Tue, 10 Mar 2026 00:09:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:de9f0d80a354763898649af4229a6f696fb51689e3b577af2e1d918d365777e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d72c30b80e1c2deaee38b267b52cab1a28e245b2a3608fcf459f2232dad3faa7`

```dockerfile
```

-	Layers:
	-	`sha256:03d9f11a7e8cf93ffe1f13ecfd86632a66af5a6efc142ae7a4ecac0c19418b2d`  
		Last Modified: Tue, 10 Mar 2026 00:09:56 GMT  
		Size: 2.0 MB (2002254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:452e3f764b5054c447aa8e63046155a20784d6f10159282ce633afdb79bf9279`  
		Last Modified: Tue, 10 Mar 2026 00:09:56 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; s390x

```console
$ docker pull memcached@sha256:8e1f3fb07bf1702ad27a7e2a6b2364e61d7b5165c113d0202db31adaa90d91df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32278340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1088ed36ed575f78d3e06fdd24f1ccdcc908d6e579970b2cae128c29f8d6e7a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Sat, 07 Mar 2026 00:33:32 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Mar 2026 00:33:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Mar 2026 00:36:51 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:36:51 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:36:51 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:36:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:36:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:36:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:36:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:36:51 GMT
USER memcache
# Sat, 07 Mar 2026 00:36:51 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:36:51 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986cc162f1a9b2f1b4c673da47497d87b8a542990f29c7823ee4d64cd160ea34`  
		Last Modified: Sat, 07 Mar 2026 00:37:00 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e3b516d24d039487b70f5d718d6f2b0c5473b5da4e6b82815239c7730587d6`  
		Last Modified: Sat, 07 Mar 2026 00:37:00 GMT  
		Size: 140.5 KB (140520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb611bdb547903f4763e52741be4c28e6ed0f172ebffc4ddae4e56a1a4d3ebc2`  
		Last Modified: Sat, 07 Mar 2026 00:37:00 GMT  
		Size: 2.3 MB (2298126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b32c7b8a27f2284141ba22bde8036a295b3e0d397cde405054e47e550cced01`  
		Last Modified: Sat, 07 Mar 2026 00:37:00 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3240387a49966ed4c1475913af7c7648c5499d01045e56e16637a760300918a`  
		Last Modified: Sat, 07 Mar 2026 00:37:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:b725149e071a1d02723f7674a5f7c477144350f79f2243558bce2360da7bf73b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:628ead940c50f3d4776c150c412d2270c2238893cfd1a57f8c17647ec35223e2`

```dockerfile
```

-	Layers:
	-	`sha256:b118af94ed9d10ab8f0c0221725860a15ff82dce98bd35abb240f411b745e0f7`  
		Last Modified: Sat, 07 Mar 2026 00:37:00 GMT  
		Size: 2.0 MB (2009727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:737fa51b5113fe89d161d6b7d0d81d66c28e666617dc1fb7c410b093ecf35625`  
		Last Modified: Sat, 07 Mar 2026 00:37:00 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.41`

```console
$ docker pull memcached@sha256:d99136ed4c1cf2e3fceb498763f2b7fedec7c486a0fe8a57be19f2a0519ce1fa
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
$ docker pull memcached@sha256:c08df224e6ccee2c893ac468902a8b68d8221910014da88f892d483b145f2e80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32197142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc0c289673d3b6f117607d5014b52d276fa02ad622404df04deac38f7a3b2b75`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Sat, 07 Mar 2026 00:34:28 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Mar 2026 00:34:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Mar 2026 00:37:16 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:37:16 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:37:16 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:37:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:37:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:37:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:37:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:37:16 GMT
USER memcache
# Sat, 07 Mar 2026 00:37:16 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:37:16 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65546826072afb14e8706d66b636911c885382731f6d325cba605469fdb363e7`  
		Last Modified: Sat, 07 Mar 2026 00:37:23 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f84d4f33fb93823aaef11588c633186a7b4c7e9c0fea6cf0c2c2e912be6b9f`  
		Last Modified: Sat, 07 Mar 2026 00:37:23 GMT  
		Size: 136.7 KB (136684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f30a00378f01ca7716c334349799965f472572c2377432ae0948fb3481a330`  
		Last Modified: Sat, 07 Mar 2026 00:37:23 GMT  
		Size: 2.3 MB (2280310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd736c12c1d448b0585c460fd3f417da3a21193665ef2aefd67c221cbd97df0b`  
		Last Modified: Sat, 07 Mar 2026 00:37:23 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f072b1e28c7bdff147ef49013b08dfe871999faec678a4219890f645e2d14b`  
		Last Modified: Sat, 07 Mar 2026 00:37:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41` - unknown; unknown

```console
$ docker pull memcached@sha256:b0cd4839975a3f144a6d44260b40e6cebfaad48ae0dabae69c8a84a1912f55ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d69fb1b8b08633539bde084818362e1b13aae93417c6fc42c6c674e4039d2ab4`

```dockerfile
```

-	Layers:
	-	`sha256:0bc9fc51640e8d0b171e44a65462e97d0e54980aca3e0ea45f57320911a0f07c`  
		Last Modified: Sat, 07 Mar 2026 00:37:23 GMT  
		Size: 2.0 MB (2008290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2632163ed214b82be06d84daacb113b153e4ec7def67cd764cb771fb9700aeaf`  
		Last Modified: Sat, 07 Mar 2026 00:37:23 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41` - linux; arm variant v5

```console
$ docker pull memcached@sha256:514cbf94b5380f36ac3c88108bf78a84ae83c3ed26e638ebe2e2f5bb88bd25ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30304774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc4d63874316ce18eaa26acb02c5e3dc129e31ea8c480a3a966621c75552572c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1771804800'
# Sat, 07 Mar 2026 00:34:25 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Mar 2026 00:34:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Mar 2026 00:37:50 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:37:50 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:37:50 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:37:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:37:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:37:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:37:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:37:50 GMT
USER memcache
# Sat, 07 Mar 2026 00:37:50 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:37:50 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:280a075cc1d2a97445b9f4430aa9774bfc38fc4217b7fc9d6a7b04e7e431cb65`  
		Last Modified: Tue, 24 Feb 2026 18:42:44 GMT  
		Size: 27.9 MB (27947608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fee55b7ab1f18dde561acdb3246640b49ed746f0a6f679b8b4be2fe96c38edc`  
		Last Modified: Sat, 07 Mar 2026 00:37:56 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e90ce24e8e18d6e22b1819e0c183af55656f28a490d2a5f5db1bb199759ae2`  
		Last Modified: Sat, 07 Mar 2026 00:37:56 GMT  
		Size: 144.2 KB (144173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e14eaa4ef07ee7a2796a97655630e5b528d0f2f8120ba62ac860fcf148e2b813`  
		Last Modified: Sat, 07 Mar 2026 00:37:56 GMT  
		Size: 2.2 MB (2211477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0271cbc419600dba0091ae986cd78ada6340afbfa697b93993e1f63555a831`  
		Last Modified: Sat, 07 Mar 2026 00:37:56 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ecc8023e8fc75e87c4b1fc32230e35e765d671345bd42f98dfe13b7118bc13`  
		Last Modified: Sat, 07 Mar 2026 00:37:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41` - unknown; unknown

```console
$ docker pull memcached@sha256:3b41b0fb30672979494c2bcc11e11de72d662cbeef4e097e83bf3637c45aba4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b344e75a26fbd848f3d4bda6dfbc82971e7c99f16f8b8d3c2f4e0046b3e36cf`

```dockerfile
```

-	Layers:
	-	`sha256:a8abf2c9952faed7ee6a8484d94c195f2f516d28b4aa99d61fde6a938373ef14`  
		Last Modified: Sat, 07 Mar 2026 00:37:56 GMT  
		Size: 2.0 MB (2011293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4baff3ba9a329e3fdeaee0149357b33f76e181413fc6e5b4d1b9502670d8aab3`  
		Last Modified: Sat, 07 Mar 2026 00:37:56 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41` - linux; arm variant v7

```console
$ docker pull memcached@sha256:5e39383d269092b745c7426583a0849917817a2861226858ff17c34f227cadc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28515640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4d89f2522b7f402debcdfe4ae5ef33ccc13694e72756aabd8c894fd1a657663`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Sat, 07 Mar 2026 00:34:26 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Mar 2026 00:34:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Mar 2026 00:37:36 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:37:36 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:37:36 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:37:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:37:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:37:37 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:37:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:37:37 GMT
USER memcache
# Sat, 07 Mar 2026 00:37:37 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:37:37 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b5f623d77fff35b334b15c7b208113b4b778a70ce39168e1270421140984e6`  
		Last Modified: Sat, 07 Mar 2026 00:37:43 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d378422d428b98928a2c392598ff24dddba86412c764099339db2c9b84dab7`  
		Last Modified: Sat, 07 Mar 2026 00:37:43 GMT  
		Size: 135.4 KB (135371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ebe7571649e14f8ae60c2aa9c7464f120d47deb28852880adc72f5958fb268`  
		Last Modified: Sat, 07 Mar 2026 00:37:43 GMT  
		Size: 2.2 MB (2165006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab8a97091ab7e05c0561d93041f6833b293ec83a81c5cd316d914c7cd4797f5`  
		Last Modified: Sat, 07 Mar 2026 00:37:43 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06917ca5c3af99a9a619b7c0077abf8521b0777d4c07464889139b6030aaa445`  
		Last Modified: Sat, 07 Mar 2026 00:37:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41` - unknown; unknown

```console
$ docker pull memcached@sha256:17c7cd3931d1614e411d593e6027c70049d32dd6b78b4523f5e29ff13b7b1f21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b42f736130d7735ab6bde638b9206c6be06a848c316aa0776562b9d2b05634b5`

```dockerfile
```

-	Layers:
	-	`sha256:1700f9d32fecaf2a6fff6e275b9eac8036467ba4e592635351cf279712b2017b`  
		Last Modified: Sat, 07 Mar 2026 00:37:43 GMT  
		Size: 2.0 MB (2009750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef3320ccea4ba2f43dfdeb26388b30f9251a45c8b87522656d05eb856e022fa0`  
		Last Modified: Sat, 07 Mar 2026 00:37:43 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:03ff213526efc235b60a048b3efa0c67c6d697a62bdc207561fb8ee00f254f89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32557234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4742c51756a2139de24009e1c754635923a703d67706387249d261e4dc62712`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Sat, 07 Mar 2026 00:34:23 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Mar 2026 00:34:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Mar 2026 00:37:25 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:37:25 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:37:25 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:37:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:37:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:37:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:37:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:37:25 GMT
USER memcache
# Sat, 07 Mar 2026 00:37:25 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:37:25 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:461d33f62f9a4e4fbc09492d8ce59e548e8c794e3122411c5f7a8370f2bbedba`  
		Last Modified: Sat, 07 Mar 2026 00:37:31 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e642309aa5a12065d7f985c382b7658fa51b45c2a111039cdb9b7240299809e7`  
		Last Modified: Sat, 07 Mar 2026 00:37:31 GMT  
		Size: 153.5 KB (153496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c81e14adafcb230598de8ae3eaf03443a9ae10bd04e616ae4ab64a2f379a48d`  
		Last Modified: Sat, 07 Mar 2026 00:37:31 GMT  
		Size: 2.3 MB (2262125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62e12af1edbdc302c3fd82e9561c5eac5def3110b53dc9d527b277d70a0c5b0`  
		Last Modified: Sat, 07 Mar 2026 00:37:31 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eee7fdafd6f634c0431e5a06be62ff9a726cb1fa8367483d6b026fa3164c7f0`  
		Last Modified: Sat, 07 Mar 2026 00:37:32 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41` - unknown; unknown

```console
$ docker pull memcached@sha256:f791266a2bf814187fed117fa0abd604df8d26056d2e2791b51eb537a958de3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e7b8f74c70d2427388103547caa9c90ef2b4ec4ee11ce197e642593e10f6979`

```dockerfile
```

-	Layers:
	-	`sha256:88d9544d6eb9588edcaeabdc26922a9afb53b2222e8f9972e5b4b52199893738`  
		Last Modified: Sat, 07 Mar 2026 00:37:31 GMT  
		Size: 2.0 MB (2008606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b245266f3e6e113152f086489529a68f1c8c229363d9b678823c16250c48131`  
		Last Modified: Sat, 07 Mar 2026 00:37:31 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41` - linux; 386

```console
$ docker pull memcached@sha256:1219e49a37eb8fa43f5cabcda7eb69df920734c5d615f2fc63e4fba52a06dfd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33667722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d141db22d43d8c6503a206b3413976c2fd0b84654a45bb46a3da3f39594ee93e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1771804800'
# Sat, 07 Mar 2026 00:34:41 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Mar 2026 00:34:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Mar 2026 00:37:41 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:37:41 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:37:41 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:37:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:37:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:37:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:37:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:37:41 GMT
USER memcache
# Sat, 07 Mar 2026 00:37:41 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:37:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f4e0b944ee1e7e50bdfbfa77bda370b6eccee7d698a7adca78c38f5ca0767ca5`  
		Last Modified: Tue, 24 Feb 2026 18:43:18 GMT  
		Size: 31.3 MB (31293918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d38eff546890db9ae0646486b61a548d8067820adc96ceb6eb4f5d7c2206bb8`  
		Last Modified: Sat, 07 Mar 2026 00:37:47 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c454125cf8ccd03f95714478c13c1d671ba0807b980ee5e6df450d611f61e156`  
		Last Modified: Sat, 07 Mar 2026 00:37:47 GMT  
		Size: 147.5 KB (147517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42b7d17f494cc1acab1da36a724a41a46ecf955d058123b89b170ea63bafda97`  
		Last Modified: Sat, 07 Mar 2026 00:37:47 GMT  
		Size: 2.2 MB (2224772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56fcaee4e2b815384392953fdf84278be4b9a4b116e3a5ad6436f7b13a7c6d9`  
		Last Modified: Sat, 07 Mar 2026 00:37:47 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6adacd7f3e38f46b44efa4ff006b35719382afa26b95b7a9b0c62ef7e7a01bfc`  
		Last Modified: Sat, 07 Mar 2026 00:37:48 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41` - unknown; unknown

```console
$ docker pull memcached@sha256:9f65574f3294736b3dc217e4b07a4045282c517d258eaa96a32035e09cda6fa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb96fc147195e16ed2b6e99c3582cd8c6a67516fb0387c563d09fbf85f6a4dc0`

```dockerfile
```

-	Layers:
	-	`sha256:cdc74dec8f482313433fa0011e8531a8e816610bf31af8b63d2203318e8a59f9`  
		Last Modified: Sat, 07 Mar 2026 00:37:47 GMT  
		Size: 2.0 MB (2005447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bbcbbf7d1935fe3e711cd689ff38f789c3f7334bff2fd2518c106c4bf5d805f`  
		Last Modified: Sat, 07 Mar 2026 00:37:47 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41` - linux; ppc64le

```console
$ docker pull memcached@sha256:ffac94778c7c882a7f2cbaae5af33e755639de207d07834e052412c2b22a24b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36754462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5640d71fb49b8eaef07631709a9f4924bd191fcfe9b44b7df2d525e247075b64`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Sat, 07 Mar 2026 00:33:31 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Mar 2026 00:33:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Mar 2026 00:56:42 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:56:42 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:56:42 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:56:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:56:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:56:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:56:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:56:44 GMT
USER memcache
# Sat, 07 Mar 2026 00:56:44 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:56:44 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab70996aa4a561e7f3e1f1e1b14df7912a1456b20b317937391cfa826c93f2ea`  
		Last Modified: Sat, 07 Mar 2026 00:57:10 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1ba00921effa53d91205ba3e5e3280c719885f49b5e9e0f8e2a387cf316d89`  
		Last Modified: Sat, 07 Mar 2026 00:57:10 GMT  
		Size: 170.4 KB (170386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd00738358190677470eca91b6732f6fcc475639b7f07f1943af6f5d268ae47`  
		Last Modified: Sat, 07 Mar 2026 00:57:10 GMT  
		Size: 3.0 MB (2982343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f7dc97a8f5d8c677e24bd2f8014c3e315619d726d409033dc3ce4f6d7d7569d`  
		Last Modified: Sat, 07 Mar 2026 00:57:10 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f2b48241128f09e1c613b0fb34d37f79c77417d033b7a00041f8cd08d6241f`  
		Last Modified: Sat, 07 Mar 2026 00:57:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41` - unknown; unknown

```console
$ docker pull memcached@sha256:da557c745e92be8dd35823b9c24b79e47c55ff727768980abe9b659a14672408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e89b8bba62432d49e11baad935eddf449853276e5bb492953ae6bb995bf81ef`

```dockerfile
```

-	Layers:
	-	`sha256:7bf94ead3bca06412117cdc5395bde9d799ffc799dd28be779209634f64bfc0b`  
		Last Modified: Sat, 07 Mar 2026 00:57:10 GMT  
		Size: 2.0 MB (2011891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ec351466954789ecb039e735ecf9fd0235d5d4cfcf8bd6bcf2cf68049016c1c`  
		Last Modified: Sat, 07 Mar 2026 00:57:10 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41` - linux; riscv64

```console
$ docker pull memcached@sha256:ccac0e143b4efd5bd15fb67df5ad87f5b743cc3db826cbb27d1874cbb3b6d549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30619564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f9320af1aa6fbbae22f81ef28d68694abc001739c71a195b4b1cd490b3b9107`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 23:50:36 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 09 Mar 2026 23:51:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Mar 2026 00:09:03 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 10 Mar 2026 00:09:03 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 10 Mar 2026 00:09:03 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 10 Mar 2026 00:09:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 10 Mar 2026 00:09:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 10 Mar 2026 00:09:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 10 Mar 2026 00:09:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Mar 2026 00:09:03 GMT
USER memcache
# Tue, 10 Mar 2026 00:09:03 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 10 Mar 2026 00:09:03 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e1366b1f74881f04901f31cfdecf9f3f5d4794ebf89911083a239bf462bf21`  
		Last Modified: Tue, 10 Mar 2026 00:09:56 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918782f8ab4ae7fe2ab9f1fc0aa7ad4e48d83dc362a4dcac336048ded3de9b6e`  
		Last Modified: Tue, 10 Mar 2026 00:09:56 GMT  
		Size: 133.1 KB (133079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963fbe1d00657987e81bdc270499ad5aacf8f91b100915c30ddf9fc57cd67346`  
		Last Modified: Tue, 10 Mar 2026 00:09:56 GMT  
		Size: 2.2 MB (2208551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729657786193241c665df2cbaeb72b5d157865abb3bbd8b9460e88d08fb65fea`  
		Last Modified: Tue, 10 Mar 2026 00:09:56 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8246f12fbc1ee94790a418b9655df55d80968171273b5994aaffa40c04fa2f3c`  
		Last Modified: Tue, 10 Mar 2026 00:09:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41` - unknown; unknown

```console
$ docker pull memcached@sha256:de9f0d80a354763898649af4229a6f696fb51689e3b577af2e1d918d365777e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d72c30b80e1c2deaee38b267b52cab1a28e245b2a3608fcf459f2232dad3faa7`

```dockerfile
```

-	Layers:
	-	`sha256:03d9f11a7e8cf93ffe1f13ecfd86632a66af5a6efc142ae7a4ecac0c19418b2d`  
		Last Modified: Tue, 10 Mar 2026 00:09:56 GMT  
		Size: 2.0 MB (2002254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:452e3f764b5054c447aa8e63046155a20784d6f10159282ce633afdb79bf9279`  
		Last Modified: Tue, 10 Mar 2026 00:09:56 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41` - linux; s390x

```console
$ docker pull memcached@sha256:8e1f3fb07bf1702ad27a7e2a6b2364e61d7b5165c113d0202db31adaa90d91df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32278340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1088ed36ed575f78d3e06fdd24f1ccdcc908d6e579970b2cae128c29f8d6e7a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Sat, 07 Mar 2026 00:33:32 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Mar 2026 00:33:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Mar 2026 00:36:51 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:36:51 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:36:51 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:36:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:36:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:36:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:36:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:36:51 GMT
USER memcache
# Sat, 07 Mar 2026 00:36:51 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:36:51 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986cc162f1a9b2f1b4c673da47497d87b8a542990f29c7823ee4d64cd160ea34`  
		Last Modified: Sat, 07 Mar 2026 00:37:00 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e3b516d24d039487b70f5d718d6f2b0c5473b5da4e6b82815239c7730587d6`  
		Last Modified: Sat, 07 Mar 2026 00:37:00 GMT  
		Size: 140.5 KB (140520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb611bdb547903f4763e52741be4c28e6ed0f172ebffc4ddae4e56a1a4d3ebc2`  
		Last Modified: Sat, 07 Mar 2026 00:37:00 GMT  
		Size: 2.3 MB (2298126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b32c7b8a27f2284141ba22bde8036a295b3e0d397cde405054e47e550cced01`  
		Last Modified: Sat, 07 Mar 2026 00:37:00 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3240387a49966ed4c1475913af7c7648c5499d01045e56e16637a760300918a`  
		Last Modified: Sat, 07 Mar 2026 00:37:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41` - unknown; unknown

```console
$ docker pull memcached@sha256:b725149e071a1d02723f7674a5f7c477144350f79f2243558bce2360da7bf73b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:628ead940c50f3d4776c150c412d2270c2238893cfd1a57f8c17647ec35223e2`

```dockerfile
```

-	Layers:
	-	`sha256:b118af94ed9d10ab8f0c0221725860a15ff82dce98bd35abb240f411b745e0f7`  
		Last Modified: Sat, 07 Mar 2026 00:37:00 GMT  
		Size: 2.0 MB (2009727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:737fa51b5113fe89d161d6b7d0d81d66c28e666617dc1fb7c410b093ecf35625`  
		Last Modified: Sat, 07 Mar 2026 00:37:00 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.41-alpine`

```console
$ docker pull memcached@sha256:1c6a2d48c5f561226f1dc54ed37132f83b4cde94b5e3f3e2d88386d028b86a27
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
$ docker pull memcached@sha256:84dd21b0c8ebc30032a8aaa7270c7e6c11da52efd7bf3c7593530168946d3bd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5959699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaf5f46bdf2c26a9dda97cd7dd2b6a05c5d8135b2f9cbacf33ff8e8365f5e1eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Sat, 07 Mar 2026 00:36:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Mar 2026 00:36:14 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Mar 2026 00:38:52 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:38:52 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:38:52 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:38:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:38:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:38:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:38:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:38:52 GMT
USER memcache
# Sat, 07 Mar 2026 00:38:52 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:38:52 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d055707374a501222192f988c0ff35fcfdc5a017dd49a48e1dd38106c605f400`  
		Last Modified: Sat, 07 Mar 2026 00:38:57 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5abb10c57422a10d35029047d7b017a29437bc0081f375524cbfb3db3c9eaf9`  
		Last Modified: Sat, 07 Mar 2026 00:38:57 GMT  
		Size: 106.1 KB (106057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4fd18d57089d5254541b428a6a2429569ff07d571c824af865b666901af275e`  
		Last Modified: Sat, 07 Mar 2026 00:38:57 GMT  
		Size: 2.0 MB (1990468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885d9eb83efad8e7a74f165d5e00bd1e547b62348f4084f8748eb5123cfd5ef2`  
		Last Modified: Sat, 07 Mar 2026 00:38:57 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32954341fb1b6227e3bb596d1a3f58beb03c348455e63c0e6a810197d1922e9`  
		Last Modified: Sat, 07 Mar 2026 00:38:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:e0615e85e00302f3ab01f14593cf39cf7e4ac01f448e6904dd61247bf63b3ff0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3b92ada03392c40180327b1e82f1b29a80b1164d4b65115558c1efc811142ad`

```dockerfile
```

-	Layers:
	-	`sha256:cc3e65e74aa6c619611c020b3d498d3c756e6168a9b26434ca30c3099cfa3261`  
		Last Modified: Sat, 07 Mar 2026 00:38:57 GMT  
		Size: 94.9 KB (94873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:327a47bce4975ea9e581754831550ac249839dc3708d4841f78ebc6cbd78d014`  
		Last Modified: Sat, 07 Mar 2026 00:38:57 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:6cde7ea7574023751e83c90e1e8f1f7aef03c1d5b0fbe20a17d981d57edb99dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:376e43ecede029f4d02a7634c75d3107a5797f724660eb9b02b0eb12c3e49748`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Sat, 07 Mar 2026 00:34:25 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Mar 2026 00:34:26 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Mar 2026 00:37:29 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:37:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:37:29 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:37:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:37:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:37:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:37:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:37:29 GMT
USER memcache
# Sat, 07 Mar 2026 00:37:29 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:37:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18dad4d028ff2b78314498b57b872634656cb70add272a07cde87477543ea34b`  
		Last Modified: Sat, 07 Mar 2026 00:37:33 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5343ac0baa24b86f7ffac4e0a3296276d4a7aa05b74617720244260e34dc5aba`  
		Last Modified: Sat, 07 Mar 2026 00:37:33 GMT  
		Size: 102.7 KB (102655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f65584616382b3a0c0b70214fd4046110bedf9cfbb2c2f89c2301372f8aa27`  
		Last Modified: Sat, 07 Mar 2026 00:37:33 GMT  
		Size: 1.9 MB (1940281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a378f9c04f9d21fc788013f2928b3637ad3724011b85ecb4d8fe5a61ca9bb2`  
		Last Modified: Sat, 07 Mar 2026 00:37:33 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9600d067846989777b70f754cdd61c2012197736201713e9b5ff3703b147be02`  
		Last Modified: Sat, 07 Mar 2026 00:37:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:1d36396e4f4bb90ed2d326fbc737d8ab225cf619e64f08c3ff0beaff000177ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e204629c18255bb70ea677237338842d7ed3a140e1ecbbc4b8d5727cafa1668e`

```dockerfile
```

-	Layers:
	-	`sha256:1ea1c312fb87cc4d7c73a561d98b13a1f13504625a2de3953101370977fc6745`  
		Last Modified: Sat, 07 Mar 2026 00:37:33 GMT  
		Size: 20.5 KB (20466 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:91fe29148d686af2a0fdc23ba01a1b272f4c6365fc45bc37d00d4687a0c41b1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5273746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a56ac817dd40669cbf75609948d0f6fc05e648f6453d8f9deba7740682f741f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Sat, 07 Mar 2026 00:37:41 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Mar 2026 00:37:42 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Mar 2026 00:40:39 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:40:39 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:40:39 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:40:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:40:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:40:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:40:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:40:39 GMT
USER memcache
# Sat, 07 Mar 2026 00:40:39 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:40:39 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a51b7877e94969180dbb0be219881bc9230f055057f9e3f4b65f1db0708689a`  
		Last Modified: Sat, 07 Mar 2026 00:40:44 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c32abf408db65abfcd3224db5db2abaa977bd3ce59942c389c73320a4051cc`  
		Last Modified: Sat, 07 Mar 2026 00:40:44 GMT  
		Size: 92.4 KB (92374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ddc29b1020998fb5a3b242cc4e45954bc53540a31017ab6a020f9dff807bd22`  
		Last Modified: Sat, 07 Mar 2026 00:40:44 GMT  
		Size: 1.9 MB (1898298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae00440f5f6fd5951552907706f8df3661315090758ede99bb2933aa3384040b`  
		Last Modified: Sat, 07 Mar 2026 00:40:44 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb70de481e3407c522658dfa65d701fde07648ab9b8c732379d8a92f44092a81`  
		Last Modified: Sat, 07 Mar 2026 00:40:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:073366e4d50888ea6d43868ab35c2a063ea12dc243105f0c614c4feaa55d0eda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c47e8e147c04b6fae9be2f9c70644395f05ac10516981d5f48aac87100f9aabf`

```dockerfile
```

-	Layers:
	-	`sha256:f128294dbb16b2300fe484115b6bd24498974e73ac8835f70a3dd5df2f3211cd`  
		Last Modified: Sat, 07 Mar 2026 00:40:44 GMT  
		Size: 94.3 KB (94291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad6c6671c716b1f4cb8882be9d7cee792a3b5a0500ba4330e4c34c83d3401a1c`  
		Last Modified: Sat, 07 Mar 2026 00:40:44 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:eeb1c0de2b6b33a7a724454aaf9fd945503a062302d133c059f1b829db991b61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6287490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0de2d8f866d91b49adb4cfa80ffd26e168ac627328864d7ceae76dfd0bc4d7a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Sat, 07 Mar 2026 00:36:34 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Mar 2026 00:36:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Mar 2026 00:39:22 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:39:22 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:39:22 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:39:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:39:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:39:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:39:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:39:22 GMT
USER memcache
# Sat, 07 Mar 2026 00:39:22 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:39:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d65cacaa69d1c76240e558dab714b69561f9bb333c2c1c147f9be7d6b29c36`  
		Last Modified: Sat, 07 Mar 2026 00:39:27 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca80346986e335b6e96f14599a1ab3629964fa8702f4570e2d199da8b04498e`  
		Last Modified: Sat, 07 Mar 2026 00:39:27 GMT  
		Size: 121.9 KB (121860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bcaaaf5541ab3a5d055204886aadf36871e66f535b6c1978b4b4c58a4dc2367`  
		Last Modified: Sat, 07 Mar 2026 00:39:27 GMT  
		Size: 2.0 MB (1967188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6167d1b1458d5cedc7774a2a1e9e621f5b32de851a6b19d82ea2275ec9f1bc5`  
		Last Modified: Sat, 07 Mar 2026 00:39:27 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2040432b455fd0270cf480396dc9c1570b8710e21539cc0110e13fe10105062`  
		Last Modified: Sat, 07 Mar 2026 00:39:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:3d8284de1f87be934ca3ad16b60f3a624262a50260f7f8db4cc80575af22e7c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9a54dfb1a405917a8fe0eaf03a1588913998eac5cacc5141cad5d053c6ba838`

```dockerfile
```

-	Layers:
	-	`sha256:8eefe1140db7c68e1990a3744cd3126838a63605758bc6825cb1c090277cf806`  
		Last Modified: Sat, 07 Mar 2026 00:39:27 GMT  
		Size: 94.3 KB (94327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92f28d8e0dd01f916858b48749b2827fadaadb7ca45a0a8a872ac9d74043589d`  
		Last Modified: Sat, 07 Mar 2026 00:39:27 GMT  
		Size: 20.7 KB (20728 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-alpine` - linux; 386

```console
$ docker pull memcached@sha256:006134e843d0ad5a3c64e903cc20d00c9f3e78a542fa3d6ba1e3ecec5b0ba3c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5742709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06188a4fb3481bcf32a3e44fca9d58ab763a52c65e02c95fbef5e98f4b78ee86`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Sat, 07 Mar 2026 00:37:00 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Mar 2026 00:37:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Mar 2026 00:39:49 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:39:49 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:39:49 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:39:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:39:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:39:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:39:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:39:50 GMT
USER memcache
# Sat, 07 Mar 2026 00:39:50 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:39:50 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ba4a2e327b273e788cfdef17b5c31ac5fefd6010584aa1c11b0d0104a041d6`  
		Last Modified: Sat, 07 Mar 2026 00:39:54 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ba4e8e1182330d5f76532f2f48fe38af386558e3e7fa4d94ce3dbf055be5ab`  
		Last Modified: Sat, 07 Mar 2026 00:39:54 GMT  
		Size: 110.7 KB (110732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01c1fe355d65277d08c7962b0be21d39386b4121b36381bbcb9a60d29449a5c`  
		Last Modified: Sat, 07 Mar 2026 00:39:54 GMT  
		Size: 1.9 MB (1943630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e102587e979593069cf080e59b8471ecf62f9c40abad1e62014f1742341827d0`  
		Last Modified: Sat, 07 Mar 2026 00:39:54 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46411b86935a4104c9cbb43c595a9cbf0e0330c814ca33c36935c5a9cb7f37d`  
		Last Modified: Sat, 07 Mar 2026 00:39:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:d0cb60f8d8c989514001fd52bf793673fa8f281758af2b58f8359d1d41973b11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58f3853067ae595d4075c459fe7b8361d199af21eaa1f93413e882c2e0bc9042`

```dockerfile
```

-	Layers:
	-	`sha256:2cd10df8bfae391e9a94e270083baf145ca51970a41e64ab71cd781740d00c73`  
		Last Modified: Sat, 07 Mar 2026 00:39:54 GMT  
		Size: 94.8 KB (94828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1d4f0d3116c96944777e5e4b1130eaff94973a8664033f37d3c60ceb36ed173`  
		Last Modified: Sat, 07 Mar 2026 00:39:54 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:35c354ed5e627574c294e54f0232ed89e8eacd7ed7e2670634db2396b8f2a39c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6034990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3da727092e7c56a19e8b1a382da13658524813ce0d2bca55dee5f4067987b77a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Sat, 07 Mar 2026 00:33:31 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Mar 2026 00:33:34 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Mar 2026 00:36:15 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:36:15 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:36:15 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:36:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:36:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:36:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:36:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:36:16 GMT
USER memcache
# Sat, 07 Mar 2026 00:36:16 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:36:16 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364a7d7b961599919f81b228a22514e1935e6774971d671f38dbad14ef71cbfd`  
		Last Modified: Sat, 07 Mar 2026 00:36:29 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d77d50c27f0ae298d21083636544fb7f795b9708dc480f081e1e936f1246e7`  
		Last Modified: Sat, 07 Mar 2026 00:36:29 GMT  
		Size: 126.3 KB (126266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d559c6185e0bba610ac4ee55bed1b0d85afdad6f054f17906fadb6311cc44007`  
		Last Modified: Sat, 07 Mar 2026 00:36:29 GMT  
		Size: 2.1 MB (2077727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce553e1c7553a28f652dbbd9f3d79596edea9eecf47883032057409cd1d977f`  
		Last Modified: Sat, 07 Mar 2026 00:36:29 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf30d9d84b197d47332200b954fc9fcedf3653c9a44fe6b72a5cf721ec170f1`  
		Last Modified: Sat, 07 Mar 2026 00:36:30 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7c60879107d9d8ce6f5e597f4c108df4a413d312eaf52e4c9303b96e80e84fbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eee93b7e24e493f45076a5a793e8b01aad30e3643bcb7583bc1fa26a1c4ff826`

```dockerfile
```

-	Layers:
	-	`sha256:b4505eef72239eda1b1c608b3226cd19dc02c372be606494a473db623050489a`  
		Last Modified: Sat, 07 Mar 2026 00:36:29 GMT  
		Size: 94.3 KB (94280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43cc72cbc203c87b12cbef8914fb2835a461df6bb0445da26d96b5a14e610184`  
		Last Modified: Sat, 07 Mar 2026 00:36:29 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:874942dd4e337f828a5480fa7e7e03b28951302101475540a14d752215e0b99e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5771014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61e6da61960009cb5e1d5f173422857994cb30b45c987fc35062485420c05ddf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 11 Mar 2026 21:21:50 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 11 Mar 2026 21:21:54 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 11 Mar 2026 21:35:15 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 11 Mar 2026 21:35:15 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 11 Mar 2026 21:35:15 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 11 Mar 2026 21:35:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 11 Mar 2026 21:35:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 11 Mar 2026 21:35:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 11 Mar 2026 21:35:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2026 21:35:16 GMT
USER memcache
# Wed, 11 Mar 2026 21:35:16 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 11 Mar 2026 21:35:16 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63b25af376cdb2cb3ddbdf009ec368c61af0677da2ff36f56052ba87ef9d03e`  
		Last Modified: Wed, 11 Mar 2026 21:35:39 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efcf2b36003649471638502666fa028dd48ae26bf7a732d6d7fe38a8432a7016`  
		Last Modified: Wed, 11 Mar 2026 21:35:39 GMT  
		Size: 108.9 KB (108902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddaf732ffb5731ec8232eec8940c917de4727564501c45fce52a7e2ebd641224`  
		Last Modified: Wed, 11 Mar 2026 21:35:40 GMT  
		Size: 2.1 MB (2075471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91cabf0fbda848cc214b782cee7c5c7224ddb7674e75de41599a3bbe85d6a689`  
		Last Modified: Wed, 11 Mar 2026 21:35:39 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:306ecccaa7e256f58e1e772b44b962766fdf35f118efb1596b4c9ae2431987ab`  
		Last Modified: Wed, 11 Mar 2026 21:35:40 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:5e6d73b60a6ccb5dda56fc4d483b45097e7ef55ce412da110e15c6c478c8d882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebcfe45486057ddd0b85095c8ca2fd1a8656b95e8ecf579e4de8717551ada915`

```dockerfile
```

-	Layers:
	-	`sha256:7176cf6ddf61d50975dee6f26ce9fdcb0b77085375b0dde58bb44b8337adca94`  
		Last Modified: Wed, 11 Mar 2026 21:35:39 GMT  
		Size: 94.3 KB (94276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5799ace3d1f3a380e60d9e9676ffbd335daf84ded3af9d5e1dd8ce83eee2060`  
		Last Modified: Wed, 11 Mar 2026 21:35:39 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:9c94884aa3d27f0c0ed5df500b79a6f3c2685bba5c632e3b871c0a262314d935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5858795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cd8a0886a7efaab4d69edd3b15f2a68384bcfdb1ff1a454930ba3a6a6ba29fc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Sat, 07 Mar 2026 00:33:34 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Mar 2026 00:33:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Mar 2026 00:36:49 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:36:49 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:36:49 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:36:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:36:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:36:49 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:36:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:36:49 GMT
USER memcache
# Sat, 07 Mar 2026 00:36:49 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:36:49 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f0d8799f878cf05935221d46a9b462122587e33ba748e54c983e03bbcb7ad2`  
		Last Modified: Sat, 07 Mar 2026 00:36:57 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef440db2f09493c5c9eae06dd0e59dafbd4761a74731e3ffa8ac968dcca712ca`  
		Last Modified: Sat, 07 Mar 2026 00:36:57 GMT  
		Size: 114.3 KB (114309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:134d34534319282a3e54d23ff3c63c0362a6c2ba38fb854b6a94a202d67347c2`  
		Last Modified: Sat, 07 Mar 2026 00:36:57 GMT  
		Size: 2.0 MB (2017802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:655653db981f7dce0174439408f99d0c480cb5082436a0682568bdaab190cd39`  
		Last Modified: Sat, 07 Mar 2026 00:36:57 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92dd0a7cdddba4f0415d5e0b6aa52c11369fa65b7c8c4ae965c949d55e7d52dd`  
		Last Modified: Sat, 07 Mar 2026 00:36:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:b9dd2a68695665b98af82b5110aa7af831b2d15654c26ffd200cc198ac79fb69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29c28af5a544343faaa1ff91b74bb776f4c5013c23bc2f45a2bbadb0fa1acc12`

```dockerfile
```

-	Layers:
	-	`sha256:47a88819c43763550a569259221f913c63dfd51ac45adc283170d20d81240959`  
		Last Modified: Sat, 07 Mar 2026 00:36:57 GMT  
		Size: 94.2 KB (94222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a9409046e85d857b00aa1f263c8c811160eeaa0c58b29abf61985c657289659`  
		Last Modified: Sat, 07 Mar 2026 00:36:57 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.41-alpine3.23`

```console
$ docker pull memcached@sha256:1c6a2d48c5f561226f1dc54ed37132f83b4cde94b5e3f3e2d88386d028b86a27
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
$ docker pull memcached@sha256:84dd21b0c8ebc30032a8aaa7270c7e6c11da52efd7bf3c7593530168946d3bd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5959699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaf5f46bdf2c26a9dda97cd7dd2b6a05c5d8135b2f9cbacf33ff8e8365f5e1eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Sat, 07 Mar 2026 00:36:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Mar 2026 00:36:14 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Mar 2026 00:38:52 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:38:52 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:38:52 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:38:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:38:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:38:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:38:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:38:52 GMT
USER memcache
# Sat, 07 Mar 2026 00:38:52 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:38:52 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d055707374a501222192f988c0ff35fcfdc5a017dd49a48e1dd38106c605f400`  
		Last Modified: Sat, 07 Mar 2026 00:38:57 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5abb10c57422a10d35029047d7b017a29437bc0081f375524cbfb3db3c9eaf9`  
		Last Modified: Sat, 07 Mar 2026 00:38:57 GMT  
		Size: 106.1 KB (106057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4fd18d57089d5254541b428a6a2429569ff07d571c824af865b666901af275e`  
		Last Modified: Sat, 07 Mar 2026 00:38:57 GMT  
		Size: 2.0 MB (1990468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885d9eb83efad8e7a74f165d5e00bd1e547b62348f4084f8748eb5123cfd5ef2`  
		Last Modified: Sat, 07 Mar 2026 00:38:57 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32954341fb1b6227e3bb596d1a3f58beb03c348455e63c0e6a810197d1922e9`  
		Last Modified: Sat, 07 Mar 2026 00:38:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:e0615e85e00302f3ab01f14593cf39cf7e4ac01f448e6904dd61247bf63b3ff0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3b92ada03392c40180327b1e82f1b29a80b1164d4b65115558c1efc811142ad`

```dockerfile
```

-	Layers:
	-	`sha256:cc3e65e74aa6c619611c020b3d498d3c756e6168a9b26434ca30c3099cfa3261`  
		Last Modified: Sat, 07 Mar 2026 00:38:57 GMT  
		Size: 94.9 KB (94873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:327a47bce4975ea9e581754831550ac249839dc3708d4841f78ebc6cbd78d014`  
		Last Modified: Sat, 07 Mar 2026 00:38:57 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-alpine3.23` - linux; arm variant v6

```console
$ docker pull memcached@sha256:6cde7ea7574023751e83c90e1e8f1f7aef03c1d5b0fbe20a17d981d57edb99dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:376e43ecede029f4d02a7634c75d3107a5797f724660eb9b02b0eb12c3e49748`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Sat, 07 Mar 2026 00:34:25 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Mar 2026 00:34:26 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Mar 2026 00:37:29 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:37:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:37:29 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:37:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:37:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:37:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:37:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:37:29 GMT
USER memcache
# Sat, 07 Mar 2026 00:37:29 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:37:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18dad4d028ff2b78314498b57b872634656cb70add272a07cde87477543ea34b`  
		Last Modified: Sat, 07 Mar 2026 00:37:33 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5343ac0baa24b86f7ffac4e0a3296276d4a7aa05b74617720244260e34dc5aba`  
		Last Modified: Sat, 07 Mar 2026 00:37:33 GMT  
		Size: 102.7 KB (102655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f65584616382b3a0c0b70214fd4046110bedf9cfbb2c2f89c2301372f8aa27`  
		Last Modified: Sat, 07 Mar 2026 00:37:33 GMT  
		Size: 1.9 MB (1940281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a378f9c04f9d21fc788013f2928b3637ad3724011b85ecb4d8fe5a61ca9bb2`  
		Last Modified: Sat, 07 Mar 2026 00:37:33 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9600d067846989777b70f754cdd61c2012197736201713e9b5ff3703b147be02`  
		Last Modified: Sat, 07 Mar 2026 00:37:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:1d36396e4f4bb90ed2d326fbc737d8ab225cf619e64f08c3ff0beaff000177ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e204629c18255bb70ea677237338842d7ed3a140e1ecbbc4b8d5727cafa1668e`

```dockerfile
```

-	Layers:
	-	`sha256:1ea1c312fb87cc4d7c73a561d98b13a1f13504625a2de3953101370977fc6745`  
		Last Modified: Sat, 07 Mar 2026 00:37:33 GMT  
		Size: 20.5 KB (20466 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-alpine3.23` - linux; arm variant v7

```console
$ docker pull memcached@sha256:91fe29148d686af2a0fdc23ba01a1b272f4c6365fc45bc37d00d4687a0c41b1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5273746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a56ac817dd40669cbf75609948d0f6fc05e648f6453d8f9deba7740682f741f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Sat, 07 Mar 2026 00:37:41 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Mar 2026 00:37:42 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Mar 2026 00:40:39 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:40:39 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:40:39 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:40:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:40:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:40:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:40:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:40:39 GMT
USER memcache
# Sat, 07 Mar 2026 00:40:39 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:40:39 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a51b7877e94969180dbb0be219881bc9230f055057f9e3f4b65f1db0708689a`  
		Last Modified: Sat, 07 Mar 2026 00:40:44 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c32abf408db65abfcd3224db5db2abaa977bd3ce59942c389c73320a4051cc`  
		Last Modified: Sat, 07 Mar 2026 00:40:44 GMT  
		Size: 92.4 KB (92374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ddc29b1020998fb5a3b242cc4e45954bc53540a31017ab6a020f9dff807bd22`  
		Last Modified: Sat, 07 Mar 2026 00:40:44 GMT  
		Size: 1.9 MB (1898298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae00440f5f6fd5951552907706f8df3661315090758ede99bb2933aa3384040b`  
		Last Modified: Sat, 07 Mar 2026 00:40:44 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb70de481e3407c522658dfa65d701fde07648ab9b8c732379d8a92f44092a81`  
		Last Modified: Sat, 07 Mar 2026 00:40:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:073366e4d50888ea6d43868ab35c2a063ea12dc243105f0c614c4feaa55d0eda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c47e8e147c04b6fae9be2f9c70644395f05ac10516981d5f48aac87100f9aabf`

```dockerfile
```

-	Layers:
	-	`sha256:f128294dbb16b2300fe484115b6bd24498974e73ac8835f70a3dd5df2f3211cd`  
		Last Modified: Sat, 07 Mar 2026 00:40:44 GMT  
		Size: 94.3 KB (94291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad6c6671c716b1f4cb8882be9d7cee792a3b5a0500ba4330e4c34c83d3401a1c`  
		Last Modified: Sat, 07 Mar 2026 00:40:44 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:eeb1c0de2b6b33a7a724454aaf9fd945503a062302d133c059f1b829db991b61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6287490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0de2d8f866d91b49adb4cfa80ffd26e168ac627328864d7ceae76dfd0bc4d7a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Sat, 07 Mar 2026 00:36:34 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Mar 2026 00:36:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Mar 2026 00:39:22 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:39:22 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:39:22 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:39:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:39:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:39:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:39:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:39:22 GMT
USER memcache
# Sat, 07 Mar 2026 00:39:22 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:39:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d65cacaa69d1c76240e558dab714b69561f9bb333c2c1c147f9be7d6b29c36`  
		Last Modified: Sat, 07 Mar 2026 00:39:27 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca80346986e335b6e96f14599a1ab3629964fa8702f4570e2d199da8b04498e`  
		Last Modified: Sat, 07 Mar 2026 00:39:27 GMT  
		Size: 121.9 KB (121860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bcaaaf5541ab3a5d055204886aadf36871e66f535b6c1978b4b4c58a4dc2367`  
		Last Modified: Sat, 07 Mar 2026 00:39:27 GMT  
		Size: 2.0 MB (1967188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6167d1b1458d5cedc7774a2a1e9e621f5b32de851a6b19d82ea2275ec9f1bc5`  
		Last Modified: Sat, 07 Mar 2026 00:39:27 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2040432b455fd0270cf480396dc9c1570b8710e21539cc0110e13fe10105062`  
		Last Modified: Sat, 07 Mar 2026 00:39:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:3d8284de1f87be934ca3ad16b60f3a624262a50260f7f8db4cc80575af22e7c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9a54dfb1a405917a8fe0eaf03a1588913998eac5cacc5141cad5d053c6ba838`

```dockerfile
```

-	Layers:
	-	`sha256:8eefe1140db7c68e1990a3744cd3126838a63605758bc6825cb1c090277cf806`  
		Last Modified: Sat, 07 Mar 2026 00:39:27 GMT  
		Size: 94.3 KB (94327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92f28d8e0dd01f916858b48749b2827fadaadb7ca45a0a8a872ac9d74043589d`  
		Last Modified: Sat, 07 Mar 2026 00:39:27 GMT  
		Size: 20.7 KB (20728 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-alpine3.23` - linux; 386

```console
$ docker pull memcached@sha256:006134e843d0ad5a3c64e903cc20d00c9f3e78a542fa3d6ba1e3ecec5b0ba3c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5742709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06188a4fb3481bcf32a3e44fca9d58ab763a52c65e02c95fbef5e98f4b78ee86`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Sat, 07 Mar 2026 00:37:00 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Mar 2026 00:37:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Mar 2026 00:39:49 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:39:49 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:39:49 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:39:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:39:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:39:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:39:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:39:50 GMT
USER memcache
# Sat, 07 Mar 2026 00:39:50 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:39:50 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ba4a2e327b273e788cfdef17b5c31ac5fefd6010584aa1c11b0d0104a041d6`  
		Last Modified: Sat, 07 Mar 2026 00:39:54 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ba4e8e1182330d5f76532f2f48fe38af386558e3e7fa4d94ce3dbf055be5ab`  
		Last Modified: Sat, 07 Mar 2026 00:39:54 GMT  
		Size: 110.7 KB (110732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01c1fe355d65277d08c7962b0be21d39386b4121b36381bbcb9a60d29449a5c`  
		Last Modified: Sat, 07 Mar 2026 00:39:54 GMT  
		Size: 1.9 MB (1943630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e102587e979593069cf080e59b8471ecf62f9c40abad1e62014f1742341827d0`  
		Last Modified: Sat, 07 Mar 2026 00:39:54 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46411b86935a4104c9cbb43c595a9cbf0e0330c814ca33c36935c5a9cb7f37d`  
		Last Modified: Sat, 07 Mar 2026 00:39:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:d0cb60f8d8c989514001fd52bf793673fa8f281758af2b58f8359d1d41973b11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58f3853067ae595d4075c459fe7b8361d199af21eaa1f93413e882c2e0bc9042`

```dockerfile
```

-	Layers:
	-	`sha256:2cd10df8bfae391e9a94e270083baf145ca51970a41e64ab71cd781740d00c73`  
		Last Modified: Sat, 07 Mar 2026 00:39:54 GMT  
		Size: 94.8 KB (94828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1d4f0d3116c96944777e5e4b1130eaff94973a8664033f37d3c60ceb36ed173`  
		Last Modified: Sat, 07 Mar 2026 00:39:54 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-alpine3.23` - linux; ppc64le

```console
$ docker pull memcached@sha256:35c354ed5e627574c294e54f0232ed89e8eacd7ed7e2670634db2396b8f2a39c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6034990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3da727092e7c56a19e8b1a382da13658524813ce0d2bca55dee5f4067987b77a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Sat, 07 Mar 2026 00:33:31 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Mar 2026 00:33:34 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Mar 2026 00:36:15 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:36:15 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:36:15 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:36:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:36:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:36:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:36:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:36:16 GMT
USER memcache
# Sat, 07 Mar 2026 00:36:16 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:36:16 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364a7d7b961599919f81b228a22514e1935e6774971d671f38dbad14ef71cbfd`  
		Last Modified: Sat, 07 Mar 2026 00:36:29 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d77d50c27f0ae298d21083636544fb7f795b9708dc480f081e1e936f1246e7`  
		Last Modified: Sat, 07 Mar 2026 00:36:29 GMT  
		Size: 126.3 KB (126266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d559c6185e0bba610ac4ee55bed1b0d85afdad6f054f17906fadb6311cc44007`  
		Last Modified: Sat, 07 Mar 2026 00:36:29 GMT  
		Size: 2.1 MB (2077727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce553e1c7553a28f652dbbd9f3d79596edea9eecf47883032057409cd1d977f`  
		Last Modified: Sat, 07 Mar 2026 00:36:29 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf30d9d84b197d47332200b954fc9fcedf3653c9a44fe6b72a5cf721ec170f1`  
		Last Modified: Sat, 07 Mar 2026 00:36:30 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:7c60879107d9d8ce6f5e597f4c108df4a413d312eaf52e4c9303b96e80e84fbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eee93b7e24e493f45076a5a793e8b01aad30e3643bcb7583bc1fa26a1c4ff826`

```dockerfile
```

-	Layers:
	-	`sha256:b4505eef72239eda1b1c608b3226cd19dc02c372be606494a473db623050489a`  
		Last Modified: Sat, 07 Mar 2026 00:36:29 GMT  
		Size: 94.3 KB (94280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43cc72cbc203c87b12cbef8914fb2835a461df6bb0445da26d96b5a14e610184`  
		Last Modified: Sat, 07 Mar 2026 00:36:29 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-alpine3.23` - linux; riscv64

```console
$ docker pull memcached@sha256:874942dd4e337f828a5480fa7e7e03b28951302101475540a14d752215e0b99e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5771014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61e6da61960009cb5e1d5f173422857994cb30b45c987fc35062485420c05ddf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 11 Mar 2026 21:21:50 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 11 Mar 2026 21:21:54 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 11 Mar 2026 21:35:15 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 11 Mar 2026 21:35:15 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 11 Mar 2026 21:35:15 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 11 Mar 2026 21:35:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 11 Mar 2026 21:35:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 11 Mar 2026 21:35:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 11 Mar 2026 21:35:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2026 21:35:16 GMT
USER memcache
# Wed, 11 Mar 2026 21:35:16 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 11 Mar 2026 21:35:16 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63b25af376cdb2cb3ddbdf009ec368c61af0677da2ff36f56052ba87ef9d03e`  
		Last Modified: Wed, 11 Mar 2026 21:35:39 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efcf2b36003649471638502666fa028dd48ae26bf7a732d6d7fe38a8432a7016`  
		Last Modified: Wed, 11 Mar 2026 21:35:39 GMT  
		Size: 108.9 KB (108902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddaf732ffb5731ec8232eec8940c917de4727564501c45fce52a7e2ebd641224`  
		Last Modified: Wed, 11 Mar 2026 21:35:40 GMT  
		Size: 2.1 MB (2075471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91cabf0fbda848cc214b782cee7c5c7224ddb7674e75de41599a3bbe85d6a689`  
		Last Modified: Wed, 11 Mar 2026 21:35:39 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:306ecccaa7e256f58e1e772b44b962766fdf35f118efb1596b4c9ae2431987ab`  
		Last Modified: Wed, 11 Mar 2026 21:35:40 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:5e6d73b60a6ccb5dda56fc4d483b45097e7ef55ce412da110e15c6c478c8d882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebcfe45486057ddd0b85095c8ca2fd1a8656b95e8ecf579e4de8717551ada915`

```dockerfile
```

-	Layers:
	-	`sha256:7176cf6ddf61d50975dee6f26ce9fdcb0b77085375b0dde58bb44b8337adca94`  
		Last Modified: Wed, 11 Mar 2026 21:35:39 GMT  
		Size: 94.3 KB (94276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5799ace3d1f3a380e60d9e9676ffbd335daf84ded3af9d5e1dd8ce83eee2060`  
		Last Modified: Wed, 11 Mar 2026 21:35:39 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-alpine3.23` - linux; s390x

```console
$ docker pull memcached@sha256:9c94884aa3d27f0c0ed5df500b79a6f3c2685bba5c632e3b871c0a262314d935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5858795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cd8a0886a7efaab4d69edd3b15f2a68384bcfdb1ff1a454930ba3a6a6ba29fc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Sat, 07 Mar 2026 00:33:34 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Mar 2026 00:33:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Mar 2026 00:36:49 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:36:49 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:36:49 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:36:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:36:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:36:49 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:36:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:36:49 GMT
USER memcache
# Sat, 07 Mar 2026 00:36:49 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:36:49 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f0d8799f878cf05935221d46a9b462122587e33ba748e54c983e03bbcb7ad2`  
		Last Modified: Sat, 07 Mar 2026 00:36:57 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef440db2f09493c5c9eae06dd0e59dafbd4761a74731e3ffa8ac968dcca712ca`  
		Last Modified: Sat, 07 Mar 2026 00:36:57 GMT  
		Size: 114.3 KB (114309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:134d34534319282a3e54d23ff3c63c0362a6c2ba38fb854b6a94a202d67347c2`  
		Last Modified: Sat, 07 Mar 2026 00:36:57 GMT  
		Size: 2.0 MB (2017802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:655653db981f7dce0174439408f99d0c480cb5082436a0682568bdaab190cd39`  
		Last Modified: Sat, 07 Mar 2026 00:36:57 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92dd0a7cdddba4f0415d5e0b6aa52c11369fa65b7c8c4ae965c949d55e7d52dd`  
		Last Modified: Sat, 07 Mar 2026 00:36:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:b9dd2a68695665b98af82b5110aa7af831b2d15654c26ffd200cc198ac79fb69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29c28af5a544343faaa1ff91b74bb776f4c5013c23bc2f45a2bbadb0fa1acc12`

```dockerfile
```

-	Layers:
	-	`sha256:47a88819c43763550a569259221f913c63dfd51ac45adc283170d20d81240959`  
		Last Modified: Sat, 07 Mar 2026 00:36:57 GMT  
		Size: 94.2 KB (94222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a9409046e85d857b00aa1f263c8c811160eeaa0c58b29abf61985c657289659`  
		Last Modified: Sat, 07 Mar 2026 00:36:57 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.41-trixie`

```console
$ docker pull memcached@sha256:d99136ed4c1cf2e3fceb498763f2b7fedec7c486a0fe8a57be19f2a0519ce1fa
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
$ docker pull memcached@sha256:c08df224e6ccee2c893ac468902a8b68d8221910014da88f892d483b145f2e80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32197142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc0c289673d3b6f117607d5014b52d276fa02ad622404df04deac38f7a3b2b75`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Sat, 07 Mar 2026 00:34:28 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Mar 2026 00:34:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Mar 2026 00:37:16 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:37:16 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:37:16 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:37:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:37:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:37:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:37:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:37:16 GMT
USER memcache
# Sat, 07 Mar 2026 00:37:16 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:37:16 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65546826072afb14e8706d66b636911c885382731f6d325cba605469fdb363e7`  
		Last Modified: Sat, 07 Mar 2026 00:37:23 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f84d4f33fb93823aaef11588c633186a7b4c7e9c0fea6cf0c2c2e912be6b9f`  
		Last Modified: Sat, 07 Mar 2026 00:37:23 GMT  
		Size: 136.7 KB (136684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f30a00378f01ca7716c334349799965f472572c2377432ae0948fb3481a330`  
		Last Modified: Sat, 07 Mar 2026 00:37:23 GMT  
		Size: 2.3 MB (2280310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd736c12c1d448b0585c460fd3f417da3a21193665ef2aefd67c221cbd97df0b`  
		Last Modified: Sat, 07 Mar 2026 00:37:23 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f072b1e28c7bdff147ef49013b08dfe871999faec678a4219890f645e2d14b`  
		Last Modified: Sat, 07 Mar 2026 00:37:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:b0cd4839975a3f144a6d44260b40e6cebfaad48ae0dabae69c8a84a1912f55ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d69fb1b8b08633539bde084818362e1b13aae93417c6fc42c6c674e4039d2ab4`

```dockerfile
```

-	Layers:
	-	`sha256:0bc9fc51640e8d0b171e44a65462e97d0e54980aca3e0ea45f57320911a0f07c`  
		Last Modified: Sat, 07 Mar 2026 00:37:23 GMT  
		Size: 2.0 MB (2008290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2632163ed214b82be06d84daacb113b153e4ec7def67cd764cb771fb9700aeaf`  
		Last Modified: Sat, 07 Mar 2026 00:37:23 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-trixie` - linux; arm variant v5

```console
$ docker pull memcached@sha256:514cbf94b5380f36ac3c88108bf78a84ae83c3ed26e638ebe2e2f5bb88bd25ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30304774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc4d63874316ce18eaa26acb02c5e3dc129e31ea8c480a3a966621c75552572c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1771804800'
# Sat, 07 Mar 2026 00:34:25 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Mar 2026 00:34:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Mar 2026 00:37:50 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:37:50 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:37:50 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:37:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:37:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:37:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:37:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:37:50 GMT
USER memcache
# Sat, 07 Mar 2026 00:37:50 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:37:50 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:280a075cc1d2a97445b9f4430aa9774bfc38fc4217b7fc9d6a7b04e7e431cb65`  
		Last Modified: Tue, 24 Feb 2026 18:42:44 GMT  
		Size: 27.9 MB (27947608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fee55b7ab1f18dde561acdb3246640b49ed746f0a6f679b8b4be2fe96c38edc`  
		Last Modified: Sat, 07 Mar 2026 00:37:56 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e90ce24e8e18d6e22b1819e0c183af55656f28a490d2a5f5db1bb199759ae2`  
		Last Modified: Sat, 07 Mar 2026 00:37:56 GMT  
		Size: 144.2 KB (144173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e14eaa4ef07ee7a2796a97655630e5b528d0f2f8120ba62ac860fcf148e2b813`  
		Last Modified: Sat, 07 Mar 2026 00:37:56 GMT  
		Size: 2.2 MB (2211477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0271cbc419600dba0091ae986cd78ada6340afbfa697b93993e1f63555a831`  
		Last Modified: Sat, 07 Mar 2026 00:37:56 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ecc8023e8fc75e87c4b1fc32230e35e765d671345bd42f98dfe13b7118bc13`  
		Last Modified: Sat, 07 Mar 2026 00:37:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:3b41b0fb30672979494c2bcc11e11de72d662cbeef4e097e83bf3637c45aba4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b344e75a26fbd848f3d4bda6dfbc82971e7c99f16f8b8d3c2f4e0046b3e36cf`

```dockerfile
```

-	Layers:
	-	`sha256:a8abf2c9952faed7ee6a8484d94c195f2f516d28b4aa99d61fde6a938373ef14`  
		Last Modified: Sat, 07 Mar 2026 00:37:56 GMT  
		Size: 2.0 MB (2011293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4baff3ba9a329e3fdeaee0149357b33f76e181413fc6e5b4d1b9502670d8aab3`  
		Last Modified: Sat, 07 Mar 2026 00:37:56 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-trixie` - linux; arm variant v7

```console
$ docker pull memcached@sha256:5e39383d269092b745c7426583a0849917817a2861226858ff17c34f227cadc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28515640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4d89f2522b7f402debcdfe4ae5ef33ccc13694e72756aabd8c894fd1a657663`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Sat, 07 Mar 2026 00:34:26 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Mar 2026 00:34:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Mar 2026 00:37:36 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:37:36 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:37:36 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:37:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:37:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:37:37 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:37:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:37:37 GMT
USER memcache
# Sat, 07 Mar 2026 00:37:37 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:37:37 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b5f623d77fff35b334b15c7b208113b4b778a70ce39168e1270421140984e6`  
		Last Modified: Sat, 07 Mar 2026 00:37:43 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d378422d428b98928a2c392598ff24dddba86412c764099339db2c9b84dab7`  
		Last Modified: Sat, 07 Mar 2026 00:37:43 GMT  
		Size: 135.4 KB (135371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ebe7571649e14f8ae60c2aa9c7464f120d47deb28852880adc72f5958fb268`  
		Last Modified: Sat, 07 Mar 2026 00:37:43 GMT  
		Size: 2.2 MB (2165006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab8a97091ab7e05c0561d93041f6833b293ec83a81c5cd316d914c7cd4797f5`  
		Last Modified: Sat, 07 Mar 2026 00:37:43 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06917ca5c3af99a9a619b7c0077abf8521b0777d4c07464889139b6030aaa445`  
		Last Modified: Sat, 07 Mar 2026 00:37:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:17c7cd3931d1614e411d593e6027c70049d32dd6b78b4523f5e29ff13b7b1f21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b42f736130d7735ab6bde638b9206c6be06a848c316aa0776562b9d2b05634b5`

```dockerfile
```

-	Layers:
	-	`sha256:1700f9d32fecaf2a6fff6e275b9eac8036467ba4e592635351cf279712b2017b`  
		Last Modified: Sat, 07 Mar 2026 00:37:43 GMT  
		Size: 2.0 MB (2009750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef3320ccea4ba2f43dfdeb26388b30f9251a45c8b87522656d05eb856e022fa0`  
		Last Modified: Sat, 07 Mar 2026 00:37:43 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-trixie` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:03ff213526efc235b60a048b3efa0c67c6d697a62bdc207561fb8ee00f254f89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32557234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4742c51756a2139de24009e1c754635923a703d67706387249d261e4dc62712`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Sat, 07 Mar 2026 00:34:23 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Mar 2026 00:34:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Mar 2026 00:37:25 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:37:25 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:37:25 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:37:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:37:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:37:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:37:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:37:25 GMT
USER memcache
# Sat, 07 Mar 2026 00:37:25 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:37:25 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:461d33f62f9a4e4fbc09492d8ce59e548e8c794e3122411c5f7a8370f2bbedba`  
		Last Modified: Sat, 07 Mar 2026 00:37:31 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e642309aa5a12065d7f985c382b7658fa51b45c2a111039cdb9b7240299809e7`  
		Last Modified: Sat, 07 Mar 2026 00:37:31 GMT  
		Size: 153.5 KB (153496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c81e14adafcb230598de8ae3eaf03443a9ae10bd04e616ae4ab64a2f379a48d`  
		Last Modified: Sat, 07 Mar 2026 00:37:31 GMT  
		Size: 2.3 MB (2262125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62e12af1edbdc302c3fd82e9561c5eac5def3110b53dc9d527b277d70a0c5b0`  
		Last Modified: Sat, 07 Mar 2026 00:37:31 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eee7fdafd6f634c0431e5a06be62ff9a726cb1fa8367483d6b026fa3164c7f0`  
		Last Modified: Sat, 07 Mar 2026 00:37:32 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:f791266a2bf814187fed117fa0abd604df8d26056d2e2791b51eb537a958de3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e7b8f74c70d2427388103547caa9c90ef2b4ec4ee11ce197e642593e10f6979`

```dockerfile
```

-	Layers:
	-	`sha256:88d9544d6eb9588edcaeabdc26922a9afb53b2222e8f9972e5b4b52199893738`  
		Last Modified: Sat, 07 Mar 2026 00:37:31 GMT  
		Size: 2.0 MB (2008606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b245266f3e6e113152f086489529a68f1c8c229363d9b678823c16250c48131`  
		Last Modified: Sat, 07 Mar 2026 00:37:31 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-trixie` - linux; 386

```console
$ docker pull memcached@sha256:1219e49a37eb8fa43f5cabcda7eb69df920734c5d615f2fc63e4fba52a06dfd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33667722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d141db22d43d8c6503a206b3413976c2fd0b84654a45bb46a3da3f39594ee93e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1771804800'
# Sat, 07 Mar 2026 00:34:41 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Mar 2026 00:34:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Mar 2026 00:37:41 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:37:41 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:37:41 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:37:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:37:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:37:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:37:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:37:41 GMT
USER memcache
# Sat, 07 Mar 2026 00:37:41 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:37:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f4e0b944ee1e7e50bdfbfa77bda370b6eccee7d698a7adca78c38f5ca0767ca5`  
		Last Modified: Tue, 24 Feb 2026 18:43:18 GMT  
		Size: 31.3 MB (31293918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d38eff546890db9ae0646486b61a548d8067820adc96ceb6eb4f5d7c2206bb8`  
		Last Modified: Sat, 07 Mar 2026 00:37:47 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c454125cf8ccd03f95714478c13c1d671ba0807b980ee5e6df450d611f61e156`  
		Last Modified: Sat, 07 Mar 2026 00:37:47 GMT  
		Size: 147.5 KB (147517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42b7d17f494cc1acab1da36a724a41a46ecf955d058123b89b170ea63bafda97`  
		Last Modified: Sat, 07 Mar 2026 00:37:47 GMT  
		Size: 2.2 MB (2224772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56fcaee4e2b815384392953fdf84278be4b9a4b116e3a5ad6436f7b13a7c6d9`  
		Last Modified: Sat, 07 Mar 2026 00:37:47 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6adacd7f3e38f46b44efa4ff006b35719382afa26b95b7a9b0c62ef7e7a01bfc`  
		Last Modified: Sat, 07 Mar 2026 00:37:48 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:9f65574f3294736b3dc217e4b07a4045282c517d258eaa96a32035e09cda6fa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb96fc147195e16ed2b6e99c3582cd8c6a67516fb0387c563d09fbf85f6a4dc0`

```dockerfile
```

-	Layers:
	-	`sha256:cdc74dec8f482313433fa0011e8531a8e816610bf31af8b63d2203318e8a59f9`  
		Last Modified: Sat, 07 Mar 2026 00:37:47 GMT  
		Size: 2.0 MB (2005447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bbcbbf7d1935fe3e711cd689ff38f789c3f7334bff2fd2518c106c4bf5d805f`  
		Last Modified: Sat, 07 Mar 2026 00:37:47 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-trixie` - linux; ppc64le

```console
$ docker pull memcached@sha256:ffac94778c7c882a7f2cbaae5af33e755639de207d07834e052412c2b22a24b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36754462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5640d71fb49b8eaef07631709a9f4924bd191fcfe9b44b7df2d525e247075b64`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Sat, 07 Mar 2026 00:33:31 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Mar 2026 00:33:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Mar 2026 00:56:42 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:56:42 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:56:42 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:56:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:56:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:56:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:56:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:56:44 GMT
USER memcache
# Sat, 07 Mar 2026 00:56:44 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:56:44 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab70996aa4a561e7f3e1f1e1b14df7912a1456b20b317937391cfa826c93f2ea`  
		Last Modified: Sat, 07 Mar 2026 00:57:10 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1ba00921effa53d91205ba3e5e3280c719885f49b5e9e0f8e2a387cf316d89`  
		Last Modified: Sat, 07 Mar 2026 00:57:10 GMT  
		Size: 170.4 KB (170386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd00738358190677470eca91b6732f6fcc475639b7f07f1943af6f5d268ae47`  
		Last Modified: Sat, 07 Mar 2026 00:57:10 GMT  
		Size: 3.0 MB (2982343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f7dc97a8f5d8c677e24bd2f8014c3e315619d726d409033dc3ce4f6d7d7569d`  
		Last Modified: Sat, 07 Mar 2026 00:57:10 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f2b48241128f09e1c613b0fb34d37f79c77417d033b7a00041f8cd08d6241f`  
		Last Modified: Sat, 07 Mar 2026 00:57:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:da557c745e92be8dd35823b9c24b79e47c55ff727768980abe9b659a14672408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e89b8bba62432d49e11baad935eddf449853276e5bb492953ae6bb995bf81ef`

```dockerfile
```

-	Layers:
	-	`sha256:7bf94ead3bca06412117cdc5395bde9d799ffc799dd28be779209634f64bfc0b`  
		Last Modified: Sat, 07 Mar 2026 00:57:10 GMT  
		Size: 2.0 MB (2011891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ec351466954789ecb039e735ecf9fd0235d5d4cfcf8bd6bcf2cf68049016c1c`  
		Last Modified: Sat, 07 Mar 2026 00:57:10 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-trixie` - linux; riscv64

```console
$ docker pull memcached@sha256:ccac0e143b4efd5bd15fb67df5ad87f5b743cc3db826cbb27d1874cbb3b6d549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30619564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f9320af1aa6fbbae22f81ef28d68694abc001739c71a195b4b1cd490b3b9107`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 23:50:36 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 09 Mar 2026 23:51:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Mar 2026 00:09:03 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 10 Mar 2026 00:09:03 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 10 Mar 2026 00:09:03 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 10 Mar 2026 00:09:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 10 Mar 2026 00:09:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 10 Mar 2026 00:09:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 10 Mar 2026 00:09:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Mar 2026 00:09:03 GMT
USER memcache
# Tue, 10 Mar 2026 00:09:03 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 10 Mar 2026 00:09:03 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e1366b1f74881f04901f31cfdecf9f3f5d4794ebf89911083a239bf462bf21`  
		Last Modified: Tue, 10 Mar 2026 00:09:56 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918782f8ab4ae7fe2ab9f1fc0aa7ad4e48d83dc362a4dcac336048ded3de9b6e`  
		Last Modified: Tue, 10 Mar 2026 00:09:56 GMT  
		Size: 133.1 KB (133079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963fbe1d00657987e81bdc270499ad5aacf8f91b100915c30ddf9fc57cd67346`  
		Last Modified: Tue, 10 Mar 2026 00:09:56 GMT  
		Size: 2.2 MB (2208551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729657786193241c665df2cbaeb72b5d157865abb3bbd8b9460e88d08fb65fea`  
		Last Modified: Tue, 10 Mar 2026 00:09:56 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8246f12fbc1ee94790a418b9655df55d80968171273b5994aaffa40c04fa2f3c`  
		Last Modified: Tue, 10 Mar 2026 00:09:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:de9f0d80a354763898649af4229a6f696fb51689e3b577af2e1d918d365777e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d72c30b80e1c2deaee38b267b52cab1a28e245b2a3608fcf459f2232dad3faa7`

```dockerfile
```

-	Layers:
	-	`sha256:03d9f11a7e8cf93ffe1f13ecfd86632a66af5a6efc142ae7a4ecac0c19418b2d`  
		Last Modified: Tue, 10 Mar 2026 00:09:56 GMT  
		Size: 2.0 MB (2002254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:452e3f764b5054c447aa8e63046155a20784d6f10159282ce633afdb79bf9279`  
		Last Modified: Tue, 10 Mar 2026 00:09:56 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-trixie` - linux; s390x

```console
$ docker pull memcached@sha256:8e1f3fb07bf1702ad27a7e2a6b2364e61d7b5165c113d0202db31adaa90d91df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32278340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1088ed36ed575f78d3e06fdd24f1ccdcc908d6e579970b2cae128c29f8d6e7a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Sat, 07 Mar 2026 00:33:32 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Mar 2026 00:33:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Mar 2026 00:36:51 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:36:51 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:36:51 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:36:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:36:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:36:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:36:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:36:51 GMT
USER memcache
# Sat, 07 Mar 2026 00:36:51 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:36:51 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986cc162f1a9b2f1b4c673da47497d87b8a542990f29c7823ee4d64cd160ea34`  
		Last Modified: Sat, 07 Mar 2026 00:37:00 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e3b516d24d039487b70f5d718d6f2b0c5473b5da4e6b82815239c7730587d6`  
		Last Modified: Sat, 07 Mar 2026 00:37:00 GMT  
		Size: 140.5 KB (140520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb611bdb547903f4763e52741be4c28e6ed0f172ebffc4ddae4e56a1a4d3ebc2`  
		Last Modified: Sat, 07 Mar 2026 00:37:00 GMT  
		Size: 2.3 MB (2298126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b32c7b8a27f2284141ba22bde8036a295b3e0d397cde405054e47e550cced01`  
		Last Modified: Sat, 07 Mar 2026 00:37:00 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3240387a49966ed4c1475913af7c7648c5499d01045e56e16637a760300918a`  
		Last Modified: Sat, 07 Mar 2026 00:37:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:b725149e071a1d02723f7674a5f7c477144350f79f2243558bce2360da7bf73b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:628ead940c50f3d4776c150c412d2270c2238893cfd1a57f8c17647ec35223e2`

```dockerfile
```

-	Layers:
	-	`sha256:b118af94ed9d10ab8f0c0221725860a15ff82dce98bd35abb240f411b745e0f7`  
		Last Modified: Sat, 07 Mar 2026 00:37:00 GMT  
		Size: 2.0 MB (2009727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:737fa51b5113fe89d161d6b7d0d81d66c28e666617dc1fb7c410b093ecf35625`  
		Last Modified: Sat, 07 Mar 2026 00:37:00 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine`

```console
$ docker pull memcached@sha256:1c6a2d48c5f561226f1dc54ed37132f83b4cde94b5e3f3e2d88386d028b86a27
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
$ docker pull memcached@sha256:84dd21b0c8ebc30032a8aaa7270c7e6c11da52efd7bf3c7593530168946d3bd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5959699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaf5f46bdf2c26a9dda97cd7dd2b6a05c5d8135b2f9cbacf33ff8e8365f5e1eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Sat, 07 Mar 2026 00:36:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Mar 2026 00:36:14 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Mar 2026 00:38:52 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:38:52 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:38:52 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:38:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:38:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:38:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:38:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:38:52 GMT
USER memcache
# Sat, 07 Mar 2026 00:38:52 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:38:52 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d055707374a501222192f988c0ff35fcfdc5a017dd49a48e1dd38106c605f400`  
		Last Modified: Sat, 07 Mar 2026 00:38:57 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5abb10c57422a10d35029047d7b017a29437bc0081f375524cbfb3db3c9eaf9`  
		Last Modified: Sat, 07 Mar 2026 00:38:57 GMT  
		Size: 106.1 KB (106057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4fd18d57089d5254541b428a6a2429569ff07d571c824af865b666901af275e`  
		Last Modified: Sat, 07 Mar 2026 00:38:57 GMT  
		Size: 2.0 MB (1990468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885d9eb83efad8e7a74f165d5e00bd1e547b62348f4084f8748eb5123cfd5ef2`  
		Last Modified: Sat, 07 Mar 2026 00:38:57 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32954341fb1b6227e3bb596d1a3f58beb03c348455e63c0e6a810197d1922e9`  
		Last Modified: Sat, 07 Mar 2026 00:38:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:e0615e85e00302f3ab01f14593cf39cf7e4ac01f448e6904dd61247bf63b3ff0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3b92ada03392c40180327b1e82f1b29a80b1164d4b65115558c1efc811142ad`

```dockerfile
```

-	Layers:
	-	`sha256:cc3e65e74aa6c619611c020b3d498d3c756e6168a9b26434ca30c3099cfa3261`  
		Last Modified: Sat, 07 Mar 2026 00:38:57 GMT  
		Size: 94.9 KB (94873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:327a47bce4975ea9e581754831550ac249839dc3708d4841f78ebc6cbd78d014`  
		Last Modified: Sat, 07 Mar 2026 00:38:57 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:6cde7ea7574023751e83c90e1e8f1f7aef03c1d5b0fbe20a17d981d57edb99dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:376e43ecede029f4d02a7634c75d3107a5797f724660eb9b02b0eb12c3e49748`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Sat, 07 Mar 2026 00:34:25 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Mar 2026 00:34:26 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Mar 2026 00:37:29 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:37:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:37:29 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:37:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:37:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:37:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:37:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:37:29 GMT
USER memcache
# Sat, 07 Mar 2026 00:37:29 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:37:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18dad4d028ff2b78314498b57b872634656cb70add272a07cde87477543ea34b`  
		Last Modified: Sat, 07 Mar 2026 00:37:33 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5343ac0baa24b86f7ffac4e0a3296276d4a7aa05b74617720244260e34dc5aba`  
		Last Modified: Sat, 07 Mar 2026 00:37:33 GMT  
		Size: 102.7 KB (102655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f65584616382b3a0c0b70214fd4046110bedf9cfbb2c2f89c2301372f8aa27`  
		Last Modified: Sat, 07 Mar 2026 00:37:33 GMT  
		Size: 1.9 MB (1940281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a378f9c04f9d21fc788013f2928b3637ad3724011b85ecb4d8fe5a61ca9bb2`  
		Last Modified: Sat, 07 Mar 2026 00:37:33 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9600d067846989777b70f754cdd61c2012197736201713e9b5ff3703b147be02`  
		Last Modified: Sat, 07 Mar 2026 00:37:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:1d36396e4f4bb90ed2d326fbc737d8ab225cf619e64f08c3ff0beaff000177ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e204629c18255bb70ea677237338842d7ed3a140e1ecbbc4b8d5727cafa1668e`

```dockerfile
```

-	Layers:
	-	`sha256:1ea1c312fb87cc4d7c73a561d98b13a1f13504625a2de3953101370977fc6745`  
		Last Modified: Sat, 07 Mar 2026 00:37:33 GMT  
		Size: 20.5 KB (20466 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:91fe29148d686af2a0fdc23ba01a1b272f4c6365fc45bc37d00d4687a0c41b1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5273746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a56ac817dd40669cbf75609948d0f6fc05e648f6453d8f9deba7740682f741f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Sat, 07 Mar 2026 00:37:41 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Mar 2026 00:37:42 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Mar 2026 00:40:39 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:40:39 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:40:39 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:40:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:40:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:40:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:40:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:40:39 GMT
USER memcache
# Sat, 07 Mar 2026 00:40:39 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:40:39 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a51b7877e94969180dbb0be219881bc9230f055057f9e3f4b65f1db0708689a`  
		Last Modified: Sat, 07 Mar 2026 00:40:44 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c32abf408db65abfcd3224db5db2abaa977bd3ce59942c389c73320a4051cc`  
		Last Modified: Sat, 07 Mar 2026 00:40:44 GMT  
		Size: 92.4 KB (92374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ddc29b1020998fb5a3b242cc4e45954bc53540a31017ab6a020f9dff807bd22`  
		Last Modified: Sat, 07 Mar 2026 00:40:44 GMT  
		Size: 1.9 MB (1898298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae00440f5f6fd5951552907706f8df3661315090758ede99bb2933aa3384040b`  
		Last Modified: Sat, 07 Mar 2026 00:40:44 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb70de481e3407c522658dfa65d701fde07648ab9b8c732379d8a92f44092a81`  
		Last Modified: Sat, 07 Mar 2026 00:40:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:073366e4d50888ea6d43868ab35c2a063ea12dc243105f0c614c4feaa55d0eda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c47e8e147c04b6fae9be2f9c70644395f05ac10516981d5f48aac87100f9aabf`

```dockerfile
```

-	Layers:
	-	`sha256:f128294dbb16b2300fe484115b6bd24498974e73ac8835f70a3dd5df2f3211cd`  
		Last Modified: Sat, 07 Mar 2026 00:40:44 GMT  
		Size: 94.3 KB (94291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad6c6671c716b1f4cb8882be9d7cee792a3b5a0500ba4330e4c34c83d3401a1c`  
		Last Modified: Sat, 07 Mar 2026 00:40:44 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:eeb1c0de2b6b33a7a724454aaf9fd945503a062302d133c059f1b829db991b61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6287490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0de2d8f866d91b49adb4cfa80ffd26e168ac627328864d7ceae76dfd0bc4d7a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Sat, 07 Mar 2026 00:36:34 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Mar 2026 00:36:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Mar 2026 00:39:22 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:39:22 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:39:22 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:39:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:39:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:39:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:39:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:39:22 GMT
USER memcache
# Sat, 07 Mar 2026 00:39:22 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:39:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d65cacaa69d1c76240e558dab714b69561f9bb333c2c1c147f9be7d6b29c36`  
		Last Modified: Sat, 07 Mar 2026 00:39:27 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca80346986e335b6e96f14599a1ab3629964fa8702f4570e2d199da8b04498e`  
		Last Modified: Sat, 07 Mar 2026 00:39:27 GMT  
		Size: 121.9 KB (121860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bcaaaf5541ab3a5d055204886aadf36871e66f535b6c1978b4b4c58a4dc2367`  
		Last Modified: Sat, 07 Mar 2026 00:39:27 GMT  
		Size: 2.0 MB (1967188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6167d1b1458d5cedc7774a2a1e9e621f5b32de851a6b19d82ea2275ec9f1bc5`  
		Last Modified: Sat, 07 Mar 2026 00:39:27 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2040432b455fd0270cf480396dc9c1570b8710e21539cc0110e13fe10105062`  
		Last Modified: Sat, 07 Mar 2026 00:39:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:3d8284de1f87be934ca3ad16b60f3a624262a50260f7f8db4cc80575af22e7c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9a54dfb1a405917a8fe0eaf03a1588913998eac5cacc5141cad5d053c6ba838`

```dockerfile
```

-	Layers:
	-	`sha256:8eefe1140db7c68e1990a3744cd3126838a63605758bc6825cb1c090277cf806`  
		Last Modified: Sat, 07 Mar 2026 00:39:27 GMT  
		Size: 94.3 KB (94327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92f28d8e0dd01f916858b48749b2827fadaadb7ca45a0a8a872ac9d74043589d`  
		Last Modified: Sat, 07 Mar 2026 00:39:27 GMT  
		Size: 20.7 KB (20728 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; 386

```console
$ docker pull memcached@sha256:006134e843d0ad5a3c64e903cc20d00c9f3e78a542fa3d6ba1e3ecec5b0ba3c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5742709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06188a4fb3481bcf32a3e44fca9d58ab763a52c65e02c95fbef5e98f4b78ee86`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Sat, 07 Mar 2026 00:37:00 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Mar 2026 00:37:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Mar 2026 00:39:49 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:39:49 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:39:49 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:39:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:39:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:39:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:39:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:39:50 GMT
USER memcache
# Sat, 07 Mar 2026 00:39:50 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:39:50 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ba4a2e327b273e788cfdef17b5c31ac5fefd6010584aa1c11b0d0104a041d6`  
		Last Modified: Sat, 07 Mar 2026 00:39:54 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ba4e8e1182330d5f76532f2f48fe38af386558e3e7fa4d94ce3dbf055be5ab`  
		Last Modified: Sat, 07 Mar 2026 00:39:54 GMT  
		Size: 110.7 KB (110732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01c1fe355d65277d08c7962b0be21d39386b4121b36381bbcb9a60d29449a5c`  
		Last Modified: Sat, 07 Mar 2026 00:39:54 GMT  
		Size: 1.9 MB (1943630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e102587e979593069cf080e59b8471ecf62f9c40abad1e62014f1742341827d0`  
		Last Modified: Sat, 07 Mar 2026 00:39:54 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46411b86935a4104c9cbb43c595a9cbf0e0330c814ca33c36935c5a9cb7f37d`  
		Last Modified: Sat, 07 Mar 2026 00:39:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:d0cb60f8d8c989514001fd52bf793673fa8f281758af2b58f8359d1d41973b11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58f3853067ae595d4075c459fe7b8361d199af21eaa1f93413e882c2e0bc9042`

```dockerfile
```

-	Layers:
	-	`sha256:2cd10df8bfae391e9a94e270083baf145ca51970a41e64ab71cd781740d00c73`  
		Last Modified: Sat, 07 Mar 2026 00:39:54 GMT  
		Size: 94.8 KB (94828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1d4f0d3116c96944777e5e4b1130eaff94973a8664033f37d3c60ceb36ed173`  
		Last Modified: Sat, 07 Mar 2026 00:39:54 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:35c354ed5e627574c294e54f0232ed89e8eacd7ed7e2670634db2396b8f2a39c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6034990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3da727092e7c56a19e8b1a382da13658524813ce0d2bca55dee5f4067987b77a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Sat, 07 Mar 2026 00:33:31 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Mar 2026 00:33:34 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Mar 2026 00:36:15 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:36:15 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:36:15 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:36:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:36:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:36:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:36:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:36:16 GMT
USER memcache
# Sat, 07 Mar 2026 00:36:16 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:36:16 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364a7d7b961599919f81b228a22514e1935e6774971d671f38dbad14ef71cbfd`  
		Last Modified: Sat, 07 Mar 2026 00:36:29 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d77d50c27f0ae298d21083636544fb7f795b9708dc480f081e1e936f1246e7`  
		Last Modified: Sat, 07 Mar 2026 00:36:29 GMT  
		Size: 126.3 KB (126266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d559c6185e0bba610ac4ee55bed1b0d85afdad6f054f17906fadb6311cc44007`  
		Last Modified: Sat, 07 Mar 2026 00:36:29 GMT  
		Size: 2.1 MB (2077727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce553e1c7553a28f652dbbd9f3d79596edea9eecf47883032057409cd1d977f`  
		Last Modified: Sat, 07 Mar 2026 00:36:29 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf30d9d84b197d47332200b954fc9fcedf3653c9a44fe6b72a5cf721ec170f1`  
		Last Modified: Sat, 07 Mar 2026 00:36:30 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7c60879107d9d8ce6f5e597f4c108df4a413d312eaf52e4c9303b96e80e84fbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eee93b7e24e493f45076a5a793e8b01aad30e3643bcb7583bc1fa26a1c4ff826`

```dockerfile
```

-	Layers:
	-	`sha256:b4505eef72239eda1b1c608b3226cd19dc02c372be606494a473db623050489a`  
		Last Modified: Sat, 07 Mar 2026 00:36:29 GMT  
		Size: 94.3 KB (94280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43cc72cbc203c87b12cbef8914fb2835a461df6bb0445da26d96b5a14e610184`  
		Last Modified: Sat, 07 Mar 2026 00:36:29 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:874942dd4e337f828a5480fa7e7e03b28951302101475540a14d752215e0b99e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5771014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61e6da61960009cb5e1d5f173422857994cb30b45c987fc35062485420c05ddf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 11 Mar 2026 21:21:50 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 11 Mar 2026 21:21:54 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 11 Mar 2026 21:35:15 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 11 Mar 2026 21:35:15 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 11 Mar 2026 21:35:15 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 11 Mar 2026 21:35:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 11 Mar 2026 21:35:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 11 Mar 2026 21:35:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 11 Mar 2026 21:35:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2026 21:35:16 GMT
USER memcache
# Wed, 11 Mar 2026 21:35:16 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 11 Mar 2026 21:35:16 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63b25af376cdb2cb3ddbdf009ec368c61af0677da2ff36f56052ba87ef9d03e`  
		Last Modified: Wed, 11 Mar 2026 21:35:39 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efcf2b36003649471638502666fa028dd48ae26bf7a732d6d7fe38a8432a7016`  
		Last Modified: Wed, 11 Mar 2026 21:35:39 GMT  
		Size: 108.9 KB (108902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddaf732ffb5731ec8232eec8940c917de4727564501c45fce52a7e2ebd641224`  
		Last Modified: Wed, 11 Mar 2026 21:35:40 GMT  
		Size: 2.1 MB (2075471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91cabf0fbda848cc214b782cee7c5c7224ddb7674e75de41599a3bbe85d6a689`  
		Last Modified: Wed, 11 Mar 2026 21:35:39 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:306ecccaa7e256f58e1e772b44b962766fdf35f118efb1596b4c9ae2431987ab`  
		Last Modified: Wed, 11 Mar 2026 21:35:40 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:5e6d73b60a6ccb5dda56fc4d483b45097e7ef55ce412da110e15c6c478c8d882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebcfe45486057ddd0b85095c8ca2fd1a8656b95e8ecf579e4de8717551ada915`

```dockerfile
```

-	Layers:
	-	`sha256:7176cf6ddf61d50975dee6f26ce9fdcb0b77085375b0dde58bb44b8337adca94`  
		Last Modified: Wed, 11 Mar 2026 21:35:39 GMT  
		Size: 94.3 KB (94276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5799ace3d1f3a380e60d9e9676ffbd335daf84ded3af9d5e1dd8ce83eee2060`  
		Last Modified: Wed, 11 Mar 2026 21:35:39 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; s390x

```console
$ docker pull memcached@sha256:9c94884aa3d27f0c0ed5df500b79a6f3c2685bba5c632e3b871c0a262314d935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5858795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cd8a0886a7efaab4d69edd3b15f2a68384bcfdb1ff1a454930ba3a6a6ba29fc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Sat, 07 Mar 2026 00:33:34 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Mar 2026 00:33:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Mar 2026 00:36:49 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:36:49 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:36:49 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:36:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:36:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:36:49 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:36:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:36:49 GMT
USER memcache
# Sat, 07 Mar 2026 00:36:49 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:36:49 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f0d8799f878cf05935221d46a9b462122587e33ba748e54c983e03bbcb7ad2`  
		Last Modified: Sat, 07 Mar 2026 00:36:57 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef440db2f09493c5c9eae06dd0e59dafbd4761a74731e3ffa8ac968dcca712ca`  
		Last Modified: Sat, 07 Mar 2026 00:36:57 GMT  
		Size: 114.3 KB (114309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:134d34534319282a3e54d23ff3c63c0362a6c2ba38fb854b6a94a202d67347c2`  
		Last Modified: Sat, 07 Mar 2026 00:36:57 GMT  
		Size: 2.0 MB (2017802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:655653db981f7dce0174439408f99d0c480cb5082436a0682568bdaab190cd39`  
		Last Modified: Sat, 07 Mar 2026 00:36:57 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92dd0a7cdddba4f0415d5e0b6aa52c11369fa65b7c8c4ae965c949d55e7d52dd`  
		Last Modified: Sat, 07 Mar 2026 00:36:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:b9dd2a68695665b98af82b5110aa7af831b2d15654c26ffd200cc198ac79fb69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29c28af5a544343faaa1ff91b74bb776f4c5013c23bc2f45a2bbadb0fa1acc12`

```dockerfile
```

-	Layers:
	-	`sha256:47a88819c43763550a569259221f913c63dfd51ac45adc283170d20d81240959`  
		Last Modified: Sat, 07 Mar 2026 00:36:57 GMT  
		Size: 94.2 KB (94222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a9409046e85d857b00aa1f263c8c811160eeaa0c58b29abf61985c657289659`  
		Last Modified: Sat, 07 Mar 2026 00:36:57 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine3.23`

```console
$ docker pull memcached@sha256:1c6a2d48c5f561226f1dc54ed37132f83b4cde94b5e3f3e2d88386d028b86a27
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
$ docker pull memcached@sha256:84dd21b0c8ebc30032a8aaa7270c7e6c11da52efd7bf3c7593530168946d3bd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5959699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaf5f46bdf2c26a9dda97cd7dd2b6a05c5d8135b2f9cbacf33ff8e8365f5e1eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Sat, 07 Mar 2026 00:36:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Mar 2026 00:36:14 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Mar 2026 00:38:52 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:38:52 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:38:52 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:38:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:38:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:38:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:38:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:38:52 GMT
USER memcache
# Sat, 07 Mar 2026 00:38:52 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:38:52 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d055707374a501222192f988c0ff35fcfdc5a017dd49a48e1dd38106c605f400`  
		Last Modified: Sat, 07 Mar 2026 00:38:57 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5abb10c57422a10d35029047d7b017a29437bc0081f375524cbfb3db3c9eaf9`  
		Last Modified: Sat, 07 Mar 2026 00:38:57 GMT  
		Size: 106.1 KB (106057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4fd18d57089d5254541b428a6a2429569ff07d571c824af865b666901af275e`  
		Last Modified: Sat, 07 Mar 2026 00:38:57 GMT  
		Size: 2.0 MB (1990468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885d9eb83efad8e7a74f165d5e00bd1e547b62348f4084f8748eb5123cfd5ef2`  
		Last Modified: Sat, 07 Mar 2026 00:38:57 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32954341fb1b6227e3bb596d1a3f58beb03c348455e63c0e6a810197d1922e9`  
		Last Modified: Sat, 07 Mar 2026 00:38:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:e0615e85e00302f3ab01f14593cf39cf7e4ac01f448e6904dd61247bf63b3ff0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3b92ada03392c40180327b1e82f1b29a80b1164d4b65115558c1efc811142ad`

```dockerfile
```

-	Layers:
	-	`sha256:cc3e65e74aa6c619611c020b3d498d3c756e6168a9b26434ca30c3099cfa3261`  
		Last Modified: Sat, 07 Mar 2026 00:38:57 GMT  
		Size: 94.9 KB (94873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:327a47bce4975ea9e581754831550ac249839dc3708d4841f78ebc6cbd78d014`  
		Last Modified: Sat, 07 Mar 2026 00:38:57 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.23` - linux; arm variant v6

```console
$ docker pull memcached@sha256:6cde7ea7574023751e83c90e1e8f1f7aef03c1d5b0fbe20a17d981d57edb99dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:376e43ecede029f4d02a7634c75d3107a5797f724660eb9b02b0eb12c3e49748`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Sat, 07 Mar 2026 00:34:25 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Mar 2026 00:34:26 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Mar 2026 00:37:29 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:37:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:37:29 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:37:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:37:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:37:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:37:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:37:29 GMT
USER memcache
# Sat, 07 Mar 2026 00:37:29 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:37:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18dad4d028ff2b78314498b57b872634656cb70add272a07cde87477543ea34b`  
		Last Modified: Sat, 07 Mar 2026 00:37:33 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5343ac0baa24b86f7ffac4e0a3296276d4a7aa05b74617720244260e34dc5aba`  
		Last Modified: Sat, 07 Mar 2026 00:37:33 GMT  
		Size: 102.7 KB (102655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f65584616382b3a0c0b70214fd4046110bedf9cfbb2c2f89c2301372f8aa27`  
		Last Modified: Sat, 07 Mar 2026 00:37:33 GMT  
		Size: 1.9 MB (1940281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a378f9c04f9d21fc788013f2928b3637ad3724011b85ecb4d8fe5a61ca9bb2`  
		Last Modified: Sat, 07 Mar 2026 00:37:33 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9600d067846989777b70f754cdd61c2012197736201713e9b5ff3703b147be02`  
		Last Modified: Sat, 07 Mar 2026 00:37:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:1d36396e4f4bb90ed2d326fbc737d8ab225cf619e64f08c3ff0beaff000177ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e204629c18255bb70ea677237338842d7ed3a140e1ecbbc4b8d5727cafa1668e`

```dockerfile
```

-	Layers:
	-	`sha256:1ea1c312fb87cc4d7c73a561d98b13a1f13504625a2de3953101370977fc6745`  
		Last Modified: Sat, 07 Mar 2026 00:37:33 GMT  
		Size: 20.5 KB (20466 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.23` - linux; arm variant v7

```console
$ docker pull memcached@sha256:91fe29148d686af2a0fdc23ba01a1b272f4c6365fc45bc37d00d4687a0c41b1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5273746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a56ac817dd40669cbf75609948d0f6fc05e648f6453d8f9deba7740682f741f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Sat, 07 Mar 2026 00:37:41 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Mar 2026 00:37:42 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Mar 2026 00:40:39 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:40:39 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:40:39 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:40:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:40:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:40:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:40:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:40:39 GMT
USER memcache
# Sat, 07 Mar 2026 00:40:39 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:40:39 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a51b7877e94969180dbb0be219881bc9230f055057f9e3f4b65f1db0708689a`  
		Last Modified: Sat, 07 Mar 2026 00:40:44 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c32abf408db65abfcd3224db5db2abaa977bd3ce59942c389c73320a4051cc`  
		Last Modified: Sat, 07 Mar 2026 00:40:44 GMT  
		Size: 92.4 KB (92374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ddc29b1020998fb5a3b242cc4e45954bc53540a31017ab6a020f9dff807bd22`  
		Last Modified: Sat, 07 Mar 2026 00:40:44 GMT  
		Size: 1.9 MB (1898298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae00440f5f6fd5951552907706f8df3661315090758ede99bb2933aa3384040b`  
		Last Modified: Sat, 07 Mar 2026 00:40:44 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb70de481e3407c522658dfa65d701fde07648ab9b8c732379d8a92f44092a81`  
		Last Modified: Sat, 07 Mar 2026 00:40:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:073366e4d50888ea6d43868ab35c2a063ea12dc243105f0c614c4feaa55d0eda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c47e8e147c04b6fae9be2f9c70644395f05ac10516981d5f48aac87100f9aabf`

```dockerfile
```

-	Layers:
	-	`sha256:f128294dbb16b2300fe484115b6bd24498974e73ac8835f70a3dd5df2f3211cd`  
		Last Modified: Sat, 07 Mar 2026 00:40:44 GMT  
		Size: 94.3 KB (94291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad6c6671c716b1f4cb8882be9d7cee792a3b5a0500ba4330e4c34c83d3401a1c`  
		Last Modified: Sat, 07 Mar 2026 00:40:44 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.23` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:eeb1c0de2b6b33a7a724454aaf9fd945503a062302d133c059f1b829db991b61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6287490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0de2d8f866d91b49adb4cfa80ffd26e168ac627328864d7ceae76dfd0bc4d7a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Sat, 07 Mar 2026 00:36:34 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Mar 2026 00:36:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Mar 2026 00:39:22 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:39:22 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:39:22 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:39:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:39:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:39:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:39:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:39:22 GMT
USER memcache
# Sat, 07 Mar 2026 00:39:22 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:39:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d65cacaa69d1c76240e558dab714b69561f9bb333c2c1c147f9be7d6b29c36`  
		Last Modified: Sat, 07 Mar 2026 00:39:27 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca80346986e335b6e96f14599a1ab3629964fa8702f4570e2d199da8b04498e`  
		Last Modified: Sat, 07 Mar 2026 00:39:27 GMT  
		Size: 121.9 KB (121860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bcaaaf5541ab3a5d055204886aadf36871e66f535b6c1978b4b4c58a4dc2367`  
		Last Modified: Sat, 07 Mar 2026 00:39:27 GMT  
		Size: 2.0 MB (1967188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6167d1b1458d5cedc7774a2a1e9e621f5b32de851a6b19d82ea2275ec9f1bc5`  
		Last Modified: Sat, 07 Mar 2026 00:39:27 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2040432b455fd0270cf480396dc9c1570b8710e21539cc0110e13fe10105062`  
		Last Modified: Sat, 07 Mar 2026 00:39:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:3d8284de1f87be934ca3ad16b60f3a624262a50260f7f8db4cc80575af22e7c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9a54dfb1a405917a8fe0eaf03a1588913998eac5cacc5141cad5d053c6ba838`

```dockerfile
```

-	Layers:
	-	`sha256:8eefe1140db7c68e1990a3744cd3126838a63605758bc6825cb1c090277cf806`  
		Last Modified: Sat, 07 Mar 2026 00:39:27 GMT  
		Size: 94.3 KB (94327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92f28d8e0dd01f916858b48749b2827fadaadb7ca45a0a8a872ac9d74043589d`  
		Last Modified: Sat, 07 Mar 2026 00:39:27 GMT  
		Size: 20.7 KB (20728 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.23` - linux; 386

```console
$ docker pull memcached@sha256:006134e843d0ad5a3c64e903cc20d00c9f3e78a542fa3d6ba1e3ecec5b0ba3c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5742709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06188a4fb3481bcf32a3e44fca9d58ab763a52c65e02c95fbef5e98f4b78ee86`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Sat, 07 Mar 2026 00:37:00 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Mar 2026 00:37:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Mar 2026 00:39:49 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:39:49 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:39:49 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:39:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:39:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:39:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:39:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:39:50 GMT
USER memcache
# Sat, 07 Mar 2026 00:39:50 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:39:50 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ba4a2e327b273e788cfdef17b5c31ac5fefd6010584aa1c11b0d0104a041d6`  
		Last Modified: Sat, 07 Mar 2026 00:39:54 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ba4e8e1182330d5f76532f2f48fe38af386558e3e7fa4d94ce3dbf055be5ab`  
		Last Modified: Sat, 07 Mar 2026 00:39:54 GMT  
		Size: 110.7 KB (110732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01c1fe355d65277d08c7962b0be21d39386b4121b36381bbcb9a60d29449a5c`  
		Last Modified: Sat, 07 Mar 2026 00:39:54 GMT  
		Size: 1.9 MB (1943630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e102587e979593069cf080e59b8471ecf62f9c40abad1e62014f1742341827d0`  
		Last Modified: Sat, 07 Mar 2026 00:39:54 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46411b86935a4104c9cbb43c595a9cbf0e0330c814ca33c36935c5a9cb7f37d`  
		Last Modified: Sat, 07 Mar 2026 00:39:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:d0cb60f8d8c989514001fd52bf793673fa8f281758af2b58f8359d1d41973b11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58f3853067ae595d4075c459fe7b8361d199af21eaa1f93413e882c2e0bc9042`

```dockerfile
```

-	Layers:
	-	`sha256:2cd10df8bfae391e9a94e270083baf145ca51970a41e64ab71cd781740d00c73`  
		Last Modified: Sat, 07 Mar 2026 00:39:54 GMT  
		Size: 94.8 KB (94828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1d4f0d3116c96944777e5e4b1130eaff94973a8664033f37d3c60ceb36ed173`  
		Last Modified: Sat, 07 Mar 2026 00:39:54 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.23` - linux; ppc64le

```console
$ docker pull memcached@sha256:35c354ed5e627574c294e54f0232ed89e8eacd7ed7e2670634db2396b8f2a39c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6034990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3da727092e7c56a19e8b1a382da13658524813ce0d2bca55dee5f4067987b77a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Sat, 07 Mar 2026 00:33:31 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Mar 2026 00:33:34 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Mar 2026 00:36:15 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:36:15 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:36:15 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:36:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:36:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:36:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:36:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:36:16 GMT
USER memcache
# Sat, 07 Mar 2026 00:36:16 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:36:16 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364a7d7b961599919f81b228a22514e1935e6774971d671f38dbad14ef71cbfd`  
		Last Modified: Sat, 07 Mar 2026 00:36:29 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d77d50c27f0ae298d21083636544fb7f795b9708dc480f081e1e936f1246e7`  
		Last Modified: Sat, 07 Mar 2026 00:36:29 GMT  
		Size: 126.3 KB (126266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d559c6185e0bba610ac4ee55bed1b0d85afdad6f054f17906fadb6311cc44007`  
		Last Modified: Sat, 07 Mar 2026 00:36:29 GMT  
		Size: 2.1 MB (2077727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce553e1c7553a28f652dbbd9f3d79596edea9eecf47883032057409cd1d977f`  
		Last Modified: Sat, 07 Mar 2026 00:36:29 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf30d9d84b197d47332200b954fc9fcedf3653c9a44fe6b72a5cf721ec170f1`  
		Last Modified: Sat, 07 Mar 2026 00:36:30 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:7c60879107d9d8ce6f5e597f4c108df4a413d312eaf52e4c9303b96e80e84fbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eee93b7e24e493f45076a5a793e8b01aad30e3643bcb7583bc1fa26a1c4ff826`

```dockerfile
```

-	Layers:
	-	`sha256:b4505eef72239eda1b1c608b3226cd19dc02c372be606494a473db623050489a`  
		Last Modified: Sat, 07 Mar 2026 00:36:29 GMT  
		Size: 94.3 KB (94280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43cc72cbc203c87b12cbef8914fb2835a461df6bb0445da26d96b5a14e610184`  
		Last Modified: Sat, 07 Mar 2026 00:36:29 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.23` - linux; riscv64

```console
$ docker pull memcached@sha256:874942dd4e337f828a5480fa7e7e03b28951302101475540a14d752215e0b99e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5771014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61e6da61960009cb5e1d5f173422857994cb30b45c987fc35062485420c05ddf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 11 Mar 2026 21:21:50 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 11 Mar 2026 21:21:54 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 11 Mar 2026 21:35:15 GMT
ENV MEMCACHED_VERSION=1.6.41
# Wed, 11 Mar 2026 21:35:15 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Wed, 11 Mar 2026 21:35:15 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Wed, 11 Mar 2026 21:35:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 11 Mar 2026 21:35:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 11 Mar 2026 21:35:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 11 Mar 2026 21:35:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2026 21:35:16 GMT
USER memcache
# Wed, 11 Mar 2026 21:35:16 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 11 Mar 2026 21:35:16 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63b25af376cdb2cb3ddbdf009ec368c61af0677da2ff36f56052ba87ef9d03e`  
		Last Modified: Wed, 11 Mar 2026 21:35:39 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efcf2b36003649471638502666fa028dd48ae26bf7a732d6d7fe38a8432a7016`  
		Last Modified: Wed, 11 Mar 2026 21:35:39 GMT  
		Size: 108.9 KB (108902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddaf732ffb5731ec8232eec8940c917de4727564501c45fce52a7e2ebd641224`  
		Last Modified: Wed, 11 Mar 2026 21:35:40 GMT  
		Size: 2.1 MB (2075471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91cabf0fbda848cc214b782cee7c5c7224ddb7674e75de41599a3bbe85d6a689`  
		Last Modified: Wed, 11 Mar 2026 21:35:39 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:306ecccaa7e256f58e1e772b44b962766fdf35f118efb1596b4c9ae2431987ab`  
		Last Modified: Wed, 11 Mar 2026 21:35:40 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:5e6d73b60a6ccb5dda56fc4d483b45097e7ef55ce412da110e15c6c478c8d882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebcfe45486057ddd0b85095c8ca2fd1a8656b95e8ecf579e4de8717551ada915`

```dockerfile
```

-	Layers:
	-	`sha256:7176cf6ddf61d50975dee6f26ce9fdcb0b77085375b0dde58bb44b8337adca94`  
		Last Modified: Wed, 11 Mar 2026 21:35:39 GMT  
		Size: 94.3 KB (94276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5799ace3d1f3a380e60d9e9676ffbd335daf84ded3af9d5e1dd8ce83eee2060`  
		Last Modified: Wed, 11 Mar 2026 21:35:39 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.23` - linux; s390x

```console
$ docker pull memcached@sha256:9c94884aa3d27f0c0ed5df500b79a6f3c2685bba5c632e3b871c0a262314d935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5858795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cd8a0886a7efaab4d69edd3b15f2a68384bcfdb1ff1a454930ba3a6a6ba29fc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Sat, 07 Mar 2026 00:33:34 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Mar 2026 00:33:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Mar 2026 00:36:49 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:36:49 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:36:49 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:36:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:36:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:36:49 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:36:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:36:49 GMT
USER memcache
# Sat, 07 Mar 2026 00:36:49 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:36:49 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f0d8799f878cf05935221d46a9b462122587e33ba748e54c983e03bbcb7ad2`  
		Last Modified: Sat, 07 Mar 2026 00:36:57 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef440db2f09493c5c9eae06dd0e59dafbd4761a74731e3ffa8ac968dcca712ca`  
		Last Modified: Sat, 07 Mar 2026 00:36:57 GMT  
		Size: 114.3 KB (114309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:134d34534319282a3e54d23ff3c63c0362a6c2ba38fb854b6a94a202d67347c2`  
		Last Modified: Sat, 07 Mar 2026 00:36:57 GMT  
		Size: 2.0 MB (2017802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:655653db981f7dce0174439408f99d0c480cb5082436a0682568bdaab190cd39`  
		Last Modified: Sat, 07 Mar 2026 00:36:57 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92dd0a7cdddba4f0415d5e0b6aa52c11369fa65b7c8c4ae965c949d55e7d52dd`  
		Last Modified: Sat, 07 Mar 2026 00:36:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:b9dd2a68695665b98af82b5110aa7af831b2d15654c26ffd200cc198ac79fb69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29c28af5a544343faaa1ff91b74bb776f4c5013c23bc2f45a2bbadb0fa1acc12`

```dockerfile
```

-	Layers:
	-	`sha256:47a88819c43763550a569259221f913c63dfd51ac45adc283170d20d81240959`  
		Last Modified: Sat, 07 Mar 2026 00:36:57 GMT  
		Size: 94.2 KB (94222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a9409046e85d857b00aa1f263c8c811160eeaa0c58b29abf61985c657289659`  
		Last Modified: Sat, 07 Mar 2026 00:36:57 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:latest`

```console
$ docker pull memcached@sha256:d99136ed4c1cf2e3fceb498763f2b7fedec7c486a0fe8a57be19f2a0519ce1fa
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
$ docker pull memcached@sha256:c08df224e6ccee2c893ac468902a8b68d8221910014da88f892d483b145f2e80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32197142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc0c289673d3b6f117607d5014b52d276fa02ad622404df04deac38f7a3b2b75`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Sat, 07 Mar 2026 00:34:28 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Mar 2026 00:34:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Mar 2026 00:37:16 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:37:16 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:37:16 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:37:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:37:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:37:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:37:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:37:16 GMT
USER memcache
# Sat, 07 Mar 2026 00:37:16 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:37:16 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65546826072afb14e8706d66b636911c885382731f6d325cba605469fdb363e7`  
		Last Modified: Sat, 07 Mar 2026 00:37:23 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f84d4f33fb93823aaef11588c633186a7b4c7e9c0fea6cf0c2c2e912be6b9f`  
		Last Modified: Sat, 07 Mar 2026 00:37:23 GMT  
		Size: 136.7 KB (136684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f30a00378f01ca7716c334349799965f472572c2377432ae0948fb3481a330`  
		Last Modified: Sat, 07 Mar 2026 00:37:23 GMT  
		Size: 2.3 MB (2280310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd736c12c1d448b0585c460fd3f417da3a21193665ef2aefd67c221cbd97df0b`  
		Last Modified: Sat, 07 Mar 2026 00:37:23 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f072b1e28c7bdff147ef49013b08dfe871999faec678a4219890f645e2d14b`  
		Last Modified: Sat, 07 Mar 2026 00:37:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:b0cd4839975a3f144a6d44260b40e6cebfaad48ae0dabae69c8a84a1912f55ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d69fb1b8b08633539bde084818362e1b13aae93417c6fc42c6c674e4039d2ab4`

```dockerfile
```

-	Layers:
	-	`sha256:0bc9fc51640e8d0b171e44a65462e97d0e54980aca3e0ea45f57320911a0f07c`  
		Last Modified: Sat, 07 Mar 2026 00:37:23 GMT  
		Size: 2.0 MB (2008290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2632163ed214b82be06d84daacb113b153e4ec7def67cd764cb771fb9700aeaf`  
		Last Modified: Sat, 07 Mar 2026 00:37:23 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm variant v5

```console
$ docker pull memcached@sha256:514cbf94b5380f36ac3c88108bf78a84ae83c3ed26e638ebe2e2f5bb88bd25ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30304774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc4d63874316ce18eaa26acb02c5e3dc129e31ea8c480a3a966621c75552572c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1771804800'
# Sat, 07 Mar 2026 00:34:25 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Mar 2026 00:34:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Mar 2026 00:37:50 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:37:50 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:37:50 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:37:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:37:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:37:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:37:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:37:50 GMT
USER memcache
# Sat, 07 Mar 2026 00:37:50 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:37:50 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:280a075cc1d2a97445b9f4430aa9774bfc38fc4217b7fc9d6a7b04e7e431cb65`  
		Last Modified: Tue, 24 Feb 2026 18:42:44 GMT  
		Size: 27.9 MB (27947608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fee55b7ab1f18dde561acdb3246640b49ed746f0a6f679b8b4be2fe96c38edc`  
		Last Modified: Sat, 07 Mar 2026 00:37:56 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e90ce24e8e18d6e22b1819e0c183af55656f28a490d2a5f5db1bb199759ae2`  
		Last Modified: Sat, 07 Mar 2026 00:37:56 GMT  
		Size: 144.2 KB (144173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e14eaa4ef07ee7a2796a97655630e5b528d0f2f8120ba62ac860fcf148e2b813`  
		Last Modified: Sat, 07 Mar 2026 00:37:56 GMT  
		Size: 2.2 MB (2211477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0271cbc419600dba0091ae986cd78ada6340afbfa697b93993e1f63555a831`  
		Last Modified: Sat, 07 Mar 2026 00:37:56 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ecc8023e8fc75e87c4b1fc32230e35e765d671345bd42f98dfe13b7118bc13`  
		Last Modified: Sat, 07 Mar 2026 00:37:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:3b41b0fb30672979494c2bcc11e11de72d662cbeef4e097e83bf3637c45aba4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b344e75a26fbd848f3d4bda6dfbc82971e7c99f16f8b8d3c2f4e0046b3e36cf`

```dockerfile
```

-	Layers:
	-	`sha256:a8abf2c9952faed7ee6a8484d94c195f2f516d28b4aa99d61fde6a938373ef14`  
		Last Modified: Sat, 07 Mar 2026 00:37:56 GMT  
		Size: 2.0 MB (2011293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4baff3ba9a329e3fdeaee0149357b33f76e181413fc6e5b4d1b9502670d8aab3`  
		Last Modified: Sat, 07 Mar 2026 00:37:56 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm variant v7

```console
$ docker pull memcached@sha256:5e39383d269092b745c7426583a0849917817a2861226858ff17c34f227cadc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28515640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4d89f2522b7f402debcdfe4ae5ef33ccc13694e72756aabd8c894fd1a657663`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Sat, 07 Mar 2026 00:34:26 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Mar 2026 00:34:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Mar 2026 00:37:36 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:37:36 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:37:36 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:37:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:37:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:37:37 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:37:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:37:37 GMT
USER memcache
# Sat, 07 Mar 2026 00:37:37 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:37:37 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b5f623d77fff35b334b15c7b208113b4b778a70ce39168e1270421140984e6`  
		Last Modified: Sat, 07 Mar 2026 00:37:43 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d378422d428b98928a2c392598ff24dddba86412c764099339db2c9b84dab7`  
		Last Modified: Sat, 07 Mar 2026 00:37:43 GMT  
		Size: 135.4 KB (135371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ebe7571649e14f8ae60c2aa9c7464f120d47deb28852880adc72f5958fb268`  
		Last Modified: Sat, 07 Mar 2026 00:37:43 GMT  
		Size: 2.2 MB (2165006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab8a97091ab7e05c0561d93041f6833b293ec83a81c5cd316d914c7cd4797f5`  
		Last Modified: Sat, 07 Mar 2026 00:37:43 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06917ca5c3af99a9a619b7c0077abf8521b0777d4c07464889139b6030aaa445`  
		Last Modified: Sat, 07 Mar 2026 00:37:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:17c7cd3931d1614e411d593e6027c70049d32dd6b78b4523f5e29ff13b7b1f21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b42f736130d7735ab6bde638b9206c6be06a848c316aa0776562b9d2b05634b5`

```dockerfile
```

-	Layers:
	-	`sha256:1700f9d32fecaf2a6fff6e275b9eac8036467ba4e592635351cf279712b2017b`  
		Last Modified: Sat, 07 Mar 2026 00:37:43 GMT  
		Size: 2.0 MB (2009750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef3320ccea4ba2f43dfdeb26388b30f9251a45c8b87522656d05eb856e022fa0`  
		Last Modified: Sat, 07 Mar 2026 00:37:43 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:03ff213526efc235b60a048b3efa0c67c6d697a62bdc207561fb8ee00f254f89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32557234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4742c51756a2139de24009e1c754635923a703d67706387249d261e4dc62712`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Sat, 07 Mar 2026 00:34:23 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Mar 2026 00:34:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Mar 2026 00:37:25 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:37:25 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:37:25 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:37:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:37:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:37:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:37:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:37:25 GMT
USER memcache
# Sat, 07 Mar 2026 00:37:25 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:37:25 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:461d33f62f9a4e4fbc09492d8ce59e548e8c794e3122411c5f7a8370f2bbedba`  
		Last Modified: Sat, 07 Mar 2026 00:37:31 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e642309aa5a12065d7f985c382b7658fa51b45c2a111039cdb9b7240299809e7`  
		Last Modified: Sat, 07 Mar 2026 00:37:31 GMT  
		Size: 153.5 KB (153496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c81e14adafcb230598de8ae3eaf03443a9ae10bd04e616ae4ab64a2f379a48d`  
		Last Modified: Sat, 07 Mar 2026 00:37:31 GMT  
		Size: 2.3 MB (2262125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62e12af1edbdc302c3fd82e9561c5eac5def3110b53dc9d527b277d70a0c5b0`  
		Last Modified: Sat, 07 Mar 2026 00:37:31 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eee7fdafd6f634c0431e5a06be62ff9a726cb1fa8367483d6b026fa3164c7f0`  
		Last Modified: Sat, 07 Mar 2026 00:37:32 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:f791266a2bf814187fed117fa0abd604df8d26056d2e2791b51eb537a958de3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e7b8f74c70d2427388103547caa9c90ef2b4ec4ee11ce197e642593e10f6979`

```dockerfile
```

-	Layers:
	-	`sha256:88d9544d6eb9588edcaeabdc26922a9afb53b2222e8f9972e5b4b52199893738`  
		Last Modified: Sat, 07 Mar 2026 00:37:31 GMT  
		Size: 2.0 MB (2008606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b245266f3e6e113152f086489529a68f1c8c229363d9b678823c16250c48131`  
		Last Modified: Sat, 07 Mar 2026 00:37:31 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; 386

```console
$ docker pull memcached@sha256:1219e49a37eb8fa43f5cabcda7eb69df920734c5d615f2fc63e4fba52a06dfd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33667722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d141db22d43d8c6503a206b3413976c2fd0b84654a45bb46a3da3f39594ee93e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1771804800'
# Sat, 07 Mar 2026 00:34:41 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Mar 2026 00:34:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Mar 2026 00:37:41 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:37:41 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:37:41 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:37:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:37:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:37:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:37:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:37:41 GMT
USER memcache
# Sat, 07 Mar 2026 00:37:41 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:37:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f4e0b944ee1e7e50bdfbfa77bda370b6eccee7d698a7adca78c38f5ca0767ca5`  
		Last Modified: Tue, 24 Feb 2026 18:43:18 GMT  
		Size: 31.3 MB (31293918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d38eff546890db9ae0646486b61a548d8067820adc96ceb6eb4f5d7c2206bb8`  
		Last Modified: Sat, 07 Mar 2026 00:37:47 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c454125cf8ccd03f95714478c13c1d671ba0807b980ee5e6df450d611f61e156`  
		Last Modified: Sat, 07 Mar 2026 00:37:47 GMT  
		Size: 147.5 KB (147517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42b7d17f494cc1acab1da36a724a41a46ecf955d058123b89b170ea63bafda97`  
		Last Modified: Sat, 07 Mar 2026 00:37:47 GMT  
		Size: 2.2 MB (2224772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56fcaee4e2b815384392953fdf84278be4b9a4b116e3a5ad6436f7b13a7c6d9`  
		Last Modified: Sat, 07 Mar 2026 00:37:47 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6adacd7f3e38f46b44efa4ff006b35719382afa26b95b7a9b0c62ef7e7a01bfc`  
		Last Modified: Sat, 07 Mar 2026 00:37:48 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:9f65574f3294736b3dc217e4b07a4045282c517d258eaa96a32035e09cda6fa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb96fc147195e16ed2b6e99c3582cd8c6a67516fb0387c563d09fbf85f6a4dc0`

```dockerfile
```

-	Layers:
	-	`sha256:cdc74dec8f482313433fa0011e8531a8e816610bf31af8b63d2203318e8a59f9`  
		Last Modified: Sat, 07 Mar 2026 00:37:47 GMT  
		Size: 2.0 MB (2005447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bbcbbf7d1935fe3e711cd689ff38f789c3f7334bff2fd2518c106c4bf5d805f`  
		Last Modified: Sat, 07 Mar 2026 00:37:47 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; ppc64le

```console
$ docker pull memcached@sha256:ffac94778c7c882a7f2cbaae5af33e755639de207d07834e052412c2b22a24b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36754462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5640d71fb49b8eaef07631709a9f4924bd191fcfe9b44b7df2d525e247075b64`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Sat, 07 Mar 2026 00:33:31 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Mar 2026 00:33:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Mar 2026 00:56:42 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:56:42 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:56:42 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:56:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:56:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:56:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:56:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:56:44 GMT
USER memcache
# Sat, 07 Mar 2026 00:56:44 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:56:44 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab70996aa4a561e7f3e1f1e1b14df7912a1456b20b317937391cfa826c93f2ea`  
		Last Modified: Sat, 07 Mar 2026 00:57:10 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1ba00921effa53d91205ba3e5e3280c719885f49b5e9e0f8e2a387cf316d89`  
		Last Modified: Sat, 07 Mar 2026 00:57:10 GMT  
		Size: 170.4 KB (170386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd00738358190677470eca91b6732f6fcc475639b7f07f1943af6f5d268ae47`  
		Last Modified: Sat, 07 Mar 2026 00:57:10 GMT  
		Size: 3.0 MB (2982343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f7dc97a8f5d8c677e24bd2f8014c3e315619d726d409033dc3ce4f6d7d7569d`  
		Last Modified: Sat, 07 Mar 2026 00:57:10 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f2b48241128f09e1c613b0fb34d37f79c77417d033b7a00041f8cd08d6241f`  
		Last Modified: Sat, 07 Mar 2026 00:57:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:da557c745e92be8dd35823b9c24b79e47c55ff727768980abe9b659a14672408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e89b8bba62432d49e11baad935eddf449853276e5bb492953ae6bb995bf81ef`

```dockerfile
```

-	Layers:
	-	`sha256:7bf94ead3bca06412117cdc5395bde9d799ffc799dd28be779209634f64bfc0b`  
		Last Modified: Sat, 07 Mar 2026 00:57:10 GMT  
		Size: 2.0 MB (2011891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ec351466954789ecb039e735ecf9fd0235d5d4cfcf8bd6bcf2cf68049016c1c`  
		Last Modified: Sat, 07 Mar 2026 00:57:10 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; riscv64

```console
$ docker pull memcached@sha256:ccac0e143b4efd5bd15fb67df5ad87f5b743cc3db826cbb27d1874cbb3b6d549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30619564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f9320af1aa6fbbae22f81ef28d68694abc001739c71a195b4b1cd490b3b9107`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 23:50:36 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 09 Mar 2026 23:51:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Mar 2026 00:09:03 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 10 Mar 2026 00:09:03 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 10 Mar 2026 00:09:03 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 10 Mar 2026 00:09:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 10 Mar 2026 00:09:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 10 Mar 2026 00:09:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 10 Mar 2026 00:09:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Mar 2026 00:09:03 GMT
USER memcache
# Tue, 10 Mar 2026 00:09:03 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 10 Mar 2026 00:09:03 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e1366b1f74881f04901f31cfdecf9f3f5d4794ebf89911083a239bf462bf21`  
		Last Modified: Tue, 10 Mar 2026 00:09:56 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918782f8ab4ae7fe2ab9f1fc0aa7ad4e48d83dc362a4dcac336048ded3de9b6e`  
		Last Modified: Tue, 10 Mar 2026 00:09:56 GMT  
		Size: 133.1 KB (133079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963fbe1d00657987e81bdc270499ad5aacf8f91b100915c30ddf9fc57cd67346`  
		Last Modified: Tue, 10 Mar 2026 00:09:56 GMT  
		Size: 2.2 MB (2208551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729657786193241c665df2cbaeb72b5d157865abb3bbd8b9460e88d08fb65fea`  
		Last Modified: Tue, 10 Mar 2026 00:09:56 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8246f12fbc1ee94790a418b9655df55d80968171273b5994aaffa40c04fa2f3c`  
		Last Modified: Tue, 10 Mar 2026 00:09:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:de9f0d80a354763898649af4229a6f696fb51689e3b577af2e1d918d365777e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d72c30b80e1c2deaee38b267b52cab1a28e245b2a3608fcf459f2232dad3faa7`

```dockerfile
```

-	Layers:
	-	`sha256:03d9f11a7e8cf93ffe1f13ecfd86632a66af5a6efc142ae7a4ecac0c19418b2d`  
		Last Modified: Tue, 10 Mar 2026 00:09:56 GMT  
		Size: 2.0 MB (2002254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:452e3f764b5054c447aa8e63046155a20784d6f10159282ce633afdb79bf9279`  
		Last Modified: Tue, 10 Mar 2026 00:09:56 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; s390x

```console
$ docker pull memcached@sha256:8e1f3fb07bf1702ad27a7e2a6b2364e61d7b5165c113d0202db31adaa90d91df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32278340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1088ed36ed575f78d3e06fdd24f1ccdcc908d6e579970b2cae128c29f8d6e7a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Sat, 07 Mar 2026 00:33:32 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Mar 2026 00:33:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Mar 2026 00:36:51 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:36:51 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:36:51 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:36:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:36:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:36:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:36:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:36:51 GMT
USER memcache
# Sat, 07 Mar 2026 00:36:51 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:36:51 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986cc162f1a9b2f1b4c673da47497d87b8a542990f29c7823ee4d64cd160ea34`  
		Last Modified: Sat, 07 Mar 2026 00:37:00 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e3b516d24d039487b70f5d718d6f2b0c5473b5da4e6b82815239c7730587d6`  
		Last Modified: Sat, 07 Mar 2026 00:37:00 GMT  
		Size: 140.5 KB (140520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb611bdb547903f4763e52741be4c28e6ed0f172ebffc4ddae4e56a1a4d3ebc2`  
		Last Modified: Sat, 07 Mar 2026 00:37:00 GMT  
		Size: 2.3 MB (2298126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b32c7b8a27f2284141ba22bde8036a295b3e0d397cde405054e47e550cced01`  
		Last Modified: Sat, 07 Mar 2026 00:37:00 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3240387a49966ed4c1475913af7c7648c5499d01045e56e16637a760300918a`  
		Last Modified: Sat, 07 Mar 2026 00:37:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:b725149e071a1d02723f7674a5f7c477144350f79f2243558bce2360da7bf73b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:628ead940c50f3d4776c150c412d2270c2238893cfd1a57f8c17647ec35223e2`

```dockerfile
```

-	Layers:
	-	`sha256:b118af94ed9d10ab8f0c0221725860a15ff82dce98bd35abb240f411b745e0f7`  
		Last Modified: Sat, 07 Mar 2026 00:37:00 GMT  
		Size: 2.0 MB (2009727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:737fa51b5113fe89d161d6b7d0d81d66c28e666617dc1fb7c410b093ecf35625`  
		Last Modified: Sat, 07 Mar 2026 00:37:00 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:trixie`

```console
$ docker pull memcached@sha256:d99136ed4c1cf2e3fceb498763f2b7fedec7c486a0fe8a57be19f2a0519ce1fa
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
$ docker pull memcached@sha256:c08df224e6ccee2c893ac468902a8b68d8221910014da88f892d483b145f2e80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32197142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc0c289673d3b6f117607d5014b52d276fa02ad622404df04deac38f7a3b2b75`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Sat, 07 Mar 2026 00:34:28 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Mar 2026 00:34:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Mar 2026 00:37:16 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:37:16 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:37:16 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:37:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:37:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:37:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:37:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:37:16 GMT
USER memcache
# Sat, 07 Mar 2026 00:37:16 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:37:16 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65546826072afb14e8706d66b636911c885382731f6d325cba605469fdb363e7`  
		Last Modified: Sat, 07 Mar 2026 00:37:23 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f84d4f33fb93823aaef11588c633186a7b4c7e9c0fea6cf0c2c2e912be6b9f`  
		Last Modified: Sat, 07 Mar 2026 00:37:23 GMT  
		Size: 136.7 KB (136684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f30a00378f01ca7716c334349799965f472572c2377432ae0948fb3481a330`  
		Last Modified: Sat, 07 Mar 2026 00:37:23 GMT  
		Size: 2.3 MB (2280310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd736c12c1d448b0585c460fd3f417da3a21193665ef2aefd67c221cbd97df0b`  
		Last Modified: Sat, 07 Mar 2026 00:37:23 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f072b1e28c7bdff147ef49013b08dfe871999faec678a4219890f645e2d14b`  
		Last Modified: Sat, 07 Mar 2026 00:37:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:b0cd4839975a3f144a6d44260b40e6cebfaad48ae0dabae69c8a84a1912f55ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d69fb1b8b08633539bde084818362e1b13aae93417c6fc42c6c674e4039d2ab4`

```dockerfile
```

-	Layers:
	-	`sha256:0bc9fc51640e8d0b171e44a65462e97d0e54980aca3e0ea45f57320911a0f07c`  
		Last Modified: Sat, 07 Mar 2026 00:37:23 GMT  
		Size: 2.0 MB (2008290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2632163ed214b82be06d84daacb113b153e4ec7def67cd764cb771fb9700aeaf`  
		Last Modified: Sat, 07 Mar 2026 00:37:23 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; arm variant v5

```console
$ docker pull memcached@sha256:514cbf94b5380f36ac3c88108bf78a84ae83c3ed26e638ebe2e2f5bb88bd25ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30304774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc4d63874316ce18eaa26acb02c5e3dc129e31ea8c480a3a966621c75552572c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1771804800'
# Sat, 07 Mar 2026 00:34:25 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Mar 2026 00:34:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Mar 2026 00:37:50 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:37:50 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:37:50 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:37:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:37:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:37:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:37:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:37:50 GMT
USER memcache
# Sat, 07 Mar 2026 00:37:50 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:37:50 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:280a075cc1d2a97445b9f4430aa9774bfc38fc4217b7fc9d6a7b04e7e431cb65`  
		Last Modified: Tue, 24 Feb 2026 18:42:44 GMT  
		Size: 27.9 MB (27947608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fee55b7ab1f18dde561acdb3246640b49ed746f0a6f679b8b4be2fe96c38edc`  
		Last Modified: Sat, 07 Mar 2026 00:37:56 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e90ce24e8e18d6e22b1819e0c183af55656f28a490d2a5f5db1bb199759ae2`  
		Last Modified: Sat, 07 Mar 2026 00:37:56 GMT  
		Size: 144.2 KB (144173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e14eaa4ef07ee7a2796a97655630e5b528d0f2f8120ba62ac860fcf148e2b813`  
		Last Modified: Sat, 07 Mar 2026 00:37:56 GMT  
		Size: 2.2 MB (2211477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0271cbc419600dba0091ae986cd78ada6340afbfa697b93993e1f63555a831`  
		Last Modified: Sat, 07 Mar 2026 00:37:56 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ecc8023e8fc75e87c4b1fc32230e35e765d671345bd42f98dfe13b7118bc13`  
		Last Modified: Sat, 07 Mar 2026 00:37:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:3b41b0fb30672979494c2bcc11e11de72d662cbeef4e097e83bf3637c45aba4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b344e75a26fbd848f3d4bda6dfbc82971e7c99f16f8b8d3c2f4e0046b3e36cf`

```dockerfile
```

-	Layers:
	-	`sha256:a8abf2c9952faed7ee6a8484d94c195f2f516d28b4aa99d61fde6a938373ef14`  
		Last Modified: Sat, 07 Mar 2026 00:37:56 GMT  
		Size: 2.0 MB (2011293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4baff3ba9a329e3fdeaee0149357b33f76e181413fc6e5b4d1b9502670d8aab3`  
		Last Modified: Sat, 07 Mar 2026 00:37:56 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; arm variant v7

```console
$ docker pull memcached@sha256:5e39383d269092b745c7426583a0849917817a2861226858ff17c34f227cadc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28515640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4d89f2522b7f402debcdfe4ae5ef33ccc13694e72756aabd8c894fd1a657663`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Sat, 07 Mar 2026 00:34:26 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Mar 2026 00:34:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Mar 2026 00:37:36 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:37:36 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:37:36 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:37:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:37:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:37:37 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:37:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:37:37 GMT
USER memcache
# Sat, 07 Mar 2026 00:37:37 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:37:37 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b5f623d77fff35b334b15c7b208113b4b778a70ce39168e1270421140984e6`  
		Last Modified: Sat, 07 Mar 2026 00:37:43 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d378422d428b98928a2c392598ff24dddba86412c764099339db2c9b84dab7`  
		Last Modified: Sat, 07 Mar 2026 00:37:43 GMT  
		Size: 135.4 KB (135371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ebe7571649e14f8ae60c2aa9c7464f120d47deb28852880adc72f5958fb268`  
		Last Modified: Sat, 07 Mar 2026 00:37:43 GMT  
		Size: 2.2 MB (2165006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab8a97091ab7e05c0561d93041f6833b293ec83a81c5cd316d914c7cd4797f5`  
		Last Modified: Sat, 07 Mar 2026 00:37:43 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06917ca5c3af99a9a619b7c0077abf8521b0777d4c07464889139b6030aaa445`  
		Last Modified: Sat, 07 Mar 2026 00:37:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:17c7cd3931d1614e411d593e6027c70049d32dd6b78b4523f5e29ff13b7b1f21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b42f736130d7735ab6bde638b9206c6be06a848c316aa0776562b9d2b05634b5`

```dockerfile
```

-	Layers:
	-	`sha256:1700f9d32fecaf2a6fff6e275b9eac8036467ba4e592635351cf279712b2017b`  
		Last Modified: Sat, 07 Mar 2026 00:37:43 GMT  
		Size: 2.0 MB (2009750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef3320ccea4ba2f43dfdeb26388b30f9251a45c8b87522656d05eb856e022fa0`  
		Last Modified: Sat, 07 Mar 2026 00:37:43 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:03ff213526efc235b60a048b3efa0c67c6d697a62bdc207561fb8ee00f254f89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32557234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4742c51756a2139de24009e1c754635923a703d67706387249d261e4dc62712`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Sat, 07 Mar 2026 00:34:23 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Mar 2026 00:34:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Mar 2026 00:37:25 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:37:25 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:37:25 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:37:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:37:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:37:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:37:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:37:25 GMT
USER memcache
# Sat, 07 Mar 2026 00:37:25 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:37:25 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:461d33f62f9a4e4fbc09492d8ce59e548e8c794e3122411c5f7a8370f2bbedba`  
		Last Modified: Sat, 07 Mar 2026 00:37:31 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e642309aa5a12065d7f985c382b7658fa51b45c2a111039cdb9b7240299809e7`  
		Last Modified: Sat, 07 Mar 2026 00:37:31 GMT  
		Size: 153.5 KB (153496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c81e14adafcb230598de8ae3eaf03443a9ae10bd04e616ae4ab64a2f379a48d`  
		Last Modified: Sat, 07 Mar 2026 00:37:31 GMT  
		Size: 2.3 MB (2262125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62e12af1edbdc302c3fd82e9561c5eac5def3110b53dc9d527b277d70a0c5b0`  
		Last Modified: Sat, 07 Mar 2026 00:37:31 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eee7fdafd6f634c0431e5a06be62ff9a726cb1fa8367483d6b026fa3164c7f0`  
		Last Modified: Sat, 07 Mar 2026 00:37:32 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:f791266a2bf814187fed117fa0abd604df8d26056d2e2791b51eb537a958de3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e7b8f74c70d2427388103547caa9c90ef2b4ec4ee11ce197e642593e10f6979`

```dockerfile
```

-	Layers:
	-	`sha256:88d9544d6eb9588edcaeabdc26922a9afb53b2222e8f9972e5b4b52199893738`  
		Last Modified: Sat, 07 Mar 2026 00:37:31 GMT  
		Size: 2.0 MB (2008606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b245266f3e6e113152f086489529a68f1c8c229363d9b678823c16250c48131`  
		Last Modified: Sat, 07 Mar 2026 00:37:31 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; 386

```console
$ docker pull memcached@sha256:1219e49a37eb8fa43f5cabcda7eb69df920734c5d615f2fc63e4fba52a06dfd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33667722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d141db22d43d8c6503a206b3413976c2fd0b84654a45bb46a3da3f39594ee93e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1771804800'
# Sat, 07 Mar 2026 00:34:41 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Mar 2026 00:34:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Mar 2026 00:37:41 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:37:41 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:37:41 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:37:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:37:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:37:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:37:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:37:41 GMT
USER memcache
# Sat, 07 Mar 2026 00:37:41 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:37:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f4e0b944ee1e7e50bdfbfa77bda370b6eccee7d698a7adca78c38f5ca0767ca5`  
		Last Modified: Tue, 24 Feb 2026 18:43:18 GMT  
		Size: 31.3 MB (31293918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d38eff546890db9ae0646486b61a548d8067820adc96ceb6eb4f5d7c2206bb8`  
		Last Modified: Sat, 07 Mar 2026 00:37:47 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c454125cf8ccd03f95714478c13c1d671ba0807b980ee5e6df450d611f61e156`  
		Last Modified: Sat, 07 Mar 2026 00:37:47 GMT  
		Size: 147.5 KB (147517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42b7d17f494cc1acab1da36a724a41a46ecf955d058123b89b170ea63bafda97`  
		Last Modified: Sat, 07 Mar 2026 00:37:47 GMT  
		Size: 2.2 MB (2224772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56fcaee4e2b815384392953fdf84278be4b9a4b116e3a5ad6436f7b13a7c6d9`  
		Last Modified: Sat, 07 Mar 2026 00:37:47 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6adacd7f3e38f46b44efa4ff006b35719382afa26b95b7a9b0c62ef7e7a01bfc`  
		Last Modified: Sat, 07 Mar 2026 00:37:48 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:9f65574f3294736b3dc217e4b07a4045282c517d258eaa96a32035e09cda6fa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb96fc147195e16ed2b6e99c3582cd8c6a67516fb0387c563d09fbf85f6a4dc0`

```dockerfile
```

-	Layers:
	-	`sha256:cdc74dec8f482313433fa0011e8531a8e816610bf31af8b63d2203318e8a59f9`  
		Last Modified: Sat, 07 Mar 2026 00:37:47 GMT  
		Size: 2.0 MB (2005447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bbcbbf7d1935fe3e711cd689ff38f789c3f7334bff2fd2518c106c4bf5d805f`  
		Last Modified: Sat, 07 Mar 2026 00:37:47 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; ppc64le

```console
$ docker pull memcached@sha256:ffac94778c7c882a7f2cbaae5af33e755639de207d07834e052412c2b22a24b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36754462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5640d71fb49b8eaef07631709a9f4924bd191fcfe9b44b7df2d525e247075b64`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Sat, 07 Mar 2026 00:33:31 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Mar 2026 00:33:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Mar 2026 00:56:42 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:56:42 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:56:42 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:56:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:56:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:56:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:56:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:56:44 GMT
USER memcache
# Sat, 07 Mar 2026 00:56:44 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:56:44 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab70996aa4a561e7f3e1f1e1b14df7912a1456b20b317937391cfa826c93f2ea`  
		Last Modified: Sat, 07 Mar 2026 00:57:10 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1ba00921effa53d91205ba3e5e3280c719885f49b5e9e0f8e2a387cf316d89`  
		Last Modified: Sat, 07 Mar 2026 00:57:10 GMT  
		Size: 170.4 KB (170386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd00738358190677470eca91b6732f6fcc475639b7f07f1943af6f5d268ae47`  
		Last Modified: Sat, 07 Mar 2026 00:57:10 GMT  
		Size: 3.0 MB (2982343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f7dc97a8f5d8c677e24bd2f8014c3e315619d726d409033dc3ce4f6d7d7569d`  
		Last Modified: Sat, 07 Mar 2026 00:57:10 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f2b48241128f09e1c613b0fb34d37f79c77417d033b7a00041f8cd08d6241f`  
		Last Modified: Sat, 07 Mar 2026 00:57:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:da557c745e92be8dd35823b9c24b79e47c55ff727768980abe9b659a14672408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e89b8bba62432d49e11baad935eddf449853276e5bb492953ae6bb995bf81ef`

```dockerfile
```

-	Layers:
	-	`sha256:7bf94ead3bca06412117cdc5395bde9d799ffc799dd28be779209634f64bfc0b`  
		Last Modified: Sat, 07 Mar 2026 00:57:10 GMT  
		Size: 2.0 MB (2011891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ec351466954789ecb039e735ecf9fd0235d5d4cfcf8bd6bcf2cf68049016c1c`  
		Last Modified: Sat, 07 Mar 2026 00:57:10 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; riscv64

```console
$ docker pull memcached@sha256:ccac0e143b4efd5bd15fb67df5ad87f5b743cc3db826cbb27d1874cbb3b6d549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30619564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f9320af1aa6fbbae22f81ef28d68694abc001739c71a195b4b1cd490b3b9107`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 23:50:36 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 09 Mar 2026 23:51:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Mar 2026 00:09:03 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 10 Mar 2026 00:09:03 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 10 Mar 2026 00:09:03 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 10 Mar 2026 00:09:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 10 Mar 2026 00:09:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 10 Mar 2026 00:09:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 10 Mar 2026 00:09:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Mar 2026 00:09:03 GMT
USER memcache
# Tue, 10 Mar 2026 00:09:03 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 10 Mar 2026 00:09:03 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e1366b1f74881f04901f31cfdecf9f3f5d4794ebf89911083a239bf462bf21`  
		Last Modified: Tue, 10 Mar 2026 00:09:56 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918782f8ab4ae7fe2ab9f1fc0aa7ad4e48d83dc362a4dcac336048ded3de9b6e`  
		Last Modified: Tue, 10 Mar 2026 00:09:56 GMT  
		Size: 133.1 KB (133079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963fbe1d00657987e81bdc270499ad5aacf8f91b100915c30ddf9fc57cd67346`  
		Last Modified: Tue, 10 Mar 2026 00:09:56 GMT  
		Size: 2.2 MB (2208551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729657786193241c665df2cbaeb72b5d157865abb3bbd8b9460e88d08fb65fea`  
		Last Modified: Tue, 10 Mar 2026 00:09:56 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8246f12fbc1ee94790a418b9655df55d80968171273b5994aaffa40c04fa2f3c`  
		Last Modified: Tue, 10 Mar 2026 00:09:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:de9f0d80a354763898649af4229a6f696fb51689e3b577af2e1d918d365777e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d72c30b80e1c2deaee38b267b52cab1a28e245b2a3608fcf459f2232dad3faa7`

```dockerfile
```

-	Layers:
	-	`sha256:03d9f11a7e8cf93ffe1f13ecfd86632a66af5a6efc142ae7a4ecac0c19418b2d`  
		Last Modified: Tue, 10 Mar 2026 00:09:56 GMT  
		Size: 2.0 MB (2002254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:452e3f764b5054c447aa8e63046155a20784d6f10159282ce633afdb79bf9279`  
		Last Modified: Tue, 10 Mar 2026 00:09:56 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; s390x

```console
$ docker pull memcached@sha256:8e1f3fb07bf1702ad27a7e2a6b2364e61d7b5165c113d0202db31adaa90d91df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32278340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1088ed36ed575f78d3e06fdd24f1ccdcc908d6e579970b2cae128c29f8d6e7a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Sat, 07 Mar 2026 00:33:32 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Mar 2026 00:33:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Mar 2026 00:36:51 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:36:51 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:36:51 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:36:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:36:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:36:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:36:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:36:51 GMT
USER memcache
# Sat, 07 Mar 2026 00:36:51 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:36:51 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986cc162f1a9b2f1b4c673da47497d87b8a542990f29c7823ee4d64cd160ea34`  
		Last Modified: Sat, 07 Mar 2026 00:37:00 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e3b516d24d039487b70f5d718d6f2b0c5473b5da4e6b82815239c7730587d6`  
		Last Modified: Sat, 07 Mar 2026 00:37:00 GMT  
		Size: 140.5 KB (140520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb611bdb547903f4763e52741be4c28e6ed0f172ebffc4ddae4e56a1a4d3ebc2`  
		Last Modified: Sat, 07 Mar 2026 00:37:00 GMT  
		Size: 2.3 MB (2298126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b32c7b8a27f2284141ba22bde8036a295b3e0d397cde405054e47e550cced01`  
		Last Modified: Sat, 07 Mar 2026 00:37:00 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3240387a49966ed4c1475913af7c7648c5499d01045e56e16637a760300918a`  
		Last Modified: Sat, 07 Mar 2026 00:37:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:b725149e071a1d02723f7674a5f7c477144350f79f2243558bce2360da7bf73b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:628ead940c50f3d4776c150c412d2270c2238893cfd1a57f8c17647ec35223e2`

```dockerfile
```

-	Layers:
	-	`sha256:b118af94ed9d10ab8f0c0221725860a15ff82dce98bd35abb240f411b745e0f7`  
		Last Modified: Sat, 07 Mar 2026 00:37:00 GMT  
		Size: 2.0 MB (2009727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:737fa51b5113fe89d161d6b7d0d81d66c28e666617dc1fb7c410b093ecf35625`  
		Last Modified: Sat, 07 Mar 2026 00:37:00 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json
