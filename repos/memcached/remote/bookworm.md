## `memcached:bookworm`

```console
$ docker pull memcached@sha256:09eaba8e0b136af2f1d8a4985b4fda74ce2793f95ea66d82fbe5769c05b42ea3
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

### `memcached:bookworm` - linux; amd64

```console
$ docker pull memcached@sha256:405390d9c38a0e3d59f34088c2265a710da10e5e9f3cdeb4fb5264c829509aa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32894836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10895cbae2201dbd8d84c3c9047f79424e9ed1ccbe25884d1b4d795d0ac6d5fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4129f47668200cd75e7d6aa28137d019d65b34d6144533d4c61d02002786fc2`  
		Last Modified: Wed, 24 Apr 2024 04:58:30 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:744ca95230b13b1e9e5f98589fd877fd8b41c6b22acc7b318317b4050f37aa7a`  
		Last Modified: Wed, 24 Apr 2024 04:58:31 GMT  
		Size: 2.5 MB (2488517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae6b4d4bfc0b415f2f71dfa80f987ddad9de59be9b7a7886ad9bdaef0c95a4e`  
		Last Modified: Wed, 24 Apr 2024 04:58:31 GMT  
		Size: 1.3 MB (1254327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc7f043e733e1d442a2a781e47b23ec6a0854f6adcb9ffde51a78d60e5804e7`  
		Last Modified: Wed, 24 Apr 2024 04:58:30 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f4b8dbb80f3c2046731086fcefec9d87cfe0d75c6257b158f2380571fee358`  
		Last Modified: Wed, 24 Apr 2024 04:58:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:1d27dea50bc28fa19c0797272c6cb9429dbb42c7cf69999a6f0e22886b0adabe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab3f6921bc3d539a2759e6a6332c2ed1a006f38d9c41941210727656069e6a9d`

```dockerfile
```

-	Layers:
	-	`sha256:82615c3da645e41f3882b16c3f194da79f8a9109b587815e13233f8955bf4791`  
		Last Modified: Wed, 24 Apr 2024 04:58:31 GMT  
		Size: 2.3 MB (2261261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8730bf8939b3c17c94865c382c10776ba63e0184d1a7efadac08eb2b9026411`  
		Last Modified: Wed, 24 Apr 2024 04:58:31 GMT  
		Size: 21.1 KB (21146 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:0b7ef9caf0969bde35ebffe75de743d43f067c4d21f726779376f350060852a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30235680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:773f6729bbdb0cf400fd54945dad86de0161757faeb1222ca5c619b39e8906b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:0140ab9be4171f94aae33901f189ffd8822ce6da4a052798883fd66d03b79be9 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2c9444d4d8a989f4536a8afd8b41a3461ede5b15d490d87c3369b051095d7ae3`  
		Last Modified: Wed, 24 Apr 2024 03:56:28 GMT  
		Size: 26.9 MB (26910029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb7ab01eefadf50cda1a69620f8ebbdbe564ae5e4948d441a046e73beba10f5`  
		Last Modified: Wed, 24 Apr 2024 17:23:50 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f80391c4dfe0b57b2703f5bbeee5f3c06f1e97caa317551b020ed7e290a6bf`  
		Last Modified: Wed, 24 Apr 2024 17:23:50 GMT  
		Size: 2.1 MB (2089520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f90038121a2dcf34821ab7667d4adae00eae271a0f250ed8d539782350f9460`  
		Last Modified: Wed, 24 Apr 2024 17:23:50 GMT  
		Size: 1.2 MB (1234615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b80f018df33ad7536224f92fab6be93311c3112624802850f074c2d6cdbcc558`  
		Last Modified: Wed, 24 Apr 2024 17:23:50 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428c8c9af637766c90123d1ec1fa1a358d8ecfc5f324a9d72fe0c901cf46c179`  
		Last Modified: Wed, 24 Apr 2024 17:23:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:09daecd129479a515f4ea8e53fff1dac5ff8b1f9dd74b4abe887233bfc9ffeec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2285669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cb63ca854d1d2f378329e965e5a5c64a0f013e70f9a7ca89f1ee082def6bf13`

```dockerfile
```

-	Layers:
	-	`sha256:0e5d982b6df17f7c0f32468611d589bebfb5da853622a8c7ba321cdc6e05a18f`  
		Last Modified: Wed, 24 Apr 2024 17:23:50 GMT  
		Size: 2.3 MB (2264549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eab299b375d05024ba5f4838c9161c837b763500e307541a0cfa44d07d31e4fe`  
		Last Modified: Wed, 24 Apr 2024 17:23:50 GMT  
		Size: 21.1 KB (21120 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:d848ec0e7fd016c877f5c7b2441741e363f47b4657f611e29260174fb7f5906f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32779502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30a9755c487d28faa9cc5a30028058039b5bf30dc68f57dba813a1c638dfdf5f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8526410ee80ca263cfaba3c1ca4f8c2ff3102fb0ae99ad123d140deb09113e7c`  
		Last Modified: Thu, 25 Apr 2024 07:35:13 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77abff488dd54b291eee02724fbe326c137dd4d1fcce1b67d0cf6e9b6b334680`  
		Last Modified: Thu, 25 Apr 2024 07:35:14 GMT  
		Size: 2.3 MB (2346225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be2ca094ac0ffc80c9caeba3e8ba06efead9889731d49ff3e6bcb3be212b4af`  
		Last Modified: Thu, 25 Apr 2024 07:35:13 GMT  
		Size: 1.3 MB (1251829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a9a249ff9fc40523b8ff9d36749c484c9ffe686e373ec7f4c92c9c2c7a883b`  
		Last Modified: Thu, 25 Apr 2024 07:35:13 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d249287eb80fede3bb001966299d7f04a136ad4068c042fc4ef9e4cd4b076e65`  
		Last Modified: Thu, 25 Apr 2024 07:35:14 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:2c23a6c97c218cbfb28d8ef9b2d0e2e48933e30f55856a69d6074c2f3e96d17c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:241b569b533dfc355f1dfb00b1bc2e6cb2978e8e5212740dfa27bff516b9f878`

```dockerfile
```

-	Layers:
	-	`sha256:856b94b03a6cf59ebf3de68ac6f9bf5c80cae0e0965529122eae83bfd64d4397`  
		Last Modified: Thu, 25 Apr 2024 07:35:13 GMT  
		Size: 2.3 MB (2261490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:954c5b306a204640106bc830ca97d3e26226ba00914f18e1c6d44493b0550543`  
		Last Modified: Thu, 25 Apr 2024 07:35:13 GMT  
		Size: 21.0 KB (20997 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; 386

```console
$ docker pull memcached@sha256:46b1135239ef87a25cfe9bbecfff7101e18652b28acb62a79b2ae947d602f115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33912878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b2df86a1f18ed03d43409276aefac7f6d5474caa1d0f9624832a268284955c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:104afc54fe81c235eceb94cef0c07d1e8032f01fb7c450dffd4e251671d445ba in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:af3150ac61338e2036c167b18f712ab80fd82f6b215de3e4732cb6defbd8bcb2`  
		Last Modified: Wed, 24 Apr 2024 03:43:36 GMT  
		Size: 30.2 MB (30163183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9170912a46039a4bf18c888e6b3b4d3d94512edd688860d581e585e54943b864`  
		Last Modified: Wed, 24 Apr 2024 04:58:35 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d576ee5b91b4ff82a80818993e7f3f8d0e442b6179a5876357d674fde185adeb`  
		Last Modified: Wed, 24 Apr 2024 04:58:35 GMT  
		Size: 2.5 MB (2492685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4916d6e94a60cc27afe44a26252965fb6dd21aec05e70778c874c2daea0ddcd6`  
		Last Modified: Wed, 24 Apr 2024 04:58:35 GMT  
		Size: 1.3 MB (1255494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:602e9186230f92e4d7169d2bcee14830f00112c296ae71af94fb871cf6201fdf`  
		Last Modified: Wed, 24 Apr 2024 04:58:35 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:991cbe7461637496b4d79cf6bf30b5a7af5c77a726b75296270f1a32e25708cd`  
		Last Modified: Wed, 24 Apr 2024 04:58:36 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:a9db8c622a654fddad84431680831ba17cdc6811d6421a7689cc4474c625e651
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2279450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88e36b09a88ed97ad506fa4e80ae11a7e12f15128b0f896047ed6f1ded171573`

```dockerfile
```

-	Layers:
	-	`sha256:c590417958ad379329a42ea5d922786a0b5ea5459e1dc84b237d1f93763690e1`  
		Last Modified: Wed, 24 Apr 2024 04:58:35 GMT  
		Size: 2.3 MB (2258359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2811269b7c62b3f41c63370a727b1f2ca38f02e51e20bc15f700f240aa01e490`  
		Last Modified: Wed, 24 Apr 2024 04:58:35 GMT  
		Size: 21.1 KB (21091 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:0521aebecbb12c89f89f9591316d9af4aa16b805f3737380405181d10791eb59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32334270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:295bfea4ef279164cd6fdd6d5ba3ceece5640fd56c5970fc8febab689d28b12c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:a3e63beab80160854bfc2d48f69e7c70a9542cdfaf3c5b50f1d6248a998b75ae in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:af25825be002e7bdd52bf28c2fbef5bae0ba9fcef8118e5591a874e7a70b2a62`  
		Last Modified: Wed, 24 Apr 2024 03:25:20 GMT  
		Size: 29.1 MB (29144174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eab10ab537afe3142cebeedb47aab0f0fd68a1f8a3a3a5126c399c7d0509d37`  
		Last Modified: Thu, 25 Apr 2024 00:07:40 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a494ba47330451fe35234b1e21cde0f797ca7a662bda68cfe1c291c67db32e`  
		Last Modified: Thu, 25 Apr 2024 00:07:41 GMT  
		Size: 1.9 MB (1937741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac831a90c998935d64ae677aebbc621090878a6954a72ec003c6e63cee15a1aa`  
		Last Modified: Thu, 25 Apr 2024 00:07:42 GMT  
		Size: 1.3 MB (1250836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e28c1b19277147d056a1b36137256be33a0ca07b383d9b10b41b0fe1a3ecaec`  
		Last Modified: Thu, 25 Apr 2024 00:07:41 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee8c1df57402d61e485f8308e66a58e392f66221e1f7eeaa7270ce73d2891da`  
		Last Modified: Thu, 25 Apr 2024 00:07:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:60887a1a12a49c168c614e0b0742ed2608d1269aeb9d56c4513f1b036fe59ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afe803241a2ffd1541b22f58450236eef849c63fcbc6aba3f7975de8b65489b9`

```dockerfile
```

-	Layers:
	-	`sha256:df5e9394cfce445733f007695c3314ff7b22b6bd25032cd972ca0ddcceef69d0`  
		Last Modified: Thu, 25 Apr 2024 00:07:40 GMT  
		Size: 20.9 KB (20862 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:dbf49790a58d41e51065da268024ab7608ad5d4a43fda1feccb283b6aa07cdc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37161030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe3f45fa53a786f0f2ea352a95fba6e44ff3fae576966711b6a2c2f561ef4b71`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:c7bb343c1806994c9561ecf8d3efa31be5e52ef43e2d7bfa957bafa0a7b4c586 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6638f5b33adcc7d860acf4acdb1fe172ee2c42fa259745b817b65978748c2788`  
		Last Modified: Wed, 24 Apr 2024 03:26:31 GMT  
		Size: 33.1 MB (33141201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db5a94756b0e48a0cf340b7f9d526031b4586a7abf0981edf82f3d1187f60c0`  
		Last Modified: Thu, 25 Apr 2024 03:29:48 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a35c1ffc1970ea56682aa89151aa06e03c6745a8c5d4a3f7c88263e0447ed9a`  
		Last Modified: Thu, 25 Apr 2024 03:29:48 GMT  
		Size: 2.7 MB (2698414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059df9ef4d524740ed4ada4b326517f689306ad5f4c028006cce2fb4d7a0caa9`  
		Last Modified: Thu, 25 Apr 2024 03:29:48 GMT  
		Size: 1.3 MB (1319900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eabf88f350295313ab6b674550ba3ac3359925b5384242d322cdaef28c398eb5`  
		Last Modified: Thu, 25 Apr 2024 03:29:48 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e86080ebc2f978706f6bb3a37049b74c6367a74a22506c04d170af875c2d4ed`  
		Last Modified: Thu, 25 Apr 2024 03:29:49 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:41e52b3c3230b7bd8c5314ffa30940f416940c897b90862b7f2ee4eb7aaa23fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2286679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdfe1022024097ed3bc96b490517785b7164df214645ea3b1cdfe3615128e320`

```dockerfile
```

-	Layers:
	-	`sha256:2f1213680b57369f927f30f06a44b65a89b39a2d8b98abfc86ca1f1f4c4b00e4`  
		Last Modified: Thu, 25 Apr 2024 03:29:48 GMT  
		Size: 2.3 MB (2265632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a4c13a60f5ad5d6a17dfe3153132b30a3ab3d0b428649522df9511add0ebb22`  
		Last Modified: Thu, 25 Apr 2024 03:29:48 GMT  
		Size: 21.0 KB (21047 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:8f297dcc6e8a58c5b703c7db76eedb172426c98c60f75cc7feefdc7f8bca6aac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30900246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3408130c76f8abfc35ddaefd50568612926d544e78211633ab34d3a7deeeee8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:8cb22057960ef730bf4b15ce944d70fb8050d356172942041bcdbdb9d2a3a901 in / 
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_VERSION=1.6.26
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.26.tar.gz
# Fri, 05 Apr 2024 21:52:05 GMT
ENV MEMCACHED_SHA1=03b9ea47eb9819bf0f53f48db908f45150f1072b
# Fri, 05 Apr 2024 21:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 05 Apr 2024 21:52:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:52:05 GMT
USER memcache
# Fri, 05 Apr 2024 21:52:05 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 05 Apr 2024 21:52:05 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a0ff905a311848701ed9798adb40b6da9a87d229896e7a643fe00f69142410a8`  
		Last Modified: Wed, 24 Apr 2024 03:49:17 GMT  
		Size: 27.5 MB (27512355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8887960fe4c03780d2e785808f62d3402f441b9cbe52327425bac14eb36c98a`  
		Last Modified: Thu, 25 Apr 2024 02:35:31 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b03de28877b5906fca4f93385e6f9553293581021d2d2e6d6f55d51cb57d250`  
		Last Modified: Thu, 25 Apr 2024 02:35:31 GMT  
		Size: 2.2 MB (2152656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d791341a67ab8cca0ef594fca271279c84e9c05054b079b73eb720fcc0ee8f0`  
		Last Modified: Thu, 25 Apr 2024 02:35:31 GMT  
		Size: 1.2 MB (1233719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:605a777bfbd0d9e0c08cf8e4371d4f83fffd4d961422e7feb979d2972a3a183c`  
		Last Modified: Thu, 25 Apr 2024 02:35:31 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6064b7a78e8028567a9787d525c81a4d971f1ac6249b082c54855647fcccb69a`  
		Last Modified: Thu, 25 Apr 2024 02:35:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:a9aa42482c52b8d3803b391dea18508cf31e4cd2c9252231c605c49cfbd5f351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f9fcfa76109e5a26e5cff52a7806d3c43eced1285399aea287dc77468ef95f2`

```dockerfile
```

-	Layers:
	-	`sha256:dda539cb0e51b9165c9ec4820f3de2c3317ef6b25b82b57dea63da25020945cd`  
		Last Modified: Thu, 25 Apr 2024 02:35:32 GMT  
		Size: 2.3 MB (2261082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a28af74d992870b6c1f1294fe0f545b8bb8d3a23ad450a77015ac600fd21168e`  
		Last Modified: Thu, 25 Apr 2024 02:35:31 GMT  
		Size: 21.0 KB (20978 bytes)  
		MIME: application/vnd.in-toto+json
