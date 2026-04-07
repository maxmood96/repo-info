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
$ docker pull memcached@sha256:db739c92f80323018f33e3ddd392c7bb62c015280c7319f7e5dc207677ea3467
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
$ docker pull memcached@sha256:b788f2a69f7e53a4668d9e3a453544adace1d9f2515c87d16028be02b926b905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32194148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:957ebc2af9489fa034d85ce154bc33379c455514085cc54f8086e40af0b43dc1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:23:38 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 07 Apr 2026 01:23:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:26:29 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 07 Apr 2026 01:26:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 07 Apr 2026 01:26:29 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 07 Apr 2026 01:26:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 07 Apr 2026 01:26:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:26:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:26:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:26:29 GMT
USER memcache
# Tue, 07 Apr 2026 01:26:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 07 Apr 2026 01:26:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc6c716c6ddb3b32bea971a53985a917085b4cf120fff8d63d40df089226dc37`  
		Last Modified: Tue, 07 Apr 2026 01:26:35 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae9f08fb341368e75befbb98e1bb0ed398ec27d146ed1b86f063e558ec36994`  
		Last Modified: Tue, 07 Apr 2026 01:26:35 GMT  
		Size: 136.7 KB (136734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3715ece0607f0ad72fed1bab4785d71fb1f4a53248c7f0d0d728554d8a7e1d43`  
		Last Modified: Tue, 07 Apr 2026 01:26:35 GMT  
		Size: 2.3 MB (2280263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2587bd93e3d7081e72165f649bd56146508ef2a1d5bcecc34fc4a3c9e977c8cc`  
		Last Modified: Tue, 07 Apr 2026 01:26:35 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599d0131f8440d49de823ebacd72ff2b085e5b87424cb008b0fb9684815e96b1`  
		Last Modified: Tue, 07 Apr 2026 01:26:36 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:e52108fe5333bd921fcda699fa5e0a9a1f856476f94aa131ce3fca1bdc9c3333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8019a8ee5dc1bbcc7869825c68e49ab3cc98e0c26343fff78495facc0ed7166b`

```dockerfile
```

-	Layers:
	-	`sha256:3ee85043155b825da3cb759588dfd4ae9c5fb420241223c8eb0ea098db0d4352`  
		Last Modified: Tue, 07 Apr 2026 01:26:36 GMT  
		Size: 2.0 MB (2008326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63715707b27c7dcf51c74925a3a18c525a66f2a166fc8e44d63972b0c435d1eb`  
		Last Modified: Tue, 07 Apr 2026 01:26:35 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm variant v5

```console
$ docker pull memcached@sha256:df004aea9a02d7d4ee3ddc5465873404f20e8fa25c15e06d7b89d01d6cc1e356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30300952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea196d440f1b33851c03e3b418146249e09eb85317650c01e40dee92aa1966f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:36:58 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 07 Apr 2026 01:37:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:40:22 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 07 Apr 2026 01:40:22 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 07 Apr 2026 01:40:22 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 07 Apr 2026 01:40:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 07 Apr 2026 01:40:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:40:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:40:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:40:22 GMT
USER memcache
# Tue, 07 Apr 2026 01:40:22 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 07 Apr 2026 01:40:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3a32056c13d69abfd2a107f36cfc2049bdb6b52dbb76427fb9c1f688273f6bce`  
		Last Modified: Tue, 07 Apr 2026 00:11:10 GMT  
		Size: 27.9 MB (27943808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28da11ded538198c9b718c34fa43b8c4def75a2f31b50ed3a8bda92c1030d2f5`  
		Last Modified: Tue, 07 Apr 2026 01:40:28 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0cec49185fb79e2c1fd6b70122aa01ed8d60551bf8210a8c1266bc57db7262b`  
		Last Modified: Tue, 07 Apr 2026 01:40:28 GMT  
		Size: 144.2 KB (144201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:005ba68552dfbe267043ef794ab62753f9b67961868dc0a9948a3d153a6ab565`  
		Last Modified: Tue, 07 Apr 2026 01:40:28 GMT  
		Size: 2.2 MB (2211430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6514869f5fe8bb29cf6cd1481ed37590bf107b175195e617525696fe78550b`  
		Last Modified: Tue, 07 Apr 2026 01:40:28 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff4d287d37148bcd3c24209d83e46e78903ea757dce43fd6afc57731e84f401`  
		Last Modified: Tue, 07 Apr 2026 01:40:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:f240f6fbe003c002d394d498174c33dcc7af139322e3c52e5e090e7b49465c18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483b0a17344b9495480290bd9db97e169606d4a2ba8364d8018cb7464afc40a3`

```dockerfile
```

-	Layers:
	-	`sha256:2be307cba0a326ce27f955114acf18cc984e34bd185e2aad06e8d42126d6e019`  
		Last Modified: Tue, 07 Apr 2026 01:40:28 GMT  
		Size: 2.0 MB (2011329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1477528adcd0b2dbf9ee526a5e432557bcad4fedf5230183e7ba89f4132d2f36`  
		Last Modified: Tue, 07 Apr 2026 01:40:28 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm variant v7

```console
$ docker pull memcached@sha256:63893617a36fd6b52c4b87c082bae12bc14274921e436270f91bdced09696da8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28511650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb221d7cbc04c1704a1e11a7f3ec5fcec8e3409a06dadd58ea9e9e04b5e65fc7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:17:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 07 Apr 2026 01:17:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:20:21 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 07 Apr 2026 01:20:21 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 07 Apr 2026 01:20:21 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 07 Apr 2026 01:20:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 07 Apr 2026 01:20:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:20:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:20:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:20:21 GMT
USER memcache
# Tue, 07 Apr 2026 01:20:21 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 07 Apr 2026 01:20:21 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4c6d27739d1db2f26843c4e427219b60cd29d0d75a2f4c9eae2e732971275433`  
		Last Modified: Tue, 07 Apr 2026 01:00:39 GMT  
		Size: 26.2 MB (26209653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d53472c0d88747c450fe9d3a3ba402bff41134da0962fbc59dfddfc56bb7b2c`  
		Last Modified: Tue, 07 Apr 2026 01:20:27 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3911c933984424fe429e8a15f9ab53ec77e667a0217b071fa3d01a921dd25913`  
		Last Modified: Tue, 07 Apr 2026 01:20:27 GMT  
		Size: 135.4 KB (135405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df499710205ab866d69d874fc6de40178e60769f933a3d145604f2b641e48d1c`  
		Last Modified: Tue, 07 Apr 2026 01:20:27 GMT  
		Size: 2.2 MB (2165079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34502d029fbb87d2f994316b9034a00c81dc08a82c42bdac8f81991edd08d2dc`  
		Last Modified: Tue, 07 Apr 2026 01:20:27 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ffb0b865cbcbdeeb08432af5c96699db4b4d69822435141b3e0c6f4d63db69`  
		Last Modified: Tue, 07 Apr 2026 01:20:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:1736638210fa09980ce5ebd09ce778cb8bc99fde47be5e8919be7738a3343c97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a00642889a4ff9ad670d05a820454947cf9fe1dfd985a101e7ebaec77fd4e8d`

```dockerfile
```

-	Layers:
	-	`sha256:161d47d2d576cd7c620e85b92f138e51552979275c48f2972219108ac38ceeae`  
		Last Modified: Tue, 07 Apr 2026 01:20:27 GMT  
		Size: 2.0 MB (2009786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b60515cacf7c0e607b9ed02815936fe4979bb4980c85442fd2390bb5cad32ef9`  
		Last Modified: Tue, 07 Apr 2026 01:20:27 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:d998cfcd5bd550af6b2f9b9049095513de8f20594cc24c1bd7cad8c4ee6833d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32555698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee38d7a837c09c980e5060dea464fd640effc7729440b92dfd9bce0f3d0938fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:22:41 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 07 Apr 2026 01:22:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:25:43 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 07 Apr 2026 01:25:43 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 07 Apr 2026 01:25:43 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 07 Apr 2026 01:25:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 07 Apr 2026 01:25:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:25:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:25:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:25:43 GMT
USER memcache
# Tue, 07 Apr 2026 01:25:43 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 07 Apr 2026 01:25:43 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2b769d44c974357a7852d0b379e4db204456d0c805bc9c156302ce5d18e70a`  
		Last Modified: Tue, 07 Apr 2026 01:25:49 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c5c15e10eaaac316ae60d4fac40ff1017f02b2b875b407bf682c77298d93a7`  
		Last Modified: Tue, 07 Apr 2026 01:25:49 GMT  
		Size: 153.5 KB (153536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b4ed74f4e6520e66630e36cdb82c8f7ca27efc5933b5349505c1585057e90d`  
		Last Modified: Tue, 07 Apr 2026 01:25:49 GMT  
		Size: 2.3 MB (2262094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3e3951f2c6832a2e7b51f69b34a00904ca49fa4c6f41d57326d88e67efee443`  
		Last Modified: Tue, 07 Apr 2026 01:25:49 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca5d4a8d60cff74d81f68e759a28cf6eb088ee9cdf6a9c4addee256ae2077f7`  
		Last Modified: Tue, 07 Apr 2026 01:25:50 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:bbdcd7b1ee43fd986fc607ae612d760d1e019609ab9fbd3a0ecd4cc1f6633039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c8c88f72b4b8583399ce3dae76299eaccfe1e0817a4fbe7b2b69455600a6176`

```dockerfile
```

-	Layers:
	-	`sha256:1303514cbeaa570f5d824c226ba9dd6a62444501edb3f9993e3924bdbed20795`  
		Last Modified: Tue, 07 Apr 2026 01:25:49 GMT  
		Size: 2.0 MB (2008642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2aec570ce5326329f95567738d5d7f18b7d670eb63d25dcc3f4d8daa7ff1d7a`  
		Last Modified: Tue, 07 Apr 2026 01:25:49 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; 386

```console
$ docker pull memcached@sha256:14a8e0dca582269247d9148e01b5245b21dec2272071ca4f0de57bfe5da798ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33665093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20735a6c9bab36926f3fdc6fced1b8175cfe3f105a1bab23554f8456daea2896`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:16:16 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 07 Apr 2026 01:16:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:19:11 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 07 Apr 2026 01:19:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 07 Apr 2026 01:19:11 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 07 Apr 2026 01:19:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 07 Apr 2026 01:19:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:19:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:19:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:19:11 GMT
USER memcache
# Tue, 07 Apr 2026 01:19:11 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 07 Apr 2026 01:19:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3c3d391a832256e6eca1fcef63254ce2b8cf2d25bc53ac0b56d9de64a11a7f30`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 31.3 MB (31291252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2980a28d02ccf82ab767a9e89afc9e4c15e85753a882a8a2263a2c0691a1004c`  
		Last Modified: Tue, 07 Apr 2026 01:19:17 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28192b8169c943bc464428731249fa5ca713d3be14de53eda8e012b20cabeb2c`  
		Last Modified: Tue, 07 Apr 2026 01:19:17 GMT  
		Size: 147.6 KB (147564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29865350ef2f7a2af74486f1fb3649b504a46931ac3e09e8a07592896b665b2`  
		Last Modified: Tue, 07 Apr 2026 01:19:18 GMT  
		Size: 2.2 MB (2224764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d14265a50518850c61aebad318e069eef28a5e9b25658ec7de3279062fdfa0`  
		Last Modified: Tue, 07 Apr 2026 01:19:18 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ce4f1d852aaa9c090f21a5e62d9c34e913461645b4111373022564ec41227d`  
		Last Modified: Tue, 07 Apr 2026 01:19:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:0d86c338928dbeda1a6e986a64858fb0aed68a0f6c21e11882ec5ed8447078c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:075a856de16e6ed042abc19a38a81d43d11ecd7a857943cc72e8b6ddd7313cdc`

```dockerfile
```

-	Layers:
	-	`sha256:e5945497f00077342a9e73ad0d2cbc87810b1953e63c42228d117969dbfec8ee`  
		Last Modified: Tue, 07 Apr 2026 01:19:18 GMT  
		Size: 2.0 MB (2005483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46aed5ae982da715bb47a610f0f68cbf4b5326ce9401e5b9d9270b4aaeee19a1`  
		Last Modified: Tue, 07 Apr 2026 01:19:18 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; ppc64le

```console
$ docker pull memcached@sha256:92ac8b2eb8a499448552281cc533c85175af918bb0596c8dc74fd5b36a75bd9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36159274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b82cf6a623a63a6ae0c8138a0541bee731e8bd82763d58be64d6699c425fe2f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:35:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 07 Apr 2026 01:35:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:38:51 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 07 Apr 2026 01:38:51 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 07 Apr 2026 01:38:51 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 07 Apr 2026 01:38:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 07 Apr 2026 01:38:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:38:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:38:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:38:52 GMT
USER memcache
# Tue, 07 Apr 2026 01:38:52 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 07 Apr 2026 01:38:52 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e3428d4efac15fe7728b465c9c3bc5d71a07ad502becbd70250a2c560e32b53`  
		Last Modified: Tue, 07 Apr 2026 00:12:50 GMT  
		Size: 33.6 MB (33593016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7eee776338abb1e966582aa93d7c23fd9fcd920abfbbdd3cea4bce8cf338f2e`  
		Last Modified: Tue, 07 Apr 2026 01:39:10 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19eab5a207ad27e6d36357fcd01d34c3642fe0ed80f2f88a793cca9f476f30f7`  
		Last Modified: Tue, 07 Apr 2026 01:39:10 GMT  
		Size: 170.4 KB (170414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3625df055c4a6c1ff4e05c28e38811218be01d19aa2acc0795fc57b5de83d1be`  
		Last Modified: Tue, 07 Apr 2026 01:39:10 GMT  
		Size: 2.4 MB (2394331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd4414756055219a9ca9c5147693091d8b0eb78130291d723e0cb2c9ce300a9`  
		Last Modified: Tue, 07 Apr 2026 01:39:10 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5635c499788fcf6fe44b99aac274f62a1c7a5da6cc7b5aa86372cb6073bb209b`  
		Last Modified: Tue, 07 Apr 2026 01:39:11 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:2c06d5accf94e67fd3485443b1c72edccb0acad4470fe42460bc84e82ae9e65f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcd4dbec1613b0c5fc1bbb19ba085247f554ca63690b28c52441c0b058dde46e`

```dockerfile
```

-	Layers:
	-	`sha256:c3f3c4328760b53a1cc92c96577452cafa2c7320c7ed12f724fec785c444f5ed`  
		Last Modified: Tue, 07 Apr 2026 01:39:10 GMT  
		Size: 2.0 MB (2011927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bc399d77df625da1dc8870003a0130dbe6e49e04edbd00017af3b4b6189acc2`  
		Last Modified: Tue, 07 Apr 2026 01:39:10 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; riscv64

```console
$ docker pull memcached@sha256:343fd1c6e9e7f911bda94d07d87041db133ac3b59520418cf1583edfdc3ce77f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30618876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf8181bc4bb9dd1d641b682d8c26ed16fc76cbe854cee7b23e7f6ba281fb8047`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 04:59:33 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 07 Apr 2026 05:00:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 05:13:37 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 07 Apr 2026 05:13:37 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 07 Apr 2026 05:13:37 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 07 Apr 2026 05:13:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 07 Apr 2026 05:13:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 05:13:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 05:13:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 05:13:38 GMT
USER memcache
# Tue, 07 Apr 2026 05:13:38 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 07 Apr 2026 05:13:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:51128e253868f85aa5e3b9e86448414d946e8a6b685e02db1030aaa2b11e81d4`  
		Last Modified: Tue, 07 Apr 2026 01:55:37 GMT  
		Size: 28.3 MB (28275778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172bc18e8051f399e255dee35e79f9e5fa9aa64562d2a8516dd4182f4d4520f2`  
		Last Modified: Tue, 07 Apr 2026 05:14:23 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3677dcf4246be900eca90abef0e04b5b1e429066cc6b3a57604bd40e0c452b`  
		Last Modified: Tue, 07 Apr 2026 05:14:23 GMT  
		Size: 133.1 KB (133140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03668775341afe9414f4c7e2652b23d3086383a5816cb62b8fb69364eff41155`  
		Last Modified: Tue, 07 Apr 2026 05:14:24 GMT  
		Size: 2.2 MB (2208446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf395524f6f820cc7011bc1a2fcc5eba29e77275e6e044e4354d2614eea65f5`  
		Last Modified: Tue, 07 Apr 2026 05:14:23 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9f8103185e19fe4e971346e1109fa338f4d760dbb9e45dff1e3f928b8072dca`  
		Last Modified: Tue, 07 Apr 2026 05:14:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:b63ba37aad81705484c23176eb4f65464146117c69f7e8ff18a7768f27ace4ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a87be3b1386b7e3afd6748a7748bebffdafd2e21f6de7ad9f393c6719938cbc`

```dockerfile
```

-	Layers:
	-	`sha256:e7592dbf997c4d12b7436af51984acabb26f49a58b3ee14c6bc50f79a06a1845`  
		Last Modified: Tue, 07 Apr 2026 05:14:24 GMT  
		Size: 2.0 MB (2002290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f494bfe8ab328d634b3363d6b47b1bcc8e76f8982a3ffbb690421ebbcf84be6f`  
		Last Modified: Tue, 07 Apr 2026 05:14:23 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; s390x

```console
$ docker pull memcached@sha256:59e3f9c04b50a8743ccabeca5a84541d363991bd60c566bcbcff5ab0a1ade514
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32276001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e64324407ea5f5792674919ee94e90c11c6811d91a80f580cc94408724f09f98`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:23:36 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 07 Apr 2026 01:23:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:27:33 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 07 Apr 2026 01:27:33 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 07 Apr 2026 01:27:33 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 07 Apr 2026 01:27:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 07 Apr 2026 01:27:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:27:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:27:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:27:34 GMT
USER memcache
# Tue, 07 Apr 2026 01:27:34 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 07 Apr 2026 01:27:34 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:82e48a38ec87473a03164a244b5d8dfc2b55ef7a891305e41ee39d937de3c4a4`  
		Last Modified: Tue, 07 Apr 2026 00:13:47 GMT  
		Size: 29.8 MB (29835418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea198846c92f684bb855bad5d89ae842effe4af57b25418506f1776bc0aecc1d`  
		Last Modified: Tue, 07 Apr 2026 01:27:59 GMT  
		Size: 1.1 KB (1115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63dbd168e3da58f5483989937676b90f414dcc112658e545873c8eabd1d451a`  
		Last Modified: Tue, 07 Apr 2026 01:27:59 GMT  
		Size: 140.6 KB (140591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4b420453294ae853b5eb6817eedaf54a487727358ea0a41c0a6d91fbcf58a6`  
		Last Modified: Tue, 07 Apr 2026 01:27:59 GMT  
		Size: 2.3 MB (2298473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da8e2eac18f15307576ba0dc01cd984583807f983a57441622c7a5a41f0442ba`  
		Last Modified: Tue, 07 Apr 2026 01:27:59 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b5b25d6119e86ee9944ee5a8a604ae736fdeba1ff080bd84b774cbc11445b3e`  
		Last Modified: Tue, 07 Apr 2026 01:28:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:bd8097d65b8d6412d3ba3894adaef6aece7c4a57b12bac8838da6055b6e209fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b51a26520e00e9fcc204efc072451c2142451aef3b94f7e60d60532ae15662c`

```dockerfile
```

-	Layers:
	-	`sha256:a733a1255fb11524d515ae4a1ed12313958c1dd2d74cfb266144dc3c4fa044fc`  
		Last Modified: Tue, 07 Apr 2026 01:27:59 GMT  
		Size: 2.0 MB (2009763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8de5419a2a0f8a330a78a810bf9d25dbc33c70e95754f11bc392ffadf0372651`  
		Last Modified: Tue, 07 Apr 2026 01:27:59 GMT  
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
$ docker pull memcached@sha256:db739c92f80323018f33e3ddd392c7bb62c015280c7319f7e5dc207677ea3467
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
$ docker pull memcached@sha256:b788f2a69f7e53a4668d9e3a453544adace1d9f2515c87d16028be02b926b905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32194148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:957ebc2af9489fa034d85ce154bc33379c455514085cc54f8086e40af0b43dc1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:23:38 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 07 Apr 2026 01:23:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:26:29 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 07 Apr 2026 01:26:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 07 Apr 2026 01:26:29 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 07 Apr 2026 01:26:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 07 Apr 2026 01:26:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:26:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:26:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:26:29 GMT
USER memcache
# Tue, 07 Apr 2026 01:26:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 07 Apr 2026 01:26:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc6c716c6ddb3b32bea971a53985a917085b4cf120fff8d63d40df089226dc37`  
		Last Modified: Tue, 07 Apr 2026 01:26:35 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae9f08fb341368e75befbb98e1bb0ed398ec27d146ed1b86f063e558ec36994`  
		Last Modified: Tue, 07 Apr 2026 01:26:35 GMT  
		Size: 136.7 KB (136734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3715ece0607f0ad72fed1bab4785d71fb1f4a53248c7f0d0d728554d8a7e1d43`  
		Last Modified: Tue, 07 Apr 2026 01:26:35 GMT  
		Size: 2.3 MB (2280263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2587bd93e3d7081e72165f649bd56146508ef2a1d5bcecc34fc4a3c9e977c8cc`  
		Last Modified: Tue, 07 Apr 2026 01:26:35 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599d0131f8440d49de823ebacd72ff2b085e5b87424cb008b0fb9684815e96b1`  
		Last Modified: Tue, 07 Apr 2026 01:26:36 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:e52108fe5333bd921fcda699fa5e0a9a1f856476f94aa131ce3fca1bdc9c3333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8019a8ee5dc1bbcc7869825c68e49ab3cc98e0c26343fff78495facc0ed7166b`

```dockerfile
```

-	Layers:
	-	`sha256:3ee85043155b825da3cb759588dfd4ae9c5fb420241223c8eb0ea098db0d4352`  
		Last Modified: Tue, 07 Apr 2026 01:26:36 GMT  
		Size: 2.0 MB (2008326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63715707b27c7dcf51c74925a3a18c525a66f2a166fc8e44d63972b0c435d1eb`  
		Last Modified: Tue, 07 Apr 2026 01:26:35 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; arm variant v5

```console
$ docker pull memcached@sha256:df004aea9a02d7d4ee3ddc5465873404f20e8fa25c15e06d7b89d01d6cc1e356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30300952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea196d440f1b33851c03e3b418146249e09eb85317650c01e40dee92aa1966f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:36:58 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 07 Apr 2026 01:37:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:40:22 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 07 Apr 2026 01:40:22 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 07 Apr 2026 01:40:22 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 07 Apr 2026 01:40:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 07 Apr 2026 01:40:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:40:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:40:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:40:22 GMT
USER memcache
# Tue, 07 Apr 2026 01:40:22 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 07 Apr 2026 01:40:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3a32056c13d69abfd2a107f36cfc2049bdb6b52dbb76427fb9c1f688273f6bce`  
		Last Modified: Tue, 07 Apr 2026 00:11:10 GMT  
		Size: 27.9 MB (27943808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28da11ded538198c9b718c34fa43b8c4def75a2f31b50ed3a8bda92c1030d2f5`  
		Last Modified: Tue, 07 Apr 2026 01:40:28 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0cec49185fb79e2c1fd6b70122aa01ed8d60551bf8210a8c1266bc57db7262b`  
		Last Modified: Tue, 07 Apr 2026 01:40:28 GMT  
		Size: 144.2 KB (144201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:005ba68552dfbe267043ef794ab62753f9b67961868dc0a9948a3d153a6ab565`  
		Last Modified: Tue, 07 Apr 2026 01:40:28 GMT  
		Size: 2.2 MB (2211430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6514869f5fe8bb29cf6cd1481ed37590bf107b175195e617525696fe78550b`  
		Last Modified: Tue, 07 Apr 2026 01:40:28 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff4d287d37148bcd3c24209d83e46e78903ea757dce43fd6afc57731e84f401`  
		Last Modified: Tue, 07 Apr 2026 01:40:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:f240f6fbe003c002d394d498174c33dcc7af139322e3c52e5e090e7b49465c18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483b0a17344b9495480290bd9db97e169606d4a2ba8364d8018cb7464afc40a3`

```dockerfile
```

-	Layers:
	-	`sha256:2be307cba0a326ce27f955114acf18cc984e34bd185e2aad06e8d42126d6e019`  
		Last Modified: Tue, 07 Apr 2026 01:40:28 GMT  
		Size: 2.0 MB (2011329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1477528adcd0b2dbf9ee526a5e432557bcad4fedf5230183e7ba89f4132d2f36`  
		Last Modified: Tue, 07 Apr 2026 01:40:28 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; arm variant v7

```console
$ docker pull memcached@sha256:63893617a36fd6b52c4b87c082bae12bc14274921e436270f91bdced09696da8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28511650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb221d7cbc04c1704a1e11a7f3ec5fcec8e3409a06dadd58ea9e9e04b5e65fc7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:17:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 07 Apr 2026 01:17:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:20:21 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 07 Apr 2026 01:20:21 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 07 Apr 2026 01:20:21 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 07 Apr 2026 01:20:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 07 Apr 2026 01:20:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:20:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:20:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:20:21 GMT
USER memcache
# Tue, 07 Apr 2026 01:20:21 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 07 Apr 2026 01:20:21 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4c6d27739d1db2f26843c4e427219b60cd29d0d75a2f4c9eae2e732971275433`  
		Last Modified: Tue, 07 Apr 2026 01:00:39 GMT  
		Size: 26.2 MB (26209653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d53472c0d88747c450fe9d3a3ba402bff41134da0962fbc59dfddfc56bb7b2c`  
		Last Modified: Tue, 07 Apr 2026 01:20:27 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3911c933984424fe429e8a15f9ab53ec77e667a0217b071fa3d01a921dd25913`  
		Last Modified: Tue, 07 Apr 2026 01:20:27 GMT  
		Size: 135.4 KB (135405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df499710205ab866d69d874fc6de40178e60769f933a3d145604f2b641e48d1c`  
		Last Modified: Tue, 07 Apr 2026 01:20:27 GMT  
		Size: 2.2 MB (2165079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34502d029fbb87d2f994316b9034a00c81dc08a82c42bdac8f81991edd08d2dc`  
		Last Modified: Tue, 07 Apr 2026 01:20:27 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ffb0b865cbcbdeeb08432af5c96699db4b4d69822435141b3e0c6f4d63db69`  
		Last Modified: Tue, 07 Apr 2026 01:20:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:1736638210fa09980ce5ebd09ce778cb8bc99fde47be5e8919be7738a3343c97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a00642889a4ff9ad670d05a820454947cf9fe1dfd985a101e7ebaec77fd4e8d`

```dockerfile
```

-	Layers:
	-	`sha256:161d47d2d576cd7c620e85b92f138e51552979275c48f2972219108ac38ceeae`  
		Last Modified: Tue, 07 Apr 2026 01:20:27 GMT  
		Size: 2.0 MB (2009786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b60515cacf7c0e607b9ed02815936fe4979bb4980c85442fd2390bb5cad32ef9`  
		Last Modified: Tue, 07 Apr 2026 01:20:27 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:d998cfcd5bd550af6b2f9b9049095513de8f20594cc24c1bd7cad8c4ee6833d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32555698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee38d7a837c09c980e5060dea464fd640effc7729440b92dfd9bce0f3d0938fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:22:41 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 07 Apr 2026 01:22:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:25:43 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 07 Apr 2026 01:25:43 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 07 Apr 2026 01:25:43 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 07 Apr 2026 01:25:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 07 Apr 2026 01:25:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:25:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:25:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:25:43 GMT
USER memcache
# Tue, 07 Apr 2026 01:25:43 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 07 Apr 2026 01:25:43 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2b769d44c974357a7852d0b379e4db204456d0c805bc9c156302ce5d18e70a`  
		Last Modified: Tue, 07 Apr 2026 01:25:49 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c5c15e10eaaac316ae60d4fac40ff1017f02b2b875b407bf682c77298d93a7`  
		Last Modified: Tue, 07 Apr 2026 01:25:49 GMT  
		Size: 153.5 KB (153536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b4ed74f4e6520e66630e36cdb82c8f7ca27efc5933b5349505c1585057e90d`  
		Last Modified: Tue, 07 Apr 2026 01:25:49 GMT  
		Size: 2.3 MB (2262094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3e3951f2c6832a2e7b51f69b34a00904ca49fa4c6f41d57326d88e67efee443`  
		Last Modified: Tue, 07 Apr 2026 01:25:49 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca5d4a8d60cff74d81f68e759a28cf6eb088ee9cdf6a9c4addee256ae2077f7`  
		Last Modified: Tue, 07 Apr 2026 01:25:50 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:bbdcd7b1ee43fd986fc607ae612d760d1e019609ab9fbd3a0ecd4cc1f6633039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c8c88f72b4b8583399ce3dae76299eaccfe1e0817a4fbe7b2b69455600a6176`

```dockerfile
```

-	Layers:
	-	`sha256:1303514cbeaa570f5d824c226ba9dd6a62444501edb3f9993e3924bdbed20795`  
		Last Modified: Tue, 07 Apr 2026 01:25:49 GMT  
		Size: 2.0 MB (2008642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2aec570ce5326329f95567738d5d7f18b7d670eb63d25dcc3f4d8daa7ff1d7a`  
		Last Modified: Tue, 07 Apr 2026 01:25:49 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; 386

```console
$ docker pull memcached@sha256:14a8e0dca582269247d9148e01b5245b21dec2272071ca4f0de57bfe5da798ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33665093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20735a6c9bab36926f3fdc6fced1b8175cfe3f105a1bab23554f8456daea2896`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:16:16 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 07 Apr 2026 01:16:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:19:11 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 07 Apr 2026 01:19:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 07 Apr 2026 01:19:11 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 07 Apr 2026 01:19:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 07 Apr 2026 01:19:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:19:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:19:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:19:11 GMT
USER memcache
# Tue, 07 Apr 2026 01:19:11 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 07 Apr 2026 01:19:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3c3d391a832256e6eca1fcef63254ce2b8cf2d25bc53ac0b56d9de64a11a7f30`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 31.3 MB (31291252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2980a28d02ccf82ab767a9e89afc9e4c15e85753a882a8a2263a2c0691a1004c`  
		Last Modified: Tue, 07 Apr 2026 01:19:17 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28192b8169c943bc464428731249fa5ca713d3be14de53eda8e012b20cabeb2c`  
		Last Modified: Tue, 07 Apr 2026 01:19:17 GMT  
		Size: 147.6 KB (147564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29865350ef2f7a2af74486f1fb3649b504a46931ac3e09e8a07592896b665b2`  
		Last Modified: Tue, 07 Apr 2026 01:19:18 GMT  
		Size: 2.2 MB (2224764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d14265a50518850c61aebad318e069eef28a5e9b25658ec7de3279062fdfa0`  
		Last Modified: Tue, 07 Apr 2026 01:19:18 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ce4f1d852aaa9c090f21a5e62d9c34e913461645b4111373022564ec41227d`  
		Last Modified: Tue, 07 Apr 2026 01:19:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:0d86c338928dbeda1a6e986a64858fb0aed68a0f6c21e11882ec5ed8447078c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:075a856de16e6ed042abc19a38a81d43d11ecd7a857943cc72e8b6ddd7313cdc`

```dockerfile
```

-	Layers:
	-	`sha256:e5945497f00077342a9e73ad0d2cbc87810b1953e63c42228d117969dbfec8ee`  
		Last Modified: Tue, 07 Apr 2026 01:19:18 GMT  
		Size: 2.0 MB (2005483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46aed5ae982da715bb47a610f0f68cbf4b5326ce9401e5b9d9270b4aaeee19a1`  
		Last Modified: Tue, 07 Apr 2026 01:19:18 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; ppc64le

```console
$ docker pull memcached@sha256:92ac8b2eb8a499448552281cc533c85175af918bb0596c8dc74fd5b36a75bd9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36159274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b82cf6a623a63a6ae0c8138a0541bee731e8bd82763d58be64d6699c425fe2f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:35:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 07 Apr 2026 01:35:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:38:51 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 07 Apr 2026 01:38:51 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 07 Apr 2026 01:38:51 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 07 Apr 2026 01:38:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 07 Apr 2026 01:38:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:38:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:38:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:38:52 GMT
USER memcache
# Tue, 07 Apr 2026 01:38:52 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 07 Apr 2026 01:38:52 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e3428d4efac15fe7728b465c9c3bc5d71a07ad502becbd70250a2c560e32b53`  
		Last Modified: Tue, 07 Apr 2026 00:12:50 GMT  
		Size: 33.6 MB (33593016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7eee776338abb1e966582aa93d7c23fd9fcd920abfbbdd3cea4bce8cf338f2e`  
		Last Modified: Tue, 07 Apr 2026 01:39:10 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19eab5a207ad27e6d36357fcd01d34c3642fe0ed80f2f88a793cca9f476f30f7`  
		Last Modified: Tue, 07 Apr 2026 01:39:10 GMT  
		Size: 170.4 KB (170414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3625df055c4a6c1ff4e05c28e38811218be01d19aa2acc0795fc57b5de83d1be`  
		Last Modified: Tue, 07 Apr 2026 01:39:10 GMT  
		Size: 2.4 MB (2394331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd4414756055219a9ca9c5147693091d8b0eb78130291d723e0cb2c9ce300a9`  
		Last Modified: Tue, 07 Apr 2026 01:39:10 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5635c499788fcf6fe44b99aac274f62a1c7a5da6cc7b5aa86372cb6073bb209b`  
		Last Modified: Tue, 07 Apr 2026 01:39:11 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:2c06d5accf94e67fd3485443b1c72edccb0acad4470fe42460bc84e82ae9e65f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcd4dbec1613b0c5fc1bbb19ba085247f554ca63690b28c52441c0b058dde46e`

```dockerfile
```

-	Layers:
	-	`sha256:c3f3c4328760b53a1cc92c96577452cafa2c7320c7ed12f724fec785c444f5ed`  
		Last Modified: Tue, 07 Apr 2026 01:39:10 GMT  
		Size: 2.0 MB (2011927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bc399d77df625da1dc8870003a0130dbe6e49e04edbd00017af3b4b6189acc2`  
		Last Modified: Tue, 07 Apr 2026 01:39:10 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; riscv64

```console
$ docker pull memcached@sha256:343fd1c6e9e7f911bda94d07d87041db133ac3b59520418cf1583edfdc3ce77f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30618876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf8181bc4bb9dd1d641b682d8c26ed16fc76cbe854cee7b23e7f6ba281fb8047`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 04:59:33 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 07 Apr 2026 05:00:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 05:13:37 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 07 Apr 2026 05:13:37 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 07 Apr 2026 05:13:37 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 07 Apr 2026 05:13:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 07 Apr 2026 05:13:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 05:13:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 05:13:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 05:13:38 GMT
USER memcache
# Tue, 07 Apr 2026 05:13:38 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 07 Apr 2026 05:13:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:51128e253868f85aa5e3b9e86448414d946e8a6b685e02db1030aaa2b11e81d4`  
		Last Modified: Tue, 07 Apr 2026 01:55:37 GMT  
		Size: 28.3 MB (28275778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172bc18e8051f399e255dee35e79f9e5fa9aa64562d2a8516dd4182f4d4520f2`  
		Last Modified: Tue, 07 Apr 2026 05:14:23 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3677dcf4246be900eca90abef0e04b5b1e429066cc6b3a57604bd40e0c452b`  
		Last Modified: Tue, 07 Apr 2026 05:14:23 GMT  
		Size: 133.1 KB (133140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03668775341afe9414f4c7e2652b23d3086383a5816cb62b8fb69364eff41155`  
		Last Modified: Tue, 07 Apr 2026 05:14:24 GMT  
		Size: 2.2 MB (2208446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf395524f6f820cc7011bc1a2fcc5eba29e77275e6e044e4354d2614eea65f5`  
		Last Modified: Tue, 07 Apr 2026 05:14:23 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9f8103185e19fe4e971346e1109fa338f4d760dbb9e45dff1e3f928b8072dca`  
		Last Modified: Tue, 07 Apr 2026 05:14:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:b63ba37aad81705484c23176eb4f65464146117c69f7e8ff18a7768f27ace4ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a87be3b1386b7e3afd6748a7748bebffdafd2e21f6de7ad9f393c6719938cbc`

```dockerfile
```

-	Layers:
	-	`sha256:e7592dbf997c4d12b7436af51984acabb26f49a58b3ee14c6bc50f79a06a1845`  
		Last Modified: Tue, 07 Apr 2026 05:14:24 GMT  
		Size: 2.0 MB (2002290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f494bfe8ab328d634b3363d6b47b1bcc8e76f8982a3ffbb690421ebbcf84be6f`  
		Last Modified: Tue, 07 Apr 2026 05:14:23 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; s390x

```console
$ docker pull memcached@sha256:59e3f9c04b50a8743ccabeca5a84541d363991bd60c566bcbcff5ab0a1ade514
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32276001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e64324407ea5f5792674919ee94e90c11c6811d91a80f580cc94408724f09f98`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:23:36 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 07 Apr 2026 01:23:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:27:33 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 07 Apr 2026 01:27:33 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 07 Apr 2026 01:27:33 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 07 Apr 2026 01:27:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 07 Apr 2026 01:27:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:27:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:27:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:27:34 GMT
USER memcache
# Tue, 07 Apr 2026 01:27:34 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 07 Apr 2026 01:27:34 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:82e48a38ec87473a03164a244b5d8dfc2b55ef7a891305e41ee39d937de3c4a4`  
		Last Modified: Tue, 07 Apr 2026 00:13:47 GMT  
		Size: 29.8 MB (29835418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea198846c92f684bb855bad5d89ae842effe4af57b25418506f1776bc0aecc1d`  
		Last Modified: Tue, 07 Apr 2026 01:27:59 GMT  
		Size: 1.1 KB (1115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63dbd168e3da58f5483989937676b90f414dcc112658e545873c8eabd1d451a`  
		Last Modified: Tue, 07 Apr 2026 01:27:59 GMT  
		Size: 140.6 KB (140591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4b420453294ae853b5eb6817eedaf54a487727358ea0a41c0a6d91fbcf58a6`  
		Last Modified: Tue, 07 Apr 2026 01:27:59 GMT  
		Size: 2.3 MB (2298473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da8e2eac18f15307576ba0dc01cd984583807f983a57441622c7a5a41f0442ba`  
		Last Modified: Tue, 07 Apr 2026 01:27:59 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b5b25d6119e86ee9944ee5a8a604ae736fdeba1ff080bd84b774cbc11445b3e`  
		Last Modified: Tue, 07 Apr 2026 01:28:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:bd8097d65b8d6412d3ba3894adaef6aece7c4a57b12bac8838da6055b6e209fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b51a26520e00e9fcc204efc072451c2142451aef3b94f7e60d60532ae15662c`

```dockerfile
```

-	Layers:
	-	`sha256:a733a1255fb11524d515ae4a1ed12313958c1dd2d74cfb266144dc3c4fa044fc`  
		Last Modified: Tue, 07 Apr 2026 01:27:59 GMT  
		Size: 2.0 MB (2009763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8de5419a2a0f8a330a78a810bf9d25dbc33c70e95754f11bc392ffadf0372651`  
		Last Modified: Tue, 07 Apr 2026 01:27:59 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6`

```console
$ docker pull memcached@sha256:db739c92f80323018f33e3ddd392c7bb62c015280c7319f7e5dc207677ea3467
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
$ docker pull memcached@sha256:b788f2a69f7e53a4668d9e3a453544adace1d9f2515c87d16028be02b926b905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32194148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:957ebc2af9489fa034d85ce154bc33379c455514085cc54f8086e40af0b43dc1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:23:38 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 07 Apr 2026 01:23:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:26:29 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 07 Apr 2026 01:26:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 07 Apr 2026 01:26:29 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 07 Apr 2026 01:26:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 07 Apr 2026 01:26:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:26:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:26:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:26:29 GMT
USER memcache
# Tue, 07 Apr 2026 01:26:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 07 Apr 2026 01:26:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc6c716c6ddb3b32bea971a53985a917085b4cf120fff8d63d40df089226dc37`  
		Last Modified: Tue, 07 Apr 2026 01:26:35 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae9f08fb341368e75befbb98e1bb0ed398ec27d146ed1b86f063e558ec36994`  
		Last Modified: Tue, 07 Apr 2026 01:26:35 GMT  
		Size: 136.7 KB (136734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3715ece0607f0ad72fed1bab4785d71fb1f4a53248c7f0d0d728554d8a7e1d43`  
		Last Modified: Tue, 07 Apr 2026 01:26:35 GMT  
		Size: 2.3 MB (2280263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2587bd93e3d7081e72165f649bd56146508ef2a1d5bcecc34fc4a3c9e977c8cc`  
		Last Modified: Tue, 07 Apr 2026 01:26:35 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599d0131f8440d49de823ebacd72ff2b085e5b87424cb008b0fb9684815e96b1`  
		Last Modified: Tue, 07 Apr 2026 01:26:36 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:e52108fe5333bd921fcda699fa5e0a9a1f856476f94aa131ce3fca1bdc9c3333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8019a8ee5dc1bbcc7869825c68e49ab3cc98e0c26343fff78495facc0ed7166b`

```dockerfile
```

-	Layers:
	-	`sha256:3ee85043155b825da3cb759588dfd4ae9c5fb420241223c8eb0ea098db0d4352`  
		Last Modified: Tue, 07 Apr 2026 01:26:36 GMT  
		Size: 2.0 MB (2008326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63715707b27c7dcf51c74925a3a18c525a66f2a166fc8e44d63972b0c435d1eb`  
		Last Modified: Tue, 07 Apr 2026 01:26:35 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm variant v5

```console
$ docker pull memcached@sha256:df004aea9a02d7d4ee3ddc5465873404f20e8fa25c15e06d7b89d01d6cc1e356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30300952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea196d440f1b33851c03e3b418146249e09eb85317650c01e40dee92aa1966f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:36:58 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 07 Apr 2026 01:37:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:40:22 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 07 Apr 2026 01:40:22 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 07 Apr 2026 01:40:22 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 07 Apr 2026 01:40:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 07 Apr 2026 01:40:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:40:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:40:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:40:22 GMT
USER memcache
# Tue, 07 Apr 2026 01:40:22 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 07 Apr 2026 01:40:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3a32056c13d69abfd2a107f36cfc2049bdb6b52dbb76427fb9c1f688273f6bce`  
		Last Modified: Tue, 07 Apr 2026 00:11:10 GMT  
		Size: 27.9 MB (27943808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28da11ded538198c9b718c34fa43b8c4def75a2f31b50ed3a8bda92c1030d2f5`  
		Last Modified: Tue, 07 Apr 2026 01:40:28 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0cec49185fb79e2c1fd6b70122aa01ed8d60551bf8210a8c1266bc57db7262b`  
		Last Modified: Tue, 07 Apr 2026 01:40:28 GMT  
		Size: 144.2 KB (144201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:005ba68552dfbe267043ef794ab62753f9b67961868dc0a9948a3d153a6ab565`  
		Last Modified: Tue, 07 Apr 2026 01:40:28 GMT  
		Size: 2.2 MB (2211430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6514869f5fe8bb29cf6cd1481ed37590bf107b175195e617525696fe78550b`  
		Last Modified: Tue, 07 Apr 2026 01:40:28 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff4d287d37148bcd3c24209d83e46e78903ea757dce43fd6afc57731e84f401`  
		Last Modified: Tue, 07 Apr 2026 01:40:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:f240f6fbe003c002d394d498174c33dcc7af139322e3c52e5e090e7b49465c18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483b0a17344b9495480290bd9db97e169606d4a2ba8364d8018cb7464afc40a3`

```dockerfile
```

-	Layers:
	-	`sha256:2be307cba0a326ce27f955114acf18cc984e34bd185e2aad06e8d42126d6e019`  
		Last Modified: Tue, 07 Apr 2026 01:40:28 GMT  
		Size: 2.0 MB (2011329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1477528adcd0b2dbf9ee526a5e432557bcad4fedf5230183e7ba89f4132d2f36`  
		Last Modified: Tue, 07 Apr 2026 01:40:28 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm variant v7

```console
$ docker pull memcached@sha256:63893617a36fd6b52c4b87c082bae12bc14274921e436270f91bdced09696da8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28511650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb221d7cbc04c1704a1e11a7f3ec5fcec8e3409a06dadd58ea9e9e04b5e65fc7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:17:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 07 Apr 2026 01:17:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:20:21 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 07 Apr 2026 01:20:21 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 07 Apr 2026 01:20:21 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 07 Apr 2026 01:20:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 07 Apr 2026 01:20:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:20:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:20:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:20:21 GMT
USER memcache
# Tue, 07 Apr 2026 01:20:21 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 07 Apr 2026 01:20:21 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4c6d27739d1db2f26843c4e427219b60cd29d0d75a2f4c9eae2e732971275433`  
		Last Modified: Tue, 07 Apr 2026 01:00:39 GMT  
		Size: 26.2 MB (26209653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d53472c0d88747c450fe9d3a3ba402bff41134da0962fbc59dfddfc56bb7b2c`  
		Last Modified: Tue, 07 Apr 2026 01:20:27 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3911c933984424fe429e8a15f9ab53ec77e667a0217b071fa3d01a921dd25913`  
		Last Modified: Tue, 07 Apr 2026 01:20:27 GMT  
		Size: 135.4 KB (135405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df499710205ab866d69d874fc6de40178e60769f933a3d145604f2b641e48d1c`  
		Last Modified: Tue, 07 Apr 2026 01:20:27 GMT  
		Size: 2.2 MB (2165079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34502d029fbb87d2f994316b9034a00c81dc08a82c42bdac8f81991edd08d2dc`  
		Last Modified: Tue, 07 Apr 2026 01:20:27 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ffb0b865cbcbdeeb08432af5c96699db4b4d69822435141b3e0c6f4d63db69`  
		Last Modified: Tue, 07 Apr 2026 01:20:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:1736638210fa09980ce5ebd09ce778cb8bc99fde47be5e8919be7738a3343c97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a00642889a4ff9ad670d05a820454947cf9fe1dfd985a101e7ebaec77fd4e8d`

```dockerfile
```

-	Layers:
	-	`sha256:161d47d2d576cd7c620e85b92f138e51552979275c48f2972219108ac38ceeae`  
		Last Modified: Tue, 07 Apr 2026 01:20:27 GMT  
		Size: 2.0 MB (2009786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b60515cacf7c0e607b9ed02815936fe4979bb4980c85442fd2390bb5cad32ef9`  
		Last Modified: Tue, 07 Apr 2026 01:20:27 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:d998cfcd5bd550af6b2f9b9049095513de8f20594cc24c1bd7cad8c4ee6833d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32555698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee38d7a837c09c980e5060dea464fd640effc7729440b92dfd9bce0f3d0938fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:22:41 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 07 Apr 2026 01:22:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:25:43 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 07 Apr 2026 01:25:43 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 07 Apr 2026 01:25:43 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 07 Apr 2026 01:25:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 07 Apr 2026 01:25:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:25:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:25:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:25:43 GMT
USER memcache
# Tue, 07 Apr 2026 01:25:43 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 07 Apr 2026 01:25:43 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2b769d44c974357a7852d0b379e4db204456d0c805bc9c156302ce5d18e70a`  
		Last Modified: Tue, 07 Apr 2026 01:25:49 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c5c15e10eaaac316ae60d4fac40ff1017f02b2b875b407bf682c77298d93a7`  
		Last Modified: Tue, 07 Apr 2026 01:25:49 GMT  
		Size: 153.5 KB (153536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b4ed74f4e6520e66630e36cdb82c8f7ca27efc5933b5349505c1585057e90d`  
		Last Modified: Tue, 07 Apr 2026 01:25:49 GMT  
		Size: 2.3 MB (2262094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3e3951f2c6832a2e7b51f69b34a00904ca49fa4c6f41d57326d88e67efee443`  
		Last Modified: Tue, 07 Apr 2026 01:25:49 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca5d4a8d60cff74d81f68e759a28cf6eb088ee9cdf6a9c4addee256ae2077f7`  
		Last Modified: Tue, 07 Apr 2026 01:25:50 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:bbdcd7b1ee43fd986fc607ae612d760d1e019609ab9fbd3a0ecd4cc1f6633039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c8c88f72b4b8583399ce3dae76299eaccfe1e0817a4fbe7b2b69455600a6176`

```dockerfile
```

-	Layers:
	-	`sha256:1303514cbeaa570f5d824c226ba9dd6a62444501edb3f9993e3924bdbed20795`  
		Last Modified: Tue, 07 Apr 2026 01:25:49 GMT  
		Size: 2.0 MB (2008642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2aec570ce5326329f95567738d5d7f18b7d670eb63d25dcc3f4d8daa7ff1d7a`  
		Last Modified: Tue, 07 Apr 2026 01:25:49 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; 386

```console
$ docker pull memcached@sha256:14a8e0dca582269247d9148e01b5245b21dec2272071ca4f0de57bfe5da798ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33665093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20735a6c9bab36926f3fdc6fced1b8175cfe3f105a1bab23554f8456daea2896`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:16:16 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 07 Apr 2026 01:16:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:19:11 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 07 Apr 2026 01:19:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 07 Apr 2026 01:19:11 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 07 Apr 2026 01:19:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 07 Apr 2026 01:19:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:19:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:19:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:19:11 GMT
USER memcache
# Tue, 07 Apr 2026 01:19:11 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 07 Apr 2026 01:19:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3c3d391a832256e6eca1fcef63254ce2b8cf2d25bc53ac0b56d9de64a11a7f30`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 31.3 MB (31291252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2980a28d02ccf82ab767a9e89afc9e4c15e85753a882a8a2263a2c0691a1004c`  
		Last Modified: Tue, 07 Apr 2026 01:19:17 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28192b8169c943bc464428731249fa5ca713d3be14de53eda8e012b20cabeb2c`  
		Last Modified: Tue, 07 Apr 2026 01:19:17 GMT  
		Size: 147.6 KB (147564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29865350ef2f7a2af74486f1fb3649b504a46931ac3e09e8a07592896b665b2`  
		Last Modified: Tue, 07 Apr 2026 01:19:18 GMT  
		Size: 2.2 MB (2224764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d14265a50518850c61aebad318e069eef28a5e9b25658ec7de3279062fdfa0`  
		Last Modified: Tue, 07 Apr 2026 01:19:18 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ce4f1d852aaa9c090f21a5e62d9c34e913461645b4111373022564ec41227d`  
		Last Modified: Tue, 07 Apr 2026 01:19:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:0d86c338928dbeda1a6e986a64858fb0aed68a0f6c21e11882ec5ed8447078c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:075a856de16e6ed042abc19a38a81d43d11ecd7a857943cc72e8b6ddd7313cdc`

```dockerfile
```

-	Layers:
	-	`sha256:e5945497f00077342a9e73ad0d2cbc87810b1953e63c42228d117969dbfec8ee`  
		Last Modified: Tue, 07 Apr 2026 01:19:18 GMT  
		Size: 2.0 MB (2005483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46aed5ae982da715bb47a610f0f68cbf4b5326ce9401e5b9d9270b4aaeee19a1`  
		Last Modified: Tue, 07 Apr 2026 01:19:18 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; ppc64le

```console
$ docker pull memcached@sha256:92ac8b2eb8a499448552281cc533c85175af918bb0596c8dc74fd5b36a75bd9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36159274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b82cf6a623a63a6ae0c8138a0541bee731e8bd82763d58be64d6699c425fe2f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:35:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 07 Apr 2026 01:35:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:38:51 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 07 Apr 2026 01:38:51 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 07 Apr 2026 01:38:51 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 07 Apr 2026 01:38:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 07 Apr 2026 01:38:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:38:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:38:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:38:52 GMT
USER memcache
# Tue, 07 Apr 2026 01:38:52 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 07 Apr 2026 01:38:52 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e3428d4efac15fe7728b465c9c3bc5d71a07ad502becbd70250a2c560e32b53`  
		Last Modified: Tue, 07 Apr 2026 00:12:50 GMT  
		Size: 33.6 MB (33593016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7eee776338abb1e966582aa93d7c23fd9fcd920abfbbdd3cea4bce8cf338f2e`  
		Last Modified: Tue, 07 Apr 2026 01:39:10 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19eab5a207ad27e6d36357fcd01d34c3642fe0ed80f2f88a793cca9f476f30f7`  
		Last Modified: Tue, 07 Apr 2026 01:39:10 GMT  
		Size: 170.4 KB (170414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3625df055c4a6c1ff4e05c28e38811218be01d19aa2acc0795fc57b5de83d1be`  
		Last Modified: Tue, 07 Apr 2026 01:39:10 GMT  
		Size: 2.4 MB (2394331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd4414756055219a9ca9c5147693091d8b0eb78130291d723e0cb2c9ce300a9`  
		Last Modified: Tue, 07 Apr 2026 01:39:10 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5635c499788fcf6fe44b99aac274f62a1c7a5da6cc7b5aa86372cb6073bb209b`  
		Last Modified: Tue, 07 Apr 2026 01:39:11 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:2c06d5accf94e67fd3485443b1c72edccb0acad4470fe42460bc84e82ae9e65f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcd4dbec1613b0c5fc1bbb19ba085247f554ca63690b28c52441c0b058dde46e`

```dockerfile
```

-	Layers:
	-	`sha256:c3f3c4328760b53a1cc92c96577452cafa2c7320c7ed12f724fec785c444f5ed`  
		Last Modified: Tue, 07 Apr 2026 01:39:10 GMT  
		Size: 2.0 MB (2011927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bc399d77df625da1dc8870003a0130dbe6e49e04edbd00017af3b4b6189acc2`  
		Last Modified: Tue, 07 Apr 2026 01:39:10 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; riscv64

```console
$ docker pull memcached@sha256:343fd1c6e9e7f911bda94d07d87041db133ac3b59520418cf1583edfdc3ce77f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30618876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf8181bc4bb9dd1d641b682d8c26ed16fc76cbe854cee7b23e7f6ba281fb8047`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 04:59:33 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 07 Apr 2026 05:00:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 05:13:37 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 07 Apr 2026 05:13:37 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 07 Apr 2026 05:13:37 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 07 Apr 2026 05:13:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 07 Apr 2026 05:13:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 05:13:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 05:13:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 05:13:38 GMT
USER memcache
# Tue, 07 Apr 2026 05:13:38 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 07 Apr 2026 05:13:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:51128e253868f85aa5e3b9e86448414d946e8a6b685e02db1030aaa2b11e81d4`  
		Last Modified: Tue, 07 Apr 2026 01:55:37 GMT  
		Size: 28.3 MB (28275778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172bc18e8051f399e255dee35e79f9e5fa9aa64562d2a8516dd4182f4d4520f2`  
		Last Modified: Tue, 07 Apr 2026 05:14:23 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3677dcf4246be900eca90abef0e04b5b1e429066cc6b3a57604bd40e0c452b`  
		Last Modified: Tue, 07 Apr 2026 05:14:23 GMT  
		Size: 133.1 KB (133140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03668775341afe9414f4c7e2652b23d3086383a5816cb62b8fb69364eff41155`  
		Last Modified: Tue, 07 Apr 2026 05:14:24 GMT  
		Size: 2.2 MB (2208446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf395524f6f820cc7011bc1a2fcc5eba29e77275e6e044e4354d2614eea65f5`  
		Last Modified: Tue, 07 Apr 2026 05:14:23 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9f8103185e19fe4e971346e1109fa338f4d760dbb9e45dff1e3f928b8072dca`  
		Last Modified: Tue, 07 Apr 2026 05:14:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:b63ba37aad81705484c23176eb4f65464146117c69f7e8ff18a7768f27ace4ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a87be3b1386b7e3afd6748a7748bebffdafd2e21f6de7ad9f393c6719938cbc`

```dockerfile
```

-	Layers:
	-	`sha256:e7592dbf997c4d12b7436af51984acabb26f49a58b3ee14c6bc50f79a06a1845`  
		Last Modified: Tue, 07 Apr 2026 05:14:24 GMT  
		Size: 2.0 MB (2002290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f494bfe8ab328d634b3363d6b47b1bcc8e76f8982a3ffbb690421ebbcf84be6f`  
		Last Modified: Tue, 07 Apr 2026 05:14:23 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; s390x

```console
$ docker pull memcached@sha256:59e3f9c04b50a8743ccabeca5a84541d363991bd60c566bcbcff5ab0a1ade514
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32276001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e64324407ea5f5792674919ee94e90c11c6811d91a80f580cc94408724f09f98`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:23:36 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 07 Apr 2026 01:23:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:27:33 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 07 Apr 2026 01:27:33 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 07 Apr 2026 01:27:33 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 07 Apr 2026 01:27:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 07 Apr 2026 01:27:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:27:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:27:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:27:34 GMT
USER memcache
# Tue, 07 Apr 2026 01:27:34 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 07 Apr 2026 01:27:34 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:82e48a38ec87473a03164a244b5d8dfc2b55ef7a891305e41ee39d937de3c4a4`  
		Last Modified: Tue, 07 Apr 2026 00:13:47 GMT  
		Size: 29.8 MB (29835418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea198846c92f684bb855bad5d89ae842effe4af57b25418506f1776bc0aecc1d`  
		Last Modified: Tue, 07 Apr 2026 01:27:59 GMT  
		Size: 1.1 KB (1115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63dbd168e3da58f5483989937676b90f414dcc112658e545873c8eabd1d451a`  
		Last Modified: Tue, 07 Apr 2026 01:27:59 GMT  
		Size: 140.6 KB (140591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4b420453294ae853b5eb6817eedaf54a487727358ea0a41c0a6d91fbcf58a6`  
		Last Modified: Tue, 07 Apr 2026 01:27:59 GMT  
		Size: 2.3 MB (2298473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da8e2eac18f15307576ba0dc01cd984583807f983a57441622c7a5a41f0442ba`  
		Last Modified: Tue, 07 Apr 2026 01:27:59 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b5b25d6119e86ee9944ee5a8a604ae736fdeba1ff080bd84b774cbc11445b3e`  
		Last Modified: Tue, 07 Apr 2026 01:28:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:bd8097d65b8d6412d3ba3894adaef6aece7c4a57b12bac8838da6055b6e209fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b51a26520e00e9fcc204efc072451c2142451aef3b94f7e60d60532ae15662c`

```dockerfile
```

-	Layers:
	-	`sha256:a733a1255fb11524d515ae4a1ed12313958c1dd2d74cfb266144dc3c4fa044fc`  
		Last Modified: Tue, 07 Apr 2026 01:27:59 GMT  
		Size: 2.0 MB (2009763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8de5419a2a0f8a330a78a810bf9d25dbc33c70e95754f11bc392ffadf0372651`  
		Last Modified: Tue, 07 Apr 2026 01:27:59 GMT  
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
$ docker pull memcached@sha256:db739c92f80323018f33e3ddd392c7bb62c015280c7319f7e5dc207677ea3467
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
$ docker pull memcached@sha256:b788f2a69f7e53a4668d9e3a453544adace1d9f2515c87d16028be02b926b905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32194148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:957ebc2af9489fa034d85ce154bc33379c455514085cc54f8086e40af0b43dc1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:23:38 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 07 Apr 2026 01:23:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:26:29 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 07 Apr 2026 01:26:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 07 Apr 2026 01:26:29 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 07 Apr 2026 01:26:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 07 Apr 2026 01:26:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:26:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:26:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:26:29 GMT
USER memcache
# Tue, 07 Apr 2026 01:26:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 07 Apr 2026 01:26:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc6c716c6ddb3b32bea971a53985a917085b4cf120fff8d63d40df089226dc37`  
		Last Modified: Tue, 07 Apr 2026 01:26:35 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae9f08fb341368e75befbb98e1bb0ed398ec27d146ed1b86f063e558ec36994`  
		Last Modified: Tue, 07 Apr 2026 01:26:35 GMT  
		Size: 136.7 KB (136734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3715ece0607f0ad72fed1bab4785d71fb1f4a53248c7f0d0d728554d8a7e1d43`  
		Last Modified: Tue, 07 Apr 2026 01:26:35 GMT  
		Size: 2.3 MB (2280263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2587bd93e3d7081e72165f649bd56146508ef2a1d5bcecc34fc4a3c9e977c8cc`  
		Last Modified: Tue, 07 Apr 2026 01:26:35 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599d0131f8440d49de823ebacd72ff2b085e5b87424cb008b0fb9684815e96b1`  
		Last Modified: Tue, 07 Apr 2026 01:26:36 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:e52108fe5333bd921fcda699fa5e0a9a1f856476f94aa131ce3fca1bdc9c3333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8019a8ee5dc1bbcc7869825c68e49ab3cc98e0c26343fff78495facc0ed7166b`

```dockerfile
```

-	Layers:
	-	`sha256:3ee85043155b825da3cb759588dfd4ae9c5fb420241223c8eb0ea098db0d4352`  
		Last Modified: Tue, 07 Apr 2026 01:26:36 GMT  
		Size: 2.0 MB (2008326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63715707b27c7dcf51c74925a3a18c525a66f2a166fc8e44d63972b0c435d1eb`  
		Last Modified: Tue, 07 Apr 2026 01:26:35 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; arm variant v5

```console
$ docker pull memcached@sha256:df004aea9a02d7d4ee3ddc5465873404f20e8fa25c15e06d7b89d01d6cc1e356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30300952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea196d440f1b33851c03e3b418146249e09eb85317650c01e40dee92aa1966f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:36:58 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 07 Apr 2026 01:37:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:40:22 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 07 Apr 2026 01:40:22 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 07 Apr 2026 01:40:22 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 07 Apr 2026 01:40:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 07 Apr 2026 01:40:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:40:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:40:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:40:22 GMT
USER memcache
# Tue, 07 Apr 2026 01:40:22 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 07 Apr 2026 01:40:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3a32056c13d69abfd2a107f36cfc2049bdb6b52dbb76427fb9c1f688273f6bce`  
		Last Modified: Tue, 07 Apr 2026 00:11:10 GMT  
		Size: 27.9 MB (27943808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28da11ded538198c9b718c34fa43b8c4def75a2f31b50ed3a8bda92c1030d2f5`  
		Last Modified: Tue, 07 Apr 2026 01:40:28 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0cec49185fb79e2c1fd6b70122aa01ed8d60551bf8210a8c1266bc57db7262b`  
		Last Modified: Tue, 07 Apr 2026 01:40:28 GMT  
		Size: 144.2 KB (144201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:005ba68552dfbe267043ef794ab62753f9b67961868dc0a9948a3d153a6ab565`  
		Last Modified: Tue, 07 Apr 2026 01:40:28 GMT  
		Size: 2.2 MB (2211430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6514869f5fe8bb29cf6cd1481ed37590bf107b175195e617525696fe78550b`  
		Last Modified: Tue, 07 Apr 2026 01:40:28 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff4d287d37148bcd3c24209d83e46e78903ea757dce43fd6afc57731e84f401`  
		Last Modified: Tue, 07 Apr 2026 01:40:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:f240f6fbe003c002d394d498174c33dcc7af139322e3c52e5e090e7b49465c18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483b0a17344b9495480290bd9db97e169606d4a2ba8364d8018cb7464afc40a3`

```dockerfile
```

-	Layers:
	-	`sha256:2be307cba0a326ce27f955114acf18cc984e34bd185e2aad06e8d42126d6e019`  
		Last Modified: Tue, 07 Apr 2026 01:40:28 GMT  
		Size: 2.0 MB (2011329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1477528adcd0b2dbf9ee526a5e432557bcad4fedf5230183e7ba89f4132d2f36`  
		Last Modified: Tue, 07 Apr 2026 01:40:28 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; arm variant v7

```console
$ docker pull memcached@sha256:63893617a36fd6b52c4b87c082bae12bc14274921e436270f91bdced09696da8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28511650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb221d7cbc04c1704a1e11a7f3ec5fcec8e3409a06dadd58ea9e9e04b5e65fc7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:17:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 07 Apr 2026 01:17:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:20:21 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 07 Apr 2026 01:20:21 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 07 Apr 2026 01:20:21 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 07 Apr 2026 01:20:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 07 Apr 2026 01:20:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:20:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:20:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:20:21 GMT
USER memcache
# Tue, 07 Apr 2026 01:20:21 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 07 Apr 2026 01:20:21 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4c6d27739d1db2f26843c4e427219b60cd29d0d75a2f4c9eae2e732971275433`  
		Last Modified: Tue, 07 Apr 2026 01:00:39 GMT  
		Size: 26.2 MB (26209653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d53472c0d88747c450fe9d3a3ba402bff41134da0962fbc59dfddfc56bb7b2c`  
		Last Modified: Tue, 07 Apr 2026 01:20:27 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3911c933984424fe429e8a15f9ab53ec77e667a0217b071fa3d01a921dd25913`  
		Last Modified: Tue, 07 Apr 2026 01:20:27 GMT  
		Size: 135.4 KB (135405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df499710205ab866d69d874fc6de40178e60769f933a3d145604f2b641e48d1c`  
		Last Modified: Tue, 07 Apr 2026 01:20:27 GMT  
		Size: 2.2 MB (2165079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34502d029fbb87d2f994316b9034a00c81dc08a82c42bdac8f81991edd08d2dc`  
		Last Modified: Tue, 07 Apr 2026 01:20:27 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ffb0b865cbcbdeeb08432af5c96699db4b4d69822435141b3e0c6f4d63db69`  
		Last Modified: Tue, 07 Apr 2026 01:20:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:1736638210fa09980ce5ebd09ce778cb8bc99fde47be5e8919be7738a3343c97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a00642889a4ff9ad670d05a820454947cf9fe1dfd985a101e7ebaec77fd4e8d`

```dockerfile
```

-	Layers:
	-	`sha256:161d47d2d576cd7c620e85b92f138e51552979275c48f2972219108ac38ceeae`  
		Last Modified: Tue, 07 Apr 2026 01:20:27 GMT  
		Size: 2.0 MB (2009786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b60515cacf7c0e607b9ed02815936fe4979bb4980c85442fd2390bb5cad32ef9`  
		Last Modified: Tue, 07 Apr 2026 01:20:27 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:d998cfcd5bd550af6b2f9b9049095513de8f20594cc24c1bd7cad8c4ee6833d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32555698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee38d7a837c09c980e5060dea464fd640effc7729440b92dfd9bce0f3d0938fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:22:41 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 07 Apr 2026 01:22:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:25:43 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 07 Apr 2026 01:25:43 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 07 Apr 2026 01:25:43 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 07 Apr 2026 01:25:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 07 Apr 2026 01:25:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:25:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:25:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:25:43 GMT
USER memcache
# Tue, 07 Apr 2026 01:25:43 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 07 Apr 2026 01:25:43 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2b769d44c974357a7852d0b379e4db204456d0c805bc9c156302ce5d18e70a`  
		Last Modified: Tue, 07 Apr 2026 01:25:49 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c5c15e10eaaac316ae60d4fac40ff1017f02b2b875b407bf682c77298d93a7`  
		Last Modified: Tue, 07 Apr 2026 01:25:49 GMT  
		Size: 153.5 KB (153536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b4ed74f4e6520e66630e36cdb82c8f7ca27efc5933b5349505c1585057e90d`  
		Last Modified: Tue, 07 Apr 2026 01:25:49 GMT  
		Size: 2.3 MB (2262094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3e3951f2c6832a2e7b51f69b34a00904ca49fa4c6f41d57326d88e67efee443`  
		Last Modified: Tue, 07 Apr 2026 01:25:49 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca5d4a8d60cff74d81f68e759a28cf6eb088ee9cdf6a9c4addee256ae2077f7`  
		Last Modified: Tue, 07 Apr 2026 01:25:50 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:bbdcd7b1ee43fd986fc607ae612d760d1e019609ab9fbd3a0ecd4cc1f6633039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c8c88f72b4b8583399ce3dae76299eaccfe1e0817a4fbe7b2b69455600a6176`

```dockerfile
```

-	Layers:
	-	`sha256:1303514cbeaa570f5d824c226ba9dd6a62444501edb3f9993e3924bdbed20795`  
		Last Modified: Tue, 07 Apr 2026 01:25:49 GMT  
		Size: 2.0 MB (2008642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2aec570ce5326329f95567738d5d7f18b7d670eb63d25dcc3f4d8daa7ff1d7a`  
		Last Modified: Tue, 07 Apr 2026 01:25:49 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; 386

```console
$ docker pull memcached@sha256:14a8e0dca582269247d9148e01b5245b21dec2272071ca4f0de57bfe5da798ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33665093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20735a6c9bab36926f3fdc6fced1b8175cfe3f105a1bab23554f8456daea2896`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:16:16 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 07 Apr 2026 01:16:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:19:11 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 07 Apr 2026 01:19:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 07 Apr 2026 01:19:11 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 07 Apr 2026 01:19:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 07 Apr 2026 01:19:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:19:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:19:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:19:11 GMT
USER memcache
# Tue, 07 Apr 2026 01:19:11 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 07 Apr 2026 01:19:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3c3d391a832256e6eca1fcef63254ce2b8cf2d25bc53ac0b56d9de64a11a7f30`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 31.3 MB (31291252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2980a28d02ccf82ab767a9e89afc9e4c15e85753a882a8a2263a2c0691a1004c`  
		Last Modified: Tue, 07 Apr 2026 01:19:17 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28192b8169c943bc464428731249fa5ca713d3be14de53eda8e012b20cabeb2c`  
		Last Modified: Tue, 07 Apr 2026 01:19:17 GMT  
		Size: 147.6 KB (147564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29865350ef2f7a2af74486f1fb3649b504a46931ac3e09e8a07592896b665b2`  
		Last Modified: Tue, 07 Apr 2026 01:19:18 GMT  
		Size: 2.2 MB (2224764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d14265a50518850c61aebad318e069eef28a5e9b25658ec7de3279062fdfa0`  
		Last Modified: Tue, 07 Apr 2026 01:19:18 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ce4f1d852aaa9c090f21a5e62d9c34e913461645b4111373022564ec41227d`  
		Last Modified: Tue, 07 Apr 2026 01:19:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:0d86c338928dbeda1a6e986a64858fb0aed68a0f6c21e11882ec5ed8447078c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:075a856de16e6ed042abc19a38a81d43d11ecd7a857943cc72e8b6ddd7313cdc`

```dockerfile
```

-	Layers:
	-	`sha256:e5945497f00077342a9e73ad0d2cbc87810b1953e63c42228d117969dbfec8ee`  
		Last Modified: Tue, 07 Apr 2026 01:19:18 GMT  
		Size: 2.0 MB (2005483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46aed5ae982da715bb47a610f0f68cbf4b5326ce9401e5b9d9270b4aaeee19a1`  
		Last Modified: Tue, 07 Apr 2026 01:19:18 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; ppc64le

```console
$ docker pull memcached@sha256:92ac8b2eb8a499448552281cc533c85175af918bb0596c8dc74fd5b36a75bd9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36159274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b82cf6a623a63a6ae0c8138a0541bee731e8bd82763d58be64d6699c425fe2f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:35:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 07 Apr 2026 01:35:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:38:51 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 07 Apr 2026 01:38:51 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 07 Apr 2026 01:38:51 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 07 Apr 2026 01:38:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 07 Apr 2026 01:38:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:38:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:38:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:38:52 GMT
USER memcache
# Tue, 07 Apr 2026 01:38:52 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 07 Apr 2026 01:38:52 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e3428d4efac15fe7728b465c9c3bc5d71a07ad502becbd70250a2c560e32b53`  
		Last Modified: Tue, 07 Apr 2026 00:12:50 GMT  
		Size: 33.6 MB (33593016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7eee776338abb1e966582aa93d7c23fd9fcd920abfbbdd3cea4bce8cf338f2e`  
		Last Modified: Tue, 07 Apr 2026 01:39:10 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19eab5a207ad27e6d36357fcd01d34c3642fe0ed80f2f88a793cca9f476f30f7`  
		Last Modified: Tue, 07 Apr 2026 01:39:10 GMT  
		Size: 170.4 KB (170414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3625df055c4a6c1ff4e05c28e38811218be01d19aa2acc0795fc57b5de83d1be`  
		Last Modified: Tue, 07 Apr 2026 01:39:10 GMT  
		Size: 2.4 MB (2394331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd4414756055219a9ca9c5147693091d8b0eb78130291d723e0cb2c9ce300a9`  
		Last Modified: Tue, 07 Apr 2026 01:39:10 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5635c499788fcf6fe44b99aac274f62a1c7a5da6cc7b5aa86372cb6073bb209b`  
		Last Modified: Tue, 07 Apr 2026 01:39:11 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:2c06d5accf94e67fd3485443b1c72edccb0acad4470fe42460bc84e82ae9e65f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcd4dbec1613b0c5fc1bbb19ba085247f554ca63690b28c52441c0b058dde46e`

```dockerfile
```

-	Layers:
	-	`sha256:c3f3c4328760b53a1cc92c96577452cafa2c7320c7ed12f724fec785c444f5ed`  
		Last Modified: Tue, 07 Apr 2026 01:39:10 GMT  
		Size: 2.0 MB (2011927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bc399d77df625da1dc8870003a0130dbe6e49e04edbd00017af3b4b6189acc2`  
		Last Modified: Tue, 07 Apr 2026 01:39:10 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; riscv64

```console
$ docker pull memcached@sha256:343fd1c6e9e7f911bda94d07d87041db133ac3b59520418cf1583edfdc3ce77f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30618876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf8181bc4bb9dd1d641b682d8c26ed16fc76cbe854cee7b23e7f6ba281fb8047`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 04:59:33 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 07 Apr 2026 05:00:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 05:13:37 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 07 Apr 2026 05:13:37 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 07 Apr 2026 05:13:37 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 07 Apr 2026 05:13:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 07 Apr 2026 05:13:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 05:13:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 05:13:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 05:13:38 GMT
USER memcache
# Tue, 07 Apr 2026 05:13:38 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 07 Apr 2026 05:13:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:51128e253868f85aa5e3b9e86448414d946e8a6b685e02db1030aaa2b11e81d4`  
		Last Modified: Tue, 07 Apr 2026 01:55:37 GMT  
		Size: 28.3 MB (28275778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172bc18e8051f399e255dee35e79f9e5fa9aa64562d2a8516dd4182f4d4520f2`  
		Last Modified: Tue, 07 Apr 2026 05:14:23 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3677dcf4246be900eca90abef0e04b5b1e429066cc6b3a57604bd40e0c452b`  
		Last Modified: Tue, 07 Apr 2026 05:14:23 GMT  
		Size: 133.1 KB (133140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03668775341afe9414f4c7e2652b23d3086383a5816cb62b8fb69364eff41155`  
		Last Modified: Tue, 07 Apr 2026 05:14:24 GMT  
		Size: 2.2 MB (2208446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf395524f6f820cc7011bc1a2fcc5eba29e77275e6e044e4354d2614eea65f5`  
		Last Modified: Tue, 07 Apr 2026 05:14:23 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9f8103185e19fe4e971346e1109fa338f4d760dbb9e45dff1e3f928b8072dca`  
		Last Modified: Tue, 07 Apr 2026 05:14:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:b63ba37aad81705484c23176eb4f65464146117c69f7e8ff18a7768f27ace4ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a87be3b1386b7e3afd6748a7748bebffdafd2e21f6de7ad9f393c6719938cbc`

```dockerfile
```

-	Layers:
	-	`sha256:e7592dbf997c4d12b7436af51984acabb26f49a58b3ee14c6bc50f79a06a1845`  
		Last Modified: Tue, 07 Apr 2026 05:14:24 GMT  
		Size: 2.0 MB (2002290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f494bfe8ab328d634b3363d6b47b1bcc8e76f8982a3ffbb690421ebbcf84be6f`  
		Last Modified: Tue, 07 Apr 2026 05:14:23 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; s390x

```console
$ docker pull memcached@sha256:59e3f9c04b50a8743ccabeca5a84541d363991bd60c566bcbcff5ab0a1ade514
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32276001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e64324407ea5f5792674919ee94e90c11c6811d91a80f580cc94408724f09f98`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:23:36 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 07 Apr 2026 01:23:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:27:33 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 07 Apr 2026 01:27:33 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 07 Apr 2026 01:27:33 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 07 Apr 2026 01:27:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 07 Apr 2026 01:27:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:27:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:27:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:27:34 GMT
USER memcache
# Tue, 07 Apr 2026 01:27:34 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 07 Apr 2026 01:27:34 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:82e48a38ec87473a03164a244b5d8dfc2b55ef7a891305e41ee39d937de3c4a4`  
		Last Modified: Tue, 07 Apr 2026 00:13:47 GMT  
		Size: 29.8 MB (29835418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea198846c92f684bb855bad5d89ae842effe4af57b25418506f1776bc0aecc1d`  
		Last Modified: Tue, 07 Apr 2026 01:27:59 GMT  
		Size: 1.1 KB (1115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63dbd168e3da58f5483989937676b90f414dcc112658e545873c8eabd1d451a`  
		Last Modified: Tue, 07 Apr 2026 01:27:59 GMT  
		Size: 140.6 KB (140591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4b420453294ae853b5eb6817eedaf54a487727358ea0a41c0a6d91fbcf58a6`  
		Last Modified: Tue, 07 Apr 2026 01:27:59 GMT  
		Size: 2.3 MB (2298473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da8e2eac18f15307576ba0dc01cd984583807f983a57441622c7a5a41f0442ba`  
		Last Modified: Tue, 07 Apr 2026 01:27:59 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b5b25d6119e86ee9944ee5a8a604ae736fdeba1ff080bd84b774cbc11445b3e`  
		Last Modified: Tue, 07 Apr 2026 01:28:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:bd8097d65b8d6412d3ba3894adaef6aece7c4a57b12bac8838da6055b6e209fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b51a26520e00e9fcc204efc072451c2142451aef3b94f7e60d60532ae15662c`

```dockerfile
```

-	Layers:
	-	`sha256:a733a1255fb11524d515ae4a1ed12313958c1dd2d74cfb266144dc3c4fa044fc`  
		Last Modified: Tue, 07 Apr 2026 01:27:59 GMT  
		Size: 2.0 MB (2009763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8de5419a2a0f8a330a78a810bf9d25dbc33c70e95754f11bc392ffadf0372651`  
		Last Modified: Tue, 07 Apr 2026 01:27:59 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.41`

```console
$ docker pull memcached@sha256:db739c92f80323018f33e3ddd392c7bb62c015280c7319f7e5dc207677ea3467
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
$ docker pull memcached@sha256:b788f2a69f7e53a4668d9e3a453544adace1d9f2515c87d16028be02b926b905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32194148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:957ebc2af9489fa034d85ce154bc33379c455514085cc54f8086e40af0b43dc1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:23:38 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 07 Apr 2026 01:23:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:26:29 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 07 Apr 2026 01:26:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 07 Apr 2026 01:26:29 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 07 Apr 2026 01:26:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 07 Apr 2026 01:26:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:26:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:26:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:26:29 GMT
USER memcache
# Tue, 07 Apr 2026 01:26:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 07 Apr 2026 01:26:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc6c716c6ddb3b32bea971a53985a917085b4cf120fff8d63d40df089226dc37`  
		Last Modified: Tue, 07 Apr 2026 01:26:35 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae9f08fb341368e75befbb98e1bb0ed398ec27d146ed1b86f063e558ec36994`  
		Last Modified: Tue, 07 Apr 2026 01:26:35 GMT  
		Size: 136.7 KB (136734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3715ece0607f0ad72fed1bab4785d71fb1f4a53248c7f0d0d728554d8a7e1d43`  
		Last Modified: Tue, 07 Apr 2026 01:26:35 GMT  
		Size: 2.3 MB (2280263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2587bd93e3d7081e72165f649bd56146508ef2a1d5bcecc34fc4a3c9e977c8cc`  
		Last Modified: Tue, 07 Apr 2026 01:26:35 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599d0131f8440d49de823ebacd72ff2b085e5b87424cb008b0fb9684815e96b1`  
		Last Modified: Tue, 07 Apr 2026 01:26:36 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41` - unknown; unknown

```console
$ docker pull memcached@sha256:e52108fe5333bd921fcda699fa5e0a9a1f856476f94aa131ce3fca1bdc9c3333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8019a8ee5dc1bbcc7869825c68e49ab3cc98e0c26343fff78495facc0ed7166b`

```dockerfile
```

-	Layers:
	-	`sha256:3ee85043155b825da3cb759588dfd4ae9c5fb420241223c8eb0ea098db0d4352`  
		Last Modified: Tue, 07 Apr 2026 01:26:36 GMT  
		Size: 2.0 MB (2008326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63715707b27c7dcf51c74925a3a18c525a66f2a166fc8e44d63972b0c435d1eb`  
		Last Modified: Tue, 07 Apr 2026 01:26:35 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41` - linux; arm variant v5

```console
$ docker pull memcached@sha256:df004aea9a02d7d4ee3ddc5465873404f20e8fa25c15e06d7b89d01d6cc1e356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30300952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea196d440f1b33851c03e3b418146249e09eb85317650c01e40dee92aa1966f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:36:58 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 07 Apr 2026 01:37:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:40:22 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 07 Apr 2026 01:40:22 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 07 Apr 2026 01:40:22 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 07 Apr 2026 01:40:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 07 Apr 2026 01:40:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:40:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:40:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:40:22 GMT
USER memcache
# Tue, 07 Apr 2026 01:40:22 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 07 Apr 2026 01:40:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3a32056c13d69abfd2a107f36cfc2049bdb6b52dbb76427fb9c1f688273f6bce`  
		Last Modified: Tue, 07 Apr 2026 00:11:10 GMT  
		Size: 27.9 MB (27943808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28da11ded538198c9b718c34fa43b8c4def75a2f31b50ed3a8bda92c1030d2f5`  
		Last Modified: Tue, 07 Apr 2026 01:40:28 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0cec49185fb79e2c1fd6b70122aa01ed8d60551bf8210a8c1266bc57db7262b`  
		Last Modified: Tue, 07 Apr 2026 01:40:28 GMT  
		Size: 144.2 KB (144201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:005ba68552dfbe267043ef794ab62753f9b67961868dc0a9948a3d153a6ab565`  
		Last Modified: Tue, 07 Apr 2026 01:40:28 GMT  
		Size: 2.2 MB (2211430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6514869f5fe8bb29cf6cd1481ed37590bf107b175195e617525696fe78550b`  
		Last Modified: Tue, 07 Apr 2026 01:40:28 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff4d287d37148bcd3c24209d83e46e78903ea757dce43fd6afc57731e84f401`  
		Last Modified: Tue, 07 Apr 2026 01:40:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41` - unknown; unknown

```console
$ docker pull memcached@sha256:f240f6fbe003c002d394d498174c33dcc7af139322e3c52e5e090e7b49465c18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483b0a17344b9495480290bd9db97e169606d4a2ba8364d8018cb7464afc40a3`

```dockerfile
```

-	Layers:
	-	`sha256:2be307cba0a326ce27f955114acf18cc984e34bd185e2aad06e8d42126d6e019`  
		Last Modified: Tue, 07 Apr 2026 01:40:28 GMT  
		Size: 2.0 MB (2011329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1477528adcd0b2dbf9ee526a5e432557bcad4fedf5230183e7ba89f4132d2f36`  
		Last Modified: Tue, 07 Apr 2026 01:40:28 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41` - linux; arm variant v7

```console
$ docker pull memcached@sha256:63893617a36fd6b52c4b87c082bae12bc14274921e436270f91bdced09696da8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28511650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb221d7cbc04c1704a1e11a7f3ec5fcec8e3409a06dadd58ea9e9e04b5e65fc7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:17:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 07 Apr 2026 01:17:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:20:21 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 07 Apr 2026 01:20:21 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 07 Apr 2026 01:20:21 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 07 Apr 2026 01:20:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 07 Apr 2026 01:20:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:20:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:20:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:20:21 GMT
USER memcache
# Tue, 07 Apr 2026 01:20:21 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 07 Apr 2026 01:20:21 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4c6d27739d1db2f26843c4e427219b60cd29d0d75a2f4c9eae2e732971275433`  
		Last Modified: Tue, 07 Apr 2026 01:00:39 GMT  
		Size: 26.2 MB (26209653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d53472c0d88747c450fe9d3a3ba402bff41134da0962fbc59dfddfc56bb7b2c`  
		Last Modified: Tue, 07 Apr 2026 01:20:27 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3911c933984424fe429e8a15f9ab53ec77e667a0217b071fa3d01a921dd25913`  
		Last Modified: Tue, 07 Apr 2026 01:20:27 GMT  
		Size: 135.4 KB (135405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df499710205ab866d69d874fc6de40178e60769f933a3d145604f2b641e48d1c`  
		Last Modified: Tue, 07 Apr 2026 01:20:27 GMT  
		Size: 2.2 MB (2165079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34502d029fbb87d2f994316b9034a00c81dc08a82c42bdac8f81991edd08d2dc`  
		Last Modified: Tue, 07 Apr 2026 01:20:27 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ffb0b865cbcbdeeb08432af5c96699db4b4d69822435141b3e0c6f4d63db69`  
		Last Modified: Tue, 07 Apr 2026 01:20:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41` - unknown; unknown

```console
$ docker pull memcached@sha256:1736638210fa09980ce5ebd09ce778cb8bc99fde47be5e8919be7738a3343c97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a00642889a4ff9ad670d05a820454947cf9fe1dfd985a101e7ebaec77fd4e8d`

```dockerfile
```

-	Layers:
	-	`sha256:161d47d2d576cd7c620e85b92f138e51552979275c48f2972219108ac38ceeae`  
		Last Modified: Tue, 07 Apr 2026 01:20:27 GMT  
		Size: 2.0 MB (2009786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b60515cacf7c0e607b9ed02815936fe4979bb4980c85442fd2390bb5cad32ef9`  
		Last Modified: Tue, 07 Apr 2026 01:20:27 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:d998cfcd5bd550af6b2f9b9049095513de8f20594cc24c1bd7cad8c4ee6833d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32555698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee38d7a837c09c980e5060dea464fd640effc7729440b92dfd9bce0f3d0938fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:22:41 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 07 Apr 2026 01:22:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:25:43 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 07 Apr 2026 01:25:43 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 07 Apr 2026 01:25:43 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 07 Apr 2026 01:25:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 07 Apr 2026 01:25:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:25:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:25:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:25:43 GMT
USER memcache
# Tue, 07 Apr 2026 01:25:43 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 07 Apr 2026 01:25:43 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2b769d44c974357a7852d0b379e4db204456d0c805bc9c156302ce5d18e70a`  
		Last Modified: Tue, 07 Apr 2026 01:25:49 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c5c15e10eaaac316ae60d4fac40ff1017f02b2b875b407bf682c77298d93a7`  
		Last Modified: Tue, 07 Apr 2026 01:25:49 GMT  
		Size: 153.5 KB (153536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b4ed74f4e6520e66630e36cdb82c8f7ca27efc5933b5349505c1585057e90d`  
		Last Modified: Tue, 07 Apr 2026 01:25:49 GMT  
		Size: 2.3 MB (2262094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3e3951f2c6832a2e7b51f69b34a00904ca49fa4c6f41d57326d88e67efee443`  
		Last Modified: Tue, 07 Apr 2026 01:25:49 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca5d4a8d60cff74d81f68e759a28cf6eb088ee9cdf6a9c4addee256ae2077f7`  
		Last Modified: Tue, 07 Apr 2026 01:25:50 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41` - unknown; unknown

```console
$ docker pull memcached@sha256:bbdcd7b1ee43fd986fc607ae612d760d1e019609ab9fbd3a0ecd4cc1f6633039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c8c88f72b4b8583399ce3dae76299eaccfe1e0817a4fbe7b2b69455600a6176`

```dockerfile
```

-	Layers:
	-	`sha256:1303514cbeaa570f5d824c226ba9dd6a62444501edb3f9993e3924bdbed20795`  
		Last Modified: Tue, 07 Apr 2026 01:25:49 GMT  
		Size: 2.0 MB (2008642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2aec570ce5326329f95567738d5d7f18b7d670eb63d25dcc3f4d8daa7ff1d7a`  
		Last Modified: Tue, 07 Apr 2026 01:25:49 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41` - linux; 386

```console
$ docker pull memcached@sha256:14a8e0dca582269247d9148e01b5245b21dec2272071ca4f0de57bfe5da798ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33665093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20735a6c9bab36926f3fdc6fced1b8175cfe3f105a1bab23554f8456daea2896`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:16:16 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 07 Apr 2026 01:16:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:19:11 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 07 Apr 2026 01:19:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 07 Apr 2026 01:19:11 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 07 Apr 2026 01:19:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 07 Apr 2026 01:19:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:19:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:19:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:19:11 GMT
USER memcache
# Tue, 07 Apr 2026 01:19:11 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 07 Apr 2026 01:19:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3c3d391a832256e6eca1fcef63254ce2b8cf2d25bc53ac0b56d9de64a11a7f30`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 31.3 MB (31291252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2980a28d02ccf82ab767a9e89afc9e4c15e85753a882a8a2263a2c0691a1004c`  
		Last Modified: Tue, 07 Apr 2026 01:19:17 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28192b8169c943bc464428731249fa5ca713d3be14de53eda8e012b20cabeb2c`  
		Last Modified: Tue, 07 Apr 2026 01:19:17 GMT  
		Size: 147.6 KB (147564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29865350ef2f7a2af74486f1fb3649b504a46931ac3e09e8a07592896b665b2`  
		Last Modified: Tue, 07 Apr 2026 01:19:18 GMT  
		Size: 2.2 MB (2224764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d14265a50518850c61aebad318e069eef28a5e9b25658ec7de3279062fdfa0`  
		Last Modified: Tue, 07 Apr 2026 01:19:18 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ce4f1d852aaa9c090f21a5e62d9c34e913461645b4111373022564ec41227d`  
		Last Modified: Tue, 07 Apr 2026 01:19:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41` - unknown; unknown

```console
$ docker pull memcached@sha256:0d86c338928dbeda1a6e986a64858fb0aed68a0f6c21e11882ec5ed8447078c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:075a856de16e6ed042abc19a38a81d43d11ecd7a857943cc72e8b6ddd7313cdc`

```dockerfile
```

-	Layers:
	-	`sha256:e5945497f00077342a9e73ad0d2cbc87810b1953e63c42228d117969dbfec8ee`  
		Last Modified: Tue, 07 Apr 2026 01:19:18 GMT  
		Size: 2.0 MB (2005483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46aed5ae982da715bb47a610f0f68cbf4b5326ce9401e5b9d9270b4aaeee19a1`  
		Last Modified: Tue, 07 Apr 2026 01:19:18 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41` - linux; ppc64le

```console
$ docker pull memcached@sha256:92ac8b2eb8a499448552281cc533c85175af918bb0596c8dc74fd5b36a75bd9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36159274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b82cf6a623a63a6ae0c8138a0541bee731e8bd82763d58be64d6699c425fe2f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:35:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 07 Apr 2026 01:35:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:38:51 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 07 Apr 2026 01:38:51 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 07 Apr 2026 01:38:51 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 07 Apr 2026 01:38:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 07 Apr 2026 01:38:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:38:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:38:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:38:52 GMT
USER memcache
# Tue, 07 Apr 2026 01:38:52 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 07 Apr 2026 01:38:52 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e3428d4efac15fe7728b465c9c3bc5d71a07ad502becbd70250a2c560e32b53`  
		Last Modified: Tue, 07 Apr 2026 00:12:50 GMT  
		Size: 33.6 MB (33593016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7eee776338abb1e966582aa93d7c23fd9fcd920abfbbdd3cea4bce8cf338f2e`  
		Last Modified: Tue, 07 Apr 2026 01:39:10 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19eab5a207ad27e6d36357fcd01d34c3642fe0ed80f2f88a793cca9f476f30f7`  
		Last Modified: Tue, 07 Apr 2026 01:39:10 GMT  
		Size: 170.4 KB (170414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3625df055c4a6c1ff4e05c28e38811218be01d19aa2acc0795fc57b5de83d1be`  
		Last Modified: Tue, 07 Apr 2026 01:39:10 GMT  
		Size: 2.4 MB (2394331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd4414756055219a9ca9c5147693091d8b0eb78130291d723e0cb2c9ce300a9`  
		Last Modified: Tue, 07 Apr 2026 01:39:10 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5635c499788fcf6fe44b99aac274f62a1c7a5da6cc7b5aa86372cb6073bb209b`  
		Last Modified: Tue, 07 Apr 2026 01:39:11 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41` - unknown; unknown

```console
$ docker pull memcached@sha256:2c06d5accf94e67fd3485443b1c72edccb0acad4470fe42460bc84e82ae9e65f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcd4dbec1613b0c5fc1bbb19ba085247f554ca63690b28c52441c0b058dde46e`

```dockerfile
```

-	Layers:
	-	`sha256:c3f3c4328760b53a1cc92c96577452cafa2c7320c7ed12f724fec785c444f5ed`  
		Last Modified: Tue, 07 Apr 2026 01:39:10 GMT  
		Size: 2.0 MB (2011927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bc399d77df625da1dc8870003a0130dbe6e49e04edbd00017af3b4b6189acc2`  
		Last Modified: Tue, 07 Apr 2026 01:39:10 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41` - linux; riscv64

```console
$ docker pull memcached@sha256:343fd1c6e9e7f911bda94d07d87041db133ac3b59520418cf1583edfdc3ce77f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30618876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf8181bc4bb9dd1d641b682d8c26ed16fc76cbe854cee7b23e7f6ba281fb8047`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 04:59:33 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 07 Apr 2026 05:00:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 05:13:37 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 07 Apr 2026 05:13:37 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 07 Apr 2026 05:13:37 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 07 Apr 2026 05:13:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 07 Apr 2026 05:13:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 05:13:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 05:13:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 05:13:38 GMT
USER memcache
# Tue, 07 Apr 2026 05:13:38 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 07 Apr 2026 05:13:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:51128e253868f85aa5e3b9e86448414d946e8a6b685e02db1030aaa2b11e81d4`  
		Last Modified: Tue, 07 Apr 2026 01:55:37 GMT  
		Size: 28.3 MB (28275778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172bc18e8051f399e255dee35e79f9e5fa9aa64562d2a8516dd4182f4d4520f2`  
		Last Modified: Tue, 07 Apr 2026 05:14:23 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3677dcf4246be900eca90abef0e04b5b1e429066cc6b3a57604bd40e0c452b`  
		Last Modified: Tue, 07 Apr 2026 05:14:23 GMT  
		Size: 133.1 KB (133140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03668775341afe9414f4c7e2652b23d3086383a5816cb62b8fb69364eff41155`  
		Last Modified: Tue, 07 Apr 2026 05:14:24 GMT  
		Size: 2.2 MB (2208446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf395524f6f820cc7011bc1a2fcc5eba29e77275e6e044e4354d2614eea65f5`  
		Last Modified: Tue, 07 Apr 2026 05:14:23 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9f8103185e19fe4e971346e1109fa338f4d760dbb9e45dff1e3f928b8072dca`  
		Last Modified: Tue, 07 Apr 2026 05:14:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41` - unknown; unknown

```console
$ docker pull memcached@sha256:b63ba37aad81705484c23176eb4f65464146117c69f7e8ff18a7768f27ace4ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a87be3b1386b7e3afd6748a7748bebffdafd2e21f6de7ad9f393c6719938cbc`

```dockerfile
```

-	Layers:
	-	`sha256:e7592dbf997c4d12b7436af51984acabb26f49a58b3ee14c6bc50f79a06a1845`  
		Last Modified: Tue, 07 Apr 2026 05:14:24 GMT  
		Size: 2.0 MB (2002290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f494bfe8ab328d634b3363d6b47b1bcc8e76f8982a3ffbb690421ebbcf84be6f`  
		Last Modified: Tue, 07 Apr 2026 05:14:23 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41` - linux; s390x

```console
$ docker pull memcached@sha256:59e3f9c04b50a8743ccabeca5a84541d363991bd60c566bcbcff5ab0a1ade514
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32276001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e64324407ea5f5792674919ee94e90c11c6811d91a80f580cc94408724f09f98`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:23:36 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 07 Apr 2026 01:23:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:27:33 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 07 Apr 2026 01:27:33 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 07 Apr 2026 01:27:33 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 07 Apr 2026 01:27:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 07 Apr 2026 01:27:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:27:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:27:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:27:34 GMT
USER memcache
# Tue, 07 Apr 2026 01:27:34 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 07 Apr 2026 01:27:34 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:82e48a38ec87473a03164a244b5d8dfc2b55ef7a891305e41ee39d937de3c4a4`  
		Last Modified: Tue, 07 Apr 2026 00:13:47 GMT  
		Size: 29.8 MB (29835418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea198846c92f684bb855bad5d89ae842effe4af57b25418506f1776bc0aecc1d`  
		Last Modified: Tue, 07 Apr 2026 01:27:59 GMT  
		Size: 1.1 KB (1115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63dbd168e3da58f5483989937676b90f414dcc112658e545873c8eabd1d451a`  
		Last Modified: Tue, 07 Apr 2026 01:27:59 GMT  
		Size: 140.6 KB (140591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4b420453294ae853b5eb6817eedaf54a487727358ea0a41c0a6d91fbcf58a6`  
		Last Modified: Tue, 07 Apr 2026 01:27:59 GMT  
		Size: 2.3 MB (2298473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da8e2eac18f15307576ba0dc01cd984583807f983a57441622c7a5a41f0442ba`  
		Last Modified: Tue, 07 Apr 2026 01:27:59 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b5b25d6119e86ee9944ee5a8a604ae736fdeba1ff080bd84b774cbc11445b3e`  
		Last Modified: Tue, 07 Apr 2026 01:28:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41` - unknown; unknown

```console
$ docker pull memcached@sha256:bd8097d65b8d6412d3ba3894adaef6aece7c4a57b12bac8838da6055b6e209fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b51a26520e00e9fcc204efc072451c2142451aef3b94f7e60d60532ae15662c`

```dockerfile
```

-	Layers:
	-	`sha256:a733a1255fb11524d515ae4a1ed12313958c1dd2d74cfb266144dc3c4fa044fc`  
		Last Modified: Tue, 07 Apr 2026 01:27:59 GMT  
		Size: 2.0 MB (2009763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8de5419a2a0f8a330a78a810bf9d25dbc33c70e95754f11bc392ffadf0372651`  
		Last Modified: Tue, 07 Apr 2026 01:27:59 GMT  
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
$ docker pull memcached@sha256:db739c92f80323018f33e3ddd392c7bb62c015280c7319f7e5dc207677ea3467
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
$ docker pull memcached@sha256:b788f2a69f7e53a4668d9e3a453544adace1d9f2515c87d16028be02b926b905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32194148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:957ebc2af9489fa034d85ce154bc33379c455514085cc54f8086e40af0b43dc1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:23:38 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 07 Apr 2026 01:23:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:26:29 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 07 Apr 2026 01:26:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 07 Apr 2026 01:26:29 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 07 Apr 2026 01:26:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 07 Apr 2026 01:26:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:26:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:26:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:26:29 GMT
USER memcache
# Tue, 07 Apr 2026 01:26:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 07 Apr 2026 01:26:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc6c716c6ddb3b32bea971a53985a917085b4cf120fff8d63d40df089226dc37`  
		Last Modified: Tue, 07 Apr 2026 01:26:35 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae9f08fb341368e75befbb98e1bb0ed398ec27d146ed1b86f063e558ec36994`  
		Last Modified: Tue, 07 Apr 2026 01:26:35 GMT  
		Size: 136.7 KB (136734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3715ece0607f0ad72fed1bab4785d71fb1f4a53248c7f0d0d728554d8a7e1d43`  
		Last Modified: Tue, 07 Apr 2026 01:26:35 GMT  
		Size: 2.3 MB (2280263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2587bd93e3d7081e72165f649bd56146508ef2a1d5bcecc34fc4a3c9e977c8cc`  
		Last Modified: Tue, 07 Apr 2026 01:26:35 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599d0131f8440d49de823ebacd72ff2b085e5b87424cb008b0fb9684815e96b1`  
		Last Modified: Tue, 07 Apr 2026 01:26:36 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:e52108fe5333bd921fcda699fa5e0a9a1f856476f94aa131ce3fca1bdc9c3333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8019a8ee5dc1bbcc7869825c68e49ab3cc98e0c26343fff78495facc0ed7166b`

```dockerfile
```

-	Layers:
	-	`sha256:3ee85043155b825da3cb759588dfd4ae9c5fb420241223c8eb0ea098db0d4352`  
		Last Modified: Tue, 07 Apr 2026 01:26:36 GMT  
		Size: 2.0 MB (2008326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63715707b27c7dcf51c74925a3a18c525a66f2a166fc8e44d63972b0c435d1eb`  
		Last Modified: Tue, 07 Apr 2026 01:26:35 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-trixie` - linux; arm variant v5

```console
$ docker pull memcached@sha256:df004aea9a02d7d4ee3ddc5465873404f20e8fa25c15e06d7b89d01d6cc1e356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30300952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea196d440f1b33851c03e3b418146249e09eb85317650c01e40dee92aa1966f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:36:58 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 07 Apr 2026 01:37:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:40:22 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 07 Apr 2026 01:40:22 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 07 Apr 2026 01:40:22 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 07 Apr 2026 01:40:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 07 Apr 2026 01:40:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:40:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:40:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:40:22 GMT
USER memcache
# Tue, 07 Apr 2026 01:40:22 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 07 Apr 2026 01:40:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3a32056c13d69abfd2a107f36cfc2049bdb6b52dbb76427fb9c1f688273f6bce`  
		Last Modified: Tue, 07 Apr 2026 00:11:10 GMT  
		Size: 27.9 MB (27943808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28da11ded538198c9b718c34fa43b8c4def75a2f31b50ed3a8bda92c1030d2f5`  
		Last Modified: Tue, 07 Apr 2026 01:40:28 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0cec49185fb79e2c1fd6b70122aa01ed8d60551bf8210a8c1266bc57db7262b`  
		Last Modified: Tue, 07 Apr 2026 01:40:28 GMT  
		Size: 144.2 KB (144201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:005ba68552dfbe267043ef794ab62753f9b67961868dc0a9948a3d153a6ab565`  
		Last Modified: Tue, 07 Apr 2026 01:40:28 GMT  
		Size: 2.2 MB (2211430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6514869f5fe8bb29cf6cd1481ed37590bf107b175195e617525696fe78550b`  
		Last Modified: Tue, 07 Apr 2026 01:40:28 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff4d287d37148bcd3c24209d83e46e78903ea757dce43fd6afc57731e84f401`  
		Last Modified: Tue, 07 Apr 2026 01:40:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:f240f6fbe003c002d394d498174c33dcc7af139322e3c52e5e090e7b49465c18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483b0a17344b9495480290bd9db97e169606d4a2ba8364d8018cb7464afc40a3`

```dockerfile
```

-	Layers:
	-	`sha256:2be307cba0a326ce27f955114acf18cc984e34bd185e2aad06e8d42126d6e019`  
		Last Modified: Tue, 07 Apr 2026 01:40:28 GMT  
		Size: 2.0 MB (2011329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1477528adcd0b2dbf9ee526a5e432557bcad4fedf5230183e7ba89f4132d2f36`  
		Last Modified: Tue, 07 Apr 2026 01:40:28 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-trixie` - linux; arm variant v7

```console
$ docker pull memcached@sha256:63893617a36fd6b52c4b87c082bae12bc14274921e436270f91bdced09696da8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28511650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb221d7cbc04c1704a1e11a7f3ec5fcec8e3409a06dadd58ea9e9e04b5e65fc7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:17:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 07 Apr 2026 01:17:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:20:21 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 07 Apr 2026 01:20:21 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 07 Apr 2026 01:20:21 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 07 Apr 2026 01:20:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 07 Apr 2026 01:20:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:20:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:20:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:20:21 GMT
USER memcache
# Tue, 07 Apr 2026 01:20:21 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 07 Apr 2026 01:20:21 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4c6d27739d1db2f26843c4e427219b60cd29d0d75a2f4c9eae2e732971275433`  
		Last Modified: Tue, 07 Apr 2026 01:00:39 GMT  
		Size: 26.2 MB (26209653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d53472c0d88747c450fe9d3a3ba402bff41134da0962fbc59dfddfc56bb7b2c`  
		Last Modified: Tue, 07 Apr 2026 01:20:27 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3911c933984424fe429e8a15f9ab53ec77e667a0217b071fa3d01a921dd25913`  
		Last Modified: Tue, 07 Apr 2026 01:20:27 GMT  
		Size: 135.4 KB (135405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df499710205ab866d69d874fc6de40178e60769f933a3d145604f2b641e48d1c`  
		Last Modified: Tue, 07 Apr 2026 01:20:27 GMT  
		Size: 2.2 MB (2165079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34502d029fbb87d2f994316b9034a00c81dc08a82c42bdac8f81991edd08d2dc`  
		Last Modified: Tue, 07 Apr 2026 01:20:27 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ffb0b865cbcbdeeb08432af5c96699db4b4d69822435141b3e0c6f4d63db69`  
		Last Modified: Tue, 07 Apr 2026 01:20:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:1736638210fa09980ce5ebd09ce778cb8bc99fde47be5e8919be7738a3343c97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a00642889a4ff9ad670d05a820454947cf9fe1dfd985a101e7ebaec77fd4e8d`

```dockerfile
```

-	Layers:
	-	`sha256:161d47d2d576cd7c620e85b92f138e51552979275c48f2972219108ac38ceeae`  
		Last Modified: Tue, 07 Apr 2026 01:20:27 GMT  
		Size: 2.0 MB (2009786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b60515cacf7c0e607b9ed02815936fe4979bb4980c85442fd2390bb5cad32ef9`  
		Last Modified: Tue, 07 Apr 2026 01:20:27 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-trixie` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:d998cfcd5bd550af6b2f9b9049095513de8f20594cc24c1bd7cad8c4ee6833d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32555698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee38d7a837c09c980e5060dea464fd640effc7729440b92dfd9bce0f3d0938fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:22:41 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 07 Apr 2026 01:22:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:25:43 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 07 Apr 2026 01:25:43 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 07 Apr 2026 01:25:43 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 07 Apr 2026 01:25:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 07 Apr 2026 01:25:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:25:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:25:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:25:43 GMT
USER memcache
# Tue, 07 Apr 2026 01:25:43 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 07 Apr 2026 01:25:43 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2b769d44c974357a7852d0b379e4db204456d0c805bc9c156302ce5d18e70a`  
		Last Modified: Tue, 07 Apr 2026 01:25:49 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c5c15e10eaaac316ae60d4fac40ff1017f02b2b875b407bf682c77298d93a7`  
		Last Modified: Tue, 07 Apr 2026 01:25:49 GMT  
		Size: 153.5 KB (153536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b4ed74f4e6520e66630e36cdb82c8f7ca27efc5933b5349505c1585057e90d`  
		Last Modified: Tue, 07 Apr 2026 01:25:49 GMT  
		Size: 2.3 MB (2262094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3e3951f2c6832a2e7b51f69b34a00904ca49fa4c6f41d57326d88e67efee443`  
		Last Modified: Tue, 07 Apr 2026 01:25:49 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca5d4a8d60cff74d81f68e759a28cf6eb088ee9cdf6a9c4addee256ae2077f7`  
		Last Modified: Tue, 07 Apr 2026 01:25:50 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:bbdcd7b1ee43fd986fc607ae612d760d1e019609ab9fbd3a0ecd4cc1f6633039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c8c88f72b4b8583399ce3dae76299eaccfe1e0817a4fbe7b2b69455600a6176`

```dockerfile
```

-	Layers:
	-	`sha256:1303514cbeaa570f5d824c226ba9dd6a62444501edb3f9993e3924bdbed20795`  
		Last Modified: Tue, 07 Apr 2026 01:25:49 GMT  
		Size: 2.0 MB (2008642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2aec570ce5326329f95567738d5d7f18b7d670eb63d25dcc3f4d8daa7ff1d7a`  
		Last Modified: Tue, 07 Apr 2026 01:25:49 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-trixie` - linux; 386

```console
$ docker pull memcached@sha256:14a8e0dca582269247d9148e01b5245b21dec2272071ca4f0de57bfe5da798ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33665093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20735a6c9bab36926f3fdc6fced1b8175cfe3f105a1bab23554f8456daea2896`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:16:16 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 07 Apr 2026 01:16:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:19:11 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 07 Apr 2026 01:19:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 07 Apr 2026 01:19:11 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 07 Apr 2026 01:19:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 07 Apr 2026 01:19:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:19:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:19:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:19:11 GMT
USER memcache
# Tue, 07 Apr 2026 01:19:11 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 07 Apr 2026 01:19:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3c3d391a832256e6eca1fcef63254ce2b8cf2d25bc53ac0b56d9de64a11a7f30`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 31.3 MB (31291252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2980a28d02ccf82ab767a9e89afc9e4c15e85753a882a8a2263a2c0691a1004c`  
		Last Modified: Tue, 07 Apr 2026 01:19:17 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28192b8169c943bc464428731249fa5ca713d3be14de53eda8e012b20cabeb2c`  
		Last Modified: Tue, 07 Apr 2026 01:19:17 GMT  
		Size: 147.6 KB (147564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29865350ef2f7a2af74486f1fb3649b504a46931ac3e09e8a07592896b665b2`  
		Last Modified: Tue, 07 Apr 2026 01:19:18 GMT  
		Size: 2.2 MB (2224764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d14265a50518850c61aebad318e069eef28a5e9b25658ec7de3279062fdfa0`  
		Last Modified: Tue, 07 Apr 2026 01:19:18 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ce4f1d852aaa9c090f21a5e62d9c34e913461645b4111373022564ec41227d`  
		Last Modified: Tue, 07 Apr 2026 01:19:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:0d86c338928dbeda1a6e986a64858fb0aed68a0f6c21e11882ec5ed8447078c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:075a856de16e6ed042abc19a38a81d43d11ecd7a857943cc72e8b6ddd7313cdc`

```dockerfile
```

-	Layers:
	-	`sha256:e5945497f00077342a9e73ad0d2cbc87810b1953e63c42228d117969dbfec8ee`  
		Last Modified: Tue, 07 Apr 2026 01:19:18 GMT  
		Size: 2.0 MB (2005483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46aed5ae982da715bb47a610f0f68cbf4b5326ce9401e5b9d9270b4aaeee19a1`  
		Last Modified: Tue, 07 Apr 2026 01:19:18 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-trixie` - linux; ppc64le

```console
$ docker pull memcached@sha256:92ac8b2eb8a499448552281cc533c85175af918bb0596c8dc74fd5b36a75bd9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36159274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b82cf6a623a63a6ae0c8138a0541bee731e8bd82763d58be64d6699c425fe2f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:35:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 07 Apr 2026 01:35:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:38:51 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 07 Apr 2026 01:38:51 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 07 Apr 2026 01:38:51 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 07 Apr 2026 01:38:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 07 Apr 2026 01:38:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:38:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:38:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:38:52 GMT
USER memcache
# Tue, 07 Apr 2026 01:38:52 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 07 Apr 2026 01:38:52 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e3428d4efac15fe7728b465c9c3bc5d71a07ad502becbd70250a2c560e32b53`  
		Last Modified: Tue, 07 Apr 2026 00:12:50 GMT  
		Size: 33.6 MB (33593016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7eee776338abb1e966582aa93d7c23fd9fcd920abfbbdd3cea4bce8cf338f2e`  
		Last Modified: Tue, 07 Apr 2026 01:39:10 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19eab5a207ad27e6d36357fcd01d34c3642fe0ed80f2f88a793cca9f476f30f7`  
		Last Modified: Tue, 07 Apr 2026 01:39:10 GMT  
		Size: 170.4 KB (170414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3625df055c4a6c1ff4e05c28e38811218be01d19aa2acc0795fc57b5de83d1be`  
		Last Modified: Tue, 07 Apr 2026 01:39:10 GMT  
		Size: 2.4 MB (2394331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd4414756055219a9ca9c5147693091d8b0eb78130291d723e0cb2c9ce300a9`  
		Last Modified: Tue, 07 Apr 2026 01:39:10 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5635c499788fcf6fe44b99aac274f62a1c7a5da6cc7b5aa86372cb6073bb209b`  
		Last Modified: Tue, 07 Apr 2026 01:39:11 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:2c06d5accf94e67fd3485443b1c72edccb0acad4470fe42460bc84e82ae9e65f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcd4dbec1613b0c5fc1bbb19ba085247f554ca63690b28c52441c0b058dde46e`

```dockerfile
```

-	Layers:
	-	`sha256:c3f3c4328760b53a1cc92c96577452cafa2c7320c7ed12f724fec785c444f5ed`  
		Last Modified: Tue, 07 Apr 2026 01:39:10 GMT  
		Size: 2.0 MB (2011927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bc399d77df625da1dc8870003a0130dbe6e49e04edbd00017af3b4b6189acc2`  
		Last Modified: Tue, 07 Apr 2026 01:39:10 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-trixie` - linux; riscv64

```console
$ docker pull memcached@sha256:343fd1c6e9e7f911bda94d07d87041db133ac3b59520418cf1583edfdc3ce77f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30618876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf8181bc4bb9dd1d641b682d8c26ed16fc76cbe854cee7b23e7f6ba281fb8047`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 04:59:33 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 07 Apr 2026 05:00:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 05:13:37 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 07 Apr 2026 05:13:37 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 07 Apr 2026 05:13:37 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 07 Apr 2026 05:13:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 07 Apr 2026 05:13:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 05:13:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 05:13:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 05:13:38 GMT
USER memcache
# Tue, 07 Apr 2026 05:13:38 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 07 Apr 2026 05:13:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:51128e253868f85aa5e3b9e86448414d946e8a6b685e02db1030aaa2b11e81d4`  
		Last Modified: Tue, 07 Apr 2026 01:55:37 GMT  
		Size: 28.3 MB (28275778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172bc18e8051f399e255dee35e79f9e5fa9aa64562d2a8516dd4182f4d4520f2`  
		Last Modified: Tue, 07 Apr 2026 05:14:23 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3677dcf4246be900eca90abef0e04b5b1e429066cc6b3a57604bd40e0c452b`  
		Last Modified: Tue, 07 Apr 2026 05:14:23 GMT  
		Size: 133.1 KB (133140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03668775341afe9414f4c7e2652b23d3086383a5816cb62b8fb69364eff41155`  
		Last Modified: Tue, 07 Apr 2026 05:14:24 GMT  
		Size: 2.2 MB (2208446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf395524f6f820cc7011bc1a2fcc5eba29e77275e6e044e4354d2614eea65f5`  
		Last Modified: Tue, 07 Apr 2026 05:14:23 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9f8103185e19fe4e971346e1109fa338f4d760dbb9e45dff1e3f928b8072dca`  
		Last Modified: Tue, 07 Apr 2026 05:14:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:b63ba37aad81705484c23176eb4f65464146117c69f7e8ff18a7768f27ace4ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a87be3b1386b7e3afd6748a7748bebffdafd2e21f6de7ad9f393c6719938cbc`

```dockerfile
```

-	Layers:
	-	`sha256:e7592dbf997c4d12b7436af51984acabb26f49a58b3ee14c6bc50f79a06a1845`  
		Last Modified: Tue, 07 Apr 2026 05:14:24 GMT  
		Size: 2.0 MB (2002290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f494bfe8ab328d634b3363d6b47b1bcc8e76f8982a3ffbb690421ebbcf84be6f`  
		Last Modified: Tue, 07 Apr 2026 05:14:23 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.41-trixie` - linux; s390x

```console
$ docker pull memcached@sha256:59e3f9c04b50a8743ccabeca5a84541d363991bd60c566bcbcff5ab0a1ade514
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32276001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e64324407ea5f5792674919ee94e90c11c6811d91a80f580cc94408724f09f98`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:23:36 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 07 Apr 2026 01:23:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:27:33 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 07 Apr 2026 01:27:33 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 07 Apr 2026 01:27:33 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 07 Apr 2026 01:27:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 07 Apr 2026 01:27:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:27:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:27:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:27:34 GMT
USER memcache
# Tue, 07 Apr 2026 01:27:34 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 07 Apr 2026 01:27:34 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:82e48a38ec87473a03164a244b5d8dfc2b55ef7a891305e41ee39d937de3c4a4`  
		Last Modified: Tue, 07 Apr 2026 00:13:47 GMT  
		Size: 29.8 MB (29835418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea198846c92f684bb855bad5d89ae842effe4af57b25418506f1776bc0aecc1d`  
		Last Modified: Tue, 07 Apr 2026 01:27:59 GMT  
		Size: 1.1 KB (1115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63dbd168e3da58f5483989937676b90f414dcc112658e545873c8eabd1d451a`  
		Last Modified: Tue, 07 Apr 2026 01:27:59 GMT  
		Size: 140.6 KB (140591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4b420453294ae853b5eb6817eedaf54a487727358ea0a41c0a6d91fbcf58a6`  
		Last Modified: Tue, 07 Apr 2026 01:27:59 GMT  
		Size: 2.3 MB (2298473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da8e2eac18f15307576ba0dc01cd984583807f983a57441622c7a5a41f0442ba`  
		Last Modified: Tue, 07 Apr 2026 01:27:59 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b5b25d6119e86ee9944ee5a8a604ae736fdeba1ff080bd84b774cbc11445b3e`  
		Last Modified: Tue, 07 Apr 2026 01:28:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.41-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:bd8097d65b8d6412d3ba3894adaef6aece7c4a57b12bac8838da6055b6e209fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b51a26520e00e9fcc204efc072451c2142451aef3b94f7e60d60532ae15662c`

```dockerfile
```

-	Layers:
	-	`sha256:a733a1255fb11524d515ae4a1ed12313958c1dd2d74cfb266144dc3c4fa044fc`  
		Last Modified: Tue, 07 Apr 2026 01:27:59 GMT  
		Size: 2.0 MB (2009763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8de5419a2a0f8a330a78a810bf9d25dbc33c70e95754f11bc392ffadf0372651`  
		Last Modified: Tue, 07 Apr 2026 01:27:59 GMT  
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
$ docker pull memcached@sha256:db739c92f80323018f33e3ddd392c7bb62c015280c7319f7e5dc207677ea3467
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
$ docker pull memcached@sha256:b788f2a69f7e53a4668d9e3a453544adace1d9f2515c87d16028be02b926b905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32194148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:957ebc2af9489fa034d85ce154bc33379c455514085cc54f8086e40af0b43dc1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:23:38 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 07 Apr 2026 01:23:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:26:29 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 07 Apr 2026 01:26:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 07 Apr 2026 01:26:29 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 07 Apr 2026 01:26:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 07 Apr 2026 01:26:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:26:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:26:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:26:29 GMT
USER memcache
# Tue, 07 Apr 2026 01:26:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 07 Apr 2026 01:26:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc6c716c6ddb3b32bea971a53985a917085b4cf120fff8d63d40df089226dc37`  
		Last Modified: Tue, 07 Apr 2026 01:26:35 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae9f08fb341368e75befbb98e1bb0ed398ec27d146ed1b86f063e558ec36994`  
		Last Modified: Tue, 07 Apr 2026 01:26:35 GMT  
		Size: 136.7 KB (136734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3715ece0607f0ad72fed1bab4785d71fb1f4a53248c7f0d0d728554d8a7e1d43`  
		Last Modified: Tue, 07 Apr 2026 01:26:35 GMT  
		Size: 2.3 MB (2280263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2587bd93e3d7081e72165f649bd56146508ef2a1d5bcecc34fc4a3c9e977c8cc`  
		Last Modified: Tue, 07 Apr 2026 01:26:35 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599d0131f8440d49de823ebacd72ff2b085e5b87424cb008b0fb9684815e96b1`  
		Last Modified: Tue, 07 Apr 2026 01:26:36 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:e52108fe5333bd921fcda699fa5e0a9a1f856476f94aa131ce3fca1bdc9c3333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8019a8ee5dc1bbcc7869825c68e49ab3cc98e0c26343fff78495facc0ed7166b`

```dockerfile
```

-	Layers:
	-	`sha256:3ee85043155b825da3cb759588dfd4ae9c5fb420241223c8eb0ea098db0d4352`  
		Last Modified: Tue, 07 Apr 2026 01:26:36 GMT  
		Size: 2.0 MB (2008326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63715707b27c7dcf51c74925a3a18c525a66f2a166fc8e44d63972b0c435d1eb`  
		Last Modified: Tue, 07 Apr 2026 01:26:35 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm variant v5

```console
$ docker pull memcached@sha256:df004aea9a02d7d4ee3ddc5465873404f20e8fa25c15e06d7b89d01d6cc1e356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30300952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea196d440f1b33851c03e3b418146249e09eb85317650c01e40dee92aa1966f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:36:58 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 07 Apr 2026 01:37:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:40:22 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 07 Apr 2026 01:40:22 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 07 Apr 2026 01:40:22 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 07 Apr 2026 01:40:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 07 Apr 2026 01:40:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:40:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:40:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:40:22 GMT
USER memcache
# Tue, 07 Apr 2026 01:40:22 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 07 Apr 2026 01:40:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3a32056c13d69abfd2a107f36cfc2049bdb6b52dbb76427fb9c1f688273f6bce`  
		Last Modified: Tue, 07 Apr 2026 00:11:10 GMT  
		Size: 27.9 MB (27943808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28da11ded538198c9b718c34fa43b8c4def75a2f31b50ed3a8bda92c1030d2f5`  
		Last Modified: Tue, 07 Apr 2026 01:40:28 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0cec49185fb79e2c1fd6b70122aa01ed8d60551bf8210a8c1266bc57db7262b`  
		Last Modified: Tue, 07 Apr 2026 01:40:28 GMT  
		Size: 144.2 KB (144201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:005ba68552dfbe267043ef794ab62753f9b67961868dc0a9948a3d153a6ab565`  
		Last Modified: Tue, 07 Apr 2026 01:40:28 GMT  
		Size: 2.2 MB (2211430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6514869f5fe8bb29cf6cd1481ed37590bf107b175195e617525696fe78550b`  
		Last Modified: Tue, 07 Apr 2026 01:40:28 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff4d287d37148bcd3c24209d83e46e78903ea757dce43fd6afc57731e84f401`  
		Last Modified: Tue, 07 Apr 2026 01:40:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:f240f6fbe003c002d394d498174c33dcc7af139322e3c52e5e090e7b49465c18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483b0a17344b9495480290bd9db97e169606d4a2ba8364d8018cb7464afc40a3`

```dockerfile
```

-	Layers:
	-	`sha256:2be307cba0a326ce27f955114acf18cc984e34bd185e2aad06e8d42126d6e019`  
		Last Modified: Tue, 07 Apr 2026 01:40:28 GMT  
		Size: 2.0 MB (2011329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1477528adcd0b2dbf9ee526a5e432557bcad4fedf5230183e7ba89f4132d2f36`  
		Last Modified: Tue, 07 Apr 2026 01:40:28 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm variant v7

```console
$ docker pull memcached@sha256:63893617a36fd6b52c4b87c082bae12bc14274921e436270f91bdced09696da8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28511650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb221d7cbc04c1704a1e11a7f3ec5fcec8e3409a06dadd58ea9e9e04b5e65fc7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:17:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 07 Apr 2026 01:17:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:20:21 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 07 Apr 2026 01:20:21 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 07 Apr 2026 01:20:21 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 07 Apr 2026 01:20:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 07 Apr 2026 01:20:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:20:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:20:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:20:21 GMT
USER memcache
# Tue, 07 Apr 2026 01:20:21 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 07 Apr 2026 01:20:21 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4c6d27739d1db2f26843c4e427219b60cd29d0d75a2f4c9eae2e732971275433`  
		Last Modified: Tue, 07 Apr 2026 01:00:39 GMT  
		Size: 26.2 MB (26209653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d53472c0d88747c450fe9d3a3ba402bff41134da0962fbc59dfddfc56bb7b2c`  
		Last Modified: Tue, 07 Apr 2026 01:20:27 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3911c933984424fe429e8a15f9ab53ec77e667a0217b071fa3d01a921dd25913`  
		Last Modified: Tue, 07 Apr 2026 01:20:27 GMT  
		Size: 135.4 KB (135405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df499710205ab866d69d874fc6de40178e60769f933a3d145604f2b641e48d1c`  
		Last Modified: Tue, 07 Apr 2026 01:20:27 GMT  
		Size: 2.2 MB (2165079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34502d029fbb87d2f994316b9034a00c81dc08a82c42bdac8f81991edd08d2dc`  
		Last Modified: Tue, 07 Apr 2026 01:20:27 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ffb0b865cbcbdeeb08432af5c96699db4b4d69822435141b3e0c6f4d63db69`  
		Last Modified: Tue, 07 Apr 2026 01:20:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:1736638210fa09980ce5ebd09ce778cb8bc99fde47be5e8919be7738a3343c97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a00642889a4ff9ad670d05a820454947cf9fe1dfd985a101e7ebaec77fd4e8d`

```dockerfile
```

-	Layers:
	-	`sha256:161d47d2d576cd7c620e85b92f138e51552979275c48f2972219108ac38ceeae`  
		Last Modified: Tue, 07 Apr 2026 01:20:27 GMT  
		Size: 2.0 MB (2009786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b60515cacf7c0e607b9ed02815936fe4979bb4980c85442fd2390bb5cad32ef9`  
		Last Modified: Tue, 07 Apr 2026 01:20:27 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:d998cfcd5bd550af6b2f9b9049095513de8f20594cc24c1bd7cad8c4ee6833d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32555698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee38d7a837c09c980e5060dea464fd640effc7729440b92dfd9bce0f3d0938fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:22:41 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 07 Apr 2026 01:22:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:25:43 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 07 Apr 2026 01:25:43 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 07 Apr 2026 01:25:43 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 07 Apr 2026 01:25:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 07 Apr 2026 01:25:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:25:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:25:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:25:43 GMT
USER memcache
# Tue, 07 Apr 2026 01:25:43 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 07 Apr 2026 01:25:43 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2b769d44c974357a7852d0b379e4db204456d0c805bc9c156302ce5d18e70a`  
		Last Modified: Tue, 07 Apr 2026 01:25:49 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c5c15e10eaaac316ae60d4fac40ff1017f02b2b875b407bf682c77298d93a7`  
		Last Modified: Tue, 07 Apr 2026 01:25:49 GMT  
		Size: 153.5 KB (153536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b4ed74f4e6520e66630e36cdb82c8f7ca27efc5933b5349505c1585057e90d`  
		Last Modified: Tue, 07 Apr 2026 01:25:49 GMT  
		Size: 2.3 MB (2262094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3e3951f2c6832a2e7b51f69b34a00904ca49fa4c6f41d57326d88e67efee443`  
		Last Modified: Tue, 07 Apr 2026 01:25:49 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca5d4a8d60cff74d81f68e759a28cf6eb088ee9cdf6a9c4addee256ae2077f7`  
		Last Modified: Tue, 07 Apr 2026 01:25:50 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:bbdcd7b1ee43fd986fc607ae612d760d1e019609ab9fbd3a0ecd4cc1f6633039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c8c88f72b4b8583399ce3dae76299eaccfe1e0817a4fbe7b2b69455600a6176`

```dockerfile
```

-	Layers:
	-	`sha256:1303514cbeaa570f5d824c226ba9dd6a62444501edb3f9993e3924bdbed20795`  
		Last Modified: Tue, 07 Apr 2026 01:25:49 GMT  
		Size: 2.0 MB (2008642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2aec570ce5326329f95567738d5d7f18b7d670eb63d25dcc3f4d8daa7ff1d7a`  
		Last Modified: Tue, 07 Apr 2026 01:25:49 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; 386

```console
$ docker pull memcached@sha256:14a8e0dca582269247d9148e01b5245b21dec2272071ca4f0de57bfe5da798ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33665093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20735a6c9bab36926f3fdc6fced1b8175cfe3f105a1bab23554f8456daea2896`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:16:16 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 07 Apr 2026 01:16:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:19:11 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 07 Apr 2026 01:19:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 07 Apr 2026 01:19:11 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 07 Apr 2026 01:19:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 07 Apr 2026 01:19:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:19:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:19:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:19:11 GMT
USER memcache
# Tue, 07 Apr 2026 01:19:11 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 07 Apr 2026 01:19:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3c3d391a832256e6eca1fcef63254ce2b8cf2d25bc53ac0b56d9de64a11a7f30`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 31.3 MB (31291252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2980a28d02ccf82ab767a9e89afc9e4c15e85753a882a8a2263a2c0691a1004c`  
		Last Modified: Tue, 07 Apr 2026 01:19:17 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28192b8169c943bc464428731249fa5ca713d3be14de53eda8e012b20cabeb2c`  
		Last Modified: Tue, 07 Apr 2026 01:19:17 GMT  
		Size: 147.6 KB (147564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29865350ef2f7a2af74486f1fb3649b504a46931ac3e09e8a07592896b665b2`  
		Last Modified: Tue, 07 Apr 2026 01:19:18 GMT  
		Size: 2.2 MB (2224764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d14265a50518850c61aebad318e069eef28a5e9b25658ec7de3279062fdfa0`  
		Last Modified: Tue, 07 Apr 2026 01:19:18 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ce4f1d852aaa9c090f21a5e62d9c34e913461645b4111373022564ec41227d`  
		Last Modified: Tue, 07 Apr 2026 01:19:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:0d86c338928dbeda1a6e986a64858fb0aed68a0f6c21e11882ec5ed8447078c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:075a856de16e6ed042abc19a38a81d43d11ecd7a857943cc72e8b6ddd7313cdc`

```dockerfile
```

-	Layers:
	-	`sha256:e5945497f00077342a9e73ad0d2cbc87810b1953e63c42228d117969dbfec8ee`  
		Last Modified: Tue, 07 Apr 2026 01:19:18 GMT  
		Size: 2.0 MB (2005483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46aed5ae982da715bb47a610f0f68cbf4b5326ce9401e5b9d9270b4aaeee19a1`  
		Last Modified: Tue, 07 Apr 2026 01:19:18 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; ppc64le

```console
$ docker pull memcached@sha256:92ac8b2eb8a499448552281cc533c85175af918bb0596c8dc74fd5b36a75bd9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36159274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b82cf6a623a63a6ae0c8138a0541bee731e8bd82763d58be64d6699c425fe2f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:35:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 07 Apr 2026 01:35:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:38:51 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 07 Apr 2026 01:38:51 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 07 Apr 2026 01:38:51 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 07 Apr 2026 01:38:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 07 Apr 2026 01:38:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:38:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:38:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:38:52 GMT
USER memcache
# Tue, 07 Apr 2026 01:38:52 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 07 Apr 2026 01:38:52 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e3428d4efac15fe7728b465c9c3bc5d71a07ad502becbd70250a2c560e32b53`  
		Last Modified: Tue, 07 Apr 2026 00:12:50 GMT  
		Size: 33.6 MB (33593016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7eee776338abb1e966582aa93d7c23fd9fcd920abfbbdd3cea4bce8cf338f2e`  
		Last Modified: Tue, 07 Apr 2026 01:39:10 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19eab5a207ad27e6d36357fcd01d34c3642fe0ed80f2f88a793cca9f476f30f7`  
		Last Modified: Tue, 07 Apr 2026 01:39:10 GMT  
		Size: 170.4 KB (170414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3625df055c4a6c1ff4e05c28e38811218be01d19aa2acc0795fc57b5de83d1be`  
		Last Modified: Tue, 07 Apr 2026 01:39:10 GMT  
		Size: 2.4 MB (2394331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd4414756055219a9ca9c5147693091d8b0eb78130291d723e0cb2c9ce300a9`  
		Last Modified: Tue, 07 Apr 2026 01:39:10 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5635c499788fcf6fe44b99aac274f62a1c7a5da6cc7b5aa86372cb6073bb209b`  
		Last Modified: Tue, 07 Apr 2026 01:39:11 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:2c06d5accf94e67fd3485443b1c72edccb0acad4470fe42460bc84e82ae9e65f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcd4dbec1613b0c5fc1bbb19ba085247f554ca63690b28c52441c0b058dde46e`

```dockerfile
```

-	Layers:
	-	`sha256:c3f3c4328760b53a1cc92c96577452cafa2c7320c7ed12f724fec785c444f5ed`  
		Last Modified: Tue, 07 Apr 2026 01:39:10 GMT  
		Size: 2.0 MB (2011927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bc399d77df625da1dc8870003a0130dbe6e49e04edbd00017af3b4b6189acc2`  
		Last Modified: Tue, 07 Apr 2026 01:39:10 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; riscv64

```console
$ docker pull memcached@sha256:343fd1c6e9e7f911bda94d07d87041db133ac3b59520418cf1583edfdc3ce77f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30618876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf8181bc4bb9dd1d641b682d8c26ed16fc76cbe854cee7b23e7f6ba281fb8047`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 04:59:33 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 07 Apr 2026 05:00:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 05:13:37 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 07 Apr 2026 05:13:37 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 07 Apr 2026 05:13:37 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 07 Apr 2026 05:13:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 07 Apr 2026 05:13:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 05:13:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 05:13:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 05:13:38 GMT
USER memcache
# Tue, 07 Apr 2026 05:13:38 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 07 Apr 2026 05:13:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:51128e253868f85aa5e3b9e86448414d946e8a6b685e02db1030aaa2b11e81d4`  
		Last Modified: Tue, 07 Apr 2026 01:55:37 GMT  
		Size: 28.3 MB (28275778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172bc18e8051f399e255dee35e79f9e5fa9aa64562d2a8516dd4182f4d4520f2`  
		Last Modified: Tue, 07 Apr 2026 05:14:23 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3677dcf4246be900eca90abef0e04b5b1e429066cc6b3a57604bd40e0c452b`  
		Last Modified: Tue, 07 Apr 2026 05:14:23 GMT  
		Size: 133.1 KB (133140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03668775341afe9414f4c7e2652b23d3086383a5816cb62b8fb69364eff41155`  
		Last Modified: Tue, 07 Apr 2026 05:14:24 GMT  
		Size: 2.2 MB (2208446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf395524f6f820cc7011bc1a2fcc5eba29e77275e6e044e4354d2614eea65f5`  
		Last Modified: Tue, 07 Apr 2026 05:14:23 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9f8103185e19fe4e971346e1109fa338f4d760dbb9e45dff1e3f928b8072dca`  
		Last Modified: Tue, 07 Apr 2026 05:14:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:b63ba37aad81705484c23176eb4f65464146117c69f7e8ff18a7768f27ace4ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a87be3b1386b7e3afd6748a7748bebffdafd2e21f6de7ad9f393c6719938cbc`

```dockerfile
```

-	Layers:
	-	`sha256:e7592dbf997c4d12b7436af51984acabb26f49a58b3ee14c6bc50f79a06a1845`  
		Last Modified: Tue, 07 Apr 2026 05:14:24 GMT  
		Size: 2.0 MB (2002290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f494bfe8ab328d634b3363d6b47b1bcc8e76f8982a3ffbb690421ebbcf84be6f`  
		Last Modified: Tue, 07 Apr 2026 05:14:23 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; s390x

```console
$ docker pull memcached@sha256:59e3f9c04b50a8743ccabeca5a84541d363991bd60c566bcbcff5ab0a1ade514
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32276001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e64324407ea5f5792674919ee94e90c11c6811d91a80f580cc94408724f09f98`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:23:36 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 07 Apr 2026 01:23:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:27:33 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 07 Apr 2026 01:27:33 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 07 Apr 2026 01:27:33 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 07 Apr 2026 01:27:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 07 Apr 2026 01:27:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:27:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:27:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:27:34 GMT
USER memcache
# Tue, 07 Apr 2026 01:27:34 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 07 Apr 2026 01:27:34 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:82e48a38ec87473a03164a244b5d8dfc2b55ef7a891305e41ee39d937de3c4a4`  
		Last Modified: Tue, 07 Apr 2026 00:13:47 GMT  
		Size: 29.8 MB (29835418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea198846c92f684bb855bad5d89ae842effe4af57b25418506f1776bc0aecc1d`  
		Last Modified: Tue, 07 Apr 2026 01:27:59 GMT  
		Size: 1.1 KB (1115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63dbd168e3da58f5483989937676b90f414dcc112658e545873c8eabd1d451a`  
		Last Modified: Tue, 07 Apr 2026 01:27:59 GMT  
		Size: 140.6 KB (140591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4b420453294ae853b5eb6817eedaf54a487727358ea0a41c0a6d91fbcf58a6`  
		Last Modified: Tue, 07 Apr 2026 01:27:59 GMT  
		Size: 2.3 MB (2298473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da8e2eac18f15307576ba0dc01cd984583807f983a57441622c7a5a41f0442ba`  
		Last Modified: Tue, 07 Apr 2026 01:27:59 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b5b25d6119e86ee9944ee5a8a604ae736fdeba1ff080bd84b774cbc11445b3e`  
		Last Modified: Tue, 07 Apr 2026 01:28:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:bd8097d65b8d6412d3ba3894adaef6aece7c4a57b12bac8838da6055b6e209fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b51a26520e00e9fcc204efc072451c2142451aef3b94f7e60d60532ae15662c`

```dockerfile
```

-	Layers:
	-	`sha256:a733a1255fb11524d515ae4a1ed12313958c1dd2d74cfb266144dc3c4fa044fc`  
		Last Modified: Tue, 07 Apr 2026 01:27:59 GMT  
		Size: 2.0 MB (2009763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8de5419a2a0f8a330a78a810bf9d25dbc33c70e95754f11bc392ffadf0372651`  
		Last Modified: Tue, 07 Apr 2026 01:27:59 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:trixie`

```console
$ docker pull memcached@sha256:db739c92f80323018f33e3ddd392c7bb62c015280c7319f7e5dc207677ea3467
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
$ docker pull memcached@sha256:b788f2a69f7e53a4668d9e3a453544adace1d9f2515c87d16028be02b926b905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32194148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:957ebc2af9489fa034d85ce154bc33379c455514085cc54f8086e40af0b43dc1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:23:38 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 07 Apr 2026 01:23:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:26:29 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 07 Apr 2026 01:26:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 07 Apr 2026 01:26:29 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 07 Apr 2026 01:26:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 07 Apr 2026 01:26:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:26:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:26:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:26:29 GMT
USER memcache
# Tue, 07 Apr 2026 01:26:29 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 07 Apr 2026 01:26:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc6c716c6ddb3b32bea971a53985a917085b4cf120fff8d63d40df089226dc37`  
		Last Modified: Tue, 07 Apr 2026 01:26:35 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae9f08fb341368e75befbb98e1bb0ed398ec27d146ed1b86f063e558ec36994`  
		Last Modified: Tue, 07 Apr 2026 01:26:35 GMT  
		Size: 136.7 KB (136734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3715ece0607f0ad72fed1bab4785d71fb1f4a53248c7f0d0d728554d8a7e1d43`  
		Last Modified: Tue, 07 Apr 2026 01:26:35 GMT  
		Size: 2.3 MB (2280263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2587bd93e3d7081e72165f649bd56146508ef2a1d5bcecc34fc4a3c9e977c8cc`  
		Last Modified: Tue, 07 Apr 2026 01:26:35 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599d0131f8440d49de823ebacd72ff2b085e5b87424cb008b0fb9684815e96b1`  
		Last Modified: Tue, 07 Apr 2026 01:26:36 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:e52108fe5333bd921fcda699fa5e0a9a1f856476f94aa131ce3fca1bdc9c3333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8019a8ee5dc1bbcc7869825c68e49ab3cc98e0c26343fff78495facc0ed7166b`

```dockerfile
```

-	Layers:
	-	`sha256:3ee85043155b825da3cb759588dfd4ae9c5fb420241223c8eb0ea098db0d4352`  
		Last Modified: Tue, 07 Apr 2026 01:26:36 GMT  
		Size: 2.0 MB (2008326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63715707b27c7dcf51c74925a3a18c525a66f2a166fc8e44d63972b0c435d1eb`  
		Last Modified: Tue, 07 Apr 2026 01:26:35 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; arm variant v5

```console
$ docker pull memcached@sha256:df004aea9a02d7d4ee3ddc5465873404f20e8fa25c15e06d7b89d01d6cc1e356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30300952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea196d440f1b33851c03e3b418146249e09eb85317650c01e40dee92aa1966f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:36:58 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 07 Apr 2026 01:37:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:40:22 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 07 Apr 2026 01:40:22 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 07 Apr 2026 01:40:22 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 07 Apr 2026 01:40:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 07 Apr 2026 01:40:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:40:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:40:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:40:22 GMT
USER memcache
# Tue, 07 Apr 2026 01:40:22 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 07 Apr 2026 01:40:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3a32056c13d69abfd2a107f36cfc2049bdb6b52dbb76427fb9c1f688273f6bce`  
		Last Modified: Tue, 07 Apr 2026 00:11:10 GMT  
		Size: 27.9 MB (27943808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28da11ded538198c9b718c34fa43b8c4def75a2f31b50ed3a8bda92c1030d2f5`  
		Last Modified: Tue, 07 Apr 2026 01:40:28 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0cec49185fb79e2c1fd6b70122aa01ed8d60551bf8210a8c1266bc57db7262b`  
		Last Modified: Tue, 07 Apr 2026 01:40:28 GMT  
		Size: 144.2 KB (144201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:005ba68552dfbe267043ef794ab62753f9b67961868dc0a9948a3d153a6ab565`  
		Last Modified: Tue, 07 Apr 2026 01:40:28 GMT  
		Size: 2.2 MB (2211430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6514869f5fe8bb29cf6cd1481ed37590bf107b175195e617525696fe78550b`  
		Last Modified: Tue, 07 Apr 2026 01:40:28 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff4d287d37148bcd3c24209d83e46e78903ea757dce43fd6afc57731e84f401`  
		Last Modified: Tue, 07 Apr 2026 01:40:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:f240f6fbe003c002d394d498174c33dcc7af139322e3c52e5e090e7b49465c18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483b0a17344b9495480290bd9db97e169606d4a2ba8364d8018cb7464afc40a3`

```dockerfile
```

-	Layers:
	-	`sha256:2be307cba0a326ce27f955114acf18cc984e34bd185e2aad06e8d42126d6e019`  
		Last Modified: Tue, 07 Apr 2026 01:40:28 GMT  
		Size: 2.0 MB (2011329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1477528adcd0b2dbf9ee526a5e432557bcad4fedf5230183e7ba89f4132d2f36`  
		Last Modified: Tue, 07 Apr 2026 01:40:28 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; arm variant v7

```console
$ docker pull memcached@sha256:63893617a36fd6b52c4b87c082bae12bc14274921e436270f91bdced09696da8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28511650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb221d7cbc04c1704a1e11a7f3ec5fcec8e3409a06dadd58ea9e9e04b5e65fc7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:17:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 07 Apr 2026 01:17:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:20:21 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 07 Apr 2026 01:20:21 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 07 Apr 2026 01:20:21 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 07 Apr 2026 01:20:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 07 Apr 2026 01:20:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:20:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:20:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:20:21 GMT
USER memcache
# Tue, 07 Apr 2026 01:20:21 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 07 Apr 2026 01:20:21 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4c6d27739d1db2f26843c4e427219b60cd29d0d75a2f4c9eae2e732971275433`  
		Last Modified: Tue, 07 Apr 2026 01:00:39 GMT  
		Size: 26.2 MB (26209653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d53472c0d88747c450fe9d3a3ba402bff41134da0962fbc59dfddfc56bb7b2c`  
		Last Modified: Tue, 07 Apr 2026 01:20:27 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3911c933984424fe429e8a15f9ab53ec77e667a0217b071fa3d01a921dd25913`  
		Last Modified: Tue, 07 Apr 2026 01:20:27 GMT  
		Size: 135.4 KB (135405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df499710205ab866d69d874fc6de40178e60769f933a3d145604f2b641e48d1c`  
		Last Modified: Tue, 07 Apr 2026 01:20:27 GMT  
		Size: 2.2 MB (2165079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34502d029fbb87d2f994316b9034a00c81dc08a82c42bdac8f81991edd08d2dc`  
		Last Modified: Tue, 07 Apr 2026 01:20:27 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ffb0b865cbcbdeeb08432af5c96699db4b4d69822435141b3e0c6f4d63db69`  
		Last Modified: Tue, 07 Apr 2026 01:20:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:1736638210fa09980ce5ebd09ce778cb8bc99fde47be5e8919be7738a3343c97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a00642889a4ff9ad670d05a820454947cf9fe1dfd985a101e7ebaec77fd4e8d`

```dockerfile
```

-	Layers:
	-	`sha256:161d47d2d576cd7c620e85b92f138e51552979275c48f2972219108ac38ceeae`  
		Last Modified: Tue, 07 Apr 2026 01:20:27 GMT  
		Size: 2.0 MB (2009786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b60515cacf7c0e607b9ed02815936fe4979bb4980c85442fd2390bb5cad32ef9`  
		Last Modified: Tue, 07 Apr 2026 01:20:27 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:d998cfcd5bd550af6b2f9b9049095513de8f20594cc24c1bd7cad8c4ee6833d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32555698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee38d7a837c09c980e5060dea464fd640effc7729440b92dfd9bce0f3d0938fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:22:41 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 07 Apr 2026 01:22:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:25:43 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 07 Apr 2026 01:25:43 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 07 Apr 2026 01:25:43 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 07 Apr 2026 01:25:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 07 Apr 2026 01:25:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:25:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:25:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:25:43 GMT
USER memcache
# Tue, 07 Apr 2026 01:25:43 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 07 Apr 2026 01:25:43 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2b769d44c974357a7852d0b379e4db204456d0c805bc9c156302ce5d18e70a`  
		Last Modified: Tue, 07 Apr 2026 01:25:49 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c5c15e10eaaac316ae60d4fac40ff1017f02b2b875b407bf682c77298d93a7`  
		Last Modified: Tue, 07 Apr 2026 01:25:49 GMT  
		Size: 153.5 KB (153536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b4ed74f4e6520e66630e36cdb82c8f7ca27efc5933b5349505c1585057e90d`  
		Last Modified: Tue, 07 Apr 2026 01:25:49 GMT  
		Size: 2.3 MB (2262094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3e3951f2c6832a2e7b51f69b34a00904ca49fa4c6f41d57326d88e67efee443`  
		Last Modified: Tue, 07 Apr 2026 01:25:49 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca5d4a8d60cff74d81f68e759a28cf6eb088ee9cdf6a9c4addee256ae2077f7`  
		Last Modified: Tue, 07 Apr 2026 01:25:50 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:bbdcd7b1ee43fd986fc607ae612d760d1e019609ab9fbd3a0ecd4cc1f6633039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c8c88f72b4b8583399ce3dae76299eaccfe1e0817a4fbe7b2b69455600a6176`

```dockerfile
```

-	Layers:
	-	`sha256:1303514cbeaa570f5d824c226ba9dd6a62444501edb3f9993e3924bdbed20795`  
		Last Modified: Tue, 07 Apr 2026 01:25:49 GMT  
		Size: 2.0 MB (2008642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2aec570ce5326329f95567738d5d7f18b7d670eb63d25dcc3f4d8daa7ff1d7a`  
		Last Modified: Tue, 07 Apr 2026 01:25:49 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; 386

```console
$ docker pull memcached@sha256:14a8e0dca582269247d9148e01b5245b21dec2272071ca4f0de57bfe5da798ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33665093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20735a6c9bab36926f3fdc6fced1b8175cfe3f105a1bab23554f8456daea2896`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:16:16 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 07 Apr 2026 01:16:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:19:11 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 07 Apr 2026 01:19:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 07 Apr 2026 01:19:11 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 07 Apr 2026 01:19:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 07 Apr 2026 01:19:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:19:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:19:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:19:11 GMT
USER memcache
# Tue, 07 Apr 2026 01:19:11 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 07 Apr 2026 01:19:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3c3d391a832256e6eca1fcef63254ce2b8cf2d25bc53ac0b56d9de64a11a7f30`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 31.3 MB (31291252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2980a28d02ccf82ab767a9e89afc9e4c15e85753a882a8a2263a2c0691a1004c`  
		Last Modified: Tue, 07 Apr 2026 01:19:17 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28192b8169c943bc464428731249fa5ca713d3be14de53eda8e012b20cabeb2c`  
		Last Modified: Tue, 07 Apr 2026 01:19:17 GMT  
		Size: 147.6 KB (147564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29865350ef2f7a2af74486f1fb3649b504a46931ac3e09e8a07592896b665b2`  
		Last Modified: Tue, 07 Apr 2026 01:19:18 GMT  
		Size: 2.2 MB (2224764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d14265a50518850c61aebad318e069eef28a5e9b25658ec7de3279062fdfa0`  
		Last Modified: Tue, 07 Apr 2026 01:19:18 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ce4f1d852aaa9c090f21a5e62d9c34e913461645b4111373022564ec41227d`  
		Last Modified: Tue, 07 Apr 2026 01:19:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:0d86c338928dbeda1a6e986a64858fb0aed68a0f6c21e11882ec5ed8447078c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:075a856de16e6ed042abc19a38a81d43d11ecd7a857943cc72e8b6ddd7313cdc`

```dockerfile
```

-	Layers:
	-	`sha256:e5945497f00077342a9e73ad0d2cbc87810b1953e63c42228d117969dbfec8ee`  
		Last Modified: Tue, 07 Apr 2026 01:19:18 GMT  
		Size: 2.0 MB (2005483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46aed5ae982da715bb47a610f0f68cbf4b5326ce9401e5b9d9270b4aaeee19a1`  
		Last Modified: Tue, 07 Apr 2026 01:19:18 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; ppc64le

```console
$ docker pull memcached@sha256:92ac8b2eb8a499448552281cc533c85175af918bb0596c8dc74fd5b36a75bd9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36159274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b82cf6a623a63a6ae0c8138a0541bee731e8bd82763d58be64d6699c425fe2f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:35:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 07 Apr 2026 01:35:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:38:51 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 07 Apr 2026 01:38:51 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 07 Apr 2026 01:38:51 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 07 Apr 2026 01:38:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 07 Apr 2026 01:38:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:38:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:38:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:38:52 GMT
USER memcache
# Tue, 07 Apr 2026 01:38:52 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 07 Apr 2026 01:38:52 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e3428d4efac15fe7728b465c9c3bc5d71a07ad502becbd70250a2c560e32b53`  
		Last Modified: Tue, 07 Apr 2026 00:12:50 GMT  
		Size: 33.6 MB (33593016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7eee776338abb1e966582aa93d7c23fd9fcd920abfbbdd3cea4bce8cf338f2e`  
		Last Modified: Tue, 07 Apr 2026 01:39:10 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19eab5a207ad27e6d36357fcd01d34c3642fe0ed80f2f88a793cca9f476f30f7`  
		Last Modified: Tue, 07 Apr 2026 01:39:10 GMT  
		Size: 170.4 KB (170414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3625df055c4a6c1ff4e05c28e38811218be01d19aa2acc0795fc57b5de83d1be`  
		Last Modified: Tue, 07 Apr 2026 01:39:10 GMT  
		Size: 2.4 MB (2394331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd4414756055219a9ca9c5147693091d8b0eb78130291d723e0cb2c9ce300a9`  
		Last Modified: Tue, 07 Apr 2026 01:39:10 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5635c499788fcf6fe44b99aac274f62a1c7a5da6cc7b5aa86372cb6073bb209b`  
		Last Modified: Tue, 07 Apr 2026 01:39:11 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:2c06d5accf94e67fd3485443b1c72edccb0acad4470fe42460bc84e82ae9e65f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcd4dbec1613b0c5fc1bbb19ba085247f554ca63690b28c52441c0b058dde46e`

```dockerfile
```

-	Layers:
	-	`sha256:c3f3c4328760b53a1cc92c96577452cafa2c7320c7ed12f724fec785c444f5ed`  
		Last Modified: Tue, 07 Apr 2026 01:39:10 GMT  
		Size: 2.0 MB (2011927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bc399d77df625da1dc8870003a0130dbe6e49e04edbd00017af3b4b6189acc2`  
		Last Modified: Tue, 07 Apr 2026 01:39:10 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; riscv64

```console
$ docker pull memcached@sha256:343fd1c6e9e7f911bda94d07d87041db133ac3b59520418cf1583edfdc3ce77f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30618876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf8181bc4bb9dd1d641b682d8c26ed16fc76cbe854cee7b23e7f6ba281fb8047`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 04:59:33 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 07 Apr 2026 05:00:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 05:13:37 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 07 Apr 2026 05:13:37 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 07 Apr 2026 05:13:37 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 07 Apr 2026 05:13:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 07 Apr 2026 05:13:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 05:13:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 05:13:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 05:13:38 GMT
USER memcache
# Tue, 07 Apr 2026 05:13:38 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 07 Apr 2026 05:13:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:51128e253868f85aa5e3b9e86448414d946e8a6b685e02db1030aaa2b11e81d4`  
		Last Modified: Tue, 07 Apr 2026 01:55:37 GMT  
		Size: 28.3 MB (28275778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172bc18e8051f399e255dee35e79f9e5fa9aa64562d2a8516dd4182f4d4520f2`  
		Last Modified: Tue, 07 Apr 2026 05:14:23 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3677dcf4246be900eca90abef0e04b5b1e429066cc6b3a57604bd40e0c452b`  
		Last Modified: Tue, 07 Apr 2026 05:14:23 GMT  
		Size: 133.1 KB (133140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03668775341afe9414f4c7e2652b23d3086383a5816cb62b8fb69364eff41155`  
		Last Modified: Tue, 07 Apr 2026 05:14:24 GMT  
		Size: 2.2 MB (2208446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf395524f6f820cc7011bc1a2fcc5eba29e77275e6e044e4354d2614eea65f5`  
		Last Modified: Tue, 07 Apr 2026 05:14:23 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9f8103185e19fe4e971346e1109fa338f4d760dbb9e45dff1e3f928b8072dca`  
		Last Modified: Tue, 07 Apr 2026 05:14:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:b63ba37aad81705484c23176eb4f65464146117c69f7e8ff18a7768f27ace4ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a87be3b1386b7e3afd6748a7748bebffdafd2e21f6de7ad9f393c6719938cbc`

```dockerfile
```

-	Layers:
	-	`sha256:e7592dbf997c4d12b7436af51984acabb26f49a58b3ee14c6bc50f79a06a1845`  
		Last Modified: Tue, 07 Apr 2026 05:14:24 GMT  
		Size: 2.0 MB (2002290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f494bfe8ab328d634b3363d6b47b1bcc8e76f8982a3ffbb690421ebbcf84be6f`  
		Last Modified: Tue, 07 Apr 2026 05:14:23 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; s390x

```console
$ docker pull memcached@sha256:59e3f9c04b50a8743ccabeca5a84541d363991bd60c566bcbcff5ab0a1ade514
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32276001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e64324407ea5f5792674919ee94e90c11c6811d91a80f580cc94408724f09f98`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:23:36 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Tue, 07 Apr 2026 01:23:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:27:33 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 07 Apr 2026 01:27:33 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 07 Apr 2026 01:27:33 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 07 Apr 2026 01:27:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 07 Apr 2026 01:27:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:27:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 07 Apr 2026 01:27:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:27:34 GMT
USER memcache
# Tue, 07 Apr 2026 01:27:34 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 07 Apr 2026 01:27:34 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:82e48a38ec87473a03164a244b5d8dfc2b55ef7a891305e41ee39d937de3c4a4`  
		Last Modified: Tue, 07 Apr 2026 00:13:47 GMT  
		Size: 29.8 MB (29835418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea198846c92f684bb855bad5d89ae842effe4af57b25418506f1776bc0aecc1d`  
		Last Modified: Tue, 07 Apr 2026 01:27:59 GMT  
		Size: 1.1 KB (1115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63dbd168e3da58f5483989937676b90f414dcc112658e545873c8eabd1d451a`  
		Last Modified: Tue, 07 Apr 2026 01:27:59 GMT  
		Size: 140.6 KB (140591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4b420453294ae853b5eb6817eedaf54a487727358ea0a41c0a6d91fbcf58a6`  
		Last Modified: Tue, 07 Apr 2026 01:27:59 GMT  
		Size: 2.3 MB (2298473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da8e2eac18f15307576ba0dc01cd984583807f983a57441622c7a5a41f0442ba`  
		Last Modified: Tue, 07 Apr 2026 01:27:59 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b5b25d6119e86ee9944ee5a8a604ae736fdeba1ff080bd84b774cbc11445b3e`  
		Last Modified: Tue, 07 Apr 2026 01:28:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:bd8097d65b8d6412d3ba3894adaef6aece7c4a57b12bac8838da6055b6e209fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b51a26520e00e9fcc204efc072451c2142451aef3b94f7e60d60532ae15662c`

```dockerfile
```

-	Layers:
	-	`sha256:a733a1255fb11524d515ae4a1ed12313958c1dd2d74cfb266144dc3c4fa044fc`  
		Last Modified: Tue, 07 Apr 2026 01:27:59 GMT  
		Size: 2.0 MB (2009763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8de5419a2a0f8a330a78a810bf9d25dbc33c70e95754f11bc392ffadf0372651`  
		Last Modified: Tue, 07 Apr 2026 01:27:59 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json
