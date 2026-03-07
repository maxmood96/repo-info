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
$ docker pull memcached@sha256:572b011ce33954ee809066d8cecbeb3ec98912109ee3be3663a3197425fd81ac
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
$ docker pull memcached@sha256:023c4e23c94ba68b5a97a6f56c2828ebedc281e85a52ac0b2690b58700b3bb7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32195506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:033ea2f06d6420e86006806fd73fd124d41bf3a1ccfa612823af947b880ca8c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:04:39 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 24 Feb 2026 19:04:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:07:27 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 24 Feb 2026 19:07:27 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 24 Feb 2026 19:07:27 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 24 Feb 2026 19:07:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 24 Feb 2026 19:07:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:07:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 24 Feb 2026 19:07:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:07:27 GMT
USER memcache
# Tue, 24 Feb 2026 19:07:27 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 24 Feb 2026 19:07:27 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36056d8f6cc22203cda4cb7a7b65e6597244fb8468bf7015c6d9ae2e76f2e9a0`  
		Last Modified: Tue, 24 Feb 2026 19:07:33 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:185bddc36e29c3f75831b51c77695b60ce372b05fa6a05cdf757fd7224e140f7`  
		Last Modified: Tue, 24 Feb 2026 19:07:33 GMT  
		Size: 136.7 KB (136687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f8366e7d29ee7ccd518666350d7b6c8573a147053d8d883ec991efe322d5f5`  
		Last Modified: Tue, 24 Feb 2026 19:07:33 GMT  
		Size: 2.3 MB (2278677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd467f5caa7f19a29f886aeff83e2edf03c41832304f1a8d53b50ca9e97dc8c`  
		Last Modified: Tue, 24 Feb 2026 19:07:33 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6a0854d419bc2397f7c1b7ac5b15319f81aab68a1e055e271d32b69360dfcc`  
		Last Modified: Tue, 24 Feb 2026 19:07:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:93eb971a0f54e3ff33aa02af6d7ea3dbfc884c93129b25b2a433551d611e6877
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ec223135b79851b5f9b5ee88b297cefbf1858a2d669b454b60e27ff96d6512a`

```dockerfile
```

-	Layers:
	-	`sha256:7e3c52b39ce2400a537d122eef601ccaa8527c356dc34ba5e233ae089eca6bcc`  
		Last Modified: Tue, 24 Feb 2026 19:07:33 GMT  
		Size: 2.0 MB (2008290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4860fbffaac75568c714f1a1a433740f20ee1ce624d4bb3f82d7ebbb1c2e288e`  
		Last Modified: Tue, 24 Feb 2026 19:07:33 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm variant v5

```console
$ docker pull memcached@sha256:ba68b1eb22f8d62ea931bc8e125f0e795b01242209298c7f23060d94ea748463
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30303705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b00afbdbae6e13cdf413d8caed5854add790bb103c4ca68b363f971794cb651d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 18:59:37 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 24 Feb 2026 18:59:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:03:00 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 24 Feb 2026 19:03:00 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 24 Feb 2026 19:03:00 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 24 Feb 2026 19:03:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 24 Feb 2026 19:03:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:03:00 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 24 Feb 2026 19:03:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:03:00 GMT
USER memcache
# Tue, 24 Feb 2026 19:03:00 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 24 Feb 2026 19:03:00 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:280a075cc1d2a97445b9f4430aa9774bfc38fc4217b7fc9d6a7b04e7e431cb65`  
		Last Modified: Tue, 24 Feb 2026 18:42:44 GMT  
		Size: 27.9 MB (27947608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf8f6794c0e26d45659cabbb095050aeae71ae849a69981e8b0bbf72278c8a3`  
		Last Modified: Tue, 24 Feb 2026 19:03:06 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec23046983d4d416a3fdd21ee149b45f2d0adafd4951a0c1d3a2b6b5b46f0019`  
		Last Modified: Tue, 24 Feb 2026 19:03:06 GMT  
		Size: 144.2 KB (144174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238dcf6c237d3a80010ba1d7f9b108159fa5cbfa8c450954f88c1183ce4f3667`  
		Last Modified: Tue, 24 Feb 2026 19:03:06 GMT  
		Size: 2.2 MB (2210411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c950303c16fe639587ececa73419dc844738b41140b423b7eb0384ea716267`  
		Last Modified: Tue, 24 Feb 2026 19:03:06 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e93319de4797e67380bf08f73a8c50f44a58bc5d48b1f23fb6f08e4ffeb6db10`  
		Last Modified: Tue, 24 Feb 2026 19:03:07 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:0cf62386cd305d86703ad800762c1372a34293bfad797b6a29e27282f3b1f3f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd0998a1e5967fa757cf01fe012763ec5c2a1924834b1b5b71293d9d8e6b6e73`

```dockerfile
```

-	Layers:
	-	`sha256:2a59dac704d61fc3b17645258ea234efe69b7e467c6e660e0226a6f828e75acf`  
		Last Modified: Tue, 24 Feb 2026 19:03:06 GMT  
		Size: 2.0 MB (2011293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10a2bc4477f2db7316f6a3b19832420a977c86d7e21d4eb855955079d793b60d`  
		Last Modified: Tue, 24 Feb 2026 19:03:06 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm variant v7

```console
$ docker pull memcached@sha256:be3fc72ab6cfa1ea6cf0e4934c88efff77606bf59e9b967282e0146142af3ded
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28514687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91c5981c3560c3a86da48563ea4ad119abd5a3afe1897a22de0465775fbba444`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:04:15 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 24 Feb 2026 19:04:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:07:24 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 24 Feb 2026 19:07:24 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 24 Feb 2026 19:07:24 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 24 Feb 2026 19:07:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 24 Feb 2026 19:07:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:07:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 24 Feb 2026 19:07:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:07:24 GMT
USER memcache
# Tue, 24 Feb 2026 19:07:24 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 24 Feb 2026 19:07:24 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1190ad5d6adaf3041f81179fb1a2a2ffd13c6236c4011b3b0e574b20a0240248`  
		Last Modified: Tue, 24 Feb 2026 19:07:30 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a4d01b331567500cc2848dc045c00005a609b0caa7819712aa4c0b1c36a602`  
		Last Modified: Tue, 24 Feb 2026 19:07:30 GMT  
		Size: 135.4 KB (135372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09feae8fb4ac83c32d5ac15d5578c16a87b563518fb4ece9bc65c0dd4eec4617`  
		Last Modified: Tue, 24 Feb 2026 19:07:30 GMT  
		Size: 2.2 MB (2164057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3f5af79bcb8f4d70c5d381d7623a5157340c864a02043363b99fd392b70a49`  
		Last Modified: Tue, 24 Feb 2026 19:07:30 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f525abc9eb110fb4d08a2fc9aec1c625c91ecc14675ea27b19ad4528db27e29`  
		Last Modified: Tue, 24 Feb 2026 19:07:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:0c0b5fadc4b970f34bfb9e213bc510f9cf711fee0d731866b79b9a7725bbfe67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d19c5e298b74d1907a036edbf16180a9c315d79341636a8d7283fd667a7f399`

```dockerfile
```

-	Layers:
	-	`sha256:bec22f2e6f0aa5f193a09a38b693ac428534a6f02b83ded0ae660639f5b2e63a`  
		Last Modified: Tue, 24 Feb 2026 19:07:31 GMT  
		Size: 2.0 MB (2009750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:535737c7b64de5d274415f285b181b237967739c8145f2a0c666ebc2addff27d`  
		Last Modified: Tue, 24 Feb 2026 19:07:31 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:383b83f45bfcba593d3017bf4e72398bad4c3d31bc3a92665c75cb44d6d8010a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32556427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:931b22f98bd50f35ac08c7bdbd76091693ea91dfeac1b0a01a1943fc1e5c7d34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:07:31 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 24 Feb 2026 19:07:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:10:30 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 24 Feb 2026 19:10:30 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 24 Feb 2026 19:10:30 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 24 Feb 2026 19:10:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 24 Feb 2026 19:10:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:10:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 24 Feb 2026 19:10:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:10:30 GMT
USER memcache
# Tue, 24 Feb 2026 19:10:30 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 24 Feb 2026 19:10:30 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da63b3df116854958d3edc49224f00f800f8feceb07f409a89da01a568acfd74`  
		Last Modified: Tue, 24 Feb 2026 19:10:35 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d7d6dca284320d75e2a6b070eba5471c445206c750390794bffa12a045cf25`  
		Last Modified: Tue, 24 Feb 2026 19:10:36 GMT  
		Size: 153.5 KB (153473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa939cfd8be671996b32d233394ecff0cb4ee1ad010d7d95d0ff847976387b7`  
		Last Modified: Tue, 24 Feb 2026 19:10:36 GMT  
		Size: 2.3 MB (2261343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82787d9b0b7359766dc7a263f2c52ad3c430ae67068af1de0a775f4039c2c11d`  
		Last Modified: Tue, 24 Feb 2026 19:10:36 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc91ce04553e029ee43de7fd212662cbb243747b9b554ccb2515963360487b78`  
		Last Modified: Tue, 24 Feb 2026 19:10:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:df115eb253a89a2fb8823967dfc90bb6eaef5f8c68d172c472e80a97983ea047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac6cbdb8c151703cc011a84d25f241b73c56094667b7b2e14f5b78f1567cb431`

```dockerfile
```

-	Layers:
	-	`sha256:1f68573ab5b0140c68ab975345114e497f510b3df716041482fc47ea1c8c1e97`  
		Last Modified: Tue, 24 Feb 2026 19:10:36 GMT  
		Size: 2.0 MB (2008606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3ed1c1193f31e42d639c05820912adaf7632e1444abe907acb5d020b2941c8c`  
		Last Modified: Tue, 24 Feb 2026 19:10:35 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; 386

```console
$ docker pull memcached@sha256:8d2616d6d6f7cf8b88e84529a283bb7d5905e04ab68b771d3da78c7faaa3863f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33666622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:060038b35b56cd38bd725bc0d26e82d247ead0b7723d50ad8efa423fd9a7e9a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 18:59:23 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 24 Feb 2026 18:59:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:02:23 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 24 Feb 2026 19:02:23 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 24 Feb 2026 19:02:23 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 24 Feb 2026 19:02:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 24 Feb 2026 19:02:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:02:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 24 Feb 2026 19:02:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:02:23 GMT
USER memcache
# Tue, 24 Feb 2026 19:02:23 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 24 Feb 2026 19:02:23 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f4e0b944ee1e7e50bdfbfa77bda370b6eccee7d698a7adca78c38f5ca0767ca5`  
		Last Modified: Tue, 24 Feb 2026 18:43:18 GMT  
		Size: 31.3 MB (31293918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7370c6d23e537397165580c793f3f488b5c1e3725032c34ddff16242efc509e`  
		Last Modified: Tue, 24 Feb 2026 19:02:29 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0af0c71eb6719f8e1973879b2ea81a32290a2bfdba4580598f838b40d74d0a9`  
		Last Modified: Tue, 24 Feb 2026 19:02:29 GMT  
		Size: 147.5 KB (147516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e12a16ad70a850a1f54b2b691348dd7e9a2f00ad453b2c79be3c6aeff3ef7b`  
		Last Modified: Tue, 24 Feb 2026 19:02:29 GMT  
		Size: 2.2 MB (2223676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8177c4ca17c056b8c5a4548fe0c9c760b3bbb1954ac900869d5efa1453c5ea`  
		Last Modified: Tue, 24 Feb 2026 19:02:29 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:272ec8dc3492083ced99bc57e9db1b10009f74c1c83b6795ed38c110fd42cdaf`  
		Last Modified: Tue, 24 Feb 2026 19:02:30 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:5070ac2246d76cda16369492c5adf738ae74e24f338e539a063259c5437cda2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c35cb195506953c3800638d94cb495f01b68d5bf564a91c0863c783a44e63495`

```dockerfile
```

-	Layers:
	-	`sha256:c87395201667ae86b09526c196163cf3d7ee8fef27350876c4d0e8889c5f026d`  
		Last Modified: Tue, 24 Feb 2026 19:02:29 GMT  
		Size: 2.0 MB (2005447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b3952676542fa0fbd53a1e5d2b08b33f01828e2ea0d9bdca0f6a44f980418e1`  
		Last Modified: Tue, 24 Feb 2026 19:02:29 GMT  
		Size: 22.1 KB (22094 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; ppc64le

```console
$ docker pull memcached@sha256:295640646e2e642c4ba4a954358685a29bd942df8b9a3fd0a8bf92346372c68a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36166011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a3c07f4fe24eef5f498b6370e9d70655e93d823d70348f0c03de8caa64bf5b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 24 Feb 2026 19:14:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:18:32 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 24 Feb 2026 19:18:32 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 24 Feb 2026 19:18:32 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 24 Feb 2026 19:18:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 24 Feb 2026 19:18:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:18:33 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 24 Feb 2026 19:18:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:18:33 GMT
USER memcache
# Tue, 24 Feb 2026 19:18:33 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 24 Feb 2026 19:18:33 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ad3fa262401e234341c4865354faecb35fd4a15ce23d4369debdd68a4e0ba1`  
		Last Modified: Tue, 24 Feb 2026 19:18:51 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37018ee7f60ce5d622bc47071034caa8643168e590eb82f2859530e295c2d74`  
		Last Modified: Tue, 24 Feb 2026 19:18:51 GMT  
		Size: 170.4 KB (170364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8293edd47a62890de39041653fd374133f7c81506463cd4c8f1fd3999c25c41a`  
		Last Modified: Tue, 24 Feb 2026 19:18:51 GMT  
		Size: 2.4 MB (2393913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54918c9a7df48c86af7a40a80c050b442a77e99b2a733c83726b0f546d6d9176`  
		Last Modified: Tue, 24 Feb 2026 19:18:51 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ae01ebdb25dffa16d71caa402e2f64eedeadcf5505f9afcb9b0deed17b6046`  
		Last Modified: Tue, 24 Feb 2026 19:18:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:9ed368016d333d4d55370690943777bae8f79c9f72a2e191366bfd728c2527e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b009746df9b6c47b18442bec8d9bd2eb4f7da37e6d23d23c7b3d106924496dc3`

```dockerfile
```

-	Layers:
	-	`sha256:0cd5dd42f5171c2e7ffb3ecfb193700298aa51685c923038e547720b7968393f`  
		Last Modified: Tue, 24 Feb 2026 19:18:51 GMT  
		Size: 2.0 MB (2011891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7f7951a0f59cb83944081d3c657d0a48918adcefc5ae2f3ee64a42c6cf4c144`  
		Last Modified: Tue, 24 Feb 2026 19:18:50 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; riscv64

```console
$ docker pull memcached@sha256:4d92d3a017ca8ca7948c884d9ee25e96e8e1838bb94d53dda569f07101262c74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30618541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b8cdde436a640517ee901b0927c2e128caa695cf3b0a71d4b3bd027993c2c10`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Wed, 25 Feb 2026 03:12:58 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 25 Feb 2026 03:13:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Feb 2026 03:27:04 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 25 Feb 2026 03:27:04 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 25 Feb 2026 03:27:04 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 25 Feb 2026 03:27:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 25 Feb 2026 03:27:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Feb 2026 03:27:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 25 Feb 2026 03:27:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Feb 2026 03:27:05 GMT
USER memcache
# Wed, 25 Feb 2026 03:27:05 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 25 Feb 2026 03:27:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fce183db3522d3b87ff4ec8768ec38313bc647df242c4d2245264321599e224`  
		Last Modified: Wed, 25 Feb 2026 03:27:51 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e1dbc92883ea2cad6fb0e4ff4a478e862dc760d2ec927369aa328b52592cb9`  
		Last Modified: Wed, 25 Feb 2026 03:27:51 GMT  
		Size: 133.1 KB (133074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c5718939dc18cc9d82791adad3e4ce75827c393387d12514f92f85467b359f`  
		Last Modified: Wed, 25 Feb 2026 03:27:51 GMT  
		Size: 2.2 MB (2207537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e44b817acb07e256823d291317d247cbe97bdbc55a0994ec267467d04b30022`  
		Last Modified: Wed, 25 Feb 2026 03:27:51 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:841d2d3e5a28536b578d3aab8c1da972de21a13e202997467bfa050b0dfe6a64`  
		Last Modified: Wed, 25 Feb 2026 03:27:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:a9b01e3fd82fcc2536a8b4f8a38b204a12799015583aaab4ff3ac8bcd7c192fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f57f541807865ade76a34e9e121a96114daa4ab2ca34a5c924d5d19255cb885d`

```dockerfile
```

-	Layers:
	-	`sha256:ce3f35cea1f210746ebccb073cfc7ce51878ce03482e8c9a09457641385bc443`  
		Last Modified: Wed, 25 Feb 2026 03:27:51 GMT  
		Size: 2.0 MB (2002254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba4ac2058d1632d5f3a3cf0698ec37889198d45cfe57218c131d295df9df13be`  
		Last Modified: Wed, 25 Feb 2026 03:27:51 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; s390x

```console
$ docker pull memcached@sha256:423ba67b801204b46b8a1dba1974e6f2e209639dbc48c62b9d33190987e2226f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32277818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:284d259d569d7694ea6f980a0e46469afbf8ca345caaf21a16df77cd30bd0759`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:01:44 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 24 Feb 2026 19:01:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:05:47 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 24 Feb 2026 19:05:47 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 24 Feb 2026 19:05:47 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 24 Feb 2026 19:05:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 24 Feb 2026 19:05:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:05:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 24 Feb 2026 19:05:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:05:47 GMT
USER memcache
# Tue, 24 Feb 2026 19:05:47 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 24 Feb 2026 19:05:47 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:604ba03d7a54182e1f14697e43fa7f23271204247cf53166e71e93154e0e1b7c`  
		Last Modified: Tue, 24 Feb 2026 19:06:02 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60f992885eee7a354d3a7f3a15cbe933eaf1769daaf5aeec0816188eee9c235`  
		Last Modified: Tue, 24 Feb 2026 19:06:02 GMT  
		Size: 140.5 KB (140518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ba39b84415354f148c7bf1358db39e8c60c8ee7d57aae315707efcbe4a97f8`  
		Last Modified: Tue, 24 Feb 2026 19:06:02 GMT  
		Size: 2.3 MB (2297608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:748f3d38558f1ce81c9c5df4831b79004bdd8407d6de9a1f6242190e6bdec648`  
		Last Modified: Tue, 24 Feb 2026 19:06:02 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d826358b929a42dd9b9a6eabd6d7f0bd6f454a14926713798750f8f4f58dacc7`  
		Last Modified: Tue, 24 Feb 2026 19:06:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:7db0b5141cc4d90b60e471db94061e9e1cd536bf5f19001772a4428dfcc06aa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c61de11a61ead852674daabea6eb13f5c704df55e4c57bef85fccde8e16dc89b`

```dockerfile
```

-	Layers:
	-	`sha256:3038f05f0370cca0449ad250c4f0a7f2ad5ead64983ea5fcb6604efc88eff2c6`  
		Last Modified: Tue, 24 Feb 2026 19:06:02 GMT  
		Size: 2.0 MB (2009727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5be29fae8812d4c817fe359ed16601d8204939006a63c3b9e676a4a5e7462b9`  
		Last Modified: Tue, 24 Feb 2026 19:06:02 GMT  
		Size: 22.2 KB (22152 bytes)  
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
$ docker pull memcached@sha256:572b011ce33954ee809066d8cecbeb3ec98912109ee3be3663a3197425fd81ac
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
$ docker pull memcached@sha256:023c4e23c94ba68b5a97a6f56c2828ebedc281e85a52ac0b2690b58700b3bb7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32195506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:033ea2f06d6420e86006806fd73fd124d41bf3a1ccfa612823af947b880ca8c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:04:39 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 24 Feb 2026 19:04:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:07:27 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 24 Feb 2026 19:07:27 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 24 Feb 2026 19:07:27 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 24 Feb 2026 19:07:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 24 Feb 2026 19:07:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:07:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 24 Feb 2026 19:07:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:07:27 GMT
USER memcache
# Tue, 24 Feb 2026 19:07:27 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 24 Feb 2026 19:07:27 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36056d8f6cc22203cda4cb7a7b65e6597244fb8468bf7015c6d9ae2e76f2e9a0`  
		Last Modified: Tue, 24 Feb 2026 19:07:33 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:185bddc36e29c3f75831b51c77695b60ce372b05fa6a05cdf757fd7224e140f7`  
		Last Modified: Tue, 24 Feb 2026 19:07:33 GMT  
		Size: 136.7 KB (136687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f8366e7d29ee7ccd518666350d7b6c8573a147053d8d883ec991efe322d5f5`  
		Last Modified: Tue, 24 Feb 2026 19:07:33 GMT  
		Size: 2.3 MB (2278677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd467f5caa7f19a29f886aeff83e2edf03c41832304f1a8d53b50ca9e97dc8c`  
		Last Modified: Tue, 24 Feb 2026 19:07:33 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6a0854d419bc2397f7c1b7ac5b15319f81aab68a1e055e271d32b69360dfcc`  
		Last Modified: Tue, 24 Feb 2026 19:07:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:93eb971a0f54e3ff33aa02af6d7ea3dbfc884c93129b25b2a433551d611e6877
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ec223135b79851b5f9b5ee88b297cefbf1858a2d669b454b60e27ff96d6512a`

```dockerfile
```

-	Layers:
	-	`sha256:7e3c52b39ce2400a537d122eef601ccaa8527c356dc34ba5e233ae089eca6bcc`  
		Last Modified: Tue, 24 Feb 2026 19:07:33 GMT  
		Size: 2.0 MB (2008290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4860fbffaac75568c714f1a1a433740f20ee1ce624d4bb3f82d7ebbb1c2e288e`  
		Last Modified: Tue, 24 Feb 2026 19:07:33 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; arm variant v5

```console
$ docker pull memcached@sha256:ba68b1eb22f8d62ea931bc8e125f0e795b01242209298c7f23060d94ea748463
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30303705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b00afbdbae6e13cdf413d8caed5854add790bb103c4ca68b363f971794cb651d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 18:59:37 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 24 Feb 2026 18:59:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:03:00 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 24 Feb 2026 19:03:00 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 24 Feb 2026 19:03:00 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 24 Feb 2026 19:03:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 24 Feb 2026 19:03:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:03:00 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 24 Feb 2026 19:03:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:03:00 GMT
USER memcache
# Tue, 24 Feb 2026 19:03:00 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 24 Feb 2026 19:03:00 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:280a075cc1d2a97445b9f4430aa9774bfc38fc4217b7fc9d6a7b04e7e431cb65`  
		Last Modified: Tue, 24 Feb 2026 18:42:44 GMT  
		Size: 27.9 MB (27947608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf8f6794c0e26d45659cabbb095050aeae71ae849a69981e8b0bbf72278c8a3`  
		Last Modified: Tue, 24 Feb 2026 19:03:06 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec23046983d4d416a3fdd21ee149b45f2d0adafd4951a0c1d3a2b6b5b46f0019`  
		Last Modified: Tue, 24 Feb 2026 19:03:06 GMT  
		Size: 144.2 KB (144174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238dcf6c237d3a80010ba1d7f9b108159fa5cbfa8c450954f88c1183ce4f3667`  
		Last Modified: Tue, 24 Feb 2026 19:03:06 GMT  
		Size: 2.2 MB (2210411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c950303c16fe639587ececa73419dc844738b41140b423b7eb0384ea716267`  
		Last Modified: Tue, 24 Feb 2026 19:03:06 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e93319de4797e67380bf08f73a8c50f44a58bc5d48b1f23fb6f08e4ffeb6db10`  
		Last Modified: Tue, 24 Feb 2026 19:03:07 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:0cf62386cd305d86703ad800762c1372a34293bfad797b6a29e27282f3b1f3f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd0998a1e5967fa757cf01fe012763ec5c2a1924834b1b5b71293d9d8e6b6e73`

```dockerfile
```

-	Layers:
	-	`sha256:2a59dac704d61fc3b17645258ea234efe69b7e467c6e660e0226a6f828e75acf`  
		Last Modified: Tue, 24 Feb 2026 19:03:06 GMT  
		Size: 2.0 MB (2011293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10a2bc4477f2db7316f6a3b19832420a977c86d7e21d4eb855955079d793b60d`  
		Last Modified: Tue, 24 Feb 2026 19:03:06 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; arm variant v7

```console
$ docker pull memcached@sha256:be3fc72ab6cfa1ea6cf0e4934c88efff77606bf59e9b967282e0146142af3ded
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28514687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91c5981c3560c3a86da48563ea4ad119abd5a3afe1897a22de0465775fbba444`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:04:15 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 24 Feb 2026 19:04:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:07:24 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 24 Feb 2026 19:07:24 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 24 Feb 2026 19:07:24 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 24 Feb 2026 19:07:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 24 Feb 2026 19:07:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:07:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 24 Feb 2026 19:07:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:07:24 GMT
USER memcache
# Tue, 24 Feb 2026 19:07:24 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 24 Feb 2026 19:07:24 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1190ad5d6adaf3041f81179fb1a2a2ffd13c6236c4011b3b0e574b20a0240248`  
		Last Modified: Tue, 24 Feb 2026 19:07:30 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a4d01b331567500cc2848dc045c00005a609b0caa7819712aa4c0b1c36a602`  
		Last Modified: Tue, 24 Feb 2026 19:07:30 GMT  
		Size: 135.4 KB (135372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09feae8fb4ac83c32d5ac15d5578c16a87b563518fb4ece9bc65c0dd4eec4617`  
		Last Modified: Tue, 24 Feb 2026 19:07:30 GMT  
		Size: 2.2 MB (2164057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3f5af79bcb8f4d70c5d381d7623a5157340c864a02043363b99fd392b70a49`  
		Last Modified: Tue, 24 Feb 2026 19:07:30 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f525abc9eb110fb4d08a2fc9aec1c625c91ecc14675ea27b19ad4528db27e29`  
		Last Modified: Tue, 24 Feb 2026 19:07:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:0c0b5fadc4b970f34bfb9e213bc510f9cf711fee0d731866b79b9a7725bbfe67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d19c5e298b74d1907a036edbf16180a9c315d79341636a8d7283fd667a7f399`

```dockerfile
```

-	Layers:
	-	`sha256:bec22f2e6f0aa5f193a09a38b693ac428534a6f02b83ded0ae660639f5b2e63a`  
		Last Modified: Tue, 24 Feb 2026 19:07:31 GMT  
		Size: 2.0 MB (2009750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:535737c7b64de5d274415f285b181b237967739c8145f2a0c666ebc2addff27d`  
		Last Modified: Tue, 24 Feb 2026 19:07:31 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:383b83f45bfcba593d3017bf4e72398bad4c3d31bc3a92665c75cb44d6d8010a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32556427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:931b22f98bd50f35ac08c7bdbd76091693ea91dfeac1b0a01a1943fc1e5c7d34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:07:31 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 24 Feb 2026 19:07:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:10:30 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 24 Feb 2026 19:10:30 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 24 Feb 2026 19:10:30 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 24 Feb 2026 19:10:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 24 Feb 2026 19:10:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:10:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 24 Feb 2026 19:10:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:10:30 GMT
USER memcache
# Tue, 24 Feb 2026 19:10:30 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 24 Feb 2026 19:10:30 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da63b3df116854958d3edc49224f00f800f8feceb07f409a89da01a568acfd74`  
		Last Modified: Tue, 24 Feb 2026 19:10:35 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d7d6dca284320d75e2a6b070eba5471c445206c750390794bffa12a045cf25`  
		Last Modified: Tue, 24 Feb 2026 19:10:36 GMT  
		Size: 153.5 KB (153473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa939cfd8be671996b32d233394ecff0cb4ee1ad010d7d95d0ff847976387b7`  
		Last Modified: Tue, 24 Feb 2026 19:10:36 GMT  
		Size: 2.3 MB (2261343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82787d9b0b7359766dc7a263f2c52ad3c430ae67068af1de0a775f4039c2c11d`  
		Last Modified: Tue, 24 Feb 2026 19:10:36 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc91ce04553e029ee43de7fd212662cbb243747b9b554ccb2515963360487b78`  
		Last Modified: Tue, 24 Feb 2026 19:10:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:df115eb253a89a2fb8823967dfc90bb6eaef5f8c68d172c472e80a97983ea047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac6cbdb8c151703cc011a84d25f241b73c56094667b7b2e14f5b78f1567cb431`

```dockerfile
```

-	Layers:
	-	`sha256:1f68573ab5b0140c68ab975345114e497f510b3df716041482fc47ea1c8c1e97`  
		Last Modified: Tue, 24 Feb 2026 19:10:36 GMT  
		Size: 2.0 MB (2008606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3ed1c1193f31e42d639c05820912adaf7632e1444abe907acb5d020b2941c8c`  
		Last Modified: Tue, 24 Feb 2026 19:10:35 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; 386

```console
$ docker pull memcached@sha256:8d2616d6d6f7cf8b88e84529a283bb7d5905e04ab68b771d3da78c7faaa3863f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33666622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:060038b35b56cd38bd725bc0d26e82d247ead0b7723d50ad8efa423fd9a7e9a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 18:59:23 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 24 Feb 2026 18:59:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:02:23 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 24 Feb 2026 19:02:23 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 24 Feb 2026 19:02:23 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 24 Feb 2026 19:02:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 24 Feb 2026 19:02:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:02:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 24 Feb 2026 19:02:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:02:23 GMT
USER memcache
# Tue, 24 Feb 2026 19:02:23 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 24 Feb 2026 19:02:23 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f4e0b944ee1e7e50bdfbfa77bda370b6eccee7d698a7adca78c38f5ca0767ca5`  
		Last Modified: Tue, 24 Feb 2026 18:43:18 GMT  
		Size: 31.3 MB (31293918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7370c6d23e537397165580c793f3f488b5c1e3725032c34ddff16242efc509e`  
		Last Modified: Tue, 24 Feb 2026 19:02:29 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0af0c71eb6719f8e1973879b2ea81a32290a2bfdba4580598f838b40d74d0a9`  
		Last Modified: Tue, 24 Feb 2026 19:02:29 GMT  
		Size: 147.5 KB (147516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e12a16ad70a850a1f54b2b691348dd7e9a2f00ad453b2c79be3c6aeff3ef7b`  
		Last Modified: Tue, 24 Feb 2026 19:02:29 GMT  
		Size: 2.2 MB (2223676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8177c4ca17c056b8c5a4548fe0c9c760b3bbb1954ac900869d5efa1453c5ea`  
		Last Modified: Tue, 24 Feb 2026 19:02:29 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:272ec8dc3492083ced99bc57e9db1b10009f74c1c83b6795ed38c110fd42cdaf`  
		Last Modified: Tue, 24 Feb 2026 19:02:30 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:5070ac2246d76cda16369492c5adf738ae74e24f338e539a063259c5437cda2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c35cb195506953c3800638d94cb495f01b68d5bf564a91c0863c783a44e63495`

```dockerfile
```

-	Layers:
	-	`sha256:c87395201667ae86b09526c196163cf3d7ee8fef27350876c4d0e8889c5f026d`  
		Last Modified: Tue, 24 Feb 2026 19:02:29 GMT  
		Size: 2.0 MB (2005447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b3952676542fa0fbd53a1e5d2b08b33f01828e2ea0d9bdca0f6a44f980418e1`  
		Last Modified: Tue, 24 Feb 2026 19:02:29 GMT  
		Size: 22.1 KB (22094 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; ppc64le

```console
$ docker pull memcached@sha256:295640646e2e642c4ba4a954358685a29bd942df8b9a3fd0a8bf92346372c68a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36166011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a3c07f4fe24eef5f498b6370e9d70655e93d823d70348f0c03de8caa64bf5b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 24 Feb 2026 19:14:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:18:32 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 24 Feb 2026 19:18:32 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 24 Feb 2026 19:18:32 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 24 Feb 2026 19:18:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 24 Feb 2026 19:18:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:18:33 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 24 Feb 2026 19:18:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:18:33 GMT
USER memcache
# Tue, 24 Feb 2026 19:18:33 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 24 Feb 2026 19:18:33 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ad3fa262401e234341c4865354faecb35fd4a15ce23d4369debdd68a4e0ba1`  
		Last Modified: Tue, 24 Feb 2026 19:18:51 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37018ee7f60ce5d622bc47071034caa8643168e590eb82f2859530e295c2d74`  
		Last Modified: Tue, 24 Feb 2026 19:18:51 GMT  
		Size: 170.4 KB (170364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8293edd47a62890de39041653fd374133f7c81506463cd4c8f1fd3999c25c41a`  
		Last Modified: Tue, 24 Feb 2026 19:18:51 GMT  
		Size: 2.4 MB (2393913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54918c9a7df48c86af7a40a80c050b442a77e99b2a733c83726b0f546d6d9176`  
		Last Modified: Tue, 24 Feb 2026 19:18:51 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ae01ebdb25dffa16d71caa402e2f64eedeadcf5505f9afcb9b0deed17b6046`  
		Last Modified: Tue, 24 Feb 2026 19:18:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:9ed368016d333d4d55370690943777bae8f79c9f72a2e191366bfd728c2527e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b009746df9b6c47b18442bec8d9bd2eb4f7da37e6d23d23c7b3d106924496dc3`

```dockerfile
```

-	Layers:
	-	`sha256:0cd5dd42f5171c2e7ffb3ecfb193700298aa51685c923038e547720b7968393f`  
		Last Modified: Tue, 24 Feb 2026 19:18:51 GMT  
		Size: 2.0 MB (2011891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7f7951a0f59cb83944081d3c657d0a48918adcefc5ae2f3ee64a42c6cf4c144`  
		Last Modified: Tue, 24 Feb 2026 19:18:50 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; riscv64

```console
$ docker pull memcached@sha256:4d92d3a017ca8ca7948c884d9ee25e96e8e1838bb94d53dda569f07101262c74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30618541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b8cdde436a640517ee901b0927c2e128caa695cf3b0a71d4b3bd027993c2c10`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Wed, 25 Feb 2026 03:12:58 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 25 Feb 2026 03:13:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Feb 2026 03:27:04 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 25 Feb 2026 03:27:04 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 25 Feb 2026 03:27:04 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 25 Feb 2026 03:27:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 25 Feb 2026 03:27:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Feb 2026 03:27:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 25 Feb 2026 03:27:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Feb 2026 03:27:05 GMT
USER memcache
# Wed, 25 Feb 2026 03:27:05 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 25 Feb 2026 03:27:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fce183db3522d3b87ff4ec8768ec38313bc647df242c4d2245264321599e224`  
		Last Modified: Wed, 25 Feb 2026 03:27:51 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e1dbc92883ea2cad6fb0e4ff4a478e862dc760d2ec927369aa328b52592cb9`  
		Last Modified: Wed, 25 Feb 2026 03:27:51 GMT  
		Size: 133.1 KB (133074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c5718939dc18cc9d82791adad3e4ce75827c393387d12514f92f85467b359f`  
		Last Modified: Wed, 25 Feb 2026 03:27:51 GMT  
		Size: 2.2 MB (2207537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e44b817acb07e256823d291317d247cbe97bdbc55a0994ec267467d04b30022`  
		Last Modified: Wed, 25 Feb 2026 03:27:51 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:841d2d3e5a28536b578d3aab8c1da972de21a13e202997467bfa050b0dfe6a64`  
		Last Modified: Wed, 25 Feb 2026 03:27:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:a9b01e3fd82fcc2536a8b4f8a38b204a12799015583aaab4ff3ac8bcd7c192fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f57f541807865ade76a34e9e121a96114daa4ab2ca34a5c924d5d19255cb885d`

```dockerfile
```

-	Layers:
	-	`sha256:ce3f35cea1f210746ebccb073cfc7ce51878ce03482e8c9a09457641385bc443`  
		Last Modified: Wed, 25 Feb 2026 03:27:51 GMT  
		Size: 2.0 MB (2002254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba4ac2058d1632d5f3a3cf0698ec37889198d45cfe57218c131d295df9df13be`  
		Last Modified: Wed, 25 Feb 2026 03:27:51 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; s390x

```console
$ docker pull memcached@sha256:423ba67b801204b46b8a1dba1974e6f2e209639dbc48c62b9d33190987e2226f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32277818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:284d259d569d7694ea6f980a0e46469afbf8ca345caaf21a16df77cd30bd0759`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:01:44 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 24 Feb 2026 19:01:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:05:47 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 24 Feb 2026 19:05:47 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 24 Feb 2026 19:05:47 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 24 Feb 2026 19:05:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 24 Feb 2026 19:05:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:05:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 24 Feb 2026 19:05:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:05:47 GMT
USER memcache
# Tue, 24 Feb 2026 19:05:47 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 24 Feb 2026 19:05:47 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:604ba03d7a54182e1f14697e43fa7f23271204247cf53166e71e93154e0e1b7c`  
		Last Modified: Tue, 24 Feb 2026 19:06:02 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60f992885eee7a354d3a7f3a15cbe933eaf1769daaf5aeec0816188eee9c235`  
		Last Modified: Tue, 24 Feb 2026 19:06:02 GMT  
		Size: 140.5 KB (140518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ba39b84415354f148c7bf1358db39e8c60c8ee7d57aae315707efcbe4a97f8`  
		Last Modified: Tue, 24 Feb 2026 19:06:02 GMT  
		Size: 2.3 MB (2297608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:748f3d38558f1ce81c9c5df4831b79004bdd8407d6de9a1f6242190e6bdec648`  
		Last Modified: Tue, 24 Feb 2026 19:06:02 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d826358b929a42dd9b9a6eabd6d7f0bd6f454a14926713798750f8f4f58dacc7`  
		Last Modified: Tue, 24 Feb 2026 19:06:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:7db0b5141cc4d90b60e471db94061e9e1cd536bf5f19001772a4428dfcc06aa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c61de11a61ead852674daabea6eb13f5c704df55e4c57bef85fccde8e16dc89b`

```dockerfile
```

-	Layers:
	-	`sha256:3038f05f0370cca0449ad250c4f0a7f2ad5ead64983ea5fcb6604efc88eff2c6`  
		Last Modified: Tue, 24 Feb 2026 19:06:02 GMT  
		Size: 2.0 MB (2009727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5be29fae8812d4c817fe359ed16601d8204939006a63c3b9e676a4a5e7462b9`  
		Last Modified: Tue, 24 Feb 2026 19:06:02 GMT  
		Size: 22.2 KB (22152 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6`

```console
$ docker pull memcached@sha256:572b011ce33954ee809066d8cecbeb3ec98912109ee3be3663a3197425fd81ac
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
$ docker pull memcached@sha256:023c4e23c94ba68b5a97a6f56c2828ebedc281e85a52ac0b2690b58700b3bb7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32195506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:033ea2f06d6420e86006806fd73fd124d41bf3a1ccfa612823af947b880ca8c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:04:39 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 24 Feb 2026 19:04:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:07:27 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 24 Feb 2026 19:07:27 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 24 Feb 2026 19:07:27 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 24 Feb 2026 19:07:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 24 Feb 2026 19:07:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:07:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 24 Feb 2026 19:07:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:07:27 GMT
USER memcache
# Tue, 24 Feb 2026 19:07:27 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 24 Feb 2026 19:07:27 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36056d8f6cc22203cda4cb7a7b65e6597244fb8468bf7015c6d9ae2e76f2e9a0`  
		Last Modified: Tue, 24 Feb 2026 19:07:33 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:185bddc36e29c3f75831b51c77695b60ce372b05fa6a05cdf757fd7224e140f7`  
		Last Modified: Tue, 24 Feb 2026 19:07:33 GMT  
		Size: 136.7 KB (136687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f8366e7d29ee7ccd518666350d7b6c8573a147053d8d883ec991efe322d5f5`  
		Last Modified: Tue, 24 Feb 2026 19:07:33 GMT  
		Size: 2.3 MB (2278677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd467f5caa7f19a29f886aeff83e2edf03c41832304f1a8d53b50ca9e97dc8c`  
		Last Modified: Tue, 24 Feb 2026 19:07:33 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6a0854d419bc2397f7c1b7ac5b15319f81aab68a1e055e271d32b69360dfcc`  
		Last Modified: Tue, 24 Feb 2026 19:07:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:93eb971a0f54e3ff33aa02af6d7ea3dbfc884c93129b25b2a433551d611e6877
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ec223135b79851b5f9b5ee88b297cefbf1858a2d669b454b60e27ff96d6512a`

```dockerfile
```

-	Layers:
	-	`sha256:7e3c52b39ce2400a537d122eef601ccaa8527c356dc34ba5e233ae089eca6bcc`  
		Last Modified: Tue, 24 Feb 2026 19:07:33 GMT  
		Size: 2.0 MB (2008290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4860fbffaac75568c714f1a1a433740f20ee1ce624d4bb3f82d7ebbb1c2e288e`  
		Last Modified: Tue, 24 Feb 2026 19:07:33 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm variant v5

```console
$ docker pull memcached@sha256:ba68b1eb22f8d62ea931bc8e125f0e795b01242209298c7f23060d94ea748463
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30303705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b00afbdbae6e13cdf413d8caed5854add790bb103c4ca68b363f971794cb651d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 18:59:37 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 24 Feb 2026 18:59:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:03:00 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 24 Feb 2026 19:03:00 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 24 Feb 2026 19:03:00 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 24 Feb 2026 19:03:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 24 Feb 2026 19:03:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:03:00 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 24 Feb 2026 19:03:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:03:00 GMT
USER memcache
# Tue, 24 Feb 2026 19:03:00 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 24 Feb 2026 19:03:00 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:280a075cc1d2a97445b9f4430aa9774bfc38fc4217b7fc9d6a7b04e7e431cb65`  
		Last Modified: Tue, 24 Feb 2026 18:42:44 GMT  
		Size: 27.9 MB (27947608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf8f6794c0e26d45659cabbb095050aeae71ae849a69981e8b0bbf72278c8a3`  
		Last Modified: Tue, 24 Feb 2026 19:03:06 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec23046983d4d416a3fdd21ee149b45f2d0adafd4951a0c1d3a2b6b5b46f0019`  
		Last Modified: Tue, 24 Feb 2026 19:03:06 GMT  
		Size: 144.2 KB (144174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238dcf6c237d3a80010ba1d7f9b108159fa5cbfa8c450954f88c1183ce4f3667`  
		Last Modified: Tue, 24 Feb 2026 19:03:06 GMT  
		Size: 2.2 MB (2210411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c950303c16fe639587ececa73419dc844738b41140b423b7eb0384ea716267`  
		Last Modified: Tue, 24 Feb 2026 19:03:06 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e93319de4797e67380bf08f73a8c50f44a58bc5d48b1f23fb6f08e4ffeb6db10`  
		Last Modified: Tue, 24 Feb 2026 19:03:07 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:0cf62386cd305d86703ad800762c1372a34293bfad797b6a29e27282f3b1f3f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd0998a1e5967fa757cf01fe012763ec5c2a1924834b1b5b71293d9d8e6b6e73`

```dockerfile
```

-	Layers:
	-	`sha256:2a59dac704d61fc3b17645258ea234efe69b7e467c6e660e0226a6f828e75acf`  
		Last Modified: Tue, 24 Feb 2026 19:03:06 GMT  
		Size: 2.0 MB (2011293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10a2bc4477f2db7316f6a3b19832420a977c86d7e21d4eb855955079d793b60d`  
		Last Modified: Tue, 24 Feb 2026 19:03:06 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm variant v7

```console
$ docker pull memcached@sha256:be3fc72ab6cfa1ea6cf0e4934c88efff77606bf59e9b967282e0146142af3ded
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28514687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91c5981c3560c3a86da48563ea4ad119abd5a3afe1897a22de0465775fbba444`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:04:15 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 24 Feb 2026 19:04:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:07:24 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 24 Feb 2026 19:07:24 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 24 Feb 2026 19:07:24 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 24 Feb 2026 19:07:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 24 Feb 2026 19:07:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:07:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 24 Feb 2026 19:07:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:07:24 GMT
USER memcache
# Tue, 24 Feb 2026 19:07:24 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 24 Feb 2026 19:07:24 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1190ad5d6adaf3041f81179fb1a2a2ffd13c6236c4011b3b0e574b20a0240248`  
		Last Modified: Tue, 24 Feb 2026 19:07:30 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a4d01b331567500cc2848dc045c00005a609b0caa7819712aa4c0b1c36a602`  
		Last Modified: Tue, 24 Feb 2026 19:07:30 GMT  
		Size: 135.4 KB (135372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09feae8fb4ac83c32d5ac15d5578c16a87b563518fb4ece9bc65c0dd4eec4617`  
		Last Modified: Tue, 24 Feb 2026 19:07:30 GMT  
		Size: 2.2 MB (2164057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3f5af79bcb8f4d70c5d381d7623a5157340c864a02043363b99fd392b70a49`  
		Last Modified: Tue, 24 Feb 2026 19:07:30 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f525abc9eb110fb4d08a2fc9aec1c625c91ecc14675ea27b19ad4528db27e29`  
		Last Modified: Tue, 24 Feb 2026 19:07:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:0c0b5fadc4b970f34bfb9e213bc510f9cf711fee0d731866b79b9a7725bbfe67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d19c5e298b74d1907a036edbf16180a9c315d79341636a8d7283fd667a7f399`

```dockerfile
```

-	Layers:
	-	`sha256:bec22f2e6f0aa5f193a09a38b693ac428534a6f02b83ded0ae660639f5b2e63a`  
		Last Modified: Tue, 24 Feb 2026 19:07:31 GMT  
		Size: 2.0 MB (2009750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:535737c7b64de5d274415f285b181b237967739c8145f2a0c666ebc2addff27d`  
		Last Modified: Tue, 24 Feb 2026 19:07:31 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:383b83f45bfcba593d3017bf4e72398bad4c3d31bc3a92665c75cb44d6d8010a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32556427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:931b22f98bd50f35ac08c7bdbd76091693ea91dfeac1b0a01a1943fc1e5c7d34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:07:31 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 24 Feb 2026 19:07:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:10:30 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 24 Feb 2026 19:10:30 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 24 Feb 2026 19:10:30 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 24 Feb 2026 19:10:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 24 Feb 2026 19:10:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:10:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 24 Feb 2026 19:10:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:10:30 GMT
USER memcache
# Tue, 24 Feb 2026 19:10:30 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 24 Feb 2026 19:10:30 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da63b3df116854958d3edc49224f00f800f8feceb07f409a89da01a568acfd74`  
		Last Modified: Tue, 24 Feb 2026 19:10:35 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d7d6dca284320d75e2a6b070eba5471c445206c750390794bffa12a045cf25`  
		Last Modified: Tue, 24 Feb 2026 19:10:36 GMT  
		Size: 153.5 KB (153473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa939cfd8be671996b32d233394ecff0cb4ee1ad010d7d95d0ff847976387b7`  
		Last Modified: Tue, 24 Feb 2026 19:10:36 GMT  
		Size: 2.3 MB (2261343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82787d9b0b7359766dc7a263f2c52ad3c430ae67068af1de0a775f4039c2c11d`  
		Last Modified: Tue, 24 Feb 2026 19:10:36 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc91ce04553e029ee43de7fd212662cbb243747b9b554ccb2515963360487b78`  
		Last Modified: Tue, 24 Feb 2026 19:10:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:df115eb253a89a2fb8823967dfc90bb6eaef5f8c68d172c472e80a97983ea047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac6cbdb8c151703cc011a84d25f241b73c56094667b7b2e14f5b78f1567cb431`

```dockerfile
```

-	Layers:
	-	`sha256:1f68573ab5b0140c68ab975345114e497f510b3df716041482fc47ea1c8c1e97`  
		Last Modified: Tue, 24 Feb 2026 19:10:36 GMT  
		Size: 2.0 MB (2008606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3ed1c1193f31e42d639c05820912adaf7632e1444abe907acb5d020b2941c8c`  
		Last Modified: Tue, 24 Feb 2026 19:10:35 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; 386

```console
$ docker pull memcached@sha256:8d2616d6d6f7cf8b88e84529a283bb7d5905e04ab68b771d3da78c7faaa3863f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33666622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:060038b35b56cd38bd725bc0d26e82d247ead0b7723d50ad8efa423fd9a7e9a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 18:59:23 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 24 Feb 2026 18:59:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:02:23 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 24 Feb 2026 19:02:23 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 24 Feb 2026 19:02:23 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 24 Feb 2026 19:02:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 24 Feb 2026 19:02:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:02:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 24 Feb 2026 19:02:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:02:23 GMT
USER memcache
# Tue, 24 Feb 2026 19:02:23 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 24 Feb 2026 19:02:23 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f4e0b944ee1e7e50bdfbfa77bda370b6eccee7d698a7adca78c38f5ca0767ca5`  
		Last Modified: Tue, 24 Feb 2026 18:43:18 GMT  
		Size: 31.3 MB (31293918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7370c6d23e537397165580c793f3f488b5c1e3725032c34ddff16242efc509e`  
		Last Modified: Tue, 24 Feb 2026 19:02:29 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0af0c71eb6719f8e1973879b2ea81a32290a2bfdba4580598f838b40d74d0a9`  
		Last Modified: Tue, 24 Feb 2026 19:02:29 GMT  
		Size: 147.5 KB (147516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e12a16ad70a850a1f54b2b691348dd7e9a2f00ad453b2c79be3c6aeff3ef7b`  
		Last Modified: Tue, 24 Feb 2026 19:02:29 GMT  
		Size: 2.2 MB (2223676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8177c4ca17c056b8c5a4548fe0c9c760b3bbb1954ac900869d5efa1453c5ea`  
		Last Modified: Tue, 24 Feb 2026 19:02:29 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:272ec8dc3492083ced99bc57e9db1b10009f74c1c83b6795ed38c110fd42cdaf`  
		Last Modified: Tue, 24 Feb 2026 19:02:30 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:5070ac2246d76cda16369492c5adf738ae74e24f338e539a063259c5437cda2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c35cb195506953c3800638d94cb495f01b68d5bf564a91c0863c783a44e63495`

```dockerfile
```

-	Layers:
	-	`sha256:c87395201667ae86b09526c196163cf3d7ee8fef27350876c4d0e8889c5f026d`  
		Last Modified: Tue, 24 Feb 2026 19:02:29 GMT  
		Size: 2.0 MB (2005447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b3952676542fa0fbd53a1e5d2b08b33f01828e2ea0d9bdca0f6a44f980418e1`  
		Last Modified: Tue, 24 Feb 2026 19:02:29 GMT  
		Size: 22.1 KB (22094 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; ppc64le

```console
$ docker pull memcached@sha256:295640646e2e642c4ba4a954358685a29bd942df8b9a3fd0a8bf92346372c68a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36166011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a3c07f4fe24eef5f498b6370e9d70655e93d823d70348f0c03de8caa64bf5b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 24 Feb 2026 19:14:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:18:32 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 24 Feb 2026 19:18:32 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 24 Feb 2026 19:18:32 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 24 Feb 2026 19:18:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 24 Feb 2026 19:18:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:18:33 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 24 Feb 2026 19:18:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:18:33 GMT
USER memcache
# Tue, 24 Feb 2026 19:18:33 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 24 Feb 2026 19:18:33 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ad3fa262401e234341c4865354faecb35fd4a15ce23d4369debdd68a4e0ba1`  
		Last Modified: Tue, 24 Feb 2026 19:18:51 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37018ee7f60ce5d622bc47071034caa8643168e590eb82f2859530e295c2d74`  
		Last Modified: Tue, 24 Feb 2026 19:18:51 GMT  
		Size: 170.4 KB (170364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8293edd47a62890de39041653fd374133f7c81506463cd4c8f1fd3999c25c41a`  
		Last Modified: Tue, 24 Feb 2026 19:18:51 GMT  
		Size: 2.4 MB (2393913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54918c9a7df48c86af7a40a80c050b442a77e99b2a733c83726b0f546d6d9176`  
		Last Modified: Tue, 24 Feb 2026 19:18:51 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ae01ebdb25dffa16d71caa402e2f64eedeadcf5505f9afcb9b0deed17b6046`  
		Last Modified: Tue, 24 Feb 2026 19:18:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:9ed368016d333d4d55370690943777bae8f79c9f72a2e191366bfd728c2527e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b009746df9b6c47b18442bec8d9bd2eb4f7da37e6d23d23c7b3d106924496dc3`

```dockerfile
```

-	Layers:
	-	`sha256:0cd5dd42f5171c2e7ffb3ecfb193700298aa51685c923038e547720b7968393f`  
		Last Modified: Tue, 24 Feb 2026 19:18:51 GMT  
		Size: 2.0 MB (2011891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7f7951a0f59cb83944081d3c657d0a48918adcefc5ae2f3ee64a42c6cf4c144`  
		Last Modified: Tue, 24 Feb 2026 19:18:50 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; riscv64

```console
$ docker pull memcached@sha256:4d92d3a017ca8ca7948c884d9ee25e96e8e1838bb94d53dda569f07101262c74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30618541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b8cdde436a640517ee901b0927c2e128caa695cf3b0a71d4b3bd027993c2c10`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Wed, 25 Feb 2026 03:12:58 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 25 Feb 2026 03:13:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Feb 2026 03:27:04 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 25 Feb 2026 03:27:04 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 25 Feb 2026 03:27:04 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 25 Feb 2026 03:27:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 25 Feb 2026 03:27:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Feb 2026 03:27:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 25 Feb 2026 03:27:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Feb 2026 03:27:05 GMT
USER memcache
# Wed, 25 Feb 2026 03:27:05 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 25 Feb 2026 03:27:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fce183db3522d3b87ff4ec8768ec38313bc647df242c4d2245264321599e224`  
		Last Modified: Wed, 25 Feb 2026 03:27:51 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e1dbc92883ea2cad6fb0e4ff4a478e862dc760d2ec927369aa328b52592cb9`  
		Last Modified: Wed, 25 Feb 2026 03:27:51 GMT  
		Size: 133.1 KB (133074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c5718939dc18cc9d82791adad3e4ce75827c393387d12514f92f85467b359f`  
		Last Modified: Wed, 25 Feb 2026 03:27:51 GMT  
		Size: 2.2 MB (2207537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e44b817acb07e256823d291317d247cbe97bdbc55a0994ec267467d04b30022`  
		Last Modified: Wed, 25 Feb 2026 03:27:51 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:841d2d3e5a28536b578d3aab8c1da972de21a13e202997467bfa050b0dfe6a64`  
		Last Modified: Wed, 25 Feb 2026 03:27:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:a9b01e3fd82fcc2536a8b4f8a38b204a12799015583aaab4ff3ac8bcd7c192fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f57f541807865ade76a34e9e121a96114daa4ab2ca34a5c924d5d19255cb885d`

```dockerfile
```

-	Layers:
	-	`sha256:ce3f35cea1f210746ebccb073cfc7ce51878ce03482e8c9a09457641385bc443`  
		Last Modified: Wed, 25 Feb 2026 03:27:51 GMT  
		Size: 2.0 MB (2002254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba4ac2058d1632d5f3a3cf0698ec37889198d45cfe57218c131d295df9df13be`  
		Last Modified: Wed, 25 Feb 2026 03:27:51 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; s390x

```console
$ docker pull memcached@sha256:423ba67b801204b46b8a1dba1974e6f2e209639dbc48c62b9d33190987e2226f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32277818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:284d259d569d7694ea6f980a0e46469afbf8ca345caaf21a16df77cd30bd0759`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:01:44 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 24 Feb 2026 19:01:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:05:47 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 24 Feb 2026 19:05:47 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 24 Feb 2026 19:05:47 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 24 Feb 2026 19:05:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 24 Feb 2026 19:05:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:05:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 24 Feb 2026 19:05:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:05:47 GMT
USER memcache
# Tue, 24 Feb 2026 19:05:47 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 24 Feb 2026 19:05:47 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:604ba03d7a54182e1f14697e43fa7f23271204247cf53166e71e93154e0e1b7c`  
		Last Modified: Tue, 24 Feb 2026 19:06:02 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60f992885eee7a354d3a7f3a15cbe933eaf1769daaf5aeec0816188eee9c235`  
		Last Modified: Tue, 24 Feb 2026 19:06:02 GMT  
		Size: 140.5 KB (140518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ba39b84415354f148c7bf1358db39e8c60c8ee7d57aae315707efcbe4a97f8`  
		Last Modified: Tue, 24 Feb 2026 19:06:02 GMT  
		Size: 2.3 MB (2297608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:748f3d38558f1ce81c9c5df4831b79004bdd8407d6de9a1f6242190e6bdec648`  
		Last Modified: Tue, 24 Feb 2026 19:06:02 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d826358b929a42dd9b9a6eabd6d7f0bd6f454a14926713798750f8f4f58dacc7`  
		Last Modified: Tue, 24 Feb 2026 19:06:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:7db0b5141cc4d90b60e471db94061e9e1cd536bf5f19001772a4428dfcc06aa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c61de11a61ead852674daabea6eb13f5c704df55e4c57bef85fccde8e16dc89b`

```dockerfile
```

-	Layers:
	-	`sha256:3038f05f0370cca0449ad250c4f0a7f2ad5ead64983ea5fcb6604efc88eff2c6`  
		Last Modified: Tue, 24 Feb 2026 19:06:02 GMT  
		Size: 2.0 MB (2009727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5be29fae8812d4c817fe359ed16601d8204939006a63c3b9e676a4a5e7462b9`  
		Last Modified: Tue, 24 Feb 2026 19:06:02 GMT  
		Size: 22.2 KB (22152 bytes)  
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
$ docker pull memcached@sha256:572b011ce33954ee809066d8cecbeb3ec98912109ee3be3663a3197425fd81ac
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
$ docker pull memcached@sha256:023c4e23c94ba68b5a97a6f56c2828ebedc281e85a52ac0b2690b58700b3bb7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32195506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:033ea2f06d6420e86006806fd73fd124d41bf3a1ccfa612823af947b880ca8c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:04:39 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 24 Feb 2026 19:04:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:07:27 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 24 Feb 2026 19:07:27 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 24 Feb 2026 19:07:27 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 24 Feb 2026 19:07:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 24 Feb 2026 19:07:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:07:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 24 Feb 2026 19:07:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:07:27 GMT
USER memcache
# Tue, 24 Feb 2026 19:07:27 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 24 Feb 2026 19:07:27 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36056d8f6cc22203cda4cb7a7b65e6597244fb8468bf7015c6d9ae2e76f2e9a0`  
		Last Modified: Tue, 24 Feb 2026 19:07:33 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:185bddc36e29c3f75831b51c77695b60ce372b05fa6a05cdf757fd7224e140f7`  
		Last Modified: Tue, 24 Feb 2026 19:07:33 GMT  
		Size: 136.7 KB (136687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f8366e7d29ee7ccd518666350d7b6c8573a147053d8d883ec991efe322d5f5`  
		Last Modified: Tue, 24 Feb 2026 19:07:33 GMT  
		Size: 2.3 MB (2278677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd467f5caa7f19a29f886aeff83e2edf03c41832304f1a8d53b50ca9e97dc8c`  
		Last Modified: Tue, 24 Feb 2026 19:07:33 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6a0854d419bc2397f7c1b7ac5b15319f81aab68a1e055e271d32b69360dfcc`  
		Last Modified: Tue, 24 Feb 2026 19:07:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:93eb971a0f54e3ff33aa02af6d7ea3dbfc884c93129b25b2a433551d611e6877
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ec223135b79851b5f9b5ee88b297cefbf1858a2d669b454b60e27ff96d6512a`

```dockerfile
```

-	Layers:
	-	`sha256:7e3c52b39ce2400a537d122eef601ccaa8527c356dc34ba5e233ae089eca6bcc`  
		Last Modified: Tue, 24 Feb 2026 19:07:33 GMT  
		Size: 2.0 MB (2008290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4860fbffaac75568c714f1a1a433740f20ee1ce624d4bb3f82d7ebbb1c2e288e`  
		Last Modified: Tue, 24 Feb 2026 19:07:33 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; arm variant v5

```console
$ docker pull memcached@sha256:ba68b1eb22f8d62ea931bc8e125f0e795b01242209298c7f23060d94ea748463
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30303705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b00afbdbae6e13cdf413d8caed5854add790bb103c4ca68b363f971794cb651d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 18:59:37 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 24 Feb 2026 18:59:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:03:00 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 24 Feb 2026 19:03:00 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 24 Feb 2026 19:03:00 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 24 Feb 2026 19:03:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 24 Feb 2026 19:03:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:03:00 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 24 Feb 2026 19:03:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:03:00 GMT
USER memcache
# Tue, 24 Feb 2026 19:03:00 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 24 Feb 2026 19:03:00 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:280a075cc1d2a97445b9f4430aa9774bfc38fc4217b7fc9d6a7b04e7e431cb65`  
		Last Modified: Tue, 24 Feb 2026 18:42:44 GMT  
		Size: 27.9 MB (27947608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf8f6794c0e26d45659cabbb095050aeae71ae849a69981e8b0bbf72278c8a3`  
		Last Modified: Tue, 24 Feb 2026 19:03:06 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec23046983d4d416a3fdd21ee149b45f2d0adafd4951a0c1d3a2b6b5b46f0019`  
		Last Modified: Tue, 24 Feb 2026 19:03:06 GMT  
		Size: 144.2 KB (144174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238dcf6c237d3a80010ba1d7f9b108159fa5cbfa8c450954f88c1183ce4f3667`  
		Last Modified: Tue, 24 Feb 2026 19:03:06 GMT  
		Size: 2.2 MB (2210411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c950303c16fe639587ececa73419dc844738b41140b423b7eb0384ea716267`  
		Last Modified: Tue, 24 Feb 2026 19:03:06 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e93319de4797e67380bf08f73a8c50f44a58bc5d48b1f23fb6f08e4ffeb6db10`  
		Last Modified: Tue, 24 Feb 2026 19:03:07 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:0cf62386cd305d86703ad800762c1372a34293bfad797b6a29e27282f3b1f3f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd0998a1e5967fa757cf01fe012763ec5c2a1924834b1b5b71293d9d8e6b6e73`

```dockerfile
```

-	Layers:
	-	`sha256:2a59dac704d61fc3b17645258ea234efe69b7e467c6e660e0226a6f828e75acf`  
		Last Modified: Tue, 24 Feb 2026 19:03:06 GMT  
		Size: 2.0 MB (2011293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10a2bc4477f2db7316f6a3b19832420a977c86d7e21d4eb855955079d793b60d`  
		Last Modified: Tue, 24 Feb 2026 19:03:06 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; arm variant v7

```console
$ docker pull memcached@sha256:be3fc72ab6cfa1ea6cf0e4934c88efff77606bf59e9b967282e0146142af3ded
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28514687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91c5981c3560c3a86da48563ea4ad119abd5a3afe1897a22de0465775fbba444`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:04:15 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 24 Feb 2026 19:04:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:07:24 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 24 Feb 2026 19:07:24 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 24 Feb 2026 19:07:24 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 24 Feb 2026 19:07:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 24 Feb 2026 19:07:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:07:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 24 Feb 2026 19:07:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:07:24 GMT
USER memcache
# Tue, 24 Feb 2026 19:07:24 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 24 Feb 2026 19:07:24 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1190ad5d6adaf3041f81179fb1a2a2ffd13c6236c4011b3b0e574b20a0240248`  
		Last Modified: Tue, 24 Feb 2026 19:07:30 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a4d01b331567500cc2848dc045c00005a609b0caa7819712aa4c0b1c36a602`  
		Last Modified: Tue, 24 Feb 2026 19:07:30 GMT  
		Size: 135.4 KB (135372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09feae8fb4ac83c32d5ac15d5578c16a87b563518fb4ece9bc65c0dd4eec4617`  
		Last Modified: Tue, 24 Feb 2026 19:07:30 GMT  
		Size: 2.2 MB (2164057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3f5af79bcb8f4d70c5d381d7623a5157340c864a02043363b99fd392b70a49`  
		Last Modified: Tue, 24 Feb 2026 19:07:30 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f525abc9eb110fb4d08a2fc9aec1c625c91ecc14675ea27b19ad4528db27e29`  
		Last Modified: Tue, 24 Feb 2026 19:07:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:0c0b5fadc4b970f34bfb9e213bc510f9cf711fee0d731866b79b9a7725bbfe67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d19c5e298b74d1907a036edbf16180a9c315d79341636a8d7283fd667a7f399`

```dockerfile
```

-	Layers:
	-	`sha256:bec22f2e6f0aa5f193a09a38b693ac428534a6f02b83ded0ae660639f5b2e63a`  
		Last Modified: Tue, 24 Feb 2026 19:07:31 GMT  
		Size: 2.0 MB (2009750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:535737c7b64de5d274415f285b181b237967739c8145f2a0c666ebc2addff27d`  
		Last Modified: Tue, 24 Feb 2026 19:07:31 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:383b83f45bfcba593d3017bf4e72398bad4c3d31bc3a92665c75cb44d6d8010a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32556427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:931b22f98bd50f35ac08c7bdbd76091693ea91dfeac1b0a01a1943fc1e5c7d34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:07:31 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 24 Feb 2026 19:07:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:10:30 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 24 Feb 2026 19:10:30 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 24 Feb 2026 19:10:30 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 24 Feb 2026 19:10:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 24 Feb 2026 19:10:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:10:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 24 Feb 2026 19:10:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:10:30 GMT
USER memcache
# Tue, 24 Feb 2026 19:10:30 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 24 Feb 2026 19:10:30 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da63b3df116854958d3edc49224f00f800f8feceb07f409a89da01a568acfd74`  
		Last Modified: Tue, 24 Feb 2026 19:10:35 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d7d6dca284320d75e2a6b070eba5471c445206c750390794bffa12a045cf25`  
		Last Modified: Tue, 24 Feb 2026 19:10:36 GMT  
		Size: 153.5 KB (153473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa939cfd8be671996b32d233394ecff0cb4ee1ad010d7d95d0ff847976387b7`  
		Last Modified: Tue, 24 Feb 2026 19:10:36 GMT  
		Size: 2.3 MB (2261343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82787d9b0b7359766dc7a263f2c52ad3c430ae67068af1de0a775f4039c2c11d`  
		Last Modified: Tue, 24 Feb 2026 19:10:36 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc91ce04553e029ee43de7fd212662cbb243747b9b554ccb2515963360487b78`  
		Last Modified: Tue, 24 Feb 2026 19:10:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:df115eb253a89a2fb8823967dfc90bb6eaef5f8c68d172c472e80a97983ea047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac6cbdb8c151703cc011a84d25f241b73c56094667b7b2e14f5b78f1567cb431`

```dockerfile
```

-	Layers:
	-	`sha256:1f68573ab5b0140c68ab975345114e497f510b3df716041482fc47ea1c8c1e97`  
		Last Modified: Tue, 24 Feb 2026 19:10:36 GMT  
		Size: 2.0 MB (2008606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3ed1c1193f31e42d639c05820912adaf7632e1444abe907acb5d020b2941c8c`  
		Last Modified: Tue, 24 Feb 2026 19:10:35 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; 386

```console
$ docker pull memcached@sha256:8d2616d6d6f7cf8b88e84529a283bb7d5905e04ab68b771d3da78c7faaa3863f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33666622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:060038b35b56cd38bd725bc0d26e82d247ead0b7723d50ad8efa423fd9a7e9a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 18:59:23 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 24 Feb 2026 18:59:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:02:23 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 24 Feb 2026 19:02:23 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 24 Feb 2026 19:02:23 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 24 Feb 2026 19:02:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 24 Feb 2026 19:02:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:02:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 24 Feb 2026 19:02:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:02:23 GMT
USER memcache
# Tue, 24 Feb 2026 19:02:23 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 24 Feb 2026 19:02:23 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f4e0b944ee1e7e50bdfbfa77bda370b6eccee7d698a7adca78c38f5ca0767ca5`  
		Last Modified: Tue, 24 Feb 2026 18:43:18 GMT  
		Size: 31.3 MB (31293918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7370c6d23e537397165580c793f3f488b5c1e3725032c34ddff16242efc509e`  
		Last Modified: Tue, 24 Feb 2026 19:02:29 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0af0c71eb6719f8e1973879b2ea81a32290a2bfdba4580598f838b40d74d0a9`  
		Last Modified: Tue, 24 Feb 2026 19:02:29 GMT  
		Size: 147.5 KB (147516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e12a16ad70a850a1f54b2b691348dd7e9a2f00ad453b2c79be3c6aeff3ef7b`  
		Last Modified: Tue, 24 Feb 2026 19:02:29 GMT  
		Size: 2.2 MB (2223676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8177c4ca17c056b8c5a4548fe0c9c760b3bbb1954ac900869d5efa1453c5ea`  
		Last Modified: Tue, 24 Feb 2026 19:02:29 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:272ec8dc3492083ced99bc57e9db1b10009f74c1c83b6795ed38c110fd42cdaf`  
		Last Modified: Tue, 24 Feb 2026 19:02:30 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:5070ac2246d76cda16369492c5adf738ae74e24f338e539a063259c5437cda2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c35cb195506953c3800638d94cb495f01b68d5bf564a91c0863c783a44e63495`

```dockerfile
```

-	Layers:
	-	`sha256:c87395201667ae86b09526c196163cf3d7ee8fef27350876c4d0e8889c5f026d`  
		Last Modified: Tue, 24 Feb 2026 19:02:29 GMT  
		Size: 2.0 MB (2005447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b3952676542fa0fbd53a1e5d2b08b33f01828e2ea0d9bdca0f6a44f980418e1`  
		Last Modified: Tue, 24 Feb 2026 19:02:29 GMT  
		Size: 22.1 KB (22094 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; ppc64le

```console
$ docker pull memcached@sha256:295640646e2e642c4ba4a954358685a29bd942df8b9a3fd0a8bf92346372c68a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36166011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a3c07f4fe24eef5f498b6370e9d70655e93d823d70348f0c03de8caa64bf5b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 24 Feb 2026 19:14:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:18:32 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 24 Feb 2026 19:18:32 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 24 Feb 2026 19:18:32 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 24 Feb 2026 19:18:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 24 Feb 2026 19:18:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:18:33 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 24 Feb 2026 19:18:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:18:33 GMT
USER memcache
# Tue, 24 Feb 2026 19:18:33 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 24 Feb 2026 19:18:33 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ad3fa262401e234341c4865354faecb35fd4a15ce23d4369debdd68a4e0ba1`  
		Last Modified: Tue, 24 Feb 2026 19:18:51 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37018ee7f60ce5d622bc47071034caa8643168e590eb82f2859530e295c2d74`  
		Last Modified: Tue, 24 Feb 2026 19:18:51 GMT  
		Size: 170.4 KB (170364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8293edd47a62890de39041653fd374133f7c81506463cd4c8f1fd3999c25c41a`  
		Last Modified: Tue, 24 Feb 2026 19:18:51 GMT  
		Size: 2.4 MB (2393913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54918c9a7df48c86af7a40a80c050b442a77e99b2a733c83726b0f546d6d9176`  
		Last Modified: Tue, 24 Feb 2026 19:18:51 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ae01ebdb25dffa16d71caa402e2f64eedeadcf5505f9afcb9b0deed17b6046`  
		Last Modified: Tue, 24 Feb 2026 19:18:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:9ed368016d333d4d55370690943777bae8f79c9f72a2e191366bfd728c2527e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b009746df9b6c47b18442bec8d9bd2eb4f7da37e6d23d23c7b3d106924496dc3`

```dockerfile
```

-	Layers:
	-	`sha256:0cd5dd42f5171c2e7ffb3ecfb193700298aa51685c923038e547720b7968393f`  
		Last Modified: Tue, 24 Feb 2026 19:18:51 GMT  
		Size: 2.0 MB (2011891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7f7951a0f59cb83944081d3c657d0a48918adcefc5ae2f3ee64a42c6cf4c144`  
		Last Modified: Tue, 24 Feb 2026 19:18:50 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; riscv64

```console
$ docker pull memcached@sha256:4d92d3a017ca8ca7948c884d9ee25e96e8e1838bb94d53dda569f07101262c74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30618541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b8cdde436a640517ee901b0927c2e128caa695cf3b0a71d4b3bd027993c2c10`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Wed, 25 Feb 2026 03:12:58 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 25 Feb 2026 03:13:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Feb 2026 03:27:04 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 25 Feb 2026 03:27:04 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 25 Feb 2026 03:27:04 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 25 Feb 2026 03:27:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 25 Feb 2026 03:27:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Feb 2026 03:27:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 25 Feb 2026 03:27:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Feb 2026 03:27:05 GMT
USER memcache
# Wed, 25 Feb 2026 03:27:05 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 25 Feb 2026 03:27:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fce183db3522d3b87ff4ec8768ec38313bc647df242c4d2245264321599e224`  
		Last Modified: Wed, 25 Feb 2026 03:27:51 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e1dbc92883ea2cad6fb0e4ff4a478e862dc760d2ec927369aa328b52592cb9`  
		Last Modified: Wed, 25 Feb 2026 03:27:51 GMT  
		Size: 133.1 KB (133074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c5718939dc18cc9d82791adad3e4ce75827c393387d12514f92f85467b359f`  
		Last Modified: Wed, 25 Feb 2026 03:27:51 GMT  
		Size: 2.2 MB (2207537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e44b817acb07e256823d291317d247cbe97bdbc55a0994ec267467d04b30022`  
		Last Modified: Wed, 25 Feb 2026 03:27:51 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:841d2d3e5a28536b578d3aab8c1da972de21a13e202997467bfa050b0dfe6a64`  
		Last Modified: Wed, 25 Feb 2026 03:27:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:a9b01e3fd82fcc2536a8b4f8a38b204a12799015583aaab4ff3ac8bcd7c192fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f57f541807865ade76a34e9e121a96114daa4ab2ca34a5c924d5d19255cb885d`

```dockerfile
```

-	Layers:
	-	`sha256:ce3f35cea1f210746ebccb073cfc7ce51878ce03482e8c9a09457641385bc443`  
		Last Modified: Wed, 25 Feb 2026 03:27:51 GMT  
		Size: 2.0 MB (2002254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba4ac2058d1632d5f3a3cf0698ec37889198d45cfe57218c131d295df9df13be`  
		Last Modified: Wed, 25 Feb 2026 03:27:51 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; s390x

```console
$ docker pull memcached@sha256:423ba67b801204b46b8a1dba1974e6f2e209639dbc48c62b9d33190987e2226f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32277818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:284d259d569d7694ea6f980a0e46469afbf8ca345caaf21a16df77cd30bd0759`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:01:44 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 24 Feb 2026 19:01:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:05:47 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 24 Feb 2026 19:05:47 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 24 Feb 2026 19:05:47 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 24 Feb 2026 19:05:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 24 Feb 2026 19:05:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:05:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 24 Feb 2026 19:05:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:05:47 GMT
USER memcache
# Tue, 24 Feb 2026 19:05:47 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 24 Feb 2026 19:05:47 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:604ba03d7a54182e1f14697e43fa7f23271204247cf53166e71e93154e0e1b7c`  
		Last Modified: Tue, 24 Feb 2026 19:06:02 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60f992885eee7a354d3a7f3a15cbe933eaf1769daaf5aeec0816188eee9c235`  
		Last Modified: Tue, 24 Feb 2026 19:06:02 GMT  
		Size: 140.5 KB (140518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ba39b84415354f148c7bf1358db39e8c60c8ee7d57aae315707efcbe4a97f8`  
		Last Modified: Tue, 24 Feb 2026 19:06:02 GMT  
		Size: 2.3 MB (2297608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:748f3d38558f1ce81c9c5df4831b79004bdd8407d6de9a1f6242190e6bdec648`  
		Last Modified: Tue, 24 Feb 2026 19:06:02 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d826358b929a42dd9b9a6eabd6d7f0bd6f454a14926713798750f8f4f58dacc7`  
		Last Modified: Tue, 24 Feb 2026 19:06:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:7db0b5141cc4d90b60e471db94061e9e1cd536bf5f19001772a4428dfcc06aa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c61de11a61ead852674daabea6eb13f5c704df55e4c57bef85fccde8e16dc89b`

```dockerfile
```

-	Layers:
	-	`sha256:3038f05f0370cca0449ad250c4f0a7f2ad5ead64983ea5fcb6604efc88eff2c6`  
		Last Modified: Tue, 24 Feb 2026 19:06:02 GMT  
		Size: 2.0 MB (2009727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5be29fae8812d4c817fe359ed16601d8204939006a63c3b9e676a4a5e7462b9`  
		Last Modified: Tue, 24 Feb 2026 19:06:02 GMT  
		Size: 22.2 KB (22152 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.41`

**does not exist** (yet?)

## `memcached:1.6.41-alpine`

**does not exist** (yet?)

## `memcached:1.6.41-alpine3.23`

**does not exist** (yet?)

## `memcached:1.6.41-trixie`

**does not exist** (yet?)

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
$ docker pull memcached@sha256:572b011ce33954ee809066d8cecbeb3ec98912109ee3be3663a3197425fd81ac
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
$ docker pull memcached@sha256:023c4e23c94ba68b5a97a6f56c2828ebedc281e85a52ac0b2690b58700b3bb7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32195506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:033ea2f06d6420e86006806fd73fd124d41bf3a1ccfa612823af947b880ca8c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:04:39 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 24 Feb 2026 19:04:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:07:27 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 24 Feb 2026 19:07:27 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 24 Feb 2026 19:07:27 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 24 Feb 2026 19:07:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 24 Feb 2026 19:07:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:07:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 24 Feb 2026 19:07:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:07:27 GMT
USER memcache
# Tue, 24 Feb 2026 19:07:27 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 24 Feb 2026 19:07:27 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36056d8f6cc22203cda4cb7a7b65e6597244fb8468bf7015c6d9ae2e76f2e9a0`  
		Last Modified: Tue, 24 Feb 2026 19:07:33 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:185bddc36e29c3f75831b51c77695b60ce372b05fa6a05cdf757fd7224e140f7`  
		Last Modified: Tue, 24 Feb 2026 19:07:33 GMT  
		Size: 136.7 KB (136687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f8366e7d29ee7ccd518666350d7b6c8573a147053d8d883ec991efe322d5f5`  
		Last Modified: Tue, 24 Feb 2026 19:07:33 GMT  
		Size: 2.3 MB (2278677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd467f5caa7f19a29f886aeff83e2edf03c41832304f1a8d53b50ca9e97dc8c`  
		Last Modified: Tue, 24 Feb 2026 19:07:33 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6a0854d419bc2397f7c1b7ac5b15319f81aab68a1e055e271d32b69360dfcc`  
		Last Modified: Tue, 24 Feb 2026 19:07:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:93eb971a0f54e3ff33aa02af6d7ea3dbfc884c93129b25b2a433551d611e6877
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ec223135b79851b5f9b5ee88b297cefbf1858a2d669b454b60e27ff96d6512a`

```dockerfile
```

-	Layers:
	-	`sha256:7e3c52b39ce2400a537d122eef601ccaa8527c356dc34ba5e233ae089eca6bcc`  
		Last Modified: Tue, 24 Feb 2026 19:07:33 GMT  
		Size: 2.0 MB (2008290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4860fbffaac75568c714f1a1a433740f20ee1ce624d4bb3f82d7ebbb1c2e288e`  
		Last Modified: Tue, 24 Feb 2026 19:07:33 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm variant v5

```console
$ docker pull memcached@sha256:ba68b1eb22f8d62ea931bc8e125f0e795b01242209298c7f23060d94ea748463
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30303705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b00afbdbae6e13cdf413d8caed5854add790bb103c4ca68b363f971794cb651d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 18:59:37 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 24 Feb 2026 18:59:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:03:00 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 24 Feb 2026 19:03:00 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 24 Feb 2026 19:03:00 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 24 Feb 2026 19:03:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 24 Feb 2026 19:03:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:03:00 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 24 Feb 2026 19:03:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:03:00 GMT
USER memcache
# Tue, 24 Feb 2026 19:03:00 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 24 Feb 2026 19:03:00 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:280a075cc1d2a97445b9f4430aa9774bfc38fc4217b7fc9d6a7b04e7e431cb65`  
		Last Modified: Tue, 24 Feb 2026 18:42:44 GMT  
		Size: 27.9 MB (27947608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf8f6794c0e26d45659cabbb095050aeae71ae849a69981e8b0bbf72278c8a3`  
		Last Modified: Tue, 24 Feb 2026 19:03:06 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec23046983d4d416a3fdd21ee149b45f2d0adafd4951a0c1d3a2b6b5b46f0019`  
		Last Modified: Tue, 24 Feb 2026 19:03:06 GMT  
		Size: 144.2 KB (144174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238dcf6c237d3a80010ba1d7f9b108159fa5cbfa8c450954f88c1183ce4f3667`  
		Last Modified: Tue, 24 Feb 2026 19:03:06 GMT  
		Size: 2.2 MB (2210411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c950303c16fe639587ececa73419dc844738b41140b423b7eb0384ea716267`  
		Last Modified: Tue, 24 Feb 2026 19:03:06 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e93319de4797e67380bf08f73a8c50f44a58bc5d48b1f23fb6f08e4ffeb6db10`  
		Last Modified: Tue, 24 Feb 2026 19:03:07 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:0cf62386cd305d86703ad800762c1372a34293bfad797b6a29e27282f3b1f3f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd0998a1e5967fa757cf01fe012763ec5c2a1924834b1b5b71293d9d8e6b6e73`

```dockerfile
```

-	Layers:
	-	`sha256:2a59dac704d61fc3b17645258ea234efe69b7e467c6e660e0226a6f828e75acf`  
		Last Modified: Tue, 24 Feb 2026 19:03:06 GMT  
		Size: 2.0 MB (2011293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10a2bc4477f2db7316f6a3b19832420a977c86d7e21d4eb855955079d793b60d`  
		Last Modified: Tue, 24 Feb 2026 19:03:06 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm variant v7

```console
$ docker pull memcached@sha256:be3fc72ab6cfa1ea6cf0e4934c88efff77606bf59e9b967282e0146142af3ded
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28514687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91c5981c3560c3a86da48563ea4ad119abd5a3afe1897a22de0465775fbba444`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:04:15 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 24 Feb 2026 19:04:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:07:24 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 24 Feb 2026 19:07:24 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 24 Feb 2026 19:07:24 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 24 Feb 2026 19:07:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 24 Feb 2026 19:07:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:07:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 24 Feb 2026 19:07:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:07:24 GMT
USER memcache
# Tue, 24 Feb 2026 19:07:24 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 24 Feb 2026 19:07:24 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1190ad5d6adaf3041f81179fb1a2a2ffd13c6236c4011b3b0e574b20a0240248`  
		Last Modified: Tue, 24 Feb 2026 19:07:30 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a4d01b331567500cc2848dc045c00005a609b0caa7819712aa4c0b1c36a602`  
		Last Modified: Tue, 24 Feb 2026 19:07:30 GMT  
		Size: 135.4 KB (135372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09feae8fb4ac83c32d5ac15d5578c16a87b563518fb4ece9bc65c0dd4eec4617`  
		Last Modified: Tue, 24 Feb 2026 19:07:30 GMT  
		Size: 2.2 MB (2164057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3f5af79bcb8f4d70c5d381d7623a5157340c864a02043363b99fd392b70a49`  
		Last Modified: Tue, 24 Feb 2026 19:07:30 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f525abc9eb110fb4d08a2fc9aec1c625c91ecc14675ea27b19ad4528db27e29`  
		Last Modified: Tue, 24 Feb 2026 19:07:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:0c0b5fadc4b970f34bfb9e213bc510f9cf711fee0d731866b79b9a7725bbfe67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d19c5e298b74d1907a036edbf16180a9c315d79341636a8d7283fd667a7f399`

```dockerfile
```

-	Layers:
	-	`sha256:bec22f2e6f0aa5f193a09a38b693ac428534a6f02b83ded0ae660639f5b2e63a`  
		Last Modified: Tue, 24 Feb 2026 19:07:31 GMT  
		Size: 2.0 MB (2009750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:535737c7b64de5d274415f285b181b237967739c8145f2a0c666ebc2addff27d`  
		Last Modified: Tue, 24 Feb 2026 19:07:31 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:383b83f45bfcba593d3017bf4e72398bad4c3d31bc3a92665c75cb44d6d8010a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32556427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:931b22f98bd50f35ac08c7bdbd76091693ea91dfeac1b0a01a1943fc1e5c7d34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:07:31 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 24 Feb 2026 19:07:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:10:30 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 24 Feb 2026 19:10:30 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 24 Feb 2026 19:10:30 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 24 Feb 2026 19:10:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 24 Feb 2026 19:10:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:10:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 24 Feb 2026 19:10:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:10:30 GMT
USER memcache
# Tue, 24 Feb 2026 19:10:30 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 24 Feb 2026 19:10:30 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da63b3df116854958d3edc49224f00f800f8feceb07f409a89da01a568acfd74`  
		Last Modified: Tue, 24 Feb 2026 19:10:35 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d7d6dca284320d75e2a6b070eba5471c445206c750390794bffa12a045cf25`  
		Last Modified: Tue, 24 Feb 2026 19:10:36 GMT  
		Size: 153.5 KB (153473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa939cfd8be671996b32d233394ecff0cb4ee1ad010d7d95d0ff847976387b7`  
		Last Modified: Tue, 24 Feb 2026 19:10:36 GMT  
		Size: 2.3 MB (2261343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82787d9b0b7359766dc7a263f2c52ad3c430ae67068af1de0a775f4039c2c11d`  
		Last Modified: Tue, 24 Feb 2026 19:10:36 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc91ce04553e029ee43de7fd212662cbb243747b9b554ccb2515963360487b78`  
		Last Modified: Tue, 24 Feb 2026 19:10:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:df115eb253a89a2fb8823967dfc90bb6eaef5f8c68d172c472e80a97983ea047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac6cbdb8c151703cc011a84d25f241b73c56094667b7b2e14f5b78f1567cb431`

```dockerfile
```

-	Layers:
	-	`sha256:1f68573ab5b0140c68ab975345114e497f510b3df716041482fc47ea1c8c1e97`  
		Last Modified: Tue, 24 Feb 2026 19:10:36 GMT  
		Size: 2.0 MB (2008606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3ed1c1193f31e42d639c05820912adaf7632e1444abe907acb5d020b2941c8c`  
		Last Modified: Tue, 24 Feb 2026 19:10:35 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; 386

```console
$ docker pull memcached@sha256:8d2616d6d6f7cf8b88e84529a283bb7d5905e04ab68b771d3da78c7faaa3863f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33666622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:060038b35b56cd38bd725bc0d26e82d247ead0b7723d50ad8efa423fd9a7e9a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 18:59:23 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 24 Feb 2026 18:59:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:02:23 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 24 Feb 2026 19:02:23 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 24 Feb 2026 19:02:23 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 24 Feb 2026 19:02:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 24 Feb 2026 19:02:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:02:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 24 Feb 2026 19:02:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:02:23 GMT
USER memcache
# Tue, 24 Feb 2026 19:02:23 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 24 Feb 2026 19:02:23 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f4e0b944ee1e7e50bdfbfa77bda370b6eccee7d698a7adca78c38f5ca0767ca5`  
		Last Modified: Tue, 24 Feb 2026 18:43:18 GMT  
		Size: 31.3 MB (31293918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7370c6d23e537397165580c793f3f488b5c1e3725032c34ddff16242efc509e`  
		Last Modified: Tue, 24 Feb 2026 19:02:29 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0af0c71eb6719f8e1973879b2ea81a32290a2bfdba4580598f838b40d74d0a9`  
		Last Modified: Tue, 24 Feb 2026 19:02:29 GMT  
		Size: 147.5 KB (147516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e12a16ad70a850a1f54b2b691348dd7e9a2f00ad453b2c79be3c6aeff3ef7b`  
		Last Modified: Tue, 24 Feb 2026 19:02:29 GMT  
		Size: 2.2 MB (2223676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8177c4ca17c056b8c5a4548fe0c9c760b3bbb1954ac900869d5efa1453c5ea`  
		Last Modified: Tue, 24 Feb 2026 19:02:29 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:272ec8dc3492083ced99bc57e9db1b10009f74c1c83b6795ed38c110fd42cdaf`  
		Last Modified: Tue, 24 Feb 2026 19:02:30 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:5070ac2246d76cda16369492c5adf738ae74e24f338e539a063259c5437cda2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c35cb195506953c3800638d94cb495f01b68d5bf564a91c0863c783a44e63495`

```dockerfile
```

-	Layers:
	-	`sha256:c87395201667ae86b09526c196163cf3d7ee8fef27350876c4d0e8889c5f026d`  
		Last Modified: Tue, 24 Feb 2026 19:02:29 GMT  
		Size: 2.0 MB (2005447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b3952676542fa0fbd53a1e5d2b08b33f01828e2ea0d9bdca0f6a44f980418e1`  
		Last Modified: Tue, 24 Feb 2026 19:02:29 GMT  
		Size: 22.1 KB (22094 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; ppc64le

```console
$ docker pull memcached@sha256:295640646e2e642c4ba4a954358685a29bd942df8b9a3fd0a8bf92346372c68a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36166011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a3c07f4fe24eef5f498b6370e9d70655e93d823d70348f0c03de8caa64bf5b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 24 Feb 2026 19:14:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:18:32 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 24 Feb 2026 19:18:32 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 24 Feb 2026 19:18:32 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 24 Feb 2026 19:18:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 24 Feb 2026 19:18:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:18:33 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 24 Feb 2026 19:18:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:18:33 GMT
USER memcache
# Tue, 24 Feb 2026 19:18:33 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 24 Feb 2026 19:18:33 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ad3fa262401e234341c4865354faecb35fd4a15ce23d4369debdd68a4e0ba1`  
		Last Modified: Tue, 24 Feb 2026 19:18:51 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37018ee7f60ce5d622bc47071034caa8643168e590eb82f2859530e295c2d74`  
		Last Modified: Tue, 24 Feb 2026 19:18:51 GMT  
		Size: 170.4 KB (170364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8293edd47a62890de39041653fd374133f7c81506463cd4c8f1fd3999c25c41a`  
		Last Modified: Tue, 24 Feb 2026 19:18:51 GMT  
		Size: 2.4 MB (2393913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54918c9a7df48c86af7a40a80c050b442a77e99b2a733c83726b0f546d6d9176`  
		Last Modified: Tue, 24 Feb 2026 19:18:51 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ae01ebdb25dffa16d71caa402e2f64eedeadcf5505f9afcb9b0deed17b6046`  
		Last Modified: Tue, 24 Feb 2026 19:18:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:9ed368016d333d4d55370690943777bae8f79c9f72a2e191366bfd728c2527e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b009746df9b6c47b18442bec8d9bd2eb4f7da37e6d23d23c7b3d106924496dc3`

```dockerfile
```

-	Layers:
	-	`sha256:0cd5dd42f5171c2e7ffb3ecfb193700298aa51685c923038e547720b7968393f`  
		Last Modified: Tue, 24 Feb 2026 19:18:51 GMT  
		Size: 2.0 MB (2011891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7f7951a0f59cb83944081d3c657d0a48918adcefc5ae2f3ee64a42c6cf4c144`  
		Last Modified: Tue, 24 Feb 2026 19:18:50 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; riscv64

```console
$ docker pull memcached@sha256:4d92d3a017ca8ca7948c884d9ee25e96e8e1838bb94d53dda569f07101262c74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30618541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b8cdde436a640517ee901b0927c2e128caa695cf3b0a71d4b3bd027993c2c10`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Wed, 25 Feb 2026 03:12:58 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 25 Feb 2026 03:13:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Feb 2026 03:27:04 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 25 Feb 2026 03:27:04 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 25 Feb 2026 03:27:04 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 25 Feb 2026 03:27:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 25 Feb 2026 03:27:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Feb 2026 03:27:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 25 Feb 2026 03:27:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Feb 2026 03:27:05 GMT
USER memcache
# Wed, 25 Feb 2026 03:27:05 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 25 Feb 2026 03:27:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fce183db3522d3b87ff4ec8768ec38313bc647df242c4d2245264321599e224`  
		Last Modified: Wed, 25 Feb 2026 03:27:51 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e1dbc92883ea2cad6fb0e4ff4a478e862dc760d2ec927369aa328b52592cb9`  
		Last Modified: Wed, 25 Feb 2026 03:27:51 GMT  
		Size: 133.1 KB (133074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c5718939dc18cc9d82791adad3e4ce75827c393387d12514f92f85467b359f`  
		Last Modified: Wed, 25 Feb 2026 03:27:51 GMT  
		Size: 2.2 MB (2207537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e44b817acb07e256823d291317d247cbe97bdbc55a0994ec267467d04b30022`  
		Last Modified: Wed, 25 Feb 2026 03:27:51 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:841d2d3e5a28536b578d3aab8c1da972de21a13e202997467bfa050b0dfe6a64`  
		Last Modified: Wed, 25 Feb 2026 03:27:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:a9b01e3fd82fcc2536a8b4f8a38b204a12799015583aaab4ff3ac8bcd7c192fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f57f541807865ade76a34e9e121a96114daa4ab2ca34a5c924d5d19255cb885d`

```dockerfile
```

-	Layers:
	-	`sha256:ce3f35cea1f210746ebccb073cfc7ce51878ce03482e8c9a09457641385bc443`  
		Last Modified: Wed, 25 Feb 2026 03:27:51 GMT  
		Size: 2.0 MB (2002254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba4ac2058d1632d5f3a3cf0698ec37889198d45cfe57218c131d295df9df13be`  
		Last Modified: Wed, 25 Feb 2026 03:27:51 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; s390x

```console
$ docker pull memcached@sha256:423ba67b801204b46b8a1dba1974e6f2e209639dbc48c62b9d33190987e2226f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32277818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:284d259d569d7694ea6f980a0e46469afbf8ca345caaf21a16df77cd30bd0759`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:01:44 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 24 Feb 2026 19:01:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:05:47 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 24 Feb 2026 19:05:47 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 24 Feb 2026 19:05:47 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 24 Feb 2026 19:05:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 24 Feb 2026 19:05:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:05:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 24 Feb 2026 19:05:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:05:47 GMT
USER memcache
# Tue, 24 Feb 2026 19:05:47 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 24 Feb 2026 19:05:47 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:604ba03d7a54182e1f14697e43fa7f23271204247cf53166e71e93154e0e1b7c`  
		Last Modified: Tue, 24 Feb 2026 19:06:02 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60f992885eee7a354d3a7f3a15cbe933eaf1769daaf5aeec0816188eee9c235`  
		Last Modified: Tue, 24 Feb 2026 19:06:02 GMT  
		Size: 140.5 KB (140518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ba39b84415354f148c7bf1358db39e8c60c8ee7d57aae315707efcbe4a97f8`  
		Last Modified: Tue, 24 Feb 2026 19:06:02 GMT  
		Size: 2.3 MB (2297608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:748f3d38558f1ce81c9c5df4831b79004bdd8407d6de9a1f6242190e6bdec648`  
		Last Modified: Tue, 24 Feb 2026 19:06:02 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d826358b929a42dd9b9a6eabd6d7f0bd6f454a14926713798750f8f4f58dacc7`  
		Last Modified: Tue, 24 Feb 2026 19:06:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:7db0b5141cc4d90b60e471db94061e9e1cd536bf5f19001772a4428dfcc06aa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c61de11a61ead852674daabea6eb13f5c704df55e4c57bef85fccde8e16dc89b`

```dockerfile
```

-	Layers:
	-	`sha256:3038f05f0370cca0449ad250c4f0a7f2ad5ead64983ea5fcb6604efc88eff2c6`  
		Last Modified: Tue, 24 Feb 2026 19:06:02 GMT  
		Size: 2.0 MB (2009727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5be29fae8812d4c817fe359ed16601d8204939006a63c3b9e676a4a5e7462b9`  
		Last Modified: Tue, 24 Feb 2026 19:06:02 GMT  
		Size: 22.2 KB (22152 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:trixie`

```console
$ docker pull memcached@sha256:572b011ce33954ee809066d8cecbeb3ec98912109ee3be3663a3197425fd81ac
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
$ docker pull memcached@sha256:023c4e23c94ba68b5a97a6f56c2828ebedc281e85a52ac0b2690b58700b3bb7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32195506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:033ea2f06d6420e86006806fd73fd124d41bf3a1ccfa612823af947b880ca8c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:04:39 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 24 Feb 2026 19:04:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:07:27 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 24 Feb 2026 19:07:27 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 24 Feb 2026 19:07:27 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 24 Feb 2026 19:07:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 24 Feb 2026 19:07:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:07:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 24 Feb 2026 19:07:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:07:27 GMT
USER memcache
# Tue, 24 Feb 2026 19:07:27 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 24 Feb 2026 19:07:27 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36056d8f6cc22203cda4cb7a7b65e6597244fb8468bf7015c6d9ae2e76f2e9a0`  
		Last Modified: Tue, 24 Feb 2026 19:07:33 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:185bddc36e29c3f75831b51c77695b60ce372b05fa6a05cdf757fd7224e140f7`  
		Last Modified: Tue, 24 Feb 2026 19:07:33 GMT  
		Size: 136.7 KB (136687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f8366e7d29ee7ccd518666350d7b6c8573a147053d8d883ec991efe322d5f5`  
		Last Modified: Tue, 24 Feb 2026 19:07:33 GMT  
		Size: 2.3 MB (2278677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd467f5caa7f19a29f886aeff83e2edf03c41832304f1a8d53b50ca9e97dc8c`  
		Last Modified: Tue, 24 Feb 2026 19:07:33 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6a0854d419bc2397f7c1b7ac5b15319f81aab68a1e055e271d32b69360dfcc`  
		Last Modified: Tue, 24 Feb 2026 19:07:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:93eb971a0f54e3ff33aa02af6d7ea3dbfc884c93129b25b2a433551d611e6877
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ec223135b79851b5f9b5ee88b297cefbf1858a2d669b454b60e27ff96d6512a`

```dockerfile
```

-	Layers:
	-	`sha256:7e3c52b39ce2400a537d122eef601ccaa8527c356dc34ba5e233ae089eca6bcc`  
		Last Modified: Tue, 24 Feb 2026 19:07:33 GMT  
		Size: 2.0 MB (2008290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4860fbffaac75568c714f1a1a433740f20ee1ce624d4bb3f82d7ebbb1c2e288e`  
		Last Modified: Tue, 24 Feb 2026 19:07:33 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; arm variant v5

```console
$ docker pull memcached@sha256:ba68b1eb22f8d62ea931bc8e125f0e795b01242209298c7f23060d94ea748463
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30303705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b00afbdbae6e13cdf413d8caed5854add790bb103c4ca68b363f971794cb651d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 18:59:37 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 24 Feb 2026 18:59:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:03:00 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 24 Feb 2026 19:03:00 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 24 Feb 2026 19:03:00 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 24 Feb 2026 19:03:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 24 Feb 2026 19:03:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:03:00 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 24 Feb 2026 19:03:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:03:00 GMT
USER memcache
# Tue, 24 Feb 2026 19:03:00 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 24 Feb 2026 19:03:00 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:280a075cc1d2a97445b9f4430aa9774bfc38fc4217b7fc9d6a7b04e7e431cb65`  
		Last Modified: Tue, 24 Feb 2026 18:42:44 GMT  
		Size: 27.9 MB (27947608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf8f6794c0e26d45659cabbb095050aeae71ae849a69981e8b0bbf72278c8a3`  
		Last Modified: Tue, 24 Feb 2026 19:03:06 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec23046983d4d416a3fdd21ee149b45f2d0adafd4951a0c1d3a2b6b5b46f0019`  
		Last Modified: Tue, 24 Feb 2026 19:03:06 GMT  
		Size: 144.2 KB (144174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238dcf6c237d3a80010ba1d7f9b108159fa5cbfa8c450954f88c1183ce4f3667`  
		Last Modified: Tue, 24 Feb 2026 19:03:06 GMT  
		Size: 2.2 MB (2210411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c950303c16fe639587ececa73419dc844738b41140b423b7eb0384ea716267`  
		Last Modified: Tue, 24 Feb 2026 19:03:06 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e93319de4797e67380bf08f73a8c50f44a58bc5d48b1f23fb6f08e4ffeb6db10`  
		Last Modified: Tue, 24 Feb 2026 19:03:07 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:0cf62386cd305d86703ad800762c1372a34293bfad797b6a29e27282f3b1f3f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd0998a1e5967fa757cf01fe012763ec5c2a1924834b1b5b71293d9d8e6b6e73`

```dockerfile
```

-	Layers:
	-	`sha256:2a59dac704d61fc3b17645258ea234efe69b7e467c6e660e0226a6f828e75acf`  
		Last Modified: Tue, 24 Feb 2026 19:03:06 GMT  
		Size: 2.0 MB (2011293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10a2bc4477f2db7316f6a3b19832420a977c86d7e21d4eb855955079d793b60d`  
		Last Modified: Tue, 24 Feb 2026 19:03:06 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; arm variant v7

```console
$ docker pull memcached@sha256:be3fc72ab6cfa1ea6cf0e4934c88efff77606bf59e9b967282e0146142af3ded
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28514687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91c5981c3560c3a86da48563ea4ad119abd5a3afe1897a22de0465775fbba444`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:04:15 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 24 Feb 2026 19:04:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:07:24 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 24 Feb 2026 19:07:24 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 24 Feb 2026 19:07:24 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 24 Feb 2026 19:07:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 24 Feb 2026 19:07:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:07:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 24 Feb 2026 19:07:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:07:24 GMT
USER memcache
# Tue, 24 Feb 2026 19:07:24 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 24 Feb 2026 19:07:24 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1190ad5d6adaf3041f81179fb1a2a2ffd13c6236c4011b3b0e574b20a0240248`  
		Last Modified: Tue, 24 Feb 2026 19:07:30 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a4d01b331567500cc2848dc045c00005a609b0caa7819712aa4c0b1c36a602`  
		Last Modified: Tue, 24 Feb 2026 19:07:30 GMT  
		Size: 135.4 KB (135372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09feae8fb4ac83c32d5ac15d5578c16a87b563518fb4ece9bc65c0dd4eec4617`  
		Last Modified: Tue, 24 Feb 2026 19:07:30 GMT  
		Size: 2.2 MB (2164057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3f5af79bcb8f4d70c5d381d7623a5157340c864a02043363b99fd392b70a49`  
		Last Modified: Tue, 24 Feb 2026 19:07:30 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f525abc9eb110fb4d08a2fc9aec1c625c91ecc14675ea27b19ad4528db27e29`  
		Last Modified: Tue, 24 Feb 2026 19:07:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:0c0b5fadc4b970f34bfb9e213bc510f9cf711fee0d731866b79b9a7725bbfe67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d19c5e298b74d1907a036edbf16180a9c315d79341636a8d7283fd667a7f399`

```dockerfile
```

-	Layers:
	-	`sha256:bec22f2e6f0aa5f193a09a38b693ac428534a6f02b83ded0ae660639f5b2e63a`  
		Last Modified: Tue, 24 Feb 2026 19:07:31 GMT  
		Size: 2.0 MB (2009750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:535737c7b64de5d274415f285b181b237967739c8145f2a0c666ebc2addff27d`  
		Last Modified: Tue, 24 Feb 2026 19:07:31 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:383b83f45bfcba593d3017bf4e72398bad4c3d31bc3a92665c75cb44d6d8010a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32556427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:931b22f98bd50f35ac08c7bdbd76091693ea91dfeac1b0a01a1943fc1e5c7d34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:07:31 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 24 Feb 2026 19:07:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:10:30 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 24 Feb 2026 19:10:30 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 24 Feb 2026 19:10:30 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 24 Feb 2026 19:10:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 24 Feb 2026 19:10:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:10:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 24 Feb 2026 19:10:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:10:30 GMT
USER memcache
# Tue, 24 Feb 2026 19:10:30 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 24 Feb 2026 19:10:30 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da63b3df116854958d3edc49224f00f800f8feceb07f409a89da01a568acfd74`  
		Last Modified: Tue, 24 Feb 2026 19:10:35 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d7d6dca284320d75e2a6b070eba5471c445206c750390794bffa12a045cf25`  
		Last Modified: Tue, 24 Feb 2026 19:10:36 GMT  
		Size: 153.5 KB (153473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa939cfd8be671996b32d233394ecff0cb4ee1ad010d7d95d0ff847976387b7`  
		Last Modified: Tue, 24 Feb 2026 19:10:36 GMT  
		Size: 2.3 MB (2261343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82787d9b0b7359766dc7a263f2c52ad3c430ae67068af1de0a775f4039c2c11d`  
		Last Modified: Tue, 24 Feb 2026 19:10:36 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc91ce04553e029ee43de7fd212662cbb243747b9b554ccb2515963360487b78`  
		Last Modified: Tue, 24 Feb 2026 19:10:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:df115eb253a89a2fb8823967dfc90bb6eaef5f8c68d172c472e80a97983ea047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac6cbdb8c151703cc011a84d25f241b73c56094667b7b2e14f5b78f1567cb431`

```dockerfile
```

-	Layers:
	-	`sha256:1f68573ab5b0140c68ab975345114e497f510b3df716041482fc47ea1c8c1e97`  
		Last Modified: Tue, 24 Feb 2026 19:10:36 GMT  
		Size: 2.0 MB (2008606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3ed1c1193f31e42d639c05820912adaf7632e1444abe907acb5d020b2941c8c`  
		Last Modified: Tue, 24 Feb 2026 19:10:35 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; 386

```console
$ docker pull memcached@sha256:8d2616d6d6f7cf8b88e84529a283bb7d5905e04ab68b771d3da78c7faaa3863f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33666622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:060038b35b56cd38bd725bc0d26e82d247ead0b7723d50ad8efa423fd9a7e9a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 18:59:23 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 24 Feb 2026 18:59:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:02:23 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 24 Feb 2026 19:02:23 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 24 Feb 2026 19:02:23 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 24 Feb 2026 19:02:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 24 Feb 2026 19:02:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:02:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 24 Feb 2026 19:02:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:02:23 GMT
USER memcache
# Tue, 24 Feb 2026 19:02:23 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 24 Feb 2026 19:02:23 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f4e0b944ee1e7e50bdfbfa77bda370b6eccee7d698a7adca78c38f5ca0767ca5`  
		Last Modified: Tue, 24 Feb 2026 18:43:18 GMT  
		Size: 31.3 MB (31293918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7370c6d23e537397165580c793f3f488b5c1e3725032c34ddff16242efc509e`  
		Last Modified: Tue, 24 Feb 2026 19:02:29 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0af0c71eb6719f8e1973879b2ea81a32290a2bfdba4580598f838b40d74d0a9`  
		Last Modified: Tue, 24 Feb 2026 19:02:29 GMT  
		Size: 147.5 KB (147516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e12a16ad70a850a1f54b2b691348dd7e9a2f00ad453b2c79be3c6aeff3ef7b`  
		Last Modified: Tue, 24 Feb 2026 19:02:29 GMT  
		Size: 2.2 MB (2223676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8177c4ca17c056b8c5a4548fe0c9c760b3bbb1954ac900869d5efa1453c5ea`  
		Last Modified: Tue, 24 Feb 2026 19:02:29 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:272ec8dc3492083ced99bc57e9db1b10009f74c1c83b6795ed38c110fd42cdaf`  
		Last Modified: Tue, 24 Feb 2026 19:02:30 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:5070ac2246d76cda16369492c5adf738ae74e24f338e539a063259c5437cda2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c35cb195506953c3800638d94cb495f01b68d5bf564a91c0863c783a44e63495`

```dockerfile
```

-	Layers:
	-	`sha256:c87395201667ae86b09526c196163cf3d7ee8fef27350876c4d0e8889c5f026d`  
		Last Modified: Tue, 24 Feb 2026 19:02:29 GMT  
		Size: 2.0 MB (2005447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b3952676542fa0fbd53a1e5d2b08b33f01828e2ea0d9bdca0f6a44f980418e1`  
		Last Modified: Tue, 24 Feb 2026 19:02:29 GMT  
		Size: 22.1 KB (22094 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; ppc64le

```console
$ docker pull memcached@sha256:295640646e2e642c4ba4a954358685a29bd942df8b9a3fd0a8bf92346372c68a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36166011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a3c07f4fe24eef5f498b6370e9d70655e93d823d70348f0c03de8caa64bf5b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 24 Feb 2026 19:14:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:18:32 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 24 Feb 2026 19:18:32 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 24 Feb 2026 19:18:32 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 24 Feb 2026 19:18:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 24 Feb 2026 19:18:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:18:33 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 24 Feb 2026 19:18:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:18:33 GMT
USER memcache
# Tue, 24 Feb 2026 19:18:33 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 24 Feb 2026 19:18:33 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ad3fa262401e234341c4865354faecb35fd4a15ce23d4369debdd68a4e0ba1`  
		Last Modified: Tue, 24 Feb 2026 19:18:51 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37018ee7f60ce5d622bc47071034caa8643168e590eb82f2859530e295c2d74`  
		Last Modified: Tue, 24 Feb 2026 19:18:51 GMT  
		Size: 170.4 KB (170364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8293edd47a62890de39041653fd374133f7c81506463cd4c8f1fd3999c25c41a`  
		Last Modified: Tue, 24 Feb 2026 19:18:51 GMT  
		Size: 2.4 MB (2393913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54918c9a7df48c86af7a40a80c050b442a77e99b2a733c83726b0f546d6d9176`  
		Last Modified: Tue, 24 Feb 2026 19:18:51 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ae01ebdb25dffa16d71caa402e2f64eedeadcf5505f9afcb9b0deed17b6046`  
		Last Modified: Tue, 24 Feb 2026 19:18:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:9ed368016d333d4d55370690943777bae8f79c9f72a2e191366bfd728c2527e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b009746df9b6c47b18442bec8d9bd2eb4f7da37e6d23d23c7b3d106924496dc3`

```dockerfile
```

-	Layers:
	-	`sha256:0cd5dd42f5171c2e7ffb3ecfb193700298aa51685c923038e547720b7968393f`  
		Last Modified: Tue, 24 Feb 2026 19:18:51 GMT  
		Size: 2.0 MB (2011891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7f7951a0f59cb83944081d3c657d0a48918adcefc5ae2f3ee64a42c6cf4c144`  
		Last Modified: Tue, 24 Feb 2026 19:18:50 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; riscv64

```console
$ docker pull memcached@sha256:4d92d3a017ca8ca7948c884d9ee25e96e8e1838bb94d53dda569f07101262c74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30618541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b8cdde436a640517ee901b0927c2e128caa695cf3b0a71d4b3bd027993c2c10`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Wed, 25 Feb 2026 03:12:58 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 25 Feb 2026 03:13:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Feb 2026 03:27:04 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 25 Feb 2026 03:27:04 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 25 Feb 2026 03:27:04 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 25 Feb 2026 03:27:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 25 Feb 2026 03:27:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Feb 2026 03:27:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 25 Feb 2026 03:27:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Feb 2026 03:27:05 GMT
USER memcache
# Wed, 25 Feb 2026 03:27:05 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 25 Feb 2026 03:27:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fce183db3522d3b87ff4ec8768ec38313bc647df242c4d2245264321599e224`  
		Last Modified: Wed, 25 Feb 2026 03:27:51 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e1dbc92883ea2cad6fb0e4ff4a478e862dc760d2ec927369aa328b52592cb9`  
		Last Modified: Wed, 25 Feb 2026 03:27:51 GMT  
		Size: 133.1 KB (133074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c5718939dc18cc9d82791adad3e4ce75827c393387d12514f92f85467b359f`  
		Last Modified: Wed, 25 Feb 2026 03:27:51 GMT  
		Size: 2.2 MB (2207537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e44b817acb07e256823d291317d247cbe97bdbc55a0994ec267467d04b30022`  
		Last Modified: Wed, 25 Feb 2026 03:27:51 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:841d2d3e5a28536b578d3aab8c1da972de21a13e202997467bfa050b0dfe6a64`  
		Last Modified: Wed, 25 Feb 2026 03:27:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:a9b01e3fd82fcc2536a8b4f8a38b204a12799015583aaab4ff3ac8bcd7c192fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f57f541807865ade76a34e9e121a96114daa4ab2ca34a5c924d5d19255cb885d`

```dockerfile
```

-	Layers:
	-	`sha256:ce3f35cea1f210746ebccb073cfc7ce51878ce03482e8c9a09457641385bc443`  
		Last Modified: Wed, 25 Feb 2026 03:27:51 GMT  
		Size: 2.0 MB (2002254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba4ac2058d1632d5f3a3cf0698ec37889198d45cfe57218c131d295df9df13be`  
		Last Modified: Wed, 25 Feb 2026 03:27:51 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; s390x

```console
$ docker pull memcached@sha256:423ba67b801204b46b8a1dba1974e6f2e209639dbc48c62b9d33190987e2226f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32277818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:284d259d569d7694ea6f980a0e46469afbf8ca345caaf21a16df77cd30bd0759`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:01:44 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 24 Feb 2026 19:01:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:05:47 GMT
ENV MEMCACHED_VERSION=1.6.40
# Tue, 24 Feb 2026 19:05:47 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Tue, 24 Feb 2026 19:05:47 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Tue, 24 Feb 2026 19:05:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 24 Feb 2026 19:05:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:05:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 24 Feb 2026 19:05:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:05:47 GMT
USER memcache
# Tue, 24 Feb 2026 19:05:47 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 24 Feb 2026 19:05:47 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:604ba03d7a54182e1f14697e43fa7f23271204247cf53166e71e93154e0e1b7c`  
		Last Modified: Tue, 24 Feb 2026 19:06:02 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60f992885eee7a354d3a7f3a15cbe933eaf1769daaf5aeec0816188eee9c235`  
		Last Modified: Tue, 24 Feb 2026 19:06:02 GMT  
		Size: 140.5 KB (140518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ba39b84415354f148c7bf1358db39e8c60c8ee7d57aae315707efcbe4a97f8`  
		Last Modified: Tue, 24 Feb 2026 19:06:02 GMT  
		Size: 2.3 MB (2297608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:748f3d38558f1ce81c9c5df4831b79004bdd8407d6de9a1f6242190e6bdec648`  
		Last Modified: Tue, 24 Feb 2026 19:06:02 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d826358b929a42dd9b9a6eabd6d7f0bd6f454a14926713798750f8f4f58dacc7`  
		Last Modified: Tue, 24 Feb 2026 19:06:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:7db0b5141cc4d90b60e471db94061e9e1cd536bf5f19001772a4428dfcc06aa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c61de11a61ead852674daabea6eb13f5c704df55e4c57bef85fccde8e16dc89b`

```dockerfile
```

-	Layers:
	-	`sha256:3038f05f0370cca0449ad250c4f0a7f2ad5ead64983ea5fcb6604efc88eff2c6`  
		Last Modified: Tue, 24 Feb 2026 19:06:02 GMT  
		Size: 2.0 MB (2009727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5be29fae8812d4c817fe359ed16601d8204939006a63c3b9e676a4a5e7462b9`  
		Last Modified: Tue, 24 Feb 2026 19:06:02 GMT  
		Size: 22.2 KB (22152 bytes)  
		MIME: application/vnd.in-toto+json
