## `haproxy:bookworm`

```console
$ docker pull haproxy@sha256:90b48a89c0c05db64be3dece40fa2e726d1f0f9ef989b58d22821980afff9a74
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `haproxy:bookworm` - linux; amd64

```console
$ docker pull haproxy@sha256:42c372f5ae0415559dd84f7737ecfb01e4812db7d9559fb22a06c4611b6cd7cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.8 MB (41781392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1974ef943cbd4be3918b4d3ce0f4dbfd94e2ffe3c574943f5fe6950ca5dd84f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Thu, 17 Apr 2025 17:13:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Apr 2025 17:13:29 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 17 Apr 2025 17:13:29 GMT
ENV HAPROXY_VERSION=3.1.7
# Thu, 17 Apr 2025 17:13:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.7.tar.gz
# Thu, 17 Apr 2025 17:13:29 GMT
ENV HAPROXY_SHA256=a3952644ef939b36260d91d81a335636aa9b44572b4cb8b6001272f88545c666
# Thu, 17 Apr 2025 17:13:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 17 Apr 2025 17:13:29 GMT
STOPSIGNAL SIGUSR1
# Thu, 17 Apr 2025 17:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 17 Apr 2025 17:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Apr 2025 17:13:29 GMT
USER haproxy
# Thu, 17 Apr 2025 17:13:29 GMT
WORKDIR /var/lib/haproxy
# Thu, 17 Apr 2025 17:13:29 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ad64f8fe64e86dfcb798b7f58f63c9b0707d74669a24c91e45b69326acde5c`  
		Last Modified: Thu, 17 Apr 2025 18:30:29 GMT  
		Size: 3.5 MB (3499342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0cf6a78796719086e8577a9c086906e2247d03a2dfbf258d88d9941e0406f3`  
		Last Modified: Thu, 17 Apr 2025 18:30:29 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc835e4fc840b4c3e3db2c43cbd119f8f3bd60079c5f73836fd0de0d12768ab`  
		Last Modified: Thu, 17 Apr 2025 18:30:29 GMT  
		Size: 10.1 MB (10053146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43a8e5df452aae064702d86375f53ba63ff527a2e3833e797ca166ee0949c056`  
		Last Modified: Thu, 17 Apr 2025 18:30:29 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:4d811b50c17a87da510c5f4700145868ef8ac8f1a3bbb7e2bc2f6af24d2d6544
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2392180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff38b9cc7dd406d905b8ebfec668bc75df3dd76765b64187e50166c679b15f7f`

```dockerfile
```

-	Layers:
	-	`sha256:8eb3f829e03e155b1b1c78d12db40e0b532ca2e7ed38da5ed82d0c0fbd557530`  
		Last Modified: Thu, 17 Apr 2025 18:30:29 GMT  
		Size: 2.4 MB (2370407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:deb2a128740255a8179e9f833292c55cb7a0abb01a76da953f6eaae31e8d614a`  
		Last Modified: Thu, 17 Apr 2025 18:30:29 GMT  
		Size: 21.8 KB (21773 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:40cf6c1ec10ebad08424293e5a9309066529a08674e931570297017b6db5c6e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38939407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d00f7faac8bddb77ee9c1b9fe44f3c6243907e57348a43b54f9f8f233b412e9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1743984000'
# Thu, 17 Apr 2025 17:13:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Apr 2025 17:13:29 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 17 Apr 2025 17:13:29 GMT
ENV HAPROXY_VERSION=3.1.7
# Thu, 17 Apr 2025 17:13:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.7.tar.gz
# Thu, 17 Apr 2025 17:13:29 GMT
ENV HAPROXY_SHA256=a3952644ef939b36260d91d81a335636aa9b44572b4cb8b6001272f88545c666
# Thu, 17 Apr 2025 17:13:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 17 Apr 2025 17:13:29 GMT
STOPSIGNAL SIGUSR1
# Thu, 17 Apr 2025 17:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 17 Apr 2025 17:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Apr 2025 17:13:29 GMT
USER haproxy
# Thu, 17 Apr 2025 17:13:29 GMT
WORKDIR /var/lib/haproxy
# Thu, 17 Apr 2025 17:13:29 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:bee0b90cda85f033e5343bbd7872c95c9de54d2dbe2fe864e9cb4b10716bc994`  
		Last Modified: Tue, 08 Apr 2025 00:23:07 GMT  
		Size: 25.8 MB (25757818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76da0305b2b23f80b1908c2ce6cdaee30c7f0a90503be88e1a607ebd5d8c65f1`  
		Last Modified: Tue, 08 Apr 2025 01:15:14 GMT  
		Size: 3.1 MB (3073460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab545fcf5aee846efc6cba753da45cc34479d11f27cd91a73b4d9791ccec82a5`  
		Last Modified: Tue, 08 Apr 2025 01:15:13 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccfbd97b6f7e3afb6d026134138e128b9ced8fca08fe59830468d99d4ebd785e`  
		Last Modified: Thu, 17 Apr 2025 18:30:01 GMT  
		Size: 10.1 MB (10106487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96383ebc20b4112016877efc61510d18e47671b6d7558fdb8c00bf84ebc64fde`  
		Last Modified: Thu, 17 Apr 2025 18:30:01 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:f90ae46ad559f8079d5811913f9277bd145a1017a5f2ef41c242136fc73b7393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2395812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2558bacd7034f3877d1adaa9384f0197343f5ad6398e2e021a93b665e529fdec`

```dockerfile
```

-	Layers:
	-	`sha256:f850f6a2a62a1c1de8e5024dc0e8b4943718d1c0dd0a5a524e5f24e98c75a21a`  
		Last Modified: Thu, 17 Apr 2025 18:30:01 GMT  
		Size: 2.4 MB (2373921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de36e1a0398317e7a83dba4ae58410e4480696dd37ac3da74e13cf62a6d207e4`  
		Last Modified: Thu, 17 Apr 2025 18:30:00 GMT  
		Size: 21.9 KB (21891 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:d4333ffb209dcccd73b6a834f05c9b5c88dd7e19c1938378e88cbaaf6c254bd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.7 MB (36743557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f50ad7db4568fe33e35d007c4c2a24a6bc0f93dc1606038b4d070bff530041ec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
# Thu, 17 Apr 2025 17:13:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Apr 2025 17:13:29 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 17 Apr 2025 17:13:29 GMT
ENV HAPROXY_VERSION=3.1.7
# Thu, 17 Apr 2025 17:13:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.7.tar.gz
# Thu, 17 Apr 2025 17:13:29 GMT
ENV HAPROXY_SHA256=a3952644ef939b36260d91d81a335636aa9b44572b4cb8b6001272f88545c666
# Thu, 17 Apr 2025 17:13:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 17 Apr 2025 17:13:29 GMT
STOPSIGNAL SIGUSR1
# Thu, 17 Apr 2025 17:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 17 Apr 2025 17:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Apr 2025 17:13:29 GMT
USER haproxy
# Thu, 17 Apr 2025 17:13:29 GMT
WORKDIR /var/lib/haproxy
# Thu, 17 Apr 2025 17:13:29 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:addc1be20d0979aa781d79a726ebf749adbc030186e63a44319274194e89cfa3`  
		Last Modified: Tue, 08 Apr 2025 00:23:15 GMT  
		Size: 23.9 MB (23937867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428b9af88c849258200dfe951d2ab46f39e95311b0593488e6b7736531419708`  
		Last Modified: Tue, 08 Apr 2025 01:16:30 GMT  
		Size: 2.9 MB (2907779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c335d0f71373bed2334812b2451b30088049a848c153af540562a7ffe26d439`  
		Last Modified: Tue, 08 Apr 2025 01:16:30 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb4eebcdb3df9d4b75426de7a0398751c3d4176272fc9688d2e2a7a5b65afda`  
		Last Modified: Thu, 17 Apr 2025 18:48:47 GMT  
		Size: 9.9 MB (9896268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a099f9e26f7c6060535a3ca9e06e0a44b934968b8d03a13075d34235a9881f27`  
		Last Modified: Thu, 17 Apr 2025 18:48:46 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:d8e151103316cb269c9edb56eb8a8eb62e233448712f3e5ff19cb45bd5db1de3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2394538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b3363ba8ff3b42259fd6f79730a992e33aebc56d32e3a60ac6a116e296919b4`

```dockerfile
```

-	Layers:
	-	`sha256:fe554a83e62c25ae218c03bb04496d27569df98581caf6f82727f9c78d0713cc`  
		Last Modified: Thu, 17 Apr 2025 18:48:46 GMT  
		Size: 2.4 MB (2372650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba4cf167cb1005ccca12c0f01b0583954b8b7ecd97d0bc70ddc3af26b9c2fa14`  
		Last Modified: Thu, 17 Apr 2025 18:48:46 GMT  
		Size: 21.9 KB (21888 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:3fecca0db9d02ab02894d3bec890d80256cb1ce92f260397ba0c6c12a6de0ec7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 MB (41401200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be43ba7fa8a5dd7d5e42dee14cc26637a5dea1725cdee59dd63676b26653b169`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 20 Mar 2025 17:16:47 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Thu, 20 Mar 2025 17:16:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 17:16:47 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 20 Mar 2025 17:16:47 GMT
ENV HAPROXY_VERSION=3.1.6
# Thu, 20 Mar 2025 17:16:47 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.6.tar.gz
# Thu, 20 Mar 2025 17:16:47 GMT
ENV HAPROXY_SHA256=21852e4a374bb8d9b3dda5dc834afe6557f422d7029f4fe3eac3c305f5124760
# Thu, 20 Mar 2025 17:16:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 20 Mar 2025 17:16:47 GMT
STOPSIGNAL SIGUSR1
# Thu, 20 Mar 2025 17:16:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 17:16:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 17:16:47 GMT
USER haproxy
# Thu, 20 Mar 2025 17:16:47 GMT
WORKDIR /var/lib/haproxy
# Thu, 20 Mar 2025 17:16:47 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aa2de5f47784eeac44d104145d3ce6fb0c0af731d1f98c56441ce3ffeed401d`  
		Last Modified: Tue, 08 Apr 2025 01:17:12 GMT  
		Size: 3.3 MB (3322887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97dad2f5675b0cdf464e63a9b48c409ac612b17f996bbf7b338c749f6fda86c4`  
		Last Modified: Tue, 08 Apr 2025 01:17:12 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49615b5a6bf3d444903a8e01790c8183126167cc99e8f23a7ff248e0430c0a27`  
		Last Modified: Tue, 08 Apr 2025 01:19:35 GMT  
		Size: 10.0 MB (10010354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0ee4ecb5d45fcad351e6b6011f65c34123af9f34495aa671a28310be28b6c24`  
		Last Modified: Tue, 08 Apr 2025 01:19:34 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:1ff98df2d74fe56fd59e4268697be68e179aab01276656c5bc70881b136225bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2392620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e20b3dedc9b6a30fb528594f9bd698f73f5a8a26b3b22857383498c52fdcb43`

```dockerfile
```

-	Layers:
	-	`sha256:8cac33ca28437b139b78ba3bf5d6e278f63f151198ab6dda1a78d66658b212db`  
		Last Modified: Tue, 08 Apr 2025 01:19:34 GMT  
		Size: 2.4 MB (2370690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c408df15502a8d78e7cc774a9a409b5c8f03628613730d9e6278afc508dbf7ce`  
		Last Modified: Tue, 08 Apr 2025 01:19:34 GMT  
		Size: 21.9 KB (21930 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; 386

```console
$ docker pull haproxy@sha256:b64cfe5f854f1499afd4c591f4d3210c0542209a82d63a532cbb8934ff94efd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.4 MB (42441552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e76e6ea18d6b4f1455e055dfaf4e17e73b2e175f0e86744178313a01a3a360f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1743984000'
# Thu, 17 Apr 2025 17:13:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Apr 2025 17:13:29 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 17 Apr 2025 17:13:29 GMT
ENV HAPROXY_VERSION=3.1.7
# Thu, 17 Apr 2025 17:13:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.7.tar.gz
# Thu, 17 Apr 2025 17:13:29 GMT
ENV HAPROXY_SHA256=a3952644ef939b36260d91d81a335636aa9b44572b4cb8b6001272f88545c666
# Thu, 17 Apr 2025 17:13:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 17 Apr 2025 17:13:29 GMT
STOPSIGNAL SIGUSR1
# Thu, 17 Apr 2025 17:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 17 Apr 2025 17:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Apr 2025 17:13:29 GMT
USER haproxy
# Thu, 17 Apr 2025 17:13:29 GMT
WORKDIR /var/lib/haproxy
# Thu, 17 Apr 2025 17:13:29 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:e4fab02059329179b6416bda7cdc389d26699f1c93a02194f146c047031c4748`  
		Last Modified: Tue, 08 Apr 2025 00:23:49 GMT  
		Size: 29.2 MB (29210731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4212f93a452b8888ec2486aca12c7ec6f28b33ce4ab21415f5e626533790a4e`  
		Last Modified: Thu, 17 Apr 2025 18:30:25 GMT  
		Size: 3.5 MB (3503438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffe4ef28d62ea21100dfb09ff6e1791eeb1548dd76c1bd9c1cda711bc27a167d`  
		Last Modified: Thu, 17 Apr 2025 18:30:25 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a861541523b7fe86fea4702f1fc9f838efdbdedbc2eff1cccc491e275803061`  
		Last Modified: Thu, 17 Apr 2025 18:30:26 GMT  
		Size: 9.7 MB (9725736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e591ce0a5c51a0f165bb607e6736780d808756f32db63d23b70d3cfeeda9a09`  
		Last Modified: Thu, 17 Apr 2025 18:30:25 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:7cfd42bce5c3020de5b43381d706ee55e548b4760aeec6629e308dc17f6be053
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2389257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d55f37b4c3a1174ffc0f3a111b802db62e5f4582d8b754b5fe759cd5485ab79c`

```dockerfile
```

-	Layers:
	-	`sha256:486a45b9ded802b6e589b99939d849d290e5537b44025aaa075a7995c5c501b3`  
		Last Modified: Thu, 17 Apr 2025 18:30:25 GMT  
		Size: 2.4 MB (2367535 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d42e18a7e0f2f9172063342dc1726e14bedb640ef9bc398dec685a92a578560`  
		Last Modified: Thu, 17 Apr 2025 18:30:25 GMT  
		Size: 21.7 KB (21722 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; mips64le

```console
$ docker pull haproxy@sha256:8fee5b844124eea16a84b2ca783bdeeb525f7799db16a93e7799a2e1d9aa8ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.6 MB (41593507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6635ab6fc7199faae000659cef821417a651a4b181232d0ff9afb36e6dd6738f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1743984000'
# Thu, 17 Apr 2025 17:13:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Apr 2025 17:13:29 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 17 Apr 2025 17:13:29 GMT
ENV HAPROXY_VERSION=3.1.7
# Thu, 17 Apr 2025 17:13:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.7.tar.gz
# Thu, 17 Apr 2025 17:13:29 GMT
ENV HAPROXY_SHA256=a3952644ef939b36260d91d81a335636aa9b44572b4cb8b6001272f88545c666
# Thu, 17 Apr 2025 17:13:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 17 Apr 2025 17:13:29 GMT
STOPSIGNAL SIGUSR1
# Thu, 17 Apr 2025 17:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 17 Apr 2025 17:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Apr 2025 17:13:29 GMT
USER haproxy
# Thu, 17 Apr 2025 17:13:29 GMT
WORKDIR /var/lib/haproxy
# Thu, 17 Apr 2025 17:13:29 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c5170849255c666bce01dd02c1afbe442b1ecb682c342680d91dcd7cd477b57d`  
		Last Modified: Tue, 08 Apr 2025 00:23:28 GMT  
		Size: 28.5 MB (28513953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6949d2412d1813d925526134f33bbbd4b60e21f566ca57a9d89acc7ac2b8b0d6`  
		Last Modified: Tue, 08 Apr 2025 01:29:32 GMT  
		Size: 2.9 MB (2895366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821b52f5ed8e1f10c8be219e38ade04f17a5c6e6f88d0c36e73271efde31de0c`  
		Last Modified: Tue, 08 Apr 2025 01:29:31 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0953b8d5430c180f2ab666ec8046d1a8be546994c627ce522eed4413a8373a85`  
		Last Modified: Thu, 17 Apr 2025 18:34:06 GMT  
		Size: 10.2 MB (10182540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f3993b11253d17d95b246ec690b7d0148d9d81c88c3196d15295748911926d`  
		Last Modified: Thu, 17 Apr 2025 18:34:05 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:33ce628cfc50e92beca25e369e381118f9a3232684d26c1d4fd318fd6745cec7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 KB (21647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec5603a800a2373c4fdb2a85f4131988698ca893ae2356feedccb9c49dc0f916`

```dockerfile
```

-	Layers:
	-	`sha256:12a620ce0ae4fca4ed69b79b2fa0b03c53c0bbf6692652e19a8c4ce40055b896`  
		Last Modified: Thu, 17 Apr 2025 18:34:05 GMT  
		Size: 21.6 KB (21647 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; ppc64le

```console
$ docker pull haproxy@sha256:8eed3819f9d4c98ef7e595d629b00d0403371d99dc6555a3034791c26853a12e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46296729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98e1f933982318b97f5ba389c9465cbd8e41110c3677f52d7d4780b10bcd9d5b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 20 Mar 2025 17:16:47 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1743984000'
# Thu, 20 Mar 2025 17:16:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 17:16:47 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 20 Mar 2025 17:16:47 GMT
ENV HAPROXY_VERSION=3.1.6
# Thu, 20 Mar 2025 17:16:47 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.6.tar.gz
# Thu, 20 Mar 2025 17:16:47 GMT
ENV HAPROXY_SHA256=21852e4a374bb8d9b3dda5dc834afe6557f422d7029f4fe3eac3c305f5124760
# Thu, 20 Mar 2025 17:16:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 20 Mar 2025 17:16:47 GMT
STOPSIGNAL SIGUSR1
# Thu, 20 Mar 2025 17:16:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 17:16:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 17:16:47 GMT
USER haproxy
# Thu, 20 Mar 2025 17:16:47 GMT
WORKDIR /var/lib/haproxy
# Thu, 20 Mar 2025 17:16:47 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:eda04574e09a8e08ba343dd01ac61bceb64282d2e992a997bd2102897b52d004`  
		Last Modified: Tue, 08 Apr 2025 00:23:44 GMT  
		Size: 32.1 MB (32068231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42468877a74e57c50c11233c777cffdbaa83d62017691c314be00ed02fbee779`  
		Last Modified: Tue, 08 Apr 2025 01:19:17 GMT  
		Size: 3.7 MB (3702920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e733c236b1c36a34f8989c83253cc91216e17a8ae4d8df75664f2bf82c25fc8`  
		Last Modified: Tue, 08 Apr 2025 01:19:16 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1427191d29aacf717049fda9846c58069e47de2a344df69208cad55fd22906a2`  
		Last Modified: Tue, 08 Apr 2025 01:21:08 GMT  
		Size: 10.5 MB (10523939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e181d903712fbeb2af3be7f1e030b32e382b14226be26dde654dc2f630b473b`  
		Last Modified: Tue, 08 Apr 2025 01:21:07 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:2f7f339729d15491299d612f692f2acdf4c084b7219fa2ca0f2da315a78ef00d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2396554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72b9cf5b0938bc8c3b27866781673971dcdeb65e8450b0ece89459d1aca39866`

```dockerfile
```

-	Layers:
	-	`sha256:48080222a15a7e4da2eee4245184e726c89a26401c62b5bc7e2c12e2c4937b23`  
		Last Modified: Tue, 08 Apr 2025 01:21:08 GMT  
		Size: 2.4 MB (2374721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:541e3d58dfed9a9b483b00147678b90af5a9db8cfe07fca89dea4ae19ee0a871`  
		Last Modified: Tue, 08 Apr 2025 01:21:07 GMT  
		Size: 21.8 KB (21833 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; s390x

```console
$ docker pull haproxy@sha256:7080276b0bf7a08e971eb90136ddd0b06de7c7b141ccca422fc9c5b42aa8dd3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.0 MB (39963206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8de9da0e6f709b89aaec9988d770c6dd12166742938a013815acd214ed532c75`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 20 Mar 2025 17:16:47 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1743984000'
# Thu, 20 Mar 2025 17:16:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 17:16:47 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 20 Mar 2025 17:16:47 GMT
ENV HAPROXY_VERSION=3.1.6
# Thu, 20 Mar 2025 17:16:47 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.6.tar.gz
# Thu, 20 Mar 2025 17:16:47 GMT
ENV HAPROXY_SHA256=21852e4a374bb8d9b3dda5dc834afe6557f422d7029f4fe3eac3c305f5124760
# Thu, 20 Mar 2025 17:16:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 20 Mar 2025 17:16:47 GMT
STOPSIGNAL SIGUSR1
# Thu, 20 Mar 2025 17:16:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 17:16:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 17:16:47 GMT
USER haproxy
# Thu, 20 Mar 2025 17:16:47 GMT
WORKDIR /var/lib/haproxy
# Thu, 20 Mar 2025 17:16:47 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:4d39bd57bcf7f4854587de5b4defd11e1b3b354bad1320b74c6994d07d7b3671`  
		Last Modified: Tue, 08 Apr 2025 00:24:14 GMT  
		Size: 26.9 MB (26884606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b5390cf33ec28c798a2df11ec64efd7f989ab7db3d4d33d56e88209a2178b13`  
		Last Modified: Tue, 08 Apr 2025 01:15:45 GMT  
		Size: 3.2 MB (3163368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcfffa6b73ae4d5d069267e9a17062dd54eecf9383eca25920655be9d759a569`  
		Last Modified: Tue, 08 Apr 2025 01:15:41 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9483b9753af7f1a3d1ca3de92f9b177cd15bc979aaa841610a7b404dc8f1f3ea`  
		Last Modified: Tue, 08 Apr 2025 01:16:48 GMT  
		Size: 9.9 MB (9913594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dee83a03a84a2e421fc3fe57e7272ca76545b9794a4695bd61094d577457957`  
		Last Modified: Tue, 08 Apr 2025 01:16:48 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:b7367d79396c9184d9508a61810608c001ae5206b6aca63143cdda900f32fb69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2391898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dbcdb96a17a9ba9b013f6316c37fd5006dfd0d3767ed5dd94b822bf1d9e5c01`

```dockerfile
```

-	Layers:
	-	`sha256:f11850df15da11e54f5ba3430747df42dd606cebc9ff1ec2181b9fed20ae5b75`  
		Last Modified: Tue, 08 Apr 2025 01:16:47 GMT  
		Size: 2.4 MB (2370129 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a85d9546a696323aaa691d3b48a9de9f88a304f32da4dd2ed9139a63d1b920b`  
		Last Modified: Tue, 08 Apr 2025 01:16:47 GMT  
		Size: 21.8 KB (21769 bytes)  
		MIME: application/vnd.in-toto+json
