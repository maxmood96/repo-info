## `memcached:latest`

```console
$ docker pull memcached@sha256:03931e8d8cddcfad7746ce5c02b2500b1364b7cd54a70bc8659e38489de568ec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 15
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `memcached:latest` - linux; amd64

```console
$ docker pull memcached@sha256:ff30590f737a537eda95003f3eebf9954bb71ae3eae92326d36d8efe995ae0d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38817611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e89b92b1e7ff13f14853ae2b16915de3b3afbf465b958005d848a01a249df57c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:af0f4e41d68b67ca88a1ce6297326159e18e27670d7bfc0bf5804a4e2b268cc8 in / 
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c57ee5000d61345aa3ee6684794a8110328e2274d9a5ae7855969d1a26394463`  
		Last Modified: Wed, 31 Jan 2024 22:39:55 GMT  
		Size: 29.2 MB (29150465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f8266cefe136fd2f1ab13b1394f89c6c4703bc3654678d2da5af15e4cbb3f1`  
		Last Modified: Wed, 31 Jan 2024 23:58:12 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f15e20f332b9b7671a545f46faf60e5d727284b8bdb80f398e1e9dfb4811209`  
		Last Modified: Wed, 31 Jan 2024 23:58:13 GMT  
		Size: 2.5 MB (2488287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c5ee734813fffb0ab014577770c8a8a78595b8b5a842113392f5e48b5cc5a4`  
		Last Modified: Wed, 31 Jan 2024 23:58:13 GMT  
		Size: 7.2 MB (7177345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:689292f0b9daa2c749263d90fcd1f9d1522a41790533a291e922a92c50393538`  
		Last Modified: Wed, 31 Jan 2024 23:58:12 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f7439b1a90269ca53407226816f8b68b388d0b93a1a7c161f58160e6a36bc8b`  
		Last Modified: Wed, 31 Jan 2024 23:58:13 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:5a82860e855baa701e19b31ef826f266fbdf2fc4a9c81379c4efed4beeccf9b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3077977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c693f59edab94442f8c91c26a913e6084c8a4c8262200a6031be817fb958f246`

```dockerfile
```

-	Layers:
	-	`sha256:fe54d111ed7e067b9b221ecf4b96c3783bb842d0f302d58ab1592a65eb25ad34`  
		Last Modified: Wed, 31 Jan 2024 23:58:13 GMT  
		Size: 3.1 MB (3056860 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31118b2dc5d42c88fbaf84dfab7821e1b35870cb8e57d55e000650b05ef77228`  
		Last Modified: Wed, 31 Jan 2024 23:58:12 GMT  
		Size: 21.1 KB (21117 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm variant v5

```console
$ docker pull memcached@sha256:8e86128cd2c342c70f09781122cf0f05a3272ff453390d7ad0bc297f045fec73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34837870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd7c48a5dca72bd4ccb09d5cf7d2a47f288fae2a314f0d3cf9ef19180d1c35c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:557a5348da1e680593a9ba709ef059b96baf15e0c89d8f8343e97bf008d9dc05 in / 
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b508f3272b9b70b8dd19c621a4da1be63880a1f6412063787647ceeb464d772a`  
		Last Modified: Wed, 31 Jan 2024 22:48:00 GMT  
		Size: 26.9 MB (26909323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ba9a8852680f3cd38888d0d8a0bebb47528cdf5e052bd19583852b7d43e67e`  
		Last Modified: Thu, 01 Feb 2024 12:03:54 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89527861abbd712337498c067ec298a29decbf12459572af1711d56a34dee0a1`  
		Last Modified: Thu, 01 Feb 2024 12:03:55 GMT  
		Size: 2.1 MB (2089337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d522efca1b0ccdcaf6b05d16e90f1bbf0b8e2dfe22f431eeee3a302bd186220`  
		Last Modified: Thu, 01 Feb 2024 12:03:55 GMT  
		Size: 5.8 MB (5837697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25881524efc77f47ad43de631c004391fa7a89d6dc0514e1cfa8073de21da220`  
		Last Modified: Thu, 01 Feb 2024 12:03:54 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f0dd581faca44eb4c17e6eaed561277197fb4e94c40fac94f57ae66563e7d47`  
		Last Modified: Thu, 01 Feb 2024 12:03:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:8b8e6b54c0f8fbd0c1186e280c96ab15c7b154bac4692540b322c4998ef74637
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3052683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cbc187760c3e1cf619df4e57ba85ce22f1bfb0817f135c231c936cc134574d7`

```dockerfile
```

-	Layers:
	-	`sha256:e92f2cae653ab89999b7d6fe0b321176c8a61a7189105a939b127375e058cc93`  
		Last Modified: Thu, 01 Feb 2024 12:03:55 GMT  
		Size: 3.0 MB (3031592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0272a95396760e3361496c2020e39647222569e7c7aadae2d978c7b4ef8ea528`  
		Last Modified: Thu, 01 Feb 2024 12:03:54 GMT  
		Size: 21.1 KB (21091 bytes)  
		MIME: application/vnd.in-toto+json

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
$ docker pull memcached@sha256:9d718ce26a805aec4485817a1bd552ad45d32ea847ce3fc84b60053d3a5dfd43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37713646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c8d699449910b7ac3ddf91d5426959cc2ba738af46ead998d420e59a9c436ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:ef6f078c1e72fcfafb9bfeeff0c1c771219dc2efe34650963106f63d32183b49 in / 
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:25d3892798f8b99159e3c1136799bfed560027ce451b50d57d961f4f02577ff5`  
		Last Modified: Wed, 31 Jan 2024 22:48:07 GMT  
		Size: 29.2 MB (29180832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab18bb1a48e459d35562d68e4d72fbe40d8122622e23a200c5b54e1989da051`  
		Last Modified: Thu, 01 Feb 2024 15:45:07 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee6a1368704439587e2f4ad30d961a7a73db9959b816c6a015e03eaf8dc7e93`  
		Last Modified: Thu, 01 Feb 2024 15:45:07 GMT  
		Size: 2.3 MB (2346029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10bef75433444308341fb147de10d548d986ac22b3de67b6210782e8a82bf2bd`  
		Last Modified: Thu, 01 Feb 2024 15:45:07 GMT  
		Size: 6.2 MB (6185271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0290edc95a87f11d9bad6e5bb40f825ae5aceaab8a7a797c971d476135087a81`  
		Last Modified: Thu, 01 Feb 2024 15:45:07 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44cd2a5ad3367bb8046501b88e7a9e42cead0a07b9472f37e76affe0828056c3`  
		Last Modified: Thu, 01 Feb 2024 15:45:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:fe9cd6870d88c823b374f9a63d0c8060570547492f80eed9afe89a4130497537
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3053019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c491546ae238bfe3883c1aa804c64132974cd1bbc6231ec62fbbc16ec11bd627`

```dockerfile
```

-	Layers:
	-	`sha256:ed859e0caef4812572948d51d02b995f286fb0c623151e8f036270e3a3805931`  
		Last Modified: Thu, 01 Feb 2024 15:45:07 GMT  
		Size: 3.0 MB (3032051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c06e6fde8575a2a28e4a507a9c9c3ba78984770a78887e57e1747d016330710a`  
		Last Modified: Thu, 01 Feb 2024 15:45:07 GMT  
		Size: 21.0 KB (20968 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; 386

```console
$ docker pull memcached@sha256:ca3b6ca982deaa72dcfdc5da6df027479a4736932fd9919cfffc5bae42c421ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39296439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf0c4c2a178ea5e2c4702f614bcc26b9c9ead8a427d7b5e05776820ef5e12e93`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:540e2de73452bd162dd7f630bf29f60e7d2e4a7a5d32a495bedf8ad390b59d7f in / 
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:34ef135b45f33052e8e5bca668f9a45a938944a9cf3fb73a46f54a7bf11f091b`  
		Last Modified: Wed, 31 Jan 2024 22:43:46 GMT  
		Size: 30.2 MB (30165018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5478fab2ccb797d86b46482eb05f7133c2b3f9dae9865e93299ea51cf22285`  
		Last Modified: Wed, 31 Jan 2024 23:58:08 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d31863b054bfad60b8b30dee7709bd98320b57dbdcf6c0bf83d387b0adf6ba`  
		Last Modified: Wed, 31 Jan 2024 23:58:08 GMT  
		Size: 2.5 MB (2492548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28f7c8c0b676ced8194663f8f2c9861b31c8e97d1db96d48290cd56863d1ca8a`  
		Last Modified: Wed, 31 Jan 2024 23:58:09 GMT  
		Size: 6.6 MB (6637360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3db08dc73d9fbae8259028dc816383a88b7a5768bde676fa3893ad57db45e1b`  
		Last Modified: Wed, 31 Jan 2024 23:58:08 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b878efec9e6e1d3d6cdbac9abf8d74061f832572f8fa8650858a1cbeff5ae6`  
		Last Modified: Wed, 31 Jan 2024 23:58:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:66631e96cafdbfb2bec44fec011b2f6c6afc043c7ac5c2025764b60b7ae94c40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3072225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9381af31968bb045fed6da3ab0349ca70f51140689e90065748ce79d2e977e8`

```dockerfile
```

-	Layers:
	-	`sha256:43296035206d08347837af96c0c1aa8124158fc9aac7621c7e6e16c87fd08464`  
		Last Modified: Wed, 31 Jan 2024 23:58:09 GMT  
		Size: 3.1 MB (3051163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41ebcd051b80d30692a4944bf6a1114cb6699b201d5fffed5613a84b8e4102aa`  
		Last Modified: Wed, 31 Jan 2024 23:58:08 GMT  
		Size: 21.1 KB (21062 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; mips64le

```console
$ docker pull memcached@sha256:b0d2a77badf1e2d1a99e6bb7115326d6b911d6ca2c246dfdb56c96a2a9c8981c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37564346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc5c60532478160437282118a662e353eae40a7868f889d1bfdbc86942a42ba5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:61bc6da4a8a8247e6b88cf149051dbb04a6a5e6e1ffc5da16a85d1b4f24be297 in / 
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4f1541106f1f6cee2d65a870d8d3fbbaef35e04dbcb8abaa9623a9f7137a6ae5`  
		Last Modified: Thu, 11 Jan 2024 02:22:46 GMT  
		Size: 29.1 MB (29121397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef2fb570e6fcef7e8ab69928066def22aa34c3502d43341f5e19ec8cfa1676d`  
		Last Modified: Fri, 12 Jan 2024 03:59:35 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74ec7faabaa26819dfb3452d8d7de1acca479fce5b0cca2375f1b7b32f859cf`  
		Last Modified: Fri, 12 Jan 2024 03:59:35 GMT  
		Size: 1.9 MB (1937519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a85208eb590ea0a7eb554c32359b8cfef3bc72b04fa53d9a8b0f952de341da`  
		Last Modified: Fri, 12 Jan 2024 03:59:36 GMT  
		Size: 6.5 MB (6503913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e48a65a1d8ef8b534588b9a37b73a0f023cc581beca25f945b24f4c2f9b1a06e`  
		Last Modified: Fri, 12 Jan 2024 03:59:35 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8cfa39320a3903c9f1ba71e24ced26243c8c5903f9cfdd3c8293f50ef0ca67`  
		Last Modified: Fri, 12 Jan 2024 03:59:36 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:a4f67d3b570b7c893ec9792e0caf38fe2505694b8605b0deb19092923c703010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f1c9080020a19467b5cbb27860d5f730b75880bf6eb846ec5d90263b7c596bb`

```dockerfile
```

-	Layers:
	-	`sha256:e18ad2cb250c856e66d4cf41aff50aa5017497ba19004bc8d6aef0ac669c2cdd`  
		Last Modified: Fri, 12 Jan 2024 03:59:35 GMT  
		Size: 20.8 KB (20836 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; ppc64le

```console
$ docker pull memcached@sha256:ecd6dadcdef583c8d3c4d794c97d1adbc9b61dba6c159054583fce11d59aed8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.0 MB (43032879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a7cd2dcbe213623485104fdffb2ba72838d2cce3fb3c396e519a6fdf18b4709`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:fca8b919a8d1e36420dd1e3f3e427aaaae28a2f57e46c27207acd8e3df0d7a97 in / 
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:dfeacd5cd8171f4516ea86dadfb60a372eabf49428dc23d2efdda68cff5b05e7`  
		Last Modified: Wed, 31 Jan 2024 22:34:24 GMT  
		Size: 33.1 MB (33142917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32887b5925f858268780490025fddcc36ca0b29296eb4b4f40ad08f021b18981`  
		Last Modified: Thu, 01 Feb 2024 13:18:22 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e68859bd20462eab721e5d0b691471b945575fe99088663ec6fbe22a0ac0fbc4`  
		Last Modified: Thu, 01 Feb 2024 13:18:22 GMT  
		Size: 2.7 MB (2698225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e71dbf42012ab98bd878e63e425dc08cd3c7131242c61763234ac5c844ec854`  
		Last Modified: Thu, 01 Feb 2024 13:18:22 GMT  
		Size: 7.2 MB (7190225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bdb7f683db851ce3c60bae8d4f83707259d6624cc5abcec486bee1e25e299e4`  
		Last Modified: Thu, 01 Feb 2024 13:18:22 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d01a9fd606614804578135dd39abf21b8ac94d34e713548be984e27fca57e6`  
		Last Modified: Thu, 01 Feb 2024 13:18:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:4a244f61a26dde3259ad807d257e80d025c2b6dcb549560f7a7b7ad10c21b40a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3066464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caa6ca56b8eef2ee38f47416d84e1a2b65bc7295efe17e4df6021499b5595cef`

```dockerfile
```

-	Layers:
	-	`sha256:f74f3d4a56b2406d053d87b74e003b254a205d55d6ec9f5649e1deb35c4f6377`  
		Last Modified: Thu, 01 Feb 2024 13:18:22 GMT  
		Size: 3.0 MB (3045446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6f49e97e96a695b97829da06cff03318f5c14b3d1d4ef8fe78c2eeca476c573`  
		Last Modified: Thu, 01 Feb 2024 13:18:22 GMT  
		Size: 21.0 KB (21018 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; s390x

```console
$ docker pull memcached@sha256:1d9c5334c3a326967ffeb2b21b3ba4c4988192008cda85f1f976eac33903647d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35722133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7be50d49c39d71ec665a9e23266dbc3d552da5999b72f07ec7930d3a429191bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 10 Jan 2024 01:54:10 GMT
ADD file:65dbcebb09bfa0253ba47edc09622e132326164df51df5626ae3a06a0e5d179b in / 
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a26174f024d942f0adb6db11b3ae9df606c112928e1b40e24779a0fdab24cb41`  
		Last Modified: Thu, 11 Jan 2024 01:50:51 GMT  
		Size: 27.5 MB (27491850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88a75131d890735cbd441c97a4614bf6921c70516a44035e94ab2602abda823`  
		Last Modified: Fri, 12 Jan 2024 10:23:47 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9824164d5b254bac6f47c1f9f1f789ee242bdb78d2af76ae97ec7bb6ba3374bc`  
		Last Modified: Fri, 12 Jan 2024 10:23:47 GMT  
		Size: 2.2 MB (2152470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f5ab339bbef10007f610f6cc66b17e089a2c025365bd222621f7672ed423c8d`  
		Last Modified: Fri, 12 Jan 2024 10:23:47 GMT  
		Size: 6.1 MB (6076302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd554521a38eea81119557ba2eb11baa41a041aefeca8a53e27d07764285b22`  
		Last Modified: Fri, 12 Jan 2024 10:23:47 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2d254b5efbc48dcf49595e413d313512a9a93d1a03d46d47477594804f4117`  
		Last Modified: Fri, 12 Jan 2024 10:23:48 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:b2f25d0a110fe0eefd9665ee1cf97cda670515da5428ec34cb95ba76d7203911
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3067351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc68ff9eb0c6a60d51fc8287b9b821f85ba68aed2a2055f7d89135b7ac09c031`

```dockerfile
```

-	Layers:
	-	`sha256:7b268d71137f2e13413f8ec3c0541f386472902b0bf8f9f39a99a79e50c98b8c`  
		Last Modified: Fri, 12 Jan 2024 10:23:47 GMT  
		Size: 3.0 MB (3046401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8677225d69190d57c1ae3c6d9a998072f6e67cdf398c58457065b1c68a7153b6`  
		Last Modified: Fri, 12 Jan 2024 10:23:47 GMT  
		Size: 20.9 KB (20950 bytes)  
		MIME: application/vnd.in-toto+json
