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
-	[`memcached:1.6.28`](#memcached1628)
-	[`memcached:1.6.28-alpine`](#memcached1628-alpine)
-	[`memcached:1.6.28-alpine3.20`](#memcached1628-alpine320)
-	[`memcached:1.6.28-bookworm`](#memcached1628-bookworm)
-	[`memcached:alpine`](#memcachedalpine)
-	[`memcached:alpine3.20`](#memcachedalpine320)
-	[`memcached:bookworm`](#memcachedbookworm)
-	[`memcached:latest`](#memcachedlatest)

## `memcached:1`

```console
$ docker pull memcached@sha256:58225aeaf238b8d6ca5b0c7cfc7cb81f44cdebd1ca184f032478cf4470c89520
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
$ docker pull memcached@sha256:3a548271d024b9f019806f9c57ab0c78b12721b99161b37c5fa1a54871aa4f1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32335604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58e4157cda75177132acadaa737dcc4ffbf23b3f4821d0948b4f9b882e606d2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 May 2024 09:14:35 GMT
ADD file:a92da94a28279478b2eae11dcdcd2913fc06af02498a5515cc3f288668d74e43 in / 
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
	-	`sha256:6ccc6628d3cdcda935b3b60cb54fa578d669965454d9cf39de3df9c1276132b7`  
		Last Modified: Tue, 14 May 2024 01:22:19 GMT  
		Size: 29.1 MB (29143688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ee82bdcb1e3a635fe9f1d5352d366d13d345f09eb3adfca8c9cdac667f12d4`  
		Last Modified: Tue, 14 May 2024 21:39:45 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6772b6152d32070d1bd037b4d40168112ccbe96e562d2b44c4be24a5f01f9b`  
		Last Modified: Tue, 14 May 2024 21:39:45 GMT  
		Size: 1.9 MB (1937746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833a7d6af8137233d7ad16026d9b1e1439a875762d4d0300c5b8fad018adba6b`  
		Last Modified: Tue, 14 May 2024 21:39:45 GMT  
		Size: 1.3 MB (1252656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdcc9953d5a8982f1bda95e99618eb60ce77f306601a4bd87e2b7032f58158fd`  
		Last Modified: Tue, 14 May 2024 21:39:45 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90055ed64046ecc2a6b606da0a99148b1b1006371fb88ea34d8116628aae47f3`  
		Last Modified: Tue, 14 May 2024 21:39:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:f17b6790b9c5b13d08059746553cd24795e4578c706cccada105ade01f3e16b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f05a4b82f72ff2643271e6710a1abb766fe5fbc715a018cabf4045f9cb137aa8`

```dockerfile
```

-	Layers:
	-	`sha256:57f1868b984b0196002a8a186c5ac8833f8eee2db97961c5355b4da6684b0fa4`  
		Last Modified: Tue, 14 May 2024 21:39:45 GMT  
		Size: 20.9 KB (20861 bytes)  
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
$ docker pull memcached@sha256:b7474699be8a7cee225d1b7e4eef893d75bb92b7c6f5aae74ca9e4e95883ba96
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
$ docker pull memcached@sha256:5db13a42799b2fad49009ca0a76d26a2e05a662b5e9fefc080c5212a475e4a91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4680929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cef3a92c10bad723df3e5f47c23c6ab348ad3dc66c78bff564de8be3abb5642b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_VERSION=1.6.27
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 22 May 2024 18:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 18:54:12 GMT
USER memcache
# Wed, 22 May 2024 18:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 May 2024 18:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342a61fd751d022d1e9c72ba1b21e59935adbd6cb70b898d3cc459c0c0fda6a2`  
		Last Modified: Wed, 22 May 2024 22:58:40 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79489751750523d635370701c07fd1c88082d79215033bd9ca22d0255b48d1a1`  
		Last Modified: Wed, 22 May 2024 22:58:41 GMT  
		Size: 103.8 KB (103819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d972318261d7575d3f661b9dee0c0e0b42b4d1a480b0fbd7cb7d46f9fcc4eeb`  
		Last Modified: Wed, 22 May 2024 22:58:41 GMT  
		Size: 953.6 KB (953649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e73ab9b1403e8e6831efae93c083646a1856d194bac2dbddebfd33ec9bde5a1`  
		Last Modified: Wed, 22 May 2024 22:58:41 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fde407aeac5e16df26055d7ac8c318c420bcabb2a4ac507140f2db121ba8b8f0`  
		Last Modified: Wed, 22 May 2024 22:58:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:5635e12850ad272fd2d1fdd231445e5c65b60313a7674618a79804217102bbc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.7 KB (103735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f91d07fc259e406e39ccba78a20068801cbc6910b2ec70a3455899f993fb503c`

```dockerfile
```

-	Layers:
	-	`sha256:1ab3c7ccb18461e449a08496b5f2e0a26f8d2ab5f85e9ee0f5ce295fdf9611bc`  
		Last Modified: Wed, 22 May 2024 22:58:41 GMT  
		Size: 84.3 KB (84268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b7927aaa969cbae3829d94e66bdd3a7f141c6524b4deb74397a7ad6d6695ca6`  
		Last Modified: Wed, 22 May 2024 22:58:40 GMT  
		Size: 19.5 KB (19467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:e0688d9873a4cf749f89b43548d03f7d6c873596b1495b6da6943d4a3e767df1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5166898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6a1a46a5867d6ecd3c9bf99a695a89cc1f746f59d3a9a140b85a42b99a2e26`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_VERSION=1.6.27
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 22 May 2024 18:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 18:54:12 GMT
USER memcache
# Wed, 22 May 2024 18:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 May 2024 18:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024a9ccd1af8ffcfe453e22adead9362703e916c9dec4f1d4e94b597e660f23e`  
		Last Modified: Thu, 23 May 2024 06:29:57 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab592fa6ce63bf6772b1c208275d773ef6e671af73b2bd119e98de86dce4fc1`  
		Last Modified: Thu, 23 May 2024 06:29:58 GMT  
		Size: 121.0 KB (121017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd20d288c43aabf4d5e06a885b2e2f24583aae8e102eca2bf9257ce5e307a2cd`  
		Last Modified: Thu, 23 May 2024 06:29:57 GMT  
		Size: 957.7 KB (957743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d039a0fcb8c2c4f062cb3fb5c2b20ae16915479721254aadfc68d0319c84ee25`  
		Last Modified: Thu, 23 May 2024 06:29:57 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12cf5bc5246a4e40149d2a6b161c9fbce8354373e305c03088715546070c2742`  
		Last Modified: Thu, 23 May 2024 06:29:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:ec1932014529a81f308cae2db47073ddf344ef48cbc77766d95510cb7385b2af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 KB (103606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f0d85c8cad5520d9245c1563457fcf55da9b744f736c305ad21fad10027e013`

```dockerfile
```

-	Layers:
	-	`sha256:f77bdac9710cd22ef4eb7ba293b1b4fe4736e109a3767950432991fe0237fa54`  
		Last Modified: Thu, 23 May 2024 06:29:57 GMT  
		Size: 84.3 KB (84287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12016cd6764c2821a23d0e8fb3c182eda4d12d096e83cf52f57eb0103616d5e8`  
		Last Modified: Thu, 23 May 2024 06:29:57 GMT  
		Size: 19.3 KB (19319 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; 386

```console
$ docker pull memcached@sha256:95b69b6853d1e7b707eeacfd443723ac67c1a07a4d3adfaf8d639c8d26e864a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4524678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:924c2a8b8733b2b922abaabf6edf609336f035c3ee2158ec9daee20648f41f80`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:05:50 GMT
ADD file:6a4a5e48a600b064b83b954a55f1ddd3352780d69a6fb0ad816258011f5a3e47 in / 
# Wed, 22 May 2024 18:05:51 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_VERSION=1.6.27
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 22 May 2024 18:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 18:54:12 GMT
USER memcache
# Wed, 22 May 2024 18:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 May 2024 18:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:271acb68d2933b32dac564003959c5aea6d5d436c2779e253600ab35d7745465`  
		Last Modified: Wed, 22 May 2024 18:06:11 GMT  
		Size: 3.5 MB (3467181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c828318950f314a45b930bb2ecce44606839c736b30e5a536da98c623b8d299`  
		Last Modified: Wed, 22 May 2024 22:58:55 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13470cb0fe3b718059121f9e336d8a39c7c6501b74223ef6341256658e1bcace`  
		Last Modified: Wed, 22 May 2024 22:58:56 GMT  
		Size: 109.0 KB (108952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb71cb4f8348194cc15fc03b348a7627488d870e97825c6b90943b0ae338cf78`  
		Last Modified: Wed, 22 May 2024 22:58:56 GMT  
		Size: 947.2 KB (947179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf76962900461e1b3abb72f20d20631d3b25499cb012ab300ff1821376388957`  
		Last Modified: Wed, 22 May 2024 22:58:56 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08e50381e18fbb7d44b8873051260c894b923dd7c0f3d5991ecdf29adce92b4f`  
		Last Modified: Wed, 22 May 2024 22:58:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:01c1aa4e15267a5d1ef8e1cce888ba1771e62572694e66e5325091d9462e97fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 KB (103635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08a7c8c3c66f6209ec1c9f32c410d4b36b45c40a9666ac58a1065cb5c5fa7d55`

```dockerfile
```

-	Layers:
	-	`sha256:3988b31dcd280e09051b45d43e2292273ee750d0802ae268cddfc6223b0e2d32`  
		Last Modified: Wed, 22 May 2024 22:58:56 GMT  
		Size: 84.2 KB (84223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:792ae2253532accb256a734c25cb5e4e8dc47177df82f43084a73db1d2e3a5d9`  
		Last Modified: Wed, 22 May 2024 22:58:56 GMT  
		Size: 19.4 KB (19412 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:1cbe62d07f4a083cb5b5cb21eecf18f2c0662afda48b072a76d0711587b2a09c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4686554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ecef3bdf44124caa92d058e30ea98781387381719c49ea7dc28ae38302902f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:07:11 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_VERSION=1.6.27
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 22 May 2024 18:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 18:54:12 GMT
USER memcache
# Wed, 22 May 2024 18:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 May 2024 18:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea342fb939ae41c1145ee79234693ad7df9dba58d9a9d9ebb09071eec9886537`  
		Last Modified: Tue, 28 May 2024 23:38:45 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64a76d46c4c3cea865876670b86a10ceb59f479311d77bf613b1b301d97da3a`  
		Last Modified: Tue, 28 May 2024 23:38:46 GMT  
		Size: 123.0 KB (123006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca4b665cc9f3db507ee1264e940f8374dc3e014aefd2e5a46a9e6749f128a1d9`  
		Last Modified: Tue, 28 May 2024 23:38:46 GMT  
		Size: 992.3 KB (992335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da628c50da1874ce9bde8045dd3fbb7afc353942007abfb9a2e46ea34da235f6`  
		Last Modified: Tue, 28 May 2024 23:38:46 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bfe485c630c4e7e38f4195c2e2d6a35389a292c8a06f3f81e8ea6980a90daa5`  
		Last Modified: Tue, 28 May 2024 23:38:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:79bb7f48dd6a74241c1c606814efbe97139b8292c820acdb3f45ebf69cb029ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 KB (101741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c5ebac83e5929edb9713461ef04850f38b12eaef76efc9e139bd4e38922bc72`

```dockerfile
```

-	Layers:
	-	`sha256:51f7cf389b1f2aae558b2e6058899d13c84befb3bf2ab9932efce3a99495f2e3`  
		Last Modified: Tue, 28 May 2024 23:38:45 GMT  
		Size: 82.4 KB (82372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d3233692d06b58a5c2a997b62411dd2922e73826a8330abba28784bbfde1742`  
		Last Modified: Tue, 28 May 2024 23:38:45 GMT  
		Size: 19.4 KB (19369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:43ea726a69d7aa19d38600a6b0c98114eac30a3f70d46c14f55746d508773378
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4551268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4218baf28d875e94ee50ce255b26888caf5671d153bb189ac30bebcc6635843b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_VERSION=1.6.27
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 22 May 2024 18:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 18:54:12 GMT
USER memcache
# Wed, 22 May 2024 18:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 May 2024 18:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bda8f56f465ce0440892acfd910a54a797991e554b31b96388ad100cb8dd18c`  
		Last Modified: Thu, 23 May 2024 03:19:15 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9810404860e30f64bc35f99f5cc930c953fa654ed2da190a4f4adf46c3914ea`  
		Last Modified: Thu, 23 May 2024 03:19:15 GMT  
		Size: 112.7 KB (112736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436abf7c43bfae37e20b0ae2fdaafa8c0165c2bbfcfd1242cd0ed17c846fdda4`  
		Last Modified: Thu, 23 May 2024 03:19:15 GMT  
		Size: 976.8 KB (976829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a62044b74bd7a363ba1ebba030952851d221ab43ab666a8bd59960ca5c76e9`  
		Last Modified: Thu, 23 May 2024 03:19:15 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc10b1e30c81f41f9d4012eda90ae84cfd53312c55770b504774fe80b5ba3ce`  
		Last Modified: Thu, 23 May 2024 03:19:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:5d3ab77f58725536e38b01d6e4bd4532e7bfa6cf7bd9eac35e77a4b70c8b8402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.6 KB (101615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd8bbbe1c27095d48770c6007e70e45c80a7c382286aaababe2fc83010d5fdda`

```dockerfile
```

-	Layers:
	-	`sha256:ea5bb003c385255e2e282399fe22ce79290bf682bb186d9a3901082902cc5d57`  
		Last Modified: Thu, 23 May 2024 03:19:15 GMT  
		Size: 82.3 KB (82314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb3910214e4a01e12528ebb507acafe782392af9209e1928be56b58e352cf7e1`  
		Last Modified: Thu, 23 May 2024 03:19:15 GMT  
		Size: 19.3 KB (19301 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine3.20`

```console
$ docker pull memcached@sha256:b7474699be8a7cee225d1b7e4eef893d75bb92b7c6f5aae74ca9e4e95883ba96
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

### `memcached:1-alpine3.20` - linux; amd64

```console
$ docker pull memcached@sha256:5db13a42799b2fad49009ca0a76d26a2e05a662b5e9fefc080c5212a475e4a91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4680929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cef3a92c10bad723df3e5f47c23c6ab348ad3dc66c78bff564de8be3abb5642b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_VERSION=1.6.27
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 22 May 2024 18:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 18:54:12 GMT
USER memcache
# Wed, 22 May 2024 18:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 May 2024 18:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342a61fd751d022d1e9c72ba1b21e59935adbd6cb70b898d3cc459c0c0fda6a2`  
		Last Modified: Wed, 22 May 2024 22:58:40 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79489751750523d635370701c07fd1c88082d79215033bd9ca22d0255b48d1a1`  
		Last Modified: Wed, 22 May 2024 22:58:41 GMT  
		Size: 103.8 KB (103819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d972318261d7575d3f661b9dee0c0e0b42b4d1a480b0fbd7cb7d46f9fcc4eeb`  
		Last Modified: Wed, 22 May 2024 22:58:41 GMT  
		Size: 953.6 KB (953649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e73ab9b1403e8e6831efae93c083646a1856d194bac2dbddebfd33ec9bde5a1`  
		Last Modified: Wed, 22 May 2024 22:58:41 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fde407aeac5e16df26055d7ac8c318c420bcabb2a4ac507140f2db121ba8b8f0`  
		Last Modified: Wed, 22 May 2024 22:58:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:5635e12850ad272fd2d1fdd231445e5c65b60313a7674618a79804217102bbc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.7 KB (103735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f91d07fc259e406e39ccba78a20068801cbc6910b2ec70a3455899f993fb503c`

```dockerfile
```

-	Layers:
	-	`sha256:1ab3c7ccb18461e449a08496b5f2e0a26f8d2ab5f85e9ee0f5ce295fdf9611bc`  
		Last Modified: Wed, 22 May 2024 22:58:41 GMT  
		Size: 84.3 KB (84268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b7927aaa969cbae3829d94e66bdd3a7f141c6524b4deb74397a7ad6d6695ca6`  
		Last Modified: Wed, 22 May 2024 22:58:40 GMT  
		Size: 19.5 KB (19467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:e0688d9873a4cf749f89b43548d03f7d6c873596b1495b6da6943d4a3e767df1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5166898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6a1a46a5867d6ecd3c9bf99a695a89cc1f746f59d3a9a140b85a42b99a2e26`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_VERSION=1.6.27
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 22 May 2024 18:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 18:54:12 GMT
USER memcache
# Wed, 22 May 2024 18:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 May 2024 18:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024a9ccd1af8ffcfe453e22adead9362703e916c9dec4f1d4e94b597e660f23e`  
		Last Modified: Thu, 23 May 2024 06:29:57 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab592fa6ce63bf6772b1c208275d773ef6e671af73b2bd119e98de86dce4fc1`  
		Last Modified: Thu, 23 May 2024 06:29:58 GMT  
		Size: 121.0 KB (121017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd20d288c43aabf4d5e06a885b2e2f24583aae8e102eca2bf9257ce5e307a2cd`  
		Last Modified: Thu, 23 May 2024 06:29:57 GMT  
		Size: 957.7 KB (957743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d039a0fcb8c2c4f062cb3fb5c2b20ae16915479721254aadfc68d0319c84ee25`  
		Last Modified: Thu, 23 May 2024 06:29:57 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12cf5bc5246a4e40149d2a6b161c9fbce8354373e305c03088715546070c2742`  
		Last Modified: Thu, 23 May 2024 06:29:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:ec1932014529a81f308cae2db47073ddf344ef48cbc77766d95510cb7385b2af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 KB (103606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f0d85c8cad5520d9245c1563457fcf55da9b744f736c305ad21fad10027e013`

```dockerfile
```

-	Layers:
	-	`sha256:f77bdac9710cd22ef4eb7ba293b1b4fe4736e109a3767950432991fe0237fa54`  
		Last Modified: Thu, 23 May 2024 06:29:57 GMT  
		Size: 84.3 KB (84287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12016cd6764c2821a23d0e8fb3c182eda4d12d096e83cf52f57eb0103616d5e8`  
		Last Modified: Thu, 23 May 2024 06:29:57 GMT  
		Size: 19.3 KB (19319 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.20` - linux; 386

```console
$ docker pull memcached@sha256:95b69b6853d1e7b707eeacfd443723ac67c1a07a4d3adfaf8d639c8d26e864a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4524678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:924c2a8b8733b2b922abaabf6edf609336f035c3ee2158ec9daee20648f41f80`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:05:50 GMT
ADD file:6a4a5e48a600b064b83b954a55f1ddd3352780d69a6fb0ad816258011f5a3e47 in / 
# Wed, 22 May 2024 18:05:51 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_VERSION=1.6.27
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 22 May 2024 18:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 18:54:12 GMT
USER memcache
# Wed, 22 May 2024 18:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 May 2024 18:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:271acb68d2933b32dac564003959c5aea6d5d436c2779e253600ab35d7745465`  
		Last Modified: Wed, 22 May 2024 18:06:11 GMT  
		Size: 3.5 MB (3467181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c828318950f314a45b930bb2ecce44606839c736b30e5a536da98c623b8d299`  
		Last Modified: Wed, 22 May 2024 22:58:55 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13470cb0fe3b718059121f9e336d8a39c7c6501b74223ef6341256658e1bcace`  
		Last Modified: Wed, 22 May 2024 22:58:56 GMT  
		Size: 109.0 KB (108952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb71cb4f8348194cc15fc03b348a7627488d870e97825c6b90943b0ae338cf78`  
		Last Modified: Wed, 22 May 2024 22:58:56 GMT  
		Size: 947.2 KB (947179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf76962900461e1b3abb72f20d20631d3b25499cb012ab300ff1821376388957`  
		Last Modified: Wed, 22 May 2024 22:58:56 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08e50381e18fbb7d44b8873051260c894b923dd7c0f3d5991ecdf29adce92b4f`  
		Last Modified: Wed, 22 May 2024 22:58:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:01c1aa4e15267a5d1ef8e1cce888ba1771e62572694e66e5325091d9462e97fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 KB (103635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08a7c8c3c66f6209ec1c9f32c410d4b36b45c40a9666ac58a1065cb5c5fa7d55`

```dockerfile
```

-	Layers:
	-	`sha256:3988b31dcd280e09051b45d43e2292273ee750d0802ae268cddfc6223b0e2d32`  
		Last Modified: Wed, 22 May 2024 22:58:56 GMT  
		Size: 84.2 KB (84223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:792ae2253532accb256a734c25cb5e4e8dc47177df82f43084a73db1d2e3a5d9`  
		Last Modified: Wed, 22 May 2024 22:58:56 GMT  
		Size: 19.4 KB (19412 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.20` - linux; ppc64le

```console
$ docker pull memcached@sha256:1cbe62d07f4a083cb5b5cb21eecf18f2c0662afda48b072a76d0711587b2a09c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4686554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ecef3bdf44124caa92d058e30ea98781387381719c49ea7dc28ae38302902f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:07:11 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_VERSION=1.6.27
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 22 May 2024 18:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 18:54:12 GMT
USER memcache
# Wed, 22 May 2024 18:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 May 2024 18:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea342fb939ae41c1145ee79234693ad7df9dba58d9a9d9ebb09071eec9886537`  
		Last Modified: Tue, 28 May 2024 23:38:45 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64a76d46c4c3cea865876670b86a10ceb59f479311d77bf613b1b301d97da3a`  
		Last Modified: Tue, 28 May 2024 23:38:46 GMT  
		Size: 123.0 KB (123006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca4b665cc9f3db507ee1264e940f8374dc3e014aefd2e5a46a9e6749f128a1d9`  
		Last Modified: Tue, 28 May 2024 23:38:46 GMT  
		Size: 992.3 KB (992335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da628c50da1874ce9bde8045dd3fbb7afc353942007abfb9a2e46ea34da235f6`  
		Last Modified: Tue, 28 May 2024 23:38:46 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bfe485c630c4e7e38f4195c2e2d6a35389a292c8a06f3f81e8ea6980a90daa5`  
		Last Modified: Tue, 28 May 2024 23:38:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:79bb7f48dd6a74241c1c606814efbe97139b8292c820acdb3f45ebf69cb029ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 KB (101741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c5ebac83e5929edb9713461ef04850f38b12eaef76efc9e139bd4e38922bc72`

```dockerfile
```

-	Layers:
	-	`sha256:51f7cf389b1f2aae558b2e6058899d13c84befb3bf2ab9932efce3a99495f2e3`  
		Last Modified: Tue, 28 May 2024 23:38:45 GMT  
		Size: 82.4 KB (82372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d3233692d06b58a5c2a997b62411dd2922e73826a8330abba28784bbfde1742`  
		Last Modified: Tue, 28 May 2024 23:38:45 GMT  
		Size: 19.4 KB (19369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.20` - linux; s390x

```console
$ docker pull memcached@sha256:43ea726a69d7aa19d38600a6b0c98114eac30a3f70d46c14f55746d508773378
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4551268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4218baf28d875e94ee50ce255b26888caf5671d153bb189ac30bebcc6635843b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_VERSION=1.6.27
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 22 May 2024 18:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 18:54:12 GMT
USER memcache
# Wed, 22 May 2024 18:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 May 2024 18:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bda8f56f465ce0440892acfd910a54a797991e554b31b96388ad100cb8dd18c`  
		Last Modified: Thu, 23 May 2024 03:19:15 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9810404860e30f64bc35f99f5cc930c953fa654ed2da190a4f4adf46c3914ea`  
		Last Modified: Thu, 23 May 2024 03:19:15 GMT  
		Size: 112.7 KB (112736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436abf7c43bfae37e20b0ae2fdaafa8c0165c2bbfcfd1242cd0ed17c846fdda4`  
		Last Modified: Thu, 23 May 2024 03:19:15 GMT  
		Size: 976.8 KB (976829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a62044b74bd7a363ba1ebba030952851d221ab43ab666a8bd59960ca5c76e9`  
		Last Modified: Thu, 23 May 2024 03:19:15 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc10b1e30c81f41f9d4012eda90ae84cfd53312c55770b504774fe80b5ba3ce`  
		Last Modified: Thu, 23 May 2024 03:19:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:5d3ab77f58725536e38b01d6e4bd4532e7bfa6cf7bd9eac35e77a4b70c8b8402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.6 KB (101615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd8bbbe1c27095d48770c6007e70e45c80a7c382286aaababe2fc83010d5fdda`

```dockerfile
```

-	Layers:
	-	`sha256:ea5bb003c385255e2e282399fe22ce79290bf682bb186d9a3901082902cc5d57`  
		Last Modified: Thu, 23 May 2024 03:19:15 GMT  
		Size: 82.3 KB (82314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb3910214e4a01e12528ebb507acafe782392af9209e1928be56b58e352cf7e1`  
		Last Modified: Thu, 23 May 2024 03:19:15 GMT  
		Size: 19.3 KB (19301 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-bookworm`

```console
$ docker pull memcached@sha256:58225aeaf238b8d6ca5b0c7cfc7cb81f44cdebd1ca184f032478cf4470c89520
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
$ docker pull memcached@sha256:3a548271d024b9f019806f9c57ab0c78b12721b99161b37c5fa1a54871aa4f1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32335604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58e4157cda75177132acadaa737dcc4ffbf23b3f4821d0948b4f9b882e606d2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 May 2024 09:14:35 GMT
ADD file:a92da94a28279478b2eae11dcdcd2913fc06af02498a5515cc3f288668d74e43 in / 
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
	-	`sha256:6ccc6628d3cdcda935b3b60cb54fa578d669965454d9cf39de3df9c1276132b7`  
		Last Modified: Tue, 14 May 2024 01:22:19 GMT  
		Size: 29.1 MB (29143688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ee82bdcb1e3a635fe9f1d5352d366d13d345f09eb3adfca8c9cdac667f12d4`  
		Last Modified: Tue, 14 May 2024 21:39:45 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6772b6152d32070d1bd037b4d40168112ccbe96e562d2b44c4be24a5f01f9b`  
		Last Modified: Tue, 14 May 2024 21:39:45 GMT  
		Size: 1.9 MB (1937746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833a7d6af8137233d7ad16026d9b1e1439a875762d4d0300c5b8fad018adba6b`  
		Last Modified: Tue, 14 May 2024 21:39:45 GMT  
		Size: 1.3 MB (1252656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdcc9953d5a8982f1bda95e99618eb60ce77f306601a4bd87e2b7032f58158fd`  
		Last Modified: Tue, 14 May 2024 21:39:45 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90055ed64046ecc2a6b606da0a99148b1b1006371fb88ea34d8116628aae47f3`  
		Last Modified: Tue, 14 May 2024 21:39:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:f17b6790b9c5b13d08059746553cd24795e4578c706cccada105ade01f3e16b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f05a4b82f72ff2643271e6710a1abb766fe5fbc715a018cabf4045f9cb137aa8`

```dockerfile
```

-	Layers:
	-	`sha256:57f1868b984b0196002a8a186c5ac8833f8eee2db97961c5355b4da6684b0fa4`  
		Last Modified: Tue, 14 May 2024 21:39:45 GMT  
		Size: 20.9 KB (20861 bytes)  
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
$ docker pull memcached@sha256:58225aeaf238b8d6ca5b0c7cfc7cb81f44cdebd1ca184f032478cf4470c89520
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
$ docker pull memcached@sha256:3a548271d024b9f019806f9c57ab0c78b12721b99161b37c5fa1a54871aa4f1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32335604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58e4157cda75177132acadaa737dcc4ffbf23b3f4821d0948b4f9b882e606d2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 May 2024 09:14:35 GMT
ADD file:a92da94a28279478b2eae11dcdcd2913fc06af02498a5515cc3f288668d74e43 in / 
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
	-	`sha256:6ccc6628d3cdcda935b3b60cb54fa578d669965454d9cf39de3df9c1276132b7`  
		Last Modified: Tue, 14 May 2024 01:22:19 GMT  
		Size: 29.1 MB (29143688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ee82bdcb1e3a635fe9f1d5352d366d13d345f09eb3adfca8c9cdac667f12d4`  
		Last Modified: Tue, 14 May 2024 21:39:45 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6772b6152d32070d1bd037b4d40168112ccbe96e562d2b44c4be24a5f01f9b`  
		Last Modified: Tue, 14 May 2024 21:39:45 GMT  
		Size: 1.9 MB (1937746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833a7d6af8137233d7ad16026d9b1e1439a875762d4d0300c5b8fad018adba6b`  
		Last Modified: Tue, 14 May 2024 21:39:45 GMT  
		Size: 1.3 MB (1252656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdcc9953d5a8982f1bda95e99618eb60ce77f306601a4bd87e2b7032f58158fd`  
		Last Modified: Tue, 14 May 2024 21:39:45 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90055ed64046ecc2a6b606da0a99148b1b1006371fb88ea34d8116628aae47f3`  
		Last Modified: Tue, 14 May 2024 21:39:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:f17b6790b9c5b13d08059746553cd24795e4578c706cccada105ade01f3e16b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f05a4b82f72ff2643271e6710a1abb766fe5fbc715a018cabf4045f9cb137aa8`

```dockerfile
```

-	Layers:
	-	`sha256:57f1868b984b0196002a8a186c5ac8833f8eee2db97961c5355b4da6684b0fa4`  
		Last Modified: Tue, 14 May 2024 21:39:45 GMT  
		Size: 20.9 KB (20861 bytes)  
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
$ docker pull memcached@sha256:b7474699be8a7cee225d1b7e4eef893d75bb92b7c6f5aae74ca9e4e95883ba96
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
$ docker pull memcached@sha256:5db13a42799b2fad49009ca0a76d26a2e05a662b5e9fefc080c5212a475e4a91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4680929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cef3a92c10bad723df3e5f47c23c6ab348ad3dc66c78bff564de8be3abb5642b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_VERSION=1.6.27
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 22 May 2024 18:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 18:54:12 GMT
USER memcache
# Wed, 22 May 2024 18:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 May 2024 18:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342a61fd751d022d1e9c72ba1b21e59935adbd6cb70b898d3cc459c0c0fda6a2`  
		Last Modified: Wed, 22 May 2024 22:58:40 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79489751750523d635370701c07fd1c88082d79215033bd9ca22d0255b48d1a1`  
		Last Modified: Wed, 22 May 2024 22:58:41 GMT  
		Size: 103.8 KB (103819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d972318261d7575d3f661b9dee0c0e0b42b4d1a480b0fbd7cb7d46f9fcc4eeb`  
		Last Modified: Wed, 22 May 2024 22:58:41 GMT  
		Size: 953.6 KB (953649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e73ab9b1403e8e6831efae93c083646a1856d194bac2dbddebfd33ec9bde5a1`  
		Last Modified: Wed, 22 May 2024 22:58:41 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fde407aeac5e16df26055d7ac8c318c420bcabb2a4ac507140f2db121ba8b8f0`  
		Last Modified: Wed, 22 May 2024 22:58:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:5635e12850ad272fd2d1fdd231445e5c65b60313a7674618a79804217102bbc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.7 KB (103735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f91d07fc259e406e39ccba78a20068801cbc6910b2ec70a3455899f993fb503c`

```dockerfile
```

-	Layers:
	-	`sha256:1ab3c7ccb18461e449a08496b5f2e0a26f8d2ab5f85e9ee0f5ce295fdf9611bc`  
		Last Modified: Wed, 22 May 2024 22:58:41 GMT  
		Size: 84.3 KB (84268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b7927aaa969cbae3829d94e66bdd3a7f141c6524b4deb74397a7ad6d6695ca6`  
		Last Modified: Wed, 22 May 2024 22:58:40 GMT  
		Size: 19.5 KB (19467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:e0688d9873a4cf749f89b43548d03f7d6c873596b1495b6da6943d4a3e767df1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5166898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6a1a46a5867d6ecd3c9bf99a695a89cc1f746f59d3a9a140b85a42b99a2e26`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_VERSION=1.6.27
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 22 May 2024 18:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 18:54:12 GMT
USER memcache
# Wed, 22 May 2024 18:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 May 2024 18:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024a9ccd1af8ffcfe453e22adead9362703e916c9dec4f1d4e94b597e660f23e`  
		Last Modified: Thu, 23 May 2024 06:29:57 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab592fa6ce63bf6772b1c208275d773ef6e671af73b2bd119e98de86dce4fc1`  
		Last Modified: Thu, 23 May 2024 06:29:58 GMT  
		Size: 121.0 KB (121017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd20d288c43aabf4d5e06a885b2e2f24583aae8e102eca2bf9257ce5e307a2cd`  
		Last Modified: Thu, 23 May 2024 06:29:57 GMT  
		Size: 957.7 KB (957743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d039a0fcb8c2c4f062cb3fb5c2b20ae16915479721254aadfc68d0319c84ee25`  
		Last Modified: Thu, 23 May 2024 06:29:57 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12cf5bc5246a4e40149d2a6b161c9fbce8354373e305c03088715546070c2742`  
		Last Modified: Thu, 23 May 2024 06:29:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:ec1932014529a81f308cae2db47073ddf344ef48cbc77766d95510cb7385b2af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 KB (103606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f0d85c8cad5520d9245c1563457fcf55da9b744f736c305ad21fad10027e013`

```dockerfile
```

-	Layers:
	-	`sha256:f77bdac9710cd22ef4eb7ba293b1b4fe4736e109a3767950432991fe0237fa54`  
		Last Modified: Thu, 23 May 2024 06:29:57 GMT  
		Size: 84.3 KB (84287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12016cd6764c2821a23d0e8fb3c182eda4d12d096e83cf52f57eb0103616d5e8`  
		Last Modified: Thu, 23 May 2024 06:29:57 GMT  
		Size: 19.3 KB (19319 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; 386

```console
$ docker pull memcached@sha256:95b69b6853d1e7b707eeacfd443723ac67c1a07a4d3adfaf8d639c8d26e864a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4524678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:924c2a8b8733b2b922abaabf6edf609336f035c3ee2158ec9daee20648f41f80`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:05:50 GMT
ADD file:6a4a5e48a600b064b83b954a55f1ddd3352780d69a6fb0ad816258011f5a3e47 in / 
# Wed, 22 May 2024 18:05:51 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_VERSION=1.6.27
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 22 May 2024 18:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 18:54:12 GMT
USER memcache
# Wed, 22 May 2024 18:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 May 2024 18:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:271acb68d2933b32dac564003959c5aea6d5d436c2779e253600ab35d7745465`  
		Last Modified: Wed, 22 May 2024 18:06:11 GMT  
		Size: 3.5 MB (3467181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c828318950f314a45b930bb2ecce44606839c736b30e5a536da98c623b8d299`  
		Last Modified: Wed, 22 May 2024 22:58:55 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13470cb0fe3b718059121f9e336d8a39c7c6501b74223ef6341256658e1bcace`  
		Last Modified: Wed, 22 May 2024 22:58:56 GMT  
		Size: 109.0 KB (108952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb71cb4f8348194cc15fc03b348a7627488d870e97825c6b90943b0ae338cf78`  
		Last Modified: Wed, 22 May 2024 22:58:56 GMT  
		Size: 947.2 KB (947179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf76962900461e1b3abb72f20d20631d3b25499cb012ab300ff1821376388957`  
		Last Modified: Wed, 22 May 2024 22:58:56 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08e50381e18fbb7d44b8873051260c894b923dd7c0f3d5991ecdf29adce92b4f`  
		Last Modified: Wed, 22 May 2024 22:58:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:01c1aa4e15267a5d1ef8e1cce888ba1771e62572694e66e5325091d9462e97fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 KB (103635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08a7c8c3c66f6209ec1c9f32c410d4b36b45c40a9666ac58a1065cb5c5fa7d55`

```dockerfile
```

-	Layers:
	-	`sha256:3988b31dcd280e09051b45d43e2292273ee750d0802ae268cddfc6223b0e2d32`  
		Last Modified: Wed, 22 May 2024 22:58:56 GMT  
		Size: 84.2 KB (84223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:792ae2253532accb256a734c25cb5e4e8dc47177df82f43084a73db1d2e3a5d9`  
		Last Modified: Wed, 22 May 2024 22:58:56 GMT  
		Size: 19.4 KB (19412 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:1cbe62d07f4a083cb5b5cb21eecf18f2c0662afda48b072a76d0711587b2a09c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4686554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ecef3bdf44124caa92d058e30ea98781387381719c49ea7dc28ae38302902f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:07:11 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_VERSION=1.6.27
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 22 May 2024 18:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 18:54:12 GMT
USER memcache
# Wed, 22 May 2024 18:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 May 2024 18:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea342fb939ae41c1145ee79234693ad7df9dba58d9a9d9ebb09071eec9886537`  
		Last Modified: Tue, 28 May 2024 23:38:45 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64a76d46c4c3cea865876670b86a10ceb59f479311d77bf613b1b301d97da3a`  
		Last Modified: Tue, 28 May 2024 23:38:46 GMT  
		Size: 123.0 KB (123006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca4b665cc9f3db507ee1264e940f8374dc3e014aefd2e5a46a9e6749f128a1d9`  
		Last Modified: Tue, 28 May 2024 23:38:46 GMT  
		Size: 992.3 KB (992335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da628c50da1874ce9bde8045dd3fbb7afc353942007abfb9a2e46ea34da235f6`  
		Last Modified: Tue, 28 May 2024 23:38:46 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bfe485c630c4e7e38f4195c2e2d6a35389a292c8a06f3f81e8ea6980a90daa5`  
		Last Modified: Tue, 28 May 2024 23:38:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:79bb7f48dd6a74241c1c606814efbe97139b8292c820acdb3f45ebf69cb029ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 KB (101741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c5ebac83e5929edb9713461ef04850f38b12eaef76efc9e139bd4e38922bc72`

```dockerfile
```

-	Layers:
	-	`sha256:51f7cf389b1f2aae558b2e6058899d13c84befb3bf2ab9932efce3a99495f2e3`  
		Last Modified: Tue, 28 May 2024 23:38:45 GMT  
		Size: 82.4 KB (82372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d3233692d06b58a5c2a997b62411dd2922e73826a8330abba28784bbfde1742`  
		Last Modified: Tue, 28 May 2024 23:38:45 GMT  
		Size: 19.4 KB (19369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:43ea726a69d7aa19d38600a6b0c98114eac30a3f70d46c14f55746d508773378
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4551268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4218baf28d875e94ee50ce255b26888caf5671d153bb189ac30bebcc6635843b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_VERSION=1.6.27
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 22 May 2024 18:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 18:54:12 GMT
USER memcache
# Wed, 22 May 2024 18:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 May 2024 18:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bda8f56f465ce0440892acfd910a54a797991e554b31b96388ad100cb8dd18c`  
		Last Modified: Thu, 23 May 2024 03:19:15 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9810404860e30f64bc35f99f5cc930c953fa654ed2da190a4f4adf46c3914ea`  
		Last Modified: Thu, 23 May 2024 03:19:15 GMT  
		Size: 112.7 KB (112736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436abf7c43bfae37e20b0ae2fdaafa8c0165c2bbfcfd1242cd0ed17c846fdda4`  
		Last Modified: Thu, 23 May 2024 03:19:15 GMT  
		Size: 976.8 KB (976829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a62044b74bd7a363ba1ebba030952851d221ab43ab666a8bd59960ca5c76e9`  
		Last Modified: Thu, 23 May 2024 03:19:15 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc10b1e30c81f41f9d4012eda90ae84cfd53312c55770b504774fe80b5ba3ce`  
		Last Modified: Thu, 23 May 2024 03:19:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:5d3ab77f58725536e38b01d6e4bd4532e7bfa6cf7bd9eac35e77a4b70c8b8402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.6 KB (101615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd8bbbe1c27095d48770c6007e70e45c80a7c382286aaababe2fc83010d5fdda`

```dockerfile
```

-	Layers:
	-	`sha256:ea5bb003c385255e2e282399fe22ce79290bf682bb186d9a3901082902cc5d57`  
		Last Modified: Thu, 23 May 2024 03:19:15 GMT  
		Size: 82.3 KB (82314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb3910214e4a01e12528ebb507acafe782392af9209e1928be56b58e352cf7e1`  
		Last Modified: Thu, 23 May 2024 03:19:15 GMT  
		Size: 19.3 KB (19301 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine3.20`

```console
$ docker pull memcached@sha256:b7474699be8a7cee225d1b7e4eef893d75bb92b7c6f5aae74ca9e4e95883ba96
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

### `memcached:1.6-alpine3.20` - linux; amd64

```console
$ docker pull memcached@sha256:5db13a42799b2fad49009ca0a76d26a2e05a662b5e9fefc080c5212a475e4a91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4680929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cef3a92c10bad723df3e5f47c23c6ab348ad3dc66c78bff564de8be3abb5642b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_VERSION=1.6.27
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 22 May 2024 18:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 18:54:12 GMT
USER memcache
# Wed, 22 May 2024 18:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 May 2024 18:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342a61fd751d022d1e9c72ba1b21e59935adbd6cb70b898d3cc459c0c0fda6a2`  
		Last Modified: Wed, 22 May 2024 22:58:40 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79489751750523d635370701c07fd1c88082d79215033bd9ca22d0255b48d1a1`  
		Last Modified: Wed, 22 May 2024 22:58:41 GMT  
		Size: 103.8 KB (103819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d972318261d7575d3f661b9dee0c0e0b42b4d1a480b0fbd7cb7d46f9fcc4eeb`  
		Last Modified: Wed, 22 May 2024 22:58:41 GMT  
		Size: 953.6 KB (953649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e73ab9b1403e8e6831efae93c083646a1856d194bac2dbddebfd33ec9bde5a1`  
		Last Modified: Wed, 22 May 2024 22:58:41 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fde407aeac5e16df26055d7ac8c318c420bcabb2a4ac507140f2db121ba8b8f0`  
		Last Modified: Wed, 22 May 2024 22:58:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:5635e12850ad272fd2d1fdd231445e5c65b60313a7674618a79804217102bbc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.7 KB (103735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f91d07fc259e406e39ccba78a20068801cbc6910b2ec70a3455899f993fb503c`

```dockerfile
```

-	Layers:
	-	`sha256:1ab3c7ccb18461e449a08496b5f2e0a26f8d2ab5f85e9ee0f5ce295fdf9611bc`  
		Last Modified: Wed, 22 May 2024 22:58:41 GMT  
		Size: 84.3 KB (84268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b7927aaa969cbae3829d94e66bdd3a7f141c6524b4deb74397a7ad6d6695ca6`  
		Last Modified: Wed, 22 May 2024 22:58:40 GMT  
		Size: 19.5 KB (19467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:e0688d9873a4cf749f89b43548d03f7d6c873596b1495b6da6943d4a3e767df1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5166898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6a1a46a5867d6ecd3c9bf99a695a89cc1f746f59d3a9a140b85a42b99a2e26`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_VERSION=1.6.27
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 22 May 2024 18:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 18:54:12 GMT
USER memcache
# Wed, 22 May 2024 18:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 May 2024 18:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024a9ccd1af8ffcfe453e22adead9362703e916c9dec4f1d4e94b597e660f23e`  
		Last Modified: Thu, 23 May 2024 06:29:57 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab592fa6ce63bf6772b1c208275d773ef6e671af73b2bd119e98de86dce4fc1`  
		Last Modified: Thu, 23 May 2024 06:29:58 GMT  
		Size: 121.0 KB (121017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd20d288c43aabf4d5e06a885b2e2f24583aae8e102eca2bf9257ce5e307a2cd`  
		Last Modified: Thu, 23 May 2024 06:29:57 GMT  
		Size: 957.7 KB (957743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d039a0fcb8c2c4f062cb3fb5c2b20ae16915479721254aadfc68d0319c84ee25`  
		Last Modified: Thu, 23 May 2024 06:29:57 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12cf5bc5246a4e40149d2a6b161c9fbce8354373e305c03088715546070c2742`  
		Last Modified: Thu, 23 May 2024 06:29:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:ec1932014529a81f308cae2db47073ddf344ef48cbc77766d95510cb7385b2af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 KB (103606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f0d85c8cad5520d9245c1563457fcf55da9b744f736c305ad21fad10027e013`

```dockerfile
```

-	Layers:
	-	`sha256:f77bdac9710cd22ef4eb7ba293b1b4fe4736e109a3767950432991fe0237fa54`  
		Last Modified: Thu, 23 May 2024 06:29:57 GMT  
		Size: 84.3 KB (84287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12016cd6764c2821a23d0e8fb3c182eda4d12d096e83cf52f57eb0103616d5e8`  
		Last Modified: Thu, 23 May 2024 06:29:57 GMT  
		Size: 19.3 KB (19319 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.20` - linux; 386

```console
$ docker pull memcached@sha256:95b69b6853d1e7b707eeacfd443723ac67c1a07a4d3adfaf8d639c8d26e864a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4524678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:924c2a8b8733b2b922abaabf6edf609336f035c3ee2158ec9daee20648f41f80`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:05:50 GMT
ADD file:6a4a5e48a600b064b83b954a55f1ddd3352780d69a6fb0ad816258011f5a3e47 in / 
# Wed, 22 May 2024 18:05:51 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_VERSION=1.6.27
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 22 May 2024 18:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 18:54:12 GMT
USER memcache
# Wed, 22 May 2024 18:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 May 2024 18:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:271acb68d2933b32dac564003959c5aea6d5d436c2779e253600ab35d7745465`  
		Last Modified: Wed, 22 May 2024 18:06:11 GMT  
		Size: 3.5 MB (3467181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c828318950f314a45b930bb2ecce44606839c736b30e5a536da98c623b8d299`  
		Last Modified: Wed, 22 May 2024 22:58:55 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13470cb0fe3b718059121f9e336d8a39c7c6501b74223ef6341256658e1bcace`  
		Last Modified: Wed, 22 May 2024 22:58:56 GMT  
		Size: 109.0 KB (108952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb71cb4f8348194cc15fc03b348a7627488d870e97825c6b90943b0ae338cf78`  
		Last Modified: Wed, 22 May 2024 22:58:56 GMT  
		Size: 947.2 KB (947179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf76962900461e1b3abb72f20d20631d3b25499cb012ab300ff1821376388957`  
		Last Modified: Wed, 22 May 2024 22:58:56 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08e50381e18fbb7d44b8873051260c894b923dd7c0f3d5991ecdf29adce92b4f`  
		Last Modified: Wed, 22 May 2024 22:58:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:01c1aa4e15267a5d1ef8e1cce888ba1771e62572694e66e5325091d9462e97fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 KB (103635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08a7c8c3c66f6209ec1c9f32c410d4b36b45c40a9666ac58a1065cb5c5fa7d55`

```dockerfile
```

-	Layers:
	-	`sha256:3988b31dcd280e09051b45d43e2292273ee750d0802ae268cddfc6223b0e2d32`  
		Last Modified: Wed, 22 May 2024 22:58:56 GMT  
		Size: 84.2 KB (84223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:792ae2253532accb256a734c25cb5e4e8dc47177df82f43084a73db1d2e3a5d9`  
		Last Modified: Wed, 22 May 2024 22:58:56 GMT  
		Size: 19.4 KB (19412 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.20` - linux; ppc64le

```console
$ docker pull memcached@sha256:1cbe62d07f4a083cb5b5cb21eecf18f2c0662afda48b072a76d0711587b2a09c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4686554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ecef3bdf44124caa92d058e30ea98781387381719c49ea7dc28ae38302902f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:07:11 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_VERSION=1.6.27
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 22 May 2024 18:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 18:54:12 GMT
USER memcache
# Wed, 22 May 2024 18:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 May 2024 18:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea342fb939ae41c1145ee79234693ad7df9dba58d9a9d9ebb09071eec9886537`  
		Last Modified: Tue, 28 May 2024 23:38:45 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64a76d46c4c3cea865876670b86a10ceb59f479311d77bf613b1b301d97da3a`  
		Last Modified: Tue, 28 May 2024 23:38:46 GMT  
		Size: 123.0 KB (123006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca4b665cc9f3db507ee1264e940f8374dc3e014aefd2e5a46a9e6749f128a1d9`  
		Last Modified: Tue, 28 May 2024 23:38:46 GMT  
		Size: 992.3 KB (992335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da628c50da1874ce9bde8045dd3fbb7afc353942007abfb9a2e46ea34da235f6`  
		Last Modified: Tue, 28 May 2024 23:38:46 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bfe485c630c4e7e38f4195c2e2d6a35389a292c8a06f3f81e8ea6980a90daa5`  
		Last Modified: Tue, 28 May 2024 23:38:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:79bb7f48dd6a74241c1c606814efbe97139b8292c820acdb3f45ebf69cb029ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 KB (101741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c5ebac83e5929edb9713461ef04850f38b12eaef76efc9e139bd4e38922bc72`

```dockerfile
```

-	Layers:
	-	`sha256:51f7cf389b1f2aae558b2e6058899d13c84befb3bf2ab9932efce3a99495f2e3`  
		Last Modified: Tue, 28 May 2024 23:38:45 GMT  
		Size: 82.4 KB (82372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d3233692d06b58a5c2a997b62411dd2922e73826a8330abba28784bbfde1742`  
		Last Modified: Tue, 28 May 2024 23:38:45 GMT  
		Size: 19.4 KB (19369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.20` - linux; s390x

```console
$ docker pull memcached@sha256:43ea726a69d7aa19d38600a6b0c98114eac30a3f70d46c14f55746d508773378
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4551268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4218baf28d875e94ee50ce255b26888caf5671d153bb189ac30bebcc6635843b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_VERSION=1.6.27
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 22 May 2024 18:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 18:54:12 GMT
USER memcache
# Wed, 22 May 2024 18:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 May 2024 18:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bda8f56f465ce0440892acfd910a54a797991e554b31b96388ad100cb8dd18c`  
		Last Modified: Thu, 23 May 2024 03:19:15 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9810404860e30f64bc35f99f5cc930c953fa654ed2da190a4f4adf46c3914ea`  
		Last Modified: Thu, 23 May 2024 03:19:15 GMT  
		Size: 112.7 KB (112736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436abf7c43bfae37e20b0ae2fdaafa8c0165c2bbfcfd1242cd0ed17c846fdda4`  
		Last Modified: Thu, 23 May 2024 03:19:15 GMT  
		Size: 976.8 KB (976829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a62044b74bd7a363ba1ebba030952851d221ab43ab666a8bd59960ca5c76e9`  
		Last Modified: Thu, 23 May 2024 03:19:15 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc10b1e30c81f41f9d4012eda90ae84cfd53312c55770b504774fe80b5ba3ce`  
		Last Modified: Thu, 23 May 2024 03:19:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:5d3ab77f58725536e38b01d6e4bd4532e7bfa6cf7bd9eac35e77a4b70c8b8402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.6 KB (101615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd8bbbe1c27095d48770c6007e70e45c80a7c382286aaababe2fc83010d5fdda`

```dockerfile
```

-	Layers:
	-	`sha256:ea5bb003c385255e2e282399fe22ce79290bf682bb186d9a3901082902cc5d57`  
		Last Modified: Thu, 23 May 2024 03:19:15 GMT  
		Size: 82.3 KB (82314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb3910214e4a01e12528ebb507acafe782392af9209e1928be56b58e352cf7e1`  
		Last Modified: Thu, 23 May 2024 03:19:15 GMT  
		Size: 19.3 KB (19301 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-bookworm`

```console
$ docker pull memcached@sha256:58225aeaf238b8d6ca5b0c7cfc7cb81f44cdebd1ca184f032478cf4470c89520
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
$ docker pull memcached@sha256:3a548271d024b9f019806f9c57ab0c78b12721b99161b37c5fa1a54871aa4f1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32335604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58e4157cda75177132acadaa737dcc4ffbf23b3f4821d0948b4f9b882e606d2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 May 2024 09:14:35 GMT
ADD file:a92da94a28279478b2eae11dcdcd2913fc06af02498a5515cc3f288668d74e43 in / 
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
	-	`sha256:6ccc6628d3cdcda935b3b60cb54fa578d669965454d9cf39de3df9c1276132b7`  
		Last Modified: Tue, 14 May 2024 01:22:19 GMT  
		Size: 29.1 MB (29143688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ee82bdcb1e3a635fe9f1d5352d366d13d345f09eb3adfca8c9cdac667f12d4`  
		Last Modified: Tue, 14 May 2024 21:39:45 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6772b6152d32070d1bd037b4d40168112ccbe96e562d2b44c4be24a5f01f9b`  
		Last Modified: Tue, 14 May 2024 21:39:45 GMT  
		Size: 1.9 MB (1937746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833a7d6af8137233d7ad16026d9b1e1439a875762d4d0300c5b8fad018adba6b`  
		Last Modified: Tue, 14 May 2024 21:39:45 GMT  
		Size: 1.3 MB (1252656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdcc9953d5a8982f1bda95e99618eb60ce77f306601a4bd87e2b7032f58158fd`  
		Last Modified: Tue, 14 May 2024 21:39:45 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90055ed64046ecc2a6b606da0a99148b1b1006371fb88ea34d8116628aae47f3`  
		Last Modified: Tue, 14 May 2024 21:39:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:f17b6790b9c5b13d08059746553cd24795e4578c706cccada105ade01f3e16b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f05a4b82f72ff2643271e6710a1abb766fe5fbc715a018cabf4045f9cb137aa8`

```dockerfile
```

-	Layers:
	-	`sha256:57f1868b984b0196002a8a186c5ac8833f8eee2db97961c5355b4da6684b0fa4`  
		Last Modified: Tue, 14 May 2024 21:39:45 GMT  
		Size: 20.9 KB (20861 bytes)  
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

## `memcached:1.6.28`

```console
$ docker pull memcached@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `memcached:1.6.28-alpine`

```console
$ docker pull memcached@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `memcached:1.6.28-alpine3.20`

```console
$ docker pull memcached@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `memcached:1.6.28-bookworm`

```console
$ docker pull memcached@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `memcached:alpine`

```console
$ docker pull memcached@sha256:b7474699be8a7cee225d1b7e4eef893d75bb92b7c6f5aae74ca9e4e95883ba96
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
$ docker pull memcached@sha256:5db13a42799b2fad49009ca0a76d26a2e05a662b5e9fefc080c5212a475e4a91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4680929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cef3a92c10bad723df3e5f47c23c6ab348ad3dc66c78bff564de8be3abb5642b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_VERSION=1.6.27
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 22 May 2024 18:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 18:54:12 GMT
USER memcache
# Wed, 22 May 2024 18:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 May 2024 18:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342a61fd751d022d1e9c72ba1b21e59935adbd6cb70b898d3cc459c0c0fda6a2`  
		Last Modified: Wed, 22 May 2024 22:58:40 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79489751750523d635370701c07fd1c88082d79215033bd9ca22d0255b48d1a1`  
		Last Modified: Wed, 22 May 2024 22:58:41 GMT  
		Size: 103.8 KB (103819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d972318261d7575d3f661b9dee0c0e0b42b4d1a480b0fbd7cb7d46f9fcc4eeb`  
		Last Modified: Wed, 22 May 2024 22:58:41 GMT  
		Size: 953.6 KB (953649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e73ab9b1403e8e6831efae93c083646a1856d194bac2dbddebfd33ec9bde5a1`  
		Last Modified: Wed, 22 May 2024 22:58:41 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fde407aeac5e16df26055d7ac8c318c420bcabb2a4ac507140f2db121ba8b8f0`  
		Last Modified: Wed, 22 May 2024 22:58:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:5635e12850ad272fd2d1fdd231445e5c65b60313a7674618a79804217102bbc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.7 KB (103735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f91d07fc259e406e39ccba78a20068801cbc6910b2ec70a3455899f993fb503c`

```dockerfile
```

-	Layers:
	-	`sha256:1ab3c7ccb18461e449a08496b5f2e0a26f8d2ab5f85e9ee0f5ce295fdf9611bc`  
		Last Modified: Wed, 22 May 2024 22:58:41 GMT  
		Size: 84.3 KB (84268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b7927aaa969cbae3829d94e66bdd3a7f141c6524b4deb74397a7ad6d6695ca6`  
		Last Modified: Wed, 22 May 2024 22:58:40 GMT  
		Size: 19.5 KB (19467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:e0688d9873a4cf749f89b43548d03f7d6c873596b1495b6da6943d4a3e767df1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5166898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6a1a46a5867d6ecd3c9bf99a695a89cc1f746f59d3a9a140b85a42b99a2e26`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_VERSION=1.6.27
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 22 May 2024 18:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 18:54:12 GMT
USER memcache
# Wed, 22 May 2024 18:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 May 2024 18:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024a9ccd1af8ffcfe453e22adead9362703e916c9dec4f1d4e94b597e660f23e`  
		Last Modified: Thu, 23 May 2024 06:29:57 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab592fa6ce63bf6772b1c208275d773ef6e671af73b2bd119e98de86dce4fc1`  
		Last Modified: Thu, 23 May 2024 06:29:58 GMT  
		Size: 121.0 KB (121017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd20d288c43aabf4d5e06a885b2e2f24583aae8e102eca2bf9257ce5e307a2cd`  
		Last Modified: Thu, 23 May 2024 06:29:57 GMT  
		Size: 957.7 KB (957743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d039a0fcb8c2c4f062cb3fb5c2b20ae16915479721254aadfc68d0319c84ee25`  
		Last Modified: Thu, 23 May 2024 06:29:57 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12cf5bc5246a4e40149d2a6b161c9fbce8354373e305c03088715546070c2742`  
		Last Modified: Thu, 23 May 2024 06:29:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:ec1932014529a81f308cae2db47073ddf344ef48cbc77766d95510cb7385b2af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 KB (103606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f0d85c8cad5520d9245c1563457fcf55da9b744f736c305ad21fad10027e013`

```dockerfile
```

-	Layers:
	-	`sha256:f77bdac9710cd22ef4eb7ba293b1b4fe4736e109a3767950432991fe0237fa54`  
		Last Modified: Thu, 23 May 2024 06:29:57 GMT  
		Size: 84.3 KB (84287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12016cd6764c2821a23d0e8fb3c182eda4d12d096e83cf52f57eb0103616d5e8`  
		Last Modified: Thu, 23 May 2024 06:29:57 GMT  
		Size: 19.3 KB (19319 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; 386

```console
$ docker pull memcached@sha256:95b69b6853d1e7b707eeacfd443723ac67c1a07a4d3adfaf8d639c8d26e864a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4524678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:924c2a8b8733b2b922abaabf6edf609336f035c3ee2158ec9daee20648f41f80`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:05:50 GMT
ADD file:6a4a5e48a600b064b83b954a55f1ddd3352780d69a6fb0ad816258011f5a3e47 in / 
# Wed, 22 May 2024 18:05:51 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_VERSION=1.6.27
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 22 May 2024 18:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 18:54:12 GMT
USER memcache
# Wed, 22 May 2024 18:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 May 2024 18:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:271acb68d2933b32dac564003959c5aea6d5d436c2779e253600ab35d7745465`  
		Last Modified: Wed, 22 May 2024 18:06:11 GMT  
		Size: 3.5 MB (3467181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c828318950f314a45b930bb2ecce44606839c736b30e5a536da98c623b8d299`  
		Last Modified: Wed, 22 May 2024 22:58:55 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13470cb0fe3b718059121f9e336d8a39c7c6501b74223ef6341256658e1bcace`  
		Last Modified: Wed, 22 May 2024 22:58:56 GMT  
		Size: 109.0 KB (108952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb71cb4f8348194cc15fc03b348a7627488d870e97825c6b90943b0ae338cf78`  
		Last Modified: Wed, 22 May 2024 22:58:56 GMT  
		Size: 947.2 KB (947179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf76962900461e1b3abb72f20d20631d3b25499cb012ab300ff1821376388957`  
		Last Modified: Wed, 22 May 2024 22:58:56 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08e50381e18fbb7d44b8873051260c894b923dd7c0f3d5991ecdf29adce92b4f`  
		Last Modified: Wed, 22 May 2024 22:58:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:01c1aa4e15267a5d1ef8e1cce888ba1771e62572694e66e5325091d9462e97fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 KB (103635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08a7c8c3c66f6209ec1c9f32c410d4b36b45c40a9666ac58a1065cb5c5fa7d55`

```dockerfile
```

-	Layers:
	-	`sha256:3988b31dcd280e09051b45d43e2292273ee750d0802ae268cddfc6223b0e2d32`  
		Last Modified: Wed, 22 May 2024 22:58:56 GMT  
		Size: 84.2 KB (84223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:792ae2253532accb256a734c25cb5e4e8dc47177df82f43084a73db1d2e3a5d9`  
		Last Modified: Wed, 22 May 2024 22:58:56 GMT  
		Size: 19.4 KB (19412 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:1cbe62d07f4a083cb5b5cb21eecf18f2c0662afda48b072a76d0711587b2a09c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4686554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ecef3bdf44124caa92d058e30ea98781387381719c49ea7dc28ae38302902f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:07:11 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_VERSION=1.6.27
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 22 May 2024 18:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 18:54:12 GMT
USER memcache
# Wed, 22 May 2024 18:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 May 2024 18:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea342fb939ae41c1145ee79234693ad7df9dba58d9a9d9ebb09071eec9886537`  
		Last Modified: Tue, 28 May 2024 23:38:45 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64a76d46c4c3cea865876670b86a10ceb59f479311d77bf613b1b301d97da3a`  
		Last Modified: Tue, 28 May 2024 23:38:46 GMT  
		Size: 123.0 KB (123006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca4b665cc9f3db507ee1264e940f8374dc3e014aefd2e5a46a9e6749f128a1d9`  
		Last Modified: Tue, 28 May 2024 23:38:46 GMT  
		Size: 992.3 KB (992335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da628c50da1874ce9bde8045dd3fbb7afc353942007abfb9a2e46ea34da235f6`  
		Last Modified: Tue, 28 May 2024 23:38:46 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bfe485c630c4e7e38f4195c2e2d6a35389a292c8a06f3f81e8ea6980a90daa5`  
		Last Modified: Tue, 28 May 2024 23:38:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:79bb7f48dd6a74241c1c606814efbe97139b8292c820acdb3f45ebf69cb029ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 KB (101741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c5ebac83e5929edb9713461ef04850f38b12eaef76efc9e139bd4e38922bc72`

```dockerfile
```

-	Layers:
	-	`sha256:51f7cf389b1f2aae558b2e6058899d13c84befb3bf2ab9932efce3a99495f2e3`  
		Last Modified: Tue, 28 May 2024 23:38:45 GMT  
		Size: 82.4 KB (82372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d3233692d06b58a5c2a997b62411dd2922e73826a8330abba28784bbfde1742`  
		Last Modified: Tue, 28 May 2024 23:38:45 GMT  
		Size: 19.4 KB (19369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; s390x

```console
$ docker pull memcached@sha256:43ea726a69d7aa19d38600a6b0c98114eac30a3f70d46c14f55746d508773378
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4551268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4218baf28d875e94ee50ce255b26888caf5671d153bb189ac30bebcc6635843b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_VERSION=1.6.27
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 22 May 2024 18:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 18:54:12 GMT
USER memcache
# Wed, 22 May 2024 18:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 May 2024 18:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bda8f56f465ce0440892acfd910a54a797991e554b31b96388ad100cb8dd18c`  
		Last Modified: Thu, 23 May 2024 03:19:15 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9810404860e30f64bc35f99f5cc930c953fa654ed2da190a4f4adf46c3914ea`  
		Last Modified: Thu, 23 May 2024 03:19:15 GMT  
		Size: 112.7 KB (112736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436abf7c43bfae37e20b0ae2fdaafa8c0165c2bbfcfd1242cd0ed17c846fdda4`  
		Last Modified: Thu, 23 May 2024 03:19:15 GMT  
		Size: 976.8 KB (976829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a62044b74bd7a363ba1ebba030952851d221ab43ab666a8bd59960ca5c76e9`  
		Last Modified: Thu, 23 May 2024 03:19:15 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc10b1e30c81f41f9d4012eda90ae84cfd53312c55770b504774fe80b5ba3ce`  
		Last Modified: Thu, 23 May 2024 03:19:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:5d3ab77f58725536e38b01d6e4bd4532e7bfa6cf7bd9eac35e77a4b70c8b8402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.6 KB (101615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd8bbbe1c27095d48770c6007e70e45c80a7c382286aaababe2fc83010d5fdda`

```dockerfile
```

-	Layers:
	-	`sha256:ea5bb003c385255e2e282399fe22ce79290bf682bb186d9a3901082902cc5d57`  
		Last Modified: Thu, 23 May 2024 03:19:15 GMT  
		Size: 82.3 KB (82314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb3910214e4a01e12528ebb507acafe782392af9209e1928be56b58e352cf7e1`  
		Last Modified: Thu, 23 May 2024 03:19:15 GMT  
		Size: 19.3 KB (19301 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine3.20`

```console
$ docker pull memcached@sha256:b7474699be8a7cee225d1b7e4eef893d75bb92b7c6f5aae74ca9e4e95883ba96
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

### `memcached:alpine3.20` - linux; amd64

```console
$ docker pull memcached@sha256:5db13a42799b2fad49009ca0a76d26a2e05a662b5e9fefc080c5212a475e4a91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4680929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cef3a92c10bad723df3e5f47c23c6ab348ad3dc66c78bff564de8be3abb5642b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_VERSION=1.6.27
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 22 May 2024 18:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 18:54:12 GMT
USER memcache
# Wed, 22 May 2024 18:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 May 2024 18:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342a61fd751d022d1e9c72ba1b21e59935adbd6cb70b898d3cc459c0c0fda6a2`  
		Last Modified: Wed, 22 May 2024 22:58:40 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79489751750523d635370701c07fd1c88082d79215033bd9ca22d0255b48d1a1`  
		Last Modified: Wed, 22 May 2024 22:58:41 GMT  
		Size: 103.8 KB (103819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d972318261d7575d3f661b9dee0c0e0b42b4d1a480b0fbd7cb7d46f9fcc4eeb`  
		Last Modified: Wed, 22 May 2024 22:58:41 GMT  
		Size: 953.6 KB (953649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e73ab9b1403e8e6831efae93c083646a1856d194bac2dbddebfd33ec9bde5a1`  
		Last Modified: Wed, 22 May 2024 22:58:41 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fde407aeac5e16df26055d7ac8c318c420bcabb2a4ac507140f2db121ba8b8f0`  
		Last Modified: Wed, 22 May 2024 22:58:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:5635e12850ad272fd2d1fdd231445e5c65b60313a7674618a79804217102bbc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.7 KB (103735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f91d07fc259e406e39ccba78a20068801cbc6910b2ec70a3455899f993fb503c`

```dockerfile
```

-	Layers:
	-	`sha256:1ab3c7ccb18461e449a08496b5f2e0a26f8d2ab5f85e9ee0f5ce295fdf9611bc`  
		Last Modified: Wed, 22 May 2024 22:58:41 GMT  
		Size: 84.3 KB (84268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b7927aaa969cbae3829d94e66bdd3a7f141c6524b4deb74397a7ad6d6695ca6`  
		Last Modified: Wed, 22 May 2024 22:58:40 GMT  
		Size: 19.5 KB (19467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.20` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:e0688d9873a4cf749f89b43548d03f7d6c873596b1495b6da6943d4a3e767df1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5166898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6a1a46a5867d6ecd3c9bf99a695a89cc1f746f59d3a9a140b85a42b99a2e26`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_VERSION=1.6.27
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 22 May 2024 18:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 18:54:12 GMT
USER memcache
# Wed, 22 May 2024 18:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 May 2024 18:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024a9ccd1af8ffcfe453e22adead9362703e916c9dec4f1d4e94b597e660f23e`  
		Last Modified: Thu, 23 May 2024 06:29:57 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab592fa6ce63bf6772b1c208275d773ef6e671af73b2bd119e98de86dce4fc1`  
		Last Modified: Thu, 23 May 2024 06:29:58 GMT  
		Size: 121.0 KB (121017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd20d288c43aabf4d5e06a885b2e2f24583aae8e102eca2bf9257ce5e307a2cd`  
		Last Modified: Thu, 23 May 2024 06:29:57 GMT  
		Size: 957.7 KB (957743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d039a0fcb8c2c4f062cb3fb5c2b20ae16915479721254aadfc68d0319c84ee25`  
		Last Modified: Thu, 23 May 2024 06:29:57 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12cf5bc5246a4e40149d2a6b161c9fbce8354373e305c03088715546070c2742`  
		Last Modified: Thu, 23 May 2024 06:29:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:ec1932014529a81f308cae2db47073ddf344ef48cbc77766d95510cb7385b2af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 KB (103606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f0d85c8cad5520d9245c1563457fcf55da9b744f736c305ad21fad10027e013`

```dockerfile
```

-	Layers:
	-	`sha256:f77bdac9710cd22ef4eb7ba293b1b4fe4736e109a3767950432991fe0237fa54`  
		Last Modified: Thu, 23 May 2024 06:29:57 GMT  
		Size: 84.3 KB (84287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12016cd6764c2821a23d0e8fb3c182eda4d12d096e83cf52f57eb0103616d5e8`  
		Last Modified: Thu, 23 May 2024 06:29:57 GMT  
		Size: 19.3 KB (19319 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.20` - linux; 386

```console
$ docker pull memcached@sha256:95b69b6853d1e7b707eeacfd443723ac67c1a07a4d3adfaf8d639c8d26e864a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4524678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:924c2a8b8733b2b922abaabf6edf609336f035c3ee2158ec9daee20648f41f80`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:05:50 GMT
ADD file:6a4a5e48a600b064b83b954a55f1ddd3352780d69a6fb0ad816258011f5a3e47 in / 
# Wed, 22 May 2024 18:05:51 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_VERSION=1.6.27
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 22 May 2024 18:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 18:54:12 GMT
USER memcache
# Wed, 22 May 2024 18:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 May 2024 18:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:271acb68d2933b32dac564003959c5aea6d5d436c2779e253600ab35d7745465`  
		Last Modified: Wed, 22 May 2024 18:06:11 GMT  
		Size: 3.5 MB (3467181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c828318950f314a45b930bb2ecce44606839c736b30e5a536da98c623b8d299`  
		Last Modified: Wed, 22 May 2024 22:58:55 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13470cb0fe3b718059121f9e336d8a39c7c6501b74223ef6341256658e1bcace`  
		Last Modified: Wed, 22 May 2024 22:58:56 GMT  
		Size: 109.0 KB (108952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb71cb4f8348194cc15fc03b348a7627488d870e97825c6b90943b0ae338cf78`  
		Last Modified: Wed, 22 May 2024 22:58:56 GMT  
		Size: 947.2 KB (947179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf76962900461e1b3abb72f20d20631d3b25499cb012ab300ff1821376388957`  
		Last Modified: Wed, 22 May 2024 22:58:56 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08e50381e18fbb7d44b8873051260c894b923dd7c0f3d5991ecdf29adce92b4f`  
		Last Modified: Wed, 22 May 2024 22:58:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:01c1aa4e15267a5d1ef8e1cce888ba1771e62572694e66e5325091d9462e97fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 KB (103635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08a7c8c3c66f6209ec1c9f32c410d4b36b45c40a9666ac58a1065cb5c5fa7d55`

```dockerfile
```

-	Layers:
	-	`sha256:3988b31dcd280e09051b45d43e2292273ee750d0802ae268cddfc6223b0e2d32`  
		Last Modified: Wed, 22 May 2024 22:58:56 GMT  
		Size: 84.2 KB (84223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:792ae2253532accb256a734c25cb5e4e8dc47177df82f43084a73db1d2e3a5d9`  
		Last Modified: Wed, 22 May 2024 22:58:56 GMT  
		Size: 19.4 KB (19412 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.20` - linux; ppc64le

```console
$ docker pull memcached@sha256:1cbe62d07f4a083cb5b5cb21eecf18f2c0662afda48b072a76d0711587b2a09c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4686554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ecef3bdf44124caa92d058e30ea98781387381719c49ea7dc28ae38302902f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:07:11 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_VERSION=1.6.27
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 22 May 2024 18:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 18:54:12 GMT
USER memcache
# Wed, 22 May 2024 18:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 May 2024 18:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea342fb939ae41c1145ee79234693ad7df9dba58d9a9d9ebb09071eec9886537`  
		Last Modified: Tue, 28 May 2024 23:38:45 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64a76d46c4c3cea865876670b86a10ceb59f479311d77bf613b1b301d97da3a`  
		Last Modified: Tue, 28 May 2024 23:38:46 GMT  
		Size: 123.0 KB (123006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca4b665cc9f3db507ee1264e940f8374dc3e014aefd2e5a46a9e6749f128a1d9`  
		Last Modified: Tue, 28 May 2024 23:38:46 GMT  
		Size: 992.3 KB (992335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da628c50da1874ce9bde8045dd3fbb7afc353942007abfb9a2e46ea34da235f6`  
		Last Modified: Tue, 28 May 2024 23:38:46 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bfe485c630c4e7e38f4195c2e2d6a35389a292c8a06f3f81e8ea6980a90daa5`  
		Last Modified: Tue, 28 May 2024 23:38:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:79bb7f48dd6a74241c1c606814efbe97139b8292c820acdb3f45ebf69cb029ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 KB (101741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c5ebac83e5929edb9713461ef04850f38b12eaef76efc9e139bd4e38922bc72`

```dockerfile
```

-	Layers:
	-	`sha256:51f7cf389b1f2aae558b2e6058899d13c84befb3bf2ab9932efce3a99495f2e3`  
		Last Modified: Tue, 28 May 2024 23:38:45 GMT  
		Size: 82.4 KB (82372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d3233692d06b58a5c2a997b62411dd2922e73826a8330abba28784bbfde1742`  
		Last Modified: Tue, 28 May 2024 23:38:45 GMT  
		Size: 19.4 KB (19369 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.20` - linux; s390x

```console
$ docker pull memcached@sha256:43ea726a69d7aa19d38600a6b0c98114eac30a3f70d46c14f55746d508773378
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4551268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4218baf28d875e94ee50ce255b26888caf5671d153bb189ac30bebcc6635843b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_VERSION=1.6.27
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.27.tar.gz
# Wed, 22 May 2024 18:54:12 GMT
ENV MEMCACHED_SHA1=baf2e7494e1f62d275ff29a99f270abbdb923f75
# Wed, 22 May 2024 18:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 22 May 2024 18:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 18:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 May 2024 18:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 18:54:12 GMT
USER memcache
# Wed, 22 May 2024 18:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 22 May 2024 18:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bda8f56f465ce0440892acfd910a54a797991e554b31b96388ad100cb8dd18c`  
		Last Modified: Thu, 23 May 2024 03:19:15 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9810404860e30f64bc35f99f5cc930c953fa654ed2da190a4f4adf46c3914ea`  
		Last Modified: Thu, 23 May 2024 03:19:15 GMT  
		Size: 112.7 KB (112736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436abf7c43bfae37e20b0ae2fdaafa8c0165c2bbfcfd1242cd0ed17c846fdda4`  
		Last Modified: Thu, 23 May 2024 03:19:15 GMT  
		Size: 976.8 KB (976829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a62044b74bd7a363ba1ebba030952851d221ab43ab666a8bd59960ca5c76e9`  
		Last Modified: Thu, 23 May 2024 03:19:15 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc10b1e30c81f41f9d4012eda90ae84cfd53312c55770b504774fe80b5ba3ce`  
		Last Modified: Thu, 23 May 2024 03:19:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:5d3ab77f58725536e38b01d6e4bd4532e7bfa6cf7bd9eac35e77a4b70c8b8402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.6 KB (101615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd8bbbe1c27095d48770c6007e70e45c80a7c382286aaababe2fc83010d5fdda`

```dockerfile
```

-	Layers:
	-	`sha256:ea5bb003c385255e2e282399fe22ce79290bf682bb186d9a3901082902cc5d57`  
		Last Modified: Thu, 23 May 2024 03:19:15 GMT  
		Size: 82.3 KB (82314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb3910214e4a01e12528ebb507acafe782392af9209e1928be56b58e352cf7e1`  
		Last Modified: Thu, 23 May 2024 03:19:15 GMT  
		Size: 19.3 KB (19301 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:bookworm`

```console
$ docker pull memcached@sha256:58225aeaf238b8d6ca5b0c7cfc7cb81f44cdebd1ca184f032478cf4470c89520
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
$ docker pull memcached@sha256:3a548271d024b9f019806f9c57ab0c78b12721b99161b37c5fa1a54871aa4f1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32335604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58e4157cda75177132acadaa737dcc4ffbf23b3f4821d0948b4f9b882e606d2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 May 2024 09:14:35 GMT
ADD file:a92da94a28279478b2eae11dcdcd2913fc06af02498a5515cc3f288668d74e43 in / 
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
	-	`sha256:6ccc6628d3cdcda935b3b60cb54fa578d669965454d9cf39de3df9c1276132b7`  
		Last Modified: Tue, 14 May 2024 01:22:19 GMT  
		Size: 29.1 MB (29143688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ee82bdcb1e3a635fe9f1d5352d366d13d345f09eb3adfca8c9cdac667f12d4`  
		Last Modified: Tue, 14 May 2024 21:39:45 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6772b6152d32070d1bd037b4d40168112ccbe96e562d2b44c4be24a5f01f9b`  
		Last Modified: Tue, 14 May 2024 21:39:45 GMT  
		Size: 1.9 MB (1937746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833a7d6af8137233d7ad16026d9b1e1439a875762d4d0300c5b8fad018adba6b`  
		Last Modified: Tue, 14 May 2024 21:39:45 GMT  
		Size: 1.3 MB (1252656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdcc9953d5a8982f1bda95e99618eb60ce77f306601a4bd87e2b7032f58158fd`  
		Last Modified: Tue, 14 May 2024 21:39:45 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90055ed64046ecc2a6b606da0a99148b1b1006371fb88ea34d8116628aae47f3`  
		Last Modified: Tue, 14 May 2024 21:39:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:f17b6790b9c5b13d08059746553cd24795e4578c706cccada105ade01f3e16b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f05a4b82f72ff2643271e6710a1abb766fe5fbc715a018cabf4045f9cb137aa8`

```dockerfile
```

-	Layers:
	-	`sha256:57f1868b984b0196002a8a186c5ac8833f8eee2db97961c5355b4da6684b0fa4`  
		Last Modified: Tue, 14 May 2024 21:39:45 GMT  
		Size: 20.9 KB (20861 bytes)  
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
$ docker pull memcached@sha256:58225aeaf238b8d6ca5b0c7cfc7cb81f44cdebd1ca184f032478cf4470c89520
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
$ docker pull memcached@sha256:3a548271d024b9f019806f9c57ab0c78b12721b99161b37c5fa1a54871aa4f1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32335604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58e4157cda75177132acadaa737dcc4ffbf23b3f4821d0948b4f9b882e606d2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 06 May 2024 09:14:35 GMT
ADD file:a92da94a28279478b2eae11dcdcd2913fc06af02498a5515cc3f288668d74e43 in / 
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
	-	`sha256:6ccc6628d3cdcda935b3b60cb54fa578d669965454d9cf39de3df9c1276132b7`  
		Last Modified: Tue, 14 May 2024 01:22:19 GMT  
		Size: 29.1 MB (29143688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ee82bdcb1e3a635fe9f1d5352d366d13d345f09eb3adfca8c9cdac667f12d4`  
		Last Modified: Tue, 14 May 2024 21:39:45 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6772b6152d32070d1bd037b4d40168112ccbe96e562d2b44c4be24a5f01f9b`  
		Last Modified: Tue, 14 May 2024 21:39:45 GMT  
		Size: 1.9 MB (1937746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833a7d6af8137233d7ad16026d9b1e1439a875762d4d0300c5b8fad018adba6b`  
		Last Modified: Tue, 14 May 2024 21:39:45 GMT  
		Size: 1.3 MB (1252656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdcc9953d5a8982f1bda95e99618eb60ce77f306601a4bd87e2b7032f58158fd`  
		Last Modified: Tue, 14 May 2024 21:39:45 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90055ed64046ecc2a6b606da0a99148b1b1006371fb88ea34d8116628aae47f3`  
		Last Modified: Tue, 14 May 2024 21:39:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:f17b6790b9c5b13d08059746553cd24795e4578c706cccada105ade01f3e16b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f05a4b82f72ff2643271e6710a1abb766fe5fbc715a018cabf4045f9cb137aa8`

```dockerfile
```

-	Layers:
	-	`sha256:57f1868b984b0196002a8a186c5ac8833f8eee2db97961c5355b4da6684b0fa4`  
		Last Modified: Tue, 14 May 2024 21:39:45 GMT  
		Size: 20.9 KB (20861 bytes)  
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
