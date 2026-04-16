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
