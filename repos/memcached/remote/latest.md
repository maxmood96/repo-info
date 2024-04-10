## `memcached:latest`

```console
$ docker pull memcached@sha256:1afd569c56493154173398bb556a56def24268a450f05c14275b24357ce96631
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
$ docker pull memcached@sha256:2967dc980ac80883003061c899102ed6c8749ed50712d4cf592b7c53efd7a498
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32872677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7787f9f0d27b97ee6da8b7b2fdf9dec18a1c0fa6c05b0d4a454cc84138bfceb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 05 Apr 2024 21:52:05 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
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
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:131f56ef3fe0a1487206d17cc66325f94d97854c231561697099f0162c37a033`  
		Last Modified: Wed, 10 Apr 2024 02:57:18 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa35112bf68c5c494491a4c7fbbb8ba5e4d9d410ce9150f1b3238414cbc091b0`  
		Last Modified: Wed, 10 Apr 2024 02:57:19 GMT  
		Size: 2.5 MB (2488500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a672c032d4a7b7c0de949d9fe1d4896cc7da42256b16e1daba353de964968b8`  
		Last Modified: Wed, 10 Apr 2024 02:57:18 GMT  
		Size: 1.3 MB (1251305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e01135bb689569cd15c6a2b8d8e115947652e4d61a01127729ea24513d1f57d2`  
		Last Modified: Wed, 10 Apr 2024 02:57:18 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48f53906ef45e3138f6a1f1ee8ebd01ca24a3c3a2c15301afe932077984afbb`  
		Last Modified: Wed, 10 Apr 2024 02:57:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:ace7b79050b8d00e7046345e319209248f2ce44b7b3a67968e6662d559b4cebe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0612146bf8ed0f19690c2070f49b81b2f59f0df0c0aee6b38606b04c32b3b1bc`

```dockerfile
```

-	Layers:
	-	`sha256:cbbd757e27c72cb57f0f51a89cb3d65360e0afa594c47eff406c9db9d3a27de0`  
		Last Modified: Wed, 10 Apr 2024 02:57:18 GMT  
		Size: 2.3 MB (2261161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d398ef36731f34f7e28948dd252f5bd1ec36dbc3a4f7b23dd7fc9d195992db2`  
		Last Modified: Wed, 10 Apr 2024 02:57:18 GMT  
		Size: 21.1 KB (21142 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm variant v5

```console
$ docker pull memcached@sha256:7161782b9d363059b65a6af8ea9de69504dd1be1a90f7025cf0d0459d5135221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30206296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b79e2ec3e3c389038f672897f755e7988dd716500ad345b8468a20bd7bb62149`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 00:48:31 GMT
ADD file:b1bd2ec7dd2a8894ea7b5837afba4e15ba798f4809586f0ac1b8855bd0032651 in / 
# Tue, 12 Mar 2024 00:48:31 GMT
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
	-	`sha256:e250365604bf1f3b73bc7378ee29efbff0b147bc6534a00cb34f46c46d95c9a4`  
		Last Modified: Tue, 09 Apr 2024 05:07:07 GMT  
		Size: 1.2 MB (1231284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be19c46e8aaa16feb6388ed0533114ec0b10f90a5812796e0142cb2a2fbfe343`  
		Last Modified: Tue, 09 Apr 2024 05:07:07 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ceaf8b435ef512cb41c1b4c89a5c503f80df9ac438b63706f8aea1852cb893`  
		Last Modified: Tue, 09 Apr 2024 05:07:07 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:ca566403578280e2ec4f616d6eca610eaae9c0cc67d383e8edda60c022ba0421
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2286849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f4c6a4232d7fbaa5f4890edb2420e9712ce05aa224f28e37982be032ce3b044`

```dockerfile
```

-	Layers:
	-	`sha256:1efdd8a782e7292d7e86c490c1ecf6784d706a79bb20fcd1eea7e58cb221c9c4`  
		Last Modified: Tue, 09 Apr 2024 05:07:08 GMT  
		Size: 2.3 MB (2265733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cfadf34092d8c3aa720e880c8be7b6c3da96d77723357d9eb377f78b47ba98c`  
		Last Modified: Tue, 09 Apr 2024 05:07:07 GMT  
		Size: 21.1 KB (21116 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:0b7a2cdf5534cc7e79394c29cc487ee4db92d8de636de6d80a49636b7a8ccd93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32752620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4745c1ded4bd3704e9a5c557290da38fa2d04cbf0673ab340bded6a255858e58`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:36 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Tue, 12 Mar 2024 00:45:37 GMT
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
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac48a97998740def0fa8b1b7e818bbec003d87e56636ed14d66e8ea9c1b49c18`  
		Last Modified: Wed, 20 Mar 2024 22:05:32 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e6aa77c2974c982d56d398f0e7fde37261a6e629e0ae13bd38cbcfbc94d0f2`  
		Last Modified: Wed, 20 Mar 2024 22:05:33 GMT  
		Size: 2.3 MB (2346182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b29a5a5612b938e90c4d775802759955740bcda0f4c0bd5648404b7d77f686`  
		Last Modified: Tue, 09 Apr 2024 06:35:19 GMT  
		Size: 1.2 MB (1248490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0290be2fc72e6d6c5ae154981ea6f07773c8b0d4f39a21eed501db4da197043`  
		Last Modified: Tue, 09 Apr 2024 06:35:19 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07324f2054ca8b0ab5da55f38bb3734f1deb6194bd4a9e9146ea6596b2db72b9`  
		Last Modified: Tue, 09 Apr 2024 06:35:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:b3c7c52e0bb518dd090bbcf5b5275284e5829391a3e7f1bbb8b83956385733c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2283667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7fa1cc8e9d009a8da236baba804ffe59e8d0f47df3a86b34960ef623b26075c`

```dockerfile
```

-	Layers:
	-	`sha256:ec496c1b959e2bb8206e8b2065945cbd9755086141d7964776b2732a38f50f94`  
		Last Modified: Tue, 09 Apr 2024 06:35:19 GMT  
		Size: 2.3 MB (2262674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:128fd8be992e3d9d5a7acd6e561ee371b0edd3f62f845bd955aa932de23e40fd`  
		Last Modified: Tue, 09 Apr 2024 06:35:18 GMT  
		Size: 21.0 KB (20993 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; 386

```console
$ docker pull memcached@sha256:e2b64885e9a784d1da7cf944a72781bd5d676a4304d62bce3568bedbc24e7822
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33888676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65e9b5bac07c4744cc812d66d035824076e0f0d57b9019e26590936993287923`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 00:57:59 GMT
ADD file:88f04d79dc9f1691544c636ff52d6744a2ff68d504793ea8034b797d0bfc6fd3 in / 
# Tue, 12 Mar 2024 00:58:00 GMT
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
	-	`sha256:576af7ffb10b3f3b8d5523e6b91da8667eb39393cdfd50fb26dfc178e504ba70`  
		Last Modified: Tue, 12 Mar 2024 01:02:43 GMT  
		Size: 30.1 MB (30141873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6958130e47aeaaeb72d42b669e8f29b90de0544391e16fad7f0268570062180`  
		Last Modified: Mon, 08 Apr 2024 22:02:40 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff93d852593aef3b8eb10b1b4e206a3d03ccf2c655cd624793b91503a457aafa`  
		Last Modified: Mon, 08 Apr 2024 22:02:40 GMT  
		Size: 2.5 MB (2492657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f8c4840ec264f12d2a2ff2b79461d3e0b32edb9e96521d742938d4a1f41ca49`  
		Last Modified: Mon, 08 Apr 2024 22:02:40 GMT  
		Size: 1.3 MB (1252629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83170a1a8d1b8c664a8715a4b7b81f6d62987e9b122d5762bbd11f083ca138f2`  
		Last Modified: Mon, 08 Apr 2024 22:02:40 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4315b7d3add1ca8ec255536a6ceaf95e98db079deb29e3ce42bf7553e0d8b81`  
		Last Modified: Mon, 08 Apr 2024 22:02:40 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:986876f14377a977ff648f9622ae77f3c4016669a134ad9b9260c04bf55fdf3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2280630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7612e4d58dbc473107f7587a1da1aad0c5c9eeb89238ccb469f7a4a7db3662ad`

```dockerfile
```

-	Layers:
	-	`sha256:39f9a811984e9ba97b4619d674dc4ee0d40be9404b0c1dfd948a2253e9ec1b81`  
		Last Modified: Mon, 08 Apr 2024 22:02:40 GMT  
		Size: 2.3 MB (2259543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:537ea3eb55595d0fe6b97f63a5ef597904de6fcfc865865ff747c59b9a892fb3`  
		Last Modified: Mon, 08 Apr 2024 22:02:40 GMT  
		Size: 21.1 KB (21087 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; mips64le

```console
$ docker pull memcached@sha256:fc8892b557a9bdb7b41273e3403bc2fdb3d04f99fb56a3874e9081d8dfa128d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32306668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99a48487cefaf60f8ad4d3a059b0db4796bee3adbf408393dcc4c49da664f723`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 01:06:19 GMT
ADD file:c03c59e261bb08f39e6a97df2fd4b82f1e11b49a62d1859a8f8efac680b80a88 in / 
# Tue, 12 Mar 2024 01:06:23 GMT
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
	-	`sha256:aad79459a0f767fcded51c9547150a1cfd96638972389ab8621b5f3eb4a9c280`  
		Last Modified: Tue, 12 Mar 2024 01:17:09 GMT  
		Size: 29.1 MB (29119205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460befff49885c738329c53c06bca553e2869317c73b0b5f76661a7053f578ad`  
		Last Modified: Tue, 09 Apr 2024 15:25:07 GMT  
		Size: 1.1 KB (1117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6dc8cf2380155c1bacde757237b8551c77167e46ac5393332be9deb2b8dbc5`  
		Last Modified: Tue, 09 Apr 2024 15:25:07 GMT  
		Size: 1.9 MB (1937657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66db33dc07294fd7ecc848862384efa6b829c96c8939643a7098e35bbbe81d8f`  
		Last Modified: Tue, 09 Apr 2024 15:25:07 GMT  
		Size: 1.2 MB (1248284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1650df259f3af60ff6184e164ac094f261bffea30679d803c7cff2759e001699`  
		Last Modified: Tue, 09 Apr 2024 15:25:07 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a51c337d2a6d822be89d42ae3e0ae8472dbd1673e648f8cdf1c769309105aaca`  
		Last Modified: Tue, 09 Apr 2024 15:25:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:831ec04c94a8b50c1aff4f18c97c8cae1d537c32821a0b8aeca9b0a1aecacae2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7033955a79b1242de9912088e5d0f703e2133fce52308636758ba5ce2059d38c`

```dockerfile
```

-	Layers:
	-	`sha256:abd2f28a59a5e89ae224244ff2945a51f564194853e6abaaa8f5648413960325`  
		Last Modified: Tue, 09 Apr 2024 15:25:07 GMT  
		Size: 20.9 KB (20862 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; ppc64le

```console
$ docker pull memcached@sha256:dc36455fb79f84d62ac6d34100afc15f0a238192dfa3224e93f753cd67d74798
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37135966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:430a51910c252bd83b91329bef7a7f1a2344a5bc6b42075d419bb0facc468286`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 00:30:19 GMT
ADD file:9273ef56d086dbc93b46b7e8ae424eb04096fb00c693dd6cda1f48346290d4d5 in / 
# Tue, 12 Mar 2024 00:30:24 GMT
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
	-	`sha256:c28cd0e276dcdeb4d44f5cc5bb958610750ff902a081b668e3863c2f38eef054`  
		Last Modified: Tue, 12 Mar 2024 00:38:06 GMT  
		Size: 33.1 MB (33119023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708b42bb3654f69ef8bfee96e8cd256f668ec36c0c79dffa3833c5a717f9eb5f`  
		Last Modified: Wed, 20 Mar 2024 21:57:50 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c66c4756024ccda97c6fbe022e48d010bf3335191ef2516ace6ee30de5e87389`  
		Last Modified: Wed, 20 Mar 2024 21:57:51 GMT  
		Size: 2.7 MB (2698368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ea5604f0c8a697cb056d47640ff8d8852849f35d9a26e62b42036629bcaf9c`  
		Last Modified: Tue, 09 Apr 2024 05:05:54 GMT  
		Size: 1.3 MB (1317055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810d9546da33f92c2106ed1bbfc26223b8bef8f8e2be48b862a0270380818526`  
		Last Modified: Tue, 09 Apr 2024 05:05:54 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c78ea7da271614754f4fdc7e7d86c64da966e871cce4bab839266e27bd62912`  
		Last Modified: Tue, 09 Apr 2024 05:05:54 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:a78edf1158eed48cbec064a641fcac3c873e1b1fee26b1d8407a0269870baa23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2287859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:618f6dcb01dc21ed0cc62f7efaeabc4c883f32d56e5f51a66cba2e87b31ed783`

```dockerfile
```

-	Layers:
	-	`sha256:13692af6f7d1860a31d9a8610f75d0d12eaa87131aef9b5615a57c5aaad34643`  
		Last Modified: Tue, 09 Apr 2024 05:05:54 GMT  
		Size: 2.3 MB (2266816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eae96d76b66c8c2450ce3e926ee185c9043ceff0f51f91e18694e094fd6d91af`  
		Last Modified: Tue, 09 Apr 2024 05:05:53 GMT  
		Size: 21.0 KB (21043 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; s390x

```console
$ docker pull memcached@sha256:3af0cb7bc651113fdea970716a6f0a534823c322990bacbde20cc166648bb952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30873795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9d9bcea2e734469166d18b5a96ac76cdcd310b4c95140b542777073e6158051`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 12 Mar 2024 00:54:02 GMT
ADD file:80ab985d4871ca6a72156bedfe1038e6b1a89591fc2fd86c4ef778d293223aff in / 
# Tue, 12 Mar 2024 00:54:03 GMT
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
	-	`sha256:9cada496cd2b8a88571bf23d513e7fce34888d13321fcf23c6613bffe4c37297`  
		Last Modified: Tue, 12 Mar 2024 01:21:14 GMT  
		Size: 27.5 MB (27488684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c430faffa085700d40355ac1aea08d429376e112bef3b9c00780b1ede56859c2`  
		Last Modified: Wed, 20 Mar 2024 22:17:08 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf1db148a80e9f25b06fe946c697ba8fa83bc46c13515904d4ceceaeb2a4eeb`  
		Last Modified: Wed, 20 Mar 2024 22:17:12 GMT  
		Size: 2.2 MB (2152657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400f8ed9afb04b498a060de1a774c9272cec70272754126b664985cd98414623`  
		Last Modified: Tue, 09 Apr 2024 14:59:31 GMT  
		Size: 1.2 MB (1230937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ca205adef44fe63941fcd64a5ea1c792c297534b81b7c23838857081d464f6`  
		Last Modified: Tue, 09 Apr 2024 14:59:31 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b24165a664a9007bca136f51d3c60c906ddf8626c9ab9403969454d4c0c47ac`  
		Last Modified: Tue, 09 Apr 2024 14:59:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:e8a1f799f3a7047f3ea6db5f3bebbdcf84726e7a0b3b45157df167d441495d0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2283204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee48fbaae81e8e950ac399f89ee0eb0f7ad3e7da77d66ce435def816b3814ca`

```dockerfile
```

-	Layers:
	-	`sha256:bda232575879bf9ee6d85b64ea286f2469deccdb87ecc3991ba0fd95a508d8fa`  
		Last Modified: Tue, 09 Apr 2024 14:59:30 GMT  
		Size: 2.3 MB (2262266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13f17df99c3a427fb2b41aa30a6b4f13b2de20e1567da419bc3c6f2febb08832`  
		Last Modified: Tue, 09 Apr 2024 14:59:31 GMT  
		Size: 20.9 KB (20938 bytes)  
		MIME: application/vnd.in-toto+json
