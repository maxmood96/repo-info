## `memcached:1-bookworm`

```console
$ docker pull memcached@sha256:9232f48174d2e94252ef10af60ed5482a1fd81293acd6079b7a221c856e5b24c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
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

### `memcached:1-bookworm` - linux; amd64

```console
$ docker pull memcached@sha256:eb8b1feb1315c6c2fb45a5f56f8071248bc3920795bd6b301a3b55e125e9c92c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38788420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eaf219d4325581d3712fc18a4ad5580e9b86593ebafab93f8140acdf84508d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Feb 2024 07:54:11 GMT
ADD file:b86ae1c7ca3586d8feedcd9ff1b2b1e8ab872caf6587618f1da689045a5d7ae4 in / 
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8a1e25ce7c4f75e372e9884f8f7b1bedcfe4a7a7d452eb4b0a1c7477c9a90345`  
		Last Modified: Tue, 12 Mar 2024 01:25:41 GMT  
		Size: 29.1 MB (29124181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4e5651d3b18aeb31a747d494ffd476c9a3fa59a267e7fb185a6be532c4a448`  
		Last Modified: Tue, 12 Mar 2024 01:58:18 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9c18827670ea3f4403adfb7f79e1aa7e93ffcd344ea2218f63d6c9c86665aac`  
		Last Modified: Tue, 12 Mar 2024 01:58:18 GMT  
		Size: 2.5 MB (2488478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b2169ebed513f01a5b38c8647b5472020f26e9dbfd53b7d4e8f69123b004bd5`  
		Last Modified: Tue, 12 Mar 2024 01:58:18 GMT  
		Size: 7.2 MB (7174246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63cc61f1f6b38f9f92da2e783bfb4a3cf2d8769414c6649198bfe01d6c76fea6`  
		Last Modified: Tue, 12 Mar 2024 01:58:18 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df362dd3d3dfa6ff85dcd8a5751c3770f4a9641ac917995bc897e119c6eebade`  
		Last Modified: Tue, 12 Mar 2024 01:58:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:bfda8530f9686f03660c1fd2dc2116b02efd7c87436b52519f74319675f6a1bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3536051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:807428c53478a8dea9f2a1744156b055365c0424a9b3763dccc8a8b2db7f6497`

```dockerfile
```

-	Layers:
	-	`sha256:b8ca29d6a98c867384f22b29563e4fc40ae192805537e71dd09bccd09cf78558`  
		Last Modified: Tue, 12 Mar 2024 01:58:18 GMT  
		Size: 3.5 MB (3514934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d1fe8739195306489684020faf7c666087c282955f6ae7340bd0939821260fd`  
		Last Modified: Tue, 12 Mar 2024 01:58:18 GMT  
		Size: 21.1 KB (21117 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:97526d95a8e636880ff486c5ca3a41e7c05e34ffc33d9764ec8c557588c8a311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34810886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44f0331d4d71c4d3d6f2d93b6073316fec4b08d475dbea0db96ee4cd3c5cca93`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Feb 2024 07:54:11 GMT
ADD file:b1bd2ec7dd2a8894ea7b5837afba4e15ba798f4809586f0ac1b8855bd0032651 in / 
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:64806d9455193063a6bd4aebf47380e94fad8313f6ad1b5d831882c453f43261`  
		Last Modified: Tue, 12 Mar 2024 00:51:39 GMT  
		Size: 26.9 MB (26884021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e32a50f75b9d40c50ce7692a0631af44e30f327e696aa5b28831455123c0d1`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a78498071cf34c7c6bcb0da9274a1a38c73fbb294d613cfac9c0100e903977`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 2.1 MB (2089476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a5b58a66453c0fffc63e703b2f567ded5a4c7d4201d052875f7c57ac03487d`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 5.8 MB (5835877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eea2c7e10f649b41e653958ee3e704680233d441f8e34b3b7ef69f85cfcc2b9`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:932489b471f2cd1fcedf275075c32805b88530e65e8c309fbea1c872145766f6`  
		Last Modified: Tue, 12 Mar 2024 15:00:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:f5ae50973e7b24315f9e4f24a2005db27a3777c108329b83eac47743c89b3a54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3506304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed9f38295119bf1cb94aa0766bae3a4b7f92c5b45dbb3f4318b91512cd3439af`

```dockerfile
```

-	Layers:
	-	`sha256:2304579d3145fc8d11406653c5a1aac0d36e928b2b7473acbc095c300e97ea1a`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 3.5 MB (3485214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b012268ed16d3d5997dc117014ee647292b0d6a75252269c1b9cd0696f30046`  
		Last Modified: Tue, 12 Mar 2024 15:00:56 GMT  
		Size: 21.1 KB (21090 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:8234a3b58f7d6ba5c37a4c024303e1c2091863e16c2055c456173f7f1fd445ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37686508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:097b1868fbeb54c0c59f0518cba1c00eca85a42d8d26afb42460ea33bcb9a087`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Feb 2024 07:54:11 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b586b7b1730c3541ccded1f78b4ceae75bebc2adce73c0107844f0b826c0834b`  
		Last Modified: Tue, 12 Mar 2024 22:16:19 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0dd730cf897622268168cb7cd6c1d29096e4e1ecafe079752761909b98e644`  
		Last Modified: Tue, 12 Mar 2024 22:16:20 GMT  
		Size: 2.3 MB (2346193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa1f8bdb6c41c2e0eb7b5e70265de70083d67b3edf743e8fd8e00c171613578`  
		Last Modified: Tue, 12 Mar 2024 22:16:19 GMT  
		Size: 6.2 MB (6182365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fdc2882c9a1ce343043a1b1c104a02bdb5b11fe482a35398bd2d8af92f8244e`  
		Last Modified: Tue, 12 Mar 2024 22:16:19 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e7bf20027a3bc3dbcfafad5a8f11f269a23aca6150bbd439f2373bc118a5b57`  
		Last Modified: Tue, 12 Mar 2024 22:16:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:cd312a8d8491ac7d6cdfa4556238cbacf661668397c81a509826de8ab7d7e5fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3507065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cf41544feacc92a84c983de1e92919c4a00674d5621190a26fe39717845e04a`

```dockerfile
```

-	Layers:
	-	`sha256:849ac4e0efd4d5de555a1e21523f5adfa5bb50fb8497d8dbdb51db8b80cdd14b`  
		Last Modified: Tue, 12 Mar 2024 22:16:19 GMT  
		Size: 3.5 MB (3486097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c067d1f27643533ea5a8e27826536bedb9fba8b6afad95e769e622066d349edd`  
		Last Modified: Tue, 12 Mar 2024 22:16:19 GMT  
		Size: 21.0 KB (20968 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:90de6f9655772d484ab74caffd6c853d7b210aaa56a91427002ef3c2db8ccbcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39271146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4726669b71af511573ec6d1792a6b69ebd9ed2003cfb61713b4fdaffc673ed7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Feb 2024 07:54:11 GMT
ADD file:88f04d79dc9f1691544c636ff52d6744a2ff68d504793ea8034b797d0bfc6fd3 in / 
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:576af7ffb10b3f3b8d5523e6b91da8667eb39393cdfd50fb26dfc178e504ba70`  
		Last Modified: Tue, 12 Mar 2024 01:02:43 GMT  
		Size: 30.1 MB (30141873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64bcfef6653dd3b44ed28c65a61556eb6b0961ee00465593211de83202a1c75`  
		Last Modified: Tue, 12 Mar 2024 01:58:29 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf03250eea5d9f414cb6ffcf3e378ea06608ebb699bcd47e75c80bc6904d037`  
		Last Modified: Tue, 12 Mar 2024 01:58:29 GMT  
		Size: 2.5 MB (2492631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbbdb4afa76af434da5666d042efcd7290f9d3266cec48c029ba208ead47324`  
		Last Modified: Tue, 12 Mar 2024 01:58:29 GMT  
		Size: 6.6 MB (6635128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72d413e626334ca90311c2d83e5f6613369a186c8c82e86651f34d9f84047f9`  
		Last Modified: Tue, 12 Mar 2024 01:58:29 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf37bc080f6d87be39e31acfe79cdabdc20259d73e116225dbd7ab55cf329e5`  
		Last Modified: Tue, 12 Mar 2024 01:58:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:fda4a9ff0495ce58d6081ee9ad4980745b476f052e43fd62ea9f00f6201b4c16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3529875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f0d0ee94b326b4504dba6aa986d9c3b6ff5f90db66a891bbc033a78020628f`

```dockerfile
```

-	Layers:
	-	`sha256:c319fd614b67b18c6e4538fdc0872ad8501213cbbc39c1d7d12bdd69d558d83b`  
		Last Modified: Tue, 12 Mar 2024 01:58:29 GMT  
		Size: 3.5 MB (3508813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0755f69004f96bda020355a85879459f0723681fdc85e6feba2a7a17c1c5b05`  
		Last Modified: Tue, 12 Mar 2024 01:58:29 GMT  
		Size: 21.1 KB (21062 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:b3f5dfdfb6a83e76f4a99f1633d38d6e068e7e432904861300d2187a36b0627f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37562648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e95ccd48050a17ba18c55d351b2a4b101172e5a24ac929e9558cc10fc39c9e52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Feb 2024 07:54:11 GMT
ADD file:c03c59e261bb08f39e6a97df2fd4b82f1e11b49a62d1859a8f8efac680b80a88 in / 
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:aad79459a0f767fcded51c9547150a1cfd96638972389ab8621b5f3eb4a9c280`  
		Last Modified: Tue, 12 Mar 2024 01:17:09 GMT  
		Size: 29.1 MB (29119205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6cc7756610dcfcc0b14294a56a615e45e9e3d3a4459ae8a4c4ef534fbcdce01`  
		Last Modified: Wed, 13 Mar 2024 02:41:00 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:817fea43c2ab940b7c83fba15c24608a69f48ba981fdfd8ec70072fabb05af9b`  
		Last Modified: Wed, 13 Mar 2024 02:41:01 GMT  
		Size: 1.9 MB (1937661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b0133779e6ba0d7a06c0b169d0105df3d95a76ef4fd4c1bbdf86550bae17546`  
		Last Modified: Wed, 13 Mar 2024 02:41:01 GMT  
		Size: 6.5 MB (6504263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff70f27c6a52e1428abf53acb6be63a841380a79c37aa700c0e203d36a311c25`  
		Last Modified: Wed, 13 Mar 2024 02:41:00 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a09c5efbfb833f7e9fd844521a96020f57201e7164224f178411fb88e7cd85e3`  
		Last Modified: Wed, 13 Mar 2024 02:41:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:362245922a3b8b8f3d41a616987192022e4c8018e09d90f60d79c9bd7a76d596
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4d98c32b75c2dc503417f1c21a8ab67bcdcb68a438359a8ed39e8f835fc5bf1`

```dockerfile
```

-	Layers:
	-	`sha256:ec414e0f52b7e1247b68cbc259604b48c191abaddf0bcccd9416cc74edc34b3c`  
		Last Modified: Wed, 13 Mar 2024 02:41:00 GMT  
		Size: 20.8 KB (20837 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:4c3db32aa1a397cf2a03078efa95429139072b980ab1cfe1d38a3fc03e16b21b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.0 MB (43006041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6ea28ef1fe375457227b59ed4cffadfe2eb8c198795094bf26e6233bd556c8d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Feb 2024 07:54:11 GMT
ADD file:9273ef56d086dbc93b46b7e8ae424eb04096fb00c693dd6cda1f48346290d4d5 in / 
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c28cd0e276dcdeb4d44f5cc5bb958610750ff902a081b668e3863c2f38eef054`  
		Last Modified: Tue, 12 Mar 2024 00:38:06 GMT  
		Size: 33.1 MB (33119023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62aa36b84dc23bc5eecf52bd0d09534dcc186ab27089192c7aed8210f610e32`  
		Last Modified: Wed, 13 Mar 2024 02:14:26 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec1785cd98038ba62eb16a4aacec38cdbb91c26f98360aafb2ed1017cda3df8`  
		Last Modified: Wed, 13 Mar 2024 02:14:27 GMT  
		Size: 2.7 MB (2698364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c5105d8a1d382e8083f62216ad1a3ac3ed9e0dab0a2cd5110eb1afa516b084b`  
		Last Modified: Wed, 13 Mar 2024 02:14:27 GMT  
		Size: 7.2 MB (7187142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356eaa328e166dd1628acf5a67acf74c032ae2b79667868199736be62871fcc9`  
		Last Modified: Wed, 13 Mar 2024 02:14:27 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936d8dbc2ebbedc4ae8dc525f7a6ed2c953784d75251955a347e5cb1eab83a22`  
		Last Modified: Wed, 13 Mar 2024 02:14:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:7ba7fc566a7ca1cc4ee19a4562d3c8ff3cbd5c66504843364b286c16a51c673a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3521676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e456fccef08393cbfaa927989c957a984aca49d5b68aff7e43a60bebf063443e`

```dockerfile
```

-	Layers:
	-	`sha256:40dd29e81bcfdcdc7a12cb2843f9bc037c7633d5502e7d49aeab7f1a38b351d1`  
		Last Modified: Wed, 13 Mar 2024 02:14:27 GMT  
		Size: 3.5 MB (3500658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1acb5997eff88a90491a6c619d8236c97c1febf8bf3b8fce15b91660a29910df`  
		Last Modified: Wed, 13 Mar 2024 02:14:26 GMT  
		Size: 21.0 KB (21018 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:52a995e0a683561200ebb4b20710893bf0d3a1461398f83dc25814332788db63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35719944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cb244b1909115480962c160cf49e50594cf6621dac63f8a8f367bec16b99994`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Feb 2024 07:54:11 GMT
ADD file:80ab985d4871ca6a72156bedfe1038e6b1a89591fc2fd86c4ef778d293223aff in / 
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_VERSION=1.6.24
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.24.tar.gz
# Wed, 28 Feb 2024 07:54:11 GMT
ENV MEMCACHED_SHA1=ee5760180a59520794b046b3fe38b923f8a6ad28
# Wed, 28 Feb 2024 07:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 07:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 07:54:11 GMT
USER memcache
# Wed, 28 Feb 2024 07:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Feb 2024 07:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9cada496cd2b8a88571bf23d513e7fce34888d13321fcf23c6613bffe4c37297`  
		Last Modified: Tue, 12 Mar 2024 01:21:14 GMT  
		Size: 27.5 MB (27488684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce72c52ade5b417b11c394225062ef24f5c05addd82d146058026a8c2f9d21d7`  
		Last Modified: Wed, 13 Mar 2024 16:11:45 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb0efc0aafbf2ddf0ff2695e11c2a2e97e3bdcf9cbb2b5c1d95908bfa1e46f8`  
		Last Modified: Wed, 13 Mar 2024 16:11:45 GMT  
		Size: 2.2 MB (2152651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7de114a91ade9f40fc7afef12df65a695ad9b7052bfc65d5b6fdab8aa38e5c5`  
		Last Modified: Wed, 13 Mar 2024 16:11:45 GMT  
		Size: 6.1 MB (6077094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48661e5e272fe1fcbda39e5860569626207dff60ba1ff66b536296a4a2cf287e`  
		Last Modified: Wed, 13 Mar 2024 16:11:45 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:287c17d5b28ef687f677b4b3fafc3ab71b96ad9008d1903c25b42053cad7a877`  
		Last Modified: Wed, 13 Mar 2024 16:11:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:77e5177914fceef8561d4bca602eeaa239baf81bba003b3a8387f265767dd8db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3524153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:525c9355951501cb07f5a47473fb6b966c78a6b9fbfab43642dd226411ce89a8`

```dockerfile
```

-	Layers:
	-	`sha256:eb2c02faf4e7317079009cea67ffbb88bcbd3ba820d2f88dcf283589f9523c3d`  
		Last Modified: Wed, 13 Mar 2024 16:11:45 GMT  
		Size: 3.5 MB (3503203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1b605c50c74252ff551dbebfabda3573fb02e0131bae6841fa9123a3016c3be`  
		Last Modified: Wed, 13 Mar 2024 16:11:45 GMT  
		Size: 20.9 KB (20950 bytes)  
		MIME: application/vnd.in-toto+json
