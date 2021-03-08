<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `haproxy`

-	[`haproxy:1.7`](#haproxy17)
-	[`haproxy:1.7.12`](#haproxy1712)
-	[`haproxy:1.7.12-alpine`](#haproxy1712-alpine)
-	[`haproxy:1.7-alpine`](#haproxy17-alpine)
-	[`haproxy:1.8`](#haproxy18)
-	[`haproxy:1.8.28`](#haproxy1828)
-	[`haproxy:1.8.28-alpine`](#haproxy1828-alpine)
-	[`haproxy:1.8-alpine`](#haproxy18-alpine)
-	[`haproxy:2.0`](#haproxy20)
-	[`haproxy:2.0.20`](#haproxy2020)
-	[`haproxy:2.0.20-alpine`](#haproxy2020-alpine)
-	[`haproxy:2.0-alpine`](#haproxy20-alpine)
-	[`haproxy:2.1`](#haproxy21)
-	[`haproxy:2.1.11`](#haproxy2111)
-	[`haproxy:2.1.11-alpine`](#haproxy2111-alpine)
-	[`haproxy:2.1-alpine`](#haproxy21-alpine)
-	[`haproxy:2.2`](#haproxy22)
-	[`haproxy:2.2.10`](#haproxy2210)
-	[`haproxy:2.2.10-alpine`](#haproxy2210-alpine)
-	[`haproxy:2.2-alpine`](#haproxy22-alpine)
-	[`haproxy:2.3`](#haproxy23)
-	[`haproxy:2.3.6`](#haproxy236)
-	[`haproxy:2.3.6-alpine`](#haproxy236-alpine)
-	[`haproxy:2.3-alpine`](#haproxy23-alpine)
-	[`haproxy:2.4-dev`](#haproxy24-dev)
-	[`haproxy:2.4-dev11`](#haproxy24-dev11)
-	[`haproxy:2.4-dev11-alpine`](#haproxy24-dev11-alpine)
-	[`haproxy:2.4-dev-alpine`](#haproxy24-dev-alpine)
-	[`haproxy:alpine`](#haproxyalpine)
-	[`haproxy:latest`](#haproxylatest)
-	[`haproxy:lts`](#haproxylts)
-	[`haproxy:lts-alpine`](#haproxylts-alpine)

## `haproxy:1.7`

```console
$ docker pull haproxy@sha256:edc8c85a94789541774f039506cf8a89bed539537472785be53eb77054240fd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `haproxy:1.7` - linux; amd64

```console
$ docker pull haproxy@sha256:119b805973c071e774718868244cbceed376f18e9531771609a8044f59e870ce
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32474286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3d3b72953731b55b715f8fb0fc7718468f5afc4ecf2c3c83c6fe40517cb9d87`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Mon, 08 Mar 2021 21:37:25 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 21:50:53 GMT
ENV HAPROXY_VERSION=1.7.12
# Mon, 08 Mar 2021 21:50:53 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.7/src/haproxy-1.7.12.tar.gz
# Mon, 08 Mar 2021 21:50:53 GMT
ENV HAPROXY_SHA256=4118178b553a107b227f3f84774c7a50ae0b3ac2be39211c3db511ed4efe48ce
# Mon, 08 Mar 2021 21:51:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 08 Mar 2021 21:51:24 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 21:51:25 GMT
COPY file:9a05f2c8b43e780abf69d813f7c45613cced5481a65611bf8127c6f222dff4e3 in /usr/local/bin/ 
# Mon, 08 Mar 2021 21:51:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 08 Mar 2021 21:51:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 21:51:26 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7bca45a971fe608786870ce75c9976f8e5a958f55e1287a6120048b897c63b6`  
		Last Modified: Mon, 08 Mar 2021 21:52:33 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:354c55b6a82a8a9e6925c42d24ed2d51daebff99990e70923a5d02e68e2d0d9d`  
		Last Modified: Mon, 08 Mar 2021 21:55:27 GMT  
		Size: 5.4 MB (5377174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b93fc6908cdb503cf2286f0940b339c4045f2808904a2d8e5e62c6117ecc1d7`  
		Last Modified: Mon, 08 Mar 2021 21:55:29 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c188b46dbd38eb9c0ec85c577bddad66dc38bd7200293c7b9a595552ed6d33f3`  
		Last Modified: Mon, 08 Mar 2021 21:55:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.7` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:8a19cad8062d4496d5c4b120b8e1af4c6c4166ffa81287983e2ee7b5cf8b061e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.9 MB (29850083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fae256b6443bbb3e0a9ee6b9a5904622e3302be9e7ed830d62bce7276850cca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:50:10 GMT
ADD file:fbd00ef7871dc27d7ed5fa8c238cdc80652bd87b8033be7de9e54a799bbf10a4 in / 
# Tue, 09 Feb 2021 02:50:11 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:45:24 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 09 Feb 2021 03:53:29 GMT
ENV HAPROXY_VERSION=1.7.12
# Tue, 09 Feb 2021 03:53:30 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.7/src/haproxy-1.7.12.tar.gz
# Tue, 09 Feb 2021 03:53:32 GMT
ENV HAPROXY_SHA256=4118178b553a107b227f3f84774c7a50ae0b3ac2be39211c3db511ed4efe48ce
# Tue, 09 Feb 2021 03:54:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 09 Feb 2021 03:54:23 GMT
STOPSIGNAL SIGUSR1
# Tue, 09 Feb 2021 03:54:24 GMT
COPY file:9a05f2c8b43e780abf69d813f7c45613cced5481a65611bf8127c6f222dff4e3 in /usr/local/bin/ 
# Tue, 09 Feb 2021 03:54:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 09 Feb 2021 03:54:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Feb 2021 03:54:28 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:8e683fcc73f4da7d69ce1d5f4e1d77510aa459490068f38db2d8663698b391a0`  
		Last Modified: Tue, 09 Feb 2021 02:59:07 GMT  
		Size: 24.8 MB (24839297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def565d52deae74587a55f60d168bd531ebe8095c594027b7057a8fc1be0e8af`  
		Last Modified: Tue, 09 Feb 2021 03:54:54 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caccfbe89a6a82d7d11c0a5dd3e17f117553ba0647d31074847b69f997dba830`  
		Last Modified: Tue, 09 Feb 2021 03:55:58 GMT  
		Size: 5.0 MB (5008822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8a51ed81a112128f089c2f53ef3c66006457dd42aeb83a7fadb2ef8d123197c`  
		Last Modified: Tue, 09 Feb 2021 03:55:57 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8366cfe41f6e14fde9dd452961959c91b9c887d116fc99650686a057115bc8c2`  
		Last Modified: Tue, 09 Feb 2021 03:55:56 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.7` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:236f09c8276a0e3db3b5f8689c5bc48102fc2b4901fef551e77ddec1cb862ec6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27580523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11f450811f965ef7a87c7175122b79e6ee8202139d8173c5c509cede1ee2ecf5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 03:00:57 GMT
ADD file:e675d50366bde57173a75f9a29367d765e7da2b7254c5254b64e777cf6870502 in / 
# Tue, 09 Feb 2021 03:01:00 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:49:38 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 09 Feb 2021 03:56:40 GMT
ENV HAPROXY_VERSION=1.7.12
# Tue, 09 Feb 2021 03:56:40 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.7/src/haproxy-1.7.12.tar.gz
# Tue, 09 Feb 2021 03:56:41 GMT
ENV HAPROXY_SHA256=4118178b553a107b227f3f84774c7a50ae0b3ac2be39211c3db511ed4efe48ce
# Tue, 09 Feb 2021 03:57:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 09 Feb 2021 03:57:26 GMT
STOPSIGNAL SIGUSR1
# Tue, 09 Feb 2021 03:57:27 GMT
COPY file:9a05f2c8b43e780abf69d813f7c45613cced5481a65611bf8127c6f222dff4e3 in /usr/local/bin/ 
# Tue, 09 Feb 2021 03:57:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 09 Feb 2021 03:57:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Feb 2021 03:57:32 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:db574d82360c3b60abadbef4f3daf8dee01f24741fc6ab3692aa543558d8b624`  
		Last Modified: Tue, 09 Feb 2021 03:09:46 GMT  
		Size: 22.7 MB (22703384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9978ebb1881387f11e025fb46dce2b3c715f705f6d240737574f8848c27fa0d7`  
		Last Modified: Tue, 09 Feb 2021 03:58:16 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0904496d6669d3035ee4f76e1cd26236e719ad332d797e9749a9f27d47bc727`  
		Last Modified: Tue, 09 Feb 2021 03:59:23 GMT  
		Size: 4.9 MB (4875174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20757dd7dc51d07bf4f6a5df48f6859aa9643759b7fde9f458b8769e2de807da`  
		Last Modified: Tue, 09 Feb 2021 03:59:22 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f3c6212281f061ceed1955d145170500f89f7224d83fd9b29bbb50b04b29272`  
		Last Modified: Tue, 09 Feb 2021 03:59:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.7` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:d5eba597a791cb44dff0e436d4bdaa4846fe49779b2826361b61dff6475e40f7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31117578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9461f8882da335f0ac2efa06d4dc7150740c33013ba3111a6962d177cfa11064`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:41:10 GMT
ADD file:d906dedaf14d8e3874b46787f7a1dbf268bc124c4e1dd32f13f3079e12f22238 in / 
# Tue, 09 Feb 2021 02:41:13 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:59:41 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 09 Feb 2021 04:06:57 GMT
ENV HAPROXY_VERSION=1.7.12
# Tue, 09 Feb 2021 04:06:57 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.7/src/haproxy-1.7.12.tar.gz
# Tue, 09 Feb 2021 04:06:58 GMT
ENV HAPROXY_SHA256=4118178b553a107b227f3f84774c7a50ae0b3ac2be39211c3db511ed4efe48ce
# Tue, 09 Feb 2021 04:07:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 09 Feb 2021 04:07:42 GMT
STOPSIGNAL SIGUSR1
# Tue, 09 Feb 2021 04:07:43 GMT
COPY file:9a05f2c8b43e780abf69d813f7c45613cced5481a65611bf8127c6f222dff4e3 in /usr/local/bin/ 
# Tue, 09 Feb 2021 04:07:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 09 Feb 2021 04:07:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Feb 2021 04:07:48 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:83c5cfdaa5385ea6fc4d31e724fd4dc5d74de847a7bdd968555b8f2c558dac0e`  
		Last Modified: Tue, 09 Feb 2021 02:47:27 GMT  
		Size: 25.9 MB (25851449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b7f43dd52365bce2c2b75f29577aa39d2b5794e2561cddc0678422ffc1f7d15`  
		Last Modified: Tue, 09 Feb 2021 04:08:36 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d8c3de44d1e105730b4f66b262320f4e31019ebfaa6d1f1eb768d66fd7d646`  
		Last Modified: Tue, 09 Feb 2021 04:09:42 GMT  
		Size: 5.3 MB (5264162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc6d37f3655455f3dc9079ef2c659e3355f5c2e7000384e0af351d04cc0f1f4`  
		Last Modified: Tue, 09 Feb 2021 04:09:41 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54c844a67c2c77fd99deee7dc9e27eb91911cd829b5a00c8454eca13a9b0b0e1`  
		Last Modified: Tue, 09 Feb 2021 04:09:41 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.7` - linux; 386

```console
$ docker pull haproxy@sha256:f244511b564a5138663e7a6c150e49e540d872b9ca119638179bfbe526bf25b1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.1 MB (33064521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06ac072a7db0c5bb4cb1d835623f9587a310b9ae97f1e9a95e80a07dbeceb403`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:39:47 GMT
ADD file:61c31b1037672781ed0ecbc080ee3d49c83af49f5578b011544513fa9625698d in / 
# Tue, 09 Feb 2021 02:39:47 GMT
CMD ["bash"]
# Mon, 08 Mar 2021 22:02:40 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 22:15:31 GMT
ENV HAPROXY_VERSION=1.7.12
# Mon, 08 Mar 2021 22:15:31 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.7/src/haproxy-1.7.12.tar.gz
# Mon, 08 Mar 2021 22:15:31 GMT
ENV HAPROXY_SHA256=4118178b553a107b227f3f84774c7a50ae0b3ac2be39211c3db511ed4efe48ce
# Mon, 08 Mar 2021 22:16:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 08 Mar 2021 22:16:02 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 22:16:03 GMT
COPY file:9a05f2c8b43e780abf69d813f7c45613cced5481a65611bf8127c6f222dff4e3 in /usr/local/bin/ 
# Mon, 08 Mar 2021 22:16:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 08 Mar 2021 22:16:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 22:16:04 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:27cbb00346a16ea900c1049a2e5b47942c586c377179e098382c8ca1c8e87966`  
		Last Modified: Tue, 09 Feb 2021 02:45:51 GMT  
		Size: 27.8 MB (27752731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b6129a97a33727ea8a598d1e797bccce491920bf29d769880cf2fc6d3e0436`  
		Last Modified: Mon, 08 Mar 2021 22:17:48 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e82c1d67749e4ed80b7c2276954c4d75034a6afab3df4937009d806b536c8239`  
		Last Modified: Mon, 08 Mar 2021 22:20:45 GMT  
		Size: 5.3 MB (5309827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf95b65335e441923a3ed713a5a92c79fdf48ab5d750598d4fa2df7924b95717`  
		Last Modified: Mon, 08 Mar 2021 22:20:45 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df53524c328ab022e092aafdb5d2f3dd23de98d3fbcbae684e7c215950c64a4`  
		Last Modified: Mon, 08 Mar 2021 22:20:41 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.7` - linux; mips64le

```console
$ docker pull haproxy@sha256:3f4a3ad46303d073d1632050c4498fdc9c00de00947eba4359cc1c433d727842
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 MB (30780167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5df41bdec068aca343ee488f5e79c308c5d34f94e766a051789cbe0e8bcb3476`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 03:09:26 GMT
ADD file:0222a151f4e5033d9eae98ce2b703a63f52d049dd72ac40bdd0dc2dafe619f0a in / 
# Tue, 09 Feb 2021 03:09:27 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:41:09 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 09 Feb 2021 03:55:59 GMT
ENV HAPROXY_VERSION=1.7.12
# Tue, 09 Feb 2021 03:55:59 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.7/src/haproxy-1.7.12.tar.gz
# Tue, 09 Feb 2021 03:55:59 GMT
ENV HAPROXY_SHA256=4118178b553a107b227f3f84774c7a50ae0b3ac2be39211c3db511ed4efe48ce
# Tue, 09 Feb 2021 03:57:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 09 Feb 2021 03:57:25 GMT
STOPSIGNAL SIGUSR1
# Tue, 09 Feb 2021 03:57:25 GMT
COPY file:9a05f2c8b43e780abf69d813f7c45613cced5481a65611bf8127c6f222dff4e3 in /usr/local/bin/ 
# Tue, 09 Feb 2021 03:57:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 09 Feb 2021 03:57:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Feb 2021 03:57:28 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:dfb81134097d874e01b495d1fba82e384056d0a3a45f01a69a2e86ae82af1e96`  
		Last Modified: Tue, 09 Feb 2021 03:15:55 GMT  
		Size: 25.8 MB (25764640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a549d56662447dd8cb15faf59ca0fc2eda7a877e9aee16aadd09fd46e4214a`  
		Last Modified: Tue, 09 Feb 2021 03:57:56 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b44bcf0254fd5eadcfa76c8d554eb8e3b3e20bb16dc5ba18b3b2eb9d3c2e42`  
		Last Modified: Tue, 09 Feb 2021 03:59:44 GMT  
		Size: 5.0 MB (5013558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a8a2d6ad64b59ceed1bbd3c436e54851d8a006294fda33bf2a53b3fb66cc7b`  
		Last Modified: Tue, 09 Feb 2021 03:59:41 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36ed3f7edc1954ab6f053036a2e7baab54b6dcaec38a11c3c6ef319d636a7f03`  
		Last Modified: Tue, 09 Feb 2021 03:59:41 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.7` - linux; ppc64le

```console
$ docker pull haproxy@sha256:db32dab977fd448211a6c17025e42abf9e18caab6063ba4961eb92a92bcd9873
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36215161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb7e2adda4f9e417354c0c51830a1f2ace23b9e809887dae1351d38d2aa22be6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:19:19 GMT
ADD file:9a8cfdf0eab394a693b5cde0700ad47b6e8506ef0b79fabb8a07874b96e6c394 in / 
# Tue, 09 Feb 2021 02:19:34 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 05:52:23 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 09 Feb 2021 06:31:35 GMT
ENV HAPROXY_VERSION=1.7.12
# Tue, 09 Feb 2021 06:31:43 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.7/src/haproxy-1.7.12.tar.gz
# Tue, 09 Feb 2021 06:31:48 GMT
ENV HAPROXY_SHA256=4118178b553a107b227f3f84774c7a50ae0b3ac2be39211c3db511ed4efe48ce
# Tue, 09 Feb 2021 06:37:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 09 Feb 2021 06:37:34 GMT
STOPSIGNAL SIGUSR1
# Tue, 09 Feb 2021 06:37:37 GMT
COPY file:9a05f2c8b43e780abf69d813f7c45613cced5481a65611bf8127c6f222dff4e3 in /usr/local/bin/ 
# Tue, 09 Feb 2021 06:37:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 09 Feb 2021 06:37:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Feb 2021 06:37:50 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:9996b4fb6bc1c50f95ba30f8988c9c89526556fa320d3fda59d3d8359f7810d6`  
		Last Modified: Tue, 09 Feb 2021 02:27:59 GMT  
		Size: 30.5 MB (30519509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7f600bc4989eb9f12d5006a73f5958eb4fe85f86bc4008d7a899bb935b0f1c`  
		Last Modified: Tue, 09 Feb 2021 06:38:36 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6deb7498d6b48c4e250d2ef780731517b82e52ca28b770c66185f53c198221af`  
		Last Modified: Tue, 09 Feb 2021 06:40:08 GMT  
		Size: 5.7 MB (5693685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b407e1fb599510b5a8f93dc9c92e47e18ee9a5b556ae7f977ae89d1415986d58`  
		Last Modified: Tue, 09 Feb 2021 06:40:07 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80356779393c7c2d00f0aa589123da6c877056c789d7f56f810bafd5cdb8c413`  
		Last Modified: Tue, 09 Feb 2021 06:40:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.7` - linux; s390x

```console
$ docker pull haproxy@sha256:60d0f1c28672e8206688f127bef30f1478f4ed4100525c2745e15cdd1dd89c83
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 MB (30821360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74cf1e00801d68b8718fac9fb4b05e0e91f6268f22dcab57d283ff87c724961a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:42:10 GMT
ADD file:0edb2de05df54191a141bd125f59d7e14eef0cc4576927a247b8dd7d6f255d04 in / 
# Tue, 09 Feb 2021 02:42:12 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:39:30 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 09 Feb 2021 03:43:32 GMT
ENV HAPROXY_VERSION=1.7.12
# Tue, 09 Feb 2021 03:43:33 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.7/src/haproxy-1.7.12.tar.gz
# Tue, 09 Feb 2021 03:43:33 GMT
ENV HAPROXY_SHA256=4118178b553a107b227f3f84774c7a50ae0b3ac2be39211c3db511ed4efe48ce
# Tue, 09 Feb 2021 03:43:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 09 Feb 2021 03:43:52 GMT
STOPSIGNAL SIGUSR1
# Tue, 09 Feb 2021 03:43:52 GMT
COPY file:9a05f2c8b43e780abf69d813f7c45613cced5481a65611bf8127c6f222dff4e3 in /usr/local/bin/ 
# Tue, 09 Feb 2021 03:43:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 09 Feb 2021 03:43:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Feb 2021 03:43:53 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:032413a44cf56b097e48b8221bf475ca1bec26e7a27f35fe61d699366a335b79`  
		Last Modified: Tue, 09 Feb 2021 02:45:31 GMT  
		Size: 25.7 MB (25710021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e65f701864562492efa2c0035134b62d68efdb6e7241a0a2dcc3151e6d5775b`  
		Last Modified: Tue, 09 Feb 2021 03:44:28 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4e3420e68f3ae99d8991a4b0d1af805c198727de7b29e2cde33979e435127cd`  
		Last Modified: Tue, 09 Feb 2021 03:45:29 GMT  
		Size: 5.1 MB (5109374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:927850badcae047d963792a5e2740ec9578ff4265493fc01a8f45bd9bb6a3bdd`  
		Last Modified: Tue, 09 Feb 2021 03:45:29 GMT  
		Size: 471.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88da612e555ceb62d58cff6fdce3cf87b23ac80799213d4b8239ad893874ab88`  
		Last Modified: Tue, 09 Feb 2021 03:45:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haproxy:1.7.12`

```console
$ docker pull haproxy@sha256:edc8c85a94789541774f039506cf8a89bed539537472785be53eb77054240fd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `haproxy:1.7.12` - linux; amd64

```console
$ docker pull haproxy@sha256:119b805973c071e774718868244cbceed376f18e9531771609a8044f59e870ce
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32474286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3d3b72953731b55b715f8fb0fc7718468f5afc4ecf2c3c83c6fe40517cb9d87`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Mon, 08 Mar 2021 21:37:25 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 21:50:53 GMT
ENV HAPROXY_VERSION=1.7.12
# Mon, 08 Mar 2021 21:50:53 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.7/src/haproxy-1.7.12.tar.gz
# Mon, 08 Mar 2021 21:50:53 GMT
ENV HAPROXY_SHA256=4118178b553a107b227f3f84774c7a50ae0b3ac2be39211c3db511ed4efe48ce
# Mon, 08 Mar 2021 21:51:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 08 Mar 2021 21:51:24 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 21:51:25 GMT
COPY file:9a05f2c8b43e780abf69d813f7c45613cced5481a65611bf8127c6f222dff4e3 in /usr/local/bin/ 
# Mon, 08 Mar 2021 21:51:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 08 Mar 2021 21:51:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 21:51:26 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7bca45a971fe608786870ce75c9976f8e5a958f55e1287a6120048b897c63b6`  
		Last Modified: Mon, 08 Mar 2021 21:52:33 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:354c55b6a82a8a9e6925c42d24ed2d51daebff99990e70923a5d02e68e2d0d9d`  
		Last Modified: Mon, 08 Mar 2021 21:55:27 GMT  
		Size: 5.4 MB (5377174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b93fc6908cdb503cf2286f0940b339c4045f2808904a2d8e5e62c6117ecc1d7`  
		Last Modified: Mon, 08 Mar 2021 21:55:29 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c188b46dbd38eb9c0ec85c577bddad66dc38bd7200293c7b9a595552ed6d33f3`  
		Last Modified: Mon, 08 Mar 2021 21:55:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.7.12` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:8a19cad8062d4496d5c4b120b8e1af4c6c4166ffa81287983e2ee7b5cf8b061e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.9 MB (29850083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fae256b6443bbb3e0a9ee6b9a5904622e3302be9e7ed830d62bce7276850cca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:50:10 GMT
ADD file:fbd00ef7871dc27d7ed5fa8c238cdc80652bd87b8033be7de9e54a799bbf10a4 in / 
# Tue, 09 Feb 2021 02:50:11 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:45:24 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 09 Feb 2021 03:53:29 GMT
ENV HAPROXY_VERSION=1.7.12
# Tue, 09 Feb 2021 03:53:30 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.7/src/haproxy-1.7.12.tar.gz
# Tue, 09 Feb 2021 03:53:32 GMT
ENV HAPROXY_SHA256=4118178b553a107b227f3f84774c7a50ae0b3ac2be39211c3db511ed4efe48ce
# Tue, 09 Feb 2021 03:54:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 09 Feb 2021 03:54:23 GMT
STOPSIGNAL SIGUSR1
# Tue, 09 Feb 2021 03:54:24 GMT
COPY file:9a05f2c8b43e780abf69d813f7c45613cced5481a65611bf8127c6f222dff4e3 in /usr/local/bin/ 
# Tue, 09 Feb 2021 03:54:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 09 Feb 2021 03:54:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Feb 2021 03:54:28 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:8e683fcc73f4da7d69ce1d5f4e1d77510aa459490068f38db2d8663698b391a0`  
		Last Modified: Tue, 09 Feb 2021 02:59:07 GMT  
		Size: 24.8 MB (24839297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def565d52deae74587a55f60d168bd531ebe8095c594027b7057a8fc1be0e8af`  
		Last Modified: Tue, 09 Feb 2021 03:54:54 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caccfbe89a6a82d7d11c0a5dd3e17f117553ba0647d31074847b69f997dba830`  
		Last Modified: Tue, 09 Feb 2021 03:55:58 GMT  
		Size: 5.0 MB (5008822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8a51ed81a112128f089c2f53ef3c66006457dd42aeb83a7fadb2ef8d123197c`  
		Last Modified: Tue, 09 Feb 2021 03:55:57 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8366cfe41f6e14fde9dd452961959c91b9c887d116fc99650686a057115bc8c2`  
		Last Modified: Tue, 09 Feb 2021 03:55:56 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.7.12` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:236f09c8276a0e3db3b5f8689c5bc48102fc2b4901fef551e77ddec1cb862ec6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27580523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11f450811f965ef7a87c7175122b79e6ee8202139d8173c5c509cede1ee2ecf5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 03:00:57 GMT
ADD file:e675d50366bde57173a75f9a29367d765e7da2b7254c5254b64e777cf6870502 in / 
# Tue, 09 Feb 2021 03:01:00 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:49:38 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 09 Feb 2021 03:56:40 GMT
ENV HAPROXY_VERSION=1.7.12
# Tue, 09 Feb 2021 03:56:40 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.7/src/haproxy-1.7.12.tar.gz
# Tue, 09 Feb 2021 03:56:41 GMT
ENV HAPROXY_SHA256=4118178b553a107b227f3f84774c7a50ae0b3ac2be39211c3db511ed4efe48ce
# Tue, 09 Feb 2021 03:57:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 09 Feb 2021 03:57:26 GMT
STOPSIGNAL SIGUSR1
# Tue, 09 Feb 2021 03:57:27 GMT
COPY file:9a05f2c8b43e780abf69d813f7c45613cced5481a65611bf8127c6f222dff4e3 in /usr/local/bin/ 
# Tue, 09 Feb 2021 03:57:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 09 Feb 2021 03:57:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Feb 2021 03:57:32 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:db574d82360c3b60abadbef4f3daf8dee01f24741fc6ab3692aa543558d8b624`  
		Last Modified: Tue, 09 Feb 2021 03:09:46 GMT  
		Size: 22.7 MB (22703384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9978ebb1881387f11e025fb46dce2b3c715f705f6d240737574f8848c27fa0d7`  
		Last Modified: Tue, 09 Feb 2021 03:58:16 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0904496d6669d3035ee4f76e1cd26236e719ad332d797e9749a9f27d47bc727`  
		Last Modified: Tue, 09 Feb 2021 03:59:23 GMT  
		Size: 4.9 MB (4875174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20757dd7dc51d07bf4f6a5df48f6859aa9643759b7fde9f458b8769e2de807da`  
		Last Modified: Tue, 09 Feb 2021 03:59:22 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f3c6212281f061ceed1955d145170500f89f7224d83fd9b29bbb50b04b29272`  
		Last Modified: Tue, 09 Feb 2021 03:59:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.7.12` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:d5eba597a791cb44dff0e436d4bdaa4846fe49779b2826361b61dff6475e40f7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31117578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9461f8882da335f0ac2efa06d4dc7150740c33013ba3111a6962d177cfa11064`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:41:10 GMT
ADD file:d906dedaf14d8e3874b46787f7a1dbf268bc124c4e1dd32f13f3079e12f22238 in / 
# Tue, 09 Feb 2021 02:41:13 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:59:41 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 09 Feb 2021 04:06:57 GMT
ENV HAPROXY_VERSION=1.7.12
# Tue, 09 Feb 2021 04:06:57 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.7/src/haproxy-1.7.12.tar.gz
# Tue, 09 Feb 2021 04:06:58 GMT
ENV HAPROXY_SHA256=4118178b553a107b227f3f84774c7a50ae0b3ac2be39211c3db511ed4efe48ce
# Tue, 09 Feb 2021 04:07:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 09 Feb 2021 04:07:42 GMT
STOPSIGNAL SIGUSR1
# Tue, 09 Feb 2021 04:07:43 GMT
COPY file:9a05f2c8b43e780abf69d813f7c45613cced5481a65611bf8127c6f222dff4e3 in /usr/local/bin/ 
# Tue, 09 Feb 2021 04:07:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 09 Feb 2021 04:07:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Feb 2021 04:07:48 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:83c5cfdaa5385ea6fc4d31e724fd4dc5d74de847a7bdd968555b8f2c558dac0e`  
		Last Modified: Tue, 09 Feb 2021 02:47:27 GMT  
		Size: 25.9 MB (25851449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b7f43dd52365bce2c2b75f29577aa39d2b5794e2561cddc0678422ffc1f7d15`  
		Last Modified: Tue, 09 Feb 2021 04:08:36 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d8c3de44d1e105730b4f66b262320f4e31019ebfaa6d1f1eb768d66fd7d646`  
		Last Modified: Tue, 09 Feb 2021 04:09:42 GMT  
		Size: 5.3 MB (5264162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc6d37f3655455f3dc9079ef2c659e3355f5c2e7000384e0af351d04cc0f1f4`  
		Last Modified: Tue, 09 Feb 2021 04:09:41 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54c844a67c2c77fd99deee7dc9e27eb91911cd829b5a00c8454eca13a9b0b0e1`  
		Last Modified: Tue, 09 Feb 2021 04:09:41 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.7.12` - linux; 386

```console
$ docker pull haproxy@sha256:f244511b564a5138663e7a6c150e49e540d872b9ca119638179bfbe526bf25b1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.1 MB (33064521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06ac072a7db0c5bb4cb1d835623f9587a310b9ae97f1e9a95e80a07dbeceb403`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:39:47 GMT
ADD file:61c31b1037672781ed0ecbc080ee3d49c83af49f5578b011544513fa9625698d in / 
# Tue, 09 Feb 2021 02:39:47 GMT
CMD ["bash"]
# Mon, 08 Mar 2021 22:02:40 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 22:15:31 GMT
ENV HAPROXY_VERSION=1.7.12
# Mon, 08 Mar 2021 22:15:31 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.7/src/haproxy-1.7.12.tar.gz
# Mon, 08 Mar 2021 22:15:31 GMT
ENV HAPROXY_SHA256=4118178b553a107b227f3f84774c7a50ae0b3ac2be39211c3db511ed4efe48ce
# Mon, 08 Mar 2021 22:16:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 08 Mar 2021 22:16:02 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 22:16:03 GMT
COPY file:9a05f2c8b43e780abf69d813f7c45613cced5481a65611bf8127c6f222dff4e3 in /usr/local/bin/ 
# Mon, 08 Mar 2021 22:16:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 08 Mar 2021 22:16:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 22:16:04 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:27cbb00346a16ea900c1049a2e5b47942c586c377179e098382c8ca1c8e87966`  
		Last Modified: Tue, 09 Feb 2021 02:45:51 GMT  
		Size: 27.8 MB (27752731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b6129a97a33727ea8a598d1e797bccce491920bf29d769880cf2fc6d3e0436`  
		Last Modified: Mon, 08 Mar 2021 22:17:48 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e82c1d67749e4ed80b7c2276954c4d75034a6afab3df4937009d806b536c8239`  
		Last Modified: Mon, 08 Mar 2021 22:20:45 GMT  
		Size: 5.3 MB (5309827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf95b65335e441923a3ed713a5a92c79fdf48ab5d750598d4fa2df7924b95717`  
		Last Modified: Mon, 08 Mar 2021 22:20:45 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df53524c328ab022e092aafdb5d2f3dd23de98d3fbcbae684e7c215950c64a4`  
		Last Modified: Mon, 08 Mar 2021 22:20:41 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.7.12` - linux; mips64le

```console
$ docker pull haproxy@sha256:3f4a3ad46303d073d1632050c4498fdc9c00de00947eba4359cc1c433d727842
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 MB (30780167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5df41bdec068aca343ee488f5e79c308c5d34f94e766a051789cbe0e8bcb3476`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 03:09:26 GMT
ADD file:0222a151f4e5033d9eae98ce2b703a63f52d049dd72ac40bdd0dc2dafe619f0a in / 
# Tue, 09 Feb 2021 03:09:27 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:41:09 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 09 Feb 2021 03:55:59 GMT
ENV HAPROXY_VERSION=1.7.12
# Tue, 09 Feb 2021 03:55:59 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.7/src/haproxy-1.7.12.tar.gz
# Tue, 09 Feb 2021 03:55:59 GMT
ENV HAPROXY_SHA256=4118178b553a107b227f3f84774c7a50ae0b3ac2be39211c3db511ed4efe48ce
# Tue, 09 Feb 2021 03:57:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 09 Feb 2021 03:57:25 GMT
STOPSIGNAL SIGUSR1
# Tue, 09 Feb 2021 03:57:25 GMT
COPY file:9a05f2c8b43e780abf69d813f7c45613cced5481a65611bf8127c6f222dff4e3 in /usr/local/bin/ 
# Tue, 09 Feb 2021 03:57:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 09 Feb 2021 03:57:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Feb 2021 03:57:28 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:dfb81134097d874e01b495d1fba82e384056d0a3a45f01a69a2e86ae82af1e96`  
		Last Modified: Tue, 09 Feb 2021 03:15:55 GMT  
		Size: 25.8 MB (25764640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a549d56662447dd8cb15faf59ca0fc2eda7a877e9aee16aadd09fd46e4214a`  
		Last Modified: Tue, 09 Feb 2021 03:57:56 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b44bcf0254fd5eadcfa76c8d554eb8e3b3e20bb16dc5ba18b3b2eb9d3c2e42`  
		Last Modified: Tue, 09 Feb 2021 03:59:44 GMT  
		Size: 5.0 MB (5013558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a8a2d6ad64b59ceed1bbd3c436e54851d8a006294fda33bf2a53b3fb66cc7b`  
		Last Modified: Tue, 09 Feb 2021 03:59:41 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36ed3f7edc1954ab6f053036a2e7baab54b6dcaec38a11c3c6ef319d636a7f03`  
		Last Modified: Tue, 09 Feb 2021 03:59:41 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.7.12` - linux; ppc64le

```console
$ docker pull haproxy@sha256:db32dab977fd448211a6c17025e42abf9e18caab6063ba4961eb92a92bcd9873
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36215161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb7e2adda4f9e417354c0c51830a1f2ace23b9e809887dae1351d38d2aa22be6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:19:19 GMT
ADD file:9a8cfdf0eab394a693b5cde0700ad47b6e8506ef0b79fabb8a07874b96e6c394 in / 
# Tue, 09 Feb 2021 02:19:34 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 05:52:23 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 09 Feb 2021 06:31:35 GMT
ENV HAPROXY_VERSION=1.7.12
# Tue, 09 Feb 2021 06:31:43 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.7/src/haproxy-1.7.12.tar.gz
# Tue, 09 Feb 2021 06:31:48 GMT
ENV HAPROXY_SHA256=4118178b553a107b227f3f84774c7a50ae0b3ac2be39211c3db511ed4efe48ce
# Tue, 09 Feb 2021 06:37:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 09 Feb 2021 06:37:34 GMT
STOPSIGNAL SIGUSR1
# Tue, 09 Feb 2021 06:37:37 GMT
COPY file:9a05f2c8b43e780abf69d813f7c45613cced5481a65611bf8127c6f222dff4e3 in /usr/local/bin/ 
# Tue, 09 Feb 2021 06:37:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 09 Feb 2021 06:37:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Feb 2021 06:37:50 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:9996b4fb6bc1c50f95ba30f8988c9c89526556fa320d3fda59d3d8359f7810d6`  
		Last Modified: Tue, 09 Feb 2021 02:27:59 GMT  
		Size: 30.5 MB (30519509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7f600bc4989eb9f12d5006a73f5958eb4fe85f86bc4008d7a899bb935b0f1c`  
		Last Modified: Tue, 09 Feb 2021 06:38:36 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6deb7498d6b48c4e250d2ef780731517b82e52ca28b770c66185f53c198221af`  
		Last Modified: Tue, 09 Feb 2021 06:40:08 GMT  
		Size: 5.7 MB (5693685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b407e1fb599510b5a8f93dc9c92e47e18ee9a5b556ae7f977ae89d1415986d58`  
		Last Modified: Tue, 09 Feb 2021 06:40:07 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80356779393c7c2d00f0aa589123da6c877056c789d7f56f810bafd5cdb8c413`  
		Last Modified: Tue, 09 Feb 2021 06:40:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.7.12` - linux; s390x

```console
$ docker pull haproxy@sha256:60d0f1c28672e8206688f127bef30f1478f4ed4100525c2745e15cdd1dd89c83
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 MB (30821360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74cf1e00801d68b8718fac9fb4b05e0e91f6268f22dcab57d283ff87c724961a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:42:10 GMT
ADD file:0edb2de05df54191a141bd125f59d7e14eef0cc4576927a247b8dd7d6f255d04 in / 
# Tue, 09 Feb 2021 02:42:12 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:39:30 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 09 Feb 2021 03:43:32 GMT
ENV HAPROXY_VERSION=1.7.12
# Tue, 09 Feb 2021 03:43:33 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.7/src/haproxy-1.7.12.tar.gz
# Tue, 09 Feb 2021 03:43:33 GMT
ENV HAPROXY_SHA256=4118178b553a107b227f3f84774c7a50ae0b3ac2be39211c3db511ed4efe48ce
# Tue, 09 Feb 2021 03:43:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 09 Feb 2021 03:43:52 GMT
STOPSIGNAL SIGUSR1
# Tue, 09 Feb 2021 03:43:52 GMT
COPY file:9a05f2c8b43e780abf69d813f7c45613cced5481a65611bf8127c6f222dff4e3 in /usr/local/bin/ 
# Tue, 09 Feb 2021 03:43:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 09 Feb 2021 03:43:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Feb 2021 03:43:53 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:032413a44cf56b097e48b8221bf475ca1bec26e7a27f35fe61d699366a335b79`  
		Last Modified: Tue, 09 Feb 2021 02:45:31 GMT  
		Size: 25.7 MB (25710021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e65f701864562492efa2c0035134b62d68efdb6e7241a0a2dcc3151e6d5775b`  
		Last Modified: Tue, 09 Feb 2021 03:44:28 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4e3420e68f3ae99d8991a4b0d1af805c198727de7b29e2cde33979e435127cd`  
		Last Modified: Tue, 09 Feb 2021 03:45:29 GMT  
		Size: 5.1 MB (5109374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:927850badcae047d963792a5e2740ec9578ff4265493fc01a8f45bd9bb6a3bdd`  
		Last Modified: Tue, 09 Feb 2021 03:45:29 GMT  
		Size: 471.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88da612e555ceb62d58cff6fdce3cf87b23ac80799213d4b8239ad893874ab88`  
		Last Modified: Tue, 09 Feb 2021 03:45:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haproxy:1.7.12-alpine`

```console
$ docker pull haproxy@sha256:e1804b53df074ca0b499c4e068a36d020c5ff19f7556ccbec54c7d17d3d981c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `haproxy:1.7.12-alpine` - linux; amd64

```console
$ docker pull haproxy@sha256:71f6a72398f3f3d9f71fda8fb7cdc2e5e853578304a628f900ea6e4f583f5eb4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3545379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c70fbaa97615f84ded660f22f137fdb0793306a292ce4f0f4d88f4d91820c42`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Mon, 08 Mar 2021 21:51:36 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 21:51:36 GMT
ENV HAPROXY_VERSION=1.7.12
# Mon, 08 Mar 2021 21:51:36 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.7/src/haproxy-1.7.12.tar.gz
# Mon, 08 Mar 2021 21:51:37 GMT
ENV HAPROXY_SHA256=4118178b553a107b227f3f84774c7a50ae0b3ac2be39211c3db511ed4efe48ce
# Mon, 08 Mar 2021 21:51:56 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		CFLAGS+="-Wno-address-of-packed-member" 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Mon, 08 Mar 2021 21:51:56 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 21:51:56 GMT
COPY file:9a05f2c8b43e780abf69d813f7c45613cced5481a65611bf8127c6f222dff4e3 in /usr/local/bin/ 
# Mon, 08 Mar 2021 21:51:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 08 Mar 2021 21:51:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 21:51:58 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61cfca094beb50121fedc085e05424ef801ffc8e4db02feb1058fc1849ded964`  
		Last Modified: Mon, 08 Mar 2021 21:55:38 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:950e5077b04f7048a989368700c9698b5d1f4f6a5642a4bda20ce197c306cf0e`  
		Last Modified: Mon, 08 Mar 2021 21:55:39 GMT  
		Size: 744.1 KB (744104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:019969b2ded8166efd171d53453e475c63ed144b9c90a700e066fbb1e4fb7ea9`  
		Last Modified: Mon, 08 Mar 2021 21:55:38 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c06aadd47fc8bb9ac7d32ceb1348d8094f8b0ff2435c12eeb454c0931e4e2a3f`  
		Last Modified: Mon, 08 Mar 2021 21:55:38 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.7.12-alpine` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:9ac9cf38b8fe3c1c30f579b6f57e36fe6cda5695c07ded754467106e1ac8d4cd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3321546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:412923049f39ba769a9fdf63ba318ee9f277c89f3c29036b28706f2db91825fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 24 Feb 2021 20:50:34 GMT
ADD file:8bbb59eeaad0cbcf11559bc6e2b4492aadf6822d1935ed50c710f8bed858b7b5 in / 
# Wed, 24 Feb 2021 20:50:35 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 21:20:53 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 24 Feb 2021 21:20:54 GMT
ENV HAPROXY_VERSION=1.7.12
# Wed, 24 Feb 2021 21:20:54 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.7/src/haproxy-1.7.12.tar.gz
# Wed, 24 Feb 2021 21:20:55 GMT
ENV HAPROXY_SHA256=4118178b553a107b227f3f84774c7a50ae0b3ac2be39211c3db511ed4efe48ce
# Wed, 24 Feb 2021 21:21:04 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		CFLAGS+="-Wno-address-of-packed-member" 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 24 Feb 2021 21:21:04 GMT
STOPSIGNAL SIGUSR1
# Wed, 24 Feb 2021 21:21:05 GMT
COPY file:9a05f2c8b43e780abf69d813f7c45613cced5481a65611bf8127c6f222dff4e3 in /usr/local/bin/ 
# Wed, 24 Feb 2021 21:21:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 24 Feb 2021 21:21:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Feb 2021 21:21:08 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:55242616b0494f68f44470d864da746cd2a8f8f2d1ffca698114de64032247ef`  
		Last Modified: Wed, 24 Feb 2021 20:51:17 GMT  
		Size: 2.6 MB (2604518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bdbd14c28043c5cc96860fac45ad8bc709436d957698ee0577f595c4dc2bca3`  
		Last Modified: Wed, 24 Feb 2021 21:21:44 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc56d798e26723b2f13287d3c54b30736ce399d73c64382997ca3cd4f729fb1a`  
		Last Modified: Wed, 24 Feb 2021 21:21:45 GMT  
		Size: 715.2 KB (715249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32770773bc3f576d91acbcebf9535c1723b72c344caca6dde1ccc39baf98644f`  
		Last Modified: Wed, 24 Feb 2021 21:21:44 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03400ec01a1e86b5efbaa4251bdb01a0514ab1c6ec34b325a6017dcad3609ad5`  
		Last Modified: Wed, 24 Feb 2021 21:21:44 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.7.12-alpine` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:f6236daabca11994a017fa21142d7e3145fd278a4041b0cd074942d9e2757324
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3083025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5645b9f37de0fcf48f8064d55c3a4e74c916fecb1ff6aaacc2956c2851c14f9b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 24 Feb 2021 21:03:35 GMT
ADD file:2632f48dd643f8927da2b1af8365b3edb484bd6b7d9fee4009e69f6cf3310e91 in / 
# Wed, 24 Feb 2021 21:03:36 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 21:52:14 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 24 Feb 2021 21:52:14 GMT
ENV HAPROXY_VERSION=1.7.12
# Wed, 24 Feb 2021 21:52:15 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.7/src/haproxy-1.7.12.tar.gz
# Wed, 24 Feb 2021 21:52:16 GMT
ENV HAPROXY_SHA256=4118178b553a107b227f3f84774c7a50ae0b3ac2be39211c3db511ed4efe48ce
# Wed, 24 Feb 2021 21:52:24 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		CFLAGS+="-Wno-address-of-packed-member" 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 24 Feb 2021 21:52:25 GMT
STOPSIGNAL SIGUSR1
# Wed, 24 Feb 2021 21:52:25 GMT
COPY file:9a05f2c8b43e780abf69d813f7c45613cced5481a65611bf8127c6f222dff4e3 in /usr/local/bin/ 
# Wed, 24 Feb 2021 21:52:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 24 Feb 2021 21:52:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Feb 2021 21:52:30 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:8e85c7428c31ea48b47424ca0e4663106c54591c83545d32b66a77093f90ffd0`  
		Last Modified: Wed, 24 Feb 2021 21:04:23 GMT  
		Size: 2.4 MB (2408004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f33d35d3cb78949f9eed37fbe99c4f52b700070ac7c22703b5be28c97ea9a18`  
		Last Modified: Wed, 24 Feb 2021 21:53:25 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:828e1b64e8d56a081c57b60909a658f03f659b17965e8dde834ce35eb846e93a`  
		Last Modified: Wed, 24 Feb 2021 21:53:25 GMT  
		Size: 673.2 KB (673240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2113ebbb17f9be3f7a129669fa6fb779a70abafba4330d55c7872b135605c1`  
		Last Modified: Wed, 24 Feb 2021 21:53:25 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eef89b48dcc25e6db0d5f2c934cf1325737db53d443f94625b9c8d79becd16fb`  
		Last Modified: Wed, 24 Feb 2021 21:53:25 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.7.12-alpine` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:43e67db484ad67774c69b7123ff409258ee9bb95bf7ea54042e2cded947da44b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3431886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47dba951f17b1bce35217ac3fb4341ea323f3be1de91e042aed78a60eca50fed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 24 Feb 2021 20:39:39 GMT
ADD file:7e82858ef85f6db90c131ed835a390d736cfdbd1a0cf8bccaeed8f7e30172ddb in / 
# Wed, 24 Feb 2021 20:39:40 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 22:01:03 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 24 Feb 2021 22:01:04 GMT
ENV HAPROXY_VERSION=1.7.12
# Wed, 24 Feb 2021 22:01:04 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.7/src/haproxy-1.7.12.tar.gz
# Wed, 24 Feb 2021 22:01:06 GMT
ENV HAPROXY_SHA256=4118178b553a107b227f3f84774c7a50ae0b3ac2be39211c3db511ed4efe48ce
# Wed, 24 Feb 2021 22:01:16 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		CFLAGS+="-Wno-address-of-packed-member" 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 24 Feb 2021 22:01:17 GMT
STOPSIGNAL SIGUSR1
# Wed, 24 Feb 2021 22:01:18 GMT
COPY file:9a05f2c8b43e780abf69d813f7c45613cced5481a65611bf8127c6f222dff4e3 in /usr/local/bin/ 
# Wed, 24 Feb 2021 22:01:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 24 Feb 2021 22:01:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Feb 2021 22:01:21 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:dce8679b510e95d136241d02ababff86469dd14220812a7ce9202833c0e32f66`  
		Last Modified: Wed, 24 Feb 2021 20:40:26 GMT  
		Size: 2.7 MB (2709880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a9590b9a540ec8f16d55696143e189cc0a2926f50e7a26aeebd3ac11597618f`  
		Last Modified: Wed, 24 Feb 2021 22:02:26 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57a00cfeba4679650e05eab699e088df1b230d368c52189d0543126937af2d29`  
		Last Modified: Wed, 24 Feb 2021 22:02:26 GMT  
		Size: 720.2 KB (720224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49936e4cdb97c502efd4da3bfb6acc80a5c4601834c6b23d3e0931c65013d7f0`  
		Last Modified: Wed, 24 Feb 2021 22:02:26 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3fd2a1bd16af67d7296038cf2a6e98dc147dcb736c15e4d7c32c2368ee6a47d`  
		Last Modified: Wed, 24 Feb 2021 22:02:26 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.7.12-alpine` - linux; 386

```console
$ docker pull haproxy@sha256:8d8abe82d39578e1d36d45c4a106417ca6dbd65d6e82ff4c8c17237e074f10cd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3552487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72fef1bce5e6ed51ed5fda04c574053d3b133f1f0693bffc033a50160e417947`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 24 Feb 2021 20:38:41 GMT
ADD file:1f1a1b55522505e78fcc069edb6c793371f78991e90dcb464e4ddac7efd6588c in / 
# Wed, 24 Feb 2021 20:38:41 GMT
CMD ["/bin/sh"]
# Mon, 08 Mar 2021 22:16:15 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 22:16:15 GMT
ENV HAPROXY_VERSION=1.7.12
# Mon, 08 Mar 2021 22:16:15 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.7/src/haproxy-1.7.12.tar.gz
# Mon, 08 Mar 2021 22:16:15 GMT
ENV HAPROXY_SHA256=4118178b553a107b227f3f84774c7a50ae0b3ac2be39211c3db511ed4efe48ce
# Mon, 08 Mar 2021 22:16:28 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		CFLAGS+="-Wno-address-of-packed-member" 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Mon, 08 Mar 2021 22:16:28 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 22:16:29 GMT
COPY file:9a05f2c8b43e780abf69d813f7c45613cced5481a65611bf8127c6f222dff4e3 in /usr/local/bin/ 
# Mon, 08 Mar 2021 22:16:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 08 Mar 2021 22:16:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 22:16:30 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:045e8056601208133bee5c98e76028f9b97e055c738892f8d6283205e1006173`  
		Last Modified: Wed, 24 Feb 2021 20:39:27 GMT  
		Size: 2.8 MB (2794750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4edf5685dc9d4ffdb2d48eb57003c667fa2b11a7347440d7ad7864c8b5c93c9c`  
		Last Modified: Mon, 08 Mar 2021 22:20:59 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae99fbf637e210982c88a2b1f160cc9d9dd9fb57d23604520615265da2312856`  
		Last Modified: Mon, 08 Mar 2021 22:21:00 GMT  
		Size: 756.0 KB (755962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58474d2fce79674176aa73105a324960e38120adced74d0968fb64ec0f4abf92`  
		Last Modified: Mon, 08 Mar 2021 22:20:59 GMT  
		Size: 467.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5187aad79ad1bb31895dbd2a311a1eede4d53250fc614cd211019c6d4f5a1a32`  
		Last Modified: Mon, 08 Mar 2021 22:20:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.7.12-alpine` - linux; ppc64le

```console
$ docker pull haproxy@sha256:9b52d1d0fba85725153a787a90f69e446aa6aeddddf4457fabdd947bf5f2aa51
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3571874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c15ee1b717a708a9546a0729c3077de09bb1855cd8e2b7063373ecf4f51df448`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 24 Feb 2021 20:45:10 GMT
ADD file:90df4b3d767cd67ff62e490ca0a7d69bae532cf3fa6f8971a0d2c1b27fb4bdd1 in / 
# Wed, 24 Feb 2021 20:45:16 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 21:58:48 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 24 Feb 2021 21:58:53 GMT
ENV HAPROXY_VERSION=1.7.12
# Wed, 24 Feb 2021 21:59:00 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.7/src/haproxy-1.7.12.tar.gz
# Wed, 24 Feb 2021 21:59:06 GMT
ENV HAPROXY_SHA256=4118178b553a107b227f3f84774c7a50ae0b3ac2be39211c3db511ed4efe48ce
# Wed, 24 Feb 2021 21:59:47 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		CFLAGS+="-Wno-address-of-packed-member" 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 24 Feb 2021 22:00:08 GMT
STOPSIGNAL SIGUSR1
# Wed, 24 Feb 2021 22:00:21 GMT
COPY file:9a05f2c8b43e780abf69d813f7c45613cced5481a65611bf8127c6f222dff4e3 in /usr/local/bin/ 
# Wed, 24 Feb 2021 22:00:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 24 Feb 2021 22:00:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Feb 2021 22:01:09 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:8f446c8f22d4a7a7520099080f73ffa6f455358a840b542fb2ad15c0032adeca`  
		Last Modified: Wed, 24 Feb 2021 20:46:19 GMT  
		Size: 2.8 MB (2805893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49409cae7ffcdac55e8540a510a9881e2a1b02456f2b2ca53a259c9c0e8d40bb`  
		Last Modified: Wed, 24 Feb 2021 22:02:09 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97c56ebfda965b4db03d2725117a2f39dd5483e297f554e0cf243fda19a7f03`  
		Last Modified: Wed, 24 Feb 2021 22:02:08 GMT  
		Size: 764.2 KB (764200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf682249844618c74f6af602f0eb6759224dba6571d2836b799fa744fcd1c47`  
		Last Modified: Wed, 24 Feb 2021 22:02:07 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bebdfd12abd3da40fd7f6691974c8a2c1a3d6033cce0d11f64a7203e55fdbb59`  
		Last Modified: Wed, 24 Feb 2021 22:02:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.7.12-alpine` - linux; s390x

```console
$ docker pull haproxy@sha256:3df8a3e4ac9b633a10d8aba0019b95fbda1692dcaa5b4230e047a39e841b60b2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dce9becf960ae76ae83bddc9c4307c44e234f714f807f7fc2b508f93ffaa39df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 24 Feb 2021 20:42:00 GMT
ADD file:ad5b3d24d5412d341e932d4497614d564c9c413984feaf8542113d6674b34b53 in / 
# Wed, 24 Feb 2021 20:42:01 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 21:34:41 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 24 Feb 2021 21:34:41 GMT
ENV HAPROXY_VERSION=1.7.12
# Wed, 24 Feb 2021 21:34:42 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.7/src/haproxy-1.7.12.tar.gz
# Wed, 24 Feb 2021 21:34:43 GMT
ENV HAPROXY_SHA256=4118178b553a107b227f3f84774c7a50ae0b3ac2be39211c3db511ed4efe48ce
# Wed, 24 Feb 2021 21:34:54 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		CFLAGS+="-Wno-address-of-packed-member" 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 24 Feb 2021 21:34:54 GMT
STOPSIGNAL SIGUSR1
# Wed, 24 Feb 2021 21:34:55 GMT
COPY file:9a05f2c8b43e780abf69d813f7c45613cced5481a65611bf8127c6f222dff4e3 in /usr/local/bin/ 
# Wed, 24 Feb 2021 21:34:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 24 Feb 2021 21:34:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Feb 2021 21:34:58 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:84a604a54099b51a6c81db20dff8dc298ec82555e772be84328b067d3f35a93e`  
		Last Modified: Wed, 24 Feb 2021 20:42:40 GMT  
		Size: 2.6 MB (2567318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dc235c40a316f4f9079fd34b0dc756150ccabb41d754a8729dab3dedcb1e04f`  
		Last Modified: Wed, 24 Feb 2021 21:35:59 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75d3725f63f840237a91bc09312ba6d3f460634ee68acfbe8b898e48c123feb6`  
		Last Modified: Wed, 24 Feb 2021 21:35:59 GMT  
		Size: 774.5 KB (774519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33bca3d370726bef307d76fbf3e232dfb7751a2b0b340ca8230b85c572e5cb2d`  
		Last Modified: Wed, 24 Feb 2021 21:35:59 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2279b0ba34ec524e4df62f438e695042f6665fb646c3995d1ce98fcfabaae677`  
		Last Modified: Wed, 24 Feb 2021 21:35:59 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haproxy:1.7-alpine`

```console
$ docker pull haproxy@sha256:e1804b53df074ca0b499c4e068a36d020c5ff19f7556ccbec54c7d17d3d981c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `haproxy:1.7-alpine` - linux; amd64

```console
$ docker pull haproxy@sha256:71f6a72398f3f3d9f71fda8fb7cdc2e5e853578304a628f900ea6e4f583f5eb4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3545379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c70fbaa97615f84ded660f22f137fdb0793306a292ce4f0f4d88f4d91820c42`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Mon, 08 Mar 2021 21:51:36 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 21:51:36 GMT
ENV HAPROXY_VERSION=1.7.12
# Mon, 08 Mar 2021 21:51:36 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.7/src/haproxy-1.7.12.tar.gz
# Mon, 08 Mar 2021 21:51:37 GMT
ENV HAPROXY_SHA256=4118178b553a107b227f3f84774c7a50ae0b3ac2be39211c3db511ed4efe48ce
# Mon, 08 Mar 2021 21:51:56 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		CFLAGS+="-Wno-address-of-packed-member" 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Mon, 08 Mar 2021 21:51:56 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 21:51:56 GMT
COPY file:9a05f2c8b43e780abf69d813f7c45613cced5481a65611bf8127c6f222dff4e3 in /usr/local/bin/ 
# Mon, 08 Mar 2021 21:51:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 08 Mar 2021 21:51:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 21:51:58 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61cfca094beb50121fedc085e05424ef801ffc8e4db02feb1058fc1849ded964`  
		Last Modified: Mon, 08 Mar 2021 21:55:38 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:950e5077b04f7048a989368700c9698b5d1f4f6a5642a4bda20ce197c306cf0e`  
		Last Modified: Mon, 08 Mar 2021 21:55:39 GMT  
		Size: 744.1 KB (744104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:019969b2ded8166efd171d53453e475c63ed144b9c90a700e066fbb1e4fb7ea9`  
		Last Modified: Mon, 08 Mar 2021 21:55:38 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c06aadd47fc8bb9ac7d32ceb1348d8094f8b0ff2435c12eeb454c0931e4e2a3f`  
		Last Modified: Mon, 08 Mar 2021 21:55:38 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.7-alpine` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:9ac9cf38b8fe3c1c30f579b6f57e36fe6cda5695c07ded754467106e1ac8d4cd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3321546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:412923049f39ba769a9fdf63ba318ee9f277c89f3c29036b28706f2db91825fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 24 Feb 2021 20:50:34 GMT
ADD file:8bbb59eeaad0cbcf11559bc6e2b4492aadf6822d1935ed50c710f8bed858b7b5 in / 
# Wed, 24 Feb 2021 20:50:35 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 21:20:53 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 24 Feb 2021 21:20:54 GMT
ENV HAPROXY_VERSION=1.7.12
# Wed, 24 Feb 2021 21:20:54 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.7/src/haproxy-1.7.12.tar.gz
# Wed, 24 Feb 2021 21:20:55 GMT
ENV HAPROXY_SHA256=4118178b553a107b227f3f84774c7a50ae0b3ac2be39211c3db511ed4efe48ce
# Wed, 24 Feb 2021 21:21:04 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		CFLAGS+="-Wno-address-of-packed-member" 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 24 Feb 2021 21:21:04 GMT
STOPSIGNAL SIGUSR1
# Wed, 24 Feb 2021 21:21:05 GMT
COPY file:9a05f2c8b43e780abf69d813f7c45613cced5481a65611bf8127c6f222dff4e3 in /usr/local/bin/ 
# Wed, 24 Feb 2021 21:21:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 24 Feb 2021 21:21:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Feb 2021 21:21:08 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:55242616b0494f68f44470d864da746cd2a8f8f2d1ffca698114de64032247ef`  
		Last Modified: Wed, 24 Feb 2021 20:51:17 GMT  
		Size: 2.6 MB (2604518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bdbd14c28043c5cc96860fac45ad8bc709436d957698ee0577f595c4dc2bca3`  
		Last Modified: Wed, 24 Feb 2021 21:21:44 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc56d798e26723b2f13287d3c54b30736ce399d73c64382997ca3cd4f729fb1a`  
		Last Modified: Wed, 24 Feb 2021 21:21:45 GMT  
		Size: 715.2 KB (715249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32770773bc3f576d91acbcebf9535c1723b72c344caca6dde1ccc39baf98644f`  
		Last Modified: Wed, 24 Feb 2021 21:21:44 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03400ec01a1e86b5efbaa4251bdb01a0514ab1c6ec34b325a6017dcad3609ad5`  
		Last Modified: Wed, 24 Feb 2021 21:21:44 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.7-alpine` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:f6236daabca11994a017fa21142d7e3145fd278a4041b0cd074942d9e2757324
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3083025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5645b9f37de0fcf48f8064d55c3a4e74c916fecb1ff6aaacc2956c2851c14f9b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 24 Feb 2021 21:03:35 GMT
ADD file:2632f48dd643f8927da2b1af8365b3edb484bd6b7d9fee4009e69f6cf3310e91 in / 
# Wed, 24 Feb 2021 21:03:36 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 21:52:14 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 24 Feb 2021 21:52:14 GMT
ENV HAPROXY_VERSION=1.7.12
# Wed, 24 Feb 2021 21:52:15 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.7/src/haproxy-1.7.12.tar.gz
# Wed, 24 Feb 2021 21:52:16 GMT
ENV HAPROXY_SHA256=4118178b553a107b227f3f84774c7a50ae0b3ac2be39211c3db511ed4efe48ce
# Wed, 24 Feb 2021 21:52:24 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		CFLAGS+="-Wno-address-of-packed-member" 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 24 Feb 2021 21:52:25 GMT
STOPSIGNAL SIGUSR1
# Wed, 24 Feb 2021 21:52:25 GMT
COPY file:9a05f2c8b43e780abf69d813f7c45613cced5481a65611bf8127c6f222dff4e3 in /usr/local/bin/ 
# Wed, 24 Feb 2021 21:52:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 24 Feb 2021 21:52:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Feb 2021 21:52:30 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:8e85c7428c31ea48b47424ca0e4663106c54591c83545d32b66a77093f90ffd0`  
		Last Modified: Wed, 24 Feb 2021 21:04:23 GMT  
		Size: 2.4 MB (2408004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f33d35d3cb78949f9eed37fbe99c4f52b700070ac7c22703b5be28c97ea9a18`  
		Last Modified: Wed, 24 Feb 2021 21:53:25 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:828e1b64e8d56a081c57b60909a658f03f659b17965e8dde834ce35eb846e93a`  
		Last Modified: Wed, 24 Feb 2021 21:53:25 GMT  
		Size: 673.2 KB (673240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2113ebbb17f9be3f7a129669fa6fb779a70abafba4330d55c7872b135605c1`  
		Last Modified: Wed, 24 Feb 2021 21:53:25 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eef89b48dcc25e6db0d5f2c934cf1325737db53d443f94625b9c8d79becd16fb`  
		Last Modified: Wed, 24 Feb 2021 21:53:25 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.7-alpine` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:43e67db484ad67774c69b7123ff409258ee9bb95bf7ea54042e2cded947da44b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3431886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47dba951f17b1bce35217ac3fb4341ea323f3be1de91e042aed78a60eca50fed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 24 Feb 2021 20:39:39 GMT
ADD file:7e82858ef85f6db90c131ed835a390d736cfdbd1a0cf8bccaeed8f7e30172ddb in / 
# Wed, 24 Feb 2021 20:39:40 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 22:01:03 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 24 Feb 2021 22:01:04 GMT
ENV HAPROXY_VERSION=1.7.12
# Wed, 24 Feb 2021 22:01:04 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.7/src/haproxy-1.7.12.tar.gz
# Wed, 24 Feb 2021 22:01:06 GMT
ENV HAPROXY_SHA256=4118178b553a107b227f3f84774c7a50ae0b3ac2be39211c3db511ed4efe48ce
# Wed, 24 Feb 2021 22:01:16 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		CFLAGS+="-Wno-address-of-packed-member" 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 24 Feb 2021 22:01:17 GMT
STOPSIGNAL SIGUSR1
# Wed, 24 Feb 2021 22:01:18 GMT
COPY file:9a05f2c8b43e780abf69d813f7c45613cced5481a65611bf8127c6f222dff4e3 in /usr/local/bin/ 
# Wed, 24 Feb 2021 22:01:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 24 Feb 2021 22:01:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Feb 2021 22:01:21 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:dce8679b510e95d136241d02ababff86469dd14220812a7ce9202833c0e32f66`  
		Last Modified: Wed, 24 Feb 2021 20:40:26 GMT  
		Size: 2.7 MB (2709880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a9590b9a540ec8f16d55696143e189cc0a2926f50e7a26aeebd3ac11597618f`  
		Last Modified: Wed, 24 Feb 2021 22:02:26 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57a00cfeba4679650e05eab699e088df1b230d368c52189d0543126937af2d29`  
		Last Modified: Wed, 24 Feb 2021 22:02:26 GMT  
		Size: 720.2 KB (720224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49936e4cdb97c502efd4da3bfb6acc80a5c4601834c6b23d3e0931c65013d7f0`  
		Last Modified: Wed, 24 Feb 2021 22:02:26 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3fd2a1bd16af67d7296038cf2a6e98dc147dcb736c15e4d7c32c2368ee6a47d`  
		Last Modified: Wed, 24 Feb 2021 22:02:26 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.7-alpine` - linux; 386

```console
$ docker pull haproxy@sha256:8d8abe82d39578e1d36d45c4a106417ca6dbd65d6e82ff4c8c17237e074f10cd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3552487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72fef1bce5e6ed51ed5fda04c574053d3b133f1f0693bffc033a50160e417947`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 24 Feb 2021 20:38:41 GMT
ADD file:1f1a1b55522505e78fcc069edb6c793371f78991e90dcb464e4ddac7efd6588c in / 
# Wed, 24 Feb 2021 20:38:41 GMT
CMD ["/bin/sh"]
# Mon, 08 Mar 2021 22:16:15 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 22:16:15 GMT
ENV HAPROXY_VERSION=1.7.12
# Mon, 08 Mar 2021 22:16:15 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.7/src/haproxy-1.7.12.tar.gz
# Mon, 08 Mar 2021 22:16:15 GMT
ENV HAPROXY_SHA256=4118178b553a107b227f3f84774c7a50ae0b3ac2be39211c3db511ed4efe48ce
# Mon, 08 Mar 2021 22:16:28 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		CFLAGS+="-Wno-address-of-packed-member" 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Mon, 08 Mar 2021 22:16:28 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 22:16:29 GMT
COPY file:9a05f2c8b43e780abf69d813f7c45613cced5481a65611bf8127c6f222dff4e3 in /usr/local/bin/ 
# Mon, 08 Mar 2021 22:16:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 08 Mar 2021 22:16:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 22:16:30 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:045e8056601208133bee5c98e76028f9b97e055c738892f8d6283205e1006173`  
		Last Modified: Wed, 24 Feb 2021 20:39:27 GMT  
		Size: 2.8 MB (2794750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4edf5685dc9d4ffdb2d48eb57003c667fa2b11a7347440d7ad7864c8b5c93c9c`  
		Last Modified: Mon, 08 Mar 2021 22:20:59 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae99fbf637e210982c88a2b1f160cc9d9dd9fb57d23604520615265da2312856`  
		Last Modified: Mon, 08 Mar 2021 22:21:00 GMT  
		Size: 756.0 KB (755962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58474d2fce79674176aa73105a324960e38120adced74d0968fb64ec0f4abf92`  
		Last Modified: Mon, 08 Mar 2021 22:20:59 GMT  
		Size: 467.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5187aad79ad1bb31895dbd2a311a1eede4d53250fc614cd211019c6d4f5a1a32`  
		Last Modified: Mon, 08 Mar 2021 22:20:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.7-alpine` - linux; ppc64le

```console
$ docker pull haproxy@sha256:9b52d1d0fba85725153a787a90f69e446aa6aeddddf4457fabdd947bf5f2aa51
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3571874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c15ee1b717a708a9546a0729c3077de09bb1855cd8e2b7063373ecf4f51df448`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 24 Feb 2021 20:45:10 GMT
ADD file:90df4b3d767cd67ff62e490ca0a7d69bae532cf3fa6f8971a0d2c1b27fb4bdd1 in / 
# Wed, 24 Feb 2021 20:45:16 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 21:58:48 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 24 Feb 2021 21:58:53 GMT
ENV HAPROXY_VERSION=1.7.12
# Wed, 24 Feb 2021 21:59:00 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.7/src/haproxy-1.7.12.tar.gz
# Wed, 24 Feb 2021 21:59:06 GMT
ENV HAPROXY_SHA256=4118178b553a107b227f3f84774c7a50ae0b3ac2be39211c3db511ed4efe48ce
# Wed, 24 Feb 2021 21:59:47 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		CFLAGS+="-Wno-address-of-packed-member" 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 24 Feb 2021 22:00:08 GMT
STOPSIGNAL SIGUSR1
# Wed, 24 Feb 2021 22:00:21 GMT
COPY file:9a05f2c8b43e780abf69d813f7c45613cced5481a65611bf8127c6f222dff4e3 in /usr/local/bin/ 
# Wed, 24 Feb 2021 22:00:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 24 Feb 2021 22:00:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Feb 2021 22:01:09 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:8f446c8f22d4a7a7520099080f73ffa6f455358a840b542fb2ad15c0032adeca`  
		Last Modified: Wed, 24 Feb 2021 20:46:19 GMT  
		Size: 2.8 MB (2805893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49409cae7ffcdac55e8540a510a9881e2a1b02456f2b2ca53a259c9c0e8d40bb`  
		Last Modified: Wed, 24 Feb 2021 22:02:09 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97c56ebfda965b4db03d2725117a2f39dd5483e297f554e0cf243fda19a7f03`  
		Last Modified: Wed, 24 Feb 2021 22:02:08 GMT  
		Size: 764.2 KB (764200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf682249844618c74f6af602f0eb6759224dba6571d2836b799fa744fcd1c47`  
		Last Modified: Wed, 24 Feb 2021 22:02:07 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bebdfd12abd3da40fd7f6691974c8a2c1a3d6033cce0d11f64a7203e55fdbb59`  
		Last Modified: Wed, 24 Feb 2021 22:02:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.7-alpine` - linux; s390x

```console
$ docker pull haproxy@sha256:3df8a3e4ac9b633a10d8aba0019b95fbda1692dcaa5b4230e047a39e841b60b2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dce9becf960ae76ae83bddc9c4307c44e234f714f807f7fc2b508f93ffaa39df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 24 Feb 2021 20:42:00 GMT
ADD file:ad5b3d24d5412d341e932d4497614d564c9c413984feaf8542113d6674b34b53 in / 
# Wed, 24 Feb 2021 20:42:01 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 21:34:41 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 24 Feb 2021 21:34:41 GMT
ENV HAPROXY_VERSION=1.7.12
# Wed, 24 Feb 2021 21:34:42 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.7/src/haproxy-1.7.12.tar.gz
# Wed, 24 Feb 2021 21:34:43 GMT
ENV HAPROXY_SHA256=4118178b553a107b227f3f84774c7a50ae0b3ac2be39211c3db511ed4efe48ce
# Wed, 24 Feb 2021 21:34:54 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		CFLAGS+="-Wno-address-of-packed-member" 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 24 Feb 2021 21:34:54 GMT
STOPSIGNAL SIGUSR1
# Wed, 24 Feb 2021 21:34:55 GMT
COPY file:9a05f2c8b43e780abf69d813f7c45613cced5481a65611bf8127c6f222dff4e3 in /usr/local/bin/ 
# Wed, 24 Feb 2021 21:34:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 24 Feb 2021 21:34:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Feb 2021 21:34:58 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:84a604a54099b51a6c81db20dff8dc298ec82555e772be84328b067d3f35a93e`  
		Last Modified: Wed, 24 Feb 2021 20:42:40 GMT  
		Size: 2.6 MB (2567318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dc235c40a316f4f9079fd34b0dc756150ccabb41d754a8729dab3dedcb1e04f`  
		Last Modified: Wed, 24 Feb 2021 21:35:59 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75d3725f63f840237a91bc09312ba6d3f460634ee68acfbe8b898e48c123feb6`  
		Last Modified: Wed, 24 Feb 2021 21:35:59 GMT  
		Size: 774.5 KB (774519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33bca3d370726bef307d76fbf3e232dfb7751a2b0b340ca8230b85c572e5cb2d`  
		Last Modified: Wed, 24 Feb 2021 21:35:59 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2279b0ba34ec524e4df62f438e695042f6665fb646c3995d1ce98fcfabaae677`  
		Last Modified: Wed, 24 Feb 2021 21:35:59 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haproxy:1.8`

```console
$ docker pull haproxy@sha256:65e46f5742129c62876c50a010a0395da7827b6c088b43580ffafa6b2afe2da5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `haproxy:1.8` - linux; amd64

```console
$ docker pull haproxy@sha256:41a073089a901b4c751f93ce00474cf931cb470ea6602f6cea9dcdfd00ba5637
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33733805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6f5ac621a6c7d82ca756a2fb259a5725c79b4435d98bbb6e0a13cdcc9c491df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Mon, 08 Mar 2021 21:37:25 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 21:49:19 GMT
ENV HAPROXY_VERSION=1.8.28
# Mon, 08 Mar 2021 21:49:20 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.8/src/haproxy-1.8.28.tar.gz
# Mon, 08 Mar 2021 21:49:20 GMT
ENV HAPROXY_SHA256=fecf031486014d5838499f69cba0348abffa076e55f6fadf86a8da93cbf94e89
# Mon, 08 Mar 2021 21:50:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 08 Mar 2021 21:50:04 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 21:50:04 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 21:50:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 08 Mar 2021 21:50:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 21:50:06 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7bca45a971fe608786870ce75c9976f8e5a958f55e1287a6120048b897c63b6`  
		Last Modified: Mon, 08 Mar 2021 21:52:33 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea7751df38bd766a1d0e1b23049b096a8fc48eb31a9c005ad23036a4394830c`  
		Last Modified: Mon, 08 Mar 2021 21:55:04 GMT  
		Size: 6.6 MB (6636712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30349bedac426a897c6600875c6dd8eb913e17679b49deefa0436441e1e9c359`  
		Last Modified: Mon, 08 Mar 2021 21:54:59 GMT  
		Size: 454.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ca0ffa545feae21748efcc1bc5887d5d4969f22832dfc04710231283360f3a4`  
		Last Modified: Mon, 08 Mar 2021 21:54:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.8` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:70f74c199ffd51822bd6fcb82f633e5c01295ff4bd2e82e3fd54c85501fad31f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31057008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f696bc2c238868ffc11bf39e92a96438340b77416740e55c160303447acc16b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:50:10 GMT
ADD file:fbd00ef7871dc27d7ed5fa8c238cdc80652bd87b8033be7de9e54a799bbf10a4 in / 
# Tue, 09 Feb 2021 02:50:11 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:45:24 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 09 Feb 2021 03:52:20 GMT
ENV HAPROXY_VERSION=1.8.28
# Tue, 09 Feb 2021 03:52:22 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.8/src/haproxy-1.8.28.tar.gz
# Tue, 09 Feb 2021 03:52:23 GMT
ENV HAPROXY_SHA256=fecf031486014d5838499f69cba0348abffa076e55f6fadf86a8da93cbf94e89
# Tue, 09 Feb 2021 03:53:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 09 Feb 2021 03:53:12 GMT
STOPSIGNAL SIGUSR1
# Tue, 09 Feb 2021 03:53:13 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 09 Feb 2021 03:53:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 09 Feb 2021 03:53:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Feb 2021 03:53:19 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:8e683fcc73f4da7d69ce1d5f4e1d77510aa459490068f38db2d8663698b391a0`  
		Last Modified: Tue, 09 Feb 2021 02:59:07 GMT  
		Size: 24.8 MB (24839297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def565d52deae74587a55f60d168bd531ebe8095c594027b7057a8fc1be0e8af`  
		Last Modified: Tue, 09 Feb 2021 03:54:54 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7832243e64e8d632c0412491e96014b8f8e8865baf66a7e48a022983d67dd9c4`  
		Last Modified: Tue, 09 Feb 2021 03:55:50 GMT  
		Size: 6.2 MB (6215767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd83f21270498cb39474793c8a7646ad3794ab7aa54d15f97f1a2f81de676365`  
		Last Modified: Tue, 09 Feb 2021 03:55:48 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:553afa23a9968a26fb8d09453f16362df92bf56ca382741ab753d3bf8c627305`  
		Last Modified: Tue, 09 Feb 2021 03:55:48 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.8` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:f6467db82009fea4776b32062f2aeb06a0ac8a544a6a116db243b5a77e7b8b9e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.8 MB (28761659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad0e28ae7d64f67a621b923b6b550bf72ea7dc337bcc766a914b522d08cfa1b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 03:00:57 GMT
ADD file:e675d50366bde57173a75f9a29367d765e7da2b7254c5254b64e777cf6870502 in / 
# Tue, 09 Feb 2021 03:01:00 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:49:38 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 09 Feb 2021 03:55:37 GMT
ENV HAPROXY_VERSION=1.8.28
# Tue, 09 Feb 2021 03:55:38 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.8/src/haproxy-1.8.28.tar.gz
# Tue, 09 Feb 2021 03:55:38 GMT
ENV HAPROXY_SHA256=fecf031486014d5838499f69cba0348abffa076e55f6fadf86a8da93cbf94e89
# Tue, 09 Feb 2021 03:56:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 09 Feb 2021 03:56:18 GMT
STOPSIGNAL SIGUSR1
# Tue, 09 Feb 2021 03:56:19 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 09 Feb 2021 03:56:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 09 Feb 2021 03:56:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Feb 2021 03:56:23 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:db574d82360c3b60abadbef4f3daf8dee01f24741fc6ab3692aa543558d8b624`  
		Last Modified: Tue, 09 Feb 2021 03:09:46 GMT  
		Size: 22.7 MB (22703384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9978ebb1881387f11e025fb46dce2b3c715f705f6d240737574f8848c27fa0d7`  
		Last Modified: Tue, 09 Feb 2021 03:58:16 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9ef0deb6ee2afcf9f2a5a6112dabe6690d317315f200824080ced001412bf9`  
		Last Modified: Tue, 09 Feb 2021 03:59:15 GMT  
		Size: 6.1 MB (6056334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e0140d5a01a264f289e8fe7e57073b0f4aa3e5b1130f54451047f403c2a4664`  
		Last Modified: Tue, 09 Feb 2021 03:59:13 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:539622d3e1238a54ef634670bf4b38d5862affa2242983133e6ba283ae43fcc4`  
		Last Modified: Tue, 09 Feb 2021 03:59:13 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.8` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:e4d6f93ecb59bafc4d8e94a3e42b61b8e30369fee9f2d0a2287d8ab609b3ac08
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32290951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3799a5c534aa9981c3df51242fc0631310fcd4450b48b6ceb009abe0e117926`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:41:10 GMT
ADD file:d906dedaf14d8e3874b46787f7a1dbf268bc124c4e1dd32f13f3079e12f22238 in / 
# Tue, 09 Feb 2021 02:41:13 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:59:41 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 09 Feb 2021 04:05:55 GMT
ENV HAPROXY_VERSION=1.8.28
# Tue, 09 Feb 2021 04:05:56 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.8/src/haproxy-1.8.28.tar.gz
# Tue, 09 Feb 2021 04:05:57 GMT
ENV HAPROXY_SHA256=fecf031486014d5838499f69cba0348abffa076e55f6fadf86a8da93cbf94e89
# Tue, 09 Feb 2021 04:06:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 09 Feb 2021 04:06:40 GMT
STOPSIGNAL SIGUSR1
# Tue, 09 Feb 2021 04:06:40 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 09 Feb 2021 04:06:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 09 Feb 2021 04:06:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Feb 2021 04:06:44 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:83c5cfdaa5385ea6fc4d31e724fd4dc5d74de847a7bdd968555b8f2c558dac0e`  
		Last Modified: Tue, 09 Feb 2021 02:47:27 GMT  
		Size: 25.9 MB (25851449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b7f43dd52365bce2c2b75f29577aa39d2b5794e2561cddc0678422ffc1f7d15`  
		Last Modified: Tue, 09 Feb 2021 04:08:36 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce51e8165fb548e8dd6b32e10f8a905f72e2ef75459fd15e012678aca49ddc8c`  
		Last Modified: Tue, 09 Feb 2021 04:09:33 GMT  
		Size: 6.4 MB (6437557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:186c550f124ad2c6b80d061db7a4a6fba05340b7a512c4161f82828da2531e5d`  
		Last Modified: Tue, 09 Feb 2021 04:09:33 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff1a475f2cc8cea0a84d223889e1d3134d90bd5ec1793440cf10a4c8a9366eb`  
		Last Modified: Tue, 09 Feb 2021 04:09:32 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.8` - linux; 386

```console
$ docker pull haproxy@sha256:7dc87a15a924d5134f279d34923f384e58f863d56840003d5a568eee427c026e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34319934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09bc018f69ae109e22f9054f2f305bc99fd46c2e28d5adf86d9d6ea436c8e2d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:39:47 GMT
ADD file:61c31b1037672781ed0ecbc080ee3d49c83af49f5578b011544513fa9625698d in / 
# Tue, 09 Feb 2021 02:39:47 GMT
CMD ["bash"]
# Mon, 08 Mar 2021 22:02:40 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 22:13:54 GMT
ENV HAPROXY_VERSION=1.8.28
# Mon, 08 Mar 2021 22:13:54 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.8/src/haproxy-1.8.28.tar.gz
# Mon, 08 Mar 2021 22:13:54 GMT
ENV HAPROXY_SHA256=fecf031486014d5838499f69cba0348abffa076e55f6fadf86a8da93cbf94e89
# Mon, 08 Mar 2021 22:14:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 08 Mar 2021 22:14:32 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 22:14:32 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 22:14:33 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 08 Mar 2021 22:14:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 22:14:33 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:27cbb00346a16ea900c1049a2e5b47942c586c377179e098382c8ca1c8e87966`  
		Last Modified: Tue, 09 Feb 2021 02:45:51 GMT  
		Size: 27.8 MB (27752731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b6129a97a33727ea8a598d1e797bccce491920bf29d769880cf2fc6d3e0436`  
		Last Modified: Mon, 08 Mar 2021 22:17:48 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8313c57de9caed3ce74f28a1d34e6409a0e718c87de578eb6bb7e369fe894dc5`  
		Last Modified: Mon, 08 Mar 2021 22:20:17 GMT  
		Size: 6.6 MB (6565263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3f88d7e56c937f3b373b3f51e244e1afd8ae0e09e61c16129ff7a9335574ed2`  
		Last Modified: Mon, 08 Mar 2021 22:20:14 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd26618fbf4f9a7ce719f38ebdc73d1297b488fff2ef34fac7dc3d68e34a7fd0`  
		Last Modified: Mon, 08 Mar 2021 22:20:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.8` - linux; mips64le

```console
$ docker pull haproxy@sha256:4eee103fccbe2fa7a9794b3719f4d9c8da4b494b65497faf75748c988584fc5d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.9 MB (31894310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f44515bf18217c2a8b338230d3a5d9631afcc27b8ea674cd9c3090759a9d4a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 03:09:26 GMT
ADD file:0222a151f4e5033d9eae98ce2b703a63f52d049dd72ac40bdd0dc2dafe619f0a in / 
# Tue, 09 Feb 2021 03:09:27 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:41:09 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 09 Feb 2021 03:54:03 GMT
ENV HAPROXY_VERSION=1.8.28
# Tue, 09 Feb 2021 03:54:03 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.8/src/haproxy-1.8.28.tar.gz
# Tue, 09 Feb 2021 03:54:04 GMT
ENV HAPROXY_SHA256=fecf031486014d5838499f69cba0348abffa076e55f6fadf86a8da93cbf94e89
# Tue, 09 Feb 2021 03:55:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 09 Feb 2021 03:55:44 GMT
STOPSIGNAL SIGUSR1
# Tue, 09 Feb 2021 03:55:44 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 09 Feb 2021 03:55:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 09 Feb 2021 03:55:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Feb 2021 03:55:47 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:dfb81134097d874e01b495d1fba82e384056d0a3a45f01a69a2e86ae82af1e96`  
		Last Modified: Tue, 09 Feb 2021 03:15:55 GMT  
		Size: 25.8 MB (25764640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a549d56662447dd8cb15faf59ca0fc2eda7a877e9aee16aadd09fd46e4214a`  
		Last Modified: Tue, 09 Feb 2021 03:57:56 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:836737511cc6a81d4610ab50fce6cdb2db608bc8d444d78ca871447bbf2f35fc`  
		Last Modified: Tue, 09 Feb 2021 03:59:30 GMT  
		Size: 6.1 MB (6127722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7614c03a53b3e903ff643669609411df6300109548c817531ed8beef909d16b5`  
		Last Modified: Tue, 09 Feb 2021 03:59:26 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30703ad990db565f73764723a60caf0a0f203afb4b3c8a5fdcf3a2b2b75de1c2`  
		Last Modified: Tue, 09 Feb 2021 03:59:25 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.8` - linux; ppc64le

```console
$ docker pull haproxy@sha256:a7b9aa91142ceebe19207a13de2745aca20d9a312e1c73aad483259762972497
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.4 MB (37449094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92f6e55c3e13540a0fa36ef28a82b7e676dfcafb6689651cd59508b6d580a47d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:19:19 GMT
ADD file:9a8cfdf0eab394a693b5cde0700ad47b6e8506ef0b79fabb8a07874b96e6c394 in / 
# Tue, 09 Feb 2021 02:19:34 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 05:52:23 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 09 Feb 2021 06:24:18 GMT
ENV HAPROXY_VERSION=1.8.28
# Tue, 09 Feb 2021 06:24:31 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.8/src/haproxy-1.8.28.tar.gz
# Tue, 09 Feb 2021 06:24:34 GMT
ENV HAPROXY_SHA256=fecf031486014d5838499f69cba0348abffa076e55f6fadf86a8da93cbf94e89
# Tue, 09 Feb 2021 06:29:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 09 Feb 2021 06:30:05 GMT
STOPSIGNAL SIGUSR1
# Tue, 09 Feb 2021 06:30:11 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 09 Feb 2021 06:30:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 09 Feb 2021 06:30:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Feb 2021 06:31:00 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:9996b4fb6bc1c50f95ba30f8988c9c89526556fa320d3fda59d3d8359f7810d6`  
		Last Modified: Tue, 09 Feb 2021 02:27:59 GMT  
		Size: 30.5 MB (30519509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7f600bc4989eb9f12d5006a73f5958eb4fe85f86bc4008d7a899bb935b0f1c`  
		Last Modified: Tue, 09 Feb 2021 06:38:36 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c3b6f6a74b11a02230c295e565bcc4e3e2f13791bca735621e33848beb97d60`  
		Last Modified: Tue, 09 Feb 2021 06:39:52 GMT  
		Size: 6.9 MB (6927641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cd65624071b3b01d302a6933004d66192c40846c1290993d93609b26827076f`  
		Last Modified: Tue, 09 Feb 2021 06:39:48 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f65d578d418eadb71efadc7f59c21ff98e5d67519ba032ea90e24bdff66ff934`  
		Last Modified: Tue, 09 Feb 2021 06:39:48 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.8` - linux; s390x

```console
$ docker pull haproxy@sha256:953e4a55b3aa3e377031d15d27308d55128cca5bc0a06906d07242c09c4cc6b3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.9 MB (31926104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fa0630bd5bf1d8a1bcc61886ed54072109f754704b44d592ccbfe152fdbdb14`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:42:10 GMT
ADD file:0edb2de05df54191a141bd125f59d7e14eef0cc4576927a247b8dd7d6f255d04 in / 
# Tue, 09 Feb 2021 02:42:12 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:39:30 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 09 Feb 2021 03:42:58 GMT
ENV HAPROXY_VERSION=1.8.28
# Tue, 09 Feb 2021 03:42:58 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.8/src/haproxy-1.8.28.tar.gz
# Tue, 09 Feb 2021 03:42:58 GMT
ENV HAPROXY_SHA256=fecf031486014d5838499f69cba0348abffa076e55f6fadf86a8da93cbf94e89
# Tue, 09 Feb 2021 03:43:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 09 Feb 2021 03:43:20 GMT
STOPSIGNAL SIGUSR1
# Tue, 09 Feb 2021 03:43:20 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 09 Feb 2021 03:43:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 09 Feb 2021 03:43:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Feb 2021 03:43:21 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:032413a44cf56b097e48b8221bf475ca1bec26e7a27f35fe61d699366a335b79`  
		Last Modified: Tue, 09 Feb 2021 02:45:31 GMT  
		Size: 25.7 MB (25710021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e65f701864562492efa2c0035134b62d68efdb6e7241a0a2dcc3151e6d5775b`  
		Last Modified: Tue, 09 Feb 2021 03:44:28 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0f934921384073c2d651d6aaa64e42402cc3d0a68e6c44a7c50148b92625dc8`  
		Last Modified: Tue, 09 Feb 2021 03:45:21 GMT  
		Size: 6.2 MB (6214140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85ca77e5cdb73ea10f8a7cbf994901e997eb57d0ed190c099c623f08d80e0326`  
		Last Modified: Tue, 09 Feb 2021 03:45:20 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9ed39651b93dfe915280e7472ceaf1d70a00b1e483ff7cc0e32d18c7c4cc3be`  
		Last Modified: Tue, 09 Feb 2021 03:45:20 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haproxy:1.8.28`

```console
$ docker pull haproxy@sha256:65e46f5742129c62876c50a010a0395da7827b6c088b43580ffafa6b2afe2da5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `haproxy:1.8.28` - linux; amd64

```console
$ docker pull haproxy@sha256:41a073089a901b4c751f93ce00474cf931cb470ea6602f6cea9dcdfd00ba5637
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33733805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6f5ac621a6c7d82ca756a2fb259a5725c79b4435d98bbb6e0a13cdcc9c491df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Mon, 08 Mar 2021 21:37:25 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 21:49:19 GMT
ENV HAPROXY_VERSION=1.8.28
# Mon, 08 Mar 2021 21:49:20 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.8/src/haproxy-1.8.28.tar.gz
# Mon, 08 Mar 2021 21:49:20 GMT
ENV HAPROXY_SHA256=fecf031486014d5838499f69cba0348abffa076e55f6fadf86a8da93cbf94e89
# Mon, 08 Mar 2021 21:50:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 08 Mar 2021 21:50:04 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 21:50:04 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 21:50:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 08 Mar 2021 21:50:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 21:50:06 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7bca45a971fe608786870ce75c9976f8e5a958f55e1287a6120048b897c63b6`  
		Last Modified: Mon, 08 Mar 2021 21:52:33 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea7751df38bd766a1d0e1b23049b096a8fc48eb31a9c005ad23036a4394830c`  
		Last Modified: Mon, 08 Mar 2021 21:55:04 GMT  
		Size: 6.6 MB (6636712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30349bedac426a897c6600875c6dd8eb913e17679b49deefa0436441e1e9c359`  
		Last Modified: Mon, 08 Mar 2021 21:54:59 GMT  
		Size: 454.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ca0ffa545feae21748efcc1bc5887d5d4969f22832dfc04710231283360f3a4`  
		Last Modified: Mon, 08 Mar 2021 21:54:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.8.28` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:70f74c199ffd51822bd6fcb82f633e5c01295ff4bd2e82e3fd54c85501fad31f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31057008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f696bc2c238868ffc11bf39e92a96438340b77416740e55c160303447acc16b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:50:10 GMT
ADD file:fbd00ef7871dc27d7ed5fa8c238cdc80652bd87b8033be7de9e54a799bbf10a4 in / 
# Tue, 09 Feb 2021 02:50:11 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:45:24 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 09 Feb 2021 03:52:20 GMT
ENV HAPROXY_VERSION=1.8.28
# Tue, 09 Feb 2021 03:52:22 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.8/src/haproxy-1.8.28.tar.gz
# Tue, 09 Feb 2021 03:52:23 GMT
ENV HAPROXY_SHA256=fecf031486014d5838499f69cba0348abffa076e55f6fadf86a8da93cbf94e89
# Tue, 09 Feb 2021 03:53:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 09 Feb 2021 03:53:12 GMT
STOPSIGNAL SIGUSR1
# Tue, 09 Feb 2021 03:53:13 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 09 Feb 2021 03:53:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 09 Feb 2021 03:53:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Feb 2021 03:53:19 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:8e683fcc73f4da7d69ce1d5f4e1d77510aa459490068f38db2d8663698b391a0`  
		Last Modified: Tue, 09 Feb 2021 02:59:07 GMT  
		Size: 24.8 MB (24839297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def565d52deae74587a55f60d168bd531ebe8095c594027b7057a8fc1be0e8af`  
		Last Modified: Tue, 09 Feb 2021 03:54:54 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7832243e64e8d632c0412491e96014b8f8e8865baf66a7e48a022983d67dd9c4`  
		Last Modified: Tue, 09 Feb 2021 03:55:50 GMT  
		Size: 6.2 MB (6215767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd83f21270498cb39474793c8a7646ad3794ab7aa54d15f97f1a2f81de676365`  
		Last Modified: Tue, 09 Feb 2021 03:55:48 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:553afa23a9968a26fb8d09453f16362df92bf56ca382741ab753d3bf8c627305`  
		Last Modified: Tue, 09 Feb 2021 03:55:48 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.8.28` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:f6467db82009fea4776b32062f2aeb06a0ac8a544a6a116db243b5a77e7b8b9e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.8 MB (28761659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad0e28ae7d64f67a621b923b6b550bf72ea7dc337bcc766a914b522d08cfa1b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 03:00:57 GMT
ADD file:e675d50366bde57173a75f9a29367d765e7da2b7254c5254b64e777cf6870502 in / 
# Tue, 09 Feb 2021 03:01:00 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:49:38 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 09 Feb 2021 03:55:37 GMT
ENV HAPROXY_VERSION=1.8.28
# Tue, 09 Feb 2021 03:55:38 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.8/src/haproxy-1.8.28.tar.gz
# Tue, 09 Feb 2021 03:55:38 GMT
ENV HAPROXY_SHA256=fecf031486014d5838499f69cba0348abffa076e55f6fadf86a8da93cbf94e89
# Tue, 09 Feb 2021 03:56:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 09 Feb 2021 03:56:18 GMT
STOPSIGNAL SIGUSR1
# Tue, 09 Feb 2021 03:56:19 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 09 Feb 2021 03:56:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 09 Feb 2021 03:56:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Feb 2021 03:56:23 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:db574d82360c3b60abadbef4f3daf8dee01f24741fc6ab3692aa543558d8b624`  
		Last Modified: Tue, 09 Feb 2021 03:09:46 GMT  
		Size: 22.7 MB (22703384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9978ebb1881387f11e025fb46dce2b3c715f705f6d240737574f8848c27fa0d7`  
		Last Modified: Tue, 09 Feb 2021 03:58:16 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9ef0deb6ee2afcf9f2a5a6112dabe6690d317315f200824080ced001412bf9`  
		Last Modified: Tue, 09 Feb 2021 03:59:15 GMT  
		Size: 6.1 MB (6056334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e0140d5a01a264f289e8fe7e57073b0f4aa3e5b1130f54451047f403c2a4664`  
		Last Modified: Tue, 09 Feb 2021 03:59:13 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:539622d3e1238a54ef634670bf4b38d5862affa2242983133e6ba283ae43fcc4`  
		Last Modified: Tue, 09 Feb 2021 03:59:13 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.8.28` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:e4d6f93ecb59bafc4d8e94a3e42b61b8e30369fee9f2d0a2287d8ab609b3ac08
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32290951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3799a5c534aa9981c3df51242fc0631310fcd4450b48b6ceb009abe0e117926`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:41:10 GMT
ADD file:d906dedaf14d8e3874b46787f7a1dbf268bc124c4e1dd32f13f3079e12f22238 in / 
# Tue, 09 Feb 2021 02:41:13 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:59:41 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 09 Feb 2021 04:05:55 GMT
ENV HAPROXY_VERSION=1.8.28
# Tue, 09 Feb 2021 04:05:56 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.8/src/haproxy-1.8.28.tar.gz
# Tue, 09 Feb 2021 04:05:57 GMT
ENV HAPROXY_SHA256=fecf031486014d5838499f69cba0348abffa076e55f6fadf86a8da93cbf94e89
# Tue, 09 Feb 2021 04:06:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 09 Feb 2021 04:06:40 GMT
STOPSIGNAL SIGUSR1
# Tue, 09 Feb 2021 04:06:40 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 09 Feb 2021 04:06:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 09 Feb 2021 04:06:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Feb 2021 04:06:44 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:83c5cfdaa5385ea6fc4d31e724fd4dc5d74de847a7bdd968555b8f2c558dac0e`  
		Last Modified: Tue, 09 Feb 2021 02:47:27 GMT  
		Size: 25.9 MB (25851449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b7f43dd52365bce2c2b75f29577aa39d2b5794e2561cddc0678422ffc1f7d15`  
		Last Modified: Tue, 09 Feb 2021 04:08:36 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce51e8165fb548e8dd6b32e10f8a905f72e2ef75459fd15e012678aca49ddc8c`  
		Last Modified: Tue, 09 Feb 2021 04:09:33 GMT  
		Size: 6.4 MB (6437557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:186c550f124ad2c6b80d061db7a4a6fba05340b7a512c4161f82828da2531e5d`  
		Last Modified: Tue, 09 Feb 2021 04:09:33 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff1a475f2cc8cea0a84d223889e1d3134d90bd5ec1793440cf10a4c8a9366eb`  
		Last Modified: Tue, 09 Feb 2021 04:09:32 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.8.28` - linux; 386

```console
$ docker pull haproxy@sha256:7dc87a15a924d5134f279d34923f384e58f863d56840003d5a568eee427c026e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34319934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09bc018f69ae109e22f9054f2f305bc99fd46c2e28d5adf86d9d6ea436c8e2d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:39:47 GMT
ADD file:61c31b1037672781ed0ecbc080ee3d49c83af49f5578b011544513fa9625698d in / 
# Tue, 09 Feb 2021 02:39:47 GMT
CMD ["bash"]
# Mon, 08 Mar 2021 22:02:40 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 22:13:54 GMT
ENV HAPROXY_VERSION=1.8.28
# Mon, 08 Mar 2021 22:13:54 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.8/src/haproxy-1.8.28.tar.gz
# Mon, 08 Mar 2021 22:13:54 GMT
ENV HAPROXY_SHA256=fecf031486014d5838499f69cba0348abffa076e55f6fadf86a8da93cbf94e89
# Mon, 08 Mar 2021 22:14:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 08 Mar 2021 22:14:32 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 22:14:32 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 22:14:33 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 08 Mar 2021 22:14:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 22:14:33 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:27cbb00346a16ea900c1049a2e5b47942c586c377179e098382c8ca1c8e87966`  
		Last Modified: Tue, 09 Feb 2021 02:45:51 GMT  
		Size: 27.8 MB (27752731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b6129a97a33727ea8a598d1e797bccce491920bf29d769880cf2fc6d3e0436`  
		Last Modified: Mon, 08 Mar 2021 22:17:48 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8313c57de9caed3ce74f28a1d34e6409a0e718c87de578eb6bb7e369fe894dc5`  
		Last Modified: Mon, 08 Mar 2021 22:20:17 GMT  
		Size: 6.6 MB (6565263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3f88d7e56c937f3b373b3f51e244e1afd8ae0e09e61c16129ff7a9335574ed2`  
		Last Modified: Mon, 08 Mar 2021 22:20:14 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd26618fbf4f9a7ce719f38ebdc73d1297b488fff2ef34fac7dc3d68e34a7fd0`  
		Last Modified: Mon, 08 Mar 2021 22:20:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.8.28` - linux; mips64le

```console
$ docker pull haproxy@sha256:4eee103fccbe2fa7a9794b3719f4d9c8da4b494b65497faf75748c988584fc5d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.9 MB (31894310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f44515bf18217c2a8b338230d3a5d9631afcc27b8ea674cd9c3090759a9d4a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 03:09:26 GMT
ADD file:0222a151f4e5033d9eae98ce2b703a63f52d049dd72ac40bdd0dc2dafe619f0a in / 
# Tue, 09 Feb 2021 03:09:27 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:41:09 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 09 Feb 2021 03:54:03 GMT
ENV HAPROXY_VERSION=1.8.28
# Tue, 09 Feb 2021 03:54:03 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.8/src/haproxy-1.8.28.tar.gz
# Tue, 09 Feb 2021 03:54:04 GMT
ENV HAPROXY_SHA256=fecf031486014d5838499f69cba0348abffa076e55f6fadf86a8da93cbf94e89
# Tue, 09 Feb 2021 03:55:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 09 Feb 2021 03:55:44 GMT
STOPSIGNAL SIGUSR1
# Tue, 09 Feb 2021 03:55:44 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 09 Feb 2021 03:55:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 09 Feb 2021 03:55:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Feb 2021 03:55:47 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:dfb81134097d874e01b495d1fba82e384056d0a3a45f01a69a2e86ae82af1e96`  
		Last Modified: Tue, 09 Feb 2021 03:15:55 GMT  
		Size: 25.8 MB (25764640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a549d56662447dd8cb15faf59ca0fc2eda7a877e9aee16aadd09fd46e4214a`  
		Last Modified: Tue, 09 Feb 2021 03:57:56 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:836737511cc6a81d4610ab50fce6cdb2db608bc8d444d78ca871447bbf2f35fc`  
		Last Modified: Tue, 09 Feb 2021 03:59:30 GMT  
		Size: 6.1 MB (6127722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7614c03a53b3e903ff643669609411df6300109548c817531ed8beef909d16b5`  
		Last Modified: Tue, 09 Feb 2021 03:59:26 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30703ad990db565f73764723a60caf0a0f203afb4b3c8a5fdcf3a2b2b75de1c2`  
		Last Modified: Tue, 09 Feb 2021 03:59:25 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.8.28` - linux; ppc64le

```console
$ docker pull haproxy@sha256:a7b9aa91142ceebe19207a13de2745aca20d9a312e1c73aad483259762972497
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.4 MB (37449094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92f6e55c3e13540a0fa36ef28a82b7e676dfcafb6689651cd59508b6d580a47d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:19:19 GMT
ADD file:9a8cfdf0eab394a693b5cde0700ad47b6e8506ef0b79fabb8a07874b96e6c394 in / 
# Tue, 09 Feb 2021 02:19:34 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 05:52:23 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 09 Feb 2021 06:24:18 GMT
ENV HAPROXY_VERSION=1.8.28
# Tue, 09 Feb 2021 06:24:31 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.8/src/haproxy-1.8.28.tar.gz
# Tue, 09 Feb 2021 06:24:34 GMT
ENV HAPROXY_SHA256=fecf031486014d5838499f69cba0348abffa076e55f6fadf86a8da93cbf94e89
# Tue, 09 Feb 2021 06:29:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 09 Feb 2021 06:30:05 GMT
STOPSIGNAL SIGUSR1
# Tue, 09 Feb 2021 06:30:11 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 09 Feb 2021 06:30:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 09 Feb 2021 06:30:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Feb 2021 06:31:00 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:9996b4fb6bc1c50f95ba30f8988c9c89526556fa320d3fda59d3d8359f7810d6`  
		Last Modified: Tue, 09 Feb 2021 02:27:59 GMT  
		Size: 30.5 MB (30519509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7f600bc4989eb9f12d5006a73f5958eb4fe85f86bc4008d7a899bb935b0f1c`  
		Last Modified: Tue, 09 Feb 2021 06:38:36 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c3b6f6a74b11a02230c295e565bcc4e3e2f13791bca735621e33848beb97d60`  
		Last Modified: Tue, 09 Feb 2021 06:39:52 GMT  
		Size: 6.9 MB (6927641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cd65624071b3b01d302a6933004d66192c40846c1290993d93609b26827076f`  
		Last Modified: Tue, 09 Feb 2021 06:39:48 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f65d578d418eadb71efadc7f59c21ff98e5d67519ba032ea90e24bdff66ff934`  
		Last Modified: Tue, 09 Feb 2021 06:39:48 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.8.28` - linux; s390x

```console
$ docker pull haproxy@sha256:953e4a55b3aa3e377031d15d27308d55128cca5bc0a06906d07242c09c4cc6b3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.9 MB (31926104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fa0630bd5bf1d8a1bcc61886ed54072109f754704b44d592ccbfe152fdbdb14`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:42:10 GMT
ADD file:0edb2de05df54191a141bd125f59d7e14eef0cc4576927a247b8dd7d6f255d04 in / 
# Tue, 09 Feb 2021 02:42:12 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:39:30 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 09 Feb 2021 03:42:58 GMT
ENV HAPROXY_VERSION=1.8.28
# Tue, 09 Feb 2021 03:42:58 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.8/src/haproxy-1.8.28.tar.gz
# Tue, 09 Feb 2021 03:42:58 GMT
ENV HAPROXY_SHA256=fecf031486014d5838499f69cba0348abffa076e55f6fadf86a8da93cbf94e89
# Tue, 09 Feb 2021 03:43:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 09 Feb 2021 03:43:20 GMT
STOPSIGNAL SIGUSR1
# Tue, 09 Feb 2021 03:43:20 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 09 Feb 2021 03:43:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 09 Feb 2021 03:43:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Feb 2021 03:43:21 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:032413a44cf56b097e48b8221bf475ca1bec26e7a27f35fe61d699366a335b79`  
		Last Modified: Tue, 09 Feb 2021 02:45:31 GMT  
		Size: 25.7 MB (25710021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e65f701864562492efa2c0035134b62d68efdb6e7241a0a2dcc3151e6d5775b`  
		Last Modified: Tue, 09 Feb 2021 03:44:28 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0f934921384073c2d651d6aaa64e42402cc3d0a68e6c44a7c50148b92625dc8`  
		Last Modified: Tue, 09 Feb 2021 03:45:21 GMT  
		Size: 6.2 MB (6214140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85ca77e5cdb73ea10f8a7cbf994901e997eb57d0ed190c099c623f08d80e0326`  
		Last Modified: Tue, 09 Feb 2021 03:45:20 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9ed39651b93dfe915280e7472ceaf1d70a00b1e483ff7cc0e32d18c7c4cc3be`  
		Last Modified: Tue, 09 Feb 2021 03:45:20 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haproxy:1.8.28-alpine`

```console
$ docker pull haproxy@sha256:145db50918a363b727c439ecc4bb71185556e45a7806a920b8bb89a92104e5c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `haproxy:1.8.28-alpine` - linux; amd64

```console
$ docker pull haproxy@sha256:4e73aa036e0743d00ae74c680d725d740677fff1cafc74276789ce7e5cfdb6b9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6779328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d817987db6b8c3ca596b41050d0d0cb3aa95d20ed221f6a4b6827f11a746d05`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 21:19:54 GMT
ADD file:80bf8bd014071345b1c0364eeb0a5e48f3fb0d87f9c31cb990e57caa652b59b8 in / 
# Wed, 17 Feb 2021 21:19:54 GMT
CMD ["/bin/sh"]
# Mon, 08 Mar 2021 21:38:26 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 21:50:10 GMT
ENV HAPROXY_VERSION=1.8.28
# Mon, 08 Mar 2021 21:50:10 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.8/src/haproxy-1.8.28.tar.gz
# Mon, 08 Mar 2021 21:50:10 GMT
ENV HAPROXY_SHA256=fecf031486014d5838499f69cba0348abffa076e55f6fadf86a8da93cbf94e89
# Mon, 08 Mar 2021 21:50:47 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Mon, 08 Mar 2021 21:50:47 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 21:50:47 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 21:50:48 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 08 Mar 2021 21:50:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 21:50:49 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:ba3557a56b150f9b813f9d02274d62914fd8fce120dd374d9ee17b87cf1d277d`  
		Last Modified: Wed, 17 Feb 2021 21:20:25 GMT  
		Size: 2.8 MB (2811657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9216237f12c4d44ab183590086cf2a09004b5609c4b50871d88658faa495245`  
		Last Modified: Mon, 08 Mar 2021 21:52:45 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c572dcfde483c47a4b14c7a2ed93c00a6986bec0f20a81ec3e6d12fbf23ca2d`  
		Last Modified: Mon, 08 Mar 2021 21:55:16 GMT  
		Size: 4.0 MB (3965916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:215df7eb945b46dbb7b1f65b27f357cc7537fc07c4ea4bc369b7fd007ac4f127`  
		Last Modified: Mon, 08 Mar 2021 21:55:14 GMT  
		Size: 448.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad1dec6ebfef0d19c89676d2166931e6715f0caadaedc36b52d9c5eb7b202fdb`  
		Last Modified: Mon, 08 Mar 2021 21:55:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.8.28-alpine` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:ed40dc95dd16c2e94baf8addf3da66d7bc2d3780350e79282958df54ea5170c8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6457955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c618c56e8b4d85c1c4075d981fc50160093cba7e50dfec581cf4aaf815df9690`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 20:49:32 GMT
ADD file:c04fbd3b039001c592cfa14f8388f8934ed4223ccf274dbb926e75039e172af4 in / 
# Wed, 17 Feb 2021 20:49:33 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 21:08:27 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 17 Feb 2021 21:11:29 GMT
ENV HAPROXY_VERSION=1.8.28
# Wed, 17 Feb 2021 21:11:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.8/src/haproxy-1.8.28.tar.gz
# Wed, 17 Feb 2021 21:11:30 GMT
ENV HAPROXY_SHA256=fecf031486014d5838499f69cba0348abffa076e55f6fadf86a8da93cbf94e89
# Wed, 17 Feb 2021 21:11:54 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 17 Feb 2021 21:11:55 GMT
STOPSIGNAL SIGUSR1
# Wed, 17 Feb 2021 21:11:56 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 17 Feb 2021 21:11:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 17 Feb 2021 21:11:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Feb 2021 21:12:00 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:1353527ebe111f9bb1e271264a3c182e909e4b36463f80d7dbde1be0713eb892`  
		Last Modified: Wed, 17 Feb 2021 20:50:06 GMT  
		Size: 2.6 MB (2622039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d174378d3ee2c0c6e6a85b5228f929557826d80bcd23b2434093942f499361a7`  
		Last Modified: Wed, 17 Feb 2021 21:12:31 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c878e900cddd3355fd3277e31c18029a94b54f4a29088abb076ee90bd348bc1`  
		Last Modified: Wed, 17 Feb 2021 21:13:21 GMT  
		Size: 3.8 MB (3834159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25bc05f9009c454b2533421596d9882c0b6123a30288bd5adb922c24657db10b`  
		Last Modified: Wed, 17 Feb 2021 21:13:20 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43db1713027b035e027b90cbe11b81656864504dc996baa8ff19de4081ca9be1`  
		Last Modified: Wed, 17 Feb 2021 21:13:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.8.28-alpine` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:4dee252b50597a58c5278d228d39bd0683f20249a022d66d23846f12b70f039c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6199713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fd0615a04098f6a2f05c5bf78593eb325aed56352537274e641e81956fba3a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 20:57:36 GMT
ADD file:efdd39e5243eaf378f12ad5a85d2222b44930850a90263e5f17e8a6b5e9bc9b8 in / 
# Wed, 17 Feb 2021 20:57:37 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 21:49:42 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 17 Feb 2021 21:53:38 GMT
ENV HAPROXY_VERSION=1.8.28
# Wed, 17 Feb 2021 21:53:39 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.8/src/haproxy-1.8.28.tar.gz
# Wed, 17 Feb 2021 21:53:40 GMT
ENV HAPROXY_SHA256=fecf031486014d5838499f69cba0348abffa076e55f6fadf86a8da93cbf94e89
# Wed, 17 Feb 2021 21:54:00 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 17 Feb 2021 21:54:02 GMT
STOPSIGNAL SIGUSR1
# Wed, 17 Feb 2021 21:54:03 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 17 Feb 2021 21:54:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 17 Feb 2021 21:54:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Feb 2021 21:54:07 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f55b840e27d3dbe27e44497103a4397f043749f933eb0433d29e2f104b3435ef`  
		Last Modified: Wed, 17 Feb 2021 20:58:14 GMT  
		Size: 2.4 MB (2423892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86398e5ccaeed703d9464d57f2d97546fad0481312144292414eb1cf857b617f`  
		Last Modified: Wed, 17 Feb 2021 21:55:00 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e167953148798ef619c46429dc64b4b9a07a620b6d03a068a18401cc2895bc`  
		Last Modified: Wed, 17 Feb 2021 21:55:57 GMT  
		Size: 3.8 MB (3774064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7e0c6e6595562be33375d026b38d895cc562a3fc0ead0d548d6ae4f9a46ad9`  
		Last Modified: Wed, 17 Feb 2021 21:55:55 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27ead44862777fe42723b3f193d4a90a18362c46801a86f1f1e7d3a301673c2`  
		Last Modified: Wed, 17 Feb 2021 21:55:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.8.28-alpine` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:56d777ed142f79d7425f6ea43ac513d885a808762a0dcc0d13537673bb908f69
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6637610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47e568791114e5e8c4af638836dd48d94792c31e134b15065ccbea51b785bfc5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 20:39:29 GMT
ADD file:3bf1497bd250cf7c73c12231dc4ebe3a3a67f2cd99e35bce47ef6674683aeb1d in / 
# Wed, 17 Feb 2021 20:39:30 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 21:36:08 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 17 Feb 2021 21:39:50 GMT
ENV HAPROXY_VERSION=1.8.28
# Wed, 17 Feb 2021 21:39:51 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.8/src/haproxy-1.8.28.tar.gz
# Wed, 17 Feb 2021 21:39:51 GMT
ENV HAPROXY_SHA256=fecf031486014d5838499f69cba0348abffa076e55f6fadf86a8da93cbf94e89
# Wed, 17 Feb 2021 21:40:13 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 17 Feb 2021 21:40:14 GMT
STOPSIGNAL SIGUSR1
# Wed, 17 Feb 2021 21:40:15 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 17 Feb 2021 21:40:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 17 Feb 2021 21:40:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Feb 2021 21:40:20 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:069a56d6d07f6b186fbb82e4486616b9be9a37ce32a63013af6cddcb65898182`  
		Last Modified: Wed, 17 Feb 2021 20:40:04 GMT  
		Size: 2.7 MB (2711572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6644620fa9074da825714fc7794756e2b0e36f3e83ffc2bc01bbc9df0de9e373`  
		Last Modified: Wed, 17 Feb 2021 21:41:18 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab6890d1129123eb4faae211aed2720d177540a03e8f4ba6985d6350040e1d6`  
		Last Modified: Wed, 17 Feb 2021 21:42:08 GMT  
		Size: 3.9 MB (3924280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a244cf2e7892c988a9f60ae624bdbb547f17add8036b3ec910276672999292c`  
		Last Modified: Wed, 17 Feb 2021 21:42:07 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:837db93d8cb5829a08d3ad2711001de5bd775017a6a880196269e33de7b3e49f`  
		Last Modified: Wed, 17 Feb 2021 21:42:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.8.28-alpine` - linux; 386

```console
$ docker pull haproxy@sha256:b7d37f121a5c762df8b71640127ed0b034735abe0519ee7e5140a7438a3eb2a6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6698596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:845213d4e40537862c1f096b6b441d3cf1ed0a83b37d41282a429ec7b42f6318`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 21:38:34 GMT
ADD file:eaee53da3c87749799de55809e4a5b526c56855332b961a85b1184c660f1d65b in / 
# Wed, 17 Feb 2021 21:38:35 GMT
CMD ["/bin/sh"]
# Mon, 08 Mar 2021 22:03:53 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 22:14:39 GMT
ENV HAPROXY_VERSION=1.8.28
# Mon, 08 Mar 2021 22:14:39 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.8/src/haproxy-1.8.28.tar.gz
# Mon, 08 Mar 2021 22:14:39 GMT
ENV HAPROXY_SHA256=fecf031486014d5838499f69cba0348abffa076e55f6fadf86a8da93cbf94e89
# Mon, 08 Mar 2021 22:15:19 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Mon, 08 Mar 2021 22:15:19 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 22:15:19 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 22:15:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 08 Mar 2021 22:15:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 22:15:21 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:86205afa28f6bc624469015a543d16608258d2828411a92c662f4fdc6d276e18`  
		Last Modified: Wed, 17 Feb 2021 21:39:07 GMT  
		Size: 2.8 MB (2818177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080e85d941540171ac6a020af17b393f2a40b03d40b9677d708d31ffb6e31b71`  
		Last Modified: Mon, 08 Mar 2021 22:18:02 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7740653a76e10f6d00921b60b80bea2139ef05d8baf1d94006e78a32c962fc4`  
		Last Modified: Mon, 08 Mar 2021 22:20:30 GMT  
		Size: 3.9 MB (3878667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8becf00f4c03eaed13210fa0f1dd85d78e6e4556e5bcc796782f71aa782cc980`  
		Last Modified: Mon, 08 Mar 2021 22:20:29 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0674c045e260d98de7c73f0fbfedaa2598020a607dc3c3298fa999aeea8b33`  
		Last Modified: Mon, 08 Mar 2021 22:20:29 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.8.28-alpine` - linux; ppc64le

```console
$ docker pull haproxy@sha256:2622f6be543aa8acc2b8587a21d574d2bd852d9174201cb12a83262337f071bc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6944923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17f4336f18316091bbd6cccf4f4b63b872c70a0c56c19a83e08e99656f98ccf8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 21:17:29 GMT
ADD file:28f4377c61c0f8eb43a6b36e6a24ef5893f51d405d25b62e364988223537ae0b in / 
# Wed, 17 Feb 2021 21:17:37 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 22:10:46 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 17 Feb 2021 22:20:35 GMT
ENV HAPROXY_VERSION=1.8.28
# Wed, 17 Feb 2021 22:20:47 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.8/src/haproxy-1.8.28.tar.gz
# Wed, 17 Feb 2021 22:20:56 GMT
ENV HAPROXY_SHA256=fecf031486014d5838499f69cba0348abffa076e55f6fadf86a8da93cbf94e89
# Wed, 17 Feb 2021 22:21:30 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 17 Feb 2021 22:21:40 GMT
STOPSIGNAL SIGUSR1
# Wed, 17 Feb 2021 22:21:42 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 17 Feb 2021 22:21:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 17 Feb 2021 22:21:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Feb 2021 22:22:05 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:cb672e0375a8f9bb3d33049ceb372ffa49b959bfc84fe6f72bfb97b682a608c8`  
		Last Modified: Wed, 17 Feb 2021 21:18:10 GMT  
		Size: 2.8 MB (2813081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f391a7d74b9bf5c2089e7957996d00d99ddc33d8295873bf28746716bb728a`  
		Last Modified: Wed, 17 Feb 2021 22:23:02 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e9eed9cc81261230210db20ef1e84eb543ed8e4a21ee1d34ec6cbba51862d2d`  
		Last Modified: Wed, 17 Feb 2021 22:24:14 GMT  
		Size: 4.1 MB (4130080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a23b6dd8d1f14fd7b3e645ffb0c4fd7be763e5c08af8c65bfa0c8de92226db9`  
		Last Modified: Wed, 17 Feb 2021 22:24:13 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df387d74c2f18ce66b5d053b4f67acd3d71aa3445f14a22b4a28a8afa7c574c7`  
		Last Modified: Wed, 17 Feb 2021 22:24:13 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.8.28-alpine` - linux; s390x

```console
$ docker pull haproxy@sha256:dbb685f905fc41df8570b6a47050949d47ae830fa176c25740799c256a5b7f7b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6463630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44c12c255f2dccf7bfb430e0d7c510d430c3d5614922e082e58aaaac8974d935`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 20:41:27 GMT
ADD file:630c66f8d774d75b51e32aff812b438d377ebd3389c4aa6c324fdf8c03b6fa13 in / 
# Wed, 17 Feb 2021 20:41:27 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 21:33:33 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 17 Feb 2021 21:42:01 GMT
ENV HAPROXY_VERSION=1.8.28
# Wed, 17 Feb 2021 21:42:02 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.8/src/haproxy-1.8.28.tar.gz
# Wed, 17 Feb 2021 21:42:02 GMT
ENV HAPROXY_SHA256=fecf031486014d5838499f69cba0348abffa076e55f6fadf86a8da93cbf94e89
# Wed, 17 Feb 2021 21:42:58 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 17 Feb 2021 21:42:59 GMT
STOPSIGNAL SIGUSR1
# Wed, 17 Feb 2021 21:42:59 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 17 Feb 2021 21:43:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 17 Feb 2021 21:43:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Feb 2021 21:43:03 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:ff5e8cb87555e9fa38a441f5cf0414e91353e2cd21cdb48d48b7de5bb39ce674`  
		Last Modified: Wed, 17 Feb 2021 20:41:58 GMT  
		Size: 2.6 MB (2602381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de25a3a0de168e6603cb978691ef3e7f11d7c9108d0ade38d3185d5d9dbdc094`  
		Last Modified: Wed, 17 Feb 2021 21:43:59 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c09c401ce37de2718a28f69f8f6889e3de106eb9938b7509c120aec0a807669`  
		Last Modified: Wed, 17 Feb 2021 21:44:47 GMT  
		Size: 3.9 MB (3859494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca3c93c3719a73d7ec87847ba4e9ac8bf93f61c2443746f84ed0965bba8b6776`  
		Last Modified: Wed, 17 Feb 2021 21:44:46 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50ade78a9f6bdbfebd51e58d596b9601716a8e3a399cce1676a64aec54f38246`  
		Last Modified: Wed, 17 Feb 2021 21:44:47 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haproxy:1.8-alpine`

```console
$ docker pull haproxy@sha256:145db50918a363b727c439ecc4bb71185556e45a7806a920b8bb89a92104e5c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `haproxy:1.8-alpine` - linux; amd64

```console
$ docker pull haproxy@sha256:4e73aa036e0743d00ae74c680d725d740677fff1cafc74276789ce7e5cfdb6b9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6779328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d817987db6b8c3ca596b41050d0d0cb3aa95d20ed221f6a4b6827f11a746d05`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 21:19:54 GMT
ADD file:80bf8bd014071345b1c0364eeb0a5e48f3fb0d87f9c31cb990e57caa652b59b8 in / 
# Wed, 17 Feb 2021 21:19:54 GMT
CMD ["/bin/sh"]
# Mon, 08 Mar 2021 21:38:26 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 21:50:10 GMT
ENV HAPROXY_VERSION=1.8.28
# Mon, 08 Mar 2021 21:50:10 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.8/src/haproxy-1.8.28.tar.gz
# Mon, 08 Mar 2021 21:50:10 GMT
ENV HAPROXY_SHA256=fecf031486014d5838499f69cba0348abffa076e55f6fadf86a8da93cbf94e89
# Mon, 08 Mar 2021 21:50:47 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Mon, 08 Mar 2021 21:50:47 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 21:50:47 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 21:50:48 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 08 Mar 2021 21:50:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 21:50:49 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:ba3557a56b150f9b813f9d02274d62914fd8fce120dd374d9ee17b87cf1d277d`  
		Last Modified: Wed, 17 Feb 2021 21:20:25 GMT  
		Size: 2.8 MB (2811657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9216237f12c4d44ab183590086cf2a09004b5609c4b50871d88658faa495245`  
		Last Modified: Mon, 08 Mar 2021 21:52:45 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c572dcfde483c47a4b14c7a2ed93c00a6986bec0f20a81ec3e6d12fbf23ca2d`  
		Last Modified: Mon, 08 Mar 2021 21:55:16 GMT  
		Size: 4.0 MB (3965916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:215df7eb945b46dbb7b1f65b27f357cc7537fc07c4ea4bc369b7fd007ac4f127`  
		Last Modified: Mon, 08 Mar 2021 21:55:14 GMT  
		Size: 448.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad1dec6ebfef0d19c89676d2166931e6715f0caadaedc36b52d9c5eb7b202fdb`  
		Last Modified: Mon, 08 Mar 2021 21:55:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.8-alpine` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:ed40dc95dd16c2e94baf8addf3da66d7bc2d3780350e79282958df54ea5170c8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6457955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c618c56e8b4d85c1c4075d981fc50160093cba7e50dfec581cf4aaf815df9690`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 20:49:32 GMT
ADD file:c04fbd3b039001c592cfa14f8388f8934ed4223ccf274dbb926e75039e172af4 in / 
# Wed, 17 Feb 2021 20:49:33 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 21:08:27 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 17 Feb 2021 21:11:29 GMT
ENV HAPROXY_VERSION=1.8.28
# Wed, 17 Feb 2021 21:11:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.8/src/haproxy-1.8.28.tar.gz
# Wed, 17 Feb 2021 21:11:30 GMT
ENV HAPROXY_SHA256=fecf031486014d5838499f69cba0348abffa076e55f6fadf86a8da93cbf94e89
# Wed, 17 Feb 2021 21:11:54 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 17 Feb 2021 21:11:55 GMT
STOPSIGNAL SIGUSR1
# Wed, 17 Feb 2021 21:11:56 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 17 Feb 2021 21:11:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 17 Feb 2021 21:11:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Feb 2021 21:12:00 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:1353527ebe111f9bb1e271264a3c182e909e4b36463f80d7dbde1be0713eb892`  
		Last Modified: Wed, 17 Feb 2021 20:50:06 GMT  
		Size: 2.6 MB (2622039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d174378d3ee2c0c6e6a85b5228f929557826d80bcd23b2434093942f499361a7`  
		Last Modified: Wed, 17 Feb 2021 21:12:31 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c878e900cddd3355fd3277e31c18029a94b54f4a29088abb076ee90bd348bc1`  
		Last Modified: Wed, 17 Feb 2021 21:13:21 GMT  
		Size: 3.8 MB (3834159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25bc05f9009c454b2533421596d9882c0b6123a30288bd5adb922c24657db10b`  
		Last Modified: Wed, 17 Feb 2021 21:13:20 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43db1713027b035e027b90cbe11b81656864504dc996baa8ff19de4081ca9be1`  
		Last Modified: Wed, 17 Feb 2021 21:13:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.8-alpine` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:4dee252b50597a58c5278d228d39bd0683f20249a022d66d23846f12b70f039c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6199713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fd0615a04098f6a2f05c5bf78593eb325aed56352537274e641e81956fba3a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 20:57:36 GMT
ADD file:efdd39e5243eaf378f12ad5a85d2222b44930850a90263e5f17e8a6b5e9bc9b8 in / 
# Wed, 17 Feb 2021 20:57:37 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 21:49:42 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 17 Feb 2021 21:53:38 GMT
ENV HAPROXY_VERSION=1.8.28
# Wed, 17 Feb 2021 21:53:39 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.8/src/haproxy-1.8.28.tar.gz
# Wed, 17 Feb 2021 21:53:40 GMT
ENV HAPROXY_SHA256=fecf031486014d5838499f69cba0348abffa076e55f6fadf86a8da93cbf94e89
# Wed, 17 Feb 2021 21:54:00 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 17 Feb 2021 21:54:02 GMT
STOPSIGNAL SIGUSR1
# Wed, 17 Feb 2021 21:54:03 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 17 Feb 2021 21:54:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 17 Feb 2021 21:54:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Feb 2021 21:54:07 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f55b840e27d3dbe27e44497103a4397f043749f933eb0433d29e2f104b3435ef`  
		Last Modified: Wed, 17 Feb 2021 20:58:14 GMT  
		Size: 2.4 MB (2423892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86398e5ccaeed703d9464d57f2d97546fad0481312144292414eb1cf857b617f`  
		Last Modified: Wed, 17 Feb 2021 21:55:00 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e167953148798ef619c46429dc64b4b9a07a620b6d03a068a18401cc2895bc`  
		Last Modified: Wed, 17 Feb 2021 21:55:57 GMT  
		Size: 3.8 MB (3774064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7e0c6e6595562be33375d026b38d895cc562a3fc0ead0d548d6ae4f9a46ad9`  
		Last Modified: Wed, 17 Feb 2021 21:55:55 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27ead44862777fe42723b3f193d4a90a18362c46801a86f1f1e7d3a301673c2`  
		Last Modified: Wed, 17 Feb 2021 21:55:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.8-alpine` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:56d777ed142f79d7425f6ea43ac513d885a808762a0dcc0d13537673bb908f69
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6637610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47e568791114e5e8c4af638836dd48d94792c31e134b15065ccbea51b785bfc5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 20:39:29 GMT
ADD file:3bf1497bd250cf7c73c12231dc4ebe3a3a67f2cd99e35bce47ef6674683aeb1d in / 
# Wed, 17 Feb 2021 20:39:30 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 21:36:08 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 17 Feb 2021 21:39:50 GMT
ENV HAPROXY_VERSION=1.8.28
# Wed, 17 Feb 2021 21:39:51 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.8/src/haproxy-1.8.28.tar.gz
# Wed, 17 Feb 2021 21:39:51 GMT
ENV HAPROXY_SHA256=fecf031486014d5838499f69cba0348abffa076e55f6fadf86a8da93cbf94e89
# Wed, 17 Feb 2021 21:40:13 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 17 Feb 2021 21:40:14 GMT
STOPSIGNAL SIGUSR1
# Wed, 17 Feb 2021 21:40:15 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 17 Feb 2021 21:40:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 17 Feb 2021 21:40:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Feb 2021 21:40:20 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:069a56d6d07f6b186fbb82e4486616b9be9a37ce32a63013af6cddcb65898182`  
		Last Modified: Wed, 17 Feb 2021 20:40:04 GMT  
		Size: 2.7 MB (2711572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6644620fa9074da825714fc7794756e2b0e36f3e83ffc2bc01bbc9df0de9e373`  
		Last Modified: Wed, 17 Feb 2021 21:41:18 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab6890d1129123eb4faae211aed2720d177540a03e8f4ba6985d6350040e1d6`  
		Last Modified: Wed, 17 Feb 2021 21:42:08 GMT  
		Size: 3.9 MB (3924280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a244cf2e7892c988a9f60ae624bdbb547f17add8036b3ec910276672999292c`  
		Last Modified: Wed, 17 Feb 2021 21:42:07 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:837db93d8cb5829a08d3ad2711001de5bd775017a6a880196269e33de7b3e49f`  
		Last Modified: Wed, 17 Feb 2021 21:42:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.8-alpine` - linux; 386

```console
$ docker pull haproxy@sha256:b7d37f121a5c762df8b71640127ed0b034735abe0519ee7e5140a7438a3eb2a6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6698596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:845213d4e40537862c1f096b6b441d3cf1ed0a83b37d41282a429ec7b42f6318`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 21:38:34 GMT
ADD file:eaee53da3c87749799de55809e4a5b526c56855332b961a85b1184c660f1d65b in / 
# Wed, 17 Feb 2021 21:38:35 GMT
CMD ["/bin/sh"]
# Mon, 08 Mar 2021 22:03:53 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 22:14:39 GMT
ENV HAPROXY_VERSION=1.8.28
# Mon, 08 Mar 2021 22:14:39 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.8/src/haproxy-1.8.28.tar.gz
# Mon, 08 Mar 2021 22:14:39 GMT
ENV HAPROXY_SHA256=fecf031486014d5838499f69cba0348abffa076e55f6fadf86a8da93cbf94e89
# Mon, 08 Mar 2021 22:15:19 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Mon, 08 Mar 2021 22:15:19 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 22:15:19 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 22:15:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 08 Mar 2021 22:15:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 22:15:21 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:86205afa28f6bc624469015a543d16608258d2828411a92c662f4fdc6d276e18`  
		Last Modified: Wed, 17 Feb 2021 21:39:07 GMT  
		Size: 2.8 MB (2818177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080e85d941540171ac6a020af17b393f2a40b03d40b9677d708d31ffb6e31b71`  
		Last Modified: Mon, 08 Mar 2021 22:18:02 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7740653a76e10f6d00921b60b80bea2139ef05d8baf1d94006e78a32c962fc4`  
		Last Modified: Mon, 08 Mar 2021 22:20:30 GMT  
		Size: 3.9 MB (3878667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8becf00f4c03eaed13210fa0f1dd85d78e6e4556e5bcc796782f71aa782cc980`  
		Last Modified: Mon, 08 Mar 2021 22:20:29 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0674c045e260d98de7c73f0fbfedaa2598020a607dc3c3298fa999aeea8b33`  
		Last Modified: Mon, 08 Mar 2021 22:20:29 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.8-alpine` - linux; ppc64le

```console
$ docker pull haproxy@sha256:2622f6be543aa8acc2b8587a21d574d2bd852d9174201cb12a83262337f071bc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6944923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17f4336f18316091bbd6cccf4f4b63b872c70a0c56c19a83e08e99656f98ccf8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 21:17:29 GMT
ADD file:28f4377c61c0f8eb43a6b36e6a24ef5893f51d405d25b62e364988223537ae0b in / 
# Wed, 17 Feb 2021 21:17:37 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 22:10:46 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 17 Feb 2021 22:20:35 GMT
ENV HAPROXY_VERSION=1.8.28
# Wed, 17 Feb 2021 22:20:47 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.8/src/haproxy-1.8.28.tar.gz
# Wed, 17 Feb 2021 22:20:56 GMT
ENV HAPROXY_SHA256=fecf031486014d5838499f69cba0348abffa076e55f6fadf86a8da93cbf94e89
# Wed, 17 Feb 2021 22:21:30 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 17 Feb 2021 22:21:40 GMT
STOPSIGNAL SIGUSR1
# Wed, 17 Feb 2021 22:21:42 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 17 Feb 2021 22:21:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 17 Feb 2021 22:21:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Feb 2021 22:22:05 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:cb672e0375a8f9bb3d33049ceb372ffa49b959bfc84fe6f72bfb97b682a608c8`  
		Last Modified: Wed, 17 Feb 2021 21:18:10 GMT  
		Size: 2.8 MB (2813081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f391a7d74b9bf5c2089e7957996d00d99ddc33d8295873bf28746716bb728a`  
		Last Modified: Wed, 17 Feb 2021 22:23:02 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e9eed9cc81261230210db20ef1e84eb543ed8e4a21ee1d34ec6cbba51862d2d`  
		Last Modified: Wed, 17 Feb 2021 22:24:14 GMT  
		Size: 4.1 MB (4130080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a23b6dd8d1f14fd7b3e645ffb0c4fd7be763e5c08af8c65bfa0c8de92226db9`  
		Last Modified: Wed, 17 Feb 2021 22:24:13 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df387d74c2f18ce66b5d053b4f67acd3d71aa3445f14a22b4a28a8afa7c574c7`  
		Last Modified: Wed, 17 Feb 2021 22:24:13 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.8-alpine` - linux; s390x

```console
$ docker pull haproxy@sha256:dbb685f905fc41df8570b6a47050949d47ae830fa176c25740799c256a5b7f7b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6463630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44c12c255f2dccf7bfb430e0d7c510d430c3d5614922e082e58aaaac8974d935`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 20:41:27 GMT
ADD file:630c66f8d774d75b51e32aff812b438d377ebd3389c4aa6c324fdf8c03b6fa13 in / 
# Wed, 17 Feb 2021 20:41:27 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 21:33:33 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 17 Feb 2021 21:42:01 GMT
ENV HAPROXY_VERSION=1.8.28
# Wed, 17 Feb 2021 21:42:02 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.8/src/haproxy-1.8.28.tar.gz
# Wed, 17 Feb 2021 21:42:02 GMT
ENV HAPROXY_SHA256=fecf031486014d5838499f69cba0348abffa076e55f6fadf86a8da93cbf94e89
# Wed, 17 Feb 2021 21:42:58 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 17 Feb 2021 21:42:59 GMT
STOPSIGNAL SIGUSR1
# Wed, 17 Feb 2021 21:42:59 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 17 Feb 2021 21:43:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 17 Feb 2021 21:43:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Feb 2021 21:43:03 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:ff5e8cb87555e9fa38a441f5cf0414e91353e2cd21cdb48d48b7de5bb39ce674`  
		Last Modified: Wed, 17 Feb 2021 20:41:58 GMT  
		Size: 2.6 MB (2602381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de25a3a0de168e6603cb978691ef3e7f11d7c9108d0ade38d3185d5d9dbdc094`  
		Last Modified: Wed, 17 Feb 2021 21:43:59 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c09c401ce37de2718a28f69f8f6889e3de106eb9938b7509c120aec0a807669`  
		Last Modified: Wed, 17 Feb 2021 21:44:47 GMT  
		Size: 3.9 MB (3859494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca3c93c3719a73d7ec87847ba4e9ac8bf93f61c2443746f84ed0965bba8b6776`  
		Last Modified: Wed, 17 Feb 2021 21:44:46 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50ade78a9f6bdbfebd51e58d596b9601716a8e3a399cce1676a64aec54f38246`  
		Last Modified: Wed, 17 Feb 2021 21:44:47 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haproxy:2.0`

```console
$ docker pull haproxy@sha256:09d3717d648e2ef6c24cc107adc6c9c444cfd34aa99996019c8aa09ae2b08169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `haproxy:2.0` - linux; amd64

```console
$ docker pull haproxy@sha256:b3c1f0fb0b5abb961be8ab75052b1545d5e707184929ead7af28ea5be7fad6cf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 MB (35773881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c87449cc1c50a07a2b44d747bec999b351e232d8c86875b3f86c2cc29ac0db7f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Mon, 08 Mar 2021 21:37:25 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 21:47:07 GMT
ENV HAPROXY_VERSION=2.0.20
# Mon, 08 Mar 2021 21:47:07 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.0/src/haproxy-2.0.20.tar.gz
# Mon, 08 Mar 2021 21:47:07 GMT
ENV HAPROXY_SHA256=65153c989e7412f6815d3b047184bb07eeb73ccb10f5c05e757347ea6c317ce1
# Mon, 08 Mar 2021 21:48:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 08 Mar 2021 21:48:08 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 21:48:08 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 21:48:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 08 Mar 2021 21:48:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 21:48:09 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7bca45a971fe608786870ce75c9976f8e5a958f55e1287a6120048b897c63b6`  
		Last Modified: Mon, 08 Mar 2021 21:52:33 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b6033caa7edd4fc54742b27283092fc6badfc2e1957d6a8e79fd366d3c687d`  
		Last Modified: Mon, 08 Mar 2021 21:54:36 GMT  
		Size: 8.7 MB (8676791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f32b79eaf3f315706108c9ac4e6445d0c48acf25cc9f38297c2f3d5f5533964`  
		Last Modified: Mon, 08 Mar 2021 21:54:35 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ae323fefb49a9a4785ae0657b69ab73d1ef97c05e446957211b69ad20e01ee`  
		Last Modified: Mon, 08 Mar 2021 21:54:35 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.0` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:2f6de09a748452838a50d06c057f543a2b95997663d364aec92f8e53479d008c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (33000666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c82b301e3a01a0768acbc7ee5cb4df59bd37546cfee5858a48d53b0de509d303`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:50:10 GMT
ADD file:fbd00ef7871dc27d7ed5fa8c238cdc80652bd87b8033be7de9e54a799bbf10a4 in / 
# Tue, 09 Feb 2021 02:50:11 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:45:24 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 09 Feb 2021 03:51:00 GMT
ENV HAPROXY_VERSION=2.0.20
# Tue, 09 Feb 2021 03:51:01 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.0/src/haproxy-2.0.20.tar.gz
# Tue, 09 Feb 2021 03:51:02 GMT
ENV HAPROXY_SHA256=65153c989e7412f6815d3b047184bb07eeb73ccb10f5c05e757347ea6c317ce1
# Tue, 09 Feb 2021 03:51:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 09 Feb 2021 03:51:58 GMT
STOPSIGNAL SIGUSR1
# Tue, 09 Feb 2021 03:51:59 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 09 Feb 2021 03:52:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 09 Feb 2021 03:52:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Feb 2021 03:52:04 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:8e683fcc73f4da7d69ce1d5f4e1d77510aa459490068f38db2d8663698b391a0`  
		Last Modified: Tue, 09 Feb 2021 02:59:07 GMT  
		Size: 24.8 MB (24839297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def565d52deae74587a55f60d168bd531ebe8095c594027b7057a8fc1be0e8af`  
		Last Modified: Tue, 09 Feb 2021 03:54:54 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad2845922289ec9e3a446887b44a7b3fa0ab7f5f08b88def28061507458391d`  
		Last Modified: Tue, 09 Feb 2021 03:55:41 GMT  
		Size: 8.2 MB (8159425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7f2de6869d9906d1d4fa36ef17436726eee6720bb09633a2b3150e38dd212d`  
		Last Modified: Tue, 09 Feb 2021 03:55:39 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2beaf27a5879998c4fea7ce79503aef304efd5b9939bb7ef6ca2a983cbfccc9f`  
		Last Modified: Tue, 09 Feb 2021 03:55:39 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.0` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:5a439f622d1124768a437aece99afb549591f4b0a6bec5b90efa9e2cc5ee928e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 MB (30809625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71e483ded4c4553966b7f30090972108b1d0da3894a4fc3db9ae5d9aa09cbca3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 03:00:57 GMT
ADD file:e675d50366bde57173a75f9a29367d765e7da2b7254c5254b64e777cf6870502 in / 
# Tue, 09 Feb 2021 03:01:00 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:49:38 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 09 Feb 2021 03:54:36 GMT
ENV HAPROXY_VERSION=2.0.20
# Tue, 09 Feb 2021 03:54:38 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.0/src/haproxy-2.0.20.tar.gz
# Tue, 09 Feb 2021 03:54:39 GMT
ENV HAPROXY_SHA256=65153c989e7412f6815d3b047184bb07eeb73ccb10f5c05e757347ea6c317ce1
# Tue, 09 Feb 2021 03:55:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 09 Feb 2021 03:55:21 GMT
STOPSIGNAL SIGUSR1
# Tue, 09 Feb 2021 03:55:22 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 09 Feb 2021 03:55:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 09 Feb 2021 03:55:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Feb 2021 03:55:25 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:db574d82360c3b60abadbef4f3daf8dee01f24741fc6ab3692aa543558d8b624`  
		Last Modified: Tue, 09 Feb 2021 03:09:46 GMT  
		Size: 22.7 MB (22703384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9978ebb1881387f11e025fb46dce2b3c715f705f6d240737574f8848c27fa0d7`  
		Last Modified: Tue, 09 Feb 2021 03:58:16 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6830a85677814ff05fc8201534241f586e88d99a23868731e3e9915ecb8106bc`  
		Last Modified: Tue, 09 Feb 2021 03:59:06 GMT  
		Size: 8.1 MB (8104297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f4a209f640956b139d9d08b90fe93dc4f227629e08b0acaff40233ccc7745e1`  
		Last Modified: Tue, 09 Feb 2021 03:59:03 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed6b483e9518444af3974aa6d36dff50abf8f8914279df261e22c7184bdf86fc`  
		Last Modified: Tue, 09 Feb 2021 03:59:03 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.0` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:a9dc2667fc86017d9206d448f333587408509f9678f6c5a6d9e7066212b8e55d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.4 MB (34364997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cb3e265bcccd7b51eada3ab1dd3c0faedde5bd3957a722731659cacefe83b81`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:41:10 GMT
ADD file:d906dedaf14d8e3874b46787f7a1dbf268bc124c4e1dd32f13f3079e12f22238 in / 
# Tue, 09 Feb 2021 02:41:13 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:59:41 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 09 Feb 2021 04:04:52 GMT
ENV HAPROXY_VERSION=2.0.20
# Tue, 09 Feb 2021 04:04:53 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.0/src/haproxy-2.0.20.tar.gz
# Tue, 09 Feb 2021 04:04:54 GMT
ENV HAPROXY_SHA256=65153c989e7412f6815d3b047184bb07eeb73ccb10f5c05e757347ea6c317ce1
# Tue, 09 Feb 2021 04:05:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 09 Feb 2021 04:05:36 GMT
STOPSIGNAL SIGUSR1
# Tue, 09 Feb 2021 04:05:37 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 09 Feb 2021 04:05:40 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 09 Feb 2021 04:05:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Feb 2021 04:05:41 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:83c5cfdaa5385ea6fc4d31e724fd4dc5d74de847a7bdd968555b8f2c558dac0e`  
		Last Modified: Tue, 09 Feb 2021 02:47:27 GMT  
		Size: 25.9 MB (25851449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b7f43dd52365bce2c2b75f29577aa39d2b5794e2561cddc0678422ffc1f7d15`  
		Last Modified: Tue, 09 Feb 2021 04:08:36 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f0a22ec3704203d2819a1814270189a465a90203c722bdad925f59f9ca0339`  
		Last Modified: Tue, 09 Feb 2021 04:09:24 GMT  
		Size: 8.5 MB (8511601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d64ce9228abffd55dd1c82b8a4763e682bf0848d0f51d0708c50ad38b961776`  
		Last Modified: Tue, 09 Feb 2021 04:09:22 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:070414b6da34ece8df556eb4af8c895e998fc31445662f44663d11a96516bbc0`  
		Last Modified: Tue, 09 Feb 2021 04:09:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.0` - linux; 386

```console
$ docker pull haproxy@sha256:513050c26322b5ca96f54c557cc59794a6c626bd56493deb8bb4abb6450313c9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36223205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83c470e1de3484cd49576d80d34988128d6dd950837ce45988be034beb92eea9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:39:47 GMT
ADD file:61c31b1037672781ed0ecbc080ee3d49c83af49f5578b011544513fa9625698d in / 
# Tue, 09 Feb 2021 02:39:47 GMT
CMD ["bash"]
# Mon, 08 Mar 2021 22:02:40 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 22:11:50 GMT
ENV HAPROXY_VERSION=2.0.20
# Mon, 08 Mar 2021 22:11:50 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.0/src/haproxy-2.0.20.tar.gz
# Mon, 08 Mar 2021 22:11:50 GMT
ENV HAPROXY_SHA256=65153c989e7412f6815d3b047184bb07eeb73ccb10f5c05e757347ea6c317ce1
# Mon, 08 Mar 2021 22:12:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 08 Mar 2021 22:12:36 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 22:12:36 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 22:12:37 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 08 Mar 2021 22:12:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 22:12:38 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:27cbb00346a16ea900c1049a2e5b47942c586c377179e098382c8ca1c8e87966`  
		Last Modified: Tue, 09 Feb 2021 02:45:51 GMT  
		Size: 27.8 MB (27752731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b6129a97a33727ea8a598d1e797bccce491920bf29d769880cf2fc6d3e0436`  
		Last Modified: Mon, 08 Mar 2021 22:17:48 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5643251b7f4fc8419293a6fb8a01d41c9ec9077fa7760ca0f0bc4afd8b591433`  
		Last Modified: Mon, 08 Mar 2021 22:19:48 GMT  
		Size: 8.5 MB (8468532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cce7451d0b07bd6018bf0e51b34e0b4fc0d446bebe856f7a138e9f594a8437f2`  
		Last Modified: Mon, 08 Mar 2021 22:19:46 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5788e78f350c1aa999691491517c5f4d4291ca0a4126879673c68745c734bc3`  
		Last Modified: Mon, 08 Mar 2021 22:19:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.0` - linux; mips64le

```console
$ docker pull haproxy@sha256:68967fb5eb64c113a23e60d4023efcf834d1a431a16bc8759b75fb6d5384943d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33901649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:840fdab6364ef6e3cf852054298ee14aec686111645ed4529c4550bf051d8cb3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 03:09:26 GMT
ADD file:0222a151f4e5033d9eae98ce2b703a63f52d049dd72ac40bdd0dc2dafe619f0a in / 
# Tue, 09 Feb 2021 03:09:27 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:41:09 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 09 Feb 2021 03:51:37 GMT
ENV HAPROXY_VERSION=2.0.20
# Tue, 09 Feb 2021 03:51:37 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.0/src/haproxy-2.0.20.tar.gz
# Tue, 09 Feb 2021 03:51:38 GMT
ENV HAPROXY_SHA256=65153c989e7412f6815d3b047184bb07eeb73ccb10f5c05e757347ea6c317ce1
# Tue, 09 Feb 2021 03:53:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 09 Feb 2021 03:53:48 GMT
STOPSIGNAL SIGUSR1
# Tue, 09 Feb 2021 03:53:48 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 09 Feb 2021 03:53:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 09 Feb 2021 03:53:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Feb 2021 03:53:51 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:dfb81134097d874e01b495d1fba82e384056d0a3a45f01a69a2e86ae82af1e96`  
		Last Modified: Tue, 09 Feb 2021 03:15:55 GMT  
		Size: 25.8 MB (25764640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a549d56662447dd8cb15faf59ca0fc2eda7a877e9aee16aadd09fd46e4214a`  
		Last Modified: Tue, 09 Feb 2021 03:57:56 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc51d0de6bedfd89e339f209975d16d2169c7a6c02fb8628dc40bd170b9bd03`  
		Last Modified: Tue, 09 Feb 2021 03:59:15 GMT  
		Size: 8.1 MB (8135060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12c521c4e325cd0f343932ca83456482e8ae958aad502d7e84363548c24a3e99`  
		Last Modified: Tue, 09 Feb 2021 03:59:10 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c74ce4bc22662d59d6ca77fd41f06272d4fda648829082877fb0f19e08b9e492`  
		Last Modified: Tue, 09 Feb 2021 03:59:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.0` - linux; ppc64le

```console
$ docker pull haproxy@sha256:793105f03702a93d9358ead4f99b472c62368555d12a12a7475f952fcf0f1abf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.5 MB (39462448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8f011494c4956f6083b852c7e80ea70b31fe04a2670b5fe7527d0f2ca5abc4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:19:19 GMT
ADD file:9a8cfdf0eab394a693b5cde0700ad47b6e8506ef0b79fabb8a07874b96e6c394 in / 
# Tue, 09 Feb 2021 02:19:34 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 05:52:23 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 09 Feb 2021 06:17:12 GMT
ENV HAPROXY_VERSION=2.0.20
# Tue, 09 Feb 2021 06:17:21 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.0/src/haproxy-2.0.20.tar.gz
# Tue, 09 Feb 2021 06:17:30 GMT
ENV HAPROXY_SHA256=65153c989e7412f6815d3b047184bb07eeb73ccb10f5c05e757347ea6c317ce1
# Tue, 09 Feb 2021 06:23:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 09 Feb 2021 06:23:16 GMT
STOPSIGNAL SIGUSR1
# Tue, 09 Feb 2021 06:23:19 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 09 Feb 2021 06:23:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 09 Feb 2021 06:23:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Feb 2021 06:23:51 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:9996b4fb6bc1c50f95ba30f8988c9c89526556fa320d3fda59d3d8359f7810d6`  
		Last Modified: Tue, 09 Feb 2021 02:27:59 GMT  
		Size: 30.5 MB (30519509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7f600bc4989eb9f12d5006a73f5958eb4fe85f86bc4008d7a899bb935b0f1c`  
		Last Modified: Tue, 09 Feb 2021 06:38:36 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bd9ae063a2baa6da6d5ba0b880f52465941c6139534bc320e4040fdef11b55b`  
		Last Modified: Tue, 09 Feb 2021 06:39:37 GMT  
		Size: 8.9 MB (8940991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0fc094fa75a8808c9afd0e650f6b69cc6618f6c92a1e20ddf5b7db08e369b02`  
		Last Modified: Tue, 09 Feb 2021 06:39:36 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:861f5efadd0b26fc12ba3a5cdd72c11fde8ec20bc5945aeca5d60d8f79b72e80`  
		Last Modified: Tue, 09 Feb 2021 06:39:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.0` - linux; s390x

```console
$ docker pull haproxy@sha256:e23d1b61e10d2cdbce29a256e16ff6b02c68a71138fe188aab0de2dddb1e6a17
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33940345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbd22506827b48cbd914589a91bd5e7a08efbdaaf65d70d303928886d26787e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:42:10 GMT
ADD file:0edb2de05df54191a141bd125f59d7e14eef0cc4576927a247b8dd7d6f255d04 in / 
# Tue, 09 Feb 2021 02:42:12 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:39:30 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 09 Feb 2021 03:42:18 GMT
ENV HAPROXY_VERSION=2.0.20
# Tue, 09 Feb 2021 03:42:19 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.0/src/haproxy-2.0.20.tar.gz
# Tue, 09 Feb 2021 03:42:19 GMT
ENV HAPROXY_SHA256=65153c989e7412f6815d3b047184bb07eeb73ccb10f5c05e757347ea6c317ce1
# Tue, 09 Feb 2021 03:42:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 09 Feb 2021 03:42:45 GMT
STOPSIGNAL SIGUSR1
# Tue, 09 Feb 2021 03:42:45 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 09 Feb 2021 03:42:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 09 Feb 2021 03:42:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Feb 2021 03:42:46 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:032413a44cf56b097e48b8221bf475ca1bec26e7a27f35fe61d699366a335b79`  
		Last Modified: Tue, 09 Feb 2021 02:45:31 GMT  
		Size: 25.7 MB (25710021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e65f701864562492efa2c0035134b62d68efdb6e7241a0a2dcc3151e6d5775b`  
		Last Modified: Tue, 09 Feb 2021 03:44:28 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4282993cf1f51ab3fe5a2c3a932cab755669406bf14cd8796d80af35511256da`  
		Last Modified: Tue, 09 Feb 2021 03:45:11 GMT  
		Size: 8.2 MB (8228381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6e4094b538182a6bff81c60e5c11e422bc715412af2841a25ff4de192762b4`  
		Last Modified: Tue, 09 Feb 2021 03:45:10 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd033a2110f271869fd3ff33da4c18b608e13160de24c48155150385ef9fe9c6`  
		Last Modified: Tue, 09 Feb 2021 03:45:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haproxy:2.0.20`

```console
$ docker pull haproxy@sha256:09d3717d648e2ef6c24cc107adc6c9c444cfd34aa99996019c8aa09ae2b08169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `haproxy:2.0.20` - linux; amd64

```console
$ docker pull haproxy@sha256:b3c1f0fb0b5abb961be8ab75052b1545d5e707184929ead7af28ea5be7fad6cf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 MB (35773881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c87449cc1c50a07a2b44d747bec999b351e232d8c86875b3f86c2cc29ac0db7f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Mon, 08 Mar 2021 21:37:25 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 21:47:07 GMT
ENV HAPROXY_VERSION=2.0.20
# Mon, 08 Mar 2021 21:47:07 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.0/src/haproxy-2.0.20.tar.gz
# Mon, 08 Mar 2021 21:47:07 GMT
ENV HAPROXY_SHA256=65153c989e7412f6815d3b047184bb07eeb73ccb10f5c05e757347ea6c317ce1
# Mon, 08 Mar 2021 21:48:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 08 Mar 2021 21:48:08 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 21:48:08 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 21:48:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 08 Mar 2021 21:48:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 21:48:09 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7bca45a971fe608786870ce75c9976f8e5a958f55e1287a6120048b897c63b6`  
		Last Modified: Mon, 08 Mar 2021 21:52:33 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b6033caa7edd4fc54742b27283092fc6badfc2e1957d6a8e79fd366d3c687d`  
		Last Modified: Mon, 08 Mar 2021 21:54:36 GMT  
		Size: 8.7 MB (8676791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f32b79eaf3f315706108c9ac4e6445d0c48acf25cc9f38297c2f3d5f5533964`  
		Last Modified: Mon, 08 Mar 2021 21:54:35 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ae323fefb49a9a4785ae0657b69ab73d1ef97c05e446957211b69ad20e01ee`  
		Last Modified: Mon, 08 Mar 2021 21:54:35 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.0.20` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:2f6de09a748452838a50d06c057f543a2b95997663d364aec92f8e53479d008c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (33000666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c82b301e3a01a0768acbc7ee5cb4df59bd37546cfee5858a48d53b0de509d303`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:50:10 GMT
ADD file:fbd00ef7871dc27d7ed5fa8c238cdc80652bd87b8033be7de9e54a799bbf10a4 in / 
# Tue, 09 Feb 2021 02:50:11 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:45:24 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 09 Feb 2021 03:51:00 GMT
ENV HAPROXY_VERSION=2.0.20
# Tue, 09 Feb 2021 03:51:01 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.0/src/haproxy-2.0.20.tar.gz
# Tue, 09 Feb 2021 03:51:02 GMT
ENV HAPROXY_SHA256=65153c989e7412f6815d3b047184bb07eeb73ccb10f5c05e757347ea6c317ce1
# Tue, 09 Feb 2021 03:51:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 09 Feb 2021 03:51:58 GMT
STOPSIGNAL SIGUSR1
# Tue, 09 Feb 2021 03:51:59 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 09 Feb 2021 03:52:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 09 Feb 2021 03:52:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Feb 2021 03:52:04 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:8e683fcc73f4da7d69ce1d5f4e1d77510aa459490068f38db2d8663698b391a0`  
		Last Modified: Tue, 09 Feb 2021 02:59:07 GMT  
		Size: 24.8 MB (24839297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def565d52deae74587a55f60d168bd531ebe8095c594027b7057a8fc1be0e8af`  
		Last Modified: Tue, 09 Feb 2021 03:54:54 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad2845922289ec9e3a446887b44a7b3fa0ab7f5f08b88def28061507458391d`  
		Last Modified: Tue, 09 Feb 2021 03:55:41 GMT  
		Size: 8.2 MB (8159425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7f2de6869d9906d1d4fa36ef17436726eee6720bb09633a2b3150e38dd212d`  
		Last Modified: Tue, 09 Feb 2021 03:55:39 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2beaf27a5879998c4fea7ce79503aef304efd5b9939bb7ef6ca2a983cbfccc9f`  
		Last Modified: Tue, 09 Feb 2021 03:55:39 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.0.20` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:5a439f622d1124768a437aece99afb549591f4b0a6bec5b90efa9e2cc5ee928e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 MB (30809625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71e483ded4c4553966b7f30090972108b1d0da3894a4fc3db9ae5d9aa09cbca3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 03:00:57 GMT
ADD file:e675d50366bde57173a75f9a29367d765e7da2b7254c5254b64e777cf6870502 in / 
# Tue, 09 Feb 2021 03:01:00 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:49:38 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 09 Feb 2021 03:54:36 GMT
ENV HAPROXY_VERSION=2.0.20
# Tue, 09 Feb 2021 03:54:38 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.0/src/haproxy-2.0.20.tar.gz
# Tue, 09 Feb 2021 03:54:39 GMT
ENV HAPROXY_SHA256=65153c989e7412f6815d3b047184bb07eeb73ccb10f5c05e757347ea6c317ce1
# Tue, 09 Feb 2021 03:55:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 09 Feb 2021 03:55:21 GMT
STOPSIGNAL SIGUSR1
# Tue, 09 Feb 2021 03:55:22 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 09 Feb 2021 03:55:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 09 Feb 2021 03:55:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Feb 2021 03:55:25 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:db574d82360c3b60abadbef4f3daf8dee01f24741fc6ab3692aa543558d8b624`  
		Last Modified: Tue, 09 Feb 2021 03:09:46 GMT  
		Size: 22.7 MB (22703384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9978ebb1881387f11e025fb46dce2b3c715f705f6d240737574f8848c27fa0d7`  
		Last Modified: Tue, 09 Feb 2021 03:58:16 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6830a85677814ff05fc8201534241f586e88d99a23868731e3e9915ecb8106bc`  
		Last Modified: Tue, 09 Feb 2021 03:59:06 GMT  
		Size: 8.1 MB (8104297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f4a209f640956b139d9d08b90fe93dc4f227629e08b0acaff40233ccc7745e1`  
		Last Modified: Tue, 09 Feb 2021 03:59:03 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed6b483e9518444af3974aa6d36dff50abf8f8914279df261e22c7184bdf86fc`  
		Last Modified: Tue, 09 Feb 2021 03:59:03 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.0.20` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:a9dc2667fc86017d9206d448f333587408509f9678f6c5a6d9e7066212b8e55d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.4 MB (34364997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cb3e265bcccd7b51eada3ab1dd3c0faedde5bd3957a722731659cacefe83b81`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:41:10 GMT
ADD file:d906dedaf14d8e3874b46787f7a1dbf268bc124c4e1dd32f13f3079e12f22238 in / 
# Tue, 09 Feb 2021 02:41:13 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:59:41 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 09 Feb 2021 04:04:52 GMT
ENV HAPROXY_VERSION=2.0.20
# Tue, 09 Feb 2021 04:04:53 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.0/src/haproxy-2.0.20.tar.gz
# Tue, 09 Feb 2021 04:04:54 GMT
ENV HAPROXY_SHA256=65153c989e7412f6815d3b047184bb07eeb73ccb10f5c05e757347ea6c317ce1
# Tue, 09 Feb 2021 04:05:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 09 Feb 2021 04:05:36 GMT
STOPSIGNAL SIGUSR1
# Tue, 09 Feb 2021 04:05:37 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 09 Feb 2021 04:05:40 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 09 Feb 2021 04:05:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Feb 2021 04:05:41 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:83c5cfdaa5385ea6fc4d31e724fd4dc5d74de847a7bdd968555b8f2c558dac0e`  
		Last Modified: Tue, 09 Feb 2021 02:47:27 GMT  
		Size: 25.9 MB (25851449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b7f43dd52365bce2c2b75f29577aa39d2b5794e2561cddc0678422ffc1f7d15`  
		Last Modified: Tue, 09 Feb 2021 04:08:36 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f0a22ec3704203d2819a1814270189a465a90203c722bdad925f59f9ca0339`  
		Last Modified: Tue, 09 Feb 2021 04:09:24 GMT  
		Size: 8.5 MB (8511601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d64ce9228abffd55dd1c82b8a4763e682bf0848d0f51d0708c50ad38b961776`  
		Last Modified: Tue, 09 Feb 2021 04:09:22 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:070414b6da34ece8df556eb4af8c895e998fc31445662f44663d11a96516bbc0`  
		Last Modified: Tue, 09 Feb 2021 04:09:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.0.20` - linux; 386

```console
$ docker pull haproxy@sha256:513050c26322b5ca96f54c557cc59794a6c626bd56493deb8bb4abb6450313c9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36223205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83c470e1de3484cd49576d80d34988128d6dd950837ce45988be034beb92eea9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:39:47 GMT
ADD file:61c31b1037672781ed0ecbc080ee3d49c83af49f5578b011544513fa9625698d in / 
# Tue, 09 Feb 2021 02:39:47 GMT
CMD ["bash"]
# Mon, 08 Mar 2021 22:02:40 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 22:11:50 GMT
ENV HAPROXY_VERSION=2.0.20
# Mon, 08 Mar 2021 22:11:50 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.0/src/haproxy-2.0.20.tar.gz
# Mon, 08 Mar 2021 22:11:50 GMT
ENV HAPROXY_SHA256=65153c989e7412f6815d3b047184bb07eeb73ccb10f5c05e757347ea6c317ce1
# Mon, 08 Mar 2021 22:12:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 08 Mar 2021 22:12:36 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 22:12:36 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 22:12:37 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 08 Mar 2021 22:12:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 22:12:38 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:27cbb00346a16ea900c1049a2e5b47942c586c377179e098382c8ca1c8e87966`  
		Last Modified: Tue, 09 Feb 2021 02:45:51 GMT  
		Size: 27.8 MB (27752731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b6129a97a33727ea8a598d1e797bccce491920bf29d769880cf2fc6d3e0436`  
		Last Modified: Mon, 08 Mar 2021 22:17:48 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5643251b7f4fc8419293a6fb8a01d41c9ec9077fa7760ca0f0bc4afd8b591433`  
		Last Modified: Mon, 08 Mar 2021 22:19:48 GMT  
		Size: 8.5 MB (8468532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cce7451d0b07bd6018bf0e51b34e0b4fc0d446bebe856f7a138e9f594a8437f2`  
		Last Modified: Mon, 08 Mar 2021 22:19:46 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5788e78f350c1aa999691491517c5f4d4291ca0a4126879673c68745c734bc3`  
		Last Modified: Mon, 08 Mar 2021 22:19:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.0.20` - linux; mips64le

```console
$ docker pull haproxy@sha256:68967fb5eb64c113a23e60d4023efcf834d1a431a16bc8759b75fb6d5384943d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33901649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:840fdab6364ef6e3cf852054298ee14aec686111645ed4529c4550bf051d8cb3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 03:09:26 GMT
ADD file:0222a151f4e5033d9eae98ce2b703a63f52d049dd72ac40bdd0dc2dafe619f0a in / 
# Tue, 09 Feb 2021 03:09:27 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:41:09 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 09 Feb 2021 03:51:37 GMT
ENV HAPROXY_VERSION=2.0.20
# Tue, 09 Feb 2021 03:51:37 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.0/src/haproxy-2.0.20.tar.gz
# Tue, 09 Feb 2021 03:51:38 GMT
ENV HAPROXY_SHA256=65153c989e7412f6815d3b047184bb07eeb73ccb10f5c05e757347ea6c317ce1
# Tue, 09 Feb 2021 03:53:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 09 Feb 2021 03:53:48 GMT
STOPSIGNAL SIGUSR1
# Tue, 09 Feb 2021 03:53:48 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 09 Feb 2021 03:53:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 09 Feb 2021 03:53:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Feb 2021 03:53:51 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:dfb81134097d874e01b495d1fba82e384056d0a3a45f01a69a2e86ae82af1e96`  
		Last Modified: Tue, 09 Feb 2021 03:15:55 GMT  
		Size: 25.8 MB (25764640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a549d56662447dd8cb15faf59ca0fc2eda7a877e9aee16aadd09fd46e4214a`  
		Last Modified: Tue, 09 Feb 2021 03:57:56 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc51d0de6bedfd89e339f209975d16d2169c7a6c02fb8628dc40bd170b9bd03`  
		Last Modified: Tue, 09 Feb 2021 03:59:15 GMT  
		Size: 8.1 MB (8135060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12c521c4e325cd0f343932ca83456482e8ae958aad502d7e84363548c24a3e99`  
		Last Modified: Tue, 09 Feb 2021 03:59:10 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c74ce4bc22662d59d6ca77fd41f06272d4fda648829082877fb0f19e08b9e492`  
		Last Modified: Tue, 09 Feb 2021 03:59:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.0.20` - linux; ppc64le

```console
$ docker pull haproxy@sha256:793105f03702a93d9358ead4f99b472c62368555d12a12a7475f952fcf0f1abf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.5 MB (39462448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8f011494c4956f6083b852c7e80ea70b31fe04a2670b5fe7527d0f2ca5abc4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:19:19 GMT
ADD file:9a8cfdf0eab394a693b5cde0700ad47b6e8506ef0b79fabb8a07874b96e6c394 in / 
# Tue, 09 Feb 2021 02:19:34 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 05:52:23 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 09 Feb 2021 06:17:12 GMT
ENV HAPROXY_VERSION=2.0.20
# Tue, 09 Feb 2021 06:17:21 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.0/src/haproxy-2.0.20.tar.gz
# Tue, 09 Feb 2021 06:17:30 GMT
ENV HAPROXY_SHA256=65153c989e7412f6815d3b047184bb07eeb73ccb10f5c05e757347ea6c317ce1
# Tue, 09 Feb 2021 06:23:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 09 Feb 2021 06:23:16 GMT
STOPSIGNAL SIGUSR1
# Tue, 09 Feb 2021 06:23:19 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 09 Feb 2021 06:23:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 09 Feb 2021 06:23:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Feb 2021 06:23:51 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:9996b4fb6bc1c50f95ba30f8988c9c89526556fa320d3fda59d3d8359f7810d6`  
		Last Modified: Tue, 09 Feb 2021 02:27:59 GMT  
		Size: 30.5 MB (30519509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7f600bc4989eb9f12d5006a73f5958eb4fe85f86bc4008d7a899bb935b0f1c`  
		Last Modified: Tue, 09 Feb 2021 06:38:36 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bd9ae063a2baa6da6d5ba0b880f52465941c6139534bc320e4040fdef11b55b`  
		Last Modified: Tue, 09 Feb 2021 06:39:37 GMT  
		Size: 8.9 MB (8940991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0fc094fa75a8808c9afd0e650f6b69cc6618f6c92a1e20ddf5b7db08e369b02`  
		Last Modified: Tue, 09 Feb 2021 06:39:36 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:861f5efadd0b26fc12ba3a5cdd72c11fde8ec20bc5945aeca5d60d8f79b72e80`  
		Last Modified: Tue, 09 Feb 2021 06:39:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.0.20` - linux; s390x

```console
$ docker pull haproxy@sha256:e23d1b61e10d2cdbce29a256e16ff6b02c68a71138fe188aab0de2dddb1e6a17
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33940345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbd22506827b48cbd914589a91bd5e7a08efbdaaf65d70d303928886d26787e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:42:10 GMT
ADD file:0edb2de05df54191a141bd125f59d7e14eef0cc4576927a247b8dd7d6f255d04 in / 
# Tue, 09 Feb 2021 02:42:12 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:39:30 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 09 Feb 2021 03:42:18 GMT
ENV HAPROXY_VERSION=2.0.20
# Tue, 09 Feb 2021 03:42:19 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.0/src/haproxy-2.0.20.tar.gz
# Tue, 09 Feb 2021 03:42:19 GMT
ENV HAPROXY_SHA256=65153c989e7412f6815d3b047184bb07eeb73ccb10f5c05e757347ea6c317ce1
# Tue, 09 Feb 2021 03:42:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 09 Feb 2021 03:42:45 GMT
STOPSIGNAL SIGUSR1
# Tue, 09 Feb 2021 03:42:45 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 09 Feb 2021 03:42:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 09 Feb 2021 03:42:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Feb 2021 03:42:46 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:032413a44cf56b097e48b8221bf475ca1bec26e7a27f35fe61d699366a335b79`  
		Last Modified: Tue, 09 Feb 2021 02:45:31 GMT  
		Size: 25.7 MB (25710021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e65f701864562492efa2c0035134b62d68efdb6e7241a0a2dcc3151e6d5775b`  
		Last Modified: Tue, 09 Feb 2021 03:44:28 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4282993cf1f51ab3fe5a2c3a932cab755669406bf14cd8796d80af35511256da`  
		Last Modified: Tue, 09 Feb 2021 03:45:11 GMT  
		Size: 8.2 MB (8228381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6e4094b538182a6bff81c60e5c11e422bc715412af2841a25ff4de192762b4`  
		Last Modified: Tue, 09 Feb 2021 03:45:10 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd033a2110f271869fd3ff33da4c18b608e13160de24c48155150385ef9fe9c6`  
		Last Modified: Tue, 09 Feb 2021 03:45:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haproxy:2.0.20-alpine`

```console
$ docker pull haproxy@sha256:d6d2dcae1f93485a2277c96eac5692bdc0bcd5be6849aa0781cd0c49dbbb6820
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `haproxy:2.0.20-alpine` - linux; amd64

```console
$ docker pull haproxy@sha256:61ddebc917f98e16a8c479f0fe90d01ed54c5f53ab7937449906f0a89b69e61e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8649801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39a4d54af66c5a8fe19e8b3677c22b0f6812b5c71cf640c14e91dd1636588ff1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 21:19:54 GMT
ADD file:80bf8bd014071345b1c0364eeb0a5e48f3fb0d87f9c31cb990e57caa652b59b8 in / 
# Wed, 17 Feb 2021 21:19:54 GMT
CMD ["/bin/sh"]
# Mon, 08 Mar 2021 21:38:26 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 21:48:18 GMT
ENV HAPROXY_VERSION=2.0.20
# Mon, 08 Mar 2021 21:48:18 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.0/src/haproxy-2.0.20.tar.gz
# Mon, 08 Mar 2021 21:48:19 GMT
ENV HAPROXY_SHA256=65153c989e7412f6815d3b047184bb07eeb73ccb10f5c05e757347ea6c317ce1
# Mon, 08 Mar 2021 21:49:11 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Mon, 08 Mar 2021 21:49:11 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 21:49:11 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 21:49:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 08 Mar 2021 21:49:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 21:49:13 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:ba3557a56b150f9b813f9d02274d62914fd8fce120dd374d9ee17b87cf1d277d`  
		Last Modified: Wed, 17 Feb 2021 21:20:25 GMT  
		Size: 2.8 MB (2811657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9216237f12c4d44ab183590086cf2a09004b5609c4b50871d88658faa495245`  
		Last Modified: Mon, 08 Mar 2021 21:52:45 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bce3e8fb2fc31479ee1526aba4b66534abd59ef2dc1b52d48cb9ad32646f5f7`  
		Last Modified: Mon, 08 Mar 2021 21:54:47 GMT  
		Size: 5.8 MB (5836387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76964579d9a00e41f65eae95867049c8f4ac9a121a7a963ba2973ac83e113743`  
		Last Modified: Mon, 08 Mar 2021 21:54:46 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e907e7f36a5aa7b1718f1e0424a775139bb8fc3d9979f896e42026bc49603bf`  
		Last Modified: Mon, 08 Mar 2021 21:54:47 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.0.20-alpine` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:8c6a6ea9fde7544678218f44fc1c99ee58da3c6f5a47d81b987dd1298b9ceb0e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8299651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5b123b2bb7dc7be94d173cfa94f04bab998834ddce12125e7f36fadd2d58524`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 20:49:32 GMT
ADD file:c04fbd3b039001c592cfa14f8388f8934ed4223ccf274dbb926e75039e172af4 in / 
# Wed, 17 Feb 2021 20:49:33 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 21:08:27 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 17 Feb 2021 21:10:57 GMT
ENV HAPROXY_VERSION=2.0.20
# Wed, 17 Feb 2021 21:10:58 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.0/src/haproxy-2.0.20.tar.gz
# Wed, 17 Feb 2021 21:10:58 GMT
ENV HAPROXY_SHA256=65153c989e7412f6815d3b047184bb07eeb73ccb10f5c05e757347ea6c317ce1
# Wed, 17 Feb 2021 21:11:17 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 17 Feb 2021 21:11:18 GMT
STOPSIGNAL SIGUSR1
# Wed, 17 Feb 2021 21:11:18 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 17 Feb 2021 21:11:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 17 Feb 2021 21:11:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Feb 2021 21:11:21 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:1353527ebe111f9bb1e271264a3c182e909e4b36463f80d7dbde1be0713eb892`  
		Last Modified: Wed, 17 Feb 2021 20:50:06 GMT  
		Size: 2.6 MB (2622039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d174378d3ee2c0c6e6a85b5228f929557826d80bcd23b2434093942f499361a7`  
		Last Modified: Wed, 17 Feb 2021 21:12:31 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15dd03e37139bfa10ab22cc83955f8ba8a4448663be68cde61ac5fe55fb2712c`  
		Last Modified: Wed, 17 Feb 2021 21:13:12 GMT  
		Size: 5.7 MB (5675857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:777e8769addf8b790ea5d6c1d7f3a1450dc0abd05be0678d9d8da1f36adbe26e`  
		Last Modified: Wed, 17 Feb 2021 21:13:10 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4451a13c479abd4e7cd3633b506f2964c5d88d65712b4ebbeef4e9459e74ab0`  
		Last Modified: Wed, 17 Feb 2021 21:13:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.0.20-alpine` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:bd47ef03aed5c8f9c981f88033d956bbb2140f667402ee94190d6ba1c95e272a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8073757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b10860c516424b07b1ed215b86098bff014c89ead12a754dae87f7fa6a967471`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 20:57:36 GMT
ADD file:efdd39e5243eaf378f12ad5a85d2222b44930850a90263e5f17e8a6b5e9bc9b8 in / 
# Wed, 17 Feb 2021 20:57:37 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 21:49:42 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 17 Feb 2021 21:52:58 GMT
ENV HAPROXY_VERSION=2.0.20
# Wed, 17 Feb 2021 21:52:58 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.0/src/haproxy-2.0.20.tar.gz
# Wed, 17 Feb 2021 21:52:59 GMT
ENV HAPROXY_SHA256=65153c989e7412f6815d3b047184bb07eeb73ccb10f5c05e757347ea6c317ce1
# Wed, 17 Feb 2021 21:53:21 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 17 Feb 2021 21:53:22 GMT
STOPSIGNAL SIGUSR1
# Wed, 17 Feb 2021 21:53:23 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 17 Feb 2021 21:53:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 17 Feb 2021 21:53:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Feb 2021 21:53:27 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f55b840e27d3dbe27e44497103a4397f043749f933eb0433d29e2f104b3435ef`  
		Last Modified: Wed, 17 Feb 2021 20:58:14 GMT  
		Size: 2.4 MB (2423892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86398e5ccaeed703d9464d57f2d97546fad0481312144292414eb1cf857b617f`  
		Last Modified: Wed, 17 Feb 2021 21:55:00 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ff2118b8156f4a2e5ae568f14c888dee9a7fe3a26437fc37174213658af1291`  
		Last Modified: Wed, 17 Feb 2021 21:55:48 GMT  
		Size: 5.6 MB (5648109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01151e1d8c646b34780bd372f90c33cf799ddd130cc450024d55eabf8fa53358`  
		Last Modified: Wed, 17 Feb 2021 21:55:45 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb22b07ca8270155e7a08b6b6eee9e15ad23cef78c18ad00ff302afe68de4a7`  
		Last Modified: Wed, 17 Feb 2021 21:55:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.0.20-alpine` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:d911cea07a3b30755492d2a56e0d37821a486eca1f16a12ab9d0722efadedf3f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8542373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad4ab84f222d5c04bba953828ca89884be69b5796a91d0678e9db9128962018b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 20:39:29 GMT
ADD file:3bf1497bd250cf7c73c12231dc4ebe3a3a67f2cd99e35bce47ef6674683aeb1d in / 
# Wed, 17 Feb 2021 20:39:30 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 21:36:08 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 17 Feb 2021 21:39:09 GMT
ENV HAPROXY_VERSION=2.0.20
# Wed, 17 Feb 2021 21:39:10 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.0/src/haproxy-2.0.20.tar.gz
# Wed, 17 Feb 2021 21:39:11 GMT
ENV HAPROXY_SHA256=65153c989e7412f6815d3b047184bb07eeb73ccb10f5c05e757347ea6c317ce1
# Wed, 17 Feb 2021 21:39:32 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 17 Feb 2021 21:39:33 GMT
STOPSIGNAL SIGUSR1
# Wed, 17 Feb 2021 21:39:34 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 17 Feb 2021 21:39:36 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 17 Feb 2021 21:39:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Feb 2021 21:39:37 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:069a56d6d07f6b186fbb82e4486616b9be9a37ce32a63013af6cddcb65898182`  
		Last Modified: Wed, 17 Feb 2021 20:40:04 GMT  
		Size: 2.7 MB (2711572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6644620fa9074da825714fc7794756e2b0e36f3e83ffc2bc01bbc9df0de9e373`  
		Last Modified: Wed, 17 Feb 2021 21:41:18 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17f339fc80b25fdae41c3fa7d82eb5d2aca5e2d3b82e54e6efb7c3d247734def`  
		Last Modified: Wed, 17 Feb 2021 21:41:59 GMT  
		Size: 5.8 MB (5829045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7564a8fb3aea20b243316caa8de2cba17ee48fb87b7e929c661b4a71ce60285d`  
		Last Modified: Wed, 17 Feb 2021 21:41:57 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be7ef4d8847f07f258cec09512a3d83bc50077ef5d3e0b39fbf6180e85d18467`  
		Last Modified: Wed, 17 Feb 2021 21:41:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.0.20-alpine` - linux; 386

```console
$ docker pull haproxy@sha256:440c59f0680ca675a334290ab59b45b1d6afea33018c2e5a85f6e88e03e0bef6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8507517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b68f9d5289d73231ec5f2bcede7184688ab52e0f6dece96e5b68c6a871fb6263`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 21:38:34 GMT
ADD file:eaee53da3c87749799de55809e4a5b526c56855332b961a85b1184c660f1d65b in / 
# Wed, 17 Feb 2021 21:38:35 GMT
CMD ["/bin/sh"]
# Mon, 08 Mar 2021 22:03:53 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 22:12:51 GMT
ENV HAPROXY_VERSION=2.0.20
# Mon, 08 Mar 2021 22:12:51 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.0/src/haproxy-2.0.20.tar.gz
# Mon, 08 Mar 2021 22:12:52 GMT
ENV HAPROXY_SHA256=65153c989e7412f6815d3b047184bb07eeb73ccb10f5c05e757347ea6c317ce1
# Mon, 08 Mar 2021 22:13:48 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Mon, 08 Mar 2021 22:13:48 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 22:13:48 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 22:13:49 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 08 Mar 2021 22:13:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 22:13:49 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:86205afa28f6bc624469015a543d16608258d2828411a92c662f4fdc6d276e18`  
		Last Modified: Wed, 17 Feb 2021 21:39:07 GMT  
		Size: 2.8 MB (2818177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080e85d941540171ac6a020af17b393f2a40b03d40b9677d708d31ffb6e31b71`  
		Last Modified: Mon, 08 Mar 2021 22:18:02 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaa1c22cf4e5cf993e8aa35d0736ec8eeb7b1e0f11dea3efa65c0ec22bd2ee4f`  
		Last Modified: Mon, 08 Mar 2021 22:20:02 GMT  
		Size: 5.7 MB (5687587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a439a4ed4899eec428dd8512c4f5b9b88f90fdf01fb6385cd2792b4b3c90db`  
		Last Modified: Mon, 08 Mar 2021 22:20:00 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:951642f641235b65143ffb408d80b6be9172485b44c81300147f0fcc65722d41`  
		Last Modified: Mon, 08 Mar 2021 22:20:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.0.20-alpine` - linux; ppc64le

```console
$ docker pull haproxy@sha256:a9497c0b64a27342b5a945b0ff3648c3f2a9a9177a353ed65e3e7218980d0396
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8852243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeddcc95a39477620aa9367ef8990e972110edb855bb814868f2a33f89f9fa40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 21:17:29 GMT
ADD file:28f4377c61c0f8eb43a6b36e6a24ef5893f51d405d25b62e364988223537ae0b in / 
# Wed, 17 Feb 2021 21:17:37 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 22:10:46 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 17 Feb 2021 22:18:35 GMT
ENV HAPROXY_VERSION=2.0.20
# Wed, 17 Feb 2021 22:18:42 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.0/src/haproxy-2.0.20.tar.gz
# Wed, 17 Feb 2021 22:18:47 GMT
ENV HAPROXY_SHA256=65153c989e7412f6815d3b047184bb07eeb73ccb10f5c05e757347ea6c317ce1
# Wed, 17 Feb 2021 22:19:34 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 17 Feb 2021 22:19:44 GMT
STOPSIGNAL SIGUSR1
# Wed, 17 Feb 2021 22:19:47 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 17 Feb 2021 22:20:04 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 17 Feb 2021 22:20:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Feb 2021 22:20:24 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:cb672e0375a8f9bb3d33049ceb372ffa49b959bfc84fe6f72bfb97b682a608c8`  
		Last Modified: Wed, 17 Feb 2021 21:18:10 GMT  
		Size: 2.8 MB (2813081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f391a7d74b9bf5c2089e7957996d00d99ddc33d8295873bf28746716bb728a`  
		Last Modified: Wed, 17 Feb 2021 22:23:02 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b8a2918c79b70ca1a888fb3f8e0883625161c1696335aa130208ade42f018a2`  
		Last Modified: Wed, 17 Feb 2021 22:24:00 GMT  
		Size: 6.0 MB (6037400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0821d4907d535068a6e28a48b0783ec27276d5feebf0996f91159444fcefb9e`  
		Last Modified: Wed, 17 Feb 2021 22:23:58 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee2a04e1f33c06a7feaee16d61085de80b67bb1c922653ba42a337985012623`  
		Last Modified: Wed, 17 Feb 2021 22:23:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.0.20-alpine` - linux; s390x

```console
$ docker pull haproxy@sha256:20fadd7e2c221b1cc0cc9555cbb792127c14ea6b4a04c614db19a175e5fa0ffa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8368358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dda5bebcfc651fb54614b80c148e799ae14b3af0c60f01fa994c53998c2f180`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 20:41:27 GMT
ADD file:630c66f8d774d75b51e32aff812b438d377ebd3389c4aa6c324fdf8c03b6fa13 in / 
# Wed, 17 Feb 2021 20:41:27 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 21:33:33 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 17 Feb 2021 21:40:19 GMT
ENV HAPROXY_VERSION=2.0.20
# Wed, 17 Feb 2021 21:40:19 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.0/src/haproxy-2.0.20.tar.gz
# Wed, 17 Feb 2021 21:40:20 GMT
ENV HAPROXY_SHA256=65153c989e7412f6815d3b047184bb07eeb73ccb10f5c05e757347ea6c317ce1
# Wed, 17 Feb 2021 21:41:38 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 17 Feb 2021 21:41:39 GMT
STOPSIGNAL SIGUSR1
# Wed, 17 Feb 2021 21:41:40 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 17 Feb 2021 21:41:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 17 Feb 2021 21:41:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Feb 2021 21:41:44 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:ff5e8cb87555e9fa38a441f5cf0414e91353e2cd21cdb48d48b7de5bb39ce674`  
		Last Modified: Wed, 17 Feb 2021 20:41:58 GMT  
		Size: 2.6 MB (2602381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de25a3a0de168e6603cb978691ef3e7f11d7c9108d0ade38d3185d5d9dbdc094`  
		Last Modified: Wed, 17 Feb 2021 21:43:59 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43646cbce92e1609d894b4f24b64cf6d559615e094109b16971e5254b23b89b3`  
		Last Modified: Wed, 17 Feb 2021 21:44:39 GMT  
		Size: 5.8 MB (5764220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c39d68a1f090326a7afbf54bd10a19875dcbb1ced699ed80b22b6239afbd914`  
		Last Modified: Wed, 17 Feb 2021 21:44:37 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caaba189c1d89312179458b0da455a6fbf4a2920ece95cce08c186d267d6b5f8`  
		Last Modified: Wed, 17 Feb 2021 21:44:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haproxy:2.0-alpine`

```console
$ docker pull haproxy@sha256:d6d2dcae1f93485a2277c96eac5692bdc0bcd5be6849aa0781cd0c49dbbb6820
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `haproxy:2.0-alpine` - linux; amd64

```console
$ docker pull haproxy@sha256:61ddebc917f98e16a8c479f0fe90d01ed54c5f53ab7937449906f0a89b69e61e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8649801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39a4d54af66c5a8fe19e8b3677c22b0f6812b5c71cf640c14e91dd1636588ff1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 21:19:54 GMT
ADD file:80bf8bd014071345b1c0364eeb0a5e48f3fb0d87f9c31cb990e57caa652b59b8 in / 
# Wed, 17 Feb 2021 21:19:54 GMT
CMD ["/bin/sh"]
# Mon, 08 Mar 2021 21:38:26 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 21:48:18 GMT
ENV HAPROXY_VERSION=2.0.20
# Mon, 08 Mar 2021 21:48:18 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.0/src/haproxy-2.0.20.tar.gz
# Mon, 08 Mar 2021 21:48:19 GMT
ENV HAPROXY_SHA256=65153c989e7412f6815d3b047184bb07eeb73ccb10f5c05e757347ea6c317ce1
# Mon, 08 Mar 2021 21:49:11 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Mon, 08 Mar 2021 21:49:11 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 21:49:11 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 21:49:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 08 Mar 2021 21:49:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 21:49:13 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:ba3557a56b150f9b813f9d02274d62914fd8fce120dd374d9ee17b87cf1d277d`  
		Last Modified: Wed, 17 Feb 2021 21:20:25 GMT  
		Size: 2.8 MB (2811657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9216237f12c4d44ab183590086cf2a09004b5609c4b50871d88658faa495245`  
		Last Modified: Mon, 08 Mar 2021 21:52:45 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bce3e8fb2fc31479ee1526aba4b66534abd59ef2dc1b52d48cb9ad32646f5f7`  
		Last Modified: Mon, 08 Mar 2021 21:54:47 GMT  
		Size: 5.8 MB (5836387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76964579d9a00e41f65eae95867049c8f4ac9a121a7a963ba2973ac83e113743`  
		Last Modified: Mon, 08 Mar 2021 21:54:46 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e907e7f36a5aa7b1718f1e0424a775139bb8fc3d9979f896e42026bc49603bf`  
		Last Modified: Mon, 08 Mar 2021 21:54:47 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.0-alpine` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:8c6a6ea9fde7544678218f44fc1c99ee58da3c6f5a47d81b987dd1298b9ceb0e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8299651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5b123b2bb7dc7be94d173cfa94f04bab998834ddce12125e7f36fadd2d58524`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 20:49:32 GMT
ADD file:c04fbd3b039001c592cfa14f8388f8934ed4223ccf274dbb926e75039e172af4 in / 
# Wed, 17 Feb 2021 20:49:33 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 21:08:27 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 17 Feb 2021 21:10:57 GMT
ENV HAPROXY_VERSION=2.0.20
# Wed, 17 Feb 2021 21:10:58 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.0/src/haproxy-2.0.20.tar.gz
# Wed, 17 Feb 2021 21:10:58 GMT
ENV HAPROXY_SHA256=65153c989e7412f6815d3b047184bb07eeb73ccb10f5c05e757347ea6c317ce1
# Wed, 17 Feb 2021 21:11:17 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 17 Feb 2021 21:11:18 GMT
STOPSIGNAL SIGUSR1
# Wed, 17 Feb 2021 21:11:18 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 17 Feb 2021 21:11:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 17 Feb 2021 21:11:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Feb 2021 21:11:21 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:1353527ebe111f9bb1e271264a3c182e909e4b36463f80d7dbde1be0713eb892`  
		Last Modified: Wed, 17 Feb 2021 20:50:06 GMT  
		Size: 2.6 MB (2622039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d174378d3ee2c0c6e6a85b5228f929557826d80bcd23b2434093942f499361a7`  
		Last Modified: Wed, 17 Feb 2021 21:12:31 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15dd03e37139bfa10ab22cc83955f8ba8a4448663be68cde61ac5fe55fb2712c`  
		Last Modified: Wed, 17 Feb 2021 21:13:12 GMT  
		Size: 5.7 MB (5675857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:777e8769addf8b790ea5d6c1d7f3a1450dc0abd05be0678d9d8da1f36adbe26e`  
		Last Modified: Wed, 17 Feb 2021 21:13:10 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4451a13c479abd4e7cd3633b506f2964c5d88d65712b4ebbeef4e9459e74ab0`  
		Last Modified: Wed, 17 Feb 2021 21:13:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.0-alpine` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:bd47ef03aed5c8f9c981f88033d956bbb2140f667402ee94190d6ba1c95e272a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8073757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b10860c516424b07b1ed215b86098bff014c89ead12a754dae87f7fa6a967471`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 20:57:36 GMT
ADD file:efdd39e5243eaf378f12ad5a85d2222b44930850a90263e5f17e8a6b5e9bc9b8 in / 
# Wed, 17 Feb 2021 20:57:37 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 21:49:42 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 17 Feb 2021 21:52:58 GMT
ENV HAPROXY_VERSION=2.0.20
# Wed, 17 Feb 2021 21:52:58 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.0/src/haproxy-2.0.20.tar.gz
# Wed, 17 Feb 2021 21:52:59 GMT
ENV HAPROXY_SHA256=65153c989e7412f6815d3b047184bb07eeb73ccb10f5c05e757347ea6c317ce1
# Wed, 17 Feb 2021 21:53:21 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 17 Feb 2021 21:53:22 GMT
STOPSIGNAL SIGUSR1
# Wed, 17 Feb 2021 21:53:23 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 17 Feb 2021 21:53:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 17 Feb 2021 21:53:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Feb 2021 21:53:27 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f55b840e27d3dbe27e44497103a4397f043749f933eb0433d29e2f104b3435ef`  
		Last Modified: Wed, 17 Feb 2021 20:58:14 GMT  
		Size: 2.4 MB (2423892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86398e5ccaeed703d9464d57f2d97546fad0481312144292414eb1cf857b617f`  
		Last Modified: Wed, 17 Feb 2021 21:55:00 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ff2118b8156f4a2e5ae568f14c888dee9a7fe3a26437fc37174213658af1291`  
		Last Modified: Wed, 17 Feb 2021 21:55:48 GMT  
		Size: 5.6 MB (5648109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01151e1d8c646b34780bd372f90c33cf799ddd130cc450024d55eabf8fa53358`  
		Last Modified: Wed, 17 Feb 2021 21:55:45 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb22b07ca8270155e7a08b6b6eee9e15ad23cef78c18ad00ff302afe68de4a7`  
		Last Modified: Wed, 17 Feb 2021 21:55:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.0-alpine` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:d911cea07a3b30755492d2a56e0d37821a486eca1f16a12ab9d0722efadedf3f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8542373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad4ab84f222d5c04bba953828ca89884be69b5796a91d0678e9db9128962018b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 20:39:29 GMT
ADD file:3bf1497bd250cf7c73c12231dc4ebe3a3a67f2cd99e35bce47ef6674683aeb1d in / 
# Wed, 17 Feb 2021 20:39:30 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 21:36:08 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 17 Feb 2021 21:39:09 GMT
ENV HAPROXY_VERSION=2.0.20
# Wed, 17 Feb 2021 21:39:10 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.0/src/haproxy-2.0.20.tar.gz
# Wed, 17 Feb 2021 21:39:11 GMT
ENV HAPROXY_SHA256=65153c989e7412f6815d3b047184bb07eeb73ccb10f5c05e757347ea6c317ce1
# Wed, 17 Feb 2021 21:39:32 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 17 Feb 2021 21:39:33 GMT
STOPSIGNAL SIGUSR1
# Wed, 17 Feb 2021 21:39:34 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 17 Feb 2021 21:39:36 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 17 Feb 2021 21:39:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Feb 2021 21:39:37 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:069a56d6d07f6b186fbb82e4486616b9be9a37ce32a63013af6cddcb65898182`  
		Last Modified: Wed, 17 Feb 2021 20:40:04 GMT  
		Size: 2.7 MB (2711572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6644620fa9074da825714fc7794756e2b0e36f3e83ffc2bc01bbc9df0de9e373`  
		Last Modified: Wed, 17 Feb 2021 21:41:18 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17f339fc80b25fdae41c3fa7d82eb5d2aca5e2d3b82e54e6efb7c3d247734def`  
		Last Modified: Wed, 17 Feb 2021 21:41:59 GMT  
		Size: 5.8 MB (5829045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7564a8fb3aea20b243316caa8de2cba17ee48fb87b7e929c661b4a71ce60285d`  
		Last Modified: Wed, 17 Feb 2021 21:41:57 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be7ef4d8847f07f258cec09512a3d83bc50077ef5d3e0b39fbf6180e85d18467`  
		Last Modified: Wed, 17 Feb 2021 21:41:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.0-alpine` - linux; 386

```console
$ docker pull haproxy@sha256:440c59f0680ca675a334290ab59b45b1d6afea33018c2e5a85f6e88e03e0bef6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8507517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b68f9d5289d73231ec5f2bcede7184688ab52e0f6dece96e5b68c6a871fb6263`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 21:38:34 GMT
ADD file:eaee53da3c87749799de55809e4a5b526c56855332b961a85b1184c660f1d65b in / 
# Wed, 17 Feb 2021 21:38:35 GMT
CMD ["/bin/sh"]
# Mon, 08 Mar 2021 22:03:53 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 22:12:51 GMT
ENV HAPROXY_VERSION=2.0.20
# Mon, 08 Mar 2021 22:12:51 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.0/src/haproxy-2.0.20.tar.gz
# Mon, 08 Mar 2021 22:12:52 GMT
ENV HAPROXY_SHA256=65153c989e7412f6815d3b047184bb07eeb73ccb10f5c05e757347ea6c317ce1
# Mon, 08 Mar 2021 22:13:48 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Mon, 08 Mar 2021 22:13:48 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 22:13:48 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 22:13:49 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 08 Mar 2021 22:13:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 22:13:49 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:86205afa28f6bc624469015a543d16608258d2828411a92c662f4fdc6d276e18`  
		Last Modified: Wed, 17 Feb 2021 21:39:07 GMT  
		Size: 2.8 MB (2818177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080e85d941540171ac6a020af17b393f2a40b03d40b9677d708d31ffb6e31b71`  
		Last Modified: Mon, 08 Mar 2021 22:18:02 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaa1c22cf4e5cf993e8aa35d0736ec8eeb7b1e0f11dea3efa65c0ec22bd2ee4f`  
		Last Modified: Mon, 08 Mar 2021 22:20:02 GMT  
		Size: 5.7 MB (5687587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a439a4ed4899eec428dd8512c4f5b9b88f90fdf01fb6385cd2792b4b3c90db`  
		Last Modified: Mon, 08 Mar 2021 22:20:00 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:951642f641235b65143ffb408d80b6be9172485b44c81300147f0fcc65722d41`  
		Last Modified: Mon, 08 Mar 2021 22:20:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.0-alpine` - linux; ppc64le

```console
$ docker pull haproxy@sha256:a9497c0b64a27342b5a945b0ff3648c3f2a9a9177a353ed65e3e7218980d0396
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8852243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeddcc95a39477620aa9367ef8990e972110edb855bb814868f2a33f89f9fa40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 21:17:29 GMT
ADD file:28f4377c61c0f8eb43a6b36e6a24ef5893f51d405d25b62e364988223537ae0b in / 
# Wed, 17 Feb 2021 21:17:37 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 22:10:46 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 17 Feb 2021 22:18:35 GMT
ENV HAPROXY_VERSION=2.0.20
# Wed, 17 Feb 2021 22:18:42 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.0/src/haproxy-2.0.20.tar.gz
# Wed, 17 Feb 2021 22:18:47 GMT
ENV HAPROXY_SHA256=65153c989e7412f6815d3b047184bb07eeb73ccb10f5c05e757347ea6c317ce1
# Wed, 17 Feb 2021 22:19:34 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 17 Feb 2021 22:19:44 GMT
STOPSIGNAL SIGUSR1
# Wed, 17 Feb 2021 22:19:47 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 17 Feb 2021 22:20:04 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 17 Feb 2021 22:20:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Feb 2021 22:20:24 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:cb672e0375a8f9bb3d33049ceb372ffa49b959bfc84fe6f72bfb97b682a608c8`  
		Last Modified: Wed, 17 Feb 2021 21:18:10 GMT  
		Size: 2.8 MB (2813081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f391a7d74b9bf5c2089e7957996d00d99ddc33d8295873bf28746716bb728a`  
		Last Modified: Wed, 17 Feb 2021 22:23:02 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b8a2918c79b70ca1a888fb3f8e0883625161c1696335aa130208ade42f018a2`  
		Last Modified: Wed, 17 Feb 2021 22:24:00 GMT  
		Size: 6.0 MB (6037400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0821d4907d535068a6e28a48b0783ec27276d5feebf0996f91159444fcefb9e`  
		Last Modified: Wed, 17 Feb 2021 22:23:58 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee2a04e1f33c06a7feaee16d61085de80b67bb1c922653ba42a337985012623`  
		Last Modified: Wed, 17 Feb 2021 22:23:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.0-alpine` - linux; s390x

```console
$ docker pull haproxy@sha256:20fadd7e2c221b1cc0cc9555cbb792127c14ea6b4a04c614db19a175e5fa0ffa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8368358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dda5bebcfc651fb54614b80c148e799ae14b3af0c60f01fa994c53998c2f180`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 20:41:27 GMT
ADD file:630c66f8d774d75b51e32aff812b438d377ebd3389c4aa6c324fdf8c03b6fa13 in / 
# Wed, 17 Feb 2021 20:41:27 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 21:33:33 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 17 Feb 2021 21:40:19 GMT
ENV HAPROXY_VERSION=2.0.20
# Wed, 17 Feb 2021 21:40:19 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.0/src/haproxy-2.0.20.tar.gz
# Wed, 17 Feb 2021 21:40:20 GMT
ENV HAPROXY_SHA256=65153c989e7412f6815d3b047184bb07eeb73ccb10f5c05e757347ea6c317ce1
# Wed, 17 Feb 2021 21:41:38 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 17 Feb 2021 21:41:39 GMT
STOPSIGNAL SIGUSR1
# Wed, 17 Feb 2021 21:41:40 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 17 Feb 2021 21:41:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 17 Feb 2021 21:41:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Feb 2021 21:41:44 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:ff5e8cb87555e9fa38a441f5cf0414e91353e2cd21cdb48d48b7de5bb39ce674`  
		Last Modified: Wed, 17 Feb 2021 20:41:58 GMT  
		Size: 2.6 MB (2602381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de25a3a0de168e6603cb978691ef3e7f11d7c9108d0ade38d3185d5d9dbdc094`  
		Last Modified: Wed, 17 Feb 2021 21:43:59 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43646cbce92e1609d894b4f24b64cf6d559615e094109b16971e5254b23b89b3`  
		Last Modified: Wed, 17 Feb 2021 21:44:39 GMT  
		Size: 5.8 MB (5764220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c39d68a1f090326a7afbf54bd10a19875dcbb1ced699ed80b22b6239afbd914`  
		Last Modified: Wed, 17 Feb 2021 21:44:37 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caaba189c1d89312179458b0da455a6fbf4a2920ece95cce08c186d267d6b5f8`  
		Last Modified: Wed, 17 Feb 2021 21:44:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haproxy:2.1`

```console
$ docker pull haproxy@sha256:b15ed53ebe5defe9b1d5c719c5a8473477185d892bd9217b6fdf219680906524
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `haproxy:2.1` - linux; amd64

```console
$ docker pull haproxy@sha256:058036aaab4b4372e0cbf4a914b684b6dd6bca4a9b8357ea1d123e1ec29bede4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36154168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97108b00299f21c34d42f1524a60a634c2e00efa7ea720baf71107abb0a0b8b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Mon, 08 Mar 2021 21:37:25 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 21:44:29 GMT
ENV HAPROXY_VERSION=2.1.11
# Mon, 08 Mar 2021 21:44:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.1/src/haproxy-2.1.11.tar.gz
# Mon, 08 Mar 2021 21:44:30 GMT
ENV HAPROXY_SHA256=feff37a5459d7aca8fcca50fa0e6d20d176394019cec3be17ec9c6ba0fdbdbad
# Mon, 08 Mar 2021 21:45:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 08 Mar 2021 21:45:27 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 21:45:27 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 21:45:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 08 Mar 2021 21:45:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 21:45:29 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7bca45a971fe608786870ce75c9976f8e5a958f55e1287a6120048b897c63b6`  
		Last Modified: Mon, 08 Mar 2021 21:52:33 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b04d31d88d6e0c90d4599ecb9cda1dbc54aafa82dd863b8ec9caf196fcf69eb`  
		Last Modified: Mon, 08 Mar 2021 21:54:13 GMT  
		Size: 9.1 MB (9057077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b84dc2397a3e235ab2c545e139ab48c7f400d604ae96e1affb6285edce9112`  
		Last Modified: Mon, 08 Mar 2021 21:54:11 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c51e426666164bda770b6005c8bafd1df5cd8f857bbae74b7cbe0a094158738`  
		Last Modified: Mon, 08 Mar 2021 21:54:11 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.1` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:26f3d30aef07184cb201597c8910cc48ba3828d2d706c5c4835c97de505f671d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33343094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94be1557923ed2e99c8d58f36cf17059121d2c50af35302f4fc85f28cce4a719`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:50:10 GMT
ADD file:fbd00ef7871dc27d7ed5fa8c238cdc80652bd87b8033be7de9e54a799bbf10a4 in / 
# Tue, 09 Feb 2021 02:50:11 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:45:24 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 09 Feb 2021 03:49:52 GMT
ENV HAPROXY_VERSION=2.1.11
# Tue, 09 Feb 2021 03:49:53 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.1/src/haproxy-2.1.11.tar.gz
# Tue, 09 Feb 2021 03:49:54 GMT
ENV HAPROXY_SHA256=feff37a5459d7aca8fcca50fa0e6d20d176394019cec3be17ec9c6ba0fdbdbad
# Tue, 09 Feb 2021 03:50:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 09 Feb 2021 03:50:48 GMT
STOPSIGNAL SIGUSR1
# Tue, 09 Feb 2021 03:50:49 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 09 Feb 2021 03:50:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 09 Feb 2021 03:50:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Feb 2021 03:50:53 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:8e683fcc73f4da7d69ce1d5f4e1d77510aa459490068f38db2d8663698b391a0`  
		Last Modified: Tue, 09 Feb 2021 02:59:07 GMT  
		Size: 24.8 MB (24839297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def565d52deae74587a55f60d168bd531ebe8095c594027b7057a8fc1be0e8af`  
		Last Modified: Tue, 09 Feb 2021 03:54:54 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b901b8357320b59dd49f063f6922b16fd20f8ab67b11a840792c2498622b6cc7`  
		Last Modified: Tue, 09 Feb 2021 03:55:32 GMT  
		Size: 8.5 MB (8501855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:566a6e271324efe6d84666edb4303fadfc6fb3610a165e58b42e721275cc3de6`  
		Last Modified: Tue, 09 Feb 2021 03:55:30 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b12f544536b33776045decfb1c352c4df5f286f4eabc8c667eeb21c990c8bd`  
		Last Modified: Tue, 09 Feb 2021 03:55:30 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.1` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:7139d6104e3f401f4a46dd88d848b5f27865bd4c42bb8bd96e5e297c84ee70f3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31156536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3852b0d58b81ee4c90beddd66ad4c7b1926696f1dcfb9153b883f549741066a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 03:00:57 GMT
ADD file:e675d50366bde57173a75f9a29367d765e7da2b7254c5254b64e777cf6870502 in / 
# Tue, 09 Feb 2021 03:01:00 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:49:38 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 09 Feb 2021 03:53:23 GMT
ENV HAPROXY_VERSION=2.1.11
# Tue, 09 Feb 2021 03:53:24 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.1/src/haproxy-2.1.11.tar.gz
# Tue, 09 Feb 2021 03:53:26 GMT
ENV HAPROXY_SHA256=feff37a5459d7aca8fcca50fa0e6d20d176394019cec3be17ec9c6ba0fdbdbad
# Tue, 09 Feb 2021 03:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 09 Feb 2021 03:54:12 GMT
STOPSIGNAL SIGUSR1
# Tue, 09 Feb 2021 03:54:13 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 09 Feb 2021 03:54:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 09 Feb 2021 03:54:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Feb 2021 03:54:19 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:db574d82360c3b60abadbef4f3daf8dee01f24741fc6ab3692aa543558d8b624`  
		Last Modified: Tue, 09 Feb 2021 03:09:46 GMT  
		Size: 22.7 MB (22703384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9978ebb1881387f11e025fb46dce2b3c715f705f6d240737574f8848c27fa0d7`  
		Last Modified: Tue, 09 Feb 2021 03:58:16 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bcb1b2473bdb76e258f75a463bb5e432005cc44a6fdefa0689128dfb747cce7`  
		Last Modified: Tue, 09 Feb 2021 03:58:55 GMT  
		Size: 8.5 MB (8451207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc84cf69cc9d486b9de9a8df58e30461e02dc671868478ca12cbb001589ff077`  
		Last Modified: Tue, 09 Feb 2021 03:58:52 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ab3f670e0d98cda8512cfb573f7fe22d728ff4a97ee08fa4e524ecaa82106a`  
		Last Modified: Tue, 09 Feb 2021 03:58:52 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.1` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:ef132befede302d23ace72d693c00b429ab16ebbb873b68acc4b23e443ba51ca
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34713983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31f6a7ef05bf3dae3334f2fd2c62781f0068525af801e3c215cf32f7cedd41a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:41:10 GMT
ADD file:d906dedaf14d8e3874b46787f7a1dbf268bc124c4e1dd32f13f3079e12f22238 in / 
# Tue, 09 Feb 2021 02:41:13 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:59:41 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 09 Feb 2021 04:03:41 GMT
ENV HAPROXY_VERSION=2.1.11
# Tue, 09 Feb 2021 04:03:42 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.1/src/haproxy-2.1.11.tar.gz
# Tue, 09 Feb 2021 04:03:44 GMT
ENV HAPROXY_SHA256=feff37a5459d7aca8fcca50fa0e6d20d176394019cec3be17ec9c6ba0fdbdbad
# Tue, 09 Feb 2021 04:04:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 09 Feb 2021 04:04:31 GMT
STOPSIGNAL SIGUSR1
# Tue, 09 Feb 2021 04:04:32 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 09 Feb 2021 04:04:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 09 Feb 2021 04:04:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Feb 2021 04:04:35 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:83c5cfdaa5385ea6fc4d31e724fd4dc5d74de847a7bdd968555b8f2c558dac0e`  
		Last Modified: Tue, 09 Feb 2021 02:47:27 GMT  
		Size: 25.9 MB (25851449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b7f43dd52365bce2c2b75f29577aa39d2b5794e2561cddc0678422ffc1f7d15`  
		Last Modified: Tue, 09 Feb 2021 04:08:36 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d84fe349f988c1566dcd75b8e50704040f9f5f022501d22271ac88b703075b0d`  
		Last Modified: Tue, 09 Feb 2021 04:09:15 GMT  
		Size: 8.9 MB (8860589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08436cd1d3b23ec9b417fa7e21536bfd0a8c04ddb529ad5ba9cd4746db953000`  
		Last Modified: Tue, 09 Feb 2021 04:09:12 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e90c5be53b8aac6be1540c928e1229848f339c435f23a2b4c32675055a2042d`  
		Last Modified: Tue, 09 Feb 2021 04:09:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.1` - linux; 386

```console
$ docker pull haproxy@sha256:0a9bd9a8d59f9a79710c7c477f1226b6260f0462f2615e0b76d89df2f650db9e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 MB (36565407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8afbb14bb10e86b5cdbcbc5c696f346ff0e849f5ce45af24768e3f8f99c92477`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:39:47 GMT
ADD file:61c31b1037672781ed0ecbc080ee3d49c83af49f5578b011544513fa9625698d in / 
# Tue, 09 Feb 2021 02:39:47 GMT
CMD ["bash"]
# Mon, 08 Mar 2021 22:02:40 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 22:09:35 GMT
ENV HAPROXY_VERSION=2.1.11
# Mon, 08 Mar 2021 22:09:35 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.1/src/haproxy-2.1.11.tar.gz
# Mon, 08 Mar 2021 22:09:36 GMT
ENV HAPROXY_SHA256=feff37a5459d7aca8fcca50fa0e6d20d176394019cec3be17ec9c6ba0fdbdbad
# Mon, 08 Mar 2021 22:10:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 08 Mar 2021 22:10:23 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 22:10:23 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 22:10:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 08 Mar 2021 22:10:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 22:10:24 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:27cbb00346a16ea900c1049a2e5b47942c586c377179e098382c8ca1c8e87966`  
		Last Modified: Tue, 09 Feb 2021 02:45:51 GMT  
		Size: 27.8 MB (27752731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b6129a97a33727ea8a598d1e797bccce491920bf29d769880cf2fc6d3e0436`  
		Last Modified: Mon, 08 Mar 2021 22:17:48 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7b31d0097aeefea7422dea4783723139cdfd025d373e858a39e4fb95f1f7c01`  
		Last Modified: Mon, 08 Mar 2021 22:19:22 GMT  
		Size: 8.8 MB (8810733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f10d72141d055778e8b7118ca07e30eaf4e07fbb0ed781d176d5ce823fa1e5c0`  
		Last Modified: Mon, 08 Mar 2021 22:19:20 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16f30853317863b120654aab5803d2ffb8ccd75d3b0d2242401db244157cc458`  
		Last Modified: Mon, 08 Mar 2021 22:19:20 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.1` - linux; mips64le

```console
$ docker pull haproxy@sha256:3e78da0c9d0f2ea8febf75b34d66e9619a6219c8abbfc9671185293e6125cfa4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 MB (34224406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bfd9376d31463612782d09216e96923106291708f3bd686c7a3ad4000dda001`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 03:09:26 GMT
ADD file:0222a151f4e5033d9eae98ce2b703a63f52d049dd72ac40bdd0dc2dafe619f0a in / 
# Tue, 09 Feb 2021 03:09:27 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:41:09 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 09 Feb 2021 03:49:11 GMT
ENV HAPROXY_VERSION=2.1.11
# Tue, 09 Feb 2021 03:49:12 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.1/src/haproxy-2.1.11.tar.gz
# Tue, 09 Feb 2021 03:49:12 GMT
ENV HAPROXY_SHA256=feff37a5459d7aca8fcca50fa0e6d20d176394019cec3be17ec9c6ba0fdbdbad
# Tue, 09 Feb 2021 03:51:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 09 Feb 2021 03:51:24 GMT
STOPSIGNAL SIGUSR1
# Tue, 09 Feb 2021 03:51:24 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 09 Feb 2021 03:51:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 09 Feb 2021 03:51:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Feb 2021 03:51:26 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:dfb81134097d874e01b495d1fba82e384056d0a3a45f01a69a2e86ae82af1e96`  
		Last Modified: Tue, 09 Feb 2021 03:15:55 GMT  
		Size: 25.8 MB (25764640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a549d56662447dd8cb15faf59ca0fc2eda7a877e9aee16aadd09fd46e4214a`  
		Last Modified: Tue, 09 Feb 2021 03:57:56 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9d53512fc5751fa60369bcb6c8c9bafb34cf3b5616ce67d8409bcffaa0b216c`  
		Last Modified: Tue, 09 Feb 2021 03:58:59 GMT  
		Size: 8.5 MB (8457816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32a5ae3fa74e543af85b70b61154a9a6313f75530877683daf062ef7b8632d36`  
		Last Modified: Tue, 09 Feb 2021 03:58:52 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f52283468e8de4724ac1b6f0199e12907e8cdf9ca893f588c1d454847e11feec`  
		Last Modified: Tue, 09 Feb 2021 03:58:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.1` - linux; ppc64le

```console
$ docker pull haproxy@sha256:dd5e46016691fc71840fc0400fb94617e39c49f45c3ff78cedf550988665b752
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39820097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107863456d835cb525fb772a5c0e28e8f2910f312e057b1380937dafe10b5c5a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:19:19 GMT
ADD file:9a8cfdf0eab394a693b5cde0700ad47b6e8506ef0b79fabb8a07874b96e6c394 in / 
# Tue, 09 Feb 2021 02:19:34 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 05:52:23 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 09 Feb 2021 06:11:36 GMT
ENV HAPROXY_VERSION=2.1.11
# Tue, 09 Feb 2021 06:11:48 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.1/src/haproxy-2.1.11.tar.gz
# Tue, 09 Feb 2021 06:11:57 GMT
ENV HAPROXY_SHA256=feff37a5459d7aca8fcca50fa0e6d20d176394019cec3be17ec9c6ba0fdbdbad
# Tue, 09 Feb 2021 06:16:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 09 Feb 2021 06:16:17 GMT
STOPSIGNAL SIGUSR1
# Tue, 09 Feb 2021 06:16:19 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 09 Feb 2021 06:16:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 09 Feb 2021 06:16:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Feb 2021 06:16:44 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:9996b4fb6bc1c50f95ba30f8988c9c89526556fa320d3fda59d3d8359f7810d6`  
		Last Modified: Tue, 09 Feb 2021 02:27:59 GMT  
		Size: 30.5 MB (30519509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7f600bc4989eb9f12d5006a73f5958eb4fe85f86bc4008d7a899bb935b0f1c`  
		Last Modified: Tue, 09 Feb 2021 06:38:36 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a959a5a513b4378da0a41c518deec7e5adf652eb1f48393785fe90b50fbd9ad`  
		Last Modified: Tue, 09 Feb 2021 06:39:23 GMT  
		Size: 9.3 MB (9298641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f96fc9d1b9d1da7faa15e5e3347d6b04cab67039937dbf04210037aee2fc1add`  
		Last Modified: Tue, 09 Feb 2021 06:39:23 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:229c9ec499471cf6a59cf55fd4341ea8bf993ec1e8f8fa909739a65d21a74c7a`  
		Last Modified: Tue, 09 Feb 2021 06:39:21 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.1` - linux; s390x

```console
$ docker pull haproxy@sha256:94e335f859a33da8c30ff8d118e391de396b87623f2959052b0779495be24178
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34265227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72291b86a2d7c33c2201cfe944eabe11323a4fc62ccdcd43b367e780c0584572`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:42:10 GMT
ADD file:0edb2de05df54191a141bd125f59d7e14eef0cc4576927a247b8dd7d6f255d04 in / 
# Tue, 09 Feb 2021 02:42:12 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:39:30 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 09 Feb 2021 03:41:38 GMT
ENV HAPROXY_VERSION=2.1.11
# Tue, 09 Feb 2021 03:41:39 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.1/src/haproxy-2.1.11.tar.gz
# Tue, 09 Feb 2021 03:41:39 GMT
ENV HAPROXY_SHA256=feff37a5459d7aca8fcca50fa0e6d20d176394019cec3be17ec9c6ba0fdbdbad
# Tue, 09 Feb 2021 03:42:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 09 Feb 2021 03:42:06 GMT
STOPSIGNAL SIGUSR1
# Tue, 09 Feb 2021 03:42:06 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 09 Feb 2021 03:42:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 09 Feb 2021 03:42:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Feb 2021 03:42:07 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:032413a44cf56b097e48b8221bf475ca1bec26e7a27f35fe61d699366a335b79`  
		Last Modified: Tue, 09 Feb 2021 02:45:31 GMT  
		Size: 25.7 MB (25710021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e65f701864562492efa2c0035134b62d68efdb6e7241a0a2dcc3151e6d5775b`  
		Last Modified: Tue, 09 Feb 2021 03:44:28 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c01295dd1240452c26d8aee6d8d60d1a1c4b98bbb528ed57e3e42819e99a8d`  
		Last Modified: Tue, 09 Feb 2021 03:44:59 GMT  
		Size: 8.6 MB (8553262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d37165df9978366350497bd2f7b057b6dc7533fcf646e2a1c14f9bad036b5a`  
		Last Modified: Tue, 09 Feb 2021 03:44:58 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:442f82b39b59911a6ab28a1f2685c2b101e75042800f2a28c7bc3eb70dbf4f55`  
		Last Modified: Tue, 09 Feb 2021 03:44:58 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haproxy:2.1.11`

```console
$ docker pull haproxy@sha256:b15ed53ebe5defe9b1d5c719c5a8473477185d892bd9217b6fdf219680906524
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `haproxy:2.1.11` - linux; amd64

```console
$ docker pull haproxy@sha256:058036aaab4b4372e0cbf4a914b684b6dd6bca4a9b8357ea1d123e1ec29bede4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36154168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97108b00299f21c34d42f1524a60a634c2e00efa7ea720baf71107abb0a0b8b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Mon, 08 Mar 2021 21:37:25 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 21:44:29 GMT
ENV HAPROXY_VERSION=2.1.11
# Mon, 08 Mar 2021 21:44:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.1/src/haproxy-2.1.11.tar.gz
# Mon, 08 Mar 2021 21:44:30 GMT
ENV HAPROXY_SHA256=feff37a5459d7aca8fcca50fa0e6d20d176394019cec3be17ec9c6ba0fdbdbad
# Mon, 08 Mar 2021 21:45:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 08 Mar 2021 21:45:27 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 21:45:27 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 21:45:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 08 Mar 2021 21:45:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 21:45:29 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7bca45a971fe608786870ce75c9976f8e5a958f55e1287a6120048b897c63b6`  
		Last Modified: Mon, 08 Mar 2021 21:52:33 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b04d31d88d6e0c90d4599ecb9cda1dbc54aafa82dd863b8ec9caf196fcf69eb`  
		Last Modified: Mon, 08 Mar 2021 21:54:13 GMT  
		Size: 9.1 MB (9057077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b84dc2397a3e235ab2c545e139ab48c7f400d604ae96e1affb6285edce9112`  
		Last Modified: Mon, 08 Mar 2021 21:54:11 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c51e426666164bda770b6005c8bafd1df5cd8f857bbae74b7cbe0a094158738`  
		Last Modified: Mon, 08 Mar 2021 21:54:11 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.1.11` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:26f3d30aef07184cb201597c8910cc48ba3828d2d706c5c4835c97de505f671d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33343094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94be1557923ed2e99c8d58f36cf17059121d2c50af35302f4fc85f28cce4a719`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:50:10 GMT
ADD file:fbd00ef7871dc27d7ed5fa8c238cdc80652bd87b8033be7de9e54a799bbf10a4 in / 
# Tue, 09 Feb 2021 02:50:11 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:45:24 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 09 Feb 2021 03:49:52 GMT
ENV HAPROXY_VERSION=2.1.11
# Tue, 09 Feb 2021 03:49:53 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.1/src/haproxy-2.1.11.tar.gz
# Tue, 09 Feb 2021 03:49:54 GMT
ENV HAPROXY_SHA256=feff37a5459d7aca8fcca50fa0e6d20d176394019cec3be17ec9c6ba0fdbdbad
# Tue, 09 Feb 2021 03:50:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 09 Feb 2021 03:50:48 GMT
STOPSIGNAL SIGUSR1
# Tue, 09 Feb 2021 03:50:49 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 09 Feb 2021 03:50:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 09 Feb 2021 03:50:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Feb 2021 03:50:53 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:8e683fcc73f4da7d69ce1d5f4e1d77510aa459490068f38db2d8663698b391a0`  
		Last Modified: Tue, 09 Feb 2021 02:59:07 GMT  
		Size: 24.8 MB (24839297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def565d52deae74587a55f60d168bd531ebe8095c594027b7057a8fc1be0e8af`  
		Last Modified: Tue, 09 Feb 2021 03:54:54 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b901b8357320b59dd49f063f6922b16fd20f8ab67b11a840792c2498622b6cc7`  
		Last Modified: Tue, 09 Feb 2021 03:55:32 GMT  
		Size: 8.5 MB (8501855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:566a6e271324efe6d84666edb4303fadfc6fb3610a165e58b42e721275cc3de6`  
		Last Modified: Tue, 09 Feb 2021 03:55:30 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b12f544536b33776045decfb1c352c4df5f286f4eabc8c667eeb21c990c8bd`  
		Last Modified: Tue, 09 Feb 2021 03:55:30 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.1.11` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:7139d6104e3f401f4a46dd88d848b5f27865bd4c42bb8bd96e5e297c84ee70f3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31156536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3852b0d58b81ee4c90beddd66ad4c7b1926696f1dcfb9153b883f549741066a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 03:00:57 GMT
ADD file:e675d50366bde57173a75f9a29367d765e7da2b7254c5254b64e777cf6870502 in / 
# Tue, 09 Feb 2021 03:01:00 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:49:38 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 09 Feb 2021 03:53:23 GMT
ENV HAPROXY_VERSION=2.1.11
# Tue, 09 Feb 2021 03:53:24 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.1/src/haproxy-2.1.11.tar.gz
# Tue, 09 Feb 2021 03:53:26 GMT
ENV HAPROXY_SHA256=feff37a5459d7aca8fcca50fa0e6d20d176394019cec3be17ec9c6ba0fdbdbad
# Tue, 09 Feb 2021 03:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 09 Feb 2021 03:54:12 GMT
STOPSIGNAL SIGUSR1
# Tue, 09 Feb 2021 03:54:13 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 09 Feb 2021 03:54:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 09 Feb 2021 03:54:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Feb 2021 03:54:19 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:db574d82360c3b60abadbef4f3daf8dee01f24741fc6ab3692aa543558d8b624`  
		Last Modified: Tue, 09 Feb 2021 03:09:46 GMT  
		Size: 22.7 MB (22703384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9978ebb1881387f11e025fb46dce2b3c715f705f6d240737574f8848c27fa0d7`  
		Last Modified: Tue, 09 Feb 2021 03:58:16 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bcb1b2473bdb76e258f75a463bb5e432005cc44a6fdefa0689128dfb747cce7`  
		Last Modified: Tue, 09 Feb 2021 03:58:55 GMT  
		Size: 8.5 MB (8451207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc84cf69cc9d486b9de9a8df58e30461e02dc671868478ca12cbb001589ff077`  
		Last Modified: Tue, 09 Feb 2021 03:58:52 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ab3f670e0d98cda8512cfb573f7fe22d728ff4a97ee08fa4e524ecaa82106a`  
		Last Modified: Tue, 09 Feb 2021 03:58:52 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.1.11` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:ef132befede302d23ace72d693c00b429ab16ebbb873b68acc4b23e443ba51ca
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34713983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31f6a7ef05bf3dae3334f2fd2c62781f0068525af801e3c215cf32f7cedd41a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:41:10 GMT
ADD file:d906dedaf14d8e3874b46787f7a1dbf268bc124c4e1dd32f13f3079e12f22238 in / 
# Tue, 09 Feb 2021 02:41:13 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:59:41 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 09 Feb 2021 04:03:41 GMT
ENV HAPROXY_VERSION=2.1.11
# Tue, 09 Feb 2021 04:03:42 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.1/src/haproxy-2.1.11.tar.gz
# Tue, 09 Feb 2021 04:03:44 GMT
ENV HAPROXY_SHA256=feff37a5459d7aca8fcca50fa0e6d20d176394019cec3be17ec9c6ba0fdbdbad
# Tue, 09 Feb 2021 04:04:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 09 Feb 2021 04:04:31 GMT
STOPSIGNAL SIGUSR1
# Tue, 09 Feb 2021 04:04:32 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 09 Feb 2021 04:04:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 09 Feb 2021 04:04:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Feb 2021 04:04:35 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:83c5cfdaa5385ea6fc4d31e724fd4dc5d74de847a7bdd968555b8f2c558dac0e`  
		Last Modified: Tue, 09 Feb 2021 02:47:27 GMT  
		Size: 25.9 MB (25851449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b7f43dd52365bce2c2b75f29577aa39d2b5794e2561cddc0678422ffc1f7d15`  
		Last Modified: Tue, 09 Feb 2021 04:08:36 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d84fe349f988c1566dcd75b8e50704040f9f5f022501d22271ac88b703075b0d`  
		Last Modified: Tue, 09 Feb 2021 04:09:15 GMT  
		Size: 8.9 MB (8860589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08436cd1d3b23ec9b417fa7e21536bfd0a8c04ddb529ad5ba9cd4746db953000`  
		Last Modified: Tue, 09 Feb 2021 04:09:12 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e90c5be53b8aac6be1540c928e1229848f339c435f23a2b4c32675055a2042d`  
		Last Modified: Tue, 09 Feb 2021 04:09:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.1.11` - linux; 386

```console
$ docker pull haproxy@sha256:0a9bd9a8d59f9a79710c7c477f1226b6260f0462f2615e0b76d89df2f650db9e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 MB (36565407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8afbb14bb10e86b5cdbcbc5c696f346ff0e849f5ce45af24768e3f8f99c92477`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:39:47 GMT
ADD file:61c31b1037672781ed0ecbc080ee3d49c83af49f5578b011544513fa9625698d in / 
# Tue, 09 Feb 2021 02:39:47 GMT
CMD ["bash"]
# Mon, 08 Mar 2021 22:02:40 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 22:09:35 GMT
ENV HAPROXY_VERSION=2.1.11
# Mon, 08 Mar 2021 22:09:35 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.1/src/haproxy-2.1.11.tar.gz
# Mon, 08 Mar 2021 22:09:36 GMT
ENV HAPROXY_SHA256=feff37a5459d7aca8fcca50fa0e6d20d176394019cec3be17ec9c6ba0fdbdbad
# Mon, 08 Mar 2021 22:10:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 08 Mar 2021 22:10:23 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 22:10:23 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 22:10:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 08 Mar 2021 22:10:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 22:10:24 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:27cbb00346a16ea900c1049a2e5b47942c586c377179e098382c8ca1c8e87966`  
		Last Modified: Tue, 09 Feb 2021 02:45:51 GMT  
		Size: 27.8 MB (27752731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b6129a97a33727ea8a598d1e797bccce491920bf29d769880cf2fc6d3e0436`  
		Last Modified: Mon, 08 Mar 2021 22:17:48 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7b31d0097aeefea7422dea4783723139cdfd025d373e858a39e4fb95f1f7c01`  
		Last Modified: Mon, 08 Mar 2021 22:19:22 GMT  
		Size: 8.8 MB (8810733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f10d72141d055778e8b7118ca07e30eaf4e07fbb0ed781d176d5ce823fa1e5c0`  
		Last Modified: Mon, 08 Mar 2021 22:19:20 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16f30853317863b120654aab5803d2ffb8ccd75d3b0d2242401db244157cc458`  
		Last Modified: Mon, 08 Mar 2021 22:19:20 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.1.11` - linux; mips64le

```console
$ docker pull haproxy@sha256:3e78da0c9d0f2ea8febf75b34d66e9619a6219c8abbfc9671185293e6125cfa4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 MB (34224406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bfd9376d31463612782d09216e96923106291708f3bd686c7a3ad4000dda001`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 03:09:26 GMT
ADD file:0222a151f4e5033d9eae98ce2b703a63f52d049dd72ac40bdd0dc2dafe619f0a in / 
# Tue, 09 Feb 2021 03:09:27 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:41:09 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 09 Feb 2021 03:49:11 GMT
ENV HAPROXY_VERSION=2.1.11
# Tue, 09 Feb 2021 03:49:12 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.1/src/haproxy-2.1.11.tar.gz
# Tue, 09 Feb 2021 03:49:12 GMT
ENV HAPROXY_SHA256=feff37a5459d7aca8fcca50fa0e6d20d176394019cec3be17ec9c6ba0fdbdbad
# Tue, 09 Feb 2021 03:51:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 09 Feb 2021 03:51:24 GMT
STOPSIGNAL SIGUSR1
# Tue, 09 Feb 2021 03:51:24 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 09 Feb 2021 03:51:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 09 Feb 2021 03:51:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Feb 2021 03:51:26 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:dfb81134097d874e01b495d1fba82e384056d0a3a45f01a69a2e86ae82af1e96`  
		Last Modified: Tue, 09 Feb 2021 03:15:55 GMT  
		Size: 25.8 MB (25764640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a549d56662447dd8cb15faf59ca0fc2eda7a877e9aee16aadd09fd46e4214a`  
		Last Modified: Tue, 09 Feb 2021 03:57:56 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9d53512fc5751fa60369bcb6c8c9bafb34cf3b5616ce67d8409bcffaa0b216c`  
		Last Modified: Tue, 09 Feb 2021 03:58:59 GMT  
		Size: 8.5 MB (8457816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32a5ae3fa74e543af85b70b61154a9a6313f75530877683daf062ef7b8632d36`  
		Last Modified: Tue, 09 Feb 2021 03:58:52 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f52283468e8de4724ac1b6f0199e12907e8cdf9ca893f588c1d454847e11feec`  
		Last Modified: Tue, 09 Feb 2021 03:58:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.1.11` - linux; ppc64le

```console
$ docker pull haproxy@sha256:dd5e46016691fc71840fc0400fb94617e39c49f45c3ff78cedf550988665b752
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39820097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107863456d835cb525fb772a5c0e28e8f2910f312e057b1380937dafe10b5c5a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:19:19 GMT
ADD file:9a8cfdf0eab394a693b5cde0700ad47b6e8506ef0b79fabb8a07874b96e6c394 in / 
# Tue, 09 Feb 2021 02:19:34 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 05:52:23 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 09 Feb 2021 06:11:36 GMT
ENV HAPROXY_VERSION=2.1.11
# Tue, 09 Feb 2021 06:11:48 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.1/src/haproxy-2.1.11.tar.gz
# Tue, 09 Feb 2021 06:11:57 GMT
ENV HAPROXY_SHA256=feff37a5459d7aca8fcca50fa0e6d20d176394019cec3be17ec9c6ba0fdbdbad
# Tue, 09 Feb 2021 06:16:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 09 Feb 2021 06:16:17 GMT
STOPSIGNAL SIGUSR1
# Tue, 09 Feb 2021 06:16:19 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 09 Feb 2021 06:16:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 09 Feb 2021 06:16:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Feb 2021 06:16:44 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:9996b4fb6bc1c50f95ba30f8988c9c89526556fa320d3fda59d3d8359f7810d6`  
		Last Modified: Tue, 09 Feb 2021 02:27:59 GMT  
		Size: 30.5 MB (30519509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7f600bc4989eb9f12d5006a73f5958eb4fe85f86bc4008d7a899bb935b0f1c`  
		Last Modified: Tue, 09 Feb 2021 06:38:36 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a959a5a513b4378da0a41c518deec7e5adf652eb1f48393785fe90b50fbd9ad`  
		Last Modified: Tue, 09 Feb 2021 06:39:23 GMT  
		Size: 9.3 MB (9298641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f96fc9d1b9d1da7faa15e5e3347d6b04cab67039937dbf04210037aee2fc1add`  
		Last Modified: Tue, 09 Feb 2021 06:39:23 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:229c9ec499471cf6a59cf55fd4341ea8bf993ec1e8f8fa909739a65d21a74c7a`  
		Last Modified: Tue, 09 Feb 2021 06:39:21 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.1.11` - linux; s390x

```console
$ docker pull haproxy@sha256:94e335f859a33da8c30ff8d118e391de396b87623f2959052b0779495be24178
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34265227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72291b86a2d7c33c2201cfe944eabe11323a4fc62ccdcd43b367e780c0584572`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:42:10 GMT
ADD file:0edb2de05df54191a141bd125f59d7e14eef0cc4576927a247b8dd7d6f255d04 in / 
# Tue, 09 Feb 2021 02:42:12 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:39:30 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 09 Feb 2021 03:41:38 GMT
ENV HAPROXY_VERSION=2.1.11
# Tue, 09 Feb 2021 03:41:39 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.1/src/haproxy-2.1.11.tar.gz
# Tue, 09 Feb 2021 03:41:39 GMT
ENV HAPROXY_SHA256=feff37a5459d7aca8fcca50fa0e6d20d176394019cec3be17ec9c6ba0fdbdbad
# Tue, 09 Feb 2021 03:42:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 09 Feb 2021 03:42:06 GMT
STOPSIGNAL SIGUSR1
# Tue, 09 Feb 2021 03:42:06 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 09 Feb 2021 03:42:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 09 Feb 2021 03:42:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Feb 2021 03:42:07 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:032413a44cf56b097e48b8221bf475ca1bec26e7a27f35fe61d699366a335b79`  
		Last Modified: Tue, 09 Feb 2021 02:45:31 GMT  
		Size: 25.7 MB (25710021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e65f701864562492efa2c0035134b62d68efdb6e7241a0a2dcc3151e6d5775b`  
		Last Modified: Tue, 09 Feb 2021 03:44:28 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c01295dd1240452c26d8aee6d8d60d1a1c4b98bbb528ed57e3e42819e99a8d`  
		Last Modified: Tue, 09 Feb 2021 03:44:59 GMT  
		Size: 8.6 MB (8553262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d37165df9978366350497bd2f7b057b6dc7533fcf646e2a1c14f9bad036b5a`  
		Last Modified: Tue, 09 Feb 2021 03:44:58 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:442f82b39b59911a6ab28a1f2685c2b101e75042800f2a28c7bc3eb70dbf4f55`  
		Last Modified: Tue, 09 Feb 2021 03:44:58 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haproxy:2.1.11-alpine`

```console
$ docker pull haproxy@sha256:3ddd3e45db0a0097f7803819a319d288585c43d587313fe33ad4b5b953be1297
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `haproxy:2.1.11-alpine` - linux; amd64

```console
$ docker pull haproxy@sha256:54f4f139caca0e0214634b2f0923c452055a34112e736b3cbb6a56b19317ac3b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8933206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:938b4b295c0d164d017d190d8d5b9fc77610de8e0bca3df6a89fe47fb4aaa4f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 21:19:54 GMT
ADD file:80bf8bd014071345b1c0364eeb0a5e48f3fb0d87f9c31cb990e57caa652b59b8 in / 
# Wed, 17 Feb 2021 21:19:54 GMT
CMD ["/bin/sh"]
# Mon, 08 Mar 2021 21:38:26 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 21:45:41 GMT
ENV HAPROXY_VERSION=2.1.11
# Mon, 08 Mar 2021 21:45:41 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.1/src/haproxy-2.1.11.tar.gz
# Mon, 08 Mar 2021 21:45:41 GMT
ENV HAPROXY_SHA256=feff37a5459d7aca8fcca50fa0e6d20d176394019cec3be17ec9c6ba0fdbdbad
# Mon, 08 Mar 2021 21:46:51 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Mon, 08 Mar 2021 21:46:51 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 21:46:51 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 21:46:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 08 Mar 2021 21:46:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 21:46:52 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:ba3557a56b150f9b813f9d02274d62914fd8fce120dd374d9ee17b87cf1d277d`  
		Last Modified: Wed, 17 Feb 2021 21:20:25 GMT  
		Size: 2.8 MB (2811657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9216237f12c4d44ab183590086cf2a09004b5609c4b50871d88658faa495245`  
		Last Modified: Mon, 08 Mar 2021 21:52:45 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0375e826cc0f268b074b9f39d6e7f8d1fe209f40f782b80b077faf6dd969d3d`  
		Last Modified: Mon, 08 Mar 2021 21:54:25 GMT  
		Size: 6.1 MB (6119791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e41b41243f575e115d2b3bb5ef839a965ce80de8ff7a00f544bd434cfec86c7d`  
		Last Modified: Mon, 08 Mar 2021 21:54:23 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eef7db5ef86d2d008e3e59ece5a5c062d3e0a04d2106d57aca15ab171f515c5`  
		Last Modified: Mon, 08 Mar 2021 21:54:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.1.11-alpine` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:2648e08a0fbba1cd1fe3837b3464cfd75af74c7d9cc7efdb3af8eb63ace33194
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8581091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd4c9efdd148f0a4c471af22576514cdc265a5b37a2a94d5b1fdfb2508b54379`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 20:49:32 GMT
ADD file:c04fbd3b039001c592cfa14f8388f8934ed4223ccf274dbb926e75039e172af4 in / 
# Wed, 17 Feb 2021 20:49:33 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 21:08:27 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 17 Feb 2021 21:10:20 GMT
ENV HAPROXY_VERSION=2.1.11
# Wed, 17 Feb 2021 21:10:21 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.1/src/haproxy-2.1.11.tar.gz
# Wed, 17 Feb 2021 21:10:21 GMT
ENV HAPROXY_SHA256=feff37a5459d7aca8fcca50fa0e6d20d176394019cec3be17ec9c6ba0fdbdbad
# Wed, 17 Feb 2021 21:10:45 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 17 Feb 2021 21:10:45 GMT
STOPSIGNAL SIGUSR1
# Wed, 17 Feb 2021 21:10:46 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 17 Feb 2021 21:10:48 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 17 Feb 2021 21:10:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Feb 2021 21:10:49 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:1353527ebe111f9bb1e271264a3c182e909e4b36463f80d7dbde1be0713eb892`  
		Last Modified: Wed, 17 Feb 2021 20:50:06 GMT  
		Size: 2.6 MB (2622039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d174378d3ee2c0c6e6a85b5228f929557826d80bcd23b2434093942f499361a7`  
		Last Modified: Wed, 17 Feb 2021 21:12:31 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5da04b7a6d6583259ff32e3bad15cd83bd5ea15ebd70f31b20c57b90b1629a9f`  
		Last Modified: Wed, 17 Feb 2021 21:13:04 GMT  
		Size: 6.0 MB (5957295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e93a869720ef31585e613eda53f4ec88f26ba08308a2931a49d4e74ce85188a`  
		Last Modified: Wed, 17 Feb 2021 21:13:01 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba5a64c7b537fdd84478db65d6924e5c1559a7b1e38b43555b7a6d0a8fe8206`  
		Last Modified: Wed, 17 Feb 2021 21:13:01 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.1.11-alpine` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:30318a216776a6336e3d3061e6a6558af989b070ac2dea5053255588b70862be
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8367841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c62f30f5d43773b604254fa308b9a50b313f4849cd26c36a0a41f8495d716523`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 20:57:36 GMT
ADD file:efdd39e5243eaf378f12ad5a85d2222b44930850a90263e5f17e8a6b5e9bc9b8 in / 
# Wed, 17 Feb 2021 20:57:37 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 21:49:42 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 17 Feb 2021 21:52:06 GMT
ENV HAPROXY_VERSION=2.1.11
# Wed, 17 Feb 2021 21:52:07 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.1/src/haproxy-2.1.11.tar.gz
# Wed, 17 Feb 2021 21:52:08 GMT
ENV HAPROXY_SHA256=feff37a5459d7aca8fcca50fa0e6d20d176394019cec3be17ec9c6ba0fdbdbad
# Wed, 17 Feb 2021 21:52:40 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 17 Feb 2021 21:52:41 GMT
STOPSIGNAL SIGUSR1
# Wed, 17 Feb 2021 21:52:42 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 17 Feb 2021 21:52:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 17 Feb 2021 21:52:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Feb 2021 21:52:46 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f55b840e27d3dbe27e44497103a4397f043749f933eb0433d29e2f104b3435ef`  
		Last Modified: Wed, 17 Feb 2021 20:58:14 GMT  
		Size: 2.4 MB (2423892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86398e5ccaeed703d9464d57f2d97546fad0481312144292414eb1cf857b617f`  
		Last Modified: Wed, 17 Feb 2021 21:55:00 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa7e5e366fb490acfe619d44f8824f03676fa5ae7add095ae9fe6dcf6c784203`  
		Last Modified: Wed, 17 Feb 2021 21:55:35 GMT  
		Size: 5.9 MB (5942191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5589321216c528ab0e51d4ccd689ee84ddfccf9148f240bb68e66d4d9bcbe50a`  
		Last Modified: Wed, 17 Feb 2021 21:55:34 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83ed65258fa74330ab0d0d556f444bd4c7855360fe8fd03ab53c84b5ca1b0f1c`  
		Last Modified: Wed, 17 Feb 2021 21:55:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.1.11-alpine` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:b12821cea2f1f64aa02cf3680aa2e06d4c7acecefb836efa93b0b90cb82a6bc0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8819528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8922951cf529735b0b107a3182447b86bad0f297693ef2a726cf3027fa22f2e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 20:39:29 GMT
ADD file:3bf1497bd250cf7c73c12231dc4ebe3a3a67f2cd99e35bce47ef6674683aeb1d in / 
# Wed, 17 Feb 2021 20:39:30 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 21:36:08 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 17 Feb 2021 21:38:22 GMT
ENV HAPROXY_VERSION=2.1.11
# Wed, 17 Feb 2021 21:38:22 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.1/src/haproxy-2.1.11.tar.gz
# Wed, 17 Feb 2021 21:38:23 GMT
ENV HAPROXY_SHA256=feff37a5459d7aca8fcca50fa0e6d20d176394019cec3be17ec9c6ba0fdbdbad
# Wed, 17 Feb 2021 21:38:49 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 17 Feb 2021 21:38:50 GMT
STOPSIGNAL SIGUSR1
# Wed, 17 Feb 2021 21:38:51 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 17 Feb 2021 21:38:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 17 Feb 2021 21:38:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Feb 2021 21:38:54 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:069a56d6d07f6b186fbb82e4486616b9be9a37ce32a63013af6cddcb65898182`  
		Last Modified: Wed, 17 Feb 2021 20:40:04 GMT  
		Size: 2.7 MB (2711572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6644620fa9074da825714fc7794756e2b0e36f3e83ffc2bc01bbc9df0de9e373`  
		Last Modified: Wed, 17 Feb 2021 21:41:18 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70960d78a7306a10cf2d19c585ed5ecfa45c95fe04574d5662af5cedbdb06b3c`  
		Last Modified: Wed, 17 Feb 2021 21:41:50 GMT  
		Size: 6.1 MB (6106200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43b19c712d1bc12faf13fb45d892deb65f0fdf0543fadc7d1946cfeb67d2f731`  
		Last Modified: Wed, 17 Feb 2021 21:41:48 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40be9b81257342c97b3262e38cd188a31cb675aa32c39803233c81b1bcb24ab7`  
		Last Modified: Wed, 17 Feb 2021 21:41:48 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.1.11-alpine` - linux; 386

```console
$ docker pull haproxy@sha256:51857f9377f919b420c5e3332dc0d5eb654e6fcbf961b15df242c56edf3f71d2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8775034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fe6fabb603741fda7df51d1b882b94ae3a2cb67838cdc94e6f051505249c234`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 21:38:34 GMT
ADD file:eaee53da3c87749799de55809e4a5b526c56855332b961a85b1184c660f1d65b in / 
# Wed, 17 Feb 2021 21:38:35 GMT
CMD ["/bin/sh"]
# Mon, 08 Mar 2021 22:03:53 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 22:10:37 GMT
ENV HAPROXY_VERSION=2.1.11
# Mon, 08 Mar 2021 22:10:37 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.1/src/haproxy-2.1.11.tar.gz
# Mon, 08 Mar 2021 22:10:37 GMT
ENV HAPROXY_SHA256=feff37a5459d7aca8fcca50fa0e6d20d176394019cec3be17ec9c6ba0fdbdbad
# Mon, 08 Mar 2021 22:11:34 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Mon, 08 Mar 2021 22:11:35 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 22:11:35 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 22:11:36 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 08 Mar 2021 22:11:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 22:11:36 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:86205afa28f6bc624469015a543d16608258d2828411a92c662f4fdc6d276e18`  
		Last Modified: Wed, 17 Feb 2021 21:39:07 GMT  
		Size: 2.8 MB (2818177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080e85d941540171ac6a020af17b393f2a40b03d40b9677d708d31ffb6e31b71`  
		Last Modified: Mon, 08 Mar 2021 22:18:02 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e96737cecba53e0f8308c50a80768c0c8f74f7a9fa01fa505fe24db3c7a0ea4`  
		Last Modified: Mon, 08 Mar 2021 22:19:35 GMT  
		Size: 6.0 MB (5955104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:748fb4aaa27ecdcf8ccf477164e33f6d50604dafad14151201e99b3ee584f34a`  
		Last Modified: Mon, 08 Mar 2021 22:19:33 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4212c42ea7a921ba219a40fecb5c4f113eb86018c4c534e0cbf80aca77556e99`  
		Last Modified: Mon, 08 Mar 2021 22:19:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.1.11-alpine` - linux; ppc64le

```console
$ docker pull haproxy@sha256:7a107a9dc2dc3659e27f38ed042e0b283028834dc3952dd62091db239d7cef18
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9147063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f76dd8d9f35883a5fa03083252f6d7897ab03dc489a1e8119322fcac1554f92`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 21:17:29 GMT
ADD file:28f4377c61c0f8eb43a6b36e6a24ef5893f51d405d25b62e364988223537ae0b in / 
# Wed, 17 Feb 2021 21:17:37 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 22:10:46 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 17 Feb 2021 22:16:21 GMT
ENV HAPROXY_VERSION=2.1.11
# Wed, 17 Feb 2021 22:16:27 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.1/src/haproxy-2.1.11.tar.gz
# Wed, 17 Feb 2021 22:16:36 GMT
ENV HAPROXY_SHA256=feff37a5459d7aca8fcca50fa0e6d20d176394019cec3be17ec9c6ba0fdbdbad
# Wed, 17 Feb 2021 22:17:26 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 17 Feb 2021 22:17:34 GMT
STOPSIGNAL SIGUSR1
# Wed, 17 Feb 2021 22:17:36 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 17 Feb 2021 22:17:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 17 Feb 2021 22:18:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Feb 2021 22:18:14 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:cb672e0375a8f9bb3d33049ceb372ffa49b959bfc84fe6f72bfb97b682a608c8`  
		Last Modified: Wed, 17 Feb 2021 21:18:10 GMT  
		Size: 2.8 MB (2813081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f391a7d74b9bf5c2089e7957996d00d99ddc33d8295873bf28746716bb728a`  
		Last Modified: Wed, 17 Feb 2021 22:23:02 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dd03b44fedcdc44a51845776153a51eec69658c78b31ebbb7d4c9c5d9477441`  
		Last Modified: Wed, 17 Feb 2021 22:23:45 GMT  
		Size: 6.3 MB (6332218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccdce88ca5d3907cbb768fbaa27a821148e3ca73e1c87154542b072db235a712`  
		Last Modified: Wed, 17 Feb 2021 22:23:44 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d12b27836fb8ec99d79da07994133a4e40e88ca4441a058068445e6378b1976`  
		Last Modified: Wed, 17 Feb 2021 22:23:44 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.1.11-alpine` - linux; s390x

```console
$ docker pull haproxy@sha256:0c1210dfa3b0b8f0993215d25c9cf774efd5440cee85c30ba0fceda96d8c38ba
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8642859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b36c79ab0c8179ef5fcf9c459fb7674d3b786a7f137de663e78a6a03ba4327ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 20:41:27 GMT
ADD file:630c66f8d774d75b51e32aff812b438d377ebd3389c4aa6c324fdf8c03b6fa13 in / 
# Wed, 17 Feb 2021 20:41:27 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 21:33:33 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 17 Feb 2021 21:38:35 GMT
ENV HAPROXY_VERSION=2.1.11
# Wed, 17 Feb 2021 21:38:36 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.1/src/haproxy-2.1.11.tar.gz
# Wed, 17 Feb 2021 21:38:36 GMT
ENV HAPROXY_SHA256=feff37a5459d7aca8fcca50fa0e6d20d176394019cec3be17ec9c6ba0fdbdbad
# Wed, 17 Feb 2021 21:39:57 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 17 Feb 2021 21:39:59 GMT
STOPSIGNAL SIGUSR1
# Wed, 17 Feb 2021 21:39:59 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 17 Feb 2021 21:40:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 17 Feb 2021 21:40:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Feb 2021 21:40:03 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:ff5e8cb87555e9fa38a441f5cf0414e91353e2cd21cdb48d48b7de5bb39ce674`  
		Last Modified: Wed, 17 Feb 2021 20:41:58 GMT  
		Size: 2.6 MB (2602381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de25a3a0de168e6603cb978691ef3e7f11d7c9108d0ade38d3185d5d9dbdc094`  
		Last Modified: Wed, 17 Feb 2021 21:43:59 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a554ce42cf66fc32c16bbfbb6921589b11fd7a72eb4ef898b5c1fcc80c9c2d90`  
		Last Modified: Wed, 17 Feb 2021 21:44:30 GMT  
		Size: 6.0 MB (6038721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7db60cb31eaf76ee07470ae89b216f50876da7320605702196c77051d95bd61`  
		Last Modified: Wed, 17 Feb 2021 21:44:29 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c8d64fd3df5379cb79e77425280f5e7387a78b0423fc679d88bc09a6df53ac`  
		Last Modified: Wed, 17 Feb 2021 21:44:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haproxy:2.1-alpine`

```console
$ docker pull haproxy@sha256:3ddd3e45db0a0097f7803819a319d288585c43d587313fe33ad4b5b953be1297
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `haproxy:2.1-alpine` - linux; amd64

```console
$ docker pull haproxy@sha256:54f4f139caca0e0214634b2f0923c452055a34112e736b3cbb6a56b19317ac3b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8933206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:938b4b295c0d164d017d190d8d5b9fc77610de8e0bca3df6a89fe47fb4aaa4f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 21:19:54 GMT
ADD file:80bf8bd014071345b1c0364eeb0a5e48f3fb0d87f9c31cb990e57caa652b59b8 in / 
# Wed, 17 Feb 2021 21:19:54 GMT
CMD ["/bin/sh"]
# Mon, 08 Mar 2021 21:38:26 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 21:45:41 GMT
ENV HAPROXY_VERSION=2.1.11
# Mon, 08 Mar 2021 21:45:41 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.1/src/haproxy-2.1.11.tar.gz
# Mon, 08 Mar 2021 21:45:41 GMT
ENV HAPROXY_SHA256=feff37a5459d7aca8fcca50fa0e6d20d176394019cec3be17ec9c6ba0fdbdbad
# Mon, 08 Mar 2021 21:46:51 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Mon, 08 Mar 2021 21:46:51 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 21:46:51 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 21:46:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 08 Mar 2021 21:46:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 21:46:52 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:ba3557a56b150f9b813f9d02274d62914fd8fce120dd374d9ee17b87cf1d277d`  
		Last Modified: Wed, 17 Feb 2021 21:20:25 GMT  
		Size: 2.8 MB (2811657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9216237f12c4d44ab183590086cf2a09004b5609c4b50871d88658faa495245`  
		Last Modified: Mon, 08 Mar 2021 21:52:45 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0375e826cc0f268b074b9f39d6e7f8d1fe209f40f782b80b077faf6dd969d3d`  
		Last Modified: Mon, 08 Mar 2021 21:54:25 GMT  
		Size: 6.1 MB (6119791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e41b41243f575e115d2b3bb5ef839a965ce80de8ff7a00f544bd434cfec86c7d`  
		Last Modified: Mon, 08 Mar 2021 21:54:23 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eef7db5ef86d2d008e3e59ece5a5c062d3e0a04d2106d57aca15ab171f515c5`  
		Last Modified: Mon, 08 Mar 2021 21:54:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.1-alpine` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:2648e08a0fbba1cd1fe3837b3464cfd75af74c7d9cc7efdb3af8eb63ace33194
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8581091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd4c9efdd148f0a4c471af22576514cdc265a5b37a2a94d5b1fdfb2508b54379`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 20:49:32 GMT
ADD file:c04fbd3b039001c592cfa14f8388f8934ed4223ccf274dbb926e75039e172af4 in / 
# Wed, 17 Feb 2021 20:49:33 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 21:08:27 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 17 Feb 2021 21:10:20 GMT
ENV HAPROXY_VERSION=2.1.11
# Wed, 17 Feb 2021 21:10:21 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.1/src/haproxy-2.1.11.tar.gz
# Wed, 17 Feb 2021 21:10:21 GMT
ENV HAPROXY_SHA256=feff37a5459d7aca8fcca50fa0e6d20d176394019cec3be17ec9c6ba0fdbdbad
# Wed, 17 Feb 2021 21:10:45 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 17 Feb 2021 21:10:45 GMT
STOPSIGNAL SIGUSR1
# Wed, 17 Feb 2021 21:10:46 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 17 Feb 2021 21:10:48 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 17 Feb 2021 21:10:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Feb 2021 21:10:49 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:1353527ebe111f9bb1e271264a3c182e909e4b36463f80d7dbde1be0713eb892`  
		Last Modified: Wed, 17 Feb 2021 20:50:06 GMT  
		Size: 2.6 MB (2622039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d174378d3ee2c0c6e6a85b5228f929557826d80bcd23b2434093942f499361a7`  
		Last Modified: Wed, 17 Feb 2021 21:12:31 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5da04b7a6d6583259ff32e3bad15cd83bd5ea15ebd70f31b20c57b90b1629a9f`  
		Last Modified: Wed, 17 Feb 2021 21:13:04 GMT  
		Size: 6.0 MB (5957295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e93a869720ef31585e613eda53f4ec88f26ba08308a2931a49d4e74ce85188a`  
		Last Modified: Wed, 17 Feb 2021 21:13:01 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba5a64c7b537fdd84478db65d6924e5c1559a7b1e38b43555b7a6d0a8fe8206`  
		Last Modified: Wed, 17 Feb 2021 21:13:01 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.1-alpine` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:30318a216776a6336e3d3061e6a6558af989b070ac2dea5053255588b70862be
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8367841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c62f30f5d43773b604254fa308b9a50b313f4849cd26c36a0a41f8495d716523`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 20:57:36 GMT
ADD file:efdd39e5243eaf378f12ad5a85d2222b44930850a90263e5f17e8a6b5e9bc9b8 in / 
# Wed, 17 Feb 2021 20:57:37 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 21:49:42 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 17 Feb 2021 21:52:06 GMT
ENV HAPROXY_VERSION=2.1.11
# Wed, 17 Feb 2021 21:52:07 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.1/src/haproxy-2.1.11.tar.gz
# Wed, 17 Feb 2021 21:52:08 GMT
ENV HAPROXY_SHA256=feff37a5459d7aca8fcca50fa0e6d20d176394019cec3be17ec9c6ba0fdbdbad
# Wed, 17 Feb 2021 21:52:40 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 17 Feb 2021 21:52:41 GMT
STOPSIGNAL SIGUSR1
# Wed, 17 Feb 2021 21:52:42 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 17 Feb 2021 21:52:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 17 Feb 2021 21:52:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Feb 2021 21:52:46 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f55b840e27d3dbe27e44497103a4397f043749f933eb0433d29e2f104b3435ef`  
		Last Modified: Wed, 17 Feb 2021 20:58:14 GMT  
		Size: 2.4 MB (2423892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86398e5ccaeed703d9464d57f2d97546fad0481312144292414eb1cf857b617f`  
		Last Modified: Wed, 17 Feb 2021 21:55:00 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa7e5e366fb490acfe619d44f8824f03676fa5ae7add095ae9fe6dcf6c784203`  
		Last Modified: Wed, 17 Feb 2021 21:55:35 GMT  
		Size: 5.9 MB (5942191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5589321216c528ab0e51d4ccd689ee84ddfccf9148f240bb68e66d4d9bcbe50a`  
		Last Modified: Wed, 17 Feb 2021 21:55:34 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83ed65258fa74330ab0d0d556f444bd4c7855360fe8fd03ab53c84b5ca1b0f1c`  
		Last Modified: Wed, 17 Feb 2021 21:55:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.1-alpine` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:b12821cea2f1f64aa02cf3680aa2e06d4c7acecefb836efa93b0b90cb82a6bc0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8819528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8922951cf529735b0b107a3182447b86bad0f297693ef2a726cf3027fa22f2e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 20:39:29 GMT
ADD file:3bf1497bd250cf7c73c12231dc4ebe3a3a67f2cd99e35bce47ef6674683aeb1d in / 
# Wed, 17 Feb 2021 20:39:30 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 21:36:08 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 17 Feb 2021 21:38:22 GMT
ENV HAPROXY_VERSION=2.1.11
# Wed, 17 Feb 2021 21:38:22 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.1/src/haproxy-2.1.11.tar.gz
# Wed, 17 Feb 2021 21:38:23 GMT
ENV HAPROXY_SHA256=feff37a5459d7aca8fcca50fa0e6d20d176394019cec3be17ec9c6ba0fdbdbad
# Wed, 17 Feb 2021 21:38:49 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 17 Feb 2021 21:38:50 GMT
STOPSIGNAL SIGUSR1
# Wed, 17 Feb 2021 21:38:51 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 17 Feb 2021 21:38:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 17 Feb 2021 21:38:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Feb 2021 21:38:54 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:069a56d6d07f6b186fbb82e4486616b9be9a37ce32a63013af6cddcb65898182`  
		Last Modified: Wed, 17 Feb 2021 20:40:04 GMT  
		Size: 2.7 MB (2711572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6644620fa9074da825714fc7794756e2b0e36f3e83ffc2bc01bbc9df0de9e373`  
		Last Modified: Wed, 17 Feb 2021 21:41:18 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70960d78a7306a10cf2d19c585ed5ecfa45c95fe04574d5662af5cedbdb06b3c`  
		Last Modified: Wed, 17 Feb 2021 21:41:50 GMT  
		Size: 6.1 MB (6106200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43b19c712d1bc12faf13fb45d892deb65f0fdf0543fadc7d1946cfeb67d2f731`  
		Last Modified: Wed, 17 Feb 2021 21:41:48 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40be9b81257342c97b3262e38cd188a31cb675aa32c39803233c81b1bcb24ab7`  
		Last Modified: Wed, 17 Feb 2021 21:41:48 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.1-alpine` - linux; 386

```console
$ docker pull haproxy@sha256:51857f9377f919b420c5e3332dc0d5eb654e6fcbf961b15df242c56edf3f71d2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8775034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fe6fabb603741fda7df51d1b882b94ae3a2cb67838cdc94e6f051505249c234`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 21:38:34 GMT
ADD file:eaee53da3c87749799de55809e4a5b526c56855332b961a85b1184c660f1d65b in / 
# Wed, 17 Feb 2021 21:38:35 GMT
CMD ["/bin/sh"]
# Mon, 08 Mar 2021 22:03:53 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 22:10:37 GMT
ENV HAPROXY_VERSION=2.1.11
# Mon, 08 Mar 2021 22:10:37 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.1/src/haproxy-2.1.11.tar.gz
# Mon, 08 Mar 2021 22:10:37 GMT
ENV HAPROXY_SHA256=feff37a5459d7aca8fcca50fa0e6d20d176394019cec3be17ec9c6ba0fdbdbad
# Mon, 08 Mar 2021 22:11:34 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Mon, 08 Mar 2021 22:11:35 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 22:11:35 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 22:11:36 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 08 Mar 2021 22:11:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 22:11:36 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:86205afa28f6bc624469015a543d16608258d2828411a92c662f4fdc6d276e18`  
		Last Modified: Wed, 17 Feb 2021 21:39:07 GMT  
		Size: 2.8 MB (2818177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080e85d941540171ac6a020af17b393f2a40b03d40b9677d708d31ffb6e31b71`  
		Last Modified: Mon, 08 Mar 2021 22:18:02 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e96737cecba53e0f8308c50a80768c0c8f74f7a9fa01fa505fe24db3c7a0ea4`  
		Last Modified: Mon, 08 Mar 2021 22:19:35 GMT  
		Size: 6.0 MB (5955104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:748fb4aaa27ecdcf8ccf477164e33f6d50604dafad14151201e99b3ee584f34a`  
		Last Modified: Mon, 08 Mar 2021 22:19:33 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4212c42ea7a921ba219a40fecb5c4f113eb86018c4c534e0cbf80aca77556e99`  
		Last Modified: Mon, 08 Mar 2021 22:19:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.1-alpine` - linux; ppc64le

```console
$ docker pull haproxy@sha256:7a107a9dc2dc3659e27f38ed042e0b283028834dc3952dd62091db239d7cef18
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9147063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f76dd8d9f35883a5fa03083252f6d7897ab03dc489a1e8119322fcac1554f92`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 21:17:29 GMT
ADD file:28f4377c61c0f8eb43a6b36e6a24ef5893f51d405d25b62e364988223537ae0b in / 
# Wed, 17 Feb 2021 21:17:37 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 22:10:46 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 17 Feb 2021 22:16:21 GMT
ENV HAPROXY_VERSION=2.1.11
# Wed, 17 Feb 2021 22:16:27 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.1/src/haproxy-2.1.11.tar.gz
# Wed, 17 Feb 2021 22:16:36 GMT
ENV HAPROXY_SHA256=feff37a5459d7aca8fcca50fa0e6d20d176394019cec3be17ec9c6ba0fdbdbad
# Wed, 17 Feb 2021 22:17:26 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 17 Feb 2021 22:17:34 GMT
STOPSIGNAL SIGUSR1
# Wed, 17 Feb 2021 22:17:36 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 17 Feb 2021 22:17:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 17 Feb 2021 22:18:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Feb 2021 22:18:14 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:cb672e0375a8f9bb3d33049ceb372ffa49b959bfc84fe6f72bfb97b682a608c8`  
		Last Modified: Wed, 17 Feb 2021 21:18:10 GMT  
		Size: 2.8 MB (2813081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f391a7d74b9bf5c2089e7957996d00d99ddc33d8295873bf28746716bb728a`  
		Last Modified: Wed, 17 Feb 2021 22:23:02 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dd03b44fedcdc44a51845776153a51eec69658c78b31ebbb7d4c9c5d9477441`  
		Last Modified: Wed, 17 Feb 2021 22:23:45 GMT  
		Size: 6.3 MB (6332218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccdce88ca5d3907cbb768fbaa27a821148e3ca73e1c87154542b072db235a712`  
		Last Modified: Wed, 17 Feb 2021 22:23:44 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d12b27836fb8ec99d79da07994133a4e40e88ca4441a058068445e6378b1976`  
		Last Modified: Wed, 17 Feb 2021 22:23:44 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.1-alpine` - linux; s390x

```console
$ docker pull haproxy@sha256:0c1210dfa3b0b8f0993215d25c9cf774efd5440cee85c30ba0fceda96d8c38ba
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8642859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b36c79ab0c8179ef5fcf9c459fb7674d3b786a7f137de663e78a6a03ba4327ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 20:41:27 GMT
ADD file:630c66f8d774d75b51e32aff812b438d377ebd3389c4aa6c324fdf8c03b6fa13 in / 
# Wed, 17 Feb 2021 20:41:27 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 21:33:33 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 17 Feb 2021 21:38:35 GMT
ENV HAPROXY_VERSION=2.1.11
# Wed, 17 Feb 2021 21:38:36 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.1/src/haproxy-2.1.11.tar.gz
# Wed, 17 Feb 2021 21:38:36 GMT
ENV HAPROXY_SHA256=feff37a5459d7aca8fcca50fa0e6d20d176394019cec3be17ec9c6ba0fdbdbad
# Wed, 17 Feb 2021 21:39:57 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 17 Feb 2021 21:39:59 GMT
STOPSIGNAL SIGUSR1
# Wed, 17 Feb 2021 21:39:59 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 17 Feb 2021 21:40:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 17 Feb 2021 21:40:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Feb 2021 21:40:03 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:ff5e8cb87555e9fa38a441f5cf0414e91353e2cd21cdb48d48b7de5bb39ce674`  
		Last Modified: Wed, 17 Feb 2021 20:41:58 GMT  
		Size: 2.6 MB (2602381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de25a3a0de168e6603cb978691ef3e7f11d7c9108d0ade38d3185d5d9dbdc094`  
		Last Modified: Wed, 17 Feb 2021 21:43:59 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a554ce42cf66fc32c16bbfbb6921589b11fd7a72eb4ef898b5c1fcc80c9c2d90`  
		Last Modified: Wed, 17 Feb 2021 21:44:30 GMT  
		Size: 6.0 MB (6038721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7db60cb31eaf76ee07470ae89b216f50876da7320605702196c77051d95bd61`  
		Last Modified: Wed, 17 Feb 2021 21:44:29 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c8d64fd3df5379cb79e77425280f5e7387a78b0423fc679d88bc09a6df53ac`  
		Last Modified: Wed, 17 Feb 2021 21:44:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haproxy:2.2`

```console
$ docker pull haproxy@sha256:17fc839f8647c90a1b8bfdb038ca15c70b3343a3b18155d4560aaba0feb4f23a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `haproxy:2.2` - linux; amd64

```console
$ docker pull haproxy@sha256:30fa9029baf82d42817be3ec10bc1e6d996bccdf350e0d60ea873110ab4c8cea
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36394072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d25326e1fec59f886205720c25366e7c209c54166a8bf8833077290ddd96510e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Mon, 08 Mar 2021 21:37:25 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 21:42:15 GMT
ENV HAPROXY_VERSION=2.2.10
# Mon, 08 Mar 2021 21:42:16 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.10.tar.gz
# Mon, 08 Mar 2021 21:42:16 GMT
ENV HAPROXY_SHA256=a027e9cd8f703ba48dc193f5ae34d9aa152221f67ab58a4e939c96b9f4edd3bc
# Mon, 08 Mar 2021 21:43:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 08 Mar 2021 21:43:05 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 21:43:05 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 21:43:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 08 Mar 2021 21:43:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 21:43:07 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7bca45a971fe608786870ce75c9976f8e5a958f55e1287a6120048b897c63b6`  
		Last Modified: Mon, 08 Mar 2021 21:52:33 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58f76c5dffb4c0a380d771810394a448234e32317f451d201fde80fb9a78eeed`  
		Last Modified: Mon, 08 Mar 2021 21:53:33 GMT  
		Size: 9.3 MB (9296986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b42b266bfd6b703e104c7feab7d02f7f829eb215e4956b3130a9df588dbfb2`  
		Last Modified: Mon, 08 Mar 2021 21:53:31 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47974a3e33f57ab6455f2472a18124450765ae233844059cd8b06743dff54bb`  
		Last Modified: Mon, 08 Mar 2021 21:53:32 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.2` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:73ff91d0f66aab67498a5fe774694b861ec7b1a749d3d5a9a1f01e97ab141bc9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33745871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41d3c16388f2706b685aced37923df63cbf2ecfdd1e69a10408c9df9ffe298b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:50:10 GMT
ADD file:fbd00ef7871dc27d7ed5fa8c238cdc80652bd87b8033be7de9e54a799bbf10a4 in / 
# Tue, 09 Feb 2021 02:50:11 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:45:24 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 03 Mar 2021 23:49:55 GMT
ENV HAPROXY_VERSION=2.2.10
# Wed, 03 Mar 2021 23:49:56 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.10.tar.gz
# Wed, 03 Mar 2021 23:49:56 GMT
ENV HAPROXY_SHA256=a027e9cd8f703ba48dc193f5ae34d9aa152221f67ab58a4e939c96b9f4edd3bc
# Wed, 03 Mar 2021 23:51:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 Mar 2021 23:51:17 GMT
STOPSIGNAL SIGUSR1
# Wed, 03 Mar 2021 23:51:19 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 03 Mar 2021 23:51:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 03 Mar 2021 23:51:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Mar 2021 23:51:33 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:8e683fcc73f4da7d69ce1d5f4e1d77510aa459490068f38db2d8663698b391a0`  
		Last Modified: Tue, 09 Feb 2021 02:59:07 GMT  
		Size: 24.8 MB (24839297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def565d52deae74587a55f60d168bd531ebe8095c594027b7057a8fc1be0e8af`  
		Last Modified: Tue, 09 Feb 2021 03:54:54 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:535ac2988228ac414cbf90d59aefe24781b4120b74285d4247c1c19fc3c285ff`  
		Last Modified: Wed, 03 Mar 2021 23:53:06 GMT  
		Size: 8.9 MB (8904631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c75860718fd09d4d1d1c08cf1e5004861505f3a1c39cfb8a7db6bc7a44038693`  
		Last Modified: Wed, 03 Mar 2021 23:53:02 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0628c5c9105fe74ab92e2956a77371fa0c3b0706d23e61a6b44c4b94de09a137`  
		Last Modified: Wed, 03 Mar 2021 23:53:01 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.2` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:20aea1a6a06f9934f5568b11e8853c8178dbe25bf4451b8f4c924a663fac2d8a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31421875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:133497e3b909eee15f36602495221781241792d52a8f98b12681dc8dd78386f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 03:00:57 GMT
ADD file:e675d50366bde57173a75f9a29367d765e7da2b7254c5254b64e777cf6870502 in / 
# Tue, 09 Feb 2021 03:01:00 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:49:38 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Thu, 04 Mar 2021 00:02:18 GMT
ENV HAPROXY_VERSION=2.2.10
# Thu, 04 Mar 2021 00:02:19 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.10.tar.gz
# Thu, 04 Mar 2021 00:02:21 GMT
ENV HAPROXY_SHA256=a027e9cd8f703ba48dc193f5ae34d9aa152221f67ab58a4e939c96b9f4edd3bc
# Thu, 04 Mar 2021 00:03:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 04 Mar 2021 00:03:46 GMT
STOPSIGNAL SIGUSR1
# Thu, 04 Mar 2021 00:03:48 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Thu, 04 Mar 2021 00:03:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 04 Mar 2021 00:03:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 00:03:56 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:db574d82360c3b60abadbef4f3daf8dee01f24741fc6ab3692aa543558d8b624`  
		Last Modified: Tue, 09 Feb 2021 03:09:46 GMT  
		Size: 22.7 MB (22703384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9978ebb1881387f11e025fb46dce2b3c715f705f6d240737574f8848c27fa0d7`  
		Last Modified: Tue, 09 Feb 2021 03:58:16 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d010a4f26095dac57fe322c8fca77e3ded2f3d272ee339ed750f4e4bda194cdc`  
		Last Modified: Thu, 04 Mar 2021 00:06:50 GMT  
		Size: 8.7 MB (8716549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6d9b893b368a4a867dc7d658afae85d822a29ea39c8edd8349ff07360c275b5`  
		Last Modified: Thu, 04 Mar 2021 00:06:48 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf5154622b3ad275982ebd343b0b1589448f33031f427285db574d08fc71da31`  
		Last Modified: Thu, 04 Mar 2021 00:06:48 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.2` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:3c3c947970064255078b0881210fed5bfccf4ffd32c650d4919544969598e535
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 MB (34964493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1fc4b06991e42504cf8ddda55c497c45c91d92fbb22bf996f8b0713deedef17`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:41:10 GMT
ADD file:d906dedaf14d8e3874b46787f7a1dbf268bc124c4e1dd32f13f3079e12f22238 in / 
# Tue, 09 Feb 2021 02:41:13 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:59:41 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 03 Mar 2021 23:42:07 GMT
ENV HAPROXY_VERSION=2.2.10
# Wed, 03 Mar 2021 23:42:08 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.10.tar.gz
# Wed, 03 Mar 2021 23:42:09 GMT
ENV HAPROXY_SHA256=a027e9cd8f703ba48dc193f5ae34d9aa152221f67ab58a4e939c96b9f4edd3bc
# Wed, 03 Mar 2021 23:42:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 Mar 2021 23:42:53 GMT
STOPSIGNAL SIGUSR1
# Wed, 03 Mar 2021 23:42:54 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 03 Mar 2021 23:42:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 03 Mar 2021 23:42:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Mar 2021 23:42:58 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:83c5cfdaa5385ea6fc4d31e724fd4dc5d74de847a7bdd968555b8f2c558dac0e`  
		Last Modified: Tue, 09 Feb 2021 02:47:27 GMT  
		Size: 25.9 MB (25851449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b7f43dd52365bce2c2b75f29577aa39d2b5794e2561cddc0678422ffc1f7d15`  
		Last Modified: Tue, 09 Feb 2021 04:08:36 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f93139e350e3df128fb0ea90fbfccc5b56d02db9d1f60958071391134dc48a3`  
		Last Modified: Wed, 03 Mar 2021 23:45:10 GMT  
		Size: 9.1 MB (9111101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b237a4ba4c115c155d87955ded33db31756d7f23009d6ab7c8c50a922939c7`  
		Last Modified: Wed, 03 Mar 2021 23:45:07 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eafe8f72c0e58ab277e633aa227b6912d7dabce25668e59adfae325d92b7116a`  
		Last Modified: Wed, 03 Mar 2021 23:45:07 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.2` - linux; 386

```console
$ docker pull haproxy@sha256:e8cd578831262c68c9f780e4bce0437d68a1f76015a06a3a1974dae9c4c40760
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 MB (36931345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:facdf90ca5a8342db83825a14b68ce8f75b9b361198e73149912a81da0fb1271`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:39:47 GMT
ADD file:61c31b1037672781ed0ecbc080ee3d49c83af49f5578b011544513fa9625698d in / 
# Tue, 09 Feb 2021 02:39:47 GMT
CMD ["bash"]
# Mon, 08 Mar 2021 22:02:40 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 22:07:20 GMT
ENV HAPROXY_VERSION=2.2.10
# Mon, 08 Mar 2021 22:07:20 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.10.tar.gz
# Mon, 08 Mar 2021 22:07:21 GMT
ENV HAPROXY_SHA256=a027e9cd8f703ba48dc193f5ae34d9aa152221f67ab58a4e939c96b9f4edd3bc
# Mon, 08 Mar 2021 22:08:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 08 Mar 2021 22:08:11 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 22:08:11 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 22:08:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 08 Mar 2021 22:08:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 22:08:12 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:27cbb00346a16ea900c1049a2e5b47942c586c377179e098382c8ca1c8e87966`  
		Last Modified: Tue, 09 Feb 2021 02:45:51 GMT  
		Size: 27.8 MB (27752731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b6129a97a33727ea8a598d1e797bccce491920bf29d769880cf2fc6d3e0436`  
		Last Modified: Mon, 08 Mar 2021 22:17:48 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a95aceb58fa39c7678dd2871722d308e7da51bb6635fd623de1e9bc45a0d612`  
		Last Modified: Mon, 08 Mar 2021 22:18:50 GMT  
		Size: 9.2 MB (9176672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54383f3c5fa30fd23c18b8855a9f3afd7df04fba710979b28404e6e2e0ba1736`  
		Last Modified: Mon, 08 Mar 2021 22:18:49 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0398b52a60591eda6202fd00b49bf8ecfa0a3e5d4cf45c2af876fc598e5ac71`  
		Last Modified: Mon, 08 Mar 2021 22:18:48 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.2` - linux; mips64le

```console
$ docker pull haproxy@sha256:68fce50fbcefd8cf3ee44e79ccbdcde6bff9062d8f7bdd31a75cd812af1dbcbf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34627259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ffbe5e71c677f9550a20a49495c9a54b1f70dad80206752ca96299f4225c481`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 03:09:26 GMT
ADD file:0222a151f4e5033d9eae98ce2b703a63f52d049dd72ac40bdd0dc2dafe619f0a in / 
# Tue, 09 Feb 2021 03:09:27 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:41:09 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 03 Mar 2021 23:10:04 GMT
ENV HAPROXY_VERSION=2.2.10
# Wed, 03 Mar 2021 23:10:05 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.10.tar.gz
# Wed, 03 Mar 2021 23:10:05 GMT
ENV HAPROXY_SHA256=a027e9cd8f703ba48dc193f5ae34d9aa152221f67ab58a4e939c96b9f4edd3bc
# Wed, 03 Mar 2021 23:12:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 Mar 2021 23:12:27 GMT
STOPSIGNAL SIGUSR1
# Wed, 03 Mar 2021 23:12:27 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 03 Mar 2021 23:12:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 03 Mar 2021 23:12:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Mar 2021 23:12:29 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:dfb81134097d874e01b495d1fba82e384056d0a3a45f01a69a2e86ae82af1e96`  
		Last Modified: Tue, 09 Feb 2021 03:15:55 GMT  
		Size: 25.8 MB (25764640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a549d56662447dd8cb15faf59ca0fc2eda7a877e9aee16aadd09fd46e4214a`  
		Last Modified: Tue, 09 Feb 2021 03:57:56 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65be8d0220e343aa0ba1db949674ff16f39389fb3c14309ce16783ed1924a1b7`  
		Last Modified: Wed, 03 Mar 2021 23:13:41 GMT  
		Size: 8.9 MB (8860669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5439ba6a6b54a0fe85acf47dcfe4b3465fd66d6d1fbe3aea3769acddab607594`  
		Last Modified: Wed, 03 Mar 2021 23:13:35 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8fde2a50b54742467311844dcb5636fd1ad40c152a43a629b366b301c582ae7`  
		Last Modified: Wed, 03 Mar 2021 23:13:35 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.2` - linux; ppc64le

```console
$ docker pull haproxy@sha256:3efd7155a63f7105e130532a3594776248df544bd493b909bf7f206bfa656f71
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40289282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7df67eff1aab2863a69fcea96ea8af6171ff19aac7152bf3824db5f957e54064`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:19:19 GMT
ADD file:9a8cfdf0eab394a693b5cde0700ad47b6e8506ef0b79fabb8a07874b96e6c394 in / 
# Tue, 09 Feb 2021 02:19:34 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 05:52:23 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 03 Mar 2021 23:23:38 GMT
ENV HAPROXY_VERSION=2.2.10
# Wed, 03 Mar 2021 23:23:42 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.10.tar.gz
# Wed, 03 Mar 2021 23:23:48 GMT
ENV HAPROXY_SHA256=a027e9cd8f703ba48dc193f5ae34d9aa152221f67ab58a4e939c96b9f4edd3bc
# Wed, 03 Mar 2021 23:28:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 Mar 2021 23:28:21 GMT
STOPSIGNAL SIGUSR1
# Wed, 03 Mar 2021 23:28:22 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 03 Mar 2021 23:28:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 03 Mar 2021 23:28:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Mar 2021 23:28:50 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:9996b4fb6bc1c50f95ba30f8988c9c89526556fa320d3fda59d3d8359f7810d6`  
		Last Modified: Tue, 09 Feb 2021 02:27:59 GMT  
		Size: 30.5 MB (30519509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7f600bc4989eb9f12d5006a73f5958eb4fe85f86bc4008d7a899bb935b0f1c`  
		Last Modified: Tue, 09 Feb 2021 06:38:36 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b76b41179c41c897d8edf7d548f5975bec661a4f4b4dfa41bf1ad552d6b46df6`  
		Last Modified: Wed, 03 Mar 2021 23:32:16 GMT  
		Size: 9.8 MB (9767826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f9cdabeced7eb35a6a7ca4ac5e8ecfa86ef0670b1d2037fbc9d3815cf733c9`  
		Last Modified: Wed, 03 Mar 2021 23:32:14 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d15db81144a7e1545a6f22b92ab6c4d2d16eedd0eef2aa766315b6c045d836d`  
		Last Modified: Wed, 03 Mar 2021 23:32:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.2` - linux; s390x

```console
$ docker pull haproxy@sha256:21ed36dee62cfe436cbc1fa93fd6564f3cee16ee4a9526020f246d5b4fb16760
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34709539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f22bf5194ddcbee6e27b5238d7ecf6dd66d96194c3a650d35a5de1bcbd8510a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:42:10 GMT
ADD file:0edb2de05df54191a141bd125f59d7e14eef0cc4576927a247b8dd7d6f255d04 in / 
# Tue, 09 Feb 2021 02:42:12 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:39:30 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 03 Mar 2021 23:43:15 GMT
ENV HAPROXY_VERSION=2.2.10
# Wed, 03 Mar 2021 23:43:16 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.10.tar.gz
# Wed, 03 Mar 2021 23:43:16 GMT
ENV HAPROXY_SHA256=a027e9cd8f703ba48dc193f5ae34d9aa152221f67ab58a4e939c96b9f4edd3bc
# Wed, 03 Mar 2021 23:43:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 Mar 2021 23:43:52 GMT
STOPSIGNAL SIGUSR1
# Wed, 03 Mar 2021 23:43:52 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 03 Mar 2021 23:43:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 03 Mar 2021 23:43:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Mar 2021 23:43:55 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:032413a44cf56b097e48b8221bf475ca1bec26e7a27f35fe61d699366a335b79`  
		Last Modified: Tue, 09 Feb 2021 02:45:31 GMT  
		Size: 25.7 MB (25710021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e65f701864562492efa2c0035134b62d68efdb6e7241a0a2dcc3151e6d5775b`  
		Last Modified: Tue, 09 Feb 2021 03:44:28 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2f87d09b1e4f93d137fcd4aca47d17548c96dc51b1974840f8582386165439a`  
		Last Modified: Wed, 03 Mar 2021 23:46:18 GMT  
		Size: 9.0 MB (8997573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4014d184cd70f402072c04852e6e2af2abfaac153e70d6d1cd20a31bdbcb4663`  
		Last Modified: Wed, 03 Mar 2021 23:46:15 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e21792cc4eacae1d21897fd6dc774923fca5fd0aeb505e893846a21c4e3fe06`  
		Last Modified: Wed, 03 Mar 2021 23:46:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haproxy:2.2.10`

```console
$ docker pull haproxy@sha256:17fc839f8647c90a1b8bfdb038ca15c70b3343a3b18155d4560aaba0feb4f23a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `haproxy:2.2.10` - linux; amd64

```console
$ docker pull haproxy@sha256:30fa9029baf82d42817be3ec10bc1e6d996bccdf350e0d60ea873110ab4c8cea
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36394072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d25326e1fec59f886205720c25366e7c209c54166a8bf8833077290ddd96510e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Mon, 08 Mar 2021 21:37:25 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 21:42:15 GMT
ENV HAPROXY_VERSION=2.2.10
# Mon, 08 Mar 2021 21:42:16 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.10.tar.gz
# Mon, 08 Mar 2021 21:42:16 GMT
ENV HAPROXY_SHA256=a027e9cd8f703ba48dc193f5ae34d9aa152221f67ab58a4e939c96b9f4edd3bc
# Mon, 08 Mar 2021 21:43:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 08 Mar 2021 21:43:05 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 21:43:05 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 21:43:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 08 Mar 2021 21:43:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 21:43:07 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7bca45a971fe608786870ce75c9976f8e5a958f55e1287a6120048b897c63b6`  
		Last Modified: Mon, 08 Mar 2021 21:52:33 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58f76c5dffb4c0a380d771810394a448234e32317f451d201fde80fb9a78eeed`  
		Last Modified: Mon, 08 Mar 2021 21:53:33 GMT  
		Size: 9.3 MB (9296986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b42b266bfd6b703e104c7feab7d02f7f829eb215e4956b3130a9df588dbfb2`  
		Last Modified: Mon, 08 Mar 2021 21:53:31 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47974a3e33f57ab6455f2472a18124450765ae233844059cd8b06743dff54bb`  
		Last Modified: Mon, 08 Mar 2021 21:53:32 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.2.10` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:73ff91d0f66aab67498a5fe774694b861ec7b1a749d3d5a9a1f01e97ab141bc9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33745871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41d3c16388f2706b685aced37923df63cbf2ecfdd1e69a10408c9df9ffe298b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:50:10 GMT
ADD file:fbd00ef7871dc27d7ed5fa8c238cdc80652bd87b8033be7de9e54a799bbf10a4 in / 
# Tue, 09 Feb 2021 02:50:11 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:45:24 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 03 Mar 2021 23:49:55 GMT
ENV HAPROXY_VERSION=2.2.10
# Wed, 03 Mar 2021 23:49:56 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.10.tar.gz
# Wed, 03 Mar 2021 23:49:56 GMT
ENV HAPROXY_SHA256=a027e9cd8f703ba48dc193f5ae34d9aa152221f67ab58a4e939c96b9f4edd3bc
# Wed, 03 Mar 2021 23:51:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 Mar 2021 23:51:17 GMT
STOPSIGNAL SIGUSR1
# Wed, 03 Mar 2021 23:51:19 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 03 Mar 2021 23:51:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 03 Mar 2021 23:51:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Mar 2021 23:51:33 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:8e683fcc73f4da7d69ce1d5f4e1d77510aa459490068f38db2d8663698b391a0`  
		Last Modified: Tue, 09 Feb 2021 02:59:07 GMT  
		Size: 24.8 MB (24839297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def565d52deae74587a55f60d168bd531ebe8095c594027b7057a8fc1be0e8af`  
		Last Modified: Tue, 09 Feb 2021 03:54:54 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:535ac2988228ac414cbf90d59aefe24781b4120b74285d4247c1c19fc3c285ff`  
		Last Modified: Wed, 03 Mar 2021 23:53:06 GMT  
		Size: 8.9 MB (8904631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c75860718fd09d4d1d1c08cf1e5004861505f3a1c39cfb8a7db6bc7a44038693`  
		Last Modified: Wed, 03 Mar 2021 23:53:02 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0628c5c9105fe74ab92e2956a77371fa0c3b0706d23e61a6b44c4b94de09a137`  
		Last Modified: Wed, 03 Mar 2021 23:53:01 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.2.10` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:20aea1a6a06f9934f5568b11e8853c8178dbe25bf4451b8f4c924a663fac2d8a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31421875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:133497e3b909eee15f36602495221781241792d52a8f98b12681dc8dd78386f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 03:00:57 GMT
ADD file:e675d50366bde57173a75f9a29367d765e7da2b7254c5254b64e777cf6870502 in / 
# Tue, 09 Feb 2021 03:01:00 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:49:38 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Thu, 04 Mar 2021 00:02:18 GMT
ENV HAPROXY_VERSION=2.2.10
# Thu, 04 Mar 2021 00:02:19 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.10.tar.gz
# Thu, 04 Mar 2021 00:02:21 GMT
ENV HAPROXY_SHA256=a027e9cd8f703ba48dc193f5ae34d9aa152221f67ab58a4e939c96b9f4edd3bc
# Thu, 04 Mar 2021 00:03:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 04 Mar 2021 00:03:46 GMT
STOPSIGNAL SIGUSR1
# Thu, 04 Mar 2021 00:03:48 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Thu, 04 Mar 2021 00:03:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 04 Mar 2021 00:03:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 00:03:56 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:db574d82360c3b60abadbef4f3daf8dee01f24741fc6ab3692aa543558d8b624`  
		Last Modified: Tue, 09 Feb 2021 03:09:46 GMT  
		Size: 22.7 MB (22703384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9978ebb1881387f11e025fb46dce2b3c715f705f6d240737574f8848c27fa0d7`  
		Last Modified: Tue, 09 Feb 2021 03:58:16 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d010a4f26095dac57fe322c8fca77e3ded2f3d272ee339ed750f4e4bda194cdc`  
		Last Modified: Thu, 04 Mar 2021 00:06:50 GMT  
		Size: 8.7 MB (8716549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6d9b893b368a4a867dc7d658afae85d822a29ea39c8edd8349ff07360c275b5`  
		Last Modified: Thu, 04 Mar 2021 00:06:48 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf5154622b3ad275982ebd343b0b1589448f33031f427285db574d08fc71da31`  
		Last Modified: Thu, 04 Mar 2021 00:06:48 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.2.10` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:3c3c947970064255078b0881210fed5bfccf4ffd32c650d4919544969598e535
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 MB (34964493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1fc4b06991e42504cf8ddda55c497c45c91d92fbb22bf996f8b0713deedef17`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:41:10 GMT
ADD file:d906dedaf14d8e3874b46787f7a1dbf268bc124c4e1dd32f13f3079e12f22238 in / 
# Tue, 09 Feb 2021 02:41:13 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:59:41 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 03 Mar 2021 23:42:07 GMT
ENV HAPROXY_VERSION=2.2.10
# Wed, 03 Mar 2021 23:42:08 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.10.tar.gz
# Wed, 03 Mar 2021 23:42:09 GMT
ENV HAPROXY_SHA256=a027e9cd8f703ba48dc193f5ae34d9aa152221f67ab58a4e939c96b9f4edd3bc
# Wed, 03 Mar 2021 23:42:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 Mar 2021 23:42:53 GMT
STOPSIGNAL SIGUSR1
# Wed, 03 Mar 2021 23:42:54 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 03 Mar 2021 23:42:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 03 Mar 2021 23:42:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Mar 2021 23:42:58 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:83c5cfdaa5385ea6fc4d31e724fd4dc5d74de847a7bdd968555b8f2c558dac0e`  
		Last Modified: Tue, 09 Feb 2021 02:47:27 GMT  
		Size: 25.9 MB (25851449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b7f43dd52365bce2c2b75f29577aa39d2b5794e2561cddc0678422ffc1f7d15`  
		Last Modified: Tue, 09 Feb 2021 04:08:36 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f93139e350e3df128fb0ea90fbfccc5b56d02db9d1f60958071391134dc48a3`  
		Last Modified: Wed, 03 Mar 2021 23:45:10 GMT  
		Size: 9.1 MB (9111101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b237a4ba4c115c155d87955ded33db31756d7f23009d6ab7c8c50a922939c7`  
		Last Modified: Wed, 03 Mar 2021 23:45:07 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eafe8f72c0e58ab277e633aa227b6912d7dabce25668e59adfae325d92b7116a`  
		Last Modified: Wed, 03 Mar 2021 23:45:07 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.2.10` - linux; 386

```console
$ docker pull haproxy@sha256:e8cd578831262c68c9f780e4bce0437d68a1f76015a06a3a1974dae9c4c40760
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 MB (36931345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:facdf90ca5a8342db83825a14b68ce8f75b9b361198e73149912a81da0fb1271`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:39:47 GMT
ADD file:61c31b1037672781ed0ecbc080ee3d49c83af49f5578b011544513fa9625698d in / 
# Tue, 09 Feb 2021 02:39:47 GMT
CMD ["bash"]
# Mon, 08 Mar 2021 22:02:40 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 22:07:20 GMT
ENV HAPROXY_VERSION=2.2.10
# Mon, 08 Mar 2021 22:07:20 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.10.tar.gz
# Mon, 08 Mar 2021 22:07:21 GMT
ENV HAPROXY_SHA256=a027e9cd8f703ba48dc193f5ae34d9aa152221f67ab58a4e939c96b9f4edd3bc
# Mon, 08 Mar 2021 22:08:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 08 Mar 2021 22:08:11 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 22:08:11 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 22:08:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 08 Mar 2021 22:08:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 22:08:12 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:27cbb00346a16ea900c1049a2e5b47942c586c377179e098382c8ca1c8e87966`  
		Last Modified: Tue, 09 Feb 2021 02:45:51 GMT  
		Size: 27.8 MB (27752731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b6129a97a33727ea8a598d1e797bccce491920bf29d769880cf2fc6d3e0436`  
		Last Modified: Mon, 08 Mar 2021 22:17:48 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a95aceb58fa39c7678dd2871722d308e7da51bb6635fd623de1e9bc45a0d612`  
		Last Modified: Mon, 08 Mar 2021 22:18:50 GMT  
		Size: 9.2 MB (9176672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54383f3c5fa30fd23c18b8855a9f3afd7df04fba710979b28404e6e2e0ba1736`  
		Last Modified: Mon, 08 Mar 2021 22:18:49 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0398b52a60591eda6202fd00b49bf8ecfa0a3e5d4cf45c2af876fc598e5ac71`  
		Last Modified: Mon, 08 Mar 2021 22:18:48 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.2.10` - linux; mips64le

```console
$ docker pull haproxy@sha256:68fce50fbcefd8cf3ee44e79ccbdcde6bff9062d8f7bdd31a75cd812af1dbcbf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34627259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ffbe5e71c677f9550a20a49495c9a54b1f70dad80206752ca96299f4225c481`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 03:09:26 GMT
ADD file:0222a151f4e5033d9eae98ce2b703a63f52d049dd72ac40bdd0dc2dafe619f0a in / 
# Tue, 09 Feb 2021 03:09:27 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:41:09 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 03 Mar 2021 23:10:04 GMT
ENV HAPROXY_VERSION=2.2.10
# Wed, 03 Mar 2021 23:10:05 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.10.tar.gz
# Wed, 03 Mar 2021 23:10:05 GMT
ENV HAPROXY_SHA256=a027e9cd8f703ba48dc193f5ae34d9aa152221f67ab58a4e939c96b9f4edd3bc
# Wed, 03 Mar 2021 23:12:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 Mar 2021 23:12:27 GMT
STOPSIGNAL SIGUSR1
# Wed, 03 Mar 2021 23:12:27 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 03 Mar 2021 23:12:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 03 Mar 2021 23:12:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Mar 2021 23:12:29 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:dfb81134097d874e01b495d1fba82e384056d0a3a45f01a69a2e86ae82af1e96`  
		Last Modified: Tue, 09 Feb 2021 03:15:55 GMT  
		Size: 25.8 MB (25764640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a549d56662447dd8cb15faf59ca0fc2eda7a877e9aee16aadd09fd46e4214a`  
		Last Modified: Tue, 09 Feb 2021 03:57:56 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65be8d0220e343aa0ba1db949674ff16f39389fb3c14309ce16783ed1924a1b7`  
		Last Modified: Wed, 03 Mar 2021 23:13:41 GMT  
		Size: 8.9 MB (8860669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5439ba6a6b54a0fe85acf47dcfe4b3465fd66d6d1fbe3aea3769acddab607594`  
		Last Modified: Wed, 03 Mar 2021 23:13:35 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8fde2a50b54742467311844dcb5636fd1ad40c152a43a629b366b301c582ae7`  
		Last Modified: Wed, 03 Mar 2021 23:13:35 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.2.10` - linux; ppc64le

```console
$ docker pull haproxy@sha256:3efd7155a63f7105e130532a3594776248df544bd493b909bf7f206bfa656f71
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40289282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7df67eff1aab2863a69fcea96ea8af6171ff19aac7152bf3824db5f957e54064`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:19:19 GMT
ADD file:9a8cfdf0eab394a693b5cde0700ad47b6e8506ef0b79fabb8a07874b96e6c394 in / 
# Tue, 09 Feb 2021 02:19:34 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 05:52:23 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 03 Mar 2021 23:23:38 GMT
ENV HAPROXY_VERSION=2.2.10
# Wed, 03 Mar 2021 23:23:42 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.10.tar.gz
# Wed, 03 Mar 2021 23:23:48 GMT
ENV HAPROXY_SHA256=a027e9cd8f703ba48dc193f5ae34d9aa152221f67ab58a4e939c96b9f4edd3bc
# Wed, 03 Mar 2021 23:28:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 Mar 2021 23:28:21 GMT
STOPSIGNAL SIGUSR1
# Wed, 03 Mar 2021 23:28:22 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 03 Mar 2021 23:28:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 03 Mar 2021 23:28:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Mar 2021 23:28:50 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:9996b4fb6bc1c50f95ba30f8988c9c89526556fa320d3fda59d3d8359f7810d6`  
		Last Modified: Tue, 09 Feb 2021 02:27:59 GMT  
		Size: 30.5 MB (30519509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7f600bc4989eb9f12d5006a73f5958eb4fe85f86bc4008d7a899bb935b0f1c`  
		Last Modified: Tue, 09 Feb 2021 06:38:36 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b76b41179c41c897d8edf7d548f5975bec661a4f4b4dfa41bf1ad552d6b46df6`  
		Last Modified: Wed, 03 Mar 2021 23:32:16 GMT  
		Size: 9.8 MB (9767826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f9cdabeced7eb35a6a7ca4ac5e8ecfa86ef0670b1d2037fbc9d3815cf733c9`  
		Last Modified: Wed, 03 Mar 2021 23:32:14 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d15db81144a7e1545a6f22b92ab6c4d2d16eedd0eef2aa766315b6c045d836d`  
		Last Modified: Wed, 03 Mar 2021 23:32:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.2.10` - linux; s390x

```console
$ docker pull haproxy@sha256:21ed36dee62cfe436cbc1fa93fd6564f3cee16ee4a9526020f246d5b4fb16760
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34709539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f22bf5194ddcbee6e27b5238d7ecf6dd66d96194c3a650d35a5de1bcbd8510a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:42:10 GMT
ADD file:0edb2de05df54191a141bd125f59d7e14eef0cc4576927a247b8dd7d6f255d04 in / 
# Tue, 09 Feb 2021 02:42:12 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:39:30 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 03 Mar 2021 23:43:15 GMT
ENV HAPROXY_VERSION=2.2.10
# Wed, 03 Mar 2021 23:43:16 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.10.tar.gz
# Wed, 03 Mar 2021 23:43:16 GMT
ENV HAPROXY_SHA256=a027e9cd8f703ba48dc193f5ae34d9aa152221f67ab58a4e939c96b9f4edd3bc
# Wed, 03 Mar 2021 23:43:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 Mar 2021 23:43:52 GMT
STOPSIGNAL SIGUSR1
# Wed, 03 Mar 2021 23:43:52 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 03 Mar 2021 23:43:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 03 Mar 2021 23:43:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Mar 2021 23:43:55 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:032413a44cf56b097e48b8221bf475ca1bec26e7a27f35fe61d699366a335b79`  
		Last Modified: Tue, 09 Feb 2021 02:45:31 GMT  
		Size: 25.7 MB (25710021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e65f701864562492efa2c0035134b62d68efdb6e7241a0a2dcc3151e6d5775b`  
		Last Modified: Tue, 09 Feb 2021 03:44:28 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2f87d09b1e4f93d137fcd4aca47d17548c96dc51b1974840f8582386165439a`  
		Last Modified: Wed, 03 Mar 2021 23:46:18 GMT  
		Size: 9.0 MB (8997573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4014d184cd70f402072c04852e6e2af2abfaac153e70d6d1cd20a31bdbcb4663`  
		Last Modified: Wed, 03 Mar 2021 23:46:15 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e21792cc4eacae1d21897fd6dc774923fca5fd0aeb505e893846a21c4e3fe06`  
		Last Modified: Wed, 03 Mar 2021 23:46:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haproxy:2.2.10-alpine`

```console
$ docker pull haproxy@sha256:4396bf1f43cbeea0f4e2d651b9989685b505d474a347c10855b41dcf49aa7a1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `haproxy:2.2.10-alpine` - linux; amd64

```console
$ docker pull haproxy@sha256:2f877531092feb1a6596ee8bc6eb00d9d993dab984715d4ce3513805df05aa02
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9177632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2549b4a31f8af89b6bdb4695a4a59374b47fd8b40b8df2f2c20628da267486d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 21:19:54 GMT
ADD file:80bf8bd014071345b1c0364eeb0a5e48f3fb0d87f9c31cb990e57caa652b59b8 in / 
# Wed, 17 Feb 2021 21:19:54 GMT
CMD ["/bin/sh"]
# Mon, 08 Mar 2021 21:38:26 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 21:43:17 GMT
ENV HAPROXY_VERSION=2.2.10
# Mon, 08 Mar 2021 21:43:17 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.10.tar.gz
# Mon, 08 Mar 2021 21:43:17 GMT
ENV HAPROXY_SHA256=a027e9cd8f703ba48dc193f5ae34d9aa152221f67ab58a4e939c96b9f4edd3bc
# Mon, 08 Mar 2021 21:44:18 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Mon, 08 Mar 2021 21:44:18 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 21:44:18 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 21:44:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 08 Mar 2021 21:44:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 21:44:20 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:ba3557a56b150f9b813f9d02274d62914fd8fce120dd374d9ee17b87cf1d277d`  
		Last Modified: Wed, 17 Feb 2021 21:20:25 GMT  
		Size: 2.8 MB (2811657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9216237f12c4d44ab183590086cf2a09004b5609c4b50871d88658faa495245`  
		Last Modified: Mon, 08 Mar 2021 21:52:45 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ab448b61e71513906284c50caa18b4bbead3c9f4e44e9563a51155483cc814`  
		Last Modified: Mon, 08 Mar 2021 21:53:58 GMT  
		Size: 6.4 MB (6364220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1496e8d1fc05d2242dec46f741fd8fb5b7f5f763ff5fe19ac959ef58db7c8c15`  
		Last Modified: Mon, 08 Mar 2021 21:53:46 GMT  
		Size: 448.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c883a4dc2f6239a275129836cd6fe8c66fc9f419c95de34ba15df40807eadd0`  
		Last Modified: Mon, 08 Mar 2021 21:53:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.2.10-alpine` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:dce2bd7fdb71321a8829f51ee51fe1f8df12ede9854586f628de4bf9b6b390c5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8871339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07e6e2e4dd3516d94cc27ed41c046bad56909aff74a5eebdb69d23185cf56e6e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 20:49:32 GMT
ADD file:c04fbd3b039001c592cfa14f8388f8934ed4223ccf274dbb926e75039e172af4 in / 
# Wed, 17 Feb 2021 20:49:33 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 21:08:27 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 03 Mar 2021 23:53:11 GMT
ENV HAPROXY_VERSION=2.2.10
# Wed, 03 Mar 2021 23:53:13 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.10.tar.gz
# Wed, 03 Mar 2021 23:53:14 GMT
ENV HAPROXY_SHA256=a027e9cd8f703ba48dc193f5ae34d9aa152221f67ab58a4e939c96b9f4edd3bc
# Wed, 03 Mar 2021 23:53:47 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 03 Mar 2021 23:53:48 GMT
STOPSIGNAL SIGUSR1
# Wed, 03 Mar 2021 23:53:49 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 03 Mar 2021 23:53:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 03 Mar 2021 23:53:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Mar 2021 23:53:57 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:1353527ebe111f9bb1e271264a3c182e909e4b36463f80d7dbde1be0713eb892`  
		Last Modified: Wed, 17 Feb 2021 20:50:06 GMT  
		Size: 2.6 MB (2622039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d174378d3ee2c0c6e6a85b5228f929557826d80bcd23b2434093942f499361a7`  
		Last Modified: Wed, 17 Feb 2021 21:12:31 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d92e731bf4971bbb56699109cc2c7bf258a08b8c71fd2ce618628ed0b4be2b1a`  
		Last Modified: Wed, 03 Mar 2021 23:55:11 GMT  
		Size: 6.2 MB (6247545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8313b91724ce11e0d69d1f84cd9ba8ce0fd4dd4784e6deb2c2987413db0b472b`  
		Last Modified: Wed, 03 Mar 2021 23:55:09 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528f6166aa7000e8e0a6ddf712ac1e81bc5ddee4e5003b80a6542ad199662e23`  
		Last Modified: Wed, 03 Mar 2021 23:55:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.2.10-alpine` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:bd8a4e822b3d304f69ee657b808cc512c82005f7986e37a1b61a8308e14d5ba5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8588802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0035fe4ee0d310975e18c33d050c0fed342d40fc90715c6b91982cb91f1aa0fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 20:57:36 GMT
ADD file:efdd39e5243eaf378f12ad5a85d2222b44930850a90263e5f17e8a6b5e9bc9b8 in / 
# Wed, 17 Feb 2021 20:57:37 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 21:49:42 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Thu, 04 Mar 2021 00:04:07 GMT
ENV HAPROXY_VERSION=2.2.10
# Thu, 04 Mar 2021 00:04:09 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.10.tar.gz
# Thu, 04 Mar 2021 00:04:12 GMT
ENV HAPROXY_SHA256=a027e9cd8f703ba48dc193f5ae34d9aa152221f67ab58a4e939c96b9f4edd3bc
# Thu, 04 Mar 2021 00:04:46 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Thu, 04 Mar 2021 00:04:47 GMT
STOPSIGNAL SIGUSR1
# Thu, 04 Mar 2021 00:04:49 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Thu, 04 Mar 2021 00:04:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 04 Mar 2021 00:04:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 00:04:55 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f55b840e27d3dbe27e44497103a4397f043749f933eb0433d29e2f104b3435ef`  
		Last Modified: Wed, 17 Feb 2021 20:58:14 GMT  
		Size: 2.4 MB (2423892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86398e5ccaeed703d9464d57f2d97546fad0481312144292414eb1cf857b617f`  
		Last Modified: Wed, 17 Feb 2021 21:55:00 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00ad0cba7b2138c19356311eceb6fd5d2af2432778f97cf07d9b384d5524278`  
		Last Modified: Thu, 04 Mar 2021 00:07:00 GMT  
		Size: 6.2 MB (6163153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b337734f16cc0eff0d2bb38d7431f457cd7992e4992f77789263d6611d7e407b`  
		Last Modified: Thu, 04 Mar 2021 00:06:58 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb03a37f226d57efe43f03eb956ef49a20693dc865f15de068de3f08e6c56aba`  
		Last Modified: Thu, 04 Mar 2021 00:06:58 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.2.10-alpine` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:9df40d9acef87692f82a74b70ce1d60af5cca36f61239d82d12433ed0af482d8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9083113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e914a0cee60954b5adb34a5fd43d3fa4698fb1e4747afcaca9006dbc9e6c4cf2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 20:39:29 GMT
ADD file:3bf1497bd250cf7c73c12231dc4ebe3a3a67f2cd99e35bce47ef6674683aeb1d in / 
# Wed, 17 Feb 2021 20:39:30 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 21:36:08 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 03 Mar 2021 23:43:05 GMT
ENV HAPROXY_VERSION=2.2.10
# Wed, 03 Mar 2021 23:43:06 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.10.tar.gz
# Wed, 03 Mar 2021 23:43:07 GMT
ENV HAPROXY_SHA256=a027e9cd8f703ba48dc193f5ae34d9aa152221f67ab58a4e939c96b9f4edd3bc
# Wed, 03 Mar 2021 23:43:29 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 03 Mar 2021 23:43:30 GMT
STOPSIGNAL SIGUSR1
# Wed, 03 Mar 2021 23:43:31 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 03 Mar 2021 23:43:33 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 03 Mar 2021 23:43:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Mar 2021 23:43:35 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:069a56d6d07f6b186fbb82e4486616b9be9a37ce32a63013af6cddcb65898182`  
		Last Modified: Wed, 17 Feb 2021 20:40:04 GMT  
		Size: 2.7 MB (2711572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6644620fa9074da825714fc7794756e2b0e36f3e83ffc2bc01bbc9df0de9e373`  
		Last Modified: Wed, 17 Feb 2021 21:41:18 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a59369a058df1f7b291ab7b129ef07290c2a99545bea6f42cfa0f54436183bb`  
		Last Modified: Wed, 03 Mar 2021 23:45:22 GMT  
		Size: 6.4 MB (6369785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e982f4480ea14efe8106105e56424bc6bee3368b3299cd98b1aad1e5609140`  
		Last Modified: Wed, 03 Mar 2021 23:45:20 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffebf1b2b70d66bcbda9707eb957d0e25635210167d94d991cc7e81130ded334`  
		Last Modified: Wed, 03 Mar 2021 23:45:20 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.2.10-alpine` - linux; 386

```console
$ docker pull haproxy@sha256:659a38f29b31e96bd5aecab83a003f3f09e1eb5eebd43d6169b02ac77d8ed7be
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9012210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c724357a8f8f4b645b234f5584c0748d1a8db582d156e91d506d5574ccf1b2ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 21:38:34 GMT
ADD file:eaee53da3c87749799de55809e4a5b526c56855332b961a85b1184c660f1d65b in / 
# Wed, 17 Feb 2021 21:38:35 GMT
CMD ["/bin/sh"]
# Mon, 08 Mar 2021 22:03:53 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 22:08:22 GMT
ENV HAPROXY_VERSION=2.2.10
# Mon, 08 Mar 2021 22:08:22 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.10.tar.gz
# Mon, 08 Mar 2021 22:08:22 GMT
ENV HAPROXY_SHA256=a027e9cd8f703ba48dc193f5ae34d9aa152221f67ab58a4e939c96b9f4edd3bc
# Mon, 08 Mar 2021 22:09:21 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Mon, 08 Mar 2021 22:09:21 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 22:09:21 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 22:09:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 08 Mar 2021 22:09:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 22:09:23 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:86205afa28f6bc624469015a543d16608258d2828411a92c662f4fdc6d276e18`  
		Last Modified: Wed, 17 Feb 2021 21:39:07 GMT  
		Size: 2.8 MB (2818177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080e85d941540171ac6a020af17b393f2a40b03d40b9677d708d31ffb6e31b71`  
		Last Modified: Mon, 08 Mar 2021 22:18:02 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dafe934780af9f6588fe0b199a4c0b60e557597c52ed66de79f143c33b9f40c`  
		Last Modified: Mon, 08 Mar 2021 22:19:06 GMT  
		Size: 6.2 MB (6192281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6792eb8d4ba43ae0b592f09026d5cc688e72235dc893697be4e2b5c446409863`  
		Last Modified: Mon, 08 Mar 2021 22:19:04 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:682c8c2e4bc6bc83b8e4eea6ff73da639b17e212f85d36a5407aadb8a64f9024`  
		Last Modified: Mon, 08 Mar 2021 22:19:04 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.2.10-alpine` - linux; ppc64le

```console
$ docker pull haproxy@sha256:7c55559ea5e08f971f817d05e45bb569929812dd49110cc075bde9c0c74fbf8b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9496257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fa09275b3a555d9d28aca6380470a700262bc2fa9550d6cceefe3327d8299af`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 21:17:29 GMT
ADD file:28f4377c61c0f8eb43a6b36e6a24ef5893f51d405d25b62e364988223537ae0b in / 
# Wed, 17 Feb 2021 21:17:37 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 22:10:46 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 03 Mar 2021 23:29:05 GMT
ENV HAPROXY_VERSION=2.2.10
# Wed, 03 Mar 2021 23:29:08 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.10.tar.gz
# Wed, 03 Mar 2021 23:29:12 GMT
ENV HAPROXY_SHA256=a027e9cd8f703ba48dc193f5ae34d9aa152221f67ab58a4e939c96b9f4edd3bc
# Wed, 03 Mar 2021 23:29:57 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 03 Mar 2021 23:30:06 GMT
STOPSIGNAL SIGUSR1
# Wed, 03 Mar 2021 23:30:07 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 03 Mar 2021 23:30:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 03 Mar 2021 23:30:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Mar 2021 23:30:34 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:cb672e0375a8f9bb3d33049ceb372ffa49b959bfc84fe6f72bfb97b682a608c8`  
		Last Modified: Wed, 17 Feb 2021 21:18:10 GMT  
		Size: 2.8 MB (2813081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f391a7d74b9bf5c2089e7957996d00d99ddc33d8295873bf28746716bb728a`  
		Last Modified: Wed, 17 Feb 2021 22:23:02 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3895621bf409c59caef35106ecb9c73d57db6ab26c83e908bb2f846ce3b2420e`  
		Last Modified: Wed, 03 Mar 2021 23:32:35 GMT  
		Size: 6.7 MB (6681415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a16f70021d25609a108a39f41eff539ab12df1aba78f8d87564a9022864f65d`  
		Last Modified: Wed, 03 Mar 2021 23:32:34 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67bc8b05d75cf8717f438ad79f81f009294c601e828c4cbd406b08d167bd4f80`  
		Last Modified: Wed, 03 Mar 2021 23:32:34 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.2.10-alpine` - linux; s390x

```console
$ docker pull haproxy@sha256:5882e4526d054b2db8cdc8b0478d1a2b56273796af2dcc87c2fcd3b9b38f0dcf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8934271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97f0501dfe1a6477b450f2c11dc0f5c7db80bea48457a4de575e5798fd920abe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 20:41:27 GMT
ADD file:630c66f8d774d75b51e32aff812b438d377ebd3389c4aa6c324fdf8c03b6fa13 in / 
# Wed, 17 Feb 2021 20:41:27 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 21:33:33 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 03 Mar 2021 23:44:04 GMT
ENV HAPROXY_VERSION=2.2.10
# Wed, 03 Mar 2021 23:44:04 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.10.tar.gz
# Wed, 03 Mar 2021 23:44:05 GMT
ENV HAPROXY_SHA256=a027e9cd8f703ba48dc193f5ae34d9aa152221f67ab58a4e939c96b9f4edd3bc
# Wed, 03 Mar 2021 23:44:42 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 03 Mar 2021 23:44:43 GMT
STOPSIGNAL SIGUSR1
# Wed, 03 Mar 2021 23:44:43 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 03 Mar 2021 23:44:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 03 Mar 2021 23:44:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Mar 2021 23:44:44 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:ff5e8cb87555e9fa38a441f5cf0414e91353e2cd21cdb48d48b7de5bb39ce674`  
		Last Modified: Wed, 17 Feb 2021 20:41:58 GMT  
		Size: 2.6 MB (2602381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de25a3a0de168e6603cb978691ef3e7f11d7c9108d0ade38d3185d5d9dbdc094`  
		Last Modified: Wed, 17 Feb 2021 21:43:59 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc37ee0272550cdbed16f03b4d75571d970685b3a0c7b8d29484c919d8a9705`  
		Last Modified: Wed, 03 Mar 2021 23:46:27 GMT  
		Size: 6.3 MB (6330135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36a50696ff802571b01c8fa6b843837fc6b5e23d4948b2b73404ce94b9fa2ee`  
		Last Modified: Wed, 03 Mar 2021 23:46:26 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5abb15abe9d69125c600f2786dc4197578896c9d134fc5233bbbfcbcd125744`  
		Last Modified: Wed, 03 Mar 2021 23:46:27 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haproxy:2.2-alpine`

```console
$ docker pull haproxy@sha256:4396bf1f43cbeea0f4e2d651b9989685b505d474a347c10855b41dcf49aa7a1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `haproxy:2.2-alpine` - linux; amd64

```console
$ docker pull haproxy@sha256:2f877531092feb1a6596ee8bc6eb00d9d993dab984715d4ce3513805df05aa02
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9177632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2549b4a31f8af89b6bdb4695a4a59374b47fd8b40b8df2f2c20628da267486d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 21:19:54 GMT
ADD file:80bf8bd014071345b1c0364eeb0a5e48f3fb0d87f9c31cb990e57caa652b59b8 in / 
# Wed, 17 Feb 2021 21:19:54 GMT
CMD ["/bin/sh"]
# Mon, 08 Mar 2021 21:38:26 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 21:43:17 GMT
ENV HAPROXY_VERSION=2.2.10
# Mon, 08 Mar 2021 21:43:17 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.10.tar.gz
# Mon, 08 Mar 2021 21:43:17 GMT
ENV HAPROXY_SHA256=a027e9cd8f703ba48dc193f5ae34d9aa152221f67ab58a4e939c96b9f4edd3bc
# Mon, 08 Mar 2021 21:44:18 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Mon, 08 Mar 2021 21:44:18 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 21:44:18 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 21:44:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 08 Mar 2021 21:44:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 21:44:20 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:ba3557a56b150f9b813f9d02274d62914fd8fce120dd374d9ee17b87cf1d277d`  
		Last Modified: Wed, 17 Feb 2021 21:20:25 GMT  
		Size: 2.8 MB (2811657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9216237f12c4d44ab183590086cf2a09004b5609c4b50871d88658faa495245`  
		Last Modified: Mon, 08 Mar 2021 21:52:45 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ab448b61e71513906284c50caa18b4bbead3c9f4e44e9563a51155483cc814`  
		Last Modified: Mon, 08 Mar 2021 21:53:58 GMT  
		Size: 6.4 MB (6364220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1496e8d1fc05d2242dec46f741fd8fb5b7f5f763ff5fe19ac959ef58db7c8c15`  
		Last Modified: Mon, 08 Mar 2021 21:53:46 GMT  
		Size: 448.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c883a4dc2f6239a275129836cd6fe8c66fc9f419c95de34ba15df40807eadd0`  
		Last Modified: Mon, 08 Mar 2021 21:53:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.2-alpine` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:dce2bd7fdb71321a8829f51ee51fe1f8df12ede9854586f628de4bf9b6b390c5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8871339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07e6e2e4dd3516d94cc27ed41c046bad56909aff74a5eebdb69d23185cf56e6e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 20:49:32 GMT
ADD file:c04fbd3b039001c592cfa14f8388f8934ed4223ccf274dbb926e75039e172af4 in / 
# Wed, 17 Feb 2021 20:49:33 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 21:08:27 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 03 Mar 2021 23:53:11 GMT
ENV HAPROXY_VERSION=2.2.10
# Wed, 03 Mar 2021 23:53:13 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.10.tar.gz
# Wed, 03 Mar 2021 23:53:14 GMT
ENV HAPROXY_SHA256=a027e9cd8f703ba48dc193f5ae34d9aa152221f67ab58a4e939c96b9f4edd3bc
# Wed, 03 Mar 2021 23:53:47 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 03 Mar 2021 23:53:48 GMT
STOPSIGNAL SIGUSR1
# Wed, 03 Mar 2021 23:53:49 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 03 Mar 2021 23:53:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 03 Mar 2021 23:53:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Mar 2021 23:53:57 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:1353527ebe111f9bb1e271264a3c182e909e4b36463f80d7dbde1be0713eb892`  
		Last Modified: Wed, 17 Feb 2021 20:50:06 GMT  
		Size: 2.6 MB (2622039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d174378d3ee2c0c6e6a85b5228f929557826d80bcd23b2434093942f499361a7`  
		Last Modified: Wed, 17 Feb 2021 21:12:31 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d92e731bf4971bbb56699109cc2c7bf258a08b8c71fd2ce618628ed0b4be2b1a`  
		Last Modified: Wed, 03 Mar 2021 23:55:11 GMT  
		Size: 6.2 MB (6247545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8313b91724ce11e0d69d1f84cd9ba8ce0fd4dd4784e6deb2c2987413db0b472b`  
		Last Modified: Wed, 03 Mar 2021 23:55:09 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528f6166aa7000e8e0a6ddf712ac1e81bc5ddee4e5003b80a6542ad199662e23`  
		Last Modified: Wed, 03 Mar 2021 23:55:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.2-alpine` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:bd8a4e822b3d304f69ee657b808cc512c82005f7986e37a1b61a8308e14d5ba5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8588802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0035fe4ee0d310975e18c33d050c0fed342d40fc90715c6b91982cb91f1aa0fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 20:57:36 GMT
ADD file:efdd39e5243eaf378f12ad5a85d2222b44930850a90263e5f17e8a6b5e9bc9b8 in / 
# Wed, 17 Feb 2021 20:57:37 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 21:49:42 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Thu, 04 Mar 2021 00:04:07 GMT
ENV HAPROXY_VERSION=2.2.10
# Thu, 04 Mar 2021 00:04:09 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.10.tar.gz
# Thu, 04 Mar 2021 00:04:12 GMT
ENV HAPROXY_SHA256=a027e9cd8f703ba48dc193f5ae34d9aa152221f67ab58a4e939c96b9f4edd3bc
# Thu, 04 Mar 2021 00:04:46 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Thu, 04 Mar 2021 00:04:47 GMT
STOPSIGNAL SIGUSR1
# Thu, 04 Mar 2021 00:04:49 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Thu, 04 Mar 2021 00:04:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 04 Mar 2021 00:04:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 00:04:55 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f55b840e27d3dbe27e44497103a4397f043749f933eb0433d29e2f104b3435ef`  
		Last Modified: Wed, 17 Feb 2021 20:58:14 GMT  
		Size: 2.4 MB (2423892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86398e5ccaeed703d9464d57f2d97546fad0481312144292414eb1cf857b617f`  
		Last Modified: Wed, 17 Feb 2021 21:55:00 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00ad0cba7b2138c19356311eceb6fd5d2af2432778f97cf07d9b384d5524278`  
		Last Modified: Thu, 04 Mar 2021 00:07:00 GMT  
		Size: 6.2 MB (6163153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b337734f16cc0eff0d2bb38d7431f457cd7992e4992f77789263d6611d7e407b`  
		Last Modified: Thu, 04 Mar 2021 00:06:58 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb03a37f226d57efe43f03eb956ef49a20693dc865f15de068de3f08e6c56aba`  
		Last Modified: Thu, 04 Mar 2021 00:06:58 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.2-alpine` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:9df40d9acef87692f82a74b70ce1d60af5cca36f61239d82d12433ed0af482d8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9083113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e914a0cee60954b5adb34a5fd43d3fa4698fb1e4747afcaca9006dbc9e6c4cf2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 20:39:29 GMT
ADD file:3bf1497bd250cf7c73c12231dc4ebe3a3a67f2cd99e35bce47ef6674683aeb1d in / 
# Wed, 17 Feb 2021 20:39:30 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 21:36:08 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 03 Mar 2021 23:43:05 GMT
ENV HAPROXY_VERSION=2.2.10
# Wed, 03 Mar 2021 23:43:06 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.10.tar.gz
# Wed, 03 Mar 2021 23:43:07 GMT
ENV HAPROXY_SHA256=a027e9cd8f703ba48dc193f5ae34d9aa152221f67ab58a4e939c96b9f4edd3bc
# Wed, 03 Mar 2021 23:43:29 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 03 Mar 2021 23:43:30 GMT
STOPSIGNAL SIGUSR1
# Wed, 03 Mar 2021 23:43:31 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 03 Mar 2021 23:43:33 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 03 Mar 2021 23:43:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Mar 2021 23:43:35 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:069a56d6d07f6b186fbb82e4486616b9be9a37ce32a63013af6cddcb65898182`  
		Last Modified: Wed, 17 Feb 2021 20:40:04 GMT  
		Size: 2.7 MB (2711572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6644620fa9074da825714fc7794756e2b0e36f3e83ffc2bc01bbc9df0de9e373`  
		Last Modified: Wed, 17 Feb 2021 21:41:18 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a59369a058df1f7b291ab7b129ef07290c2a99545bea6f42cfa0f54436183bb`  
		Last Modified: Wed, 03 Mar 2021 23:45:22 GMT  
		Size: 6.4 MB (6369785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e982f4480ea14efe8106105e56424bc6bee3368b3299cd98b1aad1e5609140`  
		Last Modified: Wed, 03 Mar 2021 23:45:20 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffebf1b2b70d66bcbda9707eb957d0e25635210167d94d991cc7e81130ded334`  
		Last Modified: Wed, 03 Mar 2021 23:45:20 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.2-alpine` - linux; 386

```console
$ docker pull haproxy@sha256:659a38f29b31e96bd5aecab83a003f3f09e1eb5eebd43d6169b02ac77d8ed7be
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9012210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c724357a8f8f4b645b234f5584c0748d1a8db582d156e91d506d5574ccf1b2ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 21:38:34 GMT
ADD file:eaee53da3c87749799de55809e4a5b526c56855332b961a85b1184c660f1d65b in / 
# Wed, 17 Feb 2021 21:38:35 GMT
CMD ["/bin/sh"]
# Mon, 08 Mar 2021 22:03:53 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 22:08:22 GMT
ENV HAPROXY_VERSION=2.2.10
# Mon, 08 Mar 2021 22:08:22 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.10.tar.gz
# Mon, 08 Mar 2021 22:08:22 GMT
ENV HAPROXY_SHA256=a027e9cd8f703ba48dc193f5ae34d9aa152221f67ab58a4e939c96b9f4edd3bc
# Mon, 08 Mar 2021 22:09:21 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Mon, 08 Mar 2021 22:09:21 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 22:09:21 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 22:09:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 08 Mar 2021 22:09:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 22:09:23 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:86205afa28f6bc624469015a543d16608258d2828411a92c662f4fdc6d276e18`  
		Last Modified: Wed, 17 Feb 2021 21:39:07 GMT  
		Size: 2.8 MB (2818177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080e85d941540171ac6a020af17b393f2a40b03d40b9677d708d31ffb6e31b71`  
		Last Modified: Mon, 08 Mar 2021 22:18:02 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dafe934780af9f6588fe0b199a4c0b60e557597c52ed66de79f143c33b9f40c`  
		Last Modified: Mon, 08 Mar 2021 22:19:06 GMT  
		Size: 6.2 MB (6192281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6792eb8d4ba43ae0b592f09026d5cc688e72235dc893697be4e2b5c446409863`  
		Last Modified: Mon, 08 Mar 2021 22:19:04 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:682c8c2e4bc6bc83b8e4eea6ff73da639b17e212f85d36a5407aadb8a64f9024`  
		Last Modified: Mon, 08 Mar 2021 22:19:04 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.2-alpine` - linux; ppc64le

```console
$ docker pull haproxy@sha256:7c55559ea5e08f971f817d05e45bb569929812dd49110cc075bde9c0c74fbf8b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9496257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fa09275b3a555d9d28aca6380470a700262bc2fa9550d6cceefe3327d8299af`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 21:17:29 GMT
ADD file:28f4377c61c0f8eb43a6b36e6a24ef5893f51d405d25b62e364988223537ae0b in / 
# Wed, 17 Feb 2021 21:17:37 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 22:10:46 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 03 Mar 2021 23:29:05 GMT
ENV HAPROXY_VERSION=2.2.10
# Wed, 03 Mar 2021 23:29:08 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.10.tar.gz
# Wed, 03 Mar 2021 23:29:12 GMT
ENV HAPROXY_SHA256=a027e9cd8f703ba48dc193f5ae34d9aa152221f67ab58a4e939c96b9f4edd3bc
# Wed, 03 Mar 2021 23:29:57 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 03 Mar 2021 23:30:06 GMT
STOPSIGNAL SIGUSR1
# Wed, 03 Mar 2021 23:30:07 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 03 Mar 2021 23:30:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 03 Mar 2021 23:30:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Mar 2021 23:30:34 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:cb672e0375a8f9bb3d33049ceb372ffa49b959bfc84fe6f72bfb97b682a608c8`  
		Last Modified: Wed, 17 Feb 2021 21:18:10 GMT  
		Size: 2.8 MB (2813081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f391a7d74b9bf5c2089e7957996d00d99ddc33d8295873bf28746716bb728a`  
		Last Modified: Wed, 17 Feb 2021 22:23:02 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3895621bf409c59caef35106ecb9c73d57db6ab26c83e908bb2f846ce3b2420e`  
		Last Modified: Wed, 03 Mar 2021 23:32:35 GMT  
		Size: 6.7 MB (6681415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a16f70021d25609a108a39f41eff539ab12df1aba78f8d87564a9022864f65d`  
		Last Modified: Wed, 03 Mar 2021 23:32:34 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67bc8b05d75cf8717f438ad79f81f009294c601e828c4cbd406b08d167bd4f80`  
		Last Modified: Wed, 03 Mar 2021 23:32:34 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.2-alpine` - linux; s390x

```console
$ docker pull haproxy@sha256:5882e4526d054b2db8cdc8b0478d1a2b56273796af2dcc87c2fcd3b9b38f0dcf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8934271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97f0501dfe1a6477b450f2c11dc0f5c7db80bea48457a4de575e5798fd920abe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 20:41:27 GMT
ADD file:630c66f8d774d75b51e32aff812b438d377ebd3389c4aa6c324fdf8c03b6fa13 in / 
# Wed, 17 Feb 2021 20:41:27 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 21:33:33 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 03 Mar 2021 23:44:04 GMT
ENV HAPROXY_VERSION=2.2.10
# Wed, 03 Mar 2021 23:44:04 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.10.tar.gz
# Wed, 03 Mar 2021 23:44:05 GMT
ENV HAPROXY_SHA256=a027e9cd8f703ba48dc193f5ae34d9aa152221f67ab58a4e939c96b9f4edd3bc
# Wed, 03 Mar 2021 23:44:42 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 03 Mar 2021 23:44:43 GMT
STOPSIGNAL SIGUSR1
# Wed, 03 Mar 2021 23:44:43 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 03 Mar 2021 23:44:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 03 Mar 2021 23:44:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Mar 2021 23:44:44 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:ff5e8cb87555e9fa38a441f5cf0414e91353e2cd21cdb48d48b7de5bb39ce674`  
		Last Modified: Wed, 17 Feb 2021 20:41:58 GMT  
		Size: 2.6 MB (2602381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de25a3a0de168e6603cb978691ef3e7f11d7c9108d0ade38d3185d5d9dbdc094`  
		Last Modified: Wed, 17 Feb 2021 21:43:59 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc37ee0272550cdbed16f03b4d75571d970685b3a0c7b8d29484c919d8a9705`  
		Last Modified: Wed, 03 Mar 2021 23:46:27 GMT  
		Size: 6.3 MB (6330135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36a50696ff802571b01c8fa6b843837fc6b5e23d4948b2b73404ce94b9fa2ee`  
		Last Modified: Wed, 03 Mar 2021 23:46:26 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5abb15abe9d69125c600f2786dc4197578896c9d134fc5233bbbfcbcd125744`  
		Last Modified: Wed, 03 Mar 2021 23:46:27 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haproxy:2.3`

```console
$ docker pull haproxy@sha256:3214ebf1267b178440a327cbb5c6167b65c22a6dd64a56f25fbace986757300f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `haproxy:2.3` - linux; amd64

```console
$ docker pull haproxy@sha256:586ed760a5a2f7c662a0c0c6499ba4deee11caea609aaba3c5a381d75b3df61f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36767363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4e151b1aac28b63489aae6e912ce76d98fef88f6573f88d548dd2d54f9ca5d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Mon, 08 Mar 2021 21:37:25 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 21:39:38 GMT
ENV HAPROXY_VERSION=2.3.6
# Mon, 08 Mar 2021 21:39:38 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.6.tar.gz
# Mon, 08 Mar 2021 21:39:38 GMT
ENV HAPROXY_SHA256=6d4620e5da1d93ed75f229011216db81d5097b68bf175e309f2fab2890bba036
# Mon, 08 Mar 2021 21:40:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 08 Mar 2021 21:40:39 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 21:40:40 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 21:40:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 08 Mar 2021 21:40:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 21:40:41 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7bca45a971fe608786870ce75c9976f8e5a958f55e1287a6120048b897c63b6`  
		Last Modified: Mon, 08 Mar 2021 21:52:33 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9de78517be39f734e7e1882b46afaea8cdb7ce9a0b3f7665a3a0e33a658fbaa`  
		Last Modified: Mon, 08 Mar 2021 21:52:59 GMT  
		Size: 9.7 MB (9670271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b4c22e4f7cc999fa3fefe75b56d996159c8b4190b98b7b36d80a0e5e24caad2`  
		Last Modified: Mon, 08 Mar 2021 21:52:57 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43c239ac2f6da77003db0b8d9bee46a28e2ef72974b205d843b7de6411daef69`  
		Last Modified: Mon, 08 Mar 2021 21:52:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.3` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:fd160acb019b9cee4334606628c1835a3c2a55cdaf157b622cd772058f0b7663
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.1 MB (34126380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef626ed9cf808dab1b3f6f9fc89cc41094363728e62d88eceaa7c8bdd39ab4a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:50:10 GMT
ADD file:fbd00ef7871dc27d7ed5fa8c238cdc80652bd87b8033be7de9e54a799bbf10a4 in / 
# Tue, 09 Feb 2021 02:50:11 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:45:24 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 03 Mar 2021 23:48:37 GMT
ENV HAPROXY_VERSION=2.3.6
# Wed, 03 Mar 2021 23:48:39 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.6.tar.gz
# Wed, 03 Mar 2021 23:48:40 GMT
ENV HAPROXY_SHA256=6d4620e5da1d93ed75f229011216db81d5097b68bf175e309f2fab2890bba036
# Wed, 03 Mar 2021 23:49:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 Mar 2021 23:49:42 GMT
STOPSIGNAL SIGUSR1
# Wed, 03 Mar 2021 23:49:43 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 03 Mar 2021 23:49:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 03 Mar 2021 23:49:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Mar 2021 23:49:46 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:8e683fcc73f4da7d69ce1d5f4e1d77510aa459490068f38db2d8663698b391a0`  
		Last Modified: Tue, 09 Feb 2021 02:59:07 GMT  
		Size: 24.8 MB (24839297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def565d52deae74587a55f60d168bd531ebe8095c594027b7057a8fc1be0e8af`  
		Last Modified: Tue, 09 Feb 2021 03:54:54 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fff3e31705a444ba58f6fedc10fd7e8509560df170ce2a6464e3c7c680f5512`  
		Last Modified: Wed, 03 Mar 2021 23:52:53 GMT  
		Size: 9.3 MB (9285141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:302d9907c27970d03ed0ac50d978a7ec92b9627bd8dfe895d0ce38c29ff8abae`  
		Last Modified: Wed, 03 Mar 2021 23:52:48 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d9fe9f8f082ead91dcc43c0af3b0ce2eec1e43e565420891144646e2e66c0bc`  
		Last Modified: Wed, 03 Mar 2021 23:52:47 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.3` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:22739469108f3026eb1cc7566b171ad09e6baf29d82ecfe6971acb8b1d390ec6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31800938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e24a61c6cff6c522f2e6dc8dc2eefb1283b754cef79e8fc718bc2e851d64dff4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 03:00:57 GMT
ADD file:e675d50366bde57173a75f9a29367d765e7da2b7254c5254b64e777cf6870502 in / 
# Tue, 09 Feb 2021 03:01:00 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:49:38 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 03 Mar 2021 23:59:53 GMT
ENV HAPROXY_VERSION=2.3.6
# Wed, 03 Mar 2021 23:59:55 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.6.tar.gz
# Wed, 03 Mar 2021 23:59:57 GMT
ENV HAPROXY_SHA256=6d4620e5da1d93ed75f229011216db81d5097b68bf175e309f2fab2890bba036
# Thu, 04 Mar 2021 00:00:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 04 Mar 2021 00:00:45 GMT
STOPSIGNAL SIGUSR1
# Thu, 04 Mar 2021 00:00:48 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Thu, 04 Mar 2021 00:00:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 04 Mar 2021 00:00:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 00:00:56 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:db574d82360c3b60abadbef4f3daf8dee01f24741fc6ab3692aa543558d8b624`  
		Last Modified: Tue, 09 Feb 2021 03:09:46 GMT  
		Size: 22.7 MB (22703384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9978ebb1881387f11e025fb46dce2b3c715f705f6d240737574f8848c27fa0d7`  
		Last Modified: Tue, 09 Feb 2021 03:58:16 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9b042e3b0a9b457749c8b6be38159bf336900ac0a449ef7837355b905d54513`  
		Last Modified: Thu, 04 Mar 2021 00:06:28 GMT  
		Size: 9.1 MB (9095610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cb11dc12989b181df9b197123d5c719e0263ed7a7dd62a319b386a262407e5c`  
		Last Modified: Thu, 04 Mar 2021 00:06:22 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45586ab18fd80a8fca25174c46c6093922dcbd4130cd774955373136fb442bcc`  
		Last Modified: Thu, 04 Mar 2021 00:06:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.3` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:fb7ce8e18b0ce77f8541295869bf9addf4f39936e606fb2f95fd60f183820553
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 MB (35345046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:149902bcb92ba5cbb82706a611dfcee896c375e4d9ea66fe4d6a73359d1af05b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:41:10 GMT
ADD file:d906dedaf14d8e3874b46787f7a1dbf268bc124c4e1dd32f13f3079e12f22238 in / 
# Tue, 09 Feb 2021 02:41:13 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:59:41 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 03 Mar 2021 23:40:11 GMT
ENV HAPROXY_VERSION=2.3.6
# Wed, 03 Mar 2021 23:40:12 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.6.tar.gz
# Wed, 03 Mar 2021 23:40:13 GMT
ENV HAPROXY_SHA256=6d4620e5da1d93ed75f229011216db81d5097b68bf175e309f2fab2890bba036
# Wed, 03 Mar 2021 23:40:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 Mar 2021 23:40:54 GMT
STOPSIGNAL SIGUSR1
# Wed, 03 Mar 2021 23:40:55 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 03 Mar 2021 23:40:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 03 Mar 2021 23:40:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Mar 2021 23:40:58 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:83c5cfdaa5385ea6fc4d31e724fd4dc5d74de847a7bdd968555b8f2c558dac0e`  
		Last Modified: Tue, 09 Feb 2021 02:47:27 GMT  
		Size: 25.9 MB (25851449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b7f43dd52365bce2c2b75f29577aa39d2b5794e2561cddc0678422ffc1f7d15`  
		Last Modified: Tue, 09 Feb 2021 04:08:36 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab089d5e39e2bee9f1457db0064c673f2197022e4f35bd09866546237fcce328`  
		Last Modified: Wed, 03 Mar 2021 23:44:50 GMT  
		Size: 9.5 MB (9491653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bca2e6c325b028c12e42ea4e7d6d92b0db82199b38df988fcb4e62cefe820bb`  
		Last Modified: Wed, 03 Mar 2021 23:44:48 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48adef33c780445a2435d0b2c14556b53b34fc9ca5795864b6c3cbc7cc4b25d6`  
		Last Modified: Wed, 03 Mar 2021 23:44:48 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.3` - linux; 386

```console
$ docker pull haproxy@sha256:08029dd29e3f4a419baf0ece22ad92d46b2f27ce01cec80f4859d2492f13c0b8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 MB (37318546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1457ecba48f46c6e0909e9a34ff886af1fd3b5a35c05286c03d3f4da1456539b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:39:47 GMT
ADD file:61c31b1037672781ed0ecbc080ee3d49c83af49f5578b011544513fa9625698d in / 
# Tue, 09 Feb 2021 02:39:47 GMT
CMD ["bash"]
# Mon, 08 Mar 2021 22:02:40 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 22:05:06 GMT
ENV HAPROXY_VERSION=2.3.6
# Mon, 08 Mar 2021 22:05:06 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.6.tar.gz
# Mon, 08 Mar 2021 22:05:06 GMT
ENV HAPROXY_SHA256=6d4620e5da1d93ed75f229011216db81d5097b68bf175e309f2fab2890bba036
# Mon, 08 Mar 2021 22:05:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 08 Mar 2021 22:05:57 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 22:05:57 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 22:05:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 08 Mar 2021 22:05:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 22:05:58 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:27cbb00346a16ea900c1049a2e5b47942c586c377179e098382c8ca1c8e87966`  
		Last Modified: Tue, 09 Feb 2021 02:45:51 GMT  
		Size: 27.8 MB (27752731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b6129a97a33727ea8a598d1e797bccce491920bf29d769880cf2fc6d3e0436`  
		Last Modified: Mon, 08 Mar 2021 22:17:48 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66fc7f55bb52d577bb49216caae38e742ba182d2719615fd195125099570f183`  
		Last Modified: Mon, 08 Mar 2021 22:18:17 GMT  
		Size: 9.6 MB (9563873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91893e7877fd0573b74c92a13310c45ca6568bbfc3b61cadce60a54553812896`  
		Last Modified: Mon, 08 Mar 2021 22:18:14 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14935bdf9a0768984c33b8ba5f706939f3133106b3412589747e11f46a54221`  
		Last Modified: Mon, 08 Mar 2021 22:18:15 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.3` - linux; mips64le

```console
$ docker pull haproxy@sha256:f047f58d1b05f146259a460b5534d4f371a3bfd8a5adeb09a04276656fa00af0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 MB (35014317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc7140e196cccbd6502dc6775c8fa25da1dea923c269c4fa57aec0831eb87b8f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 03:09:26 GMT
ADD file:0222a151f4e5033d9eae98ce2b703a63f52d049dd72ac40bdd0dc2dafe619f0a in / 
# Tue, 09 Feb 2021 03:09:27 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:41:09 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 03 Mar 2021 23:07:23 GMT
ENV HAPROXY_VERSION=2.3.6
# Wed, 03 Mar 2021 23:07:23 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.6.tar.gz
# Wed, 03 Mar 2021 23:07:23 GMT
ENV HAPROXY_SHA256=6d4620e5da1d93ed75f229011216db81d5097b68bf175e309f2fab2890bba036
# Wed, 03 Mar 2021 23:09:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 Mar 2021 23:09:49 GMT
STOPSIGNAL SIGUSR1
# Wed, 03 Mar 2021 23:09:49 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 03 Mar 2021 23:09:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 03 Mar 2021 23:09:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Mar 2021 23:09:52 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:dfb81134097d874e01b495d1fba82e384056d0a3a45f01a69a2e86ae82af1e96`  
		Last Modified: Tue, 09 Feb 2021 03:15:55 GMT  
		Size: 25.8 MB (25764640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a549d56662447dd8cb15faf59ca0fc2eda7a877e9aee16aadd09fd46e4214a`  
		Last Modified: Tue, 09 Feb 2021 03:57:56 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fd84d34b65468db17bc6bb2cb72cc70ef09422490d888737d7c029ec4d8e344`  
		Last Modified: Wed, 03 Mar 2021 23:13:19 GMT  
		Size: 9.2 MB (9247729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a561995add47ef6d0a089710e967ccabeaf9d9a416be3e03be23ef058b4834`  
		Last Modified: Wed, 03 Mar 2021 23:13:09 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0499d598e07691795e195c0d80a2dbf4807859d41722ba9689117269d2c452f4`  
		Last Modified: Wed, 03 Mar 2021 23:13:09 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.3` - linux; ppc64le

```console
$ docker pull haproxy@sha256:741a0dc67c8b115376f867d987bc1d9a4bc90619a4939074c94ce0cd1defbd89
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.7 MB (40679819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ce2f4a27a4c4caea7672c616fe0801ca3902d1d571793e66f1158d9ace20952`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:19:19 GMT
ADD file:9a8cfdf0eab394a693b5cde0700ad47b6e8506ef0b79fabb8a07874b96e6c394 in / 
# Tue, 09 Feb 2021 02:19:34 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 05:52:23 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 03 Mar 2021 23:16:59 GMT
ENV HAPROXY_VERSION=2.3.6
# Wed, 03 Mar 2021 23:17:02 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.6.tar.gz
# Wed, 03 Mar 2021 23:17:07 GMT
ENV HAPROXY_SHA256=6d4620e5da1d93ed75f229011216db81d5097b68bf175e309f2fab2890bba036
# Wed, 03 Mar 2021 23:21:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 Mar 2021 23:21:21 GMT
STOPSIGNAL SIGUSR1
# Wed, 03 Mar 2021 23:21:24 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 03 Mar 2021 23:21:36 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 03 Mar 2021 23:21:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Mar 2021 23:21:43 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:9996b4fb6bc1c50f95ba30f8988c9c89526556fa320d3fda59d3d8359f7810d6`  
		Last Modified: Tue, 09 Feb 2021 02:27:59 GMT  
		Size: 30.5 MB (30519509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7f600bc4989eb9f12d5006a73f5958eb4fe85f86bc4008d7a899bb935b0f1c`  
		Last Modified: Tue, 09 Feb 2021 06:38:36 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f996cf993595d7dfaa53dd8b2756f38db1c17c7fd9711ac10dc4191cec786d60`  
		Last Modified: Wed, 03 Mar 2021 23:31:40 GMT  
		Size: 10.2 MB (10158363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7991881f420b992a3223335c3213fc329c88dffe0516c57bf925f34dd2783fe`  
		Last Modified: Wed, 03 Mar 2021 23:31:37 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51f9d3ebe569638afe6c4bad4532d993022b91325ea88fafc3a593a4d0c8848d`  
		Last Modified: Wed, 03 Mar 2021 23:31:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.3` - linux; s390x

```console
$ docker pull haproxy@sha256:7caad1df1cc08ce7f758568a4a2fb426d700c62c3dc78d0041de32e5d57477bc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.1 MB (35093083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3cdecbc4babbecaa160b39e9ef4bd2cc182628cb8bce7bfdd24d2f91c10bd48`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:42:10 GMT
ADD file:0edb2de05df54191a141bd125f59d7e14eef0cc4576927a247b8dd7d6f255d04 in / 
# Tue, 09 Feb 2021 02:42:12 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:39:30 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 03 Mar 2021 23:41:38 GMT
ENV HAPROXY_VERSION=2.3.6
# Wed, 03 Mar 2021 23:41:38 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.6.tar.gz
# Wed, 03 Mar 2021 23:41:39 GMT
ENV HAPROXY_SHA256=6d4620e5da1d93ed75f229011216db81d5097b68bf175e309f2fab2890bba036
# Wed, 03 Mar 2021 23:42:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 Mar 2021 23:42:19 GMT
STOPSIGNAL SIGUSR1
# Wed, 03 Mar 2021 23:42:19 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 03 Mar 2021 23:42:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 03 Mar 2021 23:42:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Mar 2021 23:42:21 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:032413a44cf56b097e48b8221bf475ca1bec26e7a27f35fe61d699366a335b79`  
		Last Modified: Tue, 09 Feb 2021 02:45:31 GMT  
		Size: 25.7 MB (25710021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e65f701864562492efa2c0035134b62d68efdb6e7241a0a2dcc3151e6d5775b`  
		Last Modified: Tue, 09 Feb 2021 03:44:28 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62fc0238f1fd6fa72a0d48c70d25c0223d69ee003d98edc91896d34a78569752`  
		Last Modified: Wed, 03 Mar 2021 23:45:58 GMT  
		Size: 9.4 MB (9381115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a706369cf995e0ac6dc64e80d0aa1273c88faef770d5525485b9be6b982dafa`  
		Last Modified: Wed, 03 Mar 2021 23:45:54 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bac4428d8a67f044ee63239ab25919c550a35aefffd9dcd18e8dea892fba0a42`  
		Last Modified: Wed, 03 Mar 2021 23:45:54 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haproxy:2.3.6`

```console
$ docker pull haproxy@sha256:3214ebf1267b178440a327cbb5c6167b65c22a6dd64a56f25fbace986757300f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `haproxy:2.3.6` - linux; amd64

```console
$ docker pull haproxy@sha256:586ed760a5a2f7c662a0c0c6499ba4deee11caea609aaba3c5a381d75b3df61f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36767363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4e151b1aac28b63489aae6e912ce76d98fef88f6573f88d548dd2d54f9ca5d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Mon, 08 Mar 2021 21:37:25 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 21:39:38 GMT
ENV HAPROXY_VERSION=2.3.6
# Mon, 08 Mar 2021 21:39:38 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.6.tar.gz
# Mon, 08 Mar 2021 21:39:38 GMT
ENV HAPROXY_SHA256=6d4620e5da1d93ed75f229011216db81d5097b68bf175e309f2fab2890bba036
# Mon, 08 Mar 2021 21:40:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 08 Mar 2021 21:40:39 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 21:40:40 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 21:40:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 08 Mar 2021 21:40:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 21:40:41 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7bca45a971fe608786870ce75c9976f8e5a958f55e1287a6120048b897c63b6`  
		Last Modified: Mon, 08 Mar 2021 21:52:33 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9de78517be39f734e7e1882b46afaea8cdb7ce9a0b3f7665a3a0e33a658fbaa`  
		Last Modified: Mon, 08 Mar 2021 21:52:59 GMT  
		Size: 9.7 MB (9670271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b4c22e4f7cc999fa3fefe75b56d996159c8b4190b98b7b36d80a0e5e24caad2`  
		Last Modified: Mon, 08 Mar 2021 21:52:57 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43c239ac2f6da77003db0b8d9bee46a28e2ef72974b205d843b7de6411daef69`  
		Last Modified: Mon, 08 Mar 2021 21:52:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.3.6` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:fd160acb019b9cee4334606628c1835a3c2a55cdaf157b622cd772058f0b7663
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.1 MB (34126380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef626ed9cf808dab1b3f6f9fc89cc41094363728e62d88eceaa7c8bdd39ab4a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:50:10 GMT
ADD file:fbd00ef7871dc27d7ed5fa8c238cdc80652bd87b8033be7de9e54a799bbf10a4 in / 
# Tue, 09 Feb 2021 02:50:11 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:45:24 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 03 Mar 2021 23:48:37 GMT
ENV HAPROXY_VERSION=2.3.6
# Wed, 03 Mar 2021 23:48:39 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.6.tar.gz
# Wed, 03 Mar 2021 23:48:40 GMT
ENV HAPROXY_SHA256=6d4620e5da1d93ed75f229011216db81d5097b68bf175e309f2fab2890bba036
# Wed, 03 Mar 2021 23:49:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 Mar 2021 23:49:42 GMT
STOPSIGNAL SIGUSR1
# Wed, 03 Mar 2021 23:49:43 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 03 Mar 2021 23:49:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 03 Mar 2021 23:49:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Mar 2021 23:49:46 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:8e683fcc73f4da7d69ce1d5f4e1d77510aa459490068f38db2d8663698b391a0`  
		Last Modified: Tue, 09 Feb 2021 02:59:07 GMT  
		Size: 24.8 MB (24839297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def565d52deae74587a55f60d168bd531ebe8095c594027b7057a8fc1be0e8af`  
		Last Modified: Tue, 09 Feb 2021 03:54:54 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fff3e31705a444ba58f6fedc10fd7e8509560df170ce2a6464e3c7c680f5512`  
		Last Modified: Wed, 03 Mar 2021 23:52:53 GMT  
		Size: 9.3 MB (9285141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:302d9907c27970d03ed0ac50d978a7ec92b9627bd8dfe895d0ce38c29ff8abae`  
		Last Modified: Wed, 03 Mar 2021 23:52:48 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d9fe9f8f082ead91dcc43c0af3b0ce2eec1e43e565420891144646e2e66c0bc`  
		Last Modified: Wed, 03 Mar 2021 23:52:47 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.3.6` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:22739469108f3026eb1cc7566b171ad09e6baf29d82ecfe6971acb8b1d390ec6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31800938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e24a61c6cff6c522f2e6dc8dc2eefb1283b754cef79e8fc718bc2e851d64dff4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 03:00:57 GMT
ADD file:e675d50366bde57173a75f9a29367d765e7da2b7254c5254b64e777cf6870502 in / 
# Tue, 09 Feb 2021 03:01:00 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:49:38 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 03 Mar 2021 23:59:53 GMT
ENV HAPROXY_VERSION=2.3.6
# Wed, 03 Mar 2021 23:59:55 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.6.tar.gz
# Wed, 03 Mar 2021 23:59:57 GMT
ENV HAPROXY_SHA256=6d4620e5da1d93ed75f229011216db81d5097b68bf175e309f2fab2890bba036
# Thu, 04 Mar 2021 00:00:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 04 Mar 2021 00:00:45 GMT
STOPSIGNAL SIGUSR1
# Thu, 04 Mar 2021 00:00:48 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Thu, 04 Mar 2021 00:00:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 04 Mar 2021 00:00:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 00:00:56 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:db574d82360c3b60abadbef4f3daf8dee01f24741fc6ab3692aa543558d8b624`  
		Last Modified: Tue, 09 Feb 2021 03:09:46 GMT  
		Size: 22.7 MB (22703384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9978ebb1881387f11e025fb46dce2b3c715f705f6d240737574f8848c27fa0d7`  
		Last Modified: Tue, 09 Feb 2021 03:58:16 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9b042e3b0a9b457749c8b6be38159bf336900ac0a449ef7837355b905d54513`  
		Last Modified: Thu, 04 Mar 2021 00:06:28 GMT  
		Size: 9.1 MB (9095610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cb11dc12989b181df9b197123d5c719e0263ed7a7dd62a319b386a262407e5c`  
		Last Modified: Thu, 04 Mar 2021 00:06:22 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45586ab18fd80a8fca25174c46c6093922dcbd4130cd774955373136fb442bcc`  
		Last Modified: Thu, 04 Mar 2021 00:06:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.3.6` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:fb7ce8e18b0ce77f8541295869bf9addf4f39936e606fb2f95fd60f183820553
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 MB (35345046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:149902bcb92ba5cbb82706a611dfcee896c375e4d9ea66fe4d6a73359d1af05b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:41:10 GMT
ADD file:d906dedaf14d8e3874b46787f7a1dbf268bc124c4e1dd32f13f3079e12f22238 in / 
# Tue, 09 Feb 2021 02:41:13 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:59:41 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 03 Mar 2021 23:40:11 GMT
ENV HAPROXY_VERSION=2.3.6
# Wed, 03 Mar 2021 23:40:12 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.6.tar.gz
# Wed, 03 Mar 2021 23:40:13 GMT
ENV HAPROXY_SHA256=6d4620e5da1d93ed75f229011216db81d5097b68bf175e309f2fab2890bba036
# Wed, 03 Mar 2021 23:40:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 Mar 2021 23:40:54 GMT
STOPSIGNAL SIGUSR1
# Wed, 03 Mar 2021 23:40:55 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 03 Mar 2021 23:40:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 03 Mar 2021 23:40:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Mar 2021 23:40:58 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:83c5cfdaa5385ea6fc4d31e724fd4dc5d74de847a7bdd968555b8f2c558dac0e`  
		Last Modified: Tue, 09 Feb 2021 02:47:27 GMT  
		Size: 25.9 MB (25851449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b7f43dd52365bce2c2b75f29577aa39d2b5794e2561cddc0678422ffc1f7d15`  
		Last Modified: Tue, 09 Feb 2021 04:08:36 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab089d5e39e2bee9f1457db0064c673f2197022e4f35bd09866546237fcce328`  
		Last Modified: Wed, 03 Mar 2021 23:44:50 GMT  
		Size: 9.5 MB (9491653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bca2e6c325b028c12e42ea4e7d6d92b0db82199b38df988fcb4e62cefe820bb`  
		Last Modified: Wed, 03 Mar 2021 23:44:48 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48adef33c780445a2435d0b2c14556b53b34fc9ca5795864b6c3cbc7cc4b25d6`  
		Last Modified: Wed, 03 Mar 2021 23:44:48 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.3.6` - linux; 386

```console
$ docker pull haproxy@sha256:08029dd29e3f4a419baf0ece22ad92d46b2f27ce01cec80f4859d2492f13c0b8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 MB (37318546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1457ecba48f46c6e0909e9a34ff886af1fd3b5a35c05286c03d3f4da1456539b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:39:47 GMT
ADD file:61c31b1037672781ed0ecbc080ee3d49c83af49f5578b011544513fa9625698d in / 
# Tue, 09 Feb 2021 02:39:47 GMT
CMD ["bash"]
# Mon, 08 Mar 2021 22:02:40 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 22:05:06 GMT
ENV HAPROXY_VERSION=2.3.6
# Mon, 08 Mar 2021 22:05:06 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.6.tar.gz
# Mon, 08 Mar 2021 22:05:06 GMT
ENV HAPROXY_SHA256=6d4620e5da1d93ed75f229011216db81d5097b68bf175e309f2fab2890bba036
# Mon, 08 Mar 2021 22:05:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 08 Mar 2021 22:05:57 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 22:05:57 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 22:05:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 08 Mar 2021 22:05:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 22:05:58 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:27cbb00346a16ea900c1049a2e5b47942c586c377179e098382c8ca1c8e87966`  
		Last Modified: Tue, 09 Feb 2021 02:45:51 GMT  
		Size: 27.8 MB (27752731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b6129a97a33727ea8a598d1e797bccce491920bf29d769880cf2fc6d3e0436`  
		Last Modified: Mon, 08 Mar 2021 22:17:48 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66fc7f55bb52d577bb49216caae38e742ba182d2719615fd195125099570f183`  
		Last Modified: Mon, 08 Mar 2021 22:18:17 GMT  
		Size: 9.6 MB (9563873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91893e7877fd0573b74c92a13310c45ca6568bbfc3b61cadce60a54553812896`  
		Last Modified: Mon, 08 Mar 2021 22:18:14 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14935bdf9a0768984c33b8ba5f706939f3133106b3412589747e11f46a54221`  
		Last Modified: Mon, 08 Mar 2021 22:18:15 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.3.6` - linux; mips64le

```console
$ docker pull haproxy@sha256:f047f58d1b05f146259a460b5534d4f371a3bfd8a5adeb09a04276656fa00af0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 MB (35014317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc7140e196cccbd6502dc6775c8fa25da1dea923c269c4fa57aec0831eb87b8f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 03:09:26 GMT
ADD file:0222a151f4e5033d9eae98ce2b703a63f52d049dd72ac40bdd0dc2dafe619f0a in / 
# Tue, 09 Feb 2021 03:09:27 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:41:09 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 03 Mar 2021 23:07:23 GMT
ENV HAPROXY_VERSION=2.3.6
# Wed, 03 Mar 2021 23:07:23 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.6.tar.gz
# Wed, 03 Mar 2021 23:07:23 GMT
ENV HAPROXY_SHA256=6d4620e5da1d93ed75f229011216db81d5097b68bf175e309f2fab2890bba036
# Wed, 03 Mar 2021 23:09:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 Mar 2021 23:09:49 GMT
STOPSIGNAL SIGUSR1
# Wed, 03 Mar 2021 23:09:49 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 03 Mar 2021 23:09:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 03 Mar 2021 23:09:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Mar 2021 23:09:52 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:dfb81134097d874e01b495d1fba82e384056d0a3a45f01a69a2e86ae82af1e96`  
		Last Modified: Tue, 09 Feb 2021 03:15:55 GMT  
		Size: 25.8 MB (25764640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a549d56662447dd8cb15faf59ca0fc2eda7a877e9aee16aadd09fd46e4214a`  
		Last Modified: Tue, 09 Feb 2021 03:57:56 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fd84d34b65468db17bc6bb2cb72cc70ef09422490d888737d7c029ec4d8e344`  
		Last Modified: Wed, 03 Mar 2021 23:13:19 GMT  
		Size: 9.2 MB (9247729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a561995add47ef6d0a089710e967ccabeaf9d9a416be3e03be23ef058b4834`  
		Last Modified: Wed, 03 Mar 2021 23:13:09 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0499d598e07691795e195c0d80a2dbf4807859d41722ba9689117269d2c452f4`  
		Last Modified: Wed, 03 Mar 2021 23:13:09 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.3.6` - linux; ppc64le

```console
$ docker pull haproxy@sha256:741a0dc67c8b115376f867d987bc1d9a4bc90619a4939074c94ce0cd1defbd89
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.7 MB (40679819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ce2f4a27a4c4caea7672c616fe0801ca3902d1d571793e66f1158d9ace20952`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:19:19 GMT
ADD file:9a8cfdf0eab394a693b5cde0700ad47b6e8506ef0b79fabb8a07874b96e6c394 in / 
# Tue, 09 Feb 2021 02:19:34 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 05:52:23 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 03 Mar 2021 23:16:59 GMT
ENV HAPROXY_VERSION=2.3.6
# Wed, 03 Mar 2021 23:17:02 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.6.tar.gz
# Wed, 03 Mar 2021 23:17:07 GMT
ENV HAPROXY_SHA256=6d4620e5da1d93ed75f229011216db81d5097b68bf175e309f2fab2890bba036
# Wed, 03 Mar 2021 23:21:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 Mar 2021 23:21:21 GMT
STOPSIGNAL SIGUSR1
# Wed, 03 Mar 2021 23:21:24 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 03 Mar 2021 23:21:36 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 03 Mar 2021 23:21:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Mar 2021 23:21:43 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:9996b4fb6bc1c50f95ba30f8988c9c89526556fa320d3fda59d3d8359f7810d6`  
		Last Modified: Tue, 09 Feb 2021 02:27:59 GMT  
		Size: 30.5 MB (30519509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7f600bc4989eb9f12d5006a73f5958eb4fe85f86bc4008d7a899bb935b0f1c`  
		Last Modified: Tue, 09 Feb 2021 06:38:36 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f996cf993595d7dfaa53dd8b2756f38db1c17c7fd9711ac10dc4191cec786d60`  
		Last Modified: Wed, 03 Mar 2021 23:31:40 GMT  
		Size: 10.2 MB (10158363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7991881f420b992a3223335c3213fc329c88dffe0516c57bf925f34dd2783fe`  
		Last Modified: Wed, 03 Mar 2021 23:31:37 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51f9d3ebe569638afe6c4bad4532d993022b91325ea88fafc3a593a4d0c8848d`  
		Last Modified: Wed, 03 Mar 2021 23:31:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.3.6` - linux; s390x

```console
$ docker pull haproxy@sha256:7caad1df1cc08ce7f758568a4a2fb426d700c62c3dc78d0041de32e5d57477bc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.1 MB (35093083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3cdecbc4babbecaa160b39e9ef4bd2cc182628cb8bce7bfdd24d2f91c10bd48`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:42:10 GMT
ADD file:0edb2de05df54191a141bd125f59d7e14eef0cc4576927a247b8dd7d6f255d04 in / 
# Tue, 09 Feb 2021 02:42:12 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:39:30 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 03 Mar 2021 23:41:38 GMT
ENV HAPROXY_VERSION=2.3.6
# Wed, 03 Mar 2021 23:41:38 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.6.tar.gz
# Wed, 03 Mar 2021 23:41:39 GMT
ENV HAPROXY_SHA256=6d4620e5da1d93ed75f229011216db81d5097b68bf175e309f2fab2890bba036
# Wed, 03 Mar 2021 23:42:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 Mar 2021 23:42:19 GMT
STOPSIGNAL SIGUSR1
# Wed, 03 Mar 2021 23:42:19 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 03 Mar 2021 23:42:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 03 Mar 2021 23:42:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Mar 2021 23:42:21 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:032413a44cf56b097e48b8221bf475ca1bec26e7a27f35fe61d699366a335b79`  
		Last Modified: Tue, 09 Feb 2021 02:45:31 GMT  
		Size: 25.7 MB (25710021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e65f701864562492efa2c0035134b62d68efdb6e7241a0a2dcc3151e6d5775b`  
		Last Modified: Tue, 09 Feb 2021 03:44:28 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62fc0238f1fd6fa72a0d48c70d25c0223d69ee003d98edc91896d34a78569752`  
		Last Modified: Wed, 03 Mar 2021 23:45:58 GMT  
		Size: 9.4 MB (9381115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a706369cf995e0ac6dc64e80d0aa1273c88faef770d5525485b9be6b982dafa`  
		Last Modified: Wed, 03 Mar 2021 23:45:54 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bac4428d8a67f044ee63239ab25919c550a35aefffd9dcd18e8dea892fba0a42`  
		Last Modified: Wed, 03 Mar 2021 23:45:54 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haproxy:2.3.6-alpine`

```console
$ docker pull haproxy@sha256:1acfe61b2c69a62809ba7899b3b4c8e7013e6e669073c65913eda836cd8e46ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `haproxy:2.3.6-alpine` - linux; amd64

```console
$ docker pull haproxy@sha256:bb0e20bf8631ecf3edb8fc5d38f32e4f8683f4bfa22ee4d3c1c19257260c3e10
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9470523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c739eebc3708f3bf44ad3721798cd90428e16ce16fd7fd00e0913a0a6f911224`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 21:19:54 GMT
ADD file:80bf8bd014071345b1c0364eeb0a5e48f3fb0d87f9c31cb990e57caa652b59b8 in / 
# Wed, 17 Feb 2021 21:19:54 GMT
CMD ["/bin/sh"]
# Mon, 08 Mar 2021 21:38:26 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 21:40:50 GMT
ENV HAPROXY_VERSION=2.3.6
# Mon, 08 Mar 2021 21:40:50 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.6.tar.gz
# Mon, 08 Mar 2021 21:40:50 GMT
ENV HAPROXY_SHA256=6d4620e5da1d93ed75f229011216db81d5097b68bf175e309f2fab2890bba036
# Mon, 08 Mar 2021 21:42:05 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Mon, 08 Mar 2021 21:42:05 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 21:42:06 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 21:42:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 08 Mar 2021 21:42:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 21:42:07 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:ba3557a56b150f9b813f9d02274d62914fd8fce120dd374d9ee17b87cf1d277d`  
		Last Modified: Wed, 17 Feb 2021 21:20:25 GMT  
		Size: 2.8 MB (2811657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9216237f12c4d44ab183590086cf2a09004b5609c4b50871d88658faa495245`  
		Last Modified: Mon, 08 Mar 2021 21:52:45 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ecd249d2b29591c8718e8042dbbb0295cf28f32e5d6f2d0c6137588c835a373`  
		Last Modified: Mon, 08 Mar 2021 21:53:19 GMT  
		Size: 6.7 MB (6657113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ffe9787642facf9bd36f4d104f20530c82832162f57aea7303cf18e78e18381`  
		Last Modified: Mon, 08 Mar 2021 21:53:18 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76363271b801b0e06ee5b00d57f806f69f4dd16018917904e2a7366ca5d4f691`  
		Last Modified: Mon, 08 Mar 2021 21:53:18 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.3.6-alpine` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:dad539f489eddffa79e2bc62db45c170d386e7e50f3ed9764c6f2725c956d8cc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9180433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1eae12a743b81699c7d83b505ab33f3215795d7f585cd5a6d85bb9f1df74595`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 20:49:32 GMT
ADD file:c04fbd3b039001c592cfa14f8388f8934ed4223ccf274dbb926e75039e172af4 in / 
# Wed, 17 Feb 2021 20:49:33 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 21:08:27 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 03 Mar 2021 23:52:03 GMT
ENV HAPROXY_VERSION=2.3.6
# Wed, 03 Mar 2021 23:52:04 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.6.tar.gz
# Wed, 03 Mar 2021 23:52:05 GMT
ENV HAPROXY_SHA256=6d4620e5da1d93ed75f229011216db81d5097b68bf175e309f2fab2890bba036
# Wed, 03 Mar 2021 23:52:46 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 03 Mar 2021 23:52:47 GMT
STOPSIGNAL SIGUSR1
# Wed, 03 Mar 2021 23:52:50 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 03 Mar 2021 23:52:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 03 Mar 2021 23:52:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Mar 2021 23:52:58 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:1353527ebe111f9bb1e271264a3c182e909e4b36463f80d7dbde1be0713eb892`  
		Last Modified: Wed, 17 Feb 2021 20:50:06 GMT  
		Size: 2.6 MB (2622039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d174378d3ee2c0c6e6a85b5228f929557826d80bcd23b2434093942f499361a7`  
		Last Modified: Wed, 17 Feb 2021 21:12:31 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ccee6a4d6ac6225e6187dc0e46c70472f929133726f02d42c2cf67cf98a26f0`  
		Last Modified: Wed, 03 Mar 2021 23:55:01 GMT  
		Size: 6.6 MB (6556640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cff92ae4d51d26dcd1ace6305cd0065294b2c57cb28f5cd1d5fb8c87d0eb0de5`  
		Last Modified: Wed, 03 Mar 2021 23:54:58 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141ebb3c783c45f4d18a6a36fde22ab8925733991323335789c6079b8288257d`  
		Last Modified: Wed, 03 Mar 2021 23:54:58 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.3.6-alpine` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:b20ebce77cee18aa4b18109c23f165d16f1fa602087f9cc6500719a555d877f9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8902072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edb1f5a0f63bae55a706913af7ee4303dcd8da7ff29bd169c99425e8f8d78028`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 20:57:36 GMT
ADD file:efdd39e5243eaf378f12ad5a85d2222b44930850a90263e5f17e8a6b5e9bc9b8 in / 
# Wed, 17 Feb 2021 20:57:37 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 21:49:42 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Thu, 04 Mar 2021 00:01:06 GMT
ENV HAPROXY_VERSION=2.3.6
# Thu, 04 Mar 2021 00:01:07 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.6.tar.gz
# Thu, 04 Mar 2021 00:01:09 GMT
ENV HAPROXY_SHA256=6d4620e5da1d93ed75f229011216db81d5097b68bf175e309f2fab2890bba036
# Thu, 04 Mar 2021 00:01:47 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Thu, 04 Mar 2021 00:01:48 GMT
STOPSIGNAL SIGUSR1
# Thu, 04 Mar 2021 00:01:51 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Thu, 04 Mar 2021 00:01:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 04 Mar 2021 00:01:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 00:02:00 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f55b840e27d3dbe27e44497103a4397f043749f933eb0433d29e2f104b3435ef`  
		Last Modified: Wed, 17 Feb 2021 20:58:14 GMT  
		Size: 2.4 MB (2423892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86398e5ccaeed703d9464d57f2d97546fad0481312144292414eb1cf857b617f`  
		Last Modified: Wed, 17 Feb 2021 21:55:00 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bfad952fdf51b889dc5d6e3b4fd1cc4ee75e696df82fc4ab61a934b3d7d0963`  
		Last Modified: Thu, 04 Mar 2021 00:06:38 GMT  
		Size: 6.5 MB (6476423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6974c640fb0a7c93496a49eda6f453ded411da802620224ab9eabb800ac7b25c`  
		Last Modified: Thu, 04 Mar 2021 00:06:36 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3c686e3ab18a686bd3d0d979838afafff033210b4a23d632987958bf6819f67`  
		Last Modified: Thu, 04 Mar 2021 00:06:36 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.3.6-alpine` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:4fbb7b77eec6f9ee10edfd294837fad3e682e5b3f74c2ca24683e7fc808b4270
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9380846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2dd25c0078f44eca15948151ec0ff316e79f750fec9191e8f3efd49a4ff980f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 20:39:29 GMT
ADD file:3bf1497bd250cf7c73c12231dc4ebe3a3a67f2cd99e35bce47ef6674683aeb1d in / 
# Wed, 17 Feb 2021 20:39:30 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 21:36:08 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 03 Mar 2021 23:41:14 GMT
ENV HAPROXY_VERSION=2.3.6
# Wed, 03 Mar 2021 23:41:15 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.6.tar.gz
# Wed, 03 Mar 2021 23:41:16 GMT
ENV HAPROXY_SHA256=6d4620e5da1d93ed75f229011216db81d5097b68bf175e309f2fab2890bba036
# Wed, 03 Mar 2021 23:41:49 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 03 Mar 2021 23:41:50 GMT
STOPSIGNAL SIGUSR1
# Wed, 03 Mar 2021 23:41:53 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 03 Mar 2021 23:41:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 03 Mar 2021 23:41:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Mar 2021 23:41:57 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:069a56d6d07f6b186fbb82e4486616b9be9a37ce32a63013af6cddcb65898182`  
		Last Modified: Wed, 17 Feb 2021 20:40:04 GMT  
		Size: 2.7 MB (2711572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6644620fa9074da825714fc7794756e2b0e36f3e83ffc2bc01bbc9df0de9e373`  
		Last Modified: Wed, 17 Feb 2021 21:41:18 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc1f8d42c267e784c8b356dfea3c9253203b122ad990cd4d37ded39a0e656e9`  
		Last Modified: Wed, 03 Mar 2021 23:45:00 GMT  
		Size: 6.7 MB (6667516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a90e0b19f903de5d2fe3915f417de80c2ef7d2a56661a7e72942b224f32b86`  
		Last Modified: Wed, 03 Mar 2021 23:44:58 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbca444d151b0822cef49ee7729684f9ece293a9a81bc6282fc78559124d793b`  
		Last Modified: Wed, 03 Mar 2021 23:44:58 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.3.6-alpine` - linux; 386

```console
$ docker pull haproxy@sha256:994058b2b2ba55b755e38344adba0c31d56640911e9cd83eb7f1e87901f3900b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9323078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f000368b08b43f83fc8fb4d5dd02fdabf666bc713f749d3fc4b5e4392dd5366b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 21:38:34 GMT
ADD file:eaee53da3c87749799de55809e4a5b526c56855332b961a85b1184c660f1d65b in / 
# Wed, 17 Feb 2021 21:38:35 GMT
CMD ["/bin/sh"]
# Mon, 08 Mar 2021 22:03:53 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 22:06:07 GMT
ENV HAPROXY_VERSION=2.3.6
# Mon, 08 Mar 2021 22:06:07 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.6.tar.gz
# Mon, 08 Mar 2021 22:06:07 GMT
ENV HAPROXY_SHA256=6d4620e5da1d93ed75f229011216db81d5097b68bf175e309f2fab2890bba036
# Mon, 08 Mar 2021 22:07:07 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Mon, 08 Mar 2021 22:07:07 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 22:07:08 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 22:07:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 08 Mar 2021 22:07:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 22:07:09 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:86205afa28f6bc624469015a543d16608258d2828411a92c662f4fdc6d276e18`  
		Last Modified: Wed, 17 Feb 2021 21:39:07 GMT  
		Size: 2.8 MB (2818177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080e85d941540171ac6a020af17b393f2a40b03d40b9677d708d31ffb6e31b71`  
		Last Modified: Mon, 08 Mar 2021 22:18:02 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1501416f7b36ee8ae1db9b34eceed0af66b127a1ce1a24b627883048028d1d06`  
		Last Modified: Mon, 08 Mar 2021 22:18:33 GMT  
		Size: 6.5 MB (6503146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5700332802e415bfca89d97df82941bdf05c6cbc177f50a7c3e96d784a508a2`  
		Last Modified: Mon, 08 Mar 2021 22:18:32 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f6a4303e7e72e2141a6a68bd313e07230e8f857dda792113b4746f97b84155`  
		Last Modified: Mon, 08 Mar 2021 22:18:32 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.3.6-alpine` - linux; ppc64le

```console
$ docker pull haproxy@sha256:7d3892886cd28df906de4269cf803495cdc753bd3ee815e71b729ffaae219b93
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9798645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7bb459e90ff5599695221ef998010e7da3c41f3b1d284dc8d03a34a9443ce4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 21:17:29 GMT
ADD file:28f4377c61c0f8eb43a6b36e6a24ef5893f51d405d25b62e364988223537ae0b in / 
# Wed, 17 Feb 2021 21:17:37 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 22:10:46 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 03 Mar 2021 23:21:56 GMT
ENV HAPROXY_VERSION=2.3.6
# Wed, 03 Mar 2021 23:22:01 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.6.tar.gz
# Wed, 03 Mar 2021 23:22:06 GMT
ENV HAPROXY_SHA256=6d4620e5da1d93ed75f229011216db81d5097b68bf175e309f2fab2890bba036
# Wed, 03 Mar 2021 23:22:47 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 03 Mar 2021 23:22:54 GMT
STOPSIGNAL SIGUSR1
# Wed, 03 Mar 2021 23:22:58 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 03 Mar 2021 23:23:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 03 Mar 2021 23:23:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Mar 2021 23:23:22 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:cb672e0375a8f9bb3d33049ceb372ffa49b959bfc84fe6f72bfb97b682a608c8`  
		Last Modified: Wed, 17 Feb 2021 21:18:10 GMT  
		Size: 2.8 MB (2813081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f391a7d74b9bf5c2089e7957996d00d99ddc33d8295873bf28746716bb728a`  
		Last Modified: Wed, 17 Feb 2021 22:23:02 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8505b18905139bf39bbee5b1d18e7d1cd0d729fc1ea3a2630643c89f760e9b3d`  
		Last Modified: Wed, 03 Mar 2021 23:32:00 GMT  
		Size: 7.0 MB (6983804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69d123eec920832dc833ae5ebe82126f063dfbf0401f32d1d47e75c54ca1829a`  
		Last Modified: Wed, 03 Mar 2021 23:31:59 GMT  
		Size: 448.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea331f8b85bdb9c8c7f7c51ea304edd7fb486abda08b014da26b95bd3b63af41`  
		Last Modified: Wed, 03 Mar 2021 23:31:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.3.6-alpine` - linux; s390x

```console
$ docker pull haproxy@sha256:e4a841f57598b3e66eb87c80436106cea84efd6c9d137ec28641ec8e057cb742
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9227626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c55a39fa38ab3d8c3aa8f4f7c6649619ad06a4445975af1730c9aa1a73805f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 20:41:27 GMT
ADD file:630c66f8d774d75b51e32aff812b438d377ebd3389c4aa6c324fdf8c03b6fa13 in / 
# Wed, 17 Feb 2021 20:41:27 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 21:33:33 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 03 Mar 2021 23:42:26 GMT
ENV HAPROXY_VERSION=2.3.6
# Wed, 03 Mar 2021 23:42:27 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.6.tar.gz
# Wed, 03 Mar 2021 23:42:27 GMT
ENV HAPROXY_SHA256=6d4620e5da1d93ed75f229011216db81d5097b68bf175e309f2fab2890bba036
# Wed, 03 Mar 2021 23:43:05 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 03 Mar 2021 23:43:06 GMT
STOPSIGNAL SIGUSR1
# Wed, 03 Mar 2021 23:43:06 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 03 Mar 2021 23:43:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 03 Mar 2021 23:43:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Mar 2021 23:43:08 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:ff5e8cb87555e9fa38a441f5cf0414e91353e2cd21cdb48d48b7de5bb39ce674`  
		Last Modified: Wed, 17 Feb 2021 20:41:58 GMT  
		Size: 2.6 MB (2602381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de25a3a0de168e6603cb978691ef3e7f11d7c9108d0ade38d3185d5d9dbdc094`  
		Last Modified: Wed, 17 Feb 2021 21:43:59 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0df5fca35947aa6a68611a88bc3b2d7b1213d50a7776cd1460c718c970c3a0a`  
		Last Modified: Wed, 03 Mar 2021 23:46:07 GMT  
		Size: 6.6 MB (6623491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e31ff14df8c306d11a15e27642d466ac2c59267055f69b77ed86ea72289114f`  
		Last Modified: Wed, 03 Mar 2021 23:46:06 GMT  
		Size: 448.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22aea0c74922fd9cb56014cf281aeb5c1df5d59e73ca4a4694c5903d80230d3a`  
		Last Modified: Wed, 03 Mar 2021 23:45:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haproxy:2.3-alpine`

```console
$ docker pull haproxy@sha256:1acfe61b2c69a62809ba7899b3b4c8e7013e6e669073c65913eda836cd8e46ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `haproxy:2.3-alpine` - linux; amd64

```console
$ docker pull haproxy@sha256:bb0e20bf8631ecf3edb8fc5d38f32e4f8683f4bfa22ee4d3c1c19257260c3e10
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9470523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c739eebc3708f3bf44ad3721798cd90428e16ce16fd7fd00e0913a0a6f911224`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 21:19:54 GMT
ADD file:80bf8bd014071345b1c0364eeb0a5e48f3fb0d87f9c31cb990e57caa652b59b8 in / 
# Wed, 17 Feb 2021 21:19:54 GMT
CMD ["/bin/sh"]
# Mon, 08 Mar 2021 21:38:26 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 21:40:50 GMT
ENV HAPROXY_VERSION=2.3.6
# Mon, 08 Mar 2021 21:40:50 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.6.tar.gz
# Mon, 08 Mar 2021 21:40:50 GMT
ENV HAPROXY_SHA256=6d4620e5da1d93ed75f229011216db81d5097b68bf175e309f2fab2890bba036
# Mon, 08 Mar 2021 21:42:05 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Mon, 08 Mar 2021 21:42:05 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 21:42:06 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 21:42:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 08 Mar 2021 21:42:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 21:42:07 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:ba3557a56b150f9b813f9d02274d62914fd8fce120dd374d9ee17b87cf1d277d`  
		Last Modified: Wed, 17 Feb 2021 21:20:25 GMT  
		Size: 2.8 MB (2811657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9216237f12c4d44ab183590086cf2a09004b5609c4b50871d88658faa495245`  
		Last Modified: Mon, 08 Mar 2021 21:52:45 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ecd249d2b29591c8718e8042dbbb0295cf28f32e5d6f2d0c6137588c835a373`  
		Last Modified: Mon, 08 Mar 2021 21:53:19 GMT  
		Size: 6.7 MB (6657113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ffe9787642facf9bd36f4d104f20530c82832162f57aea7303cf18e78e18381`  
		Last Modified: Mon, 08 Mar 2021 21:53:18 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76363271b801b0e06ee5b00d57f806f69f4dd16018917904e2a7366ca5d4f691`  
		Last Modified: Mon, 08 Mar 2021 21:53:18 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.3-alpine` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:dad539f489eddffa79e2bc62db45c170d386e7e50f3ed9764c6f2725c956d8cc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9180433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1eae12a743b81699c7d83b505ab33f3215795d7f585cd5a6d85bb9f1df74595`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 20:49:32 GMT
ADD file:c04fbd3b039001c592cfa14f8388f8934ed4223ccf274dbb926e75039e172af4 in / 
# Wed, 17 Feb 2021 20:49:33 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 21:08:27 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 03 Mar 2021 23:52:03 GMT
ENV HAPROXY_VERSION=2.3.6
# Wed, 03 Mar 2021 23:52:04 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.6.tar.gz
# Wed, 03 Mar 2021 23:52:05 GMT
ENV HAPROXY_SHA256=6d4620e5da1d93ed75f229011216db81d5097b68bf175e309f2fab2890bba036
# Wed, 03 Mar 2021 23:52:46 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 03 Mar 2021 23:52:47 GMT
STOPSIGNAL SIGUSR1
# Wed, 03 Mar 2021 23:52:50 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 03 Mar 2021 23:52:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 03 Mar 2021 23:52:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Mar 2021 23:52:58 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:1353527ebe111f9bb1e271264a3c182e909e4b36463f80d7dbde1be0713eb892`  
		Last Modified: Wed, 17 Feb 2021 20:50:06 GMT  
		Size: 2.6 MB (2622039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d174378d3ee2c0c6e6a85b5228f929557826d80bcd23b2434093942f499361a7`  
		Last Modified: Wed, 17 Feb 2021 21:12:31 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ccee6a4d6ac6225e6187dc0e46c70472f929133726f02d42c2cf67cf98a26f0`  
		Last Modified: Wed, 03 Mar 2021 23:55:01 GMT  
		Size: 6.6 MB (6556640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cff92ae4d51d26dcd1ace6305cd0065294b2c57cb28f5cd1d5fb8c87d0eb0de5`  
		Last Modified: Wed, 03 Mar 2021 23:54:58 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141ebb3c783c45f4d18a6a36fde22ab8925733991323335789c6079b8288257d`  
		Last Modified: Wed, 03 Mar 2021 23:54:58 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.3-alpine` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:b20ebce77cee18aa4b18109c23f165d16f1fa602087f9cc6500719a555d877f9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8902072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edb1f5a0f63bae55a706913af7ee4303dcd8da7ff29bd169c99425e8f8d78028`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 20:57:36 GMT
ADD file:efdd39e5243eaf378f12ad5a85d2222b44930850a90263e5f17e8a6b5e9bc9b8 in / 
# Wed, 17 Feb 2021 20:57:37 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 21:49:42 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Thu, 04 Mar 2021 00:01:06 GMT
ENV HAPROXY_VERSION=2.3.6
# Thu, 04 Mar 2021 00:01:07 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.6.tar.gz
# Thu, 04 Mar 2021 00:01:09 GMT
ENV HAPROXY_SHA256=6d4620e5da1d93ed75f229011216db81d5097b68bf175e309f2fab2890bba036
# Thu, 04 Mar 2021 00:01:47 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Thu, 04 Mar 2021 00:01:48 GMT
STOPSIGNAL SIGUSR1
# Thu, 04 Mar 2021 00:01:51 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Thu, 04 Mar 2021 00:01:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 04 Mar 2021 00:01:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 00:02:00 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f55b840e27d3dbe27e44497103a4397f043749f933eb0433d29e2f104b3435ef`  
		Last Modified: Wed, 17 Feb 2021 20:58:14 GMT  
		Size: 2.4 MB (2423892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86398e5ccaeed703d9464d57f2d97546fad0481312144292414eb1cf857b617f`  
		Last Modified: Wed, 17 Feb 2021 21:55:00 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bfad952fdf51b889dc5d6e3b4fd1cc4ee75e696df82fc4ab61a934b3d7d0963`  
		Last Modified: Thu, 04 Mar 2021 00:06:38 GMT  
		Size: 6.5 MB (6476423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6974c640fb0a7c93496a49eda6f453ded411da802620224ab9eabb800ac7b25c`  
		Last Modified: Thu, 04 Mar 2021 00:06:36 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3c686e3ab18a686bd3d0d979838afafff033210b4a23d632987958bf6819f67`  
		Last Modified: Thu, 04 Mar 2021 00:06:36 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.3-alpine` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:4fbb7b77eec6f9ee10edfd294837fad3e682e5b3f74c2ca24683e7fc808b4270
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9380846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2dd25c0078f44eca15948151ec0ff316e79f750fec9191e8f3efd49a4ff980f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 20:39:29 GMT
ADD file:3bf1497bd250cf7c73c12231dc4ebe3a3a67f2cd99e35bce47ef6674683aeb1d in / 
# Wed, 17 Feb 2021 20:39:30 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 21:36:08 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 03 Mar 2021 23:41:14 GMT
ENV HAPROXY_VERSION=2.3.6
# Wed, 03 Mar 2021 23:41:15 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.6.tar.gz
# Wed, 03 Mar 2021 23:41:16 GMT
ENV HAPROXY_SHA256=6d4620e5da1d93ed75f229011216db81d5097b68bf175e309f2fab2890bba036
# Wed, 03 Mar 2021 23:41:49 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 03 Mar 2021 23:41:50 GMT
STOPSIGNAL SIGUSR1
# Wed, 03 Mar 2021 23:41:53 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 03 Mar 2021 23:41:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 03 Mar 2021 23:41:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Mar 2021 23:41:57 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:069a56d6d07f6b186fbb82e4486616b9be9a37ce32a63013af6cddcb65898182`  
		Last Modified: Wed, 17 Feb 2021 20:40:04 GMT  
		Size: 2.7 MB (2711572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6644620fa9074da825714fc7794756e2b0e36f3e83ffc2bc01bbc9df0de9e373`  
		Last Modified: Wed, 17 Feb 2021 21:41:18 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc1f8d42c267e784c8b356dfea3c9253203b122ad990cd4d37ded39a0e656e9`  
		Last Modified: Wed, 03 Mar 2021 23:45:00 GMT  
		Size: 6.7 MB (6667516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a90e0b19f903de5d2fe3915f417de80c2ef7d2a56661a7e72942b224f32b86`  
		Last Modified: Wed, 03 Mar 2021 23:44:58 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbca444d151b0822cef49ee7729684f9ece293a9a81bc6282fc78559124d793b`  
		Last Modified: Wed, 03 Mar 2021 23:44:58 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.3-alpine` - linux; 386

```console
$ docker pull haproxy@sha256:994058b2b2ba55b755e38344adba0c31d56640911e9cd83eb7f1e87901f3900b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9323078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f000368b08b43f83fc8fb4d5dd02fdabf666bc713f749d3fc4b5e4392dd5366b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 21:38:34 GMT
ADD file:eaee53da3c87749799de55809e4a5b526c56855332b961a85b1184c660f1d65b in / 
# Wed, 17 Feb 2021 21:38:35 GMT
CMD ["/bin/sh"]
# Mon, 08 Mar 2021 22:03:53 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 22:06:07 GMT
ENV HAPROXY_VERSION=2.3.6
# Mon, 08 Mar 2021 22:06:07 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.6.tar.gz
# Mon, 08 Mar 2021 22:06:07 GMT
ENV HAPROXY_SHA256=6d4620e5da1d93ed75f229011216db81d5097b68bf175e309f2fab2890bba036
# Mon, 08 Mar 2021 22:07:07 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Mon, 08 Mar 2021 22:07:07 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 22:07:08 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 22:07:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 08 Mar 2021 22:07:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 22:07:09 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:86205afa28f6bc624469015a543d16608258d2828411a92c662f4fdc6d276e18`  
		Last Modified: Wed, 17 Feb 2021 21:39:07 GMT  
		Size: 2.8 MB (2818177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080e85d941540171ac6a020af17b393f2a40b03d40b9677d708d31ffb6e31b71`  
		Last Modified: Mon, 08 Mar 2021 22:18:02 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1501416f7b36ee8ae1db9b34eceed0af66b127a1ce1a24b627883048028d1d06`  
		Last Modified: Mon, 08 Mar 2021 22:18:33 GMT  
		Size: 6.5 MB (6503146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5700332802e415bfca89d97df82941bdf05c6cbc177f50a7c3e96d784a508a2`  
		Last Modified: Mon, 08 Mar 2021 22:18:32 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f6a4303e7e72e2141a6a68bd313e07230e8f857dda792113b4746f97b84155`  
		Last Modified: Mon, 08 Mar 2021 22:18:32 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.3-alpine` - linux; ppc64le

```console
$ docker pull haproxy@sha256:7d3892886cd28df906de4269cf803495cdc753bd3ee815e71b729ffaae219b93
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9798645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7bb459e90ff5599695221ef998010e7da3c41f3b1d284dc8d03a34a9443ce4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 21:17:29 GMT
ADD file:28f4377c61c0f8eb43a6b36e6a24ef5893f51d405d25b62e364988223537ae0b in / 
# Wed, 17 Feb 2021 21:17:37 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 22:10:46 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 03 Mar 2021 23:21:56 GMT
ENV HAPROXY_VERSION=2.3.6
# Wed, 03 Mar 2021 23:22:01 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.6.tar.gz
# Wed, 03 Mar 2021 23:22:06 GMT
ENV HAPROXY_SHA256=6d4620e5da1d93ed75f229011216db81d5097b68bf175e309f2fab2890bba036
# Wed, 03 Mar 2021 23:22:47 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 03 Mar 2021 23:22:54 GMT
STOPSIGNAL SIGUSR1
# Wed, 03 Mar 2021 23:22:58 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 03 Mar 2021 23:23:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 03 Mar 2021 23:23:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Mar 2021 23:23:22 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:cb672e0375a8f9bb3d33049ceb372ffa49b959bfc84fe6f72bfb97b682a608c8`  
		Last Modified: Wed, 17 Feb 2021 21:18:10 GMT  
		Size: 2.8 MB (2813081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f391a7d74b9bf5c2089e7957996d00d99ddc33d8295873bf28746716bb728a`  
		Last Modified: Wed, 17 Feb 2021 22:23:02 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8505b18905139bf39bbee5b1d18e7d1cd0d729fc1ea3a2630643c89f760e9b3d`  
		Last Modified: Wed, 03 Mar 2021 23:32:00 GMT  
		Size: 7.0 MB (6983804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69d123eec920832dc833ae5ebe82126f063dfbf0401f32d1d47e75c54ca1829a`  
		Last Modified: Wed, 03 Mar 2021 23:31:59 GMT  
		Size: 448.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea331f8b85bdb9c8c7f7c51ea304edd7fb486abda08b014da26b95bd3b63af41`  
		Last Modified: Wed, 03 Mar 2021 23:31:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.3-alpine` - linux; s390x

```console
$ docker pull haproxy@sha256:e4a841f57598b3e66eb87c80436106cea84efd6c9d137ec28641ec8e057cb742
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9227626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c55a39fa38ab3d8c3aa8f4f7c6649619ad06a4445975af1730c9aa1a73805f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 20:41:27 GMT
ADD file:630c66f8d774d75b51e32aff812b438d377ebd3389c4aa6c324fdf8c03b6fa13 in / 
# Wed, 17 Feb 2021 20:41:27 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 21:33:33 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 03 Mar 2021 23:42:26 GMT
ENV HAPROXY_VERSION=2.3.6
# Wed, 03 Mar 2021 23:42:27 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.6.tar.gz
# Wed, 03 Mar 2021 23:42:27 GMT
ENV HAPROXY_SHA256=6d4620e5da1d93ed75f229011216db81d5097b68bf175e309f2fab2890bba036
# Wed, 03 Mar 2021 23:43:05 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 03 Mar 2021 23:43:06 GMT
STOPSIGNAL SIGUSR1
# Wed, 03 Mar 2021 23:43:06 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 03 Mar 2021 23:43:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 03 Mar 2021 23:43:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Mar 2021 23:43:08 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:ff5e8cb87555e9fa38a441f5cf0414e91353e2cd21cdb48d48b7de5bb39ce674`  
		Last Modified: Wed, 17 Feb 2021 20:41:58 GMT  
		Size: 2.6 MB (2602381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de25a3a0de168e6603cb978691ef3e7f11d7c9108d0ade38d3185d5d9dbdc094`  
		Last Modified: Wed, 17 Feb 2021 21:43:59 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0df5fca35947aa6a68611a88bc3b2d7b1213d50a7776cd1460c718c970c3a0a`  
		Last Modified: Wed, 03 Mar 2021 23:46:07 GMT  
		Size: 6.6 MB (6623491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e31ff14df8c306d11a15e27642d466ac2c59267055f69b77ed86ea72289114f`  
		Last Modified: Wed, 03 Mar 2021 23:46:06 GMT  
		Size: 448.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22aea0c74922fd9cb56014cf281aeb5c1df5d59e73ca4a4694c5903d80230d3a`  
		Last Modified: Wed, 03 Mar 2021 23:45:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haproxy:2.4-dev`

```console
$ docker pull haproxy@sha256:6902a22c22a9cfb618e603ecbaef857eb447dc735e70f886bc412999541bd157
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `haproxy:2.4-dev` - linux; amd64

```console
$ docker pull haproxy@sha256:ae1de77b4872df6bf9887d81386bd40f2cedfc218a5c726e490664ea50b3cb38
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37210329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d737e5d757f1583b4c7b612a3d99c076da05c9442e40b940088273cd1b2c3741`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Mon, 08 Mar 2021 21:37:25 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 21:37:25 GMT
ENV HAPROXY_VERSION=2.4-dev11
# Mon, 08 Mar 2021 21:37:26 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/devel/haproxy-2.4-dev11.tar.gz
# Mon, 08 Mar 2021 21:37:26 GMT
ENV HAPROXY_SHA256=6c1ecf45bab27f0ded664f97ef50cfbd757bd91605a90a8a0a954295596c2ddb
# Mon, 08 Mar 2021 21:38:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 08 Mar 2021 21:38:16 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 21:38:16 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 21:38:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 21:38:16 GMT
USER haproxy
# Mon, 08 Mar 2021 21:38:16 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7bca45a971fe608786870ce75c9976f8e5a958f55e1287a6120048b897c63b6`  
		Last Modified: Mon, 08 Mar 2021 21:52:33 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:832bf410038b4a55ce691f1b2e2dcd8297f696dddffd5bfecccb39deea6def7f`  
		Last Modified: Mon, 08 Mar 2021 21:52:35 GMT  
		Size: 10.1 MB (10113360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a0dc9645bd5bf81b1438bfdc1565341e74a50ad86b059c8b07ab91defefed9`  
		Last Modified: Mon, 08 Mar 2021 21:52:33 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.4-dev` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:7b976d396d2fc5e558826d7cf12b29c16e0412a656eacf29208cc295a323624d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34556519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e53116ac8e0c18892e87d225ce40e5c73ffb40969de7a31d6ebb457d15a871ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:50:10 GMT
ADD file:fbd00ef7871dc27d7ed5fa8c238cdc80652bd87b8033be7de9e54a799bbf10a4 in / 
# Tue, 09 Feb 2021 02:50:11 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:45:24 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 21:52:12 GMT
ENV HAPROXY_VERSION=2.4-dev11
# Mon, 08 Mar 2021 21:52:13 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/devel/haproxy-2.4-dev11.tar.gz
# Mon, 08 Mar 2021 21:52:13 GMT
ENV HAPROXY_SHA256=6c1ecf45bab27f0ded664f97ef50cfbd757bd91605a90a8a0a954295596c2ddb
# Mon, 08 Mar 2021 21:53:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 08 Mar 2021 21:53:03 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 21:53:04 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 21:53:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 21:53:06 GMT
USER haproxy
# Mon, 08 Mar 2021 21:53:07 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:8e683fcc73f4da7d69ce1d5f4e1d77510aa459490068f38db2d8663698b391a0`  
		Last Modified: Tue, 09 Feb 2021 02:59:07 GMT  
		Size: 24.8 MB (24839297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def565d52deae74587a55f60d168bd531ebe8095c594027b7057a8fc1be0e8af`  
		Last Modified: Tue, 09 Feb 2021 03:54:54 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50ce703c49d4103ab9001ee933cc5980420cf45cfcfbfba8616f70feda18cbce`  
		Last Modified: Mon, 08 Mar 2021 21:54:10 GMT  
		Size: 9.7 MB (9715399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409b7a3c5ef6c61f5294112ada1db89b97a04504c7728d629853d5df473cf83b`  
		Last Modified: Mon, 08 Mar 2021 21:54:02 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.4-dev` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:0bd52f7812aa6de56f6151c24d0d5a475af43fc36c9037e05bc7d038822372e3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32292384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32a0674b88b1431d474fb0374cb522a3bdf4792a471a529159132820d03cb1b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 03:00:57 GMT
ADD file:e675d50366bde57173a75f9a29367d765e7da2b7254c5254b64e777cf6870502 in / 
# Tue, 09 Feb 2021 03:01:00 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:49:38 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 21:02:24 GMT
ENV HAPROXY_VERSION=2.4-dev11
# Mon, 08 Mar 2021 21:02:24 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/devel/haproxy-2.4-dev11.tar.gz
# Mon, 08 Mar 2021 21:02:25 GMT
ENV HAPROXY_SHA256=6c1ecf45bab27f0ded664f97ef50cfbd757bd91605a90a8a0a954295596c2ddb
# Mon, 08 Mar 2021 21:03:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 08 Mar 2021 21:03:08 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 21:03:08 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 21:03:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 21:03:10 GMT
USER haproxy
# Mon, 08 Mar 2021 21:03:11 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:db574d82360c3b60abadbef4f3daf8dee01f24741fc6ab3692aa543558d8b624`  
		Last Modified: Tue, 09 Feb 2021 03:09:46 GMT  
		Size: 22.7 MB (22703384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9978ebb1881387f11e025fb46dce2b3c715f705f6d240737574f8848c27fa0d7`  
		Last Modified: Tue, 09 Feb 2021 03:58:16 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1ae436ce816eec9474849099ed0f12345391cc8f346d6afdfbf0fcdcdab2ad3`  
		Last Modified: Mon, 08 Mar 2021 21:05:40 GMT  
		Size: 9.6 MB (9587176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03954fdc507a433b4a898227dd79d5883acaf962b6f8770affa423679536e572`  
		Last Modified: Mon, 08 Mar 2021 21:05:37 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.4-dev` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:39d5b12da706050b599b7a3774c36fe88a7b602a64872d650afb99cb75dd317b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 MB (35848256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b87a739dbe29963e5cf9376497fbbcc9cd57e0f5e0a8e447d5d7f4425efab19`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:41:10 GMT
ADD file:d906dedaf14d8e3874b46787f7a1dbf268bc124c4e1dd32f13f3079e12f22238 in / 
# Tue, 09 Feb 2021 02:41:13 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:59:41 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 21:44:00 GMT
ENV HAPROXY_VERSION=2.4-dev11
# Mon, 08 Mar 2021 21:44:00 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/devel/haproxy-2.4-dev11.tar.gz
# Mon, 08 Mar 2021 21:44:01 GMT
ENV HAPROXY_SHA256=6c1ecf45bab27f0ded664f97ef50cfbd757bd91605a90a8a0a954295596c2ddb
# Mon, 08 Mar 2021 21:44:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 08 Mar 2021 21:44:42 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 21:44:43 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 21:44:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 21:44:44 GMT
USER haproxy
# Mon, 08 Mar 2021 21:44:45 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:83c5cfdaa5385ea6fc4d31e724fd4dc5d74de847a7bdd968555b8f2c558dac0e`  
		Last Modified: Tue, 09 Feb 2021 02:47:27 GMT  
		Size: 25.9 MB (25851449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b7f43dd52365bce2c2b75f29577aa39d2b5794e2561cddc0678422ffc1f7d15`  
		Last Modified: Tue, 09 Feb 2021 04:08:36 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b78e7bd0f4b8d81960df5db4c5a5ed0659525a847ff44fd7a3afb9d0d2d2a2e3`  
		Last Modified: Mon, 08 Mar 2021 21:47:06 GMT  
		Size: 10.0 MB (9994981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c608ed6599d700b773dc76fcaca8573939860d1c7f25be8add1df0d19df99e63`  
		Last Modified: Mon, 08 Mar 2021 21:47:04 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.4-dev` - linux; 386

```console
$ docker pull haproxy@sha256:19b12851f96594dd96086d2e3f4885f2fdf015a74db18f04295bbb770d10ee57
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37718674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfa6c175bf0276657bc968c7345efff1b6d947d5e2c8820a3654a8db8a6ea30e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:39:47 GMT
ADD file:61c31b1037672781ed0ecbc080ee3d49c83af49f5578b011544513fa9625698d in / 
# Tue, 09 Feb 2021 02:39:47 GMT
CMD ["bash"]
# Mon, 08 Mar 2021 22:02:40 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 22:02:41 GMT
ENV HAPROXY_VERSION=2.4-dev11
# Mon, 08 Mar 2021 22:02:41 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/devel/haproxy-2.4-dev11.tar.gz
# Mon, 08 Mar 2021 22:02:41 GMT
ENV HAPROXY_SHA256=6c1ecf45bab27f0ded664f97ef50cfbd757bd91605a90a8a0a954295596c2ddb
# Mon, 08 Mar 2021 22:03:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 08 Mar 2021 22:03:37 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 22:03:37 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 22:03:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 22:03:37 GMT
USER haproxy
# Mon, 08 Mar 2021 22:03:37 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:27cbb00346a16ea900c1049a2e5b47942c586c377179e098382c8ca1c8e87966`  
		Last Modified: Tue, 09 Feb 2021 02:45:51 GMT  
		Size: 27.8 MB (27752731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b6129a97a33727ea8a598d1e797bccce491920bf29d769880cf2fc6d3e0436`  
		Last Modified: Mon, 08 Mar 2021 22:17:48 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2801a8dd0b2fae13c091b4ea13b51fc6d77d9c0c2b9e94b7ea2cef237dd6802f`  
		Last Modified: Mon, 08 Mar 2021 22:17:50 GMT  
		Size: 10.0 MB (9964121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b4e900b8cdc36ca34f2bedf722c9f5978a04cea1b8fcd27298210eab81d0da6`  
		Last Modified: Mon, 08 Mar 2021 22:17:48 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.4-dev` - linux; mips64le

```console
$ docker pull haproxy@sha256:9171c9e4cb7790f7640bc65b1d1a8f1a6ea40d818108888dc581a24ccb1d9e18
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.5 MB (35459593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e26f3910de6b3744acb4f3de31c3f465e5112bf2092975e0e2538d1c39273d4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 03:09:26 GMT
ADD file:0222a151f4e5033d9eae98ce2b703a63f52d049dd72ac40bdd0dc2dafe619f0a in / 
# Tue, 09 Feb 2021 03:09:27 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:41:09 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 21:07:29 GMT
ENV HAPROXY_VERSION=2.4-dev11
# Mon, 08 Mar 2021 21:07:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/devel/haproxy-2.4-dev11.tar.gz
# Mon, 08 Mar 2021 21:07:29 GMT
ENV HAPROXY_SHA256=6c1ecf45bab27f0ded664f97ef50cfbd757bd91605a90a8a0a954295596c2ddb
# Mon, 08 Mar 2021 21:10:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 08 Mar 2021 21:10:02 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 21:10:03 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 21:10:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 21:10:03 GMT
USER haproxy
# Mon, 08 Mar 2021 21:10:04 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:dfb81134097d874e01b495d1fba82e384056d0a3a45f01a69a2e86ae82af1e96`  
		Last Modified: Tue, 09 Feb 2021 03:15:55 GMT  
		Size: 25.8 MB (25764640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a549d56662447dd8cb15faf59ca0fc2eda7a877e9aee16aadd09fd46e4214a`  
		Last Modified: Tue, 09 Feb 2021 03:57:56 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87db6d3264b96dd6f8de08ae7a7f9d653c310f58bcc6d601a32caa2f44455f19`  
		Last Modified: Mon, 08 Mar 2021 21:10:46 GMT  
		Size: 9.7 MB (9693124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79cc02ebb0b1a36d153cd787370351a3d58936a790710feb76c11833248e8112`  
		Last Modified: Mon, 08 Mar 2021 21:10:40 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.4-dev` - linux; ppc64le

```console
$ docker pull haproxy@sha256:60d67a2c41015724a25094f2b0e70e89c5168d5da5f1f29b14f3fa99444e4dd3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41127881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b55e3c9858f00fe1ac5a5940c45389d822af136004282ebd8d2451e46a0fabac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:19:19 GMT
ADD file:9a8cfdf0eab394a693b5cde0700ad47b6e8506ef0b79fabb8a07874b96e6c394 in / 
# Tue, 09 Feb 2021 02:19:34 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 05:52:23 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 21:34:57 GMT
ENV HAPROXY_VERSION=2.4-dev11
# Mon, 08 Mar 2021 21:35:01 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/devel/haproxy-2.4-dev11.tar.gz
# Mon, 08 Mar 2021 21:35:05 GMT
ENV HAPROXY_SHA256=6c1ecf45bab27f0ded664f97ef50cfbd757bd91605a90a8a0a954295596c2ddb
# Mon, 08 Mar 2021 21:40:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 08 Mar 2021 21:40:37 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 21:40:38 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 21:40:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 21:40:48 GMT
USER haproxy
# Mon, 08 Mar 2021 21:40:54 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:9996b4fb6bc1c50f95ba30f8988c9c89526556fa320d3fda59d3d8359f7810d6`  
		Last Modified: Tue, 09 Feb 2021 02:27:59 GMT  
		Size: 30.5 MB (30519509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7f600bc4989eb9f12d5006a73f5958eb4fe85f86bc4008d7a899bb935b0f1c`  
		Last Modified: Tue, 09 Feb 2021 06:38:36 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90cfe20b02989697cb0d388946a2909640e82759eaf8fbb5e413f3d75f0ae18b`  
		Last Modified: Mon, 08 Mar 2021 21:43:57 GMT  
		Size: 10.6 MB (10606548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78aaaad554adbbc4ca76b38b49db8fdf26796ac56f22f2d847f4fd1510d2f913`  
		Last Modified: Mon, 08 Mar 2021 21:43:54 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.4-dev` - linux; s390x

```console
$ docker pull haproxy@sha256:616d0537e97dc31eafbbbaff584e4b63531df501d15a16283af6c60e1c5ee763
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.5 MB (35517177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f36ccd7c98dff373eba182918eadc90fd2407b57ed015267ccf0499372dec8e9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:42:10 GMT
ADD file:0edb2de05df54191a141bd125f59d7e14eef0cc4576927a247b8dd7d6f255d04 in / 
# Tue, 09 Feb 2021 02:42:12 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:39:30 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 21:44:04 GMT
ENV HAPROXY_VERSION=2.4-dev11
# Mon, 08 Mar 2021 21:44:04 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/devel/haproxy-2.4-dev11.tar.gz
# Mon, 08 Mar 2021 21:44:04 GMT
ENV HAPROXY_SHA256=6c1ecf45bab27f0ded664f97ef50cfbd757bd91605a90a8a0a954295596c2ddb
# Mon, 08 Mar 2021 21:44:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 08 Mar 2021 21:44:44 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 21:44:44 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 21:44:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 21:44:44 GMT
USER haproxy
# Mon, 08 Mar 2021 21:44:45 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:032413a44cf56b097e48b8221bf475ca1bec26e7a27f35fe61d699366a335b79`  
		Last Modified: Tue, 09 Feb 2021 02:45:31 GMT  
		Size: 25.7 MB (25710021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e65f701864562492efa2c0035134b62d68efdb6e7241a0a2dcc3151e6d5775b`  
		Last Modified: Tue, 09 Feb 2021 03:44:28 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a050b4129a2aefa89f0ac882cc596d1e9f07b3feb3d1d83aec7d8d3320abcf54`  
		Last Modified: Mon, 08 Mar 2021 21:46:56 GMT  
		Size: 9.8 MB (9805331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7feeb9566e7b317739a8c919613cb8ef6ef24444ce16a4ded2050fa913554227`  
		Last Modified: Mon, 08 Mar 2021 21:46:54 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haproxy:2.4-dev11`

```console
$ docker pull haproxy@sha256:6902a22c22a9cfb618e603ecbaef857eb447dc735e70f886bc412999541bd157
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `haproxy:2.4-dev11` - linux; amd64

```console
$ docker pull haproxy@sha256:ae1de77b4872df6bf9887d81386bd40f2cedfc218a5c726e490664ea50b3cb38
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37210329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d737e5d757f1583b4c7b612a3d99c076da05c9442e40b940088273cd1b2c3741`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Mon, 08 Mar 2021 21:37:25 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 21:37:25 GMT
ENV HAPROXY_VERSION=2.4-dev11
# Mon, 08 Mar 2021 21:37:26 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/devel/haproxy-2.4-dev11.tar.gz
# Mon, 08 Mar 2021 21:37:26 GMT
ENV HAPROXY_SHA256=6c1ecf45bab27f0ded664f97ef50cfbd757bd91605a90a8a0a954295596c2ddb
# Mon, 08 Mar 2021 21:38:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 08 Mar 2021 21:38:16 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 21:38:16 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 21:38:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 21:38:16 GMT
USER haproxy
# Mon, 08 Mar 2021 21:38:16 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7bca45a971fe608786870ce75c9976f8e5a958f55e1287a6120048b897c63b6`  
		Last Modified: Mon, 08 Mar 2021 21:52:33 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:832bf410038b4a55ce691f1b2e2dcd8297f696dddffd5bfecccb39deea6def7f`  
		Last Modified: Mon, 08 Mar 2021 21:52:35 GMT  
		Size: 10.1 MB (10113360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a0dc9645bd5bf81b1438bfdc1565341e74a50ad86b059c8b07ab91defefed9`  
		Last Modified: Mon, 08 Mar 2021 21:52:33 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.4-dev11` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:7b976d396d2fc5e558826d7cf12b29c16e0412a656eacf29208cc295a323624d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34556519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e53116ac8e0c18892e87d225ce40e5c73ffb40969de7a31d6ebb457d15a871ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:50:10 GMT
ADD file:fbd00ef7871dc27d7ed5fa8c238cdc80652bd87b8033be7de9e54a799bbf10a4 in / 
# Tue, 09 Feb 2021 02:50:11 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:45:24 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 21:52:12 GMT
ENV HAPROXY_VERSION=2.4-dev11
# Mon, 08 Mar 2021 21:52:13 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/devel/haproxy-2.4-dev11.tar.gz
# Mon, 08 Mar 2021 21:52:13 GMT
ENV HAPROXY_SHA256=6c1ecf45bab27f0ded664f97ef50cfbd757bd91605a90a8a0a954295596c2ddb
# Mon, 08 Mar 2021 21:53:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 08 Mar 2021 21:53:03 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 21:53:04 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 21:53:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 21:53:06 GMT
USER haproxy
# Mon, 08 Mar 2021 21:53:07 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:8e683fcc73f4da7d69ce1d5f4e1d77510aa459490068f38db2d8663698b391a0`  
		Last Modified: Tue, 09 Feb 2021 02:59:07 GMT  
		Size: 24.8 MB (24839297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def565d52deae74587a55f60d168bd531ebe8095c594027b7057a8fc1be0e8af`  
		Last Modified: Tue, 09 Feb 2021 03:54:54 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50ce703c49d4103ab9001ee933cc5980420cf45cfcfbfba8616f70feda18cbce`  
		Last Modified: Mon, 08 Mar 2021 21:54:10 GMT  
		Size: 9.7 MB (9715399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409b7a3c5ef6c61f5294112ada1db89b97a04504c7728d629853d5df473cf83b`  
		Last Modified: Mon, 08 Mar 2021 21:54:02 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.4-dev11` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:0bd52f7812aa6de56f6151c24d0d5a475af43fc36c9037e05bc7d038822372e3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32292384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32a0674b88b1431d474fb0374cb522a3bdf4792a471a529159132820d03cb1b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 03:00:57 GMT
ADD file:e675d50366bde57173a75f9a29367d765e7da2b7254c5254b64e777cf6870502 in / 
# Tue, 09 Feb 2021 03:01:00 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:49:38 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 21:02:24 GMT
ENV HAPROXY_VERSION=2.4-dev11
# Mon, 08 Mar 2021 21:02:24 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/devel/haproxy-2.4-dev11.tar.gz
# Mon, 08 Mar 2021 21:02:25 GMT
ENV HAPROXY_SHA256=6c1ecf45bab27f0ded664f97ef50cfbd757bd91605a90a8a0a954295596c2ddb
# Mon, 08 Mar 2021 21:03:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 08 Mar 2021 21:03:08 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 21:03:08 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 21:03:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 21:03:10 GMT
USER haproxy
# Mon, 08 Mar 2021 21:03:11 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:db574d82360c3b60abadbef4f3daf8dee01f24741fc6ab3692aa543558d8b624`  
		Last Modified: Tue, 09 Feb 2021 03:09:46 GMT  
		Size: 22.7 MB (22703384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9978ebb1881387f11e025fb46dce2b3c715f705f6d240737574f8848c27fa0d7`  
		Last Modified: Tue, 09 Feb 2021 03:58:16 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1ae436ce816eec9474849099ed0f12345391cc8f346d6afdfbf0fcdcdab2ad3`  
		Last Modified: Mon, 08 Mar 2021 21:05:40 GMT  
		Size: 9.6 MB (9587176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03954fdc507a433b4a898227dd79d5883acaf962b6f8770affa423679536e572`  
		Last Modified: Mon, 08 Mar 2021 21:05:37 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.4-dev11` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:39d5b12da706050b599b7a3774c36fe88a7b602a64872d650afb99cb75dd317b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 MB (35848256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b87a739dbe29963e5cf9376497fbbcc9cd57e0f5e0a8e447d5d7f4425efab19`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:41:10 GMT
ADD file:d906dedaf14d8e3874b46787f7a1dbf268bc124c4e1dd32f13f3079e12f22238 in / 
# Tue, 09 Feb 2021 02:41:13 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:59:41 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 21:44:00 GMT
ENV HAPROXY_VERSION=2.4-dev11
# Mon, 08 Mar 2021 21:44:00 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/devel/haproxy-2.4-dev11.tar.gz
# Mon, 08 Mar 2021 21:44:01 GMT
ENV HAPROXY_SHA256=6c1ecf45bab27f0ded664f97ef50cfbd757bd91605a90a8a0a954295596c2ddb
# Mon, 08 Mar 2021 21:44:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 08 Mar 2021 21:44:42 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 21:44:43 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 21:44:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 21:44:44 GMT
USER haproxy
# Mon, 08 Mar 2021 21:44:45 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:83c5cfdaa5385ea6fc4d31e724fd4dc5d74de847a7bdd968555b8f2c558dac0e`  
		Last Modified: Tue, 09 Feb 2021 02:47:27 GMT  
		Size: 25.9 MB (25851449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b7f43dd52365bce2c2b75f29577aa39d2b5794e2561cddc0678422ffc1f7d15`  
		Last Modified: Tue, 09 Feb 2021 04:08:36 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b78e7bd0f4b8d81960df5db4c5a5ed0659525a847ff44fd7a3afb9d0d2d2a2e3`  
		Last Modified: Mon, 08 Mar 2021 21:47:06 GMT  
		Size: 10.0 MB (9994981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c608ed6599d700b773dc76fcaca8573939860d1c7f25be8add1df0d19df99e63`  
		Last Modified: Mon, 08 Mar 2021 21:47:04 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.4-dev11` - linux; 386

```console
$ docker pull haproxy@sha256:19b12851f96594dd96086d2e3f4885f2fdf015a74db18f04295bbb770d10ee57
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37718674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfa6c175bf0276657bc968c7345efff1b6d947d5e2c8820a3654a8db8a6ea30e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:39:47 GMT
ADD file:61c31b1037672781ed0ecbc080ee3d49c83af49f5578b011544513fa9625698d in / 
# Tue, 09 Feb 2021 02:39:47 GMT
CMD ["bash"]
# Mon, 08 Mar 2021 22:02:40 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 22:02:41 GMT
ENV HAPROXY_VERSION=2.4-dev11
# Mon, 08 Mar 2021 22:02:41 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/devel/haproxy-2.4-dev11.tar.gz
# Mon, 08 Mar 2021 22:02:41 GMT
ENV HAPROXY_SHA256=6c1ecf45bab27f0ded664f97ef50cfbd757bd91605a90a8a0a954295596c2ddb
# Mon, 08 Mar 2021 22:03:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 08 Mar 2021 22:03:37 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 22:03:37 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 22:03:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 22:03:37 GMT
USER haproxy
# Mon, 08 Mar 2021 22:03:37 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:27cbb00346a16ea900c1049a2e5b47942c586c377179e098382c8ca1c8e87966`  
		Last Modified: Tue, 09 Feb 2021 02:45:51 GMT  
		Size: 27.8 MB (27752731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b6129a97a33727ea8a598d1e797bccce491920bf29d769880cf2fc6d3e0436`  
		Last Modified: Mon, 08 Mar 2021 22:17:48 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2801a8dd0b2fae13c091b4ea13b51fc6d77d9c0c2b9e94b7ea2cef237dd6802f`  
		Last Modified: Mon, 08 Mar 2021 22:17:50 GMT  
		Size: 10.0 MB (9964121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b4e900b8cdc36ca34f2bedf722c9f5978a04cea1b8fcd27298210eab81d0da6`  
		Last Modified: Mon, 08 Mar 2021 22:17:48 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.4-dev11` - linux; mips64le

```console
$ docker pull haproxy@sha256:9171c9e4cb7790f7640bc65b1d1a8f1a6ea40d818108888dc581a24ccb1d9e18
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.5 MB (35459593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e26f3910de6b3744acb4f3de31c3f465e5112bf2092975e0e2538d1c39273d4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 03:09:26 GMT
ADD file:0222a151f4e5033d9eae98ce2b703a63f52d049dd72ac40bdd0dc2dafe619f0a in / 
# Tue, 09 Feb 2021 03:09:27 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:41:09 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 21:07:29 GMT
ENV HAPROXY_VERSION=2.4-dev11
# Mon, 08 Mar 2021 21:07:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/devel/haproxy-2.4-dev11.tar.gz
# Mon, 08 Mar 2021 21:07:29 GMT
ENV HAPROXY_SHA256=6c1ecf45bab27f0ded664f97ef50cfbd757bd91605a90a8a0a954295596c2ddb
# Mon, 08 Mar 2021 21:10:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 08 Mar 2021 21:10:02 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 21:10:03 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 21:10:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 21:10:03 GMT
USER haproxy
# Mon, 08 Mar 2021 21:10:04 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:dfb81134097d874e01b495d1fba82e384056d0a3a45f01a69a2e86ae82af1e96`  
		Last Modified: Tue, 09 Feb 2021 03:15:55 GMT  
		Size: 25.8 MB (25764640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a549d56662447dd8cb15faf59ca0fc2eda7a877e9aee16aadd09fd46e4214a`  
		Last Modified: Tue, 09 Feb 2021 03:57:56 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87db6d3264b96dd6f8de08ae7a7f9d653c310f58bcc6d601a32caa2f44455f19`  
		Last Modified: Mon, 08 Mar 2021 21:10:46 GMT  
		Size: 9.7 MB (9693124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79cc02ebb0b1a36d153cd787370351a3d58936a790710feb76c11833248e8112`  
		Last Modified: Mon, 08 Mar 2021 21:10:40 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.4-dev11` - linux; ppc64le

```console
$ docker pull haproxy@sha256:60d67a2c41015724a25094f2b0e70e89c5168d5da5f1f29b14f3fa99444e4dd3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41127881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b55e3c9858f00fe1ac5a5940c45389d822af136004282ebd8d2451e46a0fabac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:19:19 GMT
ADD file:9a8cfdf0eab394a693b5cde0700ad47b6e8506ef0b79fabb8a07874b96e6c394 in / 
# Tue, 09 Feb 2021 02:19:34 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 05:52:23 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 21:34:57 GMT
ENV HAPROXY_VERSION=2.4-dev11
# Mon, 08 Mar 2021 21:35:01 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/devel/haproxy-2.4-dev11.tar.gz
# Mon, 08 Mar 2021 21:35:05 GMT
ENV HAPROXY_SHA256=6c1ecf45bab27f0ded664f97ef50cfbd757bd91605a90a8a0a954295596c2ddb
# Mon, 08 Mar 2021 21:40:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 08 Mar 2021 21:40:37 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 21:40:38 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 21:40:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 21:40:48 GMT
USER haproxy
# Mon, 08 Mar 2021 21:40:54 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:9996b4fb6bc1c50f95ba30f8988c9c89526556fa320d3fda59d3d8359f7810d6`  
		Last Modified: Tue, 09 Feb 2021 02:27:59 GMT  
		Size: 30.5 MB (30519509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7f600bc4989eb9f12d5006a73f5958eb4fe85f86bc4008d7a899bb935b0f1c`  
		Last Modified: Tue, 09 Feb 2021 06:38:36 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90cfe20b02989697cb0d388946a2909640e82759eaf8fbb5e413f3d75f0ae18b`  
		Last Modified: Mon, 08 Mar 2021 21:43:57 GMT  
		Size: 10.6 MB (10606548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78aaaad554adbbc4ca76b38b49db8fdf26796ac56f22f2d847f4fd1510d2f913`  
		Last Modified: Mon, 08 Mar 2021 21:43:54 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.4-dev11` - linux; s390x

```console
$ docker pull haproxy@sha256:616d0537e97dc31eafbbbaff584e4b63531df501d15a16283af6c60e1c5ee763
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.5 MB (35517177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f36ccd7c98dff373eba182918eadc90fd2407b57ed015267ccf0499372dec8e9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:42:10 GMT
ADD file:0edb2de05df54191a141bd125f59d7e14eef0cc4576927a247b8dd7d6f255d04 in / 
# Tue, 09 Feb 2021 02:42:12 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:39:30 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 21:44:04 GMT
ENV HAPROXY_VERSION=2.4-dev11
# Mon, 08 Mar 2021 21:44:04 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/devel/haproxy-2.4-dev11.tar.gz
# Mon, 08 Mar 2021 21:44:04 GMT
ENV HAPROXY_SHA256=6c1ecf45bab27f0ded664f97ef50cfbd757bd91605a90a8a0a954295596c2ddb
# Mon, 08 Mar 2021 21:44:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 08 Mar 2021 21:44:44 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 21:44:44 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 21:44:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 21:44:44 GMT
USER haproxy
# Mon, 08 Mar 2021 21:44:45 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:032413a44cf56b097e48b8221bf475ca1bec26e7a27f35fe61d699366a335b79`  
		Last Modified: Tue, 09 Feb 2021 02:45:31 GMT  
		Size: 25.7 MB (25710021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e65f701864562492efa2c0035134b62d68efdb6e7241a0a2dcc3151e6d5775b`  
		Last Modified: Tue, 09 Feb 2021 03:44:28 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a050b4129a2aefa89f0ac882cc596d1e9f07b3feb3d1d83aec7d8d3320abcf54`  
		Last Modified: Mon, 08 Mar 2021 21:46:56 GMT  
		Size: 9.8 MB (9805331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7feeb9566e7b317739a8c919613cb8ef6ef24444ce16a4ded2050fa913554227`  
		Last Modified: Mon, 08 Mar 2021 21:46:54 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haproxy:2.4-dev11-alpine`

```console
$ docker pull haproxy@sha256:b7390005b7a91a671a28006db1c2bc6809ec88abcd05b0256245a36328f3525a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `haproxy:2.4-dev11-alpine` - linux; amd64

```console
$ docker pull haproxy@sha256:42b3c0938facea09551b919ecf07b52893175f7d6c30f66eee81c231ed7f7902
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9971372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0a7ca71484a44bc17e1603168d19595a0a36b2c6504f14f33c3d7a5c1195c2a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 21:19:54 GMT
ADD file:80bf8bd014071345b1c0364eeb0a5e48f3fb0d87f9c31cb990e57caa652b59b8 in / 
# Wed, 17 Feb 2021 21:19:54 GMT
CMD ["/bin/sh"]
# Mon, 08 Mar 2021 21:38:26 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 21:38:26 GMT
ENV HAPROXY_VERSION=2.4-dev11
# Mon, 08 Mar 2021 21:38:26 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/devel/haproxy-2.4-dev11.tar.gz
# Mon, 08 Mar 2021 21:38:26 GMT
ENV HAPROXY_SHA256=6c1ecf45bab27f0ded664f97ef50cfbd757bd91605a90a8a0a954295596c2ddb
# Mon, 08 Mar 2021 21:39:30 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Mon, 08 Mar 2021 21:39:30 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 21:39:31 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 21:39:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 21:39:31 GMT
USER haproxy
# Mon, 08 Mar 2021 21:39:31 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:ba3557a56b150f9b813f9d02274d62914fd8fce120dd374d9ee17b87cf1d277d`  
		Last Modified: Wed, 17 Feb 2021 21:20:25 GMT  
		Size: 2.8 MB (2811657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9216237f12c4d44ab183590086cf2a09004b5609c4b50871d88658faa495245`  
		Last Modified: Mon, 08 Mar 2021 21:52:45 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a717e6689c2ed8f901ff9602e3395e5080cf74435d0eeaba3d88d25670ff40`  
		Last Modified: Mon, 08 Mar 2021 21:52:47 GMT  
		Size: 7.2 MB (7158080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f02cabb31ea12cc1b867867f8ccd2956919a41341ff0c5296d317747847260`  
		Last Modified: Mon, 08 Mar 2021 21:52:45 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.4-dev11-alpine` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:fe978bbede61f9a9c70438eb4fd794e3ccedc211c56b46fc08219c96283ed5cb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9649386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac577de19a36cf29ffdebfe0d0013f38cfbe0e829539fd045f23d6ca448cfa5b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 20:49:32 GMT
ADD file:c04fbd3b039001c592cfa14f8388f8934ed4223ccf274dbb926e75039e172af4 in / 
# Wed, 17 Feb 2021 20:49:33 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 21:08:27 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 21:49:39 GMT
ENV HAPROXY_VERSION=2.4-dev11
# Mon, 08 Mar 2021 21:49:40 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/devel/haproxy-2.4-dev11.tar.gz
# Mon, 08 Mar 2021 21:49:42 GMT
ENV HAPROXY_SHA256=6c1ecf45bab27f0ded664f97ef50cfbd757bd91605a90a8a0a954295596c2ddb
# Mon, 08 Mar 2021 21:50:10 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Mon, 08 Mar 2021 21:50:20 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 21:50:21 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 21:50:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 21:50:28 GMT
USER haproxy
# Mon, 08 Mar 2021 21:50:29 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:1353527ebe111f9bb1e271264a3c182e909e4b36463f80d7dbde1be0713eb892`  
		Last Modified: Wed, 17 Feb 2021 20:50:06 GMT  
		Size: 2.6 MB (2622039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d174378d3ee2c0c6e6a85b5228f929557826d80bcd23b2434093942f499361a7`  
		Last Modified: Wed, 17 Feb 2021 21:12:31 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a21a982ed524412b1d7e19bb35cfc78c7c4fe4f1c36d7da2b4cd2915833533`  
		Last Modified: Mon, 08 Mar 2021 21:51:42 GMT  
		Size: 7.0 MB (7025712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce883ae34fd05327193d73b2fc5ca4796db18d4015f7a8fe3f6874c3237ead7b`  
		Last Modified: Mon, 08 Mar 2021 21:51:40 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.4-dev11-alpine` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:5d03ee2f8f71c10464e2bc0c2e1b85c08f39a393d879334fa517edf04a0c8b2e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9367319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c735f473b5e3a213c160fbbbc9e8ab6a58db36f686f720db4ba712e71e7d5226`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 20:57:36 GMT
ADD file:efdd39e5243eaf378f12ad5a85d2222b44930850a90263e5f17e8a6b5e9bc9b8 in / 
# Wed, 17 Feb 2021 20:57:37 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 21:49:42 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 21:03:21 GMT
ENV HAPROXY_VERSION=2.4-dev11
# Mon, 08 Mar 2021 21:03:22 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/devel/haproxy-2.4-dev11.tar.gz
# Mon, 08 Mar 2021 21:03:22 GMT
ENV HAPROXY_SHA256=6c1ecf45bab27f0ded664f97ef50cfbd757bd91605a90a8a0a954295596c2ddb
# Mon, 08 Mar 2021 21:03:45 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Mon, 08 Mar 2021 21:03:46 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 21:03:47 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 21:03:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 21:03:50 GMT
USER haproxy
# Mon, 08 Mar 2021 21:03:53 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f55b840e27d3dbe27e44497103a4397f043749f933eb0433d29e2f104b3435ef`  
		Last Modified: Wed, 17 Feb 2021 20:58:14 GMT  
		Size: 2.4 MB (2423892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86398e5ccaeed703d9464d57f2d97546fad0481312144292414eb1cf857b617f`  
		Last Modified: Wed, 17 Feb 2021 21:55:00 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f122239d5f8fd74fd8846de655db9bebf1cba772020f34164892985442c6c0da`  
		Last Modified: Mon, 08 Mar 2021 21:05:49 GMT  
		Size: 6.9 MB (6941793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:975dcca05d1575b2017fb6396633b8767de56fe0bdf1479cedf04cc082a06348`  
		Last Modified: Mon, 08 Mar 2021 21:05:46 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.4-dev11-alpine` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:d35a52daab8fc017f7bbe458d3d552f911f4ad297c3c8f32e1c56acadc2e3137
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9895671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e660e850293545ccb647eec75235780fdafa37b23ad65671c11545b5ec03026a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 20:39:29 GMT
ADD file:3bf1497bd250cf7c73c12231dc4ebe3a3a67f2cd99e35bce47ef6674683aeb1d in / 
# Wed, 17 Feb 2021 20:39:30 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 21:36:08 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 21:44:57 GMT
ENV HAPROXY_VERSION=2.4-dev11
# Mon, 08 Mar 2021 21:44:58 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/devel/haproxy-2.4-dev11.tar.gz
# Mon, 08 Mar 2021 21:44:59 GMT
ENV HAPROXY_SHA256=6c1ecf45bab27f0ded664f97ef50cfbd757bd91605a90a8a0a954295596c2ddb
# Mon, 08 Mar 2021 21:45:24 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Mon, 08 Mar 2021 21:45:25 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 21:45:26 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 21:45:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 21:45:27 GMT
USER haproxy
# Mon, 08 Mar 2021 21:45:28 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:069a56d6d07f6b186fbb82e4486616b9be9a37ce32a63013af6cddcb65898182`  
		Last Modified: Wed, 17 Feb 2021 20:40:04 GMT  
		Size: 2.7 MB (2711572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6644620fa9074da825714fc7794756e2b0e36f3e83ffc2bc01bbc9df0de9e373`  
		Last Modified: Wed, 17 Feb 2021 21:41:18 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cc2bf48e70024eb6a9f3ea1710673f1f031c0e66374bc89f2ca5b4cd5d0db71`  
		Last Modified: Mon, 08 Mar 2021 21:47:14 GMT  
		Size: 7.2 MB (7182465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dd006216a4b5684792839314d0fe35d748caa466b6a43da16970342151c0b3d`  
		Last Modified: Mon, 08 Mar 2021 21:47:12 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.4-dev11-alpine` - linux; 386

```console
$ docker pull haproxy@sha256:f5fbe52cde260688119c428d097312a641a31ba21dc949eb17302d0d9da80aaa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9774984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a1a1e2cb85a6cc93026d91f044b3024438b4c8807c21dfb1fe132b26f65c28f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 21:38:34 GMT
ADD file:eaee53da3c87749799de55809e4a5b526c56855332b961a85b1184c660f1d65b in / 
# Wed, 17 Feb 2021 21:38:35 GMT
CMD ["/bin/sh"]
# Mon, 08 Mar 2021 22:03:53 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 22:03:54 GMT
ENV HAPROXY_VERSION=2.4-dev11
# Mon, 08 Mar 2021 22:03:54 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/devel/haproxy-2.4-dev11.tar.gz
# Mon, 08 Mar 2021 22:03:54 GMT
ENV HAPROXY_SHA256=6c1ecf45bab27f0ded664f97ef50cfbd757bd91605a90a8a0a954295596c2ddb
# Mon, 08 Mar 2021 22:05:00 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Mon, 08 Mar 2021 22:05:00 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 22:05:00 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 22:05:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 22:05:00 GMT
USER haproxy
# Mon, 08 Mar 2021 22:05:01 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:86205afa28f6bc624469015a543d16608258d2828411a92c662f4fdc6d276e18`  
		Last Modified: Wed, 17 Feb 2021 21:39:07 GMT  
		Size: 2.8 MB (2818177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080e85d941540171ac6a020af17b393f2a40b03d40b9677d708d31ffb6e31b71`  
		Last Modified: Mon, 08 Mar 2021 22:18:02 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7151c2e031b82c9a3c777ce121b2bb09216343f5d6a70a52685c318c521f0db`  
		Last Modified: Mon, 08 Mar 2021 22:18:03 GMT  
		Size: 7.0 MB (6955176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75070f5d75a9acd28cda615a419182f07d8e75d3f656b1db617bb1529a94989d`  
		Last Modified: Mon, 08 Mar 2021 22:18:02 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.4-dev11-alpine` - linux; ppc64le

```console
$ docker pull haproxy@sha256:2b62dff87bac5c635bb6e8899ed42af22728b65cd7ef91c518209f8a9c00fbb9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10315658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be553c5374d060e3b98cc5b560793a43e430481ff97ab01a5764fa65fd646c61`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 21:17:29 GMT
ADD file:28f4377c61c0f8eb43a6b36e6a24ef5893f51d405d25b62e364988223537ae0b in / 
# Wed, 17 Feb 2021 21:17:37 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 22:10:46 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 21:41:10 GMT
ENV HAPROXY_VERSION=2.4-dev11
# Mon, 08 Mar 2021 21:41:14 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/devel/haproxy-2.4-dev11.tar.gz
# Mon, 08 Mar 2021 21:41:19 GMT
ENV HAPROXY_SHA256=6c1ecf45bab27f0ded664f97ef50cfbd757bd91605a90a8a0a954295596c2ddb
# Mon, 08 Mar 2021 21:42:05 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Mon, 08 Mar 2021 21:42:10 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 21:42:12 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 21:42:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 21:42:24 GMT
USER haproxy
# Mon, 08 Mar 2021 21:42:34 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:cb672e0375a8f9bb3d33049ceb372ffa49b959bfc84fe6f72bfb97b682a608c8`  
		Last Modified: Wed, 17 Feb 2021 21:18:10 GMT  
		Size: 2.8 MB (2813081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f391a7d74b9bf5c2089e7957996d00d99ddc33d8295873bf28746716bb728a`  
		Last Modified: Wed, 17 Feb 2021 22:23:02 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b616574cea9cc75719b9990c182c03d21fe54bf4719e588fa468c46337f6b26b`  
		Last Modified: Mon, 08 Mar 2021 21:44:13 GMT  
		Size: 7.5 MB (7500932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69067708c891290b81cbd1d0d3a7dcadd8ec575ef732aabddc8017787590ce32`  
		Last Modified: Mon, 08 Mar 2021 21:44:10 GMT  
		Size: 454.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.4-dev11-alpine` - linux; s390x

```console
$ docker pull haproxy@sha256:494388ad665c691bc7aca915c012fdbc01ee50e40e97205696a6e70ddc469736
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9682342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3fe3ad2fae5b6bc4d6ead4c6f1937890c524ea20923a191ae21a1291b33e1b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 20:41:27 GMT
ADD file:630c66f8d774d75b51e32aff812b438d377ebd3389c4aa6c324fdf8c03b6fa13 in / 
# Wed, 17 Feb 2021 20:41:27 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 21:33:33 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 21:44:52 GMT
ENV HAPROXY_VERSION=2.4-dev11
# Mon, 08 Mar 2021 21:44:52 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/devel/haproxy-2.4-dev11.tar.gz
# Mon, 08 Mar 2021 21:44:52 GMT
ENV HAPROXY_SHA256=6c1ecf45bab27f0ded664f97ef50cfbd757bd91605a90a8a0a954295596c2ddb
# Mon, 08 Mar 2021 21:45:31 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Mon, 08 Mar 2021 21:45:31 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 21:45:31 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 21:45:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 21:45:32 GMT
USER haproxy
# Mon, 08 Mar 2021 21:45:32 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:ff5e8cb87555e9fa38a441f5cf0414e91353e2cd21cdb48d48b7de5bb39ce674`  
		Last Modified: Wed, 17 Feb 2021 20:41:58 GMT  
		Size: 2.6 MB (2602381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de25a3a0de168e6603cb978691ef3e7f11d7c9108d0ade38d3185d5d9dbdc094`  
		Last Modified: Wed, 17 Feb 2021 21:43:59 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e13810ecdd106b2cb83703c5bb4d7734e1868878eab925b0b038923424986dac`  
		Last Modified: Mon, 08 Mar 2021 21:47:05 GMT  
		Size: 7.1 MB (7078327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788b7276a3bb2d26d5b6e26e893d6c27342af201a6d152a04d98f185ee274d25`  
		Last Modified: Mon, 08 Mar 2021 21:47:02 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haproxy:2.4-dev-alpine`

```console
$ docker pull haproxy@sha256:b7390005b7a91a671a28006db1c2bc6809ec88abcd05b0256245a36328f3525a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `haproxy:2.4-dev-alpine` - linux; amd64

```console
$ docker pull haproxy@sha256:42b3c0938facea09551b919ecf07b52893175f7d6c30f66eee81c231ed7f7902
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9971372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0a7ca71484a44bc17e1603168d19595a0a36b2c6504f14f33c3d7a5c1195c2a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 21:19:54 GMT
ADD file:80bf8bd014071345b1c0364eeb0a5e48f3fb0d87f9c31cb990e57caa652b59b8 in / 
# Wed, 17 Feb 2021 21:19:54 GMT
CMD ["/bin/sh"]
# Mon, 08 Mar 2021 21:38:26 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 21:38:26 GMT
ENV HAPROXY_VERSION=2.4-dev11
# Mon, 08 Mar 2021 21:38:26 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/devel/haproxy-2.4-dev11.tar.gz
# Mon, 08 Mar 2021 21:38:26 GMT
ENV HAPROXY_SHA256=6c1ecf45bab27f0ded664f97ef50cfbd757bd91605a90a8a0a954295596c2ddb
# Mon, 08 Mar 2021 21:39:30 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Mon, 08 Mar 2021 21:39:30 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 21:39:31 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 21:39:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 21:39:31 GMT
USER haproxy
# Mon, 08 Mar 2021 21:39:31 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:ba3557a56b150f9b813f9d02274d62914fd8fce120dd374d9ee17b87cf1d277d`  
		Last Modified: Wed, 17 Feb 2021 21:20:25 GMT  
		Size: 2.8 MB (2811657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9216237f12c4d44ab183590086cf2a09004b5609c4b50871d88658faa495245`  
		Last Modified: Mon, 08 Mar 2021 21:52:45 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a717e6689c2ed8f901ff9602e3395e5080cf74435d0eeaba3d88d25670ff40`  
		Last Modified: Mon, 08 Mar 2021 21:52:47 GMT  
		Size: 7.2 MB (7158080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f02cabb31ea12cc1b867867f8ccd2956919a41341ff0c5296d317747847260`  
		Last Modified: Mon, 08 Mar 2021 21:52:45 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.4-dev-alpine` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:fe978bbede61f9a9c70438eb4fd794e3ccedc211c56b46fc08219c96283ed5cb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9649386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac577de19a36cf29ffdebfe0d0013f38cfbe0e829539fd045f23d6ca448cfa5b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 20:49:32 GMT
ADD file:c04fbd3b039001c592cfa14f8388f8934ed4223ccf274dbb926e75039e172af4 in / 
# Wed, 17 Feb 2021 20:49:33 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 21:08:27 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 21:49:39 GMT
ENV HAPROXY_VERSION=2.4-dev11
# Mon, 08 Mar 2021 21:49:40 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/devel/haproxy-2.4-dev11.tar.gz
# Mon, 08 Mar 2021 21:49:42 GMT
ENV HAPROXY_SHA256=6c1ecf45bab27f0ded664f97ef50cfbd757bd91605a90a8a0a954295596c2ddb
# Mon, 08 Mar 2021 21:50:10 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Mon, 08 Mar 2021 21:50:20 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 21:50:21 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 21:50:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 21:50:28 GMT
USER haproxy
# Mon, 08 Mar 2021 21:50:29 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:1353527ebe111f9bb1e271264a3c182e909e4b36463f80d7dbde1be0713eb892`  
		Last Modified: Wed, 17 Feb 2021 20:50:06 GMT  
		Size: 2.6 MB (2622039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d174378d3ee2c0c6e6a85b5228f929557826d80bcd23b2434093942f499361a7`  
		Last Modified: Wed, 17 Feb 2021 21:12:31 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a21a982ed524412b1d7e19bb35cfc78c7c4fe4f1c36d7da2b4cd2915833533`  
		Last Modified: Mon, 08 Mar 2021 21:51:42 GMT  
		Size: 7.0 MB (7025712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce883ae34fd05327193d73b2fc5ca4796db18d4015f7a8fe3f6874c3237ead7b`  
		Last Modified: Mon, 08 Mar 2021 21:51:40 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.4-dev-alpine` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:5d03ee2f8f71c10464e2bc0c2e1b85c08f39a393d879334fa517edf04a0c8b2e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9367319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c735f473b5e3a213c160fbbbc9e8ab6a58db36f686f720db4ba712e71e7d5226`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 20:57:36 GMT
ADD file:efdd39e5243eaf378f12ad5a85d2222b44930850a90263e5f17e8a6b5e9bc9b8 in / 
# Wed, 17 Feb 2021 20:57:37 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 21:49:42 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 21:03:21 GMT
ENV HAPROXY_VERSION=2.4-dev11
# Mon, 08 Mar 2021 21:03:22 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/devel/haproxy-2.4-dev11.tar.gz
# Mon, 08 Mar 2021 21:03:22 GMT
ENV HAPROXY_SHA256=6c1ecf45bab27f0ded664f97ef50cfbd757bd91605a90a8a0a954295596c2ddb
# Mon, 08 Mar 2021 21:03:45 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Mon, 08 Mar 2021 21:03:46 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 21:03:47 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 21:03:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 21:03:50 GMT
USER haproxy
# Mon, 08 Mar 2021 21:03:53 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f55b840e27d3dbe27e44497103a4397f043749f933eb0433d29e2f104b3435ef`  
		Last Modified: Wed, 17 Feb 2021 20:58:14 GMT  
		Size: 2.4 MB (2423892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86398e5ccaeed703d9464d57f2d97546fad0481312144292414eb1cf857b617f`  
		Last Modified: Wed, 17 Feb 2021 21:55:00 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f122239d5f8fd74fd8846de655db9bebf1cba772020f34164892985442c6c0da`  
		Last Modified: Mon, 08 Mar 2021 21:05:49 GMT  
		Size: 6.9 MB (6941793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:975dcca05d1575b2017fb6396633b8767de56fe0bdf1479cedf04cc082a06348`  
		Last Modified: Mon, 08 Mar 2021 21:05:46 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.4-dev-alpine` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:d35a52daab8fc017f7bbe458d3d552f911f4ad297c3c8f32e1c56acadc2e3137
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9895671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e660e850293545ccb647eec75235780fdafa37b23ad65671c11545b5ec03026a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 20:39:29 GMT
ADD file:3bf1497bd250cf7c73c12231dc4ebe3a3a67f2cd99e35bce47ef6674683aeb1d in / 
# Wed, 17 Feb 2021 20:39:30 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 21:36:08 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 21:44:57 GMT
ENV HAPROXY_VERSION=2.4-dev11
# Mon, 08 Mar 2021 21:44:58 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/devel/haproxy-2.4-dev11.tar.gz
# Mon, 08 Mar 2021 21:44:59 GMT
ENV HAPROXY_SHA256=6c1ecf45bab27f0ded664f97ef50cfbd757bd91605a90a8a0a954295596c2ddb
# Mon, 08 Mar 2021 21:45:24 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Mon, 08 Mar 2021 21:45:25 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 21:45:26 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 21:45:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 21:45:27 GMT
USER haproxy
# Mon, 08 Mar 2021 21:45:28 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:069a56d6d07f6b186fbb82e4486616b9be9a37ce32a63013af6cddcb65898182`  
		Last Modified: Wed, 17 Feb 2021 20:40:04 GMT  
		Size: 2.7 MB (2711572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6644620fa9074da825714fc7794756e2b0e36f3e83ffc2bc01bbc9df0de9e373`  
		Last Modified: Wed, 17 Feb 2021 21:41:18 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cc2bf48e70024eb6a9f3ea1710673f1f031c0e66374bc89f2ca5b4cd5d0db71`  
		Last Modified: Mon, 08 Mar 2021 21:47:14 GMT  
		Size: 7.2 MB (7182465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dd006216a4b5684792839314d0fe35d748caa466b6a43da16970342151c0b3d`  
		Last Modified: Mon, 08 Mar 2021 21:47:12 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.4-dev-alpine` - linux; 386

```console
$ docker pull haproxy@sha256:f5fbe52cde260688119c428d097312a641a31ba21dc949eb17302d0d9da80aaa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9774984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a1a1e2cb85a6cc93026d91f044b3024438b4c8807c21dfb1fe132b26f65c28f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 21:38:34 GMT
ADD file:eaee53da3c87749799de55809e4a5b526c56855332b961a85b1184c660f1d65b in / 
# Wed, 17 Feb 2021 21:38:35 GMT
CMD ["/bin/sh"]
# Mon, 08 Mar 2021 22:03:53 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 22:03:54 GMT
ENV HAPROXY_VERSION=2.4-dev11
# Mon, 08 Mar 2021 22:03:54 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/devel/haproxy-2.4-dev11.tar.gz
# Mon, 08 Mar 2021 22:03:54 GMT
ENV HAPROXY_SHA256=6c1ecf45bab27f0ded664f97ef50cfbd757bd91605a90a8a0a954295596c2ddb
# Mon, 08 Mar 2021 22:05:00 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Mon, 08 Mar 2021 22:05:00 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 22:05:00 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 22:05:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 22:05:00 GMT
USER haproxy
# Mon, 08 Mar 2021 22:05:01 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:86205afa28f6bc624469015a543d16608258d2828411a92c662f4fdc6d276e18`  
		Last Modified: Wed, 17 Feb 2021 21:39:07 GMT  
		Size: 2.8 MB (2818177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080e85d941540171ac6a020af17b393f2a40b03d40b9677d708d31ffb6e31b71`  
		Last Modified: Mon, 08 Mar 2021 22:18:02 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7151c2e031b82c9a3c777ce121b2bb09216343f5d6a70a52685c318c521f0db`  
		Last Modified: Mon, 08 Mar 2021 22:18:03 GMT  
		Size: 7.0 MB (6955176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75070f5d75a9acd28cda615a419182f07d8e75d3f656b1db617bb1529a94989d`  
		Last Modified: Mon, 08 Mar 2021 22:18:02 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.4-dev-alpine` - linux; ppc64le

```console
$ docker pull haproxy@sha256:2b62dff87bac5c635bb6e8899ed42af22728b65cd7ef91c518209f8a9c00fbb9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10315658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be553c5374d060e3b98cc5b560793a43e430481ff97ab01a5764fa65fd646c61`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 21:17:29 GMT
ADD file:28f4377c61c0f8eb43a6b36e6a24ef5893f51d405d25b62e364988223537ae0b in / 
# Wed, 17 Feb 2021 21:17:37 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 22:10:46 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 21:41:10 GMT
ENV HAPROXY_VERSION=2.4-dev11
# Mon, 08 Mar 2021 21:41:14 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/devel/haproxy-2.4-dev11.tar.gz
# Mon, 08 Mar 2021 21:41:19 GMT
ENV HAPROXY_SHA256=6c1ecf45bab27f0ded664f97ef50cfbd757bd91605a90a8a0a954295596c2ddb
# Mon, 08 Mar 2021 21:42:05 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Mon, 08 Mar 2021 21:42:10 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 21:42:12 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 21:42:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 21:42:24 GMT
USER haproxy
# Mon, 08 Mar 2021 21:42:34 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:cb672e0375a8f9bb3d33049ceb372ffa49b959bfc84fe6f72bfb97b682a608c8`  
		Last Modified: Wed, 17 Feb 2021 21:18:10 GMT  
		Size: 2.8 MB (2813081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f391a7d74b9bf5c2089e7957996d00d99ddc33d8295873bf28746716bb728a`  
		Last Modified: Wed, 17 Feb 2021 22:23:02 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b616574cea9cc75719b9990c182c03d21fe54bf4719e588fa468c46337f6b26b`  
		Last Modified: Mon, 08 Mar 2021 21:44:13 GMT  
		Size: 7.5 MB (7500932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69067708c891290b81cbd1d0d3a7dcadd8ec575ef732aabddc8017787590ce32`  
		Last Modified: Mon, 08 Mar 2021 21:44:10 GMT  
		Size: 454.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.4-dev-alpine` - linux; s390x

```console
$ docker pull haproxy@sha256:494388ad665c691bc7aca915c012fdbc01ee50e40e97205696a6e70ddc469736
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9682342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3fe3ad2fae5b6bc4d6ead4c6f1937890c524ea20923a191ae21a1291b33e1b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 20:41:27 GMT
ADD file:630c66f8d774d75b51e32aff812b438d377ebd3389c4aa6c324fdf8c03b6fa13 in / 
# Wed, 17 Feb 2021 20:41:27 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 21:33:33 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 21:44:52 GMT
ENV HAPROXY_VERSION=2.4-dev11
# Mon, 08 Mar 2021 21:44:52 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/devel/haproxy-2.4-dev11.tar.gz
# Mon, 08 Mar 2021 21:44:52 GMT
ENV HAPROXY_SHA256=6c1ecf45bab27f0ded664f97ef50cfbd757bd91605a90a8a0a954295596c2ddb
# Mon, 08 Mar 2021 21:45:31 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Mon, 08 Mar 2021 21:45:31 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 21:45:31 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 21:45:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 21:45:32 GMT
USER haproxy
# Mon, 08 Mar 2021 21:45:32 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:ff5e8cb87555e9fa38a441f5cf0414e91353e2cd21cdb48d48b7de5bb39ce674`  
		Last Modified: Wed, 17 Feb 2021 20:41:58 GMT  
		Size: 2.6 MB (2602381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de25a3a0de168e6603cb978691ef3e7f11d7c9108d0ade38d3185d5d9dbdc094`  
		Last Modified: Wed, 17 Feb 2021 21:43:59 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e13810ecdd106b2cb83703c5bb4d7734e1868878eab925b0b038923424986dac`  
		Last Modified: Mon, 08 Mar 2021 21:47:05 GMT  
		Size: 7.1 MB (7078327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788b7276a3bb2d26d5b6e26e893d6c27342af201a6d152a04d98f185ee274d25`  
		Last Modified: Mon, 08 Mar 2021 21:47:02 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haproxy:alpine`

```console
$ docker pull haproxy@sha256:1acfe61b2c69a62809ba7899b3b4c8e7013e6e669073c65913eda836cd8e46ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `haproxy:alpine` - linux; amd64

```console
$ docker pull haproxy@sha256:bb0e20bf8631ecf3edb8fc5d38f32e4f8683f4bfa22ee4d3c1c19257260c3e10
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9470523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c739eebc3708f3bf44ad3721798cd90428e16ce16fd7fd00e0913a0a6f911224`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 21:19:54 GMT
ADD file:80bf8bd014071345b1c0364eeb0a5e48f3fb0d87f9c31cb990e57caa652b59b8 in / 
# Wed, 17 Feb 2021 21:19:54 GMT
CMD ["/bin/sh"]
# Mon, 08 Mar 2021 21:38:26 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 21:40:50 GMT
ENV HAPROXY_VERSION=2.3.6
# Mon, 08 Mar 2021 21:40:50 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.6.tar.gz
# Mon, 08 Mar 2021 21:40:50 GMT
ENV HAPROXY_SHA256=6d4620e5da1d93ed75f229011216db81d5097b68bf175e309f2fab2890bba036
# Mon, 08 Mar 2021 21:42:05 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Mon, 08 Mar 2021 21:42:05 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 21:42:06 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 21:42:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 08 Mar 2021 21:42:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 21:42:07 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:ba3557a56b150f9b813f9d02274d62914fd8fce120dd374d9ee17b87cf1d277d`  
		Last Modified: Wed, 17 Feb 2021 21:20:25 GMT  
		Size: 2.8 MB (2811657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9216237f12c4d44ab183590086cf2a09004b5609c4b50871d88658faa495245`  
		Last Modified: Mon, 08 Mar 2021 21:52:45 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ecd249d2b29591c8718e8042dbbb0295cf28f32e5d6f2d0c6137588c835a373`  
		Last Modified: Mon, 08 Mar 2021 21:53:19 GMT  
		Size: 6.7 MB (6657113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ffe9787642facf9bd36f4d104f20530c82832162f57aea7303cf18e78e18381`  
		Last Modified: Mon, 08 Mar 2021 21:53:18 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76363271b801b0e06ee5b00d57f806f69f4dd16018917904e2a7366ca5d4f691`  
		Last Modified: Mon, 08 Mar 2021 21:53:18 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:alpine` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:dad539f489eddffa79e2bc62db45c170d386e7e50f3ed9764c6f2725c956d8cc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9180433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1eae12a743b81699c7d83b505ab33f3215795d7f585cd5a6d85bb9f1df74595`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 20:49:32 GMT
ADD file:c04fbd3b039001c592cfa14f8388f8934ed4223ccf274dbb926e75039e172af4 in / 
# Wed, 17 Feb 2021 20:49:33 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 21:08:27 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 03 Mar 2021 23:52:03 GMT
ENV HAPROXY_VERSION=2.3.6
# Wed, 03 Mar 2021 23:52:04 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.6.tar.gz
# Wed, 03 Mar 2021 23:52:05 GMT
ENV HAPROXY_SHA256=6d4620e5da1d93ed75f229011216db81d5097b68bf175e309f2fab2890bba036
# Wed, 03 Mar 2021 23:52:46 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 03 Mar 2021 23:52:47 GMT
STOPSIGNAL SIGUSR1
# Wed, 03 Mar 2021 23:52:50 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 03 Mar 2021 23:52:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 03 Mar 2021 23:52:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Mar 2021 23:52:58 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:1353527ebe111f9bb1e271264a3c182e909e4b36463f80d7dbde1be0713eb892`  
		Last Modified: Wed, 17 Feb 2021 20:50:06 GMT  
		Size: 2.6 MB (2622039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d174378d3ee2c0c6e6a85b5228f929557826d80bcd23b2434093942f499361a7`  
		Last Modified: Wed, 17 Feb 2021 21:12:31 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ccee6a4d6ac6225e6187dc0e46c70472f929133726f02d42c2cf67cf98a26f0`  
		Last Modified: Wed, 03 Mar 2021 23:55:01 GMT  
		Size: 6.6 MB (6556640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cff92ae4d51d26dcd1ace6305cd0065294b2c57cb28f5cd1d5fb8c87d0eb0de5`  
		Last Modified: Wed, 03 Mar 2021 23:54:58 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141ebb3c783c45f4d18a6a36fde22ab8925733991323335789c6079b8288257d`  
		Last Modified: Wed, 03 Mar 2021 23:54:58 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:alpine` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:b20ebce77cee18aa4b18109c23f165d16f1fa602087f9cc6500719a555d877f9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8902072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edb1f5a0f63bae55a706913af7ee4303dcd8da7ff29bd169c99425e8f8d78028`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 20:57:36 GMT
ADD file:efdd39e5243eaf378f12ad5a85d2222b44930850a90263e5f17e8a6b5e9bc9b8 in / 
# Wed, 17 Feb 2021 20:57:37 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 21:49:42 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Thu, 04 Mar 2021 00:01:06 GMT
ENV HAPROXY_VERSION=2.3.6
# Thu, 04 Mar 2021 00:01:07 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.6.tar.gz
# Thu, 04 Mar 2021 00:01:09 GMT
ENV HAPROXY_SHA256=6d4620e5da1d93ed75f229011216db81d5097b68bf175e309f2fab2890bba036
# Thu, 04 Mar 2021 00:01:47 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Thu, 04 Mar 2021 00:01:48 GMT
STOPSIGNAL SIGUSR1
# Thu, 04 Mar 2021 00:01:51 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Thu, 04 Mar 2021 00:01:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 04 Mar 2021 00:01:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 00:02:00 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f55b840e27d3dbe27e44497103a4397f043749f933eb0433d29e2f104b3435ef`  
		Last Modified: Wed, 17 Feb 2021 20:58:14 GMT  
		Size: 2.4 MB (2423892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86398e5ccaeed703d9464d57f2d97546fad0481312144292414eb1cf857b617f`  
		Last Modified: Wed, 17 Feb 2021 21:55:00 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bfad952fdf51b889dc5d6e3b4fd1cc4ee75e696df82fc4ab61a934b3d7d0963`  
		Last Modified: Thu, 04 Mar 2021 00:06:38 GMT  
		Size: 6.5 MB (6476423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6974c640fb0a7c93496a49eda6f453ded411da802620224ab9eabb800ac7b25c`  
		Last Modified: Thu, 04 Mar 2021 00:06:36 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3c686e3ab18a686bd3d0d979838afafff033210b4a23d632987958bf6819f67`  
		Last Modified: Thu, 04 Mar 2021 00:06:36 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:alpine` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:4fbb7b77eec6f9ee10edfd294837fad3e682e5b3f74c2ca24683e7fc808b4270
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9380846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2dd25c0078f44eca15948151ec0ff316e79f750fec9191e8f3efd49a4ff980f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 20:39:29 GMT
ADD file:3bf1497bd250cf7c73c12231dc4ebe3a3a67f2cd99e35bce47ef6674683aeb1d in / 
# Wed, 17 Feb 2021 20:39:30 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 21:36:08 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 03 Mar 2021 23:41:14 GMT
ENV HAPROXY_VERSION=2.3.6
# Wed, 03 Mar 2021 23:41:15 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.6.tar.gz
# Wed, 03 Mar 2021 23:41:16 GMT
ENV HAPROXY_SHA256=6d4620e5da1d93ed75f229011216db81d5097b68bf175e309f2fab2890bba036
# Wed, 03 Mar 2021 23:41:49 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 03 Mar 2021 23:41:50 GMT
STOPSIGNAL SIGUSR1
# Wed, 03 Mar 2021 23:41:53 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 03 Mar 2021 23:41:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 03 Mar 2021 23:41:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Mar 2021 23:41:57 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:069a56d6d07f6b186fbb82e4486616b9be9a37ce32a63013af6cddcb65898182`  
		Last Modified: Wed, 17 Feb 2021 20:40:04 GMT  
		Size: 2.7 MB (2711572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6644620fa9074da825714fc7794756e2b0e36f3e83ffc2bc01bbc9df0de9e373`  
		Last Modified: Wed, 17 Feb 2021 21:41:18 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc1f8d42c267e784c8b356dfea3c9253203b122ad990cd4d37ded39a0e656e9`  
		Last Modified: Wed, 03 Mar 2021 23:45:00 GMT  
		Size: 6.7 MB (6667516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a90e0b19f903de5d2fe3915f417de80c2ef7d2a56661a7e72942b224f32b86`  
		Last Modified: Wed, 03 Mar 2021 23:44:58 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbca444d151b0822cef49ee7729684f9ece293a9a81bc6282fc78559124d793b`  
		Last Modified: Wed, 03 Mar 2021 23:44:58 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:alpine` - linux; 386

```console
$ docker pull haproxy@sha256:994058b2b2ba55b755e38344adba0c31d56640911e9cd83eb7f1e87901f3900b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9323078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f000368b08b43f83fc8fb4d5dd02fdabf666bc713f749d3fc4b5e4392dd5366b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 21:38:34 GMT
ADD file:eaee53da3c87749799de55809e4a5b526c56855332b961a85b1184c660f1d65b in / 
# Wed, 17 Feb 2021 21:38:35 GMT
CMD ["/bin/sh"]
# Mon, 08 Mar 2021 22:03:53 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 22:06:07 GMT
ENV HAPROXY_VERSION=2.3.6
# Mon, 08 Mar 2021 22:06:07 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.6.tar.gz
# Mon, 08 Mar 2021 22:06:07 GMT
ENV HAPROXY_SHA256=6d4620e5da1d93ed75f229011216db81d5097b68bf175e309f2fab2890bba036
# Mon, 08 Mar 2021 22:07:07 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Mon, 08 Mar 2021 22:07:07 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 22:07:08 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 22:07:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 08 Mar 2021 22:07:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 22:07:09 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:86205afa28f6bc624469015a543d16608258d2828411a92c662f4fdc6d276e18`  
		Last Modified: Wed, 17 Feb 2021 21:39:07 GMT  
		Size: 2.8 MB (2818177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080e85d941540171ac6a020af17b393f2a40b03d40b9677d708d31ffb6e31b71`  
		Last Modified: Mon, 08 Mar 2021 22:18:02 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1501416f7b36ee8ae1db9b34eceed0af66b127a1ce1a24b627883048028d1d06`  
		Last Modified: Mon, 08 Mar 2021 22:18:33 GMT  
		Size: 6.5 MB (6503146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5700332802e415bfca89d97df82941bdf05c6cbc177f50a7c3e96d784a508a2`  
		Last Modified: Mon, 08 Mar 2021 22:18:32 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f6a4303e7e72e2141a6a68bd313e07230e8f857dda792113b4746f97b84155`  
		Last Modified: Mon, 08 Mar 2021 22:18:32 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:alpine` - linux; ppc64le

```console
$ docker pull haproxy@sha256:7d3892886cd28df906de4269cf803495cdc753bd3ee815e71b729ffaae219b93
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9798645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7bb459e90ff5599695221ef998010e7da3c41f3b1d284dc8d03a34a9443ce4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 21:17:29 GMT
ADD file:28f4377c61c0f8eb43a6b36e6a24ef5893f51d405d25b62e364988223537ae0b in / 
# Wed, 17 Feb 2021 21:17:37 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 22:10:46 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 03 Mar 2021 23:21:56 GMT
ENV HAPROXY_VERSION=2.3.6
# Wed, 03 Mar 2021 23:22:01 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.6.tar.gz
# Wed, 03 Mar 2021 23:22:06 GMT
ENV HAPROXY_SHA256=6d4620e5da1d93ed75f229011216db81d5097b68bf175e309f2fab2890bba036
# Wed, 03 Mar 2021 23:22:47 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 03 Mar 2021 23:22:54 GMT
STOPSIGNAL SIGUSR1
# Wed, 03 Mar 2021 23:22:58 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 03 Mar 2021 23:23:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 03 Mar 2021 23:23:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Mar 2021 23:23:22 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:cb672e0375a8f9bb3d33049ceb372ffa49b959bfc84fe6f72bfb97b682a608c8`  
		Last Modified: Wed, 17 Feb 2021 21:18:10 GMT  
		Size: 2.8 MB (2813081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f391a7d74b9bf5c2089e7957996d00d99ddc33d8295873bf28746716bb728a`  
		Last Modified: Wed, 17 Feb 2021 22:23:02 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8505b18905139bf39bbee5b1d18e7d1cd0d729fc1ea3a2630643c89f760e9b3d`  
		Last Modified: Wed, 03 Mar 2021 23:32:00 GMT  
		Size: 7.0 MB (6983804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69d123eec920832dc833ae5ebe82126f063dfbf0401f32d1d47e75c54ca1829a`  
		Last Modified: Wed, 03 Mar 2021 23:31:59 GMT  
		Size: 448.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea331f8b85bdb9c8c7f7c51ea304edd7fb486abda08b014da26b95bd3b63af41`  
		Last Modified: Wed, 03 Mar 2021 23:31:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:alpine` - linux; s390x

```console
$ docker pull haproxy@sha256:e4a841f57598b3e66eb87c80436106cea84efd6c9d137ec28641ec8e057cb742
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9227626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c55a39fa38ab3d8c3aa8f4f7c6649619ad06a4445975af1730c9aa1a73805f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 20:41:27 GMT
ADD file:630c66f8d774d75b51e32aff812b438d377ebd3389c4aa6c324fdf8c03b6fa13 in / 
# Wed, 17 Feb 2021 20:41:27 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 21:33:33 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 03 Mar 2021 23:42:26 GMT
ENV HAPROXY_VERSION=2.3.6
# Wed, 03 Mar 2021 23:42:27 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.6.tar.gz
# Wed, 03 Mar 2021 23:42:27 GMT
ENV HAPROXY_SHA256=6d4620e5da1d93ed75f229011216db81d5097b68bf175e309f2fab2890bba036
# Wed, 03 Mar 2021 23:43:05 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 03 Mar 2021 23:43:06 GMT
STOPSIGNAL SIGUSR1
# Wed, 03 Mar 2021 23:43:06 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 03 Mar 2021 23:43:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 03 Mar 2021 23:43:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Mar 2021 23:43:08 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:ff5e8cb87555e9fa38a441f5cf0414e91353e2cd21cdb48d48b7de5bb39ce674`  
		Last Modified: Wed, 17 Feb 2021 20:41:58 GMT  
		Size: 2.6 MB (2602381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de25a3a0de168e6603cb978691ef3e7f11d7c9108d0ade38d3185d5d9dbdc094`  
		Last Modified: Wed, 17 Feb 2021 21:43:59 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0df5fca35947aa6a68611a88bc3b2d7b1213d50a7776cd1460c718c970c3a0a`  
		Last Modified: Wed, 03 Mar 2021 23:46:07 GMT  
		Size: 6.6 MB (6623491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e31ff14df8c306d11a15e27642d466ac2c59267055f69b77ed86ea72289114f`  
		Last Modified: Wed, 03 Mar 2021 23:46:06 GMT  
		Size: 448.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22aea0c74922fd9cb56014cf281aeb5c1df5d59e73ca4a4694c5903d80230d3a`  
		Last Modified: Wed, 03 Mar 2021 23:45:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haproxy:latest`

```console
$ docker pull haproxy@sha256:3214ebf1267b178440a327cbb5c6167b65c22a6dd64a56f25fbace986757300f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `haproxy:latest` - linux; amd64

```console
$ docker pull haproxy@sha256:586ed760a5a2f7c662a0c0c6499ba4deee11caea609aaba3c5a381d75b3df61f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36767363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4e151b1aac28b63489aae6e912ce76d98fef88f6573f88d548dd2d54f9ca5d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Mon, 08 Mar 2021 21:37:25 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 21:39:38 GMT
ENV HAPROXY_VERSION=2.3.6
# Mon, 08 Mar 2021 21:39:38 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.6.tar.gz
# Mon, 08 Mar 2021 21:39:38 GMT
ENV HAPROXY_SHA256=6d4620e5da1d93ed75f229011216db81d5097b68bf175e309f2fab2890bba036
# Mon, 08 Mar 2021 21:40:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 08 Mar 2021 21:40:39 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 21:40:40 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 21:40:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 08 Mar 2021 21:40:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 21:40:41 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7bca45a971fe608786870ce75c9976f8e5a958f55e1287a6120048b897c63b6`  
		Last Modified: Mon, 08 Mar 2021 21:52:33 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9de78517be39f734e7e1882b46afaea8cdb7ce9a0b3f7665a3a0e33a658fbaa`  
		Last Modified: Mon, 08 Mar 2021 21:52:59 GMT  
		Size: 9.7 MB (9670271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b4c22e4f7cc999fa3fefe75b56d996159c8b4190b98b7b36d80a0e5e24caad2`  
		Last Modified: Mon, 08 Mar 2021 21:52:57 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43c239ac2f6da77003db0b8d9bee46a28e2ef72974b205d843b7de6411daef69`  
		Last Modified: Mon, 08 Mar 2021 21:52:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:latest` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:fd160acb019b9cee4334606628c1835a3c2a55cdaf157b622cd772058f0b7663
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.1 MB (34126380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef626ed9cf808dab1b3f6f9fc89cc41094363728e62d88eceaa7c8bdd39ab4a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:50:10 GMT
ADD file:fbd00ef7871dc27d7ed5fa8c238cdc80652bd87b8033be7de9e54a799bbf10a4 in / 
# Tue, 09 Feb 2021 02:50:11 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:45:24 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 03 Mar 2021 23:48:37 GMT
ENV HAPROXY_VERSION=2.3.6
# Wed, 03 Mar 2021 23:48:39 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.6.tar.gz
# Wed, 03 Mar 2021 23:48:40 GMT
ENV HAPROXY_SHA256=6d4620e5da1d93ed75f229011216db81d5097b68bf175e309f2fab2890bba036
# Wed, 03 Mar 2021 23:49:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 Mar 2021 23:49:42 GMT
STOPSIGNAL SIGUSR1
# Wed, 03 Mar 2021 23:49:43 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 03 Mar 2021 23:49:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 03 Mar 2021 23:49:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Mar 2021 23:49:46 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:8e683fcc73f4da7d69ce1d5f4e1d77510aa459490068f38db2d8663698b391a0`  
		Last Modified: Tue, 09 Feb 2021 02:59:07 GMT  
		Size: 24.8 MB (24839297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def565d52deae74587a55f60d168bd531ebe8095c594027b7057a8fc1be0e8af`  
		Last Modified: Tue, 09 Feb 2021 03:54:54 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fff3e31705a444ba58f6fedc10fd7e8509560df170ce2a6464e3c7c680f5512`  
		Last Modified: Wed, 03 Mar 2021 23:52:53 GMT  
		Size: 9.3 MB (9285141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:302d9907c27970d03ed0ac50d978a7ec92b9627bd8dfe895d0ce38c29ff8abae`  
		Last Modified: Wed, 03 Mar 2021 23:52:48 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d9fe9f8f082ead91dcc43c0af3b0ce2eec1e43e565420891144646e2e66c0bc`  
		Last Modified: Wed, 03 Mar 2021 23:52:47 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:latest` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:22739469108f3026eb1cc7566b171ad09e6baf29d82ecfe6971acb8b1d390ec6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31800938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e24a61c6cff6c522f2e6dc8dc2eefb1283b754cef79e8fc718bc2e851d64dff4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 03:00:57 GMT
ADD file:e675d50366bde57173a75f9a29367d765e7da2b7254c5254b64e777cf6870502 in / 
# Tue, 09 Feb 2021 03:01:00 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:49:38 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 03 Mar 2021 23:59:53 GMT
ENV HAPROXY_VERSION=2.3.6
# Wed, 03 Mar 2021 23:59:55 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.6.tar.gz
# Wed, 03 Mar 2021 23:59:57 GMT
ENV HAPROXY_SHA256=6d4620e5da1d93ed75f229011216db81d5097b68bf175e309f2fab2890bba036
# Thu, 04 Mar 2021 00:00:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 04 Mar 2021 00:00:45 GMT
STOPSIGNAL SIGUSR1
# Thu, 04 Mar 2021 00:00:48 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Thu, 04 Mar 2021 00:00:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 04 Mar 2021 00:00:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 00:00:56 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:db574d82360c3b60abadbef4f3daf8dee01f24741fc6ab3692aa543558d8b624`  
		Last Modified: Tue, 09 Feb 2021 03:09:46 GMT  
		Size: 22.7 MB (22703384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9978ebb1881387f11e025fb46dce2b3c715f705f6d240737574f8848c27fa0d7`  
		Last Modified: Tue, 09 Feb 2021 03:58:16 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9b042e3b0a9b457749c8b6be38159bf336900ac0a449ef7837355b905d54513`  
		Last Modified: Thu, 04 Mar 2021 00:06:28 GMT  
		Size: 9.1 MB (9095610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cb11dc12989b181df9b197123d5c719e0263ed7a7dd62a319b386a262407e5c`  
		Last Modified: Thu, 04 Mar 2021 00:06:22 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45586ab18fd80a8fca25174c46c6093922dcbd4130cd774955373136fb442bcc`  
		Last Modified: Thu, 04 Mar 2021 00:06:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:latest` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:fb7ce8e18b0ce77f8541295869bf9addf4f39936e606fb2f95fd60f183820553
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 MB (35345046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:149902bcb92ba5cbb82706a611dfcee896c375e4d9ea66fe4d6a73359d1af05b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:41:10 GMT
ADD file:d906dedaf14d8e3874b46787f7a1dbf268bc124c4e1dd32f13f3079e12f22238 in / 
# Tue, 09 Feb 2021 02:41:13 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:59:41 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 03 Mar 2021 23:40:11 GMT
ENV HAPROXY_VERSION=2.3.6
# Wed, 03 Mar 2021 23:40:12 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.6.tar.gz
# Wed, 03 Mar 2021 23:40:13 GMT
ENV HAPROXY_SHA256=6d4620e5da1d93ed75f229011216db81d5097b68bf175e309f2fab2890bba036
# Wed, 03 Mar 2021 23:40:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 Mar 2021 23:40:54 GMT
STOPSIGNAL SIGUSR1
# Wed, 03 Mar 2021 23:40:55 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 03 Mar 2021 23:40:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 03 Mar 2021 23:40:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Mar 2021 23:40:58 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:83c5cfdaa5385ea6fc4d31e724fd4dc5d74de847a7bdd968555b8f2c558dac0e`  
		Last Modified: Tue, 09 Feb 2021 02:47:27 GMT  
		Size: 25.9 MB (25851449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b7f43dd52365bce2c2b75f29577aa39d2b5794e2561cddc0678422ffc1f7d15`  
		Last Modified: Tue, 09 Feb 2021 04:08:36 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab089d5e39e2bee9f1457db0064c673f2197022e4f35bd09866546237fcce328`  
		Last Modified: Wed, 03 Mar 2021 23:44:50 GMT  
		Size: 9.5 MB (9491653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bca2e6c325b028c12e42ea4e7d6d92b0db82199b38df988fcb4e62cefe820bb`  
		Last Modified: Wed, 03 Mar 2021 23:44:48 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48adef33c780445a2435d0b2c14556b53b34fc9ca5795864b6c3cbc7cc4b25d6`  
		Last Modified: Wed, 03 Mar 2021 23:44:48 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:latest` - linux; 386

```console
$ docker pull haproxy@sha256:08029dd29e3f4a419baf0ece22ad92d46b2f27ce01cec80f4859d2492f13c0b8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 MB (37318546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1457ecba48f46c6e0909e9a34ff886af1fd3b5a35c05286c03d3f4da1456539b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:39:47 GMT
ADD file:61c31b1037672781ed0ecbc080ee3d49c83af49f5578b011544513fa9625698d in / 
# Tue, 09 Feb 2021 02:39:47 GMT
CMD ["bash"]
# Mon, 08 Mar 2021 22:02:40 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 22:05:06 GMT
ENV HAPROXY_VERSION=2.3.6
# Mon, 08 Mar 2021 22:05:06 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.6.tar.gz
# Mon, 08 Mar 2021 22:05:06 GMT
ENV HAPROXY_SHA256=6d4620e5da1d93ed75f229011216db81d5097b68bf175e309f2fab2890bba036
# Mon, 08 Mar 2021 22:05:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 08 Mar 2021 22:05:57 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 22:05:57 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 22:05:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 08 Mar 2021 22:05:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 22:05:58 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:27cbb00346a16ea900c1049a2e5b47942c586c377179e098382c8ca1c8e87966`  
		Last Modified: Tue, 09 Feb 2021 02:45:51 GMT  
		Size: 27.8 MB (27752731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b6129a97a33727ea8a598d1e797bccce491920bf29d769880cf2fc6d3e0436`  
		Last Modified: Mon, 08 Mar 2021 22:17:48 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66fc7f55bb52d577bb49216caae38e742ba182d2719615fd195125099570f183`  
		Last Modified: Mon, 08 Mar 2021 22:18:17 GMT  
		Size: 9.6 MB (9563873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91893e7877fd0573b74c92a13310c45ca6568bbfc3b61cadce60a54553812896`  
		Last Modified: Mon, 08 Mar 2021 22:18:14 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14935bdf9a0768984c33b8ba5f706939f3133106b3412589747e11f46a54221`  
		Last Modified: Mon, 08 Mar 2021 22:18:15 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:latest` - linux; mips64le

```console
$ docker pull haproxy@sha256:f047f58d1b05f146259a460b5534d4f371a3bfd8a5adeb09a04276656fa00af0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 MB (35014317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc7140e196cccbd6502dc6775c8fa25da1dea923c269c4fa57aec0831eb87b8f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 03:09:26 GMT
ADD file:0222a151f4e5033d9eae98ce2b703a63f52d049dd72ac40bdd0dc2dafe619f0a in / 
# Tue, 09 Feb 2021 03:09:27 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:41:09 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 03 Mar 2021 23:07:23 GMT
ENV HAPROXY_VERSION=2.3.6
# Wed, 03 Mar 2021 23:07:23 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.6.tar.gz
# Wed, 03 Mar 2021 23:07:23 GMT
ENV HAPROXY_SHA256=6d4620e5da1d93ed75f229011216db81d5097b68bf175e309f2fab2890bba036
# Wed, 03 Mar 2021 23:09:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 Mar 2021 23:09:49 GMT
STOPSIGNAL SIGUSR1
# Wed, 03 Mar 2021 23:09:49 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 03 Mar 2021 23:09:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 03 Mar 2021 23:09:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Mar 2021 23:09:52 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:dfb81134097d874e01b495d1fba82e384056d0a3a45f01a69a2e86ae82af1e96`  
		Last Modified: Tue, 09 Feb 2021 03:15:55 GMT  
		Size: 25.8 MB (25764640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a549d56662447dd8cb15faf59ca0fc2eda7a877e9aee16aadd09fd46e4214a`  
		Last Modified: Tue, 09 Feb 2021 03:57:56 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fd84d34b65468db17bc6bb2cb72cc70ef09422490d888737d7c029ec4d8e344`  
		Last Modified: Wed, 03 Mar 2021 23:13:19 GMT  
		Size: 9.2 MB (9247729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a561995add47ef6d0a089710e967ccabeaf9d9a416be3e03be23ef058b4834`  
		Last Modified: Wed, 03 Mar 2021 23:13:09 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0499d598e07691795e195c0d80a2dbf4807859d41722ba9689117269d2c452f4`  
		Last Modified: Wed, 03 Mar 2021 23:13:09 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:latest` - linux; ppc64le

```console
$ docker pull haproxy@sha256:741a0dc67c8b115376f867d987bc1d9a4bc90619a4939074c94ce0cd1defbd89
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.7 MB (40679819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ce2f4a27a4c4caea7672c616fe0801ca3902d1d571793e66f1158d9ace20952`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:19:19 GMT
ADD file:9a8cfdf0eab394a693b5cde0700ad47b6e8506ef0b79fabb8a07874b96e6c394 in / 
# Tue, 09 Feb 2021 02:19:34 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 05:52:23 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 03 Mar 2021 23:16:59 GMT
ENV HAPROXY_VERSION=2.3.6
# Wed, 03 Mar 2021 23:17:02 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.6.tar.gz
# Wed, 03 Mar 2021 23:17:07 GMT
ENV HAPROXY_SHA256=6d4620e5da1d93ed75f229011216db81d5097b68bf175e309f2fab2890bba036
# Wed, 03 Mar 2021 23:21:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 Mar 2021 23:21:21 GMT
STOPSIGNAL SIGUSR1
# Wed, 03 Mar 2021 23:21:24 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 03 Mar 2021 23:21:36 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 03 Mar 2021 23:21:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Mar 2021 23:21:43 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:9996b4fb6bc1c50f95ba30f8988c9c89526556fa320d3fda59d3d8359f7810d6`  
		Last Modified: Tue, 09 Feb 2021 02:27:59 GMT  
		Size: 30.5 MB (30519509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7f600bc4989eb9f12d5006a73f5958eb4fe85f86bc4008d7a899bb935b0f1c`  
		Last Modified: Tue, 09 Feb 2021 06:38:36 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f996cf993595d7dfaa53dd8b2756f38db1c17c7fd9711ac10dc4191cec786d60`  
		Last Modified: Wed, 03 Mar 2021 23:31:40 GMT  
		Size: 10.2 MB (10158363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7991881f420b992a3223335c3213fc329c88dffe0516c57bf925f34dd2783fe`  
		Last Modified: Wed, 03 Mar 2021 23:31:37 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51f9d3ebe569638afe6c4bad4532d993022b91325ea88fafc3a593a4d0c8848d`  
		Last Modified: Wed, 03 Mar 2021 23:31:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:latest` - linux; s390x

```console
$ docker pull haproxy@sha256:7caad1df1cc08ce7f758568a4a2fb426d700c62c3dc78d0041de32e5d57477bc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.1 MB (35093083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3cdecbc4babbecaa160b39e9ef4bd2cc182628cb8bce7bfdd24d2f91c10bd48`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:42:10 GMT
ADD file:0edb2de05df54191a141bd125f59d7e14eef0cc4576927a247b8dd7d6f255d04 in / 
# Tue, 09 Feb 2021 02:42:12 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:39:30 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 03 Mar 2021 23:41:38 GMT
ENV HAPROXY_VERSION=2.3.6
# Wed, 03 Mar 2021 23:41:38 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.6.tar.gz
# Wed, 03 Mar 2021 23:41:39 GMT
ENV HAPROXY_SHA256=6d4620e5da1d93ed75f229011216db81d5097b68bf175e309f2fab2890bba036
# Wed, 03 Mar 2021 23:42:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 Mar 2021 23:42:19 GMT
STOPSIGNAL SIGUSR1
# Wed, 03 Mar 2021 23:42:19 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 03 Mar 2021 23:42:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 03 Mar 2021 23:42:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Mar 2021 23:42:21 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:032413a44cf56b097e48b8221bf475ca1bec26e7a27f35fe61d699366a335b79`  
		Last Modified: Tue, 09 Feb 2021 02:45:31 GMT  
		Size: 25.7 MB (25710021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e65f701864562492efa2c0035134b62d68efdb6e7241a0a2dcc3151e6d5775b`  
		Last Modified: Tue, 09 Feb 2021 03:44:28 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62fc0238f1fd6fa72a0d48c70d25c0223d69ee003d98edc91896d34a78569752`  
		Last Modified: Wed, 03 Mar 2021 23:45:58 GMT  
		Size: 9.4 MB (9381115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a706369cf995e0ac6dc64e80d0aa1273c88faef770d5525485b9be6b982dafa`  
		Last Modified: Wed, 03 Mar 2021 23:45:54 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bac4428d8a67f044ee63239ab25919c550a35aefffd9dcd18e8dea892fba0a42`  
		Last Modified: Wed, 03 Mar 2021 23:45:54 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haproxy:lts`

```console
$ docker pull haproxy@sha256:17fc839f8647c90a1b8bfdb038ca15c70b3343a3b18155d4560aaba0feb4f23a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `haproxy:lts` - linux; amd64

```console
$ docker pull haproxy@sha256:30fa9029baf82d42817be3ec10bc1e6d996bccdf350e0d60ea873110ab4c8cea
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36394072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d25326e1fec59f886205720c25366e7c209c54166a8bf8833077290ddd96510e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Mon, 08 Mar 2021 21:37:25 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 21:42:15 GMT
ENV HAPROXY_VERSION=2.2.10
# Mon, 08 Mar 2021 21:42:16 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.10.tar.gz
# Mon, 08 Mar 2021 21:42:16 GMT
ENV HAPROXY_SHA256=a027e9cd8f703ba48dc193f5ae34d9aa152221f67ab58a4e939c96b9f4edd3bc
# Mon, 08 Mar 2021 21:43:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 08 Mar 2021 21:43:05 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 21:43:05 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 21:43:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 08 Mar 2021 21:43:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 21:43:07 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7bca45a971fe608786870ce75c9976f8e5a958f55e1287a6120048b897c63b6`  
		Last Modified: Mon, 08 Mar 2021 21:52:33 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58f76c5dffb4c0a380d771810394a448234e32317f451d201fde80fb9a78eeed`  
		Last Modified: Mon, 08 Mar 2021 21:53:33 GMT  
		Size: 9.3 MB (9296986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b42b266bfd6b703e104c7feab7d02f7f829eb215e4956b3130a9df588dbfb2`  
		Last Modified: Mon, 08 Mar 2021 21:53:31 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47974a3e33f57ab6455f2472a18124450765ae233844059cd8b06743dff54bb`  
		Last Modified: Mon, 08 Mar 2021 21:53:32 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:lts` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:73ff91d0f66aab67498a5fe774694b861ec7b1a749d3d5a9a1f01e97ab141bc9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33745871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41d3c16388f2706b685aced37923df63cbf2ecfdd1e69a10408c9df9ffe298b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:50:10 GMT
ADD file:fbd00ef7871dc27d7ed5fa8c238cdc80652bd87b8033be7de9e54a799bbf10a4 in / 
# Tue, 09 Feb 2021 02:50:11 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:45:24 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 03 Mar 2021 23:49:55 GMT
ENV HAPROXY_VERSION=2.2.10
# Wed, 03 Mar 2021 23:49:56 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.10.tar.gz
# Wed, 03 Mar 2021 23:49:56 GMT
ENV HAPROXY_SHA256=a027e9cd8f703ba48dc193f5ae34d9aa152221f67ab58a4e939c96b9f4edd3bc
# Wed, 03 Mar 2021 23:51:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 Mar 2021 23:51:17 GMT
STOPSIGNAL SIGUSR1
# Wed, 03 Mar 2021 23:51:19 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 03 Mar 2021 23:51:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 03 Mar 2021 23:51:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Mar 2021 23:51:33 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:8e683fcc73f4da7d69ce1d5f4e1d77510aa459490068f38db2d8663698b391a0`  
		Last Modified: Tue, 09 Feb 2021 02:59:07 GMT  
		Size: 24.8 MB (24839297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def565d52deae74587a55f60d168bd531ebe8095c594027b7057a8fc1be0e8af`  
		Last Modified: Tue, 09 Feb 2021 03:54:54 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:535ac2988228ac414cbf90d59aefe24781b4120b74285d4247c1c19fc3c285ff`  
		Last Modified: Wed, 03 Mar 2021 23:53:06 GMT  
		Size: 8.9 MB (8904631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c75860718fd09d4d1d1c08cf1e5004861505f3a1c39cfb8a7db6bc7a44038693`  
		Last Modified: Wed, 03 Mar 2021 23:53:02 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0628c5c9105fe74ab92e2956a77371fa0c3b0706d23e61a6b44c4b94de09a137`  
		Last Modified: Wed, 03 Mar 2021 23:53:01 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:lts` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:20aea1a6a06f9934f5568b11e8853c8178dbe25bf4451b8f4c924a663fac2d8a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31421875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:133497e3b909eee15f36602495221781241792d52a8f98b12681dc8dd78386f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 03:00:57 GMT
ADD file:e675d50366bde57173a75f9a29367d765e7da2b7254c5254b64e777cf6870502 in / 
# Tue, 09 Feb 2021 03:01:00 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:49:38 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Thu, 04 Mar 2021 00:02:18 GMT
ENV HAPROXY_VERSION=2.2.10
# Thu, 04 Mar 2021 00:02:19 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.10.tar.gz
# Thu, 04 Mar 2021 00:02:21 GMT
ENV HAPROXY_SHA256=a027e9cd8f703ba48dc193f5ae34d9aa152221f67ab58a4e939c96b9f4edd3bc
# Thu, 04 Mar 2021 00:03:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 04 Mar 2021 00:03:46 GMT
STOPSIGNAL SIGUSR1
# Thu, 04 Mar 2021 00:03:48 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Thu, 04 Mar 2021 00:03:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 04 Mar 2021 00:03:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 00:03:56 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:db574d82360c3b60abadbef4f3daf8dee01f24741fc6ab3692aa543558d8b624`  
		Last Modified: Tue, 09 Feb 2021 03:09:46 GMT  
		Size: 22.7 MB (22703384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9978ebb1881387f11e025fb46dce2b3c715f705f6d240737574f8848c27fa0d7`  
		Last Modified: Tue, 09 Feb 2021 03:58:16 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d010a4f26095dac57fe322c8fca77e3ded2f3d272ee339ed750f4e4bda194cdc`  
		Last Modified: Thu, 04 Mar 2021 00:06:50 GMT  
		Size: 8.7 MB (8716549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6d9b893b368a4a867dc7d658afae85d822a29ea39c8edd8349ff07360c275b5`  
		Last Modified: Thu, 04 Mar 2021 00:06:48 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf5154622b3ad275982ebd343b0b1589448f33031f427285db574d08fc71da31`  
		Last Modified: Thu, 04 Mar 2021 00:06:48 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:lts` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:3c3c947970064255078b0881210fed5bfccf4ffd32c650d4919544969598e535
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 MB (34964493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1fc4b06991e42504cf8ddda55c497c45c91d92fbb22bf996f8b0713deedef17`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:41:10 GMT
ADD file:d906dedaf14d8e3874b46787f7a1dbf268bc124c4e1dd32f13f3079e12f22238 in / 
# Tue, 09 Feb 2021 02:41:13 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:59:41 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 03 Mar 2021 23:42:07 GMT
ENV HAPROXY_VERSION=2.2.10
# Wed, 03 Mar 2021 23:42:08 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.10.tar.gz
# Wed, 03 Mar 2021 23:42:09 GMT
ENV HAPROXY_SHA256=a027e9cd8f703ba48dc193f5ae34d9aa152221f67ab58a4e939c96b9f4edd3bc
# Wed, 03 Mar 2021 23:42:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 Mar 2021 23:42:53 GMT
STOPSIGNAL SIGUSR1
# Wed, 03 Mar 2021 23:42:54 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 03 Mar 2021 23:42:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 03 Mar 2021 23:42:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Mar 2021 23:42:58 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:83c5cfdaa5385ea6fc4d31e724fd4dc5d74de847a7bdd968555b8f2c558dac0e`  
		Last Modified: Tue, 09 Feb 2021 02:47:27 GMT  
		Size: 25.9 MB (25851449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b7f43dd52365bce2c2b75f29577aa39d2b5794e2561cddc0678422ffc1f7d15`  
		Last Modified: Tue, 09 Feb 2021 04:08:36 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f93139e350e3df128fb0ea90fbfccc5b56d02db9d1f60958071391134dc48a3`  
		Last Modified: Wed, 03 Mar 2021 23:45:10 GMT  
		Size: 9.1 MB (9111101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b237a4ba4c115c155d87955ded33db31756d7f23009d6ab7c8c50a922939c7`  
		Last Modified: Wed, 03 Mar 2021 23:45:07 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eafe8f72c0e58ab277e633aa227b6912d7dabce25668e59adfae325d92b7116a`  
		Last Modified: Wed, 03 Mar 2021 23:45:07 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:lts` - linux; 386

```console
$ docker pull haproxy@sha256:e8cd578831262c68c9f780e4bce0437d68a1f76015a06a3a1974dae9c4c40760
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 MB (36931345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:facdf90ca5a8342db83825a14b68ce8f75b9b361198e73149912a81da0fb1271`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:39:47 GMT
ADD file:61c31b1037672781ed0ecbc080ee3d49c83af49f5578b011544513fa9625698d in / 
# Tue, 09 Feb 2021 02:39:47 GMT
CMD ["bash"]
# Mon, 08 Mar 2021 22:02:40 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 22:07:20 GMT
ENV HAPROXY_VERSION=2.2.10
# Mon, 08 Mar 2021 22:07:20 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.10.tar.gz
# Mon, 08 Mar 2021 22:07:21 GMT
ENV HAPROXY_SHA256=a027e9cd8f703ba48dc193f5ae34d9aa152221f67ab58a4e939c96b9f4edd3bc
# Mon, 08 Mar 2021 22:08:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 08 Mar 2021 22:08:11 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 22:08:11 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 22:08:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 08 Mar 2021 22:08:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 22:08:12 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:27cbb00346a16ea900c1049a2e5b47942c586c377179e098382c8ca1c8e87966`  
		Last Modified: Tue, 09 Feb 2021 02:45:51 GMT  
		Size: 27.8 MB (27752731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b6129a97a33727ea8a598d1e797bccce491920bf29d769880cf2fc6d3e0436`  
		Last Modified: Mon, 08 Mar 2021 22:17:48 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a95aceb58fa39c7678dd2871722d308e7da51bb6635fd623de1e9bc45a0d612`  
		Last Modified: Mon, 08 Mar 2021 22:18:50 GMT  
		Size: 9.2 MB (9176672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54383f3c5fa30fd23c18b8855a9f3afd7df04fba710979b28404e6e2e0ba1736`  
		Last Modified: Mon, 08 Mar 2021 22:18:49 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0398b52a60591eda6202fd00b49bf8ecfa0a3e5d4cf45c2af876fc598e5ac71`  
		Last Modified: Mon, 08 Mar 2021 22:18:48 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:lts` - linux; mips64le

```console
$ docker pull haproxy@sha256:68fce50fbcefd8cf3ee44e79ccbdcde6bff9062d8f7bdd31a75cd812af1dbcbf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34627259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ffbe5e71c677f9550a20a49495c9a54b1f70dad80206752ca96299f4225c481`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 03:09:26 GMT
ADD file:0222a151f4e5033d9eae98ce2b703a63f52d049dd72ac40bdd0dc2dafe619f0a in / 
# Tue, 09 Feb 2021 03:09:27 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:41:09 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 03 Mar 2021 23:10:04 GMT
ENV HAPROXY_VERSION=2.2.10
# Wed, 03 Mar 2021 23:10:05 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.10.tar.gz
# Wed, 03 Mar 2021 23:10:05 GMT
ENV HAPROXY_SHA256=a027e9cd8f703ba48dc193f5ae34d9aa152221f67ab58a4e939c96b9f4edd3bc
# Wed, 03 Mar 2021 23:12:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 Mar 2021 23:12:27 GMT
STOPSIGNAL SIGUSR1
# Wed, 03 Mar 2021 23:12:27 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 03 Mar 2021 23:12:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 03 Mar 2021 23:12:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Mar 2021 23:12:29 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:dfb81134097d874e01b495d1fba82e384056d0a3a45f01a69a2e86ae82af1e96`  
		Last Modified: Tue, 09 Feb 2021 03:15:55 GMT  
		Size: 25.8 MB (25764640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a549d56662447dd8cb15faf59ca0fc2eda7a877e9aee16aadd09fd46e4214a`  
		Last Modified: Tue, 09 Feb 2021 03:57:56 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65be8d0220e343aa0ba1db949674ff16f39389fb3c14309ce16783ed1924a1b7`  
		Last Modified: Wed, 03 Mar 2021 23:13:41 GMT  
		Size: 8.9 MB (8860669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5439ba6a6b54a0fe85acf47dcfe4b3465fd66d6d1fbe3aea3769acddab607594`  
		Last Modified: Wed, 03 Mar 2021 23:13:35 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8fde2a50b54742467311844dcb5636fd1ad40c152a43a629b366b301c582ae7`  
		Last Modified: Wed, 03 Mar 2021 23:13:35 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:lts` - linux; ppc64le

```console
$ docker pull haproxy@sha256:3efd7155a63f7105e130532a3594776248df544bd493b909bf7f206bfa656f71
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40289282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7df67eff1aab2863a69fcea96ea8af6171ff19aac7152bf3824db5f957e54064`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:19:19 GMT
ADD file:9a8cfdf0eab394a693b5cde0700ad47b6e8506ef0b79fabb8a07874b96e6c394 in / 
# Tue, 09 Feb 2021 02:19:34 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 05:52:23 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 03 Mar 2021 23:23:38 GMT
ENV HAPROXY_VERSION=2.2.10
# Wed, 03 Mar 2021 23:23:42 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.10.tar.gz
# Wed, 03 Mar 2021 23:23:48 GMT
ENV HAPROXY_SHA256=a027e9cd8f703ba48dc193f5ae34d9aa152221f67ab58a4e939c96b9f4edd3bc
# Wed, 03 Mar 2021 23:28:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 Mar 2021 23:28:21 GMT
STOPSIGNAL SIGUSR1
# Wed, 03 Mar 2021 23:28:22 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 03 Mar 2021 23:28:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 03 Mar 2021 23:28:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Mar 2021 23:28:50 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:9996b4fb6bc1c50f95ba30f8988c9c89526556fa320d3fda59d3d8359f7810d6`  
		Last Modified: Tue, 09 Feb 2021 02:27:59 GMT  
		Size: 30.5 MB (30519509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7f600bc4989eb9f12d5006a73f5958eb4fe85f86bc4008d7a899bb935b0f1c`  
		Last Modified: Tue, 09 Feb 2021 06:38:36 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b76b41179c41c897d8edf7d548f5975bec661a4f4b4dfa41bf1ad552d6b46df6`  
		Last Modified: Wed, 03 Mar 2021 23:32:16 GMT  
		Size: 9.8 MB (9767826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f9cdabeced7eb35a6a7ca4ac5e8ecfa86ef0670b1d2037fbc9d3815cf733c9`  
		Last Modified: Wed, 03 Mar 2021 23:32:14 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d15db81144a7e1545a6f22b92ab6c4d2d16eedd0eef2aa766315b6c045d836d`  
		Last Modified: Wed, 03 Mar 2021 23:32:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:lts` - linux; s390x

```console
$ docker pull haproxy@sha256:21ed36dee62cfe436cbc1fa93fd6564f3cee16ee4a9526020f246d5b4fb16760
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34709539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f22bf5194ddcbee6e27b5238d7ecf6dd66d96194c3a650d35a5de1bcbd8510a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:42:10 GMT
ADD file:0edb2de05df54191a141bd125f59d7e14eef0cc4576927a247b8dd7d6f255d04 in / 
# Tue, 09 Feb 2021 02:42:12 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:39:30 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 03 Mar 2021 23:43:15 GMT
ENV HAPROXY_VERSION=2.2.10
# Wed, 03 Mar 2021 23:43:16 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.10.tar.gz
# Wed, 03 Mar 2021 23:43:16 GMT
ENV HAPROXY_SHA256=a027e9cd8f703ba48dc193f5ae34d9aa152221f67ab58a4e939c96b9f4edd3bc
# Wed, 03 Mar 2021 23:43:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 Mar 2021 23:43:52 GMT
STOPSIGNAL SIGUSR1
# Wed, 03 Mar 2021 23:43:52 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 03 Mar 2021 23:43:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 03 Mar 2021 23:43:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Mar 2021 23:43:55 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:032413a44cf56b097e48b8221bf475ca1bec26e7a27f35fe61d699366a335b79`  
		Last Modified: Tue, 09 Feb 2021 02:45:31 GMT  
		Size: 25.7 MB (25710021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e65f701864562492efa2c0035134b62d68efdb6e7241a0a2dcc3151e6d5775b`  
		Last Modified: Tue, 09 Feb 2021 03:44:28 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2f87d09b1e4f93d137fcd4aca47d17548c96dc51b1974840f8582386165439a`  
		Last Modified: Wed, 03 Mar 2021 23:46:18 GMT  
		Size: 9.0 MB (8997573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4014d184cd70f402072c04852e6e2af2abfaac153e70d6d1cd20a31bdbcb4663`  
		Last Modified: Wed, 03 Mar 2021 23:46:15 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e21792cc4eacae1d21897fd6dc774923fca5fd0aeb505e893846a21c4e3fe06`  
		Last Modified: Wed, 03 Mar 2021 23:46:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haproxy:lts-alpine`

```console
$ docker pull haproxy@sha256:4396bf1f43cbeea0f4e2d651b9989685b505d474a347c10855b41dcf49aa7a1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `haproxy:lts-alpine` - linux; amd64

```console
$ docker pull haproxy@sha256:2f877531092feb1a6596ee8bc6eb00d9d993dab984715d4ce3513805df05aa02
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9177632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2549b4a31f8af89b6bdb4695a4a59374b47fd8b40b8df2f2c20628da267486d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 21:19:54 GMT
ADD file:80bf8bd014071345b1c0364eeb0a5e48f3fb0d87f9c31cb990e57caa652b59b8 in / 
# Wed, 17 Feb 2021 21:19:54 GMT
CMD ["/bin/sh"]
# Mon, 08 Mar 2021 21:38:26 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 21:43:17 GMT
ENV HAPROXY_VERSION=2.2.10
# Mon, 08 Mar 2021 21:43:17 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.10.tar.gz
# Mon, 08 Mar 2021 21:43:17 GMT
ENV HAPROXY_SHA256=a027e9cd8f703ba48dc193f5ae34d9aa152221f67ab58a4e939c96b9f4edd3bc
# Mon, 08 Mar 2021 21:44:18 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Mon, 08 Mar 2021 21:44:18 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 21:44:18 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 21:44:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 08 Mar 2021 21:44:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 21:44:20 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:ba3557a56b150f9b813f9d02274d62914fd8fce120dd374d9ee17b87cf1d277d`  
		Last Modified: Wed, 17 Feb 2021 21:20:25 GMT  
		Size: 2.8 MB (2811657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9216237f12c4d44ab183590086cf2a09004b5609c4b50871d88658faa495245`  
		Last Modified: Mon, 08 Mar 2021 21:52:45 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ab448b61e71513906284c50caa18b4bbead3c9f4e44e9563a51155483cc814`  
		Last Modified: Mon, 08 Mar 2021 21:53:58 GMT  
		Size: 6.4 MB (6364220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1496e8d1fc05d2242dec46f741fd8fb5b7f5f763ff5fe19ac959ef58db7c8c15`  
		Last Modified: Mon, 08 Mar 2021 21:53:46 GMT  
		Size: 448.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c883a4dc2f6239a275129836cd6fe8c66fc9f419c95de34ba15df40807eadd0`  
		Last Modified: Mon, 08 Mar 2021 21:53:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:lts-alpine` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:dce2bd7fdb71321a8829f51ee51fe1f8df12ede9854586f628de4bf9b6b390c5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8871339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07e6e2e4dd3516d94cc27ed41c046bad56909aff74a5eebdb69d23185cf56e6e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 20:49:32 GMT
ADD file:c04fbd3b039001c592cfa14f8388f8934ed4223ccf274dbb926e75039e172af4 in / 
# Wed, 17 Feb 2021 20:49:33 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 21:08:27 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 03 Mar 2021 23:53:11 GMT
ENV HAPROXY_VERSION=2.2.10
# Wed, 03 Mar 2021 23:53:13 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.10.tar.gz
# Wed, 03 Mar 2021 23:53:14 GMT
ENV HAPROXY_SHA256=a027e9cd8f703ba48dc193f5ae34d9aa152221f67ab58a4e939c96b9f4edd3bc
# Wed, 03 Mar 2021 23:53:47 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 03 Mar 2021 23:53:48 GMT
STOPSIGNAL SIGUSR1
# Wed, 03 Mar 2021 23:53:49 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 03 Mar 2021 23:53:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 03 Mar 2021 23:53:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Mar 2021 23:53:57 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:1353527ebe111f9bb1e271264a3c182e909e4b36463f80d7dbde1be0713eb892`  
		Last Modified: Wed, 17 Feb 2021 20:50:06 GMT  
		Size: 2.6 MB (2622039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d174378d3ee2c0c6e6a85b5228f929557826d80bcd23b2434093942f499361a7`  
		Last Modified: Wed, 17 Feb 2021 21:12:31 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d92e731bf4971bbb56699109cc2c7bf258a08b8c71fd2ce618628ed0b4be2b1a`  
		Last Modified: Wed, 03 Mar 2021 23:55:11 GMT  
		Size: 6.2 MB (6247545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8313b91724ce11e0d69d1f84cd9ba8ce0fd4dd4784e6deb2c2987413db0b472b`  
		Last Modified: Wed, 03 Mar 2021 23:55:09 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528f6166aa7000e8e0a6ddf712ac1e81bc5ddee4e5003b80a6542ad199662e23`  
		Last Modified: Wed, 03 Mar 2021 23:55:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:lts-alpine` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:bd8a4e822b3d304f69ee657b808cc512c82005f7986e37a1b61a8308e14d5ba5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8588802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0035fe4ee0d310975e18c33d050c0fed342d40fc90715c6b91982cb91f1aa0fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 20:57:36 GMT
ADD file:efdd39e5243eaf378f12ad5a85d2222b44930850a90263e5f17e8a6b5e9bc9b8 in / 
# Wed, 17 Feb 2021 20:57:37 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 21:49:42 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Thu, 04 Mar 2021 00:04:07 GMT
ENV HAPROXY_VERSION=2.2.10
# Thu, 04 Mar 2021 00:04:09 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.10.tar.gz
# Thu, 04 Mar 2021 00:04:12 GMT
ENV HAPROXY_SHA256=a027e9cd8f703ba48dc193f5ae34d9aa152221f67ab58a4e939c96b9f4edd3bc
# Thu, 04 Mar 2021 00:04:46 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Thu, 04 Mar 2021 00:04:47 GMT
STOPSIGNAL SIGUSR1
# Thu, 04 Mar 2021 00:04:49 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Thu, 04 Mar 2021 00:04:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 04 Mar 2021 00:04:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 00:04:55 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f55b840e27d3dbe27e44497103a4397f043749f933eb0433d29e2f104b3435ef`  
		Last Modified: Wed, 17 Feb 2021 20:58:14 GMT  
		Size: 2.4 MB (2423892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86398e5ccaeed703d9464d57f2d97546fad0481312144292414eb1cf857b617f`  
		Last Modified: Wed, 17 Feb 2021 21:55:00 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00ad0cba7b2138c19356311eceb6fd5d2af2432778f97cf07d9b384d5524278`  
		Last Modified: Thu, 04 Mar 2021 00:07:00 GMT  
		Size: 6.2 MB (6163153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b337734f16cc0eff0d2bb38d7431f457cd7992e4992f77789263d6611d7e407b`  
		Last Modified: Thu, 04 Mar 2021 00:06:58 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb03a37f226d57efe43f03eb956ef49a20693dc865f15de068de3f08e6c56aba`  
		Last Modified: Thu, 04 Mar 2021 00:06:58 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:lts-alpine` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:9df40d9acef87692f82a74b70ce1d60af5cca36f61239d82d12433ed0af482d8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9083113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e914a0cee60954b5adb34a5fd43d3fa4698fb1e4747afcaca9006dbc9e6c4cf2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 20:39:29 GMT
ADD file:3bf1497bd250cf7c73c12231dc4ebe3a3a67f2cd99e35bce47ef6674683aeb1d in / 
# Wed, 17 Feb 2021 20:39:30 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 21:36:08 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 03 Mar 2021 23:43:05 GMT
ENV HAPROXY_VERSION=2.2.10
# Wed, 03 Mar 2021 23:43:06 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.10.tar.gz
# Wed, 03 Mar 2021 23:43:07 GMT
ENV HAPROXY_SHA256=a027e9cd8f703ba48dc193f5ae34d9aa152221f67ab58a4e939c96b9f4edd3bc
# Wed, 03 Mar 2021 23:43:29 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 03 Mar 2021 23:43:30 GMT
STOPSIGNAL SIGUSR1
# Wed, 03 Mar 2021 23:43:31 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 03 Mar 2021 23:43:33 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 03 Mar 2021 23:43:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Mar 2021 23:43:35 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:069a56d6d07f6b186fbb82e4486616b9be9a37ce32a63013af6cddcb65898182`  
		Last Modified: Wed, 17 Feb 2021 20:40:04 GMT  
		Size: 2.7 MB (2711572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6644620fa9074da825714fc7794756e2b0e36f3e83ffc2bc01bbc9df0de9e373`  
		Last Modified: Wed, 17 Feb 2021 21:41:18 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a59369a058df1f7b291ab7b129ef07290c2a99545bea6f42cfa0f54436183bb`  
		Last Modified: Wed, 03 Mar 2021 23:45:22 GMT  
		Size: 6.4 MB (6369785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e982f4480ea14efe8106105e56424bc6bee3368b3299cd98b1aad1e5609140`  
		Last Modified: Wed, 03 Mar 2021 23:45:20 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffebf1b2b70d66bcbda9707eb957d0e25635210167d94d991cc7e81130ded334`  
		Last Modified: Wed, 03 Mar 2021 23:45:20 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:lts-alpine` - linux; 386

```console
$ docker pull haproxy@sha256:659a38f29b31e96bd5aecab83a003f3f09e1eb5eebd43d6169b02ac77d8ed7be
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9012210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c724357a8f8f4b645b234f5584c0748d1a8db582d156e91d506d5574ccf1b2ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 21:38:34 GMT
ADD file:eaee53da3c87749799de55809e4a5b526c56855332b961a85b1184c660f1d65b in / 
# Wed, 17 Feb 2021 21:38:35 GMT
CMD ["/bin/sh"]
# Mon, 08 Mar 2021 22:03:53 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 22:08:22 GMT
ENV HAPROXY_VERSION=2.2.10
# Mon, 08 Mar 2021 22:08:22 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.10.tar.gz
# Mon, 08 Mar 2021 22:08:22 GMT
ENV HAPROXY_SHA256=a027e9cd8f703ba48dc193f5ae34d9aa152221f67ab58a4e939c96b9f4edd3bc
# Mon, 08 Mar 2021 22:09:21 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Mon, 08 Mar 2021 22:09:21 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 22:09:21 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 22:09:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 08 Mar 2021 22:09:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 22:09:23 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:86205afa28f6bc624469015a543d16608258d2828411a92c662f4fdc6d276e18`  
		Last Modified: Wed, 17 Feb 2021 21:39:07 GMT  
		Size: 2.8 MB (2818177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080e85d941540171ac6a020af17b393f2a40b03d40b9677d708d31ffb6e31b71`  
		Last Modified: Mon, 08 Mar 2021 22:18:02 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dafe934780af9f6588fe0b199a4c0b60e557597c52ed66de79f143c33b9f40c`  
		Last Modified: Mon, 08 Mar 2021 22:19:06 GMT  
		Size: 6.2 MB (6192281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6792eb8d4ba43ae0b592f09026d5cc688e72235dc893697be4e2b5c446409863`  
		Last Modified: Mon, 08 Mar 2021 22:19:04 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:682c8c2e4bc6bc83b8e4eea6ff73da639b17e212f85d36a5407aadb8a64f9024`  
		Last Modified: Mon, 08 Mar 2021 22:19:04 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:lts-alpine` - linux; ppc64le

```console
$ docker pull haproxy@sha256:7c55559ea5e08f971f817d05e45bb569929812dd49110cc075bde9c0c74fbf8b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9496257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fa09275b3a555d9d28aca6380470a700262bc2fa9550d6cceefe3327d8299af`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 21:17:29 GMT
ADD file:28f4377c61c0f8eb43a6b36e6a24ef5893f51d405d25b62e364988223537ae0b in / 
# Wed, 17 Feb 2021 21:17:37 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 22:10:46 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 03 Mar 2021 23:29:05 GMT
ENV HAPROXY_VERSION=2.2.10
# Wed, 03 Mar 2021 23:29:08 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.10.tar.gz
# Wed, 03 Mar 2021 23:29:12 GMT
ENV HAPROXY_SHA256=a027e9cd8f703ba48dc193f5ae34d9aa152221f67ab58a4e939c96b9f4edd3bc
# Wed, 03 Mar 2021 23:29:57 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 03 Mar 2021 23:30:06 GMT
STOPSIGNAL SIGUSR1
# Wed, 03 Mar 2021 23:30:07 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 03 Mar 2021 23:30:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 03 Mar 2021 23:30:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Mar 2021 23:30:34 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:cb672e0375a8f9bb3d33049ceb372ffa49b959bfc84fe6f72bfb97b682a608c8`  
		Last Modified: Wed, 17 Feb 2021 21:18:10 GMT  
		Size: 2.8 MB (2813081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f391a7d74b9bf5c2089e7957996d00d99ddc33d8295873bf28746716bb728a`  
		Last Modified: Wed, 17 Feb 2021 22:23:02 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3895621bf409c59caef35106ecb9c73d57db6ab26c83e908bb2f846ce3b2420e`  
		Last Modified: Wed, 03 Mar 2021 23:32:35 GMT  
		Size: 6.7 MB (6681415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a16f70021d25609a108a39f41eff539ab12df1aba78f8d87564a9022864f65d`  
		Last Modified: Wed, 03 Mar 2021 23:32:34 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67bc8b05d75cf8717f438ad79f81f009294c601e828c4cbd406b08d167bd4f80`  
		Last Modified: Wed, 03 Mar 2021 23:32:34 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:lts-alpine` - linux; s390x

```console
$ docker pull haproxy@sha256:5882e4526d054b2db8cdc8b0478d1a2b56273796af2dcc87c2fcd3b9b38f0dcf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8934271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97f0501dfe1a6477b450f2c11dc0f5c7db80bea48457a4de575e5798fd920abe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 17 Feb 2021 20:41:27 GMT
ADD file:630c66f8d774d75b51e32aff812b438d377ebd3389c4aa6c324fdf8c03b6fa13 in / 
# Wed, 17 Feb 2021 20:41:27 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 21:33:33 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 03 Mar 2021 23:44:04 GMT
ENV HAPROXY_VERSION=2.2.10
# Wed, 03 Mar 2021 23:44:04 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.10.tar.gz
# Wed, 03 Mar 2021 23:44:05 GMT
ENV HAPROXY_SHA256=a027e9cd8f703ba48dc193f5ae34d9aa152221f67ab58a4e939c96b9f4edd3bc
# Wed, 03 Mar 2021 23:44:42 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 		&& wget -O haproxy.tar.gz "$HAPROXY_URL" 	&& echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c 	&& mkdir -p /usr/src/haproxy 	&& tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1 	&& rm haproxy.tar.gz 		&& makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	' 	&& nproc="$(getconf _NPROCESSORS_ONLN)" 	&& eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts" 	&& eval "make -C /usr/src/haproxy install-bin $makeOpts" 		&& mkdir -p /usr/local/etc/haproxy 	&& cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors 	&& rm -rf /usr/src/haproxy 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .haproxy-rundeps $runDeps 	&& apk del --no-network .build-deps
# Wed, 03 Mar 2021 23:44:43 GMT
STOPSIGNAL SIGUSR1
# Wed, 03 Mar 2021 23:44:43 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 03 Mar 2021 23:44:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 03 Mar 2021 23:44:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Mar 2021 23:44:44 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:ff5e8cb87555e9fa38a441f5cf0414e91353e2cd21cdb48d48b7de5bb39ce674`  
		Last Modified: Wed, 17 Feb 2021 20:41:58 GMT  
		Size: 2.6 MB (2602381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de25a3a0de168e6603cb978691ef3e7f11d7c9108d0ade38d3185d5d9dbdc094`  
		Last Modified: Wed, 17 Feb 2021 21:43:59 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc37ee0272550cdbed16f03b4d75571d970685b3a0c7b8d29484c919d8a9705`  
		Last Modified: Wed, 03 Mar 2021 23:46:27 GMT  
		Size: 6.3 MB (6330135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36a50696ff802571b01c8fa6b843837fc6b5e23d4948b2b73404ce94b9fa2ee`  
		Last Modified: Wed, 03 Mar 2021 23:46:26 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5abb15abe9d69125c600f2786dc4197578896c9d134fc5233bbbfcbcd125744`  
		Last Modified: Wed, 03 Mar 2021 23:46:27 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
