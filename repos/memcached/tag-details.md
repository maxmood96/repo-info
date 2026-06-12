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
$ docker pull memcached@sha256:24f46bd5e6250525c4219957edf4490e1dcff92a8c798325d9422798af8d02db
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
$ docker pull memcached@sha256:cb2d8176cf730b6e493f47a20c202e3785450ce97ac94eca4907d7690c1af307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8429739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b50ffd1c04d8028fbb3c3420cc1d60aed911ce7c0e45a4965310fce274d53ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:31 GMT
ADD alpine-minirootfs-3.24.0-x86_64.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:31 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:14:19 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:14:20 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:16:57 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:16:57 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:16:57 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:16:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:16:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:16:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:16:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:16:57 GMT
USER memcache
# Wed, 10 Jun 2026 18:16:57 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:16:57 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9b70e313681f44d32991ec943f89228bc91d7431d4a84feafc269a76e3f96a63`  
		Last Modified: Tue, 09 Jun 2026 20:11:36 GMT  
		Size: 3.9 MB (3866755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e3046ed30b13ad06ce756a4c6583941eb759870afa70848109fd8c0064519f`  
		Last Modified: Wed, 10 Jun 2026 18:17:02 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c4e652e501aa70e550ad140cba871ada70bf7f3a31a1f25b992df3b69702af`  
		Last Modified: Wed, 10 Jun 2026 18:17:03 GMT  
		Size: 106.1 KB (106068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7b3e28eeb74ba3ce98c770af704a09d48456fc4b9d0ac8ec337c30cc95f2e3`  
		Last Modified: Wed, 10 Jun 2026 18:17:03 GMT  
		Size: 4.5 MB (4455567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4da70a2e9c741455aab8b6eeecd686f79532427ac6f458f4c6df4203fb17b42`  
		Last Modified: Wed, 10 Jun 2026 18:17:02 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d9e7ab7a8a69db82d54cd5953d81a8d174f46e493dc10bcead49919ab63b80`  
		Last Modified: Wed, 10 Jun 2026 18:17:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:423aea49db161bc8ab6d8f600ba326351a44d683f648e77c38062ced876533b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6a9742524b3a500c65fd2ff4ee0ed6498d3286356dbe7b04507f7903496dcc2`

```dockerfile
```

-	Layers:
	-	`sha256:1967442755aa01c5b18b82d15e09215bb060a9a4725e69476dffdde04a11a174`  
		Last Modified: Wed, 10 Jun 2026 18:17:03 GMT  
		Size: 94.9 KB (94897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:241a34a97ffb94fa781f2bf870cb96be626d17c16414915a8e5737d781b620d1`  
		Last Modified: Wed, 10 Jun 2026 18:17:02 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:32cf627ba476a687feb05fc278c1ec76e5904f2d070ec439c114e910c770d514
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7724160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:232f09c26d3bbd4437aa7cadb96874736aca039e389a58df9594e5b6aba964b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:25 GMT
ADD alpine-minirootfs-3.24.0-armhf.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:25 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:13:29 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:13:30 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:35:53 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:35:53 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:35:53 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:35:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:35:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:35:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:35:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:35:53 GMT
USER memcache
# Wed, 10 Jun 2026 18:35:53 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:35:53 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d44d12cd5c9ecc8e4b75201d67412f77b79157eaffaaed75c3b717bcd42f61e1`  
		Last Modified: Tue, 09 Jun 2026 20:11:29 GMT  
		Size: 3.6 MB (3575314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573a1d7a0131b3bb62a9b1e14cb0e8cf4d866ce7ec68a2d4a2ac402c7357b24e`  
		Last Modified: Wed, 10 Jun 2026 18:35:57 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608fb78ccee6e69c390e8ce51d8c49d4bdac4d71cf50cc5c6e457dca3274ebf7`  
		Last Modified: Wed, 10 Jun 2026 18:35:57 GMT  
		Size: 102.6 KB (102627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e548b50ad164ad49e2be2cc291334c46cf327222804043ba289bc49d36fb202`  
		Last Modified: Wed, 10 Jun 2026 18:35:57 GMT  
		Size: 4.0 MB (4044869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3288904307a586b305537393c2f20cfcb8d98edcb8c0e51b89036d575c960cb`  
		Last Modified: Wed, 10 Jun 2026 18:35:57 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae9e7c1276f81bfb68d7489c74761c88a037e47d4b72983353c03196b97b218`  
		Last Modified: Wed, 10 Jun 2026 18:35:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:1b8dbbfd625301ca11ebb50f807fdf9060dfc1fa7f9247b6cd5556775c85c77c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f6e1cafb6d6aa90021214a707bd44e9808680bd0fcf819c2bf76e1e97319038`

```dockerfile
```

-	Layers:
	-	`sha256:added378a7ae281e9cd9406a18fcf5d2639f6ffcbf0b2f5fb5fcec47db001204`  
		Last Modified: Wed, 10 Jun 2026 18:35:57 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:01b020198ba0ce8e9af9fb0257ca2487cc71cfec9a953ad04b6cb386059f3bdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7220162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2416c6901535e0b681eeba9d0e010b8030f17e2a0f9a4e8e7bdea9261260886`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2026 20:14:38 GMT
ADD alpine-minirootfs-3.24.0-armv7.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:14:38 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:14:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:14:02 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:16:58 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:16:58 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:16:58 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:16:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:16:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:16:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:16:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:16:59 GMT
USER memcache
# Wed, 10 Jun 2026 18:16:59 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:16:59 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bce674d5697a824549061f4985dfd06a60c018b96ba50b18b7bc1f9ad6143570`  
		Last Modified: Tue, 09 Jun 2026 20:14:43 GMT  
		Size: 3.3 MB (3286160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddccf170e8b5b7071fc7d37c3e7b71b383e42d66ebc8452c8face5ccfc0ba841`  
		Last Modified: Wed, 10 Jun 2026 18:17:04 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d271b94c2d5eb987939fb26d3e872b378914ed230228478c94c4eb9271af3bea`  
		Last Modified: Wed, 10 Jun 2026 18:17:04 GMT  
		Size: 92.4 KB (92371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58107905e1ff79a6248896ab514b9cad8d31bc4ded8616894db922f6d9bc862e`  
		Last Modified: Wed, 10 Jun 2026 18:17:04 GMT  
		Size: 3.8 MB (3840281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1397705fe8ef2c310800a79d7e7f6de7db2ebad65b46e9505ba834b120347c62`  
		Last Modified: Wed, 10 Jun 2026 18:17:04 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06dbe001de1fe8d785dd53bdcb0a65b97ea4a57b4bd839da2e6ef4344226ec07`  
		Last Modified: Wed, 10 Jun 2026 18:17:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:9c08a5c1662aaac2028c9b66d84c8a5ab3ac6ce87d8d1ca8dfb2856bbf331d17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71022047d72bddcc121675d6bbe75bac274911f769029bb179b886d170baeb02`

```dockerfile
```

-	Layers:
	-	`sha256:db4bac74dcb986da8aa5a0e3af57ee133956acb18dac4ae890a9ec074f02c1b5`  
		Last Modified: Wed, 10 Jun 2026 18:17:04 GMT  
		Size: 94.3 KB (94315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a12f73bf7901f75ec1c978ac1cc49ff827de35497af898a05c43fe1d9c753e86`  
		Last Modified: Wed, 10 Jun 2026 18:17:04 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:16eb5e3d6505a7ef0a633bfe2d01f674184e0f6f9cbe79d241120567b03f054f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9059008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5f2f1760f4a10a67fb7a006f00b172c33b6e530525a2a7bf1f112c44e8a1949`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:09 GMT
ADD alpine-minirootfs-3.24.0-aarch64.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:09 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:12:27 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:12:27 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:15:17 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:15:17 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:15:17 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:15:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:15:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:15:17 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:15:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:15:17 GMT
USER memcache
# Wed, 10 Jun 2026 18:15:17 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:15:17 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c05efffaed614b5ff4e3b9a80136e7c0eed0b47f434802c81baf254c0defca91`  
		Last Modified: Tue, 09 Jun 2026 20:11:14 GMT  
		Size: 4.2 MB (4202330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e456d8825f29dfd65b2051f5b44b6de5920128138737cbd93cbae351cc088ce`  
		Last Modified: Wed, 10 Jun 2026 18:15:22 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1569a3fe1932b7d0793450f547c0e3ffcd659baefbc266fc8febd0f82dd3b197`  
		Last Modified: Wed, 10 Jun 2026 18:15:23 GMT  
		Size: 121.9 KB (121857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91674cbd7c3a07584ce0b6f5702920f8c878319100d0794e0be633caf4cd702`  
		Last Modified: Wed, 10 Jun 2026 18:15:23 GMT  
		Size: 4.7 MB (4733470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f23ddaee25aadc1b418bf3aa3c117923c06e9cac1b101e927b76def37507cd2`  
		Last Modified: Wed, 10 Jun 2026 18:15:23 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd7c50e090366a1f99c6b319c0f95302b5ce191989df8f66ddb9e1d4d163be0`  
		Last Modified: Wed, 10 Jun 2026 18:15:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:46bff7acd3c1c4e24acda5e4573e853d532c8f880c8c739e9bcc220de4b43b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:399abce8f4883f60c5fe7741d0d7c0b5fd729e48660e5df3829afc60dc755d1c`

```dockerfile
```

-	Layers:
	-	`sha256:c94369062ddc1d7c765eb1aec2fbaeb202af339dcda4691019309c6708106359`  
		Last Modified: Wed, 10 Jun 2026 18:15:22 GMT  
		Size: 94.4 KB (94351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49b2ad2a43e5a3f86c7fe35d36035450993daa3bb8ecaf1ae6d49b858da8d19b`  
		Last Modified: Wed, 10 Jun 2026 18:15:23 GMT  
		Size: 20.7 KB (20727 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; 386

```console
$ docker pull memcached@sha256:f2d4eb8c40d54fdcd5fb0684d29936ebce2fbafe26c26c0c72ae0a9335f06997
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (8024217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07138462285df4cbd1ed2c627e98451dc1a4b43b37e111b2b72e59d154f811ee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2026 20:10:54 GMT
ADD alpine-minirootfs-3.24.0-x86.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:10:54 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:25:31 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:25:32 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:28:16 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:28:16 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:28:16 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:28:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:28:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:28:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:28:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:28:16 GMT
USER memcache
# Wed, 10 Jun 2026 18:28:16 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:28:16 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:14b4480cdb6be1a40aafc14c9089d92843794d03fc3115b849ddc49717c25982`  
		Last Modified: Tue, 09 Jun 2026 20:10:59 GMT  
		Size: 3.7 MB (3691754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14cf249ff43e2409a2718494167fe16786f19bdc9666b291ba5f4fbb333e382c`  
		Last Modified: Wed, 10 Jun 2026 18:28:21 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9d4516b9de504d8b32b12ee16f3aeb0ed86d6124308df02b6a907e3e0b3ed6`  
		Last Modified: Wed, 10 Jun 2026 18:28:22 GMT  
		Size: 110.7 KB (110732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f550fd7ec906f373bb885a9a587de5a825d95ff63d1353fb88aff5bba428f19a`  
		Last Modified: Wed, 10 Jun 2026 18:28:22 GMT  
		Size: 4.2 MB (4220384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dcc14148666128c245fd38ff2cd067defeb4c4a1acfe2da55983425fe7b5cfd`  
		Last Modified: Wed, 10 Jun 2026 18:28:22 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad5170f36cabc8e1bfed343134a7a78b8ae945e7e73c0428b77c3eb5fddeadb`  
		Last Modified: Wed, 10 Jun 2026 18:28:23 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:12741aadabddc93af391c2b99e0e588138024a0fdb67bcca1191f96869187018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6490fe35195514ccd48669f08b68a82107074785228124b81b6c2e5f6a1133c8`

```dockerfile
```

-	Layers:
	-	`sha256:db2735e9fcf74530bbea1a6790fee5d18607311bb075b0ed4a074e41e6bd0f91`  
		Last Modified: Wed, 10 Jun 2026 18:28:21 GMT  
		Size: 94.9 KB (94852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dcb9494458e7383f61847d265cf37857313b48a9e23522119233328d3f808c6`  
		Last Modified: Wed, 10 Jun 2026 18:28:22 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:a51985551b3de3fae96ad49d7bd83e4bed7b04338ab59c8f1d0615a8104d681f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8377092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eec58c326d0b7fb84ebe5bb90c97ac84004c7a43061561a4551c88cadb9bbea3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2026 20:33:34 GMT
ADD alpine-minirootfs-3.24.0-ppc64le.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:33:34 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:12:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:12:36 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:15:17 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:15:17 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:15:17 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:15:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:15:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:15:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:15:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:15:18 GMT
USER memcache
# Wed, 10 Jun 2026 18:15:18 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:15:18 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:73fae309fa62bb67bbe20b40696c81037cf9f77919ce6726a7e535ae9250214e`  
		Last Modified: Tue, 09 Jun 2026 20:33:48 GMT  
		Size: 3.8 MB (3833955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0bdd5dc720242a7e084697c14693e733e595ecd986eb2cc0f8a575aab48705`  
		Last Modified: Wed, 10 Jun 2026 18:15:29 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4bbfdd2990992d37f6018cbadcbaa970bb884e82c6d96d4600fb8cba166859`  
		Last Modified: Wed, 10 Jun 2026 18:15:29 GMT  
		Size: 126.2 KB (126245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5863f1a7869d33f359d606dd6947e23ca7fcc10f7c0d821a26c0b4e7adee77a3`  
		Last Modified: Wed, 10 Jun 2026 18:15:29 GMT  
		Size: 4.4 MB (4415538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b4bc2207922da164d3875abd76e10f11db496e6018180dce3ecbe5026a026f`  
		Last Modified: Wed, 10 Jun 2026 18:15:29 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b342b964ce20aa37c3d771357dde123e5a25ec2695cfba9aa7f6278e5e11fbf5`  
		Last Modified: Wed, 10 Jun 2026 18:15:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:017746bf102a5b7fdcb2f023fcb1a50c67ccb725fc105d89d0985e7aa46df95d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9616f658a36ce366c7c705240e2d967a302d803c4b1d73c377f8c64c25bdd2da`

```dockerfile
```

-	Layers:
	-	`sha256:6682009a8af30b6df10790ac6a62a9c3850d2aacdd06b951b0016026377a7f86`  
		Last Modified: Wed, 10 Jun 2026 18:15:29 GMT  
		Size: 94.3 KB (94304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c4569b2982a6a6f9f6ef930d40862043152589ac307ce81183a90bec91860cf`  
		Last Modified: Wed, 10 Jun 2026 18:15:29 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:c5ade8803ceb4e9ca036c3b1be9b6d970446c324b3e38080eed03b1998db8dd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7915430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:450fb4c40f2f1f7e5517aeddc4034b6229d7fb443c71c7c6dd0f3697aaa05461`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:23:10 GMT
ADD alpine-minirootfs-3.24.0-riscv64.tar.gz / # buildkit
# Wed, 10 Jun 2026 00:23:10 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:13:44 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:13:48 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:27:33 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:27:33 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:27:33 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:27:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:27:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:27:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:27:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:27:34 GMT
USER memcache
# Wed, 10 Jun 2026 18:27:34 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:27:34 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3d2f730dbeff3c2e957669de5d586604e82939f67ebfd9142872c9ff56603e07`  
		Last Modified: Wed, 10 Jun 2026 00:23:34 GMT  
		Size: 3.6 MB (3591852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87dad43f2e16c76f58e5e2753765caecdfbc1feb72bd08841a5964c4da7ab22c`  
		Last Modified: Wed, 10 Jun 2026 18:27:59 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac80a7065539574d0aff698d1fc76d3744f2f00b3e6d68314fb4cb84f0e37d7`  
		Last Modified: Wed, 10 Jun 2026 18:27:59 GMT  
		Size: 108.9 KB (108888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef744b36d8487e33054d1c30cfebd18490c05aca17b4f574720ce1dda3c78412`  
		Last Modified: Wed, 10 Jun 2026 18:28:00 GMT  
		Size: 4.2 MB (4213337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a136ba7f82c19e371c7e2c7a4ee25ed1de41441c27feecbc6b989e7c79afe3f`  
		Last Modified: Wed, 10 Jun 2026 18:27:59 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:653819d879edda4020f6a5bd344241c2e118781fbd50319cfabeb965557c4234`  
		Last Modified: Wed, 10 Jun 2026 18:28:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7715a9e3170ec3a2143b197fb80db0a2d670d751a4d710a95942ec384df85a58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4297ab54a68ba59e6d3d700921a359e4850605f249ec473c36391bf423a0017b`

```dockerfile
```

-	Layers:
	-	`sha256:a1889ec9b4bd651c813e65a363b785ace86c68a6095f41a397172d7acdc47058`  
		Last Modified: Wed, 10 Jun 2026 18:27:59 GMT  
		Size: 94.3 KB (94300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec157ceb7ee3f109ef2e714168e5904e088b28fcab859065403f0a617f121d82`  
		Last Modified: Wed, 10 Jun 2026 18:27:59 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:084c53e2e39a12bbca6189febd6d4e2aadf6ccdd85445553f9a237d6c3608c3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8107287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de51c430e27f993bbd7f1be7334cdb2818c849b8e7c017552ff8cdb5fb2c2949`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2026 20:18:16 GMT
ADD alpine-minirootfs-3.24.0-s390x.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:18:16 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:20:00 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:20:05 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:49:55 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:49:55 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:49:55 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:49:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:49:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:50:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:50:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:50:01 GMT
USER memcache
# Wed, 10 Jun 2026 18:50:01 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:50:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4c421b7ac5771added0d41fbc2e1c815472072561366ed82ab9e16b926cb03c6`  
		Last Modified: Tue, 09 Jun 2026 20:18:26 GMT  
		Size: 3.7 MB (3730217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0711a972fdad3ac072246017b11d2279363fa9074279aef5f300474872ae8bd7`  
		Last Modified: Wed, 10 Jun 2026 18:50:43 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a6a5c3b22bd7a4743610e767f8e08c5bb66379e7420935b5ad890c02be1af8`  
		Last Modified: Wed, 10 Jun 2026 18:50:43 GMT  
		Size: 114.3 KB (114292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:791d693469c94f11b8cfc977eadf134459f8e13d0f21ba48b4b04664df753f71`  
		Last Modified: Wed, 10 Jun 2026 18:50:45 GMT  
		Size: 4.3 MB (4261419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dd8c588e70e6f166476b33c198ee2d77a7b5d952207365e20799c8415f1fb27`  
		Last Modified: Wed, 10 Jun 2026 18:50:43 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c17c044babfc798701d6dbfde3b27966cccf07ccfffb49929017250e203878c5`  
		Last Modified: Wed, 10 Jun 2026 18:50:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:b86d70017763ec3335085643c4fc858eb4d0ecd80da1533ab7844a082ea2096c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dde6eca01b66c07c19e6987128b39e14d1395da122e9f2a4b85c663667255978`

```dockerfile
```

-	Layers:
	-	`sha256:003e58d9144c67eaa1a52c05fa8df2908964b8150d09d954940f1c90844cf74c`  
		Last Modified: Wed, 10 Jun 2026 18:50:43 GMT  
		Size: 94.2 KB (94246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd8a5086e89c6d7f95c68b2f90f54a4730f057dc511969769bfe3bcc9a2d57da`  
		Last Modified: Wed, 10 Jun 2026 18:50:44 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine3.24`

```console
$ docker pull memcached@sha256:24f46bd5e6250525c4219957edf4490e1dcff92a8c798325d9422798af8d02db
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
$ docker pull memcached@sha256:cb2d8176cf730b6e493f47a20c202e3785450ce97ac94eca4907d7690c1af307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8429739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b50ffd1c04d8028fbb3c3420cc1d60aed911ce7c0e45a4965310fce274d53ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:31 GMT
ADD alpine-minirootfs-3.24.0-x86_64.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:31 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:14:19 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:14:20 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:16:57 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:16:57 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:16:57 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:16:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:16:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:16:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:16:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:16:57 GMT
USER memcache
# Wed, 10 Jun 2026 18:16:57 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:16:57 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9b70e313681f44d32991ec943f89228bc91d7431d4a84feafc269a76e3f96a63`  
		Last Modified: Tue, 09 Jun 2026 20:11:36 GMT  
		Size: 3.9 MB (3866755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e3046ed30b13ad06ce756a4c6583941eb759870afa70848109fd8c0064519f`  
		Last Modified: Wed, 10 Jun 2026 18:17:02 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c4e652e501aa70e550ad140cba871ada70bf7f3a31a1f25b992df3b69702af`  
		Last Modified: Wed, 10 Jun 2026 18:17:03 GMT  
		Size: 106.1 KB (106068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7b3e28eeb74ba3ce98c770af704a09d48456fc4b9d0ac8ec337c30cc95f2e3`  
		Last Modified: Wed, 10 Jun 2026 18:17:03 GMT  
		Size: 4.5 MB (4455567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4da70a2e9c741455aab8b6eeecd686f79532427ac6f458f4c6df4203fb17b42`  
		Last Modified: Wed, 10 Jun 2026 18:17:02 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d9e7ab7a8a69db82d54cd5953d81a8d174f46e493dc10bcead49919ab63b80`  
		Last Modified: Wed, 10 Jun 2026 18:17:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:423aea49db161bc8ab6d8f600ba326351a44d683f648e77c38062ced876533b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6a9742524b3a500c65fd2ff4ee0ed6498d3286356dbe7b04507f7903496dcc2`

```dockerfile
```

-	Layers:
	-	`sha256:1967442755aa01c5b18b82d15e09215bb060a9a4725e69476dffdde04a11a174`  
		Last Modified: Wed, 10 Jun 2026 18:17:03 GMT  
		Size: 94.9 KB (94897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:241a34a97ffb94fa781f2bf870cb96be626d17c16414915a8e5737d781b620d1`  
		Last Modified: Wed, 10 Jun 2026 18:17:02 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.24` - linux; arm variant v6

```console
$ docker pull memcached@sha256:32cf627ba476a687feb05fc278c1ec76e5904f2d070ec439c114e910c770d514
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7724160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:232f09c26d3bbd4437aa7cadb96874736aca039e389a58df9594e5b6aba964b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:25 GMT
ADD alpine-minirootfs-3.24.0-armhf.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:25 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:13:29 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:13:30 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:35:53 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:35:53 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:35:53 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:35:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:35:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:35:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:35:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:35:53 GMT
USER memcache
# Wed, 10 Jun 2026 18:35:53 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:35:53 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d44d12cd5c9ecc8e4b75201d67412f77b79157eaffaaed75c3b717bcd42f61e1`  
		Last Modified: Tue, 09 Jun 2026 20:11:29 GMT  
		Size: 3.6 MB (3575314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573a1d7a0131b3bb62a9b1e14cb0e8cf4d866ce7ec68a2d4a2ac402c7357b24e`  
		Last Modified: Wed, 10 Jun 2026 18:35:57 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608fb78ccee6e69c390e8ce51d8c49d4bdac4d71cf50cc5c6e457dca3274ebf7`  
		Last Modified: Wed, 10 Jun 2026 18:35:57 GMT  
		Size: 102.6 KB (102627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e548b50ad164ad49e2be2cc291334c46cf327222804043ba289bc49d36fb202`  
		Last Modified: Wed, 10 Jun 2026 18:35:57 GMT  
		Size: 4.0 MB (4044869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3288904307a586b305537393c2f20cfcb8d98edcb8c0e51b89036d575c960cb`  
		Last Modified: Wed, 10 Jun 2026 18:35:57 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae9e7c1276f81bfb68d7489c74761c88a037e47d4b72983353c03196b97b218`  
		Last Modified: Wed, 10 Jun 2026 18:35:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:1b8dbbfd625301ca11ebb50f807fdf9060dfc1fa7f9247b6cd5556775c85c77c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f6e1cafb6d6aa90021214a707bd44e9808680bd0fcf819c2bf76e1e97319038`

```dockerfile
```

-	Layers:
	-	`sha256:added378a7ae281e9cd9406a18fcf5d2639f6ffcbf0b2f5fb5fcec47db001204`  
		Last Modified: Wed, 10 Jun 2026 18:35:57 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.24` - linux; arm variant v7

```console
$ docker pull memcached@sha256:01b020198ba0ce8e9af9fb0257ca2487cc71cfec9a953ad04b6cb386059f3bdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7220162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2416c6901535e0b681eeba9d0e010b8030f17e2a0f9a4e8e7bdea9261260886`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2026 20:14:38 GMT
ADD alpine-minirootfs-3.24.0-armv7.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:14:38 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:14:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:14:02 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:16:58 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:16:58 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:16:58 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:16:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:16:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:16:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:16:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:16:59 GMT
USER memcache
# Wed, 10 Jun 2026 18:16:59 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:16:59 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bce674d5697a824549061f4985dfd06a60c018b96ba50b18b7bc1f9ad6143570`  
		Last Modified: Tue, 09 Jun 2026 20:14:43 GMT  
		Size: 3.3 MB (3286160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddccf170e8b5b7071fc7d37c3e7b71b383e42d66ebc8452c8face5ccfc0ba841`  
		Last Modified: Wed, 10 Jun 2026 18:17:04 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d271b94c2d5eb987939fb26d3e872b378914ed230228478c94c4eb9271af3bea`  
		Last Modified: Wed, 10 Jun 2026 18:17:04 GMT  
		Size: 92.4 KB (92371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58107905e1ff79a6248896ab514b9cad8d31bc4ded8616894db922f6d9bc862e`  
		Last Modified: Wed, 10 Jun 2026 18:17:04 GMT  
		Size: 3.8 MB (3840281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1397705fe8ef2c310800a79d7e7f6de7db2ebad65b46e9505ba834b120347c62`  
		Last Modified: Wed, 10 Jun 2026 18:17:04 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06dbe001de1fe8d785dd53bdcb0a65b97ea4a57b4bd839da2e6ef4344226ec07`  
		Last Modified: Wed, 10 Jun 2026 18:17:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:9c08a5c1662aaac2028c9b66d84c8a5ab3ac6ce87d8d1ca8dfb2856bbf331d17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71022047d72bddcc121675d6bbe75bac274911f769029bb179b886d170baeb02`

```dockerfile
```

-	Layers:
	-	`sha256:db4bac74dcb986da8aa5a0e3af57ee133956acb18dac4ae890a9ec074f02c1b5`  
		Last Modified: Wed, 10 Jun 2026 18:17:04 GMT  
		Size: 94.3 KB (94315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a12f73bf7901f75ec1c978ac1cc49ff827de35497af898a05c43fe1d9c753e86`  
		Last Modified: Wed, 10 Jun 2026 18:17:04 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.24` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:16eb5e3d6505a7ef0a633bfe2d01f674184e0f6f9cbe79d241120567b03f054f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9059008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5f2f1760f4a10a67fb7a006f00b172c33b6e530525a2a7bf1f112c44e8a1949`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:09 GMT
ADD alpine-minirootfs-3.24.0-aarch64.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:09 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:12:27 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:12:27 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:15:17 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:15:17 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:15:17 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:15:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:15:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:15:17 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:15:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:15:17 GMT
USER memcache
# Wed, 10 Jun 2026 18:15:17 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:15:17 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c05efffaed614b5ff4e3b9a80136e7c0eed0b47f434802c81baf254c0defca91`  
		Last Modified: Tue, 09 Jun 2026 20:11:14 GMT  
		Size: 4.2 MB (4202330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e456d8825f29dfd65b2051f5b44b6de5920128138737cbd93cbae351cc088ce`  
		Last Modified: Wed, 10 Jun 2026 18:15:22 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1569a3fe1932b7d0793450f547c0e3ffcd659baefbc266fc8febd0f82dd3b197`  
		Last Modified: Wed, 10 Jun 2026 18:15:23 GMT  
		Size: 121.9 KB (121857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91674cbd7c3a07584ce0b6f5702920f8c878319100d0794e0be633caf4cd702`  
		Last Modified: Wed, 10 Jun 2026 18:15:23 GMT  
		Size: 4.7 MB (4733470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f23ddaee25aadc1b418bf3aa3c117923c06e9cac1b101e927b76def37507cd2`  
		Last Modified: Wed, 10 Jun 2026 18:15:23 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd7c50e090366a1f99c6b319c0f95302b5ce191989df8f66ddb9e1d4d163be0`  
		Last Modified: Wed, 10 Jun 2026 18:15:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:46bff7acd3c1c4e24acda5e4573e853d532c8f880c8c739e9bcc220de4b43b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:399abce8f4883f60c5fe7741d0d7c0b5fd729e48660e5df3829afc60dc755d1c`

```dockerfile
```

-	Layers:
	-	`sha256:c94369062ddc1d7c765eb1aec2fbaeb202af339dcda4691019309c6708106359`  
		Last Modified: Wed, 10 Jun 2026 18:15:22 GMT  
		Size: 94.4 KB (94351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49b2ad2a43e5a3f86c7fe35d36035450993daa3bb8ecaf1ae6d49b858da8d19b`  
		Last Modified: Wed, 10 Jun 2026 18:15:23 GMT  
		Size: 20.7 KB (20727 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.24` - linux; 386

```console
$ docker pull memcached@sha256:f2d4eb8c40d54fdcd5fb0684d29936ebce2fbafe26c26c0c72ae0a9335f06997
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (8024217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07138462285df4cbd1ed2c627e98451dc1a4b43b37e111b2b72e59d154f811ee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2026 20:10:54 GMT
ADD alpine-minirootfs-3.24.0-x86.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:10:54 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:25:31 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:25:32 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:28:16 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:28:16 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:28:16 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:28:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:28:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:28:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:28:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:28:16 GMT
USER memcache
# Wed, 10 Jun 2026 18:28:16 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:28:16 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:14b4480cdb6be1a40aafc14c9089d92843794d03fc3115b849ddc49717c25982`  
		Last Modified: Tue, 09 Jun 2026 20:10:59 GMT  
		Size: 3.7 MB (3691754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14cf249ff43e2409a2718494167fe16786f19bdc9666b291ba5f4fbb333e382c`  
		Last Modified: Wed, 10 Jun 2026 18:28:21 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9d4516b9de504d8b32b12ee16f3aeb0ed86d6124308df02b6a907e3e0b3ed6`  
		Last Modified: Wed, 10 Jun 2026 18:28:22 GMT  
		Size: 110.7 KB (110732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f550fd7ec906f373bb885a9a587de5a825d95ff63d1353fb88aff5bba428f19a`  
		Last Modified: Wed, 10 Jun 2026 18:28:22 GMT  
		Size: 4.2 MB (4220384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dcc14148666128c245fd38ff2cd067defeb4c4a1acfe2da55983425fe7b5cfd`  
		Last Modified: Wed, 10 Jun 2026 18:28:22 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad5170f36cabc8e1bfed343134a7a78b8ae945e7e73c0428b77c3eb5fddeadb`  
		Last Modified: Wed, 10 Jun 2026 18:28:23 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:12741aadabddc93af391c2b99e0e588138024a0fdb67bcca1191f96869187018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6490fe35195514ccd48669f08b68a82107074785228124b81b6c2e5f6a1133c8`

```dockerfile
```

-	Layers:
	-	`sha256:db2735e9fcf74530bbea1a6790fee5d18607311bb075b0ed4a074e41e6bd0f91`  
		Last Modified: Wed, 10 Jun 2026 18:28:21 GMT  
		Size: 94.9 KB (94852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dcb9494458e7383f61847d265cf37857313b48a9e23522119233328d3f808c6`  
		Last Modified: Wed, 10 Jun 2026 18:28:22 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.24` - linux; ppc64le

```console
$ docker pull memcached@sha256:a51985551b3de3fae96ad49d7bd83e4bed7b04338ab59c8f1d0615a8104d681f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8377092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eec58c326d0b7fb84ebe5bb90c97ac84004c7a43061561a4551c88cadb9bbea3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2026 20:33:34 GMT
ADD alpine-minirootfs-3.24.0-ppc64le.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:33:34 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:12:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:12:36 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:15:17 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:15:17 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:15:17 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:15:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:15:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:15:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:15:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:15:18 GMT
USER memcache
# Wed, 10 Jun 2026 18:15:18 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:15:18 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:73fae309fa62bb67bbe20b40696c81037cf9f77919ce6726a7e535ae9250214e`  
		Last Modified: Tue, 09 Jun 2026 20:33:48 GMT  
		Size: 3.8 MB (3833955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0bdd5dc720242a7e084697c14693e733e595ecd986eb2cc0f8a575aab48705`  
		Last Modified: Wed, 10 Jun 2026 18:15:29 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4bbfdd2990992d37f6018cbadcbaa970bb884e82c6d96d4600fb8cba166859`  
		Last Modified: Wed, 10 Jun 2026 18:15:29 GMT  
		Size: 126.2 KB (126245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5863f1a7869d33f359d606dd6947e23ca7fcc10f7c0d821a26c0b4e7adee77a3`  
		Last Modified: Wed, 10 Jun 2026 18:15:29 GMT  
		Size: 4.4 MB (4415538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b4bc2207922da164d3875abd76e10f11db496e6018180dce3ecbe5026a026f`  
		Last Modified: Wed, 10 Jun 2026 18:15:29 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b342b964ce20aa37c3d771357dde123e5a25ec2695cfba9aa7f6278e5e11fbf5`  
		Last Modified: Wed, 10 Jun 2026 18:15:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:017746bf102a5b7fdcb2f023fcb1a50c67ccb725fc105d89d0985e7aa46df95d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9616f658a36ce366c7c705240e2d967a302d803c4b1d73c377f8c64c25bdd2da`

```dockerfile
```

-	Layers:
	-	`sha256:6682009a8af30b6df10790ac6a62a9c3850d2aacdd06b951b0016026377a7f86`  
		Last Modified: Wed, 10 Jun 2026 18:15:29 GMT  
		Size: 94.3 KB (94304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c4569b2982a6a6f9f6ef930d40862043152589ac307ce81183a90bec91860cf`  
		Last Modified: Wed, 10 Jun 2026 18:15:29 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.24` - linux; riscv64

```console
$ docker pull memcached@sha256:c5ade8803ceb4e9ca036c3b1be9b6d970446c324b3e38080eed03b1998db8dd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7915430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:450fb4c40f2f1f7e5517aeddc4034b6229d7fb443c71c7c6dd0f3697aaa05461`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:23:10 GMT
ADD alpine-minirootfs-3.24.0-riscv64.tar.gz / # buildkit
# Wed, 10 Jun 2026 00:23:10 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:13:44 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:13:48 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:27:33 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:27:33 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:27:33 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:27:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:27:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:27:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:27:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:27:34 GMT
USER memcache
# Wed, 10 Jun 2026 18:27:34 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:27:34 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3d2f730dbeff3c2e957669de5d586604e82939f67ebfd9142872c9ff56603e07`  
		Last Modified: Wed, 10 Jun 2026 00:23:34 GMT  
		Size: 3.6 MB (3591852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87dad43f2e16c76f58e5e2753765caecdfbc1feb72bd08841a5964c4da7ab22c`  
		Last Modified: Wed, 10 Jun 2026 18:27:59 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac80a7065539574d0aff698d1fc76d3744f2f00b3e6d68314fb4cb84f0e37d7`  
		Last Modified: Wed, 10 Jun 2026 18:27:59 GMT  
		Size: 108.9 KB (108888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef744b36d8487e33054d1c30cfebd18490c05aca17b4f574720ce1dda3c78412`  
		Last Modified: Wed, 10 Jun 2026 18:28:00 GMT  
		Size: 4.2 MB (4213337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a136ba7f82c19e371c7e2c7a4ee25ed1de41441c27feecbc6b989e7c79afe3f`  
		Last Modified: Wed, 10 Jun 2026 18:27:59 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:653819d879edda4020f6a5bd344241c2e118781fbd50319cfabeb965557c4234`  
		Last Modified: Wed, 10 Jun 2026 18:28:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:7715a9e3170ec3a2143b197fb80db0a2d670d751a4d710a95942ec384df85a58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4297ab54a68ba59e6d3d700921a359e4850605f249ec473c36391bf423a0017b`

```dockerfile
```

-	Layers:
	-	`sha256:a1889ec9b4bd651c813e65a363b785ace86c68a6095f41a397172d7acdc47058`  
		Last Modified: Wed, 10 Jun 2026 18:27:59 GMT  
		Size: 94.3 KB (94300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec157ceb7ee3f109ef2e714168e5904e088b28fcab859065403f0a617f121d82`  
		Last Modified: Wed, 10 Jun 2026 18:27:59 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.24` - linux; s390x

```console
$ docker pull memcached@sha256:084c53e2e39a12bbca6189febd6d4e2aadf6ccdd85445553f9a237d6c3608c3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8107287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de51c430e27f993bbd7f1be7334cdb2818c849b8e7c017552ff8cdb5fb2c2949`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2026 20:18:16 GMT
ADD alpine-minirootfs-3.24.0-s390x.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:18:16 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:20:00 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:20:05 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:49:55 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:49:55 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:49:55 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:49:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:49:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:50:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:50:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:50:01 GMT
USER memcache
# Wed, 10 Jun 2026 18:50:01 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:50:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4c421b7ac5771added0d41fbc2e1c815472072561366ed82ab9e16b926cb03c6`  
		Last Modified: Tue, 09 Jun 2026 20:18:26 GMT  
		Size: 3.7 MB (3730217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0711a972fdad3ac072246017b11d2279363fa9074279aef5f300474872ae8bd7`  
		Last Modified: Wed, 10 Jun 2026 18:50:43 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a6a5c3b22bd7a4743610e767f8e08c5bb66379e7420935b5ad890c02be1af8`  
		Last Modified: Wed, 10 Jun 2026 18:50:43 GMT  
		Size: 114.3 KB (114292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:791d693469c94f11b8cfc977eadf134459f8e13d0f21ba48b4b04664df753f71`  
		Last Modified: Wed, 10 Jun 2026 18:50:45 GMT  
		Size: 4.3 MB (4261419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dd8c588e70e6f166476b33c198ee2d77a7b5d952207365e20799c8415f1fb27`  
		Last Modified: Wed, 10 Jun 2026 18:50:43 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c17c044babfc798701d6dbfde3b27966cccf07ccfffb49929017250e203878c5`  
		Last Modified: Wed, 10 Jun 2026 18:50:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:b86d70017763ec3335085643c4fc858eb4d0ecd80da1533ab7844a082ea2096c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dde6eca01b66c07c19e6987128b39e14d1395da122e9f2a4b85c663667255978`

```dockerfile
```

-	Layers:
	-	`sha256:003e58d9144c67eaa1a52c05fa8df2908964b8150d09d954940f1c90844cf74c`  
		Last Modified: Wed, 10 Jun 2026 18:50:43 GMT  
		Size: 94.2 KB (94246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd8a5086e89c6d7f95c68b2f90f54a4730f057dc511969769bfe3bcc9a2d57da`  
		Last Modified: Wed, 10 Jun 2026 18:50:44 GMT  
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
$ docker pull memcached@sha256:24f46bd5e6250525c4219957edf4490e1dcff92a8c798325d9422798af8d02db
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
$ docker pull memcached@sha256:cb2d8176cf730b6e493f47a20c202e3785450ce97ac94eca4907d7690c1af307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8429739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b50ffd1c04d8028fbb3c3420cc1d60aed911ce7c0e45a4965310fce274d53ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:31 GMT
ADD alpine-minirootfs-3.24.0-x86_64.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:31 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:14:19 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:14:20 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:16:57 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:16:57 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:16:57 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:16:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:16:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:16:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:16:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:16:57 GMT
USER memcache
# Wed, 10 Jun 2026 18:16:57 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:16:57 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9b70e313681f44d32991ec943f89228bc91d7431d4a84feafc269a76e3f96a63`  
		Last Modified: Tue, 09 Jun 2026 20:11:36 GMT  
		Size: 3.9 MB (3866755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e3046ed30b13ad06ce756a4c6583941eb759870afa70848109fd8c0064519f`  
		Last Modified: Wed, 10 Jun 2026 18:17:02 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c4e652e501aa70e550ad140cba871ada70bf7f3a31a1f25b992df3b69702af`  
		Last Modified: Wed, 10 Jun 2026 18:17:03 GMT  
		Size: 106.1 KB (106068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7b3e28eeb74ba3ce98c770af704a09d48456fc4b9d0ac8ec337c30cc95f2e3`  
		Last Modified: Wed, 10 Jun 2026 18:17:03 GMT  
		Size: 4.5 MB (4455567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4da70a2e9c741455aab8b6eeecd686f79532427ac6f458f4c6df4203fb17b42`  
		Last Modified: Wed, 10 Jun 2026 18:17:02 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d9e7ab7a8a69db82d54cd5953d81a8d174f46e493dc10bcead49919ab63b80`  
		Last Modified: Wed, 10 Jun 2026 18:17:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:423aea49db161bc8ab6d8f600ba326351a44d683f648e77c38062ced876533b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6a9742524b3a500c65fd2ff4ee0ed6498d3286356dbe7b04507f7903496dcc2`

```dockerfile
```

-	Layers:
	-	`sha256:1967442755aa01c5b18b82d15e09215bb060a9a4725e69476dffdde04a11a174`  
		Last Modified: Wed, 10 Jun 2026 18:17:03 GMT  
		Size: 94.9 KB (94897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:241a34a97ffb94fa781f2bf870cb96be626d17c16414915a8e5737d781b620d1`  
		Last Modified: Wed, 10 Jun 2026 18:17:02 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:32cf627ba476a687feb05fc278c1ec76e5904f2d070ec439c114e910c770d514
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7724160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:232f09c26d3bbd4437aa7cadb96874736aca039e389a58df9594e5b6aba964b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:25 GMT
ADD alpine-minirootfs-3.24.0-armhf.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:25 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:13:29 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:13:30 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:35:53 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:35:53 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:35:53 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:35:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:35:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:35:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:35:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:35:53 GMT
USER memcache
# Wed, 10 Jun 2026 18:35:53 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:35:53 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d44d12cd5c9ecc8e4b75201d67412f77b79157eaffaaed75c3b717bcd42f61e1`  
		Last Modified: Tue, 09 Jun 2026 20:11:29 GMT  
		Size: 3.6 MB (3575314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573a1d7a0131b3bb62a9b1e14cb0e8cf4d866ce7ec68a2d4a2ac402c7357b24e`  
		Last Modified: Wed, 10 Jun 2026 18:35:57 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608fb78ccee6e69c390e8ce51d8c49d4bdac4d71cf50cc5c6e457dca3274ebf7`  
		Last Modified: Wed, 10 Jun 2026 18:35:57 GMT  
		Size: 102.6 KB (102627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e548b50ad164ad49e2be2cc291334c46cf327222804043ba289bc49d36fb202`  
		Last Modified: Wed, 10 Jun 2026 18:35:57 GMT  
		Size: 4.0 MB (4044869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3288904307a586b305537393c2f20cfcb8d98edcb8c0e51b89036d575c960cb`  
		Last Modified: Wed, 10 Jun 2026 18:35:57 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae9e7c1276f81bfb68d7489c74761c88a037e47d4b72983353c03196b97b218`  
		Last Modified: Wed, 10 Jun 2026 18:35:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:1b8dbbfd625301ca11ebb50f807fdf9060dfc1fa7f9247b6cd5556775c85c77c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f6e1cafb6d6aa90021214a707bd44e9808680bd0fcf819c2bf76e1e97319038`

```dockerfile
```

-	Layers:
	-	`sha256:added378a7ae281e9cd9406a18fcf5d2639f6ffcbf0b2f5fb5fcec47db001204`  
		Last Modified: Wed, 10 Jun 2026 18:35:57 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:01b020198ba0ce8e9af9fb0257ca2487cc71cfec9a953ad04b6cb386059f3bdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7220162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2416c6901535e0b681eeba9d0e010b8030f17e2a0f9a4e8e7bdea9261260886`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2026 20:14:38 GMT
ADD alpine-minirootfs-3.24.0-armv7.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:14:38 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:14:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:14:02 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:16:58 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:16:58 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:16:58 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:16:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:16:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:16:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:16:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:16:59 GMT
USER memcache
# Wed, 10 Jun 2026 18:16:59 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:16:59 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bce674d5697a824549061f4985dfd06a60c018b96ba50b18b7bc1f9ad6143570`  
		Last Modified: Tue, 09 Jun 2026 20:14:43 GMT  
		Size: 3.3 MB (3286160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddccf170e8b5b7071fc7d37c3e7b71b383e42d66ebc8452c8face5ccfc0ba841`  
		Last Modified: Wed, 10 Jun 2026 18:17:04 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d271b94c2d5eb987939fb26d3e872b378914ed230228478c94c4eb9271af3bea`  
		Last Modified: Wed, 10 Jun 2026 18:17:04 GMT  
		Size: 92.4 KB (92371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58107905e1ff79a6248896ab514b9cad8d31bc4ded8616894db922f6d9bc862e`  
		Last Modified: Wed, 10 Jun 2026 18:17:04 GMT  
		Size: 3.8 MB (3840281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1397705fe8ef2c310800a79d7e7f6de7db2ebad65b46e9505ba834b120347c62`  
		Last Modified: Wed, 10 Jun 2026 18:17:04 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06dbe001de1fe8d785dd53bdcb0a65b97ea4a57b4bd839da2e6ef4344226ec07`  
		Last Modified: Wed, 10 Jun 2026 18:17:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:9c08a5c1662aaac2028c9b66d84c8a5ab3ac6ce87d8d1ca8dfb2856bbf331d17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71022047d72bddcc121675d6bbe75bac274911f769029bb179b886d170baeb02`

```dockerfile
```

-	Layers:
	-	`sha256:db4bac74dcb986da8aa5a0e3af57ee133956acb18dac4ae890a9ec074f02c1b5`  
		Last Modified: Wed, 10 Jun 2026 18:17:04 GMT  
		Size: 94.3 KB (94315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a12f73bf7901f75ec1c978ac1cc49ff827de35497af898a05c43fe1d9c753e86`  
		Last Modified: Wed, 10 Jun 2026 18:17:04 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:16eb5e3d6505a7ef0a633bfe2d01f674184e0f6f9cbe79d241120567b03f054f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9059008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5f2f1760f4a10a67fb7a006f00b172c33b6e530525a2a7bf1f112c44e8a1949`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:09 GMT
ADD alpine-minirootfs-3.24.0-aarch64.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:09 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:12:27 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:12:27 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:15:17 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:15:17 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:15:17 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:15:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:15:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:15:17 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:15:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:15:17 GMT
USER memcache
# Wed, 10 Jun 2026 18:15:17 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:15:17 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c05efffaed614b5ff4e3b9a80136e7c0eed0b47f434802c81baf254c0defca91`  
		Last Modified: Tue, 09 Jun 2026 20:11:14 GMT  
		Size: 4.2 MB (4202330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e456d8825f29dfd65b2051f5b44b6de5920128138737cbd93cbae351cc088ce`  
		Last Modified: Wed, 10 Jun 2026 18:15:22 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1569a3fe1932b7d0793450f547c0e3ffcd659baefbc266fc8febd0f82dd3b197`  
		Last Modified: Wed, 10 Jun 2026 18:15:23 GMT  
		Size: 121.9 KB (121857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91674cbd7c3a07584ce0b6f5702920f8c878319100d0794e0be633caf4cd702`  
		Last Modified: Wed, 10 Jun 2026 18:15:23 GMT  
		Size: 4.7 MB (4733470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f23ddaee25aadc1b418bf3aa3c117923c06e9cac1b101e927b76def37507cd2`  
		Last Modified: Wed, 10 Jun 2026 18:15:23 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd7c50e090366a1f99c6b319c0f95302b5ce191989df8f66ddb9e1d4d163be0`  
		Last Modified: Wed, 10 Jun 2026 18:15:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:46bff7acd3c1c4e24acda5e4573e853d532c8f880c8c739e9bcc220de4b43b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:399abce8f4883f60c5fe7741d0d7c0b5fd729e48660e5df3829afc60dc755d1c`

```dockerfile
```

-	Layers:
	-	`sha256:c94369062ddc1d7c765eb1aec2fbaeb202af339dcda4691019309c6708106359`  
		Last Modified: Wed, 10 Jun 2026 18:15:22 GMT  
		Size: 94.4 KB (94351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49b2ad2a43e5a3f86c7fe35d36035450993daa3bb8ecaf1ae6d49b858da8d19b`  
		Last Modified: Wed, 10 Jun 2026 18:15:23 GMT  
		Size: 20.7 KB (20727 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; 386

```console
$ docker pull memcached@sha256:f2d4eb8c40d54fdcd5fb0684d29936ebce2fbafe26c26c0c72ae0a9335f06997
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (8024217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07138462285df4cbd1ed2c627e98451dc1a4b43b37e111b2b72e59d154f811ee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2026 20:10:54 GMT
ADD alpine-minirootfs-3.24.0-x86.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:10:54 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:25:31 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:25:32 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:28:16 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:28:16 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:28:16 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:28:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:28:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:28:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:28:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:28:16 GMT
USER memcache
# Wed, 10 Jun 2026 18:28:16 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:28:16 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:14b4480cdb6be1a40aafc14c9089d92843794d03fc3115b849ddc49717c25982`  
		Last Modified: Tue, 09 Jun 2026 20:10:59 GMT  
		Size: 3.7 MB (3691754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14cf249ff43e2409a2718494167fe16786f19bdc9666b291ba5f4fbb333e382c`  
		Last Modified: Wed, 10 Jun 2026 18:28:21 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9d4516b9de504d8b32b12ee16f3aeb0ed86d6124308df02b6a907e3e0b3ed6`  
		Last Modified: Wed, 10 Jun 2026 18:28:22 GMT  
		Size: 110.7 KB (110732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f550fd7ec906f373bb885a9a587de5a825d95ff63d1353fb88aff5bba428f19a`  
		Last Modified: Wed, 10 Jun 2026 18:28:22 GMT  
		Size: 4.2 MB (4220384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dcc14148666128c245fd38ff2cd067defeb4c4a1acfe2da55983425fe7b5cfd`  
		Last Modified: Wed, 10 Jun 2026 18:28:22 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad5170f36cabc8e1bfed343134a7a78b8ae945e7e73c0428b77c3eb5fddeadb`  
		Last Modified: Wed, 10 Jun 2026 18:28:23 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:12741aadabddc93af391c2b99e0e588138024a0fdb67bcca1191f96869187018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6490fe35195514ccd48669f08b68a82107074785228124b81b6c2e5f6a1133c8`

```dockerfile
```

-	Layers:
	-	`sha256:db2735e9fcf74530bbea1a6790fee5d18607311bb075b0ed4a074e41e6bd0f91`  
		Last Modified: Wed, 10 Jun 2026 18:28:21 GMT  
		Size: 94.9 KB (94852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dcb9494458e7383f61847d265cf37857313b48a9e23522119233328d3f808c6`  
		Last Modified: Wed, 10 Jun 2026 18:28:22 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:a51985551b3de3fae96ad49d7bd83e4bed7b04338ab59c8f1d0615a8104d681f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8377092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eec58c326d0b7fb84ebe5bb90c97ac84004c7a43061561a4551c88cadb9bbea3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2026 20:33:34 GMT
ADD alpine-minirootfs-3.24.0-ppc64le.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:33:34 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:12:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:12:36 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:15:17 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:15:17 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:15:17 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:15:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:15:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:15:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:15:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:15:18 GMT
USER memcache
# Wed, 10 Jun 2026 18:15:18 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:15:18 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:73fae309fa62bb67bbe20b40696c81037cf9f77919ce6726a7e535ae9250214e`  
		Last Modified: Tue, 09 Jun 2026 20:33:48 GMT  
		Size: 3.8 MB (3833955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0bdd5dc720242a7e084697c14693e733e595ecd986eb2cc0f8a575aab48705`  
		Last Modified: Wed, 10 Jun 2026 18:15:29 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4bbfdd2990992d37f6018cbadcbaa970bb884e82c6d96d4600fb8cba166859`  
		Last Modified: Wed, 10 Jun 2026 18:15:29 GMT  
		Size: 126.2 KB (126245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5863f1a7869d33f359d606dd6947e23ca7fcc10f7c0d821a26c0b4e7adee77a3`  
		Last Modified: Wed, 10 Jun 2026 18:15:29 GMT  
		Size: 4.4 MB (4415538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b4bc2207922da164d3875abd76e10f11db496e6018180dce3ecbe5026a026f`  
		Last Modified: Wed, 10 Jun 2026 18:15:29 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b342b964ce20aa37c3d771357dde123e5a25ec2695cfba9aa7f6278e5e11fbf5`  
		Last Modified: Wed, 10 Jun 2026 18:15:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:017746bf102a5b7fdcb2f023fcb1a50c67ccb725fc105d89d0985e7aa46df95d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9616f658a36ce366c7c705240e2d967a302d803c4b1d73c377f8c64c25bdd2da`

```dockerfile
```

-	Layers:
	-	`sha256:6682009a8af30b6df10790ac6a62a9c3850d2aacdd06b951b0016026377a7f86`  
		Last Modified: Wed, 10 Jun 2026 18:15:29 GMT  
		Size: 94.3 KB (94304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c4569b2982a6a6f9f6ef930d40862043152589ac307ce81183a90bec91860cf`  
		Last Modified: Wed, 10 Jun 2026 18:15:29 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:c5ade8803ceb4e9ca036c3b1be9b6d970446c324b3e38080eed03b1998db8dd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7915430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:450fb4c40f2f1f7e5517aeddc4034b6229d7fb443c71c7c6dd0f3697aaa05461`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:23:10 GMT
ADD alpine-minirootfs-3.24.0-riscv64.tar.gz / # buildkit
# Wed, 10 Jun 2026 00:23:10 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:13:44 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:13:48 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:27:33 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:27:33 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:27:33 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:27:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:27:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:27:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:27:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:27:34 GMT
USER memcache
# Wed, 10 Jun 2026 18:27:34 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:27:34 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3d2f730dbeff3c2e957669de5d586604e82939f67ebfd9142872c9ff56603e07`  
		Last Modified: Wed, 10 Jun 2026 00:23:34 GMT  
		Size: 3.6 MB (3591852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87dad43f2e16c76f58e5e2753765caecdfbc1feb72bd08841a5964c4da7ab22c`  
		Last Modified: Wed, 10 Jun 2026 18:27:59 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac80a7065539574d0aff698d1fc76d3744f2f00b3e6d68314fb4cb84f0e37d7`  
		Last Modified: Wed, 10 Jun 2026 18:27:59 GMT  
		Size: 108.9 KB (108888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef744b36d8487e33054d1c30cfebd18490c05aca17b4f574720ce1dda3c78412`  
		Last Modified: Wed, 10 Jun 2026 18:28:00 GMT  
		Size: 4.2 MB (4213337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a136ba7f82c19e371c7e2c7a4ee25ed1de41441c27feecbc6b989e7c79afe3f`  
		Last Modified: Wed, 10 Jun 2026 18:27:59 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:653819d879edda4020f6a5bd344241c2e118781fbd50319cfabeb965557c4234`  
		Last Modified: Wed, 10 Jun 2026 18:28:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7715a9e3170ec3a2143b197fb80db0a2d670d751a4d710a95942ec384df85a58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4297ab54a68ba59e6d3d700921a359e4850605f249ec473c36391bf423a0017b`

```dockerfile
```

-	Layers:
	-	`sha256:a1889ec9b4bd651c813e65a363b785ace86c68a6095f41a397172d7acdc47058`  
		Last Modified: Wed, 10 Jun 2026 18:27:59 GMT  
		Size: 94.3 KB (94300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec157ceb7ee3f109ef2e714168e5904e088b28fcab859065403f0a617f121d82`  
		Last Modified: Wed, 10 Jun 2026 18:27:59 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:084c53e2e39a12bbca6189febd6d4e2aadf6ccdd85445553f9a237d6c3608c3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8107287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de51c430e27f993bbd7f1be7334cdb2818c849b8e7c017552ff8cdb5fb2c2949`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2026 20:18:16 GMT
ADD alpine-minirootfs-3.24.0-s390x.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:18:16 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:20:00 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:20:05 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:49:55 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:49:55 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:49:55 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:49:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:49:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:50:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:50:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:50:01 GMT
USER memcache
# Wed, 10 Jun 2026 18:50:01 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:50:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4c421b7ac5771added0d41fbc2e1c815472072561366ed82ab9e16b926cb03c6`  
		Last Modified: Tue, 09 Jun 2026 20:18:26 GMT  
		Size: 3.7 MB (3730217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0711a972fdad3ac072246017b11d2279363fa9074279aef5f300474872ae8bd7`  
		Last Modified: Wed, 10 Jun 2026 18:50:43 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a6a5c3b22bd7a4743610e767f8e08c5bb66379e7420935b5ad890c02be1af8`  
		Last Modified: Wed, 10 Jun 2026 18:50:43 GMT  
		Size: 114.3 KB (114292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:791d693469c94f11b8cfc977eadf134459f8e13d0f21ba48b4b04664df753f71`  
		Last Modified: Wed, 10 Jun 2026 18:50:45 GMT  
		Size: 4.3 MB (4261419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dd8c588e70e6f166476b33c198ee2d77a7b5d952207365e20799c8415f1fb27`  
		Last Modified: Wed, 10 Jun 2026 18:50:43 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c17c044babfc798701d6dbfde3b27966cccf07ccfffb49929017250e203878c5`  
		Last Modified: Wed, 10 Jun 2026 18:50:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:b86d70017763ec3335085643c4fc858eb4d0ecd80da1533ab7844a082ea2096c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dde6eca01b66c07c19e6987128b39e14d1395da122e9f2a4b85c663667255978`

```dockerfile
```

-	Layers:
	-	`sha256:003e58d9144c67eaa1a52c05fa8df2908964b8150d09d954940f1c90844cf74c`  
		Last Modified: Wed, 10 Jun 2026 18:50:43 GMT  
		Size: 94.2 KB (94246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd8a5086e89c6d7f95c68b2f90f54a4730f057dc511969769bfe3bcc9a2d57da`  
		Last Modified: Wed, 10 Jun 2026 18:50:44 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine3.24`

```console
$ docker pull memcached@sha256:24f46bd5e6250525c4219957edf4490e1dcff92a8c798325d9422798af8d02db
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
$ docker pull memcached@sha256:cb2d8176cf730b6e493f47a20c202e3785450ce97ac94eca4907d7690c1af307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8429739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b50ffd1c04d8028fbb3c3420cc1d60aed911ce7c0e45a4965310fce274d53ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:31 GMT
ADD alpine-minirootfs-3.24.0-x86_64.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:31 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:14:19 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:14:20 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:16:57 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:16:57 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:16:57 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:16:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:16:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:16:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:16:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:16:57 GMT
USER memcache
# Wed, 10 Jun 2026 18:16:57 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:16:57 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9b70e313681f44d32991ec943f89228bc91d7431d4a84feafc269a76e3f96a63`  
		Last Modified: Tue, 09 Jun 2026 20:11:36 GMT  
		Size: 3.9 MB (3866755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e3046ed30b13ad06ce756a4c6583941eb759870afa70848109fd8c0064519f`  
		Last Modified: Wed, 10 Jun 2026 18:17:02 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c4e652e501aa70e550ad140cba871ada70bf7f3a31a1f25b992df3b69702af`  
		Last Modified: Wed, 10 Jun 2026 18:17:03 GMT  
		Size: 106.1 KB (106068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7b3e28eeb74ba3ce98c770af704a09d48456fc4b9d0ac8ec337c30cc95f2e3`  
		Last Modified: Wed, 10 Jun 2026 18:17:03 GMT  
		Size: 4.5 MB (4455567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4da70a2e9c741455aab8b6eeecd686f79532427ac6f458f4c6df4203fb17b42`  
		Last Modified: Wed, 10 Jun 2026 18:17:02 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d9e7ab7a8a69db82d54cd5953d81a8d174f46e493dc10bcead49919ab63b80`  
		Last Modified: Wed, 10 Jun 2026 18:17:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:423aea49db161bc8ab6d8f600ba326351a44d683f648e77c38062ced876533b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6a9742524b3a500c65fd2ff4ee0ed6498d3286356dbe7b04507f7903496dcc2`

```dockerfile
```

-	Layers:
	-	`sha256:1967442755aa01c5b18b82d15e09215bb060a9a4725e69476dffdde04a11a174`  
		Last Modified: Wed, 10 Jun 2026 18:17:03 GMT  
		Size: 94.9 KB (94897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:241a34a97ffb94fa781f2bf870cb96be626d17c16414915a8e5737d781b620d1`  
		Last Modified: Wed, 10 Jun 2026 18:17:02 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.24` - linux; arm variant v6

```console
$ docker pull memcached@sha256:32cf627ba476a687feb05fc278c1ec76e5904f2d070ec439c114e910c770d514
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7724160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:232f09c26d3bbd4437aa7cadb96874736aca039e389a58df9594e5b6aba964b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:25 GMT
ADD alpine-minirootfs-3.24.0-armhf.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:25 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:13:29 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:13:30 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:35:53 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:35:53 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:35:53 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:35:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:35:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:35:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:35:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:35:53 GMT
USER memcache
# Wed, 10 Jun 2026 18:35:53 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:35:53 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d44d12cd5c9ecc8e4b75201d67412f77b79157eaffaaed75c3b717bcd42f61e1`  
		Last Modified: Tue, 09 Jun 2026 20:11:29 GMT  
		Size: 3.6 MB (3575314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573a1d7a0131b3bb62a9b1e14cb0e8cf4d866ce7ec68a2d4a2ac402c7357b24e`  
		Last Modified: Wed, 10 Jun 2026 18:35:57 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608fb78ccee6e69c390e8ce51d8c49d4bdac4d71cf50cc5c6e457dca3274ebf7`  
		Last Modified: Wed, 10 Jun 2026 18:35:57 GMT  
		Size: 102.6 KB (102627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e548b50ad164ad49e2be2cc291334c46cf327222804043ba289bc49d36fb202`  
		Last Modified: Wed, 10 Jun 2026 18:35:57 GMT  
		Size: 4.0 MB (4044869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3288904307a586b305537393c2f20cfcb8d98edcb8c0e51b89036d575c960cb`  
		Last Modified: Wed, 10 Jun 2026 18:35:57 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae9e7c1276f81bfb68d7489c74761c88a037e47d4b72983353c03196b97b218`  
		Last Modified: Wed, 10 Jun 2026 18:35:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:1b8dbbfd625301ca11ebb50f807fdf9060dfc1fa7f9247b6cd5556775c85c77c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f6e1cafb6d6aa90021214a707bd44e9808680bd0fcf819c2bf76e1e97319038`

```dockerfile
```

-	Layers:
	-	`sha256:added378a7ae281e9cd9406a18fcf5d2639f6ffcbf0b2f5fb5fcec47db001204`  
		Last Modified: Wed, 10 Jun 2026 18:35:57 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.24` - linux; arm variant v7

```console
$ docker pull memcached@sha256:01b020198ba0ce8e9af9fb0257ca2487cc71cfec9a953ad04b6cb386059f3bdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7220162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2416c6901535e0b681eeba9d0e010b8030f17e2a0f9a4e8e7bdea9261260886`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2026 20:14:38 GMT
ADD alpine-minirootfs-3.24.0-armv7.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:14:38 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:14:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:14:02 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:16:58 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:16:58 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:16:58 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:16:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:16:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:16:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:16:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:16:59 GMT
USER memcache
# Wed, 10 Jun 2026 18:16:59 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:16:59 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bce674d5697a824549061f4985dfd06a60c018b96ba50b18b7bc1f9ad6143570`  
		Last Modified: Tue, 09 Jun 2026 20:14:43 GMT  
		Size: 3.3 MB (3286160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddccf170e8b5b7071fc7d37c3e7b71b383e42d66ebc8452c8face5ccfc0ba841`  
		Last Modified: Wed, 10 Jun 2026 18:17:04 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d271b94c2d5eb987939fb26d3e872b378914ed230228478c94c4eb9271af3bea`  
		Last Modified: Wed, 10 Jun 2026 18:17:04 GMT  
		Size: 92.4 KB (92371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58107905e1ff79a6248896ab514b9cad8d31bc4ded8616894db922f6d9bc862e`  
		Last Modified: Wed, 10 Jun 2026 18:17:04 GMT  
		Size: 3.8 MB (3840281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1397705fe8ef2c310800a79d7e7f6de7db2ebad65b46e9505ba834b120347c62`  
		Last Modified: Wed, 10 Jun 2026 18:17:04 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06dbe001de1fe8d785dd53bdcb0a65b97ea4a57b4bd839da2e6ef4344226ec07`  
		Last Modified: Wed, 10 Jun 2026 18:17:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:9c08a5c1662aaac2028c9b66d84c8a5ab3ac6ce87d8d1ca8dfb2856bbf331d17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71022047d72bddcc121675d6bbe75bac274911f769029bb179b886d170baeb02`

```dockerfile
```

-	Layers:
	-	`sha256:db4bac74dcb986da8aa5a0e3af57ee133956acb18dac4ae890a9ec074f02c1b5`  
		Last Modified: Wed, 10 Jun 2026 18:17:04 GMT  
		Size: 94.3 KB (94315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a12f73bf7901f75ec1c978ac1cc49ff827de35497af898a05c43fe1d9c753e86`  
		Last Modified: Wed, 10 Jun 2026 18:17:04 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.24` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:16eb5e3d6505a7ef0a633bfe2d01f674184e0f6f9cbe79d241120567b03f054f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9059008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5f2f1760f4a10a67fb7a006f00b172c33b6e530525a2a7bf1f112c44e8a1949`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:09 GMT
ADD alpine-minirootfs-3.24.0-aarch64.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:09 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:12:27 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:12:27 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:15:17 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:15:17 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:15:17 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:15:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:15:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:15:17 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:15:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:15:17 GMT
USER memcache
# Wed, 10 Jun 2026 18:15:17 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:15:17 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c05efffaed614b5ff4e3b9a80136e7c0eed0b47f434802c81baf254c0defca91`  
		Last Modified: Tue, 09 Jun 2026 20:11:14 GMT  
		Size: 4.2 MB (4202330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e456d8825f29dfd65b2051f5b44b6de5920128138737cbd93cbae351cc088ce`  
		Last Modified: Wed, 10 Jun 2026 18:15:22 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1569a3fe1932b7d0793450f547c0e3ffcd659baefbc266fc8febd0f82dd3b197`  
		Last Modified: Wed, 10 Jun 2026 18:15:23 GMT  
		Size: 121.9 KB (121857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91674cbd7c3a07584ce0b6f5702920f8c878319100d0794e0be633caf4cd702`  
		Last Modified: Wed, 10 Jun 2026 18:15:23 GMT  
		Size: 4.7 MB (4733470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f23ddaee25aadc1b418bf3aa3c117923c06e9cac1b101e927b76def37507cd2`  
		Last Modified: Wed, 10 Jun 2026 18:15:23 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd7c50e090366a1f99c6b319c0f95302b5ce191989df8f66ddb9e1d4d163be0`  
		Last Modified: Wed, 10 Jun 2026 18:15:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:46bff7acd3c1c4e24acda5e4573e853d532c8f880c8c739e9bcc220de4b43b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:399abce8f4883f60c5fe7741d0d7c0b5fd729e48660e5df3829afc60dc755d1c`

```dockerfile
```

-	Layers:
	-	`sha256:c94369062ddc1d7c765eb1aec2fbaeb202af339dcda4691019309c6708106359`  
		Last Modified: Wed, 10 Jun 2026 18:15:22 GMT  
		Size: 94.4 KB (94351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49b2ad2a43e5a3f86c7fe35d36035450993daa3bb8ecaf1ae6d49b858da8d19b`  
		Last Modified: Wed, 10 Jun 2026 18:15:23 GMT  
		Size: 20.7 KB (20727 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.24` - linux; 386

```console
$ docker pull memcached@sha256:f2d4eb8c40d54fdcd5fb0684d29936ebce2fbafe26c26c0c72ae0a9335f06997
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (8024217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07138462285df4cbd1ed2c627e98451dc1a4b43b37e111b2b72e59d154f811ee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2026 20:10:54 GMT
ADD alpine-minirootfs-3.24.0-x86.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:10:54 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:25:31 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:25:32 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:28:16 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:28:16 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:28:16 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:28:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:28:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:28:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:28:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:28:16 GMT
USER memcache
# Wed, 10 Jun 2026 18:28:16 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:28:16 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:14b4480cdb6be1a40aafc14c9089d92843794d03fc3115b849ddc49717c25982`  
		Last Modified: Tue, 09 Jun 2026 20:10:59 GMT  
		Size: 3.7 MB (3691754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14cf249ff43e2409a2718494167fe16786f19bdc9666b291ba5f4fbb333e382c`  
		Last Modified: Wed, 10 Jun 2026 18:28:21 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9d4516b9de504d8b32b12ee16f3aeb0ed86d6124308df02b6a907e3e0b3ed6`  
		Last Modified: Wed, 10 Jun 2026 18:28:22 GMT  
		Size: 110.7 KB (110732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f550fd7ec906f373bb885a9a587de5a825d95ff63d1353fb88aff5bba428f19a`  
		Last Modified: Wed, 10 Jun 2026 18:28:22 GMT  
		Size: 4.2 MB (4220384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dcc14148666128c245fd38ff2cd067defeb4c4a1acfe2da55983425fe7b5cfd`  
		Last Modified: Wed, 10 Jun 2026 18:28:22 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad5170f36cabc8e1bfed343134a7a78b8ae945e7e73c0428b77c3eb5fddeadb`  
		Last Modified: Wed, 10 Jun 2026 18:28:23 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:12741aadabddc93af391c2b99e0e588138024a0fdb67bcca1191f96869187018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6490fe35195514ccd48669f08b68a82107074785228124b81b6c2e5f6a1133c8`

```dockerfile
```

-	Layers:
	-	`sha256:db2735e9fcf74530bbea1a6790fee5d18607311bb075b0ed4a074e41e6bd0f91`  
		Last Modified: Wed, 10 Jun 2026 18:28:21 GMT  
		Size: 94.9 KB (94852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dcb9494458e7383f61847d265cf37857313b48a9e23522119233328d3f808c6`  
		Last Modified: Wed, 10 Jun 2026 18:28:22 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.24` - linux; ppc64le

```console
$ docker pull memcached@sha256:a51985551b3de3fae96ad49d7bd83e4bed7b04338ab59c8f1d0615a8104d681f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8377092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eec58c326d0b7fb84ebe5bb90c97ac84004c7a43061561a4551c88cadb9bbea3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2026 20:33:34 GMT
ADD alpine-minirootfs-3.24.0-ppc64le.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:33:34 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:12:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:12:36 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:15:17 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:15:17 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:15:17 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:15:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:15:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:15:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:15:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:15:18 GMT
USER memcache
# Wed, 10 Jun 2026 18:15:18 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:15:18 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:73fae309fa62bb67bbe20b40696c81037cf9f77919ce6726a7e535ae9250214e`  
		Last Modified: Tue, 09 Jun 2026 20:33:48 GMT  
		Size: 3.8 MB (3833955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0bdd5dc720242a7e084697c14693e733e595ecd986eb2cc0f8a575aab48705`  
		Last Modified: Wed, 10 Jun 2026 18:15:29 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4bbfdd2990992d37f6018cbadcbaa970bb884e82c6d96d4600fb8cba166859`  
		Last Modified: Wed, 10 Jun 2026 18:15:29 GMT  
		Size: 126.2 KB (126245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5863f1a7869d33f359d606dd6947e23ca7fcc10f7c0d821a26c0b4e7adee77a3`  
		Last Modified: Wed, 10 Jun 2026 18:15:29 GMT  
		Size: 4.4 MB (4415538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b4bc2207922da164d3875abd76e10f11db496e6018180dce3ecbe5026a026f`  
		Last Modified: Wed, 10 Jun 2026 18:15:29 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b342b964ce20aa37c3d771357dde123e5a25ec2695cfba9aa7f6278e5e11fbf5`  
		Last Modified: Wed, 10 Jun 2026 18:15:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:017746bf102a5b7fdcb2f023fcb1a50c67ccb725fc105d89d0985e7aa46df95d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9616f658a36ce366c7c705240e2d967a302d803c4b1d73c377f8c64c25bdd2da`

```dockerfile
```

-	Layers:
	-	`sha256:6682009a8af30b6df10790ac6a62a9c3850d2aacdd06b951b0016026377a7f86`  
		Last Modified: Wed, 10 Jun 2026 18:15:29 GMT  
		Size: 94.3 KB (94304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c4569b2982a6a6f9f6ef930d40862043152589ac307ce81183a90bec91860cf`  
		Last Modified: Wed, 10 Jun 2026 18:15:29 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.24` - linux; riscv64

```console
$ docker pull memcached@sha256:c5ade8803ceb4e9ca036c3b1be9b6d970446c324b3e38080eed03b1998db8dd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7915430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:450fb4c40f2f1f7e5517aeddc4034b6229d7fb443c71c7c6dd0f3697aaa05461`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:23:10 GMT
ADD alpine-minirootfs-3.24.0-riscv64.tar.gz / # buildkit
# Wed, 10 Jun 2026 00:23:10 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:13:44 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:13:48 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:27:33 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:27:33 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:27:33 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:27:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:27:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:27:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:27:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:27:34 GMT
USER memcache
# Wed, 10 Jun 2026 18:27:34 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:27:34 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3d2f730dbeff3c2e957669de5d586604e82939f67ebfd9142872c9ff56603e07`  
		Last Modified: Wed, 10 Jun 2026 00:23:34 GMT  
		Size: 3.6 MB (3591852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87dad43f2e16c76f58e5e2753765caecdfbc1feb72bd08841a5964c4da7ab22c`  
		Last Modified: Wed, 10 Jun 2026 18:27:59 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac80a7065539574d0aff698d1fc76d3744f2f00b3e6d68314fb4cb84f0e37d7`  
		Last Modified: Wed, 10 Jun 2026 18:27:59 GMT  
		Size: 108.9 KB (108888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef744b36d8487e33054d1c30cfebd18490c05aca17b4f574720ce1dda3c78412`  
		Last Modified: Wed, 10 Jun 2026 18:28:00 GMT  
		Size: 4.2 MB (4213337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a136ba7f82c19e371c7e2c7a4ee25ed1de41441c27feecbc6b989e7c79afe3f`  
		Last Modified: Wed, 10 Jun 2026 18:27:59 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:653819d879edda4020f6a5bd344241c2e118781fbd50319cfabeb965557c4234`  
		Last Modified: Wed, 10 Jun 2026 18:28:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:7715a9e3170ec3a2143b197fb80db0a2d670d751a4d710a95942ec384df85a58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4297ab54a68ba59e6d3d700921a359e4850605f249ec473c36391bf423a0017b`

```dockerfile
```

-	Layers:
	-	`sha256:a1889ec9b4bd651c813e65a363b785ace86c68a6095f41a397172d7acdc47058`  
		Last Modified: Wed, 10 Jun 2026 18:27:59 GMT  
		Size: 94.3 KB (94300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec157ceb7ee3f109ef2e714168e5904e088b28fcab859065403f0a617f121d82`  
		Last Modified: Wed, 10 Jun 2026 18:27:59 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.24` - linux; s390x

```console
$ docker pull memcached@sha256:084c53e2e39a12bbca6189febd6d4e2aadf6ccdd85445553f9a237d6c3608c3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8107287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de51c430e27f993bbd7f1be7334cdb2818c849b8e7c017552ff8cdb5fb2c2949`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2026 20:18:16 GMT
ADD alpine-minirootfs-3.24.0-s390x.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:18:16 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:20:00 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:20:05 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:49:55 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:49:55 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:49:55 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:49:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:49:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:50:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:50:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:50:01 GMT
USER memcache
# Wed, 10 Jun 2026 18:50:01 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:50:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4c421b7ac5771added0d41fbc2e1c815472072561366ed82ab9e16b926cb03c6`  
		Last Modified: Tue, 09 Jun 2026 20:18:26 GMT  
		Size: 3.7 MB (3730217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0711a972fdad3ac072246017b11d2279363fa9074279aef5f300474872ae8bd7`  
		Last Modified: Wed, 10 Jun 2026 18:50:43 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a6a5c3b22bd7a4743610e767f8e08c5bb66379e7420935b5ad890c02be1af8`  
		Last Modified: Wed, 10 Jun 2026 18:50:43 GMT  
		Size: 114.3 KB (114292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:791d693469c94f11b8cfc977eadf134459f8e13d0f21ba48b4b04664df753f71`  
		Last Modified: Wed, 10 Jun 2026 18:50:45 GMT  
		Size: 4.3 MB (4261419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dd8c588e70e6f166476b33c198ee2d77a7b5d952207365e20799c8415f1fb27`  
		Last Modified: Wed, 10 Jun 2026 18:50:43 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c17c044babfc798701d6dbfde3b27966cccf07ccfffb49929017250e203878c5`  
		Last Modified: Wed, 10 Jun 2026 18:50:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:b86d70017763ec3335085643c4fc858eb4d0ecd80da1533ab7844a082ea2096c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dde6eca01b66c07c19e6987128b39e14d1395da122e9f2a4b85c663667255978`

```dockerfile
```

-	Layers:
	-	`sha256:003e58d9144c67eaa1a52c05fa8df2908964b8150d09d954940f1c90844cf74c`  
		Last Modified: Wed, 10 Jun 2026 18:50:43 GMT  
		Size: 94.2 KB (94246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd8a5086e89c6d7f95c68b2f90f54a4730f057dc511969769bfe3bcc9a2d57da`  
		Last Modified: Wed, 10 Jun 2026 18:50:44 GMT  
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
$ docker pull memcached@sha256:24f46bd5e6250525c4219957edf4490e1dcff92a8c798325d9422798af8d02db
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
$ docker pull memcached@sha256:cb2d8176cf730b6e493f47a20c202e3785450ce97ac94eca4907d7690c1af307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8429739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b50ffd1c04d8028fbb3c3420cc1d60aed911ce7c0e45a4965310fce274d53ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:31 GMT
ADD alpine-minirootfs-3.24.0-x86_64.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:31 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:14:19 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:14:20 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:16:57 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:16:57 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:16:57 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:16:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:16:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:16:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:16:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:16:57 GMT
USER memcache
# Wed, 10 Jun 2026 18:16:57 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:16:57 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9b70e313681f44d32991ec943f89228bc91d7431d4a84feafc269a76e3f96a63`  
		Last Modified: Tue, 09 Jun 2026 20:11:36 GMT  
		Size: 3.9 MB (3866755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e3046ed30b13ad06ce756a4c6583941eb759870afa70848109fd8c0064519f`  
		Last Modified: Wed, 10 Jun 2026 18:17:02 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c4e652e501aa70e550ad140cba871ada70bf7f3a31a1f25b992df3b69702af`  
		Last Modified: Wed, 10 Jun 2026 18:17:03 GMT  
		Size: 106.1 KB (106068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7b3e28eeb74ba3ce98c770af704a09d48456fc4b9d0ac8ec337c30cc95f2e3`  
		Last Modified: Wed, 10 Jun 2026 18:17:03 GMT  
		Size: 4.5 MB (4455567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4da70a2e9c741455aab8b6eeecd686f79532427ac6f458f4c6df4203fb17b42`  
		Last Modified: Wed, 10 Jun 2026 18:17:02 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d9e7ab7a8a69db82d54cd5953d81a8d174f46e493dc10bcead49919ab63b80`  
		Last Modified: Wed, 10 Jun 2026 18:17:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:423aea49db161bc8ab6d8f600ba326351a44d683f648e77c38062ced876533b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6a9742524b3a500c65fd2ff4ee0ed6498d3286356dbe7b04507f7903496dcc2`

```dockerfile
```

-	Layers:
	-	`sha256:1967442755aa01c5b18b82d15e09215bb060a9a4725e69476dffdde04a11a174`  
		Last Modified: Wed, 10 Jun 2026 18:17:03 GMT  
		Size: 94.9 KB (94897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:241a34a97ffb94fa781f2bf870cb96be626d17c16414915a8e5737d781b620d1`  
		Last Modified: Wed, 10 Jun 2026 18:17:02 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42-alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:32cf627ba476a687feb05fc278c1ec76e5904f2d070ec439c114e910c770d514
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7724160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:232f09c26d3bbd4437aa7cadb96874736aca039e389a58df9594e5b6aba964b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:25 GMT
ADD alpine-minirootfs-3.24.0-armhf.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:25 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:13:29 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:13:30 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:35:53 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:35:53 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:35:53 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:35:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:35:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:35:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:35:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:35:53 GMT
USER memcache
# Wed, 10 Jun 2026 18:35:53 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:35:53 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d44d12cd5c9ecc8e4b75201d67412f77b79157eaffaaed75c3b717bcd42f61e1`  
		Last Modified: Tue, 09 Jun 2026 20:11:29 GMT  
		Size: 3.6 MB (3575314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573a1d7a0131b3bb62a9b1e14cb0e8cf4d866ce7ec68a2d4a2ac402c7357b24e`  
		Last Modified: Wed, 10 Jun 2026 18:35:57 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608fb78ccee6e69c390e8ce51d8c49d4bdac4d71cf50cc5c6e457dca3274ebf7`  
		Last Modified: Wed, 10 Jun 2026 18:35:57 GMT  
		Size: 102.6 KB (102627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e548b50ad164ad49e2be2cc291334c46cf327222804043ba289bc49d36fb202`  
		Last Modified: Wed, 10 Jun 2026 18:35:57 GMT  
		Size: 4.0 MB (4044869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3288904307a586b305537393c2f20cfcb8d98edcb8c0e51b89036d575c960cb`  
		Last Modified: Wed, 10 Jun 2026 18:35:57 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae9e7c1276f81bfb68d7489c74761c88a037e47d4b72983353c03196b97b218`  
		Last Modified: Wed, 10 Jun 2026 18:35:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:1b8dbbfd625301ca11ebb50f807fdf9060dfc1fa7f9247b6cd5556775c85c77c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f6e1cafb6d6aa90021214a707bd44e9808680bd0fcf819c2bf76e1e97319038`

```dockerfile
```

-	Layers:
	-	`sha256:added378a7ae281e9cd9406a18fcf5d2639f6ffcbf0b2f5fb5fcec47db001204`  
		Last Modified: Wed, 10 Jun 2026 18:35:57 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42-alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:01b020198ba0ce8e9af9fb0257ca2487cc71cfec9a953ad04b6cb386059f3bdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7220162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2416c6901535e0b681eeba9d0e010b8030f17e2a0f9a4e8e7bdea9261260886`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2026 20:14:38 GMT
ADD alpine-minirootfs-3.24.0-armv7.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:14:38 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:14:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:14:02 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:16:58 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:16:58 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:16:58 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:16:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:16:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:16:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:16:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:16:59 GMT
USER memcache
# Wed, 10 Jun 2026 18:16:59 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:16:59 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bce674d5697a824549061f4985dfd06a60c018b96ba50b18b7bc1f9ad6143570`  
		Last Modified: Tue, 09 Jun 2026 20:14:43 GMT  
		Size: 3.3 MB (3286160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddccf170e8b5b7071fc7d37c3e7b71b383e42d66ebc8452c8face5ccfc0ba841`  
		Last Modified: Wed, 10 Jun 2026 18:17:04 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d271b94c2d5eb987939fb26d3e872b378914ed230228478c94c4eb9271af3bea`  
		Last Modified: Wed, 10 Jun 2026 18:17:04 GMT  
		Size: 92.4 KB (92371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58107905e1ff79a6248896ab514b9cad8d31bc4ded8616894db922f6d9bc862e`  
		Last Modified: Wed, 10 Jun 2026 18:17:04 GMT  
		Size: 3.8 MB (3840281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1397705fe8ef2c310800a79d7e7f6de7db2ebad65b46e9505ba834b120347c62`  
		Last Modified: Wed, 10 Jun 2026 18:17:04 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06dbe001de1fe8d785dd53bdcb0a65b97ea4a57b4bd839da2e6ef4344226ec07`  
		Last Modified: Wed, 10 Jun 2026 18:17:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:9c08a5c1662aaac2028c9b66d84c8a5ab3ac6ce87d8d1ca8dfb2856bbf331d17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71022047d72bddcc121675d6bbe75bac274911f769029bb179b886d170baeb02`

```dockerfile
```

-	Layers:
	-	`sha256:db4bac74dcb986da8aa5a0e3af57ee133956acb18dac4ae890a9ec074f02c1b5`  
		Last Modified: Wed, 10 Jun 2026 18:17:04 GMT  
		Size: 94.3 KB (94315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a12f73bf7901f75ec1c978ac1cc49ff827de35497af898a05c43fe1d9c753e86`  
		Last Modified: Wed, 10 Jun 2026 18:17:04 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:16eb5e3d6505a7ef0a633bfe2d01f674184e0f6f9cbe79d241120567b03f054f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9059008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5f2f1760f4a10a67fb7a006f00b172c33b6e530525a2a7bf1f112c44e8a1949`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:09 GMT
ADD alpine-minirootfs-3.24.0-aarch64.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:09 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:12:27 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:12:27 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:15:17 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:15:17 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:15:17 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:15:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:15:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:15:17 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:15:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:15:17 GMT
USER memcache
# Wed, 10 Jun 2026 18:15:17 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:15:17 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c05efffaed614b5ff4e3b9a80136e7c0eed0b47f434802c81baf254c0defca91`  
		Last Modified: Tue, 09 Jun 2026 20:11:14 GMT  
		Size: 4.2 MB (4202330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e456d8825f29dfd65b2051f5b44b6de5920128138737cbd93cbae351cc088ce`  
		Last Modified: Wed, 10 Jun 2026 18:15:22 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1569a3fe1932b7d0793450f547c0e3ffcd659baefbc266fc8febd0f82dd3b197`  
		Last Modified: Wed, 10 Jun 2026 18:15:23 GMT  
		Size: 121.9 KB (121857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91674cbd7c3a07584ce0b6f5702920f8c878319100d0794e0be633caf4cd702`  
		Last Modified: Wed, 10 Jun 2026 18:15:23 GMT  
		Size: 4.7 MB (4733470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f23ddaee25aadc1b418bf3aa3c117923c06e9cac1b101e927b76def37507cd2`  
		Last Modified: Wed, 10 Jun 2026 18:15:23 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd7c50e090366a1f99c6b319c0f95302b5ce191989df8f66ddb9e1d4d163be0`  
		Last Modified: Wed, 10 Jun 2026 18:15:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:46bff7acd3c1c4e24acda5e4573e853d532c8f880c8c739e9bcc220de4b43b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:399abce8f4883f60c5fe7741d0d7c0b5fd729e48660e5df3829afc60dc755d1c`

```dockerfile
```

-	Layers:
	-	`sha256:c94369062ddc1d7c765eb1aec2fbaeb202af339dcda4691019309c6708106359`  
		Last Modified: Wed, 10 Jun 2026 18:15:22 GMT  
		Size: 94.4 KB (94351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49b2ad2a43e5a3f86c7fe35d36035450993daa3bb8ecaf1ae6d49b858da8d19b`  
		Last Modified: Wed, 10 Jun 2026 18:15:23 GMT  
		Size: 20.7 KB (20727 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42-alpine` - linux; 386

```console
$ docker pull memcached@sha256:f2d4eb8c40d54fdcd5fb0684d29936ebce2fbafe26c26c0c72ae0a9335f06997
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (8024217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07138462285df4cbd1ed2c627e98451dc1a4b43b37e111b2b72e59d154f811ee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2026 20:10:54 GMT
ADD alpine-minirootfs-3.24.0-x86.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:10:54 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:25:31 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:25:32 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:28:16 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:28:16 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:28:16 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:28:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:28:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:28:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:28:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:28:16 GMT
USER memcache
# Wed, 10 Jun 2026 18:28:16 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:28:16 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:14b4480cdb6be1a40aafc14c9089d92843794d03fc3115b849ddc49717c25982`  
		Last Modified: Tue, 09 Jun 2026 20:10:59 GMT  
		Size: 3.7 MB (3691754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14cf249ff43e2409a2718494167fe16786f19bdc9666b291ba5f4fbb333e382c`  
		Last Modified: Wed, 10 Jun 2026 18:28:21 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9d4516b9de504d8b32b12ee16f3aeb0ed86d6124308df02b6a907e3e0b3ed6`  
		Last Modified: Wed, 10 Jun 2026 18:28:22 GMT  
		Size: 110.7 KB (110732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f550fd7ec906f373bb885a9a587de5a825d95ff63d1353fb88aff5bba428f19a`  
		Last Modified: Wed, 10 Jun 2026 18:28:22 GMT  
		Size: 4.2 MB (4220384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dcc14148666128c245fd38ff2cd067defeb4c4a1acfe2da55983425fe7b5cfd`  
		Last Modified: Wed, 10 Jun 2026 18:28:22 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad5170f36cabc8e1bfed343134a7a78b8ae945e7e73c0428b77c3eb5fddeadb`  
		Last Modified: Wed, 10 Jun 2026 18:28:23 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:12741aadabddc93af391c2b99e0e588138024a0fdb67bcca1191f96869187018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6490fe35195514ccd48669f08b68a82107074785228124b81b6c2e5f6a1133c8`

```dockerfile
```

-	Layers:
	-	`sha256:db2735e9fcf74530bbea1a6790fee5d18607311bb075b0ed4a074e41e6bd0f91`  
		Last Modified: Wed, 10 Jun 2026 18:28:21 GMT  
		Size: 94.9 KB (94852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dcb9494458e7383f61847d265cf37857313b48a9e23522119233328d3f808c6`  
		Last Modified: Wed, 10 Jun 2026 18:28:22 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:a51985551b3de3fae96ad49d7bd83e4bed7b04338ab59c8f1d0615a8104d681f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8377092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eec58c326d0b7fb84ebe5bb90c97ac84004c7a43061561a4551c88cadb9bbea3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2026 20:33:34 GMT
ADD alpine-minirootfs-3.24.0-ppc64le.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:33:34 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:12:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:12:36 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:15:17 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:15:17 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:15:17 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:15:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:15:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:15:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:15:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:15:18 GMT
USER memcache
# Wed, 10 Jun 2026 18:15:18 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:15:18 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:73fae309fa62bb67bbe20b40696c81037cf9f77919ce6726a7e535ae9250214e`  
		Last Modified: Tue, 09 Jun 2026 20:33:48 GMT  
		Size: 3.8 MB (3833955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0bdd5dc720242a7e084697c14693e733e595ecd986eb2cc0f8a575aab48705`  
		Last Modified: Wed, 10 Jun 2026 18:15:29 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4bbfdd2990992d37f6018cbadcbaa970bb884e82c6d96d4600fb8cba166859`  
		Last Modified: Wed, 10 Jun 2026 18:15:29 GMT  
		Size: 126.2 KB (126245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5863f1a7869d33f359d606dd6947e23ca7fcc10f7c0d821a26c0b4e7adee77a3`  
		Last Modified: Wed, 10 Jun 2026 18:15:29 GMT  
		Size: 4.4 MB (4415538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b4bc2207922da164d3875abd76e10f11db496e6018180dce3ecbe5026a026f`  
		Last Modified: Wed, 10 Jun 2026 18:15:29 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b342b964ce20aa37c3d771357dde123e5a25ec2695cfba9aa7f6278e5e11fbf5`  
		Last Modified: Wed, 10 Jun 2026 18:15:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:017746bf102a5b7fdcb2f023fcb1a50c67ccb725fc105d89d0985e7aa46df95d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9616f658a36ce366c7c705240e2d967a302d803c4b1d73c377f8c64c25bdd2da`

```dockerfile
```

-	Layers:
	-	`sha256:6682009a8af30b6df10790ac6a62a9c3850d2aacdd06b951b0016026377a7f86`  
		Last Modified: Wed, 10 Jun 2026 18:15:29 GMT  
		Size: 94.3 KB (94304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c4569b2982a6a6f9f6ef930d40862043152589ac307ce81183a90bec91860cf`  
		Last Modified: Wed, 10 Jun 2026 18:15:29 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42-alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:c5ade8803ceb4e9ca036c3b1be9b6d970446c324b3e38080eed03b1998db8dd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7915430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:450fb4c40f2f1f7e5517aeddc4034b6229d7fb443c71c7c6dd0f3697aaa05461`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:23:10 GMT
ADD alpine-minirootfs-3.24.0-riscv64.tar.gz / # buildkit
# Wed, 10 Jun 2026 00:23:10 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:13:44 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:13:48 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:27:33 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:27:33 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:27:33 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:27:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:27:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:27:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:27:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:27:34 GMT
USER memcache
# Wed, 10 Jun 2026 18:27:34 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:27:34 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3d2f730dbeff3c2e957669de5d586604e82939f67ebfd9142872c9ff56603e07`  
		Last Modified: Wed, 10 Jun 2026 00:23:34 GMT  
		Size: 3.6 MB (3591852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87dad43f2e16c76f58e5e2753765caecdfbc1feb72bd08841a5964c4da7ab22c`  
		Last Modified: Wed, 10 Jun 2026 18:27:59 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac80a7065539574d0aff698d1fc76d3744f2f00b3e6d68314fb4cb84f0e37d7`  
		Last Modified: Wed, 10 Jun 2026 18:27:59 GMT  
		Size: 108.9 KB (108888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef744b36d8487e33054d1c30cfebd18490c05aca17b4f574720ce1dda3c78412`  
		Last Modified: Wed, 10 Jun 2026 18:28:00 GMT  
		Size: 4.2 MB (4213337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a136ba7f82c19e371c7e2c7a4ee25ed1de41441c27feecbc6b989e7c79afe3f`  
		Last Modified: Wed, 10 Jun 2026 18:27:59 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:653819d879edda4020f6a5bd344241c2e118781fbd50319cfabeb965557c4234`  
		Last Modified: Wed, 10 Jun 2026 18:28:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7715a9e3170ec3a2143b197fb80db0a2d670d751a4d710a95942ec384df85a58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4297ab54a68ba59e6d3d700921a359e4850605f249ec473c36391bf423a0017b`

```dockerfile
```

-	Layers:
	-	`sha256:a1889ec9b4bd651c813e65a363b785ace86c68a6095f41a397172d7acdc47058`  
		Last Modified: Wed, 10 Jun 2026 18:27:59 GMT  
		Size: 94.3 KB (94300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec157ceb7ee3f109ef2e714168e5904e088b28fcab859065403f0a617f121d82`  
		Last Modified: Wed, 10 Jun 2026 18:27:59 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:084c53e2e39a12bbca6189febd6d4e2aadf6ccdd85445553f9a237d6c3608c3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8107287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de51c430e27f993bbd7f1be7334cdb2818c849b8e7c017552ff8cdb5fb2c2949`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2026 20:18:16 GMT
ADD alpine-minirootfs-3.24.0-s390x.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:18:16 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:20:00 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:20:05 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:49:55 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:49:55 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:49:55 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:49:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:49:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:50:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:50:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:50:01 GMT
USER memcache
# Wed, 10 Jun 2026 18:50:01 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:50:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4c421b7ac5771added0d41fbc2e1c815472072561366ed82ab9e16b926cb03c6`  
		Last Modified: Tue, 09 Jun 2026 20:18:26 GMT  
		Size: 3.7 MB (3730217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0711a972fdad3ac072246017b11d2279363fa9074279aef5f300474872ae8bd7`  
		Last Modified: Wed, 10 Jun 2026 18:50:43 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a6a5c3b22bd7a4743610e767f8e08c5bb66379e7420935b5ad890c02be1af8`  
		Last Modified: Wed, 10 Jun 2026 18:50:43 GMT  
		Size: 114.3 KB (114292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:791d693469c94f11b8cfc977eadf134459f8e13d0f21ba48b4b04664df753f71`  
		Last Modified: Wed, 10 Jun 2026 18:50:45 GMT  
		Size: 4.3 MB (4261419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dd8c588e70e6f166476b33c198ee2d77a7b5d952207365e20799c8415f1fb27`  
		Last Modified: Wed, 10 Jun 2026 18:50:43 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c17c044babfc798701d6dbfde3b27966cccf07ccfffb49929017250e203878c5`  
		Last Modified: Wed, 10 Jun 2026 18:50:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:b86d70017763ec3335085643c4fc858eb4d0ecd80da1533ab7844a082ea2096c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dde6eca01b66c07c19e6987128b39e14d1395da122e9f2a4b85c663667255978`

```dockerfile
```

-	Layers:
	-	`sha256:003e58d9144c67eaa1a52c05fa8df2908964b8150d09d954940f1c90844cf74c`  
		Last Modified: Wed, 10 Jun 2026 18:50:43 GMT  
		Size: 94.2 KB (94246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd8a5086e89c6d7f95c68b2f90f54a4730f057dc511969769bfe3bcc9a2d57da`  
		Last Modified: Wed, 10 Jun 2026 18:50:44 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.42-alpine3.24`

```console
$ docker pull memcached@sha256:24f46bd5e6250525c4219957edf4490e1dcff92a8c798325d9422798af8d02db
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
$ docker pull memcached@sha256:cb2d8176cf730b6e493f47a20c202e3785450ce97ac94eca4907d7690c1af307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8429739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b50ffd1c04d8028fbb3c3420cc1d60aed911ce7c0e45a4965310fce274d53ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:31 GMT
ADD alpine-minirootfs-3.24.0-x86_64.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:31 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:14:19 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:14:20 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:16:57 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:16:57 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:16:57 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:16:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:16:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:16:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:16:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:16:57 GMT
USER memcache
# Wed, 10 Jun 2026 18:16:57 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:16:57 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9b70e313681f44d32991ec943f89228bc91d7431d4a84feafc269a76e3f96a63`  
		Last Modified: Tue, 09 Jun 2026 20:11:36 GMT  
		Size: 3.9 MB (3866755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e3046ed30b13ad06ce756a4c6583941eb759870afa70848109fd8c0064519f`  
		Last Modified: Wed, 10 Jun 2026 18:17:02 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c4e652e501aa70e550ad140cba871ada70bf7f3a31a1f25b992df3b69702af`  
		Last Modified: Wed, 10 Jun 2026 18:17:03 GMT  
		Size: 106.1 KB (106068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7b3e28eeb74ba3ce98c770af704a09d48456fc4b9d0ac8ec337c30cc95f2e3`  
		Last Modified: Wed, 10 Jun 2026 18:17:03 GMT  
		Size: 4.5 MB (4455567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4da70a2e9c741455aab8b6eeecd686f79532427ac6f458f4c6df4203fb17b42`  
		Last Modified: Wed, 10 Jun 2026 18:17:02 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d9e7ab7a8a69db82d54cd5953d81a8d174f46e493dc10bcead49919ab63b80`  
		Last Modified: Wed, 10 Jun 2026 18:17:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:423aea49db161bc8ab6d8f600ba326351a44d683f648e77c38062ced876533b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6a9742524b3a500c65fd2ff4ee0ed6498d3286356dbe7b04507f7903496dcc2`

```dockerfile
```

-	Layers:
	-	`sha256:1967442755aa01c5b18b82d15e09215bb060a9a4725e69476dffdde04a11a174`  
		Last Modified: Wed, 10 Jun 2026 18:17:03 GMT  
		Size: 94.9 KB (94897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:241a34a97ffb94fa781f2bf870cb96be626d17c16414915a8e5737d781b620d1`  
		Last Modified: Wed, 10 Jun 2026 18:17:02 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42-alpine3.24` - linux; arm variant v6

```console
$ docker pull memcached@sha256:32cf627ba476a687feb05fc278c1ec76e5904f2d070ec439c114e910c770d514
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7724160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:232f09c26d3bbd4437aa7cadb96874736aca039e389a58df9594e5b6aba964b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:25 GMT
ADD alpine-minirootfs-3.24.0-armhf.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:25 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:13:29 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:13:30 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:35:53 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:35:53 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:35:53 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:35:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:35:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:35:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:35:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:35:53 GMT
USER memcache
# Wed, 10 Jun 2026 18:35:53 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:35:53 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d44d12cd5c9ecc8e4b75201d67412f77b79157eaffaaed75c3b717bcd42f61e1`  
		Last Modified: Tue, 09 Jun 2026 20:11:29 GMT  
		Size: 3.6 MB (3575314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573a1d7a0131b3bb62a9b1e14cb0e8cf4d866ce7ec68a2d4a2ac402c7357b24e`  
		Last Modified: Wed, 10 Jun 2026 18:35:57 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608fb78ccee6e69c390e8ce51d8c49d4bdac4d71cf50cc5c6e457dca3274ebf7`  
		Last Modified: Wed, 10 Jun 2026 18:35:57 GMT  
		Size: 102.6 KB (102627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e548b50ad164ad49e2be2cc291334c46cf327222804043ba289bc49d36fb202`  
		Last Modified: Wed, 10 Jun 2026 18:35:57 GMT  
		Size: 4.0 MB (4044869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3288904307a586b305537393c2f20cfcb8d98edcb8c0e51b89036d575c960cb`  
		Last Modified: Wed, 10 Jun 2026 18:35:57 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae9e7c1276f81bfb68d7489c74761c88a037e47d4b72983353c03196b97b218`  
		Last Modified: Wed, 10 Jun 2026 18:35:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:1b8dbbfd625301ca11ebb50f807fdf9060dfc1fa7f9247b6cd5556775c85c77c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f6e1cafb6d6aa90021214a707bd44e9808680bd0fcf819c2bf76e1e97319038`

```dockerfile
```

-	Layers:
	-	`sha256:added378a7ae281e9cd9406a18fcf5d2639f6ffcbf0b2f5fb5fcec47db001204`  
		Last Modified: Wed, 10 Jun 2026 18:35:57 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42-alpine3.24` - linux; arm variant v7

```console
$ docker pull memcached@sha256:01b020198ba0ce8e9af9fb0257ca2487cc71cfec9a953ad04b6cb386059f3bdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7220162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2416c6901535e0b681eeba9d0e010b8030f17e2a0f9a4e8e7bdea9261260886`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2026 20:14:38 GMT
ADD alpine-minirootfs-3.24.0-armv7.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:14:38 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:14:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:14:02 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:16:58 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:16:58 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:16:58 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:16:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:16:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:16:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:16:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:16:59 GMT
USER memcache
# Wed, 10 Jun 2026 18:16:59 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:16:59 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bce674d5697a824549061f4985dfd06a60c018b96ba50b18b7bc1f9ad6143570`  
		Last Modified: Tue, 09 Jun 2026 20:14:43 GMT  
		Size: 3.3 MB (3286160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddccf170e8b5b7071fc7d37c3e7b71b383e42d66ebc8452c8face5ccfc0ba841`  
		Last Modified: Wed, 10 Jun 2026 18:17:04 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d271b94c2d5eb987939fb26d3e872b378914ed230228478c94c4eb9271af3bea`  
		Last Modified: Wed, 10 Jun 2026 18:17:04 GMT  
		Size: 92.4 KB (92371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58107905e1ff79a6248896ab514b9cad8d31bc4ded8616894db922f6d9bc862e`  
		Last Modified: Wed, 10 Jun 2026 18:17:04 GMT  
		Size: 3.8 MB (3840281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1397705fe8ef2c310800a79d7e7f6de7db2ebad65b46e9505ba834b120347c62`  
		Last Modified: Wed, 10 Jun 2026 18:17:04 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06dbe001de1fe8d785dd53bdcb0a65b97ea4a57b4bd839da2e6ef4344226ec07`  
		Last Modified: Wed, 10 Jun 2026 18:17:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:9c08a5c1662aaac2028c9b66d84c8a5ab3ac6ce87d8d1ca8dfb2856bbf331d17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71022047d72bddcc121675d6bbe75bac274911f769029bb179b886d170baeb02`

```dockerfile
```

-	Layers:
	-	`sha256:db4bac74dcb986da8aa5a0e3af57ee133956acb18dac4ae890a9ec074f02c1b5`  
		Last Modified: Wed, 10 Jun 2026 18:17:04 GMT  
		Size: 94.3 KB (94315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a12f73bf7901f75ec1c978ac1cc49ff827de35497af898a05c43fe1d9c753e86`  
		Last Modified: Wed, 10 Jun 2026 18:17:04 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42-alpine3.24` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:16eb5e3d6505a7ef0a633bfe2d01f674184e0f6f9cbe79d241120567b03f054f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9059008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5f2f1760f4a10a67fb7a006f00b172c33b6e530525a2a7bf1f112c44e8a1949`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:09 GMT
ADD alpine-minirootfs-3.24.0-aarch64.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:09 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:12:27 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:12:27 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:15:17 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:15:17 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:15:17 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:15:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:15:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:15:17 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:15:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:15:17 GMT
USER memcache
# Wed, 10 Jun 2026 18:15:17 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:15:17 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c05efffaed614b5ff4e3b9a80136e7c0eed0b47f434802c81baf254c0defca91`  
		Last Modified: Tue, 09 Jun 2026 20:11:14 GMT  
		Size: 4.2 MB (4202330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e456d8825f29dfd65b2051f5b44b6de5920128138737cbd93cbae351cc088ce`  
		Last Modified: Wed, 10 Jun 2026 18:15:22 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1569a3fe1932b7d0793450f547c0e3ffcd659baefbc266fc8febd0f82dd3b197`  
		Last Modified: Wed, 10 Jun 2026 18:15:23 GMT  
		Size: 121.9 KB (121857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91674cbd7c3a07584ce0b6f5702920f8c878319100d0794e0be633caf4cd702`  
		Last Modified: Wed, 10 Jun 2026 18:15:23 GMT  
		Size: 4.7 MB (4733470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f23ddaee25aadc1b418bf3aa3c117923c06e9cac1b101e927b76def37507cd2`  
		Last Modified: Wed, 10 Jun 2026 18:15:23 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd7c50e090366a1f99c6b319c0f95302b5ce191989df8f66ddb9e1d4d163be0`  
		Last Modified: Wed, 10 Jun 2026 18:15:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:46bff7acd3c1c4e24acda5e4573e853d532c8f880c8c739e9bcc220de4b43b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:399abce8f4883f60c5fe7741d0d7c0b5fd729e48660e5df3829afc60dc755d1c`

```dockerfile
```

-	Layers:
	-	`sha256:c94369062ddc1d7c765eb1aec2fbaeb202af339dcda4691019309c6708106359`  
		Last Modified: Wed, 10 Jun 2026 18:15:22 GMT  
		Size: 94.4 KB (94351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49b2ad2a43e5a3f86c7fe35d36035450993daa3bb8ecaf1ae6d49b858da8d19b`  
		Last Modified: Wed, 10 Jun 2026 18:15:23 GMT  
		Size: 20.7 KB (20727 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42-alpine3.24` - linux; 386

```console
$ docker pull memcached@sha256:f2d4eb8c40d54fdcd5fb0684d29936ebce2fbafe26c26c0c72ae0a9335f06997
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (8024217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07138462285df4cbd1ed2c627e98451dc1a4b43b37e111b2b72e59d154f811ee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2026 20:10:54 GMT
ADD alpine-minirootfs-3.24.0-x86.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:10:54 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:25:31 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:25:32 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:28:16 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:28:16 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:28:16 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:28:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:28:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:28:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:28:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:28:16 GMT
USER memcache
# Wed, 10 Jun 2026 18:28:16 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:28:16 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:14b4480cdb6be1a40aafc14c9089d92843794d03fc3115b849ddc49717c25982`  
		Last Modified: Tue, 09 Jun 2026 20:10:59 GMT  
		Size: 3.7 MB (3691754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14cf249ff43e2409a2718494167fe16786f19bdc9666b291ba5f4fbb333e382c`  
		Last Modified: Wed, 10 Jun 2026 18:28:21 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9d4516b9de504d8b32b12ee16f3aeb0ed86d6124308df02b6a907e3e0b3ed6`  
		Last Modified: Wed, 10 Jun 2026 18:28:22 GMT  
		Size: 110.7 KB (110732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f550fd7ec906f373bb885a9a587de5a825d95ff63d1353fb88aff5bba428f19a`  
		Last Modified: Wed, 10 Jun 2026 18:28:22 GMT  
		Size: 4.2 MB (4220384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dcc14148666128c245fd38ff2cd067defeb4c4a1acfe2da55983425fe7b5cfd`  
		Last Modified: Wed, 10 Jun 2026 18:28:22 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad5170f36cabc8e1bfed343134a7a78b8ae945e7e73c0428b77c3eb5fddeadb`  
		Last Modified: Wed, 10 Jun 2026 18:28:23 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:12741aadabddc93af391c2b99e0e588138024a0fdb67bcca1191f96869187018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6490fe35195514ccd48669f08b68a82107074785228124b81b6c2e5f6a1133c8`

```dockerfile
```

-	Layers:
	-	`sha256:db2735e9fcf74530bbea1a6790fee5d18607311bb075b0ed4a074e41e6bd0f91`  
		Last Modified: Wed, 10 Jun 2026 18:28:21 GMT  
		Size: 94.9 KB (94852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dcb9494458e7383f61847d265cf37857313b48a9e23522119233328d3f808c6`  
		Last Modified: Wed, 10 Jun 2026 18:28:22 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42-alpine3.24` - linux; ppc64le

```console
$ docker pull memcached@sha256:a51985551b3de3fae96ad49d7bd83e4bed7b04338ab59c8f1d0615a8104d681f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8377092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eec58c326d0b7fb84ebe5bb90c97ac84004c7a43061561a4551c88cadb9bbea3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2026 20:33:34 GMT
ADD alpine-minirootfs-3.24.0-ppc64le.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:33:34 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:12:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:12:36 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:15:17 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:15:17 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:15:17 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:15:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:15:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:15:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:15:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:15:18 GMT
USER memcache
# Wed, 10 Jun 2026 18:15:18 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:15:18 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:73fae309fa62bb67bbe20b40696c81037cf9f77919ce6726a7e535ae9250214e`  
		Last Modified: Tue, 09 Jun 2026 20:33:48 GMT  
		Size: 3.8 MB (3833955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0bdd5dc720242a7e084697c14693e733e595ecd986eb2cc0f8a575aab48705`  
		Last Modified: Wed, 10 Jun 2026 18:15:29 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4bbfdd2990992d37f6018cbadcbaa970bb884e82c6d96d4600fb8cba166859`  
		Last Modified: Wed, 10 Jun 2026 18:15:29 GMT  
		Size: 126.2 KB (126245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5863f1a7869d33f359d606dd6947e23ca7fcc10f7c0d821a26c0b4e7adee77a3`  
		Last Modified: Wed, 10 Jun 2026 18:15:29 GMT  
		Size: 4.4 MB (4415538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b4bc2207922da164d3875abd76e10f11db496e6018180dce3ecbe5026a026f`  
		Last Modified: Wed, 10 Jun 2026 18:15:29 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b342b964ce20aa37c3d771357dde123e5a25ec2695cfba9aa7f6278e5e11fbf5`  
		Last Modified: Wed, 10 Jun 2026 18:15:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:017746bf102a5b7fdcb2f023fcb1a50c67ccb725fc105d89d0985e7aa46df95d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9616f658a36ce366c7c705240e2d967a302d803c4b1d73c377f8c64c25bdd2da`

```dockerfile
```

-	Layers:
	-	`sha256:6682009a8af30b6df10790ac6a62a9c3850d2aacdd06b951b0016026377a7f86`  
		Last Modified: Wed, 10 Jun 2026 18:15:29 GMT  
		Size: 94.3 KB (94304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c4569b2982a6a6f9f6ef930d40862043152589ac307ce81183a90bec91860cf`  
		Last Modified: Wed, 10 Jun 2026 18:15:29 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42-alpine3.24` - linux; riscv64

```console
$ docker pull memcached@sha256:c5ade8803ceb4e9ca036c3b1be9b6d970446c324b3e38080eed03b1998db8dd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7915430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:450fb4c40f2f1f7e5517aeddc4034b6229d7fb443c71c7c6dd0f3697aaa05461`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:23:10 GMT
ADD alpine-minirootfs-3.24.0-riscv64.tar.gz / # buildkit
# Wed, 10 Jun 2026 00:23:10 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:13:44 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:13:48 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:27:33 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:27:33 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:27:33 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:27:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:27:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:27:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:27:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:27:34 GMT
USER memcache
# Wed, 10 Jun 2026 18:27:34 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:27:34 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3d2f730dbeff3c2e957669de5d586604e82939f67ebfd9142872c9ff56603e07`  
		Last Modified: Wed, 10 Jun 2026 00:23:34 GMT  
		Size: 3.6 MB (3591852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87dad43f2e16c76f58e5e2753765caecdfbc1feb72bd08841a5964c4da7ab22c`  
		Last Modified: Wed, 10 Jun 2026 18:27:59 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac80a7065539574d0aff698d1fc76d3744f2f00b3e6d68314fb4cb84f0e37d7`  
		Last Modified: Wed, 10 Jun 2026 18:27:59 GMT  
		Size: 108.9 KB (108888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef744b36d8487e33054d1c30cfebd18490c05aca17b4f574720ce1dda3c78412`  
		Last Modified: Wed, 10 Jun 2026 18:28:00 GMT  
		Size: 4.2 MB (4213337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a136ba7f82c19e371c7e2c7a4ee25ed1de41441c27feecbc6b989e7c79afe3f`  
		Last Modified: Wed, 10 Jun 2026 18:27:59 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:653819d879edda4020f6a5bd344241c2e118781fbd50319cfabeb965557c4234`  
		Last Modified: Wed, 10 Jun 2026 18:28:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:7715a9e3170ec3a2143b197fb80db0a2d670d751a4d710a95942ec384df85a58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4297ab54a68ba59e6d3d700921a359e4850605f249ec473c36391bf423a0017b`

```dockerfile
```

-	Layers:
	-	`sha256:a1889ec9b4bd651c813e65a363b785ace86c68a6095f41a397172d7acdc47058`  
		Last Modified: Wed, 10 Jun 2026 18:27:59 GMT  
		Size: 94.3 KB (94300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec157ceb7ee3f109ef2e714168e5904e088b28fcab859065403f0a617f121d82`  
		Last Modified: Wed, 10 Jun 2026 18:27:59 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.42-alpine3.24` - linux; s390x

```console
$ docker pull memcached@sha256:084c53e2e39a12bbca6189febd6d4e2aadf6ccdd85445553f9a237d6c3608c3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8107287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de51c430e27f993bbd7f1be7334cdb2818c849b8e7c017552ff8cdb5fb2c2949`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2026 20:18:16 GMT
ADD alpine-minirootfs-3.24.0-s390x.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:18:16 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:20:00 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:20:05 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:49:55 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:49:55 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:49:55 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:49:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:49:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:50:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:50:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:50:01 GMT
USER memcache
# Wed, 10 Jun 2026 18:50:01 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:50:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4c421b7ac5771added0d41fbc2e1c815472072561366ed82ab9e16b926cb03c6`  
		Last Modified: Tue, 09 Jun 2026 20:18:26 GMT  
		Size: 3.7 MB (3730217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0711a972fdad3ac072246017b11d2279363fa9074279aef5f300474872ae8bd7`  
		Last Modified: Wed, 10 Jun 2026 18:50:43 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a6a5c3b22bd7a4743610e767f8e08c5bb66379e7420935b5ad890c02be1af8`  
		Last Modified: Wed, 10 Jun 2026 18:50:43 GMT  
		Size: 114.3 KB (114292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:791d693469c94f11b8cfc977eadf134459f8e13d0f21ba48b4b04664df753f71`  
		Last Modified: Wed, 10 Jun 2026 18:50:45 GMT  
		Size: 4.3 MB (4261419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dd8c588e70e6f166476b33c198ee2d77a7b5d952207365e20799c8415f1fb27`  
		Last Modified: Wed, 10 Jun 2026 18:50:43 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c17c044babfc798701d6dbfde3b27966cccf07ccfffb49929017250e203878c5`  
		Last Modified: Wed, 10 Jun 2026 18:50:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.42-alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:b86d70017763ec3335085643c4fc858eb4d0ecd80da1533ab7844a082ea2096c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dde6eca01b66c07c19e6987128b39e14d1395da122e9f2a4b85c663667255978`

```dockerfile
```

-	Layers:
	-	`sha256:003e58d9144c67eaa1a52c05fa8df2908964b8150d09d954940f1c90844cf74c`  
		Last Modified: Wed, 10 Jun 2026 18:50:43 GMT  
		Size: 94.2 KB (94246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd8a5086e89c6d7f95c68b2f90f54a4730f057dc511969769bfe3bcc9a2d57da`  
		Last Modified: Wed, 10 Jun 2026 18:50:44 GMT  
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
$ docker pull memcached@sha256:24f46bd5e6250525c4219957edf4490e1dcff92a8c798325d9422798af8d02db
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
$ docker pull memcached@sha256:cb2d8176cf730b6e493f47a20c202e3785450ce97ac94eca4907d7690c1af307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8429739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b50ffd1c04d8028fbb3c3420cc1d60aed911ce7c0e45a4965310fce274d53ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:31 GMT
ADD alpine-minirootfs-3.24.0-x86_64.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:31 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:14:19 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:14:20 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:16:57 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:16:57 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:16:57 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:16:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:16:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:16:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:16:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:16:57 GMT
USER memcache
# Wed, 10 Jun 2026 18:16:57 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:16:57 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9b70e313681f44d32991ec943f89228bc91d7431d4a84feafc269a76e3f96a63`  
		Last Modified: Tue, 09 Jun 2026 20:11:36 GMT  
		Size: 3.9 MB (3866755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e3046ed30b13ad06ce756a4c6583941eb759870afa70848109fd8c0064519f`  
		Last Modified: Wed, 10 Jun 2026 18:17:02 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c4e652e501aa70e550ad140cba871ada70bf7f3a31a1f25b992df3b69702af`  
		Last Modified: Wed, 10 Jun 2026 18:17:03 GMT  
		Size: 106.1 KB (106068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7b3e28eeb74ba3ce98c770af704a09d48456fc4b9d0ac8ec337c30cc95f2e3`  
		Last Modified: Wed, 10 Jun 2026 18:17:03 GMT  
		Size: 4.5 MB (4455567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4da70a2e9c741455aab8b6eeecd686f79532427ac6f458f4c6df4203fb17b42`  
		Last Modified: Wed, 10 Jun 2026 18:17:02 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d9e7ab7a8a69db82d54cd5953d81a8d174f46e493dc10bcead49919ab63b80`  
		Last Modified: Wed, 10 Jun 2026 18:17:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:423aea49db161bc8ab6d8f600ba326351a44d683f648e77c38062ced876533b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6a9742524b3a500c65fd2ff4ee0ed6498d3286356dbe7b04507f7903496dcc2`

```dockerfile
```

-	Layers:
	-	`sha256:1967442755aa01c5b18b82d15e09215bb060a9a4725e69476dffdde04a11a174`  
		Last Modified: Wed, 10 Jun 2026 18:17:03 GMT  
		Size: 94.9 KB (94897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:241a34a97ffb94fa781f2bf870cb96be626d17c16414915a8e5737d781b620d1`  
		Last Modified: Wed, 10 Jun 2026 18:17:02 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:32cf627ba476a687feb05fc278c1ec76e5904f2d070ec439c114e910c770d514
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7724160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:232f09c26d3bbd4437aa7cadb96874736aca039e389a58df9594e5b6aba964b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:25 GMT
ADD alpine-minirootfs-3.24.0-armhf.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:25 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:13:29 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:13:30 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:35:53 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:35:53 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:35:53 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:35:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:35:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:35:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:35:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:35:53 GMT
USER memcache
# Wed, 10 Jun 2026 18:35:53 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:35:53 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d44d12cd5c9ecc8e4b75201d67412f77b79157eaffaaed75c3b717bcd42f61e1`  
		Last Modified: Tue, 09 Jun 2026 20:11:29 GMT  
		Size: 3.6 MB (3575314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573a1d7a0131b3bb62a9b1e14cb0e8cf4d866ce7ec68a2d4a2ac402c7357b24e`  
		Last Modified: Wed, 10 Jun 2026 18:35:57 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608fb78ccee6e69c390e8ce51d8c49d4bdac4d71cf50cc5c6e457dca3274ebf7`  
		Last Modified: Wed, 10 Jun 2026 18:35:57 GMT  
		Size: 102.6 KB (102627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e548b50ad164ad49e2be2cc291334c46cf327222804043ba289bc49d36fb202`  
		Last Modified: Wed, 10 Jun 2026 18:35:57 GMT  
		Size: 4.0 MB (4044869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3288904307a586b305537393c2f20cfcb8d98edcb8c0e51b89036d575c960cb`  
		Last Modified: Wed, 10 Jun 2026 18:35:57 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae9e7c1276f81bfb68d7489c74761c88a037e47d4b72983353c03196b97b218`  
		Last Modified: Wed, 10 Jun 2026 18:35:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:1b8dbbfd625301ca11ebb50f807fdf9060dfc1fa7f9247b6cd5556775c85c77c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f6e1cafb6d6aa90021214a707bd44e9808680bd0fcf819c2bf76e1e97319038`

```dockerfile
```

-	Layers:
	-	`sha256:added378a7ae281e9cd9406a18fcf5d2639f6ffcbf0b2f5fb5fcec47db001204`  
		Last Modified: Wed, 10 Jun 2026 18:35:57 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:01b020198ba0ce8e9af9fb0257ca2487cc71cfec9a953ad04b6cb386059f3bdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7220162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2416c6901535e0b681eeba9d0e010b8030f17e2a0f9a4e8e7bdea9261260886`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2026 20:14:38 GMT
ADD alpine-minirootfs-3.24.0-armv7.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:14:38 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:14:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:14:02 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:16:58 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:16:58 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:16:58 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:16:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:16:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:16:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:16:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:16:59 GMT
USER memcache
# Wed, 10 Jun 2026 18:16:59 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:16:59 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bce674d5697a824549061f4985dfd06a60c018b96ba50b18b7bc1f9ad6143570`  
		Last Modified: Tue, 09 Jun 2026 20:14:43 GMT  
		Size: 3.3 MB (3286160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddccf170e8b5b7071fc7d37c3e7b71b383e42d66ebc8452c8face5ccfc0ba841`  
		Last Modified: Wed, 10 Jun 2026 18:17:04 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d271b94c2d5eb987939fb26d3e872b378914ed230228478c94c4eb9271af3bea`  
		Last Modified: Wed, 10 Jun 2026 18:17:04 GMT  
		Size: 92.4 KB (92371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58107905e1ff79a6248896ab514b9cad8d31bc4ded8616894db922f6d9bc862e`  
		Last Modified: Wed, 10 Jun 2026 18:17:04 GMT  
		Size: 3.8 MB (3840281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1397705fe8ef2c310800a79d7e7f6de7db2ebad65b46e9505ba834b120347c62`  
		Last Modified: Wed, 10 Jun 2026 18:17:04 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06dbe001de1fe8d785dd53bdcb0a65b97ea4a57b4bd839da2e6ef4344226ec07`  
		Last Modified: Wed, 10 Jun 2026 18:17:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:9c08a5c1662aaac2028c9b66d84c8a5ab3ac6ce87d8d1ca8dfb2856bbf331d17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71022047d72bddcc121675d6bbe75bac274911f769029bb179b886d170baeb02`

```dockerfile
```

-	Layers:
	-	`sha256:db4bac74dcb986da8aa5a0e3af57ee133956acb18dac4ae890a9ec074f02c1b5`  
		Last Modified: Wed, 10 Jun 2026 18:17:04 GMT  
		Size: 94.3 KB (94315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a12f73bf7901f75ec1c978ac1cc49ff827de35497af898a05c43fe1d9c753e86`  
		Last Modified: Wed, 10 Jun 2026 18:17:04 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:16eb5e3d6505a7ef0a633bfe2d01f674184e0f6f9cbe79d241120567b03f054f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9059008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5f2f1760f4a10a67fb7a006f00b172c33b6e530525a2a7bf1f112c44e8a1949`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:09 GMT
ADD alpine-minirootfs-3.24.0-aarch64.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:09 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:12:27 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:12:27 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:15:17 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:15:17 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:15:17 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:15:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:15:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:15:17 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:15:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:15:17 GMT
USER memcache
# Wed, 10 Jun 2026 18:15:17 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:15:17 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c05efffaed614b5ff4e3b9a80136e7c0eed0b47f434802c81baf254c0defca91`  
		Last Modified: Tue, 09 Jun 2026 20:11:14 GMT  
		Size: 4.2 MB (4202330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e456d8825f29dfd65b2051f5b44b6de5920128138737cbd93cbae351cc088ce`  
		Last Modified: Wed, 10 Jun 2026 18:15:22 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1569a3fe1932b7d0793450f547c0e3ffcd659baefbc266fc8febd0f82dd3b197`  
		Last Modified: Wed, 10 Jun 2026 18:15:23 GMT  
		Size: 121.9 KB (121857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91674cbd7c3a07584ce0b6f5702920f8c878319100d0794e0be633caf4cd702`  
		Last Modified: Wed, 10 Jun 2026 18:15:23 GMT  
		Size: 4.7 MB (4733470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f23ddaee25aadc1b418bf3aa3c117923c06e9cac1b101e927b76def37507cd2`  
		Last Modified: Wed, 10 Jun 2026 18:15:23 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd7c50e090366a1f99c6b319c0f95302b5ce191989df8f66ddb9e1d4d163be0`  
		Last Modified: Wed, 10 Jun 2026 18:15:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:46bff7acd3c1c4e24acda5e4573e853d532c8f880c8c739e9bcc220de4b43b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:399abce8f4883f60c5fe7741d0d7c0b5fd729e48660e5df3829afc60dc755d1c`

```dockerfile
```

-	Layers:
	-	`sha256:c94369062ddc1d7c765eb1aec2fbaeb202af339dcda4691019309c6708106359`  
		Last Modified: Wed, 10 Jun 2026 18:15:22 GMT  
		Size: 94.4 KB (94351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49b2ad2a43e5a3f86c7fe35d36035450993daa3bb8ecaf1ae6d49b858da8d19b`  
		Last Modified: Wed, 10 Jun 2026 18:15:23 GMT  
		Size: 20.7 KB (20727 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; 386

```console
$ docker pull memcached@sha256:f2d4eb8c40d54fdcd5fb0684d29936ebce2fbafe26c26c0c72ae0a9335f06997
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (8024217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07138462285df4cbd1ed2c627e98451dc1a4b43b37e111b2b72e59d154f811ee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2026 20:10:54 GMT
ADD alpine-minirootfs-3.24.0-x86.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:10:54 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:25:31 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:25:32 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:28:16 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:28:16 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:28:16 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:28:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:28:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:28:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:28:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:28:16 GMT
USER memcache
# Wed, 10 Jun 2026 18:28:16 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:28:16 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:14b4480cdb6be1a40aafc14c9089d92843794d03fc3115b849ddc49717c25982`  
		Last Modified: Tue, 09 Jun 2026 20:10:59 GMT  
		Size: 3.7 MB (3691754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14cf249ff43e2409a2718494167fe16786f19bdc9666b291ba5f4fbb333e382c`  
		Last Modified: Wed, 10 Jun 2026 18:28:21 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9d4516b9de504d8b32b12ee16f3aeb0ed86d6124308df02b6a907e3e0b3ed6`  
		Last Modified: Wed, 10 Jun 2026 18:28:22 GMT  
		Size: 110.7 KB (110732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f550fd7ec906f373bb885a9a587de5a825d95ff63d1353fb88aff5bba428f19a`  
		Last Modified: Wed, 10 Jun 2026 18:28:22 GMT  
		Size: 4.2 MB (4220384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dcc14148666128c245fd38ff2cd067defeb4c4a1acfe2da55983425fe7b5cfd`  
		Last Modified: Wed, 10 Jun 2026 18:28:22 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad5170f36cabc8e1bfed343134a7a78b8ae945e7e73c0428b77c3eb5fddeadb`  
		Last Modified: Wed, 10 Jun 2026 18:28:23 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:12741aadabddc93af391c2b99e0e588138024a0fdb67bcca1191f96869187018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6490fe35195514ccd48669f08b68a82107074785228124b81b6c2e5f6a1133c8`

```dockerfile
```

-	Layers:
	-	`sha256:db2735e9fcf74530bbea1a6790fee5d18607311bb075b0ed4a074e41e6bd0f91`  
		Last Modified: Wed, 10 Jun 2026 18:28:21 GMT  
		Size: 94.9 KB (94852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dcb9494458e7383f61847d265cf37857313b48a9e23522119233328d3f808c6`  
		Last Modified: Wed, 10 Jun 2026 18:28:22 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:a51985551b3de3fae96ad49d7bd83e4bed7b04338ab59c8f1d0615a8104d681f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8377092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eec58c326d0b7fb84ebe5bb90c97ac84004c7a43061561a4551c88cadb9bbea3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2026 20:33:34 GMT
ADD alpine-minirootfs-3.24.0-ppc64le.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:33:34 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:12:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:12:36 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:15:17 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:15:17 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:15:17 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:15:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:15:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:15:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:15:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:15:18 GMT
USER memcache
# Wed, 10 Jun 2026 18:15:18 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:15:18 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:73fae309fa62bb67bbe20b40696c81037cf9f77919ce6726a7e535ae9250214e`  
		Last Modified: Tue, 09 Jun 2026 20:33:48 GMT  
		Size: 3.8 MB (3833955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0bdd5dc720242a7e084697c14693e733e595ecd986eb2cc0f8a575aab48705`  
		Last Modified: Wed, 10 Jun 2026 18:15:29 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4bbfdd2990992d37f6018cbadcbaa970bb884e82c6d96d4600fb8cba166859`  
		Last Modified: Wed, 10 Jun 2026 18:15:29 GMT  
		Size: 126.2 KB (126245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5863f1a7869d33f359d606dd6947e23ca7fcc10f7c0d821a26c0b4e7adee77a3`  
		Last Modified: Wed, 10 Jun 2026 18:15:29 GMT  
		Size: 4.4 MB (4415538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b4bc2207922da164d3875abd76e10f11db496e6018180dce3ecbe5026a026f`  
		Last Modified: Wed, 10 Jun 2026 18:15:29 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b342b964ce20aa37c3d771357dde123e5a25ec2695cfba9aa7f6278e5e11fbf5`  
		Last Modified: Wed, 10 Jun 2026 18:15:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:017746bf102a5b7fdcb2f023fcb1a50c67ccb725fc105d89d0985e7aa46df95d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9616f658a36ce366c7c705240e2d967a302d803c4b1d73c377f8c64c25bdd2da`

```dockerfile
```

-	Layers:
	-	`sha256:6682009a8af30b6df10790ac6a62a9c3850d2aacdd06b951b0016026377a7f86`  
		Last Modified: Wed, 10 Jun 2026 18:15:29 GMT  
		Size: 94.3 KB (94304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c4569b2982a6a6f9f6ef930d40862043152589ac307ce81183a90bec91860cf`  
		Last Modified: Wed, 10 Jun 2026 18:15:29 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:c5ade8803ceb4e9ca036c3b1be9b6d970446c324b3e38080eed03b1998db8dd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7915430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:450fb4c40f2f1f7e5517aeddc4034b6229d7fb443c71c7c6dd0f3697aaa05461`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:23:10 GMT
ADD alpine-minirootfs-3.24.0-riscv64.tar.gz / # buildkit
# Wed, 10 Jun 2026 00:23:10 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:13:44 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:13:48 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:27:33 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:27:33 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:27:33 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:27:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:27:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:27:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:27:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:27:34 GMT
USER memcache
# Wed, 10 Jun 2026 18:27:34 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:27:34 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3d2f730dbeff3c2e957669de5d586604e82939f67ebfd9142872c9ff56603e07`  
		Last Modified: Wed, 10 Jun 2026 00:23:34 GMT  
		Size: 3.6 MB (3591852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87dad43f2e16c76f58e5e2753765caecdfbc1feb72bd08841a5964c4da7ab22c`  
		Last Modified: Wed, 10 Jun 2026 18:27:59 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac80a7065539574d0aff698d1fc76d3744f2f00b3e6d68314fb4cb84f0e37d7`  
		Last Modified: Wed, 10 Jun 2026 18:27:59 GMT  
		Size: 108.9 KB (108888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef744b36d8487e33054d1c30cfebd18490c05aca17b4f574720ce1dda3c78412`  
		Last Modified: Wed, 10 Jun 2026 18:28:00 GMT  
		Size: 4.2 MB (4213337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a136ba7f82c19e371c7e2c7a4ee25ed1de41441c27feecbc6b989e7c79afe3f`  
		Last Modified: Wed, 10 Jun 2026 18:27:59 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:653819d879edda4020f6a5bd344241c2e118781fbd50319cfabeb965557c4234`  
		Last Modified: Wed, 10 Jun 2026 18:28:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7715a9e3170ec3a2143b197fb80db0a2d670d751a4d710a95942ec384df85a58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4297ab54a68ba59e6d3d700921a359e4850605f249ec473c36391bf423a0017b`

```dockerfile
```

-	Layers:
	-	`sha256:a1889ec9b4bd651c813e65a363b785ace86c68a6095f41a397172d7acdc47058`  
		Last Modified: Wed, 10 Jun 2026 18:27:59 GMT  
		Size: 94.3 KB (94300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec157ceb7ee3f109ef2e714168e5904e088b28fcab859065403f0a617f121d82`  
		Last Modified: Wed, 10 Jun 2026 18:27:59 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; s390x

```console
$ docker pull memcached@sha256:084c53e2e39a12bbca6189febd6d4e2aadf6ccdd85445553f9a237d6c3608c3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8107287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de51c430e27f993bbd7f1be7334cdb2818c849b8e7c017552ff8cdb5fb2c2949`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2026 20:18:16 GMT
ADD alpine-minirootfs-3.24.0-s390x.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:18:16 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:20:00 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:20:05 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:49:55 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:49:55 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:49:55 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:49:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:49:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:50:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:50:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:50:01 GMT
USER memcache
# Wed, 10 Jun 2026 18:50:01 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:50:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4c421b7ac5771added0d41fbc2e1c815472072561366ed82ab9e16b926cb03c6`  
		Last Modified: Tue, 09 Jun 2026 20:18:26 GMT  
		Size: 3.7 MB (3730217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0711a972fdad3ac072246017b11d2279363fa9074279aef5f300474872ae8bd7`  
		Last Modified: Wed, 10 Jun 2026 18:50:43 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a6a5c3b22bd7a4743610e767f8e08c5bb66379e7420935b5ad890c02be1af8`  
		Last Modified: Wed, 10 Jun 2026 18:50:43 GMT  
		Size: 114.3 KB (114292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:791d693469c94f11b8cfc977eadf134459f8e13d0f21ba48b4b04664df753f71`  
		Last Modified: Wed, 10 Jun 2026 18:50:45 GMT  
		Size: 4.3 MB (4261419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dd8c588e70e6f166476b33c198ee2d77a7b5d952207365e20799c8415f1fb27`  
		Last Modified: Wed, 10 Jun 2026 18:50:43 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c17c044babfc798701d6dbfde3b27966cccf07ccfffb49929017250e203878c5`  
		Last Modified: Wed, 10 Jun 2026 18:50:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:b86d70017763ec3335085643c4fc858eb4d0ecd80da1533ab7844a082ea2096c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dde6eca01b66c07c19e6987128b39e14d1395da122e9f2a4b85c663667255978`

```dockerfile
```

-	Layers:
	-	`sha256:003e58d9144c67eaa1a52c05fa8df2908964b8150d09d954940f1c90844cf74c`  
		Last Modified: Wed, 10 Jun 2026 18:50:43 GMT  
		Size: 94.2 KB (94246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd8a5086e89c6d7f95c68b2f90f54a4730f057dc511969769bfe3bcc9a2d57da`  
		Last Modified: Wed, 10 Jun 2026 18:50:44 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine3.24`

```console
$ docker pull memcached@sha256:24f46bd5e6250525c4219957edf4490e1dcff92a8c798325d9422798af8d02db
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
$ docker pull memcached@sha256:cb2d8176cf730b6e493f47a20c202e3785450ce97ac94eca4907d7690c1af307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8429739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b50ffd1c04d8028fbb3c3420cc1d60aed911ce7c0e45a4965310fce274d53ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:31 GMT
ADD alpine-minirootfs-3.24.0-x86_64.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:31 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:14:19 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:14:20 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:16:57 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:16:57 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:16:57 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:16:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:16:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:16:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:16:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:16:57 GMT
USER memcache
# Wed, 10 Jun 2026 18:16:57 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:16:57 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9b70e313681f44d32991ec943f89228bc91d7431d4a84feafc269a76e3f96a63`  
		Last Modified: Tue, 09 Jun 2026 20:11:36 GMT  
		Size: 3.9 MB (3866755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e3046ed30b13ad06ce756a4c6583941eb759870afa70848109fd8c0064519f`  
		Last Modified: Wed, 10 Jun 2026 18:17:02 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c4e652e501aa70e550ad140cba871ada70bf7f3a31a1f25b992df3b69702af`  
		Last Modified: Wed, 10 Jun 2026 18:17:03 GMT  
		Size: 106.1 KB (106068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7b3e28eeb74ba3ce98c770af704a09d48456fc4b9d0ac8ec337c30cc95f2e3`  
		Last Modified: Wed, 10 Jun 2026 18:17:03 GMT  
		Size: 4.5 MB (4455567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4da70a2e9c741455aab8b6eeecd686f79532427ac6f458f4c6df4203fb17b42`  
		Last Modified: Wed, 10 Jun 2026 18:17:02 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d9e7ab7a8a69db82d54cd5953d81a8d174f46e493dc10bcead49919ab63b80`  
		Last Modified: Wed, 10 Jun 2026 18:17:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:423aea49db161bc8ab6d8f600ba326351a44d683f648e77c38062ced876533b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6a9742524b3a500c65fd2ff4ee0ed6498d3286356dbe7b04507f7903496dcc2`

```dockerfile
```

-	Layers:
	-	`sha256:1967442755aa01c5b18b82d15e09215bb060a9a4725e69476dffdde04a11a174`  
		Last Modified: Wed, 10 Jun 2026 18:17:03 GMT  
		Size: 94.9 KB (94897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:241a34a97ffb94fa781f2bf870cb96be626d17c16414915a8e5737d781b620d1`  
		Last Modified: Wed, 10 Jun 2026 18:17:02 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.24` - linux; arm variant v6

```console
$ docker pull memcached@sha256:32cf627ba476a687feb05fc278c1ec76e5904f2d070ec439c114e910c770d514
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7724160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:232f09c26d3bbd4437aa7cadb96874736aca039e389a58df9594e5b6aba964b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:25 GMT
ADD alpine-minirootfs-3.24.0-armhf.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:25 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:13:29 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:13:30 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:35:53 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:35:53 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:35:53 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:35:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:35:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:35:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:35:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:35:53 GMT
USER memcache
# Wed, 10 Jun 2026 18:35:53 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:35:53 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d44d12cd5c9ecc8e4b75201d67412f77b79157eaffaaed75c3b717bcd42f61e1`  
		Last Modified: Tue, 09 Jun 2026 20:11:29 GMT  
		Size: 3.6 MB (3575314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573a1d7a0131b3bb62a9b1e14cb0e8cf4d866ce7ec68a2d4a2ac402c7357b24e`  
		Last Modified: Wed, 10 Jun 2026 18:35:57 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608fb78ccee6e69c390e8ce51d8c49d4bdac4d71cf50cc5c6e457dca3274ebf7`  
		Last Modified: Wed, 10 Jun 2026 18:35:57 GMT  
		Size: 102.6 KB (102627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e548b50ad164ad49e2be2cc291334c46cf327222804043ba289bc49d36fb202`  
		Last Modified: Wed, 10 Jun 2026 18:35:57 GMT  
		Size: 4.0 MB (4044869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3288904307a586b305537393c2f20cfcb8d98edcb8c0e51b89036d575c960cb`  
		Last Modified: Wed, 10 Jun 2026 18:35:57 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae9e7c1276f81bfb68d7489c74761c88a037e47d4b72983353c03196b97b218`  
		Last Modified: Wed, 10 Jun 2026 18:35:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:1b8dbbfd625301ca11ebb50f807fdf9060dfc1fa7f9247b6cd5556775c85c77c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f6e1cafb6d6aa90021214a707bd44e9808680bd0fcf819c2bf76e1e97319038`

```dockerfile
```

-	Layers:
	-	`sha256:added378a7ae281e9cd9406a18fcf5d2639f6ffcbf0b2f5fb5fcec47db001204`  
		Last Modified: Wed, 10 Jun 2026 18:35:57 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.24` - linux; arm variant v7

```console
$ docker pull memcached@sha256:01b020198ba0ce8e9af9fb0257ca2487cc71cfec9a953ad04b6cb386059f3bdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7220162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2416c6901535e0b681eeba9d0e010b8030f17e2a0f9a4e8e7bdea9261260886`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2026 20:14:38 GMT
ADD alpine-minirootfs-3.24.0-armv7.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:14:38 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:14:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:14:02 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:16:58 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:16:58 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:16:58 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:16:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:16:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:16:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:16:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:16:59 GMT
USER memcache
# Wed, 10 Jun 2026 18:16:59 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:16:59 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bce674d5697a824549061f4985dfd06a60c018b96ba50b18b7bc1f9ad6143570`  
		Last Modified: Tue, 09 Jun 2026 20:14:43 GMT  
		Size: 3.3 MB (3286160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddccf170e8b5b7071fc7d37c3e7b71b383e42d66ebc8452c8face5ccfc0ba841`  
		Last Modified: Wed, 10 Jun 2026 18:17:04 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d271b94c2d5eb987939fb26d3e872b378914ed230228478c94c4eb9271af3bea`  
		Last Modified: Wed, 10 Jun 2026 18:17:04 GMT  
		Size: 92.4 KB (92371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58107905e1ff79a6248896ab514b9cad8d31bc4ded8616894db922f6d9bc862e`  
		Last Modified: Wed, 10 Jun 2026 18:17:04 GMT  
		Size: 3.8 MB (3840281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1397705fe8ef2c310800a79d7e7f6de7db2ebad65b46e9505ba834b120347c62`  
		Last Modified: Wed, 10 Jun 2026 18:17:04 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06dbe001de1fe8d785dd53bdcb0a65b97ea4a57b4bd839da2e6ef4344226ec07`  
		Last Modified: Wed, 10 Jun 2026 18:17:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:9c08a5c1662aaac2028c9b66d84c8a5ab3ac6ce87d8d1ca8dfb2856bbf331d17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71022047d72bddcc121675d6bbe75bac274911f769029bb179b886d170baeb02`

```dockerfile
```

-	Layers:
	-	`sha256:db4bac74dcb986da8aa5a0e3af57ee133956acb18dac4ae890a9ec074f02c1b5`  
		Last Modified: Wed, 10 Jun 2026 18:17:04 GMT  
		Size: 94.3 KB (94315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a12f73bf7901f75ec1c978ac1cc49ff827de35497af898a05c43fe1d9c753e86`  
		Last Modified: Wed, 10 Jun 2026 18:17:04 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.24` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:16eb5e3d6505a7ef0a633bfe2d01f674184e0f6f9cbe79d241120567b03f054f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9059008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5f2f1760f4a10a67fb7a006f00b172c33b6e530525a2a7bf1f112c44e8a1949`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:09 GMT
ADD alpine-minirootfs-3.24.0-aarch64.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:09 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:12:27 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:12:27 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:15:17 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:15:17 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:15:17 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:15:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:15:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:15:17 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:15:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:15:17 GMT
USER memcache
# Wed, 10 Jun 2026 18:15:17 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:15:17 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c05efffaed614b5ff4e3b9a80136e7c0eed0b47f434802c81baf254c0defca91`  
		Last Modified: Tue, 09 Jun 2026 20:11:14 GMT  
		Size: 4.2 MB (4202330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e456d8825f29dfd65b2051f5b44b6de5920128138737cbd93cbae351cc088ce`  
		Last Modified: Wed, 10 Jun 2026 18:15:22 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1569a3fe1932b7d0793450f547c0e3ffcd659baefbc266fc8febd0f82dd3b197`  
		Last Modified: Wed, 10 Jun 2026 18:15:23 GMT  
		Size: 121.9 KB (121857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91674cbd7c3a07584ce0b6f5702920f8c878319100d0794e0be633caf4cd702`  
		Last Modified: Wed, 10 Jun 2026 18:15:23 GMT  
		Size: 4.7 MB (4733470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f23ddaee25aadc1b418bf3aa3c117923c06e9cac1b101e927b76def37507cd2`  
		Last Modified: Wed, 10 Jun 2026 18:15:23 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd7c50e090366a1f99c6b319c0f95302b5ce191989df8f66ddb9e1d4d163be0`  
		Last Modified: Wed, 10 Jun 2026 18:15:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:46bff7acd3c1c4e24acda5e4573e853d532c8f880c8c739e9bcc220de4b43b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:399abce8f4883f60c5fe7741d0d7c0b5fd729e48660e5df3829afc60dc755d1c`

```dockerfile
```

-	Layers:
	-	`sha256:c94369062ddc1d7c765eb1aec2fbaeb202af339dcda4691019309c6708106359`  
		Last Modified: Wed, 10 Jun 2026 18:15:22 GMT  
		Size: 94.4 KB (94351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49b2ad2a43e5a3f86c7fe35d36035450993daa3bb8ecaf1ae6d49b858da8d19b`  
		Last Modified: Wed, 10 Jun 2026 18:15:23 GMT  
		Size: 20.7 KB (20727 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.24` - linux; 386

```console
$ docker pull memcached@sha256:f2d4eb8c40d54fdcd5fb0684d29936ebce2fbafe26c26c0c72ae0a9335f06997
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (8024217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07138462285df4cbd1ed2c627e98451dc1a4b43b37e111b2b72e59d154f811ee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2026 20:10:54 GMT
ADD alpine-minirootfs-3.24.0-x86.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:10:54 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:25:31 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:25:32 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:28:16 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:28:16 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:28:16 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:28:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:28:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:28:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:28:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:28:16 GMT
USER memcache
# Wed, 10 Jun 2026 18:28:16 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:28:16 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:14b4480cdb6be1a40aafc14c9089d92843794d03fc3115b849ddc49717c25982`  
		Last Modified: Tue, 09 Jun 2026 20:10:59 GMT  
		Size: 3.7 MB (3691754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14cf249ff43e2409a2718494167fe16786f19bdc9666b291ba5f4fbb333e382c`  
		Last Modified: Wed, 10 Jun 2026 18:28:21 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9d4516b9de504d8b32b12ee16f3aeb0ed86d6124308df02b6a907e3e0b3ed6`  
		Last Modified: Wed, 10 Jun 2026 18:28:22 GMT  
		Size: 110.7 KB (110732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f550fd7ec906f373bb885a9a587de5a825d95ff63d1353fb88aff5bba428f19a`  
		Last Modified: Wed, 10 Jun 2026 18:28:22 GMT  
		Size: 4.2 MB (4220384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dcc14148666128c245fd38ff2cd067defeb4c4a1acfe2da55983425fe7b5cfd`  
		Last Modified: Wed, 10 Jun 2026 18:28:22 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad5170f36cabc8e1bfed343134a7a78b8ae945e7e73c0428b77c3eb5fddeadb`  
		Last Modified: Wed, 10 Jun 2026 18:28:23 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:12741aadabddc93af391c2b99e0e588138024a0fdb67bcca1191f96869187018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6490fe35195514ccd48669f08b68a82107074785228124b81b6c2e5f6a1133c8`

```dockerfile
```

-	Layers:
	-	`sha256:db2735e9fcf74530bbea1a6790fee5d18607311bb075b0ed4a074e41e6bd0f91`  
		Last Modified: Wed, 10 Jun 2026 18:28:21 GMT  
		Size: 94.9 KB (94852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dcb9494458e7383f61847d265cf37857313b48a9e23522119233328d3f808c6`  
		Last Modified: Wed, 10 Jun 2026 18:28:22 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.24` - linux; ppc64le

```console
$ docker pull memcached@sha256:a51985551b3de3fae96ad49d7bd83e4bed7b04338ab59c8f1d0615a8104d681f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8377092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eec58c326d0b7fb84ebe5bb90c97ac84004c7a43061561a4551c88cadb9bbea3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2026 20:33:34 GMT
ADD alpine-minirootfs-3.24.0-ppc64le.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:33:34 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:12:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:12:36 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:15:17 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:15:17 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:15:17 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:15:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:15:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:15:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:15:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:15:18 GMT
USER memcache
# Wed, 10 Jun 2026 18:15:18 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:15:18 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:73fae309fa62bb67bbe20b40696c81037cf9f77919ce6726a7e535ae9250214e`  
		Last Modified: Tue, 09 Jun 2026 20:33:48 GMT  
		Size: 3.8 MB (3833955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0bdd5dc720242a7e084697c14693e733e595ecd986eb2cc0f8a575aab48705`  
		Last Modified: Wed, 10 Jun 2026 18:15:29 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4bbfdd2990992d37f6018cbadcbaa970bb884e82c6d96d4600fb8cba166859`  
		Last Modified: Wed, 10 Jun 2026 18:15:29 GMT  
		Size: 126.2 KB (126245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5863f1a7869d33f359d606dd6947e23ca7fcc10f7c0d821a26c0b4e7adee77a3`  
		Last Modified: Wed, 10 Jun 2026 18:15:29 GMT  
		Size: 4.4 MB (4415538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b4bc2207922da164d3875abd76e10f11db496e6018180dce3ecbe5026a026f`  
		Last Modified: Wed, 10 Jun 2026 18:15:29 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b342b964ce20aa37c3d771357dde123e5a25ec2695cfba9aa7f6278e5e11fbf5`  
		Last Modified: Wed, 10 Jun 2026 18:15:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:017746bf102a5b7fdcb2f023fcb1a50c67ccb725fc105d89d0985e7aa46df95d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9616f658a36ce366c7c705240e2d967a302d803c4b1d73c377f8c64c25bdd2da`

```dockerfile
```

-	Layers:
	-	`sha256:6682009a8af30b6df10790ac6a62a9c3850d2aacdd06b951b0016026377a7f86`  
		Last Modified: Wed, 10 Jun 2026 18:15:29 GMT  
		Size: 94.3 KB (94304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c4569b2982a6a6f9f6ef930d40862043152589ac307ce81183a90bec91860cf`  
		Last Modified: Wed, 10 Jun 2026 18:15:29 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.24` - linux; riscv64

```console
$ docker pull memcached@sha256:c5ade8803ceb4e9ca036c3b1be9b6d970446c324b3e38080eed03b1998db8dd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7915430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:450fb4c40f2f1f7e5517aeddc4034b6229d7fb443c71c7c6dd0f3697aaa05461`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jun 2026 00:23:10 GMT
ADD alpine-minirootfs-3.24.0-riscv64.tar.gz / # buildkit
# Wed, 10 Jun 2026 00:23:10 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:13:44 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:13:48 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:27:33 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:27:33 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:27:33 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:27:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:27:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:27:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:27:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:27:34 GMT
USER memcache
# Wed, 10 Jun 2026 18:27:34 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:27:34 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3d2f730dbeff3c2e957669de5d586604e82939f67ebfd9142872c9ff56603e07`  
		Last Modified: Wed, 10 Jun 2026 00:23:34 GMT  
		Size: 3.6 MB (3591852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87dad43f2e16c76f58e5e2753765caecdfbc1feb72bd08841a5964c4da7ab22c`  
		Last Modified: Wed, 10 Jun 2026 18:27:59 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac80a7065539574d0aff698d1fc76d3744f2f00b3e6d68314fb4cb84f0e37d7`  
		Last Modified: Wed, 10 Jun 2026 18:27:59 GMT  
		Size: 108.9 KB (108888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef744b36d8487e33054d1c30cfebd18490c05aca17b4f574720ce1dda3c78412`  
		Last Modified: Wed, 10 Jun 2026 18:28:00 GMT  
		Size: 4.2 MB (4213337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a136ba7f82c19e371c7e2c7a4ee25ed1de41441c27feecbc6b989e7c79afe3f`  
		Last Modified: Wed, 10 Jun 2026 18:27:59 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:653819d879edda4020f6a5bd344241c2e118781fbd50319cfabeb965557c4234`  
		Last Modified: Wed, 10 Jun 2026 18:28:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:7715a9e3170ec3a2143b197fb80db0a2d670d751a4d710a95942ec384df85a58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4297ab54a68ba59e6d3d700921a359e4850605f249ec473c36391bf423a0017b`

```dockerfile
```

-	Layers:
	-	`sha256:a1889ec9b4bd651c813e65a363b785ace86c68a6095f41a397172d7acdc47058`  
		Last Modified: Wed, 10 Jun 2026 18:27:59 GMT  
		Size: 94.3 KB (94300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec157ceb7ee3f109ef2e714168e5904e088b28fcab859065403f0a617f121d82`  
		Last Modified: Wed, 10 Jun 2026 18:27:59 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.24` - linux; s390x

```console
$ docker pull memcached@sha256:084c53e2e39a12bbca6189febd6d4e2aadf6ccdd85445553f9a237d6c3608c3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8107287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de51c430e27f993bbd7f1be7334cdb2818c849b8e7c017552ff8cdb5fb2c2949`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2026 20:18:16 GMT
ADD alpine-minirootfs-3.24.0-s390x.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:18:16 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 18:20:00 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jun 2026 18:20:05 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jun 2026 18:49:55 GMT
ENV MEMCACHED_VERSION=1.6.42
# Wed, 10 Jun 2026 18:49:55 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.42.tar.gz
# Wed, 10 Jun 2026 18:49:55 GMT
ENV MEMCACHED_SHA1=de453f58745238c70091fe243549c406aabdc3c5
# Wed, 10 Jun 2026 18:49:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jun 2026 18:49:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 18:50:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jun 2026 18:50:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 18:50:01 GMT
USER memcache
# Wed, 10 Jun 2026 18:50:01 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jun 2026 18:50:01 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4c421b7ac5771added0d41fbc2e1c815472072561366ed82ab9e16b926cb03c6`  
		Last Modified: Tue, 09 Jun 2026 20:18:26 GMT  
		Size: 3.7 MB (3730217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0711a972fdad3ac072246017b11d2279363fa9074279aef5f300474872ae8bd7`  
		Last Modified: Wed, 10 Jun 2026 18:50:43 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a6a5c3b22bd7a4743610e767f8e08c5bb66379e7420935b5ad890c02be1af8`  
		Last Modified: Wed, 10 Jun 2026 18:50:43 GMT  
		Size: 114.3 KB (114292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:791d693469c94f11b8cfc977eadf134459f8e13d0f21ba48b4b04664df753f71`  
		Last Modified: Wed, 10 Jun 2026 18:50:45 GMT  
		Size: 4.3 MB (4261419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dd8c588e70e6f166476b33c198ee2d77a7b5d952207365e20799c8415f1fb27`  
		Last Modified: Wed, 10 Jun 2026 18:50:43 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c17c044babfc798701d6dbfde3b27966cccf07ccfffb49929017250e203878c5`  
		Last Modified: Wed, 10 Jun 2026 18:50:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.24` - unknown; unknown

```console
$ docker pull memcached@sha256:b86d70017763ec3335085643c4fc858eb4d0ecd80da1533ab7844a082ea2096c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dde6eca01b66c07c19e6987128b39e14d1395da122e9f2a4b85c663667255978`

```dockerfile
```

-	Layers:
	-	`sha256:003e58d9144c67eaa1a52c05fa8df2908964b8150d09d954940f1c90844cf74c`  
		Last Modified: Wed, 10 Jun 2026 18:50:43 GMT  
		Size: 94.2 KB (94246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd8a5086e89c6d7f95c68b2f90f54a4730f057dc511969769bfe3bcc9a2d57da`  
		Last Modified: Wed, 10 Jun 2026 18:50:44 GMT  
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
