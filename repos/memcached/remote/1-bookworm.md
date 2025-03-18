## `memcached:1-bookworm`

```console
$ docker pull memcached@sha256:399304df4e474a185a3e168b791f2f4bd48a7dc6cc567767677737f89338b9ba
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
$ docker pull memcached@sha256:534fbad5dedd43ef1e62c285bb17383f7d7148df3b84a27103a605d56d5634a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31965228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1d29ade1660e28d197e6f5dc4a21db5049281536ac4e4ac4c95f86623fec37d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 21 Feb 2025 01:54:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac5e3b14f8139051848f9d9af0688e20495c2b8de2052c7172896bc3870418d`  
		Last Modified: Mon, 17 Mar 2025 23:16:02 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5801c5a64bd50cbf68ce9be6107c458a92734f8a114a15598fff99f4d9a258ef`  
		Last Modified: Mon, 17 Mar 2025 23:16:02 GMT  
		Size: 2.5 MB (2491775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d64c549fbf6a3d7b4a7ced9dc3ce16c50117d30ae59526cc6c773616198a337`  
		Last Modified: Mon, 17 Mar 2025 23:16:02 GMT  
		Size: 1.3 MB (1267076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf639a9e652ea04149a5915c3d04eaa0f0e0b6e98801258cf108319d3ab919d5`  
		Last Modified: Mon, 17 Mar 2025 23:16:02 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abec249763a31ac5850e2bc15bcde7b0617e12ab29db383a7a908d1c9fc14788`  
		Last Modified: Mon, 17 Mar 2025 23:16:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:d978b149b104534ad0649381f978e0861acd80c662a336773efd706d2bda0c3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0274b7a19adfa374885d1dd3d16423ab1448391b1a1aa2adc2d84c5a44497a11`

```dockerfile
```

-	Layers:
	-	`sha256:3481bd0fb9a1241c5eef5a4800c6a2fab7a2a5b474909ac552050b9b93baaeed`  
		Last Modified: Mon, 17 Mar 2025 23:16:02 GMT  
		Size: 2.3 MB (2289333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b07ac55cb7cbcdc38eed9eaac0d3a49a1993fec36980781bc1ae2f1e72de548`  
		Last Modified: Mon, 17 Mar 2025 23:16:02 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:bfecdf0980a8147a4be5ade4611f37380d2c47a881d5e96514fd98fb56a53736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29078853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:618e31e9d2443e635fd12f97a07a702131c835ab0859bc393b4dfc1397a33687`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 21 Feb 2025 01:54:11 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1742169600'
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:87c352465466fcf04c9686fee29c2541af5fc39172801545bb24d9faa8cdeabb`  
		Last Modified: Mon, 17 Mar 2025 22:17:36 GMT  
		Size: 25.7 MB (25735853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582aa80e513a22785cc5ca8afc34dcaecd6b2676ee7861e0b459dfcae9754ad5`  
		Last Modified: Tue, 18 Mar 2025 03:22:47 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc17ec5309de3924838ccbf6a9a035ad50b95939b0e23b35e7fc4790fdf9b7c1`  
		Last Modified: Tue, 18 Mar 2025 03:22:47 GMT  
		Size: 2.1 MB (2096160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77cb8c560a1d2a635146f9ab01f2efad25d7ae0b36afca64aa89e7cf3989ead2`  
		Last Modified: Tue, 18 Mar 2025 03:22:47 GMT  
		Size: 1.2 MB (1245325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d2dd7b827b7afc53e47507b0ad7dd230036645c66c2a4c9e0329e9e0981818`  
		Last Modified: Tue, 18 Mar 2025 03:22:47 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49652765a7b53d90d6134927bdeb7d968fb9a049c0da7953763c4d2efb44ac8f`  
		Last Modified: Tue, 18 Mar 2025 03:22:48 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:ac209e9bd4d2662ac0e5dbdf014b088ef41ce9f7d79b0faa68d7762cd369e98b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a86b73a8cb937461b7a7135e55650a21d5233ce9694e79816cd5e8ded2a007e`

```dockerfile
```

-	Layers:
	-	`sha256:a5ed32ffa5c1ba6b5765fc1be8541b4dd8061c9ad3e5cbaf532abf6524d45cd9`  
		Last Modified: Tue, 18 Mar 2025 03:22:47 GMT  
		Size: 2.3 MB (2292871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a061abef9a5035890642e2c2fcfd4803307c02749f9fd8c477e8bd1dcdf2909`  
		Last Modified: Tue, 18 Mar 2025 03:22:47 GMT  
		Size: 21.4 KB (21368 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:9954271ace5eec932637b57888de35a851dbbf7752a48bdd07d67f8b003e4110
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31665871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae2fb642e5fcb87861c0dd769575e25f9dbb356450410b9ef195d24c93e2354`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 21 Feb 2025 01:54:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9160f941b22d431d23f3cf0e601fa05dab4af2b3231abbf96dacdd57f95047c1`  
		Last Modified: Tue, 25 Feb 2025 02:58:39 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a204596a46bb55ed0990edcc3c355653414edee37de7772249518745d7abdaae`  
		Last Modified: Tue, 25 Feb 2025 02:58:40 GMT  
		Size: 2.4 MB (2355299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ebd550cfd456b16c1a8b85d43ca91dddf6ecb641c79bc22350ce3941d2a9cc2`  
		Last Modified: Tue, 25 Feb 2025 02:58:40 GMT  
		Size: 1.3 MB (1260633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c887777f86ee0e99d46848c129a65b43ba517ddbe9805f847e558697380b808`  
		Last Modified: Tue, 25 Feb 2025 02:58:39 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f5de2678cb72c85a28df5b5ae4142388329417a34b29ce91a917d8a0c24143`  
		Last Modified: Tue, 25 Feb 2025 02:58:40 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:86f797ce37335fb0ba0f42beca6de6664d7686459a8fc84ecd69635614ad566e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2311059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a50d85826a348dbf6fd6406540492f41f12d4e2591f2a1129b502fa98896df55`

```dockerfile
```

-	Layers:
	-	`sha256:00341736c2044ea8b93f6292d7533652e88b16cdf3ca0a9810dd3f12886e2b19`  
		Last Modified: Tue, 25 Feb 2025 02:58:40 GMT  
		Size: 2.3 MB (2289640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f214bd78b815479cb8e76838f5748eea4b4cf582f85906efe25b39d41631669b`  
		Last Modified: Tue, 25 Feb 2025 02:58:39 GMT  
		Size: 21.4 KB (21419 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:5d9c38fa118b043e7de43c595d949da7618cf8a6210220178f848f8a593a572d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32958097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:571ae841e7743f045b38a5409a1f45e5ab52f7938a31e50afdb75e1d1f8c4222`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 21 Feb 2025 01:54:11 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bdeb081d427d7feac6a8c0bd36a2c34506a1aa38143fe43a5c5a8c162698a854`  
		Last Modified: Mon, 17 Mar 2025 22:17:35 GMT  
		Size: 29.2 MB (29189528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb99cf505c4debbb4f0ebd76076a82766ebbec6aa3f0fb0dcb3b6d8429cb43f4`  
		Last Modified: Mon, 17 Mar 2025 23:28:29 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:615e5d3379d093290f416dae6e474d065c605364572ad0de8275cfc22dc8aadf`  
		Last Modified: Mon, 17 Mar 2025 23:28:29 GMT  
		Size: 2.5 MB (2500704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f732c826714febb3819e3f5d2cf70878002f3707253ad0a2cb7a948db437001a`  
		Last Modified: Mon, 17 Mar 2025 23:28:29 GMT  
		Size: 1.3 MB (1266354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a2ed45420ebb786594d75dbc35d540e137e64988b69590b5aacb5203b052f61`  
		Last Modified: Mon, 17 Mar 2025 23:28:29 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bbebea79d0ed426ce6d336440942c14baea20efd194ca752026f26dfc9f39ed`  
		Last Modified: Mon, 17 Mar 2025 23:28:30 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:f18fca8bcb6d573adb080debd82b05a2fca6da0b6d3f7733f1d4e71a7052fee6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:175b038b849bd9af8a8d2cc8f76a3ec5b66a9e0320e492044ae7c1776d8f45ee`

```dockerfile
```

-	Layers:
	-	`sha256:a552254a2b6dd8a31449863e83e6367ae4ab7fc4d968c43535713eea841fea10`  
		Last Modified: Mon, 17 Mar 2025 23:28:29 GMT  
		Size: 2.3 MB (2286432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:876a02da1b8ba55beec0b657e109777a8592eb5980e6473fb6ffa732161b1ac6`  
		Last Modified: Mon, 17 Mar 2025 23:28:29 GMT  
		Size: 21.2 KB (21164 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:b4dc119bebc07bf26c7c8ecc9ee3ea9dbe5d205045a55de17cf778971fa0ac27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31699418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63573bf2053a799cc956c48d8113c82428ad27732bfc161e684fdde8ca4fc9cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 21 Feb 2025 01:54:11 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1740355200'
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1851efe37d59b19d5c7092778464657e31dbfae35874c19fb94fb95542e2fba7`  
		Last Modified: Tue, 25 Feb 2025 01:30:49 GMT  
		Size: 28.5 MB (28493681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b5380400fe8c2b902c36fe65b6621dad8bc77dd06dbc6e62d6b54b73cb86c57`  
		Last Modified: Wed, 26 Feb 2025 02:02:13 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9481bb7bf5fb57e80a641b728d11a65e92ef52cf44da4b8ae7b5fc27fee5e840`  
		Last Modified: Wed, 26 Feb 2025 02:02:14 GMT  
		Size: 1.9 MB (1943176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb878849bb4535cea7ef05376145b9455c873a3d7e75b9119e81bd328533a115`  
		Last Modified: Wed, 26 Feb 2025 02:02:14 GMT  
		Size: 1.3 MB (1261044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c44ed5b04f97478a120bc9ac3fddcc5ce29e85e26428dc06bdf422ab71114c1f`  
		Last Modified: Wed, 26 Feb 2025 02:02:13 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec0a6f4dac8c5233ab3e17f58e7f1b3aed73384bfb8ac29e5c3c1f9ff1647d6`  
		Last Modified: Wed, 26 Feb 2025 02:02:14 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:da44d8d4fab001c43ce03c6ee15c4f37ed3cd07d4d433b1044b8e93a8ad4043f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 KB (21118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04dbbe7a2deeaf469f4354f15914e7b4024361e5aaa67015dc653ae255165d57`

```dockerfile
```

-	Layers:
	-	`sha256:3f78092f8cbf0c9dc711f0fbac20302d294190465dbd8c9b4c8c8445d107b76a`  
		Last Modified: Wed, 26 Feb 2025 02:02:13 GMT  
		Size: 21.1 KB (21118 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:849e6a5204188d2ed3ea27fe724b16602e6032994c7d42de722a65e869623684
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36088886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42ed3c7b29dbf5d76fa07ae75c15d534d1479eddda154dc181a78b7cfa28b470`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 21 Feb 2025 01:54:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1742169600'
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:89104bade2bef9a11eda15952361b42943ba7a21a6bc452862cf92faeccc17cf`  
		Last Modified: Mon, 17 Mar 2025 22:20:32 GMT  
		Size: 32.0 MB (32047814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b545668ac9e2cb98070e6c0e66c12ae28f85db2525cc65cb15e33041fdfdabc1`  
		Last Modified: Tue, 18 Mar 2025 05:20:40 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2903da04dbc00e25b3147ad28f9537060dfae4cf6de100f51e8991d3384a62a`  
		Last Modified: Tue, 18 Mar 2025 05:20:41 GMT  
		Size: 2.7 MB (2708629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836c17c3d6e2c9fc5a9786491cad6b69b9bebe294b96b907681919b0f41ed9cc`  
		Last Modified: Tue, 18 Mar 2025 05:20:40 GMT  
		Size: 1.3 MB (1330932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f159be90d67a1ccedda45aa6e064640ae4929d2692c7d70610988b2d3806574d`  
		Last Modified: Tue, 18 Mar 2025 05:20:40 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba12444f32f5f5885014a55fc30dc160db1e6097ad8f98c3c387412883d7b57`  
		Last Modified: Tue, 18 Mar 2025 05:20:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:1ef6038d201bbf79536b41d2fc2b8225782e5263668d894c24199928c3de7631
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2315001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95d85dfc771127cb9d176ef202ae1e3c2e5035557cabc46f634b4724ae7af8bf`

```dockerfile
```

-	Layers:
	-	`sha256:03d8b0df13a7a76fcc1783cf5d54e338e02d8ce3c29699213f9ec154ecc5b6fa`  
		Last Modified: Tue, 18 Mar 2025 05:20:41 GMT  
		Size: 2.3 MB (2293705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:073894a91face36824f5e18c08c5e3169518161e822aab3e883e01d909c9709e`  
		Last Modified: Tue, 18 Mar 2025 05:20:40 GMT  
		Size: 21.3 KB (21296 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:04aa65a4bed54d49808f994b03bff29f2884edbd81cefb2cda76ea9b0c3bdc78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30264166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad715d063da1679a87486cdd457c6f78521303cbf67951fb4c1638529c9fa22e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 21 Feb 2025 01:54:11 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1742169600'
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_VERSION=1.6.37
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.37.tar.gz
# Fri, 21 Feb 2025 01:54:11 GMT
ENV MEMCACHED_SHA1=c85e2f5f57ca18501f22bf40f69257a890ccd79d
# Fri, 21 Feb 2025 01:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 21 Feb 2025 01:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 01:54:11 GMT
USER memcache
# Fri, 21 Feb 2025 01:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 21 Feb 2025 01:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c25b115468ab81aaa9017d4d794bc086cba904c84f73abda1eac28615cd44629`  
		Last Modified: Mon, 17 Mar 2025 22:27:10 GMT  
		Size: 26.9 MB (26861059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:068fca8050d0f79b3f0448deb56abe519d59252586faa2d7ac7e083b62e1790c`  
		Last Modified: Tue, 18 Mar 2025 04:47:57 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9049331ae8825a94e431be8b2ba532165a1044a90904d6bc1faa2e05b2cd963d`  
		Last Modified: Tue, 18 Mar 2025 04:47:57 GMT  
		Size: 2.2 MB (2156408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:523a8a59265c4ae46825a4b759e255c86750e51d6fdc0358f12056ef9f00b934`  
		Last Modified: Tue, 18 Mar 2025 04:47:57 GMT  
		Size: 1.2 MB (1245187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c584915774744c0ea4b0d908789b087545e3006c8b3cf5c0d4ba3ae5e54f8b78`  
		Last Modified: Tue, 18 Mar 2025 04:47:57 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:688742c1f76d42ad144413209e76e0e9a0fbb51ff89746a1f836b50543e29a3f`  
		Last Modified: Tue, 18 Mar 2025 04:47:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:9a3923e29bde049e87977fe00ff345d134820b8f7f7efdffb39cd350bfab1738
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9384b6b0222641cce6cc148693cc9d70d5d5c169c30deffe5200cd53111b6651`

```dockerfile
```

-	Layers:
	-	`sha256:e7d6ec36bc2f49a179561851a378baf99f36ef15bdb9e4ba7f01a9c5771cde4c`  
		Last Modified: Tue, 18 Mar 2025 04:47:57 GMT  
		Size: 2.3 MB (2289047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c76f07a393fe20004871fdb9b646a126129df3e0a1d593db6cc036496c4a6b2`  
		Last Modified: Tue, 18 Mar 2025 04:47:57 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json
