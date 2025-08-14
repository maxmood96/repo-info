## `memcached:latest`

```console
$ docker pull memcached@sha256:c8b53d421310f274ece68507406126575bfc2af3ddc66b72709f81ede5fbe2a6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `memcached:latest` - linux; amd64

```console
$ docker pull memcached@sha256:489c2e770f5baac8e88e7b0fc7bd9ec7482c560232093860fa776480fd535059
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32204915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09da43b5484edc83f2f153e8f750eae1edfc09a59f9c3c8a0d1543ad028f7702`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebfc0a813c97c15541bf6e00db67cec64e96bf712ccfedb445eff79095d78dd6`  
		Last Modified: Wed, 13 Aug 2025 21:21:18 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d44cb640c5a78307f95a5ba37e9b3ff77e080db5144ad044331bdd27e2ac3b8`  
		Last Modified: Wed, 13 Aug 2025 21:21:32 GMT  
		Size: 136.6 KB (136560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c2449a0115fae5ca7c26d3857bdae261f4168d8334ad67cb6c3461a0910fc6`  
		Last Modified: Wed, 13 Aug 2025 21:21:36 GMT  
		Size: 2.3 MB (2293557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9bbdd035dc48ae794ba5af4721f9afdab19142a19ba004aa4b42738ef8758d8`  
		Last Modified: Wed, 13 Aug 2025 21:21:42 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc99f3761e7cd9c6f00023c8aa0d889222b7b233949d24870d0f9b7ad10f58dd`  
		Last Modified: Wed, 13 Aug 2025 21:21:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:98607b9259666dec40f29b040ae0cac2276fac6541257d7f3a4d2fa8d30e3ae6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2029528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ad42f4e39d2637475a5aaa10a446b94d8cb9b730bd194a0f995abf19ecba3e7`

```dockerfile
```

-	Layers:
	-	`sha256:249ac3e00cc732e2b029808c9c00d3520da2cdf38b1fc01081a592ea90a5e050`  
		Last Modified: Wed, 13 Aug 2025 21:34:23 GMT  
		Size: 2.0 MB (2007332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fdd95540cec834ae6e6c6bf9ad1d03f83f75af3a4d5bc52a9b7018dd212823a`  
		Last Modified: Wed, 13 Aug 2025 21:34:24 GMT  
		Size: 22.2 KB (22196 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm variant v5

```console
$ docker pull memcached@sha256:11a993750bd36cfb7d37197d06ccbf217f829c9012146de0d45d0e3494add433
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30314569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c2cfe621133fc4a453c7272eacac5ac0ae1cd214c7f7076d785ec3ed0fb6554`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:498399880872f14c562c46bd2a1ef4cfcf3c2a1453514ff0d0f6b7d89f8010dd`  
		Last Modified: Tue, 12 Aug 2025 22:02:01 GMT  
		Size: 27.9 MB (27941706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a99137a20a1adabf0ea411a3bed51f642b1fd51a7c56596ed760ece4727e8c3`  
		Last Modified: Wed, 13 Aug 2025 23:01:56 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f7528817abdc345977b6df3988bcacfd622b20f1e6b64e6c01f3c3203275806`  
		Last Modified: Wed, 13 Aug 2025 23:01:57 GMT  
		Size: 144.0 KB (144046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5147466300d5970b08521247c1dcffd9c72644b33c0c4c7a7455293fdaa7514d`  
		Last Modified: Wed, 13 Aug 2025 23:01:58 GMT  
		Size: 2.2 MB (2227304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403dfb443663282b32ef64dddd4d9ece2badd91a91669659aad2213ef1db444c`  
		Last Modified: Wed, 13 Aug 2025 23:00:39 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ac9453a3752c151d9eb3d487d5be8ee9971ce482aa48cbcbffa05e594977ac`  
		Last Modified: Wed, 13 Aug 2025 23:01:59 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:99d7cc2296b1fdf18d0156098b6c8db466fa371221860e1628d6da1f33862b48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe55e32abc4c444556bb77a6cd989bc4c29ae0720781b045162ad41710f332b0`

```dockerfile
```

-	Layers:
	-	`sha256:49bb7a93a18c7972be0483acacb6a99b49edc4bf097a764ed976c48c0516bc14`  
		Last Modified: Thu, 14 Aug 2025 00:34:25 GMT  
		Size: 2.0 MB (2010335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b1896ac27634d50430d62234a56bf5e22627fb59bbe9e2f974832c3f5823cfd`  
		Last Modified: Thu, 14 Aug 2025 00:34:26 GMT  
		Size: 22.3 KB (22343 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm variant v7

```console
$ docker pull memcached@sha256:4b9bce762cb0cd433a31cf56c571b0a5bb7789813cbb111958bf806cba8b87af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28526851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a10eddf8fe36bdc9bc58ad2f45be5555dd9f6f746d916f9ce491ee5f8239bf7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d480d07cd33d2a61cb24d871a17254661d250ae887a2db15a7e99cb67383a74e`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 26.2 MB (26207488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc714abeba0eb64ab96f4d3b22e0750d8fb5ca04c15135a1da25d7f28cb90c8`  
		Last Modified: Thu, 14 Aug 2025 03:26:02 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b548feee9753e7f47e9e09d371fbbc5da58c093655fbe6a70e9e8ce1792c6ddc`  
		Last Modified: Thu, 14 Aug 2025 03:26:02 GMT  
		Size: 135.3 KB (135298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a9fd10cb429ca884c5738921b455ecc2d83781179e716d4003166bdc8c44e27`  
		Last Modified: Thu, 14 Aug 2025 03:26:01 GMT  
		Size: 2.2 MB (2182550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59893ea711e5a2631eada91282e598b013d3173b17a0edb0fdbe97d67d122e7`  
		Last Modified: Thu, 14 Aug 2025 03:26:02 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8512db29f6abd27987969691ca0de8c6cc141db19a00f2e80bd8996e6cb5de`  
		Last Modified: Thu, 14 Aug 2025 03:26:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:f4b425f37419b579837d2d7857c8ed429c6b2356824bf7c3f83036db9125cc20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f026c9ae0860a234d056b9a6607c5d4673b4e40c52e93c31e76e3cf463fa3c45`

```dockerfile
```

-	Layers:
	-	`sha256:58eba98bd420cdad2a71753e58bb1b1a587f0039d88944045180d74e4c08996c`  
		Last Modified: Thu, 14 Aug 2025 06:34:23 GMT  
		Size: 2.0 MB (2008792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab426c3e7d709a71c837bd5c98de92c219718788268a0700d3c8305f5117b7b8`  
		Last Modified: Thu, 14 Aug 2025 06:34:24 GMT  
		Size: 22.3 KB (22342 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:78a21084b1c4e79dc2fffab373fb465acb723f351bffdc0639a504a5bdc6a2d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32566079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:717e9950cc2b302a7f75cdc9919226e0160142934f76014b1a905aa5e39c4046`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d84227403935277ab9817ff62ad9fca6d45f7c109953945d36caa72d73813d0`  
		Last Modified: Wed, 13 Aug 2025 23:02:57 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb0aae300c3cd52b99acd2ae25cb8bf507859ae7b182097672be779a7337fd4`  
		Last Modified: Wed, 13 Aug 2025 23:02:58 GMT  
		Size: 153.4 KB (153369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbd2017b19819b1012be52dad0541d85c7797897955d5d0b747b8b86f08da76e`  
		Last Modified: Wed, 13 Aug 2025 23:03:00 GMT  
		Size: 2.3 MB (2275152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad146d7e60bd2063118973d72ff4507de475a826636f2b8fc3bdf36633379d07`  
		Last Modified: Wed, 13 Aug 2025 23:02:59 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45fe42a1afd3681fa0efd222132b453c718236f571b4b56018cf362f2333cfb7`  
		Last Modified: Wed, 13 Aug 2025 23:02:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:f34a398dc1f988e0076ebc490e58021e7dc24976392ab10fb871628e11888166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98dee621777b57d248833b652d7622be9c6c901776820489ce629be6f59e5d5f`

```dockerfile
```

-	Layers:
	-	`sha256:4b5fb9727c43d6c906cc0c58b470a99299321ac1e3bcc6a9ea9ec90086d4260d`  
		Last Modified: Thu, 14 Aug 2025 00:34:33 GMT  
		Size: 2.0 MB (2007648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a88652c31f79e7599a31a3fe7d0341deeb4915c7ae0dab214e3c4768ec058300`  
		Last Modified: Thu, 14 Aug 2025 00:34:33 GMT  
		Size: 22.4 KB (22393 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; 386

```console
$ docker pull memcached@sha256:5b9ccecd7eb2ba800cc927d7dfaa5941d25387818d57d8583260ed7d5ea2ef8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33682664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c160d159b0b83b9824df1d8b4cbe201c4c67902d0171a4a03282d3e230939d9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:346d0c953bdbc38917a27a6f30726e5b46419d98ecaf4d2d8f201bc3b7025e57`  
		Last Modified: Tue, 12 Aug 2025 20:45:00 GMT  
		Size: 31.3 MB (31289378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa1f928fbfcc7da63ca647a381869549b7db17d2971110bc771c27aeed80b33c`  
		Last Modified: Wed, 13 Aug 2025 21:09:56 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49988f067cdbb2558e23451192304fe7f89c2cbe23fcf5463b9e0b80dfbd2a36`  
		Last Modified: Wed, 13 Aug 2025 21:09:56 GMT  
		Size: 147.4 KB (147419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a19f3e01a2ee783f4cf292ba84f151492df7a0170128094f4d011075d629af43`  
		Last Modified: Wed, 13 Aug 2025 21:09:56 GMT  
		Size: 2.2 MB (2244354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2288d51449876e6f7fb89b6cac2eda51fef5f03deb3722ef32bf3a9bdc2f5e17`  
		Last Modified: Wed, 13 Aug 2025 21:09:56 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3668cc13fc1544b7319b7b3307e0d74b4e82d36ca065c5a3be7d080267054267`  
		Last Modified: Wed, 13 Aug 2025 21:09:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:df8cca141522937dd5415946521e71f57731ecc574e78d3175b26ce6260dcd46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2026627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff448533f7fe52a0dc6195d7b9320b996bd2623b7c1e7a5b02f7f5cee32b92a4`

```dockerfile
```

-	Layers:
	-	`sha256:80c0a6ea529144e269d6dc30e72d370cfbc53736314c92cca55d737de9562dd6`  
		Last Modified: Wed, 13 Aug 2025 21:34:31 GMT  
		Size: 2.0 MB (2004489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32faf37cac7f889e11009fc41358994c9714a5ebc9aed8843e1fb57a3de6d243`  
		Last Modified: Wed, 13 Aug 2025 21:34:32 GMT  
		Size: 22.1 KB (22138 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; ppc64le

```console
$ docker pull memcached@sha256:dcc628faf353367b245beec24d23d1b3103986479dff33e10653c5ef2d8b54b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36182904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d113eca2d57658d5e20bd62171298229010cdbce2c33479664dcad6be5ec2acd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:52a4daa8724e9e1632306e15fe478aa26ff0ebcb7ba924cb168e9b6738c239d5`  
		Last Modified: Wed, 13 Aug 2025 01:42:36 GMT  
		Size: 33.6 MB (33594213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26c42ec1bf9e33e4a6a75b57802a57b9d166fccf4b2e5b13cef2b9742fc5025`  
		Last Modified: Thu, 14 Aug 2025 02:32:42 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a82df09860007e05001d706e92e1aa450bfd12fc72a24522ccca5edc6f43cd`  
		Last Modified: Thu, 14 Aug 2025 02:32:42 GMT  
		Size: 170.2 KB (170241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f425e49b56f20bc4209bec20b1ab8671bd728a94104369def1c947c90134052`  
		Last Modified: Thu, 14 Aug 2025 02:32:42 GMT  
		Size: 2.4 MB (2416933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b832c8b1a0256fd9b38e9fd823309571e179c77a2f44d5115f06ae282b7972f`  
		Last Modified: Thu, 14 Aug 2025 02:32:42 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da165b338847a53b7c8a0a0a08c089c86721f3997c5f507291c4737245ade82f`  
		Last Modified: Thu, 14 Aug 2025 02:32:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:d11fb93c72d4e4416799b886acc2230eefbe26e6381d65c674a1a47f310f22ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2154e1260dfec440f34afa1451b8e89c13a23e1eb451b2250766c9c88cf993a`

```dockerfile
```

-	Layers:
	-	`sha256:3c0cb7a63a69d321f183e466c5c0a934dd9a09173b6e174e2f17a9a24e241dee`  
		Last Modified: Thu, 14 Aug 2025 03:34:34 GMT  
		Size: 2.0 MB (2010933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e4dcd6c60091d8eaa78af8659654106ffc91270b3f5b4b6e166f41e295e361f`  
		Last Modified: Thu, 14 Aug 2025 03:34:35 GMT  
		Size: 22.3 KB (22269 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; s390x

```console
$ docker pull memcached@sha256:c7b8d8a8065d2a0ea3bdaaadd564986a39a88ad9d9ef599faf4f923888bb9126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32288745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6fca6b4af0e7ae24559fc296fb0ce831a94645f64b986956f57f9306df1ed22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.39
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Wed, 13 Aug 2025 00:54:11 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Wed, 13 Aug 2025 00:54:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 13 Aug 2025 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 00:54:11 GMT
USER memcache
# Wed, 13 Aug 2025 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 13 Aug 2025 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bfe4d60a27c9392ab729f16b50a763cda36622d744066c3cf029a072133f2907`  
		Last Modified: Tue, 12 Aug 2025 20:59:52 GMT  
		Size: 29.8 MB (29833057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024aba4218861d2cdfa6f7186fcca6f2f2041ce6c7210cd258e28d55a2c1fa16`  
		Last Modified: Thu, 14 Aug 2025 02:58:06 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2b32b5cc5f77750b103e7bdeb63810088dca53dae4f8b6eed4e17f219a5826`  
		Last Modified: Thu, 14 Aug 2025 02:58:05 GMT  
		Size: 140.4 KB (140388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a046ba92157d2c0b391049e3f702ebcac682b0c6ee6e651f44d940e5d9bd8cd7`  
		Last Modified: Thu, 14 Aug 2025 02:58:07 GMT  
		Size: 2.3 MB (2313787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd7d0eef9a2ce528ea647334f74bfda29496059b15274182ae0d16fb7e5f28d`  
		Last Modified: Thu, 14 Aug 2025 02:58:06 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c5230e4318cec0912586827ea533d6abfaed20ff08b3662b6cf6871a9abae1`  
		Last Modified: Thu, 14 Aug 2025 02:58:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:88badce3b30eeb4fdb00156647e4a3479b0c7cf8dddb286e0bd07105084f4e5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7704cd55751a22fc58eb4a349020abdd760508cd1b9344ccb0df28dc62d35f98`

```dockerfile
```

-	Layers:
	-	`sha256:91e3962d713f291258d33cdc619c48c657c3a72b3a6c808786e3b209389502b2`  
		Last Modified: Thu, 14 Aug 2025 03:34:39 GMT  
		Size: 2.0 MB (2008769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76baa03c0dea63878577ee4ab27db735c1db244cbefee8f9c7b5d5eb4d3887f1`  
		Last Modified: Thu, 14 Aug 2025 03:34:39 GMT  
		Size: 22.2 KB (22196 bytes)  
		MIME: application/vnd.in-toto+json
