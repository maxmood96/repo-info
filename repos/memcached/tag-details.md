<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `memcached`

-	[`memcached:1`](#memcached1)
-	[`memcached:1-alpine`](#memcached1-alpine)
-	[`memcached:1-alpine3.18`](#memcached1-alpine318)
-	[`memcached:1-bookworm`](#memcached1-bookworm)
-	[`memcached:1.6`](#memcached16)
-	[`memcached:1.6-alpine`](#memcached16-alpine)
-	[`memcached:1.6-alpine3.18`](#memcached16-alpine318)
-	[`memcached:1.6-bookworm`](#memcached16-bookworm)
-	[`memcached:1.6.20`](#memcached1620)
-	[`memcached:1.6.20-alpine`](#memcached1620-alpine)
-	[`memcached:1.6.20-alpine3.18`](#memcached1620-alpine318)
-	[`memcached:1.6.20-bookworm`](#memcached1620-bookworm)
-	[`memcached:alpine`](#memcachedalpine)
-	[`memcached:alpine3.18`](#memcachedalpine318)
-	[`memcached:bookworm`](#memcachedbookworm)
-	[`memcached:latest`](#memcachedlatest)

## `memcached:1`

```console
$ docker pull memcached@sha256:b98fa1ffaab2dcd8d970fe7030487920c8edc93b2a932f263bc4e0475d0ac2b3
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
$ docker pull memcached@sha256:533c607824b2f5781b179e175fcdf055577a3f076fb0a0fdcd13487c7c92125f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (38973406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbcfa8d0003c80b0bba4004f4b15b4a5600b9dd481ac2d887bc31e794f067464`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jun 2023 23:20:42 GMT
ADD file:ba1250b6ecd5dd09d4914189d72741c2817988994e7da514bf62be439a34bdb5 in / 
# Mon, 12 Jun 2023 23:20:42 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 20:48:19 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 14 Jun 2023 20:48:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jun 2023 20:48:24 GMT
ENV MEMCACHED_VERSION=1.6.20
# Wed, 14 Jun 2023 20:48:24 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Wed, 14 Jun 2023 20:50:40 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 14 Jun 2023 20:50:40 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 14 Jun 2023 20:50:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Jun 2023 20:50:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 20:50:41 GMT
USER memcache
# Wed, 14 Jun 2023 20:50:41 GMT
EXPOSE 11211
# Wed, 14 Jun 2023 20:50:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5b5fe70539cd6989aa19f25826309f9715a9489cf1c057982d6a84c1ad8975c7`  
		Last Modified: Mon, 12 Jun 2023 23:25:49 GMT  
		Size: 29.1 MB (29124744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab209434009a85e82d99c0547bb947940f9e1002ce6e965417396ee22a6820db`  
		Last Modified: Wed, 14 Jun 2023 20:53:33 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f4dfc49c9cdae8d4df855de7cc0460e5db8c762e73786d4f8fa4f69ba11d6d`  
		Last Modified: Wed, 14 Jun 2023 20:53:33 GMT  
		Size: 2.7 MB (2677239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96a3de0d22592d9a254814d5b77e3a84e73d2f055d162503fe811f731a320701`  
		Last Modified: Wed, 14 Jun 2023 20:53:34 GMT  
		Size: 7.2 MB (7169888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a38b201fb7fc8d917459453ee1c0218cf9845c96b885a02b02999f81b21c6bb`  
		Last Modified: Wed, 14 Jun 2023 20:53:33 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6f5720dc1980c886ee7e8d6067ed87e102bb31824e557a85fbd54273542debf`  
		Last Modified: Wed, 14 Jun 2023 20:53:33 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1` - linux; arm variant v5

```console
$ docker pull memcached@sha256:9dba87e9c87eb3058b7db8d6a35423e25ff2aaa7baabb27c5e6137017c48fe1a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 MB (30470602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:308667429b0aed213503576d9f474cc30e4f0181773f9cee3aa2ac42d3c74a7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jun 2023 23:48:46 GMT
ADD file:b2773fa62bdb5672863ef317ee1b58de2a6074fe6aa0d8287a7cd0999028d7d2 in / 
# Mon, 12 Jun 2023 23:48:47 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 04:08:38 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 13 Jun 2023 04:08:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 04:08:45 GMT
ENV MEMCACHED_VERSION=1.6.20
# Tue, 13 Jun 2023 04:08:45 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Tue, 13 Jun 2023 04:11:47 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 13 Jun 2023 04:11:47 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 13 Jun 2023 04:11:48 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 13 Jun 2023 04:11:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jun 2023 04:11:49 GMT
USER memcache
# Tue, 13 Jun 2023 04:11:49 GMT
EXPOSE 11211
# Tue, 13 Jun 2023 04:11:49 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c04d7d6633d9b8cf1bfa9f6831ac7dd6f985411cb6307d91c6373085b09b8c19`  
		Last Modified: Mon, 12 Jun 2023 23:52:06 GMT  
		Size: 28.9 MB (28918779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1860b36b146eb799ae5299a102c03f7c12063adcb754066bd9eab20450d0cebb`  
		Last Modified: Tue, 13 Jun 2023 04:12:05 GMT  
		Size: 4.9 KB (4890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:557508c54a290bb2d6fda92e97a2058bcc1de808bcca254bb1559ea268d1bc8c`  
		Last Modified: Tue, 13 Jun 2023 04:12:06 GMT  
		Size: 316.8 KB (316757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67839ee937c662a3b1177503ab80dd4b2c4f95b5d0a8ffdf33276e7e30eecc85`  
		Last Modified: Tue, 13 Jun 2023 04:12:06 GMT  
		Size: 1.2 MB (1229770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e2a90f0421d9b93e896ff2136b06e5d157fd43ccd4cd1d62da5d0f8ba0466d9`  
		Last Modified: Tue, 13 Jun 2023 04:12:05 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e85a558ae3e0a483e80e987991797c179374d3573bf62638af5a4e2b1fb3c730`  
		Last Modified: Tue, 13 Jun 2023 04:12:05 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1` - linux; arm variant v7

```console
$ docker pull memcached@sha256:2841be0a36134563966c09a6ed68b21053d20342ec8736cf92763c28077ead43
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28094215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cf74ffa940dd93988fc0beb6698c5796563c82a40b7dd668153969f64d2e6ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 09 Feb 2023 06:12:09 GMT
ADD file:5f1a343224e8486690bd90dd1e50c8d84b3d770c51bb6829544e5cf650c0419c in / 
# Thu, 09 Feb 2023 06:12:10 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 07:52:31 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Thu, 09 Feb 2023 07:52:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 07:52:35 GMT
ENV MEMCACHED_VERSION=1.6.18
# Thu, 09 Feb 2023 07:52:35 GMT
ENV MEMCACHED_SHA1=be16909bb75ab972ee5fe438312501de01c4725a
# Thu, 09 Feb 2023 07:55:44 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Thu, 09 Feb 2023 07:55:44 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 09 Feb 2023 07:55:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 09 Feb 2023 07:55:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Feb 2023 07:55:44 GMT
USER memcache
# Thu, 09 Feb 2023 07:55:45 GMT
EXPOSE 11211
# Thu, 09 Feb 2023 07:55:45 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:e7318f6106ad75d7d482ae9dddf4d927b0872ef3ddb6e1330aa691fc8d17279e`  
		Last Modified: Thu, 09 Feb 2023 06:19:19 GMT  
		Size: 26.6 MB (26577666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de49d9d72daf1680b5f1b9532dd2eb0162829f36c8db9669935462636fbf99d9`  
		Last Modified: Thu, 09 Feb 2023 08:06:11 GMT  
		Size: 4.9 KB (4895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0beac9d5bcac946f8c54c72b8a9c136914b1aa7a5fe2b8c3df4c7d8858ea6559`  
		Last Modified: Thu, 09 Feb 2023 08:06:11 GMT  
		Size: 312.1 KB (312088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4c9e5a265394e4c0f357779e6195a4e82d767a3691a0e77d427e56651c3e54a`  
		Last Modified: Thu, 09 Feb 2023 08:06:11 GMT  
		Size: 1.2 MB (1199163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ea82ad892fe1ae8623d84e32c8c027087cda8aa49e40d4546ed6942e471c60`  
		Last Modified: Thu, 09 Feb 2023 08:06:11 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2ae3bcdc0d114ba49a67df022b6f7215fc87f1f50e64939fcfbbec4eaadee5`  
		Last Modified: Thu, 09 Feb 2023 08:06:11 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:3464bfccdfad0dc788e056949d59fc0b665ec165654b3a8502a2f4a3868a3dc7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 MB (37872888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20f33353745665e05e1722aa9af40e06b3f58778f8e758e786eaad30054de61f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jun 2023 23:40:13 GMT
ADD file:f75c3fe22fec548b35a86a9a5802fdc97497f5d253cf630d65f13282169d3f3f in / 
# Mon, 12 Jun 2023 23:40:14 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 20:54:33 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 14 Jun 2023 20:54:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jun 2023 20:54:37 GMT
ENV MEMCACHED_VERSION=1.6.20
# Wed, 14 Jun 2023 20:54:37 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Wed, 14 Jun 2023 20:57:13 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 14 Jun 2023 20:57:13 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 14 Jun 2023 20:57:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Jun 2023 20:57:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 20:57:14 GMT
USER memcache
# Wed, 14 Jun 2023 20:57:14 GMT
EXPOSE 11211
# Wed, 14 Jun 2023 20:57:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:95039a22a7cc3ae41d71f075e6e09e91e8da850fb5f80aba2f4a09f254520539`  
		Last Modified: Mon, 12 Jun 2023 23:44:08 GMT  
		Size: 29.2 MB (29152534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6da70104cc8ee465752315034f04011354e6149243e2bc69b9da49e6855df4b8`  
		Last Modified: Wed, 14 Jun 2023 21:00:29 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a7b40152f53e05b8cbcfe09be5b1598fcc05cf4f9ffad3b296eca43305450da`  
		Last Modified: Wed, 14 Jun 2023 21:00:30 GMT  
		Size: 2.5 MB (2539179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bf09d04f9c61af195486f42915b137b8612584f982737f5e465d02648a6dc8a`  
		Last Modified: Wed, 14 Jun 2023 21:00:30 GMT  
		Size: 6.2 MB (6179640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e71555e51295eeceeab1a9ab6bebb21108fbbe59e01349857c51932deea0f64`  
		Last Modified: Wed, 14 Jun 2023 21:00:29 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15cd3195dbfc5cedaf71b7c156002599dfb94219b51f85c966a1bee80bc37e65`  
		Last Modified: Wed, 14 Jun 2023 21:00:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1` - linux; 386

```console
$ docker pull memcached@sha256:719a898d7d05b1981b584eaaadd22e357c8a3b1b53509053cb6cc089cd6a38e0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (33997029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae0070d643d6b72bec5cad5100ac31c4fcb9b3108bade974a59d9933c70bda21`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jun 2023 23:39:58 GMT
ADD file:440924fd31c090a7f5e3d36276d17574922eb3e8ececce333fa42f7a95bdd9ce in / 
# Mon, 12 Jun 2023 23:39:58 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 20:20:47 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 13 Jun 2023 20:20:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 20:20:52 GMT
ENV MEMCACHED_VERSION=1.6.20
# Tue, 13 Jun 2023 20:20:52 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Tue, 13 Jun 2023 20:24:26 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 13 Jun 2023 20:24:26 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 13 Jun 2023 20:24:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 13 Jun 2023 20:24:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jun 2023 20:24:27 GMT
USER memcache
# Tue, 13 Jun 2023 20:24:27 GMT
EXPOSE 11211
# Tue, 13 Jun 2023 20:24:27 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1646137eb700afc9e891c03fdf28d3f5bc489ef0200fdacc67beee837d48db7d`  
		Last Modified: Mon, 12 Jun 2023 23:47:07 GMT  
		Size: 32.4 MB (32397388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9622551bea561b9c36a4e6d3a95484a278b356138badefce3b9186fc736fd556`  
		Last Modified: Tue, 13 Jun 2023 20:25:00 GMT  
		Size: 4.9 KB (4894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c12401a5e374bfe8c291818c808a2425cd0b16ac8cd178a47c8bf5eea598755b`  
		Last Modified: Tue, 13 Jun 2023 20:25:00 GMT  
		Size: 336.8 KB (336783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c456f2d87234421d6c272fad6161dc85df8bac55c7ea1750d68a216dd1534ee`  
		Last Modified: Tue, 13 Jun 2023 20:25:11 GMT  
		Size: 1.3 MB (1257556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:178b408b1cbfa94c9656a36bf64bf57a8df765953c7ec4c7e224851c29d35f71`  
		Last Modified: Tue, 13 Jun 2023 20:25:00 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6210b196c4e58f73e538fc8b508a56ac8918a914f6da6fd95c9721389d06c0a9`  
		Last Modified: Tue, 13 Jun 2023 20:25:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1` - linux; mips64le

```console
$ docker pull memcached@sha256:d2855c4deb19365dd1c83b81c9e1fa36f7873cc8b3dd02f8f01de10200bf208e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37554221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7068fffc8ee0a4607e1586297977a273786efb52e1782f11396ee5f7a5150c0f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 13 Jun 2023 00:09:02 GMT
ADD file:f91bd2a174259cb69646fc34ba2fc6b8941ad8e171d2d7952a4d8ac3d95e2ad7 in / 
# Tue, 13 Jun 2023 00:09:06 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 18:38:15 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 14 Jun 2023 18:38:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jun 2023 18:38:39 GMT
ENV MEMCACHED_VERSION=1.6.20
# Wed, 14 Jun 2023 18:38:41 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Wed, 14 Jun 2023 18:45:20 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 14 Jun 2023 18:45:23 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 14 Jun 2023 18:45:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Jun 2023 18:45:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 18:45:32 GMT
USER memcache
# Wed, 14 Jun 2023 18:45:35 GMT
EXPOSE 11211
# Wed, 14 Jun 2023 18:45:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3fc28260a4d871ef9781cad2bb064ad7212a5063de3a1d35dba938ce82115e5b`  
		Last Modified: Tue, 13 Jun 2023 00:22:29 GMT  
		Size: 29.1 MB (29118129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c804aeb794275ae845d32d2939d0e0fefa75cd112f1075aaf2104097050ae8`  
		Last Modified: Wed, 14 Jun 2023 18:46:04 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf29fcbe26928e2f4086a889098220505bdd4401dc87958f623ade0618efcd28`  
		Last Modified: Wed, 14 Jun 2023 18:46:05 GMT  
		Size: 1.9 MB (1934899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76d4e9cc234d41e69eba3bf411cb1d3ebe17e2fefbffb0c3458d613f2545337e`  
		Last Modified: Wed, 14 Jun 2023 18:46:09 GMT  
		Size: 6.5 MB (6499709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0988c34e4840378b9876eba362b50458e769389d0cc626698bef65e46c721458`  
		Last Modified: Wed, 14 Jun 2023 18:46:04 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db55745458426cdf0d23fd0589fd440e2d328e4d5ffb00a9ef6d2e0225cec8bf`  
		Last Modified: Wed, 14 Jun 2023 18:46:04 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1` - linux; ppc64le

```console
$ docker pull memcached@sha256:0e023c41d9c6a8d04edad22ecea59cfcf424d0dc3895c442a9e7a4575961d53d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43193448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a85a60b74a9575a203aba1a5f800dfe479b80cde8ff577ccd5e7e77bdaab64c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jun 2023 23:17:34 GMT
ADD file:3f8b9849acb625537f99921ef80190de7b03afdc287a5d1113a92cc41ae24be2 in / 
# Mon, 12 Jun 2023 23:17:36 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 18:15:42 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 14 Jun 2023 18:15:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jun 2023 18:15:50 GMT
ENV MEMCACHED_VERSION=1.6.20
# Wed, 14 Jun 2023 18:15:51 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Wed, 14 Jun 2023 18:19:27 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 14 Jun 2023 18:19:28 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 14 Jun 2023 18:19:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Jun 2023 18:19:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 18:19:31 GMT
USER memcache
# Wed, 14 Jun 2023 18:19:32 GMT
EXPOSE 11211
# Wed, 14 Jun 2023 18:19:32 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9f041b53cef30007c43057f2520876c85ed6bee6be5aaee867dfb31a053d6cca`  
		Last Modified: Mon, 12 Jun 2023 23:24:09 GMT  
		Size: 33.1 MB (33116725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a2d84b1fee81412bbd9bb301c77e6dfacfac70c2f1485de806658b49b06e08`  
		Last Modified: Wed, 14 Jun 2023 18:19:49 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca8bb5af043b48c9fe0e110ee13c139ceb715570346140fc86092d582d38b52b`  
		Last Modified: Wed, 14 Jun 2023 18:19:50 GMT  
		Size: 2.9 MB (2891306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e2d7805a151ec1618da95ad34cb2fdc6ae889b9f7908aaca6d063ca864f3e24`  
		Last Modified: Wed, 14 Jun 2023 18:19:52 GMT  
		Size: 7.2 MB (7183881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc5db4b315753422be0d08638f594b1ec64484c44f68942473f903387853b3bd`  
		Last Modified: Wed, 14 Jun 2023 18:19:49 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a8a9b2ed7c41d27d92f9db3c21beec2a2e288b0bc54a19aa1d3574b6085eaa6`  
		Last Modified: Wed, 14 Jun 2023 18:19:49 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1` - linux; s390x

```console
$ docker pull memcached@sha256:882f9d1d57c58c374c6074cbce0784748bdce465757ad946f699a47a924f4518
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31228777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:098ff94df44cb535cdd4f10e4106756fc1766a232277b3a9c2f51ff567ee3082`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 13 Jun 2023 04:30:13 GMT
ADD file:558e8c34e969d458ce6bf4207d9c0fe05d2e67d3457c1d5689666749e82ef2ab in / 
# Tue, 13 Jun 2023 04:30:14 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 18:41:51 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 13 Jun 2023 18:41:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 18:41:54 GMT
ENV MEMCACHED_VERSION=1.6.20
# Tue, 13 Jun 2023 18:41:54 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Tue, 13 Jun 2023 18:44:58 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 13 Jun 2023 18:44:58 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 13 Jun 2023 18:44:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 13 Jun 2023 18:44:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jun 2023 18:44:59 GMT
USER memcache
# Tue, 13 Jun 2023 18:44:59 GMT
EXPOSE 11211
# Tue, 13 Jun 2023 18:44:59 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6a752e2308c741009b6f5a88a8ea6764b96ebe7f544197912d8ef9a3ec8c8763`  
		Last Modified: Tue, 13 Jun 2023 04:34:49 GMT  
		Size: 29.7 MB (29652514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:465e13673c57447925389cdcf074d61ff5114faa447fd3b775481a229ac38019`  
		Last Modified: Tue, 13 Jun 2023 18:45:27 GMT  
		Size: 5.0 KB (5023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a81fcab4fd1cd8ac9cc18539fde149b89e423f0b5c80f2f07460f49209907ca`  
		Last Modified: Tue, 13 Jun 2023 18:45:27 GMT  
		Size: 324.3 KB (324337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a035c15be3c1e4f3cd28a1c060f56d03f4fa02c5e86290288ac74b2533feca`  
		Last Modified: Tue, 13 Jun 2023 18:45:27 GMT  
		Size: 1.2 MB (1246496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdda04e27e25f6bf6f5489a28d36c1903052488bf96ee74f76b993a5926207b7`  
		Last Modified: Tue, 13 Jun 2023 18:45:27 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d62044b354beed912ecf01ba2d6b0efc230907a720539c8850809e2b76f9ac89`  
		Last Modified: Tue, 13 Jun 2023 18:45:27 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:1-alpine`

```console
$ docker pull memcached@sha256:dd03af6acd2f6e2fad2a24cb0db1c987074c6f968c2995c6d9920015efb243a7
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
$ docker pull memcached@sha256:a7a04bc20ec122d9f024dff57494853d5dc9705fb97af9170cc31a1f531dcaa5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4462373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15429daa972e1d57884e75ecc7f784564ae7cf089c25671dd118a0025f806b6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 20:50:58 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Wed, 14 Jun 2023 20:50:59 GMT
RUN apk add --no-cache libsasl
# Wed, 14 Jun 2023 20:50:59 GMT
ENV MEMCACHED_VERSION=1.6.20
# Wed, 14 Jun 2023 20:50:59 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Wed, 14 Jun 2023 20:53:09 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Wed, 14 Jun 2023 20:53:09 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 14 Jun 2023 20:53:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Jun 2023 20:53:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 20:53:09 GMT
USER memcache
# Wed, 14 Jun 2023 20:53:09 GMT
EXPOSE 11211
# Wed, 14 Jun 2023 20:53:09 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b2b2df106c5026cd33ea4ac655b77f25410ec9f4b8a6756ebc1ceeb79fca3c7`  
		Last Modified: Wed, 14 Jun 2023 20:53:58 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed63668528d3e2159f55909c66dc48a6f746ce24c2e2f6d963b992aefaa457ce`  
		Last Modified: Wed, 14 Jun 2023 20:53:58 GMT  
		Size: 108.1 KB (108080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc06ea6ffc2a4279c91e26e37b450afb1e0f1007815b19a7146d52b016dddc61`  
		Last Modified: Wed, 14 Jun 2023 20:53:59 GMT  
		Size: 954.7 KB (954748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:098e9e56712cb64736718f40b476d8eeb9410130c28ce94fe1bc2d380d9083cf`  
		Last Modified: Wed, 14 Jun 2023 20:53:59 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5c14818f6fb630a615284b18f945c89c0563530c25f07af955d0f85504020e9`  
		Last Modified: Wed, 14 Jun 2023 20:53:58 GMT  
		Size: 118.0 B  
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
$ docker pull memcached@sha256:e59934ff7bef6e6053b618f65923d2c1fa7235a008fb20f4fe9db13f8d6dc167
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4399194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dab6918acf63bcf26d1a95d40666c44f281aa14f0d4e27884d4c2f4b227dd9b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 20:57:26 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Wed, 14 Jun 2023 20:57:27 GMT
RUN apk add --no-cache libsasl
# Wed, 14 Jun 2023 20:57:27 GMT
ENV MEMCACHED_VERSION=1.6.20
# Wed, 14 Jun 2023 20:57:27 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Wed, 14 Jun 2023 20:59:54 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Wed, 14 Jun 2023 20:59:54 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 14 Jun 2023 20:59:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Jun 2023 20:59:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 20:59:55 GMT
USER memcache
# Wed, 14 Jun 2023 20:59:55 GMT
EXPOSE 11211
# Wed, 14 Jun 2023 20:59:55 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:666588188768f19b27fb821e02d084406af8fd867cc4595b896b9eed50b2105e`  
		Last Modified: Wed, 14 Jun 2023 21:00:51 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d958a137d671266f063c0af4d7b0b6d44d9018b77fdbddb8fd412d3c0b1be3`  
		Last Modified: Wed, 14 Jun 2023 21:00:51 GMT  
		Size: 124.1 KB (124137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eddee3cdc367d6f8265fe941f97020460db6cb5555711640b2ad62bd5c2a613c`  
		Last Modified: Wed, 14 Jun 2023 21:00:51 GMT  
		Size: 944.1 KB (944138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfec1ffcd9427d8fb06b908c1d3e0715a9db99c94c46f7896890a98b95c5f049`  
		Last Modified: Wed, 14 Jun 2023 21:00:51 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aea835bd4a5d779b88da37bc977813dd1ed9d228f5e78e3459edde4fa6f155e2`  
		Last Modified: Wed, 14 Jun 2023 21:00:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine` - linux; 386

```console
$ docker pull memcached@sha256:126e7a3993f53145ad966b11e0c8e7cb9f92520ea9899abfaa550aaee49c9f5c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4313116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:835ad308527d3b6bc85d49a990ae4c544363b3e3b3cef7a7a49ea6081d81a121`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 May 2023 23:11:03 GMT
ADD file:cfe47ebe49c4a75094234cafa52aa13aa26abcdad49b89293585884b3a8faeae in / 
# Tue, 09 May 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Thu, 11 May 2023 19:56:01 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Thu, 11 May 2023 19:56:03 GMT
RUN apk add --no-cache libsasl
# Mon, 15 May 2023 21:42:18 GMT
ENV MEMCACHED_VERSION=1.6.20
# Mon, 15 May 2023 21:42:18 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Mon, 15 May 2023 21:45:44 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Mon, 15 May 2023 21:45:44 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Mon, 15 May 2023 21:45:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 15 May 2023 21:45:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 15 May 2023 21:45:45 GMT
USER memcache
# Mon, 15 May 2023 21:45:45 GMT
EXPOSE 11211
# Mon, 15 May 2023 21:45:45 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:613767c5530f4016482e81288d0efdca4e58c62031252130d8fccd6f6260a068`  
		Last Modified: Tue, 09 May 2023 23:11:20 GMT  
		Size: 3.3 MB (3264862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72c25994ef1ec30cf62d081517b625d1ea87b0836bb6a90cd7ab8b1ab0501bb6`  
		Last Modified: Thu, 11 May 2023 20:00:35 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c42385514308725216c1a4eadb9aa4270c08f3140c342b6db43060f55af1ed`  
		Last Modified: Thu, 11 May 2023 20:00:35 GMT  
		Size: 109.5 KB (109521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3acbe617b4c6e3f32de32c1e69b84aa2c4e9c31d5e84a648a8340acda2452e03`  
		Last Modified: Mon, 15 May 2023 21:46:28 GMT  
		Size: 937.1 KB (937060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a81b72d4c28496fdd77fd3bf62a9800bd545660f44738482a100b00f99b3649c`  
		Last Modified: Mon, 15 May 2023 21:46:27 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c224abc2162f00f8769eeacb44838cbed654dd60d38e8d08d585003cb6495a`  
		Last Modified: Mon, 15 May 2023 21:46:27 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:912319e8c2e48db747d88d979ed43b691d125b7c05619189b4dcbe86f19b9a8b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4494043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c26bf354613881c6a96c357992e4176080f21ed4cac05a673e9a34056bd7d8be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 May 2023 23:11:09 GMT
ADD file:0a227602737a24c596923d3fd0a7c8b7d9000dbc6b80561473def09abbebbfa6 in / 
# Tue, 09 May 2023 23:11:10 GMT
CMD ["/bin/sh"]
# Thu, 11 May 2023 20:28:43 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Thu, 11 May 2023 20:28:45 GMT
RUN apk add --no-cache libsasl
# Mon, 15 May 2023 21:20:18 GMT
ENV MEMCACHED_VERSION=1.6.20
# Mon, 15 May 2023 21:20:18 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Mon, 15 May 2023 21:23:19 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Mon, 15 May 2023 21:23:19 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Mon, 15 May 2023 21:23:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 15 May 2023 21:23:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 15 May 2023 21:23:20 GMT
USER memcache
# Mon, 15 May 2023 21:23:20 GMT
EXPOSE 11211
# Mon, 15 May 2023 21:23:21 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5c0986f188e93dd7e76a4dc49a9170da2cd124709f5e1590b378e31a2b0d9587`  
		Last Modified: Tue, 09 May 2023 23:11:31 GMT  
		Size: 3.4 MB (3385631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2637efcb2bfb898454103e5536179d5f732cbddcd32f89c4ed51466ed8c6a14`  
		Last Modified: Thu, 11 May 2023 20:32:50 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45b064e3e507b9c35d5b605a606755605f7807236709d725567d0609ac53ee29`  
		Last Modified: Thu, 11 May 2023 20:32:50 GMT  
		Size: 123.9 KB (123933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a5d4f2fcda4a8d8a11f4f09bab2989aa2ec605ec585ed61bb4b519b62f5a47`  
		Last Modified: Mon, 15 May 2023 21:24:04 GMT  
		Size: 982.8 KB (982805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81d636c8d2e3e1cce3ec344ad3d21645a62a2c2286037cc287cd4e56c21d3fe7`  
		Last Modified: Mon, 15 May 2023 21:24:03 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca8ad226ad66d4c655b3b77ce26667f5b878d47000bfc558dae9c53ec6cff9b5`  
		Last Modified: Mon, 15 May 2023 21:24:03 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:029a3ea9286bc7541646e7ca99fb57db8faffea15abf7bee651ee5cac65c4732
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4290940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac9f545f21c06b546f33df533b248b59335e5960e61844e6729780e8c404af6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 May 2023 23:11:06 GMT
ADD file:89d6e366e8ab41011a5866f8ca43aac6cfef00edffebad565918ab632a6d6210 in / 
# Tue, 09 May 2023 23:11:07 GMT
CMD ["/bin/sh"]
# Thu, 11 May 2023 19:55:27 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Thu, 11 May 2023 19:55:28 GMT
RUN apk add --no-cache libsasl
# Mon, 15 May 2023 21:51:02 GMT
ENV MEMCACHED_VERSION=1.6.20
# Mon, 15 May 2023 21:51:02 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Mon, 15 May 2023 21:54:04 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Mon, 15 May 2023 21:54:04 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Mon, 15 May 2023 21:54:04 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 15 May 2023 21:54:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 15 May 2023 21:54:04 GMT
USER memcache
# Mon, 15 May 2023 21:54:05 GMT
EXPOSE 11211
# Mon, 15 May 2023 21:54:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:25da54cc0a08f4ca602c6bcd3e52d70082eb8a25ee022bc9f1dda019de49197a`  
		Last Modified: Tue, 09 May 2023 23:11:35 GMT  
		Size: 3.2 MB (3226303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b276b6acd2b3a86c684a2f6a3641c76b4e2e5b3ce67562b64266899a052e6d4d`  
		Last Modified: Thu, 11 May 2023 19:59:45 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:483fe7c616264b630bec3883deae3b95c3220c0d46c5440048f5f2372224979c`  
		Last Modified: Thu, 11 May 2023 19:59:45 GMT  
		Size: 112.8 KB (112850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19827c7b432b650815a5843027a98d18e43bbd207cdda86bc95dc2f55c69b498`  
		Last Modified: Mon, 15 May 2023 21:54:45 GMT  
		Size: 950.1 KB (950116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da2238a07815946f6ba0dcbb105f0a4dab9db865ab4696d5c561fdd473328147`  
		Last Modified: Mon, 15 May 2023 21:54:46 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03dc27afabfb97c92d4893b707ee04b92ec5dd5e64ce581e0c27d7b344d7e735`  
		Last Modified: Mon, 15 May 2023 21:54:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:1-alpine3.18`

```console
$ docker pull memcached@sha256:f9aad561ac4e31d347b252c0fef6beede071bdaa205e38dc9dc5369201d8ff47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `memcached:1-alpine3.18` - linux; amd64

```console
$ docker pull memcached@sha256:a7a04bc20ec122d9f024dff57494853d5dc9705fb97af9170cc31a1f531dcaa5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4462373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15429daa972e1d57884e75ecc7f784564ae7cf089c25671dd118a0025f806b6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 20:50:58 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Wed, 14 Jun 2023 20:50:59 GMT
RUN apk add --no-cache libsasl
# Wed, 14 Jun 2023 20:50:59 GMT
ENV MEMCACHED_VERSION=1.6.20
# Wed, 14 Jun 2023 20:50:59 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Wed, 14 Jun 2023 20:53:09 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Wed, 14 Jun 2023 20:53:09 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 14 Jun 2023 20:53:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Jun 2023 20:53:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 20:53:09 GMT
USER memcache
# Wed, 14 Jun 2023 20:53:09 GMT
EXPOSE 11211
# Wed, 14 Jun 2023 20:53:09 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b2b2df106c5026cd33ea4ac655b77f25410ec9f4b8a6756ebc1ceeb79fca3c7`  
		Last Modified: Wed, 14 Jun 2023 20:53:58 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed63668528d3e2159f55909c66dc48a6f746ce24c2e2f6d963b992aefaa457ce`  
		Last Modified: Wed, 14 Jun 2023 20:53:58 GMT  
		Size: 108.1 KB (108080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc06ea6ffc2a4279c91e26e37b450afb1e0f1007815b19a7146d52b016dddc61`  
		Last Modified: Wed, 14 Jun 2023 20:53:59 GMT  
		Size: 954.7 KB (954748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:098e9e56712cb64736718f40b476d8eeb9410130c28ce94fe1bc2d380d9083cf`  
		Last Modified: Wed, 14 Jun 2023 20:53:59 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5c14818f6fb630a615284b18f945c89c0563530c25f07af955d0f85504020e9`  
		Last Modified: Wed, 14 Jun 2023 20:53:58 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:e59934ff7bef6e6053b618f65923d2c1fa7235a008fb20f4fe9db13f8d6dc167
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4399194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dab6918acf63bcf26d1a95d40666c44f281aa14f0d4e27884d4c2f4b227dd9b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 20:57:26 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Wed, 14 Jun 2023 20:57:27 GMT
RUN apk add --no-cache libsasl
# Wed, 14 Jun 2023 20:57:27 GMT
ENV MEMCACHED_VERSION=1.6.20
# Wed, 14 Jun 2023 20:57:27 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Wed, 14 Jun 2023 20:59:54 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Wed, 14 Jun 2023 20:59:54 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 14 Jun 2023 20:59:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Jun 2023 20:59:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 20:59:55 GMT
USER memcache
# Wed, 14 Jun 2023 20:59:55 GMT
EXPOSE 11211
# Wed, 14 Jun 2023 20:59:55 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:666588188768f19b27fb821e02d084406af8fd867cc4595b896b9eed50b2105e`  
		Last Modified: Wed, 14 Jun 2023 21:00:51 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d958a137d671266f063c0af4d7b0b6d44d9018b77fdbddb8fd412d3c0b1be3`  
		Last Modified: Wed, 14 Jun 2023 21:00:51 GMT  
		Size: 124.1 KB (124137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eddee3cdc367d6f8265fe941f97020460db6cb5555711640b2ad62bd5c2a613c`  
		Last Modified: Wed, 14 Jun 2023 21:00:51 GMT  
		Size: 944.1 KB (944138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfec1ffcd9427d8fb06b908c1d3e0715a9db99c94c46f7896890a98b95c5f049`  
		Last Modified: Wed, 14 Jun 2023 21:00:51 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aea835bd4a5d779b88da37bc977813dd1ed9d228f5e78e3459edde4fa6f155e2`  
		Last Modified: Wed, 14 Jun 2023 21:00:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine3.18` - linux; 386

```console
$ docker pull memcached@sha256:126e7a3993f53145ad966b11e0c8e7cb9f92520ea9899abfaa550aaee49c9f5c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4313116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:835ad308527d3b6bc85d49a990ae4c544363b3e3b3cef7a7a49ea6081d81a121`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 May 2023 23:11:03 GMT
ADD file:cfe47ebe49c4a75094234cafa52aa13aa26abcdad49b89293585884b3a8faeae in / 
# Tue, 09 May 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Thu, 11 May 2023 19:56:01 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Thu, 11 May 2023 19:56:03 GMT
RUN apk add --no-cache libsasl
# Mon, 15 May 2023 21:42:18 GMT
ENV MEMCACHED_VERSION=1.6.20
# Mon, 15 May 2023 21:42:18 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Mon, 15 May 2023 21:45:44 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Mon, 15 May 2023 21:45:44 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Mon, 15 May 2023 21:45:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 15 May 2023 21:45:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 15 May 2023 21:45:45 GMT
USER memcache
# Mon, 15 May 2023 21:45:45 GMT
EXPOSE 11211
# Mon, 15 May 2023 21:45:45 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:613767c5530f4016482e81288d0efdca4e58c62031252130d8fccd6f6260a068`  
		Last Modified: Tue, 09 May 2023 23:11:20 GMT  
		Size: 3.3 MB (3264862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72c25994ef1ec30cf62d081517b625d1ea87b0836bb6a90cd7ab8b1ab0501bb6`  
		Last Modified: Thu, 11 May 2023 20:00:35 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c42385514308725216c1a4eadb9aa4270c08f3140c342b6db43060f55af1ed`  
		Last Modified: Thu, 11 May 2023 20:00:35 GMT  
		Size: 109.5 KB (109521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3acbe617b4c6e3f32de32c1e69b84aa2c4e9c31d5e84a648a8340acda2452e03`  
		Last Modified: Mon, 15 May 2023 21:46:28 GMT  
		Size: 937.1 KB (937060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a81b72d4c28496fdd77fd3bf62a9800bd545660f44738482a100b00f99b3649c`  
		Last Modified: Mon, 15 May 2023 21:46:27 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c224abc2162f00f8769eeacb44838cbed654dd60d38e8d08d585003cb6495a`  
		Last Modified: Mon, 15 May 2023 21:46:27 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine3.18` - linux; ppc64le

```console
$ docker pull memcached@sha256:912319e8c2e48db747d88d979ed43b691d125b7c05619189b4dcbe86f19b9a8b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4494043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c26bf354613881c6a96c357992e4176080f21ed4cac05a673e9a34056bd7d8be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 May 2023 23:11:09 GMT
ADD file:0a227602737a24c596923d3fd0a7c8b7d9000dbc6b80561473def09abbebbfa6 in / 
# Tue, 09 May 2023 23:11:10 GMT
CMD ["/bin/sh"]
# Thu, 11 May 2023 20:28:43 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Thu, 11 May 2023 20:28:45 GMT
RUN apk add --no-cache libsasl
# Mon, 15 May 2023 21:20:18 GMT
ENV MEMCACHED_VERSION=1.6.20
# Mon, 15 May 2023 21:20:18 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Mon, 15 May 2023 21:23:19 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Mon, 15 May 2023 21:23:19 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Mon, 15 May 2023 21:23:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 15 May 2023 21:23:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 15 May 2023 21:23:20 GMT
USER memcache
# Mon, 15 May 2023 21:23:20 GMT
EXPOSE 11211
# Mon, 15 May 2023 21:23:21 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5c0986f188e93dd7e76a4dc49a9170da2cd124709f5e1590b378e31a2b0d9587`  
		Last Modified: Tue, 09 May 2023 23:11:31 GMT  
		Size: 3.4 MB (3385631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2637efcb2bfb898454103e5536179d5f732cbddcd32f89c4ed51466ed8c6a14`  
		Last Modified: Thu, 11 May 2023 20:32:50 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45b064e3e507b9c35d5b605a606755605f7807236709d725567d0609ac53ee29`  
		Last Modified: Thu, 11 May 2023 20:32:50 GMT  
		Size: 123.9 KB (123933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a5d4f2fcda4a8d8a11f4f09bab2989aa2ec605ec585ed61bb4b519b62f5a47`  
		Last Modified: Mon, 15 May 2023 21:24:04 GMT  
		Size: 982.8 KB (982805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81d636c8d2e3e1cce3ec344ad3d21645a62a2c2286037cc287cd4e56c21d3fe7`  
		Last Modified: Mon, 15 May 2023 21:24:03 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca8ad226ad66d4c655b3b77ce26667f5b878d47000bfc558dae9c53ec6cff9b5`  
		Last Modified: Mon, 15 May 2023 21:24:03 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine3.18` - linux; s390x

```console
$ docker pull memcached@sha256:029a3ea9286bc7541646e7ca99fb57db8faffea15abf7bee651ee5cac65c4732
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4290940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac9f545f21c06b546f33df533b248b59335e5960e61844e6729780e8c404af6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 May 2023 23:11:06 GMT
ADD file:89d6e366e8ab41011a5866f8ca43aac6cfef00edffebad565918ab632a6d6210 in / 
# Tue, 09 May 2023 23:11:07 GMT
CMD ["/bin/sh"]
# Thu, 11 May 2023 19:55:27 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Thu, 11 May 2023 19:55:28 GMT
RUN apk add --no-cache libsasl
# Mon, 15 May 2023 21:51:02 GMT
ENV MEMCACHED_VERSION=1.6.20
# Mon, 15 May 2023 21:51:02 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Mon, 15 May 2023 21:54:04 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Mon, 15 May 2023 21:54:04 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Mon, 15 May 2023 21:54:04 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 15 May 2023 21:54:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 15 May 2023 21:54:04 GMT
USER memcache
# Mon, 15 May 2023 21:54:05 GMT
EXPOSE 11211
# Mon, 15 May 2023 21:54:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:25da54cc0a08f4ca602c6bcd3e52d70082eb8a25ee022bc9f1dda019de49197a`  
		Last Modified: Tue, 09 May 2023 23:11:35 GMT  
		Size: 3.2 MB (3226303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b276b6acd2b3a86c684a2f6a3641c76b4e2e5b3ce67562b64266899a052e6d4d`  
		Last Modified: Thu, 11 May 2023 19:59:45 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:483fe7c616264b630bec3883deae3b95c3220c0d46c5440048f5f2372224979c`  
		Last Modified: Thu, 11 May 2023 19:59:45 GMT  
		Size: 112.8 KB (112850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19827c7b432b650815a5843027a98d18e43bbd207cdda86bc95dc2f55c69b498`  
		Last Modified: Mon, 15 May 2023 21:54:45 GMT  
		Size: 950.1 KB (950116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da2238a07815946f6ba0dcbb105f0a4dab9db865ab4696d5c561fdd473328147`  
		Last Modified: Mon, 15 May 2023 21:54:46 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03dc27afabfb97c92d4893b707ee04b92ec5dd5e64ce581e0c27d7b344d7e735`  
		Last Modified: Mon, 15 May 2023 21:54:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:1-bookworm`

```console
$ docker pull memcached@sha256:0495a71949e29a0dd91782be635586b244a336a765e79c78cfea895cd541e312
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; mips64le
	-	linux; ppc64le

### `memcached:1-bookworm` - linux; amd64

```console
$ docker pull memcached@sha256:533c607824b2f5781b179e175fcdf055577a3f076fb0a0fdcd13487c7c92125f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (38973406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbcfa8d0003c80b0bba4004f4b15b4a5600b9dd481ac2d887bc31e794f067464`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jun 2023 23:20:42 GMT
ADD file:ba1250b6ecd5dd09d4914189d72741c2817988994e7da514bf62be439a34bdb5 in / 
# Mon, 12 Jun 2023 23:20:42 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 20:48:19 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 14 Jun 2023 20:48:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jun 2023 20:48:24 GMT
ENV MEMCACHED_VERSION=1.6.20
# Wed, 14 Jun 2023 20:48:24 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Wed, 14 Jun 2023 20:50:40 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 14 Jun 2023 20:50:40 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 14 Jun 2023 20:50:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Jun 2023 20:50:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 20:50:41 GMT
USER memcache
# Wed, 14 Jun 2023 20:50:41 GMT
EXPOSE 11211
# Wed, 14 Jun 2023 20:50:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5b5fe70539cd6989aa19f25826309f9715a9489cf1c057982d6a84c1ad8975c7`  
		Last Modified: Mon, 12 Jun 2023 23:25:49 GMT  
		Size: 29.1 MB (29124744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab209434009a85e82d99c0547bb947940f9e1002ce6e965417396ee22a6820db`  
		Last Modified: Wed, 14 Jun 2023 20:53:33 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f4dfc49c9cdae8d4df855de7cc0460e5db8c762e73786d4f8fa4f69ba11d6d`  
		Last Modified: Wed, 14 Jun 2023 20:53:33 GMT  
		Size: 2.7 MB (2677239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96a3de0d22592d9a254814d5b77e3a84e73d2f055d162503fe811f731a320701`  
		Last Modified: Wed, 14 Jun 2023 20:53:34 GMT  
		Size: 7.2 MB (7169888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a38b201fb7fc8d917459453ee1c0218cf9845c96b885a02b02999f81b21c6bb`  
		Last Modified: Wed, 14 Jun 2023 20:53:33 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6f5720dc1980c886ee7e8d6067ed87e102bb31824e557a85fbd54273542debf`  
		Last Modified: Wed, 14 Jun 2023 20:53:33 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:3464bfccdfad0dc788e056949d59fc0b665ec165654b3a8502a2f4a3868a3dc7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 MB (37872888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20f33353745665e05e1722aa9af40e06b3f58778f8e758e786eaad30054de61f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jun 2023 23:40:13 GMT
ADD file:f75c3fe22fec548b35a86a9a5802fdc97497f5d253cf630d65f13282169d3f3f in / 
# Mon, 12 Jun 2023 23:40:14 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 20:54:33 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 14 Jun 2023 20:54:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jun 2023 20:54:37 GMT
ENV MEMCACHED_VERSION=1.6.20
# Wed, 14 Jun 2023 20:54:37 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Wed, 14 Jun 2023 20:57:13 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 14 Jun 2023 20:57:13 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 14 Jun 2023 20:57:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Jun 2023 20:57:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 20:57:14 GMT
USER memcache
# Wed, 14 Jun 2023 20:57:14 GMT
EXPOSE 11211
# Wed, 14 Jun 2023 20:57:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:95039a22a7cc3ae41d71f075e6e09e91e8da850fb5f80aba2f4a09f254520539`  
		Last Modified: Mon, 12 Jun 2023 23:44:08 GMT  
		Size: 29.2 MB (29152534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6da70104cc8ee465752315034f04011354e6149243e2bc69b9da49e6855df4b8`  
		Last Modified: Wed, 14 Jun 2023 21:00:29 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a7b40152f53e05b8cbcfe09be5b1598fcc05cf4f9ffad3b296eca43305450da`  
		Last Modified: Wed, 14 Jun 2023 21:00:30 GMT  
		Size: 2.5 MB (2539179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bf09d04f9c61af195486f42915b137b8612584f982737f5e465d02648a6dc8a`  
		Last Modified: Wed, 14 Jun 2023 21:00:30 GMT  
		Size: 6.2 MB (6179640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e71555e51295eeceeab1a9ab6bebb21108fbbe59e01349857c51932deea0f64`  
		Last Modified: Wed, 14 Jun 2023 21:00:29 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15cd3195dbfc5cedaf71b7c156002599dfb94219b51f85c966a1bee80bc37e65`  
		Last Modified: Wed, 14 Jun 2023 21:00:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:d2855c4deb19365dd1c83b81c9e1fa36f7873cc8b3dd02f8f01de10200bf208e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37554221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7068fffc8ee0a4607e1586297977a273786efb52e1782f11396ee5f7a5150c0f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 13 Jun 2023 00:09:02 GMT
ADD file:f91bd2a174259cb69646fc34ba2fc6b8941ad8e171d2d7952a4d8ac3d95e2ad7 in / 
# Tue, 13 Jun 2023 00:09:06 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 18:38:15 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 14 Jun 2023 18:38:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jun 2023 18:38:39 GMT
ENV MEMCACHED_VERSION=1.6.20
# Wed, 14 Jun 2023 18:38:41 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Wed, 14 Jun 2023 18:45:20 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 14 Jun 2023 18:45:23 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 14 Jun 2023 18:45:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Jun 2023 18:45:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 18:45:32 GMT
USER memcache
# Wed, 14 Jun 2023 18:45:35 GMT
EXPOSE 11211
# Wed, 14 Jun 2023 18:45:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3fc28260a4d871ef9781cad2bb064ad7212a5063de3a1d35dba938ce82115e5b`  
		Last Modified: Tue, 13 Jun 2023 00:22:29 GMT  
		Size: 29.1 MB (29118129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c804aeb794275ae845d32d2939d0e0fefa75cd112f1075aaf2104097050ae8`  
		Last Modified: Wed, 14 Jun 2023 18:46:04 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf29fcbe26928e2f4086a889098220505bdd4401dc87958f623ade0618efcd28`  
		Last Modified: Wed, 14 Jun 2023 18:46:05 GMT  
		Size: 1.9 MB (1934899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76d4e9cc234d41e69eba3bf411cb1d3ebe17e2fefbffb0c3458d613f2545337e`  
		Last Modified: Wed, 14 Jun 2023 18:46:09 GMT  
		Size: 6.5 MB (6499709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0988c34e4840378b9876eba362b50458e769389d0cc626698bef65e46c721458`  
		Last Modified: Wed, 14 Jun 2023 18:46:04 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db55745458426cdf0d23fd0589fd440e2d328e4d5ffb00a9ef6d2e0225cec8bf`  
		Last Modified: Wed, 14 Jun 2023 18:46:04 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:0e023c41d9c6a8d04edad22ecea59cfcf424d0dc3895c442a9e7a4575961d53d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43193448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a85a60b74a9575a203aba1a5f800dfe479b80cde8ff577ccd5e7e77bdaab64c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jun 2023 23:17:34 GMT
ADD file:3f8b9849acb625537f99921ef80190de7b03afdc287a5d1113a92cc41ae24be2 in / 
# Mon, 12 Jun 2023 23:17:36 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 18:15:42 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 14 Jun 2023 18:15:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jun 2023 18:15:50 GMT
ENV MEMCACHED_VERSION=1.6.20
# Wed, 14 Jun 2023 18:15:51 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Wed, 14 Jun 2023 18:19:27 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 14 Jun 2023 18:19:28 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 14 Jun 2023 18:19:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Jun 2023 18:19:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 18:19:31 GMT
USER memcache
# Wed, 14 Jun 2023 18:19:32 GMT
EXPOSE 11211
# Wed, 14 Jun 2023 18:19:32 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9f041b53cef30007c43057f2520876c85ed6bee6be5aaee867dfb31a053d6cca`  
		Last Modified: Mon, 12 Jun 2023 23:24:09 GMT  
		Size: 33.1 MB (33116725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a2d84b1fee81412bbd9bb301c77e6dfacfac70c2f1485de806658b49b06e08`  
		Last Modified: Wed, 14 Jun 2023 18:19:49 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca8bb5af043b48c9fe0e110ee13c139ceb715570346140fc86092d582d38b52b`  
		Last Modified: Wed, 14 Jun 2023 18:19:50 GMT  
		Size: 2.9 MB (2891306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e2d7805a151ec1618da95ad34cb2fdc6ae889b9f7908aaca6d063ca864f3e24`  
		Last Modified: Wed, 14 Jun 2023 18:19:52 GMT  
		Size: 7.2 MB (7183881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc5db4b315753422be0d08638f594b1ec64484c44f68942473f903387853b3bd`  
		Last Modified: Wed, 14 Jun 2023 18:19:49 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a8a9b2ed7c41d27d92f9db3c21beec2a2e288b0bc54a19aa1d3574b6085eaa6`  
		Last Modified: Wed, 14 Jun 2023 18:19:49 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:1.6`

```console
$ docker pull memcached@sha256:b98fa1ffaab2dcd8d970fe7030487920c8edc93b2a932f263bc4e0475d0ac2b3
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
$ docker pull memcached@sha256:533c607824b2f5781b179e175fcdf055577a3f076fb0a0fdcd13487c7c92125f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (38973406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbcfa8d0003c80b0bba4004f4b15b4a5600b9dd481ac2d887bc31e794f067464`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jun 2023 23:20:42 GMT
ADD file:ba1250b6ecd5dd09d4914189d72741c2817988994e7da514bf62be439a34bdb5 in / 
# Mon, 12 Jun 2023 23:20:42 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 20:48:19 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 14 Jun 2023 20:48:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jun 2023 20:48:24 GMT
ENV MEMCACHED_VERSION=1.6.20
# Wed, 14 Jun 2023 20:48:24 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Wed, 14 Jun 2023 20:50:40 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 14 Jun 2023 20:50:40 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 14 Jun 2023 20:50:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Jun 2023 20:50:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 20:50:41 GMT
USER memcache
# Wed, 14 Jun 2023 20:50:41 GMT
EXPOSE 11211
# Wed, 14 Jun 2023 20:50:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5b5fe70539cd6989aa19f25826309f9715a9489cf1c057982d6a84c1ad8975c7`  
		Last Modified: Mon, 12 Jun 2023 23:25:49 GMT  
		Size: 29.1 MB (29124744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab209434009a85e82d99c0547bb947940f9e1002ce6e965417396ee22a6820db`  
		Last Modified: Wed, 14 Jun 2023 20:53:33 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f4dfc49c9cdae8d4df855de7cc0460e5db8c762e73786d4f8fa4f69ba11d6d`  
		Last Modified: Wed, 14 Jun 2023 20:53:33 GMT  
		Size: 2.7 MB (2677239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96a3de0d22592d9a254814d5b77e3a84e73d2f055d162503fe811f731a320701`  
		Last Modified: Wed, 14 Jun 2023 20:53:34 GMT  
		Size: 7.2 MB (7169888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a38b201fb7fc8d917459453ee1c0218cf9845c96b885a02b02999f81b21c6bb`  
		Last Modified: Wed, 14 Jun 2023 20:53:33 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6f5720dc1980c886ee7e8d6067ed87e102bb31824e557a85fbd54273542debf`  
		Last Modified: Wed, 14 Jun 2023 20:53:33 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6` - linux; arm variant v5

```console
$ docker pull memcached@sha256:9dba87e9c87eb3058b7db8d6a35423e25ff2aaa7baabb27c5e6137017c48fe1a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 MB (30470602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:308667429b0aed213503576d9f474cc30e4f0181773f9cee3aa2ac42d3c74a7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jun 2023 23:48:46 GMT
ADD file:b2773fa62bdb5672863ef317ee1b58de2a6074fe6aa0d8287a7cd0999028d7d2 in / 
# Mon, 12 Jun 2023 23:48:47 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 04:08:38 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 13 Jun 2023 04:08:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 04:08:45 GMT
ENV MEMCACHED_VERSION=1.6.20
# Tue, 13 Jun 2023 04:08:45 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Tue, 13 Jun 2023 04:11:47 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 13 Jun 2023 04:11:47 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 13 Jun 2023 04:11:48 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 13 Jun 2023 04:11:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jun 2023 04:11:49 GMT
USER memcache
# Tue, 13 Jun 2023 04:11:49 GMT
EXPOSE 11211
# Tue, 13 Jun 2023 04:11:49 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c04d7d6633d9b8cf1bfa9f6831ac7dd6f985411cb6307d91c6373085b09b8c19`  
		Last Modified: Mon, 12 Jun 2023 23:52:06 GMT  
		Size: 28.9 MB (28918779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1860b36b146eb799ae5299a102c03f7c12063adcb754066bd9eab20450d0cebb`  
		Last Modified: Tue, 13 Jun 2023 04:12:05 GMT  
		Size: 4.9 KB (4890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:557508c54a290bb2d6fda92e97a2058bcc1de808bcca254bb1559ea268d1bc8c`  
		Last Modified: Tue, 13 Jun 2023 04:12:06 GMT  
		Size: 316.8 KB (316757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67839ee937c662a3b1177503ab80dd4b2c4f95b5d0a8ffdf33276e7e30eecc85`  
		Last Modified: Tue, 13 Jun 2023 04:12:06 GMT  
		Size: 1.2 MB (1229770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e2a90f0421d9b93e896ff2136b06e5d157fd43ccd4cd1d62da5d0f8ba0466d9`  
		Last Modified: Tue, 13 Jun 2023 04:12:05 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e85a558ae3e0a483e80e987991797c179374d3573bf62638af5a4e2b1fb3c730`  
		Last Modified: Tue, 13 Jun 2023 04:12:05 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6` - linux; arm variant v7

```console
$ docker pull memcached@sha256:2841be0a36134563966c09a6ed68b21053d20342ec8736cf92763c28077ead43
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28094215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cf74ffa940dd93988fc0beb6698c5796563c82a40b7dd668153969f64d2e6ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 09 Feb 2023 06:12:09 GMT
ADD file:5f1a343224e8486690bd90dd1e50c8d84b3d770c51bb6829544e5cf650c0419c in / 
# Thu, 09 Feb 2023 06:12:10 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 07:52:31 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Thu, 09 Feb 2023 07:52:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 07:52:35 GMT
ENV MEMCACHED_VERSION=1.6.18
# Thu, 09 Feb 2023 07:52:35 GMT
ENV MEMCACHED_SHA1=be16909bb75ab972ee5fe438312501de01c4725a
# Thu, 09 Feb 2023 07:55:44 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Thu, 09 Feb 2023 07:55:44 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 09 Feb 2023 07:55:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 09 Feb 2023 07:55:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Feb 2023 07:55:44 GMT
USER memcache
# Thu, 09 Feb 2023 07:55:45 GMT
EXPOSE 11211
# Thu, 09 Feb 2023 07:55:45 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:e7318f6106ad75d7d482ae9dddf4d927b0872ef3ddb6e1330aa691fc8d17279e`  
		Last Modified: Thu, 09 Feb 2023 06:19:19 GMT  
		Size: 26.6 MB (26577666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de49d9d72daf1680b5f1b9532dd2eb0162829f36c8db9669935462636fbf99d9`  
		Last Modified: Thu, 09 Feb 2023 08:06:11 GMT  
		Size: 4.9 KB (4895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0beac9d5bcac946f8c54c72b8a9c136914b1aa7a5fe2b8c3df4c7d8858ea6559`  
		Last Modified: Thu, 09 Feb 2023 08:06:11 GMT  
		Size: 312.1 KB (312088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4c9e5a265394e4c0f357779e6195a4e82d767a3691a0e77d427e56651c3e54a`  
		Last Modified: Thu, 09 Feb 2023 08:06:11 GMT  
		Size: 1.2 MB (1199163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ea82ad892fe1ae8623d84e32c8c027087cda8aa49e40d4546ed6942e471c60`  
		Last Modified: Thu, 09 Feb 2023 08:06:11 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2ae3bcdc0d114ba49a67df022b6f7215fc87f1f50e64939fcfbbec4eaadee5`  
		Last Modified: Thu, 09 Feb 2023 08:06:11 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:3464bfccdfad0dc788e056949d59fc0b665ec165654b3a8502a2f4a3868a3dc7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 MB (37872888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20f33353745665e05e1722aa9af40e06b3f58778f8e758e786eaad30054de61f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jun 2023 23:40:13 GMT
ADD file:f75c3fe22fec548b35a86a9a5802fdc97497f5d253cf630d65f13282169d3f3f in / 
# Mon, 12 Jun 2023 23:40:14 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 20:54:33 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 14 Jun 2023 20:54:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jun 2023 20:54:37 GMT
ENV MEMCACHED_VERSION=1.6.20
# Wed, 14 Jun 2023 20:54:37 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Wed, 14 Jun 2023 20:57:13 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 14 Jun 2023 20:57:13 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 14 Jun 2023 20:57:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Jun 2023 20:57:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 20:57:14 GMT
USER memcache
# Wed, 14 Jun 2023 20:57:14 GMT
EXPOSE 11211
# Wed, 14 Jun 2023 20:57:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:95039a22a7cc3ae41d71f075e6e09e91e8da850fb5f80aba2f4a09f254520539`  
		Last Modified: Mon, 12 Jun 2023 23:44:08 GMT  
		Size: 29.2 MB (29152534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6da70104cc8ee465752315034f04011354e6149243e2bc69b9da49e6855df4b8`  
		Last Modified: Wed, 14 Jun 2023 21:00:29 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a7b40152f53e05b8cbcfe09be5b1598fcc05cf4f9ffad3b296eca43305450da`  
		Last Modified: Wed, 14 Jun 2023 21:00:30 GMT  
		Size: 2.5 MB (2539179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bf09d04f9c61af195486f42915b137b8612584f982737f5e465d02648a6dc8a`  
		Last Modified: Wed, 14 Jun 2023 21:00:30 GMT  
		Size: 6.2 MB (6179640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e71555e51295eeceeab1a9ab6bebb21108fbbe59e01349857c51932deea0f64`  
		Last Modified: Wed, 14 Jun 2023 21:00:29 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15cd3195dbfc5cedaf71b7c156002599dfb94219b51f85c966a1bee80bc37e65`  
		Last Modified: Wed, 14 Jun 2023 21:00:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6` - linux; 386

```console
$ docker pull memcached@sha256:719a898d7d05b1981b584eaaadd22e357c8a3b1b53509053cb6cc089cd6a38e0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (33997029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae0070d643d6b72bec5cad5100ac31c4fcb9b3108bade974a59d9933c70bda21`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jun 2023 23:39:58 GMT
ADD file:440924fd31c090a7f5e3d36276d17574922eb3e8ececce333fa42f7a95bdd9ce in / 
# Mon, 12 Jun 2023 23:39:58 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 20:20:47 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 13 Jun 2023 20:20:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 20:20:52 GMT
ENV MEMCACHED_VERSION=1.6.20
# Tue, 13 Jun 2023 20:20:52 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Tue, 13 Jun 2023 20:24:26 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 13 Jun 2023 20:24:26 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 13 Jun 2023 20:24:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 13 Jun 2023 20:24:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jun 2023 20:24:27 GMT
USER memcache
# Tue, 13 Jun 2023 20:24:27 GMT
EXPOSE 11211
# Tue, 13 Jun 2023 20:24:27 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1646137eb700afc9e891c03fdf28d3f5bc489ef0200fdacc67beee837d48db7d`  
		Last Modified: Mon, 12 Jun 2023 23:47:07 GMT  
		Size: 32.4 MB (32397388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9622551bea561b9c36a4e6d3a95484a278b356138badefce3b9186fc736fd556`  
		Last Modified: Tue, 13 Jun 2023 20:25:00 GMT  
		Size: 4.9 KB (4894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c12401a5e374bfe8c291818c808a2425cd0b16ac8cd178a47c8bf5eea598755b`  
		Last Modified: Tue, 13 Jun 2023 20:25:00 GMT  
		Size: 336.8 KB (336783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c456f2d87234421d6c272fad6161dc85df8bac55c7ea1750d68a216dd1534ee`  
		Last Modified: Tue, 13 Jun 2023 20:25:11 GMT  
		Size: 1.3 MB (1257556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:178b408b1cbfa94c9656a36bf64bf57a8df765953c7ec4c7e224851c29d35f71`  
		Last Modified: Tue, 13 Jun 2023 20:25:00 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6210b196c4e58f73e538fc8b508a56ac8918a914f6da6fd95c9721389d06c0a9`  
		Last Modified: Tue, 13 Jun 2023 20:25:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6` - linux; mips64le

```console
$ docker pull memcached@sha256:d2855c4deb19365dd1c83b81c9e1fa36f7873cc8b3dd02f8f01de10200bf208e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37554221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7068fffc8ee0a4607e1586297977a273786efb52e1782f11396ee5f7a5150c0f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 13 Jun 2023 00:09:02 GMT
ADD file:f91bd2a174259cb69646fc34ba2fc6b8941ad8e171d2d7952a4d8ac3d95e2ad7 in / 
# Tue, 13 Jun 2023 00:09:06 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 18:38:15 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 14 Jun 2023 18:38:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jun 2023 18:38:39 GMT
ENV MEMCACHED_VERSION=1.6.20
# Wed, 14 Jun 2023 18:38:41 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Wed, 14 Jun 2023 18:45:20 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 14 Jun 2023 18:45:23 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 14 Jun 2023 18:45:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Jun 2023 18:45:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 18:45:32 GMT
USER memcache
# Wed, 14 Jun 2023 18:45:35 GMT
EXPOSE 11211
# Wed, 14 Jun 2023 18:45:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3fc28260a4d871ef9781cad2bb064ad7212a5063de3a1d35dba938ce82115e5b`  
		Last Modified: Tue, 13 Jun 2023 00:22:29 GMT  
		Size: 29.1 MB (29118129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c804aeb794275ae845d32d2939d0e0fefa75cd112f1075aaf2104097050ae8`  
		Last Modified: Wed, 14 Jun 2023 18:46:04 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf29fcbe26928e2f4086a889098220505bdd4401dc87958f623ade0618efcd28`  
		Last Modified: Wed, 14 Jun 2023 18:46:05 GMT  
		Size: 1.9 MB (1934899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76d4e9cc234d41e69eba3bf411cb1d3ebe17e2fefbffb0c3458d613f2545337e`  
		Last Modified: Wed, 14 Jun 2023 18:46:09 GMT  
		Size: 6.5 MB (6499709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0988c34e4840378b9876eba362b50458e769389d0cc626698bef65e46c721458`  
		Last Modified: Wed, 14 Jun 2023 18:46:04 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db55745458426cdf0d23fd0589fd440e2d328e4d5ffb00a9ef6d2e0225cec8bf`  
		Last Modified: Wed, 14 Jun 2023 18:46:04 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6` - linux; ppc64le

```console
$ docker pull memcached@sha256:0e023c41d9c6a8d04edad22ecea59cfcf424d0dc3895c442a9e7a4575961d53d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43193448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a85a60b74a9575a203aba1a5f800dfe479b80cde8ff577ccd5e7e77bdaab64c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jun 2023 23:17:34 GMT
ADD file:3f8b9849acb625537f99921ef80190de7b03afdc287a5d1113a92cc41ae24be2 in / 
# Mon, 12 Jun 2023 23:17:36 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 18:15:42 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 14 Jun 2023 18:15:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jun 2023 18:15:50 GMT
ENV MEMCACHED_VERSION=1.6.20
# Wed, 14 Jun 2023 18:15:51 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Wed, 14 Jun 2023 18:19:27 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 14 Jun 2023 18:19:28 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 14 Jun 2023 18:19:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Jun 2023 18:19:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 18:19:31 GMT
USER memcache
# Wed, 14 Jun 2023 18:19:32 GMT
EXPOSE 11211
# Wed, 14 Jun 2023 18:19:32 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9f041b53cef30007c43057f2520876c85ed6bee6be5aaee867dfb31a053d6cca`  
		Last Modified: Mon, 12 Jun 2023 23:24:09 GMT  
		Size: 33.1 MB (33116725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a2d84b1fee81412bbd9bb301c77e6dfacfac70c2f1485de806658b49b06e08`  
		Last Modified: Wed, 14 Jun 2023 18:19:49 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca8bb5af043b48c9fe0e110ee13c139ceb715570346140fc86092d582d38b52b`  
		Last Modified: Wed, 14 Jun 2023 18:19:50 GMT  
		Size: 2.9 MB (2891306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e2d7805a151ec1618da95ad34cb2fdc6ae889b9f7908aaca6d063ca864f3e24`  
		Last Modified: Wed, 14 Jun 2023 18:19:52 GMT  
		Size: 7.2 MB (7183881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc5db4b315753422be0d08638f594b1ec64484c44f68942473f903387853b3bd`  
		Last Modified: Wed, 14 Jun 2023 18:19:49 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a8a9b2ed7c41d27d92f9db3c21beec2a2e288b0bc54a19aa1d3574b6085eaa6`  
		Last Modified: Wed, 14 Jun 2023 18:19:49 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6` - linux; s390x

```console
$ docker pull memcached@sha256:882f9d1d57c58c374c6074cbce0784748bdce465757ad946f699a47a924f4518
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31228777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:098ff94df44cb535cdd4f10e4106756fc1766a232277b3a9c2f51ff567ee3082`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 13 Jun 2023 04:30:13 GMT
ADD file:558e8c34e969d458ce6bf4207d9c0fe05d2e67d3457c1d5689666749e82ef2ab in / 
# Tue, 13 Jun 2023 04:30:14 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 18:41:51 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 13 Jun 2023 18:41:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 18:41:54 GMT
ENV MEMCACHED_VERSION=1.6.20
# Tue, 13 Jun 2023 18:41:54 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Tue, 13 Jun 2023 18:44:58 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 13 Jun 2023 18:44:58 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 13 Jun 2023 18:44:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 13 Jun 2023 18:44:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jun 2023 18:44:59 GMT
USER memcache
# Tue, 13 Jun 2023 18:44:59 GMT
EXPOSE 11211
# Tue, 13 Jun 2023 18:44:59 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6a752e2308c741009b6f5a88a8ea6764b96ebe7f544197912d8ef9a3ec8c8763`  
		Last Modified: Tue, 13 Jun 2023 04:34:49 GMT  
		Size: 29.7 MB (29652514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:465e13673c57447925389cdcf074d61ff5114faa447fd3b775481a229ac38019`  
		Last Modified: Tue, 13 Jun 2023 18:45:27 GMT  
		Size: 5.0 KB (5023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a81fcab4fd1cd8ac9cc18539fde149b89e423f0b5c80f2f07460f49209907ca`  
		Last Modified: Tue, 13 Jun 2023 18:45:27 GMT  
		Size: 324.3 KB (324337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a035c15be3c1e4f3cd28a1c060f56d03f4fa02c5e86290288ac74b2533feca`  
		Last Modified: Tue, 13 Jun 2023 18:45:27 GMT  
		Size: 1.2 MB (1246496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdda04e27e25f6bf6f5489a28d36c1903052488bf96ee74f76b993a5926207b7`  
		Last Modified: Tue, 13 Jun 2023 18:45:27 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d62044b354beed912ecf01ba2d6b0efc230907a720539c8850809e2b76f9ac89`  
		Last Modified: Tue, 13 Jun 2023 18:45:27 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:1.6-alpine`

```console
$ docker pull memcached@sha256:dd03af6acd2f6e2fad2a24cb0db1c987074c6f968c2995c6d9920015efb243a7
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
$ docker pull memcached@sha256:a7a04bc20ec122d9f024dff57494853d5dc9705fb97af9170cc31a1f531dcaa5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4462373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15429daa972e1d57884e75ecc7f784564ae7cf089c25671dd118a0025f806b6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 20:50:58 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Wed, 14 Jun 2023 20:50:59 GMT
RUN apk add --no-cache libsasl
# Wed, 14 Jun 2023 20:50:59 GMT
ENV MEMCACHED_VERSION=1.6.20
# Wed, 14 Jun 2023 20:50:59 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Wed, 14 Jun 2023 20:53:09 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Wed, 14 Jun 2023 20:53:09 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 14 Jun 2023 20:53:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Jun 2023 20:53:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 20:53:09 GMT
USER memcache
# Wed, 14 Jun 2023 20:53:09 GMT
EXPOSE 11211
# Wed, 14 Jun 2023 20:53:09 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b2b2df106c5026cd33ea4ac655b77f25410ec9f4b8a6756ebc1ceeb79fca3c7`  
		Last Modified: Wed, 14 Jun 2023 20:53:58 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed63668528d3e2159f55909c66dc48a6f746ce24c2e2f6d963b992aefaa457ce`  
		Last Modified: Wed, 14 Jun 2023 20:53:58 GMT  
		Size: 108.1 KB (108080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc06ea6ffc2a4279c91e26e37b450afb1e0f1007815b19a7146d52b016dddc61`  
		Last Modified: Wed, 14 Jun 2023 20:53:59 GMT  
		Size: 954.7 KB (954748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:098e9e56712cb64736718f40b476d8eeb9410130c28ce94fe1bc2d380d9083cf`  
		Last Modified: Wed, 14 Jun 2023 20:53:59 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5c14818f6fb630a615284b18f945c89c0563530c25f07af955d0f85504020e9`  
		Last Modified: Wed, 14 Jun 2023 20:53:58 GMT  
		Size: 118.0 B  
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
$ docker pull memcached@sha256:e59934ff7bef6e6053b618f65923d2c1fa7235a008fb20f4fe9db13f8d6dc167
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4399194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dab6918acf63bcf26d1a95d40666c44f281aa14f0d4e27884d4c2f4b227dd9b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 20:57:26 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Wed, 14 Jun 2023 20:57:27 GMT
RUN apk add --no-cache libsasl
# Wed, 14 Jun 2023 20:57:27 GMT
ENV MEMCACHED_VERSION=1.6.20
# Wed, 14 Jun 2023 20:57:27 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Wed, 14 Jun 2023 20:59:54 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Wed, 14 Jun 2023 20:59:54 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 14 Jun 2023 20:59:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Jun 2023 20:59:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 20:59:55 GMT
USER memcache
# Wed, 14 Jun 2023 20:59:55 GMT
EXPOSE 11211
# Wed, 14 Jun 2023 20:59:55 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:666588188768f19b27fb821e02d084406af8fd867cc4595b896b9eed50b2105e`  
		Last Modified: Wed, 14 Jun 2023 21:00:51 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d958a137d671266f063c0af4d7b0b6d44d9018b77fdbddb8fd412d3c0b1be3`  
		Last Modified: Wed, 14 Jun 2023 21:00:51 GMT  
		Size: 124.1 KB (124137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eddee3cdc367d6f8265fe941f97020460db6cb5555711640b2ad62bd5c2a613c`  
		Last Modified: Wed, 14 Jun 2023 21:00:51 GMT  
		Size: 944.1 KB (944138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfec1ffcd9427d8fb06b908c1d3e0715a9db99c94c46f7896890a98b95c5f049`  
		Last Modified: Wed, 14 Jun 2023 21:00:51 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aea835bd4a5d779b88da37bc977813dd1ed9d228f5e78e3459edde4fa6f155e2`  
		Last Modified: Wed, 14 Jun 2023 21:00:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6-alpine` - linux; 386

```console
$ docker pull memcached@sha256:126e7a3993f53145ad966b11e0c8e7cb9f92520ea9899abfaa550aaee49c9f5c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4313116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:835ad308527d3b6bc85d49a990ae4c544363b3e3b3cef7a7a49ea6081d81a121`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 May 2023 23:11:03 GMT
ADD file:cfe47ebe49c4a75094234cafa52aa13aa26abcdad49b89293585884b3a8faeae in / 
# Tue, 09 May 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Thu, 11 May 2023 19:56:01 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Thu, 11 May 2023 19:56:03 GMT
RUN apk add --no-cache libsasl
# Mon, 15 May 2023 21:42:18 GMT
ENV MEMCACHED_VERSION=1.6.20
# Mon, 15 May 2023 21:42:18 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Mon, 15 May 2023 21:45:44 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Mon, 15 May 2023 21:45:44 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Mon, 15 May 2023 21:45:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 15 May 2023 21:45:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 15 May 2023 21:45:45 GMT
USER memcache
# Mon, 15 May 2023 21:45:45 GMT
EXPOSE 11211
# Mon, 15 May 2023 21:45:45 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:613767c5530f4016482e81288d0efdca4e58c62031252130d8fccd6f6260a068`  
		Last Modified: Tue, 09 May 2023 23:11:20 GMT  
		Size: 3.3 MB (3264862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72c25994ef1ec30cf62d081517b625d1ea87b0836bb6a90cd7ab8b1ab0501bb6`  
		Last Modified: Thu, 11 May 2023 20:00:35 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c42385514308725216c1a4eadb9aa4270c08f3140c342b6db43060f55af1ed`  
		Last Modified: Thu, 11 May 2023 20:00:35 GMT  
		Size: 109.5 KB (109521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3acbe617b4c6e3f32de32c1e69b84aa2c4e9c31d5e84a648a8340acda2452e03`  
		Last Modified: Mon, 15 May 2023 21:46:28 GMT  
		Size: 937.1 KB (937060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a81b72d4c28496fdd77fd3bf62a9800bd545660f44738482a100b00f99b3649c`  
		Last Modified: Mon, 15 May 2023 21:46:27 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c224abc2162f00f8769eeacb44838cbed654dd60d38e8d08d585003cb6495a`  
		Last Modified: Mon, 15 May 2023 21:46:27 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:912319e8c2e48db747d88d979ed43b691d125b7c05619189b4dcbe86f19b9a8b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4494043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c26bf354613881c6a96c357992e4176080f21ed4cac05a673e9a34056bd7d8be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 May 2023 23:11:09 GMT
ADD file:0a227602737a24c596923d3fd0a7c8b7d9000dbc6b80561473def09abbebbfa6 in / 
# Tue, 09 May 2023 23:11:10 GMT
CMD ["/bin/sh"]
# Thu, 11 May 2023 20:28:43 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Thu, 11 May 2023 20:28:45 GMT
RUN apk add --no-cache libsasl
# Mon, 15 May 2023 21:20:18 GMT
ENV MEMCACHED_VERSION=1.6.20
# Mon, 15 May 2023 21:20:18 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Mon, 15 May 2023 21:23:19 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Mon, 15 May 2023 21:23:19 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Mon, 15 May 2023 21:23:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 15 May 2023 21:23:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 15 May 2023 21:23:20 GMT
USER memcache
# Mon, 15 May 2023 21:23:20 GMT
EXPOSE 11211
# Mon, 15 May 2023 21:23:21 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5c0986f188e93dd7e76a4dc49a9170da2cd124709f5e1590b378e31a2b0d9587`  
		Last Modified: Tue, 09 May 2023 23:11:31 GMT  
		Size: 3.4 MB (3385631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2637efcb2bfb898454103e5536179d5f732cbddcd32f89c4ed51466ed8c6a14`  
		Last Modified: Thu, 11 May 2023 20:32:50 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45b064e3e507b9c35d5b605a606755605f7807236709d725567d0609ac53ee29`  
		Last Modified: Thu, 11 May 2023 20:32:50 GMT  
		Size: 123.9 KB (123933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a5d4f2fcda4a8d8a11f4f09bab2989aa2ec605ec585ed61bb4b519b62f5a47`  
		Last Modified: Mon, 15 May 2023 21:24:04 GMT  
		Size: 982.8 KB (982805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81d636c8d2e3e1cce3ec344ad3d21645a62a2c2286037cc287cd4e56c21d3fe7`  
		Last Modified: Mon, 15 May 2023 21:24:03 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca8ad226ad66d4c655b3b77ce26667f5b878d47000bfc558dae9c53ec6cff9b5`  
		Last Modified: Mon, 15 May 2023 21:24:03 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:029a3ea9286bc7541646e7ca99fb57db8faffea15abf7bee651ee5cac65c4732
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4290940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac9f545f21c06b546f33df533b248b59335e5960e61844e6729780e8c404af6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 May 2023 23:11:06 GMT
ADD file:89d6e366e8ab41011a5866f8ca43aac6cfef00edffebad565918ab632a6d6210 in / 
# Tue, 09 May 2023 23:11:07 GMT
CMD ["/bin/sh"]
# Thu, 11 May 2023 19:55:27 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Thu, 11 May 2023 19:55:28 GMT
RUN apk add --no-cache libsasl
# Mon, 15 May 2023 21:51:02 GMT
ENV MEMCACHED_VERSION=1.6.20
# Mon, 15 May 2023 21:51:02 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Mon, 15 May 2023 21:54:04 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Mon, 15 May 2023 21:54:04 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Mon, 15 May 2023 21:54:04 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 15 May 2023 21:54:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 15 May 2023 21:54:04 GMT
USER memcache
# Mon, 15 May 2023 21:54:05 GMT
EXPOSE 11211
# Mon, 15 May 2023 21:54:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:25da54cc0a08f4ca602c6bcd3e52d70082eb8a25ee022bc9f1dda019de49197a`  
		Last Modified: Tue, 09 May 2023 23:11:35 GMT  
		Size: 3.2 MB (3226303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b276b6acd2b3a86c684a2f6a3641c76b4e2e5b3ce67562b64266899a052e6d4d`  
		Last Modified: Thu, 11 May 2023 19:59:45 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:483fe7c616264b630bec3883deae3b95c3220c0d46c5440048f5f2372224979c`  
		Last Modified: Thu, 11 May 2023 19:59:45 GMT  
		Size: 112.8 KB (112850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19827c7b432b650815a5843027a98d18e43bbd207cdda86bc95dc2f55c69b498`  
		Last Modified: Mon, 15 May 2023 21:54:45 GMT  
		Size: 950.1 KB (950116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da2238a07815946f6ba0dcbb105f0a4dab9db865ab4696d5c561fdd473328147`  
		Last Modified: Mon, 15 May 2023 21:54:46 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03dc27afabfb97c92d4893b707ee04b92ec5dd5e64ce581e0c27d7b344d7e735`  
		Last Modified: Mon, 15 May 2023 21:54:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:1.6-alpine3.18`

```console
$ docker pull memcached@sha256:f9aad561ac4e31d347b252c0fef6beede071bdaa205e38dc9dc5369201d8ff47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `memcached:1.6-alpine3.18` - linux; amd64

```console
$ docker pull memcached@sha256:a7a04bc20ec122d9f024dff57494853d5dc9705fb97af9170cc31a1f531dcaa5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4462373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15429daa972e1d57884e75ecc7f784564ae7cf089c25671dd118a0025f806b6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 20:50:58 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Wed, 14 Jun 2023 20:50:59 GMT
RUN apk add --no-cache libsasl
# Wed, 14 Jun 2023 20:50:59 GMT
ENV MEMCACHED_VERSION=1.6.20
# Wed, 14 Jun 2023 20:50:59 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Wed, 14 Jun 2023 20:53:09 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Wed, 14 Jun 2023 20:53:09 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 14 Jun 2023 20:53:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Jun 2023 20:53:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 20:53:09 GMT
USER memcache
# Wed, 14 Jun 2023 20:53:09 GMT
EXPOSE 11211
# Wed, 14 Jun 2023 20:53:09 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b2b2df106c5026cd33ea4ac655b77f25410ec9f4b8a6756ebc1ceeb79fca3c7`  
		Last Modified: Wed, 14 Jun 2023 20:53:58 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed63668528d3e2159f55909c66dc48a6f746ce24c2e2f6d963b992aefaa457ce`  
		Last Modified: Wed, 14 Jun 2023 20:53:58 GMT  
		Size: 108.1 KB (108080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc06ea6ffc2a4279c91e26e37b450afb1e0f1007815b19a7146d52b016dddc61`  
		Last Modified: Wed, 14 Jun 2023 20:53:59 GMT  
		Size: 954.7 KB (954748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:098e9e56712cb64736718f40b476d8eeb9410130c28ce94fe1bc2d380d9083cf`  
		Last Modified: Wed, 14 Jun 2023 20:53:59 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5c14818f6fb630a615284b18f945c89c0563530c25f07af955d0f85504020e9`  
		Last Modified: Wed, 14 Jun 2023 20:53:58 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:e59934ff7bef6e6053b618f65923d2c1fa7235a008fb20f4fe9db13f8d6dc167
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4399194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dab6918acf63bcf26d1a95d40666c44f281aa14f0d4e27884d4c2f4b227dd9b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 20:57:26 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Wed, 14 Jun 2023 20:57:27 GMT
RUN apk add --no-cache libsasl
# Wed, 14 Jun 2023 20:57:27 GMT
ENV MEMCACHED_VERSION=1.6.20
# Wed, 14 Jun 2023 20:57:27 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Wed, 14 Jun 2023 20:59:54 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Wed, 14 Jun 2023 20:59:54 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 14 Jun 2023 20:59:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Jun 2023 20:59:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 20:59:55 GMT
USER memcache
# Wed, 14 Jun 2023 20:59:55 GMT
EXPOSE 11211
# Wed, 14 Jun 2023 20:59:55 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:666588188768f19b27fb821e02d084406af8fd867cc4595b896b9eed50b2105e`  
		Last Modified: Wed, 14 Jun 2023 21:00:51 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d958a137d671266f063c0af4d7b0b6d44d9018b77fdbddb8fd412d3c0b1be3`  
		Last Modified: Wed, 14 Jun 2023 21:00:51 GMT  
		Size: 124.1 KB (124137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eddee3cdc367d6f8265fe941f97020460db6cb5555711640b2ad62bd5c2a613c`  
		Last Modified: Wed, 14 Jun 2023 21:00:51 GMT  
		Size: 944.1 KB (944138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfec1ffcd9427d8fb06b908c1d3e0715a9db99c94c46f7896890a98b95c5f049`  
		Last Modified: Wed, 14 Jun 2023 21:00:51 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aea835bd4a5d779b88da37bc977813dd1ed9d228f5e78e3459edde4fa6f155e2`  
		Last Modified: Wed, 14 Jun 2023 21:00:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6-alpine3.18` - linux; 386

```console
$ docker pull memcached@sha256:126e7a3993f53145ad966b11e0c8e7cb9f92520ea9899abfaa550aaee49c9f5c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4313116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:835ad308527d3b6bc85d49a990ae4c544363b3e3b3cef7a7a49ea6081d81a121`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 May 2023 23:11:03 GMT
ADD file:cfe47ebe49c4a75094234cafa52aa13aa26abcdad49b89293585884b3a8faeae in / 
# Tue, 09 May 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Thu, 11 May 2023 19:56:01 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Thu, 11 May 2023 19:56:03 GMT
RUN apk add --no-cache libsasl
# Mon, 15 May 2023 21:42:18 GMT
ENV MEMCACHED_VERSION=1.6.20
# Mon, 15 May 2023 21:42:18 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Mon, 15 May 2023 21:45:44 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Mon, 15 May 2023 21:45:44 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Mon, 15 May 2023 21:45:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 15 May 2023 21:45:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 15 May 2023 21:45:45 GMT
USER memcache
# Mon, 15 May 2023 21:45:45 GMT
EXPOSE 11211
# Mon, 15 May 2023 21:45:45 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:613767c5530f4016482e81288d0efdca4e58c62031252130d8fccd6f6260a068`  
		Last Modified: Tue, 09 May 2023 23:11:20 GMT  
		Size: 3.3 MB (3264862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72c25994ef1ec30cf62d081517b625d1ea87b0836bb6a90cd7ab8b1ab0501bb6`  
		Last Modified: Thu, 11 May 2023 20:00:35 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c42385514308725216c1a4eadb9aa4270c08f3140c342b6db43060f55af1ed`  
		Last Modified: Thu, 11 May 2023 20:00:35 GMT  
		Size: 109.5 KB (109521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3acbe617b4c6e3f32de32c1e69b84aa2c4e9c31d5e84a648a8340acda2452e03`  
		Last Modified: Mon, 15 May 2023 21:46:28 GMT  
		Size: 937.1 KB (937060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a81b72d4c28496fdd77fd3bf62a9800bd545660f44738482a100b00f99b3649c`  
		Last Modified: Mon, 15 May 2023 21:46:27 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c224abc2162f00f8769eeacb44838cbed654dd60d38e8d08d585003cb6495a`  
		Last Modified: Mon, 15 May 2023 21:46:27 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6-alpine3.18` - linux; ppc64le

```console
$ docker pull memcached@sha256:912319e8c2e48db747d88d979ed43b691d125b7c05619189b4dcbe86f19b9a8b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4494043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c26bf354613881c6a96c357992e4176080f21ed4cac05a673e9a34056bd7d8be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 May 2023 23:11:09 GMT
ADD file:0a227602737a24c596923d3fd0a7c8b7d9000dbc6b80561473def09abbebbfa6 in / 
# Tue, 09 May 2023 23:11:10 GMT
CMD ["/bin/sh"]
# Thu, 11 May 2023 20:28:43 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Thu, 11 May 2023 20:28:45 GMT
RUN apk add --no-cache libsasl
# Mon, 15 May 2023 21:20:18 GMT
ENV MEMCACHED_VERSION=1.6.20
# Mon, 15 May 2023 21:20:18 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Mon, 15 May 2023 21:23:19 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Mon, 15 May 2023 21:23:19 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Mon, 15 May 2023 21:23:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 15 May 2023 21:23:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 15 May 2023 21:23:20 GMT
USER memcache
# Mon, 15 May 2023 21:23:20 GMT
EXPOSE 11211
# Mon, 15 May 2023 21:23:21 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5c0986f188e93dd7e76a4dc49a9170da2cd124709f5e1590b378e31a2b0d9587`  
		Last Modified: Tue, 09 May 2023 23:11:31 GMT  
		Size: 3.4 MB (3385631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2637efcb2bfb898454103e5536179d5f732cbddcd32f89c4ed51466ed8c6a14`  
		Last Modified: Thu, 11 May 2023 20:32:50 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45b064e3e507b9c35d5b605a606755605f7807236709d725567d0609ac53ee29`  
		Last Modified: Thu, 11 May 2023 20:32:50 GMT  
		Size: 123.9 KB (123933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a5d4f2fcda4a8d8a11f4f09bab2989aa2ec605ec585ed61bb4b519b62f5a47`  
		Last Modified: Mon, 15 May 2023 21:24:04 GMT  
		Size: 982.8 KB (982805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81d636c8d2e3e1cce3ec344ad3d21645a62a2c2286037cc287cd4e56c21d3fe7`  
		Last Modified: Mon, 15 May 2023 21:24:03 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca8ad226ad66d4c655b3b77ce26667f5b878d47000bfc558dae9c53ec6cff9b5`  
		Last Modified: Mon, 15 May 2023 21:24:03 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6-alpine3.18` - linux; s390x

```console
$ docker pull memcached@sha256:029a3ea9286bc7541646e7ca99fb57db8faffea15abf7bee651ee5cac65c4732
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4290940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac9f545f21c06b546f33df533b248b59335e5960e61844e6729780e8c404af6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 May 2023 23:11:06 GMT
ADD file:89d6e366e8ab41011a5866f8ca43aac6cfef00edffebad565918ab632a6d6210 in / 
# Tue, 09 May 2023 23:11:07 GMT
CMD ["/bin/sh"]
# Thu, 11 May 2023 19:55:27 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Thu, 11 May 2023 19:55:28 GMT
RUN apk add --no-cache libsasl
# Mon, 15 May 2023 21:51:02 GMT
ENV MEMCACHED_VERSION=1.6.20
# Mon, 15 May 2023 21:51:02 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Mon, 15 May 2023 21:54:04 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Mon, 15 May 2023 21:54:04 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Mon, 15 May 2023 21:54:04 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 15 May 2023 21:54:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 15 May 2023 21:54:04 GMT
USER memcache
# Mon, 15 May 2023 21:54:05 GMT
EXPOSE 11211
# Mon, 15 May 2023 21:54:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:25da54cc0a08f4ca602c6bcd3e52d70082eb8a25ee022bc9f1dda019de49197a`  
		Last Modified: Tue, 09 May 2023 23:11:35 GMT  
		Size: 3.2 MB (3226303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b276b6acd2b3a86c684a2f6a3641c76b4e2e5b3ce67562b64266899a052e6d4d`  
		Last Modified: Thu, 11 May 2023 19:59:45 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:483fe7c616264b630bec3883deae3b95c3220c0d46c5440048f5f2372224979c`  
		Last Modified: Thu, 11 May 2023 19:59:45 GMT  
		Size: 112.8 KB (112850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19827c7b432b650815a5843027a98d18e43bbd207cdda86bc95dc2f55c69b498`  
		Last Modified: Mon, 15 May 2023 21:54:45 GMT  
		Size: 950.1 KB (950116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da2238a07815946f6ba0dcbb105f0a4dab9db865ab4696d5c561fdd473328147`  
		Last Modified: Mon, 15 May 2023 21:54:46 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03dc27afabfb97c92d4893b707ee04b92ec5dd5e64ce581e0c27d7b344d7e735`  
		Last Modified: Mon, 15 May 2023 21:54:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:1.6-bookworm`

```console
$ docker pull memcached@sha256:0495a71949e29a0dd91782be635586b244a336a765e79c78cfea895cd541e312
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; mips64le
	-	linux; ppc64le

### `memcached:1.6-bookworm` - linux; amd64

```console
$ docker pull memcached@sha256:533c607824b2f5781b179e175fcdf055577a3f076fb0a0fdcd13487c7c92125f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (38973406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbcfa8d0003c80b0bba4004f4b15b4a5600b9dd481ac2d887bc31e794f067464`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jun 2023 23:20:42 GMT
ADD file:ba1250b6ecd5dd09d4914189d72741c2817988994e7da514bf62be439a34bdb5 in / 
# Mon, 12 Jun 2023 23:20:42 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 20:48:19 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 14 Jun 2023 20:48:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jun 2023 20:48:24 GMT
ENV MEMCACHED_VERSION=1.6.20
# Wed, 14 Jun 2023 20:48:24 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Wed, 14 Jun 2023 20:50:40 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 14 Jun 2023 20:50:40 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 14 Jun 2023 20:50:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Jun 2023 20:50:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 20:50:41 GMT
USER memcache
# Wed, 14 Jun 2023 20:50:41 GMT
EXPOSE 11211
# Wed, 14 Jun 2023 20:50:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5b5fe70539cd6989aa19f25826309f9715a9489cf1c057982d6a84c1ad8975c7`  
		Last Modified: Mon, 12 Jun 2023 23:25:49 GMT  
		Size: 29.1 MB (29124744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab209434009a85e82d99c0547bb947940f9e1002ce6e965417396ee22a6820db`  
		Last Modified: Wed, 14 Jun 2023 20:53:33 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f4dfc49c9cdae8d4df855de7cc0460e5db8c762e73786d4f8fa4f69ba11d6d`  
		Last Modified: Wed, 14 Jun 2023 20:53:33 GMT  
		Size: 2.7 MB (2677239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96a3de0d22592d9a254814d5b77e3a84e73d2f055d162503fe811f731a320701`  
		Last Modified: Wed, 14 Jun 2023 20:53:34 GMT  
		Size: 7.2 MB (7169888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a38b201fb7fc8d917459453ee1c0218cf9845c96b885a02b02999f81b21c6bb`  
		Last Modified: Wed, 14 Jun 2023 20:53:33 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6f5720dc1980c886ee7e8d6067ed87e102bb31824e557a85fbd54273542debf`  
		Last Modified: Wed, 14 Jun 2023 20:53:33 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:3464bfccdfad0dc788e056949d59fc0b665ec165654b3a8502a2f4a3868a3dc7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 MB (37872888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20f33353745665e05e1722aa9af40e06b3f58778f8e758e786eaad30054de61f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jun 2023 23:40:13 GMT
ADD file:f75c3fe22fec548b35a86a9a5802fdc97497f5d253cf630d65f13282169d3f3f in / 
# Mon, 12 Jun 2023 23:40:14 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 20:54:33 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 14 Jun 2023 20:54:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jun 2023 20:54:37 GMT
ENV MEMCACHED_VERSION=1.6.20
# Wed, 14 Jun 2023 20:54:37 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Wed, 14 Jun 2023 20:57:13 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 14 Jun 2023 20:57:13 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 14 Jun 2023 20:57:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Jun 2023 20:57:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 20:57:14 GMT
USER memcache
# Wed, 14 Jun 2023 20:57:14 GMT
EXPOSE 11211
# Wed, 14 Jun 2023 20:57:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:95039a22a7cc3ae41d71f075e6e09e91e8da850fb5f80aba2f4a09f254520539`  
		Last Modified: Mon, 12 Jun 2023 23:44:08 GMT  
		Size: 29.2 MB (29152534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6da70104cc8ee465752315034f04011354e6149243e2bc69b9da49e6855df4b8`  
		Last Modified: Wed, 14 Jun 2023 21:00:29 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a7b40152f53e05b8cbcfe09be5b1598fcc05cf4f9ffad3b296eca43305450da`  
		Last Modified: Wed, 14 Jun 2023 21:00:30 GMT  
		Size: 2.5 MB (2539179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bf09d04f9c61af195486f42915b137b8612584f982737f5e465d02648a6dc8a`  
		Last Modified: Wed, 14 Jun 2023 21:00:30 GMT  
		Size: 6.2 MB (6179640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e71555e51295eeceeab1a9ab6bebb21108fbbe59e01349857c51932deea0f64`  
		Last Modified: Wed, 14 Jun 2023 21:00:29 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15cd3195dbfc5cedaf71b7c156002599dfb94219b51f85c966a1bee80bc37e65`  
		Last Modified: Wed, 14 Jun 2023 21:00:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:d2855c4deb19365dd1c83b81c9e1fa36f7873cc8b3dd02f8f01de10200bf208e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37554221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7068fffc8ee0a4607e1586297977a273786efb52e1782f11396ee5f7a5150c0f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 13 Jun 2023 00:09:02 GMT
ADD file:f91bd2a174259cb69646fc34ba2fc6b8941ad8e171d2d7952a4d8ac3d95e2ad7 in / 
# Tue, 13 Jun 2023 00:09:06 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 18:38:15 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 14 Jun 2023 18:38:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jun 2023 18:38:39 GMT
ENV MEMCACHED_VERSION=1.6.20
# Wed, 14 Jun 2023 18:38:41 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Wed, 14 Jun 2023 18:45:20 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 14 Jun 2023 18:45:23 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 14 Jun 2023 18:45:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Jun 2023 18:45:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 18:45:32 GMT
USER memcache
# Wed, 14 Jun 2023 18:45:35 GMT
EXPOSE 11211
# Wed, 14 Jun 2023 18:45:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3fc28260a4d871ef9781cad2bb064ad7212a5063de3a1d35dba938ce82115e5b`  
		Last Modified: Tue, 13 Jun 2023 00:22:29 GMT  
		Size: 29.1 MB (29118129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c804aeb794275ae845d32d2939d0e0fefa75cd112f1075aaf2104097050ae8`  
		Last Modified: Wed, 14 Jun 2023 18:46:04 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf29fcbe26928e2f4086a889098220505bdd4401dc87958f623ade0618efcd28`  
		Last Modified: Wed, 14 Jun 2023 18:46:05 GMT  
		Size: 1.9 MB (1934899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76d4e9cc234d41e69eba3bf411cb1d3ebe17e2fefbffb0c3458d613f2545337e`  
		Last Modified: Wed, 14 Jun 2023 18:46:09 GMT  
		Size: 6.5 MB (6499709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0988c34e4840378b9876eba362b50458e769389d0cc626698bef65e46c721458`  
		Last Modified: Wed, 14 Jun 2023 18:46:04 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db55745458426cdf0d23fd0589fd440e2d328e4d5ffb00a9ef6d2e0225cec8bf`  
		Last Modified: Wed, 14 Jun 2023 18:46:04 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:0e023c41d9c6a8d04edad22ecea59cfcf424d0dc3895c442a9e7a4575961d53d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43193448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a85a60b74a9575a203aba1a5f800dfe479b80cde8ff577ccd5e7e77bdaab64c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jun 2023 23:17:34 GMT
ADD file:3f8b9849acb625537f99921ef80190de7b03afdc287a5d1113a92cc41ae24be2 in / 
# Mon, 12 Jun 2023 23:17:36 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 18:15:42 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 14 Jun 2023 18:15:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jun 2023 18:15:50 GMT
ENV MEMCACHED_VERSION=1.6.20
# Wed, 14 Jun 2023 18:15:51 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Wed, 14 Jun 2023 18:19:27 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 14 Jun 2023 18:19:28 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 14 Jun 2023 18:19:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Jun 2023 18:19:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 18:19:31 GMT
USER memcache
# Wed, 14 Jun 2023 18:19:32 GMT
EXPOSE 11211
# Wed, 14 Jun 2023 18:19:32 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9f041b53cef30007c43057f2520876c85ed6bee6be5aaee867dfb31a053d6cca`  
		Last Modified: Mon, 12 Jun 2023 23:24:09 GMT  
		Size: 33.1 MB (33116725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a2d84b1fee81412bbd9bb301c77e6dfacfac70c2f1485de806658b49b06e08`  
		Last Modified: Wed, 14 Jun 2023 18:19:49 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca8bb5af043b48c9fe0e110ee13c139ceb715570346140fc86092d582d38b52b`  
		Last Modified: Wed, 14 Jun 2023 18:19:50 GMT  
		Size: 2.9 MB (2891306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e2d7805a151ec1618da95ad34cb2fdc6ae889b9f7908aaca6d063ca864f3e24`  
		Last Modified: Wed, 14 Jun 2023 18:19:52 GMT  
		Size: 7.2 MB (7183881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc5db4b315753422be0d08638f594b1ec64484c44f68942473f903387853b3bd`  
		Last Modified: Wed, 14 Jun 2023 18:19:49 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a8a9b2ed7c41d27d92f9db3c21beec2a2e288b0bc54a19aa1d3574b6085eaa6`  
		Last Modified: Wed, 14 Jun 2023 18:19:49 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:1.6.20`

```console
$ docker pull memcached@sha256:cf0e777f77ae9a11bf3d945f8586a49d7e0fc6ecb812c3b4194e18680d87e745
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `memcached:1.6.20` - linux; amd64

```console
$ docker pull memcached@sha256:533c607824b2f5781b179e175fcdf055577a3f076fb0a0fdcd13487c7c92125f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (38973406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbcfa8d0003c80b0bba4004f4b15b4a5600b9dd481ac2d887bc31e794f067464`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jun 2023 23:20:42 GMT
ADD file:ba1250b6ecd5dd09d4914189d72741c2817988994e7da514bf62be439a34bdb5 in / 
# Mon, 12 Jun 2023 23:20:42 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 20:48:19 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 14 Jun 2023 20:48:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jun 2023 20:48:24 GMT
ENV MEMCACHED_VERSION=1.6.20
# Wed, 14 Jun 2023 20:48:24 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Wed, 14 Jun 2023 20:50:40 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 14 Jun 2023 20:50:40 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 14 Jun 2023 20:50:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Jun 2023 20:50:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 20:50:41 GMT
USER memcache
# Wed, 14 Jun 2023 20:50:41 GMT
EXPOSE 11211
# Wed, 14 Jun 2023 20:50:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5b5fe70539cd6989aa19f25826309f9715a9489cf1c057982d6a84c1ad8975c7`  
		Last Modified: Mon, 12 Jun 2023 23:25:49 GMT  
		Size: 29.1 MB (29124744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab209434009a85e82d99c0547bb947940f9e1002ce6e965417396ee22a6820db`  
		Last Modified: Wed, 14 Jun 2023 20:53:33 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f4dfc49c9cdae8d4df855de7cc0460e5db8c762e73786d4f8fa4f69ba11d6d`  
		Last Modified: Wed, 14 Jun 2023 20:53:33 GMT  
		Size: 2.7 MB (2677239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96a3de0d22592d9a254814d5b77e3a84e73d2f055d162503fe811f731a320701`  
		Last Modified: Wed, 14 Jun 2023 20:53:34 GMT  
		Size: 7.2 MB (7169888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a38b201fb7fc8d917459453ee1c0218cf9845c96b885a02b02999f81b21c6bb`  
		Last Modified: Wed, 14 Jun 2023 20:53:33 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6f5720dc1980c886ee7e8d6067ed87e102bb31824e557a85fbd54273542debf`  
		Last Modified: Wed, 14 Jun 2023 20:53:33 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.20` - linux; arm variant v5

```console
$ docker pull memcached@sha256:9dba87e9c87eb3058b7db8d6a35423e25ff2aaa7baabb27c5e6137017c48fe1a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 MB (30470602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:308667429b0aed213503576d9f474cc30e4f0181773f9cee3aa2ac42d3c74a7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jun 2023 23:48:46 GMT
ADD file:b2773fa62bdb5672863ef317ee1b58de2a6074fe6aa0d8287a7cd0999028d7d2 in / 
# Mon, 12 Jun 2023 23:48:47 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 04:08:38 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 13 Jun 2023 04:08:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 04:08:45 GMT
ENV MEMCACHED_VERSION=1.6.20
# Tue, 13 Jun 2023 04:08:45 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Tue, 13 Jun 2023 04:11:47 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 13 Jun 2023 04:11:47 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 13 Jun 2023 04:11:48 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 13 Jun 2023 04:11:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jun 2023 04:11:49 GMT
USER memcache
# Tue, 13 Jun 2023 04:11:49 GMT
EXPOSE 11211
# Tue, 13 Jun 2023 04:11:49 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c04d7d6633d9b8cf1bfa9f6831ac7dd6f985411cb6307d91c6373085b09b8c19`  
		Last Modified: Mon, 12 Jun 2023 23:52:06 GMT  
		Size: 28.9 MB (28918779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1860b36b146eb799ae5299a102c03f7c12063adcb754066bd9eab20450d0cebb`  
		Last Modified: Tue, 13 Jun 2023 04:12:05 GMT  
		Size: 4.9 KB (4890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:557508c54a290bb2d6fda92e97a2058bcc1de808bcca254bb1559ea268d1bc8c`  
		Last Modified: Tue, 13 Jun 2023 04:12:06 GMT  
		Size: 316.8 KB (316757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67839ee937c662a3b1177503ab80dd4b2c4f95b5d0a8ffdf33276e7e30eecc85`  
		Last Modified: Tue, 13 Jun 2023 04:12:06 GMT  
		Size: 1.2 MB (1229770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e2a90f0421d9b93e896ff2136b06e5d157fd43ccd4cd1d62da5d0f8ba0466d9`  
		Last Modified: Tue, 13 Jun 2023 04:12:05 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e85a558ae3e0a483e80e987991797c179374d3573bf62638af5a4e2b1fb3c730`  
		Last Modified: Tue, 13 Jun 2023 04:12:05 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.20` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:3464bfccdfad0dc788e056949d59fc0b665ec165654b3a8502a2f4a3868a3dc7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 MB (37872888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20f33353745665e05e1722aa9af40e06b3f58778f8e758e786eaad30054de61f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jun 2023 23:40:13 GMT
ADD file:f75c3fe22fec548b35a86a9a5802fdc97497f5d253cf630d65f13282169d3f3f in / 
# Mon, 12 Jun 2023 23:40:14 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 20:54:33 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 14 Jun 2023 20:54:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jun 2023 20:54:37 GMT
ENV MEMCACHED_VERSION=1.6.20
# Wed, 14 Jun 2023 20:54:37 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Wed, 14 Jun 2023 20:57:13 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 14 Jun 2023 20:57:13 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 14 Jun 2023 20:57:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Jun 2023 20:57:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 20:57:14 GMT
USER memcache
# Wed, 14 Jun 2023 20:57:14 GMT
EXPOSE 11211
# Wed, 14 Jun 2023 20:57:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:95039a22a7cc3ae41d71f075e6e09e91e8da850fb5f80aba2f4a09f254520539`  
		Last Modified: Mon, 12 Jun 2023 23:44:08 GMT  
		Size: 29.2 MB (29152534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6da70104cc8ee465752315034f04011354e6149243e2bc69b9da49e6855df4b8`  
		Last Modified: Wed, 14 Jun 2023 21:00:29 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a7b40152f53e05b8cbcfe09be5b1598fcc05cf4f9ffad3b296eca43305450da`  
		Last Modified: Wed, 14 Jun 2023 21:00:30 GMT  
		Size: 2.5 MB (2539179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bf09d04f9c61af195486f42915b137b8612584f982737f5e465d02648a6dc8a`  
		Last Modified: Wed, 14 Jun 2023 21:00:30 GMT  
		Size: 6.2 MB (6179640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e71555e51295eeceeab1a9ab6bebb21108fbbe59e01349857c51932deea0f64`  
		Last Modified: Wed, 14 Jun 2023 21:00:29 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15cd3195dbfc5cedaf71b7c156002599dfb94219b51f85c966a1bee80bc37e65`  
		Last Modified: Wed, 14 Jun 2023 21:00:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.20` - linux; 386

```console
$ docker pull memcached@sha256:719a898d7d05b1981b584eaaadd22e357c8a3b1b53509053cb6cc089cd6a38e0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (33997029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae0070d643d6b72bec5cad5100ac31c4fcb9b3108bade974a59d9933c70bda21`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jun 2023 23:39:58 GMT
ADD file:440924fd31c090a7f5e3d36276d17574922eb3e8ececce333fa42f7a95bdd9ce in / 
# Mon, 12 Jun 2023 23:39:58 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 20:20:47 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 13 Jun 2023 20:20:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 20:20:52 GMT
ENV MEMCACHED_VERSION=1.6.20
# Tue, 13 Jun 2023 20:20:52 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Tue, 13 Jun 2023 20:24:26 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 13 Jun 2023 20:24:26 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 13 Jun 2023 20:24:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 13 Jun 2023 20:24:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jun 2023 20:24:27 GMT
USER memcache
# Tue, 13 Jun 2023 20:24:27 GMT
EXPOSE 11211
# Tue, 13 Jun 2023 20:24:27 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1646137eb700afc9e891c03fdf28d3f5bc489ef0200fdacc67beee837d48db7d`  
		Last Modified: Mon, 12 Jun 2023 23:47:07 GMT  
		Size: 32.4 MB (32397388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9622551bea561b9c36a4e6d3a95484a278b356138badefce3b9186fc736fd556`  
		Last Modified: Tue, 13 Jun 2023 20:25:00 GMT  
		Size: 4.9 KB (4894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c12401a5e374bfe8c291818c808a2425cd0b16ac8cd178a47c8bf5eea598755b`  
		Last Modified: Tue, 13 Jun 2023 20:25:00 GMT  
		Size: 336.8 KB (336783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c456f2d87234421d6c272fad6161dc85df8bac55c7ea1750d68a216dd1534ee`  
		Last Modified: Tue, 13 Jun 2023 20:25:11 GMT  
		Size: 1.3 MB (1257556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:178b408b1cbfa94c9656a36bf64bf57a8df765953c7ec4c7e224851c29d35f71`  
		Last Modified: Tue, 13 Jun 2023 20:25:00 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6210b196c4e58f73e538fc8b508a56ac8918a914f6da6fd95c9721389d06c0a9`  
		Last Modified: Tue, 13 Jun 2023 20:25:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.20` - linux; mips64le

```console
$ docker pull memcached@sha256:d2855c4deb19365dd1c83b81c9e1fa36f7873cc8b3dd02f8f01de10200bf208e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37554221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7068fffc8ee0a4607e1586297977a273786efb52e1782f11396ee5f7a5150c0f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 13 Jun 2023 00:09:02 GMT
ADD file:f91bd2a174259cb69646fc34ba2fc6b8941ad8e171d2d7952a4d8ac3d95e2ad7 in / 
# Tue, 13 Jun 2023 00:09:06 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 18:38:15 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 14 Jun 2023 18:38:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jun 2023 18:38:39 GMT
ENV MEMCACHED_VERSION=1.6.20
# Wed, 14 Jun 2023 18:38:41 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Wed, 14 Jun 2023 18:45:20 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 14 Jun 2023 18:45:23 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 14 Jun 2023 18:45:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Jun 2023 18:45:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 18:45:32 GMT
USER memcache
# Wed, 14 Jun 2023 18:45:35 GMT
EXPOSE 11211
# Wed, 14 Jun 2023 18:45:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3fc28260a4d871ef9781cad2bb064ad7212a5063de3a1d35dba938ce82115e5b`  
		Last Modified: Tue, 13 Jun 2023 00:22:29 GMT  
		Size: 29.1 MB (29118129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c804aeb794275ae845d32d2939d0e0fefa75cd112f1075aaf2104097050ae8`  
		Last Modified: Wed, 14 Jun 2023 18:46:04 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf29fcbe26928e2f4086a889098220505bdd4401dc87958f623ade0618efcd28`  
		Last Modified: Wed, 14 Jun 2023 18:46:05 GMT  
		Size: 1.9 MB (1934899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76d4e9cc234d41e69eba3bf411cb1d3ebe17e2fefbffb0c3458d613f2545337e`  
		Last Modified: Wed, 14 Jun 2023 18:46:09 GMT  
		Size: 6.5 MB (6499709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0988c34e4840378b9876eba362b50458e769389d0cc626698bef65e46c721458`  
		Last Modified: Wed, 14 Jun 2023 18:46:04 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db55745458426cdf0d23fd0589fd440e2d328e4d5ffb00a9ef6d2e0225cec8bf`  
		Last Modified: Wed, 14 Jun 2023 18:46:04 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.20` - linux; ppc64le

```console
$ docker pull memcached@sha256:0e023c41d9c6a8d04edad22ecea59cfcf424d0dc3895c442a9e7a4575961d53d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43193448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a85a60b74a9575a203aba1a5f800dfe479b80cde8ff577ccd5e7e77bdaab64c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jun 2023 23:17:34 GMT
ADD file:3f8b9849acb625537f99921ef80190de7b03afdc287a5d1113a92cc41ae24be2 in / 
# Mon, 12 Jun 2023 23:17:36 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 18:15:42 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 14 Jun 2023 18:15:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jun 2023 18:15:50 GMT
ENV MEMCACHED_VERSION=1.6.20
# Wed, 14 Jun 2023 18:15:51 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Wed, 14 Jun 2023 18:19:27 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 14 Jun 2023 18:19:28 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 14 Jun 2023 18:19:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Jun 2023 18:19:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 18:19:31 GMT
USER memcache
# Wed, 14 Jun 2023 18:19:32 GMT
EXPOSE 11211
# Wed, 14 Jun 2023 18:19:32 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9f041b53cef30007c43057f2520876c85ed6bee6be5aaee867dfb31a053d6cca`  
		Last Modified: Mon, 12 Jun 2023 23:24:09 GMT  
		Size: 33.1 MB (33116725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a2d84b1fee81412bbd9bb301c77e6dfacfac70c2f1485de806658b49b06e08`  
		Last Modified: Wed, 14 Jun 2023 18:19:49 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca8bb5af043b48c9fe0e110ee13c139ceb715570346140fc86092d582d38b52b`  
		Last Modified: Wed, 14 Jun 2023 18:19:50 GMT  
		Size: 2.9 MB (2891306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e2d7805a151ec1618da95ad34cb2fdc6ae889b9f7908aaca6d063ca864f3e24`  
		Last Modified: Wed, 14 Jun 2023 18:19:52 GMT  
		Size: 7.2 MB (7183881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc5db4b315753422be0d08638f594b1ec64484c44f68942473f903387853b3bd`  
		Last Modified: Wed, 14 Jun 2023 18:19:49 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a8a9b2ed7c41d27d92f9db3c21beec2a2e288b0bc54a19aa1d3574b6085eaa6`  
		Last Modified: Wed, 14 Jun 2023 18:19:49 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.20` - linux; s390x

```console
$ docker pull memcached@sha256:882f9d1d57c58c374c6074cbce0784748bdce465757ad946f699a47a924f4518
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31228777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:098ff94df44cb535cdd4f10e4106756fc1766a232277b3a9c2f51ff567ee3082`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 13 Jun 2023 04:30:13 GMT
ADD file:558e8c34e969d458ce6bf4207d9c0fe05d2e67d3457c1d5689666749e82ef2ab in / 
# Tue, 13 Jun 2023 04:30:14 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 18:41:51 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 13 Jun 2023 18:41:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 18:41:54 GMT
ENV MEMCACHED_VERSION=1.6.20
# Tue, 13 Jun 2023 18:41:54 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Tue, 13 Jun 2023 18:44:58 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 13 Jun 2023 18:44:58 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 13 Jun 2023 18:44:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 13 Jun 2023 18:44:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jun 2023 18:44:59 GMT
USER memcache
# Tue, 13 Jun 2023 18:44:59 GMT
EXPOSE 11211
# Tue, 13 Jun 2023 18:44:59 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6a752e2308c741009b6f5a88a8ea6764b96ebe7f544197912d8ef9a3ec8c8763`  
		Last Modified: Tue, 13 Jun 2023 04:34:49 GMT  
		Size: 29.7 MB (29652514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:465e13673c57447925389cdcf074d61ff5114faa447fd3b775481a229ac38019`  
		Last Modified: Tue, 13 Jun 2023 18:45:27 GMT  
		Size: 5.0 KB (5023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a81fcab4fd1cd8ac9cc18539fde149b89e423f0b5c80f2f07460f49209907ca`  
		Last Modified: Tue, 13 Jun 2023 18:45:27 GMT  
		Size: 324.3 KB (324337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a035c15be3c1e4f3cd28a1c060f56d03f4fa02c5e86290288ac74b2533feca`  
		Last Modified: Tue, 13 Jun 2023 18:45:27 GMT  
		Size: 1.2 MB (1246496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdda04e27e25f6bf6f5489a28d36c1903052488bf96ee74f76b993a5926207b7`  
		Last Modified: Tue, 13 Jun 2023 18:45:27 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d62044b354beed912ecf01ba2d6b0efc230907a720539c8850809e2b76f9ac89`  
		Last Modified: Tue, 13 Jun 2023 18:45:27 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:1.6.20-alpine`

```console
$ docker pull memcached@sha256:f9aad561ac4e31d347b252c0fef6beede071bdaa205e38dc9dc5369201d8ff47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `memcached:1.6.20-alpine` - linux; amd64

```console
$ docker pull memcached@sha256:a7a04bc20ec122d9f024dff57494853d5dc9705fb97af9170cc31a1f531dcaa5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4462373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15429daa972e1d57884e75ecc7f784564ae7cf089c25671dd118a0025f806b6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 20:50:58 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Wed, 14 Jun 2023 20:50:59 GMT
RUN apk add --no-cache libsasl
# Wed, 14 Jun 2023 20:50:59 GMT
ENV MEMCACHED_VERSION=1.6.20
# Wed, 14 Jun 2023 20:50:59 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Wed, 14 Jun 2023 20:53:09 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Wed, 14 Jun 2023 20:53:09 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 14 Jun 2023 20:53:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Jun 2023 20:53:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 20:53:09 GMT
USER memcache
# Wed, 14 Jun 2023 20:53:09 GMT
EXPOSE 11211
# Wed, 14 Jun 2023 20:53:09 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b2b2df106c5026cd33ea4ac655b77f25410ec9f4b8a6756ebc1ceeb79fca3c7`  
		Last Modified: Wed, 14 Jun 2023 20:53:58 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed63668528d3e2159f55909c66dc48a6f746ce24c2e2f6d963b992aefaa457ce`  
		Last Modified: Wed, 14 Jun 2023 20:53:58 GMT  
		Size: 108.1 KB (108080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc06ea6ffc2a4279c91e26e37b450afb1e0f1007815b19a7146d52b016dddc61`  
		Last Modified: Wed, 14 Jun 2023 20:53:59 GMT  
		Size: 954.7 KB (954748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:098e9e56712cb64736718f40b476d8eeb9410130c28ce94fe1bc2d380d9083cf`  
		Last Modified: Wed, 14 Jun 2023 20:53:59 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5c14818f6fb630a615284b18f945c89c0563530c25f07af955d0f85504020e9`  
		Last Modified: Wed, 14 Jun 2023 20:53:58 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.20-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:e59934ff7bef6e6053b618f65923d2c1fa7235a008fb20f4fe9db13f8d6dc167
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4399194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dab6918acf63bcf26d1a95d40666c44f281aa14f0d4e27884d4c2f4b227dd9b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 20:57:26 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Wed, 14 Jun 2023 20:57:27 GMT
RUN apk add --no-cache libsasl
# Wed, 14 Jun 2023 20:57:27 GMT
ENV MEMCACHED_VERSION=1.6.20
# Wed, 14 Jun 2023 20:57:27 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Wed, 14 Jun 2023 20:59:54 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Wed, 14 Jun 2023 20:59:54 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 14 Jun 2023 20:59:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Jun 2023 20:59:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 20:59:55 GMT
USER memcache
# Wed, 14 Jun 2023 20:59:55 GMT
EXPOSE 11211
# Wed, 14 Jun 2023 20:59:55 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:666588188768f19b27fb821e02d084406af8fd867cc4595b896b9eed50b2105e`  
		Last Modified: Wed, 14 Jun 2023 21:00:51 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d958a137d671266f063c0af4d7b0b6d44d9018b77fdbddb8fd412d3c0b1be3`  
		Last Modified: Wed, 14 Jun 2023 21:00:51 GMT  
		Size: 124.1 KB (124137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eddee3cdc367d6f8265fe941f97020460db6cb5555711640b2ad62bd5c2a613c`  
		Last Modified: Wed, 14 Jun 2023 21:00:51 GMT  
		Size: 944.1 KB (944138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfec1ffcd9427d8fb06b908c1d3e0715a9db99c94c46f7896890a98b95c5f049`  
		Last Modified: Wed, 14 Jun 2023 21:00:51 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aea835bd4a5d779b88da37bc977813dd1ed9d228f5e78e3459edde4fa6f155e2`  
		Last Modified: Wed, 14 Jun 2023 21:00:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.20-alpine` - linux; 386

```console
$ docker pull memcached@sha256:126e7a3993f53145ad966b11e0c8e7cb9f92520ea9899abfaa550aaee49c9f5c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4313116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:835ad308527d3b6bc85d49a990ae4c544363b3e3b3cef7a7a49ea6081d81a121`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 May 2023 23:11:03 GMT
ADD file:cfe47ebe49c4a75094234cafa52aa13aa26abcdad49b89293585884b3a8faeae in / 
# Tue, 09 May 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Thu, 11 May 2023 19:56:01 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Thu, 11 May 2023 19:56:03 GMT
RUN apk add --no-cache libsasl
# Mon, 15 May 2023 21:42:18 GMT
ENV MEMCACHED_VERSION=1.6.20
# Mon, 15 May 2023 21:42:18 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Mon, 15 May 2023 21:45:44 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Mon, 15 May 2023 21:45:44 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Mon, 15 May 2023 21:45:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 15 May 2023 21:45:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 15 May 2023 21:45:45 GMT
USER memcache
# Mon, 15 May 2023 21:45:45 GMT
EXPOSE 11211
# Mon, 15 May 2023 21:45:45 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:613767c5530f4016482e81288d0efdca4e58c62031252130d8fccd6f6260a068`  
		Last Modified: Tue, 09 May 2023 23:11:20 GMT  
		Size: 3.3 MB (3264862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72c25994ef1ec30cf62d081517b625d1ea87b0836bb6a90cd7ab8b1ab0501bb6`  
		Last Modified: Thu, 11 May 2023 20:00:35 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c42385514308725216c1a4eadb9aa4270c08f3140c342b6db43060f55af1ed`  
		Last Modified: Thu, 11 May 2023 20:00:35 GMT  
		Size: 109.5 KB (109521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3acbe617b4c6e3f32de32c1e69b84aa2c4e9c31d5e84a648a8340acda2452e03`  
		Last Modified: Mon, 15 May 2023 21:46:28 GMT  
		Size: 937.1 KB (937060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a81b72d4c28496fdd77fd3bf62a9800bd545660f44738482a100b00f99b3649c`  
		Last Modified: Mon, 15 May 2023 21:46:27 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c224abc2162f00f8769eeacb44838cbed654dd60d38e8d08d585003cb6495a`  
		Last Modified: Mon, 15 May 2023 21:46:27 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.20-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:912319e8c2e48db747d88d979ed43b691d125b7c05619189b4dcbe86f19b9a8b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4494043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c26bf354613881c6a96c357992e4176080f21ed4cac05a673e9a34056bd7d8be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 May 2023 23:11:09 GMT
ADD file:0a227602737a24c596923d3fd0a7c8b7d9000dbc6b80561473def09abbebbfa6 in / 
# Tue, 09 May 2023 23:11:10 GMT
CMD ["/bin/sh"]
# Thu, 11 May 2023 20:28:43 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Thu, 11 May 2023 20:28:45 GMT
RUN apk add --no-cache libsasl
# Mon, 15 May 2023 21:20:18 GMT
ENV MEMCACHED_VERSION=1.6.20
# Mon, 15 May 2023 21:20:18 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Mon, 15 May 2023 21:23:19 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Mon, 15 May 2023 21:23:19 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Mon, 15 May 2023 21:23:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 15 May 2023 21:23:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 15 May 2023 21:23:20 GMT
USER memcache
# Mon, 15 May 2023 21:23:20 GMT
EXPOSE 11211
# Mon, 15 May 2023 21:23:21 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5c0986f188e93dd7e76a4dc49a9170da2cd124709f5e1590b378e31a2b0d9587`  
		Last Modified: Tue, 09 May 2023 23:11:31 GMT  
		Size: 3.4 MB (3385631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2637efcb2bfb898454103e5536179d5f732cbddcd32f89c4ed51466ed8c6a14`  
		Last Modified: Thu, 11 May 2023 20:32:50 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45b064e3e507b9c35d5b605a606755605f7807236709d725567d0609ac53ee29`  
		Last Modified: Thu, 11 May 2023 20:32:50 GMT  
		Size: 123.9 KB (123933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a5d4f2fcda4a8d8a11f4f09bab2989aa2ec605ec585ed61bb4b519b62f5a47`  
		Last Modified: Mon, 15 May 2023 21:24:04 GMT  
		Size: 982.8 KB (982805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81d636c8d2e3e1cce3ec344ad3d21645a62a2c2286037cc287cd4e56c21d3fe7`  
		Last Modified: Mon, 15 May 2023 21:24:03 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca8ad226ad66d4c655b3b77ce26667f5b878d47000bfc558dae9c53ec6cff9b5`  
		Last Modified: Mon, 15 May 2023 21:24:03 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.20-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:029a3ea9286bc7541646e7ca99fb57db8faffea15abf7bee651ee5cac65c4732
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4290940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac9f545f21c06b546f33df533b248b59335e5960e61844e6729780e8c404af6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 May 2023 23:11:06 GMT
ADD file:89d6e366e8ab41011a5866f8ca43aac6cfef00edffebad565918ab632a6d6210 in / 
# Tue, 09 May 2023 23:11:07 GMT
CMD ["/bin/sh"]
# Thu, 11 May 2023 19:55:27 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Thu, 11 May 2023 19:55:28 GMT
RUN apk add --no-cache libsasl
# Mon, 15 May 2023 21:51:02 GMT
ENV MEMCACHED_VERSION=1.6.20
# Mon, 15 May 2023 21:51:02 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Mon, 15 May 2023 21:54:04 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Mon, 15 May 2023 21:54:04 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Mon, 15 May 2023 21:54:04 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 15 May 2023 21:54:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 15 May 2023 21:54:04 GMT
USER memcache
# Mon, 15 May 2023 21:54:05 GMT
EXPOSE 11211
# Mon, 15 May 2023 21:54:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:25da54cc0a08f4ca602c6bcd3e52d70082eb8a25ee022bc9f1dda019de49197a`  
		Last Modified: Tue, 09 May 2023 23:11:35 GMT  
		Size: 3.2 MB (3226303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b276b6acd2b3a86c684a2f6a3641c76b4e2e5b3ce67562b64266899a052e6d4d`  
		Last Modified: Thu, 11 May 2023 19:59:45 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:483fe7c616264b630bec3883deae3b95c3220c0d46c5440048f5f2372224979c`  
		Last Modified: Thu, 11 May 2023 19:59:45 GMT  
		Size: 112.8 KB (112850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19827c7b432b650815a5843027a98d18e43bbd207cdda86bc95dc2f55c69b498`  
		Last Modified: Mon, 15 May 2023 21:54:45 GMT  
		Size: 950.1 KB (950116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da2238a07815946f6ba0dcbb105f0a4dab9db865ab4696d5c561fdd473328147`  
		Last Modified: Mon, 15 May 2023 21:54:46 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03dc27afabfb97c92d4893b707ee04b92ec5dd5e64ce581e0c27d7b344d7e735`  
		Last Modified: Mon, 15 May 2023 21:54:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:1.6.20-alpine3.18`

```console
$ docker pull memcached@sha256:f9aad561ac4e31d347b252c0fef6beede071bdaa205e38dc9dc5369201d8ff47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `memcached:1.6.20-alpine3.18` - linux; amd64

```console
$ docker pull memcached@sha256:a7a04bc20ec122d9f024dff57494853d5dc9705fb97af9170cc31a1f531dcaa5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4462373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15429daa972e1d57884e75ecc7f784564ae7cf089c25671dd118a0025f806b6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 20:50:58 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Wed, 14 Jun 2023 20:50:59 GMT
RUN apk add --no-cache libsasl
# Wed, 14 Jun 2023 20:50:59 GMT
ENV MEMCACHED_VERSION=1.6.20
# Wed, 14 Jun 2023 20:50:59 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Wed, 14 Jun 2023 20:53:09 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Wed, 14 Jun 2023 20:53:09 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 14 Jun 2023 20:53:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Jun 2023 20:53:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 20:53:09 GMT
USER memcache
# Wed, 14 Jun 2023 20:53:09 GMT
EXPOSE 11211
# Wed, 14 Jun 2023 20:53:09 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b2b2df106c5026cd33ea4ac655b77f25410ec9f4b8a6756ebc1ceeb79fca3c7`  
		Last Modified: Wed, 14 Jun 2023 20:53:58 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed63668528d3e2159f55909c66dc48a6f746ce24c2e2f6d963b992aefaa457ce`  
		Last Modified: Wed, 14 Jun 2023 20:53:58 GMT  
		Size: 108.1 KB (108080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc06ea6ffc2a4279c91e26e37b450afb1e0f1007815b19a7146d52b016dddc61`  
		Last Modified: Wed, 14 Jun 2023 20:53:59 GMT  
		Size: 954.7 KB (954748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:098e9e56712cb64736718f40b476d8eeb9410130c28ce94fe1bc2d380d9083cf`  
		Last Modified: Wed, 14 Jun 2023 20:53:59 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5c14818f6fb630a615284b18f945c89c0563530c25f07af955d0f85504020e9`  
		Last Modified: Wed, 14 Jun 2023 20:53:58 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.20-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:e59934ff7bef6e6053b618f65923d2c1fa7235a008fb20f4fe9db13f8d6dc167
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4399194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dab6918acf63bcf26d1a95d40666c44f281aa14f0d4e27884d4c2f4b227dd9b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 20:57:26 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Wed, 14 Jun 2023 20:57:27 GMT
RUN apk add --no-cache libsasl
# Wed, 14 Jun 2023 20:57:27 GMT
ENV MEMCACHED_VERSION=1.6.20
# Wed, 14 Jun 2023 20:57:27 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Wed, 14 Jun 2023 20:59:54 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Wed, 14 Jun 2023 20:59:54 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 14 Jun 2023 20:59:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Jun 2023 20:59:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 20:59:55 GMT
USER memcache
# Wed, 14 Jun 2023 20:59:55 GMT
EXPOSE 11211
# Wed, 14 Jun 2023 20:59:55 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:666588188768f19b27fb821e02d084406af8fd867cc4595b896b9eed50b2105e`  
		Last Modified: Wed, 14 Jun 2023 21:00:51 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d958a137d671266f063c0af4d7b0b6d44d9018b77fdbddb8fd412d3c0b1be3`  
		Last Modified: Wed, 14 Jun 2023 21:00:51 GMT  
		Size: 124.1 KB (124137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eddee3cdc367d6f8265fe941f97020460db6cb5555711640b2ad62bd5c2a613c`  
		Last Modified: Wed, 14 Jun 2023 21:00:51 GMT  
		Size: 944.1 KB (944138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfec1ffcd9427d8fb06b908c1d3e0715a9db99c94c46f7896890a98b95c5f049`  
		Last Modified: Wed, 14 Jun 2023 21:00:51 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aea835bd4a5d779b88da37bc977813dd1ed9d228f5e78e3459edde4fa6f155e2`  
		Last Modified: Wed, 14 Jun 2023 21:00:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.20-alpine3.18` - linux; 386

```console
$ docker pull memcached@sha256:126e7a3993f53145ad966b11e0c8e7cb9f92520ea9899abfaa550aaee49c9f5c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4313116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:835ad308527d3b6bc85d49a990ae4c544363b3e3b3cef7a7a49ea6081d81a121`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 May 2023 23:11:03 GMT
ADD file:cfe47ebe49c4a75094234cafa52aa13aa26abcdad49b89293585884b3a8faeae in / 
# Tue, 09 May 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Thu, 11 May 2023 19:56:01 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Thu, 11 May 2023 19:56:03 GMT
RUN apk add --no-cache libsasl
# Mon, 15 May 2023 21:42:18 GMT
ENV MEMCACHED_VERSION=1.6.20
# Mon, 15 May 2023 21:42:18 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Mon, 15 May 2023 21:45:44 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Mon, 15 May 2023 21:45:44 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Mon, 15 May 2023 21:45:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 15 May 2023 21:45:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 15 May 2023 21:45:45 GMT
USER memcache
# Mon, 15 May 2023 21:45:45 GMT
EXPOSE 11211
# Mon, 15 May 2023 21:45:45 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:613767c5530f4016482e81288d0efdca4e58c62031252130d8fccd6f6260a068`  
		Last Modified: Tue, 09 May 2023 23:11:20 GMT  
		Size: 3.3 MB (3264862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72c25994ef1ec30cf62d081517b625d1ea87b0836bb6a90cd7ab8b1ab0501bb6`  
		Last Modified: Thu, 11 May 2023 20:00:35 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c42385514308725216c1a4eadb9aa4270c08f3140c342b6db43060f55af1ed`  
		Last Modified: Thu, 11 May 2023 20:00:35 GMT  
		Size: 109.5 KB (109521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3acbe617b4c6e3f32de32c1e69b84aa2c4e9c31d5e84a648a8340acda2452e03`  
		Last Modified: Mon, 15 May 2023 21:46:28 GMT  
		Size: 937.1 KB (937060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a81b72d4c28496fdd77fd3bf62a9800bd545660f44738482a100b00f99b3649c`  
		Last Modified: Mon, 15 May 2023 21:46:27 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c224abc2162f00f8769eeacb44838cbed654dd60d38e8d08d585003cb6495a`  
		Last Modified: Mon, 15 May 2023 21:46:27 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.20-alpine3.18` - linux; ppc64le

```console
$ docker pull memcached@sha256:912319e8c2e48db747d88d979ed43b691d125b7c05619189b4dcbe86f19b9a8b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4494043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c26bf354613881c6a96c357992e4176080f21ed4cac05a673e9a34056bd7d8be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 May 2023 23:11:09 GMT
ADD file:0a227602737a24c596923d3fd0a7c8b7d9000dbc6b80561473def09abbebbfa6 in / 
# Tue, 09 May 2023 23:11:10 GMT
CMD ["/bin/sh"]
# Thu, 11 May 2023 20:28:43 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Thu, 11 May 2023 20:28:45 GMT
RUN apk add --no-cache libsasl
# Mon, 15 May 2023 21:20:18 GMT
ENV MEMCACHED_VERSION=1.6.20
# Mon, 15 May 2023 21:20:18 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Mon, 15 May 2023 21:23:19 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Mon, 15 May 2023 21:23:19 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Mon, 15 May 2023 21:23:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 15 May 2023 21:23:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 15 May 2023 21:23:20 GMT
USER memcache
# Mon, 15 May 2023 21:23:20 GMT
EXPOSE 11211
# Mon, 15 May 2023 21:23:21 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5c0986f188e93dd7e76a4dc49a9170da2cd124709f5e1590b378e31a2b0d9587`  
		Last Modified: Tue, 09 May 2023 23:11:31 GMT  
		Size: 3.4 MB (3385631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2637efcb2bfb898454103e5536179d5f732cbddcd32f89c4ed51466ed8c6a14`  
		Last Modified: Thu, 11 May 2023 20:32:50 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45b064e3e507b9c35d5b605a606755605f7807236709d725567d0609ac53ee29`  
		Last Modified: Thu, 11 May 2023 20:32:50 GMT  
		Size: 123.9 KB (123933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a5d4f2fcda4a8d8a11f4f09bab2989aa2ec605ec585ed61bb4b519b62f5a47`  
		Last Modified: Mon, 15 May 2023 21:24:04 GMT  
		Size: 982.8 KB (982805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81d636c8d2e3e1cce3ec344ad3d21645a62a2c2286037cc287cd4e56c21d3fe7`  
		Last Modified: Mon, 15 May 2023 21:24:03 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca8ad226ad66d4c655b3b77ce26667f5b878d47000bfc558dae9c53ec6cff9b5`  
		Last Modified: Mon, 15 May 2023 21:24:03 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.20-alpine3.18` - linux; s390x

```console
$ docker pull memcached@sha256:029a3ea9286bc7541646e7ca99fb57db8faffea15abf7bee651ee5cac65c4732
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4290940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac9f545f21c06b546f33df533b248b59335e5960e61844e6729780e8c404af6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 May 2023 23:11:06 GMT
ADD file:89d6e366e8ab41011a5866f8ca43aac6cfef00edffebad565918ab632a6d6210 in / 
# Tue, 09 May 2023 23:11:07 GMT
CMD ["/bin/sh"]
# Thu, 11 May 2023 19:55:27 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Thu, 11 May 2023 19:55:28 GMT
RUN apk add --no-cache libsasl
# Mon, 15 May 2023 21:51:02 GMT
ENV MEMCACHED_VERSION=1.6.20
# Mon, 15 May 2023 21:51:02 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Mon, 15 May 2023 21:54:04 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Mon, 15 May 2023 21:54:04 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Mon, 15 May 2023 21:54:04 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 15 May 2023 21:54:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 15 May 2023 21:54:04 GMT
USER memcache
# Mon, 15 May 2023 21:54:05 GMT
EXPOSE 11211
# Mon, 15 May 2023 21:54:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:25da54cc0a08f4ca602c6bcd3e52d70082eb8a25ee022bc9f1dda019de49197a`  
		Last Modified: Tue, 09 May 2023 23:11:35 GMT  
		Size: 3.2 MB (3226303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b276b6acd2b3a86c684a2f6a3641c76b4e2e5b3ce67562b64266899a052e6d4d`  
		Last Modified: Thu, 11 May 2023 19:59:45 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:483fe7c616264b630bec3883deae3b95c3220c0d46c5440048f5f2372224979c`  
		Last Modified: Thu, 11 May 2023 19:59:45 GMT  
		Size: 112.8 KB (112850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19827c7b432b650815a5843027a98d18e43bbd207cdda86bc95dc2f55c69b498`  
		Last Modified: Mon, 15 May 2023 21:54:45 GMT  
		Size: 950.1 KB (950116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da2238a07815946f6ba0dcbb105f0a4dab9db865ab4696d5c561fdd473328147`  
		Last Modified: Mon, 15 May 2023 21:54:46 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03dc27afabfb97c92d4893b707ee04b92ec5dd5e64ce581e0c27d7b344d7e735`  
		Last Modified: Mon, 15 May 2023 21:54:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:1.6.20-bookworm`

```console
$ docker pull memcached@sha256:0495a71949e29a0dd91782be635586b244a336a765e79c78cfea895cd541e312
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; mips64le
	-	linux; ppc64le

### `memcached:1.6.20-bookworm` - linux; amd64

```console
$ docker pull memcached@sha256:533c607824b2f5781b179e175fcdf055577a3f076fb0a0fdcd13487c7c92125f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (38973406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbcfa8d0003c80b0bba4004f4b15b4a5600b9dd481ac2d887bc31e794f067464`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jun 2023 23:20:42 GMT
ADD file:ba1250b6ecd5dd09d4914189d72741c2817988994e7da514bf62be439a34bdb5 in / 
# Mon, 12 Jun 2023 23:20:42 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 20:48:19 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 14 Jun 2023 20:48:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jun 2023 20:48:24 GMT
ENV MEMCACHED_VERSION=1.6.20
# Wed, 14 Jun 2023 20:48:24 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Wed, 14 Jun 2023 20:50:40 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 14 Jun 2023 20:50:40 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 14 Jun 2023 20:50:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Jun 2023 20:50:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 20:50:41 GMT
USER memcache
# Wed, 14 Jun 2023 20:50:41 GMT
EXPOSE 11211
# Wed, 14 Jun 2023 20:50:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5b5fe70539cd6989aa19f25826309f9715a9489cf1c057982d6a84c1ad8975c7`  
		Last Modified: Mon, 12 Jun 2023 23:25:49 GMT  
		Size: 29.1 MB (29124744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab209434009a85e82d99c0547bb947940f9e1002ce6e965417396ee22a6820db`  
		Last Modified: Wed, 14 Jun 2023 20:53:33 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f4dfc49c9cdae8d4df855de7cc0460e5db8c762e73786d4f8fa4f69ba11d6d`  
		Last Modified: Wed, 14 Jun 2023 20:53:33 GMT  
		Size: 2.7 MB (2677239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96a3de0d22592d9a254814d5b77e3a84e73d2f055d162503fe811f731a320701`  
		Last Modified: Wed, 14 Jun 2023 20:53:34 GMT  
		Size: 7.2 MB (7169888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a38b201fb7fc8d917459453ee1c0218cf9845c96b885a02b02999f81b21c6bb`  
		Last Modified: Wed, 14 Jun 2023 20:53:33 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6f5720dc1980c886ee7e8d6067ed87e102bb31824e557a85fbd54273542debf`  
		Last Modified: Wed, 14 Jun 2023 20:53:33 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.20-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:3464bfccdfad0dc788e056949d59fc0b665ec165654b3a8502a2f4a3868a3dc7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 MB (37872888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20f33353745665e05e1722aa9af40e06b3f58778f8e758e786eaad30054de61f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jun 2023 23:40:13 GMT
ADD file:f75c3fe22fec548b35a86a9a5802fdc97497f5d253cf630d65f13282169d3f3f in / 
# Mon, 12 Jun 2023 23:40:14 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 20:54:33 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 14 Jun 2023 20:54:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jun 2023 20:54:37 GMT
ENV MEMCACHED_VERSION=1.6.20
# Wed, 14 Jun 2023 20:54:37 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Wed, 14 Jun 2023 20:57:13 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 14 Jun 2023 20:57:13 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 14 Jun 2023 20:57:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Jun 2023 20:57:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 20:57:14 GMT
USER memcache
# Wed, 14 Jun 2023 20:57:14 GMT
EXPOSE 11211
# Wed, 14 Jun 2023 20:57:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:95039a22a7cc3ae41d71f075e6e09e91e8da850fb5f80aba2f4a09f254520539`  
		Last Modified: Mon, 12 Jun 2023 23:44:08 GMT  
		Size: 29.2 MB (29152534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6da70104cc8ee465752315034f04011354e6149243e2bc69b9da49e6855df4b8`  
		Last Modified: Wed, 14 Jun 2023 21:00:29 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a7b40152f53e05b8cbcfe09be5b1598fcc05cf4f9ffad3b296eca43305450da`  
		Last Modified: Wed, 14 Jun 2023 21:00:30 GMT  
		Size: 2.5 MB (2539179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bf09d04f9c61af195486f42915b137b8612584f982737f5e465d02648a6dc8a`  
		Last Modified: Wed, 14 Jun 2023 21:00:30 GMT  
		Size: 6.2 MB (6179640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e71555e51295eeceeab1a9ab6bebb21108fbbe59e01349857c51932deea0f64`  
		Last Modified: Wed, 14 Jun 2023 21:00:29 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15cd3195dbfc5cedaf71b7c156002599dfb94219b51f85c966a1bee80bc37e65`  
		Last Modified: Wed, 14 Jun 2023 21:00:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.20-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:d2855c4deb19365dd1c83b81c9e1fa36f7873cc8b3dd02f8f01de10200bf208e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37554221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7068fffc8ee0a4607e1586297977a273786efb52e1782f11396ee5f7a5150c0f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 13 Jun 2023 00:09:02 GMT
ADD file:f91bd2a174259cb69646fc34ba2fc6b8941ad8e171d2d7952a4d8ac3d95e2ad7 in / 
# Tue, 13 Jun 2023 00:09:06 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 18:38:15 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 14 Jun 2023 18:38:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jun 2023 18:38:39 GMT
ENV MEMCACHED_VERSION=1.6.20
# Wed, 14 Jun 2023 18:38:41 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Wed, 14 Jun 2023 18:45:20 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 14 Jun 2023 18:45:23 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 14 Jun 2023 18:45:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Jun 2023 18:45:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 18:45:32 GMT
USER memcache
# Wed, 14 Jun 2023 18:45:35 GMT
EXPOSE 11211
# Wed, 14 Jun 2023 18:45:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3fc28260a4d871ef9781cad2bb064ad7212a5063de3a1d35dba938ce82115e5b`  
		Last Modified: Tue, 13 Jun 2023 00:22:29 GMT  
		Size: 29.1 MB (29118129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c804aeb794275ae845d32d2939d0e0fefa75cd112f1075aaf2104097050ae8`  
		Last Modified: Wed, 14 Jun 2023 18:46:04 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf29fcbe26928e2f4086a889098220505bdd4401dc87958f623ade0618efcd28`  
		Last Modified: Wed, 14 Jun 2023 18:46:05 GMT  
		Size: 1.9 MB (1934899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76d4e9cc234d41e69eba3bf411cb1d3ebe17e2fefbffb0c3458d613f2545337e`  
		Last Modified: Wed, 14 Jun 2023 18:46:09 GMT  
		Size: 6.5 MB (6499709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0988c34e4840378b9876eba362b50458e769389d0cc626698bef65e46c721458`  
		Last Modified: Wed, 14 Jun 2023 18:46:04 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db55745458426cdf0d23fd0589fd440e2d328e4d5ffb00a9ef6d2e0225cec8bf`  
		Last Modified: Wed, 14 Jun 2023 18:46:04 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6.20-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:0e023c41d9c6a8d04edad22ecea59cfcf424d0dc3895c442a9e7a4575961d53d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43193448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a85a60b74a9575a203aba1a5f800dfe479b80cde8ff577ccd5e7e77bdaab64c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jun 2023 23:17:34 GMT
ADD file:3f8b9849acb625537f99921ef80190de7b03afdc287a5d1113a92cc41ae24be2 in / 
# Mon, 12 Jun 2023 23:17:36 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 18:15:42 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 14 Jun 2023 18:15:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jun 2023 18:15:50 GMT
ENV MEMCACHED_VERSION=1.6.20
# Wed, 14 Jun 2023 18:15:51 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Wed, 14 Jun 2023 18:19:27 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 14 Jun 2023 18:19:28 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 14 Jun 2023 18:19:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Jun 2023 18:19:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 18:19:31 GMT
USER memcache
# Wed, 14 Jun 2023 18:19:32 GMT
EXPOSE 11211
# Wed, 14 Jun 2023 18:19:32 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9f041b53cef30007c43057f2520876c85ed6bee6be5aaee867dfb31a053d6cca`  
		Last Modified: Mon, 12 Jun 2023 23:24:09 GMT  
		Size: 33.1 MB (33116725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a2d84b1fee81412bbd9bb301c77e6dfacfac70c2f1485de806658b49b06e08`  
		Last Modified: Wed, 14 Jun 2023 18:19:49 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca8bb5af043b48c9fe0e110ee13c139ceb715570346140fc86092d582d38b52b`  
		Last Modified: Wed, 14 Jun 2023 18:19:50 GMT  
		Size: 2.9 MB (2891306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e2d7805a151ec1618da95ad34cb2fdc6ae889b9f7908aaca6d063ca864f3e24`  
		Last Modified: Wed, 14 Jun 2023 18:19:52 GMT  
		Size: 7.2 MB (7183881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc5db4b315753422be0d08638f594b1ec64484c44f68942473f903387853b3bd`  
		Last Modified: Wed, 14 Jun 2023 18:19:49 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a8a9b2ed7c41d27d92f9db3c21beec2a2e288b0bc54a19aa1d3574b6085eaa6`  
		Last Modified: Wed, 14 Jun 2023 18:19:49 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:alpine`

```console
$ docker pull memcached@sha256:dd03af6acd2f6e2fad2a24cb0db1c987074c6f968c2995c6d9920015efb243a7
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
$ docker pull memcached@sha256:a7a04bc20ec122d9f024dff57494853d5dc9705fb97af9170cc31a1f531dcaa5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4462373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15429daa972e1d57884e75ecc7f784564ae7cf089c25671dd118a0025f806b6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 20:50:58 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Wed, 14 Jun 2023 20:50:59 GMT
RUN apk add --no-cache libsasl
# Wed, 14 Jun 2023 20:50:59 GMT
ENV MEMCACHED_VERSION=1.6.20
# Wed, 14 Jun 2023 20:50:59 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Wed, 14 Jun 2023 20:53:09 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Wed, 14 Jun 2023 20:53:09 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 14 Jun 2023 20:53:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Jun 2023 20:53:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 20:53:09 GMT
USER memcache
# Wed, 14 Jun 2023 20:53:09 GMT
EXPOSE 11211
# Wed, 14 Jun 2023 20:53:09 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b2b2df106c5026cd33ea4ac655b77f25410ec9f4b8a6756ebc1ceeb79fca3c7`  
		Last Modified: Wed, 14 Jun 2023 20:53:58 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed63668528d3e2159f55909c66dc48a6f746ce24c2e2f6d963b992aefaa457ce`  
		Last Modified: Wed, 14 Jun 2023 20:53:58 GMT  
		Size: 108.1 KB (108080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc06ea6ffc2a4279c91e26e37b450afb1e0f1007815b19a7146d52b016dddc61`  
		Last Modified: Wed, 14 Jun 2023 20:53:59 GMT  
		Size: 954.7 KB (954748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:098e9e56712cb64736718f40b476d8eeb9410130c28ce94fe1bc2d380d9083cf`  
		Last Modified: Wed, 14 Jun 2023 20:53:59 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5c14818f6fb630a615284b18f945c89c0563530c25f07af955d0f85504020e9`  
		Last Modified: Wed, 14 Jun 2023 20:53:58 GMT  
		Size: 118.0 B  
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
$ docker pull memcached@sha256:e59934ff7bef6e6053b618f65923d2c1fa7235a008fb20f4fe9db13f8d6dc167
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4399194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dab6918acf63bcf26d1a95d40666c44f281aa14f0d4e27884d4c2f4b227dd9b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 20:57:26 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Wed, 14 Jun 2023 20:57:27 GMT
RUN apk add --no-cache libsasl
# Wed, 14 Jun 2023 20:57:27 GMT
ENV MEMCACHED_VERSION=1.6.20
# Wed, 14 Jun 2023 20:57:27 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Wed, 14 Jun 2023 20:59:54 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Wed, 14 Jun 2023 20:59:54 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 14 Jun 2023 20:59:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Jun 2023 20:59:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 20:59:55 GMT
USER memcache
# Wed, 14 Jun 2023 20:59:55 GMT
EXPOSE 11211
# Wed, 14 Jun 2023 20:59:55 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:666588188768f19b27fb821e02d084406af8fd867cc4595b896b9eed50b2105e`  
		Last Modified: Wed, 14 Jun 2023 21:00:51 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d958a137d671266f063c0af4d7b0b6d44d9018b77fdbddb8fd412d3c0b1be3`  
		Last Modified: Wed, 14 Jun 2023 21:00:51 GMT  
		Size: 124.1 KB (124137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eddee3cdc367d6f8265fe941f97020460db6cb5555711640b2ad62bd5c2a613c`  
		Last Modified: Wed, 14 Jun 2023 21:00:51 GMT  
		Size: 944.1 KB (944138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfec1ffcd9427d8fb06b908c1d3e0715a9db99c94c46f7896890a98b95c5f049`  
		Last Modified: Wed, 14 Jun 2023 21:00:51 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aea835bd4a5d779b88da37bc977813dd1ed9d228f5e78e3459edde4fa6f155e2`  
		Last Modified: Wed, 14 Jun 2023 21:00:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:alpine` - linux; 386

```console
$ docker pull memcached@sha256:126e7a3993f53145ad966b11e0c8e7cb9f92520ea9899abfaa550aaee49c9f5c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4313116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:835ad308527d3b6bc85d49a990ae4c544363b3e3b3cef7a7a49ea6081d81a121`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 May 2023 23:11:03 GMT
ADD file:cfe47ebe49c4a75094234cafa52aa13aa26abcdad49b89293585884b3a8faeae in / 
# Tue, 09 May 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Thu, 11 May 2023 19:56:01 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Thu, 11 May 2023 19:56:03 GMT
RUN apk add --no-cache libsasl
# Mon, 15 May 2023 21:42:18 GMT
ENV MEMCACHED_VERSION=1.6.20
# Mon, 15 May 2023 21:42:18 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Mon, 15 May 2023 21:45:44 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Mon, 15 May 2023 21:45:44 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Mon, 15 May 2023 21:45:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 15 May 2023 21:45:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 15 May 2023 21:45:45 GMT
USER memcache
# Mon, 15 May 2023 21:45:45 GMT
EXPOSE 11211
# Mon, 15 May 2023 21:45:45 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:613767c5530f4016482e81288d0efdca4e58c62031252130d8fccd6f6260a068`  
		Last Modified: Tue, 09 May 2023 23:11:20 GMT  
		Size: 3.3 MB (3264862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72c25994ef1ec30cf62d081517b625d1ea87b0836bb6a90cd7ab8b1ab0501bb6`  
		Last Modified: Thu, 11 May 2023 20:00:35 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c42385514308725216c1a4eadb9aa4270c08f3140c342b6db43060f55af1ed`  
		Last Modified: Thu, 11 May 2023 20:00:35 GMT  
		Size: 109.5 KB (109521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3acbe617b4c6e3f32de32c1e69b84aa2c4e9c31d5e84a648a8340acda2452e03`  
		Last Modified: Mon, 15 May 2023 21:46:28 GMT  
		Size: 937.1 KB (937060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a81b72d4c28496fdd77fd3bf62a9800bd545660f44738482a100b00f99b3649c`  
		Last Modified: Mon, 15 May 2023 21:46:27 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c224abc2162f00f8769eeacb44838cbed654dd60d38e8d08d585003cb6495a`  
		Last Modified: Mon, 15 May 2023 21:46:27 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:912319e8c2e48db747d88d979ed43b691d125b7c05619189b4dcbe86f19b9a8b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4494043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c26bf354613881c6a96c357992e4176080f21ed4cac05a673e9a34056bd7d8be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 May 2023 23:11:09 GMT
ADD file:0a227602737a24c596923d3fd0a7c8b7d9000dbc6b80561473def09abbebbfa6 in / 
# Tue, 09 May 2023 23:11:10 GMT
CMD ["/bin/sh"]
# Thu, 11 May 2023 20:28:43 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Thu, 11 May 2023 20:28:45 GMT
RUN apk add --no-cache libsasl
# Mon, 15 May 2023 21:20:18 GMT
ENV MEMCACHED_VERSION=1.6.20
# Mon, 15 May 2023 21:20:18 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Mon, 15 May 2023 21:23:19 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Mon, 15 May 2023 21:23:19 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Mon, 15 May 2023 21:23:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 15 May 2023 21:23:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 15 May 2023 21:23:20 GMT
USER memcache
# Mon, 15 May 2023 21:23:20 GMT
EXPOSE 11211
# Mon, 15 May 2023 21:23:21 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5c0986f188e93dd7e76a4dc49a9170da2cd124709f5e1590b378e31a2b0d9587`  
		Last Modified: Tue, 09 May 2023 23:11:31 GMT  
		Size: 3.4 MB (3385631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2637efcb2bfb898454103e5536179d5f732cbddcd32f89c4ed51466ed8c6a14`  
		Last Modified: Thu, 11 May 2023 20:32:50 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45b064e3e507b9c35d5b605a606755605f7807236709d725567d0609ac53ee29`  
		Last Modified: Thu, 11 May 2023 20:32:50 GMT  
		Size: 123.9 KB (123933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a5d4f2fcda4a8d8a11f4f09bab2989aa2ec605ec585ed61bb4b519b62f5a47`  
		Last Modified: Mon, 15 May 2023 21:24:04 GMT  
		Size: 982.8 KB (982805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81d636c8d2e3e1cce3ec344ad3d21645a62a2c2286037cc287cd4e56c21d3fe7`  
		Last Modified: Mon, 15 May 2023 21:24:03 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca8ad226ad66d4c655b3b77ce26667f5b878d47000bfc558dae9c53ec6cff9b5`  
		Last Modified: Mon, 15 May 2023 21:24:03 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:alpine` - linux; s390x

```console
$ docker pull memcached@sha256:029a3ea9286bc7541646e7ca99fb57db8faffea15abf7bee651ee5cac65c4732
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4290940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac9f545f21c06b546f33df533b248b59335e5960e61844e6729780e8c404af6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 May 2023 23:11:06 GMT
ADD file:89d6e366e8ab41011a5866f8ca43aac6cfef00edffebad565918ab632a6d6210 in / 
# Tue, 09 May 2023 23:11:07 GMT
CMD ["/bin/sh"]
# Thu, 11 May 2023 19:55:27 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Thu, 11 May 2023 19:55:28 GMT
RUN apk add --no-cache libsasl
# Mon, 15 May 2023 21:51:02 GMT
ENV MEMCACHED_VERSION=1.6.20
# Mon, 15 May 2023 21:51:02 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Mon, 15 May 2023 21:54:04 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Mon, 15 May 2023 21:54:04 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Mon, 15 May 2023 21:54:04 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 15 May 2023 21:54:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 15 May 2023 21:54:04 GMT
USER memcache
# Mon, 15 May 2023 21:54:05 GMT
EXPOSE 11211
# Mon, 15 May 2023 21:54:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:25da54cc0a08f4ca602c6bcd3e52d70082eb8a25ee022bc9f1dda019de49197a`  
		Last Modified: Tue, 09 May 2023 23:11:35 GMT  
		Size: 3.2 MB (3226303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b276b6acd2b3a86c684a2f6a3641c76b4e2e5b3ce67562b64266899a052e6d4d`  
		Last Modified: Thu, 11 May 2023 19:59:45 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:483fe7c616264b630bec3883deae3b95c3220c0d46c5440048f5f2372224979c`  
		Last Modified: Thu, 11 May 2023 19:59:45 GMT  
		Size: 112.8 KB (112850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19827c7b432b650815a5843027a98d18e43bbd207cdda86bc95dc2f55c69b498`  
		Last Modified: Mon, 15 May 2023 21:54:45 GMT  
		Size: 950.1 KB (950116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da2238a07815946f6ba0dcbb105f0a4dab9db865ab4696d5c561fdd473328147`  
		Last Modified: Mon, 15 May 2023 21:54:46 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03dc27afabfb97c92d4893b707ee04b92ec5dd5e64ce581e0c27d7b344d7e735`  
		Last Modified: Mon, 15 May 2023 21:54:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:alpine3.18`

```console
$ docker pull memcached@sha256:f9aad561ac4e31d347b252c0fef6beede071bdaa205e38dc9dc5369201d8ff47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `memcached:alpine3.18` - linux; amd64

```console
$ docker pull memcached@sha256:a7a04bc20ec122d9f024dff57494853d5dc9705fb97af9170cc31a1f531dcaa5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4462373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15429daa972e1d57884e75ecc7f784564ae7cf089c25671dd118a0025f806b6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 20:50:58 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Wed, 14 Jun 2023 20:50:59 GMT
RUN apk add --no-cache libsasl
# Wed, 14 Jun 2023 20:50:59 GMT
ENV MEMCACHED_VERSION=1.6.20
# Wed, 14 Jun 2023 20:50:59 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Wed, 14 Jun 2023 20:53:09 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Wed, 14 Jun 2023 20:53:09 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 14 Jun 2023 20:53:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Jun 2023 20:53:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 20:53:09 GMT
USER memcache
# Wed, 14 Jun 2023 20:53:09 GMT
EXPOSE 11211
# Wed, 14 Jun 2023 20:53:09 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b2b2df106c5026cd33ea4ac655b77f25410ec9f4b8a6756ebc1ceeb79fca3c7`  
		Last Modified: Wed, 14 Jun 2023 20:53:58 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed63668528d3e2159f55909c66dc48a6f746ce24c2e2f6d963b992aefaa457ce`  
		Last Modified: Wed, 14 Jun 2023 20:53:58 GMT  
		Size: 108.1 KB (108080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc06ea6ffc2a4279c91e26e37b450afb1e0f1007815b19a7146d52b016dddc61`  
		Last Modified: Wed, 14 Jun 2023 20:53:59 GMT  
		Size: 954.7 KB (954748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:098e9e56712cb64736718f40b476d8eeb9410130c28ce94fe1bc2d380d9083cf`  
		Last Modified: Wed, 14 Jun 2023 20:53:59 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5c14818f6fb630a615284b18f945c89c0563530c25f07af955d0f85504020e9`  
		Last Modified: Wed, 14 Jun 2023 20:53:58 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:alpine3.18` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:e59934ff7bef6e6053b618f65923d2c1fa7235a008fb20f4fe9db13f8d6dc167
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4399194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dab6918acf63bcf26d1a95d40666c44f281aa14f0d4e27884d4c2f4b227dd9b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 20:57:26 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Wed, 14 Jun 2023 20:57:27 GMT
RUN apk add --no-cache libsasl
# Wed, 14 Jun 2023 20:57:27 GMT
ENV MEMCACHED_VERSION=1.6.20
# Wed, 14 Jun 2023 20:57:27 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Wed, 14 Jun 2023 20:59:54 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Wed, 14 Jun 2023 20:59:54 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 14 Jun 2023 20:59:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Jun 2023 20:59:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 20:59:55 GMT
USER memcache
# Wed, 14 Jun 2023 20:59:55 GMT
EXPOSE 11211
# Wed, 14 Jun 2023 20:59:55 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:666588188768f19b27fb821e02d084406af8fd867cc4595b896b9eed50b2105e`  
		Last Modified: Wed, 14 Jun 2023 21:00:51 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d958a137d671266f063c0af4d7b0b6d44d9018b77fdbddb8fd412d3c0b1be3`  
		Last Modified: Wed, 14 Jun 2023 21:00:51 GMT  
		Size: 124.1 KB (124137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eddee3cdc367d6f8265fe941f97020460db6cb5555711640b2ad62bd5c2a613c`  
		Last Modified: Wed, 14 Jun 2023 21:00:51 GMT  
		Size: 944.1 KB (944138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfec1ffcd9427d8fb06b908c1d3e0715a9db99c94c46f7896890a98b95c5f049`  
		Last Modified: Wed, 14 Jun 2023 21:00:51 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aea835bd4a5d779b88da37bc977813dd1ed9d228f5e78e3459edde4fa6f155e2`  
		Last Modified: Wed, 14 Jun 2023 21:00:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:alpine3.18` - linux; 386

```console
$ docker pull memcached@sha256:126e7a3993f53145ad966b11e0c8e7cb9f92520ea9899abfaa550aaee49c9f5c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4313116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:835ad308527d3b6bc85d49a990ae4c544363b3e3b3cef7a7a49ea6081d81a121`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 May 2023 23:11:03 GMT
ADD file:cfe47ebe49c4a75094234cafa52aa13aa26abcdad49b89293585884b3a8faeae in / 
# Tue, 09 May 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Thu, 11 May 2023 19:56:01 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Thu, 11 May 2023 19:56:03 GMT
RUN apk add --no-cache libsasl
# Mon, 15 May 2023 21:42:18 GMT
ENV MEMCACHED_VERSION=1.6.20
# Mon, 15 May 2023 21:42:18 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Mon, 15 May 2023 21:45:44 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Mon, 15 May 2023 21:45:44 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Mon, 15 May 2023 21:45:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 15 May 2023 21:45:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 15 May 2023 21:45:45 GMT
USER memcache
# Mon, 15 May 2023 21:45:45 GMT
EXPOSE 11211
# Mon, 15 May 2023 21:45:45 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:613767c5530f4016482e81288d0efdca4e58c62031252130d8fccd6f6260a068`  
		Last Modified: Tue, 09 May 2023 23:11:20 GMT  
		Size: 3.3 MB (3264862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72c25994ef1ec30cf62d081517b625d1ea87b0836bb6a90cd7ab8b1ab0501bb6`  
		Last Modified: Thu, 11 May 2023 20:00:35 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c42385514308725216c1a4eadb9aa4270c08f3140c342b6db43060f55af1ed`  
		Last Modified: Thu, 11 May 2023 20:00:35 GMT  
		Size: 109.5 KB (109521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3acbe617b4c6e3f32de32c1e69b84aa2c4e9c31d5e84a648a8340acda2452e03`  
		Last Modified: Mon, 15 May 2023 21:46:28 GMT  
		Size: 937.1 KB (937060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a81b72d4c28496fdd77fd3bf62a9800bd545660f44738482a100b00f99b3649c`  
		Last Modified: Mon, 15 May 2023 21:46:27 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c224abc2162f00f8769eeacb44838cbed654dd60d38e8d08d585003cb6495a`  
		Last Modified: Mon, 15 May 2023 21:46:27 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:alpine3.18` - linux; ppc64le

```console
$ docker pull memcached@sha256:912319e8c2e48db747d88d979ed43b691d125b7c05619189b4dcbe86f19b9a8b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4494043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c26bf354613881c6a96c357992e4176080f21ed4cac05a673e9a34056bd7d8be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 May 2023 23:11:09 GMT
ADD file:0a227602737a24c596923d3fd0a7c8b7d9000dbc6b80561473def09abbebbfa6 in / 
# Tue, 09 May 2023 23:11:10 GMT
CMD ["/bin/sh"]
# Thu, 11 May 2023 20:28:43 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Thu, 11 May 2023 20:28:45 GMT
RUN apk add --no-cache libsasl
# Mon, 15 May 2023 21:20:18 GMT
ENV MEMCACHED_VERSION=1.6.20
# Mon, 15 May 2023 21:20:18 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Mon, 15 May 2023 21:23:19 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Mon, 15 May 2023 21:23:19 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Mon, 15 May 2023 21:23:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 15 May 2023 21:23:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 15 May 2023 21:23:20 GMT
USER memcache
# Mon, 15 May 2023 21:23:20 GMT
EXPOSE 11211
# Mon, 15 May 2023 21:23:21 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5c0986f188e93dd7e76a4dc49a9170da2cd124709f5e1590b378e31a2b0d9587`  
		Last Modified: Tue, 09 May 2023 23:11:31 GMT  
		Size: 3.4 MB (3385631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2637efcb2bfb898454103e5536179d5f732cbddcd32f89c4ed51466ed8c6a14`  
		Last Modified: Thu, 11 May 2023 20:32:50 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45b064e3e507b9c35d5b605a606755605f7807236709d725567d0609ac53ee29`  
		Last Modified: Thu, 11 May 2023 20:32:50 GMT  
		Size: 123.9 KB (123933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a5d4f2fcda4a8d8a11f4f09bab2989aa2ec605ec585ed61bb4b519b62f5a47`  
		Last Modified: Mon, 15 May 2023 21:24:04 GMT  
		Size: 982.8 KB (982805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81d636c8d2e3e1cce3ec344ad3d21645a62a2c2286037cc287cd4e56c21d3fe7`  
		Last Modified: Mon, 15 May 2023 21:24:03 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca8ad226ad66d4c655b3b77ce26667f5b878d47000bfc558dae9c53ec6cff9b5`  
		Last Modified: Mon, 15 May 2023 21:24:03 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:alpine3.18` - linux; s390x

```console
$ docker pull memcached@sha256:029a3ea9286bc7541646e7ca99fb57db8faffea15abf7bee651ee5cac65c4732
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4290940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac9f545f21c06b546f33df533b248b59335e5960e61844e6729780e8c404af6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 May 2023 23:11:06 GMT
ADD file:89d6e366e8ab41011a5866f8ca43aac6cfef00edffebad565918ab632a6d6210 in / 
# Tue, 09 May 2023 23:11:07 GMT
CMD ["/bin/sh"]
# Thu, 11 May 2023 19:55:27 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Thu, 11 May 2023 19:55:28 GMT
RUN apk add --no-cache libsasl
# Mon, 15 May 2023 21:51:02 GMT
ENV MEMCACHED_VERSION=1.6.20
# Mon, 15 May 2023 21:51:02 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Mon, 15 May 2023 21:54:04 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Mon, 15 May 2023 21:54:04 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Mon, 15 May 2023 21:54:04 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 15 May 2023 21:54:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 15 May 2023 21:54:04 GMT
USER memcache
# Mon, 15 May 2023 21:54:05 GMT
EXPOSE 11211
# Mon, 15 May 2023 21:54:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:25da54cc0a08f4ca602c6bcd3e52d70082eb8a25ee022bc9f1dda019de49197a`  
		Last Modified: Tue, 09 May 2023 23:11:35 GMT  
		Size: 3.2 MB (3226303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b276b6acd2b3a86c684a2f6a3641c76b4e2e5b3ce67562b64266899a052e6d4d`  
		Last Modified: Thu, 11 May 2023 19:59:45 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:483fe7c616264b630bec3883deae3b95c3220c0d46c5440048f5f2372224979c`  
		Last Modified: Thu, 11 May 2023 19:59:45 GMT  
		Size: 112.8 KB (112850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19827c7b432b650815a5843027a98d18e43bbd207cdda86bc95dc2f55c69b498`  
		Last Modified: Mon, 15 May 2023 21:54:45 GMT  
		Size: 950.1 KB (950116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da2238a07815946f6ba0dcbb105f0a4dab9db865ab4696d5c561fdd473328147`  
		Last Modified: Mon, 15 May 2023 21:54:46 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03dc27afabfb97c92d4893b707ee04b92ec5dd5e64ce581e0c27d7b344d7e735`  
		Last Modified: Mon, 15 May 2023 21:54:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:bookworm`

```console
$ docker pull memcached@sha256:0495a71949e29a0dd91782be635586b244a336a765e79c78cfea895cd541e312
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; mips64le
	-	linux; ppc64le

### `memcached:bookworm` - linux; amd64

```console
$ docker pull memcached@sha256:533c607824b2f5781b179e175fcdf055577a3f076fb0a0fdcd13487c7c92125f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (38973406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbcfa8d0003c80b0bba4004f4b15b4a5600b9dd481ac2d887bc31e794f067464`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jun 2023 23:20:42 GMT
ADD file:ba1250b6ecd5dd09d4914189d72741c2817988994e7da514bf62be439a34bdb5 in / 
# Mon, 12 Jun 2023 23:20:42 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 20:48:19 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 14 Jun 2023 20:48:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jun 2023 20:48:24 GMT
ENV MEMCACHED_VERSION=1.6.20
# Wed, 14 Jun 2023 20:48:24 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Wed, 14 Jun 2023 20:50:40 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 14 Jun 2023 20:50:40 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 14 Jun 2023 20:50:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Jun 2023 20:50:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 20:50:41 GMT
USER memcache
# Wed, 14 Jun 2023 20:50:41 GMT
EXPOSE 11211
# Wed, 14 Jun 2023 20:50:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5b5fe70539cd6989aa19f25826309f9715a9489cf1c057982d6a84c1ad8975c7`  
		Last Modified: Mon, 12 Jun 2023 23:25:49 GMT  
		Size: 29.1 MB (29124744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab209434009a85e82d99c0547bb947940f9e1002ce6e965417396ee22a6820db`  
		Last Modified: Wed, 14 Jun 2023 20:53:33 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f4dfc49c9cdae8d4df855de7cc0460e5db8c762e73786d4f8fa4f69ba11d6d`  
		Last Modified: Wed, 14 Jun 2023 20:53:33 GMT  
		Size: 2.7 MB (2677239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96a3de0d22592d9a254814d5b77e3a84e73d2f055d162503fe811f731a320701`  
		Last Modified: Wed, 14 Jun 2023 20:53:34 GMT  
		Size: 7.2 MB (7169888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a38b201fb7fc8d917459453ee1c0218cf9845c96b885a02b02999f81b21c6bb`  
		Last Modified: Wed, 14 Jun 2023 20:53:33 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6f5720dc1980c886ee7e8d6067ed87e102bb31824e557a85fbd54273542debf`  
		Last Modified: Wed, 14 Jun 2023 20:53:33 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:3464bfccdfad0dc788e056949d59fc0b665ec165654b3a8502a2f4a3868a3dc7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 MB (37872888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20f33353745665e05e1722aa9af40e06b3f58778f8e758e786eaad30054de61f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jun 2023 23:40:13 GMT
ADD file:f75c3fe22fec548b35a86a9a5802fdc97497f5d253cf630d65f13282169d3f3f in / 
# Mon, 12 Jun 2023 23:40:14 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 20:54:33 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 14 Jun 2023 20:54:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jun 2023 20:54:37 GMT
ENV MEMCACHED_VERSION=1.6.20
# Wed, 14 Jun 2023 20:54:37 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Wed, 14 Jun 2023 20:57:13 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 14 Jun 2023 20:57:13 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 14 Jun 2023 20:57:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Jun 2023 20:57:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 20:57:14 GMT
USER memcache
# Wed, 14 Jun 2023 20:57:14 GMT
EXPOSE 11211
# Wed, 14 Jun 2023 20:57:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:95039a22a7cc3ae41d71f075e6e09e91e8da850fb5f80aba2f4a09f254520539`  
		Last Modified: Mon, 12 Jun 2023 23:44:08 GMT  
		Size: 29.2 MB (29152534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6da70104cc8ee465752315034f04011354e6149243e2bc69b9da49e6855df4b8`  
		Last Modified: Wed, 14 Jun 2023 21:00:29 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a7b40152f53e05b8cbcfe09be5b1598fcc05cf4f9ffad3b296eca43305450da`  
		Last Modified: Wed, 14 Jun 2023 21:00:30 GMT  
		Size: 2.5 MB (2539179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bf09d04f9c61af195486f42915b137b8612584f982737f5e465d02648a6dc8a`  
		Last Modified: Wed, 14 Jun 2023 21:00:30 GMT  
		Size: 6.2 MB (6179640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e71555e51295eeceeab1a9ab6bebb21108fbbe59e01349857c51932deea0f64`  
		Last Modified: Wed, 14 Jun 2023 21:00:29 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15cd3195dbfc5cedaf71b7c156002599dfb94219b51f85c966a1bee80bc37e65`  
		Last Modified: Wed, 14 Jun 2023 21:00:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:d2855c4deb19365dd1c83b81c9e1fa36f7873cc8b3dd02f8f01de10200bf208e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37554221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7068fffc8ee0a4607e1586297977a273786efb52e1782f11396ee5f7a5150c0f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 13 Jun 2023 00:09:02 GMT
ADD file:f91bd2a174259cb69646fc34ba2fc6b8941ad8e171d2d7952a4d8ac3d95e2ad7 in / 
# Tue, 13 Jun 2023 00:09:06 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 18:38:15 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 14 Jun 2023 18:38:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jun 2023 18:38:39 GMT
ENV MEMCACHED_VERSION=1.6.20
# Wed, 14 Jun 2023 18:38:41 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Wed, 14 Jun 2023 18:45:20 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 14 Jun 2023 18:45:23 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 14 Jun 2023 18:45:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Jun 2023 18:45:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 18:45:32 GMT
USER memcache
# Wed, 14 Jun 2023 18:45:35 GMT
EXPOSE 11211
# Wed, 14 Jun 2023 18:45:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3fc28260a4d871ef9781cad2bb064ad7212a5063de3a1d35dba938ce82115e5b`  
		Last Modified: Tue, 13 Jun 2023 00:22:29 GMT  
		Size: 29.1 MB (29118129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c804aeb794275ae845d32d2939d0e0fefa75cd112f1075aaf2104097050ae8`  
		Last Modified: Wed, 14 Jun 2023 18:46:04 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf29fcbe26928e2f4086a889098220505bdd4401dc87958f623ade0618efcd28`  
		Last Modified: Wed, 14 Jun 2023 18:46:05 GMT  
		Size: 1.9 MB (1934899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76d4e9cc234d41e69eba3bf411cb1d3ebe17e2fefbffb0c3458d613f2545337e`  
		Last Modified: Wed, 14 Jun 2023 18:46:09 GMT  
		Size: 6.5 MB (6499709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0988c34e4840378b9876eba362b50458e769389d0cc626698bef65e46c721458`  
		Last Modified: Wed, 14 Jun 2023 18:46:04 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db55745458426cdf0d23fd0589fd440e2d328e4d5ffb00a9ef6d2e0225cec8bf`  
		Last Modified: Wed, 14 Jun 2023 18:46:04 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:0e023c41d9c6a8d04edad22ecea59cfcf424d0dc3895c442a9e7a4575961d53d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43193448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a85a60b74a9575a203aba1a5f800dfe479b80cde8ff577ccd5e7e77bdaab64c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jun 2023 23:17:34 GMT
ADD file:3f8b9849acb625537f99921ef80190de7b03afdc287a5d1113a92cc41ae24be2 in / 
# Mon, 12 Jun 2023 23:17:36 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 18:15:42 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 14 Jun 2023 18:15:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jun 2023 18:15:50 GMT
ENV MEMCACHED_VERSION=1.6.20
# Wed, 14 Jun 2023 18:15:51 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Wed, 14 Jun 2023 18:19:27 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 14 Jun 2023 18:19:28 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 14 Jun 2023 18:19:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Jun 2023 18:19:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 18:19:31 GMT
USER memcache
# Wed, 14 Jun 2023 18:19:32 GMT
EXPOSE 11211
# Wed, 14 Jun 2023 18:19:32 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9f041b53cef30007c43057f2520876c85ed6bee6be5aaee867dfb31a053d6cca`  
		Last Modified: Mon, 12 Jun 2023 23:24:09 GMT  
		Size: 33.1 MB (33116725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a2d84b1fee81412bbd9bb301c77e6dfacfac70c2f1485de806658b49b06e08`  
		Last Modified: Wed, 14 Jun 2023 18:19:49 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca8bb5af043b48c9fe0e110ee13c139ceb715570346140fc86092d582d38b52b`  
		Last Modified: Wed, 14 Jun 2023 18:19:50 GMT  
		Size: 2.9 MB (2891306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e2d7805a151ec1618da95ad34cb2fdc6ae889b9f7908aaca6d063ca864f3e24`  
		Last Modified: Wed, 14 Jun 2023 18:19:52 GMT  
		Size: 7.2 MB (7183881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc5db4b315753422be0d08638f594b1ec64484c44f68942473f903387853b3bd`  
		Last Modified: Wed, 14 Jun 2023 18:19:49 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a8a9b2ed7c41d27d92f9db3c21beec2a2e288b0bc54a19aa1d3574b6085eaa6`  
		Last Modified: Wed, 14 Jun 2023 18:19:49 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:latest`

```console
$ docker pull memcached@sha256:b98fa1ffaab2dcd8d970fe7030487920c8edc93b2a932f263bc4e0475d0ac2b3
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
$ docker pull memcached@sha256:533c607824b2f5781b179e175fcdf055577a3f076fb0a0fdcd13487c7c92125f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (38973406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbcfa8d0003c80b0bba4004f4b15b4a5600b9dd481ac2d887bc31e794f067464`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jun 2023 23:20:42 GMT
ADD file:ba1250b6ecd5dd09d4914189d72741c2817988994e7da514bf62be439a34bdb5 in / 
# Mon, 12 Jun 2023 23:20:42 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 20:48:19 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 14 Jun 2023 20:48:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jun 2023 20:48:24 GMT
ENV MEMCACHED_VERSION=1.6.20
# Wed, 14 Jun 2023 20:48:24 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Wed, 14 Jun 2023 20:50:40 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 14 Jun 2023 20:50:40 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 14 Jun 2023 20:50:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Jun 2023 20:50:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 20:50:41 GMT
USER memcache
# Wed, 14 Jun 2023 20:50:41 GMT
EXPOSE 11211
# Wed, 14 Jun 2023 20:50:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5b5fe70539cd6989aa19f25826309f9715a9489cf1c057982d6a84c1ad8975c7`  
		Last Modified: Mon, 12 Jun 2023 23:25:49 GMT  
		Size: 29.1 MB (29124744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab209434009a85e82d99c0547bb947940f9e1002ce6e965417396ee22a6820db`  
		Last Modified: Wed, 14 Jun 2023 20:53:33 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f4dfc49c9cdae8d4df855de7cc0460e5db8c762e73786d4f8fa4f69ba11d6d`  
		Last Modified: Wed, 14 Jun 2023 20:53:33 GMT  
		Size: 2.7 MB (2677239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96a3de0d22592d9a254814d5b77e3a84e73d2f055d162503fe811f731a320701`  
		Last Modified: Wed, 14 Jun 2023 20:53:34 GMT  
		Size: 7.2 MB (7169888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a38b201fb7fc8d917459453ee1c0218cf9845c96b885a02b02999f81b21c6bb`  
		Last Modified: Wed, 14 Jun 2023 20:53:33 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6f5720dc1980c886ee7e8d6067ed87e102bb31824e557a85fbd54273542debf`  
		Last Modified: Wed, 14 Jun 2023 20:53:33 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:latest` - linux; arm variant v5

```console
$ docker pull memcached@sha256:9dba87e9c87eb3058b7db8d6a35423e25ff2aaa7baabb27c5e6137017c48fe1a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 MB (30470602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:308667429b0aed213503576d9f474cc30e4f0181773f9cee3aa2ac42d3c74a7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jun 2023 23:48:46 GMT
ADD file:b2773fa62bdb5672863ef317ee1b58de2a6074fe6aa0d8287a7cd0999028d7d2 in / 
# Mon, 12 Jun 2023 23:48:47 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 04:08:38 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 13 Jun 2023 04:08:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 04:08:45 GMT
ENV MEMCACHED_VERSION=1.6.20
# Tue, 13 Jun 2023 04:08:45 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Tue, 13 Jun 2023 04:11:47 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 13 Jun 2023 04:11:47 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 13 Jun 2023 04:11:48 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 13 Jun 2023 04:11:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jun 2023 04:11:49 GMT
USER memcache
# Tue, 13 Jun 2023 04:11:49 GMT
EXPOSE 11211
# Tue, 13 Jun 2023 04:11:49 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c04d7d6633d9b8cf1bfa9f6831ac7dd6f985411cb6307d91c6373085b09b8c19`  
		Last Modified: Mon, 12 Jun 2023 23:52:06 GMT  
		Size: 28.9 MB (28918779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1860b36b146eb799ae5299a102c03f7c12063adcb754066bd9eab20450d0cebb`  
		Last Modified: Tue, 13 Jun 2023 04:12:05 GMT  
		Size: 4.9 KB (4890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:557508c54a290bb2d6fda92e97a2058bcc1de808bcca254bb1559ea268d1bc8c`  
		Last Modified: Tue, 13 Jun 2023 04:12:06 GMT  
		Size: 316.8 KB (316757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67839ee937c662a3b1177503ab80dd4b2c4f95b5d0a8ffdf33276e7e30eecc85`  
		Last Modified: Tue, 13 Jun 2023 04:12:06 GMT  
		Size: 1.2 MB (1229770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e2a90f0421d9b93e896ff2136b06e5d157fd43ccd4cd1d62da5d0f8ba0466d9`  
		Last Modified: Tue, 13 Jun 2023 04:12:05 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e85a558ae3e0a483e80e987991797c179374d3573bf62638af5a4e2b1fb3c730`  
		Last Modified: Tue, 13 Jun 2023 04:12:05 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:latest` - linux; arm variant v7

```console
$ docker pull memcached@sha256:2841be0a36134563966c09a6ed68b21053d20342ec8736cf92763c28077ead43
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28094215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cf74ffa940dd93988fc0beb6698c5796563c82a40b7dd668153969f64d2e6ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 09 Feb 2023 06:12:09 GMT
ADD file:5f1a343224e8486690bd90dd1e50c8d84b3d770c51bb6829544e5cf650c0419c in / 
# Thu, 09 Feb 2023 06:12:10 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 07:52:31 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Thu, 09 Feb 2023 07:52:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 07:52:35 GMT
ENV MEMCACHED_VERSION=1.6.18
# Thu, 09 Feb 2023 07:52:35 GMT
ENV MEMCACHED_SHA1=be16909bb75ab972ee5fe438312501de01c4725a
# Thu, 09 Feb 2023 07:55:44 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Thu, 09 Feb 2023 07:55:44 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 09 Feb 2023 07:55:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 09 Feb 2023 07:55:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Feb 2023 07:55:44 GMT
USER memcache
# Thu, 09 Feb 2023 07:55:45 GMT
EXPOSE 11211
# Thu, 09 Feb 2023 07:55:45 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:e7318f6106ad75d7d482ae9dddf4d927b0872ef3ddb6e1330aa691fc8d17279e`  
		Last Modified: Thu, 09 Feb 2023 06:19:19 GMT  
		Size: 26.6 MB (26577666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de49d9d72daf1680b5f1b9532dd2eb0162829f36c8db9669935462636fbf99d9`  
		Last Modified: Thu, 09 Feb 2023 08:06:11 GMT  
		Size: 4.9 KB (4895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0beac9d5bcac946f8c54c72b8a9c136914b1aa7a5fe2b8c3df4c7d8858ea6559`  
		Last Modified: Thu, 09 Feb 2023 08:06:11 GMT  
		Size: 312.1 KB (312088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4c9e5a265394e4c0f357779e6195a4e82d767a3691a0e77d427e56651c3e54a`  
		Last Modified: Thu, 09 Feb 2023 08:06:11 GMT  
		Size: 1.2 MB (1199163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ea82ad892fe1ae8623d84e32c8c027087cda8aa49e40d4546ed6942e471c60`  
		Last Modified: Thu, 09 Feb 2023 08:06:11 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2ae3bcdc0d114ba49a67df022b6f7215fc87f1f50e64939fcfbbec4eaadee5`  
		Last Modified: Thu, 09 Feb 2023 08:06:11 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:latest` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:3464bfccdfad0dc788e056949d59fc0b665ec165654b3a8502a2f4a3868a3dc7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 MB (37872888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20f33353745665e05e1722aa9af40e06b3f58778f8e758e786eaad30054de61f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jun 2023 23:40:13 GMT
ADD file:f75c3fe22fec548b35a86a9a5802fdc97497f5d253cf630d65f13282169d3f3f in / 
# Mon, 12 Jun 2023 23:40:14 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 20:54:33 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 14 Jun 2023 20:54:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jun 2023 20:54:37 GMT
ENV MEMCACHED_VERSION=1.6.20
# Wed, 14 Jun 2023 20:54:37 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Wed, 14 Jun 2023 20:57:13 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 14 Jun 2023 20:57:13 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 14 Jun 2023 20:57:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Jun 2023 20:57:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 20:57:14 GMT
USER memcache
# Wed, 14 Jun 2023 20:57:14 GMT
EXPOSE 11211
# Wed, 14 Jun 2023 20:57:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:95039a22a7cc3ae41d71f075e6e09e91e8da850fb5f80aba2f4a09f254520539`  
		Last Modified: Mon, 12 Jun 2023 23:44:08 GMT  
		Size: 29.2 MB (29152534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6da70104cc8ee465752315034f04011354e6149243e2bc69b9da49e6855df4b8`  
		Last Modified: Wed, 14 Jun 2023 21:00:29 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a7b40152f53e05b8cbcfe09be5b1598fcc05cf4f9ffad3b296eca43305450da`  
		Last Modified: Wed, 14 Jun 2023 21:00:30 GMT  
		Size: 2.5 MB (2539179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bf09d04f9c61af195486f42915b137b8612584f982737f5e465d02648a6dc8a`  
		Last Modified: Wed, 14 Jun 2023 21:00:30 GMT  
		Size: 6.2 MB (6179640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e71555e51295eeceeab1a9ab6bebb21108fbbe59e01349857c51932deea0f64`  
		Last Modified: Wed, 14 Jun 2023 21:00:29 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15cd3195dbfc5cedaf71b7c156002599dfb94219b51f85c966a1bee80bc37e65`  
		Last Modified: Wed, 14 Jun 2023 21:00:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:latest` - linux; 386

```console
$ docker pull memcached@sha256:719a898d7d05b1981b584eaaadd22e357c8a3b1b53509053cb6cc089cd6a38e0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (33997029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae0070d643d6b72bec5cad5100ac31c4fcb9b3108bade974a59d9933c70bda21`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jun 2023 23:39:58 GMT
ADD file:440924fd31c090a7f5e3d36276d17574922eb3e8ececce333fa42f7a95bdd9ce in / 
# Mon, 12 Jun 2023 23:39:58 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 20:20:47 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 13 Jun 2023 20:20:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 20:20:52 GMT
ENV MEMCACHED_VERSION=1.6.20
# Tue, 13 Jun 2023 20:20:52 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Tue, 13 Jun 2023 20:24:26 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 13 Jun 2023 20:24:26 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 13 Jun 2023 20:24:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 13 Jun 2023 20:24:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jun 2023 20:24:27 GMT
USER memcache
# Tue, 13 Jun 2023 20:24:27 GMT
EXPOSE 11211
# Tue, 13 Jun 2023 20:24:27 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1646137eb700afc9e891c03fdf28d3f5bc489ef0200fdacc67beee837d48db7d`  
		Last Modified: Mon, 12 Jun 2023 23:47:07 GMT  
		Size: 32.4 MB (32397388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9622551bea561b9c36a4e6d3a95484a278b356138badefce3b9186fc736fd556`  
		Last Modified: Tue, 13 Jun 2023 20:25:00 GMT  
		Size: 4.9 KB (4894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c12401a5e374bfe8c291818c808a2425cd0b16ac8cd178a47c8bf5eea598755b`  
		Last Modified: Tue, 13 Jun 2023 20:25:00 GMT  
		Size: 336.8 KB (336783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c456f2d87234421d6c272fad6161dc85df8bac55c7ea1750d68a216dd1534ee`  
		Last Modified: Tue, 13 Jun 2023 20:25:11 GMT  
		Size: 1.3 MB (1257556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:178b408b1cbfa94c9656a36bf64bf57a8df765953c7ec4c7e224851c29d35f71`  
		Last Modified: Tue, 13 Jun 2023 20:25:00 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6210b196c4e58f73e538fc8b508a56ac8918a914f6da6fd95c9721389d06c0a9`  
		Last Modified: Tue, 13 Jun 2023 20:25:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:latest` - linux; mips64le

```console
$ docker pull memcached@sha256:d2855c4deb19365dd1c83b81c9e1fa36f7873cc8b3dd02f8f01de10200bf208e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37554221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7068fffc8ee0a4607e1586297977a273786efb52e1782f11396ee5f7a5150c0f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 13 Jun 2023 00:09:02 GMT
ADD file:f91bd2a174259cb69646fc34ba2fc6b8941ad8e171d2d7952a4d8ac3d95e2ad7 in / 
# Tue, 13 Jun 2023 00:09:06 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 18:38:15 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 14 Jun 2023 18:38:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jun 2023 18:38:39 GMT
ENV MEMCACHED_VERSION=1.6.20
# Wed, 14 Jun 2023 18:38:41 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Wed, 14 Jun 2023 18:45:20 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 14 Jun 2023 18:45:23 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 14 Jun 2023 18:45:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Jun 2023 18:45:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 18:45:32 GMT
USER memcache
# Wed, 14 Jun 2023 18:45:35 GMT
EXPOSE 11211
# Wed, 14 Jun 2023 18:45:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3fc28260a4d871ef9781cad2bb064ad7212a5063de3a1d35dba938ce82115e5b`  
		Last Modified: Tue, 13 Jun 2023 00:22:29 GMT  
		Size: 29.1 MB (29118129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c804aeb794275ae845d32d2939d0e0fefa75cd112f1075aaf2104097050ae8`  
		Last Modified: Wed, 14 Jun 2023 18:46:04 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf29fcbe26928e2f4086a889098220505bdd4401dc87958f623ade0618efcd28`  
		Last Modified: Wed, 14 Jun 2023 18:46:05 GMT  
		Size: 1.9 MB (1934899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76d4e9cc234d41e69eba3bf411cb1d3ebe17e2fefbffb0c3458d613f2545337e`  
		Last Modified: Wed, 14 Jun 2023 18:46:09 GMT  
		Size: 6.5 MB (6499709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0988c34e4840378b9876eba362b50458e769389d0cc626698bef65e46c721458`  
		Last Modified: Wed, 14 Jun 2023 18:46:04 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db55745458426cdf0d23fd0589fd440e2d328e4d5ffb00a9ef6d2e0225cec8bf`  
		Last Modified: Wed, 14 Jun 2023 18:46:04 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:latest` - linux; ppc64le

```console
$ docker pull memcached@sha256:0e023c41d9c6a8d04edad22ecea59cfcf424d0dc3895c442a9e7a4575961d53d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43193448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a85a60b74a9575a203aba1a5f800dfe479b80cde8ff577ccd5e7e77bdaab64c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 12 Jun 2023 23:17:34 GMT
ADD file:3f8b9849acb625537f99921ef80190de7b03afdc287a5d1113a92cc41ae24be2 in / 
# Mon, 12 Jun 2023 23:17:36 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 18:15:42 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Wed, 14 Jun 2023 18:15:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jun 2023 18:15:50 GMT
ENV MEMCACHED_VERSION=1.6.20
# Wed, 14 Jun 2023 18:15:51 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Wed, 14 Jun 2023 18:19:27 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Wed, 14 Jun 2023 18:19:28 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Wed, 14 Jun 2023 18:19:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Jun 2023 18:19:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 18:19:31 GMT
USER memcache
# Wed, 14 Jun 2023 18:19:32 GMT
EXPOSE 11211
# Wed, 14 Jun 2023 18:19:32 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9f041b53cef30007c43057f2520876c85ed6bee6be5aaee867dfb31a053d6cca`  
		Last Modified: Mon, 12 Jun 2023 23:24:09 GMT  
		Size: 33.1 MB (33116725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a2d84b1fee81412bbd9bb301c77e6dfacfac70c2f1485de806658b49b06e08`  
		Last Modified: Wed, 14 Jun 2023 18:19:49 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca8bb5af043b48c9fe0e110ee13c139ceb715570346140fc86092d582d38b52b`  
		Last Modified: Wed, 14 Jun 2023 18:19:50 GMT  
		Size: 2.9 MB (2891306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e2d7805a151ec1618da95ad34cb2fdc6ae889b9f7908aaca6d063ca864f3e24`  
		Last Modified: Wed, 14 Jun 2023 18:19:52 GMT  
		Size: 7.2 MB (7183881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc5db4b315753422be0d08638f594b1ec64484c44f68942473f903387853b3bd`  
		Last Modified: Wed, 14 Jun 2023 18:19:49 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a8a9b2ed7c41d27d92f9db3c21beec2a2e288b0bc54a19aa1d3574b6085eaa6`  
		Last Modified: Wed, 14 Jun 2023 18:19:49 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:latest` - linux; s390x

```console
$ docker pull memcached@sha256:882f9d1d57c58c374c6074cbce0784748bdce465757ad946f699a47a924f4518
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31228777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:098ff94df44cb535cdd4f10e4106756fc1766a232277b3a9c2f51ff567ee3082`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 13 Jun 2023 04:30:13 GMT
ADD file:558e8c34e969d458ce6bf4207d9c0fe05d2e67d3457c1d5689666749e82ef2ab in / 
# Tue, 13 Jun 2023 04:30:14 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 18:41:51 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 13 Jun 2023 18:41:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 18:41:54 GMT
ENV MEMCACHED_VERSION=1.6.20
# Tue, 13 Jun 2023 18:41:54 GMT
ENV MEMCACHED_SHA1=face85ed6fad41432ad818445b24eca55bccdd78
# Tue, 13 Jun 2023 18:44:58 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 13 Jun 2023 18:44:58 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 13 Jun 2023 18:44:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 13 Jun 2023 18:44:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jun 2023 18:44:59 GMT
USER memcache
# Tue, 13 Jun 2023 18:44:59 GMT
EXPOSE 11211
# Tue, 13 Jun 2023 18:44:59 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6a752e2308c741009b6f5a88a8ea6764b96ebe7f544197912d8ef9a3ec8c8763`  
		Last Modified: Tue, 13 Jun 2023 04:34:49 GMT  
		Size: 29.7 MB (29652514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:465e13673c57447925389cdcf074d61ff5114faa447fd3b775481a229ac38019`  
		Last Modified: Tue, 13 Jun 2023 18:45:27 GMT  
		Size: 5.0 KB (5023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a81fcab4fd1cd8ac9cc18539fde149b89e423f0b5c80f2f07460f49209907ca`  
		Last Modified: Tue, 13 Jun 2023 18:45:27 GMT  
		Size: 324.3 KB (324337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a035c15be3c1e4f3cd28a1c060f56d03f4fa02c5e86290288ac74b2533feca`  
		Last Modified: Tue, 13 Jun 2023 18:45:27 GMT  
		Size: 1.2 MB (1246496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdda04e27e25f6bf6f5489a28d36c1903052488bf96ee74f76b993a5926207b7`  
		Last Modified: Tue, 13 Jun 2023 18:45:27 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d62044b354beed912ecf01ba2d6b0efc230907a720539c8850809e2b76f9ac89`  
		Last Modified: Tue, 13 Jun 2023 18:45:27 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
