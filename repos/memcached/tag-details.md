<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `memcached`

-	[`memcached:1`](#memcached1)
-	[`memcached:1-alpine`](#memcached1-alpine)
-	[`memcached:1-alpine3.16`](#memcached1-alpine316)
-	[`memcached:1-bullseye`](#memcached1-bullseye)
-	[`memcached:1.6`](#memcached16)
-	[`memcached:1.6-alpine`](#memcached16-alpine)
-	[`memcached:1.6-alpine3.16`](#memcached16-alpine316)
-	[`memcached:1.6-bullseye`](#memcached16-bullseye)
-	[`memcached:1.6.16`](#memcached1616)
-	[`memcached:1.6.16-alpine`](#memcached1616-alpine)
-	[`memcached:1.6.16-alpine3.16`](#memcached1616-alpine316)
-	[`memcached:1.6.16-bullseye`](#memcached1616-bullseye)
-	[`memcached:alpine`](#memcachedalpine)
-	[`memcached:alpine3.16`](#memcachedalpine316)
-	[`memcached:bullseye`](#memcachedbullseye)
-	[`memcached:latest`](#memcachedlatest)

## `memcached:1`

```console
$ docker pull memcached@sha256:22ed710ee778c797865ebff08e825df55df20508075cf275311cca55a235e652
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
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
$ docker pull memcached@sha256:a5dc74cbb9f905192c3caa290e32a4c725aba0d21f94c15cd7ca8530ffe01776
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32970763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdff4547b1b7092afe2104dbf710a439a2b8bcdf54b87fbfda0de4631da4ef6a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Aug 2022 00:20:50 GMT
ADD file:7726efb0e0eb5003dbcf2967ec29364479eec8b41f2569ff189372153115b54b in / 
# Tue, 23 Aug 2022 00:20:51 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 02:54:26 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 23 Aug 2022 02:54:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 02:54:30 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 23 Aug 2022 02:54:30 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 23 Aug 2022 02:57:13 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 23 Aug 2022 02:57:13 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 23 Aug 2022 02:57:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 23 Aug 2022 02:57:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 02:57:14 GMT
USER memcache
# Tue, 23 Aug 2022 02:57:14 GMT
EXPOSE 11211
# Tue, 23 Aug 2022 02:57:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7a6db449b51b92eac5c81cdbd82917785343f1664b2be57b22337b0a40c5b29d`  
		Last Modified: Tue, 23 Aug 2022 00:24:59 GMT  
		Size: 31.4 MB (31381485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa73fb65ea8b12a2375459f0d656d3ad06e2863c906fcf962486eda3701f3fd6`  
		Last Modified: Tue, 23 Aug 2022 02:57:38 GMT  
		Size: 5.0 KB (4981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:502b4e8803067b28098d0ea52281cfef66da1ee1e869241612b545d7e9ff12de`  
		Last Modified: Tue, 23 Aug 2022 02:57:38 GMT  
		Size: 328.1 KB (328108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4be7903a0371d25a8e62fb8f58db1b4cc0d71407206895e81b2c5edddd96716`  
		Last Modified: Tue, 23 Aug 2022 02:57:38 GMT  
		Size: 1.3 MB (1255782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ece99ce94967ae22a842630bc182d3052a46922074b332055aa65763b70c4adb`  
		Last Modified: Tue, 23 Aug 2022 02:57:37 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72302fb7547064b5cd2773f9e54e03b6579b64dc8399245d683058505e87860`  
		Last Modified: Tue, 23 Aug 2022 02:57:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1` - linux; arm variant v5

```console
$ docker pull memcached@sha256:7688ba62a1e2ca12e4fcfc18213eec8b6c8e967bb62395189bdc8d1b095f9ec8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 MB (30466108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63aeac5a0551e3a97aaddf116dbcb2a96b84635664ff3755675a42744590c23c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Aug 2022 01:17:14 GMT
ADD file:83fb076a50e935419eb0db2bd97477d7ed5f16aaac4c8cc35a4a69ac612df327 in / 
# Tue, 23 Aug 2022 01:17:14 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 01:49:29 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 23 Aug 2022 01:49:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 01:49:33 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 23 Aug 2022 01:49:34 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 23 Aug 2022 01:55:05 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 23 Aug 2022 01:55:05 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 23 Aug 2022 01:55:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 23 Aug 2022 01:55:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 01:55:06 GMT
USER memcache
# Tue, 23 Aug 2022 01:55:06 GMT
EXPOSE 11211
# Tue, 23 Aug 2022 01:55:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:74eb5afab626122970f8620ac001fcc4a200725acb05519b85aba47a38bf1016`  
		Last Modified: Tue, 23 Aug 2022 01:22:44 GMT  
		Size: 28.9 MB (28917250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a1b82f1abc9998be67c6dab29a896fcf5377c55fa3c09f0f60355321d0cc7e`  
		Last Modified: Tue, 23 Aug 2022 01:55:43 GMT  
		Size: 4.9 KB (4896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8d24ffcddd09d398cd33e29661cc865588572fdcfc4224b2ea8c0d1d001ed6`  
		Last Modified: Tue, 23 Aug 2022 01:55:44 GMT  
		Size: 316.6 KB (316628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:099cd43abb1475212736fcbb1adbd31b235ae10d1cbd4785e375473e77218967`  
		Last Modified: Tue, 23 Aug 2022 01:55:44 GMT  
		Size: 1.2 MB (1226927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b9006a418f2ced9ced0ca431dda2ce3543860c17742fc092a2309af44e78f22`  
		Last Modified: Tue, 23 Aug 2022 01:55:43 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df94046aab5da41252820ad1cb5d98c7a10c344be39148a95f1d6ad9e052bc1b`  
		Last Modified: Tue, 23 Aug 2022 01:55:44 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1` - linux; arm variant v7

```console
$ docker pull memcached@sha256:25e768546f1e321b2a9031611f8ecd4081990c82f8774f7e051a5480cf18445d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28076294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5959e4e12e1b75611311d3866bc95f9fe30048418f972e70fa2c671a66149fdd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 02 Aug 2022 00:58:59 GMT
ADD file:1575b776a15adacebc0875642e97a80807d42dcfc8917e1406d47af7ac244c97 in / 
# Tue, 02 Aug 2022 00:58:59 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 06:28:56 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 02 Aug 2022 06:29:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Aug 2022 21:30:08 GMT
ENV MEMCACHED_VERSION=1.6.16
# Thu, 04 Aug 2022 21:30:08 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Thu, 04 Aug 2022 21:36:35 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Thu, 04 Aug 2022 21:36:35 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 04 Aug 2022 21:36:36 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 04 Aug 2022 21:36:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Aug 2022 21:36:37 GMT
USER memcache
# Thu, 04 Aug 2022 21:36:37 GMT
EXPOSE 11211
# Thu, 04 Aug 2022 21:36:37 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1dd75a3a9c893a7dc313f683dd62464b7eab6c6d522ee62c8a17022631830f32`  
		Last Modified: Tue, 02 Aug 2022 01:06:45 GMT  
		Size: 26.6 MB (26560586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44a675a8ce135f198539dc76b078733393238f7c7b899c8635980eed8f35f1cc`  
		Last Modified: Tue, 02 Aug 2022 09:35:13 GMT  
		Size: 4.9 KB (4890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497b0afd04c92a1e5d41f58dbc0d5d544b8880d000c0ffbd03adb48c32c0116b`  
		Last Modified: Tue, 02 Aug 2022 09:35:13 GMT  
		Size: 312.1 KB (312067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8874fe992be272d0e0780725714c2439507699c15bfad1a073df948a34eb668d`  
		Last Modified: Fri, 05 Aug 2022 00:37:30 GMT  
		Size: 1.2 MB (1198344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cd5e042b98c640c152a56816e122c5e7b0abe91535d5d891dceed9748e42129`  
		Last Modified: Fri, 05 Aug 2022 00:37:29 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e871a0f93bdc7cb723e47f45514f914186b73d1890a53cdfe8525dd034926d59`  
		Last Modified: Fri, 05 Aug 2022 00:37:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:759082b00d406f92781542ce86756eb73c5efe20acc7df6c25ac86be320a3ef5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31433439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e91fe6663d9d90deed07c1d003a80fa6698137267c83310828f24a7ef63f6ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 02 Aug 2022 00:40:38 GMT
ADD file:6039adfbca55ed34a719c37672c664e3524130a0e2a3b8663629b8120b81b790 in / 
# Tue, 02 Aug 2022 00:40:39 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 03:56:15 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 02 Aug 2022 03:56:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Aug 2022 20:33:46 GMT
ENV MEMCACHED_VERSION=1.6.16
# Thu, 04 Aug 2022 20:33:47 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Thu, 04 Aug 2022 20:36:17 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Thu, 04 Aug 2022 20:36:19 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 04 Aug 2022 20:36:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 04 Aug 2022 20:36:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Aug 2022 20:36:21 GMT
USER memcache
# Thu, 04 Aug 2022 20:36:22 GMT
EXPOSE 11211
# Thu, 04 Aug 2022 20:36:23 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a9fe95647e78b5516c7e2327355b6996e2ea295cd76ae242cbfe87f016b4e760`  
		Last Modified: Tue, 02 Aug 2022 00:46:05 GMT  
		Size: 30.1 MB (30054304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b983df009e7dc88033f53f015c09c56fd4db032d1abcade3333d8d4b515ff4af`  
		Last Modified: Tue, 02 Aug 2022 03:59:48 GMT  
		Size: 4.9 KB (4902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60720019405b50af041f391ec7dad90893ee95fc63fd6b3fb9da04850936f5db`  
		Last Modified: Tue, 02 Aug 2022 03:59:48 GMT  
		Size: 119.2 KB (119225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70569bedb4ee539337d6d3fd88e4076a1464b3a77bcfcca6604e18b815dbc402`  
		Last Modified: Thu, 04 Aug 2022 20:40:00 GMT  
		Size: 1.3 MB (1254600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:565112c01ad7b82688180f4fe70f5433126d79cc4b74e3d7f308601e2d34d9fe`  
		Last Modified: Thu, 04 Aug 2022 20:39:59 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce11290eb88924797c1fa048bd052c1243e4cb47e3469b26f3f1a3bc26472d19`  
		Last Modified: Thu, 04 Aug 2022 20:39:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1` - linux; 386

```console
$ docker pull memcached@sha256:3770f2e3c3f2abb5f85a6a615e62fd5c78a61513ca573ee4385adf42629bd88c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.8 MB (33775724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2804b930e07f367a1e5adc6a5631e87c78a986d3ad64e06e3c549c20ad7ce735`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Aug 2022 01:02:40 GMT
ADD file:5ca62c98116941aaa64ec72afb689a088c46f75a3e83d5b0d4e58d65ec905ccd in / 
# Tue, 23 Aug 2022 01:02:40 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 03:22:44 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 23 Aug 2022 03:22:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 03:22:49 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 23 Aug 2022 03:22:50 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 23 Aug 2022 03:26:54 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 23 Aug 2022 03:26:56 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 23 Aug 2022 03:26:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 23 Aug 2022 03:26:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 03:26:58 GMT
USER memcache
# Tue, 23 Aug 2022 03:26:59 GMT
EXPOSE 11211
# Tue, 23 Aug 2022 03:27:00 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6b3cb4a05a891d9d8a87a2bd7247b16f79832a9d4afbad3ff5068f6fc2ba1560`  
		Last Modified: Tue, 23 Aug 2022 01:08:25 GMT  
		Size: 32.4 MB (32387317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd24201e0b5e9a68a67bdc3b464a01aeb9a2e5a859a582cdaa80ab08a608337`  
		Last Modified: Tue, 23 Aug 2022 03:27:47 GMT  
		Size: 4.8 KB (4774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3070e5e3b1d98fa0b67b8390880b7596c4719b774864de21f36ed86873041793`  
		Last Modified: Tue, 23 Aug 2022 03:27:48 GMT  
		Size: 130.1 KB (130136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a076923bc48ef00816393d79ac2aa3ad931f47309aff7a6cf0c6c74d443080f`  
		Last Modified: Tue, 23 Aug 2022 03:27:48 GMT  
		Size: 1.3 MB (1253091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7169b397a99c6597495d00b3cb6b04483b8950d04bc7cbdcccf983f225294bb4`  
		Last Modified: Tue, 23 Aug 2022 03:27:48 GMT  
		Size: 288.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55ee497fd4fa66154f7c38bc2bb37f6e356318dc032b26ed65eb94ddc8355995`  
		Last Modified: Tue, 23 Aug 2022 03:27:47 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1` - linux; mips64le

```console
$ docker pull memcached@sha256:0d6798ccd4a9ac44c6ca7c358b2de6bdedbfe104de7d9987eedc68864ab8acc0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 MB (31002934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aca3e1ecca25fb97ad1d376d73b212cad11874d1f051c4c4bac1b2d27abc15fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 02 Aug 2022 01:10:34 GMT
ADD file:6dc22a1e5b5fcf23f2549406ddcc45c4e244f46e21eafa881de81fa87438e5d8 in / 
# Tue, 02 Aug 2022 01:10:38 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 03:22:53 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 02 Aug 2022 03:23:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Aug 2022 20:07:25 GMT
ENV MEMCACHED_VERSION=1.6.16
# Thu, 04 Aug 2022 20:07:28 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Thu, 04 Aug 2022 20:14:28 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Thu, 04 Aug 2022 20:14:30 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 04 Aug 2022 20:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 04 Aug 2022 20:14:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Aug 2022 20:14:40 GMT
USER memcache
# Thu, 04 Aug 2022 20:14:42 GMT
EXPOSE 11211
# Thu, 04 Aug 2022 20:14:45 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:88350749a27614c791450c256b051f023d81cdd256211274b1efac493779d2be`  
		Last Modified: Tue, 02 Aug 2022 01:21:02 GMT  
		Size: 29.6 MB (29628964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:117af7bbaadea9c81bbaa3a8a77b1ab5cd05bcac856c462cda2e81c9a40596ab`  
		Last Modified: Tue, 02 Aug 2022 03:30:45 GMT  
		Size: 4.9 KB (4863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a16d313748bd6b2dade87de73d79edd8a08e4cb662769a717f8587abc8d5e0`  
		Last Modified: Tue, 02 Aug 2022 03:30:46 GMT  
		Size: 117.1 KB (117127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d524786af3243ee367d118f6d5260cffa06d800f492f9b4bb36c910958186933`  
		Last Modified: Thu, 04 Aug 2022 20:15:05 GMT  
		Size: 1.3 MB (1251571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4badb1f1970762d08dbd43d7e101081a5fabd3c45e18afd70636397e83102d2f`  
		Last Modified: Thu, 04 Aug 2022 20:15:04 GMT  
		Size: 288.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3102636392803c3bbff48f39e7f143e3bf9a0528365d63b90dc31cd32060d3e0`  
		Last Modified: Thu, 04 Aug 2022 20:15:04 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1` - linux; ppc64le

```console
$ docker pull memcached@sha256:6eac50a2d123c021e75657700bdd2d0335dcc97db595e783eb6feaf81e0d6ab0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 MB (36969051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77075f2945ec5e196ccf20148829ebe266a384c2972f723f72361e05e3ee1bf5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Aug 2022 01:24:52 GMT
ADD file:d35213360d726a18e220276d33f245115c3e94a321addaa4c9127488368b0203 in / 
# Tue, 23 Aug 2022 01:24:54 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 02:34:49 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 23 Aug 2022 02:34:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 02:34:56 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 23 Aug 2022 02:34:56 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 23 Aug 2022 02:38:10 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 23 Aug 2022 02:38:10 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 23 Aug 2022 02:38:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 23 Aug 2022 02:38:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 02:38:12 GMT
USER memcache
# Tue, 23 Aug 2022 02:38:12 GMT
EXPOSE 11211
# Tue, 23 Aug 2022 02:38:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:698954eda09d38dd1ccc9ce777b1f6bc7f7473fc6c4c3eb634acc8d035a42eae`  
		Last Modified: Tue, 23 Aug 2022 01:30:36 GMT  
		Size: 35.3 MB (35284280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ffb080d920662043edc67113c0de4c68258ad19c0fffd9e3b79fa01800c6015`  
		Last Modified: Tue, 23 Aug 2022 02:39:09 GMT  
		Size: 5.0 KB (4980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b1f66b68991d8f5ab064b3988db37a48b8f28b4ef0eb8e83efa4c419b630ff`  
		Last Modified: Tue, 23 Aug 2022 02:39:09 GMT  
		Size: 356.9 KB (356931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9653070548c34c29ed693878ef68223dbe9ccefc4653b86d3c8225bc8f85ac1`  
		Last Modified: Tue, 23 Aug 2022 02:39:09 GMT  
		Size: 1.3 MB (1322453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd51b501bab55d128a547f5c14e6410e4ef4b7b08f1867c7c933db716d7791e7`  
		Last Modified: Tue, 23 Aug 2022 02:39:09 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e693f7e8dfc8fe4a2af505658484b885fe097586d4f22c43aaf8278756e76ca`  
		Last Modified: Tue, 23 Aug 2022 02:39:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1` - linux; s390x

```console
$ docker pull memcached@sha256:4f7e9706bfd16d98bfb48a6435c8359a167ab733777f16f24996cad3f431bdc5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31211398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6739ca31062c74398fdfec102afbacead1c25fa0decf2fa14bdecdcb6b160543`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 02 Aug 2022 00:42:27 GMT
ADD file:c2afc8990930846fbe7c99bfdfe9ea562c75feb6e3c9122431f7c9f8b5e51a7f in / 
# Tue, 02 Aug 2022 00:42:29 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 02:37:02 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 02 Aug 2022 02:37:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Aug 2022 20:28:18 GMT
ENV MEMCACHED_VERSION=1.6.16
# Thu, 04 Aug 2022 20:28:18 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Thu, 04 Aug 2022 20:31:37 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Thu, 04 Aug 2022 20:31:37 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 04 Aug 2022 20:31:37 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 04 Aug 2022 20:31:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Aug 2022 20:31:38 GMT
USER memcache
# Thu, 04 Aug 2022 20:31:38 GMT
EXPOSE 11211
# Thu, 04 Aug 2022 20:31:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:026d311d0716db60eba0572ea784c21031f420960510cebcc383dc53949b4db8`  
		Last Modified: Tue, 02 Aug 2022 00:48:01 GMT  
		Size: 29.6 MB (29640259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0ffdb328e548bd6b6311c78665ac8cd3be8f0b2e09691701d9b0bae0924f8f5`  
		Last Modified: Tue, 02 Aug 2022 02:41:16 GMT  
		Size: 5.0 KB (5025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fbb9677007b0ebab2fe6feab520da1962d3fcffb3490aa844681a46fcb35749`  
		Last Modified: Tue, 02 Aug 2022 02:41:16 GMT  
		Size: 324.2 KB (324183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9c93abfa1f832f2e1f02fbe7b9a489735142c2051dafa7af20d985ff2e2106b`  
		Last Modified: Thu, 04 Aug 2022 20:36:17 GMT  
		Size: 1.2 MB (1241523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f78bf4cf172bedc6ad3c92b859859b10c0394104262328d5664ddc0b1488b29`  
		Last Modified: Thu, 04 Aug 2022 20:36:17 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6a26d2d4c34166613098e1380842f1355b534e2335a1dea2128c193b7f19bec`  
		Last Modified: Thu, 04 Aug 2022 20:36:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:1-alpine`

```console
$ docker pull memcached@sha256:67a95346c7d0fbe3b1e6d1160cdec386503e0ad7c06e8d4056c3b0754e679eed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `memcached:1-alpine` - linux; amd64

```console
$ docker pull memcached@sha256:b1e59612ccc1ab79ccb764e8ae694c89c6e2dece9927b202c1a1820a665268f4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3867486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af3c4fe62d9dafd4336d17fc19dcc8e0ea69a41c4ea586e0544c371319a9497b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:53:39 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Tue, 09 Aug 2022 20:53:40 GMT
RUN apk add --no-cache libsasl
# Tue, 09 Aug 2022 20:53:40 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 09 Aug 2022 20:53:41 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 09 Aug 2022 20:56:30 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 09 Aug 2022 20:56:30 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 09 Aug 2022 20:56:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 09 Aug 2022 20:56:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 20:56:31 GMT
USER memcache
# Tue, 09 Aug 2022 20:56:31 GMT
EXPOSE 11211
# Tue, 09 Aug 2022 20:56:31 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d572ef57cdf8eb58de4b4e89970c5e64c6a2f8470bbbe4746efd56927df10611`  
		Last Modified: Tue, 09 Aug 2022 20:57:08 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed8976416286665206f17c9c2ead879425c6c6c62051fa7af308abd8790c0bc`  
		Last Modified: Tue, 09 Aug 2022 20:57:08 GMT  
		Size: 108.3 KB (108322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c657d873aa5cf9fbc93f3c3b68b8e7543ec1bc6335404b259ea5a7db4196422d`  
		Last Modified: Tue, 09 Aug 2022 20:57:08 GMT  
		Size: 951.4 KB (951438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f91921ed85e235501e9cd091c8d8601f04ea194fe4a461629fe7ab9eb9badd`  
		Last Modified: Tue, 09 Aug 2022 20:57:08 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198a10264961105745cf7038c02c22ae20695d9213c38421ec14d7cc8eda0d44`  
		Last Modified: Tue, 09 Aug 2022 20:57:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:79a5646a0c845a791f36017fda3292281b48295b06c53f13d62c9f94237d4731
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3960292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2afac0e49af3ce3f1769abe11a29f8f5610c6a736d8c5b6c7b9770c8d8e94e91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 16 Dec 2020 23:58:14 GMT
ADD file:bd07f77a2b2741ca6bda80d9203be9c7274cf73145bff778cf000db0d8d4e903 in / 
# Wed, 16 Dec 2020 23:58:15 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 06:43:29 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Thu, 17 Dec 2020 06:43:31 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Thu, 17 Dec 2020 06:43:33 GMT
ENV MEMCACHED_VERSION=1.6.9
# Thu, 17 Dec 2020 06:43:35 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Thu, 17 Dec 2020 06:46:32 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Thu, 17 Dec 2020 06:46:33 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 17 Dec 2020 06:46:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 17 Dec 2020 06:46:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 06:46:36 GMT
USER memcache
# Thu, 17 Dec 2020 06:46:38 GMT
EXPOSE 11211
# Thu, 17 Dec 2020 06:46:39 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c58e8a26a8407acc3ead776f6526efa889fda03270a8d05109208d9f59159420`  
		Last Modified: Wed, 16 Dec 2020 23:58:59 GMT  
		Size: 2.4 MB (2407555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68564bbfc09f153688e942bf54d5375d1e27f3507c0bed6b038c2ac8ce095aa5`  
		Last Modified: Thu, 17 Dec 2020 06:46:58 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cac3a91edee49d0b08a25706ae86059bed89941a08b496e72ef092e57c4ecb3`  
		Last Modified: Thu, 17 Dec 2020 06:46:58 GMT  
		Size: 13.8 KB (13825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf16e9bb942ec42a35a792beab65aea843209e7bdde7e856499b9fc85f93bc4e`  
		Last Modified: Thu, 17 Dec 2020 06:46:58 GMT  
		Size: 1.5 MB (1537248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc15394239bd0c083e1b6df806aa5ffeb8b9cc7e80113afc2959721de49f90d1`  
		Last Modified: Thu, 17 Dec 2020 06:46:58 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:482f0eb571548eae5720c652ff7da13558e56a8722dc9932cf7eb1ef3eb33acb`  
		Last Modified: Thu, 17 Dec 2020 06:46:58 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:44f0d141458db00ee50b9ad0ec9f39a08f2054fe45924bafddc3920d446727f0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3757682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5799dfb510c6b2e85d9290ef1eae349ba3365b9584932dbc450562979a046d9f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:48:03 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Tue, 09 Aug 2022 20:48:05 GMT
RUN apk add --no-cache libsasl
# Tue, 09 Aug 2022 20:48:05 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 09 Aug 2022 20:48:06 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 09 Aug 2022 20:50:51 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 09 Aug 2022 20:50:53 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 09 Aug 2022 20:50:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 09 Aug 2022 20:50:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 20:50:55 GMT
USER memcache
# Tue, 09 Aug 2022 20:50:56 GMT
EXPOSE 11211
# Tue, 09 Aug 2022 20:50:57 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d15db589ad12df2825238bc4f6832b2c6e3d991704c9b41db7865df5d402276`  
		Last Modified: Tue, 09 Aug 2022 20:51:50 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103b4be7608736e9e24d225ccd97cc4dfad6bacbe7bcf2ca1cd716b45ee32855`  
		Last Modified: Tue, 09 Aug 2022 20:51:50 GMT  
		Size: 109.6 KB (109566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be29d81faebb3b793bdb052326cbb181f786eb99078f62f6f00935c60c14a9fe`  
		Last Modified: Tue, 09 Aug 2022 20:51:50 GMT  
		Size: 938.8 KB (938808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a590dbe104d4e1ec4c488c22500f75e3b44977e09523893500694356ff65008b`  
		Last Modified: Tue, 09 Aug 2022 20:51:50 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da7fd81bf28f2c80e4823f86aea754145c41614f1a924f56f0d2f7e51747873`  
		Last Modified: Tue, 09 Aug 2022 20:51:50 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine` - linux; 386

```console
$ docker pull memcached@sha256:e6fc7462999869fb634dbc73338735811a34ba127cbf512785b2d036132b7496
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3891350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b662b6ea7b7b0638994baa098f88f7a247ecc3da8fa1057e586dd3fdd1fe007`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Aug 2022 17:38:39 GMT
ADD file:b828bc14bc5ff03c8f7310fe0aed6ac5df19a393622d5d1d779a523234d07c0a in / 
# Tue, 09 Aug 2022 17:38:39 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:34:01 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Tue, 09 Aug 2022 18:34:02 GMT
RUN apk add --no-cache libsasl
# Tue, 09 Aug 2022 18:34:03 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 09 Aug 2022 18:34:04 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 09 Aug 2022 18:37:07 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 09 Aug 2022 18:37:09 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 09 Aug 2022 18:37:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 09 Aug 2022 18:37:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 18:37:11 GMT
USER memcache
# Tue, 09 Aug 2022 18:37:12 GMT
EXPOSE 11211
# Tue, 09 Aug 2022 18:37:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6c0d3b419d848ea31ca748254611d5d5ce3b76e3d7bba520fd87400fbb75f3b9`  
		Last Modified: Tue, 09 Aug 2022 17:39:33 GMT  
		Size: 2.8 MB (2807121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:240e236335200614c944d9ba79e2d7eda5cfa258a69e669b585cc28314d754f5`  
		Last Modified: Tue, 09 Aug 2022 18:38:05 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:844d1ba63a22190468423984b12b7d36f6c005e3316461b983f975f4b8dc9ee8`  
		Last Modified: Tue, 09 Aug 2022 18:38:05 GMT  
		Size: 119.8 KB (119826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad6d3cd2261a998624eba6805148058d37a9733e41f66cef88d3b5103170e4a8`  
		Last Modified: Tue, 09 Aug 2022 18:38:06 GMT  
		Size: 962.8 KB (962759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7983bf58c38f033ac9ab3011fd046fa03cb7848d5b2fb86955fd5e20c62e27fc`  
		Last Modified: Tue, 09 Aug 2022 18:38:05 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a108c54c3e573033e837b18319fbbfab59f4bbca1dfd29610c5be85ad2ea1bc9`  
		Last Modified: Tue, 09 Aug 2022 18:38:05 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:d798237b2695cb4cdcde6ad5c5ebeb01b03cb86bd534f5ef703d8b88c3f60db1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3912215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfb1d9b800eeba8d9cadba9dfee6f8b7db71228a7f42e7fd208109e6f8d33a2e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Aug 2022 17:17:09 GMT
ADD file:66b351666e41834033d334aeb3dc6998dea77aa22e8e254028c923fee67a41a8 in / 
# Tue, 09 Aug 2022 17:17:10 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:48:17 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Tue, 09 Aug 2022 18:48:19 GMT
RUN apk add --no-cache libsasl
# Tue, 09 Aug 2022 18:48:19 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 09 Aug 2022 18:48:19 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 09 Aug 2022 18:51:34 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 09 Aug 2022 18:51:34 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 09 Aug 2022 18:51:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 09 Aug 2022 18:51:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 18:51:36 GMT
USER memcache
# Tue, 09 Aug 2022 18:51:36 GMT
EXPOSE 11211
# Tue, 09 Aug 2022 18:51:37 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c79e5d1a8c89b87020a754c8a5c8370faaa37bfb5bca1d8af66770d522ef1caf`  
		Last Modified: Tue, 09 Aug 2022 17:18:26 GMT  
		Size: 2.8 MB (2803320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086c869249c97411ce380e3b76305e0b85731874d0ea57dfd0de74e1f387443d`  
		Last Modified: Tue, 09 Aug 2022 18:52:28 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75e55886182590f2e7eef7f1c21851fd9c322339484e8345afd12376d976ddbd`  
		Last Modified: Tue, 09 Aug 2022 18:52:28 GMT  
		Size: 126.1 KB (126064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5986c4b1340bf1f46f9c87bfe46749c8b2c36b125cc144d44369ffa6da235643`  
		Last Modified: Tue, 09 Aug 2022 18:52:29 GMT  
		Size: 981.2 KB (981160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94057389e17fb62c8067389939b22ba89063219c50a7a348d0343d3aee37d933`  
		Last Modified: Tue, 09 Aug 2022 18:52:28 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989f24ebe1a18ca3cac84b41e1b10934fc83856828b9fb1da76a8d894048512e`  
		Last Modified: Tue, 09 Aug 2022 18:52:28 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:f05c64785454795713f41d5cf814a5debb9cf42c3d4d1b6298ba93d897cfc72a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3646606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef9e9b1c8f1ad73aa6d447c3635fa404bffc5d074a3480ae8644c2ae121a39af`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Aug 2022 17:41:46 GMT
ADD file:b43a065471bc4711415d3c67cd5b6559b0c48ee7ffe9761530477cf457a6dc34 in / 
# Tue, 09 Aug 2022 17:41:46 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 19:11:19 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Tue, 09 Aug 2022 19:11:20 GMT
RUN apk add --no-cache libsasl
# Tue, 09 Aug 2022 19:11:20 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 09 Aug 2022 19:11:20 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 09 Aug 2022 19:14:45 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 09 Aug 2022 19:14:45 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 09 Aug 2022 19:14:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 09 Aug 2022 19:14:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 19:14:46 GMT
USER memcache
# Tue, 09 Aug 2022 19:14:46 GMT
EXPOSE 11211
# Tue, 09 Aug 2022 19:14:46 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:790c84f1f3409eab952345157df7fa804ba6b5f06d4ceb6f2dfa3c6de2064397`  
		Last Modified: Tue, 09 Aug 2022 17:42:45 GMT  
		Size: 2.6 MB (2590597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:463a70f3df946e83a223bd55002470af1b7f8d483babe452e515a809b965d35c`  
		Last Modified: Tue, 09 Aug 2022 19:15:35 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df0b8be6e73cbbdde959ca7a21d3fd6c8e36e05bc9c7a46be4e5bfa5b664a50c`  
		Last Modified: Tue, 09 Aug 2022 19:15:35 GMT  
		Size: 112.5 KB (112508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f39508191d6e035471ed454d54a8ec05b775ff26d4e6902076dd66901c870fd4`  
		Last Modified: Tue, 09 Aug 2022 19:15:35 GMT  
		Size: 941.8 KB (941827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:664e864043941612ce16890523ab6ef1ca3d7a253f0384d99b2e0c3957b6398f`  
		Last Modified: Tue, 09 Aug 2022 19:15:35 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f2ba1910d2ededf72d427c17c6dd473de7acc0ad7513e183ab5c4c3a0c43142`  
		Last Modified: Tue, 09 Aug 2022 19:15:35 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:1-alpine3.16`

```console
$ docker pull memcached@sha256:22fd822b2417986f627bd96bc687e85360200db73e8bc818fe6ffdfe1f24e413
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `memcached:1-alpine3.16` - linux; amd64

```console
$ docker pull memcached@sha256:b1e59612ccc1ab79ccb764e8ae694c89c6e2dece9927b202c1a1820a665268f4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3867486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af3c4fe62d9dafd4336d17fc19dcc8e0ea69a41c4ea586e0544c371319a9497b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:53:39 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Tue, 09 Aug 2022 20:53:40 GMT
RUN apk add --no-cache libsasl
# Tue, 09 Aug 2022 20:53:40 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 09 Aug 2022 20:53:41 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 09 Aug 2022 20:56:30 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 09 Aug 2022 20:56:30 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 09 Aug 2022 20:56:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 09 Aug 2022 20:56:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 20:56:31 GMT
USER memcache
# Tue, 09 Aug 2022 20:56:31 GMT
EXPOSE 11211
# Tue, 09 Aug 2022 20:56:31 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d572ef57cdf8eb58de4b4e89970c5e64c6a2f8470bbbe4746efd56927df10611`  
		Last Modified: Tue, 09 Aug 2022 20:57:08 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed8976416286665206f17c9c2ead879425c6c6c62051fa7af308abd8790c0bc`  
		Last Modified: Tue, 09 Aug 2022 20:57:08 GMT  
		Size: 108.3 KB (108322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c657d873aa5cf9fbc93f3c3b68b8e7543ec1bc6335404b259ea5a7db4196422d`  
		Last Modified: Tue, 09 Aug 2022 20:57:08 GMT  
		Size: 951.4 KB (951438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f91921ed85e235501e9cd091c8d8601f04ea194fe4a461629fe7ab9eb9badd`  
		Last Modified: Tue, 09 Aug 2022 20:57:08 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198a10264961105745cf7038c02c22ae20695d9213c38421ec14d7cc8eda0d44`  
		Last Modified: Tue, 09 Aug 2022 20:57:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine3.16` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:44f0d141458db00ee50b9ad0ec9f39a08f2054fe45924bafddc3920d446727f0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3757682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5799dfb510c6b2e85d9290ef1eae349ba3365b9584932dbc450562979a046d9f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:48:03 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Tue, 09 Aug 2022 20:48:05 GMT
RUN apk add --no-cache libsasl
# Tue, 09 Aug 2022 20:48:05 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 09 Aug 2022 20:48:06 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 09 Aug 2022 20:50:51 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 09 Aug 2022 20:50:53 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 09 Aug 2022 20:50:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 09 Aug 2022 20:50:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 20:50:55 GMT
USER memcache
# Tue, 09 Aug 2022 20:50:56 GMT
EXPOSE 11211
# Tue, 09 Aug 2022 20:50:57 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d15db589ad12df2825238bc4f6832b2c6e3d991704c9b41db7865df5d402276`  
		Last Modified: Tue, 09 Aug 2022 20:51:50 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103b4be7608736e9e24d225ccd97cc4dfad6bacbe7bcf2ca1cd716b45ee32855`  
		Last Modified: Tue, 09 Aug 2022 20:51:50 GMT  
		Size: 109.6 KB (109566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be29d81faebb3b793bdb052326cbb181f786eb99078f62f6f00935c60c14a9fe`  
		Last Modified: Tue, 09 Aug 2022 20:51:50 GMT  
		Size: 938.8 KB (938808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a590dbe104d4e1ec4c488c22500f75e3b44977e09523893500694356ff65008b`  
		Last Modified: Tue, 09 Aug 2022 20:51:50 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da7fd81bf28f2c80e4823f86aea754145c41614f1a924f56f0d2f7e51747873`  
		Last Modified: Tue, 09 Aug 2022 20:51:50 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine3.16` - linux; 386

```console
$ docker pull memcached@sha256:e6fc7462999869fb634dbc73338735811a34ba127cbf512785b2d036132b7496
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3891350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b662b6ea7b7b0638994baa098f88f7a247ecc3da8fa1057e586dd3fdd1fe007`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Aug 2022 17:38:39 GMT
ADD file:b828bc14bc5ff03c8f7310fe0aed6ac5df19a393622d5d1d779a523234d07c0a in / 
# Tue, 09 Aug 2022 17:38:39 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:34:01 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Tue, 09 Aug 2022 18:34:02 GMT
RUN apk add --no-cache libsasl
# Tue, 09 Aug 2022 18:34:03 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 09 Aug 2022 18:34:04 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 09 Aug 2022 18:37:07 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 09 Aug 2022 18:37:09 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 09 Aug 2022 18:37:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 09 Aug 2022 18:37:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 18:37:11 GMT
USER memcache
# Tue, 09 Aug 2022 18:37:12 GMT
EXPOSE 11211
# Tue, 09 Aug 2022 18:37:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6c0d3b419d848ea31ca748254611d5d5ce3b76e3d7bba520fd87400fbb75f3b9`  
		Last Modified: Tue, 09 Aug 2022 17:39:33 GMT  
		Size: 2.8 MB (2807121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:240e236335200614c944d9ba79e2d7eda5cfa258a69e669b585cc28314d754f5`  
		Last Modified: Tue, 09 Aug 2022 18:38:05 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:844d1ba63a22190468423984b12b7d36f6c005e3316461b983f975f4b8dc9ee8`  
		Last Modified: Tue, 09 Aug 2022 18:38:05 GMT  
		Size: 119.8 KB (119826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad6d3cd2261a998624eba6805148058d37a9733e41f66cef88d3b5103170e4a8`  
		Last Modified: Tue, 09 Aug 2022 18:38:06 GMT  
		Size: 962.8 KB (962759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7983bf58c38f033ac9ab3011fd046fa03cb7848d5b2fb86955fd5e20c62e27fc`  
		Last Modified: Tue, 09 Aug 2022 18:38:05 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a108c54c3e573033e837b18319fbbfab59f4bbca1dfd29610c5be85ad2ea1bc9`  
		Last Modified: Tue, 09 Aug 2022 18:38:05 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine3.16` - linux; ppc64le

```console
$ docker pull memcached@sha256:d798237b2695cb4cdcde6ad5c5ebeb01b03cb86bd534f5ef703d8b88c3f60db1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3912215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfb1d9b800eeba8d9cadba9dfee6f8b7db71228a7f42e7fd208109e6f8d33a2e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Aug 2022 17:17:09 GMT
ADD file:66b351666e41834033d334aeb3dc6998dea77aa22e8e254028c923fee67a41a8 in / 
# Tue, 09 Aug 2022 17:17:10 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:48:17 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Tue, 09 Aug 2022 18:48:19 GMT
RUN apk add --no-cache libsasl
# Tue, 09 Aug 2022 18:48:19 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 09 Aug 2022 18:48:19 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 09 Aug 2022 18:51:34 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 09 Aug 2022 18:51:34 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 09 Aug 2022 18:51:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 09 Aug 2022 18:51:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 18:51:36 GMT
USER memcache
# Tue, 09 Aug 2022 18:51:36 GMT
EXPOSE 11211
# Tue, 09 Aug 2022 18:51:37 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c79e5d1a8c89b87020a754c8a5c8370faaa37bfb5bca1d8af66770d522ef1caf`  
		Last Modified: Tue, 09 Aug 2022 17:18:26 GMT  
		Size: 2.8 MB (2803320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086c869249c97411ce380e3b76305e0b85731874d0ea57dfd0de74e1f387443d`  
		Last Modified: Tue, 09 Aug 2022 18:52:28 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75e55886182590f2e7eef7f1c21851fd9c322339484e8345afd12376d976ddbd`  
		Last Modified: Tue, 09 Aug 2022 18:52:28 GMT  
		Size: 126.1 KB (126064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5986c4b1340bf1f46f9c87bfe46749c8b2c36b125cc144d44369ffa6da235643`  
		Last Modified: Tue, 09 Aug 2022 18:52:29 GMT  
		Size: 981.2 KB (981160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94057389e17fb62c8067389939b22ba89063219c50a7a348d0343d3aee37d933`  
		Last Modified: Tue, 09 Aug 2022 18:52:28 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989f24ebe1a18ca3cac84b41e1b10934fc83856828b9fb1da76a8d894048512e`  
		Last Modified: Tue, 09 Aug 2022 18:52:28 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine3.16` - linux; s390x

```console
$ docker pull memcached@sha256:f05c64785454795713f41d5cf814a5debb9cf42c3d4d1b6298ba93d897cfc72a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3646606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef9e9b1c8f1ad73aa6d447c3635fa404bffc5d074a3480ae8644c2ae121a39af`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Aug 2022 17:41:46 GMT
ADD file:b43a065471bc4711415d3c67cd5b6559b0c48ee7ffe9761530477cf457a6dc34 in / 
# Tue, 09 Aug 2022 17:41:46 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 19:11:19 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Tue, 09 Aug 2022 19:11:20 GMT
RUN apk add --no-cache libsasl
# Tue, 09 Aug 2022 19:11:20 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 09 Aug 2022 19:11:20 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 09 Aug 2022 19:14:45 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 09 Aug 2022 19:14:45 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 09 Aug 2022 19:14:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 09 Aug 2022 19:14:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 19:14:46 GMT
USER memcache
# Tue, 09 Aug 2022 19:14:46 GMT
EXPOSE 11211
# Tue, 09 Aug 2022 19:14:46 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:790c84f1f3409eab952345157df7fa804ba6b5f06d4ceb6f2dfa3c6de2064397`  
		Last Modified: Tue, 09 Aug 2022 17:42:45 GMT  
		Size: 2.6 MB (2590597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:463a70f3df946e83a223bd55002470af1b7f8d483babe452e515a809b965d35c`  
		Last Modified: Tue, 09 Aug 2022 19:15:35 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df0b8be6e73cbbdde959ca7a21d3fd6c8e36e05bc9c7a46be4e5bfa5b664a50c`  
		Last Modified: Tue, 09 Aug 2022 19:15:35 GMT  
		Size: 112.5 KB (112508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f39508191d6e035471ed454d54a8ec05b775ff26d4e6902076dd66901c870fd4`  
		Last Modified: Tue, 09 Aug 2022 19:15:35 GMT  
		Size: 941.8 KB (941827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:664e864043941612ce16890523ab6ef1ca3d7a253f0384d99b2e0c3957b6398f`  
		Last Modified: Tue, 09 Aug 2022 19:15:35 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f2ba1910d2ededf72d427c17c6dd473de7acc0ad7513e183ab5c4c3a0c43142`  
		Last Modified: Tue, 09 Aug 2022 19:15:35 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:1-bullseye`

```console
$ docker pull memcached@sha256:22ed710ee778c797865ebff08e825df55df20508075cf275311cca55a235e652
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `memcached:1-bullseye` - linux; amd64

```console
$ docker pull memcached@sha256:a5dc74cbb9f905192c3caa290e32a4c725aba0d21f94c15cd7ca8530ffe01776
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32970763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdff4547b1b7092afe2104dbf710a439a2b8bcdf54b87fbfda0de4631da4ef6a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Aug 2022 00:20:50 GMT
ADD file:7726efb0e0eb5003dbcf2967ec29364479eec8b41f2569ff189372153115b54b in / 
# Tue, 23 Aug 2022 00:20:51 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 02:54:26 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 23 Aug 2022 02:54:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 02:54:30 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 23 Aug 2022 02:54:30 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 23 Aug 2022 02:57:13 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 23 Aug 2022 02:57:13 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 23 Aug 2022 02:57:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 23 Aug 2022 02:57:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 02:57:14 GMT
USER memcache
# Tue, 23 Aug 2022 02:57:14 GMT
EXPOSE 11211
# Tue, 23 Aug 2022 02:57:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7a6db449b51b92eac5c81cdbd82917785343f1664b2be57b22337b0a40c5b29d`  
		Last Modified: Tue, 23 Aug 2022 00:24:59 GMT  
		Size: 31.4 MB (31381485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa73fb65ea8b12a2375459f0d656d3ad06e2863c906fcf962486eda3701f3fd6`  
		Last Modified: Tue, 23 Aug 2022 02:57:38 GMT  
		Size: 5.0 KB (4981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:502b4e8803067b28098d0ea52281cfef66da1ee1e869241612b545d7e9ff12de`  
		Last Modified: Tue, 23 Aug 2022 02:57:38 GMT  
		Size: 328.1 KB (328108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4be7903a0371d25a8e62fb8f58db1b4cc0d71407206895e81b2c5edddd96716`  
		Last Modified: Tue, 23 Aug 2022 02:57:38 GMT  
		Size: 1.3 MB (1255782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ece99ce94967ae22a842630bc182d3052a46922074b332055aa65763b70c4adb`  
		Last Modified: Tue, 23 Aug 2022 02:57:37 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72302fb7547064b5cd2773f9e54e03b6579b64dc8399245d683058505e87860`  
		Last Modified: Tue, 23 Aug 2022 02:57:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-bullseye` - linux; arm variant v5

```console
$ docker pull memcached@sha256:7688ba62a1e2ca12e4fcfc18213eec8b6c8e967bb62395189bdc8d1b095f9ec8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 MB (30466108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63aeac5a0551e3a97aaddf116dbcb2a96b84635664ff3755675a42744590c23c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Aug 2022 01:17:14 GMT
ADD file:83fb076a50e935419eb0db2bd97477d7ed5f16aaac4c8cc35a4a69ac612df327 in / 
# Tue, 23 Aug 2022 01:17:14 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 01:49:29 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 23 Aug 2022 01:49:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 01:49:33 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 23 Aug 2022 01:49:34 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 23 Aug 2022 01:55:05 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 23 Aug 2022 01:55:05 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 23 Aug 2022 01:55:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 23 Aug 2022 01:55:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 01:55:06 GMT
USER memcache
# Tue, 23 Aug 2022 01:55:06 GMT
EXPOSE 11211
# Tue, 23 Aug 2022 01:55:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:74eb5afab626122970f8620ac001fcc4a200725acb05519b85aba47a38bf1016`  
		Last Modified: Tue, 23 Aug 2022 01:22:44 GMT  
		Size: 28.9 MB (28917250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a1b82f1abc9998be67c6dab29a896fcf5377c55fa3c09f0f60355321d0cc7e`  
		Last Modified: Tue, 23 Aug 2022 01:55:43 GMT  
		Size: 4.9 KB (4896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8d24ffcddd09d398cd33e29661cc865588572fdcfc4224b2ea8c0d1d001ed6`  
		Last Modified: Tue, 23 Aug 2022 01:55:44 GMT  
		Size: 316.6 KB (316628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:099cd43abb1475212736fcbb1adbd31b235ae10d1cbd4785e375473e77218967`  
		Last Modified: Tue, 23 Aug 2022 01:55:44 GMT  
		Size: 1.2 MB (1226927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b9006a418f2ced9ced0ca431dda2ce3543860c17742fc092a2309af44e78f22`  
		Last Modified: Tue, 23 Aug 2022 01:55:43 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df94046aab5da41252820ad1cb5d98c7a10c344be39148a95f1d6ad9e052bc1b`  
		Last Modified: Tue, 23 Aug 2022 01:55:44 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-bullseye` - linux; arm variant v7

```console
$ docker pull memcached@sha256:25e768546f1e321b2a9031611f8ecd4081990c82f8774f7e051a5480cf18445d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28076294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5959e4e12e1b75611311d3866bc95f9fe30048418f972e70fa2c671a66149fdd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 02 Aug 2022 00:58:59 GMT
ADD file:1575b776a15adacebc0875642e97a80807d42dcfc8917e1406d47af7ac244c97 in / 
# Tue, 02 Aug 2022 00:58:59 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 06:28:56 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 02 Aug 2022 06:29:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Aug 2022 21:30:08 GMT
ENV MEMCACHED_VERSION=1.6.16
# Thu, 04 Aug 2022 21:30:08 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Thu, 04 Aug 2022 21:36:35 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Thu, 04 Aug 2022 21:36:35 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 04 Aug 2022 21:36:36 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 04 Aug 2022 21:36:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Aug 2022 21:36:37 GMT
USER memcache
# Thu, 04 Aug 2022 21:36:37 GMT
EXPOSE 11211
# Thu, 04 Aug 2022 21:36:37 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1dd75a3a9c893a7dc313f683dd62464b7eab6c6d522ee62c8a17022631830f32`  
		Last Modified: Tue, 02 Aug 2022 01:06:45 GMT  
		Size: 26.6 MB (26560586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44a675a8ce135f198539dc76b078733393238f7c7b899c8635980eed8f35f1cc`  
		Last Modified: Tue, 02 Aug 2022 09:35:13 GMT  
		Size: 4.9 KB (4890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497b0afd04c92a1e5d41f58dbc0d5d544b8880d000c0ffbd03adb48c32c0116b`  
		Last Modified: Tue, 02 Aug 2022 09:35:13 GMT  
		Size: 312.1 KB (312067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8874fe992be272d0e0780725714c2439507699c15bfad1a073df948a34eb668d`  
		Last Modified: Fri, 05 Aug 2022 00:37:30 GMT  
		Size: 1.2 MB (1198344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cd5e042b98c640c152a56816e122c5e7b0abe91535d5d891dceed9748e42129`  
		Last Modified: Fri, 05 Aug 2022 00:37:29 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e871a0f93bdc7cb723e47f45514f914186b73d1890a53cdfe8525dd034926d59`  
		Last Modified: Fri, 05 Aug 2022 00:37:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-bullseye` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:759082b00d406f92781542ce86756eb73c5efe20acc7df6c25ac86be320a3ef5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31433439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e91fe6663d9d90deed07c1d003a80fa6698137267c83310828f24a7ef63f6ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 02 Aug 2022 00:40:38 GMT
ADD file:6039adfbca55ed34a719c37672c664e3524130a0e2a3b8663629b8120b81b790 in / 
# Tue, 02 Aug 2022 00:40:39 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 03:56:15 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 02 Aug 2022 03:56:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Aug 2022 20:33:46 GMT
ENV MEMCACHED_VERSION=1.6.16
# Thu, 04 Aug 2022 20:33:47 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Thu, 04 Aug 2022 20:36:17 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Thu, 04 Aug 2022 20:36:19 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 04 Aug 2022 20:36:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 04 Aug 2022 20:36:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Aug 2022 20:36:21 GMT
USER memcache
# Thu, 04 Aug 2022 20:36:22 GMT
EXPOSE 11211
# Thu, 04 Aug 2022 20:36:23 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a9fe95647e78b5516c7e2327355b6996e2ea295cd76ae242cbfe87f016b4e760`  
		Last Modified: Tue, 02 Aug 2022 00:46:05 GMT  
		Size: 30.1 MB (30054304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b983df009e7dc88033f53f015c09c56fd4db032d1abcade3333d8d4b515ff4af`  
		Last Modified: Tue, 02 Aug 2022 03:59:48 GMT  
		Size: 4.9 KB (4902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60720019405b50af041f391ec7dad90893ee95fc63fd6b3fb9da04850936f5db`  
		Last Modified: Tue, 02 Aug 2022 03:59:48 GMT  
		Size: 119.2 KB (119225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70569bedb4ee539337d6d3fd88e4076a1464b3a77bcfcca6604e18b815dbc402`  
		Last Modified: Thu, 04 Aug 2022 20:40:00 GMT  
		Size: 1.3 MB (1254600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:565112c01ad7b82688180f4fe70f5433126d79cc4b74e3d7f308601e2d34d9fe`  
		Last Modified: Thu, 04 Aug 2022 20:39:59 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce11290eb88924797c1fa048bd052c1243e4cb47e3469b26f3f1a3bc26472d19`  
		Last Modified: Thu, 04 Aug 2022 20:39:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-bullseye` - linux; 386

```console
$ docker pull memcached@sha256:3770f2e3c3f2abb5f85a6a615e62fd5c78a61513ca573ee4385adf42629bd88c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.8 MB (33775724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2804b930e07f367a1e5adc6a5631e87c78a986d3ad64e06e3c549c20ad7ce735`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Aug 2022 01:02:40 GMT
ADD file:5ca62c98116941aaa64ec72afb689a088c46f75a3e83d5b0d4e58d65ec905ccd in / 
# Tue, 23 Aug 2022 01:02:40 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 03:22:44 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 23 Aug 2022 03:22:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 03:22:49 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 23 Aug 2022 03:22:50 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 23 Aug 2022 03:26:54 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 23 Aug 2022 03:26:56 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 23 Aug 2022 03:26:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 23 Aug 2022 03:26:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 03:26:58 GMT
USER memcache
# Tue, 23 Aug 2022 03:26:59 GMT
EXPOSE 11211
# Tue, 23 Aug 2022 03:27:00 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6b3cb4a05a891d9d8a87a2bd7247b16f79832a9d4afbad3ff5068f6fc2ba1560`  
		Last Modified: Tue, 23 Aug 2022 01:08:25 GMT  
		Size: 32.4 MB (32387317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd24201e0b5e9a68a67bdc3b464a01aeb9a2e5a859a582cdaa80ab08a608337`  
		Last Modified: Tue, 23 Aug 2022 03:27:47 GMT  
		Size: 4.8 KB (4774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3070e5e3b1d98fa0b67b8390880b7596c4719b774864de21f36ed86873041793`  
		Last Modified: Tue, 23 Aug 2022 03:27:48 GMT  
		Size: 130.1 KB (130136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a076923bc48ef00816393d79ac2aa3ad931f47309aff7a6cf0c6c74d443080f`  
		Last Modified: Tue, 23 Aug 2022 03:27:48 GMT  
		Size: 1.3 MB (1253091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7169b397a99c6597495d00b3cb6b04483b8950d04bc7cbdcccf983f225294bb4`  
		Last Modified: Tue, 23 Aug 2022 03:27:48 GMT  
		Size: 288.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55ee497fd4fa66154f7c38bc2bb37f6e356318dc032b26ed65eb94ddc8355995`  
		Last Modified: Tue, 23 Aug 2022 03:27:47 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-bullseye` - linux; mips64le

```console
$ docker pull memcached@sha256:0d6798ccd4a9ac44c6ca7c358b2de6bdedbfe104de7d9987eedc68864ab8acc0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 MB (31002934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aca3e1ecca25fb97ad1d376d73b212cad11874d1f051c4c4bac1b2d27abc15fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 02 Aug 2022 01:10:34 GMT
ADD file:6dc22a1e5b5fcf23f2549406ddcc45c4e244f46e21eafa881de81fa87438e5d8 in / 
# Tue, 02 Aug 2022 01:10:38 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 03:22:53 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 02 Aug 2022 03:23:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Aug 2022 20:07:25 GMT
ENV MEMCACHED_VERSION=1.6.16
# Thu, 04 Aug 2022 20:07:28 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Thu, 04 Aug 2022 20:14:28 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Thu, 04 Aug 2022 20:14:30 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 04 Aug 2022 20:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 04 Aug 2022 20:14:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Aug 2022 20:14:40 GMT
USER memcache
# Thu, 04 Aug 2022 20:14:42 GMT
EXPOSE 11211
# Thu, 04 Aug 2022 20:14:45 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:88350749a27614c791450c256b051f023d81cdd256211274b1efac493779d2be`  
		Last Modified: Tue, 02 Aug 2022 01:21:02 GMT  
		Size: 29.6 MB (29628964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:117af7bbaadea9c81bbaa3a8a77b1ab5cd05bcac856c462cda2e81c9a40596ab`  
		Last Modified: Tue, 02 Aug 2022 03:30:45 GMT  
		Size: 4.9 KB (4863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a16d313748bd6b2dade87de73d79edd8a08e4cb662769a717f8587abc8d5e0`  
		Last Modified: Tue, 02 Aug 2022 03:30:46 GMT  
		Size: 117.1 KB (117127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d524786af3243ee367d118f6d5260cffa06d800f492f9b4bb36c910958186933`  
		Last Modified: Thu, 04 Aug 2022 20:15:05 GMT  
		Size: 1.3 MB (1251571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4badb1f1970762d08dbd43d7e101081a5fabd3c45e18afd70636397e83102d2f`  
		Last Modified: Thu, 04 Aug 2022 20:15:04 GMT  
		Size: 288.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3102636392803c3bbff48f39e7f143e3bf9a0528365d63b90dc31cd32060d3e0`  
		Last Modified: Thu, 04 Aug 2022 20:15:04 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-bullseye` - linux; ppc64le

```console
$ docker pull memcached@sha256:6eac50a2d123c021e75657700bdd2d0335dcc97db595e783eb6feaf81e0d6ab0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 MB (36969051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77075f2945ec5e196ccf20148829ebe266a384c2972f723f72361e05e3ee1bf5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Aug 2022 01:24:52 GMT
ADD file:d35213360d726a18e220276d33f245115c3e94a321addaa4c9127488368b0203 in / 
# Tue, 23 Aug 2022 01:24:54 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 02:34:49 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 23 Aug 2022 02:34:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 02:34:56 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 23 Aug 2022 02:34:56 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 23 Aug 2022 02:38:10 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 23 Aug 2022 02:38:10 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 23 Aug 2022 02:38:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 23 Aug 2022 02:38:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 02:38:12 GMT
USER memcache
# Tue, 23 Aug 2022 02:38:12 GMT
EXPOSE 11211
# Tue, 23 Aug 2022 02:38:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:698954eda09d38dd1ccc9ce777b1f6bc7f7473fc6c4c3eb634acc8d035a42eae`  
		Last Modified: Tue, 23 Aug 2022 01:30:36 GMT  
		Size: 35.3 MB (35284280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ffb080d920662043edc67113c0de4c68258ad19c0fffd9e3b79fa01800c6015`  
		Last Modified: Tue, 23 Aug 2022 02:39:09 GMT  
		Size: 5.0 KB (4980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b1f66b68991d8f5ab064b3988db37a48b8f28b4ef0eb8e83efa4c419b630ff`  
		Last Modified: Tue, 23 Aug 2022 02:39:09 GMT  
		Size: 356.9 KB (356931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9653070548c34c29ed693878ef68223dbe9ccefc4653b86d3c8225bc8f85ac1`  
		Last Modified: Tue, 23 Aug 2022 02:39:09 GMT  
		Size: 1.3 MB (1322453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd51b501bab55d128a547f5c14e6410e4ef4b7b08f1867c7c933db716d7791e7`  
		Last Modified: Tue, 23 Aug 2022 02:39:09 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e693f7e8dfc8fe4a2af505658484b885fe097586d4f22c43aaf8278756e76ca`  
		Last Modified: Tue, 23 Aug 2022 02:39:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-bullseye` - linux; s390x

```console
$ docker pull memcached@sha256:4f7e9706bfd16d98bfb48a6435c8359a167ab733777f16f24996cad3f431bdc5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31211398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6739ca31062c74398fdfec102afbacead1c25fa0decf2fa14bdecdcb6b160543`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 02 Aug 2022 00:42:27 GMT
ADD file:c2afc8990930846fbe7c99bfdfe9ea562c75feb6e3c9122431f7c9f8b5e51a7f in / 
# Tue, 02 Aug 2022 00:42:29 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 02:37:02 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 02 Aug 2022 02:37:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Aug 2022 20:28:18 GMT
ENV MEMCACHED_VERSION=1.6.16
# Thu, 04 Aug 2022 20:28:18 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Thu, 04 Aug 2022 20:31:37 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Thu, 04 Aug 2022 20:31:37 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 04 Aug 2022 20:31:37 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 04 Aug 2022 20:31:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Aug 2022 20:31:38 GMT
USER memcache
# Thu, 04 Aug 2022 20:31:38 GMT
EXPOSE 11211
# Thu, 04 Aug 2022 20:31:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:026d311d0716db60eba0572ea784c21031f420960510cebcc383dc53949b4db8`  
		Last Modified: Tue, 02 Aug 2022 00:48:01 GMT  
		Size: 29.6 MB (29640259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0ffdb328e548bd6b6311c78665ac8cd3be8f0b2e09691701d9b0bae0924f8f5`  
		Last Modified: Tue, 02 Aug 2022 02:41:16 GMT  
		Size: 5.0 KB (5025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fbb9677007b0ebab2fe6feab520da1962d3fcffb3490aa844681a46fcb35749`  
		Last Modified: Tue, 02 Aug 2022 02:41:16 GMT  
		Size: 324.2 KB (324183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9c93abfa1f832f2e1f02fbe7b9a489735142c2051dafa7af20d985ff2e2106b`  
		Last Modified: Thu, 04 Aug 2022 20:36:17 GMT  
		Size: 1.2 MB (1241523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f78bf4cf172bedc6ad3c92b859859b10c0394104262328d5664ddc0b1488b29`  
		Last Modified: Thu, 04 Aug 2022 20:36:17 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6a26d2d4c34166613098e1380842f1355b534e2335a1dea2128c193b7f19bec`  
		Last Modified: Thu, 04 Aug 2022 20:36:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:1.6`

```console
$ docker pull memcached@sha256:22ed710ee778c797865ebff08e825df55df20508075cf275311cca55a235e652
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
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
$ docker pull memcached@sha256:a5dc74cbb9f905192c3caa290e32a4c725aba0d21f94c15cd7ca8530ffe01776
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32970763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdff4547b1b7092afe2104dbf710a439a2b8bcdf54b87fbfda0de4631da4ef6a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Aug 2022 00:20:50 GMT
ADD file:7726efb0e0eb5003dbcf2967ec29364479eec8b41f2569ff189372153115b54b in / 
# Tue, 23 Aug 2022 00:20:51 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 02:54:26 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 23 Aug 2022 02:54:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 02:54:30 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 23 Aug 2022 02:54:30 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 23 Aug 2022 02:57:13 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 23 Aug 2022 02:57:13 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 23 Aug 2022 02:57:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 23 Aug 2022 02:57:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 02:57:14 GMT
USER memcache
# Tue, 23 Aug 2022 02:57:14 GMT
EXPOSE 11211
# Tue, 23 Aug 2022 02:57:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7a6db449b51b92eac5c81cdbd82917785343f1664b2be57b22337b0a40c5b29d`  
		Last Modified: Tue, 23 Aug 2022 00:24:59 GMT  
		Size: 31.4 MB (31381485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa73fb65ea8b12a2375459f0d656d3ad06e2863c906fcf962486eda3701f3fd6`  
		Last Modified: Tue, 23 Aug 2022 02:57:38 GMT  
		Size: 5.0 KB (4981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:502b4e8803067b28098d0ea52281cfef66da1ee1e869241612b545d7e9ff12de`  
		Last Modified: Tue, 23 Aug 2022 02:57:38 GMT  
		Size: 328.1 KB (328108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4be7903a0371d25a8e62fb8f58db1b4cc0d71407206895e81b2c5edddd96716`  
		Last Modified: Tue, 23 Aug 2022 02:57:38 GMT  
		Size: 1.3 MB (1255782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ece99ce94967ae22a842630bc182d3052a46922074b332055aa65763b70c4adb`  
		Last Modified: Tue, 23 Aug 2022 02:57:37 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72302fb7547064b5cd2773f9e54e03b6579b64dc8399245d683058505e87860`  
		Last Modified: Tue, 23 Aug 2022 02:57:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6` - linux; arm variant v5

```console
$ docker pull memcached@sha256:7688ba62a1e2ca12e4fcfc18213eec8b6c8e967bb62395189bdc8d1b095f9ec8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 MB (30466108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63aeac5a0551e3a97aaddf116dbcb2a96b84635664ff3755675a42744590c23c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Aug 2022 01:17:14 GMT
ADD file:83fb076a50e935419eb0db2bd97477d7ed5f16aaac4c8cc35a4a69ac612df327 in / 
# Tue, 23 Aug 2022 01:17:14 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 01:49:29 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 23 Aug 2022 01:49:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 01:49:33 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 23 Aug 2022 01:49:34 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 23 Aug 2022 01:55:05 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 23 Aug 2022 01:55:05 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 23 Aug 2022 01:55:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 23 Aug 2022 01:55:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 01:55:06 GMT
USER memcache
# Tue, 23 Aug 2022 01:55:06 GMT
EXPOSE 11211
# Tue, 23 Aug 2022 01:55:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:74eb5afab626122970f8620ac001fcc4a200725acb05519b85aba47a38bf1016`  
		Last Modified: Tue, 23 Aug 2022 01:22:44 GMT  
		Size: 28.9 MB (28917250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a1b82f1abc9998be67c6dab29a896fcf5377c55fa3c09f0f60355321d0cc7e`  
		Last Modified: Tue, 23 Aug 2022 01:55:43 GMT  
		Size: 4.9 KB (4896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8d24ffcddd09d398cd33e29661cc865588572fdcfc4224b2ea8c0d1d001ed6`  
		Last Modified: Tue, 23 Aug 2022 01:55:44 GMT  
		Size: 316.6 KB (316628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:099cd43abb1475212736fcbb1adbd31b235ae10d1cbd4785e375473e77218967`  
		Last Modified: Tue, 23 Aug 2022 01:55:44 GMT  
		Size: 1.2 MB (1226927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b9006a418f2ced9ced0ca431dda2ce3543860c17742fc092a2309af44e78f22`  
		Last Modified: Tue, 23 Aug 2022 01:55:43 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df94046aab5da41252820ad1cb5d98c7a10c344be39148a95f1d6ad9e052bc1b`  
		Last Modified: Tue, 23 Aug 2022 01:55:44 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6` - linux; arm variant v7

```console
$ docker pull memcached@sha256:25e768546f1e321b2a9031611f8ecd4081990c82f8774f7e051a5480cf18445d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28076294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5959e4e12e1b75611311d3866bc95f9fe30048418f972e70fa2c671a66149fdd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 02 Aug 2022 00:58:59 GMT
ADD file:1575b776a15adacebc0875642e97a80807d42dcfc8917e1406d47af7ac244c97 in / 
# Tue, 02 Aug 2022 00:58:59 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 06:28:56 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 02 Aug 2022 06:29:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Aug 2022 21:30:08 GMT
ENV MEMCACHED_VERSION=1.6.16
# Thu, 04 Aug 2022 21:30:08 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Thu, 04 Aug 2022 21:36:35 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Thu, 04 Aug 2022 21:36:35 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 04 Aug 2022 21:36:36 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 04 Aug 2022 21:36:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Aug 2022 21:36:37 GMT
USER memcache
# Thu, 04 Aug 2022 21:36:37 GMT
EXPOSE 11211
# Thu, 04 Aug 2022 21:36:37 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1dd75a3a9c893a7dc313f683dd62464b7eab6c6d522ee62c8a17022631830f32`  
		Last Modified: Tue, 02 Aug 2022 01:06:45 GMT  
		Size: 26.6 MB (26560586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44a675a8ce135f198539dc76b078733393238f7c7b899c8635980eed8f35f1cc`  
		Last Modified: Tue, 02 Aug 2022 09:35:13 GMT  
		Size: 4.9 KB (4890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497b0afd04c92a1e5d41f58dbc0d5d544b8880d000c0ffbd03adb48c32c0116b`  
		Last Modified: Tue, 02 Aug 2022 09:35:13 GMT  
		Size: 312.1 KB (312067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8874fe992be272d0e0780725714c2439507699c15bfad1a073df948a34eb668d`  
		Last Modified: Fri, 05 Aug 2022 00:37:30 GMT  
		Size: 1.2 MB (1198344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cd5e042b98c640c152a56816e122c5e7b0abe91535d5d891dceed9748e42129`  
		Last Modified: Fri, 05 Aug 2022 00:37:29 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e871a0f93bdc7cb723e47f45514f914186b73d1890a53cdfe8525dd034926d59`  
		Last Modified: Fri, 05 Aug 2022 00:37:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:759082b00d406f92781542ce86756eb73c5efe20acc7df6c25ac86be320a3ef5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31433439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e91fe6663d9d90deed07c1d003a80fa6698137267c83310828f24a7ef63f6ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 02 Aug 2022 00:40:38 GMT
ADD file:6039adfbca55ed34a719c37672c664e3524130a0e2a3b8663629b8120b81b790 in / 
# Tue, 02 Aug 2022 00:40:39 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 03:56:15 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 02 Aug 2022 03:56:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Aug 2022 20:33:46 GMT
ENV MEMCACHED_VERSION=1.6.16
# Thu, 04 Aug 2022 20:33:47 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Thu, 04 Aug 2022 20:36:17 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Thu, 04 Aug 2022 20:36:19 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 04 Aug 2022 20:36:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 04 Aug 2022 20:36:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Aug 2022 20:36:21 GMT
USER memcache
# Thu, 04 Aug 2022 20:36:22 GMT
EXPOSE 11211
# Thu, 04 Aug 2022 20:36:23 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a9fe95647e78b5516c7e2327355b6996e2ea295cd76ae242cbfe87f016b4e760`  
		Last Modified: Tue, 02 Aug 2022 00:46:05 GMT  
		Size: 30.1 MB (30054304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b983df009e7dc88033f53f015c09c56fd4db032d1abcade3333d8d4b515ff4af`  
		Last Modified: Tue, 02 Aug 2022 03:59:48 GMT  
		Size: 4.9 KB (4902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60720019405b50af041f391ec7dad90893ee95fc63fd6b3fb9da04850936f5db`  
		Last Modified: Tue, 02 Aug 2022 03:59:48 GMT  
		Size: 119.2 KB (119225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70569bedb4ee539337d6d3fd88e4076a1464b3a77bcfcca6604e18b815dbc402`  
		Last Modified: Thu, 04 Aug 2022 20:40:00 GMT  
		Size: 1.3 MB (1254600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:565112c01ad7b82688180f4fe70f5433126d79cc4b74e3d7f308601e2d34d9fe`  
		Last Modified: Thu, 04 Aug 2022 20:39:59 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce11290eb88924797c1fa048bd052c1243e4cb47e3469b26f3f1a3bc26472d19`  
		Last Modified: Thu, 04 Aug 2022 20:39:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6` - linux; 386

```console
$ docker pull memcached@sha256:3770f2e3c3f2abb5f85a6a615e62fd5c78a61513ca573ee4385adf42629bd88c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.8 MB (33775724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2804b930e07f367a1e5adc6a5631e87c78a986d3ad64e06e3c549c20ad7ce735`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Aug 2022 01:02:40 GMT
ADD file:5ca62c98116941aaa64ec72afb689a088c46f75a3e83d5b0d4e58d65ec905ccd in / 
# Tue, 23 Aug 2022 01:02:40 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 03:22:44 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 23 Aug 2022 03:22:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 03:22:49 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 23 Aug 2022 03:22:50 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 23 Aug 2022 03:26:54 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 23 Aug 2022 03:26:56 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 23 Aug 2022 03:26:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 23 Aug 2022 03:26:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 03:26:58 GMT
USER memcache
# Tue, 23 Aug 2022 03:26:59 GMT
EXPOSE 11211
# Tue, 23 Aug 2022 03:27:00 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6b3cb4a05a891d9d8a87a2bd7247b16f79832a9d4afbad3ff5068f6fc2ba1560`  
		Last Modified: Tue, 23 Aug 2022 01:08:25 GMT  
		Size: 32.4 MB (32387317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd24201e0b5e9a68a67bdc3b464a01aeb9a2e5a859a582cdaa80ab08a608337`  
		Last Modified: Tue, 23 Aug 2022 03:27:47 GMT  
		Size: 4.8 KB (4774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3070e5e3b1d98fa0b67b8390880b7596c4719b774864de21f36ed86873041793`  
		Last Modified: Tue, 23 Aug 2022 03:27:48 GMT  
		Size: 130.1 KB (130136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a076923bc48ef00816393d79ac2aa3ad931f47309aff7a6cf0c6c74d443080f`  
		Last Modified: Tue, 23 Aug 2022 03:27:48 GMT  
		Size: 1.3 MB (1253091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7169b397a99c6597495d00b3cb6b04483b8950d04bc7cbdcccf983f225294bb4`  
		Last Modified: Tue, 23 Aug 2022 03:27:48 GMT  
		Size: 288.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55ee497fd4fa66154f7c38bc2bb37f6e356318dc032b26ed65eb94ddc8355995`  
		Last Modified: Tue, 23 Aug 2022 03:27:47 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6` - linux; mips64le

```console
$ docker pull memcached@sha256:0d6798ccd4a9ac44c6ca7c358b2de6bdedbfe104de7d9987eedc68864ab8acc0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 MB (31002934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aca3e1ecca25fb97ad1d376d73b212cad11874d1f051c4c4bac1b2d27abc15fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 02 Aug 2022 01:10:34 GMT
ADD file:6dc22a1e5b5fcf23f2549406ddcc45c4e244f46e21eafa881de81fa87438e5d8 in / 
# Tue, 02 Aug 2022 01:10:38 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 03:22:53 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 02 Aug 2022 03:23:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Aug 2022 20:07:25 GMT
ENV MEMCACHED_VERSION=1.6.16
# Thu, 04 Aug 2022 20:07:28 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Thu, 04 Aug 2022 20:14:28 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Thu, 04 Aug 2022 20:14:30 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 04 Aug 2022 20:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 04 Aug 2022 20:14:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Aug 2022 20:14:40 GMT
USER memcache
# Thu, 04 Aug 2022 20:14:42 GMT
EXPOSE 11211
# Thu, 04 Aug 2022 20:14:45 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:88350749a27614c791450c256b051f023d81cdd256211274b1efac493779d2be`  
		Last Modified: Tue, 02 Aug 2022 01:21:02 GMT  
		Size: 29.6 MB (29628964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:117af7bbaadea9c81bbaa3a8a77b1ab5cd05bcac856c462cda2e81c9a40596ab`  
		Last Modified: Tue, 02 Aug 2022 03:30:45 GMT  
		Size: 4.9 KB (4863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a16d313748bd6b2dade87de73d79edd8a08e4cb662769a717f8587abc8d5e0`  
		Last Modified: Tue, 02 Aug 2022 03:30:46 GMT  
		Size: 117.1 KB (117127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d524786af3243ee367d118f6d5260cffa06d800f492f9b4bb36c910958186933`  
		Last Modified: Thu, 04 Aug 2022 20:15:05 GMT  
		Size: 1.3 MB (1251571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4badb1f1970762d08dbd43d7e101081a5fabd3c45e18afd70636397e83102d2f`  
		Last Modified: Thu, 04 Aug 2022 20:15:04 GMT  
		Size: 288.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3102636392803c3bbff48f39e7f143e3bf9a0528365d63b90dc31cd32060d3e0`  
		Last Modified: Thu, 04 Aug 2022 20:15:04 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6` - linux; ppc64le

```console
$ docker pull memcached@sha256:6eac50a2d123c021e75657700bdd2d0335dcc97db595e783eb6feaf81e0d6ab0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 MB (36969051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77075f2945ec5e196ccf20148829ebe266a384c2972f723f72361e05e3ee1bf5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Aug 2022 01:24:52 GMT
ADD file:d35213360d726a18e220276d33f245115c3e94a321addaa4c9127488368b0203 in / 
# Tue, 23 Aug 2022 01:24:54 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 02:34:49 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 23 Aug 2022 02:34:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 02:34:56 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 23 Aug 2022 02:34:56 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 23 Aug 2022 02:38:10 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 23 Aug 2022 02:38:10 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 23 Aug 2022 02:38:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 23 Aug 2022 02:38:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 02:38:12 GMT
USER memcache
# Tue, 23 Aug 2022 02:38:12 GMT
EXPOSE 11211
# Tue, 23 Aug 2022 02:38:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:698954eda09d38dd1ccc9ce777b1f6bc7f7473fc6c4c3eb634acc8d035a42eae`  
		Last Modified: Tue, 23 Aug 2022 01:30:36 GMT  
		Size: 35.3 MB (35284280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ffb080d920662043edc67113c0de4c68258ad19c0fffd9e3b79fa01800c6015`  
		Last Modified: Tue, 23 Aug 2022 02:39:09 GMT  
		Size: 5.0 KB (4980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b1f66b68991d8f5ab064b3988db37a48b8f28b4ef0eb8e83efa4c419b630ff`  
		Last Modified: Tue, 23 Aug 2022 02:39:09 GMT  
		Size: 356.9 KB (356931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9653070548c34c29ed693878ef68223dbe9ccefc4653b86d3c8225bc8f85ac1`  
		Last Modified: Tue, 23 Aug 2022 02:39:09 GMT  
		Size: 1.3 MB (1322453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd51b501bab55d128a547f5c14e6410e4ef4b7b08f1867c7c933db716d7791e7`  
		Last Modified: Tue, 23 Aug 2022 02:39:09 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e693f7e8dfc8fe4a2af505658484b885fe097586d4f22c43aaf8278756e76ca`  
		Last Modified: Tue, 23 Aug 2022 02:39:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6` - linux; s390x

```console
$ docker pull memcached@sha256:4f7e9706bfd16d98bfb48a6435c8359a167ab733777f16f24996cad3f431bdc5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31211398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6739ca31062c74398fdfec102afbacead1c25fa0decf2fa14bdecdcb6b160543`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 02 Aug 2022 00:42:27 GMT
ADD file:c2afc8990930846fbe7c99bfdfe9ea562c75feb6e3c9122431f7c9f8b5e51a7f in / 
# Tue, 02 Aug 2022 00:42:29 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 02:37:02 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 02 Aug 2022 02:37:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Aug 2022 20:28:18 GMT
ENV MEMCACHED_VERSION=1.6.16
# Thu, 04 Aug 2022 20:28:18 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Thu, 04 Aug 2022 20:31:37 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Thu, 04 Aug 2022 20:31:37 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 04 Aug 2022 20:31:37 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 04 Aug 2022 20:31:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Aug 2022 20:31:38 GMT
USER memcache
# Thu, 04 Aug 2022 20:31:38 GMT
EXPOSE 11211
# Thu, 04 Aug 2022 20:31:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:026d311d0716db60eba0572ea784c21031f420960510cebcc383dc53949b4db8`  
		Last Modified: Tue, 02 Aug 2022 00:48:01 GMT  
		Size: 29.6 MB (29640259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0ffdb328e548bd6b6311c78665ac8cd3be8f0b2e09691701d9b0bae0924f8f5`  
		Last Modified: Tue, 02 Aug 2022 02:41:16 GMT  
		Size: 5.0 KB (5025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fbb9677007b0ebab2fe6feab520da1962d3fcffb3490aa844681a46fcb35749`  
		Last Modified: Tue, 02 Aug 2022 02:41:16 GMT  
		Size: 324.2 KB (324183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9c93abfa1f832f2e1f02fbe7b9a489735142c2051dafa7af20d985ff2e2106b`  
		Last Modified: Thu, 04 Aug 2022 20:36:17 GMT  
		Size: 1.2 MB (1241523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f78bf4cf172bedc6ad3c92b859859b10c0394104262328d5664ddc0b1488b29`  
		Last Modified: Thu, 04 Aug 2022 20:36:17 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6a26d2d4c34166613098e1380842f1355b534e2335a1dea2128c193b7f19bec`  
		Last Modified: Thu, 04 Aug 2022 20:36:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:1.6-alpine`

```console
$ docker pull memcached@sha256:67a95346c7d0fbe3b1e6d1160cdec386503e0ad7c06e8d4056c3b0754e679eed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `memcached:1.6-alpine` - linux; amd64

```console
$ docker pull memcached@sha256:b1e59612ccc1ab79ccb764e8ae694c89c6e2dece9927b202c1a1820a665268f4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3867486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af3c4fe62d9dafd4336d17fc19dcc8e0ea69a41c4ea586e0544c371319a9497b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:53:39 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Tue, 09 Aug 2022 20:53:40 GMT
RUN apk add --no-cache libsasl
# Tue, 09 Aug 2022 20:53:40 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 09 Aug 2022 20:53:41 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 09 Aug 2022 20:56:30 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 09 Aug 2022 20:56:30 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 09 Aug 2022 20:56:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 09 Aug 2022 20:56:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 20:56:31 GMT
USER memcache
# Tue, 09 Aug 2022 20:56:31 GMT
EXPOSE 11211
# Tue, 09 Aug 2022 20:56:31 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d572ef57cdf8eb58de4b4e89970c5e64c6a2f8470bbbe4746efd56927df10611`  
		Last Modified: Tue, 09 Aug 2022 20:57:08 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed8976416286665206f17c9c2ead879425c6c6c62051fa7af308abd8790c0bc`  
		Last Modified: Tue, 09 Aug 2022 20:57:08 GMT  
		Size: 108.3 KB (108322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c657d873aa5cf9fbc93f3c3b68b8e7543ec1bc6335404b259ea5a7db4196422d`  
		Last Modified: Tue, 09 Aug 2022 20:57:08 GMT  
		Size: 951.4 KB (951438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f91921ed85e235501e9cd091c8d8601f04ea194fe4a461629fe7ab9eb9badd`  
		Last Modified: Tue, 09 Aug 2022 20:57:08 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198a10264961105745cf7038c02c22ae20695d9213c38421ec14d7cc8eda0d44`  
		Last Modified: Tue, 09 Aug 2022 20:57:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6-alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:79a5646a0c845a791f36017fda3292281b48295b06c53f13d62c9f94237d4731
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3960292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2afac0e49af3ce3f1769abe11a29f8f5610c6a736d8c5b6c7b9770c8d8e94e91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 16 Dec 2020 23:58:14 GMT
ADD file:bd07f77a2b2741ca6bda80d9203be9c7274cf73145bff778cf000db0d8d4e903 in / 
# Wed, 16 Dec 2020 23:58:15 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 06:43:29 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Thu, 17 Dec 2020 06:43:31 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Thu, 17 Dec 2020 06:43:33 GMT
ENV MEMCACHED_VERSION=1.6.9
# Thu, 17 Dec 2020 06:43:35 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Thu, 17 Dec 2020 06:46:32 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Thu, 17 Dec 2020 06:46:33 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 17 Dec 2020 06:46:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 17 Dec 2020 06:46:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 06:46:36 GMT
USER memcache
# Thu, 17 Dec 2020 06:46:38 GMT
EXPOSE 11211
# Thu, 17 Dec 2020 06:46:39 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c58e8a26a8407acc3ead776f6526efa889fda03270a8d05109208d9f59159420`  
		Last Modified: Wed, 16 Dec 2020 23:58:59 GMT  
		Size: 2.4 MB (2407555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68564bbfc09f153688e942bf54d5375d1e27f3507c0bed6b038c2ac8ce095aa5`  
		Last Modified: Thu, 17 Dec 2020 06:46:58 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cac3a91edee49d0b08a25706ae86059bed89941a08b496e72ef092e57c4ecb3`  
		Last Modified: Thu, 17 Dec 2020 06:46:58 GMT  
		Size: 13.8 KB (13825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf16e9bb942ec42a35a792beab65aea843209e7bdde7e856499b9fc85f93bc4e`  
		Last Modified: Thu, 17 Dec 2020 06:46:58 GMT  
		Size: 1.5 MB (1537248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc15394239bd0c083e1b6df806aa5ffeb8b9cc7e80113afc2959721de49f90d1`  
		Last Modified: Thu, 17 Dec 2020 06:46:58 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:482f0eb571548eae5720c652ff7da13558e56a8722dc9932cf7eb1ef3eb33acb`  
		Last Modified: Thu, 17 Dec 2020 06:46:58 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:44f0d141458db00ee50b9ad0ec9f39a08f2054fe45924bafddc3920d446727f0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3757682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5799dfb510c6b2e85d9290ef1eae349ba3365b9584932dbc450562979a046d9f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:48:03 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Tue, 09 Aug 2022 20:48:05 GMT
RUN apk add --no-cache libsasl
# Tue, 09 Aug 2022 20:48:05 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 09 Aug 2022 20:48:06 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 09 Aug 2022 20:50:51 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 09 Aug 2022 20:50:53 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 09 Aug 2022 20:50:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 09 Aug 2022 20:50:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 20:50:55 GMT
USER memcache
# Tue, 09 Aug 2022 20:50:56 GMT
EXPOSE 11211
# Tue, 09 Aug 2022 20:50:57 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d15db589ad12df2825238bc4f6832b2c6e3d991704c9b41db7865df5d402276`  
		Last Modified: Tue, 09 Aug 2022 20:51:50 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103b4be7608736e9e24d225ccd97cc4dfad6bacbe7bcf2ca1cd716b45ee32855`  
		Last Modified: Tue, 09 Aug 2022 20:51:50 GMT  
		Size: 109.6 KB (109566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be29d81faebb3b793bdb052326cbb181f786eb99078f62f6f00935c60c14a9fe`  
		Last Modified: Tue, 09 Aug 2022 20:51:50 GMT  
		Size: 938.8 KB (938808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a590dbe104d4e1ec4c488c22500f75e3b44977e09523893500694356ff65008b`  
		Last Modified: Tue, 09 Aug 2022 20:51:50 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da7fd81bf28f2c80e4823f86aea754145c41614f1a924f56f0d2f7e51747873`  
		Last Modified: Tue, 09 Aug 2022 20:51:50 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6-alpine` - linux; 386

```console
$ docker pull memcached@sha256:e6fc7462999869fb634dbc73338735811a34ba127cbf512785b2d036132b7496
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3891350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b662b6ea7b7b0638994baa098f88f7a247ecc3da8fa1057e586dd3fdd1fe007`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Aug 2022 17:38:39 GMT
ADD file:b828bc14bc5ff03c8f7310fe0aed6ac5df19a393622d5d1d779a523234d07c0a in / 
# Tue, 09 Aug 2022 17:38:39 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:34:01 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Tue, 09 Aug 2022 18:34:02 GMT
RUN apk add --no-cache libsasl
# Tue, 09 Aug 2022 18:34:03 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 09 Aug 2022 18:34:04 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 09 Aug 2022 18:37:07 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 09 Aug 2022 18:37:09 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 09 Aug 2022 18:37:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 09 Aug 2022 18:37:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 18:37:11 GMT
USER memcache
# Tue, 09 Aug 2022 18:37:12 GMT
EXPOSE 11211
# Tue, 09 Aug 2022 18:37:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6c0d3b419d848ea31ca748254611d5d5ce3b76e3d7bba520fd87400fbb75f3b9`  
		Last Modified: Tue, 09 Aug 2022 17:39:33 GMT  
		Size: 2.8 MB (2807121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:240e236335200614c944d9ba79e2d7eda5cfa258a69e669b585cc28314d754f5`  
		Last Modified: Tue, 09 Aug 2022 18:38:05 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:844d1ba63a22190468423984b12b7d36f6c005e3316461b983f975f4b8dc9ee8`  
		Last Modified: Tue, 09 Aug 2022 18:38:05 GMT  
		Size: 119.8 KB (119826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad6d3cd2261a998624eba6805148058d37a9733e41f66cef88d3b5103170e4a8`  
		Last Modified: Tue, 09 Aug 2022 18:38:06 GMT  
		Size: 962.8 KB (962759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7983bf58c38f033ac9ab3011fd046fa03cb7848d5b2fb86955fd5e20c62e27fc`  
		Last Modified: Tue, 09 Aug 2022 18:38:05 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a108c54c3e573033e837b18319fbbfab59f4bbca1dfd29610c5be85ad2ea1bc9`  
		Last Modified: Tue, 09 Aug 2022 18:38:05 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:d798237b2695cb4cdcde6ad5c5ebeb01b03cb86bd534f5ef703d8b88c3f60db1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3912215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfb1d9b800eeba8d9cadba9dfee6f8b7db71228a7f42e7fd208109e6f8d33a2e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Aug 2022 17:17:09 GMT
ADD file:66b351666e41834033d334aeb3dc6998dea77aa22e8e254028c923fee67a41a8 in / 
# Tue, 09 Aug 2022 17:17:10 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:48:17 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Tue, 09 Aug 2022 18:48:19 GMT
RUN apk add --no-cache libsasl
# Tue, 09 Aug 2022 18:48:19 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 09 Aug 2022 18:48:19 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 09 Aug 2022 18:51:34 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 09 Aug 2022 18:51:34 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 09 Aug 2022 18:51:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 09 Aug 2022 18:51:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 18:51:36 GMT
USER memcache
# Tue, 09 Aug 2022 18:51:36 GMT
EXPOSE 11211
# Tue, 09 Aug 2022 18:51:37 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c79e5d1a8c89b87020a754c8a5c8370faaa37bfb5bca1d8af66770d522ef1caf`  
		Last Modified: Tue, 09 Aug 2022 17:18:26 GMT  
		Size: 2.8 MB (2803320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086c869249c97411ce380e3b76305e0b85731874d0ea57dfd0de74e1f387443d`  
		Last Modified: Tue, 09 Aug 2022 18:52:28 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75e55886182590f2e7eef7f1c21851fd9c322339484e8345afd12376d976ddbd`  
		Last Modified: Tue, 09 Aug 2022 18:52:28 GMT  
		Size: 126.1 KB (126064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5986c4b1340bf1f46f9c87bfe46749c8b2c36b125cc144d44369ffa6da235643`  
		Last Modified: Tue, 09 Aug 2022 18:52:29 GMT  
		Size: 981.2 KB (981160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94057389e17fb62c8067389939b22ba89063219c50a7a348d0343d3aee37d933`  
		Last Modified: Tue, 09 Aug 2022 18:52:28 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989f24ebe1a18ca3cac84b41e1b10934fc83856828b9fb1da76a8d894048512e`  
		Last Modified: Tue, 09 Aug 2022 18:52:28 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:f05c64785454795713f41d5cf814a5debb9cf42c3d4d1b6298ba93d897cfc72a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3646606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef9e9b1c8f1ad73aa6d447c3635fa404bffc5d074a3480ae8644c2ae121a39af`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Aug 2022 17:41:46 GMT
ADD file:b43a065471bc4711415d3c67cd5b6559b0c48ee7ffe9761530477cf457a6dc34 in / 
# Tue, 09 Aug 2022 17:41:46 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 19:11:19 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Tue, 09 Aug 2022 19:11:20 GMT
RUN apk add --no-cache libsasl
# Tue, 09 Aug 2022 19:11:20 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 09 Aug 2022 19:11:20 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 09 Aug 2022 19:14:45 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 09 Aug 2022 19:14:45 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 09 Aug 2022 19:14:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 09 Aug 2022 19:14:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 19:14:46 GMT
USER memcache
# Tue, 09 Aug 2022 19:14:46 GMT
EXPOSE 11211
# Tue, 09 Aug 2022 19:14:46 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:790c84f1f3409eab952345157df7fa804ba6b5f06d4ceb6f2dfa3c6de2064397`  
		Last Modified: Tue, 09 Aug 2022 17:42:45 GMT  
		Size: 2.6 MB (2590597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:463a70f3df946e83a223bd55002470af1b7f8d483babe452e515a809b965d35c`  
		Last Modified: Tue, 09 Aug 2022 19:15:35 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df0b8be6e73cbbdde959ca7a21d3fd6c8e36e05bc9c7a46be4e5bfa5b664a50c`  
		Last Modified: Tue, 09 Aug 2022 19:15:35 GMT  
		Size: 112.5 KB (112508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f39508191d6e035471ed454d54a8ec05b775ff26d4e6902076dd66901c870fd4`  
		Last Modified: Tue, 09 Aug 2022 19:15:35 GMT  
		Size: 941.8 KB (941827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:664e864043941612ce16890523ab6ef1ca3d7a253f0384d99b2e0c3957b6398f`  
		Last Modified: Tue, 09 Aug 2022 19:15:35 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f2ba1910d2ededf72d427c17c6dd473de7acc0ad7513e183ab5c4c3a0c43142`  
		Last Modified: Tue, 09 Aug 2022 19:15:35 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:1.6-alpine3.16`

```console
$ docker pull memcached@sha256:22fd822b2417986f627bd96bc687e85360200db73e8bc818fe6ffdfe1f24e413
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `memcached:1.6-alpine3.16` - linux; amd64

```console
$ docker pull memcached@sha256:b1e59612ccc1ab79ccb764e8ae694c89c6e2dece9927b202c1a1820a665268f4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3867486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af3c4fe62d9dafd4336d17fc19dcc8e0ea69a41c4ea586e0544c371319a9497b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:53:39 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Tue, 09 Aug 2022 20:53:40 GMT
RUN apk add --no-cache libsasl
# Tue, 09 Aug 2022 20:53:40 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 09 Aug 2022 20:53:41 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 09 Aug 2022 20:56:30 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 09 Aug 2022 20:56:30 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 09 Aug 2022 20:56:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 09 Aug 2022 20:56:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 20:56:31 GMT
USER memcache
# Tue, 09 Aug 2022 20:56:31 GMT
EXPOSE 11211
# Tue, 09 Aug 2022 20:56:31 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d572ef57cdf8eb58de4b4e89970c5e64c6a2f8470bbbe4746efd56927df10611`  
		Last Modified: Tue, 09 Aug 2022 20:57:08 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed8976416286665206f17c9c2ead879425c6c6c62051fa7af308abd8790c0bc`  
		Last Modified: Tue, 09 Aug 2022 20:57:08 GMT  
		Size: 108.3 KB (108322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c657d873aa5cf9fbc93f3c3b68b8e7543ec1bc6335404b259ea5a7db4196422d`  
		Last Modified: Tue, 09 Aug 2022 20:57:08 GMT  
		Size: 951.4 KB (951438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f91921ed85e235501e9cd091c8d8601f04ea194fe4a461629fe7ab9eb9badd`  
		Last Modified: Tue, 09 Aug 2022 20:57:08 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198a10264961105745cf7038c02c22ae20695d9213c38421ec14d7cc8eda0d44`  
		Last Modified: Tue, 09 Aug 2022 20:57:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6-alpine3.16` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:44f0d141458db00ee50b9ad0ec9f39a08f2054fe45924bafddc3920d446727f0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3757682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5799dfb510c6b2e85d9290ef1eae349ba3365b9584932dbc450562979a046d9f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:48:03 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Tue, 09 Aug 2022 20:48:05 GMT
RUN apk add --no-cache libsasl
# Tue, 09 Aug 2022 20:48:05 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 09 Aug 2022 20:48:06 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 09 Aug 2022 20:50:51 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 09 Aug 2022 20:50:53 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 09 Aug 2022 20:50:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 09 Aug 2022 20:50:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 20:50:55 GMT
USER memcache
# Tue, 09 Aug 2022 20:50:56 GMT
EXPOSE 11211
# Tue, 09 Aug 2022 20:50:57 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d15db589ad12df2825238bc4f6832b2c6e3d991704c9b41db7865df5d402276`  
		Last Modified: Tue, 09 Aug 2022 20:51:50 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103b4be7608736e9e24d225ccd97cc4dfad6bacbe7bcf2ca1cd716b45ee32855`  
		Last Modified: Tue, 09 Aug 2022 20:51:50 GMT  
		Size: 109.6 KB (109566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be29d81faebb3b793bdb052326cbb181f786eb99078f62f6f00935c60c14a9fe`  
		Last Modified: Tue, 09 Aug 2022 20:51:50 GMT  
		Size: 938.8 KB (938808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a590dbe104d4e1ec4c488c22500f75e3b44977e09523893500694356ff65008b`  
		Last Modified: Tue, 09 Aug 2022 20:51:50 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da7fd81bf28f2c80e4823f86aea754145c41614f1a924f56f0d2f7e51747873`  
		Last Modified: Tue, 09 Aug 2022 20:51:50 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6-alpine3.16` - linux; 386

```console
$ docker pull memcached@sha256:e6fc7462999869fb634dbc73338735811a34ba127cbf512785b2d036132b7496
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3891350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b662b6ea7b7b0638994baa098f88f7a247ecc3da8fa1057e586dd3fdd1fe007`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Aug 2022 17:38:39 GMT
ADD file:b828bc14bc5ff03c8f7310fe0aed6ac5df19a393622d5d1d779a523234d07c0a in / 
# Tue, 09 Aug 2022 17:38:39 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:34:01 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Tue, 09 Aug 2022 18:34:02 GMT
RUN apk add --no-cache libsasl
# Tue, 09 Aug 2022 18:34:03 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 09 Aug 2022 18:34:04 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 09 Aug 2022 18:37:07 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 09 Aug 2022 18:37:09 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 09 Aug 2022 18:37:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 09 Aug 2022 18:37:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 18:37:11 GMT
USER memcache
# Tue, 09 Aug 2022 18:37:12 GMT
EXPOSE 11211
# Tue, 09 Aug 2022 18:37:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6c0d3b419d848ea31ca748254611d5d5ce3b76e3d7bba520fd87400fbb75f3b9`  
		Last Modified: Tue, 09 Aug 2022 17:39:33 GMT  
		Size: 2.8 MB (2807121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:240e236335200614c944d9ba79e2d7eda5cfa258a69e669b585cc28314d754f5`  
		Last Modified: Tue, 09 Aug 2022 18:38:05 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:844d1ba63a22190468423984b12b7d36f6c005e3316461b983f975f4b8dc9ee8`  
		Last Modified: Tue, 09 Aug 2022 18:38:05 GMT  
		Size: 119.8 KB (119826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad6d3cd2261a998624eba6805148058d37a9733e41f66cef88d3b5103170e4a8`  
		Last Modified: Tue, 09 Aug 2022 18:38:06 GMT  
		Size: 962.8 KB (962759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7983bf58c38f033ac9ab3011fd046fa03cb7848d5b2fb86955fd5e20c62e27fc`  
		Last Modified: Tue, 09 Aug 2022 18:38:05 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a108c54c3e573033e837b18319fbbfab59f4bbca1dfd29610c5be85ad2ea1bc9`  
		Last Modified: Tue, 09 Aug 2022 18:38:05 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6-alpine3.16` - linux; ppc64le

```console
$ docker pull memcached@sha256:d798237b2695cb4cdcde6ad5c5ebeb01b03cb86bd534f5ef703d8b88c3f60db1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3912215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfb1d9b800eeba8d9cadba9dfee6f8b7db71228a7f42e7fd208109e6f8d33a2e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Aug 2022 17:17:09 GMT
ADD file:66b351666e41834033d334aeb3dc6998dea77aa22e8e254028c923fee67a41a8 in / 
# Tue, 09 Aug 2022 17:17:10 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:48:17 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Tue, 09 Aug 2022 18:48:19 GMT
RUN apk add --no-cache libsasl
# Tue, 09 Aug 2022 18:48:19 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 09 Aug 2022 18:48:19 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 09 Aug 2022 18:51:34 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 09 Aug 2022 18:51:34 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 09 Aug 2022 18:51:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 09 Aug 2022 18:51:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 18:51:36 GMT
USER memcache
# Tue, 09 Aug 2022 18:51:36 GMT
EXPOSE 11211
# Tue, 09 Aug 2022 18:51:37 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c79e5d1a8c89b87020a754c8a5c8370faaa37bfb5bca1d8af66770d522ef1caf`  
		Last Modified: Tue, 09 Aug 2022 17:18:26 GMT  
		Size: 2.8 MB (2803320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086c869249c97411ce380e3b76305e0b85731874d0ea57dfd0de74e1f387443d`  
		Last Modified: Tue, 09 Aug 2022 18:52:28 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75e55886182590f2e7eef7f1c21851fd9c322339484e8345afd12376d976ddbd`  
		Last Modified: Tue, 09 Aug 2022 18:52:28 GMT  
		Size: 126.1 KB (126064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5986c4b1340bf1f46f9c87bfe46749c8b2c36b125cc144d44369ffa6da235643`  
		Last Modified: Tue, 09 Aug 2022 18:52:29 GMT  
		Size: 981.2 KB (981160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94057389e17fb62c8067389939b22ba89063219c50a7a348d0343d3aee37d933`  
		Last Modified: Tue, 09 Aug 2022 18:52:28 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989f24ebe1a18ca3cac84b41e1b10934fc83856828b9fb1da76a8d894048512e`  
		Last Modified: Tue, 09 Aug 2022 18:52:28 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6-alpine3.16` - linux; s390x

```console
$ docker pull memcached@sha256:f05c64785454795713f41d5cf814a5debb9cf42c3d4d1b6298ba93d897cfc72a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3646606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef9e9b1c8f1ad73aa6d447c3635fa404bffc5d074a3480ae8644c2ae121a39af`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Aug 2022 17:41:46 GMT
ADD file:b43a065471bc4711415d3c67cd5b6559b0c48ee7ffe9761530477cf457a6dc34 in / 
# Tue, 09 Aug 2022 17:41:46 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 19:11:19 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Tue, 09 Aug 2022 19:11:20 GMT
RUN apk add --no-cache libsasl
# Tue, 09 Aug 2022 19:11:20 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 09 Aug 2022 19:11:20 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 09 Aug 2022 19:14:45 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 09 Aug 2022 19:14:45 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 09 Aug 2022 19:14:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 09 Aug 2022 19:14:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 19:14:46 GMT
USER memcache
# Tue, 09 Aug 2022 19:14:46 GMT
EXPOSE 11211
# Tue, 09 Aug 2022 19:14:46 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:790c84f1f3409eab952345157df7fa804ba6b5f06d4ceb6f2dfa3c6de2064397`  
		Last Modified: Tue, 09 Aug 2022 17:42:45 GMT  
		Size: 2.6 MB (2590597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:463a70f3df946e83a223bd55002470af1b7f8d483babe452e515a809b965d35c`  
		Last Modified: Tue, 09 Aug 2022 19:15:35 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df0b8be6e73cbbdde959ca7a21d3fd6c8e36e05bc9c7a46be4e5bfa5b664a50c`  
		Last Modified: Tue, 09 Aug 2022 19:15:35 GMT  
		Size: 112.5 KB (112508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f39508191d6e035471ed454d54a8ec05b775ff26d4e6902076dd66901c870fd4`  
		Last Modified: Tue, 09 Aug 2022 19:15:35 GMT  
		Size: 941.8 KB (941827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:664e864043941612ce16890523ab6ef1ca3d7a253f0384d99b2e0c3957b6398f`  
		Last Modified: Tue, 09 Aug 2022 19:15:35 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f2ba1910d2ededf72d427c17c6dd473de7acc0ad7513e183ab5c4c3a0c43142`  
		Last Modified: Tue, 09 Aug 2022 19:15:35 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:1.6-bullseye`

```console
$ docker pull memcached@sha256:22ed710ee778c797865ebff08e825df55df20508075cf275311cca55a235e652
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `memcached:1.6-bullseye` - linux; amd64

```console
$ docker pull memcached@sha256:a5dc74cbb9f905192c3caa290e32a4c725aba0d21f94c15cd7ca8530ffe01776
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32970763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdff4547b1b7092afe2104dbf710a439a2b8bcdf54b87fbfda0de4631da4ef6a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Aug 2022 00:20:50 GMT
ADD file:7726efb0e0eb5003dbcf2967ec29364479eec8b41f2569ff189372153115b54b in / 
# Tue, 23 Aug 2022 00:20:51 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 02:54:26 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 23 Aug 2022 02:54:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 02:54:30 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 23 Aug 2022 02:54:30 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 23 Aug 2022 02:57:13 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 23 Aug 2022 02:57:13 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 23 Aug 2022 02:57:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 23 Aug 2022 02:57:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 02:57:14 GMT
USER memcache
# Tue, 23 Aug 2022 02:57:14 GMT
EXPOSE 11211
# Tue, 23 Aug 2022 02:57:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7a6db449b51b92eac5c81cdbd82917785343f1664b2be57b22337b0a40c5b29d`  
		Last Modified: Tue, 23 Aug 2022 00:24:59 GMT  
		Size: 31.4 MB (31381485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa73fb65ea8b12a2375459f0d656d3ad06e2863c906fcf962486eda3701f3fd6`  
		Last Modified: Tue, 23 Aug 2022 02:57:38 GMT  
		Size: 5.0 KB (4981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:502b4e8803067b28098d0ea52281cfef66da1ee1e869241612b545d7e9ff12de`  
		Last Modified: Tue, 23 Aug 2022 02:57:38 GMT  
		Size: 328.1 KB (328108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4be7903a0371d25a8e62fb8f58db1b4cc0d71407206895e81b2c5edddd96716`  
		Last Modified: Tue, 23 Aug 2022 02:57:38 GMT  
		Size: 1.3 MB (1255782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ece99ce94967ae22a842630bc182d3052a46922074b332055aa65763b70c4adb`  
		Last Modified: Tue, 23 Aug 2022 02:57:37 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72302fb7547064b5cd2773f9e54e03b6579b64dc8399245d683058505e87860`  
		Last Modified: Tue, 23 Aug 2022 02:57:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6-bullseye` - linux; arm variant v5

```console
$ docker pull memcached@sha256:7688ba62a1e2ca12e4fcfc18213eec8b6c8e967bb62395189bdc8d1b095f9ec8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 MB (30466108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63aeac5a0551e3a97aaddf116dbcb2a96b84635664ff3755675a42744590c23c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Aug 2022 01:17:14 GMT
ADD file:83fb076a50e935419eb0db2bd97477d7ed5f16aaac4c8cc35a4a69ac612df327 in / 
# Tue, 23 Aug 2022 01:17:14 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 01:49:29 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 23 Aug 2022 01:49:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 01:49:33 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 23 Aug 2022 01:49:34 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 23 Aug 2022 01:55:05 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 23 Aug 2022 01:55:05 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 23 Aug 2022 01:55:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 23 Aug 2022 01:55:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 01:55:06 GMT
USER memcache
# Tue, 23 Aug 2022 01:55:06 GMT
EXPOSE 11211
# Tue, 23 Aug 2022 01:55:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:74eb5afab626122970f8620ac001fcc4a200725acb05519b85aba47a38bf1016`  
		Last Modified: Tue, 23 Aug 2022 01:22:44 GMT  
		Size: 28.9 MB (28917250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a1b82f1abc9998be67c6dab29a896fcf5377c55fa3c09f0f60355321d0cc7e`  
		Last Modified: Tue, 23 Aug 2022 01:55:43 GMT  
		Size: 4.9 KB (4896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8d24ffcddd09d398cd33e29661cc865588572fdcfc4224b2ea8c0d1d001ed6`  
		Last Modified: Tue, 23 Aug 2022 01:55:44 GMT  
		Size: 316.6 KB (316628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:099cd43abb1475212736fcbb1adbd31b235ae10d1cbd4785e375473e77218967`  
		Last Modified: Tue, 23 Aug 2022 01:55:44 GMT  
		Size: 1.2 MB (1226927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b9006a418f2ced9ced0ca431dda2ce3543860c17742fc092a2309af44e78f22`  
		Last Modified: Tue, 23 Aug 2022 01:55:43 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df94046aab5da41252820ad1cb5d98c7a10c344be39148a95f1d6ad9e052bc1b`  
		Last Modified: Tue, 23 Aug 2022 01:55:44 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6-bullseye` - linux; arm variant v7

```console
$ docker pull memcached@sha256:25e768546f1e321b2a9031611f8ecd4081990c82f8774f7e051a5480cf18445d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28076294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5959e4e12e1b75611311d3866bc95f9fe30048418f972e70fa2c671a66149fdd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 02 Aug 2022 00:58:59 GMT
ADD file:1575b776a15adacebc0875642e97a80807d42dcfc8917e1406d47af7ac244c97 in / 
# Tue, 02 Aug 2022 00:58:59 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 06:28:56 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 02 Aug 2022 06:29:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Aug 2022 21:30:08 GMT
ENV MEMCACHED_VERSION=1.6.16
# Thu, 04 Aug 2022 21:30:08 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Thu, 04 Aug 2022 21:36:35 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Thu, 04 Aug 2022 21:36:35 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 04 Aug 2022 21:36:36 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 04 Aug 2022 21:36:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Aug 2022 21:36:37 GMT
USER memcache
# Thu, 04 Aug 2022 21:36:37 GMT
EXPOSE 11211
# Thu, 04 Aug 2022 21:36:37 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1dd75a3a9c893a7dc313f683dd62464b7eab6c6d522ee62c8a17022631830f32`  
		Last Modified: Tue, 02 Aug 2022 01:06:45 GMT  
		Size: 26.6 MB (26560586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44a675a8ce135f198539dc76b078733393238f7c7b899c8635980eed8f35f1cc`  
		Last Modified: Tue, 02 Aug 2022 09:35:13 GMT  
		Size: 4.9 KB (4890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497b0afd04c92a1e5d41f58dbc0d5d544b8880d000c0ffbd03adb48c32c0116b`  
		Last Modified: Tue, 02 Aug 2022 09:35:13 GMT  
		Size: 312.1 KB (312067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8874fe992be272d0e0780725714c2439507699c15bfad1a073df948a34eb668d`  
		Last Modified: Fri, 05 Aug 2022 00:37:30 GMT  
		Size: 1.2 MB (1198344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cd5e042b98c640c152a56816e122c5e7b0abe91535d5d891dceed9748e42129`  
		Last Modified: Fri, 05 Aug 2022 00:37:29 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e871a0f93bdc7cb723e47f45514f914186b73d1890a53cdfe8525dd034926d59`  
		Last Modified: Fri, 05 Aug 2022 00:37:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6-bullseye` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:759082b00d406f92781542ce86756eb73c5efe20acc7df6c25ac86be320a3ef5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31433439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e91fe6663d9d90deed07c1d003a80fa6698137267c83310828f24a7ef63f6ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 02 Aug 2022 00:40:38 GMT
ADD file:6039adfbca55ed34a719c37672c664e3524130a0e2a3b8663629b8120b81b790 in / 
# Tue, 02 Aug 2022 00:40:39 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 03:56:15 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 02 Aug 2022 03:56:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Aug 2022 20:33:46 GMT
ENV MEMCACHED_VERSION=1.6.16
# Thu, 04 Aug 2022 20:33:47 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Thu, 04 Aug 2022 20:36:17 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Thu, 04 Aug 2022 20:36:19 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 04 Aug 2022 20:36:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 04 Aug 2022 20:36:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Aug 2022 20:36:21 GMT
USER memcache
# Thu, 04 Aug 2022 20:36:22 GMT
EXPOSE 11211
# Thu, 04 Aug 2022 20:36:23 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a9fe95647e78b5516c7e2327355b6996e2ea295cd76ae242cbfe87f016b4e760`  
		Last Modified: Tue, 02 Aug 2022 00:46:05 GMT  
		Size: 30.1 MB (30054304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b983df009e7dc88033f53f015c09c56fd4db032d1abcade3333d8d4b515ff4af`  
		Last Modified: Tue, 02 Aug 2022 03:59:48 GMT  
		Size: 4.9 KB (4902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60720019405b50af041f391ec7dad90893ee95fc63fd6b3fb9da04850936f5db`  
		Last Modified: Tue, 02 Aug 2022 03:59:48 GMT  
		Size: 119.2 KB (119225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70569bedb4ee539337d6d3fd88e4076a1464b3a77bcfcca6604e18b815dbc402`  
		Last Modified: Thu, 04 Aug 2022 20:40:00 GMT  
		Size: 1.3 MB (1254600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:565112c01ad7b82688180f4fe70f5433126d79cc4b74e3d7f308601e2d34d9fe`  
		Last Modified: Thu, 04 Aug 2022 20:39:59 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce11290eb88924797c1fa048bd052c1243e4cb47e3469b26f3f1a3bc26472d19`  
		Last Modified: Thu, 04 Aug 2022 20:39:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6-bullseye` - linux; 386

```console
$ docker pull memcached@sha256:3770f2e3c3f2abb5f85a6a615e62fd5c78a61513ca573ee4385adf42629bd88c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.8 MB (33775724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2804b930e07f367a1e5adc6a5631e87c78a986d3ad64e06e3c549c20ad7ce735`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Aug 2022 01:02:40 GMT
ADD file:5ca62c98116941aaa64ec72afb689a088c46f75a3e83d5b0d4e58d65ec905ccd in / 
# Tue, 23 Aug 2022 01:02:40 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 03:22:44 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 23 Aug 2022 03:22:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 03:22:49 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 23 Aug 2022 03:22:50 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 23 Aug 2022 03:26:54 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 23 Aug 2022 03:26:56 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 23 Aug 2022 03:26:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 23 Aug 2022 03:26:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 03:26:58 GMT
USER memcache
# Tue, 23 Aug 2022 03:26:59 GMT
EXPOSE 11211
# Tue, 23 Aug 2022 03:27:00 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6b3cb4a05a891d9d8a87a2bd7247b16f79832a9d4afbad3ff5068f6fc2ba1560`  
		Last Modified: Tue, 23 Aug 2022 01:08:25 GMT  
		Size: 32.4 MB (32387317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd24201e0b5e9a68a67bdc3b464a01aeb9a2e5a859a582cdaa80ab08a608337`  
		Last Modified: Tue, 23 Aug 2022 03:27:47 GMT  
		Size: 4.8 KB (4774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3070e5e3b1d98fa0b67b8390880b7596c4719b774864de21f36ed86873041793`  
		Last Modified: Tue, 23 Aug 2022 03:27:48 GMT  
		Size: 130.1 KB (130136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a076923bc48ef00816393d79ac2aa3ad931f47309aff7a6cf0c6c74d443080f`  
		Last Modified: Tue, 23 Aug 2022 03:27:48 GMT  
		Size: 1.3 MB (1253091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7169b397a99c6597495d00b3cb6b04483b8950d04bc7cbdcccf983f225294bb4`  
		Last Modified: Tue, 23 Aug 2022 03:27:48 GMT  
		Size: 288.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55ee497fd4fa66154f7c38bc2bb37f6e356318dc032b26ed65eb94ddc8355995`  
		Last Modified: Tue, 23 Aug 2022 03:27:47 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6-bullseye` - linux; mips64le

```console
$ docker pull memcached@sha256:0d6798ccd4a9ac44c6ca7c358b2de6bdedbfe104de7d9987eedc68864ab8acc0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 MB (31002934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aca3e1ecca25fb97ad1d376d73b212cad11874d1f051c4c4bac1b2d27abc15fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 02 Aug 2022 01:10:34 GMT
ADD file:6dc22a1e5b5fcf23f2549406ddcc45c4e244f46e21eafa881de81fa87438e5d8 in / 
# Tue, 02 Aug 2022 01:10:38 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 03:22:53 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 02 Aug 2022 03:23:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Aug 2022 20:07:25 GMT
ENV MEMCACHED_VERSION=1.6.16
# Thu, 04 Aug 2022 20:07:28 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Thu, 04 Aug 2022 20:14:28 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Thu, 04 Aug 2022 20:14:30 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 04 Aug 2022 20:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 04 Aug 2022 20:14:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Aug 2022 20:14:40 GMT
USER memcache
# Thu, 04 Aug 2022 20:14:42 GMT
EXPOSE 11211
# Thu, 04 Aug 2022 20:14:45 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:88350749a27614c791450c256b051f023d81cdd256211274b1efac493779d2be`  
		Last Modified: Tue, 02 Aug 2022 01:21:02 GMT  
		Size: 29.6 MB (29628964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:117af7bbaadea9c81bbaa3a8a77b1ab5cd05bcac856c462cda2e81c9a40596ab`  
		Last Modified: Tue, 02 Aug 2022 03:30:45 GMT  
		Size: 4.9 KB (4863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a16d313748bd6b2dade87de73d79edd8a08e4cb662769a717f8587abc8d5e0`  
		Last Modified: Tue, 02 Aug 2022 03:30:46 GMT  
		Size: 117.1 KB (117127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d524786af3243ee367d118f6d5260cffa06d800f492f9b4bb36c910958186933`  
		Last Modified: Thu, 04 Aug 2022 20:15:05 GMT  
		Size: 1.3 MB (1251571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4badb1f1970762d08dbd43d7e101081a5fabd3c45e18afd70636397e83102d2f`  
		Last Modified: Thu, 04 Aug 2022 20:15:04 GMT  
		Size: 288.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3102636392803c3bbff48f39e7f143e3bf9a0528365d63b90dc31cd32060d3e0`  
		Last Modified: Thu, 04 Aug 2022 20:15:04 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6-bullseye` - linux; ppc64le

```console
$ docker pull memcached@sha256:6eac50a2d123c021e75657700bdd2d0335dcc97db595e783eb6feaf81e0d6ab0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 MB (36969051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77075f2945ec5e196ccf20148829ebe266a384c2972f723f72361e05e3ee1bf5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Aug 2022 01:24:52 GMT
ADD file:d35213360d726a18e220276d33f245115c3e94a321addaa4c9127488368b0203 in / 
# Tue, 23 Aug 2022 01:24:54 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 02:34:49 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 23 Aug 2022 02:34:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 02:34:56 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 23 Aug 2022 02:34:56 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 23 Aug 2022 02:38:10 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 23 Aug 2022 02:38:10 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 23 Aug 2022 02:38:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 23 Aug 2022 02:38:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 02:38:12 GMT
USER memcache
# Tue, 23 Aug 2022 02:38:12 GMT
EXPOSE 11211
# Tue, 23 Aug 2022 02:38:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:698954eda09d38dd1ccc9ce777b1f6bc7f7473fc6c4c3eb634acc8d035a42eae`  
		Last Modified: Tue, 23 Aug 2022 01:30:36 GMT  
		Size: 35.3 MB (35284280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ffb080d920662043edc67113c0de4c68258ad19c0fffd9e3b79fa01800c6015`  
		Last Modified: Tue, 23 Aug 2022 02:39:09 GMT  
		Size: 5.0 KB (4980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b1f66b68991d8f5ab064b3988db37a48b8f28b4ef0eb8e83efa4c419b630ff`  
		Last Modified: Tue, 23 Aug 2022 02:39:09 GMT  
		Size: 356.9 KB (356931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9653070548c34c29ed693878ef68223dbe9ccefc4653b86d3c8225bc8f85ac1`  
		Last Modified: Tue, 23 Aug 2022 02:39:09 GMT  
		Size: 1.3 MB (1322453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd51b501bab55d128a547f5c14e6410e4ef4b7b08f1867c7c933db716d7791e7`  
		Last Modified: Tue, 23 Aug 2022 02:39:09 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e693f7e8dfc8fe4a2af505658484b885fe097586d4f22c43aaf8278756e76ca`  
		Last Modified: Tue, 23 Aug 2022 02:39:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6-bullseye` - linux; s390x

```console
$ docker pull memcached@sha256:4f7e9706bfd16d98bfb48a6435c8359a167ab733777f16f24996cad3f431bdc5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31211398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6739ca31062c74398fdfec102afbacead1c25fa0decf2fa14bdecdcb6b160543`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 02 Aug 2022 00:42:27 GMT
ADD file:c2afc8990930846fbe7c99bfdfe9ea562c75feb6e3c9122431f7c9f8b5e51a7f in / 
# Tue, 02 Aug 2022 00:42:29 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 02:37:02 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 02 Aug 2022 02:37:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Aug 2022 20:28:18 GMT
ENV MEMCACHED_VERSION=1.6.16
# Thu, 04 Aug 2022 20:28:18 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Thu, 04 Aug 2022 20:31:37 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Thu, 04 Aug 2022 20:31:37 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 04 Aug 2022 20:31:37 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 04 Aug 2022 20:31:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Aug 2022 20:31:38 GMT
USER memcache
# Thu, 04 Aug 2022 20:31:38 GMT
EXPOSE 11211
# Thu, 04 Aug 2022 20:31:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:026d311d0716db60eba0572ea784c21031f420960510cebcc383dc53949b4db8`  
		Last Modified: Tue, 02 Aug 2022 00:48:01 GMT  
		Size: 29.6 MB (29640259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0ffdb328e548bd6b6311c78665ac8cd3be8f0b2e09691701d9b0bae0924f8f5`  
		Last Modified: Tue, 02 Aug 2022 02:41:16 GMT  
		Size: 5.0 KB (5025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fbb9677007b0ebab2fe6feab520da1962d3fcffb3490aa844681a46fcb35749`  
		Last Modified: Tue, 02 Aug 2022 02:41:16 GMT  
		Size: 324.2 KB (324183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9c93abfa1f832f2e1f02fbe7b9a489735142c2051dafa7af20d985ff2e2106b`  
		Last Modified: Thu, 04 Aug 2022 20:36:17 GMT  
		Size: 1.2 MB (1241523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f78bf4cf172bedc6ad3c92b859859b10c0394104262328d5664ddc0b1488b29`  
		Last Modified: Thu, 04 Aug 2022 20:36:17 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6a26d2d4c34166613098e1380842f1355b534e2335a1dea2128c193b7f19bec`  
		Last Modified: Thu, 04 Aug 2022 20:36:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:1.6.16`

```console
$ docker pull memcached@sha256:22ed710ee778c797865ebff08e825df55df20508075cf275311cca55a235e652
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `memcached:1.6.16` - linux; amd64

```console
$ docker pull memcached@sha256:a5dc74cbb9f905192c3caa290e32a4c725aba0d21f94c15cd7ca8530ffe01776
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32970763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdff4547b1b7092afe2104dbf710a439a2b8bcdf54b87fbfda0de4631da4ef6a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Aug 2022 00:20:50 GMT
ADD file:7726efb0e0eb5003dbcf2967ec29364479eec8b41f2569ff189372153115b54b in / 
# Tue, 23 Aug 2022 00:20:51 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 02:54:26 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 23 Aug 2022 02:54:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 02:54:30 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 23 Aug 2022 02:54:30 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 23 Aug 2022 02:57:13 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 23 Aug 2022 02:57:13 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 23 Aug 2022 02:57:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 23 Aug 2022 02:57:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 02:57:14 GMT
USER memcache
# Tue, 23 Aug 2022 02:57:14 GMT
EXPOSE 11211
# Tue, 23 Aug 2022 02:57:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7a6db449b51b92eac5c81cdbd82917785343f1664b2be57b22337b0a40c5b29d`  
		Last Modified: Tue, 23 Aug 2022 00:24:59 GMT  
		Size: 31.4 MB (31381485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa73fb65ea8b12a2375459f0d656d3ad06e2863c906fcf962486eda3701f3fd6`  
		Last Modified: Tue, 23 Aug 2022 02:57:38 GMT  
		Size: 5.0 KB (4981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:502b4e8803067b28098d0ea52281cfef66da1ee1e869241612b545d7e9ff12de`  
		Last Modified: Tue, 23 Aug 2022 02:57:38 GMT  
		Size: 328.1 KB (328108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4be7903a0371d25a8e62fb8f58db1b4cc0d71407206895e81b2c5edddd96716`  
		Last Modified: Tue, 23 Aug 2022 02:57:38 GMT  
		Size: 1.3 MB (1255782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ece99ce94967ae22a842630bc182d3052a46922074b332055aa65763b70c4adb`  
		Last Modified: Tue, 23 Aug 2022 02:57:37 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72302fb7547064b5cd2773f9e54e03b6579b64dc8399245d683058505e87860`  
		Last Modified: Tue, 23 Aug 2022 02:57:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.16` - linux; arm variant v5

```console
$ docker pull memcached@sha256:7688ba62a1e2ca12e4fcfc18213eec8b6c8e967bb62395189bdc8d1b095f9ec8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 MB (30466108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63aeac5a0551e3a97aaddf116dbcb2a96b84635664ff3755675a42744590c23c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Aug 2022 01:17:14 GMT
ADD file:83fb076a50e935419eb0db2bd97477d7ed5f16aaac4c8cc35a4a69ac612df327 in / 
# Tue, 23 Aug 2022 01:17:14 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 01:49:29 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 23 Aug 2022 01:49:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 01:49:33 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 23 Aug 2022 01:49:34 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 23 Aug 2022 01:55:05 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 23 Aug 2022 01:55:05 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 23 Aug 2022 01:55:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 23 Aug 2022 01:55:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 01:55:06 GMT
USER memcache
# Tue, 23 Aug 2022 01:55:06 GMT
EXPOSE 11211
# Tue, 23 Aug 2022 01:55:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:74eb5afab626122970f8620ac001fcc4a200725acb05519b85aba47a38bf1016`  
		Last Modified: Tue, 23 Aug 2022 01:22:44 GMT  
		Size: 28.9 MB (28917250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a1b82f1abc9998be67c6dab29a896fcf5377c55fa3c09f0f60355321d0cc7e`  
		Last Modified: Tue, 23 Aug 2022 01:55:43 GMT  
		Size: 4.9 KB (4896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8d24ffcddd09d398cd33e29661cc865588572fdcfc4224b2ea8c0d1d001ed6`  
		Last Modified: Tue, 23 Aug 2022 01:55:44 GMT  
		Size: 316.6 KB (316628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:099cd43abb1475212736fcbb1adbd31b235ae10d1cbd4785e375473e77218967`  
		Last Modified: Tue, 23 Aug 2022 01:55:44 GMT  
		Size: 1.2 MB (1226927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b9006a418f2ced9ced0ca431dda2ce3543860c17742fc092a2309af44e78f22`  
		Last Modified: Tue, 23 Aug 2022 01:55:43 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df94046aab5da41252820ad1cb5d98c7a10c344be39148a95f1d6ad9e052bc1b`  
		Last Modified: Tue, 23 Aug 2022 01:55:44 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.16` - linux; arm variant v7

```console
$ docker pull memcached@sha256:25e768546f1e321b2a9031611f8ecd4081990c82f8774f7e051a5480cf18445d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28076294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5959e4e12e1b75611311d3866bc95f9fe30048418f972e70fa2c671a66149fdd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 02 Aug 2022 00:58:59 GMT
ADD file:1575b776a15adacebc0875642e97a80807d42dcfc8917e1406d47af7ac244c97 in / 
# Tue, 02 Aug 2022 00:58:59 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 06:28:56 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 02 Aug 2022 06:29:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Aug 2022 21:30:08 GMT
ENV MEMCACHED_VERSION=1.6.16
# Thu, 04 Aug 2022 21:30:08 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Thu, 04 Aug 2022 21:36:35 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Thu, 04 Aug 2022 21:36:35 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 04 Aug 2022 21:36:36 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 04 Aug 2022 21:36:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Aug 2022 21:36:37 GMT
USER memcache
# Thu, 04 Aug 2022 21:36:37 GMT
EXPOSE 11211
# Thu, 04 Aug 2022 21:36:37 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1dd75a3a9c893a7dc313f683dd62464b7eab6c6d522ee62c8a17022631830f32`  
		Last Modified: Tue, 02 Aug 2022 01:06:45 GMT  
		Size: 26.6 MB (26560586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44a675a8ce135f198539dc76b078733393238f7c7b899c8635980eed8f35f1cc`  
		Last Modified: Tue, 02 Aug 2022 09:35:13 GMT  
		Size: 4.9 KB (4890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497b0afd04c92a1e5d41f58dbc0d5d544b8880d000c0ffbd03adb48c32c0116b`  
		Last Modified: Tue, 02 Aug 2022 09:35:13 GMT  
		Size: 312.1 KB (312067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8874fe992be272d0e0780725714c2439507699c15bfad1a073df948a34eb668d`  
		Last Modified: Fri, 05 Aug 2022 00:37:30 GMT  
		Size: 1.2 MB (1198344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cd5e042b98c640c152a56816e122c5e7b0abe91535d5d891dceed9748e42129`  
		Last Modified: Fri, 05 Aug 2022 00:37:29 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e871a0f93bdc7cb723e47f45514f914186b73d1890a53cdfe8525dd034926d59`  
		Last Modified: Fri, 05 Aug 2022 00:37:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.16` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:759082b00d406f92781542ce86756eb73c5efe20acc7df6c25ac86be320a3ef5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31433439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e91fe6663d9d90deed07c1d003a80fa6698137267c83310828f24a7ef63f6ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 02 Aug 2022 00:40:38 GMT
ADD file:6039adfbca55ed34a719c37672c664e3524130a0e2a3b8663629b8120b81b790 in / 
# Tue, 02 Aug 2022 00:40:39 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 03:56:15 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 02 Aug 2022 03:56:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Aug 2022 20:33:46 GMT
ENV MEMCACHED_VERSION=1.6.16
# Thu, 04 Aug 2022 20:33:47 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Thu, 04 Aug 2022 20:36:17 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Thu, 04 Aug 2022 20:36:19 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 04 Aug 2022 20:36:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 04 Aug 2022 20:36:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Aug 2022 20:36:21 GMT
USER memcache
# Thu, 04 Aug 2022 20:36:22 GMT
EXPOSE 11211
# Thu, 04 Aug 2022 20:36:23 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a9fe95647e78b5516c7e2327355b6996e2ea295cd76ae242cbfe87f016b4e760`  
		Last Modified: Tue, 02 Aug 2022 00:46:05 GMT  
		Size: 30.1 MB (30054304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b983df009e7dc88033f53f015c09c56fd4db032d1abcade3333d8d4b515ff4af`  
		Last Modified: Tue, 02 Aug 2022 03:59:48 GMT  
		Size: 4.9 KB (4902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60720019405b50af041f391ec7dad90893ee95fc63fd6b3fb9da04850936f5db`  
		Last Modified: Tue, 02 Aug 2022 03:59:48 GMT  
		Size: 119.2 KB (119225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70569bedb4ee539337d6d3fd88e4076a1464b3a77bcfcca6604e18b815dbc402`  
		Last Modified: Thu, 04 Aug 2022 20:40:00 GMT  
		Size: 1.3 MB (1254600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:565112c01ad7b82688180f4fe70f5433126d79cc4b74e3d7f308601e2d34d9fe`  
		Last Modified: Thu, 04 Aug 2022 20:39:59 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce11290eb88924797c1fa048bd052c1243e4cb47e3469b26f3f1a3bc26472d19`  
		Last Modified: Thu, 04 Aug 2022 20:39:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.16` - linux; 386

```console
$ docker pull memcached@sha256:3770f2e3c3f2abb5f85a6a615e62fd5c78a61513ca573ee4385adf42629bd88c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.8 MB (33775724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2804b930e07f367a1e5adc6a5631e87c78a986d3ad64e06e3c549c20ad7ce735`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Aug 2022 01:02:40 GMT
ADD file:5ca62c98116941aaa64ec72afb689a088c46f75a3e83d5b0d4e58d65ec905ccd in / 
# Tue, 23 Aug 2022 01:02:40 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 03:22:44 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 23 Aug 2022 03:22:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 03:22:49 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 23 Aug 2022 03:22:50 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 23 Aug 2022 03:26:54 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 23 Aug 2022 03:26:56 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 23 Aug 2022 03:26:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 23 Aug 2022 03:26:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 03:26:58 GMT
USER memcache
# Tue, 23 Aug 2022 03:26:59 GMT
EXPOSE 11211
# Tue, 23 Aug 2022 03:27:00 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6b3cb4a05a891d9d8a87a2bd7247b16f79832a9d4afbad3ff5068f6fc2ba1560`  
		Last Modified: Tue, 23 Aug 2022 01:08:25 GMT  
		Size: 32.4 MB (32387317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd24201e0b5e9a68a67bdc3b464a01aeb9a2e5a859a582cdaa80ab08a608337`  
		Last Modified: Tue, 23 Aug 2022 03:27:47 GMT  
		Size: 4.8 KB (4774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3070e5e3b1d98fa0b67b8390880b7596c4719b774864de21f36ed86873041793`  
		Last Modified: Tue, 23 Aug 2022 03:27:48 GMT  
		Size: 130.1 KB (130136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a076923bc48ef00816393d79ac2aa3ad931f47309aff7a6cf0c6c74d443080f`  
		Last Modified: Tue, 23 Aug 2022 03:27:48 GMT  
		Size: 1.3 MB (1253091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7169b397a99c6597495d00b3cb6b04483b8950d04bc7cbdcccf983f225294bb4`  
		Last Modified: Tue, 23 Aug 2022 03:27:48 GMT  
		Size: 288.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55ee497fd4fa66154f7c38bc2bb37f6e356318dc032b26ed65eb94ddc8355995`  
		Last Modified: Tue, 23 Aug 2022 03:27:47 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.16` - linux; mips64le

```console
$ docker pull memcached@sha256:0d6798ccd4a9ac44c6ca7c358b2de6bdedbfe104de7d9987eedc68864ab8acc0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 MB (31002934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aca3e1ecca25fb97ad1d376d73b212cad11874d1f051c4c4bac1b2d27abc15fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 02 Aug 2022 01:10:34 GMT
ADD file:6dc22a1e5b5fcf23f2549406ddcc45c4e244f46e21eafa881de81fa87438e5d8 in / 
# Tue, 02 Aug 2022 01:10:38 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 03:22:53 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 02 Aug 2022 03:23:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Aug 2022 20:07:25 GMT
ENV MEMCACHED_VERSION=1.6.16
# Thu, 04 Aug 2022 20:07:28 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Thu, 04 Aug 2022 20:14:28 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Thu, 04 Aug 2022 20:14:30 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 04 Aug 2022 20:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 04 Aug 2022 20:14:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Aug 2022 20:14:40 GMT
USER memcache
# Thu, 04 Aug 2022 20:14:42 GMT
EXPOSE 11211
# Thu, 04 Aug 2022 20:14:45 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:88350749a27614c791450c256b051f023d81cdd256211274b1efac493779d2be`  
		Last Modified: Tue, 02 Aug 2022 01:21:02 GMT  
		Size: 29.6 MB (29628964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:117af7bbaadea9c81bbaa3a8a77b1ab5cd05bcac856c462cda2e81c9a40596ab`  
		Last Modified: Tue, 02 Aug 2022 03:30:45 GMT  
		Size: 4.9 KB (4863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a16d313748bd6b2dade87de73d79edd8a08e4cb662769a717f8587abc8d5e0`  
		Last Modified: Tue, 02 Aug 2022 03:30:46 GMT  
		Size: 117.1 KB (117127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d524786af3243ee367d118f6d5260cffa06d800f492f9b4bb36c910958186933`  
		Last Modified: Thu, 04 Aug 2022 20:15:05 GMT  
		Size: 1.3 MB (1251571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4badb1f1970762d08dbd43d7e101081a5fabd3c45e18afd70636397e83102d2f`  
		Last Modified: Thu, 04 Aug 2022 20:15:04 GMT  
		Size: 288.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3102636392803c3bbff48f39e7f143e3bf9a0528365d63b90dc31cd32060d3e0`  
		Last Modified: Thu, 04 Aug 2022 20:15:04 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.16` - linux; ppc64le

```console
$ docker pull memcached@sha256:6eac50a2d123c021e75657700bdd2d0335dcc97db595e783eb6feaf81e0d6ab0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 MB (36969051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77075f2945ec5e196ccf20148829ebe266a384c2972f723f72361e05e3ee1bf5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Aug 2022 01:24:52 GMT
ADD file:d35213360d726a18e220276d33f245115c3e94a321addaa4c9127488368b0203 in / 
# Tue, 23 Aug 2022 01:24:54 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 02:34:49 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 23 Aug 2022 02:34:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 02:34:56 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 23 Aug 2022 02:34:56 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 23 Aug 2022 02:38:10 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 23 Aug 2022 02:38:10 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 23 Aug 2022 02:38:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 23 Aug 2022 02:38:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 02:38:12 GMT
USER memcache
# Tue, 23 Aug 2022 02:38:12 GMT
EXPOSE 11211
# Tue, 23 Aug 2022 02:38:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:698954eda09d38dd1ccc9ce777b1f6bc7f7473fc6c4c3eb634acc8d035a42eae`  
		Last Modified: Tue, 23 Aug 2022 01:30:36 GMT  
		Size: 35.3 MB (35284280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ffb080d920662043edc67113c0de4c68258ad19c0fffd9e3b79fa01800c6015`  
		Last Modified: Tue, 23 Aug 2022 02:39:09 GMT  
		Size: 5.0 KB (4980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b1f66b68991d8f5ab064b3988db37a48b8f28b4ef0eb8e83efa4c419b630ff`  
		Last Modified: Tue, 23 Aug 2022 02:39:09 GMT  
		Size: 356.9 KB (356931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9653070548c34c29ed693878ef68223dbe9ccefc4653b86d3c8225bc8f85ac1`  
		Last Modified: Tue, 23 Aug 2022 02:39:09 GMT  
		Size: 1.3 MB (1322453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd51b501bab55d128a547f5c14e6410e4ef4b7b08f1867c7c933db716d7791e7`  
		Last Modified: Tue, 23 Aug 2022 02:39:09 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e693f7e8dfc8fe4a2af505658484b885fe097586d4f22c43aaf8278756e76ca`  
		Last Modified: Tue, 23 Aug 2022 02:39:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.16` - linux; s390x

```console
$ docker pull memcached@sha256:4f7e9706bfd16d98bfb48a6435c8359a167ab733777f16f24996cad3f431bdc5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31211398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6739ca31062c74398fdfec102afbacead1c25fa0decf2fa14bdecdcb6b160543`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 02 Aug 2022 00:42:27 GMT
ADD file:c2afc8990930846fbe7c99bfdfe9ea562c75feb6e3c9122431f7c9f8b5e51a7f in / 
# Tue, 02 Aug 2022 00:42:29 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 02:37:02 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 02 Aug 2022 02:37:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Aug 2022 20:28:18 GMT
ENV MEMCACHED_VERSION=1.6.16
# Thu, 04 Aug 2022 20:28:18 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Thu, 04 Aug 2022 20:31:37 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Thu, 04 Aug 2022 20:31:37 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 04 Aug 2022 20:31:37 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 04 Aug 2022 20:31:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Aug 2022 20:31:38 GMT
USER memcache
# Thu, 04 Aug 2022 20:31:38 GMT
EXPOSE 11211
# Thu, 04 Aug 2022 20:31:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:026d311d0716db60eba0572ea784c21031f420960510cebcc383dc53949b4db8`  
		Last Modified: Tue, 02 Aug 2022 00:48:01 GMT  
		Size: 29.6 MB (29640259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0ffdb328e548bd6b6311c78665ac8cd3be8f0b2e09691701d9b0bae0924f8f5`  
		Last Modified: Tue, 02 Aug 2022 02:41:16 GMT  
		Size: 5.0 KB (5025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fbb9677007b0ebab2fe6feab520da1962d3fcffb3490aa844681a46fcb35749`  
		Last Modified: Tue, 02 Aug 2022 02:41:16 GMT  
		Size: 324.2 KB (324183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9c93abfa1f832f2e1f02fbe7b9a489735142c2051dafa7af20d985ff2e2106b`  
		Last Modified: Thu, 04 Aug 2022 20:36:17 GMT  
		Size: 1.2 MB (1241523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f78bf4cf172bedc6ad3c92b859859b10c0394104262328d5664ddc0b1488b29`  
		Last Modified: Thu, 04 Aug 2022 20:36:17 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6a26d2d4c34166613098e1380842f1355b534e2335a1dea2128c193b7f19bec`  
		Last Modified: Thu, 04 Aug 2022 20:36:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:1.6.16-alpine`

```console
$ docker pull memcached@sha256:22fd822b2417986f627bd96bc687e85360200db73e8bc818fe6ffdfe1f24e413
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `memcached:1.6.16-alpine` - linux; amd64

```console
$ docker pull memcached@sha256:b1e59612ccc1ab79ccb764e8ae694c89c6e2dece9927b202c1a1820a665268f4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3867486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af3c4fe62d9dafd4336d17fc19dcc8e0ea69a41c4ea586e0544c371319a9497b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:53:39 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Tue, 09 Aug 2022 20:53:40 GMT
RUN apk add --no-cache libsasl
# Tue, 09 Aug 2022 20:53:40 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 09 Aug 2022 20:53:41 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 09 Aug 2022 20:56:30 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 09 Aug 2022 20:56:30 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 09 Aug 2022 20:56:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 09 Aug 2022 20:56:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 20:56:31 GMT
USER memcache
# Tue, 09 Aug 2022 20:56:31 GMT
EXPOSE 11211
# Tue, 09 Aug 2022 20:56:31 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d572ef57cdf8eb58de4b4e89970c5e64c6a2f8470bbbe4746efd56927df10611`  
		Last Modified: Tue, 09 Aug 2022 20:57:08 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed8976416286665206f17c9c2ead879425c6c6c62051fa7af308abd8790c0bc`  
		Last Modified: Tue, 09 Aug 2022 20:57:08 GMT  
		Size: 108.3 KB (108322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c657d873aa5cf9fbc93f3c3b68b8e7543ec1bc6335404b259ea5a7db4196422d`  
		Last Modified: Tue, 09 Aug 2022 20:57:08 GMT  
		Size: 951.4 KB (951438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f91921ed85e235501e9cd091c8d8601f04ea194fe4a461629fe7ab9eb9badd`  
		Last Modified: Tue, 09 Aug 2022 20:57:08 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198a10264961105745cf7038c02c22ae20695d9213c38421ec14d7cc8eda0d44`  
		Last Modified: Tue, 09 Aug 2022 20:57:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.16-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:44f0d141458db00ee50b9ad0ec9f39a08f2054fe45924bafddc3920d446727f0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3757682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5799dfb510c6b2e85d9290ef1eae349ba3365b9584932dbc450562979a046d9f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:48:03 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Tue, 09 Aug 2022 20:48:05 GMT
RUN apk add --no-cache libsasl
# Tue, 09 Aug 2022 20:48:05 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 09 Aug 2022 20:48:06 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 09 Aug 2022 20:50:51 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 09 Aug 2022 20:50:53 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 09 Aug 2022 20:50:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 09 Aug 2022 20:50:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 20:50:55 GMT
USER memcache
# Tue, 09 Aug 2022 20:50:56 GMT
EXPOSE 11211
# Tue, 09 Aug 2022 20:50:57 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d15db589ad12df2825238bc4f6832b2c6e3d991704c9b41db7865df5d402276`  
		Last Modified: Tue, 09 Aug 2022 20:51:50 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103b4be7608736e9e24d225ccd97cc4dfad6bacbe7bcf2ca1cd716b45ee32855`  
		Last Modified: Tue, 09 Aug 2022 20:51:50 GMT  
		Size: 109.6 KB (109566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be29d81faebb3b793bdb052326cbb181f786eb99078f62f6f00935c60c14a9fe`  
		Last Modified: Tue, 09 Aug 2022 20:51:50 GMT  
		Size: 938.8 KB (938808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a590dbe104d4e1ec4c488c22500f75e3b44977e09523893500694356ff65008b`  
		Last Modified: Tue, 09 Aug 2022 20:51:50 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da7fd81bf28f2c80e4823f86aea754145c41614f1a924f56f0d2f7e51747873`  
		Last Modified: Tue, 09 Aug 2022 20:51:50 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.16-alpine` - linux; 386

```console
$ docker pull memcached@sha256:e6fc7462999869fb634dbc73338735811a34ba127cbf512785b2d036132b7496
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3891350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b662b6ea7b7b0638994baa098f88f7a247ecc3da8fa1057e586dd3fdd1fe007`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Aug 2022 17:38:39 GMT
ADD file:b828bc14bc5ff03c8f7310fe0aed6ac5df19a393622d5d1d779a523234d07c0a in / 
# Tue, 09 Aug 2022 17:38:39 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:34:01 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Tue, 09 Aug 2022 18:34:02 GMT
RUN apk add --no-cache libsasl
# Tue, 09 Aug 2022 18:34:03 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 09 Aug 2022 18:34:04 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 09 Aug 2022 18:37:07 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 09 Aug 2022 18:37:09 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 09 Aug 2022 18:37:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 09 Aug 2022 18:37:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 18:37:11 GMT
USER memcache
# Tue, 09 Aug 2022 18:37:12 GMT
EXPOSE 11211
# Tue, 09 Aug 2022 18:37:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6c0d3b419d848ea31ca748254611d5d5ce3b76e3d7bba520fd87400fbb75f3b9`  
		Last Modified: Tue, 09 Aug 2022 17:39:33 GMT  
		Size: 2.8 MB (2807121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:240e236335200614c944d9ba79e2d7eda5cfa258a69e669b585cc28314d754f5`  
		Last Modified: Tue, 09 Aug 2022 18:38:05 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:844d1ba63a22190468423984b12b7d36f6c005e3316461b983f975f4b8dc9ee8`  
		Last Modified: Tue, 09 Aug 2022 18:38:05 GMT  
		Size: 119.8 KB (119826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad6d3cd2261a998624eba6805148058d37a9733e41f66cef88d3b5103170e4a8`  
		Last Modified: Tue, 09 Aug 2022 18:38:06 GMT  
		Size: 962.8 KB (962759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7983bf58c38f033ac9ab3011fd046fa03cb7848d5b2fb86955fd5e20c62e27fc`  
		Last Modified: Tue, 09 Aug 2022 18:38:05 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a108c54c3e573033e837b18319fbbfab59f4bbca1dfd29610c5be85ad2ea1bc9`  
		Last Modified: Tue, 09 Aug 2022 18:38:05 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.16-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:d798237b2695cb4cdcde6ad5c5ebeb01b03cb86bd534f5ef703d8b88c3f60db1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3912215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfb1d9b800eeba8d9cadba9dfee6f8b7db71228a7f42e7fd208109e6f8d33a2e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Aug 2022 17:17:09 GMT
ADD file:66b351666e41834033d334aeb3dc6998dea77aa22e8e254028c923fee67a41a8 in / 
# Tue, 09 Aug 2022 17:17:10 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:48:17 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Tue, 09 Aug 2022 18:48:19 GMT
RUN apk add --no-cache libsasl
# Tue, 09 Aug 2022 18:48:19 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 09 Aug 2022 18:48:19 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 09 Aug 2022 18:51:34 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 09 Aug 2022 18:51:34 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 09 Aug 2022 18:51:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 09 Aug 2022 18:51:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 18:51:36 GMT
USER memcache
# Tue, 09 Aug 2022 18:51:36 GMT
EXPOSE 11211
# Tue, 09 Aug 2022 18:51:37 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c79e5d1a8c89b87020a754c8a5c8370faaa37bfb5bca1d8af66770d522ef1caf`  
		Last Modified: Tue, 09 Aug 2022 17:18:26 GMT  
		Size: 2.8 MB (2803320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086c869249c97411ce380e3b76305e0b85731874d0ea57dfd0de74e1f387443d`  
		Last Modified: Tue, 09 Aug 2022 18:52:28 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75e55886182590f2e7eef7f1c21851fd9c322339484e8345afd12376d976ddbd`  
		Last Modified: Tue, 09 Aug 2022 18:52:28 GMT  
		Size: 126.1 KB (126064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5986c4b1340bf1f46f9c87bfe46749c8b2c36b125cc144d44369ffa6da235643`  
		Last Modified: Tue, 09 Aug 2022 18:52:29 GMT  
		Size: 981.2 KB (981160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94057389e17fb62c8067389939b22ba89063219c50a7a348d0343d3aee37d933`  
		Last Modified: Tue, 09 Aug 2022 18:52:28 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989f24ebe1a18ca3cac84b41e1b10934fc83856828b9fb1da76a8d894048512e`  
		Last Modified: Tue, 09 Aug 2022 18:52:28 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.16-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:f05c64785454795713f41d5cf814a5debb9cf42c3d4d1b6298ba93d897cfc72a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3646606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef9e9b1c8f1ad73aa6d447c3635fa404bffc5d074a3480ae8644c2ae121a39af`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Aug 2022 17:41:46 GMT
ADD file:b43a065471bc4711415d3c67cd5b6559b0c48ee7ffe9761530477cf457a6dc34 in / 
# Tue, 09 Aug 2022 17:41:46 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 19:11:19 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Tue, 09 Aug 2022 19:11:20 GMT
RUN apk add --no-cache libsasl
# Tue, 09 Aug 2022 19:11:20 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 09 Aug 2022 19:11:20 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 09 Aug 2022 19:14:45 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 09 Aug 2022 19:14:45 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 09 Aug 2022 19:14:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 09 Aug 2022 19:14:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 19:14:46 GMT
USER memcache
# Tue, 09 Aug 2022 19:14:46 GMT
EXPOSE 11211
# Tue, 09 Aug 2022 19:14:46 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:790c84f1f3409eab952345157df7fa804ba6b5f06d4ceb6f2dfa3c6de2064397`  
		Last Modified: Tue, 09 Aug 2022 17:42:45 GMT  
		Size: 2.6 MB (2590597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:463a70f3df946e83a223bd55002470af1b7f8d483babe452e515a809b965d35c`  
		Last Modified: Tue, 09 Aug 2022 19:15:35 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df0b8be6e73cbbdde959ca7a21d3fd6c8e36e05bc9c7a46be4e5bfa5b664a50c`  
		Last Modified: Tue, 09 Aug 2022 19:15:35 GMT  
		Size: 112.5 KB (112508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f39508191d6e035471ed454d54a8ec05b775ff26d4e6902076dd66901c870fd4`  
		Last Modified: Tue, 09 Aug 2022 19:15:35 GMT  
		Size: 941.8 KB (941827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:664e864043941612ce16890523ab6ef1ca3d7a253f0384d99b2e0c3957b6398f`  
		Last Modified: Tue, 09 Aug 2022 19:15:35 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f2ba1910d2ededf72d427c17c6dd473de7acc0ad7513e183ab5c4c3a0c43142`  
		Last Modified: Tue, 09 Aug 2022 19:15:35 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:1.6.16-alpine3.16`

```console
$ docker pull memcached@sha256:22fd822b2417986f627bd96bc687e85360200db73e8bc818fe6ffdfe1f24e413
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `memcached:1.6.16-alpine3.16` - linux; amd64

```console
$ docker pull memcached@sha256:b1e59612ccc1ab79ccb764e8ae694c89c6e2dece9927b202c1a1820a665268f4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3867486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af3c4fe62d9dafd4336d17fc19dcc8e0ea69a41c4ea586e0544c371319a9497b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:53:39 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Tue, 09 Aug 2022 20:53:40 GMT
RUN apk add --no-cache libsasl
# Tue, 09 Aug 2022 20:53:40 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 09 Aug 2022 20:53:41 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 09 Aug 2022 20:56:30 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 09 Aug 2022 20:56:30 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 09 Aug 2022 20:56:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 09 Aug 2022 20:56:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 20:56:31 GMT
USER memcache
# Tue, 09 Aug 2022 20:56:31 GMT
EXPOSE 11211
# Tue, 09 Aug 2022 20:56:31 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d572ef57cdf8eb58de4b4e89970c5e64c6a2f8470bbbe4746efd56927df10611`  
		Last Modified: Tue, 09 Aug 2022 20:57:08 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed8976416286665206f17c9c2ead879425c6c6c62051fa7af308abd8790c0bc`  
		Last Modified: Tue, 09 Aug 2022 20:57:08 GMT  
		Size: 108.3 KB (108322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c657d873aa5cf9fbc93f3c3b68b8e7543ec1bc6335404b259ea5a7db4196422d`  
		Last Modified: Tue, 09 Aug 2022 20:57:08 GMT  
		Size: 951.4 KB (951438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f91921ed85e235501e9cd091c8d8601f04ea194fe4a461629fe7ab9eb9badd`  
		Last Modified: Tue, 09 Aug 2022 20:57:08 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198a10264961105745cf7038c02c22ae20695d9213c38421ec14d7cc8eda0d44`  
		Last Modified: Tue, 09 Aug 2022 20:57:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.16-alpine3.16` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:44f0d141458db00ee50b9ad0ec9f39a08f2054fe45924bafddc3920d446727f0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3757682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5799dfb510c6b2e85d9290ef1eae349ba3365b9584932dbc450562979a046d9f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:48:03 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Tue, 09 Aug 2022 20:48:05 GMT
RUN apk add --no-cache libsasl
# Tue, 09 Aug 2022 20:48:05 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 09 Aug 2022 20:48:06 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 09 Aug 2022 20:50:51 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 09 Aug 2022 20:50:53 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 09 Aug 2022 20:50:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 09 Aug 2022 20:50:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 20:50:55 GMT
USER memcache
# Tue, 09 Aug 2022 20:50:56 GMT
EXPOSE 11211
# Tue, 09 Aug 2022 20:50:57 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d15db589ad12df2825238bc4f6832b2c6e3d991704c9b41db7865df5d402276`  
		Last Modified: Tue, 09 Aug 2022 20:51:50 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103b4be7608736e9e24d225ccd97cc4dfad6bacbe7bcf2ca1cd716b45ee32855`  
		Last Modified: Tue, 09 Aug 2022 20:51:50 GMT  
		Size: 109.6 KB (109566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be29d81faebb3b793bdb052326cbb181f786eb99078f62f6f00935c60c14a9fe`  
		Last Modified: Tue, 09 Aug 2022 20:51:50 GMT  
		Size: 938.8 KB (938808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a590dbe104d4e1ec4c488c22500f75e3b44977e09523893500694356ff65008b`  
		Last Modified: Tue, 09 Aug 2022 20:51:50 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da7fd81bf28f2c80e4823f86aea754145c41614f1a924f56f0d2f7e51747873`  
		Last Modified: Tue, 09 Aug 2022 20:51:50 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.16-alpine3.16` - linux; 386

```console
$ docker pull memcached@sha256:e6fc7462999869fb634dbc73338735811a34ba127cbf512785b2d036132b7496
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3891350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b662b6ea7b7b0638994baa098f88f7a247ecc3da8fa1057e586dd3fdd1fe007`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Aug 2022 17:38:39 GMT
ADD file:b828bc14bc5ff03c8f7310fe0aed6ac5df19a393622d5d1d779a523234d07c0a in / 
# Tue, 09 Aug 2022 17:38:39 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:34:01 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Tue, 09 Aug 2022 18:34:02 GMT
RUN apk add --no-cache libsasl
# Tue, 09 Aug 2022 18:34:03 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 09 Aug 2022 18:34:04 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 09 Aug 2022 18:37:07 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 09 Aug 2022 18:37:09 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 09 Aug 2022 18:37:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 09 Aug 2022 18:37:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 18:37:11 GMT
USER memcache
# Tue, 09 Aug 2022 18:37:12 GMT
EXPOSE 11211
# Tue, 09 Aug 2022 18:37:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6c0d3b419d848ea31ca748254611d5d5ce3b76e3d7bba520fd87400fbb75f3b9`  
		Last Modified: Tue, 09 Aug 2022 17:39:33 GMT  
		Size: 2.8 MB (2807121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:240e236335200614c944d9ba79e2d7eda5cfa258a69e669b585cc28314d754f5`  
		Last Modified: Tue, 09 Aug 2022 18:38:05 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:844d1ba63a22190468423984b12b7d36f6c005e3316461b983f975f4b8dc9ee8`  
		Last Modified: Tue, 09 Aug 2022 18:38:05 GMT  
		Size: 119.8 KB (119826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad6d3cd2261a998624eba6805148058d37a9733e41f66cef88d3b5103170e4a8`  
		Last Modified: Tue, 09 Aug 2022 18:38:06 GMT  
		Size: 962.8 KB (962759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7983bf58c38f033ac9ab3011fd046fa03cb7848d5b2fb86955fd5e20c62e27fc`  
		Last Modified: Tue, 09 Aug 2022 18:38:05 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a108c54c3e573033e837b18319fbbfab59f4bbca1dfd29610c5be85ad2ea1bc9`  
		Last Modified: Tue, 09 Aug 2022 18:38:05 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.16-alpine3.16` - linux; ppc64le

```console
$ docker pull memcached@sha256:d798237b2695cb4cdcde6ad5c5ebeb01b03cb86bd534f5ef703d8b88c3f60db1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3912215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfb1d9b800eeba8d9cadba9dfee6f8b7db71228a7f42e7fd208109e6f8d33a2e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Aug 2022 17:17:09 GMT
ADD file:66b351666e41834033d334aeb3dc6998dea77aa22e8e254028c923fee67a41a8 in / 
# Tue, 09 Aug 2022 17:17:10 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:48:17 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Tue, 09 Aug 2022 18:48:19 GMT
RUN apk add --no-cache libsasl
# Tue, 09 Aug 2022 18:48:19 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 09 Aug 2022 18:48:19 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 09 Aug 2022 18:51:34 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 09 Aug 2022 18:51:34 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 09 Aug 2022 18:51:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 09 Aug 2022 18:51:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 18:51:36 GMT
USER memcache
# Tue, 09 Aug 2022 18:51:36 GMT
EXPOSE 11211
# Tue, 09 Aug 2022 18:51:37 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c79e5d1a8c89b87020a754c8a5c8370faaa37bfb5bca1d8af66770d522ef1caf`  
		Last Modified: Tue, 09 Aug 2022 17:18:26 GMT  
		Size: 2.8 MB (2803320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086c869249c97411ce380e3b76305e0b85731874d0ea57dfd0de74e1f387443d`  
		Last Modified: Tue, 09 Aug 2022 18:52:28 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75e55886182590f2e7eef7f1c21851fd9c322339484e8345afd12376d976ddbd`  
		Last Modified: Tue, 09 Aug 2022 18:52:28 GMT  
		Size: 126.1 KB (126064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5986c4b1340bf1f46f9c87bfe46749c8b2c36b125cc144d44369ffa6da235643`  
		Last Modified: Tue, 09 Aug 2022 18:52:29 GMT  
		Size: 981.2 KB (981160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94057389e17fb62c8067389939b22ba89063219c50a7a348d0343d3aee37d933`  
		Last Modified: Tue, 09 Aug 2022 18:52:28 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989f24ebe1a18ca3cac84b41e1b10934fc83856828b9fb1da76a8d894048512e`  
		Last Modified: Tue, 09 Aug 2022 18:52:28 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.16-alpine3.16` - linux; s390x

```console
$ docker pull memcached@sha256:f05c64785454795713f41d5cf814a5debb9cf42c3d4d1b6298ba93d897cfc72a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3646606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef9e9b1c8f1ad73aa6d447c3635fa404bffc5d074a3480ae8644c2ae121a39af`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Aug 2022 17:41:46 GMT
ADD file:b43a065471bc4711415d3c67cd5b6559b0c48ee7ffe9761530477cf457a6dc34 in / 
# Tue, 09 Aug 2022 17:41:46 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 19:11:19 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Tue, 09 Aug 2022 19:11:20 GMT
RUN apk add --no-cache libsasl
# Tue, 09 Aug 2022 19:11:20 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 09 Aug 2022 19:11:20 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 09 Aug 2022 19:14:45 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 09 Aug 2022 19:14:45 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 09 Aug 2022 19:14:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 09 Aug 2022 19:14:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 19:14:46 GMT
USER memcache
# Tue, 09 Aug 2022 19:14:46 GMT
EXPOSE 11211
# Tue, 09 Aug 2022 19:14:46 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:790c84f1f3409eab952345157df7fa804ba6b5f06d4ceb6f2dfa3c6de2064397`  
		Last Modified: Tue, 09 Aug 2022 17:42:45 GMT  
		Size: 2.6 MB (2590597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:463a70f3df946e83a223bd55002470af1b7f8d483babe452e515a809b965d35c`  
		Last Modified: Tue, 09 Aug 2022 19:15:35 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df0b8be6e73cbbdde959ca7a21d3fd6c8e36e05bc9c7a46be4e5bfa5b664a50c`  
		Last Modified: Tue, 09 Aug 2022 19:15:35 GMT  
		Size: 112.5 KB (112508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f39508191d6e035471ed454d54a8ec05b775ff26d4e6902076dd66901c870fd4`  
		Last Modified: Tue, 09 Aug 2022 19:15:35 GMT  
		Size: 941.8 KB (941827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:664e864043941612ce16890523ab6ef1ca3d7a253f0384d99b2e0c3957b6398f`  
		Last Modified: Tue, 09 Aug 2022 19:15:35 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f2ba1910d2ededf72d427c17c6dd473de7acc0ad7513e183ab5c4c3a0c43142`  
		Last Modified: Tue, 09 Aug 2022 19:15:35 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:1.6.16-bullseye`

```console
$ docker pull memcached@sha256:22ed710ee778c797865ebff08e825df55df20508075cf275311cca55a235e652
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `memcached:1.6.16-bullseye` - linux; amd64

```console
$ docker pull memcached@sha256:a5dc74cbb9f905192c3caa290e32a4c725aba0d21f94c15cd7ca8530ffe01776
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32970763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdff4547b1b7092afe2104dbf710a439a2b8bcdf54b87fbfda0de4631da4ef6a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Aug 2022 00:20:50 GMT
ADD file:7726efb0e0eb5003dbcf2967ec29364479eec8b41f2569ff189372153115b54b in / 
# Tue, 23 Aug 2022 00:20:51 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 02:54:26 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 23 Aug 2022 02:54:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 02:54:30 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 23 Aug 2022 02:54:30 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 23 Aug 2022 02:57:13 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 23 Aug 2022 02:57:13 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 23 Aug 2022 02:57:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 23 Aug 2022 02:57:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 02:57:14 GMT
USER memcache
# Tue, 23 Aug 2022 02:57:14 GMT
EXPOSE 11211
# Tue, 23 Aug 2022 02:57:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7a6db449b51b92eac5c81cdbd82917785343f1664b2be57b22337b0a40c5b29d`  
		Last Modified: Tue, 23 Aug 2022 00:24:59 GMT  
		Size: 31.4 MB (31381485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa73fb65ea8b12a2375459f0d656d3ad06e2863c906fcf962486eda3701f3fd6`  
		Last Modified: Tue, 23 Aug 2022 02:57:38 GMT  
		Size: 5.0 KB (4981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:502b4e8803067b28098d0ea52281cfef66da1ee1e869241612b545d7e9ff12de`  
		Last Modified: Tue, 23 Aug 2022 02:57:38 GMT  
		Size: 328.1 KB (328108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4be7903a0371d25a8e62fb8f58db1b4cc0d71407206895e81b2c5edddd96716`  
		Last Modified: Tue, 23 Aug 2022 02:57:38 GMT  
		Size: 1.3 MB (1255782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ece99ce94967ae22a842630bc182d3052a46922074b332055aa65763b70c4adb`  
		Last Modified: Tue, 23 Aug 2022 02:57:37 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72302fb7547064b5cd2773f9e54e03b6579b64dc8399245d683058505e87860`  
		Last Modified: Tue, 23 Aug 2022 02:57:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.16-bullseye` - linux; arm variant v5

```console
$ docker pull memcached@sha256:7688ba62a1e2ca12e4fcfc18213eec8b6c8e967bb62395189bdc8d1b095f9ec8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 MB (30466108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63aeac5a0551e3a97aaddf116dbcb2a96b84635664ff3755675a42744590c23c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Aug 2022 01:17:14 GMT
ADD file:83fb076a50e935419eb0db2bd97477d7ed5f16aaac4c8cc35a4a69ac612df327 in / 
# Tue, 23 Aug 2022 01:17:14 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 01:49:29 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 23 Aug 2022 01:49:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 01:49:33 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 23 Aug 2022 01:49:34 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 23 Aug 2022 01:55:05 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 23 Aug 2022 01:55:05 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 23 Aug 2022 01:55:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 23 Aug 2022 01:55:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 01:55:06 GMT
USER memcache
# Tue, 23 Aug 2022 01:55:06 GMT
EXPOSE 11211
# Tue, 23 Aug 2022 01:55:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:74eb5afab626122970f8620ac001fcc4a200725acb05519b85aba47a38bf1016`  
		Last Modified: Tue, 23 Aug 2022 01:22:44 GMT  
		Size: 28.9 MB (28917250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a1b82f1abc9998be67c6dab29a896fcf5377c55fa3c09f0f60355321d0cc7e`  
		Last Modified: Tue, 23 Aug 2022 01:55:43 GMT  
		Size: 4.9 KB (4896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8d24ffcddd09d398cd33e29661cc865588572fdcfc4224b2ea8c0d1d001ed6`  
		Last Modified: Tue, 23 Aug 2022 01:55:44 GMT  
		Size: 316.6 KB (316628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:099cd43abb1475212736fcbb1adbd31b235ae10d1cbd4785e375473e77218967`  
		Last Modified: Tue, 23 Aug 2022 01:55:44 GMT  
		Size: 1.2 MB (1226927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b9006a418f2ced9ced0ca431dda2ce3543860c17742fc092a2309af44e78f22`  
		Last Modified: Tue, 23 Aug 2022 01:55:43 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df94046aab5da41252820ad1cb5d98c7a10c344be39148a95f1d6ad9e052bc1b`  
		Last Modified: Tue, 23 Aug 2022 01:55:44 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.16-bullseye` - linux; arm variant v7

```console
$ docker pull memcached@sha256:25e768546f1e321b2a9031611f8ecd4081990c82f8774f7e051a5480cf18445d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28076294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5959e4e12e1b75611311d3866bc95f9fe30048418f972e70fa2c671a66149fdd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 02 Aug 2022 00:58:59 GMT
ADD file:1575b776a15adacebc0875642e97a80807d42dcfc8917e1406d47af7ac244c97 in / 
# Tue, 02 Aug 2022 00:58:59 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 06:28:56 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 02 Aug 2022 06:29:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Aug 2022 21:30:08 GMT
ENV MEMCACHED_VERSION=1.6.16
# Thu, 04 Aug 2022 21:30:08 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Thu, 04 Aug 2022 21:36:35 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Thu, 04 Aug 2022 21:36:35 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 04 Aug 2022 21:36:36 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 04 Aug 2022 21:36:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Aug 2022 21:36:37 GMT
USER memcache
# Thu, 04 Aug 2022 21:36:37 GMT
EXPOSE 11211
# Thu, 04 Aug 2022 21:36:37 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1dd75a3a9c893a7dc313f683dd62464b7eab6c6d522ee62c8a17022631830f32`  
		Last Modified: Tue, 02 Aug 2022 01:06:45 GMT  
		Size: 26.6 MB (26560586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44a675a8ce135f198539dc76b078733393238f7c7b899c8635980eed8f35f1cc`  
		Last Modified: Tue, 02 Aug 2022 09:35:13 GMT  
		Size: 4.9 KB (4890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497b0afd04c92a1e5d41f58dbc0d5d544b8880d000c0ffbd03adb48c32c0116b`  
		Last Modified: Tue, 02 Aug 2022 09:35:13 GMT  
		Size: 312.1 KB (312067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8874fe992be272d0e0780725714c2439507699c15bfad1a073df948a34eb668d`  
		Last Modified: Fri, 05 Aug 2022 00:37:30 GMT  
		Size: 1.2 MB (1198344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cd5e042b98c640c152a56816e122c5e7b0abe91535d5d891dceed9748e42129`  
		Last Modified: Fri, 05 Aug 2022 00:37:29 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e871a0f93bdc7cb723e47f45514f914186b73d1890a53cdfe8525dd034926d59`  
		Last Modified: Fri, 05 Aug 2022 00:37:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.16-bullseye` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:759082b00d406f92781542ce86756eb73c5efe20acc7df6c25ac86be320a3ef5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31433439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e91fe6663d9d90deed07c1d003a80fa6698137267c83310828f24a7ef63f6ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 02 Aug 2022 00:40:38 GMT
ADD file:6039adfbca55ed34a719c37672c664e3524130a0e2a3b8663629b8120b81b790 in / 
# Tue, 02 Aug 2022 00:40:39 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 03:56:15 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 02 Aug 2022 03:56:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Aug 2022 20:33:46 GMT
ENV MEMCACHED_VERSION=1.6.16
# Thu, 04 Aug 2022 20:33:47 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Thu, 04 Aug 2022 20:36:17 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Thu, 04 Aug 2022 20:36:19 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 04 Aug 2022 20:36:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 04 Aug 2022 20:36:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Aug 2022 20:36:21 GMT
USER memcache
# Thu, 04 Aug 2022 20:36:22 GMT
EXPOSE 11211
# Thu, 04 Aug 2022 20:36:23 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a9fe95647e78b5516c7e2327355b6996e2ea295cd76ae242cbfe87f016b4e760`  
		Last Modified: Tue, 02 Aug 2022 00:46:05 GMT  
		Size: 30.1 MB (30054304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b983df009e7dc88033f53f015c09c56fd4db032d1abcade3333d8d4b515ff4af`  
		Last Modified: Tue, 02 Aug 2022 03:59:48 GMT  
		Size: 4.9 KB (4902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60720019405b50af041f391ec7dad90893ee95fc63fd6b3fb9da04850936f5db`  
		Last Modified: Tue, 02 Aug 2022 03:59:48 GMT  
		Size: 119.2 KB (119225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70569bedb4ee539337d6d3fd88e4076a1464b3a77bcfcca6604e18b815dbc402`  
		Last Modified: Thu, 04 Aug 2022 20:40:00 GMT  
		Size: 1.3 MB (1254600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:565112c01ad7b82688180f4fe70f5433126d79cc4b74e3d7f308601e2d34d9fe`  
		Last Modified: Thu, 04 Aug 2022 20:39:59 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce11290eb88924797c1fa048bd052c1243e4cb47e3469b26f3f1a3bc26472d19`  
		Last Modified: Thu, 04 Aug 2022 20:39:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.16-bullseye` - linux; 386

```console
$ docker pull memcached@sha256:3770f2e3c3f2abb5f85a6a615e62fd5c78a61513ca573ee4385adf42629bd88c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.8 MB (33775724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2804b930e07f367a1e5adc6a5631e87c78a986d3ad64e06e3c549c20ad7ce735`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Aug 2022 01:02:40 GMT
ADD file:5ca62c98116941aaa64ec72afb689a088c46f75a3e83d5b0d4e58d65ec905ccd in / 
# Tue, 23 Aug 2022 01:02:40 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 03:22:44 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 23 Aug 2022 03:22:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 03:22:49 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 23 Aug 2022 03:22:50 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 23 Aug 2022 03:26:54 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 23 Aug 2022 03:26:56 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 23 Aug 2022 03:26:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 23 Aug 2022 03:26:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 03:26:58 GMT
USER memcache
# Tue, 23 Aug 2022 03:26:59 GMT
EXPOSE 11211
# Tue, 23 Aug 2022 03:27:00 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6b3cb4a05a891d9d8a87a2bd7247b16f79832a9d4afbad3ff5068f6fc2ba1560`  
		Last Modified: Tue, 23 Aug 2022 01:08:25 GMT  
		Size: 32.4 MB (32387317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd24201e0b5e9a68a67bdc3b464a01aeb9a2e5a859a582cdaa80ab08a608337`  
		Last Modified: Tue, 23 Aug 2022 03:27:47 GMT  
		Size: 4.8 KB (4774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3070e5e3b1d98fa0b67b8390880b7596c4719b774864de21f36ed86873041793`  
		Last Modified: Tue, 23 Aug 2022 03:27:48 GMT  
		Size: 130.1 KB (130136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a076923bc48ef00816393d79ac2aa3ad931f47309aff7a6cf0c6c74d443080f`  
		Last Modified: Tue, 23 Aug 2022 03:27:48 GMT  
		Size: 1.3 MB (1253091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7169b397a99c6597495d00b3cb6b04483b8950d04bc7cbdcccf983f225294bb4`  
		Last Modified: Tue, 23 Aug 2022 03:27:48 GMT  
		Size: 288.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55ee497fd4fa66154f7c38bc2bb37f6e356318dc032b26ed65eb94ddc8355995`  
		Last Modified: Tue, 23 Aug 2022 03:27:47 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.16-bullseye` - linux; mips64le

```console
$ docker pull memcached@sha256:0d6798ccd4a9ac44c6ca7c358b2de6bdedbfe104de7d9987eedc68864ab8acc0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 MB (31002934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aca3e1ecca25fb97ad1d376d73b212cad11874d1f051c4c4bac1b2d27abc15fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 02 Aug 2022 01:10:34 GMT
ADD file:6dc22a1e5b5fcf23f2549406ddcc45c4e244f46e21eafa881de81fa87438e5d8 in / 
# Tue, 02 Aug 2022 01:10:38 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 03:22:53 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 02 Aug 2022 03:23:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Aug 2022 20:07:25 GMT
ENV MEMCACHED_VERSION=1.6.16
# Thu, 04 Aug 2022 20:07:28 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Thu, 04 Aug 2022 20:14:28 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Thu, 04 Aug 2022 20:14:30 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 04 Aug 2022 20:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 04 Aug 2022 20:14:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Aug 2022 20:14:40 GMT
USER memcache
# Thu, 04 Aug 2022 20:14:42 GMT
EXPOSE 11211
# Thu, 04 Aug 2022 20:14:45 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:88350749a27614c791450c256b051f023d81cdd256211274b1efac493779d2be`  
		Last Modified: Tue, 02 Aug 2022 01:21:02 GMT  
		Size: 29.6 MB (29628964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:117af7bbaadea9c81bbaa3a8a77b1ab5cd05bcac856c462cda2e81c9a40596ab`  
		Last Modified: Tue, 02 Aug 2022 03:30:45 GMT  
		Size: 4.9 KB (4863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a16d313748bd6b2dade87de73d79edd8a08e4cb662769a717f8587abc8d5e0`  
		Last Modified: Tue, 02 Aug 2022 03:30:46 GMT  
		Size: 117.1 KB (117127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d524786af3243ee367d118f6d5260cffa06d800f492f9b4bb36c910958186933`  
		Last Modified: Thu, 04 Aug 2022 20:15:05 GMT  
		Size: 1.3 MB (1251571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4badb1f1970762d08dbd43d7e101081a5fabd3c45e18afd70636397e83102d2f`  
		Last Modified: Thu, 04 Aug 2022 20:15:04 GMT  
		Size: 288.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3102636392803c3bbff48f39e7f143e3bf9a0528365d63b90dc31cd32060d3e0`  
		Last Modified: Thu, 04 Aug 2022 20:15:04 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.16-bullseye` - linux; ppc64le

```console
$ docker pull memcached@sha256:6eac50a2d123c021e75657700bdd2d0335dcc97db595e783eb6feaf81e0d6ab0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 MB (36969051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77075f2945ec5e196ccf20148829ebe266a384c2972f723f72361e05e3ee1bf5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Aug 2022 01:24:52 GMT
ADD file:d35213360d726a18e220276d33f245115c3e94a321addaa4c9127488368b0203 in / 
# Tue, 23 Aug 2022 01:24:54 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 02:34:49 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 23 Aug 2022 02:34:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 02:34:56 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 23 Aug 2022 02:34:56 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 23 Aug 2022 02:38:10 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 23 Aug 2022 02:38:10 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 23 Aug 2022 02:38:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 23 Aug 2022 02:38:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 02:38:12 GMT
USER memcache
# Tue, 23 Aug 2022 02:38:12 GMT
EXPOSE 11211
# Tue, 23 Aug 2022 02:38:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:698954eda09d38dd1ccc9ce777b1f6bc7f7473fc6c4c3eb634acc8d035a42eae`  
		Last Modified: Tue, 23 Aug 2022 01:30:36 GMT  
		Size: 35.3 MB (35284280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ffb080d920662043edc67113c0de4c68258ad19c0fffd9e3b79fa01800c6015`  
		Last Modified: Tue, 23 Aug 2022 02:39:09 GMT  
		Size: 5.0 KB (4980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b1f66b68991d8f5ab064b3988db37a48b8f28b4ef0eb8e83efa4c419b630ff`  
		Last Modified: Tue, 23 Aug 2022 02:39:09 GMT  
		Size: 356.9 KB (356931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9653070548c34c29ed693878ef68223dbe9ccefc4653b86d3c8225bc8f85ac1`  
		Last Modified: Tue, 23 Aug 2022 02:39:09 GMT  
		Size: 1.3 MB (1322453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd51b501bab55d128a547f5c14e6410e4ef4b7b08f1867c7c933db716d7791e7`  
		Last Modified: Tue, 23 Aug 2022 02:39:09 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e693f7e8dfc8fe4a2af505658484b885fe097586d4f22c43aaf8278756e76ca`  
		Last Modified: Tue, 23 Aug 2022 02:39:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.16-bullseye` - linux; s390x

```console
$ docker pull memcached@sha256:4f7e9706bfd16d98bfb48a6435c8359a167ab733777f16f24996cad3f431bdc5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31211398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6739ca31062c74398fdfec102afbacead1c25fa0decf2fa14bdecdcb6b160543`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 02 Aug 2022 00:42:27 GMT
ADD file:c2afc8990930846fbe7c99bfdfe9ea562c75feb6e3c9122431f7c9f8b5e51a7f in / 
# Tue, 02 Aug 2022 00:42:29 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 02:37:02 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 02 Aug 2022 02:37:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Aug 2022 20:28:18 GMT
ENV MEMCACHED_VERSION=1.6.16
# Thu, 04 Aug 2022 20:28:18 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Thu, 04 Aug 2022 20:31:37 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Thu, 04 Aug 2022 20:31:37 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 04 Aug 2022 20:31:37 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 04 Aug 2022 20:31:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Aug 2022 20:31:38 GMT
USER memcache
# Thu, 04 Aug 2022 20:31:38 GMT
EXPOSE 11211
# Thu, 04 Aug 2022 20:31:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:026d311d0716db60eba0572ea784c21031f420960510cebcc383dc53949b4db8`  
		Last Modified: Tue, 02 Aug 2022 00:48:01 GMT  
		Size: 29.6 MB (29640259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0ffdb328e548bd6b6311c78665ac8cd3be8f0b2e09691701d9b0bae0924f8f5`  
		Last Modified: Tue, 02 Aug 2022 02:41:16 GMT  
		Size: 5.0 KB (5025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fbb9677007b0ebab2fe6feab520da1962d3fcffb3490aa844681a46fcb35749`  
		Last Modified: Tue, 02 Aug 2022 02:41:16 GMT  
		Size: 324.2 KB (324183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9c93abfa1f832f2e1f02fbe7b9a489735142c2051dafa7af20d985ff2e2106b`  
		Last Modified: Thu, 04 Aug 2022 20:36:17 GMT  
		Size: 1.2 MB (1241523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f78bf4cf172bedc6ad3c92b859859b10c0394104262328d5664ddc0b1488b29`  
		Last Modified: Thu, 04 Aug 2022 20:36:17 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6a26d2d4c34166613098e1380842f1355b534e2335a1dea2128c193b7f19bec`  
		Last Modified: Thu, 04 Aug 2022 20:36:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:alpine`

```console
$ docker pull memcached@sha256:67a95346c7d0fbe3b1e6d1160cdec386503e0ad7c06e8d4056c3b0754e679eed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `memcached:alpine` - linux; amd64

```console
$ docker pull memcached@sha256:b1e59612ccc1ab79ccb764e8ae694c89c6e2dece9927b202c1a1820a665268f4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3867486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af3c4fe62d9dafd4336d17fc19dcc8e0ea69a41c4ea586e0544c371319a9497b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:53:39 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Tue, 09 Aug 2022 20:53:40 GMT
RUN apk add --no-cache libsasl
# Tue, 09 Aug 2022 20:53:40 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 09 Aug 2022 20:53:41 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 09 Aug 2022 20:56:30 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 09 Aug 2022 20:56:30 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 09 Aug 2022 20:56:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 09 Aug 2022 20:56:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 20:56:31 GMT
USER memcache
# Tue, 09 Aug 2022 20:56:31 GMT
EXPOSE 11211
# Tue, 09 Aug 2022 20:56:31 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d572ef57cdf8eb58de4b4e89970c5e64c6a2f8470bbbe4746efd56927df10611`  
		Last Modified: Tue, 09 Aug 2022 20:57:08 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed8976416286665206f17c9c2ead879425c6c6c62051fa7af308abd8790c0bc`  
		Last Modified: Tue, 09 Aug 2022 20:57:08 GMT  
		Size: 108.3 KB (108322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c657d873aa5cf9fbc93f3c3b68b8e7543ec1bc6335404b259ea5a7db4196422d`  
		Last Modified: Tue, 09 Aug 2022 20:57:08 GMT  
		Size: 951.4 KB (951438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f91921ed85e235501e9cd091c8d8601f04ea194fe4a461629fe7ab9eb9badd`  
		Last Modified: Tue, 09 Aug 2022 20:57:08 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198a10264961105745cf7038c02c22ae20695d9213c38421ec14d7cc8eda0d44`  
		Last Modified: Tue, 09 Aug 2022 20:57:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:79a5646a0c845a791f36017fda3292281b48295b06c53f13d62c9f94237d4731
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3960292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2afac0e49af3ce3f1769abe11a29f8f5610c6a736d8c5b6c7b9770c8d8e94e91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 16 Dec 2020 23:58:14 GMT
ADD file:bd07f77a2b2741ca6bda80d9203be9c7274cf73145bff778cf000db0d8d4e903 in / 
# Wed, 16 Dec 2020 23:58:15 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 06:43:29 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Thu, 17 Dec 2020 06:43:31 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Thu, 17 Dec 2020 06:43:33 GMT
ENV MEMCACHED_VERSION=1.6.9
# Thu, 17 Dec 2020 06:43:35 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Thu, 17 Dec 2020 06:46:32 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Thu, 17 Dec 2020 06:46:33 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 17 Dec 2020 06:46:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 17 Dec 2020 06:46:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 06:46:36 GMT
USER memcache
# Thu, 17 Dec 2020 06:46:38 GMT
EXPOSE 11211
# Thu, 17 Dec 2020 06:46:39 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c58e8a26a8407acc3ead776f6526efa889fda03270a8d05109208d9f59159420`  
		Last Modified: Wed, 16 Dec 2020 23:58:59 GMT  
		Size: 2.4 MB (2407555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68564bbfc09f153688e942bf54d5375d1e27f3507c0bed6b038c2ac8ce095aa5`  
		Last Modified: Thu, 17 Dec 2020 06:46:58 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cac3a91edee49d0b08a25706ae86059bed89941a08b496e72ef092e57c4ecb3`  
		Last Modified: Thu, 17 Dec 2020 06:46:58 GMT  
		Size: 13.8 KB (13825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf16e9bb942ec42a35a792beab65aea843209e7bdde7e856499b9fc85f93bc4e`  
		Last Modified: Thu, 17 Dec 2020 06:46:58 GMT  
		Size: 1.5 MB (1537248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc15394239bd0c083e1b6df806aa5ffeb8b9cc7e80113afc2959721de49f90d1`  
		Last Modified: Thu, 17 Dec 2020 06:46:58 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:482f0eb571548eae5720c652ff7da13558e56a8722dc9932cf7eb1ef3eb33acb`  
		Last Modified: Thu, 17 Dec 2020 06:46:58 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:44f0d141458db00ee50b9ad0ec9f39a08f2054fe45924bafddc3920d446727f0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3757682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5799dfb510c6b2e85d9290ef1eae349ba3365b9584932dbc450562979a046d9f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:48:03 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Tue, 09 Aug 2022 20:48:05 GMT
RUN apk add --no-cache libsasl
# Tue, 09 Aug 2022 20:48:05 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 09 Aug 2022 20:48:06 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 09 Aug 2022 20:50:51 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 09 Aug 2022 20:50:53 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 09 Aug 2022 20:50:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 09 Aug 2022 20:50:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 20:50:55 GMT
USER memcache
# Tue, 09 Aug 2022 20:50:56 GMT
EXPOSE 11211
# Tue, 09 Aug 2022 20:50:57 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d15db589ad12df2825238bc4f6832b2c6e3d991704c9b41db7865df5d402276`  
		Last Modified: Tue, 09 Aug 2022 20:51:50 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103b4be7608736e9e24d225ccd97cc4dfad6bacbe7bcf2ca1cd716b45ee32855`  
		Last Modified: Tue, 09 Aug 2022 20:51:50 GMT  
		Size: 109.6 KB (109566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be29d81faebb3b793bdb052326cbb181f786eb99078f62f6f00935c60c14a9fe`  
		Last Modified: Tue, 09 Aug 2022 20:51:50 GMT  
		Size: 938.8 KB (938808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a590dbe104d4e1ec4c488c22500f75e3b44977e09523893500694356ff65008b`  
		Last Modified: Tue, 09 Aug 2022 20:51:50 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da7fd81bf28f2c80e4823f86aea754145c41614f1a924f56f0d2f7e51747873`  
		Last Modified: Tue, 09 Aug 2022 20:51:50 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:alpine` - linux; 386

```console
$ docker pull memcached@sha256:e6fc7462999869fb634dbc73338735811a34ba127cbf512785b2d036132b7496
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3891350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b662b6ea7b7b0638994baa098f88f7a247ecc3da8fa1057e586dd3fdd1fe007`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Aug 2022 17:38:39 GMT
ADD file:b828bc14bc5ff03c8f7310fe0aed6ac5df19a393622d5d1d779a523234d07c0a in / 
# Tue, 09 Aug 2022 17:38:39 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:34:01 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Tue, 09 Aug 2022 18:34:02 GMT
RUN apk add --no-cache libsasl
# Tue, 09 Aug 2022 18:34:03 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 09 Aug 2022 18:34:04 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 09 Aug 2022 18:37:07 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 09 Aug 2022 18:37:09 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 09 Aug 2022 18:37:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 09 Aug 2022 18:37:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 18:37:11 GMT
USER memcache
# Tue, 09 Aug 2022 18:37:12 GMT
EXPOSE 11211
# Tue, 09 Aug 2022 18:37:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6c0d3b419d848ea31ca748254611d5d5ce3b76e3d7bba520fd87400fbb75f3b9`  
		Last Modified: Tue, 09 Aug 2022 17:39:33 GMT  
		Size: 2.8 MB (2807121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:240e236335200614c944d9ba79e2d7eda5cfa258a69e669b585cc28314d754f5`  
		Last Modified: Tue, 09 Aug 2022 18:38:05 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:844d1ba63a22190468423984b12b7d36f6c005e3316461b983f975f4b8dc9ee8`  
		Last Modified: Tue, 09 Aug 2022 18:38:05 GMT  
		Size: 119.8 KB (119826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad6d3cd2261a998624eba6805148058d37a9733e41f66cef88d3b5103170e4a8`  
		Last Modified: Tue, 09 Aug 2022 18:38:06 GMT  
		Size: 962.8 KB (962759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7983bf58c38f033ac9ab3011fd046fa03cb7848d5b2fb86955fd5e20c62e27fc`  
		Last Modified: Tue, 09 Aug 2022 18:38:05 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a108c54c3e573033e837b18319fbbfab59f4bbca1dfd29610c5be85ad2ea1bc9`  
		Last Modified: Tue, 09 Aug 2022 18:38:05 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:d798237b2695cb4cdcde6ad5c5ebeb01b03cb86bd534f5ef703d8b88c3f60db1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3912215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfb1d9b800eeba8d9cadba9dfee6f8b7db71228a7f42e7fd208109e6f8d33a2e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Aug 2022 17:17:09 GMT
ADD file:66b351666e41834033d334aeb3dc6998dea77aa22e8e254028c923fee67a41a8 in / 
# Tue, 09 Aug 2022 17:17:10 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:48:17 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Tue, 09 Aug 2022 18:48:19 GMT
RUN apk add --no-cache libsasl
# Tue, 09 Aug 2022 18:48:19 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 09 Aug 2022 18:48:19 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 09 Aug 2022 18:51:34 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 09 Aug 2022 18:51:34 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 09 Aug 2022 18:51:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 09 Aug 2022 18:51:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 18:51:36 GMT
USER memcache
# Tue, 09 Aug 2022 18:51:36 GMT
EXPOSE 11211
# Tue, 09 Aug 2022 18:51:37 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c79e5d1a8c89b87020a754c8a5c8370faaa37bfb5bca1d8af66770d522ef1caf`  
		Last Modified: Tue, 09 Aug 2022 17:18:26 GMT  
		Size: 2.8 MB (2803320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086c869249c97411ce380e3b76305e0b85731874d0ea57dfd0de74e1f387443d`  
		Last Modified: Tue, 09 Aug 2022 18:52:28 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75e55886182590f2e7eef7f1c21851fd9c322339484e8345afd12376d976ddbd`  
		Last Modified: Tue, 09 Aug 2022 18:52:28 GMT  
		Size: 126.1 KB (126064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5986c4b1340bf1f46f9c87bfe46749c8b2c36b125cc144d44369ffa6da235643`  
		Last Modified: Tue, 09 Aug 2022 18:52:29 GMT  
		Size: 981.2 KB (981160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94057389e17fb62c8067389939b22ba89063219c50a7a348d0343d3aee37d933`  
		Last Modified: Tue, 09 Aug 2022 18:52:28 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989f24ebe1a18ca3cac84b41e1b10934fc83856828b9fb1da76a8d894048512e`  
		Last Modified: Tue, 09 Aug 2022 18:52:28 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:alpine` - linux; s390x

```console
$ docker pull memcached@sha256:f05c64785454795713f41d5cf814a5debb9cf42c3d4d1b6298ba93d897cfc72a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3646606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef9e9b1c8f1ad73aa6d447c3635fa404bffc5d074a3480ae8644c2ae121a39af`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Aug 2022 17:41:46 GMT
ADD file:b43a065471bc4711415d3c67cd5b6559b0c48ee7ffe9761530477cf457a6dc34 in / 
# Tue, 09 Aug 2022 17:41:46 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 19:11:19 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Tue, 09 Aug 2022 19:11:20 GMT
RUN apk add --no-cache libsasl
# Tue, 09 Aug 2022 19:11:20 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 09 Aug 2022 19:11:20 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 09 Aug 2022 19:14:45 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 09 Aug 2022 19:14:45 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 09 Aug 2022 19:14:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 09 Aug 2022 19:14:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 19:14:46 GMT
USER memcache
# Tue, 09 Aug 2022 19:14:46 GMT
EXPOSE 11211
# Tue, 09 Aug 2022 19:14:46 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:790c84f1f3409eab952345157df7fa804ba6b5f06d4ceb6f2dfa3c6de2064397`  
		Last Modified: Tue, 09 Aug 2022 17:42:45 GMT  
		Size: 2.6 MB (2590597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:463a70f3df946e83a223bd55002470af1b7f8d483babe452e515a809b965d35c`  
		Last Modified: Tue, 09 Aug 2022 19:15:35 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df0b8be6e73cbbdde959ca7a21d3fd6c8e36e05bc9c7a46be4e5bfa5b664a50c`  
		Last Modified: Tue, 09 Aug 2022 19:15:35 GMT  
		Size: 112.5 KB (112508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f39508191d6e035471ed454d54a8ec05b775ff26d4e6902076dd66901c870fd4`  
		Last Modified: Tue, 09 Aug 2022 19:15:35 GMT  
		Size: 941.8 KB (941827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:664e864043941612ce16890523ab6ef1ca3d7a253f0384d99b2e0c3957b6398f`  
		Last Modified: Tue, 09 Aug 2022 19:15:35 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f2ba1910d2ededf72d427c17c6dd473de7acc0ad7513e183ab5c4c3a0c43142`  
		Last Modified: Tue, 09 Aug 2022 19:15:35 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:alpine3.16`

```console
$ docker pull memcached@sha256:22fd822b2417986f627bd96bc687e85360200db73e8bc818fe6ffdfe1f24e413
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `memcached:alpine3.16` - linux; amd64

```console
$ docker pull memcached@sha256:b1e59612ccc1ab79ccb764e8ae694c89c6e2dece9927b202c1a1820a665268f4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3867486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af3c4fe62d9dafd4336d17fc19dcc8e0ea69a41c4ea586e0544c371319a9497b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:53:39 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Tue, 09 Aug 2022 20:53:40 GMT
RUN apk add --no-cache libsasl
# Tue, 09 Aug 2022 20:53:40 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 09 Aug 2022 20:53:41 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 09 Aug 2022 20:56:30 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 09 Aug 2022 20:56:30 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 09 Aug 2022 20:56:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 09 Aug 2022 20:56:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 20:56:31 GMT
USER memcache
# Tue, 09 Aug 2022 20:56:31 GMT
EXPOSE 11211
# Tue, 09 Aug 2022 20:56:31 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d572ef57cdf8eb58de4b4e89970c5e64c6a2f8470bbbe4746efd56927df10611`  
		Last Modified: Tue, 09 Aug 2022 20:57:08 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed8976416286665206f17c9c2ead879425c6c6c62051fa7af308abd8790c0bc`  
		Last Modified: Tue, 09 Aug 2022 20:57:08 GMT  
		Size: 108.3 KB (108322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c657d873aa5cf9fbc93f3c3b68b8e7543ec1bc6335404b259ea5a7db4196422d`  
		Last Modified: Tue, 09 Aug 2022 20:57:08 GMT  
		Size: 951.4 KB (951438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f91921ed85e235501e9cd091c8d8601f04ea194fe4a461629fe7ab9eb9badd`  
		Last Modified: Tue, 09 Aug 2022 20:57:08 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198a10264961105745cf7038c02c22ae20695d9213c38421ec14d7cc8eda0d44`  
		Last Modified: Tue, 09 Aug 2022 20:57:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:alpine3.16` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:44f0d141458db00ee50b9ad0ec9f39a08f2054fe45924bafddc3920d446727f0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3757682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5799dfb510c6b2e85d9290ef1eae349ba3365b9584932dbc450562979a046d9f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:48:03 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Tue, 09 Aug 2022 20:48:05 GMT
RUN apk add --no-cache libsasl
# Tue, 09 Aug 2022 20:48:05 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 09 Aug 2022 20:48:06 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 09 Aug 2022 20:50:51 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 09 Aug 2022 20:50:53 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 09 Aug 2022 20:50:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 09 Aug 2022 20:50:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 20:50:55 GMT
USER memcache
# Tue, 09 Aug 2022 20:50:56 GMT
EXPOSE 11211
# Tue, 09 Aug 2022 20:50:57 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d15db589ad12df2825238bc4f6832b2c6e3d991704c9b41db7865df5d402276`  
		Last Modified: Tue, 09 Aug 2022 20:51:50 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103b4be7608736e9e24d225ccd97cc4dfad6bacbe7bcf2ca1cd716b45ee32855`  
		Last Modified: Tue, 09 Aug 2022 20:51:50 GMT  
		Size: 109.6 KB (109566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be29d81faebb3b793bdb052326cbb181f786eb99078f62f6f00935c60c14a9fe`  
		Last Modified: Tue, 09 Aug 2022 20:51:50 GMT  
		Size: 938.8 KB (938808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a590dbe104d4e1ec4c488c22500f75e3b44977e09523893500694356ff65008b`  
		Last Modified: Tue, 09 Aug 2022 20:51:50 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da7fd81bf28f2c80e4823f86aea754145c41614f1a924f56f0d2f7e51747873`  
		Last Modified: Tue, 09 Aug 2022 20:51:50 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:alpine3.16` - linux; 386

```console
$ docker pull memcached@sha256:e6fc7462999869fb634dbc73338735811a34ba127cbf512785b2d036132b7496
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3891350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b662b6ea7b7b0638994baa098f88f7a247ecc3da8fa1057e586dd3fdd1fe007`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Aug 2022 17:38:39 GMT
ADD file:b828bc14bc5ff03c8f7310fe0aed6ac5df19a393622d5d1d779a523234d07c0a in / 
# Tue, 09 Aug 2022 17:38:39 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:34:01 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Tue, 09 Aug 2022 18:34:02 GMT
RUN apk add --no-cache libsasl
# Tue, 09 Aug 2022 18:34:03 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 09 Aug 2022 18:34:04 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 09 Aug 2022 18:37:07 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 09 Aug 2022 18:37:09 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 09 Aug 2022 18:37:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 09 Aug 2022 18:37:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 18:37:11 GMT
USER memcache
# Tue, 09 Aug 2022 18:37:12 GMT
EXPOSE 11211
# Tue, 09 Aug 2022 18:37:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6c0d3b419d848ea31ca748254611d5d5ce3b76e3d7bba520fd87400fbb75f3b9`  
		Last Modified: Tue, 09 Aug 2022 17:39:33 GMT  
		Size: 2.8 MB (2807121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:240e236335200614c944d9ba79e2d7eda5cfa258a69e669b585cc28314d754f5`  
		Last Modified: Tue, 09 Aug 2022 18:38:05 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:844d1ba63a22190468423984b12b7d36f6c005e3316461b983f975f4b8dc9ee8`  
		Last Modified: Tue, 09 Aug 2022 18:38:05 GMT  
		Size: 119.8 KB (119826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad6d3cd2261a998624eba6805148058d37a9733e41f66cef88d3b5103170e4a8`  
		Last Modified: Tue, 09 Aug 2022 18:38:06 GMT  
		Size: 962.8 KB (962759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7983bf58c38f033ac9ab3011fd046fa03cb7848d5b2fb86955fd5e20c62e27fc`  
		Last Modified: Tue, 09 Aug 2022 18:38:05 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a108c54c3e573033e837b18319fbbfab59f4bbca1dfd29610c5be85ad2ea1bc9`  
		Last Modified: Tue, 09 Aug 2022 18:38:05 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:alpine3.16` - linux; ppc64le

```console
$ docker pull memcached@sha256:d798237b2695cb4cdcde6ad5c5ebeb01b03cb86bd534f5ef703d8b88c3f60db1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3912215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfb1d9b800eeba8d9cadba9dfee6f8b7db71228a7f42e7fd208109e6f8d33a2e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Aug 2022 17:17:09 GMT
ADD file:66b351666e41834033d334aeb3dc6998dea77aa22e8e254028c923fee67a41a8 in / 
# Tue, 09 Aug 2022 17:17:10 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:48:17 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Tue, 09 Aug 2022 18:48:19 GMT
RUN apk add --no-cache libsasl
# Tue, 09 Aug 2022 18:48:19 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 09 Aug 2022 18:48:19 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 09 Aug 2022 18:51:34 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 09 Aug 2022 18:51:34 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 09 Aug 2022 18:51:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 09 Aug 2022 18:51:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 18:51:36 GMT
USER memcache
# Tue, 09 Aug 2022 18:51:36 GMT
EXPOSE 11211
# Tue, 09 Aug 2022 18:51:37 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c79e5d1a8c89b87020a754c8a5c8370faaa37bfb5bca1d8af66770d522ef1caf`  
		Last Modified: Tue, 09 Aug 2022 17:18:26 GMT  
		Size: 2.8 MB (2803320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086c869249c97411ce380e3b76305e0b85731874d0ea57dfd0de74e1f387443d`  
		Last Modified: Tue, 09 Aug 2022 18:52:28 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75e55886182590f2e7eef7f1c21851fd9c322339484e8345afd12376d976ddbd`  
		Last Modified: Tue, 09 Aug 2022 18:52:28 GMT  
		Size: 126.1 KB (126064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5986c4b1340bf1f46f9c87bfe46749c8b2c36b125cc144d44369ffa6da235643`  
		Last Modified: Tue, 09 Aug 2022 18:52:29 GMT  
		Size: 981.2 KB (981160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94057389e17fb62c8067389939b22ba89063219c50a7a348d0343d3aee37d933`  
		Last Modified: Tue, 09 Aug 2022 18:52:28 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989f24ebe1a18ca3cac84b41e1b10934fc83856828b9fb1da76a8d894048512e`  
		Last Modified: Tue, 09 Aug 2022 18:52:28 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:alpine3.16` - linux; s390x

```console
$ docker pull memcached@sha256:f05c64785454795713f41d5cf814a5debb9cf42c3d4d1b6298ba93d897cfc72a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3646606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef9e9b1c8f1ad73aa6d447c3635fa404bffc5d074a3480ae8644c2ae121a39af`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Aug 2022 17:41:46 GMT
ADD file:b43a065471bc4711415d3c67cd5b6559b0c48ee7ffe9761530477cf457a6dc34 in / 
# Tue, 09 Aug 2022 17:41:46 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 19:11:19 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Tue, 09 Aug 2022 19:11:20 GMT
RUN apk add --no-cache libsasl
# Tue, 09 Aug 2022 19:11:20 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 09 Aug 2022 19:11:20 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 09 Aug 2022 19:14:45 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Tue, 09 Aug 2022 19:14:45 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 09 Aug 2022 19:14:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 09 Aug 2022 19:14:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 19:14:46 GMT
USER memcache
# Tue, 09 Aug 2022 19:14:46 GMT
EXPOSE 11211
# Tue, 09 Aug 2022 19:14:46 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:790c84f1f3409eab952345157df7fa804ba6b5f06d4ceb6f2dfa3c6de2064397`  
		Last Modified: Tue, 09 Aug 2022 17:42:45 GMT  
		Size: 2.6 MB (2590597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:463a70f3df946e83a223bd55002470af1b7f8d483babe452e515a809b965d35c`  
		Last Modified: Tue, 09 Aug 2022 19:15:35 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df0b8be6e73cbbdde959ca7a21d3fd6c8e36e05bc9c7a46be4e5bfa5b664a50c`  
		Last Modified: Tue, 09 Aug 2022 19:15:35 GMT  
		Size: 112.5 KB (112508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f39508191d6e035471ed454d54a8ec05b775ff26d4e6902076dd66901c870fd4`  
		Last Modified: Tue, 09 Aug 2022 19:15:35 GMT  
		Size: 941.8 KB (941827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:664e864043941612ce16890523ab6ef1ca3d7a253f0384d99b2e0c3957b6398f`  
		Last Modified: Tue, 09 Aug 2022 19:15:35 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f2ba1910d2ededf72d427c17c6dd473de7acc0ad7513e183ab5c4c3a0c43142`  
		Last Modified: Tue, 09 Aug 2022 19:15:35 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:bullseye`

```console
$ docker pull memcached@sha256:22ed710ee778c797865ebff08e825df55df20508075cf275311cca55a235e652
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `memcached:bullseye` - linux; amd64

```console
$ docker pull memcached@sha256:a5dc74cbb9f905192c3caa290e32a4c725aba0d21f94c15cd7ca8530ffe01776
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32970763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdff4547b1b7092afe2104dbf710a439a2b8bcdf54b87fbfda0de4631da4ef6a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Aug 2022 00:20:50 GMT
ADD file:7726efb0e0eb5003dbcf2967ec29364479eec8b41f2569ff189372153115b54b in / 
# Tue, 23 Aug 2022 00:20:51 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 02:54:26 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 23 Aug 2022 02:54:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 02:54:30 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 23 Aug 2022 02:54:30 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 23 Aug 2022 02:57:13 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 23 Aug 2022 02:57:13 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 23 Aug 2022 02:57:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 23 Aug 2022 02:57:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 02:57:14 GMT
USER memcache
# Tue, 23 Aug 2022 02:57:14 GMT
EXPOSE 11211
# Tue, 23 Aug 2022 02:57:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7a6db449b51b92eac5c81cdbd82917785343f1664b2be57b22337b0a40c5b29d`  
		Last Modified: Tue, 23 Aug 2022 00:24:59 GMT  
		Size: 31.4 MB (31381485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa73fb65ea8b12a2375459f0d656d3ad06e2863c906fcf962486eda3701f3fd6`  
		Last Modified: Tue, 23 Aug 2022 02:57:38 GMT  
		Size: 5.0 KB (4981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:502b4e8803067b28098d0ea52281cfef66da1ee1e869241612b545d7e9ff12de`  
		Last Modified: Tue, 23 Aug 2022 02:57:38 GMT  
		Size: 328.1 KB (328108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4be7903a0371d25a8e62fb8f58db1b4cc0d71407206895e81b2c5edddd96716`  
		Last Modified: Tue, 23 Aug 2022 02:57:38 GMT  
		Size: 1.3 MB (1255782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ece99ce94967ae22a842630bc182d3052a46922074b332055aa65763b70c4adb`  
		Last Modified: Tue, 23 Aug 2022 02:57:37 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72302fb7547064b5cd2773f9e54e03b6579b64dc8399245d683058505e87860`  
		Last Modified: Tue, 23 Aug 2022 02:57:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:bullseye` - linux; arm variant v5

```console
$ docker pull memcached@sha256:7688ba62a1e2ca12e4fcfc18213eec8b6c8e967bb62395189bdc8d1b095f9ec8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 MB (30466108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63aeac5a0551e3a97aaddf116dbcb2a96b84635664ff3755675a42744590c23c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Aug 2022 01:17:14 GMT
ADD file:83fb076a50e935419eb0db2bd97477d7ed5f16aaac4c8cc35a4a69ac612df327 in / 
# Tue, 23 Aug 2022 01:17:14 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 01:49:29 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 23 Aug 2022 01:49:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 01:49:33 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 23 Aug 2022 01:49:34 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 23 Aug 2022 01:55:05 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 23 Aug 2022 01:55:05 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 23 Aug 2022 01:55:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 23 Aug 2022 01:55:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 01:55:06 GMT
USER memcache
# Tue, 23 Aug 2022 01:55:06 GMT
EXPOSE 11211
# Tue, 23 Aug 2022 01:55:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:74eb5afab626122970f8620ac001fcc4a200725acb05519b85aba47a38bf1016`  
		Last Modified: Tue, 23 Aug 2022 01:22:44 GMT  
		Size: 28.9 MB (28917250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a1b82f1abc9998be67c6dab29a896fcf5377c55fa3c09f0f60355321d0cc7e`  
		Last Modified: Tue, 23 Aug 2022 01:55:43 GMT  
		Size: 4.9 KB (4896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8d24ffcddd09d398cd33e29661cc865588572fdcfc4224b2ea8c0d1d001ed6`  
		Last Modified: Tue, 23 Aug 2022 01:55:44 GMT  
		Size: 316.6 KB (316628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:099cd43abb1475212736fcbb1adbd31b235ae10d1cbd4785e375473e77218967`  
		Last Modified: Tue, 23 Aug 2022 01:55:44 GMT  
		Size: 1.2 MB (1226927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b9006a418f2ced9ced0ca431dda2ce3543860c17742fc092a2309af44e78f22`  
		Last Modified: Tue, 23 Aug 2022 01:55:43 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df94046aab5da41252820ad1cb5d98c7a10c344be39148a95f1d6ad9e052bc1b`  
		Last Modified: Tue, 23 Aug 2022 01:55:44 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:bullseye` - linux; arm variant v7

```console
$ docker pull memcached@sha256:25e768546f1e321b2a9031611f8ecd4081990c82f8774f7e051a5480cf18445d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28076294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5959e4e12e1b75611311d3866bc95f9fe30048418f972e70fa2c671a66149fdd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 02 Aug 2022 00:58:59 GMT
ADD file:1575b776a15adacebc0875642e97a80807d42dcfc8917e1406d47af7ac244c97 in / 
# Tue, 02 Aug 2022 00:58:59 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 06:28:56 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 02 Aug 2022 06:29:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Aug 2022 21:30:08 GMT
ENV MEMCACHED_VERSION=1.6.16
# Thu, 04 Aug 2022 21:30:08 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Thu, 04 Aug 2022 21:36:35 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Thu, 04 Aug 2022 21:36:35 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 04 Aug 2022 21:36:36 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 04 Aug 2022 21:36:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Aug 2022 21:36:37 GMT
USER memcache
# Thu, 04 Aug 2022 21:36:37 GMT
EXPOSE 11211
# Thu, 04 Aug 2022 21:36:37 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1dd75a3a9c893a7dc313f683dd62464b7eab6c6d522ee62c8a17022631830f32`  
		Last Modified: Tue, 02 Aug 2022 01:06:45 GMT  
		Size: 26.6 MB (26560586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44a675a8ce135f198539dc76b078733393238f7c7b899c8635980eed8f35f1cc`  
		Last Modified: Tue, 02 Aug 2022 09:35:13 GMT  
		Size: 4.9 KB (4890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497b0afd04c92a1e5d41f58dbc0d5d544b8880d000c0ffbd03adb48c32c0116b`  
		Last Modified: Tue, 02 Aug 2022 09:35:13 GMT  
		Size: 312.1 KB (312067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8874fe992be272d0e0780725714c2439507699c15bfad1a073df948a34eb668d`  
		Last Modified: Fri, 05 Aug 2022 00:37:30 GMT  
		Size: 1.2 MB (1198344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cd5e042b98c640c152a56816e122c5e7b0abe91535d5d891dceed9748e42129`  
		Last Modified: Fri, 05 Aug 2022 00:37:29 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e871a0f93bdc7cb723e47f45514f914186b73d1890a53cdfe8525dd034926d59`  
		Last Modified: Fri, 05 Aug 2022 00:37:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:bullseye` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:759082b00d406f92781542ce86756eb73c5efe20acc7df6c25ac86be320a3ef5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31433439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e91fe6663d9d90deed07c1d003a80fa6698137267c83310828f24a7ef63f6ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 02 Aug 2022 00:40:38 GMT
ADD file:6039adfbca55ed34a719c37672c664e3524130a0e2a3b8663629b8120b81b790 in / 
# Tue, 02 Aug 2022 00:40:39 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 03:56:15 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 02 Aug 2022 03:56:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Aug 2022 20:33:46 GMT
ENV MEMCACHED_VERSION=1.6.16
# Thu, 04 Aug 2022 20:33:47 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Thu, 04 Aug 2022 20:36:17 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Thu, 04 Aug 2022 20:36:19 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 04 Aug 2022 20:36:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 04 Aug 2022 20:36:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Aug 2022 20:36:21 GMT
USER memcache
# Thu, 04 Aug 2022 20:36:22 GMT
EXPOSE 11211
# Thu, 04 Aug 2022 20:36:23 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a9fe95647e78b5516c7e2327355b6996e2ea295cd76ae242cbfe87f016b4e760`  
		Last Modified: Tue, 02 Aug 2022 00:46:05 GMT  
		Size: 30.1 MB (30054304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b983df009e7dc88033f53f015c09c56fd4db032d1abcade3333d8d4b515ff4af`  
		Last Modified: Tue, 02 Aug 2022 03:59:48 GMT  
		Size: 4.9 KB (4902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60720019405b50af041f391ec7dad90893ee95fc63fd6b3fb9da04850936f5db`  
		Last Modified: Tue, 02 Aug 2022 03:59:48 GMT  
		Size: 119.2 KB (119225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70569bedb4ee539337d6d3fd88e4076a1464b3a77bcfcca6604e18b815dbc402`  
		Last Modified: Thu, 04 Aug 2022 20:40:00 GMT  
		Size: 1.3 MB (1254600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:565112c01ad7b82688180f4fe70f5433126d79cc4b74e3d7f308601e2d34d9fe`  
		Last Modified: Thu, 04 Aug 2022 20:39:59 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce11290eb88924797c1fa048bd052c1243e4cb47e3469b26f3f1a3bc26472d19`  
		Last Modified: Thu, 04 Aug 2022 20:39:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:bullseye` - linux; 386

```console
$ docker pull memcached@sha256:3770f2e3c3f2abb5f85a6a615e62fd5c78a61513ca573ee4385adf42629bd88c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.8 MB (33775724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2804b930e07f367a1e5adc6a5631e87c78a986d3ad64e06e3c549c20ad7ce735`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Aug 2022 01:02:40 GMT
ADD file:5ca62c98116941aaa64ec72afb689a088c46f75a3e83d5b0d4e58d65ec905ccd in / 
# Tue, 23 Aug 2022 01:02:40 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 03:22:44 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 23 Aug 2022 03:22:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 03:22:49 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 23 Aug 2022 03:22:50 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 23 Aug 2022 03:26:54 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 23 Aug 2022 03:26:56 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 23 Aug 2022 03:26:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 23 Aug 2022 03:26:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 03:26:58 GMT
USER memcache
# Tue, 23 Aug 2022 03:26:59 GMT
EXPOSE 11211
# Tue, 23 Aug 2022 03:27:00 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6b3cb4a05a891d9d8a87a2bd7247b16f79832a9d4afbad3ff5068f6fc2ba1560`  
		Last Modified: Tue, 23 Aug 2022 01:08:25 GMT  
		Size: 32.4 MB (32387317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd24201e0b5e9a68a67bdc3b464a01aeb9a2e5a859a582cdaa80ab08a608337`  
		Last Modified: Tue, 23 Aug 2022 03:27:47 GMT  
		Size: 4.8 KB (4774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3070e5e3b1d98fa0b67b8390880b7596c4719b774864de21f36ed86873041793`  
		Last Modified: Tue, 23 Aug 2022 03:27:48 GMT  
		Size: 130.1 KB (130136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a076923bc48ef00816393d79ac2aa3ad931f47309aff7a6cf0c6c74d443080f`  
		Last Modified: Tue, 23 Aug 2022 03:27:48 GMT  
		Size: 1.3 MB (1253091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7169b397a99c6597495d00b3cb6b04483b8950d04bc7cbdcccf983f225294bb4`  
		Last Modified: Tue, 23 Aug 2022 03:27:48 GMT  
		Size: 288.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55ee497fd4fa66154f7c38bc2bb37f6e356318dc032b26ed65eb94ddc8355995`  
		Last Modified: Tue, 23 Aug 2022 03:27:47 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:bullseye` - linux; mips64le

```console
$ docker pull memcached@sha256:0d6798ccd4a9ac44c6ca7c358b2de6bdedbfe104de7d9987eedc68864ab8acc0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 MB (31002934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aca3e1ecca25fb97ad1d376d73b212cad11874d1f051c4c4bac1b2d27abc15fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 02 Aug 2022 01:10:34 GMT
ADD file:6dc22a1e5b5fcf23f2549406ddcc45c4e244f46e21eafa881de81fa87438e5d8 in / 
# Tue, 02 Aug 2022 01:10:38 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 03:22:53 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 02 Aug 2022 03:23:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Aug 2022 20:07:25 GMT
ENV MEMCACHED_VERSION=1.6.16
# Thu, 04 Aug 2022 20:07:28 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Thu, 04 Aug 2022 20:14:28 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Thu, 04 Aug 2022 20:14:30 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 04 Aug 2022 20:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 04 Aug 2022 20:14:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Aug 2022 20:14:40 GMT
USER memcache
# Thu, 04 Aug 2022 20:14:42 GMT
EXPOSE 11211
# Thu, 04 Aug 2022 20:14:45 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:88350749a27614c791450c256b051f023d81cdd256211274b1efac493779d2be`  
		Last Modified: Tue, 02 Aug 2022 01:21:02 GMT  
		Size: 29.6 MB (29628964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:117af7bbaadea9c81bbaa3a8a77b1ab5cd05bcac856c462cda2e81c9a40596ab`  
		Last Modified: Tue, 02 Aug 2022 03:30:45 GMT  
		Size: 4.9 KB (4863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a16d313748bd6b2dade87de73d79edd8a08e4cb662769a717f8587abc8d5e0`  
		Last Modified: Tue, 02 Aug 2022 03:30:46 GMT  
		Size: 117.1 KB (117127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d524786af3243ee367d118f6d5260cffa06d800f492f9b4bb36c910958186933`  
		Last Modified: Thu, 04 Aug 2022 20:15:05 GMT  
		Size: 1.3 MB (1251571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4badb1f1970762d08dbd43d7e101081a5fabd3c45e18afd70636397e83102d2f`  
		Last Modified: Thu, 04 Aug 2022 20:15:04 GMT  
		Size: 288.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3102636392803c3bbff48f39e7f143e3bf9a0528365d63b90dc31cd32060d3e0`  
		Last Modified: Thu, 04 Aug 2022 20:15:04 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:bullseye` - linux; ppc64le

```console
$ docker pull memcached@sha256:6eac50a2d123c021e75657700bdd2d0335dcc97db595e783eb6feaf81e0d6ab0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 MB (36969051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77075f2945ec5e196ccf20148829ebe266a384c2972f723f72361e05e3ee1bf5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Aug 2022 01:24:52 GMT
ADD file:d35213360d726a18e220276d33f245115c3e94a321addaa4c9127488368b0203 in / 
# Tue, 23 Aug 2022 01:24:54 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 02:34:49 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 23 Aug 2022 02:34:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 02:34:56 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 23 Aug 2022 02:34:56 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 23 Aug 2022 02:38:10 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 23 Aug 2022 02:38:10 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 23 Aug 2022 02:38:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 23 Aug 2022 02:38:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 02:38:12 GMT
USER memcache
# Tue, 23 Aug 2022 02:38:12 GMT
EXPOSE 11211
# Tue, 23 Aug 2022 02:38:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:698954eda09d38dd1ccc9ce777b1f6bc7f7473fc6c4c3eb634acc8d035a42eae`  
		Last Modified: Tue, 23 Aug 2022 01:30:36 GMT  
		Size: 35.3 MB (35284280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ffb080d920662043edc67113c0de4c68258ad19c0fffd9e3b79fa01800c6015`  
		Last Modified: Tue, 23 Aug 2022 02:39:09 GMT  
		Size: 5.0 KB (4980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b1f66b68991d8f5ab064b3988db37a48b8f28b4ef0eb8e83efa4c419b630ff`  
		Last Modified: Tue, 23 Aug 2022 02:39:09 GMT  
		Size: 356.9 KB (356931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9653070548c34c29ed693878ef68223dbe9ccefc4653b86d3c8225bc8f85ac1`  
		Last Modified: Tue, 23 Aug 2022 02:39:09 GMT  
		Size: 1.3 MB (1322453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd51b501bab55d128a547f5c14e6410e4ef4b7b08f1867c7c933db716d7791e7`  
		Last Modified: Tue, 23 Aug 2022 02:39:09 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e693f7e8dfc8fe4a2af505658484b885fe097586d4f22c43aaf8278756e76ca`  
		Last Modified: Tue, 23 Aug 2022 02:39:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:bullseye` - linux; s390x

```console
$ docker pull memcached@sha256:4f7e9706bfd16d98bfb48a6435c8359a167ab733777f16f24996cad3f431bdc5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31211398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6739ca31062c74398fdfec102afbacead1c25fa0decf2fa14bdecdcb6b160543`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 02 Aug 2022 00:42:27 GMT
ADD file:c2afc8990930846fbe7c99bfdfe9ea562c75feb6e3c9122431f7c9f8b5e51a7f in / 
# Tue, 02 Aug 2022 00:42:29 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 02:37:02 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 02 Aug 2022 02:37:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Aug 2022 20:28:18 GMT
ENV MEMCACHED_VERSION=1.6.16
# Thu, 04 Aug 2022 20:28:18 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Thu, 04 Aug 2022 20:31:37 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Thu, 04 Aug 2022 20:31:37 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 04 Aug 2022 20:31:37 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 04 Aug 2022 20:31:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Aug 2022 20:31:38 GMT
USER memcache
# Thu, 04 Aug 2022 20:31:38 GMT
EXPOSE 11211
# Thu, 04 Aug 2022 20:31:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:026d311d0716db60eba0572ea784c21031f420960510cebcc383dc53949b4db8`  
		Last Modified: Tue, 02 Aug 2022 00:48:01 GMT  
		Size: 29.6 MB (29640259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0ffdb328e548bd6b6311c78665ac8cd3be8f0b2e09691701d9b0bae0924f8f5`  
		Last Modified: Tue, 02 Aug 2022 02:41:16 GMT  
		Size: 5.0 KB (5025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fbb9677007b0ebab2fe6feab520da1962d3fcffb3490aa844681a46fcb35749`  
		Last Modified: Tue, 02 Aug 2022 02:41:16 GMT  
		Size: 324.2 KB (324183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9c93abfa1f832f2e1f02fbe7b9a489735142c2051dafa7af20d985ff2e2106b`  
		Last Modified: Thu, 04 Aug 2022 20:36:17 GMT  
		Size: 1.2 MB (1241523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f78bf4cf172bedc6ad3c92b859859b10c0394104262328d5664ddc0b1488b29`  
		Last Modified: Thu, 04 Aug 2022 20:36:17 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6a26d2d4c34166613098e1380842f1355b534e2335a1dea2128c193b7f19bec`  
		Last Modified: Thu, 04 Aug 2022 20:36:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:latest`

```console
$ docker pull memcached@sha256:22ed710ee778c797865ebff08e825df55df20508075cf275311cca55a235e652
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
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
$ docker pull memcached@sha256:a5dc74cbb9f905192c3caa290e32a4c725aba0d21f94c15cd7ca8530ffe01776
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32970763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdff4547b1b7092afe2104dbf710a439a2b8bcdf54b87fbfda0de4631da4ef6a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Aug 2022 00:20:50 GMT
ADD file:7726efb0e0eb5003dbcf2967ec29364479eec8b41f2569ff189372153115b54b in / 
# Tue, 23 Aug 2022 00:20:51 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 02:54:26 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 23 Aug 2022 02:54:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 02:54:30 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 23 Aug 2022 02:54:30 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 23 Aug 2022 02:57:13 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 23 Aug 2022 02:57:13 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 23 Aug 2022 02:57:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 23 Aug 2022 02:57:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 02:57:14 GMT
USER memcache
# Tue, 23 Aug 2022 02:57:14 GMT
EXPOSE 11211
# Tue, 23 Aug 2022 02:57:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7a6db449b51b92eac5c81cdbd82917785343f1664b2be57b22337b0a40c5b29d`  
		Last Modified: Tue, 23 Aug 2022 00:24:59 GMT  
		Size: 31.4 MB (31381485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa73fb65ea8b12a2375459f0d656d3ad06e2863c906fcf962486eda3701f3fd6`  
		Last Modified: Tue, 23 Aug 2022 02:57:38 GMT  
		Size: 5.0 KB (4981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:502b4e8803067b28098d0ea52281cfef66da1ee1e869241612b545d7e9ff12de`  
		Last Modified: Tue, 23 Aug 2022 02:57:38 GMT  
		Size: 328.1 KB (328108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4be7903a0371d25a8e62fb8f58db1b4cc0d71407206895e81b2c5edddd96716`  
		Last Modified: Tue, 23 Aug 2022 02:57:38 GMT  
		Size: 1.3 MB (1255782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ece99ce94967ae22a842630bc182d3052a46922074b332055aa65763b70c4adb`  
		Last Modified: Tue, 23 Aug 2022 02:57:37 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72302fb7547064b5cd2773f9e54e03b6579b64dc8399245d683058505e87860`  
		Last Modified: Tue, 23 Aug 2022 02:57:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:latest` - linux; arm variant v5

```console
$ docker pull memcached@sha256:7688ba62a1e2ca12e4fcfc18213eec8b6c8e967bb62395189bdc8d1b095f9ec8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 MB (30466108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63aeac5a0551e3a97aaddf116dbcb2a96b84635664ff3755675a42744590c23c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Aug 2022 01:17:14 GMT
ADD file:83fb076a50e935419eb0db2bd97477d7ed5f16aaac4c8cc35a4a69ac612df327 in / 
# Tue, 23 Aug 2022 01:17:14 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 01:49:29 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 23 Aug 2022 01:49:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 01:49:33 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 23 Aug 2022 01:49:34 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 23 Aug 2022 01:55:05 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 23 Aug 2022 01:55:05 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 23 Aug 2022 01:55:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 23 Aug 2022 01:55:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 01:55:06 GMT
USER memcache
# Tue, 23 Aug 2022 01:55:06 GMT
EXPOSE 11211
# Tue, 23 Aug 2022 01:55:06 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:74eb5afab626122970f8620ac001fcc4a200725acb05519b85aba47a38bf1016`  
		Last Modified: Tue, 23 Aug 2022 01:22:44 GMT  
		Size: 28.9 MB (28917250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a1b82f1abc9998be67c6dab29a896fcf5377c55fa3c09f0f60355321d0cc7e`  
		Last Modified: Tue, 23 Aug 2022 01:55:43 GMT  
		Size: 4.9 KB (4896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8d24ffcddd09d398cd33e29661cc865588572fdcfc4224b2ea8c0d1d001ed6`  
		Last Modified: Tue, 23 Aug 2022 01:55:44 GMT  
		Size: 316.6 KB (316628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:099cd43abb1475212736fcbb1adbd31b235ae10d1cbd4785e375473e77218967`  
		Last Modified: Tue, 23 Aug 2022 01:55:44 GMT  
		Size: 1.2 MB (1226927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b9006a418f2ced9ced0ca431dda2ce3543860c17742fc092a2309af44e78f22`  
		Last Modified: Tue, 23 Aug 2022 01:55:43 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df94046aab5da41252820ad1cb5d98c7a10c344be39148a95f1d6ad9e052bc1b`  
		Last Modified: Tue, 23 Aug 2022 01:55:44 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:latest` - linux; arm variant v7

```console
$ docker pull memcached@sha256:25e768546f1e321b2a9031611f8ecd4081990c82f8774f7e051a5480cf18445d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28076294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5959e4e12e1b75611311d3866bc95f9fe30048418f972e70fa2c671a66149fdd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 02 Aug 2022 00:58:59 GMT
ADD file:1575b776a15adacebc0875642e97a80807d42dcfc8917e1406d47af7ac244c97 in / 
# Tue, 02 Aug 2022 00:58:59 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 06:28:56 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 02 Aug 2022 06:29:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Aug 2022 21:30:08 GMT
ENV MEMCACHED_VERSION=1.6.16
# Thu, 04 Aug 2022 21:30:08 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Thu, 04 Aug 2022 21:36:35 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Thu, 04 Aug 2022 21:36:35 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 04 Aug 2022 21:36:36 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 04 Aug 2022 21:36:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Aug 2022 21:36:37 GMT
USER memcache
# Thu, 04 Aug 2022 21:36:37 GMT
EXPOSE 11211
# Thu, 04 Aug 2022 21:36:37 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1dd75a3a9c893a7dc313f683dd62464b7eab6c6d522ee62c8a17022631830f32`  
		Last Modified: Tue, 02 Aug 2022 01:06:45 GMT  
		Size: 26.6 MB (26560586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44a675a8ce135f198539dc76b078733393238f7c7b899c8635980eed8f35f1cc`  
		Last Modified: Tue, 02 Aug 2022 09:35:13 GMT  
		Size: 4.9 KB (4890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497b0afd04c92a1e5d41f58dbc0d5d544b8880d000c0ffbd03adb48c32c0116b`  
		Last Modified: Tue, 02 Aug 2022 09:35:13 GMT  
		Size: 312.1 KB (312067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8874fe992be272d0e0780725714c2439507699c15bfad1a073df948a34eb668d`  
		Last Modified: Fri, 05 Aug 2022 00:37:30 GMT  
		Size: 1.2 MB (1198344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cd5e042b98c640c152a56816e122c5e7b0abe91535d5d891dceed9748e42129`  
		Last Modified: Fri, 05 Aug 2022 00:37:29 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e871a0f93bdc7cb723e47f45514f914186b73d1890a53cdfe8525dd034926d59`  
		Last Modified: Fri, 05 Aug 2022 00:37:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:latest` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:759082b00d406f92781542ce86756eb73c5efe20acc7df6c25ac86be320a3ef5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31433439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e91fe6663d9d90deed07c1d003a80fa6698137267c83310828f24a7ef63f6ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 02 Aug 2022 00:40:38 GMT
ADD file:6039adfbca55ed34a719c37672c664e3524130a0e2a3b8663629b8120b81b790 in / 
# Tue, 02 Aug 2022 00:40:39 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 03:56:15 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 02 Aug 2022 03:56:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Aug 2022 20:33:46 GMT
ENV MEMCACHED_VERSION=1.6.16
# Thu, 04 Aug 2022 20:33:47 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Thu, 04 Aug 2022 20:36:17 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Thu, 04 Aug 2022 20:36:19 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 04 Aug 2022 20:36:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 04 Aug 2022 20:36:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Aug 2022 20:36:21 GMT
USER memcache
# Thu, 04 Aug 2022 20:36:22 GMT
EXPOSE 11211
# Thu, 04 Aug 2022 20:36:23 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a9fe95647e78b5516c7e2327355b6996e2ea295cd76ae242cbfe87f016b4e760`  
		Last Modified: Tue, 02 Aug 2022 00:46:05 GMT  
		Size: 30.1 MB (30054304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b983df009e7dc88033f53f015c09c56fd4db032d1abcade3333d8d4b515ff4af`  
		Last Modified: Tue, 02 Aug 2022 03:59:48 GMT  
		Size: 4.9 KB (4902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60720019405b50af041f391ec7dad90893ee95fc63fd6b3fb9da04850936f5db`  
		Last Modified: Tue, 02 Aug 2022 03:59:48 GMT  
		Size: 119.2 KB (119225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70569bedb4ee539337d6d3fd88e4076a1464b3a77bcfcca6604e18b815dbc402`  
		Last Modified: Thu, 04 Aug 2022 20:40:00 GMT  
		Size: 1.3 MB (1254600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:565112c01ad7b82688180f4fe70f5433126d79cc4b74e3d7f308601e2d34d9fe`  
		Last Modified: Thu, 04 Aug 2022 20:39:59 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce11290eb88924797c1fa048bd052c1243e4cb47e3469b26f3f1a3bc26472d19`  
		Last Modified: Thu, 04 Aug 2022 20:39:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:latest` - linux; 386

```console
$ docker pull memcached@sha256:3770f2e3c3f2abb5f85a6a615e62fd5c78a61513ca573ee4385adf42629bd88c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.8 MB (33775724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2804b930e07f367a1e5adc6a5631e87c78a986d3ad64e06e3c549c20ad7ce735`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Aug 2022 01:02:40 GMT
ADD file:5ca62c98116941aaa64ec72afb689a088c46f75a3e83d5b0d4e58d65ec905ccd in / 
# Tue, 23 Aug 2022 01:02:40 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 03:22:44 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 23 Aug 2022 03:22:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 03:22:49 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 23 Aug 2022 03:22:50 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 23 Aug 2022 03:26:54 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 23 Aug 2022 03:26:56 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 23 Aug 2022 03:26:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 23 Aug 2022 03:26:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 03:26:58 GMT
USER memcache
# Tue, 23 Aug 2022 03:26:59 GMT
EXPOSE 11211
# Tue, 23 Aug 2022 03:27:00 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6b3cb4a05a891d9d8a87a2bd7247b16f79832a9d4afbad3ff5068f6fc2ba1560`  
		Last Modified: Tue, 23 Aug 2022 01:08:25 GMT  
		Size: 32.4 MB (32387317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd24201e0b5e9a68a67bdc3b464a01aeb9a2e5a859a582cdaa80ab08a608337`  
		Last Modified: Tue, 23 Aug 2022 03:27:47 GMT  
		Size: 4.8 KB (4774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3070e5e3b1d98fa0b67b8390880b7596c4719b774864de21f36ed86873041793`  
		Last Modified: Tue, 23 Aug 2022 03:27:48 GMT  
		Size: 130.1 KB (130136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a076923bc48ef00816393d79ac2aa3ad931f47309aff7a6cf0c6c74d443080f`  
		Last Modified: Tue, 23 Aug 2022 03:27:48 GMT  
		Size: 1.3 MB (1253091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7169b397a99c6597495d00b3cb6b04483b8950d04bc7cbdcccf983f225294bb4`  
		Last Modified: Tue, 23 Aug 2022 03:27:48 GMT  
		Size: 288.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55ee497fd4fa66154f7c38bc2bb37f6e356318dc032b26ed65eb94ddc8355995`  
		Last Modified: Tue, 23 Aug 2022 03:27:47 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:latest` - linux; mips64le

```console
$ docker pull memcached@sha256:0d6798ccd4a9ac44c6ca7c358b2de6bdedbfe104de7d9987eedc68864ab8acc0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 MB (31002934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aca3e1ecca25fb97ad1d376d73b212cad11874d1f051c4c4bac1b2d27abc15fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 02 Aug 2022 01:10:34 GMT
ADD file:6dc22a1e5b5fcf23f2549406ddcc45c4e244f46e21eafa881de81fa87438e5d8 in / 
# Tue, 02 Aug 2022 01:10:38 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 03:22:53 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 02 Aug 2022 03:23:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Aug 2022 20:07:25 GMT
ENV MEMCACHED_VERSION=1.6.16
# Thu, 04 Aug 2022 20:07:28 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Thu, 04 Aug 2022 20:14:28 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Thu, 04 Aug 2022 20:14:30 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 04 Aug 2022 20:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 04 Aug 2022 20:14:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Aug 2022 20:14:40 GMT
USER memcache
# Thu, 04 Aug 2022 20:14:42 GMT
EXPOSE 11211
# Thu, 04 Aug 2022 20:14:45 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:88350749a27614c791450c256b051f023d81cdd256211274b1efac493779d2be`  
		Last Modified: Tue, 02 Aug 2022 01:21:02 GMT  
		Size: 29.6 MB (29628964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:117af7bbaadea9c81bbaa3a8a77b1ab5cd05bcac856c462cda2e81c9a40596ab`  
		Last Modified: Tue, 02 Aug 2022 03:30:45 GMT  
		Size: 4.9 KB (4863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a16d313748bd6b2dade87de73d79edd8a08e4cb662769a717f8587abc8d5e0`  
		Last Modified: Tue, 02 Aug 2022 03:30:46 GMT  
		Size: 117.1 KB (117127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d524786af3243ee367d118f6d5260cffa06d800f492f9b4bb36c910958186933`  
		Last Modified: Thu, 04 Aug 2022 20:15:05 GMT  
		Size: 1.3 MB (1251571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4badb1f1970762d08dbd43d7e101081a5fabd3c45e18afd70636397e83102d2f`  
		Last Modified: Thu, 04 Aug 2022 20:15:04 GMT  
		Size: 288.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3102636392803c3bbff48f39e7f143e3bf9a0528365d63b90dc31cd32060d3e0`  
		Last Modified: Thu, 04 Aug 2022 20:15:04 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:latest` - linux; ppc64le

```console
$ docker pull memcached@sha256:6eac50a2d123c021e75657700bdd2d0335dcc97db595e783eb6feaf81e0d6ab0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 MB (36969051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77075f2945ec5e196ccf20148829ebe266a384c2972f723f72361e05e3ee1bf5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 23 Aug 2022 01:24:52 GMT
ADD file:d35213360d726a18e220276d33f245115c3e94a321addaa4c9127488368b0203 in / 
# Tue, 23 Aug 2022 01:24:54 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 02:34:49 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 23 Aug 2022 02:34:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 02:34:56 GMT
ENV MEMCACHED_VERSION=1.6.16
# Tue, 23 Aug 2022 02:34:56 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Tue, 23 Aug 2022 02:38:10 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 23 Aug 2022 02:38:10 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 23 Aug 2022 02:38:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 23 Aug 2022 02:38:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Aug 2022 02:38:12 GMT
USER memcache
# Tue, 23 Aug 2022 02:38:12 GMT
EXPOSE 11211
# Tue, 23 Aug 2022 02:38:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:698954eda09d38dd1ccc9ce777b1f6bc7f7473fc6c4c3eb634acc8d035a42eae`  
		Last Modified: Tue, 23 Aug 2022 01:30:36 GMT  
		Size: 35.3 MB (35284280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ffb080d920662043edc67113c0de4c68258ad19c0fffd9e3b79fa01800c6015`  
		Last Modified: Tue, 23 Aug 2022 02:39:09 GMT  
		Size: 5.0 KB (4980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b1f66b68991d8f5ab064b3988db37a48b8f28b4ef0eb8e83efa4c419b630ff`  
		Last Modified: Tue, 23 Aug 2022 02:39:09 GMT  
		Size: 356.9 KB (356931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9653070548c34c29ed693878ef68223dbe9ccefc4653b86d3c8225bc8f85ac1`  
		Last Modified: Tue, 23 Aug 2022 02:39:09 GMT  
		Size: 1.3 MB (1322453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd51b501bab55d128a547f5c14e6410e4ef4b7b08f1867c7c933db716d7791e7`  
		Last Modified: Tue, 23 Aug 2022 02:39:09 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e693f7e8dfc8fe4a2af505658484b885fe097586d4f22c43aaf8278756e76ca`  
		Last Modified: Tue, 23 Aug 2022 02:39:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:latest` - linux; s390x

```console
$ docker pull memcached@sha256:4f7e9706bfd16d98bfb48a6435c8359a167ab733777f16f24996cad3f431bdc5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31211398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6739ca31062c74398fdfec102afbacead1c25fa0decf2fa14bdecdcb6b160543`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 02 Aug 2022 00:42:27 GMT
ADD file:c2afc8990930846fbe7c99bfdfe9ea562c75feb6e3c9122431f7c9f8b5e51a7f in / 
# Tue, 02 Aug 2022 00:42:29 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 02:37:02 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 02 Aug 2022 02:37:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Aug 2022 20:28:18 GMT
ENV MEMCACHED_VERSION=1.6.16
# Thu, 04 Aug 2022 20:28:18 GMT
ENV MEMCACHED_SHA1=724f31c3462fb6b07264d72d0043fd65545fd84a
# Thu, 04 Aug 2022 20:31:37 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Thu, 04 Aug 2022 20:31:37 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 04 Aug 2022 20:31:37 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 04 Aug 2022 20:31:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Aug 2022 20:31:38 GMT
USER memcache
# Thu, 04 Aug 2022 20:31:38 GMT
EXPOSE 11211
# Thu, 04 Aug 2022 20:31:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:026d311d0716db60eba0572ea784c21031f420960510cebcc383dc53949b4db8`  
		Last Modified: Tue, 02 Aug 2022 00:48:01 GMT  
		Size: 29.6 MB (29640259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0ffdb328e548bd6b6311c78665ac8cd3be8f0b2e09691701d9b0bae0924f8f5`  
		Last Modified: Tue, 02 Aug 2022 02:41:16 GMT  
		Size: 5.0 KB (5025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fbb9677007b0ebab2fe6feab520da1962d3fcffb3490aa844681a46fcb35749`  
		Last Modified: Tue, 02 Aug 2022 02:41:16 GMT  
		Size: 324.2 KB (324183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9c93abfa1f832f2e1f02fbe7b9a489735142c2051dafa7af20d985ff2e2106b`  
		Last Modified: Thu, 04 Aug 2022 20:36:17 GMT  
		Size: 1.2 MB (1241523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f78bf4cf172bedc6ad3c92b859859b10c0394104262328d5664ddc0b1488b29`  
		Last Modified: Thu, 04 Aug 2022 20:36:17 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6a26d2d4c34166613098e1380842f1355b534e2335a1dea2128c193b7f19bec`  
		Last Modified: Thu, 04 Aug 2022 20:36:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
