<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `memcached`

-	[`memcached:1`](#memcached1)
-	[`memcached:1.6`](#memcached16)
-	[`memcached:1.6.9`](#memcached169)
-	[`memcached:1.6.9-alpine`](#memcached169-alpine)
-	[`memcached:1.6-alpine`](#memcached16-alpine)
-	[`memcached:1-alpine`](#memcached1-alpine)
-	[`memcached:alpine`](#memcachedalpine)
-	[`memcached:latest`](#memcachedlatest)

## `memcached:1`

```console
$ docker pull memcached@sha256:944f6eb53be39dfcb895ab110d685e4f0320ffa00b8a1c0fe35aeb52f4f89d30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `memcached:1` - linux; amd64

```console
$ docker pull memcached@sha256:6d78552afa63c897afdb38ac829e12f04779ed8c59b7caaa23371e00f57b70fb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 MB (30507788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dac5d0dc8aa45ddc209b926c202ff526cee0efba6582686c8d6c0dcd85f00eaa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 11 Dec 2020 02:06:10 GMT
ADD file:3a7bff4e139bcacc5831fd70a035c130a91b5da001dd91c08b2acd635c7064e8 in / 
# Fri, 11 Dec 2020 02:06:10 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 06:14:16 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Fri, 11 Dec 2020 06:14:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 06:14:21 GMT
ENV MEMCACHED_VERSION=1.6.9
# Fri, 11 Dec 2020 06:14:21 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Fri, 11 Dec 2020 06:19:00 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Fri, 11 Dec 2020 06:19:00 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Fri, 11 Dec 2020 06:19:02 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 11 Dec 2020 06:19:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 06:19:02 GMT
USER memcache
# Fri, 11 Dec 2020 06:19:03 GMT
EXPOSE 11211
# Fri, 11 Dec 2020 06:19:03 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6ec7b7d162b24bd6df88abde89ceb6d7bbc2be927f025c9dd061af2b0c328cfe`  
		Last Modified: Fri, 11 Dec 2020 02:12:26 GMT  
		Size: 27.1 MB (27099295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9818b92b6967ba1cd3b0f1e2d737b06a5c35c86f33459aabaffc428f24e645b1`  
		Last Modified: Fri, 11 Dec 2020 06:24:23 GMT  
		Size: 5.0 KB (4984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9544667d8552cce305a40b1b48e6b093e78ea017033e55711a59b5c37c53394`  
		Last Modified: Fri, 11 Dec 2020 06:24:23 GMT  
		Size: 2.2 MB (2196778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b877c55f6d97a0b40d741a747c9b118c51bf1163b613bae389a7364ce7e24222`  
		Last Modified: Fri, 11 Dec 2020 06:24:23 GMT  
		Size: 1.2 MB (1206324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8facb17105d37c092d0638d397ff7764c35b746327da272f54040fa1f90ac98c`  
		Last Modified: Fri, 11 Dec 2020 06:24:22 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee20652cffd7b48ba83f645a010a98c20af2035fc94be68981de899035dc657b`  
		Last Modified: Fri, 11 Dec 2020 06:24:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1` - linux; arm variant v5

```console
$ docker pull memcached@sha256:0373c46dd337fbf5f8a2c3577436549a0100b721e5ce04c418d516a328f43f82
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.9 MB (27925021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddff2df6aa17cc7f39472a8f3aa245748cb771b7c0224dd869a8f6ca56828b2a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:49 GMT
ADD file:58ebb3ffaf26d9b7621efba5f109ae9d22832f2f22865cda36604b138cbdb7b8 in / 
# Fri, 11 Dec 2020 02:04:56 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 03:36:36 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Fri, 11 Dec 2020 03:36:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 03:36:50 GMT
ENV MEMCACHED_VERSION=1.6.9
# Fri, 11 Dec 2020 03:36:52 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Fri, 11 Dec 2020 03:40:48 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Fri, 11 Dec 2020 03:40:49 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Fri, 11 Dec 2020 03:40:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 11 Dec 2020 03:40:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 03:40:55 GMT
USER memcache
# Fri, 11 Dec 2020 03:40:56 GMT
EXPOSE 11211
# Fri, 11 Dec 2020 03:40:58 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8cbd1f790d64c77fcac6c9dbfe4d4c82f0365de9438f1a42b0560dc88f9e6a55`  
		Last Modified: Fri, 11 Dec 2020 02:14:44 GMT  
		Size: 24.8 MB (24843461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:803513e868412453cb2bdaa71c148eab32e8f4cfaee3543153975947f87b661f`  
		Last Modified: Fri, 11 Dec 2020 03:41:20 GMT  
		Size: 4.9 KB (4893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59c7cf3dbc3c0b485c43489bcda8bbd0193303b2647fad83d7805e80e1f6941`  
		Last Modified: Fri, 11 Dec 2020 03:41:21 GMT  
		Size: 1.9 MB (1897145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98bb531a4f2242979d0549a74f72a40522c6b4d74e4243503c995916b19ad2db`  
		Last Modified: Fri, 11 Dec 2020 03:41:20 GMT  
		Size: 1.2 MB (1179116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:678b76c238901201d213d9b7db70aa329013315d456d5443f32c905426f99799`  
		Last Modified: Fri, 11 Dec 2020 03:41:20 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0151320cb9bcff65b1aace9cea43dcfdd6c3e82ac7c93be4c62abe843d6499cc`  
		Last Modified: Fri, 11 Dec 2020 03:41:20 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1` - linux; arm variant v7

```console
$ docker pull memcached@sha256:7731cf0112d45e7b8c852237c66a7f46ca0e185320094e2bacc4ac17fb00b308
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25674187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81ab97c7b1a8af34be252318deb461a0f1a2e4ca023041276e9ad4a03cdfaec2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 11 Dec 2020 02:23:37 GMT
ADD file:75ca842ac2d6e9f6617bb3df280af1e4c9619c9805fd5e00c1c3d6b8b4e3d802 in / 
# Fri, 11 Dec 2020 02:23:39 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 04:40:02 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Fri, 11 Dec 2020 04:40:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 04:40:20 GMT
ENV MEMCACHED_VERSION=1.6.9
# Fri, 11 Dec 2020 04:40:22 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Fri, 11 Dec 2020 04:43:59 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Fri, 11 Dec 2020 04:44:00 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Fri, 11 Dec 2020 04:44:02 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 11 Dec 2020 04:44:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 04:44:04 GMT
USER memcache
# Fri, 11 Dec 2020 04:44:05 GMT
EXPOSE 11211
# Fri, 11 Dec 2020 04:44:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c06905228d4fc5a5c840a70e2e6ced56596a8bc73abc69e6a1867bbb6f7ae7e7`  
		Last Modified: Fri, 11 Dec 2020 02:33:07 GMT  
		Size: 22.7 MB (22707662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92651243e16dc9394c858200d94836db14ccba7cb4834aeeae694f0a4687cf6b`  
		Last Modified: Fri, 11 Dec 2020 04:47:52 GMT  
		Size: 4.9 KB (4892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b2d826e32b2f2e43c3e916a26bd2df22d1c05b4a3c269771f692cc6109a5219`  
		Last Modified: Fri, 11 Dec 2020 04:47:53 GMT  
		Size: 1.8 MB (1811638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d51d0c29898f0b1851ca4596deed2bce269765e91227407da6a13ed97f36789b`  
		Last Modified: Fri, 11 Dec 2020 04:47:52 GMT  
		Size: 1.1 MB (1149588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9980de41615bdd4ec214564640fc3debc326ee0a2f0c5010dc348cb0688c63fa`  
		Last Modified: Fri, 11 Dec 2020 04:47:53 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b841afed721ef8c4147c8af69401487f31b89d0d483e01b0b1e6dd9f6f3f9fa0`  
		Last Modified: Fri, 11 Dec 2020 04:47:52 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:ba77a96f15913bc91a757d3092df841020bc4bfb5eb8d2e379e2b574d233dee5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29115518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96037dc9e04dc221c12561d6fd7b9838b736d23355b5183cf1f847c7ca2a7be8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 11 Dec 2020 02:45:53 GMT
ADD file:a5a2f039c00bc638b88cefdff4c3cd1865b4d415bf80c4fe6b496d975af7cc1f in / 
# Fri, 11 Dec 2020 02:45:57 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 06:17:49 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Fri, 11 Dec 2020 06:17:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 06:17:58 GMT
ENV MEMCACHED_VERSION=1.6.9
# Fri, 11 Dec 2020 06:17:59 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Fri, 11 Dec 2020 06:21:52 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Fri, 11 Dec 2020 06:21:52 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Fri, 11 Dec 2020 06:21:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 11 Dec 2020 06:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 06:21:56 GMT
USER memcache
# Fri, 11 Dec 2020 06:21:57 GMT
EXPOSE 11211
# Fri, 11 Dec 2020 06:21:57 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c9648d7fcbb6d597cf33916d8fcd207fde8ec05d764b4480d4f3e884e142a902`  
		Last Modified: Fri, 11 Dec 2020 02:53:14 GMT  
		Size: 25.9 MB (25856191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4a2989a5f0ead8f181bf0a3d83c3942b680601a3d54507ae9cc7e9de4c0753e`  
		Last Modified: Fri, 11 Dec 2020 06:25:40 GMT  
		Size: 5.0 KB (5025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d8830b39b6645b4cb0dde9646d4f8061cdf8ada45104e46f5b34a61ac86bed`  
		Last Modified: Fri, 11 Dec 2020 06:25:40 GMT  
		Size: 2.1 MB (2075073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d391a789256382a7a47ee06b4d35a3edded36259031fb3224ba5f7ca1f9742d4`  
		Last Modified: Fri, 11 Dec 2020 06:25:40 GMT  
		Size: 1.2 MB (1178823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfb3c1da48281e238cd187736bfa7235d50ff6259377132eefe18e3232a0447c`  
		Last Modified: Fri, 11 Dec 2020 06:25:40 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c504fa6fcce1d5dcf11dce135016d72f448155fab34ab26f437e352cdaf216ac`  
		Last Modified: Fri, 11 Dec 2020 06:25:39 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1` - linux; 386

```console
$ docker pull memcached@sha256:863e1bdc397af4d93b2c8e1eb0a45e0c142993b6b8fd603a3e1bbe6dc3b4ef9b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31175097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:542592c8f397aed9543c98f050687f49357cc4b41dca959a9ddf05d8a9198925`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 11 Dec 2020 02:03:07 GMT
ADD file:a0879774b23f70c4db7f7b04736cca142beb0b22e93f5952364ca990a1675552 in / 
# Fri, 11 Dec 2020 02:03:08 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 05:34:46 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Fri, 11 Dec 2020 05:34:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 05:34:54 GMT
ENV MEMCACHED_VERSION=1.6.9
# Fri, 11 Dec 2020 05:34:55 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Fri, 11 Dec 2020 05:39:41 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Fri, 11 Dec 2020 05:39:41 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Fri, 11 Dec 2020 05:39:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 11 Dec 2020 05:39:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 05:39:43 GMT
USER memcache
# Fri, 11 Dec 2020 05:39:44 GMT
EXPOSE 11211
# Fri, 11 Dec 2020 05:39:44 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:cfec07a090788e68b692f30d34e11dc7af0f1c8112fbc846e8e40e24faf882d7`  
		Last Modified: Fri, 11 Dec 2020 02:09:41 GMT  
		Size: 27.8 MB (27757584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:125b182979466ebdbd3684a56e18ea817967570f9d1da07d9c718800ee13b416`  
		Last Modified: Fri, 11 Dec 2020 05:45:04 GMT  
		Size: 4.9 KB (4896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285fdabbbbfd7d8439d518ed03f316e8f277aa4a9065eb0f7e8aca3e742715ba`  
		Last Modified: Fri, 11 Dec 2020 05:45:04 GMT  
		Size: 2.2 MB (2208312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d562f6207bb4224e6ed498f2681d75cd3b8a29895ac7937d7aa7365bed41a0`  
		Last Modified: Fri, 11 Dec 2020 05:45:05 GMT  
		Size: 1.2 MB (1203898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa4610f56210f92d9512e834853224b8c11fe48b8e905c119fccbf8c9ea5735`  
		Last Modified: Fri, 11 Dec 2020 05:45:04 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09602d135be3e9fa1bd567c87855653a3e3c8f8eaf212c6877c123615940b3b`  
		Last Modified: Fri, 11 Dec 2020 05:45:04 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1` - linux; mips64le

```console
$ docker pull memcached@sha256:7db583e5b72c87669d31ad8e231e6c7adfdaf7d534c936f229b982b5e0dae8a3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.8 MB (28750173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f1fa615248a5befd5ecbf5f7a7a1eafcb767aa432e95d5b65347dd114d893fa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 11 Dec 2020 02:03:30 GMT
ADD file:edb758d587972f30ef28b162dcabf79f61b685afa3c6066cb611c61abea124f3 in / 
# Fri, 11 Dec 2020 02:03:30 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 03:09:11 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Fri, 11 Dec 2020 03:09:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 03:09:24 GMT
ENV MEMCACHED_VERSION=1.6.9
# Fri, 11 Dec 2020 03:09:24 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Fri, 11 Dec 2020 03:15:05 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Fri, 11 Dec 2020 03:15:05 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Fri, 11 Dec 2020 03:15:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 11 Dec 2020 03:15:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 03:15:07 GMT
USER memcache
# Fri, 11 Dec 2020 03:15:08 GMT
EXPOSE 11211
# Fri, 11 Dec 2020 03:15:08 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bed35f8e8e003f268bd91c8bc28d93f0b1463296add14ab3ec84c3d3d30e9025`  
		Last Modified: Fri, 11 Dec 2020 02:10:15 GMT  
		Size: 25.8 MB (25769881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ad87d218b0aae22ee1256aeaeb3c17629573b0974420752b41c8669bd82173`  
		Last Modified: Fri, 11 Dec 2020 03:15:31 GMT  
		Size: 5.0 KB (4979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c113c88acc60509bb945511ae953da94c2f6cba67440c33d6d592568b131ae0`  
		Last Modified: Fri, 11 Dec 2020 03:15:32 GMT  
		Size: 1.8 MB (1776264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86f68e3fb18b7005b2291db6286f4b8be1a908a5dbc4cbea34f789b583729d1c`  
		Last Modified: Fri, 11 Dec 2020 03:15:32 GMT  
		Size: 1.2 MB (1198641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01eccd7ed1e8b1bc7ae953db8ed512bb963d96e5523bcbbe8ac0b7130b246266`  
		Last Modified: Fri, 11 Dec 2020 03:15:31 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:224d3b20e2efa0cb7b62cd59a9572f87606ff20c5b3bf04ea2a23f17a836efa7`  
		Last Modified: Fri, 11 Dec 2020 03:15:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1` - linux; ppc64le

```console
$ docker pull memcached@sha256:6f8c28503a9a3aadaba20c8a60fea9f450cff6023be384229c6093d1cce78a32
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.1 MB (34085694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f68f9d6f6d0ff09d1c44ad6fdc31842fa02b165535d452d0cf7ced031aca0ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 11 Dec 2020 03:34:02 GMT
ADD file:eca1a7737bd5e84ff883c4c284c0cd22492145d9cd7ae3b8e7b490e3d8e5aefb in / 
# Fri, 11 Dec 2020 03:34:11 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 16:07:08 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Fri, 11 Dec 2020 16:07:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 16:07:29 GMT
ENV MEMCACHED_VERSION=1.6.9
# Fri, 11 Dec 2020 16:07:31 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Fri, 11 Dec 2020 16:14:44 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Fri, 11 Dec 2020 16:14:48 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Fri, 11 Dec 2020 16:14:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 11 Dec 2020 16:15:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 16:15:02 GMT
USER memcache
# Fri, 11 Dec 2020 16:15:04 GMT
EXPOSE 11211
# Fri, 11 Dec 2020 16:15:07 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c0f0648876332890be87a9f32ec4ad2a939e805be3152ab991a923f7dec2b35d`  
		Last Modified: Fri, 11 Dec 2020 03:41:39 GMT  
		Size: 30.5 MB (30524717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86be564d1b6e201f1d3e3d2ce8c9f7d54d6db1ba9303e9298d16527aa7022552`  
		Last Modified: Fri, 11 Dec 2020 16:20:10 GMT  
		Size: 5.0 KB (4985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea84c614bd4b7a09070e40efb6388c77482da788f3f51158d7bdf2920858b5c5`  
		Last Modified: Fri, 11 Dec 2020 16:20:09 GMT  
		Size: 2.3 MB (2322953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e7a7cdc7a222a1e649894b9cd60aaf904f5e600c65f1542ccc70457826bf54`  
		Last Modified: Fri, 11 Dec 2020 16:20:10 GMT  
		Size: 1.2 MB (1232631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:124ca47ab85a63f4ae7b141905196be41389d3a529dd605b341f7b26201c6262`  
		Last Modified: Fri, 11 Dec 2020 16:20:10 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12cb3df4339b3922a947928cfb29b24307e1a3aed08a26a807b27a40c520c432`  
		Last Modified: Fri, 11 Dec 2020 16:20:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1` - linux; s390x

```console
$ docker pull memcached@sha256:3d178b57d4226285dd7555e8a466e47337bedcb188d20e07049daa6e84b7f49a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.8 MB (28804148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6dc93e8d3427938db6bb6a79bae64a3e0f3e2813e8e662e272f8e62a6e7e94b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 11 Dec 2020 02:12:11 GMT
ADD file:db86ce5a1665b6d8ac734c54ac249a811c58484f569b935b14772445962428aa in / 
# Fri, 11 Dec 2020 02:12:15 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 03:36:28 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Fri, 11 Dec 2020 03:36:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 03:36:33 GMT
ENV MEMCACHED_VERSION=1.6.9
# Fri, 11 Dec 2020 03:36:34 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Fri, 11 Dec 2020 03:40:23 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Fri, 11 Dec 2020 03:40:23 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Fri, 11 Dec 2020 03:40:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 11 Dec 2020 03:40:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 03:40:25 GMT
USER memcache
# Fri, 11 Dec 2020 03:40:26 GMT
EXPOSE 11211
# Fri, 11 Dec 2020 03:40:26 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f4cf10ca9f31aab0854647d7878dc4db838e93b892b843dde3db24f2e909a106`  
		Last Modified: Fri, 11 Dec 2020 02:17:07 GMT  
		Size: 25.7 MB (25713957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5fee0f9b7c8f8029b3f0e84c478491b92a268655b1f6d560bc233b2ae31ebb1`  
		Last Modified: Fri, 11 Dec 2020 03:45:07 GMT  
		Size: 5.0 KB (5025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33dd61679906d3d1911efeb12a5b0aa35b2663ecdfa293504b022b5e475177bc`  
		Last Modified: Fri, 11 Dec 2020 03:45:08 GMT  
		Size: 1.9 MB (1886302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c0c80075aa43e4d25ca63fe3b55044f06f3955f2d4e356238a25578e26b629f`  
		Last Modified: Fri, 11 Dec 2020 03:45:07 GMT  
		Size: 1.2 MB (1198456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65c68b5e030c291a2b89d310aa10afd000bba8b1e52baaf825baf1de8e87d45d`  
		Last Modified: Fri, 11 Dec 2020 03:45:07 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf651365e6ca5de80f44c00f8cf1f9b822bc0cf09443dc1fd0ca11935567b37`  
		Last Modified: Fri, 11 Dec 2020 03:45:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:1.6`

```console
$ docker pull memcached@sha256:944f6eb53be39dfcb895ab110d685e4f0320ffa00b8a1c0fe35aeb52f4f89d30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `memcached:1.6` - linux; amd64

```console
$ docker pull memcached@sha256:6d78552afa63c897afdb38ac829e12f04779ed8c59b7caaa23371e00f57b70fb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 MB (30507788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dac5d0dc8aa45ddc209b926c202ff526cee0efba6582686c8d6c0dcd85f00eaa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 11 Dec 2020 02:06:10 GMT
ADD file:3a7bff4e139bcacc5831fd70a035c130a91b5da001dd91c08b2acd635c7064e8 in / 
# Fri, 11 Dec 2020 02:06:10 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 06:14:16 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Fri, 11 Dec 2020 06:14:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 06:14:21 GMT
ENV MEMCACHED_VERSION=1.6.9
# Fri, 11 Dec 2020 06:14:21 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Fri, 11 Dec 2020 06:19:00 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Fri, 11 Dec 2020 06:19:00 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Fri, 11 Dec 2020 06:19:02 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 11 Dec 2020 06:19:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 06:19:02 GMT
USER memcache
# Fri, 11 Dec 2020 06:19:03 GMT
EXPOSE 11211
# Fri, 11 Dec 2020 06:19:03 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6ec7b7d162b24bd6df88abde89ceb6d7bbc2be927f025c9dd061af2b0c328cfe`  
		Last Modified: Fri, 11 Dec 2020 02:12:26 GMT  
		Size: 27.1 MB (27099295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9818b92b6967ba1cd3b0f1e2d737b06a5c35c86f33459aabaffc428f24e645b1`  
		Last Modified: Fri, 11 Dec 2020 06:24:23 GMT  
		Size: 5.0 KB (4984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9544667d8552cce305a40b1b48e6b093e78ea017033e55711a59b5c37c53394`  
		Last Modified: Fri, 11 Dec 2020 06:24:23 GMT  
		Size: 2.2 MB (2196778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b877c55f6d97a0b40d741a747c9b118c51bf1163b613bae389a7364ce7e24222`  
		Last Modified: Fri, 11 Dec 2020 06:24:23 GMT  
		Size: 1.2 MB (1206324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8facb17105d37c092d0638d397ff7764c35b746327da272f54040fa1f90ac98c`  
		Last Modified: Fri, 11 Dec 2020 06:24:22 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee20652cffd7b48ba83f645a010a98c20af2035fc94be68981de899035dc657b`  
		Last Modified: Fri, 11 Dec 2020 06:24:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6` - linux; arm variant v5

```console
$ docker pull memcached@sha256:0373c46dd337fbf5f8a2c3577436549a0100b721e5ce04c418d516a328f43f82
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.9 MB (27925021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddff2df6aa17cc7f39472a8f3aa245748cb771b7c0224dd869a8f6ca56828b2a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:49 GMT
ADD file:58ebb3ffaf26d9b7621efba5f109ae9d22832f2f22865cda36604b138cbdb7b8 in / 
# Fri, 11 Dec 2020 02:04:56 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 03:36:36 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Fri, 11 Dec 2020 03:36:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 03:36:50 GMT
ENV MEMCACHED_VERSION=1.6.9
# Fri, 11 Dec 2020 03:36:52 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Fri, 11 Dec 2020 03:40:48 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Fri, 11 Dec 2020 03:40:49 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Fri, 11 Dec 2020 03:40:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 11 Dec 2020 03:40:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 03:40:55 GMT
USER memcache
# Fri, 11 Dec 2020 03:40:56 GMT
EXPOSE 11211
# Fri, 11 Dec 2020 03:40:58 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8cbd1f790d64c77fcac6c9dbfe4d4c82f0365de9438f1a42b0560dc88f9e6a55`  
		Last Modified: Fri, 11 Dec 2020 02:14:44 GMT  
		Size: 24.8 MB (24843461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:803513e868412453cb2bdaa71c148eab32e8f4cfaee3543153975947f87b661f`  
		Last Modified: Fri, 11 Dec 2020 03:41:20 GMT  
		Size: 4.9 KB (4893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59c7cf3dbc3c0b485c43489bcda8bbd0193303b2647fad83d7805e80e1f6941`  
		Last Modified: Fri, 11 Dec 2020 03:41:21 GMT  
		Size: 1.9 MB (1897145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98bb531a4f2242979d0549a74f72a40522c6b4d74e4243503c995916b19ad2db`  
		Last Modified: Fri, 11 Dec 2020 03:41:20 GMT  
		Size: 1.2 MB (1179116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:678b76c238901201d213d9b7db70aa329013315d456d5443f32c905426f99799`  
		Last Modified: Fri, 11 Dec 2020 03:41:20 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0151320cb9bcff65b1aace9cea43dcfdd6c3e82ac7c93be4c62abe843d6499cc`  
		Last Modified: Fri, 11 Dec 2020 03:41:20 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6` - linux; arm variant v7

```console
$ docker pull memcached@sha256:7731cf0112d45e7b8c852237c66a7f46ca0e185320094e2bacc4ac17fb00b308
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25674187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81ab97c7b1a8af34be252318deb461a0f1a2e4ca023041276e9ad4a03cdfaec2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 11 Dec 2020 02:23:37 GMT
ADD file:75ca842ac2d6e9f6617bb3df280af1e4c9619c9805fd5e00c1c3d6b8b4e3d802 in / 
# Fri, 11 Dec 2020 02:23:39 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 04:40:02 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Fri, 11 Dec 2020 04:40:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 04:40:20 GMT
ENV MEMCACHED_VERSION=1.6.9
# Fri, 11 Dec 2020 04:40:22 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Fri, 11 Dec 2020 04:43:59 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Fri, 11 Dec 2020 04:44:00 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Fri, 11 Dec 2020 04:44:02 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 11 Dec 2020 04:44:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 04:44:04 GMT
USER memcache
# Fri, 11 Dec 2020 04:44:05 GMT
EXPOSE 11211
# Fri, 11 Dec 2020 04:44:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c06905228d4fc5a5c840a70e2e6ced56596a8bc73abc69e6a1867bbb6f7ae7e7`  
		Last Modified: Fri, 11 Dec 2020 02:33:07 GMT  
		Size: 22.7 MB (22707662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92651243e16dc9394c858200d94836db14ccba7cb4834aeeae694f0a4687cf6b`  
		Last Modified: Fri, 11 Dec 2020 04:47:52 GMT  
		Size: 4.9 KB (4892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b2d826e32b2f2e43c3e916a26bd2df22d1c05b4a3c269771f692cc6109a5219`  
		Last Modified: Fri, 11 Dec 2020 04:47:53 GMT  
		Size: 1.8 MB (1811638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d51d0c29898f0b1851ca4596deed2bce269765e91227407da6a13ed97f36789b`  
		Last Modified: Fri, 11 Dec 2020 04:47:52 GMT  
		Size: 1.1 MB (1149588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9980de41615bdd4ec214564640fc3debc326ee0a2f0c5010dc348cb0688c63fa`  
		Last Modified: Fri, 11 Dec 2020 04:47:53 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b841afed721ef8c4147c8af69401487f31b89d0d483e01b0b1e6dd9f6f3f9fa0`  
		Last Modified: Fri, 11 Dec 2020 04:47:52 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:ba77a96f15913bc91a757d3092df841020bc4bfb5eb8d2e379e2b574d233dee5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29115518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96037dc9e04dc221c12561d6fd7b9838b736d23355b5183cf1f847c7ca2a7be8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 11 Dec 2020 02:45:53 GMT
ADD file:a5a2f039c00bc638b88cefdff4c3cd1865b4d415bf80c4fe6b496d975af7cc1f in / 
# Fri, 11 Dec 2020 02:45:57 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 06:17:49 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Fri, 11 Dec 2020 06:17:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 06:17:58 GMT
ENV MEMCACHED_VERSION=1.6.9
# Fri, 11 Dec 2020 06:17:59 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Fri, 11 Dec 2020 06:21:52 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Fri, 11 Dec 2020 06:21:52 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Fri, 11 Dec 2020 06:21:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 11 Dec 2020 06:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 06:21:56 GMT
USER memcache
# Fri, 11 Dec 2020 06:21:57 GMT
EXPOSE 11211
# Fri, 11 Dec 2020 06:21:57 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c9648d7fcbb6d597cf33916d8fcd207fde8ec05d764b4480d4f3e884e142a902`  
		Last Modified: Fri, 11 Dec 2020 02:53:14 GMT  
		Size: 25.9 MB (25856191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4a2989a5f0ead8f181bf0a3d83c3942b680601a3d54507ae9cc7e9de4c0753e`  
		Last Modified: Fri, 11 Dec 2020 06:25:40 GMT  
		Size: 5.0 KB (5025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d8830b39b6645b4cb0dde9646d4f8061cdf8ada45104e46f5b34a61ac86bed`  
		Last Modified: Fri, 11 Dec 2020 06:25:40 GMT  
		Size: 2.1 MB (2075073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d391a789256382a7a47ee06b4d35a3edded36259031fb3224ba5f7ca1f9742d4`  
		Last Modified: Fri, 11 Dec 2020 06:25:40 GMT  
		Size: 1.2 MB (1178823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfb3c1da48281e238cd187736bfa7235d50ff6259377132eefe18e3232a0447c`  
		Last Modified: Fri, 11 Dec 2020 06:25:40 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c504fa6fcce1d5dcf11dce135016d72f448155fab34ab26f437e352cdaf216ac`  
		Last Modified: Fri, 11 Dec 2020 06:25:39 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6` - linux; 386

```console
$ docker pull memcached@sha256:863e1bdc397af4d93b2c8e1eb0a45e0c142993b6b8fd603a3e1bbe6dc3b4ef9b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31175097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:542592c8f397aed9543c98f050687f49357cc4b41dca959a9ddf05d8a9198925`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 11 Dec 2020 02:03:07 GMT
ADD file:a0879774b23f70c4db7f7b04736cca142beb0b22e93f5952364ca990a1675552 in / 
# Fri, 11 Dec 2020 02:03:08 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 05:34:46 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Fri, 11 Dec 2020 05:34:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 05:34:54 GMT
ENV MEMCACHED_VERSION=1.6.9
# Fri, 11 Dec 2020 05:34:55 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Fri, 11 Dec 2020 05:39:41 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Fri, 11 Dec 2020 05:39:41 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Fri, 11 Dec 2020 05:39:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 11 Dec 2020 05:39:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 05:39:43 GMT
USER memcache
# Fri, 11 Dec 2020 05:39:44 GMT
EXPOSE 11211
# Fri, 11 Dec 2020 05:39:44 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:cfec07a090788e68b692f30d34e11dc7af0f1c8112fbc846e8e40e24faf882d7`  
		Last Modified: Fri, 11 Dec 2020 02:09:41 GMT  
		Size: 27.8 MB (27757584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:125b182979466ebdbd3684a56e18ea817967570f9d1da07d9c718800ee13b416`  
		Last Modified: Fri, 11 Dec 2020 05:45:04 GMT  
		Size: 4.9 KB (4896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285fdabbbbfd7d8439d518ed03f316e8f277aa4a9065eb0f7e8aca3e742715ba`  
		Last Modified: Fri, 11 Dec 2020 05:45:04 GMT  
		Size: 2.2 MB (2208312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d562f6207bb4224e6ed498f2681d75cd3b8a29895ac7937d7aa7365bed41a0`  
		Last Modified: Fri, 11 Dec 2020 05:45:05 GMT  
		Size: 1.2 MB (1203898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa4610f56210f92d9512e834853224b8c11fe48b8e905c119fccbf8c9ea5735`  
		Last Modified: Fri, 11 Dec 2020 05:45:04 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09602d135be3e9fa1bd567c87855653a3e3c8f8eaf212c6877c123615940b3b`  
		Last Modified: Fri, 11 Dec 2020 05:45:04 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6` - linux; mips64le

```console
$ docker pull memcached@sha256:7db583e5b72c87669d31ad8e231e6c7adfdaf7d534c936f229b982b5e0dae8a3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.8 MB (28750173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f1fa615248a5befd5ecbf5f7a7a1eafcb767aa432e95d5b65347dd114d893fa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 11 Dec 2020 02:03:30 GMT
ADD file:edb758d587972f30ef28b162dcabf79f61b685afa3c6066cb611c61abea124f3 in / 
# Fri, 11 Dec 2020 02:03:30 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 03:09:11 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Fri, 11 Dec 2020 03:09:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 03:09:24 GMT
ENV MEMCACHED_VERSION=1.6.9
# Fri, 11 Dec 2020 03:09:24 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Fri, 11 Dec 2020 03:15:05 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Fri, 11 Dec 2020 03:15:05 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Fri, 11 Dec 2020 03:15:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 11 Dec 2020 03:15:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 03:15:07 GMT
USER memcache
# Fri, 11 Dec 2020 03:15:08 GMT
EXPOSE 11211
# Fri, 11 Dec 2020 03:15:08 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bed35f8e8e003f268bd91c8bc28d93f0b1463296add14ab3ec84c3d3d30e9025`  
		Last Modified: Fri, 11 Dec 2020 02:10:15 GMT  
		Size: 25.8 MB (25769881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ad87d218b0aae22ee1256aeaeb3c17629573b0974420752b41c8669bd82173`  
		Last Modified: Fri, 11 Dec 2020 03:15:31 GMT  
		Size: 5.0 KB (4979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c113c88acc60509bb945511ae953da94c2f6cba67440c33d6d592568b131ae0`  
		Last Modified: Fri, 11 Dec 2020 03:15:32 GMT  
		Size: 1.8 MB (1776264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86f68e3fb18b7005b2291db6286f4b8be1a908a5dbc4cbea34f789b583729d1c`  
		Last Modified: Fri, 11 Dec 2020 03:15:32 GMT  
		Size: 1.2 MB (1198641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01eccd7ed1e8b1bc7ae953db8ed512bb963d96e5523bcbbe8ac0b7130b246266`  
		Last Modified: Fri, 11 Dec 2020 03:15:31 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:224d3b20e2efa0cb7b62cd59a9572f87606ff20c5b3bf04ea2a23f17a836efa7`  
		Last Modified: Fri, 11 Dec 2020 03:15:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6` - linux; ppc64le

```console
$ docker pull memcached@sha256:6f8c28503a9a3aadaba20c8a60fea9f450cff6023be384229c6093d1cce78a32
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.1 MB (34085694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f68f9d6f6d0ff09d1c44ad6fdc31842fa02b165535d452d0cf7ced031aca0ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 11 Dec 2020 03:34:02 GMT
ADD file:eca1a7737bd5e84ff883c4c284c0cd22492145d9cd7ae3b8e7b490e3d8e5aefb in / 
# Fri, 11 Dec 2020 03:34:11 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 16:07:08 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Fri, 11 Dec 2020 16:07:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 16:07:29 GMT
ENV MEMCACHED_VERSION=1.6.9
# Fri, 11 Dec 2020 16:07:31 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Fri, 11 Dec 2020 16:14:44 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Fri, 11 Dec 2020 16:14:48 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Fri, 11 Dec 2020 16:14:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 11 Dec 2020 16:15:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 16:15:02 GMT
USER memcache
# Fri, 11 Dec 2020 16:15:04 GMT
EXPOSE 11211
# Fri, 11 Dec 2020 16:15:07 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c0f0648876332890be87a9f32ec4ad2a939e805be3152ab991a923f7dec2b35d`  
		Last Modified: Fri, 11 Dec 2020 03:41:39 GMT  
		Size: 30.5 MB (30524717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86be564d1b6e201f1d3e3d2ce8c9f7d54d6db1ba9303e9298d16527aa7022552`  
		Last Modified: Fri, 11 Dec 2020 16:20:10 GMT  
		Size: 5.0 KB (4985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea84c614bd4b7a09070e40efb6388c77482da788f3f51158d7bdf2920858b5c5`  
		Last Modified: Fri, 11 Dec 2020 16:20:09 GMT  
		Size: 2.3 MB (2322953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e7a7cdc7a222a1e649894b9cd60aaf904f5e600c65f1542ccc70457826bf54`  
		Last Modified: Fri, 11 Dec 2020 16:20:10 GMT  
		Size: 1.2 MB (1232631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:124ca47ab85a63f4ae7b141905196be41389d3a529dd605b341f7b26201c6262`  
		Last Modified: Fri, 11 Dec 2020 16:20:10 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12cb3df4339b3922a947928cfb29b24307e1a3aed08a26a807b27a40c520c432`  
		Last Modified: Fri, 11 Dec 2020 16:20:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6` - linux; s390x

```console
$ docker pull memcached@sha256:3d178b57d4226285dd7555e8a466e47337bedcb188d20e07049daa6e84b7f49a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.8 MB (28804148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6dc93e8d3427938db6bb6a79bae64a3e0f3e2813e8e662e272f8e62a6e7e94b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 11 Dec 2020 02:12:11 GMT
ADD file:db86ce5a1665b6d8ac734c54ac249a811c58484f569b935b14772445962428aa in / 
# Fri, 11 Dec 2020 02:12:15 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 03:36:28 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Fri, 11 Dec 2020 03:36:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 03:36:33 GMT
ENV MEMCACHED_VERSION=1.6.9
# Fri, 11 Dec 2020 03:36:34 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Fri, 11 Dec 2020 03:40:23 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Fri, 11 Dec 2020 03:40:23 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Fri, 11 Dec 2020 03:40:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 11 Dec 2020 03:40:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 03:40:25 GMT
USER memcache
# Fri, 11 Dec 2020 03:40:26 GMT
EXPOSE 11211
# Fri, 11 Dec 2020 03:40:26 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f4cf10ca9f31aab0854647d7878dc4db838e93b892b843dde3db24f2e909a106`  
		Last Modified: Fri, 11 Dec 2020 02:17:07 GMT  
		Size: 25.7 MB (25713957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5fee0f9b7c8f8029b3f0e84c478491b92a268655b1f6d560bc233b2ae31ebb1`  
		Last Modified: Fri, 11 Dec 2020 03:45:07 GMT  
		Size: 5.0 KB (5025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33dd61679906d3d1911efeb12a5b0aa35b2663ecdfa293504b022b5e475177bc`  
		Last Modified: Fri, 11 Dec 2020 03:45:08 GMT  
		Size: 1.9 MB (1886302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c0c80075aa43e4d25ca63fe3b55044f06f3955f2d4e356238a25578e26b629f`  
		Last Modified: Fri, 11 Dec 2020 03:45:07 GMT  
		Size: 1.2 MB (1198456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65c68b5e030c291a2b89d310aa10afd000bba8b1e52baaf825baf1de8e87d45d`  
		Last Modified: Fri, 11 Dec 2020 03:45:07 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf651365e6ca5de80f44c00f8cf1f9b822bc0cf09443dc1fd0ca11935567b37`  
		Last Modified: Fri, 11 Dec 2020 03:45:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:1.6.9`

```console
$ docker pull memcached@sha256:944f6eb53be39dfcb895ab110d685e4f0320ffa00b8a1c0fe35aeb52f4f89d30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `memcached:1.6.9` - linux; amd64

```console
$ docker pull memcached@sha256:6d78552afa63c897afdb38ac829e12f04779ed8c59b7caaa23371e00f57b70fb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 MB (30507788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dac5d0dc8aa45ddc209b926c202ff526cee0efba6582686c8d6c0dcd85f00eaa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 11 Dec 2020 02:06:10 GMT
ADD file:3a7bff4e139bcacc5831fd70a035c130a91b5da001dd91c08b2acd635c7064e8 in / 
# Fri, 11 Dec 2020 02:06:10 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 06:14:16 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Fri, 11 Dec 2020 06:14:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 06:14:21 GMT
ENV MEMCACHED_VERSION=1.6.9
# Fri, 11 Dec 2020 06:14:21 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Fri, 11 Dec 2020 06:19:00 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Fri, 11 Dec 2020 06:19:00 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Fri, 11 Dec 2020 06:19:02 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 11 Dec 2020 06:19:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 06:19:02 GMT
USER memcache
# Fri, 11 Dec 2020 06:19:03 GMT
EXPOSE 11211
# Fri, 11 Dec 2020 06:19:03 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6ec7b7d162b24bd6df88abde89ceb6d7bbc2be927f025c9dd061af2b0c328cfe`  
		Last Modified: Fri, 11 Dec 2020 02:12:26 GMT  
		Size: 27.1 MB (27099295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9818b92b6967ba1cd3b0f1e2d737b06a5c35c86f33459aabaffc428f24e645b1`  
		Last Modified: Fri, 11 Dec 2020 06:24:23 GMT  
		Size: 5.0 KB (4984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9544667d8552cce305a40b1b48e6b093e78ea017033e55711a59b5c37c53394`  
		Last Modified: Fri, 11 Dec 2020 06:24:23 GMT  
		Size: 2.2 MB (2196778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b877c55f6d97a0b40d741a747c9b118c51bf1163b613bae389a7364ce7e24222`  
		Last Modified: Fri, 11 Dec 2020 06:24:23 GMT  
		Size: 1.2 MB (1206324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8facb17105d37c092d0638d397ff7764c35b746327da272f54040fa1f90ac98c`  
		Last Modified: Fri, 11 Dec 2020 06:24:22 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee20652cffd7b48ba83f645a010a98c20af2035fc94be68981de899035dc657b`  
		Last Modified: Fri, 11 Dec 2020 06:24:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.9` - linux; arm variant v5

```console
$ docker pull memcached@sha256:0373c46dd337fbf5f8a2c3577436549a0100b721e5ce04c418d516a328f43f82
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.9 MB (27925021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddff2df6aa17cc7f39472a8f3aa245748cb771b7c0224dd869a8f6ca56828b2a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:49 GMT
ADD file:58ebb3ffaf26d9b7621efba5f109ae9d22832f2f22865cda36604b138cbdb7b8 in / 
# Fri, 11 Dec 2020 02:04:56 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 03:36:36 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Fri, 11 Dec 2020 03:36:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 03:36:50 GMT
ENV MEMCACHED_VERSION=1.6.9
# Fri, 11 Dec 2020 03:36:52 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Fri, 11 Dec 2020 03:40:48 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Fri, 11 Dec 2020 03:40:49 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Fri, 11 Dec 2020 03:40:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 11 Dec 2020 03:40:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 03:40:55 GMT
USER memcache
# Fri, 11 Dec 2020 03:40:56 GMT
EXPOSE 11211
# Fri, 11 Dec 2020 03:40:58 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8cbd1f790d64c77fcac6c9dbfe4d4c82f0365de9438f1a42b0560dc88f9e6a55`  
		Last Modified: Fri, 11 Dec 2020 02:14:44 GMT  
		Size: 24.8 MB (24843461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:803513e868412453cb2bdaa71c148eab32e8f4cfaee3543153975947f87b661f`  
		Last Modified: Fri, 11 Dec 2020 03:41:20 GMT  
		Size: 4.9 KB (4893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59c7cf3dbc3c0b485c43489bcda8bbd0193303b2647fad83d7805e80e1f6941`  
		Last Modified: Fri, 11 Dec 2020 03:41:21 GMT  
		Size: 1.9 MB (1897145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98bb531a4f2242979d0549a74f72a40522c6b4d74e4243503c995916b19ad2db`  
		Last Modified: Fri, 11 Dec 2020 03:41:20 GMT  
		Size: 1.2 MB (1179116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:678b76c238901201d213d9b7db70aa329013315d456d5443f32c905426f99799`  
		Last Modified: Fri, 11 Dec 2020 03:41:20 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0151320cb9bcff65b1aace9cea43dcfdd6c3e82ac7c93be4c62abe843d6499cc`  
		Last Modified: Fri, 11 Dec 2020 03:41:20 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.9` - linux; arm variant v7

```console
$ docker pull memcached@sha256:7731cf0112d45e7b8c852237c66a7f46ca0e185320094e2bacc4ac17fb00b308
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25674187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81ab97c7b1a8af34be252318deb461a0f1a2e4ca023041276e9ad4a03cdfaec2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 11 Dec 2020 02:23:37 GMT
ADD file:75ca842ac2d6e9f6617bb3df280af1e4c9619c9805fd5e00c1c3d6b8b4e3d802 in / 
# Fri, 11 Dec 2020 02:23:39 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 04:40:02 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Fri, 11 Dec 2020 04:40:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 04:40:20 GMT
ENV MEMCACHED_VERSION=1.6.9
# Fri, 11 Dec 2020 04:40:22 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Fri, 11 Dec 2020 04:43:59 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Fri, 11 Dec 2020 04:44:00 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Fri, 11 Dec 2020 04:44:02 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 11 Dec 2020 04:44:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 04:44:04 GMT
USER memcache
# Fri, 11 Dec 2020 04:44:05 GMT
EXPOSE 11211
# Fri, 11 Dec 2020 04:44:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c06905228d4fc5a5c840a70e2e6ced56596a8bc73abc69e6a1867bbb6f7ae7e7`  
		Last Modified: Fri, 11 Dec 2020 02:33:07 GMT  
		Size: 22.7 MB (22707662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92651243e16dc9394c858200d94836db14ccba7cb4834aeeae694f0a4687cf6b`  
		Last Modified: Fri, 11 Dec 2020 04:47:52 GMT  
		Size: 4.9 KB (4892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b2d826e32b2f2e43c3e916a26bd2df22d1c05b4a3c269771f692cc6109a5219`  
		Last Modified: Fri, 11 Dec 2020 04:47:53 GMT  
		Size: 1.8 MB (1811638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d51d0c29898f0b1851ca4596deed2bce269765e91227407da6a13ed97f36789b`  
		Last Modified: Fri, 11 Dec 2020 04:47:52 GMT  
		Size: 1.1 MB (1149588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9980de41615bdd4ec214564640fc3debc326ee0a2f0c5010dc348cb0688c63fa`  
		Last Modified: Fri, 11 Dec 2020 04:47:53 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b841afed721ef8c4147c8af69401487f31b89d0d483e01b0b1e6dd9f6f3f9fa0`  
		Last Modified: Fri, 11 Dec 2020 04:47:52 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.9` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:ba77a96f15913bc91a757d3092df841020bc4bfb5eb8d2e379e2b574d233dee5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29115518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96037dc9e04dc221c12561d6fd7b9838b736d23355b5183cf1f847c7ca2a7be8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 11 Dec 2020 02:45:53 GMT
ADD file:a5a2f039c00bc638b88cefdff4c3cd1865b4d415bf80c4fe6b496d975af7cc1f in / 
# Fri, 11 Dec 2020 02:45:57 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 06:17:49 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Fri, 11 Dec 2020 06:17:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 06:17:58 GMT
ENV MEMCACHED_VERSION=1.6.9
# Fri, 11 Dec 2020 06:17:59 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Fri, 11 Dec 2020 06:21:52 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Fri, 11 Dec 2020 06:21:52 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Fri, 11 Dec 2020 06:21:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 11 Dec 2020 06:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 06:21:56 GMT
USER memcache
# Fri, 11 Dec 2020 06:21:57 GMT
EXPOSE 11211
# Fri, 11 Dec 2020 06:21:57 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c9648d7fcbb6d597cf33916d8fcd207fde8ec05d764b4480d4f3e884e142a902`  
		Last Modified: Fri, 11 Dec 2020 02:53:14 GMT  
		Size: 25.9 MB (25856191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4a2989a5f0ead8f181bf0a3d83c3942b680601a3d54507ae9cc7e9de4c0753e`  
		Last Modified: Fri, 11 Dec 2020 06:25:40 GMT  
		Size: 5.0 KB (5025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d8830b39b6645b4cb0dde9646d4f8061cdf8ada45104e46f5b34a61ac86bed`  
		Last Modified: Fri, 11 Dec 2020 06:25:40 GMT  
		Size: 2.1 MB (2075073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d391a789256382a7a47ee06b4d35a3edded36259031fb3224ba5f7ca1f9742d4`  
		Last Modified: Fri, 11 Dec 2020 06:25:40 GMT  
		Size: 1.2 MB (1178823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfb3c1da48281e238cd187736bfa7235d50ff6259377132eefe18e3232a0447c`  
		Last Modified: Fri, 11 Dec 2020 06:25:40 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c504fa6fcce1d5dcf11dce135016d72f448155fab34ab26f437e352cdaf216ac`  
		Last Modified: Fri, 11 Dec 2020 06:25:39 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.9` - linux; 386

```console
$ docker pull memcached@sha256:863e1bdc397af4d93b2c8e1eb0a45e0c142993b6b8fd603a3e1bbe6dc3b4ef9b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31175097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:542592c8f397aed9543c98f050687f49357cc4b41dca959a9ddf05d8a9198925`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 11 Dec 2020 02:03:07 GMT
ADD file:a0879774b23f70c4db7f7b04736cca142beb0b22e93f5952364ca990a1675552 in / 
# Fri, 11 Dec 2020 02:03:08 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 05:34:46 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Fri, 11 Dec 2020 05:34:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 05:34:54 GMT
ENV MEMCACHED_VERSION=1.6.9
# Fri, 11 Dec 2020 05:34:55 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Fri, 11 Dec 2020 05:39:41 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Fri, 11 Dec 2020 05:39:41 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Fri, 11 Dec 2020 05:39:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 11 Dec 2020 05:39:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 05:39:43 GMT
USER memcache
# Fri, 11 Dec 2020 05:39:44 GMT
EXPOSE 11211
# Fri, 11 Dec 2020 05:39:44 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:cfec07a090788e68b692f30d34e11dc7af0f1c8112fbc846e8e40e24faf882d7`  
		Last Modified: Fri, 11 Dec 2020 02:09:41 GMT  
		Size: 27.8 MB (27757584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:125b182979466ebdbd3684a56e18ea817967570f9d1da07d9c718800ee13b416`  
		Last Modified: Fri, 11 Dec 2020 05:45:04 GMT  
		Size: 4.9 KB (4896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285fdabbbbfd7d8439d518ed03f316e8f277aa4a9065eb0f7e8aca3e742715ba`  
		Last Modified: Fri, 11 Dec 2020 05:45:04 GMT  
		Size: 2.2 MB (2208312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d562f6207bb4224e6ed498f2681d75cd3b8a29895ac7937d7aa7365bed41a0`  
		Last Modified: Fri, 11 Dec 2020 05:45:05 GMT  
		Size: 1.2 MB (1203898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa4610f56210f92d9512e834853224b8c11fe48b8e905c119fccbf8c9ea5735`  
		Last Modified: Fri, 11 Dec 2020 05:45:04 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09602d135be3e9fa1bd567c87855653a3e3c8f8eaf212c6877c123615940b3b`  
		Last Modified: Fri, 11 Dec 2020 05:45:04 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.9` - linux; mips64le

```console
$ docker pull memcached@sha256:7db583e5b72c87669d31ad8e231e6c7adfdaf7d534c936f229b982b5e0dae8a3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.8 MB (28750173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f1fa615248a5befd5ecbf5f7a7a1eafcb767aa432e95d5b65347dd114d893fa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 11 Dec 2020 02:03:30 GMT
ADD file:edb758d587972f30ef28b162dcabf79f61b685afa3c6066cb611c61abea124f3 in / 
# Fri, 11 Dec 2020 02:03:30 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 03:09:11 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Fri, 11 Dec 2020 03:09:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 03:09:24 GMT
ENV MEMCACHED_VERSION=1.6.9
# Fri, 11 Dec 2020 03:09:24 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Fri, 11 Dec 2020 03:15:05 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Fri, 11 Dec 2020 03:15:05 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Fri, 11 Dec 2020 03:15:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 11 Dec 2020 03:15:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 03:15:07 GMT
USER memcache
# Fri, 11 Dec 2020 03:15:08 GMT
EXPOSE 11211
# Fri, 11 Dec 2020 03:15:08 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bed35f8e8e003f268bd91c8bc28d93f0b1463296add14ab3ec84c3d3d30e9025`  
		Last Modified: Fri, 11 Dec 2020 02:10:15 GMT  
		Size: 25.8 MB (25769881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ad87d218b0aae22ee1256aeaeb3c17629573b0974420752b41c8669bd82173`  
		Last Modified: Fri, 11 Dec 2020 03:15:31 GMT  
		Size: 5.0 KB (4979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c113c88acc60509bb945511ae953da94c2f6cba67440c33d6d592568b131ae0`  
		Last Modified: Fri, 11 Dec 2020 03:15:32 GMT  
		Size: 1.8 MB (1776264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86f68e3fb18b7005b2291db6286f4b8be1a908a5dbc4cbea34f789b583729d1c`  
		Last Modified: Fri, 11 Dec 2020 03:15:32 GMT  
		Size: 1.2 MB (1198641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01eccd7ed1e8b1bc7ae953db8ed512bb963d96e5523bcbbe8ac0b7130b246266`  
		Last Modified: Fri, 11 Dec 2020 03:15:31 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:224d3b20e2efa0cb7b62cd59a9572f87606ff20c5b3bf04ea2a23f17a836efa7`  
		Last Modified: Fri, 11 Dec 2020 03:15:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.9` - linux; ppc64le

```console
$ docker pull memcached@sha256:6f8c28503a9a3aadaba20c8a60fea9f450cff6023be384229c6093d1cce78a32
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.1 MB (34085694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f68f9d6f6d0ff09d1c44ad6fdc31842fa02b165535d452d0cf7ced031aca0ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 11 Dec 2020 03:34:02 GMT
ADD file:eca1a7737bd5e84ff883c4c284c0cd22492145d9cd7ae3b8e7b490e3d8e5aefb in / 
# Fri, 11 Dec 2020 03:34:11 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 16:07:08 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Fri, 11 Dec 2020 16:07:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 16:07:29 GMT
ENV MEMCACHED_VERSION=1.6.9
# Fri, 11 Dec 2020 16:07:31 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Fri, 11 Dec 2020 16:14:44 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Fri, 11 Dec 2020 16:14:48 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Fri, 11 Dec 2020 16:14:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 11 Dec 2020 16:15:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 16:15:02 GMT
USER memcache
# Fri, 11 Dec 2020 16:15:04 GMT
EXPOSE 11211
# Fri, 11 Dec 2020 16:15:07 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c0f0648876332890be87a9f32ec4ad2a939e805be3152ab991a923f7dec2b35d`  
		Last Modified: Fri, 11 Dec 2020 03:41:39 GMT  
		Size: 30.5 MB (30524717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86be564d1b6e201f1d3e3d2ce8c9f7d54d6db1ba9303e9298d16527aa7022552`  
		Last Modified: Fri, 11 Dec 2020 16:20:10 GMT  
		Size: 5.0 KB (4985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea84c614bd4b7a09070e40efb6388c77482da788f3f51158d7bdf2920858b5c5`  
		Last Modified: Fri, 11 Dec 2020 16:20:09 GMT  
		Size: 2.3 MB (2322953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e7a7cdc7a222a1e649894b9cd60aaf904f5e600c65f1542ccc70457826bf54`  
		Last Modified: Fri, 11 Dec 2020 16:20:10 GMT  
		Size: 1.2 MB (1232631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:124ca47ab85a63f4ae7b141905196be41389d3a529dd605b341f7b26201c6262`  
		Last Modified: Fri, 11 Dec 2020 16:20:10 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12cb3df4339b3922a947928cfb29b24307e1a3aed08a26a807b27a40c520c432`  
		Last Modified: Fri, 11 Dec 2020 16:20:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.9` - linux; s390x

```console
$ docker pull memcached@sha256:3d178b57d4226285dd7555e8a466e47337bedcb188d20e07049daa6e84b7f49a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.8 MB (28804148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6dc93e8d3427938db6bb6a79bae64a3e0f3e2813e8e662e272f8e62a6e7e94b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 11 Dec 2020 02:12:11 GMT
ADD file:db86ce5a1665b6d8ac734c54ac249a811c58484f569b935b14772445962428aa in / 
# Fri, 11 Dec 2020 02:12:15 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 03:36:28 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Fri, 11 Dec 2020 03:36:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 03:36:33 GMT
ENV MEMCACHED_VERSION=1.6.9
# Fri, 11 Dec 2020 03:36:34 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Fri, 11 Dec 2020 03:40:23 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Fri, 11 Dec 2020 03:40:23 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Fri, 11 Dec 2020 03:40:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 11 Dec 2020 03:40:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 03:40:25 GMT
USER memcache
# Fri, 11 Dec 2020 03:40:26 GMT
EXPOSE 11211
# Fri, 11 Dec 2020 03:40:26 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f4cf10ca9f31aab0854647d7878dc4db838e93b892b843dde3db24f2e909a106`  
		Last Modified: Fri, 11 Dec 2020 02:17:07 GMT  
		Size: 25.7 MB (25713957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5fee0f9b7c8f8029b3f0e84c478491b92a268655b1f6d560bc233b2ae31ebb1`  
		Last Modified: Fri, 11 Dec 2020 03:45:07 GMT  
		Size: 5.0 KB (5025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33dd61679906d3d1911efeb12a5b0aa35b2663ecdfa293504b022b5e475177bc`  
		Last Modified: Fri, 11 Dec 2020 03:45:08 GMT  
		Size: 1.9 MB (1886302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c0c80075aa43e4d25ca63fe3b55044f06f3955f2d4e356238a25578e26b629f`  
		Last Modified: Fri, 11 Dec 2020 03:45:07 GMT  
		Size: 1.2 MB (1198456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65c68b5e030c291a2b89d310aa10afd000bba8b1e52baaf825baf1de8e87d45d`  
		Last Modified: Fri, 11 Dec 2020 03:45:07 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf651365e6ca5de80f44c00f8cf1f9b822bc0cf09443dc1fd0ca11935567b37`  
		Last Modified: Fri, 11 Dec 2020 03:45:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:1.6.9-alpine`

```console
$ docker pull memcached@sha256:2078c959f70dfd6053c2309d713022ca5b7995f8b1027288c9b5d933a81bfdb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `memcached:1.6.9-alpine` - linux; amd64

```console
$ docker pull memcached@sha256:691e70c8483ee0cd2f9634b2a3e2a129f945c25e1c687937f46b9b407d70d11c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4503585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e141bc64c1463eed191cb3ab1adad1e5ddd70cd5f3a94a2ddd71c5d16849fb5b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:06 GMT
ADD file:62a1e09319acb6d1bad91ef1c35aabdc7e5e19883a77f30f1951ccfffc812124 in / 
# Fri, 11 Dec 2020 02:04:07 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 06:19:22 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Fri, 11 Dec 2020 06:19:24 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Fri, 11 Dec 2020 06:19:24 GMT
ENV MEMCACHED_VERSION=1.6.9
# Fri, 11 Dec 2020 06:19:25 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Fri, 11 Dec 2020 06:24:01 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Fri, 11 Dec 2020 06:24:02 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Fri, 11 Dec 2020 06:24:04 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 11 Dec 2020 06:24:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 06:24:04 GMT
USER memcache
# Fri, 11 Dec 2020 06:24:05 GMT
EXPOSE 11211
# Fri, 11 Dec 2020 06:24:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:05e7bc50f07f000e9993ec0d264b9ffcbb9a01a4d69c68f556d25e9811a8f7f4`  
		Last Modified: Fri, 11 Dec 2020 02:04:37 GMT  
		Size: 2.8 MB (2796945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b5d61d52bf8492fedc6398ec81e362de087350385dcd6af525eeaefb9567f48`  
		Last Modified: Fri, 11 Dec 2020 06:24:32 GMT  
		Size: 1.2 KB (1229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90487ba3ac99c5207669e34d25cf1cbde67b59e61ee8a99a7e864a02393a39b`  
		Last Modified: Fri, 11 Dec 2020 06:24:32 GMT  
		Size: 15.3 KB (15298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9907d94cbfb040b78161ad7a4c2d76f515f9bf6a9298013306b8743d2ec14f83`  
		Last Modified: Fri, 11 Dec 2020 06:24:32 GMT  
		Size: 1.7 MB (1689704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f7796e2d1614664de986b74411d12dc4032b5550d7c2d9f0e8e3a1b8699a2e`  
		Last Modified: Fri, 11 Dec 2020 06:24:32 GMT  
		Size: 288.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f9253a3ddb10ef7212753ded436b4cb46964aa53a3e8b1af412be9e1e9e4a41`  
		Last Modified: Fri, 11 Dec 2020 06:24:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.9-alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:4d05de82436bd51ed609a745b8ddd01e296692beb5a372dcbdcf0b1f54818d03
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4270486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56e8bda6e6346ca01fa3a313ef7bcfcc696040d48be803f6c16922dedc8deae1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 16 Dec 2020 23:49:43 GMT
ADD file:0a16715e2d0e5811c3c578945d618db0e269847a799340248f9ba8d393c9eec2 in / 
# Wed, 16 Dec 2020 23:49:45 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 01:44:25 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Thu, 17 Dec 2020 01:44:29 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Thu, 17 Dec 2020 01:44:30 GMT
ENV MEMCACHED_VERSION=1.6.9
# Thu, 17 Dec 2020 01:44:31 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Thu, 17 Dec 2020 01:47:40 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Thu, 17 Dec 2020 01:47:41 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 17 Dec 2020 01:47:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 17 Dec 2020 01:47:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 01:47:44 GMT
USER memcache
# Thu, 17 Dec 2020 01:47:45 GMT
EXPOSE 11211
# Thu, 17 Dec 2020 01:47:46 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:93247449aef3c56eb4f7ab7b3fed95743c974b823def6dd86ec84008126e7903`  
		Last Modified: Wed, 16 Dec 2020 23:50:24 GMT  
		Size: 2.6 MB (2604163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cc04af65958529b14246e2401008ef0186d74a33d2aa1b64d5f49633a1ff8f1`  
		Last Modified: Thu, 17 Dec 2020 01:48:06 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08bb28157acd02855bdf031eb7158f2cbb9849a6a9e6b45b4b82b507df6d83e9`  
		Last Modified: Thu, 17 Dec 2020 01:48:06 GMT  
		Size: 14.9 KB (14904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b32778d38f805e0e2a84689dba047adda457098c6f4a0b3aeb51a9e9d3e7f2b`  
		Last Modified: Thu, 17 Dec 2020 01:48:06 GMT  
		Size: 1.6 MB (1649753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506d15aa86681d1812c5696615302d2a50938410c852b6aa0d0680c7baa4589f`  
		Last Modified: Thu, 17 Dec 2020 01:48:06 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f55730e61cf75cdadfaf0682212c74d7a2355e652e0655cc74ba35a4b7cfb4c1`  
		Last Modified: Thu, 17 Dec 2020 01:48:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.9-alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:025f705a0505141d417c4e51c1729ef82ff4b9fbdaf0839e3243775009acd086
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3958429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e00970e77f2ebe2d2ba858b7df67cfb5e150d5eb0355ed729bf89e895376869`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 11 Dec 2020 02:20:33 GMT
ADD file:0e85952ec585d17378d9bb15a94ddc10c3ed8f766f275cf50fb36be1126f35d2 in / 
# Fri, 11 Dec 2020 02:20:34 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 04:44:21 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Fri, 11 Dec 2020 04:44:24 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Fri, 11 Dec 2020 04:44:24 GMT
ENV MEMCACHED_VERSION=1.6.9
# Fri, 11 Dec 2020 04:44:25 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Fri, 11 Dec 2020 04:47:21 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Fri, 11 Dec 2020 04:47:22 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Fri, 11 Dec 2020 04:47:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 11 Dec 2020 04:47:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 04:47:25 GMT
USER memcache
# Fri, 11 Dec 2020 04:47:26 GMT
EXPOSE 11211
# Fri, 11 Dec 2020 04:47:27 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f70c74f2e22556cebd0cbbff78c03d4f0560d76979bf799d67730340a639aa57`  
		Last Modified: Fri, 11 Dec 2020 02:21:18 GMT  
		Size: 2.4 MB (2405692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:768546c6e0d3e4378d243c7cb7e879198125f68127e80959ca72dcec557ff316`  
		Last Modified: Fri, 11 Dec 2020 04:48:04 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca9b4acc3830b3a8d19222da2083d2ad5f1094cc85f0d5c3d23bbc090b6c477`  
		Last Modified: Fri, 11 Dec 2020 04:48:04 GMT  
		Size: 13.8 KB (13828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:884909597bafb82a692dee46723b5658228d7b09a14ffaaac251c369ddcd9f58`  
		Last Modified: Fri, 11 Dec 2020 04:48:05 GMT  
		Size: 1.5 MB (1537241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a64d8e8df54c198e648639cfdf128ad77ba99753933e913b5ab4fad89fc9b0e`  
		Last Modified: Fri, 11 Dec 2020 04:48:04 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e50c30196b75de66eee5631e81459a85a4d771aff5fc75b3310a31e692f04e20`  
		Last Modified: Fri, 11 Dec 2020 04:48:04 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.9-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:d63d8466bfb54fc0fe13ec9c277732f4620146b6021c6f8421281809c61724b0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4424413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fc9075d7b7f039c08144775b94c053c30bf84a069de4706220d6cffd5314a2c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 16 Dec 2020 23:40:26 GMT
ADD file:a4845c3840a3fd0e41e4635a179cce20c81afc6c02e34e3fd5bd2d535698918b in / 
# Wed, 16 Dec 2020 23:40:29 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 01:37:23 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Thu, 17 Dec 2020 01:37:26 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Thu, 17 Dec 2020 01:37:29 GMT
ENV MEMCACHED_VERSION=1.6.9
# Thu, 17 Dec 2020 01:37:32 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Thu, 17 Dec 2020 01:43:55 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Thu, 17 Dec 2020 01:43:55 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 17 Dec 2020 01:43:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 17 Dec 2020 01:43:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 01:43:59 GMT
USER memcache
# Thu, 17 Dec 2020 01:43:59 GMT
EXPOSE 11211
# Thu, 17 Dec 2020 01:44:00 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:159e5727ea618dfe8b08811112e2c51f5bd2b9ae7db9eb214914a65249f70ca0`  
		Last Modified: Wed, 16 Dec 2020 23:41:08 GMT  
		Size: 2.7 MB (2709048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efddf5fc31c997eee1cf28bc1a2b2945bbdc74752b38cdf4c9ec7d85b67bb43d`  
		Last Modified: Thu, 17 Dec 2020 01:44:29 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47319da96c7d47abe996d9884e2cc6614059cbeb4651a55b1691ebb1953a5e61`  
		Last Modified: Thu, 17 Dec 2020 01:44:29 GMT  
		Size: 15.7 KB (15686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a77083b4544bef7ddd2dd0e87b02897b5c406c2789b78da79be60e56e2ff4106`  
		Last Modified: Thu, 17 Dec 2020 01:44:29 GMT  
		Size: 1.7 MB (1698013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63bbe77f7afecd6785a470bf354cc90fa94e44adb990c331ae24d5d6ec6a2448`  
		Last Modified: Thu, 17 Dec 2020 01:44:29 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:475728acf5f3313d53a5de130cbd69dfa27062d365a897a0c4e5be3bf14f1e6c`  
		Last Modified: Thu, 17 Dec 2020 01:44:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.9-alpine` - linux; 386

```console
$ docker pull memcached@sha256:ade825257f6c304561270199626837918c2045e3337064e439b131072bf420cc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4591306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c08ab552727aea8b3fd64b4a6484b1a9f6790fd2d44486228a0b242a27bb268`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 11 Dec 2020 02:01:14 GMT
ADD file:8812e502f26af2dc4efdfb7387f8bf99f2a098b6c95b9f6abf900df2ce74e3da in / 
# Fri, 11 Dec 2020 02:01:14 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 05:39:50 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Fri, 11 Dec 2020 05:39:52 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Fri, 11 Dec 2020 05:39:52 GMT
ENV MEMCACHED_VERSION=1.6.9
# Fri, 11 Dec 2020 05:39:52 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Fri, 11 Dec 2020 05:44:35 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Fri, 11 Dec 2020 05:44:36 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Fri, 11 Dec 2020 05:44:36 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 11 Dec 2020 05:44:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 05:44:37 GMT
USER memcache
# Fri, 11 Dec 2020 05:44:37 GMT
EXPOSE 11211
# Fri, 11 Dec 2020 05:44:37 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b62269920a7a62a905817c7c1b33f33b6e658121e9a054715ff052a23f7de3a0`  
		Last Modified: Fri, 11 Dec 2020 02:01:43 GMT  
		Size: 2.8 MB (2791504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:622762d7c54e6354b4df55c50b95359a408e9dd65b8f00478d406b75a70fc738`  
		Last Modified: Fri, 11 Dec 2020 05:45:13 GMT  
		Size: 1.2 KB (1228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6c16c7dd098acb916cc5dba31b109c3fbbd72f8afd8a27c069787de11d22c19`  
		Last Modified: Fri, 11 Dec 2020 05:45:14 GMT  
		Size: 16.3 KB (16329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eeb5cfc11e39d55a86976c976cebc1498042dfec623c02443c44b58e387e48b`  
		Last Modified: Fri, 11 Dec 2020 05:45:14 GMT  
		Size: 1.8 MB (1781840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28d68462e91b07ebcfee21fbe17d9c131dd46a0a98459fb8a037f7726f2b0d00`  
		Last Modified: Fri, 11 Dec 2020 05:45:13 GMT  
		Size: 284.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29fec6ea0857f0a8736f2ba3c0e920280f2bf9c739355cd857e3db66ed9bc59c`  
		Last Modified: Fri, 11 Dec 2020 05:45:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.9-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:6acd9ca432c36df56ab119467f78ce38ca0d6367960aef01287224b97c3d010f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4571132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4eca59e7708c484618cd0e1184fc494bbee0b97a1a60d7f27686950150f6518`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 11 Dec 2020 03:30:29 GMT
ADD file:9b4b44ee9eaddedc13f114bb55c9abeabceff6abd47f4a660734e431d22fcdce in / 
# Fri, 11 Dec 2020 03:30:32 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 16:15:25 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Fri, 11 Dec 2020 16:15:40 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Fri, 11 Dec 2020 16:15:42 GMT
ENV MEMCACHED_VERSION=1.6.9
# Fri, 11 Dec 2020 16:15:44 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Fri, 11 Dec 2020 16:19:12 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Fri, 11 Dec 2020 16:19:14 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Fri, 11 Dec 2020 16:19:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 11 Dec 2020 16:19:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 16:19:36 GMT
USER memcache
# Fri, 11 Dec 2020 16:19:39 GMT
EXPOSE 11211
# Fri, 11 Dec 2020 16:19:42 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ed596bc4dd0a0c7ff1952005f6cae53a061e1c7998282289586bbfc17a2fd6db`  
		Last Modified: Fri, 11 Dec 2020 03:31:06 GMT  
		Size: 2.8 MB (2803424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb0deb5fb9a1fe630c56c0a2f951e7736fe44505b8a8753a1b94d8d76b336b1`  
		Last Modified: Fri, 11 Dec 2020 16:20:29 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c3d4d573d26b0ed61dcedf75ac24ad38c1feebbe1e76babc2cb89804ab202c`  
		Last Modified: Fri, 11 Dec 2020 16:20:29 GMT  
		Size: 16.3 KB (16320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e4d902164cc3c380c38fb92eebfc73b558508b2246b7f05fb58dce6e6782ac`  
		Last Modified: Fri, 11 Dec 2020 16:20:29 GMT  
		Size: 1.7 MB (1749722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ab874b327a94cf3f3a98efea386979559032cbf0d81c98eac8700b2f121790`  
		Last Modified: Fri, 11 Dec 2020 16:20:29 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c553e6b88120ab98811107dc0646f808e6964794ffb6860efb13aa18526fbf6`  
		Last Modified: Fri, 11 Dec 2020 16:20:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.9-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:59b29e95f04ad4077c9bf81c399bda12695233e400229a06fd97dc0fd7fa10aa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4285134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60592d315caed52aaf7b4ed4e68a49f6705fad0331826b22feb6835668d04069`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 11 Dec 2020 02:09:52 GMT
ADD file:c9395a36a4e03768aabd282eb1f31705cc00181d3147222d9c940eaa5a8fd511 in / 
# Fri, 11 Dec 2020 02:09:53 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 03:40:35 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Fri, 11 Dec 2020 03:40:36 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Fri, 11 Dec 2020 03:40:37 GMT
ENV MEMCACHED_VERSION=1.6.9
# Fri, 11 Dec 2020 03:40:38 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Fri, 11 Dec 2020 03:44:41 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Fri, 11 Dec 2020 03:44:41 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Fri, 11 Dec 2020 03:44:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 11 Dec 2020 03:44:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 03:44:44 GMT
USER memcache
# Fri, 11 Dec 2020 03:44:44 GMT
EXPOSE 11211
# Fri, 11 Dec 2020 03:44:45 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7c2470fe3d16cb70fca0826168095a96838b1322a8cd1502b28284ee8561b491`  
		Last Modified: Fri, 11 Dec 2020 02:10:27 GMT  
		Size: 2.6 MB (2565988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32fcd45bf7121f7a7e805de4c371092cd98580c04cb598614413284ed298e94a`  
		Last Modified: Fri, 11 Dec 2020 03:45:18 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36656d9772d7915b6478a3b431af02133eae46401438d438e9c68e3f24d7758`  
		Last Modified: Fri, 11 Dec 2020 03:45:19 GMT  
		Size: 15.6 KB (15562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a30c3955e5be946b12a1a157b49ac133ba31944622e14f41dc6e5ccb92982a`  
		Last Modified: Fri, 11 Dec 2020 03:45:19 GMT  
		Size: 1.7 MB (1701921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa0b2645fecc2076f3e31bee7d1aef495b5b188dadf4b5efa57c4b678cb28ee5`  
		Last Modified: Fri, 11 Dec 2020 03:45:19 GMT  
		Size: 284.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e33d966fe4e589f2973c3098d9c1f37eb50212c4279c8baa6f0528f4f0d09f`  
		Last Modified: Fri, 11 Dec 2020 03:45:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:1.6-alpine`

```console
$ docker pull memcached@sha256:2078c959f70dfd6053c2309d713022ca5b7995f8b1027288c9b5d933a81bfdb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `memcached:1.6-alpine` - linux; amd64

```console
$ docker pull memcached@sha256:691e70c8483ee0cd2f9634b2a3e2a129f945c25e1c687937f46b9b407d70d11c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4503585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e141bc64c1463eed191cb3ab1adad1e5ddd70cd5f3a94a2ddd71c5d16849fb5b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:06 GMT
ADD file:62a1e09319acb6d1bad91ef1c35aabdc7e5e19883a77f30f1951ccfffc812124 in / 
# Fri, 11 Dec 2020 02:04:07 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 06:19:22 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Fri, 11 Dec 2020 06:19:24 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Fri, 11 Dec 2020 06:19:24 GMT
ENV MEMCACHED_VERSION=1.6.9
# Fri, 11 Dec 2020 06:19:25 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Fri, 11 Dec 2020 06:24:01 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Fri, 11 Dec 2020 06:24:02 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Fri, 11 Dec 2020 06:24:04 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 11 Dec 2020 06:24:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 06:24:04 GMT
USER memcache
# Fri, 11 Dec 2020 06:24:05 GMT
EXPOSE 11211
# Fri, 11 Dec 2020 06:24:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:05e7bc50f07f000e9993ec0d264b9ffcbb9a01a4d69c68f556d25e9811a8f7f4`  
		Last Modified: Fri, 11 Dec 2020 02:04:37 GMT  
		Size: 2.8 MB (2796945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b5d61d52bf8492fedc6398ec81e362de087350385dcd6af525eeaefb9567f48`  
		Last Modified: Fri, 11 Dec 2020 06:24:32 GMT  
		Size: 1.2 KB (1229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90487ba3ac99c5207669e34d25cf1cbde67b59e61ee8a99a7e864a02393a39b`  
		Last Modified: Fri, 11 Dec 2020 06:24:32 GMT  
		Size: 15.3 KB (15298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9907d94cbfb040b78161ad7a4c2d76f515f9bf6a9298013306b8743d2ec14f83`  
		Last Modified: Fri, 11 Dec 2020 06:24:32 GMT  
		Size: 1.7 MB (1689704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f7796e2d1614664de986b74411d12dc4032b5550d7c2d9f0e8e3a1b8699a2e`  
		Last Modified: Fri, 11 Dec 2020 06:24:32 GMT  
		Size: 288.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f9253a3ddb10ef7212753ded436b4cb46964aa53a3e8b1af412be9e1e9e4a41`  
		Last Modified: Fri, 11 Dec 2020 06:24:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6-alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:4d05de82436bd51ed609a745b8ddd01e296692beb5a372dcbdcf0b1f54818d03
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4270486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56e8bda6e6346ca01fa3a313ef7bcfcc696040d48be803f6c16922dedc8deae1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 16 Dec 2020 23:49:43 GMT
ADD file:0a16715e2d0e5811c3c578945d618db0e269847a799340248f9ba8d393c9eec2 in / 
# Wed, 16 Dec 2020 23:49:45 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 01:44:25 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Thu, 17 Dec 2020 01:44:29 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Thu, 17 Dec 2020 01:44:30 GMT
ENV MEMCACHED_VERSION=1.6.9
# Thu, 17 Dec 2020 01:44:31 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Thu, 17 Dec 2020 01:47:40 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Thu, 17 Dec 2020 01:47:41 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 17 Dec 2020 01:47:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 17 Dec 2020 01:47:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 01:47:44 GMT
USER memcache
# Thu, 17 Dec 2020 01:47:45 GMT
EXPOSE 11211
# Thu, 17 Dec 2020 01:47:46 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:93247449aef3c56eb4f7ab7b3fed95743c974b823def6dd86ec84008126e7903`  
		Last Modified: Wed, 16 Dec 2020 23:50:24 GMT  
		Size: 2.6 MB (2604163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cc04af65958529b14246e2401008ef0186d74a33d2aa1b64d5f49633a1ff8f1`  
		Last Modified: Thu, 17 Dec 2020 01:48:06 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08bb28157acd02855bdf031eb7158f2cbb9849a6a9e6b45b4b82b507df6d83e9`  
		Last Modified: Thu, 17 Dec 2020 01:48:06 GMT  
		Size: 14.9 KB (14904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b32778d38f805e0e2a84689dba047adda457098c6f4a0b3aeb51a9e9d3e7f2b`  
		Last Modified: Thu, 17 Dec 2020 01:48:06 GMT  
		Size: 1.6 MB (1649753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506d15aa86681d1812c5696615302d2a50938410c852b6aa0d0680c7baa4589f`  
		Last Modified: Thu, 17 Dec 2020 01:48:06 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f55730e61cf75cdadfaf0682212c74d7a2355e652e0655cc74ba35a4b7cfb4c1`  
		Last Modified: Thu, 17 Dec 2020 01:48:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6-alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:025f705a0505141d417c4e51c1729ef82ff4b9fbdaf0839e3243775009acd086
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3958429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e00970e77f2ebe2d2ba858b7df67cfb5e150d5eb0355ed729bf89e895376869`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 11 Dec 2020 02:20:33 GMT
ADD file:0e85952ec585d17378d9bb15a94ddc10c3ed8f766f275cf50fb36be1126f35d2 in / 
# Fri, 11 Dec 2020 02:20:34 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 04:44:21 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Fri, 11 Dec 2020 04:44:24 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Fri, 11 Dec 2020 04:44:24 GMT
ENV MEMCACHED_VERSION=1.6.9
# Fri, 11 Dec 2020 04:44:25 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Fri, 11 Dec 2020 04:47:21 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Fri, 11 Dec 2020 04:47:22 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Fri, 11 Dec 2020 04:47:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 11 Dec 2020 04:47:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 04:47:25 GMT
USER memcache
# Fri, 11 Dec 2020 04:47:26 GMT
EXPOSE 11211
# Fri, 11 Dec 2020 04:47:27 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f70c74f2e22556cebd0cbbff78c03d4f0560d76979bf799d67730340a639aa57`  
		Last Modified: Fri, 11 Dec 2020 02:21:18 GMT  
		Size: 2.4 MB (2405692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:768546c6e0d3e4378d243c7cb7e879198125f68127e80959ca72dcec557ff316`  
		Last Modified: Fri, 11 Dec 2020 04:48:04 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca9b4acc3830b3a8d19222da2083d2ad5f1094cc85f0d5c3d23bbc090b6c477`  
		Last Modified: Fri, 11 Dec 2020 04:48:04 GMT  
		Size: 13.8 KB (13828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:884909597bafb82a692dee46723b5658228d7b09a14ffaaac251c369ddcd9f58`  
		Last Modified: Fri, 11 Dec 2020 04:48:05 GMT  
		Size: 1.5 MB (1537241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a64d8e8df54c198e648639cfdf128ad77ba99753933e913b5ab4fad89fc9b0e`  
		Last Modified: Fri, 11 Dec 2020 04:48:04 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e50c30196b75de66eee5631e81459a85a4d771aff5fc75b3310a31e692f04e20`  
		Last Modified: Fri, 11 Dec 2020 04:48:04 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:d63d8466bfb54fc0fe13ec9c277732f4620146b6021c6f8421281809c61724b0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4424413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fc9075d7b7f039c08144775b94c053c30bf84a069de4706220d6cffd5314a2c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 16 Dec 2020 23:40:26 GMT
ADD file:a4845c3840a3fd0e41e4635a179cce20c81afc6c02e34e3fd5bd2d535698918b in / 
# Wed, 16 Dec 2020 23:40:29 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 01:37:23 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Thu, 17 Dec 2020 01:37:26 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Thu, 17 Dec 2020 01:37:29 GMT
ENV MEMCACHED_VERSION=1.6.9
# Thu, 17 Dec 2020 01:37:32 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Thu, 17 Dec 2020 01:43:55 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Thu, 17 Dec 2020 01:43:55 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 17 Dec 2020 01:43:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 17 Dec 2020 01:43:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 01:43:59 GMT
USER memcache
# Thu, 17 Dec 2020 01:43:59 GMT
EXPOSE 11211
# Thu, 17 Dec 2020 01:44:00 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:159e5727ea618dfe8b08811112e2c51f5bd2b9ae7db9eb214914a65249f70ca0`  
		Last Modified: Wed, 16 Dec 2020 23:41:08 GMT  
		Size: 2.7 MB (2709048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efddf5fc31c997eee1cf28bc1a2b2945bbdc74752b38cdf4c9ec7d85b67bb43d`  
		Last Modified: Thu, 17 Dec 2020 01:44:29 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47319da96c7d47abe996d9884e2cc6614059cbeb4651a55b1691ebb1953a5e61`  
		Last Modified: Thu, 17 Dec 2020 01:44:29 GMT  
		Size: 15.7 KB (15686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a77083b4544bef7ddd2dd0e87b02897b5c406c2789b78da79be60e56e2ff4106`  
		Last Modified: Thu, 17 Dec 2020 01:44:29 GMT  
		Size: 1.7 MB (1698013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63bbe77f7afecd6785a470bf354cc90fa94e44adb990c331ae24d5d6ec6a2448`  
		Last Modified: Thu, 17 Dec 2020 01:44:29 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:475728acf5f3313d53a5de130cbd69dfa27062d365a897a0c4e5be3bf14f1e6c`  
		Last Modified: Thu, 17 Dec 2020 01:44:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6-alpine` - linux; 386

```console
$ docker pull memcached@sha256:ade825257f6c304561270199626837918c2045e3337064e439b131072bf420cc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4591306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c08ab552727aea8b3fd64b4a6484b1a9f6790fd2d44486228a0b242a27bb268`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 11 Dec 2020 02:01:14 GMT
ADD file:8812e502f26af2dc4efdfb7387f8bf99f2a098b6c95b9f6abf900df2ce74e3da in / 
# Fri, 11 Dec 2020 02:01:14 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 05:39:50 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Fri, 11 Dec 2020 05:39:52 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Fri, 11 Dec 2020 05:39:52 GMT
ENV MEMCACHED_VERSION=1.6.9
# Fri, 11 Dec 2020 05:39:52 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Fri, 11 Dec 2020 05:44:35 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Fri, 11 Dec 2020 05:44:36 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Fri, 11 Dec 2020 05:44:36 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 11 Dec 2020 05:44:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 05:44:37 GMT
USER memcache
# Fri, 11 Dec 2020 05:44:37 GMT
EXPOSE 11211
# Fri, 11 Dec 2020 05:44:37 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b62269920a7a62a905817c7c1b33f33b6e658121e9a054715ff052a23f7de3a0`  
		Last Modified: Fri, 11 Dec 2020 02:01:43 GMT  
		Size: 2.8 MB (2791504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:622762d7c54e6354b4df55c50b95359a408e9dd65b8f00478d406b75a70fc738`  
		Last Modified: Fri, 11 Dec 2020 05:45:13 GMT  
		Size: 1.2 KB (1228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6c16c7dd098acb916cc5dba31b109c3fbbd72f8afd8a27c069787de11d22c19`  
		Last Modified: Fri, 11 Dec 2020 05:45:14 GMT  
		Size: 16.3 KB (16329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eeb5cfc11e39d55a86976c976cebc1498042dfec623c02443c44b58e387e48b`  
		Last Modified: Fri, 11 Dec 2020 05:45:14 GMT  
		Size: 1.8 MB (1781840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28d68462e91b07ebcfee21fbe17d9c131dd46a0a98459fb8a037f7726f2b0d00`  
		Last Modified: Fri, 11 Dec 2020 05:45:13 GMT  
		Size: 284.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29fec6ea0857f0a8736f2ba3c0e920280f2bf9c739355cd857e3db66ed9bc59c`  
		Last Modified: Fri, 11 Dec 2020 05:45:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:6acd9ca432c36df56ab119467f78ce38ca0d6367960aef01287224b97c3d010f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4571132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4eca59e7708c484618cd0e1184fc494bbee0b97a1a60d7f27686950150f6518`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 11 Dec 2020 03:30:29 GMT
ADD file:9b4b44ee9eaddedc13f114bb55c9abeabceff6abd47f4a660734e431d22fcdce in / 
# Fri, 11 Dec 2020 03:30:32 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 16:15:25 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Fri, 11 Dec 2020 16:15:40 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Fri, 11 Dec 2020 16:15:42 GMT
ENV MEMCACHED_VERSION=1.6.9
# Fri, 11 Dec 2020 16:15:44 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Fri, 11 Dec 2020 16:19:12 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Fri, 11 Dec 2020 16:19:14 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Fri, 11 Dec 2020 16:19:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 11 Dec 2020 16:19:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 16:19:36 GMT
USER memcache
# Fri, 11 Dec 2020 16:19:39 GMT
EXPOSE 11211
# Fri, 11 Dec 2020 16:19:42 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ed596bc4dd0a0c7ff1952005f6cae53a061e1c7998282289586bbfc17a2fd6db`  
		Last Modified: Fri, 11 Dec 2020 03:31:06 GMT  
		Size: 2.8 MB (2803424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb0deb5fb9a1fe630c56c0a2f951e7736fe44505b8a8753a1b94d8d76b336b1`  
		Last Modified: Fri, 11 Dec 2020 16:20:29 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c3d4d573d26b0ed61dcedf75ac24ad38c1feebbe1e76babc2cb89804ab202c`  
		Last Modified: Fri, 11 Dec 2020 16:20:29 GMT  
		Size: 16.3 KB (16320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e4d902164cc3c380c38fb92eebfc73b558508b2246b7f05fb58dce6e6782ac`  
		Last Modified: Fri, 11 Dec 2020 16:20:29 GMT  
		Size: 1.7 MB (1749722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ab874b327a94cf3f3a98efea386979559032cbf0d81c98eac8700b2f121790`  
		Last Modified: Fri, 11 Dec 2020 16:20:29 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c553e6b88120ab98811107dc0646f808e6964794ffb6860efb13aa18526fbf6`  
		Last Modified: Fri, 11 Dec 2020 16:20:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:59b29e95f04ad4077c9bf81c399bda12695233e400229a06fd97dc0fd7fa10aa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4285134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60592d315caed52aaf7b4ed4e68a49f6705fad0331826b22feb6835668d04069`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 11 Dec 2020 02:09:52 GMT
ADD file:c9395a36a4e03768aabd282eb1f31705cc00181d3147222d9c940eaa5a8fd511 in / 
# Fri, 11 Dec 2020 02:09:53 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 03:40:35 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Fri, 11 Dec 2020 03:40:36 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Fri, 11 Dec 2020 03:40:37 GMT
ENV MEMCACHED_VERSION=1.6.9
# Fri, 11 Dec 2020 03:40:38 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Fri, 11 Dec 2020 03:44:41 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Fri, 11 Dec 2020 03:44:41 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Fri, 11 Dec 2020 03:44:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 11 Dec 2020 03:44:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 03:44:44 GMT
USER memcache
# Fri, 11 Dec 2020 03:44:44 GMT
EXPOSE 11211
# Fri, 11 Dec 2020 03:44:45 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7c2470fe3d16cb70fca0826168095a96838b1322a8cd1502b28284ee8561b491`  
		Last Modified: Fri, 11 Dec 2020 02:10:27 GMT  
		Size: 2.6 MB (2565988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32fcd45bf7121f7a7e805de4c371092cd98580c04cb598614413284ed298e94a`  
		Last Modified: Fri, 11 Dec 2020 03:45:18 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36656d9772d7915b6478a3b431af02133eae46401438d438e9c68e3f24d7758`  
		Last Modified: Fri, 11 Dec 2020 03:45:19 GMT  
		Size: 15.6 KB (15562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a30c3955e5be946b12a1a157b49ac133ba31944622e14f41dc6e5ccb92982a`  
		Last Modified: Fri, 11 Dec 2020 03:45:19 GMT  
		Size: 1.7 MB (1701921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa0b2645fecc2076f3e31bee7d1aef495b5b188dadf4b5efa57c4b678cb28ee5`  
		Last Modified: Fri, 11 Dec 2020 03:45:19 GMT  
		Size: 284.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e33d966fe4e589f2973c3098d9c1f37eb50212c4279c8baa6f0528f4f0d09f`  
		Last Modified: Fri, 11 Dec 2020 03:45:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:1-alpine`

```console
$ docker pull memcached@sha256:2078c959f70dfd6053c2309d713022ca5b7995f8b1027288c9b5d933a81bfdb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `memcached:1-alpine` - linux; amd64

```console
$ docker pull memcached@sha256:691e70c8483ee0cd2f9634b2a3e2a129f945c25e1c687937f46b9b407d70d11c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4503585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e141bc64c1463eed191cb3ab1adad1e5ddd70cd5f3a94a2ddd71c5d16849fb5b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:06 GMT
ADD file:62a1e09319acb6d1bad91ef1c35aabdc7e5e19883a77f30f1951ccfffc812124 in / 
# Fri, 11 Dec 2020 02:04:07 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 06:19:22 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Fri, 11 Dec 2020 06:19:24 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Fri, 11 Dec 2020 06:19:24 GMT
ENV MEMCACHED_VERSION=1.6.9
# Fri, 11 Dec 2020 06:19:25 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Fri, 11 Dec 2020 06:24:01 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Fri, 11 Dec 2020 06:24:02 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Fri, 11 Dec 2020 06:24:04 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 11 Dec 2020 06:24:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 06:24:04 GMT
USER memcache
# Fri, 11 Dec 2020 06:24:05 GMT
EXPOSE 11211
# Fri, 11 Dec 2020 06:24:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:05e7bc50f07f000e9993ec0d264b9ffcbb9a01a4d69c68f556d25e9811a8f7f4`  
		Last Modified: Fri, 11 Dec 2020 02:04:37 GMT  
		Size: 2.8 MB (2796945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b5d61d52bf8492fedc6398ec81e362de087350385dcd6af525eeaefb9567f48`  
		Last Modified: Fri, 11 Dec 2020 06:24:32 GMT  
		Size: 1.2 KB (1229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90487ba3ac99c5207669e34d25cf1cbde67b59e61ee8a99a7e864a02393a39b`  
		Last Modified: Fri, 11 Dec 2020 06:24:32 GMT  
		Size: 15.3 KB (15298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9907d94cbfb040b78161ad7a4c2d76f515f9bf6a9298013306b8743d2ec14f83`  
		Last Modified: Fri, 11 Dec 2020 06:24:32 GMT  
		Size: 1.7 MB (1689704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f7796e2d1614664de986b74411d12dc4032b5550d7c2d9f0e8e3a1b8699a2e`  
		Last Modified: Fri, 11 Dec 2020 06:24:32 GMT  
		Size: 288.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f9253a3ddb10ef7212753ded436b4cb46964aa53a3e8b1af412be9e1e9e4a41`  
		Last Modified: Fri, 11 Dec 2020 06:24:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:4d05de82436bd51ed609a745b8ddd01e296692beb5a372dcbdcf0b1f54818d03
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4270486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56e8bda6e6346ca01fa3a313ef7bcfcc696040d48be803f6c16922dedc8deae1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 16 Dec 2020 23:49:43 GMT
ADD file:0a16715e2d0e5811c3c578945d618db0e269847a799340248f9ba8d393c9eec2 in / 
# Wed, 16 Dec 2020 23:49:45 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 01:44:25 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Thu, 17 Dec 2020 01:44:29 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Thu, 17 Dec 2020 01:44:30 GMT
ENV MEMCACHED_VERSION=1.6.9
# Thu, 17 Dec 2020 01:44:31 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Thu, 17 Dec 2020 01:47:40 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Thu, 17 Dec 2020 01:47:41 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 17 Dec 2020 01:47:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 17 Dec 2020 01:47:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 01:47:44 GMT
USER memcache
# Thu, 17 Dec 2020 01:47:45 GMT
EXPOSE 11211
# Thu, 17 Dec 2020 01:47:46 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:93247449aef3c56eb4f7ab7b3fed95743c974b823def6dd86ec84008126e7903`  
		Last Modified: Wed, 16 Dec 2020 23:50:24 GMT  
		Size: 2.6 MB (2604163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cc04af65958529b14246e2401008ef0186d74a33d2aa1b64d5f49633a1ff8f1`  
		Last Modified: Thu, 17 Dec 2020 01:48:06 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08bb28157acd02855bdf031eb7158f2cbb9849a6a9e6b45b4b82b507df6d83e9`  
		Last Modified: Thu, 17 Dec 2020 01:48:06 GMT  
		Size: 14.9 KB (14904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b32778d38f805e0e2a84689dba047adda457098c6f4a0b3aeb51a9e9d3e7f2b`  
		Last Modified: Thu, 17 Dec 2020 01:48:06 GMT  
		Size: 1.6 MB (1649753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506d15aa86681d1812c5696615302d2a50938410c852b6aa0d0680c7baa4589f`  
		Last Modified: Thu, 17 Dec 2020 01:48:06 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f55730e61cf75cdadfaf0682212c74d7a2355e652e0655cc74ba35a4b7cfb4c1`  
		Last Modified: Thu, 17 Dec 2020 01:48:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:025f705a0505141d417c4e51c1729ef82ff4b9fbdaf0839e3243775009acd086
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3958429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e00970e77f2ebe2d2ba858b7df67cfb5e150d5eb0355ed729bf89e895376869`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 11 Dec 2020 02:20:33 GMT
ADD file:0e85952ec585d17378d9bb15a94ddc10c3ed8f766f275cf50fb36be1126f35d2 in / 
# Fri, 11 Dec 2020 02:20:34 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 04:44:21 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Fri, 11 Dec 2020 04:44:24 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Fri, 11 Dec 2020 04:44:24 GMT
ENV MEMCACHED_VERSION=1.6.9
# Fri, 11 Dec 2020 04:44:25 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Fri, 11 Dec 2020 04:47:21 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Fri, 11 Dec 2020 04:47:22 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Fri, 11 Dec 2020 04:47:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 11 Dec 2020 04:47:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 04:47:25 GMT
USER memcache
# Fri, 11 Dec 2020 04:47:26 GMT
EXPOSE 11211
# Fri, 11 Dec 2020 04:47:27 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f70c74f2e22556cebd0cbbff78c03d4f0560d76979bf799d67730340a639aa57`  
		Last Modified: Fri, 11 Dec 2020 02:21:18 GMT  
		Size: 2.4 MB (2405692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:768546c6e0d3e4378d243c7cb7e879198125f68127e80959ca72dcec557ff316`  
		Last Modified: Fri, 11 Dec 2020 04:48:04 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca9b4acc3830b3a8d19222da2083d2ad5f1094cc85f0d5c3d23bbc090b6c477`  
		Last Modified: Fri, 11 Dec 2020 04:48:04 GMT  
		Size: 13.8 KB (13828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:884909597bafb82a692dee46723b5658228d7b09a14ffaaac251c369ddcd9f58`  
		Last Modified: Fri, 11 Dec 2020 04:48:05 GMT  
		Size: 1.5 MB (1537241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a64d8e8df54c198e648639cfdf128ad77ba99753933e913b5ab4fad89fc9b0e`  
		Last Modified: Fri, 11 Dec 2020 04:48:04 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e50c30196b75de66eee5631e81459a85a4d771aff5fc75b3310a31e692f04e20`  
		Last Modified: Fri, 11 Dec 2020 04:48:04 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:d63d8466bfb54fc0fe13ec9c277732f4620146b6021c6f8421281809c61724b0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4424413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fc9075d7b7f039c08144775b94c053c30bf84a069de4706220d6cffd5314a2c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 16 Dec 2020 23:40:26 GMT
ADD file:a4845c3840a3fd0e41e4635a179cce20c81afc6c02e34e3fd5bd2d535698918b in / 
# Wed, 16 Dec 2020 23:40:29 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 01:37:23 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Thu, 17 Dec 2020 01:37:26 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Thu, 17 Dec 2020 01:37:29 GMT
ENV MEMCACHED_VERSION=1.6.9
# Thu, 17 Dec 2020 01:37:32 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Thu, 17 Dec 2020 01:43:55 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Thu, 17 Dec 2020 01:43:55 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 17 Dec 2020 01:43:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 17 Dec 2020 01:43:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 01:43:59 GMT
USER memcache
# Thu, 17 Dec 2020 01:43:59 GMT
EXPOSE 11211
# Thu, 17 Dec 2020 01:44:00 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:159e5727ea618dfe8b08811112e2c51f5bd2b9ae7db9eb214914a65249f70ca0`  
		Last Modified: Wed, 16 Dec 2020 23:41:08 GMT  
		Size: 2.7 MB (2709048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efddf5fc31c997eee1cf28bc1a2b2945bbdc74752b38cdf4c9ec7d85b67bb43d`  
		Last Modified: Thu, 17 Dec 2020 01:44:29 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47319da96c7d47abe996d9884e2cc6614059cbeb4651a55b1691ebb1953a5e61`  
		Last Modified: Thu, 17 Dec 2020 01:44:29 GMT  
		Size: 15.7 KB (15686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a77083b4544bef7ddd2dd0e87b02897b5c406c2789b78da79be60e56e2ff4106`  
		Last Modified: Thu, 17 Dec 2020 01:44:29 GMT  
		Size: 1.7 MB (1698013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63bbe77f7afecd6785a470bf354cc90fa94e44adb990c331ae24d5d6ec6a2448`  
		Last Modified: Thu, 17 Dec 2020 01:44:29 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:475728acf5f3313d53a5de130cbd69dfa27062d365a897a0c4e5be3bf14f1e6c`  
		Last Modified: Thu, 17 Dec 2020 01:44:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine` - linux; 386

```console
$ docker pull memcached@sha256:ade825257f6c304561270199626837918c2045e3337064e439b131072bf420cc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4591306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c08ab552727aea8b3fd64b4a6484b1a9f6790fd2d44486228a0b242a27bb268`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 11 Dec 2020 02:01:14 GMT
ADD file:8812e502f26af2dc4efdfb7387f8bf99f2a098b6c95b9f6abf900df2ce74e3da in / 
# Fri, 11 Dec 2020 02:01:14 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 05:39:50 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Fri, 11 Dec 2020 05:39:52 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Fri, 11 Dec 2020 05:39:52 GMT
ENV MEMCACHED_VERSION=1.6.9
# Fri, 11 Dec 2020 05:39:52 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Fri, 11 Dec 2020 05:44:35 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Fri, 11 Dec 2020 05:44:36 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Fri, 11 Dec 2020 05:44:36 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 11 Dec 2020 05:44:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 05:44:37 GMT
USER memcache
# Fri, 11 Dec 2020 05:44:37 GMT
EXPOSE 11211
# Fri, 11 Dec 2020 05:44:37 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b62269920a7a62a905817c7c1b33f33b6e658121e9a054715ff052a23f7de3a0`  
		Last Modified: Fri, 11 Dec 2020 02:01:43 GMT  
		Size: 2.8 MB (2791504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:622762d7c54e6354b4df55c50b95359a408e9dd65b8f00478d406b75a70fc738`  
		Last Modified: Fri, 11 Dec 2020 05:45:13 GMT  
		Size: 1.2 KB (1228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6c16c7dd098acb916cc5dba31b109c3fbbd72f8afd8a27c069787de11d22c19`  
		Last Modified: Fri, 11 Dec 2020 05:45:14 GMT  
		Size: 16.3 KB (16329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eeb5cfc11e39d55a86976c976cebc1498042dfec623c02443c44b58e387e48b`  
		Last Modified: Fri, 11 Dec 2020 05:45:14 GMT  
		Size: 1.8 MB (1781840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28d68462e91b07ebcfee21fbe17d9c131dd46a0a98459fb8a037f7726f2b0d00`  
		Last Modified: Fri, 11 Dec 2020 05:45:13 GMT  
		Size: 284.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29fec6ea0857f0a8736f2ba3c0e920280f2bf9c739355cd857e3db66ed9bc59c`  
		Last Modified: Fri, 11 Dec 2020 05:45:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:6acd9ca432c36df56ab119467f78ce38ca0d6367960aef01287224b97c3d010f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4571132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4eca59e7708c484618cd0e1184fc494bbee0b97a1a60d7f27686950150f6518`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 11 Dec 2020 03:30:29 GMT
ADD file:9b4b44ee9eaddedc13f114bb55c9abeabceff6abd47f4a660734e431d22fcdce in / 
# Fri, 11 Dec 2020 03:30:32 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 16:15:25 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Fri, 11 Dec 2020 16:15:40 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Fri, 11 Dec 2020 16:15:42 GMT
ENV MEMCACHED_VERSION=1.6.9
# Fri, 11 Dec 2020 16:15:44 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Fri, 11 Dec 2020 16:19:12 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Fri, 11 Dec 2020 16:19:14 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Fri, 11 Dec 2020 16:19:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 11 Dec 2020 16:19:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 16:19:36 GMT
USER memcache
# Fri, 11 Dec 2020 16:19:39 GMT
EXPOSE 11211
# Fri, 11 Dec 2020 16:19:42 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ed596bc4dd0a0c7ff1952005f6cae53a061e1c7998282289586bbfc17a2fd6db`  
		Last Modified: Fri, 11 Dec 2020 03:31:06 GMT  
		Size: 2.8 MB (2803424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb0deb5fb9a1fe630c56c0a2f951e7736fe44505b8a8753a1b94d8d76b336b1`  
		Last Modified: Fri, 11 Dec 2020 16:20:29 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c3d4d573d26b0ed61dcedf75ac24ad38c1feebbe1e76babc2cb89804ab202c`  
		Last Modified: Fri, 11 Dec 2020 16:20:29 GMT  
		Size: 16.3 KB (16320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e4d902164cc3c380c38fb92eebfc73b558508b2246b7f05fb58dce6e6782ac`  
		Last Modified: Fri, 11 Dec 2020 16:20:29 GMT  
		Size: 1.7 MB (1749722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ab874b327a94cf3f3a98efea386979559032cbf0d81c98eac8700b2f121790`  
		Last Modified: Fri, 11 Dec 2020 16:20:29 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c553e6b88120ab98811107dc0646f808e6964794ffb6860efb13aa18526fbf6`  
		Last Modified: Fri, 11 Dec 2020 16:20:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:59b29e95f04ad4077c9bf81c399bda12695233e400229a06fd97dc0fd7fa10aa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4285134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60592d315caed52aaf7b4ed4e68a49f6705fad0331826b22feb6835668d04069`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 11 Dec 2020 02:09:52 GMT
ADD file:c9395a36a4e03768aabd282eb1f31705cc00181d3147222d9c940eaa5a8fd511 in / 
# Fri, 11 Dec 2020 02:09:53 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 03:40:35 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Fri, 11 Dec 2020 03:40:36 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Fri, 11 Dec 2020 03:40:37 GMT
ENV MEMCACHED_VERSION=1.6.9
# Fri, 11 Dec 2020 03:40:38 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Fri, 11 Dec 2020 03:44:41 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Fri, 11 Dec 2020 03:44:41 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Fri, 11 Dec 2020 03:44:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 11 Dec 2020 03:44:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 03:44:44 GMT
USER memcache
# Fri, 11 Dec 2020 03:44:44 GMT
EXPOSE 11211
# Fri, 11 Dec 2020 03:44:45 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7c2470fe3d16cb70fca0826168095a96838b1322a8cd1502b28284ee8561b491`  
		Last Modified: Fri, 11 Dec 2020 02:10:27 GMT  
		Size: 2.6 MB (2565988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32fcd45bf7121f7a7e805de4c371092cd98580c04cb598614413284ed298e94a`  
		Last Modified: Fri, 11 Dec 2020 03:45:18 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36656d9772d7915b6478a3b431af02133eae46401438d438e9c68e3f24d7758`  
		Last Modified: Fri, 11 Dec 2020 03:45:19 GMT  
		Size: 15.6 KB (15562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a30c3955e5be946b12a1a157b49ac133ba31944622e14f41dc6e5ccb92982a`  
		Last Modified: Fri, 11 Dec 2020 03:45:19 GMT  
		Size: 1.7 MB (1701921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa0b2645fecc2076f3e31bee7d1aef495b5b188dadf4b5efa57c4b678cb28ee5`  
		Last Modified: Fri, 11 Dec 2020 03:45:19 GMT  
		Size: 284.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e33d966fe4e589f2973c3098d9c1f37eb50212c4279c8baa6f0528f4f0d09f`  
		Last Modified: Fri, 11 Dec 2020 03:45:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:alpine`

```console
$ docker pull memcached@sha256:2078c959f70dfd6053c2309d713022ca5b7995f8b1027288c9b5d933a81bfdb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `memcached:alpine` - linux; amd64

```console
$ docker pull memcached@sha256:691e70c8483ee0cd2f9634b2a3e2a129f945c25e1c687937f46b9b407d70d11c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4503585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e141bc64c1463eed191cb3ab1adad1e5ddd70cd5f3a94a2ddd71c5d16849fb5b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:06 GMT
ADD file:62a1e09319acb6d1bad91ef1c35aabdc7e5e19883a77f30f1951ccfffc812124 in / 
# Fri, 11 Dec 2020 02:04:07 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 06:19:22 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Fri, 11 Dec 2020 06:19:24 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Fri, 11 Dec 2020 06:19:24 GMT
ENV MEMCACHED_VERSION=1.6.9
# Fri, 11 Dec 2020 06:19:25 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Fri, 11 Dec 2020 06:24:01 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Fri, 11 Dec 2020 06:24:02 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Fri, 11 Dec 2020 06:24:04 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 11 Dec 2020 06:24:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 06:24:04 GMT
USER memcache
# Fri, 11 Dec 2020 06:24:05 GMT
EXPOSE 11211
# Fri, 11 Dec 2020 06:24:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:05e7bc50f07f000e9993ec0d264b9ffcbb9a01a4d69c68f556d25e9811a8f7f4`  
		Last Modified: Fri, 11 Dec 2020 02:04:37 GMT  
		Size: 2.8 MB (2796945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b5d61d52bf8492fedc6398ec81e362de087350385dcd6af525eeaefb9567f48`  
		Last Modified: Fri, 11 Dec 2020 06:24:32 GMT  
		Size: 1.2 KB (1229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90487ba3ac99c5207669e34d25cf1cbde67b59e61ee8a99a7e864a02393a39b`  
		Last Modified: Fri, 11 Dec 2020 06:24:32 GMT  
		Size: 15.3 KB (15298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9907d94cbfb040b78161ad7a4c2d76f515f9bf6a9298013306b8743d2ec14f83`  
		Last Modified: Fri, 11 Dec 2020 06:24:32 GMT  
		Size: 1.7 MB (1689704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f7796e2d1614664de986b74411d12dc4032b5550d7c2d9f0e8e3a1b8699a2e`  
		Last Modified: Fri, 11 Dec 2020 06:24:32 GMT  
		Size: 288.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f9253a3ddb10ef7212753ded436b4cb46964aa53a3e8b1af412be9e1e9e4a41`  
		Last Modified: Fri, 11 Dec 2020 06:24:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:4d05de82436bd51ed609a745b8ddd01e296692beb5a372dcbdcf0b1f54818d03
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4270486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56e8bda6e6346ca01fa3a313ef7bcfcc696040d48be803f6c16922dedc8deae1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 16 Dec 2020 23:49:43 GMT
ADD file:0a16715e2d0e5811c3c578945d618db0e269847a799340248f9ba8d393c9eec2 in / 
# Wed, 16 Dec 2020 23:49:45 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 01:44:25 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Thu, 17 Dec 2020 01:44:29 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Thu, 17 Dec 2020 01:44:30 GMT
ENV MEMCACHED_VERSION=1.6.9
# Thu, 17 Dec 2020 01:44:31 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Thu, 17 Dec 2020 01:47:40 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Thu, 17 Dec 2020 01:47:41 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 17 Dec 2020 01:47:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 17 Dec 2020 01:47:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 01:47:44 GMT
USER memcache
# Thu, 17 Dec 2020 01:47:45 GMT
EXPOSE 11211
# Thu, 17 Dec 2020 01:47:46 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:93247449aef3c56eb4f7ab7b3fed95743c974b823def6dd86ec84008126e7903`  
		Last Modified: Wed, 16 Dec 2020 23:50:24 GMT  
		Size: 2.6 MB (2604163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cc04af65958529b14246e2401008ef0186d74a33d2aa1b64d5f49633a1ff8f1`  
		Last Modified: Thu, 17 Dec 2020 01:48:06 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08bb28157acd02855bdf031eb7158f2cbb9849a6a9e6b45b4b82b507df6d83e9`  
		Last Modified: Thu, 17 Dec 2020 01:48:06 GMT  
		Size: 14.9 KB (14904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b32778d38f805e0e2a84689dba047adda457098c6f4a0b3aeb51a9e9d3e7f2b`  
		Last Modified: Thu, 17 Dec 2020 01:48:06 GMT  
		Size: 1.6 MB (1649753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506d15aa86681d1812c5696615302d2a50938410c852b6aa0d0680c7baa4589f`  
		Last Modified: Thu, 17 Dec 2020 01:48:06 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f55730e61cf75cdadfaf0682212c74d7a2355e652e0655cc74ba35a4b7cfb4c1`  
		Last Modified: Thu, 17 Dec 2020 01:48:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:025f705a0505141d417c4e51c1729ef82ff4b9fbdaf0839e3243775009acd086
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3958429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e00970e77f2ebe2d2ba858b7df67cfb5e150d5eb0355ed729bf89e895376869`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 11 Dec 2020 02:20:33 GMT
ADD file:0e85952ec585d17378d9bb15a94ddc10c3ed8f766f275cf50fb36be1126f35d2 in / 
# Fri, 11 Dec 2020 02:20:34 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 04:44:21 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Fri, 11 Dec 2020 04:44:24 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Fri, 11 Dec 2020 04:44:24 GMT
ENV MEMCACHED_VERSION=1.6.9
# Fri, 11 Dec 2020 04:44:25 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Fri, 11 Dec 2020 04:47:21 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Fri, 11 Dec 2020 04:47:22 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Fri, 11 Dec 2020 04:47:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 11 Dec 2020 04:47:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 04:47:25 GMT
USER memcache
# Fri, 11 Dec 2020 04:47:26 GMT
EXPOSE 11211
# Fri, 11 Dec 2020 04:47:27 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f70c74f2e22556cebd0cbbff78c03d4f0560d76979bf799d67730340a639aa57`  
		Last Modified: Fri, 11 Dec 2020 02:21:18 GMT  
		Size: 2.4 MB (2405692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:768546c6e0d3e4378d243c7cb7e879198125f68127e80959ca72dcec557ff316`  
		Last Modified: Fri, 11 Dec 2020 04:48:04 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca9b4acc3830b3a8d19222da2083d2ad5f1094cc85f0d5c3d23bbc090b6c477`  
		Last Modified: Fri, 11 Dec 2020 04:48:04 GMT  
		Size: 13.8 KB (13828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:884909597bafb82a692dee46723b5658228d7b09a14ffaaac251c369ddcd9f58`  
		Last Modified: Fri, 11 Dec 2020 04:48:05 GMT  
		Size: 1.5 MB (1537241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a64d8e8df54c198e648639cfdf128ad77ba99753933e913b5ab4fad89fc9b0e`  
		Last Modified: Fri, 11 Dec 2020 04:48:04 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e50c30196b75de66eee5631e81459a85a4d771aff5fc75b3310a31e692f04e20`  
		Last Modified: Fri, 11 Dec 2020 04:48:04 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:d63d8466bfb54fc0fe13ec9c277732f4620146b6021c6f8421281809c61724b0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4424413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fc9075d7b7f039c08144775b94c053c30bf84a069de4706220d6cffd5314a2c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 16 Dec 2020 23:40:26 GMT
ADD file:a4845c3840a3fd0e41e4635a179cce20c81afc6c02e34e3fd5bd2d535698918b in / 
# Wed, 16 Dec 2020 23:40:29 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 01:37:23 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Thu, 17 Dec 2020 01:37:26 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Thu, 17 Dec 2020 01:37:29 GMT
ENV MEMCACHED_VERSION=1.6.9
# Thu, 17 Dec 2020 01:37:32 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Thu, 17 Dec 2020 01:43:55 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Thu, 17 Dec 2020 01:43:55 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 17 Dec 2020 01:43:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 17 Dec 2020 01:43:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 01:43:59 GMT
USER memcache
# Thu, 17 Dec 2020 01:43:59 GMT
EXPOSE 11211
# Thu, 17 Dec 2020 01:44:00 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:159e5727ea618dfe8b08811112e2c51f5bd2b9ae7db9eb214914a65249f70ca0`  
		Last Modified: Wed, 16 Dec 2020 23:41:08 GMT  
		Size: 2.7 MB (2709048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efddf5fc31c997eee1cf28bc1a2b2945bbdc74752b38cdf4c9ec7d85b67bb43d`  
		Last Modified: Thu, 17 Dec 2020 01:44:29 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47319da96c7d47abe996d9884e2cc6614059cbeb4651a55b1691ebb1953a5e61`  
		Last Modified: Thu, 17 Dec 2020 01:44:29 GMT  
		Size: 15.7 KB (15686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a77083b4544bef7ddd2dd0e87b02897b5c406c2789b78da79be60e56e2ff4106`  
		Last Modified: Thu, 17 Dec 2020 01:44:29 GMT  
		Size: 1.7 MB (1698013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63bbe77f7afecd6785a470bf354cc90fa94e44adb990c331ae24d5d6ec6a2448`  
		Last Modified: Thu, 17 Dec 2020 01:44:29 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:475728acf5f3313d53a5de130cbd69dfa27062d365a897a0c4e5be3bf14f1e6c`  
		Last Modified: Thu, 17 Dec 2020 01:44:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:alpine` - linux; 386

```console
$ docker pull memcached@sha256:ade825257f6c304561270199626837918c2045e3337064e439b131072bf420cc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4591306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c08ab552727aea8b3fd64b4a6484b1a9f6790fd2d44486228a0b242a27bb268`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 11 Dec 2020 02:01:14 GMT
ADD file:8812e502f26af2dc4efdfb7387f8bf99f2a098b6c95b9f6abf900df2ce74e3da in / 
# Fri, 11 Dec 2020 02:01:14 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 05:39:50 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Fri, 11 Dec 2020 05:39:52 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Fri, 11 Dec 2020 05:39:52 GMT
ENV MEMCACHED_VERSION=1.6.9
# Fri, 11 Dec 2020 05:39:52 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Fri, 11 Dec 2020 05:44:35 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Fri, 11 Dec 2020 05:44:36 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Fri, 11 Dec 2020 05:44:36 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 11 Dec 2020 05:44:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 05:44:37 GMT
USER memcache
# Fri, 11 Dec 2020 05:44:37 GMT
EXPOSE 11211
# Fri, 11 Dec 2020 05:44:37 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b62269920a7a62a905817c7c1b33f33b6e658121e9a054715ff052a23f7de3a0`  
		Last Modified: Fri, 11 Dec 2020 02:01:43 GMT  
		Size: 2.8 MB (2791504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:622762d7c54e6354b4df55c50b95359a408e9dd65b8f00478d406b75a70fc738`  
		Last Modified: Fri, 11 Dec 2020 05:45:13 GMT  
		Size: 1.2 KB (1228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6c16c7dd098acb916cc5dba31b109c3fbbd72f8afd8a27c069787de11d22c19`  
		Last Modified: Fri, 11 Dec 2020 05:45:14 GMT  
		Size: 16.3 KB (16329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eeb5cfc11e39d55a86976c976cebc1498042dfec623c02443c44b58e387e48b`  
		Last Modified: Fri, 11 Dec 2020 05:45:14 GMT  
		Size: 1.8 MB (1781840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28d68462e91b07ebcfee21fbe17d9c131dd46a0a98459fb8a037f7726f2b0d00`  
		Last Modified: Fri, 11 Dec 2020 05:45:13 GMT  
		Size: 284.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29fec6ea0857f0a8736f2ba3c0e920280f2bf9c739355cd857e3db66ed9bc59c`  
		Last Modified: Fri, 11 Dec 2020 05:45:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:6acd9ca432c36df56ab119467f78ce38ca0d6367960aef01287224b97c3d010f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4571132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4eca59e7708c484618cd0e1184fc494bbee0b97a1a60d7f27686950150f6518`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 11 Dec 2020 03:30:29 GMT
ADD file:9b4b44ee9eaddedc13f114bb55c9abeabceff6abd47f4a660734e431d22fcdce in / 
# Fri, 11 Dec 2020 03:30:32 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 16:15:25 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Fri, 11 Dec 2020 16:15:40 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Fri, 11 Dec 2020 16:15:42 GMT
ENV MEMCACHED_VERSION=1.6.9
# Fri, 11 Dec 2020 16:15:44 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Fri, 11 Dec 2020 16:19:12 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Fri, 11 Dec 2020 16:19:14 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Fri, 11 Dec 2020 16:19:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 11 Dec 2020 16:19:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 16:19:36 GMT
USER memcache
# Fri, 11 Dec 2020 16:19:39 GMT
EXPOSE 11211
# Fri, 11 Dec 2020 16:19:42 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ed596bc4dd0a0c7ff1952005f6cae53a061e1c7998282289586bbfc17a2fd6db`  
		Last Modified: Fri, 11 Dec 2020 03:31:06 GMT  
		Size: 2.8 MB (2803424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb0deb5fb9a1fe630c56c0a2f951e7736fe44505b8a8753a1b94d8d76b336b1`  
		Last Modified: Fri, 11 Dec 2020 16:20:29 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c3d4d573d26b0ed61dcedf75ac24ad38c1feebbe1e76babc2cb89804ab202c`  
		Last Modified: Fri, 11 Dec 2020 16:20:29 GMT  
		Size: 16.3 KB (16320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e4d902164cc3c380c38fb92eebfc73b558508b2246b7f05fb58dce6e6782ac`  
		Last Modified: Fri, 11 Dec 2020 16:20:29 GMT  
		Size: 1.7 MB (1749722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ab874b327a94cf3f3a98efea386979559032cbf0d81c98eac8700b2f121790`  
		Last Modified: Fri, 11 Dec 2020 16:20:29 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c553e6b88120ab98811107dc0646f808e6964794ffb6860efb13aa18526fbf6`  
		Last Modified: Fri, 11 Dec 2020 16:20:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:alpine` - linux; s390x

```console
$ docker pull memcached@sha256:59b29e95f04ad4077c9bf81c399bda12695233e400229a06fd97dc0fd7fa10aa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4285134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60592d315caed52aaf7b4ed4e68a49f6705fad0331826b22feb6835668d04069`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 11 Dec 2020 02:09:52 GMT
ADD file:c9395a36a4e03768aabd282eb1f31705cc00181d3147222d9c940eaa5a8fd511 in / 
# Fri, 11 Dec 2020 02:09:53 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 03:40:35 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Fri, 11 Dec 2020 03:40:36 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Fri, 11 Dec 2020 03:40:37 GMT
ENV MEMCACHED_VERSION=1.6.9
# Fri, 11 Dec 2020 03:40:38 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Fri, 11 Dec 2020 03:44:41 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Fri, 11 Dec 2020 03:44:41 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Fri, 11 Dec 2020 03:44:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 11 Dec 2020 03:44:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 03:44:44 GMT
USER memcache
# Fri, 11 Dec 2020 03:44:44 GMT
EXPOSE 11211
# Fri, 11 Dec 2020 03:44:45 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7c2470fe3d16cb70fca0826168095a96838b1322a8cd1502b28284ee8561b491`  
		Last Modified: Fri, 11 Dec 2020 02:10:27 GMT  
		Size: 2.6 MB (2565988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32fcd45bf7121f7a7e805de4c371092cd98580c04cb598614413284ed298e94a`  
		Last Modified: Fri, 11 Dec 2020 03:45:18 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36656d9772d7915b6478a3b431af02133eae46401438d438e9c68e3f24d7758`  
		Last Modified: Fri, 11 Dec 2020 03:45:19 GMT  
		Size: 15.6 KB (15562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a30c3955e5be946b12a1a157b49ac133ba31944622e14f41dc6e5ccb92982a`  
		Last Modified: Fri, 11 Dec 2020 03:45:19 GMT  
		Size: 1.7 MB (1701921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa0b2645fecc2076f3e31bee7d1aef495b5b188dadf4b5efa57c4b678cb28ee5`  
		Last Modified: Fri, 11 Dec 2020 03:45:19 GMT  
		Size: 284.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e33d966fe4e589f2973c3098d9c1f37eb50212c4279c8baa6f0528f4f0d09f`  
		Last Modified: Fri, 11 Dec 2020 03:45:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:latest`

```console
$ docker pull memcached@sha256:944f6eb53be39dfcb895ab110d685e4f0320ffa00b8a1c0fe35aeb52f4f89d30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `memcached:latest` - linux; amd64

```console
$ docker pull memcached@sha256:6d78552afa63c897afdb38ac829e12f04779ed8c59b7caaa23371e00f57b70fb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 MB (30507788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dac5d0dc8aa45ddc209b926c202ff526cee0efba6582686c8d6c0dcd85f00eaa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 11 Dec 2020 02:06:10 GMT
ADD file:3a7bff4e139bcacc5831fd70a035c130a91b5da001dd91c08b2acd635c7064e8 in / 
# Fri, 11 Dec 2020 02:06:10 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 06:14:16 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Fri, 11 Dec 2020 06:14:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 06:14:21 GMT
ENV MEMCACHED_VERSION=1.6.9
# Fri, 11 Dec 2020 06:14:21 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Fri, 11 Dec 2020 06:19:00 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Fri, 11 Dec 2020 06:19:00 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Fri, 11 Dec 2020 06:19:02 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 11 Dec 2020 06:19:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 06:19:02 GMT
USER memcache
# Fri, 11 Dec 2020 06:19:03 GMT
EXPOSE 11211
# Fri, 11 Dec 2020 06:19:03 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6ec7b7d162b24bd6df88abde89ceb6d7bbc2be927f025c9dd061af2b0c328cfe`  
		Last Modified: Fri, 11 Dec 2020 02:12:26 GMT  
		Size: 27.1 MB (27099295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9818b92b6967ba1cd3b0f1e2d737b06a5c35c86f33459aabaffc428f24e645b1`  
		Last Modified: Fri, 11 Dec 2020 06:24:23 GMT  
		Size: 5.0 KB (4984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9544667d8552cce305a40b1b48e6b093e78ea017033e55711a59b5c37c53394`  
		Last Modified: Fri, 11 Dec 2020 06:24:23 GMT  
		Size: 2.2 MB (2196778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b877c55f6d97a0b40d741a747c9b118c51bf1163b613bae389a7364ce7e24222`  
		Last Modified: Fri, 11 Dec 2020 06:24:23 GMT  
		Size: 1.2 MB (1206324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8facb17105d37c092d0638d397ff7764c35b746327da272f54040fa1f90ac98c`  
		Last Modified: Fri, 11 Dec 2020 06:24:22 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee20652cffd7b48ba83f645a010a98c20af2035fc94be68981de899035dc657b`  
		Last Modified: Fri, 11 Dec 2020 06:24:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:latest` - linux; arm variant v5

```console
$ docker pull memcached@sha256:0373c46dd337fbf5f8a2c3577436549a0100b721e5ce04c418d516a328f43f82
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.9 MB (27925021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddff2df6aa17cc7f39472a8f3aa245748cb771b7c0224dd869a8f6ca56828b2a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:49 GMT
ADD file:58ebb3ffaf26d9b7621efba5f109ae9d22832f2f22865cda36604b138cbdb7b8 in / 
# Fri, 11 Dec 2020 02:04:56 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 03:36:36 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Fri, 11 Dec 2020 03:36:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 03:36:50 GMT
ENV MEMCACHED_VERSION=1.6.9
# Fri, 11 Dec 2020 03:36:52 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Fri, 11 Dec 2020 03:40:48 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Fri, 11 Dec 2020 03:40:49 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Fri, 11 Dec 2020 03:40:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 11 Dec 2020 03:40:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 03:40:55 GMT
USER memcache
# Fri, 11 Dec 2020 03:40:56 GMT
EXPOSE 11211
# Fri, 11 Dec 2020 03:40:58 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8cbd1f790d64c77fcac6c9dbfe4d4c82f0365de9438f1a42b0560dc88f9e6a55`  
		Last Modified: Fri, 11 Dec 2020 02:14:44 GMT  
		Size: 24.8 MB (24843461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:803513e868412453cb2bdaa71c148eab32e8f4cfaee3543153975947f87b661f`  
		Last Modified: Fri, 11 Dec 2020 03:41:20 GMT  
		Size: 4.9 KB (4893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59c7cf3dbc3c0b485c43489bcda8bbd0193303b2647fad83d7805e80e1f6941`  
		Last Modified: Fri, 11 Dec 2020 03:41:21 GMT  
		Size: 1.9 MB (1897145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98bb531a4f2242979d0549a74f72a40522c6b4d74e4243503c995916b19ad2db`  
		Last Modified: Fri, 11 Dec 2020 03:41:20 GMT  
		Size: 1.2 MB (1179116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:678b76c238901201d213d9b7db70aa329013315d456d5443f32c905426f99799`  
		Last Modified: Fri, 11 Dec 2020 03:41:20 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0151320cb9bcff65b1aace9cea43dcfdd6c3e82ac7c93be4c62abe843d6499cc`  
		Last Modified: Fri, 11 Dec 2020 03:41:20 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:latest` - linux; arm variant v7

```console
$ docker pull memcached@sha256:7731cf0112d45e7b8c852237c66a7f46ca0e185320094e2bacc4ac17fb00b308
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25674187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81ab97c7b1a8af34be252318deb461a0f1a2e4ca023041276e9ad4a03cdfaec2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 11 Dec 2020 02:23:37 GMT
ADD file:75ca842ac2d6e9f6617bb3df280af1e4c9619c9805fd5e00c1c3d6b8b4e3d802 in / 
# Fri, 11 Dec 2020 02:23:39 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 04:40:02 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Fri, 11 Dec 2020 04:40:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 04:40:20 GMT
ENV MEMCACHED_VERSION=1.6.9
# Fri, 11 Dec 2020 04:40:22 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Fri, 11 Dec 2020 04:43:59 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Fri, 11 Dec 2020 04:44:00 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Fri, 11 Dec 2020 04:44:02 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 11 Dec 2020 04:44:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 04:44:04 GMT
USER memcache
# Fri, 11 Dec 2020 04:44:05 GMT
EXPOSE 11211
# Fri, 11 Dec 2020 04:44:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c06905228d4fc5a5c840a70e2e6ced56596a8bc73abc69e6a1867bbb6f7ae7e7`  
		Last Modified: Fri, 11 Dec 2020 02:33:07 GMT  
		Size: 22.7 MB (22707662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92651243e16dc9394c858200d94836db14ccba7cb4834aeeae694f0a4687cf6b`  
		Last Modified: Fri, 11 Dec 2020 04:47:52 GMT  
		Size: 4.9 KB (4892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b2d826e32b2f2e43c3e916a26bd2df22d1c05b4a3c269771f692cc6109a5219`  
		Last Modified: Fri, 11 Dec 2020 04:47:53 GMT  
		Size: 1.8 MB (1811638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d51d0c29898f0b1851ca4596deed2bce269765e91227407da6a13ed97f36789b`  
		Last Modified: Fri, 11 Dec 2020 04:47:52 GMT  
		Size: 1.1 MB (1149588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9980de41615bdd4ec214564640fc3debc326ee0a2f0c5010dc348cb0688c63fa`  
		Last Modified: Fri, 11 Dec 2020 04:47:53 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b841afed721ef8c4147c8af69401487f31b89d0d483e01b0b1e6dd9f6f3f9fa0`  
		Last Modified: Fri, 11 Dec 2020 04:47:52 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:latest` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:ba77a96f15913bc91a757d3092df841020bc4bfb5eb8d2e379e2b574d233dee5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29115518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96037dc9e04dc221c12561d6fd7b9838b736d23355b5183cf1f847c7ca2a7be8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 11 Dec 2020 02:45:53 GMT
ADD file:a5a2f039c00bc638b88cefdff4c3cd1865b4d415bf80c4fe6b496d975af7cc1f in / 
# Fri, 11 Dec 2020 02:45:57 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 06:17:49 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Fri, 11 Dec 2020 06:17:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 06:17:58 GMT
ENV MEMCACHED_VERSION=1.6.9
# Fri, 11 Dec 2020 06:17:59 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Fri, 11 Dec 2020 06:21:52 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Fri, 11 Dec 2020 06:21:52 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Fri, 11 Dec 2020 06:21:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 11 Dec 2020 06:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 06:21:56 GMT
USER memcache
# Fri, 11 Dec 2020 06:21:57 GMT
EXPOSE 11211
# Fri, 11 Dec 2020 06:21:57 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c9648d7fcbb6d597cf33916d8fcd207fde8ec05d764b4480d4f3e884e142a902`  
		Last Modified: Fri, 11 Dec 2020 02:53:14 GMT  
		Size: 25.9 MB (25856191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4a2989a5f0ead8f181bf0a3d83c3942b680601a3d54507ae9cc7e9de4c0753e`  
		Last Modified: Fri, 11 Dec 2020 06:25:40 GMT  
		Size: 5.0 KB (5025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d8830b39b6645b4cb0dde9646d4f8061cdf8ada45104e46f5b34a61ac86bed`  
		Last Modified: Fri, 11 Dec 2020 06:25:40 GMT  
		Size: 2.1 MB (2075073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d391a789256382a7a47ee06b4d35a3edded36259031fb3224ba5f7ca1f9742d4`  
		Last Modified: Fri, 11 Dec 2020 06:25:40 GMT  
		Size: 1.2 MB (1178823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfb3c1da48281e238cd187736bfa7235d50ff6259377132eefe18e3232a0447c`  
		Last Modified: Fri, 11 Dec 2020 06:25:40 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c504fa6fcce1d5dcf11dce135016d72f448155fab34ab26f437e352cdaf216ac`  
		Last Modified: Fri, 11 Dec 2020 06:25:39 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:latest` - linux; 386

```console
$ docker pull memcached@sha256:863e1bdc397af4d93b2c8e1eb0a45e0c142993b6b8fd603a3e1bbe6dc3b4ef9b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31175097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:542592c8f397aed9543c98f050687f49357cc4b41dca959a9ddf05d8a9198925`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 11 Dec 2020 02:03:07 GMT
ADD file:a0879774b23f70c4db7f7b04736cca142beb0b22e93f5952364ca990a1675552 in / 
# Fri, 11 Dec 2020 02:03:08 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 05:34:46 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Fri, 11 Dec 2020 05:34:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 05:34:54 GMT
ENV MEMCACHED_VERSION=1.6.9
# Fri, 11 Dec 2020 05:34:55 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Fri, 11 Dec 2020 05:39:41 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Fri, 11 Dec 2020 05:39:41 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Fri, 11 Dec 2020 05:39:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 11 Dec 2020 05:39:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 05:39:43 GMT
USER memcache
# Fri, 11 Dec 2020 05:39:44 GMT
EXPOSE 11211
# Fri, 11 Dec 2020 05:39:44 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:cfec07a090788e68b692f30d34e11dc7af0f1c8112fbc846e8e40e24faf882d7`  
		Last Modified: Fri, 11 Dec 2020 02:09:41 GMT  
		Size: 27.8 MB (27757584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:125b182979466ebdbd3684a56e18ea817967570f9d1da07d9c718800ee13b416`  
		Last Modified: Fri, 11 Dec 2020 05:45:04 GMT  
		Size: 4.9 KB (4896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285fdabbbbfd7d8439d518ed03f316e8f277aa4a9065eb0f7e8aca3e742715ba`  
		Last Modified: Fri, 11 Dec 2020 05:45:04 GMT  
		Size: 2.2 MB (2208312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d562f6207bb4224e6ed498f2681d75cd3b8a29895ac7937d7aa7365bed41a0`  
		Last Modified: Fri, 11 Dec 2020 05:45:05 GMT  
		Size: 1.2 MB (1203898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa4610f56210f92d9512e834853224b8c11fe48b8e905c119fccbf8c9ea5735`  
		Last Modified: Fri, 11 Dec 2020 05:45:04 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09602d135be3e9fa1bd567c87855653a3e3c8f8eaf212c6877c123615940b3b`  
		Last Modified: Fri, 11 Dec 2020 05:45:04 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:latest` - linux; mips64le

```console
$ docker pull memcached@sha256:7db583e5b72c87669d31ad8e231e6c7adfdaf7d534c936f229b982b5e0dae8a3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.8 MB (28750173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f1fa615248a5befd5ecbf5f7a7a1eafcb767aa432e95d5b65347dd114d893fa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 11 Dec 2020 02:03:30 GMT
ADD file:edb758d587972f30ef28b162dcabf79f61b685afa3c6066cb611c61abea124f3 in / 
# Fri, 11 Dec 2020 02:03:30 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 03:09:11 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Fri, 11 Dec 2020 03:09:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 03:09:24 GMT
ENV MEMCACHED_VERSION=1.6.9
# Fri, 11 Dec 2020 03:09:24 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Fri, 11 Dec 2020 03:15:05 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Fri, 11 Dec 2020 03:15:05 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Fri, 11 Dec 2020 03:15:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 11 Dec 2020 03:15:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 03:15:07 GMT
USER memcache
# Fri, 11 Dec 2020 03:15:08 GMT
EXPOSE 11211
# Fri, 11 Dec 2020 03:15:08 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bed35f8e8e003f268bd91c8bc28d93f0b1463296add14ab3ec84c3d3d30e9025`  
		Last Modified: Fri, 11 Dec 2020 02:10:15 GMT  
		Size: 25.8 MB (25769881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ad87d218b0aae22ee1256aeaeb3c17629573b0974420752b41c8669bd82173`  
		Last Modified: Fri, 11 Dec 2020 03:15:31 GMT  
		Size: 5.0 KB (4979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c113c88acc60509bb945511ae953da94c2f6cba67440c33d6d592568b131ae0`  
		Last Modified: Fri, 11 Dec 2020 03:15:32 GMT  
		Size: 1.8 MB (1776264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86f68e3fb18b7005b2291db6286f4b8be1a908a5dbc4cbea34f789b583729d1c`  
		Last Modified: Fri, 11 Dec 2020 03:15:32 GMT  
		Size: 1.2 MB (1198641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01eccd7ed1e8b1bc7ae953db8ed512bb963d96e5523bcbbe8ac0b7130b246266`  
		Last Modified: Fri, 11 Dec 2020 03:15:31 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:224d3b20e2efa0cb7b62cd59a9572f87606ff20c5b3bf04ea2a23f17a836efa7`  
		Last Modified: Fri, 11 Dec 2020 03:15:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:latest` - linux; ppc64le

```console
$ docker pull memcached@sha256:6f8c28503a9a3aadaba20c8a60fea9f450cff6023be384229c6093d1cce78a32
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.1 MB (34085694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f68f9d6f6d0ff09d1c44ad6fdc31842fa02b165535d452d0cf7ced031aca0ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 11 Dec 2020 03:34:02 GMT
ADD file:eca1a7737bd5e84ff883c4c284c0cd22492145d9cd7ae3b8e7b490e3d8e5aefb in / 
# Fri, 11 Dec 2020 03:34:11 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 16:07:08 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Fri, 11 Dec 2020 16:07:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 16:07:29 GMT
ENV MEMCACHED_VERSION=1.6.9
# Fri, 11 Dec 2020 16:07:31 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Fri, 11 Dec 2020 16:14:44 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Fri, 11 Dec 2020 16:14:48 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Fri, 11 Dec 2020 16:14:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 11 Dec 2020 16:15:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 16:15:02 GMT
USER memcache
# Fri, 11 Dec 2020 16:15:04 GMT
EXPOSE 11211
# Fri, 11 Dec 2020 16:15:07 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c0f0648876332890be87a9f32ec4ad2a939e805be3152ab991a923f7dec2b35d`  
		Last Modified: Fri, 11 Dec 2020 03:41:39 GMT  
		Size: 30.5 MB (30524717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86be564d1b6e201f1d3e3d2ce8c9f7d54d6db1ba9303e9298d16527aa7022552`  
		Last Modified: Fri, 11 Dec 2020 16:20:10 GMT  
		Size: 5.0 KB (4985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea84c614bd4b7a09070e40efb6388c77482da788f3f51158d7bdf2920858b5c5`  
		Last Modified: Fri, 11 Dec 2020 16:20:09 GMT  
		Size: 2.3 MB (2322953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e7a7cdc7a222a1e649894b9cd60aaf904f5e600c65f1542ccc70457826bf54`  
		Last Modified: Fri, 11 Dec 2020 16:20:10 GMT  
		Size: 1.2 MB (1232631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:124ca47ab85a63f4ae7b141905196be41389d3a529dd605b341f7b26201c6262`  
		Last Modified: Fri, 11 Dec 2020 16:20:10 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12cb3df4339b3922a947928cfb29b24307e1a3aed08a26a807b27a40c520c432`  
		Last Modified: Fri, 11 Dec 2020 16:20:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:latest` - linux; s390x

```console
$ docker pull memcached@sha256:3d178b57d4226285dd7555e8a466e47337bedcb188d20e07049daa6e84b7f49a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.8 MB (28804148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6dc93e8d3427938db6bb6a79bae64a3e0f3e2813e8e662e272f8e62a6e7e94b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 11 Dec 2020 02:12:11 GMT
ADD file:db86ce5a1665b6d8ac734c54ac249a811c58484f569b935b14772445962428aa in / 
# Fri, 11 Dec 2020 02:12:15 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 03:36:28 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Fri, 11 Dec 2020 03:36:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 03:36:33 GMT
ENV MEMCACHED_VERSION=1.6.9
# Fri, 11 Dec 2020 03:36:34 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Fri, 11 Dec 2020 03:40:23 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Fri, 11 Dec 2020 03:40:23 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Fri, 11 Dec 2020 03:40:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 11 Dec 2020 03:40:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 03:40:25 GMT
USER memcache
# Fri, 11 Dec 2020 03:40:26 GMT
EXPOSE 11211
# Fri, 11 Dec 2020 03:40:26 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f4cf10ca9f31aab0854647d7878dc4db838e93b892b843dde3db24f2e909a106`  
		Last Modified: Fri, 11 Dec 2020 02:17:07 GMT  
		Size: 25.7 MB (25713957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5fee0f9b7c8f8029b3f0e84c478491b92a268655b1f6d560bc233b2ae31ebb1`  
		Last Modified: Fri, 11 Dec 2020 03:45:07 GMT  
		Size: 5.0 KB (5025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33dd61679906d3d1911efeb12a5b0aa35b2663ecdfa293504b022b5e475177bc`  
		Last Modified: Fri, 11 Dec 2020 03:45:08 GMT  
		Size: 1.9 MB (1886302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c0c80075aa43e4d25ca63fe3b55044f06f3955f2d4e356238a25578e26b629f`  
		Last Modified: Fri, 11 Dec 2020 03:45:07 GMT  
		Size: 1.2 MB (1198456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65c68b5e030c291a2b89d310aa10afd000bba8b1e52baaf825baf1de8e87d45d`  
		Last Modified: Fri, 11 Dec 2020 03:45:07 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf651365e6ca5de80f44c00f8cf1f9b822bc0cf09443dc1fd0ca11935567b37`  
		Last Modified: Fri, 11 Dec 2020 03:45:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
