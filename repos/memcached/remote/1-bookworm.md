## `memcached:1-bookworm`

```console
$ docker pull memcached@sha256:5231c344fa8941a6c81b2b28189a3dd9f451a08048f8cecbd9858990599496c3
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
$ docker pull memcached@sha256:620ecea8deb528e3e893f8662d2cd322c475190024d502f0c07063e6abfed93d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32878602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e7ce60dbfae9a3eef8fc3ffcbccc3b5af34889857e8b3e696acfda2f3731e63`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:47 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Wed, 04 Sep 2024 22:30:47 GMT
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
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5daf70fef96378c7f8b4ca1a442a4e51217ee222de6b4b64ea750067deb882a`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b7f6e48c9927d830a3f205954a49a9035a557c52d8f685ab3bce04a497d1f9`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 2.5 MB (2491329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759ef1ab0c87bae1805e5e79f7a7f34b77c091f7c7e4fb9d63e5776850349644`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 1.3 MB (1259277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5823fa7609d8b81f325d4505bd66a4d923bfb8bcb19e9880d1406f0b24a4ed1c`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5565e224421e7e82bb8bdadbfdea11b6426688532c964b8728942cc8fa9bba58`  
		Last Modified: Mon, 09 Sep 2024 23:04:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:d124cfe1c0f5925870e7b810ccd8e9b84b7ae57bbc8cb257f601580241791ba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3248b9e15894a60958e3f3f1c66564b4f2c8d0ee7bed5a625e90cfbc05e1fe82`

```dockerfile
```

-	Layers:
	-	`sha256:4ce33d17ddcf76504f0aa552cf3d99b59393d3b6cb3df1b41ecc8b6aa6ca6fb1`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 2.3 MB (2280679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3117473d00805fdb2ec6c70aacc5fe5de29e63a09abf3876f509a362a096311`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
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
$ docker pull memcached@sha256:8f6cedb3f9f70ae2e491224e7f0f380fbeadfdb25d000e66cee2cda70f797405
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32767634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c9dfadf53cf218d4f5087fc40b1c2b67f0924ecad5a35ea70f8f9955c640359`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:52 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Wed, 04 Sep 2024 21:39:53 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
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
	-	`sha256:8e347b6bbc062475d080bedc03d636e26305ce03600c644fe514c2847a7d9264`  
		Last Modified: Fri, 06 Sep 2024 22:18:47 GMT  
		Size: 1.3 MB (1254750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a85e8571505effdc6e68311cf17c4f6d2abfc2945b155d284628f88505bbba8`  
		Last Modified: Fri, 06 Sep 2024 22:18:47 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b66bb924137a98866e534194d5f2a6cf3d778fcc56a210a1f06287bf3d1cbe4f`  
		Last Modified: Fri, 06 Sep 2024 22:18:48 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:66f09614b8645eb926793c445977404c55bb5479e153264d85717363cbf9b017
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0340976a032fcd3dad02a0d55c94a0d8001909ff3936483b6bbf17d73592c481`

```dockerfile
```

-	Layers:
	-	`sha256:628223a69e93a557d96659afcec9be5696cc1df83d5e5d97f82097f3f2dc7df8`  
		Last Modified: Fri, 06 Sep 2024 22:18:47 GMT  
		Size: 2.3 MB (2280993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebf9ac81c8d90f484e3ccc3c12919eca89305cc060f566cb28b1fcb376116005`  
		Last Modified: Fri, 06 Sep 2024 22:18:47 GMT  
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
