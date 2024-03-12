## `memcached:1-bookworm`

```console
$ docker pull memcached@sha256:9186bcea714c539cf8901c4bcef6061b2fac738cacbfa6c91977ceb283c6d402
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
$ docker pull memcached@sha256:00d7905ca914c42a44c7d28114d1105ba67ef54deb13032d51c92c754f99d6ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34810824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2417706d40df90366fb3366397b260b7efa241d7870815ac7a634459e1116380`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 13 Feb 2024 01:08:21 GMT
ADD file:468c16fc087244db1784e8f07bec3a1a417cd85172afa7dc960c2d1ecd1f37bc in / 
# Tue, 13 Feb 2024 01:08:21 GMT
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
	-	`sha256:e0d489e60efeee042d73afc4d45ad77014188c0ac8941f9ba5f15760d2288c3a`  
		Last Modified: Tue, 13 Feb 2024 01:13:30 GMT  
		Size: 26.9 MB (26883902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e5bb052af08baa3f1cc9c7c3a12dacb29c6782bf02f389a8a0e84c01bc76501`  
		Last Modified: Tue, 13 Feb 2024 18:07:36 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd523b949fb7caf462ef2ebe8c93ba4ec7b7077faaec5cde88ada68b24227a8`  
		Last Modified: Tue, 13 Feb 2024 18:07:36 GMT  
		Size: 2.1 MB (2089473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:655850c15be7ab7ade23d99ea122c70aa8b731a0ba7808de616d2b82d21e6f00`  
		Last Modified: Wed, 28 Feb 2024 21:52:15 GMT  
		Size: 5.8 MB (5835937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ddf7b83faff3db64156f539558de0f52a79c43ce3fa7de78a553e3ebe22e71f`  
		Last Modified: Wed, 28 Feb 2024 21:52:14 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a46846c110fed52c191dcd66537f05374bb3b8e61aee7e608a1774350db355`  
		Last Modified: Wed, 28 Feb 2024 21:52:14 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:9636887e4acc7b63e182564c2e0fd4c593cc7908802a1b75e242b34fa029533b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3506305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f8c3d46b4b7311203dac8333a5f11248fc09cd0a14c1146cef24ffc6f605827`

```dockerfile
```

-	Layers:
	-	`sha256:c5b03e1f7629766e20e5c9fd3f3f12426dd131d66ef1ce4c45191752c333b5a1`  
		Last Modified: Wed, 28 Feb 2024 21:52:14 GMT  
		Size: 3.5 MB (3485214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad5c024791ae7ad04c83a7a68c009dba7de1829795c48758b9b84e2858f91def`  
		Last Modified: Wed, 28 Feb 2024 21:52:14 GMT  
		Size: 21.1 KB (21091 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:f0ca9642df4558917dcb1a89b2993d09c9920f100125d63f71ea6fd13f259f5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37686510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41cdb306d68198edcc7795e48820c1be1b3deefe360c6d10fd34044f150b9bb9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:20 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Tue, 13 Feb 2024 00:41:20 GMT
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
	-	`sha256:f546e941f15b76df3d982d56985432b05bc065e3923fb35be25a4d33d5c0f911`  
		Last Modified: Tue, 13 Feb 2024 00:44:54 GMT  
		Size: 29.2 MB (29156363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22074550eafb454e17d2939bc2d65011ccb55368a89e5c1572a06ddee7d14781`  
		Last Modified: Wed, 14 Feb 2024 00:46:02 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0634e036e15957c161657754d81209edc13b7b54ba120ca37699f1abdcc8f253`  
		Last Modified: Wed, 14 Feb 2024 00:46:02 GMT  
		Size: 2.3 MB (2346185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c8f4eacd8665cc7099c6304b83e34965675215de895df23cc4f18fec64da08`  
		Last Modified: Wed, 28 Feb 2024 21:51:41 GMT  
		Size: 6.2 MB (6182452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5daa76d71d100de2919329f7c450ed91caa8d20c667fda494d0efb7aeb305654`  
		Last Modified: Wed, 28 Feb 2024 21:51:40 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2dec88e095eae4e21422ddf0f6fe4b2da01c2f9c6852cbded300df415a61b01`  
		Last Modified: Wed, 28 Feb 2024 21:51:40 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:3c42dcd58bf6766747be8aa16d2e4119023735a6abb31de4196ce98b4d8a2a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3507065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a90a33aaff3fbdf0576b92c6a8d6a7d0d151a82db9d981fa6ba54c825d50e1d`

```dockerfile
```

-	Layers:
	-	`sha256:4efe66f4e7a1e38059e074b02b537f6ff0d769a89e5511b6681ce6f6a85c916c`  
		Last Modified: Wed, 28 Feb 2024 21:51:41 GMT  
		Size: 3.5 MB (3486097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd3258cf1a6d6ab88ff7beb5359a020823a9b7654fec52d322075bdbecf71da1`  
		Last Modified: Wed, 28 Feb 2024 21:51:40 GMT  
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
$ docker pull memcached@sha256:97e6d099b44a4d06863682c4f0b865bbbd6aad68e517e07f810ca80643a13006
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37562543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b73271e47e8116b8839edbb2758243dceae1a6f98436f0a62c0bb499a0a0bc9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 13 Feb 2024 02:04:14 GMT
ADD file:7b0bbeed7888e49f58bdffd816596bc88b87bd4a3761c5a2590f3123c077899b in / 
# Tue, 13 Feb 2024 02:04:18 GMT
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
	-	`sha256:78ede1ea2c0b185708583060a40bd2aeddee7b533566b4df729e98e5e5de458b`  
		Last Modified: Tue, 13 Feb 2024 02:15:10 GMT  
		Size: 29.1 MB (29119092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f37b0f90bac773aa84b74a3f97fdfc6ac8f70ad93a3c9223d8bca0227643c3`  
		Last Modified: Wed, 28 Feb 2024 21:56:49 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ed8a5ba75c84cd350f53e6640c5e8f2914ec1514ba9d396d0c4cfeeeab0535`  
		Last Modified: Wed, 28 Feb 2024 21:56:50 GMT  
		Size: 1.9 MB (1937647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da0478cb8cf35b02627d1e2decfe012f63689dfe58dee90ede3a049282da6a3`  
		Last Modified: Wed, 28 Feb 2024 21:56:50 GMT  
		Size: 6.5 MB (6504288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32ba334ea25bd80c79925e85e915647c1f1b72d0f7845698bfc2cecc64fbfe0`  
		Last Modified: Wed, 28 Feb 2024 21:56:50 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1580436aec4d325ca8c65b36bb09cb6d36224e2665693c79161bdf4bb17020a9`  
		Last Modified: Wed, 28 Feb 2024 21:56:50 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:4c4a7c399cf508d32f60fc89aab7570abf1d554fcc56ee4a2c3f3ba82337f203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a2e28419a09cca31a53ab8a0fb0696c5f8e2fb0226f4ca72c89c9b187b6796f`

```dockerfile
```

-	Layers:
	-	`sha256:a6b5bb434cac40b0cceb8246d1a5426f9b7133b24c65cb050007a16e639d60c2`  
		Last Modified: Wed, 28 Feb 2024 21:56:49 GMT  
		Size: 20.8 KB (20837 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:4cfc302cba628510f1d2624a83be502f9251a86b148cba4d0158acc657365f1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.0 MB (43006015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:046eb87090d6cd0642de51444d330ab5c524b13c37dca1ee170dc4e694c8df28`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:03 GMT
ADD file:b65bdf3d9277efbf6bbf8bf0121f92bdcd342ed0c4f49f1cee3b91adafacd76c in / 
# Tue, 13 Feb 2024 00:39:05 GMT
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
	-	`sha256:b1cce6d9947985e4270ac998aa258401bc5deca94d504040a14f9f3c47258d68`  
		Last Modified: Tue, 13 Feb 2024 00:43:56 GMT  
		Size: 33.1 MB (33118908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25caa81f2d0da1d846a121d659704c94c921a21f08938e476c49795b8007c7c3`  
		Last Modified: Tue, 13 Feb 2024 22:15:19 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a84e251667fbe9b03e6203397f3abaa99c83486b5a718d98b7083a7bfd386c1`  
		Last Modified: Tue, 13 Feb 2024 22:15:19 GMT  
		Size: 2.7 MB (2698377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de17e00c55ca105c3066c8071fd9227b284f202fa8ed41893715b82e2f47b91`  
		Last Modified: Wed, 28 Feb 2024 22:14:01 GMT  
		Size: 7.2 MB (7187216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b374f3e29aebf5f52b4e78803b02bc249cf99311b1be8d49db3f19c530aca82a`  
		Last Modified: Wed, 28 Feb 2024 22:14:01 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:643af4261406fac5276144dd99a1387d2768e387440f1353796347e93bf81fa7`  
		Last Modified: Wed, 28 Feb 2024 22:14:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:d8718d6327b11385d18dd2f64e67ffb6ec5cc0e5798086ce17600938d81d9866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3521675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d522252422bb1612a888765f3184cc9cd640e2949b4fe6429fbfb5f4a5c9405d`

```dockerfile
```

-	Layers:
	-	`sha256:fba15fd2f1944306934f0776cb34724faa7a7b89832cd7784abb20afe02e9b82`  
		Last Modified: Wed, 28 Feb 2024 22:14:01 GMT  
		Size: 3.5 MB (3500658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:275a4ce2c08488b6bd8fb4dd5e962e56aaebd5033acc023691da34965ec3d725`  
		Last Modified: Wed, 28 Feb 2024 22:14:00 GMT  
		Size: 21.0 KB (21017 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:5fe5e61ec110840bc00bb17fb69a8d22872d81230256320e33138ab250ec85b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35719906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0962b6fe88e7428a9aa14beab6b72f25025b38e60e059423497f4873850350f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 13 Feb 2024 01:02:37 GMT
ADD file:2dc5fd465b3cc728990229e12489d68faf8a93e6f574cacdca11cc9bf31f511d in / 
# Tue, 13 Feb 2024 01:02:39 GMT
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
	-	`sha256:e55f0b78e9a121a048a72242f0aec2a221466b10bedb873c07b73e4b99f873cb`  
		Last Modified: Tue, 13 Feb 2024 01:30:22 GMT  
		Size: 27.5 MB (27488587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0748a343755438517f5647d8675e5f835df79c46d674ad680568153f77e4e6a`  
		Last Modified: Thu, 15 Feb 2024 05:21:05 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd18dfa7f1fc6e57e11be5145d32fd00f1ff50b52bbb3dbc15f293e9ed0a5597`  
		Last Modified: Thu, 15 Feb 2024 05:21:05 GMT  
		Size: 2.2 MB (2152661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecd95b872c88a45f688f57e301d2c8b3fc7f04840265f6a7fb2a4a752a184ab`  
		Last Modified: Wed, 28 Feb 2024 21:57:03 GMT  
		Size: 6.1 MB (6077146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9a815c91b19b7601266298dd59f09ac7aa82cce744ebac330b4467f5ad34e6`  
		Last Modified: Wed, 28 Feb 2024 21:57:03 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b671bec8dd3a2747e69390439e7f2cee30152c4f95e4ef09647f7485656884`  
		Last Modified: Wed, 28 Feb 2024 21:57:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:69f0a93a5138984bc7235e822f9772cafc96fb4a2289da907dbe0f77dd54b1b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3524153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be28ed1a0aeaf1526fa9d7c803a42e51a551c1c3ff6098a4115fc5c9419b2aa4`

```dockerfile
```

-	Layers:
	-	`sha256:3e67191d814845546a16918d4b01e78b07ee0548e6d263302718284ff2fc79be`  
		Last Modified: Wed, 28 Feb 2024 21:57:03 GMT  
		Size: 3.5 MB (3503203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:640874506e23a600c327b24761b8c97ed77c72c54fbadf9d9a5991556227dcc3`  
		Last Modified: Wed, 28 Feb 2024 21:57:03 GMT  
		Size: 20.9 KB (20950 bytes)  
		MIME: application/vnd.in-toto+json
