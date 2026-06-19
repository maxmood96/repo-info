<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `memcached`

-	[`memcached:1`](#memcached1)
-	[`memcached:1-alpine`](#memcached1-alpine)
-	[`memcached:1-alpine3.24`](#memcached1-alpine324)
-	[`memcached:1-trixie`](#memcached1-trixie)
-	[`memcached:1.6`](#memcached16)
-	[`memcached:1.6-alpine`](#memcached16-alpine)
-	[`memcached:1.6-alpine3.24`](#memcached16-alpine324)
-	[`memcached:1.6-trixie`](#memcached16-trixie)
-	[`memcached:1.6.42`](#memcached1642)
-	[`memcached:1.6.42-alpine`](#memcached1642-alpine)
-	[`memcached:1.6.42-alpine3.24`](#memcached1642-alpine324)
-	[`memcached:1.6.42-trixie`](#memcached1642-trixie)
-	[`memcached:alpine`](#memcachedalpine)
-	[`memcached:alpine3.24`](#memcachedalpine324)
-	[`memcached:latest`](#memcachedlatest)
-	[`memcached:trixie`](#memcachedtrixie)

## `memcached:1`

```console
$ docker pull memcached@sha256:85c0ab87f71b8b3ade708271177a8e5efca5e93c00287b6f25a2d74a27180bfa
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
$ docker pull memcached@sha256:09ac4118d89005e47ef3118221840c62f0fa909a2bee07ff571ae1ae59d9a79b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32204821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ad15119e1f73d99f3fbdc56187ea014f4fae2c8fcbe215c259f2fb2b387aefa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:23:00 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 11 Jun 2026 00:23:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:25:47 GMT
ENV MEMCACHED_VERSION=1.6.42
# Thu, 11 Jun 2026 00:25:47 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Thu, 11 Jun 2026 00:25:47 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Thu, 11 Jun 2026 00:25:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 11 Jun 2026 00:25:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:25:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 11 Jun 2026 00:25:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:25:47 GMT
USER memcache
# Thu, 11 Jun 2026 00:25:47 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 11 Jun 2026 00:25:47 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7883ff600bb4cc730c755ccb8be3f5a06371865abe00be70037283c04f4f3f5`  
		Last Modified: Thu, 11 Jun 2026 00:25:53 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d73a0d6b79b50aa2429aebc30b68c38fb0fb43a4a597ce0dd3936605fbb8912e`  
		Last Modified: Thu, 11 Jun 2026 00:25:53 GMT  
		Size: 136.7 KB (136685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5716730726452d6a54ff03d59c7dffbb7ed4f05836877734acf92f7a0512d6a9`  
		Last Modified: Thu, 11 Jun 2026 00:25:53 GMT  
		Size: 2.3 MB (2281206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f338318b7809e3c4be59b7eccaa1e5387cdbe8015c49eac3267097258c54ae89`  
		Last Modified: Thu, 11 Jun 2026 00:25:53 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ca13d7300d84ca43fcce2aa8304787015f83333e041c81c04796354eadce6b`  
		Last Modified: Thu, 11 Jun 2026 00:25:54 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:3d476e3ec28b0dda5046a3223b0e5a8c9ab8dec20bb294a8853da81d828c154d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e2358f67931681260618f406ea3e0032f17f7a82b2a7d36e5511e6413a7133f`

```dockerfile
```

-	Layers:
	-	`sha256:9cb94c17b8cb82e97f6ad217227fa08e25e0fdc9b96fd2fe418e0acc53911305`  
		Last Modified: Thu, 11 Jun 2026 00:25:53 GMT  
		Size: 2.0 MB (2008368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f8a18d24b8d75bd4b8d856878db21e4d4df7e3e553b9d72d0156bbe58c869d3`  
		Last Modified: Thu, 11 Jun 2026 00:25:53 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm variant v5

```console
$ docker pull memcached@sha256:f059b77d971253090e3862e28d374840935b5c06467230e9bea207fdb6ef3bf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30316631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c99754215fd2490daf10c8c1046bee3ab237e1e95bd4b46ef0610ca9d1c9badc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:19:47 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 11 Jun 2026 00:19:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:23:08 GMT
ENV MEMCACHED_VERSION=1.6.42
# Thu, 11 Jun 2026 00:23:08 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Thu, 11 Jun 2026 00:23:08 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Thu, 11 Jun 2026 00:23:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 11 Jun 2026 00:23:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:23:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 11 Jun 2026 00:23:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:23:08 GMT
USER memcache
# Thu, 11 Jun 2026 00:23:08 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 11 Jun 2026 00:23:08 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ed883f3fd95b7edef302d7ca9520eefdae280af081509bd7e9e5b5ff8f4cda7c`  
		Last Modified: Wed, 10 Jun 2026 23:41:17 GMT  
		Size: 28.0 MB (27959200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e92527947bdcc341ab63777422e7409751516a8bc5ffc61040d76b72e7d58c`  
		Last Modified: Thu, 11 Jun 2026 00:23:14 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c52c9bd0c151ce908cf5e8c55694b4a321a916d3053e9e4cd3b06837e55f325`  
		Last Modified: Thu, 11 Jun 2026 00:23:14 GMT  
		Size: 144.2 KB (144156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ec2615dd4e79e84378f7223c9d7c70a6cdfb8835717c19cadbab17a726210d`  
		Last Modified: Thu, 11 Jun 2026 00:23:14 GMT  
		Size: 2.2 MB (2211763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4249a738c6e8e951ca0bf1608e335442f8f50ff9fe57a524b1bdb472e59ed1`  
		Last Modified: Thu, 11 Jun 2026 00:23:14 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab171fa641968acda113ed8ec0cbff5159a4895efed9c4e08bb6e466a40fb5ce`  
		Last Modified: Thu, 11 Jun 2026 00:23:15 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:a7356b3e73eada1ea16535f45e9a297b7913adfb103e9df5d0a2ee333c58f443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c75fc3f8c74e188d3585642b303189b73ae78c14b089bd14f0d37da2b085f25`

```dockerfile
```

-	Layers:
	-	`sha256:5a953398782781fbd31e5d1fb67c1cdeb82c91397fb27ce32b9d756cc938a03a`  
		Last Modified: Thu, 11 Jun 2026 00:23:14 GMT  
		Size: 2.0 MB (2011371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aeae6ddb09b0b52fdf1e1db9b67dfa04fba888fbba5c54b1b7e30ecbd56dafde`  
		Last Modified: Thu, 11 Jun 2026 00:23:14 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm variant v7

```console
$ docker pull memcached@sha256:7b20950329f422c7b322057fe1f944f98589cf937e5e65118b6d4bb241436ffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28513288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5d65e3287f7256814db41a73f2978df2252f6ac399369fe1a7a3eb1c4ceb3e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:21:55 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 11 Jun 2026 00:21:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:25:06 GMT
ENV MEMCACHED_VERSION=1.6.42
# Thu, 11 Jun 2026 00:25:06 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Thu, 11 Jun 2026 00:25:06 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Thu, 11 Jun 2026 00:25:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 11 Jun 2026 00:25:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:25:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 11 Jun 2026 00:25:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:25:06 GMT
USER memcache
# Thu, 11 Jun 2026 00:25:06 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 11 Jun 2026 00:25:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4bd6ddea06d5009ee47ddb0f254a2569aff0230c005869ebd416b20295d945c0`  
		Last Modified: Wed, 10 Jun 2026 23:42:34 GMT  
		Size: 26.2 MB (26211004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bcac116a5bd6f8c4ba910742373294134be4443587cce918db3492895262e16`  
		Last Modified: Thu, 11 Jun 2026 00:25:12 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af6a74cecf5734c352e3c2ea5fb348246cfe77549b6cb2afe3116aaf39983ff8`  
		Last Modified: Thu, 11 Jun 2026 00:25:12 GMT  
		Size: 135.4 KB (135382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6189c46b05f5cdb39083034f258358c5472cc6824a25a7dc8a8f60ae58891116`  
		Last Modified: Thu, 11 Jun 2026 00:25:12 GMT  
		Size: 2.2 MB (2165385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfeedbf1b9c25a3c29e32962704f935689b2b60c4096315dbee3365a9cec4dc0`  
		Last Modified: Thu, 11 Jun 2026 00:25:12 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0309704e28c847b1dd0249a490a5774838b3d27bf059481108e0f1a300efd4ae`  
		Last Modified: Thu, 11 Jun 2026 00:25:13 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:84793c5cdc418c73cc53c1dcdf3ebaf9d1c2a7910ec63c85d179a691e05f1ddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0981cd8d43f93fb996bbc87f0659a7c3a7163d74a5c84503eb77588ed240010c`

```dockerfile
```

-	Layers:
	-	`sha256:39acaedd56024e59130ae654692bdff06d01b71719567ede3d9ece539679150e`  
		Last Modified: Thu, 11 Jun 2026 00:25:13 GMT  
		Size: 2.0 MB (2009828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ada0017eed4fa0f3db9a2e1669d0eb74e2908e65a483af6819df971d18d767a`  
		Last Modified: Thu, 11 Jun 2026 00:25:12 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:a36eca5b5840c718ca41526a871fd751dc96965f182778a7631a0c2896c3f44a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32566560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31c7500da651c7c5945a2db8b00248c02ad2947b4eccb66b464759cd6f4ea2c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:23:08 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 11 Jun 2026 00:23:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:26:08 GMT
ENV MEMCACHED_VERSION=1.6.42
# Thu, 11 Jun 2026 00:26:08 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Thu, 11 Jun 2026 00:26:08 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Thu, 11 Jun 2026 00:26:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 11 Jun 2026 00:26:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:26:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 11 Jun 2026 00:26:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:26:08 GMT
USER memcache
# Thu, 11 Jun 2026 00:26:08 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 11 Jun 2026 00:26:08 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb68ad832950ffa1d5fe24c7e7ee4e061b358d6bcb14dfdb1bb2dec4c557f7a2`  
		Last Modified: Thu, 11 Jun 2026 00:26:15 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f6f966199cad211cd492fc65c6c927fde3a05499bdd9a2112d65deb706cfbc6`  
		Last Modified: Thu, 11 Jun 2026 00:26:14 GMT  
		Size: 153.5 KB (153481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3314b48b94577865e96641c557d5048167254c141db1725db6a5b7a623b68f7b`  
		Last Modified: Thu, 11 Jun 2026 00:26:15 GMT  
		Size: 2.3 MB (2263038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e33e48bcfd48ec271ffa516b5c3b03458185abfb31596aca0b854e9c9367fb9`  
		Last Modified: Thu, 11 Jun 2026 00:26:15 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb41e83cd817b17ff4c2b62ce482681096f6783b2a32be0407cada277d4f293`  
		Last Modified: Thu, 11 Jun 2026 00:26:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:0253549da149222537eeb2e51a1b411b7662c20d8c8964e71967cf670ce9c992
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af9894c8fa8e920a07bf631bed91c9b67398338986159408229a8da050b21c3b`

```dockerfile
```

-	Layers:
	-	`sha256:a11c09037e68845f3c8c01efb996710c3b2d21ba868a98c3ba2582a28d0f1047`  
		Last Modified: Thu, 11 Jun 2026 00:26:15 GMT  
		Size: 2.0 MB (2008676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40468c38b6f60c4625c352d5bdc83ea61510da0efeb2542777603da191a5d2fa`  
		Last Modified: Thu, 11 Jun 2026 00:26:14 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; 386

```console
$ docker pull memcached@sha256:e134667b3198bc9f05962d9bb97cf359ab04c31cb8d11c75e2683de54cebd46e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33675616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cba4eb3d3e82545273aa5ff6f0e6f7bf2b1240176b9489d2315fcf290b9c49a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:18:22 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 11 Jun 2026 00:18:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:21:26 GMT
ENV MEMCACHED_VERSION=1.6.42
# Thu, 11 Jun 2026 00:21:26 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Thu, 11 Jun 2026 00:21:26 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Thu, 11 Jun 2026 00:21:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 11 Jun 2026 00:21:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:21:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 11 Jun 2026 00:21:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:21:26 GMT
USER memcache
# Thu, 11 Jun 2026 00:21:26 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 11 Jun 2026 00:21:26 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:720f951a68f4f9ab464e52b53cf88cfb86bc876b3f00956d000420777ab93c0c`  
		Last Modified: Wed, 10 Jun 2026 23:40:30 GMT  
		Size: 31.3 MB (31301194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2607fca8a1b7fbebf74214d1b33f4f0a54aed5fef2bed18ddc89836a7d00e04b`  
		Last Modified: Thu, 11 Jun 2026 00:21:31 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4620fc98d601bc463a1a505fb0ecf42cb42fa76088d5e80dee41474c74f39f1`  
		Last Modified: Thu, 11 Jun 2026 00:21:32 GMT  
		Size: 147.5 KB (147511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a4c97894b05376111399fa19e7429f36d493cb528c53cb81318a2920d5a954`  
		Last Modified: Thu, 11 Jun 2026 00:21:32 GMT  
		Size: 2.2 MB (2225398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f4a764af02d7ba61dd0909ddb429ba92c9a367243a225936fd625fda113340`  
		Last Modified: Thu, 11 Jun 2026 00:21:32 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52e82109e627ebc0d88a9f7c357b97f14b8ac06bdab5d0b6aa50c3b958a13a8`  
		Last Modified: Thu, 11 Jun 2026 00:21:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:6670b6485b54bcae32ddeda5c2d1764d0ee2066f036d0c17f2cc89734f0be8c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d0aef4dacfecea9e8dbc20498736f77e48bf5106eb60bcfa08c1e81a5c4f06c`

```dockerfile
```

-	Layers:
	-	`sha256:0ebdf5fe0d474785e4448d36043967631fb650ec7b52bd865126a7360978a2ea`  
		Last Modified: Thu, 11 Jun 2026 00:21:32 GMT  
		Size: 2.0 MB (2005525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f257ddeb15df7a03d8e7bb57e01531d894c998af32f33cb528199914bd8f6e1c`  
		Last Modified: Thu, 11 Jun 2026 00:21:32 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; ppc64le

```console
$ docker pull memcached@sha256:25e41a95392ee3c63e35711fec0648fbedc92c6be718456ad8fb89ab66f4e825
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36762178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a04e55188a4c60d5cd8eb00b50628fd87658d0d1814097b40417d71b18479e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 02:36:51 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 11 Jun 2026 02:36:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:59:49 GMT
ENV MEMCACHED_VERSION=1.6.42
# Thu, 11 Jun 2026 02:59:49 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Thu, 11 Jun 2026 02:59:49 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Thu, 11 Jun 2026 02:59:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 11 Jun 2026 02:59:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 02:59:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 11 Jun 2026 02:59:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 02:59:50 GMT
USER memcache
# Thu, 11 Jun 2026 02:59:50 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 11 Jun 2026 02:59:50 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9d6b2e320e2b74843186d830e8202c50ebfaeccf823d239e3e3e349a8a508d80`  
		Last Modified: Thu, 11 Jun 2026 00:24:42 GMT  
		Size: 33.6 MB (33606340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d389c79e93b7c7b3cc2a8226edeb6460d8101e245642213048c1a187d08a935d`  
		Last Modified: Thu, 11 Jun 2026 03:00:07 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7bb22e37f822a0e94fa24cd439d7666c214637b0d59c384dd19e12674c74a82`  
		Last Modified: Thu, 11 Jun 2026 03:00:07 GMT  
		Size: 170.4 KB (170363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82cbb5c5e79cdcec98bd562e1a62768994b805ff7d805b6b75b5bf0e349cff8`  
		Last Modified: Thu, 11 Jun 2026 03:00:06 GMT  
		Size: 3.0 MB (2983963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e60c6f3b8886967bbbabece38cfe74eccdfde98cdae42045a33c5b2b29fd6da`  
		Last Modified: Thu, 11 Jun 2026 03:00:08 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc87d370da3b9877481bf9620bda982328b4d722812ec3e77a7b4c50d016eb33`  
		Last Modified: Thu, 11 Jun 2026 03:00:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:0101df893b4af64daa7ee54d012d7b8682b6c1a9ad1d85700cf8ff269664b19e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b06e6f43b0b95c657fb0043338f12918e63fcac640df48783c49ac29092afb0b`

```dockerfile
```

-	Layers:
	-	`sha256:8ed9fcb43f9f08fb8702ae2709d918b6370866fb4697ddf04b93f42080b23d94`  
		Last Modified: Thu, 11 Jun 2026 03:00:08 GMT  
		Size: 2.0 MB (2011969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c6915dddb9ee13a9cd4156b07c521335c76c9687dcb3a08e66e147af9d99453`  
		Last Modified: Thu, 11 Jun 2026 03:00:06 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; riscv64

```console
$ docker pull memcached@sha256:918c03d1a36c36f13b67e3fbf100f93adad50fbbb452fecc3769db0b8cde487c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30626726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1c8f5f48c37fb2ef15e785c080f746aec65afab782672de8b6a63bd88942e41`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1781049600'
# Fri, 12 Jun 2026 00:28:54 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 12 Jun 2026 00:29:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jun 2026 00:42:57 GMT
ENV MEMCACHED_VERSION=1.6.42
# Fri, 12 Jun 2026 00:42:57 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Fri, 12 Jun 2026 00:42:57 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Fri, 12 Jun 2026 00:42:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 12 Jun 2026 00:42:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Jun 2026 00:42:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 12 Jun 2026 00:42:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2026 00:42:57 GMT
USER memcache
# Fri, 12 Jun 2026 00:42:57 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 12 Jun 2026 00:42:57 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0b510fe8545cab831b696965b5a825649c5c945581e912d31a08a0b30ff940c0`  
		Last Modified: Thu, 11 Jun 2026 03:01:06 GMT  
		Size: 28.3 MB (28282305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35e7a152e660b7a61f448299ac325c28198a870bc53d54cd2584d111c3cef30`  
		Last Modified: Fri, 12 Jun 2026 00:43:44 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d26b2af070be1166e165d4bd1eb073a685622ddb1edb5cf4382cb7825faa21a`  
		Last Modified: Fri, 12 Jun 2026 00:43:44 GMT  
		Size: 133.1 KB (133071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ac4d08e6c19ea726574dc4cd56f4d39216f427cdfd9d6e19c91b06583e6630`  
		Last Modified: Fri, 12 Jun 2026 00:43:44 GMT  
		Size: 2.2 MB (2209833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:039ac44117911671ad0fca8638fa93282ad5865273a55e1328d3180ac5c4f463`  
		Last Modified: Fri, 12 Jun 2026 00:43:44 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65787f51c4d435ccf6c4c9c11e27fe642bd5af3fdd4489e11005614f51c21c29`  
		Last Modified: Fri, 12 Jun 2026 00:43:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:5db8b7d0f9f634b02f9f4dfb45d2f0d3fb2ef1778c3e52058327cd5dec31ebce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0de6ff12136279a3005dae5ce29967a780efb19d8a50b71f33b8153d38859c49`

```dockerfile
```

-	Layers:
	-	`sha256:256f6cfcbc556a40776a58fddd91ccacf0870ab5955a42e7e3ea23601ff76633`  
		Last Modified: Fri, 12 Jun 2026 00:43:44 GMT  
		Size: 2.0 MB (2002332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdfa564b06be9c36a9d81da00994136c858ca65d81762277469168a418a9c9fa`  
		Last Modified: Fri, 12 Jun 2026 00:43:44 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; s390x

```console
$ docker pull memcached@sha256:75f4e343898a5a326a82f6560f0efdd5d11c5aea7a710327cdfd400ac3244341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32291904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd9e841717be4c79746136574299d1a6552f88fe8566606318efb07377ef20c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:19:32 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 11 Jun 2026 00:19:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:22:55 GMT
ENV MEMCACHED_VERSION=1.6.42
# Thu, 11 Jun 2026 00:22:55 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Thu, 11 Jun 2026 00:22:55 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Thu, 11 Jun 2026 00:22:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 11 Jun 2026 00:22:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:22:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 11 Jun 2026 00:22:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:22:55 GMT
USER memcache
# Thu, 11 Jun 2026 00:22:55 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 11 Jun 2026 00:22:55 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:760dcf74fdfe93300ce15b5b23adf9aa4af45b6ba9d69925863198f64881a537`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 29.9 MB (29851354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159eeccf7c6aa583901267e3c00bf9c124c32be82a1074722d2be0b547fee632`  
		Last Modified: Thu, 11 Jun 2026 00:23:05 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d08bb26724ea31dfaf95eb6c1647b7686671b3869632300d6056a05c3532bd`  
		Last Modified: Thu, 11 Jun 2026 00:23:05 GMT  
		Size: 140.5 KB (140545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b341a8e7ca68a391e79c556246f3f0b81e4a5e747fed517e274d78f49faa30`  
		Last Modified: Thu, 11 Jun 2026 00:23:05 GMT  
		Size: 2.3 MB (2298492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff1b1dd9080cb995308882030f9579f4c5bf2af5b26b7270d6682de75f6e6d5`  
		Last Modified: Thu, 11 Jun 2026 00:23:05 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075343c77f8c8b9a1bb9fe079e853c0e4628b60f1fff7d8dce82d38c3a344bf8`  
		Last Modified: Thu, 11 Jun 2026 00:23:06 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:1f977b6725f519f48d75ffc92c711df863d7c0e4a1d1f0c5a5bc6605533f35e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1104b534613c8d2cc0544b9adf96821b4f7f623262ef6ddc425f13fa94427850`

```dockerfile
```

-	Layers:
	-	`sha256:66bb879abbe8f943d53561fcf4f4262e1b78fb31b6aa3fdac560ffdc45e3d4b5`  
		Last Modified: Thu, 11 Jun 2026 00:23:05 GMT  
		Size: 2.0 MB (2009805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e448bf5a0443ce0296756453f8bca10e0ec97ebc01576de74a28f60b78299f2b`  
		Last Modified: Thu, 11 Jun 2026 00:23:05 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine`

```console
$ docker pull memcached@sha256:7381333da6d6ae06e02d8dfc87ee6f2c7cd0a19f7ba048d5efc538d2100e2208
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
$ docker pull memcached@sha256:ce375dd48f976d33bf35beb966cc37f202fd840a90891e58b9e71171fc74174d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5921579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19d284e7a8445d8dc70e97c673a8a0175d18f39d5336ccbdfa8b240c0ef3ce4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:29 GMT
ADD alpine-minirootfs-3.24.1-x86_64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:15:18 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:15:18 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:17:54 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:17:54 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:17:54 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:17:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:17:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:17:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:17:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:17:54 GMT
USER memcache
# Tue, 16 Jun 2026 00:17:54 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:17:54 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:55afa1ecc21d2bb5e5045f32dafee56272ffd89860bac26f6c32123439af26a4`  
		Last Modified: Sun, 14 Jun 2026 06:44:06 GMT  
		Size: 3.8 MB (3846391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb73756dcbbebc424eab53d3adda4d9f64001e7a91272a7b2a834622c08b093`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f0d6a5291334f2b54ec652193cd4e17ee22455b2f3ff3bd9b66acff6436c7b`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 106.1 KB (106066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ac11a8307528096ac745e0ef681b64854bbd012ffdfbce85587153eec73563`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 2.0 MB (1967772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3626493aad85d70a212bc66e9d45db8aef43b4bc662259563f916398165f1e64`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cdcd3f20e3aa439838f5491e6f457a42bad6c80ed9b099313bf79b57a721ea8`  
		Last Modified: Tue, 16 Jun 2026 00:18:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:bb948800301f1cae8e18e317f2b9e85636c86c4a1924ee85e125da37cb1333e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c3e084937eb543038244e151b03b8d9a0dce0b4d5bf87c2d471fa397ed5702`

```dockerfile
```

-	Layers:
	-	`sha256:9d05a792212c92363a76bb6a8205a6e7f386113b3efc1b5d600f93d4e237c975`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 94.9 KB (94897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee0e7e70ef03205f55c68bc1b74ac7854183aee4e871112794975dc852761b19`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:4b144cdbc67c11035b3d0f0c812b590ee694977f2f6a32321e538237bd2f841c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5573158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e9bb70df1535a2f8ca960f733a4404cbde900a13156a1f4446c2fd110258e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:25 GMT
ADD alpine-minirootfs-3.24.1-armhf.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:25 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:14:43 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:14:44 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:17:47 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:17:47 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:17:47 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:17:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:17:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:17:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:17:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:17:47 GMT
USER memcache
# Tue, 16 Jun 2026 00:17:47 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:17:47 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3c4836a46d600cfe9a422adf7a80205cb534097e6213325e0176c51f6e5cc02e`  
		Last Modified: Sun, 14 Jun 2026 06:44:57 GMT  
		Size: 3.6 MB (3553450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e732a60042adf5cff5fe4fe0de83f937f6e5c8896500f7023e8bf68ed0670d65`  
		Last Modified: Tue, 16 Jun 2026 00:17:51 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad86d1fea29db061a5ae896a0a595b144edcdb4af59deac2b75b0fb8f5fa2d4c`  
		Last Modified: Tue, 16 Jun 2026 00:17:50 GMT  
		Size: 102.6 KB (102624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f26dd2445dbf4d5624417ca290f5ae2e5774fa7fec4f5655cd2377ee3147e4`  
		Last Modified: Tue, 16 Jun 2026 00:17:51 GMT  
		Size: 1.9 MB (1915730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080a186f0ca6beb06a5ce4a86fbc71f5b9995713fcc899c73f995f251ef7c987`  
		Last Modified: Tue, 16 Jun 2026 00:17:51 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c4d4f455f9a2b633cca28e3aa2190e4c42ca83ca6e3ea88ea4abe16944d238`  
		Last Modified: Tue, 16 Jun 2026 00:17:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:d6b7abf6ef34abf12ab2c7f84bd29ac2461eb3271d1c4070456ed9b94e4b41a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43a767571287c8ca227e321ee8d65f9da82e558098bedbb15888434dcc1ce9fa`

```dockerfile
```

-	Layers:
	-	`sha256:1794ccef4392c0db4ba36ad7fde22cdacbda40f4d56f0adbef802163c87e066c`  
		Last Modified: Tue, 16 Jun 2026 00:17:51 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:848c5e0ced69b802cca72c23bec05a4c6f23136212a4a1d5cc22b7c8f0154bf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:286f62a53a8947036e39f2b79567b31d38309fd84c7a39e43de8c5f9817a2f64`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:26 GMT
ADD alpine-minirootfs-3.24.1-armv7.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:26 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:17:59 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:17:59 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:20:56 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:20:56 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:20:56 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:20:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:20:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:20:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:20:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:20:56 GMT
USER memcache
# Tue, 16 Jun 2026 00:20:56 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:20:56 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bc03a9e5b4dd452551f246e199537fe7afc1765f53f510bc81d26df9845e4008`  
		Last Modified: Sun, 14 Jun 2026 06:45:22 GMT  
		Size: 3.3 MB (3260615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f0249bacfc8953b72899bf7b6c904c8750482fce4c93108f57b2c64228b279`  
		Last Modified: Tue, 16 Jun 2026 00:21:00 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95e1b321ffc31d01e766d5d1d054967d613940563406fc54ee981926b7f6049`  
		Last Modified: Tue, 16 Jun 2026 00:21:01 GMT  
		Size: 92.4 KB (92366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce112e60c1b15077277c233a7707831818dff0a15f1fc977ebebc93f817dad43`  
		Last Modified: Tue, 16 Jun 2026 00:21:01 GMT  
		Size: 1.9 MB (1875183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32fa6ed5b14fd6fcf96a7cde2996063f10b8efe802c386479288a232af826027`  
		Last Modified: Tue, 16 Jun 2026 00:21:01 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6648f8180a4eea1f5197f2fa2d356fbbf4e5f65345e189e720e227af64a5e31`  
		Last Modified: Tue, 16 Jun 2026 00:21:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:59387f31eff7cfb3166c5e6d4bad92e255705affcc15c84c4a06c86ecb1a9890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:174eb460b1df4523a4f71ba5a996f2285fa845fe8ef76d2df3ea8c4962c6b6ca`

```dockerfile
```

-	Layers:
	-	`sha256:4ff5e70775e819cab551295c56b58fdb0c44c105cdc4f72247e3968accd2ab2f`  
		Last Modified: Tue, 16 Jun 2026 00:21:00 GMT  
		Size: 94.3 KB (94315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00f10e1301c7e61396658f7e3ed330e400a9f304c6a0323de8ff644aba987474`  
		Last Modified: Tue, 16 Jun 2026 00:21:01 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:33261748facce282dbe4dbb4d9f875139680fce4cefc13cb9ad8e1ced23f9557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6250475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1614bb2865c8f849c2bc5bf77703a1ab711695c607a8bc6edb013a076ec16d6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:20 GMT
ADD alpine-minirootfs-3.24.1-aarch64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:20 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:13:18 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:13:18 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:16:06 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:16:06 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:16:06 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:16:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:16:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:16:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:16:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:16:06 GMT
USER memcache
# Tue, 16 Jun 2026 00:16:06 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:16:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5de55e5ef9c033997441461efe7ba23a986db059c0bb78b38f84ee0d72b99167`  
		Last Modified: Sun, 14 Jun 2026 06:44:31 GMT  
		Size: 4.2 MB (4183037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5faa19f06c4d5e26332739c7f08fd3dcd2c81817471c62029a6d99af6be8748`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377a35d28f00766e2679c788b95b0a67b9aa5a76c8ef701a2a9604e2a00c3b46`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 121.8 KB (121841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0b819e89558d70f1401ca58cbc19c58ae13e15be8184fd9b2733e022f318a4`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 1.9 MB (1944247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca539cef48ff8c3f723ab23506b6786c9ed26a9cac713601b71de2dc775d26a`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c4c456deed244daa6d7076f40a1cf0364d294059bb43e533677a89027843b15`  
		Last Modified: Tue, 16 Jun 2026 00:16:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:4d25960abc53b5ba1896b8f5ee04ba5ac1389900ab9b413eb62285af7281aedb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d1a4b7ad428a08c8a174d5ecd9763d530e849f54a2d9b90aef934e54b9477d4`

```dockerfile
```

-	Layers:
	-	`sha256:9c0a8e5e07390fae6abe9204450009671011c4d2d5aa5fe4afdd82324fdb49b9`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 94.4 KB (94351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ee01158358d01c082867cf46a5225cf101013e4d5b7eae18fc7853e277ff0f4`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 20.7 KB (20727 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; 386

```console
$ docker pull memcached@sha256:5436d0ef6e12f2f8e454384ff4a703132b3fe820c41a55336f520bb5d1622574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5702329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8946be3d97c7b9825159f58cbf832b131c75cb90b3fb46a40d5429b9ffe32bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:19 GMT
ADD alpine-minirootfs-3.24.1-x86.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:19 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:13:59 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:13:59 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:16:45 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:16:45 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:16:45 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:16:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:16:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:16:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:16:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:16:46 GMT
USER memcache
# Tue, 16 Jun 2026 00:16:46 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:16:46 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f86df9d778509895efbf9363d8fcb0cbe0b772de536c7218e4c4c947f0be879f`  
		Last Modified: Sun, 14 Jun 2026 06:45:46 GMT  
		Size: 3.7 MB (3670141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043137360442e605bc150f28f20e1fa2d23d90131370bc405ad7d35309594491`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900ce6eeaece12033b12f1c8641c33dcf62ff2525584411911368cfcd0b38224`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 110.7 KB (110729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e8cc1c8f6bc6391eb1a43a46f0b55ca7845f824fc0f2fc7ae7587a7715814e`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 1.9 MB (1920111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d94f6e4d3be92188fc182a3557fe43af5bc9f3e768a7f265977743a56eea527e`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f8a19f18dfff271426de7a17ab6780788fa4345d5fa0120e6d03720d552bd4`  
		Last Modified: Tue, 16 Jun 2026 00:16:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:00dc6a7f29b7f2f5ac46fc5678b80c43c7b1e46b4ca3c84c5597034180aeb644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6de04019c7775544db9adbb4c4558d0e7c842c279e5d70532b2ac0b988ac1345`

```dockerfile
```

-	Layers:
	-	`sha256:80895f8f5e9c9b015e419096426322f4c86c33d55ca8860ee046b61d52782847`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 94.9 KB (94852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c69be8c1f82a066b46cc389712508e85c1dcd77e649c922dba46ace64b343ae`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:c7857941a51b85b136781035703afcc8854a2d70fa2091208a51f8bb7e71f934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5998515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b02b2222212c64e444ac1a2227b19f0cfb1282c8a8ced386c1b79ae48c641b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:15 GMT
ADD alpine-minirootfs-3.24.1-ppc64le.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:15 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:15:37 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:15:38 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:18:22 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:18:22 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:18:22 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:18:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:18:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:18:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:18:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:18:22 GMT
USER memcache
# Tue, 16 Jun 2026 00:18:22 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:18:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3ebcdcd395ccee658b9200e4b27d7699e5d6ed9f6c1858dea12781aac519ff59`  
		Last Modified: Sun, 14 Jun 2026 06:46:36 GMT  
		Size: 3.8 MB (3813400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b108e2058722fb0fb5a9310e8ebe82ab4b9c021228a94b3125ba49d318e9667`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb8160ed736eda8513164d5d703082fb0c9af9e037472ab70a02579caa3eb99`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 126.3 KB (126252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5cb88dd03ce07ecf1613c2aff220fb392763d8f22edc900c4ad032ee7103d34`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 2.1 MB (2057508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a12fd57420ca797ab383c58a488044d324c4d43b3c94a848f86a0524ed3064b4`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1c0c7b7a77e9375d8a75fb825fa274d9127ca96de79107550517be29501c817`  
		Last Modified: Tue, 16 Jun 2026 00:18:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:851f463d4778539d5e4981f972420f9a57ec2559488f8a59fba6abab6065032f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:734dd3d91f2d6cf217233f7a9dacc3c20ff0590246adb790f95713fb21c115de`

```dockerfile
```

-	Layers:
	-	`sha256:c0d4c203ef9f66cf827ec62098d7801e1c49f1187e0fe047fd32fc2a3271f636`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 94.3 KB (94304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b734d170b5463fa77dd77072e06d51a28efe59a53600d47435b015ebcadae92`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:ba5bf40b4adc1fe04f32e2e239fa9c0020d4e89bf4079493f8bc11a92c8f4b51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5738070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d12fbf86d6880aaa9d517425d9cecddcf545ba87e577a039dea9ea99ad53d8a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 05:59:15 GMT
ADD alpine-minirootfs-3.24.1-riscv64.tar.gz / # buildkit
# Tue, 16 Jun 2026 05:59:15 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 08:28:27 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 19 Jun 2026 08:28:31 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 19 Jun 2026 08:41:52 GMT
ENV MEMCACHED_VERSION=1.6.42
# Fri, 19 Jun 2026 08:41:52 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Fri, 19 Jun 2026 08:41:52 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Fri, 19 Jun 2026 08:41:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 19 Jun 2026 08:41:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 08:41:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 19 Jun 2026 08:41:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 08:41:53 GMT
USER memcache
# Fri, 19 Jun 2026 08:41:53 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 19 Jun 2026 08:41:53 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c34e5222b29b86391cdae95b0473ef789493ff1a0068a3a30b5d66f544bd7cf6`  
		Last Modified: Sun, 14 Jun 2026 06:47:00 GMT  
		Size: 3.6 MB (3574358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e09d95a0f414638430c0cd3ecfdcce75606201917a27c7cb2ce1e34cb928b26a`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a5335c7af79a1b08af55862ba77644afdae5544d9a7871e45c91b364bd4f71d`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 108.9 KB (108888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3622a6ea71515db1ef566afdbb121daed1f408aacf1519f4173b40dabe2ae627`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 2.1 MB (2053467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1db0e3e31ca3f2830f5404436e92b1862a4078adefacacec09a9580a3ad0a2`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1463b0fd26a37659aaad7f99696e5213764ad03bb094f40836c3309713d7a60`  
		Last Modified: Fri, 19 Jun 2026 08:42:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:aadb3b9338400b87692f95e00931e43940f8d6ddd13f046bd256848dd825e458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bde4b5a4a468d795a5f58dd934b371adfe72cd2ae24e166e1258ad65aa455a56`

```dockerfile
```

-	Layers:
	-	`sha256:debb70180cf674562f7ca321270e3dfa350c5d1596c05dbfcc27b38c65652528`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 94.3 KB (94300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a895bbe0bfec24678c1c92ddd283cb7392e0e8d229f31c769a23c95224c0d371`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:e1b640e8d192055e5c3ccd05b077776a0f4d35664191596f7a8230b2cd7ef0f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5823313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1ef6221f9c2854683b0633325a98a0e7a0d3b7d865b02d7cdf4c1d49d2e5090`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:21 GMT
ADD alpine-minirootfs-3.24.1-s390x.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:21 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:13:46 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:13:46 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:17:12 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:17:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:17:12 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:17:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:17:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:17:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:17:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:17:12 GMT
USER memcache
# Tue, 16 Jun 2026 00:17:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:17:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:da43be6afaaa3ec1b607461ce64380942a6d76c3d52cda4337b0770d9a96fa89`  
		Last Modified: Sun, 14 Jun 2026 06:47:25 GMT  
		Size: 3.7 MB (3709320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757d04238e02c9bbe1cfd4030cc19e29421650a1b1562a8ca4090d90e9ae17b0`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1949e0fa71fc91bebf4f2e4293108b27de8357d98f98b673bc4f3ed1980b52c`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 114.3 KB (114289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f0e22966bce79fbc8a20f7c27aa07ce63229bb50181319c810ca29f1fb4032`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 2.0 MB (1998350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15eb5e912ef8ec6e3abe76c361cdddb568d20a60be21be379d4d8d7d0ebaa11e`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a549d59ad0d4761ac6f4cca272c4bea521471ed091d0e79143bfda8ff29cf9ce`  
		Last Modified: Tue, 16 Jun 2026 00:17:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:6dbf7c8a98f02a949769403ad1c92583b34a28dccc66b7d83d91863785a6dad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a89d23372d19daf2d6d4e1c4de732f7864316ed5e7713b1103918303873683e`

```dockerfile
```

-	Layers:
	-	`sha256:099ab2d711ef73783b01895824a4664c7d65e2a333e81237b4766cf053a8f6f0`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 94.2 KB (94246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0eccbabf44891af00e622624c5cfd5a295656f82f1c15073b240ac34d47af96c`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine3.24`

```console
$ docker pull memcached@sha256:7381333da6d6ae06e02d8dfc87ee6f2c7cd0a19f7ba048d5efc538d2100e2208
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

### `memcached:1-alpine3.24` - linux; amd64

```console
$ docker pull memcached@sha256:ce375dd48f976d33bf35beb966cc37f202fd840a90891e58b9e71171fc74174d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5921579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19d284e7a8445d8dc70e97c673a8a0175d18f39d5336ccbdfa8b240c0ef3ce4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:29 GMT
ADD alpine-minirootfs-3.24.1-x86_64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:15:18 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:15:18 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:17:54 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:17:54 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:17:54 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:17:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:17:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:17:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:17:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:17:54 GMT
USER memcache
# Tue, 16 Jun 2026 00:17:54 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:17:54 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:55afa1ecc21d2bb5e5045f32dafee56272ffd89860bac26f6c32123439af26a4`  
		Last Modified: Sun, 14 Jun 2026 06:44:06 GMT  
		Size: 3.8 MB (3846391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb73756dcbbebc424eab53d3adda4d9f64001e7a91272a7b2a834622c08b093`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f0d6a5291334f2b54ec652193cd4e17ee22455b2f3ff3bd9b66acff6436c7b`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 106.1 KB (106066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ac11a8307528096ac745e0ef681b64854bbd012ffdfbce85587153eec73563`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 2.0 MB (1967772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3626493aad85d70a212bc66e9d45db8aef43b4bc662259563f916398165f1e64`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cdcd3f20e3aa439838f5491e6f457a42bad6c80ed9b099313bf79b57a721ea8`  
		Last Modified: Tue, 16 Jun 2026 00:18:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:bb948800301f1cae8e18e317f2b9e85636c86c4a1924ee85e125da37cb1333e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c3e084937eb543038244e151b03b8d9a0dce0b4d5bf87c2d471fa397ed5702`

```dockerfile
```

-	Layers:
	-	`sha256:9d05a792212c92363a76bb6a8205a6e7f386113b3efc1b5d600f93d4e237c975`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 94.9 KB (94897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee0e7e70ef03205f55c68bc1b74ac7854183aee4e871112794975dc852761b19`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.24` - linux; arm variant v6

```console
$ docker pull memcached@sha256:4b144cdbc67c11035b3d0f0c812b590ee694977f2f6a32321e538237bd2f841c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5573158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e9bb70df1535a2f8ca960f733a4404cbde900a13156a1f4446c2fd110258e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:25 GMT
ADD alpine-minirootfs-3.24.1-armhf.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:25 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:14:43 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:14:44 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:17:47 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:17:47 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:17:47 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:17:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:17:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:17:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:17:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:17:47 GMT
USER memcache
# Tue, 16 Jun 2026 00:17:47 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:17:47 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3c4836a46d600cfe9a422adf7a80205cb534097e6213325e0176c51f6e5cc02e`  
		Last Modified: Sun, 14 Jun 2026 06:44:57 GMT  
		Size: 3.6 MB (3553450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e732a60042adf5cff5fe4fe0de83f937f6e5c8896500f7023e8bf68ed0670d65`  
		Last Modified: Tue, 16 Jun 2026 00:17:51 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad86d1fea29db061a5ae896a0a595b144edcdb4af59deac2b75b0fb8f5fa2d4c`  
		Last Modified: Tue, 16 Jun 2026 00:17:50 GMT  
		Size: 102.6 KB (102624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f26dd2445dbf4d5624417ca290f5ae2e5774fa7fec4f5655cd2377ee3147e4`  
		Last Modified: Tue, 16 Jun 2026 00:17:51 GMT  
		Size: 1.9 MB (1915730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080a186f0ca6beb06a5ce4a86fbc71f5b9995713fcc899c73f995f251ef7c987`  
		Last Modified: Tue, 16 Jun 2026 00:17:51 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c4d4f455f9a2b633cca28e3aa2190e4c42ca83ca6e3ea88ea4abe16944d238`  
		Last Modified: Tue, 16 Jun 2026 00:17:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:d6b7abf6ef34abf12ab2c7f84bd29ac2461eb3271d1c4070456ed9b94e4b41a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43a767571287c8ca227e321ee8d65f9da82e558098bedbb15888434dcc1ce9fa`

```dockerfile
```

-	Layers:
	-	`sha256:1794ccef4392c0db4ba36ad7fde22cdacbda40f4d56f0adbef802163c87e066c`  
		Last Modified: Tue, 16 Jun 2026 00:17:51 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.24` - linux; arm variant v7

```console
$ docker pull memcached@sha256:848c5e0ced69b802cca72c23bec05a4c6f23136212a4a1d5cc22b7c8f0154bf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:286f62a53a8947036e39f2b79567b31d38309fd84c7a39e43de8c5f9817a2f64`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:26 GMT
ADD alpine-minirootfs-3.24.1-armv7.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:26 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:17:59 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:17:59 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:20:56 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:20:56 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:20:56 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:20:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:20:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:20:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:20:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:20:56 GMT
USER memcache
# Tue, 16 Jun 2026 00:20:56 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:20:56 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bc03a9e5b4dd452551f246e199537fe7afc1765f53f510bc81d26df9845e4008`  
		Last Modified: Sun, 14 Jun 2026 06:45:22 GMT  
		Size: 3.3 MB (3260615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f0249bacfc8953b72899bf7b6c904c8750482fce4c93108f57b2c64228b279`  
		Last Modified: Tue, 16 Jun 2026 00:21:00 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95e1b321ffc31d01e766d5d1d054967d613940563406fc54ee981926b7f6049`  
		Last Modified: Tue, 16 Jun 2026 00:21:01 GMT  
		Size: 92.4 KB (92366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce112e60c1b15077277c233a7707831818dff0a15f1fc977ebebc93f817dad43`  
		Last Modified: Tue, 16 Jun 2026 00:21:01 GMT  
		Size: 1.9 MB (1875183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32fa6ed5b14fd6fcf96a7cde2996063f10b8efe802c386479288a232af826027`  
		Last Modified: Tue, 16 Jun 2026 00:21:01 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6648f8180a4eea1f5197f2fa2d356fbbf4e5f65345e189e720e227af64a5e31`  
		Last Modified: Tue, 16 Jun 2026 00:21:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:59387f31eff7cfb3166c5e6d4bad92e255705affcc15c84c4a06c86ecb1a9890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:174eb460b1df4523a4f71ba5a996f2285fa845fe8ef76d2df3ea8c4962c6b6ca`

```dockerfile
```

-	Layers:
	-	`sha256:4ff5e70775e819cab551295c56b58fdb0c44c105cdc4f72247e3968accd2ab2f`  
		Last Modified: Tue, 16 Jun 2026 00:21:00 GMT  
		Size: 94.3 KB (94315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00f10e1301c7e61396658f7e3ed330e400a9f304c6a0323de8ff644aba987474`  
		Last Modified: Tue, 16 Jun 2026 00:21:01 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.24` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:33261748facce282dbe4dbb4d9f875139680fce4cefc13cb9ad8e1ced23f9557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6250475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1614bb2865c8f849c2bc5bf77703a1ab711695c607a8bc6edb013a076ec16d6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:20 GMT
ADD alpine-minirootfs-3.24.1-aarch64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:20 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:13:18 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:13:18 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:16:06 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:16:06 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:16:06 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:16:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:16:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:16:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:16:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:16:06 GMT
USER memcache
# Tue, 16 Jun 2026 00:16:06 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:16:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5de55e5ef9c033997441461efe7ba23a986db059c0bb78b38f84ee0d72b99167`  
		Last Modified: Sun, 14 Jun 2026 06:44:31 GMT  
		Size: 4.2 MB (4183037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5faa19f06c4d5e26332739c7f08fd3dcd2c81817471c62029a6d99af6be8748`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377a35d28f00766e2679c788b95b0a67b9aa5a76c8ef701a2a9604e2a00c3b46`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 121.8 KB (121841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0b819e89558d70f1401ca58cbc19c58ae13e15be8184fd9b2733e022f318a4`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 1.9 MB (1944247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca539cef48ff8c3f723ab23506b6786c9ed26a9cac713601b71de2dc775d26a`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c4c456deed244daa6d7076f40a1cf0364d294059bb43e533677a89027843b15`  
		Last Modified: Tue, 16 Jun 2026 00:16:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:4d25960abc53b5ba1896b8f5ee04ba5ac1389900ab9b413eb62285af7281aedb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d1a4b7ad428a08c8a174d5ecd9763d530e849f54a2d9b90aef934e54b9477d4`

```dockerfile
```

-	Layers:
	-	`sha256:9c0a8e5e07390fae6abe9204450009671011c4d2d5aa5fe4afdd82324fdb49b9`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 94.4 KB (94351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ee01158358d01c082867cf46a5225cf101013e4d5b7eae18fc7853e277ff0f4`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 20.7 KB (20727 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.24` - linux; 386

```console
$ docker pull memcached@sha256:5436d0ef6e12f2f8e454384ff4a703132b3fe820c41a55336f520bb5d1622574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5702329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8946be3d97c7b9825159f58cbf832b131c75cb90b3fb46a40d5429b9ffe32bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:19 GMT
ADD alpine-minirootfs-3.24.1-x86.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:19 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:13:59 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:13:59 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:16:45 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:16:45 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:16:45 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:16:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:16:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:16:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:16:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:16:46 GMT
USER memcache
# Tue, 16 Jun 2026 00:16:46 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:16:46 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f86df9d778509895efbf9363d8fcb0cbe0b772de536c7218e4c4c947f0be879f`  
		Last Modified: Sun, 14 Jun 2026 06:45:46 GMT  
		Size: 3.7 MB (3670141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043137360442e605bc150f28f20e1fa2d23d90131370bc405ad7d35309594491`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900ce6eeaece12033b12f1c8641c33dcf62ff2525584411911368cfcd0b38224`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 110.7 KB (110729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e8cc1c8f6bc6391eb1a43a46f0b55ca7845f824fc0f2fc7ae7587a7715814e`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 1.9 MB (1920111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d94f6e4d3be92188fc182a3557fe43af5bc9f3e768a7f265977743a56eea527e`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f8a19f18dfff271426de7a17ab6780788fa4345d5fa0120e6d03720d552bd4`  
		Last Modified: Tue, 16 Jun 2026 00:16:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:00dc6a7f29b7f2f5ac46fc5678b80c43c7b1e46b4ca3c84c5597034180aeb644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6de04019c7775544db9adbb4c4558d0e7c842c279e5d70532b2ac0b988ac1345`

```dockerfile
```

-	Layers:
	-	`sha256:80895f8f5e9c9b015e419096426322f4c86c33d55ca8860ee046b61d52782847`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 94.9 KB (94852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c69be8c1f82a066b46cc389712508e85c1dcd77e649c922dba46ace64b343ae`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.24` - linux; ppc64le

```console
$ docker pull memcached@sha256:c7857941a51b85b136781035703afcc8854a2d70fa2091208a51f8bb7e71f934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5998515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b02b2222212c64e444ac1a2227b19f0cfb1282c8a8ced386c1b79ae48c641b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:15 GMT
ADD alpine-minirootfs-3.24.1-ppc64le.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:15 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:15:37 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:15:38 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:18:22 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:18:22 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:18:22 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:18:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:18:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:18:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:18:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:18:22 GMT
USER memcache
# Tue, 16 Jun 2026 00:18:22 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:18:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3ebcdcd395ccee658b9200e4b27d7699e5d6ed9f6c1858dea12781aac519ff59`  
		Last Modified: Sun, 14 Jun 2026 06:46:36 GMT  
		Size: 3.8 MB (3813400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b108e2058722fb0fb5a9310e8ebe82ab4b9c021228a94b3125ba49d318e9667`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb8160ed736eda8513164d5d703082fb0c9af9e037472ab70a02579caa3eb99`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 126.3 KB (126252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5cb88dd03ce07ecf1613c2aff220fb392763d8f22edc900c4ad032ee7103d34`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 2.1 MB (2057508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a12fd57420ca797ab383c58a488044d324c4d43b3c94a848f86a0524ed3064b4`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1c0c7b7a77e9375d8a75fb825fa274d9127ca96de79107550517be29501c817`  
		Last Modified: Tue, 16 Jun 2026 00:18:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:851f463d4778539d5e4981f972420f9a57ec2559488f8a59fba6abab6065032f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:734dd3d91f2d6cf217233f7a9dacc3c20ff0590246adb790f95713fb21c115de`

```dockerfile
```

-	Layers:
	-	`sha256:c0d4c203ef9f66cf827ec62098d7801e1c49f1187e0fe047fd32fc2a3271f636`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 94.3 KB (94304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b734d170b5463fa77dd77072e06d51a28efe59a53600d47435b015ebcadae92`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.24` - linux; riscv64

```console
$ docker pull memcached@sha256:ba5bf40b4adc1fe04f32e2e239fa9c0020d4e89bf4079493f8bc11a92c8f4b51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5738070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d12fbf86d6880aaa9d517425d9cecddcf545ba87e577a039dea9ea99ad53d8a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 05:59:15 GMT
ADD alpine-minirootfs-3.24.1-riscv64.tar.gz / # buildkit
# Tue, 16 Jun 2026 05:59:15 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 08:28:27 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 19 Jun 2026 08:28:31 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 19 Jun 2026 08:41:52 GMT
ENV MEMCACHED_VERSION=1.6.42
# Fri, 19 Jun 2026 08:41:52 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Fri, 19 Jun 2026 08:41:52 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Fri, 19 Jun 2026 08:41:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 19 Jun 2026 08:41:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 08:41:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 19 Jun 2026 08:41:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 08:41:53 GMT
USER memcache
# Fri, 19 Jun 2026 08:41:53 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 19 Jun 2026 08:41:53 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c34e5222b29b86391cdae95b0473ef789493ff1a0068a3a30b5d66f544bd7cf6`  
		Last Modified: Sun, 14 Jun 2026 06:47:00 GMT  
		Size: 3.6 MB (3574358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e09d95a0f414638430c0cd3ecfdcce75606201917a27c7cb2ce1e34cb928b26a`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a5335c7af79a1b08af55862ba77644afdae5544d9a7871e45c91b364bd4f71d`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 108.9 KB (108888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3622a6ea71515db1ef566afdbb121daed1f408aacf1519f4173b40dabe2ae627`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 2.1 MB (2053467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1db0e3e31ca3f2830f5404436e92b1862a4078adefacacec09a9580a3ad0a2`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1463b0fd26a37659aaad7f99696e5213764ad03bb094f40836c3309713d7a60`  
		Last Modified: Fri, 19 Jun 2026 08:42:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:aadb3b9338400b87692f95e00931e43940f8d6ddd13f046bd256848dd825e458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bde4b5a4a468d795a5f58dd934b371adfe72cd2ae24e166e1258ad65aa455a56`

```dockerfile
```

-	Layers:
	-	`sha256:debb70180cf674562f7ca321270e3dfa350c5d1596c05dbfcc27b38c65652528`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 94.3 KB (94300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a895bbe0bfec24678c1c92ddd283cb7392e0e8d229f31c769a23c95224c0d371`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.24` - linux; s390x

```console
$ docker pull memcached@sha256:e1b640e8d192055e5c3ccd05b077776a0f4d35664191596f7a8230b2cd7ef0f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5823313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1ef6221f9c2854683b0633325a98a0e7a0d3b7d865b02d7cdf4c1d49d2e5090`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:21 GMT
ADD alpine-minirootfs-3.24.1-s390x.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:21 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:13:46 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:13:46 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:17:12 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:17:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:17:12 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:17:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:17:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:17:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:17:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:17:12 GMT
USER memcache
# Tue, 16 Jun 2026 00:17:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:17:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:da43be6afaaa3ec1b607461ce64380942a6d76c3d52cda4337b0770d9a96fa89`  
		Last Modified: Sun, 14 Jun 2026 06:47:25 GMT  
		Size: 3.7 MB (3709320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757d04238e02c9bbe1cfd4030cc19e29421650a1b1562a8ca4090d90e9ae17b0`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1949e0fa71fc91bebf4f2e4293108b27de8357d98f98b673bc4f3ed1980b52c`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 114.3 KB (114289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f0e22966bce79fbc8a20f7c27aa07ce63229bb50181319c810ca29f1fb4032`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 2.0 MB (1998350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15eb5e912ef8ec6e3abe76c361cdddb568d20a60be21be379d4d8d7d0ebaa11e`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a549d59ad0d4761ac6f4cca272c4bea521471ed091d0e79143bfda8ff29cf9ce`  
		Last Modified: Tue, 16 Jun 2026 00:17:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:6dbf7c8a98f02a949769403ad1c92583b34a28dccc66b7d83d91863785a6dad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a89d23372d19daf2d6d4e1c4de732f7864316ed5e7713b1103918303873683e`

```dockerfile
```

-	Layers:
	-	`sha256:099ab2d711ef73783b01895824a4664c7d65e2a333e81237b4766cf053a8f6f0`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 94.2 KB (94246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0eccbabf44891af00e622624c5cfd5a295656f82f1c15073b240ac34d47af96c`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-trixie`

```console
$ docker pull memcached@sha256:85c0ab87f71b8b3ade708271177a8e5efca5e93c00287b6f25a2d74a27180bfa
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
$ docker pull memcached@sha256:09ac4118d89005e47ef3118221840c62f0fa909a2bee07ff571ae1ae59d9a79b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32204821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ad15119e1f73d99f3fbdc56187ea014f4fae2c8fcbe215c259f2fb2b387aefa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:23:00 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 11 Jun 2026 00:23:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:25:47 GMT
ENV MEMCACHED_VERSION=1.6.42
# Thu, 11 Jun 2026 00:25:47 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Thu, 11 Jun 2026 00:25:47 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Thu, 11 Jun 2026 00:25:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 11 Jun 2026 00:25:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:25:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 11 Jun 2026 00:25:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:25:47 GMT
USER memcache
# Thu, 11 Jun 2026 00:25:47 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 11 Jun 2026 00:25:47 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7883ff600bb4cc730c755ccb8be3f5a06371865abe00be70037283c04f4f3f5`  
		Last Modified: Thu, 11 Jun 2026 00:25:53 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d73a0d6b79b50aa2429aebc30b68c38fb0fb43a4a597ce0dd3936605fbb8912e`  
		Last Modified: Thu, 11 Jun 2026 00:25:53 GMT  
		Size: 136.7 KB (136685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5716730726452d6a54ff03d59c7dffbb7ed4f05836877734acf92f7a0512d6a9`  
		Last Modified: Thu, 11 Jun 2026 00:25:53 GMT  
		Size: 2.3 MB (2281206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f338318b7809e3c4be59b7eccaa1e5387cdbe8015c49eac3267097258c54ae89`  
		Last Modified: Thu, 11 Jun 2026 00:25:53 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ca13d7300d84ca43fcce2aa8304787015f83333e041c81c04796354eadce6b`  
		Last Modified: Thu, 11 Jun 2026 00:25:54 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:3d476e3ec28b0dda5046a3223b0e5a8c9ab8dec20bb294a8853da81d828c154d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e2358f67931681260618f406ea3e0032f17f7a82b2a7d36e5511e6413a7133f`

```dockerfile
```

-	Layers:
	-	`sha256:9cb94c17b8cb82e97f6ad217227fa08e25e0fdc9b96fd2fe418e0acc53911305`  
		Last Modified: Thu, 11 Jun 2026 00:25:53 GMT  
		Size: 2.0 MB (2008368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f8a18d24b8d75bd4b8d856878db21e4d4df7e3e553b9d72d0156bbe58c869d3`  
		Last Modified: Thu, 11 Jun 2026 00:25:53 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; arm variant v5

```console
$ docker pull memcached@sha256:f059b77d971253090e3862e28d374840935b5c06467230e9bea207fdb6ef3bf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30316631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c99754215fd2490daf10c8c1046bee3ab237e1e95bd4b46ef0610ca9d1c9badc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:19:47 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 11 Jun 2026 00:19:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:23:08 GMT
ENV MEMCACHED_VERSION=1.6.42
# Thu, 11 Jun 2026 00:23:08 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Thu, 11 Jun 2026 00:23:08 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Thu, 11 Jun 2026 00:23:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 11 Jun 2026 00:23:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:23:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 11 Jun 2026 00:23:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:23:08 GMT
USER memcache
# Thu, 11 Jun 2026 00:23:08 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 11 Jun 2026 00:23:08 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ed883f3fd95b7edef302d7ca9520eefdae280af081509bd7e9e5b5ff8f4cda7c`  
		Last Modified: Wed, 10 Jun 2026 23:41:17 GMT  
		Size: 28.0 MB (27959200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e92527947bdcc341ab63777422e7409751516a8bc5ffc61040d76b72e7d58c`  
		Last Modified: Thu, 11 Jun 2026 00:23:14 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c52c9bd0c151ce908cf5e8c55694b4a321a916d3053e9e4cd3b06837e55f325`  
		Last Modified: Thu, 11 Jun 2026 00:23:14 GMT  
		Size: 144.2 KB (144156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ec2615dd4e79e84378f7223c9d7c70a6cdfb8835717c19cadbab17a726210d`  
		Last Modified: Thu, 11 Jun 2026 00:23:14 GMT  
		Size: 2.2 MB (2211763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4249a738c6e8e951ca0bf1608e335442f8f50ff9fe57a524b1bdb472e59ed1`  
		Last Modified: Thu, 11 Jun 2026 00:23:14 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab171fa641968acda113ed8ec0cbff5159a4895efed9c4e08bb6e466a40fb5ce`  
		Last Modified: Thu, 11 Jun 2026 00:23:15 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:a7356b3e73eada1ea16535f45e9a297b7913adfb103e9df5d0a2ee333c58f443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c75fc3f8c74e188d3585642b303189b73ae78c14b089bd14f0d37da2b085f25`

```dockerfile
```

-	Layers:
	-	`sha256:5a953398782781fbd31e5d1fb67c1cdeb82c91397fb27ce32b9d756cc938a03a`  
		Last Modified: Thu, 11 Jun 2026 00:23:14 GMT  
		Size: 2.0 MB (2011371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aeae6ddb09b0b52fdf1e1db9b67dfa04fba888fbba5c54b1b7e30ecbd56dafde`  
		Last Modified: Thu, 11 Jun 2026 00:23:14 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; arm variant v7

```console
$ docker pull memcached@sha256:7b20950329f422c7b322057fe1f944f98589cf937e5e65118b6d4bb241436ffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28513288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5d65e3287f7256814db41a73f2978df2252f6ac399369fe1a7a3eb1c4ceb3e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:21:55 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 11 Jun 2026 00:21:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:25:06 GMT
ENV MEMCACHED_VERSION=1.6.42
# Thu, 11 Jun 2026 00:25:06 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Thu, 11 Jun 2026 00:25:06 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Thu, 11 Jun 2026 00:25:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 11 Jun 2026 00:25:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:25:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 11 Jun 2026 00:25:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:25:06 GMT
USER memcache
# Thu, 11 Jun 2026 00:25:06 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 11 Jun 2026 00:25:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4bd6ddea06d5009ee47ddb0f254a2569aff0230c005869ebd416b20295d945c0`  
		Last Modified: Wed, 10 Jun 2026 23:42:34 GMT  
		Size: 26.2 MB (26211004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bcac116a5bd6f8c4ba910742373294134be4443587cce918db3492895262e16`  
		Last Modified: Thu, 11 Jun 2026 00:25:12 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af6a74cecf5734c352e3c2ea5fb348246cfe77549b6cb2afe3116aaf39983ff8`  
		Last Modified: Thu, 11 Jun 2026 00:25:12 GMT  
		Size: 135.4 KB (135382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6189c46b05f5cdb39083034f258358c5472cc6824a25a7dc8a8f60ae58891116`  
		Last Modified: Thu, 11 Jun 2026 00:25:12 GMT  
		Size: 2.2 MB (2165385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfeedbf1b9c25a3c29e32962704f935689b2b60c4096315dbee3365a9cec4dc0`  
		Last Modified: Thu, 11 Jun 2026 00:25:12 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0309704e28c847b1dd0249a490a5774838b3d27bf059481108e0f1a300efd4ae`  
		Last Modified: Thu, 11 Jun 2026 00:25:13 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:84793c5cdc418c73cc53c1dcdf3ebaf9d1c2a7910ec63c85d179a691e05f1ddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0981cd8d43f93fb996bbc87f0659a7c3a7163d74a5c84503eb77588ed240010c`

```dockerfile
```

-	Layers:
	-	`sha256:39acaedd56024e59130ae654692bdff06d01b71719567ede3d9ece539679150e`  
		Last Modified: Thu, 11 Jun 2026 00:25:13 GMT  
		Size: 2.0 MB (2009828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ada0017eed4fa0f3db9a2e1669d0eb74e2908e65a483af6819df971d18d767a`  
		Last Modified: Thu, 11 Jun 2026 00:25:12 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:a36eca5b5840c718ca41526a871fd751dc96965f182778a7631a0c2896c3f44a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32566560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31c7500da651c7c5945a2db8b00248c02ad2947b4eccb66b464759cd6f4ea2c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:23:08 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 11 Jun 2026 00:23:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:26:08 GMT
ENV MEMCACHED_VERSION=1.6.42
# Thu, 11 Jun 2026 00:26:08 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Thu, 11 Jun 2026 00:26:08 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Thu, 11 Jun 2026 00:26:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 11 Jun 2026 00:26:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:26:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 11 Jun 2026 00:26:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:26:08 GMT
USER memcache
# Thu, 11 Jun 2026 00:26:08 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 11 Jun 2026 00:26:08 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb68ad832950ffa1d5fe24c7e7ee4e061b358d6bcb14dfdb1bb2dec4c557f7a2`  
		Last Modified: Thu, 11 Jun 2026 00:26:15 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f6f966199cad211cd492fc65c6c927fde3a05499bdd9a2112d65deb706cfbc6`  
		Last Modified: Thu, 11 Jun 2026 00:26:14 GMT  
		Size: 153.5 KB (153481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3314b48b94577865e96641c557d5048167254c141db1725db6a5b7a623b68f7b`  
		Last Modified: Thu, 11 Jun 2026 00:26:15 GMT  
		Size: 2.3 MB (2263038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e33e48bcfd48ec271ffa516b5c3b03458185abfb31596aca0b854e9c9367fb9`  
		Last Modified: Thu, 11 Jun 2026 00:26:15 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb41e83cd817b17ff4c2b62ce482681096f6783b2a32be0407cada277d4f293`  
		Last Modified: Thu, 11 Jun 2026 00:26:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:0253549da149222537eeb2e51a1b411b7662c20d8c8964e71967cf670ce9c992
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af9894c8fa8e920a07bf631bed91c9b67398338986159408229a8da050b21c3b`

```dockerfile
```

-	Layers:
	-	`sha256:a11c09037e68845f3c8c01efb996710c3b2d21ba868a98c3ba2582a28d0f1047`  
		Last Modified: Thu, 11 Jun 2026 00:26:15 GMT  
		Size: 2.0 MB (2008676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40468c38b6f60c4625c352d5bdc83ea61510da0efeb2542777603da191a5d2fa`  
		Last Modified: Thu, 11 Jun 2026 00:26:14 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; 386

```console
$ docker pull memcached@sha256:e134667b3198bc9f05962d9bb97cf359ab04c31cb8d11c75e2683de54cebd46e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33675616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cba4eb3d3e82545273aa5ff6f0e6f7bf2b1240176b9489d2315fcf290b9c49a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:18:22 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 11 Jun 2026 00:18:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:21:26 GMT
ENV MEMCACHED_VERSION=1.6.42
# Thu, 11 Jun 2026 00:21:26 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Thu, 11 Jun 2026 00:21:26 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Thu, 11 Jun 2026 00:21:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 11 Jun 2026 00:21:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:21:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 11 Jun 2026 00:21:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:21:26 GMT
USER memcache
# Thu, 11 Jun 2026 00:21:26 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 11 Jun 2026 00:21:26 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:720f951a68f4f9ab464e52b53cf88cfb86bc876b3f00956d000420777ab93c0c`  
		Last Modified: Wed, 10 Jun 2026 23:40:30 GMT  
		Size: 31.3 MB (31301194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2607fca8a1b7fbebf74214d1b33f4f0a54aed5fef2bed18ddc89836a7d00e04b`  
		Last Modified: Thu, 11 Jun 2026 00:21:31 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4620fc98d601bc463a1a505fb0ecf42cb42fa76088d5e80dee41474c74f39f1`  
		Last Modified: Thu, 11 Jun 2026 00:21:32 GMT  
		Size: 147.5 KB (147511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a4c97894b05376111399fa19e7429f36d493cb528c53cb81318a2920d5a954`  
		Last Modified: Thu, 11 Jun 2026 00:21:32 GMT  
		Size: 2.2 MB (2225398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f4a764af02d7ba61dd0909ddb429ba92c9a367243a225936fd625fda113340`  
		Last Modified: Thu, 11 Jun 2026 00:21:32 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52e82109e627ebc0d88a9f7c357b97f14b8ac06bdab5d0b6aa50c3b958a13a8`  
		Last Modified: Thu, 11 Jun 2026 00:21:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:6670b6485b54bcae32ddeda5c2d1764d0ee2066f036d0c17f2cc89734f0be8c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d0aef4dacfecea9e8dbc20498736f77e48bf5106eb60bcfa08c1e81a5c4f06c`

```dockerfile
```

-	Layers:
	-	`sha256:0ebdf5fe0d474785e4448d36043967631fb650ec7b52bd865126a7360978a2ea`  
		Last Modified: Thu, 11 Jun 2026 00:21:32 GMT  
		Size: 2.0 MB (2005525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f257ddeb15df7a03d8e7bb57e01531d894c998af32f33cb528199914bd8f6e1c`  
		Last Modified: Thu, 11 Jun 2026 00:21:32 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; ppc64le

```console
$ docker pull memcached@sha256:25e41a95392ee3c63e35711fec0648fbedc92c6be718456ad8fb89ab66f4e825
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36762178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a04e55188a4c60d5cd8eb00b50628fd87658d0d1814097b40417d71b18479e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 02:36:51 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 11 Jun 2026 02:36:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:59:49 GMT
ENV MEMCACHED_VERSION=1.6.42
# Thu, 11 Jun 2026 02:59:49 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Thu, 11 Jun 2026 02:59:49 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Thu, 11 Jun 2026 02:59:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 11 Jun 2026 02:59:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 02:59:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 11 Jun 2026 02:59:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 02:59:50 GMT
USER memcache
# Thu, 11 Jun 2026 02:59:50 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 11 Jun 2026 02:59:50 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9d6b2e320e2b74843186d830e8202c50ebfaeccf823d239e3e3e349a8a508d80`  
		Last Modified: Thu, 11 Jun 2026 00:24:42 GMT  
		Size: 33.6 MB (33606340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d389c79e93b7c7b3cc2a8226edeb6460d8101e245642213048c1a187d08a935d`  
		Last Modified: Thu, 11 Jun 2026 03:00:07 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7bb22e37f822a0e94fa24cd439d7666c214637b0d59c384dd19e12674c74a82`  
		Last Modified: Thu, 11 Jun 2026 03:00:07 GMT  
		Size: 170.4 KB (170363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82cbb5c5e79cdcec98bd562e1a62768994b805ff7d805b6b75b5bf0e349cff8`  
		Last Modified: Thu, 11 Jun 2026 03:00:06 GMT  
		Size: 3.0 MB (2983963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e60c6f3b8886967bbbabece38cfe74eccdfde98cdae42045a33c5b2b29fd6da`  
		Last Modified: Thu, 11 Jun 2026 03:00:08 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc87d370da3b9877481bf9620bda982328b4d722812ec3e77a7b4c50d016eb33`  
		Last Modified: Thu, 11 Jun 2026 03:00:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:0101df893b4af64daa7ee54d012d7b8682b6c1a9ad1d85700cf8ff269664b19e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b06e6f43b0b95c657fb0043338f12918e63fcac640df48783c49ac29092afb0b`

```dockerfile
```

-	Layers:
	-	`sha256:8ed9fcb43f9f08fb8702ae2709d918b6370866fb4697ddf04b93f42080b23d94`  
		Last Modified: Thu, 11 Jun 2026 03:00:08 GMT  
		Size: 2.0 MB (2011969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c6915dddb9ee13a9cd4156b07c521335c76c9687dcb3a08e66e147af9d99453`  
		Last Modified: Thu, 11 Jun 2026 03:00:06 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; riscv64

```console
$ docker pull memcached@sha256:918c03d1a36c36f13b67e3fbf100f93adad50fbbb452fecc3769db0b8cde487c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30626726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1c8f5f48c37fb2ef15e785c080f746aec65afab782672de8b6a63bd88942e41`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1781049600'
# Fri, 12 Jun 2026 00:28:54 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 12 Jun 2026 00:29:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jun 2026 00:42:57 GMT
ENV MEMCACHED_VERSION=1.6.42
# Fri, 12 Jun 2026 00:42:57 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Fri, 12 Jun 2026 00:42:57 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Fri, 12 Jun 2026 00:42:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 12 Jun 2026 00:42:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Jun 2026 00:42:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 12 Jun 2026 00:42:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2026 00:42:57 GMT
USER memcache
# Fri, 12 Jun 2026 00:42:57 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 12 Jun 2026 00:42:57 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0b510fe8545cab831b696965b5a825649c5c945581e912d31a08a0b30ff940c0`  
		Last Modified: Thu, 11 Jun 2026 03:01:06 GMT  
		Size: 28.3 MB (28282305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35e7a152e660b7a61f448299ac325c28198a870bc53d54cd2584d111c3cef30`  
		Last Modified: Fri, 12 Jun 2026 00:43:44 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d26b2af070be1166e165d4bd1eb073a685622ddb1edb5cf4382cb7825faa21a`  
		Last Modified: Fri, 12 Jun 2026 00:43:44 GMT  
		Size: 133.1 KB (133071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ac4d08e6c19ea726574dc4cd56f4d39216f427cdfd9d6e19c91b06583e6630`  
		Last Modified: Fri, 12 Jun 2026 00:43:44 GMT  
		Size: 2.2 MB (2209833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:039ac44117911671ad0fca8638fa93282ad5865273a55e1328d3180ac5c4f463`  
		Last Modified: Fri, 12 Jun 2026 00:43:44 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65787f51c4d435ccf6c4c9c11e27fe642bd5af3fdd4489e11005614f51c21c29`  
		Last Modified: Fri, 12 Jun 2026 00:43:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:5db8b7d0f9f634b02f9f4dfb45d2f0d3fb2ef1778c3e52058327cd5dec31ebce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0de6ff12136279a3005dae5ce29967a780efb19d8a50b71f33b8153d38859c49`

```dockerfile
```

-	Layers:
	-	`sha256:256f6cfcbc556a40776a58fddd91ccacf0870ab5955a42e7e3ea23601ff76633`  
		Last Modified: Fri, 12 Jun 2026 00:43:44 GMT  
		Size: 2.0 MB (2002332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdfa564b06be9c36a9d81da00994136c858ca65d81762277469168a418a9c9fa`  
		Last Modified: Fri, 12 Jun 2026 00:43:44 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; s390x

```console
$ docker pull memcached@sha256:75f4e343898a5a326a82f6560f0efdd5d11c5aea7a710327cdfd400ac3244341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32291904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd9e841717be4c79746136574299d1a6552f88fe8566606318efb07377ef20c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:19:32 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 11 Jun 2026 00:19:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:22:55 GMT
ENV MEMCACHED_VERSION=1.6.42
# Thu, 11 Jun 2026 00:22:55 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Thu, 11 Jun 2026 00:22:55 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Thu, 11 Jun 2026 00:22:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 11 Jun 2026 00:22:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:22:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 11 Jun 2026 00:22:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:22:55 GMT
USER memcache
# Thu, 11 Jun 2026 00:22:55 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 11 Jun 2026 00:22:55 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:760dcf74fdfe93300ce15b5b23adf9aa4af45b6ba9d69925863198f64881a537`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 29.9 MB (29851354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159eeccf7c6aa583901267e3c00bf9c124c32be82a1074722d2be0b547fee632`  
		Last Modified: Thu, 11 Jun 2026 00:23:05 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d08bb26724ea31dfaf95eb6c1647b7686671b3869632300d6056a05c3532bd`  
		Last Modified: Thu, 11 Jun 2026 00:23:05 GMT  
		Size: 140.5 KB (140545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b341a8e7ca68a391e79c556246f3f0b81e4a5e747fed517e274d78f49faa30`  
		Last Modified: Thu, 11 Jun 2026 00:23:05 GMT  
		Size: 2.3 MB (2298492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff1b1dd9080cb995308882030f9579f4c5bf2af5b26b7270d6682de75f6e6d5`  
		Last Modified: Thu, 11 Jun 2026 00:23:05 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075343c77f8c8b9a1bb9fe079e853c0e4628b60f1fff7d8dce82d38c3a344bf8`  
		Last Modified: Thu, 11 Jun 2026 00:23:06 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:1f977b6725f519f48d75ffc92c711df863d7c0e4a1d1f0c5a5bc6605533f35e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1104b534613c8d2cc0544b9adf96821b4f7f623262ef6ddc425f13fa94427850`

```dockerfile
```

-	Layers:
	-	`sha256:66bb879abbe8f943d53561fcf4f4262e1b78fb31b6aa3fdac560ffdc45e3d4b5`  
		Last Modified: Thu, 11 Jun 2026 00:23:05 GMT  
		Size: 2.0 MB (2009805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e448bf5a0443ce0296756453f8bca10e0ec97ebc01576de74a28f60b78299f2b`  
		Last Modified: Thu, 11 Jun 2026 00:23:05 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6`

```console
$ docker pull memcached@sha256:85c0ab87f71b8b3ade708271177a8e5efca5e93c00287b6f25a2d74a27180bfa
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
$ docker pull memcached@sha256:09ac4118d89005e47ef3118221840c62f0fa909a2bee07ff571ae1ae59d9a79b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32204821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ad15119e1f73d99f3fbdc56187ea014f4fae2c8fcbe215c259f2fb2b387aefa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:23:00 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 11 Jun 2026 00:23:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:25:47 GMT
ENV MEMCACHED_VERSION=1.6.42
# Thu, 11 Jun 2026 00:25:47 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Thu, 11 Jun 2026 00:25:47 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Thu, 11 Jun 2026 00:25:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 11 Jun 2026 00:25:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:25:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 11 Jun 2026 00:25:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:25:47 GMT
USER memcache
# Thu, 11 Jun 2026 00:25:47 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 11 Jun 2026 00:25:47 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7883ff600bb4cc730c755ccb8be3f5a06371865abe00be70037283c04f4f3f5`  
		Last Modified: Thu, 11 Jun 2026 00:25:53 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d73a0d6b79b50aa2429aebc30b68c38fb0fb43a4a597ce0dd3936605fbb8912e`  
		Last Modified: Thu, 11 Jun 2026 00:25:53 GMT  
		Size: 136.7 KB (136685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5716730726452d6a54ff03d59c7dffbb7ed4f05836877734acf92f7a0512d6a9`  
		Last Modified: Thu, 11 Jun 2026 00:25:53 GMT  
		Size: 2.3 MB (2281206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f338318b7809e3c4be59b7eccaa1e5387cdbe8015c49eac3267097258c54ae89`  
		Last Modified: Thu, 11 Jun 2026 00:25:53 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ca13d7300d84ca43fcce2aa8304787015f83333e041c81c04796354eadce6b`  
		Last Modified: Thu, 11 Jun 2026 00:25:54 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:3d476e3ec28b0dda5046a3223b0e5a8c9ab8dec20bb294a8853da81d828c154d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e2358f67931681260618f406ea3e0032f17f7a82b2a7d36e5511e6413a7133f`

```dockerfile
```

-	Layers:
	-	`sha256:9cb94c17b8cb82e97f6ad217227fa08e25e0fdc9b96fd2fe418e0acc53911305`  
		Last Modified: Thu, 11 Jun 2026 00:25:53 GMT  
		Size: 2.0 MB (2008368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f8a18d24b8d75bd4b8d856878db21e4d4df7e3e553b9d72d0156bbe58c869d3`  
		Last Modified: Thu, 11 Jun 2026 00:25:53 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm variant v5

```console
$ docker pull memcached@sha256:f059b77d971253090e3862e28d374840935b5c06467230e9bea207fdb6ef3bf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30316631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c99754215fd2490daf10c8c1046bee3ab237e1e95bd4b46ef0610ca9d1c9badc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:19:47 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 11 Jun 2026 00:19:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:23:08 GMT
ENV MEMCACHED_VERSION=1.6.42
# Thu, 11 Jun 2026 00:23:08 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Thu, 11 Jun 2026 00:23:08 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Thu, 11 Jun 2026 00:23:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 11 Jun 2026 00:23:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:23:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 11 Jun 2026 00:23:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:23:08 GMT
USER memcache
# Thu, 11 Jun 2026 00:23:08 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 11 Jun 2026 00:23:08 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ed883f3fd95b7edef302d7ca9520eefdae280af081509bd7e9e5b5ff8f4cda7c`  
		Last Modified: Wed, 10 Jun 2026 23:41:17 GMT  
		Size: 28.0 MB (27959200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e92527947bdcc341ab63777422e7409751516a8bc5ffc61040d76b72e7d58c`  
		Last Modified: Thu, 11 Jun 2026 00:23:14 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c52c9bd0c151ce908cf5e8c55694b4a321a916d3053e9e4cd3b06837e55f325`  
		Last Modified: Thu, 11 Jun 2026 00:23:14 GMT  
		Size: 144.2 KB (144156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ec2615dd4e79e84378f7223c9d7c70a6cdfb8835717c19cadbab17a726210d`  
		Last Modified: Thu, 11 Jun 2026 00:23:14 GMT  
		Size: 2.2 MB (2211763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4249a738c6e8e951ca0bf1608e335442f8f50ff9fe57a524b1bdb472e59ed1`  
		Last Modified: Thu, 11 Jun 2026 00:23:14 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab171fa641968acda113ed8ec0cbff5159a4895efed9c4e08bb6e466a40fb5ce`  
		Last Modified: Thu, 11 Jun 2026 00:23:15 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:a7356b3e73eada1ea16535f45e9a297b7913adfb103e9df5d0a2ee333c58f443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c75fc3f8c74e188d3585642b303189b73ae78c14b089bd14f0d37da2b085f25`

```dockerfile
```

-	Layers:
	-	`sha256:5a953398782781fbd31e5d1fb67c1cdeb82c91397fb27ce32b9d756cc938a03a`  
		Last Modified: Thu, 11 Jun 2026 00:23:14 GMT  
		Size: 2.0 MB (2011371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aeae6ddb09b0b52fdf1e1db9b67dfa04fba888fbba5c54b1b7e30ecbd56dafde`  
		Last Modified: Thu, 11 Jun 2026 00:23:14 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm variant v7

```console
$ docker pull memcached@sha256:7b20950329f422c7b322057fe1f944f98589cf937e5e65118b6d4bb241436ffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28513288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5d65e3287f7256814db41a73f2978df2252f6ac399369fe1a7a3eb1c4ceb3e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:21:55 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 11 Jun 2026 00:21:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:25:06 GMT
ENV MEMCACHED_VERSION=1.6.42
# Thu, 11 Jun 2026 00:25:06 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Thu, 11 Jun 2026 00:25:06 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Thu, 11 Jun 2026 00:25:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 11 Jun 2026 00:25:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:25:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 11 Jun 2026 00:25:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:25:06 GMT
USER memcache
# Thu, 11 Jun 2026 00:25:06 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 11 Jun 2026 00:25:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4bd6ddea06d5009ee47ddb0f254a2569aff0230c005869ebd416b20295d945c0`  
		Last Modified: Wed, 10 Jun 2026 23:42:34 GMT  
		Size: 26.2 MB (26211004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bcac116a5bd6f8c4ba910742373294134be4443587cce918db3492895262e16`  
		Last Modified: Thu, 11 Jun 2026 00:25:12 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af6a74cecf5734c352e3c2ea5fb348246cfe77549b6cb2afe3116aaf39983ff8`  
		Last Modified: Thu, 11 Jun 2026 00:25:12 GMT  
		Size: 135.4 KB (135382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6189c46b05f5cdb39083034f258358c5472cc6824a25a7dc8a8f60ae58891116`  
		Last Modified: Thu, 11 Jun 2026 00:25:12 GMT  
		Size: 2.2 MB (2165385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfeedbf1b9c25a3c29e32962704f935689b2b60c4096315dbee3365a9cec4dc0`  
		Last Modified: Thu, 11 Jun 2026 00:25:12 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0309704e28c847b1dd0249a490a5774838b3d27bf059481108e0f1a300efd4ae`  
		Last Modified: Thu, 11 Jun 2026 00:25:13 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:84793c5cdc418c73cc53c1dcdf3ebaf9d1c2a7910ec63c85d179a691e05f1ddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0981cd8d43f93fb996bbc87f0659a7c3a7163d74a5c84503eb77588ed240010c`

```dockerfile
```

-	Layers:
	-	`sha256:39acaedd56024e59130ae654692bdff06d01b71719567ede3d9ece539679150e`  
		Last Modified: Thu, 11 Jun 2026 00:25:13 GMT  
		Size: 2.0 MB (2009828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ada0017eed4fa0f3db9a2e1669d0eb74e2908e65a483af6819df971d18d767a`  
		Last Modified: Thu, 11 Jun 2026 00:25:12 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:a36eca5b5840c718ca41526a871fd751dc96965f182778a7631a0c2896c3f44a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32566560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31c7500da651c7c5945a2db8b00248c02ad2947b4eccb66b464759cd6f4ea2c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:23:08 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 11 Jun 2026 00:23:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:26:08 GMT
ENV MEMCACHED_VERSION=1.6.42
# Thu, 11 Jun 2026 00:26:08 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Thu, 11 Jun 2026 00:26:08 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Thu, 11 Jun 2026 00:26:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 11 Jun 2026 00:26:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:26:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 11 Jun 2026 00:26:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:26:08 GMT
USER memcache
# Thu, 11 Jun 2026 00:26:08 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 11 Jun 2026 00:26:08 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb68ad832950ffa1d5fe24c7e7ee4e061b358d6bcb14dfdb1bb2dec4c557f7a2`  
		Last Modified: Thu, 11 Jun 2026 00:26:15 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f6f966199cad211cd492fc65c6c927fde3a05499bdd9a2112d65deb706cfbc6`  
		Last Modified: Thu, 11 Jun 2026 00:26:14 GMT  
		Size: 153.5 KB (153481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3314b48b94577865e96641c557d5048167254c141db1725db6a5b7a623b68f7b`  
		Last Modified: Thu, 11 Jun 2026 00:26:15 GMT  
		Size: 2.3 MB (2263038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e33e48bcfd48ec271ffa516b5c3b03458185abfb31596aca0b854e9c9367fb9`  
		Last Modified: Thu, 11 Jun 2026 00:26:15 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb41e83cd817b17ff4c2b62ce482681096f6783b2a32be0407cada277d4f293`  
		Last Modified: Thu, 11 Jun 2026 00:26:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:0253549da149222537eeb2e51a1b411b7662c20d8c8964e71967cf670ce9c992
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af9894c8fa8e920a07bf631bed91c9b67398338986159408229a8da050b21c3b`

```dockerfile
```

-	Layers:
	-	`sha256:a11c09037e68845f3c8c01efb996710c3b2d21ba868a98c3ba2582a28d0f1047`  
		Last Modified: Thu, 11 Jun 2026 00:26:15 GMT  
		Size: 2.0 MB (2008676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40468c38b6f60c4625c352d5bdc83ea61510da0efeb2542777603da191a5d2fa`  
		Last Modified: Thu, 11 Jun 2026 00:26:14 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; 386

```console
$ docker pull memcached@sha256:e134667b3198bc9f05962d9bb97cf359ab04c31cb8d11c75e2683de54cebd46e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33675616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cba4eb3d3e82545273aa5ff6f0e6f7bf2b1240176b9489d2315fcf290b9c49a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:18:22 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 11 Jun 2026 00:18:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:21:26 GMT
ENV MEMCACHED_VERSION=1.6.42
# Thu, 11 Jun 2026 00:21:26 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Thu, 11 Jun 2026 00:21:26 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Thu, 11 Jun 2026 00:21:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 11 Jun 2026 00:21:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:21:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 11 Jun 2026 00:21:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:21:26 GMT
USER memcache
# Thu, 11 Jun 2026 00:21:26 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 11 Jun 2026 00:21:26 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:720f951a68f4f9ab464e52b53cf88cfb86bc876b3f00956d000420777ab93c0c`  
		Last Modified: Wed, 10 Jun 2026 23:40:30 GMT  
		Size: 31.3 MB (31301194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2607fca8a1b7fbebf74214d1b33f4f0a54aed5fef2bed18ddc89836a7d00e04b`  
		Last Modified: Thu, 11 Jun 2026 00:21:31 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4620fc98d601bc463a1a505fb0ecf42cb42fa76088d5e80dee41474c74f39f1`  
		Last Modified: Thu, 11 Jun 2026 00:21:32 GMT  
		Size: 147.5 KB (147511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a4c97894b05376111399fa19e7429f36d493cb528c53cb81318a2920d5a954`  
		Last Modified: Thu, 11 Jun 2026 00:21:32 GMT  
		Size: 2.2 MB (2225398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f4a764af02d7ba61dd0909ddb429ba92c9a367243a225936fd625fda113340`  
		Last Modified: Thu, 11 Jun 2026 00:21:32 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52e82109e627ebc0d88a9f7c357b97f14b8ac06bdab5d0b6aa50c3b958a13a8`  
		Last Modified: Thu, 11 Jun 2026 00:21:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:6670b6485b54bcae32ddeda5c2d1764d0ee2066f036d0c17f2cc89734f0be8c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d0aef4dacfecea9e8dbc20498736f77e48bf5106eb60bcfa08c1e81a5c4f06c`

```dockerfile
```

-	Layers:
	-	`sha256:0ebdf5fe0d474785e4448d36043967631fb650ec7b52bd865126a7360978a2ea`  
		Last Modified: Thu, 11 Jun 2026 00:21:32 GMT  
		Size: 2.0 MB (2005525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f257ddeb15df7a03d8e7bb57e01531d894c998af32f33cb528199914bd8f6e1c`  
		Last Modified: Thu, 11 Jun 2026 00:21:32 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; ppc64le

```console
$ docker pull memcached@sha256:25e41a95392ee3c63e35711fec0648fbedc92c6be718456ad8fb89ab66f4e825
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36762178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a04e55188a4c60d5cd8eb00b50628fd87658d0d1814097b40417d71b18479e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 02:36:51 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 11 Jun 2026 02:36:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:59:49 GMT
ENV MEMCACHED_VERSION=1.6.42
# Thu, 11 Jun 2026 02:59:49 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Thu, 11 Jun 2026 02:59:49 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Thu, 11 Jun 2026 02:59:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 11 Jun 2026 02:59:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 02:59:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 11 Jun 2026 02:59:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 02:59:50 GMT
USER memcache
# Thu, 11 Jun 2026 02:59:50 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 11 Jun 2026 02:59:50 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9d6b2e320e2b74843186d830e8202c50ebfaeccf823d239e3e3e349a8a508d80`  
		Last Modified: Thu, 11 Jun 2026 00:24:42 GMT  
		Size: 33.6 MB (33606340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d389c79e93b7c7b3cc2a8226edeb6460d8101e245642213048c1a187d08a935d`  
		Last Modified: Thu, 11 Jun 2026 03:00:07 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7bb22e37f822a0e94fa24cd439d7666c214637b0d59c384dd19e12674c74a82`  
		Last Modified: Thu, 11 Jun 2026 03:00:07 GMT  
		Size: 170.4 KB (170363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82cbb5c5e79cdcec98bd562e1a62768994b805ff7d805b6b75b5bf0e349cff8`  
		Last Modified: Thu, 11 Jun 2026 03:00:06 GMT  
		Size: 3.0 MB (2983963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e60c6f3b8886967bbbabece38cfe74eccdfde98cdae42045a33c5b2b29fd6da`  
		Last Modified: Thu, 11 Jun 2026 03:00:08 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc87d370da3b9877481bf9620bda982328b4d722812ec3e77a7b4c50d016eb33`  
		Last Modified: Thu, 11 Jun 2026 03:00:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:0101df893b4af64daa7ee54d012d7b8682b6c1a9ad1d85700cf8ff269664b19e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b06e6f43b0b95c657fb0043338f12918e63fcac640df48783c49ac29092afb0b`

```dockerfile
```

-	Layers:
	-	`sha256:8ed9fcb43f9f08fb8702ae2709d918b6370866fb4697ddf04b93f42080b23d94`  
		Last Modified: Thu, 11 Jun 2026 03:00:08 GMT  
		Size: 2.0 MB (2011969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c6915dddb9ee13a9cd4156b07c521335c76c9687dcb3a08e66e147af9d99453`  
		Last Modified: Thu, 11 Jun 2026 03:00:06 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; riscv64

```console
$ docker pull memcached@sha256:918c03d1a36c36f13b67e3fbf100f93adad50fbbb452fecc3769db0b8cde487c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30626726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1c8f5f48c37fb2ef15e785c080f746aec65afab782672de8b6a63bd88942e41`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1781049600'
# Fri, 12 Jun 2026 00:28:54 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 12 Jun 2026 00:29:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jun 2026 00:42:57 GMT
ENV MEMCACHED_VERSION=1.6.42
# Fri, 12 Jun 2026 00:42:57 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Fri, 12 Jun 2026 00:42:57 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Fri, 12 Jun 2026 00:42:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 12 Jun 2026 00:42:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Jun 2026 00:42:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 12 Jun 2026 00:42:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2026 00:42:57 GMT
USER memcache
# Fri, 12 Jun 2026 00:42:57 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 12 Jun 2026 00:42:57 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0b510fe8545cab831b696965b5a825649c5c945581e912d31a08a0b30ff940c0`  
		Last Modified: Thu, 11 Jun 2026 03:01:06 GMT  
		Size: 28.3 MB (28282305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35e7a152e660b7a61f448299ac325c28198a870bc53d54cd2584d111c3cef30`  
		Last Modified: Fri, 12 Jun 2026 00:43:44 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d26b2af070be1166e165d4bd1eb073a685622ddb1edb5cf4382cb7825faa21a`  
		Last Modified: Fri, 12 Jun 2026 00:43:44 GMT  
		Size: 133.1 KB (133071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ac4d08e6c19ea726574dc4cd56f4d39216f427cdfd9d6e19c91b06583e6630`  
		Last Modified: Fri, 12 Jun 2026 00:43:44 GMT  
		Size: 2.2 MB (2209833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:039ac44117911671ad0fca8638fa93282ad5865273a55e1328d3180ac5c4f463`  
		Last Modified: Fri, 12 Jun 2026 00:43:44 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65787f51c4d435ccf6c4c9c11e27fe642bd5af3fdd4489e11005614f51c21c29`  
		Last Modified: Fri, 12 Jun 2026 00:43:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:5db8b7d0f9f634b02f9f4dfb45d2f0d3fb2ef1778c3e52058327cd5dec31ebce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0de6ff12136279a3005dae5ce29967a780efb19d8a50b71f33b8153d38859c49`

```dockerfile
```

-	Layers:
	-	`sha256:256f6cfcbc556a40776a58fddd91ccacf0870ab5955a42e7e3ea23601ff76633`  
		Last Modified: Fri, 12 Jun 2026 00:43:44 GMT  
		Size: 2.0 MB (2002332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdfa564b06be9c36a9d81da00994136c858ca65d81762277469168a418a9c9fa`  
		Last Modified: Fri, 12 Jun 2026 00:43:44 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; s390x

```console
$ docker pull memcached@sha256:75f4e343898a5a326a82f6560f0efdd5d11c5aea7a710327cdfd400ac3244341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32291904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd9e841717be4c79746136574299d1a6552f88fe8566606318efb07377ef20c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:19:32 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 11 Jun 2026 00:19:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:22:55 GMT
ENV MEMCACHED_VERSION=1.6.42
# Thu, 11 Jun 2026 00:22:55 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Thu, 11 Jun 2026 00:22:55 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Thu, 11 Jun 2026 00:22:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 11 Jun 2026 00:22:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:22:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 11 Jun 2026 00:22:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:22:55 GMT
USER memcache
# Thu, 11 Jun 2026 00:22:55 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 11 Jun 2026 00:22:55 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:760dcf74fdfe93300ce15b5b23adf9aa4af45b6ba9d69925863198f64881a537`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 29.9 MB (29851354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159eeccf7c6aa583901267e3c00bf9c124c32be82a1074722d2be0b547fee632`  
		Last Modified: Thu, 11 Jun 2026 00:23:05 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d08bb26724ea31dfaf95eb6c1647b7686671b3869632300d6056a05c3532bd`  
		Last Modified: Thu, 11 Jun 2026 00:23:05 GMT  
		Size: 140.5 KB (140545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b341a8e7ca68a391e79c556246f3f0b81e4a5e747fed517e274d78f49faa30`  
		Last Modified: Thu, 11 Jun 2026 00:23:05 GMT  
		Size: 2.3 MB (2298492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff1b1dd9080cb995308882030f9579f4c5bf2af5b26b7270d6682de75f6e6d5`  
		Last Modified: Thu, 11 Jun 2026 00:23:05 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075343c77f8c8b9a1bb9fe079e853c0e4628b60f1fff7d8dce82d38c3a344bf8`  
		Last Modified: Thu, 11 Jun 2026 00:23:06 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:1f977b6725f519f48d75ffc92c711df863d7c0e4a1d1f0c5a5bc6605533f35e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1104b534613c8d2cc0544b9adf96821b4f7f623262ef6ddc425f13fa94427850`

```dockerfile
```

-	Layers:
	-	`sha256:66bb879abbe8f943d53561fcf4f4262e1b78fb31b6aa3fdac560ffdc45e3d4b5`  
		Last Modified: Thu, 11 Jun 2026 00:23:05 GMT  
		Size: 2.0 MB (2009805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e448bf5a0443ce0296756453f8bca10e0ec97ebc01576de74a28f60b78299f2b`  
		Last Modified: Thu, 11 Jun 2026 00:23:05 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine`

```console
$ docker pull memcached@sha256:7381333da6d6ae06e02d8dfc87ee6f2c7cd0a19f7ba048d5efc538d2100e2208
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
$ docker pull memcached@sha256:ce375dd48f976d33bf35beb966cc37f202fd840a90891e58b9e71171fc74174d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5921579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19d284e7a8445d8dc70e97c673a8a0175d18f39d5336ccbdfa8b240c0ef3ce4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:29 GMT
ADD alpine-minirootfs-3.24.1-x86_64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:15:18 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:15:18 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:17:54 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:17:54 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:17:54 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:17:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:17:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:17:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:17:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:17:54 GMT
USER memcache
# Tue, 16 Jun 2026 00:17:54 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:17:54 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:55afa1ecc21d2bb5e5045f32dafee56272ffd89860bac26f6c32123439af26a4`  
		Last Modified: Sun, 14 Jun 2026 06:44:06 GMT  
		Size: 3.8 MB (3846391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb73756dcbbebc424eab53d3adda4d9f64001e7a91272a7b2a834622c08b093`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f0d6a5291334f2b54ec652193cd4e17ee22455b2f3ff3bd9b66acff6436c7b`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 106.1 KB (106066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ac11a8307528096ac745e0ef681b64854bbd012ffdfbce85587153eec73563`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 2.0 MB (1967772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3626493aad85d70a212bc66e9d45db8aef43b4bc662259563f916398165f1e64`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cdcd3f20e3aa439838f5491e6f457a42bad6c80ed9b099313bf79b57a721ea8`  
		Last Modified: Tue, 16 Jun 2026 00:18:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:bb948800301f1cae8e18e317f2b9e85636c86c4a1924ee85e125da37cb1333e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c3e084937eb543038244e151b03b8d9a0dce0b4d5bf87c2d471fa397ed5702`

```dockerfile
```

-	Layers:
	-	`sha256:9d05a792212c92363a76bb6a8205a6e7f386113b3efc1b5d600f93d4e237c975`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 94.9 KB (94897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee0e7e70ef03205f55c68bc1b74ac7854183aee4e871112794975dc852761b19`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:4b144cdbc67c11035b3d0f0c812b590ee694977f2f6a32321e538237bd2f841c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5573158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e9bb70df1535a2f8ca960f733a4404cbde900a13156a1f4446c2fd110258e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:25 GMT
ADD alpine-minirootfs-3.24.1-armhf.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:25 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:14:43 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:14:44 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:17:47 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:17:47 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:17:47 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:17:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:17:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:17:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:17:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:17:47 GMT
USER memcache
# Tue, 16 Jun 2026 00:17:47 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:17:47 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3c4836a46d600cfe9a422adf7a80205cb534097e6213325e0176c51f6e5cc02e`  
		Last Modified: Sun, 14 Jun 2026 06:44:57 GMT  
		Size: 3.6 MB (3553450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e732a60042adf5cff5fe4fe0de83f937f6e5c8896500f7023e8bf68ed0670d65`  
		Last Modified: Tue, 16 Jun 2026 00:17:51 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad86d1fea29db061a5ae896a0a595b144edcdb4af59deac2b75b0fb8f5fa2d4c`  
		Last Modified: Tue, 16 Jun 2026 00:17:50 GMT  
		Size: 102.6 KB (102624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f26dd2445dbf4d5624417ca290f5ae2e5774fa7fec4f5655cd2377ee3147e4`  
		Last Modified: Tue, 16 Jun 2026 00:17:51 GMT  
		Size: 1.9 MB (1915730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080a186f0ca6beb06a5ce4a86fbc71f5b9995713fcc899c73f995f251ef7c987`  
		Last Modified: Tue, 16 Jun 2026 00:17:51 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c4d4f455f9a2b633cca28e3aa2190e4c42ca83ca6e3ea88ea4abe16944d238`  
		Last Modified: Tue, 16 Jun 2026 00:17:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:d6b7abf6ef34abf12ab2c7f84bd29ac2461eb3271d1c4070456ed9b94e4b41a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43a767571287c8ca227e321ee8d65f9da82e558098bedbb15888434dcc1ce9fa`

```dockerfile
```

-	Layers:
	-	`sha256:1794ccef4392c0db4ba36ad7fde22cdacbda40f4d56f0adbef802163c87e066c`  
		Last Modified: Tue, 16 Jun 2026 00:17:51 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:848c5e0ced69b802cca72c23bec05a4c6f23136212a4a1d5cc22b7c8f0154bf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:286f62a53a8947036e39f2b79567b31d38309fd84c7a39e43de8c5f9817a2f64`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:26 GMT
ADD alpine-minirootfs-3.24.1-armv7.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:26 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:17:59 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:17:59 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:20:56 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:20:56 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:20:56 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:20:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:20:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:20:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:20:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:20:56 GMT
USER memcache
# Tue, 16 Jun 2026 00:20:56 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:20:56 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bc03a9e5b4dd452551f246e199537fe7afc1765f53f510bc81d26df9845e4008`  
		Last Modified: Sun, 14 Jun 2026 06:45:22 GMT  
		Size: 3.3 MB (3260615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f0249bacfc8953b72899bf7b6c904c8750482fce4c93108f57b2c64228b279`  
		Last Modified: Tue, 16 Jun 2026 00:21:00 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95e1b321ffc31d01e766d5d1d054967d613940563406fc54ee981926b7f6049`  
		Last Modified: Tue, 16 Jun 2026 00:21:01 GMT  
		Size: 92.4 KB (92366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce112e60c1b15077277c233a7707831818dff0a15f1fc977ebebc93f817dad43`  
		Last Modified: Tue, 16 Jun 2026 00:21:01 GMT  
		Size: 1.9 MB (1875183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32fa6ed5b14fd6fcf96a7cde2996063f10b8efe802c386479288a232af826027`  
		Last Modified: Tue, 16 Jun 2026 00:21:01 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6648f8180a4eea1f5197f2fa2d356fbbf4e5f65345e189e720e227af64a5e31`  
		Last Modified: Tue, 16 Jun 2026 00:21:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:59387f31eff7cfb3166c5e6d4bad92e255705affcc15c84c4a06c86ecb1a9890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:174eb460b1df4523a4f71ba5a996f2285fa845fe8ef76d2df3ea8c4962c6b6ca`

```dockerfile
```

-	Layers:
	-	`sha256:4ff5e70775e819cab551295c56b58fdb0c44c105cdc4f72247e3968accd2ab2f`  
		Last Modified: Tue, 16 Jun 2026 00:21:00 GMT  
		Size: 94.3 KB (94315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00f10e1301c7e61396658f7e3ed330e400a9f304c6a0323de8ff644aba987474`  
		Last Modified: Tue, 16 Jun 2026 00:21:01 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:33261748facce282dbe4dbb4d9f875139680fce4cefc13cb9ad8e1ced23f9557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6250475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1614bb2865c8f849c2bc5bf77703a1ab711695c607a8bc6edb013a076ec16d6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:20 GMT
ADD alpine-minirootfs-3.24.1-aarch64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:20 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:13:18 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:13:18 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:16:06 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:16:06 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:16:06 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:16:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:16:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:16:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:16:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:16:06 GMT
USER memcache
# Tue, 16 Jun 2026 00:16:06 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:16:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5de55e5ef9c033997441461efe7ba23a986db059c0bb78b38f84ee0d72b99167`  
		Last Modified: Sun, 14 Jun 2026 06:44:31 GMT  
		Size: 4.2 MB (4183037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5faa19f06c4d5e26332739c7f08fd3dcd2c81817471c62029a6d99af6be8748`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377a35d28f00766e2679c788b95b0a67b9aa5a76c8ef701a2a9604e2a00c3b46`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 121.8 KB (121841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0b819e89558d70f1401ca58cbc19c58ae13e15be8184fd9b2733e022f318a4`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 1.9 MB (1944247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca539cef48ff8c3f723ab23506b6786c9ed26a9cac713601b71de2dc775d26a`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c4c456deed244daa6d7076f40a1cf0364d294059bb43e533677a89027843b15`  
		Last Modified: Tue, 16 Jun 2026 00:16:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:4d25960abc53b5ba1896b8f5ee04ba5ac1389900ab9b413eb62285af7281aedb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d1a4b7ad428a08c8a174d5ecd9763d530e849f54a2d9b90aef934e54b9477d4`

```dockerfile
```

-	Layers:
	-	`sha256:9c0a8e5e07390fae6abe9204450009671011c4d2d5aa5fe4afdd82324fdb49b9`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 94.4 KB (94351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ee01158358d01c082867cf46a5225cf101013e4d5b7eae18fc7853e277ff0f4`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 20.7 KB (20727 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; 386

```console
$ docker pull memcached@sha256:5436d0ef6e12f2f8e454384ff4a703132b3fe820c41a55336f520bb5d1622574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5702329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8946be3d97c7b9825159f58cbf832b131c75cb90b3fb46a40d5429b9ffe32bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:19 GMT
ADD alpine-minirootfs-3.24.1-x86.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:19 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:13:59 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:13:59 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:16:45 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:16:45 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:16:45 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:16:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:16:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:16:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:16:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:16:46 GMT
USER memcache
# Tue, 16 Jun 2026 00:16:46 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:16:46 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f86df9d778509895efbf9363d8fcb0cbe0b772de536c7218e4c4c947f0be879f`  
		Last Modified: Sun, 14 Jun 2026 06:45:46 GMT  
		Size: 3.7 MB (3670141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043137360442e605bc150f28f20e1fa2d23d90131370bc405ad7d35309594491`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900ce6eeaece12033b12f1c8641c33dcf62ff2525584411911368cfcd0b38224`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 110.7 KB (110729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e8cc1c8f6bc6391eb1a43a46f0b55ca7845f824fc0f2fc7ae7587a7715814e`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 1.9 MB (1920111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d94f6e4d3be92188fc182a3557fe43af5bc9f3e768a7f265977743a56eea527e`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f8a19f18dfff271426de7a17ab6780788fa4345d5fa0120e6d03720d552bd4`  
		Last Modified: Tue, 16 Jun 2026 00:16:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:00dc6a7f29b7f2f5ac46fc5678b80c43c7b1e46b4ca3c84c5597034180aeb644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6de04019c7775544db9adbb4c4558d0e7c842c279e5d70532b2ac0b988ac1345`

```dockerfile
```

-	Layers:
	-	`sha256:80895f8f5e9c9b015e419096426322f4c86c33d55ca8860ee046b61d52782847`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 94.9 KB (94852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c69be8c1f82a066b46cc389712508e85c1dcd77e649c922dba46ace64b343ae`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:c7857941a51b85b136781035703afcc8854a2d70fa2091208a51f8bb7e71f934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5998515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b02b2222212c64e444ac1a2227b19f0cfb1282c8a8ced386c1b79ae48c641b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:15 GMT
ADD alpine-minirootfs-3.24.1-ppc64le.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:15 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:15:37 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:15:38 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:18:22 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:18:22 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:18:22 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:18:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:18:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:18:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:18:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:18:22 GMT
USER memcache
# Tue, 16 Jun 2026 00:18:22 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:18:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3ebcdcd395ccee658b9200e4b27d7699e5d6ed9f6c1858dea12781aac519ff59`  
		Last Modified: Sun, 14 Jun 2026 06:46:36 GMT  
		Size: 3.8 MB (3813400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b108e2058722fb0fb5a9310e8ebe82ab4b9c021228a94b3125ba49d318e9667`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb8160ed736eda8513164d5d703082fb0c9af9e037472ab70a02579caa3eb99`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 126.3 KB (126252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5cb88dd03ce07ecf1613c2aff220fb392763d8f22edc900c4ad032ee7103d34`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 2.1 MB (2057508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a12fd57420ca797ab383c58a488044d324c4d43b3c94a848f86a0524ed3064b4`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1c0c7b7a77e9375d8a75fb825fa274d9127ca96de79107550517be29501c817`  
		Last Modified: Tue, 16 Jun 2026 00:18:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:851f463d4778539d5e4981f972420f9a57ec2559488f8a59fba6abab6065032f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:734dd3d91f2d6cf217233f7a9dacc3c20ff0590246adb790f95713fb21c115de`

```dockerfile
```

-	Layers:
	-	`sha256:c0d4c203ef9f66cf827ec62098d7801e1c49f1187e0fe047fd32fc2a3271f636`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 94.3 KB (94304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b734d170b5463fa77dd77072e06d51a28efe59a53600d47435b015ebcadae92`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:ba5bf40b4adc1fe04f32e2e239fa9c0020d4e89bf4079493f8bc11a92c8f4b51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5738070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d12fbf86d6880aaa9d517425d9cecddcf545ba87e577a039dea9ea99ad53d8a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 05:59:15 GMT
ADD alpine-minirootfs-3.24.1-riscv64.tar.gz / # buildkit
# Tue, 16 Jun 2026 05:59:15 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 08:28:27 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 19 Jun 2026 08:28:31 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 19 Jun 2026 08:41:52 GMT
ENV MEMCACHED_VERSION=1.6.42
# Fri, 19 Jun 2026 08:41:52 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Fri, 19 Jun 2026 08:41:52 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Fri, 19 Jun 2026 08:41:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 19 Jun 2026 08:41:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 08:41:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 19 Jun 2026 08:41:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 08:41:53 GMT
USER memcache
# Fri, 19 Jun 2026 08:41:53 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 19 Jun 2026 08:41:53 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c34e5222b29b86391cdae95b0473ef789493ff1a0068a3a30b5d66f544bd7cf6`  
		Last Modified: Sun, 14 Jun 2026 06:47:00 GMT  
		Size: 3.6 MB (3574358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e09d95a0f414638430c0cd3ecfdcce75606201917a27c7cb2ce1e34cb928b26a`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a5335c7af79a1b08af55862ba77644afdae5544d9a7871e45c91b364bd4f71d`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 108.9 KB (108888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3622a6ea71515db1ef566afdbb121daed1f408aacf1519f4173b40dabe2ae627`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 2.1 MB (2053467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1db0e3e31ca3f2830f5404436e92b1862a4078adefacacec09a9580a3ad0a2`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1463b0fd26a37659aaad7f99696e5213764ad03bb094f40836c3309713d7a60`  
		Last Modified: Fri, 19 Jun 2026 08:42:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:aadb3b9338400b87692f95e00931e43940f8d6ddd13f046bd256848dd825e458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bde4b5a4a468d795a5f58dd934b371adfe72cd2ae24e166e1258ad65aa455a56`

```dockerfile
```

-	Layers:
	-	`sha256:debb70180cf674562f7ca321270e3dfa350c5d1596c05dbfcc27b38c65652528`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 94.3 KB (94300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a895bbe0bfec24678c1c92ddd283cb7392e0e8d229f31c769a23c95224c0d371`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:e1b640e8d192055e5c3ccd05b077776a0f4d35664191596f7a8230b2cd7ef0f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5823313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1ef6221f9c2854683b0633325a98a0e7a0d3b7d865b02d7cdf4c1d49d2e5090`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:21 GMT
ADD alpine-minirootfs-3.24.1-s390x.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:21 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:13:46 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:13:46 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:17:12 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:17:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:17:12 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:17:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:17:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:17:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:17:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:17:12 GMT
USER memcache
# Tue, 16 Jun 2026 00:17:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:17:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:da43be6afaaa3ec1b607461ce64380942a6d76c3d52cda4337b0770d9a96fa89`  
		Last Modified: Sun, 14 Jun 2026 06:47:25 GMT  
		Size: 3.7 MB (3709320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757d04238e02c9bbe1cfd4030cc19e29421650a1b1562a8ca4090d90e9ae17b0`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1949e0fa71fc91bebf4f2e4293108b27de8357d98f98b673bc4f3ed1980b52c`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 114.3 KB (114289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f0e22966bce79fbc8a20f7c27aa07ce63229bb50181319c810ca29f1fb4032`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 2.0 MB (1998350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15eb5e912ef8ec6e3abe76c361cdddb568d20a60be21be379d4d8d7d0ebaa11e`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a549d59ad0d4761ac6f4cca272c4bea521471ed091d0e79143bfda8ff29cf9ce`  
		Last Modified: Tue, 16 Jun 2026 00:17:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:6dbf7c8a98f02a949769403ad1c92583b34a28dccc66b7d83d91863785a6dad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a89d23372d19daf2d6d4e1c4de732f7864316ed5e7713b1103918303873683e`

```dockerfile
```

-	Layers:
	-	`sha256:099ab2d711ef73783b01895824a4664c7d65e2a333e81237b4766cf053a8f6f0`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 94.2 KB (94246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0eccbabf44891af00e622624c5cfd5a295656f82f1c15073b240ac34d47af96c`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine3.24`

```console
$ docker pull memcached@sha256:7381333da6d6ae06e02d8dfc87ee6f2c7cd0a19f7ba048d5efc538d2100e2208
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

### `memcached:1.6-alpine3.24` - linux; amd64

```console
$ docker pull memcached@sha256:ce375dd48f976d33bf35beb966cc37f202fd840a90891e58b9e71171fc74174d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5921579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19d284e7a8445d8dc70e97c673a8a0175d18f39d5336ccbdfa8b240c0ef3ce4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:29 GMT
ADD alpine-minirootfs-3.24.1-x86_64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:15:18 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:15:18 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:17:54 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:17:54 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:17:54 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:17:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:17:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:17:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:17:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:17:54 GMT
USER memcache
# Tue, 16 Jun 2026 00:17:54 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:17:54 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:55afa1ecc21d2bb5e5045f32dafee56272ffd89860bac26f6c32123439af26a4`  
		Last Modified: Sun, 14 Jun 2026 06:44:06 GMT  
		Size: 3.8 MB (3846391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb73756dcbbebc424eab53d3adda4d9f64001e7a91272a7b2a834622c08b093`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f0d6a5291334f2b54ec652193cd4e17ee22455b2f3ff3bd9b66acff6436c7b`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 106.1 KB (106066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ac11a8307528096ac745e0ef681b64854bbd012ffdfbce85587153eec73563`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 2.0 MB (1967772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3626493aad85d70a212bc66e9d45db8aef43b4bc662259563f916398165f1e64`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cdcd3f20e3aa439838f5491e6f457a42bad6c80ed9b099313bf79b57a721ea8`  
		Last Modified: Tue, 16 Jun 2026 00:18:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:bb948800301f1cae8e18e317f2b9e85636c86c4a1924ee85e125da37cb1333e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c3e084937eb543038244e151b03b8d9a0dce0b4d5bf87c2d471fa397ed5702`

```dockerfile
```

-	Layers:
	-	`sha256:9d05a792212c92363a76bb6a8205a6e7f386113b3efc1b5d600f93d4e237c975`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 94.9 KB (94897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee0e7e70ef03205f55c68bc1b74ac7854183aee4e871112794975dc852761b19`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.24` - linux; arm variant v6

```console
$ docker pull memcached@sha256:4b144cdbc67c11035b3d0f0c812b590ee694977f2f6a32321e538237bd2f841c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5573158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e9bb70df1535a2f8ca960f733a4404cbde900a13156a1f4446c2fd110258e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:25 GMT
ADD alpine-minirootfs-3.24.1-armhf.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:25 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:14:43 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:14:44 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:17:47 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:17:47 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:17:47 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:17:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:17:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:17:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:17:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:17:47 GMT
USER memcache
# Tue, 16 Jun 2026 00:17:47 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:17:47 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3c4836a46d600cfe9a422adf7a80205cb534097e6213325e0176c51f6e5cc02e`  
		Last Modified: Sun, 14 Jun 2026 06:44:57 GMT  
		Size: 3.6 MB (3553450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e732a60042adf5cff5fe4fe0de83f937f6e5c8896500f7023e8bf68ed0670d65`  
		Last Modified: Tue, 16 Jun 2026 00:17:51 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad86d1fea29db061a5ae896a0a595b144edcdb4af59deac2b75b0fb8f5fa2d4c`  
		Last Modified: Tue, 16 Jun 2026 00:17:50 GMT  
		Size: 102.6 KB (102624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f26dd2445dbf4d5624417ca290f5ae2e5774fa7fec4f5655cd2377ee3147e4`  
		Last Modified: Tue, 16 Jun 2026 00:17:51 GMT  
		Size: 1.9 MB (1915730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080a186f0ca6beb06a5ce4a86fbc71f5b9995713fcc899c73f995f251ef7c987`  
		Last Modified: Tue, 16 Jun 2026 00:17:51 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c4d4f455f9a2b633cca28e3aa2190e4c42ca83ca6e3ea88ea4abe16944d238`  
		Last Modified: Tue, 16 Jun 2026 00:17:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:d6b7abf6ef34abf12ab2c7f84bd29ac2461eb3271d1c4070456ed9b94e4b41a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43a767571287c8ca227e321ee8d65f9da82e558098bedbb15888434dcc1ce9fa`

```dockerfile
```

-	Layers:
	-	`sha256:1794ccef4392c0db4ba36ad7fde22cdacbda40f4d56f0adbef802163c87e066c`  
		Last Modified: Tue, 16 Jun 2026 00:17:51 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.24` - linux; arm variant v7

```console
$ docker pull memcached@sha256:848c5e0ced69b802cca72c23bec05a4c6f23136212a4a1d5cc22b7c8f0154bf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:286f62a53a8947036e39f2b79567b31d38309fd84c7a39e43de8c5f9817a2f64`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:26 GMT
ADD alpine-minirootfs-3.24.1-armv7.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:26 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:17:59 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:17:59 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:20:56 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:20:56 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:20:56 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:20:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:20:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:20:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:20:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:20:56 GMT
USER memcache
# Tue, 16 Jun 2026 00:20:56 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:20:56 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bc03a9e5b4dd452551f246e199537fe7afc1765f53f510bc81d26df9845e4008`  
		Last Modified: Sun, 14 Jun 2026 06:45:22 GMT  
		Size: 3.3 MB (3260615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f0249bacfc8953b72899bf7b6c904c8750482fce4c93108f57b2c64228b279`  
		Last Modified: Tue, 16 Jun 2026 00:21:00 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95e1b321ffc31d01e766d5d1d054967d613940563406fc54ee981926b7f6049`  
		Last Modified: Tue, 16 Jun 2026 00:21:01 GMT  
		Size: 92.4 KB (92366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce112e60c1b15077277c233a7707831818dff0a15f1fc977ebebc93f817dad43`  
		Last Modified: Tue, 16 Jun 2026 00:21:01 GMT  
		Size: 1.9 MB (1875183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32fa6ed5b14fd6fcf96a7cde2996063f10b8efe802c386479288a232af826027`  
		Last Modified: Tue, 16 Jun 2026 00:21:01 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6648f8180a4eea1f5197f2fa2d356fbbf4e5f65345e189e720e227af64a5e31`  
		Last Modified: Tue, 16 Jun 2026 00:21:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:59387f31eff7cfb3166c5e6d4bad92e255705affcc15c84c4a06c86ecb1a9890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:174eb460b1df4523a4f71ba5a996f2285fa845fe8ef76d2df3ea8c4962c6b6ca`

```dockerfile
```

-	Layers:
	-	`sha256:4ff5e70775e819cab551295c56b58fdb0c44c105cdc4f72247e3968accd2ab2f`  
		Last Modified: Tue, 16 Jun 2026 00:21:00 GMT  
		Size: 94.3 KB (94315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00f10e1301c7e61396658f7e3ed330e400a9f304c6a0323de8ff644aba987474`  
		Last Modified: Tue, 16 Jun 2026 00:21:01 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.24` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:33261748facce282dbe4dbb4d9f875139680fce4cefc13cb9ad8e1ced23f9557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6250475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1614bb2865c8f849c2bc5bf77703a1ab711695c607a8bc6edb013a076ec16d6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:20 GMT
ADD alpine-minirootfs-3.24.1-aarch64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:20 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:13:18 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:13:18 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:16:06 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:16:06 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:16:06 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:16:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:16:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:16:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:16:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:16:06 GMT
USER memcache
# Tue, 16 Jun 2026 00:16:06 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:16:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5de55e5ef9c033997441461efe7ba23a986db059c0bb78b38f84ee0d72b99167`  
		Last Modified: Sun, 14 Jun 2026 06:44:31 GMT  
		Size: 4.2 MB (4183037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5faa19f06c4d5e26332739c7f08fd3dcd2c81817471c62029a6d99af6be8748`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377a35d28f00766e2679c788b95b0a67b9aa5a76c8ef701a2a9604e2a00c3b46`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 121.8 KB (121841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0b819e89558d70f1401ca58cbc19c58ae13e15be8184fd9b2733e022f318a4`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 1.9 MB (1944247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca539cef48ff8c3f723ab23506b6786c9ed26a9cac713601b71de2dc775d26a`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c4c456deed244daa6d7076f40a1cf0364d294059bb43e533677a89027843b15`  
		Last Modified: Tue, 16 Jun 2026 00:16:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:4d25960abc53b5ba1896b8f5ee04ba5ac1389900ab9b413eb62285af7281aedb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d1a4b7ad428a08c8a174d5ecd9763d530e849f54a2d9b90aef934e54b9477d4`

```dockerfile
```

-	Layers:
	-	`sha256:9c0a8e5e07390fae6abe9204450009671011c4d2d5aa5fe4afdd82324fdb49b9`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 94.4 KB (94351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ee01158358d01c082867cf46a5225cf101013e4d5b7eae18fc7853e277ff0f4`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 20.7 KB (20727 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.24` - linux; 386

```console
$ docker pull memcached@sha256:5436d0ef6e12f2f8e454384ff4a703132b3fe820c41a55336f520bb5d1622574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5702329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8946be3d97c7b9825159f58cbf832b131c75cb90b3fb46a40d5429b9ffe32bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:19 GMT
ADD alpine-minirootfs-3.24.1-x86.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:19 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:13:59 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:13:59 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:16:45 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:16:45 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:16:45 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:16:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:16:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:16:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:16:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:16:46 GMT
USER memcache
# Tue, 16 Jun 2026 00:16:46 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:16:46 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f86df9d778509895efbf9363d8fcb0cbe0b772de536c7218e4c4c947f0be879f`  
		Last Modified: Sun, 14 Jun 2026 06:45:46 GMT  
		Size: 3.7 MB (3670141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043137360442e605bc150f28f20e1fa2d23d90131370bc405ad7d35309594491`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900ce6eeaece12033b12f1c8641c33dcf62ff2525584411911368cfcd0b38224`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 110.7 KB (110729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e8cc1c8f6bc6391eb1a43a46f0b55ca7845f824fc0f2fc7ae7587a7715814e`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 1.9 MB (1920111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d94f6e4d3be92188fc182a3557fe43af5bc9f3e768a7f265977743a56eea527e`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f8a19f18dfff271426de7a17ab6780788fa4345d5fa0120e6d03720d552bd4`  
		Last Modified: Tue, 16 Jun 2026 00:16:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:00dc6a7f29b7f2f5ac46fc5678b80c43c7b1e46b4ca3c84c5597034180aeb644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6de04019c7775544db9adbb4c4558d0e7c842c279e5d70532b2ac0b988ac1345`

```dockerfile
```

-	Layers:
	-	`sha256:80895f8f5e9c9b015e419096426322f4c86c33d55ca8860ee046b61d52782847`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 94.9 KB (94852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c69be8c1f82a066b46cc389712508e85c1dcd77e649c922dba46ace64b343ae`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.24` - linux; ppc64le

```console
$ docker pull memcached@sha256:c7857941a51b85b136781035703afcc8854a2d70fa2091208a51f8bb7e71f934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5998515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b02b2222212c64e444ac1a2227b19f0cfb1282c8a8ced386c1b79ae48c641b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:15 GMT
ADD alpine-minirootfs-3.24.1-ppc64le.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:15 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:15:37 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:15:38 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:18:22 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:18:22 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:18:22 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:18:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:18:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:18:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:18:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:18:22 GMT
USER memcache
# Tue, 16 Jun 2026 00:18:22 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:18:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3ebcdcd395ccee658b9200e4b27d7699e5d6ed9f6c1858dea12781aac519ff59`  
		Last Modified: Sun, 14 Jun 2026 06:46:36 GMT  
		Size: 3.8 MB (3813400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b108e2058722fb0fb5a9310e8ebe82ab4b9c021228a94b3125ba49d318e9667`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb8160ed736eda8513164d5d703082fb0c9af9e037472ab70a02579caa3eb99`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 126.3 KB (126252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5cb88dd03ce07ecf1613c2aff220fb392763d8f22edc900c4ad032ee7103d34`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 2.1 MB (2057508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a12fd57420ca797ab383c58a488044d324c4d43b3c94a848f86a0524ed3064b4`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1c0c7b7a77e9375d8a75fb825fa274d9127ca96de79107550517be29501c817`  
		Last Modified: Tue, 16 Jun 2026 00:18:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:851f463d4778539d5e4981f972420f9a57ec2559488f8a59fba6abab6065032f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:734dd3d91f2d6cf217233f7a9dacc3c20ff0590246adb790f95713fb21c115de`

```dockerfile
```

-	Layers:
	-	`sha256:c0d4c203ef9f66cf827ec62098d7801e1c49f1187e0fe047fd32fc2a3271f636`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 94.3 KB (94304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b734d170b5463fa77dd77072e06d51a28efe59a53600d47435b015ebcadae92`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.24` - linux; riscv64

```console
$ docker pull memcached@sha256:ba5bf40b4adc1fe04f32e2e239fa9c0020d4e89bf4079493f8bc11a92c8f4b51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5738070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d12fbf86d6880aaa9d517425d9cecddcf545ba87e577a039dea9ea99ad53d8a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 05:59:15 GMT
ADD alpine-minirootfs-3.24.1-riscv64.tar.gz / # buildkit
# Tue, 16 Jun 2026 05:59:15 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 08:28:27 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 19 Jun 2026 08:28:31 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 19 Jun 2026 08:41:52 GMT
ENV MEMCACHED_VERSION=1.6.42
# Fri, 19 Jun 2026 08:41:52 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Fri, 19 Jun 2026 08:41:52 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Fri, 19 Jun 2026 08:41:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 19 Jun 2026 08:41:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 08:41:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 19 Jun 2026 08:41:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 08:41:53 GMT
USER memcache
# Fri, 19 Jun 2026 08:41:53 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 19 Jun 2026 08:41:53 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c34e5222b29b86391cdae95b0473ef789493ff1a0068a3a30b5d66f544bd7cf6`  
		Last Modified: Sun, 14 Jun 2026 06:47:00 GMT  
		Size: 3.6 MB (3574358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e09d95a0f414638430c0cd3ecfdcce75606201917a27c7cb2ce1e34cb928b26a`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a5335c7af79a1b08af55862ba77644afdae5544d9a7871e45c91b364bd4f71d`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 108.9 KB (108888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3622a6ea71515db1ef566afdbb121daed1f408aacf1519f4173b40dabe2ae627`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 2.1 MB (2053467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1db0e3e31ca3f2830f5404436e92b1862a4078adefacacec09a9580a3ad0a2`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1463b0fd26a37659aaad7f99696e5213764ad03bb094f40836c3309713d7a60`  
		Last Modified: Fri, 19 Jun 2026 08:42:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:aadb3b9338400b87692f95e00931e43940f8d6ddd13f046bd256848dd825e458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bde4b5a4a468d795a5f58dd934b371adfe72cd2ae24e166e1258ad65aa455a56`

```dockerfile
```

-	Layers:
	-	`sha256:debb70180cf674562f7ca321270e3dfa350c5d1596c05dbfcc27b38c65652528`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 94.3 KB (94300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a895bbe0bfec24678c1c92ddd283cb7392e0e8d229f31c769a23c95224c0d371`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.24` - linux; s390x

```console
$ docker pull memcached@sha256:e1b640e8d192055e5c3ccd05b077776a0f4d35664191596f7a8230b2cd7ef0f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5823313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1ef6221f9c2854683b0633325a98a0e7a0d3b7d865b02d7cdf4c1d49d2e5090`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:21 GMT
ADD alpine-minirootfs-3.24.1-s390x.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:21 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:13:46 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:13:46 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:17:12 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:17:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:17:12 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:17:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:17:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:17:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:17:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:17:12 GMT
USER memcache
# Tue, 16 Jun 2026 00:17:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:17:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:da43be6afaaa3ec1b607461ce64380942a6d76c3d52cda4337b0770d9a96fa89`  
		Last Modified: Sun, 14 Jun 2026 06:47:25 GMT  
		Size: 3.7 MB (3709320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757d04238e02c9bbe1cfd4030cc19e29421650a1b1562a8ca4090d90e9ae17b0`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1949e0fa71fc91bebf4f2e4293108b27de8357d98f98b673bc4f3ed1980b52c`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 114.3 KB (114289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f0e22966bce79fbc8a20f7c27aa07ce63229bb50181319c810ca29f1fb4032`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 2.0 MB (1998350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15eb5e912ef8ec6e3abe76c361cdddb568d20a60be21be379d4d8d7d0ebaa11e`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a549d59ad0d4761ac6f4cca272c4bea521471ed091d0e79143bfda8ff29cf9ce`  
		Last Modified: Tue, 16 Jun 2026 00:17:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:6dbf7c8a98f02a949769403ad1c92583b34a28dccc66b7d83d91863785a6dad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a89d23372d19daf2d6d4e1c4de732f7864316ed5e7713b1103918303873683e`

```dockerfile
```

-	Layers:
	-	`sha256:099ab2d711ef73783b01895824a4664c7d65e2a333e81237b4766cf053a8f6f0`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 94.2 KB (94246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0eccbabf44891af00e622624c5cfd5a295656f82f1c15073b240ac34d47af96c`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-trixie`

```console
$ docker pull memcached@sha256:85c0ab87f71b8b3ade708271177a8e5efca5e93c00287b6f25a2d74a27180bfa
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
$ docker pull memcached@sha256:09ac4118d89005e47ef3118221840c62f0fa909a2bee07ff571ae1ae59d9a79b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32204821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ad15119e1f73d99f3fbdc56187ea014f4fae2c8fcbe215c259f2fb2b387aefa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:23:00 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 11 Jun 2026 00:23:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:25:47 GMT
ENV MEMCACHED_VERSION=1.6.42
# Thu, 11 Jun 2026 00:25:47 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Thu, 11 Jun 2026 00:25:47 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Thu, 11 Jun 2026 00:25:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 11 Jun 2026 00:25:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:25:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 11 Jun 2026 00:25:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:25:47 GMT
USER memcache
# Thu, 11 Jun 2026 00:25:47 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 11 Jun 2026 00:25:47 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7883ff600bb4cc730c755ccb8be3f5a06371865abe00be70037283c04f4f3f5`  
		Last Modified: Thu, 11 Jun 2026 00:25:53 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d73a0d6b79b50aa2429aebc30b68c38fb0fb43a4a597ce0dd3936605fbb8912e`  
		Last Modified: Thu, 11 Jun 2026 00:25:53 GMT  
		Size: 136.7 KB (136685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5716730726452d6a54ff03d59c7dffbb7ed4f05836877734acf92f7a0512d6a9`  
		Last Modified: Thu, 11 Jun 2026 00:25:53 GMT  
		Size: 2.3 MB (2281206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f338318b7809e3c4be59b7eccaa1e5387cdbe8015c49eac3267097258c54ae89`  
		Last Modified: Thu, 11 Jun 2026 00:25:53 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ca13d7300d84ca43fcce2aa8304787015f83333e041c81c04796354eadce6b`  
		Last Modified: Thu, 11 Jun 2026 00:25:54 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:3d476e3ec28b0dda5046a3223b0e5a8c9ab8dec20bb294a8853da81d828c154d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e2358f67931681260618f406ea3e0032f17f7a82b2a7d36e5511e6413a7133f`

```dockerfile
```

-	Layers:
	-	`sha256:9cb94c17b8cb82e97f6ad217227fa08e25e0fdc9b96fd2fe418e0acc53911305`  
		Last Modified: Thu, 11 Jun 2026 00:25:53 GMT  
		Size: 2.0 MB (2008368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f8a18d24b8d75bd4b8d856878db21e4d4df7e3e553b9d72d0156bbe58c869d3`  
		Last Modified: Thu, 11 Jun 2026 00:25:53 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; arm variant v5

```console
$ docker pull memcached@sha256:f059b77d971253090e3862e28d374840935b5c06467230e9bea207fdb6ef3bf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30316631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c99754215fd2490daf10c8c1046bee3ab237e1e95bd4b46ef0610ca9d1c9badc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:19:47 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 11 Jun 2026 00:19:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:23:08 GMT
ENV MEMCACHED_VERSION=1.6.42
# Thu, 11 Jun 2026 00:23:08 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Thu, 11 Jun 2026 00:23:08 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Thu, 11 Jun 2026 00:23:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 11 Jun 2026 00:23:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:23:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 11 Jun 2026 00:23:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:23:08 GMT
USER memcache
# Thu, 11 Jun 2026 00:23:08 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 11 Jun 2026 00:23:08 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ed883f3fd95b7edef302d7ca9520eefdae280af081509bd7e9e5b5ff8f4cda7c`  
		Last Modified: Wed, 10 Jun 2026 23:41:17 GMT  
		Size: 28.0 MB (27959200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e92527947bdcc341ab63777422e7409751516a8bc5ffc61040d76b72e7d58c`  
		Last Modified: Thu, 11 Jun 2026 00:23:14 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c52c9bd0c151ce908cf5e8c55694b4a321a916d3053e9e4cd3b06837e55f325`  
		Last Modified: Thu, 11 Jun 2026 00:23:14 GMT  
		Size: 144.2 KB (144156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ec2615dd4e79e84378f7223c9d7c70a6cdfb8835717c19cadbab17a726210d`  
		Last Modified: Thu, 11 Jun 2026 00:23:14 GMT  
		Size: 2.2 MB (2211763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4249a738c6e8e951ca0bf1608e335442f8f50ff9fe57a524b1bdb472e59ed1`  
		Last Modified: Thu, 11 Jun 2026 00:23:14 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab171fa641968acda113ed8ec0cbff5159a4895efed9c4e08bb6e466a40fb5ce`  
		Last Modified: Thu, 11 Jun 2026 00:23:15 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:a7356b3e73eada1ea16535f45e9a297b7913adfb103e9df5d0a2ee333c58f443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c75fc3f8c74e188d3585642b303189b73ae78c14b089bd14f0d37da2b085f25`

```dockerfile
```

-	Layers:
	-	`sha256:5a953398782781fbd31e5d1fb67c1cdeb82c91397fb27ce32b9d756cc938a03a`  
		Last Modified: Thu, 11 Jun 2026 00:23:14 GMT  
		Size: 2.0 MB (2011371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aeae6ddb09b0b52fdf1e1db9b67dfa04fba888fbba5c54b1b7e30ecbd56dafde`  
		Last Modified: Thu, 11 Jun 2026 00:23:14 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; arm variant v7

```console
$ docker pull memcached@sha256:7b20950329f422c7b322057fe1f944f98589cf937e5e65118b6d4bb241436ffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28513288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5d65e3287f7256814db41a73f2978df2252f6ac399369fe1a7a3eb1c4ceb3e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:21:55 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 11 Jun 2026 00:21:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:25:06 GMT
ENV MEMCACHED_VERSION=1.6.42
# Thu, 11 Jun 2026 00:25:06 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Thu, 11 Jun 2026 00:25:06 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Thu, 11 Jun 2026 00:25:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 11 Jun 2026 00:25:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:25:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 11 Jun 2026 00:25:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:25:06 GMT
USER memcache
# Thu, 11 Jun 2026 00:25:06 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 11 Jun 2026 00:25:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4bd6ddea06d5009ee47ddb0f254a2569aff0230c005869ebd416b20295d945c0`  
		Last Modified: Wed, 10 Jun 2026 23:42:34 GMT  
		Size: 26.2 MB (26211004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bcac116a5bd6f8c4ba910742373294134be4443587cce918db3492895262e16`  
		Last Modified: Thu, 11 Jun 2026 00:25:12 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af6a74cecf5734c352e3c2ea5fb348246cfe77549b6cb2afe3116aaf39983ff8`  
		Last Modified: Thu, 11 Jun 2026 00:25:12 GMT  
		Size: 135.4 KB (135382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6189c46b05f5cdb39083034f258358c5472cc6824a25a7dc8a8f60ae58891116`  
		Last Modified: Thu, 11 Jun 2026 00:25:12 GMT  
		Size: 2.2 MB (2165385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfeedbf1b9c25a3c29e32962704f935689b2b60c4096315dbee3365a9cec4dc0`  
		Last Modified: Thu, 11 Jun 2026 00:25:12 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0309704e28c847b1dd0249a490a5774838b3d27bf059481108e0f1a300efd4ae`  
		Last Modified: Thu, 11 Jun 2026 00:25:13 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:84793c5cdc418c73cc53c1dcdf3ebaf9d1c2a7910ec63c85d179a691e05f1ddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0981cd8d43f93fb996bbc87f0659a7c3a7163d74a5c84503eb77588ed240010c`

```dockerfile
```

-	Layers:
	-	`sha256:39acaedd56024e59130ae654692bdff06d01b71719567ede3d9ece539679150e`  
		Last Modified: Thu, 11 Jun 2026 00:25:13 GMT  
		Size: 2.0 MB (2009828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ada0017eed4fa0f3db9a2e1669d0eb74e2908e65a483af6819df971d18d767a`  
		Last Modified: Thu, 11 Jun 2026 00:25:12 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:a36eca5b5840c718ca41526a871fd751dc96965f182778a7631a0c2896c3f44a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32566560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31c7500da651c7c5945a2db8b00248c02ad2947b4eccb66b464759cd6f4ea2c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:23:08 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 11 Jun 2026 00:23:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:26:08 GMT
ENV MEMCACHED_VERSION=1.6.42
# Thu, 11 Jun 2026 00:26:08 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Thu, 11 Jun 2026 00:26:08 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Thu, 11 Jun 2026 00:26:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 11 Jun 2026 00:26:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:26:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 11 Jun 2026 00:26:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:26:08 GMT
USER memcache
# Thu, 11 Jun 2026 00:26:08 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 11 Jun 2026 00:26:08 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb68ad832950ffa1d5fe24c7e7ee4e061b358d6bcb14dfdb1bb2dec4c557f7a2`  
		Last Modified: Thu, 11 Jun 2026 00:26:15 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f6f966199cad211cd492fc65c6c927fde3a05499bdd9a2112d65deb706cfbc6`  
		Last Modified: Thu, 11 Jun 2026 00:26:14 GMT  
		Size: 153.5 KB (153481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3314b48b94577865e96641c557d5048167254c141db1725db6a5b7a623b68f7b`  
		Last Modified: Thu, 11 Jun 2026 00:26:15 GMT  
		Size: 2.3 MB (2263038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e33e48bcfd48ec271ffa516b5c3b03458185abfb31596aca0b854e9c9367fb9`  
		Last Modified: Thu, 11 Jun 2026 00:26:15 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb41e83cd817b17ff4c2b62ce482681096f6783b2a32be0407cada277d4f293`  
		Last Modified: Thu, 11 Jun 2026 00:26:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:0253549da149222537eeb2e51a1b411b7662c20d8c8964e71967cf670ce9c992
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af9894c8fa8e920a07bf631bed91c9b67398338986159408229a8da050b21c3b`

```dockerfile
```

-	Layers:
	-	`sha256:a11c09037e68845f3c8c01efb996710c3b2d21ba868a98c3ba2582a28d0f1047`  
		Last Modified: Thu, 11 Jun 2026 00:26:15 GMT  
		Size: 2.0 MB (2008676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40468c38b6f60c4625c352d5bdc83ea61510da0efeb2542777603da191a5d2fa`  
		Last Modified: Thu, 11 Jun 2026 00:26:14 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; 386

```console
$ docker pull memcached@sha256:e134667b3198bc9f05962d9bb97cf359ab04c31cb8d11c75e2683de54cebd46e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33675616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cba4eb3d3e82545273aa5ff6f0e6f7bf2b1240176b9489d2315fcf290b9c49a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:18:22 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 11 Jun 2026 00:18:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:21:26 GMT
ENV MEMCACHED_VERSION=1.6.42
# Thu, 11 Jun 2026 00:21:26 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Thu, 11 Jun 2026 00:21:26 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Thu, 11 Jun 2026 00:21:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 11 Jun 2026 00:21:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:21:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 11 Jun 2026 00:21:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:21:26 GMT
USER memcache
# Thu, 11 Jun 2026 00:21:26 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 11 Jun 2026 00:21:26 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:720f951a68f4f9ab464e52b53cf88cfb86bc876b3f00956d000420777ab93c0c`  
		Last Modified: Wed, 10 Jun 2026 23:40:30 GMT  
		Size: 31.3 MB (31301194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2607fca8a1b7fbebf74214d1b33f4f0a54aed5fef2bed18ddc89836a7d00e04b`  
		Last Modified: Thu, 11 Jun 2026 00:21:31 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4620fc98d601bc463a1a505fb0ecf42cb42fa76088d5e80dee41474c74f39f1`  
		Last Modified: Thu, 11 Jun 2026 00:21:32 GMT  
		Size: 147.5 KB (147511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a4c97894b05376111399fa19e7429f36d493cb528c53cb81318a2920d5a954`  
		Last Modified: Thu, 11 Jun 2026 00:21:32 GMT  
		Size: 2.2 MB (2225398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f4a764af02d7ba61dd0909ddb429ba92c9a367243a225936fd625fda113340`  
		Last Modified: Thu, 11 Jun 2026 00:21:32 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52e82109e627ebc0d88a9f7c357b97f14b8ac06bdab5d0b6aa50c3b958a13a8`  
		Last Modified: Thu, 11 Jun 2026 00:21:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:6670b6485b54bcae32ddeda5c2d1764d0ee2066f036d0c17f2cc89734f0be8c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d0aef4dacfecea9e8dbc20498736f77e48bf5106eb60bcfa08c1e81a5c4f06c`

```dockerfile
```

-	Layers:
	-	`sha256:0ebdf5fe0d474785e4448d36043967631fb650ec7b52bd865126a7360978a2ea`  
		Last Modified: Thu, 11 Jun 2026 00:21:32 GMT  
		Size: 2.0 MB (2005525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f257ddeb15df7a03d8e7bb57e01531d894c998af32f33cb528199914bd8f6e1c`  
		Last Modified: Thu, 11 Jun 2026 00:21:32 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; ppc64le

```console
$ docker pull memcached@sha256:25e41a95392ee3c63e35711fec0648fbedc92c6be718456ad8fb89ab66f4e825
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36762178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a04e55188a4c60d5cd8eb00b50628fd87658d0d1814097b40417d71b18479e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 02:36:51 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 11 Jun 2026 02:36:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:59:49 GMT
ENV MEMCACHED_VERSION=1.6.42
# Thu, 11 Jun 2026 02:59:49 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Thu, 11 Jun 2026 02:59:49 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Thu, 11 Jun 2026 02:59:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 11 Jun 2026 02:59:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 02:59:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 11 Jun 2026 02:59:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 02:59:50 GMT
USER memcache
# Thu, 11 Jun 2026 02:59:50 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 11 Jun 2026 02:59:50 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9d6b2e320e2b74843186d830e8202c50ebfaeccf823d239e3e3e349a8a508d80`  
		Last Modified: Thu, 11 Jun 2026 00:24:42 GMT  
		Size: 33.6 MB (33606340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d389c79e93b7c7b3cc2a8226edeb6460d8101e245642213048c1a187d08a935d`  
		Last Modified: Thu, 11 Jun 2026 03:00:07 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7bb22e37f822a0e94fa24cd439d7666c214637b0d59c384dd19e12674c74a82`  
		Last Modified: Thu, 11 Jun 2026 03:00:07 GMT  
		Size: 170.4 KB (170363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82cbb5c5e79cdcec98bd562e1a62768994b805ff7d805b6b75b5bf0e349cff8`  
		Last Modified: Thu, 11 Jun 2026 03:00:06 GMT  
		Size: 3.0 MB (2983963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e60c6f3b8886967bbbabece38cfe74eccdfde98cdae42045a33c5b2b29fd6da`  
		Last Modified: Thu, 11 Jun 2026 03:00:08 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc87d370da3b9877481bf9620bda982328b4d722812ec3e77a7b4c50d016eb33`  
		Last Modified: Thu, 11 Jun 2026 03:00:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:0101df893b4af64daa7ee54d012d7b8682b6c1a9ad1d85700cf8ff269664b19e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b06e6f43b0b95c657fb0043338f12918e63fcac640df48783c49ac29092afb0b`

```dockerfile
```

-	Layers:
	-	`sha256:8ed9fcb43f9f08fb8702ae2709d918b6370866fb4697ddf04b93f42080b23d94`  
		Last Modified: Thu, 11 Jun 2026 03:00:08 GMT  
		Size: 2.0 MB (2011969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c6915dddb9ee13a9cd4156b07c521335c76c9687dcb3a08e66e147af9d99453`  
		Last Modified: Thu, 11 Jun 2026 03:00:06 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; riscv64

```console
$ docker pull memcached@sha256:918c03d1a36c36f13b67e3fbf100f93adad50fbbb452fecc3769db0b8cde487c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30626726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1c8f5f48c37fb2ef15e785c080f746aec65afab782672de8b6a63bd88942e41`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1781049600'
# Fri, 12 Jun 2026 00:28:54 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 12 Jun 2026 00:29:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jun 2026 00:42:57 GMT
ENV MEMCACHED_VERSION=1.6.42
# Fri, 12 Jun 2026 00:42:57 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Fri, 12 Jun 2026 00:42:57 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Fri, 12 Jun 2026 00:42:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 12 Jun 2026 00:42:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Jun 2026 00:42:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 12 Jun 2026 00:42:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2026 00:42:57 GMT
USER memcache
# Fri, 12 Jun 2026 00:42:57 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 12 Jun 2026 00:42:57 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0b510fe8545cab831b696965b5a825649c5c945581e912d31a08a0b30ff940c0`  
		Last Modified: Thu, 11 Jun 2026 03:01:06 GMT  
		Size: 28.3 MB (28282305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35e7a152e660b7a61f448299ac325c28198a870bc53d54cd2584d111c3cef30`  
		Last Modified: Fri, 12 Jun 2026 00:43:44 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d26b2af070be1166e165d4bd1eb073a685622ddb1edb5cf4382cb7825faa21a`  
		Last Modified: Fri, 12 Jun 2026 00:43:44 GMT  
		Size: 133.1 KB (133071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ac4d08e6c19ea726574dc4cd56f4d39216f427cdfd9d6e19c91b06583e6630`  
		Last Modified: Fri, 12 Jun 2026 00:43:44 GMT  
		Size: 2.2 MB (2209833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:039ac44117911671ad0fca8638fa93282ad5865273a55e1328d3180ac5c4f463`  
		Last Modified: Fri, 12 Jun 2026 00:43:44 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65787f51c4d435ccf6c4c9c11e27fe642bd5af3fdd4489e11005614f51c21c29`  
		Last Modified: Fri, 12 Jun 2026 00:43:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:5db8b7d0f9f634b02f9f4dfb45d2f0d3fb2ef1778c3e52058327cd5dec31ebce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0de6ff12136279a3005dae5ce29967a780efb19d8a50b71f33b8153d38859c49`

```dockerfile
```

-	Layers:
	-	`sha256:256f6cfcbc556a40776a58fddd91ccacf0870ab5955a42e7e3ea23601ff76633`  
		Last Modified: Fri, 12 Jun 2026 00:43:44 GMT  
		Size: 2.0 MB (2002332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdfa564b06be9c36a9d81da00994136c858ca65d81762277469168a418a9c9fa`  
		Last Modified: Fri, 12 Jun 2026 00:43:44 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-trixie` - linux; s390x

```console
$ docker pull memcached@sha256:75f4e343898a5a326a82f6560f0efdd5d11c5aea7a710327cdfd400ac3244341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32291904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd9e841717be4c79746136574299d1a6552f88fe8566606318efb07377ef20c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:19:32 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 11 Jun 2026 00:19:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:22:55 GMT
ENV MEMCACHED_VERSION=1.6.42
# Thu, 11 Jun 2026 00:22:55 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Thu, 11 Jun 2026 00:22:55 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Thu, 11 Jun 2026 00:22:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 11 Jun 2026 00:22:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:22:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 11 Jun 2026 00:22:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:22:55 GMT
USER memcache
# Thu, 11 Jun 2026 00:22:55 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 11 Jun 2026 00:22:55 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:760dcf74fdfe93300ce15b5b23adf9aa4af45b6ba9d69925863198f64881a537`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 29.9 MB (29851354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159eeccf7c6aa583901267e3c00bf9c124c32be82a1074722d2be0b547fee632`  
		Last Modified: Thu, 11 Jun 2026 00:23:05 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d08bb26724ea31dfaf95eb6c1647b7686671b3869632300d6056a05c3532bd`  
		Last Modified: Thu, 11 Jun 2026 00:23:05 GMT  
		Size: 140.5 KB (140545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b341a8e7ca68a391e79c556246f3f0b81e4a5e747fed517e274d78f49faa30`  
		Last Modified: Thu, 11 Jun 2026 00:23:05 GMT  
		Size: 2.3 MB (2298492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff1b1dd9080cb995308882030f9579f4c5bf2af5b26b7270d6682de75f6e6d5`  
		Last Modified: Thu, 11 Jun 2026 00:23:05 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075343c77f8c8b9a1bb9fe079e853c0e4628b60f1fff7d8dce82d38c3a344bf8`  
		Last Modified: Thu, 11 Jun 2026 00:23:06 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:1f977b6725f519f48d75ffc92c711df863d7c0e4a1d1f0c5a5bc6605533f35e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1104b534613c8d2cc0544b9adf96821b4f7f623262ef6ddc425f13fa94427850`

```dockerfile
```

-	Layers:
	-	`sha256:66bb879abbe8f943d53561fcf4f4262e1b78fb31b6aa3fdac560ffdc45e3d4b5`  
		Last Modified: Thu, 11 Jun 2026 00:23:05 GMT  
		Size: 2.0 MB (2009805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e448bf5a0443ce0296756453f8bca10e0ec97ebc01576de74a28f60b78299f2b`  
		Last Modified: Thu, 11 Jun 2026 00:23:05 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.42`

```console
$ docker pull memcached@sha256:85c0ab87f71b8b3ade708271177a8e5efca5e93c00287b6f25a2d74a27180bfa
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

### `memcached:1.6.42` - linux; amd64

```console
$ docker pull memcached@sha256:09ac4118d89005e47ef3118221840c62f0fa909a2bee07ff571ae1ae59d9a79b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32204821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ad15119e1f73d99f3fbdc56187ea014f4fae2c8fcbe215c259f2fb2b387aefa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:23:00 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 11 Jun 2026 00:23:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:25:47 GMT
ENV MEMCACHED_VERSION=1.6.42
# Thu, 11 Jun 2026 00:25:47 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Thu, 11 Jun 2026 00:25:47 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Thu, 11 Jun 2026 00:25:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 11 Jun 2026 00:25:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:25:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 11 Jun 2026 00:25:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:25:47 GMT
USER memcache
# Thu, 11 Jun 2026 00:25:47 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 11 Jun 2026 00:25:47 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7883ff600bb4cc730c755ccb8be3f5a06371865abe00be70037283c04f4f3f5`  
		Last Modified: Thu, 11 Jun 2026 00:25:53 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d73a0d6b79b50aa2429aebc30b68c38fb0fb43a4a597ce0dd3936605fbb8912e`  
		Last Modified: Thu, 11 Jun 2026 00:25:53 GMT  
		Size: 136.7 KB (136685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5716730726452d6a54ff03d59c7dffbb7ed4f05836877734acf92f7a0512d6a9`  
		Last Modified: Thu, 11 Jun 2026 00:25:53 GMT  
		Size: 2.3 MB (2281206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f338318b7809e3c4be59b7eccaa1e5387cdbe8015c49eac3267097258c54ae89`  
		Last Modified: Thu, 11 Jun 2026 00:25:53 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ca13d7300d84ca43fcce2aa8304787015f83333e041c81c04796354eadce6b`  
		Last Modified: Thu, 11 Jun 2026 00:25:54 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42` - unknown; unknown

```console
$ docker pull memcached@sha256:3d476e3ec28b0dda5046a3223b0e5a8c9ab8dec20bb294a8853da81d828c154d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e2358f67931681260618f406ea3e0032f17f7a82b2a7d36e5511e6413a7133f`

```dockerfile
```

-	Layers:
	-	`sha256:9cb94c17b8cb82e97f6ad217227fa08e25e0fdc9b96fd2fe418e0acc53911305`  
		Last Modified: Thu, 11 Jun 2026 00:25:53 GMT  
		Size: 2.0 MB (2008368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f8a18d24b8d75bd4b8d856878db21e4d4df7e3e553b9d72d0156bbe58c869d3`  
		Last Modified: Thu, 11 Jun 2026 00:25:53 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42` - linux; arm variant v5

```console
$ docker pull memcached@sha256:f059b77d971253090e3862e28d374840935b5c06467230e9bea207fdb6ef3bf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30316631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c99754215fd2490daf10c8c1046bee3ab237e1e95bd4b46ef0610ca9d1c9badc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:19:47 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 11 Jun 2026 00:19:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:23:08 GMT
ENV MEMCACHED_VERSION=1.6.42
# Thu, 11 Jun 2026 00:23:08 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Thu, 11 Jun 2026 00:23:08 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Thu, 11 Jun 2026 00:23:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 11 Jun 2026 00:23:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:23:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 11 Jun 2026 00:23:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:23:08 GMT
USER memcache
# Thu, 11 Jun 2026 00:23:08 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 11 Jun 2026 00:23:08 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ed883f3fd95b7edef302d7ca9520eefdae280af081509bd7e9e5b5ff8f4cda7c`  
		Last Modified: Wed, 10 Jun 2026 23:41:17 GMT  
		Size: 28.0 MB (27959200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e92527947bdcc341ab63777422e7409751516a8bc5ffc61040d76b72e7d58c`  
		Last Modified: Thu, 11 Jun 2026 00:23:14 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c52c9bd0c151ce908cf5e8c55694b4a321a916d3053e9e4cd3b06837e55f325`  
		Last Modified: Thu, 11 Jun 2026 00:23:14 GMT  
		Size: 144.2 KB (144156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ec2615dd4e79e84378f7223c9d7c70a6cdfb8835717c19cadbab17a726210d`  
		Last Modified: Thu, 11 Jun 2026 00:23:14 GMT  
		Size: 2.2 MB (2211763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4249a738c6e8e951ca0bf1608e335442f8f50ff9fe57a524b1bdb472e59ed1`  
		Last Modified: Thu, 11 Jun 2026 00:23:14 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab171fa641968acda113ed8ec0cbff5159a4895efed9c4e08bb6e466a40fb5ce`  
		Last Modified: Thu, 11 Jun 2026 00:23:15 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42` - unknown; unknown

```console
$ docker pull memcached@sha256:a7356b3e73eada1ea16535f45e9a297b7913adfb103e9df5d0a2ee333c58f443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c75fc3f8c74e188d3585642b303189b73ae78c14b089bd14f0d37da2b085f25`

```dockerfile
```

-	Layers:
	-	`sha256:5a953398782781fbd31e5d1fb67c1cdeb82c91397fb27ce32b9d756cc938a03a`  
		Last Modified: Thu, 11 Jun 2026 00:23:14 GMT  
		Size: 2.0 MB (2011371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aeae6ddb09b0b52fdf1e1db9b67dfa04fba888fbba5c54b1b7e30ecbd56dafde`  
		Last Modified: Thu, 11 Jun 2026 00:23:14 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42` - linux; arm variant v7

```console
$ docker pull memcached@sha256:7b20950329f422c7b322057fe1f944f98589cf937e5e65118b6d4bb241436ffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28513288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5d65e3287f7256814db41a73f2978df2252f6ac399369fe1a7a3eb1c4ceb3e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:21:55 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 11 Jun 2026 00:21:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:25:06 GMT
ENV MEMCACHED_VERSION=1.6.42
# Thu, 11 Jun 2026 00:25:06 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Thu, 11 Jun 2026 00:25:06 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Thu, 11 Jun 2026 00:25:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 11 Jun 2026 00:25:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:25:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 11 Jun 2026 00:25:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:25:06 GMT
USER memcache
# Thu, 11 Jun 2026 00:25:06 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 11 Jun 2026 00:25:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4bd6ddea06d5009ee47ddb0f254a2569aff0230c005869ebd416b20295d945c0`  
		Last Modified: Wed, 10 Jun 2026 23:42:34 GMT  
		Size: 26.2 MB (26211004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bcac116a5bd6f8c4ba910742373294134be4443587cce918db3492895262e16`  
		Last Modified: Thu, 11 Jun 2026 00:25:12 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af6a74cecf5734c352e3c2ea5fb348246cfe77549b6cb2afe3116aaf39983ff8`  
		Last Modified: Thu, 11 Jun 2026 00:25:12 GMT  
		Size: 135.4 KB (135382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6189c46b05f5cdb39083034f258358c5472cc6824a25a7dc8a8f60ae58891116`  
		Last Modified: Thu, 11 Jun 2026 00:25:12 GMT  
		Size: 2.2 MB (2165385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfeedbf1b9c25a3c29e32962704f935689b2b60c4096315dbee3365a9cec4dc0`  
		Last Modified: Thu, 11 Jun 2026 00:25:12 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0309704e28c847b1dd0249a490a5774838b3d27bf059481108e0f1a300efd4ae`  
		Last Modified: Thu, 11 Jun 2026 00:25:13 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42` - unknown; unknown

```console
$ docker pull memcached@sha256:84793c5cdc418c73cc53c1dcdf3ebaf9d1c2a7910ec63c85d179a691e05f1ddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0981cd8d43f93fb996bbc87f0659a7c3a7163d74a5c84503eb77588ed240010c`

```dockerfile
```

-	Layers:
	-	`sha256:39acaedd56024e59130ae654692bdff06d01b71719567ede3d9ece539679150e`  
		Last Modified: Thu, 11 Jun 2026 00:25:13 GMT  
		Size: 2.0 MB (2009828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ada0017eed4fa0f3db9a2e1669d0eb74e2908e65a483af6819df971d18d767a`  
		Last Modified: Thu, 11 Jun 2026 00:25:12 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:a36eca5b5840c718ca41526a871fd751dc96965f182778a7631a0c2896c3f44a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32566560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31c7500da651c7c5945a2db8b00248c02ad2947b4eccb66b464759cd6f4ea2c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:23:08 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 11 Jun 2026 00:23:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:26:08 GMT
ENV MEMCACHED_VERSION=1.6.42
# Thu, 11 Jun 2026 00:26:08 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Thu, 11 Jun 2026 00:26:08 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Thu, 11 Jun 2026 00:26:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 11 Jun 2026 00:26:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:26:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 11 Jun 2026 00:26:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:26:08 GMT
USER memcache
# Thu, 11 Jun 2026 00:26:08 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 11 Jun 2026 00:26:08 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb68ad832950ffa1d5fe24c7e7ee4e061b358d6bcb14dfdb1bb2dec4c557f7a2`  
		Last Modified: Thu, 11 Jun 2026 00:26:15 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f6f966199cad211cd492fc65c6c927fde3a05499bdd9a2112d65deb706cfbc6`  
		Last Modified: Thu, 11 Jun 2026 00:26:14 GMT  
		Size: 153.5 KB (153481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3314b48b94577865e96641c557d5048167254c141db1725db6a5b7a623b68f7b`  
		Last Modified: Thu, 11 Jun 2026 00:26:15 GMT  
		Size: 2.3 MB (2263038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e33e48bcfd48ec271ffa516b5c3b03458185abfb31596aca0b854e9c9367fb9`  
		Last Modified: Thu, 11 Jun 2026 00:26:15 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb41e83cd817b17ff4c2b62ce482681096f6783b2a32be0407cada277d4f293`  
		Last Modified: Thu, 11 Jun 2026 00:26:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42` - unknown; unknown

```console
$ docker pull memcached@sha256:0253549da149222537eeb2e51a1b411b7662c20d8c8964e71967cf670ce9c992
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af9894c8fa8e920a07bf631bed91c9b67398338986159408229a8da050b21c3b`

```dockerfile
```

-	Layers:
	-	`sha256:a11c09037e68845f3c8c01efb996710c3b2d21ba868a98c3ba2582a28d0f1047`  
		Last Modified: Thu, 11 Jun 2026 00:26:15 GMT  
		Size: 2.0 MB (2008676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40468c38b6f60c4625c352d5bdc83ea61510da0efeb2542777603da191a5d2fa`  
		Last Modified: Thu, 11 Jun 2026 00:26:14 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42` - linux; 386

```console
$ docker pull memcached@sha256:e134667b3198bc9f05962d9bb97cf359ab04c31cb8d11c75e2683de54cebd46e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33675616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cba4eb3d3e82545273aa5ff6f0e6f7bf2b1240176b9489d2315fcf290b9c49a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:18:22 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 11 Jun 2026 00:18:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:21:26 GMT
ENV MEMCACHED_VERSION=1.6.42
# Thu, 11 Jun 2026 00:21:26 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Thu, 11 Jun 2026 00:21:26 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Thu, 11 Jun 2026 00:21:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 11 Jun 2026 00:21:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:21:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 11 Jun 2026 00:21:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:21:26 GMT
USER memcache
# Thu, 11 Jun 2026 00:21:26 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 11 Jun 2026 00:21:26 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:720f951a68f4f9ab464e52b53cf88cfb86bc876b3f00956d000420777ab93c0c`  
		Last Modified: Wed, 10 Jun 2026 23:40:30 GMT  
		Size: 31.3 MB (31301194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2607fca8a1b7fbebf74214d1b33f4f0a54aed5fef2bed18ddc89836a7d00e04b`  
		Last Modified: Thu, 11 Jun 2026 00:21:31 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4620fc98d601bc463a1a505fb0ecf42cb42fa76088d5e80dee41474c74f39f1`  
		Last Modified: Thu, 11 Jun 2026 00:21:32 GMT  
		Size: 147.5 KB (147511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a4c97894b05376111399fa19e7429f36d493cb528c53cb81318a2920d5a954`  
		Last Modified: Thu, 11 Jun 2026 00:21:32 GMT  
		Size: 2.2 MB (2225398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f4a764af02d7ba61dd0909ddb429ba92c9a367243a225936fd625fda113340`  
		Last Modified: Thu, 11 Jun 2026 00:21:32 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52e82109e627ebc0d88a9f7c357b97f14b8ac06bdab5d0b6aa50c3b958a13a8`  
		Last Modified: Thu, 11 Jun 2026 00:21:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42` - unknown; unknown

```console
$ docker pull memcached@sha256:6670b6485b54bcae32ddeda5c2d1764d0ee2066f036d0c17f2cc89734f0be8c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d0aef4dacfecea9e8dbc20498736f77e48bf5106eb60bcfa08c1e81a5c4f06c`

```dockerfile
```

-	Layers:
	-	`sha256:0ebdf5fe0d474785e4448d36043967631fb650ec7b52bd865126a7360978a2ea`  
		Last Modified: Thu, 11 Jun 2026 00:21:32 GMT  
		Size: 2.0 MB (2005525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f257ddeb15df7a03d8e7bb57e01531d894c998af32f33cb528199914bd8f6e1c`  
		Last Modified: Thu, 11 Jun 2026 00:21:32 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42` - linux; ppc64le

```console
$ docker pull memcached@sha256:25e41a95392ee3c63e35711fec0648fbedc92c6be718456ad8fb89ab66f4e825
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36762178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a04e55188a4c60d5cd8eb00b50628fd87658d0d1814097b40417d71b18479e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 02:36:51 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 11 Jun 2026 02:36:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:59:49 GMT
ENV MEMCACHED_VERSION=1.6.42
# Thu, 11 Jun 2026 02:59:49 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Thu, 11 Jun 2026 02:59:49 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Thu, 11 Jun 2026 02:59:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 11 Jun 2026 02:59:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 02:59:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 11 Jun 2026 02:59:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 02:59:50 GMT
USER memcache
# Thu, 11 Jun 2026 02:59:50 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 11 Jun 2026 02:59:50 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9d6b2e320e2b74843186d830e8202c50ebfaeccf823d239e3e3e349a8a508d80`  
		Last Modified: Thu, 11 Jun 2026 00:24:42 GMT  
		Size: 33.6 MB (33606340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d389c79e93b7c7b3cc2a8226edeb6460d8101e245642213048c1a187d08a935d`  
		Last Modified: Thu, 11 Jun 2026 03:00:07 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7bb22e37f822a0e94fa24cd439d7666c214637b0d59c384dd19e12674c74a82`  
		Last Modified: Thu, 11 Jun 2026 03:00:07 GMT  
		Size: 170.4 KB (170363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82cbb5c5e79cdcec98bd562e1a62768994b805ff7d805b6b75b5bf0e349cff8`  
		Last Modified: Thu, 11 Jun 2026 03:00:06 GMT  
		Size: 3.0 MB (2983963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e60c6f3b8886967bbbabece38cfe74eccdfde98cdae42045a33c5b2b29fd6da`  
		Last Modified: Thu, 11 Jun 2026 03:00:08 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc87d370da3b9877481bf9620bda982328b4d722812ec3e77a7b4c50d016eb33`  
		Last Modified: Thu, 11 Jun 2026 03:00:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42` - unknown; unknown

```console
$ docker pull memcached@sha256:0101df893b4af64daa7ee54d012d7b8682b6c1a9ad1d85700cf8ff269664b19e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b06e6f43b0b95c657fb0043338f12918e63fcac640df48783c49ac29092afb0b`

```dockerfile
```

-	Layers:
	-	`sha256:8ed9fcb43f9f08fb8702ae2709d918b6370866fb4697ddf04b93f42080b23d94`  
		Last Modified: Thu, 11 Jun 2026 03:00:08 GMT  
		Size: 2.0 MB (2011969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c6915dddb9ee13a9cd4156b07c521335c76c9687dcb3a08e66e147af9d99453`  
		Last Modified: Thu, 11 Jun 2026 03:00:06 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42` - linux; riscv64

```console
$ docker pull memcached@sha256:918c03d1a36c36f13b67e3fbf100f93adad50fbbb452fecc3769db0b8cde487c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30626726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1c8f5f48c37fb2ef15e785c080f746aec65afab782672de8b6a63bd88942e41`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1781049600'
# Fri, 12 Jun 2026 00:28:54 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 12 Jun 2026 00:29:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jun 2026 00:42:57 GMT
ENV MEMCACHED_VERSION=1.6.42
# Fri, 12 Jun 2026 00:42:57 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Fri, 12 Jun 2026 00:42:57 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Fri, 12 Jun 2026 00:42:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 12 Jun 2026 00:42:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Jun 2026 00:42:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 12 Jun 2026 00:42:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2026 00:42:57 GMT
USER memcache
# Fri, 12 Jun 2026 00:42:57 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 12 Jun 2026 00:42:57 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0b510fe8545cab831b696965b5a825649c5c945581e912d31a08a0b30ff940c0`  
		Last Modified: Thu, 11 Jun 2026 03:01:06 GMT  
		Size: 28.3 MB (28282305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35e7a152e660b7a61f448299ac325c28198a870bc53d54cd2584d111c3cef30`  
		Last Modified: Fri, 12 Jun 2026 00:43:44 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d26b2af070be1166e165d4bd1eb073a685622ddb1edb5cf4382cb7825faa21a`  
		Last Modified: Fri, 12 Jun 2026 00:43:44 GMT  
		Size: 133.1 KB (133071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ac4d08e6c19ea726574dc4cd56f4d39216f427cdfd9d6e19c91b06583e6630`  
		Last Modified: Fri, 12 Jun 2026 00:43:44 GMT  
		Size: 2.2 MB (2209833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:039ac44117911671ad0fca8638fa93282ad5865273a55e1328d3180ac5c4f463`  
		Last Modified: Fri, 12 Jun 2026 00:43:44 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65787f51c4d435ccf6c4c9c11e27fe642bd5af3fdd4489e11005614f51c21c29`  
		Last Modified: Fri, 12 Jun 2026 00:43:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42` - unknown; unknown

```console
$ docker pull memcached@sha256:5db8b7d0f9f634b02f9f4dfb45d2f0d3fb2ef1778c3e52058327cd5dec31ebce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0de6ff12136279a3005dae5ce29967a780efb19d8a50b71f33b8153d38859c49`

```dockerfile
```

-	Layers:
	-	`sha256:256f6cfcbc556a40776a58fddd91ccacf0870ab5955a42e7e3ea23601ff76633`  
		Last Modified: Fri, 12 Jun 2026 00:43:44 GMT  
		Size: 2.0 MB (2002332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdfa564b06be9c36a9d81da00994136c858ca65d81762277469168a418a9c9fa`  
		Last Modified: Fri, 12 Jun 2026 00:43:44 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42` - linux; s390x

```console
$ docker pull memcached@sha256:75f4e343898a5a326a82f6560f0efdd5d11c5aea7a710327cdfd400ac3244341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32291904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd9e841717be4c79746136574299d1a6552f88fe8566606318efb07377ef20c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:19:32 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 11 Jun 2026 00:19:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:22:55 GMT
ENV MEMCACHED_VERSION=1.6.42
# Thu, 11 Jun 2026 00:22:55 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Thu, 11 Jun 2026 00:22:55 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Thu, 11 Jun 2026 00:22:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 11 Jun 2026 00:22:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:22:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 11 Jun 2026 00:22:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:22:55 GMT
USER memcache
# Thu, 11 Jun 2026 00:22:55 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 11 Jun 2026 00:22:55 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:760dcf74fdfe93300ce15b5b23adf9aa4af45b6ba9d69925863198f64881a537`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 29.9 MB (29851354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159eeccf7c6aa583901267e3c00bf9c124c32be82a1074722d2be0b547fee632`  
		Last Modified: Thu, 11 Jun 2026 00:23:05 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d08bb26724ea31dfaf95eb6c1647b7686671b3869632300d6056a05c3532bd`  
		Last Modified: Thu, 11 Jun 2026 00:23:05 GMT  
		Size: 140.5 KB (140545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b341a8e7ca68a391e79c556246f3f0b81e4a5e747fed517e274d78f49faa30`  
		Last Modified: Thu, 11 Jun 2026 00:23:05 GMT  
		Size: 2.3 MB (2298492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff1b1dd9080cb995308882030f9579f4c5bf2af5b26b7270d6682de75f6e6d5`  
		Last Modified: Thu, 11 Jun 2026 00:23:05 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075343c77f8c8b9a1bb9fe079e853c0e4628b60f1fff7d8dce82d38c3a344bf8`  
		Last Modified: Thu, 11 Jun 2026 00:23:06 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42` - unknown; unknown

```console
$ docker pull memcached@sha256:1f977b6725f519f48d75ffc92c711df863d7c0e4a1d1f0c5a5bc6605533f35e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1104b534613c8d2cc0544b9adf96821b4f7f623262ef6ddc425f13fa94427850`

```dockerfile
```

-	Layers:
	-	`sha256:66bb879abbe8f943d53561fcf4f4262e1b78fb31b6aa3fdac560ffdc45e3d4b5`  
		Last Modified: Thu, 11 Jun 2026 00:23:05 GMT  
		Size: 2.0 MB (2009805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e448bf5a0443ce0296756453f8bca10e0ec97ebc01576de74a28f60b78299f2b`  
		Last Modified: Thu, 11 Jun 2026 00:23:05 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.42-alpine`

```console
$ docker pull memcached@sha256:7381333da6d6ae06e02d8dfc87ee6f2c7cd0a19f7ba048d5efc538d2100e2208
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

### `memcached:1.6.42-alpine` - linux; amd64

```console
$ docker pull memcached@sha256:ce375dd48f976d33bf35beb966cc37f202fd840a90891e58b9e71171fc74174d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5921579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19d284e7a8445d8dc70e97c673a8a0175d18f39d5336ccbdfa8b240c0ef3ce4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:29 GMT
ADD alpine-minirootfs-3.24.1-x86_64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:15:18 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:15:18 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:17:54 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:17:54 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:17:54 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:17:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:17:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:17:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:17:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:17:54 GMT
USER memcache
# Tue, 16 Jun 2026 00:17:54 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:17:54 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:55afa1ecc21d2bb5e5045f32dafee56272ffd89860bac26f6c32123439af26a4`  
		Last Modified: Sun, 14 Jun 2026 06:44:06 GMT  
		Size: 3.8 MB (3846391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb73756dcbbebc424eab53d3adda4d9f64001e7a91272a7b2a834622c08b093`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f0d6a5291334f2b54ec652193cd4e17ee22455b2f3ff3bd9b66acff6436c7b`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 106.1 KB (106066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ac11a8307528096ac745e0ef681b64854bbd012ffdfbce85587153eec73563`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 2.0 MB (1967772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3626493aad85d70a212bc66e9d45db8aef43b4bc662259563f916398165f1e64`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cdcd3f20e3aa439838f5491e6f457a42bad6c80ed9b099313bf79b57a721ea8`  
		Last Modified: Tue, 16 Jun 2026 00:18:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:bb948800301f1cae8e18e317f2b9e85636c86c4a1924ee85e125da37cb1333e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c3e084937eb543038244e151b03b8d9a0dce0b4d5bf87c2d471fa397ed5702`

```dockerfile
```

-	Layers:
	-	`sha256:9d05a792212c92363a76bb6a8205a6e7f386113b3efc1b5d600f93d4e237c975`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 94.9 KB (94897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee0e7e70ef03205f55c68bc1b74ac7854183aee4e871112794975dc852761b19`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42-alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:4b144cdbc67c11035b3d0f0c812b590ee694977f2f6a32321e538237bd2f841c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5573158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e9bb70df1535a2f8ca960f733a4404cbde900a13156a1f4446c2fd110258e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:25 GMT
ADD alpine-minirootfs-3.24.1-armhf.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:25 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:14:43 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:14:44 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:17:47 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:17:47 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:17:47 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:17:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:17:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:17:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:17:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:17:47 GMT
USER memcache
# Tue, 16 Jun 2026 00:17:47 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:17:47 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3c4836a46d600cfe9a422adf7a80205cb534097e6213325e0176c51f6e5cc02e`  
		Last Modified: Sun, 14 Jun 2026 06:44:57 GMT  
		Size: 3.6 MB (3553450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e732a60042adf5cff5fe4fe0de83f937f6e5c8896500f7023e8bf68ed0670d65`  
		Last Modified: Tue, 16 Jun 2026 00:17:51 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad86d1fea29db061a5ae896a0a595b144edcdb4af59deac2b75b0fb8f5fa2d4c`  
		Last Modified: Tue, 16 Jun 2026 00:17:50 GMT  
		Size: 102.6 KB (102624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f26dd2445dbf4d5624417ca290f5ae2e5774fa7fec4f5655cd2377ee3147e4`  
		Last Modified: Tue, 16 Jun 2026 00:17:51 GMT  
		Size: 1.9 MB (1915730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080a186f0ca6beb06a5ce4a86fbc71f5b9995713fcc899c73f995f251ef7c987`  
		Last Modified: Tue, 16 Jun 2026 00:17:51 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c4d4f455f9a2b633cca28e3aa2190e4c42ca83ca6e3ea88ea4abe16944d238`  
		Last Modified: Tue, 16 Jun 2026 00:17:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:d6b7abf6ef34abf12ab2c7f84bd29ac2461eb3271d1c4070456ed9b94e4b41a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43a767571287c8ca227e321ee8d65f9da82e558098bedbb15888434dcc1ce9fa`

```dockerfile
```

-	Layers:
	-	`sha256:1794ccef4392c0db4ba36ad7fde22cdacbda40f4d56f0adbef802163c87e066c`  
		Last Modified: Tue, 16 Jun 2026 00:17:51 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42-alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:848c5e0ced69b802cca72c23bec05a4c6f23136212a4a1d5cc22b7c8f0154bf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:286f62a53a8947036e39f2b79567b31d38309fd84c7a39e43de8c5f9817a2f64`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:26 GMT
ADD alpine-minirootfs-3.24.1-armv7.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:26 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:17:59 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:17:59 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:20:56 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:20:56 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:20:56 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:20:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:20:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:20:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:20:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:20:56 GMT
USER memcache
# Tue, 16 Jun 2026 00:20:56 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:20:56 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bc03a9e5b4dd452551f246e199537fe7afc1765f53f510bc81d26df9845e4008`  
		Last Modified: Sun, 14 Jun 2026 06:45:22 GMT  
		Size: 3.3 MB (3260615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f0249bacfc8953b72899bf7b6c904c8750482fce4c93108f57b2c64228b279`  
		Last Modified: Tue, 16 Jun 2026 00:21:00 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95e1b321ffc31d01e766d5d1d054967d613940563406fc54ee981926b7f6049`  
		Last Modified: Tue, 16 Jun 2026 00:21:01 GMT  
		Size: 92.4 KB (92366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce112e60c1b15077277c233a7707831818dff0a15f1fc977ebebc93f817dad43`  
		Last Modified: Tue, 16 Jun 2026 00:21:01 GMT  
		Size: 1.9 MB (1875183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32fa6ed5b14fd6fcf96a7cde2996063f10b8efe802c386479288a232af826027`  
		Last Modified: Tue, 16 Jun 2026 00:21:01 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6648f8180a4eea1f5197f2fa2d356fbbf4e5f65345e189e720e227af64a5e31`  
		Last Modified: Tue, 16 Jun 2026 00:21:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:59387f31eff7cfb3166c5e6d4bad92e255705affcc15c84c4a06c86ecb1a9890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:174eb460b1df4523a4f71ba5a996f2285fa845fe8ef76d2df3ea8c4962c6b6ca`

```dockerfile
```

-	Layers:
	-	`sha256:4ff5e70775e819cab551295c56b58fdb0c44c105cdc4f72247e3968accd2ab2f`  
		Last Modified: Tue, 16 Jun 2026 00:21:00 GMT  
		Size: 94.3 KB (94315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00f10e1301c7e61396658f7e3ed330e400a9f304c6a0323de8ff644aba987474`  
		Last Modified: Tue, 16 Jun 2026 00:21:01 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:33261748facce282dbe4dbb4d9f875139680fce4cefc13cb9ad8e1ced23f9557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6250475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1614bb2865c8f849c2bc5bf77703a1ab711695c607a8bc6edb013a076ec16d6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:20 GMT
ADD alpine-minirootfs-3.24.1-aarch64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:20 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:13:18 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:13:18 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:16:06 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:16:06 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:16:06 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:16:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:16:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:16:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:16:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:16:06 GMT
USER memcache
# Tue, 16 Jun 2026 00:16:06 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:16:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5de55e5ef9c033997441461efe7ba23a986db059c0bb78b38f84ee0d72b99167`  
		Last Modified: Sun, 14 Jun 2026 06:44:31 GMT  
		Size: 4.2 MB (4183037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5faa19f06c4d5e26332739c7f08fd3dcd2c81817471c62029a6d99af6be8748`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377a35d28f00766e2679c788b95b0a67b9aa5a76c8ef701a2a9604e2a00c3b46`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 121.8 KB (121841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0b819e89558d70f1401ca58cbc19c58ae13e15be8184fd9b2733e022f318a4`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 1.9 MB (1944247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca539cef48ff8c3f723ab23506b6786c9ed26a9cac713601b71de2dc775d26a`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c4c456deed244daa6d7076f40a1cf0364d294059bb43e533677a89027843b15`  
		Last Modified: Tue, 16 Jun 2026 00:16:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:4d25960abc53b5ba1896b8f5ee04ba5ac1389900ab9b413eb62285af7281aedb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d1a4b7ad428a08c8a174d5ecd9763d530e849f54a2d9b90aef934e54b9477d4`

```dockerfile
```

-	Layers:
	-	`sha256:9c0a8e5e07390fae6abe9204450009671011c4d2d5aa5fe4afdd82324fdb49b9`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 94.4 KB (94351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ee01158358d01c082867cf46a5225cf101013e4d5b7eae18fc7853e277ff0f4`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 20.7 KB (20727 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42-alpine` - linux; 386

```console
$ docker pull memcached@sha256:5436d0ef6e12f2f8e454384ff4a703132b3fe820c41a55336f520bb5d1622574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5702329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8946be3d97c7b9825159f58cbf832b131c75cb90b3fb46a40d5429b9ffe32bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:19 GMT
ADD alpine-minirootfs-3.24.1-x86.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:19 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:13:59 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:13:59 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:16:45 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:16:45 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:16:45 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:16:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:16:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:16:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:16:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:16:46 GMT
USER memcache
# Tue, 16 Jun 2026 00:16:46 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:16:46 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f86df9d778509895efbf9363d8fcb0cbe0b772de536c7218e4c4c947f0be879f`  
		Last Modified: Sun, 14 Jun 2026 06:45:46 GMT  
		Size: 3.7 MB (3670141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043137360442e605bc150f28f20e1fa2d23d90131370bc405ad7d35309594491`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900ce6eeaece12033b12f1c8641c33dcf62ff2525584411911368cfcd0b38224`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 110.7 KB (110729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e8cc1c8f6bc6391eb1a43a46f0b55ca7845f824fc0f2fc7ae7587a7715814e`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 1.9 MB (1920111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d94f6e4d3be92188fc182a3557fe43af5bc9f3e768a7f265977743a56eea527e`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f8a19f18dfff271426de7a17ab6780788fa4345d5fa0120e6d03720d552bd4`  
		Last Modified: Tue, 16 Jun 2026 00:16:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:00dc6a7f29b7f2f5ac46fc5678b80c43c7b1e46b4ca3c84c5597034180aeb644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6de04019c7775544db9adbb4c4558d0e7c842c279e5d70532b2ac0b988ac1345`

```dockerfile
```

-	Layers:
	-	`sha256:80895f8f5e9c9b015e419096426322f4c86c33d55ca8860ee046b61d52782847`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 94.9 KB (94852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c69be8c1f82a066b46cc389712508e85c1dcd77e649c922dba46ace64b343ae`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:c7857941a51b85b136781035703afcc8854a2d70fa2091208a51f8bb7e71f934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5998515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b02b2222212c64e444ac1a2227b19f0cfb1282c8a8ced386c1b79ae48c641b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:15 GMT
ADD alpine-minirootfs-3.24.1-ppc64le.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:15 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:15:37 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:15:38 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:18:22 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:18:22 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:18:22 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:18:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:18:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:18:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:18:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:18:22 GMT
USER memcache
# Tue, 16 Jun 2026 00:18:22 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:18:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3ebcdcd395ccee658b9200e4b27d7699e5d6ed9f6c1858dea12781aac519ff59`  
		Last Modified: Sun, 14 Jun 2026 06:46:36 GMT  
		Size: 3.8 MB (3813400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b108e2058722fb0fb5a9310e8ebe82ab4b9c021228a94b3125ba49d318e9667`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb8160ed736eda8513164d5d703082fb0c9af9e037472ab70a02579caa3eb99`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 126.3 KB (126252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5cb88dd03ce07ecf1613c2aff220fb392763d8f22edc900c4ad032ee7103d34`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 2.1 MB (2057508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a12fd57420ca797ab383c58a488044d324c4d43b3c94a848f86a0524ed3064b4`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1c0c7b7a77e9375d8a75fb825fa274d9127ca96de79107550517be29501c817`  
		Last Modified: Tue, 16 Jun 2026 00:18:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:851f463d4778539d5e4981f972420f9a57ec2559488f8a59fba6abab6065032f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:734dd3d91f2d6cf217233f7a9dacc3c20ff0590246adb790f95713fb21c115de`

```dockerfile
```

-	Layers:
	-	`sha256:c0d4c203ef9f66cf827ec62098d7801e1c49f1187e0fe047fd32fc2a3271f636`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 94.3 KB (94304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b734d170b5463fa77dd77072e06d51a28efe59a53600d47435b015ebcadae92`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42-alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:ba5bf40b4adc1fe04f32e2e239fa9c0020d4e89bf4079493f8bc11a92c8f4b51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5738070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d12fbf86d6880aaa9d517425d9cecddcf545ba87e577a039dea9ea99ad53d8a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 05:59:15 GMT
ADD alpine-minirootfs-3.24.1-riscv64.tar.gz / # buildkit
# Tue, 16 Jun 2026 05:59:15 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 08:28:27 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 19 Jun 2026 08:28:31 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 19 Jun 2026 08:41:52 GMT
ENV MEMCACHED_VERSION=1.6.42
# Fri, 19 Jun 2026 08:41:52 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Fri, 19 Jun 2026 08:41:52 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Fri, 19 Jun 2026 08:41:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 19 Jun 2026 08:41:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 08:41:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 19 Jun 2026 08:41:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 08:41:53 GMT
USER memcache
# Fri, 19 Jun 2026 08:41:53 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 19 Jun 2026 08:41:53 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c34e5222b29b86391cdae95b0473ef789493ff1a0068a3a30b5d66f544bd7cf6`  
		Last Modified: Sun, 14 Jun 2026 06:47:00 GMT  
		Size: 3.6 MB (3574358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e09d95a0f414638430c0cd3ecfdcce75606201917a27c7cb2ce1e34cb928b26a`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a5335c7af79a1b08af55862ba77644afdae5544d9a7871e45c91b364bd4f71d`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 108.9 KB (108888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3622a6ea71515db1ef566afdbb121daed1f408aacf1519f4173b40dabe2ae627`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 2.1 MB (2053467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1db0e3e31ca3f2830f5404436e92b1862a4078adefacacec09a9580a3ad0a2`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1463b0fd26a37659aaad7f99696e5213764ad03bb094f40836c3309713d7a60`  
		Last Modified: Fri, 19 Jun 2026 08:42:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:aadb3b9338400b87692f95e00931e43940f8d6ddd13f046bd256848dd825e458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bde4b5a4a468d795a5f58dd934b371adfe72cd2ae24e166e1258ad65aa455a56`

```dockerfile
```

-	Layers:
	-	`sha256:debb70180cf674562f7ca321270e3dfa350c5d1596c05dbfcc27b38c65652528`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 94.3 KB (94300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a895bbe0bfec24678c1c92ddd283cb7392e0e8d229f31c769a23c95224c0d371`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:e1b640e8d192055e5c3ccd05b077776a0f4d35664191596f7a8230b2cd7ef0f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5823313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1ef6221f9c2854683b0633325a98a0e7a0d3b7d865b02d7cdf4c1d49d2e5090`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:21 GMT
ADD alpine-minirootfs-3.24.1-s390x.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:21 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:13:46 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:13:46 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:17:12 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:17:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:17:12 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:17:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:17:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:17:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:17:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:17:12 GMT
USER memcache
# Tue, 16 Jun 2026 00:17:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:17:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:da43be6afaaa3ec1b607461ce64380942a6d76c3d52cda4337b0770d9a96fa89`  
		Last Modified: Sun, 14 Jun 2026 06:47:25 GMT  
		Size: 3.7 MB (3709320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757d04238e02c9bbe1cfd4030cc19e29421650a1b1562a8ca4090d90e9ae17b0`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1949e0fa71fc91bebf4f2e4293108b27de8357d98f98b673bc4f3ed1980b52c`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 114.3 KB (114289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f0e22966bce79fbc8a20f7c27aa07ce63229bb50181319c810ca29f1fb4032`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 2.0 MB (1998350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15eb5e912ef8ec6e3abe76c361cdddb568d20a60be21be379d4d8d7d0ebaa11e`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a549d59ad0d4761ac6f4cca272c4bea521471ed091d0e79143bfda8ff29cf9ce`  
		Last Modified: Tue, 16 Jun 2026 00:17:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:6dbf7c8a98f02a949769403ad1c92583b34a28dccc66b7d83d91863785a6dad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a89d23372d19daf2d6d4e1c4de732f7864316ed5e7713b1103918303873683e`

```dockerfile
```

-	Layers:
	-	`sha256:099ab2d711ef73783b01895824a4664c7d65e2a333e81237b4766cf053a8f6f0`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 94.2 KB (94246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0eccbabf44891af00e622624c5cfd5a295656f82f1c15073b240ac34d47af96c`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.42-alpine3.24`

```console
$ docker pull memcached@sha256:7381333da6d6ae06e02d8dfc87ee6f2c7cd0a19f7ba048d5efc538d2100e2208
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

### `memcached:1.6.42-alpine3.24` - linux; amd64

```console
$ docker pull memcached@sha256:ce375dd48f976d33bf35beb966cc37f202fd840a90891e58b9e71171fc74174d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5921579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19d284e7a8445d8dc70e97c673a8a0175d18f39d5336ccbdfa8b240c0ef3ce4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:29 GMT
ADD alpine-minirootfs-3.24.1-x86_64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:15:18 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:15:18 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:17:54 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:17:54 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:17:54 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:17:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:17:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:17:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:17:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:17:54 GMT
USER memcache
# Tue, 16 Jun 2026 00:17:54 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:17:54 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:55afa1ecc21d2bb5e5045f32dafee56272ffd89860bac26f6c32123439af26a4`  
		Last Modified: Sun, 14 Jun 2026 06:44:06 GMT  
		Size: 3.8 MB (3846391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb73756dcbbebc424eab53d3adda4d9f64001e7a91272a7b2a834622c08b093`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f0d6a5291334f2b54ec652193cd4e17ee22455b2f3ff3bd9b66acff6436c7b`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 106.1 KB (106066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ac11a8307528096ac745e0ef681b64854bbd012ffdfbce85587153eec73563`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 2.0 MB (1967772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3626493aad85d70a212bc66e9d45db8aef43b4bc662259563f916398165f1e64`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cdcd3f20e3aa439838f5491e6f457a42bad6c80ed9b099313bf79b57a721ea8`  
		Last Modified: Tue, 16 Jun 2026 00:18:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:bb948800301f1cae8e18e317f2b9e85636c86c4a1924ee85e125da37cb1333e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c3e084937eb543038244e151b03b8d9a0dce0b4d5bf87c2d471fa397ed5702`

```dockerfile
```

-	Layers:
	-	`sha256:9d05a792212c92363a76bb6a8205a6e7f386113b3efc1b5d600f93d4e237c975`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 94.9 KB (94897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee0e7e70ef03205f55c68bc1b74ac7854183aee4e871112794975dc852761b19`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42-alpine3.24` - linux; arm variant v6

```console
$ docker pull memcached@sha256:4b144cdbc67c11035b3d0f0c812b590ee694977f2f6a32321e538237bd2f841c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5573158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e9bb70df1535a2f8ca960f733a4404cbde900a13156a1f4446c2fd110258e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:25 GMT
ADD alpine-minirootfs-3.24.1-armhf.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:25 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:14:43 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:14:44 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:17:47 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:17:47 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:17:47 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:17:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:17:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:17:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:17:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:17:47 GMT
USER memcache
# Tue, 16 Jun 2026 00:17:47 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:17:47 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3c4836a46d600cfe9a422adf7a80205cb534097e6213325e0176c51f6e5cc02e`  
		Last Modified: Sun, 14 Jun 2026 06:44:57 GMT  
		Size: 3.6 MB (3553450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e732a60042adf5cff5fe4fe0de83f937f6e5c8896500f7023e8bf68ed0670d65`  
		Last Modified: Tue, 16 Jun 2026 00:17:51 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad86d1fea29db061a5ae896a0a595b144edcdb4af59deac2b75b0fb8f5fa2d4c`  
		Last Modified: Tue, 16 Jun 2026 00:17:50 GMT  
		Size: 102.6 KB (102624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f26dd2445dbf4d5624417ca290f5ae2e5774fa7fec4f5655cd2377ee3147e4`  
		Last Modified: Tue, 16 Jun 2026 00:17:51 GMT  
		Size: 1.9 MB (1915730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080a186f0ca6beb06a5ce4a86fbc71f5b9995713fcc899c73f995f251ef7c987`  
		Last Modified: Tue, 16 Jun 2026 00:17:51 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c4d4f455f9a2b633cca28e3aa2190e4c42ca83ca6e3ea88ea4abe16944d238`  
		Last Modified: Tue, 16 Jun 2026 00:17:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:d6b7abf6ef34abf12ab2c7f84bd29ac2461eb3271d1c4070456ed9b94e4b41a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43a767571287c8ca227e321ee8d65f9da82e558098bedbb15888434dcc1ce9fa`

```dockerfile
```

-	Layers:
	-	`sha256:1794ccef4392c0db4ba36ad7fde22cdacbda40f4d56f0adbef802163c87e066c`  
		Last Modified: Tue, 16 Jun 2026 00:17:51 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42-alpine3.24` - linux; arm variant v7

```console
$ docker pull memcached@sha256:848c5e0ced69b802cca72c23bec05a4c6f23136212a4a1d5cc22b7c8f0154bf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:286f62a53a8947036e39f2b79567b31d38309fd84c7a39e43de8c5f9817a2f64`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:26 GMT
ADD alpine-minirootfs-3.24.1-armv7.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:26 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:17:59 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:17:59 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:20:56 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:20:56 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:20:56 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:20:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:20:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:20:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:20:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:20:56 GMT
USER memcache
# Tue, 16 Jun 2026 00:20:56 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:20:56 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bc03a9e5b4dd452551f246e199537fe7afc1765f53f510bc81d26df9845e4008`  
		Last Modified: Sun, 14 Jun 2026 06:45:22 GMT  
		Size: 3.3 MB (3260615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f0249bacfc8953b72899bf7b6c904c8750482fce4c93108f57b2c64228b279`  
		Last Modified: Tue, 16 Jun 2026 00:21:00 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95e1b321ffc31d01e766d5d1d054967d613940563406fc54ee981926b7f6049`  
		Last Modified: Tue, 16 Jun 2026 00:21:01 GMT  
		Size: 92.4 KB (92366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce112e60c1b15077277c233a7707831818dff0a15f1fc977ebebc93f817dad43`  
		Last Modified: Tue, 16 Jun 2026 00:21:01 GMT  
		Size: 1.9 MB (1875183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32fa6ed5b14fd6fcf96a7cde2996063f10b8efe802c386479288a232af826027`  
		Last Modified: Tue, 16 Jun 2026 00:21:01 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6648f8180a4eea1f5197f2fa2d356fbbf4e5f65345e189e720e227af64a5e31`  
		Last Modified: Tue, 16 Jun 2026 00:21:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:59387f31eff7cfb3166c5e6d4bad92e255705affcc15c84c4a06c86ecb1a9890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:174eb460b1df4523a4f71ba5a996f2285fa845fe8ef76d2df3ea8c4962c6b6ca`

```dockerfile
```

-	Layers:
	-	`sha256:4ff5e70775e819cab551295c56b58fdb0c44c105cdc4f72247e3968accd2ab2f`  
		Last Modified: Tue, 16 Jun 2026 00:21:00 GMT  
		Size: 94.3 KB (94315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00f10e1301c7e61396658f7e3ed330e400a9f304c6a0323de8ff644aba987474`  
		Last Modified: Tue, 16 Jun 2026 00:21:01 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42-alpine3.24` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:33261748facce282dbe4dbb4d9f875139680fce4cefc13cb9ad8e1ced23f9557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6250475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1614bb2865c8f849c2bc5bf77703a1ab711695c607a8bc6edb013a076ec16d6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:20 GMT
ADD alpine-minirootfs-3.24.1-aarch64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:20 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:13:18 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:13:18 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:16:06 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:16:06 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:16:06 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:16:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:16:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:16:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:16:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:16:06 GMT
USER memcache
# Tue, 16 Jun 2026 00:16:06 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:16:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5de55e5ef9c033997441461efe7ba23a986db059c0bb78b38f84ee0d72b99167`  
		Last Modified: Sun, 14 Jun 2026 06:44:31 GMT  
		Size: 4.2 MB (4183037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5faa19f06c4d5e26332739c7f08fd3dcd2c81817471c62029a6d99af6be8748`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377a35d28f00766e2679c788b95b0a67b9aa5a76c8ef701a2a9604e2a00c3b46`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 121.8 KB (121841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0b819e89558d70f1401ca58cbc19c58ae13e15be8184fd9b2733e022f318a4`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 1.9 MB (1944247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca539cef48ff8c3f723ab23506b6786c9ed26a9cac713601b71de2dc775d26a`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c4c456deed244daa6d7076f40a1cf0364d294059bb43e533677a89027843b15`  
		Last Modified: Tue, 16 Jun 2026 00:16:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:4d25960abc53b5ba1896b8f5ee04ba5ac1389900ab9b413eb62285af7281aedb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d1a4b7ad428a08c8a174d5ecd9763d530e849f54a2d9b90aef934e54b9477d4`

```dockerfile
```

-	Layers:
	-	`sha256:9c0a8e5e07390fae6abe9204450009671011c4d2d5aa5fe4afdd82324fdb49b9`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 94.4 KB (94351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ee01158358d01c082867cf46a5225cf101013e4d5b7eae18fc7853e277ff0f4`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 20.7 KB (20727 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42-alpine3.24` - linux; 386

```console
$ docker pull memcached@sha256:5436d0ef6e12f2f8e454384ff4a703132b3fe820c41a55336f520bb5d1622574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5702329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8946be3d97c7b9825159f58cbf832b131c75cb90b3fb46a40d5429b9ffe32bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:19 GMT
ADD alpine-minirootfs-3.24.1-x86.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:19 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:13:59 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:13:59 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:16:45 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:16:45 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:16:45 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:16:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:16:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:16:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:16:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:16:46 GMT
USER memcache
# Tue, 16 Jun 2026 00:16:46 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:16:46 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f86df9d778509895efbf9363d8fcb0cbe0b772de536c7218e4c4c947f0be879f`  
		Last Modified: Sun, 14 Jun 2026 06:45:46 GMT  
		Size: 3.7 MB (3670141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043137360442e605bc150f28f20e1fa2d23d90131370bc405ad7d35309594491`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900ce6eeaece12033b12f1c8641c33dcf62ff2525584411911368cfcd0b38224`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 110.7 KB (110729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e8cc1c8f6bc6391eb1a43a46f0b55ca7845f824fc0f2fc7ae7587a7715814e`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 1.9 MB (1920111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d94f6e4d3be92188fc182a3557fe43af5bc9f3e768a7f265977743a56eea527e`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f8a19f18dfff271426de7a17ab6780788fa4345d5fa0120e6d03720d552bd4`  
		Last Modified: Tue, 16 Jun 2026 00:16:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:00dc6a7f29b7f2f5ac46fc5678b80c43c7b1e46b4ca3c84c5597034180aeb644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6de04019c7775544db9adbb4c4558d0e7c842c279e5d70532b2ac0b988ac1345`

```dockerfile
```

-	Layers:
	-	`sha256:80895f8f5e9c9b015e419096426322f4c86c33d55ca8860ee046b61d52782847`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 94.9 KB (94852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c69be8c1f82a066b46cc389712508e85c1dcd77e649c922dba46ace64b343ae`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42-alpine3.24` - linux; ppc64le

```console
$ docker pull memcached@sha256:c7857941a51b85b136781035703afcc8854a2d70fa2091208a51f8bb7e71f934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5998515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b02b2222212c64e444ac1a2227b19f0cfb1282c8a8ced386c1b79ae48c641b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:15 GMT
ADD alpine-minirootfs-3.24.1-ppc64le.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:15 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:15:37 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:15:38 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:18:22 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:18:22 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:18:22 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:18:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:18:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:18:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:18:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:18:22 GMT
USER memcache
# Tue, 16 Jun 2026 00:18:22 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:18:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3ebcdcd395ccee658b9200e4b27d7699e5d6ed9f6c1858dea12781aac519ff59`  
		Last Modified: Sun, 14 Jun 2026 06:46:36 GMT  
		Size: 3.8 MB (3813400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b108e2058722fb0fb5a9310e8ebe82ab4b9c021228a94b3125ba49d318e9667`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb8160ed736eda8513164d5d703082fb0c9af9e037472ab70a02579caa3eb99`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 126.3 KB (126252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5cb88dd03ce07ecf1613c2aff220fb392763d8f22edc900c4ad032ee7103d34`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 2.1 MB (2057508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a12fd57420ca797ab383c58a488044d324c4d43b3c94a848f86a0524ed3064b4`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1c0c7b7a77e9375d8a75fb825fa274d9127ca96de79107550517be29501c817`  
		Last Modified: Tue, 16 Jun 2026 00:18:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:851f463d4778539d5e4981f972420f9a57ec2559488f8a59fba6abab6065032f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:734dd3d91f2d6cf217233f7a9dacc3c20ff0590246adb790f95713fb21c115de`

```dockerfile
```

-	Layers:
	-	`sha256:c0d4c203ef9f66cf827ec62098d7801e1c49f1187e0fe047fd32fc2a3271f636`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 94.3 KB (94304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b734d170b5463fa77dd77072e06d51a28efe59a53600d47435b015ebcadae92`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42-alpine3.24` - linux; riscv64

```console
$ docker pull memcached@sha256:ba5bf40b4adc1fe04f32e2e239fa9c0020d4e89bf4079493f8bc11a92c8f4b51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5738070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d12fbf86d6880aaa9d517425d9cecddcf545ba87e577a039dea9ea99ad53d8a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 05:59:15 GMT
ADD alpine-minirootfs-3.24.1-riscv64.tar.gz / # buildkit
# Tue, 16 Jun 2026 05:59:15 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 08:28:27 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 19 Jun 2026 08:28:31 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 19 Jun 2026 08:41:52 GMT
ENV MEMCACHED_VERSION=1.6.42
# Fri, 19 Jun 2026 08:41:52 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Fri, 19 Jun 2026 08:41:52 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Fri, 19 Jun 2026 08:41:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 19 Jun 2026 08:41:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 08:41:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 19 Jun 2026 08:41:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 08:41:53 GMT
USER memcache
# Fri, 19 Jun 2026 08:41:53 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 19 Jun 2026 08:41:53 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c34e5222b29b86391cdae95b0473ef789493ff1a0068a3a30b5d66f544bd7cf6`  
		Last Modified: Sun, 14 Jun 2026 06:47:00 GMT  
		Size: 3.6 MB (3574358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e09d95a0f414638430c0cd3ecfdcce75606201917a27c7cb2ce1e34cb928b26a`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a5335c7af79a1b08af55862ba77644afdae5544d9a7871e45c91b364bd4f71d`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 108.9 KB (108888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3622a6ea71515db1ef566afdbb121daed1f408aacf1519f4173b40dabe2ae627`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 2.1 MB (2053467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1db0e3e31ca3f2830f5404436e92b1862a4078adefacacec09a9580a3ad0a2`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1463b0fd26a37659aaad7f99696e5213764ad03bb094f40836c3309713d7a60`  
		Last Modified: Fri, 19 Jun 2026 08:42:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:aadb3b9338400b87692f95e00931e43940f8d6ddd13f046bd256848dd825e458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bde4b5a4a468d795a5f58dd934b371adfe72cd2ae24e166e1258ad65aa455a56`

```dockerfile
```

-	Layers:
	-	`sha256:debb70180cf674562f7ca321270e3dfa350c5d1596c05dbfcc27b38c65652528`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 94.3 KB (94300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a895bbe0bfec24678c1c92ddd283cb7392e0e8d229f31c769a23c95224c0d371`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42-alpine3.24` - linux; s390x

```console
$ docker pull memcached@sha256:e1b640e8d192055e5c3ccd05b077776a0f4d35664191596f7a8230b2cd7ef0f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5823313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1ef6221f9c2854683b0633325a98a0e7a0d3b7d865b02d7cdf4c1d49d2e5090`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:21 GMT
ADD alpine-minirootfs-3.24.1-s390x.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:21 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:13:46 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:13:46 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:17:12 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:17:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:17:12 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:17:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:17:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:17:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:17:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:17:12 GMT
USER memcache
# Tue, 16 Jun 2026 00:17:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:17:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:da43be6afaaa3ec1b607461ce64380942a6d76c3d52cda4337b0770d9a96fa89`  
		Last Modified: Sun, 14 Jun 2026 06:47:25 GMT  
		Size: 3.7 MB (3709320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757d04238e02c9bbe1cfd4030cc19e29421650a1b1562a8ca4090d90e9ae17b0`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1949e0fa71fc91bebf4f2e4293108b27de8357d98f98b673bc4f3ed1980b52c`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 114.3 KB (114289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f0e22966bce79fbc8a20f7c27aa07ce63229bb50181319c810ca29f1fb4032`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 2.0 MB (1998350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15eb5e912ef8ec6e3abe76c361cdddb568d20a60be21be379d4d8d7d0ebaa11e`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a549d59ad0d4761ac6f4cca272c4bea521471ed091d0e79143bfda8ff29cf9ce`  
		Last Modified: Tue, 16 Jun 2026 00:17:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:6dbf7c8a98f02a949769403ad1c92583b34a28dccc66b7d83d91863785a6dad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a89d23372d19daf2d6d4e1c4de732f7864316ed5e7713b1103918303873683e`

```dockerfile
```

-	Layers:
	-	`sha256:099ab2d711ef73783b01895824a4664c7d65e2a333e81237b4766cf053a8f6f0`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 94.2 KB (94246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0eccbabf44891af00e622624c5cfd5a295656f82f1c15073b240ac34d47af96c`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.42-trixie`

```console
$ docker pull memcached@sha256:85c0ab87f71b8b3ade708271177a8e5efca5e93c00287b6f25a2d74a27180bfa
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

### `memcached:1.6.42-trixie` - linux; amd64

```console
$ docker pull memcached@sha256:09ac4118d89005e47ef3118221840c62f0fa909a2bee07ff571ae1ae59d9a79b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32204821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ad15119e1f73d99f3fbdc56187ea014f4fae2c8fcbe215c259f2fb2b387aefa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:23:00 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 11 Jun 2026 00:23:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:25:47 GMT
ENV MEMCACHED_VERSION=1.6.42
# Thu, 11 Jun 2026 00:25:47 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Thu, 11 Jun 2026 00:25:47 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Thu, 11 Jun 2026 00:25:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 11 Jun 2026 00:25:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:25:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 11 Jun 2026 00:25:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:25:47 GMT
USER memcache
# Thu, 11 Jun 2026 00:25:47 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 11 Jun 2026 00:25:47 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7883ff600bb4cc730c755ccb8be3f5a06371865abe00be70037283c04f4f3f5`  
		Last Modified: Thu, 11 Jun 2026 00:25:53 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d73a0d6b79b50aa2429aebc30b68c38fb0fb43a4a597ce0dd3936605fbb8912e`  
		Last Modified: Thu, 11 Jun 2026 00:25:53 GMT  
		Size: 136.7 KB (136685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5716730726452d6a54ff03d59c7dffbb7ed4f05836877734acf92f7a0512d6a9`  
		Last Modified: Thu, 11 Jun 2026 00:25:53 GMT  
		Size: 2.3 MB (2281206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f338318b7809e3c4be59b7eccaa1e5387cdbe8015c49eac3267097258c54ae89`  
		Last Modified: Thu, 11 Jun 2026 00:25:53 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ca13d7300d84ca43fcce2aa8304787015f83333e041c81c04796354eadce6b`  
		Last Modified: Thu, 11 Jun 2026 00:25:54 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:3d476e3ec28b0dda5046a3223b0e5a8c9ab8dec20bb294a8853da81d828c154d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e2358f67931681260618f406ea3e0032f17f7a82b2a7d36e5511e6413a7133f`

```dockerfile
```

-	Layers:
	-	`sha256:9cb94c17b8cb82e97f6ad217227fa08e25e0fdc9b96fd2fe418e0acc53911305`  
		Last Modified: Thu, 11 Jun 2026 00:25:53 GMT  
		Size: 2.0 MB (2008368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f8a18d24b8d75bd4b8d856878db21e4d4df7e3e553b9d72d0156bbe58c869d3`  
		Last Modified: Thu, 11 Jun 2026 00:25:53 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42-trixie` - linux; arm variant v5

```console
$ docker pull memcached@sha256:f059b77d971253090e3862e28d374840935b5c06467230e9bea207fdb6ef3bf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30316631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c99754215fd2490daf10c8c1046bee3ab237e1e95bd4b46ef0610ca9d1c9badc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:19:47 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 11 Jun 2026 00:19:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:23:08 GMT
ENV MEMCACHED_VERSION=1.6.42
# Thu, 11 Jun 2026 00:23:08 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Thu, 11 Jun 2026 00:23:08 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Thu, 11 Jun 2026 00:23:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 11 Jun 2026 00:23:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:23:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 11 Jun 2026 00:23:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:23:08 GMT
USER memcache
# Thu, 11 Jun 2026 00:23:08 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 11 Jun 2026 00:23:08 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ed883f3fd95b7edef302d7ca9520eefdae280af081509bd7e9e5b5ff8f4cda7c`  
		Last Modified: Wed, 10 Jun 2026 23:41:17 GMT  
		Size: 28.0 MB (27959200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e92527947bdcc341ab63777422e7409751516a8bc5ffc61040d76b72e7d58c`  
		Last Modified: Thu, 11 Jun 2026 00:23:14 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c52c9bd0c151ce908cf5e8c55694b4a321a916d3053e9e4cd3b06837e55f325`  
		Last Modified: Thu, 11 Jun 2026 00:23:14 GMT  
		Size: 144.2 KB (144156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ec2615dd4e79e84378f7223c9d7c70a6cdfb8835717c19cadbab17a726210d`  
		Last Modified: Thu, 11 Jun 2026 00:23:14 GMT  
		Size: 2.2 MB (2211763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4249a738c6e8e951ca0bf1608e335442f8f50ff9fe57a524b1bdb472e59ed1`  
		Last Modified: Thu, 11 Jun 2026 00:23:14 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab171fa641968acda113ed8ec0cbff5159a4895efed9c4e08bb6e466a40fb5ce`  
		Last Modified: Thu, 11 Jun 2026 00:23:15 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:a7356b3e73eada1ea16535f45e9a297b7913adfb103e9df5d0a2ee333c58f443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c75fc3f8c74e188d3585642b303189b73ae78c14b089bd14f0d37da2b085f25`

```dockerfile
```

-	Layers:
	-	`sha256:5a953398782781fbd31e5d1fb67c1cdeb82c91397fb27ce32b9d756cc938a03a`  
		Last Modified: Thu, 11 Jun 2026 00:23:14 GMT  
		Size: 2.0 MB (2011371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aeae6ddb09b0b52fdf1e1db9b67dfa04fba888fbba5c54b1b7e30ecbd56dafde`  
		Last Modified: Thu, 11 Jun 2026 00:23:14 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42-trixie` - linux; arm variant v7

```console
$ docker pull memcached@sha256:7b20950329f422c7b322057fe1f944f98589cf937e5e65118b6d4bb241436ffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28513288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5d65e3287f7256814db41a73f2978df2252f6ac399369fe1a7a3eb1c4ceb3e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:21:55 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 11 Jun 2026 00:21:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:25:06 GMT
ENV MEMCACHED_VERSION=1.6.42
# Thu, 11 Jun 2026 00:25:06 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Thu, 11 Jun 2026 00:25:06 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Thu, 11 Jun 2026 00:25:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 11 Jun 2026 00:25:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:25:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 11 Jun 2026 00:25:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:25:06 GMT
USER memcache
# Thu, 11 Jun 2026 00:25:06 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 11 Jun 2026 00:25:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4bd6ddea06d5009ee47ddb0f254a2569aff0230c005869ebd416b20295d945c0`  
		Last Modified: Wed, 10 Jun 2026 23:42:34 GMT  
		Size: 26.2 MB (26211004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bcac116a5bd6f8c4ba910742373294134be4443587cce918db3492895262e16`  
		Last Modified: Thu, 11 Jun 2026 00:25:12 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af6a74cecf5734c352e3c2ea5fb348246cfe77549b6cb2afe3116aaf39983ff8`  
		Last Modified: Thu, 11 Jun 2026 00:25:12 GMT  
		Size: 135.4 KB (135382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6189c46b05f5cdb39083034f258358c5472cc6824a25a7dc8a8f60ae58891116`  
		Last Modified: Thu, 11 Jun 2026 00:25:12 GMT  
		Size: 2.2 MB (2165385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfeedbf1b9c25a3c29e32962704f935689b2b60c4096315dbee3365a9cec4dc0`  
		Last Modified: Thu, 11 Jun 2026 00:25:12 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0309704e28c847b1dd0249a490a5774838b3d27bf059481108e0f1a300efd4ae`  
		Last Modified: Thu, 11 Jun 2026 00:25:13 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:84793c5cdc418c73cc53c1dcdf3ebaf9d1c2a7910ec63c85d179a691e05f1ddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0981cd8d43f93fb996bbc87f0659a7c3a7163d74a5c84503eb77588ed240010c`

```dockerfile
```

-	Layers:
	-	`sha256:39acaedd56024e59130ae654692bdff06d01b71719567ede3d9ece539679150e`  
		Last Modified: Thu, 11 Jun 2026 00:25:13 GMT  
		Size: 2.0 MB (2009828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ada0017eed4fa0f3db9a2e1669d0eb74e2908e65a483af6819df971d18d767a`  
		Last Modified: Thu, 11 Jun 2026 00:25:12 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42-trixie` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:a36eca5b5840c718ca41526a871fd751dc96965f182778a7631a0c2896c3f44a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32566560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31c7500da651c7c5945a2db8b00248c02ad2947b4eccb66b464759cd6f4ea2c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:23:08 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 11 Jun 2026 00:23:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:26:08 GMT
ENV MEMCACHED_VERSION=1.6.42
# Thu, 11 Jun 2026 00:26:08 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Thu, 11 Jun 2026 00:26:08 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Thu, 11 Jun 2026 00:26:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 11 Jun 2026 00:26:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:26:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 11 Jun 2026 00:26:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:26:08 GMT
USER memcache
# Thu, 11 Jun 2026 00:26:08 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 11 Jun 2026 00:26:08 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb68ad832950ffa1d5fe24c7e7ee4e061b358d6bcb14dfdb1bb2dec4c557f7a2`  
		Last Modified: Thu, 11 Jun 2026 00:26:15 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f6f966199cad211cd492fc65c6c927fde3a05499bdd9a2112d65deb706cfbc6`  
		Last Modified: Thu, 11 Jun 2026 00:26:14 GMT  
		Size: 153.5 KB (153481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3314b48b94577865e96641c557d5048167254c141db1725db6a5b7a623b68f7b`  
		Last Modified: Thu, 11 Jun 2026 00:26:15 GMT  
		Size: 2.3 MB (2263038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e33e48bcfd48ec271ffa516b5c3b03458185abfb31596aca0b854e9c9367fb9`  
		Last Modified: Thu, 11 Jun 2026 00:26:15 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb41e83cd817b17ff4c2b62ce482681096f6783b2a32be0407cada277d4f293`  
		Last Modified: Thu, 11 Jun 2026 00:26:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:0253549da149222537eeb2e51a1b411b7662c20d8c8964e71967cf670ce9c992
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af9894c8fa8e920a07bf631bed91c9b67398338986159408229a8da050b21c3b`

```dockerfile
```

-	Layers:
	-	`sha256:a11c09037e68845f3c8c01efb996710c3b2d21ba868a98c3ba2582a28d0f1047`  
		Last Modified: Thu, 11 Jun 2026 00:26:15 GMT  
		Size: 2.0 MB (2008676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40468c38b6f60c4625c352d5bdc83ea61510da0efeb2542777603da191a5d2fa`  
		Last Modified: Thu, 11 Jun 2026 00:26:14 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42-trixie` - linux; 386

```console
$ docker pull memcached@sha256:e134667b3198bc9f05962d9bb97cf359ab04c31cb8d11c75e2683de54cebd46e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33675616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cba4eb3d3e82545273aa5ff6f0e6f7bf2b1240176b9489d2315fcf290b9c49a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:18:22 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 11 Jun 2026 00:18:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:21:26 GMT
ENV MEMCACHED_VERSION=1.6.42
# Thu, 11 Jun 2026 00:21:26 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Thu, 11 Jun 2026 00:21:26 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Thu, 11 Jun 2026 00:21:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 11 Jun 2026 00:21:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:21:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 11 Jun 2026 00:21:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:21:26 GMT
USER memcache
# Thu, 11 Jun 2026 00:21:26 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 11 Jun 2026 00:21:26 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:720f951a68f4f9ab464e52b53cf88cfb86bc876b3f00956d000420777ab93c0c`  
		Last Modified: Wed, 10 Jun 2026 23:40:30 GMT  
		Size: 31.3 MB (31301194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2607fca8a1b7fbebf74214d1b33f4f0a54aed5fef2bed18ddc89836a7d00e04b`  
		Last Modified: Thu, 11 Jun 2026 00:21:31 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4620fc98d601bc463a1a505fb0ecf42cb42fa76088d5e80dee41474c74f39f1`  
		Last Modified: Thu, 11 Jun 2026 00:21:32 GMT  
		Size: 147.5 KB (147511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a4c97894b05376111399fa19e7429f36d493cb528c53cb81318a2920d5a954`  
		Last Modified: Thu, 11 Jun 2026 00:21:32 GMT  
		Size: 2.2 MB (2225398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f4a764af02d7ba61dd0909ddb429ba92c9a367243a225936fd625fda113340`  
		Last Modified: Thu, 11 Jun 2026 00:21:32 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52e82109e627ebc0d88a9f7c357b97f14b8ac06bdab5d0b6aa50c3b958a13a8`  
		Last Modified: Thu, 11 Jun 2026 00:21:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:6670b6485b54bcae32ddeda5c2d1764d0ee2066f036d0c17f2cc89734f0be8c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d0aef4dacfecea9e8dbc20498736f77e48bf5106eb60bcfa08c1e81a5c4f06c`

```dockerfile
```

-	Layers:
	-	`sha256:0ebdf5fe0d474785e4448d36043967631fb650ec7b52bd865126a7360978a2ea`  
		Last Modified: Thu, 11 Jun 2026 00:21:32 GMT  
		Size: 2.0 MB (2005525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f257ddeb15df7a03d8e7bb57e01531d894c998af32f33cb528199914bd8f6e1c`  
		Last Modified: Thu, 11 Jun 2026 00:21:32 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42-trixie` - linux; ppc64le

```console
$ docker pull memcached@sha256:25e41a95392ee3c63e35711fec0648fbedc92c6be718456ad8fb89ab66f4e825
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36762178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a04e55188a4c60d5cd8eb00b50628fd87658d0d1814097b40417d71b18479e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 02:36:51 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 11 Jun 2026 02:36:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:59:49 GMT
ENV MEMCACHED_VERSION=1.6.42
# Thu, 11 Jun 2026 02:59:49 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Thu, 11 Jun 2026 02:59:49 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Thu, 11 Jun 2026 02:59:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 11 Jun 2026 02:59:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 02:59:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 11 Jun 2026 02:59:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 02:59:50 GMT
USER memcache
# Thu, 11 Jun 2026 02:59:50 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 11 Jun 2026 02:59:50 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9d6b2e320e2b74843186d830e8202c50ebfaeccf823d239e3e3e349a8a508d80`  
		Last Modified: Thu, 11 Jun 2026 00:24:42 GMT  
		Size: 33.6 MB (33606340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d389c79e93b7c7b3cc2a8226edeb6460d8101e245642213048c1a187d08a935d`  
		Last Modified: Thu, 11 Jun 2026 03:00:07 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7bb22e37f822a0e94fa24cd439d7666c214637b0d59c384dd19e12674c74a82`  
		Last Modified: Thu, 11 Jun 2026 03:00:07 GMT  
		Size: 170.4 KB (170363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82cbb5c5e79cdcec98bd562e1a62768994b805ff7d805b6b75b5bf0e349cff8`  
		Last Modified: Thu, 11 Jun 2026 03:00:06 GMT  
		Size: 3.0 MB (2983963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e60c6f3b8886967bbbabece38cfe74eccdfde98cdae42045a33c5b2b29fd6da`  
		Last Modified: Thu, 11 Jun 2026 03:00:08 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc87d370da3b9877481bf9620bda982328b4d722812ec3e77a7b4c50d016eb33`  
		Last Modified: Thu, 11 Jun 2026 03:00:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:0101df893b4af64daa7ee54d012d7b8682b6c1a9ad1d85700cf8ff269664b19e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b06e6f43b0b95c657fb0043338f12918e63fcac640df48783c49ac29092afb0b`

```dockerfile
```

-	Layers:
	-	`sha256:8ed9fcb43f9f08fb8702ae2709d918b6370866fb4697ddf04b93f42080b23d94`  
		Last Modified: Thu, 11 Jun 2026 03:00:08 GMT  
		Size: 2.0 MB (2011969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c6915dddb9ee13a9cd4156b07c521335c76c9687dcb3a08e66e147af9d99453`  
		Last Modified: Thu, 11 Jun 2026 03:00:06 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42-trixie` - linux; riscv64

```console
$ docker pull memcached@sha256:918c03d1a36c36f13b67e3fbf100f93adad50fbbb452fecc3769db0b8cde487c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30626726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1c8f5f48c37fb2ef15e785c080f746aec65afab782672de8b6a63bd88942e41`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1781049600'
# Fri, 12 Jun 2026 00:28:54 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 12 Jun 2026 00:29:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jun 2026 00:42:57 GMT
ENV MEMCACHED_VERSION=1.6.42
# Fri, 12 Jun 2026 00:42:57 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Fri, 12 Jun 2026 00:42:57 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Fri, 12 Jun 2026 00:42:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 12 Jun 2026 00:42:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Jun 2026 00:42:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 12 Jun 2026 00:42:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2026 00:42:57 GMT
USER memcache
# Fri, 12 Jun 2026 00:42:57 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 12 Jun 2026 00:42:57 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0b510fe8545cab831b696965b5a825649c5c945581e912d31a08a0b30ff940c0`  
		Last Modified: Thu, 11 Jun 2026 03:01:06 GMT  
		Size: 28.3 MB (28282305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35e7a152e660b7a61f448299ac325c28198a870bc53d54cd2584d111c3cef30`  
		Last Modified: Fri, 12 Jun 2026 00:43:44 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d26b2af070be1166e165d4bd1eb073a685622ddb1edb5cf4382cb7825faa21a`  
		Last Modified: Fri, 12 Jun 2026 00:43:44 GMT  
		Size: 133.1 KB (133071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ac4d08e6c19ea726574dc4cd56f4d39216f427cdfd9d6e19c91b06583e6630`  
		Last Modified: Fri, 12 Jun 2026 00:43:44 GMT  
		Size: 2.2 MB (2209833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:039ac44117911671ad0fca8638fa93282ad5865273a55e1328d3180ac5c4f463`  
		Last Modified: Fri, 12 Jun 2026 00:43:44 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65787f51c4d435ccf6c4c9c11e27fe642bd5af3fdd4489e11005614f51c21c29`  
		Last Modified: Fri, 12 Jun 2026 00:43:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:5db8b7d0f9f634b02f9f4dfb45d2f0d3fb2ef1778c3e52058327cd5dec31ebce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0de6ff12136279a3005dae5ce29967a780efb19d8a50b71f33b8153d38859c49`

```dockerfile
```

-	Layers:
	-	`sha256:256f6cfcbc556a40776a58fddd91ccacf0870ab5955a42e7e3ea23601ff76633`  
		Last Modified: Fri, 12 Jun 2026 00:43:44 GMT  
		Size: 2.0 MB (2002332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdfa564b06be9c36a9d81da00994136c858ca65d81762277469168a418a9c9fa`  
		Last Modified: Fri, 12 Jun 2026 00:43:44 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42-trixie` - linux; s390x

```console
$ docker pull memcached@sha256:75f4e343898a5a326a82f6560f0efdd5d11c5aea7a710327cdfd400ac3244341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32291904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd9e841717be4c79746136574299d1a6552f88fe8566606318efb07377ef20c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:19:32 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 11 Jun 2026 00:19:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:22:55 GMT
ENV MEMCACHED_VERSION=1.6.42
# Thu, 11 Jun 2026 00:22:55 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Thu, 11 Jun 2026 00:22:55 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Thu, 11 Jun 2026 00:22:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 11 Jun 2026 00:22:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:22:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 11 Jun 2026 00:22:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:22:55 GMT
USER memcache
# Thu, 11 Jun 2026 00:22:55 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 11 Jun 2026 00:22:55 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:760dcf74fdfe93300ce15b5b23adf9aa4af45b6ba9d69925863198f64881a537`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 29.9 MB (29851354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159eeccf7c6aa583901267e3c00bf9c124c32be82a1074722d2be0b547fee632`  
		Last Modified: Thu, 11 Jun 2026 00:23:05 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d08bb26724ea31dfaf95eb6c1647b7686671b3869632300d6056a05c3532bd`  
		Last Modified: Thu, 11 Jun 2026 00:23:05 GMT  
		Size: 140.5 KB (140545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b341a8e7ca68a391e79c556246f3f0b81e4a5e747fed517e274d78f49faa30`  
		Last Modified: Thu, 11 Jun 2026 00:23:05 GMT  
		Size: 2.3 MB (2298492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff1b1dd9080cb995308882030f9579f4c5bf2af5b26b7270d6682de75f6e6d5`  
		Last Modified: Thu, 11 Jun 2026 00:23:05 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075343c77f8c8b9a1bb9fe079e853c0e4628b60f1fff7d8dce82d38c3a344bf8`  
		Last Modified: Thu, 11 Jun 2026 00:23:06 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:1f977b6725f519f48d75ffc92c711df863d7c0e4a1d1f0c5a5bc6605533f35e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1104b534613c8d2cc0544b9adf96821b4f7f623262ef6ddc425f13fa94427850`

```dockerfile
```

-	Layers:
	-	`sha256:66bb879abbe8f943d53561fcf4f4262e1b78fb31b6aa3fdac560ffdc45e3d4b5`  
		Last Modified: Thu, 11 Jun 2026 00:23:05 GMT  
		Size: 2.0 MB (2009805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e448bf5a0443ce0296756453f8bca10e0ec97ebc01576de74a28f60b78299f2b`  
		Last Modified: Thu, 11 Jun 2026 00:23:05 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine`

```console
$ docker pull memcached@sha256:7381333da6d6ae06e02d8dfc87ee6f2c7cd0a19f7ba048d5efc538d2100e2208
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
$ docker pull memcached@sha256:ce375dd48f976d33bf35beb966cc37f202fd840a90891e58b9e71171fc74174d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5921579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19d284e7a8445d8dc70e97c673a8a0175d18f39d5336ccbdfa8b240c0ef3ce4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:29 GMT
ADD alpine-minirootfs-3.24.1-x86_64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:15:18 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:15:18 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:17:54 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:17:54 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:17:54 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:17:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:17:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:17:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:17:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:17:54 GMT
USER memcache
# Tue, 16 Jun 2026 00:17:54 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:17:54 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:55afa1ecc21d2bb5e5045f32dafee56272ffd89860bac26f6c32123439af26a4`  
		Last Modified: Sun, 14 Jun 2026 06:44:06 GMT  
		Size: 3.8 MB (3846391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb73756dcbbebc424eab53d3adda4d9f64001e7a91272a7b2a834622c08b093`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f0d6a5291334f2b54ec652193cd4e17ee22455b2f3ff3bd9b66acff6436c7b`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 106.1 KB (106066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ac11a8307528096ac745e0ef681b64854bbd012ffdfbce85587153eec73563`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 2.0 MB (1967772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3626493aad85d70a212bc66e9d45db8aef43b4bc662259563f916398165f1e64`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cdcd3f20e3aa439838f5491e6f457a42bad6c80ed9b099313bf79b57a721ea8`  
		Last Modified: Tue, 16 Jun 2026 00:18:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:bb948800301f1cae8e18e317f2b9e85636c86c4a1924ee85e125da37cb1333e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c3e084937eb543038244e151b03b8d9a0dce0b4d5bf87c2d471fa397ed5702`

```dockerfile
```

-	Layers:
	-	`sha256:9d05a792212c92363a76bb6a8205a6e7f386113b3efc1b5d600f93d4e237c975`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 94.9 KB (94897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee0e7e70ef03205f55c68bc1b74ac7854183aee4e871112794975dc852761b19`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:4b144cdbc67c11035b3d0f0c812b590ee694977f2f6a32321e538237bd2f841c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5573158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e9bb70df1535a2f8ca960f733a4404cbde900a13156a1f4446c2fd110258e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:25 GMT
ADD alpine-minirootfs-3.24.1-armhf.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:25 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:14:43 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:14:44 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:17:47 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:17:47 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:17:47 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:17:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:17:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:17:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:17:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:17:47 GMT
USER memcache
# Tue, 16 Jun 2026 00:17:47 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:17:47 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3c4836a46d600cfe9a422adf7a80205cb534097e6213325e0176c51f6e5cc02e`  
		Last Modified: Sun, 14 Jun 2026 06:44:57 GMT  
		Size: 3.6 MB (3553450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e732a60042adf5cff5fe4fe0de83f937f6e5c8896500f7023e8bf68ed0670d65`  
		Last Modified: Tue, 16 Jun 2026 00:17:51 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad86d1fea29db061a5ae896a0a595b144edcdb4af59deac2b75b0fb8f5fa2d4c`  
		Last Modified: Tue, 16 Jun 2026 00:17:50 GMT  
		Size: 102.6 KB (102624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f26dd2445dbf4d5624417ca290f5ae2e5774fa7fec4f5655cd2377ee3147e4`  
		Last Modified: Tue, 16 Jun 2026 00:17:51 GMT  
		Size: 1.9 MB (1915730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080a186f0ca6beb06a5ce4a86fbc71f5b9995713fcc899c73f995f251ef7c987`  
		Last Modified: Tue, 16 Jun 2026 00:17:51 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c4d4f455f9a2b633cca28e3aa2190e4c42ca83ca6e3ea88ea4abe16944d238`  
		Last Modified: Tue, 16 Jun 2026 00:17:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:d6b7abf6ef34abf12ab2c7f84bd29ac2461eb3271d1c4070456ed9b94e4b41a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43a767571287c8ca227e321ee8d65f9da82e558098bedbb15888434dcc1ce9fa`

```dockerfile
```

-	Layers:
	-	`sha256:1794ccef4392c0db4ba36ad7fde22cdacbda40f4d56f0adbef802163c87e066c`  
		Last Modified: Tue, 16 Jun 2026 00:17:51 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:848c5e0ced69b802cca72c23bec05a4c6f23136212a4a1d5cc22b7c8f0154bf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:286f62a53a8947036e39f2b79567b31d38309fd84c7a39e43de8c5f9817a2f64`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:26 GMT
ADD alpine-minirootfs-3.24.1-armv7.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:26 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:17:59 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:17:59 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:20:56 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:20:56 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:20:56 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:20:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:20:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:20:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:20:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:20:56 GMT
USER memcache
# Tue, 16 Jun 2026 00:20:56 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:20:56 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bc03a9e5b4dd452551f246e199537fe7afc1765f53f510bc81d26df9845e4008`  
		Last Modified: Sun, 14 Jun 2026 06:45:22 GMT  
		Size: 3.3 MB (3260615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f0249bacfc8953b72899bf7b6c904c8750482fce4c93108f57b2c64228b279`  
		Last Modified: Tue, 16 Jun 2026 00:21:00 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95e1b321ffc31d01e766d5d1d054967d613940563406fc54ee981926b7f6049`  
		Last Modified: Tue, 16 Jun 2026 00:21:01 GMT  
		Size: 92.4 KB (92366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce112e60c1b15077277c233a7707831818dff0a15f1fc977ebebc93f817dad43`  
		Last Modified: Tue, 16 Jun 2026 00:21:01 GMT  
		Size: 1.9 MB (1875183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32fa6ed5b14fd6fcf96a7cde2996063f10b8efe802c386479288a232af826027`  
		Last Modified: Tue, 16 Jun 2026 00:21:01 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6648f8180a4eea1f5197f2fa2d356fbbf4e5f65345e189e720e227af64a5e31`  
		Last Modified: Tue, 16 Jun 2026 00:21:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:59387f31eff7cfb3166c5e6d4bad92e255705affcc15c84c4a06c86ecb1a9890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:174eb460b1df4523a4f71ba5a996f2285fa845fe8ef76d2df3ea8c4962c6b6ca`

```dockerfile
```

-	Layers:
	-	`sha256:4ff5e70775e819cab551295c56b58fdb0c44c105cdc4f72247e3968accd2ab2f`  
		Last Modified: Tue, 16 Jun 2026 00:21:00 GMT  
		Size: 94.3 KB (94315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00f10e1301c7e61396658f7e3ed330e400a9f304c6a0323de8ff644aba987474`  
		Last Modified: Tue, 16 Jun 2026 00:21:01 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:33261748facce282dbe4dbb4d9f875139680fce4cefc13cb9ad8e1ced23f9557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6250475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1614bb2865c8f849c2bc5bf77703a1ab711695c607a8bc6edb013a076ec16d6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:20 GMT
ADD alpine-minirootfs-3.24.1-aarch64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:20 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:13:18 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:13:18 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:16:06 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:16:06 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:16:06 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:16:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:16:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:16:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:16:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:16:06 GMT
USER memcache
# Tue, 16 Jun 2026 00:16:06 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:16:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5de55e5ef9c033997441461efe7ba23a986db059c0bb78b38f84ee0d72b99167`  
		Last Modified: Sun, 14 Jun 2026 06:44:31 GMT  
		Size: 4.2 MB (4183037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5faa19f06c4d5e26332739c7f08fd3dcd2c81817471c62029a6d99af6be8748`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377a35d28f00766e2679c788b95b0a67b9aa5a76c8ef701a2a9604e2a00c3b46`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 121.8 KB (121841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0b819e89558d70f1401ca58cbc19c58ae13e15be8184fd9b2733e022f318a4`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 1.9 MB (1944247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca539cef48ff8c3f723ab23506b6786c9ed26a9cac713601b71de2dc775d26a`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c4c456deed244daa6d7076f40a1cf0364d294059bb43e533677a89027843b15`  
		Last Modified: Tue, 16 Jun 2026 00:16:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:4d25960abc53b5ba1896b8f5ee04ba5ac1389900ab9b413eb62285af7281aedb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d1a4b7ad428a08c8a174d5ecd9763d530e849f54a2d9b90aef934e54b9477d4`

```dockerfile
```

-	Layers:
	-	`sha256:9c0a8e5e07390fae6abe9204450009671011c4d2d5aa5fe4afdd82324fdb49b9`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 94.4 KB (94351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ee01158358d01c082867cf46a5225cf101013e4d5b7eae18fc7853e277ff0f4`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 20.7 KB (20727 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; 386

```console
$ docker pull memcached@sha256:5436d0ef6e12f2f8e454384ff4a703132b3fe820c41a55336f520bb5d1622574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5702329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8946be3d97c7b9825159f58cbf832b131c75cb90b3fb46a40d5429b9ffe32bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:19 GMT
ADD alpine-minirootfs-3.24.1-x86.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:19 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:13:59 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:13:59 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:16:45 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:16:45 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:16:45 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:16:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:16:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:16:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:16:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:16:46 GMT
USER memcache
# Tue, 16 Jun 2026 00:16:46 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:16:46 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f86df9d778509895efbf9363d8fcb0cbe0b772de536c7218e4c4c947f0be879f`  
		Last Modified: Sun, 14 Jun 2026 06:45:46 GMT  
		Size: 3.7 MB (3670141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043137360442e605bc150f28f20e1fa2d23d90131370bc405ad7d35309594491`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900ce6eeaece12033b12f1c8641c33dcf62ff2525584411911368cfcd0b38224`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 110.7 KB (110729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e8cc1c8f6bc6391eb1a43a46f0b55ca7845f824fc0f2fc7ae7587a7715814e`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 1.9 MB (1920111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d94f6e4d3be92188fc182a3557fe43af5bc9f3e768a7f265977743a56eea527e`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f8a19f18dfff271426de7a17ab6780788fa4345d5fa0120e6d03720d552bd4`  
		Last Modified: Tue, 16 Jun 2026 00:16:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:00dc6a7f29b7f2f5ac46fc5678b80c43c7b1e46b4ca3c84c5597034180aeb644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6de04019c7775544db9adbb4c4558d0e7c842c279e5d70532b2ac0b988ac1345`

```dockerfile
```

-	Layers:
	-	`sha256:80895f8f5e9c9b015e419096426322f4c86c33d55ca8860ee046b61d52782847`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 94.9 KB (94852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c69be8c1f82a066b46cc389712508e85c1dcd77e649c922dba46ace64b343ae`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:c7857941a51b85b136781035703afcc8854a2d70fa2091208a51f8bb7e71f934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5998515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b02b2222212c64e444ac1a2227b19f0cfb1282c8a8ced386c1b79ae48c641b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:15 GMT
ADD alpine-minirootfs-3.24.1-ppc64le.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:15 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:15:37 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:15:38 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:18:22 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:18:22 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:18:22 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:18:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:18:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:18:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:18:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:18:22 GMT
USER memcache
# Tue, 16 Jun 2026 00:18:22 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:18:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3ebcdcd395ccee658b9200e4b27d7699e5d6ed9f6c1858dea12781aac519ff59`  
		Last Modified: Sun, 14 Jun 2026 06:46:36 GMT  
		Size: 3.8 MB (3813400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b108e2058722fb0fb5a9310e8ebe82ab4b9c021228a94b3125ba49d318e9667`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb8160ed736eda8513164d5d703082fb0c9af9e037472ab70a02579caa3eb99`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 126.3 KB (126252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5cb88dd03ce07ecf1613c2aff220fb392763d8f22edc900c4ad032ee7103d34`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 2.1 MB (2057508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a12fd57420ca797ab383c58a488044d324c4d43b3c94a848f86a0524ed3064b4`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1c0c7b7a77e9375d8a75fb825fa274d9127ca96de79107550517be29501c817`  
		Last Modified: Tue, 16 Jun 2026 00:18:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:851f463d4778539d5e4981f972420f9a57ec2559488f8a59fba6abab6065032f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:734dd3d91f2d6cf217233f7a9dacc3c20ff0590246adb790f95713fb21c115de`

```dockerfile
```

-	Layers:
	-	`sha256:c0d4c203ef9f66cf827ec62098d7801e1c49f1187e0fe047fd32fc2a3271f636`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 94.3 KB (94304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b734d170b5463fa77dd77072e06d51a28efe59a53600d47435b015ebcadae92`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:ba5bf40b4adc1fe04f32e2e239fa9c0020d4e89bf4079493f8bc11a92c8f4b51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5738070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d12fbf86d6880aaa9d517425d9cecddcf545ba87e577a039dea9ea99ad53d8a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 05:59:15 GMT
ADD alpine-minirootfs-3.24.1-riscv64.tar.gz / # buildkit
# Tue, 16 Jun 2026 05:59:15 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 08:28:27 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 19 Jun 2026 08:28:31 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 19 Jun 2026 08:41:52 GMT
ENV MEMCACHED_VERSION=1.6.42
# Fri, 19 Jun 2026 08:41:52 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Fri, 19 Jun 2026 08:41:52 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Fri, 19 Jun 2026 08:41:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 19 Jun 2026 08:41:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 08:41:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 19 Jun 2026 08:41:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 08:41:53 GMT
USER memcache
# Fri, 19 Jun 2026 08:41:53 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 19 Jun 2026 08:41:53 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c34e5222b29b86391cdae95b0473ef789493ff1a0068a3a30b5d66f544bd7cf6`  
		Last Modified: Sun, 14 Jun 2026 06:47:00 GMT  
		Size: 3.6 MB (3574358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e09d95a0f414638430c0cd3ecfdcce75606201917a27c7cb2ce1e34cb928b26a`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a5335c7af79a1b08af55862ba77644afdae5544d9a7871e45c91b364bd4f71d`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 108.9 KB (108888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3622a6ea71515db1ef566afdbb121daed1f408aacf1519f4173b40dabe2ae627`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 2.1 MB (2053467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1db0e3e31ca3f2830f5404436e92b1862a4078adefacacec09a9580a3ad0a2`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1463b0fd26a37659aaad7f99696e5213764ad03bb094f40836c3309713d7a60`  
		Last Modified: Fri, 19 Jun 2026 08:42:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:aadb3b9338400b87692f95e00931e43940f8d6ddd13f046bd256848dd825e458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bde4b5a4a468d795a5f58dd934b371adfe72cd2ae24e166e1258ad65aa455a56`

```dockerfile
```

-	Layers:
	-	`sha256:debb70180cf674562f7ca321270e3dfa350c5d1596c05dbfcc27b38c65652528`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 94.3 KB (94300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a895bbe0bfec24678c1c92ddd283cb7392e0e8d229f31c769a23c95224c0d371`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; s390x

```console
$ docker pull memcached@sha256:e1b640e8d192055e5c3ccd05b077776a0f4d35664191596f7a8230b2cd7ef0f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5823313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1ef6221f9c2854683b0633325a98a0e7a0d3b7d865b02d7cdf4c1d49d2e5090`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:21 GMT
ADD alpine-minirootfs-3.24.1-s390x.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:21 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:13:46 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:13:46 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:17:12 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:17:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:17:12 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:17:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:17:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:17:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:17:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:17:12 GMT
USER memcache
# Tue, 16 Jun 2026 00:17:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:17:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:da43be6afaaa3ec1b607461ce64380942a6d76c3d52cda4337b0770d9a96fa89`  
		Last Modified: Sun, 14 Jun 2026 06:47:25 GMT  
		Size: 3.7 MB (3709320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757d04238e02c9bbe1cfd4030cc19e29421650a1b1562a8ca4090d90e9ae17b0`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1949e0fa71fc91bebf4f2e4293108b27de8357d98f98b673bc4f3ed1980b52c`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 114.3 KB (114289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f0e22966bce79fbc8a20f7c27aa07ce63229bb50181319c810ca29f1fb4032`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 2.0 MB (1998350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15eb5e912ef8ec6e3abe76c361cdddb568d20a60be21be379d4d8d7d0ebaa11e`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a549d59ad0d4761ac6f4cca272c4bea521471ed091d0e79143bfda8ff29cf9ce`  
		Last Modified: Tue, 16 Jun 2026 00:17:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:6dbf7c8a98f02a949769403ad1c92583b34a28dccc66b7d83d91863785a6dad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a89d23372d19daf2d6d4e1c4de732f7864316ed5e7713b1103918303873683e`

```dockerfile
```

-	Layers:
	-	`sha256:099ab2d711ef73783b01895824a4664c7d65e2a333e81237b4766cf053a8f6f0`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 94.2 KB (94246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0eccbabf44891af00e622624c5cfd5a295656f82f1c15073b240ac34d47af96c`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine3.24`

```console
$ docker pull memcached@sha256:7381333da6d6ae06e02d8dfc87ee6f2c7cd0a19f7ba048d5efc538d2100e2208
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

### `memcached:alpine3.24` - linux; amd64

```console
$ docker pull memcached@sha256:ce375dd48f976d33bf35beb966cc37f202fd840a90891e58b9e71171fc74174d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5921579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19d284e7a8445d8dc70e97c673a8a0175d18f39d5336ccbdfa8b240c0ef3ce4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:29 GMT
ADD alpine-minirootfs-3.24.1-x86_64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:15:18 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:15:18 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:17:54 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:17:54 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:17:54 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:17:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:17:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:17:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:17:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:17:54 GMT
USER memcache
# Tue, 16 Jun 2026 00:17:54 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:17:54 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:55afa1ecc21d2bb5e5045f32dafee56272ffd89860bac26f6c32123439af26a4`  
		Last Modified: Sun, 14 Jun 2026 06:44:06 GMT  
		Size: 3.8 MB (3846391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb73756dcbbebc424eab53d3adda4d9f64001e7a91272a7b2a834622c08b093`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f0d6a5291334f2b54ec652193cd4e17ee22455b2f3ff3bd9b66acff6436c7b`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 106.1 KB (106066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ac11a8307528096ac745e0ef681b64854bbd012ffdfbce85587153eec73563`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 2.0 MB (1967772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3626493aad85d70a212bc66e9d45db8aef43b4bc662259563f916398165f1e64`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cdcd3f20e3aa439838f5491e6f457a42bad6c80ed9b099313bf79b57a721ea8`  
		Last Modified: Tue, 16 Jun 2026 00:18:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:bb948800301f1cae8e18e317f2b9e85636c86c4a1924ee85e125da37cb1333e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c3e084937eb543038244e151b03b8d9a0dce0b4d5bf87c2d471fa397ed5702`

```dockerfile
```

-	Layers:
	-	`sha256:9d05a792212c92363a76bb6a8205a6e7f386113b3efc1b5d600f93d4e237c975`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 94.9 KB (94897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee0e7e70ef03205f55c68bc1b74ac7854183aee4e871112794975dc852761b19`  
		Last Modified: Tue, 16 Jun 2026 00:17:59 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.24` - linux; arm variant v6

```console
$ docker pull memcached@sha256:4b144cdbc67c11035b3d0f0c812b590ee694977f2f6a32321e538237bd2f841c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5573158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e9bb70df1535a2f8ca960f733a4404cbde900a13156a1f4446c2fd110258e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:25 GMT
ADD alpine-minirootfs-3.24.1-armhf.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:25 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:14:43 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:14:44 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:17:47 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:17:47 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:17:47 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:17:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:17:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:17:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:17:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:17:47 GMT
USER memcache
# Tue, 16 Jun 2026 00:17:47 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:17:47 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3c4836a46d600cfe9a422adf7a80205cb534097e6213325e0176c51f6e5cc02e`  
		Last Modified: Sun, 14 Jun 2026 06:44:57 GMT  
		Size: 3.6 MB (3553450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e732a60042adf5cff5fe4fe0de83f937f6e5c8896500f7023e8bf68ed0670d65`  
		Last Modified: Tue, 16 Jun 2026 00:17:51 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad86d1fea29db061a5ae896a0a595b144edcdb4af59deac2b75b0fb8f5fa2d4c`  
		Last Modified: Tue, 16 Jun 2026 00:17:50 GMT  
		Size: 102.6 KB (102624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f26dd2445dbf4d5624417ca290f5ae2e5774fa7fec4f5655cd2377ee3147e4`  
		Last Modified: Tue, 16 Jun 2026 00:17:51 GMT  
		Size: 1.9 MB (1915730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080a186f0ca6beb06a5ce4a86fbc71f5b9995713fcc899c73f995f251ef7c987`  
		Last Modified: Tue, 16 Jun 2026 00:17:51 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c4d4f455f9a2b633cca28e3aa2190e4c42ca83ca6e3ea88ea4abe16944d238`  
		Last Modified: Tue, 16 Jun 2026 00:17:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:d6b7abf6ef34abf12ab2c7f84bd29ac2461eb3271d1c4070456ed9b94e4b41a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43a767571287c8ca227e321ee8d65f9da82e558098bedbb15888434dcc1ce9fa`

```dockerfile
```

-	Layers:
	-	`sha256:1794ccef4392c0db4ba36ad7fde22cdacbda40f4d56f0adbef802163c87e066c`  
		Last Modified: Tue, 16 Jun 2026 00:17:51 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.24` - linux; arm variant v7

```console
$ docker pull memcached@sha256:848c5e0ced69b802cca72c23bec05a4c6f23136212a4a1d5cc22b7c8f0154bf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:286f62a53a8947036e39f2b79567b31d38309fd84c7a39e43de8c5f9817a2f64`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:26 GMT
ADD alpine-minirootfs-3.24.1-armv7.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:26 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:17:59 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:17:59 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:20:56 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:20:56 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:20:56 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:20:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:20:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:20:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:20:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:20:56 GMT
USER memcache
# Tue, 16 Jun 2026 00:20:56 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:20:56 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bc03a9e5b4dd452551f246e199537fe7afc1765f53f510bc81d26df9845e4008`  
		Last Modified: Sun, 14 Jun 2026 06:45:22 GMT  
		Size: 3.3 MB (3260615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f0249bacfc8953b72899bf7b6c904c8750482fce4c93108f57b2c64228b279`  
		Last Modified: Tue, 16 Jun 2026 00:21:00 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95e1b321ffc31d01e766d5d1d054967d613940563406fc54ee981926b7f6049`  
		Last Modified: Tue, 16 Jun 2026 00:21:01 GMT  
		Size: 92.4 KB (92366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce112e60c1b15077277c233a7707831818dff0a15f1fc977ebebc93f817dad43`  
		Last Modified: Tue, 16 Jun 2026 00:21:01 GMT  
		Size: 1.9 MB (1875183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32fa6ed5b14fd6fcf96a7cde2996063f10b8efe802c386479288a232af826027`  
		Last Modified: Tue, 16 Jun 2026 00:21:01 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6648f8180a4eea1f5197f2fa2d356fbbf4e5f65345e189e720e227af64a5e31`  
		Last Modified: Tue, 16 Jun 2026 00:21:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:59387f31eff7cfb3166c5e6d4bad92e255705affcc15c84c4a06c86ecb1a9890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:174eb460b1df4523a4f71ba5a996f2285fa845fe8ef76d2df3ea8c4962c6b6ca`

```dockerfile
```

-	Layers:
	-	`sha256:4ff5e70775e819cab551295c56b58fdb0c44c105cdc4f72247e3968accd2ab2f`  
		Last Modified: Tue, 16 Jun 2026 00:21:00 GMT  
		Size: 94.3 KB (94315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00f10e1301c7e61396658f7e3ed330e400a9f304c6a0323de8ff644aba987474`  
		Last Modified: Tue, 16 Jun 2026 00:21:01 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.24` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:33261748facce282dbe4dbb4d9f875139680fce4cefc13cb9ad8e1ced23f9557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6250475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1614bb2865c8f849c2bc5bf77703a1ab711695c607a8bc6edb013a076ec16d6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:20 GMT
ADD alpine-minirootfs-3.24.1-aarch64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:20 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:13:18 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:13:18 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:16:06 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:16:06 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:16:06 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:16:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:16:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:16:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:16:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:16:06 GMT
USER memcache
# Tue, 16 Jun 2026 00:16:06 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:16:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5de55e5ef9c033997441461efe7ba23a986db059c0bb78b38f84ee0d72b99167`  
		Last Modified: Sun, 14 Jun 2026 06:44:31 GMT  
		Size: 4.2 MB (4183037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5faa19f06c4d5e26332739c7f08fd3dcd2c81817471c62029a6d99af6be8748`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377a35d28f00766e2679c788b95b0a67b9aa5a76c8ef701a2a9604e2a00c3b46`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 121.8 KB (121841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0b819e89558d70f1401ca58cbc19c58ae13e15be8184fd9b2733e022f318a4`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 1.9 MB (1944247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca539cef48ff8c3f723ab23506b6786c9ed26a9cac713601b71de2dc775d26a`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c4c456deed244daa6d7076f40a1cf0364d294059bb43e533677a89027843b15`  
		Last Modified: Tue, 16 Jun 2026 00:16:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:4d25960abc53b5ba1896b8f5ee04ba5ac1389900ab9b413eb62285af7281aedb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d1a4b7ad428a08c8a174d5ecd9763d530e849f54a2d9b90aef934e54b9477d4`

```dockerfile
```

-	Layers:
	-	`sha256:9c0a8e5e07390fae6abe9204450009671011c4d2d5aa5fe4afdd82324fdb49b9`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 94.4 KB (94351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ee01158358d01c082867cf46a5225cf101013e4d5b7eae18fc7853e277ff0f4`  
		Last Modified: Tue, 16 Jun 2026 00:16:11 GMT  
		Size: 20.7 KB (20727 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.24` - linux; 386

```console
$ docker pull memcached@sha256:5436d0ef6e12f2f8e454384ff4a703132b3fe820c41a55336f520bb5d1622574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5702329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8946be3d97c7b9825159f58cbf832b131c75cb90b3fb46a40d5429b9ffe32bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:19 GMT
ADD alpine-minirootfs-3.24.1-x86.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:19 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:13:59 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:13:59 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:16:45 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:16:45 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:16:45 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:16:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:16:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:16:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:16:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:16:46 GMT
USER memcache
# Tue, 16 Jun 2026 00:16:46 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:16:46 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f86df9d778509895efbf9363d8fcb0cbe0b772de536c7218e4c4c947f0be879f`  
		Last Modified: Sun, 14 Jun 2026 06:45:46 GMT  
		Size: 3.7 MB (3670141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043137360442e605bc150f28f20e1fa2d23d90131370bc405ad7d35309594491`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900ce6eeaece12033b12f1c8641c33dcf62ff2525584411911368cfcd0b38224`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 110.7 KB (110729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e8cc1c8f6bc6391eb1a43a46f0b55ca7845f824fc0f2fc7ae7587a7715814e`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 1.9 MB (1920111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d94f6e4d3be92188fc182a3557fe43af5bc9f3e768a7f265977743a56eea527e`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f8a19f18dfff271426de7a17ab6780788fa4345d5fa0120e6d03720d552bd4`  
		Last Modified: Tue, 16 Jun 2026 00:16:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:00dc6a7f29b7f2f5ac46fc5678b80c43c7b1e46b4ca3c84c5597034180aeb644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6de04019c7775544db9adbb4c4558d0e7c842c279e5d70532b2ac0b988ac1345`

```dockerfile
```

-	Layers:
	-	`sha256:80895f8f5e9c9b015e419096426322f4c86c33d55ca8860ee046b61d52782847`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 94.9 KB (94852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c69be8c1f82a066b46cc389712508e85c1dcd77e649c922dba46ace64b343ae`  
		Last Modified: Tue, 16 Jun 2026 00:16:51 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.24` - linux; ppc64le

```console
$ docker pull memcached@sha256:c7857941a51b85b136781035703afcc8854a2d70fa2091208a51f8bb7e71f934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5998515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b02b2222212c64e444ac1a2227b19f0cfb1282c8a8ced386c1b79ae48c641b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:15 GMT
ADD alpine-minirootfs-3.24.1-ppc64le.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:15 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:15:37 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:15:38 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:18:22 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:18:22 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:18:22 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:18:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:18:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:18:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:18:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:18:22 GMT
USER memcache
# Tue, 16 Jun 2026 00:18:22 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:18:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3ebcdcd395ccee658b9200e4b27d7699e5d6ed9f6c1858dea12781aac519ff59`  
		Last Modified: Sun, 14 Jun 2026 06:46:36 GMT  
		Size: 3.8 MB (3813400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b108e2058722fb0fb5a9310e8ebe82ab4b9c021228a94b3125ba49d318e9667`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb8160ed736eda8513164d5d703082fb0c9af9e037472ab70a02579caa3eb99`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 126.3 KB (126252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5cb88dd03ce07ecf1613c2aff220fb392763d8f22edc900c4ad032ee7103d34`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 2.1 MB (2057508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a12fd57420ca797ab383c58a488044d324c4d43b3c94a848f86a0524ed3064b4`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1c0c7b7a77e9375d8a75fb825fa274d9127ca96de79107550517be29501c817`  
		Last Modified: Tue, 16 Jun 2026 00:18:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:851f463d4778539d5e4981f972420f9a57ec2559488f8a59fba6abab6065032f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:734dd3d91f2d6cf217233f7a9dacc3c20ff0590246adb790f95713fb21c115de`

```dockerfile
```

-	Layers:
	-	`sha256:c0d4c203ef9f66cf827ec62098d7801e1c49f1187e0fe047fd32fc2a3271f636`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 94.3 KB (94304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b734d170b5463fa77dd77072e06d51a28efe59a53600d47435b015ebcadae92`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.24` - linux; riscv64

```console
$ docker pull memcached@sha256:ba5bf40b4adc1fe04f32e2e239fa9c0020d4e89bf4079493f8bc11a92c8f4b51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5738070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d12fbf86d6880aaa9d517425d9cecddcf545ba87e577a039dea9ea99ad53d8a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 05:59:15 GMT
ADD alpine-minirootfs-3.24.1-riscv64.tar.gz / # buildkit
# Tue, 16 Jun 2026 05:59:15 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 08:28:27 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 19 Jun 2026 08:28:31 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 19 Jun 2026 08:41:52 GMT
ENV MEMCACHED_VERSION=1.6.42
# Fri, 19 Jun 2026 08:41:52 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Fri, 19 Jun 2026 08:41:52 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Fri, 19 Jun 2026 08:41:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 19 Jun 2026 08:41:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 08:41:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 19 Jun 2026 08:41:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 08:41:53 GMT
USER memcache
# Fri, 19 Jun 2026 08:41:53 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 19 Jun 2026 08:41:53 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c34e5222b29b86391cdae95b0473ef789493ff1a0068a3a30b5d66f544bd7cf6`  
		Last Modified: Sun, 14 Jun 2026 06:47:00 GMT  
		Size: 3.6 MB (3574358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e09d95a0f414638430c0cd3ecfdcce75606201917a27c7cb2ce1e34cb928b26a`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a5335c7af79a1b08af55862ba77644afdae5544d9a7871e45c91b364bd4f71d`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 108.9 KB (108888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3622a6ea71515db1ef566afdbb121daed1f408aacf1519f4173b40dabe2ae627`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 2.1 MB (2053467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1db0e3e31ca3f2830f5404436e92b1862a4078adefacacec09a9580a3ad0a2`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1463b0fd26a37659aaad7f99696e5213764ad03bb094f40836c3309713d7a60`  
		Last Modified: Fri, 19 Jun 2026 08:42:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:aadb3b9338400b87692f95e00931e43940f8d6ddd13f046bd256848dd825e458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bde4b5a4a468d795a5f58dd934b371adfe72cd2ae24e166e1258ad65aa455a56`

```dockerfile
```

-	Layers:
	-	`sha256:debb70180cf674562f7ca321270e3dfa350c5d1596c05dbfcc27b38c65652528`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 94.3 KB (94300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a895bbe0bfec24678c1c92ddd283cb7392e0e8d229f31c769a23c95224c0d371`  
		Last Modified: Fri, 19 Jun 2026 08:42:17 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.24` - linux; s390x

```console
$ docker pull memcached@sha256:e1b640e8d192055e5c3ccd05b077776a0f4d35664191596f7a8230b2cd7ef0f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5823313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1ef6221f9c2854683b0633325a98a0e7a0d3b7d865b02d7cdf4c1d49d2e5090`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:21 GMT
ADD alpine-minirootfs-3.24.1-s390x.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:21 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:13:46 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 16 Jun 2026 00:13:46 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 16 Jun 2026 00:17:12 GMT
ENV MEMCACHED_VERSION=1.6.42
# Tue, 16 Jun 2026 00:17:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Tue, 16 Jun 2026 00:17:12 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Tue, 16 Jun 2026 00:17:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 16 Jun 2026 00:17:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:17:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 16 Jun 2026 00:17:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 00:17:12 GMT
USER memcache
# Tue, 16 Jun 2026 00:17:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 16 Jun 2026 00:17:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:da43be6afaaa3ec1b607461ce64380942a6d76c3d52cda4337b0770d9a96fa89`  
		Last Modified: Sun, 14 Jun 2026 06:47:25 GMT  
		Size: 3.7 MB (3709320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757d04238e02c9bbe1cfd4030cc19e29421650a1b1562a8ca4090d90e9ae17b0`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1949e0fa71fc91bebf4f2e4293108b27de8357d98f98b673bc4f3ed1980b52c`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 114.3 KB (114289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f0e22966bce79fbc8a20f7c27aa07ce63229bb50181319c810ca29f1fb4032`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 2.0 MB (1998350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15eb5e912ef8ec6e3abe76c361cdddb568d20a60be21be379d4d8d7d0ebaa11e`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a549d59ad0d4761ac6f4cca272c4bea521471ed091d0e79143bfda8ff29cf9ce`  
		Last Modified: Tue, 16 Jun 2026 00:17:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:6dbf7c8a98f02a949769403ad1c92583b34a28dccc66b7d83d91863785a6dad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a89d23372d19daf2d6d4e1c4de732f7864316ed5e7713b1103918303873683e`

```dockerfile
```

-	Layers:
	-	`sha256:099ab2d711ef73783b01895824a4664c7d65e2a333e81237b4766cf053a8f6f0`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 94.2 KB (94246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0eccbabf44891af00e622624c5cfd5a295656f82f1c15073b240ac34d47af96c`  
		Last Modified: Tue, 16 Jun 2026 00:17:26 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:latest`

```console
$ docker pull memcached@sha256:85c0ab87f71b8b3ade708271177a8e5efca5e93c00287b6f25a2d74a27180bfa
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
$ docker pull memcached@sha256:09ac4118d89005e47ef3118221840c62f0fa909a2bee07ff571ae1ae59d9a79b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32204821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ad15119e1f73d99f3fbdc56187ea014f4fae2c8fcbe215c259f2fb2b387aefa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:23:00 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 11 Jun 2026 00:23:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:25:47 GMT
ENV MEMCACHED_VERSION=1.6.42
# Thu, 11 Jun 2026 00:25:47 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Thu, 11 Jun 2026 00:25:47 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Thu, 11 Jun 2026 00:25:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 11 Jun 2026 00:25:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:25:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 11 Jun 2026 00:25:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:25:47 GMT
USER memcache
# Thu, 11 Jun 2026 00:25:47 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 11 Jun 2026 00:25:47 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7883ff600bb4cc730c755ccb8be3f5a06371865abe00be70037283c04f4f3f5`  
		Last Modified: Thu, 11 Jun 2026 00:25:53 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d73a0d6b79b50aa2429aebc30b68c38fb0fb43a4a597ce0dd3936605fbb8912e`  
		Last Modified: Thu, 11 Jun 2026 00:25:53 GMT  
		Size: 136.7 KB (136685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5716730726452d6a54ff03d59c7dffbb7ed4f05836877734acf92f7a0512d6a9`  
		Last Modified: Thu, 11 Jun 2026 00:25:53 GMT  
		Size: 2.3 MB (2281206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f338318b7809e3c4be59b7eccaa1e5387cdbe8015c49eac3267097258c54ae89`  
		Last Modified: Thu, 11 Jun 2026 00:25:53 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ca13d7300d84ca43fcce2aa8304787015f83333e041c81c04796354eadce6b`  
		Last Modified: Thu, 11 Jun 2026 00:25:54 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:3d476e3ec28b0dda5046a3223b0e5a8c9ab8dec20bb294a8853da81d828c154d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e2358f67931681260618f406ea3e0032f17f7a82b2a7d36e5511e6413a7133f`

```dockerfile
```

-	Layers:
	-	`sha256:9cb94c17b8cb82e97f6ad217227fa08e25e0fdc9b96fd2fe418e0acc53911305`  
		Last Modified: Thu, 11 Jun 2026 00:25:53 GMT  
		Size: 2.0 MB (2008368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f8a18d24b8d75bd4b8d856878db21e4d4df7e3e553b9d72d0156bbe58c869d3`  
		Last Modified: Thu, 11 Jun 2026 00:25:53 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm variant v5

```console
$ docker pull memcached@sha256:f059b77d971253090e3862e28d374840935b5c06467230e9bea207fdb6ef3bf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30316631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c99754215fd2490daf10c8c1046bee3ab237e1e95bd4b46ef0610ca9d1c9badc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:19:47 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 11 Jun 2026 00:19:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:23:08 GMT
ENV MEMCACHED_VERSION=1.6.42
# Thu, 11 Jun 2026 00:23:08 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Thu, 11 Jun 2026 00:23:08 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Thu, 11 Jun 2026 00:23:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 11 Jun 2026 00:23:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:23:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 11 Jun 2026 00:23:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:23:08 GMT
USER memcache
# Thu, 11 Jun 2026 00:23:08 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 11 Jun 2026 00:23:08 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ed883f3fd95b7edef302d7ca9520eefdae280af081509bd7e9e5b5ff8f4cda7c`  
		Last Modified: Wed, 10 Jun 2026 23:41:17 GMT  
		Size: 28.0 MB (27959200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e92527947bdcc341ab63777422e7409751516a8bc5ffc61040d76b72e7d58c`  
		Last Modified: Thu, 11 Jun 2026 00:23:14 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c52c9bd0c151ce908cf5e8c55694b4a321a916d3053e9e4cd3b06837e55f325`  
		Last Modified: Thu, 11 Jun 2026 00:23:14 GMT  
		Size: 144.2 KB (144156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ec2615dd4e79e84378f7223c9d7c70a6cdfb8835717c19cadbab17a726210d`  
		Last Modified: Thu, 11 Jun 2026 00:23:14 GMT  
		Size: 2.2 MB (2211763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4249a738c6e8e951ca0bf1608e335442f8f50ff9fe57a524b1bdb472e59ed1`  
		Last Modified: Thu, 11 Jun 2026 00:23:14 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab171fa641968acda113ed8ec0cbff5159a4895efed9c4e08bb6e466a40fb5ce`  
		Last Modified: Thu, 11 Jun 2026 00:23:15 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:a7356b3e73eada1ea16535f45e9a297b7913adfb103e9df5d0a2ee333c58f443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c75fc3f8c74e188d3585642b303189b73ae78c14b089bd14f0d37da2b085f25`

```dockerfile
```

-	Layers:
	-	`sha256:5a953398782781fbd31e5d1fb67c1cdeb82c91397fb27ce32b9d756cc938a03a`  
		Last Modified: Thu, 11 Jun 2026 00:23:14 GMT  
		Size: 2.0 MB (2011371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aeae6ddb09b0b52fdf1e1db9b67dfa04fba888fbba5c54b1b7e30ecbd56dafde`  
		Last Modified: Thu, 11 Jun 2026 00:23:14 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm variant v7

```console
$ docker pull memcached@sha256:7b20950329f422c7b322057fe1f944f98589cf937e5e65118b6d4bb241436ffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28513288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5d65e3287f7256814db41a73f2978df2252f6ac399369fe1a7a3eb1c4ceb3e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:21:55 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 11 Jun 2026 00:21:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:25:06 GMT
ENV MEMCACHED_VERSION=1.6.42
# Thu, 11 Jun 2026 00:25:06 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Thu, 11 Jun 2026 00:25:06 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Thu, 11 Jun 2026 00:25:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 11 Jun 2026 00:25:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:25:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 11 Jun 2026 00:25:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:25:06 GMT
USER memcache
# Thu, 11 Jun 2026 00:25:06 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 11 Jun 2026 00:25:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4bd6ddea06d5009ee47ddb0f254a2569aff0230c005869ebd416b20295d945c0`  
		Last Modified: Wed, 10 Jun 2026 23:42:34 GMT  
		Size: 26.2 MB (26211004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bcac116a5bd6f8c4ba910742373294134be4443587cce918db3492895262e16`  
		Last Modified: Thu, 11 Jun 2026 00:25:12 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af6a74cecf5734c352e3c2ea5fb348246cfe77549b6cb2afe3116aaf39983ff8`  
		Last Modified: Thu, 11 Jun 2026 00:25:12 GMT  
		Size: 135.4 KB (135382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6189c46b05f5cdb39083034f258358c5472cc6824a25a7dc8a8f60ae58891116`  
		Last Modified: Thu, 11 Jun 2026 00:25:12 GMT  
		Size: 2.2 MB (2165385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfeedbf1b9c25a3c29e32962704f935689b2b60c4096315dbee3365a9cec4dc0`  
		Last Modified: Thu, 11 Jun 2026 00:25:12 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0309704e28c847b1dd0249a490a5774838b3d27bf059481108e0f1a300efd4ae`  
		Last Modified: Thu, 11 Jun 2026 00:25:13 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:84793c5cdc418c73cc53c1dcdf3ebaf9d1c2a7910ec63c85d179a691e05f1ddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0981cd8d43f93fb996bbc87f0659a7c3a7163d74a5c84503eb77588ed240010c`

```dockerfile
```

-	Layers:
	-	`sha256:39acaedd56024e59130ae654692bdff06d01b71719567ede3d9ece539679150e`  
		Last Modified: Thu, 11 Jun 2026 00:25:13 GMT  
		Size: 2.0 MB (2009828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ada0017eed4fa0f3db9a2e1669d0eb74e2908e65a483af6819df971d18d767a`  
		Last Modified: Thu, 11 Jun 2026 00:25:12 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:a36eca5b5840c718ca41526a871fd751dc96965f182778a7631a0c2896c3f44a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32566560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31c7500da651c7c5945a2db8b00248c02ad2947b4eccb66b464759cd6f4ea2c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:23:08 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 11 Jun 2026 00:23:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:26:08 GMT
ENV MEMCACHED_VERSION=1.6.42
# Thu, 11 Jun 2026 00:26:08 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Thu, 11 Jun 2026 00:26:08 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Thu, 11 Jun 2026 00:26:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 11 Jun 2026 00:26:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:26:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 11 Jun 2026 00:26:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:26:08 GMT
USER memcache
# Thu, 11 Jun 2026 00:26:08 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 11 Jun 2026 00:26:08 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb68ad832950ffa1d5fe24c7e7ee4e061b358d6bcb14dfdb1bb2dec4c557f7a2`  
		Last Modified: Thu, 11 Jun 2026 00:26:15 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f6f966199cad211cd492fc65c6c927fde3a05499bdd9a2112d65deb706cfbc6`  
		Last Modified: Thu, 11 Jun 2026 00:26:14 GMT  
		Size: 153.5 KB (153481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3314b48b94577865e96641c557d5048167254c141db1725db6a5b7a623b68f7b`  
		Last Modified: Thu, 11 Jun 2026 00:26:15 GMT  
		Size: 2.3 MB (2263038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e33e48bcfd48ec271ffa516b5c3b03458185abfb31596aca0b854e9c9367fb9`  
		Last Modified: Thu, 11 Jun 2026 00:26:15 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb41e83cd817b17ff4c2b62ce482681096f6783b2a32be0407cada277d4f293`  
		Last Modified: Thu, 11 Jun 2026 00:26:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:0253549da149222537eeb2e51a1b411b7662c20d8c8964e71967cf670ce9c992
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af9894c8fa8e920a07bf631bed91c9b67398338986159408229a8da050b21c3b`

```dockerfile
```

-	Layers:
	-	`sha256:a11c09037e68845f3c8c01efb996710c3b2d21ba868a98c3ba2582a28d0f1047`  
		Last Modified: Thu, 11 Jun 2026 00:26:15 GMT  
		Size: 2.0 MB (2008676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40468c38b6f60c4625c352d5bdc83ea61510da0efeb2542777603da191a5d2fa`  
		Last Modified: Thu, 11 Jun 2026 00:26:14 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; 386

```console
$ docker pull memcached@sha256:e134667b3198bc9f05962d9bb97cf359ab04c31cb8d11c75e2683de54cebd46e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33675616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cba4eb3d3e82545273aa5ff6f0e6f7bf2b1240176b9489d2315fcf290b9c49a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:18:22 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 11 Jun 2026 00:18:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:21:26 GMT
ENV MEMCACHED_VERSION=1.6.42
# Thu, 11 Jun 2026 00:21:26 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Thu, 11 Jun 2026 00:21:26 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Thu, 11 Jun 2026 00:21:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 11 Jun 2026 00:21:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:21:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 11 Jun 2026 00:21:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:21:26 GMT
USER memcache
# Thu, 11 Jun 2026 00:21:26 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 11 Jun 2026 00:21:26 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:720f951a68f4f9ab464e52b53cf88cfb86bc876b3f00956d000420777ab93c0c`  
		Last Modified: Wed, 10 Jun 2026 23:40:30 GMT  
		Size: 31.3 MB (31301194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2607fca8a1b7fbebf74214d1b33f4f0a54aed5fef2bed18ddc89836a7d00e04b`  
		Last Modified: Thu, 11 Jun 2026 00:21:31 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4620fc98d601bc463a1a505fb0ecf42cb42fa76088d5e80dee41474c74f39f1`  
		Last Modified: Thu, 11 Jun 2026 00:21:32 GMT  
		Size: 147.5 KB (147511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a4c97894b05376111399fa19e7429f36d493cb528c53cb81318a2920d5a954`  
		Last Modified: Thu, 11 Jun 2026 00:21:32 GMT  
		Size: 2.2 MB (2225398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f4a764af02d7ba61dd0909ddb429ba92c9a367243a225936fd625fda113340`  
		Last Modified: Thu, 11 Jun 2026 00:21:32 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52e82109e627ebc0d88a9f7c357b97f14b8ac06bdab5d0b6aa50c3b958a13a8`  
		Last Modified: Thu, 11 Jun 2026 00:21:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:6670b6485b54bcae32ddeda5c2d1764d0ee2066f036d0c17f2cc89734f0be8c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d0aef4dacfecea9e8dbc20498736f77e48bf5106eb60bcfa08c1e81a5c4f06c`

```dockerfile
```

-	Layers:
	-	`sha256:0ebdf5fe0d474785e4448d36043967631fb650ec7b52bd865126a7360978a2ea`  
		Last Modified: Thu, 11 Jun 2026 00:21:32 GMT  
		Size: 2.0 MB (2005525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f257ddeb15df7a03d8e7bb57e01531d894c998af32f33cb528199914bd8f6e1c`  
		Last Modified: Thu, 11 Jun 2026 00:21:32 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; ppc64le

```console
$ docker pull memcached@sha256:25e41a95392ee3c63e35711fec0648fbedc92c6be718456ad8fb89ab66f4e825
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36762178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a04e55188a4c60d5cd8eb00b50628fd87658d0d1814097b40417d71b18479e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 02:36:51 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 11 Jun 2026 02:36:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:59:49 GMT
ENV MEMCACHED_VERSION=1.6.42
# Thu, 11 Jun 2026 02:59:49 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Thu, 11 Jun 2026 02:59:49 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Thu, 11 Jun 2026 02:59:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 11 Jun 2026 02:59:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 02:59:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 11 Jun 2026 02:59:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 02:59:50 GMT
USER memcache
# Thu, 11 Jun 2026 02:59:50 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 11 Jun 2026 02:59:50 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9d6b2e320e2b74843186d830e8202c50ebfaeccf823d239e3e3e349a8a508d80`  
		Last Modified: Thu, 11 Jun 2026 00:24:42 GMT  
		Size: 33.6 MB (33606340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d389c79e93b7c7b3cc2a8226edeb6460d8101e245642213048c1a187d08a935d`  
		Last Modified: Thu, 11 Jun 2026 03:00:07 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7bb22e37f822a0e94fa24cd439d7666c214637b0d59c384dd19e12674c74a82`  
		Last Modified: Thu, 11 Jun 2026 03:00:07 GMT  
		Size: 170.4 KB (170363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82cbb5c5e79cdcec98bd562e1a62768994b805ff7d805b6b75b5bf0e349cff8`  
		Last Modified: Thu, 11 Jun 2026 03:00:06 GMT  
		Size: 3.0 MB (2983963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e60c6f3b8886967bbbabece38cfe74eccdfde98cdae42045a33c5b2b29fd6da`  
		Last Modified: Thu, 11 Jun 2026 03:00:08 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc87d370da3b9877481bf9620bda982328b4d722812ec3e77a7b4c50d016eb33`  
		Last Modified: Thu, 11 Jun 2026 03:00:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:0101df893b4af64daa7ee54d012d7b8682b6c1a9ad1d85700cf8ff269664b19e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b06e6f43b0b95c657fb0043338f12918e63fcac640df48783c49ac29092afb0b`

```dockerfile
```

-	Layers:
	-	`sha256:8ed9fcb43f9f08fb8702ae2709d918b6370866fb4697ddf04b93f42080b23d94`  
		Last Modified: Thu, 11 Jun 2026 03:00:08 GMT  
		Size: 2.0 MB (2011969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c6915dddb9ee13a9cd4156b07c521335c76c9687dcb3a08e66e147af9d99453`  
		Last Modified: Thu, 11 Jun 2026 03:00:06 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; riscv64

```console
$ docker pull memcached@sha256:918c03d1a36c36f13b67e3fbf100f93adad50fbbb452fecc3769db0b8cde487c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30626726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1c8f5f48c37fb2ef15e785c080f746aec65afab782672de8b6a63bd88942e41`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1781049600'
# Fri, 12 Jun 2026 00:28:54 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 12 Jun 2026 00:29:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jun 2026 00:42:57 GMT
ENV MEMCACHED_VERSION=1.6.42
# Fri, 12 Jun 2026 00:42:57 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Fri, 12 Jun 2026 00:42:57 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Fri, 12 Jun 2026 00:42:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 12 Jun 2026 00:42:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Jun 2026 00:42:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 12 Jun 2026 00:42:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2026 00:42:57 GMT
USER memcache
# Fri, 12 Jun 2026 00:42:57 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 12 Jun 2026 00:42:57 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0b510fe8545cab831b696965b5a825649c5c945581e912d31a08a0b30ff940c0`  
		Last Modified: Thu, 11 Jun 2026 03:01:06 GMT  
		Size: 28.3 MB (28282305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35e7a152e660b7a61f448299ac325c28198a870bc53d54cd2584d111c3cef30`  
		Last Modified: Fri, 12 Jun 2026 00:43:44 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d26b2af070be1166e165d4bd1eb073a685622ddb1edb5cf4382cb7825faa21a`  
		Last Modified: Fri, 12 Jun 2026 00:43:44 GMT  
		Size: 133.1 KB (133071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ac4d08e6c19ea726574dc4cd56f4d39216f427cdfd9d6e19c91b06583e6630`  
		Last Modified: Fri, 12 Jun 2026 00:43:44 GMT  
		Size: 2.2 MB (2209833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:039ac44117911671ad0fca8638fa93282ad5865273a55e1328d3180ac5c4f463`  
		Last Modified: Fri, 12 Jun 2026 00:43:44 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65787f51c4d435ccf6c4c9c11e27fe642bd5af3fdd4489e11005614f51c21c29`  
		Last Modified: Fri, 12 Jun 2026 00:43:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:5db8b7d0f9f634b02f9f4dfb45d2f0d3fb2ef1778c3e52058327cd5dec31ebce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0de6ff12136279a3005dae5ce29967a780efb19d8a50b71f33b8153d38859c49`

```dockerfile
```

-	Layers:
	-	`sha256:256f6cfcbc556a40776a58fddd91ccacf0870ab5955a42e7e3ea23601ff76633`  
		Last Modified: Fri, 12 Jun 2026 00:43:44 GMT  
		Size: 2.0 MB (2002332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdfa564b06be9c36a9d81da00994136c858ca65d81762277469168a418a9c9fa`  
		Last Modified: Fri, 12 Jun 2026 00:43:44 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; s390x

```console
$ docker pull memcached@sha256:75f4e343898a5a326a82f6560f0efdd5d11c5aea7a710327cdfd400ac3244341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32291904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd9e841717be4c79746136574299d1a6552f88fe8566606318efb07377ef20c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:19:32 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 11 Jun 2026 00:19:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:22:55 GMT
ENV MEMCACHED_VERSION=1.6.42
# Thu, 11 Jun 2026 00:22:55 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Thu, 11 Jun 2026 00:22:55 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Thu, 11 Jun 2026 00:22:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 11 Jun 2026 00:22:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:22:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 11 Jun 2026 00:22:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:22:55 GMT
USER memcache
# Thu, 11 Jun 2026 00:22:55 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 11 Jun 2026 00:22:55 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:760dcf74fdfe93300ce15b5b23adf9aa4af45b6ba9d69925863198f64881a537`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 29.9 MB (29851354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159eeccf7c6aa583901267e3c00bf9c124c32be82a1074722d2be0b547fee632`  
		Last Modified: Thu, 11 Jun 2026 00:23:05 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d08bb26724ea31dfaf95eb6c1647b7686671b3869632300d6056a05c3532bd`  
		Last Modified: Thu, 11 Jun 2026 00:23:05 GMT  
		Size: 140.5 KB (140545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b341a8e7ca68a391e79c556246f3f0b81e4a5e747fed517e274d78f49faa30`  
		Last Modified: Thu, 11 Jun 2026 00:23:05 GMT  
		Size: 2.3 MB (2298492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff1b1dd9080cb995308882030f9579f4c5bf2af5b26b7270d6682de75f6e6d5`  
		Last Modified: Thu, 11 Jun 2026 00:23:05 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075343c77f8c8b9a1bb9fe079e853c0e4628b60f1fff7d8dce82d38c3a344bf8`  
		Last Modified: Thu, 11 Jun 2026 00:23:06 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:1f977b6725f519f48d75ffc92c711df863d7c0e4a1d1f0c5a5bc6605533f35e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1104b534613c8d2cc0544b9adf96821b4f7f623262ef6ddc425f13fa94427850`

```dockerfile
```

-	Layers:
	-	`sha256:66bb879abbe8f943d53561fcf4f4262e1b78fb31b6aa3fdac560ffdc45e3d4b5`  
		Last Modified: Thu, 11 Jun 2026 00:23:05 GMT  
		Size: 2.0 MB (2009805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e448bf5a0443ce0296756453f8bca10e0ec97ebc01576de74a28f60b78299f2b`  
		Last Modified: Thu, 11 Jun 2026 00:23:05 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:trixie`

```console
$ docker pull memcached@sha256:85c0ab87f71b8b3ade708271177a8e5efca5e93c00287b6f25a2d74a27180bfa
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
$ docker pull memcached@sha256:09ac4118d89005e47ef3118221840c62f0fa909a2bee07ff571ae1ae59d9a79b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32204821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ad15119e1f73d99f3fbdc56187ea014f4fae2c8fcbe215c259f2fb2b387aefa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:23:00 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 11 Jun 2026 00:23:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:25:47 GMT
ENV MEMCACHED_VERSION=1.6.42
# Thu, 11 Jun 2026 00:25:47 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Thu, 11 Jun 2026 00:25:47 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Thu, 11 Jun 2026 00:25:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 11 Jun 2026 00:25:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:25:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 11 Jun 2026 00:25:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:25:47 GMT
USER memcache
# Thu, 11 Jun 2026 00:25:47 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 11 Jun 2026 00:25:47 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7883ff600bb4cc730c755ccb8be3f5a06371865abe00be70037283c04f4f3f5`  
		Last Modified: Thu, 11 Jun 2026 00:25:53 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d73a0d6b79b50aa2429aebc30b68c38fb0fb43a4a597ce0dd3936605fbb8912e`  
		Last Modified: Thu, 11 Jun 2026 00:25:53 GMT  
		Size: 136.7 KB (136685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5716730726452d6a54ff03d59c7dffbb7ed4f05836877734acf92f7a0512d6a9`  
		Last Modified: Thu, 11 Jun 2026 00:25:53 GMT  
		Size: 2.3 MB (2281206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f338318b7809e3c4be59b7eccaa1e5387cdbe8015c49eac3267097258c54ae89`  
		Last Modified: Thu, 11 Jun 2026 00:25:53 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ca13d7300d84ca43fcce2aa8304787015f83333e041c81c04796354eadce6b`  
		Last Modified: Thu, 11 Jun 2026 00:25:54 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:3d476e3ec28b0dda5046a3223b0e5a8c9ab8dec20bb294a8853da81d828c154d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e2358f67931681260618f406ea3e0032f17f7a82b2a7d36e5511e6413a7133f`

```dockerfile
```

-	Layers:
	-	`sha256:9cb94c17b8cb82e97f6ad217227fa08e25e0fdc9b96fd2fe418e0acc53911305`  
		Last Modified: Thu, 11 Jun 2026 00:25:53 GMT  
		Size: 2.0 MB (2008368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f8a18d24b8d75bd4b8d856878db21e4d4df7e3e553b9d72d0156bbe58c869d3`  
		Last Modified: Thu, 11 Jun 2026 00:25:53 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; arm variant v5

```console
$ docker pull memcached@sha256:f059b77d971253090e3862e28d374840935b5c06467230e9bea207fdb6ef3bf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30316631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c99754215fd2490daf10c8c1046bee3ab237e1e95bd4b46ef0610ca9d1c9badc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:19:47 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 11 Jun 2026 00:19:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:23:08 GMT
ENV MEMCACHED_VERSION=1.6.42
# Thu, 11 Jun 2026 00:23:08 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Thu, 11 Jun 2026 00:23:08 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Thu, 11 Jun 2026 00:23:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 11 Jun 2026 00:23:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:23:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 11 Jun 2026 00:23:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:23:08 GMT
USER memcache
# Thu, 11 Jun 2026 00:23:08 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 11 Jun 2026 00:23:08 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ed883f3fd95b7edef302d7ca9520eefdae280af081509bd7e9e5b5ff8f4cda7c`  
		Last Modified: Wed, 10 Jun 2026 23:41:17 GMT  
		Size: 28.0 MB (27959200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e92527947bdcc341ab63777422e7409751516a8bc5ffc61040d76b72e7d58c`  
		Last Modified: Thu, 11 Jun 2026 00:23:14 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c52c9bd0c151ce908cf5e8c55694b4a321a916d3053e9e4cd3b06837e55f325`  
		Last Modified: Thu, 11 Jun 2026 00:23:14 GMT  
		Size: 144.2 KB (144156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ec2615dd4e79e84378f7223c9d7c70a6cdfb8835717c19cadbab17a726210d`  
		Last Modified: Thu, 11 Jun 2026 00:23:14 GMT  
		Size: 2.2 MB (2211763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4249a738c6e8e951ca0bf1608e335442f8f50ff9fe57a524b1bdb472e59ed1`  
		Last Modified: Thu, 11 Jun 2026 00:23:14 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab171fa641968acda113ed8ec0cbff5159a4895efed9c4e08bb6e466a40fb5ce`  
		Last Modified: Thu, 11 Jun 2026 00:23:15 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:a7356b3e73eada1ea16535f45e9a297b7913adfb103e9df5d0a2ee333c58f443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c75fc3f8c74e188d3585642b303189b73ae78c14b089bd14f0d37da2b085f25`

```dockerfile
```

-	Layers:
	-	`sha256:5a953398782781fbd31e5d1fb67c1cdeb82c91397fb27ce32b9d756cc938a03a`  
		Last Modified: Thu, 11 Jun 2026 00:23:14 GMT  
		Size: 2.0 MB (2011371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aeae6ddb09b0b52fdf1e1db9b67dfa04fba888fbba5c54b1b7e30ecbd56dafde`  
		Last Modified: Thu, 11 Jun 2026 00:23:14 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; arm variant v7

```console
$ docker pull memcached@sha256:7b20950329f422c7b322057fe1f944f98589cf937e5e65118b6d4bb241436ffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28513288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5d65e3287f7256814db41a73f2978df2252f6ac399369fe1a7a3eb1c4ceb3e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:21:55 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 11 Jun 2026 00:21:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:25:06 GMT
ENV MEMCACHED_VERSION=1.6.42
# Thu, 11 Jun 2026 00:25:06 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Thu, 11 Jun 2026 00:25:06 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Thu, 11 Jun 2026 00:25:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 11 Jun 2026 00:25:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:25:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 11 Jun 2026 00:25:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:25:06 GMT
USER memcache
# Thu, 11 Jun 2026 00:25:06 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 11 Jun 2026 00:25:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4bd6ddea06d5009ee47ddb0f254a2569aff0230c005869ebd416b20295d945c0`  
		Last Modified: Wed, 10 Jun 2026 23:42:34 GMT  
		Size: 26.2 MB (26211004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bcac116a5bd6f8c4ba910742373294134be4443587cce918db3492895262e16`  
		Last Modified: Thu, 11 Jun 2026 00:25:12 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af6a74cecf5734c352e3c2ea5fb348246cfe77549b6cb2afe3116aaf39983ff8`  
		Last Modified: Thu, 11 Jun 2026 00:25:12 GMT  
		Size: 135.4 KB (135382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6189c46b05f5cdb39083034f258358c5472cc6824a25a7dc8a8f60ae58891116`  
		Last Modified: Thu, 11 Jun 2026 00:25:12 GMT  
		Size: 2.2 MB (2165385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfeedbf1b9c25a3c29e32962704f935689b2b60c4096315dbee3365a9cec4dc0`  
		Last Modified: Thu, 11 Jun 2026 00:25:12 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0309704e28c847b1dd0249a490a5774838b3d27bf059481108e0f1a300efd4ae`  
		Last Modified: Thu, 11 Jun 2026 00:25:13 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:84793c5cdc418c73cc53c1dcdf3ebaf9d1c2a7910ec63c85d179a691e05f1ddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0981cd8d43f93fb996bbc87f0659a7c3a7163d74a5c84503eb77588ed240010c`

```dockerfile
```

-	Layers:
	-	`sha256:39acaedd56024e59130ae654692bdff06d01b71719567ede3d9ece539679150e`  
		Last Modified: Thu, 11 Jun 2026 00:25:13 GMT  
		Size: 2.0 MB (2009828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ada0017eed4fa0f3db9a2e1669d0eb74e2908e65a483af6819df971d18d767a`  
		Last Modified: Thu, 11 Jun 2026 00:25:12 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:a36eca5b5840c718ca41526a871fd751dc96965f182778a7631a0c2896c3f44a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32566560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31c7500da651c7c5945a2db8b00248c02ad2947b4eccb66b464759cd6f4ea2c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:23:08 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 11 Jun 2026 00:23:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:26:08 GMT
ENV MEMCACHED_VERSION=1.6.42
# Thu, 11 Jun 2026 00:26:08 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Thu, 11 Jun 2026 00:26:08 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Thu, 11 Jun 2026 00:26:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 11 Jun 2026 00:26:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:26:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 11 Jun 2026 00:26:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:26:08 GMT
USER memcache
# Thu, 11 Jun 2026 00:26:08 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 11 Jun 2026 00:26:08 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb68ad832950ffa1d5fe24c7e7ee4e061b358d6bcb14dfdb1bb2dec4c557f7a2`  
		Last Modified: Thu, 11 Jun 2026 00:26:15 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f6f966199cad211cd492fc65c6c927fde3a05499bdd9a2112d65deb706cfbc6`  
		Last Modified: Thu, 11 Jun 2026 00:26:14 GMT  
		Size: 153.5 KB (153481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3314b48b94577865e96641c557d5048167254c141db1725db6a5b7a623b68f7b`  
		Last Modified: Thu, 11 Jun 2026 00:26:15 GMT  
		Size: 2.3 MB (2263038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e33e48bcfd48ec271ffa516b5c3b03458185abfb31596aca0b854e9c9367fb9`  
		Last Modified: Thu, 11 Jun 2026 00:26:15 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb41e83cd817b17ff4c2b62ce482681096f6783b2a32be0407cada277d4f293`  
		Last Modified: Thu, 11 Jun 2026 00:26:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:0253549da149222537eeb2e51a1b411b7662c20d8c8964e71967cf670ce9c992
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af9894c8fa8e920a07bf631bed91c9b67398338986159408229a8da050b21c3b`

```dockerfile
```

-	Layers:
	-	`sha256:a11c09037e68845f3c8c01efb996710c3b2d21ba868a98c3ba2582a28d0f1047`  
		Last Modified: Thu, 11 Jun 2026 00:26:15 GMT  
		Size: 2.0 MB (2008676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40468c38b6f60c4625c352d5bdc83ea61510da0efeb2542777603da191a5d2fa`  
		Last Modified: Thu, 11 Jun 2026 00:26:14 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; 386

```console
$ docker pull memcached@sha256:e134667b3198bc9f05962d9bb97cf359ab04c31cb8d11c75e2683de54cebd46e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33675616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cba4eb3d3e82545273aa5ff6f0e6f7bf2b1240176b9489d2315fcf290b9c49a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:18:22 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 11 Jun 2026 00:18:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:21:26 GMT
ENV MEMCACHED_VERSION=1.6.42
# Thu, 11 Jun 2026 00:21:26 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Thu, 11 Jun 2026 00:21:26 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Thu, 11 Jun 2026 00:21:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 11 Jun 2026 00:21:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:21:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 11 Jun 2026 00:21:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:21:26 GMT
USER memcache
# Thu, 11 Jun 2026 00:21:26 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 11 Jun 2026 00:21:26 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:720f951a68f4f9ab464e52b53cf88cfb86bc876b3f00956d000420777ab93c0c`  
		Last Modified: Wed, 10 Jun 2026 23:40:30 GMT  
		Size: 31.3 MB (31301194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2607fca8a1b7fbebf74214d1b33f4f0a54aed5fef2bed18ddc89836a7d00e04b`  
		Last Modified: Thu, 11 Jun 2026 00:21:31 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4620fc98d601bc463a1a505fb0ecf42cb42fa76088d5e80dee41474c74f39f1`  
		Last Modified: Thu, 11 Jun 2026 00:21:32 GMT  
		Size: 147.5 KB (147511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a4c97894b05376111399fa19e7429f36d493cb528c53cb81318a2920d5a954`  
		Last Modified: Thu, 11 Jun 2026 00:21:32 GMT  
		Size: 2.2 MB (2225398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f4a764af02d7ba61dd0909ddb429ba92c9a367243a225936fd625fda113340`  
		Last Modified: Thu, 11 Jun 2026 00:21:32 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52e82109e627ebc0d88a9f7c357b97f14b8ac06bdab5d0b6aa50c3b958a13a8`  
		Last Modified: Thu, 11 Jun 2026 00:21:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:6670b6485b54bcae32ddeda5c2d1764d0ee2066f036d0c17f2cc89734f0be8c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d0aef4dacfecea9e8dbc20498736f77e48bf5106eb60bcfa08c1e81a5c4f06c`

```dockerfile
```

-	Layers:
	-	`sha256:0ebdf5fe0d474785e4448d36043967631fb650ec7b52bd865126a7360978a2ea`  
		Last Modified: Thu, 11 Jun 2026 00:21:32 GMT  
		Size: 2.0 MB (2005525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f257ddeb15df7a03d8e7bb57e01531d894c998af32f33cb528199914bd8f6e1c`  
		Last Modified: Thu, 11 Jun 2026 00:21:32 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; ppc64le

```console
$ docker pull memcached@sha256:25e41a95392ee3c63e35711fec0648fbedc92c6be718456ad8fb89ab66f4e825
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36762178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a04e55188a4c60d5cd8eb00b50628fd87658d0d1814097b40417d71b18479e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 02:36:51 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 11 Jun 2026 02:36:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:59:49 GMT
ENV MEMCACHED_VERSION=1.6.42
# Thu, 11 Jun 2026 02:59:49 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Thu, 11 Jun 2026 02:59:49 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Thu, 11 Jun 2026 02:59:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 11 Jun 2026 02:59:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 02:59:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 11 Jun 2026 02:59:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 02:59:50 GMT
USER memcache
# Thu, 11 Jun 2026 02:59:50 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 11 Jun 2026 02:59:50 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9d6b2e320e2b74843186d830e8202c50ebfaeccf823d239e3e3e349a8a508d80`  
		Last Modified: Thu, 11 Jun 2026 00:24:42 GMT  
		Size: 33.6 MB (33606340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d389c79e93b7c7b3cc2a8226edeb6460d8101e245642213048c1a187d08a935d`  
		Last Modified: Thu, 11 Jun 2026 03:00:07 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7bb22e37f822a0e94fa24cd439d7666c214637b0d59c384dd19e12674c74a82`  
		Last Modified: Thu, 11 Jun 2026 03:00:07 GMT  
		Size: 170.4 KB (170363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82cbb5c5e79cdcec98bd562e1a62768994b805ff7d805b6b75b5bf0e349cff8`  
		Last Modified: Thu, 11 Jun 2026 03:00:06 GMT  
		Size: 3.0 MB (2983963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e60c6f3b8886967bbbabece38cfe74eccdfde98cdae42045a33c5b2b29fd6da`  
		Last Modified: Thu, 11 Jun 2026 03:00:08 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc87d370da3b9877481bf9620bda982328b4d722812ec3e77a7b4c50d016eb33`  
		Last Modified: Thu, 11 Jun 2026 03:00:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:0101df893b4af64daa7ee54d012d7b8682b6c1a9ad1d85700cf8ff269664b19e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b06e6f43b0b95c657fb0043338f12918e63fcac640df48783c49ac29092afb0b`

```dockerfile
```

-	Layers:
	-	`sha256:8ed9fcb43f9f08fb8702ae2709d918b6370866fb4697ddf04b93f42080b23d94`  
		Last Modified: Thu, 11 Jun 2026 03:00:08 GMT  
		Size: 2.0 MB (2011969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c6915dddb9ee13a9cd4156b07c521335c76c9687dcb3a08e66e147af9d99453`  
		Last Modified: Thu, 11 Jun 2026 03:00:06 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; riscv64

```console
$ docker pull memcached@sha256:918c03d1a36c36f13b67e3fbf100f93adad50fbbb452fecc3769db0b8cde487c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30626726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1c8f5f48c37fb2ef15e785c080f746aec65afab782672de8b6a63bd88942e41`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1781049600'
# Fri, 12 Jun 2026 00:28:54 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 12 Jun 2026 00:29:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jun 2026 00:42:57 GMT
ENV MEMCACHED_VERSION=1.6.42
# Fri, 12 Jun 2026 00:42:57 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Fri, 12 Jun 2026 00:42:57 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Fri, 12 Jun 2026 00:42:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 12 Jun 2026 00:42:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Jun 2026 00:42:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 12 Jun 2026 00:42:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2026 00:42:57 GMT
USER memcache
# Fri, 12 Jun 2026 00:42:57 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 12 Jun 2026 00:42:57 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0b510fe8545cab831b696965b5a825649c5c945581e912d31a08a0b30ff940c0`  
		Last Modified: Thu, 11 Jun 2026 03:01:06 GMT  
		Size: 28.3 MB (28282305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35e7a152e660b7a61f448299ac325c28198a870bc53d54cd2584d111c3cef30`  
		Last Modified: Fri, 12 Jun 2026 00:43:44 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d26b2af070be1166e165d4bd1eb073a685622ddb1edb5cf4382cb7825faa21a`  
		Last Modified: Fri, 12 Jun 2026 00:43:44 GMT  
		Size: 133.1 KB (133071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ac4d08e6c19ea726574dc4cd56f4d39216f427cdfd9d6e19c91b06583e6630`  
		Last Modified: Fri, 12 Jun 2026 00:43:44 GMT  
		Size: 2.2 MB (2209833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:039ac44117911671ad0fca8638fa93282ad5865273a55e1328d3180ac5c4f463`  
		Last Modified: Fri, 12 Jun 2026 00:43:44 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65787f51c4d435ccf6c4c9c11e27fe642bd5af3fdd4489e11005614f51c21c29`  
		Last Modified: Fri, 12 Jun 2026 00:43:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:5db8b7d0f9f634b02f9f4dfb45d2f0d3fb2ef1778c3e52058327cd5dec31ebce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0de6ff12136279a3005dae5ce29967a780efb19d8a50b71f33b8153d38859c49`

```dockerfile
```

-	Layers:
	-	`sha256:256f6cfcbc556a40776a58fddd91ccacf0870ab5955a42e7e3ea23601ff76633`  
		Last Modified: Fri, 12 Jun 2026 00:43:44 GMT  
		Size: 2.0 MB (2002332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdfa564b06be9c36a9d81da00994136c858ca65d81762277469168a418a9c9fa`  
		Last Modified: Fri, 12 Jun 2026 00:43:44 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:trixie` - linux; s390x

```console
$ docker pull memcached@sha256:75f4e343898a5a326a82f6560f0efdd5d11c5aea7a710327cdfd400ac3244341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32291904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd9e841717be4c79746136574299d1a6552f88fe8566606318efb07377ef20c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:19:32 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Thu, 11 Jun 2026 00:19:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:22:55 GMT
ENV MEMCACHED_VERSION=1.6.42
# Thu, 11 Jun 2026 00:22:55 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Thu, 11 Jun 2026 00:22:55 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Thu, 11 Jun 2026 00:22:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Thu, 11 Jun 2026 00:22:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:22:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 11 Jun 2026 00:22:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:22:55 GMT
USER memcache
# Thu, 11 Jun 2026 00:22:55 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 11 Jun 2026 00:22:55 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:760dcf74fdfe93300ce15b5b23adf9aa4af45b6ba9d69925863198f64881a537`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 29.9 MB (29851354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159eeccf7c6aa583901267e3c00bf9c124c32be82a1074722d2be0b547fee632`  
		Last Modified: Thu, 11 Jun 2026 00:23:05 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d08bb26724ea31dfaf95eb6c1647b7686671b3869632300d6056a05c3532bd`  
		Last Modified: Thu, 11 Jun 2026 00:23:05 GMT  
		Size: 140.5 KB (140545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b341a8e7ca68a391e79c556246f3f0b81e4a5e747fed517e274d78f49faa30`  
		Last Modified: Thu, 11 Jun 2026 00:23:05 GMT  
		Size: 2.3 MB (2298492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff1b1dd9080cb995308882030f9579f4c5bf2af5b26b7270d6682de75f6e6d5`  
		Last Modified: Thu, 11 Jun 2026 00:23:05 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075343c77f8c8b9a1bb9fe079e853c0e4628b60f1fff7d8dce82d38c3a344bf8`  
		Last Modified: Thu, 11 Jun 2026 00:23:06 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:1f977b6725f519f48d75ffc92c711df863d7c0e4a1d1f0c5a5bc6605533f35e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1104b534613c8d2cc0544b9adf96821b4f7f623262ef6ddc425f13fa94427850`

```dockerfile
```

-	Layers:
	-	`sha256:66bb879abbe8f943d53561fcf4f4262e1b78fb31b6aa3fdac560ffdc45e3d4b5`  
		Last Modified: Thu, 11 Jun 2026 00:23:05 GMT  
		Size: 2.0 MB (2009805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e448bf5a0443ce0296756453f8bca10e0ec97ebc01576de74a28f60b78299f2b`  
		Last Modified: Thu, 11 Jun 2026 00:23:05 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json
