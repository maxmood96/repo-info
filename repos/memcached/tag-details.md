<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `memcached`

-	[`memcached:1`](#memcached1)
-	[`memcached:1.6`](#memcached16)
-	[`memcached:1.6.6`](#memcached166)
-	[`memcached:1.6.6-alpine`](#memcached166-alpine)
-	[`memcached:1.6-alpine`](#memcached16-alpine)
-	[`memcached:1-alpine`](#memcached1-alpine)
-	[`memcached:alpine`](#memcachedalpine)
-	[`memcached:latest`](#memcachedlatest)

## `memcached:1`

```console
$ docker pull memcached@sha256:960a35d3fa6876225014a159850d1cb2067a22a924361bf40245846a939ae10b
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
$ docker pull memcached@sha256:4883efd6cfc85109bebdbca6e121dc2aa8095f5157f28407f86a2e5c2451bed6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 MB (30493622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddb9497b15e51ab6a3d1e51c0f943f3aefd6d7e18bf3029b6754b86db9ce67d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2020 01:20:56 GMT
ADD file:4d35f6c8bbbe6801cc5f44989730fb6d349a644ecb36eca481e7df25842d6321 in / 
# Tue, 09 Jun 2020 01:20:56 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:09:50 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 09 Jun 2020 07:09:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 07:09:55 GMT
ENV MEMCACHED_VERSION=1.6.6
# Tue, 09 Jun 2020 07:09:56 GMT
ENV MEMCACHED_SHA1=d8895b12dc9fc82b389f1713e2c09cc6ca3d03e4
# Tue, 09 Jun 2020 07:19:35 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 09 Jun 2020 07:19:35 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 09 Jun 2020 07:19:36 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 09 Jun 2020 07:19:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2020 07:19:36 GMT
USER memcache
# Tue, 09 Jun 2020 07:19:36 GMT
EXPOSE 11211
# Tue, 09 Jun 2020 07:19:36 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8559a31e96f442f2c7b6da49d6c84705f98a39d8be10b3f5f14821d0ee8417df`  
		Last Modified: Tue, 09 Jun 2020 01:25:50 GMT  
		Size: 27.1 MB (27098265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12f77f53de123f2d7381bf86a4a557eec07f2228f8d89b370535571abd3a73b6`  
		Last Modified: Tue, 09 Jun 2020 07:19:51 GMT  
		Size: 5.0 KB (4979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d4b924046de20905ddbdff30ce6ad8e886c078d3f37c5c65821fac3d7c82790`  
		Last Modified: Tue, 09 Jun 2020 07:19:52 GMT  
		Size: 2.2 MB (2196411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e09bb1c847d482fc3e3ffafe59cab644788c34accaa04a99fbddf6041eb36a38`  
		Last Modified: Tue, 09 Jun 2020 07:19:51 GMT  
		Size: 1.2 MB (1193561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba5fe779b315da0e76b031a17cbe96d16eb55dc9d1013834eaee74742aacf84f`  
		Last Modified: Tue, 09 Jun 2020 07:19:51 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df0fd9fcff94218c4182c328d693e7f79f185a577db6f8c94495011d7d21a726`  
		Last Modified: Tue, 09 Jun 2020 07:19:50 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1` - linux; arm variant v5

```console
$ docker pull memcached@sha256:0032271a53786587f2d8ce5e200da92642381a13f8e986846444978aede2f033
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.9 MB (27902256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2fabf24619ac13321a89500b1cbc36167c5effdd82a52ce4ab61218266a23fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2020 00:51:58 GMT
ADD file:7fde417d1c70a9ef2b4e468f6e2ee4cbd3f340fb2d5b67ede087c81520c95f4a in / 
# Tue, 09 Jun 2020 00:51:59 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 02:22:42 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 09 Jun 2020 02:22:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 02:22:57 GMT
ENV MEMCACHED_VERSION=1.6.6
# Tue, 09 Jun 2020 02:22:58 GMT
ENV MEMCACHED_SHA1=d8895b12dc9fc82b389f1713e2c09cc6ca3d03e4
# Tue, 09 Jun 2020 02:33:31 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 09 Jun 2020 02:33:32 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 09 Jun 2020 02:33:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 09 Jun 2020 02:33:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2020 02:33:36 GMT
USER memcache
# Tue, 09 Jun 2020 02:33:37 GMT
EXPOSE 11211
# Tue, 09 Jun 2020 02:33:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5b11fc09c1a26b11a7df7d593adf43baff53c5cdba71cf8a87ae4a6dd17eb52c`  
		Last Modified: Tue, 09 Jun 2020 00:59:24 GMT  
		Size: 24.8 MB (24837249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3baa3b116d24495c921f946ba122d5d463f3cf18626b0a80eb3f0bf9c4b6fe88`  
		Last Modified: Tue, 09 Jun 2020 02:34:05 GMT  
		Size: 4.9 KB (4892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c14a1ca330de132590916156f832d30211e6a8bfdb7f8e1dbda8dfdec102868b`  
		Last Modified: Tue, 09 Jun 2020 02:33:59 GMT  
		Size: 1.9 MB (1896798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b0e6e0e7ce0edef15dfccb8720e6c174a6fbc836fa16d483777c2e5b2bd0463`  
		Last Modified: Tue, 09 Jun 2020 02:33:59 GMT  
		Size: 1.2 MB (1162911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb4bdac6e198938d837ced8ba070de21a57812e113dd004d73ce5b1f2f21cd1`  
		Last Modified: Tue, 09 Jun 2020 02:33:59 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb5331ba343b59e5da9dc29eaaac2fa7bbd864b5607219c05aaadafb20d14dea`  
		Last Modified: Tue, 09 Jun 2020 02:33:59 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1` - linux; arm variant v7

```console
$ docker pull memcached@sha256:208c4d971048d73ce06174e8f5fa949e63e9a44e10f24e429e86478137c26c93
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25657276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ee4792808615b8ebe900de30833bca0acab941721546afc53b9599ebc2bbc12`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2020 01:01:24 GMT
ADD file:a35ca31d2a743d6a1738b1652f4f06c789abbca314d120f0e7e748311ac09ed2 in / 
# Tue, 09 Jun 2020 01:01:30 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 04:34:44 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 09 Jun 2020 04:34:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 04:34:54 GMT
ENV MEMCACHED_VERSION=1.6.6
# Tue, 09 Jun 2020 04:34:55 GMT
ENV MEMCACHED_SHA1=d8895b12dc9fc82b389f1713e2c09cc6ca3d03e4
# Tue, 09 Jun 2020 04:45:19 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 09 Jun 2020 04:45:20 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 09 Jun 2020 04:45:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 09 Jun 2020 04:45:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2020 04:45:23 GMT
USER memcache
# Tue, 09 Jun 2020 04:45:24 GMT
EXPOSE 11211
# Tue, 09 Jun 2020 04:45:24 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2dd003996c9ab82cac8112be0a4c04068e666e7a5d0cce3c65fb8f064de284e7`  
		Last Modified: Tue, 09 Jun 2020 01:10:25 GMT  
		Size: 22.7 MB (22705913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7558d3648391e15793448c35242f8b4fe3a52dab471b01435aefe6b66a2877d5`  
		Last Modified: Tue, 09 Jun 2020 04:45:54 GMT  
		Size: 4.9 KB (4897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13456188db29b97fae4ae70b260328de60b0bbfd9c0bc7c07e5e3d0555e3cd8`  
		Last Modified: Tue, 09 Jun 2020 04:45:54 GMT  
		Size: 1.8 MB (1811479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b7af48e3409ed86c6b2c330d38c8d31666b7852d2768e081d6aab0db9b9964`  
		Last Modified: Tue, 09 Jun 2020 04:45:55 GMT  
		Size: 1.1 MB (1134581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e94ff05fa5ccad573fbe816e4329a3cee522aa7d4d6050fe059e81748f5427e`  
		Last Modified: Tue, 09 Jun 2020 04:45:54 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d417f210bb27bb8c73a3b4fb69a7d0b0a4af17fca9dc4a46d476868546c3ab4`  
		Last Modified: Tue, 09 Jun 2020 04:45:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1` - linux; arm64 variant v8

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

### `memcached:1` - linux; 386

```console
$ docker pull memcached@sha256:cf852d337b092501b99a68fd99fa098e3158f5c906a46346afbf283b5fe842a2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31165510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e46e67a23b0df4e0a189a624fd19acfddfb18da9babf02339f500cf08deece9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2020 01:39:49 GMT
ADD file:9fb8fd8bf970c4134f555964fe485a3baa84f1d4c91c5aa35276c24404de9d5d in / 
# Tue, 09 Jun 2020 01:39:49 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:13:54 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 09 Jun 2020 07:14:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 07:14:00 GMT
ENV MEMCACHED_VERSION=1.6.6
# Tue, 09 Jun 2020 07:14:00 GMT
ENV MEMCACHED_SHA1=d8895b12dc9fc82b389f1713e2c09cc6ca3d03e4
# Tue, 09 Jun 2020 07:23:19 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 09 Jun 2020 07:23:20 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 09 Jun 2020 07:23:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 09 Jun 2020 07:23:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2020 07:23:21 GMT
USER memcache
# Tue, 09 Jun 2020 07:23:21 GMT
EXPOSE 11211
# Tue, 09 Jun 2020 07:23:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:860f8957d8be856e2235a28e49fc4dca17254951e0eb67d760769755656f5cad`  
		Last Modified: Tue, 09 Jun 2020 01:45:01 GMT  
		Size: 27.8 MB (27754909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177c77c201722fd2e38ce7eb3a8ed9e3626b787675b4f97e8b30dc814b5d8e0f`  
		Last Modified: Tue, 09 Jun 2020 07:23:39 GMT  
		Size: 4.9 KB (4888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c70883b4ec6865b74674af4157d587f6931be09be0064b4e839d84ece1f752c`  
		Last Modified: Tue, 09 Jun 2020 07:23:40 GMT  
		Size: 2.2 MB (2208123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:361fde9e5eba8562e2ba9fbb13637811f7ab77ed8154567ea7936e738712c10a`  
		Last Modified: Tue, 09 Jun 2020 07:23:40 GMT  
		Size: 1.2 MB (1197183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b45cbcad6d03b87559d072f7de237e45b57f43aa3cda322a92efd95db143bbc6`  
		Last Modified: Tue, 09 Jun 2020 07:23:39 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d26134208cbdd2c15c5eb835332adb873def0e0b00d41ed26878d5a6668e059`  
		Last Modified: Tue, 09 Jun 2020 07:23:39 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1` - linux; mips64le

```console
$ docker pull memcached@sha256:f549c5445d205ef1bb085e26731cbb587c5d0b28e3ee334cf94a089f1edd5299
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.7 MB (28727890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:195974ad8b777f8d1cb7fc6662ed73f1dfcb4adae667b145bfbbdc135a35f83f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2020 01:10:06 GMT
ADD file:faf18b832680e98050b98c329add242425904e64c6a5a491c22d33e9417ef323 in / 
# Tue, 09 Jun 2020 01:10:06 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 02:47:55 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 09 Jun 2020 02:48:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 02:48:09 GMT
ENV MEMCACHED_VERSION=1.6.6
# Tue, 09 Jun 2020 02:48:09 GMT
ENV MEMCACHED_SHA1=d8895b12dc9fc82b389f1713e2c09cc6ca3d03e4
# Tue, 09 Jun 2020 03:00:07 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 09 Jun 2020 03:00:07 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 09 Jun 2020 03:00:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 09 Jun 2020 03:00:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2020 03:00:10 GMT
USER memcache
# Tue, 09 Jun 2020 03:00:10 GMT
EXPOSE 11211
# Tue, 09 Jun 2020 03:00:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:76f2a0c8ea98ebd699a77ced9c677e97cd54b038a8c5e89670af78f38b047b33`  
		Last Modified: Tue, 09 Jun 2020 01:18:14 GMT  
		Size: 25.8 MB (25764040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaea43187ee39f4dcd055f5a5ef4a57ed46a2c369ece86cd6a0cbbe0d649a185`  
		Last Modified: Tue, 09 Jun 2020 03:00:37 GMT  
		Size: 5.0 KB (4976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d990cccfa6753239cf27654288742581cb106cc1dac9e6dbe774114b185810`  
		Last Modified: Tue, 09 Jun 2020 03:00:38 GMT  
		Size: 1.8 MB (1776013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8377e577748912f253e08d4980e821ac6204d4dc430cff1238bbc01ea6c7ca`  
		Last Modified: Tue, 09 Jun 2020 03:00:37 GMT  
		Size: 1.2 MB (1182454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45fc1e75da507493f88c70b2acd4274a2ebe28bac45a4d9d774f1b6fb863b010`  
		Last Modified: Tue, 09 Jun 2020 03:00:33 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23848a16b8c2670e004ce1a89e3d51af6c75e11d2dd1c86c89e89f1c55821032`  
		Last Modified: Tue, 09 Jun 2020 03:00:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1` - linux; ppc64le

```console
$ docker pull memcached@sha256:9d74db6d0c506cd7b5171129f6cb702277aaa191e7bafd242c551e26b7e582a2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.1 MB (34071646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caf1d9ee7c1f4c75ff401acd07ac5e28aa61e674424f1bf57ac75673845d420e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2020 01:22:34 GMT
ADD file:796aad1a35ba276b8cccc19987c152a713db101b2b65e30923db753f5b7f4b0f in / 
# Tue, 09 Jun 2020 01:22:38 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 04:23:19 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 09 Jun 2020 04:23:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 04:23:43 GMT
ENV MEMCACHED_VERSION=1.6.6
# Tue, 09 Jun 2020 04:23:47 GMT
ENV MEMCACHED_SHA1=d8895b12dc9fc82b389f1713e2c09cc6ca3d03e4
# Tue, 09 Jun 2020 04:35:57 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 09 Jun 2020 04:36:01 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 09 Jun 2020 04:36:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 09 Jun 2020 04:36:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2020 04:36:21 GMT
USER memcache
# Tue, 09 Jun 2020 04:36:26 GMT
EXPOSE 11211
# Tue, 09 Jun 2020 04:36:32 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:63dbb66c5119bb5086d9e6fb6b154211afc20b44ed136ab7df808f6044cfc6f1`  
		Last Modified: Tue, 09 Jun 2020 01:31:04 GMT  
		Size: 30.5 MB (30524405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:326347d3599c113aed8b360975de1e1295d880747ab63b945e59748ff4e00e7f`  
		Last Modified: Tue, 09 Jun 2020 04:37:10 GMT  
		Size: 5.0 KB (4980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b3c6b0b46229c12b05433642c55de042b24a1364fd631996450f9a4bb136143`  
		Last Modified: Tue, 09 Jun 2020 04:37:10 GMT  
		Size: 2.3 MB (2322714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:716f59d7781a40e402cd8add331e26fc33fbaab6a82614c43746b1afdf315747`  
		Last Modified: Tue, 09 Jun 2020 04:37:10 GMT  
		Size: 1.2 MB (1219139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b63b4e5e82673252ff53e7021ac30af1147b4a81f99a82aa1a3c58085688666`  
		Last Modified: Tue, 09 Jun 2020 04:37:10 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abf841a99428dea3a743f5fde752d2ba68f050307880829b6c354c5e5bcdf04e`  
		Last Modified: Tue, 09 Jun 2020 04:37:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1` - linux; s390x

```console
$ docker pull memcached@sha256:e481d6155413e4b844009223fa04cca68b15e430b4e5476a0e9967f49af57a50
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.8 MB (28789009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd9a8cff3ec775f7b2c039af1fb74ca8706705a6715c681797cd43f02f82090a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2020 01:42:37 GMT
ADD file:b21d426de40a194c6c76ed27593f33fb1ea470e15d4d43b00d7601472110de1a in / 
# Tue, 09 Jun 2020 01:42:38 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 03:40:46 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 09 Jun 2020 03:40:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 03:40:50 GMT
ENV MEMCACHED_VERSION=1.6.6
# Tue, 09 Jun 2020 03:40:50 GMT
ENV MEMCACHED_SHA1=d8895b12dc9fc82b389f1713e2c09cc6ca3d03e4
# Tue, 09 Jun 2020 03:49:43 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 09 Jun 2020 03:49:43 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 09 Jun 2020 03:49:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 09 Jun 2020 03:49:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2020 03:49:44 GMT
USER memcache
# Tue, 09 Jun 2020 03:49:44 GMT
EXPOSE 11211
# Tue, 09 Jun 2020 03:49:44 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:405e75bf6bb0104d67fcebf58e07cd21bf344589df9c1a41c00354a60ea3a604`  
		Last Modified: Tue, 09 Jun 2020 01:46:30 GMT  
		Size: 25.7 MB (25712668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2c03af295f2075ceec6e6cc9874e8666d63a3b26614e659f1396a367f9e2ebc`  
		Last Modified: Tue, 09 Jun 2020 03:50:08 GMT  
		Size: 5.0 KB (5023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989e958beedef1b77252896a7ad5fba801dcef12cde52098e6a9d46a57ec6d9b`  
		Last Modified: Tue, 09 Jun 2020 03:50:08 GMT  
		Size: 1.9 MB (1886033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a68df8456455057906a59f6ff163a22e695cf310443f17f2af2a3742d1e1eaaf`  
		Last Modified: Tue, 09 Jun 2020 03:50:13 GMT  
		Size: 1.2 MB (1184878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7cd9a3bb1b818c1b06baad270500facbfcbaab3102aa9fb203b7aa09fbf8be3`  
		Last Modified: Tue, 09 Jun 2020 03:50:23 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab09b03baf0f78a40dff16e0620f3af6bd5e050654d20b3a1c073fd88d1dff42`  
		Last Modified: Tue, 09 Jun 2020 03:50:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:1.6`

```console
$ docker pull memcached@sha256:960a35d3fa6876225014a159850d1cb2067a22a924361bf40245846a939ae10b
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
$ docker pull memcached@sha256:4883efd6cfc85109bebdbca6e121dc2aa8095f5157f28407f86a2e5c2451bed6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 MB (30493622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddb9497b15e51ab6a3d1e51c0f943f3aefd6d7e18bf3029b6754b86db9ce67d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2020 01:20:56 GMT
ADD file:4d35f6c8bbbe6801cc5f44989730fb6d349a644ecb36eca481e7df25842d6321 in / 
# Tue, 09 Jun 2020 01:20:56 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:09:50 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 09 Jun 2020 07:09:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 07:09:55 GMT
ENV MEMCACHED_VERSION=1.6.6
# Tue, 09 Jun 2020 07:09:56 GMT
ENV MEMCACHED_SHA1=d8895b12dc9fc82b389f1713e2c09cc6ca3d03e4
# Tue, 09 Jun 2020 07:19:35 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 09 Jun 2020 07:19:35 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 09 Jun 2020 07:19:36 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 09 Jun 2020 07:19:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2020 07:19:36 GMT
USER memcache
# Tue, 09 Jun 2020 07:19:36 GMT
EXPOSE 11211
# Tue, 09 Jun 2020 07:19:36 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8559a31e96f442f2c7b6da49d6c84705f98a39d8be10b3f5f14821d0ee8417df`  
		Last Modified: Tue, 09 Jun 2020 01:25:50 GMT  
		Size: 27.1 MB (27098265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12f77f53de123f2d7381bf86a4a557eec07f2228f8d89b370535571abd3a73b6`  
		Last Modified: Tue, 09 Jun 2020 07:19:51 GMT  
		Size: 5.0 KB (4979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d4b924046de20905ddbdff30ce6ad8e886c078d3f37c5c65821fac3d7c82790`  
		Last Modified: Tue, 09 Jun 2020 07:19:52 GMT  
		Size: 2.2 MB (2196411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e09bb1c847d482fc3e3ffafe59cab644788c34accaa04a99fbddf6041eb36a38`  
		Last Modified: Tue, 09 Jun 2020 07:19:51 GMT  
		Size: 1.2 MB (1193561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba5fe779b315da0e76b031a17cbe96d16eb55dc9d1013834eaee74742aacf84f`  
		Last Modified: Tue, 09 Jun 2020 07:19:51 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df0fd9fcff94218c4182c328d693e7f79f185a577db6f8c94495011d7d21a726`  
		Last Modified: Tue, 09 Jun 2020 07:19:50 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6` - linux; arm variant v5

```console
$ docker pull memcached@sha256:0032271a53786587f2d8ce5e200da92642381a13f8e986846444978aede2f033
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.9 MB (27902256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2fabf24619ac13321a89500b1cbc36167c5effdd82a52ce4ab61218266a23fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2020 00:51:58 GMT
ADD file:7fde417d1c70a9ef2b4e468f6e2ee4cbd3f340fb2d5b67ede087c81520c95f4a in / 
# Tue, 09 Jun 2020 00:51:59 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 02:22:42 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 09 Jun 2020 02:22:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 02:22:57 GMT
ENV MEMCACHED_VERSION=1.6.6
# Tue, 09 Jun 2020 02:22:58 GMT
ENV MEMCACHED_SHA1=d8895b12dc9fc82b389f1713e2c09cc6ca3d03e4
# Tue, 09 Jun 2020 02:33:31 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 09 Jun 2020 02:33:32 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 09 Jun 2020 02:33:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 09 Jun 2020 02:33:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2020 02:33:36 GMT
USER memcache
# Tue, 09 Jun 2020 02:33:37 GMT
EXPOSE 11211
# Tue, 09 Jun 2020 02:33:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5b11fc09c1a26b11a7df7d593adf43baff53c5cdba71cf8a87ae4a6dd17eb52c`  
		Last Modified: Tue, 09 Jun 2020 00:59:24 GMT  
		Size: 24.8 MB (24837249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3baa3b116d24495c921f946ba122d5d463f3cf18626b0a80eb3f0bf9c4b6fe88`  
		Last Modified: Tue, 09 Jun 2020 02:34:05 GMT  
		Size: 4.9 KB (4892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c14a1ca330de132590916156f832d30211e6a8bfdb7f8e1dbda8dfdec102868b`  
		Last Modified: Tue, 09 Jun 2020 02:33:59 GMT  
		Size: 1.9 MB (1896798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b0e6e0e7ce0edef15dfccb8720e6c174a6fbc836fa16d483777c2e5b2bd0463`  
		Last Modified: Tue, 09 Jun 2020 02:33:59 GMT  
		Size: 1.2 MB (1162911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb4bdac6e198938d837ced8ba070de21a57812e113dd004d73ce5b1f2f21cd1`  
		Last Modified: Tue, 09 Jun 2020 02:33:59 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb5331ba343b59e5da9dc29eaaac2fa7bbd864b5607219c05aaadafb20d14dea`  
		Last Modified: Tue, 09 Jun 2020 02:33:59 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6` - linux; arm variant v7

```console
$ docker pull memcached@sha256:208c4d971048d73ce06174e8f5fa949e63e9a44e10f24e429e86478137c26c93
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25657276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ee4792808615b8ebe900de30833bca0acab941721546afc53b9599ebc2bbc12`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2020 01:01:24 GMT
ADD file:a35ca31d2a743d6a1738b1652f4f06c789abbca314d120f0e7e748311ac09ed2 in / 
# Tue, 09 Jun 2020 01:01:30 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 04:34:44 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 09 Jun 2020 04:34:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 04:34:54 GMT
ENV MEMCACHED_VERSION=1.6.6
# Tue, 09 Jun 2020 04:34:55 GMT
ENV MEMCACHED_SHA1=d8895b12dc9fc82b389f1713e2c09cc6ca3d03e4
# Tue, 09 Jun 2020 04:45:19 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 09 Jun 2020 04:45:20 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 09 Jun 2020 04:45:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 09 Jun 2020 04:45:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2020 04:45:23 GMT
USER memcache
# Tue, 09 Jun 2020 04:45:24 GMT
EXPOSE 11211
# Tue, 09 Jun 2020 04:45:24 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2dd003996c9ab82cac8112be0a4c04068e666e7a5d0cce3c65fb8f064de284e7`  
		Last Modified: Tue, 09 Jun 2020 01:10:25 GMT  
		Size: 22.7 MB (22705913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7558d3648391e15793448c35242f8b4fe3a52dab471b01435aefe6b66a2877d5`  
		Last Modified: Tue, 09 Jun 2020 04:45:54 GMT  
		Size: 4.9 KB (4897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13456188db29b97fae4ae70b260328de60b0bbfd9c0bc7c07e5e3d0555e3cd8`  
		Last Modified: Tue, 09 Jun 2020 04:45:54 GMT  
		Size: 1.8 MB (1811479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b7af48e3409ed86c6b2c330d38c8d31666b7852d2768e081d6aab0db9b9964`  
		Last Modified: Tue, 09 Jun 2020 04:45:55 GMT  
		Size: 1.1 MB (1134581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e94ff05fa5ccad573fbe816e4329a3cee522aa7d4d6050fe059e81748f5427e`  
		Last Modified: Tue, 09 Jun 2020 04:45:54 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d417f210bb27bb8c73a3b4fb69a7d0b0a4af17fca9dc4a46d476868546c3ab4`  
		Last Modified: Tue, 09 Jun 2020 04:45:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6` - linux; arm64 variant v8

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

### `memcached:1.6` - linux; 386

```console
$ docker pull memcached@sha256:cf852d337b092501b99a68fd99fa098e3158f5c906a46346afbf283b5fe842a2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31165510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e46e67a23b0df4e0a189a624fd19acfddfb18da9babf02339f500cf08deece9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2020 01:39:49 GMT
ADD file:9fb8fd8bf970c4134f555964fe485a3baa84f1d4c91c5aa35276c24404de9d5d in / 
# Tue, 09 Jun 2020 01:39:49 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:13:54 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 09 Jun 2020 07:14:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 07:14:00 GMT
ENV MEMCACHED_VERSION=1.6.6
# Tue, 09 Jun 2020 07:14:00 GMT
ENV MEMCACHED_SHA1=d8895b12dc9fc82b389f1713e2c09cc6ca3d03e4
# Tue, 09 Jun 2020 07:23:19 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 09 Jun 2020 07:23:20 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 09 Jun 2020 07:23:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 09 Jun 2020 07:23:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2020 07:23:21 GMT
USER memcache
# Tue, 09 Jun 2020 07:23:21 GMT
EXPOSE 11211
# Tue, 09 Jun 2020 07:23:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:860f8957d8be856e2235a28e49fc4dca17254951e0eb67d760769755656f5cad`  
		Last Modified: Tue, 09 Jun 2020 01:45:01 GMT  
		Size: 27.8 MB (27754909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177c77c201722fd2e38ce7eb3a8ed9e3626b787675b4f97e8b30dc814b5d8e0f`  
		Last Modified: Tue, 09 Jun 2020 07:23:39 GMT  
		Size: 4.9 KB (4888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c70883b4ec6865b74674af4157d587f6931be09be0064b4e839d84ece1f752c`  
		Last Modified: Tue, 09 Jun 2020 07:23:40 GMT  
		Size: 2.2 MB (2208123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:361fde9e5eba8562e2ba9fbb13637811f7ab77ed8154567ea7936e738712c10a`  
		Last Modified: Tue, 09 Jun 2020 07:23:40 GMT  
		Size: 1.2 MB (1197183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b45cbcad6d03b87559d072f7de237e45b57f43aa3cda322a92efd95db143bbc6`  
		Last Modified: Tue, 09 Jun 2020 07:23:39 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d26134208cbdd2c15c5eb835332adb873def0e0b00d41ed26878d5a6668e059`  
		Last Modified: Tue, 09 Jun 2020 07:23:39 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6` - linux; mips64le

```console
$ docker pull memcached@sha256:f549c5445d205ef1bb085e26731cbb587c5d0b28e3ee334cf94a089f1edd5299
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.7 MB (28727890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:195974ad8b777f8d1cb7fc6662ed73f1dfcb4adae667b145bfbbdc135a35f83f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2020 01:10:06 GMT
ADD file:faf18b832680e98050b98c329add242425904e64c6a5a491c22d33e9417ef323 in / 
# Tue, 09 Jun 2020 01:10:06 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 02:47:55 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 09 Jun 2020 02:48:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 02:48:09 GMT
ENV MEMCACHED_VERSION=1.6.6
# Tue, 09 Jun 2020 02:48:09 GMT
ENV MEMCACHED_SHA1=d8895b12dc9fc82b389f1713e2c09cc6ca3d03e4
# Tue, 09 Jun 2020 03:00:07 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 09 Jun 2020 03:00:07 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 09 Jun 2020 03:00:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 09 Jun 2020 03:00:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2020 03:00:10 GMT
USER memcache
# Tue, 09 Jun 2020 03:00:10 GMT
EXPOSE 11211
# Tue, 09 Jun 2020 03:00:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:76f2a0c8ea98ebd699a77ced9c677e97cd54b038a8c5e89670af78f38b047b33`  
		Last Modified: Tue, 09 Jun 2020 01:18:14 GMT  
		Size: 25.8 MB (25764040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaea43187ee39f4dcd055f5a5ef4a57ed46a2c369ece86cd6a0cbbe0d649a185`  
		Last Modified: Tue, 09 Jun 2020 03:00:37 GMT  
		Size: 5.0 KB (4976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d990cccfa6753239cf27654288742581cb106cc1dac9e6dbe774114b185810`  
		Last Modified: Tue, 09 Jun 2020 03:00:38 GMT  
		Size: 1.8 MB (1776013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8377e577748912f253e08d4980e821ac6204d4dc430cff1238bbc01ea6c7ca`  
		Last Modified: Tue, 09 Jun 2020 03:00:37 GMT  
		Size: 1.2 MB (1182454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45fc1e75da507493f88c70b2acd4274a2ebe28bac45a4d9d774f1b6fb863b010`  
		Last Modified: Tue, 09 Jun 2020 03:00:33 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23848a16b8c2670e004ce1a89e3d51af6c75e11d2dd1c86c89e89f1c55821032`  
		Last Modified: Tue, 09 Jun 2020 03:00:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6` - linux; ppc64le

```console
$ docker pull memcached@sha256:9d74db6d0c506cd7b5171129f6cb702277aaa191e7bafd242c551e26b7e582a2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.1 MB (34071646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caf1d9ee7c1f4c75ff401acd07ac5e28aa61e674424f1bf57ac75673845d420e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2020 01:22:34 GMT
ADD file:796aad1a35ba276b8cccc19987c152a713db101b2b65e30923db753f5b7f4b0f in / 
# Tue, 09 Jun 2020 01:22:38 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 04:23:19 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 09 Jun 2020 04:23:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 04:23:43 GMT
ENV MEMCACHED_VERSION=1.6.6
# Tue, 09 Jun 2020 04:23:47 GMT
ENV MEMCACHED_SHA1=d8895b12dc9fc82b389f1713e2c09cc6ca3d03e4
# Tue, 09 Jun 2020 04:35:57 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 09 Jun 2020 04:36:01 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 09 Jun 2020 04:36:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 09 Jun 2020 04:36:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2020 04:36:21 GMT
USER memcache
# Tue, 09 Jun 2020 04:36:26 GMT
EXPOSE 11211
# Tue, 09 Jun 2020 04:36:32 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:63dbb66c5119bb5086d9e6fb6b154211afc20b44ed136ab7df808f6044cfc6f1`  
		Last Modified: Tue, 09 Jun 2020 01:31:04 GMT  
		Size: 30.5 MB (30524405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:326347d3599c113aed8b360975de1e1295d880747ab63b945e59748ff4e00e7f`  
		Last Modified: Tue, 09 Jun 2020 04:37:10 GMT  
		Size: 5.0 KB (4980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b3c6b0b46229c12b05433642c55de042b24a1364fd631996450f9a4bb136143`  
		Last Modified: Tue, 09 Jun 2020 04:37:10 GMT  
		Size: 2.3 MB (2322714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:716f59d7781a40e402cd8add331e26fc33fbaab6a82614c43746b1afdf315747`  
		Last Modified: Tue, 09 Jun 2020 04:37:10 GMT  
		Size: 1.2 MB (1219139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b63b4e5e82673252ff53e7021ac30af1147b4a81f99a82aa1a3c58085688666`  
		Last Modified: Tue, 09 Jun 2020 04:37:10 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abf841a99428dea3a743f5fde752d2ba68f050307880829b6c354c5e5bcdf04e`  
		Last Modified: Tue, 09 Jun 2020 04:37:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6` - linux; s390x

```console
$ docker pull memcached@sha256:e481d6155413e4b844009223fa04cca68b15e430b4e5476a0e9967f49af57a50
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.8 MB (28789009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd9a8cff3ec775f7b2c039af1fb74ca8706705a6715c681797cd43f02f82090a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2020 01:42:37 GMT
ADD file:b21d426de40a194c6c76ed27593f33fb1ea470e15d4d43b00d7601472110de1a in / 
# Tue, 09 Jun 2020 01:42:38 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 03:40:46 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 09 Jun 2020 03:40:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 03:40:50 GMT
ENV MEMCACHED_VERSION=1.6.6
# Tue, 09 Jun 2020 03:40:50 GMT
ENV MEMCACHED_SHA1=d8895b12dc9fc82b389f1713e2c09cc6ca3d03e4
# Tue, 09 Jun 2020 03:49:43 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 09 Jun 2020 03:49:43 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 09 Jun 2020 03:49:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 09 Jun 2020 03:49:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2020 03:49:44 GMT
USER memcache
# Tue, 09 Jun 2020 03:49:44 GMT
EXPOSE 11211
# Tue, 09 Jun 2020 03:49:44 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:405e75bf6bb0104d67fcebf58e07cd21bf344589df9c1a41c00354a60ea3a604`  
		Last Modified: Tue, 09 Jun 2020 01:46:30 GMT  
		Size: 25.7 MB (25712668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2c03af295f2075ceec6e6cc9874e8666d63a3b26614e659f1396a367f9e2ebc`  
		Last Modified: Tue, 09 Jun 2020 03:50:08 GMT  
		Size: 5.0 KB (5023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989e958beedef1b77252896a7ad5fba801dcef12cde52098e6a9d46a57ec6d9b`  
		Last Modified: Tue, 09 Jun 2020 03:50:08 GMT  
		Size: 1.9 MB (1886033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a68df8456455057906a59f6ff163a22e695cf310443f17f2af2a3742d1e1eaaf`  
		Last Modified: Tue, 09 Jun 2020 03:50:13 GMT  
		Size: 1.2 MB (1184878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7cd9a3bb1b818c1b06baad270500facbfcbaab3102aa9fb203b7aa09fbf8be3`  
		Last Modified: Tue, 09 Jun 2020 03:50:23 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab09b03baf0f78a40dff16e0620f3af6bd5e050654d20b3a1c073fd88d1dff42`  
		Last Modified: Tue, 09 Jun 2020 03:50:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:1.6.6`

```console
$ docker pull memcached@sha256:960a35d3fa6876225014a159850d1cb2067a22a924361bf40245846a939ae10b
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

### `memcached:1.6.6` - linux; amd64

```console
$ docker pull memcached@sha256:4883efd6cfc85109bebdbca6e121dc2aa8095f5157f28407f86a2e5c2451bed6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 MB (30493622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddb9497b15e51ab6a3d1e51c0f943f3aefd6d7e18bf3029b6754b86db9ce67d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2020 01:20:56 GMT
ADD file:4d35f6c8bbbe6801cc5f44989730fb6d349a644ecb36eca481e7df25842d6321 in / 
# Tue, 09 Jun 2020 01:20:56 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:09:50 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 09 Jun 2020 07:09:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 07:09:55 GMT
ENV MEMCACHED_VERSION=1.6.6
# Tue, 09 Jun 2020 07:09:56 GMT
ENV MEMCACHED_SHA1=d8895b12dc9fc82b389f1713e2c09cc6ca3d03e4
# Tue, 09 Jun 2020 07:19:35 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 09 Jun 2020 07:19:35 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 09 Jun 2020 07:19:36 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 09 Jun 2020 07:19:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2020 07:19:36 GMT
USER memcache
# Tue, 09 Jun 2020 07:19:36 GMT
EXPOSE 11211
# Tue, 09 Jun 2020 07:19:36 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8559a31e96f442f2c7b6da49d6c84705f98a39d8be10b3f5f14821d0ee8417df`  
		Last Modified: Tue, 09 Jun 2020 01:25:50 GMT  
		Size: 27.1 MB (27098265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12f77f53de123f2d7381bf86a4a557eec07f2228f8d89b370535571abd3a73b6`  
		Last Modified: Tue, 09 Jun 2020 07:19:51 GMT  
		Size: 5.0 KB (4979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d4b924046de20905ddbdff30ce6ad8e886c078d3f37c5c65821fac3d7c82790`  
		Last Modified: Tue, 09 Jun 2020 07:19:52 GMT  
		Size: 2.2 MB (2196411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e09bb1c847d482fc3e3ffafe59cab644788c34accaa04a99fbddf6041eb36a38`  
		Last Modified: Tue, 09 Jun 2020 07:19:51 GMT  
		Size: 1.2 MB (1193561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba5fe779b315da0e76b031a17cbe96d16eb55dc9d1013834eaee74742aacf84f`  
		Last Modified: Tue, 09 Jun 2020 07:19:51 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df0fd9fcff94218c4182c328d693e7f79f185a577db6f8c94495011d7d21a726`  
		Last Modified: Tue, 09 Jun 2020 07:19:50 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.6` - linux; arm variant v5

```console
$ docker pull memcached@sha256:0032271a53786587f2d8ce5e200da92642381a13f8e986846444978aede2f033
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.9 MB (27902256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2fabf24619ac13321a89500b1cbc36167c5effdd82a52ce4ab61218266a23fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2020 00:51:58 GMT
ADD file:7fde417d1c70a9ef2b4e468f6e2ee4cbd3f340fb2d5b67ede087c81520c95f4a in / 
# Tue, 09 Jun 2020 00:51:59 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 02:22:42 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 09 Jun 2020 02:22:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 02:22:57 GMT
ENV MEMCACHED_VERSION=1.6.6
# Tue, 09 Jun 2020 02:22:58 GMT
ENV MEMCACHED_SHA1=d8895b12dc9fc82b389f1713e2c09cc6ca3d03e4
# Tue, 09 Jun 2020 02:33:31 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 09 Jun 2020 02:33:32 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 09 Jun 2020 02:33:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 09 Jun 2020 02:33:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2020 02:33:36 GMT
USER memcache
# Tue, 09 Jun 2020 02:33:37 GMT
EXPOSE 11211
# Tue, 09 Jun 2020 02:33:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5b11fc09c1a26b11a7df7d593adf43baff53c5cdba71cf8a87ae4a6dd17eb52c`  
		Last Modified: Tue, 09 Jun 2020 00:59:24 GMT  
		Size: 24.8 MB (24837249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3baa3b116d24495c921f946ba122d5d463f3cf18626b0a80eb3f0bf9c4b6fe88`  
		Last Modified: Tue, 09 Jun 2020 02:34:05 GMT  
		Size: 4.9 KB (4892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c14a1ca330de132590916156f832d30211e6a8bfdb7f8e1dbda8dfdec102868b`  
		Last Modified: Tue, 09 Jun 2020 02:33:59 GMT  
		Size: 1.9 MB (1896798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b0e6e0e7ce0edef15dfccb8720e6c174a6fbc836fa16d483777c2e5b2bd0463`  
		Last Modified: Tue, 09 Jun 2020 02:33:59 GMT  
		Size: 1.2 MB (1162911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb4bdac6e198938d837ced8ba070de21a57812e113dd004d73ce5b1f2f21cd1`  
		Last Modified: Tue, 09 Jun 2020 02:33:59 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb5331ba343b59e5da9dc29eaaac2fa7bbd864b5607219c05aaadafb20d14dea`  
		Last Modified: Tue, 09 Jun 2020 02:33:59 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.6` - linux; arm variant v7

```console
$ docker pull memcached@sha256:208c4d971048d73ce06174e8f5fa949e63e9a44e10f24e429e86478137c26c93
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25657276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ee4792808615b8ebe900de30833bca0acab941721546afc53b9599ebc2bbc12`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2020 01:01:24 GMT
ADD file:a35ca31d2a743d6a1738b1652f4f06c789abbca314d120f0e7e748311ac09ed2 in / 
# Tue, 09 Jun 2020 01:01:30 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 04:34:44 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 09 Jun 2020 04:34:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 04:34:54 GMT
ENV MEMCACHED_VERSION=1.6.6
# Tue, 09 Jun 2020 04:34:55 GMT
ENV MEMCACHED_SHA1=d8895b12dc9fc82b389f1713e2c09cc6ca3d03e4
# Tue, 09 Jun 2020 04:45:19 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 09 Jun 2020 04:45:20 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 09 Jun 2020 04:45:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 09 Jun 2020 04:45:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2020 04:45:23 GMT
USER memcache
# Tue, 09 Jun 2020 04:45:24 GMT
EXPOSE 11211
# Tue, 09 Jun 2020 04:45:24 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2dd003996c9ab82cac8112be0a4c04068e666e7a5d0cce3c65fb8f064de284e7`  
		Last Modified: Tue, 09 Jun 2020 01:10:25 GMT  
		Size: 22.7 MB (22705913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7558d3648391e15793448c35242f8b4fe3a52dab471b01435aefe6b66a2877d5`  
		Last Modified: Tue, 09 Jun 2020 04:45:54 GMT  
		Size: 4.9 KB (4897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13456188db29b97fae4ae70b260328de60b0bbfd9c0bc7c07e5e3d0555e3cd8`  
		Last Modified: Tue, 09 Jun 2020 04:45:54 GMT  
		Size: 1.8 MB (1811479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b7af48e3409ed86c6b2c330d38c8d31666b7852d2768e081d6aab0db9b9964`  
		Last Modified: Tue, 09 Jun 2020 04:45:55 GMT  
		Size: 1.1 MB (1134581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e94ff05fa5ccad573fbe816e4329a3cee522aa7d4d6050fe059e81748f5427e`  
		Last Modified: Tue, 09 Jun 2020 04:45:54 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d417f210bb27bb8c73a3b4fb69a7d0b0a4af17fca9dc4a46d476868546c3ab4`  
		Last Modified: Tue, 09 Jun 2020 04:45:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.6` - linux; arm64 variant v8

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

### `memcached:1.6.6` - linux; 386

```console
$ docker pull memcached@sha256:cf852d337b092501b99a68fd99fa098e3158f5c906a46346afbf283b5fe842a2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31165510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e46e67a23b0df4e0a189a624fd19acfddfb18da9babf02339f500cf08deece9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2020 01:39:49 GMT
ADD file:9fb8fd8bf970c4134f555964fe485a3baa84f1d4c91c5aa35276c24404de9d5d in / 
# Tue, 09 Jun 2020 01:39:49 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:13:54 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 09 Jun 2020 07:14:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 07:14:00 GMT
ENV MEMCACHED_VERSION=1.6.6
# Tue, 09 Jun 2020 07:14:00 GMT
ENV MEMCACHED_SHA1=d8895b12dc9fc82b389f1713e2c09cc6ca3d03e4
# Tue, 09 Jun 2020 07:23:19 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 09 Jun 2020 07:23:20 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 09 Jun 2020 07:23:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 09 Jun 2020 07:23:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2020 07:23:21 GMT
USER memcache
# Tue, 09 Jun 2020 07:23:21 GMT
EXPOSE 11211
# Tue, 09 Jun 2020 07:23:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:860f8957d8be856e2235a28e49fc4dca17254951e0eb67d760769755656f5cad`  
		Last Modified: Tue, 09 Jun 2020 01:45:01 GMT  
		Size: 27.8 MB (27754909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177c77c201722fd2e38ce7eb3a8ed9e3626b787675b4f97e8b30dc814b5d8e0f`  
		Last Modified: Tue, 09 Jun 2020 07:23:39 GMT  
		Size: 4.9 KB (4888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c70883b4ec6865b74674af4157d587f6931be09be0064b4e839d84ece1f752c`  
		Last Modified: Tue, 09 Jun 2020 07:23:40 GMT  
		Size: 2.2 MB (2208123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:361fde9e5eba8562e2ba9fbb13637811f7ab77ed8154567ea7936e738712c10a`  
		Last Modified: Tue, 09 Jun 2020 07:23:40 GMT  
		Size: 1.2 MB (1197183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b45cbcad6d03b87559d072f7de237e45b57f43aa3cda322a92efd95db143bbc6`  
		Last Modified: Tue, 09 Jun 2020 07:23:39 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d26134208cbdd2c15c5eb835332adb873def0e0b00d41ed26878d5a6668e059`  
		Last Modified: Tue, 09 Jun 2020 07:23:39 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.6` - linux; mips64le

```console
$ docker pull memcached@sha256:f549c5445d205ef1bb085e26731cbb587c5d0b28e3ee334cf94a089f1edd5299
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.7 MB (28727890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:195974ad8b777f8d1cb7fc6662ed73f1dfcb4adae667b145bfbbdc135a35f83f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2020 01:10:06 GMT
ADD file:faf18b832680e98050b98c329add242425904e64c6a5a491c22d33e9417ef323 in / 
# Tue, 09 Jun 2020 01:10:06 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 02:47:55 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 09 Jun 2020 02:48:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 02:48:09 GMT
ENV MEMCACHED_VERSION=1.6.6
# Tue, 09 Jun 2020 02:48:09 GMT
ENV MEMCACHED_SHA1=d8895b12dc9fc82b389f1713e2c09cc6ca3d03e4
# Tue, 09 Jun 2020 03:00:07 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 09 Jun 2020 03:00:07 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 09 Jun 2020 03:00:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 09 Jun 2020 03:00:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2020 03:00:10 GMT
USER memcache
# Tue, 09 Jun 2020 03:00:10 GMT
EXPOSE 11211
# Tue, 09 Jun 2020 03:00:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:76f2a0c8ea98ebd699a77ced9c677e97cd54b038a8c5e89670af78f38b047b33`  
		Last Modified: Tue, 09 Jun 2020 01:18:14 GMT  
		Size: 25.8 MB (25764040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaea43187ee39f4dcd055f5a5ef4a57ed46a2c369ece86cd6a0cbbe0d649a185`  
		Last Modified: Tue, 09 Jun 2020 03:00:37 GMT  
		Size: 5.0 KB (4976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d990cccfa6753239cf27654288742581cb106cc1dac9e6dbe774114b185810`  
		Last Modified: Tue, 09 Jun 2020 03:00:38 GMT  
		Size: 1.8 MB (1776013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8377e577748912f253e08d4980e821ac6204d4dc430cff1238bbc01ea6c7ca`  
		Last Modified: Tue, 09 Jun 2020 03:00:37 GMT  
		Size: 1.2 MB (1182454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45fc1e75da507493f88c70b2acd4274a2ebe28bac45a4d9d774f1b6fb863b010`  
		Last Modified: Tue, 09 Jun 2020 03:00:33 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23848a16b8c2670e004ce1a89e3d51af6c75e11d2dd1c86c89e89f1c55821032`  
		Last Modified: Tue, 09 Jun 2020 03:00:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.6` - linux; ppc64le

```console
$ docker pull memcached@sha256:9d74db6d0c506cd7b5171129f6cb702277aaa191e7bafd242c551e26b7e582a2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.1 MB (34071646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caf1d9ee7c1f4c75ff401acd07ac5e28aa61e674424f1bf57ac75673845d420e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2020 01:22:34 GMT
ADD file:796aad1a35ba276b8cccc19987c152a713db101b2b65e30923db753f5b7f4b0f in / 
# Tue, 09 Jun 2020 01:22:38 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 04:23:19 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 09 Jun 2020 04:23:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 04:23:43 GMT
ENV MEMCACHED_VERSION=1.6.6
# Tue, 09 Jun 2020 04:23:47 GMT
ENV MEMCACHED_SHA1=d8895b12dc9fc82b389f1713e2c09cc6ca3d03e4
# Tue, 09 Jun 2020 04:35:57 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 09 Jun 2020 04:36:01 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 09 Jun 2020 04:36:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 09 Jun 2020 04:36:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2020 04:36:21 GMT
USER memcache
# Tue, 09 Jun 2020 04:36:26 GMT
EXPOSE 11211
# Tue, 09 Jun 2020 04:36:32 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:63dbb66c5119bb5086d9e6fb6b154211afc20b44ed136ab7df808f6044cfc6f1`  
		Last Modified: Tue, 09 Jun 2020 01:31:04 GMT  
		Size: 30.5 MB (30524405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:326347d3599c113aed8b360975de1e1295d880747ab63b945e59748ff4e00e7f`  
		Last Modified: Tue, 09 Jun 2020 04:37:10 GMT  
		Size: 5.0 KB (4980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b3c6b0b46229c12b05433642c55de042b24a1364fd631996450f9a4bb136143`  
		Last Modified: Tue, 09 Jun 2020 04:37:10 GMT  
		Size: 2.3 MB (2322714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:716f59d7781a40e402cd8add331e26fc33fbaab6a82614c43746b1afdf315747`  
		Last Modified: Tue, 09 Jun 2020 04:37:10 GMT  
		Size: 1.2 MB (1219139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b63b4e5e82673252ff53e7021ac30af1147b4a81f99a82aa1a3c58085688666`  
		Last Modified: Tue, 09 Jun 2020 04:37:10 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abf841a99428dea3a743f5fde752d2ba68f050307880829b6c354c5e5bcdf04e`  
		Last Modified: Tue, 09 Jun 2020 04:37:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.6` - linux; s390x

```console
$ docker pull memcached@sha256:e481d6155413e4b844009223fa04cca68b15e430b4e5476a0e9967f49af57a50
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.8 MB (28789009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd9a8cff3ec775f7b2c039af1fb74ca8706705a6715c681797cd43f02f82090a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2020 01:42:37 GMT
ADD file:b21d426de40a194c6c76ed27593f33fb1ea470e15d4d43b00d7601472110de1a in / 
# Tue, 09 Jun 2020 01:42:38 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 03:40:46 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 09 Jun 2020 03:40:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 03:40:50 GMT
ENV MEMCACHED_VERSION=1.6.6
# Tue, 09 Jun 2020 03:40:50 GMT
ENV MEMCACHED_SHA1=d8895b12dc9fc82b389f1713e2c09cc6ca3d03e4
# Tue, 09 Jun 2020 03:49:43 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 09 Jun 2020 03:49:43 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 09 Jun 2020 03:49:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 09 Jun 2020 03:49:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2020 03:49:44 GMT
USER memcache
# Tue, 09 Jun 2020 03:49:44 GMT
EXPOSE 11211
# Tue, 09 Jun 2020 03:49:44 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:405e75bf6bb0104d67fcebf58e07cd21bf344589df9c1a41c00354a60ea3a604`  
		Last Modified: Tue, 09 Jun 2020 01:46:30 GMT  
		Size: 25.7 MB (25712668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2c03af295f2075ceec6e6cc9874e8666d63a3b26614e659f1396a367f9e2ebc`  
		Last Modified: Tue, 09 Jun 2020 03:50:08 GMT  
		Size: 5.0 KB (5023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989e958beedef1b77252896a7ad5fba801dcef12cde52098e6a9d46a57ec6d9b`  
		Last Modified: Tue, 09 Jun 2020 03:50:08 GMT  
		Size: 1.9 MB (1886033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a68df8456455057906a59f6ff163a22e695cf310443f17f2af2a3742d1e1eaaf`  
		Last Modified: Tue, 09 Jun 2020 03:50:13 GMT  
		Size: 1.2 MB (1184878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7cd9a3bb1b818c1b06baad270500facbfcbaab3102aa9fb203b7aa09fbf8be3`  
		Last Modified: Tue, 09 Jun 2020 03:50:23 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab09b03baf0f78a40dff16e0620f3af6bd5e050654d20b3a1c073fd88d1dff42`  
		Last Modified: Tue, 09 Jun 2020 03:50:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:1.6.6-alpine`

```console
$ docker pull memcached@sha256:21941b2b8ad0c35c302cbb99b53daad0e4117eb1a28e1173823fbfa119b99245
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

### `memcached:1.6.6-alpine` - linux; amd64

```console
$ docker pull memcached@sha256:7aff4ef05d45a680295a97643acd5c8fd1b306697df52b9b99d3c5665cc91520
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35acd9837d07e6369afd8683ae08f7da10de93ea5d50e74050abbdeece1e6754`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 17:02:57 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Fri, 24 Apr 2020 17:02:58 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Wed, 13 May 2020 21:06:46 GMT
ENV MEMCACHED_VERSION=1.6.6
# Wed, 13 May 2020 21:06:46 GMT
ENV MEMCACHED_SHA1=d8895b12dc9fc82b389f1713e2c09cc6ca3d03e4
# Wed, 13 May 2020 21:16:24 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Wed, 13 May 2020 21:16:24 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 13 May 2020 21:16:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 13 May 2020 21:16:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2020 21:16:25 GMT
USER memcache
# Wed, 13 May 2020 21:16:25 GMT
EXPOSE 11211
# Wed, 13 May 2020 21:16:25 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b534c8dcbed02f81e7238c6977e5e3c22aa347c9d8967b7c12c392ee7a9f548b`  
		Last Modified: Fri, 24 Apr 2020 17:11:25 GMT  
		Size: 1.2 KB (1229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f82e93b65d94a9b03ff2f6758b7ad7c93eceeecf3e1310ba5c7160af4fd59962`  
		Last Modified: Fri, 24 Apr 2020 17:11:25 GMT  
		Size: 15.1 KB (15096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea07733e4053c9b83448decf54f501b7f1fc49e3dcd8d3765c66f476df674fab`  
		Last Modified: Wed, 13 May 2020 21:16:49 GMT  
		Size: 1.6 MB (1553777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa95676f933fd0bbc2cc1615e9449e9122b4a5129fbdaff414a28df5cad88222`  
		Last Modified: Wed, 13 May 2020 21:16:49 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2198a28066da8054936ad286e306fb5694ee81c36f612760266d1ca33e9563b`  
		Last Modified: Wed, 13 May 2020 21:16:49 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.6-alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:cdedb0318507c578a21a481fbac96717787aaea12acc53f151332ad36dc72a3e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4153141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84637e955a61c7f56159f60a65b17b892fe5ac952e43227f0d2725ae342bbd90`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 18:17:02 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Thu, 23 Apr 2020 18:17:05 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Wed, 13 May 2020 20:48:09 GMT
ENV MEMCACHED_VERSION=1.6.6
# Wed, 13 May 2020 20:48:09 GMT
ENV MEMCACHED_SHA1=d8895b12dc9fc82b389f1713e2c09cc6ca3d03e4
# Wed, 13 May 2020 20:58:49 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Wed, 13 May 2020 20:58:50 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 13 May 2020 20:58:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 13 May 2020 20:58:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2020 20:58:53 GMT
USER memcache
# Wed, 13 May 2020 20:58:53 GMT
EXPOSE 11211
# Wed, 13 May 2020 20:58:54 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93317744ae21705795946b5f7ccb9e69cd54b0d5b2bdbf48e38bc24ab2037dd4`  
		Last Modified: Thu, 23 Apr 2020 18:26:46 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22d5a6e65917b2d4ecdcd28e7178c79f43bd5cceabca1d40ef2708e66642b656`  
		Last Modified: Thu, 23 Apr 2020 18:26:47 GMT  
		Size: 14.7 KB (14705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55286676201b8c21a4a24628ece19d15221ee259c5df155ebcd0793841211612`  
		Last Modified: Wed, 13 May 2020 20:59:13 GMT  
		Size: 1.5 MB (1516837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c924249be839e9ffa60f403cf731eca93b38caa4e09dc57769e4cc25bcb5ca1`  
		Last Modified: Wed, 13 May 2020 20:59:13 GMT  
		Size: 284.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ded1f200c6c3b6d497cbb1a7fc81bd1ee1dd0cf53a43a8b068ce134ec3c7ab1`  
		Last Modified: Wed, 13 May 2020 20:59:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.6-alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:b8d5715c8f0905fd1d24efc8254baa1ccf6933d9942b0b84c66750a5662bb811
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3841215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:331fbc8dc15f015e7fdd524a348b69696983085d2badb3a9a53cb7424a30567d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 23 Apr 2020 22:04:19 GMT
ADD file:33578d3cacfab86c195d99396dd012ec511796a1d2d8d6f0a02b8a055673c294 in / 
# Thu, 23 Apr 2020 22:04:22 GMT
CMD ["/bin/sh"]
# Mon, 27 Apr 2020 20:41:10 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Mon, 27 Apr 2020 20:41:12 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Wed, 13 May 2020 21:00:46 GMT
ENV MEMCACHED_VERSION=1.6.6
# Wed, 13 May 2020 21:00:47 GMT
ENV MEMCACHED_SHA1=d8895b12dc9fc82b389f1713e2c09cc6ca3d03e4
# Wed, 13 May 2020 21:11:09 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Wed, 13 May 2020 21:11:10 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 13 May 2020 21:11:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 13 May 2020 21:11:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2020 21:11:13 GMT
USER memcache
# Wed, 13 May 2020 21:11:13 GMT
EXPOSE 11211
# Wed, 13 May 2020 21:11:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3cfb62949d9d8613854db4d5fe502a9219c2b55a153043500078a64e880ae234`  
		Last Modified: Thu, 23 Apr 2020 22:05:12 GMT  
		Size: 2.4 MB (2422063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea5eed70290b5b33d1d0a27554b33b5998613f63667c5797fee672c96ea93df4`  
		Last Modified: Mon, 27 Apr 2020 20:50:54 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea75d9462432267b72327c7684218d1e4d40ec6d9b6578b0e8b79fdc50e2f99b`  
		Last Modified: Mon, 27 Apr 2020 20:50:54 GMT  
		Size: 13.6 KB (13633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e2c49241690acb15f16b690b318be68612c6665317e6f7f8b4cc57b57df0d59`  
		Last Modified: Wed, 13 May 2020 21:11:45 GMT  
		Size: 1.4 MB (1403856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b9dc2878fb274ac6ea5501d45e6a552af904357136bc2c90cfdd5c0a18e445e`  
		Last Modified: Wed, 13 May 2020 21:11:45 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:684fd6b097cf009d3e00a45e92d47256b86881e70726707607ba29c24ec95f3f`  
		Last Modified: Wed, 13 May 2020 21:11:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.6-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:84ab0fed3c7720f4b9d131bcbdc1df458b99a5e9950ea32ae9c139e5e874c877
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4298272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f21d64f8b964ecd80325828de3f81900ab258b90d021c999c8db169e9dc75790`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 11:04:28 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Fri, 24 Apr 2020 11:04:30 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Wed, 13 May 2020 21:06:36 GMT
ENV MEMCACHED_VERSION=1.6.6
# Wed, 13 May 2020 21:06:36 GMT
ENV MEMCACHED_SHA1=d8895b12dc9fc82b389f1713e2c09cc6ca3d03e4
# Wed, 13 May 2020 21:17:01 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Wed, 13 May 2020 21:17:02 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 13 May 2020 21:17:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 13 May 2020 21:17:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2020 21:17:07 GMT
USER memcache
# Wed, 13 May 2020 21:17:08 GMT
EXPOSE 11211
# Wed, 13 May 2020 21:17:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:29e5d40040c18c692ed73df24511071725b74956ca1a61fe6056a651d86a13bd`  
		Last Modified: Fri, 24 Apr 2020 00:15:41 GMT  
		Size: 2.7 MB (2724424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe5c53c35221a3533be681a0b6993aafc24fb08c1669f6e2cc3a14ae53ec625`  
		Last Modified: Fri, 24 Apr 2020 11:14:02 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8563552dafaf43a304948c84a7acc248f525f7112d769119ce9c6a68a5e3691`  
		Last Modified: Fri, 24 Apr 2020 11:14:02 GMT  
		Size: 15.5 KB (15487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e025d7a35db9442b2a837e76a39855504aabc39e7e3f988809d349af719667a`  
		Last Modified: Wed, 13 May 2020 21:17:37 GMT  
		Size: 1.6 MB (1556696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcaab3e6609fb2db6c7f55beb904fead407e5d2b97b6acafb93c96c03e56799e`  
		Last Modified: Wed, 13 May 2020 21:17:36 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6109ee9cf8d24da13ee3db362111fdb6fad712167f7a2df5c40282502c86c9c`  
		Last Modified: Wed, 13 May 2020 21:17:36 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.6-alpine` - linux; 386

```console
$ docker pull memcached@sha256:ee779870e380dd4c052f241c53fd38a6ad50cb63aff72e7c5ed1332fb66bea79
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4476231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0e2dba14886b5570a636ee035029db5c230a4c7a1c2a27ee44c0751a70a2e25`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 23 Apr 2020 21:16:04 GMT
ADD file:63bd8a316cba8c404cc2e32a5120406c24aee8db3224c469a6077b941d900863 in / 
# Thu, 23 Apr 2020 21:16:04 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 05:40:17 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Fri, 24 Apr 2020 05:40:18 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Wed, 13 May 2020 20:50:05 GMT
ENV MEMCACHED_VERSION=1.6.6
# Wed, 13 May 2020 20:50:05 GMT
ENV MEMCACHED_SHA1=d8895b12dc9fc82b389f1713e2c09cc6ca3d03e4
# Wed, 13 May 2020 21:00:15 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Wed, 13 May 2020 21:00:15 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 13 May 2020 21:00:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 13 May 2020 21:00:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2020 21:00:16 GMT
USER memcache
# Wed, 13 May 2020 21:00:16 GMT
EXPOSE 11211
# Wed, 13 May 2020 21:00:16 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2826c1e79865da7e0da0a993a2a38db61c3911e05b5df617439a86d4deac90fb`  
		Last Modified: Thu, 23 Apr 2020 21:16:32 GMT  
		Size: 2.8 MB (2808418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99c8f50e3ca0c1433cc286bd4e0a3745ecca7885db26d6589ed10f87bbaab945`  
		Last Modified: Fri, 24 Apr 2020 05:49:15 GMT  
		Size: 1.2 KB (1230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc013a10731c30303c911d27a87fd13538c35f156dd04c77830fd6aae807373`  
		Last Modified: Fri, 24 Apr 2020 05:49:16 GMT  
		Size: 16.2 KB (16152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:581eaa4a0c769e8f41ab1ac20af4e05814cb531a224ef2dbe1b497701b6e4ce9`  
		Last Modified: Wed, 13 May 2020 22:02:28 GMT  
		Size: 1.7 MB (1650028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7b876f113a5523b610398aae49ba66c705dc74ebe9d9bbb14421a29b37b9d0c`  
		Last Modified: Wed, 13 May 2020 22:02:28 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:063c1cbfa63f41d8c35db6ebbcd6c703677a29ee15140de1e193b1b20a14cad5`  
		Last Modified: Wed, 13 May 2020 22:02:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.6-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:65641c9d665bdf546da4a3425c6fa8950dfea3da135fece34ec9cd02e1e9f7ad
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4451916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8fa56a4612543254641d8bef3f069be35b451b380575990325f02932c1d31d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 23 Apr 2020 20:39:04 GMT
ADD file:1aaebe252dfb1885e066fcbc84aaa915bae149c3608f19600855ad1d4f7450c1 in / 
# Thu, 23 Apr 2020 20:39:06 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 06:58:53 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Fri, 24 Apr 2020 06:59:15 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Wed, 13 May 2020 21:52:24 GMT
ENV MEMCACHED_VERSION=1.6.6
# Wed, 13 May 2020 21:52:26 GMT
ENV MEMCACHED_SHA1=d8895b12dc9fc82b389f1713e2c09cc6ca3d03e4
# Wed, 13 May 2020 22:02:40 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Wed, 13 May 2020 22:02:41 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 13 May 2020 22:02:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 13 May 2020 22:02:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2020 22:02:48 GMT
USER memcache
# Wed, 13 May 2020 22:02:51 GMT
EXPOSE 11211
# Wed, 13 May 2020 22:02:52 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9a8fdc5b698322331ee7eba7dd6f66f3a4e956554db22dd1e834d519415b4f8e`  
		Last Modified: Thu, 23 Apr 2020 20:41:33 GMT  
		Size: 2.8 MB (2821843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8003ab8fdd2231d50550cbe8a4e5715a79d4707174e50e5208a3525a93b88d58`  
		Last Modified: Fri, 24 Apr 2020 07:09:36 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cf79da4de605128ba727e77467d72e9e1045bdd33fef6b7e4be6beb023816b1`  
		Last Modified: Fri, 24 Apr 2020 07:09:36 GMT  
		Size: 16.1 KB (16137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6db567fc6e2d79ea6f1c03ddc425dbdc0f8b451588832f6e7baf60ba1074942`  
		Last Modified: Wed, 13 May 2020 22:03:33 GMT  
		Size: 1.6 MB (1612264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91270a821a4eef3c8257ffc9a240571b34b80e984b5e9bee826fadf09df8c9d3`  
		Last Modified: Wed, 13 May 2020 22:03:32 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5cd487ad1a45f4788b910ad95b419e4c85c1744025f4047847d4da12cc293fc`  
		Last Modified: Wed, 13 May 2020 22:03:32 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.6-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:e67fbfdb16b98451a2479f1b8ac1253153c1a0207446cd0b96ac3acbc8388374
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4167257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:172a7a8f96030a5bb34744dedb5dc60f06194a5967f790a4507f2f6a123a1e52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 23 Apr 2020 17:50:57 GMT
ADD file:a59a30c2fd43c9f3b820751a6f5a54688c14440a1ddace1ab255475f46e6ba2d in / 
# Thu, 23 Apr 2020 17:50:58 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 19:00:40 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Thu, 23 Apr 2020 19:00:41 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Wed, 13 May 2020 20:44:10 GMT
ENV MEMCACHED_VERSION=1.6.6
# Wed, 13 May 2020 20:44:10 GMT
ENV MEMCACHED_SHA1=d8895b12dc9fc82b389f1713e2c09cc6ca3d03e4
# Wed, 13 May 2020 20:53:11 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Wed, 13 May 2020 20:53:11 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 13 May 2020 20:53:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 13 May 2020 20:53:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2020 20:53:12 GMT
USER memcache
# Wed, 13 May 2020 20:53:13 GMT
EXPOSE 11211
# Wed, 13 May 2020 20:53:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7184c046fdf17da4c16ca482e5ede36e1f2d41ac8cea9c036e488fd149d6e8e7`  
		Last Modified: Thu, 23 Apr 2020 17:51:38 GMT  
		Size: 2.6 MB (2582859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca2971d466d139c0291506e9e9a74874f9720887c9d7589ac53625b827b4ddcb`  
		Last Modified: Wed, 13 May 2020 20:53:44 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dba5e1242654650bd369b46ebc84b7619dad9b2965728812cd6c53fbe412447`  
		Last Modified: Wed, 13 May 2020 20:53:50 GMT  
		Size: 15.4 KB (15364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c7a93509f92f968102940c5f29e41a5246d13ff2ca46d1b943913e1bdb0156`  
		Last Modified: Wed, 13 May 2020 20:53:45 GMT  
		Size: 1.6 MB (1567372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f782215b5f873e287c10ac50cd1ffafe9a48a11bce170ccb5ff224692251297a`  
		Last Modified: Wed, 13 May 2020 20:53:44 GMT  
		Size: 284.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c50080fccd2633d9e531227847ff62435c70da07804426afede4469d4c11a2`  
		Last Modified: Wed, 13 May 2020 20:53:44 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:1.6-alpine`

```console
$ docker pull memcached@sha256:21941b2b8ad0c35c302cbb99b53daad0e4117eb1a28e1173823fbfa119b99245
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
$ docker pull memcached@sha256:7aff4ef05d45a680295a97643acd5c8fd1b306697df52b9b99d3c5665cc91520
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35acd9837d07e6369afd8683ae08f7da10de93ea5d50e74050abbdeece1e6754`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 17:02:57 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Fri, 24 Apr 2020 17:02:58 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Wed, 13 May 2020 21:06:46 GMT
ENV MEMCACHED_VERSION=1.6.6
# Wed, 13 May 2020 21:06:46 GMT
ENV MEMCACHED_SHA1=d8895b12dc9fc82b389f1713e2c09cc6ca3d03e4
# Wed, 13 May 2020 21:16:24 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Wed, 13 May 2020 21:16:24 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 13 May 2020 21:16:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 13 May 2020 21:16:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2020 21:16:25 GMT
USER memcache
# Wed, 13 May 2020 21:16:25 GMT
EXPOSE 11211
# Wed, 13 May 2020 21:16:25 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b534c8dcbed02f81e7238c6977e5e3c22aa347c9d8967b7c12c392ee7a9f548b`  
		Last Modified: Fri, 24 Apr 2020 17:11:25 GMT  
		Size: 1.2 KB (1229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f82e93b65d94a9b03ff2f6758b7ad7c93eceeecf3e1310ba5c7160af4fd59962`  
		Last Modified: Fri, 24 Apr 2020 17:11:25 GMT  
		Size: 15.1 KB (15096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea07733e4053c9b83448decf54f501b7f1fc49e3dcd8d3765c66f476df674fab`  
		Last Modified: Wed, 13 May 2020 21:16:49 GMT  
		Size: 1.6 MB (1553777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa95676f933fd0bbc2cc1615e9449e9122b4a5129fbdaff414a28df5cad88222`  
		Last Modified: Wed, 13 May 2020 21:16:49 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2198a28066da8054936ad286e306fb5694ee81c36f612760266d1ca33e9563b`  
		Last Modified: Wed, 13 May 2020 21:16:49 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6-alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:cdedb0318507c578a21a481fbac96717787aaea12acc53f151332ad36dc72a3e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4153141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84637e955a61c7f56159f60a65b17b892fe5ac952e43227f0d2725ae342bbd90`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 18:17:02 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Thu, 23 Apr 2020 18:17:05 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Wed, 13 May 2020 20:48:09 GMT
ENV MEMCACHED_VERSION=1.6.6
# Wed, 13 May 2020 20:48:09 GMT
ENV MEMCACHED_SHA1=d8895b12dc9fc82b389f1713e2c09cc6ca3d03e4
# Wed, 13 May 2020 20:58:49 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Wed, 13 May 2020 20:58:50 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 13 May 2020 20:58:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 13 May 2020 20:58:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2020 20:58:53 GMT
USER memcache
# Wed, 13 May 2020 20:58:53 GMT
EXPOSE 11211
# Wed, 13 May 2020 20:58:54 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93317744ae21705795946b5f7ccb9e69cd54b0d5b2bdbf48e38bc24ab2037dd4`  
		Last Modified: Thu, 23 Apr 2020 18:26:46 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22d5a6e65917b2d4ecdcd28e7178c79f43bd5cceabca1d40ef2708e66642b656`  
		Last Modified: Thu, 23 Apr 2020 18:26:47 GMT  
		Size: 14.7 KB (14705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55286676201b8c21a4a24628ece19d15221ee259c5df155ebcd0793841211612`  
		Last Modified: Wed, 13 May 2020 20:59:13 GMT  
		Size: 1.5 MB (1516837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c924249be839e9ffa60f403cf731eca93b38caa4e09dc57769e4cc25bcb5ca1`  
		Last Modified: Wed, 13 May 2020 20:59:13 GMT  
		Size: 284.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ded1f200c6c3b6d497cbb1a7fc81bd1ee1dd0cf53a43a8b068ce134ec3c7ab1`  
		Last Modified: Wed, 13 May 2020 20:59:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6-alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:b8d5715c8f0905fd1d24efc8254baa1ccf6933d9942b0b84c66750a5662bb811
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3841215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:331fbc8dc15f015e7fdd524a348b69696983085d2badb3a9a53cb7424a30567d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 23 Apr 2020 22:04:19 GMT
ADD file:33578d3cacfab86c195d99396dd012ec511796a1d2d8d6f0a02b8a055673c294 in / 
# Thu, 23 Apr 2020 22:04:22 GMT
CMD ["/bin/sh"]
# Mon, 27 Apr 2020 20:41:10 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Mon, 27 Apr 2020 20:41:12 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Wed, 13 May 2020 21:00:46 GMT
ENV MEMCACHED_VERSION=1.6.6
# Wed, 13 May 2020 21:00:47 GMT
ENV MEMCACHED_SHA1=d8895b12dc9fc82b389f1713e2c09cc6ca3d03e4
# Wed, 13 May 2020 21:11:09 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Wed, 13 May 2020 21:11:10 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 13 May 2020 21:11:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 13 May 2020 21:11:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2020 21:11:13 GMT
USER memcache
# Wed, 13 May 2020 21:11:13 GMT
EXPOSE 11211
# Wed, 13 May 2020 21:11:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3cfb62949d9d8613854db4d5fe502a9219c2b55a153043500078a64e880ae234`  
		Last Modified: Thu, 23 Apr 2020 22:05:12 GMT  
		Size: 2.4 MB (2422063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea5eed70290b5b33d1d0a27554b33b5998613f63667c5797fee672c96ea93df4`  
		Last Modified: Mon, 27 Apr 2020 20:50:54 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea75d9462432267b72327c7684218d1e4d40ec6d9b6578b0e8b79fdc50e2f99b`  
		Last Modified: Mon, 27 Apr 2020 20:50:54 GMT  
		Size: 13.6 KB (13633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e2c49241690acb15f16b690b318be68612c6665317e6f7f8b4cc57b57df0d59`  
		Last Modified: Wed, 13 May 2020 21:11:45 GMT  
		Size: 1.4 MB (1403856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b9dc2878fb274ac6ea5501d45e6a552af904357136bc2c90cfdd5c0a18e445e`  
		Last Modified: Wed, 13 May 2020 21:11:45 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:684fd6b097cf009d3e00a45e92d47256b86881e70726707607ba29c24ec95f3f`  
		Last Modified: Wed, 13 May 2020 21:11:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:84ab0fed3c7720f4b9d131bcbdc1df458b99a5e9950ea32ae9c139e5e874c877
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4298272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f21d64f8b964ecd80325828de3f81900ab258b90d021c999c8db169e9dc75790`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 11:04:28 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Fri, 24 Apr 2020 11:04:30 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Wed, 13 May 2020 21:06:36 GMT
ENV MEMCACHED_VERSION=1.6.6
# Wed, 13 May 2020 21:06:36 GMT
ENV MEMCACHED_SHA1=d8895b12dc9fc82b389f1713e2c09cc6ca3d03e4
# Wed, 13 May 2020 21:17:01 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Wed, 13 May 2020 21:17:02 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 13 May 2020 21:17:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 13 May 2020 21:17:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2020 21:17:07 GMT
USER memcache
# Wed, 13 May 2020 21:17:08 GMT
EXPOSE 11211
# Wed, 13 May 2020 21:17:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:29e5d40040c18c692ed73df24511071725b74956ca1a61fe6056a651d86a13bd`  
		Last Modified: Fri, 24 Apr 2020 00:15:41 GMT  
		Size: 2.7 MB (2724424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe5c53c35221a3533be681a0b6993aafc24fb08c1669f6e2cc3a14ae53ec625`  
		Last Modified: Fri, 24 Apr 2020 11:14:02 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8563552dafaf43a304948c84a7acc248f525f7112d769119ce9c6a68a5e3691`  
		Last Modified: Fri, 24 Apr 2020 11:14:02 GMT  
		Size: 15.5 KB (15487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e025d7a35db9442b2a837e76a39855504aabc39e7e3f988809d349af719667a`  
		Last Modified: Wed, 13 May 2020 21:17:37 GMT  
		Size: 1.6 MB (1556696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcaab3e6609fb2db6c7f55beb904fead407e5d2b97b6acafb93c96c03e56799e`  
		Last Modified: Wed, 13 May 2020 21:17:36 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6109ee9cf8d24da13ee3db362111fdb6fad712167f7a2df5c40282502c86c9c`  
		Last Modified: Wed, 13 May 2020 21:17:36 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6-alpine` - linux; 386

```console
$ docker pull memcached@sha256:ee779870e380dd4c052f241c53fd38a6ad50cb63aff72e7c5ed1332fb66bea79
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4476231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0e2dba14886b5570a636ee035029db5c230a4c7a1c2a27ee44c0751a70a2e25`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 23 Apr 2020 21:16:04 GMT
ADD file:63bd8a316cba8c404cc2e32a5120406c24aee8db3224c469a6077b941d900863 in / 
# Thu, 23 Apr 2020 21:16:04 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 05:40:17 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Fri, 24 Apr 2020 05:40:18 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Wed, 13 May 2020 20:50:05 GMT
ENV MEMCACHED_VERSION=1.6.6
# Wed, 13 May 2020 20:50:05 GMT
ENV MEMCACHED_SHA1=d8895b12dc9fc82b389f1713e2c09cc6ca3d03e4
# Wed, 13 May 2020 21:00:15 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Wed, 13 May 2020 21:00:15 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 13 May 2020 21:00:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 13 May 2020 21:00:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2020 21:00:16 GMT
USER memcache
# Wed, 13 May 2020 21:00:16 GMT
EXPOSE 11211
# Wed, 13 May 2020 21:00:16 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2826c1e79865da7e0da0a993a2a38db61c3911e05b5df617439a86d4deac90fb`  
		Last Modified: Thu, 23 Apr 2020 21:16:32 GMT  
		Size: 2.8 MB (2808418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99c8f50e3ca0c1433cc286bd4e0a3745ecca7885db26d6589ed10f87bbaab945`  
		Last Modified: Fri, 24 Apr 2020 05:49:15 GMT  
		Size: 1.2 KB (1230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc013a10731c30303c911d27a87fd13538c35f156dd04c77830fd6aae807373`  
		Last Modified: Fri, 24 Apr 2020 05:49:16 GMT  
		Size: 16.2 KB (16152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:581eaa4a0c769e8f41ab1ac20af4e05814cb531a224ef2dbe1b497701b6e4ce9`  
		Last Modified: Wed, 13 May 2020 22:02:28 GMT  
		Size: 1.7 MB (1650028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7b876f113a5523b610398aae49ba66c705dc74ebe9d9bbb14421a29b37b9d0c`  
		Last Modified: Wed, 13 May 2020 22:02:28 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:063c1cbfa63f41d8c35db6ebbcd6c703677a29ee15140de1e193b1b20a14cad5`  
		Last Modified: Wed, 13 May 2020 22:02:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:65641c9d665bdf546da4a3425c6fa8950dfea3da135fece34ec9cd02e1e9f7ad
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4451916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8fa56a4612543254641d8bef3f069be35b451b380575990325f02932c1d31d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 23 Apr 2020 20:39:04 GMT
ADD file:1aaebe252dfb1885e066fcbc84aaa915bae149c3608f19600855ad1d4f7450c1 in / 
# Thu, 23 Apr 2020 20:39:06 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 06:58:53 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Fri, 24 Apr 2020 06:59:15 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Wed, 13 May 2020 21:52:24 GMT
ENV MEMCACHED_VERSION=1.6.6
# Wed, 13 May 2020 21:52:26 GMT
ENV MEMCACHED_SHA1=d8895b12dc9fc82b389f1713e2c09cc6ca3d03e4
# Wed, 13 May 2020 22:02:40 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Wed, 13 May 2020 22:02:41 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 13 May 2020 22:02:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 13 May 2020 22:02:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2020 22:02:48 GMT
USER memcache
# Wed, 13 May 2020 22:02:51 GMT
EXPOSE 11211
# Wed, 13 May 2020 22:02:52 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9a8fdc5b698322331ee7eba7dd6f66f3a4e956554db22dd1e834d519415b4f8e`  
		Last Modified: Thu, 23 Apr 2020 20:41:33 GMT  
		Size: 2.8 MB (2821843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8003ab8fdd2231d50550cbe8a4e5715a79d4707174e50e5208a3525a93b88d58`  
		Last Modified: Fri, 24 Apr 2020 07:09:36 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cf79da4de605128ba727e77467d72e9e1045bdd33fef6b7e4be6beb023816b1`  
		Last Modified: Fri, 24 Apr 2020 07:09:36 GMT  
		Size: 16.1 KB (16137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6db567fc6e2d79ea6f1c03ddc425dbdc0f8b451588832f6e7baf60ba1074942`  
		Last Modified: Wed, 13 May 2020 22:03:33 GMT  
		Size: 1.6 MB (1612264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91270a821a4eef3c8257ffc9a240571b34b80e984b5e9bee826fadf09df8c9d3`  
		Last Modified: Wed, 13 May 2020 22:03:32 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5cd487ad1a45f4788b910ad95b419e4c85c1744025f4047847d4da12cc293fc`  
		Last Modified: Wed, 13 May 2020 22:03:32 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:e67fbfdb16b98451a2479f1b8ac1253153c1a0207446cd0b96ac3acbc8388374
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4167257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:172a7a8f96030a5bb34744dedb5dc60f06194a5967f790a4507f2f6a123a1e52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 23 Apr 2020 17:50:57 GMT
ADD file:a59a30c2fd43c9f3b820751a6f5a54688c14440a1ddace1ab255475f46e6ba2d in / 
# Thu, 23 Apr 2020 17:50:58 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 19:00:40 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Thu, 23 Apr 2020 19:00:41 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Wed, 13 May 2020 20:44:10 GMT
ENV MEMCACHED_VERSION=1.6.6
# Wed, 13 May 2020 20:44:10 GMT
ENV MEMCACHED_SHA1=d8895b12dc9fc82b389f1713e2c09cc6ca3d03e4
# Wed, 13 May 2020 20:53:11 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Wed, 13 May 2020 20:53:11 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 13 May 2020 20:53:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 13 May 2020 20:53:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2020 20:53:12 GMT
USER memcache
# Wed, 13 May 2020 20:53:13 GMT
EXPOSE 11211
# Wed, 13 May 2020 20:53:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7184c046fdf17da4c16ca482e5ede36e1f2d41ac8cea9c036e488fd149d6e8e7`  
		Last Modified: Thu, 23 Apr 2020 17:51:38 GMT  
		Size: 2.6 MB (2582859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca2971d466d139c0291506e9e9a74874f9720887c9d7589ac53625b827b4ddcb`  
		Last Modified: Wed, 13 May 2020 20:53:44 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dba5e1242654650bd369b46ebc84b7619dad9b2965728812cd6c53fbe412447`  
		Last Modified: Wed, 13 May 2020 20:53:50 GMT  
		Size: 15.4 KB (15364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c7a93509f92f968102940c5f29e41a5246d13ff2ca46d1b943913e1bdb0156`  
		Last Modified: Wed, 13 May 2020 20:53:45 GMT  
		Size: 1.6 MB (1567372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f782215b5f873e287c10ac50cd1ffafe9a48a11bce170ccb5ff224692251297a`  
		Last Modified: Wed, 13 May 2020 20:53:44 GMT  
		Size: 284.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c50080fccd2633d9e531227847ff62435c70da07804426afede4469d4c11a2`  
		Last Modified: Wed, 13 May 2020 20:53:44 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:1-alpine`

```console
$ docker pull memcached@sha256:21941b2b8ad0c35c302cbb99b53daad0e4117eb1a28e1173823fbfa119b99245
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
$ docker pull memcached@sha256:7aff4ef05d45a680295a97643acd5c8fd1b306697df52b9b99d3c5665cc91520
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35acd9837d07e6369afd8683ae08f7da10de93ea5d50e74050abbdeece1e6754`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 17:02:57 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Fri, 24 Apr 2020 17:02:58 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Wed, 13 May 2020 21:06:46 GMT
ENV MEMCACHED_VERSION=1.6.6
# Wed, 13 May 2020 21:06:46 GMT
ENV MEMCACHED_SHA1=d8895b12dc9fc82b389f1713e2c09cc6ca3d03e4
# Wed, 13 May 2020 21:16:24 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Wed, 13 May 2020 21:16:24 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 13 May 2020 21:16:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 13 May 2020 21:16:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2020 21:16:25 GMT
USER memcache
# Wed, 13 May 2020 21:16:25 GMT
EXPOSE 11211
# Wed, 13 May 2020 21:16:25 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b534c8dcbed02f81e7238c6977e5e3c22aa347c9d8967b7c12c392ee7a9f548b`  
		Last Modified: Fri, 24 Apr 2020 17:11:25 GMT  
		Size: 1.2 KB (1229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f82e93b65d94a9b03ff2f6758b7ad7c93eceeecf3e1310ba5c7160af4fd59962`  
		Last Modified: Fri, 24 Apr 2020 17:11:25 GMT  
		Size: 15.1 KB (15096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea07733e4053c9b83448decf54f501b7f1fc49e3dcd8d3765c66f476df674fab`  
		Last Modified: Wed, 13 May 2020 21:16:49 GMT  
		Size: 1.6 MB (1553777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa95676f933fd0bbc2cc1615e9449e9122b4a5129fbdaff414a28df5cad88222`  
		Last Modified: Wed, 13 May 2020 21:16:49 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2198a28066da8054936ad286e306fb5694ee81c36f612760266d1ca33e9563b`  
		Last Modified: Wed, 13 May 2020 21:16:49 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:cdedb0318507c578a21a481fbac96717787aaea12acc53f151332ad36dc72a3e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4153141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84637e955a61c7f56159f60a65b17b892fe5ac952e43227f0d2725ae342bbd90`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 18:17:02 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Thu, 23 Apr 2020 18:17:05 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Wed, 13 May 2020 20:48:09 GMT
ENV MEMCACHED_VERSION=1.6.6
# Wed, 13 May 2020 20:48:09 GMT
ENV MEMCACHED_SHA1=d8895b12dc9fc82b389f1713e2c09cc6ca3d03e4
# Wed, 13 May 2020 20:58:49 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Wed, 13 May 2020 20:58:50 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 13 May 2020 20:58:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 13 May 2020 20:58:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2020 20:58:53 GMT
USER memcache
# Wed, 13 May 2020 20:58:53 GMT
EXPOSE 11211
# Wed, 13 May 2020 20:58:54 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93317744ae21705795946b5f7ccb9e69cd54b0d5b2bdbf48e38bc24ab2037dd4`  
		Last Modified: Thu, 23 Apr 2020 18:26:46 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22d5a6e65917b2d4ecdcd28e7178c79f43bd5cceabca1d40ef2708e66642b656`  
		Last Modified: Thu, 23 Apr 2020 18:26:47 GMT  
		Size: 14.7 KB (14705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55286676201b8c21a4a24628ece19d15221ee259c5df155ebcd0793841211612`  
		Last Modified: Wed, 13 May 2020 20:59:13 GMT  
		Size: 1.5 MB (1516837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c924249be839e9ffa60f403cf731eca93b38caa4e09dc57769e4cc25bcb5ca1`  
		Last Modified: Wed, 13 May 2020 20:59:13 GMT  
		Size: 284.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ded1f200c6c3b6d497cbb1a7fc81bd1ee1dd0cf53a43a8b068ce134ec3c7ab1`  
		Last Modified: Wed, 13 May 2020 20:59:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:b8d5715c8f0905fd1d24efc8254baa1ccf6933d9942b0b84c66750a5662bb811
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3841215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:331fbc8dc15f015e7fdd524a348b69696983085d2badb3a9a53cb7424a30567d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 23 Apr 2020 22:04:19 GMT
ADD file:33578d3cacfab86c195d99396dd012ec511796a1d2d8d6f0a02b8a055673c294 in / 
# Thu, 23 Apr 2020 22:04:22 GMT
CMD ["/bin/sh"]
# Mon, 27 Apr 2020 20:41:10 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Mon, 27 Apr 2020 20:41:12 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Wed, 13 May 2020 21:00:46 GMT
ENV MEMCACHED_VERSION=1.6.6
# Wed, 13 May 2020 21:00:47 GMT
ENV MEMCACHED_SHA1=d8895b12dc9fc82b389f1713e2c09cc6ca3d03e4
# Wed, 13 May 2020 21:11:09 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Wed, 13 May 2020 21:11:10 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 13 May 2020 21:11:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 13 May 2020 21:11:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2020 21:11:13 GMT
USER memcache
# Wed, 13 May 2020 21:11:13 GMT
EXPOSE 11211
# Wed, 13 May 2020 21:11:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3cfb62949d9d8613854db4d5fe502a9219c2b55a153043500078a64e880ae234`  
		Last Modified: Thu, 23 Apr 2020 22:05:12 GMT  
		Size: 2.4 MB (2422063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea5eed70290b5b33d1d0a27554b33b5998613f63667c5797fee672c96ea93df4`  
		Last Modified: Mon, 27 Apr 2020 20:50:54 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea75d9462432267b72327c7684218d1e4d40ec6d9b6578b0e8b79fdc50e2f99b`  
		Last Modified: Mon, 27 Apr 2020 20:50:54 GMT  
		Size: 13.6 KB (13633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e2c49241690acb15f16b690b318be68612c6665317e6f7f8b4cc57b57df0d59`  
		Last Modified: Wed, 13 May 2020 21:11:45 GMT  
		Size: 1.4 MB (1403856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b9dc2878fb274ac6ea5501d45e6a552af904357136bc2c90cfdd5c0a18e445e`  
		Last Modified: Wed, 13 May 2020 21:11:45 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:684fd6b097cf009d3e00a45e92d47256b86881e70726707607ba29c24ec95f3f`  
		Last Modified: Wed, 13 May 2020 21:11:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:84ab0fed3c7720f4b9d131bcbdc1df458b99a5e9950ea32ae9c139e5e874c877
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4298272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f21d64f8b964ecd80325828de3f81900ab258b90d021c999c8db169e9dc75790`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 11:04:28 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Fri, 24 Apr 2020 11:04:30 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Wed, 13 May 2020 21:06:36 GMT
ENV MEMCACHED_VERSION=1.6.6
# Wed, 13 May 2020 21:06:36 GMT
ENV MEMCACHED_SHA1=d8895b12dc9fc82b389f1713e2c09cc6ca3d03e4
# Wed, 13 May 2020 21:17:01 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Wed, 13 May 2020 21:17:02 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 13 May 2020 21:17:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 13 May 2020 21:17:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2020 21:17:07 GMT
USER memcache
# Wed, 13 May 2020 21:17:08 GMT
EXPOSE 11211
# Wed, 13 May 2020 21:17:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:29e5d40040c18c692ed73df24511071725b74956ca1a61fe6056a651d86a13bd`  
		Last Modified: Fri, 24 Apr 2020 00:15:41 GMT  
		Size: 2.7 MB (2724424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe5c53c35221a3533be681a0b6993aafc24fb08c1669f6e2cc3a14ae53ec625`  
		Last Modified: Fri, 24 Apr 2020 11:14:02 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8563552dafaf43a304948c84a7acc248f525f7112d769119ce9c6a68a5e3691`  
		Last Modified: Fri, 24 Apr 2020 11:14:02 GMT  
		Size: 15.5 KB (15487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e025d7a35db9442b2a837e76a39855504aabc39e7e3f988809d349af719667a`  
		Last Modified: Wed, 13 May 2020 21:17:37 GMT  
		Size: 1.6 MB (1556696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcaab3e6609fb2db6c7f55beb904fead407e5d2b97b6acafb93c96c03e56799e`  
		Last Modified: Wed, 13 May 2020 21:17:36 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6109ee9cf8d24da13ee3db362111fdb6fad712167f7a2df5c40282502c86c9c`  
		Last Modified: Wed, 13 May 2020 21:17:36 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine` - linux; 386

```console
$ docker pull memcached@sha256:ee779870e380dd4c052f241c53fd38a6ad50cb63aff72e7c5ed1332fb66bea79
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4476231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0e2dba14886b5570a636ee035029db5c230a4c7a1c2a27ee44c0751a70a2e25`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 23 Apr 2020 21:16:04 GMT
ADD file:63bd8a316cba8c404cc2e32a5120406c24aee8db3224c469a6077b941d900863 in / 
# Thu, 23 Apr 2020 21:16:04 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 05:40:17 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Fri, 24 Apr 2020 05:40:18 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Wed, 13 May 2020 20:50:05 GMT
ENV MEMCACHED_VERSION=1.6.6
# Wed, 13 May 2020 20:50:05 GMT
ENV MEMCACHED_SHA1=d8895b12dc9fc82b389f1713e2c09cc6ca3d03e4
# Wed, 13 May 2020 21:00:15 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Wed, 13 May 2020 21:00:15 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 13 May 2020 21:00:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 13 May 2020 21:00:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2020 21:00:16 GMT
USER memcache
# Wed, 13 May 2020 21:00:16 GMT
EXPOSE 11211
# Wed, 13 May 2020 21:00:16 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2826c1e79865da7e0da0a993a2a38db61c3911e05b5df617439a86d4deac90fb`  
		Last Modified: Thu, 23 Apr 2020 21:16:32 GMT  
		Size: 2.8 MB (2808418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99c8f50e3ca0c1433cc286bd4e0a3745ecca7885db26d6589ed10f87bbaab945`  
		Last Modified: Fri, 24 Apr 2020 05:49:15 GMT  
		Size: 1.2 KB (1230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc013a10731c30303c911d27a87fd13538c35f156dd04c77830fd6aae807373`  
		Last Modified: Fri, 24 Apr 2020 05:49:16 GMT  
		Size: 16.2 KB (16152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:581eaa4a0c769e8f41ab1ac20af4e05814cb531a224ef2dbe1b497701b6e4ce9`  
		Last Modified: Wed, 13 May 2020 22:02:28 GMT  
		Size: 1.7 MB (1650028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7b876f113a5523b610398aae49ba66c705dc74ebe9d9bbb14421a29b37b9d0c`  
		Last Modified: Wed, 13 May 2020 22:02:28 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:063c1cbfa63f41d8c35db6ebbcd6c703677a29ee15140de1e193b1b20a14cad5`  
		Last Modified: Wed, 13 May 2020 22:02:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:65641c9d665bdf546da4a3425c6fa8950dfea3da135fece34ec9cd02e1e9f7ad
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4451916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8fa56a4612543254641d8bef3f069be35b451b380575990325f02932c1d31d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 23 Apr 2020 20:39:04 GMT
ADD file:1aaebe252dfb1885e066fcbc84aaa915bae149c3608f19600855ad1d4f7450c1 in / 
# Thu, 23 Apr 2020 20:39:06 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 06:58:53 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Fri, 24 Apr 2020 06:59:15 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Wed, 13 May 2020 21:52:24 GMT
ENV MEMCACHED_VERSION=1.6.6
# Wed, 13 May 2020 21:52:26 GMT
ENV MEMCACHED_SHA1=d8895b12dc9fc82b389f1713e2c09cc6ca3d03e4
# Wed, 13 May 2020 22:02:40 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Wed, 13 May 2020 22:02:41 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 13 May 2020 22:02:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 13 May 2020 22:02:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2020 22:02:48 GMT
USER memcache
# Wed, 13 May 2020 22:02:51 GMT
EXPOSE 11211
# Wed, 13 May 2020 22:02:52 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9a8fdc5b698322331ee7eba7dd6f66f3a4e956554db22dd1e834d519415b4f8e`  
		Last Modified: Thu, 23 Apr 2020 20:41:33 GMT  
		Size: 2.8 MB (2821843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8003ab8fdd2231d50550cbe8a4e5715a79d4707174e50e5208a3525a93b88d58`  
		Last Modified: Fri, 24 Apr 2020 07:09:36 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cf79da4de605128ba727e77467d72e9e1045bdd33fef6b7e4be6beb023816b1`  
		Last Modified: Fri, 24 Apr 2020 07:09:36 GMT  
		Size: 16.1 KB (16137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6db567fc6e2d79ea6f1c03ddc425dbdc0f8b451588832f6e7baf60ba1074942`  
		Last Modified: Wed, 13 May 2020 22:03:33 GMT  
		Size: 1.6 MB (1612264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91270a821a4eef3c8257ffc9a240571b34b80e984b5e9bee826fadf09df8c9d3`  
		Last Modified: Wed, 13 May 2020 22:03:32 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5cd487ad1a45f4788b910ad95b419e4c85c1744025f4047847d4da12cc293fc`  
		Last Modified: Wed, 13 May 2020 22:03:32 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:e67fbfdb16b98451a2479f1b8ac1253153c1a0207446cd0b96ac3acbc8388374
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4167257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:172a7a8f96030a5bb34744dedb5dc60f06194a5967f790a4507f2f6a123a1e52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 23 Apr 2020 17:50:57 GMT
ADD file:a59a30c2fd43c9f3b820751a6f5a54688c14440a1ddace1ab255475f46e6ba2d in / 
# Thu, 23 Apr 2020 17:50:58 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 19:00:40 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Thu, 23 Apr 2020 19:00:41 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Wed, 13 May 2020 20:44:10 GMT
ENV MEMCACHED_VERSION=1.6.6
# Wed, 13 May 2020 20:44:10 GMT
ENV MEMCACHED_SHA1=d8895b12dc9fc82b389f1713e2c09cc6ca3d03e4
# Wed, 13 May 2020 20:53:11 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Wed, 13 May 2020 20:53:11 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 13 May 2020 20:53:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 13 May 2020 20:53:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2020 20:53:12 GMT
USER memcache
# Wed, 13 May 2020 20:53:13 GMT
EXPOSE 11211
# Wed, 13 May 2020 20:53:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7184c046fdf17da4c16ca482e5ede36e1f2d41ac8cea9c036e488fd149d6e8e7`  
		Last Modified: Thu, 23 Apr 2020 17:51:38 GMT  
		Size: 2.6 MB (2582859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca2971d466d139c0291506e9e9a74874f9720887c9d7589ac53625b827b4ddcb`  
		Last Modified: Wed, 13 May 2020 20:53:44 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dba5e1242654650bd369b46ebc84b7619dad9b2965728812cd6c53fbe412447`  
		Last Modified: Wed, 13 May 2020 20:53:50 GMT  
		Size: 15.4 KB (15364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c7a93509f92f968102940c5f29e41a5246d13ff2ca46d1b943913e1bdb0156`  
		Last Modified: Wed, 13 May 2020 20:53:45 GMT  
		Size: 1.6 MB (1567372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f782215b5f873e287c10ac50cd1ffafe9a48a11bce170ccb5ff224692251297a`  
		Last Modified: Wed, 13 May 2020 20:53:44 GMT  
		Size: 284.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c50080fccd2633d9e531227847ff62435c70da07804426afede4469d4c11a2`  
		Last Modified: Wed, 13 May 2020 20:53:44 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:alpine`

```console
$ docker pull memcached@sha256:21941b2b8ad0c35c302cbb99b53daad0e4117eb1a28e1173823fbfa119b99245
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
$ docker pull memcached@sha256:7aff4ef05d45a680295a97643acd5c8fd1b306697df52b9b99d3c5665cc91520
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35acd9837d07e6369afd8683ae08f7da10de93ea5d50e74050abbdeece1e6754`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 17:02:57 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Fri, 24 Apr 2020 17:02:58 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Wed, 13 May 2020 21:06:46 GMT
ENV MEMCACHED_VERSION=1.6.6
# Wed, 13 May 2020 21:06:46 GMT
ENV MEMCACHED_SHA1=d8895b12dc9fc82b389f1713e2c09cc6ca3d03e4
# Wed, 13 May 2020 21:16:24 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Wed, 13 May 2020 21:16:24 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 13 May 2020 21:16:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 13 May 2020 21:16:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2020 21:16:25 GMT
USER memcache
# Wed, 13 May 2020 21:16:25 GMT
EXPOSE 11211
# Wed, 13 May 2020 21:16:25 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b534c8dcbed02f81e7238c6977e5e3c22aa347c9d8967b7c12c392ee7a9f548b`  
		Last Modified: Fri, 24 Apr 2020 17:11:25 GMT  
		Size: 1.2 KB (1229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f82e93b65d94a9b03ff2f6758b7ad7c93eceeecf3e1310ba5c7160af4fd59962`  
		Last Modified: Fri, 24 Apr 2020 17:11:25 GMT  
		Size: 15.1 KB (15096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea07733e4053c9b83448decf54f501b7f1fc49e3dcd8d3765c66f476df674fab`  
		Last Modified: Wed, 13 May 2020 21:16:49 GMT  
		Size: 1.6 MB (1553777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa95676f933fd0bbc2cc1615e9449e9122b4a5129fbdaff414a28df5cad88222`  
		Last Modified: Wed, 13 May 2020 21:16:49 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2198a28066da8054936ad286e306fb5694ee81c36f612760266d1ca33e9563b`  
		Last Modified: Wed, 13 May 2020 21:16:49 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:cdedb0318507c578a21a481fbac96717787aaea12acc53f151332ad36dc72a3e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4153141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84637e955a61c7f56159f60a65b17b892fe5ac952e43227f0d2725ae342bbd90`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 18:17:02 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Thu, 23 Apr 2020 18:17:05 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Wed, 13 May 2020 20:48:09 GMT
ENV MEMCACHED_VERSION=1.6.6
# Wed, 13 May 2020 20:48:09 GMT
ENV MEMCACHED_SHA1=d8895b12dc9fc82b389f1713e2c09cc6ca3d03e4
# Wed, 13 May 2020 20:58:49 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Wed, 13 May 2020 20:58:50 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 13 May 2020 20:58:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 13 May 2020 20:58:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2020 20:58:53 GMT
USER memcache
# Wed, 13 May 2020 20:58:53 GMT
EXPOSE 11211
# Wed, 13 May 2020 20:58:54 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93317744ae21705795946b5f7ccb9e69cd54b0d5b2bdbf48e38bc24ab2037dd4`  
		Last Modified: Thu, 23 Apr 2020 18:26:46 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22d5a6e65917b2d4ecdcd28e7178c79f43bd5cceabca1d40ef2708e66642b656`  
		Last Modified: Thu, 23 Apr 2020 18:26:47 GMT  
		Size: 14.7 KB (14705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55286676201b8c21a4a24628ece19d15221ee259c5df155ebcd0793841211612`  
		Last Modified: Wed, 13 May 2020 20:59:13 GMT  
		Size: 1.5 MB (1516837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c924249be839e9ffa60f403cf731eca93b38caa4e09dc57769e4cc25bcb5ca1`  
		Last Modified: Wed, 13 May 2020 20:59:13 GMT  
		Size: 284.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ded1f200c6c3b6d497cbb1a7fc81bd1ee1dd0cf53a43a8b068ce134ec3c7ab1`  
		Last Modified: Wed, 13 May 2020 20:59:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:b8d5715c8f0905fd1d24efc8254baa1ccf6933d9942b0b84c66750a5662bb811
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3841215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:331fbc8dc15f015e7fdd524a348b69696983085d2badb3a9a53cb7424a30567d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 23 Apr 2020 22:04:19 GMT
ADD file:33578d3cacfab86c195d99396dd012ec511796a1d2d8d6f0a02b8a055673c294 in / 
# Thu, 23 Apr 2020 22:04:22 GMT
CMD ["/bin/sh"]
# Mon, 27 Apr 2020 20:41:10 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Mon, 27 Apr 2020 20:41:12 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Wed, 13 May 2020 21:00:46 GMT
ENV MEMCACHED_VERSION=1.6.6
# Wed, 13 May 2020 21:00:47 GMT
ENV MEMCACHED_SHA1=d8895b12dc9fc82b389f1713e2c09cc6ca3d03e4
# Wed, 13 May 2020 21:11:09 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Wed, 13 May 2020 21:11:10 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 13 May 2020 21:11:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 13 May 2020 21:11:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2020 21:11:13 GMT
USER memcache
# Wed, 13 May 2020 21:11:13 GMT
EXPOSE 11211
# Wed, 13 May 2020 21:11:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3cfb62949d9d8613854db4d5fe502a9219c2b55a153043500078a64e880ae234`  
		Last Modified: Thu, 23 Apr 2020 22:05:12 GMT  
		Size: 2.4 MB (2422063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea5eed70290b5b33d1d0a27554b33b5998613f63667c5797fee672c96ea93df4`  
		Last Modified: Mon, 27 Apr 2020 20:50:54 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea75d9462432267b72327c7684218d1e4d40ec6d9b6578b0e8b79fdc50e2f99b`  
		Last Modified: Mon, 27 Apr 2020 20:50:54 GMT  
		Size: 13.6 KB (13633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e2c49241690acb15f16b690b318be68612c6665317e6f7f8b4cc57b57df0d59`  
		Last Modified: Wed, 13 May 2020 21:11:45 GMT  
		Size: 1.4 MB (1403856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b9dc2878fb274ac6ea5501d45e6a552af904357136bc2c90cfdd5c0a18e445e`  
		Last Modified: Wed, 13 May 2020 21:11:45 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:684fd6b097cf009d3e00a45e92d47256b86881e70726707607ba29c24ec95f3f`  
		Last Modified: Wed, 13 May 2020 21:11:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:84ab0fed3c7720f4b9d131bcbdc1df458b99a5e9950ea32ae9c139e5e874c877
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4298272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f21d64f8b964ecd80325828de3f81900ab258b90d021c999c8db169e9dc75790`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 11:04:28 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Fri, 24 Apr 2020 11:04:30 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Wed, 13 May 2020 21:06:36 GMT
ENV MEMCACHED_VERSION=1.6.6
# Wed, 13 May 2020 21:06:36 GMT
ENV MEMCACHED_SHA1=d8895b12dc9fc82b389f1713e2c09cc6ca3d03e4
# Wed, 13 May 2020 21:17:01 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Wed, 13 May 2020 21:17:02 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 13 May 2020 21:17:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 13 May 2020 21:17:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2020 21:17:07 GMT
USER memcache
# Wed, 13 May 2020 21:17:08 GMT
EXPOSE 11211
# Wed, 13 May 2020 21:17:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:29e5d40040c18c692ed73df24511071725b74956ca1a61fe6056a651d86a13bd`  
		Last Modified: Fri, 24 Apr 2020 00:15:41 GMT  
		Size: 2.7 MB (2724424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe5c53c35221a3533be681a0b6993aafc24fb08c1669f6e2cc3a14ae53ec625`  
		Last Modified: Fri, 24 Apr 2020 11:14:02 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8563552dafaf43a304948c84a7acc248f525f7112d769119ce9c6a68a5e3691`  
		Last Modified: Fri, 24 Apr 2020 11:14:02 GMT  
		Size: 15.5 KB (15487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e025d7a35db9442b2a837e76a39855504aabc39e7e3f988809d349af719667a`  
		Last Modified: Wed, 13 May 2020 21:17:37 GMT  
		Size: 1.6 MB (1556696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcaab3e6609fb2db6c7f55beb904fead407e5d2b97b6acafb93c96c03e56799e`  
		Last Modified: Wed, 13 May 2020 21:17:36 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6109ee9cf8d24da13ee3db362111fdb6fad712167f7a2df5c40282502c86c9c`  
		Last Modified: Wed, 13 May 2020 21:17:36 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:alpine` - linux; 386

```console
$ docker pull memcached@sha256:ee779870e380dd4c052f241c53fd38a6ad50cb63aff72e7c5ed1332fb66bea79
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4476231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0e2dba14886b5570a636ee035029db5c230a4c7a1c2a27ee44c0751a70a2e25`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 23 Apr 2020 21:16:04 GMT
ADD file:63bd8a316cba8c404cc2e32a5120406c24aee8db3224c469a6077b941d900863 in / 
# Thu, 23 Apr 2020 21:16:04 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 05:40:17 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Fri, 24 Apr 2020 05:40:18 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Wed, 13 May 2020 20:50:05 GMT
ENV MEMCACHED_VERSION=1.6.6
# Wed, 13 May 2020 20:50:05 GMT
ENV MEMCACHED_SHA1=d8895b12dc9fc82b389f1713e2c09cc6ca3d03e4
# Wed, 13 May 2020 21:00:15 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Wed, 13 May 2020 21:00:15 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 13 May 2020 21:00:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 13 May 2020 21:00:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2020 21:00:16 GMT
USER memcache
# Wed, 13 May 2020 21:00:16 GMT
EXPOSE 11211
# Wed, 13 May 2020 21:00:16 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2826c1e79865da7e0da0a993a2a38db61c3911e05b5df617439a86d4deac90fb`  
		Last Modified: Thu, 23 Apr 2020 21:16:32 GMT  
		Size: 2.8 MB (2808418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99c8f50e3ca0c1433cc286bd4e0a3745ecca7885db26d6589ed10f87bbaab945`  
		Last Modified: Fri, 24 Apr 2020 05:49:15 GMT  
		Size: 1.2 KB (1230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc013a10731c30303c911d27a87fd13538c35f156dd04c77830fd6aae807373`  
		Last Modified: Fri, 24 Apr 2020 05:49:16 GMT  
		Size: 16.2 KB (16152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:581eaa4a0c769e8f41ab1ac20af4e05814cb531a224ef2dbe1b497701b6e4ce9`  
		Last Modified: Wed, 13 May 2020 22:02:28 GMT  
		Size: 1.7 MB (1650028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7b876f113a5523b610398aae49ba66c705dc74ebe9d9bbb14421a29b37b9d0c`  
		Last Modified: Wed, 13 May 2020 22:02:28 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:063c1cbfa63f41d8c35db6ebbcd6c703677a29ee15140de1e193b1b20a14cad5`  
		Last Modified: Wed, 13 May 2020 22:02:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:65641c9d665bdf546da4a3425c6fa8950dfea3da135fece34ec9cd02e1e9f7ad
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4451916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8fa56a4612543254641d8bef3f069be35b451b380575990325f02932c1d31d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 23 Apr 2020 20:39:04 GMT
ADD file:1aaebe252dfb1885e066fcbc84aaa915bae149c3608f19600855ad1d4f7450c1 in / 
# Thu, 23 Apr 2020 20:39:06 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 06:58:53 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Fri, 24 Apr 2020 06:59:15 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Wed, 13 May 2020 21:52:24 GMT
ENV MEMCACHED_VERSION=1.6.6
# Wed, 13 May 2020 21:52:26 GMT
ENV MEMCACHED_SHA1=d8895b12dc9fc82b389f1713e2c09cc6ca3d03e4
# Wed, 13 May 2020 22:02:40 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Wed, 13 May 2020 22:02:41 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 13 May 2020 22:02:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 13 May 2020 22:02:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2020 22:02:48 GMT
USER memcache
# Wed, 13 May 2020 22:02:51 GMT
EXPOSE 11211
# Wed, 13 May 2020 22:02:52 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9a8fdc5b698322331ee7eba7dd6f66f3a4e956554db22dd1e834d519415b4f8e`  
		Last Modified: Thu, 23 Apr 2020 20:41:33 GMT  
		Size: 2.8 MB (2821843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8003ab8fdd2231d50550cbe8a4e5715a79d4707174e50e5208a3525a93b88d58`  
		Last Modified: Fri, 24 Apr 2020 07:09:36 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cf79da4de605128ba727e77467d72e9e1045bdd33fef6b7e4be6beb023816b1`  
		Last Modified: Fri, 24 Apr 2020 07:09:36 GMT  
		Size: 16.1 KB (16137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6db567fc6e2d79ea6f1c03ddc425dbdc0f8b451588832f6e7baf60ba1074942`  
		Last Modified: Wed, 13 May 2020 22:03:33 GMT  
		Size: 1.6 MB (1612264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91270a821a4eef3c8257ffc9a240571b34b80e984b5e9bee826fadf09df8c9d3`  
		Last Modified: Wed, 13 May 2020 22:03:32 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5cd487ad1a45f4788b910ad95b419e4c85c1744025f4047847d4da12cc293fc`  
		Last Modified: Wed, 13 May 2020 22:03:32 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:alpine` - linux; s390x

```console
$ docker pull memcached@sha256:e67fbfdb16b98451a2479f1b8ac1253153c1a0207446cd0b96ac3acbc8388374
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4167257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:172a7a8f96030a5bb34744dedb5dc60f06194a5967f790a4507f2f6a123a1e52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 23 Apr 2020 17:50:57 GMT
ADD file:a59a30c2fd43c9f3b820751a6f5a54688c14440a1ddace1ab255475f46e6ba2d in / 
# Thu, 23 Apr 2020 17:50:58 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 19:00:40 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Thu, 23 Apr 2020 19:00:41 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Wed, 13 May 2020 20:44:10 GMT
ENV MEMCACHED_VERSION=1.6.6
# Wed, 13 May 2020 20:44:10 GMT
ENV MEMCACHED_SHA1=d8895b12dc9fc82b389f1713e2c09cc6ca3d03e4
# Wed, 13 May 2020 20:53:11 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Wed, 13 May 2020 20:53:11 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 13 May 2020 20:53:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 13 May 2020 20:53:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2020 20:53:12 GMT
USER memcache
# Wed, 13 May 2020 20:53:13 GMT
EXPOSE 11211
# Wed, 13 May 2020 20:53:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7184c046fdf17da4c16ca482e5ede36e1f2d41ac8cea9c036e488fd149d6e8e7`  
		Last Modified: Thu, 23 Apr 2020 17:51:38 GMT  
		Size: 2.6 MB (2582859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca2971d466d139c0291506e9e9a74874f9720887c9d7589ac53625b827b4ddcb`  
		Last Modified: Wed, 13 May 2020 20:53:44 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dba5e1242654650bd369b46ebc84b7619dad9b2965728812cd6c53fbe412447`  
		Last Modified: Wed, 13 May 2020 20:53:50 GMT  
		Size: 15.4 KB (15364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c7a93509f92f968102940c5f29e41a5246d13ff2ca46d1b943913e1bdb0156`  
		Last Modified: Wed, 13 May 2020 20:53:45 GMT  
		Size: 1.6 MB (1567372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f782215b5f873e287c10ac50cd1ffafe9a48a11bce170ccb5ff224692251297a`  
		Last Modified: Wed, 13 May 2020 20:53:44 GMT  
		Size: 284.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c50080fccd2633d9e531227847ff62435c70da07804426afede4469d4c11a2`  
		Last Modified: Wed, 13 May 2020 20:53:44 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:latest`

```console
$ docker pull memcached@sha256:960a35d3fa6876225014a159850d1cb2067a22a924361bf40245846a939ae10b
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
$ docker pull memcached@sha256:4883efd6cfc85109bebdbca6e121dc2aa8095f5157f28407f86a2e5c2451bed6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 MB (30493622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddb9497b15e51ab6a3d1e51c0f943f3aefd6d7e18bf3029b6754b86db9ce67d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2020 01:20:56 GMT
ADD file:4d35f6c8bbbe6801cc5f44989730fb6d349a644ecb36eca481e7df25842d6321 in / 
# Tue, 09 Jun 2020 01:20:56 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:09:50 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 09 Jun 2020 07:09:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 07:09:55 GMT
ENV MEMCACHED_VERSION=1.6.6
# Tue, 09 Jun 2020 07:09:56 GMT
ENV MEMCACHED_SHA1=d8895b12dc9fc82b389f1713e2c09cc6ca3d03e4
# Tue, 09 Jun 2020 07:19:35 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 09 Jun 2020 07:19:35 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 09 Jun 2020 07:19:36 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 09 Jun 2020 07:19:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2020 07:19:36 GMT
USER memcache
# Tue, 09 Jun 2020 07:19:36 GMT
EXPOSE 11211
# Tue, 09 Jun 2020 07:19:36 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8559a31e96f442f2c7b6da49d6c84705f98a39d8be10b3f5f14821d0ee8417df`  
		Last Modified: Tue, 09 Jun 2020 01:25:50 GMT  
		Size: 27.1 MB (27098265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12f77f53de123f2d7381bf86a4a557eec07f2228f8d89b370535571abd3a73b6`  
		Last Modified: Tue, 09 Jun 2020 07:19:51 GMT  
		Size: 5.0 KB (4979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d4b924046de20905ddbdff30ce6ad8e886c078d3f37c5c65821fac3d7c82790`  
		Last Modified: Tue, 09 Jun 2020 07:19:52 GMT  
		Size: 2.2 MB (2196411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e09bb1c847d482fc3e3ffafe59cab644788c34accaa04a99fbddf6041eb36a38`  
		Last Modified: Tue, 09 Jun 2020 07:19:51 GMT  
		Size: 1.2 MB (1193561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba5fe779b315da0e76b031a17cbe96d16eb55dc9d1013834eaee74742aacf84f`  
		Last Modified: Tue, 09 Jun 2020 07:19:51 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df0fd9fcff94218c4182c328d693e7f79f185a577db6f8c94495011d7d21a726`  
		Last Modified: Tue, 09 Jun 2020 07:19:50 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:latest` - linux; arm variant v5

```console
$ docker pull memcached@sha256:0032271a53786587f2d8ce5e200da92642381a13f8e986846444978aede2f033
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.9 MB (27902256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2fabf24619ac13321a89500b1cbc36167c5effdd82a52ce4ab61218266a23fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2020 00:51:58 GMT
ADD file:7fde417d1c70a9ef2b4e468f6e2ee4cbd3f340fb2d5b67ede087c81520c95f4a in / 
# Tue, 09 Jun 2020 00:51:59 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 02:22:42 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 09 Jun 2020 02:22:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 02:22:57 GMT
ENV MEMCACHED_VERSION=1.6.6
# Tue, 09 Jun 2020 02:22:58 GMT
ENV MEMCACHED_SHA1=d8895b12dc9fc82b389f1713e2c09cc6ca3d03e4
# Tue, 09 Jun 2020 02:33:31 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 09 Jun 2020 02:33:32 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 09 Jun 2020 02:33:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 09 Jun 2020 02:33:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2020 02:33:36 GMT
USER memcache
# Tue, 09 Jun 2020 02:33:37 GMT
EXPOSE 11211
# Tue, 09 Jun 2020 02:33:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5b11fc09c1a26b11a7df7d593adf43baff53c5cdba71cf8a87ae4a6dd17eb52c`  
		Last Modified: Tue, 09 Jun 2020 00:59:24 GMT  
		Size: 24.8 MB (24837249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3baa3b116d24495c921f946ba122d5d463f3cf18626b0a80eb3f0bf9c4b6fe88`  
		Last Modified: Tue, 09 Jun 2020 02:34:05 GMT  
		Size: 4.9 KB (4892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c14a1ca330de132590916156f832d30211e6a8bfdb7f8e1dbda8dfdec102868b`  
		Last Modified: Tue, 09 Jun 2020 02:33:59 GMT  
		Size: 1.9 MB (1896798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b0e6e0e7ce0edef15dfccb8720e6c174a6fbc836fa16d483777c2e5b2bd0463`  
		Last Modified: Tue, 09 Jun 2020 02:33:59 GMT  
		Size: 1.2 MB (1162911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb4bdac6e198938d837ced8ba070de21a57812e113dd004d73ce5b1f2f21cd1`  
		Last Modified: Tue, 09 Jun 2020 02:33:59 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb5331ba343b59e5da9dc29eaaac2fa7bbd864b5607219c05aaadafb20d14dea`  
		Last Modified: Tue, 09 Jun 2020 02:33:59 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:latest` - linux; arm variant v7

```console
$ docker pull memcached@sha256:208c4d971048d73ce06174e8f5fa949e63e9a44e10f24e429e86478137c26c93
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25657276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ee4792808615b8ebe900de30833bca0acab941721546afc53b9599ebc2bbc12`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2020 01:01:24 GMT
ADD file:a35ca31d2a743d6a1738b1652f4f06c789abbca314d120f0e7e748311ac09ed2 in / 
# Tue, 09 Jun 2020 01:01:30 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 04:34:44 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 09 Jun 2020 04:34:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 04:34:54 GMT
ENV MEMCACHED_VERSION=1.6.6
# Tue, 09 Jun 2020 04:34:55 GMT
ENV MEMCACHED_SHA1=d8895b12dc9fc82b389f1713e2c09cc6ca3d03e4
# Tue, 09 Jun 2020 04:45:19 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 09 Jun 2020 04:45:20 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 09 Jun 2020 04:45:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 09 Jun 2020 04:45:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2020 04:45:23 GMT
USER memcache
# Tue, 09 Jun 2020 04:45:24 GMT
EXPOSE 11211
# Tue, 09 Jun 2020 04:45:24 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2dd003996c9ab82cac8112be0a4c04068e666e7a5d0cce3c65fb8f064de284e7`  
		Last Modified: Tue, 09 Jun 2020 01:10:25 GMT  
		Size: 22.7 MB (22705913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7558d3648391e15793448c35242f8b4fe3a52dab471b01435aefe6b66a2877d5`  
		Last Modified: Tue, 09 Jun 2020 04:45:54 GMT  
		Size: 4.9 KB (4897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13456188db29b97fae4ae70b260328de60b0bbfd9c0bc7c07e5e3d0555e3cd8`  
		Last Modified: Tue, 09 Jun 2020 04:45:54 GMT  
		Size: 1.8 MB (1811479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b7af48e3409ed86c6b2c330d38c8d31666b7852d2768e081d6aab0db9b9964`  
		Last Modified: Tue, 09 Jun 2020 04:45:55 GMT  
		Size: 1.1 MB (1134581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e94ff05fa5ccad573fbe816e4329a3cee522aa7d4d6050fe059e81748f5427e`  
		Last Modified: Tue, 09 Jun 2020 04:45:54 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d417f210bb27bb8c73a3b4fb69a7d0b0a4af17fca9dc4a46d476868546c3ab4`  
		Last Modified: Tue, 09 Jun 2020 04:45:55 GMT  
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
$ docker pull memcached@sha256:cf852d337b092501b99a68fd99fa098e3158f5c906a46346afbf283b5fe842a2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31165510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e46e67a23b0df4e0a189a624fd19acfddfb18da9babf02339f500cf08deece9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2020 01:39:49 GMT
ADD file:9fb8fd8bf970c4134f555964fe485a3baa84f1d4c91c5aa35276c24404de9d5d in / 
# Tue, 09 Jun 2020 01:39:49 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:13:54 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 09 Jun 2020 07:14:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 07:14:00 GMT
ENV MEMCACHED_VERSION=1.6.6
# Tue, 09 Jun 2020 07:14:00 GMT
ENV MEMCACHED_SHA1=d8895b12dc9fc82b389f1713e2c09cc6ca3d03e4
# Tue, 09 Jun 2020 07:23:19 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 09 Jun 2020 07:23:20 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 09 Jun 2020 07:23:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 09 Jun 2020 07:23:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2020 07:23:21 GMT
USER memcache
# Tue, 09 Jun 2020 07:23:21 GMT
EXPOSE 11211
# Tue, 09 Jun 2020 07:23:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:860f8957d8be856e2235a28e49fc4dca17254951e0eb67d760769755656f5cad`  
		Last Modified: Tue, 09 Jun 2020 01:45:01 GMT  
		Size: 27.8 MB (27754909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177c77c201722fd2e38ce7eb3a8ed9e3626b787675b4f97e8b30dc814b5d8e0f`  
		Last Modified: Tue, 09 Jun 2020 07:23:39 GMT  
		Size: 4.9 KB (4888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c70883b4ec6865b74674af4157d587f6931be09be0064b4e839d84ece1f752c`  
		Last Modified: Tue, 09 Jun 2020 07:23:40 GMT  
		Size: 2.2 MB (2208123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:361fde9e5eba8562e2ba9fbb13637811f7ab77ed8154567ea7936e738712c10a`  
		Last Modified: Tue, 09 Jun 2020 07:23:40 GMT  
		Size: 1.2 MB (1197183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b45cbcad6d03b87559d072f7de237e45b57f43aa3cda322a92efd95db143bbc6`  
		Last Modified: Tue, 09 Jun 2020 07:23:39 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d26134208cbdd2c15c5eb835332adb873def0e0b00d41ed26878d5a6668e059`  
		Last Modified: Tue, 09 Jun 2020 07:23:39 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:latest` - linux; mips64le

```console
$ docker pull memcached@sha256:f549c5445d205ef1bb085e26731cbb587c5d0b28e3ee334cf94a089f1edd5299
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.7 MB (28727890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:195974ad8b777f8d1cb7fc6662ed73f1dfcb4adae667b145bfbbdc135a35f83f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2020 01:10:06 GMT
ADD file:faf18b832680e98050b98c329add242425904e64c6a5a491c22d33e9417ef323 in / 
# Tue, 09 Jun 2020 01:10:06 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 02:47:55 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 09 Jun 2020 02:48:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 02:48:09 GMT
ENV MEMCACHED_VERSION=1.6.6
# Tue, 09 Jun 2020 02:48:09 GMT
ENV MEMCACHED_SHA1=d8895b12dc9fc82b389f1713e2c09cc6ca3d03e4
# Tue, 09 Jun 2020 03:00:07 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 09 Jun 2020 03:00:07 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 09 Jun 2020 03:00:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 09 Jun 2020 03:00:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2020 03:00:10 GMT
USER memcache
# Tue, 09 Jun 2020 03:00:10 GMT
EXPOSE 11211
# Tue, 09 Jun 2020 03:00:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:76f2a0c8ea98ebd699a77ced9c677e97cd54b038a8c5e89670af78f38b047b33`  
		Last Modified: Tue, 09 Jun 2020 01:18:14 GMT  
		Size: 25.8 MB (25764040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaea43187ee39f4dcd055f5a5ef4a57ed46a2c369ece86cd6a0cbbe0d649a185`  
		Last Modified: Tue, 09 Jun 2020 03:00:37 GMT  
		Size: 5.0 KB (4976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d990cccfa6753239cf27654288742581cb106cc1dac9e6dbe774114b185810`  
		Last Modified: Tue, 09 Jun 2020 03:00:38 GMT  
		Size: 1.8 MB (1776013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8377e577748912f253e08d4980e821ac6204d4dc430cff1238bbc01ea6c7ca`  
		Last Modified: Tue, 09 Jun 2020 03:00:37 GMT  
		Size: 1.2 MB (1182454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45fc1e75da507493f88c70b2acd4274a2ebe28bac45a4d9d774f1b6fb863b010`  
		Last Modified: Tue, 09 Jun 2020 03:00:33 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23848a16b8c2670e004ce1a89e3d51af6c75e11d2dd1c86c89e89f1c55821032`  
		Last Modified: Tue, 09 Jun 2020 03:00:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:latest` - linux; ppc64le

```console
$ docker pull memcached@sha256:9d74db6d0c506cd7b5171129f6cb702277aaa191e7bafd242c551e26b7e582a2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.1 MB (34071646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caf1d9ee7c1f4c75ff401acd07ac5e28aa61e674424f1bf57ac75673845d420e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2020 01:22:34 GMT
ADD file:796aad1a35ba276b8cccc19987c152a713db101b2b65e30923db753f5b7f4b0f in / 
# Tue, 09 Jun 2020 01:22:38 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 04:23:19 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 09 Jun 2020 04:23:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 04:23:43 GMT
ENV MEMCACHED_VERSION=1.6.6
# Tue, 09 Jun 2020 04:23:47 GMT
ENV MEMCACHED_SHA1=d8895b12dc9fc82b389f1713e2c09cc6ca3d03e4
# Tue, 09 Jun 2020 04:35:57 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 09 Jun 2020 04:36:01 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 09 Jun 2020 04:36:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 09 Jun 2020 04:36:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2020 04:36:21 GMT
USER memcache
# Tue, 09 Jun 2020 04:36:26 GMT
EXPOSE 11211
# Tue, 09 Jun 2020 04:36:32 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:63dbb66c5119bb5086d9e6fb6b154211afc20b44ed136ab7df808f6044cfc6f1`  
		Last Modified: Tue, 09 Jun 2020 01:31:04 GMT  
		Size: 30.5 MB (30524405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:326347d3599c113aed8b360975de1e1295d880747ab63b945e59748ff4e00e7f`  
		Last Modified: Tue, 09 Jun 2020 04:37:10 GMT  
		Size: 5.0 KB (4980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b3c6b0b46229c12b05433642c55de042b24a1364fd631996450f9a4bb136143`  
		Last Modified: Tue, 09 Jun 2020 04:37:10 GMT  
		Size: 2.3 MB (2322714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:716f59d7781a40e402cd8add331e26fc33fbaab6a82614c43746b1afdf315747`  
		Last Modified: Tue, 09 Jun 2020 04:37:10 GMT  
		Size: 1.2 MB (1219139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b63b4e5e82673252ff53e7021ac30af1147b4a81f99a82aa1a3c58085688666`  
		Last Modified: Tue, 09 Jun 2020 04:37:10 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abf841a99428dea3a743f5fde752d2ba68f050307880829b6c354c5e5bcdf04e`  
		Last Modified: Tue, 09 Jun 2020 04:37:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:latest` - linux; s390x

```console
$ docker pull memcached@sha256:e481d6155413e4b844009223fa04cca68b15e430b4e5476a0e9967f49af57a50
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.8 MB (28789009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd9a8cff3ec775f7b2c039af1fb74ca8706705a6715c681797cd43f02f82090a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jun 2020 01:42:37 GMT
ADD file:b21d426de40a194c6c76ed27593f33fb1ea470e15d4d43b00d7601472110de1a in / 
# Tue, 09 Jun 2020 01:42:38 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 03:40:46 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 09 Jun 2020 03:40:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 03:40:50 GMT
ENV MEMCACHED_VERSION=1.6.6
# Tue, 09 Jun 2020 03:40:50 GMT
ENV MEMCACHED_SHA1=d8895b12dc9fc82b389f1713e2c09cc6ca3d03e4
# Tue, 09 Jun 2020 03:49:43 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 09 Jun 2020 03:49:43 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 09 Jun 2020 03:49:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 09 Jun 2020 03:49:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2020 03:49:44 GMT
USER memcache
# Tue, 09 Jun 2020 03:49:44 GMT
EXPOSE 11211
# Tue, 09 Jun 2020 03:49:44 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:405e75bf6bb0104d67fcebf58e07cd21bf344589df9c1a41c00354a60ea3a604`  
		Last Modified: Tue, 09 Jun 2020 01:46:30 GMT  
		Size: 25.7 MB (25712668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2c03af295f2075ceec6e6cc9874e8666d63a3b26614e659f1396a367f9e2ebc`  
		Last Modified: Tue, 09 Jun 2020 03:50:08 GMT  
		Size: 5.0 KB (5023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989e958beedef1b77252896a7ad5fba801dcef12cde52098e6a9d46a57ec6d9b`  
		Last Modified: Tue, 09 Jun 2020 03:50:08 GMT  
		Size: 1.9 MB (1886033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a68df8456455057906a59f6ff163a22e695cf310443f17f2af2a3742d1e1eaaf`  
		Last Modified: Tue, 09 Jun 2020 03:50:13 GMT  
		Size: 1.2 MB (1184878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7cd9a3bb1b818c1b06baad270500facbfcbaab3102aa9fb203b7aa09fbf8be3`  
		Last Modified: Tue, 09 Jun 2020 03:50:23 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab09b03baf0f78a40dff16e0620f3af6bd5e050654d20b3a1c073fd88d1dff42`  
		Last Modified: Tue, 09 Jun 2020 03:50:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
