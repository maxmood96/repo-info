<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `memcached`

-	[`memcached:1`](#memcached1)
-	[`memcached:1.6`](#memcached16)
-	[`memcached:1.6.5`](#memcached165)
-	[`memcached:1.6.5-alpine`](#memcached165-alpine)
-	[`memcached:1.6-alpine`](#memcached16-alpine)
-	[`memcached:1-alpine`](#memcached1-alpine)
-	[`memcached:alpine`](#memcachedalpine)
-	[`memcached:latest`](#memcachedlatest)

## `memcached:1`

```console
$ docker pull memcached@sha256:d404bf441a84afab01e3fa5ff9588ed54e5b6d3e29bf232f45c48e2565848ae6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `memcached:1` - linux; amd64

```console
$ docker pull memcached@sha256:e4b600639b0b2540e93f82cb213c9d0ab3ca7443b59459876425958f6e655834
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 MB (30485949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e310fbc8b97af886d4d825b655c4c21be64bfd5758ddd23223fdc5b13466c4b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 31 Mar 2020 01:21:01 GMT
ADD file:d1f1b387a158136fb0f8096c8a8ecf5fc146be4e85c1c3c345d44c927692723a in / 
# Tue, 31 Mar 2020 01:21:01 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 13:20:36 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 31 Mar 2020 13:20:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 Apr 2020 00:19:49 GMT
ENV MEMCACHED_VERSION=1.6.5
# Tue, 14 Apr 2020 00:19:49 GMT
ENV MEMCACHED_SHA1=1ddb5f37f69946b63512ad0f89dc448ff7ba5713
# Tue, 14 Apr 2020 00:27:55 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 14 Apr 2020 00:27:55 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 14 Apr 2020 00:27:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 14 Apr 2020 00:27:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2020 00:27:56 GMT
USER memcache
# Tue, 14 Apr 2020 00:27:56 GMT
EXPOSE 11211
# Tue, 14 Apr 2020 00:27:57 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c499e6d256d6d4a546f1c141e04b5b4951983ba7581e39deaf5cc595289ee70f`  
		Last Modified: Tue, 31 Mar 2020 01:26:37 GMT  
		Size: 27.1 MB (27091862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512f277e1da84b0b9319530d40c48750bb22b13f4816d103040d20c0635c28be`  
		Last Modified: Tue, 31 Mar 2020 13:29:52 GMT  
		Size: 5.0 KB (4984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdda69e165e26c667ba223dc215274101c3c6e41db182bd651aadf5e5623fc35`  
		Last Modified: Tue, 31 Mar 2020 13:29:53 GMT  
		Size: 2.2 MB (2196476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1780eff22105ecc8f0d35be5b018221e6cded84048aab30d770861ff638124e`  
		Last Modified: Tue, 14 Apr 2020 00:36:46 GMT  
		Size: 1.2 MB (1192218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ef130d1915ebd4a9b8360f39f34c7cc53aadf772671b5a104da3ae654221ca`  
		Last Modified: Tue, 14 Apr 2020 00:36:46 GMT  
		Size: 288.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56ebe2ea417575287b4ef17c9cb0a263ee4646fa6ed1553a617edf0b35a832b2`  
		Last Modified: Tue, 14 Apr 2020 00:36:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1` - linux; arm variant v5

```console
$ docker pull memcached@sha256:552667e7d659ec140e52ce197993eca4f4ae04580cf58bb299339f154ce9289a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.9 MB (27889465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70d335e80be14665b0694c2a8ad92bd15d99f2245a72e131de7d455d8f86e8de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 31 Mar 2020 01:24:54 GMT
ADD file:e08ed9e60228d351de400af5746474777a562d99f17e0cb1ce3e3d352e9ec751 in / 
# Tue, 31 Mar 2020 01:24:56 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:54:28 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 31 Mar 2020 01:55:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 13 Apr 2020 23:51:13 GMT
ENV MEMCACHED_VERSION=1.6.5
# Mon, 13 Apr 2020 23:51:15 GMT
ENV MEMCACHED_SHA1=1ddb5f37f69946b63512ad0f89dc448ff7ba5713
# Tue, 14 Apr 2020 01:20:37 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 14 Apr 2020 01:20:40 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 14 Apr 2020 01:20:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 14 Apr 2020 01:20:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2020 01:20:54 GMT
USER memcache
# Tue, 14 Apr 2020 01:20:56 GMT
EXPOSE 11211
# Tue, 14 Apr 2020 01:20:57 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:440df189aa3df85587f2d7d348500930481b3752dcb887d212de9b44b49076dd`  
		Last Modified: Tue, 31 Mar 2020 01:33:04 GMT  
		Size: 24.8 MB (24830324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bde8351817341fa2fec288d97635ede228892bbb58fc5c6ca54441acef6f0766`  
		Last Modified: Tue, 31 Mar 2020 03:24:42 GMT  
		Size: 4.9 KB (4896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b011e5f13bdf6608cafa62557b3c877e4794590eaadced0b8a49fe24a28d110`  
		Last Modified: Tue, 31 Mar 2020 03:24:44 GMT  
		Size: 1.9 MB (1896786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b83243350d1cc24097d68bc247cbb15df78dad5055598e77779909c8b6dc9b`  
		Last Modified: Tue, 14 Apr 2020 01:21:15 GMT  
		Size: 1.2 MB (1157053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16d88842ba9a93f3329b9f416cd2e0efca324f36356c4713ca584a17c791173b`  
		Last Modified: Tue, 14 Apr 2020 01:21:13 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35420a44da1fda5e245ef5baf104f3fa9cd5564e894134f8d3c697f50b8d42a1`  
		Last Modified: Tue, 14 Apr 2020 01:21:19 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1` - linux; arm variant v7

```console
$ docker pull memcached@sha256:54bcd309e2f20393d4697e22b71344137d3f1fdeb447078522a5a2d6a464117e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 MB (25646504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd1835a38d745cc54481b86a3603e5fe1771df287e08d6061cb35577ce92b735`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 31 Mar 2020 01:48:12 GMT
ADD file:8c3ed0df404a6bcaf7583e71796cb4c1f40e87288953a21d4ee5946079c3274f in / 
# Tue, 31 Mar 2020 01:48:13 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 03:27:08 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 31 Mar 2020 03:28:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 Apr 2020 01:21:52 GMT
ENV MEMCACHED_VERSION=1.6.5
# Tue, 14 Apr 2020 01:21:54 GMT
ENV MEMCACHED_SHA1=1ddb5f37f69946b63512ad0f89dc448ff7ba5713
# Tue, 14 Apr 2020 01:50:54 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 14 Apr 2020 01:50:57 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 14 Apr 2020 01:51:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 14 Apr 2020 01:51:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2020 01:51:11 GMT
USER memcache
# Tue, 14 Apr 2020 01:51:12 GMT
EXPOSE 11211
# Tue, 14 Apr 2020 01:51:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:98098fa10651fdba12c848231b7428536a120e17637f1f9e0d25c63880483fcc`  
		Last Modified: Tue, 31 Mar 2020 01:56:24 GMT  
		Size: 22.7 MB (22699731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a7a42e48b851419bcd11506631a8d336fb394d979dcea8feb4830f38ba7cfd7`  
		Last Modified: Tue, 31 Mar 2020 04:39:27 GMT  
		Size: 4.9 KB (4899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc96c4fde110b7a8691d85cf0523cd326fbfd1bcbf928719f6173cd292c91305`  
		Last Modified: Tue, 31 Mar 2020 04:39:35 GMT  
		Size: 1.8 MB (1811551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca1ebe9584513d346175a7b8dc24e8a0e1f282079ab035f21745b1efb49aee2`  
		Last Modified: Tue, 14 Apr 2020 03:14:41 GMT  
		Size: 1.1 MB (1129915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3670b9b896bea4402ae6cf76d7c5690c7be94b8712a6ba9bdbc5162c478c3f4a`  
		Last Modified: Tue, 14 Apr 2020 03:14:40 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13fc7c30db064f3e3c4355aa5316e9ee78fc6d5727ba346d8289b531a5244235`  
		Last Modified: Tue, 14 Apr 2020 03:14:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:296400cfcf0b05f045c250b4839f2ef4312e75a29171dc0453ea424a2a40f683
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29094935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b876c7370d1497d75e73a86321425fb8e2e449893d19fcdb24d41f856d946a08`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 31 Mar 2020 02:05:33 GMT
ADD file:47ab456123ae97a527249191ff2bc0014e7ef0ae186aec91bf6a63eb077ecb91 in / 
# Tue, 31 Mar 2020 02:05:35 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 08:39:07 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 31 Mar 2020 08:39:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 13 Apr 2020 23:47:52 GMT
ENV MEMCACHED_VERSION=1.6.5
# Mon, 13 Apr 2020 23:47:53 GMT
ENV MEMCACHED_SHA1=1ddb5f37f69946b63512ad0f89dc448ff7ba5713
# Mon, 13 Apr 2020 23:57:24 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Mon, 13 Apr 2020 23:57:24 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Mon, 13 Apr 2020 23:57:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 13 Apr 2020 23:57:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Apr 2020 23:57:27 GMT
USER memcache
# Mon, 13 Apr 2020 23:57:28 GMT
EXPOSE 11211
# Mon, 13 Apr 2020 23:57:28 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a6c32b8bc1ce2b374630673ded1d5ef5a98936d045bf0632fcf599dc2229d493`  
		Last Modified: Tue, 31 Mar 2020 02:12:15 GMT  
		Size: 25.9 MB (25851645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72560398e0dc8991a53cd07c580b14e3c2024d7af30d2dfe8428d913006af5a9`  
		Last Modified: Tue, 31 Mar 2020 08:48:55 GMT  
		Size: 5.0 KB (5028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4febdbdc3565b2d569ed0a6885c548a5755cd9a2b52c21b351d254c83e6fff7`  
		Last Modified: Tue, 31 Mar 2020 08:48:55 GMT  
		Size: 2.1 MB (2074952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8266bd2499012e842778a6e03cccde2b97d44f659ebbfcd1a69eccc22d1bc3a`  
		Last Modified: Tue, 14 Apr 2020 00:07:33 GMT  
		Size: 1.2 MB (1162903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99b2bf34e46eab97471c453efd6d739d3d6f3de32789d23cf81e6eaa94d2ea6e`  
		Last Modified: Tue, 14 Apr 2020 00:07:33 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1a5e887fbf0bacccd7a723d6c972e22f49e6cdbbdc0d5156f127d8e5507717b`  
		Last Modified: Tue, 14 Apr 2020 00:07:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1` - linux; 386

```console
$ docker pull memcached@sha256:f77cbe58b76a6763ebbacbb8d9a53c9705b0f1784d50261627ea7148225a53b4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31156720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06a5671f4598de98b696abbd0eaee1875af3cf8d5825a2c079f751054a79a319`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 31 Mar 2020 00:39:42 GMT
ADD file:a453117866661af4ddfa21203d65ce6661efeaeca2a1704e09747c83b4c58e47 in / 
# Tue, 31 Mar 2020 00:39:42 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 11:45:29 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 31 Mar 2020 11:45:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 Apr 2020 00:15:39 GMT
ENV MEMCACHED_VERSION=1.6.5
# Tue, 14 Apr 2020 00:15:40 GMT
ENV MEMCACHED_SHA1=1ddb5f37f69946b63512ad0f89dc448ff7ba5713
# Tue, 14 Apr 2020 00:24:13 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 14 Apr 2020 00:24:13 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 14 Apr 2020 00:24:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 14 Apr 2020 00:24:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2020 00:24:14 GMT
USER memcache
# Tue, 14 Apr 2020 00:24:14 GMT
EXPOSE 11211
# Tue, 14 Apr 2020 00:24:15 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2314106a15e49c7908bebb2c697dcaf3d6a1626b70fe72bc0c0cb71eb216ddc3`  
		Last Modified: Tue, 31 Mar 2020 00:45:31 GMT  
		Size: 27.7 MB (27747648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3bafab0976764495dda52d0c16addb4770d62d8f9de55728b752ff3448f2292`  
		Last Modified: Tue, 31 Mar 2020 11:55:29 GMT  
		Size: 4.9 KB (4899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8307e5e61ebc9ed2430c9e45ba3437aa1deebed0882ce15c36616e0debf28b36`  
		Last Modified: Tue, 31 Mar 2020 11:55:29 GMT  
		Size: 2.2 MB (2208079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1a1a09da032c7622fe0330fa14876496b04b5e9e81943f09df1b315bec0a4d`  
		Last Modified: Tue, 14 Apr 2020 00:33:22 GMT  
		Size: 1.2 MB (1195686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80e37d2af038355acfb8af6aca4e4cb3a65c0d08aaab7723c1987d1006fbf17b`  
		Last Modified: Tue, 14 Apr 2020 00:33:21 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ec8103e2aa301996d108c97a0d120cdc72d11519b4269350d4d72c026e919d`  
		Last Modified: Tue, 14 Apr 2020 00:33:21 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1` - linux; ppc64le

```console
$ docker pull memcached@sha256:b587e1ac02d9b43b4dc13af7294b8f81a5e638b13c981743a1ffb2798c733976
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.1 MB (34064242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8704abb1ba80a90926fd4cc6cb9e20c5f3624763df555561a961411766e635a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 31 Mar 2020 01:32:42 GMT
ADD file:36c02e92574faba45b64cfed78a0a0359d65ad175b17128bf554a2a5c0086ff5 in / 
# Tue, 31 Mar 2020 01:32:47 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 12:45:58 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 31 Mar 2020 12:46:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 Apr 2020 00:29:39 GMT
ENV MEMCACHED_VERSION=1.6.5
# Tue, 14 Apr 2020 00:29:44 GMT
ENV MEMCACHED_SHA1=1ddb5f37f69946b63512ad0f89dc448ff7ba5713
# Tue, 14 Apr 2020 00:41:15 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 14 Apr 2020 00:41:17 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 14 Apr 2020 00:41:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 14 Apr 2020 00:41:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2020 00:41:38 GMT
USER memcache
# Tue, 14 Apr 2020 00:41:45 GMT
EXPOSE 11211
# Tue, 14 Apr 2020 00:41:51 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9df6bbae5eeb29e9aac2f39cff517c694cce60f01ee477abcdedcd8e8c01c38f`  
		Last Modified: Tue, 31 Mar 2020 01:45:59 GMT  
		Size: 30.5 MB (30518493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2786c1a6fbad6e8c56e4f7e33b4d41c64efd06c4cdb303a50c07ee1f4c5f7a69`  
		Last Modified: Tue, 31 Mar 2020 12:58:00 GMT  
		Size: 5.0 KB (4987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:722cfb50c03533f4b5c83c84a2f565dbcdbf63c01460ae91d35aafacd94454fe`  
		Last Modified: Tue, 31 Mar 2020 12:58:00 GMT  
		Size: 2.3 MB (2322647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec1b5923ebd47cd1e2443a1ff44899de7b683eadb673d9404c7c259b96277c7d`  
		Last Modified: Tue, 14 Apr 2020 00:51:37 GMT  
		Size: 1.2 MB (1217708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3311546eb5856360dd803bbb0e75a832bef2fb729dce22a03be0656ebbcec2f4`  
		Last Modified: Tue, 14 Apr 2020 00:51:36 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5646db67b9fcecdc7d9a2c867f4515d81b3f3e429cbcb5b3804420a392b277ae`  
		Last Modified: Tue, 14 Apr 2020 00:51:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1` - linux; s390x

```console
$ docker pull memcached@sha256:057b9567b3c01a5b0dbf1c7dba5b89d88df721093c01da5c6a1425c1f8ad6265
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.7 MB (28694839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe2378496a97259729a8423d4b14be0ea1db6e01b3f9aa9e34431ef824d655e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 28 Dec 2019 04:42:03 GMT
ADD file:eec6c56f8680753860198c3af0d94aabb87018ca30f6f6e346621a6bffe0e4b8 in / 
# Sat, 28 Dec 2019 04:42:04 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 09:52:58 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Sat, 28 Dec 2019 09:53:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 09:53:02 GMT
ENV MEMCACHED_VERSION=1.5.20
# Sat, 28 Dec 2019 09:53:02 GMT
ENV MEMCACHED_SHA1=5d3b5af3ce0a1483d655017db7228bcaeff10d47
# Sat, 28 Dec 2019 09:57:41 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Sat, 28 Dec 2019 09:57:41 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Sat, 28 Dec 2019 09:57:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 28 Dec 2019 09:57:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Dec 2019 09:57:42 GMT
USER memcache
# Sat, 28 Dec 2019 09:57:42 GMT
EXPOSE 11211
# Sat, 28 Dec 2019 09:57:42 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f7542f43e95fb32a870ee38d7f0e7bb23267ac8dcf709e3944311b0a30d7a479`  
		Last Modified: Sat, 28 Dec 2019 04:45:08 GMT  
		Size: 25.7 MB (25705315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10233ccd3a1a569a8ec38365e560732bbd6adbbe1646b79cee3569d59f7cef73`  
		Last Modified: Sat, 28 Dec 2019 09:57:55 GMT  
		Size: 5.0 KB (5022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f3e3dfd06ace4d055f1539e38c0fb68e4d1866043a1ba372c8c2f0fec48315d`  
		Last Modified: Sat, 28 Dec 2019 09:57:55 GMT  
		Size: 1.9 MB (1885865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47cce4b30798653a4fcf3fd9160a90374e103d5c1e877e69645d033c0f916e67`  
		Last Modified: Sat, 28 Dec 2019 09:57:55 GMT  
		Size: 1.1 MB (1098229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:982ba8604e516e190f19469aa238d4197aa0000182cbc54d57345a029b765600`  
		Last Modified: Sat, 28 Dec 2019 09:57:55 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aabfe12e62b1d54d9dce449f2dc85f703ade5574f14eadfa54a601a86cc96e54`  
		Last Modified: Sat, 28 Dec 2019 09:57:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:1.6`

```console
$ docker pull memcached@sha256:f1627f38e052f628079e6b4adec2cc9104049e6e97d21b924c1a33605def03a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `memcached:1.6` - linux; amd64

```console
$ docker pull memcached@sha256:e4b600639b0b2540e93f82cb213c9d0ab3ca7443b59459876425958f6e655834
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 MB (30485949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e310fbc8b97af886d4d825b655c4c21be64bfd5758ddd23223fdc5b13466c4b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 31 Mar 2020 01:21:01 GMT
ADD file:d1f1b387a158136fb0f8096c8a8ecf5fc146be4e85c1c3c345d44c927692723a in / 
# Tue, 31 Mar 2020 01:21:01 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 13:20:36 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 31 Mar 2020 13:20:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 Apr 2020 00:19:49 GMT
ENV MEMCACHED_VERSION=1.6.5
# Tue, 14 Apr 2020 00:19:49 GMT
ENV MEMCACHED_SHA1=1ddb5f37f69946b63512ad0f89dc448ff7ba5713
# Tue, 14 Apr 2020 00:27:55 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 14 Apr 2020 00:27:55 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 14 Apr 2020 00:27:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 14 Apr 2020 00:27:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2020 00:27:56 GMT
USER memcache
# Tue, 14 Apr 2020 00:27:56 GMT
EXPOSE 11211
# Tue, 14 Apr 2020 00:27:57 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c499e6d256d6d4a546f1c141e04b5b4951983ba7581e39deaf5cc595289ee70f`  
		Last Modified: Tue, 31 Mar 2020 01:26:37 GMT  
		Size: 27.1 MB (27091862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512f277e1da84b0b9319530d40c48750bb22b13f4816d103040d20c0635c28be`  
		Last Modified: Tue, 31 Mar 2020 13:29:52 GMT  
		Size: 5.0 KB (4984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdda69e165e26c667ba223dc215274101c3c6e41db182bd651aadf5e5623fc35`  
		Last Modified: Tue, 31 Mar 2020 13:29:53 GMT  
		Size: 2.2 MB (2196476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1780eff22105ecc8f0d35be5b018221e6cded84048aab30d770861ff638124e`  
		Last Modified: Tue, 14 Apr 2020 00:36:46 GMT  
		Size: 1.2 MB (1192218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ef130d1915ebd4a9b8360f39f34c7cc53aadf772671b5a104da3ae654221ca`  
		Last Modified: Tue, 14 Apr 2020 00:36:46 GMT  
		Size: 288.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56ebe2ea417575287b4ef17c9cb0a263ee4646fa6ed1553a617edf0b35a832b2`  
		Last Modified: Tue, 14 Apr 2020 00:36:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6` - linux; arm variant v5

```console
$ docker pull memcached@sha256:552667e7d659ec140e52ce197993eca4f4ae04580cf58bb299339f154ce9289a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.9 MB (27889465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70d335e80be14665b0694c2a8ad92bd15d99f2245a72e131de7d455d8f86e8de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 31 Mar 2020 01:24:54 GMT
ADD file:e08ed9e60228d351de400af5746474777a562d99f17e0cb1ce3e3d352e9ec751 in / 
# Tue, 31 Mar 2020 01:24:56 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:54:28 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 31 Mar 2020 01:55:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 13 Apr 2020 23:51:13 GMT
ENV MEMCACHED_VERSION=1.6.5
# Mon, 13 Apr 2020 23:51:15 GMT
ENV MEMCACHED_SHA1=1ddb5f37f69946b63512ad0f89dc448ff7ba5713
# Tue, 14 Apr 2020 01:20:37 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 14 Apr 2020 01:20:40 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 14 Apr 2020 01:20:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 14 Apr 2020 01:20:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2020 01:20:54 GMT
USER memcache
# Tue, 14 Apr 2020 01:20:56 GMT
EXPOSE 11211
# Tue, 14 Apr 2020 01:20:57 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:440df189aa3df85587f2d7d348500930481b3752dcb887d212de9b44b49076dd`  
		Last Modified: Tue, 31 Mar 2020 01:33:04 GMT  
		Size: 24.8 MB (24830324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bde8351817341fa2fec288d97635ede228892bbb58fc5c6ca54441acef6f0766`  
		Last Modified: Tue, 31 Mar 2020 03:24:42 GMT  
		Size: 4.9 KB (4896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b011e5f13bdf6608cafa62557b3c877e4794590eaadced0b8a49fe24a28d110`  
		Last Modified: Tue, 31 Mar 2020 03:24:44 GMT  
		Size: 1.9 MB (1896786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b83243350d1cc24097d68bc247cbb15df78dad5055598e77779909c8b6dc9b`  
		Last Modified: Tue, 14 Apr 2020 01:21:15 GMT  
		Size: 1.2 MB (1157053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16d88842ba9a93f3329b9f416cd2e0efca324f36356c4713ca584a17c791173b`  
		Last Modified: Tue, 14 Apr 2020 01:21:13 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35420a44da1fda5e245ef5baf104f3fa9cd5564e894134f8d3c697f50b8d42a1`  
		Last Modified: Tue, 14 Apr 2020 01:21:19 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6` - linux; arm variant v7

```console
$ docker pull memcached@sha256:54bcd309e2f20393d4697e22b71344137d3f1fdeb447078522a5a2d6a464117e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 MB (25646504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd1835a38d745cc54481b86a3603e5fe1771df287e08d6061cb35577ce92b735`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 31 Mar 2020 01:48:12 GMT
ADD file:8c3ed0df404a6bcaf7583e71796cb4c1f40e87288953a21d4ee5946079c3274f in / 
# Tue, 31 Mar 2020 01:48:13 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 03:27:08 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 31 Mar 2020 03:28:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 Apr 2020 01:21:52 GMT
ENV MEMCACHED_VERSION=1.6.5
# Tue, 14 Apr 2020 01:21:54 GMT
ENV MEMCACHED_SHA1=1ddb5f37f69946b63512ad0f89dc448ff7ba5713
# Tue, 14 Apr 2020 01:50:54 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 14 Apr 2020 01:50:57 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 14 Apr 2020 01:51:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 14 Apr 2020 01:51:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2020 01:51:11 GMT
USER memcache
# Tue, 14 Apr 2020 01:51:12 GMT
EXPOSE 11211
# Tue, 14 Apr 2020 01:51:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:98098fa10651fdba12c848231b7428536a120e17637f1f9e0d25c63880483fcc`  
		Last Modified: Tue, 31 Mar 2020 01:56:24 GMT  
		Size: 22.7 MB (22699731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a7a42e48b851419bcd11506631a8d336fb394d979dcea8feb4830f38ba7cfd7`  
		Last Modified: Tue, 31 Mar 2020 04:39:27 GMT  
		Size: 4.9 KB (4899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc96c4fde110b7a8691d85cf0523cd326fbfd1bcbf928719f6173cd292c91305`  
		Last Modified: Tue, 31 Mar 2020 04:39:35 GMT  
		Size: 1.8 MB (1811551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca1ebe9584513d346175a7b8dc24e8a0e1f282079ab035f21745b1efb49aee2`  
		Last Modified: Tue, 14 Apr 2020 03:14:41 GMT  
		Size: 1.1 MB (1129915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3670b9b896bea4402ae6cf76d7c5690c7be94b8712a6ba9bdbc5162c478c3f4a`  
		Last Modified: Tue, 14 Apr 2020 03:14:40 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13fc7c30db064f3e3c4355aa5316e9ee78fc6d5727ba346d8289b531a5244235`  
		Last Modified: Tue, 14 Apr 2020 03:14:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:296400cfcf0b05f045c250b4839f2ef4312e75a29171dc0453ea424a2a40f683
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29094935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b876c7370d1497d75e73a86321425fb8e2e449893d19fcdb24d41f856d946a08`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 31 Mar 2020 02:05:33 GMT
ADD file:47ab456123ae97a527249191ff2bc0014e7ef0ae186aec91bf6a63eb077ecb91 in / 
# Tue, 31 Mar 2020 02:05:35 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 08:39:07 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 31 Mar 2020 08:39:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 13 Apr 2020 23:47:52 GMT
ENV MEMCACHED_VERSION=1.6.5
# Mon, 13 Apr 2020 23:47:53 GMT
ENV MEMCACHED_SHA1=1ddb5f37f69946b63512ad0f89dc448ff7ba5713
# Mon, 13 Apr 2020 23:57:24 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Mon, 13 Apr 2020 23:57:24 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Mon, 13 Apr 2020 23:57:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 13 Apr 2020 23:57:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Apr 2020 23:57:27 GMT
USER memcache
# Mon, 13 Apr 2020 23:57:28 GMT
EXPOSE 11211
# Mon, 13 Apr 2020 23:57:28 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a6c32b8bc1ce2b374630673ded1d5ef5a98936d045bf0632fcf599dc2229d493`  
		Last Modified: Tue, 31 Mar 2020 02:12:15 GMT  
		Size: 25.9 MB (25851645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72560398e0dc8991a53cd07c580b14e3c2024d7af30d2dfe8428d913006af5a9`  
		Last Modified: Tue, 31 Mar 2020 08:48:55 GMT  
		Size: 5.0 KB (5028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4febdbdc3565b2d569ed0a6885c548a5755cd9a2b52c21b351d254c83e6fff7`  
		Last Modified: Tue, 31 Mar 2020 08:48:55 GMT  
		Size: 2.1 MB (2074952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8266bd2499012e842778a6e03cccde2b97d44f659ebbfcd1a69eccc22d1bc3a`  
		Last Modified: Tue, 14 Apr 2020 00:07:33 GMT  
		Size: 1.2 MB (1162903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99b2bf34e46eab97471c453efd6d739d3d6f3de32789d23cf81e6eaa94d2ea6e`  
		Last Modified: Tue, 14 Apr 2020 00:07:33 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1a5e887fbf0bacccd7a723d6c972e22f49e6cdbbdc0d5156f127d8e5507717b`  
		Last Modified: Tue, 14 Apr 2020 00:07:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6` - linux; 386

```console
$ docker pull memcached@sha256:f77cbe58b76a6763ebbacbb8d9a53c9705b0f1784d50261627ea7148225a53b4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31156720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06a5671f4598de98b696abbd0eaee1875af3cf8d5825a2c079f751054a79a319`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 31 Mar 2020 00:39:42 GMT
ADD file:a453117866661af4ddfa21203d65ce6661efeaeca2a1704e09747c83b4c58e47 in / 
# Tue, 31 Mar 2020 00:39:42 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 11:45:29 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 31 Mar 2020 11:45:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 Apr 2020 00:15:39 GMT
ENV MEMCACHED_VERSION=1.6.5
# Tue, 14 Apr 2020 00:15:40 GMT
ENV MEMCACHED_SHA1=1ddb5f37f69946b63512ad0f89dc448ff7ba5713
# Tue, 14 Apr 2020 00:24:13 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 14 Apr 2020 00:24:13 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 14 Apr 2020 00:24:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 14 Apr 2020 00:24:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2020 00:24:14 GMT
USER memcache
# Tue, 14 Apr 2020 00:24:14 GMT
EXPOSE 11211
# Tue, 14 Apr 2020 00:24:15 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2314106a15e49c7908bebb2c697dcaf3d6a1626b70fe72bc0c0cb71eb216ddc3`  
		Last Modified: Tue, 31 Mar 2020 00:45:31 GMT  
		Size: 27.7 MB (27747648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3bafab0976764495dda52d0c16addb4770d62d8f9de55728b752ff3448f2292`  
		Last Modified: Tue, 31 Mar 2020 11:55:29 GMT  
		Size: 4.9 KB (4899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8307e5e61ebc9ed2430c9e45ba3437aa1deebed0882ce15c36616e0debf28b36`  
		Last Modified: Tue, 31 Mar 2020 11:55:29 GMT  
		Size: 2.2 MB (2208079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1a1a09da032c7622fe0330fa14876496b04b5e9e81943f09df1b315bec0a4d`  
		Last Modified: Tue, 14 Apr 2020 00:33:22 GMT  
		Size: 1.2 MB (1195686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80e37d2af038355acfb8af6aca4e4cb3a65c0d08aaab7723c1987d1006fbf17b`  
		Last Modified: Tue, 14 Apr 2020 00:33:21 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ec8103e2aa301996d108c97a0d120cdc72d11519b4269350d4d72c026e919d`  
		Last Modified: Tue, 14 Apr 2020 00:33:21 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6` - linux; ppc64le

```console
$ docker pull memcached@sha256:b587e1ac02d9b43b4dc13af7294b8f81a5e638b13c981743a1ffb2798c733976
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.1 MB (34064242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8704abb1ba80a90926fd4cc6cb9e20c5f3624763df555561a961411766e635a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 31 Mar 2020 01:32:42 GMT
ADD file:36c02e92574faba45b64cfed78a0a0359d65ad175b17128bf554a2a5c0086ff5 in / 
# Tue, 31 Mar 2020 01:32:47 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 12:45:58 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 31 Mar 2020 12:46:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 Apr 2020 00:29:39 GMT
ENV MEMCACHED_VERSION=1.6.5
# Tue, 14 Apr 2020 00:29:44 GMT
ENV MEMCACHED_SHA1=1ddb5f37f69946b63512ad0f89dc448ff7ba5713
# Tue, 14 Apr 2020 00:41:15 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 14 Apr 2020 00:41:17 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 14 Apr 2020 00:41:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 14 Apr 2020 00:41:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2020 00:41:38 GMT
USER memcache
# Tue, 14 Apr 2020 00:41:45 GMT
EXPOSE 11211
# Tue, 14 Apr 2020 00:41:51 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9df6bbae5eeb29e9aac2f39cff517c694cce60f01ee477abcdedcd8e8c01c38f`  
		Last Modified: Tue, 31 Mar 2020 01:45:59 GMT  
		Size: 30.5 MB (30518493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2786c1a6fbad6e8c56e4f7e33b4d41c64efd06c4cdb303a50c07ee1f4c5f7a69`  
		Last Modified: Tue, 31 Mar 2020 12:58:00 GMT  
		Size: 5.0 KB (4987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:722cfb50c03533f4b5c83c84a2f565dbcdbf63c01460ae91d35aafacd94454fe`  
		Last Modified: Tue, 31 Mar 2020 12:58:00 GMT  
		Size: 2.3 MB (2322647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec1b5923ebd47cd1e2443a1ff44899de7b683eadb673d9404c7c259b96277c7d`  
		Last Modified: Tue, 14 Apr 2020 00:51:37 GMT  
		Size: 1.2 MB (1217708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3311546eb5856360dd803bbb0e75a832bef2fb729dce22a03be0656ebbcec2f4`  
		Last Modified: Tue, 14 Apr 2020 00:51:36 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5646db67b9fcecdc7d9a2c867f4515d81b3f3e429cbcb5b3804420a392b277ae`  
		Last Modified: Tue, 14 Apr 2020 00:51:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:1.6.5`

```console
$ docker pull memcached@sha256:f1627f38e052f628079e6b4adec2cc9104049e6e97d21b924c1a33605def03a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `memcached:1.6.5` - linux; amd64

```console
$ docker pull memcached@sha256:e4b600639b0b2540e93f82cb213c9d0ab3ca7443b59459876425958f6e655834
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 MB (30485949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e310fbc8b97af886d4d825b655c4c21be64bfd5758ddd23223fdc5b13466c4b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 31 Mar 2020 01:21:01 GMT
ADD file:d1f1b387a158136fb0f8096c8a8ecf5fc146be4e85c1c3c345d44c927692723a in / 
# Tue, 31 Mar 2020 01:21:01 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 13:20:36 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 31 Mar 2020 13:20:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 Apr 2020 00:19:49 GMT
ENV MEMCACHED_VERSION=1.6.5
# Tue, 14 Apr 2020 00:19:49 GMT
ENV MEMCACHED_SHA1=1ddb5f37f69946b63512ad0f89dc448ff7ba5713
# Tue, 14 Apr 2020 00:27:55 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 14 Apr 2020 00:27:55 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 14 Apr 2020 00:27:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 14 Apr 2020 00:27:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2020 00:27:56 GMT
USER memcache
# Tue, 14 Apr 2020 00:27:56 GMT
EXPOSE 11211
# Tue, 14 Apr 2020 00:27:57 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c499e6d256d6d4a546f1c141e04b5b4951983ba7581e39deaf5cc595289ee70f`  
		Last Modified: Tue, 31 Mar 2020 01:26:37 GMT  
		Size: 27.1 MB (27091862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512f277e1da84b0b9319530d40c48750bb22b13f4816d103040d20c0635c28be`  
		Last Modified: Tue, 31 Mar 2020 13:29:52 GMT  
		Size: 5.0 KB (4984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdda69e165e26c667ba223dc215274101c3c6e41db182bd651aadf5e5623fc35`  
		Last Modified: Tue, 31 Mar 2020 13:29:53 GMT  
		Size: 2.2 MB (2196476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1780eff22105ecc8f0d35be5b018221e6cded84048aab30d770861ff638124e`  
		Last Modified: Tue, 14 Apr 2020 00:36:46 GMT  
		Size: 1.2 MB (1192218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ef130d1915ebd4a9b8360f39f34c7cc53aadf772671b5a104da3ae654221ca`  
		Last Modified: Tue, 14 Apr 2020 00:36:46 GMT  
		Size: 288.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56ebe2ea417575287b4ef17c9cb0a263ee4646fa6ed1553a617edf0b35a832b2`  
		Last Modified: Tue, 14 Apr 2020 00:36:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.5` - linux; arm variant v5

```console
$ docker pull memcached@sha256:552667e7d659ec140e52ce197993eca4f4ae04580cf58bb299339f154ce9289a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.9 MB (27889465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70d335e80be14665b0694c2a8ad92bd15d99f2245a72e131de7d455d8f86e8de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 31 Mar 2020 01:24:54 GMT
ADD file:e08ed9e60228d351de400af5746474777a562d99f17e0cb1ce3e3d352e9ec751 in / 
# Tue, 31 Mar 2020 01:24:56 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:54:28 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 31 Mar 2020 01:55:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 13 Apr 2020 23:51:13 GMT
ENV MEMCACHED_VERSION=1.6.5
# Mon, 13 Apr 2020 23:51:15 GMT
ENV MEMCACHED_SHA1=1ddb5f37f69946b63512ad0f89dc448ff7ba5713
# Tue, 14 Apr 2020 01:20:37 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 14 Apr 2020 01:20:40 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 14 Apr 2020 01:20:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 14 Apr 2020 01:20:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2020 01:20:54 GMT
USER memcache
# Tue, 14 Apr 2020 01:20:56 GMT
EXPOSE 11211
# Tue, 14 Apr 2020 01:20:57 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:440df189aa3df85587f2d7d348500930481b3752dcb887d212de9b44b49076dd`  
		Last Modified: Tue, 31 Mar 2020 01:33:04 GMT  
		Size: 24.8 MB (24830324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bde8351817341fa2fec288d97635ede228892bbb58fc5c6ca54441acef6f0766`  
		Last Modified: Tue, 31 Mar 2020 03:24:42 GMT  
		Size: 4.9 KB (4896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b011e5f13bdf6608cafa62557b3c877e4794590eaadced0b8a49fe24a28d110`  
		Last Modified: Tue, 31 Mar 2020 03:24:44 GMT  
		Size: 1.9 MB (1896786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b83243350d1cc24097d68bc247cbb15df78dad5055598e77779909c8b6dc9b`  
		Last Modified: Tue, 14 Apr 2020 01:21:15 GMT  
		Size: 1.2 MB (1157053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16d88842ba9a93f3329b9f416cd2e0efca324f36356c4713ca584a17c791173b`  
		Last Modified: Tue, 14 Apr 2020 01:21:13 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35420a44da1fda5e245ef5baf104f3fa9cd5564e894134f8d3c697f50b8d42a1`  
		Last Modified: Tue, 14 Apr 2020 01:21:19 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.5` - linux; arm variant v7

```console
$ docker pull memcached@sha256:54bcd309e2f20393d4697e22b71344137d3f1fdeb447078522a5a2d6a464117e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 MB (25646504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd1835a38d745cc54481b86a3603e5fe1771df287e08d6061cb35577ce92b735`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 31 Mar 2020 01:48:12 GMT
ADD file:8c3ed0df404a6bcaf7583e71796cb4c1f40e87288953a21d4ee5946079c3274f in / 
# Tue, 31 Mar 2020 01:48:13 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 03:27:08 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 31 Mar 2020 03:28:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 Apr 2020 01:21:52 GMT
ENV MEMCACHED_VERSION=1.6.5
# Tue, 14 Apr 2020 01:21:54 GMT
ENV MEMCACHED_SHA1=1ddb5f37f69946b63512ad0f89dc448ff7ba5713
# Tue, 14 Apr 2020 01:50:54 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 14 Apr 2020 01:50:57 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 14 Apr 2020 01:51:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 14 Apr 2020 01:51:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2020 01:51:11 GMT
USER memcache
# Tue, 14 Apr 2020 01:51:12 GMT
EXPOSE 11211
# Tue, 14 Apr 2020 01:51:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:98098fa10651fdba12c848231b7428536a120e17637f1f9e0d25c63880483fcc`  
		Last Modified: Tue, 31 Mar 2020 01:56:24 GMT  
		Size: 22.7 MB (22699731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a7a42e48b851419bcd11506631a8d336fb394d979dcea8feb4830f38ba7cfd7`  
		Last Modified: Tue, 31 Mar 2020 04:39:27 GMT  
		Size: 4.9 KB (4899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc96c4fde110b7a8691d85cf0523cd326fbfd1bcbf928719f6173cd292c91305`  
		Last Modified: Tue, 31 Mar 2020 04:39:35 GMT  
		Size: 1.8 MB (1811551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca1ebe9584513d346175a7b8dc24e8a0e1f282079ab035f21745b1efb49aee2`  
		Last Modified: Tue, 14 Apr 2020 03:14:41 GMT  
		Size: 1.1 MB (1129915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3670b9b896bea4402ae6cf76d7c5690c7be94b8712a6ba9bdbc5162c478c3f4a`  
		Last Modified: Tue, 14 Apr 2020 03:14:40 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13fc7c30db064f3e3c4355aa5316e9ee78fc6d5727ba346d8289b531a5244235`  
		Last Modified: Tue, 14 Apr 2020 03:14:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.5` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:296400cfcf0b05f045c250b4839f2ef4312e75a29171dc0453ea424a2a40f683
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29094935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b876c7370d1497d75e73a86321425fb8e2e449893d19fcdb24d41f856d946a08`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 31 Mar 2020 02:05:33 GMT
ADD file:47ab456123ae97a527249191ff2bc0014e7ef0ae186aec91bf6a63eb077ecb91 in / 
# Tue, 31 Mar 2020 02:05:35 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 08:39:07 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 31 Mar 2020 08:39:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 13 Apr 2020 23:47:52 GMT
ENV MEMCACHED_VERSION=1.6.5
# Mon, 13 Apr 2020 23:47:53 GMT
ENV MEMCACHED_SHA1=1ddb5f37f69946b63512ad0f89dc448ff7ba5713
# Mon, 13 Apr 2020 23:57:24 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Mon, 13 Apr 2020 23:57:24 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Mon, 13 Apr 2020 23:57:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 13 Apr 2020 23:57:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Apr 2020 23:57:27 GMT
USER memcache
# Mon, 13 Apr 2020 23:57:28 GMT
EXPOSE 11211
# Mon, 13 Apr 2020 23:57:28 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a6c32b8bc1ce2b374630673ded1d5ef5a98936d045bf0632fcf599dc2229d493`  
		Last Modified: Tue, 31 Mar 2020 02:12:15 GMT  
		Size: 25.9 MB (25851645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72560398e0dc8991a53cd07c580b14e3c2024d7af30d2dfe8428d913006af5a9`  
		Last Modified: Tue, 31 Mar 2020 08:48:55 GMT  
		Size: 5.0 KB (5028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4febdbdc3565b2d569ed0a6885c548a5755cd9a2b52c21b351d254c83e6fff7`  
		Last Modified: Tue, 31 Mar 2020 08:48:55 GMT  
		Size: 2.1 MB (2074952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8266bd2499012e842778a6e03cccde2b97d44f659ebbfcd1a69eccc22d1bc3a`  
		Last Modified: Tue, 14 Apr 2020 00:07:33 GMT  
		Size: 1.2 MB (1162903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99b2bf34e46eab97471c453efd6d739d3d6f3de32789d23cf81e6eaa94d2ea6e`  
		Last Modified: Tue, 14 Apr 2020 00:07:33 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1a5e887fbf0bacccd7a723d6c972e22f49e6cdbbdc0d5156f127d8e5507717b`  
		Last Modified: Tue, 14 Apr 2020 00:07:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.5` - linux; 386

```console
$ docker pull memcached@sha256:f77cbe58b76a6763ebbacbb8d9a53c9705b0f1784d50261627ea7148225a53b4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31156720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06a5671f4598de98b696abbd0eaee1875af3cf8d5825a2c079f751054a79a319`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 31 Mar 2020 00:39:42 GMT
ADD file:a453117866661af4ddfa21203d65ce6661efeaeca2a1704e09747c83b4c58e47 in / 
# Tue, 31 Mar 2020 00:39:42 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 11:45:29 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 31 Mar 2020 11:45:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 Apr 2020 00:15:39 GMT
ENV MEMCACHED_VERSION=1.6.5
# Tue, 14 Apr 2020 00:15:40 GMT
ENV MEMCACHED_SHA1=1ddb5f37f69946b63512ad0f89dc448ff7ba5713
# Tue, 14 Apr 2020 00:24:13 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 14 Apr 2020 00:24:13 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 14 Apr 2020 00:24:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 14 Apr 2020 00:24:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2020 00:24:14 GMT
USER memcache
# Tue, 14 Apr 2020 00:24:14 GMT
EXPOSE 11211
# Tue, 14 Apr 2020 00:24:15 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2314106a15e49c7908bebb2c697dcaf3d6a1626b70fe72bc0c0cb71eb216ddc3`  
		Last Modified: Tue, 31 Mar 2020 00:45:31 GMT  
		Size: 27.7 MB (27747648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3bafab0976764495dda52d0c16addb4770d62d8f9de55728b752ff3448f2292`  
		Last Modified: Tue, 31 Mar 2020 11:55:29 GMT  
		Size: 4.9 KB (4899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8307e5e61ebc9ed2430c9e45ba3437aa1deebed0882ce15c36616e0debf28b36`  
		Last Modified: Tue, 31 Mar 2020 11:55:29 GMT  
		Size: 2.2 MB (2208079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1a1a09da032c7622fe0330fa14876496b04b5e9e81943f09df1b315bec0a4d`  
		Last Modified: Tue, 14 Apr 2020 00:33:22 GMT  
		Size: 1.2 MB (1195686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80e37d2af038355acfb8af6aca4e4cb3a65c0d08aaab7723c1987d1006fbf17b`  
		Last Modified: Tue, 14 Apr 2020 00:33:21 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ec8103e2aa301996d108c97a0d120cdc72d11519b4269350d4d72c026e919d`  
		Last Modified: Tue, 14 Apr 2020 00:33:21 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.5` - linux; ppc64le

```console
$ docker pull memcached@sha256:b587e1ac02d9b43b4dc13af7294b8f81a5e638b13c981743a1ffb2798c733976
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.1 MB (34064242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8704abb1ba80a90926fd4cc6cb9e20c5f3624763df555561a961411766e635a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 31 Mar 2020 01:32:42 GMT
ADD file:36c02e92574faba45b64cfed78a0a0359d65ad175b17128bf554a2a5c0086ff5 in / 
# Tue, 31 Mar 2020 01:32:47 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 12:45:58 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 31 Mar 2020 12:46:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 Apr 2020 00:29:39 GMT
ENV MEMCACHED_VERSION=1.6.5
# Tue, 14 Apr 2020 00:29:44 GMT
ENV MEMCACHED_SHA1=1ddb5f37f69946b63512ad0f89dc448ff7ba5713
# Tue, 14 Apr 2020 00:41:15 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 14 Apr 2020 00:41:17 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 14 Apr 2020 00:41:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 14 Apr 2020 00:41:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2020 00:41:38 GMT
USER memcache
# Tue, 14 Apr 2020 00:41:45 GMT
EXPOSE 11211
# Tue, 14 Apr 2020 00:41:51 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9df6bbae5eeb29e9aac2f39cff517c694cce60f01ee477abcdedcd8e8c01c38f`  
		Last Modified: Tue, 31 Mar 2020 01:45:59 GMT  
		Size: 30.5 MB (30518493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2786c1a6fbad6e8c56e4f7e33b4d41c64efd06c4cdb303a50c07ee1f4c5f7a69`  
		Last Modified: Tue, 31 Mar 2020 12:58:00 GMT  
		Size: 5.0 KB (4987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:722cfb50c03533f4b5c83c84a2f565dbcdbf63c01460ae91d35aafacd94454fe`  
		Last Modified: Tue, 31 Mar 2020 12:58:00 GMT  
		Size: 2.3 MB (2322647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec1b5923ebd47cd1e2443a1ff44899de7b683eadb673d9404c7c259b96277c7d`  
		Last Modified: Tue, 14 Apr 2020 00:51:37 GMT  
		Size: 1.2 MB (1217708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3311546eb5856360dd803bbb0e75a832bef2fb729dce22a03be0656ebbcec2f4`  
		Last Modified: Tue, 14 Apr 2020 00:51:36 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5646db67b9fcecdc7d9a2c867f4515d81b3f3e429cbcb5b3804420a392b277ae`  
		Last Modified: Tue, 14 Apr 2020 00:51:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:1.6.5-alpine`

```console
$ docker pull memcached@sha256:78d45793a30eaf096f2fa83ee213871e2dab005f7d7ac82c0b8fa5a59b27113c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `memcached:1.6.5-alpine` - linux; amd64

```console
$ docker pull memcached@sha256:42f3c2aa162185e3c8bef259444e2211072916dcd0ea1e3a97ebc40063565c82
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4371887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acce7f7ac2ef3283ff7538edb59d788e12a173e6c988e8142eda78a9d7d465f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 00:40:06 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Tue, 24 Mar 2020 00:40:07 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Tue, 14 Apr 2020 00:28:07 GMT
ENV MEMCACHED_VERSION=1.6.5
# Tue, 14 Apr 2020 00:28:08 GMT
ENV MEMCACHED_SHA1=1ddb5f37f69946b63512ad0f89dc448ff7ba5713
# Tue, 14 Apr 2020 00:36:24 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 14 Apr 2020 00:36:25 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 14 Apr 2020 00:36:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 14 Apr 2020 00:36:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2020 00:36:26 GMT
USER memcache
# Tue, 14 Apr 2020 00:36:26 GMT
EXPOSE 11211
# Tue, 14 Apr 2020 00:36:26 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a5fb4ad400df404c486089fa4098e9e6bfdb1528c2ee85cbd5614e8a97f1f9a`  
		Last Modified: Tue, 24 Mar 2020 00:48:55 GMT  
		Size: 1.2 KB (1230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb602a49f6f4777651777faab36b80d92a2f1dbe36d865c0cce4e182439c6b5e`  
		Last Modified: Tue, 24 Mar 2020 00:48:55 GMT  
		Size: 15.1 KB (15099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2ad92cd017e016358bcdd19608005e61b96f391f551cbf28b7bf893eb08f27`  
		Last Modified: Tue, 14 Apr 2020 00:36:52 GMT  
		Size: 1.6 MB (1551900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c47c68edd2b2740171a4efac506979aa590d59657cda2b828522131128a70e68`  
		Last Modified: Tue, 14 Apr 2020 00:36:52 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a4b5b784c11b1f78e28ec0cee292cd3ab2e91add940930435cbe73099221381`  
		Last Modified: Tue, 14 Apr 2020 00:36:52 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.5-alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:2ad889e13d889d0a7bf42350cd8f4de4e63c14a935ed4eca89c15c22b650caf4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4148874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eebd4fa55e8dcf85c1736ab25138f0a2299ec97c84043b1a8893798172fcb5ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Mar 2020 21:49:26 GMT
ADD file:e2fdfc637b534345942caf4097883508a5ed23be97d85ccc3357b8277aaa5430 in / 
# Mon, 23 Mar 2020 21:49:27 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 23:15:28 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Mon, 23 Mar 2020 23:15:34 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Mon, 13 Apr 2020 23:51:16 GMT
ENV MEMCACHED_VERSION=1.6.5
# Mon, 13 Apr 2020 23:51:17 GMT
ENV MEMCACHED_SHA1=1ddb5f37f69946b63512ad0f89dc448ff7ba5713
# Tue, 14 Apr 2020 00:00:39 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 14 Apr 2020 00:00:40 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 14 Apr 2020 00:00:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 14 Apr 2020 00:00:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2020 00:00:42 GMT
USER memcache
# Tue, 14 Apr 2020 00:00:43 GMT
EXPOSE 11211
# Tue, 14 Apr 2020 00:00:44 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0776aeec3430c5a5ba3f43937f0ee6a7770a1fe81a318c9d94cc76512e5375e9`  
		Last Modified: Mon, 23 Mar 2020 21:49:50 GMT  
		Size: 2.6 MB (2618579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f329bb895b7588f4de54c119f39a5f656520bc2310d39893460c4398814112d`  
		Last Modified: Mon, 23 Mar 2020 23:25:38 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6bd8017eeb8ecce1d6b238f86b96a1af52d1a9dd44bc0da4c0573f58a7f51a8`  
		Last Modified: Mon, 23 Mar 2020 23:25:38 GMT  
		Size: 14.7 KB (14695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed1dbd69370c1c1fd0f473abbd0890a314699b93feb4e9a9397ad89e6f4d08e8`  
		Last Modified: Tue, 14 Apr 2020 00:01:00 GMT  
		Size: 1.5 MB (1513938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02da716a305370dd20bed73237b26c6686af6bb314c1730ca4b677e6b192948c`  
		Last Modified: Tue, 14 Apr 2020 00:01:01 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5a3d551b55e52c8a515a9331168aca21b6fa779ec12e67e0212eb263adeebda`  
		Last Modified: Tue, 14 Apr 2020 00:01:01 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.5-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:08e4eee2dbc1e2589c53c0bbd26363957880c8563d31786d877d09ec516c0fed
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4294422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e0270dfda3dfe68de5b0bb5335b0930004ca3beed72eca0def0c03de87601b0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Mar 2020 21:39:52 GMT
ADD file:746a5c3838a898d6acf7877552ff13d1ab40d0036ace7a662e7c747018315ddb in / 
# Mon, 23 Mar 2020 21:39:53 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 05:16:12 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Tue, 24 Mar 2020 05:16:15 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Mon, 13 Apr 2020 23:57:43 GMT
ENV MEMCACHED_VERSION=1.6.5
# Mon, 13 Apr 2020 23:57:44 GMT
ENV MEMCACHED_SHA1=1ddb5f37f69946b63512ad0f89dc448ff7ba5713
# Tue, 14 Apr 2020 00:06:55 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 14 Apr 2020 00:06:56 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 14 Apr 2020 00:06:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 14 Apr 2020 00:06:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2020 00:07:00 GMT
USER memcache
# Tue, 14 Apr 2020 00:07:01 GMT
EXPOSE 11211
# Tue, 14 Apr 2020 00:07:02 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8a0637ca1ac98db4cf29f7632449c92801adc80cf0da2cd9c9e39882ce466561`  
		Last Modified: Mon, 23 Mar 2020 21:40:19 GMT  
		Size: 2.7 MB (2723139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd1bfe9c2142f88c6e142b39adf7ba4fe722789b650d5a54184ff336826ae16f`  
		Last Modified: Tue, 24 Mar 2020 05:25:36 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f4d8154a8d6d9edf61516528f99c62d27eb41f8602571ae30fdf745976e2c6e`  
		Last Modified: Tue, 24 Mar 2020 05:25:35 GMT  
		Size: 15.5 KB (15490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5d54c7f7d9fb444dbe1aee28da7f339cfce0f93316d0e44b528e3f0b1c83a1e`  
		Last Modified: Tue, 14 Apr 2020 00:07:42 GMT  
		Size: 1.6 MB (1554129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2824223b1a0565c7df241643aa6173bcc7f918bd51af6cd082f1c4dd56375a79`  
		Last Modified: Tue, 14 Apr 2020 00:07:42 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b98391dc8eb3d7e32edcd1175b80a1588f44e5c9c8f93e0d7d35697e93f67fb`  
		Last Modified: Tue, 14 Apr 2020 00:07:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.5-alpine` - linux; 386

```console
$ docker pull memcached@sha256:788ec77b1bd7a21665769b8e4302e8978c324953b48e09aeb17b41e80e20c5f0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4472337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7638872a17e59e75a022dc0c1a0a16cbe719fb3b5503003e4a7110ff97fca043`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Mar 2020 21:38:28 GMT
ADD file:99c8234abafd4fa915c0b826eb0e3be0e6aaa7c1e33cb1214ef71a99e9c02e06 in / 
# Mon, 23 Mar 2020 21:38:28 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 04:55:12 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Tue, 24 Mar 2020 04:55:13 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Tue, 14 Apr 2020 00:24:28 GMT
ENV MEMCACHED_VERSION=1.6.5
# Tue, 14 Apr 2020 00:24:29 GMT
ENV MEMCACHED_SHA1=1ddb5f37f69946b63512ad0f89dc448ff7ba5713
# Tue, 14 Apr 2020 00:33:02 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 14 Apr 2020 00:33:02 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 14 Apr 2020 00:33:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 14 Apr 2020 00:33:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2020 00:33:03 GMT
USER memcache
# Tue, 14 Apr 2020 00:33:03 GMT
EXPOSE 11211
# Tue, 14 Apr 2020 00:33:03 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:43f6a4398e1c9e860dfb5c93d7049ab9eedf814513bd6d07e06077c560303c7a`  
		Last Modified: Mon, 23 Mar 2020 21:38:48 GMT  
		Size: 2.8 MB (2806122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a31d073afa8dea3b0bfd6eeb6ebffc6447996f0e9cabebf9d749474ac22cdf2d`  
		Last Modified: Tue, 24 Mar 2020 05:04:58 GMT  
		Size: 1.2 KB (1230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:905909a3db778acdf7295903cff6ee7b27263e33facc5982475e7b60831413fc`  
		Last Modified: Tue, 24 Mar 2020 05:04:58 GMT  
		Size: 16.1 KB (16146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e55f704c4db8d5686c61a7f5dbf01efb54c26f928a4667edb336aa6b26c9931`  
		Last Modified: Tue, 14 Apr 2020 00:33:27 GMT  
		Size: 1.6 MB (1648434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85df688f5f46cdef50f778015f724036d02ef66baf23dee71b4f2021a38784bc`  
		Last Modified: Tue, 14 Apr 2020 00:33:27 GMT  
		Size: 284.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e187a846d19d6476ac11efbcb749911f8f31990824f548f8b22ac752a1218a`  
		Last Modified: Tue, 14 Apr 2020 00:33:27 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.5-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:3797459b34cdce19dc5c399b9c197be9e7ba49a5f24eb0519aafb09597505922
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4448507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf7465343178ddd65e795fcbffde4546ce34a20537d50c03bf12dc86eb96e1e0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Mar 2020 21:21:29 GMT
ADD file:4b35131542b9682214e1c2c72fe3cea215a10e2f775e87befecd80fe2228d5a0 in / 
# Mon, 23 Mar 2020 21:21:32 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 02:24:20 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Tue, 24 Mar 2020 02:24:25 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Tue, 14 Apr 2020 00:42:05 GMT
ENV MEMCACHED_VERSION=1.6.5
# Tue, 14 Apr 2020 00:42:08 GMT
ENV MEMCACHED_SHA1=1ddb5f37f69946b63512ad0f89dc448ff7ba5713
# Tue, 14 Apr 2020 00:50:46 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 14 Apr 2020 00:50:47 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 14 Apr 2020 00:51:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 14 Apr 2020 00:51:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2020 00:51:11 GMT
USER memcache
# Tue, 14 Apr 2020 00:51:15 GMT
EXPOSE 11211
# Tue, 14 Apr 2020 00:51:17 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bc1c99f4ba60de0d3ca52dc6855483e24c91884e33df71f502bbff6eb909d9b9`  
		Last Modified: Mon, 23 Mar 2020 21:22:12 GMT  
		Size: 2.8 MB (2820052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50bd2ca891d67079878bf06e36ba609e8528e83369265c92fbd3b03e6e839f1`  
		Last Modified: Tue, 24 Mar 2020 02:34:02 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a4704e4e496c0d18b40f484fc715146c1f427050210b40271112edcf751a698`  
		Last Modified: Tue, 24 Mar 2020 02:34:02 GMT  
		Size: 16.1 KB (16131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a082e2e1ac7786e3860912de8517980c8e08afb1ffa80d05d52240fbb673698`  
		Last Modified: Tue, 14 Apr 2020 00:51:52 GMT  
		Size: 1.6 MB (1610653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b1bdbb7103a9b4c5d777d6f23357bc31745b28dba327fa333173e2306e8ba5c`  
		Last Modified: Tue, 14 Apr 2020 00:51:51 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a958ecfb0c40b2251cf63426a688c563e8432efc39006acc5192e8fe59b23ab`  
		Last Modified: Tue, 14 Apr 2020 00:51:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:1.6-alpine`

```console
$ docker pull memcached@sha256:2ab5d68564c85ce4f9d953ea4afe4379894dda80c7b30785963a626fa2acad33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `memcached:1.6-alpine` - linux; amd64

```console
$ docker pull memcached@sha256:42f3c2aa162185e3c8bef259444e2211072916dcd0ea1e3a97ebc40063565c82
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4371887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acce7f7ac2ef3283ff7538edb59d788e12a173e6c988e8142eda78a9d7d465f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 00:40:06 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Tue, 24 Mar 2020 00:40:07 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Tue, 14 Apr 2020 00:28:07 GMT
ENV MEMCACHED_VERSION=1.6.5
# Tue, 14 Apr 2020 00:28:08 GMT
ENV MEMCACHED_SHA1=1ddb5f37f69946b63512ad0f89dc448ff7ba5713
# Tue, 14 Apr 2020 00:36:24 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 14 Apr 2020 00:36:25 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 14 Apr 2020 00:36:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 14 Apr 2020 00:36:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2020 00:36:26 GMT
USER memcache
# Tue, 14 Apr 2020 00:36:26 GMT
EXPOSE 11211
# Tue, 14 Apr 2020 00:36:26 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a5fb4ad400df404c486089fa4098e9e6bfdb1528c2ee85cbd5614e8a97f1f9a`  
		Last Modified: Tue, 24 Mar 2020 00:48:55 GMT  
		Size: 1.2 KB (1230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb602a49f6f4777651777faab36b80d92a2f1dbe36d865c0cce4e182439c6b5e`  
		Last Modified: Tue, 24 Mar 2020 00:48:55 GMT  
		Size: 15.1 KB (15099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2ad92cd017e016358bcdd19608005e61b96f391f551cbf28b7bf893eb08f27`  
		Last Modified: Tue, 14 Apr 2020 00:36:52 GMT  
		Size: 1.6 MB (1551900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c47c68edd2b2740171a4efac506979aa590d59657cda2b828522131128a70e68`  
		Last Modified: Tue, 14 Apr 2020 00:36:52 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a4b5b784c11b1f78e28ec0cee292cd3ab2e91add940930435cbe73099221381`  
		Last Modified: Tue, 14 Apr 2020 00:36:52 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6-alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:2ad889e13d889d0a7bf42350cd8f4de4e63c14a935ed4eca89c15c22b650caf4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4148874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eebd4fa55e8dcf85c1736ab25138f0a2299ec97c84043b1a8893798172fcb5ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Mar 2020 21:49:26 GMT
ADD file:e2fdfc637b534345942caf4097883508a5ed23be97d85ccc3357b8277aaa5430 in / 
# Mon, 23 Mar 2020 21:49:27 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 23:15:28 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Mon, 23 Mar 2020 23:15:34 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Mon, 13 Apr 2020 23:51:16 GMT
ENV MEMCACHED_VERSION=1.6.5
# Mon, 13 Apr 2020 23:51:17 GMT
ENV MEMCACHED_SHA1=1ddb5f37f69946b63512ad0f89dc448ff7ba5713
# Tue, 14 Apr 2020 00:00:39 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 14 Apr 2020 00:00:40 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 14 Apr 2020 00:00:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 14 Apr 2020 00:00:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2020 00:00:42 GMT
USER memcache
# Tue, 14 Apr 2020 00:00:43 GMT
EXPOSE 11211
# Tue, 14 Apr 2020 00:00:44 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0776aeec3430c5a5ba3f43937f0ee6a7770a1fe81a318c9d94cc76512e5375e9`  
		Last Modified: Mon, 23 Mar 2020 21:49:50 GMT  
		Size: 2.6 MB (2618579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f329bb895b7588f4de54c119f39a5f656520bc2310d39893460c4398814112d`  
		Last Modified: Mon, 23 Mar 2020 23:25:38 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6bd8017eeb8ecce1d6b238f86b96a1af52d1a9dd44bc0da4c0573f58a7f51a8`  
		Last Modified: Mon, 23 Mar 2020 23:25:38 GMT  
		Size: 14.7 KB (14695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed1dbd69370c1c1fd0f473abbd0890a314699b93feb4e9a9397ad89e6f4d08e8`  
		Last Modified: Tue, 14 Apr 2020 00:01:00 GMT  
		Size: 1.5 MB (1513938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02da716a305370dd20bed73237b26c6686af6bb314c1730ca4b677e6b192948c`  
		Last Modified: Tue, 14 Apr 2020 00:01:01 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5a3d551b55e52c8a515a9331168aca21b6fa779ec12e67e0212eb263adeebda`  
		Last Modified: Tue, 14 Apr 2020 00:01:01 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6-alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:ec8c62ad113b358298092e63b474e8aeebb5b1e1bfabb2e6ff525646dc7458f1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3826282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5af1281a25c9479c7ad3e80e07f3e7b43e774841795c9f93004bf124abe4b0f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Mar 2020 21:57:55 GMT
ADD file:3bde6b6fd06efbf24e66446c6d32f72294fc749ae9ee6191776242e92b2f8ab4 in / 
# Mon, 23 Mar 2020 21:57:56 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:14:07 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Mon, 23 Mar 2020 22:14:20 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Tue, 24 Mar 2020 01:47:18 GMT
ENV MEMCACHED_VERSION=1.6.2
# Tue, 24 Mar 2020 01:47:22 GMT
ENV MEMCACHED_SHA1=a6a07f0433adaa13a3cafdf8c26acb640cdd001f
# Tue, 24 Mar 2020 03:19:47 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 24 Mar 2020 03:19:50 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 24 Mar 2020 03:20:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 24 Mar 2020 03:20:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2020 03:20:05 GMT
USER memcache
# Tue, 24 Mar 2020 03:20:07 GMT
EXPOSE 11211
# Tue, 24 Mar 2020 03:20:09 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d9bf605ce3d4449f4b90035c3e21d691806324781d43a5287b1da25a01779d6b`  
		Last Modified: Mon, 23 Mar 2020 21:58:16 GMT  
		Size: 2.4 MB (2420493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae54837c45cf98e10469ba87b255979740486d00d9407bc2fcdf1492469dc04`  
		Last Modified: Mon, 23 Mar 2020 22:42:38 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1459ca388d9e53a94cbb39e64789568710013f3b46396b24ea0729b570f74403`  
		Last Modified: Mon, 23 Mar 2020 22:42:44 GMT  
		Size: 13.6 KB (13638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f84775e4ae618e04e599d46af2006e35d62d9046f4908e660cc533b9cbb8c36`  
		Last Modified: Tue, 24 Mar 2020 03:21:11 GMT  
		Size: 1.4 MB (1390486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dd59b3062e02dcff6cd6cbe35ba1e84c44a571112a65c4dd0ad640b905e4ae3`  
		Last Modified: Tue, 24 Mar 2020 03:21:09 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f53094e3dbce9c8d482bfb7123a06c9a0e4e74102891a4aecc833167acbb64db`  
		Last Modified: Tue, 24 Mar 2020 03:21:15 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:08e4eee2dbc1e2589c53c0bbd26363957880c8563d31786d877d09ec516c0fed
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4294422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e0270dfda3dfe68de5b0bb5335b0930004ca3beed72eca0def0c03de87601b0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Mar 2020 21:39:52 GMT
ADD file:746a5c3838a898d6acf7877552ff13d1ab40d0036ace7a662e7c747018315ddb in / 
# Mon, 23 Mar 2020 21:39:53 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 05:16:12 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Tue, 24 Mar 2020 05:16:15 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Mon, 13 Apr 2020 23:57:43 GMT
ENV MEMCACHED_VERSION=1.6.5
# Mon, 13 Apr 2020 23:57:44 GMT
ENV MEMCACHED_SHA1=1ddb5f37f69946b63512ad0f89dc448ff7ba5713
# Tue, 14 Apr 2020 00:06:55 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 14 Apr 2020 00:06:56 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 14 Apr 2020 00:06:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 14 Apr 2020 00:06:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2020 00:07:00 GMT
USER memcache
# Tue, 14 Apr 2020 00:07:01 GMT
EXPOSE 11211
# Tue, 14 Apr 2020 00:07:02 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8a0637ca1ac98db4cf29f7632449c92801adc80cf0da2cd9c9e39882ce466561`  
		Last Modified: Mon, 23 Mar 2020 21:40:19 GMT  
		Size: 2.7 MB (2723139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd1bfe9c2142f88c6e142b39adf7ba4fe722789b650d5a54184ff336826ae16f`  
		Last Modified: Tue, 24 Mar 2020 05:25:36 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f4d8154a8d6d9edf61516528f99c62d27eb41f8602571ae30fdf745976e2c6e`  
		Last Modified: Tue, 24 Mar 2020 05:25:35 GMT  
		Size: 15.5 KB (15490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5d54c7f7d9fb444dbe1aee28da7f339cfce0f93316d0e44b528e3f0b1c83a1e`  
		Last Modified: Tue, 14 Apr 2020 00:07:42 GMT  
		Size: 1.6 MB (1554129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2824223b1a0565c7df241643aa6173bcc7f918bd51af6cd082f1c4dd56375a79`  
		Last Modified: Tue, 14 Apr 2020 00:07:42 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b98391dc8eb3d7e32edcd1175b80a1588f44e5c9c8f93e0d7d35697e93f67fb`  
		Last Modified: Tue, 14 Apr 2020 00:07:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6-alpine` - linux; 386

```console
$ docker pull memcached@sha256:788ec77b1bd7a21665769b8e4302e8978c324953b48e09aeb17b41e80e20c5f0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4472337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7638872a17e59e75a022dc0c1a0a16cbe719fb3b5503003e4a7110ff97fca043`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Mar 2020 21:38:28 GMT
ADD file:99c8234abafd4fa915c0b826eb0e3be0e6aaa7c1e33cb1214ef71a99e9c02e06 in / 
# Mon, 23 Mar 2020 21:38:28 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 04:55:12 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Tue, 24 Mar 2020 04:55:13 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Tue, 14 Apr 2020 00:24:28 GMT
ENV MEMCACHED_VERSION=1.6.5
# Tue, 14 Apr 2020 00:24:29 GMT
ENV MEMCACHED_SHA1=1ddb5f37f69946b63512ad0f89dc448ff7ba5713
# Tue, 14 Apr 2020 00:33:02 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 14 Apr 2020 00:33:02 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 14 Apr 2020 00:33:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 14 Apr 2020 00:33:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2020 00:33:03 GMT
USER memcache
# Tue, 14 Apr 2020 00:33:03 GMT
EXPOSE 11211
# Tue, 14 Apr 2020 00:33:03 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:43f6a4398e1c9e860dfb5c93d7049ab9eedf814513bd6d07e06077c560303c7a`  
		Last Modified: Mon, 23 Mar 2020 21:38:48 GMT  
		Size: 2.8 MB (2806122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a31d073afa8dea3b0bfd6eeb6ebffc6447996f0e9cabebf9d749474ac22cdf2d`  
		Last Modified: Tue, 24 Mar 2020 05:04:58 GMT  
		Size: 1.2 KB (1230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:905909a3db778acdf7295903cff6ee7b27263e33facc5982475e7b60831413fc`  
		Last Modified: Tue, 24 Mar 2020 05:04:58 GMT  
		Size: 16.1 KB (16146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e55f704c4db8d5686c61a7f5dbf01efb54c26f928a4667edb336aa6b26c9931`  
		Last Modified: Tue, 14 Apr 2020 00:33:27 GMT  
		Size: 1.6 MB (1648434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85df688f5f46cdef50f778015f724036d02ef66baf23dee71b4f2021a38784bc`  
		Last Modified: Tue, 14 Apr 2020 00:33:27 GMT  
		Size: 284.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e187a846d19d6476ac11efbcb749911f8f31990824f548f8b22ac752a1218a`  
		Last Modified: Tue, 14 Apr 2020 00:33:27 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:3797459b34cdce19dc5c399b9c197be9e7ba49a5f24eb0519aafb09597505922
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4448507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf7465343178ddd65e795fcbffde4546ce34a20537d50c03bf12dc86eb96e1e0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Mar 2020 21:21:29 GMT
ADD file:4b35131542b9682214e1c2c72fe3cea215a10e2f775e87befecd80fe2228d5a0 in / 
# Mon, 23 Mar 2020 21:21:32 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 02:24:20 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Tue, 24 Mar 2020 02:24:25 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Tue, 14 Apr 2020 00:42:05 GMT
ENV MEMCACHED_VERSION=1.6.5
# Tue, 14 Apr 2020 00:42:08 GMT
ENV MEMCACHED_SHA1=1ddb5f37f69946b63512ad0f89dc448ff7ba5713
# Tue, 14 Apr 2020 00:50:46 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 14 Apr 2020 00:50:47 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 14 Apr 2020 00:51:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 14 Apr 2020 00:51:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2020 00:51:11 GMT
USER memcache
# Tue, 14 Apr 2020 00:51:15 GMT
EXPOSE 11211
# Tue, 14 Apr 2020 00:51:17 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bc1c99f4ba60de0d3ca52dc6855483e24c91884e33df71f502bbff6eb909d9b9`  
		Last Modified: Mon, 23 Mar 2020 21:22:12 GMT  
		Size: 2.8 MB (2820052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50bd2ca891d67079878bf06e36ba609e8528e83369265c92fbd3b03e6e839f1`  
		Last Modified: Tue, 24 Mar 2020 02:34:02 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a4704e4e496c0d18b40f484fc715146c1f427050210b40271112edcf751a698`  
		Last Modified: Tue, 24 Mar 2020 02:34:02 GMT  
		Size: 16.1 KB (16131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a082e2e1ac7786e3860912de8517980c8e08afb1ffa80d05d52240fbb673698`  
		Last Modified: Tue, 14 Apr 2020 00:51:52 GMT  
		Size: 1.6 MB (1610653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b1bdbb7103a9b4c5d777d6f23357bc31745b28dba327fa333173e2306e8ba5c`  
		Last Modified: Tue, 14 Apr 2020 00:51:51 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a958ecfb0c40b2251cf63426a688c563e8432efc39006acc5192e8fe59b23ab`  
		Last Modified: Tue, 14 Apr 2020 00:51:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:1-alpine`

```console
$ docker pull memcached@sha256:7053af573b42ea8ed1028f4d942f6e950259d9cf0bca2b7c9e1680a2b26cd485
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
$ docker pull memcached@sha256:42f3c2aa162185e3c8bef259444e2211072916dcd0ea1e3a97ebc40063565c82
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4371887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acce7f7ac2ef3283ff7538edb59d788e12a173e6c988e8142eda78a9d7d465f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 00:40:06 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Tue, 24 Mar 2020 00:40:07 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Tue, 14 Apr 2020 00:28:07 GMT
ENV MEMCACHED_VERSION=1.6.5
# Tue, 14 Apr 2020 00:28:08 GMT
ENV MEMCACHED_SHA1=1ddb5f37f69946b63512ad0f89dc448ff7ba5713
# Tue, 14 Apr 2020 00:36:24 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 14 Apr 2020 00:36:25 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 14 Apr 2020 00:36:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 14 Apr 2020 00:36:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2020 00:36:26 GMT
USER memcache
# Tue, 14 Apr 2020 00:36:26 GMT
EXPOSE 11211
# Tue, 14 Apr 2020 00:36:26 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a5fb4ad400df404c486089fa4098e9e6bfdb1528c2ee85cbd5614e8a97f1f9a`  
		Last Modified: Tue, 24 Mar 2020 00:48:55 GMT  
		Size: 1.2 KB (1230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb602a49f6f4777651777faab36b80d92a2f1dbe36d865c0cce4e182439c6b5e`  
		Last Modified: Tue, 24 Mar 2020 00:48:55 GMT  
		Size: 15.1 KB (15099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2ad92cd017e016358bcdd19608005e61b96f391f551cbf28b7bf893eb08f27`  
		Last Modified: Tue, 14 Apr 2020 00:36:52 GMT  
		Size: 1.6 MB (1551900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c47c68edd2b2740171a4efac506979aa590d59657cda2b828522131128a70e68`  
		Last Modified: Tue, 14 Apr 2020 00:36:52 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a4b5b784c11b1f78e28ec0cee292cd3ab2e91add940930435cbe73099221381`  
		Last Modified: Tue, 14 Apr 2020 00:36:52 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:2ad889e13d889d0a7bf42350cd8f4de4e63c14a935ed4eca89c15c22b650caf4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4148874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eebd4fa55e8dcf85c1736ab25138f0a2299ec97c84043b1a8893798172fcb5ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Mar 2020 21:49:26 GMT
ADD file:e2fdfc637b534345942caf4097883508a5ed23be97d85ccc3357b8277aaa5430 in / 
# Mon, 23 Mar 2020 21:49:27 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 23:15:28 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Mon, 23 Mar 2020 23:15:34 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Mon, 13 Apr 2020 23:51:16 GMT
ENV MEMCACHED_VERSION=1.6.5
# Mon, 13 Apr 2020 23:51:17 GMT
ENV MEMCACHED_SHA1=1ddb5f37f69946b63512ad0f89dc448ff7ba5713
# Tue, 14 Apr 2020 00:00:39 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 14 Apr 2020 00:00:40 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 14 Apr 2020 00:00:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 14 Apr 2020 00:00:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2020 00:00:42 GMT
USER memcache
# Tue, 14 Apr 2020 00:00:43 GMT
EXPOSE 11211
# Tue, 14 Apr 2020 00:00:44 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0776aeec3430c5a5ba3f43937f0ee6a7770a1fe81a318c9d94cc76512e5375e9`  
		Last Modified: Mon, 23 Mar 2020 21:49:50 GMT  
		Size: 2.6 MB (2618579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f329bb895b7588f4de54c119f39a5f656520bc2310d39893460c4398814112d`  
		Last Modified: Mon, 23 Mar 2020 23:25:38 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6bd8017eeb8ecce1d6b238f86b96a1af52d1a9dd44bc0da4c0573f58a7f51a8`  
		Last Modified: Mon, 23 Mar 2020 23:25:38 GMT  
		Size: 14.7 KB (14695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed1dbd69370c1c1fd0f473abbd0890a314699b93feb4e9a9397ad89e6f4d08e8`  
		Last Modified: Tue, 14 Apr 2020 00:01:00 GMT  
		Size: 1.5 MB (1513938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02da716a305370dd20bed73237b26c6686af6bb314c1730ca4b677e6b192948c`  
		Last Modified: Tue, 14 Apr 2020 00:01:01 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5a3d551b55e52c8a515a9331168aca21b6fa779ec12e67e0212eb263adeebda`  
		Last Modified: Tue, 14 Apr 2020 00:01:01 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:ec8c62ad113b358298092e63b474e8aeebb5b1e1bfabb2e6ff525646dc7458f1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3826282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5af1281a25c9479c7ad3e80e07f3e7b43e774841795c9f93004bf124abe4b0f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Mar 2020 21:57:55 GMT
ADD file:3bde6b6fd06efbf24e66446c6d32f72294fc749ae9ee6191776242e92b2f8ab4 in / 
# Mon, 23 Mar 2020 21:57:56 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:14:07 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Mon, 23 Mar 2020 22:14:20 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Tue, 24 Mar 2020 01:47:18 GMT
ENV MEMCACHED_VERSION=1.6.2
# Tue, 24 Mar 2020 01:47:22 GMT
ENV MEMCACHED_SHA1=a6a07f0433adaa13a3cafdf8c26acb640cdd001f
# Tue, 24 Mar 2020 03:19:47 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 24 Mar 2020 03:19:50 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 24 Mar 2020 03:20:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 24 Mar 2020 03:20:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2020 03:20:05 GMT
USER memcache
# Tue, 24 Mar 2020 03:20:07 GMT
EXPOSE 11211
# Tue, 24 Mar 2020 03:20:09 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d9bf605ce3d4449f4b90035c3e21d691806324781d43a5287b1da25a01779d6b`  
		Last Modified: Mon, 23 Mar 2020 21:58:16 GMT  
		Size: 2.4 MB (2420493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae54837c45cf98e10469ba87b255979740486d00d9407bc2fcdf1492469dc04`  
		Last Modified: Mon, 23 Mar 2020 22:42:38 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1459ca388d9e53a94cbb39e64789568710013f3b46396b24ea0729b570f74403`  
		Last Modified: Mon, 23 Mar 2020 22:42:44 GMT  
		Size: 13.6 KB (13638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f84775e4ae618e04e599d46af2006e35d62d9046f4908e660cc533b9cbb8c36`  
		Last Modified: Tue, 24 Mar 2020 03:21:11 GMT  
		Size: 1.4 MB (1390486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dd59b3062e02dcff6cd6cbe35ba1e84c44a571112a65c4dd0ad640b905e4ae3`  
		Last Modified: Tue, 24 Mar 2020 03:21:09 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f53094e3dbce9c8d482bfb7123a06c9a0e4e74102891a4aecc833167acbb64db`  
		Last Modified: Tue, 24 Mar 2020 03:21:15 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:08e4eee2dbc1e2589c53c0bbd26363957880c8563d31786d877d09ec516c0fed
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4294422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e0270dfda3dfe68de5b0bb5335b0930004ca3beed72eca0def0c03de87601b0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Mar 2020 21:39:52 GMT
ADD file:746a5c3838a898d6acf7877552ff13d1ab40d0036ace7a662e7c747018315ddb in / 
# Mon, 23 Mar 2020 21:39:53 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 05:16:12 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Tue, 24 Mar 2020 05:16:15 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Mon, 13 Apr 2020 23:57:43 GMT
ENV MEMCACHED_VERSION=1.6.5
# Mon, 13 Apr 2020 23:57:44 GMT
ENV MEMCACHED_SHA1=1ddb5f37f69946b63512ad0f89dc448ff7ba5713
# Tue, 14 Apr 2020 00:06:55 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 14 Apr 2020 00:06:56 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 14 Apr 2020 00:06:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 14 Apr 2020 00:06:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2020 00:07:00 GMT
USER memcache
# Tue, 14 Apr 2020 00:07:01 GMT
EXPOSE 11211
# Tue, 14 Apr 2020 00:07:02 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8a0637ca1ac98db4cf29f7632449c92801adc80cf0da2cd9c9e39882ce466561`  
		Last Modified: Mon, 23 Mar 2020 21:40:19 GMT  
		Size: 2.7 MB (2723139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd1bfe9c2142f88c6e142b39adf7ba4fe722789b650d5a54184ff336826ae16f`  
		Last Modified: Tue, 24 Mar 2020 05:25:36 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f4d8154a8d6d9edf61516528f99c62d27eb41f8602571ae30fdf745976e2c6e`  
		Last Modified: Tue, 24 Mar 2020 05:25:35 GMT  
		Size: 15.5 KB (15490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5d54c7f7d9fb444dbe1aee28da7f339cfce0f93316d0e44b528e3f0b1c83a1e`  
		Last Modified: Tue, 14 Apr 2020 00:07:42 GMT  
		Size: 1.6 MB (1554129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2824223b1a0565c7df241643aa6173bcc7f918bd51af6cd082f1c4dd56375a79`  
		Last Modified: Tue, 14 Apr 2020 00:07:42 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b98391dc8eb3d7e32edcd1175b80a1588f44e5c9c8f93e0d7d35697e93f67fb`  
		Last Modified: Tue, 14 Apr 2020 00:07:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine` - linux; 386

```console
$ docker pull memcached@sha256:788ec77b1bd7a21665769b8e4302e8978c324953b48e09aeb17b41e80e20c5f0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4472337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7638872a17e59e75a022dc0c1a0a16cbe719fb3b5503003e4a7110ff97fca043`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Mar 2020 21:38:28 GMT
ADD file:99c8234abafd4fa915c0b826eb0e3be0e6aaa7c1e33cb1214ef71a99e9c02e06 in / 
# Mon, 23 Mar 2020 21:38:28 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 04:55:12 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Tue, 24 Mar 2020 04:55:13 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Tue, 14 Apr 2020 00:24:28 GMT
ENV MEMCACHED_VERSION=1.6.5
# Tue, 14 Apr 2020 00:24:29 GMT
ENV MEMCACHED_SHA1=1ddb5f37f69946b63512ad0f89dc448ff7ba5713
# Tue, 14 Apr 2020 00:33:02 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 14 Apr 2020 00:33:02 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 14 Apr 2020 00:33:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 14 Apr 2020 00:33:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2020 00:33:03 GMT
USER memcache
# Tue, 14 Apr 2020 00:33:03 GMT
EXPOSE 11211
# Tue, 14 Apr 2020 00:33:03 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:43f6a4398e1c9e860dfb5c93d7049ab9eedf814513bd6d07e06077c560303c7a`  
		Last Modified: Mon, 23 Mar 2020 21:38:48 GMT  
		Size: 2.8 MB (2806122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a31d073afa8dea3b0bfd6eeb6ebffc6447996f0e9cabebf9d749474ac22cdf2d`  
		Last Modified: Tue, 24 Mar 2020 05:04:58 GMT  
		Size: 1.2 KB (1230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:905909a3db778acdf7295903cff6ee7b27263e33facc5982475e7b60831413fc`  
		Last Modified: Tue, 24 Mar 2020 05:04:58 GMT  
		Size: 16.1 KB (16146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e55f704c4db8d5686c61a7f5dbf01efb54c26f928a4667edb336aa6b26c9931`  
		Last Modified: Tue, 14 Apr 2020 00:33:27 GMT  
		Size: 1.6 MB (1648434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85df688f5f46cdef50f778015f724036d02ef66baf23dee71b4f2021a38784bc`  
		Last Modified: Tue, 14 Apr 2020 00:33:27 GMT  
		Size: 284.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e187a846d19d6476ac11efbcb749911f8f31990824f548f8b22ac752a1218a`  
		Last Modified: Tue, 14 Apr 2020 00:33:27 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:3797459b34cdce19dc5c399b9c197be9e7ba49a5f24eb0519aafb09597505922
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4448507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf7465343178ddd65e795fcbffde4546ce34a20537d50c03bf12dc86eb96e1e0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Mar 2020 21:21:29 GMT
ADD file:4b35131542b9682214e1c2c72fe3cea215a10e2f775e87befecd80fe2228d5a0 in / 
# Mon, 23 Mar 2020 21:21:32 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 02:24:20 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Tue, 24 Mar 2020 02:24:25 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Tue, 14 Apr 2020 00:42:05 GMT
ENV MEMCACHED_VERSION=1.6.5
# Tue, 14 Apr 2020 00:42:08 GMT
ENV MEMCACHED_SHA1=1ddb5f37f69946b63512ad0f89dc448ff7ba5713
# Tue, 14 Apr 2020 00:50:46 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 14 Apr 2020 00:50:47 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 14 Apr 2020 00:51:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 14 Apr 2020 00:51:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2020 00:51:11 GMT
USER memcache
# Tue, 14 Apr 2020 00:51:15 GMT
EXPOSE 11211
# Tue, 14 Apr 2020 00:51:17 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bc1c99f4ba60de0d3ca52dc6855483e24c91884e33df71f502bbff6eb909d9b9`  
		Last Modified: Mon, 23 Mar 2020 21:22:12 GMT  
		Size: 2.8 MB (2820052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50bd2ca891d67079878bf06e36ba609e8528e83369265c92fbd3b03e6e839f1`  
		Last Modified: Tue, 24 Mar 2020 02:34:02 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a4704e4e496c0d18b40f484fc715146c1f427050210b40271112edcf751a698`  
		Last Modified: Tue, 24 Mar 2020 02:34:02 GMT  
		Size: 16.1 KB (16131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a082e2e1ac7786e3860912de8517980c8e08afb1ffa80d05d52240fbb673698`  
		Last Modified: Tue, 14 Apr 2020 00:51:52 GMT  
		Size: 1.6 MB (1610653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b1bdbb7103a9b4c5d777d6f23357bc31745b28dba327fa333173e2306e8ba5c`  
		Last Modified: Tue, 14 Apr 2020 00:51:51 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a958ecfb0c40b2251cf63426a688c563e8432efc39006acc5192e8fe59b23ab`  
		Last Modified: Tue, 14 Apr 2020 00:51:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:7295e677896a531ce8e2f171fde31f721618611720d4c911132736dbc45fa4d3
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4052728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04146b145e02520ac8848fd057a913852fd6ea8abc933fec317b7fc06010838d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 23 Jan 2020 16:52:43 GMT
ADD file:922e12714922ae035a33d6ceb8d2683ad3e454deca21ad02b699db908443342b in / 
# Thu, 23 Jan 2020 16:52:44 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:24:51 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Thu, 23 Jan 2020 17:24:52 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Thu, 23 Jan 2020 17:24:52 GMT
ENV MEMCACHED_VERSION=1.5.20
# Thu, 23 Jan 2020 17:24:52 GMT
ENV MEMCACHED_SHA1=5d3b5af3ce0a1483d655017db7228bcaeff10d47
# Thu, 23 Jan 2020 17:28:28 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		perl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		$enableExtstore 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Thu, 23 Jan 2020 17:28:28 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 23 Jan 2020 17:28:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 23 Jan 2020 17:28:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2020 17:28:29 GMT
USER memcache
# Thu, 23 Jan 2020 17:28:29 GMT
EXPOSE 11211
# Thu, 23 Jan 2020 17:28:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0449d076b2977b7e7ce4c35b0fe5199d86cabaf453e869da73b2efb66d6282dd`  
		Last Modified: Thu, 23 Jan 2020 16:53:07 GMT  
		Size: 2.6 MB (2573620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe38d0bfb4cf690c35f5cad20f2b3852cf3e3feae187d049660d61066d34266`  
		Last Modified: Thu, 23 Jan 2020 17:28:43 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e7b0be037aec2a267ac29fa65d5d2944abe8469008d0642de65630db833c613`  
		Last Modified: Thu, 23 Jan 2020 17:28:43 GMT  
		Size: 15.1 KB (15133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:721302a401eba2bc95563c39d70c6ceb2622f40852963b48a63b9436ac729b35`  
		Last Modified: Thu, 23 Jan 2020 17:28:43 GMT  
		Size: 1.5 MB (1462308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a3a38346255281bbb2fe4efbc071d94d6322906bce537bbfb2c901d054f30d`  
		Last Modified: Thu, 23 Jan 2020 17:28:43 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3309d80a3f4f5007acb79f3c9791f4d35a740e7d64bc8a859f0781987c9e51`  
		Last Modified: Thu, 23 Jan 2020 17:28:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:alpine`

```console
$ docker pull memcached@sha256:7053af573b42ea8ed1028f4d942f6e950259d9cf0bca2b7c9e1680a2b26cd485
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
$ docker pull memcached@sha256:42f3c2aa162185e3c8bef259444e2211072916dcd0ea1e3a97ebc40063565c82
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4371887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acce7f7ac2ef3283ff7538edb59d788e12a173e6c988e8142eda78a9d7d465f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 00:40:06 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Tue, 24 Mar 2020 00:40:07 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Tue, 14 Apr 2020 00:28:07 GMT
ENV MEMCACHED_VERSION=1.6.5
# Tue, 14 Apr 2020 00:28:08 GMT
ENV MEMCACHED_SHA1=1ddb5f37f69946b63512ad0f89dc448ff7ba5713
# Tue, 14 Apr 2020 00:36:24 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 14 Apr 2020 00:36:25 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 14 Apr 2020 00:36:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 14 Apr 2020 00:36:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2020 00:36:26 GMT
USER memcache
# Tue, 14 Apr 2020 00:36:26 GMT
EXPOSE 11211
# Tue, 14 Apr 2020 00:36:26 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a5fb4ad400df404c486089fa4098e9e6bfdb1528c2ee85cbd5614e8a97f1f9a`  
		Last Modified: Tue, 24 Mar 2020 00:48:55 GMT  
		Size: 1.2 KB (1230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb602a49f6f4777651777faab36b80d92a2f1dbe36d865c0cce4e182439c6b5e`  
		Last Modified: Tue, 24 Mar 2020 00:48:55 GMT  
		Size: 15.1 KB (15099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2ad92cd017e016358bcdd19608005e61b96f391f551cbf28b7bf893eb08f27`  
		Last Modified: Tue, 14 Apr 2020 00:36:52 GMT  
		Size: 1.6 MB (1551900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c47c68edd2b2740171a4efac506979aa590d59657cda2b828522131128a70e68`  
		Last Modified: Tue, 14 Apr 2020 00:36:52 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a4b5b784c11b1f78e28ec0cee292cd3ab2e91add940930435cbe73099221381`  
		Last Modified: Tue, 14 Apr 2020 00:36:52 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:2ad889e13d889d0a7bf42350cd8f4de4e63c14a935ed4eca89c15c22b650caf4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4148874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eebd4fa55e8dcf85c1736ab25138f0a2299ec97c84043b1a8893798172fcb5ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Mar 2020 21:49:26 GMT
ADD file:e2fdfc637b534345942caf4097883508a5ed23be97d85ccc3357b8277aaa5430 in / 
# Mon, 23 Mar 2020 21:49:27 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 23:15:28 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Mon, 23 Mar 2020 23:15:34 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Mon, 13 Apr 2020 23:51:16 GMT
ENV MEMCACHED_VERSION=1.6.5
# Mon, 13 Apr 2020 23:51:17 GMT
ENV MEMCACHED_SHA1=1ddb5f37f69946b63512ad0f89dc448ff7ba5713
# Tue, 14 Apr 2020 00:00:39 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 14 Apr 2020 00:00:40 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 14 Apr 2020 00:00:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 14 Apr 2020 00:00:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2020 00:00:42 GMT
USER memcache
# Tue, 14 Apr 2020 00:00:43 GMT
EXPOSE 11211
# Tue, 14 Apr 2020 00:00:44 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0776aeec3430c5a5ba3f43937f0ee6a7770a1fe81a318c9d94cc76512e5375e9`  
		Last Modified: Mon, 23 Mar 2020 21:49:50 GMT  
		Size: 2.6 MB (2618579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f329bb895b7588f4de54c119f39a5f656520bc2310d39893460c4398814112d`  
		Last Modified: Mon, 23 Mar 2020 23:25:38 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6bd8017eeb8ecce1d6b238f86b96a1af52d1a9dd44bc0da4c0573f58a7f51a8`  
		Last Modified: Mon, 23 Mar 2020 23:25:38 GMT  
		Size: 14.7 KB (14695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed1dbd69370c1c1fd0f473abbd0890a314699b93feb4e9a9397ad89e6f4d08e8`  
		Last Modified: Tue, 14 Apr 2020 00:01:00 GMT  
		Size: 1.5 MB (1513938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02da716a305370dd20bed73237b26c6686af6bb314c1730ca4b677e6b192948c`  
		Last Modified: Tue, 14 Apr 2020 00:01:01 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5a3d551b55e52c8a515a9331168aca21b6fa779ec12e67e0212eb263adeebda`  
		Last Modified: Tue, 14 Apr 2020 00:01:01 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:ec8c62ad113b358298092e63b474e8aeebb5b1e1bfabb2e6ff525646dc7458f1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3826282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5af1281a25c9479c7ad3e80e07f3e7b43e774841795c9f93004bf124abe4b0f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Mar 2020 21:57:55 GMT
ADD file:3bde6b6fd06efbf24e66446c6d32f72294fc749ae9ee6191776242e92b2f8ab4 in / 
# Mon, 23 Mar 2020 21:57:56 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:14:07 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Mon, 23 Mar 2020 22:14:20 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Tue, 24 Mar 2020 01:47:18 GMT
ENV MEMCACHED_VERSION=1.6.2
# Tue, 24 Mar 2020 01:47:22 GMT
ENV MEMCACHED_SHA1=a6a07f0433adaa13a3cafdf8c26acb640cdd001f
# Tue, 24 Mar 2020 03:19:47 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 24 Mar 2020 03:19:50 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 24 Mar 2020 03:20:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 24 Mar 2020 03:20:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2020 03:20:05 GMT
USER memcache
# Tue, 24 Mar 2020 03:20:07 GMT
EXPOSE 11211
# Tue, 24 Mar 2020 03:20:09 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d9bf605ce3d4449f4b90035c3e21d691806324781d43a5287b1da25a01779d6b`  
		Last Modified: Mon, 23 Mar 2020 21:58:16 GMT  
		Size: 2.4 MB (2420493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae54837c45cf98e10469ba87b255979740486d00d9407bc2fcdf1492469dc04`  
		Last Modified: Mon, 23 Mar 2020 22:42:38 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1459ca388d9e53a94cbb39e64789568710013f3b46396b24ea0729b570f74403`  
		Last Modified: Mon, 23 Mar 2020 22:42:44 GMT  
		Size: 13.6 KB (13638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f84775e4ae618e04e599d46af2006e35d62d9046f4908e660cc533b9cbb8c36`  
		Last Modified: Tue, 24 Mar 2020 03:21:11 GMT  
		Size: 1.4 MB (1390486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dd59b3062e02dcff6cd6cbe35ba1e84c44a571112a65c4dd0ad640b905e4ae3`  
		Last Modified: Tue, 24 Mar 2020 03:21:09 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f53094e3dbce9c8d482bfb7123a06c9a0e4e74102891a4aecc833167acbb64db`  
		Last Modified: Tue, 24 Mar 2020 03:21:15 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:08e4eee2dbc1e2589c53c0bbd26363957880c8563d31786d877d09ec516c0fed
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4294422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e0270dfda3dfe68de5b0bb5335b0930004ca3beed72eca0def0c03de87601b0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Mar 2020 21:39:52 GMT
ADD file:746a5c3838a898d6acf7877552ff13d1ab40d0036ace7a662e7c747018315ddb in / 
# Mon, 23 Mar 2020 21:39:53 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 05:16:12 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Tue, 24 Mar 2020 05:16:15 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Mon, 13 Apr 2020 23:57:43 GMT
ENV MEMCACHED_VERSION=1.6.5
# Mon, 13 Apr 2020 23:57:44 GMT
ENV MEMCACHED_SHA1=1ddb5f37f69946b63512ad0f89dc448ff7ba5713
# Tue, 14 Apr 2020 00:06:55 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 14 Apr 2020 00:06:56 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 14 Apr 2020 00:06:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 14 Apr 2020 00:06:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2020 00:07:00 GMT
USER memcache
# Tue, 14 Apr 2020 00:07:01 GMT
EXPOSE 11211
# Tue, 14 Apr 2020 00:07:02 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8a0637ca1ac98db4cf29f7632449c92801adc80cf0da2cd9c9e39882ce466561`  
		Last Modified: Mon, 23 Mar 2020 21:40:19 GMT  
		Size: 2.7 MB (2723139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd1bfe9c2142f88c6e142b39adf7ba4fe722789b650d5a54184ff336826ae16f`  
		Last Modified: Tue, 24 Mar 2020 05:25:36 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f4d8154a8d6d9edf61516528f99c62d27eb41f8602571ae30fdf745976e2c6e`  
		Last Modified: Tue, 24 Mar 2020 05:25:35 GMT  
		Size: 15.5 KB (15490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5d54c7f7d9fb444dbe1aee28da7f339cfce0f93316d0e44b528e3f0b1c83a1e`  
		Last Modified: Tue, 14 Apr 2020 00:07:42 GMT  
		Size: 1.6 MB (1554129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2824223b1a0565c7df241643aa6173bcc7f918bd51af6cd082f1c4dd56375a79`  
		Last Modified: Tue, 14 Apr 2020 00:07:42 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b98391dc8eb3d7e32edcd1175b80a1588f44e5c9c8f93e0d7d35697e93f67fb`  
		Last Modified: Tue, 14 Apr 2020 00:07:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:alpine` - linux; 386

```console
$ docker pull memcached@sha256:788ec77b1bd7a21665769b8e4302e8978c324953b48e09aeb17b41e80e20c5f0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4472337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7638872a17e59e75a022dc0c1a0a16cbe719fb3b5503003e4a7110ff97fca043`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Mar 2020 21:38:28 GMT
ADD file:99c8234abafd4fa915c0b826eb0e3be0e6aaa7c1e33cb1214ef71a99e9c02e06 in / 
# Mon, 23 Mar 2020 21:38:28 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 04:55:12 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Tue, 24 Mar 2020 04:55:13 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Tue, 14 Apr 2020 00:24:28 GMT
ENV MEMCACHED_VERSION=1.6.5
# Tue, 14 Apr 2020 00:24:29 GMT
ENV MEMCACHED_SHA1=1ddb5f37f69946b63512ad0f89dc448ff7ba5713
# Tue, 14 Apr 2020 00:33:02 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 14 Apr 2020 00:33:02 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 14 Apr 2020 00:33:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 14 Apr 2020 00:33:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2020 00:33:03 GMT
USER memcache
# Tue, 14 Apr 2020 00:33:03 GMT
EXPOSE 11211
# Tue, 14 Apr 2020 00:33:03 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:43f6a4398e1c9e860dfb5c93d7049ab9eedf814513bd6d07e06077c560303c7a`  
		Last Modified: Mon, 23 Mar 2020 21:38:48 GMT  
		Size: 2.8 MB (2806122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a31d073afa8dea3b0bfd6eeb6ebffc6447996f0e9cabebf9d749474ac22cdf2d`  
		Last Modified: Tue, 24 Mar 2020 05:04:58 GMT  
		Size: 1.2 KB (1230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:905909a3db778acdf7295903cff6ee7b27263e33facc5982475e7b60831413fc`  
		Last Modified: Tue, 24 Mar 2020 05:04:58 GMT  
		Size: 16.1 KB (16146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e55f704c4db8d5686c61a7f5dbf01efb54c26f928a4667edb336aa6b26c9931`  
		Last Modified: Tue, 14 Apr 2020 00:33:27 GMT  
		Size: 1.6 MB (1648434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85df688f5f46cdef50f778015f724036d02ef66baf23dee71b4f2021a38784bc`  
		Last Modified: Tue, 14 Apr 2020 00:33:27 GMT  
		Size: 284.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e187a846d19d6476ac11efbcb749911f8f31990824f548f8b22ac752a1218a`  
		Last Modified: Tue, 14 Apr 2020 00:33:27 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:3797459b34cdce19dc5c399b9c197be9e7ba49a5f24eb0519aafb09597505922
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4448507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf7465343178ddd65e795fcbffde4546ce34a20537d50c03bf12dc86eb96e1e0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Mar 2020 21:21:29 GMT
ADD file:4b35131542b9682214e1c2c72fe3cea215a10e2f775e87befecd80fe2228d5a0 in / 
# Mon, 23 Mar 2020 21:21:32 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 02:24:20 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Tue, 24 Mar 2020 02:24:25 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Tue, 14 Apr 2020 00:42:05 GMT
ENV MEMCACHED_VERSION=1.6.5
# Tue, 14 Apr 2020 00:42:08 GMT
ENV MEMCACHED_SHA1=1ddb5f37f69946b63512ad0f89dc448ff7ba5713
# Tue, 14 Apr 2020 00:50:46 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 14 Apr 2020 00:50:47 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 14 Apr 2020 00:51:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 14 Apr 2020 00:51:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2020 00:51:11 GMT
USER memcache
# Tue, 14 Apr 2020 00:51:15 GMT
EXPOSE 11211
# Tue, 14 Apr 2020 00:51:17 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bc1c99f4ba60de0d3ca52dc6855483e24c91884e33df71f502bbff6eb909d9b9`  
		Last Modified: Mon, 23 Mar 2020 21:22:12 GMT  
		Size: 2.8 MB (2820052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50bd2ca891d67079878bf06e36ba609e8528e83369265c92fbd3b03e6e839f1`  
		Last Modified: Tue, 24 Mar 2020 02:34:02 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a4704e4e496c0d18b40f484fc715146c1f427050210b40271112edcf751a698`  
		Last Modified: Tue, 24 Mar 2020 02:34:02 GMT  
		Size: 16.1 KB (16131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a082e2e1ac7786e3860912de8517980c8e08afb1ffa80d05d52240fbb673698`  
		Last Modified: Tue, 14 Apr 2020 00:51:52 GMT  
		Size: 1.6 MB (1610653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b1bdbb7103a9b4c5d777d6f23357bc31745b28dba327fa333173e2306e8ba5c`  
		Last Modified: Tue, 14 Apr 2020 00:51:51 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a958ecfb0c40b2251cf63426a688c563e8432efc39006acc5192e8fe59b23ab`  
		Last Modified: Tue, 14 Apr 2020 00:51:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:alpine` - linux; s390x

```console
$ docker pull memcached@sha256:7295e677896a531ce8e2f171fde31f721618611720d4c911132736dbc45fa4d3
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4052728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04146b145e02520ac8848fd057a913852fd6ea8abc933fec317b7fc06010838d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 23 Jan 2020 16:52:43 GMT
ADD file:922e12714922ae035a33d6ceb8d2683ad3e454deca21ad02b699db908443342b in / 
# Thu, 23 Jan 2020 16:52:44 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:24:51 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Thu, 23 Jan 2020 17:24:52 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Thu, 23 Jan 2020 17:24:52 GMT
ENV MEMCACHED_VERSION=1.5.20
# Thu, 23 Jan 2020 17:24:52 GMT
ENV MEMCACHED_SHA1=5d3b5af3ce0a1483d655017db7228bcaeff10d47
# Thu, 23 Jan 2020 17:28:28 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		perl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		$enableExtstore 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Thu, 23 Jan 2020 17:28:28 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 23 Jan 2020 17:28:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 23 Jan 2020 17:28:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2020 17:28:29 GMT
USER memcache
# Thu, 23 Jan 2020 17:28:29 GMT
EXPOSE 11211
# Thu, 23 Jan 2020 17:28:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0449d076b2977b7e7ce4c35b0fe5199d86cabaf453e869da73b2efb66d6282dd`  
		Last Modified: Thu, 23 Jan 2020 16:53:07 GMT  
		Size: 2.6 MB (2573620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe38d0bfb4cf690c35f5cad20f2b3852cf3e3feae187d049660d61066d34266`  
		Last Modified: Thu, 23 Jan 2020 17:28:43 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e7b0be037aec2a267ac29fa65d5d2944abe8469008d0642de65630db833c613`  
		Last Modified: Thu, 23 Jan 2020 17:28:43 GMT  
		Size: 15.1 KB (15133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:721302a401eba2bc95563c39d70c6ceb2622f40852963b48a63b9436ac729b35`  
		Last Modified: Thu, 23 Jan 2020 17:28:43 GMT  
		Size: 1.5 MB (1462308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a3a38346255281bbb2fe4efbc071d94d6322906bce537bbfb2c901d054f30d`  
		Last Modified: Thu, 23 Jan 2020 17:28:43 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3309d80a3f4f5007acb79f3c9791f4d35a740e7d64bc8a859f0781987c9e51`  
		Last Modified: Thu, 23 Jan 2020 17:28:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:latest`

```console
$ docker pull memcached@sha256:d404bf441a84afab01e3fa5ff9588ed54e5b6d3e29bf232f45c48e2565848ae6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `memcached:latest` - linux; amd64

```console
$ docker pull memcached@sha256:e4b600639b0b2540e93f82cb213c9d0ab3ca7443b59459876425958f6e655834
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 MB (30485949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e310fbc8b97af886d4d825b655c4c21be64bfd5758ddd23223fdc5b13466c4b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 31 Mar 2020 01:21:01 GMT
ADD file:d1f1b387a158136fb0f8096c8a8ecf5fc146be4e85c1c3c345d44c927692723a in / 
# Tue, 31 Mar 2020 01:21:01 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 13:20:36 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 31 Mar 2020 13:20:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 Apr 2020 00:19:49 GMT
ENV MEMCACHED_VERSION=1.6.5
# Tue, 14 Apr 2020 00:19:49 GMT
ENV MEMCACHED_SHA1=1ddb5f37f69946b63512ad0f89dc448ff7ba5713
# Tue, 14 Apr 2020 00:27:55 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 14 Apr 2020 00:27:55 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 14 Apr 2020 00:27:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 14 Apr 2020 00:27:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2020 00:27:56 GMT
USER memcache
# Tue, 14 Apr 2020 00:27:56 GMT
EXPOSE 11211
# Tue, 14 Apr 2020 00:27:57 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c499e6d256d6d4a546f1c141e04b5b4951983ba7581e39deaf5cc595289ee70f`  
		Last Modified: Tue, 31 Mar 2020 01:26:37 GMT  
		Size: 27.1 MB (27091862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512f277e1da84b0b9319530d40c48750bb22b13f4816d103040d20c0635c28be`  
		Last Modified: Tue, 31 Mar 2020 13:29:52 GMT  
		Size: 5.0 KB (4984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdda69e165e26c667ba223dc215274101c3c6e41db182bd651aadf5e5623fc35`  
		Last Modified: Tue, 31 Mar 2020 13:29:53 GMT  
		Size: 2.2 MB (2196476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1780eff22105ecc8f0d35be5b018221e6cded84048aab30d770861ff638124e`  
		Last Modified: Tue, 14 Apr 2020 00:36:46 GMT  
		Size: 1.2 MB (1192218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ef130d1915ebd4a9b8360f39f34c7cc53aadf772671b5a104da3ae654221ca`  
		Last Modified: Tue, 14 Apr 2020 00:36:46 GMT  
		Size: 288.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56ebe2ea417575287b4ef17c9cb0a263ee4646fa6ed1553a617edf0b35a832b2`  
		Last Modified: Tue, 14 Apr 2020 00:36:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:latest` - linux; arm variant v5

```console
$ docker pull memcached@sha256:552667e7d659ec140e52ce197993eca4f4ae04580cf58bb299339f154ce9289a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.9 MB (27889465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70d335e80be14665b0694c2a8ad92bd15d99f2245a72e131de7d455d8f86e8de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 31 Mar 2020 01:24:54 GMT
ADD file:e08ed9e60228d351de400af5746474777a562d99f17e0cb1ce3e3d352e9ec751 in / 
# Tue, 31 Mar 2020 01:24:56 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:54:28 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 31 Mar 2020 01:55:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 13 Apr 2020 23:51:13 GMT
ENV MEMCACHED_VERSION=1.6.5
# Mon, 13 Apr 2020 23:51:15 GMT
ENV MEMCACHED_SHA1=1ddb5f37f69946b63512ad0f89dc448ff7ba5713
# Tue, 14 Apr 2020 01:20:37 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 14 Apr 2020 01:20:40 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 14 Apr 2020 01:20:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 14 Apr 2020 01:20:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2020 01:20:54 GMT
USER memcache
# Tue, 14 Apr 2020 01:20:56 GMT
EXPOSE 11211
# Tue, 14 Apr 2020 01:20:57 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:440df189aa3df85587f2d7d348500930481b3752dcb887d212de9b44b49076dd`  
		Last Modified: Tue, 31 Mar 2020 01:33:04 GMT  
		Size: 24.8 MB (24830324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bde8351817341fa2fec288d97635ede228892bbb58fc5c6ca54441acef6f0766`  
		Last Modified: Tue, 31 Mar 2020 03:24:42 GMT  
		Size: 4.9 KB (4896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b011e5f13bdf6608cafa62557b3c877e4794590eaadced0b8a49fe24a28d110`  
		Last Modified: Tue, 31 Mar 2020 03:24:44 GMT  
		Size: 1.9 MB (1896786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b83243350d1cc24097d68bc247cbb15df78dad5055598e77779909c8b6dc9b`  
		Last Modified: Tue, 14 Apr 2020 01:21:15 GMT  
		Size: 1.2 MB (1157053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16d88842ba9a93f3329b9f416cd2e0efca324f36356c4713ca584a17c791173b`  
		Last Modified: Tue, 14 Apr 2020 01:21:13 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35420a44da1fda5e245ef5baf104f3fa9cd5564e894134f8d3c697f50b8d42a1`  
		Last Modified: Tue, 14 Apr 2020 01:21:19 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:latest` - linux; arm variant v7

```console
$ docker pull memcached@sha256:54bcd309e2f20393d4697e22b71344137d3f1fdeb447078522a5a2d6a464117e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 MB (25646504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd1835a38d745cc54481b86a3603e5fe1771df287e08d6061cb35577ce92b735`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 31 Mar 2020 01:48:12 GMT
ADD file:8c3ed0df404a6bcaf7583e71796cb4c1f40e87288953a21d4ee5946079c3274f in / 
# Tue, 31 Mar 2020 01:48:13 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 03:27:08 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 31 Mar 2020 03:28:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 Apr 2020 01:21:52 GMT
ENV MEMCACHED_VERSION=1.6.5
# Tue, 14 Apr 2020 01:21:54 GMT
ENV MEMCACHED_SHA1=1ddb5f37f69946b63512ad0f89dc448ff7ba5713
# Tue, 14 Apr 2020 01:50:54 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 14 Apr 2020 01:50:57 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 14 Apr 2020 01:51:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 14 Apr 2020 01:51:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2020 01:51:11 GMT
USER memcache
# Tue, 14 Apr 2020 01:51:12 GMT
EXPOSE 11211
# Tue, 14 Apr 2020 01:51:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:98098fa10651fdba12c848231b7428536a120e17637f1f9e0d25c63880483fcc`  
		Last Modified: Tue, 31 Mar 2020 01:56:24 GMT  
		Size: 22.7 MB (22699731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a7a42e48b851419bcd11506631a8d336fb394d979dcea8feb4830f38ba7cfd7`  
		Last Modified: Tue, 31 Mar 2020 04:39:27 GMT  
		Size: 4.9 KB (4899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc96c4fde110b7a8691d85cf0523cd326fbfd1bcbf928719f6173cd292c91305`  
		Last Modified: Tue, 31 Mar 2020 04:39:35 GMT  
		Size: 1.8 MB (1811551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca1ebe9584513d346175a7b8dc24e8a0e1f282079ab035f21745b1efb49aee2`  
		Last Modified: Tue, 14 Apr 2020 03:14:41 GMT  
		Size: 1.1 MB (1129915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3670b9b896bea4402ae6cf76d7c5690c7be94b8712a6ba9bdbc5162c478c3f4a`  
		Last Modified: Tue, 14 Apr 2020 03:14:40 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13fc7c30db064f3e3c4355aa5316e9ee78fc6d5727ba346d8289b531a5244235`  
		Last Modified: Tue, 14 Apr 2020 03:14:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:latest` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:296400cfcf0b05f045c250b4839f2ef4312e75a29171dc0453ea424a2a40f683
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29094935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b876c7370d1497d75e73a86321425fb8e2e449893d19fcdb24d41f856d946a08`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 31 Mar 2020 02:05:33 GMT
ADD file:47ab456123ae97a527249191ff2bc0014e7ef0ae186aec91bf6a63eb077ecb91 in / 
# Tue, 31 Mar 2020 02:05:35 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 08:39:07 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 31 Mar 2020 08:39:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 13 Apr 2020 23:47:52 GMT
ENV MEMCACHED_VERSION=1.6.5
# Mon, 13 Apr 2020 23:47:53 GMT
ENV MEMCACHED_SHA1=1ddb5f37f69946b63512ad0f89dc448ff7ba5713
# Mon, 13 Apr 2020 23:57:24 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Mon, 13 Apr 2020 23:57:24 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Mon, 13 Apr 2020 23:57:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 13 Apr 2020 23:57:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Apr 2020 23:57:27 GMT
USER memcache
# Mon, 13 Apr 2020 23:57:28 GMT
EXPOSE 11211
# Mon, 13 Apr 2020 23:57:28 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a6c32b8bc1ce2b374630673ded1d5ef5a98936d045bf0632fcf599dc2229d493`  
		Last Modified: Tue, 31 Mar 2020 02:12:15 GMT  
		Size: 25.9 MB (25851645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72560398e0dc8991a53cd07c580b14e3c2024d7af30d2dfe8428d913006af5a9`  
		Last Modified: Tue, 31 Mar 2020 08:48:55 GMT  
		Size: 5.0 KB (5028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4febdbdc3565b2d569ed0a6885c548a5755cd9a2b52c21b351d254c83e6fff7`  
		Last Modified: Tue, 31 Mar 2020 08:48:55 GMT  
		Size: 2.1 MB (2074952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8266bd2499012e842778a6e03cccde2b97d44f659ebbfcd1a69eccc22d1bc3a`  
		Last Modified: Tue, 14 Apr 2020 00:07:33 GMT  
		Size: 1.2 MB (1162903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99b2bf34e46eab97471c453efd6d739d3d6f3de32789d23cf81e6eaa94d2ea6e`  
		Last Modified: Tue, 14 Apr 2020 00:07:33 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1a5e887fbf0bacccd7a723d6c972e22f49e6cdbbdc0d5156f127d8e5507717b`  
		Last Modified: Tue, 14 Apr 2020 00:07:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:latest` - linux; 386

```console
$ docker pull memcached@sha256:f77cbe58b76a6763ebbacbb8d9a53c9705b0f1784d50261627ea7148225a53b4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31156720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06a5671f4598de98b696abbd0eaee1875af3cf8d5825a2c079f751054a79a319`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 31 Mar 2020 00:39:42 GMT
ADD file:a453117866661af4ddfa21203d65ce6661efeaeca2a1704e09747c83b4c58e47 in / 
# Tue, 31 Mar 2020 00:39:42 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 11:45:29 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 31 Mar 2020 11:45:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 Apr 2020 00:15:39 GMT
ENV MEMCACHED_VERSION=1.6.5
# Tue, 14 Apr 2020 00:15:40 GMT
ENV MEMCACHED_SHA1=1ddb5f37f69946b63512ad0f89dc448ff7ba5713
# Tue, 14 Apr 2020 00:24:13 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 14 Apr 2020 00:24:13 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 14 Apr 2020 00:24:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 14 Apr 2020 00:24:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2020 00:24:14 GMT
USER memcache
# Tue, 14 Apr 2020 00:24:14 GMT
EXPOSE 11211
# Tue, 14 Apr 2020 00:24:15 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2314106a15e49c7908bebb2c697dcaf3d6a1626b70fe72bc0c0cb71eb216ddc3`  
		Last Modified: Tue, 31 Mar 2020 00:45:31 GMT  
		Size: 27.7 MB (27747648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3bafab0976764495dda52d0c16addb4770d62d8f9de55728b752ff3448f2292`  
		Last Modified: Tue, 31 Mar 2020 11:55:29 GMT  
		Size: 4.9 KB (4899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8307e5e61ebc9ed2430c9e45ba3437aa1deebed0882ce15c36616e0debf28b36`  
		Last Modified: Tue, 31 Mar 2020 11:55:29 GMT  
		Size: 2.2 MB (2208079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1a1a09da032c7622fe0330fa14876496b04b5e9e81943f09df1b315bec0a4d`  
		Last Modified: Tue, 14 Apr 2020 00:33:22 GMT  
		Size: 1.2 MB (1195686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80e37d2af038355acfb8af6aca4e4cb3a65c0d08aaab7723c1987d1006fbf17b`  
		Last Modified: Tue, 14 Apr 2020 00:33:21 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ec8103e2aa301996d108c97a0d120cdc72d11519b4269350d4d72c026e919d`  
		Last Modified: Tue, 14 Apr 2020 00:33:21 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:latest` - linux; ppc64le

```console
$ docker pull memcached@sha256:b587e1ac02d9b43b4dc13af7294b8f81a5e638b13c981743a1ffb2798c733976
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.1 MB (34064242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8704abb1ba80a90926fd4cc6cb9e20c5f3624763df555561a961411766e635a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 31 Mar 2020 01:32:42 GMT
ADD file:36c02e92574faba45b64cfed78a0a0359d65ad175b17128bf554a2a5c0086ff5 in / 
# Tue, 31 Mar 2020 01:32:47 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 12:45:58 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 31 Mar 2020 12:46:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 Apr 2020 00:29:39 GMT
ENV MEMCACHED_VERSION=1.6.5
# Tue, 14 Apr 2020 00:29:44 GMT
ENV MEMCACHED_SHA1=1ddb5f37f69946b63512ad0f89dc448ff7ba5713
# Tue, 14 Apr 2020 00:41:15 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 14 Apr 2020 00:41:17 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 14 Apr 2020 00:41:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 14 Apr 2020 00:41:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2020 00:41:38 GMT
USER memcache
# Tue, 14 Apr 2020 00:41:45 GMT
EXPOSE 11211
# Tue, 14 Apr 2020 00:41:51 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9df6bbae5eeb29e9aac2f39cff517c694cce60f01ee477abcdedcd8e8c01c38f`  
		Last Modified: Tue, 31 Mar 2020 01:45:59 GMT  
		Size: 30.5 MB (30518493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2786c1a6fbad6e8c56e4f7e33b4d41c64efd06c4cdb303a50c07ee1f4c5f7a69`  
		Last Modified: Tue, 31 Mar 2020 12:58:00 GMT  
		Size: 5.0 KB (4987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:722cfb50c03533f4b5c83c84a2f565dbcdbf63c01460ae91d35aafacd94454fe`  
		Last Modified: Tue, 31 Mar 2020 12:58:00 GMT  
		Size: 2.3 MB (2322647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec1b5923ebd47cd1e2443a1ff44899de7b683eadb673d9404c7c259b96277c7d`  
		Last Modified: Tue, 14 Apr 2020 00:51:37 GMT  
		Size: 1.2 MB (1217708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3311546eb5856360dd803bbb0e75a832bef2fb729dce22a03be0656ebbcec2f4`  
		Last Modified: Tue, 14 Apr 2020 00:51:36 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5646db67b9fcecdc7d9a2c867f4515d81b3f3e429cbcb5b3804420a392b277ae`  
		Last Modified: Tue, 14 Apr 2020 00:51:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:latest` - linux; s390x

```console
$ docker pull memcached@sha256:057b9567b3c01a5b0dbf1c7dba5b89d88df721093c01da5c6a1425c1f8ad6265
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.7 MB (28694839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe2378496a97259729a8423d4b14be0ea1db6e01b3f9aa9e34431ef824d655e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 28 Dec 2019 04:42:03 GMT
ADD file:eec6c56f8680753860198c3af0d94aabb87018ca30f6f6e346621a6bffe0e4b8 in / 
# Sat, 28 Dec 2019 04:42:04 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 09:52:58 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Sat, 28 Dec 2019 09:53:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 09:53:02 GMT
ENV MEMCACHED_VERSION=1.5.20
# Sat, 28 Dec 2019 09:53:02 GMT
ENV MEMCACHED_SHA1=5d3b5af3ce0a1483d655017db7228bcaeff10d47
# Sat, 28 Dec 2019 09:57:41 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Sat, 28 Dec 2019 09:57:41 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Sat, 28 Dec 2019 09:57:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 28 Dec 2019 09:57:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Dec 2019 09:57:42 GMT
USER memcache
# Sat, 28 Dec 2019 09:57:42 GMT
EXPOSE 11211
# Sat, 28 Dec 2019 09:57:42 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f7542f43e95fb32a870ee38d7f0e7bb23267ac8dcf709e3944311b0a30d7a479`  
		Last Modified: Sat, 28 Dec 2019 04:45:08 GMT  
		Size: 25.7 MB (25705315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10233ccd3a1a569a8ec38365e560732bbd6adbbe1646b79cee3569d59f7cef73`  
		Last Modified: Sat, 28 Dec 2019 09:57:55 GMT  
		Size: 5.0 KB (5022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f3e3dfd06ace4d055f1539e38c0fb68e4d1866043a1ba372c8c2f0fec48315d`  
		Last Modified: Sat, 28 Dec 2019 09:57:55 GMT  
		Size: 1.9 MB (1885865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47cce4b30798653a4fcf3fd9160a90374e103d5c1e877e69645d033c0f916e67`  
		Last Modified: Sat, 28 Dec 2019 09:57:55 GMT  
		Size: 1.1 MB (1098229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:982ba8604e516e190f19469aa238d4197aa0000182cbc54d57345a029b765600`  
		Last Modified: Sat, 28 Dec 2019 09:57:55 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aabfe12e62b1d54d9dce449f2dc85f703ade5574f14eadfa54a601a86cc96e54`  
		Last Modified: Sat, 28 Dec 2019 09:57:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
