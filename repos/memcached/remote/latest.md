## `memcached:latest`

```console
$ docker pull memcached@sha256:520bb1cbf89b9cf160d44cd146fb8dc604c61b3199c2bc6beba794224ab3aefb
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
$ docker pull memcached@sha256:86f998ec36f9de185fdb923bf41f5cc35fec36e463bdaa751804e634751e424f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 MB (30494238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17322695c0f0e3cb6ba99fbaae416b422975a5a1b6505d3affe9080a036a07e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 15 May 2020 06:28:44 GMT
ADD file:7780c81c33e6cc5b6261af4a6c611cce0f39dec3131009bb297e65f12020c150 in / 
# Fri, 15 May 2020 06:28:44 GMT
CMD ["bash"]
# Fri, 15 May 2020 19:15:00 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Fri, 15 May 2020 19:15:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 19:15:05 GMT
ENV MEMCACHED_VERSION=1.6.6
# Fri, 15 May 2020 19:15:05 GMT
ENV MEMCACHED_SHA1=d8895b12dc9fc82b389f1713e2c09cc6ca3d03e4
# Fri, 15 May 2020 19:25:19 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Fri, 15 May 2020 19:25:19 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Fri, 15 May 2020 19:25:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 15 May 2020 19:25:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2020 19:25:20 GMT
USER memcache
# Fri, 15 May 2020 19:25:20 GMT
EXPOSE 11211
# Fri, 15 May 2020 19:25:21 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:afb6ec6fdc1c3ba04f7a56db32c5ff5ff38962dc4cd0ffdef5beaa0ce2eb77e2`  
		Last Modified: Fri, 15 May 2020 06:37:39 GMT  
		Size: 27.1 MB (27098756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b2a221a20c0801090ddaf51d2d619b28c8e37dc878021511ac6e22d32a0c9d4`  
		Last Modified: Fri, 15 May 2020 19:25:50 GMT  
		Size: 5.0 KB (4981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da6c6f4b05c3e712195c8de2ebf4bc71cb080173a1e1566007ff0bdf364c9628`  
		Last Modified: Fri, 15 May 2020 19:25:51 GMT  
		Size: 2.2 MB (2196460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfc1ad3efe0c96492092d0448407eb4403168f5406dd3ceead68ee7b55180a02`  
		Last Modified: Fri, 15 May 2020 19:25:50 GMT  
		Size: 1.2 MB (1193633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be49f2b4b3df92d4d4f08f9b438a33d538fd0515e1d9845fb5800830c8e328cb`  
		Last Modified: Fri, 15 May 2020 19:25:50 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4469aa09ad371b7b7ffff86fa693352b751e5d7a21cf9400ce1f5e62a9d5ac1c`  
		Last Modified: Fri, 15 May 2020 19:25:50 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:latest` - linux; arm variant v5

```console
$ docker pull memcached@sha256:dc9a77ee01064e8acdbf14b71dd534aae4ddabdd0510a98cd45fed6a7bd2c21c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.9 MB (27903573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28ef8d57f819cc41c572cf51b259668973ebd3c9b844ff17d142edd3592371f6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 14 May 2020 22:38:03 GMT
ADD file:cbd01ff8d2e40a25bcdb13dc19ffe124c2927b491997dc1c57d4f2c2a308e279 in / 
# Thu, 14 May 2020 22:38:05 GMT
CMD ["bash"]
# Fri, 15 May 2020 04:29:13 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Fri, 15 May 2020 04:29:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 04:29:25 GMT
ENV MEMCACHED_VERSION=1.6.6
# Fri, 15 May 2020 04:29:26 GMT
ENV MEMCACHED_SHA1=d8895b12dc9fc82b389f1713e2c09cc6ca3d03e4
# Fri, 15 May 2020 04:39:57 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Fri, 15 May 2020 04:39:58 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Fri, 15 May 2020 04:40:00 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 15 May 2020 04:40:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2020 04:40:02 GMT
USER memcache
# Fri, 15 May 2020 04:40:03 GMT
EXPOSE 11211
# Fri, 15 May 2020 04:40:04 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:24d81022117207b0239d8a8023ca1724b7dde38cb08ce5b9199f59d475d1e600`  
		Last Modified: Thu, 14 May 2020 22:46:51 GMT  
		Size: 24.8 MB (24838470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6da53be3d7a73a8ef07c1124ab0b4e28b0da9c6997130302c21e5b4c1ae97733`  
		Last Modified: Fri, 15 May 2020 04:40:17 GMT  
		Size: 4.9 KB (4891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4904755698e48802a55719bbb0f8daf0234dd0ae6d30cc58b88b9bf5c41d8ca`  
		Last Modified: Fri, 15 May 2020 04:40:18 GMT  
		Size: 1.9 MB (1896845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e9c71c2276e8c519f7b461c4190a0534f86f61dbfb6a7f39960468b1f81cd6`  
		Last Modified: Fri, 15 May 2020 04:40:18 GMT  
		Size: 1.2 MB (1162959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c1785a10a165cdc5a881d1cedd7601a895318f99fd676ee3b4ee95df5b15e1b`  
		Last Modified: Fri, 15 May 2020 04:40:17 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e82402f7f7a5e71d260a925a7a1de9667390788b0f10b861c0d0f3f97b21b20`  
		Last Modified: Fri, 15 May 2020 04:40:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:latest` - linux; arm variant v7

```console
$ docker pull memcached@sha256:629fdd3f42a6c7bf84431a4313c34757feb188efae8968eb5fe1bf5f24074f7d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25657392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85aca5d013d028989cb5f936a1dc3e623ac731bd51e2ffd03e8fe3abe229fb6a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 15 May 2020 01:00:06 GMT
ADD file:e3f9a454eccb40b4d7bf1dcc17ec29589a007ac67545d1cb5b6fa213c872c8f2 in / 
# Fri, 15 May 2020 01:00:07 GMT
CMD ["bash"]
# Fri, 15 May 2020 10:16:44 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Fri, 15 May 2020 10:16:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 10:16:54 GMT
ENV MEMCACHED_VERSION=1.6.6
# Fri, 15 May 2020 10:16:55 GMT
ENV MEMCACHED_SHA1=d8895b12dc9fc82b389f1713e2c09cc6ca3d03e4
# Fri, 15 May 2020 10:27:06 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Fri, 15 May 2020 10:27:06 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Fri, 15 May 2020 10:27:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 15 May 2020 10:27:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2020 10:27:10 GMT
USER memcache
# Fri, 15 May 2020 10:27:11 GMT
EXPOSE 11211
# Fri, 15 May 2020 10:27:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:e41e28500352be59188c3d871a4b5a3f594350b860a9a36ed5808a35920bdae4`  
		Last Modified: Fri, 15 May 2020 01:11:21 GMT  
		Size: 22.7 MB (22705925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1c79109a8458ae42d8e9a889171af08230424b8a54441c5cacadf40966ed8bf`  
		Last Modified: Fri, 15 May 2020 10:27:41 GMT  
		Size: 4.9 KB (4897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:340c1d1bcd42e8e20c1e01a518252f863e55191ec6462335bd9d6f802b68c477`  
		Last Modified: Fri, 15 May 2020 10:27:41 GMT  
		Size: 1.8 MB (1811508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fbfd80c0b8e2f877d5d32ab530ae8c9e8b3994b3cc375f4cdb3e1069695c72b`  
		Last Modified: Fri, 15 May 2020 10:27:41 GMT  
		Size: 1.1 MB (1134654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fbf772698bdee3c24823a0ee8f7d465b0ee7b30c5125b9695f187254d1a3caf`  
		Last Modified: Fri, 15 May 2020 10:27:41 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e79c751abc7c0500589a0633ee9078d0ebe91e8d370b91c5d671bcb5cbab54b`  
		Last Modified: Fri, 15 May 2020 10:27:41 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:latest` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:c2aa0d8d3eb0a2c3d98b5ddfcba421d74e042893f0a1f34f4969353b677fd8a7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29101630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d90c7f676fc3a67f33db26903d73e9261dcd36f36f1264ed070c7424898f9b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 15 May 2020 12:44:06 GMT
ADD file:b305c1792102142f183d3084026f0fc6be3ddf8d1959b32f0a5d22d35eebcd15 in / 
# Fri, 15 May 2020 12:44:07 GMT
CMD ["bash"]
# Fri, 15 May 2020 21:29:10 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Fri, 15 May 2020 21:29:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 21:29:57 GMT
ENV MEMCACHED_VERSION=1.6.6
# Fri, 15 May 2020 21:30:15 GMT
ENV MEMCACHED_SHA1=d8895b12dc9fc82b389f1713e2c09cc6ca3d03e4
# Fri, 15 May 2020 21:52:41 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Fri, 15 May 2020 21:52:53 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Fri, 15 May 2020 21:53:37 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 15 May 2020 21:53:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2020 21:53:48 GMT
USER memcache
# Fri, 15 May 2020 21:53:55 GMT
EXPOSE 11211
# Fri, 15 May 2020 21:54:04 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8a7e1e68c24e5cac20ef26d29505c58456b561c431f0c683b66d1a0943f40dd4`  
		Last Modified: Fri, 15 May 2020 12:53:36 GMT  
		Size: 25.9 MB (25857195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e94a7318ca57d36c6af1616a2662d353f544616be21ab9fc6b914fb4ffc600bb`  
		Last Modified: Fri, 15 May 2020 21:54:30 GMT  
		Size: 5.0 KB (5027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a29880f6df167f4290e8355bcbade06db88c04e332c49d5a434a9aa4b46696b9`  
		Last Modified: Fri, 15 May 2020 21:54:29 GMT  
		Size: 2.1 MB (2074972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f85914d5b5c084fed34e2b8add774a25931e7932b67f5dbad5191e989df2148`  
		Last Modified: Fri, 15 May 2020 21:54:28 GMT  
		Size: 1.2 MB (1164028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2384dd71c69a3fea52cc62f3c7b5e2aefd5b37fee211304912c3ff441bb5cf3e`  
		Last Modified: Fri, 15 May 2020 21:54:29 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8c5377eff9585348934be33ffaed39838a5fff06d3d61ea528fe45f3bf210a9`  
		Last Modified: Fri, 15 May 2020 21:54:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:latest` - linux; 386

```console
$ docker pull memcached@sha256:eaec1d72198d6440a907adb90a3bb4967ac5a78e07984d7e69c92e12fa43ac0b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31165591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6b0f58fdf728ec58361bbf2fc24dda5c8564155a94d5682d800206a31177727`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 15 May 2020 07:07:55 GMT
ADD file:0c3b44c83914e95e4604999a86af05023cdd2b2f795e71d737e428fae4a7e0ac in / 
# Fri, 15 May 2020 07:07:56 GMT
CMD ["bash"]
# Fri, 15 May 2020 18:11:46 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Fri, 15 May 2020 18:11:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 18:11:51 GMT
ENV MEMCACHED_VERSION=1.6.6
# Fri, 15 May 2020 18:11:51 GMT
ENV MEMCACHED_SHA1=d8895b12dc9fc82b389f1713e2c09cc6ca3d03e4
# Fri, 15 May 2020 18:21:46 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Fri, 15 May 2020 18:21:46 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Fri, 15 May 2020 18:21:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 15 May 2020 18:21:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2020 18:21:47 GMT
USER memcache
# Fri, 15 May 2020 18:21:47 GMT
EXPOSE 11211
# Fri, 15 May 2020 18:21:48 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a5695130085a13212b02bf2645a52af5b41dd13e6dc9b29e2d7f357e1525aa48`  
		Last Modified: Fri, 15 May 2020 07:18:14 GMT  
		Size: 27.8 MB (27754922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8c8809e96af715e2b2d62be4034f38f5cdba7624db240ed933be6b8a8b13d03`  
		Last Modified: Fri, 15 May 2020 18:22:02 GMT  
		Size: 4.9 KB (4895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be1468bc2282a70cf775707f4920acc680d1b290760c6d4e08567f0bf724b0ba`  
		Last Modified: Fri, 15 May 2020 18:22:03 GMT  
		Size: 2.2 MB (2208166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c06ead579287e05cfcbe33586645d047de77cf1de45150c2500da48926411b`  
		Last Modified: Fri, 15 May 2020 18:22:03 GMT  
		Size: 1.2 MB (1197201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1686728eefede249133dc78e0f27e7eb44fe957aee5f8cadfdb9e62a7db8ac08`  
		Last Modified: Fri, 15 May 2020 18:22:02 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:755bfb9b984d0606add25642382eda2f0077f34e85110da258ab9696b950bca4`  
		Last Modified: Fri, 15 May 2020 18:22:02 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:latest` - linux; mips64le

```console
$ docker pull memcached@sha256:c4e92fd1655c1d4525ba62fd5c64c91965c45f8040e667a4c2141b98e8c47d92
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.7 MB (28728323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8faf80eb27a2956f0916bf57b614f88483362cee8bb020452354db60324ad329`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 15 May 2020 04:48:19 GMT
ADD file:1163d3a5831eb58d132b66b60303169816e7bd8289f19caaac1157179a95f6f9 in / 
# Fri, 15 May 2020 04:48:19 GMT
CMD ["bash"]
# Fri, 15 May 2020 17:32:07 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Fri, 15 May 2020 17:32:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 17:32:21 GMT
ENV MEMCACHED_VERSION=1.6.6
# Fri, 15 May 2020 17:32:22 GMT
ENV MEMCACHED_SHA1=d8895b12dc9fc82b389f1713e2c09cc6ca3d03e4
# Fri, 15 May 2020 17:44:18 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Fri, 15 May 2020 17:44:19 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Fri, 15 May 2020 17:44:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 15 May 2020 17:44:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2020 17:44:22 GMT
USER memcache
# Fri, 15 May 2020 17:44:22 GMT
EXPOSE 11211
# Fri, 15 May 2020 17:44:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d22357c747999d33ec7501da2c05aa9e95079ebddefbcb326976c5ed5b176b3f`  
		Last Modified: Fri, 15 May 2020 04:57:10 GMT  
		Size: 25.8 MB (25764292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3115b8e8662ac555af11c478baee0fdb5f01104502d56f06b7ee41220b4e657b`  
		Last Modified: Fri, 15 May 2020 17:44:41 GMT  
		Size: 5.0 KB (4983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41913d1e9348454334017c944d80aa47d1943fd04638d62d37423770d3018479`  
		Last Modified: Fri, 15 May 2020 17:44:42 GMT  
		Size: 1.8 MB (1776052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:210fa0b24a197a98c8240a2894b51f793cfe40394f1a250e378db74d05f10344`  
		Last Modified: Fri, 15 May 2020 17:44:42 GMT  
		Size: 1.2 MB (1182589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deeb403a026c300b2dfbbffbc1c02dfb7ffc52f664c04f1fe05d5e362d6891de`  
		Last Modified: Fri, 15 May 2020 17:44:41 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:452891cb460b1154e1f384584fa272280ac33180517761a6a2cb02bf0d097798`  
		Last Modified: Fri, 15 May 2020 17:44:41 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:latest` - linux; ppc64le

```console
$ docker pull memcached@sha256:ebb6ee75ae5f1f05a1b478f046250f3994be0f2df9cf31a180d88d656e083a73
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.1 MB (34065762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4032d7ff6f5fdbba453cb43a6b5cc8a00cad2e79ce57d17aa438da99b0cb06b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 13 May 2020 22:22:26 GMT
ADD file:53bd5d792aec2fc8af7c0c836e64979e003b2cecaaf5153bd456cb4e97ba5a0e in / 
# Wed, 13 May 2020 22:22:29 GMT
CMD ["bash"]
# Wed, 13 May 2020 23:07:55 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 13 May 2020 23:08:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 23:08:15 GMT
ENV MEMCACHED_VERSION=1.6.6
# Wed, 13 May 2020 23:08:17 GMT
ENV MEMCACHED_SHA1=d8895b12dc9fc82b389f1713e2c09cc6ca3d03e4
# Wed, 13 May 2020 23:19:45 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 13 May 2020 23:19:46 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 13 May 2020 23:19:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 13 May 2020 23:19:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2020 23:19:59 GMT
USER memcache
# Wed, 13 May 2020 23:20:01 GMT
EXPOSE 11211
# Wed, 13 May 2020 23:20:03 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d23cb84f4d6399958c00ec4c457e9c302763ee7dd86a0fb5540f75ed550c17d6`  
		Last Modified: Wed, 13 May 2020 22:57:57 GMT  
		Size: 30.5 MB (30518701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b9e5e25ad65245dbeeaeb9a78d8ce6b1a9b034b85b8ce6f97b84fd4e3c9952`  
		Last Modified: Wed, 13 May 2020 23:20:22 GMT  
		Size: 5.0 KB (4981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bfd32383c7dbd73000e7d7973f01efca5898a071186eb9bf92329164aa41fc4`  
		Last Modified: Wed, 13 May 2020 23:20:23 GMT  
		Size: 2.3 MB (2322682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16d4bb064ec887fac5ffb843f201f7f2a3526cbbb64b28a89e695e90d2e9deb`  
		Last Modified: Wed, 13 May 2020 23:20:24 GMT  
		Size: 1.2 MB (1218987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080c329faf596ce4cde8dccf5aa9ea4098515398ea02c950063c800602006ef8`  
		Last Modified: Wed, 13 May 2020 23:20:22 GMT  
		Size: 290.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c8fd322f0f4277ec0cc8bef51221c062db7cc318f94f1a09ed03af429443e1`  
		Last Modified: Wed, 13 May 2020 23:20:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:latest` - linux; s390x

```console
$ docker pull memcached@sha256:f595f34c60ca6f05b8efa2ce73782d5aee650e5f640420f7c993595cedfaa066
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.8 MB (28789343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b9cda6d8bb0400fda850c01d91b5bc9d92cb22eb2c9a72ada8ef448f126601b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 14 May 2020 23:06:40 GMT
ADD file:a29e647b8dccf726d8610d8c599d6727d6145426f9374720b985fc9be9ac906c in / 
# Thu, 14 May 2020 23:06:41 GMT
CMD ["bash"]
# Fri, 15 May 2020 07:40:42 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Fri, 15 May 2020 07:40:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 07:40:46 GMT
ENV MEMCACHED_VERSION=1.6.6
# Fri, 15 May 2020 07:40:47 GMT
ENV MEMCACHED_SHA1=d8895b12dc9fc82b389f1713e2c09cc6ca3d03e4
# Fri, 15 May 2020 07:49:46 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Fri, 15 May 2020 07:49:47 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Fri, 15 May 2020 07:49:48 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 15 May 2020 07:49:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2020 07:49:48 GMT
USER memcache
# Fri, 15 May 2020 07:49:48 GMT
EXPOSE 11211
# Fri, 15 May 2020 07:49:48 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bdb298e230dde60bfce8a476ae8ea8988828f7ec9f5452f38f46102a609f57c1`  
		Last Modified: Thu, 14 May 2020 23:11:24 GMT  
		Size: 25.7 MB (25712933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2355a11bb694657b7d9099110abd9b2a694c19a6040a45395af99d2a1ecbbec8`  
		Last Modified: Fri, 15 May 2020 07:50:09 GMT  
		Size: 5.0 KB (5026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:380c4d85bdd1a6096767de4ae39c2ed333a87e7858d66ae406f7dc8347b487a9`  
		Last Modified: Fri, 15 May 2020 07:50:15 GMT  
		Size: 1.9 MB (1886038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6211acebbe647028f26379bba0952f4514e29a723d31a0c5252b247c986e4dea`  
		Last Modified: Fri, 15 May 2020 07:50:09 GMT  
		Size: 1.2 MB (1184938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44c2a07a438f4bac43aa1a9ff5c67d84a2465190356c586c61a4001eafae68f8`  
		Last Modified: Fri, 15 May 2020 07:50:24 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ac2886035ee7045e086d59dc18ff6d5d8eefc5ff28a67e7aeaa0fc1b742ef84`  
		Last Modified: Fri, 15 May 2020 07:50:25 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
