## `memcached:1-trixie`

```console
$ docker pull memcached@sha256:29eba63ee0af98db655b9fb873e679574bf0d5b6e1decb885154e3a980168fa9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `memcached:1-trixie` - linux; amd64

```console
$ docker pull memcached@sha256:6d46ecdfd0090b4f8b673739b5a1ce5e78fa20165409956597ccb68f5505574c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32194033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a2a78bcff2aaf4de0598b04deee534ff793472bd4a36a0408d612deca517825`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:22:40 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 16 Mar 2026 22:22:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:25:30 GMT
ENV MEMCACHED_VERSION=1.6.41
# Mon, 16 Mar 2026 22:25:30 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Mon, 16 Mar 2026 22:25:30 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Mon, 16 Mar 2026 22:25:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 16 Mar 2026 22:25:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:25:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 16 Mar 2026 22:25:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:25:30 GMT
USER memcache
# Mon, 16 Mar 2026 22:25:30 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 16 Mar 2026 22:25:30 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51dec6de03b12d48b6e37e129bf944eb70106232c9c31aa781758ae3be52655d`  
		Last Modified: Mon, 16 Mar 2026 22:25:36 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a929ea558d43c2be506e230ad805b5adef4bf3f5f88bf66ad5b2727e0ca9d1`  
		Last Modified: Mon, 16 Mar 2026 22:25:36 GMT  
		Size: 136.7 KB (136730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f4f23b254ea0054ead0b784ade91733c48651e2df47ee40d1d9b58dfb5f8b7`  
		Last Modified: Mon, 16 Mar 2026 22:25:36 GMT  
		Size: 2.3 MB (2280291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae38152dcb81b9fc27b02b3956d0a79bf99146330c0059679182f3e87dd7274`  
		Last Modified: Mon, 16 Mar 2026 22:25:36 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e839fccf18799779cb3d9a6d3f372c405e1e9372c16ec3753fcba956bf03643a`  
		Last Modified: Mon, 16 Mar 2026 22:25:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:38d8384f999b6b108f56ed4d48009d55e75568e64e2fd61c01b42c04c3b62a3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8b033c954a420dec21ea6c3fb022335940fa380f5c6c2ffd4754168fa0dc913`

```dockerfile
```

-	Layers:
	-	`sha256:fbbe155c9b96b631a76a85282a3eee608bbf9d582a034107ac71bc77e8c51666`  
		Last Modified: Mon, 16 Mar 2026 22:25:36 GMT  
		Size: 2.0 MB (2008326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e545affe8959c6c9a06d8f3729f1e8cc598422c62d932fa60737c757dbb8c848`  
		Last Modified: Mon, 16 Mar 2026 22:25:36 GMT  
		Size: 22.2 KB (22152 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; arm variant v5

```console
$ docker pull memcached@sha256:1060f3e562b5b0b9d3e127a989fc5728a81afccbf1117cd1ff1f36d3469f7068
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30300802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a8dbc51f521b81c2fdd453cc87123f780cf3cc2f6fd4b1f90e477cb23f2c0c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:19:22 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 16 Mar 2026 22:19:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:22:45 GMT
ENV MEMCACHED_VERSION=1.6.41
# Mon, 16 Mar 2026 22:22:45 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Mon, 16 Mar 2026 22:22:45 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Mon, 16 Mar 2026 22:22:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 16 Mar 2026 22:22:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:22:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 16 Mar 2026 22:22:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:22:45 GMT
USER memcache
# Mon, 16 Mar 2026 22:22:45 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 16 Mar 2026 22:22:45 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:eb1defba38d0de4655b895d4763345b3ab078983d3385db43c308a7caca13f2a`  
		Last Modified: Mon, 16 Mar 2026 21:52:26 GMT  
		Size: 27.9 MB (27943649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db033ebb8ef7277a324802ac3af8fe266c9d8785753e8b72283d7734f7a0eea`  
		Last Modified: Mon, 16 Mar 2026 22:22:51 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f11597c0aea99294d829a37458f4c41c93d810184c13c9c90752073a110d8c7`  
		Last Modified: Mon, 16 Mar 2026 22:22:51 GMT  
		Size: 144.2 KB (144203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05264a3583989736fa7c559a92b64fecf66ed5349fe813be1b77e94376f27710`  
		Last Modified: Mon, 16 Mar 2026 22:22:51 GMT  
		Size: 2.2 MB (2211441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e56e9fcdf6bc8c8471665ec5541c17ebc6a7b4a69804244b8579b46a9ad9487a`  
		Last Modified: Mon, 16 Mar 2026 22:22:51 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:902de232bd661982336b45644e0ee65fcffa5e60d7d132201480a6f539b4a7f9`  
		Last Modified: Mon, 16 Mar 2026 22:22:52 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:cbb894e85c7970959a8b7b65ee2f9237026b80818759d1576c1f803d35ea1e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2033633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d30e6e572ff6c3aea212651d025f001432d16ec598c8b9bae58ce2f3beb3810`

```dockerfile
```

-	Layers:
	-	`sha256:9d762415821f7f0b20d9d65a63c86ddc752a356a1b120a7d45ea4a744bb1348d`  
		Last Modified: Mon, 16 Mar 2026 22:22:52 GMT  
		Size: 2.0 MB (2011329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8edfce16a506939813af6d178eea3dbe35843219fcbb358ebaf3f1184e5ca02b`  
		Last Modified: Mon, 16 Mar 2026 22:22:51 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; arm variant v7

```console
$ docker pull memcached@sha256:1214688b707989bb7358a0bd6930bcfc31d1336418801e904e215c732a6b347d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28511389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d91a496e0673f0345e79a0e84cc6b56b737063a893008dfb2b1971f2231152a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:20:12 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 16 Mar 2026 22:20:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:23:22 GMT
ENV MEMCACHED_VERSION=1.6.41
# Mon, 16 Mar 2026 22:23:22 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Mon, 16 Mar 2026 22:23:22 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Mon, 16 Mar 2026 22:23:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 16 Mar 2026 22:23:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:23:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 16 Mar 2026 22:23:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:23:22 GMT
USER memcache
# Mon, 16 Mar 2026 22:23:22 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 16 Mar 2026 22:23:22 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7d73604d2a042e7beeb809f68c76f5be3576747809bfaa49747f334227d8d250`  
		Last Modified: Mon, 16 Mar 2026 21:53:24 GMT  
		Size: 26.2 MB (26209505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f133d58a3556da32e20643b7a0299634be0a0967f7f9663c0bf9c8e1e972890b`  
		Last Modified: Mon, 16 Mar 2026 22:23:28 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee9c4c1f4d54e8ae2ee1ed2c8b138ceb7688d05e0836115d1c2095d6f4a2e2b0`  
		Last Modified: Mon, 16 Mar 2026 22:23:28 GMT  
		Size: 135.4 KB (135402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad390241e99df8490326105bc4e801cc54fe7593f2719fc614a3e4ed27a486bb`  
		Last Modified: Mon, 16 Mar 2026 22:23:28 GMT  
		Size: 2.2 MB (2164972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f624a504b021302ec1c4c2c4e2305e05aeb5c050875a81094db8adf29e51d4`  
		Last Modified: Mon, 16 Mar 2026 22:23:28 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37111b7437173b3ae8c9e27bc5baef87758893d4d48711f0782e041d6207aa30`  
		Last Modified: Mon, 16 Mar 2026 22:23:29 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:ec97a7b968bd818cfe39da8becb2ff707220aba15a5e445c0d3d1b1f3235d998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a6fbc399cfa8cc27226ef0c80eeed2780ebfa12f4beb2ebbfecc4374d83d5fb`

```dockerfile
```

-	Layers:
	-	`sha256:620c6d213ac9b2cf60a4719409df59f158024147f48c66cc6209eedf96331297`  
		Last Modified: Mon, 16 Mar 2026 22:23:28 GMT  
		Size: 2.0 MB (2009786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48ac46c64271289f1f8134bcabb4ad9e28ca565245587690dce9b0b91a936ad0`  
		Last Modified: Mon, 16 Mar 2026 22:23:28 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:58436e8d59397bb6e9436a0d2fbcc5692b48f480a24509a936163639aa54fe38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32555536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:691a0a8d6f7273979268d2b094bc7c9bd13654934ec74093fcd72e3739ca3f3b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:22:20 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 16 Mar 2026 22:22:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:25:23 GMT
ENV MEMCACHED_VERSION=1.6.41
# Mon, 16 Mar 2026 22:25:23 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Mon, 16 Mar 2026 22:25:23 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Mon, 16 Mar 2026 22:25:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 16 Mar 2026 22:25:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:25:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 16 Mar 2026 22:25:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:25:23 GMT
USER memcache
# Mon, 16 Mar 2026 22:25:23 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 16 Mar 2026 22:25:23 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c730847c672f0d7f17833eadd2702505a2a07083e1ec29272d7cc97db7f3441`  
		Last Modified: Mon, 16 Mar 2026 22:25:28 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c414c93f8626bc36953c3aa002dee7f28c945c86314ae648864a0269e17ac3`  
		Last Modified: Mon, 16 Mar 2026 22:25:28 GMT  
		Size: 153.6 KB (153551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f236f75c716473c2c52b21eb61bac9981e46be653f672a943a12a64e2430dd46`  
		Last Modified: Mon, 16 Mar 2026 22:25:29 GMT  
		Size: 2.3 MB (2262059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:678589fbeff3b1343f6dd1d56db402ba5363d65935600b2318039b966bd992bb`  
		Last Modified: Mon, 16 Mar 2026 22:25:28 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec29d0375b58d00984704a65d1214ae47ae0524d3d1ec80fb09d68a2e29c4a42`  
		Last Modified: Mon, 16 Mar 2026 22:25:29 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:5ada12a147ee33f7c2ba122096b7cac6b81a0458416273ff560e014dd646436b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2801d895649241fe4b96c16ce3a25e34eb24a7ee2959b592ad2236249f62d023`

```dockerfile
```

-	Layers:
	-	`sha256:d8898537067441a32256330fe45db9dc0ab1a70d05df680826dbb1a48b320384`  
		Last Modified: Mon, 16 Mar 2026 22:25:29 GMT  
		Size: 2.0 MB (2008642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38dedfa7e35a11270e82ea60e23d3bbc94e8a9b957fa44d2e4ac69eb1f44a600`  
		Last Modified: Mon, 16 Mar 2026 22:25:28 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; 386

```console
$ docker pull memcached@sha256:e3dca3c5fc8743d2348e85762f057dabf8ce4f1bd3d77ae718700a18fb04703b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33664968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:193f591d78fd73d0ae2ccc1446402c0a969106e5d9a099d383d0a4ee9b7f6292`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:18:39 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 16 Mar 2026 22:18:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:21:42 GMT
ENV MEMCACHED_VERSION=1.6.41
# Mon, 16 Mar 2026 22:21:42 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Mon, 16 Mar 2026 22:21:42 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Mon, 16 Mar 2026 22:21:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 16 Mar 2026 22:21:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:21:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 16 Mar 2026 22:21:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:21:42 GMT
USER memcache
# Mon, 16 Mar 2026 22:21:42 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 16 Mar 2026 22:21:42 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2c0c3f3238f3d4cecd93e4dee6eda788943ef955de61c3ad4ff659da1f43ba60`  
		Last Modified: Mon, 16 Mar 2026 21:53:39 GMT  
		Size: 31.3 MB (31291132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b10e0f26b8a969983ebd8a480ae6e4ac0c8be9495d9c0e44093b22af1d6f6334`  
		Last Modified: Mon, 16 Mar 2026 22:21:48 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5abd1189e44a7e57d8fc431d81af9733d21f6c425486db0fc32ff208c42247`  
		Last Modified: Mon, 16 Mar 2026 22:21:48 GMT  
		Size: 147.6 KB (147571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f18540f18189ea187e56bdd8fc494d808568ca701fd828de3636d8694a5354f5`  
		Last Modified: Mon, 16 Mar 2026 22:21:48 GMT  
		Size: 2.2 MB (2224758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0747835fbac2978a1f971e8fbdc54e0321db24cae27e2ebef7fd271c4e9f3be4`  
		Last Modified: Mon, 16 Mar 2026 22:21:48 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0bcc6a55fba43e4c34d3ac61b1731378a47c5a7a5632988822f1dbf3cd193d`  
		Last Modified: Mon, 16 Mar 2026 22:21:49 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:724f8fe9a17be240c671130ba7e6d1b9da3f3e028514daf5d7066bbe3151ad24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26ae2fdc4470449d320644a0f3254daae8ec7266753b90371fda0de47b458cef`

```dockerfile
```

-	Layers:
	-	`sha256:7060a534a1753c1338cf02e9ccc44552f44bd97c1ba5f03aa4f7e99f08446f98`  
		Last Modified: Mon, 16 Mar 2026 22:21:48 GMT  
		Size: 2.0 MB (2005483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2415bc4c60cfd98b1bd6b5d31b4a561f48a0bc18dbbf383e2cbe018a6b96a0f8`  
		Last Modified: Mon, 16 Mar 2026 22:21:48 GMT  
		Size: 22.1 KB (22095 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; ppc64le

```console
$ docker pull memcached@sha256:ffac94778c7c882a7f2cbaae5af33e755639de207d07834e052412c2b22a24b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36754462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5640d71fb49b8eaef07631709a9f4924bd191fcfe9b44b7df2d525e247075b64`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Sat, 07 Mar 2026 00:33:31 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Sat, 07 Mar 2026 00:33:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Mar 2026 00:56:42 GMT
ENV MEMCACHED_VERSION=1.6.41
# Sat, 07 Mar 2026 00:56:42 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Sat, 07 Mar 2026 00:56:42 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Sat, 07 Mar 2026 00:56:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Sat, 07 Mar 2026 00:56:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Mar 2026 00:56:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Mar 2026 00:56:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Mar 2026 00:56:44 GMT
USER memcache
# Sat, 07 Mar 2026 00:56:44 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Mar 2026 00:56:44 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab70996aa4a561e7f3e1f1e1b14df7912a1456b20b317937391cfa826c93f2ea`  
		Last Modified: Sat, 07 Mar 2026 00:57:10 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1ba00921effa53d91205ba3e5e3280c719885f49b5e9e0f8e2a387cf316d89`  
		Last Modified: Sat, 07 Mar 2026 00:57:10 GMT  
		Size: 170.4 KB (170386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd00738358190677470eca91b6732f6fcc475639b7f07f1943af6f5d268ae47`  
		Last Modified: Sat, 07 Mar 2026 00:57:10 GMT  
		Size: 3.0 MB (2982343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f7dc97a8f5d8c677e24bd2f8014c3e315619d726d409033dc3ce4f6d7d7569d`  
		Last Modified: Sat, 07 Mar 2026 00:57:10 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f2b48241128f09e1c613b0fb34d37f79c77417d033b7a00041f8cd08d6241f`  
		Last Modified: Sat, 07 Mar 2026 00:57:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:da557c745e92be8dd35823b9c24b79e47c55ff727768980abe9b659a14672408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e89b8bba62432d49e11baad935eddf449853276e5bb492953ae6bb995bf81ef`

```dockerfile
```

-	Layers:
	-	`sha256:7bf94ead3bca06412117cdc5395bde9d799ffc799dd28be779209634f64bfc0b`  
		Last Modified: Sat, 07 Mar 2026 00:57:10 GMT  
		Size: 2.0 MB (2011891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ec351466954789ecb039e735ecf9fd0235d5d4cfcf8bd6bcf2cf68049016c1c`  
		Last Modified: Sat, 07 Mar 2026 00:57:10 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; riscv64

```console
$ docker pull memcached@sha256:ccac0e143b4efd5bd15fb67df5ad87f5b743cc3db826cbb27d1874cbb3b6d549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30619564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f9320af1aa6fbbae22f81ef28d68694abc001739c71a195b4b1cd490b3b9107`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 23:50:36 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 09 Mar 2026 23:51:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Mar 2026 00:09:03 GMT
ENV MEMCACHED_VERSION=1.6.41
# Tue, 10 Mar 2026 00:09:03 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Tue, 10 Mar 2026 00:09:03 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Tue, 10 Mar 2026 00:09:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Tue, 10 Mar 2026 00:09:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 10 Mar 2026 00:09:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 10 Mar 2026 00:09:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Mar 2026 00:09:03 GMT
USER memcache
# Tue, 10 Mar 2026 00:09:03 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 10 Mar 2026 00:09:03 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e1366b1f74881f04901f31cfdecf9f3f5d4794ebf89911083a239bf462bf21`  
		Last Modified: Tue, 10 Mar 2026 00:09:56 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918782f8ab4ae7fe2ab9f1fc0aa7ad4e48d83dc362a4dcac336048ded3de9b6e`  
		Last Modified: Tue, 10 Mar 2026 00:09:56 GMT  
		Size: 133.1 KB (133079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963fbe1d00657987e81bdc270499ad5aacf8f91b100915c30ddf9fc57cd67346`  
		Last Modified: Tue, 10 Mar 2026 00:09:56 GMT  
		Size: 2.2 MB (2208551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729657786193241c665df2cbaeb72b5d157865abb3bbd8b9460e88d08fb65fea`  
		Last Modified: Tue, 10 Mar 2026 00:09:56 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8246f12fbc1ee94790a418b9655df55d80968171273b5994aaffa40c04fa2f3c`  
		Last Modified: Tue, 10 Mar 2026 00:09:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:de9f0d80a354763898649af4229a6f696fb51689e3b577af2e1d918d365777e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2024481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d72c30b80e1c2deaee38b267b52cab1a28e245b2a3608fcf459f2232dad3faa7`

```dockerfile
```

-	Layers:
	-	`sha256:03d9f11a7e8cf93ffe1f13ecfd86632a66af5a6efc142ae7a4ecac0c19418b2d`  
		Last Modified: Tue, 10 Mar 2026 00:09:56 GMT  
		Size: 2.0 MB (2002254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:452e3f764b5054c447aa8e63046155a20784d6f10159282ce633afdb79bf9279`  
		Last Modified: Tue, 10 Mar 2026 00:09:56 GMT  
		Size: 22.2 KB (22227 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-trixie` - linux; s390x

```console
$ docker pull memcached@sha256:fdb7b272e0205d5e590b1b8c6cd153b5038c1e135578ff5bce4ee4f2e37e2436
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32275568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:512cb6536a24321805cd46ad212ed6ec000e59862e3bf90829b2ea944fef3013`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:19:50 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 16 Mar 2026 22:19:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:23:09 GMT
ENV MEMCACHED_VERSION=1.6.41
# Mon, 16 Mar 2026 22:23:09 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.41.tar.gz
# Mon, 16 Mar 2026 22:23:09 GMT
ENV MEMCACHED_SHA1=2a54497623f2f18971963345063b54446c8ec85a
# Mon, 16 Mar 2026 22:23:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc" || make test; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 16 Mar 2026 22:23:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:23:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 16 Mar 2026 22:23:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:23:10 GMT
USER memcache
# Mon, 16 Mar 2026 22:23:10 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 16 Mar 2026 22:23:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2c02a3d3f135c4bbe56488921bd86d969a76dcd5278abca1e81884d3bff0bd88`  
		Last Modified: Mon, 16 Mar 2026 21:52:55 GMT  
		Size: 29.8 MB (29835265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:778c3a0c2956b23abf2285c61253f94bf271f5598c204a48f295ce80131e2267`  
		Last Modified: Mon, 16 Mar 2026 22:23:21 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2108d78694e4eca215a2ca06ae28226d5cd1dd44402e98ad22061d3362b988a`  
		Last Modified: Mon, 16 Mar 2026 22:23:21 GMT  
		Size: 140.6 KB (140570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5b788ca40dcf2f66bcd97896df0f15738710039e8bcfd3d737cf6b58edaffb`  
		Last Modified: Mon, 16 Mar 2026 22:23:22 GMT  
		Size: 2.3 MB (2298223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e8f47da05530da0ccdd91e5c08651b2af04dd1bf17c27e54865c4a03bdb723`  
		Last Modified: Mon, 16 Mar 2026 22:23:21 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fdc39295ddbeab9b46d8e0222a78c03a63d733e7b9b2c606ab01bea8cc99a93`  
		Last Modified: Mon, 16 Mar 2026 22:23:22 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-trixie` - unknown; unknown

```console
$ docker pull memcached@sha256:50f6faf6b82f442f284b88f856c799250416a375b7ed35c4d39ddcd99f9fff2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffb51d687889e1e19aa123ca50786ba0192fb7a7f0862e8b884c4bc6fa8d0fef`

```dockerfile
```

-	Layers:
	-	`sha256:8612e895a2ea6b146843022582e5c0a02e2d4399c8c2d6f865d3a806627f1ecf`  
		Last Modified: Mon, 16 Mar 2026 22:23:21 GMT  
		Size: 2.0 MB (2009763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2905b734fce4bd5dabaecc27efd097dc7467480edfbbc53ea2b614e95d7be094`  
		Last Modified: Mon, 16 Mar 2026 22:23:21 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.in-toto+json
