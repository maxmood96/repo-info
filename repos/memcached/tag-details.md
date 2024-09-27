<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `memcached`

-	[`memcached:1`](#memcached1)
-	[`memcached:1-alpine`](#memcached1-alpine)
-	[`memcached:1-alpine3.20`](#memcached1-alpine320)
-	[`memcached:1-bookworm`](#memcached1-bookworm)
-	[`memcached:1.6`](#memcached16)
-	[`memcached:1.6-alpine`](#memcached16-alpine)
-	[`memcached:1.6-alpine3.20`](#memcached16-alpine320)
-	[`memcached:1.6-bookworm`](#memcached16-bookworm)
-	[`memcached:1.6.31`](#memcached1631)
-	[`memcached:1.6.31-alpine`](#memcached1631-alpine)
-	[`memcached:1.6.31-alpine3.20`](#memcached1631-alpine320)
-	[`memcached:1.6.31-bookworm`](#memcached1631-bookworm)
-	[`memcached:alpine`](#memcachedalpine)
-	[`memcached:alpine3.20`](#memcachedalpine320)
-	[`memcached:bookworm`](#memcachedbookworm)
-	[`memcached:latest`](#memcachedlatest)

## `memcached:1`

```console
$ docker pull memcached@sha256:51cdb01f624e1eab205f978b21756cf3ef96ca33da2cd074cb47245b92e0705f
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

### `memcached:1` - linux; amd64

```console
$ docker pull memcached@sha256:a658d819b6f9ab244148f9e9994489e759ff72e12cd2a93cf0a9b0259f324743
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32878406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a783d40c8b808e6a5c1d562c8ddf24732920c2c1b7e12eadaeb76b3f1e468b32`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 07 Sep 2024 18:54:11 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d937ff39f058bf2417a4fe760827ff36b1b38be77ed6c3b27fbd80872b4106b9`  
		Last Modified: Fri, 27 Sep 2024 06:05:04 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2bb47e18c2052b1e07d1957f90f1d197fcbf398748e534e8fa54f75782b3fff`  
		Last Modified: Fri, 27 Sep 2024 06:05:04 GMT  
		Size: 2.5 MB (2491322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c618990832780ea1a130f360744ad52c95ef7485138ded320b5563aedc090b`  
		Last Modified: Fri, 27 Sep 2024 06:05:04 GMT  
		Size: 1.3 MB (1259299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f09b0e04f54ca243201f3b8f205c759c2892f6752f8e75aa84434ab4a4b330`  
		Last Modified: Fri, 27 Sep 2024 06:05:04 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2038e2b3f99ec442dfe1024270c1ad10a59fb8995060bc0a2e7a6831bbc48917`  
		Last Modified: Fri, 27 Sep 2024 06:05:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:2fbb3c4bddfc491f239cbe76e97dbd05fa35514c183e7fa4ac819cda30fd5acf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b83b1908356b5b8567c67431165b1c6e4a18a87b108cb329988349341ed52f3e`

```dockerfile
```

-	Layers:
	-	`sha256:e0ac909638f1cc11061867d2eca41aafdfd8ac0189cceb25a5aa9c4ff9c7f0fc`  
		Last Modified: Fri, 27 Sep 2024 06:05:04 GMT  
		Size: 2.3 MB (2280692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c438d6540bdc9adc9140d94352ea4200a10e7cfc1168f6b3c47c8202fe19ace1`  
		Last Modified: Fri, 27 Sep 2024 06:05:04 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm variant v5

```console
$ docker pull memcached@sha256:365ca3a58f4ec2be52314d56ca69b149210604be3008c503c731cf5f4a095f5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30222872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43b582780474a2688f3e337b9c5a04bcf5697372ab5e9377d88e069e75607247`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 21:48:32 GMT
ADD file:c162e60b24ef6aed489ba1986f407fd9ab4ace659e0e3e6759ffac7eb0b7f770 in / 
# Wed, 04 Sep 2024 21:48:32 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:44990bd21e0c5db65674bd030d12ea2461a14f2bb4007469bc2667c8535a8357`  
		Last Modified: Wed, 04 Sep 2024 21:51:32 GMT  
		Size: 26.9 MB (26887411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a8ee21aa62c2c20c62d17e0dd3670c4484279b7481df253ab7dea06579e38f6`  
		Last Modified: Thu, 05 Sep 2024 03:28:45 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e5212bff7c052802224f0dcd2c61c47f77a42869600109756dedd710f28915`  
		Last Modified: Thu, 05 Sep 2024 03:28:46 GMT  
		Size: 2.1 MB (2095647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0782223d771fbfcf1c9ed4475479f748c453dd6aa6dc53aa45361cd00224de57`  
		Last Modified: Tue, 10 Sep 2024 02:36:03 GMT  
		Size: 1.2 MB (1238299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530caa10c823e2b669f21afaf522a557d974f4ea259b23e29b5a88c357559aa9`  
		Last Modified: Tue, 10 Sep 2024 02:36:02 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2f95efd2295adb5abdb3e0e56c5d975248bcc1c4951cedbfc5f10c2480cb9c`  
		Last Modified: Tue, 10 Sep 2024 02:36:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:643f24e07712d430691849d647e01c9ba7828371296a20fbe49250e582c0fac2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8e2f351cd6f24d1550b56f8e379b3e6aef1289d89b131237317ca600e4d52a0`

```dockerfile
```

-	Layers:
	-	`sha256:6d0e93f21d109f38cd7d09c5fc37735dc06c58bfcc63c9e950d187b500196f7b`  
		Last Modified: Tue, 10 Sep 2024 02:36:03 GMT  
		Size: 2.3 MB (2284110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:877d052619f8f882ecca7bddd9b19ea3ac0aff81603a8e053c4cfef2c753b056`  
		Last Modified: Tue, 10 Sep 2024 02:36:02 GMT  
		Size: 21.2 KB (21169 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:875cd34f6465e3e8fa28ef5db4bfad8c176e1c0263daff0171fc9537b0ca3a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32767698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a91d45790f325414f2734648e019a463d8d1353ca9250b2700504151dcdfbbe0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:52 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Wed, 04 Sep 2024 21:39:53 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04865bf94e709891a3952f6be4719f98f7a66c94aeb7ca127b805a21559f233b`  
		Last Modified: Fri, 06 Sep 2024 22:18:47 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2accb5dc3319c683f0fcfa968e975b4170700c037764eba741ba2d1c52c8ad0a`  
		Last Modified: Fri, 06 Sep 2024 22:18:47 GMT  
		Size: 2.4 MB (2354829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099212eee1d8aedc74760284b20c722ff3262dfeebadb7801f18e140dd2a88c4`  
		Last Modified: Tue, 10 Sep 2024 05:26:27 GMT  
		Size: 1.3 MB (1254813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfbc137765c6a6be5ae31943c75d26fb8556d6f8d6dc7372cba395a51e9600c8`  
		Last Modified: Tue, 10 Sep 2024 05:26:27 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6847381e1607ee0f70837cb4d081424ec06929f39c8c350ff85944aef711304c`  
		Last Modified: Tue, 10 Sep 2024 05:26:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:56255e99acdfe342a7754928cb5ed717ab5f7372c48426d0dc8b1515d05a4b4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:336d6748c4ae106ed4adc2a8b4c756622427e4066c4aa1351246e7a0fe352da8`

```dockerfile
```

-	Layers:
	-	`sha256:29df9c8dc456cfd5983e243674508af61ff397da6d8d6a997e017e85a4e4266c`  
		Last Modified: Tue, 10 Sep 2024 05:26:27 GMT  
		Size: 2.3 MB (2280993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d304f0d86e38bf9bc9ed7714e76015b79876a10b2d8c67f081473bfdcabe377`  
		Last Modified: Tue, 10 Sep 2024 05:26:27 GMT  
		Size: 21.4 KB (21385 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; 386

```console
$ docker pull memcached@sha256:34dcfa089dd249a4df38d93bee834b8e9ef0f20fc783cc57beecc31eb4e04fcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33904516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7bacc013d82d74a63cc6ad50eec7918e02e35d93e1138cd7405cb396e80b5a3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 22:44:34 GMT
ADD file:1d96491aed0d3091aadb984e1dfe642343013348f4a1807a69e132efaed68030 in / 
# Wed, 04 Sep 2024 22:44:34 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c304282df09b425e8240f53c55110ac282ba801da157a805e4fdbdf8c832b376`  
		Last Modified: Wed, 04 Sep 2024 22:48:08 GMT  
		Size: 30.1 MB (30144294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6c5637a99c0d5bfbc04c2f481699f0ab6cbcf940efabacc33b17680528fcb1`  
		Last Modified: Mon, 09 Sep 2024 23:04:42 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7a2b527feff9ff4df7dcb2a0b26ec01a6fa914c48cfb3bba0d873a5f7ae189`  
		Last Modified: Mon, 09 Sep 2024 23:04:42 GMT  
		Size: 2.5 MB (2499306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d54ad1af4809e5533f75ab13f83a284e966f4bdf5df4880fba412f3fa6e415`  
		Last Modified: Mon, 09 Sep 2024 23:04:42 GMT  
		Size: 1.3 MB (1259401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:683954138ef3ece20193896fd5a5df2deb974514c9f939d749eb46c161f1e4f6`  
		Last Modified: Mon, 09 Sep 2024 23:04:42 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d4e2b90164f16b0893ff5354664d43d05f691e1ef4165d1f45889cfaa8bc68`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:5f5144206a28ac6d02a6064d09bef45ba19ea0e834380667b5252173fc1aee2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2298749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c582914882b6e0802c0ff6073312ad790deb59006c1edeeca6423351ecc04295`

```dockerfile
```

-	Layers:
	-	`sha256:08d010ee1407ba55007943c5783e18992fce487cf9fc06f1001a6c6ee139ad50`  
		Last Modified: Mon, 09 Sep 2024 23:04:42 GMT  
		Size: 2.3 MB (2277777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8dabd61e7f4bdb4bd9a53e403b676e865ad1ec09201180b76f03117a501c2d7`  
		Last Modified: Mon, 09 Sep 2024 23:04:42 GMT  
		Size: 21.0 KB (20972 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; mips64le

```console
$ docker pull memcached@sha256:6f842f8998fe08cfdcb13cd83a7d09dfee91b25ae8b6937b02702480c5c55d22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32323662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d5a34a6f646baa48f817d457c47eb9762e5066adc40bc80cded7232eacb00d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 22:15:45 GMT
ADD file:9ffa4d53a074e91efecf5e26e3b67077f46165e0d042c1e6cf1b93c531ed2bc4 in / 
# Wed, 04 Sep 2024 22:15:50 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:89502a0eae32ab684bc9df3d9922ee2874839b178a693286c4b866f5ca8e93f3`  
		Last Modified: Wed, 04 Sep 2024 22:24:11 GMT  
		Size: 29.1 MB (29125054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a544e9e80cb1c7ab6c5794cb1a0a4715aa0df1fd8437a0d771017c52f3e5f5`  
		Last Modified: Thu, 05 Sep 2024 11:18:11 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7605e144a412910a4194cfffafd5d127bc44e9b19ba5191b74df2cc6a267f2e0`  
		Last Modified: Thu, 05 Sep 2024 11:18:12 GMT  
		Size: 1.9 MB (1942689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92a7d1694bf26de03563c78b52328eeabf26a387feba7ff6fbb8bb253427f27`  
		Last Modified: Tue, 10 Sep 2024 02:25:37 GMT  
		Size: 1.3 MB (1254404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c99675ddde9651d74c5ef49e2a70ca2c3351852fb856272dfb9b5f328a69e31`  
		Last Modified: Tue, 10 Sep 2024 02:25:37 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859d2e9814139aaf71bc0d3cc5e5eecdba1d8f10c4cc0196aa46b58d2830bebe`  
		Last Modified: Tue, 10 Sep 2024 02:25:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:6c4530d40688ecfde5ff475267c0fd60f9d67cd7e23c5e177ae0e20937467413
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e60bb1c6684aec9c40b2deb99de2c399adb2682fdc6efecdd98aef1881475ac`

```dockerfile
```

-	Layers:
	-	`sha256:74c8d993dc8b0fbc1c7708b04cec649eac5a3f36f5bc171bc1d523edc126aeff`  
		Last Modified: Tue, 10 Sep 2024 02:25:37 GMT  
		Size: 20.9 KB (20911 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; ppc64le

```console
$ docker pull memcached@sha256:a2c15d4ae7e15fa7457c5f843feb6bfc17bf3a4ee8c7fe278e9af0824a54be80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37154878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4f56f782d0ddfeacfa04a2d1bc62b4ee9938d6128b8c29f12647454f427251e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 22:25:52 GMT
ADD file:d83b2f8d4d3fd22a390140e3bebefb48e5f086d072ad6062f6446b4fc42ec7a8 in / 
# Wed, 04 Sep 2024 22:25:54 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f19b11698292330b7d980ed50b0141417eec298d865e0c1b305ce7a8b80b572d`  
		Last Modified: Wed, 04 Sep 2024 22:30:11 GMT  
		Size: 33.1 MB (33122358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ee1834d6aa97efd9d43db3a50a5bb3dda4b08400d531f72579cadea051609e`  
		Last Modified: Fri, 06 Sep 2024 22:02:56 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9152281fc8ce1403b29050f252829939c461cf037d8b3491653f7eeee4ece43`  
		Last Modified: Fri, 06 Sep 2024 22:02:56 GMT  
		Size: 2.7 MB (2707191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e141823a412ee63afdae23f927aa51b3eb72dd45577cf194159595a77d4577e2`  
		Last Modified: Tue, 10 Sep 2024 00:53:10 GMT  
		Size: 1.3 MB (1323809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c8e76a6f99b8b59c45f2a7eea7a5ee3870791b1a3abe6679881522a171e998`  
		Last Modified: Tue, 10 Sep 2024 00:53:10 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc7d2a375bf95c80dfd28c577fb84d803a9bb9437dd19ebc1801f99fb035120`  
		Last Modified: Tue, 10 Sep 2024 00:53:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:3bd251857bd96c65b8ad1e08a21c64177e673356369ff7404be1ba2edac796b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4713e2ddd75a9c1fba28b6cf8191e2ed2cb6b5e47a06bcb2db95a9efbbc74fda`

```dockerfile
```

-	Layers:
	-	`sha256:ca0b1f85d6ea571ab124bed1c494d1d8fb6673a42d0cb794a3eb947b1e1f9b06`  
		Last Modified: Tue, 10 Sep 2024 00:53:10 GMT  
		Size: 2.3 MB (2285050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73f6f1fc8ce970b2f59c4b67cfef86ef3c1dc692d3e5b91930a0f834c2aa8286`  
		Last Modified: Tue, 10 Sep 2024 00:53:10 GMT  
		Size: 21.1 KB (21095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; s390x

```console
$ docker pull memcached@sha256:a564ae9d7581535075625ac57d9c0b961354e9b4daba7c4b8081f9c94a7272cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30885604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0553326148f76a8da67990b40b3cda91d5eb09e6450645d355301f64cdd62ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 21:42:50 GMT
ADD file:728128617ba2b026c358eb266cd495be84354c4e5dc4ecc2953cb829190a4546 in / 
# Wed, 04 Sep 2024 21:42:52 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:95fe27c895a828dc681ee4a0cbea0264c47528dad525efdb9641a375666536bd`  
		Last Modified: Wed, 04 Sep 2024 21:47:41 GMT  
		Size: 27.5 MB (27490321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14930957f1690905df41f1da11505509319dd65a7de378761ed685a7f319746`  
		Last Modified: Fri, 06 Sep 2024 22:03:27 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0833ee43e72a5f44318da8b85bdf6aa1bb3bddf0fdd75dc5530531a126eb97`  
		Last Modified: Fri, 06 Sep 2024 22:03:27 GMT  
		Size: 2.2 MB (2155800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49ba017e9517b59a0101e268f88f7b430651242d3de79201588254bb0fe7507`  
		Last Modified: Mon, 09 Sep 2024 23:57:11 GMT  
		Size: 1.2 MB (1237972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f824a2d96ada01e3ba546f908f36e9780321cfd73e3145903949cd6f8d9bbc`  
		Last Modified: Mon, 09 Sep 2024 23:57:11 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c979fb5ce067e0a4128dc5527a66b9ee1bf3762c94b5f309c473ede06b29be`  
		Last Modified: Mon, 09 Sep 2024 23:57:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:d96f09ec7f4c6e807df2fac9bd6834a30ab928672e82902cd5cc756d638221a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d39e3cfd9222897db8d98adeddedd43e35a75647f77cf2ca9276356feeb1695`

```dockerfile
```

-	Layers:
	-	`sha256:d83c73c94a489231e85f509c8c17651508a61d8aa02ef340f03babd8b3a5253b`  
		Last Modified: Mon, 09 Sep 2024 23:57:11 GMT  
		Size: 2.3 MB (2280500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b7064082e2a2543d417d8956bcd38d8aa02707fd3284afe698b5e0c00f111b1`  
		Last Modified: Mon, 09 Sep 2024 23:57:11 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine`

```console
$ docker pull memcached@sha256:6fff88e239680465aa0b7e977b2f1a322471c3552644159371de6c1731a5014a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `memcached:1-alpine` - linux; amd64

```console
$ docker pull memcached@sha256:bc62c9b146672d0f63f0b3a38722acae32e859f635e6f32f0b31afdcb1013c7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4687755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aae0d824f4bc7874b3fd26fc5e61b2fe8c3fc9b58f82f3be24a6010c05ec1c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e2704d07ea50e4350fc30a778f91c517bee857b54bcc571b464e2b563744ab`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f89cbdbe5025b3c7d2ff8f9f6bfbb7bcd639adb35200de6f0b8b4515488f1b05`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 103.8 KB (103822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f139dbcb2579cd1e9f78db09fd279e08d323c219a6efcad878b42cd961d24a25`  
		Last Modified: Mon, 09 Sep 2024 23:04:31 GMT  
		Size: 958.8 KB (958765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3487c95e4eb9d8fb5506b2cd3406c02c1fba592fbafe1078c141420c22939fc7`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eaf1d2da7366110dda884212201a67c62fb0f9c921217de86755d35b80fbee9`  
		Last Modified: Mon, 09 Sep 2024 23:04:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:c96c825ac5a6f1db0849694d7878693b7113126e5c85540cdb4e191454d0afcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 KB (107135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a3dddb2bd6769fc79a77da8e93edcfe6d98d55badebcebbc9faaecb661ad001`

```dockerfile
```

-	Layers:
	-	`sha256:7102ff71a3580f59d96136c579e83bbb7e913951d315d57f5d15541dc8438bdb`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 87.8 KB (87785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e083725668b94672a9a645717ffd665a9f0059d9823eed6b8b1bc89bee285c4e`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 19.4 KB (19350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:a2d38a957041270c55d551e8ecf53f69df6613a17df3fb1876ab6fb65cd99ea6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5172731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3954249ac508b8b8c4a968b394a6970e8d868f1744e672affe792ee9231b39ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04310511d0b87f77a431a5f50ac0c3d95896d6a39a16aa043ba443f6b0e0fddd`  
		Last Modified: Sat, 07 Sep 2024 05:30:38 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b28609c2d169047004bf72890ec5ac9e3a88bd3aa153e465bf17c14f3ebf3b`  
		Last Modified: Sat, 07 Sep 2024 05:30:38 GMT  
		Size: 121.0 KB (121024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4adf4e4f7be512c6272c74db833112894b8410062060f6888539171290372a82`  
		Last Modified: Tue, 10 Sep 2024 05:30:03 GMT  
		Size: 962.7 KB (962700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c043e4b98daae0158835eeb78946255c4027b9ebe97d5e569fa8f1df39119c7`  
		Last Modified: Tue, 10 Sep 2024 05:30:03 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e243cd97c138165f622734a969475116f77deb0f3c6efaf70fae4ac39ebbffc`  
		Last Modified: Tue, 10 Sep 2024 05:30:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:9d2c6d970fa941ac951ded01e253b2d4492d8bda51fd29bc2f6915310f884231
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0bc6ae2b075b905b17704735488c6da23574abab2bbc1bb4aefebbe65768955`

```dockerfile
```

-	Layers:
	-	`sha256:36cf7adc241f552244e6d64628168a1dee985ba7a3176282286b5ca13998f243`  
		Last Modified: Tue, 10 Sep 2024 05:30:02 GMT  
		Size: 87.9 KB (87889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90b01e0840b58a8d84f085ca69e1f3f3eb1fd0a0abd8b42fca270e09451e6161`  
		Last Modified: Tue, 10 Sep 2024 05:30:02 GMT  
		Size: 19.7 KB (19698 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; 386

```console
$ docker pull memcached@sha256:7228773d86ac6e8955e5d2d7ffefc2ae564b00cadd0c858310dec50e9fad6f42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4531177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41f22aace0957bde9cbc95b95320e1836991afac8a43e215d16ef141508788c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:41:21 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Fri, 06 Sep 2024 22:41:21 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e2704d07ea50e4350fc30a778f91c517bee857b54bcc571b464e2b563744ab`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef4ec43894c33c1d68e1fbb24d27f314125a8617ada637af061725989f14953`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 109.0 KB (108961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b19ce951cfcb336fa2050f3422e487f515d16ddcf2c69c80d29d9f66baa9d16e`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 951.7 KB (951692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cfaaa1bc534e7c46c1b3aa67465a41ca91d4ce83071caebc7a11e3ff143be02`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0615a81d8e335acdc6d68eefcf35b5d516a3cc0ed68bac6adfd5807799b53f46`  
		Last Modified: Mon, 09 Sep 2024 23:04:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7940458999ce753465ef3f968a9eabac518a9df3d5d77386552d3526c2b946ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.0 KB (107035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e2e327ed8d984210e8a47612bf76565fb47b80c1d0e63bbc53b45c571fd09f9`

```dockerfile
```

-	Layers:
	-	`sha256:c1c9fcdee5d34fae3276a06573fa1e3d9a3a0b6d532765266d4e86f6be9a695b`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 87.7 KB (87740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12c78394468356d9d60cea99380a31c53b12f50a43699c3916eda41ba6ee3470`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 19.3 KB (19295 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:517da247dc00201621112cd48487139ce6966636899a4c40fdb02b307f3f1b5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4694177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98eb649600a0e4277874d7abade7034b99d425dcb34c55e165f11569d4166b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:06 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 22:26:07 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645d78667a8075f56004a7a283eaeb1a630309a9d950a27de5cc29eb72cec340`  
		Last Modified: Sat, 07 Sep 2024 07:05:29 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5844b90ee5623766614a832d5e5f322566849ed5853adfbe1f63e8d954b540d9`  
		Last Modified: Sat, 07 Sep 2024 07:05:29 GMT  
		Size: 123.0 KB (123003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b715436c927b60842b1c1f98f7cb7c4257838f7b36a5e2334b5f590ca152f6`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 997.4 KB (997389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ad232e17fce60e215c458fcac12f4ac1d5bdd60080527a4c28d76c6c831393`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8e18c99726667f58640d52458967d66a4da28b7f2eaaac5626723a6691ed45`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:e4e8b6df3a60e291797c10897a7779345a41715ab61dfd7f76bccdc42ef8a7ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 KB (105307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469f18677668b4dd9a3de113d4ae3f111f5b89e03f3795cef6eab0e1e3eecbbe`

```dockerfile
```

-	Layers:
	-	`sha256:f7beb1e9f1753005bac3249d305c8567220853e93353216074762ad7f1813c0a`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 85.9 KB (85889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2eea735dc745320130c1139867abe3e0b71de840a5a8a3170b9191994b69b01b`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 19.4 KB (19418 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:ceffb56b913ca8a62831ef271642b11ddbeea098de65d093af55cbba0f8d56e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4427664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c258ae7e36ddd3758d8ddff147c4db3f4928f4db92f67bc7b91ffa68c86d4ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:cdf7088bbd70519f0f5d7b4249df34386e40f0194752f45842b3d85f2d331cf5 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["/bin/sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:faf447acae27573624c0613a79c4bcf1f9bc46d29f523140352abfd3f7691282`  
		Last Modified: Mon, 22 Jul 2024 22:21:18 GMT  
		Size: 3.4 MB (3370673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230af89e5f8d3eec0e6d96c87e99a85b938e0722dacebe0009ad7b8b00ca320b`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c75b82861f48f0052a86f16f944c0324ed20af856a4c9d87c147dc645460ee6`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 108.6 KB (108596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d23c6553fa0ff65e57ebc39080a958cc4d1d02587781c94836137d124c47ce`  
		Last Modified: Sun, 28 Jul 2024 15:58:50 GMT  
		Size: 947.0 KB (947030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab42ab26d315472c0f9433b5c7f25e0e426c020b3b0e8cc52d1c7d09ca7bf91`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e436e8ed56076dff056e7dc989a1944739cb23a96400a543900ab3bd07a77b6`  
		Last Modified: Sun, 28 Jul 2024 15:58:50 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:fdf92c6c75f08244e376b28b33307c9ea75a07f7523b56b86df44f1be3335f3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 KB (105303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc24bdd15449aa6c8213cd2607de7998a598edba9ca2fb7de80b4b761b833a64`

```dockerfile
```

-	Layers:
	-	`sha256:dbb3dc8245856acbf66987c1cd0f4f37d8af7b49bc0c7b8eaacfb02321594ac5`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 85.9 KB (85885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2359a9107230c13ad5d1c580fc348790129c58ea95b407db376ee7eb5a109571`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 19.4 KB (19418 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:a6f8155d863aa33eae871b75e7543c04404c30248007928840beeffae2eb5e78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4556594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63fcf33c45f689bdee882ed4ad8692b55a55abe13941eb4cc525adeafab650c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:17 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 22:48:17 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc58d10317d926d80ab2de5020728ade9434725004663fce6207d95ecc3ba0c`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed425e517c8a02d89379669853a47dbd343281c3fcfc3e37f91b671f0b35ffc`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 112.7 KB (112740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02fe29c4e792447391a38d4b9d7aa18f9a51d6f171eb15297a427efb6a33e839`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 980.9 KB (980896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fffd060f2e26e85750706fd829abf92d787fdf9321cba829cab93f30845547f`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93825c9e15b3ee5a0f3ebddccf232551b4506353af049da3e37f7ae97e39a384`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:5c62ae13354b08074917592e56f436a96d4ccf47cbf5c4a13231f53d556be814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 KB (105181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fda0c239bf944625a0bd5aeea27175b74c697a79c4b068f9d8e137b786a2b4a4`

```dockerfile
```

-	Layers:
	-	`sha256:870d5efdd4242eb6cc01519cd2092666c5ab15b546cb69d2711791408721605b`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 85.8 KB (85831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dbbbb69edb2b376c21146fd5c88b6254433cc9264976b2868973688bb8a95cf`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 19.4 KB (19350 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine3.20`

```console
$ docker pull memcached@sha256:6fff88e239680465aa0b7e977b2f1a322471c3552644159371de6c1731a5014a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `memcached:1-alpine3.20` - linux; amd64

```console
$ docker pull memcached@sha256:bc62c9b146672d0f63f0b3a38722acae32e859f635e6f32f0b31afdcb1013c7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4687755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aae0d824f4bc7874b3fd26fc5e61b2fe8c3fc9b58f82f3be24a6010c05ec1c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e2704d07ea50e4350fc30a778f91c517bee857b54bcc571b464e2b563744ab`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f89cbdbe5025b3c7d2ff8f9f6bfbb7bcd639adb35200de6f0b8b4515488f1b05`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 103.8 KB (103822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f139dbcb2579cd1e9f78db09fd279e08d323c219a6efcad878b42cd961d24a25`  
		Last Modified: Mon, 09 Sep 2024 23:04:31 GMT  
		Size: 958.8 KB (958765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3487c95e4eb9d8fb5506b2cd3406c02c1fba592fbafe1078c141420c22939fc7`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eaf1d2da7366110dda884212201a67c62fb0f9c921217de86755d35b80fbee9`  
		Last Modified: Mon, 09 Sep 2024 23:04:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:c96c825ac5a6f1db0849694d7878693b7113126e5c85540cdb4e191454d0afcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 KB (107135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a3dddb2bd6769fc79a77da8e93edcfe6d98d55badebcebbc9faaecb661ad001`

```dockerfile
```

-	Layers:
	-	`sha256:7102ff71a3580f59d96136c579e83bbb7e913951d315d57f5d15541dc8438bdb`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 87.8 KB (87785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e083725668b94672a9a645717ffd665a9f0059d9823eed6b8b1bc89bee285c4e`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 19.4 KB (19350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:a2d38a957041270c55d551e8ecf53f69df6613a17df3fb1876ab6fb65cd99ea6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5172731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3954249ac508b8b8c4a968b394a6970e8d868f1744e672affe792ee9231b39ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04310511d0b87f77a431a5f50ac0c3d95896d6a39a16aa043ba443f6b0e0fddd`  
		Last Modified: Sat, 07 Sep 2024 05:30:38 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b28609c2d169047004bf72890ec5ac9e3a88bd3aa153e465bf17c14f3ebf3b`  
		Last Modified: Sat, 07 Sep 2024 05:30:38 GMT  
		Size: 121.0 KB (121024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4adf4e4f7be512c6272c74db833112894b8410062060f6888539171290372a82`  
		Last Modified: Tue, 10 Sep 2024 05:30:03 GMT  
		Size: 962.7 KB (962700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c043e4b98daae0158835eeb78946255c4027b9ebe97d5e569fa8f1df39119c7`  
		Last Modified: Tue, 10 Sep 2024 05:30:03 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e243cd97c138165f622734a969475116f77deb0f3c6efaf70fae4ac39ebbffc`  
		Last Modified: Tue, 10 Sep 2024 05:30:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:9d2c6d970fa941ac951ded01e253b2d4492d8bda51fd29bc2f6915310f884231
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0bc6ae2b075b905b17704735488c6da23574abab2bbc1bb4aefebbe65768955`

```dockerfile
```

-	Layers:
	-	`sha256:36cf7adc241f552244e6d64628168a1dee985ba7a3176282286b5ca13998f243`  
		Last Modified: Tue, 10 Sep 2024 05:30:02 GMT  
		Size: 87.9 KB (87889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90b01e0840b58a8d84f085ca69e1f3f3eb1fd0a0abd8b42fca270e09451e6161`  
		Last Modified: Tue, 10 Sep 2024 05:30:02 GMT  
		Size: 19.7 KB (19698 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.20` - linux; 386

```console
$ docker pull memcached@sha256:7228773d86ac6e8955e5d2d7ffefc2ae564b00cadd0c858310dec50e9fad6f42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4531177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41f22aace0957bde9cbc95b95320e1836991afac8a43e215d16ef141508788c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:41:21 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Fri, 06 Sep 2024 22:41:21 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e2704d07ea50e4350fc30a778f91c517bee857b54bcc571b464e2b563744ab`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef4ec43894c33c1d68e1fbb24d27f314125a8617ada637af061725989f14953`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 109.0 KB (108961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b19ce951cfcb336fa2050f3422e487f515d16ddcf2c69c80d29d9f66baa9d16e`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 951.7 KB (951692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cfaaa1bc534e7c46c1b3aa67465a41ca91d4ce83071caebc7a11e3ff143be02`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0615a81d8e335acdc6d68eefcf35b5d516a3cc0ed68bac6adfd5807799b53f46`  
		Last Modified: Mon, 09 Sep 2024 23:04:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:7940458999ce753465ef3f968a9eabac518a9df3d5d77386552d3526c2b946ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.0 KB (107035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e2e327ed8d984210e8a47612bf76565fb47b80c1d0e63bbc53b45c571fd09f9`

```dockerfile
```

-	Layers:
	-	`sha256:c1c9fcdee5d34fae3276a06573fa1e3d9a3a0b6d532765266d4e86f6be9a695b`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 87.7 KB (87740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12c78394468356d9d60cea99380a31c53b12f50a43699c3916eda41ba6ee3470`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 19.3 KB (19295 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.20` - linux; ppc64le

```console
$ docker pull memcached@sha256:517da247dc00201621112cd48487139ce6966636899a4c40fdb02b307f3f1b5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4694177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98eb649600a0e4277874d7abade7034b99d425dcb34c55e165f11569d4166b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:06 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 22:26:07 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645d78667a8075f56004a7a283eaeb1a630309a9d950a27de5cc29eb72cec340`  
		Last Modified: Sat, 07 Sep 2024 07:05:29 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5844b90ee5623766614a832d5e5f322566849ed5853adfbe1f63e8d954b540d9`  
		Last Modified: Sat, 07 Sep 2024 07:05:29 GMT  
		Size: 123.0 KB (123003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b715436c927b60842b1c1f98f7cb7c4257838f7b36a5e2334b5f590ca152f6`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 997.4 KB (997389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ad232e17fce60e215c458fcac12f4ac1d5bdd60080527a4c28d76c6c831393`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8e18c99726667f58640d52458967d66a4da28b7f2eaaac5626723a6691ed45`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:e4e8b6df3a60e291797c10897a7779345a41715ab61dfd7f76bccdc42ef8a7ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 KB (105307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469f18677668b4dd9a3de113d4ae3f111f5b89e03f3795cef6eab0e1e3eecbbe`

```dockerfile
```

-	Layers:
	-	`sha256:f7beb1e9f1753005bac3249d305c8567220853e93353216074762ad7f1813c0a`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 85.9 KB (85889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2eea735dc745320130c1139867abe3e0b71de840a5a8a3170b9191994b69b01b`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 19.4 KB (19418 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.20` - linux; riscv64

```console
$ docker pull memcached@sha256:ceffb56b913ca8a62831ef271642b11ddbeea098de65d093af55cbba0f8d56e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4427664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c258ae7e36ddd3758d8ddff147c4db3f4928f4db92f67bc7b91ffa68c86d4ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:cdf7088bbd70519f0f5d7b4249df34386e40f0194752f45842b3d85f2d331cf5 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["/bin/sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:faf447acae27573624c0613a79c4bcf1f9bc46d29f523140352abfd3f7691282`  
		Last Modified: Mon, 22 Jul 2024 22:21:18 GMT  
		Size: 3.4 MB (3370673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230af89e5f8d3eec0e6d96c87e99a85b938e0722dacebe0009ad7b8b00ca320b`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c75b82861f48f0052a86f16f944c0324ed20af856a4c9d87c147dc645460ee6`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 108.6 KB (108596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d23c6553fa0ff65e57ebc39080a958cc4d1d02587781c94836137d124c47ce`  
		Last Modified: Sun, 28 Jul 2024 15:58:50 GMT  
		Size: 947.0 KB (947030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab42ab26d315472c0f9433b5c7f25e0e426c020b3b0e8cc52d1c7d09ca7bf91`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e436e8ed56076dff056e7dc989a1944739cb23a96400a543900ab3bd07a77b6`  
		Last Modified: Sun, 28 Jul 2024 15:58:50 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:fdf92c6c75f08244e376b28b33307c9ea75a07f7523b56b86df44f1be3335f3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 KB (105303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc24bdd15449aa6c8213cd2607de7998a598edba9ca2fb7de80b4b761b833a64`

```dockerfile
```

-	Layers:
	-	`sha256:dbb3dc8245856acbf66987c1cd0f4f37d8af7b49bc0c7b8eaacfb02321594ac5`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 85.9 KB (85885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2359a9107230c13ad5d1c580fc348790129c58ea95b407db376ee7eb5a109571`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 19.4 KB (19418 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.20` - linux; s390x

```console
$ docker pull memcached@sha256:a6f8155d863aa33eae871b75e7543c04404c30248007928840beeffae2eb5e78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4556594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63fcf33c45f689bdee882ed4ad8692b55a55abe13941eb4cc525adeafab650c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:17 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 22:48:17 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc58d10317d926d80ab2de5020728ade9434725004663fce6207d95ecc3ba0c`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed425e517c8a02d89379669853a47dbd343281c3fcfc3e37f91b671f0b35ffc`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 112.7 KB (112740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02fe29c4e792447391a38d4b9d7aa18f9a51d6f171eb15297a427efb6a33e839`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 980.9 KB (980896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fffd060f2e26e85750706fd829abf92d787fdf9321cba829cab93f30845547f`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93825c9e15b3ee5a0f3ebddccf232551b4506353af049da3e37f7ae97e39a384`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:5c62ae13354b08074917592e56f436a96d4ccf47cbf5c4a13231f53d556be814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 KB (105181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fda0c239bf944625a0bd5aeea27175b74c697a79c4b068f9d8e137b786a2b4a4`

```dockerfile
```

-	Layers:
	-	`sha256:870d5efdd4242eb6cc01519cd2092666c5ab15b546cb69d2711791408721605b`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 85.8 KB (85831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dbbbb69edb2b376c21146fd5c88b6254433cc9264976b2868973688bb8a95cf`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 19.4 KB (19350 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-bookworm`

```console
$ docker pull memcached@sha256:51cdb01f624e1eab205f978b21756cf3ef96ca33da2cd074cb47245b92e0705f
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
$ docker pull memcached@sha256:a658d819b6f9ab244148f9e9994489e759ff72e12cd2a93cf0a9b0259f324743
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32878406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a783d40c8b808e6a5c1d562c8ddf24732920c2c1b7e12eadaeb76b3f1e468b32`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 07 Sep 2024 18:54:11 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d937ff39f058bf2417a4fe760827ff36b1b38be77ed6c3b27fbd80872b4106b9`  
		Last Modified: Fri, 27 Sep 2024 06:05:04 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2bb47e18c2052b1e07d1957f90f1d197fcbf398748e534e8fa54f75782b3fff`  
		Last Modified: Fri, 27 Sep 2024 06:05:04 GMT  
		Size: 2.5 MB (2491322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c618990832780ea1a130f360744ad52c95ef7485138ded320b5563aedc090b`  
		Last Modified: Fri, 27 Sep 2024 06:05:04 GMT  
		Size: 1.3 MB (1259299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f09b0e04f54ca243201f3b8f205c759c2892f6752f8e75aa84434ab4a4b330`  
		Last Modified: Fri, 27 Sep 2024 06:05:04 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2038e2b3f99ec442dfe1024270c1ad10a59fb8995060bc0a2e7a6831bbc48917`  
		Last Modified: Fri, 27 Sep 2024 06:05:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:2fbb3c4bddfc491f239cbe76e97dbd05fa35514c183e7fa4ac819cda30fd5acf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b83b1908356b5b8567c67431165b1c6e4a18a87b108cb329988349341ed52f3e`

```dockerfile
```

-	Layers:
	-	`sha256:e0ac909638f1cc11061867d2eca41aafdfd8ac0189cceb25a5aa9c4ff9c7f0fc`  
		Last Modified: Fri, 27 Sep 2024 06:05:04 GMT  
		Size: 2.3 MB (2280692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c438d6540bdc9adc9140d94352ea4200a10e7cfc1168f6b3c47c8202fe19ace1`  
		Last Modified: Fri, 27 Sep 2024 06:05:04 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:365ca3a58f4ec2be52314d56ca69b149210604be3008c503c731cf5f4a095f5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30222872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43b582780474a2688f3e337b9c5a04bcf5697372ab5e9377d88e069e75607247`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 21:48:32 GMT
ADD file:c162e60b24ef6aed489ba1986f407fd9ab4ace659e0e3e6759ffac7eb0b7f770 in / 
# Wed, 04 Sep 2024 21:48:32 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:44990bd21e0c5db65674bd030d12ea2461a14f2bb4007469bc2667c8535a8357`  
		Last Modified: Wed, 04 Sep 2024 21:51:32 GMT  
		Size: 26.9 MB (26887411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a8ee21aa62c2c20c62d17e0dd3670c4484279b7481df253ab7dea06579e38f6`  
		Last Modified: Thu, 05 Sep 2024 03:28:45 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e5212bff7c052802224f0dcd2c61c47f77a42869600109756dedd710f28915`  
		Last Modified: Thu, 05 Sep 2024 03:28:46 GMT  
		Size: 2.1 MB (2095647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0782223d771fbfcf1c9ed4475479f748c453dd6aa6dc53aa45361cd00224de57`  
		Last Modified: Tue, 10 Sep 2024 02:36:03 GMT  
		Size: 1.2 MB (1238299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530caa10c823e2b669f21afaf522a557d974f4ea259b23e29b5a88c357559aa9`  
		Last Modified: Tue, 10 Sep 2024 02:36:02 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2f95efd2295adb5abdb3e0e56c5d975248bcc1c4951cedbfc5f10c2480cb9c`  
		Last Modified: Tue, 10 Sep 2024 02:36:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:643f24e07712d430691849d647e01c9ba7828371296a20fbe49250e582c0fac2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8e2f351cd6f24d1550b56f8e379b3e6aef1289d89b131237317ca600e4d52a0`

```dockerfile
```

-	Layers:
	-	`sha256:6d0e93f21d109f38cd7d09c5fc37735dc06c58bfcc63c9e950d187b500196f7b`  
		Last Modified: Tue, 10 Sep 2024 02:36:03 GMT  
		Size: 2.3 MB (2284110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:877d052619f8f882ecca7bddd9b19ea3ac0aff81603a8e053c4cfef2c753b056`  
		Last Modified: Tue, 10 Sep 2024 02:36:02 GMT  
		Size: 21.2 KB (21169 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:875cd34f6465e3e8fa28ef5db4bfad8c176e1c0263daff0171fc9537b0ca3a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32767698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a91d45790f325414f2734648e019a463d8d1353ca9250b2700504151dcdfbbe0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:52 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Wed, 04 Sep 2024 21:39:53 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04865bf94e709891a3952f6be4719f98f7a66c94aeb7ca127b805a21559f233b`  
		Last Modified: Fri, 06 Sep 2024 22:18:47 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2accb5dc3319c683f0fcfa968e975b4170700c037764eba741ba2d1c52c8ad0a`  
		Last Modified: Fri, 06 Sep 2024 22:18:47 GMT  
		Size: 2.4 MB (2354829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099212eee1d8aedc74760284b20c722ff3262dfeebadb7801f18e140dd2a88c4`  
		Last Modified: Tue, 10 Sep 2024 05:26:27 GMT  
		Size: 1.3 MB (1254813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfbc137765c6a6be5ae31943c75d26fb8556d6f8d6dc7372cba395a51e9600c8`  
		Last Modified: Tue, 10 Sep 2024 05:26:27 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6847381e1607ee0f70837cb4d081424ec06929f39c8c350ff85944aef711304c`  
		Last Modified: Tue, 10 Sep 2024 05:26:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:56255e99acdfe342a7754928cb5ed717ab5f7372c48426d0dc8b1515d05a4b4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:336d6748c4ae106ed4adc2a8b4c756622427e4066c4aa1351246e7a0fe352da8`

```dockerfile
```

-	Layers:
	-	`sha256:29df9c8dc456cfd5983e243674508af61ff397da6d8d6a997e017e85a4e4266c`  
		Last Modified: Tue, 10 Sep 2024 05:26:27 GMT  
		Size: 2.3 MB (2280993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d304f0d86e38bf9bc9ed7714e76015b79876a10b2d8c67f081473bfdcabe377`  
		Last Modified: Tue, 10 Sep 2024 05:26:27 GMT  
		Size: 21.4 KB (21385 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:34dcfa089dd249a4df38d93bee834b8e9ef0f20fc783cc57beecc31eb4e04fcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33904516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7bacc013d82d74a63cc6ad50eec7918e02e35d93e1138cd7405cb396e80b5a3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 22:44:34 GMT
ADD file:1d96491aed0d3091aadb984e1dfe642343013348f4a1807a69e132efaed68030 in / 
# Wed, 04 Sep 2024 22:44:34 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c304282df09b425e8240f53c55110ac282ba801da157a805e4fdbdf8c832b376`  
		Last Modified: Wed, 04 Sep 2024 22:48:08 GMT  
		Size: 30.1 MB (30144294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6c5637a99c0d5bfbc04c2f481699f0ab6cbcf940efabacc33b17680528fcb1`  
		Last Modified: Mon, 09 Sep 2024 23:04:42 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7a2b527feff9ff4df7dcb2a0b26ec01a6fa914c48cfb3bba0d873a5f7ae189`  
		Last Modified: Mon, 09 Sep 2024 23:04:42 GMT  
		Size: 2.5 MB (2499306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d54ad1af4809e5533f75ab13f83a284e966f4bdf5df4880fba412f3fa6e415`  
		Last Modified: Mon, 09 Sep 2024 23:04:42 GMT  
		Size: 1.3 MB (1259401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:683954138ef3ece20193896fd5a5df2deb974514c9f939d749eb46c161f1e4f6`  
		Last Modified: Mon, 09 Sep 2024 23:04:42 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d4e2b90164f16b0893ff5354664d43d05f691e1ef4165d1f45889cfaa8bc68`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:5f5144206a28ac6d02a6064d09bef45ba19ea0e834380667b5252173fc1aee2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2298749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c582914882b6e0802c0ff6073312ad790deb59006c1edeeca6423351ecc04295`

```dockerfile
```

-	Layers:
	-	`sha256:08d010ee1407ba55007943c5783e18992fce487cf9fc06f1001a6c6ee139ad50`  
		Last Modified: Mon, 09 Sep 2024 23:04:42 GMT  
		Size: 2.3 MB (2277777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8dabd61e7f4bdb4bd9a53e403b676e865ad1ec09201180b76f03117a501c2d7`  
		Last Modified: Mon, 09 Sep 2024 23:04:42 GMT  
		Size: 21.0 KB (20972 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:6f842f8998fe08cfdcb13cd83a7d09dfee91b25ae8b6937b02702480c5c55d22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32323662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d5a34a6f646baa48f817d457c47eb9762e5066adc40bc80cded7232eacb00d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 22:15:45 GMT
ADD file:9ffa4d53a074e91efecf5e26e3b67077f46165e0d042c1e6cf1b93c531ed2bc4 in / 
# Wed, 04 Sep 2024 22:15:50 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:89502a0eae32ab684bc9df3d9922ee2874839b178a693286c4b866f5ca8e93f3`  
		Last Modified: Wed, 04 Sep 2024 22:24:11 GMT  
		Size: 29.1 MB (29125054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a544e9e80cb1c7ab6c5794cb1a0a4715aa0df1fd8437a0d771017c52f3e5f5`  
		Last Modified: Thu, 05 Sep 2024 11:18:11 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7605e144a412910a4194cfffafd5d127bc44e9b19ba5191b74df2cc6a267f2e0`  
		Last Modified: Thu, 05 Sep 2024 11:18:12 GMT  
		Size: 1.9 MB (1942689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92a7d1694bf26de03563c78b52328eeabf26a387feba7ff6fbb8bb253427f27`  
		Last Modified: Tue, 10 Sep 2024 02:25:37 GMT  
		Size: 1.3 MB (1254404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c99675ddde9651d74c5ef49e2a70ca2c3351852fb856272dfb9b5f328a69e31`  
		Last Modified: Tue, 10 Sep 2024 02:25:37 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859d2e9814139aaf71bc0d3cc5e5eecdba1d8f10c4cc0196aa46b58d2830bebe`  
		Last Modified: Tue, 10 Sep 2024 02:25:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:6c4530d40688ecfde5ff475267c0fd60f9d67cd7e23c5e177ae0e20937467413
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e60bb1c6684aec9c40b2deb99de2c399adb2682fdc6efecdd98aef1881475ac`

```dockerfile
```

-	Layers:
	-	`sha256:74c8d993dc8b0fbc1c7708b04cec649eac5a3f36f5bc171bc1d523edc126aeff`  
		Last Modified: Tue, 10 Sep 2024 02:25:37 GMT  
		Size: 20.9 KB (20911 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:a2c15d4ae7e15fa7457c5f843feb6bfc17bf3a4ee8c7fe278e9af0824a54be80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37154878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4f56f782d0ddfeacfa04a2d1bc62b4ee9938d6128b8c29f12647454f427251e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 22:25:52 GMT
ADD file:d83b2f8d4d3fd22a390140e3bebefb48e5f086d072ad6062f6446b4fc42ec7a8 in / 
# Wed, 04 Sep 2024 22:25:54 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f19b11698292330b7d980ed50b0141417eec298d865e0c1b305ce7a8b80b572d`  
		Last Modified: Wed, 04 Sep 2024 22:30:11 GMT  
		Size: 33.1 MB (33122358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ee1834d6aa97efd9d43db3a50a5bb3dda4b08400d531f72579cadea051609e`  
		Last Modified: Fri, 06 Sep 2024 22:02:56 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9152281fc8ce1403b29050f252829939c461cf037d8b3491653f7eeee4ece43`  
		Last Modified: Fri, 06 Sep 2024 22:02:56 GMT  
		Size: 2.7 MB (2707191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e141823a412ee63afdae23f927aa51b3eb72dd45577cf194159595a77d4577e2`  
		Last Modified: Tue, 10 Sep 2024 00:53:10 GMT  
		Size: 1.3 MB (1323809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c8e76a6f99b8b59c45f2a7eea7a5ee3870791b1a3abe6679881522a171e998`  
		Last Modified: Tue, 10 Sep 2024 00:53:10 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc7d2a375bf95c80dfd28c577fb84d803a9bb9437dd19ebc1801f99fb035120`  
		Last Modified: Tue, 10 Sep 2024 00:53:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:3bd251857bd96c65b8ad1e08a21c64177e673356369ff7404be1ba2edac796b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4713e2ddd75a9c1fba28b6cf8191e2ed2cb6b5e47a06bcb2db95a9efbbc74fda`

```dockerfile
```

-	Layers:
	-	`sha256:ca0b1f85d6ea571ab124bed1c494d1d8fb6673a42d0cb794a3eb947b1e1f9b06`  
		Last Modified: Tue, 10 Sep 2024 00:53:10 GMT  
		Size: 2.3 MB (2285050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73f6f1fc8ce970b2f59c4b67cfef86ef3c1dc692d3e5b91930a0f834c2aa8286`  
		Last Modified: Tue, 10 Sep 2024 00:53:10 GMT  
		Size: 21.1 KB (21095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:a564ae9d7581535075625ac57d9c0b961354e9b4daba7c4b8081f9c94a7272cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30885604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0553326148f76a8da67990b40b3cda91d5eb09e6450645d355301f64cdd62ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 21:42:50 GMT
ADD file:728128617ba2b026c358eb266cd495be84354c4e5dc4ecc2953cb829190a4546 in / 
# Wed, 04 Sep 2024 21:42:52 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:95fe27c895a828dc681ee4a0cbea0264c47528dad525efdb9641a375666536bd`  
		Last Modified: Wed, 04 Sep 2024 21:47:41 GMT  
		Size: 27.5 MB (27490321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14930957f1690905df41f1da11505509319dd65a7de378761ed685a7f319746`  
		Last Modified: Fri, 06 Sep 2024 22:03:27 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0833ee43e72a5f44318da8b85bdf6aa1bb3bddf0fdd75dc5530531a126eb97`  
		Last Modified: Fri, 06 Sep 2024 22:03:27 GMT  
		Size: 2.2 MB (2155800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49ba017e9517b59a0101e268f88f7b430651242d3de79201588254bb0fe7507`  
		Last Modified: Mon, 09 Sep 2024 23:57:11 GMT  
		Size: 1.2 MB (1237972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f824a2d96ada01e3ba546f908f36e9780321cfd73e3145903949cd6f8d9bbc`  
		Last Modified: Mon, 09 Sep 2024 23:57:11 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c979fb5ce067e0a4128dc5527a66b9ee1bf3762c94b5f309c473ede06b29be`  
		Last Modified: Mon, 09 Sep 2024 23:57:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:d96f09ec7f4c6e807df2fac9bd6834a30ab928672e82902cd5cc756d638221a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d39e3cfd9222897db8d98adeddedd43e35a75647f77cf2ca9276356feeb1695`

```dockerfile
```

-	Layers:
	-	`sha256:d83c73c94a489231e85f509c8c17651508a61d8aa02ef340f03babd8b3a5253b`  
		Last Modified: Mon, 09 Sep 2024 23:57:11 GMT  
		Size: 2.3 MB (2280500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b7064082e2a2543d417d8956bcd38d8aa02707fd3284afe698b5e0c00f111b1`  
		Last Modified: Mon, 09 Sep 2024 23:57:11 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6`

```console
$ docker pull memcached@sha256:51cdb01f624e1eab205f978b21756cf3ef96ca33da2cd074cb47245b92e0705f
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

### `memcached:1.6` - linux; amd64

```console
$ docker pull memcached@sha256:a658d819b6f9ab244148f9e9994489e759ff72e12cd2a93cf0a9b0259f324743
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32878406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a783d40c8b808e6a5c1d562c8ddf24732920c2c1b7e12eadaeb76b3f1e468b32`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 07 Sep 2024 18:54:11 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d937ff39f058bf2417a4fe760827ff36b1b38be77ed6c3b27fbd80872b4106b9`  
		Last Modified: Fri, 27 Sep 2024 06:05:04 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2bb47e18c2052b1e07d1957f90f1d197fcbf398748e534e8fa54f75782b3fff`  
		Last Modified: Fri, 27 Sep 2024 06:05:04 GMT  
		Size: 2.5 MB (2491322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c618990832780ea1a130f360744ad52c95ef7485138ded320b5563aedc090b`  
		Last Modified: Fri, 27 Sep 2024 06:05:04 GMT  
		Size: 1.3 MB (1259299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f09b0e04f54ca243201f3b8f205c759c2892f6752f8e75aa84434ab4a4b330`  
		Last Modified: Fri, 27 Sep 2024 06:05:04 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2038e2b3f99ec442dfe1024270c1ad10a59fb8995060bc0a2e7a6831bbc48917`  
		Last Modified: Fri, 27 Sep 2024 06:05:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:2fbb3c4bddfc491f239cbe76e97dbd05fa35514c183e7fa4ac819cda30fd5acf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b83b1908356b5b8567c67431165b1c6e4a18a87b108cb329988349341ed52f3e`

```dockerfile
```

-	Layers:
	-	`sha256:e0ac909638f1cc11061867d2eca41aafdfd8ac0189cceb25a5aa9c4ff9c7f0fc`  
		Last Modified: Fri, 27 Sep 2024 06:05:04 GMT  
		Size: 2.3 MB (2280692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c438d6540bdc9adc9140d94352ea4200a10e7cfc1168f6b3c47c8202fe19ace1`  
		Last Modified: Fri, 27 Sep 2024 06:05:04 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm variant v5

```console
$ docker pull memcached@sha256:365ca3a58f4ec2be52314d56ca69b149210604be3008c503c731cf5f4a095f5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30222872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43b582780474a2688f3e337b9c5a04bcf5697372ab5e9377d88e069e75607247`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 21:48:32 GMT
ADD file:c162e60b24ef6aed489ba1986f407fd9ab4ace659e0e3e6759ffac7eb0b7f770 in / 
# Wed, 04 Sep 2024 21:48:32 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:44990bd21e0c5db65674bd030d12ea2461a14f2bb4007469bc2667c8535a8357`  
		Last Modified: Wed, 04 Sep 2024 21:51:32 GMT  
		Size: 26.9 MB (26887411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a8ee21aa62c2c20c62d17e0dd3670c4484279b7481df253ab7dea06579e38f6`  
		Last Modified: Thu, 05 Sep 2024 03:28:45 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e5212bff7c052802224f0dcd2c61c47f77a42869600109756dedd710f28915`  
		Last Modified: Thu, 05 Sep 2024 03:28:46 GMT  
		Size: 2.1 MB (2095647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0782223d771fbfcf1c9ed4475479f748c453dd6aa6dc53aa45361cd00224de57`  
		Last Modified: Tue, 10 Sep 2024 02:36:03 GMT  
		Size: 1.2 MB (1238299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530caa10c823e2b669f21afaf522a557d974f4ea259b23e29b5a88c357559aa9`  
		Last Modified: Tue, 10 Sep 2024 02:36:02 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2f95efd2295adb5abdb3e0e56c5d975248bcc1c4951cedbfc5f10c2480cb9c`  
		Last Modified: Tue, 10 Sep 2024 02:36:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:643f24e07712d430691849d647e01c9ba7828371296a20fbe49250e582c0fac2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8e2f351cd6f24d1550b56f8e379b3e6aef1289d89b131237317ca600e4d52a0`

```dockerfile
```

-	Layers:
	-	`sha256:6d0e93f21d109f38cd7d09c5fc37735dc06c58bfcc63c9e950d187b500196f7b`  
		Last Modified: Tue, 10 Sep 2024 02:36:03 GMT  
		Size: 2.3 MB (2284110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:877d052619f8f882ecca7bddd9b19ea3ac0aff81603a8e053c4cfef2c753b056`  
		Last Modified: Tue, 10 Sep 2024 02:36:02 GMT  
		Size: 21.2 KB (21169 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:875cd34f6465e3e8fa28ef5db4bfad8c176e1c0263daff0171fc9537b0ca3a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32767698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a91d45790f325414f2734648e019a463d8d1353ca9250b2700504151dcdfbbe0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:52 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Wed, 04 Sep 2024 21:39:53 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04865bf94e709891a3952f6be4719f98f7a66c94aeb7ca127b805a21559f233b`  
		Last Modified: Fri, 06 Sep 2024 22:18:47 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2accb5dc3319c683f0fcfa968e975b4170700c037764eba741ba2d1c52c8ad0a`  
		Last Modified: Fri, 06 Sep 2024 22:18:47 GMT  
		Size: 2.4 MB (2354829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099212eee1d8aedc74760284b20c722ff3262dfeebadb7801f18e140dd2a88c4`  
		Last Modified: Tue, 10 Sep 2024 05:26:27 GMT  
		Size: 1.3 MB (1254813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfbc137765c6a6be5ae31943c75d26fb8556d6f8d6dc7372cba395a51e9600c8`  
		Last Modified: Tue, 10 Sep 2024 05:26:27 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6847381e1607ee0f70837cb4d081424ec06929f39c8c350ff85944aef711304c`  
		Last Modified: Tue, 10 Sep 2024 05:26:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:56255e99acdfe342a7754928cb5ed717ab5f7372c48426d0dc8b1515d05a4b4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:336d6748c4ae106ed4adc2a8b4c756622427e4066c4aa1351246e7a0fe352da8`

```dockerfile
```

-	Layers:
	-	`sha256:29df9c8dc456cfd5983e243674508af61ff397da6d8d6a997e017e85a4e4266c`  
		Last Modified: Tue, 10 Sep 2024 05:26:27 GMT  
		Size: 2.3 MB (2280993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d304f0d86e38bf9bc9ed7714e76015b79876a10b2d8c67f081473bfdcabe377`  
		Last Modified: Tue, 10 Sep 2024 05:26:27 GMT  
		Size: 21.4 KB (21385 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; 386

```console
$ docker pull memcached@sha256:34dcfa089dd249a4df38d93bee834b8e9ef0f20fc783cc57beecc31eb4e04fcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33904516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7bacc013d82d74a63cc6ad50eec7918e02e35d93e1138cd7405cb396e80b5a3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 22:44:34 GMT
ADD file:1d96491aed0d3091aadb984e1dfe642343013348f4a1807a69e132efaed68030 in / 
# Wed, 04 Sep 2024 22:44:34 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c304282df09b425e8240f53c55110ac282ba801da157a805e4fdbdf8c832b376`  
		Last Modified: Wed, 04 Sep 2024 22:48:08 GMT  
		Size: 30.1 MB (30144294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6c5637a99c0d5bfbc04c2f481699f0ab6cbcf940efabacc33b17680528fcb1`  
		Last Modified: Mon, 09 Sep 2024 23:04:42 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7a2b527feff9ff4df7dcb2a0b26ec01a6fa914c48cfb3bba0d873a5f7ae189`  
		Last Modified: Mon, 09 Sep 2024 23:04:42 GMT  
		Size: 2.5 MB (2499306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d54ad1af4809e5533f75ab13f83a284e966f4bdf5df4880fba412f3fa6e415`  
		Last Modified: Mon, 09 Sep 2024 23:04:42 GMT  
		Size: 1.3 MB (1259401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:683954138ef3ece20193896fd5a5df2deb974514c9f939d749eb46c161f1e4f6`  
		Last Modified: Mon, 09 Sep 2024 23:04:42 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d4e2b90164f16b0893ff5354664d43d05f691e1ef4165d1f45889cfaa8bc68`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:5f5144206a28ac6d02a6064d09bef45ba19ea0e834380667b5252173fc1aee2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2298749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c582914882b6e0802c0ff6073312ad790deb59006c1edeeca6423351ecc04295`

```dockerfile
```

-	Layers:
	-	`sha256:08d010ee1407ba55007943c5783e18992fce487cf9fc06f1001a6c6ee139ad50`  
		Last Modified: Mon, 09 Sep 2024 23:04:42 GMT  
		Size: 2.3 MB (2277777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8dabd61e7f4bdb4bd9a53e403b676e865ad1ec09201180b76f03117a501c2d7`  
		Last Modified: Mon, 09 Sep 2024 23:04:42 GMT  
		Size: 21.0 KB (20972 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; mips64le

```console
$ docker pull memcached@sha256:6f842f8998fe08cfdcb13cd83a7d09dfee91b25ae8b6937b02702480c5c55d22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32323662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d5a34a6f646baa48f817d457c47eb9762e5066adc40bc80cded7232eacb00d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 22:15:45 GMT
ADD file:9ffa4d53a074e91efecf5e26e3b67077f46165e0d042c1e6cf1b93c531ed2bc4 in / 
# Wed, 04 Sep 2024 22:15:50 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:89502a0eae32ab684bc9df3d9922ee2874839b178a693286c4b866f5ca8e93f3`  
		Last Modified: Wed, 04 Sep 2024 22:24:11 GMT  
		Size: 29.1 MB (29125054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a544e9e80cb1c7ab6c5794cb1a0a4715aa0df1fd8437a0d771017c52f3e5f5`  
		Last Modified: Thu, 05 Sep 2024 11:18:11 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7605e144a412910a4194cfffafd5d127bc44e9b19ba5191b74df2cc6a267f2e0`  
		Last Modified: Thu, 05 Sep 2024 11:18:12 GMT  
		Size: 1.9 MB (1942689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92a7d1694bf26de03563c78b52328eeabf26a387feba7ff6fbb8bb253427f27`  
		Last Modified: Tue, 10 Sep 2024 02:25:37 GMT  
		Size: 1.3 MB (1254404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c99675ddde9651d74c5ef49e2a70ca2c3351852fb856272dfb9b5f328a69e31`  
		Last Modified: Tue, 10 Sep 2024 02:25:37 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859d2e9814139aaf71bc0d3cc5e5eecdba1d8f10c4cc0196aa46b58d2830bebe`  
		Last Modified: Tue, 10 Sep 2024 02:25:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:6c4530d40688ecfde5ff475267c0fd60f9d67cd7e23c5e177ae0e20937467413
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e60bb1c6684aec9c40b2deb99de2c399adb2682fdc6efecdd98aef1881475ac`

```dockerfile
```

-	Layers:
	-	`sha256:74c8d993dc8b0fbc1c7708b04cec649eac5a3f36f5bc171bc1d523edc126aeff`  
		Last Modified: Tue, 10 Sep 2024 02:25:37 GMT  
		Size: 20.9 KB (20911 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; ppc64le

```console
$ docker pull memcached@sha256:a2c15d4ae7e15fa7457c5f843feb6bfc17bf3a4ee8c7fe278e9af0824a54be80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37154878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4f56f782d0ddfeacfa04a2d1bc62b4ee9938d6128b8c29f12647454f427251e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 22:25:52 GMT
ADD file:d83b2f8d4d3fd22a390140e3bebefb48e5f086d072ad6062f6446b4fc42ec7a8 in / 
# Wed, 04 Sep 2024 22:25:54 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f19b11698292330b7d980ed50b0141417eec298d865e0c1b305ce7a8b80b572d`  
		Last Modified: Wed, 04 Sep 2024 22:30:11 GMT  
		Size: 33.1 MB (33122358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ee1834d6aa97efd9d43db3a50a5bb3dda4b08400d531f72579cadea051609e`  
		Last Modified: Fri, 06 Sep 2024 22:02:56 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9152281fc8ce1403b29050f252829939c461cf037d8b3491653f7eeee4ece43`  
		Last Modified: Fri, 06 Sep 2024 22:02:56 GMT  
		Size: 2.7 MB (2707191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e141823a412ee63afdae23f927aa51b3eb72dd45577cf194159595a77d4577e2`  
		Last Modified: Tue, 10 Sep 2024 00:53:10 GMT  
		Size: 1.3 MB (1323809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c8e76a6f99b8b59c45f2a7eea7a5ee3870791b1a3abe6679881522a171e998`  
		Last Modified: Tue, 10 Sep 2024 00:53:10 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc7d2a375bf95c80dfd28c577fb84d803a9bb9437dd19ebc1801f99fb035120`  
		Last Modified: Tue, 10 Sep 2024 00:53:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:3bd251857bd96c65b8ad1e08a21c64177e673356369ff7404be1ba2edac796b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4713e2ddd75a9c1fba28b6cf8191e2ed2cb6b5e47a06bcb2db95a9efbbc74fda`

```dockerfile
```

-	Layers:
	-	`sha256:ca0b1f85d6ea571ab124bed1c494d1d8fb6673a42d0cb794a3eb947b1e1f9b06`  
		Last Modified: Tue, 10 Sep 2024 00:53:10 GMT  
		Size: 2.3 MB (2285050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73f6f1fc8ce970b2f59c4b67cfef86ef3c1dc692d3e5b91930a0f834c2aa8286`  
		Last Modified: Tue, 10 Sep 2024 00:53:10 GMT  
		Size: 21.1 KB (21095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; s390x

```console
$ docker pull memcached@sha256:a564ae9d7581535075625ac57d9c0b961354e9b4daba7c4b8081f9c94a7272cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30885604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0553326148f76a8da67990b40b3cda91d5eb09e6450645d355301f64cdd62ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 21:42:50 GMT
ADD file:728128617ba2b026c358eb266cd495be84354c4e5dc4ecc2953cb829190a4546 in / 
# Wed, 04 Sep 2024 21:42:52 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:95fe27c895a828dc681ee4a0cbea0264c47528dad525efdb9641a375666536bd`  
		Last Modified: Wed, 04 Sep 2024 21:47:41 GMT  
		Size: 27.5 MB (27490321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14930957f1690905df41f1da11505509319dd65a7de378761ed685a7f319746`  
		Last Modified: Fri, 06 Sep 2024 22:03:27 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0833ee43e72a5f44318da8b85bdf6aa1bb3bddf0fdd75dc5530531a126eb97`  
		Last Modified: Fri, 06 Sep 2024 22:03:27 GMT  
		Size: 2.2 MB (2155800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49ba017e9517b59a0101e268f88f7b430651242d3de79201588254bb0fe7507`  
		Last Modified: Mon, 09 Sep 2024 23:57:11 GMT  
		Size: 1.2 MB (1237972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f824a2d96ada01e3ba546f908f36e9780321cfd73e3145903949cd6f8d9bbc`  
		Last Modified: Mon, 09 Sep 2024 23:57:11 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c979fb5ce067e0a4128dc5527a66b9ee1bf3762c94b5f309c473ede06b29be`  
		Last Modified: Mon, 09 Sep 2024 23:57:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:d96f09ec7f4c6e807df2fac9bd6834a30ab928672e82902cd5cc756d638221a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d39e3cfd9222897db8d98adeddedd43e35a75647f77cf2ca9276356feeb1695`

```dockerfile
```

-	Layers:
	-	`sha256:d83c73c94a489231e85f509c8c17651508a61d8aa02ef340f03babd8b3a5253b`  
		Last Modified: Mon, 09 Sep 2024 23:57:11 GMT  
		Size: 2.3 MB (2280500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b7064082e2a2543d417d8956bcd38d8aa02707fd3284afe698b5e0c00f111b1`  
		Last Modified: Mon, 09 Sep 2024 23:57:11 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine`

```console
$ docker pull memcached@sha256:6fff88e239680465aa0b7e977b2f1a322471c3552644159371de6c1731a5014a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `memcached:1.6-alpine` - linux; amd64

```console
$ docker pull memcached@sha256:bc62c9b146672d0f63f0b3a38722acae32e859f635e6f32f0b31afdcb1013c7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4687755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aae0d824f4bc7874b3fd26fc5e61b2fe8c3fc9b58f82f3be24a6010c05ec1c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e2704d07ea50e4350fc30a778f91c517bee857b54bcc571b464e2b563744ab`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f89cbdbe5025b3c7d2ff8f9f6bfbb7bcd639adb35200de6f0b8b4515488f1b05`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 103.8 KB (103822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f139dbcb2579cd1e9f78db09fd279e08d323c219a6efcad878b42cd961d24a25`  
		Last Modified: Mon, 09 Sep 2024 23:04:31 GMT  
		Size: 958.8 KB (958765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3487c95e4eb9d8fb5506b2cd3406c02c1fba592fbafe1078c141420c22939fc7`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eaf1d2da7366110dda884212201a67c62fb0f9c921217de86755d35b80fbee9`  
		Last Modified: Mon, 09 Sep 2024 23:04:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:c96c825ac5a6f1db0849694d7878693b7113126e5c85540cdb4e191454d0afcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 KB (107135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a3dddb2bd6769fc79a77da8e93edcfe6d98d55badebcebbc9faaecb661ad001`

```dockerfile
```

-	Layers:
	-	`sha256:7102ff71a3580f59d96136c579e83bbb7e913951d315d57f5d15541dc8438bdb`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 87.8 KB (87785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e083725668b94672a9a645717ffd665a9f0059d9823eed6b8b1bc89bee285c4e`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 19.4 KB (19350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:a2d38a957041270c55d551e8ecf53f69df6613a17df3fb1876ab6fb65cd99ea6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5172731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3954249ac508b8b8c4a968b394a6970e8d868f1744e672affe792ee9231b39ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04310511d0b87f77a431a5f50ac0c3d95896d6a39a16aa043ba443f6b0e0fddd`  
		Last Modified: Sat, 07 Sep 2024 05:30:38 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b28609c2d169047004bf72890ec5ac9e3a88bd3aa153e465bf17c14f3ebf3b`  
		Last Modified: Sat, 07 Sep 2024 05:30:38 GMT  
		Size: 121.0 KB (121024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4adf4e4f7be512c6272c74db833112894b8410062060f6888539171290372a82`  
		Last Modified: Tue, 10 Sep 2024 05:30:03 GMT  
		Size: 962.7 KB (962700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c043e4b98daae0158835eeb78946255c4027b9ebe97d5e569fa8f1df39119c7`  
		Last Modified: Tue, 10 Sep 2024 05:30:03 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e243cd97c138165f622734a969475116f77deb0f3c6efaf70fae4ac39ebbffc`  
		Last Modified: Tue, 10 Sep 2024 05:30:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:9d2c6d970fa941ac951ded01e253b2d4492d8bda51fd29bc2f6915310f884231
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0bc6ae2b075b905b17704735488c6da23574abab2bbc1bb4aefebbe65768955`

```dockerfile
```

-	Layers:
	-	`sha256:36cf7adc241f552244e6d64628168a1dee985ba7a3176282286b5ca13998f243`  
		Last Modified: Tue, 10 Sep 2024 05:30:02 GMT  
		Size: 87.9 KB (87889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90b01e0840b58a8d84f085ca69e1f3f3eb1fd0a0abd8b42fca270e09451e6161`  
		Last Modified: Tue, 10 Sep 2024 05:30:02 GMT  
		Size: 19.7 KB (19698 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; 386

```console
$ docker pull memcached@sha256:7228773d86ac6e8955e5d2d7ffefc2ae564b00cadd0c858310dec50e9fad6f42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4531177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41f22aace0957bde9cbc95b95320e1836991afac8a43e215d16ef141508788c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:41:21 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Fri, 06 Sep 2024 22:41:21 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e2704d07ea50e4350fc30a778f91c517bee857b54bcc571b464e2b563744ab`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef4ec43894c33c1d68e1fbb24d27f314125a8617ada637af061725989f14953`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 109.0 KB (108961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b19ce951cfcb336fa2050f3422e487f515d16ddcf2c69c80d29d9f66baa9d16e`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 951.7 KB (951692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cfaaa1bc534e7c46c1b3aa67465a41ca91d4ce83071caebc7a11e3ff143be02`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0615a81d8e335acdc6d68eefcf35b5d516a3cc0ed68bac6adfd5807799b53f46`  
		Last Modified: Mon, 09 Sep 2024 23:04:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7940458999ce753465ef3f968a9eabac518a9df3d5d77386552d3526c2b946ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.0 KB (107035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e2e327ed8d984210e8a47612bf76565fb47b80c1d0e63bbc53b45c571fd09f9`

```dockerfile
```

-	Layers:
	-	`sha256:c1c9fcdee5d34fae3276a06573fa1e3d9a3a0b6d532765266d4e86f6be9a695b`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 87.7 KB (87740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12c78394468356d9d60cea99380a31c53b12f50a43699c3916eda41ba6ee3470`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 19.3 KB (19295 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:517da247dc00201621112cd48487139ce6966636899a4c40fdb02b307f3f1b5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4694177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98eb649600a0e4277874d7abade7034b99d425dcb34c55e165f11569d4166b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:06 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 22:26:07 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645d78667a8075f56004a7a283eaeb1a630309a9d950a27de5cc29eb72cec340`  
		Last Modified: Sat, 07 Sep 2024 07:05:29 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5844b90ee5623766614a832d5e5f322566849ed5853adfbe1f63e8d954b540d9`  
		Last Modified: Sat, 07 Sep 2024 07:05:29 GMT  
		Size: 123.0 KB (123003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b715436c927b60842b1c1f98f7cb7c4257838f7b36a5e2334b5f590ca152f6`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 997.4 KB (997389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ad232e17fce60e215c458fcac12f4ac1d5bdd60080527a4c28d76c6c831393`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8e18c99726667f58640d52458967d66a4da28b7f2eaaac5626723a6691ed45`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:e4e8b6df3a60e291797c10897a7779345a41715ab61dfd7f76bccdc42ef8a7ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 KB (105307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469f18677668b4dd9a3de113d4ae3f111f5b89e03f3795cef6eab0e1e3eecbbe`

```dockerfile
```

-	Layers:
	-	`sha256:f7beb1e9f1753005bac3249d305c8567220853e93353216074762ad7f1813c0a`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 85.9 KB (85889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2eea735dc745320130c1139867abe3e0b71de840a5a8a3170b9191994b69b01b`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 19.4 KB (19418 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:ceffb56b913ca8a62831ef271642b11ddbeea098de65d093af55cbba0f8d56e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4427664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c258ae7e36ddd3758d8ddff147c4db3f4928f4db92f67bc7b91ffa68c86d4ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:cdf7088bbd70519f0f5d7b4249df34386e40f0194752f45842b3d85f2d331cf5 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["/bin/sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:faf447acae27573624c0613a79c4bcf1f9bc46d29f523140352abfd3f7691282`  
		Last Modified: Mon, 22 Jul 2024 22:21:18 GMT  
		Size: 3.4 MB (3370673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230af89e5f8d3eec0e6d96c87e99a85b938e0722dacebe0009ad7b8b00ca320b`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c75b82861f48f0052a86f16f944c0324ed20af856a4c9d87c147dc645460ee6`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 108.6 KB (108596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d23c6553fa0ff65e57ebc39080a958cc4d1d02587781c94836137d124c47ce`  
		Last Modified: Sun, 28 Jul 2024 15:58:50 GMT  
		Size: 947.0 KB (947030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab42ab26d315472c0f9433b5c7f25e0e426c020b3b0e8cc52d1c7d09ca7bf91`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e436e8ed56076dff056e7dc989a1944739cb23a96400a543900ab3bd07a77b6`  
		Last Modified: Sun, 28 Jul 2024 15:58:50 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:fdf92c6c75f08244e376b28b33307c9ea75a07f7523b56b86df44f1be3335f3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 KB (105303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc24bdd15449aa6c8213cd2607de7998a598edba9ca2fb7de80b4b761b833a64`

```dockerfile
```

-	Layers:
	-	`sha256:dbb3dc8245856acbf66987c1cd0f4f37d8af7b49bc0c7b8eaacfb02321594ac5`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 85.9 KB (85885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2359a9107230c13ad5d1c580fc348790129c58ea95b407db376ee7eb5a109571`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 19.4 KB (19418 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:a6f8155d863aa33eae871b75e7543c04404c30248007928840beeffae2eb5e78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4556594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63fcf33c45f689bdee882ed4ad8692b55a55abe13941eb4cc525adeafab650c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:17 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 22:48:17 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc58d10317d926d80ab2de5020728ade9434725004663fce6207d95ecc3ba0c`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed425e517c8a02d89379669853a47dbd343281c3fcfc3e37f91b671f0b35ffc`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 112.7 KB (112740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02fe29c4e792447391a38d4b9d7aa18f9a51d6f171eb15297a427efb6a33e839`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 980.9 KB (980896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fffd060f2e26e85750706fd829abf92d787fdf9321cba829cab93f30845547f`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93825c9e15b3ee5a0f3ebddccf232551b4506353af049da3e37f7ae97e39a384`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:5c62ae13354b08074917592e56f436a96d4ccf47cbf5c4a13231f53d556be814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 KB (105181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fda0c239bf944625a0bd5aeea27175b74c697a79c4b068f9d8e137b786a2b4a4`

```dockerfile
```

-	Layers:
	-	`sha256:870d5efdd4242eb6cc01519cd2092666c5ab15b546cb69d2711791408721605b`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 85.8 KB (85831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dbbbb69edb2b376c21146fd5c88b6254433cc9264976b2868973688bb8a95cf`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 19.4 KB (19350 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine3.20`

```console
$ docker pull memcached@sha256:6fff88e239680465aa0b7e977b2f1a322471c3552644159371de6c1731a5014a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `memcached:1.6-alpine3.20` - linux; amd64

```console
$ docker pull memcached@sha256:bc62c9b146672d0f63f0b3a38722acae32e859f635e6f32f0b31afdcb1013c7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4687755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aae0d824f4bc7874b3fd26fc5e61b2fe8c3fc9b58f82f3be24a6010c05ec1c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e2704d07ea50e4350fc30a778f91c517bee857b54bcc571b464e2b563744ab`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f89cbdbe5025b3c7d2ff8f9f6bfbb7bcd639adb35200de6f0b8b4515488f1b05`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 103.8 KB (103822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f139dbcb2579cd1e9f78db09fd279e08d323c219a6efcad878b42cd961d24a25`  
		Last Modified: Mon, 09 Sep 2024 23:04:31 GMT  
		Size: 958.8 KB (958765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3487c95e4eb9d8fb5506b2cd3406c02c1fba592fbafe1078c141420c22939fc7`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eaf1d2da7366110dda884212201a67c62fb0f9c921217de86755d35b80fbee9`  
		Last Modified: Mon, 09 Sep 2024 23:04:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:c96c825ac5a6f1db0849694d7878693b7113126e5c85540cdb4e191454d0afcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 KB (107135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a3dddb2bd6769fc79a77da8e93edcfe6d98d55badebcebbc9faaecb661ad001`

```dockerfile
```

-	Layers:
	-	`sha256:7102ff71a3580f59d96136c579e83bbb7e913951d315d57f5d15541dc8438bdb`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 87.8 KB (87785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e083725668b94672a9a645717ffd665a9f0059d9823eed6b8b1bc89bee285c4e`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 19.4 KB (19350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:a2d38a957041270c55d551e8ecf53f69df6613a17df3fb1876ab6fb65cd99ea6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5172731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3954249ac508b8b8c4a968b394a6970e8d868f1744e672affe792ee9231b39ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04310511d0b87f77a431a5f50ac0c3d95896d6a39a16aa043ba443f6b0e0fddd`  
		Last Modified: Sat, 07 Sep 2024 05:30:38 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b28609c2d169047004bf72890ec5ac9e3a88bd3aa153e465bf17c14f3ebf3b`  
		Last Modified: Sat, 07 Sep 2024 05:30:38 GMT  
		Size: 121.0 KB (121024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4adf4e4f7be512c6272c74db833112894b8410062060f6888539171290372a82`  
		Last Modified: Tue, 10 Sep 2024 05:30:03 GMT  
		Size: 962.7 KB (962700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c043e4b98daae0158835eeb78946255c4027b9ebe97d5e569fa8f1df39119c7`  
		Last Modified: Tue, 10 Sep 2024 05:30:03 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e243cd97c138165f622734a969475116f77deb0f3c6efaf70fae4ac39ebbffc`  
		Last Modified: Tue, 10 Sep 2024 05:30:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:9d2c6d970fa941ac951ded01e253b2d4492d8bda51fd29bc2f6915310f884231
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0bc6ae2b075b905b17704735488c6da23574abab2bbc1bb4aefebbe65768955`

```dockerfile
```

-	Layers:
	-	`sha256:36cf7adc241f552244e6d64628168a1dee985ba7a3176282286b5ca13998f243`  
		Last Modified: Tue, 10 Sep 2024 05:30:02 GMT  
		Size: 87.9 KB (87889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90b01e0840b58a8d84f085ca69e1f3f3eb1fd0a0abd8b42fca270e09451e6161`  
		Last Modified: Tue, 10 Sep 2024 05:30:02 GMT  
		Size: 19.7 KB (19698 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.20` - linux; 386

```console
$ docker pull memcached@sha256:7228773d86ac6e8955e5d2d7ffefc2ae564b00cadd0c858310dec50e9fad6f42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4531177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41f22aace0957bde9cbc95b95320e1836991afac8a43e215d16ef141508788c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:41:21 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Fri, 06 Sep 2024 22:41:21 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e2704d07ea50e4350fc30a778f91c517bee857b54bcc571b464e2b563744ab`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef4ec43894c33c1d68e1fbb24d27f314125a8617ada637af061725989f14953`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 109.0 KB (108961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b19ce951cfcb336fa2050f3422e487f515d16ddcf2c69c80d29d9f66baa9d16e`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 951.7 KB (951692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cfaaa1bc534e7c46c1b3aa67465a41ca91d4ce83071caebc7a11e3ff143be02`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0615a81d8e335acdc6d68eefcf35b5d516a3cc0ed68bac6adfd5807799b53f46`  
		Last Modified: Mon, 09 Sep 2024 23:04:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:7940458999ce753465ef3f968a9eabac518a9df3d5d77386552d3526c2b946ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.0 KB (107035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e2e327ed8d984210e8a47612bf76565fb47b80c1d0e63bbc53b45c571fd09f9`

```dockerfile
```

-	Layers:
	-	`sha256:c1c9fcdee5d34fae3276a06573fa1e3d9a3a0b6d532765266d4e86f6be9a695b`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 87.7 KB (87740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12c78394468356d9d60cea99380a31c53b12f50a43699c3916eda41ba6ee3470`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 19.3 KB (19295 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.20` - linux; ppc64le

```console
$ docker pull memcached@sha256:517da247dc00201621112cd48487139ce6966636899a4c40fdb02b307f3f1b5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4694177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98eb649600a0e4277874d7abade7034b99d425dcb34c55e165f11569d4166b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:06 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 22:26:07 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645d78667a8075f56004a7a283eaeb1a630309a9d950a27de5cc29eb72cec340`  
		Last Modified: Sat, 07 Sep 2024 07:05:29 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5844b90ee5623766614a832d5e5f322566849ed5853adfbe1f63e8d954b540d9`  
		Last Modified: Sat, 07 Sep 2024 07:05:29 GMT  
		Size: 123.0 KB (123003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b715436c927b60842b1c1f98f7cb7c4257838f7b36a5e2334b5f590ca152f6`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 997.4 KB (997389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ad232e17fce60e215c458fcac12f4ac1d5bdd60080527a4c28d76c6c831393`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8e18c99726667f58640d52458967d66a4da28b7f2eaaac5626723a6691ed45`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:e4e8b6df3a60e291797c10897a7779345a41715ab61dfd7f76bccdc42ef8a7ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 KB (105307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469f18677668b4dd9a3de113d4ae3f111f5b89e03f3795cef6eab0e1e3eecbbe`

```dockerfile
```

-	Layers:
	-	`sha256:f7beb1e9f1753005bac3249d305c8567220853e93353216074762ad7f1813c0a`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 85.9 KB (85889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2eea735dc745320130c1139867abe3e0b71de840a5a8a3170b9191994b69b01b`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 19.4 KB (19418 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.20` - linux; riscv64

```console
$ docker pull memcached@sha256:ceffb56b913ca8a62831ef271642b11ddbeea098de65d093af55cbba0f8d56e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4427664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c258ae7e36ddd3758d8ddff147c4db3f4928f4db92f67bc7b91ffa68c86d4ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:cdf7088bbd70519f0f5d7b4249df34386e40f0194752f45842b3d85f2d331cf5 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["/bin/sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:faf447acae27573624c0613a79c4bcf1f9bc46d29f523140352abfd3f7691282`  
		Last Modified: Mon, 22 Jul 2024 22:21:18 GMT  
		Size: 3.4 MB (3370673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230af89e5f8d3eec0e6d96c87e99a85b938e0722dacebe0009ad7b8b00ca320b`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c75b82861f48f0052a86f16f944c0324ed20af856a4c9d87c147dc645460ee6`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 108.6 KB (108596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d23c6553fa0ff65e57ebc39080a958cc4d1d02587781c94836137d124c47ce`  
		Last Modified: Sun, 28 Jul 2024 15:58:50 GMT  
		Size: 947.0 KB (947030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab42ab26d315472c0f9433b5c7f25e0e426c020b3b0e8cc52d1c7d09ca7bf91`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e436e8ed56076dff056e7dc989a1944739cb23a96400a543900ab3bd07a77b6`  
		Last Modified: Sun, 28 Jul 2024 15:58:50 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:fdf92c6c75f08244e376b28b33307c9ea75a07f7523b56b86df44f1be3335f3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 KB (105303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc24bdd15449aa6c8213cd2607de7998a598edba9ca2fb7de80b4b761b833a64`

```dockerfile
```

-	Layers:
	-	`sha256:dbb3dc8245856acbf66987c1cd0f4f37d8af7b49bc0c7b8eaacfb02321594ac5`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 85.9 KB (85885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2359a9107230c13ad5d1c580fc348790129c58ea95b407db376ee7eb5a109571`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 19.4 KB (19418 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.20` - linux; s390x

```console
$ docker pull memcached@sha256:a6f8155d863aa33eae871b75e7543c04404c30248007928840beeffae2eb5e78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4556594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63fcf33c45f689bdee882ed4ad8692b55a55abe13941eb4cc525adeafab650c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:17 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 22:48:17 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc58d10317d926d80ab2de5020728ade9434725004663fce6207d95ecc3ba0c`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed425e517c8a02d89379669853a47dbd343281c3fcfc3e37f91b671f0b35ffc`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 112.7 KB (112740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02fe29c4e792447391a38d4b9d7aa18f9a51d6f171eb15297a427efb6a33e839`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 980.9 KB (980896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fffd060f2e26e85750706fd829abf92d787fdf9321cba829cab93f30845547f`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93825c9e15b3ee5a0f3ebddccf232551b4506353af049da3e37f7ae97e39a384`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:5c62ae13354b08074917592e56f436a96d4ccf47cbf5c4a13231f53d556be814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 KB (105181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fda0c239bf944625a0bd5aeea27175b74c697a79c4b068f9d8e137b786a2b4a4`

```dockerfile
```

-	Layers:
	-	`sha256:870d5efdd4242eb6cc01519cd2092666c5ab15b546cb69d2711791408721605b`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 85.8 KB (85831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dbbbb69edb2b376c21146fd5c88b6254433cc9264976b2868973688bb8a95cf`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 19.4 KB (19350 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-bookworm`

```console
$ docker pull memcached@sha256:51cdb01f624e1eab205f978b21756cf3ef96ca33da2cd074cb47245b92e0705f
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

### `memcached:1.6-bookworm` - linux; amd64

```console
$ docker pull memcached@sha256:a658d819b6f9ab244148f9e9994489e759ff72e12cd2a93cf0a9b0259f324743
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32878406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a783d40c8b808e6a5c1d562c8ddf24732920c2c1b7e12eadaeb76b3f1e468b32`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 07 Sep 2024 18:54:11 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d937ff39f058bf2417a4fe760827ff36b1b38be77ed6c3b27fbd80872b4106b9`  
		Last Modified: Fri, 27 Sep 2024 06:05:04 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2bb47e18c2052b1e07d1957f90f1d197fcbf398748e534e8fa54f75782b3fff`  
		Last Modified: Fri, 27 Sep 2024 06:05:04 GMT  
		Size: 2.5 MB (2491322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c618990832780ea1a130f360744ad52c95ef7485138ded320b5563aedc090b`  
		Last Modified: Fri, 27 Sep 2024 06:05:04 GMT  
		Size: 1.3 MB (1259299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f09b0e04f54ca243201f3b8f205c759c2892f6752f8e75aa84434ab4a4b330`  
		Last Modified: Fri, 27 Sep 2024 06:05:04 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2038e2b3f99ec442dfe1024270c1ad10a59fb8995060bc0a2e7a6831bbc48917`  
		Last Modified: Fri, 27 Sep 2024 06:05:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:2fbb3c4bddfc491f239cbe76e97dbd05fa35514c183e7fa4ac819cda30fd5acf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b83b1908356b5b8567c67431165b1c6e4a18a87b108cb329988349341ed52f3e`

```dockerfile
```

-	Layers:
	-	`sha256:e0ac909638f1cc11061867d2eca41aafdfd8ac0189cceb25a5aa9c4ff9c7f0fc`  
		Last Modified: Fri, 27 Sep 2024 06:05:04 GMT  
		Size: 2.3 MB (2280692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c438d6540bdc9adc9140d94352ea4200a10e7cfc1168f6b3c47c8202fe19ace1`  
		Last Modified: Fri, 27 Sep 2024 06:05:04 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:365ca3a58f4ec2be52314d56ca69b149210604be3008c503c731cf5f4a095f5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30222872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43b582780474a2688f3e337b9c5a04bcf5697372ab5e9377d88e069e75607247`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 21:48:32 GMT
ADD file:c162e60b24ef6aed489ba1986f407fd9ab4ace659e0e3e6759ffac7eb0b7f770 in / 
# Wed, 04 Sep 2024 21:48:32 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:44990bd21e0c5db65674bd030d12ea2461a14f2bb4007469bc2667c8535a8357`  
		Last Modified: Wed, 04 Sep 2024 21:51:32 GMT  
		Size: 26.9 MB (26887411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a8ee21aa62c2c20c62d17e0dd3670c4484279b7481df253ab7dea06579e38f6`  
		Last Modified: Thu, 05 Sep 2024 03:28:45 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e5212bff7c052802224f0dcd2c61c47f77a42869600109756dedd710f28915`  
		Last Modified: Thu, 05 Sep 2024 03:28:46 GMT  
		Size: 2.1 MB (2095647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0782223d771fbfcf1c9ed4475479f748c453dd6aa6dc53aa45361cd00224de57`  
		Last Modified: Tue, 10 Sep 2024 02:36:03 GMT  
		Size: 1.2 MB (1238299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530caa10c823e2b669f21afaf522a557d974f4ea259b23e29b5a88c357559aa9`  
		Last Modified: Tue, 10 Sep 2024 02:36:02 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2f95efd2295adb5abdb3e0e56c5d975248bcc1c4951cedbfc5f10c2480cb9c`  
		Last Modified: Tue, 10 Sep 2024 02:36:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:643f24e07712d430691849d647e01c9ba7828371296a20fbe49250e582c0fac2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8e2f351cd6f24d1550b56f8e379b3e6aef1289d89b131237317ca600e4d52a0`

```dockerfile
```

-	Layers:
	-	`sha256:6d0e93f21d109f38cd7d09c5fc37735dc06c58bfcc63c9e950d187b500196f7b`  
		Last Modified: Tue, 10 Sep 2024 02:36:03 GMT  
		Size: 2.3 MB (2284110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:877d052619f8f882ecca7bddd9b19ea3ac0aff81603a8e053c4cfef2c753b056`  
		Last Modified: Tue, 10 Sep 2024 02:36:02 GMT  
		Size: 21.2 KB (21169 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:875cd34f6465e3e8fa28ef5db4bfad8c176e1c0263daff0171fc9537b0ca3a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32767698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a91d45790f325414f2734648e019a463d8d1353ca9250b2700504151dcdfbbe0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:52 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Wed, 04 Sep 2024 21:39:53 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04865bf94e709891a3952f6be4719f98f7a66c94aeb7ca127b805a21559f233b`  
		Last Modified: Fri, 06 Sep 2024 22:18:47 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2accb5dc3319c683f0fcfa968e975b4170700c037764eba741ba2d1c52c8ad0a`  
		Last Modified: Fri, 06 Sep 2024 22:18:47 GMT  
		Size: 2.4 MB (2354829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099212eee1d8aedc74760284b20c722ff3262dfeebadb7801f18e140dd2a88c4`  
		Last Modified: Tue, 10 Sep 2024 05:26:27 GMT  
		Size: 1.3 MB (1254813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfbc137765c6a6be5ae31943c75d26fb8556d6f8d6dc7372cba395a51e9600c8`  
		Last Modified: Tue, 10 Sep 2024 05:26:27 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6847381e1607ee0f70837cb4d081424ec06929f39c8c350ff85944aef711304c`  
		Last Modified: Tue, 10 Sep 2024 05:26:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:56255e99acdfe342a7754928cb5ed717ab5f7372c48426d0dc8b1515d05a4b4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:336d6748c4ae106ed4adc2a8b4c756622427e4066c4aa1351246e7a0fe352da8`

```dockerfile
```

-	Layers:
	-	`sha256:29df9c8dc456cfd5983e243674508af61ff397da6d8d6a997e017e85a4e4266c`  
		Last Modified: Tue, 10 Sep 2024 05:26:27 GMT  
		Size: 2.3 MB (2280993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d304f0d86e38bf9bc9ed7714e76015b79876a10b2d8c67f081473bfdcabe377`  
		Last Modified: Tue, 10 Sep 2024 05:26:27 GMT  
		Size: 21.4 KB (21385 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:34dcfa089dd249a4df38d93bee834b8e9ef0f20fc783cc57beecc31eb4e04fcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33904516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7bacc013d82d74a63cc6ad50eec7918e02e35d93e1138cd7405cb396e80b5a3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 22:44:34 GMT
ADD file:1d96491aed0d3091aadb984e1dfe642343013348f4a1807a69e132efaed68030 in / 
# Wed, 04 Sep 2024 22:44:34 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c304282df09b425e8240f53c55110ac282ba801da157a805e4fdbdf8c832b376`  
		Last Modified: Wed, 04 Sep 2024 22:48:08 GMT  
		Size: 30.1 MB (30144294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6c5637a99c0d5bfbc04c2f481699f0ab6cbcf940efabacc33b17680528fcb1`  
		Last Modified: Mon, 09 Sep 2024 23:04:42 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7a2b527feff9ff4df7dcb2a0b26ec01a6fa914c48cfb3bba0d873a5f7ae189`  
		Last Modified: Mon, 09 Sep 2024 23:04:42 GMT  
		Size: 2.5 MB (2499306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d54ad1af4809e5533f75ab13f83a284e966f4bdf5df4880fba412f3fa6e415`  
		Last Modified: Mon, 09 Sep 2024 23:04:42 GMT  
		Size: 1.3 MB (1259401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:683954138ef3ece20193896fd5a5df2deb974514c9f939d749eb46c161f1e4f6`  
		Last Modified: Mon, 09 Sep 2024 23:04:42 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d4e2b90164f16b0893ff5354664d43d05f691e1ef4165d1f45889cfaa8bc68`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:5f5144206a28ac6d02a6064d09bef45ba19ea0e834380667b5252173fc1aee2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2298749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c582914882b6e0802c0ff6073312ad790deb59006c1edeeca6423351ecc04295`

```dockerfile
```

-	Layers:
	-	`sha256:08d010ee1407ba55007943c5783e18992fce487cf9fc06f1001a6c6ee139ad50`  
		Last Modified: Mon, 09 Sep 2024 23:04:42 GMT  
		Size: 2.3 MB (2277777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8dabd61e7f4bdb4bd9a53e403b676e865ad1ec09201180b76f03117a501c2d7`  
		Last Modified: Mon, 09 Sep 2024 23:04:42 GMT  
		Size: 21.0 KB (20972 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:6f842f8998fe08cfdcb13cd83a7d09dfee91b25ae8b6937b02702480c5c55d22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32323662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d5a34a6f646baa48f817d457c47eb9762e5066adc40bc80cded7232eacb00d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 22:15:45 GMT
ADD file:9ffa4d53a074e91efecf5e26e3b67077f46165e0d042c1e6cf1b93c531ed2bc4 in / 
# Wed, 04 Sep 2024 22:15:50 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:89502a0eae32ab684bc9df3d9922ee2874839b178a693286c4b866f5ca8e93f3`  
		Last Modified: Wed, 04 Sep 2024 22:24:11 GMT  
		Size: 29.1 MB (29125054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a544e9e80cb1c7ab6c5794cb1a0a4715aa0df1fd8437a0d771017c52f3e5f5`  
		Last Modified: Thu, 05 Sep 2024 11:18:11 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7605e144a412910a4194cfffafd5d127bc44e9b19ba5191b74df2cc6a267f2e0`  
		Last Modified: Thu, 05 Sep 2024 11:18:12 GMT  
		Size: 1.9 MB (1942689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92a7d1694bf26de03563c78b52328eeabf26a387feba7ff6fbb8bb253427f27`  
		Last Modified: Tue, 10 Sep 2024 02:25:37 GMT  
		Size: 1.3 MB (1254404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c99675ddde9651d74c5ef49e2a70ca2c3351852fb856272dfb9b5f328a69e31`  
		Last Modified: Tue, 10 Sep 2024 02:25:37 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859d2e9814139aaf71bc0d3cc5e5eecdba1d8f10c4cc0196aa46b58d2830bebe`  
		Last Modified: Tue, 10 Sep 2024 02:25:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:6c4530d40688ecfde5ff475267c0fd60f9d67cd7e23c5e177ae0e20937467413
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e60bb1c6684aec9c40b2deb99de2c399adb2682fdc6efecdd98aef1881475ac`

```dockerfile
```

-	Layers:
	-	`sha256:74c8d993dc8b0fbc1c7708b04cec649eac5a3f36f5bc171bc1d523edc126aeff`  
		Last Modified: Tue, 10 Sep 2024 02:25:37 GMT  
		Size: 20.9 KB (20911 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:a2c15d4ae7e15fa7457c5f843feb6bfc17bf3a4ee8c7fe278e9af0824a54be80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37154878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4f56f782d0ddfeacfa04a2d1bc62b4ee9938d6128b8c29f12647454f427251e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 22:25:52 GMT
ADD file:d83b2f8d4d3fd22a390140e3bebefb48e5f086d072ad6062f6446b4fc42ec7a8 in / 
# Wed, 04 Sep 2024 22:25:54 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f19b11698292330b7d980ed50b0141417eec298d865e0c1b305ce7a8b80b572d`  
		Last Modified: Wed, 04 Sep 2024 22:30:11 GMT  
		Size: 33.1 MB (33122358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ee1834d6aa97efd9d43db3a50a5bb3dda4b08400d531f72579cadea051609e`  
		Last Modified: Fri, 06 Sep 2024 22:02:56 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9152281fc8ce1403b29050f252829939c461cf037d8b3491653f7eeee4ece43`  
		Last Modified: Fri, 06 Sep 2024 22:02:56 GMT  
		Size: 2.7 MB (2707191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e141823a412ee63afdae23f927aa51b3eb72dd45577cf194159595a77d4577e2`  
		Last Modified: Tue, 10 Sep 2024 00:53:10 GMT  
		Size: 1.3 MB (1323809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c8e76a6f99b8b59c45f2a7eea7a5ee3870791b1a3abe6679881522a171e998`  
		Last Modified: Tue, 10 Sep 2024 00:53:10 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc7d2a375bf95c80dfd28c577fb84d803a9bb9437dd19ebc1801f99fb035120`  
		Last Modified: Tue, 10 Sep 2024 00:53:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:3bd251857bd96c65b8ad1e08a21c64177e673356369ff7404be1ba2edac796b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4713e2ddd75a9c1fba28b6cf8191e2ed2cb6b5e47a06bcb2db95a9efbbc74fda`

```dockerfile
```

-	Layers:
	-	`sha256:ca0b1f85d6ea571ab124bed1c494d1d8fb6673a42d0cb794a3eb947b1e1f9b06`  
		Last Modified: Tue, 10 Sep 2024 00:53:10 GMT  
		Size: 2.3 MB (2285050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73f6f1fc8ce970b2f59c4b67cfef86ef3c1dc692d3e5b91930a0f834c2aa8286`  
		Last Modified: Tue, 10 Sep 2024 00:53:10 GMT  
		Size: 21.1 KB (21095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:a564ae9d7581535075625ac57d9c0b961354e9b4daba7c4b8081f9c94a7272cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30885604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0553326148f76a8da67990b40b3cda91d5eb09e6450645d355301f64cdd62ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 21:42:50 GMT
ADD file:728128617ba2b026c358eb266cd495be84354c4e5dc4ecc2953cb829190a4546 in / 
# Wed, 04 Sep 2024 21:42:52 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:95fe27c895a828dc681ee4a0cbea0264c47528dad525efdb9641a375666536bd`  
		Last Modified: Wed, 04 Sep 2024 21:47:41 GMT  
		Size: 27.5 MB (27490321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14930957f1690905df41f1da11505509319dd65a7de378761ed685a7f319746`  
		Last Modified: Fri, 06 Sep 2024 22:03:27 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0833ee43e72a5f44318da8b85bdf6aa1bb3bddf0fdd75dc5530531a126eb97`  
		Last Modified: Fri, 06 Sep 2024 22:03:27 GMT  
		Size: 2.2 MB (2155800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49ba017e9517b59a0101e268f88f7b430651242d3de79201588254bb0fe7507`  
		Last Modified: Mon, 09 Sep 2024 23:57:11 GMT  
		Size: 1.2 MB (1237972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f824a2d96ada01e3ba546f908f36e9780321cfd73e3145903949cd6f8d9bbc`  
		Last Modified: Mon, 09 Sep 2024 23:57:11 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c979fb5ce067e0a4128dc5527a66b9ee1bf3762c94b5f309c473ede06b29be`  
		Last Modified: Mon, 09 Sep 2024 23:57:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:d96f09ec7f4c6e807df2fac9bd6834a30ab928672e82902cd5cc756d638221a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d39e3cfd9222897db8d98adeddedd43e35a75647f77cf2ca9276356feeb1695`

```dockerfile
```

-	Layers:
	-	`sha256:d83c73c94a489231e85f509c8c17651508a61d8aa02ef340f03babd8b3a5253b`  
		Last Modified: Mon, 09 Sep 2024 23:57:11 GMT  
		Size: 2.3 MB (2280500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b7064082e2a2543d417d8956bcd38d8aa02707fd3284afe698b5e0c00f111b1`  
		Last Modified: Mon, 09 Sep 2024 23:57:11 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.31`

```console
$ docker pull memcached@sha256:51cdb01f624e1eab205f978b21756cf3ef96ca33da2cd074cb47245b92e0705f
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

### `memcached:1.6.31` - linux; amd64

```console
$ docker pull memcached@sha256:a658d819b6f9ab244148f9e9994489e759ff72e12cd2a93cf0a9b0259f324743
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32878406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a783d40c8b808e6a5c1d562c8ddf24732920c2c1b7e12eadaeb76b3f1e468b32`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 07 Sep 2024 18:54:11 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d937ff39f058bf2417a4fe760827ff36b1b38be77ed6c3b27fbd80872b4106b9`  
		Last Modified: Fri, 27 Sep 2024 06:05:04 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2bb47e18c2052b1e07d1957f90f1d197fcbf398748e534e8fa54f75782b3fff`  
		Last Modified: Fri, 27 Sep 2024 06:05:04 GMT  
		Size: 2.5 MB (2491322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c618990832780ea1a130f360744ad52c95ef7485138ded320b5563aedc090b`  
		Last Modified: Fri, 27 Sep 2024 06:05:04 GMT  
		Size: 1.3 MB (1259299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f09b0e04f54ca243201f3b8f205c759c2892f6752f8e75aa84434ab4a4b330`  
		Last Modified: Fri, 27 Sep 2024 06:05:04 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2038e2b3f99ec442dfe1024270c1ad10a59fb8995060bc0a2e7a6831bbc48917`  
		Last Modified: Fri, 27 Sep 2024 06:05:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.31` - unknown; unknown

```console
$ docker pull memcached@sha256:2fbb3c4bddfc491f239cbe76e97dbd05fa35514c183e7fa4ac819cda30fd5acf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b83b1908356b5b8567c67431165b1c6e4a18a87b108cb329988349341ed52f3e`

```dockerfile
```

-	Layers:
	-	`sha256:e0ac909638f1cc11061867d2eca41aafdfd8ac0189cceb25a5aa9c4ff9c7f0fc`  
		Last Modified: Fri, 27 Sep 2024 06:05:04 GMT  
		Size: 2.3 MB (2280692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c438d6540bdc9adc9140d94352ea4200a10e7cfc1168f6b3c47c8202fe19ace1`  
		Last Modified: Fri, 27 Sep 2024 06:05:04 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.31` - linux; arm variant v5

```console
$ docker pull memcached@sha256:365ca3a58f4ec2be52314d56ca69b149210604be3008c503c731cf5f4a095f5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30222872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43b582780474a2688f3e337b9c5a04bcf5697372ab5e9377d88e069e75607247`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 21:48:32 GMT
ADD file:c162e60b24ef6aed489ba1986f407fd9ab4ace659e0e3e6759ffac7eb0b7f770 in / 
# Wed, 04 Sep 2024 21:48:32 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:44990bd21e0c5db65674bd030d12ea2461a14f2bb4007469bc2667c8535a8357`  
		Last Modified: Wed, 04 Sep 2024 21:51:32 GMT  
		Size: 26.9 MB (26887411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a8ee21aa62c2c20c62d17e0dd3670c4484279b7481df253ab7dea06579e38f6`  
		Last Modified: Thu, 05 Sep 2024 03:28:45 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e5212bff7c052802224f0dcd2c61c47f77a42869600109756dedd710f28915`  
		Last Modified: Thu, 05 Sep 2024 03:28:46 GMT  
		Size: 2.1 MB (2095647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0782223d771fbfcf1c9ed4475479f748c453dd6aa6dc53aa45361cd00224de57`  
		Last Modified: Tue, 10 Sep 2024 02:36:03 GMT  
		Size: 1.2 MB (1238299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530caa10c823e2b669f21afaf522a557d974f4ea259b23e29b5a88c357559aa9`  
		Last Modified: Tue, 10 Sep 2024 02:36:02 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2f95efd2295adb5abdb3e0e56c5d975248bcc1c4951cedbfc5f10c2480cb9c`  
		Last Modified: Tue, 10 Sep 2024 02:36:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.31` - unknown; unknown

```console
$ docker pull memcached@sha256:643f24e07712d430691849d647e01c9ba7828371296a20fbe49250e582c0fac2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8e2f351cd6f24d1550b56f8e379b3e6aef1289d89b131237317ca600e4d52a0`

```dockerfile
```

-	Layers:
	-	`sha256:6d0e93f21d109f38cd7d09c5fc37735dc06c58bfcc63c9e950d187b500196f7b`  
		Last Modified: Tue, 10 Sep 2024 02:36:03 GMT  
		Size: 2.3 MB (2284110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:877d052619f8f882ecca7bddd9b19ea3ac0aff81603a8e053c4cfef2c753b056`  
		Last Modified: Tue, 10 Sep 2024 02:36:02 GMT  
		Size: 21.2 KB (21169 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.31` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:875cd34f6465e3e8fa28ef5db4bfad8c176e1c0263daff0171fc9537b0ca3a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32767698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a91d45790f325414f2734648e019a463d8d1353ca9250b2700504151dcdfbbe0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:52 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Wed, 04 Sep 2024 21:39:53 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04865bf94e709891a3952f6be4719f98f7a66c94aeb7ca127b805a21559f233b`  
		Last Modified: Fri, 06 Sep 2024 22:18:47 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2accb5dc3319c683f0fcfa968e975b4170700c037764eba741ba2d1c52c8ad0a`  
		Last Modified: Fri, 06 Sep 2024 22:18:47 GMT  
		Size: 2.4 MB (2354829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099212eee1d8aedc74760284b20c722ff3262dfeebadb7801f18e140dd2a88c4`  
		Last Modified: Tue, 10 Sep 2024 05:26:27 GMT  
		Size: 1.3 MB (1254813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfbc137765c6a6be5ae31943c75d26fb8556d6f8d6dc7372cba395a51e9600c8`  
		Last Modified: Tue, 10 Sep 2024 05:26:27 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6847381e1607ee0f70837cb4d081424ec06929f39c8c350ff85944aef711304c`  
		Last Modified: Tue, 10 Sep 2024 05:26:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.31` - unknown; unknown

```console
$ docker pull memcached@sha256:56255e99acdfe342a7754928cb5ed717ab5f7372c48426d0dc8b1515d05a4b4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:336d6748c4ae106ed4adc2a8b4c756622427e4066c4aa1351246e7a0fe352da8`

```dockerfile
```

-	Layers:
	-	`sha256:29df9c8dc456cfd5983e243674508af61ff397da6d8d6a997e017e85a4e4266c`  
		Last Modified: Tue, 10 Sep 2024 05:26:27 GMT  
		Size: 2.3 MB (2280993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d304f0d86e38bf9bc9ed7714e76015b79876a10b2d8c67f081473bfdcabe377`  
		Last Modified: Tue, 10 Sep 2024 05:26:27 GMT  
		Size: 21.4 KB (21385 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.31` - linux; 386

```console
$ docker pull memcached@sha256:34dcfa089dd249a4df38d93bee834b8e9ef0f20fc783cc57beecc31eb4e04fcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33904516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7bacc013d82d74a63cc6ad50eec7918e02e35d93e1138cd7405cb396e80b5a3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 22:44:34 GMT
ADD file:1d96491aed0d3091aadb984e1dfe642343013348f4a1807a69e132efaed68030 in / 
# Wed, 04 Sep 2024 22:44:34 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c304282df09b425e8240f53c55110ac282ba801da157a805e4fdbdf8c832b376`  
		Last Modified: Wed, 04 Sep 2024 22:48:08 GMT  
		Size: 30.1 MB (30144294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6c5637a99c0d5bfbc04c2f481699f0ab6cbcf940efabacc33b17680528fcb1`  
		Last Modified: Mon, 09 Sep 2024 23:04:42 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7a2b527feff9ff4df7dcb2a0b26ec01a6fa914c48cfb3bba0d873a5f7ae189`  
		Last Modified: Mon, 09 Sep 2024 23:04:42 GMT  
		Size: 2.5 MB (2499306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d54ad1af4809e5533f75ab13f83a284e966f4bdf5df4880fba412f3fa6e415`  
		Last Modified: Mon, 09 Sep 2024 23:04:42 GMT  
		Size: 1.3 MB (1259401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:683954138ef3ece20193896fd5a5df2deb974514c9f939d749eb46c161f1e4f6`  
		Last Modified: Mon, 09 Sep 2024 23:04:42 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d4e2b90164f16b0893ff5354664d43d05f691e1ef4165d1f45889cfaa8bc68`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.31` - unknown; unknown

```console
$ docker pull memcached@sha256:5f5144206a28ac6d02a6064d09bef45ba19ea0e834380667b5252173fc1aee2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2298749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c582914882b6e0802c0ff6073312ad790deb59006c1edeeca6423351ecc04295`

```dockerfile
```

-	Layers:
	-	`sha256:08d010ee1407ba55007943c5783e18992fce487cf9fc06f1001a6c6ee139ad50`  
		Last Modified: Mon, 09 Sep 2024 23:04:42 GMT  
		Size: 2.3 MB (2277777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8dabd61e7f4bdb4bd9a53e403b676e865ad1ec09201180b76f03117a501c2d7`  
		Last Modified: Mon, 09 Sep 2024 23:04:42 GMT  
		Size: 21.0 KB (20972 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.31` - linux; mips64le

```console
$ docker pull memcached@sha256:6f842f8998fe08cfdcb13cd83a7d09dfee91b25ae8b6937b02702480c5c55d22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32323662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d5a34a6f646baa48f817d457c47eb9762e5066adc40bc80cded7232eacb00d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 22:15:45 GMT
ADD file:9ffa4d53a074e91efecf5e26e3b67077f46165e0d042c1e6cf1b93c531ed2bc4 in / 
# Wed, 04 Sep 2024 22:15:50 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:89502a0eae32ab684bc9df3d9922ee2874839b178a693286c4b866f5ca8e93f3`  
		Last Modified: Wed, 04 Sep 2024 22:24:11 GMT  
		Size: 29.1 MB (29125054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a544e9e80cb1c7ab6c5794cb1a0a4715aa0df1fd8437a0d771017c52f3e5f5`  
		Last Modified: Thu, 05 Sep 2024 11:18:11 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7605e144a412910a4194cfffafd5d127bc44e9b19ba5191b74df2cc6a267f2e0`  
		Last Modified: Thu, 05 Sep 2024 11:18:12 GMT  
		Size: 1.9 MB (1942689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92a7d1694bf26de03563c78b52328eeabf26a387feba7ff6fbb8bb253427f27`  
		Last Modified: Tue, 10 Sep 2024 02:25:37 GMT  
		Size: 1.3 MB (1254404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c99675ddde9651d74c5ef49e2a70ca2c3351852fb856272dfb9b5f328a69e31`  
		Last Modified: Tue, 10 Sep 2024 02:25:37 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859d2e9814139aaf71bc0d3cc5e5eecdba1d8f10c4cc0196aa46b58d2830bebe`  
		Last Modified: Tue, 10 Sep 2024 02:25:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.31` - unknown; unknown

```console
$ docker pull memcached@sha256:6c4530d40688ecfde5ff475267c0fd60f9d67cd7e23c5e177ae0e20937467413
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e60bb1c6684aec9c40b2deb99de2c399adb2682fdc6efecdd98aef1881475ac`

```dockerfile
```

-	Layers:
	-	`sha256:74c8d993dc8b0fbc1c7708b04cec649eac5a3f36f5bc171bc1d523edc126aeff`  
		Last Modified: Tue, 10 Sep 2024 02:25:37 GMT  
		Size: 20.9 KB (20911 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.31` - linux; ppc64le

```console
$ docker pull memcached@sha256:a2c15d4ae7e15fa7457c5f843feb6bfc17bf3a4ee8c7fe278e9af0824a54be80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37154878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4f56f782d0ddfeacfa04a2d1bc62b4ee9938d6128b8c29f12647454f427251e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 22:25:52 GMT
ADD file:d83b2f8d4d3fd22a390140e3bebefb48e5f086d072ad6062f6446b4fc42ec7a8 in / 
# Wed, 04 Sep 2024 22:25:54 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f19b11698292330b7d980ed50b0141417eec298d865e0c1b305ce7a8b80b572d`  
		Last Modified: Wed, 04 Sep 2024 22:30:11 GMT  
		Size: 33.1 MB (33122358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ee1834d6aa97efd9d43db3a50a5bb3dda4b08400d531f72579cadea051609e`  
		Last Modified: Fri, 06 Sep 2024 22:02:56 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9152281fc8ce1403b29050f252829939c461cf037d8b3491653f7eeee4ece43`  
		Last Modified: Fri, 06 Sep 2024 22:02:56 GMT  
		Size: 2.7 MB (2707191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e141823a412ee63afdae23f927aa51b3eb72dd45577cf194159595a77d4577e2`  
		Last Modified: Tue, 10 Sep 2024 00:53:10 GMT  
		Size: 1.3 MB (1323809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c8e76a6f99b8b59c45f2a7eea7a5ee3870791b1a3abe6679881522a171e998`  
		Last Modified: Tue, 10 Sep 2024 00:53:10 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc7d2a375bf95c80dfd28c577fb84d803a9bb9437dd19ebc1801f99fb035120`  
		Last Modified: Tue, 10 Sep 2024 00:53:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.31` - unknown; unknown

```console
$ docker pull memcached@sha256:3bd251857bd96c65b8ad1e08a21c64177e673356369ff7404be1ba2edac796b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4713e2ddd75a9c1fba28b6cf8191e2ed2cb6b5e47a06bcb2db95a9efbbc74fda`

```dockerfile
```

-	Layers:
	-	`sha256:ca0b1f85d6ea571ab124bed1c494d1d8fb6673a42d0cb794a3eb947b1e1f9b06`  
		Last Modified: Tue, 10 Sep 2024 00:53:10 GMT  
		Size: 2.3 MB (2285050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73f6f1fc8ce970b2f59c4b67cfef86ef3c1dc692d3e5b91930a0f834c2aa8286`  
		Last Modified: Tue, 10 Sep 2024 00:53:10 GMT  
		Size: 21.1 KB (21095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.31` - linux; s390x

```console
$ docker pull memcached@sha256:a564ae9d7581535075625ac57d9c0b961354e9b4daba7c4b8081f9c94a7272cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30885604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0553326148f76a8da67990b40b3cda91d5eb09e6450645d355301f64cdd62ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 21:42:50 GMT
ADD file:728128617ba2b026c358eb266cd495be84354c4e5dc4ecc2953cb829190a4546 in / 
# Wed, 04 Sep 2024 21:42:52 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:95fe27c895a828dc681ee4a0cbea0264c47528dad525efdb9641a375666536bd`  
		Last Modified: Wed, 04 Sep 2024 21:47:41 GMT  
		Size: 27.5 MB (27490321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14930957f1690905df41f1da11505509319dd65a7de378761ed685a7f319746`  
		Last Modified: Fri, 06 Sep 2024 22:03:27 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0833ee43e72a5f44318da8b85bdf6aa1bb3bddf0fdd75dc5530531a126eb97`  
		Last Modified: Fri, 06 Sep 2024 22:03:27 GMT  
		Size: 2.2 MB (2155800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49ba017e9517b59a0101e268f88f7b430651242d3de79201588254bb0fe7507`  
		Last Modified: Mon, 09 Sep 2024 23:57:11 GMT  
		Size: 1.2 MB (1237972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f824a2d96ada01e3ba546f908f36e9780321cfd73e3145903949cd6f8d9bbc`  
		Last Modified: Mon, 09 Sep 2024 23:57:11 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c979fb5ce067e0a4128dc5527a66b9ee1bf3762c94b5f309c473ede06b29be`  
		Last Modified: Mon, 09 Sep 2024 23:57:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.31` - unknown; unknown

```console
$ docker pull memcached@sha256:d96f09ec7f4c6e807df2fac9bd6834a30ab928672e82902cd5cc756d638221a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d39e3cfd9222897db8d98adeddedd43e35a75647f77cf2ca9276356feeb1695`

```dockerfile
```

-	Layers:
	-	`sha256:d83c73c94a489231e85f509c8c17651508a61d8aa02ef340f03babd8b3a5253b`  
		Last Modified: Mon, 09 Sep 2024 23:57:11 GMT  
		Size: 2.3 MB (2280500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b7064082e2a2543d417d8956bcd38d8aa02707fd3284afe698b5e0c00f111b1`  
		Last Modified: Mon, 09 Sep 2024 23:57:11 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.31-alpine`

```console
$ docker pull memcached@sha256:da20d2d6a9101cc4cef2803aa7c6c426e0d3dc2bdff2626d0efd60f6fadd9a1c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `memcached:1.6.31-alpine` - linux; amd64

```console
$ docker pull memcached@sha256:bc62c9b146672d0f63f0b3a38722acae32e859f635e6f32f0b31afdcb1013c7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4687755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aae0d824f4bc7874b3fd26fc5e61b2fe8c3fc9b58f82f3be24a6010c05ec1c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e2704d07ea50e4350fc30a778f91c517bee857b54bcc571b464e2b563744ab`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f89cbdbe5025b3c7d2ff8f9f6bfbb7bcd639adb35200de6f0b8b4515488f1b05`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 103.8 KB (103822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f139dbcb2579cd1e9f78db09fd279e08d323c219a6efcad878b42cd961d24a25`  
		Last Modified: Mon, 09 Sep 2024 23:04:31 GMT  
		Size: 958.8 KB (958765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3487c95e4eb9d8fb5506b2cd3406c02c1fba592fbafe1078c141420c22939fc7`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eaf1d2da7366110dda884212201a67c62fb0f9c921217de86755d35b80fbee9`  
		Last Modified: Mon, 09 Sep 2024 23:04:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.31-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:c96c825ac5a6f1db0849694d7878693b7113126e5c85540cdb4e191454d0afcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 KB (107135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a3dddb2bd6769fc79a77da8e93edcfe6d98d55badebcebbc9faaecb661ad001`

```dockerfile
```

-	Layers:
	-	`sha256:7102ff71a3580f59d96136c579e83bbb7e913951d315d57f5d15541dc8438bdb`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 87.8 KB (87785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e083725668b94672a9a645717ffd665a9f0059d9823eed6b8b1bc89bee285c4e`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 19.4 KB (19350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.31-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:a2d38a957041270c55d551e8ecf53f69df6613a17df3fb1876ab6fb65cd99ea6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5172731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3954249ac508b8b8c4a968b394a6970e8d868f1744e672affe792ee9231b39ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04310511d0b87f77a431a5f50ac0c3d95896d6a39a16aa043ba443f6b0e0fddd`  
		Last Modified: Sat, 07 Sep 2024 05:30:38 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b28609c2d169047004bf72890ec5ac9e3a88bd3aa153e465bf17c14f3ebf3b`  
		Last Modified: Sat, 07 Sep 2024 05:30:38 GMT  
		Size: 121.0 KB (121024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4adf4e4f7be512c6272c74db833112894b8410062060f6888539171290372a82`  
		Last Modified: Tue, 10 Sep 2024 05:30:03 GMT  
		Size: 962.7 KB (962700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c043e4b98daae0158835eeb78946255c4027b9ebe97d5e569fa8f1df39119c7`  
		Last Modified: Tue, 10 Sep 2024 05:30:03 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e243cd97c138165f622734a969475116f77deb0f3c6efaf70fae4ac39ebbffc`  
		Last Modified: Tue, 10 Sep 2024 05:30:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.31-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:9d2c6d970fa941ac951ded01e253b2d4492d8bda51fd29bc2f6915310f884231
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0bc6ae2b075b905b17704735488c6da23574abab2bbc1bb4aefebbe65768955`

```dockerfile
```

-	Layers:
	-	`sha256:36cf7adc241f552244e6d64628168a1dee985ba7a3176282286b5ca13998f243`  
		Last Modified: Tue, 10 Sep 2024 05:30:02 GMT  
		Size: 87.9 KB (87889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90b01e0840b58a8d84f085ca69e1f3f3eb1fd0a0abd8b42fca270e09451e6161`  
		Last Modified: Tue, 10 Sep 2024 05:30:02 GMT  
		Size: 19.7 KB (19698 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.31-alpine` - linux; 386

```console
$ docker pull memcached@sha256:7228773d86ac6e8955e5d2d7ffefc2ae564b00cadd0c858310dec50e9fad6f42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4531177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41f22aace0957bde9cbc95b95320e1836991afac8a43e215d16ef141508788c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:41:21 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Fri, 06 Sep 2024 22:41:21 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e2704d07ea50e4350fc30a778f91c517bee857b54bcc571b464e2b563744ab`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef4ec43894c33c1d68e1fbb24d27f314125a8617ada637af061725989f14953`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 109.0 KB (108961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b19ce951cfcb336fa2050f3422e487f515d16ddcf2c69c80d29d9f66baa9d16e`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 951.7 KB (951692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cfaaa1bc534e7c46c1b3aa67465a41ca91d4ce83071caebc7a11e3ff143be02`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0615a81d8e335acdc6d68eefcf35b5d516a3cc0ed68bac6adfd5807799b53f46`  
		Last Modified: Mon, 09 Sep 2024 23:04:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.31-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7940458999ce753465ef3f968a9eabac518a9df3d5d77386552d3526c2b946ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.0 KB (107035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e2e327ed8d984210e8a47612bf76565fb47b80c1d0e63bbc53b45c571fd09f9`

```dockerfile
```

-	Layers:
	-	`sha256:c1c9fcdee5d34fae3276a06573fa1e3d9a3a0b6d532765266d4e86f6be9a695b`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 87.7 KB (87740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12c78394468356d9d60cea99380a31c53b12f50a43699c3916eda41ba6ee3470`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 19.3 KB (19295 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.31-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:517da247dc00201621112cd48487139ce6966636899a4c40fdb02b307f3f1b5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4694177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98eb649600a0e4277874d7abade7034b99d425dcb34c55e165f11569d4166b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:06 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 22:26:07 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645d78667a8075f56004a7a283eaeb1a630309a9d950a27de5cc29eb72cec340`  
		Last Modified: Sat, 07 Sep 2024 07:05:29 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5844b90ee5623766614a832d5e5f322566849ed5853adfbe1f63e8d954b540d9`  
		Last Modified: Sat, 07 Sep 2024 07:05:29 GMT  
		Size: 123.0 KB (123003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b715436c927b60842b1c1f98f7cb7c4257838f7b36a5e2334b5f590ca152f6`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 997.4 KB (997389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ad232e17fce60e215c458fcac12f4ac1d5bdd60080527a4c28d76c6c831393`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8e18c99726667f58640d52458967d66a4da28b7f2eaaac5626723a6691ed45`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.31-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:e4e8b6df3a60e291797c10897a7779345a41715ab61dfd7f76bccdc42ef8a7ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 KB (105307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469f18677668b4dd9a3de113d4ae3f111f5b89e03f3795cef6eab0e1e3eecbbe`

```dockerfile
```

-	Layers:
	-	`sha256:f7beb1e9f1753005bac3249d305c8567220853e93353216074762ad7f1813c0a`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 85.9 KB (85889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2eea735dc745320130c1139867abe3e0b71de840a5a8a3170b9191994b69b01b`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 19.4 KB (19418 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.31-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:a6f8155d863aa33eae871b75e7543c04404c30248007928840beeffae2eb5e78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4556594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63fcf33c45f689bdee882ed4ad8692b55a55abe13941eb4cc525adeafab650c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:17 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 22:48:17 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc58d10317d926d80ab2de5020728ade9434725004663fce6207d95ecc3ba0c`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed425e517c8a02d89379669853a47dbd343281c3fcfc3e37f91b671f0b35ffc`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 112.7 KB (112740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02fe29c4e792447391a38d4b9d7aa18f9a51d6f171eb15297a427efb6a33e839`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 980.9 KB (980896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fffd060f2e26e85750706fd829abf92d787fdf9321cba829cab93f30845547f`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93825c9e15b3ee5a0f3ebddccf232551b4506353af049da3e37f7ae97e39a384`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.31-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:5c62ae13354b08074917592e56f436a96d4ccf47cbf5c4a13231f53d556be814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 KB (105181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fda0c239bf944625a0bd5aeea27175b74c697a79c4b068f9d8e137b786a2b4a4`

```dockerfile
```

-	Layers:
	-	`sha256:870d5efdd4242eb6cc01519cd2092666c5ab15b546cb69d2711791408721605b`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 85.8 KB (85831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dbbbb69edb2b376c21146fd5c88b6254433cc9264976b2868973688bb8a95cf`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 19.4 KB (19350 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.31-alpine3.20`

```console
$ docker pull memcached@sha256:da20d2d6a9101cc4cef2803aa7c6c426e0d3dc2bdff2626d0efd60f6fadd9a1c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `memcached:1.6.31-alpine3.20` - linux; amd64

```console
$ docker pull memcached@sha256:bc62c9b146672d0f63f0b3a38722acae32e859f635e6f32f0b31afdcb1013c7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4687755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aae0d824f4bc7874b3fd26fc5e61b2fe8c3fc9b58f82f3be24a6010c05ec1c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e2704d07ea50e4350fc30a778f91c517bee857b54bcc571b464e2b563744ab`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f89cbdbe5025b3c7d2ff8f9f6bfbb7bcd639adb35200de6f0b8b4515488f1b05`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 103.8 KB (103822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f139dbcb2579cd1e9f78db09fd279e08d323c219a6efcad878b42cd961d24a25`  
		Last Modified: Mon, 09 Sep 2024 23:04:31 GMT  
		Size: 958.8 KB (958765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3487c95e4eb9d8fb5506b2cd3406c02c1fba592fbafe1078c141420c22939fc7`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eaf1d2da7366110dda884212201a67c62fb0f9c921217de86755d35b80fbee9`  
		Last Modified: Mon, 09 Sep 2024 23:04:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.31-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:c96c825ac5a6f1db0849694d7878693b7113126e5c85540cdb4e191454d0afcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 KB (107135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a3dddb2bd6769fc79a77da8e93edcfe6d98d55badebcebbc9faaecb661ad001`

```dockerfile
```

-	Layers:
	-	`sha256:7102ff71a3580f59d96136c579e83bbb7e913951d315d57f5d15541dc8438bdb`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 87.8 KB (87785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e083725668b94672a9a645717ffd665a9f0059d9823eed6b8b1bc89bee285c4e`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 19.4 KB (19350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.31-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:a2d38a957041270c55d551e8ecf53f69df6613a17df3fb1876ab6fb65cd99ea6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5172731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3954249ac508b8b8c4a968b394a6970e8d868f1744e672affe792ee9231b39ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04310511d0b87f77a431a5f50ac0c3d95896d6a39a16aa043ba443f6b0e0fddd`  
		Last Modified: Sat, 07 Sep 2024 05:30:38 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b28609c2d169047004bf72890ec5ac9e3a88bd3aa153e465bf17c14f3ebf3b`  
		Last Modified: Sat, 07 Sep 2024 05:30:38 GMT  
		Size: 121.0 KB (121024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4adf4e4f7be512c6272c74db833112894b8410062060f6888539171290372a82`  
		Last Modified: Tue, 10 Sep 2024 05:30:03 GMT  
		Size: 962.7 KB (962700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c043e4b98daae0158835eeb78946255c4027b9ebe97d5e569fa8f1df39119c7`  
		Last Modified: Tue, 10 Sep 2024 05:30:03 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e243cd97c138165f622734a969475116f77deb0f3c6efaf70fae4ac39ebbffc`  
		Last Modified: Tue, 10 Sep 2024 05:30:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.31-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:9d2c6d970fa941ac951ded01e253b2d4492d8bda51fd29bc2f6915310f884231
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0bc6ae2b075b905b17704735488c6da23574abab2bbc1bb4aefebbe65768955`

```dockerfile
```

-	Layers:
	-	`sha256:36cf7adc241f552244e6d64628168a1dee985ba7a3176282286b5ca13998f243`  
		Last Modified: Tue, 10 Sep 2024 05:30:02 GMT  
		Size: 87.9 KB (87889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90b01e0840b58a8d84f085ca69e1f3f3eb1fd0a0abd8b42fca270e09451e6161`  
		Last Modified: Tue, 10 Sep 2024 05:30:02 GMT  
		Size: 19.7 KB (19698 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.31-alpine3.20` - linux; 386

```console
$ docker pull memcached@sha256:7228773d86ac6e8955e5d2d7ffefc2ae564b00cadd0c858310dec50e9fad6f42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4531177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41f22aace0957bde9cbc95b95320e1836991afac8a43e215d16ef141508788c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:41:21 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Fri, 06 Sep 2024 22:41:21 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e2704d07ea50e4350fc30a778f91c517bee857b54bcc571b464e2b563744ab`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef4ec43894c33c1d68e1fbb24d27f314125a8617ada637af061725989f14953`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 109.0 KB (108961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b19ce951cfcb336fa2050f3422e487f515d16ddcf2c69c80d29d9f66baa9d16e`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 951.7 KB (951692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cfaaa1bc534e7c46c1b3aa67465a41ca91d4ce83071caebc7a11e3ff143be02`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0615a81d8e335acdc6d68eefcf35b5d516a3cc0ed68bac6adfd5807799b53f46`  
		Last Modified: Mon, 09 Sep 2024 23:04:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.31-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:7940458999ce753465ef3f968a9eabac518a9df3d5d77386552d3526c2b946ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.0 KB (107035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e2e327ed8d984210e8a47612bf76565fb47b80c1d0e63bbc53b45c571fd09f9`

```dockerfile
```

-	Layers:
	-	`sha256:c1c9fcdee5d34fae3276a06573fa1e3d9a3a0b6d532765266d4e86f6be9a695b`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 87.7 KB (87740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12c78394468356d9d60cea99380a31c53b12f50a43699c3916eda41ba6ee3470`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 19.3 KB (19295 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.31-alpine3.20` - linux; ppc64le

```console
$ docker pull memcached@sha256:517da247dc00201621112cd48487139ce6966636899a4c40fdb02b307f3f1b5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4694177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98eb649600a0e4277874d7abade7034b99d425dcb34c55e165f11569d4166b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:06 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 22:26:07 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645d78667a8075f56004a7a283eaeb1a630309a9d950a27de5cc29eb72cec340`  
		Last Modified: Sat, 07 Sep 2024 07:05:29 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5844b90ee5623766614a832d5e5f322566849ed5853adfbe1f63e8d954b540d9`  
		Last Modified: Sat, 07 Sep 2024 07:05:29 GMT  
		Size: 123.0 KB (123003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b715436c927b60842b1c1f98f7cb7c4257838f7b36a5e2334b5f590ca152f6`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 997.4 KB (997389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ad232e17fce60e215c458fcac12f4ac1d5bdd60080527a4c28d76c6c831393`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8e18c99726667f58640d52458967d66a4da28b7f2eaaac5626723a6691ed45`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.31-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:e4e8b6df3a60e291797c10897a7779345a41715ab61dfd7f76bccdc42ef8a7ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 KB (105307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469f18677668b4dd9a3de113d4ae3f111f5b89e03f3795cef6eab0e1e3eecbbe`

```dockerfile
```

-	Layers:
	-	`sha256:f7beb1e9f1753005bac3249d305c8567220853e93353216074762ad7f1813c0a`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 85.9 KB (85889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2eea735dc745320130c1139867abe3e0b71de840a5a8a3170b9191994b69b01b`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 19.4 KB (19418 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.31-alpine3.20` - linux; s390x

```console
$ docker pull memcached@sha256:a6f8155d863aa33eae871b75e7543c04404c30248007928840beeffae2eb5e78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4556594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63fcf33c45f689bdee882ed4ad8692b55a55abe13941eb4cc525adeafab650c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:17 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 22:48:17 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc58d10317d926d80ab2de5020728ade9434725004663fce6207d95ecc3ba0c`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed425e517c8a02d89379669853a47dbd343281c3fcfc3e37f91b671f0b35ffc`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 112.7 KB (112740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02fe29c4e792447391a38d4b9d7aa18f9a51d6f171eb15297a427efb6a33e839`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 980.9 KB (980896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fffd060f2e26e85750706fd829abf92d787fdf9321cba829cab93f30845547f`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93825c9e15b3ee5a0f3ebddccf232551b4506353af049da3e37f7ae97e39a384`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.31-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:5c62ae13354b08074917592e56f436a96d4ccf47cbf5c4a13231f53d556be814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 KB (105181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fda0c239bf944625a0bd5aeea27175b74c697a79c4b068f9d8e137b786a2b4a4`

```dockerfile
```

-	Layers:
	-	`sha256:870d5efdd4242eb6cc01519cd2092666c5ab15b546cb69d2711791408721605b`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 85.8 KB (85831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dbbbb69edb2b376c21146fd5c88b6254433cc9264976b2868973688bb8a95cf`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 19.4 KB (19350 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.31-bookworm`

```console
$ docker pull memcached@sha256:51cdb01f624e1eab205f978b21756cf3ef96ca33da2cd074cb47245b92e0705f
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

### `memcached:1.6.31-bookworm` - linux; amd64

```console
$ docker pull memcached@sha256:a658d819b6f9ab244148f9e9994489e759ff72e12cd2a93cf0a9b0259f324743
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32878406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a783d40c8b808e6a5c1d562c8ddf24732920c2c1b7e12eadaeb76b3f1e468b32`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 07 Sep 2024 18:54:11 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d937ff39f058bf2417a4fe760827ff36b1b38be77ed6c3b27fbd80872b4106b9`  
		Last Modified: Fri, 27 Sep 2024 06:05:04 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2bb47e18c2052b1e07d1957f90f1d197fcbf398748e534e8fa54f75782b3fff`  
		Last Modified: Fri, 27 Sep 2024 06:05:04 GMT  
		Size: 2.5 MB (2491322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c618990832780ea1a130f360744ad52c95ef7485138ded320b5563aedc090b`  
		Last Modified: Fri, 27 Sep 2024 06:05:04 GMT  
		Size: 1.3 MB (1259299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f09b0e04f54ca243201f3b8f205c759c2892f6752f8e75aa84434ab4a4b330`  
		Last Modified: Fri, 27 Sep 2024 06:05:04 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2038e2b3f99ec442dfe1024270c1ad10a59fb8995060bc0a2e7a6831bbc48917`  
		Last Modified: Fri, 27 Sep 2024 06:05:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.31-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:2fbb3c4bddfc491f239cbe76e97dbd05fa35514c183e7fa4ac819cda30fd5acf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b83b1908356b5b8567c67431165b1c6e4a18a87b108cb329988349341ed52f3e`

```dockerfile
```

-	Layers:
	-	`sha256:e0ac909638f1cc11061867d2eca41aafdfd8ac0189cceb25a5aa9c4ff9c7f0fc`  
		Last Modified: Fri, 27 Sep 2024 06:05:04 GMT  
		Size: 2.3 MB (2280692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c438d6540bdc9adc9140d94352ea4200a10e7cfc1168f6b3c47c8202fe19ace1`  
		Last Modified: Fri, 27 Sep 2024 06:05:04 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.31-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:365ca3a58f4ec2be52314d56ca69b149210604be3008c503c731cf5f4a095f5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30222872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43b582780474a2688f3e337b9c5a04bcf5697372ab5e9377d88e069e75607247`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 21:48:32 GMT
ADD file:c162e60b24ef6aed489ba1986f407fd9ab4ace659e0e3e6759ffac7eb0b7f770 in / 
# Wed, 04 Sep 2024 21:48:32 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:44990bd21e0c5db65674bd030d12ea2461a14f2bb4007469bc2667c8535a8357`  
		Last Modified: Wed, 04 Sep 2024 21:51:32 GMT  
		Size: 26.9 MB (26887411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a8ee21aa62c2c20c62d17e0dd3670c4484279b7481df253ab7dea06579e38f6`  
		Last Modified: Thu, 05 Sep 2024 03:28:45 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e5212bff7c052802224f0dcd2c61c47f77a42869600109756dedd710f28915`  
		Last Modified: Thu, 05 Sep 2024 03:28:46 GMT  
		Size: 2.1 MB (2095647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0782223d771fbfcf1c9ed4475479f748c453dd6aa6dc53aa45361cd00224de57`  
		Last Modified: Tue, 10 Sep 2024 02:36:03 GMT  
		Size: 1.2 MB (1238299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530caa10c823e2b669f21afaf522a557d974f4ea259b23e29b5a88c357559aa9`  
		Last Modified: Tue, 10 Sep 2024 02:36:02 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2f95efd2295adb5abdb3e0e56c5d975248bcc1c4951cedbfc5f10c2480cb9c`  
		Last Modified: Tue, 10 Sep 2024 02:36:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.31-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:643f24e07712d430691849d647e01c9ba7828371296a20fbe49250e582c0fac2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8e2f351cd6f24d1550b56f8e379b3e6aef1289d89b131237317ca600e4d52a0`

```dockerfile
```

-	Layers:
	-	`sha256:6d0e93f21d109f38cd7d09c5fc37735dc06c58bfcc63c9e950d187b500196f7b`  
		Last Modified: Tue, 10 Sep 2024 02:36:03 GMT  
		Size: 2.3 MB (2284110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:877d052619f8f882ecca7bddd9b19ea3ac0aff81603a8e053c4cfef2c753b056`  
		Last Modified: Tue, 10 Sep 2024 02:36:02 GMT  
		Size: 21.2 KB (21169 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.31-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:875cd34f6465e3e8fa28ef5db4bfad8c176e1c0263daff0171fc9537b0ca3a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32767698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a91d45790f325414f2734648e019a463d8d1353ca9250b2700504151dcdfbbe0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:52 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Wed, 04 Sep 2024 21:39:53 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04865bf94e709891a3952f6be4719f98f7a66c94aeb7ca127b805a21559f233b`  
		Last Modified: Fri, 06 Sep 2024 22:18:47 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2accb5dc3319c683f0fcfa968e975b4170700c037764eba741ba2d1c52c8ad0a`  
		Last Modified: Fri, 06 Sep 2024 22:18:47 GMT  
		Size: 2.4 MB (2354829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099212eee1d8aedc74760284b20c722ff3262dfeebadb7801f18e140dd2a88c4`  
		Last Modified: Tue, 10 Sep 2024 05:26:27 GMT  
		Size: 1.3 MB (1254813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfbc137765c6a6be5ae31943c75d26fb8556d6f8d6dc7372cba395a51e9600c8`  
		Last Modified: Tue, 10 Sep 2024 05:26:27 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6847381e1607ee0f70837cb4d081424ec06929f39c8c350ff85944aef711304c`  
		Last Modified: Tue, 10 Sep 2024 05:26:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.31-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:56255e99acdfe342a7754928cb5ed717ab5f7372c48426d0dc8b1515d05a4b4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:336d6748c4ae106ed4adc2a8b4c756622427e4066c4aa1351246e7a0fe352da8`

```dockerfile
```

-	Layers:
	-	`sha256:29df9c8dc456cfd5983e243674508af61ff397da6d8d6a997e017e85a4e4266c`  
		Last Modified: Tue, 10 Sep 2024 05:26:27 GMT  
		Size: 2.3 MB (2280993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d304f0d86e38bf9bc9ed7714e76015b79876a10b2d8c67f081473bfdcabe377`  
		Last Modified: Tue, 10 Sep 2024 05:26:27 GMT  
		Size: 21.4 KB (21385 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.31-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:34dcfa089dd249a4df38d93bee834b8e9ef0f20fc783cc57beecc31eb4e04fcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33904516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7bacc013d82d74a63cc6ad50eec7918e02e35d93e1138cd7405cb396e80b5a3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 22:44:34 GMT
ADD file:1d96491aed0d3091aadb984e1dfe642343013348f4a1807a69e132efaed68030 in / 
# Wed, 04 Sep 2024 22:44:34 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c304282df09b425e8240f53c55110ac282ba801da157a805e4fdbdf8c832b376`  
		Last Modified: Wed, 04 Sep 2024 22:48:08 GMT  
		Size: 30.1 MB (30144294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6c5637a99c0d5bfbc04c2f481699f0ab6cbcf940efabacc33b17680528fcb1`  
		Last Modified: Mon, 09 Sep 2024 23:04:42 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7a2b527feff9ff4df7dcb2a0b26ec01a6fa914c48cfb3bba0d873a5f7ae189`  
		Last Modified: Mon, 09 Sep 2024 23:04:42 GMT  
		Size: 2.5 MB (2499306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d54ad1af4809e5533f75ab13f83a284e966f4bdf5df4880fba412f3fa6e415`  
		Last Modified: Mon, 09 Sep 2024 23:04:42 GMT  
		Size: 1.3 MB (1259401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:683954138ef3ece20193896fd5a5df2deb974514c9f939d749eb46c161f1e4f6`  
		Last Modified: Mon, 09 Sep 2024 23:04:42 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d4e2b90164f16b0893ff5354664d43d05f691e1ef4165d1f45889cfaa8bc68`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.31-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:5f5144206a28ac6d02a6064d09bef45ba19ea0e834380667b5252173fc1aee2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2298749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c582914882b6e0802c0ff6073312ad790deb59006c1edeeca6423351ecc04295`

```dockerfile
```

-	Layers:
	-	`sha256:08d010ee1407ba55007943c5783e18992fce487cf9fc06f1001a6c6ee139ad50`  
		Last Modified: Mon, 09 Sep 2024 23:04:42 GMT  
		Size: 2.3 MB (2277777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8dabd61e7f4bdb4bd9a53e403b676e865ad1ec09201180b76f03117a501c2d7`  
		Last Modified: Mon, 09 Sep 2024 23:04:42 GMT  
		Size: 21.0 KB (20972 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.31-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:6f842f8998fe08cfdcb13cd83a7d09dfee91b25ae8b6937b02702480c5c55d22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32323662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d5a34a6f646baa48f817d457c47eb9762e5066adc40bc80cded7232eacb00d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 22:15:45 GMT
ADD file:9ffa4d53a074e91efecf5e26e3b67077f46165e0d042c1e6cf1b93c531ed2bc4 in / 
# Wed, 04 Sep 2024 22:15:50 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:89502a0eae32ab684bc9df3d9922ee2874839b178a693286c4b866f5ca8e93f3`  
		Last Modified: Wed, 04 Sep 2024 22:24:11 GMT  
		Size: 29.1 MB (29125054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a544e9e80cb1c7ab6c5794cb1a0a4715aa0df1fd8437a0d771017c52f3e5f5`  
		Last Modified: Thu, 05 Sep 2024 11:18:11 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7605e144a412910a4194cfffafd5d127bc44e9b19ba5191b74df2cc6a267f2e0`  
		Last Modified: Thu, 05 Sep 2024 11:18:12 GMT  
		Size: 1.9 MB (1942689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92a7d1694bf26de03563c78b52328eeabf26a387feba7ff6fbb8bb253427f27`  
		Last Modified: Tue, 10 Sep 2024 02:25:37 GMT  
		Size: 1.3 MB (1254404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c99675ddde9651d74c5ef49e2a70ca2c3351852fb856272dfb9b5f328a69e31`  
		Last Modified: Tue, 10 Sep 2024 02:25:37 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859d2e9814139aaf71bc0d3cc5e5eecdba1d8f10c4cc0196aa46b58d2830bebe`  
		Last Modified: Tue, 10 Sep 2024 02:25:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.31-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:6c4530d40688ecfde5ff475267c0fd60f9d67cd7e23c5e177ae0e20937467413
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e60bb1c6684aec9c40b2deb99de2c399adb2682fdc6efecdd98aef1881475ac`

```dockerfile
```

-	Layers:
	-	`sha256:74c8d993dc8b0fbc1c7708b04cec649eac5a3f36f5bc171bc1d523edc126aeff`  
		Last Modified: Tue, 10 Sep 2024 02:25:37 GMT  
		Size: 20.9 KB (20911 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.31-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:a2c15d4ae7e15fa7457c5f843feb6bfc17bf3a4ee8c7fe278e9af0824a54be80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37154878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4f56f782d0ddfeacfa04a2d1bc62b4ee9938d6128b8c29f12647454f427251e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 22:25:52 GMT
ADD file:d83b2f8d4d3fd22a390140e3bebefb48e5f086d072ad6062f6446b4fc42ec7a8 in / 
# Wed, 04 Sep 2024 22:25:54 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f19b11698292330b7d980ed50b0141417eec298d865e0c1b305ce7a8b80b572d`  
		Last Modified: Wed, 04 Sep 2024 22:30:11 GMT  
		Size: 33.1 MB (33122358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ee1834d6aa97efd9d43db3a50a5bb3dda4b08400d531f72579cadea051609e`  
		Last Modified: Fri, 06 Sep 2024 22:02:56 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9152281fc8ce1403b29050f252829939c461cf037d8b3491653f7eeee4ece43`  
		Last Modified: Fri, 06 Sep 2024 22:02:56 GMT  
		Size: 2.7 MB (2707191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e141823a412ee63afdae23f927aa51b3eb72dd45577cf194159595a77d4577e2`  
		Last Modified: Tue, 10 Sep 2024 00:53:10 GMT  
		Size: 1.3 MB (1323809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c8e76a6f99b8b59c45f2a7eea7a5ee3870791b1a3abe6679881522a171e998`  
		Last Modified: Tue, 10 Sep 2024 00:53:10 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc7d2a375bf95c80dfd28c577fb84d803a9bb9437dd19ebc1801f99fb035120`  
		Last Modified: Tue, 10 Sep 2024 00:53:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.31-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:3bd251857bd96c65b8ad1e08a21c64177e673356369ff7404be1ba2edac796b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4713e2ddd75a9c1fba28b6cf8191e2ed2cb6b5e47a06bcb2db95a9efbbc74fda`

```dockerfile
```

-	Layers:
	-	`sha256:ca0b1f85d6ea571ab124bed1c494d1d8fb6673a42d0cb794a3eb947b1e1f9b06`  
		Last Modified: Tue, 10 Sep 2024 00:53:10 GMT  
		Size: 2.3 MB (2285050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73f6f1fc8ce970b2f59c4b67cfef86ef3c1dc692d3e5b91930a0f834c2aa8286`  
		Last Modified: Tue, 10 Sep 2024 00:53:10 GMT  
		Size: 21.1 KB (21095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.31-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:a564ae9d7581535075625ac57d9c0b961354e9b4daba7c4b8081f9c94a7272cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30885604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0553326148f76a8da67990b40b3cda91d5eb09e6450645d355301f64cdd62ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 21:42:50 GMT
ADD file:728128617ba2b026c358eb266cd495be84354c4e5dc4ecc2953cb829190a4546 in / 
# Wed, 04 Sep 2024 21:42:52 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:95fe27c895a828dc681ee4a0cbea0264c47528dad525efdb9641a375666536bd`  
		Last Modified: Wed, 04 Sep 2024 21:47:41 GMT  
		Size: 27.5 MB (27490321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14930957f1690905df41f1da11505509319dd65a7de378761ed685a7f319746`  
		Last Modified: Fri, 06 Sep 2024 22:03:27 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0833ee43e72a5f44318da8b85bdf6aa1bb3bddf0fdd75dc5530531a126eb97`  
		Last Modified: Fri, 06 Sep 2024 22:03:27 GMT  
		Size: 2.2 MB (2155800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49ba017e9517b59a0101e268f88f7b430651242d3de79201588254bb0fe7507`  
		Last Modified: Mon, 09 Sep 2024 23:57:11 GMT  
		Size: 1.2 MB (1237972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f824a2d96ada01e3ba546f908f36e9780321cfd73e3145903949cd6f8d9bbc`  
		Last Modified: Mon, 09 Sep 2024 23:57:11 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c979fb5ce067e0a4128dc5527a66b9ee1bf3762c94b5f309c473ede06b29be`  
		Last Modified: Mon, 09 Sep 2024 23:57:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.31-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:d96f09ec7f4c6e807df2fac9bd6834a30ab928672e82902cd5cc756d638221a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d39e3cfd9222897db8d98adeddedd43e35a75647f77cf2ca9276356feeb1695`

```dockerfile
```

-	Layers:
	-	`sha256:d83c73c94a489231e85f509c8c17651508a61d8aa02ef340f03babd8b3a5253b`  
		Last Modified: Mon, 09 Sep 2024 23:57:11 GMT  
		Size: 2.3 MB (2280500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b7064082e2a2543d417d8956bcd38d8aa02707fd3284afe698b5e0c00f111b1`  
		Last Modified: Mon, 09 Sep 2024 23:57:11 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine`

```console
$ docker pull memcached@sha256:6fff88e239680465aa0b7e977b2f1a322471c3552644159371de6c1731a5014a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `memcached:alpine` - linux; amd64

```console
$ docker pull memcached@sha256:bc62c9b146672d0f63f0b3a38722acae32e859f635e6f32f0b31afdcb1013c7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4687755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aae0d824f4bc7874b3fd26fc5e61b2fe8c3fc9b58f82f3be24a6010c05ec1c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e2704d07ea50e4350fc30a778f91c517bee857b54bcc571b464e2b563744ab`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f89cbdbe5025b3c7d2ff8f9f6bfbb7bcd639adb35200de6f0b8b4515488f1b05`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 103.8 KB (103822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f139dbcb2579cd1e9f78db09fd279e08d323c219a6efcad878b42cd961d24a25`  
		Last Modified: Mon, 09 Sep 2024 23:04:31 GMT  
		Size: 958.8 KB (958765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3487c95e4eb9d8fb5506b2cd3406c02c1fba592fbafe1078c141420c22939fc7`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eaf1d2da7366110dda884212201a67c62fb0f9c921217de86755d35b80fbee9`  
		Last Modified: Mon, 09 Sep 2024 23:04:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:c96c825ac5a6f1db0849694d7878693b7113126e5c85540cdb4e191454d0afcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 KB (107135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a3dddb2bd6769fc79a77da8e93edcfe6d98d55badebcebbc9faaecb661ad001`

```dockerfile
```

-	Layers:
	-	`sha256:7102ff71a3580f59d96136c579e83bbb7e913951d315d57f5d15541dc8438bdb`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 87.8 KB (87785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e083725668b94672a9a645717ffd665a9f0059d9823eed6b8b1bc89bee285c4e`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 19.4 KB (19350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:a2d38a957041270c55d551e8ecf53f69df6613a17df3fb1876ab6fb65cd99ea6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5172731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3954249ac508b8b8c4a968b394a6970e8d868f1744e672affe792ee9231b39ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04310511d0b87f77a431a5f50ac0c3d95896d6a39a16aa043ba443f6b0e0fddd`  
		Last Modified: Sat, 07 Sep 2024 05:30:38 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b28609c2d169047004bf72890ec5ac9e3a88bd3aa153e465bf17c14f3ebf3b`  
		Last Modified: Sat, 07 Sep 2024 05:30:38 GMT  
		Size: 121.0 KB (121024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4adf4e4f7be512c6272c74db833112894b8410062060f6888539171290372a82`  
		Last Modified: Tue, 10 Sep 2024 05:30:03 GMT  
		Size: 962.7 KB (962700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c043e4b98daae0158835eeb78946255c4027b9ebe97d5e569fa8f1df39119c7`  
		Last Modified: Tue, 10 Sep 2024 05:30:03 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e243cd97c138165f622734a969475116f77deb0f3c6efaf70fae4ac39ebbffc`  
		Last Modified: Tue, 10 Sep 2024 05:30:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:9d2c6d970fa941ac951ded01e253b2d4492d8bda51fd29bc2f6915310f884231
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0bc6ae2b075b905b17704735488c6da23574abab2bbc1bb4aefebbe65768955`

```dockerfile
```

-	Layers:
	-	`sha256:36cf7adc241f552244e6d64628168a1dee985ba7a3176282286b5ca13998f243`  
		Last Modified: Tue, 10 Sep 2024 05:30:02 GMT  
		Size: 87.9 KB (87889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90b01e0840b58a8d84f085ca69e1f3f3eb1fd0a0abd8b42fca270e09451e6161`  
		Last Modified: Tue, 10 Sep 2024 05:30:02 GMT  
		Size: 19.7 KB (19698 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; 386

```console
$ docker pull memcached@sha256:7228773d86ac6e8955e5d2d7ffefc2ae564b00cadd0c858310dec50e9fad6f42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4531177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41f22aace0957bde9cbc95b95320e1836991afac8a43e215d16ef141508788c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:41:21 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Fri, 06 Sep 2024 22:41:21 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e2704d07ea50e4350fc30a778f91c517bee857b54bcc571b464e2b563744ab`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef4ec43894c33c1d68e1fbb24d27f314125a8617ada637af061725989f14953`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 109.0 KB (108961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b19ce951cfcb336fa2050f3422e487f515d16ddcf2c69c80d29d9f66baa9d16e`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 951.7 KB (951692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cfaaa1bc534e7c46c1b3aa67465a41ca91d4ce83071caebc7a11e3ff143be02`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0615a81d8e335acdc6d68eefcf35b5d516a3cc0ed68bac6adfd5807799b53f46`  
		Last Modified: Mon, 09 Sep 2024 23:04:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7940458999ce753465ef3f968a9eabac518a9df3d5d77386552d3526c2b946ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.0 KB (107035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e2e327ed8d984210e8a47612bf76565fb47b80c1d0e63bbc53b45c571fd09f9`

```dockerfile
```

-	Layers:
	-	`sha256:c1c9fcdee5d34fae3276a06573fa1e3d9a3a0b6d532765266d4e86f6be9a695b`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 87.7 KB (87740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12c78394468356d9d60cea99380a31c53b12f50a43699c3916eda41ba6ee3470`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 19.3 KB (19295 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:517da247dc00201621112cd48487139ce6966636899a4c40fdb02b307f3f1b5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4694177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98eb649600a0e4277874d7abade7034b99d425dcb34c55e165f11569d4166b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:06 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 22:26:07 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645d78667a8075f56004a7a283eaeb1a630309a9d950a27de5cc29eb72cec340`  
		Last Modified: Sat, 07 Sep 2024 07:05:29 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5844b90ee5623766614a832d5e5f322566849ed5853adfbe1f63e8d954b540d9`  
		Last Modified: Sat, 07 Sep 2024 07:05:29 GMT  
		Size: 123.0 KB (123003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b715436c927b60842b1c1f98f7cb7c4257838f7b36a5e2334b5f590ca152f6`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 997.4 KB (997389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ad232e17fce60e215c458fcac12f4ac1d5bdd60080527a4c28d76c6c831393`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8e18c99726667f58640d52458967d66a4da28b7f2eaaac5626723a6691ed45`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:e4e8b6df3a60e291797c10897a7779345a41715ab61dfd7f76bccdc42ef8a7ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 KB (105307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469f18677668b4dd9a3de113d4ae3f111f5b89e03f3795cef6eab0e1e3eecbbe`

```dockerfile
```

-	Layers:
	-	`sha256:f7beb1e9f1753005bac3249d305c8567220853e93353216074762ad7f1813c0a`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 85.9 KB (85889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2eea735dc745320130c1139867abe3e0b71de840a5a8a3170b9191994b69b01b`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 19.4 KB (19418 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; riscv64

```console
$ docker pull memcached@sha256:ceffb56b913ca8a62831ef271642b11ddbeea098de65d093af55cbba0f8d56e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4427664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c258ae7e36ddd3758d8ddff147c4db3f4928f4db92f67bc7b91ffa68c86d4ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:cdf7088bbd70519f0f5d7b4249df34386e40f0194752f45842b3d85f2d331cf5 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["/bin/sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:faf447acae27573624c0613a79c4bcf1f9bc46d29f523140352abfd3f7691282`  
		Last Modified: Mon, 22 Jul 2024 22:21:18 GMT  
		Size: 3.4 MB (3370673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230af89e5f8d3eec0e6d96c87e99a85b938e0722dacebe0009ad7b8b00ca320b`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c75b82861f48f0052a86f16f944c0324ed20af856a4c9d87c147dc645460ee6`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 108.6 KB (108596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d23c6553fa0ff65e57ebc39080a958cc4d1d02587781c94836137d124c47ce`  
		Last Modified: Sun, 28 Jul 2024 15:58:50 GMT  
		Size: 947.0 KB (947030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab42ab26d315472c0f9433b5c7f25e0e426c020b3b0e8cc52d1c7d09ca7bf91`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e436e8ed56076dff056e7dc989a1944739cb23a96400a543900ab3bd07a77b6`  
		Last Modified: Sun, 28 Jul 2024 15:58:50 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:fdf92c6c75f08244e376b28b33307c9ea75a07f7523b56b86df44f1be3335f3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 KB (105303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc24bdd15449aa6c8213cd2607de7998a598edba9ca2fb7de80b4b761b833a64`

```dockerfile
```

-	Layers:
	-	`sha256:dbb3dc8245856acbf66987c1cd0f4f37d8af7b49bc0c7b8eaacfb02321594ac5`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 85.9 KB (85885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2359a9107230c13ad5d1c580fc348790129c58ea95b407db376ee7eb5a109571`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 19.4 KB (19418 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; s390x

```console
$ docker pull memcached@sha256:a6f8155d863aa33eae871b75e7543c04404c30248007928840beeffae2eb5e78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4556594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63fcf33c45f689bdee882ed4ad8692b55a55abe13941eb4cc525adeafab650c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:17 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 22:48:17 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc58d10317d926d80ab2de5020728ade9434725004663fce6207d95ecc3ba0c`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed425e517c8a02d89379669853a47dbd343281c3fcfc3e37f91b671f0b35ffc`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 112.7 KB (112740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02fe29c4e792447391a38d4b9d7aa18f9a51d6f171eb15297a427efb6a33e839`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 980.9 KB (980896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fffd060f2e26e85750706fd829abf92d787fdf9321cba829cab93f30845547f`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93825c9e15b3ee5a0f3ebddccf232551b4506353af049da3e37f7ae97e39a384`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:5c62ae13354b08074917592e56f436a96d4ccf47cbf5c4a13231f53d556be814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 KB (105181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fda0c239bf944625a0bd5aeea27175b74c697a79c4b068f9d8e137b786a2b4a4`

```dockerfile
```

-	Layers:
	-	`sha256:870d5efdd4242eb6cc01519cd2092666c5ab15b546cb69d2711791408721605b`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 85.8 KB (85831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dbbbb69edb2b376c21146fd5c88b6254433cc9264976b2868973688bb8a95cf`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 19.4 KB (19350 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine3.20`

```console
$ docker pull memcached@sha256:6fff88e239680465aa0b7e977b2f1a322471c3552644159371de6c1731a5014a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `memcached:alpine3.20` - linux; amd64

```console
$ docker pull memcached@sha256:bc62c9b146672d0f63f0b3a38722acae32e859f635e6f32f0b31afdcb1013c7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4687755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aae0d824f4bc7874b3fd26fc5e61b2fe8c3fc9b58f82f3be24a6010c05ec1c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e2704d07ea50e4350fc30a778f91c517bee857b54bcc571b464e2b563744ab`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f89cbdbe5025b3c7d2ff8f9f6bfbb7bcd639adb35200de6f0b8b4515488f1b05`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 103.8 KB (103822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f139dbcb2579cd1e9f78db09fd279e08d323c219a6efcad878b42cd961d24a25`  
		Last Modified: Mon, 09 Sep 2024 23:04:31 GMT  
		Size: 958.8 KB (958765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3487c95e4eb9d8fb5506b2cd3406c02c1fba592fbafe1078c141420c22939fc7`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eaf1d2da7366110dda884212201a67c62fb0f9c921217de86755d35b80fbee9`  
		Last Modified: Mon, 09 Sep 2024 23:04:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:c96c825ac5a6f1db0849694d7878693b7113126e5c85540cdb4e191454d0afcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 KB (107135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a3dddb2bd6769fc79a77da8e93edcfe6d98d55badebcebbc9faaecb661ad001`

```dockerfile
```

-	Layers:
	-	`sha256:7102ff71a3580f59d96136c579e83bbb7e913951d315d57f5d15541dc8438bdb`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 87.8 KB (87785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e083725668b94672a9a645717ffd665a9f0059d9823eed6b8b1bc89bee285c4e`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 19.4 KB (19350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.20` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:a2d38a957041270c55d551e8ecf53f69df6613a17df3fb1876ab6fb65cd99ea6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5172731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3954249ac508b8b8c4a968b394a6970e8d868f1744e672affe792ee9231b39ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04310511d0b87f77a431a5f50ac0c3d95896d6a39a16aa043ba443f6b0e0fddd`  
		Last Modified: Sat, 07 Sep 2024 05:30:38 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b28609c2d169047004bf72890ec5ac9e3a88bd3aa153e465bf17c14f3ebf3b`  
		Last Modified: Sat, 07 Sep 2024 05:30:38 GMT  
		Size: 121.0 KB (121024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4adf4e4f7be512c6272c74db833112894b8410062060f6888539171290372a82`  
		Last Modified: Tue, 10 Sep 2024 05:30:03 GMT  
		Size: 962.7 KB (962700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c043e4b98daae0158835eeb78946255c4027b9ebe97d5e569fa8f1df39119c7`  
		Last Modified: Tue, 10 Sep 2024 05:30:03 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e243cd97c138165f622734a969475116f77deb0f3c6efaf70fae4ac39ebbffc`  
		Last Modified: Tue, 10 Sep 2024 05:30:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:9d2c6d970fa941ac951ded01e253b2d4492d8bda51fd29bc2f6915310f884231
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0bc6ae2b075b905b17704735488c6da23574abab2bbc1bb4aefebbe65768955`

```dockerfile
```

-	Layers:
	-	`sha256:36cf7adc241f552244e6d64628168a1dee985ba7a3176282286b5ca13998f243`  
		Last Modified: Tue, 10 Sep 2024 05:30:02 GMT  
		Size: 87.9 KB (87889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90b01e0840b58a8d84f085ca69e1f3f3eb1fd0a0abd8b42fca270e09451e6161`  
		Last Modified: Tue, 10 Sep 2024 05:30:02 GMT  
		Size: 19.7 KB (19698 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.20` - linux; 386

```console
$ docker pull memcached@sha256:7228773d86ac6e8955e5d2d7ffefc2ae564b00cadd0c858310dec50e9fad6f42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4531177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41f22aace0957bde9cbc95b95320e1836991afac8a43e215d16ef141508788c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:41:21 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Fri, 06 Sep 2024 22:41:21 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e2704d07ea50e4350fc30a778f91c517bee857b54bcc571b464e2b563744ab`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef4ec43894c33c1d68e1fbb24d27f314125a8617ada637af061725989f14953`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 109.0 KB (108961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b19ce951cfcb336fa2050f3422e487f515d16ddcf2c69c80d29d9f66baa9d16e`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 951.7 KB (951692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cfaaa1bc534e7c46c1b3aa67465a41ca91d4ce83071caebc7a11e3ff143be02`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0615a81d8e335acdc6d68eefcf35b5d516a3cc0ed68bac6adfd5807799b53f46`  
		Last Modified: Mon, 09 Sep 2024 23:04:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:7940458999ce753465ef3f968a9eabac518a9df3d5d77386552d3526c2b946ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.0 KB (107035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e2e327ed8d984210e8a47612bf76565fb47b80c1d0e63bbc53b45c571fd09f9`

```dockerfile
```

-	Layers:
	-	`sha256:c1c9fcdee5d34fae3276a06573fa1e3d9a3a0b6d532765266d4e86f6be9a695b`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 87.7 KB (87740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12c78394468356d9d60cea99380a31c53b12f50a43699c3916eda41ba6ee3470`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 19.3 KB (19295 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.20` - linux; ppc64le

```console
$ docker pull memcached@sha256:517da247dc00201621112cd48487139ce6966636899a4c40fdb02b307f3f1b5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4694177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98eb649600a0e4277874d7abade7034b99d425dcb34c55e165f11569d4166b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:06 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 22:26:07 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645d78667a8075f56004a7a283eaeb1a630309a9d950a27de5cc29eb72cec340`  
		Last Modified: Sat, 07 Sep 2024 07:05:29 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5844b90ee5623766614a832d5e5f322566849ed5853adfbe1f63e8d954b540d9`  
		Last Modified: Sat, 07 Sep 2024 07:05:29 GMT  
		Size: 123.0 KB (123003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b715436c927b60842b1c1f98f7cb7c4257838f7b36a5e2334b5f590ca152f6`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 997.4 KB (997389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ad232e17fce60e215c458fcac12f4ac1d5bdd60080527a4c28d76c6c831393`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8e18c99726667f58640d52458967d66a4da28b7f2eaaac5626723a6691ed45`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:e4e8b6df3a60e291797c10897a7779345a41715ab61dfd7f76bccdc42ef8a7ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 KB (105307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469f18677668b4dd9a3de113d4ae3f111f5b89e03f3795cef6eab0e1e3eecbbe`

```dockerfile
```

-	Layers:
	-	`sha256:f7beb1e9f1753005bac3249d305c8567220853e93353216074762ad7f1813c0a`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 85.9 KB (85889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2eea735dc745320130c1139867abe3e0b71de840a5a8a3170b9191994b69b01b`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 19.4 KB (19418 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.20` - linux; riscv64

```console
$ docker pull memcached@sha256:ceffb56b913ca8a62831ef271642b11ddbeea098de65d093af55cbba0f8d56e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4427664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c258ae7e36ddd3758d8ddff147c4db3f4928f4db92f67bc7b91ffa68c86d4ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:cdf7088bbd70519f0f5d7b4249df34386e40f0194752f45842b3d85f2d331cf5 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["/bin/sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:faf447acae27573624c0613a79c4bcf1f9bc46d29f523140352abfd3f7691282`  
		Last Modified: Mon, 22 Jul 2024 22:21:18 GMT  
		Size: 3.4 MB (3370673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230af89e5f8d3eec0e6d96c87e99a85b938e0722dacebe0009ad7b8b00ca320b`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c75b82861f48f0052a86f16f944c0324ed20af856a4c9d87c147dc645460ee6`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 108.6 KB (108596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d23c6553fa0ff65e57ebc39080a958cc4d1d02587781c94836137d124c47ce`  
		Last Modified: Sun, 28 Jul 2024 15:58:50 GMT  
		Size: 947.0 KB (947030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab42ab26d315472c0f9433b5c7f25e0e426c020b3b0e8cc52d1c7d09ca7bf91`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e436e8ed56076dff056e7dc989a1944739cb23a96400a543900ab3bd07a77b6`  
		Last Modified: Sun, 28 Jul 2024 15:58:50 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:fdf92c6c75f08244e376b28b33307c9ea75a07f7523b56b86df44f1be3335f3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 KB (105303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc24bdd15449aa6c8213cd2607de7998a598edba9ca2fb7de80b4b761b833a64`

```dockerfile
```

-	Layers:
	-	`sha256:dbb3dc8245856acbf66987c1cd0f4f37d8af7b49bc0c7b8eaacfb02321594ac5`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 85.9 KB (85885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2359a9107230c13ad5d1c580fc348790129c58ea95b407db376ee7eb5a109571`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 19.4 KB (19418 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.20` - linux; s390x

```console
$ docker pull memcached@sha256:a6f8155d863aa33eae871b75e7543c04404c30248007928840beeffae2eb5e78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4556594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63fcf33c45f689bdee882ed4ad8692b55a55abe13941eb4cc525adeafab650c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:17 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 22:48:17 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc58d10317d926d80ab2de5020728ade9434725004663fce6207d95ecc3ba0c`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed425e517c8a02d89379669853a47dbd343281c3fcfc3e37f91b671f0b35ffc`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 112.7 KB (112740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02fe29c4e792447391a38d4b9d7aa18f9a51d6f171eb15297a427efb6a33e839`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 980.9 KB (980896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fffd060f2e26e85750706fd829abf92d787fdf9321cba829cab93f30845547f`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93825c9e15b3ee5a0f3ebddccf232551b4506353af049da3e37f7ae97e39a384`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:5c62ae13354b08074917592e56f436a96d4ccf47cbf5c4a13231f53d556be814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 KB (105181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fda0c239bf944625a0bd5aeea27175b74c697a79c4b068f9d8e137b786a2b4a4`

```dockerfile
```

-	Layers:
	-	`sha256:870d5efdd4242eb6cc01519cd2092666c5ab15b546cb69d2711791408721605b`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 85.8 KB (85831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dbbbb69edb2b376c21146fd5c88b6254433cc9264976b2868973688bb8a95cf`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 19.4 KB (19350 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:bookworm`

```console
$ docker pull memcached@sha256:51cdb01f624e1eab205f978b21756cf3ef96ca33da2cd074cb47245b92e0705f
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
$ docker pull memcached@sha256:a658d819b6f9ab244148f9e9994489e759ff72e12cd2a93cf0a9b0259f324743
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32878406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a783d40c8b808e6a5c1d562c8ddf24732920c2c1b7e12eadaeb76b3f1e468b32`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 07 Sep 2024 18:54:11 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d937ff39f058bf2417a4fe760827ff36b1b38be77ed6c3b27fbd80872b4106b9`  
		Last Modified: Fri, 27 Sep 2024 06:05:04 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2bb47e18c2052b1e07d1957f90f1d197fcbf398748e534e8fa54f75782b3fff`  
		Last Modified: Fri, 27 Sep 2024 06:05:04 GMT  
		Size: 2.5 MB (2491322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c618990832780ea1a130f360744ad52c95ef7485138ded320b5563aedc090b`  
		Last Modified: Fri, 27 Sep 2024 06:05:04 GMT  
		Size: 1.3 MB (1259299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f09b0e04f54ca243201f3b8f205c759c2892f6752f8e75aa84434ab4a4b330`  
		Last Modified: Fri, 27 Sep 2024 06:05:04 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2038e2b3f99ec442dfe1024270c1ad10a59fb8995060bc0a2e7a6831bbc48917`  
		Last Modified: Fri, 27 Sep 2024 06:05:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:2fbb3c4bddfc491f239cbe76e97dbd05fa35514c183e7fa4ac819cda30fd5acf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b83b1908356b5b8567c67431165b1c6e4a18a87b108cb329988349341ed52f3e`

```dockerfile
```

-	Layers:
	-	`sha256:e0ac909638f1cc11061867d2eca41aafdfd8ac0189cceb25a5aa9c4ff9c7f0fc`  
		Last Modified: Fri, 27 Sep 2024 06:05:04 GMT  
		Size: 2.3 MB (2280692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c438d6540bdc9adc9140d94352ea4200a10e7cfc1168f6b3c47c8202fe19ace1`  
		Last Modified: Fri, 27 Sep 2024 06:05:04 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:365ca3a58f4ec2be52314d56ca69b149210604be3008c503c731cf5f4a095f5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30222872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43b582780474a2688f3e337b9c5a04bcf5697372ab5e9377d88e069e75607247`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 21:48:32 GMT
ADD file:c162e60b24ef6aed489ba1986f407fd9ab4ace659e0e3e6759ffac7eb0b7f770 in / 
# Wed, 04 Sep 2024 21:48:32 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:44990bd21e0c5db65674bd030d12ea2461a14f2bb4007469bc2667c8535a8357`  
		Last Modified: Wed, 04 Sep 2024 21:51:32 GMT  
		Size: 26.9 MB (26887411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a8ee21aa62c2c20c62d17e0dd3670c4484279b7481df253ab7dea06579e38f6`  
		Last Modified: Thu, 05 Sep 2024 03:28:45 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e5212bff7c052802224f0dcd2c61c47f77a42869600109756dedd710f28915`  
		Last Modified: Thu, 05 Sep 2024 03:28:46 GMT  
		Size: 2.1 MB (2095647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0782223d771fbfcf1c9ed4475479f748c453dd6aa6dc53aa45361cd00224de57`  
		Last Modified: Tue, 10 Sep 2024 02:36:03 GMT  
		Size: 1.2 MB (1238299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530caa10c823e2b669f21afaf522a557d974f4ea259b23e29b5a88c357559aa9`  
		Last Modified: Tue, 10 Sep 2024 02:36:02 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2f95efd2295adb5abdb3e0e56c5d975248bcc1c4951cedbfc5f10c2480cb9c`  
		Last Modified: Tue, 10 Sep 2024 02:36:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:643f24e07712d430691849d647e01c9ba7828371296a20fbe49250e582c0fac2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8e2f351cd6f24d1550b56f8e379b3e6aef1289d89b131237317ca600e4d52a0`

```dockerfile
```

-	Layers:
	-	`sha256:6d0e93f21d109f38cd7d09c5fc37735dc06c58bfcc63c9e950d187b500196f7b`  
		Last Modified: Tue, 10 Sep 2024 02:36:03 GMT  
		Size: 2.3 MB (2284110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:877d052619f8f882ecca7bddd9b19ea3ac0aff81603a8e053c4cfef2c753b056`  
		Last Modified: Tue, 10 Sep 2024 02:36:02 GMT  
		Size: 21.2 KB (21169 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:875cd34f6465e3e8fa28ef5db4bfad8c176e1c0263daff0171fc9537b0ca3a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32767698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a91d45790f325414f2734648e019a463d8d1353ca9250b2700504151dcdfbbe0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:52 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Wed, 04 Sep 2024 21:39:53 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04865bf94e709891a3952f6be4719f98f7a66c94aeb7ca127b805a21559f233b`  
		Last Modified: Fri, 06 Sep 2024 22:18:47 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2accb5dc3319c683f0fcfa968e975b4170700c037764eba741ba2d1c52c8ad0a`  
		Last Modified: Fri, 06 Sep 2024 22:18:47 GMT  
		Size: 2.4 MB (2354829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099212eee1d8aedc74760284b20c722ff3262dfeebadb7801f18e140dd2a88c4`  
		Last Modified: Tue, 10 Sep 2024 05:26:27 GMT  
		Size: 1.3 MB (1254813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfbc137765c6a6be5ae31943c75d26fb8556d6f8d6dc7372cba395a51e9600c8`  
		Last Modified: Tue, 10 Sep 2024 05:26:27 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6847381e1607ee0f70837cb4d081424ec06929f39c8c350ff85944aef711304c`  
		Last Modified: Tue, 10 Sep 2024 05:26:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:56255e99acdfe342a7754928cb5ed717ab5f7372c48426d0dc8b1515d05a4b4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:336d6748c4ae106ed4adc2a8b4c756622427e4066c4aa1351246e7a0fe352da8`

```dockerfile
```

-	Layers:
	-	`sha256:29df9c8dc456cfd5983e243674508af61ff397da6d8d6a997e017e85a4e4266c`  
		Last Modified: Tue, 10 Sep 2024 05:26:27 GMT  
		Size: 2.3 MB (2280993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d304f0d86e38bf9bc9ed7714e76015b79876a10b2d8c67f081473bfdcabe377`  
		Last Modified: Tue, 10 Sep 2024 05:26:27 GMT  
		Size: 21.4 KB (21385 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; 386

```console
$ docker pull memcached@sha256:34dcfa089dd249a4df38d93bee834b8e9ef0f20fc783cc57beecc31eb4e04fcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33904516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7bacc013d82d74a63cc6ad50eec7918e02e35d93e1138cd7405cb396e80b5a3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 22:44:34 GMT
ADD file:1d96491aed0d3091aadb984e1dfe642343013348f4a1807a69e132efaed68030 in / 
# Wed, 04 Sep 2024 22:44:34 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c304282df09b425e8240f53c55110ac282ba801da157a805e4fdbdf8c832b376`  
		Last Modified: Wed, 04 Sep 2024 22:48:08 GMT  
		Size: 30.1 MB (30144294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6c5637a99c0d5bfbc04c2f481699f0ab6cbcf940efabacc33b17680528fcb1`  
		Last Modified: Mon, 09 Sep 2024 23:04:42 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7a2b527feff9ff4df7dcb2a0b26ec01a6fa914c48cfb3bba0d873a5f7ae189`  
		Last Modified: Mon, 09 Sep 2024 23:04:42 GMT  
		Size: 2.5 MB (2499306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d54ad1af4809e5533f75ab13f83a284e966f4bdf5df4880fba412f3fa6e415`  
		Last Modified: Mon, 09 Sep 2024 23:04:42 GMT  
		Size: 1.3 MB (1259401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:683954138ef3ece20193896fd5a5df2deb974514c9f939d749eb46c161f1e4f6`  
		Last Modified: Mon, 09 Sep 2024 23:04:42 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d4e2b90164f16b0893ff5354664d43d05f691e1ef4165d1f45889cfaa8bc68`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:5f5144206a28ac6d02a6064d09bef45ba19ea0e834380667b5252173fc1aee2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2298749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c582914882b6e0802c0ff6073312ad790deb59006c1edeeca6423351ecc04295`

```dockerfile
```

-	Layers:
	-	`sha256:08d010ee1407ba55007943c5783e18992fce487cf9fc06f1001a6c6ee139ad50`  
		Last Modified: Mon, 09 Sep 2024 23:04:42 GMT  
		Size: 2.3 MB (2277777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8dabd61e7f4bdb4bd9a53e403b676e865ad1ec09201180b76f03117a501c2d7`  
		Last Modified: Mon, 09 Sep 2024 23:04:42 GMT  
		Size: 21.0 KB (20972 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:6f842f8998fe08cfdcb13cd83a7d09dfee91b25ae8b6937b02702480c5c55d22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32323662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d5a34a6f646baa48f817d457c47eb9762e5066adc40bc80cded7232eacb00d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 22:15:45 GMT
ADD file:9ffa4d53a074e91efecf5e26e3b67077f46165e0d042c1e6cf1b93c531ed2bc4 in / 
# Wed, 04 Sep 2024 22:15:50 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:89502a0eae32ab684bc9df3d9922ee2874839b178a693286c4b866f5ca8e93f3`  
		Last Modified: Wed, 04 Sep 2024 22:24:11 GMT  
		Size: 29.1 MB (29125054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a544e9e80cb1c7ab6c5794cb1a0a4715aa0df1fd8437a0d771017c52f3e5f5`  
		Last Modified: Thu, 05 Sep 2024 11:18:11 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7605e144a412910a4194cfffafd5d127bc44e9b19ba5191b74df2cc6a267f2e0`  
		Last Modified: Thu, 05 Sep 2024 11:18:12 GMT  
		Size: 1.9 MB (1942689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92a7d1694bf26de03563c78b52328eeabf26a387feba7ff6fbb8bb253427f27`  
		Last Modified: Tue, 10 Sep 2024 02:25:37 GMT  
		Size: 1.3 MB (1254404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c99675ddde9651d74c5ef49e2a70ca2c3351852fb856272dfb9b5f328a69e31`  
		Last Modified: Tue, 10 Sep 2024 02:25:37 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859d2e9814139aaf71bc0d3cc5e5eecdba1d8f10c4cc0196aa46b58d2830bebe`  
		Last Modified: Tue, 10 Sep 2024 02:25:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:6c4530d40688ecfde5ff475267c0fd60f9d67cd7e23c5e177ae0e20937467413
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e60bb1c6684aec9c40b2deb99de2c399adb2682fdc6efecdd98aef1881475ac`

```dockerfile
```

-	Layers:
	-	`sha256:74c8d993dc8b0fbc1c7708b04cec649eac5a3f36f5bc171bc1d523edc126aeff`  
		Last Modified: Tue, 10 Sep 2024 02:25:37 GMT  
		Size: 20.9 KB (20911 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:a2c15d4ae7e15fa7457c5f843feb6bfc17bf3a4ee8c7fe278e9af0824a54be80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37154878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4f56f782d0ddfeacfa04a2d1bc62b4ee9938d6128b8c29f12647454f427251e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 22:25:52 GMT
ADD file:d83b2f8d4d3fd22a390140e3bebefb48e5f086d072ad6062f6446b4fc42ec7a8 in / 
# Wed, 04 Sep 2024 22:25:54 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f19b11698292330b7d980ed50b0141417eec298d865e0c1b305ce7a8b80b572d`  
		Last Modified: Wed, 04 Sep 2024 22:30:11 GMT  
		Size: 33.1 MB (33122358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ee1834d6aa97efd9d43db3a50a5bb3dda4b08400d531f72579cadea051609e`  
		Last Modified: Fri, 06 Sep 2024 22:02:56 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9152281fc8ce1403b29050f252829939c461cf037d8b3491653f7eeee4ece43`  
		Last Modified: Fri, 06 Sep 2024 22:02:56 GMT  
		Size: 2.7 MB (2707191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e141823a412ee63afdae23f927aa51b3eb72dd45577cf194159595a77d4577e2`  
		Last Modified: Tue, 10 Sep 2024 00:53:10 GMT  
		Size: 1.3 MB (1323809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c8e76a6f99b8b59c45f2a7eea7a5ee3870791b1a3abe6679881522a171e998`  
		Last Modified: Tue, 10 Sep 2024 00:53:10 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc7d2a375bf95c80dfd28c577fb84d803a9bb9437dd19ebc1801f99fb035120`  
		Last Modified: Tue, 10 Sep 2024 00:53:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:3bd251857bd96c65b8ad1e08a21c64177e673356369ff7404be1ba2edac796b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4713e2ddd75a9c1fba28b6cf8191e2ed2cb6b5e47a06bcb2db95a9efbbc74fda`

```dockerfile
```

-	Layers:
	-	`sha256:ca0b1f85d6ea571ab124bed1c494d1d8fb6673a42d0cb794a3eb947b1e1f9b06`  
		Last Modified: Tue, 10 Sep 2024 00:53:10 GMT  
		Size: 2.3 MB (2285050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73f6f1fc8ce970b2f59c4b67cfef86ef3c1dc692d3e5b91930a0f834c2aa8286`  
		Last Modified: Tue, 10 Sep 2024 00:53:10 GMT  
		Size: 21.1 KB (21095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:a564ae9d7581535075625ac57d9c0b961354e9b4daba7c4b8081f9c94a7272cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30885604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0553326148f76a8da67990b40b3cda91d5eb09e6450645d355301f64cdd62ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 21:42:50 GMT
ADD file:728128617ba2b026c358eb266cd495be84354c4e5dc4ecc2953cb829190a4546 in / 
# Wed, 04 Sep 2024 21:42:52 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:95fe27c895a828dc681ee4a0cbea0264c47528dad525efdb9641a375666536bd`  
		Last Modified: Wed, 04 Sep 2024 21:47:41 GMT  
		Size: 27.5 MB (27490321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14930957f1690905df41f1da11505509319dd65a7de378761ed685a7f319746`  
		Last Modified: Fri, 06 Sep 2024 22:03:27 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0833ee43e72a5f44318da8b85bdf6aa1bb3bddf0fdd75dc5530531a126eb97`  
		Last Modified: Fri, 06 Sep 2024 22:03:27 GMT  
		Size: 2.2 MB (2155800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49ba017e9517b59a0101e268f88f7b430651242d3de79201588254bb0fe7507`  
		Last Modified: Mon, 09 Sep 2024 23:57:11 GMT  
		Size: 1.2 MB (1237972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f824a2d96ada01e3ba546f908f36e9780321cfd73e3145903949cd6f8d9bbc`  
		Last Modified: Mon, 09 Sep 2024 23:57:11 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c979fb5ce067e0a4128dc5527a66b9ee1bf3762c94b5f309c473ede06b29be`  
		Last Modified: Mon, 09 Sep 2024 23:57:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:d96f09ec7f4c6e807df2fac9bd6834a30ab928672e82902cd5cc756d638221a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d39e3cfd9222897db8d98adeddedd43e35a75647f77cf2ca9276356feeb1695`

```dockerfile
```

-	Layers:
	-	`sha256:d83c73c94a489231e85f509c8c17651508a61d8aa02ef340f03babd8b3a5253b`  
		Last Modified: Mon, 09 Sep 2024 23:57:11 GMT  
		Size: 2.3 MB (2280500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b7064082e2a2543d417d8956bcd38d8aa02707fd3284afe698b5e0c00f111b1`  
		Last Modified: Mon, 09 Sep 2024 23:57:11 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:latest`

```console
$ docker pull memcached@sha256:51cdb01f624e1eab205f978b21756cf3ef96ca33da2cd074cb47245b92e0705f
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

### `memcached:latest` - linux; amd64

```console
$ docker pull memcached@sha256:a658d819b6f9ab244148f9e9994489e759ff72e12cd2a93cf0a9b0259f324743
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32878406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a783d40c8b808e6a5c1d562c8ddf24732920c2c1b7e12eadaeb76b3f1e468b32`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 07 Sep 2024 18:54:11 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d937ff39f058bf2417a4fe760827ff36b1b38be77ed6c3b27fbd80872b4106b9`  
		Last Modified: Fri, 27 Sep 2024 06:05:04 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2bb47e18c2052b1e07d1957f90f1d197fcbf398748e534e8fa54f75782b3fff`  
		Last Modified: Fri, 27 Sep 2024 06:05:04 GMT  
		Size: 2.5 MB (2491322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c618990832780ea1a130f360744ad52c95ef7485138ded320b5563aedc090b`  
		Last Modified: Fri, 27 Sep 2024 06:05:04 GMT  
		Size: 1.3 MB (1259299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f09b0e04f54ca243201f3b8f205c759c2892f6752f8e75aa84434ab4a4b330`  
		Last Modified: Fri, 27 Sep 2024 06:05:04 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2038e2b3f99ec442dfe1024270c1ad10a59fb8995060bc0a2e7a6831bbc48917`  
		Last Modified: Fri, 27 Sep 2024 06:05:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:2fbb3c4bddfc491f239cbe76e97dbd05fa35514c183e7fa4ac819cda30fd5acf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b83b1908356b5b8567c67431165b1c6e4a18a87b108cb329988349341ed52f3e`

```dockerfile
```

-	Layers:
	-	`sha256:e0ac909638f1cc11061867d2eca41aafdfd8ac0189cceb25a5aa9c4ff9c7f0fc`  
		Last Modified: Fri, 27 Sep 2024 06:05:04 GMT  
		Size: 2.3 MB (2280692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c438d6540bdc9adc9140d94352ea4200a10e7cfc1168f6b3c47c8202fe19ace1`  
		Last Modified: Fri, 27 Sep 2024 06:05:04 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm variant v5

```console
$ docker pull memcached@sha256:365ca3a58f4ec2be52314d56ca69b149210604be3008c503c731cf5f4a095f5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30222872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43b582780474a2688f3e337b9c5a04bcf5697372ab5e9377d88e069e75607247`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 21:48:32 GMT
ADD file:c162e60b24ef6aed489ba1986f407fd9ab4ace659e0e3e6759ffac7eb0b7f770 in / 
# Wed, 04 Sep 2024 21:48:32 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:44990bd21e0c5db65674bd030d12ea2461a14f2bb4007469bc2667c8535a8357`  
		Last Modified: Wed, 04 Sep 2024 21:51:32 GMT  
		Size: 26.9 MB (26887411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a8ee21aa62c2c20c62d17e0dd3670c4484279b7481df253ab7dea06579e38f6`  
		Last Modified: Thu, 05 Sep 2024 03:28:45 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e5212bff7c052802224f0dcd2c61c47f77a42869600109756dedd710f28915`  
		Last Modified: Thu, 05 Sep 2024 03:28:46 GMT  
		Size: 2.1 MB (2095647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0782223d771fbfcf1c9ed4475479f748c453dd6aa6dc53aa45361cd00224de57`  
		Last Modified: Tue, 10 Sep 2024 02:36:03 GMT  
		Size: 1.2 MB (1238299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530caa10c823e2b669f21afaf522a557d974f4ea259b23e29b5a88c357559aa9`  
		Last Modified: Tue, 10 Sep 2024 02:36:02 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2f95efd2295adb5abdb3e0e56c5d975248bcc1c4951cedbfc5f10c2480cb9c`  
		Last Modified: Tue, 10 Sep 2024 02:36:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:643f24e07712d430691849d647e01c9ba7828371296a20fbe49250e582c0fac2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8e2f351cd6f24d1550b56f8e379b3e6aef1289d89b131237317ca600e4d52a0`

```dockerfile
```

-	Layers:
	-	`sha256:6d0e93f21d109f38cd7d09c5fc37735dc06c58bfcc63c9e950d187b500196f7b`  
		Last Modified: Tue, 10 Sep 2024 02:36:03 GMT  
		Size: 2.3 MB (2284110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:877d052619f8f882ecca7bddd9b19ea3ac0aff81603a8e053c4cfef2c753b056`  
		Last Modified: Tue, 10 Sep 2024 02:36:02 GMT  
		Size: 21.2 KB (21169 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:875cd34f6465e3e8fa28ef5db4bfad8c176e1c0263daff0171fc9537b0ca3a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32767698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a91d45790f325414f2734648e019a463d8d1353ca9250b2700504151dcdfbbe0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:52 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Wed, 04 Sep 2024 21:39:53 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04865bf94e709891a3952f6be4719f98f7a66c94aeb7ca127b805a21559f233b`  
		Last Modified: Fri, 06 Sep 2024 22:18:47 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2accb5dc3319c683f0fcfa968e975b4170700c037764eba741ba2d1c52c8ad0a`  
		Last Modified: Fri, 06 Sep 2024 22:18:47 GMT  
		Size: 2.4 MB (2354829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099212eee1d8aedc74760284b20c722ff3262dfeebadb7801f18e140dd2a88c4`  
		Last Modified: Tue, 10 Sep 2024 05:26:27 GMT  
		Size: 1.3 MB (1254813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfbc137765c6a6be5ae31943c75d26fb8556d6f8d6dc7372cba395a51e9600c8`  
		Last Modified: Tue, 10 Sep 2024 05:26:27 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6847381e1607ee0f70837cb4d081424ec06929f39c8c350ff85944aef711304c`  
		Last Modified: Tue, 10 Sep 2024 05:26:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:56255e99acdfe342a7754928cb5ed717ab5f7372c48426d0dc8b1515d05a4b4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:336d6748c4ae106ed4adc2a8b4c756622427e4066c4aa1351246e7a0fe352da8`

```dockerfile
```

-	Layers:
	-	`sha256:29df9c8dc456cfd5983e243674508af61ff397da6d8d6a997e017e85a4e4266c`  
		Last Modified: Tue, 10 Sep 2024 05:26:27 GMT  
		Size: 2.3 MB (2280993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d304f0d86e38bf9bc9ed7714e76015b79876a10b2d8c67f081473bfdcabe377`  
		Last Modified: Tue, 10 Sep 2024 05:26:27 GMT  
		Size: 21.4 KB (21385 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; 386

```console
$ docker pull memcached@sha256:34dcfa089dd249a4df38d93bee834b8e9ef0f20fc783cc57beecc31eb4e04fcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33904516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7bacc013d82d74a63cc6ad50eec7918e02e35d93e1138cd7405cb396e80b5a3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 22:44:34 GMT
ADD file:1d96491aed0d3091aadb984e1dfe642343013348f4a1807a69e132efaed68030 in / 
# Wed, 04 Sep 2024 22:44:34 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c304282df09b425e8240f53c55110ac282ba801da157a805e4fdbdf8c832b376`  
		Last Modified: Wed, 04 Sep 2024 22:48:08 GMT  
		Size: 30.1 MB (30144294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6c5637a99c0d5bfbc04c2f481699f0ab6cbcf940efabacc33b17680528fcb1`  
		Last Modified: Mon, 09 Sep 2024 23:04:42 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7a2b527feff9ff4df7dcb2a0b26ec01a6fa914c48cfb3bba0d873a5f7ae189`  
		Last Modified: Mon, 09 Sep 2024 23:04:42 GMT  
		Size: 2.5 MB (2499306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d54ad1af4809e5533f75ab13f83a284e966f4bdf5df4880fba412f3fa6e415`  
		Last Modified: Mon, 09 Sep 2024 23:04:42 GMT  
		Size: 1.3 MB (1259401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:683954138ef3ece20193896fd5a5df2deb974514c9f939d749eb46c161f1e4f6`  
		Last Modified: Mon, 09 Sep 2024 23:04:42 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d4e2b90164f16b0893ff5354664d43d05f691e1ef4165d1f45889cfaa8bc68`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:5f5144206a28ac6d02a6064d09bef45ba19ea0e834380667b5252173fc1aee2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2298749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c582914882b6e0802c0ff6073312ad790deb59006c1edeeca6423351ecc04295`

```dockerfile
```

-	Layers:
	-	`sha256:08d010ee1407ba55007943c5783e18992fce487cf9fc06f1001a6c6ee139ad50`  
		Last Modified: Mon, 09 Sep 2024 23:04:42 GMT  
		Size: 2.3 MB (2277777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8dabd61e7f4bdb4bd9a53e403b676e865ad1ec09201180b76f03117a501c2d7`  
		Last Modified: Mon, 09 Sep 2024 23:04:42 GMT  
		Size: 21.0 KB (20972 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; mips64le

```console
$ docker pull memcached@sha256:6f842f8998fe08cfdcb13cd83a7d09dfee91b25ae8b6937b02702480c5c55d22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32323662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d5a34a6f646baa48f817d457c47eb9762e5066adc40bc80cded7232eacb00d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 22:15:45 GMT
ADD file:9ffa4d53a074e91efecf5e26e3b67077f46165e0d042c1e6cf1b93c531ed2bc4 in / 
# Wed, 04 Sep 2024 22:15:50 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:89502a0eae32ab684bc9df3d9922ee2874839b178a693286c4b866f5ca8e93f3`  
		Last Modified: Wed, 04 Sep 2024 22:24:11 GMT  
		Size: 29.1 MB (29125054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a544e9e80cb1c7ab6c5794cb1a0a4715aa0df1fd8437a0d771017c52f3e5f5`  
		Last Modified: Thu, 05 Sep 2024 11:18:11 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7605e144a412910a4194cfffafd5d127bc44e9b19ba5191b74df2cc6a267f2e0`  
		Last Modified: Thu, 05 Sep 2024 11:18:12 GMT  
		Size: 1.9 MB (1942689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92a7d1694bf26de03563c78b52328eeabf26a387feba7ff6fbb8bb253427f27`  
		Last Modified: Tue, 10 Sep 2024 02:25:37 GMT  
		Size: 1.3 MB (1254404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c99675ddde9651d74c5ef49e2a70ca2c3351852fb856272dfb9b5f328a69e31`  
		Last Modified: Tue, 10 Sep 2024 02:25:37 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859d2e9814139aaf71bc0d3cc5e5eecdba1d8f10c4cc0196aa46b58d2830bebe`  
		Last Modified: Tue, 10 Sep 2024 02:25:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:6c4530d40688ecfde5ff475267c0fd60f9d67cd7e23c5e177ae0e20937467413
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e60bb1c6684aec9c40b2deb99de2c399adb2682fdc6efecdd98aef1881475ac`

```dockerfile
```

-	Layers:
	-	`sha256:74c8d993dc8b0fbc1c7708b04cec649eac5a3f36f5bc171bc1d523edc126aeff`  
		Last Modified: Tue, 10 Sep 2024 02:25:37 GMT  
		Size: 20.9 KB (20911 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; ppc64le

```console
$ docker pull memcached@sha256:a2c15d4ae7e15fa7457c5f843feb6bfc17bf3a4ee8c7fe278e9af0824a54be80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37154878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4f56f782d0ddfeacfa04a2d1bc62b4ee9938d6128b8c29f12647454f427251e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 22:25:52 GMT
ADD file:d83b2f8d4d3fd22a390140e3bebefb48e5f086d072ad6062f6446b4fc42ec7a8 in / 
# Wed, 04 Sep 2024 22:25:54 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f19b11698292330b7d980ed50b0141417eec298d865e0c1b305ce7a8b80b572d`  
		Last Modified: Wed, 04 Sep 2024 22:30:11 GMT  
		Size: 33.1 MB (33122358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ee1834d6aa97efd9d43db3a50a5bb3dda4b08400d531f72579cadea051609e`  
		Last Modified: Fri, 06 Sep 2024 22:02:56 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9152281fc8ce1403b29050f252829939c461cf037d8b3491653f7eeee4ece43`  
		Last Modified: Fri, 06 Sep 2024 22:02:56 GMT  
		Size: 2.7 MB (2707191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e141823a412ee63afdae23f927aa51b3eb72dd45577cf194159595a77d4577e2`  
		Last Modified: Tue, 10 Sep 2024 00:53:10 GMT  
		Size: 1.3 MB (1323809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c8e76a6f99b8b59c45f2a7eea7a5ee3870791b1a3abe6679881522a171e998`  
		Last Modified: Tue, 10 Sep 2024 00:53:10 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc7d2a375bf95c80dfd28c577fb84d803a9bb9437dd19ebc1801f99fb035120`  
		Last Modified: Tue, 10 Sep 2024 00:53:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:3bd251857bd96c65b8ad1e08a21c64177e673356369ff7404be1ba2edac796b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4713e2ddd75a9c1fba28b6cf8191e2ed2cb6b5e47a06bcb2db95a9efbbc74fda`

```dockerfile
```

-	Layers:
	-	`sha256:ca0b1f85d6ea571ab124bed1c494d1d8fb6673a42d0cb794a3eb947b1e1f9b06`  
		Last Modified: Tue, 10 Sep 2024 00:53:10 GMT  
		Size: 2.3 MB (2285050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73f6f1fc8ce970b2f59c4b67cfef86ef3c1dc692d3e5b91930a0f834c2aa8286`  
		Last Modified: Tue, 10 Sep 2024 00:53:10 GMT  
		Size: 21.1 KB (21095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; s390x

```console
$ docker pull memcached@sha256:a564ae9d7581535075625ac57d9c0b961354e9b4daba7c4b8081f9c94a7272cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30885604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0553326148f76a8da67990b40b3cda91d5eb09e6450645d355301f64cdd62ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 21:42:50 GMT
ADD file:728128617ba2b026c358eb266cd495be84354c4e5dc4ecc2953cb829190a4546 in / 
# Wed, 04 Sep 2024 21:42:52 GMT
CMD ["bash"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:95fe27c895a828dc681ee4a0cbea0264c47528dad525efdb9641a375666536bd`  
		Last Modified: Wed, 04 Sep 2024 21:47:41 GMT  
		Size: 27.5 MB (27490321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14930957f1690905df41f1da11505509319dd65a7de378761ed685a7f319746`  
		Last Modified: Fri, 06 Sep 2024 22:03:27 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0833ee43e72a5f44318da8b85bdf6aa1bb3bddf0fdd75dc5530531a126eb97`  
		Last Modified: Fri, 06 Sep 2024 22:03:27 GMT  
		Size: 2.2 MB (2155800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49ba017e9517b59a0101e268f88f7b430651242d3de79201588254bb0fe7507`  
		Last Modified: Mon, 09 Sep 2024 23:57:11 GMT  
		Size: 1.2 MB (1237972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f824a2d96ada01e3ba546f908f36e9780321cfd73e3145903949cd6f8d9bbc`  
		Last Modified: Mon, 09 Sep 2024 23:57:11 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c979fb5ce067e0a4128dc5527a66b9ee1bf3762c94b5f309c473ede06b29be`  
		Last Modified: Mon, 09 Sep 2024 23:57:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:d96f09ec7f4c6e807df2fac9bd6834a30ab928672e82902cd5cc756d638221a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d39e3cfd9222897db8d98adeddedd43e35a75647f77cf2ca9276356feeb1695`

```dockerfile
```

-	Layers:
	-	`sha256:d83c73c94a489231e85f509c8c17651508a61d8aa02ef340f03babd8b3a5253b`  
		Last Modified: Mon, 09 Sep 2024 23:57:11 GMT  
		Size: 2.3 MB (2280500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b7064082e2a2543d417d8956bcd38d8aa02707fd3284afe698b5e0c00f111b1`  
		Last Modified: Mon, 09 Sep 2024 23:57:11 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json
