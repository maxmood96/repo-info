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
-	[`memcached:1.6.23`](#memcached1623)
-	[`memcached:1.6.23-alpine`](#memcached1623-alpine)
-	[`memcached:1.6.23-alpine3.19`](#memcached1623-alpine319)
-	[`memcached:1.6.23-bookworm`](#memcached1623-bookworm)
-	[`memcached:alpine`](#memcachedalpine)
-	[`memcached:alpine3.19`](#memcachedalpine319)
-	[`memcached:bookworm`](#memcachedbookworm)
-	[`memcached:latest`](#memcachedlatest)

## `memcached:1`

```console
$ docker pull memcached@sha256:fa6c8e150e7b7af5e6f05ad388bbf5f4f34925e17aef12fc494ffdef7b3911cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 15
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
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
$ docker pull memcached@sha256:643a24a57407d3cb2b8745f47a8d4b20406c19f5399ecb05db9727447637003a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38789237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d474793fb4125ae857b42efbf79eb1cbea8834a20e5d65627ea439b52b57313`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:27 GMT
ADD file:ac3cd70031d35e46d86b876934946ffc8756de4de065fbc926dce642dac07ff3 in / 
# Tue, 19 Dec 2023 01:20:28 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:af107e978371b6cd6339127a05502c5eacd1e6b0e9eb7b2f4aa7b6fc87e2dd81`  
		Last Modified: Tue, 19 Dec 2023 01:24:59 GMT  
		Size: 29.1 MB (29125963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d32ccca352404a5a8dedb6a7ca281abbc073b9d8643ef4626873ee1b8a204b1`  
		Last Modified: Wed, 10 Jan 2024 23:58:24 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d585b71055b9f919875cf91a81370309c971aad943e53b8c9fda2b63521f873`  
		Last Modified: Wed, 10 Jan 2024 23:58:25 GMT  
		Size: 2.5 MB (2488298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc47ad75df3e3af04459ae59b5c7ec1ea8dd657b7fb4cc42ec85a982a98da628`  
		Last Modified: Wed, 10 Jan 2024 23:58:25 GMT  
		Size: 7.2 MB (7173458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66204efbd683596758bec893cba01fce3fe386da63399af101051d8df26c2477`  
		Last Modified: Wed, 10 Jan 2024 23:58:25 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3406bc9285b7e906c211fd9a5d9342ee80d9e0ae728a6529d14db42aecf145`  
		Last Modified: Wed, 10 Jan 2024 23:58:25 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:8efa487487fc160476637a4fb2aec45b4a38eb677aeddcd0ecaeab362e136e85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3077977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:928c59acdba2c812e1299dcb8c4a4c7a7bdfadbc695533aab940957913a8b768`

```dockerfile
```

-	Layers:
	-	`sha256:7777c14054a0e9893c312cf26a23d80bb2f16d3cd6dacad21c21c8fb1be321a4`  
		Last Modified: Wed, 10 Jan 2024 23:58:25 GMT  
		Size: 3.1 MB (3056860 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc8d2dbb4d2d164636bb06f04252d4aec50002cf7469a8955e322e104563d025`  
		Last Modified: Wed, 10 Jan 2024 23:58:24 GMT  
		Size: 21.1 KB (21117 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm variant v5

```console
$ docker pull memcached@sha256:d01aca5f5e26f687d6ad14ec6547e704f453acc02ce0ce2e5fa5871f5013bfbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34811390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f12a90da675230d99a32d19f573412751d7740cae5f90d74a8c49b4b6f64a3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 19 Dec 2023 01:55:22 GMT
ADD file:9503ab966c9dd707eeccc7c2f633bccc94c199f8714ec4ff2c8b54dde3dbabf9 in / 
# Tue, 19 Dec 2023 01:55:22 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1ae9a2844c8c70942d2220553689b62e841cc706d77284fbfedbd770080fd699`  
		Last Modified: Tue, 19 Dec 2023 01:58:33 GMT  
		Size: 26.9 MB (26885440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ab650f4c7d61856342d3b0e4d9bad9cd0c4336fb403dab9c5c1ed2c285774f`  
		Last Modified: Thu, 11 Jan 2024 00:07:53 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b10807a0745d6e1ccc36157b11a3469a17c6477eda65233bb2f182c7958db5b8`  
		Last Modified: Thu, 11 Jan 2024 00:07:54 GMT  
		Size: 2.1 MB (2089356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5bc9bbfb0a70ce84a09ce58d70ebf97841c03e06d3968f065cd9361bd0e990`  
		Last Modified: Thu, 11 Jan 2024 00:07:54 GMT  
		Size: 5.8 MB (5835079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74b3373a0a7639196238720db6061026ccfe87c48ccf38fcfbc737699c9f2b7`  
		Last Modified: Thu, 11 Jan 2024 00:07:53 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3969d1f7528c0ba1d0047402bf5611d53c8f502f52fbbd7fb827f8de5ab813f6`  
		Last Modified: Thu, 11 Jan 2024 00:07:54 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:7484a951008b8e170922f1467a179c839a675cf4ab9555315f6bb20174be8173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3052683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d85ee8bbb3867fa9cbdd5e06e5791b62e1c7dfc410295ba05b95ead8b6c4525`

```dockerfile
```

-	Layers:
	-	`sha256:34e791a9d4149137cb6b8da59558d4bf4ce80c9bcd5ab599785c7a3aaa2fc844`  
		Last Modified: Thu, 11 Jan 2024 00:07:54 GMT  
		Size: 3.0 MB (3031592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31263ce608cc2e18001c08b34ad8f21b27befcf21ee30dd42bd87176f24a5e10`  
		Last Modified: Thu, 11 Jan 2024 00:07:53 GMT  
		Size: 21.1 KB (21091 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; arm variant v7

```console
$ docker pull memcached@sha256:2841be0a36134563966c09a6ed68b21053d20342ec8736cf92763c28077ead43
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28094215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cf74ffa940dd93988fc0beb6698c5796563c82a40b7dd668153969f64d2e6ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 09 Feb 2023 06:12:09 GMT
ADD file:5f1a343224e8486690bd90dd1e50c8d84b3d770c51bb6829544e5cf650c0419c in / 
# Thu, 09 Feb 2023 06:12:10 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 07:52:31 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Thu, 09 Feb 2023 07:52:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 07:52:35 GMT
ENV MEMCACHED_VERSION=1.6.18
# Thu, 09 Feb 2023 07:52:35 GMT
ENV MEMCACHED_SHA1=be16909bb75ab972ee5fe438312501de01c4725a
# Thu, 09 Feb 2023 07:55:44 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Thu, 09 Feb 2023 07:55:44 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 09 Feb 2023 07:55:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 09 Feb 2023 07:55:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Feb 2023 07:55:44 GMT
USER memcache
# Thu, 09 Feb 2023 07:55:45 GMT
EXPOSE 11211
# Thu, 09 Feb 2023 07:55:45 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:e7318f6106ad75d7d482ae9dddf4d927b0872ef3ddb6e1330aa691fc8d17279e`  
		Last Modified: Thu, 09 Feb 2023 06:19:19 GMT  
		Size: 26.6 MB (26577666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de49d9d72daf1680b5f1b9532dd2eb0162829f36c8db9669935462636fbf99d9`  
		Last Modified: Thu, 09 Feb 2023 08:06:11 GMT  
		Size: 4.9 KB (4895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0beac9d5bcac946f8c54c72b8a9c136914b1aa7a5fe2b8c3df4c7d8858ea6559`  
		Last Modified: Thu, 09 Feb 2023 08:06:11 GMT  
		Size: 312.1 KB (312088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4c9e5a265394e4c0f357779e6195a4e82d767a3691a0e77d427e56651c3e54a`  
		Last Modified: Thu, 09 Feb 2023 08:06:11 GMT  
		Size: 1.2 MB (1199163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ea82ad892fe1ae8623d84e32c8c027087cda8aa49e40d4546ed6942e471c60`  
		Last Modified: Thu, 09 Feb 2023 08:06:11 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2ae3bcdc0d114ba49a67df022b6f7215fc87f1f50e64939fcfbbec4eaadee5`  
		Last Modified: Thu, 09 Feb 2023 08:06:11 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:1b119620b1cbaac4281975bedfed15ff721d868ec9eda9574dc4c1ec58330716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37686962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45b76a80b62f56ff1c68ed4e7ce2dfe225b3560e00750a3210c8d897b1547f3a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:11 GMT
ADD file:262fd7bf0bc26e5d2a229fba52626e22b8a93beac29733acfc60e716c26e689d in / 
# Tue, 19 Dec 2023 01:41:11 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:24e221e92a36ab5b0075dd156b4f2ff095532a9b0927946cf6070bb1bea208b8`  
		Last Modified: Tue, 19 Dec 2023 01:44:38 GMT  
		Size: 29.2 MB (29157269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d79fe3da079136cc418087e5d4e432357c062519668a3c03b78c24710c3a6ec`  
		Last Modified: Wed, 20 Dec 2023 10:20:11 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:496388416e6f8cdbf05e6ea4a56e906308e4b95b9f984f73b5c5a3fdbe5b12aa`  
		Last Modified: Wed, 20 Dec 2023 10:20:11 GMT  
		Size: 2.3 MB (2346023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee91bf234e7544eb6ad4c5f18ba87a8c0306d87f51ee1c47b1361569175a8a7c`  
		Last Modified: Thu, 11 Jan 2024 00:20:26 GMT  
		Size: 6.2 MB (6182151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73888be7ca392dfe14270a838c67a2d7ccfe9354f1fe52147291c9756127b51`  
		Last Modified: Thu, 11 Jan 2024 00:20:25 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a917a1ebe539f36501d4bebb89957491c647a119a1702734b1a0c9c01dc2a6`  
		Last Modified: Thu, 11 Jan 2024 00:20:25 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:f96d1dde1233068de191226772289ac63a784a466d34ec1dbf67e72559643f7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3053019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f249bf848fae6f5b573dffd3d8dbd830fd3267c6f487d397fd82ba104fee46b`

```dockerfile
```

-	Layers:
	-	`sha256:09c490b7c5d08149f654887eca9ca058a49a3b659d3e7282589a431883445a49`  
		Last Modified: Thu, 11 Jan 2024 00:20:25 GMT  
		Size: 3.0 MB (3032051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abe3c6e55476a176987bc5b5f8bad00ca16d1299d36e40f52e82dcb76ed0600c`  
		Last Modified: Thu, 11 Jan 2024 00:20:25 GMT  
		Size: 21.0 KB (20968 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; 386

```console
$ docker pull memcached@sha256:a5d93bfce917e364c0f16cdad7b683a36011a997db4be6db2770644095aea01d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39272936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:902b98d31b0a747e1d90226bbd3f7fb16592c8f606009585e9b2bbb819bfb30e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 19 Dec 2023 01:39:07 GMT
ADD file:6f4083d57ea9644b5a827e67b0725087a15aa428272ec223ab968bf8b4623e42 in / 
# Tue, 19 Dec 2023 01:39:07 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8d4aad22fb6a12b8cc7a78d338dfb9bc2bd6d621517b374e446f2915833ea883`  
		Last Modified: Tue, 19 Dec 2023 01:43:45 GMT  
		Size: 30.1 MB (30143863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22ddf2b3cd1581c8f1483d20c8fb232852e525fea04a97ffd9ac744939dffc0`  
		Last Modified: Wed, 10 Jan 2024 23:58:29 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23537023da95e2b44ae9e7aebee71e05ecb397f02a351f30f6c69a752d98d1a5`  
		Last Modified: Wed, 10 Jan 2024 23:58:29 GMT  
		Size: 2.5 MB (2492560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8636f3d8b77edac77347698b78afe5ce4f443daa01f0a424d809c8ed35405ac5`  
		Last Modified: Wed, 10 Jan 2024 23:58:29 GMT  
		Size: 6.6 MB (6634994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41afb4f2ebc199845ca27aae99895e43658c24f7fbdea6a0b17769f1fd238b3f`  
		Last Modified: Wed, 10 Jan 2024 23:58:29 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aee346987d8e42b5a7c3ecdc4b2efa5e402c43f65712c94e3f30606c9b365e4`  
		Last Modified: Wed, 10 Jan 2024 23:58:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:71cbd1b0df460e30d13a768ed26659ea3d35001b788219b4eac0d77078e71ab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3072225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7173243e71de72bb179738a15514dee35cfb9c1f1ab3da05adc2fd1ea74335cf`

```dockerfile
```

-	Layers:
	-	`sha256:4e2e18fc597957c9c8202a8015176e35b070a14ec422ca3b88fdfaa64cd693d0`  
		Last Modified: Wed, 10 Jan 2024 23:58:29 GMT  
		Size: 3.1 MB (3051163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1dc46fbcfd7dddfe981ea410938185ededc5f8f383164b2ffe266c923d1e7ed`  
		Last Modified: Wed, 10 Jan 2024 23:58:29 GMT  
		Size: 21.1 KB (21062 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; mips64le

```console
$ docker pull memcached@sha256:d6b10482cd93239feb732ab9b3bcdd207e5be672b55c01b1faa72c6e10da9ee3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37564394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bed0ab2d751422f3dfcd94712006ab27d4cdd43e18f83b8b38199c2cee3b2514`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 19 Dec 2023 02:13:36 GMT
ADD file:dcd5696ac281b24df52a518e2402c7f7a4caedfcba0d82e195b7c06cd3a38fdd in / 
# Tue, 19 Dec 2023 02:13:40 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:12b1322ffb17b8e81ca1c6d9d7118e2fcee0b9d971aa3c90601e6345804a60d1`  
		Last Modified: Tue, 19 Dec 2023 02:24:36 GMT  
		Size: 29.1 MB (29121427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6b93f134841b66512a1d4138bdf28b0506ffd27490aac735508b3f20716618`  
		Last Modified: Thu, 11 Jan 2024 00:10:54 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573e69b5f2977543c86d4410256c381ef97d7f37a89be2a88bfbda683c24110e`  
		Last Modified: Thu, 11 Jan 2024 00:10:55 GMT  
		Size: 1.9 MB (1937514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb552cccf8bd4122265e6895c4c9ce039b90dd08574f0e4911a0b11aaf1f7b2c`  
		Last Modified: Thu, 11 Jan 2024 00:10:55 GMT  
		Size: 6.5 MB (6503938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b640b85282363650ba7d87fea47ce2e4cfe96da07ab6c4b47eebc739f96910`  
		Last Modified: Thu, 11 Jan 2024 00:10:54 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933eef8a1d4865a3e302557839a52d00229ef80652113710df9fd606880475c5`  
		Last Modified: Thu, 11 Jan 2024 00:10:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:c1162ead1e62fcd87632e902387935d8f33b794c009815419baf8cb396548f85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aa26ec0ff6dd44911a88c2d2af479e0c05cfb46e9db65187abe71da51f56001`

```dockerfile
```

-	Layers:
	-	`sha256:2454765cb79a60d22f96ec7e66ea9fb222b40c30758e0df9a59c7192c39847da`  
		Last Modified: Thu, 11 Jan 2024 00:10:54 GMT  
		Size: 20.8 KB (20837 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; ppc64le

```console
$ docker pull memcached@sha256:b7976b1191a4f34442e257f55f30f8b4efd28f5f8026936846e8a5471e0c8505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.0 MB (43007490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75346431bfc757a49f790022140e267e0e6838110c75cad2bf8ab9e24e2855fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 19 Dec 2023 01:21:50 GMT
ADD file:ca1db68689e0b0388337ba450ad2c8e79c159c6b78f5aa6d3ff2b89b8d7edc93 in / 
# Tue, 19 Dec 2023 01:21:51 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fc9b8f5eec3aa37ab3aace05165427479352f290d53904cea87dca6349633a09`  
		Last Modified: Tue, 19 Dec 2023 01:26:19 GMT  
		Size: 33.1 MB (33120558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f85ae146a90d1ce7561d4e67d1ce2eaf0a0da444bb8a70c5b7fc94d0dc75e389`  
		Last Modified: Wed, 20 Dec 2023 08:43:43 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23065e9a12cf130c31375986a9b4700b84f2539ccb4b47efe0f375f77938fc3`  
		Last Modified: Wed, 20 Dec 2023 08:43:44 GMT  
		Size: 2.7 MB (2698240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b8249b30995d06e02d41e31406a930c02163d057cd39ad2cb7f710df2f6c60`  
		Last Modified: Thu, 11 Jan 2024 00:10:31 GMT  
		Size: 7.2 MB (7187176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a238b8549095cec1619f8f38f82d1aeb50acdf094b2b611b1fb5c62da14635f`  
		Last Modified: Thu, 11 Jan 2024 00:10:31 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669f29d97099310deca355ff837c9885adea00bb9c6e460490904627b7a40e4b`  
		Last Modified: Thu, 11 Jan 2024 00:10:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:87bde9e8cd8d07c6306a9ef516b822eadb9669d79da8587f1ac892066646ad33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3066464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:034c7634fd9e3419a42aa94fb6c3c05bd8d951eaf75eef2fbd2e8d64150013ba`

```dockerfile
```

-	Layers:
	-	`sha256:0a90f178efc50a3500b5ee2dce72b560153f2b0ec4cc6e79aa940561e8d58590`  
		Last Modified: Thu, 11 Jan 2024 00:10:31 GMT  
		Size: 3.0 MB (3045446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35a907ae4a36d514f4ff1b8d97766c9a5166c6116bc026f627e4de4cc51111fe`  
		Last Modified: Thu, 11 Jan 2024 00:10:30 GMT  
		Size: 21.0 KB (21018 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1` - linux; s390x

```console
$ docker pull memcached@sha256:9110d0aec3fc0be39a13bfd7030a3d04f36e230034078de3b407ae883f3e3de2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35722087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aef7bb08b32c1c17f11984770392abcc11b268465af0e89884793edf6ec092dd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 04 Dec 2023 18:08:47 GMT
ADD file:f06f12fa5a93afc3a79ac4371d24b0a471a5a1818cf34c1d90004c8f410914b9 in / 
# Mon, 04 Dec 2023 18:08:47 GMT
CMD ["bash"]
# Mon, 04 Dec 2023 18:08:47 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 04 Dec 2023 18:08:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 04 Dec 2023 18:08:47 GMT
ENV MEMCACHED_VERSION=1.6.22
# Mon, 04 Dec 2023 18:08:47 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.22.tar.gz
# Mon, 04 Dec 2023 18:08:47 GMT
ENV MEMCACHED_SHA1=7a691f390d59616dbebfc9e2e4942d499c39a338
# Mon, 04 Dec 2023 18:08:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 04 Dec 2023 18:08:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 Dec 2023 18:08:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 04 Dec 2023 18:08:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 Dec 2023 18:08:47 GMT
USER memcache
# Mon, 04 Dec 2023 18:08:47 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 04 Dec 2023 18:08:47 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bc6b1888979d3ceb063da848b2034e980e2c2613642159c1e856550b79aa620c`  
		Last Modified: Tue, 19 Dec 2023 01:47:38 GMT  
		Size: 27.5 MB (27491874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b453a12051612cbbdca8ee1a3c9e8211ac636f53786a525b824574fff746cda`  
		Last Modified: Tue, 19 Dec 2023 15:38:14 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7903f8445b1bbbe476fd67c998f57a5289b3d4a9e65a1190e551b7c79083e65d`  
		Last Modified: Tue, 19 Dec 2023 15:38:15 GMT  
		Size: 2.2 MB (2152511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf54a1600c7ab496cf3e01f5ec34a3ae7dfbf25014ef90ec9c7b005aa3d887c`  
		Last Modified: Tue, 19 Dec 2023 15:38:14 GMT  
		Size: 6.1 MB (6076186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b446e4dc631c597d82b5e437bf342d8607d8a4ff3229d052f049bfbac270e2c6`  
		Last Modified: Tue, 19 Dec 2023 15:38:14 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee453ca29f8bbd4b452693cd9f2e2e1b7cff2fa139d7fc942de190d244ae6617`  
		Last Modified: Tue, 19 Dec 2023 15:38:15 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1` - unknown; unknown

```console
$ docker pull memcached@sha256:2fa3455fc28f5964cc39eaaadcfab8df0a8dd5552a08464b0f87cbc775addb70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3067351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddb3e50e2a70d6400f4ba5be3b4010e9a0f7770e69e2c1e1c599bf6224ed8ac8`

```dockerfile
```

-	Layers:
	-	`sha256:2dcfb5805d88251b9b79a3c0e144091f0dc62a366eddacb9d50aa89a825067ef`  
		Last Modified: Tue, 19 Dec 2023 15:38:14 GMT  
		Size: 3.0 MB (3046401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb52cc58a7fa498aa7b56431dbe3e004db5d4b028b724bc1f087b44c1baaa25c`  
		Last Modified: Tue, 19 Dec 2023 15:38:14 GMT  
		Size: 20.9 KB (20950 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine`

```console
$ docker pull memcached@sha256:df6a80f20b17df1f452b325ba2bee57644473669cb08fc928d55417da18cb786
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 11
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
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
$ docker pull memcached@sha256:32affe08f4a1c6f62faacae1fee90575987d8b995a7257aa35ca1b4a817bdbf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6528299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fba850e40285109fcdc4c5603f2e081dba5bb683ffbcf0d4ad2e954359ce93e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 08 Dec 2023 01:20:49 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Fri, 08 Dec 2023 01:20:49 GMT
CMD ["/bin/sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd74bdcd28e46833593b2724720938c58842faa843fe42ea2411b3afd0739cb6`  
		Last Modified: Wed, 10 Jan 2024 23:58:18 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104a06a5eef3fffb9db79f8f67d4205725b9551aadbad7cb2847b013921bc212`  
		Last Modified: Wed, 10 Jan 2024 23:58:18 GMT  
		Size: 104.2 KB (104204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3271524d49893bc0950a7d058e91621dcfabe2383d6bfc0b13263faaf85f774f`  
		Last Modified: Wed, 10 Jan 2024 23:58:18 GMT  
		Size: 3.0 MB (3013977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb917829c49dd9d022cf427a72685718c30e113cfe036cffdf3eec29523e871`  
		Last Modified: Wed, 10 Jan 2024 23:58:18 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c390a9d8c6874260017223d74f3ae0b04895aa29a26c6ea03e0bd49832fe201`  
		Last Modified: Wed, 10 Jan 2024 23:58:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:a4db06e4e22e5cb6667aafc4b272349d5db9596147a2114d7b6997ae75e265f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 KB (98074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80b0a8c4800de05bc28d0cf54908bd75ed706e519dc72a22883d057213a1afdd`

```dockerfile
```

-	Layers:
	-	`sha256:9052d3e673c4418bce0a5b5c01961846c1fc2b14ace86d3afae91720a4744b70`  
		Last Modified: Wed, 10 Jan 2024 23:58:18 GMT  
		Size: 78.6 KB (78603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:667e7c7f728f9119016e4a456207d31154a85c080f74151700cc04835b950d54`  
		Last Modified: Wed, 10 Jan 2024 23:58:18 GMT  
		Size: 19.5 KB (19471 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:79a5646a0c845a791f36017fda3292281b48295b06c53f13d62c9f94237d4731
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3960292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2afac0e49af3ce3f1769abe11a29f8f5610c6a736d8c5b6c7b9770c8d8e94e91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 16 Dec 2020 23:58:14 GMT
ADD file:bd07f77a2b2741ca6bda80d9203be9c7274cf73145bff778cf000db0d8d4e903 in / 
# Wed, 16 Dec 2020 23:58:15 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 06:43:29 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Thu, 17 Dec 2020 06:43:31 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Thu, 17 Dec 2020 06:43:33 GMT
ENV MEMCACHED_VERSION=1.6.9
# Thu, 17 Dec 2020 06:43:35 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Thu, 17 Dec 2020 06:46:32 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Thu, 17 Dec 2020 06:46:33 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 17 Dec 2020 06:46:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 17 Dec 2020 06:46:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 06:46:36 GMT
USER memcache
# Thu, 17 Dec 2020 06:46:38 GMT
EXPOSE 11211
# Thu, 17 Dec 2020 06:46:39 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c58e8a26a8407acc3ead776f6526efa889fda03270a8d05109208d9f59159420`  
		Last Modified: Wed, 16 Dec 2020 23:58:59 GMT  
		Size: 2.4 MB (2407555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68564bbfc09f153688e942bf54d5375d1e27f3507c0bed6b038c2ac8ce095aa5`  
		Last Modified: Thu, 17 Dec 2020 06:46:58 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cac3a91edee49d0b08a25706ae86059bed89941a08b496e72ef092e57c4ecb3`  
		Last Modified: Thu, 17 Dec 2020 06:46:58 GMT  
		Size: 13.8 KB (13825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf16e9bb942ec42a35a792beab65aea843209e7bdde7e856499b9fc85f93bc4e`  
		Last Modified: Thu, 17 Dec 2020 06:46:58 GMT  
		Size: 1.5 MB (1537248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc15394239bd0c083e1b6df806aa5ffeb8b9cc7e80113afc2959721de49f90d1`  
		Last Modified: Thu, 17 Dec 2020 06:46:58 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:482f0eb571548eae5720c652ff7da13558e56a8722dc9932cf7eb1ef3eb33acb`  
		Last Modified: Thu, 17 Dec 2020 06:46:58 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:5550c34a395e8c02098f113a01d35d794b40c31c374f1e553dc80472d53978c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6372430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f4edcab8bc23e09f91d9a22a6d9df2a2d0175c23ad7cd396eaa4e849528f0e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 08 Dec 2023 01:39:30 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 08 Dec 2023 01:39:30 GMT
CMD ["/bin/sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c303524923177661067f7eb378c3dd5277088c2676ebd1cd78e68397bb80fdbf`  
		Last Modified: Fri, 08 Dec 2023 01:39:48 GMT  
		Size: 3.3 MB (3347794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfede01b081f27465377bdafbbdb6b694c6fab18026972b2c380535dcef103b8`  
		Last Modified: Wed, 13 Dec 2023 01:35:47 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d7b6f4ad45bf3aee58c5a7e8083286bd79dc004840903fd5997929772bfb4c`  
		Last Modified: Wed, 13 Dec 2023 01:35:47 GMT  
		Size: 120.9 KB (120897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f6c7840c606bfa580e1e6b52087faff29fb3986005ea3aadc31c64b3e4142e`  
		Last Modified: Thu, 11 Jan 2024 00:22:58 GMT  
		Size: 2.9 MB (2902089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1335fd4bd25daf4820a1c881f1ea0a30a575682074ad886293a372089bcd4544`  
		Last Modified: Thu, 11 Jan 2024 00:22:58 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48e51e3a0b635d352137fa3c7c3747c8192e7c8de0590e533ffdcea9dc49a96`  
		Last Modified: Thu, 11 Jan 2024 00:22:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:6faa51abf4ec7649d68a12af15126861e91479130b3f97128d3fa7a487d62422
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.9 KB (97945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e975d798c27c70d9498c44491a9aca9d24cee1fe8111bfae46401e7d9b1264`

```dockerfile
```

-	Layers:
	-	`sha256:0c5c585bb2d781fc112b82e19d343028a3c75758809ef4b46e4a6839bd0a1e41`  
		Last Modified: Thu, 11 Jan 2024 00:22:58 GMT  
		Size: 78.6 KB (78622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed5eb3630ee14af5005edfb5ed56d4660a5bbf224bf729ca0bfabaa0143d9864`  
		Last Modified: Thu, 11 Jan 2024 00:22:58 GMT  
		Size: 19.3 KB (19323 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; 386

```console
$ docker pull memcached@sha256:67373b38ed96c7ba59d5c1b8ba2b471d75d058ae7056f1e22674128af0e39ece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6185193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ec7484601b2ef9f91318f7c210dbd58716132fdd37be8004e82af4e4d42015b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 08 Dec 2023 01:38:25 GMT
ADD file:bd52540f209ba362654d795d7893669c819d35011a16f9f319301727a33b3bd9 in / 
# Fri, 08 Dec 2023 01:38:25 GMT
CMD ["/bin/sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9acd8b4c9d4385585f74dabb4bc6b3351888710ae37ec5dbd9ea950281b8f9bb`  
		Last Modified: Fri, 08 Dec 2023 01:38:43 GMT  
		Size: 3.2 MB (3244115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7759a4b7aa772576870eb5c52f815fbebd9be11b4781c708dc2ab6007fa609`  
		Last Modified: Wed, 10 Jan 2024 23:58:26 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5ca5419371cb9331b9ba1ea9086eef15ad135bf369ac2787491caf04de682f`  
		Last Modified: Wed, 10 Jan 2024 23:58:26 GMT  
		Size: 109.3 KB (109334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc68a66ccf11c1510081e6e9f70c399ad3ceff564e9b876ed2895ebf29b3ebb`  
		Last Modified: Wed, 10 Jan 2024 23:58:26 GMT  
		Size: 2.8 MB (2830103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b15634bddb0499598a6044cc0030e88ba0ce4cf2b02301cfa0a0faa1ac676cdd`  
		Last Modified: Wed, 10 Jan 2024 23:58:26 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dddc1630ef7eb2545abf068534d7032d19114a744cd485791f63f40ab0b5ab18`  
		Last Modified: Wed, 10 Jan 2024 23:58:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:15c53491df84b3d051fdcc7dff9dbdb9ca3718254ea873b6e2bbff7bc221abec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.0 KB (97973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fee76928da54f07fd68a5975f71e6f5991ccd3261cf759f3093b424e8f7ba99`

```dockerfile
```

-	Layers:
	-	`sha256:1ae5a47e6fefaee5dc9532fb45757803475b71d80ddf777a416ccd10c45bd09e`  
		Last Modified: Wed, 10 Jan 2024 23:58:26 GMT  
		Size: 78.6 KB (78558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ae992c52298a54654430860ae3828320c41eec63e8702ef1c66f1a68fdb937e`  
		Last Modified: Wed, 10 Jan 2024 23:58:26 GMT  
		Size: 19.4 KB (19415 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:0639819cf6cbfd6e608ef2071abeb9ca10f049a89ecc83eee11f1d75b78cab2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6394995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12d25d4724561e2ace36bab912780d035fdb57c760fa9268b40e781584c2df0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 08 Dec 2023 01:22:51 GMT
ADD file:052421189f8d269382daaaa8beb63c687e4d8ca908c421abdce53bcc627a40b4 in / 
# Fri, 08 Dec 2023 01:22:51 GMT
CMD ["/bin/sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:243ac51c334a47917a84be93e972ee6378987e9b3b917a5a8df29025e161c1f3`  
		Last Modified: Fri, 08 Dec 2023 01:23:14 GMT  
		Size: 3.4 MB (3358233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add73e7dbebd6c86078686bb046ef57017b090fe917f656feb83ec0ef971b5f3`  
		Last Modified: Tue, 12 Dec 2023 23:20:17 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d64bed657a7e728633e13f2021b35954e98be9ecae77096d30cdaa1d9260d61e`  
		Last Modified: Tue, 12 Dec 2023 23:20:17 GMT  
		Size: 123.4 KB (123403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a69dac8774b0ef6bdf9b84b7360fb3346a88b05e510dbc3366a3a828349a839b`  
		Last Modified: Thu, 11 Jan 2024 00:13:43 GMT  
		Size: 2.9 MB (2911714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666eeed87216ed83fdc1a618d27175e1a8c8efd15354f7e22228e768ded7a7cf`  
		Last Modified: Thu, 11 Jan 2024 00:13:42 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfeab30e174bcb0fc8203612135497885d25cfc588a1e44de9e5b0b5048dcdb`  
		Last Modified: Thu, 11 Jan 2024 00:13:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:d20e9002675244162fdaf77d022444958c1a6d56dfe5901853240c568aea24b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 KB (96397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e870214daaeaabaf116e4a0a6462f63bc3d9ce9cd3d522277e53ba1d9c19a54e`

```dockerfile
```

-	Layers:
	-	`sha256:54016ce6ca1c0550269f0db7f3fec4511d81bef96b3c0f41709d785c7cefa5d3`  
		Last Modified: Thu, 11 Jan 2024 00:13:42 GMT  
		Size: 77.0 KB (77025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28bbe767bea18a4ae8896d545c4083a8a7a41145031227bdf28474500598aa2f`  
		Last Modified: Thu, 11 Jan 2024 00:13:42 GMT  
		Size: 19.4 KB (19372 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:53d0bdb491815057b9014ab30e95c68146d83accdc9d8d690e308e67e7f4eed5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4326665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b078f3aede6257187e9488318eac328332ace90ac171c8a99d0ca495e1e9ad40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 08 Dec 2023 01:41:50 GMT
ADD file:47e0982fc3ae485c06d46f3c0022afd39ed7ec95fe755c2391e6b0cfcae65dfc in / 
# Fri, 08 Dec 2023 01:41:51 GMT
CMD ["/bin/sh"]
# Sat, 09 Dec 2023 01:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 09 Dec 2023 01:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 09 Dec 2023 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.22
# Sat, 09 Dec 2023 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.22.tar.gz
# Sat, 09 Dec 2023 01:54:10 GMT
ENV MEMCACHED_SHA1=7a691f390d59616dbebfc9e2e4942d499c39a338
# Sat, 09 Dec 2023 01:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 09 Dec 2023 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 09 Dec 2023 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 09 Dec 2023 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 09 Dec 2023 01:54:10 GMT
USER memcache
# Sat, 09 Dec 2023 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 09 Dec 2023 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0fca3ee44ced87b7184bc23390283fdf10cfae0e844a25b785dd11c463815227`  
		Last Modified: Fri, 08 Dec 2023 01:42:30 GMT  
		Size: 3.2 MB (3242332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff601679be7ba19260a77b326cf587dcc37315b02c2e0b0effc7084da4684bd7`  
		Last Modified: Wed, 13 Dec 2023 00:39:43 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b2401b35befb0832d96cebfdee6215736b27c0e3d064d67da9917deca4c14c`  
		Last Modified: Wed, 13 Dec 2023 00:39:43 GMT  
		Size: 113.1 KB (113142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59b1e1447b7739e5338731014a96bea369258cbf54b2d152ef50bb06e308bad`  
		Last Modified: Wed, 13 Dec 2023 00:39:43 GMT  
		Size: 969.5 KB (969547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c62bb151b09d73f2bc083bb91abedfb6660c5045d34f7d576415190ae4e09f`  
		Last Modified: Wed, 13 Dec 2023 00:39:43 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaaf7e6dbf7fbf661d0b3f6f5d38fbd888ab6707a76919a5f4a633194e895a2f`  
		Last Modified: Wed, 13 Dec 2023 00:39:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:1c2ba4c72ac494072ca8249e1368c9974cec5e63ff363b9da79930b7a8fbb5cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.3 KB (96269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c33c986fa5bcf287e1c7594cc4bc4b13289d51ef15c3db591e513fcb7b653ce`

```dockerfile
```

-	Layers:
	-	`sha256:358b294b5bd4c90ab3ded38657baddb4cf8a5d594c5ea9c5683191efc2c70e05`  
		Last Modified: Wed, 13 Dec 2023 00:39:43 GMT  
		Size: 77.0 KB (76967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:708c671c1199a85cfb58a91ad4f1c34c29d381f2905468f64a42c8fbb6341e30`  
		Last Modified: Wed, 13 Dec 2023 00:39:43 GMT  
		Size: 19.3 KB (19302 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-alpine3.19`

```console
$ docker pull memcached@sha256:72f79c540a7204a0355f57a8e3080831c646db96684c69b6a47d36f70fc33cae
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
$ docker pull memcached@sha256:32affe08f4a1c6f62faacae1fee90575987d8b995a7257aa35ca1b4a817bdbf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6528299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fba850e40285109fcdc4c5603f2e081dba5bb683ffbcf0d4ad2e954359ce93e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 08 Dec 2023 01:20:49 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Fri, 08 Dec 2023 01:20:49 GMT
CMD ["/bin/sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd74bdcd28e46833593b2724720938c58842faa843fe42ea2411b3afd0739cb6`  
		Last Modified: Wed, 10 Jan 2024 23:58:18 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104a06a5eef3fffb9db79f8f67d4205725b9551aadbad7cb2847b013921bc212`  
		Last Modified: Wed, 10 Jan 2024 23:58:18 GMT  
		Size: 104.2 KB (104204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3271524d49893bc0950a7d058e91621dcfabe2383d6bfc0b13263faaf85f774f`  
		Last Modified: Wed, 10 Jan 2024 23:58:18 GMT  
		Size: 3.0 MB (3013977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb917829c49dd9d022cf427a72685718c30e113cfe036cffdf3eec29523e871`  
		Last Modified: Wed, 10 Jan 2024 23:58:18 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c390a9d8c6874260017223d74f3ae0b04895aa29a26c6ea03e0bd49832fe201`  
		Last Modified: Wed, 10 Jan 2024 23:58:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:a4db06e4e22e5cb6667aafc4b272349d5db9596147a2114d7b6997ae75e265f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 KB (98074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80b0a8c4800de05bc28d0cf54908bd75ed706e519dc72a22883d057213a1afdd`

```dockerfile
```

-	Layers:
	-	`sha256:9052d3e673c4418bce0a5b5c01961846c1fc2b14ace86d3afae91720a4744b70`  
		Last Modified: Wed, 10 Jan 2024 23:58:18 GMT  
		Size: 78.6 KB (78603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:667e7c7f728f9119016e4a456207d31154a85c080f74151700cc04835b950d54`  
		Last Modified: Wed, 10 Jan 2024 23:58:18 GMT  
		Size: 19.5 KB (19471 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:5550c34a395e8c02098f113a01d35d794b40c31c374f1e553dc80472d53978c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6372430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f4edcab8bc23e09f91d9a22a6d9df2a2d0175c23ad7cd396eaa4e849528f0e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 08 Dec 2023 01:39:30 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 08 Dec 2023 01:39:30 GMT
CMD ["/bin/sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c303524923177661067f7eb378c3dd5277088c2676ebd1cd78e68397bb80fdbf`  
		Last Modified: Fri, 08 Dec 2023 01:39:48 GMT  
		Size: 3.3 MB (3347794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfede01b081f27465377bdafbbdb6b694c6fab18026972b2c380535dcef103b8`  
		Last Modified: Wed, 13 Dec 2023 01:35:47 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d7b6f4ad45bf3aee58c5a7e8083286bd79dc004840903fd5997929772bfb4c`  
		Last Modified: Wed, 13 Dec 2023 01:35:47 GMT  
		Size: 120.9 KB (120897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f6c7840c606bfa580e1e6b52087faff29fb3986005ea3aadc31c64b3e4142e`  
		Last Modified: Thu, 11 Jan 2024 00:22:58 GMT  
		Size: 2.9 MB (2902089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1335fd4bd25daf4820a1c881f1ea0a30a575682074ad886293a372089bcd4544`  
		Last Modified: Thu, 11 Jan 2024 00:22:58 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48e51e3a0b635d352137fa3c7c3747c8192e7c8de0590e533ffdcea9dc49a96`  
		Last Modified: Thu, 11 Jan 2024 00:22:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:6faa51abf4ec7649d68a12af15126861e91479130b3f97128d3fa7a487d62422
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.9 KB (97945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e975d798c27c70d9498c44491a9aca9d24cee1fe8111bfae46401e7d9b1264`

```dockerfile
```

-	Layers:
	-	`sha256:0c5c585bb2d781fc112b82e19d343028a3c75758809ef4b46e4a6839bd0a1e41`  
		Last Modified: Thu, 11 Jan 2024 00:22:58 GMT  
		Size: 78.6 KB (78622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed5eb3630ee14af5005edfb5ed56d4660a5bbf224bf729ca0bfabaa0143d9864`  
		Last Modified: Thu, 11 Jan 2024 00:22:58 GMT  
		Size: 19.3 KB (19323 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.19` - linux; 386

```console
$ docker pull memcached@sha256:67373b38ed96c7ba59d5c1b8ba2b471d75d058ae7056f1e22674128af0e39ece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6185193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ec7484601b2ef9f91318f7c210dbd58716132fdd37be8004e82af4e4d42015b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 08 Dec 2023 01:38:25 GMT
ADD file:bd52540f209ba362654d795d7893669c819d35011a16f9f319301727a33b3bd9 in / 
# Fri, 08 Dec 2023 01:38:25 GMT
CMD ["/bin/sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9acd8b4c9d4385585f74dabb4bc6b3351888710ae37ec5dbd9ea950281b8f9bb`  
		Last Modified: Fri, 08 Dec 2023 01:38:43 GMT  
		Size: 3.2 MB (3244115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7759a4b7aa772576870eb5c52f815fbebd9be11b4781c708dc2ab6007fa609`  
		Last Modified: Wed, 10 Jan 2024 23:58:26 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5ca5419371cb9331b9ba1ea9086eef15ad135bf369ac2787491caf04de682f`  
		Last Modified: Wed, 10 Jan 2024 23:58:26 GMT  
		Size: 109.3 KB (109334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc68a66ccf11c1510081e6e9f70c399ad3ceff564e9b876ed2895ebf29b3ebb`  
		Last Modified: Wed, 10 Jan 2024 23:58:26 GMT  
		Size: 2.8 MB (2830103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b15634bddb0499598a6044cc0030e88ba0ce4cf2b02301cfa0a0faa1ac676cdd`  
		Last Modified: Wed, 10 Jan 2024 23:58:26 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dddc1630ef7eb2545abf068534d7032d19114a744cd485791f63f40ab0b5ab18`  
		Last Modified: Wed, 10 Jan 2024 23:58:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:15c53491df84b3d051fdcc7dff9dbdb9ca3718254ea873b6e2bbff7bc221abec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.0 KB (97973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fee76928da54f07fd68a5975f71e6f5991ccd3261cf759f3093b424e8f7ba99`

```dockerfile
```

-	Layers:
	-	`sha256:1ae5a47e6fefaee5dc9532fb45757803475b71d80ddf777a416ccd10c45bd09e`  
		Last Modified: Wed, 10 Jan 2024 23:58:26 GMT  
		Size: 78.6 KB (78558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ae992c52298a54654430860ae3828320c41eec63e8702ef1c66f1a68fdb937e`  
		Last Modified: Wed, 10 Jan 2024 23:58:26 GMT  
		Size: 19.4 KB (19415 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.19` - linux; ppc64le

```console
$ docker pull memcached@sha256:0639819cf6cbfd6e608ef2071abeb9ca10f049a89ecc83eee11f1d75b78cab2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6394995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12d25d4724561e2ace36bab912780d035fdb57c760fa9268b40e781584c2df0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 08 Dec 2023 01:22:51 GMT
ADD file:052421189f8d269382daaaa8beb63c687e4d8ca908c421abdce53bcc627a40b4 in / 
# Fri, 08 Dec 2023 01:22:51 GMT
CMD ["/bin/sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:243ac51c334a47917a84be93e972ee6378987e9b3b917a5a8df29025e161c1f3`  
		Last Modified: Fri, 08 Dec 2023 01:23:14 GMT  
		Size: 3.4 MB (3358233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add73e7dbebd6c86078686bb046ef57017b090fe917f656feb83ec0ef971b5f3`  
		Last Modified: Tue, 12 Dec 2023 23:20:17 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d64bed657a7e728633e13f2021b35954e98be9ecae77096d30cdaa1d9260d61e`  
		Last Modified: Tue, 12 Dec 2023 23:20:17 GMT  
		Size: 123.4 KB (123403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a69dac8774b0ef6bdf9b84b7360fb3346a88b05e510dbc3366a3a828349a839b`  
		Last Modified: Thu, 11 Jan 2024 00:13:43 GMT  
		Size: 2.9 MB (2911714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666eeed87216ed83fdc1a618d27175e1a8c8efd15354f7e22228e768ded7a7cf`  
		Last Modified: Thu, 11 Jan 2024 00:13:42 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfeab30e174bcb0fc8203612135497885d25cfc588a1e44de9e5b0b5048dcdb`  
		Last Modified: Thu, 11 Jan 2024 00:13:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:d20e9002675244162fdaf77d022444958c1a6d56dfe5901853240c568aea24b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 KB (96397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e870214daaeaabaf116e4a0a6462f63bc3d9ce9cd3d522277e53ba1d9c19a54e`

```dockerfile
```

-	Layers:
	-	`sha256:54016ce6ca1c0550269f0db7f3fec4511d81bef96b3c0f41709d785c7cefa5d3`  
		Last Modified: Thu, 11 Jan 2024 00:13:42 GMT  
		Size: 77.0 KB (77025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28bbe767bea18a4ae8896d545c4083a8a7a41145031227bdf28474500598aa2f`  
		Last Modified: Thu, 11 Jan 2024 00:13:42 GMT  
		Size: 19.4 KB (19372 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.19` - linux; s390x

```console
$ docker pull memcached@sha256:53d0bdb491815057b9014ab30e95c68146d83accdc9d8d690e308e67e7f4eed5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4326665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b078f3aede6257187e9488318eac328332ace90ac171c8a99d0ca495e1e9ad40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 08 Dec 2023 01:41:50 GMT
ADD file:47e0982fc3ae485c06d46f3c0022afd39ed7ec95fe755c2391e6b0cfcae65dfc in / 
# Fri, 08 Dec 2023 01:41:51 GMT
CMD ["/bin/sh"]
# Sat, 09 Dec 2023 01:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 09 Dec 2023 01:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 09 Dec 2023 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.22
# Sat, 09 Dec 2023 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.22.tar.gz
# Sat, 09 Dec 2023 01:54:10 GMT
ENV MEMCACHED_SHA1=7a691f390d59616dbebfc9e2e4942d499c39a338
# Sat, 09 Dec 2023 01:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 09 Dec 2023 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 09 Dec 2023 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 09 Dec 2023 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 09 Dec 2023 01:54:10 GMT
USER memcache
# Sat, 09 Dec 2023 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 09 Dec 2023 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0fca3ee44ced87b7184bc23390283fdf10cfae0e844a25b785dd11c463815227`  
		Last Modified: Fri, 08 Dec 2023 01:42:30 GMT  
		Size: 3.2 MB (3242332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff601679be7ba19260a77b326cf587dcc37315b02c2e0b0effc7084da4684bd7`  
		Last Modified: Wed, 13 Dec 2023 00:39:43 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b2401b35befb0832d96cebfdee6215736b27c0e3d064d67da9917deca4c14c`  
		Last Modified: Wed, 13 Dec 2023 00:39:43 GMT  
		Size: 113.1 KB (113142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59b1e1447b7739e5338731014a96bea369258cbf54b2d152ef50bb06e308bad`  
		Last Modified: Wed, 13 Dec 2023 00:39:43 GMT  
		Size: 969.5 KB (969547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c62bb151b09d73f2bc083bb91abedfb6660c5045d34f7d576415190ae4e09f`  
		Last Modified: Wed, 13 Dec 2023 00:39:43 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaaf7e6dbf7fbf661d0b3f6f5d38fbd888ab6707a76919a5f4a633194e895a2f`  
		Last Modified: Wed, 13 Dec 2023 00:39:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:1c2ba4c72ac494072ca8249e1368c9974cec5e63ff363b9da79930b7a8fbb5cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.3 KB (96269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c33c986fa5bcf287e1c7594cc4bc4b13289d51ef15c3db591e513fcb7b653ce`

```dockerfile
```

-	Layers:
	-	`sha256:358b294b5bd4c90ab3ded38657baddb4cf8a5d594c5ea9c5683191efc2c70e05`  
		Last Modified: Wed, 13 Dec 2023 00:39:43 GMT  
		Size: 77.0 KB (76967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:708c671c1199a85cfb58a91ad4f1c34c29d381f2905468f64a42c8fbb6341e30`  
		Last Modified: Wed, 13 Dec 2023 00:39:43 GMT  
		Size: 19.3 KB (19302 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1-bookworm`

```console
$ docker pull memcached@sha256:59161db99b459a9315bbb8c52a243251d3cfcdb17f35a7900da8e5e64f0a8f32
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
$ docker pull memcached@sha256:643a24a57407d3cb2b8745f47a8d4b20406c19f5399ecb05db9727447637003a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38789237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d474793fb4125ae857b42efbf79eb1cbea8834a20e5d65627ea439b52b57313`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:27 GMT
ADD file:ac3cd70031d35e46d86b876934946ffc8756de4de065fbc926dce642dac07ff3 in / 
# Tue, 19 Dec 2023 01:20:28 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:af107e978371b6cd6339127a05502c5eacd1e6b0e9eb7b2f4aa7b6fc87e2dd81`  
		Last Modified: Tue, 19 Dec 2023 01:24:59 GMT  
		Size: 29.1 MB (29125963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d32ccca352404a5a8dedb6a7ca281abbc073b9d8643ef4626873ee1b8a204b1`  
		Last Modified: Wed, 10 Jan 2024 23:58:24 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d585b71055b9f919875cf91a81370309c971aad943e53b8c9fda2b63521f873`  
		Last Modified: Wed, 10 Jan 2024 23:58:25 GMT  
		Size: 2.5 MB (2488298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc47ad75df3e3af04459ae59b5c7ec1ea8dd657b7fb4cc42ec85a982a98da628`  
		Last Modified: Wed, 10 Jan 2024 23:58:25 GMT  
		Size: 7.2 MB (7173458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66204efbd683596758bec893cba01fce3fe386da63399af101051d8df26c2477`  
		Last Modified: Wed, 10 Jan 2024 23:58:25 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3406bc9285b7e906c211fd9a5d9342ee80d9e0ae728a6529d14db42aecf145`  
		Last Modified: Wed, 10 Jan 2024 23:58:25 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:8efa487487fc160476637a4fb2aec45b4a38eb677aeddcd0ecaeab362e136e85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3077977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:928c59acdba2c812e1299dcb8c4a4c7a7bdfadbc695533aab940957913a8b768`

```dockerfile
```

-	Layers:
	-	`sha256:7777c14054a0e9893c312cf26a23d80bb2f16d3cd6dacad21c21c8fb1be321a4`  
		Last Modified: Wed, 10 Jan 2024 23:58:25 GMT  
		Size: 3.1 MB (3056860 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc8d2dbb4d2d164636bb06f04252d4aec50002cf7469a8955e322e104563d025`  
		Last Modified: Wed, 10 Jan 2024 23:58:24 GMT  
		Size: 21.1 KB (21117 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:d01aca5f5e26f687d6ad14ec6547e704f453acc02ce0ce2e5fa5871f5013bfbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34811390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f12a90da675230d99a32d19f573412751d7740cae5f90d74a8c49b4b6f64a3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 19 Dec 2023 01:55:22 GMT
ADD file:9503ab966c9dd707eeccc7c2f633bccc94c199f8714ec4ff2c8b54dde3dbabf9 in / 
# Tue, 19 Dec 2023 01:55:22 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1ae9a2844c8c70942d2220553689b62e841cc706d77284fbfedbd770080fd699`  
		Last Modified: Tue, 19 Dec 2023 01:58:33 GMT  
		Size: 26.9 MB (26885440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ab650f4c7d61856342d3b0e4d9bad9cd0c4336fb403dab9c5c1ed2c285774f`  
		Last Modified: Thu, 11 Jan 2024 00:07:53 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b10807a0745d6e1ccc36157b11a3469a17c6477eda65233bb2f182c7958db5b8`  
		Last Modified: Thu, 11 Jan 2024 00:07:54 GMT  
		Size: 2.1 MB (2089356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5bc9bbfb0a70ce84a09ce58d70ebf97841c03e06d3968f065cd9361bd0e990`  
		Last Modified: Thu, 11 Jan 2024 00:07:54 GMT  
		Size: 5.8 MB (5835079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74b3373a0a7639196238720db6061026ccfe87c48ccf38fcfbc737699c9f2b7`  
		Last Modified: Thu, 11 Jan 2024 00:07:53 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3969d1f7528c0ba1d0047402bf5611d53c8f502f52fbbd7fb827f8de5ab813f6`  
		Last Modified: Thu, 11 Jan 2024 00:07:54 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:7484a951008b8e170922f1467a179c839a675cf4ab9555315f6bb20174be8173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3052683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d85ee8bbb3867fa9cbdd5e06e5791b62e1c7dfc410295ba05b95ead8b6c4525`

```dockerfile
```

-	Layers:
	-	`sha256:34e791a9d4149137cb6b8da59558d4bf4ce80c9bcd5ab599785c7a3aaa2fc844`  
		Last Modified: Thu, 11 Jan 2024 00:07:54 GMT  
		Size: 3.0 MB (3031592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31263ce608cc2e18001c08b34ad8f21b27befcf21ee30dd42bd87176f24a5e10`  
		Last Modified: Thu, 11 Jan 2024 00:07:53 GMT  
		Size: 21.1 KB (21091 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:1b119620b1cbaac4281975bedfed15ff721d868ec9eda9574dc4c1ec58330716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37686962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45b76a80b62f56ff1c68ed4e7ce2dfe225b3560e00750a3210c8d897b1547f3a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:11 GMT
ADD file:262fd7bf0bc26e5d2a229fba52626e22b8a93beac29733acfc60e716c26e689d in / 
# Tue, 19 Dec 2023 01:41:11 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:24e221e92a36ab5b0075dd156b4f2ff095532a9b0927946cf6070bb1bea208b8`  
		Last Modified: Tue, 19 Dec 2023 01:44:38 GMT  
		Size: 29.2 MB (29157269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d79fe3da079136cc418087e5d4e432357c062519668a3c03b78c24710c3a6ec`  
		Last Modified: Wed, 20 Dec 2023 10:20:11 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:496388416e6f8cdbf05e6ea4a56e906308e4b95b9f984f73b5c5a3fdbe5b12aa`  
		Last Modified: Wed, 20 Dec 2023 10:20:11 GMT  
		Size: 2.3 MB (2346023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee91bf234e7544eb6ad4c5f18ba87a8c0306d87f51ee1c47b1361569175a8a7c`  
		Last Modified: Thu, 11 Jan 2024 00:20:26 GMT  
		Size: 6.2 MB (6182151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73888be7ca392dfe14270a838c67a2d7ccfe9354f1fe52147291c9756127b51`  
		Last Modified: Thu, 11 Jan 2024 00:20:25 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a917a1ebe539f36501d4bebb89957491c647a119a1702734b1a0c9c01dc2a6`  
		Last Modified: Thu, 11 Jan 2024 00:20:25 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:f96d1dde1233068de191226772289ac63a784a466d34ec1dbf67e72559643f7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3053019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f249bf848fae6f5b573dffd3d8dbd830fd3267c6f487d397fd82ba104fee46b`

```dockerfile
```

-	Layers:
	-	`sha256:09c490b7c5d08149f654887eca9ca058a49a3b659d3e7282589a431883445a49`  
		Last Modified: Thu, 11 Jan 2024 00:20:25 GMT  
		Size: 3.0 MB (3032051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abe3c6e55476a176987bc5b5f8bad00ca16d1299d36e40f52e82dcb76ed0600c`  
		Last Modified: Thu, 11 Jan 2024 00:20:25 GMT  
		Size: 21.0 KB (20968 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:a5d93bfce917e364c0f16cdad7b683a36011a997db4be6db2770644095aea01d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39272936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:902b98d31b0a747e1d90226bbd3f7fb16592c8f606009585e9b2bbb819bfb30e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 19 Dec 2023 01:39:07 GMT
ADD file:6f4083d57ea9644b5a827e67b0725087a15aa428272ec223ab968bf8b4623e42 in / 
# Tue, 19 Dec 2023 01:39:07 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8d4aad22fb6a12b8cc7a78d338dfb9bc2bd6d621517b374e446f2915833ea883`  
		Last Modified: Tue, 19 Dec 2023 01:43:45 GMT  
		Size: 30.1 MB (30143863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22ddf2b3cd1581c8f1483d20c8fb232852e525fea04a97ffd9ac744939dffc0`  
		Last Modified: Wed, 10 Jan 2024 23:58:29 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23537023da95e2b44ae9e7aebee71e05ecb397f02a351f30f6c69a752d98d1a5`  
		Last Modified: Wed, 10 Jan 2024 23:58:29 GMT  
		Size: 2.5 MB (2492560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8636f3d8b77edac77347698b78afe5ce4f443daa01f0a424d809c8ed35405ac5`  
		Last Modified: Wed, 10 Jan 2024 23:58:29 GMT  
		Size: 6.6 MB (6634994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41afb4f2ebc199845ca27aae99895e43658c24f7fbdea6a0b17769f1fd238b3f`  
		Last Modified: Wed, 10 Jan 2024 23:58:29 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aee346987d8e42b5a7c3ecdc4b2efa5e402c43f65712c94e3f30606c9b365e4`  
		Last Modified: Wed, 10 Jan 2024 23:58:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:71cbd1b0df460e30d13a768ed26659ea3d35001b788219b4eac0d77078e71ab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3072225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7173243e71de72bb179738a15514dee35cfb9c1f1ab3da05adc2fd1ea74335cf`

```dockerfile
```

-	Layers:
	-	`sha256:4e2e18fc597957c9c8202a8015176e35b070a14ec422ca3b88fdfaa64cd693d0`  
		Last Modified: Wed, 10 Jan 2024 23:58:29 GMT  
		Size: 3.1 MB (3051163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1dc46fbcfd7dddfe981ea410938185ededc5f8f383164b2ffe266c923d1e7ed`  
		Last Modified: Wed, 10 Jan 2024 23:58:29 GMT  
		Size: 21.1 KB (21062 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:d6b10482cd93239feb732ab9b3bcdd207e5be672b55c01b1faa72c6e10da9ee3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37564394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bed0ab2d751422f3dfcd94712006ab27d4cdd43e18f83b8b38199c2cee3b2514`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 19 Dec 2023 02:13:36 GMT
ADD file:dcd5696ac281b24df52a518e2402c7f7a4caedfcba0d82e195b7c06cd3a38fdd in / 
# Tue, 19 Dec 2023 02:13:40 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:12b1322ffb17b8e81ca1c6d9d7118e2fcee0b9d971aa3c90601e6345804a60d1`  
		Last Modified: Tue, 19 Dec 2023 02:24:36 GMT  
		Size: 29.1 MB (29121427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6b93f134841b66512a1d4138bdf28b0506ffd27490aac735508b3f20716618`  
		Last Modified: Thu, 11 Jan 2024 00:10:54 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573e69b5f2977543c86d4410256c381ef97d7f37a89be2a88bfbda683c24110e`  
		Last Modified: Thu, 11 Jan 2024 00:10:55 GMT  
		Size: 1.9 MB (1937514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb552cccf8bd4122265e6895c4c9ce039b90dd08574f0e4911a0b11aaf1f7b2c`  
		Last Modified: Thu, 11 Jan 2024 00:10:55 GMT  
		Size: 6.5 MB (6503938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b640b85282363650ba7d87fea47ce2e4cfe96da07ab6c4b47eebc739f96910`  
		Last Modified: Thu, 11 Jan 2024 00:10:54 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933eef8a1d4865a3e302557839a52d00229ef80652113710df9fd606880475c5`  
		Last Modified: Thu, 11 Jan 2024 00:10:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:c1162ead1e62fcd87632e902387935d8f33b794c009815419baf8cb396548f85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aa26ec0ff6dd44911a88c2d2af479e0c05cfb46e9db65187abe71da51f56001`

```dockerfile
```

-	Layers:
	-	`sha256:2454765cb79a60d22f96ec7e66ea9fb222b40c30758e0df9a59c7192c39847da`  
		Last Modified: Thu, 11 Jan 2024 00:10:54 GMT  
		Size: 20.8 KB (20837 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:b7976b1191a4f34442e257f55f30f8b4efd28f5f8026936846e8a5471e0c8505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.0 MB (43007490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75346431bfc757a49f790022140e267e0e6838110c75cad2bf8ab9e24e2855fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 19 Dec 2023 01:21:50 GMT
ADD file:ca1db68689e0b0388337ba450ad2c8e79c159c6b78f5aa6d3ff2b89b8d7edc93 in / 
# Tue, 19 Dec 2023 01:21:51 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fc9b8f5eec3aa37ab3aace05165427479352f290d53904cea87dca6349633a09`  
		Last Modified: Tue, 19 Dec 2023 01:26:19 GMT  
		Size: 33.1 MB (33120558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f85ae146a90d1ce7561d4e67d1ce2eaf0a0da444bb8a70c5b7fc94d0dc75e389`  
		Last Modified: Wed, 20 Dec 2023 08:43:43 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23065e9a12cf130c31375986a9b4700b84f2539ccb4b47efe0f375f77938fc3`  
		Last Modified: Wed, 20 Dec 2023 08:43:44 GMT  
		Size: 2.7 MB (2698240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b8249b30995d06e02d41e31406a930c02163d057cd39ad2cb7f710df2f6c60`  
		Last Modified: Thu, 11 Jan 2024 00:10:31 GMT  
		Size: 7.2 MB (7187176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a238b8549095cec1619f8f38f82d1aeb50acdf094b2b611b1fb5c62da14635f`  
		Last Modified: Thu, 11 Jan 2024 00:10:31 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669f29d97099310deca355ff837c9885adea00bb9c6e460490904627b7a40e4b`  
		Last Modified: Thu, 11 Jan 2024 00:10:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:87bde9e8cd8d07c6306a9ef516b822eadb9669d79da8587f1ac892066646ad33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3066464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:034c7634fd9e3419a42aa94fb6c3c05bd8d951eaf75eef2fbd2e8d64150013ba`

```dockerfile
```

-	Layers:
	-	`sha256:0a90f178efc50a3500b5ee2dce72b560153f2b0ec4cc6e79aa940561e8d58590`  
		Last Modified: Thu, 11 Jan 2024 00:10:31 GMT  
		Size: 3.0 MB (3045446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35a907ae4a36d514f4ff1b8d97766c9a5166c6116bc026f627e4de4cc51111fe`  
		Last Modified: Thu, 11 Jan 2024 00:10:30 GMT  
		Size: 21.0 KB (21018 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:9110d0aec3fc0be39a13bfd7030a3d04f36e230034078de3b407ae883f3e3de2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35722087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aef7bb08b32c1c17f11984770392abcc11b268465af0e89884793edf6ec092dd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 04 Dec 2023 18:08:47 GMT
ADD file:f06f12fa5a93afc3a79ac4371d24b0a471a5a1818cf34c1d90004c8f410914b9 in / 
# Mon, 04 Dec 2023 18:08:47 GMT
CMD ["bash"]
# Mon, 04 Dec 2023 18:08:47 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 04 Dec 2023 18:08:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 04 Dec 2023 18:08:47 GMT
ENV MEMCACHED_VERSION=1.6.22
# Mon, 04 Dec 2023 18:08:47 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.22.tar.gz
# Mon, 04 Dec 2023 18:08:47 GMT
ENV MEMCACHED_SHA1=7a691f390d59616dbebfc9e2e4942d499c39a338
# Mon, 04 Dec 2023 18:08:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 04 Dec 2023 18:08:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 Dec 2023 18:08:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 04 Dec 2023 18:08:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 Dec 2023 18:08:47 GMT
USER memcache
# Mon, 04 Dec 2023 18:08:47 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 04 Dec 2023 18:08:47 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bc6b1888979d3ceb063da848b2034e980e2c2613642159c1e856550b79aa620c`  
		Last Modified: Tue, 19 Dec 2023 01:47:38 GMT  
		Size: 27.5 MB (27491874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b453a12051612cbbdca8ee1a3c9e8211ac636f53786a525b824574fff746cda`  
		Last Modified: Tue, 19 Dec 2023 15:38:14 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7903f8445b1bbbe476fd67c998f57a5289b3d4a9e65a1190e551b7c79083e65d`  
		Last Modified: Tue, 19 Dec 2023 15:38:15 GMT  
		Size: 2.2 MB (2152511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf54a1600c7ab496cf3e01f5ec34a3ae7dfbf25014ef90ec9c7b005aa3d887c`  
		Last Modified: Tue, 19 Dec 2023 15:38:14 GMT  
		Size: 6.1 MB (6076186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b446e4dc631c597d82b5e437bf342d8607d8a4ff3229d052f049bfbac270e2c6`  
		Last Modified: Tue, 19 Dec 2023 15:38:14 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee453ca29f8bbd4b452693cd9f2e2e1b7cff2fa139d7fc942de190d244ae6617`  
		Last Modified: Tue, 19 Dec 2023 15:38:15 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:2fa3455fc28f5964cc39eaaadcfab8df0a8dd5552a08464b0f87cbc775addb70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3067351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddb3e50e2a70d6400f4ba5be3b4010e9a0f7770e69e2c1e1c599bf6224ed8ac8`

```dockerfile
```

-	Layers:
	-	`sha256:2dcfb5805d88251b9b79a3c0e144091f0dc62a366eddacb9d50aa89a825067ef`  
		Last Modified: Tue, 19 Dec 2023 15:38:14 GMT  
		Size: 3.0 MB (3046401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb52cc58a7fa498aa7b56431dbe3e004db5d4b028b724bc1f087b44c1baaa25c`  
		Last Modified: Tue, 19 Dec 2023 15:38:14 GMT  
		Size: 20.9 KB (20950 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6`

```console
$ docker pull memcached@sha256:fa6c8e150e7b7af5e6f05ad388bbf5f4f34925e17aef12fc494ffdef7b3911cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 15
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
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
$ docker pull memcached@sha256:643a24a57407d3cb2b8745f47a8d4b20406c19f5399ecb05db9727447637003a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38789237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d474793fb4125ae857b42efbf79eb1cbea8834a20e5d65627ea439b52b57313`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:27 GMT
ADD file:ac3cd70031d35e46d86b876934946ffc8756de4de065fbc926dce642dac07ff3 in / 
# Tue, 19 Dec 2023 01:20:28 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:af107e978371b6cd6339127a05502c5eacd1e6b0e9eb7b2f4aa7b6fc87e2dd81`  
		Last Modified: Tue, 19 Dec 2023 01:24:59 GMT  
		Size: 29.1 MB (29125963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d32ccca352404a5a8dedb6a7ca281abbc073b9d8643ef4626873ee1b8a204b1`  
		Last Modified: Wed, 10 Jan 2024 23:58:24 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d585b71055b9f919875cf91a81370309c971aad943e53b8c9fda2b63521f873`  
		Last Modified: Wed, 10 Jan 2024 23:58:25 GMT  
		Size: 2.5 MB (2488298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc47ad75df3e3af04459ae59b5c7ec1ea8dd657b7fb4cc42ec85a982a98da628`  
		Last Modified: Wed, 10 Jan 2024 23:58:25 GMT  
		Size: 7.2 MB (7173458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66204efbd683596758bec893cba01fce3fe386da63399af101051d8df26c2477`  
		Last Modified: Wed, 10 Jan 2024 23:58:25 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3406bc9285b7e906c211fd9a5d9342ee80d9e0ae728a6529d14db42aecf145`  
		Last Modified: Wed, 10 Jan 2024 23:58:25 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:8efa487487fc160476637a4fb2aec45b4a38eb677aeddcd0ecaeab362e136e85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3077977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:928c59acdba2c812e1299dcb8c4a4c7a7bdfadbc695533aab940957913a8b768`

```dockerfile
```

-	Layers:
	-	`sha256:7777c14054a0e9893c312cf26a23d80bb2f16d3cd6dacad21c21c8fb1be321a4`  
		Last Modified: Wed, 10 Jan 2024 23:58:25 GMT  
		Size: 3.1 MB (3056860 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc8d2dbb4d2d164636bb06f04252d4aec50002cf7469a8955e322e104563d025`  
		Last Modified: Wed, 10 Jan 2024 23:58:24 GMT  
		Size: 21.1 KB (21117 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm variant v5

```console
$ docker pull memcached@sha256:d01aca5f5e26f687d6ad14ec6547e704f453acc02ce0ce2e5fa5871f5013bfbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34811390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f12a90da675230d99a32d19f573412751d7740cae5f90d74a8c49b4b6f64a3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 19 Dec 2023 01:55:22 GMT
ADD file:9503ab966c9dd707eeccc7c2f633bccc94c199f8714ec4ff2c8b54dde3dbabf9 in / 
# Tue, 19 Dec 2023 01:55:22 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1ae9a2844c8c70942d2220553689b62e841cc706d77284fbfedbd770080fd699`  
		Last Modified: Tue, 19 Dec 2023 01:58:33 GMT  
		Size: 26.9 MB (26885440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ab650f4c7d61856342d3b0e4d9bad9cd0c4336fb403dab9c5c1ed2c285774f`  
		Last Modified: Thu, 11 Jan 2024 00:07:53 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b10807a0745d6e1ccc36157b11a3469a17c6477eda65233bb2f182c7958db5b8`  
		Last Modified: Thu, 11 Jan 2024 00:07:54 GMT  
		Size: 2.1 MB (2089356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5bc9bbfb0a70ce84a09ce58d70ebf97841c03e06d3968f065cd9361bd0e990`  
		Last Modified: Thu, 11 Jan 2024 00:07:54 GMT  
		Size: 5.8 MB (5835079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74b3373a0a7639196238720db6061026ccfe87c48ccf38fcfbc737699c9f2b7`  
		Last Modified: Thu, 11 Jan 2024 00:07:53 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3969d1f7528c0ba1d0047402bf5611d53c8f502f52fbbd7fb827f8de5ab813f6`  
		Last Modified: Thu, 11 Jan 2024 00:07:54 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:7484a951008b8e170922f1467a179c839a675cf4ab9555315f6bb20174be8173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3052683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d85ee8bbb3867fa9cbdd5e06e5791b62e1c7dfc410295ba05b95ead8b6c4525`

```dockerfile
```

-	Layers:
	-	`sha256:34e791a9d4149137cb6b8da59558d4bf4ce80c9bcd5ab599785c7a3aaa2fc844`  
		Last Modified: Thu, 11 Jan 2024 00:07:54 GMT  
		Size: 3.0 MB (3031592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31263ce608cc2e18001c08b34ad8f21b27befcf21ee30dd42bd87176f24a5e10`  
		Last Modified: Thu, 11 Jan 2024 00:07:53 GMT  
		Size: 21.1 KB (21091 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; arm variant v7

```console
$ docker pull memcached@sha256:2841be0a36134563966c09a6ed68b21053d20342ec8736cf92763c28077ead43
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28094215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cf74ffa940dd93988fc0beb6698c5796563c82a40b7dd668153969f64d2e6ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 09 Feb 2023 06:12:09 GMT
ADD file:5f1a343224e8486690bd90dd1e50c8d84b3d770c51bb6829544e5cf650c0419c in / 
# Thu, 09 Feb 2023 06:12:10 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 07:52:31 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Thu, 09 Feb 2023 07:52:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 07:52:35 GMT
ENV MEMCACHED_VERSION=1.6.18
# Thu, 09 Feb 2023 07:52:35 GMT
ENV MEMCACHED_SHA1=be16909bb75ab972ee5fe438312501de01c4725a
# Thu, 09 Feb 2023 07:55:44 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Thu, 09 Feb 2023 07:55:44 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 09 Feb 2023 07:55:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 09 Feb 2023 07:55:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Feb 2023 07:55:44 GMT
USER memcache
# Thu, 09 Feb 2023 07:55:45 GMT
EXPOSE 11211
# Thu, 09 Feb 2023 07:55:45 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:e7318f6106ad75d7d482ae9dddf4d927b0872ef3ddb6e1330aa691fc8d17279e`  
		Last Modified: Thu, 09 Feb 2023 06:19:19 GMT  
		Size: 26.6 MB (26577666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de49d9d72daf1680b5f1b9532dd2eb0162829f36c8db9669935462636fbf99d9`  
		Last Modified: Thu, 09 Feb 2023 08:06:11 GMT  
		Size: 4.9 KB (4895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0beac9d5bcac946f8c54c72b8a9c136914b1aa7a5fe2b8c3df4c7d8858ea6559`  
		Last Modified: Thu, 09 Feb 2023 08:06:11 GMT  
		Size: 312.1 KB (312088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4c9e5a265394e4c0f357779e6195a4e82d767a3691a0e77d427e56651c3e54a`  
		Last Modified: Thu, 09 Feb 2023 08:06:11 GMT  
		Size: 1.2 MB (1199163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ea82ad892fe1ae8623d84e32c8c027087cda8aa49e40d4546ed6942e471c60`  
		Last Modified: Thu, 09 Feb 2023 08:06:11 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2ae3bcdc0d114ba49a67df022b6f7215fc87f1f50e64939fcfbbec4eaadee5`  
		Last Modified: Thu, 09 Feb 2023 08:06:11 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:1b119620b1cbaac4281975bedfed15ff721d868ec9eda9574dc4c1ec58330716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37686962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45b76a80b62f56ff1c68ed4e7ce2dfe225b3560e00750a3210c8d897b1547f3a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:11 GMT
ADD file:262fd7bf0bc26e5d2a229fba52626e22b8a93beac29733acfc60e716c26e689d in / 
# Tue, 19 Dec 2023 01:41:11 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:24e221e92a36ab5b0075dd156b4f2ff095532a9b0927946cf6070bb1bea208b8`  
		Last Modified: Tue, 19 Dec 2023 01:44:38 GMT  
		Size: 29.2 MB (29157269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d79fe3da079136cc418087e5d4e432357c062519668a3c03b78c24710c3a6ec`  
		Last Modified: Wed, 20 Dec 2023 10:20:11 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:496388416e6f8cdbf05e6ea4a56e906308e4b95b9f984f73b5c5a3fdbe5b12aa`  
		Last Modified: Wed, 20 Dec 2023 10:20:11 GMT  
		Size: 2.3 MB (2346023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee91bf234e7544eb6ad4c5f18ba87a8c0306d87f51ee1c47b1361569175a8a7c`  
		Last Modified: Thu, 11 Jan 2024 00:20:26 GMT  
		Size: 6.2 MB (6182151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73888be7ca392dfe14270a838c67a2d7ccfe9354f1fe52147291c9756127b51`  
		Last Modified: Thu, 11 Jan 2024 00:20:25 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a917a1ebe539f36501d4bebb89957491c647a119a1702734b1a0c9c01dc2a6`  
		Last Modified: Thu, 11 Jan 2024 00:20:25 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:f96d1dde1233068de191226772289ac63a784a466d34ec1dbf67e72559643f7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3053019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f249bf848fae6f5b573dffd3d8dbd830fd3267c6f487d397fd82ba104fee46b`

```dockerfile
```

-	Layers:
	-	`sha256:09c490b7c5d08149f654887eca9ca058a49a3b659d3e7282589a431883445a49`  
		Last Modified: Thu, 11 Jan 2024 00:20:25 GMT  
		Size: 3.0 MB (3032051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abe3c6e55476a176987bc5b5f8bad00ca16d1299d36e40f52e82dcb76ed0600c`  
		Last Modified: Thu, 11 Jan 2024 00:20:25 GMT  
		Size: 21.0 KB (20968 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; 386

```console
$ docker pull memcached@sha256:a5d93bfce917e364c0f16cdad7b683a36011a997db4be6db2770644095aea01d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39272936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:902b98d31b0a747e1d90226bbd3f7fb16592c8f606009585e9b2bbb819bfb30e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 19 Dec 2023 01:39:07 GMT
ADD file:6f4083d57ea9644b5a827e67b0725087a15aa428272ec223ab968bf8b4623e42 in / 
# Tue, 19 Dec 2023 01:39:07 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8d4aad22fb6a12b8cc7a78d338dfb9bc2bd6d621517b374e446f2915833ea883`  
		Last Modified: Tue, 19 Dec 2023 01:43:45 GMT  
		Size: 30.1 MB (30143863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22ddf2b3cd1581c8f1483d20c8fb232852e525fea04a97ffd9ac744939dffc0`  
		Last Modified: Wed, 10 Jan 2024 23:58:29 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23537023da95e2b44ae9e7aebee71e05ecb397f02a351f30f6c69a752d98d1a5`  
		Last Modified: Wed, 10 Jan 2024 23:58:29 GMT  
		Size: 2.5 MB (2492560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8636f3d8b77edac77347698b78afe5ce4f443daa01f0a424d809c8ed35405ac5`  
		Last Modified: Wed, 10 Jan 2024 23:58:29 GMT  
		Size: 6.6 MB (6634994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41afb4f2ebc199845ca27aae99895e43658c24f7fbdea6a0b17769f1fd238b3f`  
		Last Modified: Wed, 10 Jan 2024 23:58:29 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aee346987d8e42b5a7c3ecdc4b2efa5e402c43f65712c94e3f30606c9b365e4`  
		Last Modified: Wed, 10 Jan 2024 23:58:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:71cbd1b0df460e30d13a768ed26659ea3d35001b788219b4eac0d77078e71ab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3072225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7173243e71de72bb179738a15514dee35cfb9c1f1ab3da05adc2fd1ea74335cf`

```dockerfile
```

-	Layers:
	-	`sha256:4e2e18fc597957c9c8202a8015176e35b070a14ec422ca3b88fdfaa64cd693d0`  
		Last Modified: Wed, 10 Jan 2024 23:58:29 GMT  
		Size: 3.1 MB (3051163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1dc46fbcfd7dddfe981ea410938185ededc5f8f383164b2ffe266c923d1e7ed`  
		Last Modified: Wed, 10 Jan 2024 23:58:29 GMT  
		Size: 21.1 KB (21062 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; mips64le

```console
$ docker pull memcached@sha256:d6b10482cd93239feb732ab9b3bcdd207e5be672b55c01b1faa72c6e10da9ee3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37564394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bed0ab2d751422f3dfcd94712006ab27d4cdd43e18f83b8b38199c2cee3b2514`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 19 Dec 2023 02:13:36 GMT
ADD file:dcd5696ac281b24df52a518e2402c7f7a4caedfcba0d82e195b7c06cd3a38fdd in / 
# Tue, 19 Dec 2023 02:13:40 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:12b1322ffb17b8e81ca1c6d9d7118e2fcee0b9d971aa3c90601e6345804a60d1`  
		Last Modified: Tue, 19 Dec 2023 02:24:36 GMT  
		Size: 29.1 MB (29121427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6b93f134841b66512a1d4138bdf28b0506ffd27490aac735508b3f20716618`  
		Last Modified: Thu, 11 Jan 2024 00:10:54 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573e69b5f2977543c86d4410256c381ef97d7f37a89be2a88bfbda683c24110e`  
		Last Modified: Thu, 11 Jan 2024 00:10:55 GMT  
		Size: 1.9 MB (1937514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb552cccf8bd4122265e6895c4c9ce039b90dd08574f0e4911a0b11aaf1f7b2c`  
		Last Modified: Thu, 11 Jan 2024 00:10:55 GMT  
		Size: 6.5 MB (6503938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b640b85282363650ba7d87fea47ce2e4cfe96da07ab6c4b47eebc739f96910`  
		Last Modified: Thu, 11 Jan 2024 00:10:54 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933eef8a1d4865a3e302557839a52d00229ef80652113710df9fd606880475c5`  
		Last Modified: Thu, 11 Jan 2024 00:10:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:c1162ead1e62fcd87632e902387935d8f33b794c009815419baf8cb396548f85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aa26ec0ff6dd44911a88c2d2af479e0c05cfb46e9db65187abe71da51f56001`

```dockerfile
```

-	Layers:
	-	`sha256:2454765cb79a60d22f96ec7e66ea9fb222b40c30758e0df9a59c7192c39847da`  
		Last Modified: Thu, 11 Jan 2024 00:10:54 GMT  
		Size: 20.8 KB (20837 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; ppc64le

```console
$ docker pull memcached@sha256:b7976b1191a4f34442e257f55f30f8b4efd28f5f8026936846e8a5471e0c8505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.0 MB (43007490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75346431bfc757a49f790022140e267e0e6838110c75cad2bf8ab9e24e2855fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 19 Dec 2023 01:21:50 GMT
ADD file:ca1db68689e0b0388337ba450ad2c8e79c159c6b78f5aa6d3ff2b89b8d7edc93 in / 
# Tue, 19 Dec 2023 01:21:51 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fc9b8f5eec3aa37ab3aace05165427479352f290d53904cea87dca6349633a09`  
		Last Modified: Tue, 19 Dec 2023 01:26:19 GMT  
		Size: 33.1 MB (33120558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f85ae146a90d1ce7561d4e67d1ce2eaf0a0da444bb8a70c5b7fc94d0dc75e389`  
		Last Modified: Wed, 20 Dec 2023 08:43:43 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23065e9a12cf130c31375986a9b4700b84f2539ccb4b47efe0f375f77938fc3`  
		Last Modified: Wed, 20 Dec 2023 08:43:44 GMT  
		Size: 2.7 MB (2698240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b8249b30995d06e02d41e31406a930c02163d057cd39ad2cb7f710df2f6c60`  
		Last Modified: Thu, 11 Jan 2024 00:10:31 GMT  
		Size: 7.2 MB (7187176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a238b8549095cec1619f8f38f82d1aeb50acdf094b2b611b1fb5c62da14635f`  
		Last Modified: Thu, 11 Jan 2024 00:10:31 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669f29d97099310deca355ff837c9885adea00bb9c6e460490904627b7a40e4b`  
		Last Modified: Thu, 11 Jan 2024 00:10:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:87bde9e8cd8d07c6306a9ef516b822eadb9669d79da8587f1ac892066646ad33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3066464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:034c7634fd9e3419a42aa94fb6c3c05bd8d951eaf75eef2fbd2e8d64150013ba`

```dockerfile
```

-	Layers:
	-	`sha256:0a90f178efc50a3500b5ee2dce72b560153f2b0ec4cc6e79aa940561e8d58590`  
		Last Modified: Thu, 11 Jan 2024 00:10:31 GMT  
		Size: 3.0 MB (3045446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35a907ae4a36d514f4ff1b8d97766c9a5166c6116bc026f627e4de4cc51111fe`  
		Last Modified: Thu, 11 Jan 2024 00:10:30 GMT  
		Size: 21.0 KB (21018 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6` - linux; s390x

```console
$ docker pull memcached@sha256:9110d0aec3fc0be39a13bfd7030a3d04f36e230034078de3b407ae883f3e3de2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35722087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aef7bb08b32c1c17f11984770392abcc11b268465af0e89884793edf6ec092dd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 04 Dec 2023 18:08:47 GMT
ADD file:f06f12fa5a93afc3a79ac4371d24b0a471a5a1818cf34c1d90004c8f410914b9 in / 
# Mon, 04 Dec 2023 18:08:47 GMT
CMD ["bash"]
# Mon, 04 Dec 2023 18:08:47 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 04 Dec 2023 18:08:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 04 Dec 2023 18:08:47 GMT
ENV MEMCACHED_VERSION=1.6.22
# Mon, 04 Dec 2023 18:08:47 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.22.tar.gz
# Mon, 04 Dec 2023 18:08:47 GMT
ENV MEMCACHED_SHA1=7a691f390d59616dbebfc9e2e4942d499c39a338
# Mon, 04 Dec 2023 18:08:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 04 Dec 2023 18:08:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 Dec 2023 18:08:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 04 Dec 2023 18:08:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 Dec 2023 18:08:47 GMT
USER memcache
# Mon, 04 Dec 2023 18:08:47 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 04 Dec 2023 18:08:47 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bc6b1888979d3ceb063da848b2034e980e2c2613642159c1e856550b79aa620c`  
		Last Modified: Tue, 19 Dec 2023 01:47:38 GMT  
		Size: 27.5 MB (27491874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b453a12051612cbbdca8ee1a3c9e8211ac636f53786a525b824574fff746cda`  
		Last Modified: Tue, 19 Dec 2023 15:38:14 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7903f8445b1bbbe476fd67c998f57a5289b3d4a9e65a1190e551b7c79083e65d`  
		Last Modified: Tue, 19 Dec 2023 15:38:15 GMT  
		Size: 2.2 MB (2152511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf54a1600c7ab496cf3e01f5ec34a3ae7dfbf25014ef90ec9c7b005aa3d887c`  
		Last Modified: Tue, 19 Dec 2023 15:38:14 GMT  
		Size: 6.1 MB (6076186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b446e4dc631c597d82b5e437bf342d8607d8a4ff3229d052f049bfbac270e2c6`  
		Last Modified: Tue, 19 Dec 2023 15:38:14 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee453ca29f8bbd4b452693cd9f2e2e1b7cff2fa139d7fc942de190d244ae6617`  
		Last Modified: Tue, 19 Dec 2023 15:38:15 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6` - unknown; unknown

```console
$ docker pull memcached@sha256:2fa3455fc28f5964cc39eaaadcfab8df0a8dd5552a08464b0f87cbc775addb70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3067351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddb3e50e2a70d6400f4ba5be3b4010e9a0f7770e69e2c1e1c599bf6224ed8ac8`

```dockerfile
```

-	Layers:
	-	`sha256:2dcfb5805d88251b9b79a3c0e144091f0dc62a366eddacb9d50aa89a825067ef`  
		Last Modified: Tue, 19 Dec 2023 15:38:14 GMT  
		Size: 3.0 MB (3046401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb52cc58a7fa498aa7b56431dbe3e004db5d4b028b724bc1f087b44c1baaa25c`  
		Last Modified: Tue, 19 Dec 2023 15:38:14 GMT  
		Size: 20.9 KB (20950 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine`

```console
$ docker pull memcached@sha256:df6a80f20b17df1f452b325ba2bee57644473669cb08fc928d55417da18cb786
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 11
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
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
$ docker pull memcached@sha256:32affe08f4a1c6f62faacae1fee90575987d8b995a7257aa35ca1b4a817bdbf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6528299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fba850e40285109fcdc4c5603f2e081dba5bb683ffbcf0d4ad2e954359ce93e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 08 Dec 2023 01:20:49 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Fri, 08 Dec 2023 01:20:49 GMT
CMD ["/bin/sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd74bdcd28e46833593b2724720938c58842faa843fe42ea2411b3afd0739cb6`  
		Last Modified: Wed, 10 Jan 2024 23:58:18 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104a06a5eef3fffb9db79f8f67d4205725b9551aadbad7cb2847b013921bc212`  
		Last Modified: Wed, 10 Jan 2024 23:58:18 GMT  
		Size: 104.2 KB (104204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3271524d49893bc0950a7d058e91621dcfabe2383d6bfc0b13263faaf85f774f`  
		Last Modified: Wed, 10 Jan 2024 23:58:18 GMT  
		Size: 3.0 MB (3013977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb917829c49dd9d022cf427a72685718c30e113cfe036cffdf3eec29523e871`  
		Last Modified: Wed, 10 Jan 2024 23:58:18 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c390a9d8c6874260017223d74f3ae0b04895aa29a26c6ea03e0bd49832fe201`  
		Last Modified: Wed, 10 Jan 2024 23:58:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:a4db06e4e22e5cb6667aafc4b272349d5db9596147a2114d7b6997ae75e265f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 KB (98074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80b0a8c4800de05bc28d0cf54908bd75ed706e519dc72a22883d057213a1afdd`

```dockerfile
```

-	Layers:
	-	`sha256:9052d3e673c4418bce0a5b5c01961846c1fc2b14ace86d3afae91720a4744b70`  
		Last Modified: Wed, 10 Jan 2024 23:58:18 GMT  
		Size: 78.6 KB (78603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:667e7c7f728f9119016e4a456207d31154a85c080f74151700cc04835b950d54`  
		Last Modified: Wed, 10 Jan 2024 23:58:18 GMT  
		Size: 19.5 KB (19471 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:79a5646a0c845a791f36017fda3292281b48295b06c53f13d62c9f94237d4731
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3960292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2afac0e49af3ce3f1769abe11a29f8f5610c6a736d8c5b6c7b9770c8d8e94e91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 16 Dec 2020 23:58:14 GMT
ADD file:bd07f77a2b2741ca6bda80d9203be9c7274cf73145bff778cf000db0d8d4e903 in / 
# Wed, 16 Dec 2020 23:58:15 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 06:43:29 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Thu, 17 Dec 2020 06:43:31 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Thu, 17 Dec 2020 06:43:33 GMT
ENV MEMCACHED_VERSION=1.6.9
# Thu, 17 Dec 2020 06:43:35 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Thu, 17 Dec 2020 06:46:32 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Thu, 17 Dec 2020 06:46:33 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 17 Dec 2020 06:46:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 17 Dec 2020 06:46:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 06:46:36 GMT
USER memcache
# Thu, 17 Dec 2020 06:46:38 GMT
EXPOSE 11211
# Thu, 17 Dec 2020 06:46:39 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c58e8a26a8407acc3ead776f6526efa889fda03270a8d05109208d9f59159420`  
		Last Modified: Wed, 16 Dec 2020 23:58:59 GMT  
		Size: 2.4 MB (2407555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68564bbfc09f153688e942bf54d5375d1e27f3507c0bed6b038c2ac8ce095aa5`  
		Last Modified: Thu, 17 Dec 2020 06:46:58 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cac3a91edee49d0b08a25706ae86059bed89941a08b496e72ef092e57c4ecb3`  
		Last Modified: Thu, 17 Dec 2020 06:46:58 GMT  
		Size: 13.8 KB (13825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf16e9bb942ec42a35a792beab65aea843209e7bdde7e856499b9fc85f93bc4e`  
		Last Modified: Thu, 17 Dec 2020 06:46:58 GMT  
		Size: 1.5 MB (1537248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc15394239bd0c083e1b6df806aa5ffeb8b9cc7e80113afc2959721de49f90d1`  
		Last Modified: Thu, 17 Dec 2020 06:46:58 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:482f0eb571548eae5720c652ff7da13558e56a8722dc9932cf7eb1ef3eb33acb`  
		Last Modified: Thu, 17 Dec 2020 06:46:58 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:5550c34a395e8c02098f113a01d35d794b40c31c374f1e553dc80472d53978c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6372430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f4edcab8bc23e09f91d9a22a6d9df2a2d0175c23ad7cd396eaa4e849528f0e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 08 Dec 2023 01:39:30 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 08 Dec 2023 01:39:30 GMT
CMD ["/bin/sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c303524923177661067f7eb378c3dd5277088c2676ebd1cd78e68397bb80fdbf`  
		Last Modified: Fri, 08 Dec 2023 01:39:48 GMT  
		Size: 3.3 MB (3347794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfede01b081f27465377bdafbbdb6b694c6fab18026972b2c380535dcef103b8`  
		Last Modified: Wed, 13 Dec 2023 01:35:47 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d7b6f4ad45bf3aee58c5a7e8083286bd79dc004840903fd5997929772bfb4c`  
		Last Modified: Wed, 13 Dec 2023 01:35:47 GMT  
		Size: 120.9 KB (120897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f6c7840c606bfa580e1e6b52087faff29fb3986005ea3aadc31c64b3e4142e`  
		Last Modified: Thu, 11 Jan 2024 00:22:58 GMT  
		Size: 2.9 MB (2902089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1335fd4bd25daf4820a1c881f1ea0a30a575682074ad886293a372089bcd4544`  
		Last Modified: Thu, 11 Jan 2024 00:22:58 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48e51e3a0b635d352137fa3c7c3747c8192e7c8de0590e533ffdcea9dc49a96`  
		Last Modified: Thu, 11 Jan 2024 00:22:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:6faa51abf4ec7649d68a12af15126861e91479130b3f97128d3fa7a487d62422
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.9 KB (97945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e975d798c27c70d9498c44491a9aca9d24cee1fe8111bfae46401e7d9b1264`

```dockerfile
```

-	Layers:
	-	`sha256:0c5c585bb2d781fc112b82e19d343028a3c75758809ef4b46e4a6839bd0a1e41`  
		Last Modified: Thu, 11 Jan 2024 00:22:58 GMT  
		Size: 78.6 KB (78622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed5eb3630ee14af5005edfb5ed56d4660a5bbf224bf729ca0bfabaa0143d9864`  
		Last Modified: Thu, 11 Jan 2024 00:22:58 GMT  
		Size: 19.3 KB (19323 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; 386

```console
$ docker pull memcached@sha256:67373b38ed96c7ba59d5c1b8ba2b471d75d058ae7056f1e22674128af0e39ece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6185193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ec7484601b2ef9f91318f7c210dbd58716132fdd37be8004e82af4e4d42015b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 08 Dec 2023 01:38:25 GMT
ADD file:bd52540f209ba362654d795d7893669c819d35011a16f9f319301727a33b3bd9 in / 
# Fri, 08 Dec 2023 01:38:25 GMT
CMD ["/bin/sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9acd8b4c9d4385585f74dabb4bc6b3351888710ae37ec5dbd9ea950281b8f9bb`  
		Last Modified: Fri, 08 Dec 2023 01:38:43 GMT  
		Size: 3.2 MB (3244115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7759a4b7aa772576870eb5c52f815fbebd9be11b4781c708dc2ab6007fa609`  
		Last Modified: Wed, 10 Jan 2024 23:58:26 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5ca5419371cb9331b9ba1ea9086eef15ad135bf369ac2787491caf04de682f`  
		Last Modified: Wed, 10 Jan 2024 23:58:26 GMT  
		Size: 109.3 KB (109334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc68a66ccf11c1510081e6e9f70c399ad3ceff564e9b876ed2895ebf29b3ebb`  
		Last Modified: Wed, 10 Jan 2024 23:58:26 GMT  
		Size: 2.8 MB (2830103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b15634bddb0499598a6044cc0030e88ba0ce4cf2b02301cfa0a0faa1ac676cdd`  
		Last Modified: Wed, 10 Jan 2024 23:58:26 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dddc1630ef7eb2545abf068534d7032d19114a744cd485791f63f40ab0b5ab18`  
		Last Modified: Wed, 10 Jan 2024 23:58:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:15c53491df84b3d051fdcc7dff9dbdb9ca3718254ea873b6e2bbff7bc221abec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.0 KB (97973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fee76928da54f07fd68a5975f71e6f5991ccd3261cf759f3093b424e8f7ba99`

```dockerfile
```

-	Layers:
	-	`sha256:1ae5a47e6fefaee5dc9532fb45757803475b71d80ddf777a416ccd10c45bd09e`  
		Last Modified: Wed, 10 Jan 2024 23:58:26 GMT  
		Size: 78.6 KB (78558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ae992c52298a54654430860ae3828320c41eec63e8702ef1c66f1a68fdb937e`  
		Last Modified: Wed, 10 Jan 2024 23:58:26 GMT  
		Size: 19.4 KB (19415 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:0639819cf6cbfd6e608ef2071abeb9ca10f049a89ecc83eee11f1d75b78cab2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6394995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12d25d4724561e2ace36bab912780d035fdb57c760fa9268b40e781584c2df0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 08 Dec 2023 01:22:51 GMT
ADD file:052421189f8d269382daaaa8beb63c687e4d8ca908c421abdce53bcc627a40b4 in / 
# Fri, 08 Dec 2023 01:22:51 GMT
CMD ["/bin/sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:243ac51c334a47917a84be93e972ee6378987e9b3b917a5a8df29025e161c1f3`  
		Last Modified: Fri, 08 Dec 2023 01:23:14 GMT  
		Size: 3.4 MB (3358233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add73e7dbebd6c86078686bb046ef57017b090fe917f656feb83ec0ef971b5f3`  
		Last Modified: Tue, 12 Dec 2023 23:20:17 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d64bed657a7e728633e13f2021b35954e98be9ecae77096d30cdaa1d9260d61e`  
		Last Modified: Tue, 12 Dec 2023 23:20:17 GMT  
		Size: 123.4 KB (123403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a69dac8774b0ef6bdf9b84b7360fb3346a88b05e510dbc3366a3a828349a839b`  
		Last Modified: Thu, 11 Jan 2024 00:13:43 GMT  
		Size: 2.9 MB (2911714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666eeed87216ed83fdc1a618d27175e1a8c8efd15354f7e22228e768ded7a7cf`  
		Last Modified: Thu, 11 Jan 2024 00:13:42 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfeab30e174bcb0fc8203612135497885d25cfc588a1e44de9e5b0b5048dcdb`  
		Last Modified: Thu, 11 Jan 2024 00:13:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:d20e9002675244162fdaf77d022444958c1a6d56dfe5901853240c568aea24b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 KB (96397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e870214daaeaabaf116e4a0a6462f63bc3d9ce9cd3d522277e53ba1d9c19a54e`

```dockerfile
```

-	Layers:
	-	`sha256:54016ce6ca1c0550269f0db7f3fec4511d81bef96b3c0f41709d785c7cefa5d3`  
		Last Modified: Thu, 11 Jan 2024 00:13:42 GMT  
		Size: 77.0 KB (77025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28bbe767bea18a4ae8896d545c4083a8a7a41145031227bdf28474500598aa2f`  
		Last Modified: Thu, 11 Jan 2024 00:13:42 GMT  
		Size: 19.4 KB (19372 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:53d0bdb491815057b9014ab30e95c68146d83accdc9d8d690e308e67e7f4eed5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4326665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b078f3aede6257187e9488318eac328332ace90ac171c8a99d0ca495e1e9ad40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 08 Dec 2023 01:41:50 GMT
ADD file:47e0982fc3ae485c06d46f3c0022afd39ed7ec95fe755c2391e6b0cfcae65dfc in / 
# Fri, 08 Dec 2023 01:41:51 GMT
CMD ["/bin/sh"]
# Sat, 09 Dec 2023 01:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 09 Dec 2023 01:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 09 Dec 2023 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.22
# Sat, 09 Dec 2023 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.22.tar.gz
# Sat, 09 Dec 2023 01:54:10 GMT
ENV MEMCACHED_SHA1=7a691f390d59616dbebfc9e2e4942d499c39a338
# Sat, 09 Dec 2023 01:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 09 Dec 2023 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 09 Dec 2023 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 09 Dec 2023 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 09 Dec 2023 01:54:10 GMT
USER memcache
# Sat, 09 Dec 2023 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 09 Dec 2023 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0fca3ee44ced87b7184bc23390283fdf10cfae0e844a25b785dd11c463815227`  
		Last Modified: Fri, 08 Dec 2023 01:42:30 GMT  
		Size: 3.2 MB (3242332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff601679be7ba19260a77b326cf587dcc37315b02c2e0b0effc7084da4684bd7`  
		Last Modified: Wed, 13 Dec 2023 00:39:43 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b2401b35befb0832d96cebfdee6215736b27c0e3d064d67da9917deca4c14c`  
		Last Modified: Wed, 13 Dec 2023 00:39:43 GMT  
		Size: 113.1 KB (113142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59b1e1447b7739e5338731014a96bea369258cbf54b2d152ef50bb06e308bad`  
		Last Modified: Wed, 13 Dec 2023 00:39:43 GMT  
		Size: 969.5 KB (969547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c62bb151b09d73f2bc083bb91abedfb6660c5045d34f7d576415190ae4e09f`  
		Last Modified: Wed, 13 Dec 2023 00:39:43 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaaf7e6dbf7fbf661d0b3f6f5d38fbd888ab6707a76919a5f4a633194e895a2f`  
		Last Modified: Wed, 13 Dec 2023 00:39:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:1c2ba4c72ac494072ca8249e1368c9974cec5e63ff363b9da79930b7a8fbb5cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.3 KB (96269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c33c986fa5bcf287e1c7594cc4bc4b13289d51ef15c3db591e513fcb7b653ce`

```dockerfile
```

-	Layers:
	-	`sha256:358b294b5bd4c90ab3ded38657baddb4cf8a5d594c5ea9c5683191efc2c70e05`  
		Last Modified: Wed, 13 Dec 2023 00:39:43 GMT  
		Size: 77.0 KB (76967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:708c671c1199a85cfb58a91ad4f1c34c29d381f2905468f64a42c8fbb6341e30`  
		Last Modified: Wed, 13 Dec 2023 00:39:43 GMT  
		Size: 19.3 KB (19302 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-alpine3.19`

```console
$ docker pull memcached@sha256:72f79c540a7204a0355f57a8e3080831c646db96684c69b6a47d36f70fc33cae
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
$ docker pull memcached@sha256:32affe08f4a1c6f62faacae1fee90575987d8b995a7257aa35ca1b4a817bdbf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6528299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fba850e40285109fcdc4c5603f2e081dba5bb683ffbcf0d4ad2e954359ce93e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 08 Dec 2023 01:20:49 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Fri, 08 Dec 2023 01:20:49 GMT
CMD ["/bin/sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd74bdcd28e46833593b2724720938c58842faa843fe42ea2411b3afd0739cb6`  
		Last Modified: Wed, 10 Jan 2024 23:58:18 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104a06a5eef3fffb9db79f8f67d4205725b9551aadbad7cb2847b013921bc212`  
		Last Modified: Wed, 10 Jan 2024 23:58:18 GMT  
		Size: 104.2 KB (104204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3271524d49893bc0950a7d058e91621dcfabe2383d6bfc0b13263faaf85f774f`  
		Last Modified: Wed, 10 Jan 2024 23:58:18 GMT  
		Size: 3.0 MB (3013977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb917829c49dd9d022cf427a72685718c30e113cfe036cffdf3eec29523e871`  
		Last Modified: Wed, 10 Jan 2024 23:58:18 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c390a9d8c6874260017223d74f3ae0b04895aa29a26c6ea03e0bd49832fe201`  
		Last Modified: Wed, 10 Jan 2024 23:58:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:a4db06e4e22e5cb6667aafc4b272349d5db9596147a2114d7b6997ae75e265f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 KB (98074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80b0a8c4800de05bc28d0cf54908bd75ed706e519dc72a22883d057213a1afdd`

```dockerfile
```

-	Layers:
	-	`sha256:9052d3e673c4418bce0a5b5c01961846c1fc2b14ace86d3afae91720a4744b70`  
		Last Modified: Wed, 10 Jan 2024 23:58:18 GMT  
		Size: 78.6 KB (78603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:667e7c7f728f9119016e4a456207d31154a85c080f74151700cc04835b950d54`  
		Last Modified: Wed, 10 Jan 2024 23:58:18 GMT  
		Size: 19.5 KB (19471 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:5550c34a395e8c02098f113a01d35d794b40c31c374f1e553dc80472d53978c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6372430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f4edcab8bc23e09f91d9a22a6d9df2a2d0175c23ad7cd396eaa4e849528f0e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 08 Dec 2023 01:39:30 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 08 Dec 2023 01:39:30 GMT
CMD ["/bin/sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c303524923177661067f7eb378c3dd5277088c2676ebd1cd78e68397bb80fdbf`  
		Last Modified: Fri, 08 Dec 2023 01:39:48 GMT  
		Size: 3.3 MB (3347794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfede01b081f27465377bdafbbdb6b694c6fab18026972b2c380535dcef103b8`  
		Last Modified: Wed, 13 Dec 2023 01:35:47 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d7b6f4ad45bf3aee58c5a7e8083286bd79dc004840903fd5997929772bfb4c`  
		Last Modified: Wed, 13 Dec 2023 01:35:47 GMT  
		Size: 120.9 KB (120897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f6c7840c606bfa580e1e6b52087faff29fb3986005ea3aadc31c64b3e4142e`  
		Last Modified: Thu, 11 Jan 2024 00:22:58 GMT  
		Size: 2.9 MB (2902089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1335fd4bd25daf4820a1c881f1ea0a30a575682074ad886293a372089bcd4544`  
		Last Modified: Thu, 11 Jan 2024 00:22:58 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48e51e3a0b635d352137fa3c7c3747c8192e7c8de0590e533ffdcea9dc49a96`  
		Last Modified: Thu, 11 Jan 2024 00:22:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:6faa51abf4ec7649d68a12af15126861e91479130b3f97128d3fa7a487d62422
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.9 KB (97945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e975d798c27c70d9498c44491a9aca9d24cee1fe8111bfae46401e7d9b1264`

```dockerfile
```

-	Layers:
	-	`sha256:0c5c585bb2d781fc112b82e19d343028a3c75758809ef4b46e4a6839bd0a1e41`  
		Last Modified: Thu, 11 Jan 2024 00:22:58 GMT  
		Size: 78.6 KB (78622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed5eb3630ee14af5005edfb5ed56d4660a5bbf224bf729ca0bfabaa0143d9864`  
		Last Modified: Thu, 11 Jan 2024 00:22:58 GMT  
		Size: 19.3 KB (19323 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.19` - linux; 386

```console
$ docker pull memcached@sha256:67373b38ed96c7ba59d5c1b8ba2b471d75d058ae7056f1e22674128af0e39ece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6185193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ec7484601b2ef9f91318f7c210dbd58716132fdd37be8004e82af4e4d42015b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 08 Dec 2023 01:38:25 GMT
ADD file:bd52540f209ba362654d795d7893669c819d35011a16f9f319301727a33b3bd9 in / 
# Fri, 08 Dec 2023 01:38:25 GMT
CMD ["/bin/sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9acd8b4c9d4385585f74dabb4bc6b3351888710ae37ec5dbd9ea950281b8f9bb`  
		Last Modified: Fri, 08 Dec 2023 01:38:43 GMT  
		Size: 3.2 MB (3244115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7759a4b7aa772576870eb5c52f815fbebd9be11b4781c708dc2ab6007fa609`  
		Last Modified: Wed, 10 Jan 2024 23:58:26 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5ca5419371cb9331b9ba1ea9086eef15ad135bf369ac2787491caf04de682f`  
		Last Modified: Wed, 10 Jan 2024 23:58:26 GMT  
		Size: 109.3 KB (109334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc68a66ccf11c1510081e6e9f70c399ad3ceff564e9b876ed2895ebf29b3ebb`  
		Last Modified: Wed, 10 Jan 2024 23:58:26 GMT  
		Size: 2.8 MB (2830103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b15634bddb0499598a6044cc0030e88ba0ce4cf2b02301cfa0a0faa1ac676cdd`  
		Last Modified: Wed, 10 Jan 2024 23:58:26 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dddc1630ef7eb2545abf068534d7032d19114a744cd485791f63f40ab0b5ab18`  
		Last Modified: Wed, 10 Jan 2024 23:58:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:15c53491df84b3d051fdcc7dff9dbdb9ca3718254ea873b6e2bbff7bc221abec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.0 KB (97973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fee76928da54f07fd68a5975f71e6f5991ccd3261cf759f3093b424e8f7ba99`

```dockerfile
```

-	Layers:
	-	`sha256:1ae5a47e6fefaee5dc9532fb45757803475b71d80ddf777a416ccd10c45bd09e`  
		Last Modified: Wed, 10 Jan 2024 23:58:26 GMT  
		Size: 78.6 KB (78558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ae992c52298a54654430860ae3828320c41eec63e8702ef1c66f1a68fdb937e`  
		Last Modified: Wed, 10 Jan 2024 23:58:26 GMT  
		Size: 19.4 KB (19415 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.19` - linux; ppc64le

```console
$ docker pull memcached@sha256:0639819cf6cbfd6e608ef2071abeb9ca10f049a89ecc83eee11f1d75b78cab2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6394995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12d25d4724561e2ace36bab912780d035fdb57c760fa9268b40e781584c2df0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 08 Dec 2023 01:22:51 GMT
ADD file:052421189f8d269382daaaa8beb63c687e4d8ca908c421abdce53bcc627a40b4 in / 
# Fri, 08 Dec 2023 01:22:51 GMT
CMD ["/bin/sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:243ac51c334a47917a84be93e972ee6378987e9b3b917a5a8df29025e161c1f3`  
		Last Modified: Fri, 08 Dec 2023 01:23:14 GMT  
		Size: 3.4 MB (3358233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add73e7dbebd6c86078686bb046ef57017b090fe917f656feb83ec0ef971b5f3`  
		Last Modified: Tue, 12 Dec 2023 23:20:17 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d64bed657a7e728633e13f2021b35954e98be9ecae77096d30cdaa1d9260d61e`  
		Last Modified: Tue, 12 Dec 2023 23:20:17 GMT  
		Size: 123.4 KB (123403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a69dac8774b0ef6bdf9b84b7360fb3346a88b05e510dbc3366a3a828349a839b`  
		Last Modified: Thu, 11 Jan 2024 00:13:43 GMT  
		Size: 2.9 MB (2911714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666eeed87216ed83fdc1a618d27175e1a8c8efd15354f7e22228e768ded7a7cf`  
		Last Modified: Thu, 11 Jan 2024 00:13:42 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfeab30e174bcb0fc8203612135497885d25cfc588a1e44de9e5b0b5048dcdb`  
		Last Modified: Thu, 11 Jan 2024 00:13:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:d20e9002675244162fdaf77d022444958c1a6d56dfe5901853240c568aea24b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 KB (96397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e870214daaeaabaf116e4a0a6462f63bc3d9ce9cd3d522277e53ba1d9c19a54e`

```dockerfile
```

-	Layers:
	-	`sha256:54016ce6ca1c0550269f0db7f3fec4511d81bef96b3c0f41709d785c7cefa5d3`  
		Last Modified: Thu, 11 Jan 2024 00:13:42 GMT  
		Size: 77.0 KB (77025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28bbe767bea18a4ae8896d545c4083a8a7a41145031227bdf28474500598aa2f`  
		Last Modified: Thu, 11 Jan 2024 00:13:42 GMT  
		Size: 19.4 KB (19372 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-alpine3.19` - linux; s390x

```console
$ docker pull memcached@sha256:53d0bdb491815057b9014ab30e95c68146d83accdc9d8d690e308e67e7f4eed5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4326665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b078f3aede6257187e9488318eac328332ace90ac171c8a99d0ca495e1e9ad40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 08 Dec 2023 01:41:50 GMT
ADD file:47e0982fc3ae485c06d46f3c0022afd39ed7ec95fe755c2391e6b0cfcae65dfc in / 
# Fri, 08 Dec 2023 01:41:51 GMT
CMD ["/bin/sh"]
# Sat, 09 Dec 2023 01:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 09 Dec 2023 01:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 09 Dec 2023 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.22
# Sat, 09 Dec 2023 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.22.tar.gz
# Sat, 09 Dec 2023 01:54:10 GMT
ENV MEMCACHED_SHA1=7a691f390d59616dbebfc9e2e4942d499c39a338
# Sat, 09 Dec 2023 01:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 09 Dec 2023 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 09 Dec 2023 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 09 Dec 2023 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 09 Dec 2023 01:54:10 GMT
USER memcache
# Sat, 09 Dec 2023 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 09 Dec 2023 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0fca3ee44ced87b7184bc23390283fdf10cfae0e844a25b785dd11c463815227`  
		Last Modified: Fri, 08 Dec 2023 01:42:30 GMT  
		Size: 3.2 MB (3242332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff601679be7ba19260a77b326cf587dcc37315b02c2e0b0effc7084da4684bd7`  
		Last Modified: Wed, 13 Dec 2023 00:39:43 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b2401b35befb0832d96cebfdee6215736b27c0e3d064d67da9917deca4c14c`  
		Last Modified: Wed, 13 Dec 2023 00:39:43 GMT  
		Size: 113.1 KB (113142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59b1e1447b7739e5338731014a96bea369258cbf54b2d152ef50bb06e308bad`  
		Last Modified: Wed, 13 Dec 2023 00:39:43 GMT  
		Size: 969.5 KB (969547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c62bb151b09d73f2bc083bb91abedfb6660c5045d34f7d576415190ae4e09f`  
		Last Modified: Wed, 13 Dec 2023 00:39:43 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaaf7e6dbf7fbf661d0b3f6f5d38fbd888ab6707a76919a5f4a633194e895a2f`  
		Last Modified: Wed, 13 Dec 2023 00:39:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:1c2ba4c72ac494072ca8249e1368c9974cec5e63ff363b9da79930b7a8fbb5cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.3 KB (96269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c33c986fa5bcf287e1c7594cc4bc4b13289d51ef15c3db591e513fcb7b653ce`

```dockerfile
```

-	Layers:
	-	`sha256:358b294b5bd4c90ab3ded38657baddb4cf8a5d594c5ea9c5683191efc2c70e05`  
		Last Modified: Wed, 13 Dec 2023 00:39:43 GMT  
		Size: 77.0 KB (76967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:708c671c1199a85cfb58a91ad4f1c34c29d381f2905468f64a42c8fbb6341e30`  
		Last Modified: Wed, 13 Dec 2023 00:39:43 GMT  
		Size: 19.3 KB (19302 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6-bookworm`

```console
$ docker pull memcached@sha256:59161db99b459a9315bbb8c52a243251d3cfcdb17f35a7900da8e5e64f0a8f32
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
$ docker pull memcached@sha256:643a24a57407d3cb2b8745f47a8d4b20406c19f5399ecb05db9727447637003a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38789237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d474793fb4125ae857b42efbf79eb1cbea8834a20e5d65627ea439b52b57313`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:27 GMT
ADD file:ac3cd70031d35e46d86b876934946ffc8756de4de065fbc926dce642dac07ff3 in / 
# Tue, 19 Dec 2023 01:20:28 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:af107e978371b6cd6339127a05502c5eacd1e6b0e9eb7b2f4aa7b6fc87e2dd81`  
		Last Modified: Tue, 19 Dec 2023 01:24:59 GMT  
		Size: 29.1 MB (29125963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d32ccca352404a5a8dedb6a7ca281abbc073b9d8643ef4626873ee1b8a204b1`  
		Last Modified: Wed, 10 Jan 2024 23:58:24 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d585b71055b9f919875cf91a81370309c971aad943e53b8c9fda2b63521f873`  
		Last Modified: Wed, 10 Jan 2024 23:58:25 GMT  
		Size: 2.5 MB (2488298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc47ad75df3e3af04459ae59b5c7ec1ea8dd657b7fb4cc42ec85a982a98da628`  
		Last Modified: Wed, 10 Jan 2024 23:58:25 GMT  
		Size: 7.2 MB (7173458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66204efbd683596758bec893cba01fce3fe386da63399af101051d8df26c2477`  
		Last Modified: Wed, 10 Jan 2024 23:58:25 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3406bc9285b7e906c211fd9a5d9342ee80d9e0ae728a6529d14db42aecf145`  
		Last Modified: Wed, 10 Jan 2024 23:58:25 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:8efa487487fc160476637a4fb2aec45b4a38eb677aeddcd0ecaeab362e136e85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3077977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:928c59acdba2c812e1299dcb8c4a4c7a7bdfadbc695533aab940957913a8b768`

```dockerfile
```

-	Layers:
	-	`sha256:7777c14054a0e9893c312cf26a23d80bb2f16d3cd6dacad21c21c8fb1be321a4`  
		Last Modified: Wed, 10 Jan 2024 23:58:25 GMT  
		Size: 3.1 MB (3056860 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc8d2dbb4d2d164636bb06f04252d4aec50002cf7469a8955e322e104563d025`  
		Last Modified: Wed, 10 Jan 2024 23:58:24 GMT  
		Size: 21.1 KB (21117 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:d01aca5f5e26f687d6ad14ec6547e704f453acc02ce0ce2e5fa5871f5013bfbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34811390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f12a90da675230d99a32d19f573412751d7740cae5f90d74a8c49b4b6f64a3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 19 Dec 2023 01:55:22 GMT
ADD file:9503ab966c9dd707eeccc7c2f633bccc94c199f8714ec4ff2c8b54dde3dbabf9 in / 
# Tue, 19 Dec 2023 01:55:22 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1ae9a2844c8c70942d2220553689b62e841cc706d77284fbfedbd770080fd699`  
		Last Modified: Tue, 19 Dec 2023 01:58:33 GMT  
		Size: 26.9 MB (26885440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ab650f4c7d61856342d3b0e4d9bad9cd0c4336fb403dab9c5c1ed2c285774f`  
		Last Modified: Thu, 11 Jan 2024 00:07:53 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b10807a0745d6e1ccc36157b11a3469a17c6477eda65233bb2f182c7958db5b8`  
		Last Modified: Thu, 11 Jan 2024 00:07:54 GMT  
		Size: 2.1 MB (2089356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5bc9bbfb0a70ce84a09ce58d70ebf97841c03e06d3968f065cd9361bd0e990`  
		Last Modified: Thu, 11 Jan 2024 00:07:54 GMT  
		Size: 5.8 MB (5835079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74b3373a0a7639196238720db6061026ccfe87c48ccf38fcfbc737699c9f2b7`  
		Last Modified: Thu, 11 Jan 2024 00:07:53 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3969d1f7528c0ba1d0047402bf5611d53c8f502f52fbbd7fb827f8de5ab813f6`  
		Last Modified: Thu, 11 Jan 2024 00:07:54 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:7484a951008b8e170922f1467a179c839a675cf4ab9555315f6bb20174be8173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3052683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d85ee8bbb3867fa9cbdd5e06e5791b62e1c7dfc410295ba05b95ead8b6c4525`

```dockerfile
```

-	Layers:
	-	`sha256:34e791a9d4149137cb6b8da59558d4bf4ce80c9bcd5ab599785c7a3aaa2fc844`  
		Last Modified: Thu, 11 Jan 2024 00:07:54 GMT  
		Size: 3.0 MB (3031592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31263ce608cc2e18001c08b34ad8f21b27befcf21ee30dd42bd87176f24a5e10`  
		Last Modified: Thu, 11 Jan 2024 00:07:53 GMT  
		Size: 21.1 KB (21091 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:1b119620b1cbaac4281975bedfed15ff721d868ec9eda9574dc4c1ec58330716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37686962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45b76a80b62f56ff1c68ed4e7ce2dfe225b3560e00750a3210c8d897b1547f3a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:11 GMT
ADD file:262fd7bf0bc26e5d2a229fba52626e22b8a93beac29733acfc60e716c26e689d in / 
# Tue, 19 Dec 2023 01:41:11 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:24e221e92a36ab5b0075dd156b4f2ff095532a9b0927946cf6070bb1bea208b8`  
		Last Modified: Tue, 19 Dec 2023 01:44:38 GMT  
		Size: 29.2 MB (29157269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d79fe3da079136cc418087e5d4e432357c062519668a3c03b78c24710c3a6ec`  
		Last Modified: Wed, 20 Dec 2023 10:20:11 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:496388416e6f8cdbf05e6ea4a56e906308e4b95b9f984f73b5c5a3fdbe5b12aa`  
		Last Modified: Wed, 20 Dec 2023 10:20:11 GMT  
		Size: 2.3 MB (2346023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee91bf234e7544eb6ad4c5f18ba87a8c0306d87f51ee1c47b1361569175a8a7c`  
		Last Modified: Thu, 11 Jan 2024 00:20:26 GMT  
		Size: 6.2 MB (6182151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73888be7ca392dfe14270a838c67a2d7ccfe9354f1fe52147291c9756127b51`  
		Last Modified: Thu, 11 Jan 2024 00:20:25 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a917a1ebe539f36501d4bebb89957491c647a119a1702734b1a0c9c01dc2a6`  
		Last Modified: Thu, 11 Jan 2024 00:20:25 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:f96d1dde1233068de191226772289ac63a784a466d34ec1dbf67e72559643f7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3053019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f249bf848fae6f5b573dffd3d8dbd830fd3267c6f487d397fd82ba104fee46b`

```dockerfile
```

-	Layers:
	-	`sha256:09c490b7c5d08149f654887eca9ca058a49a3b659d3e7282589a431883445a49`  
		Last Modified: Thu, 11 Jan 2024 00:20:25 GMT  
		Size: 3.0 MB (3032051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abe3c6e55476a176987bc5b5f8bad00ca16d1299d36e40f52e82dcb76ed0600c`  
		Last Modified: Thu, 11 Jan 2024 00:20:25 GMT  
		Size: 21.0 KB (20968 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:a5d93bfce917e364c0f16cdad7b683a36011a997db4be6db2770644095aea01d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39272936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:902b98d31b0a747e1d90226bbd3f7fb16592c8f606009585e9b2bbb819bfb30e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 19 Dec 2023 01:39:07 GMT
ADD file:6f4083d57ea9644b5a827e67b0725087a15aa428272ec223ab968bf8b4623e42 in / 
# Tue, 19 Dec 2023 01:39:07 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8d4aad22fb6a12b8cc7a78d338dfb9bc2bd6d621517b374e446f2915833ea883`  
		Last Modified: Tue, 19 Dec 2023 01:43:45 GMT  
		Size: 30.1 MB (30143863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22ddf2b3cd1581c8f1483d20c8fb232852e525fea04a97ffd9ac744939dffc0`  
		Last Modified: Wed, 10 Jan 2024 23:58:29 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23537023da95e2b44ae9e7aebee71e05ecb397f02a351f30f6c69a752d98d1a5`  
		Last Modified: Wed, 10 Jan 2024 23:58:29 GMT  
		Size: 2.5 MB (2492560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8636f3d8b77edac77347698b78afe5ce4f443daa01f0a424d809c8ed35405ac5`  
		Last Modified: Wed, 10 Jan 2024 23:58:29 GMT  
		Size: 6.6 MB (6634994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41afb4f2ebc199845ca27aae99895e43658c24f7fbdea6a0b17769f1fd238b3f`  
		Last Modified: Wed, 10 Jan 2024 23:58:29 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aee346987d8e42b5a7c3ecdc4b2efa5e402c43f65712c94e3f30606c9b365e4`  
		Last Modified: Wed, 10 Jan 2024 23:58:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:71cbd1b0df460e30d13a768ed26659ea3d35001b788219b4eac0d77078e71ab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3072225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7173243e71de72bb179738a15514dee35cfb9c1f1ab3da05adc2fd1ea74335cf`

```dockerfile
```

-	Layers:
	-	`sha256:4e2e18fc597957c9c8202a8015176e35b070a14ec422ca3b88fdfaa64cd693d0`  
		Last Modified: Wed, 10 Jan 2024 23:58:29 GMT  
		Size: 3.1 MB (3051163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1dc46fbcfd7dddfe981ea410938185ededc5f8f383164b2ffe266c923d1e7ed`  
		Last Modified: Wed, 10 Jan 2024 23:58:29 GMT  
		Size: 21.1 KB (21062 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:d6b10482cd93239feb732ab9b3bcdd207e5be672b55c01b1faa72c6e10da9ee3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37564394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bed0ab2d751422f3dfcd94712006ab27d4cdd43e18f83b8b38199c2cee3b2514`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 19 Dec 2023 02:13:36 GMT
ADD file:dcd5696ac281b24df52a518e2402c7f7a4caedfcba0d82e195b7c06cd3a38fdd in / 
# Tue, 19 Dec 2023 02:13:40 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:12b1322ffb17b8e81ca1c6d9d7118e2fcee0b9d971aa3c90601e6345804a60d1`  
		Last Modified: Tue, 19 Dec 2023 02:24:36 GMT  
		Size: 29.1 MB (29121427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6b93f134841b66512a1d4138bdf28b0506ffd27490aac735508b3f20716618`  
		Last Modified: Thu, 11 Jan 2024 00:10:54 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573e69b5f2977543c86d4410256c381ef97d7f37a89be2a88bfbda683c24110e`  
		Last Modified: Thu, 11 Jan 2024 00:10:55 GMT  
		Size: 1.9 MB (1937514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb552cccf8bd4122265e6895c4c9ce039b90dd08574f0e4911a0b11aaf1f7b2c`  
		Last Modified: Thu, 11 Jan 2024 00:10:55 GMT  
		Size: 6.5 MB (6503938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b640b85282363650ba7d87fea47ce2e4cfe96da07ab6c4b47eebc739f96910`  
		Last Modified: Thu, 11 Jan 2024 00:10:54 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933eef8a1d4865a3e302557839a52d00229ef80652113710df9fd606880475c5`  
		Last Modified: Thu, 11 Jan 2024 00:10:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:c1162ead1e62fcd87632e902387935d8f33b794c009815419baf8cb396548f85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aa26ec0ff6dd44911a88c2d2af479e0c05cfb46e9db65187abe71da51f56001`

```dockerfile
```

-	Layers:
	-	`sha256:2454765cb79a60d22f96ec7e66ea9fb222b40c30758e0df9a59c7192c39847da`  
		Last Modified: Thu, 11 Jan 2024 00:10:54 GMT  
		Size: 20.8 KB (20837 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:b7976b1191a4f34442e257f55f30f8b4efd28f5f8026936846e8a5471e0c8505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.0 MB (43007490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75346431bfc757a49f790022140e267e0e6838110c75cad2bf8ab9e24e2855fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 19 Dec 2023 01:21:50 GMT
ADD file:ca1db68689e0b0388337ba450ad2c8e79c159c6b78f5aa6d3ff2b89b8d7edc93 in / 
# Tue, 19 Dec 2023 01:21:51 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fc9b8f5eec3aa37ab3aace05165427479352f290d53904cea87dca6349633a09`  
		Last Modified: Tue, 19 Dec 2023 01:26:19 GMT  
		Size: 33.1 MB (33120558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f85ae146a90d1ce7561d4e67d1ce2eaf0a0da444bb8a70c5b7fc94d0dc75e389`  
		Last Modified: Wed, 20 Dec 2023 08:43:43 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23065e9a12cf130c31375986a9b4700b84f2539ccb4b47efe0f375f77938fc3`  
		Last Modified: Wed, 20 Dec 2023 08:43:44 GMT  
		Size: 2.7 MB (2698240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b8249b30995d06e02d41e31406a930c02163d057cd39ad2cb7f710df2f6c60`  
		Last Modified: Thu, 11 Jan 2024 00:10:31 GMT  
		Size: 7.2 MB (7187176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a238b8549095cec1619f8f38f82d1aeb50acdf094b2b611b1fb5c62da14635f`  
		Last Modified: Thu, 11 Jan 2024 00:10:31 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669f29d97099310deca355ff837c9885adea00bb9c6e460490904627b7a40e4b`  
		Last Modified: Thu, 11 Jan 2024 00:10:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:87bde9e8cd8d07c6306a9ef516b822eadb9669d79da8587f1ac892066646ad33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3066464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:034c7634fd9e3419a42aa94fb6c3c05bd8d951eaf75eef2fbd2e8d64150013ba`

```dockerfile
```

-	Layers:
	-	`sha256:0a90f178efc50a3500b5ee2dce72b560153f2b0ec4cc6e79aa940561e8d58590`  
		Last Modified: Thu, 11 Jan 2024 00:10:31 GMT  
		Size: 3.0 MB (3045446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35a907ae4a36d514f4ff1b8d97766c9a5166c6116bc026f627e4de4cc51111fe`  
		Last Modified: Thu, 11 Jan 2024 00:10:30 GMT  
		Size: 21.0 KB (21018 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6-bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:9110d0aec3fc0be39a13bfd7030a3d04f36e230034078de3b407ae883f3e3de2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35722087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aef7bb08b32c1c17f11984770392abcc11b268465af0e89884793edf6ec092dd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 04 Dec 2023 18:08:47 GMT
ADD file:f06f12fa5a93afc3a79ac4371d24b0a471a5a1818cf34c1d90004c8f410914b9 in / 
# Mon, 04 Dec 2023 18:08:47 GMT
CMD ["bash"]
# Mon, 04 Dec 2023 18:08:47 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 04 Dec 2023 18:08:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 04 Dec 2023 18:08:47 GMT
ENV MEMCACHED_VERSION=1.6.22
# Mon, 04 Dec 2023 18:08:47 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.22.tar.gz
# Mon, 04 Dec 2023 18:08:47 GMT
ENV MEMCACHED_SHA1=7a691f390d59616dbebfc9e2e4942d499c39a338
# Mon, 04 Dec 2023 18:08:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 04 Dec 2023 18:08:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 Dec 2023 18:08:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 04 Dec 2023 18:08:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 Dec 2023 18:08:47 GMT
USER memcache
# Mon, 04 Dec 2023 18:08:47 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 04 Dec 2023 18:08:47 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bc6b1888979d3ceb063da848b2034e980e2c2613642159c1e856550b79aa620c`  
		Last Modified: Tue, 19 Dec 2023 01:47:38 GMT  
		Size: 27.5 MB (27491874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b453a12051612cbbdca8ee1a3c9e8211ac636f53786a525b824574fff746cda`  
		Last Modified: Tue, 19 Dec 2023 15:38:14 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7903f8445b1bbbe476fd67c998f57a5289b3d4a9e65a1190e551b7c79083e65d`  
		Last Modified: Tue, 19 Dec 2023 15:38:15 GMT  
		Size: 2.2 MB (2152511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf54a1600c7ab496cf3e01f5ec34a3ae7dfbf25014ef90ec9c7b005aa3d887c`  
		Last Modified: Tue, 19 Dec 2023 15:38:14 GMT  
		Size: 6.1 MB (6076186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b446e4dc631c597d82b5e437bf342d8607d8a4ff3229d052f049bfbac270e2c6`  
		Last Modified: Tue, 19 Dec 2023 15:38:14 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee453ca29f8bbd4b452693cd9f2e2e1b7cff2fa139d7fc942de190d244ae6617`  
		Last Modified: Tue, 19 Dec 2023 15:38:15 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:2fa3455fc28f5964cc39eaaadcfab8df0a8dd5552a08464b0f87cbc775addb70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3067351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddb3e50e2a70d6400f4ba5be3b4010e9a0f7770e69e2c1e1c599bf6224ed8ac8`

```dockerfile
```

-	Layers:
	-	`sha256:2dcfb5805d88251b9b79a3c0e144091f0dc62a366eddacb9d50aa89a825067ef`  
		Last Modified: Tue, 19 Dec 2023 15:38:14 GMT  
		Size: 3.0 MB (3046401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb52cc58a7fa498aa7b56431dbe3e004db5d4b028b724bc1f087b44c1baaa25c`  
		Last Modified: Tue, 19 Dec 2023 15:38:14 GMT  
		Size: 20.9 KB (20950 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.23`

```console
$ docker pull memcached@sha256:49d7bf63abf1842ab67ab13ce42a399f72ffcdec2c6c405020be7371882abea7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
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

### `memcached:1.6.23` - linux; amd64

```console
$ docker pull memcached@sha256:643a24a57407d3cb2b8745f47a8d4b20406c19f5399ecb05db9727447637003a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38789237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d474793fb4125ae857b42efbf79eb1cbea8834a20e5d65627ea439b52b57313`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:27 GMT
ADD file:ac3cd70031d35e46d86b876934946ffc8756de4de065fbc926dce642dac07ff3 in / 
# Tue, 19 Dec 2023 01:20:28 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:af107e978371b6cd6339127a05502c5eacd1e6b0e9eb7b2f4aa7b6fc87e2dd81`  
		Last Modified: Tue, 19 Dec 2023 01:24:59 GMT  
		Size: 29.1 MB (29125963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d32ccca352404a5a8dedb6a7ca281abbc073b9d8643ef4626873ee1b8a204b1`  
		Last Modified: Wed, 10 Jan 2024 23:58:24 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d585b71055b9f919875cf91a81370309c971aad943e53b8c9fda2b63521f873`  
		Last Modified: Wed, 10 Jan 2024 23:58:25 GMT  
		Size: 2.5 MB (2488298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc47ad75df3e3af04459ae59b5c7ec1ea8dd657b7fb4cc42ec85a982a98da628`  
		Last Modified: Wed, 10 Jan 2024 23:58:25 GMT  
		Size: 7.2 MB (7173458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66204efbd683596758bec893cba01fce3fe386da63399af101051d8df26c2477`  
		Last Modified: Wed, 10 Jan 2024 23:58:25 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3406bc9285b7e906c211fd9a5d9342ee80d9e0ae728a6529d14db42aecf145`  
		Last Modified: Wed, 10 Jan 2024 23:58:25 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.23` - unknown; unknown

```console
$ docker pull memcached@sha256:8efa487487fc160476637a4fb2aec45b4a38eb677aeddcd0ecaeab362e136e85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3077977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:928c59acdba2c812e1299dcb8c4a4c7a7bdfadbc695533aab940957913a8b768`

```dockerfile
```

-	Layers:
	-	`sha256:7777c14054a0e9893c312cf26a23d80bb2f16d3cd6dacad21c21c8fb1be321a4`  
		Last Modified: Wed, 10 Jan 2024 23:58:25 GMT  
		Size: 3.1 MB (3056860 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc8d2dbb4d2d164636bb06f04252d4aec50002cf7469a8955e322e104563d025`  
		Last Modified: Wed, 10 Jan 2024 23:58:24 GMT  
		Size: 21.1 KB (21117 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.23` - linux; arm variant v5

```console
$ docker pull memcached@sha256:d01aca5f5e26f687d6ad14ec6547e704f453acc02ce0ce2e5fa5871f5013bfbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34811390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f12a90da675230d99a32d19f573412751d7740cae5f90d74a8c49b4b6f64a3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 19 Dec 2023 01:55:22 GMT
ADD file:9503ab966c9dd707eeccc7c2f633bccc94c199f8714ec4ff2c8b54dde3dbabf9 in / 
# Tue, 19 Dec 2023 01:55:22 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1ae9a2844c8c70942d2220553689b62e841cc706d77284fbfedbd770080fd699`  
		Last Modified: Tue, 19 Dec 2023 01:58:33 GMT  
		Size: 26.9 MB (26885440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ab650f4c7d61856342d3b0e4d9bad9cd0c4336fb403dab9c5c1ed2c285774f`  
		Last Modified: Thu, 11 Jan 2024 00:07:53 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b10807a0745d6e1ccc36157b11a3469a17c6477eda65233bb2f182c7958db5b8`  
		Last Modified: Thu, 11 Jan 2024 00:07:54 GMT  
		Size: 2.1 MB (2089356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5bc9bbfb0a70ce84a09ce58d70ebf97841c03e06d3968f065cd9361bd0e990`  
		Last Modified: Thu, 11 Jan 2024 00:07:54 GMT  
		Size: 5.8 MB (5835079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74b3373a0a7639196238720db6061026ccfe87c48ccf38fcfbc737699c9f2b7`  
		Last Modified: Thu, 11 Jan 2024 00:07:53 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3969d1f7528c0ba1d0047402bf5611d53c8f502f52fbbd7fb827f8de5ab813f6`  
		Last Modified: Thu, 11 Jan 2024 00:07:54 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.23` - unknown; unknown

```console
$ docker pull memcached@sha256:7484a951008b8e170922f1467a179c839a675cf4ab9555315f6bb20174be8173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3052683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d85ee8bbb3867fa9cbdd5e06e5791b62e1c7dfc410295ba05b95ead8b6c4525`

```dockerfile
```

-	Layers:
	-	`sha256:34e791a9d4149137cb6b8da59558d4bf4ce80c9bcd5ab599785c7a3aaa2fc844`  
		Last Modified: Thu, 11 Jan 2024 00:07:54 GMT  
		Size: 3.0 MB (3031592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31263ce608cc2e18001c08b34ad8f21b27befcf21ee30dd42bd87176f24a5e10`  
		Last Modified: Thu, 11 Jan 2024 00:07:53 GMT  
		Size: 21.1 KB (21091 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.23` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:1b119620b1cbaac4281975bedfed15ff721d868ec9eda9574dc4c1ec58330716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37686962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45b76a80b62f56ff1c68ed4e7ce2dfe225b3560e00750a3210c8d897b1547f3a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:11 GMT
ADD file:262fd7bf0bc26e5d2a229fba52626e22b8a93beac29733acfc60e716c26e689d in / 
# Tue, 19 Dec 2023 01:41:11 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:24e221e92a36ab5b0075dd156b4f2ff095532a9b0927946cf6070bb1bea208b8`  
		Last Modified: Tue, 19 Dec 2023 01:44:38 GMT  
		Size: 29.2 MB (29157269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d79fe3da079136cc418087e5d4e432357c062519668a3c03b78c24710c3a6ec`  
		Last Modified: Wed, 20 Dec 2023 10:20:11 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:496388416e6f8cdbf05e6ea4a56e906308e4b95b9f984f73b5c5a3fdbe5b12aa`  
		Last Modified: Wed, 20 Dec 2023 10:20:11 GMT  
		Size: 2.3 MB (2346023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee91bf234e7544eb6ad4c5f18ba87a8c0306d87f51ee1c47b1361569175a8a7c`  
		Last Modified: Thu, 11 Jan 2024 00:20:26 GMT  
		Size: 6.2 MB (6182151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73888be7ca392dfe14270a838c67a2d7ccfe9354f1fe52147291c9756127b51`  
		Last Modified: Thu, 11 Jan 2024 00:20:25 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a917a1ebe539f36501d4bebb89957491c647a119a1702734b1a0c9c01dc2a6`  
		Last Modified: Thu, 11 Jan 2024 00:20:25 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.23` - unknown; unknown

```console
$ docker pull memcached@sha256:f96d1dde1233068de191226772289ac63a784a466d34ec1dbf67e72559643f7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3053019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f249bf848fae6f5b573dffd3d8dbd830fd3267c6f487d397fd82ba104fee46b`

```dockerfile
```

-	Layers:
	-	`sha256:09c490b7c5d08149f654887eca9ca058a49a3b659d3e7282589a431883445a49`  
		Last Modified: Thu, 11 Jan 2024 00:20:25 GMT  
		Size: 3.0 MB (3032051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abe3c6e55476a176987bc5b5f8bad00ca16d1299d36e40f52e82dcb76ed0600c`  
		Last Modified: Thu, 11 Jan 2024 00:20:25 GMT  
		Size: 21.0 KB (20968 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.23` - linux; 386

```console
$ docker pull memcached@sha256:a5d93bfce917e364c0f16cdad7b683a36011a997db4be6db2770644095aea01d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39272936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:902b98d31b0a747e1d90226bbd3f7fb16592c8f606009585e9b2bbb819bfb30e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 19 Dec 2023 01:39:07 GMT
ADD file:6f4083d57ea9644b5a827e67b0725087a15aa428272ec223ab968bf8b4623e42 in / 
# Tue, 19 Dec 2023 01:39:07 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8d4aad22fb6a12b8cc7a78d338dfb9bc2bd6d621517b374e446f2915833ea883`  
		Last Modified: Tue, 19 Dec 2023 01:43:45 GMT  
		Size: 30.1 MB (30143863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22ddf2b3cd1581c8f1483d20c8fb232852e525fea04a97ffd9ac744939dffc0`  
		Last Modified: Wed, 10 Jan 2024 23:58:29 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23537023da95e2b44ae9e7aebee71e05ecb397f02a351f30f6c69a752d98d1a5`  
		Last Modified: Wed, 10 Jan 2024 23:58:29 GMT  
		Size: 2.5 MB (2492560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8636f3d8b77edac77347698b78afe5ce4f443daa01f0a424d809c8ed35405ac5`  
		Last Modified: Wed, 10 Jan 2024 23:58:29 GMT  
		Size: 6.6 MB (6634994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41afb4f2ebc199845ca27aae99895e43658c24f7fbdea6a0b17769f1fd238b3f`  
		Last Modified: Wed, 10 Jan 2024 23:58:29 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aee346987d8e42b5a7c3ecdc4b2efa5e402c43f65712c94e3f30606c9b365e4`  
		Last Modified: Wed, 10 Jan 2024 23:58:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.23` - unknown; unknown

```console
$ docker pull memcached@sha256:71cbd1b0df460e30d13a768ed26659ea3d35001b788219b4eac0d77078e71ab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3072225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7173243e71de72bb179738a15514dee35cfb9c1f1ab3da05adc2fd1ea74335cf`

```dockerfile
```

-	Layers:
	-	`sha256:4e2e18fc597957c9c8202a8015176e35b070a14ec422ca3b88fdfaa64cd693d0`  
		Last Modified: Wed, 10 Jan 2024 23:58:29 GMT  
		Size: 3.1 MB (3051163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1dc46fbcfd7dddfe981ea410938185ededc5f8f383164b2ffe266c923d1e7ed`  
		Last Modified: Wed, 10 Jan 2024 23:58:29 GMT  
		Size: 21.1 KB (21062 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.23` - linux; mips64le

```console
$ docker pull memcached@sha256:d6b10482cd93239feb732ab9b3bcdd207e5be672b55c01b1faa72c6e10da9ee3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37564394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bed0ab2d751422f3dfcd94712006ab27d4cdd43e18f83b8b38199c2cee3b2514`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 19 Dec 2023 02:13:36 GMT
ADD file:dcd5696ac281b24df52a518e2402c7f7a4caedfcba0d82e195b7c06cd3a38fdd in / 
# Tue, 19 Dec 2023 02:13:40 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:12b1322ffb17b8e81ca1c6d9d7118e2fcee0b9d971aa3c90601e6345804a60d1`  
		Last Modified: Tue, 19 Dec 2023 02:24:36 GMT  
		Size: 29.1 MB (29121427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6b93f134841b66512a1d4138bdf28b0506ffd27490aac735508b3f20716618`  
		Last Modified: Thu, 11 Jan 2024 00:10:54 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573e69b5f2977543c86d4410256c381ef97d7f37a89be2a88bfbda683c24110e`  
		Last Modified: Thu, 11 Jan 2024 00:10:55 GMT  
		Size: 1.9 MB (1937514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb552cccf8bd4122265e6895c4c9ce039b90dd08574f0e4911a0b11aaf1f7b2c`  
		Last Modified: Thu, 11 Jan 2024 00:10:55 GMT  
		Size: 6.5 MB (6503938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b640b85282363650ba7d87fea47ce2e4cfe96da07ab6c4b47eebc739f96910`  
		Last Modified: Thu, 11 Jan 2024 00:10:54 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933eef8a1d4865a3e302557839a52d00229ef80652113710df9fd606880475c5`  
		Last Modified: Thu, 11 Jan 2024 00:10:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.23` - unknown; unknown

```console
$ docker pull memcached@sha256:c1162ead1e62fcd87632e902387935d8f33b794c009815419baf8cb396548f85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aa26ec0ff6dd44911a88c2d2af479e0c05cfb46e9db65187abe71da51f56001`

```dockerfile
```

-	Layers:
	-	`sha256:2454765cb79a60d22f96ec7e66ea9fb222b40c30758e0df9a59c7192c39847da`  
		Last Modified: Thu, 11 Jan 2024 00:10:54 GMT  
		Size: 20.8 KB (20837 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.23` - linux; ppc64le

```console
$ docker pull memcached@sha256:b7976b1191a4f34442e257f55f30f8b4efd28f5f8026936846e8a5471e0c8505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.0 MB (43007490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75346431bfc757a49f790022140e267e0e6838110c75cad2bf8ab9e24e2855fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 19 Dec 2023 01:21:50 GMT
ADD file:ca1db68689e0b0388337ba450ad2c8e79c159c6b78f5aa6d3ff2b89b8d7edc93 in / 
# Tue, 19 Dec 2023 01:21:51 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fc9b8f5eec3aa37ab3aace05165427479352f290d53904cea87dca6349633a09`  
		Last Modified: Tue, 19 Dec 2023 01:26:19 GMT  
		Size: 33.1 MB (33120558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f85ae146a90d1ce7561d4e67d1ce2eaf0a0da444bb8a70c5b7fc94d0dc75e389`  
		Last Modified: Wed, 20 Dec 2023 08:43:43 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23065e9a12cf130c31375986a9b4700b84f2539ccb4b47efe0f375f77938fc3`  
		Last Modified: Wed, 20 Dec 2023 08:43:44 GMT  
		Size: 2.7 MB (2698240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b8249b30995d06e02d41e31406a930c02163d057cd39ad2cb7f710df2f6c60`  
		Last Modified: Thu, 11 Jan 2024 00:10:31 GMT  
		Size: 7.2 MB (7187176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a238b8549095cec1619f8f38f82d1aeb50acdf094b2b611b1fb5c62da14635f`  
		Last Modified: Thu, 11 Jan 2024 00:10:31 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669f29d97099310deca355ff837c9885adea00bb9c6e460490904627b7a40e4b`  
		Last Modified: Thu, 11 Jan 2024 00:10:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.23` - unknown; unknown

```console
$ docker pull memcached@sha256:87bde9e8cd8d07c6306a9ef516b822eadb9669d79da8587f1ac892066646ad33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3066464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:034c7634fd9e3419a42aa94fb6c3c05bd8d951eaf75eef2fbd2e8d64150013ba`

```dockerfile
```

-	Layers:
	-	`sha256:0a90f178efc50a3500b5ee2dce72b560153f2b0ec4cc6e79aa940561e8d58590`  
		Last Modified: Thu, 11 Jan 2024 00:10:31 GMT  
		Size: 3.0 MB (3045446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35a907ae4a36d514f4ff1b8d97766c9a5166c6116bc026f627e4de4cc51111fe`  
		Last Modified: Thu, 11 Jan 2024 00:10:30 GMT  
		Size: 21.0 KB (21018 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.23-alpine`

```console
$ docker pull memcached@sha256:72a1f3a3adf62cb2b09914c7ca1bbe69491400b6d95e8bdfea90093a4f0a866b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `memcached:1.6.23-alpine` - linux; amd64

```console
$ docker pull memcached@sha256:32affe08f4a1c6f62faacae1fee90575987d8b995a7257aa35ca1b4a817bdbf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6528299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fba850e40285109fcdc4c5603f2e081dba5bb683ffbcf0d4ad2e954359ce93e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 08 Dec 2023 01:20:49 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Fri, 08 Dec 2023 01:20:49 GMT
CMD ["/bin/sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd74bdcd28e46833593b2724720938c58842faa843fe42ea2411b3afd0739cb6`  
		Last Modified: Wed, 10 Jan 2024 23:58:18 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104a06a5eef3fffb9db79f8f67d4205725b9551aadbad7cb2847b013921bc212`  
		Last Modified: Wed, 10 Jan 2024 23:58:18 GMT  
		Size: 104.2 KB (104204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3271524d49893bc0950a7d058e91621dcfabe2383d6bfc0b13263faaf85f774f`  
		Last Modified: Wed, 10 Jan 2024 23:58:18 GMT  
		Size: 3.0 MB (3013977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb917829c49dd9d022cf427a72685718c30e113cfe036cffdf3eec29523e871`  
		Last Modified: Wed, 10 Jan 2024 23:58:18 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c390a9d8c6874260017223d74f3ae0b04895aa29a26c6ea03e0bd49832fe201`  
		Last Modified: Wed, 10 Jan 2024 23:58:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.23-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:a4db06e4e22e5cb6667aafc4b272349d5db9596147a2114d7b6997ae75e265f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 KB (98074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80b0a8c4800de05bc28d0cf54908bd75ed706e519dc72a22883d057213a1afdd`

```dockerfile
```

-	Layers:
	-	`sha256:9052d3e673c4418bce0a5b5c01961846c1fc2b14ace86d3afae91720a4744b70`  
		Last Modified: Wed, 10 Jan 2024 23:58:18 GMT  
		Size: 78.6 KB (78603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:667e7c7f728f9119016e4a456207d31154a85c080f74151700cc04835b950d54`  
		Last Modified: Wed, 10 Jan 2024 23:58:18 GMT  
		Size: 19.5 KB (19471 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.23-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:5550c34a395e8c02098f113a01d35d794b40c31c374f1e553dc80472d53978c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6372430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f4edcab8bc23e09f91d9a22a6d9df2a2d0175c23ad7cd396eaa4e849528f0e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 08 Dec 2023 01:39:30 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 08 Dec 2023 01:39:30 GMT
CMD ["/bin/sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c303524923177661067f7eb378c3dd5277088c2676ebd1cd78e68397bb80fdbf`  
		Last Modified: Fri, 08 Dec 2023 01:39:48 GMT  
		Size: 3.3 MB (3347794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfede01b081f27465377bdafbbdb6b694c6fab18026972b2c380535dcef103b8`  
		Last Modified: Wed, 13 Dec 2023 01:35:47 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d7b6f4ad45bf3aee58c5a7e8083286bd79dc004840903fd5997929772bfb4c`  
		Last Modified: Wed, 13 Dec 2023 01:35:47 GMT  
		Size: 120.9 KB (120897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f6c7840c606bfa580e1e6b52087faff29fb3986005ea3aadc31c64b3e4142e`  
		Last Modified: Thu, 11 Jan 2024 00:22:58 GMT  
		Size: 2.9 MB (2902089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1335fd4bd25daf4820a1c881f1ea0a30a575682074ad886293a372089bcd4544`  
		Last Modified: Thu, 11 Jan 2024 00:22:58 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48e51e3a0b635d352137fa3c7c3747c8192e7c8de0590e533ffdcea9dc49a96`  
		Last Modified: Thu, 11 Jan 2024 00:22:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.23-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:6faa51abf4ec7649d68a12af15126861e91479130b3f97128d3fa7a487d62422
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.9 KB (97945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e975d798c27c70d9498c44491a9aca9d24cee1fe8111bfae46401e7d9b1264`

```dockerfile
```

-	Layers:
	-	`sha256:0c5c585bb2d781fc112b82e19d343028a3c75758809ef4b46e4a6839bd0a1e41`  
		Last Modified: Thu, 11 Jan 2024 00:22:58 GMT  
		Size: 78.6 KB (78622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed5eb3630ee14af5005edfb5ed56d4660a5bbf224bf729ca0bfabaa0143d9864`  
		Last Modified: Thu, 11 Jan 2024 00:22:58 GMT  
		Size: 19.3 KB (19323 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.23-alpine` - linux; 386

```console
$ docker pull memcached@sha256:67373b38ed96c7ba59d5c1b8ba2b471d75d058ae7056f1e22674128af0e39ece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6185193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ec7484601b2ef9f91318f7c210dbd58716132fdd37be8004e82af4e4d42015b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 08 Dec 2023 01:38:25 GMT
ADD file:bd52540f209ba362654d795d7893669c819d35011a16f9f319301727a33b3bd9 in / 
# Fri, 08 Dec 2023 01:38:25 GMT
CMD ["/bin/sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9acd8b4c9d4385585f74dabb4bc6b3351888710ae37ec5dbd9ea950281b8f9bb`  
		Last Modified: Fri, 08 Dec 2023 01:38:43 GMT  
		Size: 3.2 MB (3244115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7759a4b7aa772576870eb5c52f815fbebd9be11b4781c708dc2ab6007fa609`  
		Last Modified: Wed, 10 Jan 2024 23:58:26 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5ca5419371cb9331b9ba1ea9086eef15ad135bf369ac2787491caf04de682f`  
		Last Modified: Wed, 10 Jan 2024 23:58:26 GMT  
		Size: 109.3 KB (109334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc68a66ccf11c1510081e6e9f70c399ad3ceff564e9b876ed2895ebf29b3ebb`  
		Last Modified: Wed, 10 Jan 2024 23:58:26 GMT  
		Size: 2.8 MB (2830103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b15634bddb0499598a6044cc0030e88ba0ce4cf2b02301cfa0a0faa1ac676cdd`  
		Last Modified: Wed, 10 Jan 2024 23:58:26 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dddc1630ef7eb2545abf068534d7032d19114a744cd485791f63f40ab0b5ab18`  
		Last Modified: Wed, 10 Jan 2024 23:58:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.23-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:15c53491df84b3d051fdcc7dff9dbdb9ca3718254ea873b6e2bbff7bc221abec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.0 KB (97973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fee76928da54f07fd68a5975f71e6f5991ccd3261cf759f3093b424e8f7ba99`

```dockerfile
```

-	Layers:
	-	`sha256:1ae5a47e6fefaee5dc9532fb45757803475b71d80ddf777a416ccd10c45bd09e`  
		Last Modified: Wed, 10 Jan 2024 23:58:26 GMT  
		Size: 78.6 KB (78558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ae992c52298a54654430860ae3828320c41eec63e8702ef1c66f1a68fdb937e`  
		Last Modified: Wed, 10 Jan 2024 23:58:26 GMT  
		Size: 19.4 KB (19415 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.23-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:0639819cf6cbfd6e608ef2071abeb9ca10f049a89ecc83eee11f1d75b78cab2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6394995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12d25d4724561e2ace36bab912780d035fdb57c760fa9268b40e781584c2df0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 08 Dec 2023 01:22:51 GMT
ADD file:052421189f8d269382daaaa8beb63c687e4d8ca908c421abdce53bcc627a40b4 in / 
# Fri, 08 Dec 2023 01:22:51 GMT
CMD ["/bin/sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:243ac51c334a47917a84be93e972ee6378987e9b3b917a5a8df29025e161c1f3`  
		Last Modified: Fri, 08 Dec 2023 01:23:14 GMT  
		Size: 3.4 MB (3358233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add73e7dbebd6c86078686bb046ef57017b090fe917f656feb83ec0ef971b5f3`  
		Last Modified: Tue, 12 Dec 2023 23:20:17 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d64bed657a7e728633e13f2021b35954e98be9ecae77096d30cdaa1d9260d61e`  
		Last Modified: Tue, 12 Dec 2023 23:20:17 GMT  
		Size: 123.4 KB (123403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a69dac8774b0ef6bdf9b84b7360fb3346a88b05e510dbc3366a3a828349a839b`  
		Last Modified: Thu, 11 Jan 2024 00:13:43 GMT  
		Size: 2.9 MB (2911714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666eeed87216ed83fdc1a618d27175e1a8c8efd15354f7e22228e768ded7a7cf`  
		Last Modified: Thu, 11 Jan 2024 00:13:42 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfeab30e174bcb0fc8203612135497885d25cfc588a1e44de9e5b0b5048dcdb`  
		Last Modified: Thu, 11 Jan 2024 00:13:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.23-alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:d20e9002675244162fdaf77d022444958c1a6d56dfe5901853240c568aea24b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 KB (96397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e870214daaeaabaf116e4a0a6462f63bc3d9ce9cd3d522277e53ba1d9c19a54e`

```dockerfile
```

-	Layers:
	-	`sha256:54016ce6ca1c0550269f0db7f3fec4511d81bef96b3c0f41709d785c7cefa5d3`  
		Last Modified: Thu, 11 Jan 2024 00:13:42 GMT  
		Size: 77.0 KB (77025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28bbe767bea18a4ae8896d545c4083a8a7a41145031227bdf28474500598aa2f`  
		Last Modified: Thu, 11 Jan 2024 00:13:42 GMT  
		Size: 19.4 KB (19372 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.23-alpine3.19`

```console
$ docker pull memcached@sha256:72a1f3a3adf62cb2b09914c7ca1bbe69491400b6d95e8bdfea90093a4f0a866b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `memcached:1.6.23-alpine3.19` - linux; amd64

```console
$ docker pull memcached@sha256:32affe08f4a1c6f62faacae1fee90575987d8b995a7257aa35ca1b4a817bdbf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6528299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fba850e40285109fcdc4c5603f2e081dba5bb683ffbcf0d4ad2e954359ce93e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 08 Dec 2023 01:20:49 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Fri, 08 Dec 2023 01:20:49 GMT
CMD ["/bin/sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd74bdcd28e46833593b2724720938c58842faa843fe42ea2411b3afd0739cb6`  
		Last Modified: Wed, 10 Jan 2024 23:58:18 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104a06a5eef3fffb9db79f8f67d4205725b9551aadbad7cb2847b013921bc212`  
		Last Modified: Wed, 10 Jan 2024 23:58:18 GMT  
		Size: 104.2 KB (104204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3271524d49893bc0950a7d058e91621dcfabe2383d6bfc0b13263faaf85f774f`  
		Last Modified: Wed, 10 Jan 2024 23:58:18 GMT  
		Size: 3.0 MB (3013977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb917829c49dd9d022cf427a72685718c30e113cfe036cffdf3eec29523e871`  
		Last Modified: Wed, 10 Jan 2024 23:58:18 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c390a9d8c6874260017223d74f3ae0b04895aa29a26c6ea03e0bd49832fe201`  
		Last Modified: Wed, 10 Jan 2024 23:58:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.23-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:a4db06e4e22e5cb6667aafc4b272349d5db9596147a2114d7b6997ae75e265f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 KB (98074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80b0a8c4800de05bc28d0cf54908bd75ed706e519dc72a22883d057213a1afdd`

```dockerfile
```

-	Layers:
	-	`sha256:9052d3e673c4418bce0a5b5c01961846c1fc2b14ace86d3afae91720a4744b70`  
		Last Modified: Wed, 10 Jan 2024 23:58:18 GMT  
		Size: 78.6 KB (78603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:667e7c7f728f9119016e4a456207d31154a85c080f74151700cc04835b950d54`  
		Last Modified: Wed, 10 Jan 2024 23:58:18 GMT  
		Size: 19.5 KB (19471 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.23-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:5550c34a395e8c02098f113a01d35d794b40c31c374f1e553dc80472d53978c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6372430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f4edcab8bc23e09f91d9a22a6d9df2a2d0175c23ad7cd396eaa4e849528f0e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 08 Dec 2023 01:39:30 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 08 Dec 2023 01:39:30 GMT
CMD ["/bin/sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c303524923177661067f7eb378c3dd5277088c2676ebd1cd78e68397bb80fdbf`  
		Last Modified: Fri, 08 Dec 2023 01:39:48 GMT  
		Size: 3.3 MB (3347794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfede01b081f27465377bdafbbdb6b694c6fab18026972b2c380535dcef103b8`  
		Last Modified: Wed, 13 Dec 2023 01:35:47 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d7b6f4ad45bf3aee58c5a7e8083286bd79dc004840903fd5997929772bfb4c`  
		Last Modified: Wed, 13 Dec 2023 01:35:47 GMT  
		Size: 120.9 KB (120897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f6c7840c606bfa580e1e6b52087faff29fb3986005ea3aadc31c64b3e4142e`  
		Last Modified: Thu, 11 Jan 2024 00:22:58 GMT  
		Size: 2.9 MB (2902089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1335fd4bd25daf4820a1c881f1ea0a30a575682074ad886293a372089bcd4544`  
		Last Modified: Thu, 11 Jan 2024 00:22:58 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48e51e3a0b635d352137fa3c7c3747c8192e7c8de0590e533ffdcea9dc49a96`  
		Last Modified: Thu, 11 Jan 2024 00:22:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.23-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:6faa51abf4ec7649d68a12af15126861e91479130b3f97128d3fa7a487d62422
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.9 KB (97945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e975d798c27c70d9498c44491a9aca9d24cee1fe8111bfae46401e7d9b1264`

```dockerfile
```

-	Layers:
	-	`sha256:0c5c585bb2d781fc112b82e19d343028a3c75758809ef4b46e4a6839bd0a1e41`  
		Last Modified: Thu, 11 Jan 2024 00:22:58 GMT  
		Size: 78.6 KB (78622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed5eb3630ee14af5005edfb5ed56d4660a5bbf224bf729ca0bfabaa0143d9864`  
		Last Modified: Thu, 11 Jan 2024 00:22:58 GMT  
		Size: 19.3 KB (19323 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.23-alpine3.19` - linux; 386

```console
$ docker pull memcached@sha256:67373b38ed96c7ba59d5c1b8ba2b471d75d058ae7056f1e22674128af0e39ece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6185193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ec7484601b2ef9f91318f7c210dbd58716132fdd37be8004e82af4e4d42015b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 08 Dec 2023 01:38:25 GMT
ADD file:bd52540f209ba362654d795d7893669c819d35011a16f9f319301727a33b3bd9 in / 
# Fri, 08 Dec 2023 01:38:25 GMT
CMD ["/bin/sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9acd8b4c9d4385585f74dabb4bc6b3351888710ae37ec5dbd9ea950281b8f9bb`  
		Last Modified: Fri, 08 Dec 2023 01:38:43 GMT  
		Size: 3.2 MB (3244115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7759a4b7aa772576870eb5c52f815fbebd9be11b4781c708dc2ab6007fa609`  
		Last Modified: Wed, 10 Jan 2024 23:58:26 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5ca5419371cb9331b9ba1ea9086eef15ad135bf369ac2787491caf04de682f`  
		Last Modified: Wed, 10 Jan 2024 23:58:26 GMT  
		Size: 109.3 KB (109334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc68a66ccf11c1510081e6e9f70c399ad3ceff564e9b876ed2895ebf29b3ebb`  
		Last Modified: Wed, 10 Jan 2024 23:58:26 GMT  
		Size: 2.8 MB (2830103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b15634bddb0499598a6044cc0030e88ba0ce4cf2b02301cfa0a0faa1ac676cdd`  
		Last Modified: Wed, 10 Jan 2024 23:58:26 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dddc1630ef7eb2545abf068534d7032d19114a744cd485791f63f40ab0b5ab18`  
		Last Modified: Wed, 10 Jan 2024 23:58:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.23-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:15c53491df84b3d051fdcc7dff9dbdb9ca3718254ea873b6e2bbff7bc221abec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.0 KB (97973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fee76928da54f07fd68a5975f71e6f5991ccd3261cf759f3093b424e8f7ba99`

```dockerfile
```

-	Layers:
	-	`sha256:1ae5a47e6fefaee5dc9532fb45757803475b71d80ddf777a416ccd10c45bd09e`  
		Last Modified: Wed, 10 Jan 2024 23:58:26 GMT  
		Size: 78.6 KB (78558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ae992c52298a54654430860ae3828320c41eec63e8702ef1c66f1a68fdb937e`  
		Last Modified: Wed, 10 Jan 2024 23:58:26 GMT  
		Size: 19.4 KB (19415 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.23-alpine3.19` - linux; ppc64le

```console
$ docker pull memcached@sha256:0639819cf6cbfd6e608ef2071abeb9ca10f049a89ecc83eee11f1d75b78cab2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6394995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12d25d4724561e2ace36bab912780d035fdb57c760fa9268b40e781584c2df0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 08 Dec 2023 01:22:51 GMT
ADD file:052421189f8d269382daaaa8beb63c687e4d8ca908c421abdce53bcc627a40b4 in / 
# Fri, 08 Dec 2023 01:22:51 GMT
CMD ["/bin/sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:243ac51c334a47917a84be93e972ee6378987e9b3b917a5a8df29025e161c1f3`  
		Last Modified: Fri, 08 Dec 2023 01:23:14 GMT  
		Size: 3.4 MB (3358233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add73e7dbebd6c86078686bb046ef57017b090fe917f656feb83ec0ef971b5f3`  
		Last Modified: Tue, 12 Dec 2023 23:20:17 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d64bed657a7e728633e13f2021b35954e98be9ecae77096d30cdaa1d9260d61e`  
		Last Modified: Tue, 12 Dec 2023 23:20:17 GMT  
		Size: 123.4 KB (123403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a69dac8774b0ef6bdf9b84b7360fb3346a88b05e510dbc3366a3a828349a839b`  
		Last Modified: Thu, 11 Jan 2024 00:13:43 GMT  
		Size: 2.9 MB (2911714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666eeed87216ed83fdc1a618d27175e1a8c8efd15354f7e22228e768ded7a7cf`  
		Last Modified: Thu, 11 Jan 2024 00:13:42 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfeab30e174bcb0fc8203612135497885d25cfc588a1e44de9e5b0b5048dcdb`  
		Last Modified: Thu, 11 Jan 2024 00:13:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.23-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:d20e9002675244162fdaf77d022444958c1a6d56dfe5901853240c568aea24b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 KB (96397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e870214daaeaabaf116e4a0a6462f63bc3d9ce9cd3d522277e53ba1d9c19a54e`

```dockerfile
```

-	Layers:
	-	`sha256:54016ce6ca1c0550269f0db7f3fec4511d81bef96b3c0f41709d785c7cefa5d3`  
		Last Modified: Thu, 11 Jan 2024 00:13:42 GMT  
		Size: 77.0 KB (77025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28bbe767bea18a4ae8896d545c4083a8a7a41145031227bdf28474500598aa2f`  
		Last Modified: Thu, 11 Jan 2024 00:13:42 GMT  
		Size: 19.4 KB (19372 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:1.6.23-bookworm`

```console
$ docker pull memcached@sha256:49d7bf63abf1842ab67ab13ce42a399f72ffcdec2c6c405020be7371882abea7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
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

### `memcached:1.6.23-bookworm` - linux; amd64

```console
$ docker pull memcached@sha256:643a24a57407d3cb2b8745f47a8d4b20406c19f5399ecb05db9727447637003a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38789237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d474793fb4125ae857b42efbf79eb1cbea8834a20e5d65627ea439b52b57313`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:27 GMT
ADD file:ac3cd70031d35e46d86b876934946ffc8756de4de065fbc926dce642dac07ff3 in / 
# Tue, 19 Dec 2023 01:20:28 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:af107e978371b6cd6339127a05502c5eacd1e6b0e9eb7b2f4aa7b6fc87e2dd81`  
		Last Modified: Tue, 19 Dec 2023 01:24:59 GMT  
		Size: 29.1 MB (29125963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d32ccca352404a5a8dedb6a7ca281abbc073b9d8643ef4626873ee1b8a204b1`  
		Last Modified: Wed, 10 Jan 2024 23:58:24 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d585b71055b9f919875cf91a81370309c971aad943e53b8c9fda2b63521f873`  
		Last Modified: Wed, 10 Jan 2024 23:58:25 GMT  
		Size: 2.5 MB (2488298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc47ad75df3e3af04459ae59b5c7ec1ea8dd657b7fb4cc42ec85a982a98da628`  
		Last Modified: Wed, 10 Jan 2024 23:58:25 GMT  
		Size: 7.2 MB (7173458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66204efbd683596758bec893cba01fce3fe386da63399af101051d8df26c2477`  
		Last Modified: Wed, 10 Jan 2024 23:58:25 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3406bc9285b7e906c211fd9a5d9342ee80d9e0ae728a6529d14db42aecf145`  
		Last Modified: Wed, 10 Jan 2024 23:58:25 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.23-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:8efa487487fc160476637a4fb2aec45b4a38eb677aeddcd0ecaeab362e136e85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3077977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:928c59acdba2c812e1299dcb8c4a4c7a7bdfadbc695533aab940957913a8b768`

```dockerfile
```

-	Layers:
	-	`sha256:7777c14054a0e9893c312cf26a23d80bb2f16d3cd6dacad21c21c8fb1be321a4`  
		Last Modified: Wed, 10 Jan 2024 23:58:25 GMT  
		Size: 3.1 MB (3056860 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc8d2dbb4d2d164636bb06f04252d4aec50002cf7469a8955e322e104563d025`  
		Last Modified: Wed, 10 Jan 2024 23:58:24 GMT  
		Size: 21.1 KB (21117 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.23-bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:d01aca5f5e26f687d6ad14ec6547e704f453acc02ce0ce2e5fa5871f5013bfbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34811390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f12a90da675230d99a32d19f573412751d7740cae5f90d74a8c49b4b6f64a3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 19 Dec 2023 01:55:22 GMT
ADD file:9503ab966c9dd707eeccc7c2f633bccc94c199f8714ec4ff2c8b54dde3dbabf9 in / 
# Tue, 19 Dec 2023 01:55:22 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1ae9a2844c8c70942d2220553689b62e841cc706d77284fbfedbd770080fd699`  
		Last Modified: Tue, 19 Dec 2023 01:58:33 GMT  
		Size: 26.9 MB (26885440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ab650f4c7d61856342d3b0e4d9bad9cd0c4336fb403dab9c5c1ed2c285774f`  
		Last Modified: Thu, 11 Jan 2024 00:07:53 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b10807a0745d6e1ccc36157b11a3469a17c6477eda65233bb2f182c7958db5b8`  
		Last Modified: Thu, 11 Jan 2024 00:07:54 GMT  
		Size: 2.1 MB (2089356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5bc9bbfb0a70ce84a09ce58d70ebf97841c03e06d3968f065cd9361bd0e990`  
		Last Modified: Thu, 11 Jan 2024 00:07:54 GMT  
		Size: 5.8 MB (5835079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74b3373a0a7639196238720db6061026ccfe87c48ccf38fcfbc737699c9f2b7`  
		Last Modified: Thu, 11 Jan 2024 00:07:53 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3969d1f7528c0ba1d0047402bf5611d53c8f502f52fbbd7fb827f8de5ab813f6`  
		Last Modified: Thu, 11 Jan 2024 00:07:54 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.23-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:7484a951008b8e170922f1467a179c839a675cf4ab9555315f6bb20174be8173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3052683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d85ee8bbb3867fa9cbdd5e06e5791b62e1c7dfc410295ba05b95ead8b6c4525`

```dockerfile
```

-	Layers:
	-	`sha256:34e791a9d4149137cb6b8da59558d4bf4ce80c9bcd5ab599785c7a3aaa2fc844`  
		Last Modified: Thu, 11 Jan 2024 00:07:54 GMT  
		Size: 3.0 MB (3031592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31263ce608cc2e18001c08b34ad8f21b27befcf21ee30dd42bd87176f24a5e10`  
		Last Modified: Thu, 11 Jan 2024 00:07:53 GMT  
		Size: 21.1 KB (21091 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.23-bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:1b119620b1cbaac4281975bedfed15ff721d868ec9eda9574dc4c1ec58330716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37686962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45b76a80b62f56ff1c68ed4e7ce2dfe225b3560e00750a3210c8d897b1547f3a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:11 GMT
ADD file:262fd7bf0bc26e5d2a229fba52626e22b8a93beac29733acfc60e716c26e689d in / 
# Tue, 19 Dec 2023 01:41:11 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:24e221e92a36ab5b0075dd156b4f2ff095532a9b0927946cf6070bb1bea208b8`  
		Last Modified: Tue, 19 Dec 2023 01:44:38 GMT  
		Size: 29.2 MB (29157269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d79fe3da079136cc418087e5d4e432357c062519668a3c03b78c24710c3a6ec`  
		Last Modified: Wed, 20 Dec 2023 10:20:11 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:496388416e6f8cdbf05e6ea4a56e906308e4b95b9f984f73b5c5a3fdbe5b12aa`  
		Last Modified: Wed, 20 Dec 2023 10:20:11 GMT  
		Size: 2.3 MB (2346023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee91bf234e7544eb6ad4c5f18ba87a8c0306d87f51ee1c47b1361569175a8a7c`  
		Last Modified: Thu, 11 Jan 2024 00:20:26 GMT  
		Size: 6.2 MB (6182151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73888be7ca392dfe14270a838c67a2d7ccfe9354f1fe52147291c9756127b51`  
		Last Modified: Thu, 11 Jan 2024 00:20:25 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a917a1ebe539f36501d4bebb89957491c647a119a1702734b1a0c9c01dc2a6`  
		Last Modified: Thu, 11 Jan 2024 00:20:25 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.23-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:f96d1dde1233068de191226772289ac63a784a466d34ec1dbf67e72559643f7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3053019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f249bf848fae6f5b573dffd3d8dbd830fd3267c6f487d397fd82ba104fee46b`

```dockerfile
```

-	Layers:
	-	`sha256:09c490b7c5d08149f654887eca9ca058a49a3b659d3e7282589a431883445a49`  
		Last Modified: Thu, 11 Jan 2024 00:20:25 GMT  
		Size: 3.0 MB (3032051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abe3c6e55476a176987bc5b5f8bad00ca16d1299d36e40f52e82dcb76ed0600c`  
		Last Modified: Thu, 11 Jan 2024 00:20:25 GMT  
		Size: 21.0 KB (20968 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.23-bookworm` - linux; 386

```console
$ docker pull memcached@sha256:a5d93bfce917e364c0f16cdad7b683a36011a997db4be6db2770644095aea01d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39272936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:902b98d31b0a747e1d90226bbd3f7fb16592c8f606009585e9b2bbb819bfb30e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 19 Dec 2023 01:39:07 GMT
ADD file:6f4083d57ea9644b5a827e67b0725087a15aa428272ec223ab968bf8b4623e42 in / 
# Tue, 19 Dec 2023 01:39:07 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8d4aad22fb6a12b8cc7a78d338dfb9bc2bd6d621517b374e446f2915833ea883`  
		Last Modified: Tue, 19 Dec 2023 01:43:45 GMT  
		Size: 30.1 MB (30143863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22ddf2b3cd1581c8f1483d20c8fb232852e525fea04a97ffd9ac744939dffc0`  
		Last Modified: Wed, 10 Jan 2024 23:58:29 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23537023da95e2b44ae9e7aebee71e05ecb397f02a351f30f6c69a752d98d1a5`  
		Last Modified: Wed, 10 Jan 2024 23:58:29 GMT  
		Size: 2.5 MB (2492560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8636f3d8b77edac77347698b78afe5ce4f443daa01f0a424d809c8ed35405ac5`  
		Last Modified: Wed, 10 Jan 2024 23:58:29 GMT  
		Size: 6.6 MB (6634994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41afb4f2ebc199845ca27aae99895e43658c24f7fbdea6a0b17769f1fd238b3f`  
		Last Modified: Wed, 10 Jan 2024 23:58:29 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aee346987d8e42b5a7c3ecdc4b2efa5e402c43f65712c94e3f30606c9b365e4`  
		Last Modified: Wed, 10 Jan 2024 23:58:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.23-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:71cbd1b0df460e30d13a768ed26659ea3d35001b788219b4eac0d77078e71ab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3072225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7173243e71de72bb179738a15514dee35cfb9c1f1ab3da05adc2fd1ea74335cf`

```dockerfile
```

-	Layers:
	-	`sha256:4e2e18fc597957c9c8202a8015176e35b070a14ec422ca3b88fdfaa64cd693d0`  
		Last Modified: Wed, 10 Jan 2024 23:58:29 GMT  
		Size: 3.1 MB (3051163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1dc46fbcfd7dddfe981ea410938185ededc5f8f383164b2ffe266c923d1e7ed`  
		Last Modified: Wed, 10 Jan 2024 23:58:29 GMT  
		Size: 21.1 KB (21062 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.23-bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:d6b10482cd93239feb732ab9b3bcdd207e5be672b55c01b1faa72c6e10da9ee3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37564394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bed0ab2d751422f3dfcd94712006ab27d4cdd43e18f83b8b38199c2cee3b2514`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 19 Dec 2023 02:13:36 GMT
ADD file:dcd5696ac281b24df52a518e2402c7f7a4caedfcba0d82e195b7c06cd3a38fdd in / 
# Tue, 19 Dec 2023 02:13:40 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:12b1322ffb17b8e81ca1c6d9d7118e2fcee0b9d971aa3c90601e6345804a60d1`  
		Last Modified: Tue, 19 Dec 2023 02:24:36 GMT  
		Size: 29.1 MB (29121427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6b93f134841b66512a1d4138bdf28b0506ffd27490aac735508b3f20716618`  
		Last Modified: Thu, 11 Jan 2024 00:10:54 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573e69b5f2977543c86d4410256c381ef97d7f37a89be2a88bfbda683c24110e`  
		Last Modified: Thu, 11 Jan 2024 00:10:55 GMT  
		Size: 1.9 MB (1937514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb552cccf8bd4122265e6895c4c9ce039b90dd08574f0e4911a0b11aaf1f7b2c`  
		Last Modified: Thu, 11 Jan 2024 00:10:55 GMT  
		Size: 6.5 MB (6503938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b640b85282363650ba7d87fea47ce2e4cfe96da07ab6c4b47eebc739f96910`  
		Last Modified: Thu, 11 Jan 2024 00:10:54 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933eef8a1d4865a3e302557839a52d00229ef80652113710df9fd606880475c5`  
		Last Modified: Thu, 11 Jan 2024 00:10:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.23-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:c1162ead1e62fcd87632e902387935d8f33b794c009815419baf8cb396548f85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aa26ec0ff6dd44911a88c2d2af479e0c05cfb46e9db65187abe71da51f56001`

```dockerfile
```

-	Layers:
	-	`sha256:2454765cb79a60d22f96ec7e66ea9fb222b40c30758e0df9a59c7192c39847da`  
		Last Modified: Thu, 11 Jan 2024 00:10:54 GMT  
		Size: 20.8 KB (20837 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1.6.23-bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:b7976b1191a4f34442e257f55f30f8b4efd28f5f8026936846e8a5471e0c8505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.0 MB (43007490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75346431bfc757a49f790022140e267e0e6838110c75cad2bf8ab9e24e2855fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 19 Dec 2023 01:21:50 GMT
ADD file:ca1db68689e0b0388337ba450ad2c8e79c159c6b78f5aa6d3ff2b89b8d7edc93 in / 
# Tue, 19 Dec 2023 01:21:51 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fc9b8f5eec3aa37ab3aace05165427479352f290d53904cea87dca6349633a09`  
		Last Modified: Tue, 19 Dec 2023 01:26:19 GMT  
		Size: 33.1 MB (33120558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f85ae146a90d1ce7561d4e67d1ce2eaf0a0da444bb8a70c5b7fc94d0dc75e389`  
		Last Modified: Wed, 20 Dec 2023 08:43:43 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23065e9a12cf130c31375986a9b4700b84f2539ccb4b47efe0f375f77938fc3`  
		Last Modified: Wed, 20 Dec 2023 08:43:44 GMT  
		Size: 2.7 MB (2698240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b8249b30995d06e02d41e31406a930c02163d057cd39ad2cb7f710df2f6c60`  
		Last Modified: Thu, 11 Jan 2024 00:10:31 GMT  
		Size: 7.2 MB (7187176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a238b8549095cec1619f8f38f82d1aeb50acdf094b2b611b1fb5c62da14635f`  
		Last Modified: Thu, 11 Jan 2024 00:10:31 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669f29d97099310deca355ff837c9885adea00bb9c6e460490904627b7a40e4b`  
		Last Modified: Thu, 11 Jan 2024 00:10:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1.6.23-bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:87bde9e8cd8d07c6306a9ef516b822eadb9669d79da8587f1ac892066646ad33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3066464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:034c7634fd9e3419a42aa94fb6c3c05bd8d951eaf75eef2fbd2e8d64150013ba`

```dockerfile
```

-	Layers:
	-	`sha256:0a90f178efc50a3500b5ee2dce72b560153f2b0ec4cc6e79aa940561e8d58590`  
		Last Modified: Thu, 11 Jan 2024 00:10:31 GMT  
		Size: 3.0 MB (3045446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35a907ae4a36d514f4ff1b8d97766c9a5166c6116bc026f627e4de4cc51111fe`  
		Last Modified: Thu, 11 Jan 2024 00:10:30 GMT  
		Size: 21.0 KB (21018 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine`

```console
$ docker pull memcached@sha256:df6a80f20b17df1f452b325ba2bee57644473669cb08fc928d55417da18cb786
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 11
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
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
$ docker pull memcached@sha256:32affe08f4a1c6f62faacae1fee90575987d8b995a7257aa35ca1b4a817bdbf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6528299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fba850e40285109fcdc4c5603f2e081dba5bb683ffbcf0d4ad2e954359ce93e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 08 Dec 2023 01:20:49 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Fri, 08 Dec 2023 01:20:49 GMT
CMD ["/bin/sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd74bdcd28e46833593b2724720938c58842faa843fe42ea2411b3afd0739cb6`  
		Last Modified: Wed, 10 Jan 2024 23:58:18 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104a06a5eef3fffb9db79f8f67d4205725b9551aadbad7cb2847b013921bc212`  
		Last Modified: Wed, 10 Jan 2024 23:58:18 GMT  
		Size: 104.2 KB (104204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3271524d49893bc0950a7d058e91621dcfabe2383d6bfc0b13263faaf85f774f`  
		Last Modified: Wed, 10 Jan 2024 23:58:18 GMT  
		Size: 3.0 MB (3013977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb917829c49dd9d022cf427a72685718c30e113cfe036cffdf3eec29523e871`  
		Last Modified: Wed, 10 Jan 2024 23:58:18 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c390a9d8c6874260017223d74f3ae0b04895aa29a26c6ea03e0bd49832fe201`  
		Last Modified: Wed, 10 Jan 2024 23:58:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:a4db06e4e22e5cb6667aafc4b272349d5db9596147a2114d7b6997ae75e265f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 KB (98074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80b0a8c4800de05bc28d0cf54908bd75ed706e519dc72a22883d057213a1afdd`

```dockerfile
```

-	Layers:
	-	`sha256:9052d3e673c4418bce0a5b5c01961846c1fc2b14ace86d3afae91720a4744b70`  
		Last Modified: Wed, 10 Jan 2024 23:58:18 GMT  
		Size: 78.6 KB (78603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:667e7c7f728f9119016e4a456207d31154a85c080f74151700cc04835b950d54`  
		Last Modified: Wed, 10 Jan 2024 23:58:18 GMT  
		Size: 19.5 KB (19471 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; arm variant v7

```console
$ docker pull memcached@sha256:79a5646a0c845a791f36017fda3292281b48295b06c53f13d62c9f94237d4731
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3960292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2afac0e49af3ce3f1769abe11a29f8f5610c6a736d8c5b6c7b9770c8d8e94e91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 16 Dec 2020 23:58:14 GMT
ADD file:bd07f77a2b2741ca6bda80d9203be9c7274cf73145bff778cf000db0d8d4e903 in / 
# Wed, 16 Dec 2020 23:58:15 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 06:43:29 GMT
RUN addgroup -g 11211 memcache && adduser -D -u 11211 -G memcache memcache
# Thu, 17 Dec 2020 06:43:31 GMT
RUN apk add --no-cache cyrus-sasl-plain
# Thu, 17 Dec 2020 06:43:33 GMT
ENV MEMCACHED_VERSION=1.6.9
# Thu, 17 Dec 2020 06:43:35 GMT
ENV MEMCACHED_SHA1=42ae062094fdf083cfe7b21ff377c781011c2be1
# Thu, 17 Dec 2020 06:46:32 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 		tar 		wget 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& make test PARALLEL="$nproc" 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --no-network --virtual .memcached-rundeps $runDeps 	&& apk del --no-network .build-deps 		&& memcached -V
# Thu, 17 Dec 2020 06:46:33 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 17 Dec 2020 06:46:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 17 Dec 2020 06:46:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 06:46:36 GMT
USER memcache
# Thu, 17 Dec 2020 06:46:38 GMT
EXPOSE 11211
# Thu, 17 Dec 2020 06:46:39 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c58e8a26a8407acc3ead776f6526efa889fda03270a8d05109208d9f59159420`  
		Last Modified: Wed, 16 Dec 2020 23:58:59 GMT  
		Size: 2.4 MB (2407555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68564bbfc09f153688e942bf54d5375d1e27f3507c0bed6b038c2ac8ce095aa5`  
		Last Modified: Thu, 17 Dec 2020 06:46:58 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cac3a91edee49d0b08a25706ae86059bed89941a08b496e72ef092e57c4ecb3`  
		Last Modified: Thu, 17 Dec 2020 06:46:58 GMT  
		Size: 13.8 KB (13825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf16e9bb942ec42a35a792beab65aea843209e7bdde7e856499b9fc85f93bc4e`  
		Last Modified: Thu, 17 Dec 2020 06:46:58 GMT  
		Size: 1.5 MB (1537248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc15394239bd0c083e1b6df806aa5ffeb8b9cc7e80113afc2959721de49f90d1`  
		Last Modified: Thu, 17 Dec 2020 06:46:58 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:482f0eb571548eae5720c652ff7da13558e56a8722dc9932cf7eb1ef3eb33acb`  
		Last Modified: Thu, 17 Dec 2020 06:46:58 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:5550c34a395e8c02098f113a01d35d794b40c31c374f1e553dc80472d53978c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6372430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f4edcab8bc23e09f91d9a22a6d9df2a2d0175c23ad7cd396eaa4e849528f0e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 08 Dec 2023 01:39:30 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 08 Dec 2023 01:39:30 GMT
CMD ["/bin/sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c303524923177661067f7eb378c3dd5277088c2676ebd1cd78e68397bb80fdbf`  
		Last Modified: Fri, 08 Dec 2023 01:39:48 GMT  
		Size: 3.3 MB (3347794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfede01b081f27465377bdafbbdb6b694c6fab18026972b2c380535dcef103b8`  
		Last Modified: Wed, 13 Dec 2023 01:35:47 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d7b6f4ad45bf3aee58c5a7e8083286bd79dc004840903fd5997929772bfb4c`  
		Last Modified: Wed, 13 Dec 2023 01:35:47 GMT  
		Size: 120.9 KB (120897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f6c7840c606bfa580e1e6b52087faff29fb3986005ea3aadc31c64b3e4142e`  
		Last Modified: Thu, 11 Jan 2024 00:22:58 GMT  
		Size: 2.9 MB (2902089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1335fd4bd25daf4820a1c881f1ea0a30a575682074ad886293a372089bcd4544`  
		Last Modified: Thu, 11 Jan 2024 00:22:58 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48e51e3a0b635d352137fa3c7c3747c8192e7c8de0590e533ffdcea9dc49a96`  
		Last Modified: Thu, 11 Jan 2024 00:22:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:6faa51abf4ec7649d68a12af15126861e91479130b3f97128d3fa7a487d62422
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.9 KB (97945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e975d798c27c70d9498c44491a9aca9d24cee1fe8111bfae46401e7d9b1264`

```dockerfile
```

-	Layers:
	-	`sha256:0c5c585bb2d781fc112b82e19d343028a3c75758809ef4b46e4a6839bd0a1e41`  
		Last Modified: Thu, 11 Jan 2024 00:22:58 GMT  
		Size: 78.6 KB (78622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed5eb3630ee14af5005edfb5ed56d4660a5bbf224bf729ca0bfabaa0143d9864`  
		Last Modified: Thu, 11 Jan 2024 00:22:58 GMT  
		Size: 19.3 KB (19323 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; 386

```console
$ docker pull memcached@sha256:67373b38ed96c7ba59d5c1b8ba2b471d75d058ae7056f1e22674128af0e39ece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6185193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ec7484601b2ef9f91318f7c210dbd58716132fdd37be8004e82af4e4d42015b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 08 Dec 2023 01:38:25 GMT
ADD file:bd52540f209ba362654d795d7893669c819d35011a16f9f319301727a33b3bd9 in / 
# Fri, 08 Dec 2023 01:38:25 GMT
CMD ["/bin/sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9acd8b4c9d4385585f74dabb4bc6b3351888710ae37ec5dbd9ea950281b8f9bb`  
		Last Modified: Fri, 08 Dec 2023 01:38:43 GMT  
		Size: 3.2 MB (3244115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7759a4b7aa772576870eb5c52f815fbebd9be11b4781c708dc2ab6007fa609`  
		Last Modified: Wed, 10 Jan 2024 23:58:26 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5ca5419371cb9331b9ba1ea9086eef15ad135bf369ac2787491caf04de682f`  
		Last Modified: Wed, 10 Jan 2024 23:58:26 GMT  
		Size: 109.3 KB (109334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc68a66ccf11c1510081e6e9f70c399ad3ceff564e9b876ed2895ebf29b3ebb`  
		Last Modified: Wed, 10 Jan 2024 23:58:26 GMT  
		Size: 2.8 MB (2830103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b15634bddb0499598a6044cc0030e88ba0ce4cf2b02301cfa0a0faa1ac676cdd`  
		Last Modified: Wed, 10 Jan 2024 23:58:26 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dddc1630ef7eb2545abf068534d7032d19114a744cd485791f63f40ab0b5ab18`  
		Last Modified: Wed, 10 Jan 2024 23:58:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:15c53491df84b3d051fdcc7dff9dbdb9ca3718254ea873b6e2bbff7bc221abec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.0 KB (97973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fee76928da54f07fd68a5975f71e6f5991ccd3261cf759f3093b424e8f7ba99`

```dockerfile
```

-	Layers:
	-	`sha256:1ae5a47e6fefaee5dc9532fb45757803475b71d80ddf777a416ccd10c45bd09e`  
		Last Modified: Wed, 10 Jan 2024 23:58:26 GMT  
		Size: 78.6 KB (78558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ae992c52298a54654430860ae3828320c41eec63e8702ef1c66f1a68fdb937e`  
		Last Modified: Wed, 10 Jan 2024 23:58:26 GMT  
		Size: 19.4 KB (19415 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:0639819cf6cbfd6e608ef2071abeb9ca10f049a89ecc83eee11f1d75b78cab2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6394995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12d25d4724561e2ace36bab912780d035fdb57c760fa9268b40e781584c2df0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 08 Dec 2023 01:22:51 GMT
ADD file:052421189f8d269382daaaa8beb63c687e4d8ca908c421abdce53bcc627a40b4 in / 
# Fri, 08 Dec 2023 01:22:51 GMT
CMD ["/bin/sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:243ac51c334a47917a84be93e972ee6378987e9b3b917a5a8df29025e161c1f3`  
		Last Modified: Fri, 08 Dec 2023 01:23:14 GMT  
		Size: 3.4 MB (3358233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add73e7dbebd6c86078686bb046ef57017b090fe917f656feb83ec0ef971b5f3`  
		Last Modified: Tue, 12 Dec 2023 23:20:17 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d64bed657a7e728633e13f2021b35954e98be9ecae77096d30cdaa1d9260d61e`  
		Last Modified: Tue, 12 Dec 2023 23:20:17 GMT  
		Size: 123.4 KB (123403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a69dac8774b0ef6bdf9b84b7360fb3346a88b05e510dbc3366a3a828349a839b`  
		Last Modified: Thu, 11 Jan 2024 00:13:43 GMT  
		Size: 2.9 MB (2911714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666eeed87216ed83fdc1a618d27175e1a8c8efd15354f7e22228e768ded7a7cf`  
		Last Modified: Thu, 11 Jan 2024 00:13:42 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfeab30e174bcb0fc8203612135497885d25cfc588a1e44de9e5b0b5048dcdb`  
		Last Modified: Thu, 11 Jan 2024 00:13:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:d20e9002675244162fdaf77d022444958c1a6d56dfe5901853240c568aea24b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 KB (96397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e870214daaeaabaf116e4a0a6462f63bc3d9ce9cd3d522277e53ba1d9c19a54e`

```dockerfile
```

-	Layers:
	-	`sha256:54016ce6ca1c0550269f0db7f3fec4511d81bef96b3c0f41709d785c7cefa5d3`  
		Last Modified: Thu, 11 Jan 2024 00:13:42 GMT  
		Size: 77.0 KB (77025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28bbe767bea18a4ae8896d545c4083a8a7a41145031227bdf28474500598aa2f`  
		Last Modified: Thu, 11 Jan 2024 00:13:42 GMT  
		Size: 19.4 KB (19372 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine` - linux; s390x

```console
$ docker pull memcached@sha256:53d0bdb491815057b9014ab30e95c68146d83accdc9d8d690e308e67e7f4eed5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4326665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b078f3aede6257187e9488318eac328332ace90ac171c8a99d0ca495e1e9ad40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 08 Dec 2023 01:41:50 GMT
ADD file:47e0982fc3ae485c06d46f3c0022afd39ed7ec95fe755c2391e6b0cfcae65dfc in / 
# Fri, 08 Dec 2023 01:41:51 GMT
CMD ["/bin/sh"]
# Sat, 09 Dec 2023 01:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 09 Dec 2023 01:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 09 Dec 2023 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.22
# Sat, 09 Dec 2023 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.22.tar.gz
# Sat, 09 Dec 2023 01:54:10 GMT
ENV MEMCACHED_SHA1=7a691f390d59616dbebfc9e2e4942d499c39a338
# Sat, 09 Dec 2023 01:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 09 Dec 2023 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 09 Dec 2023 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 09 Dec 2023 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 09 Dec 2023 01:54:10 GMT
USER memcache
# Sat, 09 Dec 2023 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 09 Dec 2023 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0fca3ee44ced87b7184bc23390283fdf10cfae0e844a25b785dd11c463815227`  
		Last Modified: Fri, 08 Dec 2023 01:42:30 GMT  
		Size: 3.2 MB (3242332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff601679be7ba19260a77b326cf587dcc37315b02c2e0b0effc7084da4684bd7`  
		Last Modified: Wed, 13 Dec 2023 00:39:43 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b2401b35befb0832d96cebfdee6215736b27c0e3d064d67da9917deca4c14c`  
		Last Modified: Wed, 13 Dec 2023 00:39:43 GMT  
		Size: 113.1 KB (113142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59b1e1447b7739e5338731014a96bea369258cbf54b2d152ef50bb06e308bad`  
		Last Modified: Wed, 13 Dec 2023 00:39:43 GMT  
		Size: 969.5 KB (969547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c62bb151b09d73f2bc083bb91abedfb6660c5045d34f7d576415190ae4e09f`  
		Last Modified: Wed, 13 Dec 2023 00:39:43 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaaf7e6dbf7fbf661d0b3f6f5d38fbd888ab6707a76919a5f4a633194e895a2f`  
		Last Modified: Wed, 13 Dec 2023 00:39:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine` - unknown; unknown

```console
$ docker pull memcached@sha256:1c2ba4c72ac494072ca8249e1368c9974cec5e63ff363b9da79930b7a8fbb5cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.3 KB (96269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c33c986fa5bcf287e1c7594cc4bc4b13289d51ef15c3db591e513fcb7b653ce`

```dockerfile
```

-	Layers:
	-	`sha256:358b294b5bd4c90ab3ded38657baddb4cf8a5d594c5ea9c5683191efc2c70e05`  
		Last Modified: Wed, 13 Dec 2023 00:39:43 GMT  
		Size: 77.0 KB (76967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:708c671c1199a85cfb58a91ad4f1c34c29d381f2905468f64a42c8fbb6341e30`  
		Last Modified: Wed, 13 Dec 2023 00:39:43 GMT  
		Size: 19.3 KB (19302 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:alpine3.19`

```console
$ docker pull memcached@sha256:72f79c540a7204a0355f57a8e3080831c646db96684c69b6a47d36f70fc33cae
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
$ docker pull memcached@sha256:32affe08f4a1c6f62faacae1fee90575987d8b995a7257aa35ca1b4a817bdbf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6528299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fba850e40285109fcdc4c5603f2e081dba5bb683ffbcf0d4ad2e954359ce93e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 08 Dec 2023 01:20:49 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Fri, 08 Dec 2023 01:20:49 GMT
CMD ["/bin/sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd74bdcd28e46833593b2724720938c58842faa843fe42ea2411b3afd0739cb6`  
		Last Modified: Wed, 10 Jan 2024 23:58:18 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104a06a5eef3fffb9db79f8f67d4205725b9551aadbad7cb2847b013921bc212`  
		Last Modified: Wed, 10 Jan 2024 23:58:18 GMT  
		Size: 104.2 KB (104204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3271524d49893bc0950a7d058e91621dcfabe2383d6bfc0b13263faaf85f774f`  
		Last Modified: Wed, 10 Jan 2024 23:58:18 GMT  
		Size: 3.0 MB (3013977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb917829c49dd9d022cf427a72685718c30e113cfe036cffdf3eec29523e871`  
		Last Modified: Wed, 10 Jan 2024 23:58:18 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c390a9d8c6874260017223d74f3ae0b04895aa29a26c6ea03e0bd49832fe201`  
		Last Modified: Wed, 10 Jan 2024 23:58:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:a4db06e4e22e5cb6667aafc4b272349d5db9596147a2114d7b6997ae75e265f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 KB (98074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80b0a8c4800de05bc28d0cf54908bd75ed706e519dc72a22883d057213a1afdd`

```dockerfile
```

-	Layers:
	-	`sha256:9052d3e673c4418bce0a5b5c01961846c1fc2b14ace86d3afae91720a4744b70`  
		Last Modified: Wed, 10 Jan 2024 23:58:18 GMT  
		Size: 78.6 KB (78603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:667e7c7f728f9119016e4a456207d31154a85c080f74151700cc04835b950d54`  
		Last Modified: Wed, 10 Jan 2024 23:58:18 GMT  
		Size: 19.5 KB (19471 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.19` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:5550c34a395e8c02098f113a01d35d794b40c31c374f1e553dc80472d53978c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6372430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f4edcab8bc23e09f91d9a22a6d9df2a2d0175c23ad7cd396eaa4e849528f0e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 08 Dec 2023 01:39:30 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 08 Dec 2023 01:39:30 GMT
CMD ["/bin/sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:c303524923177661067f7eb378c3dd5277088c2676ebd1cd78e68397bb80fdbf`  
		Last Modified: Fri, 08 Dec 2023 01:39:48 GMT  
		Size: 3.3 MB (3347794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfede01b081f27465377bdafbbdb6b694c6fab18026972b2c380535dcef103b8`  
		Last Modified: Wed, 13 Dec 2023 01:35:47 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d7b6f4ad45bf3aee58c5a7e8083286bd79dc004840903fd5997929772bfb4c`  
		Last Modified: Wed, 13 Dec 2023 01:35:47 GMT  
		Size: 120.9 KB (120897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f6c7840c606bfa580e1e6b52087faff29fb3986005ea3aadc31c64b3e4142e`  
		Last Modified: Thu, 11 Jan 2024 00:22:58 GMT  
		Size: 2.9 MB (2902089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1335fd4bd25daf4820a1c881f1ea0a30a575682074ad886293a372089bcd4544`  
		Last Modified: Thu, 11 Jan 2024 00:22:58 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48e51e3a0b635d352137fa3c7c3747c8192e7c8de0590e533ffdcea9dc49a96`  
		Last Modified: Thu, 11 Jan 2024 00:22:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:6faa51abf4ec7649d68a12af15126861e91479130b3f97128d3fa7a487d62422
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.9 KB (97945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e975d798c27c70d9498c44491a9aca9d24cee1fe8111bfae46401e7d9b1264`

```dockerfile
```

-	Layers:
	-	`sha256:0c5c585bb2d781fc112b82e19d343028a3c75758809ef4b46e4a6839bd0a1e41`  
		Last Modified: Thu, 11 Jan 2024 00:22:58 GMT  
		Size: 78.6 KB (78622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed5eb3630ee14af5005edfb5ed56d4660a5bbf224bf729ca0bfabaa0143d9864`  
		Last Modified: Thu, 11 Jan 2024 00:22:58 GMT  
		Size: 19.3 KB (19323 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.19` - linux; 386

```console
$ docker pull memcached@sha256:67373b38ed96c7ba59d5c1b8ba2b471d75d058ae7056f1e22674128af0e39ece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6185193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ec7484601b2ef9f91318f7c210dbd58716132fdd37be8004e82af4e4d42015b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 08 Dec 2023 01:38:25 GMT
ADD file:bd52540f209ba362654d795d7893669c819d35011a16f9f319301727a33b3bd9 in / 
# Fri, 08 Dec 2023 01:38:25 GMT
CMD ["/bin/sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9acd8b4c9d4385585f74dabb4bc6b3351888710ae37ec5dbd9ea950281b8f9bb`  
		Last Modified: Fri, 08 Dec 2023 01:38:43 GMT  
		Size: 3.2 MB (3244115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7759a4b7aa772576870eb5c52f815fbebd9be11b4781c708dc2ab6007fa609`  
		Last Modified: Wed, 10 Jan 2024 23:58:26 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5ca5419371cb9331b9ba1ea9086eef15ad135bf369ac2787491caf04de682f`  
		Last Modified: Wed, 10 Jan 2024 23:58:26 GMT  
		Size: 109.3 KB (109334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc68a66ccf11c1510081e6e9f70c399ad3ceff564e9b876ed2895ebf29b3ebb`  
		Last Modified: Wed, 10 Jan 2024 23:58:26 GMT  
		Size: 2.8 MB (2830103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b15634bddb0499598a6044cc0030e88ba0ce4cf2b02301cfa0a0faa1ac676cdd`  
		Last Modified: Wed, 10 Jan 2024 23:58:26 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dddc1630ef7eb2545abf068534d7032d19114a744cd485791f63f40ab0b5ab18`  
		Last Modified: Wed, 10 Jan 2024 23:58:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:15c53491df84b3d051fdcc7dff9dbdb9ca3718254ea873b6e2bbff7bc221abec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.0 KB (97973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fee76928da54f07fd68a5975f71e6f5991ccd3261cf759f3093b424e8f7ba99`

```dockerfile
```

-	Layers:
	-	`sha256:1ae5a47e6fefaee5dc9532fb45757803475b71d80ddf777a416ccd10c45bd09e`  
		Last Modified: Wed, 10 Jan 2024 23:58:26 GMT  
		Size: 78.6 KB (78558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ae992c52298a54654430860ae3828320c41eec63e8702ef1c66f1a68fdb937e`  
		Last Modified: Wed, 10 Jan 2024 23:58:26 GMT  
		Size: 19.4 KB (19415 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.19` - linux; ppc64le

```console
$ docker pull memcached@sha256:0639819cf6cbfd6e608ef2071abeb9ca10f049a89ecc83eee11f1d75b78cab2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6394995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12d25d4724561e2ace36bab912780d035fdb57c760fa9268b40e781584c2df0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 08 Dec 2023 01:22:51 GMT
ADD file:052421189f8d269382daaaa8beb63c687e4d8ca908c421abdce53bcc627a40b4 in / 
# Fri, 08 Dec 2023 01:22:51 GMT
CMD ["/bin/sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:243ac51c334a47917a84be93e972ee6378987e9b3b917a5a8df29025e161c1f3`  
		Last Modified: Fri, 08 Dec 2023 01:23:14 GMT  
		Size: 3.4 MB (3358233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add73e7dbebd6c86078686bb046ef57017b090fe917f656feb83ec0ef971b5f3`  
		Last Modified: Tue, 12 Dec 2023 23:20:17 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d64bed657a7e728633e13f2021b35954e98be9ecae77096d30cdaa1d9260d61e`  
		Last Modified: Tue, 12 Dec 2023 23:20:17 GMT  
		Size: 123.4 KB (123403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a69dac8774b0ef6bdf9b84b7360fb3346a88b05e510dbc3366a3a828349a839b`  
		Last Modified: Thu, 11 Jan 2024 00:13:43 GMT  
		Size: 2.9 MB (2911714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666eeed87216ed83fdc1a618d27175e1a8c8efd15354f7e22228e768ded7a7cf`  
		Last Modified: Thu, 11 Jan 2024 00:13:42 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfeab30e174bcb0fc8203612135497885d25cfc588a1e44de9e5b0b5048dcdb`  
		Last Modified: Thu, 11 Jan 2024 00:13:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:d20e9002675244162fdaf77d022444958c1a6d56dfe5901853240c568aea24b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 KB (96397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e870214daaeaabaf116e4a0a6462f63bc3d9ce9cd3d522277e53ba1d9c19a54e`

```dockerfile
```

-	Layers:
	-	`sha256:54016ce6ca1c0550269f0db7f3fec4511d81bef96b3c0f41709d785c7cefa5d3`  
		Last Modified: Thu, 11 Jan 2024 00:13:42 GMT  
		Size: 77.0 KB (77025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28bbe767bea18a4ae8896d545c4083a8a7a41145031227bdf28474500598aa2f`  
		Last Modified: Thu, 11 Jan 2024 00:13:42 GMT  
		Size: 19.4 KB (19372 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.19` - linux; s390x

```console
$ docker pull memcached@sha256:53d0bdb491815057b9014ab30e95c68146d83accdc9d8d690e308e67e7f4eed5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4326665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b078f3aede6257187e9488318eac328332ace90ac171c8a99d0ca495e1e9ad40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 08 Dec 2023 01:41:50 GMT
ADD file:47e0982fc3ae485c06d46f3c0022afd39ed7ec95fe755c2391e6b0cfcae65dfc in / 
# Fri, 08 Dec 2023 01:41:51 GMT
CMD ["/bin/sh"]
# Sat, 09 Dec 2023 01:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 09 Dec 2023 01:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 09 Dec 2023 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.22
# Sat, 09 Dec 2023 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.22.tar.gz
# Sat, 09 Dec 2023 01:54:10 GMT
ENV MEMCACHED_SHA1=7a691f390d59616dbebfc9e2e4942d499c39a338
# Sat, 09 Dec 2023 01:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 09 Dec 2023 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 09 Dec 2023 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 09 Dec 2023 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 09 Dec 2023 01:54:10 GMT
USER memcache
# Sat, 09 Dec 2023 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 09 Dec 2023 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0fca3ee44ced87b7184bc23390283fdf10cfae0e844a25b785dd11c463815227`  
		Last Modified: Fri, 08 Dec 2023 01:42:30 GMT  
		Size: 3.2 MB (3242332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff601679be7ba19260a77b326cf587dcc37315b02c2e0b0effc7084da4684bd7`  
		Last Modified: Wed, 13 Dec 2023 00:39:43 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b2401b35befb0832d96cebfdee6215736b27c0e3d064d67da9917deca4c14c`  
		Last Modified: Wed, 13 Dec 2023 00:39:43 GMT  
		Size: 113.1 KB (113142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59b1e1447b7739e5338731014a96bea369258cbf54b2d152ef50bb06e308bad`  
		Last Modified: Wed, 13 Dec 2023 00:39:43 GMT  
		Size: 969.5 KB (969547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c62bb151b09d73f2bc083bb91abedfb6660c5045d34f7d576415190ae4e09f`  
		Last Modified: Wed, 13 Dec 2023 00:39:43 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaaf7e6dbf7fbf661d0b3f6f5d38fbd888ab6707a76919a5f4a633194e895a2f`  
		Last Modified: Wed, 13 Dec 2023 00:39:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:1c2ba4c72ac494072ca8249e1368c9974cec5e63ff363b9da79930b7a8fbb5cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.3 KB (96269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c33c986fa5bcf287e1c7594cc4bc4b13289d51ef15c3db591e513fcb7b653ce`

```dockerfile
```

-	Layers:
	-	`sha256:358b294b5bd4c90ab3ded38657baddb4cf8a5d594c5ea9c5683191efc2c70e05`  
		Last Modified: Wed, 13 Dec 2023 00:39:43 GMT  
		Size: 77.0 KB (76967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:708c671c1199a85cfb58a91ad4f1c34c29d381f2905468f64a42c8fbb6341e30`  
		Last Modified: Wed, 13 Dec 2023 00:39:43 GMT  
		Size: 19.3 KB (19302 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:bookworm`

```console
$ docker pull memcached@sha256:59161db99b459a9315bbb8c52a243251d3cfcdb17f35a7900da8e5e64f0a8f32
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
$ docker pull memcached@sha256:643a24a57407d3cb2b8745f47a8d4b20406c19f5399ecb05db9727447637003a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38789237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d474793fb4125ae857b42efbf79eb1cbea8834a20e5d65627ea439b52b57313`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:27 GMT
ADD file:ac3cd70031d35e46d86b876934946ffc8756de4de065fbc926dce642dac07ff3 in / 
# Tue, 19 Dec 2023 01:20:28 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:af107e978371b6cd6339127a05502c5eacd1e6b0e9eb7b2f4aa7b6fc87e2dd81`  
		Last Modified: Tue, 19 Dec 2023 01:24:59 GMT  
		Size: 29.1 MB (29125963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d32ccca352404a5a8dedb6a7ca281abbc073b9d8643ef4626873ee1b8a204b1`  
		Last Modified: Wed, 10 Jan 2024 23:58:24 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d585b71055b9f919875cf91a81370309c971aad943e53b8c9fda2b63521f873`  
		Last Modified: Wed, 10 Jan 2024 23:58:25 GMT  
		Size: 2.5 MB (2488298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc47ad75df3e3af04459ae59b5c7ec1ea8dd657b7fb4cc42ec85a982a98da628`  
		Last Modified: Wed, 10 Jan 2024 23:58:25 GMT  
		Size: 7.2 MB (7173458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66204efbd683596758bec893cba01fce3fe386da63399af101051d8df26c2477`  
		Last Modified: Wed, 10 Jan 2024 23:58:25 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3406bc9285b7e906c211fd9a5d9342ee80d9e0ae728a6529d14db42aecf145`  
		Last Modified: Wed, 10 Jan 2024 23:58:25 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:8efa487487fc160476637a4fb2aec45b4a38eb677aeddcd0ecaeab362e136e85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3077977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:928c59acdba2c812e1299dcb8c4a4c7a7bdfadbc695533aab940957913a8b768`

```dockerfile
```

-	Layers:
	-	`sha256:7777c14054a0e9893c312cf26a23d80bb2f16d3cd6dacad21c21c8fb1be321a4`  
		Last Modified: Wed, 10 Jan 2024 23:58:25 GMT  
		Size: 3.1 MB (3056860 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc8d2dbb4d2d164636bb06f04252d4aec50002cf7469a8955e322e104563d025`  
		Last Modified: Wed, 10 Jan 2024 23:58:24 GMT  
		Size: 21.1 KB (21117 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; arm variant v5

```console
$ docker pull memcached@sha256:d01aca5f5e26f687d6ad14ec6547e704f453acc02ce0ce2e5fa5871f5013bfbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34811390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f12a90da675230d99a32d19f573412751d7740cae5f90d74a8c49b4b6f64a3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 19 Dec 2023 01:55:22 GMT
ADD file:9503ab966c9dd707eeccc7c2f633bccc94c199f8714ec4ff2c8b54dde3dbabf9 in / 
# Tue, 19 Dec 2023 01:55:22 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1ae9a2844c8c70942d2220553689b62e841cc706d77284fbfedbd770080fd699`  
		Last Modified: Tue, 19 Dec 2023 01:58:33 GMT  
		Size: 26.9 MB (26885440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ab650f4c7d61856342d3b0e4d9bad9cd0c4336fb403dab9c5c1ed2c285774f`  
		Last Modified: Thu, 11 Jan 2024 00:07:53 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b10807a0745d6e1ccc36157b11a3469a17c6477eda65233bb2f182c7958db5b8`  
		Last Modified: Thu, 11 Jan 2024 00:07:54 GMT  
		Size: 2.1 MB (2089356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5bc9bbfb0a70ce84a09ce58d70ebf97841c03e06d3968f065cd9361bd0e990`  
		Last Modified: Thu, 11 Jan 2024 00:07:54 GMT  
		Size: 5.8 MB (5835079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74b3373a0a7639196238720db6061026ccfe87c48ccf38fcfbc737699c9f2b7`  
		Last Modified: Thu, 11 Jan 2024 00:07:53 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3969d1f7528c0ba1d0047402bf5611d53c8f502f52fbbd7fb827f8de5ab813f6`  
		Last Modified: Thu, 11 Jan 2024 00:07:54 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:7484a951008b8e170922f1467a179c839a675cf4ab9555315f6bb20174be8173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3052683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d85ee8bbb3867fa9cbdd5e06e5791b62e1c7dfc410295ba05b95ead8b6c4525`

```dockerfile
```

-	Layers:
	-	`sha256:34e791a9d4149137cb6b8da59558d4bf4ce80c9bcd5ab599785c7a3aaa2fc844`  
		Last Modified: Thu, 11 Jan 2024 00:07:54 GMT  
		Size: 3.0 MB (3031592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31263ce608cc2e18001c08b34ad8f21b27befcf21ee30dd42bd87176f24a5e10`  
		Last Modified: Thu, 11 Jan 2024 00:07:53 GMT  
		Size: 21.1 KB (21091 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:1b119620b1cbaac4281975bedfed15ff721d868ec9eda9574dc4c1ec58330716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37686962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45b76a80b62f56ff1c68ed4e7ce2dfe225b3560e00750a3210c8d897b1547f3a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:11 GMT
ADD file:262fd7bf0bc26e5d2a229fba52626e22b8a93beac29733acfc60e716c26e689d in / 
# Tue, 19 Dec 2023 01:41:11 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:24e221e92a36ab5b0075dd156b4f2ff095532a9b0927946cf6070bb1bea208b8`  
		Last Modified: Tue, 19 Dec 2023 01:44:38 GMT  
		Size: 29.2 MB (29157269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d79fe3da079136cc418087e5d4e432357c062519668a3c03b78c24710c3a6ec`  
		Last Modified: Wed, 20 Dec 2023 10:20:11 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:496388416e6f8cdbf05e6ea4a56e906308e4b95b9f984f73b5c5a3fdbe5b12aa`  
		Last Modified: Wed, 20 Dec 2023 10:20:11 GMT  
		Size: 2.3 MB (2346023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee91bf234e7544eb6ad4c5f18ba87a8c0306d87f51ee1c47b1361569175a8a7c`  
		Last Modified: Thu, 11 Jan 2024 00:20:26 GMT  
		Size: 6.2 MB (6182151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73888be7ca392dfe14270a838c67a2d7ccfe9354f1fe52147291c9756127b51`  
		Last Modified: Thu, 11 Jan 2024 00:20:25 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a917a1ebe539f36501d4bebb89957491c647a119a1702734b1a0c9c01dc2a6`  
		Last Modified: Thu, 11 Jan 2024 00:20:25 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:f96d1dde1233068de191226772289ac63a784a466d34ec1dbf67e72559643f7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3053019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f249bf848fae6f5b573dffd3d8dbd830fd3267c6f487d397fd82ba104fee46b`

```dockerfile
```

-	Layers:
	-	`sha256:09c490b7c5d08149f654887eca9ca058a49a3b659d3e7282589a431883445a49`  
		Last Modified: Thu, 11 Jan 2024 00:20:25 GMT  
		Size: 3.0 MB (3032051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abe3c6e55476a176987bc5b5f8bad00ca16d1299d36e40f52e82dcb76ed0600c`  
		Last Modified: Thu, 11 Jan 2024 00:20:25 GMT  
		Size: 21.0 KB (20968 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; 386

```console
$ docker pull memcached@sha256:a5d93bfce917e364c0f16cdad7b683a36011a997db4be6db2770644095aea01d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39272936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:902b98d31b0a747e1d90226bbd3f7fb16592c8f606009585e9b2bbb819bfb30e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 19 Dec 2023 01:39:07 GMT
ADD file:6f4083d57ea9644b5a827e67b0725087a15aa428272ec223ab968bf8b4623e42 in / 
# Tue, 19 Dec 2023 01:39:07 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8d4aad22fb6a12b8cc7a78d338dfb9bc2bd6d621517b374e446f2915833ea883`  
		Last Modified: Tue, 19 Dec 2023 01:43:45 GMT  
		Size: 30.1 MB (30143863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22ddf2b3cd1581c8f1483d20c8fb232852e525fea04a97ffd9ac744939dffc0`  
		Last Modified: Wed, 10 Jan 2024 23:58:29 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23537023da95e2b44ae9e7aebee71e05ecb397f02a351f30f6c69a752d98d1a5`  
		Last Modified: Wed, 10 Jan 2024 23:58:29 GMT  
		Size: 2.5 MB (2492560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8636f3d8b77edac77347698b78afe5ce4f443daa01f0a424d809c8ed35405ac5`  
		Last Modified: Wed, 10 Jan 2024 23:58:29 GMT  
		Size: 6.6 MB (6634994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41afb4f2ebc199845ca27aae99895e43658c24f7fbdea6a0b17769f1fd238b3f`  
		Last Modified: Wed, 10 Jan 2024 23:58:29 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aee346987d8e42b5a7c3ecdc4b2efa5e402c43f65712c94e3f30606c9b365e4`  
		Last Modified: Wed, 10 Jan 2024 23:58:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:71cbd1b0df460e30d13a768ed26659ea3d35001b788219b4eac0d77078e71ab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3072225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7173243e71de72bb179738a15514dee35cfb9c1f1ab3da05adc2fd1ea74335cf`

```dockerfile
```

-	Layers:
	-	`sha256:4e2e18fc597957c9c8202a8015176e35b070a14ec422ca3b88fdfaa64cd693d0`  
		Last Modified: Wed, 10 Jan 2024 23:58:29 GMT  
		Size: 3.1 MB (3051163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1dc46fbcfd7dddfe981ea410938185ededc5f8f383164b2ffe266c923d1e7ed`  
		Last Modified: Wed, 10 Jan 2024 23:58:29 GMT  
		Size: 21.1 KB (21062 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; mips64le

```console
$ docker pull memcached@sha256:d6b10482cd93239feb732ab9b3bcdd207e5be672b55c01b1faa72c6e10da9ee3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37564394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bed0ab2d751422f3dfcd94712006ab27d4cdd43e18f83b8b38199c2cee3b2514`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 19 Dec 2023 02:13:36 GMT
ADD file:dcd5696ac281b24df52a518e2402c7f7a4caedfcba0d82e195b7c06cd3a38fdd in / 
# Tue, 19 Dec 2023 02:13:40 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:12b1322ffb17b8e81ca1c6d9d7118e2fcee0b9d971aa3c90601e6345804a60d1`  
		Last Modified: Tue, 19 Dec 2023 02:24:36 GMT  
		Size: 29.1 MB (29121427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6b93f134841b66512a1d4138bdf28b0506ffd27490aac735508b3f20716618`  
		Last Modified: Thu, 11 Jan 2024 00:10:54 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573e69b5f2977543c86d4410256c381ef97d7f37a89be2a88bfbda683c24110e`  
		Last Modified: Thu, 11 Jan 2024 00:10:55 GMT  
		Size: 1.9 MB (1937514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb552cccf8bd4122265e6895c4c9ce039b90dd08574f0e4911a0b11aaf1f7b2c`  
		Last Modified: Thu, 11 Jan 2024 00:10:55 GMT  
		Size: 6.5 MB (6503938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b640b85282363650ba7d87fea47ce2e4cfe96da07ab6c4b47eebc739f96910`  
		Last Modified: Thu, 11 Jan 2024 00:10:54 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933eef8a1d4865a3e302557839a52d00229ef80652113710df9fd606880475c5`  
		Last Modified: Thu, 11 Jan 2024 00:10:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:c1162ead1e62fcd87632e902387935d8f33b794c009815419baf8cb396548f85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aa26ec0ff6dd44911a88c2d2af479e0c05cfb46e9db65187abe71da51f56001`

```dockerfile
```

-	Layers:
	-	`sha256:2454765cb79a60d22f96ec7e66ea9fb222b40c30758e0df9a59c7192c39847da`  
		Last Modified: Thu, 11 Jan 2024 00:10:54 GMT  
		Size: 20.8 KB (20837 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; ppc64le

```console
$ docker pull memcached@sha256:b7976b1191a4f34442e257f55f30f8b4efd28f5f8026936846e8a5471e0c8505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.0 MB (43007490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75346431bfc757a49f790022140e267e0e6838110c75cad2bf8ab9e24e2855fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 19 Dec 2023 01:21:50 GMT
ADD file:ca1db68689e0b0388337ba450ad2c8e79c159c6b78f5aa6d3ff2b89b8d7edc93 in / 
# Tue, 19 Dec 2023 01:21:51 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fc9b8f5eec3aa37ab3aace05165427479352f290d53904cea87dca6349633a09`  
		Last Modified: Tue, 19 Dec 2023 01:26:19 GMT  
		Size: 33.1 MB (33120558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f85ae146a90d1ce7561d4e67d1ce2eaf0a0da444bb8a70c5b7fc94d0dc75e389`  
		Last Modified: Wed, 20 Dec 2023 08:43:43 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23065e9a12cf130c31375986a9b4700b84f2539ccb4b47efe0f375f77938fc3`  
		Last Modified: Wed, 20 Dec 2023 08:43:44 GMT  
		Size: 2.7 MB (2698240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b8249b30995d06e02d41e31406a930c02163d057cd39ad2cb7f710df2f6c60`  
		Last Modified: Thu, 11 Jan 2024 00:10:31 GMT  
		Size: 7.2 MB (7187176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a238b8549095cec1619f8f38f82d1aeb50acdf094b2b611b1fb5c62da14635f`  
		Last Modified: Thu, 11 Jan 2024 00:10:31 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669f29d97099310deca355ff837c9885adea00bb9c6e460490904627b7a40e4b`  
		Last Modified: Thu, 11 Jan 2024 00:10:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:87bde9e8cd8d07c6306a9ef516b822eadb9669d79da8587f1ac892066646ad33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3066464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:034c7634fd9e3419a42aa94fb6c3c05bd8d951eaf75eef2fbd2e8d64150013ba`

```dockerfile
```

-	Layers:
	-	`sha256:0a90f178efc50a3500b5ee2dce72b560153f2b0ec4cc6e79aa940561e8d58590`  
		Last Modified: Thu, 11 Jan 2024 00:10:31 GMT  
		Size: 3.0 MB (3045446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35a907ae4a36d514f4ff1b8d97766c9a5166c6116bc026f627e4de4cc51111fe`  
		Last Modified: Thu, 11 Jan 2024 00:10:30 GMT  
		Size: 21.0 KB (21018 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:bookworm` - linux; s390x

```console
$ docker pull memcached@sha256:9110d0aec3fc0be39a13bfd7030a3d04f36e230034078de3b407ae883f3e3de2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35722087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aef7bb08b32c1c17f11984770392abcc11b268465af0e89884793edf6ec092dd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 04 Dec 2023 18:08:47 GMT
ADD file:f06f12fa5a93afc3a79ac4371d24b0a471a5a1818cf34c1d90004c8f410914b9 in / 
# Mon, 04 Dec 2023 18:08:47 GMT
CMD ["bash"]
# Mon, 04 Dec 2023 18:08:47 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 04 Dec 2023 18:08:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 04 Dec 2023 18:08:47 GMT
ENV MEMCACHED_VERSION=1.6.22
# Mon, 04 Dec 2023 18:08:47 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.22.tar.gz
# Mon, 04 Dec 2023 18:08:47 GMT
ENV MEMCACHED_SHA1=7a691f390d59616dbebfc9e2e4942d499c39a338
# Mon, 04 Dec 2023 18:08:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 04 Dec 2023 18:08:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 Dec 2023 18:08:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 04 Dec 2023 18:08:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 Dec 2023 18:08:47 GMT
USER memcache
# Mon, 04 Dec 2023 18:08:47 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 04 Dec 2023 18:08:47 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bc6b1888979d3ceb063da848b2034e980e2c2613642159c1e856550b79aa620c`  
		Last Modified: Tue, 19 Dec 2023 01:47:38 GMT  
		Size: 27.5 MB (27491874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b453a12051612cbbdca8ee1a3c9e8211ac636f53786a525b824574fff746cda`  
		Last Modified: Tue, 19 Dec 2023 15:38:14 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7903f8445b1bbbe476fd67c998f57a5289b3d4a9e65a1190e551b7c79083e65d`  
		Last Modified: Tue, 19 Dec 2023 15:38:15 GMT  
		Size: 2.2 MB (2152511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf54a1600c7ab496cf3e01f5ec34a3ae7dfbf25014ef90ec9c7b005aa3d887c`  
		Last Modified: Tue, 19 Dec 2023 15:38:14 GMT  
		Size: 6.1 MB (6076186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b446e4dc631c597d82b5e437bf342d8607d8a4ff3229d052f049bfbac270e2c6`  
		Last Modified: Tue, 19 Dec 2023 15:38:14 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee453ca29f8bbd4b452693cd9f2e2e1b7cff2fa139d7fc942de190d244ae6617`  
		Last Modified: Tue, 19 Dec 2023 15:38:15 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:bookworm` - unknown; unknown

```console
$ docker pull memcached@sha256:2fa3455fc28f5964cc39eaaadcfab8df0a8dd5552a08464b0f87cbc775addb70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3067351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddb3e50e2a70d6400f4ba5be3b4010e9a0f7770e69e2c1e1c599bf6224ed8ac8`

```dockerfile
```

-	Layers:
	-	`sha256:2dcfb5805d88251b9b79a3c0e144091f0dc62a366eddacb9d50aa89a825067ef`  
		Last Modified: Tue, 19 Dec 2023 15:38:14 GMT  
		Size: 3.0 MB (3046401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb52cc58a7fa498aa7b56431dbe3e004db5d4b028b724bc1f087b44c1baaa25c`  
		Last Modified: Tue, 19 Dec 2023 15:38:14 GMT  
		Size: 20.9 KB (20950 bytes)  
		MIME: application/vnd.in-toto+json

## `memcached:latest`

```console
$ docker pull memcached@sha256:fa6c8e150e7b7af5e6f05ad388bbf5f4f34925e17aef12fc494ffdef7b3911cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 15
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
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
$ docker pull memcached@sha256:643a24a57407d3cb2b8745f47a8d4b20406c19f5399ecb05db9727447637003a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38789237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d474793fb4125ae857b42efbf79eb1cbea8834a20e5d65627ea439b52b57313`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:27 GMT
ADD file:ac3cd70031d35e46d86b876934946ffc8756de4de065fbc926dce642dac07ff3 in / 
# Tue, 19 Dec 2023 01:20:28 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:af107e978371b6cd6339127a05502c5eacd1e6b0e9eb7b2f4aa7b6fc87e2dd81`  
		Last Modified: Tue, 19 Dec 2023 01:24:59 GMT  
		Size: 29.1 MB (29125963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d32ccca352404a5a8dedb6a7ca281abbc073b9d8643ef4626873ee1b8a204b1`  
		Last Modified: Wed, 10 Jan 2024 23:58:24 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d585b71055b9f919875cf91a81370309c971aad943e53b8c9fda2b63521f873`  
		Last Modified: Wed, 10 Jan 2024 23:58:25 GMT  
		Size: 2.5 MB (2488298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc47ad75df3e3af04459ae59b5c7ec1ea8dd657b7fb4cc42ec85a982a98da628`  
		Last Modified: Wed, 10 Jan 2024 23:58:25 GMT  
		Size: 7.2 MB (7173458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66204efbd683596758bec893cba01fce3fe386da63399af101051d8df26c2477`  
		Last Modified: Wed, 10 Jan 2024 23:58:25 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3406bc9285b7e906c211fd9a5d9342ee80d9e0ae728a6529d14db42aecf145`  
		Last Modified: Wed, 10 Jan 2024 23:58:25 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:8efa487487fc160476637a4fb2aec45b4a38eb677aeddcd0ecaeab362e136e85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3077977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:928c59acdba2c812e1299dcb8c4a4c7a7bdfadbc695533aab940957913a8b768`

```dockerfile
```

-	Layers:
	-	`sha256:7777c14054a0e9893c312cf26a23d80bb2f16d3cd6dacad21c21c8fb1be321a4`  
		Last Modified: Wed, 10 Jan 2024 23:58:25 GMT  
		Size: 3.1 MB (3056860 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc8d2dbb4d2d164636bb06f04252d4aec50002cf7469a8955e322e104563d025`  
		Last Modified: Wed, 10 Jan 2024 23:58:24 GMT  
		Size: 21.1 KB (21117 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm variant v5

```console
$ docker pull memcached@sha256:d01aca5f5e26f687d6ad14ec6547e704f453acc02ce0ce2e5fa5871f5013bfbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34811390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f12a90da675230d99a32d19f573412751d7740cae5f90d74a8c49b4b6f64a3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 19 Dec 2023 01:55:22 GMT
ADD file:9503ab966c9dd707eeccc7c2f633bccc94c199f8714ec4ff2c8b54dde3dbabf9 in / 
# Tue, 19 Dec 2023 01:55:22 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1ae9a2844c8c70942d2220553689b62e841cc706d77284fbfedbd770080fd699`  
		Last Modified: Tue, 19 Dec 2023 01:58:33 GMT  
		Size: 26.9 MB (26885440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ab650f4c7d61856342d3b0e4d9bad9cd0c4336fb403dab9c5c1ed2c285774f`  
		Last Modified: Thu, 11 Jan 2024 00:07:53 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b10807a0745d6e1ccc36157b11a3469a17c6477eda65233bb2f182c7958db5b8`  
		Last Modified: Thu, 11 Jan 2024 00:07:54 GMT  
		Size: 2.1 MB (2089356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5bc9bbfb0a70ce84a09ce58d70ebf97841c03e06d3968f065cd9361bd0e990`  
		Last Modified: Thu, 11 Jan 2024 00:07:54 GMT  
		Size: 5.8 MB (5835079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74b3373a0a7639196238720db6061026ccfe87c48ccf38fcfbc737699c9f2b7`  
		Last Modified: Thu, 11 Jan 2024 00:07:53 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3969d1f7528c0ba1d0047402bf5611d53c8f502f52fbbd7fb827f8de5ab813f6`  
		Last Modified: Thu, 11 Jan 2024 00:07:54 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:7484a951008b8e170922f1467a179c839a675cf4ab9555315f6bb20174be8173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3052683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d85ee8bbb3867fa9cbdd5e06e5791b62e1c7dfc410295ba05b95ead8b6c4525`

```dockerfile
```

-	Layers:
	-	`sha256:34e791a9d4149137cb6b8da59558d4bf4ce80c9bcd5ab599785c7a3aaa2fc844`  
		Last Modified: Thu, 11 Jan 2024 00:07:54 GMT  
		Size: 3.0 MB (3031592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31263ce608cc2e18001c08b34ad8f21b27befcf21ee30dd42bd87176f24a5e10`  
		Last Modified: Thu, 11 Jan 2024 00:07:53 GMT  
		Size: 21.1 KB (21091 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; arm variant v7

```console
$ docker pull memcached@sha256:2841be0a36134563966c09a6ed68b21053d20342ec8736cf92763c28077ead43
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28094215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cf74ffa940dd93988fc0beb6698c5796563c82a40b7dd668153969f64d2e6ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 09 Feb 2023 06:12:09 GMT
ADD file:5f1a343224e8486690bd90dd1e50c8d84b3d770c51bb6829544e5cf650c0419c in / 
# Thu, 09 Feb 2023 06:12:10 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 07:52:31 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Thu, 09 Feb 2023 07:52:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 07:52:35 GMT
ENV MEMCACHED_VERSION=1.6.18
# Thu, 09 Feb 2023 07:52:35 GMT
ENV MEMCACHED_SHA1=be16909bb75ab972ee5fe438312501de01c4725a
# Thu, 09 Feb 2023 07:55:44 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& nproc="$(nproc)" 	&& make -j "$nproc" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test PARALLEL="$nproc" 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 		&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Thu, 09 Feb 2023 07:55:44 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 09 Feb 2023 07:55:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 09 Feb 2023 07:55:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Feb 2023 07:55:44 GMT
USER memcache
# Thu, 09 Feb 2023 07:55:45 GMT
EXPOSE 11211
# Thu, 09 Feb 2023 07:55:45 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:e7318f6106ad75d7d482ae9dddf4d927b0872ef3ddb6e1330aa691fc8d17279e`  
		Last Modified: Thu, 09 Feb 2023 06:19:19 GMT  
		Size: 26.6 MB (26577666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de49d9d72daf1680b5f1b9532dd2eb0162829f36c8db9669935462636fbf99d9`  
		Last Modified: Thu, 09 Feb 2023 08:06:11 GMT  
		Size: 4.9 KB (4895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0beac9d5bcac946f8c54c72b8a9c136914b1aa7a5fe2b8c3df4c7d8858ea6559`  
		Last Modified: Thu, 09 Feb 2023 08:06:11 GMT  
		Size: 312.1 KB (312088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4c9e5a265394e4c0f357779e6195a4e82d767a3691a0e77d427e56651c3e54a`  
		Last Modified: Thu, 09 Feb 2023 08:06:11 GMT  
		Size: 1.2 MB (1199163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ea82ad892fe1ae8623d84e32c8c027087cda8aa49e40d4546ed6942e471c60`  
		Last Modified: Thu, 09 Feb 2023 08:06:11 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2ae3bcdc0d114ba49a67df022b6f7215fc87f1f50e64939fcfbbec4eaadee5`  
		Last Modified: Thu, 09 Feb 2023 08:06:11 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:latest` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:1b119620b1cbaac4281975bedfed15ff721d868ec9eda9574dc4c1ec58330716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37686962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45b76a80b62f56ff1c68ed4e7ce2dfe225b3560e00750a3210c8d897b1547f3a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:11 GMT
ADD file:262fd7bf0bc26e5d2a229fba52626e22b8a93beac29733acfc60e716c26e689d in / 
# Tue, 19 Dec 2023 01:41:11 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:24e221e92a36ab5b0075dd156b4f2ff095532a9b0927946cf6070bb1bea208b8`  
		Last Modified: Tue, 19 Dec 2023 01:44:38 GMT  
		Size: 29.2 MB (29157269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d79fe3da079136cc418087e5d4e432357c062519668a3c03b78c24710c3a6ec`  
		Last Modified: Wed, 20 Dec 2023 10:20:11 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:496388416e6f8cdbf05e6ea4a56e906308e4b95b9f984f73b5c5a3fdbe5b12aa`  
		Last Modified: Wed, 20 Dec 2023 10:20:11 GMT  
		Size: 2.3 MB (2346023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee91bf234e7544eb6ad4c5f18ba87a8c0306d87f51ee1c47b1361569175a8a7c`  
		Last Modified: Thu, 11 Jan 2024 00:20:26 GMT  
		Size: 6.2 MB (6182151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73888be7ca392dfe14270a838c67a2d7ccfe9354f1fe52147291c9756127b51`  
		Last Modified: Thu, 11 Jan 2024 00:20:25 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a917a1ebe539f36501d4bebb89957491c647a119a1702734b1a0c9c01dc2a6`  
		Last Modified: Thu, 11 Jan 2024 00:20:25 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:f96d1dde1233068de191226772289ac63a784a466d34ec1dbf67e72559643f7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3053019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f249bf848fae6f5b573dffd3d8dbd830fd3267c6f487d397fd82ba104fee46b`

```dockerfile
```

-	Layers:
	-	`sha256:09c490b7c5d08149f654887eca9ca058a49a3b659d3e7282589a431883445a49`  
		Last Modified: Thu, 11 Jan 2024 00:20:25 GMT  
		Size: 3.0 MB (3032051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abe3c6e55476a176987bc5b5f8bad00ca16d1299d36e40f52e82dcb76ed0600c`  
		Last Modified: Thu, 11 Jan 2024 00:20:25 GMT  
		Size: 21.0 KB (20968 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; 386

```console
$ docker pull memcached@sha256:a5d93bfce917e364c0f16cdad7b683a36011a997db4be6db2770644095aea01d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39272936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:902b98d31b0a747e1d90226bbd3f7fb16592c8f606009585e9b2bbb819bfb30e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 19 Dec 2023 01:39:07 GMT
ADD file:6f4083d57ea9644b5a827e67b0725087a15aa428272ec223ab968bf8b4623e42 in / 
# Tue, 19 Dec 2023 01:39:07 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8d4aad22fb6a12b8cc7a78d338dfb9bc2bd6d621517b374e446f2915833ea883`  
		Last Modified: Tue, 19 Dec 2023 01:43:45 GMT  
		Size: 30.1 MB (30143863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22ddf2b3cd1581c8f1483d20c8fb232852e525fea04a97ffd9ac744939dffc0`  
		Last Modified: Wed, 10 Jan 2024 23:58:29 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23537023da95e2b44ae9e7aebee71e05ecb397f02a351f30f6c69a752d98d1a5`  
		Last Modified: Wed, 10 Jan 2024 23:58:29 GMT  
		Size: 2.5 MB (2492560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8636f3d8b77edac77347698b78afe5ce4f443daa01f0a424d809c8ed35405ac5`  
		Last Modified: Wed, 10 Jan 2024 23:58:29 GMT  
		Size: 6.6 MB (6634994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41afb4f2ebc199845ca27aae99895e43658c24f7fbdea6a0b17769f1fd238b3f`  
		Last Modified: Wed, 10 Jan 2024 23:58:29 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aee346987d8e42b5a7c3ecdc4b2efa5e402c43f65712c94e3f30606c9b365e4`  
		Last Modified: Wed, 10 Jan 2024 23:58:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:71cbd1b0df460e30d13a768ed26659ea3d35001b788219b4eac0d77078e71ab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3072225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7173243e71de72bb179738a15514dee35cfb9c1f1ab3da05adc2fd1ea74335cf`

```dockerfile
```

-	Layers:
	-	`sha256:4e2e18fc597957c9c8202a8015176e35b070a14ec422ca3b88fdfaa64cd693d0`  
		Last Modified: Wed, 10 Jan 2024 23:58:29 GMT  
		Size: 3.1 MB (3051163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1dc46fbcfd7dddfe981ea410938185ededc5f8f383164b2ffe266c923d1e7ed`  
		Last Modified: Wed, 10 Jan 2024 23:58:29 GMT  
		Size: 21.1 KB (21062 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; mips64le

```console
$ docker pull memcached@sha256:d6b10482cd93239feb732ab9b3bcdd207e5be672b55c01b1faa72c6e10da9ee3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37564394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bed0ab2d751422f3dfcd94712006ab27d4cdd43e18f83b8b38199c2cee3b2514`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 19 Dec 2023 02:13:36 GMT
ADD file:dcd5696ac281b24df52a518e2402c7f7a4caedfcba0d82e195b7c06cd3a38fdd in / 
# Tue, 19 Dec 2023 02:13:40 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:12b1322ffb17b8e81ca1c6d9d7118e2fcee0b9d971aa3c90601e6345804a60d1`  
		Last Modified: Tue, 19 Dec 2023 02:24:36 GMT  
		Size: 29.1 MB (29121427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6b93f134841b66512a1d4138bdf28b0506ffd27490aac735508b3f20716618`  
		Last Modified: Thu, 11 Jan 2024 00:10:54 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573e69b5f2977543c86d4410256c381ef97d7f37a89be2a88bfbda683c24110e`  
		Last Modified: Thu, 11 Jan 2024 00:10:55 GMT  
		Size: 1.9 MB (1937514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb552cccf8bd4122265e6895c4c9ce039b90dd08574f0e4911a0b11aaf1f7b2c`  
		Last Modified: Thu, 11 Jan 2024 00:10:55 GMT  
		Size: 6.5 MB (6503938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b640b85282363650ba7d87fea47ce2e4cfe96da07ab6c4b47eebc739f96910`  
		Last Modified: Thu, 11 Jan 2024 00:10:54 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933eef8a1d4865a3e302557839a52d00229ef80652113710df9fd606880475c5`  
		Last Modified: Thu, 11 Jan 2024 00:10:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:c1162ead1e62fcd87632e902387935d8f33b794c009815419baf8cb396548f85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aa26ec0ff6dd44911a88c2d2af479e0c05cfb46e9db65187abe71da51f56001`

```dockerfile
```

-	Layers:
	-	`sha256:2454765cb79a60d22f96ec7e66ea9fb222b40c30758e0df9a59c7192c39847da`  
		Last Modified: Thu, 11 Jan 2024 00:10:54 GMT  
		Size: 20.8 KB (20837 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; ppc64le

```console
$ docker pull memcached@sha256:b7976b1191a4f34442e257f55f30f8b4efd28f5f8026936846e8a5471e0c8505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.0 MB (43007490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75346431bfc757a49f790022140e267e0e6838110c75cad2bf8ab9e24e2855fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 19 Dec 2023 01:21:50 GMT
ADD file:ca1db68689e0b0388337ba450ad2c8e79c159c6b78f5aa6d3ff2b89b8d7edc93 in / 
# Tue, 19 Dec 2023 01:21:51 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.23
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.23.tar.gz
# Wed, 10 Jan 2024 01:54:10 GMT
ENV MEMCACHED_SHA1=d5490856170453b15a782ad55ffdea188c2eade0
# Wed, 10 Jan 2024 01:54:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 10 Jan 2024 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jan 2024 01:54:10 GMT
USER memcache
# Wed, 10 Jan 2024 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 10 Jan 2024 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:fc9b8f5eec3aa37ab3aace05165427479352f290d53904cea87dca6349633a09`  
		Last Modified: Tue, 19 Dec 2023 01:26:19 GMT  
		Size: 33.1 MB (33120558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f85ae146a90d1ce7561d4e67d1ce2eaf0a0da444bb8a70c5b7fc94d0dc75e389`  
		Last Modified: Wed, 20 Dec 2023 08:43:43 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23065e9a12cf130c31375986a9b4700b84f2539ccb4b47efe0f375f77938fc3`  
		Last Modified: Wed, 20 Dec 2023 08:43:44 GMT  
		Size: 2.7 MB (2698240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b8249b30995d06e02d41e31406a930c02163d057cd39ad2cb7f710df2f6c60`  
		Last Modified: Thu, 11 Jan 2024 00:10:31 GMT  
		Size: 7.2 MB (7187176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a238b8549095cec1619f8f38f82d1aeb50acdf094b2b611b1fb5c62da14635f`  
		Last Modified: Thu, 11 Jan 2024 00:10:31 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669f29d97099310deca355ff837c9885adea00bb9c6e460490904627b7a40e4b`  
		Last Modified: Thu, 11 Jan 2024 00:10:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:87bde9e8cd8d07c6306a9ef516b822eadb9669d79da8587f1ac892066646ad33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3066464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:034c7634fd9e3419a42aa94fb6c3c05bd8d951eaf75eef2fbd2e8d64150013ba`

```dockerfile
```

-	Layers:
	-	`sha256:0a90f178efc50a3500b5ee2dce72b560153f2b0ec4cc6e79aa940561e8d58590`  
		Last Modified: Thu, 11 Jan 2024 00:10:31 GMT  
		Size: 3.0 MB (3045446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35a907ae4a36d514f4ff1b8d97766c9a5166c6116bc026f627e4de4cc51111fe`  
		Last Modified: Thu, 11 Jan 2024 00:10:30 GMT  
		Size: 21.0 KB (21018 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:latest` - linux; s390x

```console
$ docker pull memcached@sha256:9110d0aec3fc0be39a13bfd7030a3d04f36e230034078de3b407ae883f3e3de2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35722087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aef7bb08b32c1c17f11984770392abcc11b268465af0e89884793edf6ec092dd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 04 Dec 2023 18:08:47 GMT
ADD file:f06f12fa5a93afc3a79ac4371d24b0a471a5a1818cf34c1d90004c8f410914b9 in / 
# Mon, 04 Dec 2023 18:08:47 GMT
CMD ["bash"]
# Mon, 04 Dec 2023 18:08:47 GMT
RUN set -eux; 	groupadd --system --gid 11211 memcache; 	useradd --system --gid memcache --uid 11211 memcache # buildkit
# Mon, 04 Dec 2023 18:08:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 04 Dec 2023 18:08:47 GMT
ENV MEMCACHED_VERSION=1.6.22
# Mon, 04 Dec 2023 18:08:47 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.22.tar.gz
# Mon, 04 Dec 2023 18:08:47 GMT
ENV MEMCACHED_SHA1=7a691f390d59616dbebfc9e2e4942d499c39a338
# Mon, 04 Dec 2023 18:08:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf; 	make test PARALLEL="$nproc"; 	mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		memcached -V # buildkit
# Mon, 04 Dec 2023 18:08:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 Dec 2023 18:08:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 04 Dec 2023 18:08:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 Dec 2023 18:08:47 GMT
USER memcache
# Mon, 04 Dec 2023 18:08:47 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 04 Dec 2023 18:08:47 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bc6b1888979d3ceb063da848b2034e980e2c2613642159c1e856550b79aa620c`  
		Last Modified: Tue, 19 Dec 2023 01:47:38 GMT  
		Size: 27.5 MB (27491874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b453a12051612cbbdca8ee1a3c9e8211ac636f53786a525b824574fff746cda`  
		Last Modified: Tue, 19 Dec 2023 15:38:14 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7903f8445b1bbbe476fd67c998f57a5289b3d4a9e65a1190e551b7c79083e65d`  
		Last Modified: Tue, 19 Dec 2023 15:38:15 GMT  
		Size: 2.2 MB (2152511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf54a1600c7ab496cf3e01f5ec34a3ae7dfbf25014ef90ec9c7b005aa3d887c`  
		Last Modified: Tue, 19 Dec 2023 15:38:14 GMT  
		Size: 6.1 MB (6076186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b446e4dc631c597d82b5e437bf342d8607d8a4ff3229d052f049bfbac270e2c6`  
		Last Modified: Tue, 19 Dec 2023 15:38:14 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee453ca29f8bbd4b452693cd9f2e2e1b7cff2fa139d7fc942de190d244ae6617`  
		Last Modified: Tue, 19 Dec 2023 15:38:15 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:latest` - unknown; unknown

```console
$ docker pull memcached@sha256:2fa3455fc28f5964cc39eaaadcfab8df0a8dd5552a08464b0f87cbc775addb70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3067351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddb3e50e2a70d6400f4ba5be3b4010e9a0f7770e69e2c1e1c599bf6224ed8ac8`

```dockerfile
```

-	Layers:
	-	`sha256:2dcfb5805d88251b9b79a3c0e144091f0dc62a366eddacb9d50aa89a825067ef`  
		Last Modified: Tue, 19 Dec 2023 15:38:14 GMT  
		Size: 3.0 MB (3046401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb52cc58a7fa498aa7b56431dbe3e004db5d4b028b724bc1f087b44c1baaa25c`  
		Last Modified: Tue, 19 Dec 2023 15:38:14 GMT  
		Size: 20.9 KB (20950 bytes)  
		MIME: application/vnd.in-toto+json
