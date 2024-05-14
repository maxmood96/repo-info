<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `memcached`

-	[`memcached:1`](#memcached1)
-	[`memcached:1-alpine`](#memcached1-alpine)
-	[`memcached:1-alpine3.19`](#memcached1-alpine319)
-	[`memcached:1-bookworm`](#memcached1-bookworm)
-	[`memcached:1.6`](#memcached16)
-	[`memcached:1.6-alpine`](#memcached16-alpine)
-	[`memcached:1.6-alpine3.19`](#memcached16-alpine319)
-	[`memcached:1.6-bookworm`](#memcached16-bookworm)
-	[`memcached:1.6.27`](#memcached1627)
-	[`memcached:1.6.27-alpine`](#memcached1627-alpine)
-	[`memcached:1.6.27-alpine3.19`](#memcached1627-alpine319)
-	[`memcached:1.6.27-bookworm`](#memcached1627-bookworm)
-	[`memcached:alpine`](#memcachedalpine)
-	[`memcached:alpine3.19`](#memcachedalpine319)
-	[`memcached:bookworm`](#memcachedbookworm)
-	[`memcached:latest`](#memcachedlatest)

## `memcached:1`

```console
$ docker pull memcached@sha256:1a37ac11adba27f1f29a81b85c6c242f6513d47757f99d2cbca5308fc5a5e0f2
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
$ docker pull memcached@sha256:7e88c146c7393fbcb8c981efcbebc410fe430f7e47593f7c7b19c1864fd8a793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32897352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4274125721ccfb5bf3696e35b8620677e442c1f5885aee1323d244ea4137214`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 May 2024 09:14:35 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Mon, 06 May 2024 09:14:35 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2aa97235084d1e9d96dcd82d59f52808027df2e6bd8df2b984b207c107037d6`  
		Last Modified: Tue, 14 May 2024 02:59:09 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c3eebfc2348c666ba1f14edd94df803c126159dd54a27513273f0c9ff2090b`  
		Last Modified: Tue, 14 May 2024 02:59:10 GMT  
		Size: 2.5 MB (2488483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5520a877f09a00e2d06002be9ff44b80c1044928b980ca9709460a4727ed9da6`  
		Last Modified: Tue, 14 May 2024 02:59:10 GMT  
		Size: 1.3 MB (1256949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe67d33c4a6967ba167fd89d19b671a74e19edb04bbe7ec7d3f4550f55d4569`  
		Last Modified: Tue, 14 May 2024 02:59:10 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450e4b8762758af67b4a485fc7041c56793f6094aa4548f89489e659396a5e35`  
		Last Modified: Tue, 14 May 2024 02:59:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:d8234d3b08b2d3a9b10f5cc7d7e8eeb881e9c71181619c2345871819be563eac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac0e31e9e20cd7d2eb5081055e082080168b1caffa48f1900a5efabb1a24537b`

```dockerfile
```

-	Layers:
	-	`sha256:bccfaa47fb8f608ebb8952b834915de2a6992656e4c56e611a32e8089167dc68`  
		Last Modified: Tue, 14 May 2024 02:59:10 GMT  
		Size: 2.3 MB (2261261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c86e940f075920cebfa2e40582ec611de7bff05d54bb06038bd3c50323add52`  
		Last Modified: Tue, 14 May 2024 02:59:09 GMT  
		Size: 21.1 KB (21146 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm variant v5

```console
$ docker pull memcached@sha256:0caa5d2f391d90fc8c56ad5009add403a518055de2115d6fd31e15e14297135c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30237095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:187a7263d807afaef1f10562634f3c06a7096cabb2f319e9ac2e644318303379`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 May 2024 09:14:35 GMT
ADD file:ee9f1914c7fc370bdb089c9e2fcfa15477f7091fc5437cb780232afdf6297586 in / 
# Mon, 06 May 2024 09:14:35 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:169fcae2368e5a601c42972560f091e123648fa0e741975d1b35900c61b9ff71`  
		Last Modified: Tue, 14 May 2024 00:51:36 GMT  
		Size: 26.9 MB (26909921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac2fb1ba5d31602a2c107dc7adc208fd66c3597693d97ca3a1743f80eb34c42`  
		Last Modified: Tue, 14 May 2024 14:50:47 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b482143aab2b97abcc7fe5e07ac0d3b24ac4ee147e8465846ada4f6bc2e4690f`  
		Last Modified: Tue, 14 May 2024 14:50:47 GMT  
		Size: 2.1 MB (2089496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7be0b16f146e3e0539004d2e158b62018843cb744689765fc6cb9048b3ccba3`  
		Last Modified: Tue, 14 May 2024 14:50:48 GMT  
		Size: 1.2 MB (1236170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ca6e022ab5c893f1324b016376e333d0e3af3d4eaf27ef824a8cb1ddb4ae16`  
		Last Modified: Tue, 14 May 2024 14:50:47 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14149cf3cd0dfd764982a3a1cb86460e564857ff4081b31ce6fa220d1271dc4f`  
		Last Modified: Tue, 14 May 2024 14:50:48 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:1846968895df68a70d92115780645a44cf0dff66edba584baff89764b3e902ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2285669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f19cddf29de06aa8a4c98debec36ac562df1f72b08de9c99bb7dcf388eff13ed`

```dockerfile
```

-	Layers:
	-	`sha256:4402e51b44f21e94146beef550d2f20402f932229666cd1bec4f48401cb43742`  
		Last Modified: Tue, 14 May 2024 14:50:47 GMT  
		Size: 2.3 MB (2264549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6f1c335ae222da5a6b0848b8c0960a13c272ccb39a51c22fa05b33276a341f4`  
		Last Modified: Tue, 14 May 2024 14:50:47 GMT  
		Size: 21.1 KB (21120 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:b953ca66ecee777524a0f33f0adefbe99183367e180f4b2ed82d1e525f57d208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32780663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a9c7e97a66ca554c0cfc88de871b1c7dfad7637ffcbd6a79b5c75b3954bb583`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 May 2024 09:14:35 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Mon, 06 May 2024 09:14:35 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994933505bafbbaba95cef494f2dfb3e85f2bfde1ea5c4a6dae5a179e39e7b5c`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9488359f89f8c6691f1737ce76ce6b7520511a8246658953dae9429090e88746`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 2.3 MB (2346183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27fa925bb96d2305b22651dc4d10899309c212aef95cb13afbdeb2ba5436cb0b`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 1.3 MB (1253469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5284a06f3ca2503602cf214d936daf8aedee3d442d7aa66a5b67874c8f156685`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a475f5b1bcd9a980f0e2923bf1af87002c6468529583ce41a151599d11b2cc`  
		Last Modified: Tue, 14 May 2024 17:41:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:303a74af5e224338560198dc50e2c9cb2a7b4a46b01d39144559de1dd7788518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e79fb901bf217f30113856b6b39e296324993066435904abd2a2152baae6156`

```dockerfile
```

-	Layers:
	-	`sha256:a35747f1af90484d4a9021de5c31be89cb3117cb5f56f499d3cebe78562716cf`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 2.3 MB (2261490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c48c7060af35b31db7e804b3ce19451726c3fb6b956edad221ee58000cf04a91`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 21.0 KB (20997 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; 386

```console
$ docker pull memcached@sha256:3f542cc336b40813213949d5eb8e2da1a57005f88566c0d51c3b8624cc911916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33914242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a44cb325942314e83e433868ace554ffea1c0ef303993f238620f928b36bbcf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 May 2024 09:14:35 GMT
ADD file:252f04703c9ed01e5aa32f764c7d751f0a3b17ed9ef1961cd1972aa8453b5cf3 in / 
# Mon, 06 May 2024 09:14:35 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7075ead1c5d56dc11510b76b25c291657dc73ecf7daad5361939429487745b9a`  
		Last Modified: Tue, 14 May 2024 00:51:58 GMT  
		Size: 30.2 MB (30162638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa82d06bb0cba58ed3fae5da8ee9c6248a027c9d105f1c1e2094d1973ab2f78`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf14cdbfbd6ea1d7231b4119cb6c85336718c7ccee9bc57573aadcc210f05e2`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 2.5 MB (2492686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bed32b6d0ec7a40384a2ba4d5fa14871afba5fd572025e99ebc3c30541ee6bf`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 1.3 MB (1257406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07ba6ac3de2271f181cd17c67b57573da49f54d516ad3c852a2610d138c85b3`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a700f395f10bfe9002c02677754b0a58c0ee8ca0f1fc73477ef1b86dc734103b`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:8932028ec9d6cdd607a57df36f524623a045c35db7110aa26040859db5599b8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2279450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:303c5c842506ac0858dd708f266252ee2b586ba9dd6f506ef93e95c9d4d06402`

```dockerfile
```

-	Layers:
	-	`sha256:e55268858bc5b4c5b04534306d270b5c41b3d3dccd563cae845878933e3d7a1c`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 2.3 MB (2258359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4afdfadae6d39596deea4cc7598059a6d7cdd84a4bf4036bfd609cacb9347c22`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 21.1 KB (21091 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; mips64le

```console
$ docker pull memcached@sha256:54a6cf440988b85512b266a181d2e83efe8a6a16530029f48b2fd002efb2e251
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38171114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac4ac5a7759abeb1658c052e8e13a0cdc6e05c7af62e12528e0d65428805b7b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 24 Apr 2024 03:14:18 GMT
ADD file:a3e63beab80160854bfc2d48f69e7c70a9542cdfaf3c5b50f1d6248a998b75ae in / 
# Wed, 24 Apr 2024 03:14:22 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:af25825be002e7bdd52bf28c2fbef5bae0ba9fcef8118e5591a874e7a70b2a62`  
		Last Modified: Wed, 24 Apr 2024 03:25:20 GMT  
		Size: 29.1 MB (29144174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70b69867f90cc0cd6ccf8b72f07ee05c80179a59283d6ce971d9191eaf11afe`  
		Last Modified: Mon, 06 May 2024 23:22:55 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361f75ee595f0c436f725a5dd64b1009cb0da358d19361f68345abf27c392f03`  
		Last Modified: Mon, 06 May 2024 23:22:56 GMT  
		Size: 1.9 MB (1937740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1d3e5a5aad136d9ada8e95bd8e9f609baf923df5c9a48a8021e50206e4e93d`  
		Last Modified: Mon, 06 May 2024 23:22:56 GMT  
		Size: 7.1 MB (7087680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913b327051e93299424d31038856dead21e1781ab1e47927437d8d135ea97338`  
		Last Modified: Mon, 06 May 2024 23:22:55 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a025835eff1c0dfdae38dce98ddefd33f8609362934acbc3106f445279e8b050`  
		Last Modified: Mon, 06 May 2024 23:22:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:062ba12de9ac3ea604948fc8045fa1f18254e15045b75fd40ba397ca49ddac94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30f78c9e4c785d57060d12fdc33b3579dde0c50533361c63c38632718921c39d`

```dockerfile
```

-	Layers:
	-	`sha256:0f87aa3b54f1e190b0d04cc9d1960d4d745a6c99015f572091bc1c532c971e12`  
		Last Modified: Mon, 06 May 2024 23:22:55 GMT  
		Size: 20.9 KB (20862 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; ppc64le

```console
$ docker pull memcached@sha256:430b7d0dd4212933d73484135db4087f520991a9e0d7499435fbf2e530fd6318
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37163910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7e11c36793a0732a32959b3d851daf998f260c7310adb4bd030bc5efd62c057`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 May 2024 09:14:35 GMT
ADD file:1622c3287b5a5c8a6e0b0b0180489212aab2c9bc7b43390b17a5cc8b153e542a in / 
# Mon, 06 May 2024 09:14:35 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:11ee2a6dbc4a6a6b182097f6023f775e595488a6bcc424e9b58001659deb7fa1`  
		Last Modified: Tue, 14 May 2024 01:24:06 GMT  
		Size: 33.1 MB (33141160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7bc98b1678c7602a43450cf1b5a0b7681ae2f5fc3f2798b1efeacf4b6f816e4`  
		Last Modified: Tue, 14 May 2024 13:32:54 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592eb5f8d51b94ab989902437d4d45fa389f90d9e020376265109959475352c8`  
		Last Modified: Tue, 14 May 2024 13:32:54 GMT  
		Size: 2.7 MB (2698407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d506236222bc33a96c083a536e37019eb18cd167ad0488e486fb7efe603856`  
		Last Modified: Tue, 14 May 2024 13:32:54 GMT  
		Size: 1.3 MB (1322831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cff49951e34e6f3a9bbca8596de07eb85450e57e2a99f66b6ce6d36a5cfa049`  
		Last Modified: Tue, 14 May 2024 13:32:55 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f72d6fdca7ec069335903535d097bd12cf1f35395a355b1b4665ab7ed230d4a2`  
		Last Modified: Tue, 14 May 2024 13:32:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:c03fdeb43ec264ab9493846e0ed7373f1e0c4353bdabd3a494684f4c321b8611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2286679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:466a2eec05699dc762f3abe6e741f13a1f0fe96e2fede2cf328da8719620ac85`

```dockerfile
```

-	Layers:
	-	`sha256:cd846922ab00a7afbef577d0a4f869b45fae65daea24ae1fec41855f72bc9b61`  
		Last Modified: Tue, 14 May 2024 13:32:54 GMT  
		Size: 2.3 MB (2265632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5104c8ee9f5261628bf21f17c74ad56f6c43c8a852d215728842b3261b1b3974`  
		Last Modified: Tue, 14 May 2024 13:32:54 GMT  
		Size: 21.0 KB (21047 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; s390x

```console
$ docker pull memcached@sha256:8be2074db9458342fce6c40d6ff648ba9c8671d9210c3bd0dabdb386cdc2c639
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30902718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fb8c642e3831e983cd5e8acdee53cd1b4a2f633ffd89c297f50d80745daafa1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 May 2024 09:14:35 GMT
ADD file:55fef93bbad6701fe968a070a0c72b3a0bd3df408dd79c9a616a43dea0de11d0 in / 
# Mon, 06 May 2024 09:14:35 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d7365433874e83ccc92aa5d768989641a64e23c3247409161401a09b4895c406`  
		Last Modified: Tue, 14 May 2024 00:47:35 GMT  
		Size: 27.5 MB (27512398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f6e2c8c427b6988b152cb191a15a2716bbf2dff9f9a6eafebf06f081eebf7b5`  
		Last Modified: Tue, 14 May 2024 17:56:21 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e6d59bd3a243d0242de493c532d8d56b279f05bb1a3d7c58724ea30a716fcf`  
		Last Modified: Tue, 14 May 2024 17:56:21 GMT  
		Size: 2.2 MB (2152659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da6ae628a520dec07948d68ad410a007894a6f040c7305dd8c4628501f77d49`  
		Last Modified: Tue, 14 May 2024 17:56:21 GMT  
		Size: 1.2 MB (1236148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb27d713cf158e879ff43c810aa223cb411f904673225d1d31f1bb782c01cb2`  
		Last Modified: Tue, 14 May 2024 17:56:21 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a400d87b577ef1da8cde4dc345372dd8e53b0d2a3c0e49aa4771038101183470`  
		Last Modified: Tue, 14 May 2024 17:56:22 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:b400e46dab61c1e9270120428db66b57ee83545f05b9bf07b59489dde48c10eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0dcf8c510ed87cdfbca560a9fa5173caed7b13966e9ddbf6a1fbaf8203265d4`

```dockerfile
```

-	Layers:
	-	`sha256:c437e8e5e7b32562cd1a77d98c41ff5a5bcf8c18102d8304295fe16c0342e460`  
		Last Modified: Tue, 14 May 2024 17:56:21 GMT  
		Size: 2.3 MB (2261082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ae942851d074d6a0dd2bdcb21bd9e83ec34c7bfd585ffd21811c317eb715284`  
		Last Modified: Tue, 14 May 2024 17:56:21 GMT  
		Size: 21.0 KB (20979 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine`

```console
$ docker pull memcached@sha256:4ee2d6582442b4920f0c9de6565947a81e18abc48089804df10251eedf388d66
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

### `memcached:1-alpine` - linux; amd64

```console
$ docker pull memcached@sha256:cf854f636d506c0834dc1159ad5b472fea96028e88702014088384915a7c08dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6535198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21047320ccba2e62e0ee66c1ffa169149658e039ee012547c37ed6aa0130ad2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59605d18a5ec7e6531bd08f0238da758082d075c4fdd6a4ec8c00fd6f792425b`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8691b75405b7042ea4a853223cc80432131a0e21745f3baf9b21b00073207ace`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 104.2 KB (104211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8925d4d8379f9d71921da012b62d23d71f826e429777c701a1b0d4d56d0399ac`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 3.0 MB (3020613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86013193f6f292637e997c2518f84ab28fec9d7a494cda4090d07457058f10de`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10cfe77bbca77075d0b682e8546bca4d6d045cfbff0be0336d51b7bbe1116983`  
		Last Modified: Mon, 06 May 2024 23:08:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:d4a846cbc9f47d5db83dbb38f019064556e6af28dad33264b1f851bebbb2858b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ab3ae8df84416fe4351914e6bb061214bfad4b0cb01537aef674b02c008994`

```dockerfile
```

-	Layers:
	-	`sha256:59634fa6bbcc5be09a70b3894761425c9ea7b231a189445bce9ae40b97f09675`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 88.1 KB (88149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2fd487a2e71a464ab83cce092819d041b742e29af0ecb901bcb36ac21fc7c2c`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 19.5 KB (19475 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:8a6f18eb424270a1dca99143a613014d570cb7376c9cb7d212b72d74c569b12a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6381171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8ddcb41c8f4d78c4720e1ad02b3c978ef7af38607d717e52219f0c53ab6fb64`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859f5f148ebb49ed2dfc712d036c8e1162fd5c08307e622f420c9e722f459c15`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a85abddca9696d1381e2dbbf52914e6119f22bd22e71c1ffc49aa385ca2d79`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 120.9 KB (120900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f80774db5f2d9cd2ec4f0bf8e7256768ab2ff5b90e1a822c70e5fb0a8d0a42`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 2.9 MB (2910908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fff6ea9e3e8e56264cef5ba1ceaacc5db1aa37fb687bf4cb684629a462a4e04`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e6b3e687f63ee869e2595d746eecfc9a9a64e49c7972eea118f9af26f3a02f`  
		Last Modified: Mon, 06 May 2024 23:43:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7677dd609f55b7dac25e997d7fc4942f1b433f1084ca54e71a01175c8608fedb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cce1cbd3428e47f29034986dc018cfef4ed121b030aef195db0d03c8a65cc79d`

```dockerfile
```

-	Layers:
	-	`sha256:c80e817fe71d2bd7ff1d9709ab1ac3d7ac30315b7cfd1b528ca1c316fecabc2f`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 88.2 KB (88168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b568b0dd9cb0ef2428bd10a39e9ee3afe06fe97f6911abc8c1ae5e642b27094`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 19.3 KB (19326 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; 386

```console
$ docker pull memcached@sha256:1557e39ed6b5f943d53c54797d59f4ea27755c53c9e7004cbfb633c08757abd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6194136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d48e3a30b8d39f2e6434ff10c1130366a5bfeac640bc8ecb88f89e6e996cdc4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c853f4fd5c9ee2e18e52b4399ccc43726449928a43d040161f83d3f67f596dd`  
		Last Modified: Mon, 06 May 2024 23:08:35 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca2d91782956c7a9591fd3f9edb724367e6a2770f04a809c6088a8ea623ea7f`  
		Last Modified: Mon, 06 May 2024 23:08:36 GMT  
		Size: 109.3 KB (109328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5c07db0e07d757431d4458ea14990c3cc0b06aa9577b0e29f8db33fc51921b`  
		Last Modified: Mon, 06 May 2024 23:08:36 GMT  
		Size: 2.8 MB (2839076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21633262023f9a6ae09f480b39a8a9a7109a0201b779ccdba90e721204cb20ae`  
		Last Modified: Mon, 06 May 2024 23:08:36 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893c3463887c0e33218f5af72fe7534fe9bebd41fd26e976944bbd03c13a9d22`  
		Last Modified: Mon, 06 May 2024 23:08:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:4184448ad3b3ff9a34654847c26c9ad677ce54b07e8a96eedb429e8c509fe5e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04225924b78526836b6ef1d8f4bd3d25e994e9f858bedc4d73fbf5308500d074`

```dockerfile
```

-	Layers:
	-	`sha256:562178e7885ee7492a868cc754c309fe7cf0a52b74299dc570dc9959ecfc0c10`  
		Last Modified: Mon, 06 May 2024 23:08:36 GMT  
		Size: 88.1 KB (88104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d1f3d52b695ee750a517e356c17e9f3b6a3778f607f791f558ae9e31397df3f`  
		Last Modified: Mon, 06 May 2024 23:08:35 GMT  
		Size: 19.4 KB (19420 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:4b1fdeda480d0b679c2b9fa5a09c508dabaf7bf0bf1600d0078fcae81e004dd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6407037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf112675855fb5780056fbde79f0822c329da1cfb19ca47270289ec2ac966e77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25735f744a453fbf0af2d088f79a0fa6de45cc2699601389d42141b2de2f21d3`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a61320e5e6694b8436a4074ba6280369b9b29e2474231252683fa11606b8e6`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 123.4 KB (123401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e809f0a1acfe802b3158bb0d4d370427885e8c5ba2ce6b98549da9bbac597e`  
		Last Modified: Mon, 06 May 2024 23:39:16 GMT  
		Size: 2.9 MB (2923638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99dc3c24ef4a44c763efcf66a6e3e44d31d723683dd339c343770bd43523007`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0b13828c450ce09acf99d42e4d9e625dbc1991b6f87a5727ff595e3e62a06c`  
		Last Modified: Mon, 06 May 2024 23:39:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:d1dc50ec127cc25ab5b90bbe3fccaf4c5cda1379629dcd1760fa93b6cab32718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 KB (105629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7934a2d41084621a7a7ff3aafbea88a9edfb76ded1149d611483fb61826d661`

```dockerfile
```

-	Layers:
	-	`sha256:dedf3264102cee8df6c9d7e964dedede98ab6b3865d8df8f76e88eeb42290632`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 86.3 KB (86253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b25fbb2f936e2b3483885e59398fdcffdf62a984c55d6171eb02b6a8b6ef44d7`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 19.4 KB (19376 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:16979dbfdc08cb52efcfffcdfdff35be32426e49b90065b36155882be545d88b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6151853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cca463729a03d73b6abb17295ed77bc6a13a336b4bc01a3b1c03a176f34fa06`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a6f11688a0fb8016d54f0f889fc4e07b5c17c62112125611f7c620bc7d3f99`  
		Last Modified: Sun, 17 Mar 2024 22:11:54 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a294d63f4311d022fef15282f082670fab839cd31782b0d6e3e8c12044283a`  
		Last Modified: Sun, 17 Mar 2024 22:11:54 GMT  
		Size: 113.1 KB (113140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d6a06c9130de338c39b57baed51f1e62b01cf60bb33a109ac31927ab8c775f`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 2.8 MB (2794432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db042a56f7b2a4ea616aa34e4b563284ea5d38557c0ff85c04706fc945bc905`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e7dbc7d250abc9822b7e752e47c8b83dd404648d74f9331600b392ac836970`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:b885694442ff65cade16142bde9307eda742f797b4c4e48b95e2ecd62c262746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 KB (105504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:023ebbf730f939171a6dd74509e836130fe404e073174c8b1be5b28fd09e514e`

```dockerfile
```

-	Layers:
	-	`sha256:b18acb410267cb31ce209d09681474ba43f18c2f4af00288845c4061bd220974`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 86.2 KB (86195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48c7d2c81f6bbcf60c7bbca78ec3114f620154531205c592fe14d252cb9daf08`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 19.3 KB (19309 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine3.19`

```console
$ docker pull memcached@sha256:4ee2d6582442b4920f0c9de6565947a81e18abc48089804df10251eedf388d66
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

### `memcached:1-alpine3.19` - linux; amd64

```console
$ docker pull memcached@sha256:cf854f636d506c0834dc1159ad5b472fea96028e88702014088384915a7c08dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6535198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21047320ccba2e62e0ee66c1ffa169149658e039ee012547c37ed6aa0130ad2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59605d18a5ec7e6531bd08f0238da758082d075c4fdd6a4ec8c00fd6f792425b`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8691b75405b7042ea4a853223cc80432131a0e21745f3baf9b21b00073207ace`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 104.2 KB (104211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8925d4d8379f9d71921da012b62d23d71f826e429777c701a1b0d4d56d0399ac`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 3.0 MB (3020613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86013193f6f292637e997c2518f84ab28fec9d7a494cda4090d07457058f10de`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10cfe77bbca77075d0b682e8546bca4d6d045cfbff0be0336d51b7bbe1116983`  
		Last Modified: Mon, 06 May 2024 23:08:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:d4a846cbc9f47d5db83dbb38f019064556e6af28dad33264b1f851bebbb2858b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ab3ae8df84416fe4351914e6bb061214bfad4b0cb01537aef674b02c008994`

```dockerfile
```

-	Layers:
	-	`sha256:59634fa6bbcc5be09a70b3894761425c9ea7b231a189445bce9ae40b97f09675`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 88.1 KB (88149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2fd487a2e71a464ab83cce092819d041b742e29af0ecb901bcb36ac21fc7c2c`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 19.5 KB (19475 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:8a6f18eb424270a1dca99143a613014d570cb7376c9cb7d212b72d74c569b12a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6381171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8ddcb41c8f4d78c4720e1ad02b3c978ef7af38607d717e52219f0c53ab6fb64`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859f5f148ebb49ed2dfc712d036c8e1162fd5c08307e622f420c9e722f459c15`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a85abddca9696d1381e2dbbf52914e6119f22bd22e71c1ffc49aa385ca2d79`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 120.9 KB (120900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f80774db5f2d9cd2ec4f0bf8e7256768ab2ff5b90e1a822c70e5fb0a8d0a42`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 2.9 MB (2910908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fff6ea9e3e8e56264cef5ba1ceaacc5db1aa37fb687bf4cb684629a462a4e04`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e6b3e687f63ee869e2595d746eecfc9a9a64e49c7972eea118f9af26f3a02f`  
		Last Modified: Mon, 06 May 2024 23:43:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:7677dd609f55b7dac25e997d7fc4942f1b433f1084ca54e71a01175c8608fedb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cce1cbd3428e47f29034986dc018cfef4ed121b030aef195db0d03c8a65cc79d`

```dockerfile
```

-	Layers:
	-	`sha256:c80e817fe71d2bd7ff1d9709ab1ac3d7ac30315b7cfd1b528ca1c316fecabc2f`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 88.2 KB (88168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b568b0dd9cb0ef2428bd10a39e9ee3afe06fe97f6911abc8c1ae5e642b27094`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 19.3 KB (19326 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.19` - linux; 386

```console
$ docker pull memcached@sha256:1557e39ed6b5f943d53c54797d59f4ea27755c53c9e7004cbfb633c08757abd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6194136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d48e3a30b8d39f2e6434ff10c1130366a5bfeac640bc8ecb88f89e6e996cdc4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c853f4fd5c9ee2e18e52b4399ccc43726449928a43d040161f83d3f67f596dd`  
		Last Modified: Mon, 06 May 2024 23:08:35 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca2d91782956c7a9591fd3f9edb724367e6a2770f04a809c6088a8ea623ea7f`  
		Last Modified: Mon, 06 May 2024 23:08:36 GMT  
		Size: 109.3 KB (109328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5c07db0e07d757431d4458ea14990c3cc0b06aa9577b0e29f8db33fc51921b`  
		Last Modified: Mon, 06 May 2024 23:08:36 GMT  
		Size: 2.8 MB (2839076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21633262023f9a6ae09f480b39a8a9a7109a0201b779ccdba90e721204cb20ae`  
		Last Modified: Mon, 06 May 2024 23:08:36 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893c3463887c0e33218f5af72fe7534fe9bebd41fd26e976944bbd03c13a9d22`  
		Last Modified: Mon, 06 May 2024 23:08:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:4184448ad3b3ff9a34654847c26c9ad677ce54b07e8a96eedb429e8c509fe5e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04225924b78526836b6ef1d8f4bd3d25e994e9f858bedc4d73fbf5308500d074`

```dockerfile
```

-	Layers:
	-	`sha256:562178e7885ee7492a868cc754c309fe7cf0a52b74299dc570dc9959ecfc0c10`  
		Last Modified: Mon, 06 May 2024 23:08:36 GMT  
		Size: 88.1 KB (88104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d1f3d52b695ee750a517e356c17e9f3b6a3778f607f791f558ae9e31397df3f`  
		Last Modified: Mon, 06 May 2024 23:08:35 GMT  
		Size: 19.4 KB (19420 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.19` - linux; ppc64le

```console
$ docker pull memcached@sha256:4b1fdeda480d0b679c2b9fa5a09c508dabaf7bf0bf1600d0078fcae81e004dd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6407037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf112675855fb5780056fbde79f0822c329da1cfb19ca47270289ec2ac966e77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25735f744a453fbf0af2d088f79a0fa6de45cc2699601389d42141b2de2f21d3`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a61320e5e6694b8436a4074ba6280369b9b29e2474231252683fa11606b8e6`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 123.4 KB (123401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e809f0a1acfe802b3158bb0d4d370427885e8c5ba2ce6b98549da9bbac597e`  
		Last Modified: Mon, 06 May 2024 23:39:16 GMT  
		Size: 2.9 MB (2923638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99dc3c24ef4a44c763efcf66a6e3e44d31d723683dd339c343770bd43523007`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0b13828c450ce09acf99d42e4d9e625dbc1991b6f87a5727ff595e3e62a06c`  
		Last Modified: Mon, 06 May 2024 23:39:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:d1dc50ec127cc25ab5b90bbe3fccaf4c5cda1379629dcd1760fa93b6cab32718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 KB (105629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7934a2d41084621a7a7ff3aafbea88a9edfb76ded1149d611483fb61826d661`

```dockerfile
```

-	Layers:
	-	`sha256:dedf3264102cee8df6c9d7e964dedede98ab6b3865d8df8f76e88eeb42290632`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 86.3 KB (86253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b25fbb2f936e2b3483885e59398fdcffdf62a984c55d6171eb02b6a8b6ef44d7`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 19.4 KB (19376 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.19` - linux; s390x

```console
$ docker pull memcached@sha256:16979dbfdc08cb52efcfffcdfdff35be32426e49b90065b36155882be545d88b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6151853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cca463729a03d73b6abb17295ed77bc6a13a336b4bc01a3b1c03a176f34fa06`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a6f11688a0fb8016d54f0f889fc4e07b5c17c62112125611f7c620bc7d3f99`  
		Last Modified: Sun, 17 Mar 2024 22:11:54 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a294d63f4311d022fef15282f082670fab839cd31782b0d6e3e8c12044283a`  
		Last Modified: Sun, 17 Mar 2024 22:11:54 GMT  
		Size: 113.1 KB (113140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d6a06c9130de338c39b57baed51f1e62b01cf60bb33a109ac31927ab8c775f`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 2.8 MB (2794432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db042a56f7b2a4ea616aa34e4b563284ea5d38557c0ff85c04706fc945bc905`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e7dbc7d250abc9822b7e752e47c8b83dd404648d74f9331600b392ac836970`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:b885694442ff65cade16142bde9307eda742f797b4c4e48b95e2ecd62c262746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 KB (105504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:023ebbf730f939171a6dd74509e836130fe404e073174c8b1be5b28fd09e514e`

```dockerfile
```

-	Layers:
	-	`sha256:b18acb410267cb31ce209d09681474ba43f18c2f4af00288845c4061bd220974`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 86.2 KB (86195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48c7d2c81f6bbcf60c7bbca78ec3114f620154531205c592fe14d252cb9daf08`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 19.3 KB (19309 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-bookworm`

```console
$ docker pull memcached@sha256:1a37ac11adba27f1f29a81b85c6c242f6513d47757f99d2cbca5308fc5a5e0f2
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
$ docker pull memcached@sha256:7e88c146c7393fbcb8c981efcbebc410fe430f7e47593f7c7b19c1864fd8a793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32897352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4274125721ccfb5bf3696e35b8620677e442c1f5885aee1323d244ea4137214`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 May 2024 09:14:35 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Mon, 06 May 2024 09:14:35 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2aa97235084d1e9d96dcd82d59f52808027df2e6bd8df2b984b207c107037d6`  
		Last Modified: Tue, 14 May 2024 02:59:09 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c3eebfc2348c666ba1f14edd94df803c126159dd54a27513273f0c9ff2090b`  
		Last Modified: Tue, 14 May 2024 02:59:10 GMT  
		Size: 2.5 MB (2488483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5520a877f09a00e2d06002be9ff44b80c1044928b980ca9709460a4727ed9da6`  
		Last Modified: Tue, 14 May 2024 02:59:10 GMT  
		Size: 1.3 MB (1256949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe67d33c4a6967ba167fd89d19b671a74e19edb04bbe7ec7d3f4550f55d4569`  
		Last Modified: Tue, 14 May 2024 02:59:10 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450e4b8762758af67b4a485fc7041c56793f6094aa4548f89489e659396a5e35`  
		Last Modified: Tue, 14 May 2024 02:59:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:d8234d3b08b2d3a9b10f5cc7d7e8eeb881e9c71181619c2345871819be563eac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac0e31e9e20cd7d2eb5081055e082080168b1caffa48f1900a5efabb1a24537b`

```dockerfile
```

-	Layers:
	-	`sha256:bccfaa47fb8f608ebb8952b834915de2a6992656e4c56e611a32e8089167dc68`  
		Last Modified: Tue, 14 May 2024 02:59:10 GMT  
		Size: 2.3 MB (2261261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c86e940f075920cebfa2e40582ec611de7bff05d54bb06038bd3c50323add52`  
		Last Modified: Tue, 14 May 2024 02:59:09 GMT  
		Size: 21.1 KB (21146 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:0caa5d2f391d90fc8c56ad5009add403a518055de2115d6fd31e15e14297135c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30237095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:187a7263d807afaef1f10562634f3c06a7096cabb2f319e9ac2e644318303379`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 May 2024 09:14:35 GMT
ADD file:ee9f1914c7fc370bdb089c9e2fcfa15477f7091fc5437cb780232afdf6297586 in / 
# Mon, 06 May 2024 09:14:35 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:169fcae2368e5a601c42972560f091e123648fa0e741975d1b35900c61b9ff71`  
		Last Modified: Tue, 14 May 2024 00:51:36 GMT  
		Size: 26.9 MB (26909921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac2fb1ba5d31602a2c107dc7adc208fd66c3597693d97ca3a1743f80eb34c42`  
		Last Modified: Tue, 14 May 2024 14:50:47 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b482143aab2b97abcc7fe5e07ac0d3b24ac4ee147e8465846ada4f6bc2e4690f`  
		Last Modified: Tue, 14 May 2024 14:50:47 GMT  
		Size: 2.1 MB (2089496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7be0b16f146e3e0539004d2e158b62018843cb744689765fc6cb9048b3ccba3`  
		Last Modified: Tue, 14 May 2024 14:50:48 GMT  
		Size: 1.2 MB (1236170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ca6e022ab5c893f1324b016376e333d0e3af3d4eaf27ef824a8cb1ddb4ae16`  
		Last Modified: Tue, 14 May 2024 14:50:47 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14149cf3cd0dfd764982a3a1cb86460e564857ff4081b31ce6fa220d1271dc4f`  
		Last Modified: Tue, 14 May 2024 14:50:48 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:1846968895df68a70d92115780645a44cf0dff66edba584baff89764b3e902ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2285669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f19cddf29de06aa8a4c98debec36ac562df1f72b08de9c99bb7dcf388eff13ed`

```dockerfile
```

-	Layers:
	-	`sha256:4402e51b44f21e94146beef550d2f20402f932229666cd1bec4f48401cb43742`  
		Last Modified: Tue, 14 May 2024 14:50:47 GMT  
		Size: 2.3 MB (2264549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6f1c335ae222da5a6b0848b8c0960a13c272ccb39a51c22fa05b33276a341f4`  
		Last Modified: Tue, 14 May 2024 14:50:47 GMT  
		Size: 21.1 KB (21120 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:b953ca66ecee777524a0f33f0adefbe99183367e180f4b2ed82d1e525f57d208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32780663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a9c7e97a66ca554c0cfc88de871b1c7dfad7637ffcbd6a79b5c75b3954bb583`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 May 2024 09:14:35 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Mon, 06 May 2024 09:14:35 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994933505bafbbaba95cef494f2dfb3e85f2bfde1ea5c4a6dae5a179e39e7b5c`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9488359f89f8c6691f1737ce76ce6b7520511a8246658953dae9429090e88746`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 2.3 MB (2346183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27fa925bb96d2305b22651dc4d10899309c212aef95cb13afbdeb2ba5436cb0b`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 1.3 MB (1253469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5284a06f3ca2503602cf214d936daf8aedee3d442d7aa66a5b67874c8f156685`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a475f5b1bcd9a980f0e2923bf1af87002c6468529583ce41a151599d11b2cc`  
		Last Modified: Tue, 14 May 2024 17:41:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:303a74af5e224338560198dc50e2c9cb2a7b4a46b01d39144559de1dd7788518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e79fb901bf217f30113856b6b39e296324993066435904abd2a2152baae6156`

```dockerfile
```

-	Layers:
	-	`sha256:a35747f1af90484d4a9021de5c31be89cb3117cb5f56f499d3cebe78562716cf`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 2.3 MB (2261490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c48c7060af35b31db7e804b3ce19451726c3fb6b956edad221ee58000cf04a91`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 21.0 KB (20997 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:3f542cc336b40813213949d5eb8e2da1a57005f88566c0d51c3b8624cc911916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33914242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a44cb325942314e83e433868ace554ffea1c0ef303993f238620f928b36bbcf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 May 2024 09:14:35 GMT
ADD file:252f04703c9ed01e5aa32f764c7d751f0a3b17ed9ef1961cd1972aa8453b5cf3 in / 
# Mon, 06 May 2024 09:14:35 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7075ead1c5d56dc11510b76b25c291657dc73ecf7daad5361939429487745b9a`  
		Last Modified: Tue, 14 May 2024 00:51:58 GMT  
		Size: 30.2 MB (30162638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa82d06bb0cba58ed3fae5da8ee9c6248a027c9d105f1c1e2094d1973ab2f78`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf14cdbfbd6ea1d7231b4119cb6c85336718c7ccee9bc57573aadcc210f05e2`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 2.5 MB (2492686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bed32b6d0ec7a40384a2ba4d5fa14871afba5fd572025e99ebc3c30541ee6bf`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 1.3 MB (1257406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07ba6ac3de2271f181cd17c67b57573da49f54d516ad3c852a2610d138c85b3`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a700f395f10bfe9002c02677754b0a58c0ee8ca0f1fc73477ef1b86dc734103b`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:8932028ec9d6cdd607a57df36f524623a045c35db7110aa26040859db5599b8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2279450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:303c5c842506ac0858dd708f266252ee2b586ba9dd6f506ef93e95c9d4d06402`

```dockerfile
```

-	Layers:
	-	`sha256:e55268858bc5b4c5b04534306d270b5c41b3d3dccd563cae845878933e3d7a1c`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 2.3 MB (2258359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4afdfadae6d39596deea4cc7598059a6d7cdd84a4bf4036bfd609cacb9347c22`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 21.1 KB (21091 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:54a6cf440988b85512b266a181d2e83efe8a6a16530029f48b2fd002efb2e251
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38171114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac4ac5a7759abeb1658c052e8e13a0cdc6e05c7af62e12528e0d65428805b7b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 24 Apr 2024 03:14:18 GMT
ADD file:a3e63beab80160854bfc2d48f69e7c70a9542cdfaf3c5b50f1d6248a998b75ae in / 
# Wed, 24 Apr 2024 03:14:22 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:af25825be002e7bdd52bf28c2fbef5bae0ba9fcef8118e5591a874e7a70b2a62`  
		Last Modified: Wed, 24 Apr 2024 03:25:20 GMT  
		Size: 29.1 MB (29144174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70b69867f90cc0cd6ccf8b72f07ee05c80179a59283d6ce971d9191eaf11afe`  
		Last Modified: Mon, 06 May 2024 23:22:55 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361f75ee595f0c436f725a5dd64b1009cb0da358d19361f68345abf27c392f03`  
		Last Modified: Mon, 06 May 2024 23:22:56 GMT  
		Size: 1.9 MB (1937740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1d3e5a5aad136d9ada8e95bd8e9f609baf923df5c9a48a8021e50206e4e93d`  
		Last Modified: Mon, 06 May 2024 23:22:56 GMT  
		Size: 7.1 MB (7087680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913b327051e93299424d31038856dead21e1781ab1e47927437d8d135ea97338`  
		Last Modified: Mon, 06 May 2024 23:22:55 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a025835eff1c0dfdae38dce98ddefd33f8609362934acbc3106f445279e8b050`  
		Last Modified: Mon, 06 May 2024 23:22:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:062ba12de9ac3ea604948fc8045fa1f18254e15045b75fd40ba397ca49ddac94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30f78c9e4c785d57060d12fdc33b3579dde0c50533361c63c38632718921c39d`

```dockerfile
```

-	Layers:
	-	`sha256:0f87aa3b54f1e190b0d04cc9d1960d4d745a6c99015f572091bc1c532c971e12`  
		Last Modified: Mon, 06 May 2024 23:22:55 GMT  
		Size: 20.9 KB (20862 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:430b7d0dd4212933d73484135db4087f520991a9e0d7499435fbf2e530fd6318
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37163910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7e11c36793a0732a32959b3d851daf998f260c7310adb4bd030bc5efd62c057`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 May 2024 09:14:35 GMT
ADD file:1622c3287b5a5c8a6e0b0b0180489212aab2c9bc7b43390b17a5cc8b153e542a in / 
# Mon, 06 May 2024 09:14:35 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:11ee2a6dbc4a6a6b182097f6023f775e595488a6bcc424e9b58001659deb7fa1`  
		Last Modified: Tue, 14 May 2024 01:24:06 GMT  
		Size: 33.1 MB (33141160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7bc98b1678c7602a43450cf1b5a0b7681ae2f5fc3f2798b1efeacf4b6f816e4`  
		Last Modified: Tue, 14 May 2024 13:32:54 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592eb5f8d51b94ab989902437d4d45fa389f90d9e020376265109959475352c8`  
		Last Modified: Tue, 14 May 2024 13:32:54 GMT  
		Size: 2.7 MB (2698407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d506236222bc33a96c083a536e37019eb18cd167ad0488e486fb7efe603856`  
		Last Modified: Tue, 14 May 2024 13:32:54 GMT  
		Size: 1.3 MB (1322831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cff49951e34e6f3a9bbca8596de07eb85450e57e2a99f66b6ce6d36a5cfa049`  
		Last Modified: Tue, 14 May 2024 13:32:55 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f72d6fdca7ec069335903535d097bd12cf1f35395a355b1b4665ab7ed230d4a2`  
		Last Modified: Tue, 14 May 2024 13:32:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:c03fdeb43ec264ab9493846e0ed7373f1e0c4353bdabd3a494684f4c321b8611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2286679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:466a2eec05699dc762f3abe6e741f13a1f0fe96e2fede2cf328da8719620ac85`

```dockerfile
```

-	Layers:
	-	`sha256:cd846922ab00a7afbef577d0a4f869b45fae65daea24ae1fec41855f72bc9b61`  
		Last Modified: Tue, 14 May 2024 13:32:54 GMT  
		Size: 2.3 MB (2265632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5104c8ee9f5261628bf21f17c74ad56f6c43c8a852d215728842b3261b1b3974`  
		Last Modified: Tue, 14 May 2024 13:32:54 GMT  
		Size: 21.0 KB (21047 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:8be2074db9458342fce6c40d6ff648ba9c8671d9210c3bd0dabdb386cdc2c639
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30902718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fb8c642e3831e983cd5e8acdee53cd1b4a2f633ffd89c297f50d80745daafa1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 May 2024 09:14:35 GMT
ADD file:55fef93bbad6701fe968a070a0c72b3a0bd3df408dd79c9a616a43dea0de11d0 in / 
# Mon, 06 May 2024 09:14:35 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d7365433874e83ccc92aa5d768989641a64e23c3247409161401a09b4895c406`  
		Last Modified: Tue, 14 May 2024 00:47:35 GMT  
		Size: 27.5 MB (27512398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f6e2c8c427b6988b152cb191a15a2716bbf2dff9f9a6eafebf06f081eebf7b5`  
		Last Modified: Tue, 14 May 2024 17:56:21 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e6d59bd3a243d0242de493c532d8d56b279f05bb1a3d7c58724ea30a716fcf`  
		Last Modified: Tue, 14 May 2024 17:56:21 GMT  
		Size: 2.2 MB (2152659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da6ae628a520dec07948d68ad410a007894a6f040c7305dd8c4628501f77d49`  
		Last Modified: Tue, 14 May 2024 17:56:21 GMT  
		Size: 1.2 MB (1236148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb27d713cf158e879ff43c810aa223cb411f904673225d1d31f1bb782c01cb2`  
		Last Modified: Tue, 14 May 2024 17:56:21 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a400d87b577ef1da8cde4dc345372dd8e53b0d2a3c0e49aa4771038101183470`  
		Last Modified: Tue, 14 May 2024 17:56:22 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:b400e46dab61c1e9270120428db66b57ee83545f05b9bf07b59489dde48c10eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0dcf8c510ed87cdfbca560a9fa5173caed7b13966e9ddbf6a1fbaf8203265d4`

```dockerfile
```

-	Layers:
	-	`sha256:c437e8e5e7b32562cd1a77d98c41ff5a5bcf8c18102d8304295fe16c0342e460`  
		Last Modified: Tue, 14 May 2024 17:56:21 GMT  
		Size: 2.3 MB (2261082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ae942851d074d6a0dd2bdcb21bd9e83ec34c7bfd585ffd21811c317eb715284`  
		Last Modified: Tue, 14 May 2024 17:56:21 GMT  
		Size: 21.0 KB (20979 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6`

```console
$ docker pull memcached@sha256:1a37ac11adba27f1f29a81b85c6c242f6513d47757f99d2cbca5308fc5a5e0f2
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
$ docker pull memcached@sha256:7e88c146c7393fbcb8c981efcbebc410fe430f7e47593f7c7b19c1864fd8a793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32897352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4274125721ccfb5bf3696e35b8620677e442c1f5885aee1323d244ea4137214`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 May 2024 09:14:35 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Mon, 06 May 2024 09:14:35 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2aa97235084d1e9d96dcd82d59f52808027df2e6bd8df2b984b207c107037d6`  
		Last Modified: Tue, 14 May 2024 02:59:09 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c3eebfc2348c666ba1f14edd94df803c126159dd54a27513273f0c9ff2090b`  
		Last Modified: Tue, 14 May 2024 02:59:10 GMT  
		Size: 2.5 MB (2488483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5520a877f09a00e2d06002be9ff44b80c1044928b980ca9709460a4727ed9da6`  
		Last Modified: Tue, 14 May 2024 02:59:10 GMT  
		Size: 1.3 MB (1256949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe67d33c4a6967ba167fd89d19b671a74e19edb04bbe7ec7d3f4550f55d4569`  
		Last Modified: Tue, 14 May 2024 02:59:10 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450e4b8762758af67b4a485fc7041c56793f6094aa4548f89489e659396a5e35`  
		Last Modified: Tue, 14 May 2024 02:59:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:d8234d3b08b2d3a9b10f5cc7d7e8eeb881e9c71181619c2345871819be563eac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac0e31e9e20cd7d2eb5081055e082080168b1caffa48f1900a5efabb1a24537b`

```dockerfile
```

-	Layers:
	-	`sha256:bccfaa47fb8f608ebb8952b834915de2a6992656e4c56e611a32e8089167dc68`  
		Last Modified: Tue, 14 May 2024 02:59:10 GMT  
		Size: 2.3 MB (2261261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c86e940f075920cebfa2e40582ec611de7bff05d54bb06038bd3c50323add52`  
		Last Modified: Tue, 14 May 2024 02:59:09 GMT  
		Size: 21.1 KB (21146 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm variant v5

```console
$ docker pull memcached@sha256:0caa5d2f391d90fc8c56ad5009add403a518055de2115d6fd31e15e14297135c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30237095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:187a7263d807afaef1f10562634f3c06a7096cabb2f319e9ac2e644318303379`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 May 2024 09:14:35 GMT
ADD file:ee9f1914c7fc370bdb089c9e2fcfa15477f7091fc5437cb780232afdf6297586 in / 
# Mon, 06 May 2024 09:14:35 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:169fcae2368e5a601c42972560f091e123648fa0e741975d1b35900c61b9ff71`  
		Last Modified: Tue, 14 May 2024 00:51:36 GMT  
		Size: 26.9 MB (26909921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac2fb1ba5d31602a2c107dc7adc208fd66c3597693d97ca3a1743f80eb34c42`  
		Last Modified: Tue, 14 May 2024 14:50:47 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b482143aab2b97abcc7fe5e07ac0d3b24ac4ee147e8465846ada4f6bc2e4690f`  
		Last Modified: Tue, 14 May 2024 14:50:47 GMT  
		Size: 2.1 MB (2089496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7be0b16f146e3e0539004d2e158b62018843cb744689765fc6cb9048b3ccba3`  
		Last Modified: Tue, 14 May 2024 14:50:48 GMT  
		Size: 1.2 MB (1236170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ca6e022ab5c893f1324b016376e333d0e3af3d4eaf27ef824a8cb1ddb4ae16`  
		Last Modified: Tue, 14 May 2024 14:50:47 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14149cf3cd0dfd764982a3a1cb86460e564857ff4081b31ce6fa220d1271dc4f`  
		Last Modified: Tue, 14 May 2024 14:50:48 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:1846968895df68a70d92115780645a44cf0dff66edba584baff89764b3e902ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2285669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f19cddf29de06aa8a4c98debec36ac562df1f72b08de9c99bb7dcf388eff13ed`

```dockerfile
```

-	Layers:
	-	`sha256:4402e51b44f21e94146beef550d2f20402f932229666cd1bec4f48401cb43742`  
		Last Modified: Tue, 14 May 2024 14:50:47 GMT  
		Size: 2.3 MB (2264549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6f1c335ae222da5a6b0848b8c0960a13c272ccb39a51c22fa05b33276a341f4`  
		Last Modified: Tue, 14 May 2024 14:50:47 GMT  
		Size: 21.1 KB (21120 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:b953ca66ecee777524a0f33f0adefbe99183367e180f4b2ed82d1e525f57d208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32780663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a9c7e97a66ca554c0cfc88de871b1c7dfad7637ffcbd6a79b5c75b3954bb583`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 May 2024 09:14:35 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Mon, 06 May 2024 09:14:35 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994933505bafbbaba95cef494f2dfb3e85f2bfde1ea5c4a6dae5a179e39e7b5c`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9488359f89f8c6691f1737ce76ce6b7520511a8246658953dae9429090e88746`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 2.3 MB (2346183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27fa925bb96d2305b22651dc4d10899309c212aef95cb13afbdeb2ba5436cb0b`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 1.3 MB (1253469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5284a06f3ca2503602cf214d936daf8aedee3d442d7aa66a5b67874c8f156685`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a475f5b1bcd9a980f0e2923bf1af87002c6468529583ce41a151599d11b2cc`  
		Last Modified: Tue, 14 May 2024 17:41:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:303a74af5e224338560198dc50e2c9cb2a7b4a46b01d39144559de1dd7788518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e79fb901bf217f30113856b6b39e296324993066435904abd2a2152baae6156`

```dockerfile
```

-	Layers:
	-	`sha256:a35747f1af90484d4a9021de5c31be89cb3117cb5f56f499d3cebe78562716cf`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 2.3 MB (2261490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c48c7060af35b31db7e804b3ce19451726c3fb6b956edad221ee58000cf04a91`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 21.0 KB (20997 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; 386

```console
$ docker pull memcached@sha256:3f542cc336b40813213949d5eb8e2da1a57005f88566c0d51c3b8624cc911916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33914242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a44cb325942314e83e433868ace554ffea1c0ef303993f238620f928b36bbcf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 May 2024 09:14:35 GMT
ADD file:252f04703c9ed01e5aa32f764c7d751f0a3b17ed9ef1961cd1972aa8453b5cf3 in / 
# Mon, 06 May 2024 09:14:35 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7075ead1c5d56dc11510b76b25c291657dc73ecf7daad5361939429487745b9a`  
		Last Modified: Tue, 14 May 2024 00:51:58 GMT  
		Size: 30.2 MB (30162638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa82d06bb0cba58ed3fae5da8ee9c6248a027c9d105f1c1e2094d1973ab2f78`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf14cdbfbd6ea1d7231b4119cb6c85336718c7ccee9bc57573aadcc210f05e2`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 2.5 MB (2492686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bed32b6d0ec7a40384a2ba4d5fa14871afba5fd572025e99ebc3c30541ee6bf`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 1.3 MB (1257406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07ba6ac3de2271f181cd17c67b57573da49f54d516ad3c852a2610d138c85b3`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a700f395f10bfe9002c02677754b0a58c0ee8ca0f1fc73477ef1b86dc734103b`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:8932028ec9d6cdd607a57df36f524623a045c35db7110aa26040859db5599b8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2279450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:303c5c842506ac0858dd708f266252ee2b586ba9dd6f506ef93e95c9d4d06402`

```dockerfile
```

-	Layers:
	-	`sha256:e55268858bc5b4c5b04534306d270b5c41b3d3dccd563cae845878933e3d7a1c`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 2.3 MB (2258359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4afdfadae6d39596deea4cc7598059a6d7cdd84a4bf4036bfd609cacb9347c22`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 21.1 KB (21091 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; mips64le

```console
$ docker pull memcached@sha256:54a6cf440988b85512b266a181d2e83efe8a6a16530029f48b2fd002efb2e251
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38171114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac4ac5a7759abeb1658c052e8e13a0cdc6e05c7af62e12528e0d65428805b7b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 24 Apr 2024 03:14:18 GMT
ADD file:a3e63beab80160854bfc2d48f69e7c70a9542cdfaf3c5b50f1d6248a998b75ae in / 
# Wed, 24 Apr 2024 03:14:22 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:af25825be002e7bdd52bf28c2fbef5bae0ba9fcef8118e5591a874e7a70b2a62`  
		Last Modified: Wed, 24 Apr 2024 03:25:20 GMT  
		Size: 29.1 MB (29144174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70b69867f90cc0cd6ccf8b72f07ee05c80179a59283d6ce971d9191eaf11afe`  
		Last Modified: Mon, 06 May 2024 23:22:55 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361f75ee595f0c436f725a5dd64b1009cb0da358d19361f68345abf27c392f03`  
		Last Modified: Mon, 06 May 2024 23:22:56 GMT  
		Size: 1.9 MB (1937740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1d3e5a5aad136d9ada8e95bd8e9f609baf923df5c9a48a8021e50206e4e93d`  
		Last Modified: Mon, 06 May 2024 23:22:56 GMT  
		Size: 7.1 MB (7087680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913b327051e93299424d31038856dead21e1781ab1e47927437d8d135ea97338`  
		Last Modified: Mon, 06 May 2024 23:22:55 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a025835eff1c0dfdae38dce98ddefd33f8609362934acbc3106f445279e8b050`  
		Last Modified: Mon, 06 May 2024 23:22:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:062ba12de9ac3ea604948fc8045fa1f18254e15045b75fd40ba397ca49ddac94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30f78c9e4c785d57060d12fdc33b3579dde0c50533361c63c38632718921c39d`

```dockerfile
```

-	Layers:
	-	`sha256:0f87aa3b54f1e190b0d04cc9d1960d4d745a6c99015f572091bc1c532c971e12`  
		Last Modified: Mon, 06 May 2024 23:22:55 GMT  
		Size: 20.9 KB (20862 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; ppc64le

```console
$ docker pull memcached@sha256:430b7d0dd4212933d73484135db4087f520991a9e0d7499435fbf2e530fd6318
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37163910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7e11c36793a0732a32959b3d851daf998f260c7310adb4bd030bc5efd62c057`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 May 2024 09:14:35 GMT
ADD file:1622c3287b5a5c8a6e0b0b0180489212aab2c9bc7b43390b17a5cc8b153e542a in / 
# Mon, 06 May 2024 09:14:35 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:11ee2a6dbc4a6a6b182097f6023f775e595488a6bcc424e9b58001659deb7fa1`  
		Last Modified: Tue, 14 May 2024 01:24:06 GMT  
		Size: 33.1 MB (33141160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7bc98b1678c7602a43450cf1b5a0b7681ae2f5fc3f2798b1efeacf4b6f816e4`  
		Last Modified: Tue, 14 May 2024 13:32:54 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592eb5f8d51b94ab989902437d4d45fa389f90d9e020376265109959475352c8`  
		Last Modified: Tue, 14 May 2024 13:32:54 GMT  
		Size: 2.7 MB (2698407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d506236222bc33a96c083a536e37019eb18cd167ad0488e486fb7efe603856`  
		Last Modified: Tue, 14 May 2024 13:32:54 GMT  
		Size: 1.3 MB (1322831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cff49951e34e6f3a9bbca8596de07eb85450e57e2a99f66b6ce6d36a5cfa049`  
		Last Modified: Tue, 14 May 2024 13:32:55 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f72d6fdca7ec069335903535d097bd12cf1f35395a355b1b4665ab7ed230d4a2`  
		Last Modified: Tue, 14 May 2024 13:32:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:c03fdeb43ec264ab9493846e0ed7373f1e0c4353bdabd3a494684f4c321b8611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2286679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:466a2eec05699dc762f3abe6e741f13a1f0fe96e2fede2cf328da8719620ac85`

```dockerfile
```

-	Layers:
	-	`sha256:cd846922ab00a7afbef577d0a4f869b45fae65daea24ae1fec41855f72bc9b61`  
		Last Modified: Tue, 14 May 2024 13:32:54 GMT  
		Size: 2.3 MB (2265632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5104c8ee9f5261628bf21f17c74ad56f6c43c8a852d215728842b3261b1b3974`  
		Last Modified: Tue, 14 May 2024 13:32:54 GMT  
		Size: 21.0 KB (21047 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; s390x

```console
$ docker pull memcached@sha256:8be2074db9458342fce6c40d6ff648ba9c8671d9210c3bd0dabdb386cdc2c639
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30902718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fb8c642e3831e983cd5e8acdee53cd1b4a2f633ffd89c297f50d80745daafa1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 May 2024 09:14:35 GMT
ADD file:55fef93bbad6701fe968a070a0c72b3a0bd3df408dd79c9a616a43dea0de11d0 in / 
# Mon, 06 May 2024 09:14:35 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d7365433874e83ccc92aa5d768989641a64e23c3247409161401a09b4895c406`  
		Last Modified: Tue, 14 May 2024 00:47:35 GMT  
		Size: 27.5 MB (27512398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f6e2c8c427b6988b152cb191a15a2716bbf2dff9f9a6eafebf06f081eebf7b5`  
		Last Modified: Tue, 14 May 2024 17:56:21 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e6d59bd3a243d0242de493c532d8d56b279f05bb1a3d7c58724ea30a716fcf`  
		Last Modified: Tue, 14 May 2024 17:56:21 GMT  
		Size: 2.2 MB (2152659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da6ae628a520dec07948d68ad410a007894a6f040c7305dd8c4628501f77d49`  
		Last Modified: Tue, 14 May 2024 17:56:21 GMT  
		Size: 1.2 MB (1236148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb27d713cf158e879ff43c810aa223cb411f904673225d1d31f1bb782c01cb2`  
		Last Modified: Tue, 14 May 2024 17:56:21 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a400d87b577ef1da8cde4dc345372dd8e53b0d2a3c0e49aa4771038101183470`  
		Last Modified: Tue, 14 May 2024 17:56:22 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:b400e46dab61c1e9270120428db66b57ee83545f05b9bf07b59489dde48c10eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0dcf8c510ed87cdfbca560a9fa5173caed7b13966e9ddbf6a1fbaf8203265d4`

```dockerfile
```

-	Layers:
	-	`sha256:c437e8e5e7b32562cd1a77d98c41ff5a5bcf8c18102d8304295fe16c0342e460`  
		Last Modified: Tue, 14 May 2024 17:56:21 GMT  
		Size: 2.3 MB (2261082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ae942851d074d6a0dd2bdcb21bd9e83ec34c7bfd585ffd21811c317eb715284`  
		Last Modified: Tue, 14 May 2024 17:56:21 GMT  
		Size: 21.0 KB (20979 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine`

```console
$ docker pull memcached@sha256:4ee2d6582442b4920f0c9de6565947a81e18abc48089804df10251eedf388d66
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

### `memcached:1.6-alpine` - linux; amd64

```console
$ docker pull memcached@sha256:cf854f636d506c0834dc1159ad5b472fea96028e88702014088384915a7c08dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6535198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21047320ccba2e62e0ee66c1ffa169149658e039ee012547c37ed6aa0130ad2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59605d18a5ec7e6531bd08f0238da758082d075c4fdd6a4ec8c00fd6f792425b`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8691b75405b7042ea4a853223cc80432131a0e21745f3baf9b21b00073207ace`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 104.2 KB (104211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8925d4d8379f9d71921da012b62d23d71f826e429777c701a1b0d4d56d0399ac`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 3.0 MB (3020613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86013193f6f292637e997c2518f84ab28fec9d7a494cda4090d07457058f10de`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10cfe77bbca77075d0b682e8546bca4d6d045cfbff0be0336d51b7bbe1116983`  
		Last Modified: Mon, 06 May 2024 23:08:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:d4a846cbc9f47d5db83dbb38f019064556e6af28dad33264b1f851bebbb2858b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ab3ae8df84416fe4351914e6bb061214bfad4b0cb01537aef674b02c008994`

```dockerfile
```

-	Layers:
	-	`sha256:59634fa6bbcc5be09a70b3894761425c9ea7b231a189445bce9ae40b97f09675`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 88.1 KB (88149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2fd487a2e71a464ab83cce092819d041b742e29af0ecb901bcb36ac21fc7c2c`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 19.5 KB (19475 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:8a6f18eb424270a1dca99143a613014d570cb7376c9cb7d212b72d74c569b12a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6381171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8ddcb41c8f4d78c4720e1ad02b3c978ef7af38607d717e52219f0c53ab6fb64`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859f5f148ebb49ed2dfc712d036c8e1162fd5c08307e622f420c9e722f459c15`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a85abddca9696d1381e2dbbf52914e6119f22bd22e71c1ffc49aa385ca2d79`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 120.9 KB (120900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f80774db5f2d9cd2ec4f0bf8e7256768ab2ff5b90e1a822c70e5fb0a8d0a42`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 2.9 MB (2910908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fff6ea9e3e8e56264cef5ba1ceaacc5db1aa37fb687bf4cb684629a462a4e04`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e6b3e687f63ee869e2595d746eecfc9a9a64e49c7972eea118f9af26f3a02f`  
		Last Modified: Mon, 06 May 2024 23:43:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7677dd609f55b7dac25e997d7fc4942f1b433f1084ca54e71a01175c8608fedb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cce1cbd3428e47f29034986dc018cfef4ed121b030aef195db0d03c8a65cc79d`

```dockerfile
```

-	Layers:
	-	`sha256:c80e817fe71d2bd7ff1d9709ab1ac3d7ac30315b7cfd1b528ca1c316fecabc2f`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 88.2 KB (88168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b568b0dd9cb0ef2428bd10a39e9ee3afe06fe97f6911abc8c1ae5e642b27094`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 19.3 KB (19326 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; 386

```console
$ docker pull memcached@sha256:1557e39ed6b5f943d53c54797d59f4ea27755c53c9e7004cbfb633c08757abd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6194136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d48e3a30b8d39f2e6434ff10c1130366a5bfeac640bc8ecb88f89e6e996cdc4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c853f4fd5c9ee2e18e52b4399ccc43726449928a43d040161f83d3f67f596dd`  
		Last Modified: Mon, 06 May 2024 23:08:35 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca2d91782956c7a9591fd3f9edb724367e6a2770f04a809c6088a8ea623ea7f`  
		Last Modified: Mon, 06 May 2024 23:08:36 GMT  
		Size: 109.3 KB (109328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5c07db0e07d757431d4458ea14990c3cc0b06aa9577b0e29f8db33fc51921b`  
		Last Modified: Mon, 06 May 2024 23:08:36 GMT  
		Size: 2.8 MB (2839076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21633262023f9a6ae09f480b39a8a9a7109a0201b779ccdba90e721204cb20ae`  
		Last Modified: Mon, 06 May 2024 23:08:36 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893c3463887c0e33218f5af72fe7534fe9bebd41fd26e976944bbd03c13a9d22`  
		Last Modified: Mon, 06 May 2024 23:08:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:4184448ad3b3ff9a34654847c26c9ad677ce54b07e8a96eedb429e8c509fe5e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04225924b78526836b6ef1d8f4bd3d25e994e9f858bedc4d73fbf5308500d074`

```dockerfile
```

-	Layers:
	-	`sha256:562178e7885ee7492a868cc754c309fe7cf0a52b74299dc570dc9959ecfc0c10`  
		Last Modified: Mon, 06 May 2024 23:08:36 GMT  
		Size: 88.1 KB (88104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d1f3d52b695ee750a517e356c17e9f3b6a3778f607f791f558ae9e31397df3f`  
		Last Modified: Mon, 06 May 2024 23:08:35 GMT  
		Size: 19.4 KB (19420 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:4b1fdeda480d0b679c2b9fa5a09c508dabaf7bf0bf1600d0078fcae81e004dd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6407037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf112675855fb5780056fbde79f0822c329da1cfb19ca47270289ec2ac966e77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25735f744a453fbf0af2d088f79a0fa6de45cc2699601389d42141b2de2f21d3`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a61320e5e6694b8436a4074ba6280369b9b29e2474231252683fa11606b8e6`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 123.4 KB (123401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e809f0a1acfe802b3158bb0d4d370427885e8c5ba2ce6b98549da9bbac597e`  
		Last Modified: Mon, 06 May 2024 23:39:16 GMT  
		Size: 2.9 MB (2923638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99dc3c24ef4a44c763efcf66a6e3e44d31d723683dd339c343770bd43523007`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0b13828c450ce09acf99d42e4d9e625dbc1991b6f87a5727ff595e3e62a06c`  
		Last Modified: Mon, 06 May 2024 23:39:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:d1dc50ec127cc25ab5b90bbe3fccaf4c5cda1379629dcd1760fa93b6cab32718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 KB (105629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7934a2d41084621a7a7ff3aafbea88a9edfb76ded1149d611483fb61826d661`

```dockerfile
```

-	Layers:
	-	`sha256:dedf3264102cee8df6c9d7e964dedede98ab6b3865d8df8f76e88eeb42290632`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 86.3 KB (86253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b25fbb2f936e2b3483885e59398fdcffdf62a984c55d6171eb02b6a8b6ef44d7`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 19.4 KB (19376 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:16979dbfdc08cb52efcfffcdfdff35be32426e49b90065b36155882be545d88b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6151853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cca463729a03d73b6abb17295ed77bc6a13a336b4bc01a3b1c03a176f34fa06`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a6f11688a0fb8016d54f0f889fc4e07b5c17c62112125611f7c620bc7d3f99`  
		Last Modified: Sun, 17 Mar 2024 22:11:54 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a294d63f4311d022fef15282f082670fab839cd31782b0d6e3e8c12044283a`  
		Last Modified: Sun, 17 Mar 2024 22:11:54 GMT  
		Size: 113.1 KB (113140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d6a06c9130de338c39b57baed51f1e62b01cf60bb33a109ac31927ab8c775f`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 2.8 MB (2794432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db042a56f7b2a4ea616aa34e4b563284ea5d38557c0ff85c04706fc945bc905`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e7dbc7d250abc9822b7e752e47c8b83dd404648d74f9331600b392ac836970`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:b885694442ff65cade16142bde9307eda742f797b4c4e48b95e2ecd62c262746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 KB (105504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:023ebbf730f939171a6dd74509e836130fe404e073174c8b1be5b28fd09e514e`

```dockerfile
```

-	Layers:
	-	`sha256:b18acb410267cb31ce209d09681474ba43f18c2f4af00288845c4061bd220974`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 86.2 KB (86195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48c7d2c81f6bbcf60c7bbca78ec3114f620154531205c592fe14d252cb9daf08`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 19.3 KB (19309 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine3.19`

```console
$ docker pull memcached@sha256:4ee2d6582442b4920f0c9de6565947a81e18abc48089804df10251eedf388d66
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

### `memcached:1.6-alpine3.19` - linux; amd64

```console
$ docker pull memcached@sha256:cf854f636d506c0834dc1159ad5b472fea96028e88702014088384915a7c08dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6535198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21047320ccba2e62e0ee66c1ffa169149658e039ee012547c37ed6aa0130ad2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59605d18a5ec7e6531bd08f0238da758082d075c4fdd6a4ec8c00fd6f792425b`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8691b75405b7042ea4a853223cc80432131a0e21745f3baf9b21b00073207ace`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 104.2 KB (104211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8925d4d8379f9d71921da012b62d23d71f826e429777c701a1b0d4d56d0399ac`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 3.0 MB (3020613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86013193f6f292637e997c2518f84ab28fec9d7a494cda4090d07457058f10de`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10cfe77bbca77075d0b682e8546bca4d6d045cfbff0be0336d51b7bbe1116983`  
		Last Modified: Mon, 06 May 2024 23:08:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:d4a846cbc9f47d5db83dbb38f019064556e6af28dad33264b1f851bebbb2858b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ab3ae8df84416fe4351914e6bb061214bfad4b0cb01537aef674b02c008994`

```dockerfile
```

-	Layers:
	-	`sha256:59634fa6bbcc5be09a70b3894761425c9ea7b231a189445bce9ae40b97f09675`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 88.1 KB (88149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2fd487a2e71a464ab83cce092819d041b742e29af0ecb901bcb36ac21fc7c2c`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 19.5 KB (19475 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:8a6f18eb424270a1dca99143a613014d570cb7376c9cb7d212b72d74c569b12a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6381171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8ddcb41c8f4d78c4720e1ad02b3c978ef7af38607d717e52219f0c53ab6fb64`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859f5f148ebb49ed2dfc712d036c8e1162fd5c08307e622f420c9e722f459c15`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a85abddca9696d1381e2dbbf52914e6119f22bd22e71c1ffc49aa385ca2d79`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 120.9 KB (120900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f80774db5f2d9cd2ec4f0bf8e7256768ab2ff5b90e1a822c70e5fb0a8d0a42`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 2.9 MB (2910908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fff6ea9e3e8e56264cef5ba1ceaacc5db1aa37fb687bf4cb684629a462a4e04`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e6b3e687f63ee869e2595d746eecfc9a9a64e49c7972eea118f9af26f3a02f`  
		Last Modified: Mon, 06 May 2024 23:43:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:7677dd609f55b7dac25e997d7fc4942f1b433f1084ca54e71a01175c8608fedb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cce1cbd3428e47f29034986dc018cfef4ed121b030aef195db0d03c8a65cc79d`

```dockerfile
```

-	Layers:
	-	`sha256:c80e817fe71d2bd7ff1d9709ab1ac3d7ac30315b7cfd1b528ca1c316fecabc2f`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 88.2 KB (88168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b568b0dd9cb0ef2428bd10a39e9ee3afe06fe97f6911abc8c1ae5e642b27094`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 19.3 KB (19326 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.19` - linux; 386

```console
$ docker pull memcached@sha256:1557e39ed6b5f943d53c54797d59f4ea27755c53c9e7004cbfb633c08757abd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6194136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d48e3a30b8d39f2e6434ff10c1130366a5bfeac640bc8ecb88f89e6e996cdc4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c853f4fd5c9ee2e18e52b4399ccc43726449928a43d040161f83d3f67f596dd`  
		Last Modified: Mon, 06 May 2024 23:08:35 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca2d91782956c7a9591fd3f9edb724367e6a2770f04a809c6088a8ea623ea7f`  
		Last Modified: Mon, 06 May 2024 23:08:36 GMT  
		Size: 109.3 KB (109328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5c07db0e07d757431d4458ea14990c3cc0b06aa9577b0e29f8db33fc51921b`  
		Last Modified: Mon, 06 May 2024 23:08:36 GMT  
		Size: 2.8 MB (2839076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21633262023f9a6ae09f480b39a8a9a7109a0201b779ccdba90e721204cb20ae`  
		Last Modified: Mon, 06 May 2024 23:08:36 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893c3463887c0e33218f5af72fe7534fe9bebd41fd26e976944bbd03c13a9d22`  
		Last Modified: Mon, 06 May 2024 23:08:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:4184448ad3b3ff9a34654847c26c9ad677ce54b07e8a96eedb429e8c509fe5e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04225924b78526836b6ef1d8f4bd3d25e994e9f858bedc4d73fbf5308500d074`

```dockerfile
```

-	Layers:
	-	`sha256:562178e7885ee7492a868cc754c309fe7cf0a52b74299dc570dc9959ecfc0c10`  
		Last Modified: Mon, 06 May 2024 23:08:36 GMT  
		Size: 88.1 KB (88104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d1f3d52b695ee750a517e356c17e9f3b6a3778f607f791f558ae9e31397df3f`  
		Last Modified: Mon, 06 May 2024 23:08:35 GMT  
		Size: 19.4 KB (19420 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.19` - linux; ppc64le

```console
$ docker pull memcached@sha256:4b1fdeda480d0b679c2b9fa5a09c508dabaf7bf0bf1600d0078fcae81e004dd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6407037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf112675855fb5780056fbde79f0822c329da1cfb19ca47270289ec2ac966e77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25735f744a453fbf0af2d088f79a0fa6de45cc2699601389d42141b2de2f21d3`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a61320e5e6694b8436a4074ba6280369b9b29e2474231252683fa11606b8e6`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 123.4 KB (123401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e809f0a1acfe802b3158bb0d4d370427885e8c5ba2ce6b98549da9bbac597e`  
		Last Modified: Mon, 06 May 2024 23:39:16 GMT  
		Size: 2.9 MB (2923638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99dc3c24ef4a44c763efcf66a6e3e44d31d723683dd339c343770bd43523007`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0b13828c450ce09acf99d42e4d9e625dbc1991b6f87a5727ff595e3e62a06c`  
		Last Modified: Mon, 06 May 2024 23:39:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:d1dc50ec127cc25ab5b90bbe3fccaf4c5cda1379629dcd1760fa93b6cab32718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 KB (105629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7934a2d41084621a7a7ff3aafbea88a9edfb76ded1149d611483fb61826d661`

```dockerfile
```

-	Layers:
	-	`sha256:dedf3264102cee8df6c9d7e964dedede98ab6b3865d8df8f76e88eeb42290632`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 86.3 KB (86253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b25fbb2f936e2b3483885e59398fdcffdf62a984c55d6171eb02b6a8b6ef44d7`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 19.4 KB (19376 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.19` - linux; s390x

```console
$ docker pull memcached@sha256:16979dbfdc08cb52efcfffcdfdff35be32426e49b90065b36155882be545d88b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6151853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cca463729a03d73b6abb17295ed77bc6a13a336b4bc01a3b1c03a176f34fa06`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a6f11688a0fb8016d54f0f889fc4e07b5c17c62112125611f7c620bc7d3f99`  
		Last Modified: Sun, 17 Mar 2024 22:11:54 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a294d63f4311d022fef15282f082670fab839cd31782b0d6e3e8c12044283a`  
		Last Modified: Sun, 17 Mar 2024 22:11:54 GMT  
		Size: 113.1 KB (113140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d6a06c9130de338c39b57baed51f1e62b01cf60bb33a109ac31927ab8c775f`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 2.8 MB (2794432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db042a56f7b2a4ea616aa34e4b563284ea5d38557c0ff85c04706fc945bc905`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e7dbc7d250abc9822b7e752e47c8b83dd404648d74f9331600b392ac836970`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:b885694442ff65cade16142bde9307eda742f797b4c4e48b95e2ecd62c262746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 KB (105504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:023ebbf730f939171a6dd74509e836130fe404e073174c8b1be5b28fd09e514e`

```dockerfile
```

-	Layers:
	-	`sha256:b18acb410267cb31ce209d09681474ba43f18c2f4af00288845c4061bd220974`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 86.2 KB (86195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48c7d2c81f6bbcf60c7bbca78ec3114f620154531205c592fe14d252cb9daf08`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 19.3 KB (19309 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-bookworm`

```console
$ docker pull memcached@sha256:1a37ac11adba27f1f29a81b85c6c242f6513d47757f99d2cbca5308fc5a5e0f2
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
$ docker pull memcached@sha256:7e88c146c7393fbcb8c981efcbebc410fe430f7e47593f7c7b19c1864fd8a793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32897352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4274125721ccfb5bf3696e35b8620677e442c1f5885aee1323d244ea4137214`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 May 2024 09:14:35 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Mon, 06 May 2024 09:14:35 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2aa97235084d1e9d96dcd82d59f52808027df2e6bd8df2b984b207c107037d6`  
		Last Modified: Tue, 14 May 2024 02:59:09 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c3eebfc2348c666ba1f14edd94df803c126159dd54a27513273f0c9ff2090b`  
		Last Modified: Tue, 14 May 2024 02:59:10 GMT  
		Size: 2.5 MB (2488483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5520a877f09a00e2d06002be9ff44b80c1044928b980ca9709460a4727ed9da6`  
		Last Modified: Tue, 14 May 2024 02:59:10 GMT  
		Size: 1.3 MB (1256949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe67d33c4a6967ba167fd89d19b671a74e19edb04bbe7ec7d3f4550f55d4569`  
		Last Modified: Tue, 14 May 2024 02:59:10 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450e4b8762758af67b4a485fc7041c56793f6094aa4548f89489e659396a5e35`  
		Last Modified: Tue, 14 May 2024 02:59:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:d8234d3b08b2d3a9b10f5cc7d7e8eeb881e9c71181619c2345871819be563eac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac0e31e9e20cd7d2eb5081055e082080168b1caffa48f1900a5efabb1a24537b`

```dockerfile
```

-	Layers:
	-	`sha256:bccfaa47fb8f608ebb8952b834915de2a6992656e4c56e611a32e8089167dc68`  
		Last Modified: Tue, 14 May 2024 02:59:10 GMT  
		Size: 2.3 MB (2261261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c86e940f075920cebfa2e40582ec611de7bff05d54bb06038bd3c50323add52`  
		Last Modified: Tue, 14 May 2024 02:59:09 GMT  
		Size: 21.1 KB (21146 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:0caa5d2f391d90fc8c56ad5009add403a518055de2115d6fd31e15e14297135c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30237095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:187a7263d807afaef1f10562634f3c06a7096cabb2f319e9ac2e644318303379`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 May 2024 09:14:35 GMT
ADD file:ee9f1914c7fc370bdb089c9e2fcfa15477f7091fc5437cb780232afdf6297586 in / 
# Mon, 06 May 2024 09:14:35 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:169fcae2368e5a601c42972560f091e123648fa0e741975d1b35900c61b9ff71`  
		Last Modified: Tue, 14 May 2024 00:51:36 GMT  
		Size: 26.9 MB (26909921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac2fb1ba5d31602a2c107dc7adc208fd66c3597693d97ca3a1743f80eb34c42`  
		Last Modified: Tue, 14 May 2024 14:50:47 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b482143aab2b97abcc7fe5e07ac0d3b24ac4ee147e8465846ada4f6bc2e4690f`  
		Last Modified: Tue, 14 May 2024 14:50:47 GMT  
		Size: 2.1 MB (2089496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7be0b16f146e3e0539004d2e158b62018843cb744689765fc6cb9048b3ccba3`  
		Last Modified: Tue, 14 May 2024 14:50:48 GMT  
		Size: 1.2 MB (1236170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ca6e022ab5c893f1324b016376e333d0e3af3d4eaf27ef824a8cb1ddb4ae16`  
		Last Modified: Tue, 14 May 2024 14:50:47 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14149cf3cd0dfd764982a3a1cb86460e564857ff4081b31ce6fa220d1271dc4f`  
		Last Modified: Tue, 14 May 2024 14:50:48 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:1846968895df68a70d92115780645a44cf0dff66edba584baff89764b3e902ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2285669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f19cddf29de06aa8a4c98debec36ac562df1f72b08de9c99bb7dcf388eff13ed`

```dockerfile
```

-	Layers:
	-	`sha256:4402e51b44f21e94146beef550d2f20402f932229666cd1bec4f48401cb43742`  
		Last Modified: Tue, 14 May 2024 14:50:47 GMT  
		Size: 2.3 MB (2264549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6f1c335ae222da5a6b0848b8c0960a13c272ccb39a51c22fa05b33276a341f4`  
		Last Modified: Tue, 14 May 2024 14:50:47 GMT  
		Size: 21.1 KB (21120 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:b953ca66ecee777524a0f33f0adefbe99183367e180f4b2ed82d1e525f57d208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32780663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a9c7e97a66ca554c0cfc88de871b1c7dfad7637ffcbd6a79b5c75b3954bb583`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 May 2024 09:14:35 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Mon, 06 May 2024 09:14:35 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994933505bafbbaba95cef494f2dfb3e85f2bfde1ea5c4a6dae5a179e39e7b5c`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9488359f89f8c6691f1737ce76ce6b7520511a8246658953dae9429090e88746`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 2.3 MB (2346183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27fa925bb96d2305b22651dc4d10899309c212aef95cb13afbdeb2ba5436cb0b`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 1.3 MB (1253469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5284a06f3ca2503602cf214d936daf8aedee3d442d7aa66a5b67874c8f156685`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a475f5b1bcd9a980f0e2923bf1af87002c6468529583ce41a151599d11b2cc`  
		Last Modified: Tue, 14 May 2024 17:41:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:303a74af5e224338560198dc50e2c9cb2a7b4a46b01d39144559de1dd7788518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e79fb901bf217f30113856b6b39e296324993066435904abd2a2152baae6156`

```dockerfile
```

-	Layers:
	-	`sha256:a35747f1af90484d4a9021de5c31be89cb3117cb5f56f499d3cebe78562716cf`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 2.3 MB (2261490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c48c7060af35b31db7e804b3ce19451726c3fb6b956edad221ee58000cf04a91`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 21.0 KB (20997 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:3f542cc336b40813213949d5eb8e2da1a57005f88566c0d51c3b8624cc911916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33914242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a44cb325942314e83e433868ace554ffea1c0ef303993f238620f928b36bbcf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 May 2024 09:14:35 GMT
ADD file:252f04703c9ed01e5aa32f764c7d751f0a3b17ed9ef1961cd1972aa8453b5cf3 in / 
# Mon, 06 May 2024 09:14:35 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7075ead1c5d56dc11510b76b25c291657dc73ecf7daad5361939429487745b9a`  
		Last Modified: Tue, 14 May 2024 00:51:58 GMT  
		Size: 30.2 MB (30162638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa82d06bb0cba58ed3fae5da8ee9c6248a027c9d105f1c1e2094d1973ab2f78`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf14cdbfbd6ea1d7231b4119cb6c85336718c7ccee9bc57573aadcc210f05e2`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 2.5 MB (2492686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bed32b6d0ec7a40384a2ba4d5fa14871afba5fd572025e99ebc3c30541ee6bf`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 1.3 MB (1257406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07ba6ac3de2271f181cd17c67b57573da49f54d516ad3c852a2610d138c85b3`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a700f395f10bfe9002c02677754b0a58c0ee8ca0f1fc73477ef1b86dc734103b`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:8932028ec9d6cdd607a57df36f524623a045c35db7110aa26040859db5599b8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2279450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:303c5c842506ac0858dd708f266252ee2b586ba9dd6f506ef93e95c9d4d06402`

```dockerfile
```

-	Layers:
	-	`sha256:e55268858bc5b4c5b04534306d270b5c41b3d3dccd563cae845878933e3d7a1c`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 2.3 MB (2258359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4afdfadae6d39596deea4cc7598059a6d7cdd84a4bf4036bfd609cacb9347c22`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 21.1 KB (21091 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:54a6cf440988b85512b266a181d2e83efe8a6a16530029f48b2fd002efb2e251
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38171114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac4ac5a7759abeb1658c052e8e13a0cdc6e05c7af62e12528e0d65428805b7b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 24 Apr 2024 03:14:18 GMT
ADD file:a3e63beab80160854bfc2d48f69e7c70a9542cdfaf3c5b50f1d6248a998b75ae in / 
# Wed, 24 Apr 2024 03:14:22 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:af25825be002e7bdd52bf28c2fbef5bae0ba9fcef8118e5591a874e7a70b2a62`  
		Last Modified: Wed, 24 Apr 2024 03:25:20 GMT  
		Size: 29.1 MB (29144174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70b69867f90cc0cd6ccf8b72f07ee05c80179a59283d6ce971d9191eaf11afe`  
		Last Modified: Mon, 06 May 2024 23:22:55 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361f75ee595f0c436f725a5dd64b1009cb0da358d19361f68345abf27c392f03`  
		Last Modified: Mon, 06 May 2024 23:22:56 GMT  
		Size: 1.9 MB (1937740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1d3e5a5aad136d9ada8e95bd8e9f609baf923df5c9a48a8021e50206e4e93d`  
		Last Modified: Mon, 06 May 2024 23:22:56 GMT  
		Size: 7.1 MB (7087680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913b327051e93299424d31038856dead21e1781ab1e47927437d8d135ea97338`  
		Last Modified: Mon, 06 May 2024 23:22:55 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a025835eff1c0dfdae38dce98ddefd33f8609362934acbc3106f445279e8b050`  
		Last Modified: Mon, 06 May 2024 23:22:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:062ba12de9ac3ea604948fc8045fa1f18254e15045b75fd40ba397ca49ddac94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30f78c9e4c785d57060d12fdc33b3579dde0c50533361c63c38632718921c39d`

```dockerfile
```

-	Layers:
	-	`sha256:0f87aa3b54f1e190b0d04cc9d1960d4d745a6c99015f572091bc1c532c971e12`  
		Last Modified: Mon, 06 May 2024 23:22:55 GMT  
		Size: 20.9 KB (20862 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:430b7d0dd4212933d73484135db4087f520991a9e0d7499435fbf2e530fd6318
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37163910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7e11c36793a0732a32959b3d851daf998f260c7310adb4bd030bc5efd62c057`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 May 2024 09:14:35 GMT
ADD file:1622c3287b5a5c8a6e0b0b0180489212aab2c9bc7b43390b17a5cc8b153e542a in / 
# Mon, 06 May 2024 09:14:35 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:11ee2a6dbc4a6a6b182097f6023f775e595488a6bcc424e9b58001659deb7fa1`  
		Last Modified: Tue, 14 May 2024 01:24:06 GMT  
		Size: 33.1 MB (33141160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7bc98b1678c7602a43450cf1b5a0b7681ae2f5fc3f2798b1efeacf4b6f816e4`  
		Last Modified: Tue, 14 May 2024 13:32:54 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592eb5f8d51b94ab989902437d4d45fa389f90d9e020376265109959475352c8`  
		Last Modified: Tue, 14 May 2024 13:32:54 GMT  
		Size: 2.7 MB (2698407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d506236222bc33a96c083a536e37019eb18cd167ad0488e486fb7efe603856`  
		Last Modified: Tue, 14 May 2024 13:32:54 GMT  
		Size: 1.3 MB (1322831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cff49951e34e6f3a9bbca8596de07eb85450e57e2a99f66b6ce6d36a5cfa049`  
		Last Modified: Tue, 14 May 2024 13:32:55 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f72d6fdca7ec069335903535d097bd12cf1f35395a355b1b4665ab7ed230d4a2`  
		Last Modified: Tue, 14 May 2024 13:32:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:c03fdeb43ec264ab9493846e0ed7373f1e0c4353bdabd3a494684f4c321b8611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2286679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:466a2eec05699dc762f3abe6e741f13a1f0fe96e2fede2cf328da8719620ac85`

```dockerfile
```

-	Layers:
	-	`sha256:cd846922ab00a7afbef577d0a4f869b45fae65daea24ae1fec41855f72bc9b61`  
		Last Modified: Tue, 14 May 2024 13:32:54 GMT  
		Size: 2.3 MB (2265632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5104c8ee9f5261628bf21f17c74ad56f6c43c8a852d215728842b3261b1b3974`  
		Last Modified: Tue, 14 May 2024 13:32:54 GMT  
		Size: 21.0 KB (21047 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:8be2074db9458342fce6c40d6ff648ba9c8671d9210c3bd0dabdb386cdc2c639
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30902718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fb8c642e3831e983cd5e8acdee53cd1b4a2f633ffd89c297f50d80745daafa1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 May 2024 09:14:35 GMT
ADD file:55fef93bbad6701fe968a070a0c72b3a0bd3df408dd79c9a616a43dea0de11d0 in / 
# Mon, 06 May 2024 09:14:35 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d7365433874e83ccc92aa5d768989641a64e23c3247409161401a09b4895c406`  
		Last Modified: Tue, 14 May 2024 00:47:35 GMT  
		Size: 27.5 MB (27512398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f6e2c8c427b6988b152cb191a15a2716bbf2dff9f9a6eafebf06f081eebf7b5`  
		Last Modified: Tue, 14 May 2024 17:56:21 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e6d59bd3a243d0242de493c532d8d56b279f05bb1a3d7c58724ea30a716fcf`  
		Last Modified: Tue, 14 May 2024 17:56:21 GMT  
		Size: 2.2 MB (2152659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da6ae628a520dec07948d68ad410a007894a6f040c7305dd8c4628501f77d49`  
		Last Modified: Tue, 14 May 2024 17:56:21 GMT  
		Size: 1.2 MB (1236148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb27d713cf158e879ff43c810aa223cb411f904673225d1d31f1bb782c01cb2`  
		Last Modified: Tue, 14 May 2024 17:56:21 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a400d87b577ef1da8cde4dc345372dd8e53b0d2a3c0e49aa4771038101183470`  
		Last Modified: Tue, 14 May 2024 17:56:22 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:b400e46dab61c1e9270120428db66b57ee83545f05b9bf07b59489dde48c10eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0dcf8c510ed87cdfbca560a9fa5173caed7b13966e9ddbf6a1fbaf8203265d4`

```dockerfile
```

-	Layers:
	-	`sha256:c437e8e5e7b32562cd1a77d98c41ff5a5bcf8c18102d8304295fe16c0342e460`  
		Last Modified: Tue, 14 May 2024 17:56:21 GMT  
		Size: 2.3 MB (2261082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ae942851d074d6a0dd2bdcb21bd9e83ec34c7bfd585ffd21811c317eb715284`  
		Last Modified: Tue, 14 May 2024 17:56:21 GMT  
		Size: 21.0 KB (20979 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.27`

```console
$ docker pull memcached@sha256:1a37ac11adba27f1f29a81b85c6c242f6513d47757f99d2cbca5308fc5a5e0f2
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

### `memcached:1.6.27` - linux; amd64

```console
$ docker pull memcached@sha256:7e88c146c7393fbcb8c981efcbebc410fe430f7e47593f7c7b19c1864fd8a793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32897352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4274125721ccfb5bf3696e35b8620677e442c1f5885aee1323d244ea4137214`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 May 2024 09:14:35 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Mon, 06 May 2024 09:14:35 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2aa97235084d1e9d96dcd82d59f52808027df2e6bd8df2b984b207c107037d6`  
		Last Modified: Tue, 14 May 2024 02:59:09 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c3eebfc2348c666ba1f14edd94df803c126159dd54a27513273f0c9ff2090b`  
		Last Modified: Tue, 14 May 2024 02:59:10 GMT  
		Size: 2.5 MB (2488483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5520a877f09a00e2d06002be9ff44b80c1044928b980ca9709460a4727ed9da6`  
		Last Modified: Tue, 14 May 2024 02:59:10 GMT  
		Size: 1.3 MB (1256949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe67d33c4a6967ba167fd89d19b671a74e19edb04bbe7ec7d3f4550f55d4569`  
		Last Modified: Tue, 14 May 2024 02:59:10 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450e4b8762758af67b4a485fc7041c56793f6094aa4548f89489e659396a5e35`  
		Last Modified: Tue, 14 May 2024 02:59:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.27` - unknown; unknown

```console
$ docker pull memcached@sha256:d8234d3b08b2d3a9b10f5cc7d7e8eeb881e9c71181619c2345871819be563eac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac0e31e9e20cd7d2eb5081055e082080168b1caffa48f1900a5efabb1a24537b`

```dockerfile
```

-	Layers:
	-	`sha256:bccfaa47fb8f608ebb8952b834915de2a6992656e4c56e611a32e8089167dc68`  
		Last Modified: Tue, 14 May 2024 02:59:10 GMT  
		Size: 2.3 MB (2261261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c86e940f075920cebfa2e40582ec611de7bff05d54bb06038bd3c50323add52`  
		Last Modified: Tue, 14 May 2024 02:59:09 GMT  
		Size: 21.1 KB (21146 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.27` - linux; arm variant v5

```console
$ docker pull memcached@sha256:0caa5d2f391d90fc8c56ad5009add403a518055de2115d6fd31e15e14297135c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30237095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:187a7263d807afaef1f10562634f3c06a7096cabb2f319e9ac2e644318303379`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 May 2024 09:14:35 GMT
ADD file:ee9f1914c7fc370bdb089c9e2fcfa15477f7091fc5437cb780232afdf6297586 in / 
# Mon, 06 May 2024 09:14:35 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:169fcae2368e5a601c42972560f091e123648fa0e741975d1b35900c61b9ff71`  
		Last Modified: Tue, 14 May 2024 00:51:36 GMT  
		Size: 26.9 MB (26909921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac2fb1ba5d31602a2c107dc7adc208fd66c3597693d97ca3a1743f80eb34c42`  
		Last Modified: Tue, 14 May 2024 14:50:47 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b482143aab2b97abcc7fe5e07ac0d3b24ac4ee147e8465846ada4f6bc2e4690f`  
		Last Modified: Tue, 14 May 2024 14:50:47 GMT  
		Size: 2.1 MB (2089496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7be0b16f146e3e0539004d2e158b62018843cb744689765fc6cb9048b3ccba3`  
		Last Modified: Tue, 14 May 2024 14:50:48 GMT  
		Size: 1.2 MB (1236170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ca6e022ab5c893f1324b016376e333d0e3af3d4eaf27ef824a8cb1ddb4ae16`  
		Last Modified: Tue, 14 May 2024 14:50:47 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14149cf3cd0dfd764982a3a1cb86460e564857ff4081b31ce6fa220d1271dc4f`  
		Last Modified: Tue, 14 May 2024 14:50:48 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.27` - unknown; unknown

```console
$ docker pull memcached@sha256:1846968895df68a70d92115780645a44cf0dff66edba584baff89764b3e902ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2285669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f19cddf29de06aa8a4c98debec36ac562df1f72b08de9c99bb7dcf388eff13ed`

```dockerfile
```

-	Layers:
	-	`sha256:4402e51b44f21e94146beef550d2f20402f932229666cd1bec4f48401cb43742`  
		Last Modified: Tue, 14 May 2024 14:50:47 GMT  
		Size: 2.3 MB (2264549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6f1c335ae222da5a6b0848b8c0960a13c272ccb39a51c22fa05b33276a341f4`  
		Last Modified: Tue, 14 May 2024 14:50:47 GMT  
		Size: 21.1 KB (21120 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.27` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:b953ca66ecee777524a0f33f0adefbe99183367e180f4b2ed82d1e525f57d208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32780663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a9c7e97a66ca554c0cfc88de871b1c7dfad7637ffcbd6a79b5c75b3954bb583`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 May 2024 09:14:35 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Mon, 06 May 2024 09:14:35 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994933505bafbbaba95cef494f2dfb3e85f2bfde1ea5c4a6dae5a179e39e7b5c`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9488359f89f8c6691f1737ce76ce6b7520511a8246658953dae9429090e88746`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 2.3 MB (2346183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27fa925bb96d2305b22651dc4d10899309c212aef95cb13afbdeb2ba5436cb0b`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 1.3 MB (1253469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5284a06f3ca2503602cf214d936daf8aedee3d442d7aa66a5b67874c8f156685`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a475f5b1bcd9a980f0e2923bf1af87002c6468529583ce41a151599d11b2cc`  
		Last Modified: Tue, 14 May 2024 17:41:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.27` - unknown; unknown

```console
$ docker pull memcached@sha256:303a74af5e224338560198dc50e2c9cb2a7b4a46b01d39144559de1dd7788518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e79fb901bf217f30113856b6b39e296324993066435904abd2a2152baae6156`

```dockerfile
```

-	Layers:
	-	`sha256:a35747f1af90484d4a9021de5c31be89cb3117cb5f56f499d3cebe78562716cf`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 2.3 MB (2261490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c48c7060af35b31db7e804b3ce19451726c3fb6b956edad221ee58000cf04a91`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 21.0 KB (20997 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.27` - linux; 386

```console
$ docker pull memcached@sha256:3f542cc336b40813213949d5eb8e2da1a57005f88566c0d51c3b8624cc911916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33914242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a44cb325942314e83e433868ace554ffea1c0ef303993f238620f928b36bbcf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 May 2024 09:14:35 GMT
ADD file:252f04703c9ed01e5aa32f764c7d751f0a3b17ed9ef1961cd1972aa8453b5cf3 in / 
# Mon, 06 May 2024 09:14:35 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7075ead1c5d56dc11510b76b25c291657dc73ecf7daad5361939429487745b9a`  
		Last Modified: Tue, 14 May 2024 00:51:58 GMT  
		Size: 30.2 MB (30162638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa82d06bb0cba58ed3fae5da8ee9c6248a027c9d105f1c1e2094d1973ab2f78`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf14cdbfbd6ea1d7231b4119cb6c85336718c7ccee9bc57573aadcc210f05e2`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 2.5 MB (2492686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bed32b6d0ec7a40384a2ba4d5fa14871afba5fd572025e99ebc3c30541ee6bf`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 1.3 MB (1257406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07ba6ac3de2271f181cd17c67b57573da49f54d516ad3c852a2610d138c85b3`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a700f395f10bfe9002c02677754b0a58c0ee8ca0f1fc73477ef1b86dc734103b`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.27` - unknown; unknown

```console
$ docker pull memcached@sha256:8932028ec9d6cdd607a57df36f524623a045c35db7110aa26040859db5599b8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2279450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:303c5c842506ac0858dd708f266252ee2b586ba9dd6f506ef93e95c9d4d06402`

```dockerfile
```

-	Layers:
	-	`sha256:e55268858bc5b4c5b04534306d270b5c41b3d3dccd563cae845878933e3d7a1c`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 2.3 MB (2258359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4afdfadae6d39596deea4cc7598059a6d7cdd84a4bf4036bfd609cacb9347c22`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 21.1 KB (21091 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.27` - linux; mips64le

```console
$ docker pull memcached@sha256:54a6cf440988b85512b266a181d2e83efe8a6a16530029f48b2fd002efb2e251
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38171114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac4ac5a7759abeb1658c052e8e13a0cdc6e05c7af62e12528e0d65428805b7b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 24 Apr 2024 03:14:18 GMT
ADD file:a3e63beab80160854bfc2d48f69e7c70a9542cdfaf3c5b50f1d6248a998b75ae in / 
# Wed, 24 Apr 2024 03:14:22 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:af25825be002e7bdd52bf28c2fbef5bae0ba9fcef8118e5591a874e7a70b2a62`  
		Last Modified: Wed, 24 Apr 2024 03:25:20 GMT  
		Size: 29.1 MB (29144174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70b69867f90cc0cd6ccf8b72f07ee05c80179a59283d6ce971d9191eaf11afe`  
		Last Modified: Mon, 06 May 2024 23:22:55 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361f75ee595f0c436f725a5dd64b1009cb0da358d19361f68345abf27c392f03`  
		Last Modified: Mon, 06 May 2024 23:22:56 GMT  
		Size: 1.9 MB (1937740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1d3e5a5aad136d9ada8e95bd8e9f609baf923df5c9a48a8021e50206e4e93d`  
		Last Modified: Mon, 06 May 2024 23:22:56 GMT  
		Size: 7.1 MB (7087680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913b327051e93299424d31038856dead21e1781ab1e47927437d8d135ea97338`  
		Last Modified: Mon, 06 May 2024 23:22:55 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a025835eff1c0dfdae38dce98ddefd33f8609362934acbc3106f445279e8b050`  
		Last Modified: Mon, 06 May 2024 23:22:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.27` - unknown; unknown

```console
$ docker pull memcached@sha256:062ba12de9ac3ea604948fc8045fa1f18254e15045b75fd40ba397ca49ddac94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30f78c9e4c785d57060d12fdc33b3579dde0c50533361c63c38632718921c39d`

```dockerfile
```

-	Layers:
	-	`sha256:0f87aa3b54f1e190b0d04cc9d1960d4d745a6c99015f572091bc1c532c971e12`  
		Last Modified: Mon, 06 May 2024 23:22:55 GMT  
		Size: 20.9 KB (20862 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.27` - linux; ppc64le

```console
$ docker pull memcached@sha256:430b7d0dd4212933d73484135db4087f520991a9e0d7499435fbf2e530fd6318
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37163910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7e11c36793a0732a32959b3d851daf998f260c7310adb4bd030bc5efd62c057`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 May 2024 09:14:35 GMT
ADD file:1622c3287b5a5c8a6e0b0b0180489212aab2c9bc7b43390b17a5cc8b153e542a in / 
# Mon, 06 May 2024 09:14:35 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:11ee2a6dbc4a6a6b182097f6023f775e595488a6bcc424e9b58001659deb7fa1`  
		Last Modified: Tue, 14 May 2024 01:24:06 GMT  
		Size: 33.1 MB (33141160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7bc98b1678c7602a43450cf1b5a0b7681ae2f5fc3f2798b1efeacf4b6f816e4`  
		Last Modified: Tue, 14 May 2024 13:32:54 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592eb5f8d51b94ab989902437d4d45fa389f90d9e020376265109959475352c8`  
		Last Modified: Tue, 14 May 2024 13:32:54 GMT  
		Size: 2.7 MB (2698407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d506236222bc33a96c083a536e37019eb18cd167ad0488e486fb7efe603856`  
		Last Modified: Tue, 14 May 2024 13:32:54 GMT  
		Size: 1.3 MB (1322831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cff49951e34e6f3a9bbca8596de07eb85450e57e2a99f66b6ce6d36a5cfa049`  
		Last Modified: Tue, 14 May 2024 13:32:55 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f72d6fdca7ec069335903535d097bd12cf1f35395a355b1b4665ab7ed230d4a2`  
		Last Modified: Tue, 14 May 2024 13:32:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.27` - unknown; unknown

```console
$ docker pull memcached@sha256:c03fdeb43ec264ab9493846e0ed7373f1e0c4353bdabd3a494684f4c321b8611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2286679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:466a2eec05699dc762f3abe6e741f13a1f0fe96e2fede2cf328da8719620ac85`

```dockerfile
```

-	Layers:
	-	`sha256:cd846922ab00a7afbef577d0a4f869b45fae65daea24ae1fec41855f72bc9b61`  
		Last Modified: Tue, 14 May 2024 13:32:54 GMT  
		Size: 2.3 MB (2265632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5104c8ee9f5261628bf21f17c74ad56f6c43c8a852d215728842b3261b1b3974`  
		Last Modified: Tue, 14 May 2024 13:32:54 GMT  
		Size: 21.0 KB (21047 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.27` - linux; s390x

```console
$ docker pull memcached@sha256:8be2074db9458342fce6c40d6ff648ba9c8671d9210c3bd0dabdb386cdc2c639
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30902718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fb8c642e3831e983cd5e8acdee53cd1b4a2f633ffd89c297f50d80745daafa1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 May 2024 09:14:35 GMT
ADD file:55fef93bbad6701fe968a070a0c72b3a0bd3df408dd79c9a616a43dea0de11d0 in / 
# Mon, 06 May 2024 09:14:35 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d7365433874e83ccc92aa5d768989641a64e23c3247409161401a09b4895c406`  
		Last Modified: Tue, 14 May 2024 00:47:35 GMT  
		Size: 27.5 MB (27512398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f6e2c8c427b6988b152cb191a15a2716bbf2dff9f9a6eafebf06f081eebf7b5`  
		Last Modified: Tue, 14 May 2024 17:56:21 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e6d59bd3a243d0242de493c532d8d56b279f05bb1a3d7c58724ea30a716fcf`  
		Last Modified: Tue, 14 May 2024 17:56:21 GMT  
		Size: 2.2 MB (2152659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da6ae628a520dec07948d68ad410a007894a6f040c7305dd8c4628501f77d49`  
		Last Modified: Tue, 14 May 2024 17:56:21 GMT  
		Size: 1.2 MB (1236148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb27d713cf158e879ff43c810aa223cb411f904673225d1d31f1bb782c01cb2`  
		Last Modified: Tue, 14 May 2024 17:56:21 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a400d87b577ef1da8cde4dc345372dd8e53b0d2a3c0e49aa4771038101183470`  
		Last Modified: Tue, 14 May 2024 17:56:22 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.27` - unknown; unknown

```console
$ docker pull memcached@sha256:b400e46dab61c1e9270120428db66b57ee83545f05b9bf07b59489dde48c10eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0dcf8c510ed87cdfbca560a9fa5173caed7b13966e9ddbf6a1fbaf8203265d4`

```dockerfile
```

-	Layers:
	-	`sha256:c437e8e5e7b32562cd1a77d98c41ff5a5bcf8c18102d8304295fe16c0342e460`  
		Last Modified: Tue, 14 May 2024 17:56:21 GMT  
		Size: 2.3 MB (2261082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ae942851d074d6a0dd2bdcb21bd9e83ec34c7bfd585ffd21811c317eb715284`  
		Last Modified: Tue, 14 May 2024 17:56:21 GMT  
		Size: 21.0 KB (20979 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.27-alpine`

```console
$ docker pull memcached@sha256:4ee2d6582442b4920f0c9de6565947a81e18abc48089804df10251eedf388d66
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

### `memcached:1.6.27-alpine` - linux; amd64

```console
$ docker pull memcached@sha256:cf854f636d506c0834dc1159ad5b472fea96028e88702014088384915a7c08dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6535198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21047320ccba2e62e0ee66c1ffa169149658e039ee012547c37ed6aa0130ad2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59605d18a5ec7e6531bd08f0238da758082d075c4fdd6a4ec8c00fd6f792425b`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8691b75405b7042ea4a853223cc80432131a0e21745f3baf9b21b00073207ace`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 104.2 KB (104211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8925d4d8379f9d71921da012b62d23d71f826e429777c701a1b0d4d56d0399ac`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 3.0 MB (3020613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86013193f6f292637e997c2518f84ab28fec9d7a494cda4090d07457058f10de`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10cfe77bbca77075d0b682e8546bca4d6d045cfbff0be0336d51b7bbe1116983`  
		Last Modified: Mon, 06 May 2024 23:08:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.27-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:d4a846cbc9f47d5db83dbb38f019064556e6af28dad33264b1f851bebbb2858b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ab3ae8df84416fe4351914e6bb061214bfad4b0cb01537aef674b02c008994`

```dockerfile
```

-	Layers:
	-	`sha256:59634fa6bbcc5be09a70b3894761425c9ea7b231a189445bce9ae40b97f09675`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 88.1 KB (88149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2fd487a2e71a464ab83cce092819d041b742e29af0ecb901bcb36ac21fc7c2c`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 19.5 KB (19475 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.27-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:8a6f18eb424270a1dca99143a613014d570cb7376c9cb7d212b72d74c569b12a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6381171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8ddcb41c8f4d78c4720e1ad02b3c978ef7af38607d717e52219f0c53ab6fb64`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859f5f148ebb49ed2dfc712d036c8e1162fd5c08307e622f420c9e722f459c15`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a85abddca9696d1381e2dbbf52914e6119f22bd22e71c1ffc49aa385ca2d79`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 120.9 KB (120900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f80774db5f2d9cd2ec4f0bf8e7256768ab2ff5b90e1a822c70e5fb0a8d0a42`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 2.9 MB (2910908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fff6ea9e3e8e56264cef5ba1ceaacc5db1aa37fb687bf4cb684629a462a4e04`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e6b3e687f63ee869e2595d746eecfc9a9a64e49c7972eea118f9af26f3a02f`  
		Last Modified: Mon, 06 May 2024 23:43:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.27-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7677dd609f55b7dac25e997d7fc4942f1b433f1084ca54e71a01175c8608fedb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cce1cbd3428e47f29034986dc018cfef4ed121b030aef195db0d03c8a65cc79d`

```dockerfile
```

-	Layers:
	-	`sha256:c80e817fe71d2bd7ff1d9709ab1ac3d7ac30315b7cfd1b528ca1c316fecabc2f`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 88.2 KB (88168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b568b0dd9cb0ef2428bd10a39e9ee3afe06fe97f6911abc8c1ae5e642b27094`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 19.3 KB (19326 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.27-alpine` - linux; 386

```console
$ docker pull memcached@sha256:1557e39ed6b5f943d53c54797d59f4ea27755c53c9e7004cbfb633c08757abd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6194136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d48e3a30b8d39f2e6434ff10c1130366a5bfeac640bc8ecb88f89e6e996cdc4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c853f4fd5c9ee2e18e52b4399ccc43726449928a43d040161f83d3f67f596dd`  
		Last Modified: Mon, 06 May 2024 23:08:35 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca2d91782956c7a9591fd3f9edb724367e6a2770f04a809c6088a8ea623ea7f`  
		Last Modified: Mon, 06 May 2024 23:08:36 GMT  
		Size: 109.3 KB (109328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5c07db0e07d757431d4458ea14990c3cc0b06aa9577b0e29f8db33fc51921b`  
		Last Modified: Mon, 06 May 2024 23:08:36 GMT  
		Size: 2.8 MB (2839076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21633262023f9a6ae09f480b39a8a9a7109a0201b779ccdba90e721204cb20ae`  
		Last Modified: Mon, 06 May 2024 23:08:36 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893c3463887c0e33218f5af72fe7534fe9bebd41fd26e976944bbd03c13a9d22`  
		Last Modified: Mon, 06 May 2024 23:08:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.27-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:4184448ad3b3ff9a34654847c26c9ad677ce54b07e8a96eedb429e8c509fe5e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04225924b78526836b6ef1d8f4bd3d25e994e9f858bedc4d73fbf5308500d074`

```dockerfile
```

-	Layers:
	-	`sha256:562178e7885ee7492a868cc754c309fe7cf0a52b74299dc570dc9959ecfc0c10`  
		Last Modified: Mon, 06 May 2024 23:08:36 GMT  
		Size: 88.1 KB (88104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d1f3d52b695ee750a517e356c17e9f3b6a3778f607f791f558ae9e31397df3f`  
		Last Modified: Mon, 06 May 2024 23:08:35 GMT  
		Size: 19.4 KB (19420 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.27-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:4b1fdeda480d0b679c2b9fa5a09c508dabaf7bf0bf1600d0078fcae81e004dd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6407037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf112675855fb5780056fbde79f0822c329da1cfb19ca47270289ec2ac966e77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25735f744a453fbf0af2d088f79a0fa6de45cc2699601389d42141b2de2f21d3`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a61320e5e6694b8436a4074ba6280369b9b29e2474231252683fa11606b8e6`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 123.4 KB (123401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e809f0a1acfe802b3158bb0d4d370427885e8c5ba2ce6b98549da9bbac597e`  
		Last Modified: Mon, 06 May 2024 23:39:16 GMT  
		Size: 2.9 MB (2923638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99dc3c24ef4a44c763efcf66a6e3e44d31d723683dd339c343770bd43523007`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0b13828c450ce09acf99d42e4d9e625dbc1991b6f87a5727ff595e3e62a06c`  
		Last Modified: Mon, 06 May 2024 23:39:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.27-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:d1dc50ec127cc25ab5b90bbe3fccaf4c5cda1379629dcd1760fa93b6cab32718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 KB (105629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7934a2d41084621a7a7ff3aafbea88a9edfb76ded1149d611483fb61826d661`

```dockerfile
```

-	Layers:
	-	`sha256:dedf3264102cee8df6c9d7e964dedede98ab6b3865d8df8f76e88eeb42290632`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 86.3 KB (86253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b25fbb2f936e2b3483885e59398fdcffdf62a984c55d6171eb02b6a8b6ef44d7`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 19.4 KB (19376 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.27-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:16979dbfdc08cb52efcfffcdfdff35be32426e49b90065b36155882be545d88b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6151853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cca463729a03d73b6abb17295ed77bc6a13a336b4bc01a3b1c03a176f34fa06`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a6f11688a0fb8016d54f0f889fc4e07b5c17c62112125611f7c620bc7d3f99`  
		Last Modified: Sun, 17 Mar 2024 22:11:54 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a294d63f4311d022fef15282f082670fab839cd31782b0d6e3e8c12044283a`  
		Last Modified: Sun, 17 Mar 2024 22:11:54 GMT  
		Size: 113.1 KB (113140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d6a06c9130de338c39b57baed51f1e62b01cf60bb33a109ac31927ab8c775f`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 2.8 MB (2794432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db042a56f7b2a4ea616aa34e4b563284ea5d38557c0ff85c04706fc945bc905`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e7dbc7d250abc9822b7e752e47c8b83dd404648d74f9331600b392ac836970`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.27-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:b885694442ff65cade16142bde9307eda742f797b4c4e48b95e2ecd62c262746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 KB (105504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:023ebbf730f939171a6dd74509e836130fe404e073174c8b1be5b28fd09e514e`

```dockerfile
```

-	Layers:
	-	`sha256:b18acb410267cb31ce209d09681474ba43f18c2f4af00288845c4061bd220974`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 86.2 KB (86195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48c7d2c81f6bbcf60c7bbca78ec3114f620154531205c592fe14d252cb9daf08`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 19.3 KB (19309 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.27-alpine3.19`

```console
$ docker pull memcached@sha256:4ee2d6582442b4920f0c9de6565947a81e18abc48089804df10251eedf388d66
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

### `memcached:1.6.27-alpine3.19` - linux; amd64

```console
$ docker pull memcached@sha256:cf854f636d506c0834dc1159ad5b472fea96028e88702014088384915a7c08dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6535198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21047320ccba2e62e0ee66c1ffa169149658e039ee012547c37ed6aa0130ad2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59605d18a5ec7e6531bd08f0238da758082d075c4fdd6a4ec8c00fd6f792425b`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8691b75405b7042ea4a853223cc80432131a0e21745f3baf9b21b00073207ace`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 104.2 KB (104211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8925d4d8379f9d71921da012b62d23d71f826e429777c701a1b0d4d56d0399ac`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 3.0 MB (3020613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86013193f6f292637e997c2518f84ab28fec9d7a494cda4090d07457058f10de`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10cfe77bbca77075d0b682e8546bca4d6d045cfbff0be0336d51b7bbe1116983`  
		Last Modified: Mon, 06 May 2024 23:08:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.27-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:d4a846cbc9f47d5db83dbb38f019064556e6af28dad33264b1f851bebbb2858b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ab3ae8df84416fe4351914e6bb061214bfad4b0cb01537aef674b02c008994`

```dockerfile
```

-	Layers:
	-	`sha256:59634fa6bbcc5be09a70b3894761425c9ea7b231a189445bce9ae40b97f09675`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 88.1 KB (88149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2fd487a2e71a464ab83cce092819d041b742e29af0ecb901bcb36ac21fc7c2c`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 19.5 KB (19475 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.27-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:8a6f18eb424270a1dca99143a613014d570cb7376c9cb7d212b72d74c569b12a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6381171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8ddcb41c8f4d78c4720e1ad02b3c978ef7af38607d717e52219f0c53ab6fb64`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859f5f148ebb49ed2dfc712d036c8e1162fd5c08307e622f420c9e722f459c15`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a85abddca9696d1381e2dbbf52914e6119f22bd22e71c1ffc49aa385ca2d79`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 120.9 KB (120900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f80774db5f2d9cd2ec4f0bf8e7256768ab2ff5b90e1a822c70e5fb0a8d0a42`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 2.9 MB (2910908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fff6ea9e3e8e56264cef5ba1ceaacc5db1aa37fb687bf4cb684629a462a4e04`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e6b3e687f63ee869e2595d746eecfc9a9a64e49c7972eea118f9af26f3a02f`  
		Last Modified: Mon, 06 May 2024 23:43:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.27-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:7677dd609f55b7dac25e997d7fc4942f1b433f1084ca54e71a01175c8608fedb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cce1cbd3428e47f29034986dc018cfef4ed121b030aef195db0d03c8a65cc79d`

```dockerfile
```

-	Layers:
	-	`sha256:c80e817fe71d2bd7ff1d9709ab1ac3d7ac30315b7cfd1b528ca1c316fecabc2f`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 88.2 KB (88168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b568b0dd9cb0ef2428bd10a39e9ee3afe06fe97f6911abc8c1ae5e642b27094`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 19.3 KB (19326 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.27-alpine3.19` - linux; 386

```console
$ docker pull memcached@sha256:1557e39ed6b5f943d53c54797d59f4ea27755c53c9e7004cbfb633c08757abd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6194136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d48e3a30b8d39f2e6434ff10c1130366a5bfeac640bc8ecb88f89e6e996cdc4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c853f4fd5c9ee2e18e52b4399ccc43726449928a43d040161f83d3f67f596dd`  
		Last Modified: Mon, 06 May 2024 23:08:35 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca2d91782956c7a9591fd3f9edb724367e6a2770f04a809c6088a8ea623ea7f`  
		Last Modified: Mon, 06 May 2024 23:08:36 GMT  
		Size: 109.3 KB (109328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5c07db0e07d757431d4458ea14990c3cc0b06aa9577b0e29f8db33fc51921b`  
		Last Modified: Mon, 06 May 2024 23:08:36 GMT  
		Size: 2.8 MB (2839076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21633262023f9a6ae09f480b39a8a9a7109a0201b779ccdba90e721204cb20ae`  
		Last Modified: Mon, 06 May 2024 23:08:36 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893c3463887c0e33218f5af72fe7534fe9bebd41fd26e976944bbd03c13a9d22`  
		Last Modified: Mon, 06 May 2024 23:08:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.27-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:4184448ad3b3ff9a34654847c26c9ad677ce54b07e8a96eedb429e8c509fe5e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04225924b78526836b6ef1d8f4bd3d25e994e9f858bedc4d73fbf5308500d074`

```dockerfile
```

-	Layers:
	-	`sha256:562178e7885ee7492a868cc754c309fe7cf0a52b74299dc570dc9959ecfc0c10`  
		Last Modified: Mon, 06 May 2024 23:08:36 GMT  
		Size: 88.1 KB (88104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d1f3d52b695ee750a517e356c17e9f3b6a3778f607f791f558ae9e31397df3f`  
		Last Modified: Mon, 06 May 2024 23:08:35 GMT  
		Size: 19.4 KB (19420 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.27-alpine3.19` - linux; ppc64le

```console
$ docker pull memcached@sha256:4b1fdeda480d0b679c2b9fa5a09c508dabaf7bf0bf1600d0078fcae81e004dd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6407037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf112675855fb5780056fbde79f0822c329da1cfb19ca47270289ec2ac966e77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25735f744a453fbf0af2d088f79a0fa6de45cc2699601389d42141b2de2f21d3`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a61320e5e6694b8436a4074ba6280369b9b29e2474231252683fa11606b8e6`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 123.4 KB (123401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e809f0a1acfe802b3158bb0d4d370427885e8c5ba2ce6b98549da9bbac597e`  
		Last Modified: Mon, 06 May 2024 23:39:16 GMT  
		Size: 2.9 MB (2923638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99dc3c24ef4a44c763efcf66a6e3e44d31d723683dd339c343770bd43523007`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0b13828c450ce09acf99d42e4d9e625dbc1991b6f87a5727ff595e3e62a06c`  
		Last Modified: Mon, 06 May 2024 23:39:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.27-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:d1dc50ec127cc25ab5b90bbe3fccaf4c5cda1379629dcd1760fa93b6cab32718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 KB (105629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7934a2d41084621a7a7ff3aafbea88a9edfb76ded1149d611483fb61826d661`

```dockerfile
```

-	Layers:
	-	`sha256:dedf3264102cee8df6c9d7e964dedede98ab6b3865d8df8f76e88eeb42290632`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 86.3 KB (86253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b25fbb2f936e2b3483885e59398fdcffdf62a984c55d6171eb02b6a8b6ef44d7`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 19.4 KB (19376 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.27-alpine3.19` - linux; s390x

```console
$ docker pull memcached@sha256:16979dbfdc08cb52efcfffcdfdff35be32426e49b90065b36155882be545d88b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6151853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cca463729a03d73b6abb17295ed77bc6a13a336b4bc01a3b1c03a176f34fa06`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a6f11688a0fb8016d54f0f889fc4e07b5c17c62112125611f7c620bc7d3f99`  
		Last Modified: Sun, 17 Mar 2024 22:11:54 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a294d63f4311d022fef15282f082670fab839cd31782b0d6e3e8c12044283a`  
		Last Modified: Sun, 17 Mar 2024 22:11:54 GMT  
		Size: 113.1 KB (113140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d6a06c9130de338c39b57baed51f1e62b01cf60bb33a109ac31927ab8c775f`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 2.8 MB (2794432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db042a56f7b2a4ea616aa34e4b563284ea5d38557c0ff85c04706fc945bc905`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e7dbc7d250abc9822b7e752e47c8b83dd404648d74f9331600b392ac836970`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.27-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:b885694442ff65cade16142bde9307eda742f797b4c4e48b95e2ecd62c262746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 KB (105504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:023ebbf730f939171a6dd74509e836130fe404e073174c8b1be5b28fd09e514e`

```dockerfile
```

-	Layers:
	-	`sha256:b18acb410267cb31ce209d09681474ba43f18c2f4af00288845c4061bd220974`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 86.2 KB (86195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48c7d2c81f6bbcf60c7bbca78ec3114f620154531205c592fe14d252cb9daf08`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 19.3 KB (19309 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.27-bookworm`

```console
$ docker pull memcached@sha256:1a37ac11adba27f1f29a81b85c6c242f6513d47757f99d2cbca5308fc5a5e0f2
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

### `memcached:1.6.27-bookworm` - linux; amd64

```console
$ docker pull memcached@sha256:7e88c146c7393fbcb8c981efcbebc410fe430f7e47593f7c7b19c1864fd8a793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32897352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4274125721ccfb5bf3696e35b8620677e442c1f5885aee1323d244ea4137214`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 May 2024 09:14:35 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Mon, 06 May 2024 09:14:35 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2aa97235084d1e9d96dcd82d59f52808027df2e6bd8df2b984b207c107037d6`  
		Last Modified: Tue, 14 May 2024 02:59:09 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c3eebfc2348c666ba1f14edd94df803c126159dd54a27513273f0c9ff2090b`  
		Last Modified: Tue, 14 May 2024 02:59:10 GMT  
		Size: 2.5 MB (2488483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5520a877f09a00e2d06002be9ff44b80c1044928b980ca9709460a4727ed9da6`  
		Last Modified: Tue, 14 May 2024 02:59:10 GMT  
		Size: 1.3 MB (1256949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe67d33c4a6967ba167fd89d19b671a74e19edb04bbe7ec7d3f4550f55d4569`  
		Last Modified: Tue, 14 May 2024 02:59:10 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450e4b8762758af67b4a485fc7041c56793f6094aa4548f89489e659396a5e35`  
		Last Modified: Tue, 14 May 2024 02:59:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.27-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:d8234d3b08b2d3a9b10f5cc7d7e8eeb881e9c71181619c2345871819be563eac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac0e31e9e20cd7d2eb5081055e082080168b1caffa48f1900a5efabb1a24537b`

```dockerfile
```

-	Layers:
	-	`sha256:bccfaa47fb8f608ebb8952b834915de2a6992656e4c56e611a32e8089167dc68`  
		Last Modified: Tue, 14 May 2024 02:59:10 GMT  
		Size: 2.3 MB (2261261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c86e940f075920cebfa2e40582ec611de7bff05d54bb06038bd3c50323add52`  
		Last Modified: Tue, 14 May 2024 02:59:09 GMT  
		Size: 21.1 KB (21146 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.27-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:0caa5d2f391d90fc8c56ad5009add403a518055de2115d6fd31e15e14297135c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30237095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:187a7263d807afaef1f10562634f3c06a7096cabb2f319e9ac2e644318303379`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 May 2024 09:14:35 GMT
ADD file:ee9f1914c7fc370bdb089c9e2fcfa15477f7091fc5437cb780232afdf6297586 in / 
# Mon, 06 May 2024 09:14:35 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:169fcae2368e5a601c42972560f091e123648fa0e741975d1b35900c61b9ff71`  
		Last Modified: Tue, 14 May 2024 00:51:36 GMT  
		Size: 26.9 MB (26909921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac2fb1ba5d31602a2c107dc7adc208fd66c3597693d97ca3a1743f80eb34c42`  
		Last Modified: Tue, 14 May 2024 14:50:47 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b482143aab2b97abcc7fe5e07ac0d3b24ac4ee147e8465846ada4f6bc2e4690f`  
		Last Modified: Tue, 14 May 2024 14:50:47 GMT  
		Size: 2.1 MB (2089496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7be0b16f146e3e0539004d2e158b62018843cb744689765fc6cb9048b3ccba3`  
		Last Modified: Tue, 14 May 2024 14:50:48 GMT  
		Size: 1.2 MB (1236170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ca6e022ab5c893f1324b016376e333d0e3af3d4eaf27ef824a8cb1ddb4ae16`  
		Last Modified: Tue, 14 May 2024 14:50:47 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14149cf3cd0dfd764982a3a1cb86460e564857ff4081b31ce6fa220d1271dc4f`  
		Last Modified: Tue, 14 May 2024 14:50:48 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.27-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:1846968895df68a70d92115780645a44cf0dff66edba584baff89764b3e902ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2285669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f19cddf29de06aa8a4c98debec36ac562df1f72b08de9c99bb7dcf388eff13ed`

```dockerfile
```

-	Layers:
	-	`sha256:4402e51b44f21e94146beef550d2f20402f932229666cd1bec4f48401cb43742`  
		Last Modified: Tue, 14 May 2024 14:50:47 GMT  
		Size: 2.3 MB (2264549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6f1c335ae222da5a6b0848b8c0960a13c272ccb39a51c22fa05b33276a341f4`  
		Last Modified: Tue, 14 May 2024 14:50:47 GMT  
		Size: 21.1 KB (21120 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.27-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:b953ca66ecee777524a0f33f0adefbe99183367e180f4b2ed82d1e525f57d208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32780663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a9c7e97a66ca554c0cfc88de871b1c7dfad7637ffcbd6a79b5c75b3954bb583`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 May 2024 09:14:35 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Mon, 06 May 2024 09:14:35 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994933505bafbbaba95cef494f2dfb3e85f2bfde1ea5c4a6dae5a179e39e7b5c`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9488359f89f8c6691f1737ce76ce6b7520511a8246658953dae9429090e88746`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 2.3 MB (2346183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27fa925bb96d2305b22651dc4d10899309c212aef95cb13afbdeb2ba5436cb0b`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 1.3 MB (1253469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5284a06f3ca2503602cf214d936daf8aedee3d442d7aa66a5b67874c8f156685`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a475f5b1bcd9a980f0e2923bf1af87002c6468529583ce41a151599d11b2cc`  
		Last Modified: Tue, 14 May 2024 17:41:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.27-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:303a74af5e224338560198dc50e2c9cb2a7b4a46b01d39144559de1dd7788518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e79fb901bf217f30113856b6b39e296324993066435904abd2a2152baae6156`

```dockerfile
```

-	Layers:
	-	`sha256:a35747f1af90484d4a9021de5c31be89cb3117cb5f56f499d3cebe78562716cf`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 2.3 MB (2261490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c48c7060af35b31db7e804b3ce19451726c3fb6b956edad221ee58000cf04a91`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 21.0 KB (20997 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.27-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:3f542cc336b40813213949d5eb8e2da1a57005f88566c0d51c3b8624cc911916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33914242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a44cb325942314e83e433868ace554ffea1c0ef303993f238620f928b36bbcf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 May 2024 09:14:35 GMT
ADD file:252f04703c9ed01e5aa32f764c7d751f0a3b17ed9ef1961cd1972aa8453b5cf3 in / 
# Mon, 06 May 2024 09:14:35 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7075ead1c5d56dc11510b76b25c291657dc73ecf7daad5361939429487745b9a`  
		Last Modified: Tue, 14 May 2024 00:51:58 GMT  
		Size: 30.2 MB (30162638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa82d06bb0cba58ed3fae5da8ee9c6248a027c9d105f1c1e2094d1973ab2f78`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf14cdbfbd6ea1d7231b4119cb6c85336718c7ccee9bc57573aadcc210f05e2`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 2.5 MB (2492686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bed32b6d0ec7a40384a2ba4d5fa14871afba5fd572025e99ebc3c30541ee6bf`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 1.3 MB (1257406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07ba6ac3de2271f181cd17c67b57573da49f54d516ad3c852a2610d138c85b3`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a700f395f10bfe9002c02677754b0a58c0ee8ca0f1fc73477ef1b86dc734103b`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.27-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:8932028ec9d6cdd607a57df36f524623a045c35db7110aa26040859db5599b8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2279450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:303c5c842506ac0858dd708f266252ee2b586ba9dd6f506ef93e95c9d4d06402`

```dockerfile
```

-	Layers:
	-	`sha256:e55268858bc5b4c5b04534306d270b5c41b3d3dccd563cae845878933e3d7a1c`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 2.3 MB (2258359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4afdfadae6d39596deea4cc7598059a6d7cdd84a4bf4036bfd609cacb9347c22`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 21.1 KB (21091 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.27-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:54a6cf440988b85512b266a181d2e83efe8a6a16530029f48b2fd002efb2e251
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38171114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac4ac5a7759abeb1658c052e8e13a0cdc6e05c7af62e12528e0d65428805b7b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 24 Apr 2024 03:14:18 GMT
ADD file:a3e63beab80160854bfc2d48f69e7c70a9542cdfaf3c5b50f1d6248a998b75ae in / 
# Wed, 24 Apr 2024 03:14:22 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:af25825be002e7bdd52bf28c2fbef5bae0ba9fcef8118e5591a874e7a70b2a62`  
		Last Modified: Wed, 24 Apr 2024 03:25:20 GMT  
		Size: 29.1 MB (29144174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70b69867f90cc0cd6ccf8b72f07ee05c80179a59283d6ce971d9191eaf11afe`  
		Last Modified: Mon, 06 May 2024 23:22:55 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361f75ee595f0c436f725a5dd64b1009cb0da358d19361f68345abf27c392f03`  
		Last Modified: Mon, 06 May 2024 23:22:56 GMT  
		Size: 1.9 MB (1937740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1d3e5a5aad136d9ada8e95bd8e9f609baf923df5c9a48a8021e50206e4e93d`  
		Last Modified: Mon, 06 May 2024 23:22:56 GMT  
		Size: 7.1 MB (7087680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913b327051e93299424d31038856dead21e1781ab1e47927437d8d135ea97338`  
		Last Modified: Mon, 06 May 2024 23:22:55 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a025835eff1c0dfdae38dce98ddefd33f8609362934acbc3106f445279e8b050`  
		Last Modified: Mon, 06 May 2024 23:22:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.27-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:062ba12de9ac3ea604948fc8045fa1f18254e15045b75fd40ba397ca49ddac94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30f78c9e4c785d57060d12fdc33b3579dde0c50533361c63c38632718921c39d`

```dockerfile
```

-	Layers:
	-	`sha256:0f87aa3b54f1e190b0d04cc9d1960d4d745a6c99015f572091bc1c532c971e12`  
		Last Modified: Mon, 06 May 2024 23:22:55 GMT  
		Size: 20.9 KB (20862 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.27-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:430b7d0dd4212933d73484135db4087f520991a9e0d7499435fbf2e530fd6318
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37163910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7e11c36793a0732a32959b3d851daf998f260c7310adb4bd030bc5efd62c057`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 May 2024 09:14:35 GMT
ADD file:1622c3287b5a5c8a6e0b0b0180489212aab2c9bc7b43390b17a5cc8b153e542a in / 
# Mon, 06 May 2024 09:14:35 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:11ee2a6dbc4a6a6b182097f6023f775e595488a6bcc424e9b58001659deb7fa1`  
		Last Modified: Tue, 14 May 2024 01:24:06 GMT  
		Size: 33.1 MB (33141160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7bc98b1678c7602a43450cf1b5a0b7681ae2f5fc3f2798b1efeacf4b6f816e4`  
		Last Modified: Tue, 14 May 2024 13:32:54 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592eb5f8d51b94ab989902437d4d45fa389f90d9e020376265109959475352c8`  
		Last Modified: Tue, 14 May 2024 13:32:54 GMT  
		Size: 2.7 MB (2698407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d506236222bc33a96c083a536e37019eb18cd167ad0488e486fb7efe603856`  
		Last Modified: Tue, 14 May 2024 13:32:54 GMT  
		Size: 1.3 MB (1322831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cff49951e34e6f3a9bbca8596de07eb85450e57e2a99f66b6ce6d36a5cfa049`  
		Last Modified: Tue, 14 May 2024 13:32:55 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f72d6fdca7ec069335903535d097bd12cf1f35395a355b1b4665ab7ed230d4a2`  
		Last Modified: Tue, 14 May 2024 13:32:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.27-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:c03fdeb43ec264ab9493846e0ed7373f1e0c4353bdabd3a494684f4c321b8611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2286679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:466a2eec05699dc762f3abe6e741f13a1f0fe96e2fede2cf328da8719620ac85`

```dockerfile
```

-	Layers:
	-	`sha256:cd846922ab00a7afbef577d0a4f869b45fae65daea24ae1fec41855f72bc9b61`  
		Last Modified: Tue, 14 May 2024 13:32:54 GMT  
		Size: 2.3 MB (2265632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5104c8ee9f5261628bf21f17c74ad56f6c43c8a852d215728842b3261b1b3974`  
		Last Modified: Tue, 14 May 2024 13:32:54 GMT  
		Size: 21.0 KB (21047 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.27-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:8be2074db9458342fce6c40d6ff648ba9c8671d9210c3bd0dabdb386cdc2c639
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30902718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fb8c642e3831e983cd5e8acdee53cd1b4a2f633ffd89c297f50d80745daafa1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 May 2024 09:14:35 GMT
ADD file:55fef93bbad6701fe968a070a0c72b3a0bd3df408dd79c9a616a43dea0de11d0 in / 
# Mon, 06 May 2024 09:14:35 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d7365433874e83ccc92aa5d768989641a64e23c3247409161401a09b4895c406`  
		Last Modified: Tue, 14 May 2024 00:47:35 GMT  
		Size: 27.5 MB (27512398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f6e2c8c427b6988b152cb191a15a2716bbf2dff9f9a6eafebf06f081eebf7b5`  
		Last Modified: Tue, 14 May 2024 17:56:21 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e6d59bd3a243d0242de493c532d8d56b279f05bb1a3d7c58724ea30a716fcf`  
		Last Modified: Tue, 14 May 2024 17:56:21 GMT  
		Size: 2.2 MB (2152659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da6ae628a520dec07948d68ad410a007894a6f040c7305dd8c4628501f77d49`  
		Last Modified: Tue, 14 May 2024 17:56:21 GMT  
		Size: 1.2 MB (1236148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb27d713cf158e879ff43c810aa223cb411f904673225d1d31f1bb782c01cb2`  
		Last Modified: Tue, 14 May 2024 17:56:21 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a400d87b577ef1da8cde4dc345372dd8e53b0d2a3c0e49aa4771038101183470`  
		Last Modified: Tue, 14 May 2024 17:56:22 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.27-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:b400e46dab61c1e9270120428db66b57ee83545f05b9bf07b59489dde48c10eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0dcf8c510ed87cdfbca560a9fa5173caed7b13966e9ddbf6a1fbaf8203265d4`

```dockerfile
```

-	Layers:
	-	`sha256:c437e8e5e7b32562cd1a77d98c41ff5a5bcf8c18102d8304295fe16c0342e460`  
		Last Modified: Tue, 14 May 2024 17:56:21 GMT  
		Size: 2.3 MB (2261082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ae942851d074d6a0dd2bdcb21bd9e83ec34c7bfd585ffd21811c317eb715284`  
		Last Modified: Tue, 14 May 2024 17:56:21 GMT  
		Size: 21.0 KB (20979 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine`

```console
$ docker pull memcached@sha256:4ee2d6582442b4920f0c9de6565947a81e18abc48089804df10251eedf388d66
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

### `memcached:alpine` - linux; amd64

```console
$ docker pull memcached@sha256:cf854f636d506c0834dc1159ad5b472fea96028e88702014088384915a7c08dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6535198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21047320ccba2e62e0ee66c1ffa169149658e039ee012547c37ed6aa0130ad2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59605d18a5ec7e6531bd08f0238da758082d075c4fdd6a4ec8c00fd6f792425b`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8691b75405b7042ea4a853223cc80432131a0e21745f3baf9b21b00073207ace`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 104.2 KB (104211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8925d4d8379f9d71921da012b62d23d71f826e429777c701a1b0d4d56d0399ac`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 3.0 MB (3020613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86013193f6f292637e997c2518f84ab28fec9d7a494cda4090d07457058f10de`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10cfe77bbca77075d0b682e8546bca4d6d045cfbff0be0336d51b7bbe1116983`  
		Last Modified: Mon, 06 May 2024 23:08:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:d4a846cbc9f47d5db83dbb38f019064556e6af28dad33264b1f851bebbb2858b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ab3ae8df84416fe4351914e6bb061214bfad4b0cb01537aef674b02c008994`

```dockerfile
```

-	Layers:
	-	`sha256:59634fa6bbcc5be09a70b3894761425c9ea7b231a189445bce9ae40b97f09675`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 88.1 KB (88149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2fd487a2e71a464ab83cce092819d041b742e29af0ecb901bcb36ac21fc7c2c`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 19.5 KB (19475 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:8a6f18eb424270a1dca99143a613014d570cb7376c9cb7d212b72d74c569b12a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6381171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8ddcb41c8f4d78c4720e1ad02b3c978ef7af38607d717e52219f0c53ab6fb64`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859f5f148ebb49ed2dfc712d036c8e1162fd5c08307e622f420c9e722f459c15`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a85abddca9696d1381e2dbbf52914e6119f22bd22e71c1ffc49aa385ca2d79`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 120.9 KB (120900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f80774db5f2d9cd2ec4f0bf8e7256768ab2ff5b90e1a822c70e5fb0a8d0a42`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 2.9 MB (2910908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fff6ea9e3e8e56264cef5ba1ceaacc5db1aa37fb687bf4cb684629a462a4e04`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e6b3e687f63ee869e2595d746eecfc9a9a64e49c7972eea118f9af26f3a02f`  
		Last Modified: Mon, 06 May 2024 23:43:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:7677dd609f55b7dac25e997d7fc4942f1b433f1084ca54e71a01175c8608fedb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cce1cbd3428e47f29034986dc018cfef4ed121b030aef195db0d03c8a65cc79d`

```dockerfile
```

-	Layers:
	-	`sha256:c80e817fe71d2bd7ff1d9709ab1ac3d7ac30315b7cfd1b528ca1c316fecabc2f`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 88.2 KB (88168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b568b0dd9cb0ef2428bd10a39e9ee3afe06fe97f6911abc8c1ae5e642b27094`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 19.3 KB (19326 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; 386

```console
$ docker pull memcached@sha256:1557e39ed6b5f943d53c54797d59f4ea27755c53c9e7004cbfb633c08757abd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6194136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d48e3a30b8d39f2e6434ff10c1130366a5bfeac640bc8ecb88f89e6e996cdc4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c853f4fd5c9ee2e18e52b4399ccc43726449928a43d040161f83d3f67f596dd`  
		Last Modified: Mon, 06 May 2024 23:08:35 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca2d91782956c7a9591fd3f9edb724367e6a2770f04a809c6088a8ea623ea7f`  
		Last Modified: Mon, 06 May 2024 23:08:36 GMT  
		Size: 109.3 KB (109328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5c07db0e07d757431d4458ea14990c3cc0b06aa9577b0e29f8db33fc51921b`  
		Last Modified: Mon, 06 May 2024 23:08:36 GMT  
		Size: 2.8 MB (2839076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21633262023f9a6ae09f480b39a8a9a7109a0201b779ccdba90e721204cb20ae`  
		Last Modified: Mon, 06 May 2024 23:08:36 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893c3463887c0e33218f5af72fe7534fe9bebd41fd26e976944bbd03c13a9d22`  
		Last Modified: Mon, 06 May 2024 23:08:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:4184448ad3b3ff9a34654847c26c9ad677ce54b07e8a96eedb429e8c509fe5e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04225924b78526836b6ef1d8f4bd3d25e994e9f858bedc4d73fbf5308500d074`

```dockerfile
```

-	Layers:
	-	`sha256:562178e7885ee7492a868cc754c309fe7cf0a52b74299dc570dc9959ecfc0c10`  
		Last Modified: Mon, 06 May 2024 23:08:36 GMT  
		Size: 88.1 KB (88104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d1f3d52b695ee750a517e356c17e9f3b6a3778f607f791f558ae9e31397df3f`  
		Last Modified: Mon, 06 May 2024 23:08:35 GMT  
		Size: 19.4 KB (19420 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:4b1fdeda480d0b679c2b9fa5a09c508dabaf7bf0bf1600d0078fcae81e004dd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6407037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf112675855fb5780056fbde79f0822c329da1cfb19ca47270289ec2ac966e77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25735f744a453fbf0af2d088f79a0fa6de45cc2699601389d42141b2de2f21d3`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a61320e5e6694b8436a4074ba6280369b9b29e2474231252683fa11606b8e6`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 123.4 KB (123401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e809f0a1acfe802b3158bb0d4d370427885e8c5ba2ce6b98549da9bbac597e`  
		Last Modified: Mon, 06 May 2024 23:39:16 GMT  
		Size: 2.9 MB (2923638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99dc3c24ef4a44c763efcf66a6e3e44d31d723683dd339c343770bd43523007`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0b13828c450ce09acf99d42e4d9e625dbc1991b6f87a5727ff595e3e62a06c`  
		Last Modified: Mon, 06 May 2024 23:39:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:d1dc50ec127cc25ab5b90bbe3fccaf4c5cda1379629dcd1760fa93b6cab32718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 KB (105629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7934a2d41084621a7a7ff3aafbea88a9edfb76ded1149d611483fb61826d661`

```dockerfile
```

-	Layers:
	-	`sha256:dedf3264102cee8df6c9d7e964dedede98ab6b3865d8df8f76e88eeb42290632`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 86.3 KB (86253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b25fbb2f936e2b3483885e59398fdcffdf62a984c55d6171eb02b6a8b6ef44d7`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 19.4 KB (19376 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; s390x

```console
$ docker pull memcached@sha256:16979dbfdc08cb52efcfffcdfdff35be32426e49b90065b36155882be545d88b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6151853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cca463729a03d73b6abb17295ed77bc6a13a336b4bc01a3b1c03a176f34fa06`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a6f11688a0fb8016d54f0f889fc4e07b5c17c62112125611f7c620bc7d3f99`  
		Last Modified: Sun, 17 Mar 2024 22:11:54 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a294d63f4311d022fef15282f082670fab839cd31782b0d6e3e8c12044283a`  
		Last Modified: Sun, 17 Mar 2024 22:11:54 GMT  
		Size: 113.1 KB (113140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d6a06c9130de338c39b57baed51f1e62b01cf60bb33a109ac31927ab8c775f`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 2.8 MB (2794432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db042a56f7b2a4ea616aa34e4b563284ea5d38557c0ff85c04706fc945bc905`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e7dbc7d250abc9822b7e752e47c8b83dd404648d74f9331600b392ac836970`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:b885694442ff65cade16142bde9307eda742f797b4c4e48b95e2ecd62c262746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 KB (105504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:023ebbf730f939171a6dd74509e836130fe404e073174c8b1be5b28fd09e514e`

```dockerfile
```

-	Layers:
	-	`sha256:b18acb410267cb31ce209d09681474ba43f18c2f4af00288845c4061bd220974`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 86.2 KB (86195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48c7d2c81f6bbcf60c7bbca78ec3114f620154531205c592fe14d252cb9daf08`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 19.3 KB (19309 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine3.19`

```console
$ docker pull memcached@sha256:4ee2d6582442b4920f0c9de6565947a81e18abc48089804df10251eedf388d66
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

### `memcached:alpine3.19` - linux; amd64

```console
$ docker pull memcached@sha256:cf854f636d506c0834dc1159ad5b472fea96028e88702014088384915a7c08dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6535198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21047320ccba2e62e0ee66c1ffa169149658e039ee012547c37ed6aa0130ad2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59605d18a5ec7e6531bd08f0238da758082d075c4fdd6a4ec8c00fd6f792425b`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8691b75405b7042ea4a853223cc80432131a0e21745f3baf9b21b00073207ace`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 104.2 KB (104211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8925d4d8379f9d71921da012b62d23d71f826e429777c701a1b0d4d56d0399ac`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 3.0 MB (3020613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86013193f6f292637e997c2518f84ab28fec9d7a494cda4090d07457058f10de`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10cfe77bbca77075d0b682e8546bca4d6d045cfbff0be0336d51b7bbe1116983`  
		Last Modified: Mon, 06 May 2024 23:08:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:d4a846cbc9f47d5db83dbb38f019064556e6af28dad33264b1f851bebbb2858b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ab3ae8df84416fe4351914e6bb061214bfad4b0cb01537aef674b02c008994`

```dockerfile
```

-	Layers:
	-	`sha256:59634fa6bbcc5be09a70b3894761425c9ea7b231a189445bce9ae40b97f09675`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 88.1 KB (88149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2fd487a2e71a464ab83cce092819d041b742e29af0ecb901bcb36ac21fc7c2c`  
		Last Modified: Mon, 06 May 2024 23:08:11 GMT  
		Size: 19.5 KB (19475 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.19` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:8a6f18eb424270a1dca99143a613014d570cb7376c9cb7d212b72d74c569b12a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6381171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8ddcb41c8f4d78c4720e1ad02b3c978ef7af38607d717e52219f0c53ab6fb64`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859f5f148ebb49ed2dfc712d036c8e1162fd5c08307e622f420c9e722f459c15`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a85abddca9696d1381e2dbbf52914e6119f22bd22e71c1ffc49aa385ca2d79`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 120.9 KB (120900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f80774db5f2d9cd2ec4f0bf8e7256768ab2ff5b90e1a822c70e5fb0a8d0a42`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 2.9 MB (2910908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fff6ea9e3e8e56264cef5ba1ceaacc5db1aa37fb687bf4cb684629a462a4e04`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e6b3e687f63ee869e2595d746eecfc9a9a64e49c7972eea118f9af26f3a02f`  
		Last Modified: Mon, 06 May 2024 23:43:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:7677dd609f55b7dac25e997d7fc4942f1b433f1084ca54e71a01175c8608fedb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cce1cbd3428e47f29034986dc018cfef4ed121b030aef195db0d03c8a65cc79d`

```dockerfile
```

-	Layers:
	-	`sha256:c80e817fe71d2bd7ff1d9709ab1ac3d7ac30315b7cfd1b528ca1c316fecabc2f`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 88.2 KB (88168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b568b0dd9cb0ef2428bd10a39e9ee3afe06fe97f6911abc8c1ae5e642b27094`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 19.3 KB (19326 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.19` - linux; 386

```console
$ docker pull memcached@sha256:1557e39ed6b5f943d53c54797d59f4ea27755c53c9e7004cbfb633c08757abd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6194136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d48e3a30b8d39f2e6434ff10c1130366a5bfeac640bc8ecb88f89e6e996cdc4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c853f4fd5c9ee2e18e52b4399ccc43726449928a43d040161f83d3f67f596dd`  
		Last Modified: Mon, 06 May 2024 23:08:35 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca2d91782956c7a9591fd3f9edb724367e6a2770f04a809c6088a8ea623ea7f`  
		Last Modified: Mon, 06 May 2024 23:08:36 GMT  
		Size: 109.3 KB (109328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5c07db0e07d757431d4458ea14990c3cc0b06aa9577b0e29f8db33fc51921b`  
		Last Modified: Mon, 06 May 2024 23:08:36 GMT  
		Size: 2.8 MB (2839076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21633262023f9a6ae09f480b39a8a9a7109a0201b779ccdba90e721204cb20ae`  
		Last Modified: Mon, 06 May 2024 23:08:36 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893c3463887c0e33218f5af72fe7534fe9bebd41fd26e976944bbd03c13a9d22`  
		Last Modified: Mon, 06 May 2024 23:08:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:4184448ad3b3ff9a34654847c26c9ad677ce54b07e8a96eedb429e8c509fe5e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 KB (107524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04225924b78526836b6ef1d8f4bd3d25e994e9f858bedc4d73fbf5308500d074`

```dockerfile
```

-	Layers:
	-	`sha256:562178e7885ee7492a868cc754c309fe7cf0a52b74299dc570dc9959ecfc0c10`  
		Last Modified: Mon, 06 May 2024 23:08:36 GMT  
		Size: 88.1 KB (88104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d1f3d52b695ee750a517e356c17e9f3b6a3778f607f791f558ae9e31397df3f`  
		Last Modified: Mon, 06 May 2024 23:08:35 GMT  
		Size: 19.4 KB (19420 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.19` - linux; ppc64le

```console
$ docker pull memcached@sha256:4b1fdeda480d0b679c2b9fa5a09c508dabaf7bf0bf1600d0078fcae81e004dd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6407037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf112675855fb5780056fbde79f0822c329da1cfb19ca47270289ec2ac966e77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25735f744a453fbf0af2d088f79a0fa6de45cc2699601389d42141b2de2f21d3`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a61320e5e6694b8436a4074ba6280369b9b29e2474231252683fa11606b8e6`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 123.4 KB (123401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e809f0a1acfe802b3158bb0d4d370427885e8c5ba2ce6b98549da9bbac597e`  
		Last Modified: Mon, 06 May 2024 23:39:16 GMT  
		Size: 2.9 MB (2923638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99dc3c24ef4a44c763efcf66a6e3e44d31d723683dd339c343770bd43523007`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0b13828c450ce09acf99d42e4d9e625dbc1991b6f87a5727ff595e3e62a06c`  
		Last Modified: Mon, 06 May 2024 23:39:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:d1dc50ec127cc25ab5b90bbe3fccaf4c5cda1379629dcd1760fa93b6cab32718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 KB (105629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7934a2d41084621a7a7ff3aafbea88a9edfb76ded1149d611483fb61826d661`

```dockerfile
```

-	Layers:
	-	`sha256:dedf3264102cee8df6c9d7e964dedede98ab6b3865d8df8f76e88eeb42290632`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 86.3 KB (86253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b25fbb2f936e2b3483885e59398fdcffdf62a984c55d6171eb02b6a8b6ef44d7`  
		Last Modified: Mon, 06 May 2024 23:39:15 GMT  
		Size: 19.4 KB (19376 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.19` - linux; s390x

```console
$ docker pull memcached@sha256:16979dbfdc08cb52efcfffcdfdff35be32426e49b90065b36155882be545d88b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6151853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cca463729a03d73b6abb17295ed77bc6a13a336b4bc01a3b1c03a176f34fa06`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a6f11688a0fb8016d54f0f889fc4e07b5c17c62112125611f7c620bc7d3f99`  
		Last Modified: Sun, 17 Mar 2024 22:11:54 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a294d63f4311d022fef15282f082670fab839cd31782b0d6e3e8c12044283a`  
		Last Modified: Sun, 17 Mar 2024 22:11:54 GMT  
		Size: 113.1 KB (113140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d6a06c9130de338c39b57baed51f1e62b01cf60bb33a109ac31927ab8c775f`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 2.8 MB (2794432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db042a56f7b2a4ea616aa34e4b563284ea5d38557c0ff85c04706fc945bc905`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e7dbc7d250abc9822b7e752e47c8b83dd404648d74f9331600b392ac836970`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:b885694442ff65cade16142bde9307eda742f797b4c4e48b95e2ecd62c262746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 KB (105504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:023ebbf730f939171a6dd74509e836130fe404e073174c8b1be5b28fd09e514e`

```dockerfile
```

-	Layers:
	-	`sha256:b18acb410267cb31ce209d09681474ba43f18c2f4af00288845c4061bd220974`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 86.2 KB (86195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48c7d2c81f6bbcf60c7bbca78ec3114f620154531205c592fe14d252cb9daf08`  
		Last Modified: Mon, 06 May 2024 23:43:11 GMT  
		Size: 19.3 KB (19309 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:bookworm`

```console
$ docker pull memcached@sha256:1a37ac11adba27f1f29a81b85c6c242f6513d47757f99d2cbca5308fc5a5e0f2
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
$ docker pull memcached@sha256:7e88c146c7393fbcb8c981efcbebc410fe430f7e47593f7c7b19c1864fd8a793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32897352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4274125721ccfb5bf3696e35b8620677e442c1f5885aee1323d244ea4137214`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 May 2024 09:14:35 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Mon, 06 May 2024 09:14:35 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2aa97235084d1e9d96dcd82d59f52808027df2e6bd8df2b984b207c107037d6`  
		Last Modified: Tue, 14 May 2024 02:59:09 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c3eebfc2348c666ba1f14edd94df803c126159dd54a27513273f0c9ff2090b`  
		Last Modified: Tue, 14 May 2024 02:59:10 GMT  
		Size: 2.5 MB (2488483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5520a877f09a00e2d06002be9ff44b80c1044928b980ca9709460a4727ed9da6`  
		Last Modified: Tue, 14 May 2024 02:59:10 GMT  
		Size: 1.3 MB (1256949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe67d33c4a6967ba167fd89d19b671a74e19edb04bbe7ec7d3f4550f55d4569`  
		Last Modified: Tue, 14 May 2024 02:59:10 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450e4b8762758af67b4a485fc7041c56793f6094aa4548f89489e659396a5e35`  
		Last Modified: Tue, 14 May 2024 02:59:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:d8234d3b08b2d3a9b10f5cc7d7e8eeb881e9c71181619c2345871819be563eac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac0e31e9e20cd7d2eb5081055e082080168b1caffa48f1900a5efabb1a24537b`

```dockerfile
```

-	Layers:
	-	`sha256:bccfaa47fb8f608ebb8952b834915de2a6992656e4c56e611a32e8089167dc68`  
		Last Modified: Tue, 14 May 2024 02:59:10 GMT  
		Size: 2.3 MB (2261261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c86e940f075920cebfa2e40582ec611de7bff05d54bb06038bd3c50323add52`  
		Last Modified: Tue, 14 May 2024 02:59:09 GMT  
		Size: 21.1 KB (21146 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:0caa5d2f391d90fc8c56ad5009add403a518055de2115d6fd31e15e14297135c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30237095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:187a7263d807afaef1f10562634f3c06a7096cabb2f319e9ac2e644318303379`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 May 2024 09:14:35 GMT
ADD file:ee9f1914c7fc370bdb089c9e2fcfa15477f7091fc5437cb780232afdf6297586 in / 
# Mon, 06 May 2024 09:14:35 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:169fcae2368e5a601c42972560f091e123648fa0e741975d1b35900c61b9ff71`  
		Last Modified: Tue, 14 May 2024 00:51:36 GMT  
		Size: 26.9 MB (26909921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac2fb1ba5d31602a2c107dc7adc208fd66c3597693d97ca3a1743f80eb34c42`  
		Last Modified: Tue, 14 May 2024 14:50:47 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b482143aab2b97abcc7fe5e07ac0d3b24ac4ee147e8465846ada4f6bc2e4690f`  
		Last Modified: Tue, 14 May 2024 14:50:47 GMT  
		Size: 2.1 MB (2089496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7be0b16f146e3e0539004d2e158b62018843cb744689765fc6cb9048b3ccba3`  
		Last Modified: Tue, 14 May 2024 14:50:48 GMT  
		Size: 1.2 MB (1236170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ca6e022ab5c893f1324b016376e333d0e3af3d4eaf27ef824a8cb1ddb4ae16`  
		Last Modified: Tue, 14 May 2024 14:50:47 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14149cf3cd0dfd764982a3a1cb86460e564857ff4081b31ce6fa220d1271dc4f`  
		Last Modified: Tue, 14 May 2024 14:50:48 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:1846968895df68a70d92115780645a44cf0dff66edba584baff89764b3e902ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2285669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f19cddf29de06aa8a4c98debec36ac562df1f72b08de9c99bb7dcf388eff13ed`

```dockerfile
```

-	Layers:
	-	`sha256:4402e51b44f21e94146beef550d2f20402f932229666cd1bec4f48401cb43742`  
		Last Modified: Tue, 14 May 2024 14:50:47 GMT  
		Size: 2.3 MB (2264549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6f1c335ae222da5a6b0848b8c0960a13c272ccb39a51c22fa05b33276a341f4`  
		Last Modified: Tue, 14 May 2024 14:50:47 GMT  
		Size: 21.1 KB (21120 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:b953ca66ecee777524a0f33f0adefbe99183367e180f4b2ed82d1e525f57d208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32780663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a9c7e97a66ca554c0cfc88de871b1c7dfad7637ffcbd6a79b5c75b3954bb583`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 May 2024 09:14:35 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Mon, 06 May 2024 09:14:35 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994933505bafbbaba95cef494f2dfb3e85f2bfde1ea5c4a6dae5a179e39e7b5c`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9488359f89f8c6691f1737ce76ce6b7520511a8246658953dae9429090e88746`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 2.3 MB (2346183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27fa925bb96d2305b22651dc4d10899309c212aef95cb13afbdeb2ba5436cb0b`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 1.3 MB (1253469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5284a06f3ca2503602cf214d936daf8aedee3d442d7aa66a5b67874c8f156685`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a475f5b1bcd9a980f0e2923bf1af87002c6468529583ce41a151599d11b2cc`  
		Last Modified: Tue, 14 May 2024 17:41:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:303a74af5e224338560198dc50e2c9cb2a7b4a46b01d39144559de1dd7788518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e79fb901bf217f30113856b6b39e296324993066435904abd2a2152baae6156`

```dockerfile
```

-	Layers:
	-	`sha256:a35747f1af90484d4a9021de5c31be89cb3117cb5f56f499d3cebe78562716cf`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 2.3 MB (2261490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c48c7060af35b31db7e804b3ce19451726c3fb6b956edad221ee58000cf04a91`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 21.0 KB (20997 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; 386

```console
$ docker pull memcached@sha256:3f542cc336b40813213949d5eb8e2da1a57005f88566c0d51c3b8624cc911916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33914242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a44cb325942314e83e433868ace554ffea1c0ef303993f238620f928b36bbcf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 May 2024 09:14:35 GMT
ADD file:252f04703c9ed01e5aa32f764c7d751f0a3b17ed9ef1961cd1972aa8453b5cf3 in / 
# Mon, 06 May 2024 09:14:35 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7075ead1c5d56dc11510b76b25c291657dc73ecf7daad5361939429487745b9a`  
		Last Modified: Tue, 14 May 2024 00:51:58 GMT  
		Size: 30.2 MB (30162638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa82d06bb0cba58ed3fae5da8ee9c6248a027c9d105f1c1e2094d1973ab2f78`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf14cdbfbd6ea1d7231b4119cb6c85336718c7ccee9bc57573aadcc210f05e2`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 2.5 MB (2492686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bed32b6d0ec7a40384a2ba4d5fa14871afba5fd572025e99ebc3c30541ee6bf`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 1.3 MB (1257406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07ba6ac3de2271f181cd17c67b57573da49f54d516ad3c852a2610d138c85b3`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a700f395f10bfe9002c02677754b0a58c0ee8ca0f1fc73477ef1b86dc734103b`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:8932028ec9d6cdd607a57df36f524623a045c35db7110aa26040859db5599b8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2279450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:303c5c842506ac0858dd708f266252ee2b586ba9dd6f506ef93e95c9d4d06402`

```dockerfile
```

-	Layers:
	-	`sha256:e55268858bc5b4c5b04534306d270b5c41b3d3dccd563cae845878933e3d7a1c`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 2.3 MB (2258359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4afdfadae6d39596deea4cc7598059a6d7cdd84a4bf4036bfd609cacb9347c22`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 21.1 KB (21091 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:54a6cf440988b85512b266a181d2e83efe8a6a16530029f48b2fd002efb2e251
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38171114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac4ac5a7759abeb1658c052e8e13a0cdc6e05c7af62e12528e0d65428805b7b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 24 Apr 2024 03:14:18 GMT
ADD file:a3e63beab80160854bfc2d48f69e7c70a9542cdfaf3c5b50f1d6248a998b75ae in / 
# Wed, 24 Apr 2024 03:14:22 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:af25825be002e7bdd52bf28c2fbef5bae0ba9fcef8118e5591a874e7a70b2a62`  
		Last Modified: Wed, 24 Apr 2024 03:25:20 GMT  
		Size: 29.1 MB (29144174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70b69867f90cc0cd6ccf8b72f07ee05c80179a59283d6ce971d9191eaf11afe`  
		Last Modified: Mon, 06 May 2024 23:22:55 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361f75ee595f0c436f725a5dd64b1009cb0da358d19361f68345abf27c392f03`  
		Last Modified: Mon, 06 May 2024 23:22:56 GMT  
		Size: 1.9 MB (1937740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1d3e5a5aad136d9ada8e95bd8e9f609baf923df5c9a48a8021e50206e4e93d`  
		Last Modified: Mon, 06 May 2024 23:22:56 GMT  
		Size: 7.1 MB (7087680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913b327051e93299424d31038856dead21e1781ab1e47927437d8d135ea97338`  
		Last Modified: Mon, 06 May 2024 23:22:55 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a025835eff1c0dfdae38dce98ddefd33f8609362934acbc3106f445279e8b050`  
		Last Modified: Mon, 06 May 2024 23:22:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:062ba12de9ac3ea604948fc8045fa1f18254e15045b75fd40ba397ca49ddac94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30f78c9e4c785d57060d12fdc33b3579dde0c50533361c63c38632718921c39d`

```dockerfile
```

-	Layers:
	-	`sha256:0f87aa3b54f1e190b0d04cc9d1960d4d745a6c99015f572091bc1c532c971e12`  
		Last Modified: Mon, 06 May 2024 23:22:55 GMT  
		Size: 20.9 KB (20862 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:430b7d0dd4212933d73484135db4087f520991a9e0d7499435fbf2e530fd6318
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37163910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7e11c36793a0732a32959b3d851daf998f260c7310adb4bd030bc5efd62c057`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 May 2024 09:14:35 GMT
ADD file:1622c3287b5a5c8a6e0b0b0180489212aab2c9bc7b43390b17a5cc8b153e542a in / 
# Mon, 06 May 2024 09:14:35 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:11ee2a6dbc4a6a6b182097f6023f775e595488a6bcc424e9b58001659deb7fa1`  
		Last Modified: Tue, 14 May 2024 01:24:06 GMT  
		Size: 33.1 MB (33141160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7bc98b1678c7602a43450cf1b5a0b7681ae2f5fc3f2798b1efeacf4b6f816e4`  
		Last Modified: Tue, 14 May 2024 13:32:54 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592eb5f8d51b94ab989902437d4d45fa389f90d9e020376265109959475352c8`  
		Last Modified: Tue, 14 May 2024 13:32:54 GMT  
		Size: 2.7 MB (2698407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d506236222bc33a96c083a536e37019eb18cd167ad0488e486fb7efe603856`  
		Last Modified: Tue, 14 May 2024 13:32:54 GMT  
		Size: 1.3 MB (1322831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cff49951e34e6f3a9bbca8596de07eb85450e57e2a99f66b6ce6d36a5cfa049`  
		Last Modified: Tue, 14 May 2024 13:32:55 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f72d6fdca7ec069335903535d097bd12cf1f35395a355b1b4665ab7ed230d4a2`  
		Last Modified: Tue, 14 May 2024 13:32:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:c03fdeb43ec264ab9493846e0ed7373f1e0c4353bdabd3a494684f4c321b8611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2286679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:466a2eec05699dc762f3abe6e741f13a1f0fe96e2fede2cf328da8719620ac85`

```dockerfile
```

-	Layers:
	-	`sha256:cd846922ab00a7afbef577d0a4f869b45fae65daea24ae1fec41855f72bc9b61`  
		Last Modified: Tue, 14 May 2024 13:32:54 GMT  
		Size: 2.3 MB (2265632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5104c8ee9f5261628bf21f17c74ad56f6c43c8a852d215728842b3261b1b3974`  
		Last Modified: Tue, 14 May 2024 13:32:54 GMT  
		Size: 21.0 KB (21047 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:8be2074db9458342fce6c40d6ff648ba9c8671d9210c3bd0dabdb386cdc2c639
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30902718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fb8c642e3831e983cd5e8acdee53cd1b4a2f633ffd89c297f50d80745daafa1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 May 2024 09:14:35 GMT
ADD file:55fef93bbad6701fe968a070a0c72b3a0bd3df408dd79c9a616a43dea0de11d0 in / 
# Mon, 06 May 2024 09:14:35 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d7365433874e83ccc92aa5d768989641a64e23c3247409161401a09b4895c406`  
		Last Modified: Tue, 14 May 2024 00:47:35 GMT  
		Size: 27.5 MB (27512398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f6e2c8c427b6988b152cb191a15a2716bbf2dff9f9a6eafebf06f081eebf7b5`  
		Last Modified: Tue, 14 May 2024 17:56:21 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e6d59bd3a243d0242de493c532d8d56b279f05bb1a3d7c58724ea30a716fcf`  
		Last Modified: Tue, 14 May 2024 17:56:21 GMT  
		Size: 2.2 MB (2152659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da6ae628a520dec07948d68ad410a007894a6f040c7305dd8c4628501f77d49`  
		Last Modified: Tue, 14 May 2024 17:56:21 GMT  
		Size: 1.2 MB (1236148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb27d713cf158e879ff43c810aa223cb411f904673225d1d31f1bb782c01cb2`  
		Last Modified: Tue, 14 May 2024 17:56:21 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a400d87b577ef1da8cde4dc345372dd8e53b0d2a3c0e49aa4771038101183470`  
		Last Modified: Tue, 14 May 2024 17:56:22 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:b400e46dab61c1e9270120428db66b57ee83545f05b9bf07b59489dde48c10eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0dcf8c510ed87cdfbca560a9fa5173caed7b13966e9ddbf6a1fbaf8203265d4`

```dockerfile
```

-	Layers:
	-	`sha256:c437e8e5e7b32562cd1a77d98c41ff5a5bcf8c18102d8304295fe16c0342e460`  
		Last Modified: Tue, 14 May 2024 17:56:21 GMT  
		Size: 2.3 MB (2261082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ae942851d074d6a0dd2bdcb21bd9e83ec34c7bfd585ffd21811c317eb715284`  
		Last Modified: Tue, 14 May 2024 17:56:21 GMT  
		Size: 21.0 KB (20979 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:latest`

```console
$ docker pull memcached@sha256:1a37ac11adba27f1f29a81b85c6c242f6513d47757f99d2cbca5308fc5a5e0f2
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
$ docker pull memcached@sha256:7e88c146c7393fbcb8c981efcbebc410fe430f7e47593f7c7b19c1864fd8a793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32897352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4274125721ccfb5bf3696e35b8620677e442c1f5885aee1323d244ea4137214`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 May 2024 09:14:35 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Mon, 06 May 2024 09:14:35 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2aa97235084d1e9d96dcd82d59f52808027df2e6bd8df2b984b207c107037d6`  
		Last Modified: Tue, 14 May 2024 02:59:09 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c3eebfc2348c666ba1f14edd94df803c126159dd54a27513273f0c9ff2090b`  
		Last Modified: Tue, 14 May 2024 02:59:10 GMT  
		Size: 2.5 MB (2488483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5520a877f09a00e2d06002be9ff44b80c1044928b980ca9709460a4727ed9da6`  
		Last Modified: Tue, 14 May 2024 02:59:10 GMT  
		Size: 1.3 MB (1256949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe67d33c4a6967ba167fd89d19b671a74e19edb04bbe7ec7d3f4550f55d4569`  
		Last Modified: Tue, 14 May 2024 02:59:10 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450e4b8762758af67b4a485fc7041c56793f6094aa4548f89489e659396a5e35`  
		Last Modified: Tue, 14 May 2024 02:59:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:d8234d3b08b2d3a9b10f5cc7d7e8eeb881e9c71181619c2345871819be563eac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac0e31e9e20cd7d2eb5081055e082080168b1caffa48f1900a5efabb1a24537b`

```dockerfile
```

-	Layers:
	-	`sha256:bccfaa47fb8f608ebb8952b834915de2a6992656e4c56e611a32e8089167dc68`  
		Last Modified: Tue, 14 May 2024 02:59:10 GMT  
		Size: 2.3 MB (2261261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c86e940f075920cebfa2e40582ec611de7bff05d54bb06038bd3c50323add52`  
		Last Modified: Tue, 14 May 2024 02:59:09 GMT  
		Size: 21.1 KB (21146 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm variant v5

```console
$ docker pull memcached@sha256:0caa5d2f391d90fc8c56ad5009add403a518055de2115d6fd31e15e14297135c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30237095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:187a7263d807afaef1f10562634f3c06a7096cabb2f319e9ac2e644318303379`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 May 2024 09:14:35 GMT
ADD file:ee9f1914c7fc370bdb089c9e2fcfa15477f7091fc5437cb780232afdf6297586 in / 
# Mon, 06 May 2024 09:14:35 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:169fcae2368e5a601c42972560f091e123648fa0e741975d1b35900c61b9ff71`  
		Last Modified: Tue, 14 May 2024 00:51:36 GMT  
		Size: 26.9 MB (26909921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac2fb1ba5d31602a2c107dc7adc208fd66c3597693d97ca3a1743f80eb34c42`  
		Last Modified: Tue, 14 May 2024 14:50:47 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b482143aab2b97abcc7fe5e07ac0d3b24ac4ee147e8465846ada4f6bc2e4690f`  
		Last Modified: Tue, 14 May 2024 14:50:47 GMT  
		Size: 2.1 MB (2089496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7be0b16f146e3e0539004d2e158b62018843cb744689765fc6cb9048b3ccba3`  
		Last Modified: Tue, 14 May 2024 14:50:48 GMT  
		Size: 1.2 MB (1236170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ca6e022ab5c893f1324b016376e333d0e3af3d4eaf27ef824a8cb1ddb4ae16`  
		Last Modified: Tue, 14 May 2024 14:50:47 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14149cf3cd0dfd764982a3a1cb86460e564857ff4081b31ce6fa220d1271dc4f`  
		Last Modified: Tue, 14 May 2024 14:50:48 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:1846968895df68a70d92115780645a44cf0dff66edba584baff89764b3e902ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2285669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f19cddf29de06aa8a4c98debec36ac562df1f72b08de9c99bb7dcf388eff13ed`

```dockerfile
```

-	Layers:
	-	`sha256:4402e51b44f21e94146beef550d2f20402f932229666cd1bec4f48401cb43742`  
		Last Modified: Tue, 14 May 2024 14:50:47 GMT  
		Size: 2.3 MB (2264549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6f1c335ae222da5a6b0848b8c0960a13c272ccb39a51c22fa05b33276a341f4`  
		Last Modified: Tue, 14 May 2024 14:50:47 GMT  
		Size: 21.1 KB (21120 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:b953ca66ecee777524a0f33f0adefbe99183367e180f4b2ed82d1e525f57d208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32780663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a9c7e97a66ca554c0cfc88de871b1c7dfad7637ffcbd6a79b5c75b3954bb583`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 May 2024 09:14:35 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Mon, 06 May 2024 09:14:35 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994933505bafbbaba95cef494f2dfb3e85f2bfde1ea5c4a6dae5a179e39e7b5c`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9488359f89f8c6691f1737ce76ce6b7520511a8246658953dae9429090e88746`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 2.3 MB (2346183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27fa925bb96d2305b22651dc4d10899309c212aef95cb13afbdeb2ba5436cb0b`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 1.3 MB (1253469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5284a06f3ca2503602cf214d936daf8aedee3d442d7aa66a5b67874c8f156685`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a475f5b1bcd9a980f0e2923bf1af87002c6468529583ce41a151599d11b2cc`  
		Last Modified: Tue, 14 May 2024 17:41:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:303a74af5e224338560198dc50e2c9cb2a7b4a46b01d39144559de1dd7788518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e79fb901bf217f30113856b6b39e296324993066435904abd2a2152baae6156`

```dockerfile
```

-	Layers:
	-	`sha256:a35747f1af90484d4a9021de5c31be89cb3117cb5f56f499d3cebe78562716cf`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 2.3 MB (2261490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c48c7060af35b31db7e804b3ce19451726c3fb6b956edad221ee58000cf04a91`  
		Last Modified: Tue, 14 May 2024 17:41:03 GMT  
		Size: 21.0 KB (20997 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; 386

```console
$ docker pull memcached@sha256:3f542cc336b40813213949d5eb8e2da1a57005f88566c0d51c3b8624cc911916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33914242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a44cb325942314e83e433868ace554ffea1c0ef303993f238620f928b36bbcf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 May 2024 09:14:35 GMT
ADD file:252f04703c9ed01e5aa32f764c7d751f0a3b17ed9ef1961cd1972aa8453b5cf3 in / 
# Mon, 06 May 2024 09:14:35 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7075ead1c5d56dc11510b76b25c291657dc73ecf7daad5361939429487745b9a`  
		Last Modified: Tue, 14 May 2024 00:51:58 GMT  
		Size: 30.2 MB (30162638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa82d06bb0cba58ed3fae5da8ee9c6248a027c9d105f1c1e2094d1973ab2f78`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf14cdbfbd6ea1d7231b4119cb6c85336718c7ccee9bc57573aadcc210f05e2`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 2.5 MB (2492686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bed32b6d0ec7a40384a2ba4d5fa14871afba5fd572025e99ebc3c30541ee6bf`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 1.3 MB (1257406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07ba6ac3de2271f181cd17c67b57573da49f54d516ad3c852a2610d138c85b3`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a700f395f10bfe9002c02677754b0a58c0ee8ca0f1fc73477ef1b86dc734103b`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:8932028ec9d6cdd607a57df36f524623a045c35db7110aa26040859db5599b8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2279450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:303c5c842506ac0858dd708f266252ee2b586ba9dd6f506ef93e95c9d4d06402`

```dockerfile
```

-	Layers:
	-	`sha256:e55268858bc5b4c5b04534306d270b5c41b3d3dccd563cae845878933e3d7a1c`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 2.3 MB (2258359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4afdfadae6d39596deea4cc7598059a6d7cdd84a4bf4036bfd609cacb9347c22`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 21.1 KB (21091 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; mips64le

```console
$ docker pull memcached@sha256:54a6cf440988b85512b266a181d2e83efe8a6a16530029f48b2fd002efb2e251
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38171114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac4ac5a7759abeb1658c052e8e13a0cdc6e05c7af62e12528e0d65428805b7b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 24 Apr 2024 03:14:18 GMT
ADD file:a3e63beab80160854bfc2d48f69e7c70a9542cdfaf3c5b50f1d6248a998b75ae in / 
# Wed, 24 Apr 2024 03:14:22 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:af25825be002e7bdd52bf28c2fbef5bae0ba9fcef8118e5591a874e7a70b2a62`  
		Last Modified: Wed, 24 Apr 2024 03:25:20 GMT  
		Size: 29.1 MB (29144174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70b69867f90cc0cd6ccf8b72f07ee05c80179a59283d6ce971d9191eaf11afe`  
		Last Modified: Mon, 06 May 2024 23:22:55 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361f75ee595f0c436f725a5dd64b1009cb0da358d19361f68345abf27c392f03`  
		Last Modified: Mon, 06 May 2024 23:22:56 GMT  
		Size: 1.9 MB (1937740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1d3e5a5aad136d9ada8e95bd8e9f609baf923df5c9a48a8021e50206e4e93d`  
		Last Modified: Mon, 06 May 2024 23:22:56 GMT  
		Size: 7.1 MB (7087680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913b327051e93299424d31038856dead21e1781ab1e47927437d8d135ea97338`  
		Last Modified: Mon, 06 May 2024 23:22:55 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a025835eff1c0dfdae38dce98ddefd33f8609362934acbc3106f445279e8b050`  
		Last Modified: Mon, 06 May 2024 23:22:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:062ba12de9ac3ea604948fc8045fa1f18254e15045b75fd40ba397ca49ddac94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30f78c9e4c785d57060d12fdc33b3579dde0c50533361c63c38632718921c39d`

```dockerfile
```

-	Layers:
	-	`sha256:0f87aa3b54f1e190b0d04cc9d1960d4d745a6c99015f572091bc1c532c971e12`  
		Last Modified: Mon, 06 May 2024 23:22:55 GMT  
		Size: 20.9 KB (20862 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; ppc64le

```console
$ docker pull memcached@sha256:430b7d0dd4212933d73484135db4087f520991a9e0d7499435fbf2e530fd6318
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37163910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7e11c36793a0732a32959b3d851daf998f260c7310adb4bd030bc5efd62c057`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 May 2024 09:14:35 GMT
ADD file:1622c3287b5a5c8a6e0b0b0180489212aab2c9bc7b43390b17a5cc8b153e542a in / 
# Mon, 06 May 2024 09:14:35 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:11ee2a6dbc4a6a6b182097f6023f775e595488a6bcc424e9b58001659deb7fa1`  
		Last Modified: Tue, 14 May 2024 01:24:06 GMT  
		Size: 33.1 MB (33141160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7bc98b1678c7602a43450cf1b5a0b7681ae2f5fc3f2798b1efeacf4b6f816e4`  
		Last Modified: Tue, 14 May 2024 13:32:54 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592eb5f8d51b94ab989902437d4d45fa389f90d9e020376265109959475352c8`  
		Last Modified: Tue, 14 May 2024 13:32:54 GMT  
		Size: 2.7 MB (2698407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d506236222bc33a96c083a536e37019eb18cd167ad0488e486fb7efe603856`  
		Last Modified: Tue, 14 May 2024 13:32:54 GMT  
		Size: 1.3 MB (1322831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cff49951e34e6f3a9bbca8596de07eb85450e57e2a99f66b6ce6d36a5cfa049`  
		Last Modified: Tue, 14 May 2024 13:32:55 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f72d6fdca7ec069335903535d097bd12cf1f35395a355b1b4665ab7ed230d4a2`  
		Last Modified: Tue, 14 May 2024 13:32:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:c03fdeb43ec264ab9493846e0ed7373f1e0c4353bdabd3a494684f4c321b8611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2286679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:466a2eec05699dc762f3abe6e741f13a1f0fe96e2fede2cf328da8719620ac85`

```dockerfile
```

-	Layers:
	-	`sha256:cd846922ab00a7afbef577d0a4f869b45fae65daea24ae1fec41855f72bc9b61`  
		Last Modified: Tue, 14 May 2024 13:32:54 GMT  
		Size: 2.3 MB (2265632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5104c8ee9f5261628bf21f17c74ad56f6c43c8a852d215728842b3261b1b3974`  
		Last Modified: Tue, 14 May 2024 13:32:54 GMT  
		Size: 21.0 KB (21047 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; s390x

```console
$ docker pull memcached@sha256:8be2074db9458342fce6c40d6ff648ba9c8671d9210c3bd0dabdb386cdc2c639
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30902718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fb8c642e3831e983cd5e8acdee53cd1b4a2f633ffd89c297f50d80745daafa1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 May 2024 09:14:35 GMT
ADD file:55fef93bbad6701fe968a070a0c72b3a0bd3df408dd79c9a616a43dea0de11d0 in / 
# Mon, 06 May 2024 09:14:35 GMT
CMD ["bash"]
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_VERSION=1.6.27
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Mon, 06 May 2024 09:14:35 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Mon, 06 May 2024 09:14:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 06 May 2024 09:14:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 May 2024 09:14:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 06 May 2024 09:14:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 May 2024 09:14:35 GMT
USER memcache
# Mon, 06 May 2024 09:14:35 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 06 May 2024 09:14:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d7365433874e83ccc92aa5d768989641a64e23c3247409161401a09b4895c406`  
		Last Modified: Tue, 14 May 2024 00:47:35 GMT  
		Size: 27.5 MB (27512398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f6e2c8c427b6988b152cb191a15a2716bbf2dff9f9a6eafebf06f081eebf7b5`  
		Last Modified: Tue, 14 May 2024 17:56:21 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e6d59bd3a243d0242de493c532d8d56b279f05bb1a3d7c58724ea30a716fcf`  
		Last Modified: Tue, 14 May 2024 17:56:21 GMT  
		Size: 2.2 MB (2152659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da6ae628a520dec07948d68ad410a007894a6f040c7305dd8c4628501f77d49`  
		Last Modified: Tue, 14 May 2024 17:56:21 GMT  
		Size: 1.2 MB (1236148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb27d713cf158e879ff43c810aa223cb411f904673225d1d31f1bb782c01cb2`  
		Last Modified: Tue, 14 May 2024 17:56:21 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a400d87b577ef1da8cde4dc345372dd8e53b0d2a3c0e49aa4771038101183470`  
		Last Modified: Tue, 14 May 2024 17:56:22 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:b400e46dab61c1e9270120428db66b57ee83545f05b9bf07b59489dde48c10eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0dcf8c510ed87cdfbca560a9fa5173caed7b13966e9ddbf6a1fbaf8203265d4`

```dockerfile
```

-	Layers:
	-	`sha256:c437e8e5e7b32562cd1a77d98c41ff5a5bcf8c18102d8304295fe16c0342e460`  
		Last Modified: Tue, 14 May 2024 17:56:21 GMT  
		Size: 2.3 MB (2261082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ae942851d074d6a0dd2bdcb21bd9e83ec34c7bfd585ffd21811c317eb715284`  
		Last Modified: Tue, 14 May 2024 17:56:21 GMT  
		Size: 21.0 KB (20979 bytes)  
		MIME: application/vnd.in-toto+json
