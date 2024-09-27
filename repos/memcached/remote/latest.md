## `memcached:latest`

```console
$ docker pull memcached@sha256:f167f65af00f404c534036ee7a3ce236bf2b06eb5315f70bd67b08f162d87a97
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
$ docker pull memcached@sha256:e9099962b29746b61d0a44fab0bac5447e23998d397e8cfa3ecd64de0de721ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30222617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78dc3a91520bafda084a65f1d8e052a44f18a765d14af6e1ef43f9128a3912f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 07 Sep 2024 18:54:11 GMT
ADD file:91b876c600b7d3198bc98296224f6861440f56fcbd15a2188c95a8785b94061a in / 
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
	-	`sha256:75a20c44e8becd141ba586ea413a1649251437a207502d4f8ad23d208f013e60`  
		Last Modified: Fri, 27 Sep 2024 03:21:44 GMT  
		Size: 26.9 MB (26887302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c2d1e75b0f77a17bd39ee74fc9f622b50ea0f1c34fbd8f32148798bfa85fe1`  
		Last Modified: Fri, 27 Sep 2024 10:45:12 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db9bf210233a166b75b21df310e99764b1208c8784d6b54c2153f0173195fe8b`  
		Last Modified: Fri, 27 Sep 2024 10:45:13 GMT  
		Size: 2.1 MB (2095618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee20ab38e759d997ba0183d59ee42fbb27c83a90a03918408df1602263c78118`  
		Last Modified: Fri, 27 Sep 2024 10:45:13 GMT  
		Size: 1.2 MB (1238183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2cdf26e0d87752c41ce4b0a37bb91a61c692c6abce6c5810e50ae8a31a0071`  
		Last Modified: Fri, 27 Sep 2024 10:45:13 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2068734dbbf77a9f3d0dcd58450e2018ae620a00595e42a0216d2634a81b6486`  
		Last Modified: Fri, 27 Sep 2024 10:45:13 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:cf98b93adfe31c4c5b61b15adfcd9fd92be173ec284efee10db812dfb407d6d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b05b6bda0dfa4ae3fa89deca7e7020bbe5641a234afa90ea36d6d7a099e0b87e`

```dockerfile
```

-	Layers:
	-	`sha256:7fabc3f1c633df97993c20a8a5e8f8603b6b27ec87e50bf1e460195ca1422f86`  
		Last Modified: Fri, 27 Sep 2024 10:45:13 GMT  
		Size: 2.3 MB (2284123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53c997ca36a5ab51c86e92b7adc904ef72d79c0a62c2f97e9fd17365dc60cafa`  
		Last Modified: Fri, 27 Sep 2024 10:45:12 GMT  
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
$ docker pull memcached@sha256:0cf1889139cdbd7bf62351155d236d3157bab7bebbe84074d66cb5071dd222d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33904453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab2d41d5508ed29cf714736329deac3b48f604594cf619f1fe42d0553fcc8d0a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 07 Sep 2024 18:54:11 GMT
ADD file:7ad74dd13b6c84de2920c6d09de06e914d0b78ba06ae75260d6e6ff344a4b024 in / 
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
	-	`sha256:c953524ed27d53ce5e7d4e7487137789de73f4058e96b05284eefbcae1b47c26`  
		Last Modified: Fri, 27 Sep 2024 07:27:04 GMT  
		Size: 30.1 MB (30144216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c9947f348b93edc13050150d2b2a607db1f3ac7ebf1da7aaa28a4bf4b23961`  
		Last Modified: Fri, 27 Sep 2024 09:06:12 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70d2b4069291d8cddaa06534b0758187c12289c461dea5c43a0d1680bc901de4`  
		Last Modified: Fri, 27 Sep 2024 09:06:12 GMT  
		Size: 2.5 MB (2499311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:674da8931a5bb177b81dfd2c1b0b5e92f620a9792c75cc1d5a9ad4fb89762625`  
		Last Modified: Fri, 27 Sep 2024 09:06:12 GMT  
		Size: 1.3 MB (1259419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d4285b27e5232708dc5f6917cc1d0ce975ba3d8f62775bcdd1788fadf7506a8`  
		Last Modified: Fri, 27 Sep 2024 09:06:12 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e34045751b6c77e21aed60d33be3e6232b338495be8c80ba3318fa3eebbc461`  
		Last Modified: Fri, 27 Sep 2024 09:06:13 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:a0d8bf20ff5482be563ad039f6c216ff58131759e956c9121a814847ace0b6ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2298763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60f17346fa1a6efa0010590c11e64589c840f918d8d988a7c9733be9cf3c1e77`

```dockerfile
```

-	Layers:
	-	`sha256:4a2b21dd34b1f4de9c3ed85e99a971b7bf345ea55cec08431f3a0b7d10c0b1e4`  
		Last Modified: Fri, 27 Sep 2024 09:06:12 GMT  
		Size: 2.3 MB (2277790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:481523133a5f54a3483bda566fbe1af7b173240396ac9df20c6666993affdea1`  
		Last Modified: Fri, 27 Sep 2024 09:06:12 GMT  
		Size: 21.0 KB (20973 bytes)  
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
